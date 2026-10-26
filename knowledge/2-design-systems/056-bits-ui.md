---
id: "bits-ui"
name: "Bits UI"
url: "https://www.bits-ui.com/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Headless Primitives Architecture", "Svelte 5 Runes Native", "WAI-ARIA Accessibility Core", "Tailwind CSS Token Alignment", "Zero-Runtime Overhead Engineering"]
densidade_informacao: "Flexivel"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS/Headless)"
stack_frameworks: ["Svelte 5 (Runes & Snippets)", "SvelteKit", "Bits UI v1", "Tailwind CSS v4 & v3", "shadcn-svelte", "TypeScript", "@floating-ui/dom", "@internationalized/date", "Lucide Svelte"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "Plus Jakarta Sans", "JetBrains Mono", "Outfit", "Satoshi"]
  paletas_ideais: ["OKLCH Semantic Palettes", "Zinc & Slate Monochromes", "Obsidian Dark Mode", "Warm Neutral (Stone/Sand)", "Deep Indigo Enterprise"]
  combinacoes_recomendadas: ["shadcn-svelte", "Svelte Motion", "Tailwind Animate", "Lucide Svelte", "Mode Watcher (Svelte)", "Formsnap (Superforms + Bits UI)"]
  conflitos_esteticos: ["Bibliotecas monolíticas com CSS opinativo inline", "Frameworks legados com acoplamento DOM rígido", "Estilos destrutivos com !important em seletores globais"]
---

# Bits UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Bits UI**, concebido e liderado pelo engenheiro Hunter Johnston ([@huntabyte](https://github.com/huntabyte)), representa o alicerce fundamental de engenharia de interface para a era moderna do **Svelte 5**. Trata-se de uma biblioteca de **primitivas headless desestilizadas e rigorosamente acessíveis (WAI-ARIA)**, projetada do zero para ser o equivalente direto do que o Radix UI representa para o ecossistema React. É o motor estrutural que alimenta o aclamado **shadcn-svelte**.

### A Filosofia Headless Pura & Desacoplamento Visual
Diferente de bibliotecas visuais opinativas (como DaisyUI, Flowbite ou Material UI), o Bits UI não impõe **nenhum** CSS, estilo inline, cor ou tipografia pré-definida. A biblioteca assume 100% da responsabilidade sobre:
1. **Comportamento & Máquina de Estados**: Gerenciamento de aberturas, fechamentos, seleções simples e múltiplas, paginação e ciclos de vida.
2. **Navegação por Teclado & Roving Focus**: Implementação estrita das diretrizes WAI-ARIA (setas direcionais, Home/End, PageUp/PageDown, Escape, Enter, Tab e Space) sem vazamento de foco acidental.
3. **Acessibilidade em Nível de DOM**: Atribuição automática e sincronizada de IDs semânticos, relações `aria-controls`, `aria-labelledby`, `aria-expanded`, `aria-activedescendant` e atributos `role`.
4. **Geometria de Posicionamento Flutuante**: Integração com a suíte matemática do `@floating-ui/dom` para posicionamento dinâmico de popovers, tooltips e dropdowns com detecção de colisões de viewport, viradas dinâmicas (*flip*) e deslocamentos adaptativos (*shift*).

A identidade visual resultante é, portanto, uma folha em branco de máxima pureza técnica: o desenvolvedor ou designer mantém a propriedade integral da camada cosmética via Tailwind CSS, CSS Modules ou Svelte scoped styles, beneficiando-se de uma fundação à prova de falhas de acessibilidade.

```
┌─────────────────────────────────────────────────────────────┐
│                      SVELTE 5 INTERFACE                     │
├─────────────────────────────────────────────────────────────┤
│  Estética & Temas (Tailwind v4 / OKLCH / CSS Scoped / Tokens)│
├─────────────────────────────────────────────────────────────┤
│  shadcn-svelte (Templates de Estilo, Variantes & Presets)   │
├─────────────────────────────────────────────────────────────┤
│  BITS UI v1 (Headless Primitives: Focus, ARIA, Teclado)     │
├─────────────────────────────────────────────────────────────┤
│  SVELTE 5 ENGINE (Runes: $state, $derived, $bindable, Snippets)│
└─────────────────────────────────────────────────────────────┘
```

### A Transição Histórica: A Ruptura de Svelte 4 para Svelte 5 Runes
Nas versões iniciais do ecossistema Svelte headless (como Melt UI e as primeiras versões do Bits UI no Svelte 4), a arquitetura apoiava-se fortemente no padrão de *Svelte Actions* (`use:action`) acopladas a *Stores reativas* (`derived`, `writable`). Embora funcional, esse modelo exigia sintaxes complexas de desestruturação (`use:builder.action`, `let:builder`), trazia penalidades de overhead de inscrição/cancelamento de listeners e sofria com atritos de tipagem em formulários densos.

Com a chegada do **Bits UI v1** para o **Svelte 5**, Hunter Johnston reconstruiu a biblioteca integralmente sobre o novo motor reativo de **Runes**:
- **Eliminação de Stores**: Todo o gerenciamento de estado interno abandonou as antigas *Svelte Stores*. Agora utiliza primitivas de compilação reativa direta: `$state`, `$derived` e `$effect`.
- **Ligação Bidirecional Fluida (`$bindable`)**: Estados como `open`, `value`, `selected` e `activePage` utilizam a diretiva `$bindable()`, permitindo vincular o estado reativo diretamente ao componente consumidor através de `bind:value={myState}` sem intermediários nem dispatchers de eventos redundantes.
- **Micro-reatividade Cirúrgica**: A reatividade ocorre no menor nó de DOM possível, sem re-renderizações globais de árvore de componentes.

### O Padrão `child` Snippet (Render Delegation Moderna)
No ecossistema React/Radix, a delegação de renderização depende da propriedade `asChild`, que utiliza `React.cloneElement` internamente para injetar props e event listeners no elemento filho — uma operação que frequentemente gera bugs com refs, fragmentos e complexidade no Virtual DOM.

Como o Svelte não possui Virtual DOM nem `cloneElement`, o Bits UI v1 introduziu o padrão **`child` snippet** aproveitando o poder nativo dos **Snippets do Svelte 5** (`{#snippet ...}`). Esse padrão fornece controle cirúrgico sobre a árvore de renderização:

```svelte
<Dialog.Trigger>
  {#snippet child({ props })}
    <!-- O desenvolvedor tem controle total do markup, repassando os handlers e ARIA do Bits UI -->
    <button {...props} class="btn-primary">
      Abrir Modal Seguro
    </button>
  {/snippet}
</Dialog.Trigger>
```

Se o desenvolvedor precisar animar ou gerenciar wrappers de posicionamento (como em Popovers e Tooltips flutuantes), o snippet expõe simultaneamente `props`, `wrapperProps` e o estado booleano de visibilidade `open`:

```svelte
<Popover.Content forceMount>
  {#snippet child({ wrapperProps, props, open })}
    {#if open}
      <div {...wrapperProps}>
        <div {...props} transition:fly={{ y: -8, duration: 150 }}>
          Conteúdo Flutuante Acessível
        </div>
      </div>
    {/if}
  {/snippet}
</Popover.Content>
```

### Assinatura Tátil e Exposição de Atributos Semânticos (`data-*`)
O Bits UI comunica seus estados internos para o CSS expondo sistematicamente atributos `data-*` padronizados em todos os nós da árvore de componentes:
- `data-state="open | closed | checked | unchecked | indeterminate"`
- `data-disabled`
- `data-highlighted` (para itens sob foco de teclado em listas)
- `data-selected`
- `data-orientation="horizontal | vertical"`
- `data-side="top | right | bottom | left"`
- `data-align="start | center | end"`

Essa padronização permite estilização pura e declarativa em Tailwind CSS via variantes de dados (`data-[state=open]:animate-in`, `data-[highlighted]:bg-accent`, `data-[disabled]:opacity-50`), garantindo uma sincronização milimétrica entre a lógica de acessibilidade e o feedback visual.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados
1. **SaaS B2B, Plataformas Enterprise & Backoffices Operacionais em SvelteKit**:
   Aplicações corporativas que dependem de dezenas de formulários complexos, modais críticos de confirmação, seletores multifacetados e tabelas interativas. O Bits UI provê a espinha dorsal de acessibilidade exigida por padrões corporativos rígidos (WCAG 2.1 AA/AAA, Seção 508).
2. **Developer Tools, Bancos de Dados & Cloud Consoles (Estilo Supabase/Vercel)**:
   Ferramentas voltadas para engenheiros onde o controle rápido pelo teclado é essencial: navegação rápida por paletas de comando (`Cmd+K`), atalhos de seleção, menus de contexto com clique direito e dropdowns aninhados sem atraso perceptível de renderização.
3. **Plataformas de Autenticação Segura & Fintechs**:
   Sistemas com fluxos de login em dois fatores (2FA/MFA), conferência de senhas de uso único (OTP) e formulários de agendamento bancário. A primitiva `PinInput` e os componentes de calendário internacionalizados (`Date Picker`, `Range Calendar`) eliminam meses de desenvolvimento arriscado.
4. **Design Systems Corporativos Customizados (White-Label)**:
   Organizações que precisam criar seu próprio sistema interno de design (ex: "Acme Svelte UI") sem carregar o peso visual ou as convenções estéticas de terceiros, construindo seus próprios componentes estilizados com seus próprios tokens Tailwind v4 sobre os blocos acessíveis do Bits UI.
5. **Formulários Ricos com Validação Conduzida (Formsnap + Superforms)**:
   A combinação Bits UI + Formsnap + SvelteKit Superforms + Zod é o padrão de ouro indiscutível no ecossistema Svelte para criação de formulários tipados, com acessibilidade ligada a mensagens de erro em tempo real.

### Papel no Ritmo Visual (A Aplicação Rigorosa da Regra 60-30-10)

- **60% — Espinha Dorsal Estrutural & Motor de Acessibilidade (A Fundação Invisível)**:
  O Bits UI atua com perfeição absoluta como o **alicerce invisível de 60%**. Ele dita como as caixas de diálogo se comportam, como os botões de rádio e caixas de seleção transmitem estados ao leitor de tela, e como os acordeões colapsam. Não há glitter nem efeitos pirotécnicos aqui: é solidez de engenharia que assegura que qualquer usuário consiga operar a interface sem atrito.
- **30% — Camada de Navegação, Orquestração e Micro-interações**:
  Os componentes voláteis do Bits UI (`DropdownMenu`, `NavigationMenu`, `Popover`, `Command`, `Sheet` e `Tabs`) gerenciam o fluxo de descoberta da interface. As transições de abertura suave, o deslizamento do viewport do menu e a aparição sutil de tooltips definem a fluidez tátil percebida pelo usuário.
- **10% — Showstoppers Protagonistas (Bibliotecas Satélites)**:
  O Bits UI **não é** nem tenta ser o showstopper visual. O seu propósito é ser a rocha firme sobre a qual os componentes de alto impacto (animações com Svelte Motion, modelos Three.js / Threlte, partículas WebGL e gráficos interativos com LayerChart) possam brilhar sem que a infraestrutura básica de navegação da página desmorone.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Projetos Presos em Svelte 3 ou Svelte 4 sem Previsão de Migração**:
  O Bits UI v1 foi arquitetado especificamente para as APIs do Svelte 5 (Runes e Snippets). Tentar retroalimentar componentes v1 em ecossistemas legados de Svelte 4 causará quebras imediatas de compilação. *(Para projetos congelados em Svelte 4, deve-se manter a versão Bits UI v0.x legada baseada em Melt UI)*.
- **Projetos "No-Build" / Websites Estáticos Sem Compilador Svelte**:
  Aplicações construídas com arquiteturas server-side puras tradicionais (templates PHP puros, Django templates, Go html/template) sem um bundler moderno (Vite/Rollup) não podem usufruir da biblioteca.
- **Necessidade de Solução "Plug-and-Play" Instantânea Sem Pipeline de Design**:
  Se uma equipe precisa de um painel de administração montado em 30 minutos sem gastar nenhum tempo escrevendo classes CSS ou ajustando temas, o Bits UI em seu estado puro causará frustração, pois é **100% headless** (sem classes ou cores). Nesses casos, o `shadcn-svelte` (que já entrega os componentes Bits UI pré-vestidos com Tailwind) ou bibliotecas pré-estilizadas são a escolha correta.
- **Páginas Puramente Estáticas de Baixa Interação**:
  Landing pages promocionais estáticas de rolagem simples sem modais, selects complexos ou acordeões não necessitam do overhead de abstrações headless; o uso de HTML semântico nativo (`<dialog>`, `<details>`, `<summary>`) é mais enxuto.

---

### ⚠️ Erros Comuns de Exagero e Implementação

1. **Omissão do Spread de Props no `child` Snippet (Desastre de Acessibilidade)**:
   Ao utilizar `{#snippet child({ props })}`, desenvolvedores inexperientes frequentemente esquecem de incluir `{...props}` na tag interna:
   ```svelte
   <!-- ❌ ERRADO: Destrói focus trap, ARIA e eventos do Bits UI -->
   <Dialog.Trigger>
     {#snippet child({ props })}
       <button class="bg-blue-600">Abrir</button>
     {/snippet}
   </Dialog.Trigger>

   <!-- ✅ CORRETO: Propaga todos os listeners e atributos acessíveis -->
   <Dialog.Trigger>
     {#snippet child({ props })}
       <button {...props} class="bg-blue-600">Abrir</button>
     {/snippet}
   </Dialog.Trigger>
   ```
2. **Conflito de Transições: Desmontagem Prematura sem `forceMount`**:
   Ao tentar usar transições nativas do Svelte (`transition:fly`, `transition:fade`) em containers de conteúdo (`Dialog.Content`, `Popover.Content`, `Select.Content`), se a propriedade `forceMount` não for declarada, o Bits UI destruirá o nó DOM no instante exato do fechamento antes que a animação de saída termine, provocando um corte abrupto e antiestético (*exit glitch*).
3. **A Armadilha do "Default shadcn-svelte Slop"**:
   Replicar cegamente os exemplos padrão de documentação mantendo o cinza neutro `#09090b` com cantos arredondados genéricos `rounded-md` sem calibrar uma paleta de identidade própria, passando a impressão de um clone indiferenciado de tutoriais de IA.
4. **Sobrecarga de Floating Elements na Mesma Tela**:
   Abrir múltiplos tooltips, hover cards e popovers simultâneos que concorrem por foco e espaço de viewport em dispositivos móveis, degradando a usabilidade ergonômica.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão 10 das primitivas mais poderosas e fundamentais da suíte Bits UI v1:

```
┌────────────────────────────────────────────────────────────────────────┐
│                        BITS UI COMPONENT SUITE                         │
├─────────────────────┬─────────────────────┬────────────────────────────┤
│   OVERLAYS / POPOVER│   FORM & DATA INPUT │   NAVIGATION & DISPLAY     │
├─────────────────────┼─────────────────────┼────────────────────────────┤
│ • Dialog / Alert    │ • Combobox          │ • Navigation Menu          │
│ • Popover / Tooltip │ • Date & Range Cal  │ • Tabs / Toggle Group      │
│ • Hover Card        │ • Pin Input (OTP)   │ • Accordion / Collapsible  │
│ • Context / Dropdown│ • Select & Slider   │ • Scroll Area              │
└─────────────────────┴─────────────────────┴────────────────────────────┘
```

### 1. Dialog & Alert Dialog (Modal Acessível com Focus Trapping & Backdrop Lock)
- **Anatomia Visual**: Composto por `Dialog.Root`, `Dialog.Trigger`, `Dialog.Portal`, `Dialog.Overlay`, `Dialog.Content`, `Dialog.Title`, `Dialog.Description` e `Dialog.Close`. Renderiza um backdrop fosco escuro (*overlay*) e uma janela centralizada suspensa na tela, isolando o restante da aplicação.
- **Gatilho de Interação**: Disparado por clique no gatilho ou programaticamente via reatividade `bind:open={isOpen}`. Suporta fechamento via clique fora (*pointer-down-outside*), tecla `Escape`, e aprisiona o tabulador do teclado (*focus lock*) no interior do diálogo. Desabilita o scroll do documento de fundo (`overflow: hidden` automático com compensação de largura de barra de rolagem).
- **Onde encaixar na página**: Confirmações de exclusão destrutiva (`AlertDialog`), modais de criação de conta, diálogos de configuração de equipe e wizards multipasso.

### 2. Combobox (Autocompleter Dinâmico & Roving Tabindex)
- **Anatomia Visual**: União arquitetural entre um campo de texto (`Combobox.Input`), botão de trigger (`Combobox.Trigger`) e menu popover (`Combobox.Content`, `Combobox.Item`, `Combobox.Group`). Permite digitação contínua para filtragem instantânea com destaque visual (*highlight*) no item atualmente focado.
- **Gatilho de Interação**: Foco e digitação no input abrem o popover; teclas de seta cima/baixo navegam ciclicamente entre opções com *roving tabindex*; `Enter` confirma a seleção; `Escape` descarta a lista.
- **Onde encaixar na página**: Seletores de países/moedas em checkouts, atribuição de tags em editores de CMS, filtros facetados de busca e busca de membros em workspaces.

### 3. Date Picker & Range Calendar (Motor de Datas com `@internationalized/date`)
- **Anatomia Visual**: Calendário de alta precisão construído com `RangeCalendar.Root`, `RangeCalendar.Header`, `RangeCalendar.Heading`, `RangeCalendar.PrevButton`, `RangeCalendar.NextButton`, `RangeCalendar.Grid`, `RangeCalendar.GridRow`, `RangeCalendar.Cell` e `RangeCalendar.Day`. Exibe dias da semana, numeração dos dias do mês e faixas de seleção contínuas (*start-date*, *middle-dates*, *end-date*).
- **Gatilho de Interação**: Clique no dia de início e término; navegação completa por teclado via setas (avançar/recuar 1 dia), `PageUp`/`PageDown` (avançar/recuar 1 mês), `Shift+PageUp`/`Shift+PageDown` (avançar/recuar 1 ano). Suporte completo a formatação de calendários internacionais (Gregoriano, Islâmico, Hebraico, Budista) e restrições de datas passadas ou indisponíveis.
- **Onde encaixar na página**: Sistemas de reserva de hotéis e passagens aéreas (check-in / check-out), filtros de período em relatórios financeiros e agendamento de reuniões.

### 4. Pin Input (Autenticação OTP com Segmentação Automática)
- **Anatomia Visual**: Conjunto de slots individuais de dígitos alinhados horizontalmente (`PinInput.Root`, `PinInput.Input`). Cada slot representa um caractere da chave de segurança, com cursor intermitente e opção de ofuscação (máscara de senha com bullets `•`).
- **Gatilho de Interação**: Digitação avança automaticamente o foco para a próxima célula; pressionar `Backspace` limpa o caractere e move o cursor para a célula anterior; colar (*Ctrl+V* ou *Cmd+V*) um código da área de transferência distribui automaticamente os caracteres em todos os slots e dispara o evento de conclusão.
- **Onde encaixar na página**: Telas de verificação em duas etapas (2FA), validação de código SMS/e-mail no cadastro e autorização de transações financeiras críticas.

### 5. Popover & Hover Card (Flutuantes com Floating UI & Safe Triangles)
- **Anatomia Visual**: Painéis flutuantes posicionados geometricamente em relação a um elemento âncora (`Popover.Trigger`, `Popover.Content`, `Popover.Arrow`). O `Hover Card` provê um preview leve com atrasos ajustáveis de abertura (*openDelay*) e fechamento (*closeDelay*), implementando algoritmos de triângulo de segurança do cursor para evitar fechamentos acidentais durante a trajetória do mouse.
- **Gatilho de Interação**: `Popover` responde a clique ou teclado; `Hover Card` responde à proximidade do cursor com tempo de tolerância.
- **Onde encaixar na página**: Previews de perfil de usuário em timelines (estilo Twitter/GitHub), cartões informativos sobre termos técnicos, e pequenos seletores de cor ou filtros rápidos.

### 6. Accordion & Collapsible (Expansão Acessível Sem Layout Shifts)
- **Anatomia Visual**: Lista de seções verticais estruturadas por `Accordion.Root`, `Accordion.Item`, `Accordion.Header`, `Accordion.Trigger` e `Accordion.Content`. Suporta modos `single` (apenas um item aberto por vez) ou `multiple` (múltiplas seções simultâneas).
- **Gatilho de Interação**: Clique no cabeçalho ou teclas `Space`/`Enter`. Gerencia internamente as variáveis de altura CSS para permitir animações fluidas de abertura e recolhimento sem solavancos bruscos de altura.
- **Onde encaixar na página**: Seção de Perguntas Frequentes (FAQ) em páginas de vendas, menus laterais com subcategorias colapsáveis e visualizadores de histórico de auditoria.

### 7. Select & Multi-Select (Substituto Acessível ao `<select>` Nativo)
- **Anatomia Visual**: Composto por `Select.Root`, `Select.Trigger`, `Select.Value`, `Select.Content`, `Select.Group`, `Select.Label`, `Select.Item`, `Select.ItemText`, `Select.ItemIndicator` e `Select.Separator`. Renderiza um gatilho estilizado com ícone chevron e menu flutuante com suporte a indicadores de marcação (*checkmarks*).
- **Gatilho de Interação**: Clique ou tecla de seta para abrir; suporte a digitação rápida (*typeahead search* — digitar "b-r-a" navega direto até "Brasil"); foco gerenciado de forma invisível.
- **Onde encaixar na página**: Formulários de cadastro de endereço, configuração de moeda em dashboards e seletores de visualização de tabelas.

### 8. Command (Menu de Ações Globais `Cmd+K`)
- **Anatomia Visual**: Modal flutuante suspenso com backdrop blur (`Command.Root`, `Command.Input`, `Command.List`, `Command.Empty`, `Command.Group`, `Command.Item`, `Command.Separator`). Contém campo de busca embutido com ícone de busca, lista de ações organizadas e atalhos de teclado renderizados via `<kbd>`.
- **Gatilho de Interação**: Tecla global de atalho `Cmd+K` / `Ctrl+K`. Filtragem instantânea conforme o usuário digita; navegação por setas e execução de comando ao teclar `Enter`.
- **Onde encaixar na página**: Barra global de busca do cabeçalho de SaaS, centro de comandos operacionais e documentações de software técnico.

### 9. Slider & Range Slider (Controle Deslizante de Precisão)
- **Anatomia Visual**: Trilho horizontal ou vertical (`Slider.Root`, `Slider.Track`, `Slider.Range`) com um ou mais botões de arraste tácteis (`Slider.Thumb`).
- **Gatilho de Interação**: Arraste contínuo via mouse/touch com snapping em passos definidos (*step*); controle minucioso via teclado: setas aumentam/diminuem pelo passo básico, `PageUp`/`PageDown` avançam em passos maiores, e `Home`/`End` vão aos extremos mínimo/máximo.
- **Onde encaixar na página**: Filtros de faixa de preço em e-commerce, controles de volume e equalizadores de áudio, e parâmetros de simulação de taxas de juros.

### 10. Navigation Menu (Menu com Viewport Compartilhado Flutuante)
- **Anatomia Visual**: Sistema sofisticado de navegação horizontal (`NavigationMenu.Root`, `NavigationMenu.List`, `NavigationMenu.Item`, `NavigationMenu.Trigger`, `NavigationMenu.Content`, `NavigationMenu.Viewport`, `NavigationMenu.Indicator`). Múltiplos gatilhos compartilham um único painel viewport flutuante que desliza e redimensiona suavemente sua largura e altura ao transitar entre itens.
- **Gatilho de Interação**: Hover com temporizador de tolerância e suporte total a navegação tabular acessível via teclado.
- **Onde encaixar na página**: Cabeçalhos principais de grandes plataformas SaaS, menus de produtos em landing pages empresariais e marketplaces.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup Moderno

O Bits UI é instalado diretamente via NPM em projetos SvelteKit ou Vite + Svelte 5:

```bash
# Instalação das primitivas centrais do Bits UI
npm install bits-ui

# Dependências recomendadas para formulários, datas e ícones
npm install @internationalized/date clsx tailwind-merge lucide-svelte
```

Para utilitários de composição de classes idênticos ao padrão da indústria, cria-se o utilitário `cn` em `src/lib/utils.ts`:

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

No ecossistema Svelte, a animação de primitivas do Bits UI pode ser realizada por três caminhos complementares:

1. **Transições Nativas do Svelte (`svelte/transition`) com `forceMount`**:
   O Bits UI mantém o elemento no DOM enquanto a transição de saída é executada:
   - Curva de desaceleração suave: `cubic-bezier(0.16, 1, 0.3, 1)`
   - Transições ideais: `fly({ y: -10, duration: 200, easing: quintOut })` e `fade({ duration: 150 })`.
2. **Classes Utilitárias Tailwind CSS + `tailwindcss-animate`**:
   Controladas diretamente pelos atributos de dados:
   ```html
   class="data-[state=open]:animate-in data-[state=closed]:animate-out data-[state=closed]:fade-out-0 data-[state=open]:fade-in-0 data-[state=closed]:zoom-out-95 data-[state=open]:zoom-in-95 data-[side=bottom]:slide-in-from-top-2"
   ```
3. **Mola Física (Spring Physics) para Svelte Motion ou Transições CSS Avançadas**:
   - `stiffness: 400`
   - `damping: 30`
   - `mass: 0.8`

---

### Receitas de Código Funcionais (Svelte 5 Runes)

#### Receita 1: Combobox Acessível com Busca Dinâmica & Runes (`$state` / `$derived`)

Esta receita demonstra o uso de Runes no Svelte 5, com estado bindable e estilização elegante via Tailwind CSS:

```svelte
<!-- src/lib/components/ui/ProjectCombobox.svelte -->
<script lang="ts">
  import { Combobox } from "bits-ui";
  import { Check, ChevronsUpDown, Search } from "lucide-svelte";
  import { cn } from "$lib/utils";

  interface Framework {
    value: string;
    label: string;
  }

  const frameworks: Framework[] = [
    { value: "svelte", label: "Svelte 5 (Runes Native)" },
    { value: "next", label: "Next.js (React 19)" },
    { value: "astro", label: "Astro Islands" },
    { value: "nuxt", label: "Nuxt 3 (Vue)" },
    { value: "remix", label: "Remix / React Router" },
  ];

  // Svelte 5 Runes de Estado
  let searchValue = $state("");
  let selectedValue = $state("svelte");

  // Runa derivada para filtragem em tempo real
  const filteredFrameworks = $derived(
    searchValue === ""
      ? frameworks
      : frameworks.filter((f) =>
          f.label.toLowerCase().includes(searchValue.toLowerCase())
        )
  );

  const selectedLabel = $derived(
    frameworks.find((f) => f.value === selectedValue)?.label ?? "Selecione a stack..."
  );
</script>

<div class="w-full max-w-sm space-y-2">
  <label for="combobox-input" class="text-xs font-semibold uppercase tracking-wider text-muted-foreground">
    Stack Tecnológica
  </label>

  <Combobox.Root
    items={frameworks}
    bind:value={selectedValue}
    type="single"
  >
    <div class="relative">
      <Combobox.Input
        id="combobox-input"
        class={cn(
          "flex h-10 w-full rounded-md border border-input bg-background px-3 py-2 pr-10 text-sm",
          "placeholder:text-muted-foreground focus-visible:outline-none focus-visible:ring-2",
          "focus-visible:ring-ring focus-visible:ring-offset-2 transition-colors"
        )}
        placeholder="Buscar tecnologia..."
        bind:value={searchValue}
      />
      <Combobox.Trigger
        class="absolute inset-y-0 right-0 flex items-center pr-3 text-muted-foreground hover:text-foreground"
      >
        <ChevronsUpDown class="h-4 w-4" />
      </Combobox.Trigger>
    </div>

    <Combobox.Portal>
      <Combobox.Content
        class={cn(
          "z-50 min-w-[var(--bits-combobox-anchor-width)] overflow-hidden rounded-md border border-border",
          "bg-popover p-1 text-popover-foreground shadow-md outline-none",
          "data-[state=open]:animate-in data-[state=closed]:animate-out data-[state=closed]:fade-out-0 data-[state=open]:fade-in-0"
        )}
        sideOffset={6}
      >
        <Combobox.ScrollArea class="max-h-60 overflow-y-auto">
          {#if filteredFrameworks.length === 0}
            <div class="py-6 text-center text-sm text-muted-foreground">
              Nenhuma tecnologia encontrada.
            </div>
          {:else}
            {#each filteredFrameworks as item (item.value)}
              <Combobox.Item
                value={item.value}
                label={item.label}
                class={cn(
                  "relative flex w-full cursor-default select-none items-center rounded-sm py-2 pl-8 pr-2 text-sm outline-none transition-colors",
                  "data-[highlighted]:bg-accent data-[highlighted]:text-accent-foreground",
                  "data-[disabled]:pointer-events-none data-[disabled]:opacity-50"
                )}
              >
                {#snippet children({ selected })}
                  <span class="absolute left-2 flex h-4 w-4 items-center justify-center">
                    {#if selected}
                      <Check class="h-4 w-4 text-primary" />
                    {/if}
                  </span>
                  <span class="truncate">{item.label}</span>
                {/snippet}
              </Combobox.Item>
            {/each}
          {/if}
        </Combobox.ScrollArea>
      </Combobox.Content>
    </Combobox.Portal>
  </Combobox.Root>

  <p class="text-xs text-muted-foreground">
    Selecionado: <span class="font-mono text-foreground font-medium">{selectedValue}</span>
  </p>
</div>
```

---

#### Receita 2: Dialog Modal com `child` Snippet & Svelte Transitions (`forceMount`)

Esta receita demonstra a orquestração perfeita entre o padrão `child` snippet do Svelte 5, o parâmetro `forceMount` para controlar animações de saída, e as transições nativas do Svelte (`fly` e `fade`):

```svelte
<!-- src/lib/components/ui/AccessibleModal.svelte -->
<script lang="ts">
  import { Dialog } from "bits-ui";
  import { fly, fade } from "svelte/transition";
  import { quintOut } from "svelte/easing";
  import { X, ShieldAlert } from "lucide-svelte";
  import { cn } from "$lib/utils";

  let open = $state(false);

  function handleConfirm() {
    // Lógica de confirmação segura
    open = false;
  }
</script>

<Dialog.Root bind:open>
  <Dialog.Trigger>
    {#snippet child({ props })}
      <button
        {...props}
        class="inline-flex h-10 items-center justify-center rounded-md bg-destructive px-4 py-2 text-sm font-medium text-destructive-foreground shadow hover:bg-destructive/90 transition-colors"
      >
        Excluir Repositório
      </button>
    {/snippet}
  </Dialog.Trigger>

  <Dialog.Portal>
    <!-- Overlay com forceMount para saída fluida via fade -->
    <Dialog.Overlay forceMount>
      {#snippet child({ props, open })}
        {#if open}
          <div
            {...props}
            transition:fade={{ duration: 180 }}
            class="fixed inset-0 z-50 bg-black/60 backdrop-blur-xs"
          />
        {/if}
      {/snippet}
    </Dialog.Overlay>

    <!-- Conteúdo com forceMount e fly físico -->
    <Dialog.Content forceMount>
      {#snippet child({ props, open })}
        {#if open}
          <div class="fixed inset-0 z-50 flex items-center justify-center p-4">
            <div
              {...props}
              transition:fly={{ y: 16, duration: 250, easing: quintOut }}
              class={cn(
                "w-full max-w-lg rounded-xl border border-border bg-card p-6 shadow-2xl",
                "text-card-foreground outline-none relative"
              )}
            >
              <div class="flex items-start gap-4">
                <div class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-destructive/10 text-destructive">
                  <ShieldAlert class="h-5 w-5" />
                </div>
                <div class="space-y-1">
                  <Dialog.Title class="text-lg font-semibold tracking-tight">
                    Confirmar Exclusão Crítica
                  </Dialog.Title>
                  <Dialog.Description class="text-sm text-muted-foreground leading-relaxed">
                    Esta ação é irreversível. Todas as instâncias em execução, branches e dados de auditoria serão permanentemente eliminados.
                  </Dialog.Description>
                </div>
              </div>

              <div class="mt-6 flex justify-end gap-3">
                <Dialog.Close>
                  {#snippet child({ props })}
                    <button
                      {...props}
                      class="inline-flex h-9 items-center justify-center rounded-md border border-input bg-background px-4 text-sm font-medium hover:bg-accent hover:text-accent-foreground transition-colors"
                    >
                      Cancelar
                    </button>
                  {/snippet}
                </Dialog.Close>
                <button
                  onclick={handleConfirm}
                  class="inline-flex h-9 items-center justify-center rounded-md bg-destructive px-4 text-sm font-medium text-destructive-foreground hover:bg-destructive/90 transition-colors"
                >
                  Sim, Excluir Definitivamente
                </button>
              </div>

              <Dialog.Close>
                {#snippet child({ props })}
                  <button
                    {...props}
                    class="absolute top-4 right-4 rounded-sm opacity-70 hover:opacity-100 transition-opacity focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring"
                    aria-label="Fechar modal"
                  >
                    <X class="h-4 w-4" />
                  </button>
                {/snippet}
              </Dialog.Close>
            </div>
          </div>
        {/if}
      {/snippet}
    </Dialog.Content>
  </Dialog.Portal>
</Dialog.Root>
```

---

#### Receita 3: PinInput de Alta Precisão (Verificação 2FA / OTP)

```svelte
<!-- src/lib/components/ui/TwoFactorPinInput.svelte -->
<script lang="ts">
  import { PinInput } from "bits-ui";
  import { cn } from "$lib/utils";

  let pinValue = $state("");
  let isComplete = $state(false);

  function handleComplete(value: string) {
    isComplete = true;
    console.log("Código OTP completo digitado:", value);
  }
</script>

<div class="flex flex-col items-center space-y-4 p-6 bg-card rounded-xl border border-border max-w-sm mx-auto shadow-sm">
  <div class="text-center space-y-1">
    <h3 class="text-base font-semibold text-foreground">Autenticação em Dois Fatores</h3>
    <p class="text-xs text-muted-foreground">Digite o código de 6 dígitos gerado pelo seu app autenticador.</p>
  </div>

  <PinInput.Root
    bind:value={pinValue}
    onComplete={handleComplete}
    maxlength={6}
    class="flex items-center gap-2"
  >
    {#snippet children({ cells })}
      <div class="flex gap-2">
        {#each cells as cell, index (index)}
          <PinInput.Cell
            {cell}
            class={cn(
              "relative flex h-12 w-10 items-center justify-center rounded-md border border-input bg-background font-mono text-lg font-bold text-foreground transition-all",
              "focus:border-primary focus:ring-2 focus:ring-ring/20 focus:outline-none",
              "data-[active]:border-ring data-[active]:ring-2 data-[active]:ring-ring/20"
            )}
          >
            {#if cell.char !== null}
              <span>{cell.char}</span>
            {/if}
            {#if cell.isActive}
              <div class="absolute inset-x-2 bottom-1.5 h-0.5 bg-primary animate-pulse" />
            {/if}
          </PinInput.Cell>
          {#if index === 2}
            <div class="flex items-center text-muted-foreground font-bold">-</div>
          {/if}
        {/each}
      </div>
    {/snippet}
  </PinInput.Root>

  {#if isComplete}
    <p class="text-xs text-emerald-600 dark:text-emerald-400 font-medium animate-in fade-in">
      ✓ Código validado com sucesso. Verificando...
    </p>
  {/if}
</div>
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir o `DESIGN_BLUEPRINT.md` de qualquer projeto baseado em **Svelte 5** ou **SvelteKit**, a IA deve seguir as seguintes diretrizes mandatórias:

### 1. Declaração de Fundação no Tech Stack
```markdown
### Component Primitives & Accessibility Engine
- **Biblioteca de Primitivas**: Bits UI v1 (`bits-ui`)
- **Arquitetura Reativa**: Svelte 5 Native (Runes: `$state`, `$derived`, `$bindable` e `child` Snippets)
- **Design System Layer**: Componentes encapsulados em `$lib/components/ui/` utilizando convenção `shadcn-svelte` com Tailwind CSS v4.
- **Engine Flutuante & Datas**: `@floating-ui/dom` (Posicionamento) e `@internationalized/date` (Calendários).
```

### 2. Padrão Arquitetural de Encapsulamento
- **Nunca** instancie primitivas brutas do `bits-ui` diretamente nas páginas ou telas de negócio (`routes/+page.svelte`).
- Crie sempre uma camada de abstração em `$lib/components/ui/` (ex: `button.svelte`, `dialog.svelte`, `popover.svelte`) que combine a primitiva Bits UI com os estilos e variantes de design tokens do projeto.
- Exponha props semânticas limpas e utilize `{#snippet child({ props })}` para permitir composabilidade total por componentes pais.

### 3. Integração com Tailwind CSS v4 & OKLCH
- Padronize todos os estados interativos utilizando as variantes de atributos de dados providas pelo Bits UI:
  - `data-[state=open]` e `data-[state=closed]` para controle de opacidade e transformações.
  - `data-[highlighted]` para hover e navegação de teclado em listas (`Combobox`, `Select`, `DropdownMenu`).
  - `data-[disabled]` para atenuar elementos desabilitados com `opacity-50 pointer-events-none`.
- Assegure que as variáveis de tema (`--background`, `--foreground`, `--primary`, `--border`) sejam declaradas em espaço perceptual OKLCH no arquivo de estilos globais para garantir transições suaves entre Modo Claro e Escuro.

### 4. Checklist de Validação de Acessibilidade
- [ ] Todos os gatilhos (`Trigger`) possuem rótulo visível ou atributo `aria-label` explícito.
- [ ] Nenhum componente com `{#snippet child({ props })}` omite a propagação `{...props}`.
- [ ] Qualquer container animado com Svelte Transitions utiliza `forceMount` para prevenir desmontagem instantânea sem animação de saída.
- [ ] Formulários associados a validações de esquema (Zod) utilizam a tríade Bits UI + Formsnap para vincular atributos `aria-invalid` e `aria-describedby` automaticamente aos textos de erro.
