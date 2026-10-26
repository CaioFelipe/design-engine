---
id: "046-minidev-ui"
name: "MiniDev UI"
url: "https://ui.minidev.pro/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Dynamic Physical Lighting", "Material Switching (Hairline, Glass, Metal, Paper)", "Base UI Headless Architecture", "Tailwind CSS v4 & OKLCH", "Craft Precision Product Surfaces"]
densidade_informacao: "Alta"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Framer Motion/JS) a Baixo (CSS/Headless)"
stack_frameworks: ["React 19 / 18", "Next.js (App Router)", "Tailwind CSS v4", "Base UI (@base-ui/react)", "Motion (Framer Motion)", "TypeScript", "Lucide React", "TanStack Table v8", "dnd-kit"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Geist Mono", "Inter", "Plus Jakarta Sans", "JetBrains Mono"]
  paletas_ideais: ["OKLCH Semantic Palette (oklch(0.22 0.025 264))", "Monochromatic Deep Ink / Light Surface", "Dynamic Material Spectrum (Frosted Glass, Brushed Alloy, Tactile Cardstock)"]
  combinacoes_recomendadas: ["shadcn/ui (registries cruzados)", "Origin UI / coss ui", "Magic UI", "Aceternity UI", "Radix Themes"]
  conflitos_esteticos: ["Neo-brutalismo cru com contornos pretos pesados", "Flat design sem profundidade ou sombras", "Cyberpunk / Glow saturado descalibrado"]
---

# MiniDev UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **MiniDev UI**, criado pelo estúdio e engenheiro de produto **Aman Kaushik** (MiniDev / AK Tech), estabelece uma evolução estética e técnica contundente sobre o ecossistema moderno de interfaces React e Tailwind. Enquanto o padrão dominante da indústria converge para superfícies planas e cartões opacos indistinguíveis, o manifesto central do MiniDev UI sintetiza sua proposta em uma declaração incisiva:

> **"Every UI kit is flat. This one is lit."**

A biblioteca introduz mais de **548 componentes, blocos de página e templates** distribuídos sob licença MIT e construídos nativamente sobre o **Tailwind CSS v4**, primitivas acessíveis do **Base UI** (`@base-ui/react`) e compatibilidade total com o protocolo de registries do **shadcn/ui**. Contudo, seu verdadeiro diferencial reside na introdução de três conceitos de engenharia de design até então inéditos em kits de interface prontos para produção:

---

### 1.1. O Motor de Iluminação Física Unificada (The Global Light Field Engine)
Em interfaces convencionais, sombras CSS (`box-shadow`) são declaradas como constantes estáticas (ex: `0 10px 15px -3px rgba(0,0,0,0.1)`), simulando uma fonte de luz fictícia perpendicular ou ligeiramente superior que nunca muda, independentemente da navegação.

O MiniDev UI trata a tela como um **campo de luz tridimensional unificado**:
- O ponteiro do mouse (ou um loop de deriva orgânica no mobile e estados ociosos) atua como uma **luz direcional física real**.
- Duas variáveis personalizadas no `:root` CSS — `--sx` e `--sy` (variando entre `-1` e `1`) — ditam as coordenadas espaciais para **todos os componentes da página em tempo real**.
- Conforme o cursor cruza a tela, as sombras de cada botão, cartão, toggle e diálogo giram e se estendem organicamente no sentido oposto ao foco luminoso.
- **Viés Gravitacional (Downward Bias)**: Um fator vertical constante (`+1px`, `+4px`, `+10px`) é incorporado matematicamente nos offsets maiores via `calc(var(--sy) * 28px + 10px)`. Isso assegura que, mesmo quando o cursor desce ao rodapé da tela e `--sy` se torna negativo, os elementos continuem firmemente ancorados à página, sem a ilusão óptica de estarem pendurados ou invertidos contra a gravidade.
- **Matiz Cromática em OKLCH**: Em vez de borrões pretos genéricos (`rgba(0,0,0,0.2)`), as sombras do MiniDev UI são tingidas no espaço perceptual **OKLCH** com a mesma temperatura fria dos neutros do tema (`oklch(0.22 0.025 264 / a)` no modo claro e `oklch(0 0 0 / 0.55)` no escuro), enquanto a borda superior voltada para a luz recebe um micro-highlight especular chanfrado (`inset 0 1px 0 0 var(--highlight)`).

---

### 1.2. O Sistema Quadrimaterial Dinâmico (`data-material`)
O MiniDev UI transcende o paradigma binário convencional de apenas "Light vs. Dark Mode". Através do atributo raiz `data-material`, toda a suíte de 548 componentes transmuta simultaneamente sua substância física e comportamento visual entre **quatro materiais tácteis reais**, sem que seja necessário modificar uma única linha de código nos componentes:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                       SISTEMA DE MATERIAIS MINIDEV UI                       │
├───────────────┬─────────────────────────────────────────────────────────────┤
│ 1. Hairline   │ Minimalismo suíço ultra-preciso (Apple / Linear). Estrutura │
│               │ de 1px, anéis sutis, contraste neutro e máxima sobriedade.  │
├───────────────┼─────────────────────────────────────────────────────────────┤
│ 2. Glass      │ Frosted glass sofisticado (`backdrop-blur-xl`, saturação    │
│               │ 150%, orbs cromáticos borrados e bordas com refração).      │
├───────────────┼─────────────────────────────────────────────────────────────┤
│ 3. Metal      │ Liga de alumínio usinado. Gradientes cônicos escovados,     │
│               │ chanfros metálicos e reflexos de brilho direcional.          │
├───────────────┼─────────────────────────────────────────────────────────────┤
│ 4. Paper      │ Textura editorial analógica. Papel cartão térmico encorpado │
│               │ (`oklch(0.95 0.02 85)`), sombras orgânicas quentes e toque. │
└───────────────┴─────────────────────────────────────────────────────────────┘
```

---

### 1.3. O Inspetor Nativo "Blueprint Mode" (`⌥` Peek / Ruler Toggle)
Projetado por engenheiros de produto para engenheiros e designers, o MiniDev UI incorpora nativamente uma camada de auditoria e inspeção técnica in-browser:
- Ao manter pressionada a tecla **`Alt` (Windows) / `Option` (macOS)** em qualquer parte da aplicação ou clicar no ícone de régua na navegação, o sistema ativa o **Blueprint Mode**.
- Cada componente expõe instantaneamente suas caixas delimitadoras (*bounding boxes* com linhas pontilhadas de engenharia), cotas métricas de altura e largura em pixels, valores exatos de `padding` interno, `gap` de flexbox/grid e os tokens de design semânticos consumidos.

---

### 1.4. Arquitetura Base UI (`@base-ui/react`) & Rigor Semântico OKLCH
Diferente das implementações históricas baseadas no Radix UI clássico, o MiniDev UI adota o **Base UI** — a biblioteca de componentes headless de última geração desenvolvida pelo time por trás do Radix, Floating UI e Material UI. Isso resulta em:
1. **Markup Semântico Puro**: Menos nós aninhados de wrappers no DOM.
2. **Tokens Semânticos Invioláveis**: O sistema proíbe hexadecimais brutos ou classes de utilitário atômicas como `bg-blue-500` em componentes. Utiliza rigorosamente a taxonomia:
   - Superfícies: `bg`, `surface`, `raised`, `sunken`.
   - Bordas: `border`, `border-strong`.
   - Tipografia: `fg`, `fg-muted`, `fg-subtle`.
   - Ações & Realce: `ink` (preto/branco contrastante de alta autoridade), `on-ink`, `accent` (violeta de marca), `accent-soft`, `accent-fg`.
   - Feedback: `success`, `warning`, `danger`, `info`.
3. **Mapeamento Transparente para shadcn/ui**: Uma folha de compatibilidade traduz automaticamente variáveis shadcn clássicas (`--background`, `--card`, `--primary`, `--ring`) para a infraestrutura MiniDev, permitindo misturar componentes de ambos os registries sem dissonância estética.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados
1. **Plataformas de IA Generativa & Agentes Autônomos (AI Copilots & Chat Surfaces)**:
   O MiniDev UI possui uma suíte inteira de componentes desenhados especificamente para interfaces de inteligência artificial: containers de streaming com leitor `ReadableStream`, blocos colapsáveis de raciocínio profundo (*reasoning blocks*), renderizadores de chamadas de ferramentas (*tool calls*) e campos de entrada de prompt com redimensionamento dinâmico.
2. **SaaS B2B Modernos, DevTools & Infraestrutura Cloud**:
   Aplicações que exigem densidade de informação extrema combinada a refinamento tátil (como faturamento complexo via Stripe, gerenciadores de chaves de API, visualizadores de logs, sidebars retráteis com atalhos de teclado `Cmd+B` e tabelas de alta performance).
3. **Fintechs, Portais de Investimento & Dashboards Executivos de Performance**:
   Ambientes com métricas financeiras críticas onde o componente `Number Roll` (dígitos verticais rolantes com máscara de gradiente) e os gráficos em **SVG puro** (sem a sobrecarga de 150KB de bibliotecas pesadas de charts) oferecem velocidade e fidelidade visual impecável.
4. **Sistemas de Gestão de Fluxos, Kanban & Roadmaps (Productivity Suites)**:
   Aplicações corporativas que necessitam de quadros Kanban com arraste fluído (`dnd-kit`), diagramas de Gantt com linhas temporais interativas e painéis redimensionáveis (*split panes*).

---

### O Papel no Ritmo Visual (A Aplicação da Regra 60-30-10)

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    DISTRIBUIÇÃO DA REGRA 60-30-10 NO MINIDEV UI             │
├───────────────────┬─────────────────────────────────────────────────────────┤
│ 60% — Fundação    │ Superfícies Hairline, tokens semânticos OKLCH, cartões   │
│     Estrutural    │ `bg-surface` com borda fina `border-border`, tipografia │
│                   │ Geist tabular, formulários e app shell utilitário.       │
├───────────────────┼─────────────────────────────────────────────────────────┤
│ 30% — Fluidez &   │ Microinterações ultra-rápidas (`duration-[70ms]`),      │
│     Transição     │ Segmented Controls com thumb deslizante, botões táteis   │
│                   │ com afundamento `active:translate-y-[0.5px]`, menus.    │
├───────────────────┼─────────────────────────────────────────────────────────┤
│ 10% — Showstopper │ O Light Field interativo seguindo o mouse na Hero,      │
│     Protagonista  │ o Material Switcher transformando toda a UI, o Split-   │
│                   │ Flap Solari board 3D e a ativação do Blueprint Mode.    │
└───────────────────┴─────────────────────────────────────────────────────────┘
```

- **60% — A Espinha Dorsal (Hairline Minimal)**:
  Em 60% do tempo de uso, o sistema deve operar no material **Hairline**. Os tokens semânticos e as superfícies neutras garantem leitura impecável de tabelas, formulários e dashboards, com zero fadiga visual.
- **30% — Microdinâmica & Affordance Tátil**:
  Transições ultrarrápidas de `70ms` a `140ms` governadas pela curva proprietária `ease-hairline` criam a sensação de resposta instantânea de hardware sob os dedos do usuário.
- **10% — Momentos Showstopper**:
  O recurso de iluminação dinâmica com cursor deve ser reservado a seções estratégicas de conversão (Hero, seções de demonstração interativa ou cards de preços). Elementos tridimensionais como o Solari Board (Split-Flap Display) funcionam como o clímax visual de landing pages ou murais de boas-vindas.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Sistemas Legados sem Pipeline de Build Moderno**:
  Aplicações construídas sobre arquiteturas antigas (ex: templates legados em PHP/Ruby sem suporte a Vite, Next.js ou Tailwind CSS v4) não conseguem processar as diretivas CSS `@theme inline` nem as funções de cores OKLCH.
- **Navegadores Obsoletos ou Ambientes Corporativos Congelados**:
  Sistemas que necessitam de suporte obrigatório a versões antigas do Safari (< 15.4) ou Chrome legado onde a sintaxe de `oklch()`, `color-mix()` e `backdrop-filter` complexo causam falha de renderização ou quedas catastróficas de contraste.
- **Estéticas Intencionalmente Neo-Brutalistas ou Y2K Caóticas**:
  Projetos cuja identidade exija bordas pretas de `3px`, cantos vivos com sombras duras de 90° sem difusão (estilo Gumroad clássico) entram em colisão estética total com a sutileza matemática das sombras e chanfros de 1px do MiniDev UI.
- **Interfaces com Restrições Críticas de Bateria / Hardware Fraco**:
  Dispositivos embarcados de quiosque ou microtelas de IoT com CPUs extremamente lentas onde o recálculo contínuo de sombras atrelado ao mouse no `:root` gere engasgos de GPU (a menos que o script de pointer seja explicitamente desativado).

---

### ⚠️ Erros Comuns de Exagero & Anti-Padrões:
1. **O Pesadelo da Sobreposição de Vidros (Glass Stacking)**:
   Ativar o material `Glass` em toda a árvore DOM e colocar cartões de vidro dentro de gavetas de vidro com modais de vidro cria múltiplos filtros `backdrop-filter: blur(...)` acumulados. Em telas Retina 4K, isso degrada a taxa de quadros de 120 FPS para menos de 30 FPS. Use Glass exclusivamente como acabamento de primeiro plano (overlays, navbars flutuantes ou cards hero destacados).
2. **Mistura Desordenada de Materiais na Mesma Vista**:
   Renderizar um card com acabamento `Paper` ao lado de um botão metálico com gradiente cônico (`Metal`) e uma tabela translúcida (`Glass`) gera cacofonia tátil e destrói a coerência mental do usuário. Mantenha o material unificado em toda a página ou alterne apenas em contextos semânticos específicos (ex: botões e cartões de hardware em Metal, todo o restante em Hairline).
3. **Corrompimento da Hierarquia do Botão `ink`**:
   No MiniDev UI, a ação primária padrão é renderizada pela cor **`ink`** (preto intenso no modo claro, branco absoluto no modo escuro com sombra volumétrica `shadow-ink`). A cor **`accent`** (violeta) é reservada para gatilhos de conversão estritos ou badges. Transformar todos os botões do sistema em violeta `accent` destrói a elegância e sofisticação suíça do sistema.
4. **Iluminação Desenfreada sem Respeito a `prefers-reduced-motion`**:
   Nunca ative a animação de rotação contínua da luz sem verificar a flag de preferência do sistema operacional (`prefers-reduced-motion`). Usuários com sensibilidade vestibular podem sentir náusea com sombras oscilantes em telas grandes.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão catalogados **12 componentes emblemáticos** do MiniDev UI, cobrindo primitivas estruturais, componentes de IA e blocos de produto de alto impacto:

---

### 1. Interactive Light Field & Directional Shadows Engine
- **Anatomia Visual**: Camada de iluminação física que intercepta as coordenadas do mouse no documento e projeta sombras compostas por até 5 camadas de `box-shadow` em OKLCH com offset dinâmico (`--o1x`, `--o4x`, `--o12x`, `--o28x`) e reflexo superior especular (`--highlight`).
- **Gatilho de Interação**: Movimento contínuo do ponteiro (`pointermove` suavizado via `requestAnimationFrame`) ou ciclo senoidal autônomo suave (*ambient drift loop*) em dispositivos móveis e períodos ociosos.
- **Onde Encaixar**: Hero Section, containers de vitrine de produto e páginas de demonstração interativa de tecnologia.

---

### 2. Material Switcher Pill Control (`data-slot="material-switcher"`)
- **Anatomia Visual**: Controle segmentado encapsulado em um pill de fundo afundado (`bg-sunken`), contendo 4 opções de rádio: **Hairline**, **Glass**, **Metal** e **Paper**. Cada opção exibe uma esfera miniaturizada com a microtextura e gradiente cônico correspondente ao material.
- **Gatilho de Interação**: Clique ou navegação por teclado (roving tabindex via setas direcionais). Altera imediatamente o atributo `data-material` no elemento `<html>`.
- **Onde Encaixar**: Navbar superior, cabeçalho de documentação, barra de ferramentas de controle de marca e painéis de acessibilidade.

---

### 3. Blueprint Mode Inspector (Alt/Option Peek Ruler)
- **Anatomia Visual**: Botão em formato de régua métrica (`lucide-ruler`) que, quando acionado ou quando a tecla `Alt`/`Option` é mantida pressionada, sobrepõe reticulados técnicos azuis, linhas pontilhadas de margem e etiquetas monocromáticas em `font-mono` exibindo dimensões em pixels e nomes de tokens em cada nó.
- **Gatilho de Interação**: Atalho de teclado global (`keydown` de `Alt`/`Option`), peek ao segurar ou toggle fixo por clique.
- **Onde Encaixar**: Barra de ferramentas de desenvolvimento, menus de rodapé para designers e portais de documentação interativa.

---

### 4. Number Roll Metric Counter (`data-slot="number-roll"`)
- **Anatomia Visual**: Contador numérico tabular de altíssima precisão onde cada caractere é encapsulado em uma coluna vertical de dígitos (0 a 9) com máscara de gradiente de opacidade superior e inferior (`[mask-image:linear-gradient(transparent,black_0.16em,black_calc(100%_-_0.16em),transparent)]`). Ao alterar o valor, os dígitos deslizam suavemente no eixo Y.
- **Gatilho de Interação**: Atualização de estado reativo em React, carregamento inicial de métricas ou toggle de período (ex: faturamento mensal para anual).
- **Onde Encaixar**: Cartões de KPI em Dashboards Executivos, seletores de planos em Páginas de Preços e contadores de receita em tempo real.

---

### 5. AI Chat Surface with Streaming, Reasoning & Tool Calls
- **Anatomia Visual**: Interface conversacional moderna composta por bolhas de mensagem em material Hairline, container colapsável expansível para cadeias de pensamento (*thought chain / reasoning block* com ícone de cérebro e chevron giratório), cartões visuais para execuções de ferramentas (*tool calls*) com status de execução (pending, running, success) e barra de prompt com botão de parada/retry e auto-expansão.
- **Gatilho de Interação**: Streaming de tokens em tempo real via `ReadableStream`, cliques para expandir/colapsar blocos de raciocínio lógico e atalho `Enter` / `Shift+Enter` na barra de envio.
- **Onde Encaixar**: Assistentes virtuais de SaaS, agentes autônomos, copilotos de código e plataformas de busca conversacional.

---

### 6. Interactive Segmented Control with Sliding Thumb
- **Anatomia Visual**: Grupo de rádio com acabamento tátil embutido em calha rebaixada (`bg-sunken`), com um indicador ativo flutuante (`segmented-control-thumb`) com sombra elevada e highlight chanfrado que desliza com física de mola suave sob a opção selecionada, acompanhado de badges de economia opcionais (ex: `-20%`).
- **Gatilho de Interação**: Clique em abas ou navegação via teclado com setas (Base UI Radio Group).
- **Onde Encaixar**: Toggles de ciclo de faturamento (Mensal/Anual), seletores de visualização de tabelas (Grade/Lista) e filtros de períodos em dashboards.

---

### 7. SaaS Workspace Billing & Plan Card with Usage Meter
- **Anatomia Visual**: Cartão volumétrico avançado com destaque visual no plano Pro/Team em fundo `bg-ink` e texto `text-on-ink`, preço integrado com `NumberRoll`, medidor visual de consumo de assentos/créditos (barra de progresso com track rebaixado e preenchimento contrastante) e lista de faturas com status em badges (Paid, Pending, Void).
- **Gatilho de Interação**: Hover com leve elevação de sombra, clique em botão de upgrade e expansão de detalhes de pagamento.
- **Onde Encaixar**: Páginas de Configuração de Conta (`/settings/billing`), fluxos de checkout e telas de precificação institucional.

---

### 8. TanStack Table v8 Hairline Data Table with Column Visibility
- **Anatomia Visual**: Grid tabular de densidade ajustável com linhas separadas por hairlines de 1px (`border-border`), ordenação com ícones bidirecionais, paginação tabular integrada, seleção múltipla de linhas via checkboxes com ação em massa e menu popover suspenso para alternar visibilidade de colunas individuais.
- **Gatilho de Interação**: Cliques de cabeçalho para ordenação, digitação com debounce para busca global e clique em ações contextuais.
- **Onde Encaixar**: Painéis administrativos, consoles de gerenciamento de usuários, inventários de banco de dados e listas de transações financeiras.

---

### 9. Split-Flap Solari Departure Board (3D Flip Animation)
- **Anatomia Visual**: Recriação digital sofisticada dos painéis mecânicos analógicos das estações ferroviárias europeias (Solari di Udine). Cada caractere é dividido horizontalmente em duas abas que realizam uma rotação no eixo tridimensional (`rotateX`) com perspectiva profunda (`perspective: 600px`), sombra de dobra central e som estético opcional.
- **Gatilho de Interação**: Mudança programática de texto com animação sequencial em cascata (*staggered character cycling*).
- **Onde Encaixar**: Painéis de status de sistemas/servidores, painéis de boas-vindas executivos e banners de anúncio de produtos de alto impacto.

---

### 10. Interactive Drag-and-Drop Kanban Board (`dnd-kit`)
- **Anatomia Visual**: Colunas verticais com contadores numéricos de tarefas, cartões leves com indicadores de prioridade (badges coloridos em tons suaves), tags de responsável e suporte nativo a reordenação fluida com placeholder fantasma e feedback sonoro/tátil de encaixe.
- **Gatilho de Interação**: Arraste por mouse (`drag-and-drop`), toque prolongado ou navegação completa por teclado (acessibilidade via `dnd-kit`).
- **Onde Encaixar**: Módulos de gerenciamento de tarefas (estilo Linear/Jira), pipelines de vendas CRM e acompanhamento de chamados de suporte.

---

### 11. Gantt Timeline Chart with Dependencies & Today Line
- **Anatomia Visual**: Visão temporal contínua com escalas intercambiáveis de dias e semanas, barras de tarefas arredondadas com preenchimento em cores semânticas, setas vetoriais SVG desenhando dependências lógicas entre itens e uma linha vertical vermelha/azul marcando a data atual (*Today Marker*).
- **Gatilho de Interação**: Scroll horizontal nativo sem travamento, hover sobre tarefas revelando popover detalhado com prazos e arraste para redimensionamento de duração.
- **Onde Encaixar**: Cronogramas de lançamento de produto, ferramentas de gestão de engenharia e roadmaps públicos.

---

### 12. Hairline Toggle Switch (`data-slot="switch"`) with Inset Ring
- **Anatomia Visual**: Interruptor de estado ultracompacto (`h-5 w-9`) com calha afundada em `bg-sunken` protegida por anel de precisão de 1px (`shadow-[inset_0_0_0_1px_var(--border-strong)]`) e um botão circular deslizante elevado (`bg-raised` com `shadow-key`) que transiciona para `bg-accent` com fluidez quando ativado.
- **Gatilho de Interação**: Clique ou tecla de Espaço, com suporte nativo a acessibilidade e transição em `140ms` via `ease-hairline`.
- **Onde Encaixar**: Painéis de preferências, formulários de configurações de notificações e telas de permissões de segurança.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Pacotes
O MiniDev UI pode ser consumido como um pacote NPM completo (`minidev-ui-kit`) ou individualmente através do utilitário de registros do shadcn:

```bash
# Opção A: Instalação via pacote completo NPM
npm i minidev-ui-kit @base-ui/react lucide-react clsx tailwind-merge

# Opção B: Adição individual via shadcn CLI (código puro no seu repositório)
npx shadcn@latest add @minidev/button
npx shadcn@latest add @minidev/data-table
npx shadcn@latest add @minidev/billing-page
```

Caso utilize o **Next.js**, inclua no seu `next.config.ts`:
```typescript
const nextConfig = {
  transpilePackages: ["minidev-ui-kit"],
};
export default nextConfig;
```

---

### Configuração de Estilos e Tokens no Tailwind CSS v4 (`globals.css`)
No Tailwind v4, toda a configuração é puramente declarativa no CSS utilizando as regras `@import` e `@theme inline`:

```css
@import "tailwindcss";

:root {
  /* Coordenadas padrão da fonte de luz global */
  --sx: 0.45;
  --sy: 0.90;

  /* Offsets dinâmicos com viés gravitacional downward */
  --o1x: calc(var(--sx) * 1px);
  --o1y: calc(var(--sy) * 1px);
  --o4x: calc(var(--sx) * 4px);
  --o4y: calc(var(--sy) * 4px + 1px);
  --o12x: calc(var(--sx) * 12px);
  --o12y: calc(var(--sy) * 12px + 4px);
  --o28x: calc(var(--sx) * 28px);
  --o28y: calc(var(--sy) * 28px + 10px);

  /* Highlight especular de borda superior */
  --highlight: oklch(1 0 0 / 0.80);

  /* Superfícies & Fundo (Light Mode) */
  --bg: oklch(0.985 0.002 264);
  --surface: oklch(1 0 0);
  --raised: oklch(1 0 0);
  --sunken: oklch(0.95 0.004 264);

  /* Bordas de precisão */
  --border: oklch(0.91 0.005 264);
  --border-strong: oklch(0.82 0.01 264);

  /* Texto */
  --fg: oklch(0.15 0.01 264);
  --fg-muted: oklch(0.45 0.01 264);
  --fg-subtle: oklch(0.65 0.01 264);

  /* Ações Primárias (Ink) & Marca (Accent) */
  --ink: oklch(0.12 0.01 264);
  --on-ink: oklch(0.98 0 0);
  --accent: oklch(0.60 0.22 280);
  --accent-soft: oklch(0.60 0.22 280 / 0.12);
  --accent-fg: oklch(0.55 0.22 280);

  /* Pilhas de sombras multicamadas em OKLCH */
  --sh-raised: 
    inset 0 1px 0 0 var(--highlight),
    var(--o1x) var(--o1y) 1px 0 oklch(0.22 0.025 264 / 0.06),
    var(--o4x) var(--o4y) 4px 0 oklch(0.22 0.025 264 / 0.06),
    var(--o12x) var(--o12y) 12px -2px oklch(0.22 0.025 264 / 0.08);

  --sh-overlay: 
    inset 0 1px 0 0 var(--highlight),
    0 0 0 1px oklch(0.22 0.025 264 / 0.05),
    var(--o4x) var(--o4y) 12px -4px oklch(0.22 0.025 264 / 0.10),
    var(--o28x) var(--o28y) 56px -12px oklch(0.22 0.025 264 / 0.24);
}

.dark {
  --highlight: oklch(1 0 0 / 0.06);

  /* Superfícies Dark */
  --bg: oklch(0.12 0.005 270);
  --surface: oklch(0.16 0.007 270);
  --raised: oklch(0.19 0.008 270);
  --sunken: oklch(0.09 0.005 270);

  --border: oklch(0.24 0.006 270);
  --border-strong: oklch(0.32 0.008 270);

  --fg: oklch(0.96 0.003 270);
  --fg-muted: oklch(0.68 0.005 270);
  --fg-subtle: oklch(0.45 0.005 270);

  --ink: oklch(0.98 0 0);
  --on-ink: oklch(0.12 0.01 264);

  /* Sombras Dark volumétricas */
  --sh-raised: 
    inset 0 1px 0 0 var(--highlight),
    0 0 0 1px var(--border),
    var(--o4x) var(--o4y) 12px -2px oklch(0 0 0 / 0.50);

  --sh-overlay: 
    inset 0 1px 0 0 var(--highlight),
    0 0 0 1px var(--border-strong),
    var(--o28x) var(--o28y) 56px -12px oklch(0 0 0 / 0.75);
}

@theme inline {
  --color-bg: var(--bg);
  --color-surface: var(--surface);
  --color-raised: var(--raised);
  --color-sunken: var(--sunken);
  --color-border: var(--border);
  --color-border-strong: var(--border-strong);
  --color-fg: var(--fg);
  --color-fg-muted: var(--fg-muted);
  --color-fg-subtle: var(--fg-subtle);
  --color-ink: var(--ink);
  --color-on-ink: var(--on-ink);
  --color-accent: var(--accent);
  --color-accent-soft: var(--accent-soft);
  --color-accent-fg: var(--accent-fg);

  --shadow-raised: var(--sh-raised);
  --shadow-overlay: var(--sh-overlay);

  /* Curva proprietária Hairline */
  --ease-hairline: cubic-bezier(0.16, 1, 0.3, 1);
}
```

---

### Física de Movimento e Constantes de Transição
- **Curva Hairline Easing**: `cubic-bezier(0.16, 1, 0.3, 1)` (desaceleração imediata inspirada nos frameworks de design suíço e Apple).
- **Escala Temporal**:
  - `70ms`: Microinterações de hover em botões, links, abas e itens de menu.
  - `140ms`: Ativação de botões, deslocamento do polegar de interruptores (*switch thumb*) e estados pressionados (`active:translate-y-[0.5px]`).
  - `200ms`: Abertura e fechamento de modais, gavetas e menus popover com desvanecimento suave.
  - `500ms`: Transição sequencial de dígitos no `NumberRoll`.
- **Física de Molas (Spring Parameters)**:
  - Abas e Segmented Thumb: `stiffness: 450`, `damping: 32`, `mass: 0.8` (resposta ultra-rápida sem oscilação residual).
  - Gavetas e Sheets: `stiffness: 180`, `damping: 24` (amortecimento suave de entrada lateral).

---

### Receita de Código Funcional e Realista

#### 1. Controlador da Fonte de Luz Global (`LightSourceProvider.tsx`)
Este componente escuta o movimento do cursor, calcula a normalização dimensional, interpola os valores com amortecimento e grava as variáveis `--sx` e `--sy` no nó raiz:

```tsx
"use client";

import React, { useEffect } from "react";

export function LightSourceProvider({ children }: { children: React.ReactNode }) {
  useEffect(() => {
    // Respeitar usuários com preferência de movimento reduzido
    if (window.matchMedia("(prefers-reduced-motion: reduce)").matches) {
      return;
    }

    let targetX = 0.45;
    let targetY = 0.9;
    let currentX = 0.45;
    let currentY = 0.9;
    let rafId: number;

    const handlePointerMove = (e: PointerEvent) => {
      const { innerWidth, innerHeight } = window;
      // Normalizar coordenadas entre -1 e 1
      targetX = ((e.clientX / innerWidth) - 0.5) * 2;
      targetY = ((e.clientY / innerHeight) - 0.5) * 2;
    };

    const updateLoop = () => {
      // Interpolação Linear (Lerp) para fluidez tátil orgânica
      currentX += (targetX - currentX) * 0.08;
      currentY += (targetY - currentY) * 0.08;

      const root = document.documentElement;
      root.style.setProperty("--sx", currentX.toFixed(3));
      root.style.setProperty("--sy", currentY.toFixed(3));

      rafId = requestAnimationFrame(updateLoop);
    };

    window.addEventListener("pointermove", handlePointerMove, { passive: true });
    rafId = requestAnimationFrame(updateLoop);

    return () => {
      window.removeEventListener("pointermove", handlePointerMove);
      cancelAnimationFrame(rafId);
    };
  }, []);

  return <>{children}</>;
}
```

---

#### 2. Componente de Cartão Físico com Suporte a Materiais (`PhysicalCard.tsx`)
Demonstração de cartão responsivo que suporta dinamicamente os materiais `Hairline`, `Glass`, `Metal` e `Paper`:

```tsx
import React from "react";
import { clsx } from "clsx";

interface PhysicalCardProps extends React.HTMLAttributes<HTMLDivElement> {
  material?: "hairline" | "glass" | "metal" | "paper";
  highlightGlow?: boolean;
}

export function PhysicalCard({
  material = "hairline",
  highlightGlow = false,
  className,
  children,
  ...props
}: PhysicalCardProps) {
  return (
    <div
      className={clsx(
        "relative overflow-hidden rounded-2xl border transition-all duration-200 ease-hairline",
        // Variantes de Materiais
        material === "hairline" &&
          "border-border bg-surface shadow-raised text-fg",
        material === "glass" &&
          "border-white/20 bg-surface/70 backdrop-blur-xl backdrop-saturate-150 shadow-overlay text-fg",
        material === "metal" &&
          "border-border-strong bg-[conic-gradient(from_210deg,oklch(0.96_0_0),oklch(0.70_0.005_250),oklch(0.98_0_0),oklch(0.62_0.005_250),oklch(0.96_0_0))] shadow-raised text-fg dark:bg-[conic-gradient(from_210deg,oklch(0.20_0_0),oklch(0.12_0.005_250),oklch(0.24_0_0),oklch(0.10_0.005_250),oklch(0.20_0_0))]",
        material === "paper" &&
          "border-[oklch(0.85_0.02_85)] bg-[oklch(0.97_0.015_85)] shadow-raised text-[oklch(0.15_0.01_85)] dark:bg-[oklch(0.14_0.01_85)] dark:border-[oklch(0.22_0.01_85)] dark:text-[oklch(0.95_0.01_85)]",
        className
      )}
      {...props}
    >
      {/* Specular Highlight de borda superior */}
      <div
        aria-hidden="true"
        className="pointer-events-none absolute inset-x-0 top-0 h-px bg-gradient-to-r from-transparent via-[var(--highlight)] to-transparent opacity-80"
      />

      {/* Brilho Especular Opcional voltado para a luz */}
      {highlightGlow && (
        <div
          aria-hidden="true"
          style={{
            transform:
              "translate3d(calc(var(--sx) * -12px), calc(var(--sy) * -12px), 0)",
          }}
          className="pointer-events-none absolute -inset-full bg-radial from-accent/15 via-transparent to-transparent opacity-50 blur-2xl"
        />
      )}

      <div className="relative p-6">{children}</div>
    </div>
  );
}
```

---

#### 3. Dígito Rolante Tabular (`NumberRoll.tsx`)
Implementação pura do mecanismo de rotação vertical de números para contadores de receita e dashboards:

```tsx
"use client";

import React from "react";

interface NumberRollProps {
  value: number;
  prefix?: string;
  suffix?: string;
}

export function NumberRoll({ value, prefix = "$", suffix = "" }: NumberRollProps) {
  const formattedStr = value.toLocaleString("en-US");
  const chars = formattedStr.split("");

  return (
    <span
      data-slot="number-roll"
      className="relative inline-flex items-baseline font-mono text-3xl font-medium tracking-tight text-fg tabular-nums"
    >
      <span className="sr-only">{`${prefix}${value}${suffix}`}</span>
      <span aria-hidden="true" className="inline-flex items-baseline overflow-hidden">
        {prefix && <span>{prefix}</span>}
        {chars.map((char, index) => {
          if (!/[0-9]/.test(char)) {
            return <span key={index}>{char}</span>;
          }

          const digit = parseInt(char, 10);
          return (
            <span
              key={index}
              className="relative -my-[0.14em] inline-block h-[1.28em] w-[0.62em] overflow-hidden py-[0.14em] [mask-image:linear-gradient(transparent,black_0.16em,black_calc(100%_-_0.16em),transparent)]"
            >
              <span
                className="absolute inset-x-0 top-[0.14em] flex flex-col transition-transform duration-500 ease-hairline"
                style={{ transform: `translateY(-${digit * 10}%)` }}
              >
                {[0, 1, 2, 3, 4, 5, 6, 7, 8, 9].map((n) => (
                  <span key={n} className="block text-center leading-[1.28em]">
                    {n}
                  </span>
                ))}
              </span>
            </span>
          );
        })}
        {suffix && <span>{suffix}</span>}
      </span>
    </span>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar o **MiniDev UI** como biblioteca ou referência de design system para um projeto no `DESIGN_BLUEPRINT.md`, a inteligência artificial e a equipe de desenvolvimento devem cumprir rigorosamente as seguintes instruções:

### 1. Declaração Formal no Blueprint
```markdown
## Design System & Component Registry
- **Base UI Registry**: MiniDev UI (`https://ui.minidev.pro/` / `@minidev`)
- **Estética Predominante**: Modern Swiss Craft Minimal + Global Dynamic Light Field
- **Material Padrão**: `Hairline` (60%), com elementos pontuais em `Glass` (10%)
- **Espaço de Cor & Tokens**: OKLCH Semântico via Tailwind CSS v4 (`@theme inline`)
- **Física de Movimento**: `ease-hairline` (cubic-bezier(0.16, 1, 0.3, 1)) com durações em 70ms / 140ms
```

### 2. Regras Estritas de Composição e Tokens
1. **Inviolabilidade dos Tokens**: Jamais escreva classes de cor literais como `text-gray-500` ou `bg-[#18181b]`. Utilize exclusivamente `text-fg-muted`, `bg-surface`, `bg-sunken` e `border-border`.
2. **Autoridade do Botão Primário**: O botão primário de ação padrão deve SEMPRE usar `bg-ink text-on-ink shadow-ink`. O variante `accent` é estritamente restrito a fluxos de checkout ou call-to-actions estratégicos.
3. **Controle de Desempenho do Light Field**: Ao instanciar o `LightSourceProvider`, declare explicitamente a trava de `prefers-reduced-motion` e utilize interpolação via `requestAnimationFrame` para evitar degradação de FPS.
4. **Copywriting Limpo**: Respeite integralmente as diretrizes de copywriting sem meta-linguagem (ex: botões com textos claros como *"Start 14-day trial"*, *"Generate API key"*, *"Export CSV"*, sem adjetivos vazios ou clichês gerados por IA).
