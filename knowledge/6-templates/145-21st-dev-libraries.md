---
id: "145-21st-dev-libraries"
name: "21st.dev Community Libraries"
url: "https://21st.dev/community/libraries"
category: "6-templates"
schema_type: "C-galleries"
dna_estetico: ["The npm for Design Engineers", "shadcn/ui Component Paradigm", "Copy-Paste Code Ownership", "Kinetic Micro-Interactions (Framer Motion)", "Bento Grid Modularity & Glowing Bevels", "Dark Craft & Linear-Inspired Minimalism", "AI Coding Agent Native (MCP & ARD)"]
densidade_informacao: "Alta/Utilitaria"
impacto_visual: "Editorial/Sofisticado"
custo_computacional: "Medio (Tailwind + CSS Transforms) a Alto (WebGL Shaders, Canvas Particles & Motion Springs)"
stack_frameworks: ["React", "Next.js", "Tailwind CSS", "Framer Motion / Motion.dev", "Radix UI Primitives", "shadcn/ui CLI", "@21st-dev/cli", "Lucide React", "Three.js / Canvas WebGL"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "General Sans", "Plus Jakarta Sans", "Satoshi", "JetBrains Mono (Tokens & Code)", "Cal Sans"]
  paletas_ideais:
    - "Dark Craft Canvas: #09090b (Fundo Primário), #18181b (Superfície Neutra), #27272a (Borda Sutil 1px), #fafafa (Tipografia Pura)"
    - "Luminescent Glow Accents: #6366f1 (Indigo Accent), #38bdf8 (Sky Beam), #a855f7 (Purple Haze), #10b981 (Emerald Ping)"
    - "Micro-Bordas Biseladas: rgba(255, 255, 255, 0.08) em dark mode / rgba(0, 0, 0, 0.08) em light mode"
    - "Pure Light Minimalist: #ffffff (Canvas Imaculado), #f4f4f5 (Card Muted), #e4e4e7 (Borda Refinada), #09090b (Ink)"
  combinacoes_recomendadas:
    - "shadcn/ui CLI + @21st-dev/cli para injeção atômica de código-fonte diretamente na árvore do projeto (/components/ui)"
    - "Motion.dev (Framer Motion v11/v12) com molas calibradas (stiffness: 300, damping: 25) para interações de micro-resposta sem latência"
    - "Radix UI Primitives (Dialog, DropdownMenu, Tooltip, Popover) para assegurar conformidade total com WAI-ARIA sem abrir mão de estilização customizada"
    - "tailwind-merge + clsx (utilitário cn()) para concatenação atômica de classes e resolução determinística de especificidade CSS"
    - "Lucide React + Lucide Animated para iconografia consistente e microinterações vetoriais cinéticas sob hover"
  conflitos_esteticos:
    - "Acúmulo desmedido de shaders e efeitos decorativos simultâneos (Spotlight + Aurora + Meteors + Marquee na mesma viewport), provocando colapso de legibilidade e sobrecarga de GPU"
    - "Mistura desregrada de raios de curvatura (rounded-none com rounded-3xl sem hierarquia de encapsulamento)"
    - "Bordas sólidas espessas (>1.5px) em cores saturadas, que destroem o acabamento milimétrico de 1px biselado"
    - "Ignorar a mídia de acessibilidade prefers-reduced-motion em animações contínuas ou de deslocamento espacial"
    - "Dependência de pacotes npm fechados para estilizações triviais, desvirtuando a premissa de posse total do código-fonte"
---

# 21st.dev Community Libraries — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
 ██████╗  ██╗███████╗████████╗    ██████╗ ███████╗██╗   ██╗    ██╗     ██╗██████╗ ██████╗  █████╗ ██████╗ ██╗███████╗███████╗
╚════██╗███║██╔════╝╚══██╔══╝    ██╔══██╗██╔════╝██║   ██║    ██║     ██║██╔══██╗██╔══██╗██╔══██╗██╔══██╗██║██╔════╝██╔════╝
 █████╔╝╚██║███████╗   ██║       ██║  ██║█████╗  ██║   ██║    ██║     ██║██████╔╝██████╔╝███████║██████╔╝██║█████╗  ███████╗
██╔═══╝  ██║╚════██║   ██║       ██║  ██║██╔══╝  ╚██╗ ██╔╝    ██║     ██║██╔══██╗██╔══██╗██╔══██║██╔══██╗██║██╔══╝  ╚════██║
███████╗ ██║███████║   ██║       ██████╔╝███████╗ ╚████╔╝     ███████╗██║██████╔╝██║  ██║██║  ██║██║  ██║██║███████╗███████║
╚══════╝ ╚═╝╚══════╝   ╚═╝       ╚═════╝ ╚══════╝  ╚═══╝      ╚══════╝╚═╝╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝╚══════╝╚══════╝
```

---

## 1. Identidade Visual & O Que Torna Único (Assinatura)

### 1.1 O Que é o 21st.dev e a Revolução do "Design Engineer"
O **21st.dev** (`https://21st.dev` e seu diretório central `https://21st.dev/community/libraries`) consolidou-se na indústria global de desenvolvimento frontend como o **"npm for design engineers"** (o gerenciador de pacotes da era dos engenheiros de design). Criado e mantido pelos engenheiros e fundadores **Serafim Korablev** (CEO, ex-Via Protocol e Gas Pump) e **Sergey Bunas** (CTO, com histórico de liderança em sistemas de design na Deel), o ecossistema foi acelerado pela prestigiada aceleradora **Y Combinator (Batch W26)** e transformou radicalmente a distribuição de componentes modernos para a web.

Historicamente, o desenvolvimento web viveu sob a tirania do modelo NPM clássico: componentes empacotados em bibliotecas monolíticas fechadas, distribuídas como arquivos compilados dentro de `node_modules`. Esse modelo gerava atritos severos de customização, sobrecarga de dependências órfãs e impotência estética quando o design exigia alterações finas de animação ou estilização. Inspirado na mudança sísmica iniciada por Guillermo Rauch e shadcn com o `shadcn/ui`, o **21st.dev** levou essa filosofia à sua potência máxima:
1. **Posse Total do Código (Code Ownership First)**: Em vez de instalar um pacote fechado, o desenvolvedor ou agente copia o código-fonte `.tsx` puro ou o injeta diretamente na árvore do seu repositório local (`/components/ui/...`).
2. **Engenharia de Movimento de Elite (Kinetic Craft)**: A curadoria é estruturada sobre a tríade de ouro do design moderno: **Tailwind CSS**, **Framer Motion / Motion.dev** e **Radix UI Primitives**.
3. **Agregação Descentralizada de Criadores Independentes**: O 21st.dev reúne sob uma mesma taxonomia rigorosa mais de **166 bibliotecas completas de componentes**, incluindo potências visuais como **Aceternity UI** (Manu Arora), **Magic UI** (Dillion Verma), **Kokonut UI** (Dorian Baffier), **Motion Primitives** (Julien Thibeaut / ibelick), **Origin UI**, **Ruixen UI**, **Fancy Components** (Daniel Petho), **HextaUI**, **cult ui**, **Agent Elements** e **Dub**.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        O ECOSSISTEMA 21ST.DEV & REGISTRY MODERNO                       │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  [ Comunidade de Criadores & Studios ]                                                │
│   • Aceternity UI    • Magic UI         • Motion Primitives   • Kokonut UI             │
│   • Origin UI        • Ruixen UI        • Fancy Components    • Vercel AI Elements     │
│                     │                                                                  │
│                     ▼                                                                  │
│  [ 21st.dev Core Registry Engine ]                                                     │
│   • 166+ Bibliotecas Catalogadas        • 12.000+ Componentes Atômicos                 │
│   • Live Interactive Sandboxes          • Categorias por Intenção & "Vibe"             │
│   • Open Registry Endpoints             • Validação de Tipagem TypeScript Rigorosa    │
│                     │                                                                  │
│                     ├───────────────────────────────┬──────────────────────────────────┤
│                     ▼                               ▼                                  ▼
│      [ shadcn CLI Direct Add ]        [ @21st-dev/cli CLI ]           [ 21st MCP Engine ]     │
│      npx shadcn@latest add ...        21st add <author>/<slug>        Cursor / Claude Code    │
│                     │                               │                                  │
│                     └───────────────────────────────┴──────────────────────────────────┘
│                                                     │
│                                                     ▼
│                             [ Seu Repositório Local / Production Code ]                │
│                              • src/components/ui/*.tsx (100% editável)                 │
│                              • Zero lock-in de dependências monolíticas                │
│                              • Aceleração nativa via Tailwind CSS & Framer Motion     │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.2 A Arquitetura Nativa para Agentes de IA (AI Coding Native & MCP)
O elemento mais disruptivo do 21st.dev frente a qualquer galeria convencional é a sua arquitetura voltada para **AI Agents**. O 21st.dev não é apenas uma vitrine visual para humanos; ele é desenhado como infraestrutura de catálogo legível por máquinas:
- **Model Context Protocol (MCP)**: Fornece um servidor MCP em tempo real (`https://21st.dev/api/mcp`) que permite a agentes como Cursor, Claude Code, Windsurf e Copilot pesquisar semanticamente no acervo de mais de 12.000 componentes e injetar blocos de código com zero alucinação de sintaxe.
- **Agent Resource Discovery (ARD)**: Implementa o padrão `/.well-known/ard.json` e documentação de alto nível em `/llms.txt`, além de permitir que qualquer página do diretório retorne Markdown semântico puro através de headers HTTP `Accept: text/markdown` ou do sufixo `.md`.
- **Dualidade Visual + Código**: Todo componente possui pré-visualização interativa ao vivo em canvas isolado, botão de cópia instantânea de código TypeScript/Tailwind e link direto para o registry do shadcn CLI.

---

## 2. Cenários Ideais de Aplicação (Quando Usar + Papel na Regra 60-30-10)

### 2.1 Cenários de Aplicação Primária
O acervo do **21st.dev Community Libraries** deve ser a referência visual e técnica obrigatória nos seguintes cenários:
1. **SaaS B2B de Alta Performance & Produtos de IA**: Produtos que necessitam de uma atmosfera tecnológica madura, moderna e polida (inspirada em interfaces como Linear, Vercel, Supabase, Raycast e OpenAI).
2. **Landing Pages de Conversão Tecnológica**: Páginas que precisam cativar o visitante nos primeiros 5 segundos através de heros interativos com feixes de luz direcionais (*Spotlight*, *Animated Beams*, *Aurora Backgrounds*), grades bento modulares e provas sociais dinâmicas.
3. **Cockpits e Dashboards Analíticos Complexos**: Plataformas com alta densidade de métricas, filtros dinâmicos, alternadores de abas segmentadas elásticas, gráficos modernos e tabelas expansíveis.
4. **Interfaces Conversacionais com Agentes de IA (LLM Chats)**: Aplicações que integram chat streams, cards de invocação de ferramentas (tool calling indicators), balões de pensamento com disclosure progressivo e inputs flutuantes táteis.
5. **Portfólios de Engenharia de Software e Design Craft**: Espaços onde o criador precisa demonstrar domínio impecável de microinterações, transições de estado fluidas e acabamento visual de alto padrão.

### 2.2 Papel na Regra 60-30-10 de Design Visual & Movimento
As bibliotecas reunidas no 21st.dev operam sob uma disciplina rígida de distribuição de peso visual para evitar o caos estético:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                   A REGRA 60-30-10 NAS BIBLIOTECAS DO 21ST.DEV                         │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  60%  SUBSTRATO ESTRUTURAL & ESPAÇO RESPIRÁVEL (The Architectural Substrate)          │
│       • Telas de fundo neutro profundo (#09090b no dark mode / #ffffff no light mode)  │
│       • Grid ortogonal de alta precisão (divisões modulares em 4px / 8px / 16px)      │
│       • Tipografia Grotesca funcional e sem floreios (Geist Sans, Inter, General Sans) │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  30%  SUPERFÍCIES TÁTEIS & MICRO-BISEL (Tactile Surfaces & Bento Cards)               │
│       • Cartões com cantos superelípticos consistentes (rounded-xl / rounded-2xl)      │
│       • Divisórias e bordas ultrafinas de 1px com transparência (border-border/60)    │
│       • Fundos ligeiramente elevados com desfoque de vidro (bg-card/30 backdrop-blur) │
│       • Badges de status monocromáticas e botões secundários com superfícies foscas   │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  10%  O TOQUE CINÉTICO DE ASSINATURA (Kinetic Signatures & Luminescent Accents)       │
│       • Feixes luminosos com gradiente cônico ou radial (Animated Beams, Spotlights)  │
│       • Bordas animadas por gradientes móveis (Glowing Border, Shimmering Gradient)   │
│       • Efeitos de hover com molas físicas amortecidas (stiffness: 300, damping: 25)   │
│       • Microinterações em ícones vetoriais (Lucide Animated) e cursores contextuais  │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

- **60% da Interface (Substrato Silencioso)**: Fundos neutros sem padrões agressivos. No modo escuro, utiliza tons de carvão e obsidiana (`#09090b`, `#0c0c0e`), permitindo que a hierarquia de texto e o espaço negativo garantam conforto visual prolongado.
- **30% da Interface (Superfícies Táteis & Estrutura Modular)**: Organização do conteúdo em blocos do tipo Bento Grid com bordas de `1px` sutis (`rgba(255, 255, 255, 0.08)`), fundos com preenchimento semitransparente e modais com desfoque de fundo (`backdrop-blur-md`).
- **10% da Interface (Assinatura Cinética & Acentos de Cor)**: Efeitos luminosos concentrados em pontos focais estratégicos (como o botão de ação primária, o destaque de um cartão de preços ou o feixe conectivo entre nós de uma integração técnica). Nunca espalhado de forma homogênea pela tela.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar / Anti-padrões)

### 3.1 Incompatibilidade Setorial e Técnica
- ⚠️ **Sistemas Legados e Ambientes Corporativos de Baixa Largura de Banda**: Aplicações destinadas a redes governamentais ou intranets restritas com hardware defasado sofrerão com múltiplos canvas WebGL ou dezenas de instâncias de Framer Motion rodando simultaneamente.
- ⚠️ **Aplicações com Políticas de Segurança Extremas (CSP Hiper-Restritivas)**: Ambientes que proíbem estritamente a execução de scripts embutidos dinâmicos, WebGL shaders (`new Function`/eval em pipelines GLSL) ou estilos injetados via runtime de CSS-in-JS.
- ⚠️ **Estéticas Brutalistas Radicais ou Anti-Design**: O ecossistema 21st.dev respira a sofisticação, precisão milimétrica e harmonia do design system moderno de São Francisco / Silicon Valley. Tentar aplicá-lo em projetos que demandam brutalismo cru, layouts caóticos intencionais ou tipografia experimental ilegível destrói a identidade da proposta.
- ⚠️ **Interfaces Voltadas a Acessibilidade Extrema (Setor Público / Saúde)**: Alguns componentes com efeitos puramente visuais (como textos com reflexos cintilantes, distorções de lente ou cursores magnéticos personalizados) violam padrões estritos se não receberem camadas redundantes de acessibilidade.

### 3.2 Anti-Padrões & Armadilhas de Imitação
1. **O Efeito "Parque de Diversões de Shaders" (Over-animation Syndrome)**:
   - *O Erro*: Incluir simultaneamente em uma mesma dobra de Hero: um fundo de Aurora com WebGL, um feixe de luz que segue o cursor (*Spotlight*), partículas de poeira (*Sparkles*), um cartão com borda cintilante (*Border Beam*) e textos com efeito de digitação mecânica.
   - *A Consequência*: A taxa de quadros (FPS) despenca de 60/120fps para menos de 30fps em notebooks convencionais e smartphones; a atenção do usuário é fragmentada e a taxa de conversão cai abruptamente.
   - *A Regra de Ouro*: Escolha **no máximo UM efeito volumétrico primário** por viewport (ex: Spotlight no Hero) e reserve apenas microinterações silenciosas para os controles interativos.
2. **Quebra da Hierarquia de Ação**:
   - Botões secundários ou badges informativas estilizadas com animações cintilantes competem visualmente com o botão de Call to Action (CTA) primário, gerando paralisia decisória no usuário.
3. **Ausência de Suporte a `prefers-reduced-motion`**:
   - É inaceitável implementar molas e transformações espaciais contínuas sem verificar a preferência do sistema operacional do usuário. Todo componente importado deve incorporar `useReducedMotion()` ou a diretiva Tailwind `motion-reduce:transition-none`.
4. **Ignorar o Box Model e Semântica de Foco**:
   - Remover as classes de `focus-visible:ring` nativas do Radix/shadcn para "limpar" o visual resulta em componentes inavegáveis por teclado, destruindo a usabilidade para usuários com deficiência motora.

---

## 4. Catálogo Detalhado de Componentes, Padrões & Efeitos Notáveis

### 4.1 Anatomia Estrutural: Grid, Ritmo, Superfícies & Cores
A anatomia que unifica as 166 bibliotecas do 21st.dev baseia-se em parâmetros milimétricos:
- **Espaçamento e Ritmo**: Escala modular estrita baseada em múltiplos de 4px (`gap-3` = 12px, `gap-4` = 16px, `gap-6` = 24px, `p-6` a `p-8` em cards de destaque).
- **Tratamento de Bordas (Micro-Bisel)**: Borda com espessura de `1px` utilizando classes como `border border-border/60` ou `ring-1 ring-white/10`. Em cantos arredondados, a preferência é por superelipses contínuas (`rounded-xl` a `rounded-2xl`).
- **Elevação Tátil**: A profundidade não provém de sombras difusas e pesadas dos anos 2010, mas de sobreposições sutis com desfoque de fundo (`bg-card/40 backdrop-blur-md`) e iluminação direcional suave.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        ANATOMIA DE UM BENTO CARD (21ST.DEV STYLE)                      │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  ┌──────────────────────────────────────────────────────────────────────────────────┐  │
│  │ [ Micro-Borda: 1px border-border/60 com Gradiente Alfa no Topo ]                 │  │
│  │                                                                                  │  │
│  │  [ Icon Container ]     [ Status Badge Monocromática ]                           │  │
│  │   • rounded-lg           • rounded-full                                          │  │
│  │   • bg-foreground/5      • text-xs px-2 py-0.5 font-mono                         │  │
│  │                                                                                  │  │
│  │  Título do Card (font-sans font-medium text-foreground tracking-tight)           │  │
│  │  Descrição concisa com line-clamp-2 (text-muted-foreground text-sm)              │  │
│  │                                                                                  │  │
│  │  [ Interactive Showcase Canvas / Micro-Visualizer ]                              │  │
│  │   • Gráfico SVG / Animated Beam / Switch Dinâmico / Preview Interativo           │  │
│  │                                                                                  │  │
│  │  [ Rodapé Técnico Tabular: Métricas em Monospace + Ação com Arrow Hover ]        │  │
│  └──────────────────────────────────────────────────────────────────────────────────┘  │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

### 4.2 Catálogo dos 10 Arquétipos Notáveis Catalogados no 21st.dev

Abaixo estão desconstruídos os 10 componentes e padrões mais influentes presentes nas bibliotecas comunitárias da plataforma:

#### 1. Aceternity UI: Spotlight Hero & Glowing Border Card
- **Criador Original**: Manu Arora (`@manuarora700`)
- **Biblioteca**: `aceternity-ui` (89 componentes, mais de 22M de visualizações no catálogo)
- **Anatomia Técnica**: Utiliza um elemento radial dinâmico com coordenadas X/Y vinculadas aos eventos de `onMouseMove` do container pai. Uma máscara elíptica em CSS (`radial-gradient(600px circle at ${mouseX}px ${mouseY}px, rgba(255,255,255,0.06), transparent 80%)`) ilumina a superfície do card apenas onde o cursor transita, revelando a micro-borda biselada de 1px.
- **Gatilho / Trigger**: `onMouseMove` e `onMouseLeave` com amortecimento linear em requestAnimationFrame.
- **Onde Encaixar**: Hero sections e cartões principais da grade de recursos (Bento Grid).

#### 2. Magic UI: Animated Beam & Interactive Bento Grid
- **Criador Original**: Dillion Verma (`@dillionverma`)
- **Biblioteca**: `magic-ui` (64 componentes, 6.9M visualizações)
- **Anatomia Técnica**: Caminho vetorial SVG (`<path>`) interligando dois nós DOM com coordenadas calculadas via `getBoundingClientRect()`. Um gradiente linear em movimento (`<linearGradient>`) com tags `stop` animadas simula um pacote de dados ou pulso de energia fluindo de um ponto A (ex: logo da aplicação) para um ponto B (ex: banco de dados).
- **Gatilho / Trigger**: Loop contínuo otimizado com Framer Motion (`animate={{ x1: ["0%", "100%"] }}`) ou acionado por evento de hover.
- **Onde Encaixar**: Seções de integrações, arquitetura de sistemas e demonstração de pipelines de API.

#### 3. Kokonut UI: Dynamic Island & Smooth Action Dock
- **Criador Original**: Dorian Baffier (`@kokonutd`)
- **Biblioteca**: `kokonut-ui` (60 componentes, 14M visualizações)
- **Anatomia Técnica**: Um container flutuante centralizado horizontalmente no topo ou na base da tela, utilizando a propriedade `layout` do Framer Motion. Quando o estado muda (ex: notificação de upload, player de áudio ou chamada de comando), o elemento expande sua largura e altura através de uma física de mola elástica sem solavancos de renderização.
- **Gatilho / Trigger**: Mudanças de estado de aplicação (mensagens de sucesso, alertas, atalhos de teclado).
- **Onde Encaixar**: Barra de status flutuante, feedback de ações globais ou barra de ferramentas contextuais.

#### 4. Motion Primitives: Expandable Morphing Card / Fluid Dialog
- **Criador Original**: Julien Thibeaut (`@ibelick`)
- **Biblioteca**: `motion-primitives` (39 componentes, 3.7M visualizações)
- **Anatomia Técnica**: Utiliza o poder do atributo `layoutId` do Framer Motion para conectar um cartão compacto na grade com um diálogo em modal expandido em tela cheia. O título, a imagem de capa e o container morphing mantêm continuidade visual absoluta sem corte seco de renderização.
- **Gatilho / Trigger**: Clique do usuário (`onClick`) com transição elástica desacelerada.
- **Onde Encaixar**: Mostruários de portfólio, cards de estudos de caso e detalhes de planos de assinatura.

#### 5. Origin UI: Micro-Interactive Inputs & Password Strength Bar
- **Criador Original**: Origin UI Core Team (`@originui`)
- **Biblioteca**: `origin-ui` (44 componentes, 3.8M visualizações)
- **Anatomia Técnica**: Inputs construídos sobre primitivas do Radix UI com indicadores visuais integrados: botão embutido de revelação de senha com transição de ícone de olho, medidor de entropia de senha dividido em 4 segmentos com cores progressivas (do vermelho ao verde esmeralda) e labels flutuantes com micro-deslocamento.
- **Gatilho / Trigger**: Eventos `onChange`, `onFocus` e validações de regex em tempo real.
- **Onde Encaixar**: Telas de onboarding, modais de autenticação e formulários de cadastro de novos usuários.

#### 6. Ruixen UI: High-Conversion Marketing Blocks & Testimonial Marquee
- **Criador Original**: Ruixen UI Team (`@ruixen.ui`)
- **Biblioteca**: `ruixen-ui` (347 componentes, 11M visualizações)
- **Anatomia Técnica**: Grade contínua de cartões de depoimentos com rolagem horizontal infinita através de animação CSS pura (`transform: translateX(...)`) com aceleração de hardware. Possui máscaras lineares de gradiente nas bordas laterais (`mask-image: linear-gradient(to right, transparent, black 15%, black 85%, transparent)`) para garantir fade out suave nas bordas da tela.
- **Gatilho / Trigger**: Rolagem automática contínua que pausa suavemente quando o cursor passa por cima (`hover:[animation-play-state:paused]`).
- **Onde Encaixar**: Seções de prova social (Social Proof) e logos de clientes em páginas de lançamento.

#### 7. Fancy Components: Magnetic Physics Velocity Button & Letter Glitch
- **Criador Original**: Daniel Petho (`@danielpetho`)
- **Biblioteca**: `fancy-components` (35 componentes, 4.2M visualizações)
- **Anatomia Técnica**: Botão magnético que calcula a distância vetorial entre o cursor e o centro do elemento (`useMotionValue`). Quando o cursor se aproxima a um raio de 100px, o botão é suavemente "atraído" pelo cursor através de molas acopladas (`useSpring(..., { stiffness: 150, damping: 15 })`), retornando à posição neutra com inércia amortecida ao sair.
- **Gatilho / Trigger**: Movimento livre do ponteiro do mouse na vizinhança do botão.
- **Onde Encaixar**: Botão principal de Call to Action (CTA) no Hero ou no rodapé final da página.

#### 8. Agent Elements / Vercel AI Elements: Multi-Turn LLM Reasoning Pill
- **Criador Original**: Vercel & 21st Team (`@21st/library/agent-elements` e `@vercel/library/ai-elements`)
- **Biblioteca**: `agent-elements` (2.8M visualizações)
- **Anatomia Técnica**: Componente de feedback para fluxos de IA generativa. Apresenta uma pílula compacta com efeito de brilho pulsante (*Shimmer Glow*) indicando o raciocínio do modelo ("Pensando...", "Buscando na Web..."). Ao ser clicada, expande suavemente um acordeão com a árvore de pensamento e ferramentas invocadas com syntax highlight em tempo real.
- **Gatilho / Trigger**: Eventos de streaming de dados SSE (Server-Sent Events) ou cliques no cabeçalho de raciocínio.
- **Onde Encaixar**: Chatbots inteligentes, copilotos integrados a produtos SaaS e interfaces de geração de código.

#### 9. 8bitcn / Neobrutalism: Retro Pixelated High-Contrast Blocks
- **Criador Original**: Ekmas (`@ekmas`) e TheOrcDev (`@theorcdev`)
- **Biblioteca**: `8bitcn` e `neobrutalism` (3M visualizações somadas)
- **Anatomia Técnica**: Adaptação do modelo shadcn para a estética retrô de 8 bits e neobrutalismo moderno. Apresenta bordas sólidas pretas de 2px a 3px com sombras duras de deslocamento fixo (`box-shadow: 4px 4px 0px #000`), sem arredondamento de cantos e com microinteração de clique que simula o afundamento mecânico do botão (`active:translate-x-1 active:translate-y-1 active:shadow-none`).
- **Gatilho / Trigger**: Eventos de clique `onMouseDown` / `onMouseUp` e foco via teclado.
- **Onde Encaixar**: Produtos voltados para comunidades de desenvolvedores, jogos web3 e landing pages irreverentes.

#### 10. Lucide Animated: Physics-Based Micro-Hover Vector Icons
- **Criador Original**: Pqoqubbw (`@pqoqubbw`)
- **Biblioteca**: `lucide-animated` (1.8M visualizações)
- **Anatomia Técnica**: Reescrita dos ícones vetoriais da biblioteca Lucide com caminhos controlados individualmente via Framer Motion. Ao passar o mouse sobre o ícone de sino, a cúpula balança com amortecimento pendular e o badalo vibra; no ícone de busca, a lente faz uma varredura orbital; no ícone de configurações, a engrenagem gira 90 graus com desaceleração exponencial.
- **Gatilho / Trigger**: Evento `onMouseEnter` sobre o botão ou card que hospeda o ícone.
- **Onde Encaixar**: Barras de navegação primárias, menus laterais e cabeçalhos de cartões interativos.

---

## 5. Arquitetura Técnica, Física de Movimento & Receita de Código Funcional

### 5.1 Parâmetros de Física de Movimento do Ecossistema 21st.dev
Diferente de frameworks tradicionais que utilizam transições baseadas em tempo e curvas bezier lineares duras, o ecossistema 21st.dev padronizou o uso de **física de molas amortecidas (Spring Physics)** do Framer Motion e curvas cúbicas de aceleração zero na saída:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                      PRESETS DE FÍSICA & TIMING DO 21ST.DEV                            │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  1. MOLA DE MICRO-RESPOSTA RÁPIDA (Boutique Click & Tab Switching):                   │
│     transition: { type: "spring", stiffness: 400, damping: 30, mass: 0.8 }            │
│     • Aplicação: Segmented Controls, Ícones animados, Active Pill Indicators.          │
│                                                                                        │
│  2. MOLA SUAVE VOLUMÉTRICA (Modal Expansion & Bento Hover):                            │
│     transition: { type: "spring", stiffness: 260, damping: 24, mass: 1 }              │
│     • Aplicação: Expansão de cards, abertura de gavetas (Drawers) e Dynamic Island.   │
│                                                                                        │
│  3. CURVA CÚBICA CINEMATOGRÁFICA (Hero Reveal & Fade In):                              │
│     cubic-bezier(0.16, 1, 0.3, 1)  [ Tailwind: ease-[cubic-bezier(0.16,1,0.3,1)] ]    │
│     • Duração: 0.6s a 0.8s                                                             │
│     • Aplicação: Entrada de títulos, revelação progressiva de seções no viewport.      │
│                                                                                        │
│  4. TRANSIÇÃO PADRÃO DE SUPERFÍCIE (Border & Color Micro-Transitions):                 │
│     cubic-bezier(0.4, 0, 0.2, 1)   [ Tailwind: ease-in-out / duration-200 ]            │
│     • Duração: 150ms a 200ms                                                           │
│     • Aplicação: Mudança de cor de fundo, troca de opacidade de texto e foco.          │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 5.2 Tokens CSS & Variáveis de Estilização
Abaixo estão os tokens de design essenciais (compatíveis com Tailwind CSS v3 e v4 e temas shadcn) que sustentam a paleta luminescente do catálogo:

```css
:root {
  /* Substrato Claro (Clean Studio) */
  --background: 0 0% 100%;
  --foreground: 240 10% 3.9%;
  --card: 0 0% 100%;
  --card-foreground: 240 10% 3.9%;
  --popover: 0 0% 100%;
  --popover-foreground: 240 10% 3.9%;
  --primary: 240 5.9% 10%;
  --primary-foreground: 0 0% 98%;
  --muted: 240 4.8% 95.9%;
  --muted-foreground: 240 3.8% 46.1%;
  --border: 240 5.9% 90%;
  --input: 240 5.9% 90%;
  --ring: 240 5.9% 10%;
  --radius: 0.75rem;

  /* Glow e Feixes Luminosos */
  --glow-indigo: rgba(99, 102, 241, 0.12);
  --glow-sky: rgba(56, 189, 248, 0.15);
  --bevel-light: rgba(0, 0, 0, 0.06);
}

.dark {
  /* Substrato Escuro (Dark Craft Linear) */
  --background: 240 10% 3.9%; /* #09090b */
  --foreground: 0 0% 98%;     /* #fafafa */
  --card: 240 10% 4.9%;       /* #0c0c0e */
  --card-foreground: 0 0% 98%;
  --popover: 240 10% 4.9%;
  --popover-foreground: 0 0% 98%;
  --primary: 0 0% 98%;
  --primary-foreground: 240 5.9% 10%;
  --muted: 240 3.7% 15.9%;    /* #27272a */
  --muted-foreground: 240 5% 64.9%;
  --border: 240 3.7% 15.9%;
  --input: 240 3.7% 15.9%;
  --ring: 240 4.9% 83.9%;

  /* Glows e Feixes Noturnos */
  --glow-indigo: rgba(99, 102, 241, 0.25);
  --glow-sky: rgba(56, 189, 248, 0.20);
  --bevel-dark: rgba(255, 255, 255, 0.08);
}
```

---

### 5.3 Receita de Código Funcional: `BentoGlowSpotlightCard.tsx`
O componente a seguir sintetiza a excelência do ecossistema 21st.dev: um cartão interativo do tipo Bento Grid com rastreamento contínuo de cursor (Spotlight), micro-borda biselada em 1px, animação vetorial com física de mola e suporte integral a acessibilidade e modo escuro:

```tsx
"use client";

import React, { useRef, useState, useCallback } from "react";
import { motion, useMotionValue, useSpring, useReducedMotion } from "framer-motion";
import { Sparkles, ArrowUpRight, Cpu } from "lucide-react";

interface BentoCardProps {
  category?: string;
  title: string;
  description: string;
  stats?: string;
  badge?: string;
  className?: string;
}

export const BentoGlowSpotlightCard: React.FC<BentoCardProps> = ({
  category = "AI AGENT ENGINE",
  title = "Context-Aware Agent Streaming",
  description = "Dispara pipelines em segundo plano com inspeção contínua de ferramentas e raciocínio em tempo real.",
  stats = "120ms latency",
  badge = "Active v2.4",
  className = "",
}) => {
  const cardRef = useRef<HTMLDivElement>(null);
  const [isHovered, setIsHovered] = useState(false);
  const shouldReduceMotion = useReducedMotion();

  // Coordenadas para o spotlight do cursor
  const mouseX = useMotionValue(-1000);
  const mouseY = useMotionValue(-1000);

  // Suavização das coordenadas com molas de baixo atrito
  const springConfig = { damping: 20, stiffness: 300, mass: 0.5 };
  const smoothX = useSpring(mouseX, springConfig);
  const smoothY = useSpring(mouseY, springConfig);

  const handleMouseMove = useCallback((e: React.MouseEvent<HTMLDivElement>) => {
    if (!cardRef.current) return;
    const { left, top } = cardRef.current.getBoundingClientRect();
    mouseX.set(e.clientX - left);
    mouseY.set(e.clientY - top);
  }, [mouseX, mouseY]);

  const handleMouseEnter = useCallback(() => setIsHovered(true), []);
  const handleMouseLeave = useCallback(() => {
    setIsHovered(false);
    mouseX.set(-1000);
    mouseY.set(-1000);
  }, [mouseX, mouseY]);

  return (
    <div
      ref={cardRef}
      onMouseMove={handleMouseMove}
      onMouseEnter={handleMouseEnter}
      onMouseLeave={handleMouseLeave}
      className={`group relative overflow-hidden rounded-2xl border border-zinc-200/80 bg-white/40 p-6 shadow-xs backdrop-blur-md transition-all duration-300 hover:border-zinc-300 dark:border-zinc-800/80 dark:bg-zinc-950/40 dark:hover:border-zinc-700 ${className}`}
    >
      {/* 1. MÁSCARA DE SPOTLIGHT QUE SEGUE O CURSOR */}
      {!shouldReduceMotion && (
        <motion.div
          className="pointer-events-none absolute -inset-px opacity-0 transition-opacity duration-300 group-hover:opacity-100"
          style={{
            background: `radial-gradient(400px circle at ${smoothX.get()}px ${smoothY.get()}px, rgba(99, 102, 241, 0.12), transparent 80%)`,
          }}
          aria-hidden="true"
        />
      )}

      {/* 2. MICRO-BORDA BISELADA NO TOPO (1px specular highlight) */}
      <div 
        className="pointer-events-none absolute inset-x-0 top-0 h-px bg-gradient-to-r from-transparent via-indigo-500/30 to-transparent dark:via-indigo-400/20"
        aria-hidden="true"
      />

      <div className="relative z-10 flex h-full flex-col justify-between">
        {/* Cabeçalho do Card */}
        <div>
          <div className="flex items-center justify-between gap-2">
            <span className="font-mono text-[11px] font-semibold tracking-wider text-indigo-600 dark:text-indigo-400">
              {category}
            </span>
            <span className="inline-flex items-center gap-1 rounded-full border border-zinc-200 bg-zinc-100/80 px-2 py-0.5 font-mono text-[10px] font-medium text-zinc-700 dark:border-zinc-800 dark:bg-zinc-900/80 dark:text-zinc-300">
              <span className="h-1.5 w-1.5 rounded-full bg-emerald-500 animate-pulse" />
              {badge}
            </span>
          </div>

          <h3 className="mt-3 text-lg font-medium tracking-tight text-zinc-900 dark:text-zinc-100 sm:text-xl">
            {title}
          </h3>

          <p className="mt-2 line-clamp-2 text-sm leading-relaxed text-zinc-600 dark:text-zinc-400">
            {description}
          </p>
        </div>

        {/* Área Visual Interativa / Showcase Central */}
        <div className="my-6 flex h-28 items-center justify-center rounded-xl border border-dashed border-zinc-200 bg-zinc-50/50 dark:border-zinc-800/80 dark:bg-zinc-900/30">
          <motion.div
            animate={
              isHovered && !shouldReduceMotion
                ? { scale: [1, 1.05, 1], rotate: [0, 5, -5, 0] }
                : { scale: 1, rotate: 0 }
            }
            transition={{ duration: 1.5, repeat: isHovered ? Infinity : 0, ease: "easeInOut" }}
            className="flex h-12 w-12 items-center justify-center rounded-xl bg-indigo-500/10 text-indigo-600 dark:bg-indigo-400/10 dark:text-indigo-400"
          >
            <Cpu className="h-6 w-6" />
          </motion.div>
        </div>

        {/* Rodapé com Estatísticas e Link de Ação */}
        <div className="flex items-center justify-between pt-2 border-t border-zinc-200/60 dark:border-zinc-800/60">
          <span className="font-mono text-xs tabular-nums text-zinc-500 dark:text-zinc-400">
            {stats}
          </span>

          <motion.a
            href="#explore"
            whileHover={shouldReduceMotion ? {} : { scale: 1.03 }}
            whileTap={shouldReduceMotion ? {} : { scale: 0.97 }}
            className="inline-flex items-center gap-1.5 rounded-lg bg-zinc-900 px-3 py-1.5 text-xs font-medium text-white shadow-xs transition-colors hover:bg-zinc-800 dark:bg-zinc-100 dark:text-zinc-900 dark:hover:bg-zinc-200 focus-visible:outline-2 focus-visible:outline-indigo-500"
          >
            <span>Ver Blueprint</span>
            <ArrowUpRight className="h-3.5 w-3.5 transition-transform duration-200 group-hover:translate-x-0.5 group-hover:-translate-y-0.5" />
          </motion.a>
        </div>
      </div>
    </div>
  );
};

export default BentoGlowSpotlightCard;
```

---

### 5.4 Como a IA Deve Pesquisar ao Vivo no 21st.dev

Para agentes autônomos (como Cursor, Claude Code, Windsurf ou LLMs de engenharia frontend) realizarem consultas em tempo real no 21st.dev sem alucinar rotas, deve-se adotar o seguinte mapa de navegação e sintaxe oficial de URLs:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        MAPA DE CONSULTA EM TEMPO REAL NO 21ST.DEV                      │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  Base Web: https://21st.dev                                                            │
│  MCP Server Endpoint: https://21st.dev/api/mcp (ou /api/mcp/readonly)                  │
│                                                                                        │
│  1. EXPLORAÇÃO DAS 166 BIBLIOTECAS COMUNITÁRIAS:                                       │
│     • Diretório Completo:           https://21st.dev/community/libraries               │
│     • Ordenação por Visualizações:   https://21st.dev/community/libraries?sort=views   │
│     • Ordenação por Mais Recentes:   https://21st.dev/community/libraries?sort=newest  │
│     • Ordenação por N° Componentes:  https://21st.dev/community/libraries?sort=components│
│                                                                                        │
│  2. FILTROS POR CATEGORIAS DE ENGENHARIA DE UI (/community/libraries/s/<slug>):        │
│     • Design System Base:   /community/libraries/s/design-system                       │
│     • Marketing UI:         /community/libraries/s/marketing                           │
│     • Dashboard UI:         /community/libraries/s/dashboard                           │
│     • Blocos de IA (Agent): /community/libraries/s/ai                                  │
│     • Microinterações/Motion:/community/libraries/s/motion                             │
│     • Gráficos & Visualização:/community/libraries/s/charts                             │
│     • Formulários Complexos:/community/libraries/s/forms                               │
│     • Ícones Animados:      /community/libraries/s/icons                               │
│                                                                                        │
│  3. BUSCA DIRETA DE COMPONENTES POR INTENÇÃO:                                          │
│     https://21st.dev/community/components?q=[termo-em-ingles]                          │
│     • Exemplo Hero:        ?q=animated%20hero%20section                                │
│     • Exemplo Pricing:     ?q=bento%20pricing%20table                                  │
│     • Exemplo AI Chat:     ?q=ai%20chat%20input                                        │
│                                                                                        │
│  4. INSTALAÇÃO DIRETA VIA SHADCN CLI OU @21st-dev/cli:                                 │
│     • Via shadcn:  npx shadcn@latest add "https://21st.dev/r/@<autor>/<componente>"    │
│     • Via 21st:    npx @21st-dev/cli@latest add <autor>/<componente>                   │
│                                                                                        │
│  5. ACESSO VIA FORMATO MARKDOWN PURO (Twin Markdown):                                  │
│     Qualquer URL pública do 21st.dev suporta o envio do header HTTP:                   │
│     Accept: text/markdown  OU  anexação do sufixo .md na URL                           │
│     Retorna o código-fonte puro e metadados estruturados para consumo direto do LLM!   │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao integrar os padrões do **21st.dev Community Libraries** em um plano de engenharia de software e design de interfaces (`DESIGN_BLUEPRINT.md`), o arquiteto de software e o agente devem cumprir rigorosamente os cinco mandamentos:

1. **Priorize a Posse do Código sobre Caixas Pretas**:
   - Nunca instale pacotes npm exóticos ou monólitos fechados para microinterações cosméticas que podem ser resolvidas com 40 linhas de React + Tailwind + Framer Motion. Traga o código para `/components/ui/` onde a equipe mantém controle absoluto do ciclo de vida.
2. **Harmonize o Padrão de Micro-Bisel (1px Precision Rule)**:
   - Adote bordas semitransparentes de `1px` (`border-border/60` ou `rgba(255, 255, 255, 0.08)`) associadas a cantos arredondados contínuos (`rounded-xl` e `rounded-2xl`). Não utilize bordas sólidas pesadas sem justificativa de linguagem neobrutalista explícita.
3. **Respeite a Física de Molas em Lugar de Durações Lineares**:
   - Não use transições CSS lineares ou `ease-in` artificiais para elementos móveis ou interativos. Configure molas físicas com `stiffness: 300` e `damping: 25`, garantindo que a resposta ao toque pareça orgânica e elástica.
4. **Resguarde a Acessibilidade e a Economia de Bateria**:
   - Toda animação espacial ou loop contínuo deve ser encapsulado sob o hook `useReducedMotion()`.
   - Elementos focáveis copiados da biblioteca devem preservar `focus-visible:ring-2 focus-visible:ring-indigo-500` e rótulos ARIA para leitores de tela.
5. **Aplique o Princípio do Ponto Focal Único**:
   - Restrinja efeitos volumétricos pesados (como shaders WebGL, partículas ou feixes luminosos) a um único elemento por viewport para manter 60fps estáveis em qualquer dispositivo e garantir que o conteúdo e os dados permaneçam como o protagonista absoluto da experiência.
