---
id: "useplanes"
name: "Useplanes (Planes)"
url: "https://www.useplanes.com/"
category: "6-templates"
schema_type: "C-galleries"
dna_estetico:
  - "Agent-Ready UI Architecture"
  - "Tactile Physics & Kinetic Settling"
  - "Bayer Ordered Dither & Halftone Data-Viz"
  - "GPU WebGL Fragment Shaders"
  - "Zero-Lockin shadcn Registry Distribution"
  - "Linear & Apple Precision Craftsmanship"
  - "Tailwind CSS v4 & Motion Engine"
densidade_informacao: "Alta/Utilitaria"
impacto_visual: "Experimental/Imersivo"
custo_computacional: "Medio (Spring Transforms & Canvas 2D) a Alto (WebGL Raymarching & Fluid Sim)"
stack_frameworks:
  - "React 19"
  - "Next.js App Router"
  - "Tailwind CSS v4"
  - "Motion (motion package / Framer Motion)"
  - "shadcn CLI Registry Architecture"
  - "TypeScript"
  - "Lucide React"
  - "HTML5 Canvas 2D"
  - "WebGL GLSL Shaders"
compatibilidade:
  fontes_ideais:
    - "Geist Sans & Geist Mono (Vercel)"
    - "Inter (Rasmus Andersson)"
    - "SF Pro & SF Mono (Apple)"
    - "Cabinet Grotesk & Clash Display"
    - "Instrument Serif (Contrastes Editoriais em Heroes)"
  paletas_ideais:
    - "Deep Void Canvas: #000000 e #09090b com superfícies de cartão #111115 e #18181b"
    - "Bisel & Luz Incidente: border-white/5 a border-white/10 com destaques internos inset 0 1px 0 rgba(255,255,255,0.08)"
    - "Monocromático Técnico: Tons neutros de cinza com saturação mínima para priorizar a física da interface"
    - "Acentos Funcionais de Alta Tensão: #2f6cff (Electric Blue), #6366f1 (Indigo Trace), #10b981 (Emerald State), #f59e0b (Amber Warning)"
    - "Gradientes Volumétricos e Caustics: Shaders fluidos RGB sem cores pastéis genéricas"
  combinacoes_recomendadas:
    - "Tailwind CSS v4 + Motion (`motion/react`) para eliminar reflows de layout através de transforms aceleradas por hardware"
    - "shadcn MCP Server integrado a Cursor / Claude Code para injeção autônoma de código em tempo de prompting"
    - "Canvas 2D API com matrizes Bayer 4x4/8x8 para renderização de gráficos dither de baixo custo computacional"
    - "Radix UI Primitives + Lucide Icons para ancoragem acessível de menus, popovers e tooltips"
  conflitos_esteticos:
    - "Animações lineares sem molas amortecidas (ex: `transition: all 0.3s ease-in-out` arbitrário)"
    - "Bordas espessas e coloridas (>1px) que quebram o refinamento milimétrico de bisel industrial"
    - "Pacotes npm pesados do tipo 'black box' que ocultam o código fonte e impedem customização nativa"
    - "Sobrecarga de múltiplos efeitos WebGL pesados rodando em background simultaneamente sem pause on viewport leave"
    - "Ignorar a diretiva de acessibilidade `prefers-reduced-motion: reduce`"
---

# Planes (Useplanes) — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
 ██████╗ ██╗      █████╗ ███╗   ██╗███████╗███████╗   ██╗   ██╗██╗
 ██╔══██╗██║     ██╔══██╗████╗  ██║██╔════╝██╔════╝   ██║   ██║██║
 ██████╔╝██║     ███████║██╔██╗ ██║█████╗  ███████╗   ██║   ██║██║
 ██╔═══╝ ██║     ██╔══██║██║╚██╗██║██╔══╝  ╚════██║   ██║   ██║██║
 ██║     ███████╗██║  ██║██║ ╚████║███████╗███████║██╗╚██████╔╝██║
 ╚═╝     ╚══════╝╚═╝  ╚═╝╚═╝  ╚═══╝╚══════╝╚══════╝╚═╝ ╚═════╝ ╚═╝
```

---

## 1. DNA Estético, Filosofia de Curadoria & O Que Torna Único (Assinatura)

O **Planes** (`https://www.useplanes.com/`), idealizado e construído pelo engenheiro de software e designer de produto **Ashish Gogula** (@ashishgogula), é uma das bibliotecas de componentes e experiências de interface mais sofisticadas e influentes do ecossistema moderno de React. Posicionando-se como *"The agent-ready interaction layer for React"*, o Planes estabelece um novo paradigma de produção: ele rejeita terminantemente tanto pacotes npm opacos com código compilado e lock-in quanto agregadores superficiais de snippets puramente decorativos.

### 1.1 A Gênese e Filosofia: "Nothing snaps, everything settles"
A filosofia central do Planes parte do princípio de que **o movimento é a forma primária pela qual o software constrói confiança com o usuário**. Antes que um visitante processe conscientemente o texto de uma proposta de valor ou analise a lista de recursos de um SaaS, ele percebe subconscientemente — em frações de milissegundos — a resposta mecânica da interface. Se os elementos saltam instantaneamente sem inércia (*snap*), se os tooltips piscam (*flicker*) ou se os diálogos travam a interação durante uma transição, a aplicação transmite fragilidade e falta de cuidado.

Em contrapartida, inspirando-se no padrão de engenharia do **Linear**, do ecossistema de design da **Apple** e da carteira **Family**, o Planes baseia-se em um mantra rigoroso:
> *"Nothing snaps, everything settles. Springs over duration curves, interruptible over choreographed, and every component respects reduced motion so polish never comes at anyone's expense."*

Cada elemento visual no Planes possui **massa**, **momento angular**, **rigidez elástica** (*stiffness*) e **amortecimento de desaceleração** (*damping*). Quando um modal fecha, um cartão é arrastado ou uma gaveta é solta, o movimento pode ser interrompido a meio caminho sem saltar para estados finais abruptos.

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                       THE PLANES INTERACTION PIPELINE                       │
├─────────────────────────────────────────────────────────────────────────────┤
│  [ Pointer / Touch Event ] ──► [ Spring Physics Kernel ] ──► [ GPU Layer ]  │
│   • Velocity Tracking          • Dynamic Stiffness           • transform 3D │
│   • Momentum Preservation      • Critical Damping (No snap)  • will-change  │
│   • Drag Resistance Bounds     • Sub-pixel Interpolation     • zero reflow  │
├─────────────────────────────────────────────────────────────────────────────┤
│  RENDER: Halftone Dither (Canvas) + Kinetic UI (Motion) + GLSL Shaders      │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 1.2 O Conceito "Agent-Ready Interaction Layer": A Fusão shadcn + MCP
O grande diferencial arquitetural do Planes em relação a qualquer galeria ou biblioteca anterior é o fato de ter sido construído nativamente para a era dos **Agentes Autônomos de Código** (Cursor, Claude Code, GitHub Copilot, Codex, Windsurf).
1. **Distribuição via shadcn Registry**: O Planes não é instalado como `node_modules/@useplanes/components`. Ele utiliza o protocolo de registro aberto do **shadcn/ui** (`npx shadcn add @useplanes/<slug>`). O código TypeScript (`.tsx`) e os estilos Tailwind v4 são injetados diretamente na árvore do repositório do desenvolvedor. O usuário é o detentor integral do código-fonte (*zero runtime lock-in*).
2. **Integração Nativa com Model Context Protocol (MCP)**: O Planes fornece suporte imediato ao servidor MCP oficial do shadcn (`shadcn@latest mcp init --client claude` ou `cursor://` deep link). Isso permite que agentes de IA compreendam os esquemas de propriedades de cada componente, inspecionem as dependências e instalem componentes complexos a partir de comandos em linguagem natural (ex: *"Adicione a tabela de preços do @useplanes com alternância anual e suporte a dark mode"*).
3. **Instruções Semânticas para Agentes (`AGENTS.md` / `CLAUDE.md`)**: A documentação do Planes é desenhada para LLMs através de arquivos compactados e sem ruído estruturados em `llms.txt` e `llms-full.txt`, garantindo que modelos de raciocínio compreendam como orquestrar seus estados sem alucinar dependências externas inexistentes.

### 1.3 Diferenciação Estratégica no Ecossistema
A tabela abaixo desconstruída do próprio laboratório do Planes explicita o abismo técnico entre as abordagens de mercado:

| Biblioteca | Foco Primário | Formato de Entrega | Onde Falha / Limitações |
| :--- | :--- | :--- | :--- |
| **Planes (useplanes.com)** | **Componentes completos de produto (AI chat, física, WebGL, dither charts, controles analógicos)** | Registro shadcn (`.tsx` puro) + MCP | Requer Tailwind v4 e React 19; componentes Pro exigem chave de licença de aquisição vitalícia única. |
| **Magic UI** | Efeitos de marketing para landing pages (bordas brilhantes, confetes) | Registro shadcn | Quase nenhuma peça voltada à UI real de produto (chat, diffs de código, charts de dados densos). |
| **Aceternity UI** | Efeitos visuais experimentais para hero sections (3D pin, lamp effect) | Código aberto / copy-paste | Focado quase exclusivamente no topo de funil de marketing; ausência de controles táteis granulares de aplicação. |
| **React Bits** | Snippets atômicos e efeitos isolados em Tailwind/CSS | Copy-paste manual | Efeitos atômicos desconectados; o desenvolvedor é obrigado a estruturar toda a UI e acessibilidade ao redor. |
| **Motion Primitives** | Blocos elementares de transição construídos em Framer Motion | Copy-paste manual | Peças muito primitivas; ausência de interfaces de alta complexidade compostas prontas para produção. |
| **Animate UI** | Versões animadas dos componentes base do shadcn/ui | Registro shadcn | Escopo limitado aos componentes padrões (tabs, tooltips, dialogs); não fornece backdrops imersivos nem visualização de dados. |

### 1.4 Taxonomia do Acervo (170+ Componentes em 12 Categorias)
O acervo do Planes é organizado em 12 pilares funcionais rigorosamente catalogados:
1. **AI & Agent Interfaces**: `Thinking Loader`, `AI Prompt Composer`, `Streaming Message`, `Reasoning Trace`, `Image Generation`, `Tool Call Card`, `Agent Plan`, `AI Chat`, `Inline Diff`, `Approval Card`, `Chat Orb`, `Pixel Image Generation`.
2. **WebGL, Shaders & GPU Fields**: `Logo Flare`, `Prism`, `Wind Tunnel`, `Cloud Sea`, `Ink`, `Slipstream`, `Embers`, `Beams`, `ASCII WebGL`, `Dither Field`, `Ferrofluid`, `Cymatics`, `Caustics`, `Thin Film`, `Topography`, `Jali`, `Galaxy`, `Eclipse`, `Streaks`, `Magma`, `Warp`.
3. **Media, Bento & 3D Interactive Surfaces**: `Link Preview`, `Radial Pop-out`, `Direction-Aware Flip Card`, `Hover Reveal`, `Photo Stack`, `Hero Card Stack`, `Swipe Card Deck`, `Photo Shuffle`, `Retro Music Player`, `Album Cover`, `Apple Music Card`, `Watch Face`, `Digital Watch Face`, `Avatar Cluster`, `Photo Lightbox`, `Scroll Zoom Reveal`, `GitHub Chart`, `Dither Renderer`, `Progressive Blur`, `Hero Media Scroll-Out`, `Bento Grid`, `Shutter Gallery`, `Photo Planes`, `Polaroid Flip Card`, `Text Cylinder`, `Expanding Card`, `Curved Video Player`, `Scroll Settle Gallery`.
4. **Carousels & Elastic Navigation**: `Logo Wall`, `Marquee`, `Image Wheel`, `Image Flow Carousel`, `Arc Marquee`, `Parallax Carousel`, `Bend Carousel`, `Elastic Carousel`, `Focus Scale Carousel`, `Cover Flow`, `Lens Carousel`.
5. **Controls, Micro-Interactions & Skewed Physical Inputs**: `Copy Button`, `Segmented Control`, `Number Stepper`, `Glow Input`, `Email Capture`, `Card Stack`, `Date Picker`, `Animated Select`, `Command Palette`, `OTP Input`, `Detent Drawer`, `Notch`, `Physical Knob`, `Reaction Arc`, `Receipt Printer`, `Rubber Band Select`, `Morphing Tray`, `Keyboard`, `Infinity Canvas`, `Scratch Card`, `Multi Select`, `File Dropzone`, `Halftone Popover`, `Cookie Consent`.
6. **Physics & Generative Systems**: `Ripple Grid`, `Particle Reveal`, `Pendulum Wave`, `Rubik's Cube`, `Dotted Sphere`, `Dot Monogram`.
7. **Kinetic Typography & Text Mechanics**: `Smooth Stagger Text`, `Cinematic Text`, `Split-Flap Board`, `Liquid Headline`, `Signature Reveal`, `Rainbow Text`, `Neon Sign`, `Glitch Reveal`, `Odometer`.
8. **Structural Sections & Page Engines**: `Shader Nav`, `Shader Strip`, `Shader Rows`, `Shader Index`, `Shader Flood`, `Hover Tabs`, `Silk Card`, `Pricing Table`, `Mega Menu`, `FAQ Section`, `Integration Beams`, `Radial Hub Diagram`, `Shader Tabs`, `World Map`, `Dotted Globe`, `Activity Feed`, `Scroll Stage`, `Radar Sweep`, `Data Table`, `Integration Grid`, `Pricing Section`, `Testimonial Wall`, `Changelog Timeline`, `CTA Section`, `Logo Testimonials`, `Navbar`, `Announcement Bar`, `Logo Cloud`, `Features Grid`, `Team Section`, `Blog Section`, `Contact Section`.
9. **Halftone Dither & Modern Data-Viz**: `Shader Area`, `Shader Bars`, `Shader Stream`, `Dither Donut`, `Dither Heatmap`, `Shader Stat Tiles`, `Dither Bar List`, `Dither Gauge`, `Dither Line Chart`, `Dither Pie`.
10. **Immersive Heroes**: `Scenic Hero`, `Editorial Hero`, `Landing Hero`, `Floating Cards Hero`, `Orbit Hero`, `Gallery Wall Hero`, `SDK Hero`, `Trail Hero`, `Type Hero`, `Desk Hero`.
11. **Authentications & Logins**: `Portal Login`, `Terminal Login`, `Auth Form`.
12. **Atmospheric Footers**: `Wordmark Footer`, `Halftone Footer`, `CTA Footer`.

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

### 2.1 Projetos Arquetípicos Onde Planes é a Referência Primária
O Planes deve ser escolhido como a **Direção de Arte Primária** nas seguintes circunstâncias:
- **Plataformas de IA Generativa & Agentes Autônomos (Agentic SaaS)**: Aplicações onde o usuário precisa acompanhar em tempo real passos de raciocínio (`Reasoning Trace`), execução de chamadas de ferramentas de terminal (`Tool Call Card`), cartões de aprovação de segurança com countdown (`Approval Card`) e deltas de código (`Inline Diff`). Nenhuma outra galeria no mundo possui esse vocabulário visual com essa densidade.
- **Ferramentas de Engenharia de Precisão & DevTools**: Dashboards B2B, plataformas de observabilidade e consoles de desenvolvedores que exigem gráficos de densidade altíssima sem parecer corporativos enfadonhos (uso pioneiro dos gráficos com técnica **Bayer Ordered Dither**).
- **Hard-Tech, Audio Software & Creative Suites**: Aplicações com controles tácteis skeuomórficos contemporâneos (potenciômetros rotatórios físicos em CSS 3D com luz reagente, teclados simulados com switches físicos, sliders de fita elástica e monitores CRT de fósforo âmbar).
- **Startups High-Craft em Tailwind v4**: Projetos que buscam o nível de acabamento de estúdios de ponta como Linear, Raycast, Vercel ou Apple, mantendo compatibilidade 100% nativa com o motor de compilação CSS do Tailwind v4.

### 2.2 Ressonância Emocional e Posicionamento de Marca
- **Cultura de Engenharia Obsessiva**: Comunica que cada detalhe, cada milissegundo de atraso e cada curva de desaceleração foram medidos e lapidados. Gera respeito imediato por parte de desenvolvedores e designers seniores.
- **Calma e Controle Cibernético**: O contraste do fundo escuro profundo (`#000000`/`#09090b`) com a micro-textura de halftone e a luz incidente cria uma atmosfera de laboratório aeroespacial ou centro de comando de missão.
- **Sensação de Tangibilidade Digital**: Componentes físicos como o `Physical Knob` e o `Receipt Printer` quebram a frieza do flat design tradicional, injetando prazer tátil em tarefas digitais rotineiras.

### 2.3 Execução da Regra 60-30-10 na Filosofia Planes

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                 60-30-10 ARCHITECTURAL BALANCE (PLANES CRAFT)               │
├─────────────────────────────────────────────────────────────────────────────┤
│  60%  SUBSTRATO ESTRUTURAL & ESPAÇO SILENCIOSO (The Void Canvas)           │
│       Fundos neutros monocromáticos (#000000 a #09090b ou #ffffff a #fafafa),│
│       grid ortogonal rigoroso, ausência de ruídos ou texturas intrusivas.   │
├─────────────────────────────────────────────────────────────────────────────┤
│  30%  SUPERFÍCIES TÁTEIS & MICRO-BISEL (Precision Enclosures)               │
│       Bordas de 1px translúcidas (border-white/8), cantos generosos         │
│       (rounded-xl/2xl), backdrop-blur com desaturação leve, superfícies     │
│       de cartão com elevação suave (#111115) e texturas dither 1-ink.       │
├─────────────────────────────────────────────────────────────────────────────┤
│  10%  CINÉTICA DE ALTA TENSÃO & LUZ FÍSICA (Kinetic Soul & Glow Accents)    │
│       Molas ativas com arrasto inercial, halos WebGL volumétricos, feixes   │
│       de luz caústica, acentos funcionais (#2f6cff, #6366f1, #10b981).      │
└─────────────────────────────────────────────────────────────────────────────┘
```

- **60% da Interface (O Substrato Vazio)**: A interface respira em um ambiente austero e hiper-limpo. O fundo não compete com o raciocínio nem com os dados. Em modo escuro, utiliza o preto quase puro para maximizar o contraste de luminância dos elementos superiores.
- **30% da Interface (Enclausuramentos Táteis & Bisel)**: Cartões com cantos arredondados contínuos (*squircle style*), linhas de costura milimétricas de `1px` (`rgba(255,255,255,0.06)` a `0.10`), menus contextuais e bandejas com física de transição fluida (`layoutId`).
- **10% da Interface (Cinética de Alta Tensão & Luz Física)**: O momento estético memorável: o brilho do `Glow Input` que respira conforme o foco do usuário, as partículas de dither que se reorganizam ao passar o mouse, a expansão de um cartão que revela código fonte e a mola oscilante de um botão de ação rápida.

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

### 3.1 Incompatibilidades Arquiteturais e Setoriais
- ⚠️ **Incompatível com E-commerces Tradicionais de Massa (Fast-Fashion, Supermercados)**: A estética refinada, o vocabulário dither e as micro-molas de alta latência perceptiva podem desacelerar a conversão de usuários não acostumados a interfaces imersivas ou com conexões e hardwares de baixo custo.
- ⚠️ **Incompatível com Stacks Sem React / Next.js ou Sem Tailwind v4**: O Planes exige a semântica de `@theme` e as diretivas CSS do Tailwind v4 combinadas com o runtime do React 19. Tentar adaptá-lo para WordPress, Drupal, Vue puro ou Angular gera atrito arquitetural desnecessário.
- ⚠️ **Incompatível com Projetos Corporativos Tradicionais (Bancos Legados, Governamentais)**: Setores governamentais e corporações financeiras burocráticas frequentemente exigem conformidade estrita com padrões visuais estáticos (Material Design, Bootstrap corporativo), onde o uso de shaders WebGL ou visualizações com halftone dithering é visto com estranhamento por reguladores ou comitês de acessibilidade conservadores.

### 3.2 Armadilhas de Imitação & Anti-Padrões
- ⚠️ **Cópia Desordenada de Shaders WebGL**: Instalar múltiplos backdrops pesados (`Magma`, `Ferrofluid`, `Cymatics`) em uma única tela faz com que a GPU de notebooks e smartphones sofra throttling térmico e queda de frames para menos de 30 FPS. Cada página deve conter no máximo **um** shader ativo por viewport.
- ⚠️ **Ignorar Estados de Redução de Movimento**: O Planes implementa `prefers-reduced-motion` em todos os seus componentes nativos. Desenvolvedores que removem essa camada em nome da "estética pura" violam regras globais de acessibilidade (WCAG 2.2 AA) e provocam náusea e desconforto visual em usuários com distúrbios vestibulares.
- ⚠️ **Excesso de Esqueuomorfismo**: Combinar componentes skeuomórficos analógicos (`Physical Knob`, `CRT Terminal Login`, `Split-Flap Board`, `Receipt Printer`) em um contexto que não seja um produto deliberadamente musical, retrô ou especializado torna a interface circense e anacrônica.

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo
O Planes opera sob uma métrica milimétrica de espaçamento:
- **Grid Ortogonal Subjacente**: Baseado no sistema de escala modular de 4px/8px do Tailwind v4 (`p-1` [4px], `p-2` [8px], `p-3` [12px], `p-4` [16px], `p-6` [24px], `p-8` [32px]).
- **Micro-Linhas Divisórias de Precisão**: Em vez de sombras pesadas ou margens vazias desproporcionais, a separação espacial ocorre via `border border-white/5` ou `border-white/10`, acompanhada frequentemente de linhas pontilhadas discretas ou padrões lineares repetitivos com `bg-[repeating-linear-gradient(...)]` para criar calhas verticais e horizontais reminiscentes de pranchetas de arquitetura.
- **Máscaras de Transição no Eixo de Scroll**: Uso extensivo de máscaras de gradiente CSS no contêiner de rolagem:
  `[mask-image:linear-gradient(to_bottom,transparent,black_40px,black_calc(100%-40px),transparent)]`. Isso impede que o conteúdo seja cortado de forma dura nas extremidades dos painéis laterais e drawers.

### 4.2 Sistemas de Cores, Superfícies & Texturas
1. **Bayer Ordered Dithering (Halftone Monocromático)**: O Planes reintroduziu o dithering ordenado da computação gráfica clássica dos anos 80/90 como uma linguagem gráfica contemporânea de alta sofisticação. Em vez de degradês contínuos pesados ou gráficos SVG vetoriais convencionais, gráficos como `Dither Heatmap`, `Dither Donut` e `Dither Bar List` utilizam matrizes de dithering (geralmente Bayer 4x4 ou 8x8) desenhadas diretamente na GPU ou via Canvas 2D em uma única tinta monocromática sobre preto ou branco.
2. **Superfícies Acetinadas em Dark Mode**: Cartões modulares não são cinzas foscos neutros; utilizam uma combinação precisa de `bg-neutral-900/95` ou `bg-card`, combinada com desfoque de fundo `backdrop-blur-xl`, `backdrop-saturate-150` e uma sombra inset superior `shadow-[inset_0_1px_0_rgba(255,255,255,0.08)]` que simula a incidência de iluminação de teto sobre bordas de policarbonato polido.

---

### 4.3 Catálogo Detalhado de Componentes Emblemáticos

Abaixo, a dissecação técnica e anatômica de 10 padrões icônicos do catálogo Planes:

#### 1. `Reasoning Trace` (AI & Agent Transcript)
- **Anatomia**: Pílula colapsável contendo um indicador de pulso luminoso (indicando pensamento ativo do LLM), contador numérico de passos (`01`, `02`, `03`), badge de modelo e painel retrátil que expõe o fluxo de raciocínio passo a passo antes de colapsar automaticamente em um resumo de 1 linha quando o raciocínio é concluído.
- **Gatilho Cinético**: Ao receber chunks de streaming, novos passos deslizam verticalmente com desfoque de entrada (`filter: blur(8px) -> blur(0px)`). Ao finalizar, uma mola crítica recolhe o painel para a altura mínima sem reflow.
- **Onde Encaixar**: Interfaces de chat com modelos de raciocínio avançado (o1, o3, Claude 3.7 Sonnet Thinking, DeepSeek-R1).

#### 2. `Tool Call Card` & `Approval Card` (Agent Safety & Transcripts)
- **Anatomia**: Linha mono-espaçada estilizada representando uma invocação de ferramenta (`read_file(config.json)` ou `bash(npm install)`). Inclui ícone de status com spinner animado que se converte em check vetorizado desenhado via `pathLength`, badge de nível de risco (Low, Medium, Critical) e botões de decisão rápida (`Allow` com anel circular de contagem regressiva que pausa no hover, e `Deny` com animação de tremor horizontal elástico).
- **Gatilho Cinético**: Hover prolongado pausa o temporizador; clique em Deny dispara um feedback háptico visual (shake de 8px em -2°/2°); clique em Allow colapsa a ficha inteira em um comprovante (*receipt*) compacto de auditoria.
- **Onde Encaixar**: Consoles de agentes autônomos de código, terminais web e painéis de aprovação humana no loop (HITL - *Human in the Loop*).

#### 3. `Streaming Message` (Iridescent Frontier Inking)
- **Anatomia**: Bloco de texto de resposta do assistente que se materializa com uma borda translúcida suave como tinta se espalhando no papel. Uma micro-linha iridescente persegue a fronteira de escrita em tempo real.
- **Gatilho Cinético**: Movimento contínuo atrelado aos tokens recebidos via WebSocket/SSE. Ações secundárias (Copiar código, Regenerar, Feedback) permanecem invisíveis e desvanecem suavemente sem alterar a altura do bloco pai.
- **Onde Encaixar**: Corpo central de mensagens em chatbots e copilotos de produtividade.

#### 4. `Physical Knob` (Skeuomorphic Rotary Controller)
- **Anatomia**: Potenciômetro giratório com chanfro chanfrado em alumínio anodizado, entalhe de precisão indicador de valor, anel periférico de LEDs concêntricos e iluminação dinâmica que acompanha o ângulo do cursor.
- **Gatilho Cinético**: Arrastar com mouse ou trackpad calcula a tangente inversa do vetor (`Math.atan2`), aplicando amortecimento elástico nos extremos (0% a 100%) com resistência inercial que simula atrito mecânico.
- **Onde Encaixar**: Aplicações de áudio Web, sintetizadores, seletores de temperatura para modelos de IA e controles industriais IoT.

#### 5. `Bayer Dither Heatmap / Dither Donut` (Halftone Monochromatic Data-Viz)
- **Anatomia**: Gráficos de dispersão e anéis construídos via Canvas 2D/WebGL que mapeiam grandezas numéricas não através de paletas de arco-íris caóticas, mas pela densidade de pontos calculada por matriz de Bayer. Quanto maior o valor, mais aglomerados e compactos tornam-se os pontos de tinta.
- **Gatilho Cinético**: No estado inicial, os pontos emergem de ruído aleatório até travarem na matriz geométrica final; ao passar o cursor, um anel de destaque amplia os pontos sob a lupa e exibe tooltip de alta precisão.
- **Onde Encaixar**: Dashboards analíticos com alta densidade de informação, relatórios de observabilidade de servidores e métricas financeiras.

#### 6. `Thin Film / Cymatics / Ferrofluid` (Physics-Driven WebGL Shaders)
- **Anatomia**: Canvas de aceleração gráfica por hardware rodando fragment shaders GLSL sem dependência de Three.js ou bibliotecas externas pesadas. Simula fenômenos físicos reais: interferência de película de sabão (*Thin Film*), figuras de ressonância acústica de Chladni (*Cymatics*) ou picos magnéticos fluidos (*Ferrofluid*).
- **Gatilho Cinético**: A posição da luz e a deformação do campo seguem as coordenadas normalizadas do ponteiro do mouse (`u_mouse`). Ao clicar, ondas de choque radiais propagam-se na grade vetorial.
- **Onde Encaixar**: Fundo imersivo de Hero Sections para startups de deep-tech, ciência de materiais, áudio e computação espacial.

#### 7. `Split-Flap Board` (Mechanical Airport Departure Display)
- **Anatomia**: Painel modular de caracteres que emula fielmente os painéis eletromecânicos de estações de trem e aeroportos clássicos (Solari di Udine), com corte horizontal no meio de cada ladrilho e linha de sombra.
- **Gatilho Cinético**: A troca de texto dispara uma cascata assíncrona onde cada caractere rotaciona no eixo X em 3D (`rotateX(90deg) -> rotateX(0deg)`) percorrendo o alfabeto até travar na letra final, acompanhado de leve som ou micro-tremor de aterrissagem.
- **Onde Encaixar**: Títulos de impacto em Hero Sections, contadores de status de implantação de software e marcos de lançamento.

#### 8. `Scroll Settle Gallery` & `Hero Media Scroll-Out` (Scroll-Bound Unfolding)
- **Anatomia**: Grade de mídia alinhada em alvenaria (*masonry*) ou cartão central de produto em perspectiva isométrica inclinada (rotacionado em 3D: `rotateX(25deg) scale(0.9)`).
- **Gatilho Cinético**: O progresso da barra de rolagem (0 a 1) controla diretamente a transformação geométrica. À medida que o usuário rola, o cartão deita em direção ao plano frontal (`rotateX: 0deg, scale: 1.0`), enquanto os elementos vizinhos abrem espaço em transição suave controlada por mola inercial.
- **Onde Encaixar**: Demonstração de interface de aplicativo em páginas de conversão de SaaS.

#### 9. `Detent Drawer` & `Morphing Tray` (Velocity-Aware Elastic Sheets)
- **Anatomia**: Folhas modais de navegação inspiradas no iOS e na carteira Family, com múltiplas alturas de repouso (*detents* de 25%, 50%, 90%), barra de tração tátil (*drag handle*) e transições contínuas de altura entre etapas sucessivas.
- **Gatilho Cinético**: O arraste calcula a velocidade de saída (*release velocity*). Se a velocidade for alta na direção descendente, o drawer fecha mesmo que solto no topo; se for lenta, ele ancora na altura de repouso mais próxima. O contêiner de transição de formulário altera a largura e altura com `layoutId` e mola viva sem cortes abruptos.
- **Onde Encaixar**: Fluxos de onboarding, finalização de compra (*checkout*), seletores mobile e carteiras cripto/fintech.

#### 10. `Shader Nav` & `Mega Menu` (Continuous Surface Reshaping)
- **Anatomia**: Barra de navegação com menu suspenso onde o painel não se fecha e reabre ao alternar entre categorias; o container se estica e redimensiona organicamente para envolver as novas colunas, mantendo uma seta (*caret*) ancorada ao gatilho ativo e um cartão de shader dinâmico que reflete a paleta cromática da seção.
- **Gatilho Cinético**: Hover com tolerância de intenção direcional (*hover intent*). A transição entre abas calcula a diferença de dimensões (*bounding rect*) e interpola altura e largura com física de mola crítica.
- **Onde Encaixar**: Headers de plataformas SaaS multi-produto e portais corporativos complexos.

---

## 5. Arquitetura Técnica, Física de Movimento & Tradução para Código

### 5.1 A Tríade Tecnológica: React 19 + Tailwind v4 + Motion
O Planes adota com pioneirismo os recursos mais recentes do ecossistema frontend:
1. **React 19**: Aproveitamento de Actions assíncronas, directivas `'use client'`, transições sem travamento de UI (`useTransition`) e renderização concorrente sem bloqueio de frames.
2. **Tailwind CSS v4**: Migração completa para a arquitetura baseada no motor Lightning CSS com configuração via CSS nativo (`@theme`), sem dependência de arquivos legados `tailwind.config.js`. Definição de tokens diretos como `@theme { --font-sans: 'Geist Sans', sans-serif; }`.
3. **Motion (`motion` package / ex-Framer Motion)**: Utilização dos pacotes modernos e leves do motor Motion v11/v12, priorizando props como `layout`, `layoutId`, `AnimatePresence` e propriedades aceleradas exclusivamente por GPU (`transform`, `opacity`, `filter`).

### 5.2 Física de Movimento: As Constantes de Mola Oficiais do Planes
O Planes não utiliza transições baseadas em tempo fixo (`transition: all 0.3s ease`). Toda a cinética é governada pela equação de amortecimento de mola com as seguintes combinações arquetípicas:

```typescript
// Configurações de Mola Canônicas do Planes
export const planesSprings = {
  // 1. Mola Rápida e Decisiva (Snappy Micro-Interaction)
  // Usada em: Hovers, botões, toggles, Segmented Control
  snappy: {
    type: "spring",
    stiffness: 500,
    damping: 35,
    mass: 0.8,
  },

  // 2. Mola Orgânica com Inércia Suave (Natural Settle)
  // Usada em: Modais, Drawers, Cartões expansíveis, Command Palette
  settle: {
    type: "spring",
    stiffness: 320,
    damping: 30,
    mass: 1.0,
  },

  // 3. Mola Pesada com Preservação de Momento (Weighty Momentum)
  // Usada em: Scroll Settle Gallery, Hero Media Scroll-Out, Cover Flow
  heavy: {
    type: "spring",
    stiffness: 180,
    damping: 24,
    mass: 1.4,
  },

  // 4. Curva de Transição Exponencial para Revelações de Texto (Text Easing)
  textEase: [0.22, 1, 0.36, 1], // Equivalente ao cubic-bezier quint/expo de desaceleração suave
};
```

---

### 5.3 Tokens CSS & Layout Recipe (Tailwind CSS v4)
A receita de CSS e tokens abaixo captura a assinatura visual do Planes:

```css
@import "tailwindcss";

@theme {
  --color-canvas-black: #000000;
  --color-canvas-subtle: #09090b;
  --color-surface-card: #111115;
  --color-surface-overlay: #18181b;
  
  --color-border-subtle: rgba(255, 255, 255, 0.07);
  --color-border-hover: rgba(255, 255, 255, 0.18);
  
  --color-brand-blue: #2f6cff;
  --color-brand-indigo: #6366f1;
  --color-brand-emerald: #10b981;
  
  --font-mono: "Geist Mono", "SF Mono", monospace;
  --font-sans: "Geist Sans", "Inter", -apple-system, sans-serif;
  
  --ease-planes-out: cubic-bezier(0.22, 1, 0.36, 1);
}

/* Utilitários Customizados de Superfície Planes */
@layer utilities {
  .planes-glass-card {
    background-color: var(--color-surface-card);
    border: 1px solid var(--color-border-subtle);
    box-shadow: 
      inset 0 1px 0 rgba(255, 255, 255, 0.08),
      0 12px 32px -16px rgba(0, 0, 0, 0.7);
    border-radius: 1.25rem; /* 20px */
  }

  .planes-dither-overlay {
    background-image: repeating-linear-gradient(
      to bottom,
      var(--color-border-subtle) 0px,
      var(--color-border-subtle) 1px,
      transparent 1px,
      transparent 10px
    );
  }
}
```

---

### 5.4 Receita de Código Funcional e Realista: `ReasoningTrace` Component

Abaixo está a implementação completa e realista do componente **ReasoningTrace**, espelhando fielmente os padrões de engenharia, estado, tipagem TypeScript e animação de mola do ecossistema Planes:

```tsx
"use client";

import React, { useState } from "react";
import { motion, AnimatePresence } from "framer-motion";
import { ChevronDown, Check, Sparkles, Terminal, ArrowRight } from "lucide-react";

export interface StepItem {
  id: string;
  title: string;
  detail?: string;
  timestamp: string;
  status: "completed" | "in-progress" | "pending";
}

interface ReasoningTraceProps {
  agentName?: string;
  modelName?: string;
  totalTimeMs?: number;
  steps?: StepItem[];
}

const defaultSteps: StepItem[] = [
  {
    id: "step-1",
    title: "Analisando estrutura de componentes do repositório",
    detail: "Varredura em components.json e detecção de Tailwind CSS v4.",
    timestamp: "0.2s",
    status: "completed",
  },
  {
    id: "step-2",
    title: "Executando inferência e validação de dependências",
    detail: "Verificação de @useplanes/cli e chave de registro autenticada.",
    timestamp: "0.8s",
    status: "completed",
  },
  {
    id: "step-3",
    title: "Sintetizando árvore de layout com Motion springs",
    detail: "Interpolando constantes de stiffness=320 e damping=30.",
    timestamp: "1.4s",
    status: "in-progress",
  },
];

export function ReasoningTrace({
  agentName = "Reasoning Engine",
  modelName = "claude-3-7-sonnet",
  totalTimeMs = 1420,
  steps = defaultSteps,
}: ReasoningTraceProps) {
  const [isOpen, setIsOpen] = useState(true);
  const isFinished = steps.every((s) => s.status === "completed");

  return (
    <div className="w-full max-w-2xl font-sans text-sm selection:bg-indigo-500/30">
      {/* Contêiner Principal da Superfície */}
      <div className="relative overflow-hidden rounded-2xl border border-white/8 bg-[#0c0d10] p-3 shadow-[inset_0_1px_0_rgba(255,255,255,0.06),0_20px_40px_-20px_rgba(0,0,0,0.8)]">
        
        {/* Barra Superior de Cabeçalho / Trigger do Colapso */}
        <button
          type="button"
          onClick={() => setIsOpen(!isOpen)}
          className="flex w-full items-center justify-between gap-3 rounded-xl px-2.5 py-1.5 transition-colors hover:bg-white/4 active:scale-[0.99] focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-indigo-500/50"
          aria-expanded={isOpen}
        >
          <div className="flex items-center gap-2.5 min-w-0">
            {/* Ícone de Pulso de Pensamento ou Check Concluído */}
            <div className="relative flex size-6 shrink-0 items-center justify-center rounded-lg border border-white/10 bg-white/5">
              {isFinished ? (
                <Check className="size-3.5 text-emerald-400" />
              ) : (
                <>
                  <span className="absolute size-2 rounded-full bg-indigo-400 animate-ping opacity-60" />
                  <Sparkles className="size-3.5 text-indigo-400" />
                </>
              )}
            </div>

            {/* Título e Badge de Modelo */}
            <div className="flex items-center gap-2 truncate">
              <span className="font-medium text-white/90 truncate">{agentName}</span>
              <span className="rounded-md border border-white/6 bg-white/3 px-1.5 py-0.5 font-mono text-[11px] text-white/50">
                {modelName}
              </span>
            </div>
          </div>

          <div className="flex items-center gap-3 shrink-0">
            {/* Duração em Milissegundos com Tipografia Monospaçada */}
            <span className="font-mono text-xs tabular-nums text-white/40">
              {(totalTimeMs / 1000).toFixed(1)}s
            </span>

            {/* Indicador Rotativo de Chevron com Mola Snappy */}
            <motion.div
              animate={{ rotate: isOpen ? 180 : 0 }}
              transition={{ type: "spring", stiffness: 450, damping: 30 }}
            >
              <ChevronDown className="size-4 text-white/40" />
            </motion.div>
          </div>
        </button>

        {/* Painel Expansível de Raciocínio (Passo a Passo) */}
        <AnimatePresence initial={false}>
          {isOpen && (
            <motion.div
              key="content"
              initial={{ height: 0, opacity: 0 }}
              animate={{ height: "auto", opacity: 1 }}
              exit={{ height: 0, opacity: 0 }}
              transition={{
                height: { type: "spring", stiffness: 320, damping: 30 },
                opacity: { duration: 0.2 },
              }}
              className="overflow-hidden"
            >
              <div className="relative mt-2 border-t border-white/6 pt-3 px-2">
                {/* Linha Guia Vertical do Trilho (Rail) */}
                <div className="absolute bottom-6 left-[1.375rem] top-6 w-px bg-white/6" />

                <div className="space-y-4">
                  {steps.map((step, idx) => {
                    const isStepCompleted = step.status === "completed";
                    const isStepActive = step.status === "in-progress";

                    return (
                      <motion.div
                        key={step.id}
                        initial={{ opacity: 0, y: 8, filter: "blur(4px)" }}
                        animate={{ opacity: 1, y: 0, filter: "blur(0px)" }}
                        transition={{
                          delay: idx * 0.08,
                          duration: 0.35,
                          ease: [0.22, 1, 0.36, 1],
                        }}
                        className="relative flex items-start gap-3.5 pl-1"
                      >
                        {/* Marcador Numérico do Passo */}
                        <div
                          className={`relative z-10 flex size-5 shrink-0 items-center justify-center rounded-full border text-[10px] font-mono font-medium transition-colors ${
                            isStepCompleted
                              ? "border-emerald-500/40 bg-emerald-950/60 text-emerald-400"
                              : isStepActive
                              ? "border-indigo-500/50 bg-indigo-950/80 text-indigo-300 ring-2 ring-indigo-500/20"
                              : "border-white/10 bg-white/5 text-white/30"
                          }`}
                        >
                          {isStepCompleted ? (
                            <Check className="size-2.5" />
                          ) : (
                            <span>{idx + 1}</span>
                          )}
                        </div>

                        {/* Conteúdo Textual do Passo */}
                        <div className="flex-1 min-w-0 -mt-0.5">
                          <div className="flex items-center justify-between gap-2">
                            <h4
                              className={`text-[13px] font-medium leading-5 ${
                                isStepActive
                                  ? "text-white"
                                  : isStepCompleted
                                  ? "text-white/80"
                                  : "text-white/40"
                              }`}
                            >
                              {step.title}
                            </h4>
                            <span className="font-mono text-[11px] text-white/30 shrink-0">
                              {step.timestamp}
                            </span>
                          </div>

                          {step.detail && (
                            <p className="mt-0.5 text-xs text-white/50 leading-relaxed font-mono">
                              {step.detail}
                            </p>
                          )}
                        </div>
                      </motion.div>
                    );
                  })}
                </div>

                {/* Rodapé Interno com Comprovante de Conclusão */}
                <div className="mt-4 flex items-center justify-between rounded-lg border border-white/4 bg-white/2 px-3 py-2 text-[11px] text-white/40">
                  <div className="flex items-center gap-1.5 font-mono">
                    <Terminal className="size-3 text-indigo-400/70" />
                    <span>Pipeline validado sem exceções</span>
                  </div>
                  <span className="text-[10px] uppercase tracking-wider font-semibold text-emerald-400/80">
                    Trace Ready
                  </span>
                </div>
              </div>
            </motion.div>
          )}
        </AnimatePresence>
      </div>
    </div>
  );
}
```

---

### 5.5 Como a IA Deve Pesquisar ao Vivo no Useplanes
Quando o agente precisar inspecionar componentes e baixar código-fonte diretamente do repositório remoto do Planes, deve seguir esta estrutura oficial de URLs e comandos:

1. **Estrutura de Categorias e Rotas Oficiais**:
   - Catálogo Geral: `https://www.useplanes.com/components`
   - Componente Individual: `https://www.useplanes.com/components/<slug>` (ex: `/components/reasoning-trace`, `/components/physical-knob`, `/components/auth-form`)
   - Seções de Topo: `/components/heroes`, `/components/logins`, `/components/footers`, `/components/charts`, `/components/physics`
   - Comparativo Oficial: `https://www.useplanes.com/compare`
   - Documentação de Integração de Agentes (MCP): `https://www.useplanes.com/components/mcp`
2. **Obtenção de Documentação em Formato Markdown Limpo**:
   - Qualquer rota no site responde com Markdown limpo e sem poluição de tags HTML se a requisição for feita com o header `Accept: text/markdown`.
   - O índice integral de todos os 170 componentes estruturado para LLMs está disponível permanentemente em `https://www.useplanes.com/llms.txt` (índice compacto) e `https://www.useplanes.com/llms-full.txt` (referência completa de props e código).
3. **Instalação Programática no Terminal**:
   - Componentes Gratuitos (sem conta necessária):
     `npx shadcn add https://useplanes.com/r/<slug>.json`
     (Ex: `segmented-control`, `cover-flow`, `otp-input`, `ripple-grid`, `pendulum-wave`, `smooth-stagger-text`, `cinematic-text`, `scroll-stage`, `number-stepper`, `thinking-loader`).
   - Componentes Pro (autenticados via chave de licença vitalícia):
     `npx @useplanes/cli init --key YOUR_KEY`
     `npx shadcn add @useplanes/<slug>`

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao transpor a identidade do Planes para um plano arquitetural de interface (`DESIGN_BLUEPRINT.md`), adote os seguintes mandamentos e listas de conferência:

### 6.1 Regras de Ouro de Execução
1. **Física Contínua, Sem Saltos Bruscos**: Substitua qualquer animação baseada em `transition: all 0.2s` por molas da família `planesSprings` parametrizadas com `stiffness` e `damping`. O movimento deve permitir interrupção a meio voo (*interruptible animations*).
2. **Substrato Minimalista + Luz Direcional de 1px**: Aplique fundos quase pretos (`#000000` ou `#09090b`) contrastados com linhas de corte milimétricas de `1px` com baixa opacidade (`rgba(255,255,255,0.06)` a `0.10`). Jamais use bordas grossas ou cores saturadas nas molduras.
3. **Halftone Dither como Alternativa a Gradientes Pesados**: Em gráficos e dashboards analíticos, priorize o padrão Bayer Ordered Dither em uma única tinta monocromática para comunicar sofisticação técnica e densidade científica.
4. **Isolamento de Carga GPU para Shaders**: Nunca renderize mais de um shader WebGL simultaneamente no mesmo viewport visível. Adicione observadores de interseção (`IntersectionObserver`) para pausar a execução do loop `requestAnimationFrame` do shader quando o componente rolar para fora da tela.

### 6.2 Checklist de Verificação de Qualidade ("Planes-Grade UI")
- [ ] O componente respeita rigorosamente `@media (prefers-reduced-motion: reduce)`?
- [ ] Os diálogos, modais e tooltips fecham sem deixar o layout dar saltos de reflow (*zero CLS*)?
- [ ] A tipografia mono-espaçada é empregada exclusivamente para dados analíticos, passos de processo, métricas e timestamps (`tabular-nums`)?
- [ ] O código-fonte foi injetado de forma modular no repositório, sem dependências opacas externas além de `motion` e `lucide-react`?
- [ ] A interação possui feedback táctil perceptível mesmo antes de uma ação de rede se concretizar (otimismo de interface com retorno elástico)?
