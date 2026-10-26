---
id: "107-saasframe-io"
name: "SaaS Frame"
url: "https://www.saasframe.io/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico:
  - "Full-Funnel Lifecycle Architecture (Marketing ⟷ Onboarding ⟷ Product UI ⟷ Emails)"
  - "Product-Led Growth (PLG) & Immediate Time-to-Value UX"
  - "High-Density B2B Enterprise Data Layouts (KPI Cards, Data Tables, Faceted Filters)"
  - "Dual-Engine Neutral Canvas (Obsidian Dark App & Pristine Slate Web)"
  - "Atomic Component Scalability (Shadcn/Radix Primitives, Tailwind CSS, 1px Crisp Borders)"
  - "Frictionless Guided Onboarding (Checklists, Step Progressors & Empty State Primers)"
  - "Retention-Driven Lifecycle Messaging (Nudges, Drip Emails & Upgrade Modals)"
densidade_informacao: "Alta/Utilitaria (In-App Product UI) a Media/Narrativa (Landing Pages & Flows)"
impacto_visual: "Editorial/Sofisticado & High-Conversion Commercial Tech"
custo_computacional: "Baixo a Moderado (Renderização pura via DOM/CSS, layouts CSS Grid/Flexbox otimizados, aceleração por GPU em transições de drawers/modais, SVGs estáticos/dinâmicos para data visualization, zero sobrecarga de WebGL)"
stack_frameworks:
  - "Next.js 14/15 (App Router, Server Components & Dynamic Routing)"
  - "React 19 / TypeScript"
  - "Tailwind CSS v3/v4 (variantes de container queries, arbitrary values, borders especulares de 1px)"
  - "Framer Motion / Motion.dev (molas com amortecimento crítico, layout animations, AnimatePresence em drawers e modais)"
  - "Radix UI / Shadcn UI (primitivos acessíveis WAI-ARIA para dropdowns, dialogs, command palettes e tooltips)"
  - "Lucide React (iconografia semântica consistente de 1.5px e 2px)"
  - "Recharts / Tremor / Visx (gráficos analíticos e micro-sparklines responsivas)"
compatibilidade:
  fontes_ideais:
    - "Neo-Grotesks Modernos de Alta Legibilidade para Interfaces de Software: Inter, Geist Sans, Plus Jakarta Sans, Satoshi, General Sans, Archivo"
    - "Display Sans para Títulos e Propostas de Valor: Cal Sans, Cabinet Grotesk, PP Neue Montreal, Clash Display"
    - "Monoespaçadas para Métricas Técnicas, IDs de Registro e Tabelas: Geist Mono, JetBrains Mono, Fira Code, Space Mono"
  paletas_ideais:
    - "SaaS Frame Enterprise Indigo (Padrão Light In-App & Web): #0F172A (Texto/Slate 900), #F8FAFC (Canvas Fundo Slate 50), #FFFFFF (Superfície Cards/Painéis), #4F46E5 / #6366F1 (Acento Primário Indigo), #E2E8F0 (Bordas Estruturais 1px), #10B981 (Sucesso/MRR Positivo), #EF4444 (Alerta/Churn)"
    - "Obsidian Deep Tech Dashboard (Padrão Dark Mode Produto): #090D16 (Fundo Espacial Escuro), #0F172A (Superfície Elevada de Painéis), #1E293B (Bordas de Alta Precisão 1px), #818CF8 (Índigo Iluminado para Contraste), #38BDF8 (Azul Ciano para Dados Secundários), #F1F5F9 (Tipografia Primária Alabastro)"
    - "FinTech Trust & Monocromo Esmeralda: #064E3B (Verde Floresta Profundo), #10B981 (Acento Esmeralda Primário), #ECFDF5 (Superfície Suave de Destaque), #0F172A (Texto de Alta Densidade), #E5E7EB (Divisores Neutros)"
    - "Regra 60-30-10 de Arquitetura de Software: 60% Superfície Neutra de Fundo (Branco puro `#FFFFFF`, Ardósia `#F8FAFC` ou Grafite `#090D16`), 30% Estrutura de Contêineres, Grids, Linhas Divisórias e Tipografia Escaneável, 10% Acentos Semânticos de Ação e Status (Botões de Ação Primária, Badges de Status, Deltas Positivos/Negativos em KPIs)"
  combinacoes_recomendadas:
    - "Barra de navegação lateral (Sidebar) colapsável com alternador de workspace, agrupamento semântico de rotas e badge de versão/status"
    - "Cabeçalho de aplicação com Command Bar (CMD+K), seletor de perfil, notificações com sino animado e atalhos rápidos"
    - "Cards de KPI com tipografia monoespaçada nas métricas, badge de porcentagem com cor contextual (verde/vermelho) e micro-gráfico de linha (Sparkline)"
    - "Checklist de onboarding progressivo com barra de preenchimento percentual ('4 de 6 etapas concluídas') e CTA de desbloqueio"
    - "Empty states explicativos com ilustrações vetoriais monocromáticas, texto explicativo do benefício e botão de ação direta para cadastrar o primeiro item"
    - "Tabela de dados densa com paginação, ordenação de colunas, filtros facetados e menu de ações em cascata de três pontos"
    - "Modais de upgrade in-app comparando limites do plano gratuito com os multiplicadores do plano Pro/Enterprise"
  conflitos_esteticos:
    - "Desconexão entre a estética da landing page de marketing e a interface real do software (marketing ultramoderno com app interno antiquado)"
    - "Telas de onboarding com questionários longos e invasivos antes de permitir ao usuário experimentar o produto (destrói o Time-to-Value do PLG)"
    - "Empty states mudos (apenas um quadrado cinza dizendo 'Sem registros', sem instrução ou botão para criar o primeiro registro)"
    - "Interfaces com tipografias decorativas extravagantes (fontes serifadas pesadas ou manuscritas aplicadas em painéis de métricas e tabelas)"
    - "Uso indiscriminado de sombras escuras e difusas (blur > 30px) em botões e tabelas, gerando aspecto amador e sujo"
    - "Falta de hierarquia cromática de status: utilizar a mesma cor de destaque da marca para botões destrutivos ou mensagens de erro"
    - "Sequestro da rolagem (scroll-jacking) ou animações pesadas de entrada que travam a visualização ágil de dados operacionais"
---

# SaaS Frame — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
███████╗ █████╗  █████╗ ███████╗    ███████╗██████╗  █████╗ ███╗   ███╗███████╗
██╔════╝██╔══██╗██╔══██╗██╔════╝    ██╔════╝██╔══██╗██╔══██╗████╗ ████║██╔════╝
███████╗███████║███████║███████╗    █████╗  ██████╔╝███████║██╔████╔██║█████╗  
╚════██║██╔══██║██╔══██║╚════██║    ██╔══╝  ██╔══██╗██╔══██║██║╚██╔╝██║██╔══╝  
███████║██║  ██║██║  ██║███████║    ██║     ██║  ██║██║  ██║██║ ╚═╝ ██║███████╗
╚══════╝╚═╝  ╚═╝╚═╝  ╚═╝╚══════╝    ╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝╚═╝     ╚═╝╚══════╝
```

---

## 1. DNA Estético & Filosofia de Curadoria

Fundado pelo estrategista de crescimento, indie hacker e designer de produto **Alex Milkoff** em 2020 — com o lançamento monumental da versão **SaaSFrame 2.0** em fevereiro de 2023 —, o **SaaS Frame** (`https://www.saasframe.io/`) consolidou-se como o acervo técnico e banco de inteligência visual definitivo para engenheiros de software, fundadores de produtos digitais e designers de produto focados no modelo **SaaS (Software-as-a-Service)**.

A gênese da plataforma nasceu de uma dor visceral no desenvolvimento moderno de software: enquanto a web estava repleta de galerias contemplativas de landing pages estáticas (que mostram apenas o "lado de fora da loja") e de arquivos de telas mobile isoladas, **não existia um repositório estruturado que conectasse todo o ciclo de vida do cliente de software**. 

Um produto SaaS bem-sucedido não é apenas uma página de apresentação atraente; ele é uma máquina coordenada composta por:
1. **Atração & Conversão**: Landing pages, comparativos de recursos e matrizes de precificação.
2. **Ativação & Primeiro Uso**: Telas de login/cadastro, onboarding progressivo, criação de workspace e checklists de ativação.
3. **Engajamento & Uso Diário**: Painéis operacionais (dashboards), ferramentas analíticas, tabelas densas de dados, estados vazios (*empty states*) e paletas de comando.
4. **Monetização & Expansão**: Modais de upgrade in-app, avisos de limite de cota, faturamento e gestão de equipe.
5. **Retenção & Re-engajamento**: Sequências de e-mails transacionais de boas-vindas, alertas de uso e gatilhos de reativação.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        THE SAAS FRAME FULL-FUNNEL MATRIX                               │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  [ MARKETING & CONVERSION ]  ──► [ ACTIVATION & ONBOARDING ] ──► [ CORE IN-APP UI ]    │
│   • High-Converting Landing       • 1-Click Social Sign-Up        • Sticky Sidebar App │
│   • Pricing Tiers & Usage         • Progressive Profiling Quiz    • Real-time Dashboards│
│   • Feature Comparison            • Workspace Initialization      • Data Tables & CRUD │
│   • Social Proof & Wall           • Interactive Checklist         • Empty State Guides │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  [ MONETIZATION / PAYWALL ]  ◄── [ RETENTION / LIFECYCLE ]   ◄── [ SETTINGS / TEAMS ]  │
│   • In-App Upgrade Modals         • Automated Welcome Drips       • Role-Based Access  │
│   • Usage Quota Limit Bars        • Milestone Celebration Mail    • API Keys & Webhooks│
│   • Stripe-Powered Billing        • Inactivity Re-engagement      • Audit Logs & Teams │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 O Abismo entre "Landing Pages Isoladas" e a "Interface Real do Software"

O SaaS Frame atua como a cura para a chamada **Síndrome da Casca Vazia**: situações em que uma startup contrata uma agência para desenhar uma landing page exuberante com gradientes complexos e 3D, mas, após o usuário criar a conta, depara-se com um software árido, desorganizado, sem hierarquia visual e com usabilidade sofrível.

A filosofia do SaaS Frame prega o **Design Sistêmico Unificado**:
- **Consistência Atômica Contínua**: O botão primário, a paleta de cores neutras, os raios de curvatura de borda (`rounded-md`, `rounded-lg`) e a escala tipográfica do site externo devem ser idênticos aos do dashboard autenticado.
- **Transparência de Produto no Topo do Funil**: Em vez de ilustrações abstratas ou metáforas conceituais, as landing pages modernas do SaaS Frame exibem capturas de alta resolução da interface real do software com animações de micro-interações, permitindo ao usuário entender o produto antes de criar a conta.
- **Product-Led Growth (PLG) por Arquitetura**: A interface é projetada para conduzir o usuário ao *"Momento Aha!"* no menor número de cliques possível, usando dados simulados de alta qualidade ou guias de autoatendimento.

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

O SaaS Frame é a **Referência Primária de Direção de Arte e Arquitetura de UI/UX** nos seguintes contextos de projeto:

1. **Desenvolvimento de Aplicações Web B2B, Micro-SaaS e Plataformas Empresariais**:
   - Criação de sistemas com autenticação de usuários, organizações multilocatárias (*multi-tenant*), controle de acesso baseado em funções (*RBAC*) e painéis de controle.
2. **Projetos Orientados a Product-Led Growth (PLG)**:
   - Softwares em que o próprio produto é o canal primário de aquisição, retenção e expansão. O SaaS Frame oferece o padrão-ouro de checklists de ativação, fluxos de boas-vindas sem fricção e empurrões contextuais de valor (*activation nudges*).
3. **Engenharia de Telas de Faturamento, Upgrades e Limites de Uso**:
   - Desenho de paywalls elegantes, barras de consumo de quota (ex: "85% dos créditos de IA utilizados"), modais de upgrade contextual que aparecem exatamente no ponto em que o usuário tenta utilizar um recurso premium, e telas de checkout autoexplicativas.
4. **Alinhamento do Design System Corporativo (Design Tokens Compartilhados)**:
   - Padronização de tokens de cor, tipografia e espaçamento entre o site de marketing em Next.js e o produto autenticado, garantindo transição sem atrito para o usuário final.
5. **Automação de E-mails de Ciclo de Vida do Cliente**:
   - Referência para estruturação de e-mails transacionais em HTML: confirmação de conta com código numérico grande, boas-vindas com 3 passos para começar, avisos de faturas geradas e e-mails de recuperação de contas inativas.
6. **Que Emoção Esse Estilo Comunica**:
   - Comunica **rigor técnico, alta previsibilidade, confiabilidade corporativa, estabilidade de infraestrutura e eficiência operacional**. O usuário sente que está utilizando uma ferramenta de classe mundial projetada para aumentar sua produtividade, e não um experimento instável.

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

### 3.1 Incompatibilidades Setoriais Críticas
- ⚠️ **Websites de Experiência Imersiva Avant-Garde e Festivais Culturais**: O estilo SaaS Frame é estritamente utilitário e orientado a tarefas. Aplicá-lo em festivais de cinema, galerias de arte contemporânea ou selos musicais resultará em uma experiência fria e corporativa.
- ⚠️ **Marcas de Luxo Haute Couture e Joalheria Exclusiva**: O luxo tradicional necessita de espaço negativo massivo, tipografia com serifas nobres, narrativas visuais cinemáticas e recusa explícita de pragmatismo técnico. Dashboards com tabelas e métricas destroem o mistério da alta costura.
- ⚠️ **Jogos Eletrônicos Fantásticos e Portfólios Lúdicos de Ilustração**: O grid regular de 12 colunas, bordas cinzentas de 1px e paletas de cores neutras do SaaS não transmitem a fantasia, organicidade e expressividade necessárias para o entretenimento interativo não utilitário.

### 3.2 Armadilhas de Imitação (Anti-Padrões de SaaS UI)

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        ANTI-PADRÕES CRÍTICOS EM SAAS UI/UX                            │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  ❌ O "Empty State Mudo"        │  ✅ O "Empty State Construtivo"                      │
│     Quadrado cinza vazio com    │     Ilustração minimalista, explicação clara do      │
│     texto "Sem registros".      │     benefício e botão "Criar Novo Projeto (+)".      │
├─────────────────────────────────┼──────────────────────────────────────────────────────┤
│  ❌ O "Onboarding Interrogatório"│  ✅ O "Onboarding Progressivo"                       │
│     Formulário de 12 campos     │     Apenas e-mail/senha no início; perfilamento      │
│     antes de acessar o app.     │     gradual em etapas opcionais de 1 clique.         │
├─────────────────────────────────┼──────────────────────────────────────────────────────┤
│  ❌ O "Upgrade Wall Opressivo"  │  ✅ O "Upgrade Contextual Transparente"              │
│     Bloqueio total de tela sem  │     Modal mostrando o que você ganha com o Pro,      │
│     explicar qual limite acabou.│     comparativo de recursos e botão de teste grátis. │
├─────────────────────────────────┼──────────────────────────────────────────────────────┤
│  ❌ A "Tabela Ilegível"         │  ✅ A "Tabela Densa com Hierarquia"                  │
│     Texto sem alinhamento, sem  │     Alinhamento numérico à direita, badges com cor   │
│     paginação e sem hover.      │     semântica, filtros facetados e menu de ações.    │
└─────────────────────────────────┘
```

1. **O Empty State Mudo**: Deixar uma página em branco quando o usuário entra pela primeira vez na plataforma. Um empty state deve sempre atuar como um professor silencioso: explicar o valor do recurso, fornecer dados de exemplo ou template inicial e oferecer um botão de ação primária em destaque para cadastrar o primeiro elemento.
2. **O Onboarding Interrogatório**: Forçar o usuário a preencher dados de tamanho da empresa, telefone, cargo e metas de faturamento antes de permitir que ele veja uma única tela do software. No ecossistema moderno catalogado pelo SaaS Frame, o onboarding é curto, com seleção rápida de objetivos via cartões clicáveis e carregamento imediato do ambiente.
3. **Upgrade Wall Opressivo e Punitivo**: Interromper o fluxo do usuário com um modal vermelho agressivo exigindo cartão de crédito imediato. O padrão moderno de paywall utiliza mensagens construtivas: *"Você atingiu o limite de 5 projetos do plano Free. Faça o upgrade para o Pro e desbloqueie projetos ilimitados e suporte prioritário."*
4. **Desconexão de Micro-Copy nos E-mails**: Enviar e-mails transacionais gerados automaticamente pelo backend com design cru sem logotipo, remetente impessoal (`no-reply@dominio.com`) e sem um botão primário com link mágico de retorno direto para a tarefa pendente no aplicativo.
5. **Sobrecarga de Cores de Acento Concorrentes**: Misturar roxo, azul, verde e laranja em botões da mesma tela sem uma convenção semântica clara. A cor de ação primária deve ser reservada para a ação que move o usuário para a frente no funil de trabalho.

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                      ANATOMIA DE UM SAAS APP DE ALTA PERFORMANCE                       │
├─────────────────────────┬──────────────────────────────────────────────────────────────┤
│ [WORKSPACE SWITCHER]    │ [BREADCRUMBS]           [SEARCH / CMD+K]  [NOTIF] [PROFILE]  │
├─────────────────────────┼──────────────────────────────────────────────────────────────┤
│  • Dashboard            │ [BANNER DE UPGRADE / STATUS DE TRIAL: 7 DIAS RESTANTES]      │
│  • Análise & Relatórios │                                                              │
│  • Clientes & Contatos  │ ┌──────────────┐ ┌──────────────┐ ┌──────────────┐ ┌───────┐ │
│  • Automações           │ │ KPI Card 1   │ │ KPI Card 2   │ │ KPI Card 3   │ │ Card 4│ │
│  • Integrações          │ │ $48,250 MRR  │ │ 1,420 Ativos │ │ 99.4% Uptime │ │ +14%  │ │
│                         │ └──────────────┘ └──────────────┘ └──────────────┘ └───────┘ │
│ [SEÇÃO SECUNDÁRIA]      │                                                              │
│  • Configurações        │ ┌──────────────────────────────────────────────────────────┐ │
│  • Membros da Equipe    │ │ TABELA DE DADOS / VISUALIZAÇÃO PRINCIPAL COM FILTROS     │ │
│  • Faturamento & Planos │ │ [Filtro ▾] [Buscar...]              [+ Criar Registro]   │ │
├─────────────────────────┤ │ ID    Nome        Plano     Status      Data      Ações  │ │
│ [STORAGE QUOTA / PRO]   │ │ #01   Acme Corp   Pro       Ativo       Hoje      [···]  │ │
│ 85% dos créditos usados │ │ #02   Stark Inc   Enterprise Ativo      Ontem     [···]  │ │
│ [Fazer Upgrade ▲]       │ └──────────────────────────────────────────────────────────┘ │
└─────────────────────────┴──────────────────────────────────────────────────────────────┘
```

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo

1. **A Estrutura de Dois Eixos (Sidebar Navigation + Main Canvas)**:
   - **Sidebar Esquerda (Navegação Persistente)**: Largura padronizada de `240px` a `280px` (`w-60` a `w-72` no Tailwind), com capacidade de colapso para modo compacto de `64px` a `72px` (apenas ícones com tooltips de apoio).
   - **Main Canvas (Área de Trabalho)**: Flexível com preenchimento de `100% - w_sidebar`, margens internas controladas de `24px` a `32px` (`p-6` a `p-8`), e contenção máxima em viewports ultrawide (`max-w-7xl mx-auto`).
   - **Top Header Fixo (Global Utility Bar)**: Altura padrão de `56px` a `64px` (`h-14` a `h-16`), com linha divisória de `1px solid #E2E8F0` (light) ou `1px solid #1E293B` (dark), contendo breadcrumbs à esquerda e busca global/notificações/avatar à direita.
2. **Escala de Espaçamento Harmônico de 4px / 8px**:
   - Todo o sistema de interface baseia-se na progressão geométrica: `4px` (gaps entre ícone e rótulo), `8px` (padding interno de botões e itens de menu), `12px` (espaçamento de campos de formulário), `16px` (gap entre cartões de métricas), `24px` (separação de seções lógicas) e `32px` (topo da área de trabalho).
3. **Alinhamento Numérico e Escaneabilidade em Tabelas**:
   - Colunas textuais (Nomes, E-mails, Categorias) são alinhadas estritamente à **esquerda**.
   - Colunas numéricas (Receita, Quantidade, Porcentagem, Datas) são alinhadas estritamente à **direita**, facilitando a comparação vertical de grandezas pelo usuário.
   - Status operacionais utilizam **Badges Pílula** com indicador luminoso de bolinha (`w-2 h-2 rounded-full`) e texto em tamanho `12px` com peso `font-medium`.

---

### 4.2 Sistemas de Cores, Superfícies & Texturas

1. **Neutral Slate Palette & Níveis de Elevação**:
   - As interfaces mais sofisticadas documentadas no SaaS Frame abandonam o preto absoluto `#000000` em favor do **Slate Profundo** (`#0F172A` / `#090D16`), conferindo densidade sem reflexo artificial.
   - **Camadas de Superfície (Hierarchy of Surfaces)**:
     - Fundo do Canvas: `#F8FAFC` (light) | `#090D16` (dark).
     - Contêineres e Cartões: `#FFFFFF` (light) | `#0F172A` (dark).
     - Menus Flutuantes, Dropdowns e Tooltips: `#FFFFFF` com `box-shadow: 0 10px 15px -3px rgba(0,0,0,0.1)` (light) | `#1E293B` com borda fina especular `rgba(255,255,255,0.08)` (dark).
2. **Cores Semânticas com Papel Funcional Invariável**:
   - **Primary Action (Brand Core)**: Índigo elétrico (`#4F46E5` / `#6366F1`) ou Violeta vibrante (`#7C3AED`) reservado exclusivamente para botões que concluem processos, criam novos registros ou confirmam compras.
   - **Success & Growth**: Esmeralda luminoso (`#10B981` / `#059669`) para métricas de faturamento (MRR/ARR), deltas positivos de crescimento (`+24.5%`), status *"Ativo"* e confirmações de pagamento.
   - **Warning & Caution**: Âmbar dourado (`#F59E0B` / `#D97706`) para avisos de cota próxima do limite (`85% utilizado`), trials que expiram em menos de 3 dias e pendências de validação.
   - **Danger & Destructive**: Rosa carmesim / Vermelho vivo (`#EF4444` / `#DC2626`) para cancelamento de assinaturas, remoção de chaves de API, deleção de workspaces e falhas de cobrança.

---

### 4.3 Catálogo Detalhado de 10 Arquétipos Estruturais Extraídos do SaaS Frame

#### Arquétipo 1: O Sticky App Sidebar com Navigation Collapse & Workspace Switcher
- **Anatomia**:
  - Topo: Menu dropdown com logotipo da organização ativa, avatar da empresa, plano atual (badge *"PRO"* em miniatura) e alternador rápido para trocar de organização com atalho de teclado.
  - Centro: Lista hierárquica de navegação dividida em grupos rotulados em caixa alta (ex: `PRINCIPAL`, `GERENCIAMENTO`, `SISTEMA`). Cada item possui um ícone em estilo contorno de 18px, rótulo textual e badge numérico opcional para notificações não lidas.
  - Base: Barra de consumo de armazenamento ou limite de requisições com botão sutil de upgrade, seguida pelo card de perfil do usuário logado (foto, nome, e-mail e chevron para menu de configurações de conta).
- **Gatilho de Interação**: Hover com transição de cor em 150ms; animação de transição fluida na largura da sidebar de 260px para 72px ao clicar no botão de recolhimento, preservando a usabilidade por atalhos de tooltip.

#### Arquétipo 2: O KPI Metric Card com Indicador de Delta Percentual e Micro Sparkline
- **Anatomia**:
  - Cabeçalho do card: Rótulo da métrica em corpo reduzido (`13px`, tom neutro `#64748B`), ícone de suporte no canto superior direito e tooltip informativo para esclarecer a regra de cálculo da métrica.
  - Valor Monumental: Número expresso em tipografia monoespaçada ou sans-serif com peso 700 e escala de `28px` a `32px` (ex: `$128,430.00`).
  - Rodapé do card: Badge de comparação temporal (`↑ 18.2% vs mês anterior`) com fundo verde suave `#ECFDF5` e texto `#059669`, acompanhado por uma micro-sparkline SVG de 80px de largura traçando a tendência dos últimos 30 dias.
- **Gatilho de Interação**: Hover com leve elevação do contêiner (`translate-y-[-2px]`) e realce do ponto de dados na sparkline com tooltip flutuante exibindo o valor exato daquele dia.

#### Arquétipo 3: O Stepper de Onboarding Progressivo com Checklist de Ativação ("Time-to-Value")
- **Anatomia**:
  - Cabeçalho motivacional: *"Configure seu ambiente em 4 etapas rápidas para desbloquear o piloto automático"*.
  - Barra de progresso horizontal fina indicando a porcentagem de conclusão (ex: *"75% completo — resta apenas 1 etapa"*).
  - Lista de 4 a 5 tarefas acionáveis com caixas de checagem interativas:
    1. *Crie seu primeiro projeto* (Concluído ✔️).
    2. *Convide 2 membros da equipe* (Concluído ✔️).
    3. *Conecte seu repositório GitHub ou banco de dados* (Concluído ✔️).
    4. *Dispare seu primeiro teste em produção* (Pendente — com botão azul *"Iniciar agora →"*).
- **Gatilho de Interação**: Ao concluir uma etapa, uma micro-animação de confetes ou pulso de cor esmeralda confirma a ação e a barra de progresso avança com física elástica. Opção de colapsar o checklist em uma pílula flutuante no canto inferior direito para não atrapalhar o uso livre.

#### Arquétipo 4: O Empty State Guiado com Ação Primária de Povoamento (First-Time User Experience)
- **Anatomia**:
  - Moldura de contorno tracejada (`border-dashed border-2 border-slate-200`) centralizada na área de conteúdo.
  - Ícone vetorial estilizado em dois tons dentro de um círculo suave (ex: pasta com sinal de adição).
  - Título propositivo e direto: *"Nenhuma campanha criada ainda"*.
  - Descrição orientada a benefício: *"As campanhas automatizadas permitem enviar sequências personalizadas para leads assim que eles se cadastram no seu site."*.
  - Botão duplo: Botão primário chamativo `[+ Criar Minha Primeira Campanha]` + Botão secundário de link `[Carregar Modelo de Exemplo]`.
- **Gatilho de Interação**: O botão de exemplo povoa a interface instantaneamente com dados simulados e etiquetas *"DEMO"*, permitindo que o usuário explore filtros e relatórios antes de conectar dados reais de produção.

#### Arquétipo 5: A Tabela de Dados Densos com Filtros Facetados, Busca Global e Ações em Linha
- **Anatomia**:
  - Barra de ferramentas da tabela: Campo de busca com ícone de lupa e atalho `[/]` para focar o cursor, menu dropdown de filtros com contador de critérios ativos (ex: `Status: Ativo, Plano: Enterprise`), seletor de colunas visíveis e botão primário `[Exportar CSV]`.
  - Cabeçalho de colunas: Títulos com indicadores de ordenação com duplo chevron (`asc / desc`), largura redimensionável e alinhamento semântico.
  - Linhas com altura confortável (`h-12` a `h-14`): Primeira coluna com checkbox de seleção múltipla, avatar com iniciais do cliente, status em badge com luz colorida e coluna final fixa com menu dropdown de três pontos `[···]` contendo opções como *Editar*, *Pausar*, *Duplicar* e *Excluir registro*.
- **Gatilho de Interação**: Efeito sutil de zebra ou realce de linha ao passar o cursor (`hover:bg-slate-50/80` no light ou `hover:bg-slate-800/50` no dark), com barra de ações em lote flutuante que surge na parte inferior da tela ao selecionar mais de 2 linhas.

#### Arquétipo 6: O Command Palette (CMD+K / Ctrl+K) para Navegação Ultrarrápida
- **Anatomia**:
  - Modal com fundo escurecido com desfoque de vidro (`backdrop-blur-sm`).
  - Campo de entrada no topo em tamanho grande (18px) com texto de ajuda: *"Digite um comando ou pesquise clientes, projetos e configurações..."*.
  - Resultados agrupados instantaneamente por categorias com badges visuais: `NAVEGAÇÃO RÁPIDA`, `AÇÕES RECENTES`, `CLIENTES ENCONTRADOS`, `CONFIGURAÇÕES`.
  - Rótulos de atalhos de teclado alinhados à direita de cada item em pequenas teclas estilizadas: `[↵ Enter para abrir]`, `[Tab para alternar]`.
- **Gatilho de Interação**: Disparado instantaneamente por evento de teclado global (`keydown` ouvindo `cmd+k` ou `ctrl+k`), navegável 100% pelas setas direcionais do teclado com seleção ativa em destaque azulado e foco automático.

#### Arquétipo 7: O In-App Upgrade Modal com Comparador Contextual de Limites
- **Anatomia**:
  - Título focado em produtividade: *"Desbloqueie colaboradores ilimitados no Plano Pro"*.
  - Ilustração de badge de diamante ou raio de energia com brilho gradiente no topo.
  - Barra comparativa visual de capacidade: *"Plano Atual (Free): 3 de 3 vagas utilizadas (100%)"* vs *"Plano Pro: Assentos Ilimitados + Permissões Avançadas por Função"*.
  - Matriz com 3 a 5 benefícios de destaque com ícones verdes de checagem.
  - Seletor de cobrança Anual (badge `Economize 20%`) vs Mensal, com valor por assento/mês.
  - Botão de ação primária de alta visibilidade `[Atualizar para o Pro Agora]` + link seguro com selo SSL e Stripe Checkout.
- **Gatilho de Interação**: Entrada com animação de escala e desvanecimento suave (`scale from 0.95 to 1.0`, `duration: 200ms`), mantendo fechamento fácil via tecla `Escape` ou clique no backdrop.

#### Arquétipo 8: O Drawer Deslizante de Detalhes de Registro (Slide-Over Inspection Panel)
- **Anatomia**:
  - Painel lateral que desliza a partir da borda direita da tela cobrindo de `480px` a `600px` sem fazer o usuário perder o contexto da tabela subjacente.
  - Cabeçalho do Drawer: Título do registro inspecionado, ID em fonte monoespaçada com botão de cópia de 1 clique, botão de fechar `[✕]` e atalho `Esc`.
  - Abas internas de navegação: `Geral`, `Histórico de Atividades`, `Faturas & Pagamentos`, `Logs de API`.
  - Formulário de edição inline com botões flutuantes no rodapé: `[Salvar Alterações]` e `[Cancelar]`.
- **Gatilho de Interação**: Transição horizontal acelerada por GPU (`translateX(0)` com curva de amortecimento rápida `cubic-bezier(0.16, 1, 0.3, 1)`), com backdrop escurecido suave que preserva a legibilidade da tabela no fundo.

#### Arquétipo 9: O Template de E-mail de Ciclo de Vida Transacional / Nudge de Ativação
- **Anatomia**:
  - Cabeçalho limpo com logotipo minimalista da marca em vetor (PNG/SVG retina-ready) centralizado sobre fundo neutro.
  - Mensagem direta em tom de consultor de produto: *"Olá Leonardo, vimos que você integrou seu banco de dados com sucesso ontem! Aqui está a última etapa para ativar os alertas em tempo real."*.
  - Bloco visual de ação única: Botão primário largo de alta legibilidade com contraste rigoroso `[Ativar Alertas em Tempo Real →]`.
  - Dica de suporte: Miniatura com link para o vídeo de 2 minutos ou documentação de ajuda.
  - Rodapé com links legais obrigatórios (CAN-SPAM/GDPR), endereço físico da empresa e link de desinscrição com 1 clique (*Unsubscribe preferences*).
- **Gatilho de Interação**: Compatibilidade universal com clientes de e-mail (Gmail, Outlook, Apple Mail), construído com HTML semântico baseado em tabelas responsivas e estilos inline para evitar quebra de renderização.

#### Arquétipo 10: A Matriz de Precificação Multi-Tier com Faturamento Dinâmico por Assentos
- **Anatomia**:
  - Alternador de ciclo de faturamento no topo (`Mensal` vs `Anual com 2 Meses Grátis`).
  - Slider ou seletor numérico dinâmico: *"Quantos assentos sua equipe precisa?"* (com cálculo automático do valor mensal final).
  - Três tiers verticais:
    - *Starter*: Para criadores solos e experimentação inicial gratuita.
    - *Team (Recomendado)*: Destacado com borda iluminada de 2px na cor da marca, badge *"Mais Escolhido"* e botão primário sólido.
    - *Enterprise*: Focado em segurança corporativa (SSO SAML, SLAs de 99.99%, suporte 24/7 dedicado) com botão `[Falar com Especialistas]`.
- **Gatilho de Interação**: Interpolação suave dos números de preço através de contadores animados quando o usuário move o slider de assentos ou altera a chave mensal/anual.

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Tokens CSS Semânticos para Aplicações SaaS (Tailwind & CSS Moderno)

```css
:root {
  /* Camada 1: Superfícies e Telas de Fundo */
  --saas-canvas-bg: #f8fafc;
  --saas-panel-bg: #ffffff;
  --saas-panel-elevated: #ffffff;
  --saas-sidebar-bg: #ffffff;
  
  /* Camada 2: Bordas Estruturais e Divisores */
  --saas-border-subtle: #e2e8f0;
  --saas-border-strong: #cbd5e1;
  --saas-border-focus: #6366f1;
  
  /* Camada 3: Tipografia e Textos */
  --saas-text-heading: #0f172a;
  --saas-text-body: #334155;
  --saas-text-muted: #64748b;
  --saas-text-faint: #94a3b8;
  
  /* Camada 4: Cores de Ação e Semânticas de Produto */
  --saas-primary: #4f46e5;
  --saas-primary-hover: #4338ca;
  --saas-primary-glow: rgba(79, 70, 229, 0.15);
  
  --saas-success: #10b981;
  --saas-success-bg: #ecfdf5;
  --saas-warning: #f59e0b;
  --saas-warning-bg: #fffbeb;
  --saas-danger: #ef4444;
  --saas-danger-bg: #fef2f2;
  
  /* Camada 5: Raios e Sombras Utilitárias */
  --saas-radius-sm: 6px;
  --saas-radius-md: 10px;
  --saas-radius-lg: 14px;
  --saas-radius-xl: 20px;
  
  --saas-shadow-card: 0 1px 3px 0 rgba(0, 0, 0, 0.04), 0 1px 2px -1px rgba(0, 0, 0, 0.04);
  --saas-shadow-floating: 0 10px 15px -3px rgba(0, 0, 0, 0.08), 0 4px 6px -4px rgba(0, 0, 0, 0.03);
  --saas-shadow-modal: 0 25px 50px -12px rgba(15, 23, 42, 0.25);
}

/* Modo Escuro (Obsidian Deep Tech Dashboard) */
.dark, [data-theme="dark"] {
  --saas-canvas-bg: #090d16;
  --saas-panel-bg: #0f172a;
  --saas-panel-elevated: #1e293b;
  --saas-sidebar-bg: #0b0f19;
  
  --saas-border-subtle: #1e293b;
  --saas-border-strong: #334155;
  --saas-border-focus: #818cf8;
  
  --saas-text-heading: #f8fafc;
  --saas-text-body: #cbd5e1;
  --saas-text-muted: #94a3b8;
  --saas-text-faint: #64748b;
  
  --saas-primary: #6366f1;
  --saas-primary-hover: #4f46e5;
  --saas-primary-glow: rgba(99, 102, 241, 0.25);
  
  --saas-success: #34d399;
  --saas-success-bg: rgba(16, 185, 129, 0.12);
  --saas-warning: #fbbf24;
  --saas-warning-bg: rgba(245, 158, 11, 0.12);
  --saas-danger: #f87171;
  --saas-danger-bg: rgba(239, 68, 68, 0.12);
  
  --saas-shadow-card: 0 1px 3px 0 rgba(0, 0, 0, 0.4);
  --saas-shadow-floating: 0 10px 25px -5px rgba(0, 0, 0, 0.6);
  --saas-shadow-modal: 0 25px 50px -12px rgba(0, 0, 0, 0.85);
}
```

---

### 5.2 Física de Movimento & Transições de Software

Em interfaces de software como as catalogadas no SaaS Frame, o movimento nunca deve ser ornamental ou lento; ele existe para **fornecer feedback de estado, preservar o modelo mental do usuário e conferir sensação de velocidade e precisão**:

- **Abertura de Drawers e Modais (Slide-Overs & Dialogs)**:
  - Curva de transição: `cubic-bezier(0.16, 1, 0.3, 1)` (curva de desaceleração suave inspirada no macOS/iOS).
  - Duração: `240ms` a `300ms`.
  - Configuração de Mola no Framer Motion: `transition: { type: "spring", stiffness: 380, damping: 30 }`.
- **Alternância de Abas e Indicadores Flutuantes (`layoutId`)**:
  - Configuração: `transition: { type: "spring", stiffness: 500, damping: 35 }`. Elimina qualquer sensação de salto brusco ao trocar de aba ativa.
- **Colapso e Expansão da Barra Lateral (Sidebar Toggle)**:
  - Duração: `200ms ease-in-out` aplicada estritamente a `width`, `min-width` e `padding`.
- **Micro-Hover em Linhas de Tabelas e Menus**:
  - Duração: `120ms ease-out` aplicada a `background-color` e `color`. A velocidade rápida cria uma resposta tátil quase instantânea aos olhos do usuário.

---

### 5.3 Receita de Código Funcional: SaaS Enterprise Dashboard com Sidebar, KPIs & Data Table

Abaixo encontra-se a implementação completa de uma interface de software moderna inspirada nos padrões de alta densidade e acabamento refinado do **SaaS Frame**. O componente inclui Sidebar responsiva com Workspace Switcher, Barra Superior com Busca global, Cards de KPI com sparkline SVG integrada, Checklist de Onboarding progressivo e Tabela de dados densa com alternador para Empty State:

```tsx
import React, { useState } from 'react';
import { motion, AnimatePresence } from 'framer-motion';
import {
  LayoutDashboard,
  Users,
  CreditCard,
  Settings,
  Bell,
  Search,
  ChevronDown,
  TrendingUp,
  TrendingDown,
  ArrowUpRight,
  MoreVertical,
  Plus,
  CheckCircle2,
  Circle,
  Sparkles,
  Command,
  ExternalLink,
  ShieldCheck,
  FolderPlus
} from 'lucide-react';

// Tipagem de dados de exemplo
interface ClientRecord {
  id: string;
  company: string;
  contact: string;
  plan: 'Starter' | 'Pro' | 'Enterprise';
  status: 'Ativo' | 'Trial' | 'Inadimplente';
  mrr: string;
  growth: string;
  isPositive: boolean;
  renewalDate: string;
}

const SAMPLE_CLIENTS: ClientRecord[] = [
  {
    id: 'CLI-8491',
    company: 'Acme Technologies Inc.',
    contact: 'sarah.vance@acme.io',
    plan: 'Enterprise',
    status: 'Ativo',
    mrr: '$4,850.00',
    growth: '+14.2%',
    isPositive: true,
    renewalDate: '15 Nov 2026',
  },
  {
    id: 'CLI-8492',
    company: 'NovaCloud Systems',
    contact: 'julian.k@novacloud.com',
    plan: 'Pro',
    status: 'Ativo',
    mrr: '$1,290.00',
    growth: '+8.5%',
    isPositive: true,
    renewalDate: '02 Dez 2026',
  },
  {
    id: 'CLI-8493',
    company: 'HyperScale AI Lab',
    contact: 'elena.rostova@hyperscale.dev',
    plan: 'Enterprise',
    status: 'Trial',
    mrr: '$5,400.00',
    growth: '+32.1%',
    isPositive: true,
    renewalDate: '28 Out 2026',
  },
  {
    id: 'CLI-8494',
    company: 'PulseMetrics Studio',
    contact: 'marcus.t@pulse.design',
    plan: 'Starter',
    status: 'Inadimplente',
    mrr: '$290.00',
    growth: '-4.1%',
    isPositive: false,
    renewalDate: '21 Out 2026',
  },
];

export const SaasDashboardShowcase: React.FC = () => {
  const [activeTab, setActiveTab] = useState<'all' | 'enterprise' | 'pro'>('all');
  const [showEmptyState, setShowEmptyState] = useState<boolean>(false);
  const [checklistCompleted, setChecklistCompleted] = useState<{ [key: number]: boolean }>({
    1: true,
    2: true,
    3: false,
    4: false,
  });

  const toggleChecklist = (id: number) => {
    setChecklistCompleted(prev => ({ ...prev, [id]: !prev[id] }));
  };

  const completedCount = Object.values(checklistCompleted).filter(Boolean).length;
  const progressPercent = (completedCount / 4) * 100;

  return (
    <div className="min-h-screen bg-[#F8FAFC] text-[#0F172A] font-sans flex antialiased">
      {/* 1. APP SIDEBAR PERSISTENTE */}
      <aside className="w-64 border-r border-[#E2E8F0] bg-white flex flex-col justify-between p-4 hidden md:flex shrink-0">
        <div>
          {/* Workspace Switcher */}
          <div className="flex items-center justify-between p-2.5 rounded-xl border border-[#E2E8F0] bg-[#F8FAFC] hover:bg-[#F1F5F9] transition-colors cursor-pointer mb-6">
            <div className="flex items-center gap-2.5">
              <div className="w-8 h-8 rounded-lg bg-[#4F46E5] text-white flex items-center justify-center font-bold text-sm shadow-sm">
                SF
              </div>
              <div className="text-left">
                <p className="text-xs font-bold leading-tight text-[#0F172A]">SaaSFrame Engine</p>
                <span className="text-[10px] text-[#64748B] font-medium flex items-center gap-1">
                  <span className="w-1.5 h-1.5 rounded-full bg-emerald-500"></span>
                  Plano Enterprise
                </span>
              </div>
            </div>
            <ChevronDown className="w-4 h-4 text-[#94A3B8]" />
          </div>

          {/* Navegação Primária */}
          <nav className="space-y-1">
            <p className="px-3 text-[11px] font-semibold text-[#94A3B8] uppercase tracking-wider mb-2">
              Workspace
            </p>
            <a
              href="#dashboard"
              className="flex items-center gap-3 px-3 py-2 rounded-lg text-sm font-semibold bg-[#4F46E5]/10 text-[#4F46E5] transition-all"
            >
              <LayoutDashboard className="w-4 h-4" />
              Visão Geral
            </a>
            <a
              href="#clients"
              className="flex items-center justify-between px-3 py-2 rounded-lg text-sm font-medium text-[#64748B] hover:text-[#0F172A] hover:bg-[#F8FAFC] transition-all"
            >
              <div className="flex items-center gap-3">
                <Users className="w-4 h-4" />
                Clientes & Contas
              </div>
              <span className="text-[11px] font-mono bg-[#E2E8F0] text-[#475569] px-2 py-0.5 rounded-full">
                48
              </span>
            </a>
            <a
              href="#billing"
              className="flex items-center gap-3 px-3 py-2 rounded-lg text-sm font-medium text-[#64748B] hover:text-[#0F172A] hover:bg-[#F8FAFC] transition-all"
            >
              <CreditCard className="w-4 h-4" />
              Faturamento & Planos
            </a>
            <a
              href="#settings"
              className="flex items-center gap-3 px-3 py-2 rounded-lg text-sm font-medium text-[#64748B] hover:text-[#0F172A] hover:bg-[#F8FAFC] transition-all"
            >
              <Settings className="w-4 h-4" />
              Configurações
            </a>
          </nav>
        </div>

        {/* Upgrade / Quota Card na Base */}
        <div className="p-3.5 rounded-xl border border-[#E2E8F0] bg-[#F8FAFC] space-y-2.5">
          <div className="flex items-center justify-between text-xs">
            <span className="font-semibold text-[#334155] flex items-center gap-1.5">
              <Sparkles className="w-3.5 h-3.5 text-[#4F46E5]" />
              Créditos de IA
            </span>
            <span className="font-mono text-[#64748B]">82%</span>
          </div>
          <div className="w-full bg-[#E2E8F0] h-1.5 rounded-full overflow-hidden">
            <div className="bg-[#4F46E5] h-full w-[82%] rounded-full"></div>
          </div>
          <p className="text-[11px] text-[#64748B] leading-tight">
            Você utilizou 41.000 de 50.000 créditos mensais.
          </p>
          <button className="w-full text-xs font-semibold py-1.5 text-[#4F46E5] bg-white border border-[#E2E8F0] hover:bg-[#F1F5F9] rounded-lg shadow-2xs transition-colors">
            Aumentar Cota
          </button>
        </div>
      </aside>

      {/* 2. MAIN APPLICATION WORKSPACE */}
      <div className="flex-1 flex flex-col min-w-0 overflow-y-auto">
        {/* Top Header com Busca e Ações Rápidas */}
        <header className="h-16 border-b border-[#E2E8F0] bg-white px-6 flex items-center justify-between sticky top-0 z-10">
          <div className="flex items-center gap-4 flex-1 max-w-md">
            <div className="relative w-full">
              <Search className="w-4 h-4 text-[#94A3B8] absolute left-3 top-1/2 -translate-y-1/2" />
              <input
                type="text"
                placeholder="Pesquisar clientes, faturas ou ações rápidas... (Pressione /)"
                className="w-full pl-9 pr-12 py-1.5 text-xs bg-[#F8FAFC] border border-[#E2E8F0] rounded-lg focus:outline-none focus:border-[#4F46E5] focus:bg-white transition-all placeholder:text-[#94A3B8]"
              />
              <div className="absolute right-2.5 top-1/2 -translate-y-1/2 flex items-center gap-0.5 text-[10px] font-mono bg-white border border-[#CBD5E1] text-[#64748B] px-1.5 py-0.5 rounded shadow-2xs">
                <Command className="w-2.5 h-2.5" /> K
              </div>
            </div>
          </div>

          <div className="flex items-center gap-3">
            {/* Toggle de Demonstração: Estado Normal vs Empty State */}
            <button
              onClick={() => setShowEmptyState(!showEmptyState)}
              className="text-xs font-medium text-[#4F46E5] bg-[#4F46E5]/10 hover:bg-[#4F46E5]/20 px-3 py-1.5 rounded-lg transition-colors"
            >
              Alternar para {showEmptyState ? 'Tabela Normal' : 'Empty State'}
            </button>

            <button className="relative p-2 rounded-lg text-[#64748B] hover:text-[#0F172A] hover:bg-[#F8FAFC] border border-[#E2E8F0] transition-colors">
              <Bell className="w-4 h-4" />
              <span className="w-2 h-2 rounded-full bg-emerald-500 absolute top-1.5 right-1.5 ring-2 ring-white"></span>
            </button>

            <div className="w-8 h-8 rounded-full bg-slate-200 border border-[#E2E8F0] overflow-hidden flex items-center justify-center font-bold text-xs text-[#475569]">
              AL
            </div>
          </div>
        </header>

        {/* Conteúdo Principal do Dashboard */}
        <main className="p-6 md:p-8 space-y-6 max-w-7xl mx-auto w-full">
          {/* Banner de Boas-Vindas e Ativação PLG */}
          <div className="flex flex-col sm:flex-row sm:items-center justify-between gap-4">
            <div>
              <h1 className="text-2xl font-bold tracking-tight text-[#0F172A]">
                Painel Executivo de Operações
              </h1>
              <p className="text-xs text-[#64748B] mt-0.5">
                Métricas atualizadas em tempo real há 2 minutos • Sincronização via Webhook Stripe
              </p>
            </div>
            <div className="flex items-center gap-2">
              <button className="px-3.5 py-2 text-xs font-semibold text-[#0F172A] bg-white border border-[#E2E8F0] hover:bg-[#F8FAFC] rounded-lg shadow-2xs transition-colors flex items-center gap-2">
                Exportar Relatório
              </button>
              <button className="px-3.5 py-2 text-xs font-semibold text-white bg-[#4F46E5] hover:bg-[#4338CA] rounded-lg shadow-sm transition-colors flex items-center gap-1.5">
                <Plus className="w-4 h-4" />
                Novo Cliente
              </button>
            </div>
          </div>

          {/* Stepper de Onboarding Progressivo (Checklist de Ativação) */}
          <div className="p-4 rounded-xl border border-[#E2E8F0] bg-white shadow-2xs space-y-3">
            <div className="flex items-center justify-between">
              <div className="flex items-center gap-2">
                <ShieldCheck className="w-4 h-4 text-[#4F46E5]" />
                <span className="text-xs font-bold text-[#0F172A]">
                  Checklist de Configuração da Sua Organização
                </span>
                <span className="text-[11px] font-mono text-[#64748B] bg-[#F1F5F9] px-2 py-0.5 rounded-md">
                  {completedCount} de 4 etapas concluídas ({progressPercent}%)
                </span>
              </div>
              <span className="text-[11px] text-[#4F46E5] font-semibold cursor-pointer hover:underline">
                Ocultar Guia
              </span>
            </div>

            <div className="w-full bg-[#F1F5F9] h-2 rounded-full overflow-hidden">
              <motion.div
                className="bg-emerald-500 h-full rounded-full"
                initial={{ width: 0 }}
                animate={{ width: `${progressPercent}%` }}
                transition={{ duration: 0.4 }}
              />
            </div>

            <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-2 pt-1">
              {[
                { id: 1, title: 'Conectar Chaves da API Stripe' },
                { id: 2, title: 'Convidar Primeiro Membro da Equipe' },
                { id: 3, title: 'Configurar Regras de Webhook' },
                { id: 4, title: 'Disparar Primeiro E-mail Transacional' },
              ].map(step => (
                <div
                  key={step.id}
                  onClick={() => toggleChecklist(step.id)}
                  className={`flex items-center gap-2.5 p-2 rounded-lg border text-xs cursor-pointer transition-colors ${
                    checklistCompleted[step.id]
                      ? 'border-emerald-200 bg-emerald-50/50 text-emerald-900'
                      : 'border-[#E2E8F0] hover:bg-[#F8FAFC] text-[#475569]'
                  }`}
                >
                  {checklistCompleted[step.id] ? (
                    <CheckCircle2 className="w-4 h-4 text-emerald-600 shrink-0" />
                  ) : (
                    <Circle className="w-4 h-4 text-[#94A3B8] shrink-0" />
                  )}
                  <span className={`text-[11px] ${checklistCompleted[step.id] ? 'line-through text-[#64748B]' : 'font-medium'}`}>
                    {step.title}
                  </span>
                </div>
              ))}
            </div>
          </div>

          {/* Cards de Métricas de Alto Desempenho (KPI Cards com Sparkline SVG) */}
          <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
            {[
              {
                title: 'Receita Mensal Recorrente (MRR)',
                value: '$54,280.00',
                delta: '+12.4%',
                isPositive: true,
                sparkline: 'M0 20 L20 18 L40 12 L60 14 L80 8 L100 2',
              },
              {
                title: 'Assinantes Ativos',
                value: '1,429',
                delta: '+8.1%',
                isPositive: true,
                sparkline: 'M0 18 L20 15 L40 16 L60 10 L80 9 L100 4',
              },
              {
                title: 'Churn Rate Médio',
                value: '1.24%',
                delta: '-0.3%',
                isPositive: true,
                sparkline: 'M0 5 L20 8 L40 10 L60 12 L80 15 L100 18',
              },
              {
                title: 'Ticket Médio (ARPU)',
                value: '$88.50',
                delta: '+4.8%',
                isPositive: true,
                sparkline: 'M0 16 L20 14 L40 11 L60 13 L80 7 L100 3',
              },
            ].map((kpi, idx) => (
              <div
                key={idx}
                className="p-5 rounded-xl border border-[#E2E8F0] bg-white shadow-2xs flex flex-col justify-between hover:shadow-xs transition-shadow"
              >
                <div className="flex items-center justify-between text-[#64748B]">
                  <span className="text-xs font-semibold">{kpi.title}</span>
                  <ArrowUpRight className="w-3.5 h-3.5 text-[#94A3B8]" />
                </div>

                <div className="my-3 flex items-baseline justify-between">
                  <p className="text-2xl font-bold font-mono text-[#0F172A] tracking-tight">
                    {kpi.value}
                  </p>
                  {/* Micro Sparkline SVG */}
                  <svg className="w-20 h-6 overflow-visible" viewBox="0 0 100 24">
                    <path
                      d={kpi.sparkline}
                      fill="none"
                      stroke={kpi.isPositive ? '#10B981' : '#EF4444'}
                      strokeWidth="2"
                      strokeLinecap="round"
                    />
                  </svg>
                </div>

                <div className="flex items-center gap-1.5 text-[11px]">
                  <span className="inline-flex items-center gap-0.5 font-semibold text-emerald-600 bg-emerald-50 px-1.5 py-0.5 rounded">
                    <TrendingUp className="w-3 h-3" />
                    {kpi.delta}
                  </span>
                  <span className="text-[#94A3B8]">vs período anterior</span>
                </div>
              </div>
            ))}
          </div>

          {/* 3. ÁREA DE DADOS: TABELA VS EMPTY STATE */}
          <div className="rounded-xl border border-[#E2E8F0] bg-white shadow-2xs overflow-hidden">
            {/* Cabeçalho da Tabela e Abas */}
            <div className="p-4 border-b border-[#E2E8F0] flex flex-col sm:flex-row sm:items-center justify-between gap-3">
              <div className="flex items-center gap-1">
                {(['all', 'enterprise', 'pro'] as const).map(tab => (
                  <button
                    key={tab}
                    onClick={() => setActiveTab(tab)}
                    className={`relative px-3 py-1.5 rounded-lg text-xs font-semibold transition-all ${
                      activeTab === tab
                        ? 'text-[#4F46E5] bg-[#4F46E5]/10'
                        : 'text-[#64748B] hover:text-[#0F172A] hover:bg-[#F8FAFC]'
                    }`}
                  >
                    {tab === 'all' && 'Todos os Clientes'}
                    {tab === 'enterprise' && 'Contas Enterprise'}
                    {tab === 'pro' && 'Assinaturas Pro'}
                  </button>
                ))}
              </div>

              <div className="flex items-center gap-2">
                <input
                  type="text"
                  placeholder="Filtrar por nome ou e-mail..."
                  className="px-3 py-1.5 text-xs bg-[#F8FAFC] border border-[#E2E8F0] rounded-lg focus:outline-none focus:border-[#4F46E5] text-[#0F172A]"
                />
                <button className="px-3 py-1.5 text-xs font-semibold text-[#475569] bg-white border border-[#E2E8F0] hover:bg-[#F8FAFC] rounded-lg shadow-2xs">
                  Filtros (2)
                </button>
              </div>
            </div>

            {/* Renderização Condicional: Tabela Densa vs Empty State Orientado a Ação */}
            {showEmptyState ? (
              <div className="py-16 px-6 text-center max-w-md mx-auto space-y-4">
                <div className="w-12 h-12 rounded-2xl bg-indigo-50 border border-indigo-100 text-[#4F46E5] flex items-center justify-center mx-auto shadow-2xs">
                  <FolderPlus className="w-6 h-6" />
                </div>
                <div>
                  <h3 className="text-base font-bold text-[#0F172A]">
                    Nenhum cliente cadastrado nesta exibição
                  </h3>
                  <p className="text-xs text-[#64748B] mt-1 leading-relaxed">
                    Comece importando sua lista de clientes existentes via arquivo CSV ou conecte sua conta Stripe para sincronização instantânea em segundo plano.
                  </p>
                </div>
                <div className="flex items-center justify-center gap-2 pt-2">
                  <button className="px-4 py-2 text-xs font-semibold text-white bg-[#4F46E5] hover:bg-[#4338CA] rounded-lg shadow-sm transition-colors flex items-center gap-2">
                    <Plus className="w-4 h-4" />
                    Cadastrar Primeiro Cliente
                  </button>
                  <button className="px-3.5 py-2 text-xs font-semibold text-[#0F172A] bg-white border border-[#E2E8F0] hover:bg-[#F8FAFC] rounded-lg shadow-2xs transition-colors">
                    Importar CSV
                  </button>
                </div>
              </div>
            ) : (
              <div className="overflow-x-auto">
                <table className="w-full text-left text-xs">
                  <thead className="bg-[#F8FAFC] border-b border-[#E2E8F0] text-[#64748B] font-semibold">
                    <tr>
                      <th className="py-3 px-4 w-10">
                        <input type="checkbox" className="rounded border-[#CBD5E1] text-[#4F46E5]" />
                      </th>
                      <th className="py-3 px-4">Empresa & Contato</th>
                      <th className="py-3 px-4">Plano</th>
                      <th className="py-3 px-4">Status</th>
                      <th className="py-3 px-4 text-right">MRR Atual</th>
                      <th className="py-3 px-4 text-right">Crescimento</th>
                      <th className="py-3 px-4">Próxima Renovação</th>
                      <th className="py-3 px-4 text-right">Ações</th>
                    </tr>
                  </thead>
                  <tbody className="divide-y divide-[#E2E8F0]">
                    {SAMPLE_CLIENTS.map(client => (
                      <tr
                        key={client.id}
                        className="hover:bg-[#F8FAFC]/80 transition-colors group cursor-pointer"
                      >
                        <td className="py-3.5 px-4">
                          <input type="checkbox" className="rounded border-[#CBD5E1] text-[#4F46E5]" />
                        </td>
                        <td className="py-3.5 px-4">
                          <div className="flex items-center gap-2.5">
                            <div className="w-7 h-7 rounded-lg bg-slate-100 border border-[#E2E8F0] flex items-center justify-center font-bold text-[10px] text-[#475569]">
                              {client.company.substring(0, 2).toUpperCase()}
                            </div>
                            <div>
                              <p className="font-semibold text-[#0F172A] group-hover:text-[#4F46E5] transition-colors">
                                {client.company}
                              </p>
                              <p className="text-[11px] text-[#64748B]">{client.contact}</p>
                            </div>
                          </div>
                        </td>
                        <td className="py-3.5 px-4">
                          <span
                            className={`inline-flex items-center px-2 py-0.5 rounded text-[11px] font-medium border ${
                              client.plan === 'Enterprise'
                                ? 'bg-indigo-50 border-indigo-200 text-[#4F46E5]'
                                : client.plan === 'Pro'
                                ? 'bg-sky-50 border-sky-200 text-sky-700'
                                : 'bg-slate-50 border-slate-200 text-slate-700'
                            }`}
                          >
                            {client.plan}
                          </span>
                        </td>
                        <td className="py-3.5 px-4">
                          <span className="inline-flex items-center gap-1.5 text-[11px] font-medium">
                            <span
                              className={`w-1.5 h-1.5 rounded-full ${
                                client.status === 'Ativo'
                                  ? 'bg-emerald-500'
                                  : client.status === 'Trial'
                                  ? 'bg-amber-500'
                                  : 'bg-rose-500'
                              }`}
                            ></span>
                            {client.status}
                          </span>
                        </td>
                        <td className="py-3.5 px-4 text-right font-mono font-bold text-[#0F172A]">
                          {client.mrr}
                        </td>
                        <td className="py-3.5 px-4 text-right font-mono text-[11px]">
                          <span
                            className={
                              client.isPositive ? 'text-emerald-600 font-semibold' : 'text-rose-600 font-semibold'
                            }
                          >
                            {client.growth}
                          </span>
                        </td>
                        <td className="py-3.5 px-4 text-[#64748B] font-mono text-[11px]">
                          {client.renewalDate}
                        </td>
                        <td className="py-3.5 px-4 text-right">
                          <button className="p-1 rounded text-[#94A3B8] hover:text-[#0F172A] hover:bg-[#E2E8F0] transition-colors">
                            <MoreVertical className="w-4 h-4" />
                          </button>
                        </td>
                      </tr>
                    ))}
                  </tbody>
                </table>
              </div>
            )}

            {/* Rodapé da Tabela com Paginação Semântica */}
            <div className="p-3.5 border-t border-[#E2E8F0] bg-[#F8FAFC] flex items-center justify-between text-xs text-[#64748B]">
              <span>Mostrando 1 a 4 de 48 contas</span>
              <div className="flex items-center gap-1">
                <button
                  disabled
                  className="px-2.5 py-1 rounded border border-[#E2E8F0] bg-white opacity-50 cursor-not-allowed text-[#94A3B8]"
                >
                  Anterior
                </button>
                <button className="px-2.5 py-1 rounded border border-[#4F46E5] bg-[#4F46E5] text-white font-semibold">
                  1
                </button>
                <button className="px-2.5 py-1 rounded border border-[#E2E8F0] bg-white hover:bg-[#F1F5F9] text-[#0F172A]">
                  2
                </button>
                <button className="px-2.5 py-1 rounded border border-[#E2E8F0] bg-white hover:bg-[#F1F5F9] text-[#0F172A]">
                  Próxima
                </button>
              </div>
            </div>
          </div>
        </main>
      </div>
    </div>
  );
};
```

---

### 5.4 Como a IA Deve Pesquisar ao Vivo no SaaS Frame

Quando um agente inteligente ou arquiteto de software precisar consultar referências reais de telas de produto no **SaaS Frame** (`https://www.saasframe.io/`), deve seguir o mapa de indexação e rotas de URL da plataforma:

1. **Navegação por Domínio Funcional (High-Level Collections)**:
   - *Marketing & Landing Pages*: `https://www.saasframe.io/pages`
   - *Fluxos Conectados de Usuário (User Flows)*: `https://www.saasframe.io/flows`
   - *Telas de Produto & Dashboards*: `https://www.saasframe.io/products`
   - *Campanhas de E-mail Transacional & Lifecycle*: `https://www.saasframe.io/emails`
2. **Páginas Específicas de Alta Conversão (Target Screen Slugs)**:
   - Para pesquisar matrizes de precificação B2B: pesquise por telas com a tag `pricing`, `upgrade-flow` ou `billing`.
   - Para pesquisar primeiros passos e ativação: pesquise por `onboarding`, `welcome-flow`, `empty-state` e `checklist`.
   - Para interfaces analíticas: pesquise por `dashboards`, `analytics`, `kpi-cards` e `data-tables`.
   - Para comunicação assíncrona: pesquise na aba `emails` por `welcome-email`, `trial-expiration` e `reactivation-nudge`.
3. **Filtros por Verticais SaaS (Industry Niches)**:
   - Ao criar produtos para nichos específicos, priorize filtros por verticais como: `Developer Tools`, `AI Assistants / LLM Co-Pilots`, `FinTech`, `Productivity & Project Management` e `CRM / Sales Enablement`.

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar o **SaaS Frame** como referência primária de direção de arte para o documento `DESIGN_BLUEPRINT.md` de um novo projeto, a equipe de engenharia e produto deve garantir conformidade estrita com o seguinte checklist:

### 6.1 Checklist de Conformidade Arquitetural (PLG & SaaS Engineering)
- [ ] **Unidade Visual entre Landing Page e Aplicação Autenticada**:
  - Utilizar a mesma paleta de neutros (`#F8FAFC` / `#0F172A`), a mesma tipografia sem serifa de alta legibilidade (Inter ou Geist Sans) e a mesma curvatura de borda (`rounded-xl` em cards, `rounded-lg` em botões) tanto no site de vendas quanto no interior do software.
- [ ] **Zero Empty States Mudas no Primeiro Login**:
  - Toda tabela ou listagem que estiver inicialmente sem dados deve exibir uma moldura pontilhada explicativa, um resumo de 2 linhas do valor da funcionalidade e um botão com ícone de adição para cadastrar o primeiro registro ou carregar dados demonstrativos.
- [ ] **Time-to-Value Imediato no Onboarding**:
  - Eliminar formulários de perfilamento complexos antes da primeira visualização da área de trabalho. Incluir um checklist de 3 a 4 etapas acionáveis com barra de progresso visível no topo da página inicial do software.
- [ ] **Alinhamento e Densidade Semântica em Tabelas**:
  - Textos alinhados à esquerda; números, valores financeiros e porcentagens alinhados à direita. Status com badge de pílula e ponto luminoso colorido. Menu de ações em cascata de três pontos na extremidade direita de cada linha.
- [ ] **Visibilidade Permanente de Cotas e Upgrades Amigáveis**:
  - Exibir barra de consumo de recursos (créditos de IA, espaço em disco, assentos de equipe) na barra lateral de navegação ou no cabeçalho, com gatilho claro e não punitivo para o modal de upgrade Pro.
- [ ] **Física de Movimento sem Perda de Produtividade**:
  - Manter transições de abertura de gavetas laterais e modais abaixo de `300ms` usando curvas elásticas suaves (`cubic-bezier(0.16, 1, 0.3, 1)` ou spring com amortecimento crítico). Desativar qualquer animação desnecessária quando a preferência do sistema operacional for `prefers-reduced-motion: reduce`.
