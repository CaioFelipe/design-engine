---
id: "102-onepagelove"
name: "One Page Love"
url: "https://onepagelove.com/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico:
  - "Single-Page Narrative & Frictionless Continuous Scroll"
  - "High-Velocity Conversion & Radical Information Focus"
  - "Section-Level Modular Deconstruction (9,300+ Crops Archive)"
  - "Craft-First Micro-SaaS, Personal Portfolios & Product Launches"
  - "Human-Curated Typography & Typographic Specimen Showcases"
  - "Clean Floating Island Navigation & Anchor Synced Scrolling"
  - "AI-Native Integration (Official MCP Server & REST API)"
densidade_informacao: "Media/Narrativa (Escaneabilidade linear cirúrgica sem dispersão por sub-rotas)"
impacto_visual: "Minimalista/Silencioso a Editorial/Sofisticado"
custo_computacional: "Baixo a Moderado (CSS nativo para scroll suave e sticky positioning, Framer Motion para spring physics em toggles e micro-interações, carregamento progressivo e lazy loading de imagens)"
stack_frameworks:
  - "Next.js (App Router, SSG/SSR)"
  - "React 19 / TypeScript"
  - "Tailwind CSS v3 / v4 (container queries, CSS variables, subgrid)"
  - "Framer Motion / Motion.dev (layout animations, micro-springs tátil)"
  - "Radix UI / Headless UI / Lucide React (acessibilidade ARIA nativa)"
  - "Framer / Webflow / Carrd (ecossistemas dominantes de prototipagem e publicação de landing pages)"
compatibilidade:
  fontes_ideais:
    - "Neo-Grotesks Modernos de Engenharia & Legibilidade: Geist Sans, Inter, Plus Jakarta Sans, General Sans, Satoshi"
    - "Display Sans de Alta Identidade para Títulos Monolíticos: Cal Sans, Cabinet Grotesk, PP Neue Montreal, Clash Display, Space Grotesk"
    - "Monospace Técnica para Metadados, Badges e Métricas: Geist Mono, JetBrains Mono, Fira Code, IBM Plex Mono"
    - "Serifas Contemporâneas e Editoriais para Portfólios e Produtos Premium: Newsreader, Instrument Serif, Fraunces, Playfair Display"
  paletas_ideais:
    - "Paper Canvas & Minimal Ink (Austeridade Clássica de One-Pager): #FFFFFF (Pure Canvas), #FAFAFA (Subtle Zinc Base), #18181B (Zinc 900 Text), #71717A (Muted Subtext), #E4E4E7 (1px Hairline Border), #E04E4E (One Page Love Signature Coral Red Accent)"
    - "Modern Obsidian & Electric Cyber (SaaS / DevTools Single-Pager): #09090B (Deep Pitch Dark), #18181B (Card Background), #27272A (Hairline Border), #FAFAFA (Pure Light Text), #38BDF8 (Sky Blue Accent), #6366F1 (Indigo Glow)"
    - "Warm Cream & Minimal Luxury (Portfólios Criativos & Lojas D2C): #F7F5F0 (Warm Alabaster Canvas), #EFECE6 (Card Surface), #1C1A17 (Deep Espresso Ink), #D97706 (Amber / Gold Accent), #E2DDD5 (Warm Border)"
    - "Regra 60-30-10 de Conversão em Página Única: 60% Fundo Canvas Neutro (respiro contínuo e espaço negativo), 30% Estrutura Modular de Cartões e Tipografia Hierárquica em Alto Contraste, 10% Cor de Conversão Cirúrgica (Botão de CTA primário repetido nas extremidades, badges de lançamento e halos de foco)"
  combinacoes_recomendadas:
    - "Sticky Floating Navigation Island com `backdrop-blur-md` e compensação de `scroll-margin-top` nos IDs de seção"
    - "Micro-SaaS Hero com Headline monolítica, badge pílula de versão e formulário de inscrição direta em 1 campo de e-mail"
    - "Bento Grid modular de recursos com micro-telas de código e painéis interativos simulando a experiência do software"
    - "Tabela de preços com toggle Mensal/Anual sincronizado com badges flutuantes de desconto (-20% OFF)"
    - "FAQ estruturado em Accordion acessível com rotação suave de ícone de 180° e interpolação fluida de altura"
  conflitos_esteticos:
    - "Arquiteturas com múltiplos menus secundários aninhados ou páginas de destino separadas que forçam navegação externa e quebram o conceito de Single-Page"
    - "Scroll-jacking descalibrado que sequestra o scroll wheel do usuário e impede a velocidade de leitura natural"
    - "Formulários de captura longos (> 2 campos) na primeira dobra que adicionam atrito cognitivo fatal para produtos novos"
    - "Falta de sincronização entre o scroll e o estado da URL (links sem atualização dinâmica de hash via IntersectionObserver)"
    - "Animações espalhafatosas ou loaders de página inteira que atrasam o First Contentful Paint em conexões lentas"
    - "Imagens de banco fotográfico corporativo genérico (pessoas engravatadas em reuniões fingidas) em vez de capturas autênticas de tela ou fotografias autorais"
---

# One Page Love — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
 ██████╗ ███╗   ██╗███████╗    ██████╗  █████╗  ██████╗ ███████╗    ██╗      ██████╗ ██╗   ██╗███████╗
██╔═══██╗████╗  ██║██╔════╝    ██╔══██╗██╔══██╗██╔════╝██╔════╝    ██║     ██╔═══██╗██║   ██║██╔════╝
██║   ██║██╔██╗ ██║█████╗      ██████╔╝███████║██║  ███╗█████╗      ██║     ██║   ██║██║   ██║█████╗  
██║   ██║██║╚██╗██║██╔══╝      ██╔═══╝ ██╔══██║██║   ██║██╔══╝      ██║     ██║   ██║╚██╗ ██╔╝██╔══╝  
╚██████╔╝██║ ╚████║███████╗    ██║     ██║  ██║╚██████╔╝███████╗    ███████╗╚██████╔╝ ╚████╔╝ ███████╗
 ╚═════╝ ╚═╝  ╚═══╝╚══════╝    ╚═╝     ╚═╝  ╚═╝ ╚═════╝ ╚══════╝    ╚══════╝ ╚═════╝   ╚═══╝  ╚══════╝
```

---

## 1. DNA Estético & Filosofia de Curadoria

Fundado em **março de 2008** pelo designer, desenvolvedor e criador de produtos sul-africano **Rob Hope**, o **One Page Love** (`https://onepagelove.com/`) é o arquivo histórico global definitivo e a autoridade máxima em design de **websites de página única ("One Pagers")**, landing pages de alta conversão, portfólios profissionais compactos e templates arquiteturais.

Em meados de 2024, a plataforma foi adquirida pela **Some Studio**, sob liderança do designer alemão **Piet Terheyden** (fundador do influente *Minimal Gallery* e curador-chefe do *Minimalissimo*), consolidando uma transição que elevou ainda mais o rigor editorial e tipográfico da curadoria, mantendo viva a base de dados de mais de 16 anos.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        THE ONE PAGE LOVE CURATORIAL ECOSYSTEM                          │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  [ Single-Page Purity ]  ──► [ Granular Dissection ]  ──► [ AI-Native Exploration ]    │
│   • Continuous Scroll Flow    • 9,300+ Section Crops       • Official Claude/Cursor    │
│   • Zero Sub-Route Friction   • Typeface Taxonomy          • Free Streamable MCP       │
│   • Unified Value Delivery    • Real Color Sampling        • High-Throughput REST API  │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  TAXONOMIC PILLARS: Genre (20) | Style (24) | Platform (12) | Tech (8) | Sections (24) │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 O Que Define um "One Pager" Autêntico

Para a curadoria do One Page Love, um website de página única não é meramente um site sem links externos; é uma **filosofia arquitetural de design e comunicação**. 

Um One Pager autêntico caracteriza-se por:
1. **Ausência de Páginas Secundárias Tradicionais**: Todo o conteúdo necessário para educar, engajar e converter o visitante reside em **uma única página contínua**. Não existem rotas separadas do tipo `/about`, `/features`, `/pricing` ou `/contact`. 
2. **Navegação Baseada em Âncoras Fluidas (Anchor-Linked Flow)**: O menu superior (frequentemente implementado como uma *floating navigation island*) atua como um mapa de âncoras internas (`#overview`, `#features`, `#pricing`, `#faq`), permitindo navegação instantânea com rolagem suave sem recarregamento de página.
3. **Sequência Psicológica Ininterrupta**: A experiência de leitura é linear e orquestrada de cima para baixo. Não há dispersão de atenção: cada seção é um elo lógico que prepara o visitante para a próxima, culminando no Call-to-Action (CTA) definitivo.
4. **Resoluções Preservadas & Memória Histórica**: Com mais de 9.180 sites catalogados, o One Page Love mantém screenshots em resolução Retina @2x capturados no momento do lançamento, preservando a história do design mesmo quando produtos e startups encerram suas atividades ou mudam de domínio.

### 1.2 O Acervo de Seções (Section Inspiration Archive)

Um dos maiores diferenciais técnicos do One Page Love — e a razão pela qual engenheiros de software e designers de UI o utilizam diariamente — é a catalogação de mais de **9.390 recortes anatômicos de seções isoladas (`/sections`)**. Em vez de forçar o profissional a analisar páginas inteiras quando ele precisa apenas de uma referência para um componente específico, a plataforma decompõe as páginas nos seguintes blocos:
- **Social Proof & Client Logo Rows**: Grades de credibilidade, contadores de métricas e faixas monocromáticas de empresas parceiras.
- **Lead Capture & Waitlist Sections**: Módulos minimalistas de campo único projetados para captação de e-mails em pré-lançamentos.
- **Pricing Tables & Billing Switchers**: Matrizes comparativas de planos com toggles mensais/anuais e destaque claro para a camada Pro.
- **FAQ Accordions**: Módulos interativos para desarme de objeções com expansão fluida e zero poluição visual.
- **Device Mockups**: Apresentação de interfaces de produto emolduradas em displays de smartphones, tablets e notebooks com iluminação e reflexos calibrados.

### 1.3 Pioneirismo em Arquitetura para Inteligência Artificial (MCP & Trends API)

Diferente de galerias convencionais que erguem barreiras agressivas contra raspagem e automação, o One Page Love adotou uma postura abertamente **AI-First**:
- **One Page Love MCP (Model Context Protocol)**: Disponível publicamente no endpoint `https://api.onepagelove.com/mcp`, permite que agentes de IA como Claude Code, Claude.ai, Cursor, Windsurf e Codex realizem buscas semânticas em tempo real por gênero, cor, plataforma, tipografia e seções, recebendo capturas visuais inline para compor moodboards e blueprints instantâneos.
- **Trends REST API**: Endpoint estruturado (`https://onepagelove.com/api`) desenhado para alimentar agentes autônomos, motores de recomendação de design e modelos de linguagem com dados JSON canônicos e limpos.

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

O One Page Love deve ser a **Referência Primária de Direção de Arte e Arquitetura de Interface** nos seguintes contextos de projeto:

- **Lançamento de Micro-SaaS e Ferramentas para Desenvolvedores (DevTools)**: Quando o software tem uma proposição de valor cirúrgica e precisa provar sua utilidade em menos de 10 segundos, demonstrando o código ou interface na primeira dobra.
- **Portfólios de Engenheiros, Designers e Criadores Independentes**: Quando o profissional precisa de uma presença online de alto impacto que condense biografia, projetos selecionados, stack de ferramentas e canais de contato em um scroll sem atrito.
- **Landing Pages de Validação Rápida & Páginas de Lista de Espera (Waitlists / Beta Signups)**: Quando o objetivo é capturar interesse para uma startup nascente antes de investir meses na construção do software final.
- **Lançamento de Produtos Digitais Únicos (Infoprodutos, E-books, Cursos, Plugins e Fontes Tipográficas)**: Páginas focadas na venda direta de um único SKU com prova social massiva, prévias visuais e garantia explícita.
- **Eventos, Conferências, Hackathons e Webinars**: Páginas com data definida que necessitam de agenda horária, lista de palestrantes, mapa do local e ingressos em uma jornada direta.
- **Que Emoção Esse Estilo Comunica**: Transmite **foco radical, ausência de burocracia, agilidade executiva e elegância funcional**. Mostra ao visitante que o criador valoriza seu tempo e organizou a mensagem com máxima clareza e respeito à atenção humana.

### 2.1 Papel na Regra 60-30-10 de Cores & Layout

Em um One Pager de alta fidelidade catalogado pelo One Page Love, a distribuição cromática obedece rigorosamente à seguinte proporção:
- **60% — Canvas de Superfície Contínua**: Fundo alabastro limpo (`#FFFFFF` ou `#FAFAFA`) no modo claro, ou grafite obsidiano profundo (`#09090B` ou `#121214`) no modo escuro. O espaço negativo amplo e os respiros verticais entre seções (80px a 140px) compõem a base visual estável que evita a sensação de claustrofobia.
- **30% — Estrutura de Cartões, Linhas e Tipografia Hierárquica**: Bordas sutis de 1px (`rgba(0,0,0,0.08)` ou `rgba(255,255,255,0.08)`), cartões elevados de tom neutro, títulos monolíticos em peso pesado (`font-bold` ou `font-extrabold`) e textos de apoio em escala de cinza médio com legibilidade garantida.
- **10% — Acento Cirúrgico de Conversão**: Reservado exclusivamente para o Call-to-Action primário (o botão que realiza a ação desejada), badges de status de versão ("v2.0 Beta"), estrelas de avaliação e micro-indicadores luminosos. O coral avermelhado característico do One Page Love (`#E04E4E`) ou um azul elétrico cobalto exemplificam como esse acento nunca deve ser pulverizado aleatoriamente pela página.

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

### 3.1 Incompatibilidades Arquiteturais Críticas
- ⚠️ **Lojas Virtuais com Múltiplas Categorias e Catálogo Extenso (> 10 SKUs)**: Tentar comprimir centenas de produtos físicos em uma única página resulta em carregamento catastrófico de recursos, paginação quebrada e incapacidade de aplicar filtros complexos de facetas.
- ⚠️ **Portais de Documentação Técnica e Referência de API (Ex: Stripe Docs, AWS)**: Engenheiros necessitam de URLs permanentes, isoladas e indexáveis para cada endpoint, método e payload. Um layout de página única tornaria a consulta profunda impraticável.
- ⚠️ **Intranets Corporativas, Portais de RH e Sistemas Bancários Tradicionais**: Aplicações com fluxos regulatórios densos, relatórios financeiros anuais de centenas de páginas e auditorias formais exigem hierarquias de navegação multinível estritas.

### 3.2 Armadilhas de Imitação no Formato Single-Page (Anti-Padrões)

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        ONE-PAGER ANTI-PATTERNS & SOLUTIONS                             │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ ❌ Fadiga de Scroll Infinito     ──► ✅ Máximo de 6 a 8 seções com cadência rítmica   │
│ ❌ Sequestro de Scroll Wheel     ──► ✅ Inércia e velocidade de rolagem nativa         │
│ ❌ Navbar Fixa sem Compensação   ──► ✅ Uso obrigatório de 'scroll-margin-top'         │
│ ❌ Quebra do Botão "Voltar"      ──► ✅ Sincronização limpa de hash via History API    │
│ ❌ Excesso de Form Fields        ──► ✅ Máximo de 1 a 2 inputs no primeiro viewport   │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

1. **A Fadiga de Scroll por Falta de Curadoria**: O erro mais comum de amadores ao tentar construir um One Pager é acumular todas as ideias possíveis em uma sequência de 25 seções. O visitante perde a paciência na metade do percurso. A regra do One Page Love é a **concisão**: apresentar somente o ganho principal, os recursos-chave, a prova social irrefutável e a conversão.
2. **Scroll-Jacking Forçado**: Interceptar o scroll wheel do usuário para desacelerar, acelerar ou girar a tela artificialmente. Isso destrói a acessibilidade e frustra o usuário que deseja simplesmente escanear o conteúdo na sua própria velocidade.
3. **Sobreposição da Barra de Navegação Fixa sobre Títulos**: Omitir a propriedade CSS `scroll-margin-top` nos elementos de seção com ID. Quando o usuário clica em "#pricing", o título fica oculto sob a navbar flutuante, gerando uma experiência amadora.
4. **Desconexão do Histórico do Navegador**: Alterar o hash da URL sem atualizar o histórico suavemente ou manipular o histórico de forma descontrolada a cada 50 pixels rolados, impedindo que o usuário use o botão "Voltar" do navegador.
5. **Formulários Burocráticos na Primeira Dobra**: Solicitar nome, telefone, cargo, tamanho da empresa e faturamento antes mesmo de explicar o que o produto faz. Em páginas de página única, o Hero deve exigir no máximo um endereço de e-mail ou um botão direto de autenticação social (OAuth).

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                   ANATOMIA ARQUITETURAL DO ONE PAGER PERFEITO                          │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ [1. Floating Nav Island]   Logo Icon + Anchor Links (#feat, #faq) + Primary CTA Pill   │
│ [2. Hero Hook]             Badge 'v2.0 Beta' + H1 Monolítico + 1-Input Fast Form       │
│ [3. Social Proof Strip]    Infinite Monochromatic Marquee com Logotipos e Clientes     │
│ [4. Value Proposition]     3 Pilares Essenciais em Grid Horizontal Simétrico           │
│ [5. Feature Bento Showcase] Micro-UIs, Snippets de Código e Métricas Vivas em Cards     │
│ [6. 3-Step Sequential Flow] '01 Conecte' ──► '02 Configure' ──► '03 Automatize'         │
│ [7. Device Mockup Canvas]  Interface Emoldurada em Hardware Retina com Sombra Real     │
│ [8. Social Wall / Quotes]  Depoimentos Curtos com Foto Autêntica e Cargo Verificado    │
│ [9. Pricing Switcher Card] Toggle Mensal/Anual (-20%) + Tier Único ou Matriz 3 Colunas  │
│ [10. Objection FAQ]        Accordion Acessível Desarmando Incertezas de Pagamento      │
│ [11. Bottom Final Hook]    Chamada Final de Encerramento com CTA em Foco Total         │
│ [12. Minimal Colophon]     Status Dot 'Operational', Copyright e Links Sociais         │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo

1. **Largura de Container e Margens Laterais**:
   - Container central com largura máxima controlada entre `1080px` e `1180px` (`max-w-5xl` a `max-w-6xl` no Tailwind CSS). Em One Pagers, containers excessivamente largos dispersam o foco horizontal, prejudicando a leitura vertical fluida.
   - Margens de segurança laterais (*inline gutters*) com `clamp(1.25rem, 5vw, 3rem)`.
2. **Ritmo Vertical de Respiro (Breathing Cadence)**:
   - Seções separadas por respiros generosos de `96px` a `144px` (`py-24` a `py-36`).
   - O uso de divisores sutis em `1px solid var(--border-subtle)` demarca transições temáticas sem quebrar o fluxo linear de leitura.
3. **Escaneabilidade Linear**:
   - Cada seção deve poder ser compreendida em um relance de 3 segundos: título claro em H2, subtítulo descritivo em uma frase e componente visual autoexplicativo (cartão, tabela ou mockup).

### 4.2 Sistemas de Cores, Superfícies & Texturas

1. **Dualidade Alabastro vs. Obsidiano Puro**:
   - **Light Canvas**: Fundo em `#FFFFFF` ou `#FAFAFA`, cartões com fundo `#F4F4F5` ou branco puro com borda de 1px em `#E4E4E7` e sombras multicamadas ultrassuaves.
   - **Dark Canvas**: Fundo em `#09090B` (Zinco Profundo), cartões em `#18181B` com bordas de 1px em `rgba(255, 255, 255, 0.08)` e halos de luz radiais em opacidade de 12% a 18%.
2. **Texturas e Vidro Fosco (Specular Backdrop Blur)**:
   - Aplicação de `backdrop-blur-md` e `backdrop-saturate-150` na barra de navegação flutuante com fundo translúcido (`rgba(255,255,255,0.75)` no modo claro ou `rgba(9,9,11,0.75)` no modo escuro).

---

### 4.3 Catálogo Detalhado de 10 Padrões & Arquétipos Extraídos do One Page Love

#### Arquétipo 1: A Floating Navigation Island com Âncoras Ativas
- **Anatomia**:
  - Pílula flutuante centralizada no topo (`fixed top-4 left-1/2 -translate-x-1/2 z-50`), contendo logotipo icônico à esquerda, links de navegação âncora no centro (`#features`, `#workflow`, `#pricing`, `#faq`) e botão de ação compacto à direita.
  - O link ativo da seção visível no viewport é destacado visualmente em tempo real através da API nativa `IntersectionObserver`.
- **Gatilho de Interação**: Transição suave de fundo e sombra ao rolar além dos primeiros 20px da página.

#### Arquétipo 2: O Hero de Lançamento de Alta Velocidade (Fast-Capture Hero)
- **Anatomia**:
  - Badge pílula no topo: `[Disponível Agora] Lançamento Oficial v1.0 →`.
  - Título H1 monumental com entrelinha ajustada (`leading-[1.1]`), utilizando de 38px a 60px com quebra de linha deliberada para criar impacto emocional.
  - Subtítulo de suporte com exatamente duas linhas explicando a transformação objetiva trazida pelo produto.
  - Caixa de captura direta com 1 campo de e-mail e botão acoplado ("Garantir Acesso Imediato"), sem redirecionamentos intermediários.
  - Micro-cópia de desarmamento logo abaixo: *"Sem cartão de crédito • 14 dias de teste gratuito • Instalação em 2 minutos"*.
- **Gatilho de Interação**: Foco de input com expansão de halo luminoso suave (`ring-4 ring-coral/20`) e botão com micro-elevação ao pairar o cursor.

#### Arquétipo 3: A Faixa Contínua de Credibilidade (Infinite Client Marquee)
- **Anatomia**:
  - Texto de abertura em caixa alta e fonte monoespaçada: `CONFIADO POR MAIS DE 4.000 CRIADORES E STARTUPS`.
  - Carrossel infinito unidirecional com máscara gradiente nas bordas esquerda e direita (`mask-image: linear-gradient(to right, transparent, black 15%, black 85%, transparent)`), garantindo que os logos entrem e saiam suavemente sem cortes bruscos.
  - Logotipos monocromáticos em escala de cinza com opacidade de 50%.
- **Gatilho de Interação**: O carrossel desacelera ou pausa suavemente ao receber o cursor do usuário (`animation-play-state: paused`).

#### Arquétipo 4: O Fluxo Sequencial em 3 Passos (3-Step How-It-Works)
- **Anatomia**:
  - Grelha horizontal de 3 colunas numeradas de forma expressiva: `01`, `02`, `03` em tipografia monoespaçada ou display sutilmente atenuada.
  - Cada passo contém: Título de ação direto (*"01. Conecte seu repositório"*, *"02. Personalize seus tokens"*, *"03. Publique em 1 clique"*), acompanhado de uma frase explicativa concisa e um micro-diagrama vetorial.
  - Linhas tracejadas ou setas conectoras ligando os passos no desktop para guiar a leitura horizontal.
- **Gatilho de Interação**: Revelação progressiva (*stagger*) à medida que o scroll atinge o bloco.

#### Arquétipo 5: O Feature Bento Grid Compacto
- **Anatomia**:
  - Layout CSS Grid com 3 cartões principais:
    - Cartão 1 (Largura dupla): Prévia de interface interativa com dados reais ou editor simulado de código.
    - Cartão 2 (Coluna simples): Métrica de desempenho monumental (`<50ms`, `99.9% uptime`).
    - Cartão 3 (Coluna simples): Ícone de integração com ecossistemas (GitHub, Figma, Vercel).
- **Gatilho de Interação**: Borda com efeito especular iluminado que acompanha sutilmente a proximidade do cursor.

#### Arquétipo 6: O Device Mockup Canvas (Emolduramento de Software)
- **Anatomia**:
  - Interface do produto renderizada dentro de um contêiner vetorial fiel que simula a janela de um navegador moderno ou a tela de um smartphone.
  - Barra de título minimalista com 3 botões de controle de janela discretos (pontos cinzas em vez de cores de semáforo berrantes) e barra de endereço com URL estéril (`app.seuservico.com`).
  - Sombra difusa projetada multicamadas (`0 25px 50px -12px rgba(0, 0, 0, 0.25)`).
- **Gatilho de Interação**: Leve inclinação 3D sutil ao mover o cursor sobre o desktop (*perspective tilt effect*).

#### Arquétipo 7: A Parede de Prova Social com Citações Autênticas (Social Wall)
- **Anatomia**:
  - Grelha em estilo alvenaria (*masonry*) de 2 ou 3 colunas contendo relatos de clientes.
  - Cada cartão apresenta: Avatar fotográfico nítido de alta resolução, nome completo, cargo profissional e logotipo da empresa, estrelas de avaliação douradas e texto conciso com uma métrica de resultado destacada em negrito.
- **Gatilho de Interação**: Elevação táctil de 4 pixels no eixo Y ao passar o mouse com transição de 200ms.

#### Arquétipo 8: O Card de Precificação Transparente com Alternador Anual
- **Anatomia**:
  - Toggle centralizado no topo: `Faturamento Mensal` ⟷ `Faturamento Anual` (com badge chamativo de `-20% de economia`).
  - Cartão de preço destacado com selo *"Mais Popular"*, valor numérico de grande escala, lista de recursos essenciais com ícones de checagem limpos e botão largo de contratação.
  - Ausência de custos ocultos com texto explícito de política de reembolso de 30 dias logo abaixo.
- **Gatilho de Interação**: Animação física de troca numérica via Framer Motion ao alternar entre cobrança mensal e anual.

#### Arquétipo 9: O FAQ Accordion Minimalista para Neutralização de Objeções
- **Anatomia**:
  - Lista vertical de perguntas frequentes delimitadas por linhas finas de 1px.
  - As perguntas abordam as dúvidas reais que impedem a compra: *"Como funciona o suporte?"*, *"Posso cancelar a qualquer momento sem multas?"*, *"Existe período de teste gratuito?"*.
  - Ícone de chevron à direita com rotação de 180° fluida.
- **Gatilho de Interação**: Expansão do corpo da resposta com física de amortecimento suave sem trancos no layout.

#### Arquétipo 10: O Bottom Final Conversion Hook
- **Anatomia**:
  - Seção de fechamento antes do rodapé com fundo contrastante e zero distrações.
  - Headline direta: *"Comece a criar hoje mesmo. Sem barreiras."*
  - Botão de conversão primário com tamanho generoso e contraste total, idêntico à ação solicitada no Hero superior.
  - Micro-aviso de suporte humano em tempo real e tempo médio de resposta de menos de 10 minutos.
- **Gatilho de Interação**: Efeito sutil de pulso suave no botão para direcionar o foco do visitante.

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Física de Movimento: A Dinâmica da Conversão Fluida em Página Única

O One Page Love estabelece um equilíbrio fundamental entre **velocidade utilitária de resposta** e **fluidez rítmica de rolagem**. Páginas de página única não podem parecer estáticas como um documento PDF, nem lentas como uma animação cinematográfica de agência que sequestra o tempo do visitante.

- **Curvas de Bézier Primárias**:
  - `cubic-bezier(0.16, 1, 0.3, 1)`: Curva padrão de desaceleração orgânica (*ease-out*) utilizada para expansão de accordions, modais e transições de abas.
  - `cubic-bezier(0.25, 1, 0.5, 1)`: Curva de alta resposta para botões, inputs e micro-interações de hover.
- **Configurações de Mola Framer Motion (`type: "spring"`)**:
  - Para alternadores de preço (Monthly / Annual Toggle): `stiffness: 400`, `damping: 30`, `mass: 0.8`.
  - Para elevação de cards no hover: `stiffness: 300`, `damping: 20`.
  - Para abertura e fechamento de accordions: `stiffness: 280`, `damping: 28`.
- **Ancoragem Suave Nativa**:
  - O documento deve utilizar `html { scroll-behavior: smooth; }` combinado com a compensação precisa de espaçamento da barra fixa em cada seção:
    ```css
    [id] {
      scroll-margin-top: calc(var(--nav-height, 4rem) + 1.5rem);
    }
    ```

---

### 5.2 Tokens de Design em CSS (CSS Custom Properties)

```css
:root {
  /* Dimensões Arquiteturais */
  --container-max-width: 1140px;
  --nav-height: 4.25rem;
  --gutter-inline: clamp(1.25rem, 4vw, 2.5rem);
  --section-spacing-y: clamp(5rem, 8vw, 8rem);

  /* Superfícies & Canvas (Light Paper Base) */
  --bg-canvas: #FAFAFA;
  --bg-surface: #FFFFFF;
  --bg-surface-elevated: #F4F4F5;
  --bg-surface-glass: rgba(255, 255, 255, 0.85);

  /* Bordas e Divisores Estruturais */
  --border-hairline: #E4E4E7;
  --border-subtle: #F4F4F5;
  --border-focus: #18181B;

  /* Tinta e Tipografia */
  --text-primary: #18181B;
  --text-secondary: #71717A;
  --text-muted: #A1A1AA;

  /* Acentos de Conversão (One Page Love Coral & Electric Indigo) */
  --accent-brand: #E04E4E;       /* Coral Característico One Page Love */
  --accent-brand-hover: #C93B3B;
  --accent-brand-subtle: rgba(224, 78, 78, 0.1);
  --accent-success: #10B981;

  /* Tipografia do Ecossistema */
  --font-sans: "Geist Sans", "Inter", -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
  --font-mono: "Geist Mono", "JetBrains Mono", Menlo, monospace;

  /* Sombras Tácteis e Efeitos Especulares */
  --shadow-island: 0 10px 25px -5px rgba(0, 0, 0, 0.05), 0 8px 10px -6px rgba(0, 0, 0, 0.02);
  --shadow-card: 0 4px 6px -1px rgba(0, 0, 0, 0.05), 0 2px 4px -2px rgba(0, 0, 0, 0.03);
  --shadow-hover: 0 20px 25px -5px rgba(0, 0, 0, 0.08), 0 8px 10px -6px rgba(0, 0, 0, 0.04);
}

/* Modo Escuro Tecnológico (Dark Obsidian) */
[data-theme="dark"],
.dark {
  --bg-canvas: #09090B;
  --bg-surface: #121214;
  --bg-surface-elevated: #18181B;
  --bg-surface-glass: rgba(18, 18, 20, 0.85);

  --border-hairline: rgba(255, 255, 255, 0.08);
  --border-subtle: rgba(255, 255, 255, 0.04);
  --border-focus: #FAFAFA;

  --text-primary: #FAFAFA;
  --text-secondary: #A1A1AA;
  --text-muted: #71717A;

  --accent-brand: #E04E4E;
  --accent-brand-hover: #F26161;
  --accent-brand-subtle: rgba(224, 78, 78, 0.15);

  --shadow-island: 0 10px 25px -5px rgba(0, 0, 0, 0.5), 0 0 1px 1px rgba(255, 255, 255, 0.1);
  --shadow-card: 0 4px 12px rgba(0, 0, 0, 0.35);
  --shadow-hover: 0 20px 30px -10px rgba(0, 0, 0, 0.6);
}

/* Compensação Obrigatória para Âncoras Fluidas */
html {
  scroll-behavior: smooth;
}

[id] {
  scroll-margin-top: calc(var(--nav-height) + 1.5rem);
}
```

---

### 5.3 Receita de Código Funcional Completa em React + Tailwind + Framer Motion

O componente abaixo é um exemplo completo e pronto para produção de uma **Landing Page de Página Única ("One Pager")** de alta conversão, incorporando navegação em ilha flutuante sincronizada com o scroll, formulário rápido de 1 campo, bento grid modular, alternador de preços e accordion com animação fluida.

```tsx
import React, { useState, useEffect } from "react";
import { motion, AnimatePresence } from "framer-motion";
import { 
  ArrowRight, 
  Check, 
  ChevronDown, 
  Star, 
  Sparkles, 
  Code2, 
  Cpu, 
  ShieldCheck, 
  Zap, 
  Terminal, 
  Layers 
} from "lucide-react";

// DADOS DE FAQ PARA NEUTRALIZAÇÃO DE OBJEÇÕES
const FAQ_ITEMS = [
  {
    id: "faq-1",
    question: "Como funciona a garantia de satisfação de 30 dias?",
    answer: "Se você testar a nossa plataforma por 30 dias e achar que ela não acelerou o desenvolvimento do seu software, basta nos enviar um e-mail com 1 linha. Reembolsamos 100% do seu investimento sem perguntas ou burocracia."
  },
  {
    id: "faq-2",
    question: "Preciso cadastrar cartão de crédito para iniciar o teste?",
    answer: "Não. Você tem acesso completo e irrestrito ao plano Pro durante 14 dias sem necessidade de fornecer qualquer dado de pagamento."
  },
  {
    id: "faq-3",
    question: "Posso integrar com o meu fluxo de trabalho existente?",
    answer: "Absolutamente. O sistema conta com conectores nativos para GitHub, Vercel, Next.js, Figma e Tailwind CSS, além de uma API REST completa documentada."
  },
  {
    id: "faq-4",
    question: "Como é calculada a cobrança anual comparada à mensal?",
    answer: "Ao optar pelo pagamento anual, você recebe automaticamente um desconto de 20% aplicado sobre o valor total, equivalente a mais de 2 meses totalmente gratuitos."
  }
];

export default function OnePageShowcase() {
  const [activeSection, setActiveSection] = useState("hero");
  const [annualBilling, setAnnualBilling] = useState(true);
  const [openFaq, setOpenFaq] = useState<string | null>("faq-1");
  const [emailInput, setEmailInput] = useState("");
  const [formSubmitted, setFormSubmitted] = useState(false);

  // SINCRONIZAÇÃO DO MENU ATIVO COM A POSIÇÃO REAL DO SCROLL
  useEffect(() => {
    const sectionIds = ["hero", "features", "how-it-works", "pricing", "faq"];
    const handleScroll = () => {
      const scrollPosition = window.scrollY + 200;
      for (const id of sectionIds) {
        const element = document.getElementById(id);
        if (element) {
          const top = element.offsetTop;
          const height = element.offsetHeight;
          if (scrollPosition >= top && scrollPosition < top + height) {
            setActiveSection(id);
            break;
          }
        }
      }
    };

    window.addEventListener("scroll", handleScroll, { passive: true });
    return () => window.removeEventListener("scroll", handleScroll);
  }, []);

  const handleFormSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    if (emailInput.trim()) {
      setFormSubmitted(true);
    }
  };

  return (
    <div className="min-h-screen bg-[#FAFAFA] dark:bg-[#09090B] text-[#18181B] dark:text-[#FAFAFA] font-sans antialiased selection:bg-[#E04E4E]/20 selection:text-[#E04E4E]">
      
      {/* 1. FLOATING NAVIGATION ISLAND (ILHA FLUTUANTE CENTRALIZADA) */}
      <header className="fixed top-4 left-1/2 -translate-x-1/2 z-50 w-[92%] max-w-4xl">
        <nav className="px-4 py-2.5 rounded-full bg-white/85 dark:bg-[#18181B]/85 backdrop-blur-md border border-[#E4E4E7] dark:border-white/10 shadow-lg shadow-black/[0.04] flex items-center justify-between transition-all">
          
          {/* Logo & Marca */}
          <a href="#hero" className="flex items-center gap-2 font-bold text-sm tracking-tight text-neutral-900 dark:text-white">
            <span className="w-6 h-6 rounded-lg bg-[#E04E4E] flex items-center justify-center text-white text-xs font-black shadow-sm">
              ♥
            </span>
            <span>Kitsune<span className="text-[#E04E4E]">.io</span></span>
          </a>

          {/* Links Âncoras do Menu */}
          <div className="hidden md:flex items-center gap-1 text-xs font-medium text-[#71717A] dark:text-[#A1A1AA]">
            {[
              { id: "hero", label: "Início" },
              { id: "features", label: "Recursos" },
              { id: "how-it-works", label: "Como Funciona" },
              { id: "pricing", label: "Preços" },
              { id: "faq", label: "Dúvidas" },
            ].map((link) => (
              <a
                key={link.id}
                href={`#${link.id}`}
                className={`px-3 py-1.5 rounded-full transition-colors ${
                  activeSection === link.id
                    ? "text-[#18181B] dark:text-white bg-black/5 dark:bg-white/10 font-semibold"
                    : "hover:text-[#18181B] dark:hover:text-white hover:bg-black/[0.02] dark:hover:bg-white/[0.04]"
                }`}
              >
                {link.label}
              </a>
            ))}
          </div>

          {/* Botão de Ação Primária da Navbar */}
          <a
            href="#pricing"
            className="px-4 py-1.5 rounded-full text-xs font-semibold bg-[#18181B] dark:bg-white text-white dark:text-[#18181B] hover:bg-[#E04E4E] dark:hover:bg-[#E04E4E] dark:hover:text-white transition-all shadow-sm"
          >
            Começar Grátis
          </a>
        </nav>
      </header>

      {/* 2. HERO SECTION DE ALTA CONVERSÃO */}
      <section id="hero" className="pt-32 pb-20 md:pt-40 md:pb-28 px-6 max-w-5xl mx-auto text-center">
        
        {/* Badge Pílula de Novidade */}
        <div className="inline-flex items-center gap-2 px-3 py-1 rounded-full text-xs font-medium bg-[#E04E4E]/10 text-[#E04E4E] border border-[#E04E4E]/20 mb-6 animate-fade-in">
          <Sparkles className="w-3.5 h-3.5" />
          <span>Versão 2.4 com suporte nativo a MCP disponível</span>
          <ArrowRight className="w-3 h-3" />
        </div>

        {/* Título Monumental H1 */}
        <h1 className="text-4xl sm:text-6xl md:text-7xl font-extrabold tracking-tight text-[#18181B] dark:text-white max-w-4xl mx-auto leading-[1.08]">
          Construa landing pages de alta conversão em <span className="underline decoration-[#E04E4E] decoration-wavy decoration-2">minutos</span>.
        </h1>

        {/* Subtítulo de Duas Linhas */}
        <p className="mt-6 text-base sm:text-lg text-[#71717A] dark:text-[#A1A1AA] max-w-2xl mx-auto leading-relaxed">
          O kit definitivo de componentes Tailwind CSS e arquitetura de página única para fundadores, desenvolvedores e criadores que valorizam velocidade e design impecável.
        </p>

        {/* Formulário de Captura Rápida em 1 Campo */}
        <div className="mt-8 max-w-md mx-auto">
          {formSubmitted ? (
            <motion.div 
              initial={{ scale: 0.95, opacity: 0 }}
              animate={{ scale: 1, opacity: 1 }}
              className="p-4 rounded-2xl bg-emerald-500/10 border border-emerald-500/20 text-emerald-600 dark:text-emerald-400 text-sm font-semibold flex items-center justify-center gap-2"
            >
              <Check className="w-4 h-4" />
              <span>Inscrição confirmada! Verifique sua caixa de entrada.</span>
            </motion.div>
          ) : (
            <form onSubmit={handleFormSubmit} className="flex flex-col sm:flex-row gap-2">
              <input
                type="email"
                required
                value={emailInput}
                onChange={(e) => setEmailInput(e.target.value)}
                placeholder="seu.email@empresa.com"
                className="flex-1 px-4 py-3 rounded-xl border border-[#E4E4E7] dark:border-white/10 bg-white dark:bg-[#18181B] text-sm text-[#18181B] dark:text-white placeholder-[#A1A1AA] focus:outline-none focus:ring-2 focus:ring-[#E04E4E] transition-all"
              />
              <button
                type="submit"
                className="px-6 py-3 rounded-xl bg-[#E04E4E] hover:bg-[#C93B3B] text-white text-sm font-semibold transition-all shadow-md shadow-[#E04E4E]/25 flex items-center justify-center gap-2 group"
              >
                <span>Acessar Agora</span>
                <ArrowRight className="w-4 h-4 group-hover:translate-x-0.5 transition-transform" />
              </button>
            </form>
          )}

          <p className="mt-3 text-xs text-[#A1A1AA] dark:text-[#71717A]">
            14 dias grátis • Sem cartão de crédito • Cancele quando quiser
          </p>
        </div>

        {/* 3. DEVICE MOCKUP CANVAS (MOCKUP FRONTAL ELEVADO) */}
        <div className="mt-14 relative mx-auto rounded-2xl border border-[#E4E4E7] dark:border-white/10 bg-white dark:bg-[#121214] p-2 shadow-2xl shadow-black/10 overflow-hidden">
          <div className="flex items-center gap-1.5 px-3 py-2 border-b border-[#E4E4E7] dark:border-white/5 bg-[#FAFAFA] dark:bg-[#18181B] rounded-t-xl">
            <span className="w-2.5 h-2.5 rounded-full bg-neutral-300 dark:bg-neutral-700" />
            <span className="w-2.5 h-2.5 rounded-full bg-neutral-300 dark:bg-neutral-700" />
            <span className="w-2.5 h-2.5 rounded-full bg-neutral-300 dark:bg-neutral-700" />
            <div className="mx-auto text-[11px] font-mono text-[#A1A1AA] bg-white dark:bg-[#121214] px-4 py-0.5 rounded-md border border-[#E4E4E7] dark:border-white/5">
              https://app.kitsune.io/dashboard
            </div>
          </div>
          <div className="aspect-[16/9] w-full bg-neutral-100 dark:bg-[#09090B] flex flex-col items-center justify-center p-8 text-left">
            <div className="w-full max-w-lg space-y-4">
              <div className="h-4 bg-neutral-200 dark:bg-neutral-800 rounded w-1/3" />
              <div className="h-10 bg-white dark:bg-[#18181B] rounded-xl border border-neutral-200 dark:border-white/10 p-3 flex items-center justify-between">
                <span className="text-xs font-mono text-[#71717A]">npm install @kitsune/core</span>
                <span className="text-xs text-[#E04E4E] font-semibold">Copiar</span>
              </div>
              <div className="grid grid-cols-3 gap-3 pt-2">
                <div className="h-20 bg-white dark:bg-[#18181B] rounded-xl border border-neutral-200 dark:border-white/10 p-3">
                  <span className="text-[10px] text-[#A1A1AA] uppercase font-mono block">Deploy Time</span>
                  <span className="text-lg font-bold text-emerald-500">1.2s</span>
                </div>
                <div className="h-20 bg-white dark:bg-[#18181B] rounded-xl border border-neutral-200 dark:border-white/10 p-3">
                  <span className="text-[10px] text-[#A1A1AA] uppercase font-mono block">Bundle Size</span>
                  <span className="text-lg font-bold text-sky-500">4.8kb</span>
                </div>
                <div className="h-20 bg-white dark:bg-[#18181B] rounded-xl border border-neutral-200 dark:border-white/10 p-3">
                  <span className="text-[10px] text-[#A1A1AA] uppercase font-mono block">Lighthouse</span>
                  <span className="text-lg font-bold text-purple-500">100/100</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* 4. INFINITE CLIENT LOGO ROW (PROVA SOCIAL MONOCROMÁTICA) */}
      <section className="py-12 border-y border-[#E4E4E7] dark:border-white/5 bg-white/50 dark:bg-[#121214]/50">
        <div className="max-w-5xl mx-auto px-6 text-center">
          <p className="text-xs font-mono uppercase tracking-widest text-[#A1A1AA] mb-8">
            Adotado por engenheiros e designers em empresas inovadoras
          </p>
          <div className="flex flex-wrap items-center justify-center gap-8 md:gap-14 opacity-60 grayscale hover:grayscale-0 transition-all">
            {["Acme Corp", "Veloce Lab", "HyperScale", "Pulse UI", "Monolith Data", "NovaTech"].map((brand) => (
              <span key={brand} className="text-sm font-semibold tracking-tight text-[#71717A] dark:text-[#A1A1AA]">
                {brand}
              </span>
            ))}
          </div>
        </div>
      </section>

      {/* 5. BENTO GRID MODULAR DE RECURSOS */}
      <section id="features" className="py-24 px-6 max-w-5xl mx-auto">
        <div className="text-center max-w-2xl mx-auto mb-16">
          <h2 className="text-3xl sm:text-4xl font-extrabold tracking-tight">
            Tudo o que você precisa. Nada de excesso.
          </h2>
          <p className="mt-3 text-sm sm:text-base text-[#71717A] dark:text-[#A1A1AA]">
            Construído para remover distrações e conduzir o visitante diretamente ao valor do seu produto.
          </p>
        </div>

        <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
          
          {/* Card Destaque 2 Colunas */}
          <div className="md:col-span-2 p-8 rounded-3xl bg-white dark:bg-[#18181B] border border-[#E4E4E7] dark:border-white/10 shadow-sm flex flex-col justify-between">
            <div>
              <div className="w-10 h-10 rounded-xl bg-indigo-500/10 text-indigo-500 flex items-center justify-center mb-6">
                <Code2 className="w-5 h-5" />
              </div>
              <h3 className="text-xl font-bold mb-2">Arquitetura de Componentes Isolados</h3>
              <p className="text-sm text-[#71717A] dark:text-[#A1A1AA] leading-relaxed max-w-md">
                Mais de 30 módulos de seção independentes: Hero, Bento Grid, Tabelas de Preço, FAQ e Depoimentos, prontos para copiar e colar diretamente no seu projeto Next.js ou Vite.
              </p>
            </div>
            <div className="mt-8 p-4 rounded-xl bg-neutral-900 text-neutral-100 font-mono text-xs overflow-x-auto border border-white/5">
              <span className="text-purple-400">import</span> &#123; OnePageHero, PricingTable &#125; <span className="text-purple-400">from</span> <span className="text-emerald-400">"@kitsune/ui"</span>;
            </div>
          </div>

          {/* Card 1 Coluna: Performance */}
          <div className="p-8 rounded-3xl bg-white dark:bg-[#18181B] border border-[#E4E4E7] dark:border-white/10 shadow-sm flex flex-col justify-between">
            <div>
              <div className="w-10 h-10 rounded-xl bg-emerald-500/10 text-emerald-500 flex items-center justify-center mb-6">
                <Zap className="w-5 h-5" />
              </div>
              <h3 className="text-xl font-bold mb-2">Zero Inércia de Scroll</h3>
              <p className="text-sm text-[#71717A] dark:text-[#A1A1AA] leading-relaxed">
                Nenhum scroll-jacking. Respeito total à física nativa do sistema operacional com resposta instantânea de 120Hz.
              </p>
            </div>
            <div className="mt-8 text-3xl font-black text-emerald-500 tracking-tight">
              100% Nativo
            </div>
          </div>

          {/* Card 1 Coluna: MCP Server */}
          <div className="p-8 rounded-3xl bg-white dark:bg-[#18181B] border border-[#E4E4E7] dark:border-white/10 shadow-sm flex flex-col justify-between">
            <div>
              <div className="w-10 h-10 rounded-xl bg-[#E04E4E]/10 text-[#E04E4E] flex items-center justify-center mb-6">
                <Terminal className="w-5 h-5" />
              </div>
              <h3 className="text-xl font-bold mb-2">Pronto para Agentes de IA</h3>
              <p className="text-sm text-[#71717A] dark:text-[#A1A1AA] leading-relaxed">
                Compatibilidade nativa com MCP para Claude Code, Cursor e Copilot inspecionarem o design diretamente.
              </p>
            </div>
            <div className="mt-8 font-mono text-xs text-[#E04E4E]">
              claude mcp add kitsune
            </div>
          </div>

          {/* Card Destaque 2 Colunas: Tipografia e Acessibilidade */}
          <div className="md:col-span-2 p-8 rounded-3xl bg-white dark:bg-[#18181B] border border-[#E4E4E7] dark:border-white/10 shadow-sm flex flex-col justify-between">
            <div>
              <div className="w-10 h-10 rounded-xl bg-sky-500/10 text-sky-500 flex items-center justify-center mb-6">
                <ShieldCheck className="w-5 h-5" />
              </div>
              <h3 className="text-xl font-bold mb-2">Conformidade Acessível WCAG AA</h3>
              <p className="text-sm text-[#71717A] dark:text-[#A1A1AA] leading-relaxed max-w-md">
                Foco visualmente explícito, contrastes de texto matematicamente validados e suporte a leitores de tela com atributos WAI-ARIA nativos em todos os componentes.
              </p>
            </div>
            <div className="mt-6 flex items-center gap-4 text-xs font-mono text-[#71717A]">
              <span className="flex items-center gap-1.5"><Check className="w-3.5 h-3.5 text-emerald-500" /> Contraste 7:1</span>
              <span className="flex items-center gap-1.5"><Check className="w-3.5 h-3.5 text-emerald-500" /> Suporte a Teclado</span>
              <span className="flex items-center gap-1.5"><Check className="w-3.5 h-3.5 text-emerald-500" /> Sem Layout Shift</span>
            </div>
          </div>

        </div>
      </section>

      {/* 6. HOW IT WORKS EM 3 ETAPAS SEQUENCIAIS */}
      <section id="how-it-works" className="py-24 px-6 border-t border-[#E4E4E7] dark:border-white/5 bg-white/40 dark:bg-[#121214]/40">
        <div className="max-w-5xl mx-auto">
          <div className="text-center max-w-xl mx-auto mb-16">
            <span className="text-xs font-mono text-[#E04E4E] uppercase tracking-widest block mb-2">
              Jornada Simplificada
            </span>
            <h2 className="text-3xl font-extrabold tracking-tight">Do Zero ao Ar em Três Passos</h2>
          </div>

          <div className="grid grid-cols-1 md:grid-cols-3 gap-8 relative">
            {[
              {
                step: "01",
                title: "Selecione o Modelo",
                desc: "Escolha um arquétipo validado da curadoria adaptado ao seu tipo específico de produto ou serviço."
              },
              {
                step: "02",
                title: "Ajuste os Tokens",
                desc: "Defina sua paleta de cores, tipografia e copie o conteúdo usando nosso guia de Clean UI Copy."
              },
              {
                step: "03",
                title: "Publique e Converta",
                desc: "Faça deploy em 1 clique na Vercel ou Cloudflare Pages com tempo de carregamento inferior a 1 segundo."
              }
            ].map((item) => (
              <div key={item.step} className="p-8 rounded-2xl bg-white dark:bg-[#18181B] border border-[#E4E4E7] dark:border-white/10 shadow-sm relative">
                <span className="text-4xl font-extrabold text-[#E04E4E]/20 font-mono block mb-4">
                  {item.step}
                </span>
                <h3 className="text-lg font-bold mb-2">{item.title}</h3>
                <p className="text-xs sm:text-sm text-[#71717A] dark:text-[#A1A1AA] leading-relaxed">
                  {item.desc}
                </p>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* 7. MATRIZ DE PRECIFICAÇÃO COM TOGGLE ANUAL */}
      <section id="pricing" className="py-24 px-6 max-w-5xl mx-auto text-center">
        <div className="max-w-xl mx-auto mb-12">
          <h2 className="text-3xl sm:text-4xl font-extrabold tracking-tight">Preço Único e Transparente</h2>
          <p className="mt-3 text-sm text-[#71717A] dark:text-[#A1A1AA]">
            Sem assinaturas complexas ou taxas ocultas de renovação.
          </p>

          {/* Billing Switcher */}
          <div className="mt-8 inline-flex items-center gap-3 p-1 rounded-full bg-neutral-200/60 dark:bg-neutral-800 border border-neutral-300/50 dark:border-white/5">
            <button
              onClick={() => setAnnualBilling(false)}
              className={`px-4 py-1.5 rounded-full text-xs font-semibold transition-all ${
                !annualBilling 
                  ? "bg-white dark:bg-[#18181B] text-[#18181B] dark:text-white shadow-sm" 
                  : "text-[#71717A] hover:text-[#18181B] dark:hover:text-white"
              }`}
            >
              Mensal
            </button>
            <button
              onClick={() => setAnnualBilling(true)}
              className={`px-4 py-1.5 rounded-full text-xs font-semibold flex items-center gap-1.5 transition-all ${
                annualBilling 
                  ? "bg-white dark:bg-[#18181B] text-[#18181B] dark:text-white shadow-sm" 
                  : "text-[#71717A] hover:text-[#18181B] dark:hover:text-white"
              }`}
            >
              <span>Anual</span>
              <span className="px-1.5 py-0.5 rounded-md text-[10px] bg-[#E04E4E]/10 text-[#E04E4E] font-bold">
                -20%
              </span>
            </button>
          </div>
        </div>

        {/* Card de Preço em Destaque */}
        <div className="max-w-md mx-auto p-8 rounded-3xl bg-white dark:bg-[#18181B] border-2 border-[#E04E4E] shadow-xl shadow-[#E04E4E]/10 relative text-left">
          <div className="absolute -top-3.5 left-1/2 -translate-x-1/2 px-3 py-1 rounded-full bg-[#E04E4E] text-white text-[11px] font-bold uppercase tracking-wider shadow-sm">
            Plano Completo
          </div>

          <div className="flex items-baseline gap-2 mb-4">
            <span className="text-4xl sm:text-5xl font-extrabold tracking-tight text-[#18181B] dark:text-white">
              {annualBilling ? "R$ 39" : "R$ 49"}
            </span>
            <span className="text-xs text-[#71717A] font-medium">/ mês faturado anualmente</span>
          </div>

          <p className="text-xs text-[#71717A] dark:text-[#A1A1AA] pb-6 border-b border-[#E4E4E7] dark:border-white/10">
            Acesso irrestrito a todos os componentes, templates e atualizações contínuas para sempre.
          </p>

          <ul className="py-6 space-y-3 text-xs text-[#18181B] dark:text-neutral-200">
            {[
              "30+ Módulos de Seção em React & Tailwind",
              "Suporte oficial ao servidor MCP de IA",
              "Garantia incondicional de 30 dias",
              "Atualizações de segurança e código perpétuas",
              "Código fonte 100% aberto sem licença de royalties"
            ].map((feat) => (
              <li key={feat} className="flex items-center gap-2.5">
                <Check className="w-4 h-4 text-[#E04E4E] shrink-0" />
                <span>{feat}</span>
              </li>
            ))}
          </ul>

          <button className="w-full py-3.5 rounded-xl bg-[#E04E4E] hover:bg-[#C93B3B] text-white text-sm font-semibold transition-all shadow-md shadow-[#E04E4E]/25 text-center block">
            Começar Agora com 30 Dias de Garantia
          </button>
        </div>
      </section>

      {/* 8. FAQ ACCORDION DE NEUTRALIZAÇÃO DE OBJEÇÕES */}
      <section id="faq" className="py-24 px-6 border-t border-[#E4E4E7] dark:border-white/5 bg-white/40 dark:bg-[#121214]/40">
        <div className="max-w-2xl mx-auto">
          <div className="text-center mb-14">
            <h2 className="text-3xl font-extrabold tracking-tight">Perguntas Frequentes</h2>
            <p className="mt-2 text-sm text-[#71717A] dark:text-[#A1A1AA]">
              Respostas diretas para dúvidas técnicas e comerciais.
            </p>
          </div>

          <div className="space-y-3">
            {FAQ_ITEMS.map((item) => {
              const isOpen = openFaq === item.id;
              return (
                <div
                  key={item.id}
                  className="rounded-2xl border border-[#E4E4E7] dark:border-white/10 bg-white dark:bg-[#18181B] overflow-hidden transition-colors"
                >
                  <button
                    onClick={() => setOpenFaq(isOpen ? null : item.id)}
                    className="w-full px-6 py-4 flex items-center justify-between text-left text-sm font-semibold text-[#18181B] dark:text-white focus:outline-none"
                  >
                    <span>{item.question}</span>
                    <motion.div
                      animate={{ rotate: isOpen ? 180 : 0 }}
                      transition={{ duration: 0.2 }}
                      className="shrink-0 ml-4"
                    >
                      <ChevronDown className="w-4 h-4 text-[#71717A]" />
                    </motion.div>
                  </button>
                  <AnimatePresence>
                    {isOpen && (
                      <motion.div
                        initial={{ height: 0, opacity: 0 }}
                        animate={{ height: "auto", opacity: 1 }}
                        exit={{ height: 0, opacity: 0 }}
                        transition={{ duration: 0.25, ease: [0.16, 1, 0.3, 1] }}
                      >
                        <div className="px-6 pb-5 text-xs text-[#71717A] dark:text-[#A1A1AA] leading-relaxed border-t border-[#E4E4E7]/60 dark:border-white/5 pt-3">
                          {item.answer}
                        </div>
                      </motion.div>
                    )}
                  </AnimatePresence>
                </div>
              );
            })}
          </div>
        </div>
      </section>

      {/* 9. BOTTOM FINAL CONVERSION HOOK */}
      <section className="py-24 px-6 text-center bg-[#18181B] text-white relative overflow-hidden">
        <div className="max-w-3xl mx-auto relative z-10">
          <h2 className="text-3xl sm:text-5xl font-extrabold tracking-tight leading-tight">
            Pronto para lançar seu produto em tempo recorde?
          </h2>
          <p className="mt-4 text-sm sm:text-base text-neutral-400 max-w-xl mx-auto">
            Junte-se a milhares de criadores independentes que publicam landing pages focadas e elegantes com o Kitsune.
          </p>
          <div className="mt-8 flex flex-col sm:flex-row items-center justify-center gap-4">
            <a
              href="#pricing"
              className="w-full sm:w-auto px-8 py-3.5 rounded-xl text-sm font-semibold bg-[#E04E4E] hover:bg-[#C93B3B] text-white shadow-xl shadow-[#E04E4E]/30 transition-all"
            >
              Criar Minha Landing Page Agora
            </a>
            <a
              href="#features"
              className="w-full sm:w-auto px-8 py-3.5 rounded-xl text-sm font-medium border border-white/10 hover:bg-white/5 text-white transition-all"
            >
              Explorar Todos os Recursos
            </a>
          </div>
          <p className="mt-4 text-xs text-neutral-500">
            Acesso instantâneo • Garantia incondicional de reembolso em 30 dias
          </p>
        </div>
      </section>

      {/* 10. MINIMAL COLOPHON FOOTER */}
      <footer className="py-12 border-t border-[#E4E4E7] dark:border-white/5 bg-white dark:bg-[#09090B] text-xs text-[#71717A]">
        <div className="max-w-5xl mx-auto px-6 flex flex-col sm:flex-row items-center justify-between gap-6">
          <div className="flex items-center gap-2.5">
            <span className="w-2 h-2 rounded-full bg-emerald-500 animate-pulse" />
            <span className="font-semibold text-[#18181B] dark:text-white">Todos os sistemas operacionais</span>
          </div>

          <div className="flex items-center gap-6">
            <a href="#hero" className="hover:text-[#18181B] dark:hover:text-white transition-colors">Voltar ao Topo ↑</a>
            <a href="#pricing" className="hover:text-[#18181B] dark:hover:text-white transition-colors">Preços</a>
            <a href="#faq" className="hover:text-[#18181B] dark:hover:text-white transition-colors">Perguntas Frequentes</a>
          </div>

          <p>© 2026 Kitsune Design Engine. Inspirado na curadoria do One Page Love.</p>
        </div>
      </footer>

    </div>
  );
}
```

---

### 5.4 Como a IA Deve Pesquisar ao Vivo no One Page Love

O One Page Love é uma das raras plataformas de design que oferecem suporte de **primeira classe para agentes de inteligência artificial**, disponibilizando tanto um protocolo nativo de MCP quanto uma API REST estruturada e URLs canônicas limpas.

#### 1. Integração Direta via Servidor MCP (Model Context Protocol)

O servidor oficial MCP do One Page Love opera através de transporte HTTP sem necessidade de chave de API privada:

- **Endpoint Oficial**: `https://api.onepagelove.com/mcp`
- **Configuração no Claude Code / Cursor / Windsurf**:
  ```json
  {
    "mcpServers": {
      "onepagelove": {
        "url": "https://api.onepagelove.com/mcp"
      }
    }
  }
  ```
- **Ferramenta Única Exposta (`search`)**: O agente pode formular solicitações compostas combinando múltiplos eixos de taxonomia (ex: `genre="portfolio"`, `style="minimal"`, `platform="framer"`, `tech="tailwind"`). Os resultados retornam com capturas de tela inline em alta resolução, link de permalink no arquivo e URL do site ao vivo.

#### 2. Endpoints da REST API Oficial

- **Documentação**: `https://api.onepagelove.com/docs`
- **Busca Estruturada**: `https://api.onepagelove.com/v1/search?genre={slug}&style={slug}&section={slug}`

#### 3. Tabela Canônica de URLs e Filtros para Navegação Web do Agente

Quando o agente precisar inspecionar referências diretamente via web ou requisições HTTP normais, ele deve utilizar a seguinte sintaxe canônica:

| Eixo de Pesquisa | Rota Direta no One Page Love | Exemplos Concretos de Slugs Válidos |
| :--- | :--- | :--- |
| **Gênero / Categoria** | `https://onepagelove.com/genre/<slug>` | `portfolio`, `landing-page`, `product`, `launching-soon`, `app`, `service`, `personal`, `event`, `informational`, `saas`, `startup` |
| **Seções Específicas** | `https://onepagelove.com/section/<slug>` | `social-proof`, `leads`, `testimonials`, `faq-accordion`, `pricing`, `pricing-table`, `team`, `client-logos`, `mockup-device`, `how-it-works` |
| **Estilos Visuais** | `https://onepagelove.com/style/<slug>` | `minimal`, `illustrative`, `scroll-effects`, `flat-design`, `typographic`, `brutalism`, `modular`, `glassmorphism`, `gradients` |
| **Plataformas de Construção** | `https://onepagelove.com/platform/<slug>` | `framer`, `webflow`, `wordpress`, `carrd`, `squarespace`, `readymag`, `elementor`, `wix` |
| **Tecnologias de Código** | `https://onepagelove.com/tech/<slug>` | `tailwind`, `next-js`, `gsap`, `shadcn-ui`, `lottie-animations`, `three-js`, `vuejs` |
| **Templates Prontos** | `https://onepagelove.com/templates` | `?pricing=free`, `?pricing=premium`, `/landing-page-templates`, `/portfolio-templates` |
| **Catálogo de Tipografias** | `https://onepagelove.com/typefaces` | Exemplos reais de uso de Geist Sans, Inter, Cal Sans, PP Neue Montreal |
| **Busca Textual Direta** | `https://onepagelove.com/?s=<query>` | `?s=minimal+saas+dark`, `?s=ai+developer+tool` |

#### Exemplos Prontos de Queries para o Agente de IA:
- **Landing Page Minimalista de SaaS em Framer**:  
  `https://onepagelove.com/genre/saas?style=minimal&platform=framer`
- **Exemplos de Tabelas de Preço de Alta Conversão**:  
  `https://onepagelove.com/section/pricing-table`
- **Páginas de Lista de Espera / Lançamento de IA**:  
  `https://onepagelove.com/genre/launching-soon?tech=tailwind`
- **Portfólios Pessoais em Dark Mode**:  
  `https://onepagelove.com/genre/portfolio?style=minimal`

---

## 6. Diretrizes Prescritivas para o DESIGN_BLUEPRINT.md

Ao elaborar o arquivo `DESIGN_BLUEPRINT.md` para qualquer aplicação web ou produto comercial cuja direção de arte adote o **One Page Love** como padrão de excelência, o agente de inteligência artificial deve seguir rigorosamente as regras abaixo:

### 6.1 Checklist de Conformidade Inegociável

- [ ] **Unicidade de Rota (Single Route)**: Toda a proposta de valor, recursos, validação e conversão DEVEM ocorrer na rota raiz `/`. É terminantemente proibido criar sub-páginas como `/sobre` ou `/precos` que fragmentem a narrativa.
- [ ] **Floating Island Navigation com Âncoras Ativas**: A barra de navegação superior DEVE ser implementada como uma ilha flutuante centralizada ou fixa com `backdrop-blur`, contendo links de âncora (`#features`, `#pricing`, `#faq`) e atualizando dinamicamente a classe ativa de acordo com a posição real de rolagem via `IntersectionObserver`.
- [ ] **Compensação Obrigatória de Âncoras**: Todos os elementos que possuem ID de seção DEVEM conter `scroll-margin-top: calc(var(--nav-height) + 1.5rem)` em seu CSS para garantir que a navbar não oculte títulos ao navegar por âncoras.
- [ ] **The 5-Second Value Hook**: O Hero DEVE conter um título H1 e subtítulo que respondam a três perguntas em menos de 5 segundos: O que é? Para quem serve? Qual métrica ou benefício transforma?
- [ ] **Captura Sem Fricção**: O formulário do Hero inicial DEVE conter no máximo 1 campo (e-mail) com botão integrado. É proibido exigir cadastro completo, telefone ou senhas na primeira dobra.
- [ ] **Prova Social no Primeiro Viewport**: Pelo menos uma linha de credibilidade (logotipos de clientes, contagem de usuários ativos ou citação influente) DEVE estar visível dentro dos primeiros `850px` de altura vertical da tela.
- [ ] **Regra 60-30-10 de Cores**: 60% Fundo Canvas Neutro (respiro contínuo e espaço negativo), 30% Estrutura de cartões elevados e tipografia em alto contraste, e estritamente 10% de acento de conversão (CTA primário repetido no topo e na base da página).
- [ ] **Neutralização de Objeções (FAQ Accordion)**: A página DEVE conter uma seção de FAQ em accordion abordando explicitamente garantia, política de reembolso, facilidade de cancelamento e suporte técnico.

### 6.2 O Que é Terminantemente Proibido

- ❌ **Scroll-Jacking**: Jamais interceptar os eventos de rolagem do mouse para acelerar, desacelerar ou aplicar inércia artificial que impeça o ritmo natural de leitura do visitante.
- ❌ **Múltiplos Botões Primários Concorrentes**: Proibido colocar botões de contraste idêntico com ações divergentes lado a lado (ex: "Comprar Agora" e "Falar com Vendas" brigando por atenção). Deve haver apenas UM CTA primário por dobra.
- ❌ **Imagens Corporativas Genéricas**: Proibido o uso de fotos de banco de imagens mostrando modelos sorridentes em salas de conferência falsas. Utilize capturas de tela reais do produto, ilustrações técnicas ou mockups vetoriais nítidos.
- ❌ **Popups Intrusivos Antes da Compreensão**: Proibido disparar modais de captura de lead nos primeiros 15 segundos de visita antes que o usuário tenha rolado pelo menos 40% da página.
- ❌ **Fadiga de Scroll (> 8 Seções)**: Proibido empilhar mais de 8 seções em um One Pager. Se o conteúdo exigir mais espaço, o texto deve ser sintetizado com maior rigor editorial.

### 6.3 Guia de Tom e Voz da UI (Clean UI Copy)

O copywriting da interface deve refletir a sobriedade e a objetividade de um engenheiro de produto de elite:
- **Títulos Orientados a Ação e Ganho Concreto**: Em vez de *"Recursos Exclusivos"*, use *"Construa, teste e publique em menos de 60 segundos"*.
- **Métricas Transparentes**: Em vez de *"Nossa ferramenta é ultrarrápida"*, use *"Tempo de resposta p99 inferior a 25ms"*.
- **Rótulos de Conversão Claros**: Use *"Iniciar Teste Gratuito de 14 Dias"*, *"Ver Demonstração ao Vivo"*, *"Garantir Acesso Antecipado"*.
