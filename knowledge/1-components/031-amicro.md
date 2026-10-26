---
id: "amicro"
name: "aMicro"
url: "https://amicro.vercel.app/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Micro-Interactions de Alta Fidelidade", "Tactile Web Haptics (Audio & Vibration)", "Modern Kinetic UI", "Dither & Procedural Canvas Shaders", "Spatial Arc & 3D Card Physics", "Dark Mode Craft Minimal"]
densidade_informacao: "Flexivel"
impacto_visual: "Moderado a Alto/Showstopper"
custo_computacional: "Baixo a Medio (Motion/Springs + Web Audio Haptics + Canvas Dither 60fps)"
stack_frameworks: ["React 19 / React 18", "Motion 12 (motion/react / framer-motion)", "Tailwind CSS v4 / v3", "TypeScript", "Vite", "Web Audio API", "Shadcn Registry CLI"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "JetBrains Mono", "SF Pro Display", "Plus Jakarta Sans"]
  paletas_ideais: ["Deep Zinc Dark Mode (zinc-950 / zinc-900 / zinc-100)", "Monochrome High-Contrast (black / white)", "Emerald & Indigo Pulse Accents", "Dithered Grayscale Gradients"]
  combinacoes_recomendadas: ["Shadcn UI", "Motion Primitives", "Cult UI", "Magic UI", "OriginKit"]
  conflitos_esteticos: ["Brutalismo cru sem easing ou molas", "Neumorfismo plástico saturado com sombras pesadas", "Animações CSS lineares rígidas sem amortecimento de inércia", "UI corporativa anos 2010 estática e sem feedback tátil"]
---

# aMicro — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo engenheiro e designer **Syed Subhan** (`@SubhanHQ` no X / `@Subhan-code` no GitHub), o **aMicro** (`amicro.vercel.app`, pacote `@subhanhq/amicro`) é uma biblioteca aberta de componentes de interface, micro-interações táteis e físicas de transição construída sobre o ecossistema moderno de **React 19**, **Motion** (anteriormente Framer Motion) e **Tailwind CSS v4**.

Enquanto a maioria das bibliotecas de UI foca em blocos estruturais genéricos (botões padronizados, formulários estáticos e tabelas neutras) ou em efeitos tridimensionais pesados que comprometem o desempenho, o aMicro estabeleceu seu diferencial em um território altamente especializado e refinado: **o refinamento sensorial de micro-momentos de interface, mecânicas espaciais de cartões e retroalimentação multissensorial na web**.

```
╭────────────────────────────────────────────────────────────────────────╮
│                                aMicro                                  │
│   The Tactile Motion & Micro-Interactions Registry for React 19       │
├────────────────────────────────────────────────────────────────────────┤
│  [ Arc Card Spreads ]  ───►  Física Parabólica & Leques Espaciais      │
│  [ Web Haptics ]       ───►  Micro-áudio sintetizado + Vibração Mobile │
│  [ Dither Canvas ]     ───►  Matrizes 60fps de dither procedural       │
│  [ AI Cockpit ]        ───►  Reasoning Traces, Streaming & Micro-Pills │
│  [ 135+ Micro-Loaders ]───►  Dynamic Island, Laser Reticle, Siri Wave  │
╰────────────────────────────────────────────────────────────────────────╯
```

### Os Pilares da Assinatura Visual do aMicro:

1. **Multissensorialidade Tátil Nativa (`useWebHaptics` & Web Audio API)**:
   A web tradicional é puramente silenciosa e bidimensional. O aMicro rompe essa barreira introduzindo feedback tátil duplo:
   - **Áudio Sintetizado Sub-perceptivo**: Utilizando a `Web Audio API` (`AudioContext`, `OscillatorNode`, envelopes de ganho exponenciais com ondas senoidais a 820Hz-1240Hz para sucesso e triangulares a 1400Hz-1750Hz para cliques mecânicos), cada clique ou cópia de código emite um estalido acústico extremamente sutil, comparável ao feedback tátil de teclados mecânicos de luxo ou da coroa digital do Apple Watch.
   - **Vibração Háptica em Smartphones**: Em dispositivos compatíveis, aciona o `navigator.vibrate` com sequências em milissegundos precisas (ex: `10ms` para toque leve, `[15ms, 60ms, 15ms]` para confirmação de sucesso).
   - O resultado é uma interface que parece "palpável", diminuindo drasticamente a sensação de atraso cognitivo do usuário.

2. **Física Parabólica de Cartões e Leques Espaciais (*Spatial Card Mechanics*)**:
   Em vez de carrosséis planos convencionais ou grids estáticos, o aMicro oferece uma família inteira de componentes de cartões organizados por fórmulas trigonométricas e parabólicas:
   - **Arc Spread (`CardArc5`, `CardArc7`, `CardLongArc5`)**: Os cartões se distribuem em um arco curvo contínuo ao receber hover. A rotação e a elevação vertical seguem uma parábola simétrica calculada em relação ao cartão central (`Math.abs(dist) === 2 ? yOffset : ...`), emulando um leque de cartas de baralho aberto na mão de um mágico.
   - **Time Machine Stack (`CardTimeMachine`)**: Inspirado na interface tridimensional do Time Machine do macOS, organiza cartões em camadas profundas no eixo Z com perspectiva forçada, permitindo navegar em um scrubber cronológico suave.
   - **CoverFlow & Wheel Fan (`CardCoverFlow`, `CardWheelFan`)**: Projeção em semi-círculo radial ou esteira de perspectiva angular.

3. **Gráficos Procedurais em Canvas com Estética Dither (*Pixel Dither Matrix*)**:
   Em componentes de dados como `DitherDonutChart`, `DitherGrowthChart`, `UptimeChart` e `ActivityHeatmap`, o aMicro abandona os vetores SVG lisos e previsíveis em favor de uma estética de alta densidade gráfica baseada em pontilhismo (*dithering*) procedural calculado via HTML5 Canvas em tempo real (60 FPS), gerando gradientes de densidade de ruído pseudo-aleatório através de algoritmos de `smoothstep` e funções de hash senoidal (`sin(x * 12.9898 + y * 78.233)`).

4. **Componentes para a Nova Era da Inteligência Artificial (AI Cockpit Primitives)**:
   A biblioteca inclui componentes especializados para produtos de IA generativa de última geração:
   - `AiPromptInput`: Campo de entrada expansível inteligente com seletor de modelos (Claude, GPT, DeepSeek, Gemini), botão de ditado com onda de voz pulsante, toggles para Web Search e Deep Thinking, e contagem de tokens em tempo real.
   - `AiReasoningTrace`: Painel sanfonado (*accordion*) de cadeia de pensamento (*Chain of Thought*), com cronômetro de tempo de raciocínio decorrido, nó cerebral pulsante e rastreamento sequencial de passos lógicos.
   - `AiResponseStream`: Bloco de código e fluxo de resposta estilo terminal com navegação por versões de ramos (*git branches*), cópia com feedback sonoro háptico e botões de avaliação morfológicos.

5. **Exaustivo Catálogo de Micro-Loaders Atômicos (Mais de 135 variações)**:
   O aMicro possui o maior repertório focado em carregadores micro-estruturais do ecossistema React. Desde o `DynamicIsland` (que expande e contrai simulando a pílula do iPhone) e o `FaceIdScan` (scanner biométrico a laser), até osciladores de mola quântica (`WavePhysicsLoader`, `NewtonsCradle`, `SiriWave`).

6. **Presets Padronizados de Física de Mola (`presets.ts`)**:
   Em vez de parâmetros mágicos espalhados pelo código, a biblioteca unifica as curvas físicas em cinco presets universais (`snappy`, `bouncy`, `smooth`, `gentle`, `stiff`), garantindo harmonia cinética em toda a aplicação.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários

1. **Aplicações de Inteligência Artificial Generativa & Agentes Autônomos**:
   - `AiPromptInput` e `AiReasoningTrace` são componentes de primeira linha para interfaces de chat com IA, copilotos em painéis SaaS e estúdios de prompt, oferecendo transparência durante o processamento do modelo sem sobrecarregar a tela.
2. **FinTechs, Neobanks & Carteiras Digitais**:
   - Os componentes de cartões em leque (`CardArc5`, `CardArc7`, `CardCoverFlow`) são a solução ideal para exibição de múltiplos cartões de crédito virtuais, planos de assinatura, cartões de fidelidade e seleção de benefícios em áreas de checkout.
3. **Dashboards de Engenharia, Infraestrutura & DevTools**:
   - Os gráficos em dither (`UptimeChart`, `DitherGrowthChart`, `ActivityHeatmap`) e os micro-loaders de status (`TerminalLoader`, `DynamicIsland`, `DashRing`) conferem a estética de alta sofisticação técnica celebrada por marcas como Linear, Vercel, Supabase e Raycast.
4. **Portfólios de Design Engineers & Creative Technologists**:
   - Para desenvolvedores front-end que desejam demonstrar domínio de micro-interações, refinamento de som e movimento sem recorrer a bibliotecas 3D volumosas como Three.js.

### Papel no Ritmo Visual (Regra 60-30-10)

- **60% — Fundação Neutra e Silenciosa (Base Estrutural)**:
  Superfícies monocromáticas com Tailwind CSS (`bg-zinc-950` / `bg-neutral-900` para Dark Mode ou `bg-zinc-50` para Light Mode), tipografia nítida (`Geist Sans` ou `Inter`), espaçamento matemático e bordas com transparência sutil (`border-white/10`).
- **30% — Camada de Fluidez e Feedback Tátil (Micro-Interações aMicro)**:
  - `MagneticButton` para botões primários de chamada para ação, adicionando atração física ao cursor do usuário.
  - `TiltCard` e `CardHover` para cartões de bento grids e recursos em landing pages.
  - `useWebHaptics` integrado a ações de cópia, deleção, envio de formulários e alternância de temas.
  - `ScrollReveal` e `ProgressIndicator` guiando a leitura natural do usuário pela página.
- **10% — Efeitos Protagonistas / Showstoppers (Showcases de Alto Impacto)**:
  - `CardArc5` / `CardArc7` abrindo um leque interativo na seção Hero ou de precificação.
  - `CardTimeMachine` apresentando o histórico de versões ou a evolução do produto com perspectiva de profundidade 3D.
  - `DitherDonutChart` ocupando o centro de um painel de métricas financeiras ou de telemetria.
  - `AiReasoningTrace` expandindo dinamicamente as fases de pensamento cognitivo de um agente autônomo.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

1. **Aplicações Estritamente Críticas com Usuários em Ambientes Sensíveis a Som (Sem Switch de Desativação)**:
   - Nunca implemente o `useWebHaptics` com som ativado por padrão em sistemas hospitalares, ferramentas jurídicas de leitura de processos ou portais corporativos formais sem fornecer um botão explícito e acessível para mutar o áudio. O aMicro inclui persistência no `localStorage` via `amicro_sound_enabled`, e esse opt-in/opt-out deve ser rigorosamente respeitado.
2. **Listas Infinitas e Grids com Centenas de Elementos Concorrentes**:
   - Adicionar `MagneticButton` ou `TiltCard` dentro de cada linha de uma tabela de 5.000 itens causará overhead massivo de listeners de mouse no DOM e degradação de FPS. O uso deve ser concentrado nos elementos focais e cartões de destaque.
3. **Projetos Brutalistas / Neobrutalistas sem Animação**:
   - Estéticas que se apoiam em cortes secos, sombras duras pretas sólidas (`shadow-[4px_4px_0px_black]`) e ausência deliberada de molas conflitam diretamente com a linguagem física fluida e orgânica do aMicro.
4. **Dispositivos Legados com Navegadores que Bloqueiam Web Audio**:
   - Em webviews restritivas ou navegadores institucionais bloqueados, garanta que os componentes possuam fallbacks silenciosos não-bloqueantes (padrão já adotado pelo hook `useWebHaptics`).

### ⚠️ Erros Comuns de Exagero ("AI Slop"):

- **Cacofonia Sensorial (Audio Spam)**:
  Ativar feedback sonoro em ações triviais e contínuas (como simplesmente mover o mouse entre links de uma navbar ou digitar cada caractere em um input de texto). O som deve ser reservado exclusivamente para eventos discretos e significativos de conclusão (ex: clique no botão enviar, cópia para o clipboard, sucesso de deploy).
- **Molas Hiper-Elásticas em Contextos Sérios**:
  Utilizar o preset `bouncy` em interfaces financeiras de confirmação de transferência bancária ou fechamento de fatura. Nesses fluxos, o usuário exige precisão e segurança; deve-se usar estritamente o preset `snappy` ou `stiff`.
- **Ignorar Usuários com Sensibilidade Vestibular**:
  Falhar ao desativar as rotações de `CardArc5` ou a perspectiva de `CardTimeMachine` quando `useReducedMotion()` estiver ativo no sistema operacional do usuário.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 12 componentes e utilitários mais representativos da biblioteca aMicro:

```
┌────────────────────────────────────────────────────────────────────────┐
│                        CATÁLOGO DE COMPONENTES                         │
├────────────────────────────────┬───────────────────────────────────────┤
│ 1. CardArc5 / CardArc7         │ Leque parabólico espacial de cartões  │
│ 2. CardTimeMachine             │ Pilha 3D com scrubber temporal        │
│ 3. CardCarousel                │ Carrossel em arco com rotação 3D      │
│ 4. DitherDonutChart            │ Gráfico de rosca procedural em Canvas │
│ 5. DitherGrowthChart           │ Linha temporal com matriz dither      │
│ 6. AiPromptInput Studio        │ Input de IA dinâmico com ditado/chips │
│ 7. AiReasoningTrace            │ Accordion de pensamento cognitivo IA  │
│ 8. MagneticButton              │ Botão atrativo com física de mola     │
│ 9. DynamicIsland Loader        │ Cápsula expansível com onda sonora    │
│ 10. FaceIdScan Loader          │ Retículo biométrico com laser sweep   │
│ 11. WavePhysicsLoader          │ Oscilador de onda de física contínua  │
│ 12. useWebHaptics Hook         │ Motor háptico de áudio e vibração     │
╰────────────────────────────────┴───────────────────────────────────────╯
```

### 1. CardArc5 & CardArc7 (`card-arc-5`, `card-arc-7`)
- **Anatomia Visual**: Conjunto de 5 ou 7 cartões que repousam empilhados em uma pilha compacta centralizada. Ao receber hover ou gatilho de ativação, os cartões se desdobram em leque angular. O cartão central se projeta ligeiramente para cima no eixo Y negativo, enquanto os cartões periféricos rotacionam progressivamente para as extremidades (`-angle` a `+angle`) e se deslocam em uma curva parabólica natural.
- **Gatilho de Interação**: `onMouseEnter` / `onMouseLeave` ou prop booleana controlada `hovered`.
- **Onde encaixar na página**: Seção Hero de landing pages, seleção de planos de cartão de crédito no Pricing, ou galeria de templates de um SaaS.

### 2. Time Machine Stack (`card-time-machine`)
- **Anatomia Visual**: Organiza cartões em profundidade 3D com perspectiva acentuada no eixo Z. À medida que o cursor se move sobre o scrubber temporal inferior (marcado com nós "Today", "1d ago", "1w ago", "1m ago", "1y ago"), o cartão ativo avança para o primeiro plano enquanto os cartões anteriores desvanecem com escala reduzida e opacidade decrescente, recriando fielmente o efeito Time Machine da Apple.
- **Gatilho de Interação**: Hover interativo sobre a régua da linha do tempo com interpolação contínua de índice (`Math.round(index)`).
- **Onde encaixar na página**: Seções de histórico de produto (*Changelog*), showcases de portfólio criativo ou auditoria de versões em painéis de segurança.

### 3. Interactive 3D Motion Carousel (`card-carousel`)
- **Anatomia Visual**: Carrossel em arco inspirado em interfaces experimentais de vanguarda. Apresenta o card central ampliado com sombra profunda e borda luminosa, ladeado por cartões laterais semi-rotacionados em perspectiva angular. Inclui controles de navegação estilizados em chevrons e indicadores circulares de paginação.
- **Gatilho de Interação**: Cliques nos botões de navegação lateral, teclado (setas esquerda/direita) ou arrasto/swipe.
- **Onde encaixar na página**: Seção de depoimentos de clientes (*Social Proof*), galeria de estudos de caso ou catálogo de produtos premium.

### 4. Dither Donut Chart (`dither-donut-chart`)
- **Anatomia Visual**: Gráfico de rosca procedural renderizado via Canvas 2D em 60 quadros por segundo. Em vez de preenchimentos sólidos convencionais, cada fatia é preenchida por uma malha de pontos estocásticos calculados matematicamente. O centro exibe a métrica numérica animada via mola física (`useSpring`), refletindo a transição de planos e períodos (semana, mês, ano).
- **Gatilho de Interação**: Hover sobre as fatias do gráfico e cliques nos seletores de granularidade de tempo.
- **Onde encaixar na página**: Bento grids de métricas, painéis analíticos SaaS e dashboards financeiros executivos.

### 5. Dither Growth Line Chart (`dither-growth-chart`)
- **Anatomia Visual**: Gráfico de área e linha contínua de alta densidade onde a região sob a curva de crescimento é preenchida com um gradiente pontilhado de dither analógico. Possui marcadores de pontos interativos e tooltips flutuantes com interpolação elástica de coordenadas.
- **Gatilho de Interação**: Movimento do mouse sobre o eixo X com detecção do nó de dado mais próximo.
- **Onde encaixar na página**: Visualização de métricas de tráfego, volume de tokens consumidos em APIs de IA e receita recorrente mensal (MRR).

### 6. AI Prompt Input Studio (`ai-prompt-input`)
- **Anatomia Visual**: Área de texto auto-expansível de alta sofisticação com design em pílula de vidro escurecido. Contém:
  - Menu suspenso de seleção de modelos de LLM (com logos, tags "Fast Reasoning", "Ultra Low Latency").
  - Indicador de ditado por voz com barra de micro-ondas dinâmicas.
  - Toggles táteis para "Deep Thinking" e "Web Search" com chips luminosos.
  - Botão de envio circular que sofre transição morfológica para o ícone de parada (*stop square*) durante o streaming.
- **Gatilho de Interação**: Digitação, expansão automática de altura, clique em atalhos de sugestão (*prompt chips*) e teclas de atalho (`Cmd+Enter`).
- **Onde encaixar na página**: Hero de produtos de IA, interfaces de copiloto integradas e estúdios de prompt generativo.

### 7. AI Reasoning Trace Accordion (`ai-reasoning-trace`)
- **Anatomia Visual**: Bloco retrátil com borda translúcida que documenta as etapas de raciocínio lógico de uma IA generativa. Apresenta o ícone de cérebro pulsante, cronômetro de milissegundos decorridos em tempo real ("Thought for 3.2s") e lista progressiva de etapas concluídas marcadas com ícones verdes de confirmação.
- **Gatilho de Interação**: Clique no cabeçalho para expandir/recolher a visualização da árvore de pensamentos.
- **Onde encaixar na página**: Abaixo das mensagens do assistente de IA em chats conversacionais e relatórios de auditoria de agentes autônomos.

### 8. Magnetic Button (`magnetic-button`)
- **Anatomia Visual**: Botão em cápsula arredondada com sombra profunda e acabamento monocromático de alto contraste. Possui um campo gravitacional virtual em seu redor: quando o cursor do mouse se aproxima do raio do botão (`range: 45px`), o botão é atraído elasticamente em direção às coordenadas do ponteiro através de duas molas desacopladas nos eixos X e Y. Ao sair do raio, o botão retorna instantaneamente para a posição de repouso com desaceleração amortecida.
- **Gatilho de Interação**: Evento de `onMouseMove` sobre a área delimitada pelo bounding rect.
- **Onde encaixar na página**: Botão de CTA principal no Hero, botão de download no header e disparador de conversão no rodapé.

### 9. Dynamic Island Micro-Loader (`dynamic-island`)
- **Anatomia Visual**: Pílula negra ultracompacta (`rounded-full`) com borda sutil em `border-white/10`. Anima continuamente a largura horizontal entre 80px e 110px em ritmo respiratório, exibindo em seu interior um ponto de status verde esmeralda piscante (`bg-emerald-500`) acompanhado de três barras oscilantes de waveform de áudio.
- **Gatilho de Interação**: Execução automática em loop (`Infinity`) durante carregamentos de segundo plano ou sincronizações.
- **Onde encaixar na página**: Barra de status superior de dashboards, indicadores de estado de conexão e notificações dinâmicas flutuantes.

### 10. Face ID Scan Loader (`face-id-scan`)
- **Anatomia Visual**: Retículo biométrico composto pelos quatro cantos em ângulo reto de um quadrado com bordas arredondadas. Uma linha horizontal luminosa de varredura a laser desliza verticalmente em ciclo contínuo, transmitindo uma sensação instantânea de autenticação e criptografia de ponta a ponta.
- **Gatilho de Interação**: Auto-play contínuo durante validações de segurança ou login.
- **Onde encaixar na página**: Modais de autenticação em duas etapas (2FA), telas de checkout seguro e desbloqueio de chaves criptográficas.

### 11. Wave Physics Loader (`wave-physics-loader`)
- **Anatomia Visual**: Padrão de 5 a 7 esferas que oscilam verticalmente em fases defasadas calculadas através de funções de onda senoidal harmônica, produzindo uma simulação física de fluido incompressível sem exigir WebGL.
- **Gatilho de Interação**: Loop contínuo com transições de mola suaves.
- **Onde encaixar na página**: Estados de carregamento de gráficos, skeletons e placeholders de carregamento assíncrono de mídia.

### 12. Hook useWebHaptics (`use-web-haptics`)
- **Anatomia Visual & Acústica**: Utilitário headless indispensável que unifica síntese de frequências acústicas (Web Audio API) e impulsos motores vibratórios (Vibration API). Oferece métodos diretos `trigger('light')`, `trigger('success')`, `trigger('error')`, `trigger('heavy')` e `toggleSound()`, integrando-se organicamente a qualquer botão ou gatilho da aplicação.
- **Gatilho de Interação**: Chamadas programáticas nos manipuladores de evento `onClick`, `onCopy`, `onDrop` e `onSubmit`.
- **Onde encaixar na página**: Camada global de hooks e providers de interação da aplicação.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Pacotes

Para incorporar o aMicro em um projeto React moderno (React 19 ou React 18 com Next.js App Router ou Vite), instale os pacotes fundamentais:

```bash
npm install motion clsx tailwind-merge lucide-react web-haptics
# ou caso utilize a biblioteca oficial completa:
npm install @subhanhq/amicro
```

### Configuração do Shadcn Registry

O aMicro adota a arquitetura de distribuição descentralizada baseada no Shadcn CLI. É possível configurar o namespace `@amicro` diretamente no seu arquivo `components.json`:

```json
{
  "$schema": "https://ui.shadcn.com/schema.json",
  "style": "default",
  "rsc": true,
  "tsx": true,
  "tailwind": {
    "config": "tailwind.config.js",
    "css": "src/app/globals.css",
    "baseColor": "zinc"
  },
  "aliases": {
    "components": "@/components",
    "utils": "@/lib/utils"
  },
  "registries": {
    "@amicro": "https://amicro.vercel.app/r/{name}.json"
  }
}
```

Após configurar o registro, qualquer componente pode ser instalado via comando único do terminal:

```bash
# Adicionar componentes de cartões espaciais
npx shadcn add @amicro/card-arc-5
npx shadcn add @amicro/card-time-machine
npx shadcn add @amicro/card-carousel

# Adicionar componentes para IA
npx shadcn add @amicro/ai-prompt-input
npx shadcn add @amicro/ai-reasoning-trace

# Adicionar micro-interações de hover e hooks
npx shadcn add @amicro/magnetic-button
npx shadcn add @amicro/use-web-haptics
npx shadcn add @amicro/presets
```

Alternativamente, utilize a CLI nativa da biblioteca:
```bash
npx @subhanhq/amicro@latest init
npx @subhanhq/amicro@latest add card-arc-5
```

---

### Tabela Oficial de Presets de Física de Mola (`presets.ts`)

O aMicro padroniza todas as suas transições através de um conjunto fixo de constantes de mola calculadas para diferentes graus de urgência e resposta tátil:

| Preset | `type` | `stiffness` | `damping` | `mass` | Sensação Tátil & Caso de Uso |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **`snappy`** | `spring` | `400` | `28` | `0.8` | Ultra-responsivo, estalo seco e preciso. Ideal para botões de ação e tabs. |
| **`bouncy`** | `spring` | `300` | `15` | `1.0` | Divertido e elástico, com rebote evidente. Excelente para chips e badges. |
| **`smooth`** | `spring` | `220` | `24` | `1.0` | Transição padrão elegante e suave. Ideal para modais e expansão de menus. |
| **`gentle`** | `spring` | `120` | `14` | `1.0` | Movimento calmo e desacelerado. Perfeito para revelação de texto e cartões. |
| **`stiff`** | `spring` | `500` | `40` | `0.5` | Alta tensão com quase zero oscilação. Essencial para rastreadores de cursor. |

---

### Receita de Código Funcional e Completa: `CardArcInteractive` com Háptica Integrada

O código abaixo reproduz a mecânica mais emblemática do aMicro: o leque de 5 cartões com física parabólica (`CardArc5`), integrado ao hook multissensorial `useWebHaptics` para emitir som sintético e vibração ao abrir o leque ou selecionar um cartão.

```tsx
"use client";

import React, { useState, useCallback, useRef } from "react";
import { motion, useReducedMotion } from "motion/react";
import { Sparkles, Check, ArrowRight, ShieldCheck, Zap } from "lucide-react";

// ==========================================
// 1. Hook useWebHaptics (Web Audio API & Vibration)
// ==========================================
export type HapticType = "light" | "medium" | "heavy" | "success" | "error";

export function useWebHaptics() {
  const audioCtxRef = useRef<AudioContext | null>(null);

  const getAudioContext = useCallback(() => {
    if (typeof window === "undefined") return null;
    if (!audioCtxRef.current) {
      const AudioCtx = window.AudioContext || (window as any).webkitAudioContext;
      if (AudioCtx) {
        audioCtxRef.current = new AudioCtx();
      }
    }
    if (audioCtxRef.current && audioCtxRef.current.state === "suspended") {
      audioCtxRef.current.resume();
    }
    return audioCtxRef.current;
  }, []);

  const trigger = useCallback((type: HapticType = "light") => {
    // 1. Áudio sintetizado de precisão mecânica
    const ctx = getAudioContext();
    if (ctx) {
      try {
        const now = ctx.currentTime;
        const osc = ctx.createOscillator();
        const gain = ctx.createGain();

        osc.connect(gain);
        gain.connect(ctx.destination);

        if (type === "success") {
          osc.type = "sine";
          osc.frequency.setValueAtTime(820, now);
          osc.frequency.exponentialRampToValueAtTime(1240, now + 0.06);
          gain.gain.setValueAtTime(0.035, now);
          gain.gain.exponentialRampToValueAtTime(0.0001, now + 0.14);
          osc.start(now);
          osc.stop(now + 0.14);
        } else {
          osc.type = "triangle";
          const freq = type === "heavy" ? 1100 : type === "medium" ? 1400 : 1750;
          osc.frequency.setValueAtTime(freq, now);
          osc.frequency.exponentialRampToValueAtTime(freq * 0.5, now + 0.02);
          gain.gain.setValueAtTime(0.025, now);
          gain.gain.exponentialRampToValueAtTime(0.0001, now + 0.025);
          osc.start(now);
          osc.stop(now + 0.025);
        }
      } catch {
        // Fallback não-bloqueante
      }
    }

    // 2. Vibração de hardware no mobile
    if (typeof window !== "undefined" && navigator?.vibrate) {
      try {
        const durations: Record<HapticType, number | number[]> = {
          light: 10,
          medium: 25,
          heavy: 50,
          success: [15, 60, 15],
          error: [60, 60, 60],
        };
        navigator.vibrate(durations[type] ?? 10);
      } catch {}
    }
  }, [getAudioContext]);

  return { trigger };
}

// ==========================================
// 2. Componente de Cartão em Leque Parabólico
// ==========================================
interface CardItem {
  id: string;
  title: string;
  subtitle: string;
  icon: React.ReactNode;
  gradient: string;
}

const DEMO_CARDS: CardItem[] = [
  { id: "c1", title: "Standard", subtitle: "Zero fees", icon: <ShieldCheck className="w-4 h-4" />, gradient: "from-zinc-800 to-zinc-900" },
  { id: "c2", title: "Premium", subtitle: "2.5% Cashback", icon: <Zap className="w-4 h-4 text-amber-400" />, gradient: "from-amber-950/60 to-zinc-900" },
  { id: "c3", title: "Founders", subtitle: "Limitless", icon: <Sparkles className="w-4 h-4 text-emerald-400" />, gradient: "from-emerald-950/60 to-zinc-900" },
  { id: "c4", title: "Enterprise", subtitle: "Custom terms", icon: <ShieldCheck className="w-4 h-4 text-blue-400" />, gradient: "from-blue-950/60 to-zinc-900" },
  { id: "c5", title: "Black Edition", subtitle: "Concierge 24/7", icon: <Sparkles className="w-4 h-4 text-purple-400" />, gradient: "from-purple-950/60 to-zinc-900" },
];

export function CardArcSpread() {
  const [isHovered, setIsHovered] = useState(false);
  const [selectedCard, setSelectedCard] = useState<number | null>(2);
  const { trigger: triggerHaptic } = useWebHaptics();
  const prefersReducedMotion = useReducedMotion();

  const angle = 28;
  const gap = 85;
  const yOffset = 12;
  const centerIndex = 2; // Cartão central do array de 5 itens

  const handleMouseEnter = () => {
    setIsHovered(true);
    triggerHaptic("light");
  };

  const handleMouseLeave = () => {
    setIsHovered(false);
  };

  const handleSelect = (index: number) => {
    setSelectedCard(index);
    triggerHaptic("success");
  };

  return (
    <div className="flex flex-col items-center justify-center p-8 bg-zinc-950 rounded-2xl border border-white/10 shadow-2xl overflow-hidden max-w-xl mx-auto">
      {/* Cabeçalho */}
      <div className="text-center mb-10">
        <span className="text-xs uppercase font-mono tracking-widest text-emerald-400 font-semibold">
          Spatial Arc Mechanics
        </span>
        <h3 className="text-xl font-bold text-white tracking-tight mt-1">
          Select Your Active Tier
        </h3>
        <p className="text-xs text-zinc-400 mt-1">
          Passe o cursor sobre os cartões para abrir o leque parabólico com áudio háptico.
        </p>
      </div>

      {/* Área do Leque de Cartões */}
      <div
        onMouseEnter={handleMouseEnter}
        onMouseLeave={handleMouseLeave}
        className="relative w-44 h-64 flex items-center justify-center cursor-pointer select-none"
      >
        {DEMO_CARDS.map((card, i) => {
          const dist = i - centerIndex;
          
          // Cálculo trigonométrico e parabólico da dispersão
          const targetRotate = !prefersReducedMotion && isHovered
            ? dist * (angle / centerIndex)
            : 0;

          const targetX = !prefersReducedMotion && isHovered
            ? dist * (gap / centerIndex)
            : 0;

          // Parábola no eixo vertical: cartões extremos descem, central sobe
          let targetY = 0;
          if (!prefersReducedMotion && isHovered) {
            if (Math.abs(dist) === 2) targetY = yOffset;
            else if (Math.abs(dist) === 1) targetY = -0.2 * yOffset;
            else targetY = -yOffset * 1.5;
          }

          const isSelected = selectedCard === i;

          return (
            <motion.div
              key={card.id}
              onClick={() => handleSelect(i)}
              animate={{
                rotate: targetRotate,
                x: targetX,
                y: targetY,
                scale: isSelected ? 1.05 : 1,
                zIndex: isSelected ? 30 : 20 - Math.abs(dist),
              }}
              transition={{
                type: "spring",
                stiffness: 380,
                damping: 26,
                mass: 0.8,
              }}
              className={`absolute top-0 w-44 h-60 rounded-xl p-4 flex flex-col justify-between border shadow-lg bg-gradient-to-b ${card.gradient} ${
                isSelected
                  ? "border-emerald-500 shadow-emerald-500/20 ring-1 ring-emerald-500/50"
                  : "border-white/10 hover:border-white/30"
              }`}
            >
              <div className="flex items-center justify-between">
                <span className="p-1.5 rounded-lg bg-white/5 border border-white/10">
                  {card.icon}
                </span>
                {isSelected && (
                  <span className="flex items-center justify-center w-5 h-5 rounded-full bg-emerald-500 text-black">
                    <Check className="w-3 h-3 stroke-[3]" />
                  </span>
                )}
              </div>

              <div>
                <h4 className="text-sm font-semibold text-white tracking-tight">
                  {card.title}
                </h4>
                <p className="text-[11px] font-medium text-zinc-400 mt-0.5">
                  {card.subtitle}
                </p>
              </div>
            </motion.div>
          );
        })}
      </div>

      {/* Rodapé Informativo */}
      <div className="mt-12 flex items-center gap-2 text-xs text-zinc-400">
        <span>Cartão ativo:</span>
        <span className="font-semibold text-white">
          {selectedCard !== null ? DEMO_CARDS[selectedCard].title : "Nenhum"}
        </span>
      </div>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir o documento de especificação de arquitetura de um novo projeto (`DESIGN_BLUEPRINT.md`), siga as instruções pragmáticas abaixo para incorporar o **aMicro**:

### 1. Declaração do Registro no Blueprint
Inclua explicitamente a URL do registro Shadcn e a versão dos pacotes de movimento:
```markdown
### Design System & Motion Stack
- **Primitives**: Shadcn UI (Radix UI)
- **Micro-Interactions & Haptics**: aMicro (`https://amicro.vercel.app/`)
  - Registro configurado: `@amicro: https://amicro.vercel.app/r/{name}.json`
  - Pacote core: `motion@^12.0.0`
  - Motor sensorial: `useWebHaptics` com `Web Audio API` e `Vibration API`
```

### 2. Mapeamento de Papéis na Regra 60-30-10
Defina rigidamente quais componentes pertencem à camada de 30% e quais são showstoppers de 10%:
- **Camada de Fluidez e Feedback (30%)**:
  - `MagneticButton`: obrigatório nos botões principais de conversão (`Hero CTA`, `Pricing Checkout`).
  - `useWebHaptics`: disparado em eventos de `copy-to-clipboard`, confirmação de pagamento e envio de prompts.
  - `DynamicIsland` ou `TerminalLoader`: usados nos estados de carregamento assíncrono de requisições.
- **Camada Showstopper (10%)**:
  - `CardArc5` / `CardArc7`: reservado para a vitrine visual principal de planos ou cartões de benefícios no Hero ou Pricing.
  - `DitherDonutChart`: elemento de destaque no quadrante superior do dashboard de telemetria.
  - `AiReasoningTrace`: acionado apenas quando o backend de IA emitir passos de raciocínio detalhados (*reasoning tokens*).

### 3. Presets de Mola Obrigatórios
Proíba parâmetros avulsos ou arbitrários de transição. Exija que os desenvolvedores importem os presets padronizados de `@amicro/presets`:
```typescript
import { presets } from "@/lib/amicro/presets";

// Correto:
<motion.div transition={presets.snappy} />

// Incorreto (anti-padrão):
<motion.div transition={{ duration: 0.3, ease: "linear" }} />
```

### 4. Checklist de Acessibilidade & Movimento Reduzido
Toda implementação de componentes espaciais do aMicro DEVE incluir:
1. `useReducedMotion()`: fallbacks para desativar rotações angulares parabólicas e translações no eixo Z caso o usuário tenha configurado sensibilidade a movimento no sistema operacional.
2. Controle Global de Som: persistência em `localStorage` com chave `amicro_sound_enabled` e switch acessível no menu de configurações para mutar sínteses de áudio a qualquer momento.
3. Atributos ARIA adequados: `aria-expanded` para o `AiReasoningTrace`, `role="tab"` para carrosséis e `aria-live="polite"` para os micro-loaders de status.
