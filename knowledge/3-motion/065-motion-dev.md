---
id: "motion-dev"
name: "Motion (motion.dev)"
url: "https://motion.dev/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["Physics-Driven Spring Fluidity", "FLIP Layout Projection", "GPU Off-Thread WAAPI", "Declarative Micro-Gestures", "Kinetic Orchestration"]
densidade_informacao: "Flexivel"
impacto_visual: "Sutil/Invisivel a Moderado (Feel & Choreography)"
custo_computacional: "Baixo a Medio (WAAPI GPU off-thread / JS Spring RAF)"
stack_frameworks: ["React 19 / 18 (motion/react)", "Vanilla JS / TypeScript (motion)", "Vue (motion-v)", "Next.js (App Router / RSC)", "Tailwind CSS v4 & v3"]
compatibilidade:
  combinacoes_recomendadas: ["Shadcn UI", "Tailwind CSS v4", "Lenis Scroll", "Lucide React", "Radix UI Primitives", "React Three Fiber"]
  conflitos_esteticos: ["Transições CSS puras concorrentes declaradas nos mesmos nós", "Reflow ingênuo de propriedades de layout (width, height, top, left) sem layout projection", "Animações lineares sem inércia física ou molas superamortecidas com sensação pastosa"]
---

# Motion (motion.dev) — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)

O **Motion** (`https://motion.dev/`), arquitetado e liderado por **Matt Perry**, representa a consolidação definitiva do ecossistema moderno de animação na web. Fruto da unificação histórica entre o aclamado **Framer Motion** (o padrão de mercado no ecossistema React) e o **Motion One** (o pioneiro motor de animação baseado na Web Animations API nativa do navegador), o Motion transcendeu as fronteiras do React para se estabelecer como uma infraestrutura universal e agnóstica de frameworks (atendendo React via `motion/react`, Vanilla JavaScript / TypeScript via `motion`, e Vue via `motion-v`).

### A Ruptura: Da Curva de Tempo Estática à Física Newtoniana em Tempo Real

Tradicionalmente, a web tratou animações sob o paradigma da cinematografia clássica: curvas de interpolação temporal de duração fixa (como `ease-in-out` de 300ms). Esse modelo impõe um comportamento artificial e robótico às interfaces:
- **Ausência de Massa e Inércia**: Um elemento de 20 pixels e um modal de 800 pixels demoram exatamente os mesmos 300ms para se deslocar, violando a intuição humana de peso e volume.
- **Quebra Mecânica em Interrupções (Jank de Interrupção)**: Quando um usuário clica em um botão no meio de uma transição de fechamento para reabri-lo, uma animação CSS clássica zera abruptamente a velocidade angular/linear ou "salta" de volta, quebrando a ilusão de materialidade contínua.

O Motion substitui esse paradigma por **física de osciladores harmônicos amortecidos (Damped Harmonic Springs)**. Em vez de declarar um tempo rígido (`duration: 0.3s`), a engenharia declara propriedades físicas inerentes à matéria:
- **Rigidez da Mola (`stiffness`)**: A tensão elástica que puxa o elemento de volta à sua posição de repouso.
- **Fator de Amortecimento (`damping`)**: O atrito viscoso do ambiente que dissipa a energia cinética do sistema.
- **Massa (`mass`)**: A inércia do objeto, determinando quanta força é necessária para acelerá-lo ou desacelerá-lo.
- **Conservação de Momento (`Velocity Handover`)**: Se um componente está sendo arrastado pelo ponteiro do usuário a 1200 pixels por segundo e é solto, o Motion injeta esse vetor de velocidade instantâneo ($v_0$) diretamente nas equações diferenciais da mola. O elemento não para de forma seca; ele desliza com desaceleração newtoniana perfeita até o repouso.

---

### A Arquitetura do Motor Híbrido (Hybrid Animation Engine)

O grande divisor técnico do Motion é sua arquitetura de **motor híbrido de duas vias**, que elimina o clássico dilema entre a performance bruta do navegador e a expressividade dinâmica do JavaScript:

```
┌────────────────────────────────────────────────────────────────────────┐
│                        MOTION RUNTIME PIPELINE                         │
└────────────────────────────────────────────────────────────────────────┘
                                    │
                  Analisa Propriedades & Restrições
                                    │
            ┌───────────────────────┴───────────────────────┐
            ▼                                               ▼
┌───────────────────────────────┐               ┌───────────────────────────────┐
│     RAMO WAAPI OFF-THREAD     │               │        RAMO JS RUNTIME        │
│    (Web Animations API)       │               │    (requestAnimationFrame)    │
├───────────────────────────────┤               ├───────────────────────────────┤
│ • Hardware-accelerated GPU    │               │ • Molas newtonianas em tempo  │
│ • Zero JS execution na thread │               │   real com velocity transfer  │
│ • Propriedades: transform,    │               │ • Layout Projection (FLIP)    │
│   opacity, filter, clip-path  │               │ • Gestos contínuos de drag    │
│ • 60/120fps garantidos mesmo  │               │ • Interpolações dinâmicas     │
│   sob bloqueio da main-thread │               │   frame-a-frame (useTransform)│
└───────────────────────────────┘               └───────────────────────────────┘
```

1. **Execução Off-Main-Thread via WAAPI**:
   Para propriedades compositadas pela GPU (`transform: translate3d/scale/rotate`, `opacity`), o Motion gera keyframes de alta densidade e os entrega diretamente ao pipeline C++ nativo do navegador via Web Animations API. Essa execução roda fora da thread principal de JavaScript; mesmo que uma re-renderização massiva de dados trave o React ou ocorra um bloqueio na main-thread, a animação continua rodando a 120fps sem perder um único quadro.
2. **Execução JS Engine com Reconciliação Instantânea**:
   Quando a animação exige cálculo físico de molas dinâmicas, detecção de colisões elásticas de drag ou projeção de layout compartilhada, o Motion comuta transparentemente para seu loop otimizado de `requestAnimationFrame`, mantendo consumo mínimo de CPU e transferindo o estado para o compositor na primeira oportunidade viável.

---

### Layout Projection: A Geometria FLIP sem Reflows Destrutivos

Mudar o tamanho ou posição de nós na árvore DOM tradicional (`width`, `height`, `top`, `left`, `flex-basis`) é uma das operações computacionalmente mais caras da renderização web, acionando o ciclo completo de:
$$\text{Recalculate Style} \longrightarrow \text{Layout (Reflow)} \longrightarrow \text{Paint} \longrightarrow \text{Composite}$$

O Motion contorna essa restrição física do navegador através do seu algoritmo exclusivo de **Layout Projection** (baseado no conceito FLIP — First, Last, Invert, Play):
1. **First**: O motor lê as coordenadas espaciais globais do elemento antes da mutação de estado através de `getBoundingClientRect()`.
2. **Last**: O estado da UI muda instantaneamente (por exemplo, uma aba muda de lugar ou uma lista é reordenada); o elemento assume sua posição final no DOM em um único ciclo de leitura.
3. **Invert**: O Motion calcula as diferenças vetoriais:
   $$\Delta x = x_{\text{first}} - x_{\text{last}}, \quad \Delta y = y_{\text{first}} - y_{\text{last}}$$
   $$\Delta s_x = \frac{\text{width}_{\text{first}}}{\text{width}_{\text{last}}}, \quad \Delta s_y = \frac{\text{height}_{\text{first}}}{\text{height}_{\text{last}}}$$
   Ele então aplica instantaneamente uma transformação matricial na GPU:
   $$\mathbf{T}_{\text{invert}} = \begin{bmatrix} \Delta s_x & 0 & \Delta x \\ 0 & \Delta s_y & \Delta y \\ 0 & 0 & 1 \end{bmatrix}$$
   Isso faz o elemento parecer visualmente estar exatamente na sua posição original, sem causar reflow.
4. **Play**: O Motion anima o `transform` da matriz invertida em direção à matriz identidade ($\mathbf{I}$), com aceleração de mola física.
5. **Scale Distortion Correction (Correção Automática de Escala)**: Em abordagens manuais de FLIP, escalar um container distorce textos, imagens e cantos arredondados (`border-radius`) dos filhos. O Motion detecta nós descendentes marcados com `layout` e aplica uma **matriz de transformação inversa proporcional** em cada frame, preservando tipografia nítida e raios de borda perfeitamente circulares durante toda a transição.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Interface e Casos de Uso Críticos

1. **Sistemas de Abas Deslizantes e Menus Segmentados ("Sliding Pill")**:
   Interfaces onde um fundo iluminado, borda ativa ou cápsula indicadora desliza de um item de menu para outro com inércia física, adaptando sua largura e posição dinamicamente com base no tamanho do texto da aba (`layoutId="active-indicator"`).
2. **Expansão de Cartão para Tela Cheia / Modal (Shared Element Transitions)**:
   Experiências ricas de e-commerce, galerias de portfólio e interfaces de leitura onde clicar em um card em miniatura faz com que ele expanda de forma contínua até preencher o centro da tela como um modal ou página de detalhes, mantendo a integridade perceptual do objeto (o usuário nunca perde o foco do item).
3. **Reordenação Dinâmica de Listas e Tabelas (Drag-and-Drop / Kanban)**:
   Listas de tarefas priorizadas, cartões de pipeline de vendas ou colunas de dados onde arrastar um item faz os elementos adjacentes abrirem espaço organicamente com física de repulsão elástica (`Reorder.Group`, `Reorder.Item`).
4. **Acordeões, Drawers e Paineis Sanfonados com Conteúdo Dinâmico**:
   Containers que expandem de zero para o tamanho natural do conteúdo sem necessidade de fixar alturas em pixels (`height: "auto"`), interpolando as dimensões de forma perfeitamente suave através de `layout="size"` e `<AnimatePresence>`.
5. **Navegação de Múltiplos Passos e Fluxos Wizard**:
   Interfaces sequenciais (telas de checkout, onboarding guiado) onde telas que entram e saem deslizam de forma orquestrada em vetores bidirecionais sem duplicar o espaço vertical (`mode="popLayout"`).
6. **Micro-Interações Táteis de Alta Precisão**:
   Botões e switches que reagem ao clique com feedback de compressão tátil (`whileTap={{ scale: 0.96 }}`), cartões interativos que rotacionam tridimensionalmente sob o ponteiro (`tilt effect`) e botões magnéticos que atraem suavemente o cursor.

---

### Papel na Composição Visual (A Aplicação da Regra 60-30-10)

```
┌────────────────────────────────────────────────────────────────────────┐
│                   A REGRA 60-30-10 DE MOTION DESIGN                    │
└────────────────────────────────────────────────────────────────────────┘

  [ 60% — A FÍSICA INVISÍVEL ] ─── Micro-interações táteis e respostas
                                   imediatas de 120ms-180ms (hover, tap,
                                   focus, checkboxes, switches). O usuário
                                   sente consistência, não "efeito".

  [ 30% — A ORQUESTRAÇÃO     ] ─── Transições de layout estrutural,
                                   abertura de dropdowns, colapso de
                                   sidebars, sliding tabs e cascatas
                                   staggered de listas (200ms-350ms).

  [ 10% — OS SHOWSTOPPERS    ] ─── Shared element morphings dramáticos
                                   (Card-to-Modal de tela cheia), heróis
                                   com tipografia cinética e timelines
                                   coreografadas de onboarding.
```

- **60% — A Física Invisível (Feel Tátil & Resposta de Sistema)**:
  O Motion deve gerenciar todas as respostas imperceptíveis de controle físico: a micro-compressão de um botão ao toque, o amortecimento suave ao passar o cursor sobre um card de tabela, a sutil vibração de erro em um campo de input. Nessas superfícies, a animação nunca dura mais do que 120ms a 180ms e emprega molas de alta rigidez e alto amortecimento (`stiffness: 400, damping: 30`). O usuário não percebe que "houve uma animação"; ele percebe que o sistema é responsivo e sólido.
- **30% — A Orquestração de Navegação e Layout Estrutural**:
  Camada responsável por conduzir a atenção espacial do usuário durante trocas de estado. Inclui o deslizamento da cápsula indicadora nas tabs, a revelação em cascata ordenada de itens em uma lista (`staggerChildren: 0.05`), a expansão suave de um accordion ao ler dados adicionais e a saída de toasts de notificação. As molas aqui são orgânicas e fluidas (`stiffness: 260, damping: 22`).
- **10% — Os Showstoppers Cinematográficos (Hero Morphs)**:
  Momentos raros e deliberados de espetáculo visual: o clique em um projeto da galeria que se desdobra cinematograficamente no modal de tela cheia com desfoque de fundo gradativo, ou a revelação tipográfica cinética na seção principal de uma landing page. Nesses casos, o Motion assume o protagonismo estético com transições ricas de 400ms a 600ms.

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Práticas Proibidas & Anti-Padrões Críticos

1. **Animar Propriedades de Layout sem Layout Projection**:
   - **O Erro**: Declarar transições diretas sobre propriedades como `animate={{ width: 400, height: 300, top: 100 }}` sem utilizar a prop `layout`.
   - **O Impacto**: Força o navegador a recalcular a geometria de toda a página (Layout Reflow) 60 a 120 vezes por segundo. Em páginas com árvores DOM densas (tabelas, dashboards), isso provoca quedas imediatas para 15-20fps, gerando travamentos perceptíveis em dispositivos móveis.
   - **A Correção**: Utilizar transformações de escala e posição via GPU (`x`, `y`, `scale`) ou delegar o cálculo de geometria à prop declarativa `layout` ou `layoutId`.
2. **Guerra de Motores: Conflito com Transições CSS Puras**:
   - **O Erro**: Adicionar classes utilitárias como `transition-all duration-300` do Tailwind em um elemento `<motion.div>` que já possui props de animação como `animate={{ scale: 1.05 }}`.
   - **O Impacto**: O motor de CSS do navegador e o motor de física do Motion tentam atualizar a mesma propriedade de forma assíncrona, criando um conflito cíclico que resulta em tremores visuais ("jitter"), travamentos e perda de velocidade no repouso.
   - **A Correção**: Remover completamente classes `transition-*` de elementos governados por Motion. Se o Motion controla o nó, ele deve ter exclusividade sobre a interpolação.
3. **Proliferação Descontrolada de Camadas de GPU (`will-change` Thrashing)**:
   - **O Erro**: Aplicar `layout` ou propriedades de animação em centenas de linhas de uma tabela virtual ou grid infinito sem desmontagem.
   - **O Impacto**: Cada elemento animado ativamente pode ser promovido a uma camada de composição de hardware separada na GPU (`compositing layer`). Em aparelhos com restrição de memória gráfica, a memória de vídeo (VRAM) se esgota rapidamente, forçando o navegador a descartar texturas e provocando o recarregamento forçado da página (crash por memória).
   - **A Correção**: Utilizar animações apenas em nós visíveis no viewport; usar `<motion.div>` nos elementos de container e delegar aos nós internos variações via CSS puro ou herança de `variants`.

---

### ⚠️ Acessibilidade Obrigatória & Conformidade WCAG 2.2

O Critério de Sucesso **2.3.3 (Animation from Interactions - Nível AAA)** das diretrizes WCAG exige que animações de movimento disparadas por interação do usuário possam ser desativadas, a menos que a animação seja estritamente essencial para a funcionalidade do sistema.

#### Protocolo de Implementação de Redução de Movimento:
O Motion disponibiliza o hook nativo `useReducedMotion()`. Quando o sistema operacional do usuário está configurado com `prefers-reduced-motion: reduce`, o sistema deve:
1. Eliminar transições espaciais amplas (deslocamentos em eixos X e Y superiores a 4px).
2. Desativar oscilações elásticas com rebotes (`bounce: 0` ou transições diretas de opacidade).
3. Manter feedback de estado através de transições instantâneas ou fades discretos de opacidade (`opacity: 0 -> 1` em 80ms).

```tsx
import { useReducedMotion, motion } from "motion/react";

export function AccessibleCard() {
  const shouldReduceMotion = useReducedMotion();

  return (
    <motion.div
      initial={{ opacity: 0, y: shouldReduceMotion ? 0 : 20 }}
      animate={{ opacity: 1, y: 0 }}
      transition={{
        duration: shouldReduceMotion ? 0.08 : 0.35,
        ease: "easeOut",
      }}
      className="p-6 rounded-xl bg-card border border-border"
    >
      Conteúdo Acessível
    </motion.div>
  );
}
```

---

## 4. Catálogo Detalhado de Componentes, Padrões & Efeitos Notáveis

### 1. Active Indicator Sliding Pill (Shared Layout Tab Tracker)
- **Comportamento Visual**:
  - *Estado Inicial*: A pílula de fundo ativa repousa sob a primeira aba selecionada.
  - *Durante a Transição*: Ao clicar ou navegar com setas do teclado para outra aba, a pílula não desaparece nem corta: ela se estica, desliza e encolhe organicamente, adaptando sua largura em tempo real à largura do rótulo da nova aba de destino.
  - *No Repouso*: Encaixe milimétrico sob o novo botão de aba, com cantos arredondados inalterados.
- **Gatilho**: Mudança de estado da aba ativa (`selectedTabId`), acionando a projeção geométrica através da mesma chave `layoutId="active-pill"`.
- **Anatomia & Onde Encaixar**: Segmented controls em dashboards, alternadores de período em painéis de análise financeira, navegação de abas no topo de páginas de configurações.

### 2. Expandable Card to Modal (Shared Element Morphing)
- **Comportamento Visual**:
  - *Estado Inicial*: Um cartão compacto posicionado dentro de uma grade de três colunas, exibindo thumbnail, categoria e título.
  - *Durante a Transição*: Ao receber clique, o container do cartão expande suas fronteiras até ocupar 90vw/85vh no centro da viewport. A imagem interna escala suavemente com correção de distorção de escala, enquanto o texto de detalhes adicionais é revelado gradualmente. Simultaneamente, uma camada de backdrop translúcida com blur ganha opacidade.
  - *No Repouso*: O modal estabiliza no centro; o botão de fechar (`Esc`) ganha foco acessível.
- **Gatilho**: Clique sobre o card selecionado (`selectedCardId`), montando o elemento modal sob o mesmo `layoutId={card.id}` dentro de um portal com `<AnimatePresence>`.
- **Anatomia & Onde Encaixar**: Galerias de portfólio de design, feeds de produtos em e-commerce, cards de expansão de métricas em analytics.

### 3. Staggered Cascade Reveal (Orquestração de Entrada em Cascata)
- **Comportamento Visual**:
  - *Estado Inicial*: Os elementos filhos repousam ocultos com `opacity: 0` e translação vertical descendente (`y: 16px`).
  - *Durante a Transição*: Ao carregar a página ou o container entrar no viewport, o primeiro elemento surge imediatamente; os elementos subsequentes entram com um atraso de intervalo rítmico fixo (ex: 45 milissegundos por nó).
  - *No Repouso*: Todos os nós atingem `opacity: 1` e `y: 0`, estabelecendo uma leitura sequencial natural sem bloquear a percepção global da tela.
- **Gatilho**: Disparo por visibilidade via `inView` ou variantes (`variants`) de orquestração do nó pai com `staggerChildren: 0.045` e `delayChildren: 0.1`.
- **Anatomia & Onde Encaixar**: Listas de transações financeiras, grids de recursos em landing pages, resultados de busca em tempo real.

### 4. Auto-Height Accordion / Collapsible Drawer (Interpolador de Altura Intrínseca)
- **Comportamento Visual**:
  - *Estado Inicial*: O corpo de texto da sanfona está completamente fechado (`height: 0, opacity: 0, overflow: "hidden"`).
  - *Durante a Transição*: Ao clicar no gatilho, o Motion lê dinamicamente a altura de conteúdo intrínseca (`scroll-height`) dos nós internos e interpola suavemente de 0 para a dimensão exata com mola física amortecida, empurrando os elementos vizinhos sem saltos secos de layout.
  - *No Repouso*: O container assume `height: "auto"`, permitindo que redimensionamentos de janela ou injeção assíncrona de texto fluam naturalmente.
- **Gatilho**: Alternância do estado booleano `isOpen`, encapsulado por `<AnimatePresence initial={false}>` e `motion.div layout="size"`.
- **Anatomia & Onde Encaixar**: Seções de FAQ corporativas, painéis retráteis de filtros laterais, gavetas de checkout e árvores de navegação em documentação.

### 5. Directional Multi-Step Switcher com `mode="popLayout"`
- **Comportamento Visual**:
  - *Estado Inicial*: A etapa atual do formulário ou onboarding está visível no centro.
  - *Durante a Transição*: Ao clicar em "Avançar", a etapa atual desliza para a esquerda (`x: -60px`) enquanto perde opacidade. Graças à propriedade `mode="popLayout"`, o nó que sai é instantaneamente retirado do fluxo normal de layout do documento e promovido a posicionamento absoluto pelo Motion, permitindo que a nova etapa entre pela direita (`x: 60px -> 0`) no mesmo frame sem duplicar a altura da página.
  - *No Repouso*: A nova etapa estabiliza perfeitamente no container com foco acessível no primeiro campo de input.
- **Gatilho**: Incremento ou decremento do índice numérico da etapa (`stepIndex`), acoplado a variantes direcionais via `custom={direction}`.
- **Anatomia & Onde Encaixar**: Wizards de cadastro em múltiplos passos, carrosséis de onboarding em aplicativos móveis, fluxos de emissão de faturamento.

### 6. Scroll-Driven Sticky Header Interpolation (Navegador Retrátil Sincronizado)
- **Comportamento Visual**:
  - *Estado Inicial*: Em `scrollY == 0`, a barra de navegação superior possui altura generosa (72px), tipografia expandida e fundo completamente transparente.
  - *Durante a Transição*: Conforme o usuário rola a página entre 0 e 120 pixels, a altura é reduzida linearmente para 52px, o espaçamento interno encolhe, uma borda inferior de 1px ganha opacidade de 0% para 100%, e o fundo adquire um acabamento fosco translúcido com `backdrop-filter: blur(12px)`.
  - *No Repouso*: Navbar compacta e legível fixa no topo, mantendo área útil de visualização maximizada durante a leitura de artigos extensos.
- **Gatilho**: Valor numérico contínuo de rolagem obtido via `useScroll()` e mapeado com `useTransform()`.
- **Anatomia & Onde Encaixar**: Barra de navegação principal de portais editoriais, SaaS landings e documentações densas.

### 7. Magnetic Button com Dynamic Pointer Tracking
- **Comportamento Visual**:
  - *Estado Inicial*: O botão repousa no seu alinhamento padrão de grid ou flexbox.
  - *Durante a Transição*: Quando o cursor do mouse se aproxima do botão (raio de atração de ~60px), o centro do botão é atraído em direção às coordenadas do ponteiro com atenuação calculada (cerca de 25% a 35% do deslocamento real), simulando um campo de atração magnética física.
  - *No Repouso / Desconexão*: Quando o cursor ultrapassa a fronteira de atração, o botão se solta e retorna à sua coordenada neutra original com um rebote suave de mola física (`stiffness: 350, damping: 20`).
- **Gatilho**: Eventos `onPointerMove` e `onPointerLeave` sobre a zona de captura, associados a hooks `useSpring()` para os eixos $X$ e $Y$.
- **Anatomia & Onde Encaixar**: Botões de Call to Action (CTA) prioritários em seções hero, botões de ação flutuantes (FAB), botões de play em players de áudio/vídeo.

### 8. Interactive 3D Tilt Card com Reflexo Especular
- **Comportamento Visual**:
  - *Estado Inicial*: Superfície retangular bidimensional plana.
  - *Durante a Transição*: O card rotaciona suavemente nos eixos $X$ e $Y$ (até um limite máximo de $\pm 12^\circ$), respondendo dinamicamente à posição relativa do mouse em relação ao centro geométrico do cartão. Simultaneamente, uma camada radial de gradiente semitransparente se desloca na direção oposta, simulando a reflexão especular de um feixe de luz incidindo sobre vidro ou policarbonato polido.
  - *No Repouso*: Ao retirar o ponteiro, o cartão desacelera fluidamente de volta à inclinação neutra de $0^\circ$ nos dois eixos.
- **Gatilho**: Leitura normalizada de coordenadas `clientX` e `clientY` dentro de `useMotionValue` acoplado a `useSpring` e propriedades `rotateX` e `rotateY`.
- **Anatomia & Onde Encaixar**: Cartões de planos de precificação Enterprise, ingressos digitais comemorativos, crachás de evento, mostruário de certificados de segurança.

### 9. Kinetic Reorderable List (Drag-to-Reorder com Physics Snapping)
- **Comportamento Visual**:
  - *Estado Inicial*: Lista vertical de itens empilhados uniformemente.
  - *Durante a Transição*: Quando o usuário clica e arrasta um item, ele eleva no eixo $Z$ visual (sombra projetada profunda e escala sutil de 1.02x). Conforme o item cruza os limiares dos itens vizinhos, os nós adjacentes se deslocam verticalmente para cima ou para baixo através de projeção FLIP instantânea, abrindo uma fenda no layout para acomodar o item que está sendo manipulado.
  - *No Repouso*: Ao soltar, o item se acomoda no novo slot com uma mola newtoniana, e os nós vizinhos confirmam sua nova posição sem piscar ou recarregar.
- **Gatilho**: Gesto de arrasto tátil integrado às primitivas `<Reorder.Group>` e `<Reorder.Item>`.
- **Anatomia & Onde Encaixar**: Quadros de tarefas estilo Kanban (estágios de progresso), reordenação de faixas em playlists, painéis de personalização de colunas em datagrids.

### 10. Kinetic Typography Split-Text & Mask Reveal
- **Comportamento Visual**:
  - *Estado Inicial*: Cada palavra ou linha de texto está posicionada com translação vertical de 100% (totalmente para fora do seu container delimitador) e escondida por um invólucro com `overflow: hidden`.
  - *Durante a Transição*: As palavras sobem rapidamente para sua posição natural de leitura através de um movimento elástico veloz e enérgico, cortadas geometricamente pelo plano de máscara da linha. O efeito cria a sensação de que o texto está sendo ejetado ou impresso a laser a partir de uma ranhura dimensional na página.
  - *No Repouso*: As palavras estabilizam perfeitamente alinhadas à grade de linha tipográfica do documento.
- **Gatilho**: Visibilidade em tela via `inView` ou disparo imediato no carregamento inicial da página com transição escalonada entre palavras (`stagger: 0.035`).
- **Anatomia & Onde Encaixar**: Manchetes e títulos principais (H1) em landing pages de lançamentos de tecnologia, citações de manifesto de marca e chamadas editoriais de alto prestígio.

---

## 5. Matemática do Movimento & Receitas de Código

### A Física do Oscilador Harmônico Amortecido

Diferente de sistemas gráficos puramente geométricos, o Motion fundamenta sua engine de física na equação diferencial clássica de segunda ordem para um **oscilador harmônico amortecido**:

$$m \frac{d^2 x(t)}{dt^2} + c \frac{dx(t)}{dt} + k x(t) = 0$$

Onde:
- $m$: Massa do elemento (`mass`). Representa a inércia do objeto físico.
- $c$: Coeficiente de amortecimento viscoso (`damping`). Representa o atrito do meio.
- $k$: Constante elástica ou rigidez da mola (`stiffness`). Representa a força restauradora.
- $x(t)$: Deslocamento vetorial em relação à posição de repouso ($x = 0$) no tempo $t$.

A razão de amortecimento adimensional ($\zeta$) governa fundamentalmente a natureza estética e comportamental da transição:

$$\zeta = \frac{c}{2\sqrt{k \cdot m}}$$

1. **Subamortecido ($\zeta < 1$)**: A mola ultrapassa o alvo de repouso antes de estabilizar, gerando o clássico efeito de **rebote elástico (overshoot / bounce)**.
2. **Amortecimento Crítico ($\zeta = 1$)**: O sistema retorna ao repouso no menor tempo fisicamente possível sem qualquer oscilação ou ultrapassagem do alvo. Este é o padrão áureo para micro-interações de produtividade enterprise.
3. **Superamortecido ($\zeta > 1$)**: O atrito supera a força restauradora da mola, produzindo um retorno lento, denso e pastoso ao repouso. Deve ser evitado em interfaces de usuário sob risco de causar sensação de lentidão e peso computacional artificial.

---

### Tabela de Presets de Molas Testados para Design Systems

| Perfil de Movimento | `stiffness` | `damping` | `mass` | Razão $\zeta$ | Tempo de Repouso | Aplicação Recomendada |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Snappy / Micro** | `450` | `35` | `0.8` | $\approx 0.92$ | $\sim 160\text{ms}$ | Botões, switches, checkboxes, micro-badges de status |
| **Fluid / Navigation** | `300` | `28` | `1.0` | $\approx 0.81$ | $\sim 260\text{ms}$ | Pílula deslizante de abas (`layoutId`), dropdown menus |
| **Gentle / Sheet** | `180` | `22` | `1.0` | $\approx 0.82$ | $\sim 380\text{ms}$ | Drawers laterais, expansão de cards para modal, sheets |
| **Bouncy / Playful** | `220` | `14` | `1.0` | $\approx 0.47$ | $\sim 520\text{ms}$ | Notificações de conquista, celebração de onboarding |
| **Critical / Precision**| `400` | `40` | `1.0` | $= 1.00$ | $\sim 180\text{ms}$ | Modais corporativos, paleta de comandos `Cmd+K` |

---

### Tabela de Curvas de Bézier Equivalentes (WAAPI / Timed Animations)

Para animações puramente temporizadas onde a duração exata em milissegundos é contratual ou ao utilizar transições executadas estritamente na GPU via WAAPI nativa:

```css
/* Curvas de Interpolação Recomendadas */
--ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);       /* Padrão Apple/Linear: início explosivo e freio suave */
--ease-snappy-quartz: cubic-bezier(0.25, 1, 0.5, 1);   /* Rápido e responsivo para micro-interações */
--ease-anticipate: cubic-bezier(0.34, 1.56, 0.64, 1);  /* Leve antecipação e overshoot com duração fechada */
--ease-in-out-smooth: cubic-bezier(0.65, 0, 0.35, 1);  /* Transições de página e rota simétricas */
```

---

### Receitas de Código Completas e Funcionais

#### Receita 1: Interactive Tab Bar com Sliding Pill Morphing (`layoutId`)

Um componente completo e tipado em TypeScript, React 19 / 18, Tailwind CSS v4 e o novo pacote unificado `motion/react`, com suporte total à navegação via teclado e layout adaptativo:

```tsx
"use client";

import React, { useState } from "react";
import { motion } from "motion/react";

interface TabItem {
  id: string;
  label: string;
  count?: number;
}

const TABS: TabItem[] = [
  { id: "overview", label: "Visão Geral" },
  { id: "analytics", label: "Métricas", count: 12 },
  { id: "deployments", label: "Deploys", count: 3 },
  { id: "settings", label: "Configurações" },
];

export function SlidingPillTabs() {
  const [activeTab, setActiveTab] = useState<string>("overview");

  return (
    <nav
      role="tablist"
      aria-label="Navegação do Projeto"
      className="inline-flex items-center gap-1 p-1.5 rounded-2xl bg-neutral-100 dark:bg-neutral-900 border border-neutral-200 dark:border-neutral-800"
    >
      {TABS.map((tab) => {
        const isActive = activeTab === tab.id;

        return (
          <button
            key={tab.id}
            role="tab"
            aria-selected={isActive}
            tabIndex={isActive ? 0 : -1}
            onClick={() => setActiveTab(tab.id)}
            className={`relative px-4 py-2 text-sm font-medium rounded-xl outline-none transition-colors duration-150 select-none ${
              isActive
                ? "text-neutral-900 dark:text-neutral-50"
                : "text-neutral-600 dark:text-neutral-400 hover:text-neutral-900 dark:hover:text-neutral-200 focus-visible:ring-2 focus-visible:ring-neutral-400"
            }`}
          >
            {/* Cápsula de Fundo que se Projeta Suavemente entre as Abas */}
            {isActive && (
              <motion.div
                layoutId="active-tab-indicator"
                className="absolute inset-0 rounded-xl bg-white dark:bg-neutral-800 shadow-sm border border-neutral-200/60 dark:border-neutral-700/60"
                transition={{
                  type: "spring",
                  stiffness: 380,
                  damping: 30,
                  mass: 0.8,
                }}
              />
            )}

            {/* Conteúdo da Aba com Camada Superior de Z-Index */}
            <span className="relative z-10 flex items-center gap-2">
              {tab.label}
              {tab.count !== undefined && (
                <span
                  className={`text-xs px-1.5 py-0.5 rounded-full transition-colors ${
                    isActive
                      ? "bg-neutral-100 text-neutral-800 dark:bg-neutral-700 dark:text-neutral-200 font-semibold"
                      : "bg-neutral-200/70 text-neutral-600 dark:bg-neutral-800 dark:text-neutral-400"
                  }`}
                >
                  {tab.count}
                </span>
              )}
            </span>
          </button>
        );
      })}
    </nav>
  );
}
```

---

#### Receita 2: Shared Element Card-to-Modal com Backdrop Blur e FLIP Projection

Uma implementação de nível de produção demonstrando a expansão contínua de um card da lista para modal em tela cheia, gerenciamento de tecla `Escape`, bloqueio de rolagem e preservação da nitidez tipográfica durante a escala geométrica:

```tsx
"use client";

import React, { useState, useEffect } from "react";
import { motion, AnimatePresence } from "motion/react";
import { X, ArrowRight } from "lucide-react";

interface ProjectCard {
  id: string;
  title: string;
  category: string;
  summary: string;
  description: string;
  accentColor: string;
}

const PROJECTS: ProjectCard[] = [
  {
    id: "proj-1",
    title: "Quantum Compiler",
    category: "Infraestrutura",
    summary: "Otimização de pipelines de compilação em arquitetura WebAssembly.",
    description: "Este projeto reconstrói o pipeline tradicional de empacotamento web utilizando compiladores vetorizados em Rust acoplados ao runtime do Motion para visualização analítica em 120fps sem interrupção de renderização.",
    accentColor: "from-blue-600 to-indigo-700",
  },
  {
    id: "proj-2",
    title: "Synapse Neural UI",
    category: "Inteligência Artificial",
    summary: "Interface conversacional autônoma de alta densidade informativa.",
    description: "Arquitetura de interface gráfica que conecta modelos de linguagem a ferramentas de execução em tempo real, integrando componentes colapsáveis com molas newtonianas e streaming contínuo de dados estruturados.",
    accentColor: "from-emerald-600 to-teal-800",
  },
];

export function ExpandableCardModal() {
  const [selectedId, setSelectedId] = useState<string | null>(null);

  // Fechamento com tecla Escape
  useEffect(() => {
    function handleKeyDown(event: KeyboardEvent) {
      if (event.key === "Escape") {
        setSelectedId(null);
      }
    }
    window.addEventListener("keydown", handleKeyDown);
    return () => window.removeEventListener("keydown", handleKeyDown);
  }, []);

  const activeCard = PROJECTS.find((p) => p.id === selectedId);

  return (
    <div className="w-full max-w-4xl mx-auto p-6">
      {/* Grid de Cards Compactos */}
      <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
        {PROJECTS.map((project) => (
          <motion.div
            key={project.id}
            layoutId={`card-container-${project.id}`}
            onClick={() => setSelectedId(project.id)}
            tabIndex={0}
            role="button"
            aria-haspopup="dialog"
            onKeyDown={(e) => e.key === "Enter" && setSelectedId(project.id)}
            className="group relative cursor-pointer overflow-hidden rounded-2xl bg-white dark:bg-neutral-900 border border-neutral-200 dark:border-neutral-800 p-6 shadow-sm hover:shadow-md transition-shadow outline-none focus-visible:ring-2 focus-visible:ring-blue-500"
            transition={{
              type: "spring",
              stiffness: 280,
              damping: 24,
            }}
          >
            {/* Banner Decorativo com layoutId */}
            <motion.div
              layoutId={`card-banner-${project.id}`}
              className={`h-24 w-full rounded-xl bg-gradient-to-r ${project.accentColor} mb-4 flex items-end p-4 text-white font-semibold text-sm`}
            >
              <motion.span layoutId={`card-category-${project.id}`}>
                {project.category}
              </motion.span>
            </motion.div>

            <motion.h3
              layoutId={`card-title-${project.id}`}
              className="text-lg font-bold text-neutral-900 dark:text-neutral-50 mb-2"
            >
              {project.title}
            </motion.h3>

            <motion.p
              layoutId={`card-summary-${project.id}`}
              className="text-sm text-neutral-600 dark:text-neutral-400 line-clamp-2"
            >
              {project.summary}
            </motion.p>

            <div className="mt-4 flex items-center gap-1.5 text-xs font-semibold text-blue-600 dark:text-blue-400 group-hover:translate-x-1 transition-transform">
              Ver detalhes <ArrowRight size={14} />
            </div>
          </motion.div>
        ))}
      </div>

      {/* Modal Expandido com Shared Layout Projection */}
      <AnimatePresence>
        {selectedId && activeCard && (
          <div className="fixed inset-0 z-50 flex items-center justify-center p-4 sm:p-6">
            {/* Backdrop Translúcido */}
            <motion.div
              initial={{ opacity: 0 }}
              animate={{ opacity: 1 }}
              exit={{ opacity: 0 }}
              transition={{ duration: 0.2 }}
              onClick={() => setSelectedId(null)}
              className="absolute inset-0 bg-neutral-950/60 backdrop-blur-md"
              aria-hidden="true"
            />

            {/* Container Centralizado do Modal Morphing */}
            <motion.div
              layoutId={`card-container-${activeCard.id}`}
              role="dialog"
              aria-modal="true"
              aria-labelledby={`card-title-${activeCard.id}`}
              className="relative z-10 w-full max-w-2xl overflow-hidden rounded-3xl bg-white dark:bg-neutral-900 border border-neutral-200 dark:border-neutral-800 shadow-2xl p-8"
              transition={{
                type: "spring",
                stiffness: 240,
                damping: 24,
                mass: 0.9,
              }}
            >
              {/* Botão de Fechar */}
              <button
                onClick={() => setSelectedId(null)}
                aria-label="Fechar modal"
                className="absolute top-6 right-6 p-2 rounded-full bg-neutral-100 dark:bg-neutral-800 text-neutral-600 dark:text-neutral-300 hover:bg-neutral-200 dark:hover:bg-neutral-700 transition-colors z-20 outline-none focus-visible:ring-2 focus-visible:ring-neutral-500"
              >
                <X size={18} />
              </button>

              {/* Banner Expandido */}
              <motion.div
                layoutId={`card-banner-${activeCard.id}`}
                className={`h-40 w-full rounded-2xl bg-gradient-to-r ${activeCard.accentColor} mb-6 flex items-end p-6 text-white font-semibold text-base shadow-inner`}
              >
                <motion.span layoutId={`card-category-${activeCard.id}`}>
                  {activeCard.category}
                </motion.span>
              </motion.div>

              <motion.h2
                layoutId={`card-title-${activeCard.id}`}
                className="text-2xl font-extrabold text-neutral-900 dark:text-neutral-50 mb-3"
              >
                {activeCard.title}
              </motion.h2>

              <motion.p
                layoutId={`card-summary-${activeCard.id}`}
                className="text-base text-neutral-700 dark:text-neutral-300 font-medium mb-4"
              >
                {activeCard.summary}
              </motion.p>

              {/* Conteúdo Detalhado Revelado */}
              <motion.div
                initial={{ opacity: 0, y: 15 }}
                animate={{ opacity: 1, y: 0 }}
                exit={{ opacity: 0, y: 10 }}
                transition={{ delay: 0.1, duration: 0.25 }}
                className="text-sm text-neutral-600 dark:text-neutral-400 leading-relaxed border-t border-neutral-100 dark:border-neutral-800 pt-4"
              >
                {activeCard.description}
              </motion.div>
            </motion.div>
          </div>
        )}
      </AnimatePresence>
    </div>
  );
}
```

---

#### Receita 3: Vanilla JS / Core WAAPI Scroll Timeline Off-Thread

Implementação ultraleve utilizando a API nativa universal `motion` (substituta e sucessora do Motion One), que roda animações sincronizadas com a rolagem do usuário diretamente no compositor da GPU sem acionar o motor de JavaScript:

```typescript
// Script Vanilla JS / TypeScript puro (import { animate, scroll } from "motion")
import { animate, scroll } from "motion";

export function initScrollIndicator(progressBarSelector: string, headerSelector: string) {
  const progressBar = document.querySelector<HTMLElement>(progressBarSelector);
  const header = document.querySelector<HTMLElement>(headerSelector);

  if (!progressBar || !header) return;

  // 1. Barra de Progresso de Leitura Superior vinculada ao Scroll da Página (100% Off-Thread WAAPI)
  scroll(
    animate(progressBar, {
      transform: ["scaleX(0)", "scaleX(1)"],
    }, {
      ease: "linear"
    })
  );

  // 2. Transição de Compactação e Blur do Header conforme o Scroll avança entre 0px e 150px
  scroll(
    animate(header, {
      backgroundColor: ["rgba(255, 255, 255, 0)", "rgba(255, 255, 255, 0.85)"],
      borderColor: ["rgba(229, 231, 235, 0)", "rgba(229, 231, 235, 1)"],
      backdropFilter: ["blur(0px)", "blur(12px)"],
      paddingTop: ["20px", "12px"],
      paddingBottom: ["20px", "12px"],
    }),
    {
      offset: ["0px", "150px"] // Intervalo estrito de scroll onde a transição opera
    }
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir o documento de especificação técnica e arquitetura de front-end (`DESIGN_BLUEPRINT.md`), a equipe de engenharia e os agentes de IA devem observar as seguintes diretrizes contratuais:

### 1. Declaração Formal da Tabela de Motion Tokens
O projeto não deve utilizar valores avulsos de molas ou easings declarados diretamente nos componentes. O blueprint deve padronizar a constante de tokens de física:

```typescript
// @/config/motion-tokens.ts
export const MOTION_TOKENS = {
  spring: {
    micro: { type: "spring", stiffness: 450, damping: 35, mass: 0.8 } as const,
    fluid: { type: "spring", stiffness: 300, damping: 28, mass: 1.0 } as const,
    gentle: { type: "spring", stiffness: 180, damping: 22, mass: 1.0 } as const,
    bouncy: { type: "spring", stiffness: 220, damping: 14, mass: 1.0 } as const,
  },
  timing: {
    instant: { duration: 0.08, ease: "easeOut" } as const,
    standard: { duration: 0.25, ease: [0.16, 1, 0.3, 1] } as const,
  },
  stagger: {
    dense: 0.035,
    normal: 0.05,
    relaxed: 0.08,
  },
} as const;
```

### 2. Mapeamento de Ilhas de Renderização (RSC vs Client Components)
- Componentes com `<motion.div>` exigem a diretiva `"use client"` no topo do arquivo no Next.js (App Router) e frameworks baseados em React Server Components.
- **Diretriz de Arquitetura**: Manter os layouts de página e estruturas de dados como Server Components (`page.tsx`), isolando as primitivas interativas do Motion em componentes folha focados (`SlidingTabs.tsx`, `ExpandableCard.tsx`) para manter o payload de hidratação JS mínimo.

### 3. Checklist Contratual de Auditoria Pré-Merge
Antes de aprovar qualquer componente que implemente animações com Motion, valide os 5 pontos de checagem:
- [ ] **Acessibilidade**: O componente consome `useReducedMotion()` e fornece uma variante estática ou de fade simples de 80ms quando ativado?
- [ ] **Ausência de Conflitos CSS**: Não existem classes `transition-*` do Tailwind concorrendo com as propriedades manipuladas pelo Motion no mesmo nó?
- [ ] **Integridade Geométrica**: Propriedades de `width`, `height`, `left` ou `top` não estão sendo interpoladas numericamente sem a prop `layout`?
- [ ] **Destruição Limpa**: Todos os elementos que saem do DOM estão aninhados sob `<AnimatePresence>` com chaves únicas (`key`) estáveis?
- [ ] **Teclado & Foco**: Transições de layout compartilhado (`layoutId`) mantêm a ordem visual coerente com a navegação sequencial via tecla `Tab`?
