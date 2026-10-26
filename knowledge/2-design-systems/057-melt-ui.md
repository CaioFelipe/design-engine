---
id: "melt-ui"
name: "Melt UI"
url: "https://melt-ui.com/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Headless Action Architecture", "Zero DOM Element Lock-in", "WAI-ARIA APG Compliance", "Svelte 5 Runes Native", "Unstyled BYOS (Bring Your Own Styles)", "Svelte Native Motion Integration"]
densidade_informacao: "Flexivel"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS/Headless)"
stack_frameworks: ["Svelte 5", "SvelteKit", "Svelte 4", "melt (Next Runes)", "@melt-ui/svelte", "Tailwind CSS v4 / v3", "TypeScript", "svelte/transition", "svelte/motion", "Floating UI"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "Plus Jakarta Sans", "JetBrains Mono", "GT Maru"]
  paletas_ideais: ["Magnum Amber / Honey Dark", "Deep Slate Monochromes", "OKLCH Neutral Grays", "Obsidian & Emerald", "High-Contrast Zinc"]
  combinacoes_recomendadas: ["Bits UI", "shadcn-svelte", "Tailwind CSS", "Lucide Svelte", "Svelte Native Transitions (slide, fly, fade)", "Floating UI"]
  conflitos_esteticos: ["Bibliotecas monolíticas opinadas com DOM engessado (Bootstrap, Material-UI legada)", "Soluções CSS que forçam especificidade excessiva via seletores globais desgovernados"]
---

# Melt UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Melt UI** (`https://melt-ui.com/`) é o padrão de ouro indiscutível da engenharia de componentes *headless* no ecossistema Svelte. Criado e mantido por engenheiros prolíficos da comunidade Svelte — como **Thomas G. Lopes** (@TGlide), **Adrian Gonzàlez** (@AdrianGonz97) e com contribuições seminais de **Hunter Johnston** (@huntabyte) —, o Melt UI nasceu para solucionar a lacuna crítica de primitivas acessíveis que bibliotecas como Radix UI e Zag.js já haviam solucionado no React.

No entanto, em vez de importar padrões alienígenas de outros frameworks (como o modelo excessivamente componentizado e propenso a wrapper divs do React), o Melt UI foi desenhado desde o primeiro dia **para abraçar os superpoderes idiomáticos do Svelte**.

### A Filosofia do "Action Builder" & Zero DOM Lock-in

O grande diferencial do Melt UI em relação a bibliotecas convencionais de interface é o abandono absoluto do conceito de componentes visuais fechados (`<Dialog>`, `<Dropdown>`). O Melt fornece **Builders**: funções construtoras puras que retornam um conjunto harmonioso de *stores* (no Svelte 3/4) ou *runes/classes* (no Svelte 5 Melt Next), atributos WAI-ARIA calculados e **Actions Svelte nativas** (`use:`).

1. **Liberdade Estrutural Total (Zero DOM Wrapper Hell)**:
   Em bibliotecas React tradicionais ou portas ingênuas, o desenvolvedor é forçado a aninhar dezenas de tags proprietárias que frequentemente injetam nós DOM parasitas (`<div>` extras que quebram o display `flex`, `grid` ou afetam o cálculo de `:first-child`). No Melt UI, o desenvolvedor escreve HTML semântico comum (`<button>`, `<section>`, `<input>`, `<dialog>`) e acopla a inteligência do Melt via diretiva de ação:
   ```svelte
   <button use:melt={$trigger}>Abrir Gaveta</button>
   ```
   Não há elementos intermediários, não há marcação oculta e não há classes CSS embutidas. O desenvolvedor é o senhor soberano do DOM.

2. **O Pré-Processador Mágico (`@melt-ui/pp`)**:
   Em Svelte 4, a linguagem não permitia nativamente mesclar atributos reativos (`{...$trigger}`) e ações DOM (`use:trigger`) em um único comando limpo. A equipe do Melt UI construiu o **`@melt-ui/pp`**, um pré-processador de compilação AST que permite a sintaxe ultralímpida:
   ```svelte
   <!-- O que o desenvolvedor escreve: -->
   <button use:melt={$trigger}>Menu</button>

   <!-- O que o pré-processador compila nos bastidores: -->
   <button {...$trigger} use:$trigger.action>Menu</button>
   ```
   Essa engenhosidade reduziu o *boilerplate* a praticamente zero, elevando o Developer Experience (DX) a um patamar incomparável na história do front-end em Svelte.

3. **A Nova Fronteira: Melt Next & Svelte 5 Runes (`melt`)**:
   Com o lançamento do Svelte 5 e a substituição das *stores* clássicas pelo sistema de reatividade fina de **Runes** (`$state`, `$derived`, `$effect`), o Melt UI evoluiu para o pacote **`melt`** (conhecido como *Melt Next*). A arquitetura foi reengenheirada em torno de classes TypeScript e getters/setters reativos:
   ```svelte
   <script lang="ts">
     import { Toggle } from 'melt/builders';
     let pressed = $state(false);
     const toggle = new Toggle({
       value: () => pressed,
       onValueChange: (v) => (pressed = v),
     });
   </script>

   <button {...toggle.trigger}>
     {toggle.value ? "Ativo" : "Inativo"}
   </button>
   ```
   Além do modo *Builder*, o Melt Next fornece invólucros amigáveis com Snippets do Svelte 5 (`melt/components`), possibilitando a ligação bidirecional direta via `bind:value` quando a equipe prefere sintaxe declarativa via template.

### Acessibilidade Rigorosa (WAI-ARIA APG by Default)

O Melt UI não apenas adiciona atributos cosméticos: ele implementa a íntegra das diretrizes do **WAI-ARIA Authoring Practices Guide (APG)**:
- **Focus Management & Trapping**: Em modais, gavetas e menus, o foco do teclado é cirurgicamente retido no elemento ativo, impedindo que o tabulador escape para o fundo da página, e devolvendo o foco milimétrico para o gatilho de origem assim que a janela fecha.
- **Roving Tabindex & Typeahead**: Menus complexos, barras de ferramentas e árvores de diretórios implementam navegação por setas (`ArrowUp`, `ArrowDown`, `Home`, `End`), além de salto instantâneo ao digitar as primeiras letras de um item (*typeahead*).
- **Atributos de Estado Contextuais**: O Melt UI sincroniza dinamicamente atributos semânticos (`aria-expanded`, `aria-selected`, `aria-controls`, `aria-haspopup`, `aria-disabled`) e gera atributos customizados no formato `data-melt-*` e `data-state="open|closed"` / `data-disabled`, fornecendo os pontos de ancoragem perfeitos para estilização reativa via CSS moderno ou Tailwind.

### A Fundação Oculta do Ecossistema: Bits UI e shadcn-svelte

O impacto do Melt UI é tão profundo que ele se tornou a base motriz de quase todo o ecossistema moderno de UI em Svelte. O consagrado projeto **`shadcn-svelte`** (a versão oficial comunitária do shadcn/ui) apoia-se diretamente nas primitivas headless do **`Bits UI`**, que por sua vez foi gerado e arquitetado sob a tutela direta da infraestrutura de comportamentos do Melt UI. Entender Melt UI é dominar o núcleo funcional de qualquer design system de alta performance construído em Svelte.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados

1. **SaaS B2B de Alta Complexidade & Workspaces Operacionais em Svelte/SvelteKit**:
   Aplicações onde o usuário passa 8 horas por dia operando tabelas, formulários aninhados, seletores multi-nível, painéis retráteis e modais encadeados. A solidez de acessibilidade e a ausência de nós DOM extras garantem renderização instantânea sem nenhum gargalo de reconciliação de Virtual DOM.
2. **Developer Tools, Ambientes de Código (IDEs Web) e Cloud Consoles**:
   Sistemas que necessitam de atalhos de teclado globais, menus de contexto acionados com botão direito (`use:melt={$contextMenu}`), barras de navegação estilo desktop (`Menubar`), árvores de diretórios (`Tree`) e comboboxes com filtros rápidos estilo terminal.
3. **Design Systems Corporativos Customizados (White-Label)**:
   Equipes de produto que possuem uma identidade visual única e rejeitam categoricamente bibliotecas opinadas que já trazem botões arredondados ou sombras pré-definidas. O Melt UI entrega 100% da lógica e 0% da estética, permitindo aplicar qualquer guia de marca sem necessidade de sobrescrever CSS legado com especificidade inflada.
4. **Aplicações Fintech, Bancárias e de Cibersegurança**:
   Interfaces de alta conformidade legal onde falhas em acessibilidade digital (conformidade WCAG 2.1 AA/AAA) acarretam auditorias, multas e penalidades regulatórias.

### Papel no Ritmo Visual (A Regra 60-30-10)

- **60% — Espinha Dorsal Funcional da Interface (A Lógica Invisível)**:
  O Melt UI é a alma funcional da camada de **60%**. Ele gerencia as estruturas invisíveis: seletor de abas (`Tabs`), acordeões de perguntas frequentes (`Accordion`), formulários com interruptores (`Switch`), campos de data com máscara acessível (`DateField`) e sliders de intervalo financeiro (`Slider`). Ele não compete com a identidade visual da marca; ele viabiliza a mecânica sobre a qual o design repousa.
- **30% — Camada de Navegação, Orquestração e Micro-Interações**:
  Ao integrar os builders dinâmicos do Melt (`DropdownMenu`, `Dialog`, `Popover`, `Tooltip`) com as **transições nativas do Svelte** (`transition:slide`, `transition:fly`, `svelte/motion`), essa camada ganha uma física de movimento com aceleração de hardware nativa (CSS transitions compiladas pelo compilador do Svelte), fluindo a 120 FPS nos monitores mais exigentes.
- **10% — Protagonistas Satélites (Showstoppers)**:
  O Melt UI fornece os gatilhos e a telemetria para os 10% de impacto visual. Por exemplo, abrir um `Dialog` do Melt pode disparar uma explosão de partículas canvas, um shader WebGL de fundo ou um efeito de distorção tipográfica sem que a lógica de retenção de foco e acessibilidade seja comprometida.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

1. **Projetos Fora do Ecossistema Svelte (React, Vue, Solid, Angular)**:
   O Melt UI é desenhado com exclusividade para o modelo de compilação, diretivas de ação (`use:`) e reatividade do Svelte (v3, v4 e Runes no v5). Em ecossistemas React, a escolha correta é Radix UI ou Ark UI; no Vue, Radix Vue; em múltiplos frameworks, Zag.js.
2. **Projetos de Prototipagem Ultra-Rápida sem Equipe de Design/CSS**:
   Se você precisa levantar um painel administrativo em 2 horas e não deseja escrever nenhuma linha de CSS ou classes Tailwind, o Melt UI é a ferramenta errada. Sendo 100% headless e desprovido de estilos, botões e modais parecerão elementos HTML crus do navegador se não forem estilizados manualmente. Nesses casos, bibliotecas com estilos prontos (como DaisyUI, Skeleton UI ou shadcn-svelte já configurado) são mais adequadas.
3. **Páginas 100% Estáticas de Conteúdo Puro (SSG sem Interatividade)**:
   Blogs textuais e documentações estáticas onde links convencionais e tags HTML nativas (`<details><summary>`) já cumprem o papel sem necessidade de carregar scripts de hidratação de JavaScript.

---

### ⚠️ Erros Comuns de Implementação & Anti-Padrões no Melt UI

1. **A Falha do `forceVisible` ao usar Transições Nativas do Svelte**:
   *O Erro Clássico*: Por padrão, o Melt UI controla a visibilidade de conteúdos dinâmicos injetando `display: none` e o atributo `hidden` no nó DOM para evitar qualquer flash visual (FOUC). Quando um desenvolvedor tenta adicionar uma transição Svelte direta (`<div use:melt={$content} transition:slide>`), o componente fecha abruptamente sem animação porque o Melt força `display: none` no mesmo milissegundo do clique.
   *A Correção Obrigatória*: Em qualquer componente onde se deseje transições do Svelte (`slide`, `fade`, `fly`), é imperativo habilitar `forceVisible: true` na inicialização do builder e envolver o elemento em um bloco condicional `{#if $open}`:
   ```svelte
   const { elements: { content, trigger }, states: { open } } = createCollapsible({
     forceVisible: true // <-- Permite que a transição de saída do Svelte conclua antes de desmontar
   });

   {#if $open}
     <div use:melt={$content} transition:slide={{ duration: 200 }}>...</div>
   {/if}
   ```
2. **"Headless Abandonment" (Esquecer Estilos de Foco e Estados WAI-ARIA)**:
   Como o Melt injeta atributos como `data-state="open|checked"`, `aria-selected="true"` e `data-disabled`, é comum desenvolvedores iniciantes estilizarem apenas os estados felizes (`hover`), esquecendo completamente de estilizar anéis de foco (`focus-visible:ring-2`) e estilos visuais de itens inativos. O leitor de tela saberá que o botão está focado, mas um usuário de teclado visual ficará cego na interface.
3. **Sobrescrever Atributos Calculados no Spread**:
   Colocar atributos estáticos após o spread do builder que anulam a acessibilidade (ex: `<button {...$trigger} role="link">`). O Melt calcula os papéis semânticos corretos segundo a especificação W3C; sobrescrevê-los quebra a árvore de acessibilidade.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

O Melt UI oferece um leque completo de construtores de alta precisão. Abaixo estão catalogados 10 dos mais sofisticados componentes da suíte:

### 1. Combobox / Autocomplete
- **Anatomia Visual**: Campo de entrada de texto (`input`) integrado a uma lista suspensa virtualizável (`menu`) com rolagem suave, filtragem de texto instantânea, destaque tipográfico das letras coincidentes e indicador de item selecionado (`data-highlighted`).
- **Gatilho de Interação**: Foco no input, digitação com debounce reativo, navegação via setas `ArrowDown`/`ArrowUp`, seleção via tecla `Enter` e cancelamento via `Escape`.
- **Onde Encaixar**: Hero (buscas globais Cmd+K), Cabeçalho da aplicação, Formulários complexos de seleção de países/moedas/produtos.

### 2. Dialog & Alert Dialog (Modal Acessível)
- **Anatomia Visual**: Janela modal centralizada com camada de sobreposição escura com desfoque de fundo (`backdrop-blur-sm`), trava automática de rolagem na tag `<body>` (`body-scroll-lock`), portal nativo para renderização no final do DOM (`data-portal`) e botão de fechamento com ícone atenuado.
- **Gatilho de Interação**: Clique no gatilho (`$trigger`), atalho de teclado global, tecla `Escape` ou clique fora da área do conteúdo (`dismissable`).
- **Onde Encaixar**: Dashboards operacionais, confirmações de exclusão destrutiva, formulários modais de cadastro rápido e visualizadores de mídia.

### 3. Date Picker & Date Range Picker
- **Anatomia Visual**: Grade matemática do calendário (`table`/`grid`) governada pelo padrão WAI-ARIA Calendar Grid, botões de navegação mensal/anual rápida, suporte a seleção de intervalos contínuos de datas com highlight dos dias intermediários e input com máscara estrita de dígitos.
- **Gatilho de Interação**: Clique para expansão do popover, digitação direta no campo de data ou navegação completa por teclado dentro da matriz de dias (`ArrowLeft`/`ArrowRight` para dias, `ArrowUp`/`ArrowDown` para semanas, `PageUp`/`PageDown` para meses).
- **Onde Encaixar**: Sistemas de reserva de viagens/hotéis, filtros de relatórios em SaaS Analytics, seletores de períodos contábeis em fintechs.

### 4. PIN Input / OTP Input (One-Time Password)
- **Anatomia Visual**: Sequência elegante de 4 a 8 células retangulares isoladas para um único caractere cada, com cursor de texto oculto (`caret-transparent`), ponto de foco destacado (`focus:border-amber-500`), suporte visual a máscara para senhas (`••••`) e animação sutil de pulso.
- **Gatilho de Interação**: Digitação rápida com auto-avanço instantâneo para a célula adjacente, tecla `Backspace` com auto-recuo e apagamento do valor anterior, e colagem inteligente de strings completas da área de transferência (`Cmd+V` preenchendo todos os blocos e disparando o callback `onComplete`).
- **Onde Encaixar**: Telas de autenticação de dois fatores (2FA/MFA), validação de transações Pix/Wire, desbloqueio de carteiras Web3.

### 5. Context Menu & Menubar (Menus Desktop de Alta Precisão)
- **Anatomia Visual**: Painéis flutuantes posicionados cirurgicamente sob o cursor do mouse ou alinhados horizontalmente no topo da aplicação, com divisores finos de seção, atalhos de teclado alinhados à direita (ex: `⌘+C`, `Shift+Del`), checkboxes embutidos e submenus desdobráveis com detecção inteligente de borda de tela (Flip & Collision detection via Floating UI).
- **Gatilho de Interação**: Clique com o botão direito do mouse no alvo (`contextmenu`), navegação fluida por setas e suporte a hover sobre itens de submenu.
- **Onde Encaixar**: Aplicações ricas tipo desktop (editores de imagem, planilhas colaborativas, IDEs no navegador e gerenciadores de arquivos).

### 6. Collapsible & Accordion
- **Anatomia Visual**: Painéis expansíveis organizados em pilhas verticais com ícones de chevron que rotacionam perfeitamente em 180 graus (`transition-transform duration-200 data-[state=open]:rotate-180`), mantendo fluxo tipográfico contínuo.
- **Gatilho de Interação**: Clique no gatilho ou ativação por teclado (`Enter` ou `Space`). Suporta modos exclusivo (apenas uma aba aberta por vez) ou múltiplo.
- **Onde Encaixar**: Seções de FAQ em páginas de Pricing, sidebars de navegação em árvore, painéis de configurações avançadas.

### 7. Range Slider com Suporte Multi-Thumb
- **Anatomia Visual**: Trilho horizontal fino (`track`) preenchido progressivamente por uma barra de destaque (`range`), com uma ou duas alças circulares ergonômicas (`thumb`) que projetam sombras volumétricas suaves e anéis de foco ativos. A posição é expressa dinamicamente via variável CSS nativa (`--percentage`).
- **Gatilho de Interação**: Arrastar com mouse/touch, clique direto no trilho para teletransporte do valor ou ajuste granular por setas de teclado (`ArrowRight` avança 1 passo, `PageUp` ou `Shift+Arrow` avança saltos maiores).
- **Onde Encaixar**: Calculadoras de ROI em páginas de produto, seletores de faixa de preço em e-commerces de precisão, painéis de equalização de áudio e ajustes de densidade.

### 8. Tabs com Indicador Deslizante
- **Anatomia Visual**: Barra horizontal ou vertical de abas de navegação contendo painéis associados. O item ativo recebe realce de superfície ou pode contar com uma pílula deslizante fluida orientada por coordenadas de bounding box.
- **Gatilho de Interação**: Clique no cabeçalho ou navegação horizontal rápida (`ArrowLeft`/`ArrowRight`), com ativação instantânea no foco ou mediante confirmação com tecla `Enter`.
- **Onde Encaixar**: Páginas de configurações de perfil, alternador de planos Mensal/Anual no Pricing, visualizadores de código multi-linguagem.

### 9. Table of Contents (ToC Automatizado)
- **Anatomia Visual**: Lista lateral estruturada e indentada de tópicos e subtópicos de um artigo longo ou documentação técnica, com um marcador lateral colorido que se desloca suavemente indicando a seção sob leitura ativa.
- **Gatilho de Interação**: Rolagem passiva da página monitorada internamente por instâncias otimizadas de `IntersectionObserver`, combinada com clique para rolagem suave (`smooth scroll`) até o cabeçalho correspondente.
- **Onde Encaixar**: Documentações de desenvolvedor, artigos de engenharia, bases de conhecimento ricas e relatórios analíticos corporativos.

### 10. Tree View (Navegação Hierárquica em Árvore)
- **Anatomia Visual**: Árvore com múltiplos níveis de aninhamento, ícones dinâmicos de pastas abertas/fechadas e arquivos de diferentes extensões, guias verticais conectando os ramos e estados de seleção com preenchimento sutil de fundo.
- **Gatilho de Interação**: `ArrowRight` abre o diretório focado; segundo `ArrowRight` entra no primeiro filho; `ArrowLeft` fecha a pasta ou retorna ao pai; tecla `*` (asterisco) expande todos os nós do mesmo nível.
- **Onde Encaixar**: Explorador de repositórios git, gerenciadores de storage em nuvem, árvores de permissões em plataformas SaaS Enterprise.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Ambiente

Para projetos em SvelteKit utilizando a abordagem moderna de Tailwind CSS e suporte completo a TypeScript:

```bash
# Para projetos Svelte 5 (Melt Next com Runes):
pnpm add melt
pnpm add -D tailwindcss @tailwindcss/vite lucide-svelte clsx tailwind-merge

# Para projetos legados em Svelte 4 / 3 (Melt UI Clássico):
pnpm add @melt-ui/svelte
pnpm add -D @melt-ui/pp
```

Se estiver utilizando o Svelte 4, configure o pré-processador no `svelte.config.js`:
```javascript
import { sequence, preprocessMeltUI } from '@melt-ui/pp';
import adapter from '@sveltejs/adapter-auto';
import { vitePreprocess } from '@sveltejs/vite-plugin-svelte';

/** @type {import('@sveltejs/kit').Config} */
const config = {
  preprocess: sequence([
    vitePreprocess(),
    preprocessMeltUI() // <-- Garante o parsing transparente de use:melt={$trigger}
  ]),
  kit: {
    adapter: adapter()
  }
};

export default config;
```

---

### Física de Movimento, Transições & Curvas de Aceleração

O Melt UI trabalha em harmonia direta com os mecanismos de animação de alto desempenho do Svelte. Em vez de calcular frames via JavaScript em tempo de execução, o Svelte compila as diretivas `transition:` diretamente em *CSS keyframes* executados no thread de composição da GPU.

#### Curvas Bézier & Easing Ideais

Para interfaces de produto com estética profissional (nível Apple/Linear), adote as seguintes curvas com as transições do Svelte:

```typescript
// Curva Quint Out — desaceleração elegante para entradas de modais e gavetas
export function quintOut(t: number): number {
  return --t * t * t * t * t + 1;
}

// Equivalente CSS cúbico para transições de propriedades Tailwind:
// cubic-bezier(0.16, 1, 0.3, 1) -> Exponential Fast-Out Slow-In
```

Configuração de Física com `svelte/motion`:
```typescript
import { spring } from 'svelte/motion';

// Mola responsiva para indicadores de abas e sliders:
export const indicatorSpring = spring(
  { x: 0, width: 0 },
  {
    stiffness: 0.18, // Firmeza: rápida resposta ao toque sem sensação elástica de brinquedo
    damping: 0.72,   // Amortecimento: estabiliza suavemente sem oscilações infinitas
    precision: 0.005
  }
);
```

---

### Receitas de Código Funcionais

#### Receita 1: Modal Acessível (`Dialog`) com Transições Nativas e Tailwind CSS

Esta receita demonstra a arquitetura do Melt UI em Svelte 5 / Svelte 4 com suporte à saída suave animada via `forceVisible: true`:

```svelte
<!-- src/lib/components/AccessibleDialog.svelte -->
<script lang="ts">
  import { createDialog, melt } from '@melt-ui/svelte';
  import { fade, scale } from 'svelte/transition';
  import { quintOut } from 'svelte/easing';
  import { X, ShieldCheck } from 'lucide-svelte';

  const {
    elements: { trigger, overlay, content, title, description, close, portalled },
    states: { open }
  } = createDialog({
    forceVisible: true, // Crucial: transfere o controle de desmontagem para o bloco #if do Svelte
    preventScroll: true
  });
</script>

<!-- Botão de Acionamento -->
<button
  use:melt={$trigger}
  class="inline-flex items-center gap-2 rounded-xl bg-amber-500 px-5 py-2.5 font-medium text-zinc-950 shadow-md shadow-amber-500/10 transition-all hover:bg-amber-400 active:scale-[0.98] focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-amber-500 focus-visible:ring-offset-2 focus-visible:ring-offset-zinc-950"
>
  <ShieldCheck class="size-4" />
  <span>Confirmar Autenticação</span>
</button>

<!-- Container com Portal Automático no Body -->
<div use:melt={$portalled}>
  {#if $open}
    <!-- Fundo Escurecido com Desfoque -->
    <div
      use:melt={$overlay}
      transition:fade={{ duration: 220 }}
      class="fixed inset-0 z-50 bg-black/60 backdrop-blur-sm"
    />

    <!-- Janela de Conteúdo do Modal -->
    <div
      class="fixed inset-0 z-50 grid place-items-center p-4 overflow-y-auto"
    >
      <div
        use:melt={$content}
        transition:scale={{ duration: 250, start: 0.96, easing: quintOut }}
        class="relative w-full max-w-lg rounded-2xl border border-zinc-800 bg-zinc-900/95 p-6 text-zinc-100 shadow-2xl shadow-black/80 backdrop-blur-xl focus:outline-none"
      >
        <!-- Cabeçalho -->
        <div class="flex items-start justify-between">
          <div class="space-y-1">
            <h2
              use:melt={$title}
              class="text-xl font-semibold tracking-tight text-white"
            >
              Autenticação de Segurança
            </h2>
            <p
              use:melt={$description}
              class="text-sm text-zinc-400 leading-relaxed"
            >
              Confirme a aprovação do dispositivo antes de prosseguir com a emissão do token criptográfico de acesso.
            </p>
          </div>

          <button
            use:melt={$close}
            aria-label="Fechar"
            class="rounded-lg p-1 text-zinc-400 transition-colors hover:bg-zinc-800 hover:text-white focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-amber-500"
          >
            <X class="size-5" />
          </button>
        </div>

        <!-- Conteúdo Interno do Formulário -->
        <div class="mt-6 rounded-xl border border-zinc-800/80 bg-zinc-950/60 p-4 font-mono text-xs text-zinc-300">
          <div class="flex items-center justify-between py-1">
            <span class="text-zinc-500">Origem da Sessão:</span>
            <span>192.168.1.104 (Belo Horizonte, BR)</span>
          </div>
          <div class="flex items-center justify-between py-1">
            <span class="text-zinc-500">Chave Pública:</span>
            <span class="truncate max-w-[200px]">ed25519:8b7a4f91...c4</span>
          </div>
        </div>

        <!-- Rodapé de Ações -->
        <div class="mt-6 flex items-center justify-end gap-3">
          <button
            use:melt={$close}
            class="rounded-xl px-4 py-2 text-sm font-medium text-zinc-300 transition-colors hover:bg-zinc-800 hover:text-white"
          >
            Cancelar
          </button>
          <button
            on:click={() => {
              // Executa a confirmação da transação
              $open = false;
            }}
            class="rounded-xl bg-amber-500 px-4 py-2 text-sm font-semibold text-zinc-950 transition hover:bg-amber-400 active:scale-95"
          >
            Autorizar Dispositivo
          </button>
        </div>
      </div>
    </div>
  {/if}
</div>
```

---

#### Receita 2: OTP / PIN Input em Svelte 5 Runes (Melt Next)

Apresentando a nova API orientada a classes e runes do pacote **`melt`** para Svelte 5:

```svelte
<!-- src/lib/components/PinVerification.svelte -->
<script lang="ts">
  import { PinInput } from 'melt/builders';

  let pinValue = $state('');
  let isComplete = $state(false);

  // Instanciação orientada a Runes e Getters reativos
  const pin = new PinInput({
    value: () => pinValue,
    onValueChange: (v) => {
      pinValue = v;
      isComplete = false;
    },
    onComplete: (v) => {
      isComplete = true;
      console.log('Código OTP validado com sucesso:', v);
    }
  });
</script>

<div class="flex flex-col items-center gap-4 p-6 rounded-2xl border border-zinc-800 bg-zinc-950 text-white max-w-sm mx-auto shadow-xl">
  <div class="text-center space-y-1">
    <h3 class="font-semibold text-base text-zinc-100">Código de Verificação</h3>
    <p class="text-xs text-zinc-400">Insira o código de 4 dígitos enviado ao seu dispositivo.</p>
  </div>

  <!-- Raiz do PIN Input -->
  <div {...pin.root} class="flex items-center justify-center gap-2.5">
    {#each pin.inputs as input, i}
      <input
        {...input}
        class="size-12 rounded-xl border-2 border-zinc-700 bg-zinc-900 text-center font-mono text-xl font-bold text-amber-400 outline-none transition-all placeholder:text-zinc-600 hover:border-zinc-500 focus:border-amber-400 focus:ring-4 focus:ring-amber-500/20 disabled:cursor-not-allowed disabled:opacity-50"
        placeholder="○"
      />
    {/each}
  </div>

  {#if isComplete}
    <p class="text-xs font-medium text-emerald-400 animate-pulse">
      ✓ Verificando token de acesso instantâneo...
    </p>
  {/if}
</div>
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao arquitetar soluções de software em Svelte e SvelteKit no documento `DESIGN_BLUEPRINT.md`, a Inteligência Artificial e a equipe técnica devem aderir às seguintes diretrizes estritas:

1. **Declaração Arquitetural do Headless Engine**:
   - Sempre declare formalmente o **Melt UI** (ou sua camada empacotada **Bits UI**) como a *camada fundacional de acessibilidade WAI-ARIA* para o ecossistema Svelte.
   - Em projetos SvelteKit rodando Svelte 5, especifique o uso do pacote moderno **`melt`** com a API de Runes (`melt/builders`), evitando a introdução de stores legadas baseadas em `writable()`.
2. **Separação Rígida entre Lógica e Estilização**:
   - Proíba qualquer tentativa de estipular classes CSS dentro dos construtores Melt. Toda a estilização deve residir no template HTML do componente (`class="..."`), alavancando os seletores contextuais gerados pelo Melt:
     - `data-[state=open]:...` / `data-[state=closed]:...`
     - `data-[state=checked]:...` / `data-[state=unchecked]:...`
     - `data-highlighted:...`
     - `disabled:...` / `data-disabled:...`
3. **Regra de Ouro da Desmontagem Animada (`forceVisible: true`)**:
   - Todo componente com dropdown, flyout, modal, sheet ou sanfona que utilizar `transition:slide`, `transition:fade`, `transition:fly` ou bibliotecas como Svelte Motion DEVE conter a propriedade explícita `forceVisible: true` declarada no seu construtor, operando em conjunto com um bloco `{#if $open}` ou condicional de estado.
4. **Governança de Portais e Empilhamento Z-Index**:
   - Elementos sobrepostos (Modais, Tooltips, Menus de Contexto, Popovers) devem SEMPRE utilizar o nó `portalled` do builder (`use:melt={$portalled}` ou wrapper equivalente). Isso garante que o elemento seja transportado para a raiz do elemento `<body>`, neutralizando problemas de contexto de empilhamento (`stacking context` / `overflow: hidden`) herdados de cartões pais.
5. **Combinação Estruturada no Blueprint**:
   - **Camada Lógica**: Melt UI (`@melt-ui/svelte` ou `melt`)
   - **Camada de Ícones**: `lucide-svelte`
   - **Camada Utilitária de Estilos**: `tailwind-merge` + `clsx` via função `cn()`
   - **Camada de Transição**: Diretivas nativas compiladas do Svelte (`svelte/transition` + `svelte/easing`) para máxima economia de bundle e performance de 120 FPS.
