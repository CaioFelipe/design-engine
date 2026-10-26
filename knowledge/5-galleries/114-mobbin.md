---
id: "mobbin"
name: "Mobbin"
url: "https://mobbin.com/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico:
  - "Real-World Shipped Production Software UX"
  - "End-to-End User Journeys & Multi-Step Interactive Flows"
  - "Multi-Platform Native Fidelity (iOS, Android & Web App Architecture)"
  - "Atomic UI Element Decomposition & Design System Taxonomy"
  - "Optical Precision & Strict 8pt Grid Human Interface Guidelines (HIG / Material 3)"
  - "OCR Text Copy Indexing & Real Microcopy Architecture"
  - "Contextual State Management (Empty States, Error States, Success Modals, Paywalls)"
  - "Figma Plugin Interoperability & Prototype Hotspot Navigation"
densidade_informacao: "Alta/Utilitaria"
impacto_visual: "Editorial/Sofisticado & High-Fidelity Native Production"
custo_computacional: "Baixo a Moderado (Componentes nativos ultra-otimizados, aceleração por GPU a 60fps/120fps ProMotion, layout springs sem layout-shift, zero WebGL superfluo)"
stack_frameworks:
  - "React Native / Expo"
  - "Swift / SwiftUI (iOS Human Interface Guidelines)"
  - "Kotlin / Jetpack Compose (Android Material 3)"
  - "Next.js 15 / React 19 / TypeScript"
  - "Tailwind CSS v3 / v4 (Container queries, arbitrary properties, safe-area utilities)"
  - "Framer Motion / Motion.dev (molas com amortecimento tátil e transições de layout compartilhado)"
  - "Radix UI Primitives / Shadcn UI / Base UI"
compatibilidade:
  fontes_ideais:
    - "Sistemas Nativos de Sistema Operacional: SF Pro Display / SF Pro Text (iOS/macOS), Roboto / Roboto Flex (Android), Segoe UI (Windows)"
    - "Neo-Grotesks Corporativas Neutras: Inter, Geist Sans, PP Neue Montreal, Roobert, Plus Jakarta Sans, Circular, DM Sans"
    - "Grotesks Geométricas Modernas de Produto: Satoshi, General Sans, Manrope, Urbanist"
    - "Monospaced Funcionais de Dados & Transações: Geist Mono, JetBrains Mono, SF Mono, Fira Code"
    - "Serifas Editoriais de Luxo & Finanças (D2C / Wealth Management): New York (Apple), Fraunces, GT Super, Instrument Serif"
  paletas_ideais:
    - "Apple Human Interface Semantic Tokens (Light & Dark Mode Nativo): Canvas (#FFFFFF / #000000), Grouped Background (#F2F2F7 / #1C1C1E), Separator (#C6C6C8 / #38383A), Tint Blue (#007AFF), Destructive Red (#FF3B30), Success Green (#34C759)"
    - "Material Design 3 Dynamic Tonal Surface: Surface (#FEF7FF / #141218), Surface Container (#F3EDF7 / #211F26), Primary (#6750A4 / #D0BCFF), Outline (#79747E / #938F99)"
    - "Modern Dark B2B / FinTech SaaS (Linear / Stripe / Mercury Vibe): #09090B (Background Zinc-950), #18181B (Surface Zinc-900), #27272A (Border Zinc-800), #FAFAFA (Text Primary), #A1A1AA (Text Secondary), #3B82F6 (Electric Accent Blue) ou #10B981 (Emerald Mint)"
    - "Clean High-Trust Consumer Mobile (Airbnb / Duolingo / Uber Vibe): #FFFFFF (Pure Canvas), #F7F7F7 (Surface Secondary), #E5E5E5 (Subtle Border), #222222 (Heading Jet Black), #717171 (Muted Gray), #FF385C (Coral Radical) ou #58CC02 (Vibrant Green)"
  combinacoes_recomendadas:
    - "Radix UI Primitives + Tailwind CSS + Framer Motion para reconstrução web de padrões mobile nativos (Action Sheets, Modais com drag gesture, Segmented Tabs, Tooltips)"
    - "Lucide Icons ou Tabler Icons em stroke uniforme de 1.5px ou 2.0px alinhados opticamente a caixas delimitadoras de 20x20px e 24x24px"
    - "Uso estrito do 8-Point Grid System (multiplos de 4px e 8px: 4, 8, 12, 16, 24, 32, 48, 64) para margens horizontais, paddings de cards e respiro vertical"
    - "Superfícies de vidro fosco com backdrop-filter (`backdrop-blur-xl` com fundo semi-transparente `rgba(255,255,255,0.7)` no Light e `rgba(24,24,27,0.75)` no Dark) para Navigation Bars e Floating Bottom Sheets"
  conflitos_esteticos:
    - "Dribbble-shots fictícios com layouts inexequíveis em código real, sem tratamento de estados de erro, loading ou overflow"
    - "Áreas de toque (Touch Targets) minúsculas menores que 44×44pt (iOS) ou 48×48dp (Android), violando ergonomia e acessibilidade WCAG"
    - "Efeitos visuais WebGL tridimensionais pesados que roubam o foco de tarefas transacionais críticas (checkout, autenticação, onboarding)"
    - "Tipografia decorativa de baixa legibilidade em corpos de texto menores que 14px em interfaces móveis"
    - "Desconsideração de áreas seguras do dispositivo (Notch, Dynamic Island, Home Indicator do iPhone, Navigation Bar do Android)"
    - "Dark Patterns ou truques visuais que induzem o usuário ao erro em telas de cancelamento ou renovação automática de assinatura"
---

# Mobbin — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
███╗   ███╗ ██████╗ ██████╗ ██████╗ ██╗███╗   ██╗
████╗ ████║██╔═══██╗██╔══██╗██╔══██╗██║████╗  ██║
██╔████╔██║██║   ██║██████╔╝██████╔╝██║██╔██╗ ██║
██║╚██╔╝██║██║   ██║██╔══██╗██╔══██╗██║██║╚██╗██║
██║ ╚═╝ ██║╚██████╔╝██████╔╝██████╔╝██║██║ ╚████║
╚═╝     ╚═╝ ╚═════╝ ╚═════╝ ╚═════╝ ╚═╝╚═╝  ╚═══╝
```

---

## 1. DNA Estético & Filosofia de Curadoria

Fundado em 2018 em Singapura pelo designer de produto independente **Jiho Lim** em colaboração com o engenheiro **Jovin Liew**, o **Mobbin** (`https://mobbin.com/`) consolidou-se como a **maior e mais rigorosa enciclopédia de padrões de interface de usuário (UI) e jornadas de experiência (UX) do planeta**. Com um acervo superior a **620.000 telas em altíssima resolução** e **153.000 fluxos de ponta a ponta indexados**, a plataforma tornou-se o benchmark obrigatório para times de design, engenharia e produto de empresas como Apple, Airbnb, Stripe, Uber, Google, Figma e Meta.

A gênese do Mobbin decorreu de uma frustração estrutural crônica vivida por Jiho Lim ao atuar como designer de aplicativos móveis: o ciclo exaustivo de ter que baixar dezenas de aplicativos na App Store, criar contas fictícias, cadastrar cartões de crédito para ultrapassar paywalls e tirar centenas de screenshots manuais para dissecar como grandes produtos resolviam problemas pontuais de onboarding, checkouts, configurações ou cancelamentos. O Mobbin nasceu para transformar esse trabalho empírico e desordenado em uma infraestrutura sistemática, consultável e de precisão cirúrgica.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        THE MOBBIN CURATORIAL MANIFESTO                                 │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  [ Shipped Production Realism ] ──► [ End-to-End User Journeys ] ──► [ Atomic Anatomy ] │
│   • 100% Real Shipped Products       • Multi-Step User Flows           • Searchable Elements │
│   • Multi-Platform (iOS/Android/Web) • Interactive Hotspots Prototype • Microcopy OCR Engine │
│   • Complete State Matrix (Error/Empty) • Direct Figma Plugin Bridge   • Version History Log │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  THE CORE AXIOM: "Good design is not an isolated still; it is an orchestrated journey."  │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

### 1.1 O Fim do "Dribbblisation of Design": Produção Real vs. Fantasia Estética

O surgimento do Mobbin representou um ponto de inflexão na cultura de design digital moderno, liderando a reação contra o que a comunidade cunhou como *"The Dribbblisation of Design"*:

1. **A Patologia do Dribbble / Behance**:
   - Telas conceituais fictícias, criadas para colecionar "likes" visuais com tipografia ultralight de 9px cinza claro sobre fundo branco;
   - Interfaces sem botões de voltar, sem tratamento de conexões offline, sem estados de validação de formulário ou suporte a internacionalização;
   - Mockups tridimensionais inclinados em ângulos de 45° com sombras neon irreais, totalmente impossíveis de serem codificados em SwiftUI, Jetpack Compose ou CSS nativo.

2. **O Paradigma Mobbin**:
   - **Realidade em Produção (Shipped Reality)**: Toda e qualquer tela catalogada está ou esteve rodando em milhões de dispositivos reais de usuários no mundo;
   - **Jornadas Conectadas (End-to-End Flows)**: Um paywall nunca é exibido isolado; o Mobbin captura o gatilho inicial (o clique numa feature bloqueada), o modal contextual de proposta de valor, a tela de seleção de planos, o prompt nativo do sistema operacional (Apple StoreKit / Google Play Billing) e a tela de confirmação/onboarding premium;
   - **Resolução de Conflitos e Casos Limite**: Mapeamento de erros de digitação de senhas, validações de dois fatores (2FA), e-mails de recuperação, telas de confirmação de permissão nativa de câmera/geolocalização e cenários de permissão negada.

---

### 1.2 As Quatro Dimensões Estruturais da Curadoria

A plataforma do Mobbin organiza a experiência do produto digital através de 4 entidades fundamentais interconectadas:

```
                                    ┌───────────────────────────────────────────────┐
                                    │             MOBBIN ENTITY CORE                │
                                    └──────────────────────┬────────────────────────┘
                                                           │
          ┌──────────────────┬─────────────────────────────┼────────────────────────────┬──────────────────┐
          ▼                  ▼                             ▼                            ▼                  ▼
┌──────────────────┐┌──────────────────┐     ┌──────────────────────┐      ┌──────────────────┐┌──────────────────┐
│     SCREENS      ││      FLOWS       │     │     UI ELEMENTS      │      │       APPS       ││    COPY SEARCH   │
├──────────────────┤├──────────────────┤     ├──────────────────────┤      ├──────────────────┤├──────────────────┤
│ • Telas unitárias││ • Jornadas passo │     │ • Decomposição       │      │ • Perfil global  ││ • OCR em tempo   │
│   capturadas em  ││   a passo        │     │   atômica da tela    │      │   de produtos    ││   real sobre     │
│   resolução @3x  ││ • Modo protótipo │     │ • Action Sheets      │      │ • Histórico de   ││   todo o texto   │
│   Retina nativa  ││   interativo     │     │ • Bottom Drawers     │      │   versões e      ││   das interfaces │
│ • Filtráveis por ││ • Hotspots de    │     │ • Segmented Controls │      │   rebrandings    ││ • Pesquisa por  │
│   plataforma e cor│   clique reais   │     │ • Modais de contexto │      │ • Metadados App  ││   "Cancel Plan", │
│ • Tags de padrão ││ • Mapeamento de  │     │ • Carrosséis de cards│      │   Store / Play   ││   "Forgot pass", │
│   e estado visual││   bifurcações UX │     │ • Banners & Badges   │      │   Store & Web    ││   "Free Trial"   │
└──────────────────┘└──────────────────┘     └──────────────────────┘      └──────────────────┘└──────────────────┘
```

1. **Screens (Telas Estáticas Detalhadas)**: Capturas de tela individuais com marcações estruturadas de elementos, permitindo inspecionar cada elemento atômico, paleta de cores dominante e hierarquia tipográfica.
2. **Flows (Fluxos Sequenciais Completos)**: A sequência linear ou ramificada que um usuário percorre para atingir um objetivo específico. O Mobbin oferece o recurso **Interactive Prototype Mode**, que transforma a sequência estática em um protótipo navegável por hotspots exatamente como o app original se comportava.
3. **UI Elements (Decomposição Atômica)**: Catálogo isolado de componentes específicos (ex: botões flutuantes, barras de abas, seletores de data, botões de alternância, bottom sheets), permitindo comparar como 50 produtos diferentes desenharam o mesmo elemento de interface.
4. **Copy Search (Busca Textual via Reconhecimento Óptico de Caracteres - OCR)**: Funcionalidade proprietária que indexa cada caractere impresso nos screenshots. Permite que um analista ou modelo de IA busque instantaneamente como a Netflix formula sua cláusula de renovação automática, como o Duolingo redige a perda de vidas ou como o Uber solicita permissão de localização.

---

### 1.3 A Matriz Completa de Taxonomia do Mobbin

A arquitetura de navegação e filtros do Mobbin cobre a totalidade do espectro de software contemporâneo:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                               MOBBIN TAXONOMY MATRIX                                   │
├───────────────────────┬────────────────────────────────┬───────────────────────────────┤
│ PLATAFORMAS (3)       │ CATEGORIAS DE APP (16+)        │ FAMÍLIAS DE FLUXOS (30+)      │
├───────────────────────┼────────────────────────────────┼───────────────────────────────┤
│ • iOS (iPhone/iPad)   │ • Finance & Fintech            │ • Onboarding & Welcome        │
│ • Android (Phones)    │ • Health & Fitness             │ • Sign Up & Registration      │
│ • Web (Apps & SaaS)   │ • Productivity & DevTools      │ • Log In & Passkey / 2FA      │
│                       │ • Social Networking            │ • Subscription & Paywall      │
│                       │ • E-Commerce & Shopping        │ • Checkout & Payment          │
│                       │ • Food & Delivery              │ • Search, Filter & Discovery  │
│                       │ • Travel & Mobility            │ • Settings & Account Mgmt     │
│                       │ • Entertainment & Streaming    │ • Permissions Priming         │
│                       │ • Education & EdTech           │ • Referrals & Viral Loops     │
│                       │ • Crypto & Web3                │ • Cancel Subscription Flow    │
│                       │ • Artificial Intelligence / ML │ • Create / Post Creation      │
├───────────────────────┴────────────────────────────────┴───────────────────────────────┤
│ ELEMENTOS DE INTERFACE (40+ UI ELEMENTS CATALOGADOS)                                   │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ Action Sheets • Activity Feeds • App Bars • Avatars • Badges • Banners • Bottom Sheets │
│ Bottom Navigation Bars • Buttons (FAB, Ghost, Primary) • Cards • Carousels • Chips     │
│ Context Menus • Date Pickers • Dialogs/Modals • Empty States • Floating Docks • Grids  │
│ Input Fields (OTP, Search, Floating Label) • Lists & Table Views • Progress Bars       │
│ Segmented Controls • Skeleton Screens • Sliders • Steppers • Tabs • Toggles/Switches   │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

O Mobbin **não** é uma galeria para buscar ornamentação estética vazia ou efeitos visuais passageiros; ele é a **fonte primária de engenharia de interação, arquitetura de fluxos de conversão e design systems de produção**.

### 2.1 Casos de Uso Canônicos

1. **Desenho de Funis de Alta Conversão (Onboarding, Autenticação e Checkout)**:
   - Quando o projeto precisa guiar um novo usuário desde o primeiro download até a ativação do valor central (Time-to-Value) sem fricção cognitiva desnecessária;
   - Referência cirúrgica para balancear coleta de dados do perfil (*Progressive Profiling*) com taxas de retenção.

2. **Arquitetura de Paywalls e Monetização Contextual**:
   - Quando o produto precisa apresentar planos mensais/anuais, destacar propostas de valor com comparativos lado a lado, desarmar objeções com períodos de teste gratuito (*Free Trial*) e cumprir diretrizes estritas da Apple App Store e Google Play.

3. **Definição de Design Systems & Tokens de Componentes Nativos**:
   - Criação de bibliotecas corporativas baseadas em Tailwind CSS, Radix UI, React Native ou SwiftUI, buscando padronizar raios de borda, elevações de sombras, estados visuais (pressionado, desabilitado, carregando) e espaçamentos no sistema 8pt.

4. **Navegação Ergonômica Mobile-First**:
   - Mapeamento de interações para a zona de alcance do polegar (*Thumb Zone*), usando Navigation Bars inferiores, Bottom Sheets expansíveis e Sticky Action Bars ancoradas acima do teclado ou na borda inferior.

---

### 2.2 Aplicação Prática da Regra 60-30-10 no Mobbin

Nas interfaces mapeadas pelo Mobbin, a distribuição cromática segue rigorosamente a psicologia de foco do usuário:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                      THE 60-30-10 RULE IN PRODUCTION UI (MOBBIN)                       │
├────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                        │
│  ██████████████████████████████  60% — THE NEUTRAL CANVAS                              │
│  Superfícies de fundo (Backgrounds), cartões agrupados e canvas limpo.                 │
│  Ex: #FFFFFF / #F2F2F7 no iOS Light Mode; #000000 / #1C1C1E no iOS Dark Mode.           │
│  Garante descanso visual, alto contraste de legibilidade e foco no conteúdo.          │
│                                                                                        │
│  ███████████████                 30% — THE STRUCTURAL & TYPOGRAPHIC LAYER              │
│  Hierarquia de texto (Títulos em preto absoluto/branco, corpo em cinza neutro),         │
│  bordas divisórias estruturais de 1px (`border-zinc-200` ou `white/10`), ícones         │
│  auxiliares, superfícies elevadas e avatares.                                          │
│                                                                                        │
│  █████                           10% — THE PURE INTENTIONAL ACCENT                     │
│  Reservado estritamente para ações críticas e feedback de status:                      │
│  Botão primário de CTA ("Continuar", "Assinar Plano"), toggle ativo, chave de seleção, │
│  notificação pendente ou badge de desconto ("Salvar 30%").                             │
│                                                                                        │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

### 3.1 ⚠️ Incompatível Com

1. **Campanhas de Branding de Luxo e Sites Cinemáticos WebGL**:
   - Projetos cujo objetivo primário é o deslumbramento audiovisual abstrato (ex: grifes de alta costura, lançamentos de automóveis conceituais, portfólios de estúdios criativos 3D). Aplicar os padrões utilitários do Mobbin nesses casos resultará em uma sensação excessivamente corporativa e funcional.

2. **Websites Editoriais Literários de Texto Puro**:
   - Revistas literárias, blogs contemplativos ou manifestos poéticos que exigem tipografia clássica serifada de página inteira, grandes margens de livro e ausência total de controles de interface ou botões de ação repetitivos.

3. **Landing Pages de Apelo Bruto / Anti-Design**:
   - Movimentos que buscam choque estético intencional, caos tipográfico, layouts desalinhados e visual neo-brutalista cru. A curadoria do Mobbin reflete o refinamento industrial moderno, simétrico e padronizado.

---

### 3.2 ⚠️ Armadilhas de Imitação & Anti-Padrões Notáveis

- 🚫 **Cargo Cult de Grandes Tecnologias (Big Tech Bias)**:
  - Copiar cegamente fluxos do Instagram, Uber ou Airbnb sem considerar o contexto do seu produto. Por exemplo: exigir que o usuário crie uma conta antes de permitir que ele experimente a ferramenta central do seu app só funciona para produtos com demanda inelástica; para novos entrantes, isso gera mais de 60% de abandono imediato no primeiro minuto.

- 🚫 **Dark Patterns & Anti-Cancelamento Opressivo**:
  - Replicar fluxos de cancelamento complexos (com múltiplos questionários de culpa, botões de "Permanecer" com cor primária chamativa e botões de "Confirmar Cancelamento" em texto cinza camuflado no fundo). Além de gerar ressentimento de marca, essas práticas violam leis de proteção ao consumidor na UE (Diretiva Omnibus) e nos EUA (FTC).

- 🚫 **Fragmentação de Paradigmas de Plataforma**:
  - Tentar forçar componentes com estética de iOS (como segmented controls e switches arredondados com botão de voltar no topo esquerdo) em um app Android nativo que deveria adotar Material You / Material 3 (com Navigation Bar com indicadores em formato de pílula, FABs e navegação por gestos do sistema operacional).

- 🚫 **Violação das Áreas Seguras e Zonas Ergonômicas**:
  - Posicionar botões de ação primária ou elementos interativos no topo extremo da tela (fora do alcance do polegar) ou colados na margem inferior sem respeitar a área segura do Home Indicator do iPhone (`safe-area-inset-bottom`), gerando toques acidentais que fecham o aplicativo.

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo

Todas as interfaces catalogadas no Mobbin obedecem rigorosamente aos padrões geométricos dos sistemas operacionais móveis e desktops:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        CANONICAL VIEWPORTS & SAFE AREAS                                │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  MOBILE NATIVO (iOS / Android):                                                        │
│  • iPhone Base: 375×812pt (Mini), 393×852pt (Standard/Pro), 430×932pt (Pro Max)       │
│  • Safe Area Top: 47pt a 59pt (Dynamic Island / Notch)                                 │
│  • Safe Area Bottom: 34pt (Home Indicator)                                             │
│  • Margens Laterais Globais: 16pt a 20pt (Padding de tela padrão)                       │
│  • Espaçamento Entre Grupos de Conteúdo: 24pt a 32pt                                    │
│                                                                                        │
│  DESKTOP WEB APPS (SaaS):                                                              │
│  • Largura de Conteúdo: 1280px ou 1440px centralizada                                  │
│  • Grid: 12 Colunas com gutters de 16px ou 24px                                        │
│  • Sidebar de Navegação: 240px a 280px fixa com estados recolhidos para 64px           │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

#### O Sistema Base-8 (8-Point Grid System)
Todos os espaçamentos, alturas de botões e paddings internos de cartões são múltiplos inteiros de **8** (com subdivisões secundárias de **4** para micro-espaçamento de ícones e rótulos):
- **4px**: Respiro entre ícone e texto ou badge e label;
- **8px**: Espaçamento entre inputs em formulários densos;
- **12px / 16px**: Padding interno de cards e inputs de texto;
- **24px**: Distância vertical entre blocos de perguntas em formulários;
- **44px / 48px / 56px**: Alturas padrão de botões primários de ação, garantindo áreas de clique confortáveis.

---

### 4.2 Sistemas de Cores, Superfícies & Materiais

O Mobbin revela a transição contemporânea de interfaces flat puras para sistemas com profundidade tátil e translucidez semântica:

1. **Camadas de Superfície Semântica (Elevation Stack)**:
   - **Nível 0 (Canvas Base)**: Fundo neutro do sistema (`#FFFFFF` no Light / `#000000` no Dark OLED);
   - **Nível 1 (Grouped Cards / Lists)**: Superfície agrupada com contraste suave (`#F2F2F7` ou `#1C1C1E`);
   - **Nível 2 (Modais e Floating Sheets)**: Superfície com sombra difusa e cantos arredondados generosos (`rounded-3xl` / 24px-32px);
   - **Nível 3 (Overlays & Alertas)**: Elevado sobre camada escura com backdrop blur (`rgba(0,0,0,0.4)` + `backdrop-blur-md`).

2. **Translucidez Dinâmica (Vibrancy & Material)**:
   - Barras de navegação superiores e docks inferiores aplicam efeito de vidro fosco (`backdrop-blur-xl`) com transparência de 80%, permitindo que o conteúdo rolante transpareça sutilmente por baixo, mantendo o usuário ancorado espacialmente.

---

### 4.3 Catálogo Detalhado de 10 Arquétipos & Componentes Notáveis do Mobbin

Abaixo estão os 10 componentes e fluxos mais catalogados e refinados no acervo do Mobbin:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        CATÁLOGO DE ARQUÉTIPOS NOTÁVEIS MOBBIN                          │
├────┬───────────────────────────────────────────────────────┬───────────────────────────┤
│ #  │ NOME DO PADRÃO / COMPONENTE                           │ DOMÍNIO TÍPICO            │
├────┼───────────────────────────────────────────────────────┼───────────────────────────┤
│ 01 │ Progressive Onboarding com Permission Priming         │ Duolingo, Headspace, Calm │
│ 02 │ Multi-Detent Interactive Bottom Sheet                 │ Apple Maps, Uber, Airbnb  │
│ 03 │ High-Converting Contextual Paywall Matrix             │ Blinkist, Flo, VSCO       │
│ 04 │ Floating Dynamic Island Tab Bar                       │ Arc Search, Linear Mobile │
│ 05 │ Predictive Search Bar com Scoped Filter Chips         │ Spotify, Notion, Airbnb   │
│ 06 │ Frictionless Auth Sequence (Passkey / Magic Link)     │ Cash App, Stripe, Robinhood│
│ 07 │ High-Empathy Educative Empty State                    │ Linear, GitHub Mobile     │
│ 08 │ Sticky Action Dock com Dual Touch Target              │ Amazon, DoorDash, ASOS    │
│ 09 │ Interactive Activity Feed com Swipe Actions           │ Superhuman, Spark, Slack  │
│ 10 │ Grouped Cell Settings Hierarchy com Visual Feedback   │ iOS Settings, Telegram    │
└────┴───────────────────────────────────────────────────────┴───────────────────────────┘
```

---

#### Arquétipo 1: Progressive Onboarding com Permission Priming

```
┌─────────────────────────────────────────┐
│ [●●●○○] 3 of 5                  [Skip]  │ ◄─── Barra de progresso segmentada
│                                         │
│        ┌───────────────────────┐        │
│        │   🔔 [ILUSTRAÇÃO 3D]   │        │ ◄─── Ilustração com significado tátil
│        └───────────────────────┘        │
│                                         │
│   Nunca perca uma oportunidade          │ ◄─── Título focado em benefício claro
│   Receba alertas em tempo real sobre    │
│   transações suspeitas e rendimentos.   │ ◄─── Texto explicativo que reduz atrito
│                                         │
│   ┌─────────────────────────────────┐   │
│   │  ✓ Sem spam ou mensagens chatas │   │ ◄─── Desarmamento de ansiedade
│   │  ✓ Ajuste os alertas a qualquer │   │
│   │    momento nas configurações    │   │
│   └─────────────────────────────────┘   │
│                                         │
│ ┌─────────────────────────────────────┐ │
│ │        Ativar Notificações          │ │ ◄─── Botão Primário (Dispara modal nativo)
│ └─────────────────────────────────────┘ │
│                Agora não                │ ◄─── Botão Secundário Ghost
└─────────────────────────────────────────┘
```
- **Anatomia**:
  1. Barra de progresso segmentada no topo informando o passo atual;
  2. Ilustração temática de alta fidelidade;
  3. Proposta de valor focada no que o usuário **ganha** permitindo o acesso;
  4. Lista de garantias desarmando o medo de spam ou invasão de privacidade;
  5. Botão primário que prepara psicologicamente o usuário antes de o app acionar a caixa de diálogo nativa e irreversível do sistema operacional.
- **Gatilho**: Após o usuário concluir a configuração inicial ou demonstrar interesse por um recurso que depende de permissão.
- **Onde Encaixar**: Entre a criação da conta e a primeira sessão de uso do produto.

---

#### Arquétipo 2: Multi-Detent Interactive Bottom Sheet (Painel Inferior de Múltiplas Alturas)

```
┌─────────────────────────────────────────┐
│ [ MAPA OU CONTEÚDO PRINCIPAL DE FUNDO ] │
│                                         │
│ ┌─────────────────────────────────────┐ │
│ │                ════                 │ │ ◄─── Grab Handle tátil centralizado
│ │ Próximo a você               [Ver +]│ │ ◄─── Cabeçalho ancorado
│ │                                     │ │
│ │ ┌───────────┐ ┌───────────────────┐ │ │
│ │ │ ☕ Café   │ │ 🥐 Padarias       │ │ │ ◄─── Carrossel horizontal de filtros
│ │ └───────────┘ └───────────────────┘ │ │
│ │                                     │ │
│ │ • Starbucks Reserve (120m)    4.8★  │ │
│ │ • Artisan Bakery (350m)       4.9★  │ │ ◄─── Lista rolante com snap points:
│ │ • Coffee Lab (500m)           4.7★  │ │      Collapsed (25%), Half (50%), Full (90%)
│ └─────────────────────────────────────┘ │
└─────────────────────────────────────────┘
```
- **Anatomia**:
  1. Alça de arraste (*Grab Handle*) de 36×5px arredondada com área de toque ampliada;
  2. Três pontos de ancoragem (*Snap Points*): Colapsado (peek view de 20%), Meia-altura (50%) e Tela Cheia (90%);
  3. Fundo translúcido com `backdrop-blur-xl` e cantos arredondados de 24px a 32px;
  4. Suporte a gesto de arrasto com inércia de velocidade física e feedback háptico na troca de detents.
- **Gatilho**: Quando o usuário pesquisa itens em um mapa, seleciona opções em uma lista ou abre detalhes rápidos sem perder o contexto subjacente.
- **Onde Encaixar**: Aplicativos de mapas, e-commerce, reprodutores de mídia e painéis de filtros.

---

#### Arquétipo 3: High-Converting Contextual Paywall Matrix

```
┌─────────────────────────────────────────┐
│ [✕]                             Restaurar│ ◄─── Botão Fechar e Restaurar Compras
│                                         │
│             ⚡ PRO UNLIMITED             │
│   Desbloqueie todo o poder da sua equipe│
│                                         │
│  ✓ Modelos de IA ilimitados e sem fila  │
│  ✓ Exportação em 4K e sincronização na nuvem
│  ✓ Suporte prioritário 24/7             │
│                                         │
│ ┌─────────────────────────────────────┐ │
│ │ 🔘 ANUAL • R$ 24,90/mês  [-45% OFF] │ │ ◄─── Opção Recomendada com Badge
│ │    Cobrado R$ 299/ano após 7 dias   │ │
│ └─────────────────────────────────────┘ │
│ ┌─────────────────────────────────────┐ │
│ │ ⚪ MENSAL • R$ 45,90/mês             │ │ ◄─── Opção Alternativa
│ └─────────────────────────────────────┘ │
│                                         │
│ ┌─────────────────────────────────────┐ │
│ │   Iniciar Teste Grátis de 7 Dias    │ │ ◄─── CTA com desarmamento de risco
│ └─────────────────────────────────────┘ │
│ Cancele facilmente nas configurações.   │ ◄─── Microcopy legal explícito
└─────────────────────────────────────────┘
```
- **Anatomia**:
  1. Botão de fechar sutil e link obrigatório de "Restaurar Compras" no topo;
  2. Proposta de valor sintetizada em 3 a 4 benefícios tangíveis;
  3. Seletores de plano estruturados com destaque visual claro para o plano anual com maior desconto;
  4. Botão primário destacando o período de teste sem custo;
  5. Microcopy de conformidade jurídica explicando data de início de cobrança e facilidade de cancelamento.
- **Gatilho**: Tentativa de acesso a um recurso premium ou ao final do fluxo de boas-vindas.
- **Onde Encaixar**: Gateways de monetização de apps B2C e SaaS móvel.

---

#### Arquétipo 4: Floating Dynamic Island Tab Bar (Barra de Abas Flutuante)

```
┌─────────────────────────────────────────┐
│                                         │
│        [ CONTEÚDO DA TELA ATIVA ]       │
│                                         │
│                                         │
│     ┌─────────────────────────────┐     │
│     │   🏠    🔍    ⚡    💬    👤   │     │ ◄─── Cápsula flutuante arredondada
│     │  Home Busca Ações Chat Perfil│     │      com backdrop-blur-2xl e sombra
│     └─────────────────────────────┘     │
│                   ═══                   │ ◄─── Respiro acima da barra do sistema
└─────────────────────────────────────────┘
```
- **Anatomia**:
  1. Cápsula centralizada flutuando a 16px da margem inferior do sistema;
  2. Borda de 1px com gradiente sutil (`border-white/15`) e sombra suave de elevação;
  3. Ícones vetoriais com indicador de seleção animado (pílula deslizante via mola elástica);
  4. Micro-animação de escala (`whileTap: 0.85`) e vibração háptica tátil ao alternar abas.
- **Gatilho**: Sempre visível nas telas principais de navegação do aplicativo.
- **Onde Encaixar**: Navegação global em apps modernos com densidade de mídia ou leitura imersiva.

---

#### Arquétipo 5: Predictive Search Bar com Scoped Filter Chips

```
┌─────────────────────────────────────────┐
│ ┌─────────────────────────────────────┐ │
│ │ 🔍  Buscar transações, tags, apps...│ │ ◄─── Input com ícone de limpeza [✕]
│ └─────────────────────────────────────┘ │
│                                         │
│ [ Tudo ] [ Hoje ] [ Finanças ] [ Contratos ] ◄─── Chips horizontais de filtro
│                                         │
│ RECENTES                         Limpar │
│ 🕒 API Key de Produção                  │
│ 🕒 Reembolso Stripe                     │ ◄─── Histórico recente persistido
│                                         │
│ SUGESTÕES POPULARES                     │
│ 💡 Faturas pendentes de aprovação       │
└─────────────────────────────────────────┘
```
- **Anatomia**:
  1. Campo de busca com foco automático, botão de limpeza rápida e cancelamento animado;
  2. Carrossel horizontal de filtros categorizados instantâneos;
  3. Seção de histórico de pesquisas salvas em armazenamento local com opção de limpar;
  4. Sugestões preditivas em tempo real com realce em negrito do termo digitado.
- **Gatilho**: Toque no campo de busca ou aba de pesquisa dedicada.
- **Onde Encaixar**: Telas de descoberta, exploração de dados complexos e bibliotecas de conteúdo.

---

#### Arquétipo 6: Frictionless Auth Sequence (Passkey & Magic Link)

```
┌─────────────────────────────────────────┐
│ [←]                                     │
│                                         │
│   Acesse sua conta                      │
│   Entre instantaneamente sem senhas.    │
│                                         │
│ ┌─────────────────────────────────────┐ │
│ │ 👤  Continuar com Face ID / Passkey │ │ ◄─── Acesso nativo de biometria
│ └─────────────────────────────────────┘ │
│                                         │
│ ────────────── ou via e-mail ────────── │
│                                         │
│ ┌─────────────────────────────────────┐ │
│ │ nome@empresa.com                    │ │ ◄─── Input de e-mail com detecção
│ └─────────────────────────────────────┘ │
│                                         │
│ ┌─────────────────────────────────────┐ │
│ │       Enviar Link Mágico            │ │ ◄─── Envio de token sem senha
│ └─────────────────────────────────────┘ │
└─────────────────────────────────────────┘
```
- **Anatomia**:
  1. Priorização de autenticação biométrica via chaves de acesso nativas (WebAuthn / Passkeys);
  2. Divisor neutro com rótulo minimalista;
  3. Campo de e-mail com teclado específico (`type="email"` / `inputmode="email"`);
  4. Redirecionamento com verificação automática de link mágico (*Deep Linking*) sem necessidade de alternância manual de telas.
- **Gatilho**: Fluxo inicial de login do usuário.
- **Onde Encaixar**: Tela de entrada em produtos que priorizam máxima velocidade de acesso e segurança bancária.

---

#### Arquétipo 7: High-Empathy Educative Empty State

```
┌─────────────────────────────────────────┐
│                                         │
│               ┌─────────┐               │
│               │ 📦 ✨  │               │ ◄─── Ilustração monocromática expressiva
│               └─────────┘               │
│                                         │
│       Nenhum projeto ativo ainda        │ ◄─── Título claro sem termos técnicos
│   Crie seu primeiro espaço de trabalho  │
│   e convide membros da equipe para      │ ◄─── Explicação educativa em 2 linhas
│   começar a colaborar em tempo real.    │
│                                         │
│        ┌───────────────────────┐        │
│        │  + Criar Novo Projeto │        │ ◄─── Ação primária imediata
│        └───────────────────────┘        │
│          Ver tutoriais rápidos          │ ◄─── Ação secundária de aprendizado
│                                         │
└─────────────────────────────────────────┘
```
- **Anatomia**:
  1. Ícone ou ilustração sem ruído visual que contextualiza o vazio;
  2. Mensagem que elimina a culpa do usuário e instrui sobre o próximo passo natural;
  3. Botão de ação proativa focado em preencher aquele espaço vazio;
  4. Link discreto para documentação ou modelos predefinidos.
- **Gatilho**: Listas vazias, buscas sem resultados ou novos recursos não utilizados.
- **Onde Encaixar**: Telas de projetos, favoritos, carrinhos de compras e caixas de entrada.

---

#### Arquétipo 8: Sticky Action Dock com Dual Touch Target

```
┌─────────────────────────────────────────┐
│                                         │
│ [ CONTEÚDO ROLANTE DO PRODUTO / PEDIDO ]│
│                                         │
├─────────────────────────────────────────┤ ◄─── Divisor sutil superior
│ ┌──────┐ ┌────────────────────────────┐ │
│ │  🤍  │ │  Finalizar Pedido • R$ 89  │ │ ◄─── Dock fixo inferior ancorado
│ └──────┘ └────────────────────────────┘ │      acima da Safe Area do sistema
│                   ═══                   │
└─────────────────────────────────────────┘
```
- **Anatomia**:
  1. Barra fixa na base da janela com fundo sólido ou vidro fosco;
  2. Botão secundário de favoritar/salvar em formato quadrado de 48×48px;
  3. Botão primário largo incorporando o valor total ou estado imediato do pedido;
  4. Margem inferior automática via CSS `env(safe-area-inset-bottom)`.
- **Gatilho**: Telas de detalhe de produto em e-commerce e finalização de compras.
- **Onde Encaixar**: Rodapé de páginas transacionais com rolagem longa.

---

#### Arquétipo 9: Interactive Activity Feed com Swipe-to-Action

```
┌─────────────────────────────────────────┐
│ ATIVIDADE RECENTE                       │
│                                         │
│ ┌─────────────────────────────────────┐ │
│ │ [Avatar] Nova menção por @marcos    │ │
│ │ "Aprovamos o novo design system..." │ │
│ └─────────────────────────────────────┘ │
│                                         │
│ ◄── [ ARRASTAR PARA A ESQUERDA ]        │
│ ┌───────────────────────────┬─────────┐ │
│ │ [Avatar] Pull Request #42 │ 🗑️ Lixeira│ ◄── Ação destrutiva revelada
│ └───────────────────────────┴─────────┘ │
│                                         │
│ ┌─────────────────────────────────────┐ │
│ │ [Avatar] Pagamento recebido • R$ 4k │ │
│ └─────────────────────────────────────┘ │
└─────────────────────────────────────────┘
```
- **Anatomia**:
  1. Linhas de lista com avatar, cabeçalho e timestamp relativo ("há 5 min");
  2. Capacidade de arrastar o card para os lados (*Swipe Gestures*) com mola elástica;
  3. Revelação de botões de arquivamento rápido, marcar como lido ou exclusão com cores semânticas;
  4. Resposta háptica ao atingir o limiar de ativação automática do comando.
- **Gatilho**: Gerenciamento de notificações, tarefas ou e-mails em dispositivos móveis.
- **Onde Encaixar**: Centrais de notificação, listas de pendências e mensageiros.

---

#### Arquétipo 10: Grouped Cell Settings Hierarchy com Visual Feedback

```
┌─────────────────────────────────────────┐
│ AJUSTES DE CONTA                        │
│ ┌─────────────────────────────────────┐ │
│ │ 👤 Perfil Pessoal               [›] │ │ ◄── Célula com chevron indicador
│ ├─────────────────────────────────────┤ │
│ │ 🔒 Autenticação em 2 Etapas    Ativo│ │ ◄── Célula com estado semântico
│ ├─────────────────────────────────────┤ │
│ │ 🌙 Modo Escuro               [🟢 O] │ │ ◄── Célula com toggle nativo
│ └─────────────────────────────────────┘ │
│                                         │
│ PREFERÊNCIAS DO SISTEMA                 │
│ ┌─────────────────────────────────────┐ │
│ │ 🔔 Notificações Push            [›] │ │
│ ├─────────────────────────────────────┤ │
│ │ 🌐 Idioma                  Português│ │
│ └─────────────────────────────────────┘ │
└─────────────────────────────────────────┘
```
- **Anatomia**:
  1. Seções de lista agrupadas em caixas com cantos arredondados (`rounded-2xl`);
  2. Divisores internos de 1px recuados à esquerda para alinhar com o início do texto;
  3. Indicadores de navegação consistentes (`ChevronRight`), textos de estado ou chaves de seleção direta;
  4. Rótulos de cabeçalho em caixa alta com tamanho reduzido e cor atenuada.
- **Gatilho**: Configurações de perfil, preferências de aplicativo e opções do sistema.
- **Onde Encaixar**: Telas de configurações, gerenciamento de conta e painéis de preferências.

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Tokens CSS / Tailwind para Aplicações de Alta Fidelidade

Os tokens abaixo capturam os padrões exatos de superfícies semânticas, bordas ópticas, tipografia e raios de curvatura documentados nas interfaces mais refinadas do Mobbin:

```css
/* ==========================================================================
   MOBBIN PRODUCTION APP DESIGN TOKENS (Tailwind / CSS Variables)
   ========================================================================== */
:root {
  /* Canvas & Structural Backgrounds (Light Mode) */
  --app-bg: #F2F2F7;
  --surface-primary: #FFFFFF;
  --surface-secondary: #F8F9FA;
  --surface-tertiary: #E9ECEF;
  --surface-glass: rgba(255, 255, 255, 0.82);

  /* Borders & Optical Dividers */
  --border-subtle: rgba(60, 60, 67, 0.12);
  --border-strong: rgba(60, 60, 67, 0.25);
  --border-focus: #007AFF;

  /* Typography Colors */
  --text-primary: #000000;
  --text-secondary: #6C757D;
  --text-tertiary: #ADB5BD;
  --text-inverse: #FFFFFF;

  /* Brand & Action Accents */
  --accent-primary: #007AFF;
  --accent-hover: #0062CC;
  --accent-tint: rgba(0, 122, 255, 0.12);
  --accent-success: #34C759;
  --accent-destructive: #FF3B30;
  --accent-warning: #FF9500;

  /* Shadows (Tonal Native Elevation) */
  --shadow-sheet: 0 -10px 40px -10px rgba(0, 0, 0, 0.15);
  --shadow-card: 0 2px 8px -2px rgba(0, 0, 0, 0.08), 0 1px 3px 0 rgba(0, 0, 0, 0.04);
  --shadow-floating: 0 12px 32px -8px rgba(0, 0, 0, 0.18);

  /* Geometry & Radii */
  --radius-xs: 6px;
  --radius-sm: 10px;
  --radius-md: 14px;
  --radius-lg: 18px;
  --radius-xl: 24px;
  --radius-sheet: 32px;
  --radius-pill: 9999px;

  /* Safe Area Helpers */
  --safe-top: env(safe-area-inset-top, 20px);
  --safe-bottom: env(safe-area-inset-bottom, 34px);
}

/* Modo Escuro Nativo (OLED Black + Dark Glass) */
.dark {
  --app-bg: #000000;
  --surface-primary: #1C1C1E;
  --surface-secondary: #2C2C2E;
  --surface-tertiary: #3A3A3C;
  --surface-glass: rgba(28, 28, 30, 0.82);

  --border-subtle: rgba(255, 255, 255, 0.10);
  --border-strong: rgba(255, 255, 255, 0.20);
  --border-focus: #0A84FF;

  --text-primary: #FFFFFF;
  --text-secondary: #8E8E93;
  --text-tertiary: #636366;
  --text-inverse: #000000;

  --accent-primary: #0A84FF;
  --accent-hover: #409CFF;
  --accent-tint: rgba(10, 132, 255, 0.18);
  --accent-success: #30D158;
  --accent-destructive: #FF453A;
  --accent-warning: #FF9F0A;

  --shadow-sheet: 0 -10px 40px -10px rgba(0, 0, 0, 0.6);
  --shadow-card: 0 2px 8px -2px rgba(0, 0, 0, 0.4);
  --shadow-floating: 0 12px 32px -8px rgba(0, 0, 0, 0.5);
}
```

---

### 5.2 Calibração de Física de Movimento (Motion Specifications & Springs)

Para reproduzir a sensação tátil de um aplicativo móvel nativo em 120Hz (ProMotion), as animações devem evitar curvas lineares ou easing estático, utilizando modelos de mola física:

1. **Abertura de Bottom Sheet & Modais**:
   - `transition: { type: "spring", damping: 32, stiffness: 350, mass: 0.8 }`
   - Resposta imediata com rápida desaceleração elástica, sem rebotes exagerados.

2. **Feedback Tátil de Clique em Botões e Cards (`whileTap`)**:
   - `scale: 0.96` com `transition: { type: "spring", stiffness: 500, damping: 25 }`
   - Dá sensação instantânea de pressão física na superfície de vidro do smartphone.

3. **Troca de Abas em Segmented Controls (Shared Layout Transition)**:
   - `transition: { type: "spring", stiffness: 450, damping: 35 }`
   - O indicador de fundo desliza fluidamente entre as abas ativas sem qualquer atraso perceptual.

4. **Arrasto de Linhas em Listas (Swipe Gestures)**:
   - Limiar de ativação (*Drag Threshold*): `80px` com resistência elástica exponencial quando arrastado além do limite.

---

### 5.3 Implementação Funcional Completa em Código

Abaixo está o código de produção em **React 19, TypeScript, Tailwind CSS e Framer Motion** reproduzindo uma **Interface Completa com Onboarding, Segmented Tab Navigation, Bottom Sheet Interativo com arrasto por gestos e Paywall Modal**, sintetizando a experiência do Mobbin:

```tsx
import React, { useState } from "react";
import { motion, AnimatePresence, PanInfo } from "framer-motion";
import {
  Sparkles,
  CheckCircle2,
  Bell,
  CreditCard,
  ChevronRight,
  X,
  Shield,
  Layers,
  ArrowRight,
  TrendingUp,
  SlidersHorizontal,
  Smartphone,
  Star
} from "lucide-react";

// Tipos de Estado da Interface
type ActiveTab = "home" | "insights" | "settings";
type SheetState = "closed" | "collapsed" | "expanded";

export default function MobbinEngineShowcase() {
  const [activeTab, setActiveTab] = useState<ActiveTab>("home");
  const [isPaywallOpen, setIsPaywallOpen] = useState(false);
  const [sheetState, setSheetState] = useState<SheetState>("collapsed");
  const [selectedPlan, setSelectedPlan] = useState<"annual" | "monthly">("annual");
  const [notificationsEnabled, setNotificationsEnabled] = useState(false);

  // Manipulador de arraste do Bottom Sheet
  const handleSheetDragEnd = (event: MouseEvent | TouchEvent | PointerEvent, info: PanInfo) => {
    if (info.offset.y > 100 || info.velocity.y > 500) {
      setSheetState("closed");
    } else if (info.offset.y < -80 || info.velocity.y < -500) {
      setSheetState("expanded");
    } else {
      setSheetState("collapsed");
    }
  };

  return (
    <div className="min-h-screen bg-[#F2F2F7] dark:bg-black text-black dark:text-white font-sans antialiased flex justify-center items-center p-0 sm:p-6">
      {/* Moldura de Smartphone com Proporção iPhone 15 Pro (393x852) */}
      <div className="relative w-full max-w-[400px] h-[852px] bg-white dark:bg-[#121214] rounded-none sm:rounded-[48px] shadow-2xl border-0 sm:border-[8px] border-zinc-300 dark:border-zinc-800 overflow-hidden flex flex-col justify-between">
        
        {/* Dynamic Island / Status Bar Topo */}
        <div className="pt-3 px-6 flex justify-between items-center text-xs font-semibold z-40 bg-white/80 dark:bg-[#121214]/80 backdrop-blur-md">
          <span>9:41</span>
          <div className="h-4 w-28 bg-black dark:bg-zinc-800 rounded-full" />
          <div className="flex items-center gap-1.5">
            <span className="text-[10px]">5G</span>
            <div className="w-5 h-2.5 border border-current rounded-sm p-0.5 flex items-center">
              <div className="h-full w-3/4 bg-current rounded-2xs" />
            </div>
          </div>
        </div>

        {/* Navigation Bar Superior */}
        <header className="px-5 py-3 border-b border-zinc-200/80 dark:border-zinc-800/80 flex items-center justify-between bg-white/70 dark:bg-[#121214]/70 backdrop-blur-lg z-30">
          <div>
            <span className="text-[11px] font-semibold uppercase tracking-wider text-zinc-500">
              Workspace
            </span>
            <h1 className="text-xl font-bold tracking-tight">FinTech Pulse</h1>
          </div>
          <motion.button
            whileTap={{ scale: 0.92 }}
            onClick={() => setIsPaywallOpen(true)}
            className="flex items-center gap-1.5 px-3 py-1.5 rounded-full bg-blue-600/10 dark:bg-blue-500/20 text-blue-600 dark:text-blue-400 font-medium text-xs border border-blue-500/20"
          >
            <Sparkles className="w-3.5 h-3.5" />
            <span>Assinar Pro</span>
          </motion.button>
        </header>

        {/* Conteúdo Central Rolante */}
        <main className="flex-1 overflow-y-auto px-5 py-4 space-y-5 pb-24">
          {/* Segmented Control / Alternador de Abas */}
          <div className="p-1 rounded-xl bg-zinc-200/70 dark:bg-zinc-800/70 flex relative">
            {(["home", "insights", "settings"] as ActiveTab[]).map((tab) => {
              const isActive = activeTab === tab;
              const labels = { home: "Painel", insights: "Métricas", settings: "Ajustes" };
              return (
                <button
                  key={tab}
                  onClick={() => setActiveTab(tab)}
                  className={`flex-1 py-1.5 text-xs font-medium rounded-lg relative z-10 transition-colors ${
                    isActive ? "text-zinc-900 dark:text-white" : "text-zinc-500 hover:text-zinc-900"
                  }`}
                >
                  {isActive && (
                    <motion.div
                      layoutId="active-pill"
                      transition={{ type: "spring", stiffness: 450, damping: 35 }}
                      className="absolute inset-0 bg-white dark:bg-zinc-700 rounded-lg shadow-sm -z-10"
                    />
                  )}
                  {labels[tab]}
                </button>
              );
            })}
          </div>

          {/* Card de Proposta de Valor e Balanço */}
          <div className="p-5 rounded-2xl bg-gradient-to-br from-blue-600 to-indigo-700 text-white shadow-lg shadow-blue-500/20">
            <span className="text-xs opacity-80 font-medium">Patrimônio Líquido Monitorado</span>
            <div className="mt-1 flex items-baseline gap-2">
              <span className="text-3xl font-extrabold tracking-tight">R$ 148.520,00</span>
              <span className="text-xs font-semibold px-2 py-0.5 rounded-full bg-white/20 text-emerald-200 flex items-center gap-0.5">
                <TrendingUp className="w-3 h-3" /> +14.2%
              </span>
            </div>
            <p className="mt-3 text-xs text-blue-100">Atualizado há 4 minutos via sincronização Open Finance.</p>
          </div>

          {/* Grupo de Ações Rápidas */}
          <div>
            <h2 className="text-xs font-bold uppercase tracking-wider text-zinc-400 mb-2 px-1">
              Ações Transacionais
            </h2>
            <div className="grid grid-cols-3 gap-2.5">
              {[
                { label: "Transferir", icon: ArrowRight },
                { label: "Cartões", icon: CreditCard },
                { label: "Regras", icon: SlidersHorizontal }
              ].map((item, idx) => (
                <motion.button
                  key={idx}
                  whileTap={{ scale: 0.95 }}
                  className="p-3 rounded-xl bg-zinc-100 dark:bg-zinc-900/80 border border-zinc-200/80 dark:border-zinc-800 flex flex-col items-center justify-center gap-1.5 shadow-xs"
                >
                  <item.icon className="w-5 h-5 text-blue-600 dark:text-blue-400" />
                  <span className="text-xs font-medium text-zinc-700 dark:text-zinc-300">{item.label}</span>
                </motion.button>
              ))}
            </div>
          </div>

          {/* Lista de Células Agrupadas Estilo iOS */}
          <div>
            <h2 className="text-xs font-bold uppercase tracking-wider text-zinc-400 mb-2 px-1">
              Preferências & Governança
            </h2>
            <div className="rounded-2xl bg-zinc-100/90 dark:bg-zinc-900/80 border border-zinc-200/80 dark:border-zinc-800 divide-y divide-zinc-200 dark:divide-zinc-800 overflow-hidden">
              <div className="p-3.5 flex items-center justify-between">
                <div className="flex items-center gap-3">
                  <div className="p-2 rounded-lg bg-blue-500/10 text-blue-600 dark:text-blue-400">
                    <Bell className="w-4 h-4" />
                  </div>
                  <div>
                    <p className="text-xs font-semibold">Notificações Push</p>
                    <p className="text-[11px] text-zinc-500">Alertas críticos de transação</p>
                  </div>
                </div>
                {/* Switch Nativo */}
                <button
                  onClick={() => setNotificationsEnabled(!notificationsEnabled)}
                  className={`w-11 h-6 rounded-full transition-colors relative p-0.5 ${
                    notificationsEnabled ? "bg-emerald-500" : "bg-zinc-300 dark:bg-zinc-700"
                  }`}
                >
                  <motion.div
                    layout
                    transition={{ type: "spring", stiffness: 500, damping: 30 }}
                    className="w-5 h-5 rounded-full bg-white shadow-md"
                    style={{ marginLeft: notificationsEnabled ? "auto" : "0" }}
                  />
                </button>
              </div>

              <div
                onClick={() => setSheetState("collapsed")}
                className="p-3.5 flex items-center justify-between cursor-pointer hover:bg-zinc-200/50 dark:hover:bg-zinc-800/50 transition-colors"
              >
                <div className="flex items-center gap-3">
                  <div className="p-2 rounded-lg bg-emerald-500/10 text-emerald-600 dark:text-emerald-400">
                    <Shield className="w-4 h-4" />
                  </div>
                  <div>
                    <p className="text-xs font-semibold">Segurança & Criptografia</p>
                    <p className="text-[11px] text-zinc-500">Chaves de acesso Passkey ativas</p>
                  </div>
                </div>
                <ChevronRight className="w-4 h-4 text-zinc-400" />
              </div>
            </div>
          </div>
        </main>

        {/* Floating Island Dynamic Bottom Tab Bar */}
        <nav className="absolute bottom-5 inset-x-5 z-30">
          <div className="rounded-full bg-white/80 dark:bg-zinc-900/80 backdrop-blur-2xl border border-zinc-200/90 dark:border-zinc-700/80 shadow-xl px-6 py-2.5 flex items-center justify-between">
            <button
              onClick={() => setActiveTab("home")}
              className={`flex flex-col items-center gap-0.5 ${
                activeTab === "home" ? "text-blue-600 dark:text-blue-400" : "text-zinc-400"
              }`}
            >
              <Smartphone className="w-5 h-5" />
              <span className="text-[10px] font-semibold">App</span>
            </button>
            <button
              onClick={() => setSheetState(sheetState === "closed" ? "collapsed" : "expanded")}
              className="p-2.5 -mt-6 rounded-full bg-blue-600 text-white shadow-lg shadow-blue-500/40 hover:bg-blue-500 transition-colors"
            >
              <Layers className="w-5 h-5" />
            </button>
            <button
              onClick={() => setActiveTab("settings")}
              className={`flex flex-col items-center gap-0.5 ${
                activeTab === "settings" ? "text-blue-600 dark:text-blue-400" : "text-zinc-400"
              }`}
            >
              <SlidersHorizontal className="w-5 h-5" />
              <span className="text-[10px] font-semibold">Menu</span>
            </button>
          </div>
        </nav>

        {/* Interactive Bottom Sheet Modal */}
        <AnimatePresence>
          {sheetState !== "closed" && (
            <>
              {/* Backdrop Escuro */}
              <motion.div
                initial={{ opacity: 0 }}
                animate={{ opacity: 0.4 }}
                exit={{ opacity: 0 }}
                onClick={() => setSheetState("closed")}
                className="absolute inset-0 bg-black z-40"
              />

              {/* Superfície do Sheet com Drag Gestures */}
              <motion.div
                initial={{ y: "100%" }}
                animate={{ y: sheetState === "expanded" ? "15%" : "60%" }}
                exit={{ y: "100%" }}
                transition={{ type: "spring", damping: 30, stiffness: 350 }}
                drag="y"
                dragConstraints={{ top: 0, bottom: 0 }}
                onDragEnd={handleSheetDragEnd}
                className="absolute inset-x-0 bottom-0 top-0 bg-white dark:bg-zinc-900 rounded-t-[32px] border-t border-zinc-200 dark:border-zinc-800 p-5 z-50 shadow-2xl flex flex-col"
              >
                {/* Grab Handle */}
                <div className="w-10 h-1.5 bg-zinc-300 dark:bg-zinc-700 rounded-full mx-auto mb-4 cursor-grab active:cursor-grabbing" />

                <div className="flex items-center justify-between pb-3 border-b border-zinc-200 dark:border-zinc-800">
                  <h3 className="text-sm font-bold">Relatório Consolidado</h3>
                  <button
                    onClick={() => setSheetState("closed")}
                    className="p-1 rounded-full text-zinc-400 hover:text-zinc-700 dark:hover:text-white"
                  >
                    <X className="w-4 h-4" />
                  </button>
                </div>

                <div className="mt-4 space-y-3 overflow-y-auto flex-1">
                  <div className="p-3 rounded-xl bg-zinc-50 dark:bg-zinc-800/60 border border-zinc-200 dark:border-zinc-700/60">
                    <p className="text-xs font-semibold">Reserva de Emergência</p>
                    <p className="text-lg font-bold text-emerald-600 dark:text-emerald-400 mt-1">
                      100% Coberta (12 Meses)
                    </p>
                    <div className="w-full bg-zinc-200 dark:bg-zinc-700 h-2 rounded-full mt-2 overflow-hidden">
                      <div className="bg-emerald-500 h-full w-full rounded-full" />
                    </div>
                  </div>

                  <div className="p-3 rounded-xl bg-zinc-50 dark:bg-zinc-800/60 border border-zinc-200 dark:border-zinc-700/60">
                    <p className="text-xs font-semibold">Alocação de Investimentos</p>
                    <div className="mt-2 flex justify-between text-xs text-zinc-600 dark:text-zinc-400">
                      <span>Renda Fixa: 60%</span>
                      <span>Ações: 30%</span>
                      <span>Cripto: 10%</span>
                    </div>
                  </div>
                </div>
              </motion.div>
            </>
          )}
        </AnimatePresence>

        {/* Modal de Paywall Contextual (High-Converting Subscription) */}
        <AnimatePresence>
          {isPaywallOpen && (
            <motion.div
              initial={{ opacity: 0, scale: 0.95 }}
              animate={{ opacity: 1, scale: 1 }}
              exit={{ opacity: 0, scale: 0.95 }}
              transition={{ duration: 0.25, ease: [0.16, 1, 0.3, 1] }}
              className="absolute inset-0 bg-white dark:bg-zinc-950 z-50 p-6 flex flex-col justify-between"
            >
              <div>
                <div className="flex items-center justify-between">
                  <button
                    onClick={() => setIsPaywallOpen(false)}
                    className="p-1.5 rounded-full bg-zinc-100 dark:bg-zinc-800 text-zinc-500 hover:text-black dark:hover:text-white"
                  >
                    <X className="w-4 h-4" />
                  </button>
                  <button className="text-xs font-medium text-zinc-400 hover:text-zinc-600">
                    Restaurar
                  </button>
                </div>

                <div className="text-center mt-6">
                  <div className="w-12 h-12 rounded-2xl bg-blue-600/10 text-blue-600 dark:text-blue-400 mx-auto flex items-center justify-center mb-3">
                    <Star className="w-6 h-6 fill-current" />
                  </div>
                  <h2 className="text-2xl font-black tracking-tight">FinTech Pulse Pro</h2>
                  <p className="text-xs text-zinc-500 mt-1 max-w-xs mx-auto">
                    Conecte contas bancárias ilimitadas, gere relatórios fiscais automáticos e conte com consultoria por IA.
                  </p>
                </div>

                {/* Benefícios */}
                <div className="mt-6 space-y-2.5">
                  {[
                    "Sincronização em tempo real de 15 instituições",
                    "Previsão de fluxo de caixa com aprendizado de máquina",
                    "Exportação para CSV/Excel e contabilidade"
                  ].map((feat, i) => (
                    <div key={i} className="flex items-center gap-2.5 text-xs text-zinc-700 dark:text-zinc-300">
                      <CheckCircle2 className="w-4 h-4 text-emerald-500 shrink-0" />
                      <span>{feat}</span>
                    </div>
                  ))}
                </div>

                {/* Matriz de Planos */}
                <div className="mt-6 space-y-3">
                  <div
                    onClick={() => setSelectedPlan("annual")}
                    className={`p-3.5 rounded-2xl border-2 transition-all cursor-pointer flex items-center justify-between ${
                      selectedPlan === "annual"
                        ? "border-blue-600 bg-blue-50/50 dark:bg-blue-950/20"
                        : "border-zinc-200 dark:border-zinc-800"
                    }`}
                  >
                    <div>
                      <div className="flex items-center gap-2">
                        <span className="text-xs font-bold">Plano Anual</span>
                        <span className="text-[10px] font-bold px-2 py-0.5 rounded-full bg-emerald-500/10 text-emerald-600 dark:text-emerald-400">
                          Economize 40%
                        </span>
                      </div>
                      <p className="text-[11px] text-zinc-500 mt-0.5">R$ 19,90/mês (R$ 238,80 cobrado anualmente)</p>
                    </div>
                    <div className={`w-4 h-4 rounded-full border flex items-center justify-center ${
                      selectedPlan === "annual" ? "border-blue-600" : "border-zinc-400"
                    }`}>
                      {selectedPlan === "annual" && <div className="w-2 h-2 rounded-full bg-blue-600" />}
                    </div>
                  </div>

                  <div
                    onClick={() => setSelectedPlan("monthly")}
                    className={`p-3.5 rounded-2xl border-2 transition-all cursor-pointer flex items-center justify-between ${
                      selectedPlan === "monthly"
                        ? "border-blue-600 bg-blue-50/50 dark:bg-blue-950/20"
                        : "border-zinc-200 dark:border-zinc-800"
                    }`}
                  >
                    <div>
                      <span className="text-xs font-bold">Plano Mensal</span>
                      <p className="text-[11px] text-zinc-500 mt-0.5">R$ 34,90/mês cobrado a cada 30 dias</p>
                    </div>
                    <div className={`w-4 h-4 rounded-full border flex items-center justify-center ${
                      selectedPlan === "monthly" ? "border-blue-600" : "border-zinc-400"
                    }`}>
                      {selectedPlan === "monthly" && <div className="w-2 h-2 rounded-full bg-blue-600" />}
                    </div>
                  </div>
                </div>
              </div>

              {/* Botão de Ação & Microcopy */}
              <div className="pt-4 border-t border-zinc-200 dark:border-zinc-800">
                <motion.button
                  whileTap={{ scale: 0.97 }}
                  onClick={() => setIsPaywallOpen(false)}
                  className="w-full py-3.5 rounded-full bg-blue-600 hover:bg-blue-500 text-white font-bold text-xs shadow-lg shadow-blue-500/30 transition-colors"
                >
                  Experimentar Grátis por 7 Dias
                </motion.button>
                <p className="text-[10px] text-center text-zinc-400 mt-2">
                  Cancele a qualquer momento na App Store sem custos.
                </p>
              </div>
            </motion.div>
          )}
        </AnimatePresence>

        {/* Home Indicator Inferior do Dispositivo */}
        <div className="pb-2 pt-1 flex justify-center z-40 bg-white/50 dark:bg-[#121214]/50">
          <div className="w-32 h-1 bg-zinc-400/80 dark:bg-zinc-600 rounded-full" />
        </div>
      </div>
    </div>
  );
}
```

---

### 5.4 Como a IA Deve Pesquisar ao Vivo no Mobbin

Quando um agente de IA precisar coletar padrões de interface ou fluxos de conversão específicos em tempo real, ele deve consultar as rotas canônicas e a estrutura de filtros do Mobbin:

#### Tabela Canônica de Rotas e Parâmetros de Busca

| Eixo de Consulta | Rota Base no Mobbin | Exemplo Prático de URL para o Agente |
| :--- | :--- | :--- |
| **Biblioteca de Telas (iOS)** | `https://mobbin.com/browse/ios/screens` | `https://mobbin.com/browse/ios/screens` |
| **Biblioteca de Telas (Android)** | `https://mobbin.com/browse/android/screens` | `https://mobbin.com/browse/android/screens` |
| **Biblioteca de Telas (Web Apps)** | `https://mobbin.com/browse/web/screens` | `https://mobbin.com/browse/web/screens` |
| **Jornadas & Fluxos (iOS)** | `https://mobbin.com/browse/ios/flows` | `https://mobbin.com/browse/ios/flows` |
| **Jornadas & Fluxos (Web)** | `https://mobbin.com/browse/web/flows` | `https://mobbin.com/browse/web/flows` |
| **Componentes Atômicos (UI Elements)** | `https://mobbin.com/browse/ios/ui-elements` | `https://mobbin.com/browse/ios/ui-elements` |
| **Filtro por Categoria de App** | `https://mobbin.com/browse/<platform>/apps?category=<cat>` | `https://mobbin.com/browse/ios/apps?category=fintech`<br>`https://mobbin.com/browse/web/apps?category=productivity` |
| **Filtro por Tipo de Fluxo (Flow Type)** | `https://mobbin.com/browse/<platform>/flows?flow=<type>` | `https://mobbin.com/browse/ios/flows?flow=onboarding`<br>`https://mobbin.com/browse/ios/flows?flow=paywall`<br>`https://mobbin.com/browse/web/flows?flow=checkout` |
| **Filtro por Elemento Específico** | `https://mobbin.com/browse/<platform>/screens?element=<el>` | `https://mobbin.com/browse/ios/screens?element=bottom-sheets`<br>`https://mobbin.com/browse/ios/screens?element=segmented-controls` |
| **Busca Textual via OCR (Copy Search)** | `https://mobbin.com/search?q=<termo>&type=screens` | `https://mobbin.com/search?q=cancel+subscription&type=screens`<br>`https://mobbin.com/search?q=free+trial&type=screens` |

---

## 6. Diretrizes Prescritivas para o DESIGN_BLUEPRINT.md

Ao gerar o documento `DESIGN_BLUEPRINT.md` para qualquer aplicativo móvel ou aplicação web complexa que utilize o **Mobbin** como bússola de direção de arte e UX, a IA deve assegurar o cumprimento rigoroso dos itens abaixo:

### 6.1 Checklist de Conformidade Inegociável

- [ ] **Ergonomia do Polegar (Thumb Zone First)**: Todas as ações destrutivas ou primárias de navegação em telas móveis DEVEM estar localizadas nos 40% inferiores do viewport.
- [ ] **Áreas de Toque Mínimas (Touch Targets)**: Nenhum elemento clicável (botão, chip, ícone, toggle) pode ter área interativa menor que `44×44pt` no iOS ou `48×48dp` no Android.
- [ ] **Respeito às Áreas Seguras do Sistema**: Toda interface deve incorporar variáveis de ambiente nativas (`env(safe-area-inset-top)` e `env(safe-area-inset-bottom)`) para evitar sobreposição sobre o notch, Dynamic Island ou a barra do Home Indicator.
- [ ] **Regra 60-30-10 de Cores**: 60% de superfícies neutras de fundo, 30% de estrutura e tipografia legível, e estritamente 10% de cor de destaque para direcionar a atenção do usuário para a ação principal.
- [ ] **Mapeamento de Estados Nulos (Empty & Error States)**: Proibido entregar telas de listas ou formulários sem especificar visualmente o estado de carregamento esqueleto (*Skeleton Loader*), o estado de vazio (*Empty State*) e o tratamento de falha de conexão.
- [ ] **Prevenção de Perda de Foco em Modais**: Modais contextuais e Bottom Sheets DEVEM possuir botão explícito de fechamento e suporte a gesto de arrasto descendente para descartar.
- [ ] **Desarmamento de Ansiedade em Paywalls**: Toda tela de monetização DEVE conter: (1) O valor exato que será debitado, (2) A data de término do período de teste gratuito e (3) Link direto para "Restaurar Compras".

### 6.2 O Que é Terminantemente Proibido

- ❌ Animações de transição lentas superiores a `400ms` que causem sensação de lentidão na operação transacional diária.
- ❌ Modais encadeados que cobrem totalmente a tela sem permitir que o usuário veja de onde veio (*Loss of Context*).
- ❌ Solicitação abrupta de permissões nativas de sistema (câmera, contatos, notificações) logo na primeira tela sem antes explicar o benefício real que o usuário obterá (*Permission Priming Violation*).
- ❌ Tipografia com corpo menor que `11pt` em textos secundários ou menor que `14pt` em corpos de leitura corrida em telas móveis.
- ❌ Cores primárias de ação com contraste inferior a 4.5:1 em relação ao fundo imediato (violação da norma WCAG 2.1 nível AA).

### 6.3 Guia de Tom e Voz da UI (Clean UI Copy)

O estilo textual das interfaces catalogadas pelo Mobbin reflete clareza imediata, brevidade e alta empatia:
- **Títulos Claros em Vez de Jargões**: Em vez de *"Módulo de Pagamento Digital"*, use *"Formas de Pagamento"*. Em vez de *"Falha no Processamento 0x84"*, use *"Não foi possível conectar ao banco. Tente novamente em instantes"*.
- **Rótulos Focados em Conclusão de Ação**: Use verbos diretos no infinitivo nos botões: *"Confirmar Assinatura"*, *"Salvar Alterações"*, *"Continuar para o Pagamento"*.
- **Microcopy de Apoio Antifricção**: Sempre que uma ação envolver cartão de crédito ou compromisso financeiro, adicione uma linha de apoio com tamanho reduzido: *"Você não será cobrado hoje • Cancele quando quiser"*.
