---
id: "base-ui"
name: "Base UI"
url: "https://base-ui.com/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Next-Gen Headless Architecture", "CSS Native Starting-Style Transitions", "Pointer-Lock Scrub Interaction", "Decoupled Geometry & Visual Surface", "Zero-CloneElement Render Delegation"]
densidade_informacao: "Flexivel"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS/Headless)"
stack_frameworks: ["React 19", "React 18", "Next.js (App Router)", "@base-ui/react", "Tailwind CSS v4 & v3", "Floating UI", "TypeScript"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "Plus Jakarta Sans", "JetBrains Mono", "SF Pro", "IBM Plex Sans"]
  paletas_ideais: ["Deep Neutral Zinc / Slate", "High-Contrast Monochrome", "OKLCH Precision Hues", "Subtle Border Craft", "Dark Mode Obsidian"]
  combinacoes_recomendadas: ["Tailwind CSS v4", "Motion (Framer Motion)", "Lucide React", "shadcn/ui (Base UI port / ReUI)", "CVA (Class Variance Authority)"]
  conflitos_esteticos: ["Bibliotecas monolíticas com CSS opinativo acoplado (MUI clássico, Ant Design)", "Sistemas com animações fixas em JavaScript que bloqueiam a thread principal", "Estilos legados que sobrescrevem transform sem cascata de positioner"]
---

# Base UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Base UI** (`@base-ui/react`, outrora incubado como `@mui/base` e `@base-ui-components/react`) é a biblioteca de **componentes headless de nova geração para React** desenvolvida através de uma aliança histórica de engenheiros lendários do ecossistema front-end: **Colm Tuite** e **Vlad Moroz** (co-fundadores e criadores originais do **Radix UI**), **James Nelson** (@atomiks, criador e mantenedor do **Floating UI**) e a equipe central da **MUI** (liderada por Olivier Tassinari e Michail Karavitis).

Essa confluência de especialistas reuniu mais de duas décadas de aprendizados práticos na vanguarda da criação de bibliotecas de componentes para resolver os gargalos estruturais, limitações de performance e armadilhas ergonômicas que assolavam a geração anterior de componentes desestilizados (como o Radix UI v1 e o Headless UI).

```
┌────────────────────────────────────────────────────────────────────────┐
│                        BASE UI ARCHITECTURE                            │
├────────────────────────────────────────────────────────────────────────┤
│  Estética & Temas (Tailwind CSS v4 / CSS Modules / OKLCH Tokens)       │
├────────────────────────────────────────────────────────────────────────┤
│  Transições CSS Nativas (@starting-style / [data-starting-style])      │
├────────────────────────────────────────────────────────────────────────┤
│  Desacoplamento Geométrico: Positioner (Floating UI) vs. Popup (Visual)│
├────────────────────────────────────────────────────────────────────────┤
│  Render Delegation Direta: `render` prop (Zero React.cloneElement)     │
├────────────────────────────────────────────────────────────────────────┤
│  BASE UI CORE ENGINE (@base-ui/react — WAI-ARIA, Focus Trap, Scrub)   │
└────────────────────────────────────────────────────────────────────────┘
```

### A Filosofia Headless Pura & Desacoplamento Visual Absoluto
O Base UI não entrega nenhuma linha de estilo CSS opinativo por padrão. Ele fornece a fundação de **engenharia de software de interface**:
1. **Comportamento & Máquina de Estados**: Orquestração resiliente de aberturas, fechamentos, navegação em cascata e seleção única ou múltipla.
2. **Acessibilidade Rigorosa WAI-ARIA**: Gestão estrita de foco, ciclos de vida de diálogos modais (`role="dialog"` e `aria-modal="true"`), árvores semânticas (`aria-expanded`, `aria-controls`, `aria-activedescendant`) e navegação por teclado (roving tabindex e typeahead search).
3. **Ergonomia Tátil de Nível Desktop**: Inovações raras na web, como áreas de *scrub* numérico via Pointer Lock API (estilo Figma/Blender) e cartões de pré-visualização enriquecida com temporizadores calibrados de hover.

---

### Os Três Grandes Saltos Arquiteturais em Relação ao Radix UI

#### 1. Fim do `asChild` e Adoção do `render` Prop Sem `React.cloneElement`
No Radix UI, a delegação de renderização depende da prop booleana `asChild` combinada com o componente utilitário `Slot`. Esse mecanismo utiliza internamente `React.cloneElement` para fundir props, interceptar callbacks de evento e repassar refs para o filho direto. Embora elegante superficialmente, o `asChild` criou um poço de bugs notórios na indústria:
- **Erros Crípticos de Refs**: Conflitos entre `forwardRef`, componentes funcionais sem ref e nós de texto.
- **Sobrescrita Silenciosa de Handlers**: Eventos `onClick` ou `onKeyDown` perdidos ou executados fora de ordem quando múltiplos componentes envelopavam o mesmo elemento.
- **Incompatibilidade com Componentes Compostos**: Dificuldade extrema em compor múltiplos gatilhos sobre a mesma tag HTML sem gerar wrappers `<div>` intermediários que quebram layouts Flexbox ou Grid.

O Base UI baniu completamente o `asChild` e o `React.cloneElement`, substituindo-os pelo poderoso e explícito **`render` prop**:

```tsx
// Substituição direta de elemento sem wrappers
<Menu.Trigger render={<button type="button" className="btn-trigger" />}>
  Abrir Opções
</Menu.Trigger>

// Composição cirúrgica entre duas primitivas Base UI
<Toolbar.Button render={<Menu.Trigger />} />

// Render function com exposição do estado interno e tipagem perfeita
<Popover.Positioner 
  render={(props, state) => (
    <div {...props} className={state.open ? 'is-active' : 'is-idle'}>
      {/* Conteúdo com acesso a props e estado */}
    </div>
  )} 
/>
```

O hook interno `useRender` do Base UI assegura que a fusão de props, merging de classNames e encadeamento de event listeners ocorram de forma previsível e auditável, permitindo inclusive invocar `event.preventBaseUIHandler()` para interromper a ação interna da biblioteca quando uma regra de negócio customizada exigir.

#### 2. Separação Cirúrgica de Geometria: `Positioner` vs. `Popup`
Um dos maiores pesadelos ao animar menus, popovers e tooltips no Radix UI ou em bibliotecas tradicionais é o conflito de transformações CSS: bibliotecas de posicionamento (como Floating UI ou Popper.js) utilizam `transform: translate3d(x, y, 0)` para posicionar o elemento ancorado na tela. Quando o desenvolvedor tenta aplicar uma animação de escala (`transform: scale(0.95) -> scale(1)`) na mesma camada, o CSS sobrescreve o posicionamento tridimensional, fazendo o popup voar subitamente para o canto superior esquerdo da tela (`(0, 0)`).

O Base UI resolveu esse problema na raiz através da arquitetura de **dois nós desacoplados**:
- **`<Component.Positioner>`**: Assume 100% da responsabilidade matemática do `@floating-ui/react`. Ele aplica as coordenadas de viewport, detecção de colisões (`flip`, `shift`), alinhamento, virtual anchors e rastreamento de cursor.
- **`<Component.Popup>`**: É a casca visual interna estritamente desprovida de matemática de tela. Nela o desenvolvedor aplica livremente opacidade, sombras, bordas, filtros de backdrop e **escalas/rotações tridimensionais** sem nenhum risco de quebrar o posicionamento do elemento âncora!

Além disso, o Base UI calcula e injeta dinamicamente a variável CSS `--transform-origin` no Positioner baseando-se no lado de acoplamento (`top`, `bottom`, `left`, `right`), permitindo que a animação de escala se origine exatamente da ponta da seta (`Arrow`).

#### 3. Paradigma de Transição CSS Nativa com `@starting-style`, `[data-starting-style]` e `[data-ending-style]`
Historicamente, criar animações de saída (*exit animations*) fluidas no React exigia manter elementos no DOM via JavaScript com bibliotecas pesadas (como `framer-motion` com `<AnimatePresence>`) ou hacks frágeis com `setTimeout` e medição de `transitionend`. Se o usuário cancelasse a interação no meio do caminho (abrindo e fechando repetidamente um menu), as animações travavam ou davam saltos bruscos.

O Base UI alinha-se aos novos padrões da especificação CSS (CSS Transitions Level 2 e CSS Toggles):
- **Montagem Sem JS Lag**: Ao montar o elemento, o Base UI atribui o atributo `[data-starting-style]` (espelhando a regra CSS `@starting-style`).
- **Transição de Entrada Suave**: O navegador transiciona naturalmente as propriedades declaradas do estado inicial para o estado aberto padrão.
- **Cancelamento Suave de Transição (Smooth Interruption)**: Se o usuário fechar o popover no milissegundo 50 de uma animação de 200ms, o Base UI aplica `[data-ending-style]` e o motor nativo do navegador reverte a interpolação imediatamente de onde ela estava, sem reiniciar nem dar "glitch".
- **Desmontagem Limpa**: O Base UI monitora os eventos `transitionend` e `animationend` no DOM e apenas remove o elemento da árvore quando a transição CSS é concluída.

```css
/* Exemplo de CSS puro no Base UI */
.my-popup {
  transition: opacity 150ms cubic-bezier(0.16, 1, 0.3, 1), 
              transform 150ms cubic-bezier(0.16, 1, 0.3, 1);
  opacity: 1;
  transform: scale(1);
}

/* Estado de partida na montagem E estado de chegada no fechamento */
.my-popup[data-starting-style],
.my-popup[data-ending-style] {
  opacity: 0;
  transform: scale(0.96);
}
```

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **Ferramentas de Criação, Design & Editores Visuais (Canvas / WebGL / Node-based)**:
   - Aplicações no nível de Figma, Spline, Blender Web, Webflow, Rive e Canva. O componente `NumberField` com Pointer Lock Scrub Area permite controle fluido de propriedades (opacidade, largura, rotação, zoom) arrastando o cursor sem limites de tela.
2. **SaaS B2B de Alta Densidade e Engenharia (DevTools / Cloud Platforms)**:
   - Ambientes como Vercel, Supabase, Neon, Cloudflare e GitHub Enterprise. O Base UI suporta milhares de instâncias de nós com sobrecarga de renderização mínima e conformidade irrestrita com normas WCAG 2.2 AAA.
3. **Fintechs, Trading Desks & Criptoanalytics**:
   - Dashboards financeiros que demandam manipulação intensiva de campos numéricos, formatação monetária automatizada via `Intl.NumberFormat`, seleção precisa de datas e menus de contexto aninhados ultra-rápidos.
4. **Design Systems Corporativos Multi-Marca (Multi-Tenant DS)**:
   - Plataformas globais que precisam de uma única espinha dorsal headless e acessível, onde diferentes marcas consomem os mesmos componentes aplicando tokens Tailwind distintos ou CSS Modules independentes.

### Momento do Fluxo na Regra 60-30-10
- **Como Espinha Dorsal (60%)**: O Base UI deve ser adotado como a **camada universal de primitivas** de todo o design system (Buttons, Fields, Inputs, Checkboxes, Dialogs, Menus, Selects e Tabs).
- **Como Camada de Fluidez (30%)**: Orquestração geométrica de camadas flutuantes (Popovers, Tooltips, Context Menus, Navigation Menus e Drawers) aproveitando a integração embutida com Floating UI.
- **Como Microinteração Protagonista / Showstopper (10%)**: Utilização de `NumberField.ScrubArea` com cursor infinito em painéis de ajuste de parâmetros e `PreviewCard` com delay configurável para visualização de metadados em grafos ou feeds.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Projetos "Out-of-the-Box" com Prazo Relâmpago (MVPs de 24h)**: Se você não tem tempo para estilizar do zero nem possui um tema Tailwind pré-configurado, usar o Base UI é contraproducente. Bibliotecas opinativas com CSS pronto (como DaisyUI, HeroUI ou shadcn pronto) entregam uma interface funcional mais rápido.
- **Websites 100% Estáticos e Content-Heavy sem Interações Ricas**: Landing pages puramente textuais, blogs simples ou portfólios institucionais sem modais ou formulários complexos não necessitam de máquinas de estado WAI-ARIA completas.
- **Aplicações Legadas com JQuery ou Estilos Globais Invasivos**: Ambientes com seletores CSS genéricos como `button { transform: ... !important; }` que desrespeitam o isolamento de classes do Tailwind e conflitam com as regras internas do Positioner.

### ⚠️ Erros Comuns de Exagero e Implementação:
1. **Aplicar Escala e Rotação no `Positioner` em vez de no `Popup`**: O erro mais destrutivo. O `Positioner` deve permanecer intocado pelo desenvolvedor no que tange a propriedades de transformação visual. Todas as classes de transição (`transition-all`, `scale-95`, etc.) pertencem exclusivamente ao `<Popup>`.
2. **Misturar Mentalidade `asChild` com `render`**: Tentar importar `Slot` do Radix UI ou passar tags como filhos com props mágicas. No Base UI, use sempre a prop explícita `render={<minhaTag />}` ou funções render `render={(props) => <div {...props} />}`.
3. **Esquecer o Atributo `[data-ending-style]` em Animações CSS**: Se você declarar apenas `[data-starting-style]` para entrada, o componente desaparecerá instantaneamente no fechamento sem animação de saída. Sempre estilize ambos ou use a regra `@starting-style` combinada.
4. **Acoplar Bibliotecas de Animação Pesadas sem Necessidade**: Adicionar Framer Motion ou GSAP para um simples fade/scale de dropdown é desperdício de runtime. O Base UI foi projetado expressamente para tornar transições CSS nativas 100% completas e resilientes.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

### 1. Number Field (Com ScrubArea & Pointer Lock API)
- **Anatomia Visual**: Composto por `<NumberField.Root>`, `<NumberField.ScrubArea>`, `<NumberField.ScrubAreaCursor>`, `<NumberField.Group>`, `<NumberField.Decrement>`, `<NumberField.Input>` e `<NumberField.Increment>`. O ScrubArea costuma envelopar a label do campo.
- **Gatilho de Interação**:
  - *Click & Drag no ScrubArea*: Ativa a Pointer Lock API. O cursor padrão do mouse é ocultado ou substituído pelo cursor direcional, permitindo que o usuário arraste horizontalmente sem esbarrar nas bordas da tela.
  - *Shift + Drag / Alt + Drag*: Multiplicadores de sensibilidade (ex: incrementos de 10x ou 0.1x).
  - *Setas do Teclado*: Incremento e decremento acessível via teclado.
- **Onde Encaixar**: Painéis de controle de ferramentas SaaS, painéis de propriedades visuais (estilo Figma/Canva), inputs de trading, seletores de opacidade e dimensões.

### 2. Preview Card (Hover Card Rico)
- **Anatomia Visual**: `<PreviewCard.Root>`, `<PreviewCard.Trigger>`, `<PreviewCard.Portal>`, `<PreviewCard.Positioner>`, `<PreviewCard.Popup>`, `<PreviewCard.Arrow>`. Exibe um cartão suspenso rico com tipografia, avatares, dados de bio ou gráficos em miniatura.
- **Gatilho de Interação**: *Hover* sustentado com tempo de espera calibrado (`openDelay={300}`, `closeDelay={200}`). O ponteiro pode se mover do trigger para o interior do popup sem que ele se feche acidentalmente graças ao polígono de tolerância do Floating UI.
- **Onde Encaixar**: Menções de usuários (`@username`) em feeds e dashboards, links de repositórios em DevTools, previews de produtos em e-commerces B2B.

### 3. Popover (Arquitetura Positioner + Popup Desacoplada)
- **Anatomia Visual**: Separação clara entre a lógica espacial (`<Popover.Positioner>`) e a superfície cosmética (`<Popover.Popup>`). Suporta setas decorativas auto-alinhadas com `<Popover.Arrow>`.
- **Gatilho de Interação**: *Click* no `<Popover.Trigger>`. Fechamento automático com clique externo (*outside click*), tecla `Escape` ou scroll.
- **Onde Encaixar**: Filtros multidimensionais em tabelas de dashboards, seletores de cores, menus de compartilhamento rápido, mini-formulários de edição in-line.

### 4. Menu & Dropdown Menu (Cascata e Roving Tabindex)
- **Anatomia Visual**: `<Menu.Root>`, `<Menu.Trigger>`, `<Menu.Portal>`, `<Menu.Positioner>`, `<Menu.Popup>`, `<Menu.Item>`, `<Menu.Separator>`, `<Menu.Group>`, `<Menu.RadioGroup>`, `<Menu.CheckboxItem>`, `<Menu.SubmenuRoot>`.
- **Gatilho de Interação**: *Click* ou navegação por teclado (`Enter`, `Espaço`, setas verticais e horizontais para entrar/sair de submenus, digitação direta para *typeahead search*).
- **Onde Encaixar**: Menus de ações de linha em tabelas (três pontinhos), menus de conta de usuário no topo da navbar, menus de contexto acionados por botão direito.

### 5. Select & Combobox (Seleção Acessível com Typeahead)
- **Anatomia Visual**: `<Select.Root>`, `<Select.Trigger>`, `<Select.Value>`, `<Select.Portal>`, `<Select.Positioner>`, `<Select.Popup>`, `<Select.ScrollUpArrow>`, `<Select.ScrollDownArrow>`, `<Select.Item>`, `<Select.ItemText>`, `<Select.ItemIndicator>`.
- **Gatilho de Interação**: *Click* ou *Space/Enter* para abrir. Rastreamento de foco via setas, indicação visual com `data-highlighted` e rolagem automática de opções longas através dos Scroll Arrows.
- **Onde Encaixar**: Formulários corporativos, seletores de moeda/país, filtros globais de relatórios.

### 6. Dialog & Alert Dialog (Modal de Alta Resiliência)
- **Anatomia Visual**: `<Dialog.Root>`, `<Dialog.Trigger>`, `<Dialog.Portal>`, `<Dialog.Backdrop>`, `<Dialog.Popup>`, `<Dialog.Title>`, `<Dialog.Description>`, `<Dialog.Close>`.
- **Gatilho de Interação**: *Click* no trigger. Bloqueio automático do scroll da página de fundo (*scroll lock* sem trepidação de layout), armadilha de foco (*focus trap* rigoroso que impede o Tab de sair da janela) e restauração do foco no botão de origem após o fechamento.
- **Onde Encaixar**: Telas de confirmação crítica (exclusão de dados), formulários modais de criação rápida, fluxos de onboarding.

### 7. Collapsible & Accordion (Expansão sem Layout Shift)
- **Anatomia Visual**: `<Accordion.Root>`, `<Accordion.Item>`, `<Accordion.Header>`, `<Accordion.Trigger>`, `<Accordion.Panel>`.
- **Gatilho de Interação**: *Click* ou navegação por teclado com suporte a modo de seleção simples (`type="single"`) ou múltipla (`type="multiple"`). Animação de altura feita via CSS sem cálculos contínuos em JavaScript.
- **Onde Encaixar**: Seções de FAQ, painéis colapsáveis de navegação secundária em dashboards, visualizadores de parâmetros em formulários densos.

### 8. Field, Fieldset & Form (Sistema Nativo de Formulários)
- **Anatomia Visual**: `<Form>`, `<Fieldset.Root>`, `<Fieldset.Legend>`, `<Field.Root>`, `<Field.Label>`, `<Field.Control>`, `<Field.Description>`, `<Field.Error>`.
- **Gatilho de Interação**: Sincronização em tempo real com a Constraint Validation API nativa do HTML5. Estados `data-invalid`, `data-valid`, `data-touched` e `data-dirty` são refletidos no markup automaticamente, garantindo que leitores de tela anunciem mensagens de erro via `aria-describedby` e `aria-errormessage`.
- **Onde Encaixar**: Formulários de autenticação, telas de checkout, cadastros de configurações de sistema.

### 9. Tabs (Navegação em Abas com Indicador Dinâmico)
- **Anatomia Visual**: `<Tabs.Root>`, `<Tabs.List>`, `<Tabs.Tab>`, `<Tabs.Indicator>`, `<Tabs.Panel>`.
- **Gatilho de Interação**: Ativação automática ao focar (*automatic activation*) ou manual via *Click/Enter*. O `<Tabs.Indicator>` permite criar aquela barra deslizante suave que corre por baixo das abas ativas.
- **Onde Encaixar**: Navegação interna de páginas de configurações em SaaS, visualização de gráficos por período (Dia, Mês, Ano), alternância de linguagens em blocos de código.

### 10. Slider (Controle Deslizante Multi-Thumb)
- **Anatomia Visual**: `<Slider.Root>`, `<Slider.Control>`, `<Slider.Track>`, `<Slider.Indicator>`, `<Slider.Thumb>`. Suporta um ou múltiplos polegares (faixa de intervalo / min-max range).
- **Gatilho de Interação**: *Drag*, *Click no Track* com salto imediato ou proporcional, e ajuste por teclas direcionais (`ArrowLeft`, `ArrowRight`, `PageUp`, `PageDown`, `Home`, `End`).
- **Onde Encaixar**: Seleção de faixa de preço em e-commerce, ajuste de volume e brilho em reprodutores de mídia, controles de granularidade em filtros.

### 11. Switch & Checkbox (Controles Booleanos e Tri-State)
- **Anatomia Visual**: `<Switch.Root>`, `<Switch.Thumb>`, `<Checkbox.Root>`, `<Checkbox.Indicator>`.
- **Gatilho de Interação**: Alternância com suporte a estado indeterminado (*indeterminate/tri-state* para seletores de "selecionar tudo" em tabelas). Totalmente sincronizado com inputs ocultos para envio padrão de formulários.
- **Onde Encaixar**: Toggles de notificações em configurações de conta, seleção em lote de linhas em tabelas de dados.

### 12. Scroll Area (Substituição Ergonômica de Barra de Rolagem)
- **Anatomia Visual**: `<ScrollArea.Root>`, `<ScrollArea.Viewport>`, `<ScrollArea.Scrollbar>`, `<ScrollArea.Thumb>`, `<ScrollArea.Corner>`.
- **Gatilho de Interação**: Mantém 100% da física e aceleração nativa de rolagem do sistema operacional do usuário (trackpad, roda do mouse e touch), enquanto renderiza uma barra de rolagem minimalista que se oculta automaticamente (*auto-hide*) quando inativa.
- **Onde Encaixar**: Painéis laterais de navegação fixa, colunas de Kanban, caixas de código com rolagem horizontal e vertical.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

Instalação oficial do pacote central do Base UI via gerenciador de pacotes:

```bash
npm install @base-ui/react
# Utilitários complementares de classes e ícones
npm install clsx tailwind-merge lucide-react
```

> [!NOTE]
> Durante as versões de teste e transição histórica, o pacote utilizou os nomes `@mui/base` e `@base-ui-components/react`. O pacote de produção oficial e definitivo é **`@base-ui/react`**.

### Física de Movimento, CSS Transitions & Curvas Bezier
O Base UI opera com **CSS Transitions nativas** associadas aos atributos de dados `[data-starting-style]` e `[data-ending-style]`. 

Para obter a assinatura tátil do Base UI (fluida, firme e orgânica), utilize as seguintes curvas matemáticas:
- **Aberturas / Overlays (Entrada Suave)**: `cubic-bezier(0.16, 1, 0.3, 1)` (Duração: `150ms` a `200ms`).
- **Fechamentos / Retrações (Saída Ágil)**: `cubic-bezier(0.4, 0, 1, 1)` ou `ease-out` (Duração: `100ms` a `150ms`).
- **Scrub & Ajustes Contínuos**: Interpolação linear de 60fps sem amortecimento para garantir feedback imediato ao ponteiro do mouse.

---

### Receita 1: NumberField Completo com ScrubArea (Pointer Lock) & Tailwind CSS

Este componente reproduz o padrão do Figma: o usuário clica e arrasta sobre a legenda "Zoom" ou "Width" para alterar o valor numericamente sem barreiras físicas na tela.

```tsx
"use client";

import * as React from "react";
import { NumberField } from "@base-ui/react/number-field";
import { ChevronDown, ChevronUp, MoveHorizontal } from "lucide-react";

interface ScrubNumberInputProps {
  label: string;
  defaultValue?: number;
  min?: number;
  max?: number;
  step?: number;
  unit?: string;
}

export function ScrubNumberInput({
  label,
  defaultValue = 100,
  min = 0,
  max = 1000,
  step = 1,
  unit = "px",
}: ScrubNumberInputProps) {
  return (
    <NumberField.Root
      defaultValue={defaultValue}
      min={min}
      max={max}
      step={step}
      className="flex flex-col gap-1.5 font-sans"
    >
      <div className="flex items-center justify-between text-xs font-medium text-zinc-400">
        {/* ScrubArea: Área de arrasto interativa com Pointer Lock */}
        <NumberField.ScrubArea className="group flex cursor-ew-resize select-none items-center gap-1 text-zinc-300 hover:text-white transition-colors">
          <MoveHorizontal className="h-3 w-3 opacity-60 group-hover:opacity-100 transition-opacity" />
          <label className="cursor-ew-resize">{label}</label>
          <NumberField.ScrubAreaCursor className="drop-shadow-md">
            <span className="rounded bg-zinc-900 border border-zinc-700 px-1 py-0.5 text-[10px] text-zinc-200">
              Arrastar
            </span>
          </NumberField.ScrubAreaCursor>
        </NumberField.ScrubArea>

        {unit && <span className="text-[11px] text-zinc-500 uppercase">{unit}</span>}
      </div>

      {/* Grupo de input e botões de incremento/decremento */}
      <NumberField.Group className="relative flex items-center rounded-lg border border-zinc-800 bg-zinc-950/80 px-2.5 py-1.5 text-sm text-zinc-100 shadow-inner focus-within:border-zinc-500 focus-within:ring-1 focus-within:ring-zinc-500 transition-all">
        <NumberField.Input className="w-full bg-transparent font-mono text-sm tabular-nums outline-none text-zinc-100 placeholder:text-zinc-600" />
        
        <div className="flex flex-col -mr-1 pl-1 border-l border-zinc-800/80">
          <NumberField.Increment className="flex h-3.5 w-4 items-center justify-center rounded text-zinc-400 hover:bg-zinc-800 hover:text-zinc-100 active:scale-95 transition-all">
            <ChevronUp className="h-3 w-3" />
          </NumberField.Increment>
          <NumberField.Decrement className="flex h-3.5 w-4 items-center justify-center rounded text-zinc-400 hover:bg-zinc-800 hover:text-zinc-100 active:scale-95 transition-all">
            <ChevronDown className="h-3 w-3" />
          </NumberField.Decrement>
        </div>
      </NumberField.Group>
    </NumberField.Root>
  );
}
```

---

### Receita 2: Popover Acessível com Separação Positioner/Popup & Transições Nativas

Demonstra a eliminação de conflitos de `transform` e o uso dos atributos `[data-starting-style]` e `[data-ending-style]` para cancelamento suave de animações:

```tsx
"use client";

import * as React from "react";
import { Popover } from "@base-ui/react/popover";
import { Settings2, X } from "lucide-react";

export function SettingsPopover() {
  return (
    <Popover.Root>
      <Popover.Trigger
        render={
          <button
            type="button"
            className="inline-flex items-center gap-2 rounded-lg border border-zinc-800 bg-zinc-900 px-3.5 py-2 text-sm font-medium text-zinc-200 shadow-sm hover:bg-zinc-800 hover:text-white active:scale-98 transition-all"
          />
        }
      >
        <Settings2 className="h-4 w-4 text-zinc-400" />
        <span>Ajustes Rápidos</span>
      </Popover.Trigger>

      <Popover.Portal>
        {/* Positioner: Geometria espacial pura do Floating UI (Sem estilos visuais) */}
        <Popover.Positioner sideOffset={8} side="bottom" align="center">
          {/* Popup: Casca visual que recebe transformações, sombras e [data-*-style] */}
          <Popover.Popup className="w-72 rounded-xl border border-zinc-800 bg-zinc-950 p-4 text-zinc-100 shadow-2xl backdrop-blur-md outline-none transition-all duration-150 ease-[cubic-bezier(0.16,1,0.3,1)] data-[starting-style]:scale-95 data-[starting-style]:opacity-0 data-[ending-style]:scale-95 data-[ending-style]:opacity-0">
            <div className="flex items-center justify-between pb-3 border-b border-zinc-800/80">
              <h3 className="text-sm font-semibold text-white">Preferências</h3>
              <Popover.Close
                render={
                  <button
                    type="button"
                    className="rounded p-1 text-zinc-400 hover:bg-zinc-800 hover:text-zinc-200 transition-colors"
                  />
                }
              >
                <X className="h-3.5 w-3.5" />
              </Popover.Close>
            </div>

            <div className="py-3 text-xs text-zinc-400 flex flex-col gap-2">
              <label className="flex items-center justify-between">
                <span>Modo de Renderização</span>
                <span className="font-mono text-zinc-200 bg-zinc-900 px-1.5 py-0.5 rounded border border-zinc-800">
                  GPU WebGL
                </span>
              </label>
              <label className="flex items-center justify-between">
                <span>Aceleração de Ponteiro</span>
                <span className="text-emerald-400 font-medium">Ativa</span>
              </label>
            </div>

            {/* Seta posicional auto-alinhada */}
            <Popover.Arrow className="fill-zinc-950 stroke-zinc-800 stroke-[1px]" />
          </Popover.Popup>
        </Popover.Positioner>
      </Popover.Portal>
    </Popover.Root>
  );
}
```

---

### Receita 3: Field & Form com Validação HTML5 e Animação de Erro

Demonstra o casamento entre a validação semântica do browser e feedback acessível via `Field.Error`:

```tsx
"use client";

import * as React from "react";
import { Field } from "@base-ui/react/field";
import { AlertCircle } from "lucide-react";

export function AccessibleEmailField() {
  return (
    <Field.Root name="email" className="flex flex-col gap-1.5 w-full max-w-sm">
      <Field.Label className="text-xs font-medium text-zinc-300">
        E-mail de Trabalho
      </Field.Label>

      <Field.Control
        type="email"
        required
        placeholder="usuario@empresa.com"
        className="w-full rounded-lg border border-zinc-800 bg-zinc-950 px-3 py-2 text-sm text-zinc-100 placeholder:text-zinc-600 outline-none transition-all focus:border-zinc-400 focus:ring-1 focus:ring-zinc-400 data-[invalid]:border-rose-500/80 data-[invalid]:focus:ring-rose-500"
      />

      <Field.Description className="text-[11px] text-zinc-500">
        Utilize seu e-mail corporativo para acesso SSO.
      </Field.Description>

      {/* O Field.Error só entra no DOM quando o campo é inválido e transiciona suavemente */}
      <Field.Error className="flex items-center gap-1.5 text-xs text-rose-400 transition-all duration-150 data-[starting-style]:opacity-0 data-[starting-style]:-translate-y-1 data-[ending-style]:opacity-0">
        <AlertCircle className="h-3.5 w-3.5 shrink-0" />
        <span>Por favor, forneça um endereço de e-mail corporativo válido.</span>
      </Field.Error>
    </Field.Root>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar e integrar o **Base UI** em um projeto dentro do documento `DESIGN_BLUEPRINT.md`, a inteligência artificial e os arquitetos de software devem seguir as instruções normativas abaixo:

### Declaração Formal da Camada Primitiva
```markdown
### UI Primitive Architecture: Base UI (@base-ui/react)
- **Engine**: Headless Primitives com WAI-ARIA nativo e Floating UI geométrico.
- **Composition Standard**: Exclusivamente via prop `render` (Eliminado qualquer uso de `asChild` ou `Slot`).
- **Animation Strategy**: CSS Transitions nativas governadas por `[data-starting-style]` e `[data-ending-style]`.
```

### Regras Mandatórias de Estruturação
1. **Regra de Ouro dos Nós Flutuantes (Positioner vs. Popup)**:
   - Toda estrutura flutuante (Menu, Popover, Tooltip, Select, PreviewCard) DEVE ser envelopada sequencialmente por:
     `<Component.Root>` -> `<Component.Trigger>` -> `<Component.Portal>` -> `<Component.Positioner>` -> `<Component.Popup>`.
   - **NUNCA** aplique classes de transição (`transition`, `scale`, `opacity`, `backdrop-blur`) no `<Positioner>`. O `<Positioner>` deve conter apenas propriedades estruturais como `sideOffset`, `alignOffset`, `side` e `align`.
   - O `<Popup>` é o único detentor das classes cosméticas e transições.

2. **Convenção de Imports Padronizada**:
   - Utilize as subpastas diretas do pacote para tree-shaking cirúrgico:
     - `import { Popover } from '@base-ui/react/popover';`
     - `import { NumberField } from '@base-ui/react/number-field';`
     - `import { Menu } from '@base-ui/react/menu';`
     - `import { Dialog } from '@base-ui/react/dialog';`
     - `import { Field } from '@base-ui/react/field';`

3. **Checklist de Conformidade de Acessibilidade**:
   - Verifique sempre se botões com ícones possuem `aria-label` apropriado.
   - Sempre utilize `Field.Label` conectado aos controles de formulário para garantir anotação nativa no leitor de tela.
   - Utilize `NumberField.ScrubAreaCursor` para dar visibilidade ao usuário sobre a capacidade de arrasto contínuo.
