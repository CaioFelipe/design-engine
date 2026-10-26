---
id: "113-refero-design"
name: "Refero Design"
url: "https://refero.design/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico:
  - "Production-Grade Real Software UI/UX Intelligence"
  - "Multi-Screen End-to-End User Journeys (Flows over Static Shots)"
  - "Atomic Component Granularity (Micro-Elements, Dialogs, Data Grids & Toolbars)"
  - "Dual-Platform Separation (Web Applications ⟷ Native iOS Apps)"
  - "AI-Native Design Ingestion (Refero MCP & DESIGN.md Token Extraction)"
  - "High-Density Structured Taxonomy (Page Types, UI Patterns, Element Atoms & Brand Catalogs)"
  - "Surgical Functional Minimalism (Dark Theme #13151A & Light Canvas #FFFFFF with 1px Sharp Precision)"
densidade_informacao: "Alta/Utilitaria & Multi-Nível (In-App Screens, Micro-Components & End-to-End User Flows)"
impacto_visual: "Editorial/Sofisticado & High-Fidelity Product Engineering"
custo_computacional: "Baixo a Moderado (Interface SPA com SSR híbrido, virtualização de grid de imagens otimizadas em WebP/AVIF servidas via CDN edge global, zero sobrecarga de WebGL desnecessário, foco em renderização nativa CSS Grid/Flexbox acelerada por hardware)"
stack_frameworks:
  - "React 19 / Next.js 14/15"
  - "TypeScript 5.x"
  - "Tailwind CSS v3/v4 (arbitrary variants, container queries, specular 1px borders)"
  - "Framer Motion / Motion.dev (layout springs, drawer transitions, smooth view transitions)"
  - "Radix UI / Shadcn UI Primitives (Dialogs, Dropdowns, Tooltips, Tabs, Accordions, Sheet Drawers)"
  - "Model Context Protocol (Refero MCP em https://api.refero.design/mcp para Claude Code, Cursor, Windsurf)"
  - "Lucide React / Phosphor Icons"
compatibilidade:
  fontes_ideais:
    - "Neo-Grotesques Técnicas de Alta Legibilidade de Interface: Inter, Geist Sans, Plus Jakarta Sans, SF Pro Display / Text, Satoshi, General Sans"
    - "Display Sans Utilitárias para Títulos e Propostas de Valor: Cabinet Grotesk, PP Neue Montreal, Cal Sans, Switzer"
    - "Monoespaçadas Corporativas para Métricas, IDs, Código e Tokens: Geist Mono, JetBrains Mono, SF Mono, Fira Code"
  paletas_ideais:
    - "Refero Dark Architecture (Canvas Principal Escuro): #13151A (Fundo Obsidian Canvas), #1C1F26 (Superfície Elevada de Cards e Painéis), #272B35 (Bordas Estruturais 1px), #3B82F6 / #6366F1 (Acento de Foco Azul Índigo), #94A3B8 (Texto Secundário Slate), #F8FAFC (Tipografia Primária Alabastro)"
    - "Refero Clean Light (Canvas Alternativo Claro): #FFFFFF (Fundo Canvas Puro), #F8FAFC (Superfície Neutra Secundária Slate 50), #E2E8F0 (Bordas de Separação 1px), #0F172A (Texto Primário Slate 900), #64748B (Legendas e Metadados), #2563EB (Acento Royal Blue)"
    - "Regra 60-30-10 de Referência de Produto: 60% Superfície Neutra de Fundo (Obsidian #13151A ou Branco #FFFFFF), 30% Estrutura de Contêineres, Grids, Linhas Divisórias e Tipografia Escaneável, 10% Acentos Semânticos de Ação, Badges de Categoria e Estados Interativos"
  combinacoes_recomendadas:
    - "Drawer lateral de inspeção de tela/fluxo com metadados de produto, data de captura, versão e links de tela anterior/próxima"
    - "Barra de filtros facetados multicamada com seleção combinada de Plataforma (Web/iOS), Tipo de Página, Elemento de UI e Marca"
    - "Modais de visualização expandida em alta resolução com ferramenta de zoom, anotação visual e cópia direta de CSS tokens"
    - "Cards de visualização de fluxo sequencial com navegação horizontal por etapas numeradas ('Etapa 1 de 5: Cadastro', 'Etapa 2: Seleção de Plano')"
    - "Paleta de busca universal (CMD+K) com pesquisa por texto semântico, busca reversa de imagem e navegação por atalhos de teclado"
    - "Integração nativa de DESIGN.md para exportação direta de tokens tipográficos, de cor e raio para editores com IA"
  conflitos_esteticos:
    - "Telas conceituais 'Dribbblescas' não funcionais sem estados de erro, loading ou empty states"
    - "Gradientes neon saturados e neomorfismos pastosos que obscurecem a usabilidade de ferramentas de trabalho reais"
    - "Ignorar a separação contextual entre UI web desktop e UI mobile nativa iOS (tratar touch como click)"
    - "Scroll-jacking e transições lentas que impedem o fluxo de navegação ágil e escaneamento do catálogo"
    - "Apresentar telas soltas sem o contexto do fluxo do usuário (ex: exibir tela de sucesso sem mostrar o passo de confirmação prévio)"
---

# Refero Design — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
██████╗ ███████╗███████╗███████╗██████╗  ██████╗ 
██╔══██╗██╔════╝██╔════╝██╔════╝██╔══██╗██╔═══██╗
██████╔╝█████╗  █████╗  █████╗  ██████╔╝██║   ██║
██╔══██╗██╔══╝  ██╔══╝  ██╔══╝  ██╔══██╗██║   ██║
██║  ██║███████╗██║     ███████╗██║  ██║╚██████╔╝
╚═╝  ╚═╝╚══════╝╚═╝     ╚══════╝╚═╝  ╚═╝ ╚═════╝ 
```

---

## 1. DNA Estético & Filosofia de Curadoria

O **Refero Design** (`https://refero.design/`), desenvolvido pela **Refero Inc.** e lançado originalmente no início de 2023, estabeleceu-se como a maior e mais sofisticada biblioteca de inteligência visual de UI/UX do mundo para **produtos digitais reais**, compreendendo dezenas de milhares de telas em produção contínua provenientes de mais de mil aplicações web e iOS de referência global (como Linear, Notion, Supabase, Stripe, Airbnb, Figma, Raycast, Vercel e Arc).

A criação do Refero representou uma ruptura paradigmática contra a chamada **"Dribbblisation" do Design**: o fenômeno em que designers conceituavam interfaces estáticas visualmente cintilantes — repletas de sombras coloridas irreais, ausência de dados densos, sem estados vazios (*empty states*), sem limites de caracteres ou tratamento de erros —, mas absolutamente impraticáveis para implementação por times de engenharia em software de produção.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        A RUPTURA FILOSÓFICA DO REFERO DESIGN                           │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  ❌ DRIBBBLISATION CONCEITUAL           │  ✅ INTELIGÊNCIA REAL DE PRODUTO (REFERO)     │
│  • Telas isoladas sem contexto          │  • Jornadas e fluxos completos ponta a ponta │
│  • Textos perfeitos simulados           │  • Dados de produção, truncamento e edge cases│
│  • Sombras difusas irreais (>40px blur) │  • Bordas de 1px nítidas e contraste WCAG AA  │
│  • Visual puramente contemplativo       │  • Resolução de fricção de usabilidade (UX)   │
│  • Incompatível com engenharia real     │  • Extração direta de DESIGN.md e via MCP AI  │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 A Tríade Estrutural: Telas, Elementos e Fluxos

Ao contrário de galerias de landing pages puras que analisam apenas a vitrine externa da aplicação, o Refero desce aos níveis mais profundos do software funcional através de uma estrutura tripartida:

1. **Screens (Telas de Aplicação)**:
   - Capturas integrais em resolução nativa de telas de dashboards analíticos, painéis de faturamento (*billing*), páginas de detalhes de produto, configurações de conta, modais de permissões e estados de erro.
2. **Elements (Átomos de UI Desconstruídos)**:
   - Catálogo granular focado em componentes isolados em seu habitat natural: botões de ação principal/secundária, tabelas de dados (*data tables*) com paginação e ordenação, barras de busca universais (`CMD+K`), seletores de cor, *steppers* de progresso, *empty states* e gavetas (*sheets*).
3. **Flows (Jornadas do Usuário Sequenciadas)**:
   - O grande diferencial técnico da plataforma: sequências lineares de telas que documentam exatamente como um produto conduz o usuário por processos complexos (ex: Onboarding inicial de 5 etapas, migração de plano com paywall contextual, fluxo de checkout, convite de membros de equipe com RBAC e cancelamento de assinatura).

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        THE REFERO TAXONOMY ENGINE                                      │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  [ PLATFORM SELECTOR ] ──► [ WEB APPLICATIONS ] vs. [ NATIVE iOS APPS ]               │
│                                                                                        │
│  [ PAGES ]             ──► Dashboards, Settings, Pricing, Paywalls, Auth, 404, Stats   │
│  [ ELEMENTS ]          ──► Modals, Tables, Sidebars, Toolbars, Badges, Tabs, Steppers  │
│  [ FLOWS ]             ──► Onboarding, Sign Up, Upgrade/Paywall, Inviting Team, Billing│
│  [ SEARCH MODES ]      ──► Text Keyword, Faceted Taxonomy, Visual Reverse Image Match  │
│  [ AI CONSUMPTION ]    ──► Refero MCP API Endpoint ⟷ Refero Styles (DESIGN.md)        │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.2 A Revolução para a Era da IA: Refero MCP & Refero Styles (`DESIGN.md`)

O Refero não foi concebido apenas como uma ferramenta para o olho humano, mas sim como a **camada de contexto visual para agentes autônomos de engenharia de software**. 

Através do protocolo **Model Context Protocol (MCP)** via endpoint oficial `https://api.refero.design/mcp` e do ecossistema **Refero Styles** (`styles.refero.design`), o Refero resolve o problema crônico das IAs geradoras de código (como Claude Code, Cursor, Windsurf e v0):
- Modelos de linguagem, quando instruídos a criar uma interface, tendem a gerar componentes genéricos, estéreis e com estilos de biblioteca padrão desatualizados.
- O Refero extrai sistematicamente a arquitetura visual completa dos principais produtos do mercado — convertendo paletas de cores semânticas, escalas de tipografia, raios de curvatura de borda, padding modular e comportamentos de transição — em arquivos estruturados **`DESIGN.md`**.
- Injetando esse arquivo no contexto do agente de IA, a IA passa a codificar interfaces com a exata maturidade, sofisticação e precisão técnica das maiores referências mundiais de software.

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

O Refero Design é a **Referência Primária de Direção de Arte e Engenharia de Produto** quando o objetivo do projeto envolve:

1. **Desenvolvimento de Aplicações Web B2B/Enterprise & Micro-SaaS de Alto Desempenho**:
   - Criação de sistemas operacionais onde a densidade de informação precisa conviver harmoniosamente com a facilidade de escaneamento visual (tabelas com dezenas de colunas, métricas financeiras em tempo real, filtros dinâmicos multifacetados).
2. **Engenharia de Fluxos de Ativação (Product-Led Growth - PLG)**:
   - Estruturação de etapas de onboarding que reduzem o *Time-to-Value* (tempo até o usuário obter valor real do software), checklists interativos e guias de início rápido.
3. **Arquitetura de Paywalls, Precificação e Gestão de Assinaturas**:
   - Desenho de telas de upgrade contextual in-app (intersticiais de limite de uso, modais comparativos de planos, confirmação de cartão com Stripe Elements e feedback de downgrade).
4. **Criação de Design Systems Modulares e Escaláveis**:
   - Levantamento de padrões de consistência para bibliotecas de componentes (como Shadcn UI, Radix Primitives e Tailwind CSS), garantindo que todos os estados de interação (*idle*, *hover*, *focus-visible*, *active*, *disabled*, *loading*) estejam previstos.
5. **Desenvolvimento de Aplicativos Nativos iOS & Multiplataforma**:
   - Consulta específica à aba `/ios-apps` para validar padrões da Apple Human Interface Guidelines (HIG), navegação baseada em *tab bars*, folhas modais destacáveis (*bottom sheets*) e ações contextuais táteis.
6. **Que Emoção e Posicionamento Esse Estilo Comunica**:
   - Comunica **rigor técnico inabalável, alta confiabilidade corporativa, elegância funcional, maturidade de produto e ausência total de amadorismo**. O usuário sente que está diante de uma ferramenta robusta na qual pode confiar operações financeiras ou dados sensíveis.
7. **Papel na Regra 60-30-10**:
   - **60% Superfície Neutra**: Canvas profundo em Dark Obsidian (`#13151A` a `#1C1F26`) ou Light Slate (`#FFFFFF` a `#F8FAFC`), proporcionando repouso visual e sustentação para dados pesados.
   - **30% Estrutura & Tipografia**: Grids modulares, divisores de 1px (`#272B35` / `#E2E8F0`), cartões de superfície elevada e tipografia neo-grotesca perfeitamente hierarquizada.
   - **10% Acentos Semânticos de Ação**: Cores primárias de alto impacto (Azul Índigo `#3B82F6` / `#6366F1`, Esmeralda para sucesso `#10B981` e Âmbar para alertas `#F59E0B`), aplicadas cirurgicamente em botões primários, tags de status e indicadores de progresso.

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

### 3.1 Incompatibilidades Setoriais Críticas
- ⚠️ **Portfólios Artísticos Avant-Garde e Experiências 3D Imersivas WebGL**: O foco do Refero é estritamente na produtividade humana e ergonomia de interfaces de software. Websites de festivais de cinema, galerias de arte brutalista ou estúdios criativos com tipografia desconstruída e física experimental não encontram respaldo nesta galeria utilitária.
- ⚠️ **Marcas de Luxo Haute Couture e Joalheria de Herança**: O luxo tradicional necessita de espaço negativo massivo, tipografia com serifas nobres da escola renascentista/modernista, fotos editoriais em tela cheia e ritmo contemplativo lento. Interfaces densas com tabelas e atalhos de teclado quebram a aura de exclusividade aristocrática.
- ⚠️ **Jogos Eletrônicos Fantásticos e Sites Infantis/Lúdicos**: A linguagem sóbria, vetores limpos e contornos de 1px do Refero geram uma atmosfera corporativa e fria, incompatível com universos lúdicos orgânicos e fantasiosos.

### 3.2 Armadilhas de Imitação (Anti-Padrões de UI/UX)

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        ANTI-PADRÕES DE IMITAÇÃO NO ECOSSISTEMA UI/UX                   │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  ❌ O "Frankenstein de Componentes"    │  ✅ Design Sistêmico Coerente                 │
│     Copiar o botão do Linear, a tabela │     Adotar um único DESIGN.md com escala de   │
│     do Notion e a navbar do Stripe     │     raios (radius), cores e pesos tipográficos│
│     criando uma salada sem identidade. │     unificados em toda a aplicação.           │
├────────────────────────────────────────┼────────────────────────────────────────────────┤
│  ❌ A "Densidade Asfixiante"           │  ✅ Respiração Modular com Espaçamento 8pt    │
│     Apertar tabelas e cards sem margem │     Equilibrar alta densidade com padding     │
│     adequada, tornando a tela ilegível │     consistente e hierarquia de cinzas para   │
│     para usuários que trabalham horas. │     separar grupos lógicos de dados.          │
├────────────────────────────────────────┼────────────────────────────────────────────────┤
│  ❌ O "Empty State Mudo e Punilista"   │  ✅ Empty State com Ação e Mentoria           │
│     Exibir uma tela em branco dizendo  │     Ilustração funcional discreta, descrição  │
│     "Nenhum dado encontrado" sem CTA.  │     do benefício e botão primário com atalho. │
├────────────────────────────────────────┼────────────────────────────────────────────────┤
│  ❌ A "Desconexão Web x iOS"           │  ✅ Respeito às Diretrizes de Plataforma      │
│     Portar a interface web desktop     │     Utilizar Tab Bars nativas, safe areas e   │
│     para mobile sem adaptar áreas de   │     gestos de swipe no iOS em vez de imitar a │
│     toque (mínimo de 44x44px no dedo). │     sidebar de desktop no celular.            │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo
- **Grid Virtualizado Responsivo**: A galeria do Refero emprega um layout modular de colunas dinâmicas baseado em CSS Grid com auto-fill e minmax (`grid-template-columns: repeat(auto-fill, minmax(320px, 1fr))`). Para coleções densas, é utilizada renderização virtualizada de nós DOM para manter 60 FPS contínuos durante a rolagem de mais de 40.000 imagens.
- **Sistema Espacial Base 4px/8px**: Toda a métrica de padding e margem obedece rigorosamente a múltiplos de 4: micro-espaçamentos em badges (`4px` e `8px`), paddings de cards (`12px` e `16px`) e respiros entre módulos principais (`24px`, `32px` e `48px`).
- **Linhas Divisórias Estruturais**: Uso sistemático de bordas de alta precisão com espessura exata de `1px` (`border-zinc-800` no modo escuro e `border-slate-200` no modo claro), evitando sombras espessas e garantindo divisão arquitetural nítida.
- **Gaveta Lateral de Inspeção (Sheet/Drawer)**: Ao clicar em qualquer tela ou fluxo, uma gaveta lateral animada via Framer Motion surge à direita da viewport (`w-[480px]` a `w-[640px]`), contendo metadados completos da aplicação: link direto para o site oficial, categorias de tags, elementos presentes, data de indexação e carrossel de passos sequenciais.

### 4.2 Sistemas de Cores, Superfícies & Texturas
- **Fundos Típicos**:
  - *Modo Escuro (Obsidian Studio)*: Fundo da janela em `#13151A`, superfícies de cartões e gavetas em `#1C1F26`, com estados de hover elevando para `#232731`.
  - *Modo Claro (Pristine Tech)*: Fundo em `#FFFFFF`, superfícies elevadas em `#F8FAFC`, divisórias em `#E2E8F0`.
- **Acabamento Especular & Micro-Bordas**: Cartões possuem frequentemente uma sutil borda de luz interior gerada via `box-shadow: inset 0 1px 0 0 rgba(255, 255, 255, 0.05)`, técnica de design de software de alto escalão popularizada por Linear e Vercel.
- **Mídia em Alta Definição com Placeholder Gradual**: Todas as capturas de tela são servidas em formatos modernos WebP/AVIF com cache em CDN edge global, acompanhadas de um esqueleto (*skeleton loader*) pulsante suave que previne oscilações de layout (*Cumulative Layout Shift - CLS*).

---

### 4.3 Catálogo de Arquétipos Notáveis de UI/UX (8 Padrões Reais)

O acervo do Refero categoriza de forma exemplar os seguintes 8 arquétipos indispensáveis na construção de produtos digitais contemporâneos:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        OS 8 ARQUÉTIPOS NOTÁVEIS DO REFERO DESIGN                       │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  1. Multi-Step Onboarding Journey  │  5. Enterprise Data Table & Faceted Filters       │
│  2. SaaS Pricing Tier Matrix       │  6. Dynamic Command Palette (CMD+K)               │
│  3. High-Density Analytics Dash    │  7. Constructive Empty State Primer               │
│  4. Contextual Paywall Interstitial│  8. Workspace RBAC Permissions Matrix             │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

#### Arquétipo 1: Multi-Step Onboarding Journey & Interactive Checklist
- **Anatomia**: Barra de progresso contínua no topo indicando porcentagem de avanço (`"Passo 2 de 4"`), título focado no benefício do usuário, campos mínimos de configuração com seleção por cards clicáveis (ex: *"Qual é o seu papel na empresa?"*), e checklist in-app expansível persistente no canto inferior direito para orientar o primeiro uso.
- **Gatilho de Interação**: Primeiro login após autenticação via OAuth/Magic Link.
- **Referência Típica no Refero**: Fluxos do Linear, Notion, Supabase e Loom.

#### Arquétipo 2: SaaS Pricing Tier Matrix & Feature Comparison
- **Anatomia**: Seletor comutador Mensal/Anual com badge de economia (`"Economize 20%"`), colunas modulares para planos (Free, Pro, Enterprise), destaque de contorno luminoso no plano mais popular (*"Most Popular"*), lista de recursos com ícones de verificação verdes (`CheckCircle`) e tabela colapsável de comparação profunda de especificações técnicas.
- **Gatilho de Interação**: Botão *"Upgrade"* no cabeçalho ou página pública de precificação.
- **Referência Típica no Refero**: Telas de precificação do Vercel, Resend, Raycast e PostHog.

#### Arquétipo 3: High-Density Analytical Dashboard & KPI Metric Cards
- **Anatomia**: Grade de 3 a 4 cartões de KPI no topo contendo o valor métrico em fonte monoespaçada de alto contraste, indicador de tendência percentual com cor semântica (verde positivo / vermelho negativo) e micro-gráfico de linha (*sparkline* SVG). Abaixo, gráficos analíticos interativos com filtros temporais rápidos (`24h`, `7d`, `30d`, `1 ano`).
- **Gatilho de Interação**: Tela inicial de entrada após autenticação.
- **Referência Típica no Refero**: Dashboards do Stripe, Plaid, June.so e Mixpanel.

#### Arquétipo 4: Contextual Paywall & Quota Limit Interstitial
- **Anatomia**: Modal elegante com fundo semi-transparente fosco (`backdrop-blur-md`), ilustração vetorial precisa do recurso bloqueado, barra de consumo de cota (`"Você atingiu 100% dos 5.000 créditos de IA"`), proposta de valor clara do plano superior e botão de chamada para ação imediato com teste gratuito de 14 dias.
- **Gatilho de Interação**: Usuário tenta disparar uma ação exclusiva do plano pago.
- **Referência Típica no Refero**: Paywalls in-app do Figma, GitHub Copilot, Midjourney e Perplexity.

#### Arquétipo 5: Enterprise Data Table com Faceted Filters & Batch Actions
- **Anatomia**: Barra de pesquisa rápida combinada com filtros rápidos (Status, Data, Responsável), cabeçalho de colunas com ordenação ascendente/descendente ao clique, linhas com altura compacta (`py-2.5`), seleção múltipla via checkbox que faz surgir uma barra flutuante de ações em lote (*batch actions*) e menu contextual de 3 pontos no final de cada registro.
- **Gatilho de Interação**: Navegação nas seções de gerenciamento de dados centrais do sistema.
- **Referência Típica no Refero**: Tabelas do Retool, Airtable, Plain e Ramp.

#### Arquétipo 6: Dynamic Command Palette (`CMD+K`) com Busca Fuzzy
- **Anatomia**: Diálogo flutuante centralizado na tela sobre overlay escurecido, campo de input limpo com atalho visível, grupos semânticos de navegação divididos por cabeçalhos sutis (*"Ações Recentes"*, *"Navegar para"*, *"Comandos de Workspace"*), cada item exibindo seu atalho de teclado correspondente alinhado à direita.
- **Gatilho de Interação**: Atalho de teclado global `CMD+K` ou `CTRL+K`, ou clique na barra de busca do topo.
- **Referência Típica no Refero**: Raycast, Linear, Cron/Notion Calendar e GitHub.

#### Arquétipo 7: Constructive Empty State Primer com Ação Direta
- **Anatomia**: Contêiner centralizado com contorno tracejado sutil (`border-dashed border-zinc-700`), ilustração monocromática minimalista, título explicativo amigável, dois parágrafos explicando como aquela funcionalidade agrega valor à operação e botão de ação em destaque com atalho de teclado para criar o primeiro registro imediatamente.
- **Gatilho de Interação**: Usuário entra em uma visualização ou pasta sem registros cadastrados.
- **Referência Típica no Refero**: Empty states do Slack, Figma Projects, Campfire e Basecamp.

#### Arquétipo 8: Workspace Settings & Granular Team RBAC Permissions
- **Anatomia**: Navegação em abas laterais ou horizontais (Geral, Membros, Cobrança, Segurança, Webhooks, API Keys). Na aba de Membros, lista de usuários com avatar, e-mail, status de convite e menu dropdown de atribuição de cargo (Owner, Admin, Member, Viewer) acompanhado de matriz descritiva de permissões.
- **Gatilho de Interação**: Configurações de administração da organização.
- **Referência Típica no Refero**: Painéis de equipe do Clerk, Supabase, Vercel Teams e Doppler.

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Arquitetura de Camadas Técnicas
Para materializar a excelência estética e a fidelidade de interação catalogadas no Refero Design, a stack recomendada combina:
- **Camada 1 (Primitivos Headless Acessíveis)**: `@radix-ui/react-dialog`, `@radix-ui/react-dropdown-menu`, `@radix-ui/react-tabs`, `@radix-ui/react-tooltip`.
- **Camada 2 (Motor de Estilos & Tokens)**: `Tailwind CSS v3/v4` com suporte a variáveis semânticas HSL/OKLCH e classes utilitárias de precisão de 1px.
- **Camada 3 (Física de Movimento & Transições)**: `framer-motion` com curvas de mola amortecida (*stiffness: 380, damping: 30*) para drawers laterais e diálogos.
- **Camada 4 (Design Tokens & DESIGN.md)**: Tokens semânticos extraídos pelo padrão Refero Styles.
- **Camada 7 (Agentes de IA & Model Context Protocol)**: Ingestão de contexto via servidor Refero MCP.

---

### 5.2 Tokens CSS & Layout Recipe

O código abaixo implementa uma **Galeria de Inspeção de UI & Navegador de Fluxos** inspirado diretamente na arquitetura funcional do Refero Design:

```tsx
// components/refero-gallery/ReferoInspectorGallery.tsx
"use client";

import React, { useState } from "react";
import { motion, AnimatePresence } from "framer-motion";
import { 
  Search, 
  Filter, 
  ExternalLink, 
  Layers, 
  Smartphone, 
  Monitor, 
  ChevronRight, 
  X, 
  Check, 
  Copy,
  SlidersHorizontal
} from "lucide-react";

interface ScreenItem {
  id: string;
  title: string;
  brand: string;
  platform: "web" | "ios";
  pageType: string;
  elements: string[];
  flowStep?: { current: number; total: number; flowName: string };
  imageUrl: string;
}

const SAMPLE_SCREENS: ScreenItem[] = [
  {
    id: "ref-01",
    title: "Interactive Onboarding Checklist & Workspace Setup",
    brand: "Linear",
    platform: "web",
    pageType: "Onboarding",
    elements: ["Checklist", "Progress Bar", "Modal", "Button Group"],
    flowStep: { current: 2, total: 5, flowName: "Team Activation Flow" },
    imageUrl: "https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?auto=format&fit=crop&w=1200&q=80"
  },
  {
    id: "ref-02",
    title: "Enterprise Pricing Matrix with Annual Savings Pill",
    brand: "Supabase",
    platform: "web",
    pageType: "Pricing",
    elements: ["Pricing Table", "Toggle Switch", "Badge", "Feature List"],
    flowStep: { current: 1, total: 3, flowName: "Plan Upgrade Flow" },
    imageUrl: "https://images.unsplash.com/photo-1551288049-bebda4e38f71?auto=format&fit=crop&w=1200&q=80"
  },
  {
    id: "ref-03",
    title: "Native iOS Biometric Auth & Quick Pay Bottom Sheet",
    brand: "Mercury",
    platform: "ios",
    pageType: "Checkout",
    elements: ["Bottom Sheet", "Numeric Keypad", "Biometric Icon", "Swipe CTA"],
    flowStep: { current: 3, total: 4, flowName: "Wire Transfer Flow" },
    imageUrl: "https://images.unsplash.com/photo-1559526324-4b87b5e36e44?auto=format&fit=crop&w=1200&q=80"
  },
  {
    id: "ref-04",
    title: "High-Density Real-time Metrics & Sparkline Cards",
    brand: "Stripe",
    platform: "web",
    pageType: "Dashboard",
    elements: ["KPI Card", "Sparkline", "Date Picker", "Export Button"],
    imageUrl: "https://images.unsplash.com/photo-1460925895917-afdab827c52f?auto=format&fit=crop&w=1200&q=80"
  }
];

export function ReferoInspectorGallery() {
  const [platform, setPlatform] = useState<"all" | "web" | "ios">("all");
  const [searchQuery, setSearchQuery] = useState("");
  const [selectedScreen, setSelectedScreen] = useState<ScreenItem | null>(null);
  const [copiedToken, setCopiedToken] = useState(false);

  const filteredScreens = SAMPLE_SCREENS.filter((screen) => {
    const matchesPlatform = platform === "all" || screen.platform === platform;
    const matchesSearch = 
      screen.title.toLowerCase().includes(searchQuery.toLowerCase()) ||
      screen.brand.toLowerCase().includes(searchQuery.toLowerCase()) ||
      screen.pageType.toLowerCase().includes(searchQuery.toLowerCase());
    return matchesPlatform && matchesSearch;
  });

  const handleCopyTokens = () => {
    navigator.clipboard.writeText(`/* Refero Design System Tokens */
:root {
  --canvas-bg: #13151A;
  --surface-card: #1C1F26;
  --surface-hover: #232731;
  --border-subtle: #272B35;
  --text-primary: #F8FAFC;
  --text-secondary: #94A3B8;
  --accent-action: #3B82F6;
  --radius-card: 10px;
}`);
    setCopiedToken(true);
    setTimeout(() => setCopiedToken(false), 2000);
  };

  return (
    <div className="min-h-screen bg-[#13151A] text-[#F8FAFC] font-sans antialiased selection:bg-blue-600 selection:text-white">
      {/* Top Navigation Bar */}
      <header className="sticky top-0 z-30 border-b border-[#272B35] bg-[#13151A]/85 backdrop-blur-md px-6 py-3.5 flex items-center justify-between">
        <div className="flex items-center gap-6">
          <div className="flex items-center gap-2.5">
            <div className="w-8 h-8 rounded-lg bg-blue-600 flex items-center justify-center font-bold text-white shadow-lg shadow-blue-500/20">
              R
            </div>
            <span className="font-semibold text-lg tracking-tight">Refero Engine</span>
            <span className="text-[11px] font-mono px-2 py-0.5 rounded-full bg-[#1C1F26] border border-[#272B35] text-[#94A3B8]">
              40,000+ Screens
            </span>
          </div>

          {/* Platform Segmented Switch */}
          <div className="hidden md:flex items-center p-0.5 rounded-lg bg-[#1C1F26] border border-[#272B35]">
            <button
              onClick={() => setPlatform("all")}
              className={`px-3 py-1 text-xs font-medium rounded-md transition-all ${
                platform === "all" ? "bg-[#272B35] text-white shadow-sm" : "text-[#94A3B8] hover:text-white"
              }`}
            >
              All Platforms
            </button>
            <button
              onClick={() => setPlatform("web")}
              className={`flex items-center gap-1.5 px-3 py-1 text-xs font-medium rounded-md transition-all ${
                platform === "web" ? "bg-[#272B35] text-white shadow-sm" : "text-[#94A3B8] hover:text-white"
              }`}
            >
              <Monitor className="w-3.5 h-3.5" /> Web Apps
            </button>
            <button
              onClick={() => setPlatform("ios")}
              className={`flex items-center gap-1.5 px-3 py-1 text-xs font-medium rounded-md transition-all ${
                platform === "ios" ? "bg-[#272B35] text-white shadow-sm" : "text-[#94A3B8] hover:text-white"
              }`}
            >
              <Smartphone className="w-3.5 h-3.5" /> iOS Apps
            </button>
          </div>
        </div>

        {/* Global Search Input & Quick Actions */}
        <div className="flex items-center gap-3 w-full max-w-md ml-4">
          <div className="relative w-full">
            <Search className="absolute left-3 top-1/2 -translate-y-1/2 w-4 h-4 text-[#94A3B8]" />
            <input
              type="text"
              value={searchQuery}
              onChange={(e) => setSearchQuery(e.target.value)}
              placeholder="Search by brand, page (Onboarding, Paywall) or element..."
              className="w-full pl-9 pr-12 py-1.5 bg-[#1C1F26] border border-[#272B35] rounded-lg text-xs placeholder-[#94A3B8] text-white focus:outline-none focus:border-blue-500 transition-colors"
            />
            <kbd className="absolute right-2.5 top-1/2 -translate-y-1/2 text-[10px] font-mono px-1.5 py-0.5 rounded bg-[#272B35] text-[#94A3B8] border border-white/5">
              ⌘K
            </kbd>
          </div>

          <button 
            onClick={handleCopyTokens}
            className="flex items-center gap-1.5 px-3 py-1.5 rounded-lg bg-[#1C1F26] hover:bg-[#272B35] border border-[#272B35] text-xs font-medium text-white transition-colors"
            title="Copy DESIGN.md CSS Tokens"
          >
            {copiedToken ? <Check className="w-3.5 h-3.5 text-emerald-400" /> : <Copy className="w-3.5 h-3.5 text-[#94A3B8]" />}
            <span className="hidden sm:inline">DESIGN.md</span>
          </button>
        </div>
      </header>

      {/* Main Grid Content */}
      <main className="p-6 max-w-[1600px] mx-auto">
        <div className="flex items-center justify-between mb-6">
          <div>
            <h1 className="text-xl font-bold tracking-tight">Curated Real-World Interface Library</h1>
            <p className="text-xs text-[#94A3B8] mt-0.5">
              Inspecting production UI screens, flows, and atomic components for software builders.
            </p>
          </div>
          <div className="flex items-center gap-2">
            <button className="flex items-center gap-1.5 px-3 py-1.5 rounded-lg bg-[#1C1F26] border border-[#272B35] text-xs text-[#94A3B8] hover:text-white transition-colors">
              <SlidersHorizontal className="w-3.5 h-3.5" /> Filters
            </button>
          </div>
        </div>

        {/* Masonry-like CSS Grid */}
        <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-5">
          {filteredScreens.map((screen) => (
            <motion.div
              key={screen.id}
              layoutId={screen.id}
              onClick={() => setSelectedScreen(screen)}
              className="group cursor-pointer rounded-xl bg-[#1C1F26] border border-[#272B35] overflow-hidden hover:border-zinc-700 hover:shadow-xl transition-all duration-200"
            >
              {/* Screen Preview Container */}
              <div className="relative aspect-[16/10] bg-[#13151A] overflow-hidden">
                <img
                  src={screen.imageUrl}
                  alt={screen.title}
                  className="w-full h-full object-cover object-top group-hover:scale-[1.02] transition-transform duration-300"
                  loading="lazy"
                />
                {screen.flowStep && (
                  <div className="absolute top-2.5 left-2.5 px-2 py-0.5 rounded-md bg-[#13151A]/85 backdrop-blur-md border border-[#272B35] text-[10px] font-mono text-blue-400 flex items-center gap-1">
                    <Layers className="w-3 h-3" /> Step {screen.flowStep.current}/{screen.flowStep.total}
                  </div>
                )}
                <div className="absolute top-2.5 right-2.5 px-2 py-0.5 rounded-md bg-[#13151A]/85 backdrop-blur-md border border-[#272B35] text-[10px] uppercase font-semibold tracking-wider text-[#94A3B8]">
                  {screen.platform}
                </div>
              </div>

              {/* Screen Meta Card */}
              <div className="p-4">
                <div className="flex items-center justify-between text-xs mb-1.5">
                  <span className="font-semibold text-white group-hover:text-blue-400 transition-colors">
                    {screen.brand}
                  </span>
                  <span className="text-[11px] px-2 py-0.5 rounded bg-[#272B35] text-[#94A3B8]">
                    {screen.pageType}
                  </span>
                </div>
                <h3 className="text-xs font-normal text-zinc-300 line-clamp-1 mb-3">
                  {screen.title}
                </h3>

                {/* Atomic Tag Pills */}
                <div className="flex flex-wrap gap-1.5">
                  {screen.elements.slice(0, 3).map((elem, i) => (
                    <span
                      key={i}
                      className="text-[10px] px-2 py-0.5 rounded-md bg-[#13151A] border border-[#272B35] text-zinc-400"
                    >
                      {elem}
                    </span>
                  ))}
                  {screen.elements.length > 3 && (
                    <span className="text-[10px] px-1.5 py-0.5 rounded-md bg-[#13151A] border border-[#272B35] text-zinc-500">
                      +{screen.elements.length - 3}
                    </span>
                  )}
                </div>
              </div>
            </motion.div>
          ))}
        </div>
      </main>

      {/* Slide-Over Inspection Drawer (Refero Inspector Pattern) */}
      <AnimatePresence>
        {selectedScreen && (
          <div className="fixed inset-0 z-50 flex justify-end">
            {/* Backdrop */}
            <motion.div
              initial={{ opacity: 0 }}
              animate={{ opacity: 1 }}
              exit={{ opacity: 0 }}
              onClick={() => setSelectedScreen(null)}
              className="absolute inset-0 bg-black/60 backdrop-blur-sm"
            />

            {/* Drawer Sheet */}
            <motion.div
              initial={{ x: "100%" }}
              animate={{ x: 0 }}
              exit={{ x: "100%" }}
              transition={{ type: "spring", stiffness: 350, damping: 32 }}
              className="relative w-full max-w-xl h-full bg-[#1C1F26] border-l border-[#272B35] shadow-2xl flex flex-col z-10"
            >
              {/* Drawer Header */}
              <div className="flex items-center justify-between p-5 border-b border-[#272B35]">
                <div className="flex items-center gap-2.5">
                  <div className="w-7 h-7 rounded-md bg-blue-600 flex items-center justify-center font-bold text-xs text-white">
                    {selectedScreen.brand[0]}
                  </div>
                  <div>
                    <h2 className="text-sm font-semibold text-white">{selectedScreen.brand}</h2>
                    <p className="text-[11px] text-[#94A3B8]">{selectedScreen.pageType} • {selectedScreen.platform.toUpperCase()}</p>
                  </div>
                </div>

                <div className="flex items-center gap-2">
                  <a
                    href="https://refero.design"
                    target="_blank"
                    rel="noreferrer"
                    className="p-1.5 rounded-lg hover:bg-[#272B35] text-[#94A3B8] hover:text-white transition-colors"
                    title="Open on Refero"
                  >
                    <ExternalLink className="w-4 h-4" />
                  </a>
                  <button
                    onClick={() => setSelectedScreen(null)}
                    className="p-1.5 rounded-lg hover:bg-[#272B35] text-[#94A3B8] hover:text-white transition-colors"
                  >
                    <X className="w-4 h-4" />
                  </button>
                </div>
              </div>

              {/* Drawer Scrollable Body */}
              <div className="flex-1 overflow-y-auto p-5 space-y-5">
                {/* Full Screenshot View */}
                <div className="rounded-lg overflow-hidden border border-[#272B35] bg-[#13151A]">
                  <img
                    src={selectedScreen.imageUrl}
                    alt={selectedScreen.title}
                    className="w-full object-contain"
                  />
                </div>

                {/* Flow Sequence Info */}
                {selectedScreen.flowStep && (
                  <div className="p-4 rounded-lg bg-[#13151A] border border-[#272B35]">
                    <div className="flex items-center justify-between mb-2">
                      <span className="text-xs font-semibold text-white flex items-center gap-1.5">
                        <Layers className="w-4 h-4 text-blue-400" />
                        {selectedScreen.flowStep.flowName}
                      </span>
                      <span className="text-[11px] font-mono text-[#94A3B8]">
                        Step {selectedScreen.flowStep.current} of {selectedScreen.flowStep.total}
                      </span>
                    </div>
                    {/* Stepper Dots */}
                    <div className="flex gap-1.5 mt-2">
                      {Array.from({ length: selectedScreen.flowStep.total }).map((_, idx) => (
                        <div
                          key={idx}
                          className={`h-1.5 flex-1 rounded-full ${
                            idx + 1 === selectedScreen.flowStep?.current
                              ? "bg-blue-500"
                              : idx + 1 < (selectedScreen.flowStep?.current || 0)
                              ? "bg-blue-900"
                              : "bg-[#272B35]"
                          }`}
                        />
                      ))}
                    </div>
                  </div>
                )}

                {/* Breakdown of UI Elements */}
                <div>
                  <h4 className="text-xs font-semibold uppercase tracking-wider text-[#94A3B8] mb-2.5">
                    Detected UI Elements & Atoms
                  </h4>
                  <div className="grid grid-cols-2 gap-2">
                    {selectedScreen.elements.map((elem, i) => (
                      <div
                        key={i}
                        className="flex items-center justify-between p-2 rounded-lg bg-[#13151A] border border-[#272B35] text-xs text-zinc-300"
                      >
                        <span>{elem}</span>
                        <ChevronRight className="w-3.5 h-3.5 text-zinc-600" />
                      </div>
                    ))}
                  </div>
                </div>

                {/* MCP Prompt Ingestion Suggestion */}
                <div className="p-4 rounded-lg bg-blue-950/20 border border-blue-900/40 text-xs">
                  <h5 className="font-semibold text-blue-300 mb-1">Refero MCP AI Prompt Suggestion:</h5>
                  <p className="text-blue-200/80 font-mono text-[11px] leading-relaxed">
                    "Implement a {selectedScreen.pageType} layout adhering to {selectedScreen.brand}'s design system with {selectedScreen.elements.join(', ')} using Tailwind CSS and Radix UI primitives."
                  </p>
                </div>
              </div>
            </motion.div>
          </div>
        )}
      </AnimatePresence>
    </div>
  );
}
```

---

### 5.3 O Formato `DESIGN.md` (Refero Styles Pattern)

Uma das maiores contribuições técnicas do ecossistema Refero para desenvolvedores e agentes de IA é o padrão estruturado **`DESIGN.md`** (distribuído através de `styles.refero.design`). Ao contrário de documentações volumosas em PDF ou páginas estáticas de storybooks, este arquivo encapsula o sistema de regras estéticas em markdown conciso que cabe perfeitamente na janela de contexto de qualquer LLM moderno.

Abaixo está o modelo canônico de um `DESIGN.md` extraído de uma aplicação SaaS de alto nível catalogada no Refero:

```markdown
# DESIGN.md — Production SaaS System Specification
Source: Extracted via Refero Styles Engine

## 1. Visual Foundation
- **Theme**: Obsidian Dark Mode (Primary) / Slate Clean Light (Secondary)
- **Border Radius**: 
  - Subtle Buttons/Inputs: `6px` (`rounded-md`)
  - Elevated Cards/Modals: `10px` (`rounded-lg`)
  - Floating Toolbars/Badges: `9999px` (`rounded-full`)
- **Grid & Layout**: 
  - Standard Canvas: 12-column grid, max-width 1440px
  - Spacing Scale: Base 4px (padding: 4px, 8px, 12px, 16px, 24px, 32px)
  - Structural Borders: `1px solid #272B35` with 0px blur drop shadows

## 2. Color Tokens
- Canvas Background: `#13151A`
- Card Surface: `#1C1F26`
- Surface Hover State: `#232731`
- Structural Border: `#272B35`
- Primary Brand Accent: `#3B82F6` (Electric Blue)
- Success / Positive Trend: `#10B981` (Emerald)
- Warning / Usage Limit: `#F59E0B` (Amber)
- Destructive / Error: `#EF4444` (Ruby)
- Typography Primary: `#F8FAFC` (Slate 50)
- Typography Muted: `#94A3B8` (Slate 400)

## 3. Typography Hierarchy
- Display Headers: Neo-Grotesque (Inter / Geist Sans), font-weight: 600, letter-spacing: -0.02em
- Body Text: Inter / Geist Sans Regular, font-weight: 400, line-height: 1.5
- Metrics & Code Tokens: Geist Mono / JetBrains Mono, font-weight: 500, tabular-nums

## 4. Component Rules
- Buttons: Primary buttons use `#3B82F6` with hover `#2563EB`, active scale(0.98), inner highlight 1px.
- Modals: Always use Radix Dialog with `backdrop-blur-md` and spring transition.
- Empty States: Must include icon, title, 2-line explanation, and primary action button.
- Data Tables: Fixed headers, row hover in `#232731`, compact cell padding (`py-2.5 px-4`).
```

---

### 5.4 Integração com Refero MCP (Model Context Protocol)

O Refero oferece integração direta com editores e ferramentas de IA (Claude Code, Cursor, Windsurf) através de seu servidor oficial MCP (`https://api.refero.design/mcp`), permitindo que agentes façam consultas em tempo real antes de escrever código de frontend.

Exemplo de configuração no arquivo `.cursor/mcp.json` ou `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "refero-design": {
      "command": "npx",
      "args": ["-y", "@refero/mcp-server"],
      "env": {
        "REFERO_API_KEY": "sua-chave-api-refero-aqui"
      }
    }
  }
}
```

Ao ativar o MCP, o agente passa a ter acesso a ferramentas como:
- `refero_search_screens(query, page_type, platform)`: Retorna capturas e metadados de telas reais de produtos.
- `refero_get_flow(flow_name, brand)`: Retorna todas as etapas sequenciais de um fluxo específico (ex: Onboarding do Linear).
- `refero_get_design_system(brand_slug)`: Retorna o arquivo `DESIGN.md` completo da marca consultada.

---

### 5.5 Guia de Pesquisa ao Vivo para Agentes de IA

Quando um agente autônomo precisar navegar ou apontar URLs de referência no Refero Design, ele deve utilizar a seguinte estrutura de rotas e taxonomia paramétrica:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        MAPA DE ROTAS & TAXONOMIA AO VIVO DO REFERO                     │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  DOMÍNIO BASE: https://refero.design/                                                  │
│                                                                                        │
│  PLATAFORMAS:                                                                          │
│  • Aplicações Web:        https://refero.design/web-apps                               │
│  • Aplicativos Móveis iOS: https://refero.design/ios-apps                               │
│                                                                                        │
│  PESQUISA POR PÁGINAS (PAGES):                                                         │
│  • Dashboards Analíticos: https://refero.design/pages/dashboard                        │
│  • Precificação / Pricing: https://refero.design/pages/pricing                          │
│  • Paywalls & Assinaturas: https://refero.design/pages/paywall                          │
│  • Autenticação & Login:  https://refero.design/pages/login                            │
│  • Configurações / Conta:  https://refero.design/pages/settings                         │
│  • Páginas de Erro 404:    https://refero.design/pages/404                              │
│                                                                                        │
│  PESQUISA POR ELEMENTOS ATÔMICOS (ELEMENTS):                                           │
│  • Modais & Diálogos:     https://refero.design/elements/modal                         │
│  • Tabelas de Dados:      https://refero.design/elements/table                         │
│  • Menus Laterais/Sidebars: https://refero.design/elements/sidebar                     │
│  • Estados Vazios / Empty: https://refero.design/elements/empty-state                  │
│  • Barras de Ferramentas: https://refero.design/elements/toolbar                       │
│                                                                                        │
│  PESQUISA POR JORNADAS DE USUÁRIO (FLOWS):                                             │
│  • Onboarding Completo:   https://refero.design/flows/onboarding                       │
│  • Cadastro / Sign Up:    https://refero.design/flows/sign-up                          │
│  • Checkout / Assinatura: https://refero.design/flows/subscribe                        │
│  • Cancelamento & Churn:  https://refero.design/flows/delete-account                   │
│                                                                                        │
│  PESQUISA POR MARCAS ESPECÍFICAS (COMPANIES):                                          │
│  • https://refero.design/companies/linear                                              │
│  • https://refero.design/companies/notion                                              │
│  • https://refero.design/companies/supabase                                            │
│  • https://refero.design/companies/stripe                                               │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao incorporar o DNA e os padrões curados do **Refero Design** na arquitetura de um projeto através do `DESIGN_BLUEPRINT.md`, os seguintes mandamentos técnicos devem ser aplicados:

1. **Adoção do Padrão "Real Software First"**:
   - Toda proposta de interface deve incluir o ciclo de vida completo: estado de carregamento (*skeleton* com animação suave), estado de sucesso com dados simulados realistas (*truncamento de strings*, *números formatados* com vírgulas e centavos), estado vazio (*empty state* construtivo com botão de ação) e modal de tratamento de erro acessível.
2. **Definição Explícita de Tokens em `DESIGN.md`**:
   - Criar e versionar um arquivo `DESIGN.md` na raiz do projeto com as exatas definições de raios de curvatura (máximo de 3 variações: `6px`, `10px` e `full`), contraste cromático em conformidade com WCAG AA e escala modular de tipografia monoespaçada e neo-grotesca.
3. **Mapeamento de Jornadas por Fluxos Multi-Telas**:
   - Não aprovar telas de checkout ou onboarding sem descrever a sequência passo a passo numerada (ex: `1. Informações básicas ──► 2. Escolha de workspace ──► 3. Convite de time ──► 4. Dashboard pronta`).
4. **Precisão Arquitetural de 1px com Sombras Especulares**:
   - Eliminar sombras difusas de software amador (`blur > 30px`). Utilizar divisores de `1px solid` em tom cinza escuro/claro e realces internos sutis (`box-shadow: inset 0 1px 0 rgba(255,255,255,0.06)`).
5. **Harmonia da Regra 60-30-10**:
   - Assegurar que 60% da área visual pertença ao canvas neutro de fundo, 30% aos contêineres e tipografia de suporte escaneável, e apenas 10% aos acentos semânticos de foco e botões de chamada primária.
