---
id: "navbar-gallery"
name: "Navbar Gallery"
url: "https://www.navbar.gallery/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico:
  - "Curadoria Atômica de Arquitetura de Navegação (Header-First Design)"
  - "Floating Dynamic Islands & Detached Pill Bars"
  - "Obsidian Glassmorphism & Frosted Blur Surfaces (Backdrop Filter)"
  - "SaaS B2B Mega Menus de Alta Densidade Informacional"
  - "Microinterações de Cursor & Sliding Tab Indicators (Molas Físicas)"
  - "Multi-Tier Header Layouts (Announcement + Global Nav + Contextual Bar)"
  - "Cinematic Fullscreen Drawers & Responsive Kinetic Menus"
densidade_informacao: "Media/Narrativa a Alta/Utilitaria"
impacto_visual: "Editorial/Sofisticado & Minimalista/Silencioso"
custo_computacional: "Moderado (Compositing de `backdrop-filter: blur()`, listener de scroll throttled/passive, GPU transform transitions em mega menus, layout animations do Framer Motion)"
stack_frameworks:
  - "Webflow (Plataforma nativa do portal de curadoria)"
  - "Finsweet Attributes (CMS Load & CMS Filter v1)"
  - "Next.js (App Router) & React 19"
  - "Tailwind CSS v3 / v4 (Arbitrary values, backdrop-filters, custom utilities)"
  - "Framer Motion / Motion.dev (Spring physics, sliding pill `layoutId`, exit transitions)"
  - "Radix UI / Shadcn UI (Primitives acessíveis de NavigationMenu, Dialog, DropdownMenu)"
  - "Lucide React / Phosphor Icons (Ícones micro-otimizados em 16-20px)"
compatibilidade:
  fontes_ideais:
    - "Neo-Grotesque Tech & Modern SaaS: Geist, Inter Display, SF Pro Display, Plus Jakarta Sans, General Sans, Satoshi"
    - "Monoespaçada de Status & Metadados: Geist Mono, JetBrains Mono, Fragment Mono, IBM Plex Mono"
    - "Serif Editorial Sofisticado (Luxury & Fashion): GT Sectra, PP Editorial New, Cormorant Garamond, Newsreader"
  paletas_ideais:
    - "Obsidian Frosted Glass (Dark Core): #08080A (Void), #121216 (Island Base 75% alpha), #22222B (Hairline 1px border), #F4F4F6 (Text 100%), #9090A0 (Text Muted 60%)"
    - "Warm Alabaster Glass (Light Editorial): #FFFFFF (Surface Pure), #F5F5F7 (Alabaster Base 80% alpha), #E2E2E8 (Hairline Subtile), #111114 (Text Primary), #686873 (Text Secondary)"
    - "High-Contrast Electric Accent (10% Energy): #4F46E5 (Indigo Radiant), #06B6D4 (Cyan Cyber), #10B981 (Emerald Live Status), #F43F5E (Alert/Promo Crimson)"
    - "Titanium Industrial: #18181B, #27272A, #3F3F46, #71717A, #A1A1AA, #FAFAFA"
  combinacoes_recomendadas:
    - "Tailwind CSS com `backdrop-blur-md` ou `backdrop-blur-xl` + `border border-white/[0.08]` + `bg-[#0a0a0c]/80` para compor ilhas flutuantes"
    - "Framer Motion com molas ágeis (`stiffness: 400, damping: 30`) para o indicador de link ativo/hover deslizante (`layoutId`)"
    - "Radix UI `NavigationMenu` para mega menus com transições de viewport dinâmicas e safe hover triangle preservado"
    - "Custom Hook `useScrollDirection` com throttling passivo para esconder a barra ao rolar para baixo e revelá-la ao rolar para cima"
  conflitos_esteticos:
    - "Z-Index War: Navbars com `z-index: 10` que são engolidas por carrosséis Swiper, embeds do Spline ou modais"
    - "Shadow Hell: Sombras projetadas pretas difusas (`box-shadow: 0 20px 40px rgba(0,0,0,0.4)`) que sujam o conteúdo de fundo em vez de criar vidro limpo"
    - "Hover Trap sem Diagonal Safe Area: Menus suspensos ou mega menus que fecham abruptamente quando o usuário move o cursor diagonalmente em direção ao submenu"
    - "Layout Shift na Rolagem: Mudanças abruptas de altura (`h-20` para `h-14`) sem transição suave de padding/height, causando jitter perceptível na página"
    - "Viewport Hogging em Mobile: Headers fixos que ocupam mais de 15% da altura de tela de smartphones modernos, sacrificando a área de leitura útil"
    - "Falta de Suporte a `:focus-visible`: Menus inacessíveis que não respondem à navegação por teclado (Tab, ArrowKeys, Escape)"
---

# Navbar Gallery — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
███╗   ██╗ █████╗ ██╗   ██╗██████╗  █████╗ ██████╗ 
████╗  ██║██╔══██╗██║   ██║██╔══██╗██╔══██╗██╔══██╗
██╔██╗ ██║███████║██║   ██║██████╔╝███████║██████╔╝
██║╚██╗██║██╔══██║╚██╗ ██╔╝██╔══██╗██╔══██║██╔══██╗
██║ ╚████║██║  ██║ ╚████╔╝ ██████╔╝██║  ██║██║  ██║
╚═╝  ╚═══╝╚═╝  ╚═╝  ╚═══╝  ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝
   G   A   L   L   E   R   Y   —   N A V I G A T I O N   E N G I N E
```

---

## 1. DNA Estético & Filosofia de Curadoria

Fundado no final de 2023 pela designer de produtos e engenheira de interfaces ucraniana **Christina Liubynska** (fundadora da *Supercharged Design* e proeminente criadora *build-in-public* no ecossistema global do design digital), o **Navbar Gallery** (`https://www.navbar.gallery/`) nasceu para preencher uma das maiores lacunas de referência anatômica na web contemporânea.

Inspirada diretamente pelo surgimento de micro-curadorias especializadas mono-componente (como o célebre *footer.design*), Liubynska identificou que, embora o cabeçalho seja o elemento mais crítico de toda a arquitetura de informação e a primeira interação tátil de qualquer visitante, não existia na internet nenhum repositório focado exclusivamente na engenharia, na ergonomia e na direção de arte de **barras de navegação, mega menus, ilhas flutuantes e menus mobile**.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        THE NAVBAR GALLERY CURATORIAL SYSTEM                            │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  [ Real Production Websites ]  ──►  [ Deconstructed Navigation ]  ──►  [ Taxonomy Matrix ]│
│   • Live URLs (No Dribbble Fakes)    • Floating Dynamic Islands         • 10 Nav Types     │
│   • Framer & Webflow Production      • Enterprise Mega Menus            • 70+ Styles/Tags  │
│   • Next.js / Custom Code Saas       • Kinetic Fullscreen Overlays      • Real-World Links │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ TAXONOMY AXES: Types (Structural) × Styles (Aesthetic Moods) × Stacks (Framer/Webflow)│
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 A Filosofia do "Atomic Navigation Engineering"

O diferencial absoluto do Navbar Gallery em relação a galerias generalistas (como Land-book, Awwwards ou Lapa Ninja) reside na sua **lente cirúrgica e atômica**:
1. **Foco no Wayfinding e na Hierarquia Tátil**: A galeria não avalia um website apenas pela beleza de seu hero banner ou pelo 3D interativo, mas sim pela inteligência com que organiza de 3 a 300 destinos de navegação sem poluir a cognição do usuário.
2. **Curadoria de Produtos Reais em Produção**: Todas as mais de 550 barras catalogadas foram extraídas de sites em produção real (empresas SaaS, agências boutique, ferramentas para desenvolvedores como *Cloudflare*, *Browserbase*, *Consensys*, *Asana*, e estúdios como *Big Dirty Agency* e *Hosier Brown*). Mockups conceituais estéreis do Dribbble são sumariamente rejeitados.
3. **Desconstrução de Microinterações de Estado**: O Navbar Gallery documenta como a barra se comporta em repouso (*at-top*), como ela reage à aceleração do scroll (*scrolling down vs. scrolling up*), como manipula o desfoque de fundo (*backdrop glassmorphism*) e como projeta overlays suspensos (*flyout dropdowns, search palettes e mega menus*).

### 1.2 A Taxonomia Tridimensional do Navbar Gallery

O Navbar Gallery organiza seu acervo por meio de uma matriz cruzada de três dimensões:

```
                              ┌───────────────────────────────┐
                              │     NAVBAR GALLERY MATRIX     │
                              └───────────────┬───────────────┘
                                              │
         ┌────────────────────────────────────┼────────────────────────────────────┐
         │                                    │                                    │
         ▼                                    ▼                                    ▼
  [ 1. NAVIGATION TYPES ]             [ 2. AESTHETIC STYLES ]              [ 3. ENGINE STACKS ]
  • Static & Sticky Edge              • Bento Box & Dark Mode             • Framer Navbars
  • Dropdowns & Flyouts               • Obsidian Blur / Glass             • Webflow Showcases
  • Mega Menus (Multi-column)         • Brutalist & Monochromatic         • Next.js / React Apps
  • Sidebars (Collapsible)            • Minimal & Typography-led          • Custom CSS / GSAP
  • Breadcrumbs & Sub-navs            • SaaS B2B & DevTools
  • Search Bars & Command Palettes    • AI / Future-Tech
  • Announcement Bars (Top-Pill)      • Editorial / Luxury
  • Fullscreen Kinetic Menus          • D2C / High-end E-Commerce
  • Tabs & Segmented Controls         • Animated / GSAP Motion
```

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

O Navbar Gallery é a **Referência Primária de Arquitetura e Engenharia de Navegação** nos seguintes cenários de produto e web design:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        DECISION MATRIX: QUANDO CONSULTAR                               │
├─────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CENÁRIO DE PROJETO                      │ TIPO DE NAVEGAÇÃO RECOMENDADA NO REPOSITÓRIO │
├─────────────────────────────────────────┼──────────────────────────────────────────────┤
│ SaaS B2B com Múltiplos Produtos / Docs  │ Mega Menu com Colunas Temáticas & Badges     │
│ Modern AI / Developer Tooling           │ Detached Floating Island com Glassmorphism   │
│ E-Commerce / D2C Premium (50+ SKUs)     │ Hierarchical Dropdown com Cards de Imagem    │
│ Studio Criativo / Editorial de Moda     │ Fullscreen Overlay com Tipografia Cinética   │
│ Web App / Dashboard Administrativo      │ Collapsible Icon-Expanded Vertical Sidebar   │
│ Launch Page / Produto de Oferta Única   │ Minimal Centered Pill com CTA Direto         │
│ Portal de Notícias / Documentação API   │ Three-Tier Header (Top Announcement + Nav +   │
│                                         │ Breadcrumb / Search In-Page)                 │
└─────────────────────────────────────────┴──────────────────────────────────────────────┘
```

### 2.1 O Papel da Barra na Regra 60-30-10

Na engenharia visual de ponta orientada pelo Navbar Gallery, a barra de navegação desempenha um papel de calibração rigoroso na regra de proporção cromática e estrutural:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        60-30-10 NAVIGATION BALANCE SYSTEM                              │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  60% — THE VOID CANVAS (Backdrop & Content Space)                                      │
│  • O fundo principal da página rola por baixo da navbar.                               │
│  • A navbar utiliza superfícies translúcidas com `backdrop-filter: blur(16px)` para     │
│    permitir que as cores da seção hero sangrem sutilmente através do vidro.            │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  30% — THE STRUCTURAL CHASSIS (Navbar Container & Nav Links)                           │
│  • A carcaça da barra (moldura 1px hairline, pills arredondados, fundo fosco).         │
│  • Tipografia secundária dos links normais com contraste suave (ex: #9090A0 no escuro, │
│    #686873 no claro), garantindo legibilidade sem competir com o hero headline.       │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  10% — THE ACCENT SPARKS (Primary CTA, New Feature Pill & Active Indicator)            │
│  • O botão de conversão primário ("Start Free Trial", "Book a Demo", "Get Started").   │
│  • Badges atômicos luminosos (ex: "v2.0 LIVE", "AI Search", pulso verde de status).    │
│  • O indicator animado (sliding pill ou underline magnético) sob o link selecionado.   │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 2.2 Que Emoção e Posicionamento a Navegação Comunica

Uma barra de navegação projetada segundo os padrões do Navbar Gallery comunica ao visitante:
- **Segurança de Wayfinding**: O usuário nunca se sente perdido; sabe exatamente onde está na taxonomia da aplicação e quanto conteúdo ainda tem para explorar.
- **Rigor Técnico e Modernidade**: O uso de superfícies vítreas aeroespaciais (*Frosted Obsidian Glass*), molas táteis (*Spring Physics*) e transições sem engasgos transmite imediatamente que a empresa é dona de um produto de software de alto nível.
- **Respeito pelo Espaço de Visualização**: A barra não sequestra a tela; ela sabe recolher-se na rolagem para baixo e expandir-se gentilmente no menor movimento ascendente do usuário (*Smart Sticky Header*).

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

Nem todo projeto exige ou tolera uma barra flutuante complexa ou um mega menu multifacetado. A adoção irrefletida dos padrões da galeria pode gerar desastres ergonômicos:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        ANTI-PATTERNS & CONTRAINDICAÇÕES CRÍTICAS                       │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ ⚠️ Checkout Flows & Funis Críticos de Conversão (Navless Architecture)                  │
│    Em telas de pagamento, onboarding de checkout ou formulários sensíveis de signup,   │
│    a presença de uma navbar completa com links externos aumenta o churn e a taxa de    │
│    abandono de carrinho em até 28%. A regra de ouro é: "No Checkout, Drop the Nav".     │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ ⚠️ Interfaces Touch Kiosk / Terminais Físicos sem Suporte a Cursor                     │
│    Mega menus que dependem de eventos de mouseover/hover falham categoricamente em      │
│    telas touch públicas ou quiosques industriais, onde cada toque deve abrir um estado  │
│    explícito e o hover inexiste.                                                       │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ ⚠️ Telas de Ferramentas Densas de Edição (Canvas / IDE / Figma-like Apps)              │
│    Em web apps como editores de vetor, dashboards CAD ou consoles de código, uma barra │
│    flutuante que invade 60px do topo consome o precioso espaço vertical de trabalho.   │
│    Nesses ambientes, substitua por uma topbar estática milimétrica de 36px ou sidebar. │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 3.1 As 6 Grandes Armadilhas de Imitação

1. **The Z-Index War of Attrition**:
   - *O Erro*: Colocar `z-[999999]` na navbar e depois descobrir que bibliotecas de modais, banners de cookies ou players de vídeo WebGL brigam pela camada superior.
   - *A Cura*: Estabelecer uma escala de tokens de elevação rigorosa no Tailwind (`z-nav: 50`, `z-dropdown: 60`, `z-modal-backdrop: 70`, `z-modal: 80`, `z-toast: 90`).

2. **The Hover Trap (Safe Area Gap)**:
   - *O Erro*: Criar uma distância de 12px entre o botão do link da navbar e o container do dropdown sem uma área de captura invisível (safe triangle / invisible pseudo-element `::after`). O usuário move o mouse diagonalmente em direção a um item secundário e o menu se fecha na sua cara.
   - *A Cura*: Aplicar Radix UI Navigation Menu ou injetar uma bridge invisível com `padding-top: 12px` ou pseudo-elemento com `pointer-events-auto`.

3. **Heavy Drop Shadow Mud**:
   - *O Erro*: Usar `box-shadow: 0 20px 50px rgba(0, 0, 0, 0.4)` em uma barra escura sobre fundos escuros, criando uma mancha suja e opaca.
   - *A Cura*: Substituir por iluminação de contorno especular: `border: 1px solid rgba(255, 255, 255, 0.08)`, `box-shadow: 0 1px 2px rgba(0,0,0,0.4), inset 0 1px 0 rgba(255,255,255,0.1)`.

4. **Scroll Layout Shift & Jitter**:
   - *O Erro*: Alterar dinamicamente a propriedade `height` do header no evento de scroll sem animar ou mudar a posição estática da página de `relative` para `fixed` sem compensar com um spacer, fazendo o conteúdo abaixo dar um tranco vertical repentino.
   - *A Cura*: Manter a navbar sempre em `fixed` com um placeholder no fluxo normal ou transformar apenas propriedades aceleradas por GPU (`transform: translateY(...)`, `opacity`, `scale`).

5. **Keyboard Inaccessibility Ghosting**:
   - *O Erro*: Utilizar `<div>` clicáveis com `onClick` para acionar menus sem atributos `aria-expanded`, `aria-haspopup`, `role="navigation"` ou suporte a navegação por Tab e setas do teclado.
   - *A Cura*: Construir exclusivamente sobre elementos `<nav>`, `<ul>`, `<li>`, `<button>` e primitives do Radix UI.

6. **Mobile Viewport Cannibalization**:
   - *O Erro*: Manter uma barra com 80px de altura estática no topo de telas de iPhone SE / 13 Mini, roubando espaço de leitura.
   - *A Cura*: Em viewports `< 768px`, compactar a barra para 52px ou transformá-la em um floating button pill ou dock inferior estilo app nativo.

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

O Navbar Gallery revela padrões milimétricos que separam headers amadores de componentes de nível mundial.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        ANATOMY OF A MODERN FLOATING PILL NAVBAR                        │
├────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                        │
│     ┌────────────────────────────────────────────────────────────────────────────┐     │
│     │ [●] Top Announcement Bar (Optional micro-pill: "v3.0 is out! Read docs →") │     │
│     └─────────────────────────────────────┬──────────────────────────────────────┘     │
│                                           │  Gap: 8px-12px                             │
│     ┌─────────────────────────────────────▼──────────────────────────────────────┐     │
│     │  ┌──────┐    ┌───────────────────────────────────┐    ┌─────────────────┐  │     │
│     │  │ LOGO │    │ Products  Solutions  Docs  Pricing│    │ Sign in [CTA →] │  │     │
│     │  └──────┘    └───────────────────────────────────┘    └─────────────────┘  │     │
│     └────────────────────────────────────────────────────────────────────────────┘     │
│        ▲                                                                      ▲        │
│        │ Hairline Border: 1px solid rgba(255,255,255,0.08)                    │        │
│        │ Backdrop Surface: rgba(10,10,12,0.80) with blur(16px)                │        │
│        └──────────────────────────────────────────────────────────────────────┘        │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo

1. **Floating Pill / Dynamic Island Dimensioning**:
   - **Largura Máxima**: `max-w-5xl` (1024px) a `max-w-6xl` (1152px) em desktops, deixando margens generosas nas laterais da viewport.
   - **Posicionamento**: `fixed top-4 inset-x-0 mx-auto z-50` ou `top-6`.
   - **Altura e Padding**: Altura nominal de `56px` a `64px`; padding interno de `px-4 py-2` a `px-6 py-2.5`.
   - **Arredondamento**: `rounded-full` para navbars ultra-compactas ou `rounded-2xl` (16px) para navbars que acomodam submenus de grande porte.

2. **Full-Bleed Edge-to-Edge Navigation**:
   - **Posicionamento**: `fixed top-0 left-0 w-full z-50`.
   - **Borda Inferior**: `border-b border-white/[0.08]` (Dark Mode) ou `border-b border-black/[0.06]` (Light Mode).
   - **Container Central**: `max-w-7xl mx-auto px-6 lg:px-8` para alinhar rigidamente o logo e o CTA com as colunas do grid principal do site.

3. **Micro-Espaçamentos e Ritmo Interno**:
   - **Logo Dimension**: Altura fixa de `20px` a `28px`, preservando o aspect-ratio original.
   - **Gap entre Links**: `gap-6` (24px) a `gap-8` (32px) para garantir zonas de toque de cursor confortáveis sem sobreposição.
   - **Botões de Ação (CTAs)**: Altura de `36px` a `40px`, texto em `text-xs font-semibold uppercase tracking-wider` ou `text-sm font-medium`.

### 4.2 Sistemas de Cores, Superfícies & Texturas

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        SPECULAR LIGHTING & MATERIAL COMPOSITION                        │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  Layer 1 (Backdrop Base) : backdrop-filter: blur(16px) saturate(180%);                 │
│  Layer 2 (Canvas Tint)   : background: rgba(10, 10, 14, 0.75);                         │
│  Layer 3 (Hairline Glow) : border: 1px solid rgba(255, 255, 255, 0.08);               │
│  Layer 4 (Inset Specular): box-shadow: inset 0 1px 0 0 rgba(255, 255, 255, 0.12);      │
│  Layer 5 (Contact Drop)  : box-shadow: 0 8px 32px -4px rgba(0, 0, 0, 0.35);           │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

- **Obsidian Dark Surface**:
  - `bg-[#0a0a0c]/80 backdrop-blur-xl border border-white/[0.08]`
  - Destaque especular superior simulado com `shadow-[inset_0_1px_0_0_rgba(255,255,255,0.12)]`.
- **Light Alabaster Frosted Glass**:
  - `bg-white/80 backdrop-blur-xl border border-black/[0.06] shadow-[0_4px_20px_-2px_rgba(0,0,0,0.05)]`.
- **Hover Micro-Pill**:
  - Fundo dinâmico com `bg-white/[0.06]` ou `bg-black/[0.04]` animado suavemente atrás do link ativo usando `layoutId="nav-pill"`.

---

### 4.3 Catálogo de 9 Arquétipos Extraídos do Repositório

O Navbar Gallery cataloga nove grandes arquétipos funcionais e estéticos:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                         CATÁLOGO DOS 9 ARQUÉTIPOS NOTÁVEIS                             │
├────┬─────────────────────────────┬────────────────────────────┬────────────────────────┤
│ #  │ ARQUÉTIPO                   │ EXEMPLOS DE REFERÊNCIA     │ CASO DE USO PREFERENCIAL│
├────┼─────────────────────────────┼────────────────────────────┼────────────────────────┤
│ 01 │ Floating Dynamic Island     │ Clonix, Aveon, Orchid      │ Startups de IA, SaaS   │
│ 02 │ Enterprise SaaS Mega Menu   │ Cloudflare, Consensys      │ B2B Multi-Produto      │
│ 03 │ Multi-Tier Announcement Nav │ Asana, Stripe              │ Atualizações & Promos  │
│ 04 │ Collapsible Side Drawer     │ Bud, Browserbase           │ Dashboards, Web Apps   │
│ 05 │ Kinetic Fullscreen Overlay  │ Big Dirty Agency, Hosier   │ Agências & Luxo        │
│ 06 │ Command Palette Embedded    │ Linear, Raycast, Supaste   │ DevTools, Docs Técnicos│
│ 07 │ Asymmetrical Split Nav      │ Editorial Mags, Studio Lab │ Portfólios de Design   │
│ 08 │ Contextual Breadcrumb Subnav│ Velt, Next.js Docs         │ Guias & E-Commerce     │
│ 09 │ Segmented Tab Controller    │ Mobile Web, Framer Kits    │ Web Apps Mobile-First  │
└────┴─────────────────────────────┴────────────────────────────┴────────────────────────┘
```

#### Arquétipo 01: The Floating Dynamic Island / Detached Pill
- **Anatomia**: Barra de navegação desconectada das bordas da viewport, centralizada horizontalmente (`mx-auto`), com raios arredondados generosos (`rounded-full` ou `rounded-2xl`).
- **Comportamento**: Ao descer a página, a barra compacta seu padding interno; em alguns casos extremos, contrai os links de texto transformando-se em um mini-dock com ícones ou botão "Menu".
- **Onde Aplicar**: Landing pages de startups de IA, produtos de tecnologia disruptiva, apps de produtividade.

#### Arquétipo 02: The Enterprise SaaS Multi-Column Mega Menu
- **Anatomia**: Ao pousar o cursor em itens como "Products" ou "Solutions", um painel de alta fidelidade desce suavemente com 2 a 4 colunas divididas por linhas `1px solid`.
- **Diferencial**: Cada link não é um mero texto, mas uma célula rica com: ícone colorido em caixa de vidro, título em negrito, descrição de 1 linha e tag opcional (*"NEW"*, *"BETA"*, *"POPULAR"*). Inclui card lateral direito com banner de case study ou webinar recente.
- **Onde Aplicar**: Empresas B2B de infraestrutura, segurança na nuvem, fintechs e plataformas com múltiplos módulos.

#### Arquétipo 03: The Multi-Tier Edge-to-Edge with Announcement Banner
- **Anatomia**: Estrutura em duas ou três camadas horizontais sobrepostas. No topo absoluto, uma barra de anúncio fina de 32px com novidades ou cupom promocional; logo abaixo, a navbar principal com logo, navegação global e botões de conta.
- **Comportamento**: Na rolagem descendente, a barra de anúncio recolhe-se suavemente para fora da tela com `transform: translateY(-100%)`, mantendo apenas a navbar principal fixa no topo.
- **Onde Aplicar**: SaaS em fase de lançamento de features, grandes plataformas de e-commerce e conferências de tecnologia.

#### Arquétipo 04: The Collapsible Vertical Sidebar
- **Anatomia**: Barra vertical fixada no lado esquerdo da tela (`left-0 top-0 h-screen`), com largura de 240px a 280px no estado expandido, e 64px a 72px no estado recolhido (mostrando apenas ícones alinhados centralmente com tooltips laterais).
- **Diferencial**: Integra seletor de workspace/organização no topo, lista hierárquica de canais/rotas no centro e perfil de usuário + toggle de tema escuro/claro na base.
- **Onde Aplicar**: Web apps complexos, consoles de nuvem, ferramentas de CRM e painéis analíticos.

#### Arquétipo 05: The Kinetic Fullscreen Overlay Menu
- **Anatomia**: Header minimalista em repouso composto apenas pelo logo de um lado e um botão magnético "Menu [ + ]" do outro. Ao clicar, uma cortina opaca ou de vidro profundo cobre 100% da viewport com animação em staggered reveal.
- **Diferencial**: Links de navegação gigantescos (`text-5xl` a `text-7xl`) em tipografia editorial ou neo-grotesca com tracking negativo severo, acompanhados de preview dinâmico de imagem ou vídeo quando o cursor pousa sobre cada item.
- **Onde Aplicar**: Estúdios de design, marcas de alta moda, casas de arquitetura, portfólios de diretores de arte.

#### Arquétipo 06: The Command Palette Integrated Header
- **Anatomia**: O elemento central da navbar não é uma lista de links, mas uma barra de pesquisa contextual e interativa exibindo o atalho universal de teclado: `⌘K` ou `Ctrl + K`.
- **Diferencial**: Ao clicar ou teclar o atalho, a interface abre instantaneamente um modal Spotlight para busca instantânea de documentação, comandos rápidos e navegação direta por páginas.
- **Onde Aplicar**: Ferramentas para desenvolvedores, repositórios de documentação técnica, ferramentas de design engineering.

#### Arquétipo 07: The Asymmetrical Split Nav (Editorial / Brand-Centric)
- **Anatomia**: O logo da marca fica posicionado exatamente no centro matemático da barra, com metade dos links à esquerda e metade à direita, finalizando com o CTA na extremidade direita.
- **Diferencial**: Cria simetria visual imponente, muito comum em publicações literárias, revistas de design e produtos físicos de luxo.
- **Onde Aplicar**: Mídias digitais, revistas de arquitetura, perfumaria e joalheria digital.

#### Arquétipo 08: The Contextual Breadcrumb & In-Page Sub-Navbar
- **Anatomia**: Segunda barra colada imediatamente abaixo do header principal. Conforme o usuário navega por níveis profundos de documentação ou categorias de e-commerce, exibe breadcrumbs clicáveis com micro-seletores (`Home > Dashboard > Analytics > Reports`).
- **Diferencial**: Permite saltar entre níveis hierárquicos sem abrir menus complexos.
- **Onde Aplicar**: Documentação de APIs, grandes portais de e-commerce e portais de suporte técnico.

#### Arquétipo 09: The Mobile Segmented Tab Controller (Bottom Dock)
- **Anatomia**: Em dispositivos móveis (`< 768px`), o menu superior é despojado de links secundários e uma barra de navegação estilo dock nativo de iOS é fixada na base da tela (`bottom-4 inset-x-4`).
- **Diferencial**: Facilidade ergonômica de alcance com o polegar (*Thumb Zone Rule*), evitando que o usuário precise esticar o dedo até o topo de telas grandes de 6.7 polegadas.
- **Onde Aplicar**: Aplicações web progressivas (PWAs), plataformas de redes sociais e lojas mobile-first.

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Tokens CSS & Design System Variables

```css
:root {
  /* Dimensões & Espaçamentos do Header */
  --nav-height-desktop: 4rem;        /* 64px */
  --nav-height-compact: 3.25rem;     /* 52px */
  --nav-pill-radius: 9999px;         /* Pleno */
  --nav-island-radius: 1rem;         /* 16px */
  --nav-max-width: 68rem;            /* 1088px */
  --nav-z-index: 50;

  /* Superfícies & Cores em Obsidian Dark */
  --nav-bg-dark: rgba(10, 10, 14, 0.78);
  --nav-border-dark: rgba(255, 255, 255, 0.08);
  --nav-specular-dark: rgba(255, 255, 255, 0.12);
  --nav-text-primary-dark: #F4F4F6;
  --nav-text-muted-dark: #8E8EA0;
  --nav-hover-pill-dark: rgba(255, 255, 255, 0.06);

  /* Superfícies & Cores em Alabaster Light */
  --nav-bg-light: rgba(255, 255, 255, 0.82);
  --nav-border-light: rgba(0, 0, 0, 0.06);
  --nav-specular-light: rgba(255, 255, 255, 0.9);
  --nav-text-primary-light: #0F0F12;
  --nav-text-muted-light: #686873;
  --nav-hover-pill-light: rgba(0, 0, 0, 0.04);

  /* Curvas e Físicas de Movimento */
  --nav-ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);
  --nav-ease-in-out-smooth: cubic-bezier(0.65, 0, 0.35, 1);
}
```

### 5.2 Física de Movimento & Spring Parameters

Para alcançar a sensação tátil de produtos como Apple, Linear e Vercel presentes no repositório, utilize os seguintes parâmetros de mola no **Framer Motion**:

```typescript
// Mola ágil para o indicador de link ativo/hover deslizante (layoutId)
export const navPillSpring = {
  type: "spring",
  stiffness: 450,
  damping: 32,
  mass: 0.8,
};

// Mola com amortecimento suave para expansão do Mega Menu / Dropdowns
export const megaMenuSpring = {
  type: "spring",
  stiffness: 320,
  damping: 28,
  mass: 1,
};

// Transição de scroll hide/show da barra inteira
export const navBarScrollTransition = {
  duration: 0.35,
  ease: [0.16, 1, 0.3, 1], // expo out
};
```

---

### 5.3 Receita de Código Funcional Completa (React 19 + TypeScript + Tailwind + Framer Motion)

Abaixo está o componente completo e production-ready de uma **Floating Dynamic Island Navbar** com:
- Detecção passiva de direção de scroll (*Smart Hide/Show*).
- Transição de estado compacto ao afastar-se do topo da página.
- Indicador deslizante tátil no hover com `layoutId` do Framer Motion.
- Dropdown animado acessível com safe-area.
- Announcement pill integrado.
- Totalmente responsivo com gaveta mobile.

```tsx
"use client";

import React, { useState, useEffect, useRef } from "react";
import { motion, AnimatePresence } from "framer-motion";
import {
  ChevronDown,
  Menu,
  X,
  Sparkles,
  ArrowRight,
  ShieldCheck,
  Zap,
  Layers,
  Cpu
} from "lucide-react";

// Tipos estruturais da navegação
interface MegaMenuItem {
  title: string;
  description: string;
  icon: React.ComponentType<{ className?: string }>;
  href: string;
  badge?: string;
}

interface NavCategory {
  label: string;
  href?: string;
  items?: MegaMenuItem[];
}

const NAVIGATION_ITEMS: NavCategory[] = [
  {
    label: "Features",
    items: [
      {
        title: "Autonomous Agents",
        description: "Deploy self-healing workflow orchestrators.",
        icon: Zap,
        href: "/features/agents",
        badge: "v2.4",
      },
      {
        title: "Neural Engine",
        description: "Sub-10ms inference at the global edge.",
        icon: Cpu,
        href: "/features/engine",
      },
      {
        title: "Design System Bridge",
        description: "Translate Figma components to React tokens.",
        icon: Layers,
        href: "/features/design-system",
      },
      {
        title: "Enterprise Vault",
        description: "Zero-knowledge encryption for AI workloads.",
        icon: ShieldCheck,
        href: "/features/vault",
        badge: "SOC2",
      },
    ],
  },
  { label: "Solutions", href: "/solutions" },
  { label: "Docs", href: "/docs" },
  { label: "Pricing", href: "/pricing" },
];

export function FloatingDynamicNavbar() {
  const [isScrolled, setIsScrolled] = useState(false);
  const [isVisible, setIsVisible] = useState(true);
  const [activeDropdown, setActiveDropdown] = useState<string | null>(null);
  const [hoveredLink, setHoveredLink] = useState<string | null>(null);
  const [isMobileMenuOpen, setIsMobileMenuOpen] = useState(false);

  const lastScrollY = useRef(0);
  const dropdownTimeoutRef = useRef<NodeJS.Timeout | null>(null);

  // Hook passivo de scroll para detectar direção e compactação
  useEffect(() => {
    const handleScroll = () => {
      const currentScrollY = window.scrollY;

      // Estado de elevação ao sair do topo absoluto
      setIsScrolled(currentScrollY > 20);

      // Ocultar ao rolar para baixo rapidamente (>80px), revelar ao rolar para cima
      if (currentScrollY > 120) {
        if (currentScrollY > lastScrollY.current && currentScrollY - lastScrollY.current > 5) {
          setIsVisible(false); // Rolando para baixo
          setActiveDropdown(null);
        } else if (lastScrollY.current - currentScrollY > 8) {
          setIsVisible(true); // Rolando para cima
        }
      } else {
        setIsVisible(true);
      }

      lastScrollY.current = currentScrollY;
    };

    window.addEventListener("scroll", handleScroll, { passive: true });
    return () => window.removeEventListener("scroll", handleScroll);
  }, []);

  // Handlers de hover com tolerância de saída para evitar fechar por engano
  const handleMouseEnter = (label: string) => {
    if (dropdownTimeoutRef.current) clearTimeout(dropdownTimeoutRef.current);
    setActiveDropdown(label);
  };

  const handleMouseLeave = () => {
    dropdownTimeoutRef.current = setTimeout(() => {
      setActiveDropdown(null);
    }, 150);
  };

  return (
    <header className="fixed top-0 inset-x-0 z-50 pointer-events-none flex flex-col items-center px-4 pt-3 sm:pt-4">
      {/* 1. Announcement Banner Superior (Opcional, recolhe no scroll) */}
      <AnimatePresence>
        {!isScrolled && (
          <motion.div
            initial={{ opacity: 0, y: -10 }}
            animate={{ opacity: 1, y: 0 }}
            exit={{ opacity: 0, y: -10, transition: { duration: 0.15 } }}
            className="pointer-events-auto mb-2.5 hidden sm:flex items-center gap-2 rounded-full border border-indigo-500/20 bg-indigo-950/40 px-3.5 py-1 text-xs text-indigo-300 backdrop-blur-md shadow-sm"
          >
            <Sparkles className="h-3.5 w-3.5 text-indigo-400" />
            <span className="font-medium">Navbar Gallery v2.0 is live!</span>
            <span className="text-white/40">•</span>
            <a href="/changelog" className="inline-flex items-center gap-1 font-semibold hover:text-white transition-colors">
              Explore 500+ patterns <ArrowRight className="h-3 w-3" />
            </a>
          </motion.div>
        )}
      </AnimatePresence>

      {/* 2. Floating Island Container Principal */}
      <motion.nav
        aria-label="Global Navigation"
        initial={{ y: -20, opacity: 0 }}
        animate={{
          y: isVisible ? 0 : -100,
          opacity: isVisible ? 1 : 0,
        }}
        transition={{ duration: 0.35, ease: [0.16, 1, 0.3, 1] }}
        className={`pointer-events-auto relative w-full max-w-5xl transition-all duration-300 ${
          isScrolled
            ? "rounded-2xl border border-white/[0.08] bg-[#0A0A0E]/85 shadow-[0_8px_32px_-4px_rgba(0,0,0,0.5),inset_0_1px_0_0_rgba(255,255,255,0.12)] backdrop-blur-xl py-2 px-4 sm:px-6"
            : "rounded-full border border-white/[0.06] bg-[#0A0A0E]/60 shadow-[0_4px_24px_rgba(0,0,0,0.2),inset_0_1px_0_0_rgba(255,255,255,0.08)] backdrop-blur-md py-2.5 px-5 sm:px-7"
        }`}
      >
        <div className="flex items-center justify-between">
          {/* Logo e Identidade da Marca */}
          <a href="/" className="flex items-center gap-2.5 group focus:outline-none focus-visible:ring-2 focus-visible:ring-indigo-500 rounded-lg">
            <div className="h-8 w-8 rounded-lg bg-gradient-to-tr from-indigo-500 to-cyan-400 p-[1px] shadow-sm">
              <div className="h-full w-full bg-[#0A0A0E] rounded-[7px] flex items-center justify-center">
                <span className="text-xs font-bold text-white tracking-tighter">NG</span>
              </div>
            </div>
            <span className="text-sm font-semibold tracking-tight text-white group-hover:text-indigo-300 transition-colors">
              Navbar<span className="text-indigo-400">.gallery</span>
            </span>
          </a>

          {/* Links Desktop Centrais com Sliding Pill Hover Indicator */}
          <div
            className="hidden md:flex items-center gap-1"
            onMouseLeave={() => setHoveredLink(null)}
          >
            {NAVIGATION_ITEMS.map((item) => {
              const isDropdown = Boolean(item.items);
              const isOpen = activeDropdown === item.label;

              return (
                <div
                  key={item.label}
                  className="relative"
                  onMouseEnter={() => {
                    setHoveredLink(item.label);
                    if (isDropdown) handleMouseEnter(item.label);
                  }}
                  onMouseLeave={() => {
                    if (isDropdown) handleMouseLeave();
                  }}
                >
                  <a
                    href={item.href || "#"}
                    className={`relative z-10 flex items-center gap-1.5 px-3.5 py-1.5 text-xs font-medium transition-colors duration-150 rounded-full ${
                      isOpen || hoveredLink === item.label
                        ? "text-white"
                        : "text-zinc-400 hover:text-zinc-200"
                    }`}
                  >
                    {item.label}
                    {isDropdown && (
                      <ChevronDown
                        className={`h-3.5 w-3.5 transition-transform duration-200 ${
                          isOpen ? "rotate-180 text-indigo-400" : "text-zinc-500"
                        }`}
                      />
                    )}
                  </a>

                  {/* Micro-Pill Deslizante sob o Link */}
                  {hoveredLink === item.label && (
                    <motion.div
                      layoutId="nav-hover-pill"
                      transition={{ type: "spring", stiffness: 450, damping: 32 }}
                      className="absolute inset-0 z-0 rounded-full bg-white/[0.08]"
                    />
                  )}

                  {/* 3. Mega Menu / Dropdown Suspenso */}
                  {isDropdown && isOpen && (
                    <div className="absolute top-full left-0 pt-3 z-50">
                      <motion.div
                        initial={{ opacity: 0, y: 8, scale: 0.98 }}
                        animate={{ opacity: 1, y: 0, scale: 1 }}
                        exit={{ opacity: 0, y: 6, scale: 0.98 }}
                        transition={{ type: "spring", stiffness: 350, damping: 28 }}
                        className="w-[480px] rounded-2xl border border-white/[0.1] bg-[#0E0E14]/95 p-3 shadow-2xl backdrop-blur-2xl"
                      >
                        <div className="grid grid-cols-2 gap-2">
                          {item.items?.map((subItem) => {
                            const IconComponent = subItem.icon;
                            return (
                              <a
                                key={subItem.title}
                                href={subItem.href}
                                className="group/card flex items-start gap-3 rounded-xl p-2.5 transition-colors hover:bg-white/[0.05]"
                              >
                                <div className="mt-0.5 flex h-8 w-8 shrink-0 items-center justify-center rounded-lg border border-white/[0.08] bg-white/[0.04] text-zinc-300 group-hover/card:border-indigo-500/40 group-hover/card:bg-indigo-500/10 group-hover/card:text-indigo-400 transition-colors">
                                  <IconComponent className="h-4 w-4" />
                                </div>
                                <div className="flex flex-col">
                                  <div className="flex items-center gap-1.5">
                                    <span className="text-xs font-semibold text-zinc-200 group-hover/card:text-white transition-colors">
                                      {subItem.title}
                                    </span>
                                    {subItem.badge && (
                                      <span className="rounded-full bg-indigo-500/20 px-1.5 py-0.2 text-[9px] font-semibold text-indigo-300">
                                        {subItem.badge}
                                      </span>
                                    )}
                                  </div>
                                  <span className="mt-0.5 text-[11px] leading-tight text-zinc-400">
                                    {subItem.description}
                                  </span>
                                </div>
                              </a>
                            );
                          })}
                        </div>

                        {/* Banner Rodapé do Mega Menu */}
                        <div className="mt-2 flex items-center justify-between border-t border-white/[0.06] pt-2 px-2 text-[11px] text-zinc-400">
                          <span>Looking for custom integrations?</span>
                          <a href="/enterprise" className="font-semibold text-indigo-400 hover:text-indigo-300 transition-colors">
                            Talk to Engineers →
                          </a>
                        </div>
                      </motion.div>
                    </div>
                  )}
                </div>
              );
            })}
          </div>

          {/* Botões de Ação à Direita (CTA) */}
          <div className="hidden md:flex items-center gap-3">
            <a
              href="/login"
              className="text-xs font-medium text-zinc-300 hover:text-white transition-colors px-2 py-1"
            >
              Log in
            </a>
            <a
              href="/signup"
              className="relative inline-flex items-center justify-center rounded-full bg-white px-4 py-1.5 text-xs font-semibold text-black shadow-md transition-all hover:bg-zinc-200 active:scale-95"
            >
              Get Started
            </a>
          </div>

          {/* Botão Hambúrguer Mobile */}
          <div className="flex md:hidden">
            <button
              onClick={() => setIsMobileMenuOpen(!isMobileMenuOpen)}
              className="p-1.5 rounded-lg text-zinc-400 hover:text-white focus:outline-none focus-visible:ring-2 focus-visible:ring-indigo-500"
              aria-label="Toggle navigation menu"
            >
              {isMobileMenuOpen ? <X className="h-5 w-5" /> : <Menu className="h-5 w-5" />}
            </button>
          </div>
        </div>

        {/* 4. Gaveta Mobile Desdobrável */}
        <AnimatePresence>
          {isMobileMenuOpen && (
            <motion.div
              initial={{ opacity: 0, height: 0 }}
              animate={{ opacity: 1, height: "auto" }}
              exit={{ opacity: 0, height: 0 }}
              transition={{ duration: 0.25, ease: "easeInOut" }}
              className="overflow-hidden md:hidden border-t border-white/[0.08] mt-3 pt-3 flex flex-col gap-2"
            >
              {NAVIGATION_ITEMS.map((item) => (
                <div key={item.label} className="flex flex-col">
                  <a
                    href={item.href || "#"}
                    className="py-2 text-sm font-medium text-zinc-300 hover:text-white"
                  >
                    {item.label}
                  </a>
                  {item.items && (
                    <div className="pl-3 flex flex-col gap-1.5 border-l border-white/[0.08] my-1">
                      {item.items.map((subItem) => (
                        <a
                          key={subItem.title}
                          href={subItem.href}
                          className="text-xs text-zinc-400 hover:text-indigo-300 py-1"
                        >
                          {subItem.title}
                        </a>
                      ))}
                    </div>
                  )}
                </div>
              ))}
              <div className="pt-2 border-t border-white/[0.08] flex flex-col gap-2">
                <a
                  href="/login"
                  className="w-full text-center py-2 text-xs font-medium text-zinc-300"
                >
                  Log in
                </a>
                <a
                  href="/signup"
                  className="w-full text-center rounded-full bg-white py-2 text-xs font-semibold text-black"
                >
                  Get Started
                </a>
              </div>
            </motion.div>
          )}
        </AnimatePresence>
      </motion.nav>
    </header>
  );
}
```

---

### 5.4 Como a IA Deve Pesquisar ao Vivo no Navbar Gallery

Quando o agente de design engineering precisar pesquisar por referências de barras específicas no portal ao vivo (`https://www.navbar.gallery/`), deve utilizar a estrutura de rotas direta do site:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        URL QUERY STRUCTURE FOR LIVE AGENTS                             │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ 1. BUSCA POR TIPO ESTRUTURAL DE NAVEGAÇÃO:                                             │
│    • Static / Sticky Básico      ► https://www.navbar.gallery/type/static              │
│    • Menus com Dropdown / Flyout ► https://www.navbar.gallery/type/dropdowns           │
│    • Mega Menus Multi-coluna     ► https://www.navbar.gallery/type/mega-menu           │
│    • Sidebars & Painéis Verticais► https://www.navbar.gallery/type/side-bar            │
│    • Barras de Busca / Cmd+K     ► https://www.navbar.gallery/type/search-bar          │
│    • Announcement / Promo Banner ► https://www.navbar.gallery/type/announcement        │
│    • Menus Fullscreen / Imersivo ► https://www.navbar.gallery/type/full-screen        │
│    • Breadcrumbs & Hierarquia    ► https://www.navbar.gallery/type/breadcrumbs        │
│    • Mobile-Specific Navigations ► https://www.navbar.gallery/mobile-navigation        │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ 2. BUSCA POR ESTILO & VERTICAL DE MERCADO:                                             │
│    • Dark Mode & Glassmorphism   ► https://www.navbar.gallery/style/dark               │
│    • Estética Bento Box          ► https://www.navbar.gallery/style/bento-box          │
│    • Superfícies Desfocadas      ► https://www.navbar.gallery/style/blurred            │
│    • Empresas e Ferramentas AI   ► https://www.navbar.gallery/style/ai                 │
│    • SaaS B2B de Alta Conversão  ► https://www.navbar.gallery/style/saas               │
│    • Brutalismo e Linhas Cruas   ► https://www.navbar.gallery/style/brutalist          │
│    • Minimalismo Editorial       ► https://www.navbar.gallery/style/minimal            │
│    • Animações GSAP Complexas    ► https://www.navbar.gallery/style/gsap               │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ 3. BUSCA POR FRAMEWORK OU CMS:                                                         │
│    • Projetos Feitos no Framer   ► https://www.navbar.gallery/framer-navbars           │
│    • Projetos Feitos no Webflow  ► https://www.navbar.gallery/webflow-navbars          │
│ 4. PAGINAÇÃO E ÍNDICE GERAL:                                                           │
│    • Página de Busca & Filtros   ► https://www.navbar.gallery/browse                   │
│    • Paginação Numérica          ► https://www.navbar.gallery/?d25fafcb_page=N         │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir o documento de arquitetura visual e técnica (`DESIGN_BLUEPRINT.md`), o arquiteto deve auditar o header do projeto contra este checklist de 12 pontos:

1. [ ] **Definição Clara do Arquétipo**: Declarar explicitamente se o projeto usará *Floating Pill Island*, *Full-bleed Edge-to-Edge*, *Enterprise Mega Menu* ou *Collapsible Sidebar*.
2. [ ] **Camada de Vidro (Backdrop Glass Recipe)**: Empregar `backdrop-blur-md` ou `backdrop-blur-xl` com fundo a 75-85% de opacidade e compensação de saturação (`saturate(180%)`).
3. [ ] **Bordas Hairline Especulares**: Substituir `box-shadow` difuso por borda milimétrica de 1px com `rgba(255,255,255,0.08)` (escuro) ou `rgba(0,0,0,0.06)` (claro), combinada com `inset 0 1px 0 rgba(255,255,255,0.12)`.
4. [ ] **Scroll Behavior Throttling**: Garantir que os listeners de rolagem utilizem eventos passivos (`{ passive: true }`) e recolham a barra apenas após rolagem descendente sustentada (>80px), reaparecendo com qualquer subida de 8px.
5. [ ] **Taxonomia de Elevação (Z-Index Scale)**: Reservar `z-50` para a navbar, `z-55` para dropdowns e garantir que modais fiquem em `z-70+`.
6. [ ] **Diagonal Safe Area no Hover**: Para menus flyout e mega menus, implementar área de tolerância ou utilizar primitivas acessíveis do Radix UI para evitar fechamento acidental do submenu.
7. [ ] **Indicador de Link Ativo Tátil**: Utilizar indicador de fundo animado (`layoutId` no Framer Motion) com parâmetros de mola rápida (`stiffness: 450, damping: 32`).
8. [ ] **Escala Tipográfica Controlada**: Links de navegação devem respeitar o limite entre 13px e 14px (`text-xs font-medium` ou `text-sm font-medium`), com tracking neutro ou ligeiramente negativo (`-0.01em`).
9. [ ] **Micro-Tags & Badges de Destaque**: Usar pílulas atômicas para itens novos (*"NEW"*, *"BETA"*, *"AI"*) com fonte monoespaçada de 9px a 10px em cores vivas.
10. [ ] **Ergonomia Mobile Dedicada**: Em viewports móveis (<768px), limitar a altura da barra a 52px ou adotar uma dock bar inferior para facilitar o alcance do polegar.
11. [ ] **Acessibilidade Teclado/Leitores de Tela**: Todos os toggles devem ter `aria-expanded`, suporte a fechamento por tecla `Escape` e contorno nítido de foco via `:focus-visible`.
12. [ ] **Isolamento de Funis de Conversão**: Remover a barra de navegação completa em fluxos sensíveis de checkout, pagamento ou formulários de onboarding de tela cheia.
