---
id: "kokonut-ui"
name: "Kokonut UI"
url: "https://www.kokonutui.com/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Tactile Micro-Interactions", "Physical Spring Dynamics", "AI Native & Copilot UI", "Clean Monospace Craft", "Shadcn Registry Native", "Modern Minimalist Light/Dark"]
densidade_informacao: "Flexivel"
impacto_visual: "Moderado a Alto/Showstopper"
custo_computacional: "Baixo (CSS/Tailwind) a Medio (Motion/Springs/Canvas)"
stack_frameworks: ["React 19", "Next.js 15 (App Router)", "Tailwind CSS v4 & v3", "Motion (motion/react)", "shadcn/ui", "TypeScript", "Lucide React"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Geist Mono", "Inter", "JetBrains Mono", "Plus Jakarta Sans"]
  paletas_ideais: ["Monochrome Grid (Pure White #FFFFFF / Pitch Black #000000 com bordas rgba(0,0,0,0.13) / rgba(255,255,255,0.14))", "Tactile Status Accents (Emerald Green #1FA834 / #3BB44B, Electric Crimson #FF2D55, Cyan Blue #44DCEA)", "Slate & Zinc Studio Dark Mode", "High-Contrast Functional Minimal"]
  combinacoes_recomendadas: ["shadcn/ui (fundação primária estrutural)", "Radix UI Primitives", "Aceternity UI (para backgrounds heroicos 3D complementares)", "Cult UI / Magic UI (para efeitos complementares)", "Lucide Icons"]
  conflitos_esteticos: ["Neumorfismo plástico com relevos opacos e sombras embaçadas", "Material Design 2 com elevação de sombras pesada e cores primárias berrantes", "Brutalismo Y2K tosco sem curvas de amortecimento físico", "Corporate Memphis pastel plano e sem contraste tátil"]
---

# Kokonut UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Kokonut UI**, criado e mantido pelo designer e engenheiro de software francês **Dorian Baffier** (Kokonut Labs), estabeleceu um padrão singular no ecossistema moderno de bibliotecas de componentes para React. Enquanto a grande maioria das bibliotecas de UI oscila entre primitivas monocromáticas utilitárias puras (estilo Radix/shadcn básico) ou demonstrações cinemáticas puramente ornamentais com shaders 3D pesados (estilo Aceternity), o Kokonut UI foca na intersecção perfeita entre **sensação tátil visceral (haptic-like feedback)** e **alta utilidade operacional diária**. Seu lema sintetiza sua filosofia de produto: *"Components that feel right"*.

A assinatura visual e sensorial do Kokonut UI repousa sobre quatro pilares técnicos essenciais:

### 1. Física de Movimento Táctil & Feedback Háptico Visual
Os componentes do Kokonut UI transmitem massa, gravidade, inércia e tensão mecânica através de molas (`springs`) afinadas com rigor milimétrico. Elementos como o *Pull Cord* respondem ao puxão com estiramento e ricochete elástico; o *Detent Dial* simula a resistência angular e os cliques magnéticos de seletores industriais; o *Slide to Confirm* reproduz o atrito progressivo e a trava irreversível de sistemas de pagamento iOS; e o *Particle Button* desdobra uma explosão estocástica calculada via Canvas de micro-partículas que voam na cor exata do botão e caem sob gravidade calibrada (`GRAVITY = 0.0016 px/ms²`).

### 2. Vocabulário Nativo para Interfaces de Inteligência Artificial (AI Native UI)
Kokonut UI destaca-se por ser uma das primeiras coleções abertas a fornecer um repertório exaustivo e refinado para copilotos e agentes de IA: inputs multimodais com alternadores de modelo de linguagem (`ai-model-selector`), medidores visuais de orçamento de contexto e janela de tokens (`ai-context-meter`), visualizadores de diff de código interativos (`ai-diff-review`), chips de aprovação humana de ações autônomas (`ai-tool-approval`), e timelines de orquestração multi-agente (`ai-agent-lanes`). Não são meras caixas de chat, mas componentes de governança e controle de IA de nível profissional.

### 3. A Estética "Clean Monospace Craft" & Linhas de Grade de Precisão
O acabamento visual do Kokonut UI é inspirado em manuais de engenharia aeroespacial e interfaces de áudio profissional (estilo Teenage Engineering e Braun). A interface organiza seus layouts em grids contínuos com separadores finíssimos de 1 pixel (`grid gap-px bg-black/[0.13] dark:bg-white/[0.14] border-black/[0.13] dark:border-white/[0.14]`), dispensando cards pesados com sombras difusas em favor de superfícies límpidas contrastantes. Cada componente é identificado por um código alfanumérico técnico em tipografia monoespaçada (`BT-01`, `CD-04`, `NV-02`, `IN-06`), acentuado por indicadores de status em verde esmeralda (`#1FA834` / `#3BB44B`) e rubi escarlate (`#FF2D55`).

### 4. Distribuição Zero-Bloat via Shadcn Registry & Prontidão para Agentes AI
Seguindo o paradigma moderno de código aberto iniciado por Guillermo Rauch e shadcn, o Kokonut UI não é um pacote NPM monolítico e fechado. Todos os seus mais de 100 componentes vivem como código TypeScript livre que pode ser instalado diretamente no diretório do projeto via CLI (`npx shadcn@latest add @kokonutui/<component>`) ou consumido nativamente por agentes autônomos de código (Claude Code, Cursor, VS Code, OpenAI Codex) através do protocolo MCP (`npx shadcn@latest mcp init`). O desenvolvedor é o proprietário definitivo do código-fonte gerado, podendo customizar cada mola, cor e tipagem sem bloqueios de fornecedor.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados
1. **Aplicações e Interfaces de Inteligência Artificial & Copilotos Cognitivos**:
   Plataformas que exigem interação contínua entre humano e IA (agentes autônomos, IDEs inteligentes, assistentes de codificação, ferramentas de geração de conteúdo). O catálogo de componentes de IA do Kokonut UI fornece imediatamente a linguagem visual de um copiloto maduro.
2. **SaaS B2B de Produtividade, Engenharia e Gestão Técnica**:
   Produtos inspirados no padrão Linear, Raycast, Figma e Notion onde a velocidade de navegação, a responsividade do teclado e a precisão dos inputs diferenciam o software de ferramentas corporativas antiquadas.
3. **Fintechs Institucionais, Dashboards de Tesouraria & Ações de Alto Risco**:
   Aplicações onde certas operações exigem confirmação inequívoca e deliberada do usuário. O *Slide to Confirm*, os *Detent Dials* e os *Amount Pads* impedem erros operacionais ao mesmo tempo em que entregam uma experiência de uso extremamente gratificante.
4. **Developer Tools, Cloud Platforms & Módulos de Upload Complexos**:
   Sistemas de arquivos, gerenciadores de clusters e portais de infraestrutura que dependem de uploaders resilientes com controle de chunks, cancelamento via `AbortSignal`, retry automático e feedback de status em tempo real.

### Papel no Ritmo Visual (A Regra 60-30-10)

Para maximizar o impacto visual sem poluir a cognição do usuário, a distribuição dos componentes Kokonut UI deve obedecer à seguinte proporção:

- **60% — Fundação Neutra e Estrutural (Base `shadcn/ui` + Geist Sans)**:
  Superfícies sólidas em preto absoluto (`bg-black`) ou branco límpido (`bg-white`), divididas por linhas de grade de 1px com baixa opacidade (`border-black/[0.13] dark:border-white/[0.14]`). A tipografia deve permanecer predominantemente Geist Sans ou Inter com hierarquias de cinza discretas (`text-black/60 dark:text-white/60`).
- **30% — Camada Tátil de Fluidez e Navegação Contextual (Micro-interações Kokonut UI)**:
  Controles de fluxo de trabalho: a barra de comandos *Action Search Bar* acessível via `Meta+K`, a *Floating Toolbar* com indicador deslizante de ferramenta ativa, o *File Upload* com fila de progresso em linha, e o *Bento Grid* organizando os blocos de dados com pequenos gráficos e contadores.
- **10% — Micro-delícias & Showstoppers de Ação (Apenas 1 a 2 por Fluxo)**:
  Momentos culminantes da jornada do usuário: o *Particle Button* disparando micro-fragmentos na aprovação de um pull request ou deploy; o *Slide to Confirm* na liquidação de uma transação financeira; o *Apple Activity Card* na conclusão de metas diárias; ou o *Background Paths* fluindo suavemente na seção Hero da landing page.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Telas Operacionais de Entrada Contínua de Dados em Lote (ex: Digitação de NF-e, Call Centers, ERPs Tradicionais)**:
  Em formulários onde o operador digita centenas de campos por hora usando a tecla `Tab` e `Enter` ininterruptamente, transições de mola, botões que expandem a largura dinamicamente ou cards que se movem provocam fadiga visual e atrasam a produtividade mecânica do usuário.
- **Projetos Legados com React < 18 ou Bundlers sem Suporte Completo a ESM**:
  Os componentes utilizam as versões mais recentes do `motion/react`, hooks como `useId`, `useLayoutEffect` e sintaxes modernas de Tailwind CSS v4. Tentar retroportar esses componentes para stacks legadas acarreta incompatibilidades severas.
- **E-commerces de Varejo de Desconto Massivo ("Flash Sales")**:
  Páginas focadas em conversão por impulso com dezenas de banners piscantes e contadores regressivos colidem frontalmente com a precisão minimalista e o ritmo sóbrio do Kokonut UI.

### ⚠️ A Síndrome do "Gimmick Overload" & Como Evitar o Clichê

O maior perigo ao utilizar bibliotecas focadas em micro-interações táteis é o exibicionismo estético desmedido — adicionar efeitos apenas porque estão disponíveis no catálogo:

1. **Anti-Padrão do Botão de Partículas Onipresente**:
   Nunca atribua o *Particle Button* a ações rotineiras, descartáveis ou frequentes (ex: botões "Fechar Modal", "Cancelar", "Próxima Página"). A explosão física de partículas deve ser reservada com rigor sacramental para conclusões memoráveis: finalizar compra, publicar site, integrar repositório, transferir fundos.
2. **Conflito de Barras Flutuantes e Elementos Sobrepostos**:
   Não coloque simultaneamente uma *Floating Toolbar* ancorada na base da viewport, uma *Morphic Navbar* no topo e uma *Action Search Bar* aberta no centro. Em dispositivos móveis, isso destrói a usabilidade, oculta o conteúdo principal e confunde o foco do leitor de tela.
3. **Ignorar Usuários com Sensibilidade a Movimento**:
   Sempre preserve a condicional de `useReducedMotion()`. Quando o sistema operacional do usuário estiver configurado para movimento reduzido, os componentes Kokonut devem desativar os bursts de partículas, substituir transições de mola por crossfades instantâneos de opacidade e desativar loops contínuos de SVG em background.
4. **Saturação de Rótulos Monoespaçados**:
   O uso de códigos como `BT-01`, `CD-04` e fontes monospace é um recurso de estilo técnico requintado quando aplicado com parcimônia (em cards de engenharia ou dashboards analíticos). Se aplicado em textos descritivos longos ou landing pages institucionais genéricas, torna a leitura truncada e artificial.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão detalhados os 12 componentes mais emblemáticos da arquitetura do Kokonut UI:

---

### 1. AI Prompt Input (`ai-prompt`)
- **Anatomia Visual**: Container integrado para conversação com IA, combinando uma área de texto auto-expansível (`Textarea` com redimensionamento vertical elástico), menu dropdown acoplado para seleção de modelo (ex: Claude 3.5 Sonnet, GPT-4o, Gemini 1.5 Pro) com ícones identificadores, área de inserção de tags/anexos e botão circular de disparo com ícone de seta para cima.
- **Gatilho de Interação**: Digitação, atalho `Enter` para envio (ou `Shift+Enter` para nova linha), atalho `/` para disparar prompts pré-configurados e hover nos badges de arquivos anexados.
- **Onde Encaixar**: Chat central de agentes de IA, barra de comando de copilotos embutidos, rodapé de assistentes flutuantes e editores contextuais generativos.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add @kokonutui/ai-prompt
  # ou via JSON direto:
  npx shadcn@latest add https://kokonutui.com/r/ai-prompt.json
  ```

---

### 2. Action Search Bar (`action-search-bar`)
- **Anatomia Visual**: Barra de busca cinemática de alto desempenho no estilo Raycast / macOS Spotlight. Exibe campo de entrada com ícone de busca em micro-animação, atalhos de teclado contextuais em chips (`⌘K`, `Esc`), sugestões de ação categorizadas com ícones Lucide específicos e breadcrumbs para subpáginas de navegação aninhadas.
- **Gatilho de Interação**: Pressionar `⌘K` ou `Ctrl+K` globalmente abre o diálogo centralizado. Navegação fluida por teclas direcionais (`ArrowUp`, `ArrowDown`), seleção imediata com `Enter` e fechamento com `Escape`. Possui indicador de progresso incorporado na linha quando a ação disparada é assíncrona.
- **Onde Encaixar**: Barra de pesquisa global da aplicação, atalho de cabeçalho em dashboards SaaS ou comando central de navegação rápida em ferramentas de desenvolvedor.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add @kokonutui/action-search-bar
  ```

---

### 3. Particle Button (`BT-01` — `particle-button`)
- **Anatomia Visual**: Botão de status de ação assíncrona com ciclo de vida completo (`idle` ➔ `pending` ➔ `success` / `error`). Seu contorno adapta-se suavemente à largura de cada rótulo via transição de mola. No estado de sucesso, desenha um ícone de verificação via SVG path e dispara uma explosão no topo da borda de 18 partículas estocásticas desenhadas em Canvas que caem com física real. Em caso de falha, aciona uma vibração elástica horizontal suave (`x: [0, -5, 5, -3, 3, 0]`).
- **Gatilho de Interação**: Clique do mouse ou ativação por teclado. Se o manipulador `onClick` retornar uma Promise, o componente gerencia automaticamente a troca entre spinner, sucesso ou erro.
- **Onde Encaixar**: Botão de envio final de formulários de pagamento, botão de "Deploy / Publish" em consoles de cloud, commits em ferramentas git e confirmação de upgrade de plano.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add https://kokonutui.com/r/particle-button.json
  ```

---

### 4. Slide to Confirm (`BT-14` — `slide-to-confirm`)
- **Anatomia Visual**: Trilho horizontal minimalista com bordas arredondadas e uma maçaneta deslizante circular com seta direcional. Conforme o usuário arrasta a maçaneta em direção à extremidade direita, o texto do trilho desvanece suavemente e o preenchimento de fundo avança proporcionalmente ao deslocamento.
- **Gatilho de Interação**: Gesto de arrastar (drag) do mouse ou toque na tela. Se o usuário soltar a maçaneta antes de atingir o limite estipulado (ex: 90% do percurso), ela recua instantaneamente à posição de origem com amortecimento elástico de mola. Ao atingir o limite final, a maçaneta trava, ativa o estado de sucesso e bloqueia novas interações.
- **Onde Encaixar**: Telas de confirmação de transferência de valores (fintechs), exclusão definitiva de clusters/bancos de dados (DevOps) e autorização de ordens de trade em exchanges.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add @kokonutui/slide-to-confirm
  ```

---

### 5. Bento Grid Modular (`bento-grid`)
- **Anatomia Visual**: Estrutura matricial de cards assimétricos com bordas milimétricas em gap contínuo (`gap-px bg-black/[0.13] dark:bg-white/[0.14]`). Cada card do grid suporta span de colunas responsivo (`colSpan: 1 | 2 | 3`), badges de status em tipografia monoespaçada, contadores dinâmicos animados e gráficos sparkline incorporados.
- **Gatilho de Interação**: Hover contextual com leve alteração de luminância de fundo e elevação de detalhes, além de capacidade para rearranjo ou expansão em modais detalhados.
- **Onde Encaixar**: Seção principal de recursos (Features Section) de landing pages de produtos tecnológicos e painéis analíticos com múltiplos KPIs.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add @kokonutui/bento-grid
  ```

---

### 6. Floating Toolbar / Tool Dock (`NV-02` — `toolbar`)
- **Anatomia Visual**: Barra flutuante de ferramentas de edição no estilo Figma / macOS Dock. Apresenta uma cápsula translúcida com desfoque de fundo (`backdrop-blur-md`), agrupamento de ícones por utilidade, e uma plaqueta deslizante de seleção ativa animada por `layoutId` do Motion que se move suavemente de um ícone para o outro.
- **Gatilho de Interação**: Hover com expansão de tooltips revelando atalhos de teclado e clique para fixação de ferramentas ou expansão de popovers aninhados.
- **Onde Encaixar**: Editores visuais, aplicações de desenho vetorial, editores de texto no-code, visualizadores de documentos PDF e painéis de anotação.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add @kokonutui/toolbar
  ```

---

### 7. Card Stack / Throw Deck (`CD-02` — `card-stack`)
- **Anatomia Visual**: Pilha física de cartas sobrepostas em perspectiva de profundidade calculada (escalas decrescentes de `0.95`, `0.90` e rotações angulares estocásticas sutis de ±2 graus). Exibe a carta superior em destaque absoluto enquanto as subjacentes aguardam no baralho.
- **Gatilho de Interação**: Arrastar a carta frontal com o cursor ou gesto de deslizar na tela. Ao ultrapassar o limite angular ou de velocidade de arremesso (flick), a carta é lançada para fora do deck com aceleração inercial e reingressa na base da pilha através de uma rotação cíclica suave.
- **Onde Encaixar**: Seções de depoimentos de clientes (Testimonials), vitrines de templates de design, galerias de portfólio interativas e triagem rápida de notificações.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add https://kokonutui.com/r/card-stack.json
  ```

---

### 8. Apple Activity Card (`CD-04` — `apple-activity-card`)
- **Anatomia Visual**: Card inspirado nos anéis de atividade do Apple Watch. Contém três arcos concêntricos em cores vibrantes de alta saturação (Move em Vermelho Carmesim, Exercise em Verde Neon e Stand em Azul Ciano) sobrepostos a um fundo escuro fosco com métricas numéricas legíveis e legendas em Geist Mono.
- **Gatilho de Interação**: Animação de montagem inicial acionada por `whileInView`, desenhando progressivamente os perímetros dos arcos SVG via `strokeDashoffset` e interpolando os números de 0 até o valor meta. Botão "Replay" para reexecução manual.
- **Onde Encaixar**: Dashboards de saúde física, métricas de produtividade diária em SaaS (ex: tarefas concluídas, tempo focado, reuniões), painéis gamificados e resumos executivos de hábitos.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add https://kokonutui.com/r/apple-activity-card.json
  ```

---

### 9. File Upload Multi-Queue (`IN-01` — `file-upload`)
- **Anatomia Visual**: Zona de upload refinada com suporte a arrastar-e-soltar (drag and drop), ícone central animado, seletor manual de arquivos e uma lista encadeada de arquivos em fila. Cada linha exibe o nome do arquivo, extensão, tamanho formatado, barra de progresso suave em gradiente, botão de repetição (retry) e botão de cancelamento individual.
- **Gatilho de Interação**: Arrastar arquivos sobre o container (com transição elástica da borda tracejada), colar da área de transferência (`paste` event) e clique no botão de cancelamento que emite imediatamente um sinal de interrupção via `AbortController`.
- **Onde Encaixar**: Telas de importação de planilhas CSV, upload de avatares/documentos fiscais, anexação de assets em ferramentas criativas e ingestão de dados em pipelines de IA.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add @kokonutui/file-upload
  ```

---

### 10. Detent Dial (`IN-06` — `detent-dial`)
- **Anatomia Visual**: Seletor rotativo cilíndrico skeuomórfico de precisão inspirado em potenciômetros de estúdios musicais e equipamentos laboratoriais. Possui marcações radiais de graus (`0°` a `360°`), entalhes mecânicos visíveis e leitura numérica instantânea em Geist Mono no núcleo central.
- **Gatilho de Interação**: Rotação com o cursor (clicar e girar circularmente) ou rolagem da roda do mouse (`wheel`). O botão "encaixa" (snap) fisicamente em posições pré-determinadas (detents), simulando cliques táteis via micro-transições angulares de mola.
- **Onde Encaixar**: Ajustes de temperatura e parâmetros de amostragem em modelos de LLM (ex: `temperature: 0.7`, `top_p`), controles de áudio em sintetizadores web, e seletores de ângulo em ferramentas de modelagem gráfica.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add https://kokonutui.com/r/detent-dial.json
  ```

---

### 11. Background Paths (`background-paths`)
- **Anatomia Visual**: Fita fluida de curvas Bézier animadas desenhadas em SVG transparente que cruzam a tela suavemente em três camadas distintas de profundidade com opacidades calibradas (`opacity-20`, `opacity-40`, `opacity-60`). Cria um pano de fundo orgânico e suntuoso sem o peso computacional de WebGL.
- **Gatilho de Interação**: Animação contínua e suave baseada em tempo (`speed`), com resposta sutil ao scroll da página ou posição do mouse.
- **Onde Encaixar**: Seções Hero de landing pages institucionais, telas de apresentação de produtos de software de alto padrão e cabeçalhos de blogs técnicos.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add https://kokonutui.com/r/background-paths.json
  ```

---

### 12. Split-Flap Text (`texts/split-flap-text`)
- **Anatomia Visual**: Display tipográfico cinemático que replica com perfeição os painéis eletromecânicos de partidas e chegadas de aeroportos clássicos e estações de trem (Solari di Udine). Cada caractere é dividido horizontalmente em duas metades com sombra vincada e rotação 3D de flap.
- **Gatilho de Interação**: Mudança de valor de texto aciona o giro cíclico em cascata de todas as placas até estacionarem na nova palavra com atraso estocástico por coluna.
- **Onde Encaixar**: Título principal de landing pages de companhias de viagem, SaaS de cotações financeiras em tempo real, tickers de notícias e anúncios de lançamento de produtos.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add @kokonutui/split-flap-text
  ```

---

## 5. Arquitetura Técnica, Instalação, Física de Movimento & Receitas de Implementação

### Dependências & Setup do Ecossistema

O Kokonut UI opera sobre o ecossistema moderno do React 19 / Next.js 15 e requer a biblioteca `motion` (o novo pacote unificado do Framer Motion v11/v12 acessível via `motion/react`).

Instale as dependências base no seu projeto:
```bash
npm install motion lucide-react class-variance-authority clsx tailwind-merge
```

Configuração recomendada no `components.json` para suportar o namespace nativo do Kokonut UI:
```json
{
  "$schema": "https://ui.shadcn.com/schema.json",
  "style": "default",
  "rsc": true,
  "tsx": true,
  "tailwind": {
    "config": "tailwind.config.ts",
    "css": "app/globals.css",
    "baseColor": "zinc",
    "cssVariables": true
  },
  "aliases": {
    "components": "@/components",
    "utils": "@/lib/utils",
    "ui": "@/components/ui"
  },
  "registries": {
    "@kokonutui": "https://kokonutui.com/r/{name}.json"
  }
}
```

Para conectar seu agente de codificação AI (Claude Code, Cursor ou VS Code) diretamente ao registry via MCP:
```bash
npx shadcn@latest mcp init --client claude
```

---

### Física de Movimento, Amortecimento & Constantes Reais da Biblioteca

Diferente de transições genéricas que usam curvas padrão de CSS (`ease-in-out`), o Kokonut UI utiliza constantes matemáticas rigorosamente afinadas pelo criador:

```typescript
// Curva cúbica quintessencial do Kokonut UI (rápida aceleração inicial com parada suave e precisa):
export const EASE_OUT = [0.23, 1, 0.32, 1] as const;

// Transição padrão para crossfade e rotação de ícones/rótulos:
export const LABEL_TRANSITION = { duration: 0.2, ease: EASE_OUT };

// Transição de mola com bounce zero para expansão/contração elástica de larguras:
export const WIDTH_TRANSITION = { type: "spring", duration: 0.35, bounce: 0 } as const;

// Parâmetros de física para simulação de partículas estocásticas em Canvas:
export const PARTICLE_COUNT = 18;
export const GRAVITY = 0.0016; // Pixels por milissegundo ao quadrado
export const DRAG = 0.0022;    // Fração de velocidade perdida por milissegundo por atrito com o ar
export const LIFETIME = 650;   // Duração de vida do burst em milissegundos
export const BLEED = 64;       // Margem de sangria ao redor do botão para o Canvas desenhar sem cortes
```

---

### Receita de Código Funcional: `ParticleButton` Completo e Produzível

Abaixo está a implementação completa e modular do **Particle Button** (`particle-button.tsx`), refletindo exatamente a arquitetura e a física utilizadas na biblioteca oficial:

```tsx
"use client";

import React, {
  type ComponentProps,
  type MouseEvent,
  type ReactNode,
  useCallback,
  useEffect,
  useLayoutEffect,
  useRef,
  useState,
} from "react";
import {
  AnimatePresence,
  motion,
  useAnimationControls,
  useReducedMotion,
} from "motion/react";
import { Check, AlertCircle, LoaderCircle } from "lucide-react";
import { cn } from "@/lib/utils";

export type ParticleButtonStatus = "idle" | "pending" | "success" | "error";

interface Particle {
  x: number;
  y: number;
  vx: number;
  vy: number;
  angle: number;
  spin: number;
  w: number;
  h: number;
}

const EASE_OUT = [0.23, 1, 0.32, 1] as const;
const LABEL_TRANSITION = { duration: 0.2, ease: EASE_OUT };
const WIDTH_TRANSITION = { type: "spring", duration: 0.35, bounce: 0 } as const;
const SHAKE_ANIMATION = { x: [0, -5, 5, -3, 3, 0] };

const PARTICLE_COUNT = 18;
const GRAVITY = 0.0016;
const DRAG = 0.0022;
const LIFETIME = 650;
const BLEED = 48;

function createParticles(originX: number, width: number): Particle[] {
  return Array.from({ length: PARTICLE_COUNT }, (_, i) => {
    const spread = (Math.random() - 0.5) * Math.min(width, 100);
    const x = Math.min(Math.max(originX + spread, 4), width - 4);
    const side = x < width / 2 ? -1 : 1;
    const speed = 0.18 + Math.random() * 0.22;
    const angle = -Math.PI / 2 + side * Math.random() * 0.85;
    const isChip = i % 3 === 0;

    return {
      x,
      y: 0,
      vx: Math.cos(angle) * speed,
      vy: Math.sin(angle) * speed,
      angle: Math.random() * Math.PI,
      spin: (Math.random() - 0.5) * 0.02,
      w: isChip ? 5 : 3,
      h: isChip ? 2 : 3,
    };
  });
}

function ParticleBurst({
  originX,
  color,
  onDone,
  buttonWidth,
  buttonHeight,
}: {
  originX: number;
  color: string;
  onDone: () => void;
  buttonWidth: number;
  buttonHeight: number;
}) {
  const canvasRef = useRef<HTMLCanvasElement>(null);

  useEffect(() => {
    const canvas = canvasRef.current;
    if (!canvas) return;
    const ctx = canvas.getContext("2d");
    if (!ctx) return;

    const particles = createParticles(originX, buttonWidth);
    const startTime = performance.now();
    let animId: number;

    const render = (now: number) => {
      const elapsed = now - startTime;
      if (elapsed >= LIFETIME) {
        onDone();
        return;
      }

      ctx.clearRect(0, 0, canvas.width, canvas.height);
      const alpha = Math.max(0, 1 - elapsed / LIFETIME);
      ctx.fillStyle = color;
      ctx.globalAlpha = alpha;

      for (const p of particles) {
        const dt = 16.6; // ~60fps step
        p.vx *= 1 - DRAG * dt;
        p.vy += GRAVITY * dt;
        p.x += p.vx * dt;
        p.y += p.vy * dt;
        p.angle += p.spin * dt;

        ctx.save();
        ctx.translate(p.x + BLEED, p.y + BLEED);
        ctx.rotate(p.angle);
        ctx.fillRect(-p.w / 2, -p.h / 2, p.w, p.h);
        ctx.restore();
      }

      animId = requestAnimationFrame(render);
    };

    animId = requestAnimationFrame(render);
    return () => cancelAnimationFrame(animId);
  }, [originX, color, onDone, buttonWidth]);

  return (
    <canvas
      ref={canvasRef}
      width={buttonWidth + BLEED * 2}
      height={buttonHeight + BLEED * 2}
      className="pointer-events-none absolute -left-[48px] -top-[48px] z-50"
      aria-hidden="true"
    />
  );
}

export interface ParticleButtonProps
  extends Omit<ComponentProps<"button">, "onClick" | "children"> {
  children?: ReactNode;
  onClick?: (event: MouseEvent<HTMLButtonElement>) => unknown;
  onSuccess?: () => void;
  onError?: (error: unknown) => void;
  status?: ParticleButtonStatus;
  successDuration?: number;
  errorDuration?: number;
  pendingLabel?: ReactNode;
  successLabel?: ReactNode;
  errorLabel?: ReactNode;
  particles?: boolean;
}

export function ParticleButton({
  children = "Confirm Action",
  onClick,
  onSuccess,
  onError,
  status: controlledStatus,
  successDuration = 1800,
  errorDuration = 2400,
  pendingLabel = "Processing...",
  successLabel = "Completed",
  errorLabel = "Failed",
  particles = true,
  className,
  disabled,
  ...props
}: ParticleButtonProps) {
  const [internalStatus, setInternalStatus] = useState<ParticleButtonStatus>("idle");
  const currentStatus = controlledStatus ?? internalStatus;
  const isReduced = useReducedMotion();
  const controls = useAnimationControls();

  const buttonRef = useRef<HTMLButtonElement>(null);
  const [clickOriginX, setClickOriginX] = useState<number>(0);
  const [buttonDimensions, setButtonDimensions] = useState({ width: 0, height: 0 });
  const [particleColor, setParticleColor] = useState<string>("#1FA834");
  const [showBurst, setShowBurst] = useState<boolean>(false);

  // Mensura as dimensões exatas do botão para posicionar o canvas
  useLayoutEffect(() => {
    if (buttonRef.current) {
      const rect = buttonRef.current.getBoundingClientRect();
      setButtonDimensions({ width: rect.width, height: rect.height });
      const style = window.getComputedStyle(buttonRef.current);
      setParticleColor(style.backgroundColor || "#1FA834");
    }
  }, [currentStatus]);

  const handleClick = async (e: MouseEvent<HTMLButtonElement>) => {
    if (currentStatus !== "idle" || disabled) return;

    if (buttonRef.current) {
      const rect = buttonRef.current.getBoundingClientRect();
      setClickOriginX(e.clientX - rect.left);
    }

    if (!onClick) {
      setInternalStatus("success");
      return;
    }

    try {
      const result = onClick(e);
      if (result instanceof Promise) {
        setInternalStatus("pending");
        await result;
      }
      setInternalStatus("success");
      onSuccess?.();
      if (particles && !isReduced) setShowBurst(true);

      setTimeout(() => {
        setInternalStatus("idle");
      }, successDuration);
    } catch (err) {
      setInternalStatus("error");
      onError?.(err);
      if (!isReduced) {
        controls.start(SHAKE_ANIMATION, { duration: 0.35, ease: EASE_OUT });
      }
      setTimeout(() => {
        setInternalStatus("idle");
      }, errorDuration);
    }
  };

  return (
    <div className="relative inline-block">
      {showBurst && (
        <ParticleBurst
          originX={clickOriginX}
          color={particleColor}
          buttonWidth={buttonDimensions.width}
          buttonHeight={buttonDimensions.height}
          onDone={() => setShowBurst(false)}
        />
      )}

      <motion.button
        ref={buttonRef}
        animate={controls}
        layout={!isReduced}
        transition={WIDTH_TRANSITION}
        onClick={handleClick}
        disabled={disabled || currentStatus === "pending"}
        className={cn(
          "relative inline-flex h-10 items-center justify-center overflow-hidden rounded-md px-4 py-2 font-medium text-sm transition-colors",
          "focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-zinc-400 focus-visible:ring-offset-2",
          "disabled:pointer-events-none disabled:opacity-50",
          currentStatus === "idle" && "bg-black text-white hover:bg-zinc-800 dark:bg-white dark:text-black dark:hover:bg-zinc-100",
          currentStatus === "pending" && "bg-zinc-200 text-zinc-600 dark:bg-zinc-800 dark:text-zinc-300",
          currentStatus === "success" && "bg-[#1FA834] text-white dark:bg-[#3BB44B]",
          currentStatus === "error" && "bg-[#FF2D55] text-white",
          className
        )}
        {...props}
      >
        <AnimatePresence mode="wait" initial={false}>
          {currentStatus === "idle" && (
            <motion.span
              key="idle"
              initial={{ opacity: 0, y: 6 }}
              animate={{ opacity: 1, y: 0 }}
              exit={{ opacity: 0, y: -6 }}
              transition={LABEL_TRANSITION}
              className="flex items-center gap-2"
            >
              {children}
            </motion.span>
          )}

          {currentStatus === "pending" && (
            <motion.span
              key="pending"
              initial={{ opacity: 0, scale: 0.8 }}
              animate={{ opacity: 1, scale: 1 }}
              exit={{ opacity: 0, scale: 0.8 }}
              transition={LABEL_TRANSITION}
              className="flex items-center gap-2"
            >
              <LoaderCircle className="h-4 w-4 animate-spin" />
              <span>{pendingLabel}</span>
            </motion.span>
          )}

          {currentStatus === "success" && (
            <motion.span
              key="success"
              initial={{ opacity: 0, scale: 0.8 }}
              animate={{ opacity: 1, scale: 1 }}
              exit={{ opacity: 0, scale: 0.8 }}
              transition={LABEL_TRANSITION}
              className="flex items-center gap-2 font-medium"
            >
              <Check className="h-4 w-4 stroke-[2.5]" />
              <span>{successLabel}</span>
            </motion.span>
          )}

          {currentStatus === "error" && (
            <motion.span
              key="error"
              initial={{ opacity: 0, scale: 0.8 }}
              animate={{ opacity: 1, scale: 1 }}
              exit={{ opacity: 0, scale: 0.8 }}
              transition={LABEL_TRANSITION}
              className="flex items-center gap-2 font-medium"
            >
              <AlertCircle className="h-4 w-4 stroke-[2.5]" />
              <span>{errorLabel}</span>
            </motion.span>
          )}
        </AnimatePresence>
      </motion.button>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar o Kokonut UI como referência ou biblioteca complementar no arquivo de arquitetura de um novo projeto (`DESIGN_BLUEPRINT.md`), declare os seguintes parâmetros operacionais obrigatórios:

### 1. Definição do Papel no Design System
- **Estatuto**: Biblioteca de Micro-Interações Táteis, Controles Nativos de IA e Navegação Rápida (Camada 30% e 10% do produto).
- **Relacionamento com a Base**: O projeto deve utilizar `shadcn/ui` como fundação estrutural neutra de 60%. Os componentes Kokonut herdam os tokens do `tailwind.config` e utilizam o utilitário `cn()` de `@/lib/utils`.

### 2. Padrão de Nomenclatura & Localização de Arquivos
- Os componentes baixados ou gerados devem residir estritamente no diretório:
  ```
  components/kokonutui/<nome-do-componente>.tsx
  ```
  Exemplo: `components/kokonutui/action-search-bar.tsx`, `components/kokonutui/particle-button.tsx`, `components/kokonutui/ai-prompt.tsx`.

### 3. Governança de Instalação para Agentes Autônomos (AI Prompts)
Declare no blueprint as instruções explícitas de instalação via CLI que os agentes devem executar:
```markdown
### Instalação de Componentes Kokonut UI
Para adicionar componentes desta biblioteca, execute sempre o comando oficial do registry:
- `npx shadcn@latest add @kokonutui/action-search-bar`
- `npx shadcn@latest add @kokonutui/ai-prompt`
- `npx shadcn@latest add @kokonutui/file-upload`
- `npx shadcn@latest add https://kokonutui.com/r/particle-button.json`
```

### 4. Checklist Obrigatório de Conformidade no Blueprint
- [ ] **Acessibilidade de Movimento**: Todo componente com física de partículas ou deslocamento inercial deve verificar `useReducedMotion()` e fornecer fallback imediato estático.
- [ ] **Limitação de Showstoppers**: Não colocar mais de 1 `ParticleButton` ou `SlideToConfirm` na mesma viewport de tela.
- [ ] **Paleta de Status Coerente**: Utilizar `#1FA834` (modo claro) / `#3BB44B` (modo escuro) para estados de confirmação positiva e `#FF2D55` para estados críticos de interrupção ou alerta.
- [ ] **Compatibilidade com Fontes**: Forçar a tipografia Geist Sans para rótulos e Geist Mono para contadores, códigos e metadados de engenharia.
