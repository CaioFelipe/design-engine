---
id: "curated-design"
name: "Curated Design"
url: "https://www.curated.design/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico:
  - "Modern High-Craft Digital Aesthetic (SaaS, Studio & Fintech Precision)"
  - "Decomposição Anatômica em Seções Atômicas (Atomic Section Dissection)"
  - "Tipografia Editorial Híbrida (Geometric Sans Euclid + Display Serif Hedvig)"
  - "Quiet Luxury Dark/Light Adaptativo (Canvas OKLCH + Progressive Blur Shaders)"
  - "Curadoria Humana Baseada em Código em Produção (Real Live Shipped Websites)"
  - "Pioneirismo em AI Coding Agent Bridge (Nativo MCP — Model Context Protocol)"
  - "Design System As Code Extraction (Tokens Tailwind v4, CSS Vars e DESIGN.md)"
densidade_informacao: "Media/Narrativa a Alta/Utilitaria"
impacto_visual: "Editorial/Sofisticado & Contemporaneo/Tech"
custo_computacional: "Medio-Baixo (Astro SSG, Edge-Optimized BunnyCDN, Lazy Video com Concurrency Control, Zero WebGL Pesado)"
stack_frameworks:
  - "Astro 4+ (Islands Architecture & Edge Static Delivery)"
  - "Tailwind CSS v3/v4 com Design Tokens Estritos"
  - "PostHog Analytics First-Party Proxy Ingestion"
  - "BunnyCDN Global Storage (HLS/MP4 Video Edge Streaming + Retina WebP)"
  - "LemonSqueezy Merchant Billing Engine"
  - "Model Context Protocol (MCP HTTP & OAuth Remote Server)"
compatibilidade:
  fontes_ideais:
    - "Display Serif Editorial & Contemporânea: Hedvig Letters Serif, Newsreader, GT Sectra, PP Editorial New, Fraunces, Ogg, Reckless"
    - "Geometric & Neo-Grotesque Sans: Euclid Circular A, PP Neue Montreal, Inter, General Sans, SF Pro Display, Suisse Int'l, Geist"
    - "Monoespaçada Técnica para Tokens & Code: Geist Mono, Fragment Mono, JetBrains Mono, SF Mono"
  paletas_ideais:
    - "Curated Pure Light (Clean SaaS Base): #FFFFFF (Canvas Pure), #F8FAFC (Base 50 Surface), #F1F5F9 (Base 100 Border), #0F172A (Base 900 High Contrast Text), #EA580C (Accent Orange 600 CTA)"
    - "Curated Dark Obsidian (Pro Ambient): oklch(0.17 0 0) (Deep OKLCH Obsidian Canvas), #171717 (Card Surface), #262626 (Hairline Border 1px), #FFFFFF (Primary Headings), #A3A3A3 (Muted Copy), #F97316 (Accent 500 Highlight)"
    - "Subtle Stone / Warm Paper: #FAFAF9 (Warm Canvas), #F5F5F4 (Warm Surface), #E7E5E4 (Rule Border), #1C1917 (Warm Black), #78716C (Warm Zinc Subtitle)"
    - "Neo-Bank Electric Iris: #090A0F (Midnight Black), #12141F (Surface Tint), #847DFF (Electric Iris Accent), #E2E8F0 (Text Slate)"
  combinacoes_recomendadas:
    - "Tailwind CSS com tokens semânticos `base-*` e `accent-*` em escala OKLCH para neutralidade perceptual estrita em transições de tema"
    - "Framer Motion com curvas de desaceleração suave (`ease: [0.16, 1, 0.3, 1]`) para gavetas de filtros modais e elevação de cards (`card-lift`)"
    - "IntersectionObserver nativo com controle de concorrência para previews em vídeo (limite de 1 vídeo em mobile, 2 em desktop)"
    - "Linear Gradient CSS Edge-Fade Masks (`mask-image: linear-gradient(...)`) acoplados a `requestAnimationFrame` para chips de scroll horizontal"
    - "Astro / Next.js com geração estática e hidratação seletiva para performance de 100 no Lighthouse"
  conflitos_esteticos:
    - "Brutalismo não intencional com tipografias descalibradas ou desalinhadas"
    - "Sombras difusas pesadas do Material Design clássico (`box-shadow: 0 10px 30px rgba(0,0,0,0.15)`); a estética Curated prioriza bordas de 1px `border-base-100` e elevações mínimas de 1px a 2px"
    - "Gradientes neon arco-íris saturados sem propósito funcional ou hierárquico"
    - "Cards sem aspect ratio disciplinado (o padrão ouro é 16:9 widescreen para websites e proporções dinâmicas contidas para seções)"
    - "Animações acrobáticas e desnecessárias de rotação 3D que atrasam a visualização rápida do produto"
---

# Curated Design — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
 ██████╗██╗   ██╗██████╗  █████╗ ████████╗███████╗██████╗     ██████╗ ███████╗███████╗██╗ ██████╗ ███╗   ██╗
██╔════╝██║   ██║██╔══██╗██╔══██╗╚══██╔══╝██╔════╝██╔══██╗    ██╔══██╗██╔════╝██╔════╝██║██╔════╝ ████╗  ██║
██║     ██║   ██║██████╔╝███████║   ██║   █████╗  ██║  ██║    ██║  ██║█████╗  ███████╗██║██║  ███╗██╔██╗ ██║
██║     ██║   ██║██╔══██╗██╔══██║   ██║   ██╔══╝  ██║  ██║    ██║  ██║██╔══╝  ╚════██║██║██║   ██║██║╚██╗██║
╚██████╗╚██████╔╝██║  ██║██║  ██║   ██║   ███████╗██████╔╝    ██████╔╝███████╗███████║██║╚██████╔╝██║ ╚████║
 ╚═════╝ ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝   ╚══════╝╚═════╝     ╚═════╝ ╚══════╝╚══════╝╚═╝ ╚═════╝ ╚═╝  ╚═══╝
               WEB DESIGN INSPIRATION FROM REAL, LIVE WEBSITES — WITH TASTE
```

---

## 1. DNA Estético & Filosofia de Curadoria

Fundado por **Farook** (designer e visionário de produtos digitais, em colaboração orgânica com a rede de design system e recursos visuais do **Craftwork**), o **Curated Design** (`https://curated.design/`) consolidou-se como a plataforma definitiva de inspiração e engenharia reversa para a elite do web design contemporâneo.

Ao contrário dos diretórios tradicionais da web (que catalogam capturas estáticas de páginas inteiras ou maquetes conceituais não testadas), o Curated Design fundamenta sua proposta de valor em três pilares axiomáticos:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        THE CURATED DESIGN ARCHITECTURAL PILLARS                        │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  [ REAL PRODUCTION CODE ] ──► [ ATOMIC SECTION DECONSTRUCTION ] ──► [ AI AGENT BRIDGE ]│
│   • 100% Live Shipped URLs    • Hero, Pricing, Bento, Footers     • Model Context Proto│
│   • Zero Dribbble mockups     • 3,338+ Isolated UI Sections       • Direct MCP Server  │
│   • Click straight through    • Tokens & Design Systems mapped    • Prompt-to-Code lib │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ AESTHETIC SIGNATURE: Quiet Craft • Crisp 1px Hairlines • Video Stream • Hybrid Type   │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 O Manifesto: "The Best Reference is a Site That's Still Running in Production"

O manifesto curatorial de Farook rejeita categoricamente maquetes de estúdio criadas exclusivamente para obter curtidas em redes sociais. Apenas websites reais, funcionais, publicados na internet e mantidos por empresas ativas (startups SaaS, fintechs de ponta, estúdios criativos, ferramentas de desenvolvedores e marcas de e-commerce premium) são aceitos. Cada entrada fornece link direto de redirecionamento, permitindo que desenvolvedores e designers inspecionem o DOM nativo, a responsividade tátil, a performance do scroll e a hierarquia tipográfica em tempo real.

### 1.2 A Revolução da Decomposição em Seções Atômicas (Sections Engine)

O grande divisor de águas do Curated Design em relação a galerias convencionais como Awwwards ou Siteinspire foi a introdução da biblioteca **Sections** (`/sections/`). Enquanto a maioria dos portais obriga o desenvolvedor a navegar por páginas completas de 5.000 pixels de altura para analisar uma simples tabela de preços, o Curated Design realiza uma **dissecação cirúrgica**:

- Mais de **3.338 seções individuais** catalogadas isoladamente.
- Classificação por blocos funcionais essenciais: Hero, Features, Bento Grids, Pricing Tables, Social Proof, Testimonials, FAQ, Footers e Navbars.
- O efeito pedagógico imediato: *"Coloque 40 tabelas de preços de ferramentas dark de desenvolvedores lado a lado e os padrões estruturais, a hierarquia de planos e o ritmo de botões CTA tornam-se óbvios."*

### 1.3 Pioneirismo Global em Conectividade para Agentes de IA (The MCP Era)

O Curated Design é a primeira galeria de design do mundo construída com arquitetura nativa para **Agentes de Código Autônomos** (Claude Code, Cursor, Codex, OpenCode, Lovable, v0). Sob o lema **"Your coding agent, with taste"**, a plataforma oferece um servidor **Model Context Protocol (MCP)** em `https://curated.design/api/mcp/`, acompanhado de um arquivo padronizado `SKILL.md`.

Isso permite que um LLM consulte o arquivo vivo do Curated Design via chamadas de ferramentas (`plan_page`, `search_sections`, `get_design_system`), baixando tokens reais de espaçamento, tipografia, paletas de cores e regras de motion antes de gerar uma única linha de JSX ou CSS, eliminando completamente as alucinações de layouts genéricos da IA (como gradientes roxos padronizados ou 3 cards idênticos centralizados).

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

O Curated Design deve ser adotado como a **Referência Primária de Direção de Arte** nas seguintes situações:

```
┌───────────────────────────────────────────────────────────────────────────────────────┐
│                        PRIMARY ARTIFACT & USE-CASE SCENARIOS                          │
├───────────────────────────────────────────────────────────────────────────────────────┤
│ 1. MODERN B2B SaaS & TECH PRODUCTS                                                    │
│    • Interfaces de alta conversão para produtos de Inteligência Artificial, DevTools, │
│      segurança cibernética, cloud infrastructure e plataformas de dados.               │
│                                                                                       │
│ 2. DARK-THEMED LUXURY & FINTECH                                                       │
│    • Plataformas financeiras modernas (estilo Stripe, Mercury, Ramp, Linear, Raycast) │
│      onde a seriedade técnica encontra a sofisticação editorial.                       │
│                                                                                       │
│ 3. DESIGN-SYSTEM-FIRST DEVELOPMENT                                                    │
│    • Projetos corporativos que exigem tokens rígidos de CSS Variables, Tailwind v4 e  │
│      documentação modularizada em `DESIGN.md`.                                        │
│                                                                                       │
│ 4. AGENT-DRIVEN DEVELOPMENT WORKFLOWS                                                 │
│    • Ambientes onde agentes de IA são instruídos a analisar e emular referências      │
│      de alto calibre antes de prototipar telas e componentes.                         │
└───────────────────────────────────────────────────────────────────────────────────────┘
```

### 2.1 Posicionamento Psicológico & Percepção de Marca
A estética catalogada no Curated Design comunica:
- **Autoridade Técnica e Rigor**: Ausência de excessos ornamentais, linhas estruturais afiadas e grids matemáticos passam credibilidade imediata.
- **Sofisticação Sem Esforço (Quiet Craft)**: O uso de tipografia display serifada contrastando com corpos de texto limpos em neo-grotesque estabelece um tom de liderança de mercado.
- **Fluidez Digital**: A presença de micro-vídeos em loop em vez de capturas estáticas estéreis transmite a sensação de um produto dinâmico, vivo e responsivo.

### 2.2 O Papel na Regra Áurea 60-30-10

| Camada | Proporção | Papel no Sistema Curated Design | Exemplos de Tokens & Superfícies |
| :--- | :---: | :--- | :--- |
| **Cor Dominante (Base Canvas)** | **60%** | Planos de fundo limpos, imersivos e silenciosos que acolhem a leitura e os dados. | `#FFFFFF` no Light Mode; `oklch(0.17 0 0)` ou `#0F1011` no Dark Mode. |
| **Cor Secundária (Superfícies & Estrutura)** | **30%** | Cards modulares, caixas de busca, bordas hairline sutis e tipografia primária de alto contraste. | `bg-base-50` (`#F8FAFC`), `border-base-100` (`#E2E8F0`), texto `base-900` (`#0F172A`). |
| **Cor de Acento (Foco de Conversão & Badges)** | **10%** | Pontos de atração visual estritamente funcionais: botões CTA principais, status de desbloqueio, chips selecionados e links ativos. | `accent-600` (`#EA580C` / Laranja Elétrico) ou `accent-iris` (`#847DFF`). |

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

> [!WARNING]
> A estética promovida pelo Curated Design não é uma solução universal. Sua aplicação indiscriminada em setores com expectativas visuais divergentes pode arruinar o engajamento e a conversão.

### 3.1 Cenários Totalmente Incompatíveis
1. **Serviços Governamentais, Utilidades Públicas ou Portais Cidadãos**: Interfaces públicas demandam contraste máximo estático, fontes padrão do sistema operacional, suporte a navegadores legados e densidade visual neutra sem elementos flutuantes ou micro-vídeos.
2. **E-commerce Popular de Varejo Massivo (FMCG)**: Lojas virtuais de varejo popular (Mercado Livre, Amazon, Shopee) dependem de badges vibrantes multicoloridos, contadores de escassez chamativos, banners gigantes promocionais e múltiplos pontos de clique ruidosos que conflitam frontalmente com a sobriedade minimalista.
3. **Aplicações para Crianças ou Gamificação Infantil**: A sobriedade dos tons monocromáticos e das fontes display serifadas gera frieza e desinteresse para públicos infantis, que demandam formas arredondadas volumosas, ilustrações multicoloridas lúdicas e tipografia orgânica amigável.
4. **Portais Corporativos Tradicionais de RH / Intranets Conservadoras**: Em setores extremamente conservadores onde a equipe utiliza monitores de baixa fidelidade cromática, fundos ultra escuros com linhas de 1px podem apresentar legibilidade comprometida.

### 3.2 Armadilhas de Imitação (Anti-Padrões Comuns)
- ❌ **"O Modo Escuro Vazio"**: Criar um fundo preto puro `#000000` sem trabalhar as camadas de elevação (`base-50`, `base-100`), resultando em uma interface chapada e sem profundidade.
- ❌ **"A Cópia Desprovida de Propósito"**: Reproduzir um Bento Grid complexo apenas pela aparência visual, espalhando dados aleatórios em caixas de tamanhos variados sem relação hierárquica lógica.
- ❌ **"Sobrecarga de Vídeos Sem Controle"**: Tentar carregar simultaneamente dezenas de animações MP4 na viewport do cliente, travando a CPU e estourando a franquia de dados móveis do usuário (o Curated Design implementa um throttle estrito com `IntersectionObserver`).
- ❌ **"Degeneração por Falta de Tokens"**: Misturar 8 tonalidades de cinza diferentes (`#111`, `#1a1a1a`, `#222`, `#2b2b2b`, `#333`) por não definir tokens semânticos unificados.

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

O Curated Design decompõe a interface moderna em elementos arquiteturais de altíssima precisão.

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo

```
┌───────────────────────────────────────────────────────────────────────────────────────┐
│                      CURATED VIEWPORT ARCHITECTURE & LAYOUT GRID                      │
├───────────────────────────────────────────────────────────────────────────────────────┤
│  [ FIXED HEADER / NAV ] ── Progressive Blur (5-Tier Backdrop Filter, 2px to 6px)      │
│  [ HERO / PROMPT BAR ] ── Max-w 3xl (768px), Natural Language Design Chat Input       │
│  [ FILTER RAIL BAR ]   ── Horizontal Snap Scroll + 64px Linear Gradient Edge-Fades    │
│  [ DENSITY SWITCHER ]  ── Switch between 2-Card (Heroic) & 3-Card (Compact Scan)      │
│  [ CARDS GRID ]        ── 1.77:1 (16:9 Aspect Video) with 1px Hairline Borders        │
│  [ EXPANDED DRAWER ]   ── 2-Column Responsive Multi-Facet Filter Matrix (Pro Lock)   │
└───────────────────────────────────────────────────────────────────────────────────────┘
```

1. **Escala de Contêineres**: O layout adota largura máxima ultra ampla (`max-w-[110rem]`, equivalente a 1760px) com padding horizontal generoso (`px-8`), aproveitando monitores de alta resolução sem comprometer a leitura.
2. **Proporção dos Cards (16:9 Widescreen)**: Todo o grid é sustentado por proporções cinematográficas (`aspect-video`, 16:9). Isso garante harmonia geométrica constante tanto para capturas estáticas quanto para streams de vídeo em alta definição.
3. **Linhas Hairline Estruturais**: Divisórias limpas de `1px` (`border-base-100`) substituem elevações baseadas em sombras difusas. Os cards contam com cantos suavemente lapidados (`rounded-lg` / 8px ou `rounded-xl` / 12px).

### 4.2 Sistemas de Cores, Superfícies & Texturas

```
┌───────────────────────────────────────────────────────────────────────────────────────┐
│                           COLOR & SURFACE SYSTEM MATRIX                               │
├───────────────────────────────────────────────────────────────────────────────────────┤
│ LIGHT MODE CORE:                                                                      │
│ Canvas Base:    #FFFFFF  │ Surface Card:  #F8FAFC (base-50)  │ Border: #E2E8F0       │
│ Ink Primary:    #0F172A  │ Ink Muted:     #64748B            │ Accent: #EA580C       │
├───────────────────────────────────────────────────────────────────────────────────────┤
│ DARK MODE CORE:                                                                       │
│ Canvas Base:    oklch(0.17 0 0) (~#161616) │ Surface: #1C1C1C │ Border: #2E2E2E     │
│ Ink Primary:    #FFFFFF                    │ Ink Muted: #888888 │ Accent: #F97316     │
├───────────────────────────────────────────────────────────────────────────────────────┤
│ SHADING & BLUR SYSTEM:                                                                │
│ Top Progressive Blur:   5 layers from blur(2px) to blur(6px) + alpha-mask ramp        │
│ Edge Fade Mask:         linear-gradient(to right, transparent, #000 64px, ...)        │
└───────────────────────────────────────────────────────────────────────────────────────┘
```

- **Canvas OKLCH**: No tema escuro, a plataforma utiliza a notação `oklch(0.17 0 0)`. Esse espaço de cor uniforme previne variações indesejadas de saturação em diferentes painéis OLED/IPS.
- **Script Anti-Flash Inline**: O tema é aplicado no `head` antes da renderização de qualquer folha de estilo (`window.__applyTheme`), garantindo que alternâncias de página nunca emitam o indesejado clarão branco (*flash of unstyled content*).
- **Progressive Blur Shaders**: A barra de navegação superior não utiliza um `backdrop-blur` uniforme simples; ela emprega um gradiente progressivo de desfoque multicamada de 5 etapas com máscaras lineares, fazendo com que o conteúdo que passa por baixo se dissolva suavemente sem recortes abruptos.

---

### 4.3 Catálogo de Arquétipos & Componentes Notáveis (8 Padrões Concretos)

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        CURATED DESIGN ARCHETYPAL PATTERNS                              │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ 1. NATURAL LANGUAGE DESIGN CHAT HERO ──► Conversational prompt input to filter library │
│ 2. DUAL-DENSITY GRID ENGINE          ──► Seamless 2-Col vs 3-Col layout switcher       │
│ 3. CONCURRENCY-THROTTLED VIDEO CARD  ──► Instant hover preview with device throttle    │
│ 4. PROGRESSIVE BLUR STEPPED NAV      ──► 5-layer optical depth navigation header       │
│ 5. EDGE-FADE HORIZONTAL FILTER CHIPS ──► Dynamic 64px alpha-gradient scroll pills      │
│ 6. ADVANCED MULTI-FACET DRAWER       ──► Accordion matrix (Styles, Visuals, Media)     │
│ 7. ATOMIC SECTION INSPECTOR & METER  ──► Code preview with token unlock quota counter  │
│ 8. MODEL CONTEXT PROTOCOL AGENT HUB  ──► One-line CLI snippet to link AI coding tools  │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

#### 1. Hero com Barra de Prompt em Linguagem Natural ("Design Chat")
- **Anatomia**: Título editorial em serif fina (`Hedvig Letters Serif`, 48px), subtítulo conciso e um campo de busca conversacional proeminente com botão de envio acionado por seta circular.
- **Gatilho & Interação**: O visitante digita livremente o que deseja construir (ex: *"A landing page for Overpass, crop maps for farmers"* ou *"Dark devtool pricing"*). O formulário dispara um evento analítico e monta uma página customizada de referências estruturadas (`/build/?brief=...`).
- **Onde Encaixar**: Heros de portais modernos, geradores de layout com IA e catálogos baseados em intenção.

#### 2. Comutador Dinâmico de Densidade de Grid (2-Col vs 3-Col Engine)
- **Anatomia**: Interruptor discreto com dois botões de ícone SVG posicionados no canto superior direito do grid.
- **Gatilho & Interação**: Permite alternar instantaneamente entre a visualização de 2 colunas (foco ampliado e detalhado na tipografia e no vídeo) e 3 colunas (visão panorâmica de alta densidade para varredura rápida). A preferência é gravada no `localStorage` e injetada via `dataset` no elemento raiz `<html>` antes do primeiro ciclo de pintura, evitando *layout shifts*.
- **Onde Encaixar**: Galerias de portfólio, catálogos de e-commerce e exploradores de componentes de UI.

#### 3. Card com Preview de Vídeo e Controle de Concorrência
- **Anatomia**: Moldura 16:9 (`aspect-video`) contendo esqueleto de carregamento cinza suave, imagem estática WebP de alta fidelidade e elemento `<video>` em loop mudo sem controles. Possui botões flutuantes de ação rápida: Bookmark (favoritar) e Direct Link (abrir site original).
- **Gatilho & Interação**: O vídeo não toca continuamente para todos os cards. Um `IntersectionObserver` calcula a visibilidade em relação ao centro da tela. Limites estritos de concorrência garantem que no máximo **1 vídeo toque por vez em dispositivos móveis** e **2 em desktops**, pausando imediatamente quando o usuário rola para fora ou ativa o modo de economia de dados (`navigator.connection.saveData`).
- **Onde Encaixar**: Showcases de produtos digitais, feeds de inspiração e páginas de templates.

#### 4. Barra de Navegação Flutuante com Desfoque Progressivo
- **Anatomia**: Barra de navegação em container largo fixo no topo (`fixed top-0 inset-x-0 z-20`), com links tipográficos nítidos de 13px, atalho de teclado global `⌘K` para busca e alternador de tema dark/light.
- **Gatilho & Interação**: Logo atrás do conteúdo da barra, um elemento com 5 camadas div sobrepostas aplica valores crescentes de desfoque (`backdrop-filter: blur(2px)` até `blur(6px)`) combinados com máscaras alfa lineares. A transição entre o cabeçalho e os cards rolando por baixo ocorre com suavidade óptica cinematográfica.
- **Onde Encaixar**: Headers de aplicações SaaS de alto padrão e landing pages corporativas.

#### 5. Trilho de Chips com Scroll Horizontal e Dissolvência Lateral (Edge-Fade)
- **Anatomia**: Fileira horizontal com chips de filtro de categorias (`All`, `Agency`, `AI`, `Dev Tools`, `Finance`, etc.) e estilos (`Minimal`, `Dark`, `Neo-brutalism`).
- **Gatilho & Interação**: Nas extremidades esquerda e direita, duas camadas com gradientes calculados via JavaScript monitoram a posição de rolagem (`scrollLeft` e `scrollWidth`). Quando a lista atinge o início ou o fim, a máscara alfa de 64px transiciona suavemente sua opacidade de `1` para `0` via `requestAnimationFrame`, indicando visualmente se há mais itens ocultos.
- **Onde Encaixar**: Menus de categorias em e-commerce, listagens com tags e seletores em smartphones.

#### 6. Gaveta de Filtros Avançados Multidimensionais (Advanced Filter Panel)
- **Anatomia**: Painel colapsável em acordeão com quatro grupos facetados: *Styles*, *Visuals* (3D, ilustrações, foto), *Attributes* e *Popular tags*, além de seletores suspensos de *Media* (Animated vs Static), *Date Added* e *Sort by*.
- **Gatilho & Interação**: O usuário seleciona múltiplos filtros sem recarregar a tela; um contador dinâmico exibe os resultados correspondentes em tempo real com opções para salvar buscas recorrentes.
- **Onde Encaixar**: Sistemas de busca complexos, diretórios de recursos e bibliotecas de componentes.

#### 7. Inspetor de Seção com Medidor de Desbloqueios Gratuitos (Free Unlocks Meter)
- **Anatomia**: Indicador visual na barra de navegação com pontos táteis (`free-meter-dots`) indicando cotas restantes de desbloqueio gratuito de blocos (2 desbloqueios gratuitos por conta).
- **Gatilho & Interação**: Ao abrir uma seção isolada, o usuário tem acesso à captura em altíssima resolução, ao prompt detalhado de reconstrução e aos tokens de código (Tailwind v4 / CSS Variables / JSON). Cada desbloqueio decrementa o medidor reativo client-side sem recarregar a página.
- **Onde Encaixar**: Modelos de negócio freemium para bibliotecas de código, UI kits e ferramentas de produtividade.

#### 8. Hub de Conexão com Agentes de Código via MCP (Model Context Protocol Hub)
- **Anatomia**: Aba interativa no portal com guias dedicadas para Claude Code, Cursor, Codex, OpenCode e REST API, contendo blocos com comandos de instalação de 1 clique e documentação das ferramentas exportadas.
- **Gatilho & Interação**: Clicar no botão de cópia copia instantaneamente o comando CLI (ex: `claude mcp add --transport http curated https://curated.design/api/mcp/`) e exibe feedback tátil no botão.
- **Onde Encaixar**: Portais de documentação para desenvolvedores, hubs de integração de IA e ferramentas para times de engenharia.

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Sistema de Variáveis e Design Tokens (CSS Tokens Recipe)

```css
/* ==========================================================================
   CURATED DESIGN TOKEN SYSTEM (OKLCH DUAL-THEME ENGINE)
   ========================================================================== */

:root {
  /* Canvas & Surfaces (Light) */
  --color-canvas: #ffffff;
  --color-surface-subtle: #f8fafc;
  --color-surface-hover: #f1f5f9;
  --color-surface-active: #e2e8f0;

  /* Hairline Borders */
  --border-hairline: #e2e8f0;
  --border-hairline-subtle: #f1f5f9;

  /* Typography Colors */
  --text-primary: #0f172a;
  --text-secondary: #475569;
  --text-muted: #94a3b8;

  /* Brand Accents */
  --color-accent-50: #fff7ed;
  --color-accent-500: #f97316;
  --color-accent-600: #ea580c;
  --color-accent-text: #ffffff;

  /* Typography Scales */
  --font-sans: "Euclid Circular A", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  --font-serif: "Hedvig Letters Serif", Georgia, serif;
  --font-mono: "Geist Mono", "JetBrains Mono", monospace;

  /* Spatial Rhythm & Radii */
  --radius-sm: 6px;
  --radius-md: 8px;
  --radius-lg: 12px;
  --radius-pill: 9999px;

  /* Fluid Motion Transitions */
  --ease-smooth: cubic-bezier(0.16, 1, 0.3, 1);
  --duration-fast: 150ms;
  --duration-normal: 300ms;
}

/* Dark Mode Activation via class "dark" */
html.dark {
  /* Canvas & Surfaces (OKLCH Obsidian Base) */
  --color-canvas: oklch(0.17 0 0); /* Ultra-pure neutral obsidian dark */
  --color-surface-subtle: #171717;
  --color-surface-hover: #262626;
  --color-surface-active: #333333;

  /* Hairline Borders */
  --border-hairline: #262626;
  --border-hairline-subtle: #1f1f1f;

  /* Typography Colors */
  --text-primary: #ffffff;
  --text-secondary: #a3a3a3;
  --text-muted: #525252;

  /* Accent Tone in Dark Space */
  --color-accent-500: #f97316;
  --color-accent-600: #ea580c;
}

/* Progressive Blur & Edge-Fade Utilities */
[data-edge-scroll] {
  --edge-fade-l: 0px;
  --edge-fade-r: 0px;
  -webkit-mask-image: linear-gradient(
    to right,
    transparent -1px,
    #000 var(--edge-fade-l),
    #000 calc(100% - var(--edge-fade-r)),
    transparent calc(100% + 1px)
  );
  mask-image: linear-gradient(
    to right,
    transparent -1px,
    #000 var(--edge-fade-l),
    #000 calc(100% - var(--edge-fade-r)),
    transparent calc(100% + 1px)
  );
}
```

---

### 5.2 Componente Funcional: Card com Vídeo Inteligente e Controle de Concorrência (React + Tailwind)

Abaixo, a implementação realista e funcional do card de website/seção utilizado no Curated Design, incluindo a reprodução inteligente de vídeo condicionada ao viewport e limites de recursos:

```tsx
import React, { useEffect, useRef, useState } from "react";
import { Bookmark, ArrowUpRight } from "lucide-react";

interface CuratedCardProps {
  id: string;
  title: string;
  category: string;
  siteUrl: string;
  thumbnailUrl: string;
  videoUrl?: string;
  isBookmarked?: boolean;
  onBookmarkToggle?: (id: string) => void;
}

export const CuratedCard: React.FC<CuratedCardProps> = ({
  id,
  title,
  category,
  siteUrl,
  thumbnailUrl,
  videoUrl,
  isBookmarked = false,
  onBookmarkToggle,
}) => {
  const [isVideoLoaded, setIsVideoLoaded] = useState(false);
  const [bookmarked, setBookmarked] = useState(isBookmarked);
  const videoRef = useRef<HTMLVideoElement>(null);
  const containerRef = useRef<HTMLDivElement>(null);

  useEffect(() => {
    const video = videoRef.current;
    if (!video || !videoUrl) return;

    // Respeita preferência por movimento reduzido ou economia de dados
    const prefersReducedMotion = window.matchMedia("(prefers-reduced-motion: reduce)").matches;
    const isSaveData = (navigator as unknown as { connection?: { saveData?: boolean } })?.connection?.saveData;

    if (prefersReducedMotion || isSaveData) return;

    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting && entry.intersectionRatio >= 0.5) {
            if (!video.src) {
              video.src = videoUrl;
              video.load();
            }
            video.play().catch(() => {
              // Bloqueio de autoplay do navegador tratado silenciosamente
            });
          } else {
            video.pause();
          }
        });
      },
      {
        rootMargin: "50px 0px",
        threshold: [0, 0.5, 1],
      }
    );

    observer.observe(video);

    return () => {
      observer.disconnect();
    };
  }, [videoUrl]);

  return (
    <article
      ref={containerRef}
      className="group relative flex flex-col rounded-xl border border-[var(--border-hairline)] bg-[var(--color-canvas)] p-2 transition-all duration-300 hover:border-zinc-400 dark:hover:border-zinc-600"
    >
      {/* Moldura de Mídia 16:9 */}
      <div className="relative aspect-video w-full overflow-hidden rounded-lg bg-[var(--color-surface-subtle)]">
        {/* Imagem estática de fallback */}
        <img
          src={thumbnailUrl}
          alt={`Screenshot do site ${title}`}
          loading="lazy"
          decoding="async"
          className="size-full object-cover object-top transition-transform duration-500 ease-out group-hover:scale-[1.02]"
        />

        {/* Stream de vídeo em loop discreto */}
        {videoUrl && (
          <video
            ref={videoRef}
            muted
            loop
            playsInline
            preload="none"
            onLoadedData={() => setIsVideoLoaded(true)}
            className={`absolute inset-0 size-full object-cover object-top transition-opacity duration-300 ${
              isVideoLoaded ? "opacity-100" : "opacity-0"
            }`}
          />
        )}

        {/* Camada de Ação Hover: Botões Flutuantes */}
        <div className="absolute right-2 top-2 z-20 flex items-center gap-1.5 opacity-0 transition-opacity duration-200 group-hover:opacity-100">
          <button
            type="button"
            onClick={(e) => {
              e.preventDefault();
              e.stopPropagation();
              setBookmarked(!bookmarked);
              onBookmarkToggle?.(id);
            }}
            aria-label={bookmarked ? "Remover dos favoritos" : "Salvar website"}
            className="flex size-8 items-center justify-center rounded-md bg-black/60 text-white backdrop-blur-md transition-colors hover:bg-black/90 active:scale-95"
          >
            <Bookmark
              size={15}
              className={bookmarked ? "fill-[var(--color-accent-500)] text-[var(--color-accent-500)]" : "text-white"}
            />
          </button>

          <a
            href={siteUrl}
            target="_blank"
            rel="noopener noreferrer"
            aria-label={`Visitar ${title} externamente`}
            className="flex size-8 items-center justify-center rounded-md bg-black/60 text-white backdrop-blur-md transition-colors hover:bg-black/90 active:scale-95"
          >
            <ArrowUpRight size={16} />
          </a>
        </div>
      </div>

      {/* Meta Informações Inferiores */}
      <div className="mt-2.5 flex items-center justify-between px-1">
        <h3 className="truncate font-sans text-sm font-medium text-[var(--text-primary)]">
          {title}
        </h3>
        <span className="rounded-md bg-[var(--color-surface-hover)] px-2 py-0.5 text-[11px] font-medium capitalize text-[var(--text-secondary)]">
          {category}
        </span>
      </div>
    </article>
  );
};
```

---

### 5.3 Como a IA Deve Pesquisar ao Vivo no Curated Design (Live Query Protocols)

Quando um agente de IA ou desenvolvedor precisar coletar inspirações em tempo real no Curated Design, ele deve utilizar a estrutura oficial de URLs e chamadas estruturadas:

#### 1. Chamadas Via Model Context Protocol (MCP)

```bash
# Adicionar o servidor remoto Curated ao agente Claude Code
claude mcp add --transport http curated https://curated.design/api/mcp/

# Estrutura JSON no arquivo .cursor/mcp.json para o Cursor
{
  "mcpServers": {
    "curated": {
      "url": "https://curated.design/api/mcp/"
    }
  }
}
```

**Chamadas de ferramentas típicas para o agente**:
- `plan_page(brief: "Dark developer tool landing page with pricing and bento grid")`
- `search_sections(type: "pricing", query: "dark devtool", page: 1)`
- `get_design_system(siteId: "140633", format: "tailwind")`
- `get_section(sectionId: "2170")`

#### 2. Estrutura de URLs de Busca Direta na Web

| Intenção de Pesquisa | Formato Exato da URL |
| :--- | :--- |
| **Explorar Todos os Websites por Categoria** | `https://curated.design/?category={agency\|artificial-intelligence\|finance\|dev-tools}` |
| **Explorar por Estilo Visual** | `https://curated.design/?style={minimal\|dark\|neobrutalism\|gradients\|animated}` |
| **Biblioteca de Seções por Tipo Específico** | `https://curated.design/sections/type/{hero\|pricing\|features\|bento\|footer}/` |
| **Busca Cruzada de Seção (Tipo + Estilo)** | `https://curated.design/sections/type/pricing/?style=dark` |
| **Busca de Seções por Indústria** | `https://curated.design/sections/?category=artificial-intelligence` |
| **Gerador de Briefing Conversacional** | `https://curated.design/build/?brief={palavras+chave+codificadas}` |
| **Endpoint REST Direto (Autenticado)** | `GET https://curated.design/api/v1/search/?q={query}&type={type}` |

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir especificações de design (`DESIGN_BLUEPRINT.md`) para projetos que se inspiram no Curated Design, o arquiteto de software e o designer de produto devem aplicar as seguintes diretrizes normativas:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        BLUEPRINT SPECIFICATION PROTOCOL                                │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ 1. PAIRING TIPOGRÁFICO HÍBRIDO                                                         │
│    • Headline H1: Hedvig Letters Serif (Display editorial, tracking -0.02em, light)   │
│    • Corpo & UI: Euclid Circular A ou PP Neue Montreal (limpa, legível, neutra)       │
│    • Tokens & Metadados: Geist Mono (tabular, números alinhados, dados técnicos)       │
│                                                                                        │
│ 2. ESTRUTURA DE BORDAS HAIRLINE & MODULARIDADE                                         │
│    • Proibir sombras pesadas difusas; utilizar exclusivamente bordas de 1px hairline   │
│      (`border-zinc-200` no light, `border-zinc-800` no dark).                          │
│    • Arredondamento consistente: 8px para cards internos, 12px para modais e gavetas.  │
│                                                                                        │
│ 3. POLÍTICA DE SEÇÕES ATÔMICAS INDEPENDENTES                                           │
│    • Cada seção da landing page deve ser concebida como um bloco auto-suficiente:      │
│      [Hero] -> [Social Proof Logos] -> [Bento Features] -> [Interactive Pricing] ->   │
│      [FAQ Accordion] -> [Minimal Footer].                                             │
│                                                                                        │
│ 4. ECONOMIA DE RECURSOS EM MÍDIA DINÂMICA                                              │
│    • Implementar IntersectionObserver com teto de concorrência estrita (1 vídeo em     │
│      mobile, 2 em desktop) com pausa automática em modo `saveData` ou bateria baixa.   │
│                                                                                        │
│ 5. RECONCILIAÇÃO COM CODING AGENTS                                                     │
│    • Todo componente deve possuir documentação de props semânticos, acessibilidade     │
│      WCAG AA (contraste mínimo 4.5:1) e atributos analíticos `data-analytics-label`.  │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### Síntese Final
O **Curated Design** transcende o conceito de uma simples galeria estética: é um **ecossistema de engenharia reversa de interfaces reais**. Ao conectar curadoria humana de alto padrão, decomposição atômica em mais de 3.000 seções e pontes automáticas de contexto para IA via MCP, a plataforma estabelece o padrão de referência para a criação de produtos digitais contemporâneos que equilibram bom gosto artístico inquestionável e rigor técnico de produção.
