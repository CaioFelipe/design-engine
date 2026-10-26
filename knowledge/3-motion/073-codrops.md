---
id: "codrops"
name: "Codrops (Tympanus)"
url: "https://tympanus.net/codrops/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["Experimental Creative Engineering", "FLIP Layout Morphing", "WebGL Shader Distortions", "Kinetic Typography & Text Reveal", "SVG Filter & Gooey Physics", "Interactive Cursor & Mouse Trails"]
densidade_informacao: "Independente"
impacto_visual: "Cinematografico/Showstopper"
custo_computacional: "Medio (JS RAF/Springs) a Alto (WebGL/GLSL/Three.js)"
stack_frameworks: ["Vanilla JavaScript / TypeScript", "GSAP (Flip, ScrollTrigger, SplitText)", "Three.js / WebGL / GLSL", "Lenis Smooth Scroll", "Curtains.js / OGL", "SVG Filters (feDisplacementMap, feColorMatrix)"]
compatibilidade:
  combinacoes_recomendadas: ["Codrops Patterns + Lenis Smooth Scroll", "Codrops WebGL Distortions + Three.js / R3F", "Codrops Layout Morphing + GSAP Flip", "Codrops Text Effects + SplitType / GSAP", "Tailwind CSS v4 + Motion.dev / Framer Motion"]
  conflitos_esteticos: ["Uso cumulativo de múltiplos efeitos showstopper na mesma viewport (sobrecarga sensorial)", "Scroll hijacking desregulador em sites e-commerce transacionais ou utilitários", "Falta de fallbacks para dispositivos sem GPU dedicada ou prefers-reduced-motion"]
---

# Codrops (Tympanus) — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)

O **Codrops** (`https://tympanus.net/codrops/`), fundado em 2009 por **Manoela Ilic** e **Pedro Botelho**, transcendeu o papel de um blog técnico convencional para se consagrar como o **epicentro global da Creative Technology** e o laboratório experimental mais influente da história do desenvolvimento front-end moderno. Com contribuições lendárias de pioneiros como **Yuri Artiukh (@akella)**, **Louis Hoebregts (@Mamboleoo)**, **Martin Laxenaire**, **Jesper Vos** e **Robin Delaporte**, o Codrops é a forja onde são concebidos, dissecados e documentados os padrões cinemáticos que definem a vanguarda dos prêmios Awwwards, FWA e Webby.

A filosofia do Codrops assenta-se na ruptura radical com a interface estática do documento web tradicional. O DOM não é tratado como uma folha bidimensional rígida de papel eletrônico, mas como um **ecossistema espacial tridimensional elástico, reativo e fluido**, onde a matéria digital possui inércia, refração luminosa, massa e tensão superficial.

---

### A Genealogia Técnica: De CSS3 Transforms a Shaders WebGL e FLIP

A evolução do ecossistema Codrops documenta as três eras da engenharia de interface experimental:

```
┌────────────────────────────────────────────────────────────────────────┐
│               EVOLUÇÃO HISTÓRICA DOS PARADIGMAS CODROPS                │
└────────────────────────────────────────────────────────────────────────┘

  [ERA 1: 2009 - 2014: O Despertar do CSS3 3D e Transições Geométricas]
    • Efeitos: 3D Book Open, Folded Paper Navigation, Cube Flips, Dropdown Sliders.
    • Motor: 'perspective', 'transform-style: preserve-3d', CSS @keyframes.
    • Limite: Ocorrência severa de aliasing, reflows por manipulação de top/left.

  [ERA 2: 2015 - 2019: SVG Filters, Liquid Morphing e GSAP Timelines]
    • Efeitos: Gooey Buttons, Organic Wave Page Transitions, Shape Morphing.
    • Motor: SVG <filter> ('feDisplacementMap', 'feColorMatrix'), Snap.svg, GSAP v2/v3.
    • Ganho: Descoberta da física de fluidos e transições elásticas vetoriais.

  [ERA 3: 2020 - PRESENTE: Shaders WebGL, FLIP Zero-Cost e Sincronia de Scroll]
    • Efeitos: RGB Split on Scroll, Grid-to-Fullscreen, Hover Trails, Fluid Canvas.
    • Motor: Three.js, Curtains.js, OGL, GLSL Shaders, GSAP Flip, Lenis Smooth Scroll.
    • Estado da Arte: Renderização híbrida (DOM para semântica/A11y + WebGL para deformação física).
```

---

### A Sensação Física (Feel): Continuidade Dimensional e Inércia Tátil

No vocabulário cinestésico do Codrops, cada micro-interação responde a princípios físicos bem determinados:

1. **Continuidade Dimensional (Spatial Coherence)**: Nenhum elemento simplesmente desaparece ou surge do vazio. Um card em uma grade de catálogo não "troca de página" para a visualização detalhada; ele se distorce, descola de sua órbita local via técnica FLIP e expande suas bordas para ocupar o viewport, mantendo o cérebro do usuário orientado no espaço tridimensional da aplicação.
2. **Inércia Viscosa (Viscous Fluid Drag)**: O cursor do mouse deixa de ser uma seta estática do sistema operacional para se tornar uma força perturbadora de um campo gravitacional ou fluido. Imagens em hover sofrem arrasto (*drag*), distorção por ondas de calor (*heat ripples*) ou deslocamento de canais RGB proporcionais à velocidade escalar do ponteiro.
3. **Massa e Amortecimento Elástico (Critically Damped Springs)**: Botões magnéticos e imagens em rastro (*trail*) nunca se deslocam em velocidade linear. Eles são regidos por equações de LERP (*Linear Interpolation*) ou sistemas massa-mola com amortecimento crítico, simulando a sensação de arrastar um objeto sólido imerso em mel ou glicerina.

---

### Arquitetura de Pipeline Visual Codrops: O Modelo Híbrido DOM + Canvas

Um dos maiores legados arquiteturais do Codrops é a **projeção e espelhamento entre o DOM HTML e o Canvas WebGL**:

```
┌──────────────────────────────────────────────────────────────────────────┐
│             PIPELINE HÍBRIDO CODROPS: SINCRONIZAÇÃO DOM ↔ GLSL           │
└──────────────────────────────────────────────────────────────────────────┘

 [HTML/CSS SEMÂNTICO]                    [MOTOR DE CONTROLE]
  • <img>, <article>, <h2>                • Lenis (Normalized Virtual Scroll)
  • Bounding Client Rects nativos         • GSAP Ticker / requestAnimationFrame
  • Acessibilidade WCAG preservada        • Event Listeners (Pointer, Scroll)
         │                                        │
         │ getBoundingClientRect()                │ Delta Y, Mouse (X, Y)
         ▼                                        ▼
 ┌────────────────────────────────────────────────────────────────────────┐
 │                     CAMADA DE TRADUÇÃO CODROPS                         │
 │   • Converte pixels DOM (Top, Left, Width, Height) em coordenadas 3D   │
 │     World Coordinates da câmera Three.js / OGL (Mesh Plane sync).      │
 │   • Atualiza uniforms: 'uScrollSpeed', 'uMouseVelocity', 'uProgress'   │
 └────────────────────────────────────────────────────────────────────────┘
                                 │
                                 ▼
 [VERTEX SHADER (GLSL)]                     [FRAGMENT SHADER (GLSL)]
  • Deforma a malha do plano com             • Aplica RGB Split e distorção
    base na velocidade do scroll:              baseada em ruído Simplex/Perlin:
    pos.y += sin(uv.x * 3.14) * uVelocity      color.r = texture2D(uv + offset)
                                 │
                                 ▼
                     [WEBGL CANVAS TELA CHEIA]
             Renderização fluida a 60fps / 120fps sobreposta
             com transparência de fundo ('pointer-events: none')
```

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Interface e Casos de Uso Críticos

1. **Hero Sections de Alto Impacto para Marcas de Vanguarda e Moda**:
   Lookbooks interativos, lançamentos automotivos, agências de publicidade e estúdios de design onde o usuário precisa ser imediatamente capturado por uma experiência sensorial memorável e imersiva.
2. **Galerias de Portfólio e Casos de Estudo (Grid-to-Fullscreen)**:
   Transição contínua entre a miniatura do projeto na listagem geral e o artigo completo em tela cheia, eliminando completamente telas em branco de carregamento e saltos visuais bruscos.
3. **Call-to-Actions (CTAs) Magnéticos e Micro-Interações de Prestígio**:
   Botões flutuantes que gravitam em direção ao cursor quando o ponteiro se aproxima em um raio de 100px, acompanhados por distorções elásticas em SVG ou shaders de plasma no preenchimento.
4. **Scrollytelling Editorial e Apresentações de Produto Interativas**:
   Narrativas onde o scroll não desloca simplesmente blocos de texto para cima, mas aciona montagens cinemáticas: desmontagem em camadas (*exploded view*), expansão de cartões em perspectiva 3D e distorções líquidas nas transições de imagem.
5. **Rastros Interativos de Cursor (Hover Image Trails)**:
   Em páginas de índice editorial, o movimento rápido do mouse sobre títulos de matérias invoca um rastro efêmero de 5 a 10 imagens que flutuam e se dissipam com rotação dinâmica, fornecendo um *preview* visual instantâneo e orgânico do conteúdo.

---

### A Regra 60-30-10 no Design System com Padrões Codrops

A incorporação das técnicas do Codrops em um produto comercial maduro exige equilíbrio cirúrgico para não converter a interface em um caos visual inutilizável:

```
┌────────────────────────────────────────────────────────────────────────┐
│                   A REGRA 60-30-10 COM EFEITOS CODROPS                 │
└────────────────────────────────────────────────────────────────────────┘

  [60% - FUNDAÇÃO E LEITURA: ESTRUTURA NEUTRA]
  • Tipografia limpa, hierarquia sólida, espaçamentos generosos (Tailwind).
  • Fundos de alto contraste (#0B0C10, #0F172A ou off-whites editoriais).
  • Layouts estáveis sem movimento perpétuo ou interferência na legibilidade.

  [30% - CINÉTICA DE FEEL: MICRO-MOVIMENTOS INVISÍVEIS]
  • Lenis Smooth Scroll com inércia sedosa e normalizada.
  • Kinetic text reveals graduais em entradas de viewport.
  • Hover states suaves com LERP de amortecimento elástico (0.1 lerp rate).
  • Transições de abas e accordions orquestradas sem trancos.

  [10% - SHOWSTOPPER CODROPS: O CLÍMAX VISUAL E MARCA DA APLICAÇÃO]
  • APENAS UM padrão épico por jornada principal:
    - OU uma distorção WebGL com RGB split na rolagem das imagens hero;
    - OU a transição Grid-to-Fullscreen via GSAP Flip no portfólio;
    - OU o cursor com rastro de imagens (Hover Trail) na navegação principal;
    - OU um botão de ação com fusão líquida via SVG feDisplacementMap.
```

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Quando Evitar Absolutamente

1. **Aplicações Transacionais Densas, Dashboards Analíticos e SaaS B2B**:
   Em ferramentas de gestão financeira, planilhas colaborativas, painéis hospitalares ou interfaces de CRM, animações com atraso elástico (*spring latency*) e distorções de texto induzem frustração cognitiva extrema e lentidão operacional.
2. **Páginas de Checkout, Pagamento e Formulários Críticos**:
   Distorções de tela, rastros visuais ou botões que se movem magneticamente podem fazer o usuário errar cliques em campos de cartão de crédito ou termos legais, gerando abandono de carrinho.
3. **Dispositivos Móveis de Entrada e Dispositivos com Bateria Restrita**:
   Shaders WebGL rodando continuamente no loop de `requestAnimationFrame` forçam a GPU do dispositivo a operar em frequências elevadas, causando estrangulamento térmico (*thermal throttling*), queda drástica de framerate e drenagem acelerada da bateria.

---

### ⚠️ Acessibilidade & Cinetose (Prefers-Reduced-Motion)

A cinetose vestibular (*vestibular disorders*) pode ser desencadeada por distorções de onda, parallax excessivo e rastros visuais contínuos. É mandatório implementar fallback estrutural:

```javascript
// Verificação de acessibilidade nativa
const prefersReducedMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;

if (prefersReducedMotion) {
  // 1. Desativar shaders WebGL de deformação e renderizar <img> padrão
  // 2. Desativar rastro de imagens e cursor magnético
  // 3. Substituir FLIP de transição complexa por fade-in simples de 200ms
  // 4. Manter scroll 100% nativo instantâneo
}
```

---

### ⚠️ Gestão Crítica de Recursos de GPU, Memory Leaks e RAF

1. **Vazamento de Memória por Contextos WebGL Órfãos**:
   Em Single Page Applications (Next.js, Remix, Vue), ao navegar entre rotas, componentes com `<canvas>` Three.js devem obrigatoriamente chamar:
   ```javascript
   renderer.dispose();
   geometry.dispose();
   material.dispose();
   texture.dispose();
   scene.clear();
   ```
   Caso contrário, o navegador atinge o limite do hardware (geralmente 8 a 16 contextos ativos) e quebra com `CONTEXT_LOST_WEBGL`.
2. **Draw Calls e Criação de Objetos no Loop RAF**:
   Nunca instancie vetores (`new THREE.Vector2()`), matrizes ou arrays dentro do loop de animação. Crie-os fora como variáveis globais estáticas para evitar coletas de lixo (*garbage collection spikes*) que causam travamentos perceptíveis de 10-50ms.
3. **Resize Observer sem Throttling**:
   Recalcular `getBoundingClientRect()` a cada pixel de redimensionamento causa reflow forçado (*layout thrashing*). Utilize `ResizeObserver` com debounce de no mínimo 100ms.

---

## 4. Catálogo Detalhado de Efeitos, Primitivas e Padrões de Animação

Abaixo estão os 10 padrões mais representativos, icônicos e reverenciados publicados e disseminados pelo Codrops:

---

### 1. Grid-to-Fullscreen Morphing (GSAP Flip Plugin)
- **Comportamento Visual**: Uma miniatura estática de imagem em um grid de 3 ou 4 colunas é clicada. O item se descola suavemente da malha do layout, flutua sobre as demais camadas com z-index elevado e expande suas dimensões físicas e proporções até ocupar 100vw e 100vh. Simultaneamente, o título do projeto migra da base do card para o topo do hero da nova visualização. Ao fechar, o processo reverso reconduz o elemento exatamente para seu receptáculo original no grid.
- **Mecanismo Técnico**: Técnica FLIP (*First, Last, Invert, Play*). Captura a geometria inicial via `getBoundingClientRect()`, posiciona o elemento no estado final no DOM, calcula a diferença escalar e posicional via `matrix3d` e anima apenas `transform` e `clip-path`, garantindo 60fps sem acionar recalculo de layout (*reflow*).
- **Gatilho**: Evento de clique (`click` / `pointerup`) no card da galeria.
- **Onde Encaixar**: Galerias de projetos em portfólios, cards de produtos em catálogos de moda de alta costura, cases de arquitetura.

---

### 2. WebGL Scroll Velocity Distortion & RGB Split (Akella Shader Pattern)
- **Comportamento Visual**: Quando o usuário rola a página rapidamente, todas as imagens do layout sofrem uma curvatura elástica de arco (como se fossem placas de borracha gelatinosa sob aceleração violenta) e suas bordas cromáticas se dividem nos canais Vermelho, Verde e Azul (aberração cromática / RGB split). No instante em que o scroll cessa, as imagens relaxam organicamente de volta à sua forma ortogonal perfeitamente nítida.
- **Mecanismo Técnico**: Projeção de um plano 3D no Three.js sincronizado geometricamente com o elemento HTML `<img>`. O vetor de velocidade do scroll (`deltaY / deltaTime`) é passado como uniforme `uVelocity` para o Vertex Shader (para curvar vértices via onda senoidal) e para o Fragment Shader (para deslocar os canais R e B em vetores opostos de UV).
- **Gatilho**: Movimento contínuo de rolagem (`scroll` normalizado via Lenis).
- **Onde Encaixar**: Seções de apresentação de produtos tecnológicos, sites de design visual, páginas de lançamento com alta carga visual.

---

### 3. Interactive Mouse Image Trail (Hover Cursor Trail Buffer)
- **Comportamento Visual**: Ao deslocar o ponteiro do mouse livremente pela tela ou sobre uma lista tipográfica de navegação, uma sucessão fluida de fotografias e tipografias surge logo atrás do cursor, como se fossem pétalas ou cartas de baralho sendo depositadas em tempo real. Cada imagem nasce com escala reduzida, atinge tamanho pleno com uma leve inclinação angular randômica correspondente à direção do vetor de movimento do mouse, e desvanece suavemente por rotação e opacidade após 600ms.
- **Mecanismo Técnico**: Fila circular (*pool*) de 10 a 20 nós DOM com posicionamento absoluto. O script mede a distância euclidiana entre a posição atual do ponteiro e a última imagem gerada. Se `hypot(dx, dy) > threshold` (ex: 80px), o próximo nó do pool é ativado na coordenada atual e animado via GSAP Timeline com curva `expo.out`.
- **Gatilho**: Movimento contínuo do ponteiro (`pointermove`).
- **Onde Encaixar**: Hero sections interativas de fotógrafos e artistas, menus editoriais minimalistas onde passar o mouse sobre o título revela os ensaios visuais.

---

### 4. Liquid Gooey Button & SVG Filter Turbulence
- **Comportamento Visual**: Um botão de call-to-action repousa com contornos aparentemente sólidos. Ao aproximar o cursor, a silhueta externa do botão emite filamentos líquidos e gotas orgânicas que se esticam, se separam e retornam à massa principal como gotas de mercúrio ou lava vulcânica. Ao clicar, uma bolha de choque percorre a superfície elástica do botão.
- **Mecanismo Técnico**: Filtro SVG embutido na página combinando `<feGaussianBlur stdDeviation="10">` com `<feColorMatrix type="matrix" values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 19 -9">`. O filtro esmaga os valores de canal alfa, fazendo com que dois elementos circulares adjacentes com blur compartilhem um menisco de atração física antes de se desconectarem.
- **Gatilho**: Proximidade e hover do mouse (`pointerenter`, `pointermove`).
- **Onde Encaixar**: Botões primários de chamada para ação em sites criativos, botões de reprodução de showreels de vídeo.

---

### 5. Kinetic Typography 3D Perspective Reveal (SplitText Stagger)
- **Comportamento Visual**: Títulos monumentais e frases de manifesto não entram em cena com fade tradicional. Cada linha ou glifo tipográfico é fragmentado e surge rotacionando a partir de um eixo 3D a 90 graus negativos no plano X, saindo de trás de uma máscara de recorte invisível, como placas de sinalização mecânica se desdobrando no espaço com ligeiro atraso (*stagger*) entre palavras.
- **Mecanismo Técnico**: Decomposição do texto em `<span>` com wrappers de máscara utilizando `overflow: hidden`. As letras recebem `transform: rotateX(-90deg) translate3d(0, 100%, 0)` com ponto de ancoragem no topo (`transform-origin: 50% 0%`). A interpolação de retorno ao repouso é orientada por uma curva de amortecimento acentuada `power4.out`.
- **Gatilho**: Disparo por interseção de scroll (`IntersectionObserver` ou `ScrollTrigger.create`).
- **Onde Encaixar**: Títulos H1 de hero sections, declarações de missão de marcas e separadores de capítulos em narrativas digitais.

---

### 6. Directional Image Hover Ripple & Heat Distortion (GLSL Shader)
- **Comportamento Visual**: Ao repousar o mouse sobre uma foto e movimentá-lo internamente, a imagem comporta-se como a superfície de uma piscina límpida tocada por uma gota: ondas circulares concêntricas ou refrações térmicas emanam exatamente da ponta do cursor, distorcendo a imagem por baixo e refratando o conteúdo subjacente.
- **Mecanismo Técnico**: Fragment shader aplicando ruído simplex 2D ou mapas de deslocamento pré-calculados. O mouse passa coordenadas UV normalizadas `(uMouse.x, uMouse.y)` e um contador de tempo `uTime`. O shader calcula a distância euclidiana da coordenada UV atual em relação ao mouse e adiciona uma perturbação senoidal decrescente à amostragem de textura.
- **Gatilho**: Posicionamento e movimentação interna do mouse (`pointermove` local).
- **Onde Encaixar**: Banners de campanhas de moda, interfaces de exposições artísticas virtuais, capas de álbuns musicais.

---

### 7. Multiplane Smooth Parallax Scrub (Lenis + ScrollTrigger)
- **Comportamento Visual**: Diferentes camadas de um layout editorial (fotos panorâmicas ao fundo, cartões flutuantes no meio e tipografias monumentais em primeiro plano) deslocam-se verticalmente a velocidades relativas diferenciadas (ex: 0.8x, 1.0x, 1.4x), criando uma sensação tátil de profundidade de campo estéreo durante a rolagem.
- **Mecanismo Técnico**: Sincronização do motor de rolagem suave Lenis com o `gsap.ticker`. O `ScrollTrigger` utiliza parâmetros de amortecimento `scrub: 1` e valores `yPercent` calculados para não estourar a aceleração de hardware. Elementos utilizam `will-change: transform`.
- **Gatilho**: Rolagem da página acoplada ao eixo vertical (`window.scrollY`).
- **Onde Encaixar**: Páginas institucionais de storytelling, apresentações de portfólio de arquitetura e estúdios de arte.

---

### 8. Magnetic Element & Elastic Cursor Follower
- **Comportamento Visual**: O cursor do mouse é substituído ou acompanhado por um anel minimalista flutuante. Quando o ponteiro entra em uma zona de proximidade de 80px ao redor de um botão, link ou tag, o botão é suavemente sugado na direção do mouse como ferro atraído por um ímã neodímio. O anel do cursor expande-se, assumindo a geometria exata do botão e encapsulando-o com tensão elástica.
- **Mecanismo Técnico**: Cálculo de vetor diferencial `(dx, dy)` entre o centro do elemento e a posição do ponteiro. O elemento HTML sofre `translate3d(dx * strength, dy * strength, 0)` interpolado via LERP `lerp(curr, target, 0.15)`. Ao sair da zona de captura, o elemento oscila brevemente de volta à origem via mola física amortecida.
- **Gatilho**: Proximidade de ponteiro (`pointermove` global com cálculo de raio).
- **Onde Encaixar**: Botões de navegação, seletores de idioma, botões de ação flutuantes e links de menu primários.

---

### 9. Infinite Horizontal Draggable WebGL Canvas
- **Comportamento Visual**: Um carrossel horizontal infinito que responde tanto ao arrasto direto do ponteiro/touchpad quanto à rolagem do mouse. As imagens movem-se horizontalmente, mas quando puxadas com ímpeto, dobram-se em um arco cilíndrico côncavo ou convexo no espaço 3D, simulando uma fita física de filme ou carrossel de diapositivos.
- **Mecanismo Técnico**: Criação de planos instanciados ou geometria repetida em Three.js. Quando o índice ultrapassa os limites do viewport, os planos são reposicionados matematicamente na outra extremidade através de aritmética modular (`modulo`). A deformação cilíndrica é processada no Vertex Shader pela equação `position.z = cos(position.x * curvature) * factor`.
- **Gatilho**: Arrasto do usuário (`pointerdown`, `pointermove`, `pointerup`) ou roda do mouse.
- **Onde Encaixar**: Galerias de projetos em tela cheia, mostruários de filmes ou coleções de produtos.

---

### 10. Organic SVG Path Curved Curtain Page Transition
- **Comportamento Visual**: Ao mudar de página ou abrir um modal de tela cheia, uma cortina visual não desce em linha reta rígida. Ela desce como uma onda fluida ou lâmina côncava e elástica: a parte inferior da cortina forma uma curva Bezier convexa dramática que oscila e depois se estica até preencher a tela, revelando o novo layout como um pano de teatro que ondula sob a brisa.
- **Mecanismo Técnico**: Manipulação animada da string `d` de um elemento SVG `<path>`. O caminho utiliza pontos de controle cúbicos `M 0 0 L 100 0 L 100 100 Q 50 150 0 100 Z`. A coordenada Y do ponto de controle central `Q` é animada via timeline GSAP com curva `power2.inOut` ou oscilador elástico.
- **Gatilho**: Evento de transição de rota ou clique em link de navegação.
- **Onde Encaixar**: Transições globais de página em sites institucionais, aberturas de gavetas de navegação (*navigation drawers*).

---

## 5. Matemática do Movimento & Receitas de Código

### 5.1 Fórmulas Matemáticas, Curvas Bezier e Interpolações Físicas

#### 1. A Equação do LERP (Linear Interpolation) com Compensação de Framerate
Toda movimentação orgânica de cursor, inércia de scroll ou câmera WebGL no padrão Codrops depende da interpolação linear entre o estado atual e o estado pretendido:

$$\text{current} = \text{current} + (\text{target} - \text{current}) \times \alpha$$

Onde $\alpha$ representa o fator de amortecimento (tipicamente entre $0.05$ e $0.2$). Para garantir que a suavidade seja idêntica em telas de 60Hz, 120Hz ou 240Hz, deve-se aplicar compensação por delta temporal:

$$\alpha_{\text{adjusted}} = 1 - (1 - \alpha)^{\Delta t \times 60}$$

#### 2. Curvas Bézier Cúbicas de Assinatura Codrops
- **Snappy Dynamic Out (Expo)**: `cubic-bezier(0.19, 1, 0.22, 1)` — Arrancada explosiva imediata e desaceleração extremamente longa e elegante. Ideal para modais e text reveals.
- **Cinematic Ease-in-Out (Power4)**: `cubic-bezier(0.77, 0, 0.175, 1)` — Transição cinematográfica para movimentos de página e layouts morphing.
- **Fluid Spring Snap**: `cubic-bezier(0.34, 1.56, 0.64, 1)` — Micro-overshoot elástico natural para ícones e botões magnéticos.

---

### 5.2 Receita 1: WebGL Scroll Distortion & RGB Split Shader (Three.js + GLSL)

Esta receita reproduz o clássico padrão Codrops (tornado célebre por Yuri Artiukh), onde planos Three.js espelham imagens HTML e sofrem distorção senoidal e aberração cromática proporcional à velocidade de rolagem:

```javascript
// WebGLScrollScene.js
import * as THREE from 'three';
import Lenis from 'lenis';

export class WebGLScrollScene {
  constructor(container, images) {
    this.container = container;
    this.images = images;
    this.planes = [];
    this.scroll = { current: 0, target: 0, velocity: 0 };
    
    this.initLenis();
    this.initThree();
    this.createMeshPlanes();
    this.addEvents();
    this.render();
  }

  initLenis() {
    this.lenis = new Lenis({ lerp: 0.1, smoothWheel: true });
    this.lenis.on('scroll', (e) => {
      this.scroll.velocity = e.velocity * 0.005; // Normaliza velocidade escalar
    });
  }

  initThree() {
    this.scene = new THREE.Scene();
    this.camera = new THREE.PerspectiveCamera(
      45,
      window.innerWidth / window.innerHeight,
      1,
      1000
    );
    // Ajusta z da câmera para que 1 unidade Three.js = 1 pixel DOM na tela
    this.camera.position.z = 600;
    this.camera.fov = 2 * Math.atan((window.innerHeight / 2) / 600) * (180 / Math.PI);
    this.camera.updateProjectionMatrix();

    this.renderer = new THREE.WebGLRenderer({ alpha: true, antialias: true, powerPreference: 'high-performance' });
    this.renderer.setSize(window.innerWidth, window.innerHeight);
    this.renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
    this.container.appendChild(this.renderer.domElement);
  }

  createMeshPlanes() {
    // Vertex Shader: Curvatura dos vértices baseada em velocidade
    const vertexShader = `
      uniform float uVelocity;
      varying vec2 vUv;
      void main() {
        vUv = uv;
        vec3 pos = position;
        // Deformação em arco senoidal ao longo da coordenada X
        pos.y += sin(uv.x * 3.141592) * uVelocity * 25.0;
        gl_Position = projectionMatrix * modelViewMatrix * vec4(pos, 1.0);
      }
    `;

    // Fragment Shader: Amostragem de canais RGB separados (Aberração Cromática)
    const fragmentShader = `
      uniform sampler2D uTexture;
      uniform float uVelocity;
      varying vec2 vUv;
      void main() {
        vec2 uv = vUv;
        // Deslocamento dos canais R e B proporcional à velocidade
        float r = texture2D(uTexture, uv + vec2(0.0, uVelocity * 0.04)).r;
        float g = texture2D(uTexture, uv).g;
        float b = texture2D(uTexture, uv - vec2(0.0, uVelocity * 0.04)).b;
        gl_FragColor = vec4(r, g, b, 1.0);
      }
    `;

    const textureLoader = new THREE.TextureLoader();

    this.images.forEach((img) => {
      const bounds = img.getBoundingClientRect();
      const texture = textureLoader.load(img.src);
      const geometry = new THREE.PlaneGeometry(bounds.width, bounds.height, 32, 32);

      const material = new THREE.ShaderMaterial({
        vertexShader,
        fragmentShader,
        uniforms: {
          uTexture: { value: texture },
          uVelocity: { value: 0.0 }
        },
        transparent: true
      });

      const mesh = new THREE.Mesh(geometry, material);
      this.scene.add(mesh);

      this.planes.push({ mesh, element: img, bounds });
      // Oculta imagem nativa do DOM preservando acessibilidade visual para SEO/Screen Readers
      img.style.opacity = '0';
    });
  }

  updatePlanesPositions() {
    this.planes.forEach(({ mesh, element }) => {
      const bounds = element.getBoundingClientRect();
      // Converte coordenadas do DOM (top-left) para sistema Three.js (centro da tela 0,0)
      mesh.position.x = bounds.left - window.innerWidth / 2 + bounds.width / 2;
      mesh.position.y = -bounds.top + window.innerHeight / 2 - bounds.height / 2;
      mesh.material.uniforms.uVelocity.value = this.scroll.velocity;
    });
  }

  render(time) {
    this.lenis.raf(time);
    // Dissipação suave da velocidade por LERP
    this.scroll.velocity += (0 - this.scroll.velocity) * 0.1;
    this.updatePlanesPositions();
    this.renderer.render(this.scene, this.camera);
    requestAnimationFrame(this.render.bind(this));
  }

  addEvents() {
    window.addEventListener('resize', () => {
      this.renderer.setSize(window.innerWidth, window.innerHeight);
      this.camera.aspect = window.innerWidth / window.innerHeight;
      this.camera.fov = 2 * Math.atan((window.innerHeight / 2) / 600) * (180 / Math.PI);
      this.camera.updateProjectionMatrix();
    });
  }
}
```

---

### 5.3 Receita 2: GSAP Flip Grid-to-Fullscreen Layout Transition (React + TypeScript)

Implementação ultra-performática da transição de galeria em tela cheia utilizando a biblioteca oficial **GSAP Flip Plugin**:

```tsx
import React, { useRef, useState } from 'react';
import gsap from 'gsap';
import { Flip } from 'gsap/Flip';

gsap.registerPlugin(Flip);

interface ItemData {
  id: string;
  title: string;
  category: string;
  imageUrl: string;
}

const ITEMS: ItemData[] = [
  { id: '1', title: 'Kinetic Architecture', category: 'Spatial Design', imageUrl: 'https://images.unsplash.com/photo-1513694203232-719a280e022f?q=80&w=1200' },
  { id: '2', title: 'Chromodynamics', category: 'Creative Coding', imageUrl: 'https://images.unsplash.com/photo-1541701494587-cb58502866ab?q=80&w=1200' },
  { id: '3', title: 'Fluid Ergonomics', category: 'Physical UI', imageUrl: 'https://images.unsplash.com/photo-1508739773434-c26b3d09e071?q=80&w=1200' }
];

export const CodropsGridToFullscreen: React.FC = () => {
  const [activeItem, setActiveItem] = useState<ItemData | null>(null);
  const containerRef = useRef<HTMLDivElement>(null);

  const handleCardClick = (item: ItemData, targetElement: HTMLElement) => {
    // 1. Grava estado FIRST de todos os elementos rastreados
    const state = Flip.getState('.flip-item, .flip-title, .flip-img');

    // 2. Altera o estado do React
    setActiveItem(item);

    // 3. Executa a transição física no próximo ciclo de renderização
    requestAnimationFrame(() => {
      Flip.from(state, {
        duration: 0.9,
        ease: 'power4.inOut',
        absolute: true,
        nested: true,
        onComplete: () => {
          gsap.fromTo('.detail-description', { opacity: 0, y: 20 }, { opacity: 1, y: 0, duration: 0.4 });
        }
      });
    });
  };

  const handleClose = () => {
    const state = Flip.getState('.flip-item, .flip-title, .flip-img');
    setActiveItem(null);

    requestAnimationFrame(() => {
      Flip.from(state, {
        duration: 0.8,
        ease: 'power3.inOut',
        absolute: true,
        nested: true
      });
    });
  };

  return (
    <div ref={containerRef} className="relative min-h-screen bg-[#0d0f12] text-white p-8 overflow-hidden">
      {/* Visualização em Grid */}
      {!activeItem && (
        <div className="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-6xl mx-auto mt-20">
          {ITEMS.map((item) => (
            <div
              key={item.id}
              data-flip-id={`card-${item.id}`}
              onClick={(e) => handleCardClick(item, e.currentTarget)}
              className="flip-item group relative h-[420px] rounded-2xl overflow-hidden cursor-pointer bg-[#181b20] border border-white/10"
            >
              <img
                data-flip-id={`img-${item.id}`}
                src={item.imageUrl}
                alt={item.title}
                className="flip-img absolute inset-0 w-full h-full object-cover transition-transform duration-700 group-hover:scale-105"
              />
              <div className="absolute inset-0 bg-gradient-to-t from-black/80 via-transparent to-transparent" />
              <div className="absolute bottom-6 left-6 right-6">
                <span className="text-xs uppercase tracking-widest text-emerald-400 font-mono">{item.category}</span>
                <h3 data-flip-id={`title-${item.id}`} className="flip-title text-2xl font-semibold mt-1">
                  {item.title}
                </h3>
              </div>
            </div>
          ))}
        </div>
      )}

      {/* Visualização em Fullscreen Detail */}
      {activeItem && (
        <div
          data-flip-id={`card-${activeItem.id}`}
          className="flip-item fixed inset-0 z-50 flex flex-col justify-between p-12 bg-[#0d0f12]"
        >
          <button
            onClick={handleClose}
            className="self-end z-10 px-5 py-2.5 rounded-full bg-white/10 backdrop-blur-md border border-white/20 hover:bg-white/20 transition-colors text-sm font-medium"
          >
            Fechar [ESC]
          </button>
          
          <div className="absolute inset-0 z-0">
            <img
              data-flip-id={`img-${activeItem.id}`}
              src={activeItem.imageUrl}
              alt={activeItem.title}
              className="flip-img w-full h-full object-cover opacity-60"
            />
            <div className="absolute inset-0 bg-gradient-to-t from-[#0d0f12] via-[#0d0f12]/40 to-transparent" />
          </div>

          <div className="relative z-10 max-w-4xl mt-auto">
            <span className="text-sm uppercase tracking-widest text-emerald-400 font-mono">{activeItem.category}</span>
            <h1 data-flip-id={`title-${activeItem.id}`} className="flip-title text-5xl md:text-7xl font-bold tracking-tight mt-2">
              {activeItem.title}
            </h1>
            <p className="detail-description mt-6 text-lg text-white/70 max-w-2xl leading-relaxed">
              Exploração sensorial de interface inspirada nas publicações canônicas do laboratório Tympanus Codrops. Geometria contínua, interpolação de matrizes e zero reflow no thread principal.
            </p>
          </div>
        </div>
      )}
    </div>
  );
};
```

---

### 5.4 Receita 3: SVG Filter Liquid Gooey Morphing Button (HTML + CSS Moderno)

O lendário efeito de fusão líquida Codrops implementado com zero dependências externas via SVG Filter nativo:

```html
<!-- SVG Filter oculto que esmaga o canal Alpha para gerar o efeito de mercúrio líquido -->
<svg class="gooey-filter-def" xmlns="http://www.w3.org/2000/svg" version="1.1" style="display: none;">
  <defs>
    <filter id="gooey-morph">
      <feGaussianBlur in="SourceGraphic" stdDeviation="10" result="blur" />
      <feColorMatrix
        in="blur"
        type="matrix"
        values="1 0 0 0 0  
                0 1 0 0 0  
                0 0 1 0 0  
                0 0 0 20 -10"
        result="goo"
      />
      <feBlend in="SourceGraphic" in2="goo" />
    </filter>
  </defs>
</svg>

<div class="gooey-button-wrapper">
  <button class="gooey-btn">
    <span class="btn-text">Iniciar Experiência</span>
    <!-- Blobs orgânicos flutuantes renderizados sob o filtro -->
    <span class="blob blob-1"></span>
    <span class="blob blob-2"></span>
    <span class="blob blob-3"></span>
  </button>
</div>

<style>
  .gooey-button-wrapper {
    position: relative;
    filter: url('#gooey-morph'); /* Aplicação do filtro sobre o contêiner */
  }

  .gooey-btn {
    position: relative;
    padding: 1.2rem 2.8rem;
    font-size: 1rem;
    font-weight: 600;
    color: #ffffff;
    background-color: #6366f1;
    border: none;
    border-radius: 9999px;
    cursor: pointer;
    outline: none;
    transition: transform 0.2s cubic-bezier(0.34, 1.56, 0.64, 1);
  }

  .gooey-btn:hover {
    transform: scale(1.05);
  }

  .btn-text {
    position: relative;
    z-index: 2;
  }

  .blob {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 32px;
    height: 32px;
    background-color: #6366f1;
    border-radius: 50%;
    transform: translate(-50%, -50%);
    pointer-events: none;
    transition: transform 0.5s cubic-bezier(0.19, 1, 0.22, 1);
  }

  /* Na aproximação do cursor, os blobs se esticam para fora criando o menisco líquido */
  .gooey-btn:hover .blob-1 {
    transform: translate(-90px, -45px) scale(1.3);
  }
  .gooey-btn:hover .blob-2 {
    transform: translate(75px, -40px) scale(1.2);
  }
  .gooey-btn:hover .blob-3 {
    transform: translate(10px, 35px) scale(1.4);
  }
</style>
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao arquitetar projetos que utilizam técnicas experimentais do Codrops, a Inteligência Artificial e a equipe de engenharia devem formalizar as seguintes decisões técnicas no `DESIGN_BLUEPRINT.md`:

```markdown
### 1. Motion & Creative Tech Blueprint (Codrops Specification)

- **Padrão Selecionado**: [Ex: Grid-to-Fullscreen via GSAP Flip | WebGL Velocity RGB Split | Hover Image Trail]
- **Camada Tecnológica**:
  - DOM Semântico: Tailwind CSS v4 + Acessibilidade WCAG 2.1 AA.
  - Orquestração de Física: [Lenis + GSAP 3.12+ | Three.js WebGL Renderer].
  - Shaders Ativos: Vertex Shader (Curvatura em arco) + Fragment Shader (RGB Aberration).
- **Taxa de Amostragem & Framerate Alvo**: 60fps mínimo / 120fps ótimo em monitores ProMotion.
- **Estratégia de Alocação de Memória GPU**:
  - Textura única atlas ou dimensões máximas de 2048x2048px (WebP).
  - Descarte obrigatório de geometrias, texturas e materiais em desmontagem de rotas SPA.
- **Acessibilidade e Fallback**:
  - Detecção imediata de `@media (prefers-reduced-motion: reduce)`.
  - Fallback móvel: desativar shader de tela cheia e aplicar `transition: opacity 0.3s ease`.
```

### Checklist de Auditoria Técnica e Performance Pré-Deploy

| Item de Verificação | Critério de Aceitação | Ação se Falhar |
| :--- | :--- | :--- |
| **Cumulative Layout Shift (CLS)** | CLS = 0.00 durante FLIP ou transição de tela | Fixar containers pais com `aspect-ratio` fixo ou `min-height`. |
| **Consumo de Contexto WebGL** | Máximo de 1 contexto WebGL ativo simultâneo | Unificar todas as imagens da página em uma única cena Three.js. |
| **Garbage Collector Stutters** | Zero instanciações (`new`) dentro de loops RAF | Pré-alocar variáveis vetoriais estáticas no escopo do módulo. |
| **Controle de Resolução em Retina** | `renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2))` | Evita crash de renderização em telas 4K/5K (pixel ratio 3x+). |
| **Fallback Prefers-Reduced-Motion** | Desativação total de distorções de onda e trails | Substituir por transições crossfade de opacidade limpas. |
