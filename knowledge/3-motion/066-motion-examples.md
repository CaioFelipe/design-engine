---
id: "motion-examples"
name: "Motion Examples"
url: "https://motion.dev/examples"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["Fluid Spring Physics", "Layout Projection / FLIP Invariance", "Kinetic Typography & Stagger", "Scroll-Linked Choreography", "Tactile Gesture Inertia", "Shared Element Morphing"]
densidade_informacao: "Independente"
impacto_visual: "Moderado a Cinematografico/Showstopper"
custo_computacional: "Baixo (WAAPI/Transforms) a Medio (JS Springs/RAF)"
stack_frameworks: ["React (motion/react v12+)", "Vanilla JavaScript (motion)", "Vue (motion/vue)", "Svelte", "Tailwind CSS v4 & v3", "Three.js / WebGL", "Lenis Smooth Scroll"]
compatibilidade:
  combinacoes_recomendadas: ["Shadcn UI + Motion Examples", "Lenis Scroll + useScroll/useTransform", "Radix Primitives + AnimatePresence", "Lucide Icons + Motion SVG Drawing", "Three.js / R3F + Motion Springs"]
  conflitos_esteticos: ["Animações puramente lineares sem easing natural (robóticas)", "Múltiplos elementos forçando reflow via width/height em vez de layout projection", "Delays em cascata excessivos (>800ms) em formulários de conversão crítica", "Ignorar prefers-reduced-motion em usuários com sensibilidade vestibular"]
---

# Motion Examples — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)

O laboratório de exemplos do **Motion** (`https://motion.dev/examples`, mantido por Matt Perry e pelo ecossistema Motion Division, anteriormente conhecido como Framer Motion) representa a referência técnica máxima no desenvolvimento de interfaces reativas baseadas em **física do mundo real**. 

Diferente das bibliotecas de animação clássicas da web — que operavam ancoradas em curvas de tempo fixo (como `ease-in-out` de 300ms) onde o movimento é uma interpolação mecânica e rígida —, o Motion adota a **Física de Molas Reais (Hooke's Law com Amortecimento Crítico)** como primitivo estrutural da interface.

### O Princípio da Interrupção Contínua (Interruptibility & Momentum)
Na web tradicional, quando um usuário interage com um elemento que já está no meio de uma transição de estado, a animação frequentemente estala, reinicia do zero ou congela em saltos bruscos. No ecossistema exemplificado pelo Motion:
- Toda animação é **inerentemente interruptível**: se um modal está abrindo e o usuário clica em cancelar, o vetor de velocidade atual (`current velocity`) é herdado instantaneamente pela mola de fechamento, sem quebra de frame.
- O gesto do ponteiro (drag/pan/flick) não apenas desloca a posição do elemento, mas **injeta momento balístico**. Quando o ponteiro se desengata, a inércia do movimento físico projeta o elemento adiante, desacelerando suavemente até o ponto de repouso geométrico mais próximo.

### Projeção de Layout sem Reflow (Layout Projection / FLIP Invariance)
Um dos gargalos históricos mais severos dos motores de renderização de navegadores (Blink, Gecko, WebKit) é o custo proibitivo do *Layout Thrashing* (cálculo de `reflow`). Animar propriedades geométricas como `width`, `height`, `top`, `left`, `padding` ou `flex-direction` força o navegador a recalcular a geometria de toda a árvore do DOM a cada frame, despencando a taxa de quadros de 60fps/120fps para menos de 20fps.

O padrão mestre dos exemplos do Motion resolve esse dilema através da **Projeção de Layout em GPU**:
1. O elemento é medido em seu estado de partida (origem) e em seu estado de chegada (destino) em coordenadas absolutas de tela (`getBoundingClientRect`).
2. A mutação do DOM ocorre de forma atômica e instantânea.
3. O Motion calcula a matriz de transformação diferencial invertida e aplica transformações puras de hardware (`transform: translate3d(...) scale3d(...)`), executadas exclusivamente na thread de composição da GPU.
4. Qualquer distorção visual em elementos filhos (como textos ou ícones esticando durante a escala) é anulada em tempo real por uma transformação inversa compensatória (`scale distortion correction`).

### O Ecosistema Unificado: WAAPI, Springs e Frame Loop
Com o renascimento da biblioteca sob a marca unificada `motion` (substituindo a antiga dependência atrelada estritamente ao Framer), os exemplos agora demonstram o uso de:
- **WAAPI Híbrida (Web Animations API)**: quando a animação possui parâmetros temporais definidos, o Motion delega a execução diretamente ao motor C++ do navegador, rodando fora da thread principal do JavaScript.
- **Micro-frame Loop Centralizado (`frame.update`, `frame.render`)**: sincronização de tarefas pesadas de física e leitura de scroll sob um único loop de `requestAnimationFrame`, eliminando leituras e escritas intercaladas no DOM.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados
1. **SaaS B2B Modernos, DevTools & Plataformas Operacionais (Padrão Linear / Vercel)**:
   - Indicadores de aba deslizante com pílula fluida (`layoutId="active-indicator"`).
   - Listas e tabelas com drag-and-drop multidimensional (`Reorder.Group` e `Reorder.Item`).
   - Painéis retráteis, accordions que expandem sem empurrões secos e janelas flutuantes com ancoragem magnética.
2. **E-Commerce High-End & Checkout Tátil**:
   - Trajetória balística parabólica ao adicionar produto ao carrinho (`Add to basket arc()`).
   - Cards de catálogo de produtos que se expandem suavemente para uma visão detalhada em tela cheia com retenção de imagem (`Shared Element Transition`).
   - Galerias de produtos imersivas (arranjos em Stack, Coverflow e Barrel 3D).
3. **Landing Pages Tecnológicas & Narrativas Guiadas por Scroll (Scrollytelling)**:
   - Revelação de tipografia palavra por palavra sincronizada com a rolagem (`Scroll word reveal` com `useScroll` e `useTransform`).
   - Efeitos de revelação de rodapé "Sticky Under-Page Reveal".
   - Parallax em múltiplas camadas de profundidade com integração a motores de smooth scroll (Lenis).
4. **Dashboards Financeiros, Métricas em Tempo Real & Gamificação**:
   - Odômetros e contadores numéricos rolantes animados com física de mola (`Rolling Number Ticker`).
   - Barras de progresso com squash-and-stretch elástico ao atingir metas.
   - Micro-estados de validação de formulários com SVG Path Drawing dinâmico.

### O Papel do Motion na Regra 60-30-10

- **60% — Fundação Estática & Neutra (Repouso Absoluto)**:
  O Motion deve permanecer inativo na maior parte estrutural da página. Tipografia estática de corpo de texto, grids de fundo, formulários inativos e layouts utilitários não devem ter movimentos autônomos contínuos. A estabilidade visual é indispensável para evitar fadiga cognitiva.
- **30% — Fluidez Invisível & Micro-Interações de Navegação (O "Feel" Tátil)**:
  É aqui que o Motion cumpre seu papel mais sofisticado:
  - Micro-escalonamento no clique de botões (`whileTap={{ scale: 0.98 }}`).
  - Pílulas indicadoras de abas ativas que deslizam sem recriação do componente.
  - Abertura e fechamento de modais com atenuação suave via `AnimatePresence`.
  - Esta camada não chama a atenção para si mesma; seu papel é fazer com que a aplicação pareça instantânea, tangível e polida.
- **10% — Showstoppers & Momentos de Destaque Visual**:
  Reservado para momentos culminantes: transição de página cinematográfica estilo cortina (`Curtains Blinds / Iris`), efeito de vôo e impacto elástico ao finalizar compra, cartões com inclinação 3D (`3D Tilt`) reagindo à luz do cursor, ou dioramas tridimensionais interativos combinando Motion e Three.js.

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Quando Evitar (Anti-padrões e Sobrecarga)
- **Animação Forçada de Propriedades de Layout**: Jamais anime diretamente `width`, `height`, `margin`, `padding` ou `top/left` em elementos com múltiplos filhos sem usar a prop `layout`. Disparar recalculo de layout síncrono em cascata degrada a métrica de *Interaction to Next Paint (INP)* e gera engasgos severos.
- **Cascata de Delays Intermináveis (Stagger Overuse)**: Em tabelas com 50 linhas ou grids densos, configurar `staggerChildren: 0.1s` faz com que os últimos elementos demorem 5 segundos para aparecer. O usuário corporativo percebe isso como travamento. Limite cascadas a no máximo 5–8 itens de primeiro plano ou use um delay máximo acumulado de 250ms.
- **Transições de Rota com Bloqueio Rígido**: Evite reter o descarregamento da página anterior por mais de 300ms enquanto uma animação complexa de saída executa. O usuário precisa de resposta imediata a cliques de navegação primária.
- **Motion Sickness em Dispositivos Móveis**: Evite rotações de perspectiva 3D contínuas ou balanços acentuados de câmera baseados em giroscópio ou rolagem acelerada em telas pequenas.

### ⚠️ Regras de Acessibilidade & Higiene de GPU
1. **Suporte Rigoroso a `prefers-reduced-motion`**:
   Todo projeto deve respeitar o hook `useReducedMotion()`. Quando ativo:
   - Substitua deslocamentos de posição (`x`, `y`, `scale`) por transições simples e rápidas de `opacity` (`duration: 0.15s`), ou anule completamente o movimento.
   ```tsx
   const shouldReduceMotion = useReducedMotion();
   const animateProps = shouldReduceMotion 
     ? { opacity: 1 } 
     : { opacity: 1, y: 0, scale: 1 };
   ```
2. **Prevenção da Explosão de Camadas de GPU (Layer Explosion)**:
   Embora o Motion gerencie propriedades de aceleração de hardware de forma eficiente, aplicar propriedades animadas em centenas de nós simultâneos força o navegador a alocar texturas de composição de GPU para cada elemento, esgotando a memória VRAM de dispositivos móveis. Use virtualização de listas (`TanStack Virtual`) ao combinar listas longas com animações de presença.
3. **Desativação Condicional em Dispositivos de Baixa Potência**:
   Efeitos de rastreamento contínuo de cursor (como luz especular ou tilt 3D) devem ser desativados em telas touch usando a media query `@media (hover: none) and (pointer: coarse)`.

---

## 4. Catálogo Detalhado de Componentes, Primitivas & Padrões

Abaixo estão catalogados **10 padrões e receitas de alto nível** extraídos da suíte oficial do Motion Examples:

```
┌────────────────────────────────────────────────────────────────────────────────┐
│                          CATÁLOGO DE PADRÕES MOTION                            │
├────────────────────────────┬───────────────────────┬───────────────────────────┤
│ Padrão / Efeito            │ Gatilho               │ Mecanismo Técnico         │
├────────────────────────────┼───────────────────────┼───────────────────────────┤
│ 1. Layout Projection Tabs  │ Estado reativo        │ FLIP + layoutId           │
│ 2. Scroll Word Reveal      │ Scroll Progress       │ useScroll + useTransform  │
│ 3. Rolling Text Button     │ Pointer Hover         │ Staggered Glyph Translate │
│ 4. Multidimensional Grid   │ Pointer Drag / Pan    │ Reorder.Group + Springs   │
│ 5. Ballistic Add-to-Basket │ Tap / Click           │ Arc Trajectory + Elastic  │
│ 6. 3D Tilt Card            │ Pointer Coordinates   │ useMotionValue + Springs  │
│ 7. SVG Path Drawing        │ In-View / Mount       │ pathLength Interpolation  │
│ 8. Curtains Page Blinds    │ Rota / AnimatePres.   │ CSS Clip / Mask Wipe Pres.│
│ 9. Lenis + Frame Loop      │ Wheel / Touch Scroll  │ frame.update Sync         │
│ 10. Pointer Collision Grid │ Swept Pointer Sweep   │ Vector Raycast Sweep      │
└────────────────────────────┴───────────────────────┴───────────────────────────┘
```

### 1. Layout Projection: Shared Element Morphing (`layoutId` Active Indicator)
- **Comportamento Visual**: Uma barra de abas onde o indicador de seleção ("pílula" de fundo) desliza suavemente entre botões de larguras variadas. A forma se adapta dinamicamente às dimensões do novo botão ativo sem salto ou piscar.
- **Gatilho**: Atualização da chave de estado `activeTab`.
- **Anatomia & Props**:
  - Elemento pai com layout dinâmico.
  - Componente `<motion.div layoutId="active-pill" />` renderizado condicionalmente dentro da aba ativa.
  - Transição baseada em mola com amortecimento crítico (`type: "spring", stiffness: 380, damping: 30`).

### 2. Scroll-Driven Storytelling: Word-by-Word Reveal (`useScroll` + `useTransform`)
- **Comportamento Visual**: Conforme o usuário rola o viewport pela seção de destaque, o texto de manchete clareia gradualmente palavra por palavra (de `opacity: 0.15` para `opacity: 1`), guiando o ritmo de leitura com precisão cinematográfica.
- **Gatilho**: Posição contínua de rolagem mapeada via `scrollYProgress`.
- **Anatomia & Props**:
  - Container rastreado com `useScroll({ target: containerRef, offset: ["start 0.9", "end 0.25"] })`.
  - Frase dividida em array de palavras (`split(" ")`).
  - Cada palavra recebe uma fatia proporcional do range `[i / total, (i + 1) / total]`, convertida em opacidade via `useTransform`.

### 3. Kinetic Typography: Rolling Text Button (Slot Machine Hover)
- **Comportamento Visual**: Ao passar o cursor sobre um botão de ação, a palavra atual sobe pelo eixo Y até sumir no topo, enquanto uma cópia idêntica entra pela base assumindo o seu lugar. Pode ser executado em bloco ou caractere por caractere com atraso escalonado (micro-stagger).
- **Gatilho**: `onHoverStart` e `onHoverEnd` (ou seletores nativos de grupo CSS/Motion).
- **Anatomia & Props**:
  - Container com `overflow: hidden`.
  - Dois blocos de texto paralelos com `y: 0%` e `y: 100%`, transicionando para `y: -100%` e `y: 0%` com `transition: { ease: [0.16, 1, 0.3, 1], duration: 0.45 }`.

### 4. Multidimensional Drag-to-Reorder Grid (`Reorder.Group` & `Reorder.Item`)
- **Comportamento Visual**: Grade interativa de cartões ou mídias. O usuário clica e arrasta qualquer item; os outros itens do grid abrem espaço e reorganizam suas posições instantaneamente com física fluida. Ao soltar, o item se fixa no novo índice com amortecimento elástico natural.
- **Gatilho**: Pointer drag contínuo.
- **Anatomia & Props**:
  - `<Reorder.Group values={items} onReorder={setItems} axis="y" className="...">`
  - `<Reorder.Item value={item} key={item.id} layout />`
  - Algoritmo interno projeta novos retângulos de colisão e redistribui a matriz visual sem interromper o drag ativo.

### 5. Ballistic Trajectory: "Add to Basket" com Curvatura Arc e Squash/Stretch
- **Comportamento Visual**: Ao clicar em "Comprar", uma miniatura do item se solta do card de produto, viaja pelo ar descrevendo uma parábola gravitacional suave até o ícone do carrinho na barra superior e desaparece em um flash. Ao receber o projétil, o ícone do carrinho sofre um impacto elástico (`squash & stretch`: escala horizontal 1.35x, escala vertical 0.75x, retornando ao repouso).
- **Gatilho**: Evento de `onClick` / `onTap`.
- **Anatomia & Props**:
  - Interpolação vetorial de coordenadas de tela `(x0, y0)` até `(x1, y1)`.
  - Decomposição de eixos: movimento horizontal com curva linear/ease-out e movimento vertical com curva senoidal/arc (`y: [0, -120, targetY]`).
  - Disparo de mola de impacto acoplada no ícone receptor via chave reativa de renderização.

### 6. Tactile 3D Tilt Card com Reflexo Especular
- **Comportamento Visual**: Cartão interativo com perspectiva tridimensional profunda (`perspective: 1000px`). Ao mover o mouse sobre sua superfície, o card inclina-se nos eixos X e Y acompanhando o cursor com física de amortecimento suave. Uma camada de gradiente radial simula a incidência de luz externa sobre o material.
- **Gatilho**: Evento `onPointerMove` dentro dos limites do componente.
- **Anatomia & Props**:
  - `useMotionValue(0)` rastreando a distância normalizada do centro `[-0.5, 0.5]`.
  - `useSpring` para converter coordenadas bruscas do mouse em valores físicos amortecidos (`stiffness: 220, damping: 22`).
  - `useTransform` convertendo coordenadas normalizadas em graus de inclinação (`rotateX: [-12deg, 12deg]`, `rotateY: [12deg, -12deg]`).

### 7. SVG Path Morphing & Stroke Drawing (`pathLength`, `pathOffset`)
- **Comportamento Visual**: Ícones de confirmação, contornos gráficos e diagramas vetoriais são "desenhados" ao vivo na tela, simulando o traço contínuo de nanquim.
- **Gatilho**: Visibilidade em tela (`whileInView`) ou conclusão de processamento assíncrono.
- **Anatomia & Props**:
  - `<motion.path d="..." initial={{ pathLength: 0, opacity: 0 }} animate={{ pathLength: 1, opacity: 1 }} transition={{ duration: 1.2, ease: "easeInOut" }} />`.
  - Manipulação de `strokeDasharray` e `strokeDashoffset` nativamente sem forçar cálculo manual de comprimento de curva pelo desenvolvedor.

### 8. Curtains Page Transitions: Presets de Cortina (Blinds, Iris, Wipe)
- **Comportamento Visual**: Transição de rota imersiva sem flash em branco. Durante a troca de página, uma cortina de ripas verticais (blinds) ou uma máscara circular originada exatamente no ponto de clique do usuário (iris wipe) se expande, oculta a tela anterior e revela a nova página já renderizada.
- **Gatilho**: Mudança de rota de aplicação (`pathname`) gerenciada via `<AnimatePresence mode="wait">`.
- **Anatomia & Props**:
  - Máscara CSS `clip-path: circle(0% at x y)` animando para `clip-path: circle(150% at x y)`.
  - Sincronização estrita de saída e entrada via `mode="wait"`.

### 9. Smooth Scroll Orchestration: Lenis + Motion Frame Loop
- **Comportamento Visual**: Rolagem suave com inércia física perfeitamente sincronizada com transformações de escala e posição de elementos da página, eliminando qualquer micro-engasgo (jitter) ou descompasso visual entre o motor de scroll e o motor de animações.
- **Gatilho**: Roda do mouse ou toque contínuo.
- **Anatomia & Props**:
  - Inicialização do Lenis Scroll.
  - Sincronização com o Motion via `frame.update((time) => lenis.raf(time))`.
  - Eliminação de ouvintes globais redundantes de `window.addEventListener('scroll')`.

### 10. Swept Pointer Collision Detection Grid
- **Comportamento Visual**: Uma malha densa de células luminosas (ex: grade de 20x20) que reage ao movimento do cursor. Mesmo em movimentos ultrarrápidos do mouse (onde o navegador saltaria coordenadas e deixaria células sem evento `mouseenter`), o algoritmo calcula o vetor contínuo de varredura (swept raycast) e ilumina todas as células interceptadas no caminho, decaindo o brilho gradualmente.
- **Gatilho**: Deslocamento vetorial de alta velocidade do ponteiro.
- **Anatomia & Props**:
  - Cálculo de linha de Bresenham ou interseção de raio entre a coordenada anterior `(px, py)` e a atual `(cx, cy)`.
  - Disparo de pulso luminoso animado por célula com transição `opacity: [1, 0]` e mola de decaimento.

---

## 5. Matemática do Movimento & Receitas de Código

### Parâmetros Físicos e Curvas Recomendadas

#### 1. Presets de Molas (Spring Configurations)
Ao configurar o Motion, priorize física baseada em molas para interfaces táteis:

| Preset | Uso Recomendado | Stiffness | Damping | Mass | Rest Delta |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Snappy / Crisp** | Botões, micro-taps, tooltips, checkboxes | `400` | `30` | `0.8` | `0.001` |
| **Smooth / Gentle** | Modais, gavetas laterais (drawers), abas | `260` | `26` | `1.0` | `0.001` |
| **Bouncy / Playful** | Badges de notificação, ícones de sucesso | `320` | `18` | `1.2` | `0.005` |
| **Inertial Glide** | Soltura de drag, carrosséis infinitos | `power: 0.8`, `timeConstant: 350`, `restDelta: 0.5` |

#### 2. Curvas de Interpolação Temporal (Cubic-Bezier)
Para transições de página ou elementos com duração fixa de tempo:
- **Ease-Out-Expo (O padrão Linear / Apple)**: `cubic-bezier(0.16, 1, 0.3, 1)` — partida instantânea e aterrissagem ultra-suave.
- **Ease-Out-Back (Micro-overshoot tátil)**: `cubic-bezier(0.34, 1.56, 0.64, 1)` — leve ultrapassagem antes do repouso.
- **Ease-In-Out-Quart (Cortinas de transição)**: `cubic-bezier(0.76, 0, 0.24, 1)` — aceleração e desaceleração simétrica e pesada.

---

### Receitas de Código Funcionais

#### Receita 1: Shared Layout Tab Navigation (Pill Indicator)
Implementação de abas de navegação onde a pílula de seleção desliza dinamicamente entre elementos com larguras variáveis usando `layoutId` e Tailwind CSS v4.

```tsx
// components/motion/layout-tabs.tsx
"use client";

import * as React from "react";
import { motion } from "motion/react";

interface Tab {
  id: string;
  label: string;
}

const TABS: Tab[] = [
  { id: "overview", label: "Visão Geral" },
  { id: "analytics", label: "Métricas & Análise" },
  { id: "deployments", label: "Deploys" },
  { id: "settings", label: "Configurações" },
];

export function LayoutTabs() {
  const [activeTab, setActiveTab] = React.useState<string>(TABS[0].id);

  return (
    <nav className="inline-flex items-center gap-1 p-1.5 rounded-full bg-zinc-900/90 border border-zinc-800 shadow-inner">
      {TABS.map((tab) => {
        const isActive = activeTab === tab.id;
        return (
          <button
            key={tab.id}
            type="button"
            onClick={() => setActiveTab(tab.id)}
            className="relative px-4 py-1.5 text-sm font-medium transition-colors duration-200 outline-none focus-visible:ring-2 focus-visible:ring-emerald-400 focus-visible:ring-offset-2 focus-visible:ring-offset-zinc-900 rounded-full cursor-pointer select-none"
            style={{
              WebkitTapHighlightColor: "transparent",
            }}
          >
            {/* Pílula Deslizante com Layout Projection */}
            {isActive && (
              <motion.div
                layoutId="active-tab-indicator"
                className="absolute inset-0 rounded-full bg-zinc-800 shadow-sm border border-zinc-700/60"
                transition={{
                  type: "spring",
                  stiffness: 380,
                  damping: 30,
                  mass: 0.9,
                }}
              />
            )}
            <span
              className={`relative z-10 transition-colors duration-200 ${
                isActive ? "text-zinc-100 font-semibold" : "text-zinc-400 hover:text-zinc-200"
              }`}
            >
              {tab.label}
            </span>
          </button>
        );
      })}
    </nav>
  );
}
```

---

#### Receita 2: Interactive 3D Tilt Card com Brilho Especular e Física de Mola
Card interativo com perspectiva de 1000px, rotação biaxial proporcional à posição do ponteiro e camada dinâmica de iluminação.

```tsx
// components/motion/tilt-card.tsx
"use client";

import * as React from "react";
import { motion, useMotionValue, useSpring, useTransform } from "motion/react";

interface TiltCardProps {
  title: string;
  category: string;
  description: string;
}

export function TiltCard({ title, category, description }: TiltCardProps) {
  const cardRef = React.useRef<HTMLDivElement>(null);

  // Posição normalizada do mouse de -0.5 a 0.5
  const mouseX = useMotionValue(0);
  const mouseY = useMotionValue(0);

  // Coordenadas em pixels para o foco de luz radial
  const glareX = useMotionValue(0);
  const glareY = useMotionValue(0);

  // Amortecimento suave das coordenadas via mola
  const springConfig = { stiffness: 220, damping: 22, mass: 0.6 };
  const smoothMouseX = useSpring(mouseX, springConfig);
  const smoothMouseY = useSpring(mouseY, springConfig);

  // Mapeamento das rotações em graus
  const rotateX = useTransform(smoothMouseY, [-0.5, 0.5], [12, -12]);
  const rotateY = useTransform(smoothMouseX, [-0.5, 0.5], [-12, 12]);

  const handlePointerMove = (e: React.PointerEvent<HTMLDivElement>) => {
    if (!cardRef.current) return;
    const rect = cardRef.current.getBoundingClientRect();
    const x = e.clientX - rect.left;
    const y = e.clientY - rect.top;

    // Normaliza de -0.5 a +0.5
    mouseX.set(x / rect.width - 0.5);
    mouseY.set(y / rect.height - 0.5);

    // Salva posições absolutas para o brilho especular
    glareX.set(x);
    glareY.set(y);
  };

  const handlePointerLeave = () => {
    mouseX.set(0);
    mouseY.set(0);
  };

  return (
    <div className="relative [perspective:1000px] inline-block">
      <motion.div
        ref={cardRef}
        onPointerMove={handlePointerMove}
        onPointerLeave={handlePointerLeave}
        style={{
          rotateX,
          rotateY,
          transformStyle: "preserve-3d",
        }}
        whileTap={{ scale: 0.98 }}
        className="relative w-80 h-96 rounded-2xl p-6 bg-zinc-900 border border-zinc-800 shadow-2xl cursor-pointer overflow-hidden select-none transition-shadow duration-300 hover:shadow-cyan-500/10"
      >
        {/* Camada Dinâmica de Brilho Especular */}
        <motion.div
          className="pointer-events-none absolute -inset-px rounded-2xl opacity-0 transition-opacity duration-300 hover:opacity-100"
          style={{
            background: useTransform(
              [glareX, glareY],
              ([x, y]) =>
                `radial-gradient(400px circle at ${x}px ${y}px, rgba(255,255,255,0.08), transparent 80%)`
            ),
          }}
        />

        <div className="relative z-10 flex flex-col justify-between h-full [transform:translateZ(30px)]">
          <div>
            <span className="text-xs font-semibold tracking-wider uppercase text-cyan-400">
              {category}
            </span>
            <h3 className="mt-2 text-xl font-bold text-zinc-100">{title}</h3>
            <p className="mt-2 text-sm text-zinc-400 leading-relaxed">{description}</p>
          </div>

          <div className="pt-4 border-t border-zinc-800/80 flex items-center justify-between">
            <span className="text-xs text-zinc-500 font-mono">MOTION 3D CORE</span>
            <button
              type="button"
              className="px-3 py-1 text-xs font-semibold rounded-lg bg-zinc-100 text-zinc-900 hover:bg-white transition-colors"
            >
              Explorar
            </button>
          </div>
        </div>
      </motion.div>
    </div>
  );
}
```

---

#### Receita 3: Kinetic Rolling Number Counter / Odometer
Contador numérico animado que transiciona valores com movimento vertical inercial de dígitos individuais (estilo odômetro de dashboard financeiro).

```tsx
// components/motion/rolling-number.tsx
"use client";

import * as React from "react";
import { motion, useSpring, useTransform } from "motion/react";

interface RollingDigitProps {
  digit: number;
}

function RollingDigit({ digit }: RollingDigitProps) {
  const animatedValue = useSpring(digit, {
    stiffness: 280,
    damping: 28,
    mass: 0.8,
  });

  React.useEffect(() => {
    animatedValue.set(digit);
  }, [digit, animatedValue]);

  const y = useTransform(animatedValue, (latest) => `${-latest * 10}%`);

  return (
    <div className="relative inline-block h-8 w-[0.62em] overflow-hidden align-top text-2xl font-bold font-mono">
      <motion.div style={{ y }} className="absolute inset-x-0 top-0 flex flex-col items-center">
        {[0, 1, 2, 3, 4, 5, 6, 7, 8, 9].map((num) => (
          <span key={num} className="h-8 flex items-center justify-center text-zinc-100">
            {num}
          </span>
        ))}
      </motion.div>
    </div>
  );
}

export function RollingCounter({ value }: { value: number }) {
  const digits = Math.abs(value).toString().padStart(4, "0").split("").map(Number);

  return (
    <div className="inline-flex items-center px-4 py-2 rounded-xl bg-zinc-950 border border-zinc-800 shadow-inner">
      <span className="text-2xl font-bold font-mono text-emerald-400 mr-1">$</span>
      {digits.map((d, index) => (
        <RollingDigit key={index} digit={d} />
      ))}
    </div>
  );
}
```

---

#### Receita 4: Scroll Word Reveal com Suporte a `useReducedMotion`
Componente que revela parágrafos editoriais palavra por palavra conforme o usuário rola a página, revertendo para renderização estática limpa caso o sistema operacional solicite redução de movimento.

```tsx
// components/motion/scroll-word-reveal.tsx
"use client";

import * as React from "react";
import { motion, useScroll, useTransform, useReducedMotion } from "motion/react";

interface ScrollWordRevealProps {
  text: string;
  className?: string;
}

export function ScrollWordReveal({ text, className = "" }: ScrollWordRevealProps) {
  const containerRef = React.useRef<HTMLParagraphElement>(null);
  const shouldReduceMotion = useReducedMotion();

  const { scrollYProgress } = useScroll({
    target: containerRef,
    offset: ["start 0.85", "end 0.35"],
  });

  const words = text.split(" ");

  if (shouldReduceMotion) {
    return (
      <p ref={containerRef} className={`text-2xl md:text-3xl font-medium text-zinc-100 ${className}`}>
        {text}
      </p>
    );
  }

  return (
    <p
      ref={containerRef}
      className={`flex flex-wrap gap-x-2 gap-y-1 text-2xl md:text-3xl font-medium leading-relaxed ${className}`}
    >
      {words.map((word, index) => {
        const start = index / words.length;
        const end = start + 1 / words.length;
        return (
          <Word key={index} progress={scrollYProgress} range={[start, end]}>
            {word}
          </Word>
        );
      })}
    </p>
  );
}

function Word({
  children,
  progress,
  range,
}: {
  children: string;
  progress: any;
  range: [number, number];
}) {
  const opacity = useTransform(progress, range, [0.15, 1]);
  const y = useTransform(progress, range, [4, 0]);

  return (
    <span className="relative inline-block">
      <motion.span style={{ opacity, y }} className="inline-block text-zinc-100">
        {children}
      </motion.span>
    </span>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir o plano arquitetural do projeto (`DESIGN_BLUEPRINT.md`), siga as diretrizes abaixo para especificar implementações de movimento:

### 1. Declaração Obrigatória de Presets de Mola
Declare formalmente os tokens de física na seção de arquitetura técnica do blueprint para manter coerência tátil em todo o produto:
```yaml
motion_physics_tokens:
  spring_crisp: { stiffness: 400, damping: 30, mass: 0.8 } # Micro-ações e botões
  spring_gentle: { stiffness: 260, damping: 26, mass: 1.0 } # Gavetas, modais, abas
  spring_bouncy: { stiffness: 320, damping: 18, mass: 1.2 } # Notificações e confirmações
  bezier_cinematic: [0.16, 1, 0.3, 1]                      # Efeito Ease-Out-Expo
```

### 2. Isolação de Renderização & Performance
- **Componentes Folha**: Todo componente animado via Motion deve ser isolado como um componente cliente folha (`"use client"`), evitando que a reatividade de física force re-execução de nós estáticos pais no Next.js App Router / React Server Components (RSC).
- **Projeção de Layout sem CLS**: Ao utilizar `layout` ou `layoutId`, sempre garanta que os containers possuam dimensões mínimas ou aspectos reservados (`min-height`, `aspect-ratio`) para prevenir saltos acumulados de layout (*Cumulative Layout Shift - CLS*) durante a montagem inicial.

### 3. Matriz de Compatibilidade e Acessibilidade
- Toda especificação de animação de scroll (`useScroll`) deve incluir a cláusula explícita de desativação ou simplificação para o hook `useReducedMotion()`.
- Especificar `@media (pointer: coarse)` para desabilitar efeitos dependentes de hover contínuo (como `3D Tilt Card` ou `Pointer Collision Grid`) em smartphones e tablets, substituindo por interações diretas de toque.
