---
id: "tremor-so"
name: "Tremor / Tremor Raw"
url: "https://www.tremor.so/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Modern Data-Dense Analytics", "Vercel / Stripe Metric Rigor", "Tailwind Native Theming", "Recharts Headless Architecture", "Radix Accessible Controls"]
densidade_informacao: "Alta"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS/Headless) a Medio (Recharts SVG/JS)"
stack_frameworks: ["React 19 / 18", "Next.js (App Router & RSC)", "Tailwind CSS v3 / v4", "Recharts", "Radix UI Primitives", "TypeScript", "@remixicon/react", "clsx", "tailwind-merge"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "JetBrains Mono", "Plus Jakarta Sans", "Fira Code", "IBM Plex Sans"]
  paletas_ideais: ["Zinc & Slate Enterprise Dark", "Emerald & Cyan Telemetry", "Deep Blue / Indigo SaaS", "Amber & Rose Alert Systems", "Monochrome Tabular Minimal"]
  combinacoes_recomendadas: ["Shadcn UI", "TanStack Table", "Radix UI", "Lucide React", "Magic UI", "Sonner"]
  conflitos_esteticos: ["Neumorfismo skeuomórfico", "Brutalismo Y2K desordenado", "Gradientes psicodélicos saturados sem legibilidade de dados", "Fontes display decorativas em eixos numéricos"]
---

# Tremor / Tremor Raw — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Tremor** (`tremor.so`) é o padrão de referência moderno na indústria global de software para a criação de dashboards executivos, interfaces analíticas e sistemas de telemetria de alta densidade informativa. Concebido e fundado pelos engenheiros **Severin Landolt** e **Christopher Kindl** (Tremor Labs), o projeto foi desenvolvido com uma tese central: preencher a lacuna crítica que existia entre bibliotecas de componentes de interface genéricas (como Shadcn UI, Radix e Tailwind UI) e as ferramentas de visualização de dados puras (como Recharts, D3 e Chart.js).

### A Evolução: Do `@tremor/react` Monolítico ao Tremor Raw

Originalmente lançado como o pacote de NPM `@tremor/react`, o ecossistema fornecia componentes pré-empacotados e altamente opinativos. Embora a adoção tenha sido imediata entre desenvolvedores Next.js e Tailwind, o modelo enfrentou os mesmos gargalos históricos dos pacotes fechados: dificuldade de customizar nós internos de SVG, dependência de versões fixas de temas e atrito ao mesclar paletas com sistemas de design proprietários.

A resposta da equipe foi o lançamento do **Tremor Raw** — uma refundação arquitetural baseada no paradigma **Copy-and-Paste (Code Ownership)** popularizado pelo Shadcn UI. No Tremor Raw:
1. **Sem Dependência de Pacote Monolítico de UI**: O desenvolvedor não instala `@tremor/react`. O código-fonte de cada gráfico, indicador e card analítico é copiado diretamente para a árvore de componentes da aplicação (`components/tremor/`).
2. **Controle Total sobre o Tailwind CSS**: Classes utilitárias do Tailwind estão expostas diretamente no JSX do componente, permitindo que bordas, opacidades de gradiente, eixos de coordenadas e tooltips herdem os tokens exatos do produto sem abstrações opacas.
3. **Casamento com Radix UI & Recharts**: Primitivas acessíveis do Radix UI (Popovers, Tooltips, Dropdowns) são integradas à flexibilidade de renderização vetorial do Recharts, proporcionando gráficos visualmente consistentes com a UI externa.

### A Aquisição pela Vercel (Janeiro de 2025)

Em janeiro de 2025, a **Vercel adquiriu o Tremor**, trazendo os fundadores Severin Landolt e Christopher Kindl para o time de **Design Engineering** da empresa. Como resultado imediato da aquisição:
- Todos os blocos avançados e layouts completos do "Tremor Pro Blocks" tornaram-se **100% gratuitos e de código aberto (MIT)**.
- O desenvolvimento do Tremor Raw convergiu harmonicamente com o ecossistema **shadcn/ui** e a infraestrutura de **Generative UI** da Vercel (alimentando ferramentas como o **v0**).
- O Tremor tornou-se o motor canônico por trás do design analítico da Vercel (Vercel Analytics, Speed Insights, Usage & Billing Dashboards).

### A Assinatura Visual: "The Vercel / Stripe Metric Precision"

A estética visual do Tremor é definida pelo rigor da precisão analítica corporativa moderna:
1. **Tipografia Numérica Tabular Imutável (`tabular-nums`)**:
   Todo elemento quantitativo no Tremor adota obrigatoriamente a classe `tabular-nums` combinada com famílias de fontes geométricas neutras (`Geist Sans`, `Inter`) ou monoespaçadas (`JetBrains Mono`). Isso elimina o tremor de layout ("jitter") durante a atualização contínua de valores numéricos em tempo real.
2. **Superfícies de Dados Neutras & Hairline Borders**:
   Cards e gráficos não competem com os dados. Eles utilizam fundos cinzas sutilíssimos (`bg-white dark:bg-gray-950`), contornos milimétricos (`border border-gray-200 dark:border-gray-800`) e sombras estruturais atenuadas (`shadow-xs` ou `shadow-sm`), criando uma sensação de prancheta de instrumentação cirúrgica.
3. **Cromas Semânticos Funcionais**:
   Cores não são ornamentais; são vetores de significado. O sistema mapeia tons de alta legibilidade:
   - **Indigo/Blue**: Séries principais de dados neutros (volumes, acessos, requisições).
   - **Emerald/Green**: Estados de sucesso, crescimento positivo de receita (MRR/ARR), uptime de 100%.
   - **Amber/Orange**: Latência elevada, consumo próximo da cota, alertas de degradação.
   - **Rose/Red**: Churn rate, quebra de SLA, exceções 5xx e falhas críticas.
   - **Gray/Slate**: Médias móveis, períodos anteriores de comparação e eixos de referência.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto

1. **SaaS B2B & Plataformas de Gestão de Negócios**:
   Painéis de controle de receita recorrente (MRR, ARR, Net Revenue Retention), visualização de cohorts de usuários, funis de conversão de marketing e relatórios de faturamento por assinatura.
2. **FinTech, Bancos Digitais & Wealth Management**:
   Extratos financeiros com reconciliação em tempo real, gráficos de volatilidade patrimonial, alocação de ativos em carteira (Donut/BarList) e monitoramento de fluxo de caixa com barras de entrada versus saída.
3. **Cloud Infrastructure, DevOps & Observabilidade**:
   Páginas de status público e privado (uptime history em 30/60/90 dias com o componente `Tracker`), visualização de latência P50/P95/P99, consumo de CPU/Memória por cluster e logs de tráfego de borda.
4. **AI Observability & Gestão de Custo de LLMs**:
   Dashboards de consumo de tokens (prompt tokens vs. completion tokens), métricas de latência TTFT (Time to First Token), custo acumulado por modelo de fundação e distribuição de chamadas de API por cliente.
5. **E-commerce Analytics & Supply Chain**:
   Monitores de faturamento diário, ticket médio por categoria, taxas de devolução, inventário de estoque com barras de alerta e performance de logística de entrega.

### Papel no Ritmo Visual (A Aplicação da Regra 60-30-10)

- **60% — Fundação Neutra de Dados**:
  A base de toda tela com Tremor é composta por grids de cards de métricas estáticos, tabelas com números tabulares alinhados à direita, cabeçalhos de eixos discretos e backgrounds com hairline borders. Essa camada fornece estabilidade visual para a leitura de dezenas de métricas simultâneas sem fadiga cognitiva.
- **30% — Camada de Navegação, Orquestração & Controles Temporais**:
  Os seletores de data (`DateRangePicker`), toggles de granularidade temporal (1H, 24H, 7D, 30D, 1Y), abas de navegação (`TabNavigation`), filtros facetados (`MultiSelect`) e os tooltips interativos flutuantes acionados por hover.
- **10% — Picos de Destaque Analítico (Showstoppers de Telemetria)**:
  Gráficos de área com preenchimento em gradiente sutil e crosshair de alta precisão (`AreaChart`), indicadores circulares de cota com stroke vivo (`ProgressCircle`), o bloco sequencial de uptime com status em tempo real (`Tracker`) e o Donut central destacado em cartões executivos de fechamento.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

1. **Websites Cinematográficos & Landing Pages Promocionais Puras**:
   Páginas voltadas para branding de moda, lançamentos artísticos ou storytelling interativo (WebGL, GSAP, Three.js) onde o objetivo é gerar impacto sensorial e quebra de regras, e não fornecer leitura analítica objetiva.
2. **Cenários de Big Data com Streaming em Tempo Real Excedendo 20.000 Pontos no DOM**:
   O Tremor (via Recharts) renderiza elementos como **vetores SVG no DOM**. Quando um gráfico precisa plotar 50.000 nós de alta frequência por segundo (como gráficos de tick de bolsa de alta frequência HFT ou gráficos de dispersão genômica com centenas de milhares de pontos), o motor de reconciliação de nós SVG sobrecarrega a thread principal do navegador. Nestes cenários extremos, ferramentas baseadas em **Canvas 2D / WebGL** (como Apache ECharts, Deck.gl, SciChart ou Uplot) são estritamente mandatórias.
3. **Aplicações Mobile com Telas Não Adaptadas**:
   Inserir um `AreaChart` de 4 séries ou uma tabela de 10 colunas em uma viewport de 360px sem simplificação gera sobreposição ilegível de labels e eixos truncados. Em viewports pequenas, gráficos complexos devem ser substituídos por `SparkChart`, `BarList` ou resumos numéricos verticais.
4. **Interfaces Skewomórficas, Neumórficas ou Retrô Y2K**:
   O design system do Tremor é 100% ancorado na estética flat-craft suíça/modernista. Aplicar sombras volumétricas pesadas, botões de plástico brilhante ou bordas chanfradas destrói a identidade da biblioteca.

---

### ⚠️ Erros Comuns de Exagero ("Dashboard Chart Junk")

1. **O Anti-padrão do "Rainbow Chart" (Arco-íris Desnecessário)**:
   Utilizar 6 a 8 cores vivas diferentes em um único gráfico ou numa única tela de métricas. Gráficos de alta legibilidade utilizam tonalidades monocromáticas da mesma família ou limitam-se a 2 ou 3 cores funcionais contrastantes com alta taxa de diferenciação perceptível.
2. **A Armadilha do Truncamento Zero (Zero-Scale Truncation)**:
   Cortar a base do eixo Y (iniciando a escala em 95 em vez de 0) em gráficos de barras ou áreas sem um indicador visual explícito de quebra. Essa prática engana o usuário, fazendo uma oscilação marginal de 1% parecer um crescimento ou queda de 80%.
3. **Poluição de Linhas de Grade (Gridlines Excessivas)**:
   Habilitar linhas de grade horizontais e verticais com alto contraste (`stroke-gray-400`). No Tremor, as linhas de grade devem ser sutis (`stroke-gray-200 dark:stroke-gray-800`), pontilhadas (`strokeDasharray="3 3"`) ou limitadas estritamente ao eixo horizontal.
4. **Ignorar Números Tabulares (`tabular-nums`)**:
   Renderizar números dinâmicos sem a propriedade CSS `font-variant-numeric: tabular-nums`. Sem isso, o caractere "1" possui largura menor que o caractere "8", gerando solavancos e reposicionamento contínuo das colunas de tabelas a cada atualização via WebSocket.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 11 componentes mais emblemáticos da arquitetura do Tremor e Tremor Raw:

```
+-----------------------------------------------------------------------------------------+
|                                    TREMOR RAW ECOSYSTEM                                  |
|                                                                                         |
|  [ KPI Metrics & Spark ]       [ Core Time-Series ]          [ Proportional & Status ]  |
|  +--------------------+       +--------------------+        +-----------------------+   |
|  | $148,290.00 ▲ 12%  |       | AreaChart (Spline) |        | Tracker (Uptime 90d)  |   |
|  | ~~~/~\___ (Spark)  |       | BarChart / Combo   |        | BarList (Rankings)    |   |
|  +--------------------+       +--------------------+        | DonutChart & Category |   |
|                                                             +-----------------------+   |
|                                                                                         |
|  [ Operational Controls ]                                   [ High-Density Tables ]     |
|  - DateRangePicker with Quick Presets                       - Tabular Numbers Monospace |
|  - MultiSelect Filterbars & Popovers                        - Inline Micro-indicators   |
+-----------------------------------------------------------------------------------------+
```

### 1. AreaChart (Visualização Temporal com Gradiente Dinâmico e Crosshair)
- **Anatomia Visual**: Gráfico de série temporal que combina curvas contínuas (spline/natural) com gradiente linear semitransparente na área subjacente (opacidade de 20% no topo a 0% na base). Inclui eixos cartesianos formatáveis, linhas de grade sutis, crosshair vertical no hover e tooltip flutuante ancorado no ponto ativo com a legenda e os valores formatados.
- **Gatilho de Interação**: Hover ao longo do eixo horizontal (captura contínua de cursor via `Tooltip` do Recharts) e clique opcional para disparar filtros contextuais.
- **Onde Encaixar**: Seção Hero de dashboards analíticos, gráficos de receita mensal, telemetria de tráfego de rede e evolução de métricas de uso de API.
- **Props Chave**: `data`, `index`, `categories`, `colors`, `valueFormatter`, `showLegend`, `showGridLines`, `curveType="monotone"`, `autoMinValue`.

### 2. BarChart & ComboChart (Comparativo Bivariado de Volume e Tendência)
- **Anatomia Visual**:
  - *BarChart*: Colunas verticais ou barras horizontais arredondadas nos cantos externos (`radius={[4, 4, 0, 0]}`), suportando agrupamento lado a lado (`type="grouped"`) ou empilhamento (`type="stacked"`).
  - *ComboChart*: Mescla um gráfico de colunas na camada de base (representando volume absoluto, ex: total de requisições) com uma linha sobreposta de eixo Y secundário (representando taxa percentual, ex: taxa de erro).
- **Gatilho de Interação**: Hover sobre a barra individual ativando realce de opacidade e exibição de tooltip detalhado.
- **Onde Encaixar**: Análise de faturamento trimestral, comparação de conversão entre diferentes canais e balanço de despesas versus receitas.
- **Props Chave**: `data`, `index`, `categories`, `colors`, `type="stacked" | "grouped"`, `yAxisWidth`, `showAnimation`.

### 3. DonutChart (Distribuição Proporcional com Anel Central e Active Slice)
- **Anatomia Visual**: Gráfico circular em formato de anel com raio interno generoso (`innerRadius="70%"`), permitindo a inserção de uma métrica agregada mestre no centro vazio (ex: "Total: 100%"). Suporta legendas interativas e cantos de arco suaves.
- **Gatilho de Interação**: Hover sobre um arco específico expande levemente o raio da fatia (`activeShape`) e atualiza o texto central com o valor da fatia correspondente.
- **Onde Encaixar**: Distribuição de métodos de pagamento, composição de despesas por departamento, share de navegadores e status de inventário.
- **Props Chave**: `data`, `category`, `value`, `colors`, `variant="donut" | "pie"`, `valueFormatter`, `onValueChange`.

### 4. SparkChart (SparkAreaChart, SparkLineChart, SparkBarChart)
- **Anatomia Visual**: Micro-gráficos ultra-compactos (altura padrão entre 24px e 40px) sem eixos, sem legendas e sem linhas de grade. Fornecem apenas a silhueta da tendência recente dos últimos 7 ou 30 dias.
- **Gatilho de Interação**: Hover discreto com tooltip flutuante minimalista sem travar a navegação.
- **Onde Encaixar**: Embutidos dentro de células de tabelas de alta densidade, ao lado de números mestres em KPI Cards ou em badges compactos de monitoramento.
- **Props Chave**: `data`, `index`, `categories`, `colors`, `className="h-8 w-24"`.

### 5. Tracker (Monitor Contínuo de Status e Uptime de Infraestrutura)
- **Anatomia Visual**: Uma sequência contínua de blocos retangulares discretos (tipicamente 30, 60 ou 90 blocos correspondentes aos últimos dias ou horas). Cada bloco possui cantos levemente arredondados (`rounded-xs`) e cor semântica indicando status: verde para operacional, amarelo para degradação, vermelho para indisponibilidade total e cinza para ausência de telemetria.
- **Gatilho de Interação**: Hover sobre cada bloco individual aciona um `Radix Tooltip` com a data exata, porcentagem de uptime (ex: "99.98%") e o tempo de resposta médio registrado.
- **Onde Encaixar**: Status pages de infraestrutura pública, monitores de saúde de microsserviços, painéis de auditoria de jobs agendados e histórico de deploys contínuos.
- **Props Chave**: `data: Array<{ key, color, tooltip, hoverEffect }>`, `defaultBackgroundColor`.

### 6. BarList (Ranking Horizontal Proporcional de Alta Densidade)
- **Anatomia Visual**: Lista vertical de barras horizontais onde o preenchimento de fundo da barra é proporcional ao valor máximo da coleção. O rótulo descritivo do item fica posicionado à esquerda (suportando links e ícones de tecnologia), e o valor absoluto formatado fica ancorado rigorosamente à direita em fonte tabular.
- **Gatilho de Interação**: Hover destaca a linha; clique opcional redireciona para a página interna daquele item ou aplica filtro global.
- **Onde Encaixar**: Páginas mais visitadas de um site, países líderes de consumo, endpoints de API mais acionados e produtos mais vendidos.
- **Props Chave**: `data: Array<{ name, value, href, icon }>`, `valueFormatter`, `sortOrder="descending"`, `showAnimation`.

### 7. CategoryBar (Medidor Segmentado com Marcador de Pino / Linear Gauge)
- **Anatomia Visual**: Barra de progresso horizontal dividida em seções cromáticas contíguas que representam faixas de classificação (ex: Saudável, Atenção, Perigo). Um marcador vertical em forma de pino ("needle") flutua sobre a régua, indicando exatamente a posição percentual ou absoluta do valor atual do sistema.
- **Gatilho de Interação**: Renderização animada do marcador deslizando até a posição correta. Tooltip explicativo opcional ao pairar sobre a agulha.
- **Onde Encaixar**: Score de crédito de usuários, nível de risco de compliance, uso de cota de armazenamento e benchmarks de performance de software.
- **Props Chave**: `values: number[]`, `colors: string[]`, `marker: { value, tooltip, showAnimation }`.

### 8. ProgressCircle (Indicador Radial em SVG com Preenchimento de Arco)
- **Anatomia Visual**: Círculo com trilha de fundo atenuada (`stroke-gray-200 dark:stroke-gray-800`) e arco de progresso superior preenchido com cor viva através das propriedades `stroke-dasharray` e `stroke-dashoffset`. O centro do círculo pode abrigar um rótulo numérico (`94%`) ou um ícone indicativo.
- **Gatilho de Interação**: Animação suave de entrada do traço SVG ao montar o componente.
- **Onde Encaixar**: Cards de consumo de planos SaaS (ex: 8.500 / 10.000 requisições consumidas), metas de faturamento mensal e indicadores de conclusão de tarefas.
- **Props Chave**: `value: number`, `max?: number`, `radius?: number`, `strokeWidth?: number`, `color?: string`, `children?: ReactNode`.

### 9. KPI Card & Metric (Bloco Analítico de Alta Densidade)
- **Anatomia Visual**: Container retangular estruturado em 3 níveis verticais:
  1. *Header*: Título da métrica (ex: "Faturamento Líquido") em tom secundário neutro (`text-gray-500 dark:text-gray-400`) acompanhado de ícone de ajuda ou tooltip informativo.
  2. *Valor Principal*: Tipografia em escala `text-3xl font-semibold tabular-nums tracking-tight`.
  3. *Rodapé Contextual*: Selo de variação delta (`BadgeDelta`) exibindo a porcentagem contra o período anterior (`+14.2%`), com seta orientada e fundo verde/vermelho translúcido, combinado com frase descritiva ("comparado a últimos 30 dias").
- **Gatilho de Interação**: Hover eleva levemente a borda do card (`hover:border-gray-300 dark:hover:border-gray-700`); clique ativa a exibição expandida da métrica.
- **Onde Encaixar**: Topo de dashboards executivos, organizados em grids de 3 a 5 colunas responsivas.
- **Props Chave**: Composto via classes Tailwind sobre `<Card>`, `<Metric>`, `<Text>`, `<BadgeDelta>`.

### 10. DateRangePicker & Calendar (Seletor Temporal com Atalhos Rápidos)
- **Anatomia Visual**: Controle popover composto por um botão disparador que exibe o intervalo ativo formatado (`01 Out 2026 - 26 Out 2026`) com ícone de calendário. Ao abrir, revela um painel dividido em duas seções: lista lateral esquerda com atalhos de um clique ("Hoje", "Últimos 7 dias", "Últimos 30 dias", "Mês atual", "Ano até a data") e grid duplo de calendário à direita com destaque visual contínuo no intervalo selecionado.
- **Gatilho de Interação**: Clique abre o Popover; seleção rápida via teclado ou cursor fecha automaticamente após a escolha do segundo dia do intervalo.
- **Onde Encaixar**: Barra de controle superior (Navbar/Header do Dashboard), controlando o estado global de datas de todos os gráficos da página.
- **Props Chave**: `value`, `onValueChange`, `presets`, `enableYearNavigation`, `placeholder`.

### 11. Filterbar & MultiSelect (Barra de Refinamento Facetado de Telemetria)
- **Anatomia Visual**: Barra de filtros horizontais contendo botões compactos com cantos arredondados. Ao clicar em um filtro (ex: "Status do Pedido"), um menu popover suspenso exibe checkboxes com contadores de itens disponíveis ao lado de cada opção e campo de busca interno. Seleções ativas geram chips dismissíveis com botão "x".
- **Gatilho de Interação**: Busca em tempo real na lista de opções; fechamento instantâneo via `Esc` ou clique externo.
- **Onde Encaixar**: Acima de tabelas analíticas complexas e grids de visualização de logs.
- **Props Chave**: `options`, `selectedValues`, `onValueChange`, `placeholder`, `showSelectAll`.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

Para implementar os componentes do Tremor Raw em uma aplicação moderna (Next.js 15 / React 19 / Vite com Tailwind CSS), são necessárias as dependências fundamentais de manipulação de classes, ícones e gráficos vetoriais:

```bash
# Dependências essenciais do Tremor Raw
npm install recharts @remixicon/react clsx tailwind-merge @radix-ui/react-tooltip @radix-ui/react-popover
```

### Utilitários de Suporte Mandatórios

A arquitetura do Tremor Raw exige a criação de dois arquivos utilitários centrais na pasta `lib/`:
1. `src/lib/utils.ts` — O helper de concatenação e desduplicação de classes Tailwind (`cx`).
2. `src/lib/chartUtils.ts` — As definições de paletas de cores semânticas, cálculos de domínio do eixo Y e classes geradoras de gradientes.

---

### Física de Movimento, Interação & Transições

1. **Interpolação de Séries SVG no Recharts**:
   Os gráficos de área e linha utilizam curvas de Bézier cúbicas controladas pelo motor interno do Recharts, configuradas por padrão para amortecimento suave:
   - `animationDuration={800}`
   - `animationEasing="ease-in-out"` (equivalente ao `cubic-bezier(0.42, 0, 0.58, 1)`)
   - Curva de interpolação: `curveType="monotone"` ou `"natural"`, garantindo que os picos nunca criem laços retrocedentes indesejados.
2. **Micro-interações de Hover (CSS / Tailwind)**:
   Os blocos de status do `Tracker` e as barras do `BarList` utilizam transições táteis instantâneas para evitar lag perceptual:
   - `transition-all duration-150 ease-out` (com escala atenuada `hover:opacity-80 active:scale-[0.98]`).
3. **Popovers e Tooltips do Radix UI**:
   Os tooltips flutuantes de dados seguem a física de amortecimento elástico dos menus do Radix:
   - `data-[state=delayed-open]:animate-in data-[state=delayed-open]:fade-in-0 data-[state=delayed-open]:zoom-in-95 duration-200`
   - Saída rápida: `data-[state=closed]:animate-out data-[state=closed]:fade-out-0 data-[state=closed]:zoom-out-95 duration-100`

---

### Receitas de Código Funcionais

#### 1. Utilitário Mestre de Cores e Gráficos (`src/lib/chartUtils.ts`)

```typescript
// src/lib/chartUtils.ts
export type ColorUtility = "emerald" | "blue" | "cyan" | "indigo" | "violet" | "amber" | "rose" | "gray"

export interface ChartColorMap {
  stroke: string
  fill: string
  bg: string
  text: string
}

export const chartColors: Record<ColorUtility, ChartColorMap> = {
  emerald: {
    stroke: "#10b981",
    fill: "rgba(16, 185, 129, 0.15)",
    bg: "bg-emerald-500",
    text: "text-emerald-500",
  },
  blue: {
    stroke: "#3b82f6",
    fill: "rgba(59, 130, 246, 0.15)",
    bg: "bg-blue-500",
    text: "text-blue-500",
  },
  cyan: {
    stroke: "#06b6d4",
    fill: "rgba(6, 182, 212, 0.15)",
    bg: "bg-cyan-500",
    text: "text-cyan-500",
  },
  indigo: {
    stroke: "#6366f1",
    fill: "rgba(99, 102, 241, 0.15)",
    bg: "bg-indigo-500",
    text: "text-indigo-500",
  },
  violet: {
    stroke: "#8b5cf6",
    fill: "rgba(139, 92, 246, 0.15)",
    bg: "bg-violet-500",
    text: "text-violet-500",
  },
  amber: {
    stroke: "#f59e0b",
    fill: "rgba(245, 158, 11, 0.15)",
    bg: "bg-amber-500",
    text: "text-amber-500",
  },
  rose: {
    stroke: "#f43f5e",
    fill: "rgba(244, 63, 94, 0.15)",
    bg: "bg-rose-500",
    text: "text-rose-500",
  },
  gray: {
    stroke: "#6b7280",
    fill: "rgba(107, 114, 128, 0.15)",
    bg: "bg-gray-500",
    text: "text-gray-500",
  },
}

export const formatCurrency = (val: number): string =>
  new Intl.NumberFormat("pt-BR", { style: "currency", currency: "BRL", maximumFractionDigits: 0 }).format(val)

export const formatCompactNumber = (val: number): string =>
  new Intl.NumberFormat("en-US", { notation: "compact", compactDisplay: "short" }).format(val)
```

---

#### 2. Componente Tracker Completo com Radix Tooltip (`src/components/tremor/Tracker.tsx`)

```tsx
// src/components/tremor/Tracker.tsx
"use client"

import React from "react"
import * as Tooltip from "@radix-ui/react-tooltip"
import { cx } from "@/lib/utils"

export interface TrackerBlockProps {
  key?: string | number
  color?: string
  tooltip?: string
  hoverEffect?: boolean
}

export interface TrackerProps extends React.HTMLAttributes<HTMLDivElement> {
  data: TrackerBlockProps[]
  defaultBackgroundColor?: string
}

export const Tracker = React.forwardRef<HTMLDivElement, TrackerProps>(
  ({ data = [], defaultBackgroundColor = "bg-gray-200 dark:bg-gray-800", className, ...props }, ref) => {
    return (
      <Tooltip.Provider delayDuration={0}>
        <div
          ref={ref}
          className={cx("flex h-8 w-full items-center gap-1 overflow-hidden rounded-md", className)}
          {...props}
        >
          {data.map((block, index) => {
            const blockContent = (
              <div
                className={cx(
                  "h-full flex-1 first:rounded-l-sm last:rounded-r-sm transition-all duration-150",
                  block.color || defaultBackgroundColor,
                  block.hoverEffect !== false && "hover:opacity-80 active:scale-95"
                )}
              />
            )

            if (!block.tooltip) {
              return <React.Fragment key={block.key ?? index}>{blockContent}</React.Fragment>
            }

            return (
              <Tooltip.Root key={block.key ?? index}>
                <Tooltip.Trigger asChild>{blockContent}</Tooltip.Trigger>
                <Tooltip.Portal>
                  <Tooltip.Content
                    side="top"
                    sideOffset={6}
                    className="z-50 rounded-md border border-gray-200 dark:border-gray-800 bg-white dark:bg-gray-950 px-2.5 py-1 text-xs font-medium text-gray-900 dark:text-gray-100 shadow-md animate-in fade-in-0 zoom-in-95 tabular-nums"
                  >
                    {block.tooltip}
                    <Tooltip.Arrow className="fill-gray-200 dark:fill-gray-800" />
                  </Tooltip.Content>
                </Tooltip.Portal>
              </Tooltip.Root>
            )
          })}
        </div>
      </Tooltip.Provider>
    )
  }
)

Tracker.displayName = "Tracker"
```

---

#### 3. Componente AreaChart Customizado com Recharts (`src/components/tremor/AreaChart.tsx`)

```tsx
// src/components/tremor/AreaChart.tsx
"use client"

import React from "react"
import {
  Area,
  AreaChart as RechartsAreaChart,
  CartesianGrid,
  ResponsiveContainer,
  Tooltip,
  XAxis,
  YAxis,
} from "recharts"
import { cx } from "@/lib/utils"
import { chartColors, ColorUtility } from "@/lib/chartUtils"

interface AreaChartProps {
  data: Array<Record<string, any>>
  index: string
  categories: string[]
  colors?: ColorUtility[]
  valueFormatter?: (value: number) => string
  className?: string
  yAxisWidth?: number
}

export function AreaChart({
  data,
  index,
  categories,
  colors = ["blue", "emerald"],
  valueFormatter = (val: number) => `${val}`,
  className,
  yAxisWidth = 48,
}: AreaChartProps) {
  return (
    <div className={cx("w-full h-72", className)}>
      <ResponsiveContainer width="100%" height="100%">
        <RechartsAreaChart data={data} margin={{ top: 10, right: 10, left: -20, bottom: 0 }}>
          <defs>
            {categories.map((cat, idx) => {
              const colorKey = colors[idx % colors.length]
              const conf = chartColors[colorKey]
              return (
                <linearGradient key={cat} id={`color-${cat}`} x1="0" y1="0" x2="0" y2="1">
                  <stop offset="5%" stopColor={conf.stroke} stopOpacity={0.25} />
                  <stop offset="95%" stopColor={conf.stroke} stopOpacity={0.0} />
                </linearGradient>
              )
            })}
          </defs>
          <CartesianGrid strokeDasharray="3 3" vertical={false} className="stroke-gray-200 dark:stroke-gray-800" />
          <XAxis
            dataKey={index}
            tickLine={false}
            axisLine={false}
            className="text-xs text-gray-400 dark:text-gray-500 font-mono"
            dy={8}
          />
          <YAxis
            tickLine={false}
            axisLine={false}
            width={yAxisWidth}
            tickFormatter={valueFormatter}
            className="text-xs text-gray-400 dark:text-gray-500 font-mono"
          />
          <Tooltip
            content={({ active, payload, label }) => {
              if (!active || !payload?.length) return null
              return (
                <div className="rounded-lg border border-gray-200 dark:border-gray-800 bg-white/95 dark:bg-gray-950/95 p-3 shadow-lg backdrop-blur-md">
                  <p className="text-xs font-semibold text-gray-700 dark:text-gray-300 mb-1">{label}</p>
                  <div className="space-y-1">
                    {payload.map((entry, idx) => (
                      <div key={idx} className="flex items-center justify-between gap-4 text-xs font-mono">
                        <span className="flex items-center gap-1.5 text-gray-500">
                          <span className="h-2 w-2 rounded-full" style={{ backgroundColor: entry.color }} />
                          {entry.name}:
                        </span>
                        <span className="font-semibold tabular-nums text-gray-900 dark:text-gray-100">
                          {valueFormatter(Number(entry.value))}
                        </span>
                      </div>
                    ))}
                  </div>
                </div>
              )
            }}
          />
          {categories.map((cat, idx) => {
            const colorKey = colors[idx % colors.length]
            const conf = chartColors[colorKey]
            return (
              <Area
                key={cat}
                type="monotone"
                dataKey={cat}
                stroke={conf.stroke}
                strokeWidth={2}
                fillOpacity={1}
                fill={`url(#color-${cat})`}
                animationDuration={800}
                animationEasing="ease-in-out"
              />
            )
          })}
        </RechartsAreaChart>
      </ResponsiveContainer>
    </div>
  )
}
```

---

#### 4. Card Analítico Completo (Métrica + Badge Delta + SparkLine + Tracker)

```tsx
// src/components/dashboard/ExecutiveKpiCard.tsx
"use client"

import React from "react"
import { RiArrowUpLine } from "@remixicon/react"
import { AreaChart } from "@/components/tremor/AreaChart"
import { Tracker, TrackerBlockProps } from "@/components/tremor/Tracker"
import { formatCurrency } from "@/lib/chartUtils"

const sparkData = [
  { day: "01", val: 3200 },
  { day: "05", val: 4100 },
  { day: "10", val: 3800 },
  { day: "15", val: 5600 },
  { day: "20", val: 6200 },
  { day: "25", val: 7890 },
]

const uptimeData: TrackerBlockProps[] = Array.from({ length: 30 }, (_, i) => ({
  key: i,
  color: i === 14 ? "bg-amber-400" : "bg-emerald-500",
  tooltip: i === 14 ? "Dia 15: Degradação pontual (98.4%)" : `Dia ${i + 1}: 100% Operacional`,
}))

export function ExecutiveKpiCard() {
  return (
    <div className="rounded-xl border border-gray-200 dark:border-gray-800 bg-white dark:bg-gray-950 p-6 shadow-xs transition-shadow hover:shadow-md">
      {/* Top Header */}
      <div className="flex items-center justify-between">
        <span className="text-xs font-medium uppercase tracking-wider text-gray-500 dark:text-gray-400">
          Receita Líquida Recorrente (MRR)
        </span>
        <span className="inline-flex items-center gap-0.5 rounded-full bg-emerald-500/10 px-2 py-0.5 text-xs font-semibold text-emerald-600 dark:text-emerald-400">
          <RiArrowUpLine className="h-3.5 w-3.5" />
          +18.4%
        </span>
      </div>

      {/* Main Metric */}
      <div className="mt-2 flex items-baseline gap-2">
        <h2 className="text-3xl font-bold tracking-tight text-gray-900 dark:text-gray-50 font-mono tabular-nums">
          {formatCurrency(148290)}
        </h2>
        <span className="text-xs text-gray-400 font-mono">BRL/mês</span>
      </div>

      {/* Spark Mini-Chart */}
      <div className="mt-4">
        <AreaChart
          data={sparkData}
          index="day"
          categories={["val"]}
          colors={["emerald"]}
          className="h-28"
          valueFormatter={(v) => formatCurrency(v)}
        />
      </div>

      {/* SLA / Uptime Sub-Tracker */}
      <div className="mt-6 border-t border-gray-100 dark:border-gray-800/80 pt-4">
        <div className="flex justify-between text-xs text-gray-500 mb-1.5 font-medium">
          <span>Disponibilidade da API (Últimos 30 dias)</span>
          <span className="font-mono tabular-nums text-gray-700 dark:text-gray-300">99.94%</span>
        </div>
        <Tracker data={uptimeData} className="h-4" />
      </div>
    </div>
  )
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao arquitetar e especificar telas que utilizam componentes analíticos do **Tremor / Tremor Raw**, a IA deve seguir rigorosamente as seguintes convenções arquiteturais:

### 1. Regra de Ouro dos Números Tabulares
- Todo componente que exiba moeda, porcentagens, timestamps, latências ou volumes numéricos DEVE aplicar explicitamente a classe CSS `tabular-nums` ou o utilitário Tailwind `font-mono tabular-nums`. Isso previne saltos visuais nas colunas de tabelas e cabeçalhos de cartões durante renderizações subsequentes.

### 2. Padrão de Dimensionamento de Contêineres de Gráficos
- O componente `<ResponsiveContainer />` do Recharts exige imperativamente que o seu elemento ancestral possua uma altura estrita definida em CSS. A IA deve sempre encapsular componentes de gráfico em wrappers com classes utilitárias explícitas:
  - Dashboards Desktop (visão ampla principal): `className="h-72 w-full"` ou `className="h-80 w-full"`.
  - Painéis Secundários ou Bento Grids de 2 colunas: `className="h-56 w-full"`.
  - Micro-gráficos embutidos (Sparklines): `className="h-8 w-24"` ou `className="h-10 w-32"`.

### 3. Coexistência Perfeita com Shadcn UI
- O Tremor Raw **não duplica** o catálogo base de inputs e modais do Shadcn UI. A recomendação canônica é:
  - Usar **Shadcn UI** para: `Button`, `Dialog`, `DropdownMenu`, `Sidebar`, `Input`, `Sheet`, `Sonner`.
  - Usar **Tremor Raw** para: `AreaChart`, `BarChart`, `DonutChart`, `Tracker`, `BarList`, `CategoryBar`, `ProgressCircle`, `DateRangePicker`.
  - Ambos os sistemas compartilham os mesmos tokens do Tailwind e a mesma filosofia de código pertencente ao repositório local.

### 4. Otimização de Performance e Memoização
- Gráficos vetoriais SVG são sensíveis a renderizações desnecessárias. Toda transformação de dataset (cálculo de agregações, agrupamento de datas, cálculo de médias móveis) deve ser protegida por `useMemo`:
  ```tsx
  const formattedData = useMemo(() => {
    return rawMetrics.map(item => ({
      date: formatDate(item.timestamp),
      revenue: item.amount / 100,
    }))
  }, [rawMetrics])
  ```
- Para séries temporais com mais de 500 pontos, deve-se aplicar downsampling (algoritmo LTTB - *Largest-Triangle-Three-Buckets*) antes de passar o array de dados para a prop `data` do gráfico.

### 5. Contraste e Acessibilidade (WCAG 2.1 AA)
- Não confiar exclusivamente na cor para transmitir estado crítico. Gráficos de barra e áreas devem sempre vir acompanhados de tooltips textuais com valores numéricos explícitos.
- Textos em eixos cartesianos devem manter contraste mínimo de `4.5:1` em relação ao fundo (usar `text-gray-500` no modo claro e `text-gray-400` no modo escuro).
