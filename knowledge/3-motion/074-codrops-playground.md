---
id: "codrops-playground"
name: "Codrops Playground (Experimental WebGL, Shaders & Creative Interactions)"
url: "https://tympanus.net/codrops/category/playground/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["DOM-to-WebGL Hybrid Sync", "Fluid Physics & Flowmaps", "Kinetic Typography Shaders", "Chromatic Dispersion & RGB Shift", "Infinite Toroidal Grids", "SVG Filter Displacement", "Organic Navier-Stokes Distortion"]
densidade_informacao: "Independente"
impacto_visual: "Cinematografico/Showstopper"
custo_computacional: "Alto (WebGL/GLSL/Three.js + Ping-Pong FBOs + Continuous RAF DOM Sync)"
stack_frameworks: ["Three.js", "Curtains.js", "OGL", "GSAP 3 (ScrollTrigger)", "Lenis / Locomotive Scroll", "GLSL (Custom Vertex/Fragment)", "React / React Three Fiber", "SVG Filters (feDisplacementMap)"]
compatibilidade:
  combinacoes_recomendadas: ["Lenis + Three.js Plane Sync", "GSAP ScrollTrigger + Custom GLSL Uniforms", "Curtains.js + WebGL Ping-Pong Flowmaps", "React Three Fiber + Drei View/Scissor", "SVG feDisplacementMap + GSAP Tween"]
  conflitos_esteticos: ["Múltiplos elementos canvas independentes competindo por contextos WebGL no mesmo documento (limite de 8-16 WebGLContexts por navegador)", "Overlays de distorção de fluidos sem desacoplamento de eventos de ponteiro (pointer-events: none quebrando cliques em formulários e botões)", "Animação de shaders com resolução nativa em telas Retina 3x sem capping de devicePixelRatio (estrangulamento de fill-rate na GPU)", "Uso de shaders invasivos em textos de leitura longa ou interfaces utilitárias de alta densidade de dados"]
---

# Codrops Playground — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)

O **Codrops Playground** (`https://tympanus.net/codrops/category/playground/`), concebido e mantido pela plataforma **Codrops** (fundada por Manoela Ilic e Pedro Botelho), é a mais influente incubadora e laboratório de computação gráfica criativa da web contemporânea. Desde o início da década de 2010, com contribuições marcantes de mestres do código criativo como Martin Laxenaire, Yuri Artiukh (Akella), Jesper Landberg, Robin Delaporte, Daniel Velasquez e Niccolò Miranda, o Playground antecipa e molda a linguagem estética que vence prêmios de prestígio internacional (Awwwards *Site of the Year*, FWA *Site of the Day*, D&AD Pencils).

Mais do que uma galeria de demonstrações visuais, o Codrops Playground estabeleceu o padrão de ouro para um dos desafios arquiteturais mais complexos da engenharia de interface: a **fusão transparente entre a árvore de layout estruturada do DOM e o pipeline de renderização acelerada por hardware de Shaders WebGL/WebGPU**.

```
┌───────────────────────────────────────────────────────────────────────────────┐
│              CODROPS HYBRID DOM-TO-WEBGL RUNTIME ARCHITECTURE                │
└───────────────────────────────────────────────────────────────────────────────┘
                                       │
                    Unified RAF Loop (Lenis / GSAP Tick)
                                       │
         ┌─────────────────────────────┴─────────────────────────────┐
         ▼                                                           ▼
┌─────────────────────────────┐                             ┌─────────────────────────────┐
│       HTML / CSS DOM        │                             │     OFFSCREEN / GPU PASS    │
│   (Semantic & Accessible)   │                             │    (Shared WebGL Canvas)    │
├─────────────────────────────┤                             ├─────────────────────────────┤
│ • <section class="hero">    │                             │ • Single Fullscreen <canvas>│
│ • <img class="gl-target">   │ getBoundingClientRect()     │ • Shared Perspective Camera │
│ • <h1 class="gl-text">      │────────────────────────────>│ • Quad Plane Meshes         │
│ • <a class="magnetic-btn">  │ [X, Y, Width, Height]       │ • World Units Projection    │
└─────────────────────────────┘                             └─────────────────────────────┘
                                                                           │
                                              ┌────────────────────────────┴────────────────────────────┐
                                              ▼                                                         ▼
                                 ┌─────────────────────────┐                               ┌─────────────────────────┐
                                 │   PHYSICS SIMULATION    │                               │   GLSL SHADER PIPELINE  │
                                 ├─────────────────────────┤                               ├─────────────────────────┤
                                 │ • Inertial Scroll Lerp  │                               │ • Vertex Mesh Ripple    │
                                 │ • Mouse Velocity Vector │───── Pass Uniforms ──────────>│ • Ping-Pong Flowmap FBO │
                                 │ • Spring Damping Forces │  (uTime, uVelocity, uProgress)│ • Multi-tap Chromatic   │
                                 │ • Audio Frequency FFT   │                               │ • Multiside Refraction  │
                                 └─────────────────────────┘                               └─────────────────────────┘
```

### Princípios Sensoriais e Físicos Fundamentais

1. **A Desconstrução da Rigidez Euclidiana da Janela do Navegador**:
   A web nativa é um arranjo cartesiano estático de retângulos ortogonais definidos por caixas CSS (`box-model`). Os experimentos do Codrops Playground subvertem essa frieza introduzindo propriedades físicas de matéria real: elasticidade viscosa, tensão superficial de fluidos, inércia mecânica, refração ótica e distorção de lentes ópticas analógicas. Uma imagem não é meramente trocada; ela se deforma pelo deslocamento da água, rasga-se em micro-partículas ou dobra-se sob a aceleração centrífuga do movimento do usuário.

2. **Projeção Câmera-Mundo de Precisão Pixel-Perfect (World-Unit Mapping)**:
   A sensação tátil dos experimentos decorre do alinhamento milimétrico entre o que o olho enxerga no HTML e o que a GPU calcula nos shaders. Ao ajustar a distância da câmera de perspectiva no eixo $Z$ em relação ao campo de visão (Field of View - FOV), a biblioteca WebGL (como Three.js ou Curtains.js) mapeia 1 unidade do mundo 3D diretamente para 1 pixel na tela:
   $$\text{Camera } Z = \frac{\text{Viewport Height}}{2 \cdot \tan\left(\frac{\text{FOV} \cdot \pi}{360}\right)}$$
   Esse acoplamento faz com que o plano WebGL coincida perfeitamente com a tag `<img>` subjacente, permitindo que a imagem HTML permaneça oculta (`opacity: 0`), enquanto o mesh 3D herda suas coordenadas exatas em tempo real, respondendo a rolagem, hover e redimensionamento.

3. **Reatividade Dinâmica à Velocidade e Inércia do Usuário**:
   Em vez de animações pré-gravadas e lineares, a física do Playground é dirigida por deltas dinâmicos de velocidade ($\Delta v = \text{scroll}_{target} - \text{scroll}_{current}$ ou $\|v_{mouse}\| = \sqrt{\Delta x^2 + \Delta y^2}$). Quando o usuário move o cursor rapidamente ou rola com força através de trackpads, os uniforms dos shaders recebem picos de impulso, manifestando aberração cromática (separação RGB), curvatura de lente barrel/pincushion e dissipação de ondas de choque hidrodinâmicas.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Seções e Experiências Insubstituíveis
- **Showcases de Portfólios e Agências Criativas (Awwwards / FWA Tier)**:
  Apresentação de estúdios de arquitetura, estúdios de design, diretores de cinema e marcas de moda de alta-costura, onde a própria interface digital é a prova de capacidade técnica e refinamento estético da marca.
- **Hero Sections de Produtos Flagship e Carros-Chefe Tecnológicos**:
  Lançamentos de consoles, hardware de ponta, fones de ouvido de luxo, superesportivos ou software de criatividade, utilizando distorção líquida controlada ou refração cáustica em tempo real para transformar o primeiro impacto do usuário em um momento memorável.
- **Galerias Interativas e Lookbooks Imersivos**:
  Carrosséis e grids infinitos com projeção toroidal e efeito de profundidade de campo (*depth-of-field blur*), onde imagens deslizam com inércia de amortecimento crítico e revelam detalhes microscópicos sob o foco do mouse.
- **Micro-interações de Prestígio (Magnetic Cursors & Gooey Elements)**:
  Botões primários de chamada para ação (CTA), seletores de filtros e menus de navegação flutuantes que se deformam elasticamente em direção ao ponteiro do mouse, transmitindo uma sensação de densidade física e feedback háptico simulado.

### O Papel na Regra 60-30-10
- **60% (Fundação Tipográfica e Estrutural Limpa)**:
  O layout da página permanece estruturado sobre um grid tipográfico robusto, semântico e com contraste visual perfeito. As tags HTML (`<article>`, `<header>`, `<h1>`, `<p>`, `<a>`) existem com acessibilidade completa, indexáveis por motores de busca e legíveis para tecnologias assistivas. Os shaders nunca substituem o HTML fundamental.
- **30% (Fluidez e Inércia Invisível)**:
  A mecânica invisível da rolagem suave (via `Lenis` ou motor de física similar), as interpolações com funções de amortecimento elástico de segunda ordem e as transições de foco. O movimento é suave, sem jank, criando a sensação de um aplicativo nativo em 120Hz.
- **10% (O Espetáculo Showstopper / Assinatura Codrops)**:
  O pico estético concentrado: o rastro de fluido interativo no header, a distorção por aberração cromática ao clicar em um card para abrir sua tela cheia, a refração volumétrica sobre uma tipografia monumental ou a dispersão por partículas de um modelo 3D. Este é o diferencial memorável que define a identidade visual do projeto.

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Quando Evitar
- **Sistemas Utilitários B2B de Alta Produtividade e Dashboards**:
  Aplicações financeiras, painéis médicos, consoles de telemetria, sistemas ERP e fluxos de checkout transacional. Nesses contextos, distorções de shader e inércia de rolagem provocam fricção operacional, reduzem a legibilidade imediata de números críticos e degradam a usabilidade.
- **Páginas Editoriais Densas de Leitura Contínua**:
  Documentações técnicas longas, artigos jornalísticos e e-readers. Distorções ópticas contínuas em áreas com texto corrido aumentam a fadiga ocular e podem induzir cinetose (*motion sickness*) em usuários sensíveis.
- **Dispositivos Móveis de Baixo Custo / Bateria em Modo de Economia**:
  Smartphones equipados com SoCs de entrada (GPUs integradas de baixa largura de banda de memória). Executar simulações contínuas de Navier-Stokes em Frame Buffer Objects (FBO) drena a bateria drasticamente e provoca quedas drásticas de framerate (< 20 fps).

### ⚠️ Regras Rígidas de GPU, Acessibilidade e Engenharia de Produção

1. **Capping Obrigatório de `devicePixelRatio`**:
   Telas modernas de smartphones e notebooks chegam a $3\times$ de densidade de pixels. Renderizar um canvas fullscreen em escala $3\times$ exige que a GPU calcule $9\times$ mais fragmentos por frame, resultando em sobrecarga térmica e throttling:
   ```typescript
   // REGRA DE OURO CODROPS: Limitar DPR a 2.0 no máximo absoluto
   const pixelRatio = Math.min(window.devicePixelRatio || 1, 2);
   renderer.setPixelRatio(pixelRatio);
   ```

2. **Acessibilidade Universal Obrigatória (`prefers-reduced-motion`)**:
   Quando a preferência de redução de movimento estiver ativa no sistema operacional, os passes de pós-processamento, distorções ondulatórias e scrubs contínuos de shaders devem ser completamente neutralizados:
   ```typescript
   const prefersReducedMotion = window.matchMedia("(prefers-reduced-motion: reduce)").matches;
   if (prefersReducedMotion) {
     // Desative simulações de fluidos e passe uniforms nulos aos shaders
     material.uniforms.uDisplacementStrength.value = 0.0;
     material.uniforms.uVelocityStrength.value = 0.0;
   }
   ```

3. **Arquitetura de Canvas Único (The Single Canvas Shared Pattern)**:
   Criar múltiplos elementos `<canvas>` WebGL na mesma página para animar diferentes cards é um anti-padrão grave: navegadores modernos limitam o contexto WebGL entre 8 e 16 instâncias. Atingido o limite, os primeiros canvas perdem o contexto silenciosamente. O padrão correto consiste em ter **um único canvas fullscreen transparente com posição `fixed`**, projetando todos os planos e meshes sobre as posições dos elementos HTML através de `scissor test` ou cálculo de posições relativas.

4. **Gerenciamento de Ciclo de Vida da VRAM e Prevenção de Memory Leaks**:
   Cada textura, geometria e render target criado aloca memória na GPU que **não é coletada automaticamente pelo Garbage Collector do JavaScript**:
   ```typescript
   function disposeMesh(mesh: THREE.Mesh) {
     mesh.geometry.dispose();
     if (Array.isArray(mesh.material)) {
       mesh.material.forEach((mat) => disposeMaterial(mat));
     } else {
       disposeMaterial(mesh.material);
     }
   }

   function disposeMaterial(material: THREE.Material) {
     Object.keys(material).forEach((key) => {
       const prop = (material as any)[key];
       if (prop && typeof prop.dispose === "function") {
         prop.dispose();
       }
     });
     material.dispose();
   }
   ```

5. **Tratamento Resiliente de Perda de Contexto WebGL (`webglcontextlost`)**:
   Em dispositivos móveis sob alta concorrência de memória, o sistema operacional pode revogar o contexto WebGL a qualquer momento:
   ```typescript
   canvas.addEventListener("webglcontextlost", (event) => {
     event.preventDefault();
     cancelAnimationFrame(rafId);
     console.warn("Contexto WebGL perdido. Alternando para fallbacks CSS.");
   }, false);

   canvas.addEventListener("webglcontextrestored", () => {
     initWebGLPipeline();
   }, false);
   ```

---

## 4. Catálogo Detalhado de Efeitos, Primitivas e Padrões de Animação

Abaixo estão descritos os 10 efeitos e arquiteturas mais emblemáticos desenvolvidos e popularizados no Codrops Playground:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        CODROPS PLAYGROUND SHADER CATALOG                               │
└────────────────────────────────────────────────────────────────────────────────────────┘
 [01] DOM-to-WebGL Synced Mesh    [02] Fluid Flowmap (Ping-Pong)  [03] Kinetic Scroll Pinch
 ┌─────────────┐                  ┌─────────────┐                 ┌─────────────┐
 │ <img> (DOM) │                  │  Mouse Drag │                 │Scroll Speed │
 │      │      │                  │      │      │                 │      │      │
 │      ▼      │                  │      ▼      │                 │      ▼      │
 │PlaneMesh(GL)│                  │Navier-Stokes│                 │RGB Split +  │
 │  Position   │                  │ FBO Flowmap │                 │Barrel Distor│
 └─────────────┘                  └─────────────┘                 └─────────────┘
 [04] Toroidal 3D Grid            [05] SVG Filter Turbulence      [06] MSDF Kinetic Ribbon
 ┌─────────────┐                  ┌─────────────┐                 ┌─────────────┐
 │Infinite Loop│                  │feDisplaceMap│                 │ Signed Dist │
 │x = mod(x, W)│                  │feTurbulence │                 │ 3D Cylinder │
 │Perspective  │                  │ DOM Ripple  │                 │ Text Twist  │
 └─────────────┘                  └─────────────┘                 └─────────────┘
 [07] Shared Element Transition   [08] Dynamic Glass Refraction   [09] Magnetic Cursor Vortex
 ┌─────────────┐                  ┌─────────────┐                 ┌─────────────┐
 │ Card Click  │                  │Transmissive │                 │Centroid Pull│
 │      │      │                  │ Mesh + Bkg  │                 │Hooke Spring │
 │      ▼      │                  │ Snell Refrac│                 │Pixel Swirl  │
 │FullscreenGL │                  │  Dispersion │                 │   Canvas    │
 └─────────────┘                  └─────────────┘                 └─────────────┘
```

### 1. DOM-to-WebGL Synchronized Plane Mesh (Padrão Curtains.js / Three.js)
- **Comportamento Visual**:
  - *Estado Inicial*: Uma grade regular de cards HTML/CSS renderiza imagens padrão. Na GPU, planos poligonais equivalentes (`PlaneGeometry(1, 1, 32, 32)`) ocupam exatamente o mesmo espaço físico na viewport em relação ao scroll.
  - *Durante a Transição*: No hover ou scroll rápido, o mesh WebGL executa uma animação de deslocamento senoidal nos vértices e ondulação no fragment shader. A tag `<img>` original permanece com opacidade zero.
  - *Repouso*: O mesh WebGL estabiliza-se e as coordenadas batem milimetricamente com a posição do card na árvore DOM.
- **Gatilho**: Eventos de rolagem (`scroll` via Lenis ou RAF loop) e mutação de tamanho de janela (`resize`), recalculando `element.getBoundingClientRect()`.

### 2. Mouse-Driven Liquid / Wave Distortion via Flowmap & Ping-Pong FBO
- **Comportamento Visual**:
  - *Estado Inicial*: A imagem ou fundo repousa com nitidez cristalina e reflexos limpos.
  - *Durante a Transição*: Conforme o ponteiro do mouse se move sobre o elemento, uma perturbação líquida dinâmica se propaga. O rastro do mouse gera vetores de velocidade que distorcem as coordenadas UV da textura. Ondas concêntricas dissipam-se suavemente ao longo do tempo como gotas em uma lâmina d'água.
  - *Repouso*: A turbulência se dissipa exponencialmente devido a um fator de decaimento viscoso ($\text{decay} \approx 0.96$), retornando à textura original sem marcas residuais.
- **Gatilho**: Evento contínuo `pointermove` alimentando um Frame Buffer duplo (Ping-Pong) que armazena vetores de momento e dissipa energia a cada frame do RAF.

### 3. Kinetic Inertial Scroll Distortion (RGB Split & Directional Barrel Pinch)
- **Comportamento Visual**:
  - *Estado Inicial*: Os elementos do catálogo ou portfólio encontram-se perfeitamente retos e com cores equilibradas.
  - *Durante a Transição*: Quando o usuário acelera a rolagem do mouse ou dispara um flick no trackpad, toda a cena sofre um abaulamento ótico proporcional à velocidade ($\text{speed} = |\Delta y| / \Delta t$). As cores sofrem aberração cromática: o canal vermelho desloca-se ligeiramente para cima/fora, o verde permanece no centro e o azul desloca-se na direção oposta, simulando a refração imperfeita de lentes fotográficas vintage de alta abertura.
  - *Repouso*: Conforme a inércia da rolagem desacelera até zero, o efeito de abaulamento e a separação cromática convergem organicamente para repouso absoluto.
- **Gatilho**: Variação da velocidade de rolagem derivada do motor de smooth-scroll (Lenis / ScrollTrigger).

### 4. Infinite 3D Wrapping Multi-Axis Grid (Toroidal Coordinate Projection)
- **Comportamento Visual**:
  - *Estado Inicial*: Uma galeria bidimensional de imagens cobrindo um plano tridimensional com leve inclinação de câmera (e.g. rotação de -15° no eixo X e 10° no eixo Y).
  - *Durante a Transição*: O usuário clica e arrasta ou usa a rolagem para navegar indefinidamente em qualquer direção ($X$ ou $Y$). Ao cruzar a borda visível da viewport, cada card é instantaneamente reposicionado na borda oposta usando aritmética modular toroidal:
    $$x_{\text{wrapped}} = ((x + W/2) \pmod W) - W/2$$
    Durante o arrasto rápido, a câmera 3D recua no eixo Z (zoom-out inercial) e os cards curvam-se no plano como se estivessem em uma superfície cilíndrica.
  - *Repouso*: Ao soltar o cursor, uma mola física suave desacelera a grade e a câmera retorna ao seu plano focal primário.
- **Gatilho**: Eventos de `pointerdown`, `pointermove`, `pointerup` com cálculo de inércia vetorial.

### 5. SVG Filter Liquid Ripple & Gooey Morphing (`feDisplacementMap` + `feTurbulence`)
- **Comportamento Visual**:
  - *Estado Inicial*: Botões, tipografias ou imagens puramente HTML/SVG com contornos nítidos.
  - *Durante a Transição*: No hover de um link ou clique em um botão, um filtro SVG inline aplica deformações orgânicas líquidas diretamente aos elementos DOM sem exigir canvas WebGL. A base de ruído fractal de `feTurbulence` tem seus atributos `baseFrequency` e `scale` interpolados via GSAP, criando o efeito de uma gota de mercúrio que treme e se reorganiza elasticamente.
  - *Repouso*: O filtro estabiliza-se em `scale="0"` ou o elemento adota sua forma expandida com bordas perfeitamente nítidas.
- **Gatilho**: Interação de cursor `mouseenter` / `mouseleave` ou acionamento programático via timeline GSAP.

### 6. Kinetic Typography Shaders (MSDF & Ribbons Cilíndricas Tridimensionais)
- **Comportamento Visual**:
  - *Estado Inicial*: Títulos editoriais de grande escala dispostos como fitas tipográficas tridimensionais curvadas em arcos senoidais ou cilindros espirais.
  - *Durante a Transição*: O texto é renderizado utilizando fontes MSDF (*Multi-channel Signed Distance Field*), garantindo nitidez absoluta em qualquer nível de zoom ou perspectiva oblíqua. No scroll ou movimento do mouse, os vértices da fita ondulam no espaço tridimensional e as letras sofrem torção cinética (*torsional twist*), passando por trás e pela frente de outros elementos da interface.
  - *Repouso*: A fita tipográfica mantém uma rotação orbital sutil em loop contínuo a 60fps.
- **Gatilho**: Loop contínuo com offset de tempo `uTime` e modulação de amplitude por scroll progress.

### 7. Seamless Shared Element Page Transition com WebGL Mesh Expansion
- **Comportamento Visual**:
  - *Estado Inicial*: Uma imagem miniatura reside dentro de um card em uma grade de projetos, ocupando por exemplo 350px × 220px.
  - *Durante a Transição*: Ao clicar no card, em vez de um reload convencional de página, o mesh WebGL associado ao card desacopla-se de sua restrição de layout e expande-se suavemente para cobrir 100% da viewport (modo tela cheia Hero), enquanto a nova rota de conteúdo é montada assincronamente em segundo plano. Durante a expansão, um shader de ruído perlin dissolve as bordas e revela o layout detalhado do projeto.
  - *Repouso*: A transição conclui-se; o mesh WebGL transfere o estado visual de volta para a tag `<img>` em tamanho real da página de destino ou mantém a renderização WebGL nativa.
- **Gatilho**: Evento de clique em âncora de navegação integrado com Next.js App Router / Barba.js / View Transitions API.

### 8. Multi-Pass Real-Time Glass Refraction & Chromatic Dispersion
- **Comportamento Visual**:
  - *Estado Inicial*: Um painel de navegação, modal flutuante ou objeto 3D de geometria orgânica paira sobre o conteúdo da página com aparência de vidro de quartzo translúcido de espessura volumétrica real.
  - *Durante a Transição*: Diferente do `backdrop-filter: blur()` convencional do CSS, o shader realiza uma amostragem direta da cena subjacente através da Lei de Refração de Snell ($n_1 \sin \theta_1 = n_2 \sin \theta_2$), distorcendo a tipografia e as cores que passam por trás do painel. A luz sofre dispersão cromática baseada na fórmula de Cauchy: o índice de refração varia em função do comprimento de onda, decompondo os feixes luminosos nas cores do arco-íris ao longo das bordas angulares do objeto.
  - *Repouso*: O objeto refrata a cena estática com cáusticas dinâmicas moduladas por um ruído de Voronoi suave.
- **Gatilho**: Render pass de textura de background capturada em um FBO (`WebGLRenderTarget`) e projetada no material de transmissão.

### 9. Magnetic Cursor Centroid com Rastro Elástico e Vórtice GLSL
- **Comportamento Visual**:
  - *Estado Inicial*: Um ponteiro customizado minimalista (ponto circular de 6px a 8px) segue o cursor do sistema operacional.
  - *Durante a Transição*: Ao se aproximar de um botão ou link interativo (dentro de um raio de atração de ~80px), o cursor é atraído magneticamente em direção ao baricentro do elemento através de uma força de Hooke com amortecimento. Concomitantemente, um canvas GLSL transparente sob o botão deforma seus pixels subjacentes em um micro-vórtice gravitacional. O botão em si sofre uma leve translação elástica na direção do cursor ($20\%$ do deslocamento).
  - *Repouso*: O cursor repousa ancorado no centro do botão; ao quebrar o raio de atração pelo movimento rápido, ele se descola com efeito elástico e retorna à escala normal.
- **Gatilho**: `pointermove` monitorando distâncias euclidianas relativas aos botões registrados no DOM.

### 10. Audio-Reactive Particle Swarm com Curl Noise & FBO GPGPU
- **Comportamento Visual**:
  - *Estado Inicial*: Uma nuvem etérea composta por centenas de milhares de micro-partículas flutua harmoniosamente em um campo vetorial de ruído turbulento (*Curl Noise*).
  - *Durante a Transição*: Ao reproduzir uma trilha sonora ou vídeo com áudio na experiência, a API `AudioContext` com `AnalyserNode` decompõe o espectro de frequências (Fast Fourier Transform - FFT). Frequências graves (Bass: 20Hz-120Hz) modulam a amplitude de expansão radial da nuvem; agudos (Treble: 4kHz-16kHz) induzem centelhamento e aceleração caótica nas partículas através de cálculo puramente em GPU (GPGPU via texturas de posição/velocidade).
  - *Repouso*: As partículas retornam à convergência fluida inicial ao silenciar o áudio.
- **Gatilho**: Eventos de streaming de áudio e dados do analisador FFT injetados no render loop do WebGL.

---

## 5. Matemática do Movimento & Receitas de Código

### Parâmetros Físicos, Equações e Curvas Notáveis

#### 1. Projeção de Coordenadas Viewport para Normalized Device Coordinates (NDC)
Para sincronizar nós do DOM em pixels com coordenadas do Vertex Shader WebGL ($[-1, 1]$):
$$x_{\text{ndc}} = \left(\frac{x_{\text{pixel}}}{\text{Viewport Width}}\right) \cdot 2.0 - 1.0$$
$$y_{\text{ndc}} = -\left(\left(\frac{y_{\text{pixel}}}{\text{Viewport Height}}\right) \cdot 2.0 - 1.0\right)$$

#### 2. Amortecimento de Inércia Hidrodinâmica (Lerp de Primeira Ordem)
Para atenuar a velocidade de scroll e movimento de ponteiro suavemente a cada frame:
$$v_{t} = v_{t-1} + (v_{\text{target}} - v_{t-1}) \cdot \lambda \quad (\text{onde } \lambda \in [0.08, 0.15] \text{ para sensação aquosa})$$

#### 3. Separação de Fase de Aberração Cromática nos Três Canais RGB
No fragment shader, a amostragem da textura com distorção por vetor de deslocamento $\vec{D}$:
$$\vec{UV}_R = \vec{UV} + \vec{D} \cdot (1.0 + \delta_{\text{spread}})$$
$$\vec{UV}_G = \vec{UV} + \vec{D}$$
$$\vec{UV}_B = \vec{UV} + \vec{D} \cdot (1.0 - \delta_{\text{spread}})$$

#### 4. Curvas de Interpolação Recomendadas
- **Snappy Kinetic Out**: `cubic-bezier(0.16, 1, 0.3, 1)` (Transições de expansão e abertura de telas cheias).
- **Inertial Liquid Glide**: `cubic-bezier(0.25, 0.46, 0.45, 0.94)` (Desaceleração de grades contínuas).
- **Mola de Amortecimento Crítico**: `stiffness: 180`, `damping: 24`, `mass: 1.0` (Movimento do cursor magnético).

---

### Receita de Produção: DOM-to-WebGL Image Distortion com RGB Split & Inércia

Abaixo está uma implementação completa, moderna e autossuficiente em **React com TypeScript**, utilizando **Three.js** e **GLSL Shaders nativos**. Ela implementa o padrão clássico do Codrops Playground: um plano WebGL sincronizado pixel a pixel sobre uma imagem DOM, que sofre ondulação líquida, curvatura direcional de rolagem e aberração cromática proporcional à velocidade de rolagem.

```tsx
/**
 * Codrops-Inspired DOM-to-WebGL Synchronized Image with Liquid Shader
 * Stack: React + TypeScript + Three.js + GLSL
 */

import React, { useEffect, useRef } from "react";
import * as THREE from "three";

// ============================================================================
// 1. GLSL SHADER DEFINITIONS
// ============================================================================

const vertexShader = /* glsl */ `
  uniform float uTime;
  uniform float uVelocity;
  uniform vec2 uHover;
  uniform float uHoverStrength;

  varying vec2 vUv;
  varying float vWave;

  void main() {
    vUv = uv;

    vec3 pos = position;

    // Distorção senoidal nos vértices proporcional à velocidade do scroll
    float scrollWave = sin(pos.y * 3.0 + uTime * 2.0) * (uVelocity * 0.05);
    
    // Deformação pontual ao redor da posição do hover
    float distToHover = distance(uv, uHover);
    float hoverEffect = sin(distToHover * 15.0 - uTime * 4.0) * exp(-distToHover * 4.0) * uHoverStrength;

    pos.z += scrollWave + (hoverEffect * 20.0);
    vWave = scrollWave + hoverEffect;

    gl_Position = projectionMatrix * modelViewMatrix * vec4(pos, 1.0);
  }
`;

const fragmentShader = /* glsl */ `
  uniform sampler2D uTexture;
  uniform float uTime;
  uniform float uVelocity;
  uniform float uHoverStrength;
  uniform vec2 uResolution;
  uniform vec2 uTextureResolution;

  varying vec2 vUv;
  varying float vWave;

  // Função para manter aspect-ratio idêntico ao "object-fit: cover" do CSS
  vec2 getCoverUv(vec2 uv, vec2 screenRes, vec2 texRes) {
    vec2 ratio = vec2(
      min((screenRes.x / screenRes.y) / (texRes.x / texRes.y), 1.0),
      min((screenRes.y / screenRes.x) / (texRes.y / texRes.x), 1.0)
    );
    return uv * ratio + (1.0 - ratio) * 0.5;
  }

  void main() {
    vec2 coverUv = getCoverUv(vUv, uResolution, uTextureResolution);

    // Vetor de distorção baseado no deslocamento da onda
    vec2 distortion = vec2(vWave * 0.04, vWave * 0.02);

    // Aberração Cromática: Amostragem individual dos canais R, G e B
    float rgbSpread = 0.02 * (abs(uVelocity) * 0.5 + uHoverStrength);
    
    float r = texture2D(uTexture, coverUv + distortion + vec2(rgbSpread, 0.0)).r;
    float g = texture2D(uTexture, coverUv + distortion).g;
    float b = texture2D(uTexture, coverUv + distortion - vec2(rgbSpread, 0.0)).b;

    // Toque sutil de vinheta nas bordas durante a deformação
    float vignette = smoothstep(0.8, 0.2, length(vUv - 0.5));
    vec3 color = vec3(r, g, b) + (abs(vWave) * 0.15 * vignette);

    gl_FragColor = vec4(color, 1.0);
  }
`;

// ============================================================================
// 2. REACT COMPONENT
// ============================================================================

interface CodropsImageProps {
  src: string;
  alt: string;
  className?: string;
}

export const CodropsImage: React.FC<CodropsImageProps> = ({ src, alt, className = "" }) => {
  const containerRef = useRef<HTMLDivElement | null>(null);
  const imgRef = useRef<HTMLImageElement | null>(null);
  const canvasRef = useRef<HTMLCanvasElement | null>(null);

  useEffect(() => {
    const container = containerRef.current;
    const img = imgRef.current;
    const canvas = canvasRef.current;
    if (!container || !img || !canvas) return;

    // Verificação de acessibilidade: Prefers Reduced Motion
    const prefersReducedMotion = window.matchMedia("(prefers-reduced-motion: reduce)").matches;

    // 1. SETUP DE CENA, CÂMERA E RENDERER
    const scene = new THREE.Scene();

    // Câmera ortográfica de projeção pixel-to-world
    const fov = 45;
    const camera = new THREE.PerspectiveCamera(fov, 1, 0.1, 1000);
    
    const renderer = new THREE.WebGLRenderer({
      canvas,
      alpha: true,
      antialias: true,
      powerPreference: "high-performance",
    });

    const dpr = Math.min(window.devicePixelRatio || 1, 2);
    renderer.setPixelRatio(dpr);

    // 2. TEXTURA E UNIFORMS
    const textureLoader = new THREE.TextureLoader();
    const texture = textureLoader.load(src, (loadedTex) => {
      // Atualizar resolução da imagem para cálculo do object-fit cover
      material.uniforms.uTextureResolution.value.set(
        loadedTex.image.naturalWidth,
        loadedTex.image.naturalHeight
      );
    });
    texture.generateMipmaps = true;
    texture.minFilter = THREE.LinearMipmapLinearFilter;

    const uniforms = {
      uTexture: { value: texture },
      uTime: { value: 0 },
      uVelocity: { value: 0 },
      uHover: { value: new THREE.Vector2(0.5, 0.5) },
      uHoverStrength: { value: 0 },
      uResolution: { value: new THREE.Vector2(1, 1) },
      uTextureResolution: { value: new THREE.Vector2(1, 1) },
    };

    const geometry = new THREE.PlaneGeometry(1, 1, 48, 48);
    const material = new THREE.ShaderMaterial({
      vertexShader,
      fragmentShader,
      uniforms,
      transparent: true,
    });

    const mesh = new THREE.Mesh(geometry, material);
    scene.add(mesh);

    // 3. SINCRONIZAÇÃO DE GEOMETRIA COM O DOM
    const updateBounds = () => {
      const rect = container.getBoundingClientRect();
      const width = rect.width;
      const height = rect.height;

      renderer.setSize(width, height);
      uniforms.uResolution.value.set(width, height);

      camera.aspect = width / height;
      // Posicionar a câmera de forma que 1 unidade 3D = 1 pixel na tela
      const cameraDistance = height / 2 / Math.tan((fov * Math.PI) / 360);
      camera.position.z = cameraDistance;
      camera.updateProjectionMatrix();

      // Ajustar a escala da malha para preencher o container exatamente
      mesh.scale.set(width, height, 1);
    };

    updateBounds();
    window.addEventListener("resize", updateBounds);

    // 4. FÍSICA DE INTERAÇÃO (Scroll e Hover)
    let lastScrollY = window.scrollY;
    let currentScrollVelocity = 0;
    let targetHoverStrength = 0;
    let currentHoverStrength = 0;

    const handleMouseMove = (e: MouseEvent) => {
      if (prefersReducedMotion) return;
      const rect = container.getBoundingClientRect();
      const x = (e.clientX - rect.left) / rect.width;
      const y = 1.0 - (e.clientY - rect.top) / rect.height;
      uniforms.uHover.value.set(x, y);
    };

    const handleMouseEnter = () => {
      if (!prefersReducedMotion) targetHoverStrength = 1.0;
    };

    const handleMouseLeave = () => {
      targetHoverStrength = 0.0;
    };

    container.addEventListener("mousemove", handleMouseMove);
    container.addEventListener("mouseenter", handleMouseEnter);
    container.addEventListener("mouseleave", handleMouseLeave);

    // 5. RENDER LOOP COM INTERPOLAÇÃO (LERP)
    let animationFrameId: number;
    let clock = new THREE.Clock();

    const renderLoop = () => {
      const elapsedTime = clock.getElapsedTime();

      // Cálculo de velocidade de scroll instantânea
      const currentScrollY = window.scrollY;
      const deltaScroll = currentScrollY - lastScrollY;
      lastScrollY = currentScrollY;

      // Amortecimento inercial (Lerp)
      currentScrollVelocity += (deltaScroll - currentScrollVelocity) * 0.1;
      currentHoverStrength += (targetHoverStrength - currentHoverStrength) * 0.08;

      if (!prefersReducedMotion) {
        uniforms.uTime.value = elapsedTime;
        uniforms.uVelocity.value = currentScrollVelocity;
        uniforms.uHoverStrength.value = currentHoverStrength;
      }

      renderer.render(scene, camera);
      animationFrameId = requestAnimationFrame(renderLoop);
    };

    animationFrameId = requestAnimationFrame(renderLoop);

    // 6. TEARDOWN E DESALOCAÇÃO DE MEMÓRIA (VRAM CLEANUP)
    return () => {
      cancelAnimationFrame(animationFrameId);
      window.removeEventListener("resize", updateBounds);
      container.removeEventListener("mousemove", handleMouseMove);
      container.removeEventListener("mouseenter", handleMouseEnter);
      container.removeEventListener("mouseleave", handleMouseLeave);

      geometry.dispose();
      material.dispose();
      texture.dispose();
      renderer.dispose();
    };
  }, [src]);

  return (
    <div
      ref={containerRef}
      className={`relative overflow-hidden cursor-pointer select-none ${className}`}
      style={{ minHeight: "360px", borderRadius: "12px" }}
    >
      {/* Imagem semântica acessível para leitores de tela e SEO (oculta visualmente) */}
      <img
        ref={imgRef}
        src={src}
        alt={alt}
        className="w-full h-full object-cover opacity-0 pointer-events-none absolute inset-0"
        loading="lazy"
      />
      {/* Canvas WebGL onde a malha distorcida é renderizada com aceleração de GPU */}
      <canvas ref={canvasRef} className="absolute inset-0 w-full h-full pointer-events-none" />
    </div>
  );
};
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma experiência de interface inspirada nos experimentos do **Codrops Playground**, o Arquiteto de Software e Engenheiro Criativo deve formalizar os seguintes pontos na especificação técnica do projeto:

### 1. Declaração Formal da Estrutura Híbrida DOM-WebGL
- **Identificação dos Nós Alvo**: Listar expressamente quais elementos do layout HTML (`hero-image`, `project-card-thumbnail`, `global-background`) receberão projeção e sincronização por malhas WebGL.
- **Topologia de Contextos WebGL**: Declarar o uso do padrão **Single Fullscreen Canvas**. Rejeitar terminantemente múltiplos `<canvas>` fragmentados para evitar o estouro do limite de contextos do navegador.
- **Definição de Coordenadas de Projeção**: Especificar o algoritmo de sincronização (`getBoundingClientRect()` acoplado ao render loop de um smooth-scroller com virtual scroll desativado ou compensado).

### 2. Orçamento de Performance Gráfica (Performance Budget)
- **Teto de Resolução (DPR Cap)**: Fixar `Math.min(devicePixelRatio, 2.0)` em todo o pipeline.
- **Orçamento de VRAM**: Não exceder 60MB totais em texturas na GPU. Utilizar compressão de texturas KTX2/Basis Universal para assets de alta resolução e mipmapping padrão linear.
- **Frame Budget**: Shaders de fragmentos devem manter o tempo de renderização abaixo de **4ms por frame** para garantir folga operacional para os 60fps/120fps nativos.

### 3. Matriz de Acessibilidade e Fallback Progressivo
- **Checklist `prefers-reduced-motion`**:
  - Quando ativo, zerar imediatamente `uVelocity` e amplitudes de distorção.
  - Alternar a opacidade das tags `<img>` e `<p>` originais do DOM para `1.0` e desativar o loop de renderização RAF do WebGL para preservar ciclos de CPU/GPU.
- **Fallback para WebGL Context Loss**:
  - Configurar ouvintes para `webglcontextlost`, exibindo a camada HTML/CSS estática com transições CSS nativas caso a GPU revogue o contexto em dispositivos com memória escassa.
- **Estratégia para Touch Devices**:
  - Em telas touch (`(pointer: coarse)`), suprimir efeitos contínuos de hover de mouse e substituir a física de fluido contínua por deformações pontuais e sutis disparadas exclusivamente no evento `touchstart`.
