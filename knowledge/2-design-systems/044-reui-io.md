---
id: "reui-io"
name: "ReUI"
url: "https://reui.io/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Enterprise SaaS Precision", "Dual-Primitive Architecture (Base UI & Radix UI)", "Tailwind CSS v4 Native", "TanStack v9 Data Densification", "AI Agent & MCP-First Design", "Copy-and-Own Registry"]
densidade_informacao: "Alta"
impacto_visual: "Utilitario/Base"
custo_computacional: "Medio (TanStack Virtual / dnd-kit / Shiki)"
stack_frameworks: ["React 19 / 18", "Next.js (App Router / RSC)", "Tailwind CSS v4", "Radix UI Primitives", "Base UI v1 Primitives", "TanStack Table v9", "TanStack Virtual v3", "dnd-kit", "Shiki", "nuqs", "React Hook Form", "Zod", "Lucide React"]
compatibilidade:
  fontes_ideais: ["Inter", "Geist Sans", "Plus Jakarta Sans", "JetBrains Mono", "IBM Plex Sans"]
  paletas_ideais: ["OKLCH Semantic Enterprise (Zinc / Slate + Deep Indigo / Emerald / Rose)", "Metronic Dark Tone (#09090b / #121215)", "High-Contrast Enterprise Light (#ffffff / #f4f4f5)"]
  combinacoes_recomendadas: ["Shadcn UI", "Magic UI", "Cult UI", "Motion Primitives", "Recharts", "Lucide Icons"]
  conflitos_esteticos: ["Brutalismo Y2K caótico desordenado", "Neumorfismo de plástico com sombras volumétricas difusas", "Interfaces B2C hiper-lúdicas com gradientes de arco-íris saturados sem alinhamento de grid"]
---

# ReUI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **ReUI** (`https://reui.io/`), concebido e desenvolvido pela equipe da **KeenThemes** (os engenheiros veteranos responsáveis pelo *Metronic*, o framework e template administrativo de maior sucesso comercial da história do desenvolvimento web com mais de 100.000 clientes corporativos ao longo de uma década), surge como uma resposta direta às limitações estruturais do ecossistema de componentes open-source contemporâneo. 

Embora o ecossistema Shadcn UI tenha padronizado primitivas acessíveis básicas (botões, modais, tooltips e campos de formulário simples), a construção de aplicações corporativas complexas (SaaS B2B, painéis de FinOps, consoles SRE/DevOps, ferramentas de gestão de pipelines e plataformas de IA) frequentemente colidia com uma barreira intransponível: a escassez de componentes de alta densidade de dados e complexidade algorítmica prontos para produção. O ReUI foi desenhado para fechar essa lacuna, operando como uma expansão corporativa de primeiro nível (*first-class registry*) sobre a arquitetura do Shadcn UI, React 19 e Tailwind CSS v4.

```
┌───────────────────────────────────────────────────────────────────────────┐
│                           CAMADA DE APLICAÇÃO SAAS                        │
├───────────────────────────────────────────────────────────────────────────┤
│    ReUI Pro Blocks (669 blocos de CRM, DevOps, AI Ops, Billing, Gantt)     │
├───────────────────────────────────────────────────────────────────────────┤
│    ReUI Primitives (27 componentes avançados: Data Grid v9, Kanban, etc.) │
├─────────────────────────────────────┬─────────────────────────────────────┤
│         Radix UI Primitives         │          Base UI Primitives         │
│          (Estilo: Lyra)             │            (Estilo: Nova)           │
├─────────────────────────────────────┴─────────────────────────────────────┤
│         Tailwind CSS v4 (Design Tokens Semânticos OKLCH Estendidos)       │
└───────────────────────────────────────────────────────────────────────────┘
```

### Os Pilares Diferenciais da Assinatura ReUI

1. **A Filosofia de "Propriedade Integral do Código" (Copy-and-Own Registry)**:
   Assim como no Shadcn UI fundamental, o ReUI não exige a instalação de pacotes monolíticos opacos do NPM (`npm install reui` não existe). Todo o sistema é distribuído através de um namespace de registro remoto no CLI oficial do Shadcn (`@reui/<component>`). Ao executar `npx shadcn@latest add @reui/data-grid`, o código-fonte puro em TypeScript e Tailwind CSS v4 é baixado diretamente para o diretório de componentes do projeto (`components/reui/`), outorgando aos arquitetos e desenvolvedores governança completa sobre a implementação, sem dependências encapsuladas ou risco de breaking changes externas.

2. **O Pioneirismo Dual-Primitive (Suporte Simétrico a Radix UI e Base UI)**:
   O ReUI é o primeiro grande ecossistema da web moderna a implementar neutralidade de primitivas headless. Cada um de seus 27 componentes customizados e 1.264 exemplos gratuitos é arquitetado com variantes duplas:
   - **Base UI v1** (a biblioteca headless de última geração da equipe do MUI): utilizado nos temas da família *Nova* (`base-nova`), priorizando flexibilidade de marcação semântica e suporte moderno ao React 19.
   - **Radix UI Primitives**: utilizado nos temas da família *Lyra* (`radix-lyra`), mantendo total retrocompatibilidade e familiaridade com a base de código clássica do ecossistema Shadcn.

3. **Engenharia de Dados Pesada: Adoção do TanStack Table v9 & Virtual v3**:
   A grande maioria das bibliotecas de UI oferece componentes de tabela meramente cosméticos, incapazes de lidar com ordenação multisessão, redimensionamento com drag-and-drop, fixação de colunas (*column pinning*), linhas em árvore hierárquica (*tree rows*), virtualização de linhas/colunas para centenas de milhares de registros, e seleção de células bidimensional com atalhos de área de transferência (estilo Google Sheets / Microsoft Excel). O ReUI construiu a implementação de referência do **TanStack Table v9** para Tailwind CSS v4, consolidando todas as features em um bundle unificado (`dataGridFeatures`).

4. **Extensão de Tokens Semânticos Enterprise**:
   O ReUI estende a taxonomia clássica de temas do Shadcn com estados semânticos essenciais para painéis corporativos, evitando gambiarras de classes pontuais:
   - `--destructive` / `--destructive-foreground`: Ações destrutivas e alertas de erro crítico.
   - `--info` / `--info-foreground`: Avisos contextuais e orientações de fluxo.
   - `--success` / `--success-foreground`: Sucessos operacionais, confirmações de build e validações.
   - `--warning` / `--warning-foreground`: Atenção a limites de cota, faturamento pendente e alertas preventivos.
   - `--invert` / `--invert-foreground`: Contrastes de alta visibilidade e inversão contextual de superfícies.

5. **MCP-First Architecture (Projetado para Coding Agents e LLMs)**:
   O ReUI é pioneiro na disponibilização de um **Hosted MCP Server** (`https://mcp.reui.io`) e arquivos estruturados `llms.txt` / `llms-full.txt`. Esse endpoint de Streamable HTTP expõe 19 ferramentas para assistentes de IA (como Claude Code, Cursor, Antigravity, Gemini CLI e v0), permitindo busca semântica ponderada de componentes, inspeção de contratos de tipagem em tempo real e instalação precisa de componentes sem qualquer alucinação de props inexistentes.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados

1. **Backoffices Corporativos, ERPs, CRMs & FinOps de Alta Complexidade**:
   Aplicações onde usuários operam 8 horas por dia visualizando e editando fluxos de dados massivos. A presença de recursos como tabelas com redimensionamento de colunas, agrupamento de cabeçalhos, totais contábeis no rodapé (*footer totals*) e edição in-line de células elimina a necessidade de integrar ferramentas proprietárias pesadas como AG-Grid ou Handsontable.

2. **Plataformas de Observabilidade, AI Ops, SRE & Infraestrutura Cloud**:
   Painéis no padrão Datadog, Grafana, Cloudflare ou AWS Console, que demandam rastreamento de traces de agentes de IA (`Trace`), gráficos com barras de status por deploy (`status-tracker`), timelines de auditoria (`Timeline`), e consoles de terminal com realce de sintaxe Shiki e suporte a streaming de tokens (`Code Block`).

3. **Ferramentas de Gestão de Projetos, Engenharia & Automação**:
   Workflows que dependem de kanbans drag-and-drop (`Kanban`), cronogramas visuais em diagramas Gantt com expansão temporal (`Gantt`), e construtores visuais de automação sobre nós interativos com React Flow.

4. **SaaS B2B Multi-Etapas com Wizards de Configuração Complexos**:
   Fluxos de onboarding e configuração com múltiplos passos condicionais, integrando o `Stepper` com `react-hook-form` e `zod` para validação progressiva por estágio.

### Papel no Ritmo Visual (A Regra 60-30-10)

```
┌────────────────────────────────────────────────────────────────────────┐
│                        RITMO VISUAL DO SISTEMA                         │
├────────────────────────────────────────────────────────────────────────┤
│ 60% ESPINHA DORSAL OPERACIONAL:                                        │
│     - App Shells, Sidebars, Data Grids, Forms, Badges, Headers         │
│     - Superfícies cinza neutro (Zinc/Slate), bordas de 1px hairline     │
├────────────────────────────────────────────────────────────────────────┤
│ 30% CAMADA DE ORQUESTRAÇÃO E NAVEGAÇÃO:                                │
│     - Steppers, DropdownMenus, Sheets laterais, Abas, Trees            │
│     - Transições de estado com foco acessível e badges dinâmicos       │
├────────────────────────────────────────────────────────────────────────┤
│ 10% SHOWSTOPPERS FUNCIONAIS ("Crafted Utilities"):                     │
│     - Planilha com fill-handle & seleção retangular (Excel style)      │
│     - Timeline do Gantt com zoom contínuo por roda do mouse            │
│     - Board Kanban com drag interativo e sombras elevadas sob cursor   │
└────────────────────────────────────────────────────────────────────────┘
```

- **60% — Espinha Dorsal Funcional e Alta Densidade de Dados**:
  O ReUI assume com autoridade máxima o papel de estrutura base. Toda a malha de tabelas, formulários, grids de métricas, cards analíticos e sidebars operacionais bebe da sua tipografia rigorosa, espaçamentos compactos (`dense layout`) e paleta monocromática com tokens semânticos funcionais.
- **30% — Camada de Navegação, Orquestração e Micro-interações**:
  Os componentes de fluxo — como o `Stepper` que guia cadastros complexos, a `Tree` que organiza hierarquias organizacionais, os `Filters` estruturados em popovers modais e os painéis retráteis `Sheet` para inspeção de registros — regem o percurso do usuário sem fricção visual.
- **10% — Efeitos de Destaque / Showstoppers ("Crafted Utility")**:
  Diferente de bibliotecas focadas em marketing com efeitos pirotécnicos 3D, no ReUI o "Showstopper" é puramente **funcional e tátil**: o impacto visual reside na fluidez de uma célula de tabela sendo arrastada para preencher valores adjacentes (*fill-handle*), no timeline responsivo de um Gantt que transiciona de dias para meses com animação contínua, ou em uma assinatura eletrônica capturada com física de tinta baseada na pressão do cursor (`Signature Pad`).

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

1. **Landing Pages Puramente Editoriais / Portfólios Artísticos de Moda & Luxo**:
   O ReUI foi lapidado para densidade de informação e arquitetura corporativa. Utilizá-lo em websites que demandam layouts fluidos assimétricos, grandes blocos tipográficos decorativos com sobreposição e estética brutalista de vanguarda gera uma sensação estéril e desproporcional.
2. **Websites Imersivos 3D WebGL / Canvas Protagonistas**:
   Projetos fundamentados em shaders WebGL contínuos, Three.js e narrativas cinematográficas não têm utilidade para formulários densos, seletores de país e tabelas paginadas.
3. **Micro-Páginas com Tabelas Estáticas Triviais**:
   Se a aplicação precisa exibir apenas uma lista estática de 4 a 6 linhas sem paginação, ordenação ou filtros, importar o ReUI Data Grid é uma má prática de engenharia. Deve-se empregar a primitiva HTML básica ou o componente `Table` leve do Shadcn puro para não inflar o bundle JS com a máquina de estados do TanStack Table v9.
4. **Projetos Mobile-Only Nativos de Paradigma Rígido (iOS Human Interface / Material You Puro)**:
   Embora os blocos sejam totalmente responsivos, a densidade visual e os controles (como resizers de coluna e multi-seleção de células) são prioritariamente concebidos para telas de trabalho desktop e híbridas.

### ⚠️ Anti-padrões e Erros Comuns de Implementação:

- **Anti-padrão 1: Omissão de `getRowId` em Data Grids Reordenáveis ou Virtualizados**:
  Ao implementar ordenação via arrasto (`drag-and-drop`), fixação de linhas (`row pinning`) ou virtualização (`TanStack Virtual`), deixar de fornecer uma chave estável via `getRowId: (row) => row.id` causa instabilidade visual catastrófica e perda de foco do DOM.
- **Anti-padrão 2: Paginação no Cliente sobre Grandes Volumes de Dados**:
  Usar o exemplo padrão de paginação cliente (`c-data-grid-1`) para datasets que ultrapassam mil registros resulta em gargalos de memória no navegador. Nesses cenários, deve-se adotar compulsoriamente a receita de paginação de servidor (`c-data-grid-34`) ou o virtualizador de rolagem infinita (`c-data-grid-28`).
- **Anti-padrão 3: Esquecimento do Token `REUI_LICENSE_KEY` em Pipelines de CI/CD**:
  Ao utilizar os Pro Blocks ou Pro Icons em ambientes automatizados (GitHub Actions, Vercel, Docker), a ausência da variável de ambiente `REUI_LICENSE_KEY` fará com que o CLI do Shadcn falhe no handshake de autorização do endpoint protegido `@reui`.
- **Anti-padrão 4: Poluição de Estados com Múltiplos Filtros Sem Sincronização de URL**:
  Implementar o componente `Filters` complexo em dashboards sem atrelar seu estado aos search params da URL (via `nuqs`) impede o compartilhamento direto de visões de dados e quebra o histórico de navegação do browser (`Back/Forward`).

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

O ReUI disponibiliza **27 primitivas customizadas** ausentes no Shadcn padrão, além de **1.264 exemplos gratuitos** e **669 blocos de aplicação**. Abaixo estão detalhados os 12 componentes mais emblemáticos para a engenharia de software contemporânea:

```
┌────────────────────────────────────────────────────────────────────────┐
│                   CATÁLOGO DE COMPONENTES REUI                         │
├────────────────────────────────────────────────────────────────────────┤
│ 01. Data Grid v9       │ TanStack v9, Virtual v3, Excel Cell Edit, Pin │
│ 02. Kanban Board       │ dnd-kit core, Sortable, Multi-column, Drawer  │
│ 03. Stepper Wizard     │ Etapas progressivas, React Hook Form + Zod    │
│ 04. Gantt Chart        │ Tree + Timeline split, Zoom contínuo, Rollups │
│ 05. Tree View          │ Diretórios hierárquicos, seleção contextual   │
│ 06. Stepped Filters    │ Construtor de queries booleanas (AND/OR)      │
│ 07. Code Block (Shiki) │ Syntax highlight, streaming token, diff mode  │
│ 08. AI Trace & Marker  │ Visualizador de reasoning traces & tool calls │
│ 09. Color Picker OKLCH │ Matiz, saturação, alpha, eyedropper, OKLCH    │
│ 10. Event Calendar     │ Mês/Semana/Dia/Agenda, drag-and-drop eventos  │
│ 11. Signature Pad      │ Tinta dinâmica por pressão/velocidade, SVG    │
│ 12. File Upload / Type │ Drag-and-drop zone, previews, 50+ mime types  │
└────────────────────────────────────────────────────────────────────────┘
```

### 1. Shadcn Data Grid (TanStack Table v9 + TanStack Virtual v3)
- **Anatomia Visual**:
  Uma superfície tabular de nível desktop composta por `DataGrid`, `DataGridTable` (ou `DataGridTableVirtual`), `DataGridColumnHeader`, `DataGridTableRowSelect`, `DataGridTableRowPin`, e `DataGridTableFoot`. Apresenta bordas finas de separação (`border-border`), linhas zebradas opcionais (`striped rows`), cabeçalhos fixos com sombra de elevação ao rolar (`sticky header`), e marcadores visuais de fixação lateral (*pinned columns*). Na variante com seleção estilo planilha, as células ativas exibem contorno azul contínuo de 2px com uma alça quadrada de preenchimento (*fill handle*) no vértice inferior direito.
- **Gatilho de Interação**:
  - **Click com Shift / Ctrl**: Seleção contínua retangular de células.
  - **Drag no Header**: Redimensionamento de largura de coluna ou reordenação lateral da ordem das colunas.
  - **Double Click na Célula**: Abre input in-line para edição direta com commit via `Enter` ou descarte via `Esc`.
  - **Atalhos de Teclado**: `Cmd+C` / `Cmd+V` para cópia e colagem com suporte à área de transferência do sistema operacional.
- **Onde Encaixar**: Telas centrais de CRM, backoffices contábeis, inventários de produtos, consoles de monitoramento de instâncias de nuvem.

### 2. Shadcn Kanban (`@dnd-kit/core` & `@dnd-kit/sortable`)
- **Anatomia Visual**:
  Estrutura em colunas verticais com cabeçalho contendo identificador de status, badge com contagem de itens e botão de adição rápida. Os cards internos possuem cantos arredondados padronizados (`rounded-lg`), tags coloridas semânticas, avatares empilhados dos responsáveis e indicador de prioridade. Durante o arrasto, o card ativo é renderizado através de um `DragOverlay` com leve rotação (+2 graus), elevação com sombra suave (`shadow-lg`) e opacidade atenuada no slot de origem.
- **Gatilho de Interação**:
  - **Drag-and-Drop**: Detecção de colisão via algoritmo `closestCorners` do `@dnd-kit`, permitindo transição contínua tanto entre posições na mesma coluna quanto transferência entre colunas distintas.
  - **Click**: Dispara abertura de drawer ou modal com o formulário de detalhes da tarefa.
- **Onde Encaixar**: Gestão de sprints de desenvolvimento, pipelines de prospecção comercial (funil de vendas), fluxo de atendimento de tickets.

### 3. Shadcn Stepper (Multi-step Process & Wizard)
- **Anatomia Visual**:
  Barra progressiva horizontal ou vertical. Cada etapa é representada por um círculo indicador com numeração ou ícone (completado exibe checkmark `CheckIcon`, em progresso exibe anel de foco destacado com pulso suave, pendente exibe borda pontilhada cinza). Linhas conectoras entre etapas transicionam de cor (`bg-muted` para `bg-primary`) conforme o avanço.
- **Gatilho de Interação**:
  - **Navegação Controlada**: Clique liberado apenas em etapas já validadas ou navegação estrita através de botões "Avançar" / "Voltar". Integrado ao `formState.isValid` do React Hook Form.
- **Onde Encaixar**: Fluxos de onboarding de novas contas, assistentes de provisionamento de infraestrutura, checkout de comércio eletrônico, formulários de compliance e KYC.

### 4. Shadcn Gantt Chart (Split Tree & Timeline Pane)
- **Anatomia Visual**:
  Painel bipartido dividido por divisor redimensionável. O painel esquerdo apresenta a árvore de tarefas hierárquica (WBS) com nomes, responsáveis e status. O painel direito apresenta a grade temporal contínua com barras horizontais coloridas de tarefas, marcos (*milestones*) em formato de diamante e linhas indicadoras da data atual ("Hoje").
- **Gatilho de Interação**:
  - **Drag Lateral**: Move datas de início e fim preservando a duração total da tarefa.
  - **Resize nas Extremidades**: Arrasto das bordas da barra para estender ou encurtar prazos.
  - **Zoom**: Botões segmentados ou roda do mouse com `Ctrl` alternando a escala de visualização entre Dias, Semanas, Meses e Anos.
- **Onde Encaixar**: Roteiros de engenharia de software (*roadmaps*), planejamento de obras civis, gestão de lançamentos corporativos.

### 5. Shadcn Tree View
- **Anatomia Visual**:
  Visualizador em árvore com indentação visual matemática precisa (`pl-4`). Nós pais contam com ícones chevron de rotação animada (0° a 90° via `transition-transform`) e ícones de pasta; nós folhas exibem o ícone do tipo de arquivo específico (`FileType`). Suporta linhas guia verticais sutis conectando nós irmãos.
- **Gatilho de Interação**:
  - **Click no Chevron / Duplo Clique no Rótulo**: Expande ou colapsa o nó.
  - **Click Simples**: Seleciona o item ativo, disparando carregamento preguiçoso (*lazy-loading*) do conteúdo no painel principal adjacente.
  - **Navegação por Teclado**: Setas `Up/Down` para navegar entre linhas, seta `Right` para abrir pasta e seta `Left` para recolher.
- **Onde Encaixar**: Exploradores de arquivos em nuvem (estilo Google Drive/Dropbox), estruturas de permissões por departamentos, navegação em documentações técnicas.

### 6. Shadcn Stepped Filters & Query Builder
- **Anatomia Visual**:
  Barra compacta de filtros compostos que combina um campo de pesquisa textual com botões de adição de critérios. Ao clicar, projeta um popover contendo seleção em cascata: *Atributo* (ex: "Status") ➔ *Operador* (ex: "é qualquer um de") ➔ *Valores* (checkboxes com contadores). Ao confirmar, gera uma "pílula de filtro" com badge visual e botão de descarte (`X`).
- **Gatilho de Interação**:
  - **Popover Trigger**: Abertura dinâmica sem recarregar a tela.
  - **URL Synchronization**: Atualização instantânea dos query parameters da URL via `nuqs`, garantindo que filtros possam ser favoritados ou compartilhados por link direto.
- **Onde Encaixar**: Topbars de Data Grids em CRMs, logs de auditoria de segurança, catálogo de produtos em e-commerces B2B.

### 7. Shadcn Code Block (Shiki + Streaming + Diff)
- **Anatomia Visual**:
  Container com cabeçalho contendo o nome do arquivo, indicador da linguagem de programação, botão de alternância de quebra de linha (*wrap*), e botão de cópia com feedback de confirmação. O corpo utiliza renderização com temas Shiki no servidor ou cliente, suporte a numeração de linhas, destaque de linhas modificadas (+ em verde, - em vermelho no modo Diff), e cursor piscante dinâmico em modo de streaming de IA.
- **Gatilho de Interação**:
  - **Click no Botão de Cópia**: Transfere o código puro sem marcadores de linha para o clipboard do sistema.
  - **Code Folding**: Clique em chevrons laterais para colapsar blocos de funções ou JSONs extensos.
- **Onde Encaixar**: Respostas de chats conversacionais de IA, documentações interativas de APIs, visualizadores de Pull Requests e revisões de código.

### 8. Shadcn AI Trace & Marker
- **Anatomia Visual**:
  Componente desenhado especificamente para visualização de execuções de Agentes Autônomos e LLMOps. Exibe uma linha vertical cronológica com marcadores temáticos: *Pensamento/Raciocínio* (ícone de cérebro/lâmpada com texto colapsável), *Chamada de Ferramenta / Tool Call* (badge monospace com nome da função e parâmetros em JSON), e *Execução/Saída* (status de sucesso ou falha com métrica de latência em milissegundos e contagem de tokens).
- **Gatilho de Interação**:
  - **Collapsible Toggle**: Clique no cabeçalho do passo para inspecionar os argumentos brutos enviados para o modelo e o retorno cru da ferramenta.
- **Onde Encaixar**: Telas de monitoramento de agentes (estilo LangSmith / Langfuse), consoles de depuração de automações corporativas.

### 9. Shadcn Color Picker (OKLCH, HEX, RGB, HSL)
- **Anatomia Visual**:
  Painel completo de engenharia de cores contendo matriz bidimensional de saturação/brilho com cursor circular arrastável, sliders cilíndricos para matiz (*hue*) e canal alfa/opacidade, seletor de paleta predefinida (*swatches*) e campos numéricos de entrada com suporte ao espaço moderno OKLCH. Acompanha botão conta-gotas (*EyeDropper API*).
- **Gatilho de Interação**:
  - **Drag no Canvas / Sliders**: Atualização em tempo real das variáveis CSS sem degradação de FPS.
  - **Click no Conta-Gotas**: Ativa o cursor do sistema para captura de cor de qualquer pixel da tela do usuário.
- **Onde Encaixar**: Configurações de personalização visual (*white-label*), editores de temas, customização de categorias e etiquetas.

### 10. Shadcn Event Calendar (Headless-First)
- **Anatomia Visual**:
  Grade de calendário expansível com cabeçalho de navegação temporal e alternador de modos: Mês, Semana, Dia, N-Dias e Agenda. Eventos são representados por blocos coloridos com tipografia truncada, horário de início/término e indicador de status. Em telas de alta resolução, suporta colunas divididas por participante da equipe.
- **Gatilho de Interação**:
  - **Drag-and-Drop de Evento**: Arrasto de blocos de compromissos entre dias ou faixas de horário com recálculo automático de horários.
  - **Click and Drag na Grade Vazia**: Criação intuitiva de um novo compromisso delimitando o intervalo visualmente.
- **Onde Encaixar**: Agendamento de consultas médicas, reservas de salas corporativas, agendamento de reuniões comerciais.

### 11. Shadcn Signature Pad
- **Anatomia Visual**:
  Quadro retangular emoldurado com linha de guia horizontal sutil e indicador textual "Assine aqui". Ao iniciar a assinatura, exibe traço vetorial de tinta fluida com espessura dinâmica baseada na velocidade do cursor ou pressão da caneta/stylus. Barra de ferramentas inferior com botões "Limpar", "Desfazer (Undo)" e "Confirmar".
- **Gatilho de Interação**:
  - **Pointer Events**: Captura universal para mouse, trackpad e telas touch com caneta sensível à pressão.
  - **Exportação**: Gera strings em Base64 ou payloads vetoriais em formato SVG diretamente para o formulário.
- **Onde Encaixar**: Assinatura de contratos digitais, ordens de serviço em campo, termos de consentimento e logística de entrega.

### 12. Shadcn File Upload & File Type
- **Anatomia Visual**:
  Área retangular com bordas pontilhadas (`border-dashed`), ícone de nuvem ou upload em destaque e textos explicativos informando tipos aceitos e peso máximo por arquivo. Ao receber itens, transiciona para uma lista de cartões com o componente `FileType` (ícone temático reconhecendo formatos como PDF, DOCX, ZIP, MP4, XLSX), nome, peso legível, barra de progresso individual e botão de exclusão.
- **Gatilho de Interação**:
  - **Drag-and-Drop Global**: Área sensível com overlay destacado ao passar arquivos arrastados do sistema operacional.
  - **File Browser Trigger**: Clique em qualquer ponto da área para abrir a janela de seleção nativa do sistema.
- **Onde Encaixar**: Anexação de documentos em chamados de suporte, upload de faturas em gateways de pagamento, cadastro de catálogos de produtos.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup Estrutural

O ReUI integra-se nativamente a um projeto baseado em **Next.js (App Router)** ou **Vite + React 19** com **Tailwind CSS v4**.

#### 1. Configuração do Registry em `components.json`:
Adicione o namespace `@reui` no seu arquivo `components.json`. Caso utilize componentes pagos (Pro Blocks/Icons), inclua o cabeçalho de autorização lendo a variável de ambiente:

```json
{
  "$schema": "https://ui.shadcn.com/schema.json",
  "style": "base-nova",
  "rsc": true,
  "tsx": true,
  "tailwind": {
    "config": "",
    "css": "app/globals.css",
    "baseColor": "zinc",
    "cssVariables": true
  },
  "aliases": {
    "components": "@/components",
    "utils": "@/lib/utils",
    "ui": "@/components/ui",
    "lib": "@/lib",
    "hooks": "@/hooks"
  },
  "registries": {
    "@reui": {
      "url": "https://reui.io/r/{style}/{name}.json",
      "headers": {
        "Authorization": "Bearer ${REUI_LICENSE_KEY}"
      }
    }
  }
}
```

#### 2. Instalação de Primitivas e Componentes via CLI:
```bash
# Instalação da primitiva fundamental de Data Grid com TanStack Table v9
npx shadcn@latest add @reui/data-grid

# Instalação do Kanban Board drag-and-drop
npx shadcn@latest add @reui/kanban

# Instalação do Stepper progressivo
npx shadcn@latest add @reui/stepper

# Instalação de blocos prontos de aplicação (requer autenticação Pro)
npx shadcn@latest add @reui/c-data-grid-22
```

---

### Física de Movimento, Transições e Curvas

O design do ReUI prioriza o tempo de resposta corporativo e a ausência de oscilação visual que possa distrair o operador:

1. **Micro-interações de Hover e Focus**:
   - `transition-colors duration-150 ease-out`: Usado universalmente em botões, linhas de tabela e menus suspensos para sensação instantânea de clique.
2. **Física de Drag-and-Drop (`dnd-kit`)**:
   - No Kanban e nas colunas reordenáveis do Data Grid, o elemento ativo recebe escala sutil (`scale(1.02)`) com elevação suave (`shadow-xl`) e amortecimento de retorno sem bounce elástico exagerado.
3. **Painéis Laterais (`Sheet` e `Drawer`)**:
   - Física de mola controlada via CSS ou Framer Motion: `stiffness: 350`, `damping: 32`, `mass: 0.8`. O drawer desliza rapidamente para o ponto de parada e desacelera firmemente, sem rebotes que atrasem a leitura do conteúdo.

---

### Receita de Código Funcional: Data Grid Corporativo com TanStack Table v9

O exemplo abaixo demonstra a anatomia de implementação real de um **ReUI Data Grid** integrado com o bundle unificado `dataGridFeatures`, colunas customizadas, badges semânticos e paginação integrada:

```tsx
"use client"

import * as React from "react"
import {
  useTable,
  getCoreRowModel,
  getPaginationRowModel,
  getSortedRowModel,
  type ColumnDef,
  type SortingState,
  type PaginationState,
} from "@tanstack/react-table"
import { ArrowUpDown, MoreHorizontal, ShieldCheck, ShieldAlert } from "lucide-react"

// Importações do módulo instalado via @reui/data-grid
import {
  DataGrid,
  DataGridTable,
  dataGridFeatures,
  type DataGridFeatures,
} from "@/components/reui/data-grid/data-grid"
import { DataGridPagination } from "@/components/reui/data-grid/data-grid-pagination"
import { Button } from "@/components/ui/button"
import { Badge } from "@/components/ui/badge"
import {
  DropdownMenu,
  DropdownMenuContent,
  DropdownMenuItem,
  DropdownMenuLabel,
  DropdownMenuTrigger,
} from "@/components/ui/dropdown-menu"

// Contrato de dados corporativo
export interface SystemUser {
  id: string
  name: string
  email: string
  role: "Admin" | "Operator" | "Auditor"
  status: "Active" | "Suspended" | "Pending"
  lastLogin: string
}

const mockUsers: SystemUser[] = [
  {
    id: "usr_01",
    name: "Helena Rostova",
    email: "h.rostova@enterprise.internal",
    role: "Admin",
    status: "Active",
    lastLogin: "2026-10-26 14:15",
  },
  {
    id: "usr_02",
    name: "Marcus Vance",
    email: "m.vance@enterprise.internal",
    role: "Operator",
    status: "Pending",
    lastLogin: "2026-10-25 09:30",
  },
  {
    id: "usr_03",
    name: "Sora Takahashi",
    email: "s.takahashi@enterprise.internal",
    role: "Auditor",
    status: "Suspended",
    lastLogin: "2026-10-20 18:44",
  },
]

export function EnterpriseUserDataGrid() {
  const [data] = React.useState<SystemUser[]>(mockUsers)
  const [sorting, setSorting] = React.useState<SortingState>([])
  const [pagination, setPagination] = React.useState<PaginationState>({
    pageIndex: 0,
    pageSize: 10,
  })

  // Definição de colunas tipada com DataGridFeatures do TanStack Table v9
  const columns = React.useMemo<ColumnDef<DataGridFeatures, SystemUser>[]>(
    () => [
      {
        accessorKey: "name",
        header: ({ column }) => (
          <Button
            variant="ghost"
            size="sm"
            className="-ml-3 h-8 data-[state=open]:bg-accent"
            onClick={() => column.toggleSorting(column.getIsSorted() === "asc")}
          >
            <span>Nome do Operador</span>
            <ArrowUpDown className="ml-2 h-3.5 w-3.5 text-muted-foreground" />
          </Button>
        ),
        cell: ({ row }) => (
          <div className="flex flex-col py-1">
            <span className="font-medium text-foreground text-sm">
              {row.original.name}
            </span>
            <span className="text-xs text-muted-foreground">
              {row.original.email}
            </span>
          </div>
        ),
      },
      {
        accessorKey: "role",
        header: "Função / Acesso",
        cell: ({ row }) => (
          <span className="text-xs font-mono text-muted-foreground">
            {row.original.role}
          </span>
        ),
      },
      {
        accessorKey: "status",
        header: "Estado Operacional",
        cell: ({ row }) => {
          const status = row.original.status
          return (
            <Badge
              variant="outline"
              className={
                status === "Active"
                  ? "border-emerald-500/20 bg-emerald-500/10 text-emerald-600 dark:text-emerald-400"
                  : status === "Pending"
                  ? "border-amber-500/20 bg-amber-500/10 text-amber-600 dark:text-amber-400"
                  : "border-rose-500/20 bg-rose-500/10 text-rose-600 dark:text-rose-400"
              }
            >
              {status === "Active" && <ShieldCheck className="mr-1 h-3 w-3" />}
              {status === "Suspended" && <ShieldAlert className="mr-1 h-3 w-3" />}
              {status}
            </Badge>
          )
        },
      },
      {
        accessorKey: "lastLogin",
        header: "Última Atividade",
        cell: ({ row }) => (
          <span className="text-xs text-muted-foreground">
            {row.original.lastLogin}
          </span>
        ),
      },
      {
        id: "actions",
        enableHiding: false,
        cell: ({ row }) => (
          <div className="flex justify-end">
            <DropdownMenu>
              <DropdownMenuTrigger asChild>
                <Button variant="ghost" className="h-8 w-8 p-0">
                  <span className="sr-only">Abrir menu</span>
                  <MoreHorizontal className="h-4 w-4" />
                </Button>
              </DropdownMenuTrigger>
              <DropdownMenuContent align="end">
                <DropdownMenuLabel>Ações</DropdownMenuLabel>
                <DropdownMenuItem
                  onClick={() => navigator.clipboard.writeText(row.original.id)}
                >
                  Copiar Identificador (ID)
                </DropdownMenuItem>
                <DropdownMenuItem>Ver Auditoria de Logs</DropdownMenuItem>
                <DropdownMenuItem className="text-destructive focus:bg-destructive/10">
                  Revogar Credenciais
                </DropdownMenuItem>
              </DropdownMenuContent>
            </DropdownMenu>
          </div>
        ),
      },
    ],
    []
  )

  // Instanciação da tabela via TanStack v9 useTable consumindo dataGridFeatures
  const table = useTable({
    features: dataGridFeatures,
    data,
    columns,
    state: {
      sorting,
      pagination,
    },
    onSortingChange: setSorting,
    onPaginationChange: setPagination,
    getCoreRowModel: getCoreRowModel(),
    getPaginationRowModel: getPaginationRowModel(),
    getSortedRowModel: getSortedRowModel(),
    getRowId: (row) => row.id,
  })

  return (
    <div className="flex flex-col gap-3 rounded-lg border border-border bg-card p-4 shadow-sm">
      <div className="flex items-center justify-between pb-2">
        <div>
          <h3 className="text-base font-semibold text-foreground">
            Gestão de Contas Corporativas
          </h3>
          <p className="text-xs text-muted-foreground">
            Controle de identidades ativas e permissões de acesso ao sistema.
          </p>
        </div>
      </div>

      {/* Renderizador principal do ReUI Data Grid */}
      <DataGrid table={table}>
        <div className="rounded-md border border-border overflow-hidden">
          <DataGridTable />
        </div>
        <div className="pt-2">
          <DataGridPagination />
        </div>
      </DataGrid>
    </div>
  )
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar o **ReUI** como ecossistema ou referência técnica de um projeto no documento de especificação (`DESIGN_BLUEPRINT.md`), a Inteligência Artificial deve registrar estritamente as diretrizes abaixo:

1. **Declaração Formal da Camada no `DESIGN_BLUEPRINT.md`**:
   - `Architecture Backbone`: Declarar o ReUI como o registry corporativo sobre o Shadcn UI.
   - `Primitive Standard`: Definir explicitamente entre `Base UI (base-nova)` ou `Radix UI (radix-lyra)`. Projetos que adotam React 19 nativo e buscam menor custo de bundling devem optar por `base-nova`; projetos já consolidados em Radix devem manter `radix-lyra`.
2. **Definição dos Tokens de Estado Enterprise**:
   - Garantir que as variáveis semânticas estendidas (`--info`, `--success`, `--warning`, `--invert`) estejam mapeadas no arquivo `globals.css` no formato `oklch(...)`.
3. **Regra de Virtualização vs. Paginação**:
   - Registrar no blueprint: *"Para listagens que superem 500 registros simultâneos em tela ou feeds analíticos contínuos, é obrigatório o uso de `DataGridTableVirtual` em conjunto com `@tanstack/react-virtual`, fornecendo `getRowId` estável. Para listagens padrão de backoffice, adotar `DataGridPagination` com tamanho padrão de 10 a 25 linhas por página"*.
4. **Governança de Automação de Agentes (MCP Integration)**:
   - Instruir o pipeline do projeto a conectar o MCP Server `https://mcp.reui.io` nas ferramentas de desenvolvimento (Cursor, Claude Code, Antigravity) para permitir a injeção automatizada de novos blocos e validação prévia de tipagens antes de gerar código no repositório.
5. **Divisão Visual 60-30-10**:
   - 60%: Superfícies neutras do ReUI (`Card`, `DataGrid`, `Forms`, `Badges`).
   - 30%: Componentes de orquestração (`Stepper`, `Tree`, `Kanban`, `Sheet`).
   - 10%: Interações refinadas de manipulação de dados (seleção retangular de células de planilha, zoom de Gantt e física de drag-and-drop).
