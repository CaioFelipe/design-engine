---
id: "115-pageflows"
name: "Page Flows"
url: "https://pageflows.com/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico:
  - "Evidence-Based UX Engineering & Real-App Dynamic Journeys"
  - "Full-Funnel Lifecycle Continuity (Desktop Web ⟷ iOS ⟷ Android ⟷ Lifecycle Emails)"
  - "Time-Synchronized Interactive Video Scrubbing with Granular Step Annotations"
  - "Product-Led Growth (PLG) Benchmarking (Onboarding, Upgrades, Invites, Paywalls, Cancellations)"
  - "Dark Obsidian Control Canvas (#0B0B0D / #18181B) with High-Contrast Canary Accent (#FEF08A)"
  - "Micro-Interaction Pragmatism & Anti-Dribbble Feasibility"
  - "Atomic Screen & UI Component Taxonomy (Inputs, Bottom Sheets, Modals, Empty States)"
densidade_informacao: "Alta/Utilitaria (Análise de fluxos operacionais, sequências de telas e timestamps) a Media/Narrativa (Apresentação de case studies)"
impacto_visual: "Editorial/Sofisticado & High-Utility Commercial Tech"
custo_computacional: "Baixo a Moderado (Renderização pura via DOM/CSS, layouts otimizados com CSS Grid/Flexbox, aceleração por GPU para drawers e timelines, carregamento assíncrono e preguiçoso de streams MP4/WebM e thumbnails WebP)"
stack_frameworks:
  - "Next.js 14/15 / Remix (SSR/SSG para páginas de catálogo, streaming para rotas dinâmicas de mídia)"
  - "React 19 / TypeScript"
  - "Tailwind CSS v3/v4 (container queries, CSS variables semânticas, bordas nítidas de 1px)"
  - "Framer Motion / Motion.dev (molas com amortecimento crítico para drawers, transições de estado de modais e timelines de scrubber)"
  - "Radix UI / Shadcn UI (primitivos acessíveis WAI-ARIA para dialogs, tooltips, tabs, dropdowns e sliders)"
  - "Video.js / Plyr / Custom HTML5 Video Player API (sincronização bidirecional de timecodes com anotações de fluxo)"
  - "Lucide React (iconografia semântica consistente de 1.5px e 2px)"
compatibilidade:
  fontes_ideais:
    - "Sans-Serif Modernas & Geométricas de Engenharia: Geist Sans, Inter, Plus Jakarta Sans, Satoshi, DM Sans, General Sans"
    - "Display Sans para Títulos e Destaques Editoriais: Cal Sans, Bricolage Grotesque, PP Neue Montreal, Cabinet Grotesk"
    - "Monoespaçadas para Timestamps, Métricas Técnicas e IDs de Transação: Geist Mono, JetBrains Mono, Fira Code, Space Mono"
  paletas_ideais:
    - "Page Flows Obsidian & Canary Dark (Canvas Mestre da Plataforma): #0B0B0D (Fundo Primário Preto Profundo), #18181B (Superfície de Contêineres Zinc 900), #27272A (Bordas e Superfícies Elevadas Zinc 800), #FEF08A (Acento Primário Amarelo Canário / Destaque de Ação), #FAFAFA (Texto Primário Branco Puro), #A1A1AA (Texto Secundário e Ícones Neutros Zinc 400), #10B981 (Confirmação/Sucesso Verde Esmeralda)"
    - "Enterprise SaaS Light Canvas (Padrão de Apps Web Desktop Inspecionados): #FFFFFF (Fundo Mestre e Cards), #F8FAFC (Canvas Fundo Slate 50), #0F172A (Texto Primário Slate 900), #64748B (Texto Secundário Slate 500), #E2E8F0 (Bordas Estruturais 1px Slate 200), #4F46E5 / #6366F1 (Acento Índigo Corporativo), #2563EB (Azul Cobalto de Foco/Seleção)"
    - "Mobile Modern Native Clean (Padrão de Apps iOS e Android Inspecionados): #000000 / #FFFFFF (Canvas Adaptativo Dinâmico), #1C1C1E / #F2F2F7 (Superfícies de Agrupamento iOS), #007AFF (Azul Sistema iOS), #34C759 (Verde Sistema iOS), #FF3B30 (Vermelho de Cancelamento/Erro Destrutivo)"
    - "Regra 60-30-10 de Arquitetura de Software: 60% Superfície Neutra de Fundo (Preto Profundo `#0B0B0D` no player ou Branco/Ardósia `#F8FAFC` nas interfaces de produto), 30% Estrutura de Contêineres, Grids, Linhas Divisórias de 1px e Tipografia Escaneável, 10% Acentos Semânticos de Ação e Interação (Amarelo Ouro `#FEF08A`, Índigo/Azul de Ação Primária, Badges de Status e Marcadores de Timeline Ativa)"
  combinacoes_recomendadas:
    - "Vídeo Player com Scrubber de Linha do Tempo e Lista Lateral de Anotações sincronizada com timecodes clicáveis"
    - "Carrossel Horizontal de Capturas de Tela em Alta Resolução com botões flutuantes de rolagem suave e atalho para download em lote"
    - "Seletor de Plataforma em 4 Abas Semânticas (iOS, Android, Desktop Web, Lifecycle Emails) com preservação de filtro contextual"
    - "Modal de Wizard Multi-Etapas com barra de progresso linear no topo, tiles de opção com seleção por rádio e botão 'Próximo' fixo no rodapé"
    - "Bottom Sheet nativo em mobile com puxador visual (drag handle) e transição de entrada amortecida via Framer Motion"
    - "Matriz de Precificação com Alternador Mensal/Trimestral/Anual e Tooltip flutuante de valor agregado ('Economize 35%')"
    - "Gatilhos de Modais de Confirmação com micro-ícone semântico, resumo dos impactos e botões empilhados (Primário vs Cancelar Neutro)"
  conflitos_esteticos:
    - "Apresentar telas isoladas de produto sem contextualizar o fluxo completo (gerando a falsa impressão de simplicidade em jornadas complexas)"
    - "Uso de layouts estáticos desconectados das transições de estado (ignorar telas de carregamento, erros de validação e estados intermediários de formulário)"
    - "Designers reproduzindo 'Dribbble fantasy UI' (sombras multicoloridas difusas > 40px, contrastes inacessíveis de texto cinza-claro sobre branco)"
    - "Onboardings com questionários exaustivos (> 6 passos) sem barra de progresso ou sem possibilidade de salvar rascunho / pular etapas"
    - "Scroll-jacking e bloqueio de rolagem do navegador em páginas de visualização de tabelas e fluxos técnicos de produto"
    - "Inconsistência entre a linguagem visual dos e-mails transacionais e a interface real do software (identidade fragmentada)"
    - "Dark patterns em fluxos de cancelamento (esconder o botão de confirmação, criar caminhos falsos ou desorientar o usuário com pegadinhas semânticas)"
---

# Page Flows — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
██████╗  █████╗  ██████╗ ███████╗    ███████╗██╗      ██████╗ ██╗    ██╗███████╗
██╔══██╗██╔══██╗██╔════╝ ██╔════╝    ██╔════╝██║     ██╔═══██╗██║    ██║██╔════╝
██████╔╝███████║██║  ███╗█████╗      █████╗  ██║     ██║   ██║██║ █╗ ██║███████╗
██╔═══╝ ██╔══██║██║   ██║██╔══╝      ██╔══╝  ██║     ██║   ██║██║███╗██║╚════██║
██║     ██║  ██║╚██████╔╝███████╗    ██║     ███████╗╚██████╔╝╚███╔███╔╝███████║
╚═╝     ╚═╝  ╚═╝ ╚═════╝ ╚══════╝    ╚═╝     ╚══════╝ ╚═════╝  ╚══╝╚══╝ ╚══════╝
```

---

## 1. DNA Estético & Filosofia de Curadoria

O **Page Flows** (`https://pageflows.com/`), idealizado e fundado em Londres pelo designer e engenheiro de produto **Ramy Khuffash**, revolucionou a metodologia de pesquisa e especificação de UI/UX no ecossistema global de software. Lançado inicialmente como um boletim curado de telas reais de produtos e transformado organicamente em uma biblioteca monumental com **mais de 100.000 telas e vídeos gravados**, o Page Flows estabeleceu uma nova categoria de ferramenta de inteligência competitiva para equipes de design de produto, fundadores e arquitetos frontend.

A filosofia seminal que fundamenta o Page Flows é a **rejeição veemente da "Dribbblização do Design"**: a tendência histórica de galerias visuais que celebram maquetes conceituais estáticas, cenários fictícios de tela única e interfaces puramente decorativas que seriam tecnicamente inviáveis, comercialmente falhas ou completamente rejeitadas em testes reais de usabilidade. 

Em contraste direto com esse modelo contemplativo, o Page Flows ancora-se em três pilares metodológicos:
1. **O Produto em Movimento Real**: Software não é uma imagem congelada; é uma **trajetória temporal de estados**. Uma tela de cadastro ganha significado apenas quando examinada dentro da transição entre o clique no CTA de marketing, os micro-estados de foco e validação de campos, o disparo de autenticação multifator (2FA) e o primeiro dashboard povoado.
2. **Registro Ponta a Ponta do Ciclo de Vida**: Da criação da conta ao cancelamento, passando por fluxos de convite de equipe, compra/checkout com 3D Secure, pesquisa facetada, integração de API e e-mails de retenção disparados no processo.
3. **Padrões Validados pelo Mercado**: Em vez de invenções arbitrárias, o acervo disseca a anatomia de produtos líderes mundiais consolidados por milhões de usuários — como **Stripe, Airbnb, Uber, Netflix, Spotify, Notion, Slack, Revolut, Robinhood, Asana, Duolingo, Klarna e Sonos**.

```
┌─────────────────────────────────────────────────────────────────────────────────────────┐
│                        PAGE FLOWS FULL-LIFECYCLE JUXTAPOSITION                          │
├─────────────────────────────────────────────────────────────────────────────────────────┤
│  [ DISCOVERY & ENTRY ]   ──►  [ PROGRESSIVE ACTIVATION ] ──►  [ RUNTIME INTERACTION ]   │
│   • Multi-Platform Entry      • Frictionless Social OAuth     • Dense Operational UI    │
│   • Plan / Pricing Matrix     • Progressive Profiling Quiz    • Bottom Sheets & Drawers │
│   • Welcome Direct Landing    • Guided Checklist Setup        • Command (CMD+K) Bar     │
├─────────────────────────────────────────────────────────────────────────────────────────┤
│  [ MONETIZATION TOUCH ]  ◄──  [ LIFECYCLE AUDIT TRAILS ] ◄──  [ RETENTION & EXPANSION ] │
│   • In-App Upgrades & Tiers   • Automated Welcome Drips       • Team Member Invitation  │
│   • Stripe Elements Checkout  • Password & 2FA Confirmations  • Data Export & Reports   │
│   • Pro-Rated Billing Modals  • Cancellation Funnels          • Settings & Permissions  │
└─────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 A Plataforma como Espelho Ergonômico de Alta Eficiência

A interface do próprio Page Flows é uma aula magistral de design utilitário dark-mode. Utilizando um canvas de fundo negro profundo (`#0B0B0D`) com contêineres de alta precisão em ardósia grafite (`#18181B` e `#27272A`), a plataforma posiciona o conteúdo inspecionado (as gravações e telas) no centro da atenção óptica do usuário. 

O uso estratégico do acento **Amarelo Canário / Ouro Quente (`#FEF08A` / `#FDE047`)** fornece um ponto focal instantâneo para ações prioritárias (como o CTA de teste de 3 dias, a seleção do plano mais popular e os marcadores de estado ativo), estabelecendo uma identidade visual singular que equilibra sobriedade industrial e calor humano.

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

O Page Flows deve ser a **Referência Primária de Direção de Arquitetura e Fluxo** quando o projeto demandar:

* **Sistemas de Onboarding com Alta Conversão (Product-Led Growth)**:
  Quando a meta for construir jornadas de ativação que reduzam o *Time-to-Value (TTV)* para menos de 60 segundos. O acervo permite mapear como o Stripe guia desenvolvedores até a primeira chave de API ou como o Notion inicializa templates a partir de três perguntas de qualificação.
* **Jornadas de Checkout, Cobrança e Upgrades In-App**:
  Quando for imperativo desenhar modais de upgrade de plano, alertas de estouro de cota de uso, fluxos de cartão de crédito com Stripe Elements ou comparativos de precificação modular com alternador de periodicidade (Mensal vs Anual).
* **Fluxos Críticos de Autenticação, Segurança e Recuperação**:
  Ao estruturar telas de login com suporte a Magic Link, biometria (WebAuthn/Passkeys), autenticação multifator (SMS, Authenticator App, chaves de segurança físicas FIDO2) e recuperação segura de conta.
* **Projetos Multiplataforma Integrados (Web ⟷ Mobile ⟷ E-mail)**:
  Quando o time precisa desenhar uma experiência unificada e contínua: o usuário começa o cadastro no desktop, valida o token de e-mail no smartphone e continua o uso no aplicativo nativo iOS ou Android com total consistência de micro-cópias e hierarquias.
* **Fluxos de Retenção e Offboarding Ético (Cancelamentos)**:
  Ao desenvolver funis de cancelamento de assinatura que oferecem pausas temporárias, descontos de incentivo ou downgrade de plano sem apelar para *dark patterns* ardilosos que irritam o usuário e mancham a reputação da marca.

### 2.1 Emoção e Posicionamento Transmitidos

Adotar o rigor do Page Flows comunica ao visitante:
* **Autoridade Operacional Inquestionável**: A sensação de estar interagindo com uma ferramenta construída por veteranos da indústria de software, onde cada botão, input e espaçamento responde com precisão milimétrica.
* **Clareza Cognitiva e Conforto**: Eliminação de barreiras cognitivas; o usuário sempre sabe em que etapa está, quantos passos faltam para concluir a tarefa e qual é a consequência imediata de cada ação.
* **Previsibilidade e Confiança Bancária/Enterprise**: A aplicação de padrões consagrados (como cartões selecionáveis, bottom sheets e tabelas facetadas) transmite a segurança psicológica necessária para operações financeiras e gestão de dados sensíveis.

### 2.2 Aplicação na Regra 60-30-10

* **60% — Superfície Neutra & Espaço de Leitura**: 
  Fundos sóbrios (branco puro `#FFFFFF` ou ardósia `#F8FAFC` em interfaces web claras; grafite escuro `#0B0B0D` / `#18181B` em dashboards e no próprio player do Page Flows).
* **30% — Estrutura de Contêineres, Grids & Tipografia Escaneável**: 
  Linhas de divisão de `1px solid` (`#E2E8F0` em light ou `#27272A` em dark), títulos com alto peso visual (`font-semibold`), rótulos em cinza neutro (`#64748B` / `#A1A1AA`), campos de texto com cantos sutis (`rounded-lg`) e cartões com bordas nítidas.
* **10% — Acentos Semânticos de Ação & Status**: 
  Amarelo Canário (`#FEF08A` no Page Flows) ou Azul Primário / Índigo de marca (`#4F46E5`), Verde Esmeralda para estados de sucesso (`#10B981`), Âmbar para advertências (`#F59E0B`) e Vermelho Rubro para ações destrutivas ou erros (`#EF4444`).

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

* ⚠️ **Incompatível com Portfólios Experimentais e Agências de Vanguarda**:
  Projetos cujo objetivo primário é o choque visual, a exploração tridimensional em WebGL/Three.js, tipografias experimentais deformáveis ou micro-sites promocionais cinematográficos (Awwwards Site of the Year). O Page Flows é a bíblia da **usabilidade e eficácia de produto**, não da arte contemplativa descontextualizada.
* ⚠️ **Incompatível com Marcas de Moda de Luxo Avant-Garde**:
  Onde convenções tradicionais de usabilidade (como barras de busca padronizadas e wizards cartesianos) são intencionalmente subvertidas para criar mistério, exclusividade e distanciamento poético.
* ⚠️ **Armadilhas de Imitação (Cargo-Cult UX)**:
  * **Copiar Fluxos de Gigantes sem Adaptar ao Contexto**: Implementar um fluxo de cadastro de 8 passos porque a Uber ou a Amazon utilizam esse formato para checagem de antecedentes ou logística complexa. Em um MVP ou SaaS inicial, cada etapa adicional pode reduzir drasticamente a conversão.
  * **Ignorar Estados de Falha e Conexão Lenta**: Desenhar apenas o "caminho feliz" (*happy path*) visto nos vídeos sem prever telas de timeout de rede, erros de cartão de crédito não autorizado ou mensagens amigáveis de validação em linha.
  * **Onboarding Fatigue por Excesso de Questionários**: Tentar traçar o perfil completo do usuário antes de permitir que ele experimente o valor central do produto (violação direta dos princípios de Product-Led Growth).

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

A desconstrução analítica do Page Flows e dos produtos de seu acervo revela padrões técnicos de alta precisão que estruturam os softwares modernos mais bem-sucedidos do planeta.

```
┌──────────────────────────────────────────────────────────────────────────────────────────────────┐
│                             PAGE FLOWS STRUCTURAL ATOMIC MATRIX                                  │
├──────────────────────────────────────────────────────────────────────────────────────────────────┤
│ [ 1. HEADER & GLOBAL BAR ]  Logo Brand ──► Search Omni (CMD+K) ──► Tabs: iOS/Android/Web/Emails │
├──────────────────────────────────────────────────────────────────────────────────────────────────┤
│ [ 2. PRODUCT HERO STRIP ]   Logo 96px (rounded-full) ──► Title H1 ──► Category Tags ──► Actions  │
│                             Version Selector Dropdown (e.g., 'August 2025' vs 'May 2021')        │
├──────────────────────────────────────────────────────────────────────────────────────────────────┤
│ [ 3. DUAL-PANE WORKSPACE ]                                                                       │
│  ┌───────────────────────────────┐ ┌───────────────────────────────────────────────────────────┐  │
│  │ SIDEBAR DE FLUXOS (25%)       │ │ MAIN STAGE: VIDEO PLAYER + TIMELINE ANNOTATIONS (75%)     │  │
│  │ • Total: '23 Flows'           │ │ • HTML5 Video Stream (16:9 Desktop Web / 9:19.5 Mobile)   │  │
│  │ • Active: Onboarding          │ │ • Scrubber de Timecodes Sincronizados com data-seconds   │  │
│  │ • Adding a Product            │ │ • 'In this video' Interactive Step Index List             │  │
│  │ • Requesting Payment          │ │ • Clickable Timestamps (e.g. 00:04 Create account)        │  │
│  │ • 2FA Authentication          │ │ • Step Annotations with Direct Thumbnail Previews         │  │
│  │ • Exporting Data              │ └───────────────────────────────────────────────────────────┘  │
│  └───────────────────────────────┘                                                                │
├──────────────────────────────────────────────────────────────────────────────────────────────────┤
│ [ 4. SCREEN SCRUBBER SLIDER ] Carrossel Horizontal: 104 Telas com Skeleton Shimmer & Lightbox    │
└──────────────────────────────────────────────────────────────────────────────────────────────────┘
```

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo

1. **Layout Dual da Aplicação de Análise**:
   * O container principal utiliza uma largura máxima contida de `1440px` com preenchimento lateral de `24px` a `48px`.
   * A divisão entre a barra lateral de fluxos do produto (lista de 15 a 30 tarefas) e a área de exibição central segue uma proporção assimétrica modular de **25% (Sidebar) / 75% (Main Stage)** no desktop.
2. **Ritmo de 8pt e Escala de Espaçamento**:
   * Gaps padronizados em múltiplos estritos de 4px e 8px: `gap-2` (8px) para itens de menu, `gap-4` (16px) para cards secundários, `gap-6` (24px) para grids de telas e `gap-8` (32px) para seções principais.
3. **Divisores e Linhas Estruturais**:
   * Todas as superfícies são delimitadas por bordas nítidas de `1px solid` com opacidades calculadas (`border-zinc-800` / `rgba(255,255,255,0.08)` no tema escuro e `border-slate-200` / `#E2E8F0` nas telas claras inspecionadas).

### 4.2 Sistemas de Cores, Superfícies & Texturas

* **Fundo Mestre do Page Flows**: `#0B0B0D` (Preto Ónix profundo que absorve luz e anula reflexos em telas OLED).
* **Superfícies de Cards e Painéis de Controle**: `#18181B` (Zinc 900) e `#27272A` (Zinc 800) com cantos arredondados padronizados em `rounded-xl` (12px) e `rounded-2xl` (16px).
* **Acento Icônico de Alta Energia**: `#FEF08A` (Amarelo Canário / Pastel Luminoso) com texto em `#0B0B0D` para contraste AAA em botões principais de conversão.
* **Superfície de Telas SaaS Analisadas**: Fundo branco puro `#FFFFFF` sobre canvas `#F8FAFC`, criando um contraste visual natural quando emolduradas pelo player escuro da galeria.

---

### 4.3 Catálogo de Arquétipos & Padrões Visuais Extraídos

O Page Flows documenta detalhadamente 8 padrões de arquitetura visual e funcional que formam a espinha dorsal de qualquer aplicação moderna:

#### Arquétipo 1: Video Player Interativo com Scrubber Sincronizado e Anotações de Passo
* **Anatomia**: Janela de reprodução de vídeo (16:9 para web desktop ou 9:19.5 com máscara de dispositivo para iOS/Android) acoplada a uma lista vertical indexada (`ul#annotations`) com timecodes no formato `MM:SS`, títulos de passo (ex: `00:04 Create account`, `00:26 Set business name`, `01:42 Add product`) e atributos `data-seconds`.
* **Gatilho & Comportamento**: Ao clicar em qualquer passo da lista, o player salta instantaneamente para o segundo exato (`video.currentTime = targetSeconds`). Durante a reprodução contínua, o item de lista correspondente ao timecode atual recebe a classe `.active` com transição suave e rolagem automática para mantê-lo visível.
* **Aplicação**: Demonstrações guiadas de software, documentações de produtos complexos, tutoriais de ativação de onboarding e análises de auditoria de UX.

#### Arquétipo 2: Wizard de Onboarding com Perfilamento Progressivo (Progressive Profiling)
* **Anatomia**: Modal centralizado ou página dedicada com barra de progresso linear no topo (ex: "Passo 2 de 5"), título direto em pergunta interrogativa, grid de cards selecionáveis (tiles) com ícone vetorial, título curto e descrição, acompanhado por um botão primário largo no rodapé.
* **Gatilho & Comportamento**: Ao clicar em uma opção, o card ativa uma borda de 2px de cor primária com micro-escala (`scale(1.02)` via CSS) e desmarca opções mutuamente exclusivas. O botão "Continuar" passa de desabilitado (`opacity: 0.5; pointer-events: none`) para ativo imediatamente.
* **Aplicação**: Configuração inicial de workspaces, personalização de algoritmos e recomendação de templates (padrão Notion, Figma e Slack).

#### Arquétipo 3: Tela de Autenticação Híbrida Social + OTP de 6 Dígitos
* **Anatomia**: Contêiner vertical de `420px` centralizado. Botões de autenticação social em 1-clique (Google, Apple, GitHub) no topo; separador elegante com texto "OU"; campo de e-mail isolado. Ao submeter, a interface realiza uma transição suave para 6 caixas de input individuais dedicadas para o PIN de 6 dígitos recebido por e-mail ou SMS.
* **Gatilho & Comportamento**: O foco salta automaticamente para o próximo campo ao digitar um dígito (`auto-advance`). Suporte total a colar código completo (`onPaste` preenche os 6 campos instantaneamente e dispara a verificação sem requerer clique adicional).
* **Aplicação**: Telas de login e registro sem senha (*passwordless*), autorização de pagamentos sensíveis e ativação de 2FA.

#### Arquétipo 4: Seletor de Planos e Matriz de Preços com Modal de Confirmação
* **Anatomia**: Três colunas de precificação no topo com um alternador de periodicidade (Trimestral vs Anual com badge `-15% Best Value`). O plano principal ("Popular / Yearly") possui contorno iluminado, badge no topo e elevação de sombra.
* **Gatilho & Comportamento**: O clique em planos aciona modais estruturados: se for um downgrade, o modal exibe ícone de alerta vermelho/âmbar, lista explicativa dos recursos que serão perdidos e exige confirmação dupla; se for um upgrade, apresenta resumo pro-rata do valor com cálculo instantâneo da diferença cobrada no cartão.
* **Aplicação**: Páginas de checkout, upgrades in-app acionados por limites de cota e gestão de faturamento em configurações.

#### Arquétipo 5: Bottom Sheet com Arrasto Tátil (Mobile App Drawer)
* **Anatomia**: Painel que desliza da base da tela cobrindo de 40% a 90% da altura da viewport móvel. Possui uma barra de puxador arredondada (*pill handle*) no topo superior central (`width: 36px; height: 4px; background: #71717A; border-radius: 9999px`), cantos superiores com curvatura suave (`rounded-t-2xl`) e fundo com backdrop-blur.
* **Gatilho & Comportamento**: Abre via slide-up vertical (`translateY: 0%`). Pode ser fechado por gesto de deslizar para baixo (*swipe-down*) com física de mola ou por toque no overlay escuro semi-transparente.
* **Aplicação**: Filtros facetados em mobile, menus contextuais de três pontos, seletores de cartões de crédito e telas de confirmação rápida.

#### Arquétipo 6: Acervo de E-mails Transacionais Conectados ao Fluxo
* **Anatomia**: Visualizador que exibe a correspondência direta entre a ação do usuário na tela e o e-mail gerado pelo servidor (ex: "Boas-vindas", "Confirme seu e-mail", "Sua fatura do Stripe", "Seu período de testes expirará em 48h").
* **Gatilho & Comportamento**: Layout responsivo em moldura de cliente de e-mail com cabeçalho de remetente, assunto, pre-header e layout em largura máxima de `600px` com botões de chamada primária bem delimitados.
* **Aplicação**: Estratégias de retenção, nutrição de onboarding e garantia de consistência tipográfica/cromática entre web app e comunicações por e-mail.

#### Arquétipo 7: Pesquisa Global Multifacetada com Seletor de Ecossistema
* **Anatomia**: Barra de busca persistente no topo que abre uma paleta de sobreposição (*search overlay* estilo CMD+K). No canto superior direito da busca, ícones de filtro rápido alternam instantaneamente entre **iOS, Android, Web e Emails**.
* **Gatilho & Comportamento**: A digitação exibe sugestões instantâneas divididas em 4 abas semânticas: *Popular*, *Flows* (fluxos de tarefas), *Products* (marcas) e *UI Elements* (componentes isolados como Text Field, Bottom Sheet, Tabs e Cards).
* **Aplicação**: Sistemas de busca em grandes bancos de dados, command centers de software B2B e documentações de engenharia.

#### Arquétipo 8: Carrossel Horizontal de Telas em Alta Definição com Download em Lote
* **Anatomia**: Faixa horizontal contínua contendo as dezenas de capturas sequenciais que compõem a jornada gravada (ex: "104 Screens"). Cada miniatura exibe skeleton loading com gradiente animado durante o carregamento.
* **Gatilho & Comportamento**: Controles de navegação com setas laterais que utilizam scroll suave baseado em interpolação quadrática (`easeInOutQuad`). Clique em qualquer imagem aciona lightbox de tela cheia com zoom em 100% dos pixels nativos. Botão superior permite baixar todas as telas em um único arquivo ZIP.
* **Aplicação**: Galerias de portfólio de produto, auditorias de UX e apresentações de design para stakeholders executivos.

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Tokens CSS Fundamentais (Sistema Page Flows)

```css
:root {
  /* Canvas Mestre Page Flows (Dark Obsidian) */
  --pf-canvas-base: #0B0B0D;
  --pf-surface-panel: #18181B;
  --pf-surface-elevated: #27272A;
  --pf-surface-hover: #3F3F46;
  --pf-border-subtle: rgba(255, 255, 255, 0.08);
  --pf-border-strong: #3F3F46;

  /* Tipografia & Contrastes Neutros */
  --pf-text-primary: #FAFAFA;
  --pf-text-secondary: #A1A1AA;
  --pf-text-tertiary: #71717A;

  /* Acento de Conversão Primário (Canary Yellow) */
  --pf-accent-primary: #FEF08A;
  --pf-accent-hover: #FDE047;
  --pf-accent-contrast: #0B0B0D;

  /* Cores Semânticas de Status */
  --pf-status-success: #10B981;
  --pf-status-warning: #F59E0B;
  --pf-status-danger: #EF4444;
  --pf-status-info: #38BDF8;

  /* Curvaturas & Elevações */
  --pf-radius-sm: 6px;
  --pf-radius-md: 10px;
  --pf-radius-lg: 14px;
  --pf-radius-pill: 9999px;

  /* Física de Transição Semântica */
  --pf-ease-snappy: cubic-bezier(0.16, 1, 0.3, 1);
  --pf-transition-fast: 150ms var(--pf-ease-snappy);
  --pf-transition-normal: 250ms var(--pf-ease-snappy);
}
```

---

### 5.2 Componente Funcional: Interactive Flow Scrubber & Video Stage

Abaixo está a implementação completa e em nível de produção do componente mestre do Page Flows em **React 19, TypeScript, Tailwind CSS e Framer Motion**: um reprodutor de vídeo sincronizado com linha do tempo de anotações clicáveis que atualiza os passos automaticamente.

```tsx
import React, { useState, useRef, useEffect } from 'react';
import { motion, AnimatePresence } from 'framer-motion';
import { Play, Pause, Bookmark, Download, Share2, Layers, CheckCircle2, ChevronRight, Laptop, Smartphone } from 'lucide-react';

export interface FlowStepAnnotation {
  id: string;
  seconds: number;
  title: string;
  description: string;
  screenThumbnailUrl: string;
}

export interface UserFlowViewerProps {
  productName: string;
  productLogoUrl: string;
  flowTitle: string;
  platform: 'desktop-web' | 'ios' | 'android';
  videoSrc: string;
  videoPoster: string;
  annotations: FlowStepAnnotation[];
}

export const InteractiveUserFlowViewer: React.FC<UserFlowViewerProps> = ({
  productName,
  productLogoUrl,
  flowTitle,
  platform,
  videoSrc,
  videoPoster,
  annotations,
}) => {
  const videoRef = useRef<HTMLVideoElement | null>(null);
  const [isPlaying, setIsPlaying] = useState<boolean>(false);
  const [currentTime, setCurrentTime] = useState<number>(0);
  const [duration, setDuration] = useState<number>(0);
  const [activeStepIndex, setActiveStepIndex] = useState<number>(0);
  const [isBookmarked, setIsBookmarked] = useState<boolean>(false);

  // Sincroniza a anotação ativa conforme o vídeo progride
  const handleTimeUpdate = () => {
    if (!videoRef.current) return;
    const time = videoRef.current.currentTime;
    setCurrentTime(time);

    // Identifica o passo atual baseado nos segundos
    let currentIdx = 0;
    for (let i = 0; i < annotations.length; i++) {
      if (time >= annotations[i].seconds) {
        currentIdx = i;
      } else {
        break;
      }
    }
    setActiveStepIndex(currentIdx);
  };

  const handleLoadedMetadata = () => {
    if (videoRef.current) {
      setDuration(videoRef.current.duration);
    }
  };

  const togglePlay = () => {
    if (!videoRef.current) return;
    if (isPlaying) {
      videoRef.current.pause();
      setIsPlaying(false);
    } else {
      videoRef.current.play();
      setIsPlaying(true);
    }
  };

  const seekToSeconds = (seconds: number, index: number) => {
    if (!videoRef.current) return;
    videoRef.current.currentTime = seconds;
    setActiveStepIndex(index);
    if (!isPlaying) {
      videoRef.current.play();
      setIsPlaying(true);
    }
  };

  const formatTime = (timeInSecs: number): string => {
    const mins = Math.floor(timeInSecs / 60);
    const secs = Math.floor(timeInSecs % 60);
    return `${mins.toString().padStart(2, '0')}:${secs.toString().padStart(2, '0')}`;
  };

  const isMobile = platform === 'ios' || platform === 'android';

  return (
    <div className="w-full bg-[#0B0B0D] text-[#FAFAFA] min-h-screen font-sans border-t border-zinc-800">
      {/* Header do Fluxo com Identidade do Produto */}
      <header className="max-w-[1440px] mx-auto px-6 py-8 border-b border-zinc-800/80">
        <div className="flex flex-col md:flex-row md:items-center justify-between gap-6">
          <div className="flex items-center gap-5">
            <div className="w-16 h-16 rounded-full bg-zinc-900 border border-zinc-800 p-1 overflow-hidden flex-shrink-0 shadow-lg">
              <img src={productLogoUrl} alt={`${productName} logo`} className="w-full h-full object-cover rounded-full" />
            </div>
            <div>
              <div className="flex items-center gap-3">
                <span className="text-xs uppercase tracking-wider font-semibold text-zinc-400 bg-zinc-900 border border-zinc-800 px-2.5 py-1 rounded-full flex items-center gap-1.5">
                  {isMobile ? <Smartphone className="w-3 h-3 text-[#FEF08A]" /> : <Laptop className="w-3 h-3 text-[#FEF08A]" />}
                  {platform.toUpperCase().replace('-', ' ')}
                </span>
                <span className="text-xs text-zinc-500">•</span>
                <span className="text-xs text-zinc-400 font-medium">{annotations.length} Passos Registrados</span>
              </div>
              <h1 className="text-2xl md:text-3xl font-bold tracking-tight text-white mt-1">
                {flowTitle} em <span className="text-zinc-300">{productName}</span>
              </h1>
            </div>
          </div>

          {/* Ações Primárias do Fluxo */}
          <div className="flex items-center gap-3">
            <button
              onClick={() => setIsBookmarked(!isBookmarked)}
              className={`flex items-center gap-2 px-4 py-2.5 rounded-lg text-sm font-semibold border transition-all duration-200 ${
                isBookmarked
                  ? 'bg-zinc-800 border-zinc-700 text-[#FEF08A]'
                  : 'bg-zinc-900/80 border-zinc-800 text-zinc-300 hover:bg-zinc-800 hover:text-white'
              }`}
            >
              <Bookmark className="w-4 h-4 fill-current" />
              <span>{isBookmarked ? 'Salvo' : 'Salvar'}</span>
            </button>

            <button className="flex items-center gap-2 px-4 py-2.5 rounded-lg text-sm font-semibold bg-zinc-900/80 border border-zinc-800 text-zinc-300 hover:bg-zinc-800 hover:text-white transition-all duration-200">
              <Share2 className="w-4 h-4" />
              <span>Compartilhar</span>
            </button>

            <button className="flex items-center gap-2 px-5 py-2.5 rounded-lg text-sm font-bold bg-[#FEF08A] hover:bg-[#FDE047] text-[#0B0B0D] shadow-md transition-all duration-200">
              <Download className="w-4 h-4" />
              <span>Download ZIP</span>
            </button>
          </div>
        </div>
      </header>

      {/* Main Stage: Player de Vídeo e Linha do Tempo de Passos */}
      <main className="max-w-[1440px] mx-auto px-6 py-8">
        <div className="grid grid-cols-1 lg:grid-cols-12 gap-8">
          
          {/* Coluna do Player de Vídeo (7 ou 8 Colunas) */}
          <div className={`lg:col-span-8 flex flex-col items-center justify-start`}>
            <div className={`relative w-full overflow-hidden rounded-2xl bg-zinc-950 border border-zinc-800/90 shadow-2xl ${
              isMobile ? 'max-w-[420px] aspect-[9/19.5] mx-auto' : 'aspect-video'
            }`}>
              <video
                ref={videoRef}
                src={videoSrc}
                poster={videoPoster}
                onTimeUpdate={handleTimeUpdate}
                onLoadedMetadata={handleLoadedMetadata}
                onClick={togglePlay}
                className="w-full h-full object-cover cursor-pointer"
                playsInline
              />

              {/* Botão de Play/Pause Flutuante Central (quando pausado) */}
              <AnimatePresence>
                {!isPlaying && (
                  <motion.div
                    initial={{ opacity: 0, scale: 0.8 }}
                    animate={{ opacity: 1, scale: 1 }}
                    exit={{ opacity: 0, scale: 0.8 }}
                    onClick={togglePlay}
                    className="absolute inset-0 m-auto w-16 h-16 rounded-full bg-[#0B0B0D]/80 backdrop-blur-md border border-zinc-700/60 flex items-center justify-center cursor-pointer text-[#FEF08A] hover:scale-110 transition-transform shadow-2xl"
                  >
                    <Play className="w-7 h-7 fill-current ml-1" />
                  </motion.div>
                )}
              </AnimatePresence>

              {/* Barra de Controles Inferior Sobreposta */}
              <div className="absolute bottom-0 inset-x-0 bg-gradient-to-t from-black/90 via-black/40 to-transparent p-4 flex flex-col gap-2">
                {/* Linha de Progresso Contínua */}
                <div
                  className="w-full h-1.5 bg-zinc-700/60 hover:h-2.5 rounded-full cursor-pointer relative overflow-hidden transition-all"
                  onClick={(e) => {
                    const rect = e.currentTarget.getBoundingClientRect();
                    const pos = (e.clientX - rect.left) / rect.width;
                    if (videoRef.current) {
                      videoRef.current.currentTime = pos * duration;
                    }
                  }}
                >
                  <div
                    className="h-full bg-[#FEF08A] rounded-full relative"
                    style={{ width: `${(currentTime / (duration || 1)) * 100}%` }}
                  />
                </div>

                <div className="flex items-center justify-between text-xs font-mono text-zinc-300">
                  <div className="flex items-center gap-3">
                    <button onClick={togglePlay} className="hover:text-white transition-colors">
                      {isPlaying ? <Pause className="w-4 h-4 fill-current" /> : <Play className="w-4 h-4 fill-current" />}
                    </button>
                    <span>{formatTime(currentTime)} / {formatTime(duration)}</span>
                  </div>

                  <span className="text-[#FEF08A] font-sans font-semibold">
                    Etapa {activeStepIndex + 1} de {annotations.length}: {annotations[activeStepIndex]?.title}
                  </span>
                </div>
              </div>
            </div>
          </div>

          {/* Coluna da Linha do Tempo e Índice de Passos (4 Colunas) */}
          <div className="lg:col-span-4 flex flex-col bg-zinc-900/60 border border-zinc-800 rounded-2xl p-5 max-h-[640px] overflow-hidden">
            <div className="flex items-center justify-between pb-4 border-b border-zinc-800">
              <div className="flex items-center gap-2">
                <Layers className="w-4 h-4 text-[#FEF08A]" />
                <h2 className="text-base font-bold text-white tracking-tight">Neste Vídeo</h2>
              </div>
              <span className="text-xs font-mono text-zinc-400 bg-zinc-800/80 px-2.5 py-1 rounded-full">
                {annotations.length} etapas
              </span>
            </div>

            {/* Lista com rolagem independente dos passos anotados */}
            <div className="overflow-y-auto space-y-2 mt-4 pr-1">
              {annotations.map((step, idx) => {
                const isActive = activeStepIndex === idx;
                const isPassed = currentTime > step.seconds;

                return (
                  <motion.div
                    key={step.id}
                    onClick={() => seekToSeconds(step.seconds, idx)}
                    whileHover={{ x: 2 }}
                    className={`group flex items-start gap-3.5 p-3 rounded-xl cursor-pointer border transition-all duration-200 ${
                      isActive
                        ? 'bg-zinc-800/90 border-[#FEF08A]/60 shadow-md'
                        : 'bg-zinc-900/40 border-zinc-800/60 hover:bg-zinc-800/40 hover:border-zinc-700'
                    }`}
                  >
                    {/* Thumbnail Miniatura com Timecode */}
                    <div className="relative w-16 h-12 rounded-lg overflow-hidden bg-black flex-shrink-0 border border-zinc-800">
                      <img src={step.screenThumbnailUrl} alt={step.title} className="w-full h-full object-cover" />
                      <div className="absolute inset-0 bg-black/20 group-hover:bg-transparent transition-colors" />
                      <span className="absolute bottom-1 right-1 bg-black/80 font-mono text-[9px] px-1 py-0.5 rounded text-zinc-300">
                        {formatTime(step.seconds)}
                      </span>
                    </div>

                    {/* Informações Textuais do Passo */}
                    <div className="flex-1 min-w-0">
                      <div className="flex items-center justify-between">
                        <span className={`text-xs font-bold leading-none ${isActive ? 'text-[#FEF08A]' : 'text-zinc-200'}`}>
                          {idx + 1}. {step.title}
                        </span>
                        {isPassed && !isActive && (
                          <CheckCircle2 className="w-3.5 h-3.5 text-emerald-500/80 flex-shrink-0" />
                        )}
                      </div>
                      <p className="text-[11px] text-zinc-400 line-clamp-1 mt-1 font-normal">
                        {step.description}
                      </p>
                    </div>

                    <ChevronRight className={`w-4 h-4 mt-1 flex-shrink-0 transition-transform ${
                      isActive ? 'text-[#FEF08A] translate-x-0.5' : 'text-zinc-600 group-hover:text-zinc-400'
                    }`} />
                  </motion.div>
                );
              })}
            </div>
          </div>

        </div>
      </main>
    </div>
  );
};
```

---

### 5.3 Engenharia de Pesquisa ao Vivo para Agentes de IA

Quando um agente inteligente ou sistema automatizado precisar consultar o acervo ao vivo do Page Flows em busca de padrões para benchmarking, deve navegar utilizando a taxonomia de URLs canônicas da plataforma:

```
┌────────────────────────────────────────────────────────────────────────────────────────────────┐
│                             PAGE FLOWS URL ROUTING ENGINE SCHEMA                               │
├────────────────────────────────────────────────────────────────────────────────────────────────┤
│ 1. POR PLATAFORMA & FLUXO TAREFA:                                                              │
│    https://pageflows.com/{platform}/flows/{flow-slug}/                                         │
│    • iOS Onboarding:             https://pageflows.com/ios/flows/onboarding/                   │
│    • Desktop Web Checkout:       https://pageflows.com/web/flows/checkout/                     │
│    • Android Upgrade Flow:       https://pageflows.com/android/flows/upgrade/                  │
│    • Web Subscriptions:          https://pageflows.com/web/flows/subscribing/                  │
│    • Web Team Invites:           https://pageflows.com/web/flows/inviting-a-member/            │
│    • iOS Account Deletion:       https://pageflows.com/ios/flows/deleting-your-account/        │
├────────────────────────────────────────────────────────────────────────────────────────────────┤
│ 2. POR PRODUTO & TAREFA ESPECÍFICA (VÍDEO DETALHADO COM TIME-STAMPS):                          │
│    https://pageflows.com/post/{platform}/{flow-slug}/{product-slug}/                           │
│    • Stripe Web Onboarding:      https://pageflows.com/post/desktop-web/onboarding/stripe/     │
│    • Revolut iOS Onboarding:     https://pageflows.com/post/ios/onboarding/revolut/            │
│    • Notion Web Onboarding:      https://pageflows.com/post/desktop-web/onboarding/notion/     │
│    • Spotify iOS Upgrading:      https://pageflows.com/post/ios/upgrading/spotify/             │
│    • Slack Web Inviting:         https://pageflows.com/post/desktop-web/inviting-member/slack/│
├────────────────────────────────────────────────────────────────────────────────────────────────┤
│ 3. POR COMPONENTE DE UI ESPECÍFICO (ATOMIC SCREENS & ELEMENTS):                                │
│    https://pageflows.com/{platform}/elements/{element-slug}/                                   │
│    • Web Dashboards:             https://pageflows.com/web/screens/dashboard/                 │
│    • iOS Bottom Sheets:          https://pageflows.com/ios/elements/bottom-sheet/              │
│    • Web Pricing Tables:         https://pageflows.com/web/screens/pricing-plans/              │
│    • Android Text Fields:        https://pageflows.com/android/elements/text-field/            │
│    • iOS Segmented Tabs:         https://pageflows.com/ios/elements/tabs/                      │
├────────────────────────────────────────────────────────────────────────────────────────────────┤
│ 4. ACERVO DE E-MAILS DE CICLO DE VIDA (LIFECYCLE & TRANSACTIONAL):                            │
│    https://pageflows.com/emails/                                                               │
│    • Welcome Emails:             https://pageflows.com/emails/welcome/                         │
│    • Security / 2FA Emails:      https://pageflows.com/emails/verification/                    │
│    • Trial Expiring Alerts:      https://pageflows.com/emails/upgrade/                         │
├────────────────────────────────────────────────────────────────────────────────────────────────┤
│ 5. QUERY PARAMETERS DA API INTERNA DE BUSCA:                                                   │
│    https://pageflows.com/search/?q={termo}&request_inform={platform}&slug={type}               │
│    Exemplo: https://pageflows.com/search/?q=two-factor&request_inform=web&slug=userflows      │
└────────────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar o **Page Flows** como motor de referência para o projeto, inclua as seguintes especificações no `DESIGN_BLUEPRINT.md`:

1. **Jornada Dinâmica Obrigatória (Dynamic Journey Priority)**:
   * Proibir a prototipação de telas soltas ou mockups desconectados. Todo entregável de UI deve ser documentado como uma sequência finita de estados: `Estado Inicial` ──► `Micro-Interação de Entrada` ──► `Feedback Visual de Validação` ──► `Transição de Sucesso/Erro` ──► `Próxima Tela`.
2. **Redução Agressiva do Time-to-Value (TTV)**:
   * O fluxo de onboarding não deve conter mais de 4 telas antes de permitir que o usuário veja a interface do produto povoada com dados reais ou modelos personalizáveis.
3. **Clareza nos Modais de Pagamento e Assinatura**:
   * O comparativo de planos deve possuir alternador de periodicidade transparente, demonstrando explicitamente o custo mensal equivalente e a economia no faturamento anual.
   * Modais de downgrade devem obrigatoriamente esclarecer o que acontece com os dados cadastrados, projetos ativos e limites de membros.
4. **Respeito às Convenções Nativas de Cada Plataforma**:
   * Em dispositivos móveis (iOS/Android), priorizar ações de seleção secundária e filtros via **Bottom Sheet** acessível pelo polegar, em vez de modais flutuantes centralizados que bloqueiam a tela.
   * No desktop web, disponibilizar sempre atalhos de teclado (ex: `Esc` para fechar gavetas, `Enter` para avançar e `CMD+K` para busca omnidirecional).
5. **Acessibilidade e Micro-Cópias Humanizadas**:
   * Todos os campos de formulário devem possuir rótulos visíveis associados semanticamente via `id` e `htmlFor`. Mensagens de erro devem explicar exatamente como solucionar a pendência (ex: *"A senha deve ter pelo menos 8 caracteres com uma letra maiúscula"* em vez de *"Entrada inválida"*).
6. **Consistência Ponta a Ponta com E-mails Transacionais**:
   * A tipografia, o tom de voz e o botão primário de ação dos e-mails de confirmação e boas-vindas devem replicar identicamente o padrão visual do software web.

---

### Conclusão & Veredito Técnico

O **Page Flows** transcende o conceito tradicional de galeria de inspiração para se firmar como um **laboratório de engenharia reversa de experiência do usuário**. Sua curadoria sistemática de vídeos passo a passo, captura de telas reais de produtos líderes e categorização atômica em múltiplos dispositivos fornecem a base empírica e científica necessária para projetar softwares com usabilidade impecável, alta retenção de clientes e conversão comercial otimizada.
