---
id: "threejs-examples"
name: "Three.js Examples & Canonical Techniques"
url: "https://threejs.org/examples/"
category: "4-shaders-3d"
schema_type: "B-motion-shaders"
dna_estetico: ["Physically Based Rendering (PBR)", "Sub-Surface Optical Refraction", "Hardware-Accelerated Instancing", "Cinematic Post-Processing Glare", "Volumetric Light Transport", "Node-Based Shader Graph (TSL)", "Spatial Scrollytelling Choreography"]
densidade_informacao: "Independente"
impacto_visual: "Cinematografico/Showstopper"
custo_computacional: "Alto (WebGL2 / WebGPU / GLSL / TSL Compute & Render Pipeline)"
stack_frameworks: ["Three.js (r160+)", "WebGPURenderer & TSL (Three Shading Language)", "React Three Fiber (@react-three/fiber)", "@react-three/drei", "@react-three/postprocessing", "three-mesh-bvh", "three-subdivide", "DRACOLoader / KTX2Loader"]
compatibilidade:
  combinacoes_recomendadas: ["Three.js (R3F) + Lenis Smooth Scroll", "R3F Canvas + GSAP ScrollTrigger", "@react-three/drei (MeshTransmissionMaterial) + ACESFilmicToneMapping", "InstancedMesh + TSL Compute / StorageBuffer", "PMREMGenerator (UltraHDR / EXR) + MeshPhysicalMaterial"]
  conflitos_esteticos: ["Loop requestAnimationFrame contínuo e irrestrito sobre baterias móveis sem controle de framerate ou invalidate on-demand", "Cenas 3D hiper-pesadas renderizadas sem frustum culling, occlusion culling ou compressão Draco/KTX2", "Transmissão física e refraction shaders aninhados recursivamente em GPUs integradas (memory bandwidth choke)", "Canvas WebGL bloqueando eventos de toque/scroll essenciais do DOM sem 'pointer-events: none' em camadas transparentes"]
---

# Three.js Examples & Canonical Techniques — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)

O repositório e vitrine oficial **Three.js Examples** (`https://threejs.org/examples/`), concebido e liderado por **Ricardo Cabello (Mr.doob)** juntamente com uma comunidade global de cientistas da computação gráfica e engenheiros de renderização, representa o catálogo canônico e a espinha dorsal de toda a computação visual 3D em tempo real na Web moderna.

Desde o nascimento do WebGL em 2011 até a revolução contemporânea do **WebGPU** e da **TSL (Three Shading Language)**, o Three.js removeu a necessidade de os desenvolvedores programarem diretamente chamadas brutas de API gráfica de baixo nível, transformando equações tensoriais de álgebra linear e manipulação de buffers de GPU em uma abstração elegante de cenas, câmeras, geometrias, materiais e luzes.

---

### A Fundação Técnica: O Pipeline Gráfico WebGL / WebGPU do Three.js

O Three.js atua como o orquestrador do ciclo de vida gráfico completo entre a CPU e o silício da GPU:

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                    THREE.JS GRAPHICS & RENDER PIPELINE                       │
└──────────────────────────────────────────────────────────────────────────────┘
                                      │
                         [Scene Graph & Hierarchy]
                   (Object3D -> Group -> Mesh / Light)
                                      │
                                      ▼
                        [Frustum Culling & BVH]
                 (Elimina objetos fora da visão da câmera)
                                      │
                                      ▼
                    [State Sorting & Material Batching]
                (Agrupa por shader program para evitar state changes)
                                      │
          ┌───────────────────────────┴───────────────────────────┐
          ▼                                                       ▼
   [WebGL 2 Pipeline]                                     [WebGPU Pipeline]
   - GLSL Compilação de Shaders                          - TSL (Three Shading Language AST)
   - Vertex & Index Buffers                              - WGSL nativo / SPIR-V
   - Texture Units (sRGB / Linear)                       - Compute Shaders & Storage Buffers
   - Framebuffer Objects (FBO)                           - Render Bundles & Pipeline Caches
          │                                                       │
          └───────────────────────────┬───────────────────────────┘
                                      ▼
                           [Rasterizer & MSAA]
                                      ▼
                         [Fragment / Pixel Shading]
             (PBR Cook-Torrance, Transmission, Shadows, IBL)
                                      ▼
                         [EffectComposer Pipeline]
               (HDR Tone Mapping, Bloom, SSAO, DepthOfField)
                                      ▼
                        [Canvas DOM Presentation]
```

### Sensação Cinestésica e Imersão Tátil (Physically Based Rendering)

O objetivo central do Three.js em interfaces modernas não é criar "joguinhos no navegador", mas fornecer **fidelidade física tátil** (*tangible presence*). Uma interface que integra materiais PBR de Three.js não aparenta ser desenhada em pixels de tela; ela aparenta possuir massa, espessura ótica, índice de refração e inércia mecânica:

1. **Micro-Facet Lighting & Fotometria Realista**: Através do modelo de micro-facetas de **Cook-Torrance** (distribuição normal GGX, sombreamento geométrico de Smith e aproximação de Fresnel de Schlick), a luz espalha-se sobre superfícies metálicas e dielétricas exatamente como fótons no mundo real.
2. **Refração Óptica e Transmissão Volumétrica**: Com `MeshPhysicalMaterial` e `transmission`, superfícies de vidro acrílico, prismas e cristais distorcem a cena subjacente com desvio cromático, dispersão de Cauchy e absorção de Beer-Lambert, conferindo profundidade háptica incomparável.
3. **Inércia Espacial e Gravidade Artificial**: O movimento 3D no Three.js é regido por transformações matriciais contínuas ($4 \times 4$ Affine Transformations). Quando associado a amortecedores de inércia (`OrbitControls.dampingFactor = 0.05` ou equações de mola em R3F), o usuário manipula objetos espaciais com resistência de atrito físico e decaimento elástico suave.

---

### A Dualidade Arquitetural: Three.js Imperativo vs. React Three Fiber (R3F) Declarativo

Na engenharia web contemporânea, a aplicação do Three.js desdobra-se em dois paradigmas complementares:

| Dimensão | Three.js Core (Imperativo) | React Three Fiber / Drei (Declarativo) |
| :--- | :--- | :--- |
| **Paradigma** | Procedural, mutações diretas em objetos C-style | Reativo, reconciliador React sobre nós de cena 3D |
| **Gerenciamento de Ciclo** | Manual via `.dispose()`, listeners imperativos | Automático via unmount de componentes e hooks (`useFrame`) |
| **Abstração de Shaders** | `ShaderMaterial` GLSL bruto ou TSL Nodes | Shaders embutidos com HMR, `shaderMaterial` e `@react-three/drei` |
| **Custo de Abstração** | Zero sobrecarga de runtime de frameworks | Minúsculo overhead de reconciliação, amortizado pela GPU |
| **Cenário de Escolha** | Engines de render dedicadas, loaders puros, Three.js core | Web apps Next.js/React, design systems dinâmicos, landing pages |

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Interface e Casos de Uso Críticos

1. **Hero Sections Showstopper com Identidade Físico-Digital**:
   Primeiras dobras de landing pages corporativas de IA, Web3, computação quântica e marcas de luxo onde uma peça central refrativa (cristal geométrico, malha topológica fluida, esfera líquida) reage à posição do cursor do mouse em 60/120fps.
2. **Configuradores de Produto Fotorealistas (E-Commerce 3D)**:
   Apresentação de automóveis, joias, relógios, calçados e eletrônicos com troca dinâmica de materiais (metal escovado, fibra de carbono, couro com normal maps, vidro óptico) com reflexos de ambiente em tempo real via HDRI IBL.
3. **Data Visualization Espacial e Redes de Grafos em Larga Escala**:
   Visualização de milhares de nós de dados, conexões de redes neurais ou constelações geoespaciais utilizando `InstancedMesh`, renderizando de 50.000 a 200.000 instâncias em uma única draw call sem gargalo de CPU.
4. **Scrollytelling Cinematográfico Imersivo (Storytelling Interativo)**:
   Navegação onde o ato de rolar a página conduz uma câmera ao longo de uma curva tridimensional (`CatmullRomCurve3`), explorando arquiteturas industriais, anatomia médica ou narrativas de produto em perfeita sincronia com textos fixados no DOM via Lenis/GSAP.
5. **Backdrops Generativos e Shaders de Ruído Orgânico**:
   Fundos abstratos reativos a áudio ou tempo que substituem vídeos pesados de background por fragment shaders de baixa largura de banda e resolução procedural infinita.

---

### A Regra 60-30-10 em Ambientes Espaciais e Shaders

A incorporação de WebGL e Shaders deve obedecer rigorosamente à hierarquia composicional para não soterrar a usabilidade:

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                    REGRA 60-30-10 EM EXPERIÊNCIAS 3D/SHADERS                │
└──────────────────────────────────────────────────────────────────────────────┘
  60% FUNDAÇÃO NEUTRA: Espaço negativo escuro ou claro (Clean Canvas, #030712
      ou #f8fafc), tipografia estável, layout bidimensional sem ruído visual.
  ─────────────────────────────────────────────────────────────────────────────
  30% ESTRUTURA INTERATIVA: Painéis de vidro acrílico DOM com backdrop-blur,
      cards de navegação em HTML, micro-interações táteis e controles UI.
  ─────────────────────────────────────────────────────────────────────────────
  10% ESPETÁCULO VISUAL 3D (O SHOWSTOPPER): A malha Three.js, os reflexos HDR,
      a refração de luz e o brilho do Bloom — agindo como ímã focal de atenção.
```

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Quando Evitar Radicalmente

1. **Aplicações de Alta Densidade Informacional e Entrada de Dados (CRUD, ERPs, Spreadsheets)**:
   Inserir canvases WebGL em ferramentas de produtividade diária (como Notion, Airtable, Linear) drena recursos da GPU corporativa, aquece laptops e introduz latência de input sem entregar valor funcional.
2. **Páginas de Checkout e Funis Críticos de Conversão E-Commerce**:
   Qualquer frame drop, falha de inicialização de contexto gráfico ou atraso no carregamento de um arquivo GLTF de 15MB pode custar o abandono imediato da compra. O 3D deve ser restrito à página de detalhe de produto (PDP).
3. **Dispositivos Móveis de Baixa Potência com Bateria Degradada**:
   Executar render loops contínuos a 120Hz com múltiplos passes de post-processing descarrega a bateria de smartphones em minutos e aciona o thermal throttling da CPU/GPU, travando toda a interface do sistema.
4. **Ambientes onde SEO Crítico Depende de Leitura Imediata de Conteúdo**:
   Textos cruciais nunca devem ser "desenhados" em texturas de canvas 3D; eles devem sempre residir como nós semânticos HTML acessíveis para crawlers e screen readers.

---

### ⚠️ Métricas de Gargalo: Draw Calls, Fill Rate e Fragment Overdraw

Para manter uma experiência a 60fps estável em 95% do parque de dispositivos, obedeça a estes limites orçamentários:

| Métrica Crítica | Limite Mobile Seguro | Limite Desktop Seguro | Consequência da Violação |
| :--- | :--- | :--- | :--- |
| **Draw Calls** | $< 30$ | $< 100$ | CPU Bottleneck (sobrecarga do driver gráfico no envio de comandos) |
| **Contagem de Vértices** | $< 100.000$ | $< 1.000.000$ | Vertex Shader Bottleneck e estouro de memória de geometria |
| **Passes de Post-Processing** | $\le 1$ pass (FXAA/ToneMapping) | $\le 3$ passes (Bloom, SSAO, FXAA) | Fill-rate exhaustion e estouro de banda de memória de vídeo |
| **Tamanho de Texturas** | Máximo $1024 \times 1024$ (KTX2) | Máximo $2048 \times 2048$ (KTX2/Basis) | VRAM Overflow e crash instantâneo no iOS WebKit (Black Screen) |
| **Tamanho Total de Bundles 3D** | $< 2.5 \text{ MB}$ (Gzip/Draco) | $< 10 \text{ MB}$ | Aumento brutal no TTI (Time to Interactive) e bounce rate |

---

### ⚠️ Regras Rígidas de GPU, Memória & Acessibilidade

#### 1. Prevenção de Memory Leaks e Protocolo de "Disposal Hygiene"
JavaScript possui Garbage Collector, mas a VRAM da GPU **não possui**. Se um nó da cena Three.js for removido da árvore sem descarte explícito de buffers e texturas, ele permanecerá congelado na memória de vídeo até o fechamento da aba.

```javascript
// Protocolo canônico de desalocação recursiva de recursos GPU
function disposeHierarchy(node) {
  if (!node) return;

  if (node.geometry) {
    node.geometry.dispose();
  }

  if (node.material) {
    if (Array.isArray(node.material)) {
      node.material.forEach(cleanMaterial);
    } else {
      cleanMaterial(node.material);
    }
  }

  while (node.children.length > 0) {
    const child = node.children[0];
    disposeHierarchy(child);
    node.remove(child);
  }
}

function cleanMaterial(material) {
  material.dispose();
  for (const key of Object.keys(material)) {
    const value = material[key];
    if (value && typeof value === 'object' && 'minFilter' in value) {
      value.dispose(); // Descarta WebGLTexture subjacente
    }
  }
}
```

#### 2. Suspensão Condicional de Renderização (Demand-Driven Rendering vs Continuous Loop)
Nunca rode um render loop contínuo desnecessariamente. Utilize renderização por demanda:

```javascript
// Em Three.js Puro: disparar render() apenas sob dirty states (controls change, scroll, resize)
controls.addEventListener('change', () => renderer.render(scene, camera));

// Em React Three Fiber:
<Canvas frameloop="demand"> {/* Renderiza apenas se houver invalidação de estado */}
```

#### 3. Suporte a `prefers-reduced-motion` e Context Lost
```javascript
// Monitorar sensibilidade vestibular do usuário
const mediaQuery = window.matchMedia('(prefers-reduced-motion: reduce)');
if (mediaQuery.matches) {
  // Desativa auto-rotação, desliga oscilações de partículas, fixa a câmera
  controls.autoRotate = false;
}

// Tratamento de Perda de Contexto WebGL
renderer.domElement.addEventListener('webglcontextlost', (event) => {
  event.preventDefault();
  console.warn('WebGL Context Lost: congelando shaders e exibindo fallback estático.');
  cancelAnimationFrame(animationFrameId);
}, false);

renderer.domElement.addEventListener('webglcontextrestored', () => {
  console.info('WebGL Context Restored: recriando buffers e texturas.');
  initGraphicsPipeline();
}, false);
```

---

## 4. Catálogo Detalhado de Componentes, Padrões & Shaders Notáveis

A seguir estão os 10 padrões essenciais documentados no catálogo de exemplos oficiais do Three.js:

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                  THREE.JS EXAMPLES ESSENTIAL TECHNIQUES                     │
└──────────────────────────────────────────────────────────────────────────────┘
  [01] PBR Refractive Physical Glass  ───▶ webgl_materials_physical_transmission
  [02] GPU High-Density Instancing    ───▶ webgl_instancing_dynamic
  [03] Cinematic Multi-Pass Bloom     ───▶ webgl_postprocessing_unreal_bloom
  [04] Image-Based Lighting (IBL)     ───▶ webgl_materials_envmaps_hdr
  [05] Screen-Space GTAO / SSAO       ───▶ webgl_postprocessing_gtao
  [06] WebGPU TSL Node Materials      ───▶ webgpu_tsl_editor / webgpu_materials
  [07] Vertex Noise Displacements     ───▶ webgl_buffergeometry_custom_attributes
  [08] Depth of Field Bokeh CoC       ───▶ webgl_postprocessing_dof
  [09] Draco / Meshopt Mesh Streaming ───▶ webgl_loader_gltf_compressed
  [10] Spatial Scrolly Camera Track   ───▶ webgl_geometry_extrude_splines
```

---

### 1. Vidro Físico Refrativo e Dispersão Óptica (`MeshPhysicalMaterial Transmission`)
- **Exemplo Oficial**: `webgl_materials_physical_transmission` / `webgl_materials_physical_clearcoat`.
- **Comportamento Visual**: Simula a refração precisa da luz ao atravessar um volume sólido ou oco. Objetos posicionados atrás da malha aparecem deformados segundo o índice de refração (`ior`), enquanto micro-rugosidades geram o efeito de vidro fosco jateado (*frosted glass*). A versão moderna emula dispersão cromática dividindo feixes de luz em comprimentos de onda RGB nas bordas de alta curvatura.
- **Gatilho**: Rotação do objeto, deslocamento da câmera ou movimento de objetos luminescentes no plano de fundo.
- **Anatomia Técnica**:
  - `transmission: 1.0` (fração de luz que atravessa o material sem absorção opaca).
  - `ior: 1.52` (índice de refração típico de vidro Crown; água = 1.333, diamante = 2.417).
  - `thickness: 1.5` (distância percorrida pelo raio de luz dentro do corpo, regendo a lei de Beer).
  - `roughness: 0.1` a `0.25` (difusão superficial dos raios refratados).
  - `dispersion: 0.05` (separação espectral cromática do feixe).
- **Encaixe no Design**: Elementos de hero flutuantes, lentes de interface, troféus 3D e interfaces de hardware transparentes de alta fidelidade.

---

### 2. Partículas Massivas e Geometrias por GPU Instancing (`InstancedMesh`)
- **Exemplo Oficial**: `webgl_instancing_dynamic` / `webgpu_instance_mesh`.
- **Comportamento Visual**: Milhares (de 5.000 a 100.000) de geometrias tridimensionais idênticas (cubos, tetraedros, esferas, cristais) movendo-se, rotacionando e alterando suas tonalidades individualmente a 60fps constantes sem sobrecarregar a CPU.
- **Gatilho**: Animação temporal contínua (`uTime`), aproximação do cursor do mouse por raycasting ou scroll da página.
- **Anatomia Técnica**:
  - `InstancedMesh(geometry, material, count)`: aloca um buffer de matrizes de transformação de 64 bytes por instância (`instanceMatrix`, buffer `Float32Array` de tamanho `count * 16`).
  - `setMatrixAt(i, matrix)` e `setColorAt(i, color)`.
  - Flag obrigatória: `instancedMesh.instanceMatrix.needsUpdate = true` no loop de renderização para submeter novos dados à GPU.
- **Encaixe no Design**: Campos estelares interativos, matrizes de dados topológicos, fragmentação procedural de logos e partículas sonoras 3D.

---

### 3. Glow Cinemático e Brilho Seletivo (`UnrealBloomPass`)
- **Exemplo Oficial**: `webgl_postprocessing_unreal_bloom_selective`.
- **Comportamento Visual**: Áreas da cena que ultrapassam um limiar de luminância física emitem uma aura difusa e volumétrica que sangra sobre os pixels vizinhos, emulando a imperfeição óptica das lentes de câmeras cinematográficas anamórficas do mundo real.
- **Gatilho**: Materiais com valores de `emissiveIntensity > 1.0` em um pipeline HDR Tone Mapped.
- **Anatomia Técnica**:
  - Downsampling sucessivo em pirâmide de Mipmaps Gaussianos (5 níveis de blur com pesos decrescentes).
  - `threshold`: determina a intensidade mínima de pixel HDR para disparar o bloom (ex: `0.85`).
  - `strength`: intensidade multiplicativa da aura luminosa (ex: `0.6` a `1.2`).
  - `radius`: raio de dispersão do espalhamento de luz (ex: `0.4` a `0.8`).
- **Encaixe no Design**: Destaque de botões de conversão 3D, fibras ópticas condutoras, circuitos futuristas e elementos incandescentes em dark mode.

---

### 4. Iluminação Físico-Ambiental baseada em Imagem (HDRI IBL & PMREM)
- **Exemplo Oficial**: `webgl_materials_envmaps_hdr` / `webgl_materials_envmaps_exr`.
- **Comportamento Visual**: Objetos 3D não recebem luz apenas de fontes pontuais ou direcionais, mas são banhados pela luz real capturada em um ambiente panorâmico $360^\circ$. Superfícies espelhadas refletem o céu e as lâmpadas do cenário; superfícies foscas recebem iluminação difusa calculada por harmônicos esféricos (*Spherical Harmonics*).
- **Gatilho**: Rotação da câmera ou transição suave entre ambientes dia/noite.
- **Anatomia Técnica**:
  - `RGBELoader` carrega arquivos `.hdr` codificados em RGBE de 32 bits por canal.
  - `PMREMGenerator` (Prefiltered Mipmapped Radiance Environment Map) pré-filtra a textura em diferentes níveis de rugosidade GGX para consulta ultrarrápida no fragment shader em um único `textureCubeLodEXT`.
  - Mapeamento: `scene.environment = envMap; scene.background = null;` (para iluminação invisível sem sobrecarregar o background visual).
- **Encaixe no Design**: Qualquer cena que utilize metais (alumínio, cromo, ouro) ou vidro, garantindo que o objeto pareça estar fisicamente inserido em um espaço tangível.

---

### 5. Oclusão de Contato Espacial em Tempo Real (`GTAOPass` / Ground Truth Ambient Occlusion)
- **Exemplo Oficial**: `webgl_postprocessing_gtao`.
- **Comportamento Visual**: Gera sombras de contato realistas em fendas, vincos e pontos de encontro entre geometrias onde a luz ambiental não consegue penetrar livremente, conferindo "peso", profundidade e eliminando o aspecto visual de "objetos flutuando no vazio".
- **Gatilho**: Posicionamento de múltiplos objetos estáticos ou dinâmicos em relação ao chão ou a superfícies vizinhas.
- **Anatomia Técnica**:
  - Utiliza o Depth Buffer e o Normal Buffer gerados em um pré-pass de renderização.
  - Calcula a integral de oclusão por amostragem de horizontes no espaço de tela (*Ground Truth horizon scanning*), superando amplamente o SSAO tradicional em precisão matemática e ausência de halos pretos espúrios.
- **Encaixe no Design**: Visualizadores de arquitetura, apresentações de embalagens e produtos de consumo em websites de e-commerce de alto padrão.

---

### 6. Materiais em Grafo e Computação GPU de Próxima Geração (`WebGPU / TSL Node Materials`)
- **Exemplo Oficial**: `webgpu_tsl_editor` / `webgpu_materials` / `webgpu_compute_particles`.
- **Comportamento Visual**: Permite a escrita de lógica de sombreamento complexa utilizando nós de JavaScript modulares e fortemente tipados em vez de strings monolíticas de GLSL, compilando diretamente para **WGSL** (WebGPU) com fallback nativo para **GLSL 3.0** (WebGL 2).
- **Gatilho**: Parâmetros reativos da interface (ex: sliders, scroll progress, uniforms dinâmicos).
- **Anatomia Técnica**:
  - Importação de primitivas TSL: `import { color, sin, time, uv, positionLocal, range, MeshStandardNodeMaterial } from 'three/tsl'`.
  - Composição direta: `material.colorNode = color(0x00ff88).mix(color(0x0066ff), sin(time.mul(2)))`.
  - Suporte a Compute Shaders: manipulação de milhões de partículas inteiramente na GPU através de nós de leitura e escrita em `StorageBuffer`.
- **Encaixe no Design**: Projetos de longo prazo que buscam compatibilidade futura com os navegadores de 2025–2030 e interfaces de computação generativa.

---

### 7. Deformação de Malha por Ruído Procedural (Perlin / Simplex Vertex Displacement)
- **Exemplo Oficial**: `webgl_buffergeometry_custom_attributes` / `webgl_shaders_ocean`.
- **Comportamento Visual**: Uma geometria tridimensional padrão (esfera, plano, toro) ganha vida biológica ou fluida orgânica, ondulando como metal líquido, tecido ao vento ou dunas alienígenas sem que a CPU calcule um único vértice.
- **Gatilho**: Uniform contínuo `uTime` e interação vetorial de ponteiro `uPointer` que perturba a superfície nas proximidades do mouse.
- **Anatomia Técnica**:
  - No Vertex Shader: o vetor `position` é deslocado ao longo da sua normal (`position + normal * noise(position * frequency + uTime) * amplitude`).
  - Recálculo das normais analíticas ou por diferenças finitas para que os reflexos de luz PBR acompanhem com perfeição a nova curvatura dinâmica da superfície.
- **Encaixe no Design**: Orbes centrais de inteligência artificial, interfaces de voz bio-inspiradas e visualizadores de streaming de dados.

---

### 8. Desfocagem de Lente Cinemática e Foco Seletivo (`BokehPass / Depth of Field`)
- **Exemplo Oficial**: `webgl_postprocessing_dof`.
- **Comportamento Visual**: Simula o comportamento físico de uma lente de cinema de grande abertura (ex: 50mm f/1.2). O objeto principal sob foco permanece perfeitamente nítido, enquanto elementos mais próximos ou distantes dissolvem-se em um desfoque óptico cremoso (*bokeh*).
- **Gatilho**: Mudança do ponto focal (`focusDistance`) acompanhando a rolagem do usuário ou o clique sobre um card específico.
- **Anatomia Técnica**:
  - Leitura do Depth Buffer linearizado.
  - Cálculo do Círculo de Confusão ($CoC = |z - \text{focus}| / z \times \text{aperture}$).
  - Filtro de dispersão circular para produzir círculos poligonais nos discos de desfoque.
- **Encaixe no Design**: Scrollytelling com profundidade de campo cinematográfica, dioramas tridimensionais e galerias de portfólio imersivas.

---

### 9. Streaming Otimizado de Malhas com Compressão Draco e Meshopt
- **Exemplo Oficial**: `webgl_loader_gltf_compressed`.
- **Comportamento Visual**: Carregamento instantâneo de modelos 3D ultra-detalhados (com centenas de milhares de polígonos) sem causar travamento na thread principal do navegador.
- **Gatilho**: Montagem da página ou carregamento sob demanda via `IntersectionObserver`.
- **Anatomia Técnica**:
  - `DRACOLoader`: decodifica geometrias compactadas via WebAssembly (WASM) em uma Web Worker separada, reduzindo o tamanho de arquivo em até 85%.
  - `MeshoptDecoder`: alternativa de altíssima descompressão que preserva os vetores de cache de vértices da GPU para renderização imediata.
- **Encaixe no Design**: Modelos CAD industriais, avatares digitais e réplicas digitais de produtos de varejo.

---

### 10. Coreografia de Câmera em Trilhos Tridimensionais (Spline Path Scrollytelling)
- **Exemplo Oficial**: `webgl_geometry_extrude_splines`.
- **Comportamento Visual**: A câmera de visão navega com suavidade infinita ao longo de uma curva tridimensional complexa através de salas virtuais ou detalhes de um produto, orientando seu vetor de visualização (`lookAt`) dinamicamente.
- **Gatilho**: Progresso normalizado de rolagem (`scrollProgress` $\in [0, 1]$ do Lenis ou GSAP ScrollTrigger).
- **Anatomia Técnica**:
  - `CatmullRomCurve3([vec3_1, vec3_2, ... vec3_n])`.
  - `curve.getPointAt(t, targetVector)` calcula a posição exata da câmera no tempo normalizado $t$.
  - Interpolação esférica (SLERP) entre quaternions para rotações contínuas sem o efeito de *Gimbal Lock*.
- **Encaixe no Design**: Narrativas imersivas corporativas, passeios virtuais de lançamento de produtos de luxo e apresentações institucionais.

---

## 5. Matemática do Movimento & Receitas de Código

### A Física e Óptica dos Shaders de Transmissão

A fidelidade de um material de vidro como o `MeshPhysicalMaterial` depende de três equações fundamentais da termodinâmica e da óptica clássica:

#### 1. Lei de Snell-Descartes da Refração
Descreve a curvatura de um raio de luz ao passar do ar (meio 1, $n_1 \approx 1.0$) para o vidro (meio 2, $n_2 = 1.52$):

$$n_1 \sin(\theta_1) = n_2 \sin(\theta_2) \implies \theta_2 = \arcsin\left(\frac{n_1}{n_2} \sin(\theta_1)\right)$$

#### 2. Aproximação de Fresnel de Schlick
Determina a proporção de luz que é refletida na superfície versus a proporção que refrata para dentro do material, com base no ângulo de incidência $\theta$:

$$F(\theta) = F_0 + (1 - F_0)(1 - \cos\theta)^5$$

Onde $F_0 = \left(\frac{n_1 - n_2}{n_1 + n_2}\right)^2$. Para vidro em ar, $F_0 \approx 0.04$ (4% de reflexão perpendicular, tendendo a 100% em ângulos rasantes).

#### 3. Lei de Absorção Volumétrica de Beer-Lambert
Determina como a intensidade da luz decai e altera sua cor à medida que penetra na profundidade $d$ (regida por `thickness` e `attenuationColor`):

$$I(d) = I_0 \cdot e^{-\alpha d}$$

Onde $\alpha$ é o coeficiente de atenuação espectral do material.

---

### Parâmetros de Amortecimento de Câmera e Springs

Para garantir que a interação do usuário seja macia e natural sem parecer mecânica ou artificial:

```javascript
// Configuração matemática ideal para OrbitControls / Camera Movement
export const CAMERA_PHYSICS = {
  dampingFactor: 0.045,        // Coeficiente de atrito inercial
  rotateSpeed: 0.65,           // Multiplicador de sensibilidade angular
  zoomSpeed: 0.8,              // Multiplicador de zoom sem aceleração destrutiva
  minDistance: 3.5,            // Limite de segurança de aproximação
  maxDistance: 18.0,           // Limite de afastamento para não descarregar frustum
  maxPolarAngle: Math.PI / 2 + 0.1, // Evita que a câmera passe por baixo do chão
};

// Configuração de Spring Física (React-Spring / Framer Motion 3D)
export const SPRING_ORBIT_CONFIG = {
  mass: 1.2,                   // Inércia perceptível (peso do objeto)
  tension: 140,                // Rigidez elástica moderada
  friction: 26,                // Amortecimento para evitar oscilações infinitas
  precision: 0.001
};
```

---

### Boilerplate Funcional Completo: Hero 3D Showstopper com React Three Fiber & Drei

Abaixo está a implementação padrão-ouro para uma seção Hero moderna utilizando **React Three Fiber**, materiais físicos refrativos (`MeshTransmissionMaterial` do `@react-three/drei`), iluminação baseada em imagem HDR (`Environment`), efeito de flutuação inercial (`Float`) e post-processing seletivo (`Bloom`).

```tsx
// HeroScene3D.tsx — Implementação de Alto Desempenho para Landing Pages Modernas
'use client';

import React, { Suspense, useRef } from 'react';
import { Canvas, useFrame } from '@react-three/fiber';
import { 
  Environment, 
  Float, 
  MeshTransmissionMaterial, 
  OrbitControls, 
  ContactShadows, 
  AdaptiveDpr, 
  BakeShadows,
  Preload
} from '@react-three/drei';
import { EffectComposer, Bloom, ToneMapping } from '@react-three/postprocessing';
import * as THREE from 'three';

// 1. Núcleo Interno Refrativo (Geometria Escultural)
function RefractiveCrystal() {
  const meshRef = useRef<THREE.Mesh>(null!);

  // Rotação suave contínua acoplada ao relógio delta da GPU
  useFrame((state, delta) => {
    meshRef.current.rotation.x += delta * 0.15;
    meshRef.current.rotation.y += delta * 0.22;
  });

  return (
    <Float speed={2.5} rotationIntensity={0.8} floatIntensity={1.2}>
      {/* Geometria de Icosaedro Chanfrado */}
      <mesh ref={meshRef} position={[0, 0, 0]} castShadow>
        <icosahedronGeometry args={[1.6, 0]} />
        
        {/* Material de Transmissão Física de Nível de Cinema */}
        <MeshTransmissionMaterial
          backside={false}            // Dupla refração interna desativada para ganho de 40% de FPS
          samples={8}                 // Amostras de raymarching (equilíbrio ideal entre ruído e FPS)
          resolution={512}            // Resolução do FBO de refração
          transmission={0.96}         // Transparência de passagem quase pura
          roughness={0.08}            // Superfície polida com micro-reflexos nítidos
          thickness={1.4}             // Profundidade óptica do corpo geométrico
          ior={1.54}                  // Índice de refração para vidro de alta densidade
          chromaticAberration={0.06}  // Separação de canais RGB nas arestas angulares
          anisotropy={0.3}            // Distorção alongada de reflexão
          distortion={0.2}            // Turbulência de onda na refração interna
          distortionScale={0.3}
          temporalDistortion={0.1}
          attenuationDistance={1.2}   // Distância de absorção de luz
          attenuationColor="#ffffff"  // Cor do núcleo refrativo
          color="#f1f5f9"
        />
      </mesh>
    </Float>
  );
}

// 2. Anéis Orbitais com Emissão HDR para Bloom Seletivo
function OrbitalEnergyRings() {
  const ringGroupRef = useRef<THREE.Group>(null!);

  useFrame((_, delta) => {
    ringGroupRef.current.rotation.z -= delta * 0.18;
    ringGroupRef.current.rotation.x += delta * 0.08;
  });

  return (
    <group ref={ringGroupRef}>
      {/* Anel 1 — Emissão Ciano */}
      <mesh rotation={[Math.PI / 4, 0, 0]}>
        <torusGeometry args={[2.5, 0.025, 16, 100]} />
        <meshStandardMaterial 
          color="#06b6d4" 
          emissive="#06b6d4" 
          emissiveIntensity={3.5} // Dispara o limiar do UnrealBloomPass
          roughness={0.2} 
        />
      </mesh>

      {/* Anel 2 — Emissão Âmbar/Violeta */}
      <mesh rotation={[-Math.PI / 3, Math.PI / 6, 0]}>
        <torusGeometry args={[3.2, 0.02, 16, 100]} />
        <meshStandardMaterial 
          color="#8b5cf6" 
          emissive="#8b5cf6" 
          emissiveIntensity={2.8} 
          roughness={0.2} 
        />
      </mesh>
    </group>
  );
}

// 3. Componente Raiz de Cena com Canvas e Fallbacks de Hardware
export default function HeroScene3D() {
  return (
    <div className="relative w-full h-[600px] lg:h-[750px] bg-slate-950 overflow-hidden select-none">
      {/* Camada 1: Canvas WebGL Three.js */}
      <Canvas
        camera={{ position: [0, 1.5, 6.5], fov: 42 }}
        dpr={[1, 2]} // Limita a 2x DPR para proteger monitores Retina de 4K
        gl={{
          antialias: false, // Antialias desativado no render inicial pois o FXAA/Bloom pós-processa
          powerPreference: 'high-performance',
          toneMapping: THREE.ACESFilmicToneMapping,
          toneMappingExposure: 1.1,
          alpha: true,
        }}
        className="absolute inset-0 z-0"
      >
        <Suspense fallback={null}>
          {/* Otimizador Adaptativo de Resolução para Hardware Fraco */}
          <AdaptiveDpr pixelated />

          {/* Iluminação Fotométrica de Estúdio */}
          <ambientLight intensity={0.5} />
          <directionalLight position={[10, 10, 5]} intensity={1.8} castShadow />
          <pointLight position={[-10, -10, -5]} intensity={0.8} color="#06b6d4" />

          {/* Ambiente HDRI para Reflexões e Transmissão Óptica */}
          <Environment preset="city" environmentIntensity={0.9} />

          {/* Elementos Centrais de Cena */}
          <group position={[0, 0.2, 0]}>
            <RefractiveCrystal />
            <OrbitalEnergyRings />
          </group>

          {/* Sombra de Contato Suave no Solo Virtual */}
          <ContactShadows 
            position={[0, -2.2, 0]} 
            opacity={0.65} 
            scale={12} 
            blur={2.4} 
            far={4} 
            color="#020617" 
          />

          {/* Controles Orbitais Amortecidos */}
          <OrbitControls
            enablePan={false}
            enableZoom={false}
            autoRotate
            autoRotateSpeed={0.8}
            dampingFactor={0.05}
            maxPolarAngle={Math.PI / 2 + 0.05}
            minPolarAngle={Math.PI / 3}
          />

          {/* Pipeline de Pós-Processamento Cinemático */}
          <EffectComposer multisampling={0} disableNormalPass>
            <Bloom 
              luminanceThreshold={0.88} // Apenas materiais com alta emissão recebem a aura
              luminanceSmoothing={0.2} 
              intensity={0.8} 
              mipmapBlur 
            />
            <ToneMapping />
          </EffectComposer>

          {/* Pré-carregamento de Buffers */}
          <BakeShadows />
          <Preload all />
        </Suspense>
      </Canvas>

      {/* Camada 2: Overlay de Conteúdo HTML Perfeitamente Acessível */}
      <div className="absolute inset-0 z-10 pointer-events-none flex flex-col items-center justify-center p-6 text-center">
        <div className="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-slate-900/60 border border-slate-800 backdrop-blur-md mb-6">
          <span className="w-2 h-2 rounded-full bg-cyan-400 animate-pulse" />
          <span className="text-xs font-mono font-medium text-slate-300 uppercase tracking-widest">
            Next-Gen Optical Core
          </span>
        </div>

        <h1 className="text-4xl sm:text-6xl lg:text-7xl font-bold tracking-tight text-white max-w-3xl drop-shadow-sm">
          A precisão da luz no coração da interface.
        </h1>

        <p className="mt-4 text-base sm:text-lg text-slate-400 max-w-xl leading-relaxed">
          Arquitetura visual renderizada em tempo real com materiais físicos refrativos e computação gráfica de baixa latência.
        </p>

        <div className="mt-8 flex gap-4 pointer-events-auto">
          <button className="px-6 py-3 rounded-lg bg-cyan-500 hover:bg-cyan-400 text-slate-950 font-semibold text-sm transition-all duration-200 shadow-[0_0_25px_rgba(6,182,212,0.4)] active:scale-95">
            Explorar Tecnologia
          </button>
          <button className="px-6 py-3 rounded-lg bg-slate-900/80 hover:bg-slate-800 text-slate-200 border border-slate-700/80 font-semibold text-sm backdrop-blur-sm transition-all duration-200 active:scale-95">
            Documentação Técnica
          </button>
        </div>
      </div>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir o plano arquitetural técnico (`DESIGN_BLUEPRINT.md`) de qualquer projeto que incorpore Three.js ou React Three Fiber, os agentes de IA devem especificar rigorosamente os seguintes parâmetros:

### 1. Critérios de Seleção do Backend de Renderização
- **WebGL2 Padrão**: Recomendado para aplicações que exigem suporte a 99% dos navegadores atuais em produção (Safari Mobile, Chrome Android, Firefox Desktop).
- **WebGPU + TSL**: Especificar exclusivamente para projetos experimentais ou de computação pesada na GPU (ex: mais de 100.000 partículas físicas, cálculos de física via compute shaders sem passar pela CPU).

### 2. Matriz de Orçamento Gráfico Obrigatória (Performance Budget)
- **Teto Máximo de Polígonos**: Indicar claramente o limite (`Desktop <= 300k faces`, `Mobile <= 50k faces`).
- **Teto de Draw Calls**: Não ultrapassar 40 draw calls por frame (utilizar `InstancedMesh` ou `BufferGeometryUtils.mergeGeometries`).
- **Orçamento de Texturas**: Indicar formato de entrega comprimido (`.ktx2` via Basis Universal ou `.webp` com mipmaps gerados). Proibir texturas PNG brutas de 4K.
- **Passes de Pós-Processamento**: Limitar a um máximo de 2 passes no mobile (`ToneMapping` + opcionalmente `Bloom` com `mipmapBlur: true`). Proibir Screen-Space Reflections (SSR) volumétricos em resoluções acima de 1080p sem downsampling de meio buffer.

### 3. Checklist de Engenharia e Integridade de Interface
- [ ] O canvas WebGL possui a classe CSS `pointer-events-none` caso haja elementos clicáveis do DOM abaixo ou acima dele?
- [ ] O componente 3D implementa limpeza explícita de memória (`disposeHierarchy` ou descarte automático de nós do R3F no ciclo de unmount)?
- [ ] O loop de animação respeita a query de acessibilidade `(prefers-reduced-motion: reduce)` congelando rotações automáticas?
- [ ] Existe uma imagem estática ou gradiente CSS estático servindo como fallback caso o contexto WebGL falhe (`webglcontextlost`) ou o WebAssembly do Draco falhe ao carregar?
- [ ] As fontes e textos críticos da página estão declarados em HTML semântico com contraste compatível com WCAG AA, e nunca rasterizados como pixels em uma textura de canvas?
