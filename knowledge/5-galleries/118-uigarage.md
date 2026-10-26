---
id: "118-uigarage"
name: "UI Garage"
url: "https://uigarage.net/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico:
  - "Multi-Platform Atomic UI Pattern Benchmarking (Web, iOS, Android, Tablet)"
  - "Granular Component Isolation over Macro-Page Distractions"
  - "Ergonomic Micro-Interaction Catalog (Empty States, Modals, Feed Cards & Drawers)"
  - "Real-World In-App Implementation Benchmarks (7,000+ Curated Production Shots)"
  - "Device-Specific Mental Models (Mobile Touch Targets ⟷ Desktop Cursor Densities)"
  - "Minimalist Utilitarian Curation Interface (Slate Canvas with 1px Hairline Precision)"
densidade_informacao: "Alta/Utilitaria & Multi-Plataforma (Componentes Atômicos, Telas de Fluxo e Micro-Estados)"
impacto_visual: "Minimalista/Silencioso & Utilitário Curado"
custo_computacional: "Baixo (Renderização DOM nativa, CSS Grid responsivo, micro-interações de elevação aceleradas por GPU, zero sobrecarga WebGL)"
stack_frameworks:
  - "React 19 / Next.js 14/15"
  - "Tailwind CSS v3/v4 (arbitrary variants, container queries, specular borders)"
  - "Framer Motion / Motion.dev (layout springs, tab switching transitions, card hover elevation)"
  - "Radix UI Primitives (Dialogs, Tabs, Tooltips, Dropdowns, Segmented Controls)"
  - "Lucide React / Phosphor Icons"
compatibilidade:
  fontes_ideais:
    - "Neo-Grotesques Técnicas de Alta Legibilidade: Inter, Geist Sans, Plus Jakarta Sans, SF Pro Display / Text, Roboto"
    - "Monoespaçadas de Engenharia para Tags, Identificadores e Tokens: IBM Plex Mono, Geist Mono, JetBrains Mono, SF Mono"
    - "Display Sans Funcionais para Títulos de Categorias: Cabinet Grotesk, PP Neue Montreal, General Sans, Satoshi"
  paletas_ideais:
    - "UI Garage Slate Minimal (Modo Claro Padrão): #FFFFFF (Canvas Fundo), #F8FAFC (Superfície Neutra Slate 50), #E2E8F0 (Borda Sutil 1px), #0F172A (Texto Primário Slate 900), #64748B (Texto Secundário Slate 500), #2563EB / #3B82F6 (Acento Royal Blue / Cobalt), #10B981 (Status Ativo / Sucesso)"
    - "UI Garage Obsidian Pro (Modo Escuro Dev/Design): #0B0F17 (Canvas Void Escuro), #131A26 (Superfície do Card), #1E293B (Borda Especular 1px), #F8FAFC (Texto Primário Alabastro), #94A3B8 (Texto Secundário Slate 400), #60A5FA (Acento Sky Blue), #38BDF8 (Hover State)"
    - "Regra 60-30-10 de Curadoria de Componentes: 60% Superfície Neutra de Fundo (#FFFFFF ou #0B0F17), 30% Estrutura de Grids, Banners de Filtro, Bordas de 1px e Tipografia Estrutural, 10% Acentos Semânticos (Badges de Plataforma 'iOS/Web/Android', Chips de Categoria Ativa, Botões de Inspeção e Ações de Cópia)"
  combinacoes_recomendadas:
    - "Seletor de Plataforma em Segmented Control (Web ⟷ iOS ⟷ Android ⟷ Tablet) no topo do catálogo"
    - "Cards de componente com proporção adaptativa (3:4 para Mobile, 16:10 para Web, 4:3 para Tablet) com crachá flutuante de plataforma"
    - "Barra de filtros facetados com hierarquia de duas camadas: Família do Componente (Navegação, Formulários, Overlays) ➔ Padrão Atômico Específico (Modals, Empty States, Bottom Sheets)"
    - "Modal de inspeção com zoom de alta fidelidade e visualização lado a lado de variações em modo claro e escuro"
    - "Gaveta lateral de detalhes com lista de micro-estados documentados (Default, Hover, Active, Disabled, Error, Loading)"
    - "Integração de busca rápida universal com sugestões por palavras-chave de componentes e atalhos de teclado"
  conflitos_esteticos:
    - "Misturar diretrizes de plataforma (ex: aplicar gestos e padrões do Material Design Android ou iOS Human Interface Guidelines sem adaptação em interfaces Desktop Web)"
    - "Telas 'Dribbblizadas' puramente conceituais sem tratamento de estados de erro, truncamento de texto longo ou requisitos de toque mínimo (44x44px no mobile)"
    - "Superfícies pesadas com gradientes agressivos ou neomorfismos opacos que competem com o conteúdo do screenshot catalogado"
    - "Carrosséis com scroll lento ou transições espalhafatosas que impedem a rápida comparação lado a lado de múltiplos padrões"
    - "Ausência de metadados de contexto (não identificar a plataforma de origem, a versão do SO ou o caso de uso do componente)"
---

# UI Garage — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
██╗   ██╗██╗     ██████╗  █████╗ ██████╗  █████╗  ██████╗ ███████╗
██║   ██║██║    ██╔════╝ ██╔══██╗██╔══██╗██╔══██╗██╔════╝ ██╔════╝
██║   ██║██║    ██║  ███╗███████║██████╔╝███████║██║  ███╗█████╗  
██║   ██║██║    ██║   ██║██╔══██║██╔══██╗██╔══██║██║   ██║██╔══╝  
╚██████╔╝██║    ╚██████╔╝██║  ██║██║  ██║██║  ██║╚██████╔╝███████╗
 ╚═════╝ ╚═╝     ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝ ╚═════╝ ╚══════╝
```

---

## 1. DNA Estético & Filosofia de Curadoria

O **UI Garage** (`https://uigarage.net/`) foi um dos pioneiros e mais influentes repositórios mundiais de **curadoria atômica de padrões de interface de usuário (UI Patterns)**, focado especificamente na desconstrução granular de telas e componentes em ambientes **Web, Mobile (iOS e Android) e Tablet**. 

Criado pelo designer de produto e empreendedor independente **Philippe Hong** (`@PhilippeHong`) em meados de 2016, o projeto foi concebido a partir de uma dor universal vivenciada por engenheiros de software e product designers: a ausência de um catálogo estruturado que respondesse não à pergunta *"como é a landing page deste produto?"*, mas sim à indagação cirúrgica: *"como os líderes do mercado desenharam o seu modal de cancelamento, a barra de navegação inferior (tab bar) no iOS ou o estado vazio (empty state) de suas tabelas de dados?"*.

Ao longo de quase uma década de operação ininterrupta — culminando na conquista de **#1 Product of the Day no Product Hunt** e reunindo um acervo de aproximadamente **7.000 componentes reais catalogados** —, o UI Garage pavimentou a metodologia de consulta atômica que mais tarde inspirou plataformas contemporâneas como Mobbin, Refero Design e SaaS Interface.

```
┌────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                              A REVOLUÇÃO ATÔMICA DO UI GARAGE (2016–2024)                              │
├────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│  ❌ GALERIAS DE MARKETING TRADICIONAIS         │  ✅ ARQUITETURA ATÔMICA DO UI GARAGE                  │
│  • Captura exclusiva da Landing Page pública   │  • Telas profundas de componentes isolados            │
│  • Foco em copywriting comercial e heróis Web  │  • Mapeamento cross-platform (Web, iOS, Android, Pad) │
│  • Nenhuma referência para micro-interações    │  • Foco em Empty States, Modals, Feed Cards, Inputs   │
│  • Dificuldade de filtrar por átomo de UI      │  • Filtros bidirecionais por Plataforma e Componente  │
│  • Inspiração superficial para frontends       │  • Especificação técnica de proporções e ergonomia    │
└────────────────────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 A Origem Histórica e a Visão de Philippe Hong

Antes do surgimento do UI Garage, a busca por inspiração de interface sofria de uma dicotomia extrema:
1. De um lado, sites como **Dribbble** e **Behance** estavam repletos de "shots" conceituais visualmente deslumbrantes, porém desconectados das restrições de código, acessibilidade, estados de erro e limites de toque físico de telas móveis.
2. De outro lado, galerias de sites como **Awwwards** e **FWA** premiavam experiências WebGL pesadas e experimentais, completamente impróprias para sistemas operacionais de software corporativo ou aplicações mobile de uso contínuo.

Philippe Hong projetou o UI Garage com a premissa de **"Design Pattern Search Engine"**: um mecanismo de busca visual onde qualquer designer ou desenvolvedor pudesse digitar `Pricing Table`, `Onboarding Walkthrough`, `Search Bar` ou `404 Error` e filtrar imediatamente pelo ambiente de destino (`iOS`, `Android`, `Web` ou `Tablet`). O objetivo primordial era economizar centenas de horas de retrabalho na engenharia de interface, demonstrando convenções consolidadas pelo mercado.

### 1.2 O Fim do Ciclo e a Transição para o Cromojo

Após oito anos de curadoria manual intensiva, o fundador encerrou oficialmente as operações ativas do UI Garage, deixando na home do domínio uma carta de agradecimento à comunidade global de design e formalizando a sua transição para uma nova ferramenta focada em otimização de conversão e receita: o **Cromojo** (`https://cromojo.com`). 

Mesmo com o encerramento da ingestão diária de novos screenshots, o legado metodológico, a taxonomia de classificação de componentes e a anatomia de layout estabelecida pelo UI Garage tornaram-se o modelo canônico para arquitetura de Design Systems, servindo de base para o padrão de catalogação atômica do nosso Design Engine.

```
┌────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                        THE UI GARAGE CROSS-PLATFORM TAXONOMY ENGINE                                    │
├────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│  [ PLATFORM SELECTOR ] ──► [ WEB (Desktop) ] ──► [ iOS (Mobile) ] ──► [ ANDROID ] ──► [ TABLET ]       │
│                                                                                                        │
│  [ 1. NAVIGATION ]     ──► Menus, Navbars, Sidebars, Tab Bars, Breadcrumbs, Pagination, Footers        │
│  [ 2. FORMS & INPUTS ] ──► Inputs, Textareas, Selects, Checkboxes, Radios, Toggles, Sliders, Pickers  │
│  [ 3. FEEDBACK/OVERLAY]──► Modals, Alerts, Tooltips, Toasts, Empty States, Progress/Loaders, 404       │
│  [ 4. CONTENT & DATA ] ──► Cards, Data Grids, Lists, Pricing Tables, Accordions, Timelines, Carousels  │
│  [ 5. USER FLOWS ]     ──► Onboarding, Sign Up, Login, Checkout / Cart, Profiles, Settings, Dashboards │
└────────────────────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

O UI Garage é a **Referência Primária de Direção de Arte e Engenharia Atômica** quando o projeto exige:

1. **Benchmarking de Micro-Interações e Componentes Desacoplados**:
   - Quando a equipe de engenharia frontend precisa prototipar uma família específica de componentes — por exemplo, desenhar um seletor de data (*date picker*), um sistema de toasts de notificação ou um modal de confirmação destrutiva — sem perder tempo reiventando a roda ergonômica.
2. **Design Systems Multi-Plataforma Omnichannel**:
   - Projetos que demandam paridade conceitual entre Web Desktop e Apps Nativos (iOS e Android). O UI Garage oferece a comparação imediata de como a mesma tarefa (ex: autenticação em duas etapas) é abordada respeitando as convenções de cada sistema operacional (Touch target de 44pt no iOS vs. foco por teclado em 24px de padding na Web).
3. **Resolução de Estados de Borda (Edge Cases & Empty States)**:
   - Interfaces funcionais não podem exibir espaços vazios estéreis. A consulta ao catálogo de *Empty States* do UI Garage orienta a composição de telas vazias educativas contendo vetor ilustrativo sutil, copy contextual explicativo e botão de chamada para ação direta (CTA).
4. **Matrizes de Preço (Pricing Tables) de Alta Conversão**:
   - Criação de tabelas comparativas de planos com alternador mensal/anual (*billing toggle*), destaque para o plano mais popular (*badge de recomendação*), lista de benefícios com ícones de checagem e botões de conversão com hierarquia visual nítida.

### 2.1 Emoção e Posicionamento de Marca

O estilo de curadoria do UI Garage comunica:
- **Pragmatismo Funcional**: Interfaces limpas que priorizam a clareza da tarefa sobre firulas estéticas.
- **Autoridade Operacional**: Utilização de padrões familiares aos usuários, reduzindo a carga cognitiva e eliminando curvas de aprendizado desnecessárias.
- **Rigor Ergonômico**: Atenção estrita ao posicionamento dos controles em relação à zona do polegar (*thumb zone*) em dispositivos móveis e à varredura visual em padrão F ou Z na Web.

### 2.2 A Regra 60-30-10 na Curadoria de Componentes

```
┌────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                              A DISTRIBUIÇÃO CROMÁTICA CANÔNICA (60-30-10)                              │
├────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│  60%  │  SUPERFÍCIE NEUTRA DE CANVAS (#FFFFFF / #F8FAFC ou #0B0F17 no Modo Escuro)                     │
│       │  Garante máxima legibilidade, contraste e espaço negativo ao redor dos componentes.            │
├───────┼────────────────────────────────────────────────────────────────────────────────────────────────┤
│  30%  │  ESTRUTURA DE CONTENÇÃO & TIPOGRAFIA (#0F172A / #E2E8F0 / #64748B)                             │
│       │  Linhas divisórias finas de 1px, cabeçalhos de seções, textos secundários e bordas de cards.   │
├───────┼────────────────────────────────────────────────────────────────────────────────────────────────┤
│  10%  │  ACENTOS SEMÂNTICOS & GATILHOS INTERATIVOS (#2563EB / #3B82F6 / #10B981)                       │
│       │  Badges de plataforma ('iOS', 'Web'), chips de seleção ativa, botões de ação e estados de foco.│
└────────────────────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

⚠️ **Incompatível com**:
1. **Sites Portfólio de Alta Expressão Artística ou Experimental**:
   - Projetos de premiação (Awwwards / FWA / CSSDA) que buscam desconstruir as convenções tradicionais da web por meio de layouts caóticos, scroll-jacking, distorções de malha 3D e tipografia monumental desestruturada.
2. **Campanhas de Branding de Luxo / Moda Imersiva**:
   - Onde o valor da marca é transmitido pelo mistério, imagens cinematográficas em tela cheia e ausência proposital de elementos utilitários evidentes.
3. **Aplicações Monolíticas sem Nuance de Plataforma**:
   - Projetos que tentam forçar um único layout web responsivo sem respeitar as peculiaridades de ecossistemas touch mobile (como gestos de deslizar, barras inferiores nativas e safe-areas de entalhe).

⚠️ **Armadilhas de Imitação (O que Evitar)**:
- **"Component Soup" (Sopa de Componentes Desconexos)**: Copiar um card do Stripe, uma barra de navegação do Airbnb e uma tabela do Notion sem unificar a escala de espaçamentos (8pt grid), os raios de curvatura de borda (`border-radius`) e a paleta de cores neutras.
- **Cegueira de Plataforma ("Platform Blindness")**: Portar controles estritamente móveis (como um seletor em tambor giratório estilo roda do iOS) diretamente para desktop, forçando o usuário de mouse a interagir com controles concebidos para o toque.
- **Obsolescência Temporal**: O UI Garage catalogou interfaces entre 2016 e 2024. É crucial não replicar padrões ultrapassados de versões antigas do iOS (como gradientes pastosos ou sombras difusas estilo skeuomorphism suave de 2016), atualizando sempre os tokens para a estética contemporânea de bordas milimétricas e superfícies translúcidas com blur.
- **Cópia Descontextualizada sem Estados de Interação**: Criar um componente apenas no seu estado estático de sucesso, sem planejar o comportamento em telas com texto longo, falhas de conexão de rede, validações assíncronas e leitores de tela acessíveis (WAI-ARIA).

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo

1. **Sistema Espacial Modular de 8 Pontos (8pt Spatial Grid)**:
   - Todo o dimensionamento de componentes, paddings internos e margens segue incrementos estritos de 4px e 8px: `gap-2` (8px), `gap-4` (16px), `gap-6` (24px), `p-6` (24px), `p-8` (32px).
2. **Grids Responsivos Adaptativos por Tipo de Dispositivo**:
   - **Visualização Web**: Grid de 3 a 4 colunas com aspect-ratio 16:10 (`aspect-[16/10]`) para acomodar telas amplas de desktop com barras laterais visíveis.
   - **Visualização Mobile**: Grid de 4 a 6 colunas de cards verticais com aspect-ratio 9:19.5 (`aspect-[9/19.5]`) reproduzindo a proporção exata de smartphones modernos com Dynamic Island ou entalhe.
   - **Visualização Tablet**: Grid de 2 a 3 colunas em aspect-ratio 4:3 (`aspect-[4/3]`) ilustrando layouts com colunas duplas e navegação mista.
3. **Contornos e Delimitação Especular**:
   - Uso cirúrgico de bordas de `1px solid` com valores sutis (`#E2E8F0` no modo claro, `#1E293B` no modo escuro) substituindo sombras pesadas por contraste de contorno de alta precisão.

### 4.2 Sistemas de Cores, Superfícies & Texturas

- **Fundos Neutros Alabastro & Ardósia**: Fundo principal `#FFFFFF` ou `#F8FAFC`, criando um palco calmo e silencioso que não distorce a fidelidade cromática das telas expostas.
- **Elevação por Camadas Sutis**: Cards com fundo branco, borda de 1px e sombra micro-linear (`box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.05), 0 1px 2px -1px rgba(0, 0, 0, 0.05)`). No hover, elevação fluida com transição física de mola (`translate-y-[-2px]` com sombra `0 10px 15px -3px rgba(0, 0, 0, 0.08)`).
- **Tipografia Escaneável**:
  - Títulos em Neo-Grotesk neutra (Inter / Geist Sans) em peso semibold (600) e tracking levemente negativo (`-0.02em`).
  - Badges e identificadores de plataforma em fonte monoespaçada legível (IBM Plex Mono / Geist Mono) em caixa alta reduzida (11px, `uppercase`, `tracking-wider`).

---

### 4.3 Catálogo Detalhado de Componentes & Padrões Notáveis

Abaixo estão os **8 principais arquétipos atômicos** desconstruídos a partir do acervo histórico do UI Garage:

```
┌────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                              CATÁLOGO DOS 8 ARQUÉTIPOS ATÔMICOS DO UI GARAGE                           │
├────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│  1. Seletor de Plataforma em Segmented Control (Web / iOS / Android / Tablet)                          │
│  2. Card de Amostra Atômica com Badge de Dispositivo & Hover Elevation                                │
│  3. Empty State Contextual com Vetor Ilustrativo & Ação Primária                                       │
│  4. Dialog Modal com Header Semântico, Área Scrollável & Barra de Ações                                │
│  5. Mobile Bottom Navigation Bar (Tab Bar com Gatilho Central Destacado)                               │
│  6. Autenticação Split-Screen (Painel de Branding + Formulário de Login/Cadastro)                      │
│  7. Matriz de Tabela de Preços (Tiered Pricing Matrix) com Alternador Anual/Mensal                     │
│  8. Gaveta Deslizante de Filtros Facetados (Slide-over Faceted Filter Drawer)                          │
└────────────────────────────────────────────────────────────────────────────────────────────────────────┘
```

#### Arquétipo 1: Seletor de Plataforma em Segmented Control

Controle de alternância segmentada localizado no topo do catálogo que permite ao usuário alternar a lente do ecossistema mantendo a mesma categoria selecionada.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│  [ 🌐 Web Desktop ]  │  [ 📱 iOS Native ]  │  [ 🤖 Android ]  │  [ 📟 Tablet ]         │
└────────────────────────────────────────────────────────────────────────────────────────┘
```
- **Anatomia**: Contêiner arredondado (`rounded-xl`), fundo cinza claro sutil (`#F1F5F9`), cursor deslizante animado com mola suave (`layoutId="activeTab"` no Framer Motion), ícones vetoriais de 16px acompanhados de label tipográfico com peso 500.
- **Gatilho**: Clique ou toque direto, com feedback tátil e atualização instantânea do aspecto dimensional dos cards na grade.
- **Onde Aplicar**: Cabeçalhos de bibliotecas de componentes, páginas de download de softwares multi-plataforma e alternadores de modo de visualização em editores de design.

#### Arquétipo 2: Card de Amostra Atômica com Badge de Dispositivo

O elemento fundamental de exibição de conteúdo do UI Garage.

```
┌──────────────────────────────────────────────┐
│  ┌────────────────────────────────────────┐  │
│  │                                        │  │
│  │            SCREENSHOT PREVIEW          │  │
│  │           (Proporção do Device)        │  │
│  │                                        │  │
│  │  [ iOS 17 ]              [ EXPAND ⤢ ]  │  │
│  └────────────────────────────────────────┘  │
│  Linear Mobile App                           │
│  BottomSheet Filter Component                │
│  #Navigation  #BottomSheet  #DarkTheme       │
└──────────────────────────────────────────────┘
```
- **Anatomia**: Contêiner com borda fina de 1px (`#E2E8F0`), cantos arredondados de 12px, área visual com máscara de corte (`overflow-hidden`), badge absoluto superior identificando a plataforma (`iOS`, `Android`, `Web`), título da aplicação, subtítulo com a taxonomia do átomo e tags clicáveis.
- **Gatilho**: `hover` do mouse ativa leve translação vertical de -3px, sombra difusa e revelação do botão flutuante de inspeção rápida.

#### Arquétipo 3: Empty State Contextual com Vetor Ilustrativo

Padrão para interfaces de tabelas, caixas de entrada ou listas sem dados cadastrados.

```
┌──────────────────────────────────────────────────────────────┐
│                                                              │
│                      ┌───────────────┐                       │
│                      │   [ 📭 ICON ]  │                       │
│                      └───────────────┘                       │
│                Nenhuma fatura encontrada                     │
│    Você ainda não gerou cobranças no ciclo fiscal atual.     │
│    Crie a sua primeira fatura para iniciar o fluxo.          │
│                                                              │
│                  ┌────────────────────────┐                  │
│                  │  + Criar Nova Fatura   │                  │
│                  └────────────────────────┘                  │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```
- **Anatomia**: Ícone circular ou ilustração geométrica em tom suave monocromático, título em H3 com contraste forte, parágrafo de apoio explicativo limitado a 380px de largura e botão primário convidativo com ícone `+`.
- **Gatilho**: Carregamento da página quando a consulta à API retorna lista vazia (`data.length === 0`).
- **Onde Aplicar**: Dashboards, gerenciadores de arquivos, listas de membros de equipe e carrinhos de compras vazios.

#### Arquétipo 4: Dialog Modal com Header Semântico e Ações Fixas

Diálogo modal de foco concentrado para configurações ou confirmações críticas.

```
┌──────────────────────────────────────────────────────────────┐
│  Confirmar Cancelamento de Assinatura             [ ✕ Esc ]  │
├──────────────────────────────────────────────────────────────┤
│  Tem certeza de que deseja encerrar o plano Pro do workspace │
│  "Acme Corp"? Ao confirmar:                                  │
│                                                              │
│  • Os membros perderão acesso imediato aos recursos de IA    │
│  • O histórico de versões será mantido por apenas 30 dias    │
│  • Nenhuma cobrança adicional será emitida no seu cartão     │
├──────────────────────────────────────────────────────────────┤
│  [ Manter Meu Plano ]             [ Confirmar Cancelamento ] │
└──────────────────────────────────────────────────────────────┘
```
- **Anatomia**: Backdrop com desfoque de fundo (`backdrop-blur-sm bg-slate-900/40`), contêiner centrado com largura máxima de 520px, cabeçalho com título claro e botão fechar, corpo informativo com lista de tópicos em bullets e rodapé com botões de cancelamento (secundário neutro) e ação destrutiva (vermelho ou texto contrastante).
- **Gatilho**: Acionamento por botão de ação sensível; fecha ao pressionar a tecla `Escape` ou clicar fora do diálogo.

#### Arquétipo 5: Mobile Bottom Navigation Bar com Central Action Trigger

A clássica barra inferior móvel (Tab Bar) com elevação física e área de toque generosa.

```
┌──────────────────────────────────────────────────────────────┐
│    [ 🏠 ]        [ 🔍 ]        ┌────┐        [ 🔔 ]    [ 👤 ]│
│    Início        Busca         │ ➕ │       Alertas    Perfil│
│                                └────┘                        │
└──────────────────────────────────────────────────────────────┘
```
- **Anatomia**: Barra de 64px de altura com preenchimento para a barra de início do sistema (`padding-bottom: env(safe-area-inset-bottom)`), 5 pontos de interação com ícones balanceados, label textual em 10px e botão central de ação proeminente em elevação flutuante (FAB) para ações de criação frequentes.
- **Gatilho**: Toque nas abas aciona transição de tela sem recarregamento; feedback com micro-vibração háptica quando em ambiente nativo.

#### Arquétipo 6: Autenticação Split-Screen (Split Hero + Form)

Layout moderno de login e cadastro corporativo com separação visual de 50/50.

```
┌──────────────────────────────┬──────────────────────────────┐
│  LOGO EMPRESA                │  Bem-vindo de volta 👋       │
│                              │  Insira suas credenciais     │
│  "A infraestrutura que       │                              │
│  potencializa mais de 10.000 │  [ Email institucional     ] │
│  sistemas críticos no mundo."│  [ Senha de acesso         ] │
│                              │                              │
│  ── Sarah Jenkins, VP Tech   │  [       Entrar no Sistema ] │
│                              │                              │
│  [ Painel Gráfico Abstrato ] │  Não tem conta? Cadastre-se  │
└──────────────────────────────┴──────────────────────────────┘
```
- **Anatomia**: Coluna esquerda contendo branding, depoimento social ou métrica relevante em fundo ardósia escuro com degradê radial sutil; coluna direita contendo formulário limpo em fundo branco, inputs com foco em anel azul (`ring-2 ring-blue-500/20`), autenticação social (SSO) e links de recuperação de senha.
- **Gatilho**: Rota `/login` ou `/signup`. Em telas mobile, a coluna esquerda é ocultada, centralizando o formulário em viewport único.

#### Arquétipo 7: Matriz de Tabela de Preços com Alternador Mensal/Anual

Componente comercial de conversão para planos de assinatura de software.

```
┌──────────────────────────────────────────────────────────────┐
│                   Escolha o plano ideal                      │
│            [ Mensal ]  ( O )  [ Anual (Economize 20%) ]       │
├──────────────────────────────┬───────────────────────────────┤
│  STARTER                     │  PRO (MAIS POPULAR) ⭐        │
│  $19 / mês                   │  $49 / mês                    │
│  Para criadores individuais  │  Para times de crescimento    │
│                              │                               │
│  ✓ Até 5 projetos ativos     │  ✓ Projetos ilimitados        │
│  ✓ Exportação em 1080p       │  ✓ Exportação em 4K HDR       │
│  ✓ Suporte por e-mail        │  ✓ Suporte prioritário 24/7   │
│                              │  ✓ Acesso à API REST          │
│                              │                               │
│  [ Começar Gratuitamente ]   │  [ Assinar Plano Pro ]        │
└──────────────────────────────┴───────────────────────────────┘
```
- **Anatomia**: Interruptor toggle no topo com etiqueta de desconto anual; cards com destaque visual para a opção recomendada (borda azul de 2px, badge flutuante superior "Mais Popular" e botão com preenchimento total contrastante vs. botão outlined nos planos regulares).
- **Gatilho**: Alternar o switch recalcula dinamicamente os valores de preço com transição animada de números.

#### Arquétipo 8: Gaveta Deslizante de Filtros Facetados (Slide-Over Drawer)

Painel lateral para refinamento de buscas complexas em catálogos com centenas de itens.

```
┌──────────────────────────────────────────────────────────────┐
│  Filtros Avançados                                [ ✕ Fechar]│
├──────────────────────────────────────────────────────────────┤
│  PLATAFORMA                                                  │
│  [✓] Web Desktop    [ ] iOS Native    [ ] Android Tablet     │
│                                                              │
│  CATEGORIA DO COMPONENTE                                     │
│  (•) Todos    ( ) Navegação    ( ) Formulários    ( ) Modais │
│                                                              │
│  TEMA VISUAL                                                 │
│  [ ] Modo Claro    [✓] Modo Escuro                           │
│                                                              │
│  INTERVALO DE DATA                                           │
│  [ Últimos 30 dias                                       ▼ ] │
├──────────────────────────────────────────────────────────────┤
│  [ Limpar Filtros ]                  [ Aplicar 142 Resultados│
└──────────────────────────────────────────────────────────────┘
```
- **Anatomia**: Painel deslizante ancorado à direita da tela (largura de 380px a 440px), cabeçalho fixo com contagem de filtros ativos, corpo com scroll vertical independente agrupando seletores por acordião ou seções semânticas, e rodapé fixo com botão de redefinição e botão primário com feedback em tempo real da contagem de resultados.
- **Gatilho**: Clique no botão "Filtros" na barra de busca principal.

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Mapeamento no Design Engine

O estilo utilitário do UI Garage se traduz perfeitamente através das camadas da nossa arquitetura de engenharia de design:
- **Camada 1 (Fundamentos & Tokens)**: Escala tipográfica rigorosa, grid de 8pt, raio modular (`rounded-xl = 12px`), paleta neutra de ardósia (Slate) e acentos azuis funcionais.
- **Camada 2 (Primitivos Headless)**: Primitivos não-estilizados do Radix UI (`@radix-ui/react-dialog`, `@radix-ui/react-tabs`, `@radix-ui/react-popover`) assegurando conformidade total com acessibilidade WAI-ARIA e suporte completo a navegação por teclado.
- **Camada 3 (Física & Movimento)**: Molas críticas (*springs*) sem oscilações espalhafatosas (`stiffness: 400`, `damping: 30`) para abertura de modais e transições de abas ativas via `layoutId`.
- **Camada 4 (Componentes Compostos)**: Cards de amostras de UI com carregamento preguiçoso (*lazy loading*), badges inteligentes e visualizador de zoom em modal.
- **Camada 7 (Agentes & LLMs)**: Regras prescritivas para IA gerar interfaces com separação consciente entre padrões Web e Mobile nativos.

---

### 5.2 Tokens CSS & Layout Recipe Canônica

```css
:root {
  /* ==========================================================================
     UI Garage Design Tokens — Slate Minimal Curation Standard
     ========================================================================== */
  
  /* Fundos e Telas */
  --uigarage-canvas: #FFFFFF;
  --uigarage-surface-muted: #F8FAFC;
  --uigarage-surface-raised: #FFFFFF;
  --uigarage-surface-overlay: rgba(15, 23, 42, 0.4);

  /* Linhas e Contornos */
  --uigarage-border-subtle: #E2E8F0;
  --uigarage-border-medium: #CBD5E1;
  --uigarage-border-focus: #3B82F6;

  /* Tipografia & Textos */
  --uigarage-text-primary: #0F172A;
  --uigarage-text-secondary: #64748B;
  --uigarage-text-tertiary: #94A3B8;
  --uigarage-text-inverted: #FFFFFF;

  /* Acentos Interativos e Plataformas */
  --uigarage-accent-primary: #2563EB;
  --uigarage-accent-hover: #1D4ED8;
  --uigarage-accent-subtle: #EFF6FF;
  --uigarage-badge-ios: #007AFF;
  --uigarage-badge-android: #34A853;
  --uigarage-badge-web: #6366F1;
  --uigarage-badge-tablet: #8B5CF6;

  /* Geometria e Raios */
  --uigarage-radius-sm: 6px;
  --uigarage-radius-md: 10px;
  --uigarage-radius-lg: 14px;
  --uigarage-radius-full: 9999px;

  /* Elevação e Sombras */
  --uigarage-shadow-card: 0 1px 3px 0 rgba(0, 0, 0, 0.05), 0 1px 2px -1px rgba(0, 0, 0, 0.05);
  --uigarage-shadow-hover: 0 12px 20px -4px rgba(15, 23, 42, 0.08), 0 4px 6px -2px rgba(15, 23, 42, 0.04);
  --uigarage-shadow-modal: 0 25px 50px -12px rgba(15, 23, 42, 0.25);

  /* Transições de Física */
  --uigarage-ease-spring: cubic-bezier(0.16, 1, 0.3, 1);
  --uigarage-duration-fast: 150ms;
  --uigarage-duration-base: 220ms;
}

/* Modo Escuro Opcional */
.dark, [data-theme="dark"] {
  --uigarage-canvas: #0B0F17;
  --uigarage-surface-muted: #111827;
  --uigarage-surface-raised: #161F30;
  --uigarage-surface-overlay: rgba(0, 0, 0, 0.75);

  --uigarage-border-subtle: #1E293B;
  --uigarage-border-medium: #334155;

  --uigarage-text-primary: #F8FAFC;
  --uigarage-text-secondary: #94A3B8;
  --uigarage-text-tertiary: #64748B;

  --uigarage-accent-subtle: #1E293B;
  --uigarage-shadow-card: 0 1px 3px 0 rgba(0, 0, 0, 0.3);
  --uigarage-shadow-hover: 0 12px 24px -4px rgba(0, 0, 0, 0.5);
}
```

---

### 5.3 Implementação Funcional Completa em React + Tailwind + Framer Motion

Abaixo está o componente completo e funcional `UIGaragePatternBrowser`, que encapsula a experiência canônica do UI Garage: alternador de plataforma em abas com mola de layout, filtragem rápida por categorias de átomos de interface, grade responsiva com aspect ratio adaptativo por dispositivo e modal de inspeção de alta precisão com visualização de tokens:

```tsx
import React, { useState } from 'react';
import { motion, AnimatePresence } from 'framer-motion';
import { 
  Laptop, 
  Smartphone, 
  Tablet as TabletIcon, 
  Layers, 
  Search, 
  ExternalLink, 
  X, 
  Check, 
  Copy, 
  ChevronRight,
  SlidersHorizontal,
  Info
} from 'lucide-react';

// Tipos do Modelo de Dados
type PlatformType = 'all' | 'web' | 'ios' | 'android' | 'tablet';
type CategoryType = 'all' | 'navigation' | 'forms' | 'overlays' | 'empty-states' | 'pricing';

interface PatternItem {
  id: string;
  title: string;
  product: string;
  platform: 'web' | 'ios' | 'android' | 'tablet';
  category: CategoryType;
  imageUrl: string;
  tags: string[];
  tokens: {
    padding: string;
    radius: string;
    border: string;
    background: string;
  };
}

// Acervo Demonstrativo com Padrões Reais de Produto
const PATTERNS_DATA: PatternItem[] = [
  {
    id: 'linear-filter-drawer',
    title: 'Faceted View Filter Drawer',
    product: 'Linear App',
    platform: 'web',
    category: 'navigation',
    imageUrl: 'https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?auto=format&fit=crop&w=800&q=80',
    tags: ['Filter', 'Drawer', 'Shortcuts', 'Dark Mode'],
    tokens: {
      padding: '16px 20px',
      radius: '12px',
      border: '1px solid #23272F',
      background: '#12141C'
    }
  },
  {
    id: 'stripe-billing-modal',
    title: 'Payment Method Confirmation Dialog',
    product: 'Stripe Dashboard',
    platform: 'web',
    category: 'overlays',
    imageUrl: 'https://images.unsplash.com/photo-1551288049-bebda4e38f71?auto=format&fit=crop&w=800&q=80',
    tags: ['Modal', 'Billing', 'Credit Card', 'Security'],
    tokens: {
      padding: '24px 32px',
      radius: '16px',
      border: '1px solid #E2E8F0',
      background: '#FFFFFF'
    }
  },
  {
    id: 'airbnb-bottom-nav',
    title: 'Haptic Bottom Navigation Tab Bar',
    product: 'Airbnb iOS',
    platform: 'ios',
    category: 'navigation',
    imageUrl: 'https://images.unsplash.com/photo-1512941937669-90a1b58e7e9c?auto=format&fit=crop&w=800&q=80',
    tags: ['TabBar', 'Touch Target', 'Safe Area', 'Micro-interactions'],
    tokens: {
      padding: '8px 16px 28px',
      radius: '0px',
      border: '1px solid #F1F5F9',
      background: 'rgba(255, 255, 255, 0.85)'
    }
  },
  {
    id: 'notion-empty-workspace',
    title: 'First-Run Blank Canvas Empty State',
    product: 'Notion Desktop',
    platform: 'web',
    category: 'empty-states',
    imageUrl: 'https://images.unsplash.com/photo-1507238691740-187a5b1d37b8?auto=format&fit=crop&w=800&q=80',
    tags: ['Empty State', 'Onboarding', 'Call-to-Action', 'Minimal'],
    tokens: {
      padding: '48px 24px',
      radius: '8px',
      border: '1px dashed #CBD5E1',
      background: '#F8FAFC'
    }
  },
  {
    id: 'revolut-kyc-stepper',
    title: 'Identity Verification Multi-Step Form',
    product: 'Revolut Android',
    platform: 'android',
    category: 'forms',
    imageUrl: 'https://images.unsplash.com/photo-1563986768609-322da13575f3?auto=format&fit=crop&w=800&q=80',
    tags: ['Form', 'KYC', 'Stepper', 'Camera Integration'],
    tokens: {
      padding: '20px 24px',
      radius: '20px',
      border: 'none',
      background: '#0F172A'
    }
  },
  {
    id: 'framer-pricing-matrix',
    title: 'Annual / Monthly Tiered Pricing Table',
    product: 'Framer Web',
    platform: 'web',
    category: 'pricing',
    imageUrl: 'https://images.unsplash.com/photo-1460925895917-afdab827c52f?auto=format&fit=crop&w=800&q=80',
    tags: ['Pricing', 'Toggle', 'Comparison', 'High Conversion'],
    tokens: {
      padding: '32px 28px',
      radius: '16px',
      border: '2px solid #3B82F6',
      background: '#FFFFFF'
    }
  }
];

export function UIGaragePatternBrowser() {
  const [selectedPlatform, setSelectedPlatform] = useState<PlatformType>('all');
  const [selectedCategory, setSelectedCategory] = useState<CategoryType>('all');
  const [searchQuery, setSearchQuery] = useState('');
  const [activeModalItem, setActiveModalItem] = useState<PatternItem | null>(null);
  const [copiedToken, setCopiedToken] = useState<string | null>(null);

  // Filtragem Dinâmica
  const filteredPatterns = PATTERNS_DATA.filter((item) => {
    const matchesPlatform = selectedPlatform === 'all' || item.platform === selectedPlatform;
    const matchesCategory = selectedCategory === 'all' || item.category === selectedCategory;
    const matchesSearch = 
      item.title.toLowerCase().includes(searchQuery.toLowerCase()) ||
      item.product.toLowerCase().includes(searchQuery.toLowerCase()) ||
      item.tags.some(t => t.toLowerCase().includes(searchQuery.toLowerCase()));

    return matchesPlatform && matchesCategory && matchesSearch;
  });

  const handleCopyToken = (key: string, value: string) => {
    navigator.clipboard.writeText(`${key}: ${value};`);
    setCopiedToken(key);
    setTimeout(() => setCopiedToken(null), 2000);
  };

  const getPlatformBadgeColor = (plat: PatternItem['platform']) => {
    switch (plat) {
      case 'ios': return 'bg-blue-50 text-blue-700 border-blue-200 dark:bg-blue-950/40 dark:text-blue-300 dark:border-blue-800';
      case 'android': return 'bg-emerald-50 text-emerald-700 border-emerald-200 dark:bg-emerald-950/40 dark:text-emerald-300 dark:border-emerald-800';
      case 'web': return 'bg-indigo-50 text-indigo-700 border-indigo-200 dark:bg-indigo-950/40 dark:text-indigo-300 dark:border-indigo-800';
      case 'tablet': return 'bg-purple-50 text-purple-700 border-purple-200 dark:bg-purple-950/40 dark:text-purple-300 dark:border-purple-800';
    }
  };

  return (
    <div className="w-full min-h-screen bg-slate-50 dark:bg-[#0B0F17] text-slate-900 dark:text-slate-100 font-sans antialiased">
      {/* Top Navigation & Brand Header */}
      <header className="sticky top-0 z-30 bg-white/90 dark:bg-[#0B0F17]/90 backdrop-blur-md border-b border-slate-200 dark:border-slate-800 px-6 py-4">
        <div className="max-w-7xl mx-auto flex flex-col md:flex-row items-center justify-between gap-4">
          <div className="flex items-center gap-3">
            <div className="w-10 h-10 rounded-xl bg-blue-600 flex items-center justify-center text-white shadow-md shadow-blue-500/20 font-bold tracking-tighter text-xl">
              UI
            </div>
            <div>
              <div className="flex items-center gap-2">
                <span className="font-bold text-lg tracking-tight">UI Garage</span>
                <span className="text-xs px-2 py-0.5 rounded-full bg-slate-100 dark:bg-slate-800 text-slate-600 dark:text-slate-400 font-mono">
                  Archive & Engine
                </span>
              </div>
              <p className="text-xs text-slate-500 dark:text-slate-400">
                Catálogo Atômico Multi-Plataforma de Padrões de Interface
              </p>
            </div>
          </div>

          {/* Quick Search Bar */}
          <div className="relative w-full md:w-80">
            <Search className="w-4 h-4 absolute left-3 top-1/2 -translate-y-1/2 text-slate-400" />
            <input 
              type="text"
              placeholder="Buscar por componente, tag ou app..."
              value={searchQuery}
              onChange={(e) => setSearchQuery(e.target.value)}
              className="w-full pl-9 pr-4 py-2 bg-slate-100 dark:bg-slate-900/60 border border-slate-200 dark:border-slate-800 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-blue-500/20 focus:border-blue-500 transition-all placeholder:text-slate-400"
            />
          </div>
        </div>
      </header>

      {/* Main Content Layout */}
      <main className="max-w-7xl mx-auto px-6 py-8">
        {/* Platform Segmented Switcher */}
        <section className="flex flex-col sm:flex-row items-start sm:items-center justify-between gap-4 mb-8">
          <div className="inline-flex p-1.5 bg-slate-200/70 dark:bg-slate-800/80 rounded-2xl border border-slate-300/40 dark:border-slate-700/50">
            {[
              { id: 'all', label: 'Todas as Plataformas', icon: Layers },
              { id: 'web', label: 'Web Desktop', icon: Laptop },
              { id: 'ios', label: 'iOS Native', icon: Smartphone },
              { id: 'android', label: 'Android', icon: Smartphone },
              { id: 'tablet', label: 'Tablet / Pad', icon: TabletIcon }
            ].map((tab) => {
              const Icon = tab.icon;
              const isActive = selectedPlatform === tab.id;
              return (
                <button
                  key={tab.id}
                  onClick={() => setSelectedPlatform(tab.id as PlatformType)}
                  className={`relative flex items-center gap-2 px-3.5 py-1.5 rounded-xl text-xs font-medium transition-colors z-10 ${
                    isActive 
                      ? 'text-slate-900 dark:text-white' 
                      : 'text-slate-600 dark:text-slate-400 hover:text-slate-900 dark:hover:text-slate-200'
                  }`}
                >
                  <Icon className="w-3.5 h-3.5" />
                  <span>{tab.label}</span>
                  {isActive && (
                    <motion.div
                      layoutId="platformActiveIndicator"
                      className="absolute inset-0 bg-white dark:bg-slate-900 rounded-xl shadow-sm -z-10 border border-slate-200/60 dark:border-slate-700"
                      transition={{ type: 'spring', stiffness: 450, damping: 32 }}
                    />
                  )}
                </button>
              );
            })}
          </div>

          <div className="text-xs font-mono text-slate-500">
            Exibindo <span className="font-semibold text-slate-900 dark:text-slate-100">{filteredPatterns.length}</span> padrões
          </div>
        </section>

        {/* Category Facet Filter Chips */}
        <div className="flex items-center gap-2 overflow-x-auto pb-4 mb-8 scrollbar-none">
          <SlidersHorizontal className="w-4 h-4 text-slate-400 shrink-0 mr-1" />
          {[
            { id: 'all', label: 'Todos os Componentes' },
            { id: 'navigation', label: 'Navegação & Tab Bars' },
            { id: 'forms', label: 'Formulários & Inputs' },
            { id: 'overlays', label: 'Modais & Diálogos' },
            { id: 'empty-states', label: 'Estados Vazios (Empty States)' },
            { id: 'pricing', label: 'Tabelas de Preços' }
          ].map((cat) => {
            const isCatActive = selectedCategory === cat.id;
            return (
              <button
                key={cat.id}
                onClick={() => setSelectedCategory(cat.id as CategoryType)}
                className={`px-3.5 py-1.5 rounded-lg text-xs font-medium whitespace-nowrap transition-all border ${
                  isCatActive
                    ? 'bg-blue-600 text-white border-blue-600 shadow-sm shadow-blue-500/20'
                    : 'bg-white dark:bg-slate-900 text-slate-600 dark:text-slate-400 border-slate-200 dark:border-slate-800 hover:border-slate-300 dark:hover:border-slate-700'
                }`}
              >
                {cat.label}
              </button>
            );
          })}
        </div>

        {/* Card Grid with Device-Aware Proportions */}
        <motion.div 
          layout
          className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6"
        >
          <AnimatePresence>
            {filteredPatterns.map((item) => (
              <motion.article
                layout
                initial={{ opacity: 0, scale: 0.95 }}
                animate={{ opacity: 1, scale: 1 }}
                exit={{ opacity: 0, scale: 0.95 }}
                transition={{ duration: 0.2 }}
                key={item.id}
                className="group relative bg-white dark:bg-[#121824] rounded-2xl border border-slate-200 dark:border-slate-800 overflow-hidden shadow-sm hover:shadow-xl hover:border-blue-300 dark:hover:border-blue-900 transition-all duration-300 flex flex-col"
              >
                {/* Visual Preview Container */}
                <div className="relative aspect-[16/10] bg-slate-100 dark:bg-slate-900 overflow-hidden">
                  <img 
                    src={item.imageUrl} 
                    alt={item.title}
                    className="w-full h-full object-cover object-top transition-transform duration-500 group-hover:scale-105"
                  />
                  <div className="absolute inset-0 bg-gradient-to-t from-black/60 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity flex items-end p-4">
                    <button 
                      onClick={() => setActiveModalItem(item)}
                      className="w-full py-2 bg-white/95 text-slate-900 rounded-xl text-xs font-semibold flex items-center justify-center gap-2 shadow-lg backdrop-blur-sm hover:bg-white transition-colors"
                    >
                      <ExternalLink className="w-3.5 h-3.5" />
                      Inspecionar Padrão Atômico
                    </button>
                  </div>

                  {/* Device Tag Badge */}
                  <span className={`absolute top-3 left-3 text-[10px] font-mono uppercase tracking-wider font-semibold px-2.5 py-1 rounded-md border shadow-xs ${getPlatformBadgeColor(item.platform)}`}>
                    {item.platform}
                  </span>
                </div>

                {/* Card Meta Content */}
                <div className="p-5 flex-1 flex flex-col justify-between">
                  <div>
                    <span className="text-[11px] font-mono text-blue-600 dark:text-blue-400 font-medium">
                      {item.product}
                    </span>
                    <h3 className="text-sm font-semibold text-slate-900 dark:text-slate-100 mt-0.5 tracking-tight group-hover:text-blue-600 dark:group-hover:text-blue-400 transition-colors">
                      {item.title}
                    </h3>
                  </div>

                  {/* Micro Tags */}
                  <div className="flex flex-wrap gap-1.5 mt-4">
                    {item.tags.map((tag) => (
                      <span 
                        key={tag}
                        className="text-[10px] px-2 py-0.5 bg-slate-100 dark:bg-slate-800/60 text-slate-600 dark:text-slate-400 rounded-md"
                      >
                        #{tag}
                      </span>
                    ))}
                  </div>
                </div>
              </motion.article>
            ))}
          </AnimatePresence>
        </motion.div>

        {/* Empty Search Fallback */}
        {filteredPatterns.length === 0 && (
          <div className="w-full py-16 flex flex-col items-center justify-center text-center">
            <div className="w-16 h-16 rounded-full bg-slate-100 dark:bg-slate-800 flex items-center justify-center text-slate-400 mb-4">
              <Info className="w-8 h-8" />
            </div>
            <h4 className="text-base font-semibold text-slate-900 dark:text-slate-100">
              Nenhum padrão encontrado
            </h4>
            <p className="text-xs text-slate-500 max-w-sm mt-1 mb-4">
              Tente redefinir a busca por texto ou alternar entre plataformas móveis e web.
            </p>
            <button
              onClick={() => {
                setSelectedPlatform('all');
                setSelectedCategory('all');
                setSearchQuery('');
              }}
              className="text-xs font-semibold px-4 py-2 bg-blue-600 text-white rounded-xl shadow-sm hover:bg-blue-700 transition-colors"
            >
              Redefinir Filtros
            </button>
          </div>
        )}
      </main>

      {/* Atomic Inspection Modal */}
      <AnimatePresence>
        {activeModalItem && (
          <div className="fixed inset-0 z-50 flex items-center justify-center p-4">
            {/* Modal Backdrop */}
            <motion.div 
              initial={{ opacity: 0 }}
              animate={{ opacity: 1 }}
              exit={{ opacity: 0 }}
              onClick={() => setActiveModalItem(null)}
              className="absolute inset-0 bg-slate-950/60 backdrop-blur-sm"
            />

            {/* Modal Window */}
            <motion.div
              initial={{ opacity: 0, scale: 0.95, y: 10 }}
              animate={{ opacity: 1, scale: 1, y: 0 }}
              exit={{ opacity: 0, scale: 0.95, y: 10 }}
              transition={{ type: 'spring', stiffness: 400, damping: 30 }}
              className="relative w-full max-w-4xl bg-white dark:bg-[#121824] rounded-2xl border border-slate-200 dark:border-slate-800 shadow-2xl overflow-hidden z-10 flex flex-col md:flex-row max-h-[90vh]"
            >
              {/* Left Column: Image Canvas */}
              <div className="md:w-3/5 bg-slate-100 dark:bg-slate-950 p-6 flex items-center justify-center overflow-auto border-b md:border-b-0 md:border-r border-slate-200 dark:border-slate-800">
                <img 
                  src={activeModalItem.imageUrl} 
                  alt={activeModalItem.title}
                  className="max-h-[60vh] w-auto object-contain rounded-lg shadow-md"
                />
              </div>

              {/* Right Column: Specifications & Tokens */}
              <div className="md:w-2/5 p-6 flex flex-col justify-between overflow-y-auto">
                <div>
                  <div className="flex items-center justify-between mb-4">
                    <span className={`text-[10px] font-mono uppercase tracking-wider font-semibold px-2.5 py-1 rounded-md border ${getPlatformBadgeColor(activeModalItem.platform)}`}>
                      {activeModalItem.platform}
                    </span>
                    <button 
                      onClick={() => setActiveModalItem(null)}
                      className="p-1 rounded-lg hover:bg-slate-100 dark:hover:bg-slate-800 text-slate-400 hover:text-slate-600 transition-colors"
                    >
                      <X className="w-5 h-5" />
                    </button>
                  </div>

                  <span className="text-xs font-mono text-blue-600 dark:text-blue-400 font-semibold">
                    {activeModalItem.product}
                  </span>
                  <h2 className="text-lg font-bold text-slate-900 dark:text-slate-100 mt-1">
                    {activeModalItem.title}
                  </h2>
                  <p className="text-xs text-slate-500 mt-2 leading-relaxed">
                    Padrão de referência atômico extraído para calibração de consistência dimensional e ritmo visual.
                  </p>

                  {/* Design Tokens Recipe */}
                  <div className="mt-6">
                    <h4 className="text-[11px] font-mono uppercase tracking-wider text-slate-400 font-semibold mb-3">
                      Tokens de Engenharia Extraídos
                    </h4>
                    <div className="space-y-2">
                      {Object.entries(activeModalItem.tokens).map(([key, val]) => (
                        <div 
                          key={key}
                          className="flex items-center justify-between p-2 rounded-lg bg-slate-50 dark:bg-slate-900/60 border border-slate-200/60 dark:border-slate-800/80 text-xs font-mono"
                        >
                          <div>
                            <span className="text-slate-400">{key}: </span>
                            <span className="font-semibold text-slate-800 dark:text-slate-200">{val}</span>
                          </div>
                          <button
                            onClick={() => handleCopyToken(key, val)}
                            className="p-1 text-slate-400 hover:text-blue-600 transition-colors"
                            title="Copiar token"
                          >
                            {copiedToken === key ? (
                              <Check className="w-3.5 h-3.5 text-emerald-500" />
                            ) : (
                              <Copy className="w-3.5 h-3.5" />
                            )}
                          </button>
                        </div>
                      ))}
                    </div>
                  </div>
                </div>

                <div className="mt-8 pt-4 border-t border-slate-200 dark:border-slate-800 flex items-center justify-between">
                  <span className="text-[11px] text-slate-400">
                    ID: {activeModalItem.id}
                  </span>
                  <button 
                    onClick={() => setActiveModalItem(null)}
                    className="px-4 py-2 bg-slate-900 dark:bg-slate-100 text-white dark:text-slate-900 text-xs font-semibold rounded-xl hover:bg-slate-800 dark:hover:bg-white transition-colors"
                  >
                    Concluir Inspeção
                  </button>
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

### 5.4 Física de Animação e Curvas de Transição

O UI Garage estabeleceu que em ferramentas de curadoria e bibliotecas de componentes, as animações nunca devem atrasar a escaneabilidade do catálogo:
- **Transição de Abas e Indicadores de Seleção**: Uso de molas críticas com amortecimento rigoroso (`type: 'spring'`, `stiffness: 450`, `damping: 32`), impedindo qualquer "bounce" elástico desconfortável ao alternar rapidamente entre abas de plataforma.
- **Elevação de Cards no Hover**: Duração ultracurta de 200ms com curva cúbica suave `cubic-bezier(0.16, 1, 0.3, 1)`, gerando percepção imediata de reatividade física sem cansar o olho do observador.
- **Abertura do Modal de Inspeção**: Entrada por escala de 0.95 para 1.0 acompanhada de desvanecimento de opacidade em 180ms, permitindo que a atenção do desenvolvedor se fixe imediatamente nos dados e tokens.

---

### 5.5 Estrutura de URLs & Como Agentes de IA Devem Pesquisar

Historicamente, o UI Garage organizava seu repositório através de uma árvore de URLs estritamente semântica e previsível, baseada no binômio **Plataforma + Categoria/Tag**:

```
┌────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                              TAXONOMIA DE URLS HISTÓRICAS DO UI GARAGE                                 │
├────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│  POR PLATAFORMA:                                                                                       │
│  • Web Desktop:                 https://uigarage.net/category/web/                                     │
│  • Mobile iOS:                  https://uigarage.net/category/ios/                                     │
│  • Mobile Android:              https://uigarage.net/category/android/                                 │
│  • Tablet / iPad:               https://uigarage.net/category/tablet/                                  │
├────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│  POR ÁTOMO DE UI / COMPONENTE:                                                                         │
│  • Menus & Navegação:           https://uigarage.net/tag/navigation/ & /tag/menus/                      │
│  • Barras Inferiores (Tab Bars):https://uigarage.net/tag/tab-bar/                                      │
│  • Modais & Diálogos:           https://uigarage.net/tag/modal/                                        │
│  • Estados Vazios:              https://uigarage.net/tag/empty-state/                                  │
│  • Tabelas de Preços:           https://uigarage.net/tag/pricing-table/                                │
│  • Telas de Autenticação:       https://uigarage.net/tag/login/ & /tag/sign-up/                        │
│  • Fluxos de Onboarding:        https://uigarage.net/tag/onboarding/                                   │
│  • Telas de Checkout & Carrinho:https://uigarage.net/tag/checkout/                                     │
├────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│  CONSULTA AO ACERVO VIA WAYBACK MACHINE:                                                               │
│  • https://web.archive.org/web/*/https://uigarage.net/                                                 │
│  SUCESSORES RECOMENDADOS PARA INGESTÃO ATIVA:                                                          │
│  • Mobbin (#114):               https://mobbin.com/ (Especialista em iOS, Android e Web Flows)         │
│  • Refero Design (#113):        https://refero.design/ (Aplicações Web reais & Refero MCP)             │
│  • SaaS Interface (#111):       https://saasinterface.com/ (UI de Telas e Componentes Pós-Login)      │
└────────────────────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir o documento de especificação arquitetural `DESIGN_BLUEPRINT.md` de um novo produto digital, incorpore as seguintes regras canônicas derivadas do legado do **UI Garage**:

1. **Classificação Atômica Obrigatória**:
   - Nunca especifique páginas sem listar os átomos que as compõem. Cada tela no blueprint deve conter uma lista exata de seus componentes reutilizáveis (ex: `HeaderNav`, `FilterDrawer`, `EmptyStateContainer`, `PrimaryActionButton`).
2. **Respeito às Restrições Físicas da Plataforma**:
   - Se o blueprint engloba Web e Mobile, mantenha tabelas de equivalência de componentes:
     - No Web Desktop: filtros em gaveta lateral ou popover suspenso com cursor de mouse.
     - No Mobile Nativo: filtros em Bottom Sheet arrastável com target mínimo de toque de 44x44px.
3. **Ergonomia dos Estados Vazios (Empty State Mandate)**:
   - Todo contêiner de dados dinâmicos (tabelas, feeds, listas, notificações) deve ter seu estado zero explicitado no blueprint, prevendo: (a) ícone temático, (b) copy curto elucidativo e (c) botão de ação direta para inserção do primeiro item.
4. **Hierarquia de Acentos (Regra 60-30-10)**:
   - Superfícies de suporte devem adotar cinzas neutros de ardósia (`Slate-50` / `Slate-900`) para que a cor de acento primária indique univocamente o elemento interativo principal de maior prioridade na tela.
5. **Adoção de Tokens de Espaçamento Padronizados**:
   - Proibir valores arbitrários de margem e padding (ex: `13px`, `27px`). Toda a geometria de layout deve aderir aos múltiplos de 4px e 8px do sistema modular canônico.
