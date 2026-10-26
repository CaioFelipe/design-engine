---
id: "shaders-com"
name: "Shaders.com (Shader Effects Inc.)"
url: "https://shaders.com/"
category: "4-shaders-3d"
schema_type: "B-motion-shaders"
dna_estetico: ["Procedural WebGPU/WebGL", "Domain Warping & FBM Fluidity", "Optical Dispersion & Chromatic Aberration", "Glass Refraction & Liquid Surfaces", "Procedural Dithering & Halftones", "Pointer & Audio Reactive Fields"]
densidade_informacao: "Independente"
impacto_visual: "Cinematografico/Showstopper"
custo_computacional: "Medio (Shaders 2D Otimizados) a Alto (Raymarching SDF / Ping-Pong FBOs)"
stack_frameworks: ["WebGPU (WGSL)", "WebGL 2.0 / 1.0 (GLSL)", "React (shaders/react)", "Vue (shaders/vue)", "Svelte (shaders/svelte)", "Solid (shaders/solid)", "Vanilla JavaScript / Canvas API", "Framer Plugin"]
compatibilidade:
  combinacoes_recomendadas: ["shaders/react + Tailwind CSS v4", "WebGL Fullscreen Quad + Lenis Smooth Scroll", "Shaders Canvas + Framer Motion (HUD Overlays)", "WebGPU Procedural Backing + Radix UI / Shadcn Semantic DOM"]
  conflitos_esteticos: ["Sobreposição de múltiplos shaders com alta frequência visual competindo com texto de baixa luminância", "Execução contínua de fragment shaders pesados em viewports fora de tela sem IntersectionObserver", "Uso indiscriminado de raymarching 3D não-otimizado em dispositivos móveis sem throttling de DPR"]
---

# Shaders.com — Dossiê de Shaders Procedurais, Física Visual WebGPU/WebGL & Engenharia Generativa

## 1. Filosofia de Movimento & Sensação Física (Feel)

O **Shaders.com** (`https://shaders.com/`), desenvolvido pela **Shader Effects Inc.**, representa uma das mais importantes viradas paradigmáticas na Creative Technology e na engenharia de interface contemporânea: a **democratização e componentização da computação gráfica em nível de fragmento (per-pixel shading)**. Historicamente, a integração de shaders GLSL em websites exigia a montagem manual de pipelines WebGL áridos, gerenciamento complexo de buffers VBO/IBO, controle de contextos gráficos, cálculos de projeção matricial e boilerplates densos em bibliotecas de cena como Three.js ou Babylon.js. O Shaders.com rompe essa barreira ao encapsular o poder de processamento massivo e paralelo da GPU moderna (WebGPU e WebGL) em **componentes declarativos, empilháveis e reativos** para os principais ecossistemas da web (`React`, `Vue`, `Svelte`, `Solid` e `Vanilla JS`).

A filosofia central do Shaders.com reside na **intersecção entre a física óptica real e a matemática procedural generativa**:

1. **A Matéria Digital Contínua (Da Geometria Discreta ao Campo Contínuo)**:
   Enquanto o modelo 3D poligonal tradicional depende de vértices, malhas geométricas (*meshes*) e pipelines de rasterização que subdividem o espaço em triângulos discretos, o Shaders.com ancora-se na renderização por campo de distância e ruído analítico sobre uma primitiva elementar: o **Fullscreen Quad (dois triângulos formando um retângulo que cobre exatamente a tela)**. Toda a ilusão de profundidade tridimensional, fluidez viscosa, refração cáustica e turbulência surge do cálculo puramente matemático executado em paralelo para cada um dos milhões de fragmentos de tela a 60fps ou 120fps.

2. **Reatividade e Inércia Tátil (Pointer, Audio & Time Coupling)**:
   Os efeitos não são vídeos pré-renderizados nem loops cíclicos estáticos. Eles respondem instantaneamente a perturbações do ambiente: o arrasto inercial do ponteiro do mouse gera convecção em campos de gradiente de cor; a velocidade de rolagem da página induz aberração cromática nas bordas; frequências de áudio modulam a escala de ruído fractal. O usuário percebe a tela não como vidro inerte, mas como uma **membrana fluida ativa**, com densidade, viscosidade e índice de refração dinâmico.

3. **Arquitetura Dual-Engine: WebGPU First com Fallback Transparente WebGL**:
   O Shaders.com lidera o salto tecnológico em direção à **WebGPU (WGSL)**, eliminando o gargalo de validação de chamadas de desenho (*draw calls*) da CPU e liberando o uso de compute shaders e precisão em ponto flutuante de 32 bits nativa. Ao mesmo tempo, mantém compatibilidade universal através de um compilador/transpilador interno com fallback automático para WebGL 2.0 e WebGL 1.0 (GLSL ES 1.00 / 3.00), assegurando que o usuário final nunca encontre uma tela em branco em GPUs legadas ou navegadores em transição.

---

### Pipeline Visual: Da Camada Declarativa ao Pipeline da GPU

Abaixo é ilustrado o ciclo de vida e a arquitetura de processamento em camadas promovida pelo Shaders.com:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                 ARQUITETURA DE PIPELINE: SHADERS.COM ECOSYSTEM              │
└─────────────────────────────────────────────────────────────────────────────┘

  [APLICAÇÃO REACT / VUE / SVELTE]
    │
    │  <Shader className="relative w-full h-screen">
    │    <MeshGradient colors={['#101014', '#1E1B4B', '#4338CA']} />
    │    <DomainWarping frequency={1.8} distortion={0.45} />
    │    <FlutedGlass roughness={0.12} refraction={1.45} />
    │    <CursorTrail decay={0.88} intensity={1.5} />
    │  </Shader>
    │
    ▼
  [SHADERS RUNTIME ENGINE]
    ├── Detecção de Capacidade de Hardware (WebGPU API vs WebGL 2.0 vs WebGL 1.0)
    ├── Sincronização de Uniforms Globais via requestAnimationFrame (RAF):
    │     • u_time (delta elapsed)
    │     • u_resolution (canvas width, canvas height)
    │     • u_mouse (interpolated mouse position x, y)
    │     • u_velocity (pointer delta / time)
    │     • u_dpr (clamped devicePixelRatio)
    ├── Intersection Observer (Pausa RAF automática quando fora do Viewport)
    └── Ping-Pong FBO Manager (Gerenciamento de texturas offscreen para persistência/advecção)
          │
          ├───────────────────────────────┬───────────────────────────────┐
          ▼                               ▼                               ▼
   [PASS 1: GENERATIVE]           [PASS 2: OPTICAL]             [PASS 3: POST-PROCESS]
   Geração Procedural             Deformação e Refração         Dithering, Halftone,
   (FBM, Mesh Gradient,           (Liquid Glass, Aberration,    Film Grain e Tone
   Worley Noise, Fluid Field)     Displacement Maps)            Mapping para sRGB
          │                               │                               │
          └───────────────────────────────┴───────────────────────────────┘
                                          │
                                          ▼
                             [GPU HARDWARE RASTERIZER]
                       Buffer de Exibição (Tela Cheia / Canvas)
                         60fps / 120fps com Zero Jitter do DOM
```

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

O uso de shaders de fragmento procedural deve ser calibrado com precisão cirúrgica para maximizar a autoridade visual sem comprometer a usabilidade e o tempo de carregamento da aplicação.

### Casos de Uso Insubstituíveis

1. **Hero Sections Cinemáticas de Plataformas Tecnológicas & AI**:
   - Criação de planos de fundo biomórficos ou energéticos (como fluxos de convecção, partículas em campo de Curl Noise ou nébula volumétrica) que reagem sutilmente ao cursor. Transmite imediatamente percepção de inovação e vanguarda.
2. **Vidro Líquido e Efeitos de Refração de UI (Liquid Glass Cards)**:
   - Aplicação de shaders de refração (*Fluted Glass*, *Frosted Glass*, *Prism*) sobre componentes que se movem ou sobre fundos iluminados. Ao contrário do simples `backdrop-filter: blur()`, o shader de vidro calcula distorções ópticas tangenciais e dispersão prismática nas bordas do card.
3. **Transições de Página e Inter-estados (Morphing & Dissolve)**:
   - Transição entre rotas ou cards através de filtros de dissolução baseados em ruído fractal (*Noise Dissolve*), rasgo de pixels (*Pixel Sort*) ou transições de corte (*Diamond Wipe*), eliminando trocas visuais abruptas.
4. **Visualizadores de Dados Interativos & Fundos de Áudio**:
   - Plataformas de streaming de música, estúdios de podcast ou assistentes de voz onde o fundo reage diretamente aos dados da Web Audio API (`AnalyserNode`), transformando amplitudes em ondulações físicas em tempo real.
5. **Brand Identity & Experiências de Micro-Interações de Alto Impacto**:
   - Botões com efeito de mercúrio (*LiquidMetal*), bordas com brilho especular cromático (*LightEdge*), e cursores que deixam rastros dinâmicos fluidos (*CursorRipples*).

---

### Enquadramento na Regra 60-30-10

Na composição de uma interface de usuário de alto nível, os shaders ocupam papéis estruturados:

| Proporção | Papel no Shaders.com | Implementação Recomendada |
| :--- | :--- | :--- |
| **60% (Base Estrutural)** | **Tela Neutra & Silêncio Gráfico** | O shader NÃO deve ocupar os 60% com animação frenética. A base de 60% é a superfície escura ou clara com um gradiente procedural extremamente sutil e de baixa velocidade (`u_time * 0.05`), sem contraste disruptivo. |
| **30% (Identidade & Profundidade)** | **Textura e Refração Física** | Cards de vidro com *Fluted Glass*, divisores de seção com *Dither* procedural, barras de navegação com curvatura especular suave e iluminação cáustica de fundo. |
| **10% (Showstopper / Acento)** | **Ponto Focal Reativo** | Elemento herói 3D renderizado por *Raymarching SDF*, efeito *LiquidMetal* interativo em botão principal de conversão, ou distorção de *Chromatic Aberration* disparada em hover. |

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

A manipulação direta de pixels na GPU exige rigor extremo com consumo de energia, taxa de preenchimento (*fill rate*) e conforto cognitivo.

### ⚠️ Quando Evitar Absolutamente

- **Telas Críticas de Leitura e Trabalho Textual Intenso**:
  Shaders de alta frequência com contraste variante sob áreas de leitura prolongada (documentação, artigos, painéis de código) geram estresse ocular imediato e falham nos critérios de contraste mínimo WCAG (4.5:1 para texto normal).
- **Aplicações Transacionais / Formulários Financeiros e Checkout**:
  Em fluxos de pagamento, formulários complexos ou consoles de gerenciamento corporativo, qualquer distração cinética no canvas diminui a confiança do usuário e induz ansiedade operacional.
- **Dispositivos Móveis de Baixa Potência com Alta Resolução de Tela**:
  Executar fragment shaders pesados com múltiplos loops de ruído (ex: 8 oitavas de FBM ou Raymarching com 128 passos) em telas de smartphone com densidade 3x (telas Super AMOLED / Retina com mais de 3.5 milhões de pixels) esgota a bateria em minutos e induz estrangulamento térmico (*thermal throttling*).

---

### ⚠️ Regras de Ouro de Acessibilidade, GPU e Boas Práticas

1. **Acessibilidade e `prefers-reduced-motion`**:
   É mandatório consultar a preferência do sistema. Se ativada, o canvas WebGL deve congelar seu tempo (`u_time = 0.0`), suspender o RAF e reduzir a velocidade para zero, ou renderizar um fallback de imagem/gradiente estático CSS:
   ```ts
   const prefersReducedMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
   if (prefersReducedMotion) {
     // Suspende loop de animação e aplica cor estática de repouso
     cancelAnimationFrame(rafId);
   }
   ```
2. **DPR Clamping (Limite Máximo de Device Pixel Ratio)**:
   Nunca passe `window.devicePixelRatio` diretamente para o tamanho interno do canvas WebGL em telas móveis ou monitores 4K/5K:
   ```ts
   // Clamp seguro entre 1.0 e 1.5 (ou no máximo 2.0)
   const dpr = Math.min(Math.max(window.devicePixelRatio || 1, 1), 1.5);
   canvas.width = Math.floor(rect.width * dpr);
   canvas.height = Math.floor(rect.height * dpr);
   ```
   *Impacto*: Reduz a quantidade de fragmentos processados por frame em mais de **50% a 70%** em telas Retina, saltando instantaneamente de 30fps para 60fps constantes.
3. **Intersection Observer para Suspensão de RAF**:
   Quando o componente de shader rolar para fora da viewport visível do navegador, o loop de renderização deve ser pausado imediatamente (`cancelAnimationFrame`), liberando 100% da GPU para o restante da página:
   ```ts
   const observer = new IntersectionObserver(([entry]) => {
     isElementVisible = entry.isIntersecting;
     if (isElementVisible) startRenderLoop();
     else stopRenderLoop();
   }, { threshold: 0.05 });
   ```
4. **Gerenciamento do Contexto Gráfico e Garbage Collection**:
   Sempre tratar os eventos `webglcontextlost` e `webglcontextrestored`. Ao desmontar componentes React/Vue, execute a deleção explícita de shaders, programas, buffers e texturas (`gl.deleteProgram`, `gl.deleteShader`, `gl.deleteTexture`, `gl.deleteBuffer`).

---

## 4. Catálogo Detalhado de Componentes, Padrões & Efeitos Notáveis

O ecossistema Shaders.com categoriza centenas de efeitos procedurais. Abaixo estão catalogados os **12 padrões fundamentais** que compõem a espinha dorsal de sua biblioteca:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    MATRIZ VISUAL DE COMPONENTES SHADERS.COM                 │
└─────────────────────────────────────────────────────────────────────────────┘

 [GERATIVOS & FLUIDOS]          [ÓPTICOS & VIDRO]            [TEXTURAS & RETRÔ]
  1. Domain Warping FBM          2. Fluted / Liquid Glass     4. Noise Dithering
  7. Pointer-Reactive Fluid      6. Chromatic Aberration      5. Halftone CMYK
  9. Bicubic Mesh Gradient      11. Thin-Film Hologram        8. CRT Phosphor Glitch
 10. Divergence-Free Curl       12. Noise Dissolve Wipe       3. Raymarching SDFs
```

---

### 1. Domain Warping FBM (Fractal Brownian Motion com Deformação de Domínio)
- **Classificação**: Gerativo & Fluido / Background Primário.
- **Comportamento Visual**: Campo de cores orgânicas que fluem como fluidos viscosos ou convecção atmosférica. Em vez de calcular ruído sobre coordenadas UV lineares, as coordenadas são deformadas recursivamente pelo próprio ruído ($p \to p + \text{noise}(p)$), gerando dobras, turbilhões e camadas hiper-detalhadas.
- **Anatomia do Efeito**: 4 a 6 oitavas de Simplex Noise combinadas por soma fractal com decaimento exponencial de amplitude (lacunaridade = 2.0, ganho = 0.5), alimentadas por um vetor de deslocamento bicomponente.
- **Gatilho**: Loop temporal contínuo suave (`u_time * 0.15`), com perturbação de vetor de velocidade em hover do ponteiro.
- **Onde Encaixar**: Hero sections, telas de carregamento de IA, seções de apresentação de produto premium.

---

### 2. Fluted Glass & Liquid Glass Refraction (Vidro Canelado e Líquido)
- **Classificação**: Óptico & Textura de Superfície.
- **Comportamento Visual**: Superfície translúcida que distorce o conteúdo posicionado atrás do plano com base em ondulações estriadas (caneladas) ou bolsas de óleo viscoso. A luz sofre desvio tangencial calculando vetores normais da superfície e aplicando a Lei de Snell ($n_1 \sin \theta_1 = n_2 \sin \theta_2$).
- **Anatomia do Efeito**: Amostragem de textura de fundo (ou frame buffer anterior) com deslocamento de UV baseado no gradiente direcional de uma função de altura (heightmap). Separação fracionária dos canais R, G e B para simular aberração cromática nas arestas.
- **Gatilho**: Movimento contínuo de conteúdo de scroll sob a lente de vidro, ou deslocamento dinâmico do card via cursor.
- **Onde Encaixar**: Cartões de destaque (Pricing / Banners), cabeçalhos fixos flutuantes (Sticky Navigation), caixas modais.

---

### 3. Raymarching SDFs (Signed Distance Fields Tridimensionais em 2D Quad)
- **Classificação**: Espacial & Showstopper 3D.
- **Comportamento Visual**: Renderização procedural de geometria tridimensional completa (esferas morphing, toros entrelaçados, sólidos platônicos pulsantes) sem nenhuma geometria 3D no DOM ou malhas OBJ/GLTF.
- **Anatomia do Efeito**: O fragment shader dispara raios virtuais da posição da câmera em direção a cada pixel da tela (*Sphere Tracing*). Em cada passo do raio, a menor distância até os objetos da cena é avaliada por equações analíticas SDF (ex: `sdSphere`, `sdBox`, `opSmoothUnion`). O vetor normal é deduzido pelo gradiente das distâncias parciais para calcular iluminação de Phong ou PBR.
- **Gatilho**: Rotação sutil e contínua em torno do eixo Y acoplada à posição polar do mouse do usuário.
- **Onde Encaixar**: Emblemas centrais de identidade de marca, tokens visuais interativos, mascotes geométricos abstratos.

---

### 4. Noise Dithering & Blue Noise Distribution (Dither Procedural)
- **Classificação**: Pós-processamento & Redução de Banding.
- **Comportamento Visual**: Grânulo estético refinado que converte gradientes contínuos em um padrão pontilhado de alta frequência perceptiva (estética editorial / retro-futurista), eliminando o clássico problema de degradação e banding de 8 bits em monitores.
- **Anatomia do Efeito**: Adição de ruído azul estocástico ou matriz ordenada de Bayer (2x2, 4x4, 8x8) antes da etapa de quantização de cores. O valor de luminância de cada pixel determina a probabilidade de ativação dos pontos discretos.
- **Gatilho**: Renderizado estaticamente ou animado em baixíssima taxa de frequência (estilo filme analógico a 12fps ou 24fps).
- **Onde Encaixar**: Divisores de seção em sites editoriais, fundos escuros de alta sofisticação, fotografias com tratamento monocromático.

---

### 5. Halftone & Screen Printing Shader (Reticulamento CMYK de Impressão)
- **Classificação**: Textura Estilizada / Editorial Gráfico.
- **Comportamento Visual**: Converte qualquer imagem ou gradiente procedural em uma matriz ortogonal ou angular de pontos de retícula de impressão gráfica industrial, onde o raio de cada círculo varia proporcionalmente à densidade tonal da imagem de entrada.
- **Anatomia do Efeito**: Espaço UV é particionado em grade celular regular via `fract(uv * scale)`. A distância euclidiana do centro de cada célula até a borda determina uma função `step()` ou `smoothstep()`, cujo limiar de corte é governado pela luminância amostrada no centro da célula correspondente.
- **Gatilho**: Reativo ao ponteiro (efeito lente de aumento sobre os pontos) ou ativado em hover de imagens de portfólio.
- **Onde Encaixar**: Galerias de agências de design, e-commerce de moda e streetwear, cards de blog de cultura visual.

---

### 6. Dynamic Chromatic Aberration & Lens Distortion (Dispersão Óptica Vetorial)
- **Classificação**: Óptico / Reativo ao Movimento.
- **Comportamento Visual**: Quando a interface se desloca rapidamente ou o ponteiro cruza a tela em velocidade acelerada, os canais de cor vermelho, verde e azul se separam fisicamente, produzindo bordas prismáticas dinâmicas que colapsam suavemente no repouso.
- **Anatomia do Efeito**: Amostragem da textura com três vetores de coordenadas distintas: $UV_r = UV + \vec{v} \cdot \delta$, $UV_g = UV$, $UV_b = UV - \vec{v} \cdot \delta$, onde $\vec{v}$ é o vetor normalizado de velocidade do scroll ou mouse.
- **Gatilho**: Derivada da velocidade de rolagem (integrada com Lenis Scroll) ou velocidade do cursor.
- **Onde Encaixar**: Transições de slides em carrosséis interativos, headers com aceleração de rolagem, efeitos cinemáticos de saída.

---

### 7. Pointer-Reactive Fluid Trail (Convecção de Fluido com FBO Ping-Pong)
- **Classificação**: Físico-Interativo / Simulação Dinâmica.
- **Comportamento Visual**: O mouse atua como uma colher imersa em líquido denso, gerando redemoinhos de fumaça luminescente ou tinta fluida que se propagam pelo espaço e se dissipam com viscosidade natural ao longo de 2 a 3 segundos.
- **Anatomia do Efeito**: Baseado nas equações simplificadas de Navier-Stokes. Dois Framebuffers (FBOs) alternam em ciclo Ping-Pong: o FBO atual grava a nova posição e momento do ponteiro, aplica advecção baseada no campo de velocidade anterior e decai a intensidade exponencialmente (`decay = 0.96`).
- **Gatilho**: Movimento inercial contínuo do ponteiro sobre o elemento canvas.
- **Onde Encaixar**: Telas de boas-vindas de portfólios, visualizadores de estúdios interativos, áreas de hero interativas.

---

### 8. CRT Screen Scanlines & Glitch Displacement (Emulação de Fósforo Analógico)
- **Classificação**: Estético Retrô / Cyberspace.
- **Comportamento Visual**: Reproduz as imperfeições físicas de monitores de tubo catódico antigos: linhas de varredura (*scanlines*) horizontais oscilantes, curvatura esférica de barril nas bordas (*barrel distortion*), ruído de estática e pequenos saltos horizontais de desfasamento cromático.
- **Anatomia do Efeito**: Deformação esférica das coordenadas UV ($UV' = UV + UV \cdot (UV.x^2 + UV.y^2) \cdot k$). Modulação senoidal vertical da cor (`sin(uv.y * numLines)`) combinada com blocos de ruído aleatório em função do tempo para induzir quebras súbitas de sincronismo.
- **Gatilho**: Pulso constante com surtos estocásticos periódicos ou gatilho em hover de itens com tema cyberpunk/dev-tools.
- **Onde Encaixar**: Terminais de desenvolvedor web, painéis de monitoramento de infraestrutura, interfaces temáticas Web3 / hacker.

---

### 9. Bicubic Mesh Gradient (Gradiente de Malha Hiper-Contínuo)
- **Classificação**: Gerativo & Fluido / Base Elegante.
- **Comportamento Visual**: Malha suave de cores com dezenas de nós cromáticos que se entrelaçam de maneira orgânica, superando as limitações lineares ou radiais dos gradientes nativos de CSS.
- **Anatomia do Efeito**: Múltiplos pontos centrais de cor cujas posições orbitam em trajetórias senoidais assíncronas. O valor de cor em cada fragmento é a média ponderada inversa pela distância a esses nós (usando funções gaussianas ou interpolação metaball).
- **Gatilho**: Ciclo temporal infinito com perturbação magnética suave pela proximidade do mouse.
- **Onde Encaixar**: Fundos de dashboard em Dark Mode elegante, banners de destaque de produto SaaS, cards de apresentação.

---

### 10. Divergence-Free Curl Noise Particle Flow (Fluxo Turbulento de Partículas)
- **Classificação**: Partículas & Simulação Vetorial.
- **Comportamento Visual**: Dezenas de milhares de micro-partículas luminosas ou filamentos de luz que fluem sem colidir e sem convergir para pontos mortos, simulando escoamento aerodinâmico ou campos magnéticos cósmicos.
- **Anatomia do Efeito**: O campo de velocidades das partículas é calculado tomando-se o rotacional (*curl*) de um campo de potencial vetorial 3D composto por ruído Perlin/Simplex: $\vec{v} = \nabla \times \vec{\Psi}$. Por definição matemática, a divergência de um rotacional é identicamente nula ($\nabla \cdot (\nabla \times \vec{\Psi}) = 0$), garantindo conservação de massa e ausência de aglomeração estéril.
- **Gatilho**: Atualização em loop de compute shader (WebGPU) ou vertex shader instanciado.
- **Onde Encaixar**: Seções de inteligência artificial de fronteira, visualizações bio-médicas, aberturas cinematográficas de keynote.

---

### 11. Holographic Thin-Film Iridescence (Interferência Luminosa em Filme Fino)
- **Classificação**: Material Físico & Superfície Especular.
- **Comportamento Visual**: Efeito de película de bolha de sabão ou cartão holográfico de alta segurança. As cores alternam reflexos iridescentes do arco-íris dependendo estritamente do ângulo de visão do observador em relação à normal da superfície.
- **Anatomia do Efeito**: Cálculo das equações de interferência de ondas luminosas de Airy. O produto escalar entre a normal da superfície e o vetor de incidência visual ($\vec{N} \cdot \vec{V}$) modula a defasagem óptica $\Delta \phi = 2 d \sqrt{n^2 - \sin^2 \theta}$, projetada sobre uma rampa de cores cosseno analítica.
- **Gatilho**: Reativo ao movimento do cursor do mouse simulando uma fonte de luz móvel sobre o plano.
- **Onde Encaixar**: Badges de fidelidade premium, cartões de crédito e identidade digital, itens colecionáveis e NFTs.

---

### 12. Noise Dissolve & Block Dissolve Wipe (Transição com Máscara Fractal)
- **Classificação**: Transição & Máscara de Revelação.
- **Comportamento Visual**: Um elemento ou cena evapora gradativamente não por transparência genérica (fade out), mas sendo consumido por bordas luminosas de ruído térmico em cinzas incandescentes ou blocos digitais desintegrados.
- **Anatomia do Efeito**: Uma máscara de ruído procedural estático ou temporal é comparada com um uniforme `u_progress` que varia de 0.0 a 1.0. Pixels onde $\text{noise}(uv) < u\_progress$ são descartados (`discard` ou alfa 0.0), enquanto a borda imediata ($\text{noise}(uv) \approx u\_progress$) recebe emissão de cor incandescente (glow/alaranjado/elétrico).
- **Gatilho**: Troca de tabs, navegação entre etapas de um fluxo wizard, ou reveal ao rolar a página.
- **Onde Encaixar**: Apresentação de antes/depois, carrosséis de casos de sucesso, reveals de produtos ao entrar na tela.

---

## 5. Arquitetura Técnica, Física de Movimento & Receitas de Código

### Parâmetros Físicos e Formulações Matemáticas Fundamentais

#### A. Domain Warping FBM
A formulação clássica de Inigo Quilez para deformação de domínio em fragment shaders:

$$q(p) = \begin{pmatrix} fbm(p + \vec{0.0}) \\ fbm(p + \vec{5.2}, \vec{1.3}) \end{pmatrix}$$

$$r(p) = \begin{pmatrix} fbm(p + 4.0 \cdot q + \vec{1.7}, \vec{9.2}) \\ fbm(p + 4.0 \cdot q + \vec{8.3}, \vec{2.8}) \end{pmatrix}$$

$$f(p) = fbm(p + 4.0 \cdot r)$$

Onde $fbm(p)$ é a soma de $N$ oitavas de ruído:

$$fbm(p) = \sum_{i=0}^{N-1} g^i \cdot \text{noise}(l^i \cdot p)$$
*(com ganho $g = 0.5$ e lacunaridade $l = 2.0$)*.

#### B. Interpolação de Uniforms (Smooth LERP & Damping)
Para evitar que o shader apresente saltos secos ao mover o mouse ou rolar a página, o estado dos uniforms no JavaScript deve passar por equações de amortecimento exponencial no loop de renderização (RAF):

$$\vec{u}_{\text{current}} = \vec{u}_{\text{current}} + (\vec{u}_{\text{target}} - \vec{u}_{\text{current}}) \cdot (1.0 - e^{-\lambda \cdot \Delta t})$$

Onde $\lambda$ é o fator de rigidez/amortecimento (geralmente entre `8.0` para resposta ágil e `3.0` para sensação viscosa de água).

---

### Receita 1: Uso da Biblioteca Declarativa Oficial `shaders/react`

Abaixo está o padrão limpo de uso declarativo do pacote oficial da Shaders.com (`npm i shaders`) em um componente React moderno:

```tsx
import React, { useRef } from 'react';
import { Shader, MeshGradient, FlutedGlass, CursorTrail } from 'shaders/react';

export function ModernHeroBackground() {
  return (
    <div className="relative w-full h-[640px] overflow-hidden rounded-2xl bg-[#090A0F] border border-white/10">
      {/* Componente Shader da Shaders.com: encapsula o canvas WebGPU/WebGL */}
      <Shader 
        className="absolute inset-0 w-full h-full pointer-events-auto"
        dprLimit={1.5}
        pauseWhenHidden={true}
      >
        {/* Camada 1: Gradiente de malha dinâmico de fundo */}
        <MeshGradient 
          colors={['#090A0F', '#181135', '#2E1065', '#0F172A']}
          speed={0.4}
          distortion={0.65}
        />

        {/* Camada 2: Rastro do cursor com convecção de fluido */}
        <CursorTrail 
          size={180}
          intensity={1.2}
          decay={0.92}
          color="#818CF8"
        />

        {/* Camada 3: Filtro de refração e dispersão de vidro canelado */}
        <FlutedGlass 
          lines={48}
          refractionStrength={0.08}
          chromaticDispersion={0.03}
        />
      </Shader>

      {/* Conteúdo DOM semântico sobreposto */}
      <div className="relative z-10 flex flex-col items-center justify-center h-full px-6 text-center select-none pointer-events-none">
        <span className="px-3 py-1 mb-4 text-xs font-mono font-medium tracking-wider text-indigo-300 uppercase rounded-full bg-indigo-500/10 border border-indigo-500/20">
          Shaders.com Engine v3.0
        </span>
        <h1 className="text-4xl md:text-6xl font-bold tracking-tight text-white max-w-3xl">
          Interfaces Vivas Potencializadas por WebGPU
        </h1>
        <p className="mt-4 text-base md:text-lg text-slate-400 max-w-xl">
          Processamento de fragmentos em tempo real com física óptica e gradientes reativos a interações do usuário.
        </p>
      </div>
    </div>
  );
}
```

---

### Receita 2: Fullscreen WebGL Quad Shader Canvas em React / Next.js (TypeScript)

Para situações em que o projeto necessita de **controle absoluto, zero dependências pesadas e footprint mínimo (< 4KB)**, abaixo está a implementação industrial completa de um Canvas WebGL que executa um shader de alta performance com **Domain Warping FBM, Aberração Cromática e Reatividade ao Ponteiro**:

```tsx
'use client';

import React, { useEffect, useRef } from 'react';

// ============================================================================
// CÓDIGO GLSL: VERTEX & FRAGMENT SHADERS DE ALTA PERFORMANCE
// ============================================================================

const VERTEX_SHADER_SOURCE = `
  attribute vec2 a_position;
  varying vec2 v_uv;
  void main() {
    v_uv = (a_position + 1.0) * 0.5;
    gl_Position = vec4(a_position, 0.0, 1.0);
  }
`;

const FRAGMENT_SHADER_SOURCE = `
  precision highp float;

  uniform vec2 u_resolution;
  uniform float u_time;
  uniform vec2 u_mouse;
  uniform float u_mouse_velocity;
  varying vec2 v_uv;

  // Ruído Simplex 2D Procedural
  vec3 permute(vec3 x) { return mod(((x*34.0)+1.0)*x, 289.0); }

  float snoise(vec2 v) {
    const vec4 C = vec4(0.211324865405187, 0.366025403784439,
                        -0.577350269189626, 0.024390243902439);
    vec2 i  = floor(v + dot(v, C.yy));
    vec2 x0 = v -   i + dot(i, C.xx);
    vec2 i1 = (x0.x > x0.y) ? vec2(1.0, 0.0) : vec2(0.0, 1.0);
    vec4 x12 = x0.xyxy + C.xxzz;
    x12.xy -= i1;
    i = mod(i, 289.0);
    vec3 p = permute(permute(i.y + vec3(0.0, i1.y, 1.0))
                   + i.x + vec3(0.0, i1.x, 1.0));
    vec3 m = max(0.5 - vec3(dot(x0, x0), dot(x12.xy, x12.xy),
                            dot(x12.zw, x12.zw)), 0.0);
    m = m * m;
    m = m * m;
    vec3 x = 2.0 * fract(p * C.www) - 1.0;
    vec3 h = abs(x) - 0.5;
    vec3 ox = floor(x + 0.5);
    vec3 a0 = x - ox;
    m *= 1.79284291400159 - 0.85373472095314 * (a0*a0 + h*h);
    vec3 g;
    g.x  = a0.x  * x0.x  + h.x  * x0.y;
    g.yz = a0.yz * x12.xz + h.yz * x12.yw;
    return 130.0 * dot(m, g);
  }

  // 4 Oitavas de Fractal Brownian Motion (FBM)
  float fbm(vec2 p) {
    float f = 0.0;
    float amp = 0.5;
    float freq = 1.0;
    for (int i = 0; i < 4; i++) {
      f += amp * snoise(p * freq);
      freq *= 2.05;
      amp *= 0.5;
    }
    return f;
  }

  // Domain Warping Procedural
  float pattern(in vec2 p, out vec2 q, out vec2 r) {
    q = vec2(fbm(p + vec2(0.0, 0.0) + u_time * 0.04),
             fbm(p + vec2(5.2, 1.3) + u_time * 0.03));

    vec2 mouseOffset = (u_mouse - 0.5) * 0.4;
    r = vec2(fbm(p + 3.0 * q + vec2(1.7, 9.2) + mouseOffset),
             fbm(p + 3.0 * q + vec2(8.3, 2.8) - mouseOffset));

    return fbm(p + 3.0 * r);
  }

  void main() {
    vec2 st = gl_FragCoord.xy / u_resolution.xy;
    st.x *= u_resolution.x / u_resolution.y; // Correção de aspect ratio

    // Aberração Cromática dinâmica baseada na velocidade do ponteiro
    float aberration = 0.008 + (u_mouse_velocity * 0.025);

    vec2 qR, rR;
    float nR = pattern(st + vec2(aberration, 0.0), qR, rR);

    vec2 qG, rG;
    float nG = pattern(st, qG, rG);

    vec2 qB, rB;
    float nB = pattern(st - vec2(aberration, 0.0), qB, rB);

    // Paleta de Cores de Alta Densidade (Midnight Indigo / Cyan / Deep Violet)
    vec3 colorA = vec3(0.04, 0.05, 0.09); // #0a0d17 Fundo base
    vec3 colorB = vec3(0.18, 0.12, 0.38); // #2e1f61 Púrpura profundo
    vec3 colorC = vec3(0.24, 0.44, 0.95); // #3d70f3 Azul elétrico
    vec3 colorD = vec3(0.10, 0.85, 0.80); // #1ad9cc Ciano highlight

    vec3 finalColor;
    finalColor.r = mix(colorA.r, colorC.r, clamp(nR * 1.2, 0.0, 1.0));
    finalColor.g = mix(colorB.g, colorD.g, clamp(nG * 0.9, 0.0, 1.0));
    finalColor.b = mix(colorC.b, colorA.b, clamp(nB * 1.5, 0.0, 1.0));

    // Dither procedural de Bayer contra color banding
    float dither = fract(sin(dot(gl_FragCoord.xy, vec2(12.9898, 78.233))) * 43758.5453);
    finalColor += (dither - 0.5) * (1.0 / 255.0);

    gl_FragColor = vec4(finalColor, 1.0);
  }
`;

// ============================================================================
// COMPONENTE REACT: ENGINE DE EXECUÇÃO WEBGL RESILIENTE
// ============================================================================

interface ShaderCanvasProps {
  className?: string;
}

export const DomainWarpingCanvas: React.FC<ShaderCanvasProps> = ({ className }) => {
  const canvasRef = useRef<HTMLCanvasElement | null>(null);

  useEffect(() => {
    const canvas = canvasRef.current;
    if (!canvas) return;

    // 1. Inicialização do Contexto WebGL com atributos otimizados
    const gl = canvas.getContext('webgl', {
      alpha: false,
      antialias: false,
      depth: false,
      stencil: false,
      powerPreference: 'high-performance',
      preserveDrawingBuffer: false,
    });

    if (!gl) {
      console.warn('WebGL não suportado neste navegador/ambiente.');
      return;
    }

    // 2. Compilação de Shaders com Verificação de Erro
    const compileShader = (type: number, source: string): WebGLShader | null => {
      const shader = gl.createShader(type);
      if (!shader) return null;
      gl.shaderSource(shader, source);
      gl.compileShader(shader);
      if (!gl.getShaderParameter(shader, gl.COMPILE_STATUS)) {
        console.error('Falha de compilação do shader:', gl.getShaderInfoLog(shader));
        gl.deleteShader(shader);
        return null;
      }
      return shader;
    };

    const vertShader = compileShader(gl.VERTEX_SHADER, VERTEX_SHADER_SOURCE);
    const fragShader = compileShader(gl.FRAGMENT_SHADER, FRAGMENT_SHADER_SOURCE);
    if (!vertShader || !fragShader) return;

    const program = gl.createProgram();
    if (!program) return;
    gl.attachShader(program, vertShader);
    gl.attachShader(program, fragShader);
    gl.linkProgram(program);

    if (!gl.getProgramParameter(program, gl.LINK_STATUS)) {
      console.error('Falha ao linkar WebGL Program:', gl.getProgramInfoLog(program));
      return;
    }

    gl.useProgram(program);

    // 3. Montagem do Fullscreen Quad (Geometry 2D Plane)
    // 2 Triângulos cobrindo [-1, -1] até [1, 1] em Normalized Device Coordinates
    const positionBuffer = gl.createBuffer();
    gl.bindBuffer(gl.ARRAY_BUFFER, positionBuffer);
    const vertices = new Float32Array([
      -1.0, -1.0,
       1.0, -1.0,
      -1.0,  1.0,
      -1.0,  1.0,
       1.0, -1.0,
       1.0,  1.0,
    ]);
    gl.bufferData(gl.ARRAY_BUFFER, vertices, gl.STATIC_DRAW);

    const aPositionLocation = gl.getAttribLocation(program, 'a_position');
    gl.enableVertexAttribArray(aPositionLocation);
    gl.vertexAttribPointer(aPositionLocation, 2, gl.FLOAT, false, 0, 0);

    // 4. Localização dos Uniforms
    const uResolutionLocation = gl.getUniformLocation(program, 'u_resolution');
    const uTimeLocation = gl.getUniformLocation(program, 'u_time');
    const uMouseLocation = gl.getUniformLocation(program, 'u_mouse');
    const uMouseVelLocation = gl.getUniformLocation(program, 'u_mouse_velocity');

    // 5. Estado do Loop e Interpolação (LERP)
    let animationFrameId: number;
    let isVisible = true;
    let startTime = performance.now();

    const mouse = { currentX: 0.5, currentY: 0.5, targetX: 0.5, targetY: 0.5, velocity: 0 };
    let lastMousePos = { x: 0.5, y: 0.5 };
    let lastMouseTime = performance.now();

    // 6. Listener de Redimensionamento com DPR Clamping Seguro
    const handleResize = () => {
      if (!canvas) return;
      const rect = canvas.getBoundingClientRect();
      // Limita o DPR a no máximo 1.5 para proteger a taxa de preenchimento (fill rate)
      const dpr = Math.min(Math.max(window.devicePixelRatio || 1, 1), 1.5);
      const width = Math.floor(rect.width * dpr);
      const height = Math.floor(rect.height * dpr);

      if (canvas.width !== width || canvas.height !== height) {
        canvas.width = width;
        canvas.height = height;
        gl.viewport(0, 0, width, height);
      }
    };

    window.addEventListener('resize', handleResize);
    handleResize();

    // 7. Rastreamento e Inércia do Mouse
    const handlePointerMove = (e: PointerEvent) => {
      const rect = canvas.getBoundingClientRect();
      const now = performance.now();
      const dt = Math.max((now - lastMouseTime) / 1000, 0.001);

      const x = (e.clientX - rect.left) / rect.width;
      const y = 1.0 - (e.clientY - rect.top) / rect.height; // Inverte eixo Y para coordenadas WebGL

      const dx = x - lastMousePos.x;
      const dy = y - lastMousePos.y;
      const instantVelocity = Math.sqrt(dx * dx + dy * dy) / dt;

      mouse.targetX = Math.min(Math.max(x, 0), 1);
      mouse.targetY = Math.min(Math.max(y, 0), 1);
      mouse.velocity = Math.min(instantVelocity * 0.05, 1.0);

      lastMousePos = { x, y };
      lastMouseTime = now;
    };

    window.addEventListener('pointermove', handlePointerMove, { passive: true });

    // 8. Intersection Observer para Pausa Automática Fora da Viewport
    const observer = new IntersectionObserver(([entry]) => {
      isVisible = entry.isIntersecting;
      if (isVisible) {
        startTime = performance.now();
        render();
      } else {
        cancelAnimationFrame(animationFrameId);
      }
    }, { threshold: 0.01 });

    observer.observe(canvas);

    // 9. Loop de Renderização a 60fps/120fps
    const render = () => {
      if (!isVisible) return;

      const currentTime = (performance.now() - startTime) / 1000;

      // Suavização do mouse via LERP (fator 0.08 para amortecimento natural)
      mouse.currentX += (mouse.targetX - mouse.currentX) * 0.08;
      mouse.currentY += (mouse.targetY - mouse.currentY) * 0.08;
      mouse.velocity *= 0.94; // Decaimento inercial da velocidade

      // Upload de Uniforms
      gl.uniform2f(uResolutionLocation, canvas.width, canvas.height);
      gl.uniform1f(uTimeLocation, currentTime);
      gl.uniform2f(uMouseLocation, mouse.currentX, mouse.currentY);
      gl.uniform1f(uMouseVelLocation, mouse.velocity);

      // Draw Call Único do Fullscreen Quad
      gl.drawArrays(gl.TRIANGLES, 0, 6);

      animationFrameId = requestAnimationFrame(render);
    };

    render();

    // 10. Limpeza Rigorosa de Memória e Recursos Gráficos
    return () => {
      cancelAnimationFrame(animationFrameId);
      observer.disconnect();
      window.removeEventListener('resize', handleResize);
      window.removeEventListener('pointermove', handlePointerMove);

      if (gl) {
        gl.deleteBuffer(positionBuffer);
        gl.deleteProgram(program);
        gl.deleteShader(vertShader);
        gl.deleteShader(fragShader);
      }
    };
  }, []);

  return (
    <canvas 
      ref={canvasRef} 
      className={className || 'w-full h-full block'}
      style={{ touchAction: 'none' }}
    />
  );
};
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma arquitetura de interface que emprega recursos do **Shaders.com**, o arquiteto de front-end deve especificar os parâmetros técnicos no plano técnico do projeto antes de qualquer linha de código ser escrita.

### Checklist Técnico Obrigatório de Especificação

1. **Definição de Papel do Shader (Showstopper vs Fundo Estrutural)**:
   - Declarar explicitamente se o shader compõe a **camada de 60%** (fundo ambiental neutro, com contraste atenuado e variação de luminância máxima de 15%), **30%** (deformação óptica de cards de vidro) ou **10%** (efeito de transição pontual ou objeto central 3D SDF).
2. **Estratégia de Resolução & Limitação de DPI**:
   - `dpr_limit: 1.5` especificado formalmente para evitar sobrecarga em monitores de alta densidade 4K/5K e aparelhos iPhone/Pixel.
3. **Mapeamento de Uniforms Reativos**:
   - Listar todos os canais de interação: `u_time` (velocidade), `u_mouse` (amortecimento LERP), `u_scroll_velocity` (acoplamento com Lenis Scroll) e `u_audio` (se houver integração sonora).
4. **Política de Acessibilidade & Modo Econômico**:
   - Declarar o comportamento quando `prefers-reduced-motion: reduce` for detectado: congelar animação ou aplicar `background: radial-gradient(...)` em CSS estático.
   - Declarar o threshold do `IntersectionObserver` (desativação de renderização fora da tela).
5. **Contraste de Acessibilidade (WCAG 2.2 AA)**:
   - Garantir que todo texto, botão ou ícone renderizado sobre o canvas mantenha relação de contraste de no mínimo 4.5:1 contra a cor média de luminância de pico do shader. Usar scrims de degradê preto (`bg-gradient-to-t from-black/80 via-transparent`) se o shader contiver picos de brilho.
6. **Hierarquia de Camadas DOM vs GPU**:
   - O canvas WebGL deve sempre operar com `pointer-events: none` caso não receba cliques diretos, permitindo que a seleção de texto e cliques em links do DOM ocorram sem impedimentos. Se houver interação com o ponteiro, capturar os eventos via `window` ou no container pai.

---

### Resumo Executivo para a Equipe de Engenharia

> *"O Shaders.com transforma a GPU em um motor estético de primeira classe para a interface web. Nunca trate o shader como uma animação solta: ele é uma superfície física calculada por pixel. Limite o DPR a 1.5, suspenda o RAF fora da viewport, amorteça os movimentos do ponteiro com LERP e reserve o espetáculo visual para os 10% de maior impacto da jornada do usuário."*
