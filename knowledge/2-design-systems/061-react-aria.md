---
id: "react-aria"
name: "React Aria"
url: "https://www.react-aria.com/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Headless Engineering Core", "WAI-ARIA Gold Standard", "Enterprise Internationalization", "State-Driven Data Attributes", "Cross-Device Input Normalization"]
densidade_informacao: "Flexivel"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS/Headless)"
stack_frameworks: ["React 19 / 18", "Next.js (App Router)", "React Aria Components", "React Stately", "@internationalized/date", "@internationalized/number", "Tailwind CSS v4 & v3", "tailwindcss-react-aria-components"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "Plus Jakarta Sans", "JetBrains Mono", "IBM Plex Sans", "Roboto"]
  paletas_ideais: ["Adobe Spectrum Neutrals", "Zinc & Slate Monochromes", "OKLCH Modern Enterprise", "High-Contrast Accessible Themes", "Dark Craft Glassmorphism"]
  combinacoes_recomendadas: ["tailwindcss-react-aria-components", "HeroUI (NextUI)", "JollyUI", "Framer Motion", "Lucide React", "TanStack Table"]
  conflitos_esteticos: ["Bibliotecas com CSS monolitico de alta especificidade (!important)", "Frameworks de UI com manipulação direta e destrutiva do DOM", "Sistemas que forçam seletores legados de mouse (:hover puro sem fallback de toque)"]
---

# React Aria — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **React Aria** (e sua evolução direta, o **React Aria Components — RAC**), desenvolvido e mantido pela equipe da Adobe sob a liderança técnica de engenheiros como Devon Govett (criador do Parcel bundler), constitui o **padrão-ouro absoluto da indústria global de software** em engenharia de acessibilidade (WAI-ARIA), robustez de comportamento e suporte a internacionalização avançada para o ecossistema React.

Diferente de bibliotecas visuais opinativas que impõem temas cosméticos pré-definidos (como Material UI, Mantine ou Chakra UI), o React Aria opera sob a premissa do **desacoplamento total entre comportamento/acessibilidade e estilização cosmética** (*Headless Architecture*). A biblioteca assume 100% da responsabilidade sobre a matemática de interação, foco, semântica ARIA e normalização de hardware, entregando uma folha em branco para que times de produto construam design systems proprietários de altíssima fidelidade.

```
┌────────────────────────────────────────────────────────────────────────┐
│                   A ARQUITETURA EM 3 CAMADAS DA ADOBE                  │
├────────────────────────────────────────────────────────────────────────┤
│  CAMADA 3: React Aria Components (RAC)                                 │
│  Primitivas headless prontas (<Button>, <Select>, <Table>, <Modal>)   │
│  com Contexts implícitos, Slots de composição e Data Attributes        │
├────────────────────────────────────────────────────────────────────────┤
│  CAMADA 2: React Aria (Hooks Core)                                     │
│  usePress, useFocusRing, useTable, useDatePicker, useListBox           │
│  Normalização de ponteiro (mouse/touch/pen/screen-reader) e WAI-ARIA   │
├────────────────────────────────────────────────────────────────────────┤
│  CAMADA 1: React Stately (Máquinas de Estado Isomórficas)              │
│  useToggleState, useSelectState, useTableState, useDatePickerState     │
│  Estado puro sem nós DOM (agnóstico de plataforma / React Native)      │
└────────────────────────────────────────────────────────────────────────┘
```

### A Assinatura Técnica: Os Pilares Inimitáveis do React Aria

#### 1. Normalização de Entrada Multi-Dispositivo (`usePress` vs `onClick`)
O evento nativo `onClick` da Web é profundamente inconsistente em cenários corporativos:
- Em dispositivos móveis de toque, navegadores podem introduzir latências artificiais de até 300ms ou disparar eventos sintéticos duplicados.
- Leitores de tela (VoiceOver no iOS/macOS, NVDA e JAWS no Windows, TalkBack no Android) emitem eventos de clique virtual sem coordenadas físicas de tela.
- Se o usuário toca a tela, segura e arrasta o dedo para fora do botão (*scroll gesture*), um `onClick` ingênuo pode disparar indevidamente.

O hook central `usePress` do React Aria normaliza todas as matrizes de entrada:
- Detecta o início real do pressionamento (`onPressStart`), cancelamento por arrasto de rolagem (`onPressCancel`) e conclusão bem-sucedida (`onPressEnd`, `onPress`).
- Emula o estado ativo de botão (`data-pressed`) instantaneamente no toque, sem atraso perceptível de tela.
- Trata teclas espaciais (`Space`) e de confirmação (`Enter`) simulando cliques físicos e prevenindo o comportamento padrão de rolagem de página.

#### 2. Roteamento de Foco e Detecção Sem Heurísticas de Falha (`useFocusRing`)
A pseudo-classe CSS `:focus-visible` nativa apresenta inconsistências entre motores Chromium, WebKit e Gecko, especialmente em elementos que recebem foco programático ou após diálogos modais serem fechados.
O React Aria provê a primitiva `useFocusRing`, que monitora o último modo de interação (teclado vs. ponteiro de mouse/toque). O anel de foco só se manifesta (`data-focus-visible="true"`) quando a navegação é genuinamente orientada por teclado ou leitor de tela, mantendo a interface limpa e elegante para usuários de mouse sem jamais comprometer a conformidade legal WCAG 2.2 Nível AA/AAA.

#### 3. Motor Internacional de Calendários e Localização (`@internationalized/date`)
Enquanto a maioria das bibliotecas de UI assume o calendário Gregoriano e a formatação americana/europeia como padrão universal, o React Aria integra nativamente o pacote `@internationalized/date`:
- Suporta **13 calendários mundiais completos**: Gregoriano, Islâmico (Umm al-Qura, Civil, Tabular), Hebraico, Budista, Persa (Jalali), Indiano Nacional, Etíope, Copta e Japonês com eras imperiais.
- Gerencia o primeiro dia da semana de acordo com o código de localidade BCP 47 (ex: Domingo nos EUA, Segunda-feira no Brasil e União Europeia, Sábado no Oriente Médio).
- Sincronização automática com direção de texto Right-to-Left (RTL) para árabe, hebraico e persa, invertendo grades de calendário e eixos de sliders sem demandar estilos manuais duplicados.

#### 4. Arquitetura de Slots e Composição sem Prop-Drilling
No React Aria Components, componentes complexos são organizados como árvores de sub-componentes semânticos. Através de uma infraestrutura inteligente de React Contexts e *Slots*, tags filhas herdam automaticamente estados, IDs gerados e atributos de acessibilidade:

```tsx
<ComboBox>
  <Label>Provedor Cloud</Label>
  <div className="relative">
    <Input />
    <Button>▼</Button>
  </div>
  <Popover>
    <ListBox>
      <ListBoxItem id="aws">Amazon Web Services</ListBoxItem>
      <ListBoxItem id="gcp">Google Cloud Platform</ListBoxItem>
    </ListBox>
  </Popover>
</ComboBox>
```
O desenvolvedor não precisa conectar manualmente `aria-expanded`, `aria-controls`, `aria-activedescendant` ou sincronizar referências `ref`: o React Aria costura os nós de DOM internamente.

#### 5. Estados Declarativos no CSS: Atributos de Dados e Render Props
O React Aria expõe dinamicamente os estados internos do componente através de atributos de dados padronizados:
- `data-hovered`: ponteiro repousado sobre o nó.
- `data-pressed`: botão ativamente pressionado (mouse ou toque).
- `data-focused`: elemento detém o foco do documento.
- `data-focus-visible`: o anel de foco acessível deve ser desenhado.
- `data-selected`: item selecionado em listas, abas, grades ou tabelas.
- `data-disabled`: elemento indisponível funcionalmente.
- `data-entering` / `data-exiting`: ciclos de montagem/desmontagem de janelas modais, tooltips e popovers para animações de entrada e saída à prova de cortes secos.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados

1. **SaaS Enterprise Global, Fintechs & Plataformas Bancárias Multi-Moeda**:
   Aplicações transacionais que operam em múltiplos países com exigências de conformidade estrita (Seção 508, Lei Europeia de Acessibilidade EAA 2025, WCAG 2.2 AA). O suporte a múltiplos fusos horários (`ZonedDateTime`), moedas internacionais e calendários específicos torna o React Aria insubstituível.
2. **Design Systems Corporativos Escaláveis (White-Label / Multi-Brand)**:
   Grandes corporações (como a própria Adobe no Spectrum 2) que necessitam de uma base de código única e imutável para comportamento e acessibilidade, permitindo que dezenas de marcas filiais criem seus próprios temas visuais via Tailwind CSS ou tokens de design sem reescrever a lógica de teclado de um combobox ou tabela.
3. **Dashboards Operacionais Densos com Tabelas Interativas e Arrastar-e-Soltar**:
   Telas de monitoramento, CRMs de vendas e ERPs que utilizam componentes de `Table` ou `GridList` com suporte a seleção única/múltipla, ordenação dinâmica por colunas, e reordenação via Drag-and-Drop 100% operável pelo teclado e compreensível por leitores de tela.
4. **Aplicações Criativas, Editores Visuais e Ferramentas de Design (Web DAW / Vector)**:
   Softwares que exigem seletores de cor de grau profissional (`ColorPicker`, `ColorArea`, `ColorWheel`, `ColorSlider`, `ColorField`), sliders de múltiplas alças e controles de zoom/rotação onde a consistência de clique e arraste sob ponteiros de caneta (stylus), touch e mouse é mandatória.
5. **Aplicações com Requisitos Rígidos de Localização RTL (Árabe, Hebraico)**:
   Sistemas que atendem mercados do Oriente Médio, onde a simples inversão de CSS comumente quebra a ordem de navegação de teclado e a física de seletores de datas.

### Papel no Ritmo Visual (Regra 60-30-10)

- **60% — Fundação Estrutural, Acessibilidade Invisível & Entrada de Dados**:
  O React Aria serve com perfeição como a **espinha dorsal dos 60%**. Ele gere todos os botões, campos de texto, caixas de seleção, alternadores (switches), seletores de rádio e máscaras de data. Ele não adiciona glitter, mas garante que a plataforma seja indestrutível em termos de estabilidade de foco, validação semântica e ergonomia de digitação.
- **30% — Orquestração de Navegação, Menus Suspensos e Overlays Flutuantes**:
  Os componentes de camadas suspensas (`Modal`, `Popover`, `Menu`, `Dialog`, `Tooltip`, `Tabs` e `Breadcrumbs`) fornecem a camada de navegação contextual. A coordenação de fechamento suave via tecla Escape, clique externo (*pointer-down-outside*) e transições gerenciadas por `data-entering` / `data-exiting` confere à aplicação a sensação de um software desktop refinado.
- **10% — Showstoppers Protagonistas (Bibliotecas Complementares)**:
  O React Aria **não é** uma biblioteca de efeitos visuais ou 3D. Os elementos showstoppers (efeitos de partículas, transições orquestradas com Framer Motion, shaders WebGL, gráficos interativos de alta densidade) são inseridos no topo da fundação sólida fornecida pelo React Aria, sem risco de colapsar a usabilidade geral.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

- **Projetos "No-CSS" / MVPs com Prazo de 24 Horas sem Pipeline de Estilo**:
  Como o React Aria Components é **100% desestilizado (headless)**, renderizar um `<Button>` sem classes resulta em um botão com os estilos de agente do navegador (user-agent stylesheet). Se o objetivo é entregar um protótipo rápido sem tempo para configurar Tailwind CSS ou tokens de design, utilize bibliotecas pré-estilizadas out-of-the-box (Mantine, Chakra UI, HeroUI) ou componentes pré-construídos prontos.
- **Aplicações Fora do Ecossistema React (Vue, Svelte, Angular, Solid)**:
  O React Aria e o React Stately são estritamente vinculados às APIs de Hooks e Ciclo de Vida do React (`useRef`, `useCallback`, `useContext`). *(Para ecossistemas Svelte, adote Bits UI; para Vue, Radix Vue).*
- **Websites Estáticos Puros sem Interatividade de Formulários**:
  Landing pages puramente editoriais de rolagem de texto e imagens sem modais, selects complexos ou calendários. Nesses casos, o overhead de bundle do React Aria e do motor de datas é desnecessário; o HTML5 semântico nativo (`<button>`, `<details>`, `<dialog>`) é mais leve e veloz.

### ⚠️ Erros Comuns de Exagero e Implementação

1. **Uso Misto e Redundante de Hooks e Components**:
   Tentar instanciar `useButton` manualmente dentro de um `<Button>` do `react-aria-components`. Os componentes RAC já executam todos os hooks internamente. A camada de hooks de baixo nível deve ser reservada para integrações customizadas com bibliotecas legadas de terceiros.
2. **Quebra da Animação de Saída por Falta de Atributos de Transição**:
   Tentar animar janelas modais ou popovers apenas com classes CSS sem escutar `data-exiting`. Se o desenvolvedor tentar aplicar animações sem que a biblioteca coordene a desmontagem do nó, a janela será desmontada subitamente no momento em que o estado transita para `false`, eliminando a transição de saída (*flash unmount*).
3. **Hardcoding de Direções Físicas em Estilos CSS (Quebrando RTL)**:
   Utilizar classes de espaçamento direcional fixas como `ml-4`, `mr-2`, `pl-6`, `text-left` ao invés de propriedades lógicas (`ms-4` [margin-inline-start], `me-2` [margin-inline-end], `ps-6`, `text-start`). Em aplicações internacionalizadas com idiomas RTL, esse erro desalinha ícones e textos de alerta.
4. **Uso de Pseudoclasses `:hover` Puras ao Invés de `data-hovered` / `rac-hover`**:
   No ecossistema móvel iOS/Android, o CSS `:hover` trava no primeiro toque e só se desfaz quando outro elemento da tela é clicado (*sticky hover bug*). O React Aria gerencia o estado `data-hovered` desativando-o imediatamente quando o ponteiro é um toque físico, prevenindo interfaces móveis com visual travado.
5. **Omissão da Tag `<Label>` Acessível em Campos de Formulário**:
   Em componentes como `TextField`, `NumberField` ou `ComboBox`, omitir o `<Label>` filho ou deixar de passar um `aria-label` explícito quebra o vínculo semântico `id` ↔ `for`, reprovando testes automatizados de auditoria (Lighthouse / axe-core).

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

```
┌────────────────────────────────────────────────────────────────────────┐
│                   CATÁLOGO DE COMPONENTES REACT ARIA                   │
├─────────────────────┬─────────────────────┬────────────────────────────┤
│   OVERLAYS & JANELAS│   DATAS, NÚMEROS &  │   DADOS, LISTAS &          │
│                     │   CORES AVANÇADAS   │   NAVEGAÇÃO               │
├─────────────────────┼─────────────────────┼────────────────────────────┤
│ • Modal & Dialog    │ • DatePicker & Range│ • Table (Selection & DnD)  │
│ • Popover & Tooltip │ • ColorPicker Suite │ • GridList (Keyboard DnD)  │
│ • Menu & Submenu    │ • NumberField & Stepper • ComboBox & Autocomplete│
│ • Toast & Banner    │ • Slider & Range    │ • Tabs & Breadcrumbs       │
└─────────────────────┴─────────────────────┴────────────────────────────┘
```

### 1. DatePicker & DateRangePicker (Motor `@internationalized/date`)
- **Anatomia Visual**: Composto estruturalmente por `DatePicker`, `Label`, `Group`, `DateInput` (dividido em múltiplos `DateSegment` individuais: dia, mês, ano, hora, período AM/PM), `Button` de gatilho do calendário, e `Popover` contendo `Dialog`, `Calendar`, `Heading`, botões anterior/próximo e a grade `CalendarGrid` com células `CalendarCell`.
- **Gatilho de Interação**: Digitação segmentada direta (setas direita/esquerda navegam entre segmentos; setas cima/baixo ou digitação numérica alteram valores). O botão abre o popover com navegação por teclado (setas alteram dias, `PageUp`/`PageDown` alteram meses, `Shift+PageUp`/`Shift+PageDown` alteram anos). Fechamento suave com `Escape` ou clique externo.
- **Onde encaixar na página**: Agendamentos corporativos, formulários de reserva de voos/hotéis (modo Range), relatórios financeiros com seleção de período fiscal e datas de nascimento.

### 2. Table com Seleção Multi-Modo e Drag-and-Drop Acessível
- **Anatomia Visual**: Estrutura matricial composta por `Table`, `TableHeader`, `Column`, `TableBody`, `Row` e `Cell`. Inclui caixas de seleção automáticas no cabeçalho (*select all*) e em cada linha, estados de destaque sob hover e foco, e indicadores visuais de ordenação ascendente/descendente.
- **Gatilho de Interação**:
  - Clique simples ou barra de espaço para selecionar linhas;
  - `Shift + Clique` ou `Shift + Setas` para seleção contínua de intervalo;
  - `Cmd/Ctrl + Clique` para seleção pontual alternada;
  - *Roving tabindex* completo: as setas do teclado navegam célula a célula ou linha a linha sem perder o foco;
  - Suporte a Drag-and-Drop acessível: pressionar `Espaço` em uma linha inicia o arraste, setas posicionam a linha antes ou depois de outro elemento e `Enter` confirma o drop, com avisos em áudio/texto para leitores de tela via Live Region ARIA.
- **Onde encaixar na página**: Painéis principais de SaaS, backoffices operacionais, visualizadores de transações financeiras e gerenciamento de inventário de produtos.

### 3. GridList com Reordenação por Teclado e Arraste Visual
- **Anatomia Visual**: Lista de itens bidimensional ou vertical densa (`GridList`, `GridListItem`), integrando botão de arraste (*drag handle*), checkbox de seleção e áreas de conteúdo flexíveis.
- **Gatilho de Interação**: Suporta arraste contínuo via mouse/touch com linhas indicadoras de inserção (*drop indicator*). Pelo teclado, o usuário pressiona uma tecla de atalho configurada para levantar o item, move-o com as setas e solta-o na nova posição sem depender de precisão motora fina.
- **Onde encaixar na página**: Gerenciamento de tarefas estilo Kanban, listas de reprodução multimídia e ordenação de prioridades em roadmaps.

### 4. ColorPicker Suite (`ColorArea`, `ColorWheel`, `ColorSlider`, `ColorField`)
- **Anatomia Visual**: O mais avançado conjunto de manipulação de cores da Web. Permite combinar uma roda cromática circular (`ColorWheel`) com um seletor bidimensional de saturação e brilho (`ColorArea`), barras deslizantes de canal alfa ou matiz (`ColorSlider`) e campo de texto com suporte a valores Hex, RGB, HSL e HSB (`ColorField`). O ponto de controle (*thumb*) adapta seu anel de contraste dinamicamente em relação à cor de fundo selecionada.
- **Gatilho de Interação**: Arraste espacial suave por mouse ou toque; controle cirúrgico por teclado: setas movem o valor em incrementos de 1%, teclas `PageUp`/`PageDown` avançam em passos de 10%, com leitor de tela anunciando a cor e o percentual em linguagem natural.
- **Onde encaixar na página**: Ferramentas de edição gráfica, estúdios de personalização de temas, configuradores de produtos e editores de templates.

### 5. ComboBox & Autocomplete com Filtragem Inteligente
- **Anatomia Visual**: Sinergia entre campo de entrada de texto (`Input`), botão de abertura de lista, indicador de carregamento assíncrono e lista flutuante (`Popover`, `ListBox`, `ListBoxItem`).
- **Gatilho de Interação**: Ao digitar, a lista se expande filtrando resultados instantaneamente. Tecla de seta para baixo entra na lista mantendo o cursor de texto intacto através de `aria-activedescendant`. `Enter` seleciona a opção e fecha o popover; `Escape` descarta a lista restaurando o valor prévio.
- **Onde encaixar na página**: Barras de busca global com sugestão de resultados, seletores de países/estados, busca de clientes em CRM e seletores de tags.

### 6. Modal & Dialog com Ciclo `data-entering` / `data-exiting`
- **Anatomia Visual**: Composto por `ModalOverlay`, `Modal` e `Dialog`, integrando título semântico (`Heading`), descrição (`Text slot="description"`) e botão de fechamento. Escurece o fundo com um backdrop fosco ajustável.
- **Gatilho de Interação**: O React Aria gerencia o aprisionamento de foco (*focus trap*), desabilita a rolagem do corpo da página com compensação automática de largura de scrollbar para evitar saltos de layout (*layout shifts*), e aplica atributos `data-entering` e `data-exiting` durante os primeiros e últimos frames de exibição para alimentar animações CSS/Tailwind sem desmontagem abrupta.
- **Onde encaixar na página**: Confirmações de ações destrutivas, janelas de autenticação, wizards multipasso e edição rápida de registros.

### 7. Slider & RangeSlider com Suporte Internacionalizado
- **Anatomia Visual**: Trilho horizontal ou vertical (`SliderTrack`) com uma ou mais alças de controle táteis (`SliderThumb`) e saída textual dinâmica do valor (`SliderOutput`) formatada de acordo com unidades locais (graus Celsius/Fahrenheit, porcentagem, moedas BRL/USD).
- **Gatilho de Interação**: Arraste contínuo com detecção de proximidade; controle por setas do teclado com suporte a limites mínimos/máximos e passos definidos (*step*).
- **Onde encaixar na página**: Simuladores de empréstimos, filtros de preço em e-commerce, controles de volume e equalizadores de som.

### 8. TagGroup & TagField com Remoção e Seleção
- **Anatomia Visual**: Coleção organizada de etiquetas interativas (`TagGroup`, `TagList`, `Tag`). Cada etiqueta exibe texto informativo e um botão integrado de remoção (*remove button*).
- **Gatilho de Interação**: Seleção por clique ou teclado; navegação horizontal fluida por setas; ao focar uma etiqueta, pressionar a tecla `Delete` ou `Backspace` remove o item disparando anúncios de acessibilidade ao leitor de tela.
- **Onde encaixar na página**: Filtros aplicados em catálogos de produtos, listas de destinatários em clientes de e-mail e atribuição de categorias em CMS.

### 9. Menu & Submenu Multinível com Atalhos de Teclado
- **Anatomia Visual**: Painel suspenso de ações rápidas (`MenuTrigger`, `Menu`, `MenuItem`, `SubmenuTrigger`, `Separator`). Exibe rótulos de ações, ícones à esquerda e combinações de teclas de atalho à direita (ex: `⌘S`, `Ctrl+P`).
- **Gatilho de Interação**: Abertura rápida por clique ou foco; atalhos por digitação direta (*typeahead search* — digitar a primeira letra pula imediatamente para a opção); tecla de seta para a direita abre o submenu multinível; seta para a esquerda retorna ao menu pai.
- **Onde encaixar na página**: Menus de contexto de botão direito em editores, menus de perfil de usuário na barra superior e menus de opções de tabela (*action menus*).

### 10. Tabs & Breadcrumbs com Sincronização de Foco
- **Anatomia Visual**: Linha horizontal ou vertical de abas (`Tabs`, `TabList`, `Tab`, `TabPanel`) com indicador animado de aba ativa; e trilha de navegação hierárquica (`Breadcrumbs`, `Breadcrumb`).
- **Gatilho de Interação**: Navegação direta com setas direcionais entre abas; suporte a ativação automática no foco ou ativação manual via tecla `Enter`/`Space`; o conteúdo associado em `TabPanel` é vinculado bidirecionalmente via atributos `id` e `aria-labelledby`.
- **Onde encaixar na página**: Cabeçalhos de painéis de configuração, separadores de visão em páginas de produto e navegação estrutural de diretórios em SaaS.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup Moderno

O pacote unificado recomendado pela Adobe para aplicações modernas é o `react-aria-components`, complementado pelo plugin oficial do Tailwind CSS e pelo motor de datas internacionalizado:

```bash
# Instalação das primitivas centrais do React Aria Components
npm install react-aria-components

# Dependências essenciais para manipulação de datas, números e ícones
npm install @internationalized/date @internationalized/number clsx tailwind-merge lucide-react

# Plugin oficial para integração com Tailwind CSS
npm install -D tailwindcss-react-aria-components
```

### Configuração do Tailwind CSS (Plugin Oficial)

No arquivo `tailwind.config.ts` (ou no pipeline Tailwind v4), inclua o plugin para habilitar variantes elegantes baseadas nos estados dos componentes (`rac-focus:`, `rac-hover:`, `rac-selected:`, etc.):

```typescript
// tailwind.config.ts
import type { Config } from "tailwindcss";
import reactAriaComponentsPlugin from "tailwindcss-react-aria-components";

export default {
  content: ["./src/**/*.{js,ts,jsx,tsx}"],
  theme: {
    extend: {
      colors: {
        // Tokens de tema alinhados à escala OKLCH
        surface: {
          DEFAULT: "var(--surface)",
          raised: "var(--surface-raised)",
          overlay: "var(--surface-overlay)",
        },
      },
    },
  },
  plugins: [
    // Registra variantes inteligentes para todos os atributos data-* do React Aria
    reactAriaComponentsPlugin({ prefix: "rac" }),
  ],
} satisfies Config;
```

Para utilitários de composição de classes idênticos ao padrão moderno da indústria, cria-se a função auxiliar `cn` em `src/lib/utils.ts`:

```typescript
// src/lib/utils.ts
import { type ClassValue, clsx } from "clsx";
import { twMerge } from "tailwind-merge";

export function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs));
}
```

---

### Física de Movimento, Curvas de Transição & Animação

O React Aria Components gerencia os ciclos de vida de sobreposições (*overlays*) atribuindo os estados `data-entering` e `data-exiting`. Isso viabiliza transições suaves puras via Tailwind CSS ou animações de mola com Framer Motion:

1. **Curva de Desaceleração Natural**:
   - `cubic-bezier(0.16, 1, 0.3, 1)` (Curva ultra-suave para entrada de diálogos e expansão de menus).
2. **Classes Utilitárias Tailwind com Animação de Entrada e Saída**:
   ```html
   class="data-[entering]:animate-in data-[entering]:fade-in-0 data-[entering]:zoom-in-95 data-[exiting]:animate-out data-[exiting]:fade-out-0 data-[exiting]:zoom-out-95"
   ```
3. **Mola Física (Spring Physics) para Overlays com Framer Motion**:
   - `stiffness: 450`
   - `damping: 32`
   - `mass: 0.8`

---

### Receitas de Código Funcionais

#### Receita 1: DatePicker Internacionalizado de Alta Precisão

Esta receita implementa um seletor de datas completo, com suporte a localização automática, navegação por teclado e popover animado via Tailwind CSS:

```tsx
// src/components/ui/AccessibleDatePicker.tsx
import React from "react";
import {
  DatePicker,
  Label,
  Group,
  DateInput,
  DateSegment,
  Button,
  Popover,
  Dialog,
  Calendar,
  CalendarGrid,
  CalendarHeaderCell,
  CalendarGridHeader,
  CalendarGridBody,
  CalendarCell,
  Heading,
  type DatePickerProps,
  type DateValue,
} from "react-aria-components";
import { Calendar as CalendarIcon, ChevronLeft, ChevronRight } from "lucide-react";
import { cn } from "@/lib/utils";

interface AccessibleDatePickerProps<T extends DateValue>
  extends DatePickerProps<T> {
  label?: string;
  description?: string;
  errorMessage?: string;
}

export function AccessibleDatePicker<T extends DateValue>({
  label = "Selecione uma data",
  description,
  errorMessage,
  className,
  ...props
}: AccessibleDatePickerProps<T>) {
  return (
    <DatePicker
      {...props}
      className={cn("flex flex-col gap-1.5 w-full max-w-xs text-sm", className)}
    >
      {label && (
        <Label className="text-xs font-semibold uppercase tracking-wider text-neutral-400">
          {label}
        </Label>
      )}

      <Group className="relative flex h-10 w-full items-center rounded-lg border border-neutral-800 bg-neutral-900/80 px-3 text-neutral-100 shadow-sm transition-all focus-within:border-neutral-500 focus-within:ring-2 focus-within:ring-neutral-400/20">
        <DateInput className="flex flex-1 items-center font-mono text-sm outline-none">
          {(segment) => (
            <DateSegment
              segment={segment}
              className="rounded px-0.5 py-0.5 text-neutral-200 outline-none transition-colors focus:bg-blue-600 focus:text-white data-[type=literal]:text-neutral-500"
            />
          )}
        </DateInput>

        <Button className="flex h-7 w-7 items-center justify-center rounded-md text-neutral-400 hover:bg-neutral-800 hover:text-neutral-100 transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-neutral-400">
          <CalendarIcon className="h-4 w-4" />
        </Button>
      </Group>

      {description && (
        <span className="text-xs text-neutral-400">{description}</span>
      )}

      <Popover
        className={cn(
          "z-50 rounded-xl border border-neutral-800 bg-neutral-950 p-4 text-neutral-100 shadow-2xl outline-none backdrop-blur-xl",
          "data-[entering]:animate-in data-[entering]:fade-in-0 data-[entering]:zoom-in-95",
          "data-[exiting]:animate-out data-[exiting]:fade-out-0 data-[exiting]:zoom-out-95"
        )}
      >
        <Dialog className="outline-none">
          <Calendar className="w-fit">
            <header className="flex items-center justify-between pb-3 border-b border-neutral-800/80">
              <Button
                slot="previous"
                className="flex h-8 w-8 items-center justify-center rounded-lg border border-neutral-800 text-neutral-400 hover:bg-neutral-900 hover:text-neutral-100 transition-colors"
              >
                <ChevronLeft className="h-4 w-4" />
              </Button>
              <Heading className="text-sm font-semibold tracking-tight text-neutral-200" />
              <Button
                slot="next"
                className="flex h-8 w-8 items-center justify-center rounded-lg border border-neutral-800 text-neutral-400 hover:bg-neutral-900 hover:text-neutral-100 transition-colors"
              >
                <ChevronRight className="h-4 w-4" />
              </Button>
            </header>

            <CalendarGrid className="mt-3 border-collapse">
              <CalendarGridHeader>
                {(day) => (
                  <CalendarHeaderCell className="h-8 w-8 text-center text-xs font-medium text-neutral-400">
                    {day}
                  </CalendarHeaderCell>
                )}
              </CalendarGridHeader>
              <CalendarGridBody>
                {(date) => (
                  <CalendarCell
                    date={date}
                    className={cn(
                      "flex h-8 w-8 items-center justify-center rounded-lg text-xs font-medium outline-none transition-all cursor-pointer",
                      "hover:bg-neutral-800 focus-visible:ring-2 focus-visible:ring-neutral-300",
                      "data-[selected]:bg-neutral-100 data-[selected]:text-neutral-950 data-[selected]:font-semibold",
                      "data-[disabled]:text-neutral-700 data-[disabled]:cursor-not-allowed",
                      "data-[unavailable]:text-red-500/50 data-[unavailable]:line-through"
                    )}
                  />
                )}
              </CalendarGridBody>
            </CalendarGrid>
          </Calendar>
        </Dialog>
      </Popover>
    </DatePicker>
  );
}
```

---

#### Receita 2: Modal Acessível com Prevenção de Desmontagem Abrupta (`data-entering` / `data-exiting`)

Esta receita demonstra o controle arquitetural de abertura e fechamento de diálogo modal com bloqueio de foco (*focus trap*), desabilitação de scroll do fundo e transições elegantes:

```tsx
// src/components/ui/AccessibleModal.tsx
import React from "react";
import {
  ModalOverlay,
  Modal,
  Dialog,
  Heading,
  Button,
  DialogTrigger,
} from "react-aria-components";
import { X, ShieldAlert } from "lucide-react";
import { cn } from "@/lib/utils";

interface ConfirmationModalProps {
  triggerText: string;
  title: string;
  description: string;
  confirmText?: string;
  cancelText?: string;
  onConfirm: () => void;
}

export function ConfirmationModal({
  triggerText,
  title,
  description,
  confirmText = "Confirmar Operação",
  cancelText = "Cancelar",
  onConfirm,
}: ConfirmationModalProps) {
  return (
    <DialogTrigger>
      <Button className="inline-flex h-10 items-center justify-center rounded-lg bg-red-600 px-4 py-2 text-sm font-semibold text-white shadow-md hover:bg-red-500 active:bg-red-700 transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-red-400">
        {triggerText}
      </Button>

      <ModalOverlay
        className={cn(
          "fixed inset-0 z-50 flex min-h-full items-center justify-center p-4 bg-black/70 backdrop-blur-sm",
          "data-[entering]:animate-in data-[entering]:fade-in-0",
          "data-[exiting]:animate-out data-[exiting]:fade-out-0"
        )}
      >
        <Modal
          className={cn(
            "w-full max-w-md rounded-2xl border border-neutral-800 bg-neutral-900 p-6 text-neutral-100 shadow-2xl outline-none",
            "data-[entering]:animate-in data-[entering]:zoom-in-95 data-[entering]:slide-in-from-bottom-2",
            "data-[exiting]:animate-out data-[exiting]:zoom-out-95 data-[exiting]:slide-out-to-bottom-2"
          )}
        >
          <Dialog role="alertdialog" className="relative outline-none">
            {({ close }) => (
              <div className="flex flex-col gap-4">
                <div className="flex items-start gap-4">
                  <div className="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-red-500/10 text-red-400 border border-red-500/20">
                    <ShieldAlert className="h-5 w-5" />
                  </div>
                  <div className="flex flex-col gap-1 pr-6">
                    <Heading
                      slot="title"
                      className="text-lg font-semibold tracking-tight text-neutral-100"
                    >
                      {title}
                    </Heading>
                    <p className="text-sm text-neutral-400 leading-relaxed">
                      {description}
                    </p>
                  </div>
                </div>

                <div className="mt-4 flex justify-end gap-3 pt-2 border-t border-neutral-800">
                  <Button
                    onPress={close}
                    className="inline-flex h-9 items-center justify-center rounded-lg border border-neutral-700 bg-transparent px-4 text-sm font-medium text-neutral-300 hover:bg-neutral-800 hover:text-white transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-neutral-400"
                  >
                    {cancelText}
                  </Button>
                  <Button
                    onPress={() => {
                      onConfirm();
                      close();
                    }}
                    className="inline-flex h-9 items-center justify-center rounded-lg bg-red-600 px-4 text-sm font-semibold text-white hover:bg-red-500 active:bg-red-700 transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-red-400"
                  >
                    {confirmText}
                  </Button>
                </div>

                <Button
                  onPress={close}
                  aria-label="Fechar diálogo"
                  className="absolute top-0 right-0 rounded-md p-1 text-neutral-400 hover:bg-neutral-800 hover:text-neutral-100 transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-neutral-400"
                >
                  <X className="h-4 w-4" />
                </Button>
              </div>
            )}
          </Dialog>
        </Modal>
      </ModalOverlay>
    </DialogTrigger>
  );
}
```

---

#### Receita 3: ColorPicker Suite Completo com Suporte HSB e Acessibilidade de Teclado

Esta receita demonstra a integração das primitivas de cor da Adobe para edição visual de alto padrão:

```tsx
// src/components/ui/AccessibleColorPicker.tsx
import React from "react";
import {
  ColorPicker,
  ColorArea,
  ColorThumb,
  ColorSlider,
  SliderTrack,
  ColorField,
  Label,
  Input,
  ColorSwatch,
  DialogTrigger,
  Button,
  Popover,
  Dialog,
  parseColor,
} from "react-aria-components";
import { Pipette } from "lucide-react";
import { cn } from "@/lib/utils";

export function AccessibleColorPicker({
  defaultValue = "#3b82f6",
  label = "Cor de Destaque",
}: {
  defaultValue?: string;
  label?: string;
}) {
  return (
    <ColorPicker defaultValue={parseColor(defaultValue)}>
      <DialogTrigger>
        <div className="flex flex-col gap-1.5 w-fit">
          <span className="text-xs font-semibold uppercase tracking-wider text-neutral-400">
            {label}
          </span>
          <Button className="flex items-center gap-3 rounded-lg border border-neutral-800 bg-neutral-900/90 px-3 py-2 text-sm text-neutral-200 hover:border-neutral-700 transition-all focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-neutral-400">
            <ColorSwatch className="h-5 w-5 rounded-md border border-white/20 shadow-inner" />
            <span className="font-mono text-xs">Ajustar Cor</span>
            <Pipette className="h-3.5 w-3.5 text-neutral-500 ml-1" />
          </Button>
        </div>

        <Popover
          className={cn(
            "z-50 rounded-2xl border border-neutral-800 bg-neutral-950 p-4 text-neutral-100 shadow-2xl outline-none backdrop-blur-xl w-64",
            "data-[entering]:animate-in data-[entering]:fade-in-0 data-[entering]:zoom-in-95",
            "data-[exiting]:animate-out data-[exiting]:fade-out-0 data-[exiting]:zoom-out-95"
          )}
        >
          <Dialog className="flex flex-col gap-4 outline-none">
            {/* Área 2D de Saturação e Brilho */}
            <ColorArea
              colorSpace="hsb"
              xChannel="saturation"
              yChannel="brightness"
              className="h-36 w-full rounded-xl border border-neutral-800 shadow-inner overflow-hidden"
            >
              <ColorThumb className="h-5 w-5 rounded-full border-2 border-white shadow-md focus-visible:ring-2 focus-visible:ring-neutral-950 focus-visible:outline-none" />
            </ColorArea>

            {/* Slider de Matiz (Hue) */}
            <div className="flex flex-col gap-1">
              <span className="text-[11px] font-medium text-neutral-400">Matiz</span>
              <ColorSlider colorSpace="hsb" channel="hue" className="w-full">
                <SliderTrack className="h-4 w-full rounded-lg border border-neutral-800">
                  <ColorThumb className="top-1/2 h-5 w-5 rounded-full border-2 border-white shadow-md focus-visible:ring-2 focus-visible:ring-neutral-950 focus-visible:outline-none" />
                </SliderTrack>
              </ColorSlider>
            </div>

            {/* Slider de Canal Alfa (Opacidade) */}
            <div className="flex flex-col gap-1">
              <span className="text-[11px] font-medium text-neutral-400">Opacidade</span>
              <ColorSlider channel="alpha" className="w-full">
                <SliderTrack className="h-4 w-full rounded-lg border border-neutral-800 bg-[linear-gradient(45deg,#262626_25%,transparent_25%),linear-gradient(-45deg,#262626_25%,transparent_25%),linear-gradient(45deg,transparent_75%,#262626_75%),linear-gradient(-45deg,transparent_75%,#262626_75%)] bg-[size:8px_8px]">
                  <ColorThumb className="top-1/2 h-5 w-5 rounded-full border-2 border-white shadow-md focus-visible:ring-2 focus-visible:ring-neutral-950 focus-visible:outline-none" />
                </SliderTrack>
              </ColorSlider>
            </div>

            {/* Campo Hexadecimal com Validação Acessível */}
            <div className="pt-2 border-t border-neutral-800 flex items-center justify-between gap-2">
              <ColorField className="flex items-center gap-2">
                <Label className="text-xs font-mono text-neutral-400">HEX</Label>
                <Input className="h-8 w-28 rounded-md border border-neutral-800 bg-neutral-900 px-2 font-mono text-xs text-neutral-100 outline-none focus:border-neutral-500 focus:ring-1 focus:ring-neutral-400" />
              </ColorField>
              <ColorSwatch className="h-8 w-8 rounded-lg border border-neutral-700 shadow-sm" />
            </div>
          </Dialog>
        </Popover>
      </DialogTrigger>
    </ColorPicker>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir o `DESIGN_BLUEPRINT.md` de qualquer produto digital fundamentado no **React Aria** ou **React Aria Components**, a IA deve seguir rigorosamente as seguintes diretrizes:

### 1. Declaração Formal no Tech Stack
```markdown
### Accessibility, Primitives & Interaction Core
- **Biblioteca de Primitivas**: React Aria Components (`react-aria-components`)
- **Arquitetura de Estado**: React Stately (`react-stately`)
- **Motor de Internacionalização**: `@internationalized/date` & `@internationalized/number`
- **Tailwind Plugin**: `tailwindcss-react-aria-components`
- **Padrão de Encapsulamento**: Design System Layer centralizada em `@/components/ui/*`
```

### 2. Encapsulamento Mandatório de Primitivas
- **Proibição Direta**: Nunca instancie tags brutas do `react-aria-components` diretamente em páginas funcionais (`app/dashboard/page.tsx`).
- **Encapsulamento**: Crie arquivos de componentes semânticos em `components/ui/` (ex: `button.tsx`, `dialog.tsx`, `date-picker.tsx`, `table.tsx`, `select.tsx`) que combinem a primitiva headless do React Aria com a identidade visual do projeto e tokens Tailwind.

### 3. Convenção de Variantes e Estados
- Utilize exclusivamente as variantes providas pelo plugin `tailwindcss-react-aria-components` ou a sintaxe de atributos de dados nativos:
  - Para foco visível: utilize `data-[focus-visible]:ring-2` (nunca apenas `:focus` que quebra com cliques de mouse).
  - Para estado pressionado: utilize `data-[pressed]:scale-[0.98]` (nunca apenas `:active` que falha em toques móveis).
  - Para transições de saída de overlays: utilize `data-[exiting]:fade-out data-[exiting]:zoom-out-95`.
  - Para seleções em listas/tabelas: utilize `data-[selected]:bg-neutral-800`.

### 4. Suporte Rigoroso a Internacionalização (i18n & RTL)
- Sempre configure o provider raiz `<I18nProvider locale={currentLocale}>` no topo da árvore de componentes (ex: `app/layout.tsx`).
- Utilize **propriedades lógicas CSS** em todas as classes utilitárias de alinhamento:
  - Prefira `ps-*` e `pe-*` em vez de `pl-*` e `pr-*`.
  - Prefira `ms-*` e `me-*` em vez de `ml-*` e `mr-*`.
  - Prefira `text-start` e `text-end` em vez de `text-left` e `text-right`.

### 5. Checklist de Validação de Acessibilidade
- [ ] Todo componente com entrada de dados possui uma tag `<Label>` associada ou atributo `aria-label` explícito.
- [ ] Todas as janelas modais (`ModalOverlay`) possuem suporte a `data-entering` e `data-exiting` para evitar desaparecimento abrupto de tela.
- [ ] Diálogos de confirmação destrutiva utilizam `role="alertdialog"`.
- [ ] Gráficos, tabelas complexas e seletores de cor têm equivalentes textuais ou navegação completa por teclado via *roving tabindex*.
- [ ] A navegação de foco (`Tab` e setas) percorre a interface sem aprisionamentos acidentais fora de janelas modais.
