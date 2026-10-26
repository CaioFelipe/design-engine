---
id: "kibo-ui"
name: "Kibo UI"
url: "https://www.kibo-ui.com/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Modern Craft Minimal", "B2B Enterprise Density", "High-Functionality Composition", "Shadcn Native Tokens", "Accessible Stateful Workflows"]
densidade_informacao: "Alta"
impacto_visual: "Moderado a Alto/Showstopper"
custo_computacional: "Medio (Framer Motion/JS) a Baixo (CSS/Headless)"
stack_frameworks: ["React 19 / 18", "Next.js", "Tailwind CSS (v3 & v4)", "Radix UI", "Dnd Kit (@dnd-kit)", "TanStack Table", "Jotai", "Date-fns", "Shiki", "Motion (Framer Motion)", "Media Chrome"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "Plus Jakarta Sans", "JetBrains Mono", "Geist Mono"]
  paletas_ideais: ["Deep Zinc Dark Mode", "Slate High-Density Monochrome", "Neutral Stone Enterprise", "Subtle Blue SaaS Accents"]
  combinacoes_recomendadas: ["Shadcn UI", "Recharts", "Lucide React", "TanStack Query", "Vaul", "Cult UI", "Magic UI"]
  conflitos_esteticos: ["Neumorfismo skeuomórfico exagerado", "Brutalismo saturado sem hierarquia", "Layouts lúdicos infantis sem grid"]
---

# Kibo UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado pelo renomado designer e engenheiro de software australiano **Hayden Bleasel** (autor do *next-forge* e diretor criativo de referência no ecossistema Next.js/Tailwind), o **Kibo UI** (`kibo-ui.com`) nasceu para resolver a maior lacuna existente no ecossistema do **shadcn/ui**: a ausência de **componentes compostos complexos e altamente funcionais** para produtos digitais em escala comercial.

Enquanto a biblioteca base do shadcn/ui fornece primitivas atômicas essenciais (botões, caixas de diálogo, menus suspensos, campos de entrada e tooltips), qualquer equipe que desenvolva um SaaS B2B moderno, ferramenta de produtividade ou painel administrativo inevitavelmente se depara com a necessidade de construir padrões pesados do zero: **Kanban boards com ordenação drag-and-drop**, **gráficos de Gantt com timeline temporal**, **calendários de distribuição de tarefas**, **zonas de upload de arquivos com validação**, **seletores de cor estilo Figma**, **árvores de diretórios colapsáveis** e **modais em pilha (dialog stacks)**.

O Kibo UI resolve essa lacuna operando sob quatro pilares conceituais:

1. **Herança Nativa de Tokens do Shadcn (`CSS Variables Architecture`)**:
   O Kibo UI não tenta inventar uma nova linguagem visual concorrente. Ele é rigorosamente construído sobre os mesmos tokens de cores semânticas (`--background`, `--foreground`, `--card`, `--primary`, `--secondary`, `--muted`, `--accent`, `--border`, `--ring`), raios de curvatura (`--radius`) e convenções do shadcn/ui. Isso significa que, ao adicionar qualquer componente do Kibo UI em uma aplicação existente com shadcn, ele se adapta de forma orgânica e indistinguível ao tema da aplicação, seja ele um dark mode profundo em Zinc ou um tema corporativo em Slate/Neutral.

2. **Propriedade Integral do Código (Open-Source Registry via CLI)**:
   Em total alinhamento com a revolução inaugurada pelo shadcn/ui, o Kibo UI não é um pacote monolítico opaco instalado no `node_modules` com estilos travados. É um **registro público e modular** distribuído via CLI (`npx kibo-ui@latest add <component>` ou `npx shadcn@latest add @kibo-ui/<component>`). O código-fonte em TypeScript puro entra diretamente na pasta do projeto (`components/ui/` ou `components/kibo-ui/`), permitindo que a equipe audite, modifique as regras de negócio, altere a tipagem e ajuste os layouts conforme a demanda.

3. **Orquestração de Motores Headless Especializados**:
   Em vez de reinventar bibliotecas complexas ou criar implementações ingênuas de arrastar e soltar que quebram acessibilidade, o Kibo UI integra e encapsula com elegância os melhores motores da web moderna:
   - **`@dnd-kit/core` & `@dnd-kit/sortable`**: Para drag-and-drop de alta performance com suporte completo a leitores de tela e navegação por teclado (WAI-ARIA).
   - **`date-fns` & `jotai`**: Para manipulação imutável de datas e gerenciamento atômico de estados de timeline (zoom, scroll temporal) sem re-renderizações desnecessárias da árvore inteira.
   - **`shiki` & `@shikijs/transformers`**: Para blocos de código com destaque de sintaxe em nível de IDE no lado cliente e servidor.
   - **`media-chrome`**: Para reprodutores de mídia totalmente acessíveis e estilizados nativamente.
   - **`motion/react` (Framer Motion v12)**: Para micro-interações táteis e interpolações de layout fluidas em controles de comparação e transições em árvore.

4. **Densidade de Informação e Estética "Craft B2B"**:
   A assinatura estética do Kibo UI é caracterizada por linhas finas (*hairline borders* de 1px com transparências sutis), tipografia compacta e hierarquizada, cartões com elevação sutil (`shadow-xs` / `shadow-sm`), anéis de foco expressivos (`ring-2 ring-primary`) para operações táteis/arrasto, e estados vazios (*empty states*) limpos com iconografia precisa via `lucide-react`.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **SaaS B2B de Gestão de Projetos e Fluxo de Trabalho (Linear / Asana / Jira Clones)**:
   É a escolha definitiva para plataformas que dependem de visualizações múltiplas do mesmo conjunto de dados (visualização em Lista, Kanban Board, Gantt Timeline e Grid de Calendário). O Kibo UI entrega exatamente essas quatro matrizes estruturadas.
2. **Plataformas de Engenharia de Software, DevTools e CI/CD**:
   Ambientes voltados a desenvolvedores que necessitam de árvores de diretórios interativas (`tree`), blocos de código com numeração de linhas e cópia instantânea (`code-block`), gráficos de atividade e commits (`contribution-graph`) e seletores avançados de parâmetros (`choicebox`).
3. **Dashboards Financeiros, CRMs Operacionais e ERPs Modernos**:
   Painéis densos onde o operador precisa processar grandes volumes de dados através de tabelas ordenáveis (`table`), visualizar métricas em rolagem suave (`ticker`, `marquee`) e gerenciar uploads de notas fiscais ou documentos de clientes (`dropzone`).
4. **Ferramentas de Criação, Design, IA e Manipulação de Mídia**:
   Aplicações de edição e geração visual que demandam corte interativo de imagens (`image-crop`), comparação antes/depois com slider deslizante (`comparison`), seletor de paletas com conta-gotas (`color-picker`) e players de vídeo customizados (`video-player`).
5. **Wizards de Configuração Complexos & Onboarding Multi-etapas**:
   Fluxos que exigem múltiplos passos sem perder o contexto visual anterior, implementados com elegância geométrica através de cartões sobrepostos (`dialog-stack`).

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Neutra e Estrutural)**:
  Fornecida pelas primitivas clássicas do shadcn/ui: estrutura de páginas, sidebar retrátil, barra superior, containers de cartão neutros (`bg-card`, `border-border/40`) e tipografia base em `Geist Sans` ou `Inter`.
- **30% (Motor Operacional e Componentes Compostos do Kibo UI)**:
  É a camada primária de interação utilitária: o **Kanban Board** central, a **Timeline de Gantt**, o **Grid de Calendário**, o **File Dropzone** e os **Choiceboxes** de parametrização. Os componentes do Kibo UI organizam e viabilizam o trabalho do usuário sem recorrer a pirotecnias visuais gratuitas.
- **10% (Showstoppers de Foco e Destaque Tátil)**:
  Micro-interações de alto impacto visual quando o usuário realiza ações de destaque: a gaveta de pilha de modais (*Dialog Stack*) se abrindo em cascata 3D sutil, o divisor interativo de imagem (*Comparison Slider*), ou a animação de partículas ao concluir tarefas no kanban.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Landing Pages Institucionais Puramente Estáticas**:
  Adicionar componentes pesados como Kanban, Gantt ou Shiki Code Block em páginas de conversão de marketing voltadas para consumidores comuns (B2C) adiciona overhead de JavaScript desnecessário e polui a mensagem de vendas com densidade operacional incompatível.
- **Aplicações com Restrições Extremas de Bundle Size para Redes 2G/3G**:
  Componentes como `@dnd-kit`, `date-fns` e `shiki` carregam peso de parse em dispositivos modestos. Embora o Kibo UI seja modular, carregar todas as dependências compostas em uma mesma página mobile sem code-splitting impacta negativamente métricas de Core Web Vitals (como Total Blocking Time e INP).
- **Projetos Brutalistas Radicais ou Y2K Maximalistas**:
  O rigor milimétrico, os cantos arredondados contidos e a sofisticação sóbria do Kibo UI entram em choque direto com layouts com bordas pretas de 4px sólidas, ausência de bordas arredondadas e cores neon primárias gritantes.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões):
- **Coexistência Simultânea de Kanban e Gantt sem Abas**:
  Tentar renderizar um quadro Kanban completo e uma timeline de Gantt na mesma viewport simultaneamente resulta em sobrecarga cognitiva grave e concorrência de listeners de scroll horizontal. Utilize abas contextuais ou rotas distintas para alternar entre as visualizações.
- **Omissão de Paginação ou Virtualização em Grandes Volumes**:
  Renderizar mais de 500 cartões no Kanban ou milhares de nós no Tree View sem virtualização de lista causa lentidão nos cálculos de matriz de colisão do `@dnd-kit`.
- **Uso Excessivo de Choiceboxes Gigantes**:
  Substituir selects compactos por choiceboxes de cartão com ícone, título e descrição em formulários que possuem mais de 10 opções verticais, gerando scrolls desnecessários de centenas de pixels.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 12 componentes mais emblemáticos e poderosos do ecossistema Kibo UI:

```
┌────────────────────────────────────────────────────────────────────────┐
│                   CATÁLOGO DE COMPONENTES KIBO UI                      │
├──────────────────────┬─────────────────────────┬───────────────────────┤
│ GESTÃO & PRODUTIVID. │ FORMULÁRIOS & SELEÇÃO   │ MÍDIA & APRESENTAÇÃO  │
├──────────────────────┼─────────────────────────┼───────────────────────┤
│ 1. Kanban Board      │ 4. Dropzone             │ 9. Tree View          │
│ 2. Gantt Chart       │ 5. Choicebox            │ 10. Comparison Slider │
│ 3. Calendar Grid     │ 6. Color Picker         │ 11. Contribution Graph│
│                      │ 7. Code Block (Shiki)   │ 12. Video Player      │
│                      │ 8. Dialog Stack         │                       │
└──────────────────────┴─────────────────────────┴───────────────────────┘
```

### 1. Kanban Board (`@repo/kanban` / `kanban`)
- **Anatomia Visual**: Composto estrutural com cabeçalho de coluna (`KanbanHeader`), lista de cartões com scroll independente (`KanbanCards` sobre `ScrollArea`), cartões arrastáveis (`KanbanCard` sobre `Card`) e indicador de área receptora com anel de foco destacado (`isOver ? "ring-primary" : "ring-transparent"`). Possui um portal dedicado (`tunnel-rat`) para renderizar um clone exato do cartão em arrasto flutuando suavemente sob o cursor com sombra elevada.
- **Gatilho de Interação**: Arrastar e soltar via mouse, toque ou navegação por teclado (Espaço para levantar, setas direcionais para mover entre colunas, Espaço para soltar), suportado nativamente pelo `@dnd-kit/core`.
- **Onde encaixar**: Seção central de produtos SaaS B2B, painéis de sprint ágil, esteiras de CRM de vendas (Lead → Qualificado → Fechado) e backlogs operacionais.

### 2. Gantt Chart (`@repo/gantt` / `gantt`)
- **Anatomia Visual**: Painel de cronograma bidimensional divido em duas áreas: hierarquia lateral de tarefas e painel temporal horizontal. Suporta três modos de escala temporal (`daily`, `monthly`, `quarterly`), marcadores de data vertical (`GanttMarker`), faixas horizontais de status compartilhado (`lanes`) e barras de tarefa arredondadas coloridas por status.
- **Gatilho de Interação**: Arrastar horizontal com travamento de eixo via `@dnd-kit/modifiers` (`restrictToHorizontalAxis`), menu de contexto com clique direito (`ContextMenuTrigger` para deletar/editar tarefas) e controle de zoom temporal com debounce.
- **Onde encaixar**: Visualizações de roadmap de produto, planejamento de projetos de engenharia, alocação de equipes e acompanhamento de marcos contratuais.

### 3. Calendar Grid (`@repo/calendar` / `calendar`)
- **Anatomia Visual**: Grade de calendário mensal de alta densidade informativa com agrupamento dinâmico de tarefas por dia de entrega (`endAt`). Cada item exibe status em pílula colorida, truncamento inteligente de texto para evitar quebras de layout e cabeçalho integrado com alternador rápido de mês e ano alimentado pelo componente `Command/Combobox`.
- **Gatilho de Interação**: Navegação entre meses via botões de chevron ou dropdown de busca textual; clique em dias individuais para filtragem de eventos; sincronização de estado através de átomos `jotai` (`useCalendarMonth`, `useCalendarYear`).
- **Onde encaixar**: Painéis editoriais de agendamento de posts, calendários de lançamentos de software, escala de plantões técnicos e visão de eventos corporativos.

### 4. Dropzone (`@repo/dropzone` / `dropzone`)
- **Anatomia Visual**: Zona receptora contornada por borda tracejada ou estilo botão outline expansível (`Button variant="outline"`). Ao receber arquivos, ativa um anel de foco pulsante (`ring-1 ring-ring`). Inclui o subcomponente `DropzoneContent` com formatação automática de tamanho de arquivo legível para humanos via função de cálculo binário (`B`, `KB`, `MB`, `GB`) e formatação gramatical localizada com `Intl.ListFormat`.
- **Gatilho de Interação**: Arrastar e soltar arquivos sobre a área (`onDrop`), clique tradicional para abrir o seletor do sistema operacional e feedback de erro imediato com tratamento de rejeição de formato MIME e limite de peso.
- **Onde encaixar**: Telas de importação de planilhas CSV, formulários de upload de documentos de identidade/KYC, anexos em chamados de suporte e galerias de upload de assets.

### 5. Choicebox (`@repo/choicebox` / `choicebox`)
- **Anatomia Visual**: Cartões de seleção rica que substituem o rádio ou checkbox convencional. Cada item (`ChoiceboxItem`) renderiza uma superfície clicável com bordas finas contendo ícone opcional, título em negrito (`ChoiceboxItemTitle`), subtítulo secundário atenuado (`ChoiceboxItemSubtitle`), descrição detalhada em texto corrido e indicador circular de seleção alinhado à direita ou esquerda.
- **Gatilho de Interação**: Clique em qualquer parte do cartão ou navegação via teclado com as setas para cima/baixo (construído sobre `@radix-ui/react-radio-group`).
- **Onde encaixar**: Seleção de planos de assinatura no Checkout (ex: Starter vs Pro vs Enterprise), escolha de métodos de entrega em e-commerce técnico, ou configuração de infraestrutura (ex: instâncias de banco de dados Shared vs Dedicated).

### 6. Color Picker (`@repo/color-picker` / `color-picker`)
- **Anatomia Visual**: Seletor de cores profissional projetado à semelhança do painel de cores do Figma. Contém matriz retangular de saturação/brilho, controle deslizante de matiz (*hue*), controle deslizante de opacidade (*alpha*), campo de entrada direta para valores HEX, RGB ou HSL e botão com ícone de conta-gotas (`PipetteIcon`).
- **Gatilho de Interação**: Arrastar do cursor pela matriz de gradientes, clique nos controles deslizantes via Radix Slider e acionamento da API nativa do navegador `EyeDropper` para capturar qualquer pixel da tela do usuário.
- **Onde encaixar**: Painéis de personalização de marca e white-label em SaaS B2B, configuradores de tema visual, construtores de email e editores de templates.

### 7. Code Block (`@repo/code-block` / `code-block`)
- **Anatomia Visual**: Bloco de código com realce de sintaxe fiel renderizado via Shiki, com suporte a múltiplos temas (Dark/Light), numeração de linhas lateral perfeitamente alinhada, badge indicando a linguagem (TypeScript, JSON, Python, etc.) e botão superior de cópia instantânea com transição de ícone para feedback de sucesso.
- **Gatilho de Interação**: Clique no botão de copiar para disparar `navigator.clipboard.writeText` e alternador de abas para múltiplos arquivos quando encapsulado em tabs.
- **Onde encaixar**: Portais de documentação de APIs para desenvolvedores, modais de visualização de payloads JSON em logs de auditoria e blocos de snippets em artigos técnicos.

### 8. Dialog Stack (`@repo/dialog-stack` / `dialog-stack`)
- **Anatomia Visual**: Padrão de modal inovador em camadas tridimensionais sobrepostas. Quando múltiplos diálogos ou passos são abertos, os cartões anteriores recuam para o topo com deslocamento vertical progressivo (`translateY(-10px)`), redução proporcional de largura (`calc(100% - 10px * offset)`) e atenuação visual, criando a sensação física de uma pilha de cartas reais.
- **Gatilho de Interação**: Clique nos botões "Avançar" / "Voltar", ou clique direto no cabeçalho visível do cartão anterior para retornar ao passo correspondente (`clickable=true`).
- **Onde encaixar**: Fluxos de onboarding complexos, wizards de configuração com múltiplos passos (Dados Básicos → Permissões → Faturamento) e processos de checkout empresarial.

### 9. Tree View (`@repo/tree` / `tree`)
- **Anatomia Visual**: Componente hierárquico expansível com ícones semânticos automáticos (`Folder`, `FolderOpen`, `File`), linhas guia conectoras que indicam profundidade de aninhamento (`showLines=true`), recuo proporcional configurável e suporte a seleção múltipla visual com cores de destaque sutis.
- **Gatilho de Interação**: Clique no chevron ou no nó para alternar expansão (animado com suavidade via `motion/react` e `AnimatePresence`), clique com tecla `Ctrl/Cmd` para seleção múltipla de arquivos.
- **Onde encaixar**: Gerenciadores de arquivos na nuvem, exploradores de código em Web IDEs, navegadores de esquemas de banco de dados e menus de documentação com árvore profunda.

### 10. Comparison Slider (`@repo/comparison` / `comparison`)
- **Anatomia Visual**: Visualizador comparativo antes/depois composto por dois elementos sobrepostos divididos por uma linha vertical divisória com pegador central (`GripVerticalIcon`). Utiliza interpolação cinemática baseada em valores de mola (`useSpring`) para movimentação orgânica sem trepidação.
- **Gatilho de Interação**: Suporte a dois modos: arraste interativo (`mode="drag"`) ou rastreamento suave da posição do cursor do mouse (`mode="hover"`), funcionando perfeitamente em telas touch.
- **Onde encaixar**: Demonstrações visuais de processamento de imagem por IA (ex: upscale, remoção de fundo), comparação de renderização de mapas de satélite, e showcases de redesign de UI.

### 11. Contribution Graph (`@repo/contribution-graph` / `contribution-graph`)
- **Anatomia Visual**: Grade de calor cronológica inspirada no histórico de contribuições do GitHub. Organizada em semanas e dias do ano, mapeia valores de atividade em 5 níveis discretos de tonalidade de cor (`level 0` a `level 4`), com rótulos de meses no topo e dias da semana à esquerda, finalizando com legenda quantitativa ("Menos" → "Mais").
- **Gatilho de Interação**: Hover sobre qualquer célula diária para exibir tooltip informativo contendo a data exata formatada e a contagem de eventos registrados.
- **Onde encaixar**: Painéis de perfil de usuário em SaaS de desenvolvimento, métricas de frequência de login em plataformas de educação, e auditoria de volumetria de deploys ou execuções de testes.

### 12. Video Player (`@repo/video-player` / `video-player`)
- **Anatomia Visual**: Reprodutor multimídia completo construído sobre a biblioteca padrão da indústria `media-chrome`. Substitui os controles nativos do navegador por botões estilizados rigorosamente com as classes de botão, slider e tooltip do shadcn/ui.
- **Gatilho de Interação**: Teclas de atalho para reproduzir/pausar (Espaço), avançar/retroceder (setas), controle de volume com slider proporcional, alternância de Picture-in-Picture (PiP) e tela cheia.
- **Onde encaixar**: Plataformas de cursos online e videoaulas (LMS), visualizadores de gravações de sessões de usuário (estilo FullStory/PostHog) e players de demonstração de produto em SaaS.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

Para utilizar o Kibo UI em um projeto React 19 / Next.js, certifique-se de que o Tailwind CSS e a configuração base do shadcn/ui estejam inicializados com a opção de variáveis CSS ativada.

```bash
# 1. Instalação das dependências centrais dos motores do Kibo UI
npm install @dnd-kit/core @dnd-kit/sortable @dnd-kit/utilities @dnd-kit/modifiers
npm install date-fns jotai lucide-react tunnel-rat motion react-dropzone
npm install shiki @shikijs/transformers media-chrome color

# 2. Instalação de componentes individuais via CLI do Kibo UI
npx kibo-ui@latest add kanban
npx kibo-ui@latest add gantt
npx kibo-ui@latest add dropzone
npx kibo-ui@latest add choicebox
npx kibo-ui@latest add dialog-stack

# 3. Ou alternativamente via Shadcn CLI oficial apontando para o registro Kibo
npx shadcn@latest add @kibo-ui/kanban
npx shadcn@latest add @kibo-ui/gantt
```

### Física de Movimento, Transições e Curvas

O Kibo UI adota uma filosofia de movimento pragmática: animações cinéticas devem fornecer **feedback físico de posicionamento** sem atrasar o operador ou introduzir oscilações lúdicas desproporcionais ao ambiente B2B.

| Componente | Mecanismo de Física | Parâmetros / Configuração | Comportamento Visual |
| :--- | :--- | :--- | :--- |
| **Kanban Drag** | `@dnd-kit/utilities` + CSS Transforms | `transform: CSS.Transform.toString(transform)` com `transition` dinâmico | O cartão segue a ponta do cursor em tempo real sem latência; o cartão placeholder suaviza a abertura de espaço |
| **Comparison Slider** | `motion/react` + `useSpring` | `bounce: 0, duration: 0` (durante o arraste) | Acompanhamento cirúrgico sem "elástico" (spring overshoot) para controle milimétrico de pixels |
| **Tree Expansion** | `motion/react` + `AnimatePresence` | `initial={{ height: 0, opacity: 0 }}`, `animate={{ height: "auto", opacity: 1 }}`, `exit={{ height: 0, opacity: 0 }}` com curva `[0.16, 1, 0.3, 1]` | Expansão de pasta com aceleração inicial rápida e desaceleração suave sem saltos |
| **Dialog Stack** | Tailwind CSS Transitions | `transition-all duration-300 ease-out` com cálculo estático de `translateY(-10px * index)` | Transição de profundidade dimensional instantânea e consistente entre passos do wizard |

---

### Receita de Código Funcional: Kanban Board B2B Completo

Abaixo está uma implementação prática e realista de um **Kanban Board de Sprint B2B** construído com os componentes oficiais do Kibo UI, demonstrando tipagem estrita em TypeScript, manipulação de estado imutável com `arrayMove`, e anúncio de acessibilidade integrado:

```tsx
"use client";

import React, { useState } from "react";
import {
  KanbanBoard,
  KanbanCards,
  KanbanCard,
  KanbanHeader,
  KanbanProvider,
  type DragEndEvent,
} from "@/components/ui/kanban";
import { Badge } from "@/components/ui/badge";
import { Avatar, AvatarFallback, AvatarImage } from "@/components/ui/avatar";
import { ClockIcon, AlertCircleIcon, CheckCircle2Icon } from "lucide-react";

// 1. Definição estrita das estruturas de dados
interface TaskItem {
  id: string;
  name: string;
  column: string;
  priority: "low" | "medium" | "high";
  assignee: {
    name: string;
    avatar: string;
    initials: string;
  };
  estimateHours: number;
}

interface ColumnItem {
  id: string;
  name: string;
  colorBadge: string;
}

const INITIAL_COLUMNS: ColumnItem[] = [
  { id: "backlog", name: "Backlog", colorBadge: "bg-neutral-500/10 text-neutral-500" },
  { id: "in-progress", name: "Em Andamento", colorBadge: "bg-blue-500/10 text-blue-500" },
  { id: "review", name: "Revisão / QA", colorBadge: "bg-amber-500/10 text-amber-500" },
  { id: "done", name: "Concluído", colorBadge: "bg-emerald-500/10 text-emerald-500" },
];

const INITIAL_TASKS: TaskItem[] = [
  {
    id: "task-101",
    name: "Refatorar pipeline de autenticação OAuth2 com PKCE",
    column: "in-progress",
    priority: "high",
    assignee: { name: "Lucas Silva", avatar: "https://avatar.vercel.sh/lucas", initials: "LS" },
    estimateHours: 12,
  },
  {
    id: "task-102",
    name: "Implementar webhook assíncrono para eventos Stripe",
    column: "backlog",
    priority: "medium",
    assignee: { name: "Elena Rostova", avatar: "https://avatar.vercel.sh/elena", initials: "ER" },
    estimateHours: 8,
  },
  {
    id: "task-103",
    name: "Auditar contraste de cores do Design System para WCAG AAA",
    column: "review",
    priority: "low",
    assignee: { name: "Marcos Lima", avatar: "https://avatar.vercel.sh/marcos", initials: "ML" },
    estimateHours: 4,
  },
  {
    id: "task-104",
    name: "Otimizar consultas SQL em tabelas de auditoria particionadas",
    column: "done",
    priority: "high",
    assignee: { name: "Lucas Silva", avatar: "https://avatar.vercel.sh/lucas", initials: "LS" },
    estimateHours: 16,
  },
];

export function ProjectKanbanBoard() {
  const [columns] = useState<ColumnItem[]>(INITIAL_COLUMNS);
  const [tasks, setTasks] = useState<TaskItem[]>(INITIAL_TASKS);

  const handleDataChange = (newTasks: TaskItem[]) => {
    setTasks(newTasks);
    // Aqui você pode disparar uma mutação assíncrona (ex: via TanStack Query ou Server Action)
    // para persistir a nova ordem e coluna no backend:
    // updateTaskPositionsAction(newTasks);
  };

  const getPriorityBadge = (priority: TaskItem["priority"]) => {
    switch (priority) {
      case "high":
        return <Badge variant="destructive" className="text-[10px] h-5 px-1.5 font-medium">Urgente</Badge>;
      case "medium":
        return <Badge variant="secondary" className="text-[10px] h-5 px-1.5 font-medium text-amber-600 bg-amber-500/10 border-amber-500/20">Médio</Badge>;
      case "low":
        return <Badge variant="outline" className="text-[10px] h-5 px-1.5 font-normal text-muted-foreground">Baixo</Badge>;
    }
  };

  return (
    <div className="w-full h-[750px] flex flex-col p-6 bg-background text-foreground gap-4">
      {/* Cabeçalho da Visão */}
      <div className="flex items-center justify-between pb-2 border-b border-border/40">
        <div>
          <h2 className="text-lg font-semibold tracking-tight">Quadro de Engenharia — Sprint 42</h2>
          <p className="text-xs text-muted-foreground">
            Gerencie tarefas e dependências da equipe em tempo real com persistência automática.
          </p>
        </div>
        <div className="flex items-center gap-2">
          <Badge variant="outline" className="text-xs font-mono">
            {tasks.length} itens ativos
          </Badge>
        </div>
      </div>

      {/* Orquestrador do Kanban com Drag-and-Drop */}
      <div className="flex-1 min-h-0 overflow-x-auto pb-2">
        <KanbanProvider
          columns={columns}
          data={tasks}
          onDataChange={handleDataChange}
          className="flex h-full gap-4 min-w-[1000px]"
        >
          {(column) => (
            <KanbanBoard
              key={column.id}
              id={column.id}
              className="flex-1 flex flex-col min-w-[280px] max-w-[340px] rounded-lg border border-border/60 bg-muted/30 p-2 shadow-xs"
            >
              {/* Título da Coluna com Contagem */}
              <KanbanHeader className="flex items-center justify-between px-2 py-1.5 mb-2 border-b border-border/30">
                <span className="font-semibold text-xs tracking-tight text-foreground">
                  {column.name}
                </span>
                <span className={`text-[10px] px-2 py-0.5 rounded-full font-mono font-medium ${column.colorBadge}`}>
                  {tasks.filter((t) => t.column === column.id).length}
                </span>
              </KanbanHeader>

              {/* Área de Cartões com Scroll Interno */}
              <KanbanCards id={column.id} className="flex-1 flex flex-col gap-2 p-1">
                {(task: TaskItem) => (
                  <KanbanCard
                    key={task.id}
                    id={task.id}
                    name={task.name}
                    column={task.column}
                    className="group border border-border/50 bg-card p-3 rounded-md shadow-xs hover:border-border transition-all duration-150"
                  >
                    <div className="flex flex-col gap-2.5">
                      <div className="flex items-center justify-between gap-2">
                        {getPriorityBadge(task.priority)}
                        <span className="text-[11px] font-mono text-muted-foreground flex items-center gap-1">
                          <ClockIcon className="size-3" />
                          {task.estimateHours}h
                        </span>
                      </div>

                      <p className="text-xs font-medium leading-snug text-foreground/90 group-hover:text-foreground">
                        {task.name}
                      </p>

                      <div className="flex items-center justify-between pt-1 border-t border-border/30">
                        <span className="text-[10px] font-mono text-muted-foreground">
                          {task.id.toUpperCase()}
                        </span>
                        <Avatar className="size-5 border border-background">
                          <AvatarImage src={task.assignee.avatar} alt={task.assignee.name} />
                          <AvatarFallback className="text-[9px]">
                            {task.assignee.initials}
                          </AvatarFallback>
                        </Avatar>
                      </div>
                    </div>
                  </KanbanCard>
                )}
              </KanbanCards>
            </KanbanBoard>
          )}
        </KanbanProvider>
      </div>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao especificar a arquitetura de interface e os sistemas de componentes em um novo projeto (`DESIGN_BLUEPRINT.md`), a Inteligência Artificial e a liderança de engenharia devem seguir as diretrizes abaixo para o **Kibo UI**:

1. **Declaração no Stack de Componentes**:
   - Declare o Kibo UI como **camada de componentes compostos de negócio (Camada 2)**, posicionado imediatamente acima do `shadcn/ui` (camada 1 de primitivas atômicas) e abaixo de eventuais efeitos visuais pontuais (`Magic UI` / `Aceternity UI` na camada 3).
   ```markdown
   - Camada 1 (Primitivas): Shadcn UI (Button, Card, Dialog, Popover, Input)
   - Camada 2 (Organismos de Negócio): Kibo UI (Kanban, Gantt, Calendar, Dropzone, Choicebox, Table)
   - Camada 3 (Showstoppers/Efeitos): Magic UI / Framer Motion
   ```

2. **Convenção de Nomenclatura e Pastas**:
   - Os componentes do Kibo UI devem ser instalados na pasta `@/components/ui/` (seguindo o padrão shadcn) ou agrupados em `@/components/kibo-ui/` caso o projeto prefira segregação de escopo.
   - Sempre documente as dependências instaladas no `package.json` para cada componente Kibo (`@dnd-kit/core`, `date-fns`, `jotai`, `react-dropzone`, etc.).

3. **Diretiva de Execução no Servidor vs Cliente (`use client`)**:
   - Quase todos os componentes complexos do Kibo UI manipulam eventos do DOM, sensores de toque/mouse ou timers e requerem obrigatoriamente a diretiva `"use client"` no topo do arquivo do componente consumidor.
   - Envolva componentes que importam Shiki (`code-block`) ou `@dnd-kit` em carregamento dinâmico (`dynamic(() => import(...), { ssr: false })`) caso sejam renderizados condicionalmente dentro de modais para evitar a sobrecarga do bundle inicial na primeira carga da página (FCP/LCP).

4. **Coerência de Tokens Semânticos**:
   - Nunca injete cores hardcoded (como `bg-[#1a1a1a]` ou `text-[#ffffff]`) dentro dos subcomponentes do Kibo UI.
   - Utilize rigorosamente as variáveis de tema: `bg-muted/40` para colunas do kanban, `border-border/60` para divisores, `ring-primary` para anéis de arraste ativo e `text-muted-foreground` para metadados secundários.
