---
id: "screenlane"
name: "Screenlane"
url: "https://screenlane.com/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico:
  - "Real-World Shipped Production Software (Mobile iOS, Android & Desktop Web)"
  - "Motion-Centric Interface Architecture & Micro-Interactions (Herança UI Movement)"
  - "End-to-End User Journeys & Multi-Screen Task Recordings"
  - "Component-Level State Matrix (Empty States, Error Validation, Modals, Paywalls)"
  - "Optical 8pt System & Native Platform Human Interface Guidelines (HIG & Material 3)"
  - "Full-Funnel Alignment: Interface Screens + Transactional Lifecycle Emails"
  - "Gesture-Driven Spatial Navigation (Bottom Sheets, Snap Drawers, Interactive Carousels)"
densidade_informacao: "Alta/Utilitaria"
impacto_visual: "Editorial/Sofisticado & High-Fidelity Native Production"
custo_computacional: "Baixo a Moderado (Renderização nativa de 60fps/120fps ProMotion, aceleração por GPU via hardware layers, transform/opacity springs, zero sobrecarga WebGL/3D irrelevante)"
stack_frameworks:
  - "React 19 / Next.js 15 (App Router, Server Components)"
  - "React Native / Expo (Cross-Platform Mobile Engine)"
  - "SwiftUI (iOS Human Interface Guidelines & Dynamic Island)"
  - "Kotlin / Jetpack Compose (Android Material 3 & Edge-to-Edge Design)"
  - "Tailwind CSS v3 / v4 (Container Queries, Safe-Area Environment Utilities)"
  - "Framer Motion / Motion.dev (molas táteis com stiffness/damping calibrados e layout animations)"
  - "Radix UI Primitives / Shadcn UI / Vaul Drawer"
compatibilidade:
  fontes_ideais:
    - "Sistemas Operacionais Nativos: SF Pro Display & SF Pro Text (Apple iOS/macOS), Roboto & Roboto Flex (Android), Segoe UI (Windows)"
    - "Neo-Grotesques Corporativas & Digitais: Inter, Geist Sans, PP Neue Montreal, Roobert, Plus Jakarta Sans, Circular Std, DM Sans"
    - "Grotesques Geométricas de Produto: Satoshi, General Sans, Manrope, Urbanist"
    - "Tipografia Numérica & Monospace de Dados: Geist Mono, JetBrains Mono, SF Mono, Fira Code"
    - "Serifas Editoriais & FinTech D2C: New York (Apple), Fraunces, GT Super, Instrument Serif"
  paletas_ideais:
    - "Apple Human Interface Semantic Tokens (Light & Dark Mode Nativo): Canvas (#FFFFFF / #000000), Grouped Background (#F2F2F7 / #1C1C1E), Elevated Surface (#FFFFFF / #2C2C2E), Separator (#C6C6C8 / #38383A), System Blue (#007AFF), System Green (#34C759), System Red (#FF3B30)"
    - "Material Design 3 Surface Roles: Surface (#FEF7FF / #141218), Surface Container (#F3EDF7 / #211F26), Surface Container High (#ECE6F0 / #2B2930), Primary (#6750A4 / #D0BCFF), Outline (#79747E / #938F99)"
    - "Modern High-Performance Dark SaaS (Linear / Raycast / Stripe): Background (#09090B - Zinc-950), Surface (#18181B - Zinc-900), Surface Hover (#27272A - Zinc-800), Border Subtitle (#3F3F46 - Zinc-700), Accent Yellow/Amber (#FEF08A / #FBBF24), Text Primary (#FAFAFA), Text Muted (#A1A1AA)"
    - "Clean Trust Consumer Mobile (Airbnb / Duolingo / Klarna): Pure Canvas (#FFFFFF), Secondary Card (#F8F9FA), Border (#E9ECEF), Text Jet Black (#111827), Text Secondary (#6B7280), Brand Accent (#FF385C Coral ou #58CC02 Emerald)"
  combinacoes_recomendadas:
    - "Vaul Drawer + Framer Motion + Tailwind CSS para reconstrução web de Bottom Sheets nativas com drag gesture e snap points"
    - "Radix Dialog / Popover + Lucide Icons (stroke 1.5px em viewBox de 20x20 ou 24x24) com optical centering"
    - "Uso irrestrito de 8-Point Grid (multiplos de 4px e 8px: 4, 8, 12, 16, 20, 24, 32, 40, 48, 64px) e variáveis CSS de Safe Area (`env(safe-area-inset-*)`)"
    - "Superfícies de vidro translúcido (`backdrop-blur-xl` com fundo `rgba(255,255,255,0.78)` no tema claro e `rgba(24,24,27,0.82)` no tema escuro) para Tab Bars flutuantes e Headers persistentes"
  conflitos_esteticos:
    - "Conceitos Dribbble inacessíveis com fontes cinza claro de 10px sobre fundo branco sem suporte a contrastes WCAG AAA"
    - "Áreas de clique e toque microscópicas menores que 44×44pt (iOS) ou 48×48dp (Android), que quebram a ergonomia móvel com uma só mão"
    - "Animações longas (>450ms) e lineares em fluxos transacionais repetitivos que frustram o usuário e causam lentidão percebida"
    - "Quebra de convenções de navegação do sistema operacional (ex: colocar botão de fechar modal do lado direito em iOS ou ignorar o back gesture padrão)"
    - "Ignorar a anatomia de hardware do dispositivo (sobreposição com o entalhe / Dynamic Island ou com a barra de navegação inferior / Home Indicator)"
    - "Dark Patterns em fluxos de cancelamento ou downgrade, como esconder o botão de confirmação ou usar contrastes enganosos"
---

# Screenlane — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
███████╗ ██████╗██████╗ ███████╗███████╗███╗   ██╗██╗      █████╗ ███╗   ██╗███████╗
██╔════╝██╔════╝██╔══██╗██╔════╝██╔════╝████╗  ██║██║     ██╔══██╗████╗  ██║██╔════╝
███████╗██║     ██████╔╝█████╗  █████╗  ██╔██╗ ██║██║     ███████║██╔██╗ ██║█████╗  
╚════██║██║     ██╔══██╗██╔══╝  ██╔══╝  ██║╚██╗██║██║     ██╔══██║██║╚██╗██║██╔══╝  
███████║╚██████╗██║  ██║███████╗███████╗██║ ╚████║███████╗██║  ██║██║ ╚████║███████╗
╚══════╝ ╚═════╝╚═╝  ╚═╝╚══════╝╚══════╝╚═╝  ╚═══╝╚══════╝╚═╝  ╚═╝╚═╝  ╚═══╝╚══════╝
```

---

## 1. DNA Estético & Filosofia de Curadoria

O **Screenlane** (`https://screenlane.com/`), idealizado e construído pelo desenvolvedor independente e designer de produto britânico **Ramy Khuffash**, representa um dos marcos mais influentes na história da pesquisa de produto digital, engenharia de usabilidade e documentação de design patterns para a comunidade de software moderna.

Nascido como uma evolução direta do **UI Movement** — o primeiro repositório e newsletter dedicado exclusivamente a catalogar animações, micro-interações e comportamento cinético de interfaces —, o Screenlane refinou esse conceito original ao transportar o foco do "efeito visual isolado" para a **arquitetura de produto funcional em produção real**. Mais recentemente, o ecossistema do Screenlane e de seus projetos irmãos consolidou-se sob a bandeira unificada do **Page Flows** (`https://pageflows.com/`), criando uma base de dados com mais de **100.000 telas gravadas em vídeo e fluxos completos de ponta a ponta**.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        THE SCREENLANE / PAGE FLOWS GENEALOGY                           │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  [ UI Movement (2014) ] ──────► [ Screenlane (2018) ] ──────► [ Page Flows (Hoje) ]   │
│   • Micro-interações & animação • Telas reais categorizadas    • Gravações em vídeo    │
│   • Foco em movimento & física  • Componentes & Mobile Patterns• Jornadas completas    │
│   • Newsletter para 30k+ devs   • Decomposição por tela/estado • Emails transacionais  │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  O AXIOMA CENTRAL: "A interface estática é uma ilusão; o design existe na transição    │
│  entre a intenção do usuário e o feedback do sistema."                                 │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 O Diferencial Estrutural: Do Still Frame à Coreografia do Fluxo

Enquanto repositórios de landing pages tradicionais capturam apenas a superfície estática de uma página promocional, o Screenlane opera na intersecção entre **design de interação (IxD)** e **engenharia de software para dispositivos móveis e web**:

1. **A Herança do UI Movement (Física & Movimento)**:
   - A gênese do Screenlane está enraizada no entendimento de que botões, cartões e abas não surgem instantaneamente do vácuo; eles se expandem, desaceleram com base em massas e molas, sofrem amortecimento e guiam a atenção do olho humano.
   - O Screenlane prioriza o registro de como os elementos se comportam em movimento: o elástico de um pull-to-refresh, a elevação de um bottom sheet ao ser arrastado com o polegar, o feedback tátil de um toggle switch e a transição fluida de abas segmentadas com shared-layout springs.

2. **Produção Real Verificada (Shipped Software Only)**:
   - Recusa deliberada e intransigente a mockups de Dribbble, Behance ou conceitos conceituais de portfólio.
   - Cada tela, vídeo e email indexado no Screenlane foi extraído de builds reais publicadas na Apple App Store, Google Play Store ou servidores de produção SaaS (ex: Uber, Airbnb, Spotify, Linear, Revolut, Klarna, Duolingo, Calm, Headspace, Notion, Slack).

3. **Arquitetura Full-Funnel (Interface + Emails de Ciclo de Vida)**:
   - O Screenlane foi pioneiro em conectar a experiência dentro do aplicativo com os **touchpoints externos**: um fluxo de onboarding catalogado inclui não apenas as 4 telas do aplicativo, mas também o email de boas-vindas recebido na caixa de entrada, o email de verificação de dois fatores (magic link), o aviso de término de período de teste (trial expiration) e o email de retenção em caso de churn.

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

O Screenlane deve ser a **Referência Primária de Consulta e Arquitetura de UI** sempre que o projeto demandar alta fidelidade em fluxos transacionais, ergonomia para telas sensíveis ao toque e clareza de estados operacionais.

```
┌────────────────────────────────────────────────────────────────────────────┐
│                    SCREENLANE COGNITIVE & TASK POSITIONING                 │
├────────────────────────────────────────────────────────────────────────────┤
│  • Objetivo Primário: Resolver fricção funcional em jornadas críticas      │
│  • Percepção do Usuário: "Este aplicativo é polido, confiável e nativo"    │
│  • Foco de Atenção: Velocidade de conclusão de tarefa e ausência de ruído  │
│  • Papel no Ecossistema: A bússola para padrões ergonômicos comprovados     │
└────────────────────────────────────────────────────────────────────────────┘
```

### 2.1 Projetos & Verticais com Encaixe Perfeito

- **Mobile First & Responsive Web Apps**:
  - Aplicações SaaS B2B e B2C que exigem paridade total de usabilidade entre o navegador do desktop e o navegador mobile do smartphone.
- **Fintechs, Bancos Digitais & Neobancos**:
  - Fluxos que exigem extrema sensação de segurança, transparência em transações, teclados numéricos personalizados, biometria (Face ID/Touch ID) e cartões dinâmicos (ex: Revolut, Monzo, Robinhood).
- **E-Commerce & Marketplaces Transacionais**:
  - Checkouts com 1 clique, gavetas de carrinho flutuantes (slide-over cart), seletores de endereço e integração com Apple Pay / Google Pay.
- **Health, Fitness, Mindfulness & EdTech**:
  - Onboardings gamificados e questionários interativos de profiling progressivo (ex: Duolingo, Headspace, Finch, Calm).
- **Productivity & Collaboration SaaS**:
  - Telas complexas de configurações de equipe, permissões baseadas em funções (RBAC), upgrade de plano corporativo e painéis de cobrança (ex: Slack, Notion, Asana, Stripe).

### 2.2 Aplicação na Regra 60-30-10 de Design

Na composição de uma interface guiada pelo repertório Screenlane, o equilíbrio cromático e hierárquico deve seguir a proporção matemática áurea:

- **60% Superfície Neutra / Canvas Estrutural**:
  - Fundo neutro e limpo (`#FFFFFF` no tema claro; `#09090B` ou `#121212` no tema escuro).
  - Define o palco silencioso onde o conteúdo, textos e gráficos do usuário são os verdadeiros protagonistas.
- **30% Hierarquia de Sistema & Estrutura Tipográfica**:
  - Cartões com bordas sutis (`border-zinc-200` / `border-zinc-800`), dividers de `1px`, títulos em tipografia sans-serif robusta, ícones com espessura uniforme de linha (1.5px) e fundos de inputs em tons de cinza suave (`#F4F4F5` / `#1C1C1E`).
- **10% Micro-Interações & Acentos de Ação (The Screenlane Sparkle)**:
  - Cor de destaque de alto contraste aplicada exclusivamente a botões de ação primária (CTA), indicadores de progresso, toggles ativos, anéis de foco acessíveis e badges contextuais.
  - O movimento cinético de feedback (o leve salto da mola ao concluir um upload ou o deslizamento suave do drawer) ocupa este espaço dos 10%, gerando prazer estético sem sobrecarregar a cognição.

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

⚠️ **Incompatível com**:
- **Experiências Artísticas & Narrativas Experimentais Imersivas**: Projetos que necessitam de WebGL denso, shaders tridimensionais, tipografia desconstruída ou layout anti-grid (como exposições interativas de museus, sites conceituais de agências de publicidade ou sites no estilo Awwwards experimental). Tentar forçar o padrão utilitário do Screenlane nesses contextos destrói o fator surpresa emocional.
- **Brutalismo Cru & Anti-Design de Contracultura**: Ambientes digitais que se alimentam de bordas pesadas de 4px pretas, sombras sólidas sem desfoque (neobrutalismo), cores ácidas fluorescentes e quebra proposital de alinhamentos.
- **Landings Pages de Produto Único Puramente Promocionais (Brand Teasers)**: O Screenlane é uma biblioteca de *produto operacional*, não de folhetos publicitários de lançamento de tênis ou de filmes. Usar sua linguagem em um teaser promocional tornará o site burocrático e sem apelo visual dramático.

⚠️ **Armadilhas de Imitação (Como Não Estragar o Estilo)**:
1. **Over-Animation (Síndrome do Circo Cinético)**:
   - Adicionar transições em cascata ou molas elásticas lentas a cada interação rotineira. Se o usuário clica em "Salvar", ele quer resposta em menos de 100ms, não uma animação de 600ms com três oscilações de bounce.
2. **Ignorar as Margens de Hardware (Safe Area Insensitivity)**:
   - Colocar botões ou menus fixos colados na borda inferior da tela, fazendo com que o *Home Indicator* do iPhone ou a barra de gestos do Android bloqueiem o toque do usuário.
3. **Cópia Cega de Microcopy Descontextualizada**:
   - Copiar textos de onboarding da Duolingo ou da Uber que não refletem a voz de marca nem a conformidade jurídica do seu produto.
4. **Desrespeito às Convenções Nativas de Plataforma**:
   - Tentar reproduzir controles típicos de iOS (como segmented controls translúcidos) de forma forçada dentro de uma aplicação Android pura que adota as diretrizes do Material Design 3, gerando estranhamento imediato ao usuário daquela plataforma.

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

O acervo do Screenlane decompõe a interface em três pilares fundamentais: arquitetura de grid adaptativa, modulação tonal de superfícies e arquétipos de fluxos funcionais.

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo

```
┌────────────────────────────────────────────────────────────────────────────┐
│                  THE MOBILE & DESKTOP DUAL-GRID SYSTEM                     │
├────────────────────────────────────────────────────────────────────────────┤
│  MOBILE (Viewport 360px - 428px):                                          │
│  ├─ Margem Externa Lateral: 16px ou 20px (Strict Padding)                  │
│  ├─ Calha (Gutter): 12px a 16px                                            │
│  ├─ Colunas: 4 colunas modulares para cards lado a lado                    │
│  └─ Altura de Toque (Touch Target): Mínimo 44px (iOS) / 48px (Android)     │
│                                                                            │
│  DESKTOP / WEB APP (Viewport > 1024px):                                    │
│  ├─ Grid: 12 Colunas fluidas com max-width centralizado (1280px / 1440px)  │
│  ├─ Calha: 24px                                                            │
│  └─ Espaçamento Vertical: Escala de 8pt (8, 16, 24, 32, 48, 64, 80px)      │
└────────────────────────────────────────────────────────────────────────────┘
```

- **A Regra de Ouro do 8-Point Grid**: Todos os paddings de containers, alturas de botões, raios de borda e respiros entre texto e elementos de ação obedecem a múltiplos de 4px e 8px:
  - Micro-espaçamentos: `4px` (entre label e input), `8px` (entre ícone e texto do botão), `12px` (padding interno compacto).
  - Macro-espaçamentos: `16px` (margem móvel padrão), `24px` (padding de cartão desktop), `32px` (respiro entre seções de formulário), `48px` (espaçamento de cabeçalho).
- **Raios de Borda (Corner Radii Hierárquicos)**:
  - Botões e tags: `8px` a `12px` ou Pílula (`9999px`).
  - Cartões e containers internos: `16px` a `20px`.
  - Modais, Bottom Sheets e superfícies flutuantes: `24px` a `32px` no topo, acompanhando o raio de curvatura físico do display dos smartphones modernos (*Continuous Curvature / Squircle*).

### 4.2 Sistemas de Cores, Superfícies & Texturas

```
┌────────────────────────────────────────────────────────────────────────────┐
│                    SURFACE ELEVATION & CONTRAST LAYERS                     │
├────────────────────────────────────────────────────────────────────────────┤
│  Nível 0 (Canvas Base): #FFFFFF (Light)  │ #09090B ou #000000 (Dark)       │
│  Nível 1 (Card / Group): #F8FAFC (Light) │ #18181B (Dark Zinc-900)         │
│  Nível 2 (Popovers):     #FFFFFF (Light) │ #27272A (Dark Zinc-800)         │
│  Nível 3 (Modal/Sheet):  #FFFFFF (Light) │ #27272A (Dark Zinc-800 com glow)│
│  Backdrop Scrim: rgba(0, 0, 0, 0.45) com backdrop-filter: blur(8px)        │
└────────────────────────────────────────────────────────────────────────────┘
```

- **Divisores Físicos Elegantes**:
  - Substituição de sombras pesadas por bordas nítidas de sub-pixel de `1px solid` (`border-zinc-200` no light, `border-zinc-800` no dark).
- **Tratamento Translúcido (Glassmorphism Controlado)**:
  - Aplicação de `backdrop-filter: blur(16px)` em barras de navegação superiores (Sticky Headers) e barras de abas inferiores (Bottom Tab Bars), garantindo que o conteúdo rolado por baixo forneça contexto visual sem comprometer a legibilidade.

---

### 4.3 Catálogo Detalhado de Componentes & Padrões Extraídos (Arquétipos)

A seguir, dissecam-se **8 arquétipos concretos** essenciais extraídos dos fluxos catalogados no Screenlane:

#### Arquétipo 1: Mobile Interactive Bottom Sheet (Drawer com Drag Gesture)
- **Anatomia**:
  - Alça tátil superior (*drag handle*) centralizada com 36×5px, fundo arredondado e cor neutra;
  - Área de cabeçalho com título curto de 18px (semi-bold) e botão de fechamento opcional;
  - Conteúdo deslizável interno com overflow-y isolado;
  - Ponto de snap em 40%, 75% e 95% da altura da viewport;
  - Fundo escurecido (*scrim*) com interpolação de opacidade vinculada ao arraste.
- **Gatilho de Entrada/Saída**: Ação do usuário ao clicar em "Opções", "Filtrar" ou "Selecionar Método de Pagamento". Desliza de baixo para cima com mola suave (`stiffness: 300, damping: 30`).
- **Onde Encaixar**: Seletores contextuais, resumos de pagamento, detalhes de itens em listas sem forçar nova navegação de tela inteira.

#### Arquétipo 2: Multi-Step Animated Onboarding Sequence (Carousel com Stepper)
- **Anatomia**:
  - Barra superior de controle com botão "Pular" (*Skip*) à direita ou botão "Voltar" à esquerda;
  - Indicador de progresso no topo: barra segmentada fina (3px de altura) ou pontos dinâmicos (*dots*) que se expandem para uma pílula elástica conforme o slide avança;
  - Área central ilustrada ou com animação em Lottie/vídeo em loop silencioso de 240×240px;
  - Bloco de tipografia: Título em 24px (`letter-spacing: -0.5px`) e descrição explicativa de no máximo duas linhas em 15px com cor atenuada;
  - Botão de ação primária ancorado na base da tela, fixo acima da área segura do sistema operacional.
- **Gatilho**: Primeiro acesso do usuário pós-download ou pós-cadastro inicial.
- **Onde Encaixar**: Explicação de proposta de valor, permissões essenciais de notificação/geolocalização e configuração inicial de preferências.

#### Arquétipo 3: Dynamic Island / Toast Notification Pill
- **Anatomia**:
  - Cápsula flutuante arredondada (`rounded-full`) posicionada no topo da tela com sombra difusa elegante;
  - Ícone de status no lado esquerdo (ícone animado de confirmação ou spinner circular de carregamento);
  - Mensagem concisa com label em negrito e valor contextual (ex: "Transação enviada • R$ 150,00");
  - Capacidade de expansão ao toque para revelar detalhes adicionais.
- **Gatilho**: Confirmação de ações assíncronas em segundo plano, como download finalizado, item adicionado ao carrinho ou sincronização concluída.
- **Onde Encaixar**: Notificações contextuais em apps com alta densidade de eventos sem interromper o fluxo central.

#### Arquétipo 4: Floating Segmented Control com Indicador em Mola (Shared Layout)
- **Anatomia**:
  - Container cinza claro neutro com padding interno de 3px a 4px e cantos arredondados (`rounded-xl`);
  - Abas de texto alinhadas com peso 500;
  - Pílula ativa flutuante com fundo branco (ou cor escura contrastante no dark mode) que desliza fisicamente de uma aba para outra através de animação de layout compartilhado do Framer Motion;
  - Feedback tátil sutil (*haptic click*) ao alternar abas em dispositivos móveis.
- **Gatilho**: Clique ou swipe entre visualizações alternativas de uma mesma entidade (ex: Diário / Semanal / Mensal; Gráfico / Tabela).
- **Onde Encaixar**: Dashboards móveis, seletores de visualização e painéis analíticos.

#### Arquétipo 5: Frictionless Paywall & Upgrade Screen (Consumer Subscription)
- **Anatomia**:
  - Botão discreto de fechar em "X" no canto superior direito (muitas vezes com delay de 2 segundos para forçar a leitura da proposta de valor);
  - Banner hero com selo premium ou ilustração sutil com gradiente metálico;
  - Lista de 3 a 5 benefícios objetivos com ícones de checkmark vibrantes;
  - Seletores de plano em cartões verticais ou lado a lado, com destaque para a opção "Anual" com badge de "Melhor Custo-Benefício (Economize 45%)";
  - Micro-texto legal com termos de renovação automática, link para restauração de compras e política de privacidade;
  - Botão CTA largo com texto imperativo: "Comece seu teste grátis de 7 dias".
- **Gatilho**: Tentativa de acesso a um recurso pago ou término do período de experimentação.
- **Onde Encaixar**: Monetização em apps B2C, ferramentas de produtividade e SaaS freemium.

#### Arquétipo 6: Contextual Empty State with Actionable Micro-Flow
- **Anatomia**:
  - Vetor ou ilustração isométrica monocromática suave centralizada verticalmente;
  - Título explicativo e amigável (ex: "Nenhum projeto encontrado");
  - Descrição orientada à ação (ex: "Você ainda não possui projetos ativos nesta pasta. Crie o primeiro para começar a colaborar.");
  - Botão primário centralizado com ícone "+" de ação imediata (ex: "Criar Novo Projeto");
  - Opção secundária em texto simples com link para documentação ou importação de arquivos de amostra.
- **Gatilho**: Listas vazias após busca sem resultados, contas recém-criadas ou filtros restritivos demais.
- **Onde Encaixar**: Tabelas de dados, gerenciadores de tarefas, caixas de entrada e galerias de favoritos.

#### Arquétipo 7: High-Converting 1-Click Mobile Checkout Sheet
- **Anatomia**:
  - Linha do tempo de pagamento com resumo do pedido recolhido em sanfona (*accordion*);
  - Seletor de endereço de entrega com visualização em mapa estático miniaturizado ou pílula com indicador de tempo estimado;
  - Seletor de forma de pagamento com destaque prioritário para Apple Pay / Google Pay / PIX com 1 clique;
  - Divisor com valor total destacado em fonte de 20px com peso bold;
  - Botão de finalização com slide gesture (*Swipe to Pay*) ou botão nativo do sistema operacional.
- **Gatilho**: Clique em "Finalizar Compra" a partir do carrinho de compras.
- **Onde Encaixar**: E-commerces, aplicativos de delivery de comida, reservas de transporte e bilheteria digital.

#### Arquétipo 8: Stepper Form / Progressive Profiling Questionnaire
- **Anatomia**:
  - Contador de passos discreto ("Pergunta 2 de 5") ou barra de preenchimento suave no topo;
  - Uma pergunta principal em destaque tipográfico grande (24px a 28px);
  - Cartões de opções selecionáveis com suporte a múltipla escolha ou escolha única, com anéis de seleção reativos que mudam de cor ao clique;
  - Validação em tempo real e transição automática para a próxima etapa assim que uma opção válida é selecionada;
  - Rodapé fixo com botão "Voltar" e "Avançar".
- **Gatilho**: Fluxos de onboarding com personalização algorítmica (ex: apps de dieta, aprendizado de idiomas ou avaliação de risco financeiro).
- **Onde Encaixar**: Qualificação de leads em SaaS e personalização de feeds.

---

## 5. Tradução para Código & Stack do Design Engine

Para reproduzir com exatidão a qualidade visual, a física e a estabilidade das interfaces catalogadas no Screenlane, o engenheiro de software deve empregar uma arquitetura de tokens CSS semânticos acoplada a motores de animação baseados em molas físicas.

### 5.1 Tokens CSS & Design System Architecture

```css
/* ==========================================================================
   SCREENLANE DESIGN SYSTEM TOKENS (CSS VARIABLES)
   Compatível com Tailwind CSS v3 / v4 e temas dinâmicos (Light & Dark)
   ========================================================================== */

:root {
  /* Escala de Espaçamento Base 8pt */
  --sl-space-1: 4px;
  --sl-space-2: 8px;
  --sl-space-3: 12px;
  --sl-space-4: 16px;
  --sl-space-5: 20px;
  --sl-space-6: 24px;
  --sl-space-8: 32px;
  --sl-space-10: 40px;
  --sl-space-12: 48px;
  --sl-space-16: 64px;

  /* Raios de Borda (Continuous Squircle Radii) */
  --sl-radius-xs: 6px;
  --sl-radius-sm: 8px;
  --sl-radius-md: 12px;
  --sl-radius-lg: 16px;
  --sl-radius-xl: 24px;
  --sl-radius-2xl: 32px;
  --sl-radius-full: 9999px;

  /* Variáveis de Áreas Seguras de Hardware */
  --sl-safe-top: env(safe-area-inset-top, 20px);
  --sl-safe-bottom: env(safe-area-inset-bottom, 20px);
  --sl-safe-left: env(safe-area-inset-left, 0px);
  --sl-safe-right: env(safe-area-inset-right, 0px);

  /* Paleta Semântica Light */
  --sl-bg-canvas: #FFFFFF;
  --sl-bg-subtle: #F8FAFC;
  --sl-bg-card: #FFFFFF;
  --sl-bg-hover: #F1F5F9;
  --sl-border: #E2E8F0;
  --sl-border-subtle: #F1F5F9;
  --sl-text-primary: #0F172A;
  --sl-text-secondary: #64748B;
  --sl-text-muted: #94A3B8;
  --sl-accent: #007AFF; /* Apple Tint Blue */
  --sl-accent-hover: #0062CC;
  --sl-accent-contrast: #FFFFFF;
  --sl-scrim: rgba(15, 23, 42, 0.45);
}

[data-theme="dark"] {
  /* Paleta Semântica Dark */
  --sl-bg-canvas: #09090B;
  --sl-bg-subtle: #18181B;
  --sl-bg-card: #18181B;
  --sl-bg-hover: #27272A;
  --sl-border: #27272A;
  --sl-border-subtle: #1E1E22;
  --sl-text-primary: #FAFAFA;
  --sl-text-secondary: #A1A1AA;
  --sl-text-muted: #71717A;
  --sl-accent: #3B82F6;
  --sl-accent-hover: #60A5FA;
  --sl-accent-contrast: #FFFFFF;
  --sl-scrim: rgba(0, 0, 0, 0.72);
}
```

---

### 5.2 Física de Movimento: Curvas de Easing & Molas (Spring Dynamics)

A identidade do Screenlane, herdada do UI Movement, repousa no movimento orgânico que imita a inércia do mundo real:

```
┌────────────────────────────────────────────────────────────────────────────┐
│                    SCREENLANE MOTION PHYSICS SPECIFICATION                 │
├────────────────────────────────────────────────────────────────────────────┤
│  1. Micro-Interações (Botões, Toggles, Tooltips):                          │
│     • Duração: 150ms a 200ms                                               │
│     • Curva CSS: cubic-bezier(0.16, 1, 0.3, 1) [Decel Ultra-Rápido]        │
│     • Framer Spring: stiffness: 500, damping: 35, mass: 0.8                │
│                                                                            │
│  2. Modais, Menus e Bottom Sheets (Ações de Grande Escala):                 │
│     • Duração: 300ms a 420ms                                               │
│     • Curva CSS: cubic-bezier(0.32, 0.72, 0, 1) [Apple Sheet Standard]     │
│     • Framer Spring: stiffness: 320, damping: 32, mass: 1.0                │
│                                                                            │
│  3. Layout Compartilhado (Pílulas de Tab e Filtros Flutuantes):            │
│     • Framer Spring: stiffness: 450, damping: 36                           │
│     • Propriedades Animadas: EXCLUSIVAMENTE transform e opacity            │
└────────────────────────────────────────────────────────────────────────────┘
```

---

### 5.3 Receita de Código Funcional Completa: Bottom Sheet Transacional Nativo

Abaixo apresenta-se um componente de produção completo em **React 19**, **Tailwind CSS** e **Framer Motion**, incorporando arrasto tátil por gestos, física de mola calibrada, suporte a temas e respeito às Safe Areas de hardware:

```tsx
import React, { useState, useEffect } from "react";
import { motion, AnimatePresence, PanInfo } from "framer-motion";
import { Check, X, ShieldCheck, ChevronRight, CreditCard, Sparkles } from "lucide-react";

interface PlanOption {
  id: string;
  name: string;
  description: string;
  price: string;
  period: string;
  badge?: string;
  popular?: boolean;
}

interface ScreenlaneUpgradeSheetProps {
  isOpen: boolean;
  onClose: () => void;
  onConfirm: (planId: string) => void;
}

const plans: PlanOption[] = [
  {
    id: "annual",
    name: "Acesso Pro Anual",
    description: "Faturado R$ 359,90 uma vez ao ano (Economia de 45%)",
    price: "R$ 29,99",
    period: "/mês",
    badge: "MAIS POPULAR",
    popular: true,
  },
  {
    id: "monthly",
    name: "Acesso Pro Mensal",
    description: "Cancele quando quiser sem fidelidade",
    price: "R$ 54,90",
    period: "/mês",
    popular: false,
  },
];

export const ScreenlaneUpgradeSheet: React.FC<ScreenlaneUpgradeSheetProps> = ({
  isOpen,
  onClose,
  onConfirm,
}) => {
  const [selectedPlan, setSelectedPlan] = useState<string>("annual");

  // Bloqueio de scroll do body quando o sheet está aberto
  useEffect(() => {
    if (isOpen) {
      document.body.style.overflow = "hidden";
    } else {
      document.body.style.overflow = "unset";
    }
    return () => {
      document.body.style.overflow = "unset";
    };
  }, [isOpen]);

  const handleDragEnd = (
    _event: MouseEvent | TouchEvent | PointerEvent,
    info: PanInfo
  ) => {
    // Se o usuário arrastar mais de 120px para baixo ou com velocidade alta, fecha o modal
    if (info.offset.y > 120 || info.velocity.y > 500) {
      onClose();
    }
  };

  return (
    <AnimatePresence>
      {isOpen && (
        <div className="fixed inset-0 z-50 flex items-end justify-center sm:items-center">
          {/* Fundo Escurecido com Blur Suave (Scrim) */}
          <motion.div
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            exit={{ opacity: 0 }}
            transition={{ duration: 0.25, ease: [0.16, 1, 0.3, 1] }}
            onClick={onClose}
            className="fixed inset-0 bg-black/60 backdrop-blur-sm"
            aria-hidden="true"
          />

          {/* Superfície do Sheet / Drawer */}
          <motion.div
            initial={{ y: "100%" }}
            animate={{ y: 0 }}
            exit={{ y: "100%" }}
            transition={{
              type: "spring",
              stiffness: 340,
              damping: 34,
              mass: 0.95,
            }}
            drag="y"
            dragConstraints={{ top: 0, bottom: 0 }}
            dragElastic={0.15}
            onDragEnd={handleDragEnd}
            role="dialog"
            aria-modal="true"
            aria-labelledby="upgrade-title"
            className="relative w-full max-w-lg rounded-t-[32px] bg-white p-6 shadow-2xl dark:bg-zinc-900 sm:rounded-[32px] sm:p-8"
            style={{
              paddingBottom: "calc(env(safe-area-inset-bottom, 20px) + 1.5rem)",
            }}
          >
            {/* Alça Tátil de Arraste (Drag Handle) */}
            <div className="flex justify-center pb-3">
              <div className="h-1.5 w-10 rounded-full bg-zinc-300 dark:bg-zinc-700" />
            </div>

            {/* Cabeçalho com Botão de Fechar */}
            <div className="flex items-start justify-between">
              <div className="flex items-center gap-3">
                <div className="flex h-10 w-10 items-center justify-center rounded-xl bg-amber-100 text-amber-600 dark:bg-amber-950/60 dark:text-amber-400">
                  <Sparkles className="h-5 w-5" />
                </div>
                <div>
                  <h3
                    id="upgrade-title"
                    className="text-xl font-bold tracking-tight text-zinc-900 dark:text-zinc-50"
                  >
                    Desbloqueie o Pro
                  </h3>
                  <p className="text-sm text-zinc-500 dark:text-zinc-400">
                    Acesso ilimitado a fluxos e templates
                  </p>
                </div>
              </div>
              <button
                onClick={onClose}
                className="rounded-full p-2 text-zinc-400 transition-colors hover:bg-zinc-100 hover:text-zinc-600 dark:hover:bg-zinc-800 dark:hover:text-zinc-200"
                aria-label="Fechar janela"
              >
                <X className="h-5 w-5" />
              </button>
            </div>

            {/* Lista de Vantagens com Ícones */}
            <div className="mt-6 space-y-3">
              {[
                "100.000+ gravações em vídeo de fluxos de produção",
                "Exportação de tokens CSS e componentes Figma",
                "Acesso a fluxos completos de onboarding e checkout",
              ].map((benefit, idx) => (
                <div key={idx} className="flex items-center gap-2.5 text-sm text-zinc-600 dark:text-zinc-300">
                  <div className="flex h-5 w-5 shrink-0 items-center justify-center rounded-full bg-emerald-100 text-emerald-600 dark:bg-emerald-950/50 dark:text-emerald-400">
                    <Check className="h-3 w-3 stroke-[3]" />
                  </div>
                  <span>{benefit}</span>
                </div>
              ))}
            </div>

            {/* Seletor de Planos em Cards */}
            <div className="mt-6 space-y-3">
              {plans.map((plan) => {
                const isSelected = selectedPlan === plan.id;
                return (
                  <div
                    key={plan.id}
                    onClick={() => setSelectedPlan(plan.id)}
                    className={`relative flex cursor-pointer items-center justify-between rounded-2xl border p-4 transition-all duration-200 ${
                      isSelected
                        ? "border-blue-600 bg-blue-50/50 ring-2 ring-blue-500/20 dark:border-blue-500 dark:bg-blue-950/20"
                        : "border-zinc-200 bg-zinc-50/50 hover:bg-zinc-100/60 dark:border-zinc-800 dark:bg-zinc-800/40 dark:hover:bg-zinc-800/80"
                    }`}
                  >
                    {plan.badge && (
                      <span className="absolute -top-2.5 right-4 rounded-full bg-blue-600 px-2.5 py-0.5 text-[10px] font-bold uppercase tracking-wider text-white dark:bg-blue-500">
                        {plan.badge}
                      </span>
                    )}
                    <div className="flex items-center gap-3">
                      <div
                        className={`flex h-5 w-5 items-center justify-center rounded-full border transition-colors ${
                          isSelected
                            ? "border-blue-600 bg-blue-600 text-white dark:border-blue-500 dark:bg-blue-500"
                            : "border-zinc-400 dark:border-zinc-600"
                        }`}
                      >
                        {isSelected && <Check className="h-3 w-3 stroke-[3]" />}
                      </div>
                      <div>
                        <div className="text-sm font-semibold text-zinc-900 dark:text-zinc-100">
                          {plan.name}
                        </div>
                        <div className="text-xs text-zinc-500 dark:text-zinc-400">
                          {plan.description}
                        </div>
                      </div>
                    </div>
                    <div className="text-right">
                      <span className="text-lg font-bold text-zinc-900 dark:text-zinc-50">
                        {plan.price}
                      </span>
                      <span className="text-xs text-zinc-500 dark:text-zinc-400">
                        {plan.period}
                      </span>
                    </div>
                  </div>
                );
              })}
            </div>

            {/* Botão de Ação Primária Fixo */}
            <div className="mt-6 space-y-3">
              <button
                onClick={() => onConfirm(selectedPlan)}
                className="flex w-full items-center justify-center gap-2 rounded-2xl bg-blue-600 py-3.5 text-base font-semibold text-white shadow-lg shadow-blue-500/25 transition-all hover:bg-blue-700 active:scale-[0.98] dark:bg-blue-500 dark:hover:bg-blue-600"
              >
                <span>Experimente por 3 Dias</span>
                <ChevronRight className="h-4 w-4" />
              </button>

              {/* Informações de Garantia & Microcopy de Confiança */}
              <div className="flex items-center justify-center gap-2 text-xs text-zinc-400 dark:text-zinc-500">
                <ShieldCheck className="h-4 w-4" />
                <span>Cancele a qualquer momento nas configurações da sua conta</span>
              </div>
            </div>
          </motion.div>
        </div>
      )}
    </AnimatePresence>
  );
};
```

---

### 5.4 Como o Agente de IA Deve Pesquisar ao Vivo no Screenlane / Page Flows

Ao consultar referências ao vivo no repositório do Screenlane (atualmente integrado com a infraestrutura do Page Flows em `https://pageflows.com/`), o modelo de linguagem ou o agente autônomo deve utilizar a seguinte matriz semântica de URLs:

```
┌────────────────────────────────────────────────────────────────────────────┐
│                  PAGE FLOWS / SCREENLANE LIVE URL TAXONOMY                 │
├────────────────────────────────────────────────────────────────────────────┤
│  1. Busca Global via Parâmetro:                                            │
│     https://pageflows.com/search/?q={termo_pesquisa}                       │
│     Ex: https://pageflows.com/search/?q=onboarding                         │
│                                                                            │
│  2. Fluxos de Tarefas por Plataforma (User Flows):                         │
│     iOS:     https://pageflows.com/ios/flows/{slug_do_fluxo}/              │
│     Android: https://pageflows.com/android/flows/{slug_do_fluxo}/          │
│     Web:     https://pageflows.com/web/flows/{slug_do_fluxo}/              │
│                                                                            │
│  3. Telas Específicas por Padrão de Tela (Screens):                        │
│     iOS:     https://pageflows.com/ios/screens/{slug_da_tela}/             │
│     Android: https://pageflows.com/android/screens/{slug_da_tela}/         │
│     Web:     https://pageflows.com/web/screens/{slug_da_tela}/             │
│                                                                            │
│  4. Elementos de Interface Isolados (UI Elements):                         │
│     https://pageflows.com/{plataforma}/elements/{slug_do_elemento}/        │
│                                                                            │
│  5. Decomposição de Produtos Específicos:                                  │
│     https://pageflows.com/post/{plataforma}/{slug_do_fluxo}/{slug_app}/    │
│     Ex: https://pageflows.com/post/ios/onboarding/revolut/                 │
│                                                                            │
│  6. Emails Transacionais de Ciclo de Vida:                                 │
│     https://pageflows.com/emails/                                          │
└────────────────────────────────────────────────────────────────────────────┘
```

#### Tabela de Slugs Oficiais para Automação de Busca:

| Categoria | Slugs Primários |
| :--- | :--- |
| **User Flows** | `onboarding`, `logging-in`, `signing-up`, `upgrading`, `cancelling-subscription`, `checking-out`, `referring-friends`, `searching`, `filtering`, `resetting-password` |
| **Screens** | `sign-up`, `login`, `checkout`, `upgrade`, `dashboard`, `pricing-plans`, `settings`, `profile`, `empty-state`, `product-detail`, `cart`, `forgot-password` |
| **UI Elements** | `text-field`, `button`, `card`, `bottom-sheet`, `tabs`, `modal`, `navigation-bar`, `search-bar`, `toast`, `segmented-control`, `toggle` |
| **Produtos Típicos** | `revolut`, `robinhood`, `monzo`, `n26`, `spotify`, `starling`, `stripe`, `notion`, `intercom`, `slack`, `shopify`, `amplitude`, `airbnb`, `uber`, `duolingo` |

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao consumir o Screenlane como referência estética para a criação de um novo produto ou sistema dentro do `DESIGN_BLUEPRINT.md`, os agentes devem aplicar estritamente as seguintes regras:

1. **Prioridade Absoluta ao Estado do Sistema**:
   - Cada componente deve ter definidos seus 5 estados operacionais antes de qualquer linha de código final: *Default*, *Hover/Pressed*, *Focus Visible*, *Loading/Skeleton* e *Error/Disabled*.
2. **Ergonomia do Polegar (The Thumb Zone Principle)**:
   - Toda ação destrutiva ou de conversão primária deve estar localizada na metade inferior da tela do dispositivo móvel. Nenhuma ação frequente deve exigir alcançar o topo do aparelho com apenas uma mão.
3. **Respeito aos Componentes Nacionais e Nativos**:
   - Para formulários brasileiros ou europeus, respeitar máscaras de campos (CPF, CEP, IBAN) e integrações nativas como Apple Pay e PIX, utilizando Bottom Sheets em vez de redirecionamentos de página inteira.
4. **Alinhamento do Microcopy**:
   - A redação de interface (*UX Writing*) deve ser livre de jargões técnicos: títulos curtos de no máximo 4 palavras e textos explicativos de até 2 linhas que deixem claro o benefício do clique para o usuário.
5. **Feedback Imediato & Ausência de Animações Bloqueantes**:
   - Ações que dependem de rede devem exibir feedback visual instantâneo (otimista ou spinner discreto) em menos de 80ms, mantendo a interface reativa sem congelar interações concomitantes.
