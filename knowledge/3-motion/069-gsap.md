---
id: "gsap"
name: "GSAP (GreenSock Animation Platform)"
url: "https://gsap.com/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["Orchestrated Timeline Choreography", "Scroll-Driven Pin & Scrub", "FLIP Layout Morphing", "Kinetic Typography & Splitting", "Sub-pixel Vector Warping", "Micro-Latency Pointer Tracking"]
densidade_informacao: "Independente"
impacto_visual: "Cinematografico/Showstopper a Sutil/Invisivel (Feel)"
custo_computacional: "Medio (JS RAF Ticker / GPU Matrix3D) a Alto (SVG/DOM intensivo sem virtualizacao)"
stack_frameworks: ["Vanilla JS / TypeScript", "React 19 / 18 (@gsap/react)", "Vue (GSAP Core)", "Svelte", "Next.js (App Router)", "Three.js / WebGL / R3F", "Canvas 2D / Pixi.js"]
compatibilidade:
  combinacoes_recomendadas: ["Lenis Smooth Scroll + ScrollTrigger", "Three.js / R3F (interpolando câmeras, uniforms de shaders e transforms)", "Tailwind CSS v4 (layout e estilo estático + GSAP para orquestração matricial)", "SplitText + CustomEase", "MorphSVG + DrawSVG para sistemas de vetores complexos", "Radix UI / Shadcn UI Primitives"]
  conflitos_esteticos: ["Transições CSS puras (`transition: all`) concorrentes no mesmo nó alvo de `gsap.to()` (causa flickering e salto de quadros)", "Framer Motion / Motion.dev concorrendo pelo mesmo atributo `transform` matricial", "ScrollTrigger sem `pinReparent` em elementos descendentes de containers com `filter`, `backdrop-filter` ou `transform`", "Animar propriedades de CPU com reflow contínuo (`top`, `left`, `width`, `height`) em vez de propriedades aceleradas por GPU (`x`, `y`, `scaleX`, `scaleY`)", "Omissão de limpeza via `gsap.context()` ou hook `useGSAP()`, provocando listeners zumbis e triggers duplicados no React StrictMode"]
---

# GSAP (GreenSock Animation Platform) — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)

O **GSAP (GreenSock Animation Platform)** (`https://gsap.com/`), idealizado e mantido sob a liderança técnica de **Jack Doyle** há mais de duas décadas, representa o ápice absoluto da engenharia de animação na web. Tendo evoluído desde os tempos pioneiros da renderização vetorial no Flash (com os consagrados *TweenLite*, *TweenMax* e *TimelineMax*) até a moderna reescrita modular do GSAP 3 e sua subsequente integração ao ecossistema global após a aquisição pela Webflow — momento em que todos os lendários plugins premium do antigo *Club GreenSock* (como `SplitText`, `MorphSVG`, `DrawSVG`, `ScrollSmoother`, `Flip`, `Inertia` e `CustomEase`) tornaram-se 100% gratuitos e de código aberto para a indústria —, o GSAP é a espinha dorsal de mais de 80% dos sites premiados no *Awwwards* e *FWA*.

Diferente de bibliotecas focadas exclusivamente em micro-interações de estado declarativo ou em física de molas reativa em tempo real, o GSAP foi projetado com uma premissa técnica singular: **o controle determinístico milimétrico do tempo através de grafos de animação hierárquicos (Timelines com Playhead Bidirecional)** acoplados a um pipeline matemático de normalização gráfica capaz de interpolar qualquer propriedade numérica ou matricial na velocidade máxima permitida pelo hardware.

```
┌────────────────────────────────────────────────────────────────────────┐
│                        GSAP CORE ARCHITECTURE PIPELINE                 │
└────────────────────────────────────────────────────────────────────────┘
                                     │
           Ticker Central (requestAnimationFrame a 60/120/240Hz)
           • Delta-Time Normalization & lagSmoothing(500, 33)
                                     │
             ┌───────────────────────┴───────────────────────┐
             ▼                                               ▼
┌───────────────────────────────┐               ┌───────────────────────────────┐
│       HIERARCHICAL GRAPH      │               │   FAST MATRIX / SUB-PIXEL     │
│   (Timelines, Tweens, Labels) │               │       RENDER PIPELINE         │
├───────────────────────────────┤               ├───────────────────────────────┤
│ • Bidirectional Scrub Playhead│               │ • transformCache isolado      │
│ • Relative alignment ("<", "-")│              │ • Sub-pixel translation (GPU) │
│ • Non-linear CustomEase curves│               │ • Normalização cross-browser  │
│ • Pause, reverse, timeScale() │               │   SVG/CSS/Canvas/WebGL        │
└───────────────────────────────┘               └───────────────────────────────┘
                                     │
             ┌───────────────────────┴───────────────────────┐
             ▼                                               ▼
┌───────────────────────────────┐               ┌───────────────────────────────┐
│   INTERACTIVE SENSORY HOOKS   │               │   HIGH FREQUENCY OPTIMIZERS   │
│ (ScrollTrigger, Flip, Observer│               │   (gsap.quickTo, quickSetter) │
├───────────────────────────────┤               ├───────────────────────────────┤
│ • Scroll sync (pin & scrub)   │               │ • Zero-overhead memory reuse  │
│ • FLIP state reconciliation   │               │ • 120fps Cursor & Physics     │
│ • Unified pointer & gesture   │               │ • Bypass tween instantiation  │
└───────────────────────────────┘               └───────────────────────────────┘
```

---

### O Paradigma da Timeline e o Playhead Determinístico

A revolução conceitual do GSAP repousa na separação absoluta entre o **desenho da coreografia** e o **avanço do relógio**:
- **O Playhead como Ponteiro Temporal**: Em uma `gsap.timeline()`, cada elemento animado reside em um grafo temporal compartilhado. Assim como em uma fita de áudio analógica ou em uma suíte de edição cinematográfica (como Premiere ou DaVinci Resolve), o tempo possui uma posição física virtual (`progress` de 0.0 a 1.0, ou tempo absoluto em segundos).
- **Controle Bidirecional em Tempo Real**: Uma timeline pode avançar (`play()`), retroceder (`reverse()`), desacelerar sua passagem cósmica (`timeScale(0.2)` para slow motion fluido), saltar instantaneamente para um marco de roteiro (`seek("hero-collapsed")`) ou ser acoplada à rotação da roda do mouse ou do trackpad (`scrollTrigger: { scrub: 1 }`).
- **Composição Relativa Não-Destrutiva**: Diferente de sequências amarradas a `setTimeout` ou `delay` estático acumulativo (que quebram ao menor ajuste de duração de uma cena intermediária), o GSAP introduziu a sintaxe de marcadores de posição relativa:
  - `"<"`: inicia no exato milissegundo de início da animação anterior.
  - `"<0.1"`: inicia 100ms após o início da animação anterior.
  - `"-=0.25"`: sobrepõe 250ms antes do encerramento do passo anterior.
  - Com isso, dezenas de nós no DOM ou objetos no WebGL dançam em sincronia harmônica sem que o engenheiro precise reescrever o tempo de 50 elementos caso decida alterar a introdução do logo de 1.2s para 0.8s.

---

### O Motor Ticker e o Mecanismo de `lagSmoothing`

No coração do GSAP reside o `gsap.ticker`, um despachador de pulso centralizado baseado em `window.requestAnimationFrame`. Ele resolve três dos problemas mais graves da renderização web contemporânea:
1. **Delta-Time Normalization (Monitores de Alta Taxa de Atualização)**:
   Em telas ProMotion de 120Hz (MacBook Pro, iPads) ou monitores gamer de 144Hz a 240Hz, um loop ingênuo baseado em contagem de quadros executa animações no dobro ou quádruplo da velocidade nominal. O `gsap.ticker` mede o intervalo de tempo decorrido ($\Delta t$) entre cada quadro com resolução de microsegundos (`performance.now()`), garantindo que uma transição de 1.5 segundo demore exatamente 1.500ms em qualquer taxa de atualização, sem acelerar nem desacelerar.
2. **Proteção Contra Congelamento de Thread (`lagSmoothing`)**:
   Quando a aba do navegador vai para segundo plano ou o JavaScript trava durante o parsing de um arquivo JSON massivo de 10MB, o relógio do sistema continua avançando. Sem proteção, ao retornar, uma animação calcularia um salto de delta-tempo gigantesco ($\Delta t = 4000\text{ms}$), fazendo elementos atravessarem a tela de forma violenta ou desaparecendo instantaneamente. O GSAP mitiga isso com `gsap.ticker.lagSmoothing(500, 33)`: se o delta ultrapassar 500ms, o motor limita o salto percebido a apenas 33ms (aproximadamente dois quadros a 60fps), retomando o fluxo de forma orgânica e macia sem saltos teletransportados.
3. **Agrupamento de Leituras e Escritas (Eliminação de Layout Thrashing)**:
   O GSAP enfileira as leituras de coordenadas de estilo computadas e realiza todas as escritas no DOM em lotes coordenados dentro do ciclo de frame, prevenindo o reflow destrutivo em cascata que ocorre quando o código alterna leituras (`offsetTop`) e escritas (`style.transform`) repetidamente.

---

### Isolamento Matricial: `transformCache` e Renderização Sub-Pixel

Um dos diferenciais técnicos mais profundos do GSAP em relação ao CSS puro e a outras bibliotecas JS é a sua decomposição interna do `transform`:
- **O Problema da String CSS**: No CSS tradicional, a propriedade `transform` é uma string unificada (ex: `rotate(45deg) translateX(100px) scale(1.2)`). A ordem dos fatores altera o produto geométrico, e interpolar valores independentes exige decomposição de matrizes ou interpolações de strings textuais custosas.
- **Cache Vetorial Independente (`transformCache`)**: O GSAP mantém um objeto interno para cada elemento contendo os componentes primitivos isolados: `x`, `y`, `z`, `scaleX`, `scaleY`, `rotation`, `rotationX`, `rotationY`, `skewX`, `skewY` e `perspective`. Quando você anima `gsap.to(el, { x: 100 })` e simultaneamente outro gatilho altera `gsap.to(el, { scale: 1.5 })`, o GSAP não reconstrói a string do zero: ele atualiza diretamente os coeficientes numéricos e gera em C++ interno a matriz final consolidada:
$$\mathbf{M} = \mathbf{T}_{x,y,z} \times \mathbf{R}_{z} \times \mathbf{R}_{y} \times \mathbf{R}_{x} \times \mathbf{S}_{x,y,z} \times \mathbf{K}_{x,y}$$
- **Aceleração 3D Forçada e Anti-Aliasing**: O GSAP aplica por padrão transformações tridimensionais via `translate3d(x, y, z)` ou matrizes 3D, forçando o navegador a alocar uma textura de composição na GPU (`RenderLayer` independente). Isso ativa a interpolação sub-pixel do motor de rasterização, garantindo que tipografias e contornos vetoriais movam-se suavemente por frações de pixel (0.1px), eliminando os micropulos de pixel snapping comuns do CSS 2D.

---

### O Paradigma de Rastreamento de Alta Frequência: `gsap.quickTo()` e `gsap.quickSetter()`

Em interações que reagem ao mouse (`pointermove`), giroscópio ou fluxo de áudio, criar uma nova instância de tween a cada evento a 120Hz gera acúmulo severo de objetos na memória e sobrecarrega o Garbage Collector (GC), provocando microtravamentos (jank).

O GSAP resolve essa física de alta frequência com `gsap.quickTo(target, property, vars)`:
- Ele pré-aloca a estrutura de tween em memória fixa uma única vez.
- Retorna uma função de alta performance otimizada que aceita apenas o valor de destino numérico.
- Quando o ponteiro move, você executa `xTo(e.clientX)`. O motor redireciona a inércia em tempo real sem instanciar novos objetos, sem repensar seletores e sem revalidar propriedades CSS, mantendo 120fps puros mesmo sob rajadas de eventos contínuos.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos Críticos de Interface e Engenharia Criativa

```
┌────────────────────────────────────────────────────────────────────────┐
│                   TERRITÓRIOS DE DOMÍNIO ABSOLUTO DO GSAP              │
└────────────────────────────────────────────────────────────────────────┘

  [ 01. SCROLLYTELLING PINNED ] ── Narrativas editoriais, landing pages de
                                   produtos físicos e hardware, onde a
                                   viewport é fixada (pinned) e o scroll
                                   revela camadas e modelos 3D em scrub.

  [ 02. KINETIC TYPOGRAPHY    ] ── Quebra de títulos e textos em linhas,
                                   palavras e glifos via SplitText, com
                                   revelações de máscara (clip) milimétricas.

  [ 03. VETORIAL SVG AVANÇADO ] ── Morfismo de vetores heterogêneos com
                                   MorphSVG e desenho sequencial de linhas
                                   técnicas e blueprints com DrawSVG.

  [ 04. FLIP LAYOUT MORPHING  ] ── Reorganização de grids complexos, filtros
                                   instantâneos e expansão de card-to-fullscreen
                                   sem travamentos de reflow.

  [ 05. ORQUESTRAÇÃO 3D / GLSL] ── Controle de câmeras no Three.js, luzes e
                                   uniforms de shaders GLSL sincronizados
                                   às ações da timeline e da página.
```

1. **Scrollytelling Editorial e Apresentações de Hardware (Estilo Apple / Awwwards Site of the Year)**:
   - Seções onde a tela trava (`pin: true`), o usuário gira a roda do mouse e uma sequência complexa acontece: o produto desmonta suas peças em visão explodida, a tipografia desliza em camadas com máscaras diagonais e o fundo transmuta de cor, tudo rigidamente atrelado ao deslocamento físico da barra de rolagem (`scrub: 1`).
2. **Carrosséis Virtuais de Rolagem Horizontal ("Fake Horizontal Scroll")**:
   - Experiências em que a página mantém a barra de rolagem vertical nativa do navegador (preservando a sensibilidade de trackpads e touchscreens), mas um container com dezenas de painéis desliza lateralmente através de translações matriciais calculadas (`xPercent: -100 * (sections.length - 1)`), permitindo transitar por portfólios densos sem quebrar o fluxo natural de navegação.
3. **Morfologia Vetorial Complexa e Efeitos de Linha (MorphSVG / DrawSVG)**:
   - Metamorfose entre dois caminhos SVG completamente diferentes, com contagens distintas de pontos de controle Bézier (ex: o contorno de um logotipo transformando-se organicamente na silhueta de um produto ou em um ícone de interface).
   - Animação de blueprints técnicos, diagramas de arquitetura e traçado de circuitos eletrônicos que se "desenham" à medida que entram na viewport.
4. **Cinética Tipográfica de Alto Nível (SplitText)**:
   - Divisão algorítmica de textos em nós HTML isolados por linha, palavra ou caractere, com recálculo automático em redimensionamento de janela e aplicação de máscaras de corte (`overflow: hidden`) onde cada palavra sobe com desaceleração exponencial independente.
5. **Transições de Layout FLIP com Elementos Heterogêneos (Flip Plugin)**:
   - Filtros de galerias em e-commerces e dashboards onde clicar em uma categoria ("Todos", "Design", "Código") reposiciona 40 cards simultaneamente, mantendo a animação puramente acelerada pela GPU sem quedas de taxa de quadros.
6. **Integração Unificada com Motores 3D (Three.js, WebGL, Pixi.js, Canvas 2D)**:
   - GSAP interpola perfeitamente propriedades de objetos puros do JavaScript: `gsap.to(camera.position, { z: 5 })`, `gsap.to(material.uniforms.uProgress, { value: 1 })`. Isso permite coreografar elementos DOM da UI e o mundo 3D dentro da exata mesma timeline com sincronismo de milissegundo.

---

### Papel na Composição Visual (A Regra 60-30-10 de Motion)

O GSAP é uma ferramenta de espectro total, mas seu posicionamento em projetos de elite deve seguir um equilíbrio rigoroso de engenharia para evitar sobrecarga sensorial:

```
┌────────────────────────────────────────────────────────────────────────┐
│                   A REGRA 60-30-10 DE MOTION DESIGN COM GSAP           │
└────────────────────────────────────────────────────────────────────────┘

  [ 60% — A INÉRCIA INVISÍVEL ] ── Micro-reações e rastreamento de cursor:
                                   gsap.quickTo para botões magnéticos,
                                   tooltips inerciais, hover states táteis
                                   de 120ms com eases responsivos.

  [ 30% — A COREOGRAFIA DE FLUXO] ── Entradas de página, staggers de cards
                                     via ScrollTrigger.batch, expansão de
                                     drawers/modais com Flip, transições
                                     de rota via Barba.js ou Next.js.

  [ 10% — OS SHOWSTOPPERS     ] ── Pinned scrollytelling de página inteira,
                                   cenas 3D Three.js orquestradas no scrub,
                                   morfismos orgânicos de SVG MorphSVG.
```

- **60% — A Inércia Invisível (Feel & Micro-Interações)**:
  Executado principalmente via `gsap.quickTo()` e `gsap.to()` ultracurtos. O usuário passa o mouse sobre botões e sente atração gravitacional sutil (efeito magnético de 15px de raio com `power3.out`); menus de dropdown revelam-se sem oscilação; campos de formulário reagem com `elastic.out(1, 0.4)` sutil em caso de foco ou erro. O usuário não percebe que existe um "motor gráfico": ele apenas sente que a interface tem massa física e firmeza tátil.
- **30% — A Coreografia de Fluxo (Layout & Transições Estruturais)**:
  Cascatas de entrada ordenadas de conteúdo quando uma seção entra na tela (`ScrollTrigger.batch` aplicando `stagger: 0.08`, `y: 40`, `ease: "power3.out"`), alternância suave de abas e painéis via `Flip.from()`, e fechamento/abertura de menus laterais com timelines orquestradas que movem o backdrop, a gaveta e os links com atrasos harmônicos.
- **10% — Os Showstoppers Cinematográficos (O Clímax Visual)**:
  O momento ápice da aplicação. A seção Hero onde a tipografia se fragmenta e recompõe em 3D, a transição de produto de tela inteira travada na rolagem, ou a animação de loading com metamorfose vetorial SVG que conecta a entrada do usuário ao ecossistema do produto.

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Práticas Proibidas & Anti-Padrões Críticos

1. **Animar Propriedades de Reflow de CPU (Geometry Thrashing)**:
   - **O Erro**: Executar `gsap.to(element, { width: 400, height: 300, top: 50, left: 100 })`.
   - **O Impacto Catastrófico**: O navegador é forçado a recalcular a árvore de layout (*Reflow*), repintar os pixels (*Paint*) e recompor a cena (*Composite*) a cada quadro (60 ou 120 vezes por segundo). Em páginas com mais de 500 nós DOM, isso derruba a taxa de quadros para 12-18fps e esgota a bateria de smartphones em minutos.
   - **A Regra de Ouro**: Anime **exclusivamente** propriedades suportadas pelo Compositor da GPU:
     - Utilize `x` e `y` em vez de `left` e `top`.
     - Utilize `scaleX` e `scaleY` em vez de `width` e `height`.
     - Utilize `autoAlpha` em vez de alternar `opacity` e `visibility` separadamente.
     - Quando for indispensável alterar o layout estrutural do DOM, utilize o **Flip Plugin**, que lê a geometria estática e interpola visualmente via matrizes na GPU.
2. **Guerra de Motores: Conflito com Transições CSS Puras**:
   - **O Erro**: Declarar classes como `transition-all duration-300 ease-in-out` do Tailwind CSS em nós controlados por `gsap.to()`, `ScrollTrigger` ou `gsap.quickTo()`.
   - **O Efeito**: A cada milissegundo em que o GSAP escreve um novo valor no atributo `style.transform`, o motor de CSS do navegador intercepta a mudança e agenda uma transição interna de 300ms sobre aquele microsalto. O resultado é um tremor visual violento (*jitter*), atraso perceptível de entrada (*lag*) e colapso de performance.
   - **Regra**: Elementos animados pelo GSAP devem ter `transition: none !important;` nas propriedades geridas pelo script.
3. **Scroll Hijacking Agressivo sem Barra Nativa (Quebra de Usabilidade Mobile)**:
   - **O Erro**: Utilizar o plugin `Observer` para bloquear completamente o evento `wheel` ou `touchmove` em navegadores mobile para criar uma apresentação estrita de telas cheias de rolagem presa.
   - **O Efeito**: Destrói a inércia nativa dos sistemas iOS e Android, impede a navegação acessível por leitores de tela ou teclado e causa profunda rejeição e claustrofobia sensorial no usuário comum.
4. **Acúmulo de Triggers e Vazamento de Memória em SPAs (Single Page Applications)**:
   - **O Erro**: Instanciar `ScrollTrigger.create()` dentro de componentes React, Vue ou Svelte sem destruí-los (`kill()`) ao desmontar o componente.
   - **O Efeito**: Em navegações de rotas (Next.js, Remix, Vue Router), os gatilhos antigos continuam escutando a janela, recalculando posições sobre nós DOM já destruídos no ar, gerando vazamento de memória massivo, travamento de scroll e exceções no console.
   - **Solução Mandatória**: Utilizar o hook `@gsap/react` com `useGSAP()` ou envolver criações em `gsap.context()`.
5. **O "Bug da Transform Matrix" com ScrollTrigger Pinning**:
   - **O Erro**: Aplicar `ScrollTrigger: { pin: true }` em um elemento que possui ancestrais no DOM com estilos CSS como `transform`, `filter`, `backdrop-filter` ou `perspective`.
   - **A Causa Física**: A especificação CSS determina que qualquer ancestral com `transform` ou `filter` cria um novo Bloco de Contenção (*Containing Block*) para elementos com `position: fixed`. Quando o ScrollTrigger aplica `position: fixed` durante o pin, o elemento fica fixado em relação ao ancestral, e não à viewport da janela, quebrando completamente a fixação visual.
   - **A Correção**: Utilizar a propriedade `pinReparent: true` ou reorganizar a hierarquia do DOM para garantir que elementos com `pin` tenham ancestrais limpos de filtros ou transforms.

---

### Diretrizes de Acessibilidade & Gestão de GPU

1. **Suporte Obrigatório a `prefers-reduced-motion` via `gsap.matchMedia()`**:
   - Usuários com distúrbios vestibulares, labirintite ou epilepsia fotossensível sofrem vertigem severa com scrubs rápidos de tela e tipografias flutuantes.
   - O GSAP fornece o método nativo `gsap.matchMedia()`, que isola e cancela automaticamente as timelines cinematográficas quando a preferência do sistema operacional do usuário estiver ativa:
   ```typescript
   const mm = gsap.matchMedia();

   mm.add({
     isDesktop: "(min-width: 1024px)",
     reduceMotion: "(prefers-reduced-motion: reduce)"
   }, (context) => {
     const { reduceMotion } = context.conditions!;

     if (reduceMotion) {
       // Apenas transição instantânea ou fade sutil sem deslocamento espacial
       gsap.set(".hero-layer", { autoAlpha: 1 });
       return;
     }

     // Coreografia completa para usuários normais
     gsap.timeline({ scrollTrigger: { trigger: ".hero", pin: true, scrub: 1 } })
       .from(".hero-layer", { yPercent: 100, stagger: 0.2 });
   });
   ```
2. **Uso Cirúrgico de `will-change: transform`**:
   - Jamais declare `* { will-change: transform; }` no CSS global.
   - Cada elemento com `will-change` consome memória de vídeo (VRAM) dedicada na placa gráfica do usuário. Em celulares intermediários, marcar mais de 30 elementos simultâneos provoca o estouro de limite de memória de texturas, forçando o navegador a descartar texturas e degradar a renderização para a CPU.
   - Deixe o próprio GSAP gerenciar camadas através de sua propriedade interna `force3D: "auto"`, que aloca a aceleração de hardware durante a execução do movimento e libera os recursos quando o elemento atinge o repouso.
3. **Alinhamento e Recálculo de Layout (`ScrollTrigger.refresh()`)**:
   - Fontes da web (Web Fonts), imagens carregadas de forma assíncrona (`loading="lazy"`) e componentes renderizados após requisições de API alteram a altura vertical da página após o carregamento inicial.
   - Sempre chame `ScrollTrigger.refresh()` após o evento `document.fonts.ready` ou após a conclusão de renderizações assíncronas para recalcular os offsets e pontos de partida exatos de cada trigger.

---

## 4. Catálogo de Efeitos, Primitivas e Padrões de Animação

Abaixo estão catalogados os **10 padrões de movimento e primitivas de engenharia mais notáveis** viabilizados pelo ecossistema do GSAP:

---

### 1. ScrollTrigger Pinned Section Scrollytelling (Fixação de Viewport com Scrub)
- **Comportamento Visual**: O container da cena atinge o topo da janela e trava magneticamente (`position: fixed` controlado). O usuário continua rolando o mouse, mas a página não avança para baixo; em vez disso, elementos internos entram, transformam-se e desvanecem em sincronia estrita com a barra de rolagem. Ao final da timeline, a página destrava naturalmente e segue o fluxo de leitura normal.
- **Anatomia & Parâmetros**:
  - `trigger`: Nó ancestral que define a área de rolagem.
  - `pin: true`: Trava o elemento alvo durante o deslocamento virtual.
  - `scrub: 1` ou `true`: 1 segundo de amortecimento elástico para absorver o tremor de mouses mecânicos.
  - `start: "top top"` e `end: "+=200%"` (a cena dura 2x a altura da viewport).
  - `anticipatePin: 1`: Calcula a fixação com antecedência de quadros para evitar flashes de salto visual.
- **Gatilho**: Progresso contínuo de rolagem (`scroll progress`).
- **Onde Encaixar**: Seções de apresentação de produto ("Como Funciona em 3 Etapas"), visualizadores de tecnologia e relatórios anuais interativos.

---

### 2. Fake Horizontal Scroll Showcase (Translação Pinned Lateral)
- **Comportamento Visual**: Enquanto o usuário efetua a rolagem vertical padrão, uma esteira horizontal de painéis ou cartões de projetos desliza lateralmente da direita para a esquerda ao longo da viewport, simulando um carrossel cinemático contínuo.
- **Anatomia & Parâmetros**:
  - `gsap.to(panelsContainer, { xPercent: -100 * (panels.length - 1), ease: "none", scrollTrigger: { trigger: wrapper, pin: true, scrub: 1, end: () => "+=" + panelsContainer.offsetWidth } })`.
- **Gatilho**: Progresso da rolagem vertical do navegador.
- **Onde Encaixar**: Galerias de portfólio de cases, cronogramas históricos corporativos e vitrines de produtos de e-commerce de luxo.

---

### 3. Kinetic Typography Split-Mask Reveal (Divisão em Linhas e Máscara de Corte)
- **Comportamento Visual**: Um grande título editorial surge na tela. O texto não se move como um bloco chapado: ele é fatiado linha a linha. Cada linha emerge de trás de uma linha invisível inferior (corte milimétrico via `overflow: hidden`), subindo suavemente com uma leve inclinação de perspectiva e atraso escalonado (*stagger*).
- **Anatomia & Parâmetros**:
  - `new SplitText(element, { type: "lines, words", linesClass: "lineChild" })`.
  - Wrapper ancestral com `overflow: hidden`.
  - Animação em `lineChild`: `yPercent: 120`, `opacity: 0` $\rightarrow$ `yPercent: 0`, `opacity: 1`, `stagger: 0.08`, `ease: "power4.out"`, `duration: 1.2`.
- **Gatilho**: Entrada de seção na tela (`ScrollTrigger`) ou transição de montagem de página.
- **Onde Encaixar**: Títulos principais de seções Hero, manifestos de marca e citações editoriais em landing pages de alto impacto.

---

### 4. High-Performance Pointer Tracker & Magnetic Button (`gsap.quickTo`)
- **Comportamento Visual**: O botão da interface atua como um polo gravitacional. Conforme o cursor aproxima-se do botão a menos de 50px, o botão e seu texto interno deslocam-se organicamente em direção ao ponteiro. Ao afastar o mouse, o botão retorna instantaneamente à sua posição de repouso com inércia amortecida sem perder nenhum quadro a 120fps.
- **Anatomia & Parâmetros**:
  - Duas instâncias de `gsap.quickTo(button, "x", { duration: 0.6, ease: "power3.out" })` e `"y"`.
  - Cálculo vetorial da distância euclidiana: $\Delta x = \text{mouseX} - \text{centerX}$, $\Delta y = \text{mouseY} - \text{centerY}$.
  - Fator de atenuação gravitacional (ex: 35% de atração para a cápsula e 55% para o texto interno).
- **Gatilho**: Evento `pointermove` e `pointerleave` do mouse.
- **Onde Encaixar**: Botões de Call to Action (CTA) principais, botões de reprodução de vídeo flutuantes e cursores personalizados.

---

### 5. FLIP Layout State Morphing (`gsap/Flip`)
- **Comportamento Visual**: Um card de produto em uma grade compacta é clicado. Em vez de abrir um modal que simplesmente surge por cima, o próprio card original expande-se fluidamente até assumir o tamanho da janela inteira (tela cheia), enquanto os textos e imagens se reacomodam organicamente. Ao fechar, ele se comprime de volta com precisão milimétrica à sua posição exata na grade.
- **Anatomia & Parâmetros**:
  - `const state = Flip.getState(".card, .card-image, .card-body");`
  - Mudança de estado no DOM / classe CSS (`card.classList.toggle("is-expanded")`).
  - `Flip.from(state, { duration: 0.7, ease: "expo.out", absolute: true, nested: true })`.
- **Gatilho**: Evento de clique de seleção do usuário.
- **Onde Encaixar**: Galerias de projetos, cards expansíveis de dashboard e transições de carrinhos de compra.

---

### 6. MorphSVG Organic Vector Metamorphosis (`gsap/MorphSVGPlugin`)
- **Comportamento Visual**: Um ícone geométrico complexo ou forma líquida abstrata de SVG transmuta-se de forma suave e orgânica em outra forma totalmente distinta (por exemplo: um ícone de estrela de 5 pontas transformando-se em um círculo perfeito ou um logotipo corporativo fundindo-se em uma seta interativa).
- **Anatomia & Parâmetros**:
  - Caminho SVG de origem `<path d="..." />` e caminho alvo `<path id="target" d="..." />`.
  - `gsap.to("#origin", { morphSVG: "#target", duration: 1.5, ease: "power2.inOut" })`.
  - O algoritmo interno recalcula e insere automaticamente pontos de ancoragem intermediários para garantir transição suave entre formas com topologias heterogêneas.
- **Gatilho**: Hover tátil, clique de alternância de modo (como Sol $\leftrightarrow$ Lua no tema escuro) ou scroll progress.
- **Onde Encaixar**: Ícones dinâmicos de alternância de estado, formas de fundo decorativas líquidas e identidades visuais dinâmicas.

---

### 7. DrawSVG Blueprint & Vector Path Progression (`gsap/DrawSVGPlugin`)
- **Comportamento Visual**: Linhas de contorno vetoriais de ilustrações técnicas, gráficos de arquitetura, assinaturas manuscritas ou fios condutores de diagramas são desenhados de forma progressiva, como se uma caneta invisível estivesse traçando o caminho na velocidade da rolagem do usuário.
- **Anatomia & Parâmetros**:
  - `gsap.fromTo(svgPath, { drawSVG: "0%" }, { drawSVG: "100%", duration: 2, ease: "power2.out", scrollTrigger: { trigger: svgPath, scrub: 0.5 } })`.
  - O plugin calcula automaticamente o comprimento exato do caminho via `getTotalLength()` e normaliza bugs de arredondamento de sub-pixel em navegadores legados e mobile.
- **Gatilho**: Entrada de elemento na tela ou avanço do scroll.
- **Onde Encaixar**: Infográficos interativos, diagramas de fluxo de dados, ilustrações isométricas de tecnologia e interfaces de assinatura eletrônica.

---

### 8. Gesture & Wheel Intent Orchestration (`gsap/Observer`)
- **Comportamento Visual**: A interface reage com precisão cirúrgica a intenções de gesto do usuário (rotação suave da roda do mouse, deslizar de dois dedos no trackpad, swipe tátil em telas de toque ou setas do teclado), disparando transições discretas de slide sem depender de elementos com rolagem nativa.
- **Anatomia & Parâmetros**:
  - `Observer.create({ target: window, type: "wheel,touch,pointer", onUp: () => gotoSlide(index + 1), onDown: () => gotoSlide(index - 1), tolerance: 15, preventDefault: true })`.
- **Gatilho**: Intenção vetorial de deslocamento em múltiplos dispositivos de entrada.
- **Onde Encaixar**: Sliders e carrosséis imersivos de tela cheia, experiências narrativas de visual novel ou galerias 3D que operam independentes do documento DOM padrão.

---

### 9. Staggered Batch Ingestion (`ScrollTrigger.batch`)
- **Comportamento Visual**: Em uma grade de 50 produtos ou postagens de blog, os elementos não disparam 50 listeners individuais pesados. Conforme grupos de 3 a 4 cards entram no campo de visão, eles são detectados em lote e revelam-se em uma cascata harmoniosa de opacidade e elevação vertical.
- **Anatomia & Parâmetros**:
  - `ScrollTrigger.batch(".grid-item", { onEnter: (batch) => gsap.to(batch, { opacity: 1, y: 0, stagger: 0.1, overwrite: true }), interval: 0.1 })`.
- **Gatilho**: Intersecção da viewport com agrupamento de nós em lote.
- **Onde Encaixar**: Feeds infinitos, catálogos de e-commerce e listagens de repositórios.

---

### 10. Smooth Inertial Layer Parallax (`ScrollSmoother` / Speed Factors)
- **Comportamento Visual**: Elementos da página deslocam-se com diferentes fatores de velocidade perceptual: imagens de fundo movem-se a 80% da velocidade da rolagem (`data-speed="0.8"`), enquanto elementos flutuantes de primeiro plano movem-se a 120% (`data-speed="1.2"`), conferindo uma sensação tridimensional de profundidade de campo estereoscópica.
- **Anatomia & Parâmetros**:
  - `ScrollSmoother.create({ smooth: 1.5, effects: true, smoothTouch: 0.1 })`.
  - Atributos declarativos no DOM: `data-speed` e `data-lag` (inércia de atraso elástico).
- **Gatilho**: Rolagem global suavizada da página.
- **Onde Encaixar**: Landing pages de moda, estúdios de arquitetura e narrativas visuais imersivas.

---

## 5. Matemática do Movimento & Receitas de Código

### Curvas de Interpolação Canônicas do GSAP

O GSAP utiliza equações analíticas pré-calculadas de altíssima eficiência que superam o custo de cálculo das curvas Bézier padrão do navegador quando há necessidade de estalo e amortecimento físico real:

```
┌────────────────────────────────────────────────────────────────────────┐
│                   EQUAÇÕES MATEMÁTICAS DAS CURVAS GSAP                 │
└────────────────────────────────────────────────────────────────────────┘

  [ power4.out ] ─── f(t) = 1 - (1 - t)⁴
                     O padrão ouro de desaceleração suave: aceleração
                     instantânea inicial com frenagem progressiva ultra-elegante.

  [ expo.out   ] ─── f(t) = t === 1 ? 1 : 1 - 2^(-10 * t)
                     O "Apple Ease": desaceleração cirúrgica dramática; ideal
                     para entradas de títulos hero e modais de tela cheia.

  [ back.out   ] ─── f(t) = 1 + (s + 1)*(t - 1)³ + s*(t - 1)²  (onde s = 1.70158)
                     Ultrapassa ligeiramente o ponto final e recua ao repouso;
                     perfeito para micro-interações de botões e switches.
```

1. **`power4.out`**:
   - Fórmula: $f(t) = 1 - (1 - t)^4$
   - Equivalente CSS: `cubic-bezier(0.25, 1, 0.5, 1)`
   - Uso recomendado: Entradas padrão de UI, revelações de cards e transições de rotas.
2. **`expo.out`**:
   - Fórmula: $f(t) = 1 - 2^{-10t}$ (para $t \in [0, 1)$)
   - Equivalente CSS: `cubic-bezier(0.16, 1, 0.3, 1)`
   - Uso recomendado: Máscaras de texto cinético (`SplitText`) e transições FLIP de tela inteira.
3. **`power2.inOut`**:
   - Fórmula: Quadrática simétrica; ideal para transições contínuas de ida e volta (loops, carrosséis infinitos, transições de modo escuro/claro).
4. **`elastic.out(amplitude, period)`**:
   - Simulação matemática de oscilador elástico com overshoot decrescente:
     $$f(t) = a \cdot 2^{-10t} \cdot \sin\left(\frac{(t \cdot d - s) \cdot 2\pi}{p}\right) + 1$$
   - Configuração recomendada para UI tátil: `ease: "elastic.out(1, 0.4)"` (amplitude 1.0, período elástico rápido de 400ms para evitar oscilações exageradas que pareçam infantis).

---

### Receita de Código 1: O Padrão Universal para React 19 / 18 com `@gsap/react`

Este componente demonstra a integração padrão ouro na indústria: uso do hook `useGSAP()` para garantir isolamento de escopo no DOM, limpeza automática de memória, segurança contra execução duplicada em modo estrito (`React.StrictMode`), responsividade declarativa com `gsap.matchMedia()` e respeito automático à acessibilidade de `prefers-reduced-motion`.

```tsx
import React, { useRef } from "react";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { SplitText } from "gsap/SplitText";
import { useGSAP } from "@gsap/react";

// Registro obrigatório de plugins do GSAP
if (typeof window !== "undefined") {
  gsap.registerPlugin(ScrollTrigger, SplitText, useGSAP);
}

interface FeatureItem {
  id: string;
  tag: string;
  title: string;
  description: string;
  metric: string;
  metricLabel: string;
}

const FEATURES_DATA: FeatureItem[] = [
  {
    id: "01",
    tag: "Orquestração Determinística",
    title: "Timelines com Precisão Milimétrica",
    description: "Controle total sobre cada frame com playheads bidirecionais sincronizados ao hardware nativo.",
    metric: "120 FPS",
    metricLabel: "Renderização Contínua em Monitores ProMotion"
  },
  {
    id: "02",
    tag: "Layout Sem Reflow",
    title: "Geometria FLIP Acelerada na GPU",
    description: "Transições de layout complexas sem disparo de reflows destrutivos através de matrizes 3D.",
    metric: "0 ms",
    metricLabel: "Layout Thrashing ou Jank de Renderização"
  },
  {
    id: "03",
    tag: "Scroll Conectado",
    title: "Fixação e Interpolação Scrub",
    description: "Narrativas cinematográficas de produtos com amortecimento inercial e controle elástico de jitter.",
    metric: "100%",
    metricLabel: "Gratuito e Livre para Ambientes Comerciais"
  }
];

export const PinnedScrollytellingShowcase: React.FC = () => {
  const containerRef = useRef<HTMLDivElement | null>(null);
  const panelsWrapperRef = useRef<HTMLDivElement | null>(null);

  useGSAP(
    () => {
      const mm = gsap.matchMedia();

      // Configuração adaptativa de Breakpoints e Acessibilidade
      mm.add(
        {
          isDesktop: "(min-width: 1024px)",
          isMobile: "(max-width: 1023px)",
          reduceMotion: "(prefers-reduced-motion: reduce)"
        },
        (context) => {
          const { isDesktop, reduceMotion } = context.conditions as {
            isDesktop: boolean;
            isMobile: boolean;
            reduceMotion: boolean;
          };

          // 1. FALLBACK DE ACESSIBILIDADE: Prefers Reduced Motion
          if (reduceMotion) {
            gsap.set(".feature-card", { opacity: 1, y: 0 });
            gsap.set(".feature-headline", { opacity: 1, y: 0 });
            return;
          }

          // 2. KINETIC TYPOGRAPHY: Revelação de Máscara no Cabeçalho
          const titleElement = containerRef.current?.querySelector(".hero-title");
          if (titleElement) {
            const split = new SplitText(titleElement, {
              type: "lines, words",
              linesClass: "overflow-hidden"
            });

            gsap.from(split.words, {
              yPercent: 120,
              duration: 1.1,
              ease: "power4.out",
              stagger: 0.04,
              scrollTrigger: {
                trigger: titleElement,
                start: "top 85%",
                toggleActions: "play none none reverse"
              }
            });
          }

          // 3. DESKTOP PINNED SCROLLYTELLING COM SCRUB
          if (isDesktop && panelsWrapperRef.current) {
            const panels = gsap.utils.toArray<HTMLElement>(".feature-card");

            const mainTimeline = gsap.timeline({
              scrollTrigger: {
                trigger: containerRef.current,
                pin: true,
                start: "top top",
                end: `+=${panels.length * 100}%`,
                scrub: 1, // 1s de inércia elástica para absorver o jitter de scrollwheels mecânicas
                anticipatePin: 1,
                snap: {
                  snapTo: 1 / (panels.length - 1),
                  duration: { min: 0.25, max: 0.6 },
                  ease: "power2.inOut"
                }
              }
            });

            panels.forEach((panel, index) => {
              if (index === 0) return; // O primeiro painel já começa visível

              mainTimeline
                .fromTo(
                  panel,
                  {
                    autoAlpha: 0,
                    scale: 0.92,
                    yPercent: 30
                  },
                  {
                    autoAlpha: 1,
                    scale: 1,
                    yPercent: 0,
                    ease: "power3.out",
                    duration: 1
                  }
                )
                .to(
                  panels[index - 1],
                  {
                    autoAlpha: 0.2,
                    scale: 0.95,
                    filter: "blur(8px)",
                    duration: 0.8
                  },
                  "<" // Executa em paralelo ao painel que surge
                );
            });
          }

          // 4. MOBILE: Revelação em Lote via ScrollTrigger.batch (Sem Pin para preservar usabilidade)
          if (!isDesktop) {
            ScrollTrigger.batch(".feature-card", {
              start: "top 85%",
              onEnter: (batch) =>
                gsap.to(batch, {
                  autoAlpha: 1,
                  y: 0,
                  stagger: 0.15,
                  duration: 0.8,
                  ease: "power3.out",
                  overwrite: true
                }),
              onLeaveBack: (batch) =>
                gsap.to(batch, {
                  autoAlpha: 0,
                  y: 40,
                  duration: 0.4,
                  overwrite: true
                })
            });
          }
        }
      );

      // Cleanup automático executado pelo useGSAP ao desmontar ou alterar dependências
    },
    { scope: containerRef }
  );

  return (
    <section
      ref={containerRef}
      className="relative w-full min-h-screen bg-[#050505] text-[#FAFAFA] flex flex-col justify-center px-6 lg:px-20 py-24 overflow-hidden select-none"
    >
      {/* Grade de Fundo Decorativa */}
      <div 
        className="absolute inset-0 bg-[linear-gradient(to_right,#151515_1px,transparent_1px),linear-gradient(to_bottom,#151515_1px,transparent_1px)] bg-[size:4rem_4rem] [mask-image:radial-gradient(ellipse_60%_50%_at_50%_50%,#000_70%,transparent_100%)] pointer-events-none opacity-40" 
        aria-hidden="true"
      />

      <div className="relative z-10 max-w-7xl mx-auto w-full mb-16">
        <span className="text-xs uppercase tracking-[0.25em] text-[#00E599] font-mono font-semibold block mb-3">
          Arquitetura de Movimento Industrial
        </span>
        <h2 className="hero-title text-4xl lg:text-7xl font-extrabold tracking-tight max-w-4xl leading-[1.05]">
          A Ciência da Coreografia Contínua e Sem Jank.
        </h2>
      </div>

      {/* Container de Painéis Fixos */}
      <div
        ref={panelsWrapperRef}
        className="relative z-10 max-w-7xl mx-auto w-full grid grid-cols-1 lg:grid-cols-3 gap-8"
      >
        {FEATURES_DATA.map((item, index) => (
          <article
            key={item.id}
            className="feature-card relative bg-[#0D0D0E]/80 backdrop-blur-xl border border-white/10 rounded-2xl p-8 flex flex-col justify-between shadow-2xl transition-colors hover:border-[#00E599]/40"
            style={{ willChange: "transform, opacity" }}
          >
            <div>
              <div className="flex items-center justify-between mb-8">
                <span className="text-sm font-mono text-white/40 tracking-wider">
                  [{item.id}]
                </span>
                <span className="text-xs font-mono uppercase bg-white/5 border border-white/10 px-3 py-1 rounded-full text-white/70">
                  {item.tag}
                </span>
              </div>
              <h3 className="text-2xl font-bold mb-4 tracking-tight text-white">
                {item.title}
              </h3>
              <p className="text-sm text-white/60 leading-relaxed">
                {item.description}
              </p>
            </div>

            <div className="mt-12 pt-6 border-t border-white/10">
              <div className="text-3xl font-mono font-black text-[#00E599] tracking-tight">
                {item.metric}
              </div>
              <div className="text-xs text-white/40 font-mono mt-1">
                {item.metricLabel}
              </div>
            </div>
          </article>
        ))}
      </div>
    </section>
  );
};
```

---

### Receita de Código 2: Micro-Interação de Botão Magnético com `gsap.quickTo()`

Esta receita implementa a física de atração magnética contínua a 120fps sem alocar lixo de memória na thread de eventos:

```tsx
import React, { useRef } from "react";
import { gsap } from "gsap";
import { useGSAP } from "@gsap/react";

interface MagneticButtonProps {
  children: React.ReactNode;
  className?: string;
  onClick?: () => void;
  strength?: number; // Fator de atração magnética (padrão: 0.35)
}

export const MagneticButton: React.FC<MagneticButtonProps> = ({
  children,
  className = "",
  onClick,
  strength = 0.35
}) => {
  const buttonRef = useRef<HTMLButtonElement | null>(null);
  const textRef = useRef<HTMLSpanElement | null>(null);

  useGSAP(
    () => {
      const button = buttonRef.current;
      const text = textRef.current;
      if (!button || !text) return;

      // Pré-aloca os interpoladores de alta performance (Zero GC Churn)
      const xToButton = gsap.quickTo(button, "x", { duration: 0.6, ease: "power3.out" });
      const yToButton = gsap.quickTo(button, "y", { duration: 0.6, ease: "power3.out" });
      const xToText = gsap.quickTo(text, "x", { duration: 0.7, ease: "power3.out" });
      const yToText = gsap.quickTo(text, "y", { duration: 0.7, ease: "power3.out" });

      const handlePointerMove = (e: PointerEvent) => {
        const { clientX, clientY } = e;
        const rect = button.getBoundingClientRect();
        
        // Vetor de distância do centro do botão ao ponteiro
        const deltaX = clientX - (rect.left + rect.width / 2);
        const deltaY = clientY - (rect.top + rect.height / 2);

        // Deslocamento diferenciado: o texto move mais que o botão para dar sensação de profundidade
        xToButton(deltaX * strength);
        yToButton(deltaY * strength);
        xToText(deltaX * (strength * 1.4));
        yToText(deltaY * (strength * 1.4));
      };

      const handlePointerLeave = () => {
        // Retorno elástico inercial suave à posição de repouso
        xToButton(0);
        yToButton(0);
        xToText(0);
        yToText(0);
      };

      button.addEventListener("pointermove", handlePointerMove);
      button.addEventListener("pointerleave", handlePointerLeave);

      return () => {
        button.removeEventListener("pointermove", handlePointerMove);
        button.removeEventListener("pointerleave", handlePointerLeave);
      };
    },
    { scope: buttonRef }
  );

  return (
    <button
      ref={buttonRef}
      onClick={onClick}
      className={`relative inline-flex items-center justify-center px-8 py-4 rounded-full font-medium transition-colors cursor-pointer select-none ${className}`}
      style={{ willChange: "transform" }}
    >
      <span ref={textRef} className="relative z-10 inline-block pointer-events-none">
        {children}
      </span>
    </button>
  );
};
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao planejar a arquitetura técnica de uma aplicação no `DESIGN_BLUEPRINT.md`, a inteligência artificial arquiteta deve aderir a convenções rigorosas de especificação de movimento antes de iniciar qualquer codificação:

### Vocabulário Mandatório de Engenharia de Movimento

A IA deve banir termos vagos como *"animação suave ao rolar"* ou *"efeito bonito no card"*, substituindo-os pelo vocabulário canônico do GSAP:
- Declarar o **Gatilho e Plugin**: `ScrollTrigger(pin, scrub: 1, anticipatePin: 1)`, `Flip(from, absolute: true)`, `SplitText(lines, words)`, `gsap.quickTo()`.
- Declarar as **Propriedades Aceleradas**: `xPercent`, `yPercent`, `scale`, `rotation`, `autoAlpha` (proibido especificar animação contínua de `width`, `height`, `top`, `left`).
- Declarar a **Curva Exata**: `power4.out`, `expo.out`, `elastic.out(1, 0.4)`, `none` (obrigatória para timelines scrubbed a fim de evitar acelerações desiguais sobre a rolagem do usuário).
- Declarar a **Estratégia de Limpeza de Ciclo de Vida**: Uso obrigatório do hook `useGSAP()` no React ou escopo isolado via `gsap.context()`.

---

### Tabela de Mapeamento Técnico de Estados de Animação

| Componente da UI | Gatilho & Frequência | Plugin / Função GSAP | Propriedades Alvo | Curva & Duração / Scrub | Estratégia de Fallback (Reduced Motion) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Hero Title** | Montagem de Rota / Page Load | `SplitText` + `gsap.from()` | `yPercent: 120`, `autoAlpha: 0` $\rightarrow$ `0`, `1` | `ease: "power4.out"`, `duration: 1.2`, `stagger: 0.05` | `autoAlpha: 1`, `yPercent: 0` instantâneo sem stagger |
| **Product Showcase** | Rolagem Vertical (`ScrollTrigger`) | `ScrollTrigger(pin: true, scrub: 1)` | `xPercent: -200`, `scale: 1.05`, `filter: blur()` | `ease: "none"`, `end: "+=300%"` | Layout vertical flex comum em coluna sem pin |
| **Botão CTA Principal** | `pointermove` contínuo (120Hz) | `gsap.quickTo()` | `x`, `y` matricial no botão e no label interno | `ease: "power3.out"`, `duration: 0.6` | Desativação do listener; hover CSS estático tradicional |
| **Grid de Projetos** | Entrada na Viewport em Lote | `ScrollTrigger.batch()` | `autoAlpha`, `y: 40` $\rightarrow$ `0` | `ease: "power3.out"`, `duration: 0.8`, `stagger: 0.08` | Elementos renderizados estaticamente com `opacity: 1` |
| **Galeria / Filtro de Cards** | Mudança de Estado de Filtro DOM | `gsap/Flip` | Leitura de layout e interpolação matricial | `ease: "expo.out"`, `duration: 0.7`, `absolute: true` | Troca instantânea de nós sem transição geométrica |
| **Contorno de Diagrama** | Entrada de Seção Técnica | `DrawSVGPlugin` | `drawSVG: "0%"` $\rightarrow$ `drawSVG: "100%"` | `ease: "power2.out"`, `duration: 1.8` | Vetor totalmente traçado no estado inicial |

---

### Checklist de Pré-Voo de Engenharia de Movimento

Antes de aprovar e executar código GSAP em produção, a IA deve validar os 7 mandamentos de segurança:
1. **Registro Central de Plugins**: Todos os plugins utilizados foram registrados com `gsap.registerPlugin()` antes de qualquer execução?
2. **Escopo e Limpeza de SPAs**: Todas as timelines e triggers estão envelopados dentro de `useGSAP({ scope: containerRef })` ou `gsap.context()` para garantir o descarte completo (`revert()`) ao desmontar o componente no React/Next.js?
3. **Imunidade ao React 18/19 StrictMode**: O código está imune ao duplo disparo de montagem característico do React sem criar ScrollTriggers zumbis duplicados na memória?
4. **Isolamento de Conflito CSS**: Nenhum nó alvo de `gsap.to()` possui classes CSS concorrentes como `transition: all` ou `transition-transform` ativas?
5. **Ancestrais de Pin Limpos de Filtros**: Todos os elementos que utilizam `pin: true` possuem ancestrais no DOM isentos de `transform`, `filter` ou `backdrop-filter` que possam corromper o Bloco de Contenção de `position: fixed` (ou possuem a flag `pinReparent: true` declarada)?
6. **Controle de `prefers-reduced-motion`**: As animações estão envelopadas em `gsap.matchMedia()` para desativar scrubs pesados e pins caso o sistema do usuário solicite redução de movimento?
7. **Recálculo Pós-Carregamento**: O script invoca `ScrollTrigger.refresh()` logo após o carregamento assíncrono de imagens (`img.onload`), renderizações de fontes web (`document.fonts.ready`) ou requisições de dados?
