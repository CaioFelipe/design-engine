---
id: "058-skeleton-dev"
name: "Skeleton UI"
url: "https://www.skeleton.dev/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Adaptive System Design", "Tailwind Semantic Utility", "Multi-Engine Reactive", "High-Contrast Accessible"]
densidade_informacao: "Flexivel"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS/Headless) a Medio (Zag.js State Machines)"
stack_frameworks: ["Tailwind CSS v4/v3", "Svelte 5", "React", "Zag.js", "TypeScript"]
compatibilidade:
  fontes_ideais: ["Inter", "Geist Sans", "Plus Jakarta Sans", "Fira Code", "system-ui"]
  paletas_ideais: ["Cerberus (Deep Slate / Violet)", "Catppuccin (Mocha Pastel)", "Crimson (High Contrast Red / Zinc)", "Wintry (Cool Nordic Cyan)"]
  combinacoes_recomendadas: ["Lucide Icons", "Radix UI", "Bits UI", "Melt UI", "Tailwind Plus"]
  conflitos_esteticos: ["DaisyUI (colisão direta de classes utilitárias e tokens)", "Flowbite (conflito de seletores e prefixos)", "Chakra UI / MUI (CSS-in-JS pesado concorrente)"]
---

# Skeleton UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Skeleton** (desenvolvido pela equipe da Skeleton Labs sob liderança de Chris Simmons / `@endigo9740`) consolidou-se na sua terceira geração (**Skeleton v3**) não apenas como a biblioteca de interface de referência do ecossistema Svelte, mas como um **Design System adaptativo e multiplataforma de classe corporativa**. Projetado diretamente sobre o Tailwind CSS e máquinas de estados finitos do **Zag.js** (criado pelos mantenedores do Chakra UI), o Skeleton transcendeu o isolamento de framework para oferecer paridade rigorosa entre **Svelte 5** (com Runes e Snippets) e **React**, além de templates para Vue, Solid e Astro.

### A Tríade da Assinatura Skeleton

1. **Arquitetura de Presets Semânticos (`preset-filled`, `preset-tonal`, `preset-outlined`)**:
   Em vez de exigir que o desenvolvedor componha dezenas de classes utilitárias repetitivas em cada elemento (`bg-indigo-600 hover:bg-indigo-700 text-white dark:bg-indigo-500...`), o Skeleton introduz camadas semânticas de alta abstração. As classes utilitárias de preset resolvem automaticamente o background, bordas, estados de hover, active e foco, adaptando-se instantaneamente ao tema ativo do projeto.
2. **Sistema de Pareamento Cromático & Contraste Automático**:
   Uma das maiores fragilidades dos design systems baseados em Tailwind é o risco de perda de contraste em temas dinâmicos (por exemplo, um texto branco ilegível sobre um botão amarelo no tema claro). O Skeleton resolve isso no nível da engine de tokens: cada escala cromática (`50` a `950` para `primary`, `secondary`, `tertiary`, `success`, `warning`, `error`, `surface`) possui um par de contraste correspondente (`--color-primary-contrast-500`), garantindo conformidade WCAG AAA automática sem esforço manual.
3. **Lógica de Componentes Headless com Zag.js**:
   Todos os componentes interativos complexos (como tabs, modais, drawers, comboboxes, file uploads e segmented controls) são governados por State Machines agnósticas de framework. Isso garante foco restrito, captura de teclado (WAI-ARIA 1.2), roving tabindex e suporte a internacionalização (RTL/LTR) idênticos tanto em Svelte quanto em React.
4. **Acabamento Sensorial e Micro-Ritmo**:
   Visualmente, o Skeleton prega uma estética contemporânea, técnica e refinada: bordas com tokens de raio precisos (`--radius-container`), superfícies translúcidas com `backdrop-blur` sutil, texturas discretas de ruído (`bg-noise`), elevações com sombras de cor volumétrica (`shadow-primary-500/50`) e foco absoluto na tipografia legível.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados

- **SaaS B2B & Plataformas Multi-Tenant (White-Label)**: A facilidade de trocar a identidade visual inteira simplesmente alterando o atributo `data-theme="..."` no elemento `<html>` torna o Skeleton imbatível para produtos que oferecem personalização de marca por cliente corporativo.
- **DevTools, Dashboards & Consoles de Infraestrutura**: Aplicações com alta densidade de dados, múltiplos gráficos, painéis colapsáveis e necessidade crítica de modo escuro/claro sem flickering.
- **Projetos Modernos em Svelte 5 / SvelteKit**: É a biblioteca de escolha número 1 do ecossistema Svelte, totalmente reescrita para aproveitar as reatividades baseadas em signals do Svelte 5 (`$state`, `$derived`, `$props`).
- **Aplicações Híbridas React / Next.js com Tailwind CSS v4**: Times que buscam a disciplina de um design system completo e acessível sem o peso de runtime das soluções clássicas de CSS-in-JS.

### Papel na Regra 60-30-10

- **60% — Espinha Dorsal (Layout & Fundação)**: O Skeleton é projetado primariamente como a infraestrutura 60% do seu produto. Ele dita os tokens de espaçamento (`--spacing`), tipografia responsiva (`--text-scaling`), paleta de cores globais, containers de cards (`card`), botões de base (`btn`), formulários (`input`, `select`, `label`) e a hierarquia de superfícies (`bg-surface-50-950`).
- **30% — Camada de Fluidez e Interatividade**: Componentes interativos orquestrados por Zag.js — Tabs sincronizadas com indicador animado deslizante, Gavetas laterais (Drawers/Dialogs) com backdrop escuro e fechamento acessível via tecla `Escape`, e Menus suspensos contextuais.
- **10% — Efeitos Protagonistas (Showstoppers)**: Mesh gradients cromáticos reativos ao tema (`radial-gradient` com `color-mix(in oklab, var(--color-primary-500) 30%, transparent)`), anéis de progresso circulares SVG animados (`ProgressRing`) e modais de busca tipo Command Palette com sombra difusa vibrante (`⌘K`).

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em

1. **Projetos com DaisyUI ou Flowbite**: O Skeleton possui incompatibilidade técnica explícita com o DaisyUI e as bibliotecas do ecossistema Flowbite. Ambas injetam utilitários conflitantes de mesmo nome (`.btn`, `.card`, `.badge`) no Tailwind, provocando colisão catastrófica de estilos e variáveis de cores.
2. **Landing Pages Puramente Artísticas / Experiências 3D Imersivas**: Projetos focados exclusivamente em shaders WebGL, Three.js ou animações tipo Awwwards sem estrutura de produto SaaS não se beneficiam da infraestrutura densa de design tokens e acessibilidade do Skeleton.
3. **Aplicações sem Tailwind CSS**: O Skeleton v3 foi concebido como uma extensão natural do Tailwind CSS (aproveitando diretivas `@theme` no v4 ou plugins no v3). Usá-lo em projetos com Vanilla CSS ou CSS Modules isolados anula sua principal proposta de valor.

### ⚠️ Erros Comuns de Exagero

- **Sobrecarga de Variantes de Cores na Mesma Interface**: Misturar na mesma tela botões `preset-filled-primary-500`, `preset-filled-secondary-500` e `preset-filled-tertiary-500`. A convenção do Skeleton determina que o `preset-filled` seja reservado para o botão de ação principal (CTA), enquanto as ações secundárias devem adotar `preset-tonal` ou `preset-outlined`.
- **Forçar Cores de Texto Hardcoded (`text-white` ou `text-black`)**: Sobrepor `text-white` manualmente em elementos com classes de preset quebra a acessibilidade automática quando o tema é trocado para um tema claro ou uma paleta de alta luminosidade. Deve-se sempre confiar nas variáveis de contraste do sistema (`text-surface-contrast-50-950`, `text-primary-contrast-500`).
- **Importar Todos os 24 Temas Nativos no Bundle Final**: Incluir todos os arquivos de tema (`@import '@skeletonlabs/skeleton/themes/...'`) no arquivo de estilo de produção inflando o bundle CSS sem necessidade. Em produção, importe apenas os temas selecionados pela aplicação.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

### 1. `Tabs` com Indicador Dinâmico Zag.js
- **Anatomia Visual**: Container com lista de gatilhos horizontais ou verticais (`Tabs.List`, `Tabs.Trigger`), painel de conteúdo associado (`Tabs.Content`) e um indicador flutuante (`Tabs.Indicator`) que desliza fisicamente com interpolação suave sob a aba ativa.
- **Gatilho de Interação**: Clique no gatilho ou navegação por setas do teclado (com seleção automática ou manual via foco WAI-ARIA).
- **Onde Encaixar**: Visão geral de dashboards, alternância de configurações de usuário, visualização de código multi-linguagem.

### 2. `Dialog & Drawer` com Transição Discreta
- **Anatomia Visual**: Camada de backdrop semitransparente com desfoque gaussiano (`backdrop-blur-sm`), centralizador geométrico (`positioner`) e o painel de conteúdo (`card`) com sombra volumétrica profunda (`shadow-xl`) e botão de fechar (`btn-icon`). Suporta abertura lateral (Drawer) ou central (Modal).
- **Gatilho de Interação**: Abertura por gatilho com foco automático no primeiro input, fechamento por tecla `Escape`, clique no backdrop ou trigger de encerramento.
- **Onde Encaixar**: Criação de novos registros, painéis de navegação mobile, confirmações de ações destrutivas.

### 3. `Combobox & Command Palette (⌘K)`
- **Anatomia Visual**: Campo de entrada integrado com ícone de lupa, lista suspensa de opções categorizadas por grupos, destaque de correspondência textual e badge de atalho de teclado (`⌘K`).
- **Gatilho de Interação**: Digitação em tempo real com filtragem otimizada, navegação via setas cima/baixo com auto-scroll para o item ativo e seleção via `Enter`.
- **Onde Encaixar**: Topbar da aplicação (pesquisa global), seletores de filtros relacionais em tabelas complexas.

### 4. `SegmentedControl`
- **Anatomia Visual**: Barra compacta estilizada com cantos arredondados contendo opções exclusivas (`SegmentedControl.Item`), com uma cápsula de preenchimento (`preset-filled` ou `preset-tonal`) que se move entre os botões.
- **Gatilho de Interação**: Clique ou arrasto de seleção.
- **Onde Encaixar**: Alternador de períodos em dashboards (Hoje, 7d, 30d, 1a), visualização em grade versus lista, alternador de moeda.

### 5. `ProgressCircular / ProgressRing`
- **Anatomia Visual**: Indicador radial vetorial em SVG com trilho de fundo opaco e arco ativo animado utilizando as cores do tema, com suporte a texto central de porcentagem ou ícone de status.
- **Gatilho de Interação**: Reativo ao estado numérico do sistema ou exibição indeterminada contínua (`stroke-dashoffset` animado).
- **Onde Encaixar**: Métricas de cota de armazenamento em cartões de faturamento, wizards de onboarding, upload de lotes.

### 6. `Switch / Toggle` de Alta Precisão
- **Anatomia Visual**: Trilho oval encapsulado (`Switch.Control`) com um pino circular (`Switch.Thumb`) que transita com aceleração física suave, acompanhado de rótulo acessível (`Switch.Label`).
- **Gatilho de Interação**: Clique, toque ou ativação por barra de espaço com foco visível de teclado.
- **Onde Encaixar**: Formulários de preferências, ativação de recursos experimentais (Feature Flags), alternador de notificações.

### 7. `FileUpload & Dropzone`
- **Anatomia Visual**: Área pontilhada ou contrastante de drag-and-drop (`FileUpload.Dropzone`), gatilho de seleção de arquivos manual (`FileUpload.Trigger`), lista de arquivos adicionados com ícones de mime-type, barra de progresso individual e botão de remoção.
- **Gatilho de Interação**: Arrastar e soltar arquivos (com destaque visual ao passar por cima) ou clique para abrir o seletor nativo do sistema operacional.
- **Onde Encaixar**: Upload de avatares, importação de planilhas CSV/JSON em SaaS, anexos em chamados de suporte.

### 8. `Accordion` Multidimensional
- **Anatomia Visual**: Pilha vertical de seções colapsáveis (`Accordion.Item`) com cabeçalho contendo título, descrição curta e ícone chevron giratório sincronizado, expandindo painéis com transição fluida de altura.
- **Gatilho de Interação**: Clique ou teclado com expansão única (modo sanfona estrita) ou expansão múltipla simultânea.
- **Onde Encaixar**: Páginas de Perguntas Frequentes (FAQ), menus laterais profundos de documentação técnica, painéis de filtros avançados.

### 9. `Preset Utility Primitives` (`.card`, `.btn`, `.badge`, `.table`)
- **Anatomia Visual**: Classes utilitárias fundamentais de Tailwind puras que não exigem JavaScript. O `.card` fornece bordas, background e padding inteligentes; o `.btn` define dimensões, centragem flexível e transição tátil; o `.badge` fornece pílulas de status compactas; o `.table` estrutura grades tabulares responsivas com zebra striping adaptativo.
- **Gatilho de Interação**: Estados nativos CSS de `:hover`, `:active` e `:focus-visible`.
- **Onde Encaixar**: Toda a superfície estrutural do projeto.

### 10. `AppBar & Navigation Rail`
- **Anatomia Visual**: Cabeçalho de aplicação com altura padronizada (`--header-height`), ancoragem fixa (`sticky top-0`), borda inferior e efeito `backdrop-blur-lg`, integrado a um trilho lateral de navegação com ícones de estado ativo (`aria-[current=page]:preset-tonal`).
- **Gatilho de Interação**: Navegação por rotas, abertura de menu hambúrguer responsivo via gaveta retrátil.
- **Onde Encaixar**: Layout principal da aplicação (App Shell).

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

O Skeleton v3 trabalha com pacotes modulares que dividem a fundação de estilos da lógica dos componentes de framework:

```bash
# 1. Instalação no ecossistema Svelte 5 / SvelteKit:
npm install @skeletonlabs/skeleton @skeletonlabs/skeleton-svelte @lucide/svelte

# 2. Instalação no ecossistema React / Next.js:
npm install @skeletonlabs/skeleton @skeletonlabs/skeleton-react lucide-react
```

### Configuração de Estilos Globais (Tailwind CSS)

No arquivo principal de estilos da sua aplicação (ex: `src/app.css` ou `src/globals.css`):

```css
/* Importação da base de design tokens do Skeleton */
@import '@skeletonlabs/skeleton';

/* Importação do módulo opcional de utilitários e presets semânticos */
@import '@skeletonlabs/skeleton/optional/presets';

/* Registro dos temas escolhidos para a aplicação */
@import '@skeletonlabs/skeleton/themes/cerberus';
@import '@skeletonlabs/skeleton/themes/catppuccin';
@import '@skeletonlabs/skeleton/themes/crimson';
```

Para aplicar o tema e o modo escuro, declare no elemento raiz (`<html data-theme="cerberus" data-mode="dark">`) ou manipule dinamicamente via JavaScript:

```javascript
document.documentElement.setAttribute('data-theme', 'cerberus');
document.documentElement.setAttribute('data-mode', 'dark'); // ou 'light' ou 'system'
```

---

### Física de Movimento e Transições

O Skeleton v3 adota uma combinação de animações nativas de CSS moderno com suporte a `starting-style` e as transições calculadas do Zag.js:

- **Transições de Modais e Overlays (`starting:data-[state=open]`)**:
  Utiliza a nova especificação CSS de `transition-discrete` para permitir transição contínua entre estados display `none` e elementos visíveis com animação suave de opacidade e translação:
  ```css
  /* Transição de entrada suave para drawers e dialogs */
  transition: opacity 200ms cubic-bezier(0.16, 1, 0.3, 1), transform 200ms cubic-bezier(0.16, 1, 0.3, 1);
  ```
- **Indicador de Abas Deslizante (`Tabs.Indicator`)**:
  Calculado via motor de animação do Zag.js que mede em tempo real a geometria da `DOMRect` da aba selecionada, aplicando interpolação com spring suave:
  - Curva de transição: `cubic-bezier(0.4, 0, 0.2, 1)` (Material Deceleration).
  - Parâmetros equivalentes de Spring: `stiffness: 350`, `damping: 32`, `mass: 1`.

---

### Receitas de Código Funcionais

#### Receita 1: Componente de Abas Fluidas com Indicador Deslizante (React)

```tsx
import React from 'react';
import { Tabs } from '@skeletonlabs/skeleton-react';
import { Activity, LayoutDashboard, ShieldCheck } from 'lucide-react';

export function ProjectOverviewTabs() {
  return (
    <div className="card preset-outlined-surface-200-800 bg-surface-50-950 p-6 space-y-6">
      <header className="flex justify-between items-center border-b border-surface-200-800 pb-4">
        <div>
          <h3 className="h3 font-bold text-surface-900-100">Painel Operacional</h3>
          <p className="text-sm text-surface-600-400">Controle de instâncias e telemetria do cluster.</p>
        </div>
        <span className="badge preset-filled-success-500 font-semibold">Online</span>
      </header>

      <Tabs defaultValue="metrics" className="w-full">
        {/* Lista com indicador animado integrado pelo Zag.js */}
        <Tabs.List className="border-b border-surface-200-800 flex gap-2 relative">
          <Tabs.Trigger
            value="metrics"
            className="btn hover:preset-tonal data-[state=selected]:text-primary-500 font-medium flex items-center gap-2 px-4 py-2"
          >
            <Activity className="size-4" />
            <span>Métricas em Tempo Real</span>
          </Tabs.Trigger>

          <Tabs.Trigger
            value="deployments"
            className="btn hover:preset-tonal data-[state=selected]:text-primary-500 font-medium flex items-center gap-2 px-4 py-2"
          >
            <LayoutDashboard className="size-4" />
            <span>Deploys Recentes</span>
          </Tabs.Trigger>

          <Tabs.Trigger
            value="security"
            className="btn hover:preset-tonal data-[state=selected]:text-primary-500 font-medium flex items-center gap-2 px-4 py-2"
          >
            <ShieldCheck className="size-4" />
            <span>Auditoria & Segurança</span>
          </Tabs.Trigger>

          {/* O Indicador desliza automaticamente com animação de largura e posição */}
          <Tabs.Indicator className="absolute bottom-0 h-0.5 bg-primary-500 transition-all duration-200" />
        </Tabs.List>

        <div className="pt-4">
          <Tabs.Content value="metrics" className="space-y-4">
            <div className="grid grid-cols-1 md:grid-cols-3 gap-4">
              <div className="card preset-tonal-surface p-4">
                <span className="text-xs uppercase font-semibold text-surface-600-400">Uso de CPU</span>
                <p className="text-2xl font-bold mt-1">28.4%</p>
              </div>
              <div className="card preset-tonal-surface p-4">
                <span className="text-xs uppercase font-semibold text-surface-600-400">Memória RAM</span>
                <p className="text-2xl font-bold mt-1">4.2 GB / 16 GB</p>
              </div>
              <div className="card preset-tonal-surface p-4">
                <span className="text-xs uppercase font-semibold text-surface-600-400">Latência p99</span>
                <p className="text-2xl font-bold mt-1">14 ms</p>
              </div>
            </div>
          </Tabs.Content>

          <Tabs.Content value="deployments">
            <p className="text-sm text-surface-700-300">
              Nenhuma implantação pendente na branch principal. Último commit verificado há 18 minutos.
            </p>
          </Tabs.Content>

          <Tabs.Content value="security">
            <p className="text-sm text-surface-700-300">
              Todas as 14 políticas de conformidade estão ativas e sem vulnerabilidades detectadas.
            </p>
          </Tabs.Content>
        </div>
      </Tabs>
    </div>
  );
}
```

---

#### Receita 2: Gaveta Lateral / Drawer Modal Acessível (Svelte 5 Runes)

```svelte
<script lang="ts">
  import { Dialog } from '@skeletonlabs/skeleton-svelte';
  import { Menu, X, ArrowRight, Settings, Users, Database } from 'lucide-svelte';

  let open = $state(false);
</script>

<Dialog bind:open>
  <!-- Gatilho de abertura no header da aplicação -->
  <Dialog.Trigger class="btn-icon preset-tonal">
    <Menu class="size-5" />
    <span class="sr-only">Abrir Menu de Navegação</span>
  </Dialog.Trigger>

  <!-- Camada de backdrop com desfoque e animação suave -->
  <Dialog.Backdrop
    class="fixed inset-0 z-50 bg-surface-50-950/60 backdrop-blur-sm transition-discrete duration-200 opacity-0 starting:data-[state=open]:opacity-0 data-[state=open]:opacity-100"
  />

  <!-- Posicionador alinhado à esquerda para efeito de Drawer -->
  <Dialog.Positioner class="fixed inset-0 z-50 flex justify-start pointer-events-none">
    <Dialog.Content
      class="pointer-events-auto card border-r border-surface-200-800 bg-surface-50-950/90 backdrop-blur-lg w-80 h-dvh p-6 space-y-6 shadow-2xl overflow-y-auto transition-discrete duration-200 opacity-0 -translate-x-full starting:data-[state=open]:opacity-0 starting:data-[state=open]:-translate-x-full data-[state=open]:opacity-100 data-[state=open]:translate-x-0"
    >
      <header class="flex justify-between items-center">
        <div>
          <Dialog.Title class="text-xl font-bold text-surface-900-100">Painel do Sistema</Dialog.Title>
          <Dialog.Description class="text-xs text-surface-600-400">Ambiente de Produção (US-East)</Dialog.Description>
        </div>
        <Dialog.CloseTrigger class="btn-icon hover:preset-tonal rounded-full">
          <X class="size-4" />
        </Dialog.CloseTrigger>
      </header>

      <hr class="hr" />

      <nav class="flex flex-col gap-2">
        <a href="#users" class="btn hover:preset-tonal justify-between px-3 py-2.5">
          <div class="flex items-center gap-3">
            <Users class="size-4 text-primary-500" />
            <span class="text-sm font-medium">Gestão de Usuários</span>
          </div>
          <ArrowRight class="size-4 opacity-40" />
        </a>

        <a href="#databases" class="btn hover:preset-tonal justify-between px-3 py-2.5">
          <div class="flex items-center gap-3">
            <Database class="size-4 text-secondary-500" />
            <span class="text-sm font-medium">Bancos de Dados</span>
          </div>
          <ArrowRight class="size-4 opacity-40" />
        </a>

        <a href="#settings" class="btn hover:preset-tonal justify-between px-3 py-2.5">
          <div class="flex items-center gap-3">
            <Settings class="size-4 text-tertiary-500" />
            <span class="text-sm font-medium">Configurações Globais</span>
          </div>
          <ArrowRight class="size-4 opacity-40" />
        </a>
      </nav>

      <footer class="pt-10">
        <button
          type="button"
          class="btn preset-filled-primary-500 w-full font-bold py-2.5 shadow-lg shadow-primary-500/20"
        >
          Criar Nova Instância
        </button>
      </footer>
    </Dialog.Content>
  </Dialog.Positioner>
</Dialog>
```

---

#### Receita 3: Definição de Tema Customizado com Variáveis CSS

Para criar uma identidade visual exclusiva usando o mecanismo de temas do Skeleton v3:

```css
/* src/styles/theme-neon-enterprise.css */
[data-theme='neon-enterprise'] {
  /* Escala de espaçamento base e tipografia */
  --spacing: 0.25rem;
  --text-scaling: 1.075;
  --radius-container: 0.75rem;

  /* Cores Semânticas - Primária (Cyan Elétrico com alto contraste) */
  --color-primary-50: #ecfeff;
  --color-primary-500: #06b6d4;
  --color-primary-600: #0891b2;
  --color-primary-950: #083344;
  --color-primary-contrast-500: #000000; /* Contraste automático calculado */

  /* Cores de Superfície Adaptativas (Modo Claro / Escuro sincronizado) */
  --color-surface-50: #f8fafc;
  --color-surface-100: #f1f5f9;
  --color-surface-200: #e2e8f0;
  --color-surface-800: #1e293b;
  --color-surface-900: #0f172a;
  --color-surface-950: #020617;
  --color-surface-contrast-50-950: #020617;

  /* Configuração Tipográfica Global */
  --typo-base--font-family: 'Geist Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --typo-heading--font-weight: 700;
  --typo-anchor--color-light: var(--color-primary-600);
  --typo-anchor--color-dark: var(--color-primary-500);
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao integrar o **Skeleton UI (v3)** na elaboração de um novo projeto no documento `DESIGN_BLUEPRINT.md`, a inteligência artificial deve observar estritamente as seguintes regras:

1. **Declaração Explícita de Tema e Modo no Setup**:
   - Exigir no blueprint a indicação do tema padrão (ex: `cerberus`, `catppuccin`, `crimson` ou nome de tema customizado).
   - Configurar o elemento raiz com `data-theme="{theme-name}"` e `data-mode="system"` (ou `dark`/`light`).
2. **Convenção de Presets Semânticos para Elementos de Interface**:
   - **Ação Primária (CTA)**: Deve utilizar obrigatoriamente `btn preset-filled-primary-500` acompanhado de sombra temática `shadow-lg shadow-primary-500/20`.
   - **Ações Secundárias / Neutras**: Devem utilizar `btn preset-tonal` ou `btn preset-outlined-surface-200-800 hover:preset-tonal`.
   - **Containers e Superfícies**: Devem utilizar a classe composta `card preset-outlined-surface-200-800 bg-surface-50-950`.
   - **Textos de Apoio e Títulos**: Proibir classes hardcoded de cinza (`text-gray-400`); usar sempre tokens adaptativos do Skeleton como `text-surface-600-400` ou `text-surface-800-200`.
3. **Guardrails de Integridade Arquitetural**:
   - **Bloqueio de Bibliotecas Incompatíveis**: Registrar no blueprint a proibição expressa de instalação conjunta com DaisyUI, Flowbite ou Tailwind Elements.
   - **Paridade Multi-Framework**: Quando o projeto for Svelte, usar exclusivamente `@skeletonlabs/skeleton-svelte` com a sintaxe de Runes (`$state`, snippets). Quando for React, importar os componentes correspondentes de `@skeletonlabs/skeleton-react`.
   - **Componentes Compostos**: Recomendar a utilização de componentes estruturados compostos (`Tabs.List`, `Tabs.Trigger`, `Tabs.Indicator`, `Tabs.Content`) em vez de recriar lógica de abas manualmente com estados booleanos avulsos.
