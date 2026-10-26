---
id: "react-spring"
name: "React Spring"
url: "https://www.react-spring.dev/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["Hooke's Law Physics", "Natural Damped Oscillations", "Direct DOM Mutation", "Multi-Target Agnostic (Web/Three/Native)", "Fluid Gesture Momentum", "Zero-Reconciliation Frame Loop"]
densidade_informacao: "Independente"
impacto_visual: "Moderado a Cinematografico/Showstopper"
custo_computacional: "Baixo (CSS/Transforms fora de render) a Medio (JS Springs/RAF / Three.js)"
stack_frameworks: ["React (v18, v19)", "Three.js / React Three Fiber (@react-spring/three)", "@use-gesture/react", "React Native (@react-spring/native)", "Konva (@react-spring/konva)", "TypeScript", "Tailwind CSS"]
compatibilidade:
  combinacoes_recomendadas: ["@use-gesture/react + @react-spring/web (gestos táteis balísticos com inércia contínua)", "React Three Fiber (R3F) + @react-spring/three (3D reativo de alta performance)", "Radix UI / Headless UI + @react-spring/web (drawers, sheets e modais físicos)", "Lucide Icons + react-spring (microinterações orgânicas de glifos SVG)", "Lenis Smooth Scroll + useScroll (orquestração de parallax cinético)"]
  conflitos_esteticos: ["Curvas de tempo fixas puramente lineares sem desaceleração física (sensação robótica)", "Manipulação de valores de animação via setState do React (re-renders a cada frame colapsam o framerate)", "Oscilações descontroladas (underdamped/wobbly) em tabelas densas, formulários corporativos ou fluxos de checkout", "Ausência de clamp em elementos com limites visuais estritos que vazam seus containers"]
---

# React Spring — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)

O **React Spring** (`https://www.react-spring.dev/`), originado pelo engenheiro Paul Henschel (`@0xca0a`) e mantido como um dos pilares do coletivo de tecnologia criativa **Poimandres (`pmndrs`)**, representa a transição paradigmática na web entre a *animação baseada em tempo* e a *simulação física computacional em tempo real*.

Enquanto bibliotecas de animação convencionais concebem transições como curvas de interpolação fixadas a um relógio (onde um elemento viaja de $A$ a $B$ em rigorosos $300\text{ms}$ através de uma curva pré-estabelecida como `ease-in-out`), o React Spring modela os componentes da interface como corpos materiais reais dotados de massa, atrito e tensão elástica, governados pela equação diferencial do oscilador harmônico amortecido (a Lei de Hooke generalizada):

$$F = -k \cdot x - c \cdot v$$

Onde:
- $k$ é o coeficiente elástico (**Tension / Rigidez**).
- $x$ é a distância do deslocamento em relação ao ponto de repouso (o equilíbrio).
- $c$ é o coeficiente de amortecimento viscoso (**Friction / Atrito**).
- $v$ é o vetor de velocidade instantânea do corpo.

```
                  ┌────────────────────────────────────────────────────────┐
                  │          DINÂMICA DE MOLA (HOOKE'S LAW)                │
                  └────────────────────────────────────────────────────────┘
                    Equilíbrio (Destino)
                              │
  [Repouso / Origem]          ▼
         ○════════════════════●═══════○───────────► Eixo X
         │◄──── Tração ─────►│◄── Inércia (Overshoot)
              F = -k·x          F_atrito = -c·v
```

### O Princípio da Interrupção Orgânica (Velocity-Preserving Interruptibility)
O maior triunfo sensorial do React Spring sobre curvas de Bézier clássicas reside na capacidade de lidar com eventos caóticos de interação humana:
1. Em uma animação de tempo fixo de $400\text{ms}$, se o usuário interrompe o movimento na metade (por exemplo, soltando o cursor de um arrasto ou clicando para fechar um modal que recém começou a abrir), a interface é forçada a truncar a curva abruptamente, resetar o cronômetro ou calcular remendos matemáticos artificiais.
2. No React Spring, o vetor de velocidade atual ($v_{\text{current}}$) nunca é descartado. Ao alterar o destino de uma mola no meio de seu trajeto, o novo cálculo de força herda a velocidade instantânea do frame anterior. O elemento não estala, não dá saltos angulares e não desacelera artificialmente: ele converte seu momento cinético de forma contínua em direção ao novo ponto de repouso, exatamente como uma corda elástica puxada para uma nova coordenada no mundo real.

### Arquitetura de Mutação Fora do Render (Zero-Reconciliation Direct Mutation)
Diferente da intuição comum em ecossistemas React — onde alterações visuais costumam passar pelo ciclo de conciliação do Virtual DOM (`re-render` $\to$ `diffing` $\to$ `commit`) —, o React Spring opera em uma camada desacoplada de ultra-alta performance:
- **`SpringValue` & `Controller`**: As instâncias matemáticas de mola residem em memória fora da árvore de componentes do React.
- **`animated(Component)` / `animated.div`**: O wrapper `animated` cria nós de subscrição direta. Quando a física da mola computa um novo valor dentro do loop unificado de `requestAnimationFrame` da biblioteca, o `SpringValue` injeta a mutação diretamente nos nós de estilo do DOM (`element.style.transform = ...`) ou nas matrizes do Three.js (`mesh.position.set(...)`), sem disparar uma única re-renderização de componente React.
- **FluidValue Pipeline**: Interpolações numéricas, strings com unidades complexas (`"translateX(100px) rotate(45deg)"`) e caminhos SVG são resolvidos no nível de nós de fluxo contínuo (*fluid streams*), garantindo estabilidade absoluta a 60fps/120fps mesmo em árvores de UI extremamente ramificadas.

### Modularidade Multi-Target Agnóstica
O núcleo matemático do React Spring (`@react-spring/core`) é completamente desacoplado do navegador. A Poimandres estruturou adaptadores dedicados para cada mídia de renderização:
- **`@react-spring/web`**: Otimizado para elementos HTML e nós SVG, mapeando propriedades diretamente para transformações aceleradas por GPU via CSSOM.
- **`@react-spring/three`**: Estende primitivas do React Three Fiber (`animated.mesh`, `animated.group`, `animated.directionalLight`), aplicando cálculos de mola diretamente a classes `Vector3`, `Euler`, `Quaternion` e materiais do Three.js.
- **`@react-spring/native`**: Conecta-se à API `Animated` nativa do iOS e Android, aproveitando o driver nativo off-thread.
- **`@react-spring/konva`** & **`@react-spring/zdog`**: Aplica física contínua a cenas 2D em Canvas e pseudo-3D vetorial.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto e Casos de Uso Recomendados

1. **Gestos Táteis Contínuos & Bottom Sheets / Gavetas com Elasticidade Balística**:
   - Interfaces mobile-first onde o elemento segue o dedo do usuário em tempo real (`@use-gesture/react`) e, ao ser solto, herda o vetor de velocidade do arrasto para decidir se completa o fechamento ou se retorna ao topo com amortecimento elástico (efeito "rubberbanding" do iOS).
2. **Cenas Tridimensionais Interativas (Web 3D / R3F)**:
   - Objetos tridimensionais em Three.js que reagem à orientação do mouse, rolagem ou clique com deformações elásticas orgânicas, foco de câmera em alvos móveis e rotação com inércia amortecida.
3. **Dashboards Financeiros com Contadores Numéricos Reais (Rolling Odometers)**:
   - Saldos bancários, cotações de ações e métricas em tempo real que fluem continuamente de um valor para o outro com aceleração física, transmitindo dinamicidade de mercado.
4. **Menus Deslizantes, Accordions Físicos & Stagger Cascades**:
   - Revelação de gavetas laterais, menus expansivos e listas encadeadas (`useTrail`) onde os elementos seguintes reagem ao movimento do líder como os vagões de um trem articulado.
5. **Transições de Presença Condicional com Retenção de Estado (Lifecycles)**:
   - Notificações de toasts, abas com montagem/desmontagem assíncrona e remoção de cartões em listas onde o elemento em saída precisa concluir sua trajetória balística antes de ser removido da árvore do DOM (`useTransition`).

### O Papel do React Spring na Regra 60-30-10

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                   DISTRIBUIÇÃO DE MOTION: REGRA 60-30-10                    │
├────────────────────────────────┬────────────────────────────────────────────┤
│ Camada                         │ Função e Aplicação com React Spring        │
├────────────────────────────────┼────────────────────────────────────────────┤
│ 60% — Estabilidade & Repouso   │ Interface estática. Tipografia, grids base,│
│                                │ inputs em repouso e blocos textuais        │
│                                │ imutáveis sem forças autônomas.            │
├────────────────────────────────┼────────────────────────────────────────────┤
│ 30% — Fluidez Tátil Invisível  │ Microinterações físicas: compressão em     │
│                                │ botões (squash), arraste com snap, modais  │
│                                │ que herdam inércia de fechamento e menus   │
│                                │ articulados via useTrail suave.            │
├────────────────────────────────┼────────────────────────────────────────────┤
│ 10% — Showstoppers & 3D Físico │ Cenas 3D completas com R3F e               │
│                                │ @react-spring/three, transições de tela    │
│                                │ balísticas em página inteira, simulações   │
│                                │ de pêndulo elástico e decks de cartas 3D.  │
└────────────────────────────────┴────────────────────────────────────────────┘
```

- **60% — Fundação Estática & Imutável**:
  A estabilidade cognitiva é essencial. Mais da metade da tela deve permanecer completamente estática e sem forças oscilatórias. Textos de leitura longa, contornos de cartões secundários e controles inativos nunca devem flutuar autonomamente sem comando do usuário.
- **30% — Micro-Física Reativa (O "Feel" Natural)**:
  Nesta camada, o React Spring opera em sua configuração `gentle` ou `stiff` com alto amortecimento ($c \ge 24$). Quando o usuário clica em um botão, este sofre uma micro-compressão proporcional (`scale: 0.96`); quando puxa um dropdown, a lista se acomoda sem solavancos. O usuário não identifica a mola conscientemente, mas sente que o software possui densidade e massa reais.
- **10% — O Showstopper Orgânico**:
  Destinado a momentos estéticos culminantes: uma malha 3D reativa que flutua e distorce conforme o scroll da página, uma galeria de produtos em cartas com rotação volumétrica completa gerida por `useSprings`, ou uma celebração de conquista com badges saltando em oscilação `wobbly`.

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Quando Evitar (Anti-padrões e Sobrecarga)

- **Animações de Render-Cycle (SetState Anti-pattern)**: Jamais use o callback `onChange` do React Spring para invocar um `setState` do React a fim de passar estilos para elementos comuns (`<div style={{ transform: state }} />`). Isso anula a maior vantagem arquitetural da biblioteca, forçando 60 a 120 re-renderizações por segundo na árvore do React, gerando quedas de frames e destruindo o *Interaction to Next Paint (INP)*. Use sempre os nós `animated.*`.
- **Oscilações Excessivas (Underdamped Molas) em UIs Críticas**: O preset `config.wobbly` ou combinações de baixo atrito (`friction: < 10`) criam oscilações repetitivas que se assemelham a gelatina. Isso é terminantemente contraindicado para interfaces corporativas, tabelas analíticas B2B, caixas de checkout e mensagens de erro de formulário. O usuário interpreta o tremor repetitivo como lentidão ou perda de precisão.
- **Omissão de Clamping em Alinhamentos Geométricos Estritos**: Quando um elemento não pode visualmente ultrapassar seu container (por exemplo, uma barra de progresso horizontal ou uma guia deslizante de abas com bordas rígidas), o overshoot característico das molas causará um vazamento temporário das bordas. Nestes casos, o parâmetro `clamp: true` é obrigatório.
- **Criação Desenfreada de Molas em Listas Longas sem Virtualização**: Instanciar 500 molas através de `useSprings` para uma lista não virtualizada consome dezenas de instâncias de `Controller` e nós de animação simultâneos na memória heap. Sempre combine listas de mais de 30 itens dinâmicos com virtualização (`@tanstack/react-virtual`).

### ⚠️ Regras de Acessibilidade & Higiene de Hardware

1. **Respeito Imperativo a `prefers-reduced-motion`**:
   Usuários com distúrbios vestibulares podem sofrer náuseas e desorientação sensorial grave diante de movimentos elásticos oscilatórios. O React Spring permite anular o motor físico globalmente ou por componente através da diretiva `immediate`:
   ```tsx
   import { useSpring, animated } from '@react-spring/web'
   import { useReducedMotion } from './useReducedMotion' // media-query hook

   export function AccessibleModal({ isOpen }: { isOpen: boolean }) {
     const prefersReduced = useReducedMotion()

     const styles = useSpring({
       opacity: isOpen ? 1 : 0,
       y: isOpen ? 0 : (prefersReduced ? 0 : 24),
       // Se o usuário solicitou menos movimento, executa a mola de forma imediata
       immediate: prefersReduced,
       config: { tension: 300, friction: 30 }
     })

     return <animated.div style={styles}>...</animated.div>
   }
   ```
2. **Higiene de GPU e Camadas de Composição**:
   Ao animar nós complexos, limite as propriedades animadas estritamente a transformações compostas na GPU: `transform` (`x`, `y`, `z`, `scale`, `rotate`) e `opacity`. Evite animar propriedades que forçam cálculos de layout (`width`, `height`, `margin`, `padding`, `top`, `left`).
3. **Limpeza e Desmontagem de Controladores**:
   Ao desacoplar componentes que utilizam `SpringRef` ou ouvintes contínuos de gestos com `@use-gesture/react`, garanta o cancelamento de streams pendentes para evitar vazamento de memória em Single Page Applications (SPAs).

---

## 4. Catálogo Detalhado de Componentes, Primitivas & Padrões

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        CATÁLOGO DE PADRÕES DO REACT SPRING                             │
├──────────────────────────────────┬──────────────────────────┬──────────────────────────┤
│ Padrão / Efeito                  │ Hook & Módulo            │ Dinâmica Física          │
├──────────────────────────────────┼──────────────────────────┼──────────────────────────┤
│ 1. Tactile Rubberband Sheet      │ useSpring + useDrag      │ Inércia + Restitution    │
│ 2. Cascading Menu Trail          │ useTrail                 │ Leader-Follower Stagger  │
│ 3. Lifecycle Item Transition     │ useTransition            │ Enter/Leave/Update FLIP  │
│ 4. Multi-Stage Choreography      │ useChain + useSpringRef  │ Timestep Dependency      │
│ 5. Interactive 3D Physics Mesh   │ @react-spring/three      │ Vector3 & Euler Springs  │
│ 6. Parallax & Scroll Gauge       │ useScroll                │ Scroll-Linked Momentum   │
│ 7. 3D Flip Card Double-Face      │ useSpring (to, from)     │ Perspective Interpolate  │
│ 8. Deck Swipe Dismiss            │ useSprings + useDrag     │ Velocity Ejection Vector │
│ 9. Elastic Button Squash-Stretch │ useSpring                │ Mass & Volume Balance    │
│ 10. Kinetic Number Odometer      │ useSpring + to()         │ Continuous Digit Roll    │
└──────────────────────────────────┴──────────────────────────┴──────────────────────────┘
```

---

### 1. Tactile Rubberband Drawer / Bottom Sheet (`useSpring` + `@use-gesture/react`)
- **Comportamento Visual**: Uma folha inferior móvel que acompanha fielmente o dedo do usuário durante o gesto de arrasto. Se puxada para além do limite superior, exibe resistência progressiva elástica ("rubberbanding"). Quando solta com velocidade angular positiva, despenca suavemente para o repouso fechado; se solta com velocidade neutra acima de um limiar, ancora no ponto aberto com desaceleração física.
- **Gatilho**: Evento de arraste contínuo (`useDrag`).
- **Anatomia & Parâmetros Físicos**:
  - `const [{ y }, api] = useSpring(() => ({ y: 0 }))`
  - Manipulação de `api.start({ y: down ? my : targetY, immediate: down, config: config.gentle })`
  - Resistência calculada: $y_{\text{display}} = \log(y_{\text{drag}} \cdot \text{scale})$ quando fora dos limites.

---

### 2. Cascading Stagger Menu Reveal (`useTrail`)
- **Comportamento Visual**: Uma sequência ordenada de itens de menu (links de navegação, opções de lista) que surge em cascata suave. Cada item sucessivo herda a aceleração do item anterior com um intervalo natural determinado pela física da mola líder, gerando a sensação orgânica de um acordeão ou leque de papel.
- **Gatilho**: Abertura do menu ou montagem da seção de navegação.
- **Anatomia & Parâmetros Físicos**:
  - `const trail = useTrail(items.length, { opacity: isOpen ? 1 : 0, x: isOpen ? 0 : -32, config: config.stiff })`
  - Mapeamento: `{trail.map((style, idx) => <animated.li style={style} key={items[idx].id}>...)}`

---

### 3. Dynamic Lifecycle Transitions (`useTransition`)
- **Comportamento Visual**: Adição, remoção e ordenação de itens em listas dinâmicas (como listas de tarefas, notificações flutuantes ou filtros de catálogo). Ao entrar, o novo elemento ganha escala e opacidade; ao ser excluído, os itens vizinhos fecham o espaço vazio enquanto o item deletado se dissipa com rotação e translação natural.
- **Gatilho**: Mutação de um array de dados no estado da aplicação.
- **Anatomia & Parâmetros Físicos**:
  - `const transitions = useTransition(items, { from: { opacity: 0, height: 0, transform: 'scale(0.8)' }, enter: { opacity: 1, height: 60, transform: 'scale(1)' }, leave: { opacity: 0, height: 0, transform: 'scale(0.8)' }, config: config.gentle })`
  - O render prop `transitions((style, item) => <animated.div style={style}>...)` garante que nós unmounted permaneçam visíveis até o término da mola de saída.

---

### 4. Orchestrated Multi-Stage Sequence (`useChain`)
- **Comportamento Visual**: Coreografia em dois ou mais atos interdependentes. Exemplo: um cartão se expande em largura e altura (Ato 1) e, apenas no instante em que sua geometria atinge o estado quase estacionário, uma grade interna de ícones e textos é revelada em cascata (Ato 2).
- **Gatilho**: Disparo explícito de ativação (`isExpanded`).
- **Anatomia & Parâmetros Físicos**:
  - Uso de referências dedicadas: `const boxRef = useSpringRef()` e `const contentRef = useSpringRef()`.
  - Orquestração: `useChain(isExpanded ? [boxRef, contentRef] : [contentRef, boxRef], [0, 0.25])`.
  - O array de timesteps relativos define que a segunda mola inicia quando 25% do tempo dinâmico da primeira tiver transcorrido.

---

### 5. Interactive 3D Physics Mesh (`@react-spring/three`)
- **Comportamento Visual**: Um objeto tridimensional (geometria de poliedro, torus ou diorama com materiais físicos) renderizado dentro de um `<Canvas>` do React Three Fiber. Ao mover o cursor pela tela ou clicar sobre o objeto, ele reage com rotação elástica contínua, oscilações no canal de emissão de luz e expansão de escala com inércia espacial completa.
- **Gatilho**: Eventos de pointer raycasting no Three.js (`onPointerOver`, `onPointerOut`, `onPointerMove`).
- **Anatomia & Parâmetros Físicos**:
  - `import { animated } from '@react-spring/three'`
  - `const { scale, rotation, color } = useSpring({ scale: active ? 1.4 : 1, rotation: active ? [0, Math.PI, 0] : [0, 0, 0], config: { mass: 2, tension: 300, friction: 25 } })`
  - Componente: `<animated.mesh scale={scale} rotation={rotation}><boxGeometry /><animated.meshStandardMaterial color={color} /></animated.mesh>`.

---

### 6. Parallax & Scroll-Progress Gauge (`useScroll`)
- **Comportamento Visual**: Uma barra de progresso no topo da viewport que se estica conforme o usuário navega verticalmente pelo conteúdo, acoplada a elementos de imagem de fundo que flutuam em velocidades diferenciais (parallax multilayer). A mola suaviza solavancos abruptos na roda do mouse, tornando a navegação contínua e aveludada.
- **Gatilho**: Rolagem de página nativa ou em container rastreado.
- **Anatomia & Parâmetros Físicos**:
  - `const { scrollYProgress } = useScroll()`
  - Interpolação fluida: `const scaleX = scrollYProgress.to([0, 1], [0, 1])`
  - Elemento indicador: `<animated.div style={{ transform: scaleX.to(s => \`scaleX(\${s})\`), transformOrigin: '0% 50%' }} />`.

---

### 7. 3D Flip Card Double-Face com Interpolação Angular
- **Comportamento Visual**: Cartão interativo com duas faces distintas (frente com dados do produto e verso com detalhes técnicos). Ao clicar em "Girar", o cartão realiza uma rotação de 180° no eixo Y com perspectiva isométrica dramática. As faces trocam de visibilidade no exato instante dos 90° de rotação sem artefatos de renderização ou bordas serrilhadas.
- **Gatilho**: Clique do usuário ou foco de acessibilidade.
- **Anatomia & Parâmetros Físicos**:
  - `const { transform, opacity } = useSpring({ transform: \`rotateY(\${flipped ? 180 : 0}deg)\`, opacity: flipped ? 1 : 0, config: { mass: 5, tension: 500, friction: 80 } })`
  - Interpolação: `transform.to(t => \`perspective(800px) \${t}\`)`.
  - Face frontal com `backface-visibility: hidden` e face traseira espelhada a 180°.

---

### 8. Deck Swipe Dismiss com Vetor de Ejeção Inercial (`useSprings`)
- **Comportamento Visual**: Uma pilha de cartões sobrepostos (estilo cartões de aprovação/rejeição). O usuário arrasta o cartão superior lateralmente; o elemento inclina-se proporcionalmente ao deslocamento horizontal. Ao soltar com velocidade suficiente, o cartão é ejetado fora da tela na direção do vetor com rotação balística, e o cartão seguinte da pilha avança para o primeiro plano.
- **Gatilho**: Arraste direcional com soltura de alta velocidade (`velocity > 0.2`).
- **Anatomia & Parâmetros Físicos**:
  - `const [props, api] = useSprings(cards.length, i => ({ x: 0, y: i * 4, scale: 1 - i * 0.04, rot: 0 }))`
  - No evento `useDrag`: cálculo de projeção de saída se $x > \text{threshold}$ ou $|v_x| > \text{threshold}$, animando para $x = \text{largura da janela} \times 1.5$.

---

### 9. Elastic Button Squash & Stretch
- **Comportamento Visual**: Feedback tátil visceral de clique. Ao pressionar o botão do mouse (`mousedown`), o elemento comprime seu eixo Y para 0.90 enquanto expande o eixo X para 1.06 (preservação de volume elástico). Ao soltar (`mouseup`), o elemento salta para $1.10\times$ no eixo vertical antes de estabilizar no repouso com micro-oscilações.
- **Gatilho**: Eventos de ponteiro `onMouseDown`, `onMouseUp`, `onMouseLeave`.
- **Anatomia & Parâmetros Físicos**:
  - `const [style, api] = useSpring(() => ({ scale: [1, 1], config: config.wobbly }))`
  - Pressionar: `api.start({ scale: [1.08, 0.90] })`; Soltar: `api.start({ scale: [1, 1] })`.

---

### 10. Kinetic Number Odometer / Rolling Metric Counter
- **Comportamento Visual**: Contador numérico dinâmico que transiciona de forma contínua entre valores inteiros ou decimais arbitrários (por exemplo, de `$ 1.250,00` para `$ 4.890,50`). A mola acelera vigorosamente nos primeiros números, atinge pico de velocidade e desacelera gradualmente até alinhar os centavos com precisão decimal.
- **Gatilho**: Atualização da propriedade numérica de entrada.
- **Anatomia & Parâmetros Físicos**:
  - `const { val } = useSpring({ val: targetNumber, from: { val: 0 }, config: config.slow })`
  - Interpolação direta no nó de texto: `<animated.span>{val.to(n => n.toLocaleString('pt-BR', { minimumFractionDigits: 2 }))}</animated.span>`.

---

## 5. Matemática do Movimento & Receitas de Código

### Parâmetros da Física de Hooke no React Spring

O comportamento da mola no React Spring é determinado pelo conjunto de parâmetros de configuração física passados no objeto `config`:

| Parâmetro | Tipo | Padrão | Descrição Matemática e Efeito Sensorial |
| :--- | :--- | :--- | :--- |
| **`mass`** | `number` | `1` | Inércia do corpo. Massas maiores ($>2$) aumentam a lentidão de aceleração e fazem o corpo projetar-se muito além do destino por pura inércia. |
| **`tension`** | `number` | `170` | Constante elástica $k$. Quanto maior ($>300$), mais rápida e violenta é a atração em direção ao destino. |
| **`friction`** | `number` | `26` | Resistência viscosa $c$. Valores baixos criam oscilações elásticas contínuas; valores altos absorvem o impacto sem oscilação. |
| **`velocity`** | `number` | `0` | Vetor de velocidade inicial injetado no início do movimento. Crucial para transições suaves de gestos. |
| **`precision`** | `number` | `0.01` | Limiar mínimo de deslocamento/velocidade para que o motor decrete repouso estático absoluto. |
| **`clamp`** | `boolean` | `false` | Quando `true`, desativa o overshoot: o corpo para instantaneamente ao tocar o valor de destino, eliminando oscilações reversas. |

---

### Presets Nativos Oficiais do React Spring

A biblioteca expõe presets prontos através de `import { config } from '@react-spring/web'`:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        PRESETS OFICIAIS DE FÍSICA (CONFIG)                             │
├──────────────────┬──────┬─────────┬──────────┬─────────────────────────────────────────┤
│ Preset           │ Mass │ Tension │ Friction │ Sensação e Aplicação Recomendada        │
├──────────────────┼──────┼─────────┼──────────┼─────────────────────────────────────────┤
│ config.default   │ 1    │ 170     │ 26       │ Equilíbrio natural. Uso geral.          │
│ config.gentle    │ 1    │ 120     │ 14       │ Suave, amplo e gracioso. Modais e abas. │
│ config.wobbly    │ 1    │ 180     │ 12       │ Saltitante, com múltiplos overshoots.   │
│ config.stiff     │ 1    │ 210     │ 20       │ Rápido, tenso e assertivo. Botões e taps│
│ config.slow      │ 1    │ 280     │ 60       │ Pesado e denso. Odômetros e contadores. │
│ config.molasses  │ 1    │ 280     │ 120      │ Extremamente denso e viscoso (mel).     │
└──────────────────┴──────┴─────────┴──────────┴─────────────────────────────────────────┘
```

---

### Receita de Código Funcional 1: Bottom Sheet Tátil com Inércia Balística & Reduced-Motion

Abaixo está a implementação completa e de grau de produção de um Bottom Sheet tátil que utiliza `@react-spring/web` e `@use-gesture/react`, respeitando preferências de acessibilidade e garantindo 60fps constantes através de mutação direta sem re-render do React.

```tsx
import React, { useEffect, useRef } from 'react'
import { useSpring, animated, config } from '@react-spring/web'
import { useDrag } from '@use-gesture/react'

interface TactileDrawerProps {
  isOpen: boolean
  onClose: () => void
  title: string
  children: React.ReactNode
}

// Hook de acessibilidade para detecção de preferência de movimento reduzido
function usePrefersReducedMotion(): boolean {
  const [prefersReducedMotion, setPrefersReducedMotion] = React.useState(false)

  useEffect(() => {
    const mediaQuery = window.matchMedia('(prefers-reduced-motion: reduce)')
    setPrefersReducedMotion(mediaQuery.matches)

    const handler = (event: MediaQueryListEvent) => setPrefersReducedMotion(event.matches)
    mediaQuery.addEventListener('change', handler)
    return () => mediaQuery.removeEventListener('change', handler)
  }, [])

  return prefersReducedMotion
}

export const TactileDrawer: React.FC<TactileDrawerProps> = ({
  isOpen,
  onClose,
  title,
  children,
}) => {
  const prefersReduced = usePrefersReducedMotion()
  const drawerHeight = 420 // Altura em pixels do painel aberto

  // Mola física que governa a coordenada vertical Y e a opacidade do backdrop
  const [{ y, backdropOpacity }, api] = useSpring(() => ({
    y: drawerHeight,
    backdropOpacity: 0,
    config: prefersReduced 
      ? { immediate: true } 
      : { tension: 280, friction: 28, mass: 0.8 },
  }))

  // Sincroniza o estado de abertura inicial com a física
  useEffect(() => {
    if (isOpen) {
      api.start({
        y: 0,
        backdropOpacity: 1,
        immediate: prefersReduced,
        config: config.gentle,
      })
    } else {
      api.start({
        y: drawerHeight,
        backdropOpacity: 0,
        immediate: prefersReduced,
      })
    }
  }, [isOpen, api, drawerHeight, prefersReduced])

  // Vinculação de gestos táteis com inércia contínua
  const bindGesture = useDrag(
    ({ last, movement: [, my], velocity: [, vy], direction: [, dy], cancel }) => {
      // Bloqueia arraste para cima além do limite (resistência com decaimento logarítmico)
      const currentY = my < 0 ? my * 0.15 : my

      if (last) {
        // Se soltou com alta velocidade descendente ou arrastou mais de 40% da altura
        const shouldClose = (dy > 0 && vy > 0.45) || currentY > drawerHeight * 0.4

        if (shouldClose) {
          api.start({
            y: drawerHeight,
            backdropOpacity: 0,
            config: { tension: 240, friction: 26, velocity: vy },
            onRest: () => onClose(),
          })
        } else {
          // Retorna elasticamente ao repouso no topo
          api.start({
            y: 0,
            backdropOpacity: 1,
            config: config.stiff,
          })
        }
      } else {
        // Atualização em tempo real frame a frame fora do ciclo do React
        api.start({
          y: Math.max(0, currentY),
          backdropOpacity: Math.max(0, 1 - currentY / drawerHeight),
          immediate: true,
        })
      }
    },
    {
      from: () => [0, y.get()],
      bounds: { top: -20 },
      rubberband: true,
      filterTaps: true,
    }
  )

  if (!isOpen && y.get() >= drawerHeight) return null

  return (
    <div className="fixed inset-0 z-50 flex items-end justify-center pointer-events-auto">
      {/* Backdrop transparente com blur reativo via SpringValue */}
      <animated.div
        onClick={onClose}
        style={{ opacity: backdropOpacity }}
        className="absolute inset-0 bg-neutral-950/60 backdrop-blur-sm cursor-pointer"
      />

      {/* Painel do Drawer animado puramente na GPU */}
      <animated.div
        {...bindGesture()}
        style={{
          transform: y.to(val => `translate3d(0, ${Math.max(0, val)}px, 0)`),
          height: `${drawerHeight}px`,
        }}
        className="relative w-full max-w-lg rounded-t-3xl bg-neutral-900 border-t border-neutral-800 p-6 text-neutral-100 shadow-2xl touch-none select-none"
      >
        {/* Barra de ancoragem tátil (Handle indicator) */}
        <div className="mx-auto -mt-2 mb-4 h-1.5 w-12 rounded-full bg-neutral-700/80 hover:bg-neutral-600 transition-colors cursor-grab active:cursor-grabbing" />

        <div className="flex items-center justify-between border-b border-neutral-800 pb-3 mb-4">
          <h2 className="text-lg font-semibold tracking-tight">{title}</h2>
          <button
            onClick={onClose}
            className="rounded-full p-1.5 text-neutral-400 hover:text-neutral-100 hover:bg-neutral-800 focus:outline-none focus:ring-2 focus:ring-neutral-400"
          >
            ✕
          </button>
        </div>

        <div className="overflow-y-auto max-h-[290px] pr-2 text-sm text-neutral-300">
          {children}
        </div>
      </animated.div>
    </div>
  )
}
```

---

### Receita de Código Funcional 2: Objeto 3D Físico com `@react-spring/three` & R3F

Demonstração de integração tridimensional de alta performance sem colapso de render loops:

```tsx
import React, { useRef, useState } from 'react'
import { Canvas } from '@react-three/fiber'
import { useSpring, animated, config } from '@react-spring/three'
import * as THREE from 'three'

function InteractivePhysicalPrism() {
  const [hovered, setHovered] = useState(false)
  const [clicked, setClicked] = useState(false)

  // Mola de Three.js animando múltiplos eixos e cores simultaneamente
  const { scale, rotation, color, roughness } = useSpring({
    scale: clicked ? [1.3, 0.7, 1.3] : hovered ? [1.15, 1.15, 1.15] : [1, 1, 1],
    rotation: clicked
      ? [0, Math.PI * 2, 0]
      : hovered
      ? [0.4, 0.6, 0]
      : [0, 0, 0],
    color: clicked ? '#38bdf8' : hovered ? '#818cf8' : '#6366f1',
    roughness: hovered ? 0.1 : 0.4,
    config: clicked ? config.wobbly : config.gentle,
  })

  return (
    <animated.mesh
      scale={scale as unknown as THREE.Vector3}
      rotation={rotation as unknown as THREE.Euler}
      onPointerOver={() => setHovered(true)}
      onPointerOut={() => setHovered(false)}
      onClick={() => setClicked(!clicked)}
      castShadow
      receiveShadow
    >
      <octahedronGeometry args={[1.8, 0]} />
      <animated.meshStandardMaterial
        color={color}
        roughness={roughness}
        metalness={0.6}
        wireframe={false}
      />
    </animated.mesh>
  )
}

export function ThreePhysicsScene() {
  return (
    <div className="w-full h-[450px] rounded-2xl overflow-hidden bg-neutral-950 border border-neutral-800 shadow-inner">
      <Canvas camera={{ position: [0, 0, 5], fov: 50 }}>
        <ambientLight intensity={0.6} />
        <directionalLight position={[10, 10, 5]} intensity={1.5} />
        <pointLight position={[-10, -10, -5]} color="#38bdf8" intensity={0.8} />
        <InteractivePhysicalPrism />
      </Canvas>
    </div>
  )
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar o **React Spring** como motor primário de movimento em uma aplicação, a IA e o Arquiteto de Software devem registrar as seguintes convenções no plano técnico antes de iniciar a codificação:

### 1. Declaração do Motor e Módulos Alvo
- **Target Principal**: Declarar expressamente se o projeto usará `@react-spring/web` (DOM/HTML/SVG) ou `@react-spring/three` (3D WebGL via R3F).
- **Parceiro Gestual Obrigatório**: Para qualquer microinteração baseada em arrasto, pinça ou inércia tátil, estipular `@use-gesture/react` como companheiro mandatório, proibindo manipuladores crus de `onMouseMove` com `useState`.

### 2. Dicionário de Tokens Físicos (Substituição de Milissegundos)
No `DESIGN_BLUEPRINT.md`, banir referências a tempos arbitrários como `duration: 300ms` para componentes táteis e declarar tokens físicos de mola:
```json
{
  "motionTokens": {
    "snappyTap": { "tension": 380, "friction": 22, "mass": 0.6, "clamp": false },
    "drawerSheet": { "tension": 260, "friction": 26, "mass": 0.9, "clamp": false },
    "modalPresence": { "tension": 220, "friction": 24, "mass": 1.0, "clamp": true },
    "numericOdometer": { "tension": 280, "friction": 60, "mass": 1.0, "clamp": true },
    "decorativeBadge": { "tension": 180, "friction": 12, "mass": 1.0, "clamp": false }
  }
}
```

### 3. Regra Arquitetural de Não-Renderização
- **Cláusula de Performance**: Qualquer desenvolvedor ou agente deve prefixar componentes mutáveis como `animated.div`, `animated.svg` ou `animated(CustomComponent)`. É estritamente vedado sincronizar coordenadas de mola com estados locais do React (`useState`) durante a execução de um loop de física.

### 4. Protocolo Obrigatório de Movimento Reduzido (Accessibility Fallback)
Todo componente interativo deve incluir uma verificação condicional para a media query `prefers-reduced-motion`. O comportamento padrão na ativação deve ser `immediate: true` (execução em 0 frames sem transição elástica), reduzindo o deslocamento espacial a zero e mantendo no máximo uma transição de opacidade instantânea.
