---
id: "snapcn-dev"
name: "Snapcn"
url: "https://snapcn.dev/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Programmatic Video UI", "Kinetic Motion Typography", "Timeline-Driven Shadcn Primitives", "Realistic Device & Cursor Simulation", "AI-Agent Orchestrated Media"]
densidade_informacao: "Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Alto (Remotion Frame-by-Frame Rendering / Canvas WebGL / MP4 Output)"
stack_frameworks: ["React 19 / React 18", "Remotion (@remotion/core, @remotion/player, @remotion/cli)", "Tailwind CSS (v3 / v4)", "shadcn/ui Registry Architecture", "TypeScript", "Lucide React"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Geist Mono", "Inter", "Caveat (Handwritten annotations)", "JetBrains Mono"]
  paletas_ideais: ["Modern Dark Craft (Zinc 950 / Black)", "High-Contrast Monochrome", "Spotlight Neon Glow Accents (Sky 400 / Emerald 500 / Violet 500)", "Subtle Glass Muted Borders"]
  combinacoes_recomendadas: ["shadcn/ui", "Remotion", "Radix UI Primitives", "Cult UI", "SmoothUI", "Number Flow"]
  conflitos_esteticos: ["Animações CSS lineares dessincronizadas do relógio de quadros", "Interfaces estáticas sem cadência rítmica", "Neumorfismo difuso com blur descontrolado", "Templates de vídeo estilo banco de stock genérico dos anos 2010"]
---

# Snapcn — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Snapcn** (`snapcn.dev`) representa uma evolução de paradigma no ecossistema front-end moderno: **é o primeiro registro no padrão shadcn/ui projetado especificamente para vídeo programático e animação determinística em React**, sustentado pelo motor do **Remotion** e estilizado com a precisão atômica do **Tailwind CSS**.

Enquanto a maioria das bibliotecas de UI tradicionais se limita à navegação estática ou a transições acionadas exclusivamente por cliques e eventos assíncronos do DOM, o Snapcn transpõe o design system de uma aplicação web diretamente para a **linha do tempo (timeline-driven computing)**. Cada componente é uma função pura do número do quadro atual (`useCurrentFrame()`), garantindo que animações complexas de lançamento de produto, demonstrações de software, tipografia cinética e gravações de tela simuladas sejam reproduzidas com fidelidade absoluta de 60 FPS, tanto em navegadores quanto em pipelines de renderização headless em nuvem (como Remotion Lambda ou CI/CD de MP4).

### Os Pilares da Assinatura Visual do Snapcn:

1. **Continuidade de Código entre Aplicação e Vídeo (Single Source of Truth UI)**:
   Tradicionalmente, a criação de vídeos de lançamento ou demos exigia ferramentas como After Effects, Cinema 4D ou Screen Studio, gerando um abismo imediato entre a UI real do produto e o vídeo promocional. O Snapcn resolve essa dissociação permitindo que os próprios componentes de tela (`Button`, `Input`, `Dialog`, `Avatar`, `Terminal`) compartilhem os mesmos tokens Tailwind, classes utilitárias e estrutura TSX do produto real, encapsulados em composições temporais ricas.

2. **Física Temporal Determinística & Interpolações Baseadas em Quadros**:
   Ao contrário de transições CSS sujeitas a gargalos de CPU e oscilações de taxa de quadros (*frame stutter*), o Snapcn utiliza a física matemática de molas do Remotion (`spring({ frame, fps, config: { damping, mass, stiffness } })`) e interpolações lineares e cúbicas com clamp rígido (`interpolate(frame, [...], [...], { extrapolateRight: 'clamp' })`). O movimento é perfeitamente reproduzível e reprojetável em qualquer escala de tempo ou resolução (de 1080p a 4K).

3. **Simulação Hiper-Realista de Interações Digitais (Cursor, Teclado e Câmera Virtual)**:
   Os componentes de visualização de tela do Snapcn recriam minuciosamente o ecossistema tátil de sistemas operacionais modernos:
   - Cursores de mouse dinâmicos que percorrem trajetórias curvas suaves até botões, acionando o estado de hover e uma deformação tátil realista no clique (*ripple/scale down*).
   - Terminais de desenvolvedor com animação de digitação em ritmo orgânico (com desvio estatístico de atraso entre teclas), cursores piscantes e fluxo de saída colorido com realce ANSI.
   - Molduras vetoriais de dispositivos (MacBook, iPhone com Dynamic Island) que realizam movimentos de câmera virtual, rotação em perspectiva 3D (`rotateX`, `rotateY`, `scale`) e aproximações focais (*Ken Burns digital*) sobre pontos de interesse da UI.

4. **Nativo para Agentes de Inteligência Artificial & Arquitetura MCP**:
   O Snapcn foi construído com a premissa de orquestração autônoma. Ele oferece integração nativa com o **Model Context Protocol (MCP)** e uma **Agent Skill** (`npx skills add snapcndev/snapcn`), permitindo que agentes de codificação (como Claude Code, Cursor e Windsurf) inspecionem o registro de componentes, calculem orçamentos temporais em quadros, configurem propriedades tipadas e componham vídeos completos a partir de especificações em linguagem natural.

5. **Distribuição Aberta e Soberania Total de Código**:
   Seguindo à risca a arquitetura shadcn CLI (`npx shadcn@latest add @snapcn/<component>`), os componentes não são instalados como uma biblioteca binária opaca e engessada no `node_modules`. O código-fonte integral TypeScript/Tailwind é baixado diretamente na árvore de arquivos do projeto (`src/components/snap-cn/...`), possibilitando customização cirúrgica de timing, cores, curvas de aceleração e layouts.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários

1. **Vídeos de Lançamento de Software & Campanha de Product Hunt (Launch Reels)**:
   Startups de SaaS B2B, plataformas de IA e ferramentas de produtividade que necessitam de vídeos de anúncio com visual refinado, cortes sincronizados, tipografia cinética de impacto e demonstração clara da interface em menos de 60 segundos.
2. **Demonstrações Interativas e Hero Sections com Player Embutido (`@remotion/player`)**:
   Landing pages de alto padrão que desejam substituir gravações de tela pesadas (vídeos MP4 comuns de 50MB ou GIFs com artefatos de compressão) por um player interativo React nativo de menos de 100KB, executando componentes vetoriais em tempo real com controle de play/pause pelo visitante.
3. **Geração Automatizada de Vídeos em Lote (Programmatic Video SaaS)**:
   Plataformas que geram vídeos personalizados para clientes em escala — como relatórios mensais dinâmicos em vídeo, resumos anuais de atividade (estilo Spotify Wrapped para B2B), certificados digitais animados ou vídeos tutoriais personalizados para onboarding de contas enterprise.
4. **Demonstração de Ferramentas de Linha de Comando & DevTools (Terminal Showcase)**:
   Produtos focados em desenvolvedores (CLIs, bancos de dados, orquestradores, frameworks) que precisam exibir instalações rápidas (`npm install`, `docker run`), comandos encadeados e fluxos de output sem a imperfeição de gravações de tela manuais.
5. **Apresentação de Fluxos de Agentes de IA e Raciocínio (`AI-Input & Reasoning Streams`)**:
   Demonstrações visuais de prompts complexos sendo preenchidos, chamadas de ferramentas (*tool calling*), expansão de árvores de pensamento e streaming de respostas em layouts de alto nível para investidores e usuários finais.

### Papel no Ritmo Visual (Regra 60-30-10)

- **60% — Fundação do Produto (Componentes Base shadcn/ui & Tailwind)**:
  A estrutura de navegação, painéis de administração, cards e formulários que compõem a aplicação operacional onde o usuário trabalha cotidianamente, utilizando a neutralidade do cinza profundo (`bg-zinc-950`), bordas sutis e tipografia legível (`Geist Sans`).
- **30% — Camada de Demonstração & Micro-Histórias Visuais (Snapcn Interativo)**:
  - *Terminal Simulator*: Seção de documentação ou Hero com simulação de linha de comando demonstrando o setup do produto em 4 passos rápidos.
  - *Phone Frame & Laptop Frame*: Elementos centrais da seção de funcionalidades exibindo a interface responsiva do produto em perspectiva isométrica leve.
  - *Card Rail & Orbit Gallery*: Carrosséis cinematográficos que apresentam integrações e parceiros flutuando na profundidade Z.
- **10% — Efeitos Protagonistas / Showstoppers Cinematográficos (Launch Climax)**:
  - *Hero Launch Scene*: Montagem inicial de 3 a 5 segundos no topo da página ou no vídeo principal, com cortes percussivos (*punch lines*), revelação de logotipo por fragmentação (*logo-assemble*) e explosão de tipografia com desfoque de movimento (*text-swell*).
  - *Karaoke Captions*: Legendas de alta energia com realce dinâmico palavra por palavra para reels e vídeos curtos no Twitter/LinkedIn.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Componentes Interativos de Formulários Críticos do Dia a Dia**:
  Não utilize componentes de tempo do Snapcn (que dependem de `useCurrentFrame`) como substitutos de botões, dropdowns ou campos de texto reais com os quais o usuário final precisa interagir com cliques e digitação em tempo real em um dashboard operacional. O Snapcn foi desenhado para **visualização determinística guiada pelo tempo**, e não para tratamento de eventos síncronos de formulário.
- **Ambientes Web com Limitação Extrema de Recursos sem Web Workers/Canvas**:
  A renderização pesada de múltiplos players Remotion simultâneos em uma mesma página pode sobrecarregar navegadores mobile de baixo custo devido ao cálculo contínuo de matrizes de transformação por quadro. Limite-se a no máximo 1 ou 2 players por viewport.
- **Interfaces Puramente Editoriais ou Burocráticas (Documentação Médica, Jurídica ou Financeira Estrita)**:
  Em manuais técnicos ou contratos legais, efeitos cinéticos de texto (*text-swell*, *phrase-swarm*) introduzem distração cognitiva desnecessária e passam uma impressão amadora ou excessivamente festiva.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "Video Slop"):
- **Cortes Hipercinéticos Sem Respiro (Efeito "Brainrot")**:
  Empilhar transições a cada 10 quadros (menos de meio segundo por cena) em uma apresentação B2B torna a proposta de valor do produto incompreensível. Uma boa cena de produto precisa de pelo menos 60 a 90 quadros (2 a 3 segundos) de sustentação visual para que o espectador assimile o que está acontecendo na interface.
- **Dessincronização de Tipos de Mola**:
  Misturar componentes com configurações de amortecimento discrepantes (exemplo: um laptop frame com mola ultra-amortecida `damping: 40` e um cursor com mola vibrante e elástica `damping: 8`) quebra a ilusão física de um ambiente coerente. Estabeleça uma única constante de física para todo o vídeo.
- **Uso Indiscriminado de Mockups sem Escala Proporcional**:
  Inserir um print em baixa resolução (720p) esticado dentro de uma moldura de MacBook 4K com zoom digital causa desfoque feio nos textos e controles da interface. Os elementos de tela devem ser preferencialmente réplicas em código vetorial (HTML/CSS/SVG) ou capturas em escala retina `@2x`/`@3x`.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo está o catálogo estruturado das 10 principais categorias e componentes emblemáticos do Snapcn:

### 1. `text-reveal` (Kinetic Typography Primitiva)
- **Anatomia Visual**: O texto emerge de uma linha de base invisível com deslocamento vertical (`translateY(24px) -> translateY(0)`), acompanhado de uma interpolação simultânea de opacidade (`0 -> 1`) e desfoque progressivo (`filter: blur(8px) -> blur(0)`). Cada palavra ou caractere possui um atraso escalonado (*stagger delay*) configurável em quadros.
- **Gatilho de Interação**: Timeline determinística (acionado em um quadro específico `startFrame`, tipicamente nos primeiros 15 quadros de uma cena).
- **Onde Encaixar**: Título principal do Hero, frases de impacto em transições de cena e encerramento com o slogan da marca.

### 2. `terminal-simulator` (DevTools Screen & Shell)
- **Anatomia Visual**: Uma janela de terminal elegante com cantos arredondados contínuos (`rounded-xl`), botões de janela estilo macOS (vermelho, amarelo, verde com opacidade balanceada) e fundo cinza ardósia ultra-escuro (`#0d1117` ou `zinc-950`). Apresenta o prompt de comando (`$`), digitação com velocidade orgânica de digitação humana, cursor de bloco pulsante em cor de destaque e renderização em cascata de logs com cores semânticas (verde para sucesso, azul para info, âmbar para avisos).
- **Gatilho de Interação**: Autoplay temporal sincronizado por quadros; permite pausar e retroceder via `@remotion/player`.
- **Onde Encaixar**: Demonstração de instalação de bibliotecas, setup de CLI, execução de migrations e outputs de testes em landing pages técnicas.

### 3. `cursor-track` (Simulação de Interação Humana & Mouse)
- **Anatomia Visual**: Renderiza uma seta de cursor vetorial estilizada (com sombra difusa profunda simulando elevação do plano da tela). O cursor interpola sua posição `(x, y)` ao longo de uma curva de Bézier cúbica suave, desacelera ao se aproximar de um alvo de clique (como um botão), comprime levemente seu tamanho (`scale: 0.88`) no instante exato do clique e gera um círculo de propagação de clique (*ripple wave*) translúcido sobre o elemento.
- **Gatilho de Interação**: Sequência temporal baseada em quadros-chave de coordenadas cartesianas `[{ frame: 0, x: 100, y: 500 }, { frame: 45, x: 640, y: 320, click: true }]`.
- **Onde Encaixar**: Guias passo-a-passo de produto, tutoriais de onboarding interativo e demonstrações de fluxos complexos de checkout ou configuração.

### 4. `laptop-frame` & `laptop-open` (Hardware Canvas 3D)
- **Anatomia Visual**: Moldura vetorial ultra-precisa inspirada no chassi de alumínio anodizado do MacBook Pro, completa com entalhe de câmera (*notch*), teclado em perspectiva inferior e tela com proporção 16:10. No componente `laptop-open`, a tampa começa fechada e se eleva no espaço tridimensional com rotação angular `rotateX(-90deg) -> rotateX(0deg)` impulsionada por uma mola com amortecimento crítico, revelando a interface iluminada com reflexos dinâmicos de luz na borda.
- **Gatilho de Interação**: Abertura de cena principal do vídeo ou transição de corte entre visão geral e detalhes do produto.
- **Onde Encaixar**: Hero Video de landing page corporativa, anúncio de novas versões de software desktop/web e trailers de produto.

### 5. `phone-stack` & `phone-frame` (Mobile Spatial Showcase)
- **Anatomia Visual**: Representação gráfica detalhada de smartphones topo de linha com Dynamic Island e bordas ultrafinas. O `phone-stack` empilha de 3 a 5 telas de aplicativo deslocadas no eixo Z com rotação lateral sutil (`rotateZ(-8deg)` e `rotateY(12deg)`). Conforme a linha do tempo avança, a tela frontal desliza para a esquerda enquanto a tela traseira vem para o primeiro plano com interpolação de escala e desfoque de profundidade.
- **Gatilho de Interação**: Ciclo de quadros (troca de tela a cada 60 quadros / 2 segundos).
- **Onde Encaixar**: Demonstração de aplicativos mobile, PWAs, visualizações responsivas e galerias de telas de produtos de consumo.

### 6. `agent-steps` & `answer-stream` (AI Workflow Orchestration)
- **Anatomia Visual**: Visualizador de execução de agentes inteligentes composto por uma linha de tempo vertical com nós de estado conectados por linhas iluminadas. Cada etapa exibe ícones contextuais (busca web, leitura de código, geração de teste), um indicador de progresso em anel pulsante (`animate-spin` suave) e uma área de dados expansível. Conforme a última etapa conclui, o componente `answer-stream` injeta o resultado final com streaming simulado de caracteres em alta velocidade.
- **Gatilho de Interação**: Linha do tempo sequencial simulando execução assíncrona de IA em tempo acelerado.
- **Onde Encaixar**: Demonstração de produtos nativos de IA, copilotos de código, sistemas de atendimento autônomos e painéis de observability de LLMs.

### 7. `count-grid` & `ticker-climb` (Kinetic Data Metrics)
- **Anatomia Visual**: Grid estilo Bento contendo cards monocromáticos com números monumentais que sobem em alta velocidade através de física de mola (`spring()`), desacelerando gradualmente até o valor final desejado (ex: "0" para "99.99%", "0ms" para "12ms", "0" para "$1.2M"). Os dígitos podem utilizar o efeito de tambor rotativo mecânico (*digit roll*).
- **Gatilho de Interação**: Entrada da cena no quadro de impacto estatístico (geralmente nos segundos intermediários do vídeo).
- **Onde Encaixar**: Seção de prova social, benchmarks de performance de bancos de dados ou relatórios de faturamento anual.

### 8. `karaoke-captions` & `word-captions` (Dynamic Video Subtitles)
- **Anatomia Visual**: Legendas dinâmicas posicionadas no terço inferior da composição. As palavras surgem em bloco com fundo cinza translúcido; a palavra atualmente falada acende instantaneamente em branco puro ou amarelo ouro vibrante, expandindo-se 10% em escala com mola elástica (`scale: 1.1`), enquanto as palavras já pronunciadas recuam para um tom cinza escuro.
- **Gatilho de Interação**: Sincronização direta com arrays de timestamps em milissegundos gerados por transcrições de áudio (formato Whisper JSON).
- **Onde Encaixar**: Vídeos falados pelo fundador, teasers verticais para TikTok, Instagram Reels, YouTube Shorts e Twitter/X.

### 9. `logo-assemble` (Brand Convergence Sting)
- **Anatomia Visual**: O logotipo da empresa ou produto começa decomposto em fragmentos geométricos flutuando fora da viewport em posições randômicas com rotação assimétrica. Ao atingir o quadro de convergência, todos os fragmentos são atraídos simultaneamente para o centro por um vetor de força magnética simulada, encaixando-se com um estalo seco e uma onda de choque de partículas (*dot-bloom*) que se propaga para as bordas.
- **Gatilho de Interação**: Primeiros 45 quadros da vinheta de introdução ou últimos 60 quadros do encerramento (CTA final).
- **Onde Encaixar**: Vinhetas de abertura de vídeo, splash screens de carregamento de dashboards e encerramentos promocionais.

### 10. `orbit-gallery` & `card-rail` (Spatial Feature Carousel)
- **Anatomia Visual**: Cards com acabamento em vidro translúcido (`backdrop-blur-md bg-white/5 border border-white/10`) contendo capturas de funcionalidades, depoimentos ou logotipos de clientes. Os cards orbitam em um caminho elíptico 3D ao redor do ponto focal do vídeo; cards que passam ao fundo recebem opacidade reduzida e desfoque gaussiano, enquanto o card frontal atinge 100% de escala e nitidez total.
- **Gatilho de Interação**: Rotação contínua baseada no quadro atual (`rotation = (frame * speed) % 360`).
- **Onde Encaixar**: Seções de ecossistema de integrações, depoimentos de clientes e catálogos de recursos premium.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Projeto

Para utilizar o Snapcn, o projeto deve ser estruturado sobre o **Remotion** com configuração do **Tailwind CSS** e o arquivo de registro do **shadcn/ui**.

#### 1. Criação do Ambiente Remotion (se não existir):
```bash
npx create-video@latest meu-video-snapcn
# Selecione o template: React + TypeScript + Tailwind CSS
```

#### 2. Configuração do `components.json` (Raiz do Projeto):
Como os projetos Remotion possuem convenções de diretório ligeiramente diferentes dos apps Next.js convencionais, o `components.json` deve mapear explicitamente os caminhos:

```json
{
  "$schema": "https://ui.shadcn.com/schema.json",
  "style": "new-york",
  "rsc": false,
  "tsx": true,
  "tailwind": {
    "config": "tailwind.config.js",
    "css": "src/index.css",
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
  "iconLibrary": "lucide"
}
```

#### 3. Instalação de Componentes via shadcn CLI:
```bash
# Adicionando componentes específicos do Snapcn
npx shadcn@latest add @snapcn/text-reveal
npx shadcn@latest add @snapcn/terminal-simulator
npx shadcn@latest add @snapcn/cursor-track
npx shadcn@latest add @snapcn/phone-frame
```

#### 4. Setup do Agente & MCP (Opcional, para automação com Claude/Cursor):
```bash
# Instala o pacote de conhecimento de design e regras do Snapcn no agente
npx skills add snapcndev/snapcn
```

---

### Física de Movimento e Parâmetros Matemáticos

O Snapcn utiliza funções matemáticas determinísticas do motor Remotion. Abaixo estão as tabelas de constantes e equações padrão da biblioteca:

#### Calibrações Padrão de Mola (`Remotion spring`):

| Padrão de Uso | `damping` | `mass` | `stiffness` | `overshootClamping` | Sensação Física |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Snappy UI / Pop** | `12` | `0.5` | `180` | `false` | Rápido, leve ricochete tátil (ideal para botões e cursores) |
| **Smooth Hardware** | `26` | `1.0` | `100` | `false` | Mecânica pesada e estável (tampas de laptop, molduras de tela) |
| **Cinematic Text** | `20` | `0.8` | `120` | `true` | Amortecimento crítico estrito sem oscilação residual |
| **Heavy Impact** | `14` | `1.8` | `220` | `false` | Impacto de peso com assentamento perceptível (cards de estatística) |

#### Curvas de Interpolação & Easing Bézier:
Nas transições baseadas em quadros onde o uso de molas não é desejável (ex: rotações contínuas ou deslocamento linear constante), o Snapcn emprega a função `Easing.bezier(x1, y1, x2, y2)`:
- **Entrada Padrão Suave**: `Easing.bezier(0.16, 1, 0.3, 1)` (curva idêntica ao desaceleramento do iOS).
- **Aceleração/Desaceleração Simétrica**: `Easing.bezier(0.65, 0, 0.35, 1)`.

---

### Receita de Código Funcional: Componente `KineticTerminalScene`

Abaixo está uma implementação realista e completa em React/Remotion/Tailwind demonstrando a sinergia entre **Terminal**, **Cursor Simulado** e **Tipografia Cinética**:

```tsx
import React from "react";
import {
  interpolate,
  spring,
  useCurrentFrame,
  useVideoConfig,
  Sequence,
} from "remotion";
import { Terminal as TerminalIcon, CheckCircle2, Copy } from "lucide-react";

// --- Tipagens do Componente ---
interface KineticTerminalSceneProps {
  title?: string;
  commandText?: string;
}

export const KineticTerminalScene: React.FC<KineticTerminalSceneProps> = ({
  title = "Deploy in seconds",
  commandText = "npx snapcn@latest add hero-launch",
}) => {
  const frame = useCurrentFrame();
  const { fps } = useVideoConfig();

  // 1. Física de entrada do Título Principal (Text Reveal com Blur e Mola)
  const titleSpring = spring({
    frame,
    fps,
    config: { damping: 18, mass: 0.8, stiffness: 120 },
  });

  const titleOpacity = interpolate(frame, [0, 20], [0, 1], {
    extrapolateRight: "clamp",
  });
  const titleY = interpolate(titleSpring, [0, 1], [40, 0]);
  const titleBlur = interpolate(titleSpring, [0, 1], [12, 0]);

  // 2. Física de elevação da Janela do Terminal (Mola com amortecimento elegante)
  const terminalFrameStart = 15;
  const terminalSpring = spring({
    frame: frame - terminalFrameStart,
    fps,
    config: { damping: 22, mass: 1.0, stiffness: 90 },
  });

  const terminalY = interpolate(terminalSpring, [0, 1], [80, 0]);
  const terminalScale = interpolate(terminalSpring, [0, 1], [0.94, 1]);
  const terminalOpacity = interpolate(
    frame,
    [terminalFrameStart, terminalFrameStart + 15],
    [0, 1],
    { extrapolateRight: "clamp" }
  );

  // 3. Efeito de digitação humana simulada no comando
  const typingStart = 35;
  const charactersCount = commandText.length;
  const typedLength = Math.floor(
    interpolate(frame, [typingStart, typingStart + 30], [0, charactersCount], {
      extrapolateLeft: "clamp",
      extrapolateRight: "clamp",
    })
  );
  const displayedCommand = commandText.slice(0, typedLength);

  // Piscar do cursor (a cada 16 quadros)
  const showCursor =
    frame >= typingStart &&
    (frame < typingStart + 35 || Math.floor(frame / 16) % 2 === 0);

  // 4. Surgimento dos logs de sucesso após a conclusão da digitação
  const logStart = typingStart + 38;
  const logOpacity = interpolate(frame, [logStart, logStart + 12], [0, 1], {
    extrapolateLeft: "clamp",
    extrapolateRight: "clamp",
  });

  // 5. Simulação do Cursor do Mouse se aproximando e clicando no botão Copiar
  const cursorStart = 75;
  const cursorProgress = spring({
    frame: frame - cursorStart,
    fps,
    config: { damping: 14, mass: 0.6, stiffness: 140 },
  });

  const cursorX = interpolate(cursorProgress, [0, 1], [900, 720]);
  const cursorY = interpolate(cursorProgress, [0, 1], [500, 310]);
  const isClicking = frame >= cursorStart + 22 && frame <= cursorStart + 28;
  const copyButtonScale = isClicking ? 0.92 : 1;

  return (
    <div className="relative flex flex-col items-center justify-center w-full h-full bg-[#09090b] text-zinc-100 overflow-hidden font-sans select-none">
      {/* Background Glow sutil com gradiente radial */}
      <div className="absolute -top-32 w-[600px] h-[600px] bg-sky-500/10 rounded-full blur-[140px] pointer-events-none" />

      {/* Título Cinético Superior */}
      <div
        style={{
          opacity: titleOpacity,
          transform: `translateY(${titleY}px)`,
          filter: `blur(${titleBlur}px)`,
        }}
        className="mb-10 text-center"
      >
        <span className="text-xs font-mono font-medium tracking-widest text-sky-400 uppercase bg-sky-950/60 border border-sky-800/50 px-3 py-1 rounded-full mb-3 inline-block">
          Instant Setup
        </span>
        <h1 className="text-4xl md:text-5xl font-extrabold tracking-tight text-white">
          {title}
        </h1>
      </div>

      {/* Janela do Terminal Estilizada */}
      <div
        style={{
          opacity: terminalOpacity,
          transform: `translateY(${terminalY}px) scale(${terminalScale})`,
        }}
        className="relative w-full max-w-2xl bg-zinc-950/90 border border-zinc-800 rounded-xl shadow-2xl backdrop-blur-xl overflow-hidden"
      >
        {/* Barra de Título da Janela (Traffic Lights macOS) */}
        <div className="flex items-center justify-between px-4 py-3 bg-zinc-900/60 border-b border-zinc-800/80">
          <div className="flex items-center space-x-2">
            <div className="w-3 h-3 rounded-full bg-red-500/80" />
            <div className="w-3 h-3 rounded-full bg-yellow-500/80" />
            <div className="w-3 h-3 rounded-full bg-green-500/80" />
          </div>

          <div className="flex items-center space-x-2 text-xs font-mono text-zinc-400">
            <TerminalIcon className="w-3.5 h-3.5 text-zinc-500" />
            <span>bash — 80x24</span>
          </div>

          {/* Botão de Copiar com feedback simulado */}
          <button
            style={{ transform: `scale(${copyButtonScale})` }}
            className="flex items-center space-x-1.5 px-2 py-1 text-xs font-mono text-zinc-400 bg-zinc-800/50 border border-zinc-700/50 rounded-md transition-transform"
          >
            <Copy className="w-3 h-3" />
            <span>Copy</span>
          </button>
        </div>

        {/* Corpo do Terminal com Tipografia Mono */}
        <div className="p-6 font-mono text-sm leading-relaxed space-y-3 min-h-[180px]">
          {/* Linha de Comando Ativa */}
          <div className="flex items-center space-x-2 text-zinc-200">
            <span className="text-sky-400 font-bold select-none">$</span>
            <span>{displayedCommand}</span>
            {showCursor && (
              <span className="inline-block w-2 h-4 bg-sky-400 animate-pulse ml-0.5 align-middle" />
            )}
          </div>

          {/* Logs de Execução Renderizados Após Digitação */}
          {frame >= logStart && (
            <div style={{ opacity: logOpacity }} className="space-y-1.5 pt-2 text-xs">
              <div className="text-zinc-500">
                ✔ Registry resolved: https://snapcn.dev/r/hero-launch.json
              </div>
              <div className="text-zinc-500">
                ✔ Installing dependencies: @remotion/core, lucide-react...
              </div>
              <div className="flex items-center space-x-2 text-emerald-400 font-medium pt-1">
                <CheckCircle2 className="w-4 h-4 text-emerald-400" />
                <span>Success! Component installed at src/components/snap-cn/hero-launch.tsx</span>
              </div>
            </div>
          )}
        </div>
      </div>

      {/* Simulação do Cursor do Mouse */}
      {frame >= cursorStart && (
        <div
          style={{
            transform: `translate3d(${cursorX}px, ${cursorY}px, 0)`,
          }}
          className="absolute top-0 left-0 pointer-events-none z-50 transition-transform duration-75"
        >
          <svg
            className={`w-6 h-6 filter drop-shadow-[0_4px_8px_rgba(0,0,0,0.6)] ${
              isClicking ? "scale-90" : "scale-100"
            }`}
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M5.5 5.5L19 11L13.4 12.45L11.95 18L5.5 5.5Z"
              fill="white"
              stroke="#09090b"
              strokeWidth="1.5"
              strokeLinejoin="round"
            />
          </svg>
          {/* Efeito de Ripple no clique */}
          {isClicking && (
            <div className="absolute -top-2 -left-2 w-8 h-8 rounded-full border border-sky-400/80 bg-sky-400/20 animate-ping" />
          )}
        </div>
      )}
    </div>
  );
};
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao integrar o **Snapcn** no `DESIGN_BLUEPRINT.md` de uma nova aplicação ou produto, declare explicitamente os seguintes blocos normativos para orientar tanto a equipe quanto os agentes de IA:

### 1. Declaração de Stack & Compatibilidade Remotion
- No bloco `Tech Stack`:
  ```markdown
  - Video & Kinetic Motion Engine: Remotion (@remotion/core, @remotion/player v4+)
  - Component Registry: Snapcn (@snapcn) via shadcn CLI
  - Path Aliases: "@/components/snap-cn/*" -> "src/components/snap-cn/*"
  - Styling System: Tailwind CSS com paleta zinc/slate e tokens de opacidade contínua
  ```

### 2. Atribuição de Funções no Ritmo Visual
- Especifique a função de cada componente Snapcn:
  - **Hero Video Showcase**: `@snapcn/hero-launch` combinado com `@snapcn/laptop-open` no frame 0 a 120.
  - **Seção de Desenvolvedor / CLI**: `@snapcn/terminal-simulator` embutido com player responsivo `@remotion/player` (`autoPlay={true}`, `loop={true}`, `controls={false}`).
  - **Prova Social & Métricas**: `@snapcn/count-grid` renderizado para animar números de transações ou velocidade sob demanda de scroll.

### 3. Regras de Orçamento Temporal (Timeline Budgeting Rules)
Para evitar composições confusas ou descompassadas, exija que todo roteiro em vídeo programático siga a regra de cadência do Snapcn:
- **Cena de Abertura (Hook)**: Máximo 90 quadros (3 segundos a 30 FPS).
- **Demonstração do Ponto de Dor (Problem/Solution)**: 120 a 180 quadros (4 a 6 segundos).
- **Passeio pelo Produto (Feature Tour via Cursor/Screens)**: 240 quadros (8 segundos divididos em blocos de 60 quadros).
- **Clímax & Chamada para Ação (CTA/Logo Assemble)**: 90 quadros (3 segundos).
- **Taxa Padrão de Quadros**: Fixada estritamente em **30 FPS** para visualizações web e **60 FPS** para renders finais de exportação MP4.

### 4. Instruções Diretas para Agentes de IA
Instrua os agentes a nunca gerarem animações de vídeo com `setTimeout` ou `setInterval` assíncronos. Todo cálculo de transição dentro de componentes de vídeo DEVE obrigatoriamente derivar de `useCurrentFrame()` e das funções `spring()` ou `interpolate()` nativas do Remotion.
