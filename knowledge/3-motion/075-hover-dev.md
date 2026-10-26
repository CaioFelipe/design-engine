---
id: "hover-dev"
name: "Hover.dev (Animated UI Components for React & Tailwind)"
url: "https://www.hover.dev/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["Tactile Cursor Tracking", "Spring Physics & Inertia", "3D Perspective Tilting", "Clip-Path Mask Transitions", "Cyber-Clean Kinetic Delight", "Morphing Surface Layouts"]
densidade_informacao: "Media a Alta"
impacto_visual: "Moderado a Cinematografico/Showstopper"
custo_computacional: "Baixo a Medio (Framer Motion RAF + GPU-accelerated transforms & SVG filters)"
stack_frameworks: ["React 19 / 18", "Framer Motion / Motion", "Tailwind CSS v3 / v4", "TypeScript", "Lucide React"]
compatibilidade:
  combinacoes_recomendadas: ["Shadcn UI", "Tailwind CSS v4", "Lenis Smooth Scroll", "Next.js App Router", "Radix UI Primitives", "Lucide React"]
  conflitos_esteticos: ["Interfaces bancárias ou enterprise ultra-estáticas sem micro-interações", "Aplicações de formulários repetitivos onde o tilt ou scramble cause distração cognitiva", "Páginas com múltiplos loops visuais infinitos competindo simultaneamente pela atenção do usuário"]
---

# Hover.dev — Dossiê de Física de Movimento, Transições & Micro-Interações

## 1. Filosofia de Movimento & Sensação Física (Feel)

O **Hover.dev** (`https://www.hover.dev/`), concebido e mantido por **Tom Phillips** (conhecido publicamente como **Tom Is Loading**), consolidou-se como a principal referência prática em **micro-interações táteis, físicas e cinematográficas** para a web moderna construída sobre o ecossistema **React**, **Tailwind CSS** e **Framer Motion (Motion)**.

### A Filosofia Central: De Telas Planas a Superfícies Hápticas Reativas

A web tradicional opera sob o paradigma do *clique e resposta assíncrona*: elementos permanecem estáticos até que uma ação seja consumada. O Hover.dev inverte essa premissa ao transformar qualquer nó da interface em um **objeto físico tridimensional reativo** dotado de massa, atrito, reflexo especular e tensão elástica:

1. **Aderência ao Ponteiro (Tactile Cursor Tracking)**:
   Em vez de simples estados `:hover` com transições CSS lineares de cor, os componentes do Hover.dev calculam continuamente as coordenadas normalizadas do cursor relative ao retângulo delimitador do elemento ($x \in [-0.5, +0.5], y \in [-0.5, +0.5]$). Essa posição alimenta funções trigonométricas e vetores de rotação que inclinam o elemento no espaço euclidiano tridimensional (`rotateX`, `rotateY`, `scale3d`).

2. **Física Newtoniana vs. Curvas de Tempo Estáticas**:
   Todas as respostas mecânicas utilizam equações de **osciladores harmônicos amortecidos** (*Damped Harmonic Oscillators*). Quando o cursor do usuário deixa um cartão inclinado a 15 graus, o elemento não volta através de uma curva pré-fabricada de 200ms; ele é puxado por uma mola virtual de alta rigidez (`stiffness`), oscila sutilmente no ponto de equilíbrio e dissipa sua energia cinética de acordo com o coeficiente de amortecimento (`damping`).

3. **Iluminação Dinâmica e Sombras Especulares (Volumetria)**:
   O movimento mecânico é complementado por gradientes de luz pontual (*spotlight shine* / *radial glare*). Uma camada semitransparente acompanha o cursor com atraso e atenuação, simulando uma fonte de luz omnidirecional física a 100 pixels acima da superfície do monitor. Isso cria a ilusão neurológica de que o componente possui acabamento de vidro fosco, alumínio anodizado ou acrílico polido.

---

### Pipeline Arquitetural de Reatividade

```
┌────────────────────────────────────────────────────────────────────────┐
│                      HOVER.DEV INTERACTION PIPELINE                    │
└────────────────────────────────────────────────────────────────────────┘
                                   │
                   Pointer Event (onPointerMove)
                                   │
                                   ▼
         ┌──────────────────────────────────────────────────┐
         │ 1. Leitura Espacial: getBoundingClientRect()     │
         │    Cálculo Normalizado:                          │
         │    xPct = (clientX - left) / width - 0.5         │
         │    yPct = (clientY - top) / height - 0.5         │
         └──────────────────────────────────────────────────┘
                                   │
                 ┌─────────────────┴─────────────────┐
                 ▼                                   ▼
   ┌───────────────────────────┐       ┌───────────────────────────┐
   │ 2. Motion Values Dinâmicos│       │ 3. Gradiente de Brilho    │
   │    useMotionValue(x, y)   │       │    useTransform(xPct, y)  │
   │    useSpring({ stiff, damp│       │    background: radial(...)│
   └───────────────────────────┘       └───────────────────────────┘
                 │                                   │
                 └─────────────────┬─────────────────┘
                                   ▼
         ┌──────────────────────────────────────────────────┐
         │ 4. GPU-Composited Transformations                │
         │    transform: perspective(1000px)                │
         │               rotateX(deg) rotateY(deg)          │
         │    preserve-3d + translateZ nas camadas filhas   │
         └──────────────────────────────────────────────────┘
```

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

O Hover.dev é projetado especificamente para converter **pontos de atrito ou apatia visual** em **momentos de deleite interativo memorável**.

### Seções Críticas de Alto Impacto
- **Hero Sections de Alta Conversão**: Efeitos dinâmicos como o *Aurora Hero* e botões *Encrypt / Scramble* capturam imediatamente o engajamento do visitante no primeiro segundo de navegação.
- **Grades de Preço & Planos (Pricing Cards)**: O uso de *Tilt Shine Cards* no plano "Pro / Mais Popular" confere peso tátil e valor percebido premium imediato.
- **Sistemas de Navegação de Alto Nível (Navbars & Tabs)**: O padrão *Slide Tabs* e *Shifting Dropdown* (semelhante aos sistemas do Stripe e da Vercel) substitui menus estáticos por superfícies elásticas e fluidas onde o foco visual nunca sofre teleportes secos.
- **Carrosséis & Showcases de Portfólio**: Padrões de *Text Parallax Content* e *Horizontal Scroll Pins* criam uma experiência imersiva de narrativa editorial.

### A Regra 60-30-10 no Ecossistema Hover.dev

```
┌────────────────────────────────────────────────────────────────────────┐
│                       REGRA 60-30-10 DE MOVIMENTO                      │
├────────────────────────┬───────────────────────┬───────────────────────┤
│    60% DO SISTEMA      │     30% DO SISTEMA    │     10% DO SISTEMA    │
│  ESTRUTURA ESTÁVEL     │   FLUIDEZ INVISÍVEL   │   SHOWSTOPPER HERO    │
├────────────────────────┼───────────────────────┼───────────────────────┤
│ • Layouts estáticos    │ • Slide Tabs na nav   │ • Tilt 3D com Glare   │
│ • Tipografia legível   │ • Dropdowns mórficos  │ • Aurora Mesh Loop    │
│ • Grids consistentes   │ • Micro-press táteis  │ • Scramble Encrypt    │
│ • Cores sólidas/fundo  │ • Inércia de springs  │ • Drag & Stack Cards  │
└────────────────────────┴───────────────────────┴───────────────────────┘
```

1. **60% — Estrutura e Estabilidade**: A fundação do layout permanece perfeitamente ancorada no DOM sem movimentos gratuitos que cansem o olhar.
2. **30% — Fluidez Invisível (Hover.dev Utilities)**: O estado ativo dos menus se desloca com molas suaves (`Slide Tabs`), gavetas de menu adaptam altura e largura com animação fluida contínua (`Shifting Dropdowns`), e botões afundam de forma consistente com micro-press.
3. **10% — Espetáculo Visual (Showstopper Moments)**: O card central de destaque do produto reage ao mouse com inclinação 3D vigorosa e reflexo de brilho especular; o botão primário de conversão decodifica seu texto com uma cifra hacker estilizada.

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Quando Evitar
1. **Tabelas de Dados Densas e Dashboards Analíticos**:
   - Nunca aplique *Tilt Cards* ou *Bouncy Cards* em linhas de tabelas financeiras, listas de transações ou grids densos com mais de 20 itens simultâneos. A proliferação de ouvintes `pointermove` e transformações 3D ativas causa sobrecarga de repaint e distrai o operador humano.
2. **Dispositivos Móveis e Superfícies Touch Puras**:
   - O paradigma do Hover.dev depende intrinsecamente do estado de `hover` contínuo. Em telas sensíveis ao toque, o primeiro toque pode acionar um estado de tilt permanente ou congelado, bloqueando o scroll vertical natural. Use `window.matchMedia('(hover: hover)')` ou ative touch-fallbacks simplificados.
3. **Fluxos de Checkout e Autenticação Crítica**:
   - Evite efeitos de desconstrução textual (*Encrypt Button*) ou deformações elásticas exageradas em botões como "Confirmar Pagamento de R$ 5.000" ou "Excluir Conta". Em momentos de estresse cognitivo, o usuário exige previsibilidade, seriedade e ausência absoluta de latência percebida.

### ⚠️ Regras Estritas de Acessibilidade & GPU

1. **Respeito Absoluto a `prefers-reduced-motion`**:
   - Usuários com distúrbios vestibulares sofrem náusea e tontura severa com inclinações de perspectiva 3D e rotações dinâmicas contínuas.
   - Todo componente com tilt, rotação ou aurora deve verificar `useReducedMotion()` do Framer Motion e degradar imediatamente para transições simples de opacidade ou contorno estático.

2. **Prevenção de Subpixel Blurring em Fontes (Texto Borrado em 3D)**:
   - A ativação de `transform: perspective(...) rotateX(...)` força a GPU a rasterizar o texto em texturas de baixa precisão caso o elemento pai não esteja isolado.
   - **Remédio Técnico**: Mantenha o texto com `transform: translateZ(30px)` e aplique `backface-visibility: hidden` e `-webkit-font-smoothing: subpixel-antialiased` no contêiner.

3. **Gerenciamento do Stacking Context e Z-Index**:
   - Elementos com `transform-style: preserve-3d` furam as hierarquias tradicionais de `z-index`. Modais e tooltips podem ser renderizados atrás do cartão tridimensional se o contexto de empilhamento global não estiver rigidamente orquestrado com `isolation: isolate`.

---

## 4. Catálogo Detalhado de Componentes, Padrões & Efeitos Notáveis

### 1. Hover Tilt Shine Card (3D Perspective Card)
- **Comportamento Visual**: O cartão detecta a posição do mouse e se inclina em direção oposta à ponta do ponteiro (canto superior esquerdo empurrado para dentro, canto inferior direito projetado para frente). Uma camada de brilho radial translúcido acompanha o cursor exatamente no ponto focal. Ao retirar o mouse, o card retorna suavemente ao plano $0^\circ$ com mola amortecida.
- **Gatilho**: Evento `onPointerMove` sobre a área delimitadora; mola de reset no `onPointerLeave`.
- **Onde Encaixar**: Cartões de planos de assinatura (Pricing), cartões de projetos em destaque, capas de produtos em e-commerces de luxo.

### 2. Slide Tabs (Floating Pill Navigation)
- **Comportamento Visual**: Uma barra de abas horizontal onde a pílula de fundo ativa (background pill) desliza com física elástica orgânica entre as opções conforme o usuário move o mouse sobre elas ou clica em uma seleção. Se o mouse sai do grupo, a pílula volta instantaneamente para a aba ativa fixa.
- **Gatilho**: `onMouseEnter` individual em cada nó de aba para pré-visualização; `onClick` para fixação de estado.
- **Onde Encaixar**: Barra de navegação principal (Header), filtros de categoria em galerias, seletores de período em gráficos (Dia / Semana / Mês).

### 3. Shifting Dropdown (Morphing Nav Container)
- **Comportamento Visual**: Inspirado na navegação icônica do Stripe e Linear. Conforme o usuário transita entre links do menu superior ("Produtos", "Soluções", "Preços"), a janela de dropdown não fecha e reabre; seu contêiner físico realiza um morphing contínuo de largura, altura e posição horizontal, enquanto a seta indicadora (caret) desliza para o centro exato do link ativo.
- **Gatilho**: Hover nos itens da lista do cabeçalho com debouncing espacial coordenado.
- **Onde Encaixar**: Cabeçalhos de plataformas SaaS complexas com submenus de densidade de conteúdo variada.

### 4. Encrypt / Scramble Button (Cyberpunk Decryption Effect)
- **Comportamento Visual**: Ao posicionar o cursor sobre o botão, os caracteres do texto original começam a se transformar em uma torrente veloz de símbolos e caracteres aleatórios (`!@#$%^&*?~`), desacelerando gradualmente da esquerda para a direita até reconstituir o texto original com precisão tipográfica.
- **Gatilho**: `onMouseEnter` no botão.
- **Onde Encaixar**: Botões de ação primária (CTA) em produtos de desenvolvedores, cibersegurança, inteligência artificial, web3 ou consoles de terminal.

### 5. Bouncy / Spring Cards (Elastic Feature Cards)
- **Comportamento Visual**: Cartões que reagem com deformações elásticas visíveis ao clique e arraste. Quando clicados, sofrem compressão com escala reduzida ($0.95$) e, ao serem soltos, disparam uma oscilação elástica nítida com ressalto perceptível antes de estacionar.
- **Gatilho**: Estados `whileHover={{ scale: 1.03 }}` e `whileTap={{ scale: 0.94 }}` com perfil de spring agressivo.
- **Onde Encaixar**: Grades de benefícios (Features Grid), seleção de avatares, cartões colecionáveis interativos.

### 6. Aurora Hero (Fluid Ambient Gradient Mesh)
- **Comportamento Visual**: Uma atmosfera luminosa suave e hipnótica no topo da página composta por múltiplos gradientes radiais em cores quentes/frias (ciano, violeta, magenta) que se deformam, rotacionam e mudam de escala lentamente em ciclos contínuos com `mix-blend-mode: screen` ou `overlay`.
- **Gatilho**: Animação contínua em loop infinito (`repeat: Infinity, repeatType: "mirror"`), combinada com desfoque gaussiano extremo (`filter: blur(80px)`).
- **Onde Encaixar**: Fundo da seção inicial (Hero) de landing pages institucionais e páginas de lançamento de produtos.

### 7. Clip-Path Reveal Links (Geometric Masking Shift)
- **Comportamento Visual**: Um link de texto comum que, ao receber o hover, revela uma camada duplicada com cor contrastante ou tipografia com peso diferente através de um polígono de recorte dinâmico (`clip-path: polygon(...)`) que corta diagonalmente o elemento de $0\%$ a $100\%$.
- **Gatilho**: `onMouseEnter` disparando transição de coordenadas de clip-path.
- **Onde Encaixar**: Rodapés minimalistas, menus full-screen de estúdios criativos, links de biografia em portfólios autorais.

### 8. Text Parallax Content (Scroll-Pinned Feature Showcase)
- **Comportamento Visual**: Uma seção com rolagem sticky onde uma imagem de fundo monumental com máscara é fixada na viewport enquanto o bloco de texto explicativo se desloca verticalmente em velocidade diferencial, sofrendo uma transição suave de escala e opacidade no início e saída da tela.
- **Gatilho**: Scroll progress mapeado via `useScroll` e interpolado com `useTransform`.
- **Onde Encaixar**: Seções de apresentação de produto em estilo Apple, narrativas de manifesto de marca, estudos de caso profundos.

### 9. Drag & Stack Cards (Physics Flick & Handover)
- **Comportamento Visual**: Uma pilha de cartões sobrepostos com rotações angulares randômicas sutis. O usuário pode arrastar o cartão do topo em qualquer direção vetorial. Se a velocidade ou a distância ultrapassarem um limiar pré-definido, o cartão é "arremessado" para fora da tela com handover de inércia e o próximo cartão da pilha sobe elasticamente.
- **Gatilho**: Gesto de arrastar do Framer Motion (`drag`, `dragConstraints`, `onDragEnd`).
- **Onde Encaixar**: Sessões de depoimentos de clientes (Testimonials), galerias de fotos de equipe, fluxos de onboarding interativos estilo Tinder.

### 10. Neubrutalism Tactile Button (Hard Shadow Displacement)
- **Comportamento Visual**: Um botão com borda preta espessa de 2px a 3px e uma sombra sólida rígida projetada para o canto inferior direito sem desfoque (`box-shadow: 4px 4px 0px #000`). Ao ser clicado (`active`), o corpo do botão se desloca exatamente $4\text{px}$ em $X$ e $Y$, zerando a sombra e simulando o pressionamento de uma tecla mecânica real.
- **Gatilho**: Estado `:active` ou Framer Motion `whileTap={{ x: 4, y: 4 }}`.
- **Onde Encaixar**: Aplicações com identidade neobrutalista, portfólios descolados, ferramentas para desenvolvedores e plataformas web3 contemporâneas.

---

## 5. Matemática do Movimento & Receitas de Código

### Parâmetros Físicos e Constantes de Mola

O Framer Motion e o Hover.dev utilizam a equação diferencial clássica do oscilador amortecido:
$$F = -k \cdot x - c \cdot v$$
Onde:
- $k$ é a rigidez (**stiffness**): quanto maior, mais rápida e agressiva é a força restauradora.
- $c$ é o coeficiente de amortecimento (**damping**): quanto menor, mais tempo o elemento continuará oscilando antes do repouso; quanto maior, mais denso/viscoso parecerá o ambiente.
- $m$ é a massa (**mass**): a inércia do corpo.

#### Matriz de Configuração de Springs Recomendada pelo Hover.dev

| Perfil de Movimento | Componentes Indicados | Stiffness ($k$) | Damping ($c$) | Mass ($m$) | Rest Delta | Sensação Tátil |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Snappy / Crisp** | Slide Tabs, Nav Carets, Switches | `400` | `30` | `0.8` | `0.001` | Resposta instantânea com parada limpa e zero oscilação excessiva |
| **Bouncy / Playful**| Bouncy Cards, Badges, Modais | `280` | `15` | `1.0` | `0.005` | Efeito elástico vibrante com 2-3 oscilações orgânicas visíveis |
| **Fluid / Heavy** | Shifting Dropdown, Modais Grandes | `200` | `24` | `1.2` | `0.01` | Sensação de vidro espesso ou peça de alumínio usinado |
| **Soft Cursor Tilt**| Hover Tilt Card (Mouse Tracking) | `150` | `15` | `0.5` | `0.001` | Movimento que segue o cursor como se flutuasse em fluido viscoso |

#### Curvas Bézier Equivalentes (Para Transições Determinísticas de CSS)
Para micro-transições que utilizam CSS puro em nós de baixa prioridade:
- **Ease-Out-Expo (Snappy Pop)**: `cubic-bezier(0.16, 1, 0.3, 1)`
- **Fluid Soft Glide**: `cubic-bezier(0.25, 1, 0.5, 1)`

---

### Receita de Código Funcional 1: Hover Tilt Shine Card Completo

Este componente representa a essência técnica do Hover.dev: tracking normalizado de coordenadas, molas suaves via `useSpring`, iluminação por gradiente radial móvel e elevação espacial 3D com respeito total a `prefers-reduced-motion`.

```tsx
import React, { useRef } from "react";
import {
  motion,
  useMotionTemplate,
  useMotionValue,
  useSpring,
  useReducedMotion,
} from "framer-motion";
import { ArrowUpRight, Sparkles } from "lucide-react";

interface TiltShineCardProps {
  title: string;
  category: string;
  description: string;
}

export const HoverTiltShineCard: React.FC<TiltShineCardProps> = ({
  title,
  category,
  description,
}) => {
  const cardRef = useRef<HTMLDivElement>(null);
  const shouldReduceMotion = useReducedMotion();

  // Valores normalizados de -0.5 a 0.5
  const rawX = useMotionValue(0);
  const rawY = useMotionValue(0);

  // Posição percentual para o gradiente de brilho (0% a 100%)
  const glareX = useMotionValue(50);
  const glareY = useMotionValue(50);

  // Molas com amortecimento para retorno e interpolação aveludada
  const springConfig = { stiffness: 180, damping: 18, mass: 0.6 };
  const smoothX = useSpring(rawX, springConfig);
  const smoothY = useSpring(rawY, springConfig);

  // Mapeamento angular: inclinação máxima de 14 graus
  // Rotação em X responde ao movimento vertical (Y)
  // Rotação em Y responde ao movimento horizontal (X)
  const dynamicRotateX = useMotionTemplate`${smoothY}deg`;
  const dynamicRotateY = useMotionTemplate`${smoothX}deg`;

  const handlePointerMove = (e: React.PointerEvent<HTMLDivElement>) => {
    if (shouldReduceMotion || !cardRef.current) return;

    const rect = cardRef.current.getBoundingClientRect();
    const width = rect.width;
    const height = rect.height;

    const mouseX = e.clientX - rect.left;
    const mouseY = e.clientY - rect.top;

    // Normalização: centro da carta é (0, 0)
    const normalizedX = (mouseX / width - 0.5) * 28; // -14 a +14 deg
    const normalizedY = (mouseY / height - 0.5) * -28; // Invertido para física correta

    rawX.set(normalizedX);
    rawY.set(normalizedY);

    // Mapeamento da luz em porcentagem
    glareX.set((mouseX / width) * 100);
    glareY.set((mouseY / height) * 100);
  };

  const handlePointerLeave = () => {
    rawX.set(0);
    rawY.set(0);
    glareX.set(50);
    glareY.set(50);
  };

  // Gradiente radial da luz especular
  const glareBackground = useMotionTemplate`radial-gradient(
    450px circle at ${glareX}% ${glareY}%,
    rgba(255, 255, 255, 0.12),
    transparent 80%
  )`;

  return (
    <div
      style={{ perspective: 1200 }}
      className="flex items-center justify-center p-6"
    >
      <motion.div
        ref={cardRef}
        onPointerMove={handlePointerMove}
        onPointerLeave={handlePointerLeave}
        style={{
          rotateX: shouldReduceMotion ? 0 : dynamicRotateX,
          rotateY: shouldReduceMotion ? 0 : dynamicRotateY,
          transformStyle: "preserve-3d",
        }}
        className="relative h-96 w-80 cursor-pointer rounded-2xl border border-neutral-800 bg-neutral-900/90 p-8 shadow-2xl transition-colors duration-300 hover:border-neutral-700 select-none overflow-hidden"
      >
        {/* Camada Dinâmica de Brilho Especular (Spotlight Glare) */}
        {!shouldReduceMotion && (
          <motion.div
            className="pointer-events-none absolute inset-0 z-10 transition-opacity duration-500"
            style={{ background: glareBackground }}
          />
        )}

        {/* Camada de Gradiente Sutil de Fundo */}
        <div className="pointer-events-none absolute -right-20 -top-20 h-56 w-56 rounded-full bg-violet-600/10 blur-3xl" />

        {/* Conteúdo com Profundidade Real (translateZ) */}
        <div
          style={{ transform: "translateZ(40px)" }}
          className="flex h-full flex-col justify-between"
        >
          <div className="flex items-center justify-between">
            <span className="inline-flex items-center gap-1.5 rounded-full border border-neutral-700/60 bg-neutral-800/80 px-3 py-1 text-xs font-medium text-neutral-300 backdrop-blur-md">
              <Sparkles className="h-3.5 w-3.5 text-violet-400" />
              {category}
            </span>
            <div className="rounded-full border border-neutral-700/50 p-2 text-neutral-400 transition-colors hover:text-white">
              <ArrowUpRight className="h-4 w-4" />
            </div>
          </div>

          <div className="space-y-2">
            <h3 className="text-2xl font-bold tracking-tight text-white">
              {title}
            </h3>
            <p className="text-sm leading-relaxed text-neutral-400">
              {description}
            </p>
          </div>

          <div className="flex items-center justify-between border-t border-neutral-800/80 pt-4">
            <span className="text-xs font-mono text-neutral-500">
              PHYSICS DRIVEN
            </span>
            <span className="text-xs font-semibold text-violet-400 hover:underline">
              Explorar Dossiê &rarr;
            </span>
          </div>
        </div>
      </motion.div>
    </div>
  );
};
```

---

### Receita de Código Funcional 2: Encrypt / Scramble Button

O famoso botão "cifra hacker" do Hover.dev, implementado com intervalos limpos em JavaScript e animação de ícone com Framer Motion.

```tsx
import React, { useRef, useState } from "react";
import { motion } from "framer-motion";
import { Lock } from "lucide-react";

const CHARS = "!@#$%^&*():{};|,.<>/?";
const CYCLES_PER_LETTER = 2;
const SHUFFLE_TIME = 35;

interface EncryptButtonProps {
  text?: string;
  onClick?: () => void;
}

export const EncryptButton: React.FC<EncryptButtonProps> = ({
  text = "DECRYPT TOKENS",
  onClick,
}) => {
  const [displayText, setDisplayText] = useState(text);
  const intervalRef = useRef<NodeJS.Timeout | null>(null);

  const scramble = () => {
    let pos = 0;

    if (intervalRef.current) clearInterval(intervalRef.current);

    intervalRef.current = setInterval(() => {
      const scrambled = text
        .split("")
        .map((char, index) => {
          if (pos / CYCLES_PER_LETTER > index) {
            return char;
          }

          const randomChar = CHARS[Math.floor(Math.random() * CHARS.length)];
          return randomChar;
        })
        .join("");

      setDisplayText(scrambled);
      pos++;

      if (pos >= text.length * CYCLES_PER_LETTER) {
        if (intervalRef.current) clearInterval(intervalRef.current);
        setDisplayText(text);
      }
    }, SHUFFLE_TIME);
  };

  const stopScramble = () => {
    if (intervalRef.current) clearInterval(intervalRef.current);
    setDisplayText(text);
  };

  return (
    <motion.button
      whileHover={{ scale: 1.025 }}
      whileTap={{ scale: 0.975 }}
      onMouseEnter={scramble}
      onMouseLeave={stopScramble}
      onClick={onClick}
      className="group relative flex items-center gap-2 overflow-hidden rounded-lg border border-neutral-700 bg-neutral-950 px-6 py-3 font-mono text-sm font-semibold text-neutral-200 transition-colors hover:border-violet-500 hover:text-white"
    >
      <Lock className="h-4 w-4 text-violet-400 transition-transform duration-300 group-hover:rotate-12" />
      <span className="relative z-10 tracking-wider">{displayText}</span>

      {/* Gradiente de fundo translúcido no hover */}
      <div className="absolute inset-0 z-0 -translate-x-full bg-gradient-to-r from-violet-600/20 to-indigo-600/20 transition-transform duration-300 ease-out group-hover:translate-x-0" />
    </motion.button>
  );
};
```

---

### Receita de Código Funcional 3: Slide Tabs (Floating Pill Navigation)

O padrão de menu superior moderno onde a pílula de fundo acompanha o hover e retorna suavemente para a posição padrão.

```tsx
import React, { useRef, useState } from "react";
import { motion } from "framer-motion";

interface TabProps {
  children: string;
  setPosition: (pos: { left: number; width: number; opacity: number }) => void;
  active?: boolean;
}

const Tab: React.FC<TabProps> = ({ children, setPosition, active }) => {
  const ref = useRef<HTMLLIElement>(null);

  return (
    <li
      ref={ref}
      onMouseEnter={() => {
        if (!ref.current) return;
        const { width } = ref.current.getBoundingClientRect();
        setPosition({
          left: ref.current.offsetLeft,
          width,
          opacity: 1,
        });
      }}
      className={`relative z-10 block cursor-pointer px-4 py-2 text-xs font-medium uppercase tracking-wider transition-colors md:px-5 md:py-2.5 md:text-sm ${
        active ? "text-white" : "text-neutral-400 hover:text-white"
      }`}
    >
      {children}
    </li>
  );
};

export const SlideTabs: React.FC = () => {
  const [position, setPosition] = useState({
    left: 0,
    width: 0,
    opacity: 0,
  });

  return (
    <nav className="flex justify-center p-4">
      <ul
        onMouseLeave={() => {
          setPosition((prev) => ({ ...prev, opacity: 0 }));
        }}
        className="relative mx-auto flex w-fit rounded-full border border-neutral-800 bg-neutral-900/90 p-1.5 backdrop-blur-md"
      >
        <Tab setPosition={setPosition} active>Home</Tab>
        <Tab setPosition={setPosition}>Recursos</Tab>
        <Tab setPosition={setPosition}>Preços</Tab>
        <Tab setPosition={setPosition}>Dossiês</Tab>
        <Tab setPosition={setPosition}>Contato</Tab>

        {/* Pílula Deslizante com Física de Spring */}
        <motion.li
          animate={{
            left: position.left,
            width: position.width,
            opacity: position.opacity,
          }}
          transition={{
            type: "spring",
            stiffness: 450,
            damping: 32,
          }}
          className="absolute z-0 h-9 rounded-full bg-neutral-800 md:h-10"
        />
      </ul>
    </nav>
  );
};
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao integrar padrões do **Hover.dev** nas especificações de arquitetura do `DESIGN_BLUEPRINT.md`, a inteligência artificial deve seguir a matriz de validação abaixo:

### 1. Declaração Explícita de Papéis na Regra 60-30-10
- Nunca declare "todo o site terá tilt 3D".
- Categorize estritamente os componentes selecionados:
  - **Showstopper (10%)**: Card do produto principal na Hero ou na grade de Pricing (`HoverTiltShineCard`).
  - **Fluidez Tátil (30%)**: Barra de navegação e filtros (`SlideTabs`), botões de ação especial (`EncryptButton`), morphing de menus (`ShiftingDropdown`).
  - **Fundação Estática (60%)**: Tipografia, tabelas, formulários de dados e grids de rodapé.

### 2. Especificação Numérica de Molas (Spring Specs)
No blueprint técnico, toda micro-interação deve conter sua assinatura de spring:
```markdown
### Motion Profile: Hero Action Cards
- Engine: Framer Motion / Motion
- Type: Physics Spring
- Stiffness: 200
- Damping: 20
- Mass: 0.8
- Reduced Motion Strategy: Desativar rotateX/rotateY, manter hover:border-violet-500 simples.
```

### 3. Checklist de Auditoria Técnica Pré-Código
- [ ] **Isolamento de Stacking Context**: O elemento pai possui `perspective: 1000px` ou `perspective: 1200px` declarado inline ou via classe utilitária do Tailwind (`[perspective:1000px]`)?
- [ ] **Preservação 3D**: Os elementos filhos possuem `transform-style: preserve-3d` e deslocamento em Z positivo (`translateZ(30px)`) para evitar subpixel blurring de texto?
- [ ] **Controle de Touch / Dispositivos Móveis**: Foi adicionado guard rail para que dispositivos sem ponteiro fino (`@media (hover: hover)`) não fiquem com o tilt travado?
- [ ] **Garantia de Acessibilidade**: `useReducedMotion()` implementado para suprimir rotações contínuas e textos cifrados caso solicitado pelo sistema operacional?
- [ ] **Performance de Repaint**: As propriedades manipuladas durante o movimento contínuo limitam-se a `transform` e `opacity` (componíveis por GPU), evitando reflows de `top`, `left`, `width` ou `height`?
