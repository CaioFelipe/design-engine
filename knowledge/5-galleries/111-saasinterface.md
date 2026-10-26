---
id: "111-saasinterface"
name: "SaaS Interface"
url: "https://saasinterface.com/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico:
  - "Post-Login B2B SaaS Application Architecture"
  - "Atomic Component-to-Page Taxonomy (26 Page Archetypes, 6 Component Families)"
  - "High-Density Data Grid & Workspace Ergonomics"
  - "Keyboard-Driven Navigation & Modern Command Palettes (Cmd+K)"
  - "Radix UI / Tailwind Utility Precision & 1px Hairline Surfaces"
  - "Enterprise Security, Billing & Settings Systems"
  - "Zero-Data Empty States & Product-Led Onboarding Flows"
densidade_informacao: "Alta/Utilitaria"
impacto_visual: "Minimalista/Silencioso & High-Utility Enterprise Tech"
custo_computacional: "Baixo (DOM estruturado, CSS Grid nativo, virtualização de listas, micro-interações aceleradas por GPU, zero sobrecarga WebGL)"
stack_frameworks:
  - "Next.js 14/15 / Nuxt 3 (App Router, Server Components & Suspense)"
  - "React 19 / TypeScript 5.x"
  - "Tailwind CSS v3/v4 (Container Queries, Hairline Borders, CSS Variables)"
  - "Framer Motion / Motion.dev (molas com amortecimento crítico, layout animations, AnimatePresence)"
  - "Radix UI / TanStack Table / Lucide React / Floating UI"
  - "TanStack Virtual (Virtualização de linhas em tabelas de alto volume)"
compatibilidade:
  fontes_ideais:
    - "Neo-Grotesks Neutras de Máxima Densidade Operacional: Inter, Geist Sans, Plus Jakarta Sans, SF Pro Display, Figtree"
    - "Display Sans de Alta Autoridade para Títulos e Cabeçalhos: Cabinet Grotesk, PP Neue Montreal, General Sans, Satoshi"
    - "Monoespaçadas para Hash IDs, Tokens de API, Dados Tabulares e Métricas: Geist Mono, JetBrains Mono, Fira Code, Roboto Mono"
  paletas_ideais:
    - "Zinc Alabaster & Enterprise Slate (Modo Claro B2B Canônico): #FFFFFF (Canvas Fundo), #F8FAFC / #F1F5F9 (Muted Panel / Table Header), #E2E8F0 (1px Hairline Border), #0F172A (Deep Slate Ink), #64748B (Secondary Text), #2563EB (Action Cobalt CTA), #10B981 (Success Green), #EF4444 (Destructive Rose)"
    - "Obsidian Workspace & Electric Cyan (Modo Escuro DevTools/AI): #090A0F (Canvas Deep Space), #12141C (Surface Panel), #1E2330 (Hairline Specular Border), #38BDF8 / #6366F1 (Primary Interactive Pulse), #F1F5F9 (Primary High-Contrast Ink), #94A3B8 (Secondary Slate), #34D399 (Operational Mint)"
    - "Neutral Carbon & Monochrome Titanium (Minimalismo Linear-like): #0D0E11 (Void Canvas), #16181D (Card Container), #23272F (Hairline Divider), #E6E8EC (Text Primary), #8B949E (Muted Text), #5E6AD2 (Signature Linear Violet Accent)"
    - "Regra 60-30-10 para Interfaces Internas de SaaS: 60% Superfície Neutra de Fundo e Contêineres de Trabalho (#FFFFFF ou #090A0F), 30% Estrutura de Informação (Bordas de 1px, Cabeçalhos de Tabela, Tipografia em Escala Escura/Clara, Barras Laterais de Navegação), 10% Acentos Semânticos e Ações Focadas (Botão de 'Salvar Alterações', Botão de Criação '+', Badges de Status 'Ativo/Pendente', Toasts de Sucesso)"
  combinacoes_recomendadas:
    - "Bifurcação analítica: Navegação entre Telas Inteiras de Aplicação (`/pages/`) e Padrões Atômicos Desacoplados (`/components/`)"
    - "Tabelas de dados com cabeçalhos fixos (sticky header), ordenação tri-state (asc/desc/none), seleção de linhas via checkbox e acionamento de barra flutuante de ações em lote (Bulk Actions Toolbar)"
    - "Painéis laterais deslizantes (Slide-over Drawers / Sheets) acionados por clique na linha da tabela, evitando troca desnecessária de página e preservando o contexto operacional do usuário"
    - "Modais de confirmação destrutiva com padrão 'Type-to-Confirm' (digite o nome do workspace para autorizar a exclusão)"
    - "Páginas de faturamento (Billing / Plan) com barras de progresso lineares de consumo de cota (Usage Quota Meters) e gatilho contextual de upgrade"
    - "Paleta de comandos globais acessível via `Cmd+K` com suporte a pesquisa difusa (fuzzy search), atalhos de teclado visíveis e navegação por setas"
  conflitos_esteticos:
    - "Interfaces com fundos saturados ou gradientes chamativos em áreas de dados (rouba o foco cognitivo da tomada de decisão)"
    - "Uso de sombras difusas e coloridas estilo 'Glow Neumórfico' sob botões utilitários em tabelas e cabeçalhos corporativos"
    - "Animações longas de entrada (> 350ms) que fazem o operador perder tempo esperando o modal ou o drawer terminar de abrir"
    - "Falta de estados vazios (Empty States) instrutivos: exibir telas brancas ou tabelas cinzas sem dados sem instruir como criar o primeiro item"
    - "Menus flutuantes e tooltips sem suporte a teclado (Tab / Esc / Arrow Keys) violando as diretrizes de acessibilidade WAI-ARIA"
    - "Botões de ação primária espalhados desordenadamente: em uma interface SaaS corporativa, cada tela deve ter apenas 1 botão de ação primária proeminente"
---

# SaaS Interface — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
 ███████╗ █████╗  █████╗ ███████╗   ██╗███╗   ██╗████████╗███████╗██████╗ ███████╗ █████╗  ██████╗███████╗
 ██╔════╝██╔══██╗██╔══██╗██╔════╝   ██║████╗  ██║╚══██╔══╝██╔════╝██╔══██╗██╔════╝██╔══██╗██╔════╝██╔════╝
 ███████╗███████║███████║███████╗   ██║██╔██╗ ██║   ██║   █████╗  ██████╔╝█████╗  ███████║██║     █████╗  
 ╚════██║██╔══██║██╔══██║╚════██║   ██║██║╚██╗██║   ██║   ██╔══╝  ██╔══██╗██╔══╝  ██╔══██║██║     ██╔══╝  
 ███████║██║  ██║██║  ██║███████║██╗██║██║ ╚████║   ██║   ███████╗██║  ██║██║     ██║  ██║╚██████╗███████╗
 ╚══════╝╚═╝  ╚═╝╚═╝  ╚═╝╚══════╝╚═╝╚═╝╚═╝  ╚═══╝   ╚═╝   ╚══════╝╚═╝  ╚═╝╚═╝     ╚═╝  ╚═╝ ╚═════╝╚══════╝
```

---

## 1. DNA Estético & Filosofia de Curadoria

O **SaaS Interface** (`https://saasinterface.com/`) é o principal repositório global e laboratório de benchmarking visual dedicado exclusivamente à **experiência pós-login de produtos de Software as a Service (SaaS), ferramentas corporativas B2B e aplicações Web modernas**. 

Enquanto a imensa maioria dos arquivos de design da internet (Awwwards, FWA, Land-book, One Page Love e Lapa Ninja) foca na **camada pré-login** — as páginas públicas de marketing, heróis chamativos e landing pages comerciais —, o SaaS Interface nasceu para solucionar o chamado **"Paradoxo Pós-Login"**: 90% da vida útil, da retenção de clientes e do valor transacional de um software acontecem **depois** que o usuário se autentica. 

Fundado e mantido pela dupla italiana de product designers e engenheiros frontend **Davide Pacilio** (`@DavidePacilio`) e **Pasquale Vitiello** (`@pacovitiello`) — as mentes responsáveis pelo ecossistema **Cruip** (`cruip.com`) e **SaaS Landing Page** (`saaslandingpage.com`, #106) —, o SaaS Interface estabeleceu o padrão de referência adotado oficialmente por times de produto de companhias como **Webflow, Paddle, Intel, Similarweb, Fastly, Circle, Voiceflow, Gorgias, GSoft e Unit**.

```
┌────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                              THE POST-LOGIN INTERFACE ENGINE TAXONOMY                                  │
├────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│  [ LEVEL 1: APPLICATION PAGES (26 ARCHETYPES) ]     ──► [ LEVEL 2: ATOMIC COMPONENTS (6 FAMILIES) ]    │
│   • Dashboards & Metrics Overviews                       • Modal & Dialog (Confirmation, Alert, Wizard)│
│   • Lists & Data Tables (Filtering, Sorting, Cells)      • Menu & Picker (Dropdowns, Color, Context)   │
│   • Settings & Workspace Configurations                  • Global Command Search (Cmd+K Palettes)      │
│   • Billing / Subscription Plans & Usage Quotas          • Side Panels (Slide-over Flyouts / Drawers)  │
│   • Kanban Boards, Calendars & Schedulers                • Advanced Faceted Filters & Filter Bars      │
│   • Canvas Builders, Editors & Visual Nodes              • Bulk Actions Sticky Floating Toolbars       │
│   • Onboarding Checklists & Guided Empty States                                                        │
├────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│  CORE METRIC: Time-to-Value (TTV), Ergonomia Cognitiva, Densidade de Dados & Acessibilidade WAI-ARIA   │
└────────────────────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 O Critério de Curadoria: Engenharia de Produto vs. Dribbble-ficação

A filosofia de curadoria do SaaS Interface rejeita radicalmente o conceito de "Dribbble-art" — interfaces conceituais com contrastes inacessíveis, sombras gigantescas fluorescentes, tipografia microscópica e ausência completa de tratamento para dados reais ou estados de erro. O critério de inclusão no SaaS Interface exige:

1. **Software em Produção Real**: Todas as telas catalogadas pertencem a aplicações comerciais ativas com milhares ou milhões de usuários ativos mensais (MAU).
2. **Tratamento Rigoroso de Edge Cases**: Telas com grandes volumes de dados (tabelas com 50 linhas, paginação complexa, textos longos com truncamento elíptico, múltiplos avatares sobrepostos).
3. **Ergonomia Operacional & Velocidade**: Padrões que priorizam o fluxo de trabalho contínuo do operador — redução de cliques para concluir tarefas, navegação por atalhos de teclado e persistência de contexto por meio de gavetas laterais (Drawers) e diálogos modais não bloqueantes.
4. **Alinhamento com Design Systems Modernos**: Padrões visuais construídos sob a influência direta de sistemas canônicos como **Vercel Design System / Geist UI**, **Linear Method**, **Stripe Dashboard**, **GitHub UI** e **Shopify Polaris**.

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

O SaaS Interface é a **Referência Canônica Primária de Arquitetura de Interface e UX** nos seguintes cenários:

- **Construção de Dashboards Analíticos e Painéis de Controle (Admin Consoles)**: Quando a interface precisa exibir métricas chave (MRR, churn, throughput, latência de API, conversão de funis) organizadas em cards modulares com sparklines, comparações percentuais em relação ao mês anterior e seletores de intervalo temporal (`Last 7 days`, `Month to Date`, `Custom Range`).
- **Engenharia de Tabelas de Dados Densas (Data-Heavy SaaS)**: Quando a aplicação gerencia listas de clientes, pedidos, faturas, logs de auditoria ou registros bancários, exigindo ordenação por coluna, seleção múltipla de linhas, ações em lote (Bulk Actions) e virtualização de renderização.
- **Desenvolvimento de Fluxos de Configuração e Permissões (Settings & RBAC)**: Projetos que demandam páginas de configurações com navegação secundária em abas verticais, cartões de perfil, gerenciadores de chaves de API com botão de cópia instantânea e matrizes de permissão por cargo (Owner, Admin, Member, Viewer).
- **Sistemas de Monetização, Faturamento e Planos (Billing & Subscription Management)**: Quando o produto requer interfaces para visualização de limites de cota (Usage Quotas), barras de consumo de créditos de IA, alternância de plano (Upgrade/Downgrade), gerenciamento de cartões de crédito e histórico de notas fiscais com download de PDF.
- **Fluxos de Ativação e Onboarding (Product-Led Growth)**: Criação de checklists interativos de primeiro uso com barras de progresso gamificadas ("3 de 5 passos concluídos"), modais de boas-vindas com seleção de caso de uso e telas de estado vazio (Empty States) instrutivas com botões de chamada primária.
- **Ferramentas de Produtividade Baseadas em Linha de Comando (Keyboard-First / DevTools)**: Aplicações voltadas para desenvolvedores, engenheiros de DevOps e operadores avançados que exigem paletas de comando no estilo `Cmd+K` para busca e execução de comandos sem tocar no mouse.

### 2.1 Emoção e Posicionamento de Marca

A estética curada no SaaS Interface transmite:
- **Confiabilidade Institucional e Solidez Operacional**: A interface passa a certeza inabalável de que o sistema é seguro, robusto e preparado para processar dados críticos sem falhas ou bugs visuais.
- **Velocidade e Ausência de Fricção**: A eliminação de ornamentos decorativos desnecessários comunica foco absoluto no trabalho a ser realizado (Jobs-to-be-Done).
- **Polimento Premium de Engenharia**: Linhas de 1px perfeitamente alinhadas, tipografia com entrelinha matemática e estados de interação imediatos demonstram alto nível de refinamento do time de desenvolvimento.

### 2.2 Aplicação Rigorosa da Regra 60-30-10 em Interfaces de Software

Diferente de websites institucionais onde a cor de destaque (10%) pode ocupar grandes blocos visuais, em **interfaces internas de SaaS** a distribuição de cor e peso precisa ser ainda mais disciplinada para evitar a fadiga visual do usuário que passa 8 horas por dia operando a tela:

```
┌────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                        A REGRA 60-30-10 EM INTERFACES DE SOFTWARE B2B (SAAS INTERFACE)                 │
├────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│  60% — SUPERFÍCIE BASE & CANVAS NEUTRO                                                                 │
│  • Modo Claro: #FFFFFF (Puro Papel) e #F8FAFC / #F1F5F9 (Superfície Slate de Contêiner)                 │
│  • Modo Escuro: #090A0F (Deep Obsidian) e #12141C (Surface Panel de Cards e Tabelas)                   │
│  • Garante contraste máximo e zero reflexo cognitivo em sessões de trabalho prolongadas               │
├────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│  30% — ESTRUTURA HIERÁRQUICA, LINHAS DE 1PX & TIPOGRAFIA                                               │
│  • Bordas estruturais de 1px (#E2E8F0 no claro / #1E2330 no escuro) separando colunas, linhas e cards  │
│  • Sidebar lateral escura ou neutra (240px a 280px fixos) com navegação em árvore                     │
│  • Tipografia em escala mono/sans (Títulos em 600/700, labels em 500, dados em 400/500 mono)            │
│  • Cabeçalhos de tabela com fundo levemente diferenciado e texto em caixa alta atenuada (text-xs)      │
├────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│  10% — PONTOS DE AÇÃO PRIMÁRIA & STATUS SEMÂNTICO (ACCENT)                                             │
│  • Botão de Ação Primária Único (CTA: #2563EB Cobalt, #6366F1 Indigo ou #0F172A Preto Carbono)          │
│  • Cores de Status Funcional estritamente semânticas:                                                  │
│    - Verde (#10B981 / #059669): Concluído, Ativo, Pagamento Aprovado, Sistema Operacional             │
│    - Amarelo/Âmbar (#F59E0B / #D97706): Pendente, Limite Próximo (80%), Requer Atenção                 │
│    - Vermelho (#EF4444 / #DC2626): Ação Destrutiva, Excluir, Falha de Conexão, Assinatura Vencida     │
│    - Azul/Ciano (#38BDF8 / #0284C7): Em Andamento, Sincronizando, Link Informativo                     │
└────────────────────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

- ⚠️ **Incompatível com**:
  - **Websites Promocionais B2C de Alto Impacto Emocional**: Marcas de moda de luxo, estúdios de cinema, festivais de música ou campanhas de lançamento onde o objetivo é provocar encantamento e imersão sensorial. Aplicar a estrutura de data-table cinza e sidebars rígidas nesses contextos resultaria em uma experiência fria e burocrática.
  - **Portfólios Artísticos e Agências Experimentais**: Onde a identidade visual exige tipografia serifada gigante, layout desconstruído fora do grid e transições WebGL líquidas.
  - **Aplicações Infantis ou Gamificadas**: Interfaces que demandam personagens 3D, elementos inflados, cores saturadas e micro-animações lúdicas contínuas.

- ⚠️ **Armadilhas de Imitação (Anti-Padrões Frequentes)**:
  - *Sobrecarga de Bordas de 1px (Grid Cage)*: Colocar bordas de 1px em absolutamente todos os elementos (em volta de cada texto, cada badge, cada ícone e cada métrica) cria um efeito de "gaiola visual" claustrofóbico. A hierarquia deve ser dada primariamente pelo espaçamento negativo e por tons de fundo sutis, reservando bordas para delimitar módulos lógicos principais.
  - *Proliferação de Botões de Ação Primária*: Colocar múltiplos botões azuis vibrantes na mesma tela disputando a atenção do operador. A regra é: **apenas 1 botão primário por contexto visual**; todas as outras ações devem ser secundárias (outline), terciárias (ghost) ou ícones sutis.
  - *Falsa Acessibilidade em Modo Escuro*: Usar cinzas excessivamente escuros para textos secundários (`#374151` sobre fundo `#090A0F`), tornando descrições e metadados completamente ilegíveis em monitores com calibração imperfeita.
  - *Tabelas Sem Truncamento ou Larguras Fixas*: Linhas que estouram a tela horizontalmente e quebram títulos de colunas de forma desordenada por falta de definição de larguras percentuais (`w-[200px]`, `truncate`).

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo Operacional

A espinha dorsal das telas catalogadas no SaaS Interface baseia-se em um sistema de grid de 8 pontos (8-point grid system), otimizado para layouts de aplicação de alta densidade:

```
┌────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                               SAAS APPLICATION WORKSPACE BLUEPRINT                                     │
├─────────────────┬──────────────────────────────────────────────────────────────────────────────────────┤
│ SIDEBAR (256px) │ TOPBAR / HEADER (64px) — Breadcrumbs, Global Search (Cmd+K), User Menu & Org Switcher│
│                 ├──────────────────────────────────────────────────────────────────────────────────────┤
│ • Org Switcher  │ PAGE HEADER (80px) — Title, Metadata Badges, Primary Actions ("+ Create Entity")    │
│ • Nav Links     ├──────────────────────────────────────────────────────────────────────────────────────┤
│ • Status Quota  │ METRICS / KPI CARDS (Grid 4 colunas: 1fr 1fr 1fr 1fr — h-120px)                     │
│ • Bottom User   ├──────────────────────────────────────────────────────────────────────────────────────┤
│                 │ FILTER & SEARCH TOOLBAR (48px) — Search Input, Faceted Tags, View Switcher (Table/Kanban)│
│                 ├──────────────────────────────────────────────────────────────────────────────────────┤
│                 │ MAIN CONTENT: DATA TABLE / LIST (Flexible Height, Virtualized Rows, 1px Hairlines)  │
│                 ├──────────────────────────────────────────────────────────────────────────────────────┤
│                 │ PAGINATION BAR (52px) — "Showing 1-25 of 1,420 items", Page Controls (Prev/Next)   │
└─────────────────┴──────────────────────────────────────────────────────────────────────────────────────┘
```

- **Sidebar de Navegação**: Largura fixa de `256px` (`w-64`) ou retrátil para `72px` (modo ícone). Estruturada com: seletor de organização (Workspace Switcher) com badge de plano (`Pro`, `Team`), lista vertical de navegação categorizada com ícones SVG de 18px e badges numéricos de pendência, indicador de cota de uso no rodapé da barra e cartão de usuário com avatar e menu de preferências.
- **Top Bar Utilitária**: Altura padrão de `56px` a `64px` (`h-14` / `h-16`), contendo breadcrumbs dinâmicos com navegação de retorno, barra de busca global centralizada com badge de atalho (`⌘K` / `Ctrl+K`), sino de notificações com indicador numérico ativo e alternador de tema claro/escuro.
- **Área Central de Trabalho (Main Stage)**: Grid elástico com margens internas de `24px` a `32px` (`p-6` / `p-8`) e largura máxima configurável (`max-w-7xl` ou `w-full` com scroll horizontal em tabelas ultra-largas).

---

### 4.2 Sistemas de Cores, Superfícies & Texturas

1. **Camadas de Elevação por Tonalidade (Elevation Stacking)**:
   - Em vez de depender de sombras projetadas pesadas, as interfaces do SaaS Interface definem profundidade através do escalonamento de tons de superfície e bordas de 1px:
     - **Camada 0 (Canvas Base)**: `#FFFFFF` (Claro) ou `#090A0F` (Escuro).
     - **Camada 1 (Cards, Tabelas, Painéis)**: `#FFFFFF` com borda `#E2E8F0` (Claro) ou `#12141C` com borda `#1E2330` (Escuro).
     - **Camada 2 (Dropdowns, Popovers, Drawers)**: `#FFFFFF` com sombra `shadow-lg` (Claro) ou `#181B26` com borda `#2B3245` (Escuro).
     - **Camada 3 (Modais de Diálogo & Alertas)**: Centralizados sobre backdrop com desfoque de fundo (`backdrop-blur-sm bg-neutral-900/40`).
2. **Texturas & Sombras de Alta Precisão**:
   - `shadow-sm`: `0 1px 2px 0 rgb(0 0 0 / 0.05)` — usada em botões secundários, inputs e cards de tabela.
   - `shadow-subtle`: `0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1)` — usada em cards KPI destacados.
   - `hairline-border`: `1px solid rgba(226, 232, 240, 0.8)` (Modo Claro) e `1px solid rgba(30, 41, 59, 0.7)` (Modo Escuro).

---

### 4.3 Catálogo Detalhado de 10 Padrões & Componentes Notáveis do SaaS Interface

Abaixo estão desconstruídos os 10 padrões de arquitetura de interface mais representativos do acervo:

#### 1. Data Table com Virtualização, Sticky Header e Linhas Interativas
- **Anatomia**: Cabeçalho de tabela fixo (`position: sticky; top: 0`) com tipografia em `text-xs uppercase font-semibold text-neutral-500`; linhas com altura uniforme de `48px` ou `56px`; primeira coluna com checkbox de seleção; células numéricas alinhadas à direita em fonte monoespaçada; coluna final com menu de ações rápidas (`...` Three Dots).
- **Gatilho de Interação**: Hover sobre a linha altera a cor de fundo sutilmente (`bg-neutral-50/50` ou `bg-neutral-800/40`) e revela o botão de ações rápidas. O clique em qualquer área da linha (exceto no checkbox) abre o Side Panel de detalhes da entidade.
- **Onde Encaixar**: Telas `/pages/lists-tables/`, gerenciamento de clientes, logs de auditoria e listagem de transações.

#### 2. Global Command Palette (`Cmd+K`) com Categorias e Ações
- **Anatomia**: Modal suspenso centralizado (`max-w-2xl`) com input de busca de alta visibilidade, ícone de lupa, botão de fechar (`Esc`), lista categorizada de resultados dividida por seções ("Navegação Rápida", "Ações Recentes", "Clientes", "Configurações") e rodapé informativo com dicas de atalhos (`↑↓ para navegar`, `↵ para selecionar`, `esc para fechar`).
- **Gatilho de Interação**: Pressionamento global de `Cmd+K` (Mac) ou `Ctrl+K` (Windows/Linux) ou clique no input de busca da Top Bar. Fechamento instantâneo via tecla `Escape`.
- **Onde Encaixar**: Presente no topo de todas as telas da aplicação (`/components/search/`).

#### 3. Slide-over Sheet / Side Panel para Inspeção de Entidade
- **Anatomia**: Gaveta lateral de `480px` a `600px` de largura que desliza a partir da borda direita da viewport, equipada com cabeçalho sticky contendo identificador da entidade (`#INV-8921`), badge de status, botão de tela cheia e botão de fechar (`X`), corpo rolável dividido em abas (ex: "Detalhes", "Atividade", "Metadados JSON", "Permissões") e rodapé sticky com ações ("Salvar Alterações", "Reenviar Fatura").
- **Gatilho de Interação**: Clique em qualquer registro da tabela de dados ou atalho `Space` sobre a linha focada.
- **Onde Encaixar**: Telas `/pages/item-details/` e padrão atômico `/components/side-panel/`.

#### 4. Floating Bulk Actions Toolbar com Contador de Seleção
- **Anatomia**: Barra de ferramentas flutuante ancorada na parte inferior central da tela (`bottom-6 left-1/2 -translate-x-1/2`), com fundo escuro de alto contraste (`bg-neutral-900 text-white shadow-2xl rounded-full`), badge com contador de itens selecionados ("14 itens selecionados"), botões de ação em lote com ícones ("Exportar CSV", "Alterar Status", "Atribuir Responsável") e botão de ação destrutiva ("Excluir Registros").
- **Gatilho de Interação**: Animação de subida suave (`translate-y` de 20px para 0) assim que o usuário seleciona 1 ou mais checkboxes na tabela; desaparece imediatamente quando a seleção é zerada.
- **Onde Encaixar**: Telas com grandes volumes de registros (`/components/bulk-actions/`).

#### 5. Faceted Filter Bar com Chips Removíveis e Popovers
- **Anatomia**: Barra horizontal posicionada acima da tabela contendo um botão seletor de filtros com popover multidimensional (Status, Data, Valor, Categoria), seguida por uma sequência de "chips" ou "pills" que representam os filtros ativos (ex: `Status: Ativo ✕`, `Período: Últimos 30 dias ✕`) e um botão de ação rápida "Limpar todos os filtros".
- **Gatilho de Interação**: Seleção no menu popover adiciona o chip com animação de expansão lateral; clique no `✕` do chip remove o critério e dispara nova consulta no dataset.
- **Onde Encaixar**: Telas `/pages/lists-tables/` e `/components/filters/`.

#### 6. Destructive Action Confirmation Modal com Type-to-Confirm
- **Anatomia**: Caixa de diálogo modal centralizada com ícone de alerta vermelho em destaque, título explícito ("Excluir Workspace Definitivamente"), texto explicativo sobre a irreversibilidade do ato, campo de texto obrigando o usuário a digitar exatamente o nome do recurso para autorizar o botão (ex: *Digite "meu-workspace-prod" para confirmar*) e botão vermelho de exclusão inicialmente desabilitado (`opacity-50 cursor-not-allowed`).
- **Gatilho de Interação**: Clique no botão "Excluir" em configurações de conta; o botão só se torna clicável quando a string digitada é idêntica ao nome do recurso.
- **Onde Encaixar**: Telas de `/pages/settings/` e padrão `/components/modal-dialog/`.

#### 7. Onboarding Stepper Checklist com Progresso Gamificado
- **Anatomia**: Card compacto ancorado na lateral ou no topo do dashboard com cabeçalho contendo barra de progresso horizontal (`h-2 bg-neutral-100 rounded-full overflow-hidden`), percentual de conclusão ("60% Concluído - 3 de 5 passos") e lista vertical de tarefas colapsáveis (ex: "1. Conectar banco de dados ✓", "2. Convidar 2 membros ✓", "3. Configurar domínio customizado", "4. Realizar primeira consulta").
- **Gatilho de Interação**: Clique em uma tarefa abre o modal correspondente ou guia o usuário com destaque visual (tour spotlight); ao concluir, a tarefa recebe um check verde animado e a barra se expande com transição fluida.
- **Onde Encaixar**: Telas `/pages/onboarding/` e `/pages/dashboard/` no primeiro login do usuário.

#### 8. Plan & Usage Meter Widget (Progress Bar com Alert Thresholds)
- **Anatomia**: Módulo de cartão em páginas de faturamento exibindo o plano contratado ("Plano Growth"), valor mensal, data da próxima renovação e barras de progresso lineares de consumo por funcionalidade (ex: "Assentos: 8 de 10 utilizados", "Créditos de IA: 82.400 de 100.000 consumidos"). Possui mudança de cor automática: azul/verde de 0% a 79%, âmbar de 80% a 94%, vermelho a partir de 95% acompanhado de badge "Limite Quase Atingido" e botão "Fazer Upgrade de Cota".
- **Gatilho de Interação**: Hover sobre a barra de progresso exibe tooltip com detalhamento do consumo diário; atingir 80% exibe aviso não intrusivo.
- **Onde Encaixar**: Telas `/pages/billing-plan/` e rodapé da barra lateral de navegação.

#### 9. Dual-Panel Settings Layout com Navegação Vertical Sticky
- **Anatomia**: Layout em duas colunas: coluna esquerda estreita (`200px`) com lista vertical de abas de navegação de configurações ("Geral", "Membros & Cargos", "Segurança & 2FA", "Faturamento", "Chaves de API", "Webhooks") e coluna direita larga (`800px max`) com cartões de configuração divididos em blocos lógicos, cada um com título, descrição atenuada, campos de formulário e rodapé com botão "Salvar Alterações".
- **Gatilho de Interação**: Navegação sem reload de página via troca instantânea de abas com preservação de estado dos formulários.
- **Onde Encaixar**: Telas `/pages/settings/` e `/pages/profile-user/`.

#### 10. Zero-Data Empty State com Ilustração Vetorial e Action Launcher
- **Anatomia**: Estado de tela vazia quando uma lista, tabela ou projeto não possui registros cadastrados. Composto por contêiner com borda tracejada (`border-2 border-dashed border-neutral-300`), ícone central estilizado ou ilustração minimalista, título direto ("Nenhum webhook cadastrado"), parágrafo explicativo ("Configure webhooks para receber notificações de eventos da sua aplicação em tempo real") e botão de ação primária destacado ("+ Criar Primeiro Webhook") acompanhado de link para a documentação técnica.
- **Gatilho de Interação**: Renderizado condicionalmente quando `data.length === 0`, evitando sensação de tela travada ou erro técnico.
- **Onde Encaixar**: Telas `/pages/empty-state/` e em todas as tabelas de dados vazias.

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Física de Movimento, Curvas Easing & Parâmetros de Mola

Interfaces internas de software exigem uma física de animação **extremamente rápida, seca e responsiva**. Qualquer atraso perceptível (> 250ms) é interpretado pelo operador como lentidão de sistema ou perda de produtividade.

```typescript
// Configurações de Mola (Spring Physics) e Easing Curado do SaaS Interface
export const saasInterfaceMotion = {
  // 1. Modais de Diálogo e Command Palette (Pop-in com amortecimento crítico)
  dialogSpring: {
    type: "spring",
    stiffness: 450,
    damping: 35,
    mass: 0.8
  },

  // 2. Slide-over Sheets / Side Panels (Entrada lateral ultra-rápida)
  sheetTransition: {
    type: "spring",
    stiffness: 320,
    damping: 32,
    mass: 1.0
  },

  // 3. Floating Bulk Actions Toolbar (Subida suave com amortecimento)
  floatingToolbarSpring: {
    type: "spring",
    stiffness: 380,
    damping: 30,
    mass: 0.9
  },

  // 4. Dropdowns, Menus e Tooltips (Transição CSS Instantânea)
  dropdownTiming: {
    duration: 0.15,
    ease: [0.16, 1, 0.3, 1] // Out-Expo acelerado
  },

  // 5. Expansão de Accordions e Linhas de Tabela
  collapseTransition: {
    duration: 0.2,
    ease: [0.25, 1, 0.5, 1]
  }
};
```

---

### 5.2 Tokens CSS & Layout Recipe

Abaixo está o sistema de tokens CSS variáveis que define o ecossistema estético do SaaS Interface:

```css
/* ==========================================================================
   SAAS INTERFACE DESIGN TOKENS (CSS VARIABLES)
   Compatível com Modo Claro e Modo Escuro via data-theme ou classe .dark
   ========================================================================== */

:root {
  /* Camada 0: Canvas Base & Superfície Neutra (60%) */
  --si-canvas-bg: #FFFFFF;
  --si-surface-subtle: #F8FAFC;
  --si-surface-panel: #FFFFFF;
  --si-surface-hover: #F1F5F9;
  --si-surface-active: #E2E8F0;

  /* Camada 1: Linhas Estruturais, Divisórias & Bordas (30%) */
  --si-border-hairline: #E2E8F0;
  --si-border-strong: #CBD5E1;
  --si-border-focus: #2563EB;

  /* Camada 2: Tipografia & Hierarquia de Tinta */
  --si-text-primary: #0F172A;     /* Slate 900 */
  --si-text-secondary: #475569;   /* Slate 600 */
  --si-text-muted: #94A3B8;       /* Slate 400 */
  --si-text-inverse: #FFFFFF;

  /* Camada 3: Cores de Ação & Status Semântico (10%) */
  --si-accent-primary: #2563EB;   /* Cobalt Blue */
  --si-accent-primary-hover: #1D4ED8;
  --si-accent-primary-subtle: #EFF6FF;

  --si-status-success: #10B981;
  --si-status-success-bg: #ECFDF5;
  --si-status-warning: #F59E0B;
  --si-status-warning-bg: #FFFBEB;
  --si-status-error: #EF4444;
  --si-status-error-bg: #FEF2F2;
  --si-status-info: #0EA5E9;
  --si-status-info-bg: #F0F9FF;

  /* Sombras de Engenharia */
  --si-shadow-xs: 0 1px 2px 0 rgba(15, 23, 42, 0.05);
  --si-shadow-sm: 0 1px 3px 0 rgba(15, 23, 42, 0.08), 0 1px 2px -1px rgba(15, 23, 42, 0.08);
  --si-shadow-md: 0 4px 6px -1px rgba(15, 23, 42, 0.08), 0 2px 4px -2px rgba(15, 23, 42, 0.08);
  --si-shadow-popover: 0 10px 15px -3px rgba(15, 23, 42, 0.1), 0 4px 6px -4px rgba(15, 23, 42, 0.05);

  /* Raios de Arredondamento */
  --si-radius-sm: 4px;
  --si-radius-md: 6px;
  --si-radius-lg: 8px;
  --si-radius-full: 9999px;
}

/* Modo Escuro (Obsidian Enterprise) */
.dark, [data-theme="dark"] {
  --si-canvas-bg: #090A0F;
  --si-surface-subtle: #0F1117;
  --si-surface-panel: #141721;
  --si-surface-hover: #1E2333;
  --si-surface-active: #283046;

  --si-border-hairline: #1E2333;
  --si-border-strong: #2D374D;
  --si-border-focus: #38BDF8;

  --si-text-primary: #F8FAFC;
  --si-text-secondary: #94A3B8;
  --si-text-muted: #64748B;
  --si-text-inverse: #090A0F;

  --si-accent-primary: #38BDF8;
  --si-accent-primary-hover: #0284C7;
  --si-accent-primary-subtle: rgba(56, 189, 248, 0.1);

  --si-status-success: #34D399;
  --si-status-success-bg: rgba(52, 211, 153, 0.12);
  --si-status-warning: #FBBF24;
  --si-status-warning-bg: rgba(251, 191, 36, 0.12);
  --si-status-error: #F87171;
  --si-status-error-bg: rgba(248, 113, 113, 0.12);
  --si-status-info: #38BDF8;
  --si-status-info-bg: rgba(56, 189, 248, 0.12);

  --si-shadow-xs: 0 1px 2px 0 rgba(0, 0, 0, 0.3);
  --si-shadow-sm: 0 1px 3px 0 rgba(0, 0, 0, 0.4);
  --si-shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.5);
  --si-shadow-popover: 0 10px 25px -3px rgba(0, 0, 0, 0.7);
}
```

---

### 5.3 Receita de Código Funcional em React, Tailwind & Framer Motion

Abaixo está uma implementação completa e pronta para produção que materializa a tríade essencial do **SaaS Interface**:
1. **Data Table com seleção de linhas e hover state**
2. **Floating Bulk Actions Toolbar com animação de entrada por mola**
3. **Slide-over Side Panel (Drawer) para inspeção de entidade sem trocar de página**

```tsx
import React, { useState } from "react";
import { motion, AnimatePresence } from "framer-motion";
import { 
  Search, 
  Filter, 
  MoreVertical, 
  X, 
  Trash2, 
  Download, 
  CheckCircle2, 
  Clock, 
  AlertCircle,
  ExternalLink,
  ChevronRight,
  ShieldCheck,
  CreditCard
} from "lucide-react";

// Definição dos tipos do modelo de dados
interface CustomerEntity {
  id: string;
  name: string;
  email: string;
  plan: "Enterprise" | "Pro" | "Starter";
  status: "Active" | "Pending" | "Suspended";
  mrr: number;
  seats: string;
  createdDate: string;
}

const mockCustomers: CustomerEntity[] = [
  {
    id: "CUST-1049",
    name: "Acme Cloud Technologies",
    email: "billing@acmecloud.io",
    plan: "Enterprise",
    status: "Active",
    mrr: 2450,
    seats: "48/50",
    createdDate: "14 Out 2026"
  },
  {
    id: "CUST-1050",
    name: "Linear Labs Studio",
    email: "ops@linearlabs.dev",
    plan: "Pro",
    status: "Active",
    mrr: 790,
    seats: "14/20",
    createdDate: "19 Out 2026"
  },
  {
    id: "CUST-1051",
    name: "Nexus Artificial Intelligence",
    email: "finance@nexusai.co",
    plan: "Enterprise",
    status: "Pending",
    mrr: 3100,
    seats: "92/100",
    createdDate: "21 Out 2026"
  },
  {
    id: "CUST-1052",
    name: "Vortex Data Pipelines",
    email: "admin@vortexdata.net",
    plan: "Starter",
    status: "Suspended",
    mrr: 120,
    seats: "2/5",
    createdDate: "23 Out 2026"
  }
];

export default function SaaSInterfaceWorkbench() {
  const [selectedIds, setSelectedIds] = useState<string[]>([]);
  const [inspectingEntity, setInspectingEntity] = useState<CustomerEntity | null>(null);
  const [searchTerm, setSearchTerm] = useState("");

  const toggleSelectAll = () => {
    if (selectedIds.length === mockCustomers.length) {
      setSelectedIds([]);
    } else {
      setSelectedIds(mockCustomers.map((c) => c.id));
    }
  };

  const toggleSelectOne = (id: string, e: React.MouseEvent) => {
    e.stopPropagation();
    setSelectedIds((prev) =>
      prev.includes(id) ? prev.filter((item) => item !== id) : [...prev, id]
    );
  };

  const filteredCustomers = mockCustomers.filter(
    (c) =>
      c.name.toLowerCase().includes(searchTerm.toLowerCase()) ||
      c.id.toLowerCase().includes(searchTerm.toLowerCase()) ||
      c.email.toLowerCase().includes(searchTerm.toLowerCase())
  );

  return (
    <div className="relative min-h-screen bg-slate-50 text-slate-900 font-sans p-6 md:p-10">
      <div className="max-w-6xl mx-auto space-y-6">
        {/* Breadcrumb & Page Header */}
        <div className="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-4">
          <div>
            <div className="flex items-center gap-2 text-xs text-slate-500 font-medium mb-1">
              <span>Workspace</span>
              <span>/</span>
              <span>Clientes & Contas</span>
              <span>/</span>
              <span className="text-slate-900 font-semibold">Base de Clientes</span>
            </div>
            <h1 className="text-2xl font-bold tracking-tight text-slate-900">
              Contratos & Subscrições Ativas
            </h1>
          </div>

          <div className="flex items-center gap-3">
            <button className="px-3.5 py-2 text-sm font-medium text-slate-700 bg-white border border-slate-200 rounded-md shadow-xs hover:bg-slate-50 transition-colors">
              Exportar Relatório
            </button>
            <button className="px-4 py-2 text-sm font-medium text-white bg-blue-600 rounded-md shadow-xs hover:bg-blue-700 transition-colors flex items-center gap-1.5">
              <span>+ Novo Cliente</span>
            </button>
          </div>
        </div>

        {/* Toolbar de Filtro e Busca */}
        <div className="flex flex-col sm:flex-row items-center justify-between gap-4 bg-white p-3.5 border border-slate-200 rounded-lg shadow-xs">
          <div className="relative w-full sm:w-80">
            <Search className="absolute left-3 top-1/2 -translate-y-1/2 w-4 h-4 text-slate-400" />
            <input
              type="text"
              value={searchTerm}
              onChange={(e) => setSearchTerm(e.target.value)}
              placeholder="Buscar por ID, empresa ou email..."
              className="w-full pl-9 pr-4 py-1.5 text-sm bg-slate-50 border border-slate-200 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-600/20 focus:border-blue-600 transition-all placeholder:text-slate-400"
            />
          </div>

          <div className="flex items-center gap-2 w-full sm:w-auto justify-end">
            <button className="px-3 py-1.5 text-sm font-medium text-slate-600 bg-slate-50 border border-slate-200 rounded-md hover:bg-slate-100 transition-colors flex items-center gap-2">
              <Filter className="w-3.5 h-3.5 text-slate-500" />
              <span>Filtros Avançados</span>
            </button>
            <span className="text-xs text-slate-400 font-mono">
              {filteredCustomers.length} registros
            </span>
          </div>
        </div>

        {/* Tabela de Dados (Data Grid) */}
        <div className="bg-white border border-slate-200 rounded-lg shadow-xs overflow-hidden">
          <div className="overflow-x-auto">
            <table className="w-full text-left border-collapse">
              <thead>
                <tr className="border-b border-slate-200 bg-slate-50/75 text-[11px] font-semibold uppercase tracking-wider text-slate-500">
                  <th className="py-3 px-4 w-12 text-center">
                    <input
                      type="checkbox"
                      checked={
                        selectedIds.length === mockCustomers.length &&
                        mockCustomers.length > 0
                      }
                      onChange={toggleSelectAll}
                      className="rounded border-slate-300 text-blue-600 focus:ring-blue-500 w-4 h-4 cursor-pointer"
                    />
                  </th>
                  <th className="py-3 px-4">Identificador</th>
                  <th className="py-3 px-4">Empresa / Email</th>
                  <th className="py-3 px-4">Plano</th>
                  <th className="py-3 px-4">Status</th>
                  <th className="py-3 px-4 text-right">MRR Mensal</th>
                  <th className="py-3 px-4">Assentos</th>
                  <th className="py-3 px-4 text-right">Ação</th>
                </tr>
              </thead>
              <tbody className="divide-y divide-slate-100 text-sm">
                {filteredCustomers.map((cust) => {
                  const isSelected = selectedIds.includes(cust.id);
                  return (
                    <tr
                      key={cust.id}
                      onClick={() => setInspectingEntity(cust)}
                      className={`group hover:bg-slate-50/80 cursor-pointer transition-colors ${
                        isSelected ? "bg-blue-50/40" : ""
                      }`}
                    >
                      <td
                        className="py-3 px-4 text-center"
                        onClick={(e) => toggleSelectOne(cust.id, e)}
                      >
                        <input
                          type="checkbox"
                          checked={isSelected}
                          onChange={() => {}}
                          className="rounded border-slate-300 text-blue-600 focus:ring-blue-500 w-4 h-4 cursor-pointer"
                        />
                      </td>

                      <td className="py-3 px-4 font-mono text-xs font-medium text-slate-500">
                        {cust.id}
                      </td>

                      <td className="py-3 px-4">
                        <div className="font-semibold text-slate-900 group-hover:text-blue-600 transition-colors">
                          {cust.name}
                        </div>
                        <div className="text-xs text-slate-500 font-mono">
                          {cust.email}
                        </div>
                      </td>

                      <td className="py-3 px-4">
                        <span
                          className={`inline-flex items-center px-2 py-0.5 rounded text-xs font-medium ${
                            cust.plan === "Enterprise"
                              ? "bg-purple-50 text-purple-700 border border-purple-200"
                              : cust.plan === "Pro"
                              ? "bg-blue-50 text-blue-700 border border-blue-200"
                              : "bg-slate-100 text-slate-700 border border-slate-200"
                          }`}
                        >
                          {cust.plan}
                        </span>
                      </td>

                      <td className="py-3 px-4">
                        {cust.status === "Active" && (
                          <span className="inline-flex items-center gap-1.5 text-xs font-medium text-emerald-700">
                            <CheckCircle2 className="w-3.5 h-3.5 text-emerald-500" />
                            Ativo
                          </span>
                        )}
                        {cust.status === "Pending" && (
                          <span className="inline-flex items-center gap-1.5 text-xs font-medium text-amber-700">
                            <Clock className="w-3.5 h-3.5 text-amber-500" />
                            Pendente
                          </span>
                        )}
                        {cust.status === "Suspended" && (
                          <span className="inline-flex items-center gap-1.5 text-xs font-medium text-rose-700">
                            <AlertCircle className="w-3.5 h-3.5 text-rose-500" />
                            Suspenso
                          </span>
                        )}
                      </td>

                      <td className="py-3 px-4 text-right font-mono font-medium text-slate-900">
                        ${cust.mrr.toLocaleString("en-US")}/mês
                      </td>

                      <td className="py-3 px-4 text-xs font-mono text-slate-500">
                        {cust.seats}
                      </td>

                      <td className="py-3 px-4 text-right">
                        <div className="flex items-center justify-end gap-1">
                          <button
                            onClick={(e) => {
                              e.stopPropagation();
                              setInspectingEntity(cust);
                            }}
                            className="p-1 text-slate-400 hover:text-slate-600 rounded transition-colors"
                          >
                            <ChevronRight className="w-4 h-4" />
                          </button>
                        </div>
                      </td>
                    </tr>
                  );
                })}
              </tbody>
            </table>
          </div>

          {/* Rodapé de Paginação */}
          <div className="py-3 px-4 border-t border-slate-200 bg-slate-50/50 flex items-center justify-between text-xs text-slate-500">
            <div>Exibindo 1 a 4 de 4 clientes encontrados</div>
            <div className="flex items-center gap-2">
              <button
                disabled
                className="px-2.5 py-1 bg-white border border-slate-200 rounded text-slate-400 cursor-not-allowed"
              >
                Anterior
              </button>
              <button
                disabled
                className="px-2.5 py-1 bg-white border border-slate-200 rounded text-slate-400 cursor-not-allowed"
              >
                Próxima
              </button>
            </div>
          </div>
        </div>
      </div>

      {/* 2. Floating Bulk Actions Toolbar (Acionada quando há seleção múltipla) */}
      <AnimatePresence>
        {selectedIds.length > 0 && (
          <motion.div
            initial={{ opacity: 0, y: 30, scale: 0.95 }}
            animate={{ opacity: 1, y: 0, scale: 1 }}
            exit={{ opacity: 0, y: 20, scale: 0.95 }}
            transition={{ type: "spring", stiffness: 400, damping: 30 }}
            className="fixed bottom-8 left-1/2 -translate-x-1/2 z-40 bg-slate-900 text-white px-5 py-3 rounded-full shadow-2xl border border-slate-700/80 flex items-center gap-4"
          >
            <div className="flex items-center gap-2 pr-3 border-r border-slate-700 text-xs font-medium">
              <span className="w-5 h-5 rounded-full bg-blue-600 text-white flex items-center justify-center text-[11px] font-bold">
                {selectedIds.length}
              </span>
              <span>selecionados</span>
            </div>

            <div className="flex items-center gap-2">
              <button className="px-3 py-1.5 text-xs font-medium bg-slate-800 hover:bg-slate-700 rounded-full transition-colors flex items-center gap-1.5">
                <Download className="w-3.5 h-3.5" />
                <span>Exportar CSV</span>
              </button>
              <button className="px-3 py-1.5 text-xs font-medium bg-slate-800 hover:bg-slate-700 rounded-full transition-colors flex items-center gap-1.5">
                <ShieldCheck className="w-3.5 h-3.5" />
                <span>Revalidar Acesso</span>
              </button>
              <button className="px-3 py-1.5 text-xs font-medium bg-rose-500/20 text-rose-300 hover:bg-rose-500/30 rounded-full transition-colors flex items-center gap-1.5">
                <Trash2 className="w-3.5 h-3.5 text-rose-400" />
                <span>Excluir</span>
              </button>
            </div>

            <button
              onClick={() => setSelectedIds([])}
              className="text-slate-400 hover:text-white p-1 rounded-full transition-colors"
            >
              <X className="w-4 h-4" />
            </button>
          </motion.div>
        )}
      </AnimatePresence>

      {/* 3. Slide-over Sheet / Side Panel para Inspeção Detalhada da Entidade */}
      <AnimatePresence>
        {inspectingEntity && (
          <>
            {/* Backdrop suave */}
            <motion.div
              initial={{ opacity: 0 }}
              animate={{ opacity: 1 }}
              exit={{ opacity: 0 }}
              onClick={() => setInspectingEntity(null)}
              className="fixed inset-0 bg-slate-900/30 backdrop-blur-xs z-50"
            />

            {/* Painel lateral direito */}
            <motion.aside
              initial={{ x: "100%" }}
              animate={{ x: 0 }}
              exit={{ x: "100%" }}
              transition={{ type: "spring", stiffness: 350, damping: 32 }}
              className="fixed top-0 right-0 bottom-0 w-full max-w-lg bg-white border-l border-slate-200 shadow-2xl z-50 flex flex-col"
            >
              {/* Header do Side Panel */}
              <div className="p-5 border-b border-slate-200 flex items-center justify-between">
                <div>
                  <div className="flex items-center gap-2">
                    <span className="font-mono text-xs text-slate-400">
                      {inspectingEntity.id}
                    </span>
                    <span className="inline-flex px-1.5 py-0.5 text-[10px] font-bold rounded bg-emerald-50 text-emerald-700 border border-emerald-200">
                      {inspectingEntity.status}
                    </span>
                  </div>
                  <h2 className="text-lg font-bold text-slate-900 mt-1">
                    {inspectingEntity.name}
                  </h2>
                </div>

                <div className="flex items-center gap-2">
                  <button className="p-1.5 text-slate-400 hover:text-slate-600 rounded-md hover:bg-slate-100 transition-colors">
                    <ExternalLink className="w-4 h-4" />
                  </button>
                  <button
                    onClick={() => setInspectingEntity(null)}
                    className="p-1.5 text-slate-400 hover:text-slate-600 rounded-md hover:bg-slate-100 transition-colors"
                  >
                    <X className="w-4 h-4" />
                  </button>
                </div>
              </div>

              {/* Corpo de Navegação e Informações */}
              <div className="flex-1 overflow-y-auto p-6 space-y-6">
                {/* Métricas Principais */}
                <div className="grid grid-cols-2 gap-4">
                  <div className="p-4 bg-slate-50 border border-slate-200 rounded-lg">
                    <div className="text-xs text-slate-500 mb-1">Faturamento Mensal</div>
                    <div className="text-xl font-bold font-mono text-slate-900">
                      ${inspectingEntity.mrr.toLocaleString("en-US")}
                    </div>
                  </div>
                  <div className="p-4 bg-slate-50 border border-slate-200 rounded-lg">
                    <div className="text-xs text-slate-500 mb-1">Assentos Ativos</div>
                    <div className="text-xl font-bold font-mono text-slate-900">
                      {inspectingEntity.seats}
                    </div>
                  </div>
                </div>

                {/* Bloco de Faturamento & Cartão */}
                <div className="border border-slate-200 rounded-lg p-4 space-y-3">
                  <div className="flex items-center justify-between">
                    <span className="text-xs font-semibold uppercase text-slate-400">
                      Método de Cobrança
                    </span>
                    <span className="text-xs text-blue-600 font-medium cursor-pointer hover:underline">
                      Alterar Cartão
                    </span>
                  </div>
                  <div className="flex items-center gap-3">
                    <div className="w-10 h-7 bg-slate-900 text-white rounded flex items-center justify-center">
                      <CreditCard className="w-4 h-4" />
                    </div>
                    <div>
                      <div className="text-sm font-semibold text-slate-900">
                        Mastercard terminando em 4821
                      </div>
                      <div className="text-xs text-slate-500">Expira em 08/2029</div>
                    </div>
                  </div>
                </div>

                {/* Histórico Recente de Auditoria */}
                <div className="space-y-3">
                  <span className="text-xs font-semibold uppercase text-slate-400">
                    Registro de Auditoria (Audit Log)
                  </span>
                  <div className="space-y-2 text-xs">
                    <div className="p-3 bg-slate-50 rounded border border-slate-100 flex justify-between">
                      <span className="text-slate-700">Upgrade de plano para Enterprise</span>
                      <span className="text-slate-400 font-mono">14 Out 16:32</span>
                    </div>
                    <div className="p-3 bg-slate-50 rounded border border-slate-100 flex justify-between">
                      <span className="text-slate-700">Convite aceito por 3 novos assentos</span>
                      <span className="text-slate-400 font-mono">18 Out 09:14</span>
                    </div>
                  </div>
                </div>
              </div>

              {/* Rodapé de Ação do Painel Lateral */}
              <div className="p-4 border-t border-slate-200 bg-slate-50/50 flex items-center justify-between">
                <button className="px-3.5 py-2 text-xs font-semibold text-rose-600 hover:bg-rose-50 border border-rose-200 rounded-md transition-colors">
                  Suspender Acesso
                </button>
                <div className="flex items-center gap-2">
                  <button
                    onClick={() => setInspectingEntity(null)}
                    className="px-3 py-2 text-xs font-medium text-slate-600 hover:bg-slate-200 rounded-md transition-colors"
                  >
                    Fechar
                  </button>
                  <button className="px-4 py-2 text-xs font-medium text-white bg-blue-600 hover:bg-blue-700 rounded-md shadow-xs transition-colors">
                    Salvar Alterações
                  </button>
                </div>
              </div>
            </motion.aside>
          </>
        )}
      </AnimatePresence>
    </div>
  );
}
```

---

### 5.4 Como o Agente de IA Deve Pesquisar ao Vivo no SaaS Interface

Quando o arquiteto ou desenvolvedor estiver construindo uma funcionalidade específica de produto e precisar de referências visuais em tempo real, o agente de IA deve consultar diretamente os pontos de extremidade canônicos do `saasinterface.com`:

```
┌────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                              TAXONOMIA DE URLS DIRETAS PARA CONSULTA AO VIVO                           │
├────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│  ARQUÉTIPOS DE PÁGINAS DE APLICAÇÃO (`/pages/<slug>/`):                                                │
│  • Dashboards Analíticos:              https://saasinterface.com/pages/dashboard/                      │
│  • Tabelas de Dados & Listagens:       https://saasinterface.com/pages/lists-tables/                   │
│  • Configurações de Workspace:         https://saasinterface.com/pages/settings/                       │
│  • Faturamento, Planos & Assentos:     https://saasinterface.com/pages/billing-plan/                   │
│  • Fluxos de Checkout Interno:         https://saasinterface.com/pages/checkout/                       │
│  • Matrizes de Preço In-App:           https://saasinterface.com/pages/pricing/                        │
│  • Quadros Kanban & Workflows:         https://saasinterface.com/pages/boards/                         │
│  • Calendários & Agendamentos:         https://saasinterface.com/pages/calendar/                       │
│  • Editores Visuais & Canvas:          https://saasinterface.com/pages/builder-editor/                 │
│  • Mensageria, Notificações & Chat:    https://saasinterface.com/pages/messaging-chat/                 │
│  • Diretório de Membros & Equipe:      https://saasinterface.com/pages/directory/                      │
│  • Fluxos de Onboarding & Setup:       https://saasinterface.com/pages/onboarding/                     │
│  • Estados Vazios (Empty States):      https://saasinterface.com/pages/empty-state/                    │
│  • Biblioteca de Mídias & Arquivos:    https://saasinterface.com/pages/library/                        │
│  • Detalhes Profundos de Entidade:     https://saasinterface.com/pages/item-details/                   │
│  • Formulários Complexos:              https://saasinterface.com/pages/forms/                          │
│  • Feeds de Atividade & Auditoria:     https://saasinterface.com/pages/activity-feed/                  │
│  • Autenticação (Sign Up / Sign In):   https://saasinterface.com/pages/sign-up/ & /sign-in/            │
│  • Perfil de Usuário & 2FA:            https://saasinterface.com/pages/profile-user/                   │
│  • Changelogs & Atualizações:          https://saasinterface.com/pages/changelog-updates/              │
├────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│  FAMÍLIAS DE COMPONENTES ATÔMICOS (`/components/<slug>/`):                                             │
│  • Modais de Diálogo & Confirmação:    https://saasinterface.com/components/modal-dialog/              │
│  • Menus de Contexto & Pickers:        https://saasinterface.com/components/menu-picker/               │
│  • Paletas de Busca Global (Cmd+K):    https://saasinterface.com/components/search/                    │
│  • Gavetas Laterais (Side Panels):     https://saasinterface.com/components/side-panel/                │
│  • Filtros Facetados & Multi-select:   https://saasinterface.com/components/filters/                   │
│  • Barras Flutuantes de Ações em Lote: https://saasinterface.com/components/bulk-actions/              │
└────────────────────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir a seção de Arquitetura de Interface e Design System de um produto no arquivo `DESIGN_BLUEPRINT.md`, as seguintes regras estritas derivadas da análise do **SaaS Interface** devem ser incorporadas:

1. **Separação de Camadas Pré-Login vs. Pós-Login**:
   - As páginas públicas de marketing (Landing Pages, Preços Públicos) devem seguir a estética comercial de conversão do **Saaspo / SaaS Landing Page** (#106 / #109).
   - Assim que o usuário entra no sistema (`/app/*` ou `/dashboard/*`), a direção de arte deve migrar imediatamente para os padrões de alta densidade e ergonomia utilitária do **SaaS Interface** (#111).
2. **Adoção de Primitivos Acessíveis (Radix UI / TanStack)**:
   - Toda tabela deve ser implementada com `@tanstack/react-table` com suporte a virtualização via `@tanstack/react-virtual`.
   - Modais, Drawers, Dropdowns e Tooltips devem derivar de primitivos desacoplados WAI-ARIA (`@radix-ui/react-dialog`, `@radix-ui/react-popover`, `@radix-ui/react-dropdown-menu`).
3. **Persistência de Contexto via Side Panels**:
   - Evitar navegar para uma rota de página inteira quando o usuário quiser inspecionar um item de tabela ou editar uma configuração rápida. Utilizar o padrão de **Slide-over Sheet (Side Panel)** de 480px com fechamento via tecla `Escape`.
4. **Disciplina de Ações Destrutivas (Type-to-Confirm)**:
   - Nenhuma entidade crítica (Workspaces, Bancos de Dados, Chaves de Produção, Exclusão de Membros) pode ser excluída com um simples clique em "OK". Exigir digitação exata do identificador do item em um diálogo modal dedicado.
5. **Comunicação Proativa de Cotas de Assinatura**:
   - Incorporar barras de progresso lineares de consumo em locais contextuais com transição semântica de cores (Azul ➔ Âmbar ➔ Vermelho), permitindo upgrade sem atrito operacional antes do bloqueio das APIs.
