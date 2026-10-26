---
id: "21st-dev-motion-libraries"
name: "21st.dev Motion Libraries"
url: "https://21st.dev/community/libraries/s/motion"
category: "6-templates"
schema_type: "C-galleries"
dna_estetico: ["Crafted Motion UI", "Tactile Micro-Interactions", "Inertial Spring Physics", "Anti-AI-Slop Curation", "Morphing Layouts (FLIP)", "Bento Spatial Cards", "Subtle Refraction Glassmorphism"]
densidade_informacao: "Media/Narrativa"
impacto_visual: "Editorial/Sofisticado"
custo_computacional: "Medio (Framer Motion / CSS Transforms) a Elevado (SVG Displacement / Snell Optics)"
stack_frameworks: ["React", "Next.js", "TypeScript", "Tailwind CSS", "Motion / Framer Motion (motion.dev)", "Radix UI Primitives", "shadcn/ui CLI Registry", "Lucide React", "21st MCP Protocol"]
compatibilidade:
  fontes_ideais: ["Inter", "Geist Sans", "Geist Mono", "General Sans", "Plus Jakarta Sans", "JetBrains Mono", "Cabinet Grotesk"]
  paletas_ideais:
    - "Dark Void Foundation: #09090b (Zinc 950 base), #121215 (Card Elevated), #18181b (Interactive Surface)"
    - "Light Clean Neutral: #ffffff (Canvas), #f4f4f5 (Zinc 100 Pill), #e4e4e7 (Zinc 200 Border)"
    - "Neon Luminescence Accents: #3b82f6 (Electric Blue), #8b5cf6 (Vibrant Violet), #10b981 (Emerald Spark), #ec4899 (Cyber Pink)"
    - "Micro-Border Bi-directional: rgba(255, 255, 255, 0.08) a rgba(255, 255, 255, 0.16) com top-highlight #27272a"
  combinacoes_recomendadas:
    - "Motion (motion.dev) + Tailwind CSS + clsx/tailwind-merge para animações orquestradas sem repaint"
    - "Radix UI Dialog/Popover/Tooltip como casca acessível combinada com Framer Motion layoutId morphing"
    - "shadcn/ui CLI (`npx shadcn add`) para consumo direto de componentes via URL de registry sem overhead"
    - "21st MCP Server (`https://21st.dev/api/mcp`) para streaming direto de tokens e blocos de código para Cursor e Claude Code"
  conflitos_esteticos:
    - "Transições lineares (`ease-in-out` padrão ou sem amortecimento crítico) que quebram o peso tátil orgânico"
    - "Over-animation / layout shifting desenfreado que causa tontura visual e degrada Core Web Vitals (CLS)"
    - "Bordas pretas puras ou gradientes arco-íris saturados sem atenuação que destroem a sobriedade craft"
    - "Animação de propriedades de layout pesado (`width`, `height`, `top`, `margin`) em vez de `transform` e `opacity`"
    - "Omissão de suporte a `prefers-reduced-motion`, impedindo o uso acessível da interface"
---

# 21st.dev Motion Libraries — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
 ██████╗  ██╗███████╗████████╗   ██████╗ ███████╗██╗   ██╗
██╔════╝ ███║██╔════╝╚══██╔══╝   ██╔══██╗██╔════╝██║   ██║
╚█████╗  ╚██║███████╗   ██║█████╗██║  ██║█████╗  ██║   ██║
 ╚═══██╗  ██║╚════██║   ██║╚════╝██║  ██║██╔══╝  ╚██╗ ██╔╝
██████╔╝  ██║███████║   ██║      ██████╔╝███████╗ ╚████╔╝ 
╚═════╝   ╚═╝╚══════╝   ╚═╝      ╚═════╝ ╚══════╝  ╚═══╝  
       [ MOTION COMPONENT LIBRARIES ECOSYSTEM ]
```

---

## 1. DNA Estético & Filosofia de Curadoria

O **21st.dev** (`https://21st.dev/`), fundado por **Serafim Korablev** (CEO) e **Sergey Bunas**, consolidou-se como o principal hub global e registro descentralizado de componentes React, Tailwind CSS e TypeScript de altíssimo acabamento para o que a plataforma define como a nova **"era do desenvolvimento assistido por agentes de IA"**. Dentro do ecossistema, a curadoria especializada **Motion Libraries** (`https://21st.dev/community/libraries/s/motion`) indexa **43 bibliotecas de ponta** dedicadas à computação gráfica na UI, física de movimento realista e micro-interações táteis.

Diferente de repositórios estáticos de templates prontos ou galerias passivas de screenshot, o índice de Motion Libraries da 21st.dev atua como uma **rede de distribuição atômica**: componentes de código aberto desenvolvidos por engenheiros e designers notáveis da comunidade global são disponibilizados para consumo imediato tanto por humanos quanto por agentes autônomos de código (Cursor, Claude Code, Cline, Windsurf, Codex e Devin).

```
┌────────────────────────────────────────────────────────────────────────┐
│               THE 21ST.DEV AGENTIC MOTION ECOSYSTEM                    │
├────────────────────────────────────────────────────────────────────────┤
│  [ 43 Curated Motion Libs ]  ──►  [ Magic MCP Server ]  ──►  [ AI Agent]│
│   • Aceternity UI (@manuarora)     • Streamable HTTP         • Cursor  │
│   • Magic UI (@dillionverma)       • Semantic UI Search      • Claude  │
│   • Motion Primitives (@ibelick)   • Registry JSON Schema    • Windsurf│
│   • Fancy Components (@danielpetho)• Instant Code Twin       • Cline   │
├────────────────────────────────────────────────────────────────────────┤
│  OUTPUT: Zero AI-Slop, 60fps GPU-Accelerated, Accessible React/Tailwind │
└────────────────────────────────────────────────────────────────────────┘
```

### 1.1 Critérios de Curadoria & Identidade de Marca
O índice de Motion Libraries segue quatro diretrizes conceituais rigorosas:
1. **Motion como Fator de Conexão Cognitiva (Crafted UI)**: A animação não é um adorno pós-produção; ela orienta o foco do usuário através de transferências espaciais contínuas, conservação de volume e estados visuais elásticos.
2. **Arquitetura Aberta Baseada no shadcn/ui Registry Pattern**: Cada componente pode ser copiado em TSX puro ou injetado via CLI (`npx shadcn add "https://21st.dev/r/..."`), garantindo que o desenvolvedor mantenha propriedade total sobre o código (`code ownership`) sem dependências em caixas-pretas proprietárias.
3. **Engenharia Anti-AI-Slop**: Combate à homogeneização da web gerada por modelos de linguagem tradicionais, substituindo botões planos e layouts monótonos por superfícies táteis, reflexos com refração óptica de Snell (como em `Liquid Glass`), botões magnéticos e revelação tipográfica cinética.
4. **Prontidão para Agentes de Código (Magic MCP & CLI Nativo)**: Integração com o protocolo aberto **Model Context Protocol (MCP)** (`https://21st.dev/api/mcp`), permitindo que assistentes analisem semântica de interfaces, propriedades de física e variáveis de tokens em frações de segundo.

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

### 2.1 Papel na Regra 60-30-10 de Design & Movimento
O catálogo de Motion Libraries estabelece uma hierarquia perceptual onde o dinamismo cinético enriquece a experiência sem prejudicar a clareza utilitária:

```
┌────────────────────────────────────────────────────────────────────────┐
│            60-30-10 ARCHITECTURAL MOTION RATIO (21ST.DEV)              │
├────────────────────────────────────────────────────────────────────────┤
│  60%  ESTRUTURA DE NAVEGAÇÃO & TIPOGRAFIA ESTÁVEL                      │
│       Fundos neutros (#09090b ou #ffffff), grid estruturado, leitura   │
│       silenciosa, ausência de movimento contínuo nos blocos de leitura. │
├────────────────────────────────────────────────────────────────────────┤
│  30%  SUPERFÍCIES INTERATIVAS & RESPOSTAS TÁTEIS (Micro-Motion)        │
│       Hover states elásticos, micro-borders que respondem ao cursor,   │
│       segmented docks com layoutId FLIP, accordions com spring physics.│
├────────────────────────────────────────────────────────────────────────┤
│  10%  O IMPACTO CINÉTICO DE ASSINATURA (Hero & Focal Moments)          │
│       Morphing dialogs de tela cheia, lentes líquidas de refração,     │
│       revelações tipográficas cinéticas e partículas dinâmicas no hero.│
└────────────────────────────────────────────────────────────────────────┘
```

- **60% da Interface (Estrutura Silenciosa e Estável)**: Fundo, grid e corpos de texto mantêm-se totalmente legíveis e fixos, sem trepidações ou animações invasivas de scroll.
- **30% da Interface (Micro-Interações Táteis de Suporte)**: Botões com física magnética que acompanham o cursor, pílulas de navegação com transição fluida de seleção via `layoutId`, feedback de cópia com check elástico e expansão de menus via molas amortecidas.
- **10% da Interface (Clímax Cinético)**: O ponto alto da narrativa visual do produto: um card que se expande organicamente para uma modal de tela cheia conservando suas bordas, ou um botão de ação com feixe de luz iridescente em loop perfeitamente calibrado.

### 2.2 Nichos de Projeto Ideais
- **DevTools, Plataformas de Infraestrutura & Agentes de IA**: Interfaces para engenheiros e desenvolvedores que valorizam alta densidade, precisão milimétrica e feedback de terminal ágil.
- **SaaS B2B Moderno & Produtos "Product-Led Growth" (PLG)**: Plataformas com estilo visual no padrão Linear, Raycast, Vercel e Supabase.
- **Portfólios de Design Engineers & Creative Coders**: Apresentação de trabalhos de desenvolvedores front-end seniores que precisam provar domínio sobre shaders, WebGL, SVG displacement e física vetorial.
- **Landing Pages de Alto Ticket & Fintechs Web3**: Produtos digitais cujo valor percebido depende diretamente da sofisticação sensorial e da fluidez de cada clique.

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

### 3.1 ⚠️ Setores Incompatíveis
- **Softwares Críticos de Operação e Finanças Clássicas (Ex: Bloomberg Terminal, ERPs hospitalares)**: Onde qualquer latência perceptual introduzida por animações de layout pode gerar estresse operacional ou lentidão em fluxos contínuos de digitação e atalhos de teclado.
- **Portais Governamentais e Serviços Públicos Universais (WCAG AAA)**: Ambientes com dispositivos de baixa potência gráfica (GPUs integradas antigas, smartphones de entrada) que não toleram cálculo contínuo de matrizes de transformação e filtros SVG.
- **Interfaces Text-Heavy & Leitores Editoriais**: Aplicações focadas em leitura prolongada (blogs densos, documentações acadêmicas), onde elementos em movimento contínuo provocam fadiga ocular e distração.

### 3.2 ⚠️ Armadilhas de Imitação Comuns
1. **Layout Thrashing por Animação de Altura (`height: auto`)**: Tentar animar diretamente a altura de contêineres sem utilizar técnicas de medição de bounding box ou `layoutId` do Motion, causando reflow global em 60fps e derrubando a taxa de quadros.
2. **Overdosing de Springs (Molas Descontroladas)**: Configurar molas com amortecimento muito baixo (`damping < 15`), gerando oscilações borrachudas infinitas que parecem desenhos animados infantis em vez de software de engenharia aeroespacial.
3. **Z-Index Warfare em Componentes com `transform`**: Esquecer que qualquer elemento com propriedade `transform` cria um novo contexto de empilhamento (`stacking context`), quebrando a renderização correta de tooltips, dropdowns e selects nativos.
4. **Desrespeito à Media Query `prefers-reduced-motion`**: Não fornecer variantes de transição instantânea (`duration: 0`) para usuários que sofrem de transtornos vestibulares.

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

```
┌────────────────────────────────────────────────────────────────────────┐
│           21ST.DEV MOTION LIBRARIES LANDSCAPE ARCHITECTURE             │
├────────────────────────────────────────────────────────────────────────┤
│                                                                        │
│  [ GLOBAL HEADER: Micro-Dock Pill / Search Bar / MCP Agent Trigger ]   │
│                                                                        │
│  [ HERO BANNER: Animated Bento Highlights & Spring Interaction Demos ] │
│                                                                        │
│  [ 43 LIBRARY CLUSTERS BY FOUNDATIONAL FLAVOR ]:                       │
│    ├── Morphing & Layout FLIP (Motion Primitives, UI Layouts)          │
│    ├── Marketing Kinetic Delight (Magic UI, Aceternity UI)             │
│    ├── Optical & Physics Shaders (Liquid Glass, ThreeUI)               │
│    ├── Minimalist Craft & Micro-Interactions (Fancy Components, Cult)  │
│    └── Localized & Production Utility Sets (Uai, Joly UI, Forge UI)    │
│                                                                        │
│  [ INTERACTIVE LIVE RUNTIME: Copy TSX / Install via shadcn CLI / MCP ] │
│                                                                        │
│  [ MONOSPACE STATUS FOOTER: Build Info, Registry Metrics, MIT Licenses]│
└────────────────────────────────────────────────────────────────────────┘
```

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo
- **Modularidade Bento com Respiro Respirável**: A disposição de componentes utiliza grids CSS com gap adaptativo (`gap-4 md:gap-6`), empregando `grid-template-columns: repeat(auto-fill, minmax(320px, 1fr))` para acomodar previews interativos sem corte de viewport.
- **Contenção Estrita de Layout (`contain: paint / layout`)**: Componentes de alta intensidade cinética isolam seus nós filhos com `overflow-hidden` e classes de contenção visual, prevenindo que repaints de gradientes afetem o fluxo do documento principal.
- **Régua de 1px Subpixel**: Divisórias e contornos de cartões operam na espessura de 1px com semi-transparência (`border border-border/60` ou `rgba(255, 255, 255, 0.08)`), destacando o conteúdo interno e mantendo a sensação tátil.

### 4.2 Sistemas de Cores, Superfícies & Texturas
- **Fundos Noturnos Escavados (Deep Zinc)**: Base em `#09090b` (zinc-950) com cartões elevados em `#121215` ou `rgba(255, 255, 255, 0.02)`.
- **Refração e Lentes Ópticas (Snell's Law Optics)**: Implementada por bibliotecas como `@avenra/liquid-glass`, emprega filtros SVG de deslocamento (`feDisplacementMap` + `feTurbulence`) e curvaturas convexas que distorcem o conteúdo subjacente de acordo com o índice de refração do vidro físico real.
- **Bordas Dinâmicas de Feixe (Beam/Shimmer Borders)**: Gradientes angulares em rotação contínua (`conic-gradient`) combinados com máscaras CSS para criar um contorno luminoso de 1 pixel que percorre os limites do contêiner.

---

### 4.3 Catálogo de Arquétipos & Componentes Notáveis do 21st.dev Motion

Abaixo está o mapeamento detalhado de 12 arquétipos fundamentais extraídos das 43 bibliotecas de movimento do ecossistema:

| # | Arquétipo / Componente | Biblioteca de Origem & Autor | Anatomia & Comportamento Mecânico | Gatilho & Física de Interação | Onde Encaixar no Projeto |
|---|------------------------|------------------------------|-----------------------------------|-------------------------------|--------------------------|
| 1 | **Morphing Dialog (Expandable Card)** | **Motion Primitives** (`@ibelick`) | Card compacto que se transmuta sem emendas em uma janela modal centralizada, compartilhando o mesmo `layoutId`. O conteúdo interno revela textos adicionais com stagger suave. | Clique do usuário. Mola de alta densidade (`stiffness: 300, damping: 30`). Tecla Esc ou clique fora para retração elástica reversa. | Vitrines de casos de estudo, grades de produtos, detalhes de planos de assinatura. |
| 2 | **Interactive Bento 3D Tilt Card** | **Magic UI** (`@dillionverma`) | Cartão com perspectiva CSS (`perspective: 1000px`) cuja matriz tridimensional oscila sutilmente conforme a posição do ponteiro do mouse, projetando luz especular radial. | `onMouseMove` com mapeamento angular linear restrito a `[-10deg, 10deg]`. Retorno suave ao centro em `onMouseLeave`. | Seção de recursos principais (Features), cards de funcionalidades de IA em SaaS. |
| 3 | **Liquid Glass Refraction Lens** | **Liquid Glass** (`@devsam7t3`) | Lente convexa baseada em física que aplica refração da Lei de Snell através de um filtro SVG dinâmico, simulando aberração cromática e reflexos internos de vidro líquido real. | Movimento do cursor ou drag tátil do usuário. Molas inerciais com conservação de momentum. | Badges flutuantes, barras de status dinâmicas, cursor magnético experimental. |
| 4 | **Floating Island Segmented Dock** | **UI Layouts** (`@uilayout.contact`) | Barra de navegação em cápsula flutuante (`backdrop-blur-md`) onde o cursor ao passar sobre os ícones gera ampliação escalonada (efeito fisheye inspirado no macOS Dock). | Hover contínuo com interpolação de distância euclidiana via `useMotionValue` e `useTransform`. | Menu de navegação primário inferior para web apps e dashboards modernos. |
| 5 | **Text Scramble & Kinetic Reveal** | **Fancy Components** (`@danielpetho`) | Tipografia monoespaçada que, ao entrar na viewport ou receber foco, substitui ciclicamente caracteres aleatórios até convergir para a palavra final. | `whileInView` ou hover sobre títulos. Temporizador em ticks de 30ms com conjunto de caracteres alfa-numéricos e símbolos. | Títulos heróicos (H1), chamadas para ação em DevTools e terminais web. |
| 6 | **Spotlight Radial Glow Card** | **Aceternity UI** (`@manuarora700`) | Contêiner escuro com borda sutil cujo gradiente radial semitransparente segue o ponteiro do mouse em coordenadas relativas, revelando bordas ocultas em tempo real. | `onMouseMove` calculando `clientX - left` e `clientY - top`. Interpolação via variáveis CSS nativas `--mouse-x` e `--mouse-y`. | Seções de precificação (Pricing Cards) e matriz de especificações técnicas. |
| 7 | **Infinite Velocity Marquee** | **Magic UI** (`@dillionverma`) | Carrossel horizontal contínuo de logotipos ou cartões que ajusta sua velocidade de rotação com base na aceleração da rolagem da página do usuário. | Interseção com `useScroll` e `useVelocity`. Deslocamento acelerado proporcional à velocidade de rolagem do leitor. | Prova social (Wall of Love), logotipos de parceiros e clientes corporativos. |
| 8 | **Magnetic Spring Follower Button** | **Cult UI** (`@cult-ui`) / **Fancy Components** | Botão cujo centroide é puxado em direção ao ponteiro do mouse quando o cursor se aproxima do seu raio magnético de captura, retornando elásticamente. | Detecção de proximidade com mola rápida (`stiffness: 400, damping: 25`). O texto e o invólucro possuem fatores de deslocamento distintos. | Botão de Conversão Principal (CTA Hero) e links de contato de portfólio. |
| 9 | **Progressive Path Drawing Stepper** | **Animata** (`@hari`) / **Motion Primitives** | Linha vetorial vertical ou horizontal que se desenha com `pathLength` animado conforme o usuário avança entre etapas de um fluxo de configuração. | Estado do formulário ou scroll progressivo. Mola amortecida que preenche a linha até a coordenada do próximo nó. | Fluxos de Onboarding interativo, cronogramas de lançamento (Roadmaps). |
| 10 | **Drag-to-Dismiss Mobile Drawer** | **SmoothUI** (`@educalvolpz`) / **Uai** (`@victor-teles`) | Gaveta modal que sobe do rodapé da tela em dispositivos móveis, permitindo fechamento por arrasto inercial descendente com limite de resistência elástica. | Gesto tátil de arraste (`drag="y"`, `dragConstraints={{ top: 0 }}`). Se arrastado além de 100px com velocidade negativa, aciona fechamento. | Seletores móveis, menus contextuais, interfaces brasileiras (Pix/CEP via Uai). |
| 11 | **Iridescent Shimmer Border Button** | **Magic UI** / **Aceternity UI** | Botão oval ou retangular que possui um anel externo brilhante em rotação perpétua de 360 graus sob uma máscara interna de fundo sólido. | Animação CSS em GPU (`conic-gradient` rotacionado por `@keyframes`) sem consumo de thread principal do JS. | Botão secundário de assinatura Pro e chamadas de upgrade de plano. |
| 12 | **Fluid Tab Underline Switcher** | **Motion Primitives** (`@ibelick`) | Conjunto de abas onde o indicador de aba ativa (pílula sólida ou sublinhado) desliza horizontalmente de forma contínua entre abas de diferentes larguras. | Clique ou foco via teclado. `layoutId="activeTabIndicator"` com mola elástica suave (`stiffness: 500, damping: 35`). | Segmentadores de painéis, filtros de catálogo e alternadores de visualização de código. |

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Tokens CSS & Variáveis de Assinatura
Para materializar a linguagem das Motion Libraries do 21st.dev em qualquer projeto React/Tailwind, adicione estas definições ao seu arquivo global de CSS ou configuração de Tailwind:

```css
@layer base {
  :root {
    --motion-bg: 240 10% 3.9%;
    --motion-card: 240 10% 6%;
    --motion-card-hover: 240 10% 8.5%;
    --motion-border-dim: 240 3.7% 15.9%;
    --motion-border-bright: 240 4.8% 25%;
    --motion-accent: 217.2 91.2% 59.8%;
    --motion-glow: 263.4 70% 50.4%;

    /* Física de Curvas de Referência */
    --ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);
    --ease-in-out-smooth: cubic-bezier(0.65, 0, 0.35, 1);
  }
}

@keyframes spinConic {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

.animate-spin-conic {
  animation: spinConic 4s linear infinite;
}

@keyframes shimmerSweep {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(100%);
  }
}

.animate-shimmer-sweep {
  animation: shimmerSweep 2.2s cubic-bezier(0.16, 1, 0.3, 1) infinite;
}
```

### 5.2 Física de Movimento & Transições
O ecossistema 21st.dev diferencia-se de animações CSS convencionais pelo uso sistemático de **física newtoniana de molas (Spring Physics)** calculada no tempo real de frame:

- **Mola de Interação Tátil Rápida (Botões, Toggles, Badges)**:
  - `stiffness: 400`, `damping: 25`, `mass: 0.8` (Snappy, assertivo, sem latência).
- **Mola de Transição de Layout FLIP (Expandable Cards, Abas, Docks)**:
  - `stiffness: 320`, `damping: 30`, `mass: 1.0` (Orgânico, peso natural, sem overshoot excessivo).
- **Mola Flutuante Suave (Modais, Drawers, Telas Cheias)**:
  - `stiffness: 220`, `damping: 28`, `mass: 1.2` (Elegante, desaceleração cinematográfica).
- **Curva Exponencial para Transições Numéricas e Opacidade**:
  - `cubic-bezier(0.16, 1, 0.3, 1)` (Desaceleração rápida no início, ancoragem suave no fim).

---

### 5.3 Implementação Funcional Completa em React + Tailwind + Framer Motion

O componente abaixo apresenta uma implementação de grau de produção do padrão **Morphing Dialog Card** (padrão consagrado por `@ibelick` em Motion Primitives e refinado no ecossistema 21st.dev). Ele implementa conservação geométrica com `layoutId`, gerenciamento acessível de foco com tecla `Escape`, prevenção de layout shift, backdrop blur cinemático e física elástica calibrada:

```tsx
import React, { useState, useEffect, useRef } from "react";
import { motion, AnimatePresence } from "framer-motion";
import { X, ArrowRight, Sparkles, Terminal, Layers, Cpu, Check } from "lucide-react";

export interface MotionLibraryCardData {
  id: string;
  title: string;
  author: string;
  authorHandle: string;
  authorAvatar: string;
  description: string;
  fullContent: string;
  installCommand: string;
  tags: string[];
  componentsCount: number;
  highlightMetric: string;
}

export const sampleLibraries: MotionLibraryCardData[] = [
  {
    id: "motion-primitives",
    title: "Motion Primitives",
    author: "Julien Thibeaut",
    authorHandle: "@ibelick",
    authorAvatar: "https://images.unsplash.com/photo-1534528741775-53994a69daeb?w=100&h=100&fit=crop&crop=faces",
    description: "Componentes de movimento elementares, morphing dialogs e transições de layout em física pura.",
    fullContent: "Motion Primitives é uma biblioteca modular focada em fornecer as peças fundamentais de animação que faltam nas suítes convencionais. Constrói morphings estruturais fluidos onde contêineres e imagens transferem geometria sem quebra de hierarquia DOM.",
    installCommand: "npx shadcn@latest add \"https://21st.dev/r/ibelick/motion-primitives\"",
    tags: ["Morphing", "FLIP Layout", "Springs", "Micro-UX"],
    componentsCount: 32,
    highlightMetric: "450k+ views",
  },
  {
    id: "liquid-glass",
    title: "Liquid Glass",
    author: "Dev Sam",
    authorHandle: "@devsam7t3",
    authorAvatar: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=100&h=100&fit=crop&crop=faces",
    description: "Lentes de vidro baseadas na física óptica da Lei de Snell com refração e dispersão espectral.",
    fullContent: "Desenvolvida com filtros SVG nativos combinados a transições por mola, Liquid Glass reproduz o comportamento óptico do vidro orgânico no navegador sem o peso de motores WebGL proprietários. A distorção reage à aceleração do mouse.",
    installCommand: "npx shadcn@latest add \"https://21st.dev/r/devsam7t3/liquid-glass\"",
    tags: ["Physics", "Snell Law", "SVG Optics", "Dynamic Glass"],
    componentsCount: 12,
    highlightMetric: "98k+ views",
  },
  {
    id: "fancy-components",
    title: "Fancy Components",
    author: "Daniel Petho",
    authorHandle: "@danielpetho",
    authorAvatar: "https://images.unsplash.com/photo-1500648767791-00dcc994a43e?w=100&h=100&fit=crop&crop=faces",
    description: "Micro-interações de ponta, botões magnéticos, scramblers tipográficos e efeitos analógicos.",
    fullContent: "Fancy Components é uma suíte de refinamentos táteis concebida para elevar interfaces funcionais ao status de design premiado. Apresenta controles reativos ao cursor, text scramblers para terminais de IA e botões com amortecimento inercial.",
    installCommand: "npx shadcn@latest add \"https://21st.dev/r/danielpetho/fancy-components\"",
    tags: ["Kinetic Typography", "Magnetic", "DevTools UI"],
    componentsCount: 48,
    highlightMetric: "320k+ views",
  },
];

export const MotionMorphingShowcase: React.FC = () => {
  const [selectedCard, setSelectedCard] = useState<MotionLibraryCardData | null>(null);
  const [copiedId, setCopiedId] = useState<string | null>(null);

  // Fechar com tecla Escape
  useEffect(() => {
    const handleKeyDown = (e: KeyboardEvent) => {
      if (e.key === "Escape") {
        setSelectedCard(null);
      }
    };
    window.addEventListener("keydown", handleKeyDown);
    return () => window.removeEventListener("keydown", handleKeyDown);
  }, []);

  const handleCopy = (command: string, id: string) => {
    navigator.clipboard.writeText(command);
    setCopiedId(id);
    setTimeout(() => setCopiedId(null), 2200);
  };

  return (
    <div className="relative w-full min-h-[640px] bg-[#09090b] text-zinc-100 p-6 md:p-10 font-sans selection:bg-blue-500/30 selection:text-white rounded-3xl border border-zinc-800/80 overflow-hidden shadow-2xl">
      {/* Luz ambiente de fundo */}
      <div 
        className="pointer-events-none absolute -top-32 left-1/2 -translate-x-1/2 w-[700px] h-[350px] opacity-20 blur-[140px] rounded-full"
        style={{ background: "radial-gradient(circle, #3b82f6 0%, #8b5cf6 50%, transparent 80%)" }}
      />

      {/* Cabeçalho da Seção */}
      <div className="relative z-10 max-w-4xl mx-auto mb-10 text-center">
        <div className="inline-flex items-center gap-2 px-3 py-1 rounded-full border border-zinc-800 bg-zinc-900/80 text-xs font-medium text-zinc-400 mb-4 backdrop-blur-md">
          <Sparkles className="w-3.5 h-3.5 text-blue-400" />
          <span>Curadoria 21st.dev · 43 Motion Libraries</span>
        </div>
        <h2 className="text-3xl md:text-4xl font-bold tracking-tight text-white mb-3">
          Micro-Interações & Física Orgânica de Layout
        </h2>
        <p className="text-zinc-400 text-sm md:text-base max-w-xl mx-auto leading-relaxed">
          Clique em qualquer cartão para experimentar a transferência espacial contínua (<code className="text-xs bg-zinc-800/80 px-1.5 py-0.5 rounded text-blue-300 font-mono">layoutId</code>) sem reflow de documento.
        </p>
      </div>

      {/* Grade de Cartões Bento com Morphing */}
      <div className="relative z-10 max-w-5xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-5">
        {sampleLibraries.map((lib) => (
          <motion.div
            key={lib.id}
            layoutId={`card-container-${lib.id}`}
            onClick={() => setSelectedCard(lib)}
            className="group relative flex flex-col justify-between p-5 rounded-2xl bg-zinc-900/60 hover:bg-zinc-900/90 border border-zinc-800/80 hover:border-zinc-700/80 transition-colors duration-300 cursor-pointer overflow-hidden backdrop-blur-sm shadow-lg hover:shadow-blue-950/20"
            transition={{
              type: "spring",
              stiffness: 340,
              damping: 30,
            }}
          >
            {/* Top Bar do Card */}
            <div>
              <div className="flex items-center justify-between mb-4">
                <div className="flex items-center gap-2.5">
                  <img
                    src={lib.authorAvatar}
                    alt={lib.author}
                    className="w-8 h-8 rounded-full border border-zinc-700/60 object-cover"
                  />
                  <div>
                    <h3 className="text-sm font-semibold text-white group-hover:text-blue-400 transition-colors">
                      {lib.title}
                    </h3>
                    <span className="text-xs text-zinc-500 font-mono">{lib.authorHandle}</span>
                  </div>
                </div>
                <span className="text-[11px] font-mono font-medium px-2 py-0.5 rounded bg-zinc-800/80 text-zinc-400 border border-zinc-700/40">
                  {lib.componentsCount} ui
                </span>
              </div>

              <motion.p 
                layoutId={`card-desc-${lib.id}`}
                className="text-xs text-zinc-400 leading-relaxed mb-5 line-clamp-3"
              >
                {lib.description}
              </motion.p>
            </div>

            {/* Rodapé do Card */}
            <div className="pt-3 border-t border-zinc-800/60 flex items-center justify-between text-xs">
              <span className="text-[11px] text-zinc-500 font-medium">{lib.highlightMetric}</span>
              <span className="inline-flex items-center gap-1 text-blue-400 font-semibold group-hover:translate-x-1 transition-transform duration-200">
                <span>Explorar</span>
                <ArrowRight className="w-3.5 h-3.5" />
              </span>
            </div>
          </motion.div>
        ))}
      </div>

      {/* Modal Expandida (Morphing Dialog Target) */}
      <AnimatePresence>
        {selectedCard && (
          <div className="fixed inset-0 z-50 flex items-center justify-center p-4 sm:p-6">
            {/* Backdrop com Blur Gradual */}
            <motion.div
              initial={{ opacity: 0 }}
              animate={{ opacity: 1 }}
              exit={{ opacity: 0 }}
              transition={{ duration: 0.25, ease: "easeOut" }}
              onClick={() => setSelectedCard(null)}
              className="absolute inset-0 bg-black/70 backdrop-blur-md"
            />

            {/* Conteúdo Expandido com Preservação de Geometria */}
            <motion.div
              layoutId={`card-container-${selectedCard.id}`}
              className="relative w-full max-w-xl bg-zinc-900 border border-zinc-700/80 rounded-3xl p-6 md:p-8 shadow-2xl text-zinc-100 z-10 overflow-hidden"
              transition={{
                type: "spring",
                stiffness: 300,
                damping: 28,
              }}
            >
              {/* Botão de Fechar */}
              <button
                onClick={() => setSelectedCard(null)}
                aria-label="Fechar diálogo"
                className="absolute top-5 right-5 p-2 rounded-full bg-zinc-800/80 hover:bg-zinc-700 text-zinc-400 hover:text-white transition-colors border border-zinc-700/50"
              >
                <X className="w-4 h-4" />
              </button>

              {/* Informações do Autor e Título */}
              <div className="flex items-center gap-3 mb-5">
                <img
                  src={selectedCard.authorAvatar}
                  alt={selectedCard.author}
                  className="w-12 h-12 rounded-full border border-zinc-600 object-cover"
                />
                <div>
                  <h3 className="text-xl font-bold text-white flex items-center gap-2">
                    {selectedCard.title}
                  </h3>
                  <p className="text-xs text-zinc-400 font-mono">
                    Criado por {selectedCard.author} ({selectedCard.authorHandle})
                  </p>
                </div>
              </div>

              {/* Tags de Categoria */}
              <div className="flex flex-wrap gap-1.5 mb-6">
                {selectedCard.tags.map((tag) => (
                  <span
                    key={tag}
                    className="text-[11px] font-medium px-2.5 py-0.5 rounded-full bg-blue-500/10 text-blue-400 border border-blue-500/20"
                  >
                    {tag}
                  </span>
                ))}
              </div>

              {/* Texto Expandido */}
              <motion.div
                initial={{ opacity: 0, y: 10 }}
                animate={{ opacity: 1, y: 0 }}
                transition={{ delay: 0.1, duration: 0.3 }}
                className="mb-6 space-y-3"
              >
                <p className="text-sm text-zinc-300 leading-relaxed font-normal">
                  {selectedCard.fullContent}
                </p>
              </motion.div>

              {/* Bloco de Código shadcn CLI de 1 Clique */}
              <div className="rounded-xl bg-zinc-950 border border-zinc-800 p-3.5 mb-6">
                <div className="flex items-center justify-between text-xs text-zinc-400 mb-2">
                  <span className="flex items-center gap-1.5 font-mono text-[11px] text-zinc-400">
                    <Terminal className="w-3.5 h-3.5 text-emerald-400" />
                    <span>Instalação via shadcn CLI</span>
                  </span>
                  <button
                    onClick={() => handleCopy(selectedCard.installCommand, selectedCard.id)}
                    className="inline-flex items-center gap-1 px-2.5 py-1 rounded bg-zinc-800 hover:bg-zinc-700 text-zinc-200 transition-colors text-[11px] font-medium cursor-pointer"
                  >
                    {copiedId === selectedCard.id ? (
                      <>
                        <Check className="w-3 h-3 text-emerald-400" />
                        <span className="text-emerald-400">Copiado!</span>
                      </>
                    ) : (
                      <span>Copiar CLI</span>
                    )}
                  </button>
                </div>
                <pre className="text-xs font-mono text-zinc-300 overflow-x-auto whitespace-pre-wrap break-all select-all">
                  {selectedCard.installCommand}
                </pre>
              </div>

              {/* Ações Inferiores */}
              <div className="flex items-center justify-between pt-2">
                <span className="text-xs text-zinc-500 font-mono">
                  {selectedCard.componentsCount} componentes de movimento prontos
                </span>
                <button
                  onClick={() => setSelectedCard(null)}
                  className="px-5 py-2 text-xs font-semibold rounded-lg bg-zinc-100 hover:bg-white text-zinc-950 transition-colors shadow-sm cursor-pointer"
                >
                  Concluído
                </button>
              </div>
            </motion.div>
          </div>
        )}
      </AnimatePresence>
    </div>
  );
};

export default MotionMorphingShowcase;
```

---

### 5.4 Como a IA Deve Pesquisar ao Vivo no 21st.dev

Quando um agente autônomo (Claude Code, Cursor, Windsurf ou Devin) necessitar consultar o índice ao vivo para buscar bibliotecas de movimento ou extrair novos componentes, ele deve seguir os seguintes pontos de entrada oficiais:

1. **Protocolo Nativo Magic MCP (Model Context Protocol)**:
   - Endpoint Streamable HTTP (com chave ou OAuth): `https://21st.dev/api/mcp`
   - Endpoint Read-Only aberto para consulta rápida: `https://21st.dev/api/mcp/readonly`
   - Comando CLI para inicialização em 1 linha:
     ```bash
     npx @21st-dev/cli@latest init --client <cursor|claude|codex|vscode|devin> [--write]
     ```
2. **Estrutura de URLs Diretas para Navegação e Resolução**:
   - Índice de bibliotecas de movimento: `https://21st.dev/community/libraries/s/motion`
   - Busca semântica por componentes animados: `https://21st.dev/community/components?q=<termo-de-busca>` (ex: `q=magnetic+button` ou `q=morphing+dialog`)
   - Visualização de componente individual em Markdown leve: enviar cabeçalho `Accept: text/markdown` ou adicionar `.md` na rota: `https://21st.dev/@<autor>/components/<slug>.md`
   - Índice completo do autor: `https://21st.dev/@<autor>`
   - Documento de descoberta de agentes (ARD): `https://21st.dev/.well-known/ard.json` e `https://21st.dev/llms.txt`.
3. **Padrão de Injeção no Projeto via shadcn CLI**:
   - Os componentes do 21st.dev seguem estritamente a especificação de registro do shadcn. Qualquer componente de qualquer autor pode ser injetado diretamente no repositório local sem instalação manual de dependências npm globais:
     ```bash
     npx shadcn@latest add "https://21st.dev/r/@<autor>/<slug-do-componente>"
     ```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao adotar o **21st.dev Motion Libraries** como a espinha dorsal de micro-interações e física de movimento para um novo produto digital, certifique-se de validar os seguintes requisitos no `DESIGN_BLUEPRINT.md`:

### Checklist de Engenharia de Movimento & Direção de Arte
- [ ] **Configuração da Stack Base**: Confirmar presença de `motion` (ou `framer-motion`), `clsx`, `tailwind-merge` e ícones `lucide-react` no `package.json`.
- [ ] **Aceleração Exclusiva por GPU**:
  - Toda e qualquer animação deve atuar estritamente sobre propriedades de transformação geométrica (`transform: translate3d, scale, rotate`) e canal alfa (`opacity`).
  - Proibir categoricamente a interpolação de `width`, `height`, `top`, `left`, `margin` ou `padding` fora do motor FLIP (`layoutId`).
- [ ] **Padronização das Constantes de Mola**:
  - Evitar valores aleatórios de animação em cada componente. Centralizar os objetos de configuração de spring em um arquivo de tokens (`src/lib/motion-tokens.ts`):
    - `SPRING_SNAPPY`: `{ type: "spring", stiffness: 400, damping: 25, mass: 0.8 }`
    - `SPRING_MORPH`: `{ type: "spring", stiffness: 320, damping: 30, mass: 1.0 }`
    - `SPRING_MODAL`: `{ type: "spring", stiffness: 220, damping: 28, mass: 1.2 }`
- [ ] **Acessibilidade Universal (WCAG 2.2 Nível AA)**:
  - Implementar o hook `useReducedMotion()` do Framer Motion em contêineres principais:
    ```tsx
    const shouldReduceMotion = useReducedMotion();
    const transition = shouldReduceMotion ? { duration: 0 } : SPRING_MORPH;
    ```
  - Assegurar que todas as modais e gavetas expansíveis capturem o foco com `Tab` e respondam à tecla `Escape`.
- [ ] **Zero Cumulative Layout Shift (CLS = 0)**:
  - Garantir que contêineres que recebem carregamento dinâmico ou scramblers tipográficos possuam alturas mínimas (`min-h-[...]`) e reservas espaciais predefinidas.
- [ ] **Estratégia de Integração via CLI**:
  - Priorizar a instalação de blocos pelo comando oficial `npx shadcn@latest add "https://21st.dev/r/..."` para garantir modularidade no diretório `components/ui/` do projeto.
