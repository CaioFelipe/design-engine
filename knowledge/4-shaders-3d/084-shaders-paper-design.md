---
id: "084-shaders-paper-design"
name: "Paper Design Shaders (@paper-design/shaders & @paper-design/shaders-react)"
url: "https://shaders.paper.design/"
category: "4-shaders-3d"
schema_type: "B-motion-shaders"
dna_estetico: ["Zero-Dependency WebGL2 Architecture", "High-End Procedural Noise (Simplex, Perlin, Voronoi)", "Analog Grain & Dithering Textures", "Domain Warping & Fluid Mesh Dynamics", "Optical Glass Refraction & Liquid Metal Dispersion", "Resource-Aware RAF Throttling (IntersectionObserver / Visibility API)"]
densidade_informacao: "Independente"
impacto_visual: "Cinematografico/Showstopper"
custo_computacional: "Baixo a Medio (Zero-Dependency WebGL2 Quad com Throttling e DPR Clamping nativo)"
stack_frameworks: ["Vanilla JavaScript / TypeScript (@paper-design/shaders)", "React 18/19 (@paper-design/shaders-react)", "Next.js (App Router / Client Component)", "WebGL 2.0 (GLSL ES 3.00)", "Tailwind CSS v4", "Motion.dev / Framer Motion"]
compatibilidade:
  combinacoes_recomendadas: ["Paper Shaders + Tailwind CSS v4 (Design Tokens & Color Arrays)", "Paper Shaders + Motion.dev (Spring-driven Uniform Interpolation)", "Paper Shaders + Lenis Smooth Scroll (Parallax & Velocity Coupling)", "Paper Shaders + Radix UI / Shadcn (Backdrop Texturing & Card Borders)"]
  conflitos_esteticos: ["Multiplicação excessiva de nós WebGL em viewport simultâneo (ultrapassar limite de 8-16 WebGL contexts do browser)", "Ausência de controle prefers-reduced-motion deixando animações contínuas a 60fps para usuários sensíveis", "Sobreposição de gradientes fluorescentes sob tipografia de baixo contraste sem máscara de escurecimento ou scrim", "Renderização em telas Retina 3x sem capping de maxPixelCount causando estouro de fill-rate da GPU"]
---

# Paper Design Shaders — Dossiê de Shaders WebGL2, Física Procedural & Computação Gráfica Ultraleve

## 1. Filosofia de Movimento & Sensação Física (Feel)

O ecossistema **Paper Design Shaders** (`https://shaders.paper.design/`), desenvolvido pela equipe da **Paper** (`paper.design` — liderada por Vlad Moroz, Stephen Haney, Ksenya Kondrashova e Madou), representa a superação definitiva de um dos maiores dilemas da Creative Technology contemporânea: **como trazer a magnificência visual de fragment shaders cinematográficos para interfaces web sem arrastar o peso titânico, a complexidade estrutural e os riscos de vazamento de memória dos motores 3D tradicionais**.

Disponibilizado como software livre sob a licença **Apache-2.0** nos pacotes `@paper-design/shaders` (Vanilla JS/TS) e `@paper-design/shaders-react` (React 18 e 19), o Paper Shaders introduz uma arquitetura de renderização **zero-dependency WebGL2** desenhada com rigor estético de alta-costura digital.

---

### A Ruptura: O Fim do Overhead Monolítico do Three.js para Planos de Fundo 2D

Durante quase uma década, desenvolvedores e designers que buscavam enriquecer websites com gradientes líquidos, deformações orgânicas, aberrações ópticas e texturas de vidro foram coagidos a utilizar ecossistemas monumentais como **Three.js** ou **React Three Fiber (R3F)**. Essa escolha trazia um custo desproporcional para a experiência do usuário:

```
┌────────────────────────────────────────────────────────────────────────┐
│        PARADIGMA LEGADO (THREE.JS / R3F PARA BACKGROUND SHADERS)       │
└────────────────────────────────────────────────────────────────────────┘
  [Bundle Size: > 600 KB min/gzip]
       │
       ▼ Overhead Arquitetural Desnecessário:
  [Scenegraph Complexo + Árvores de Hierarquia Matricial (Matrix4)]
  [Câmeras Ortográficas / Perspectivas + Vetores de Frustum Culling]
  [Sistemas de Iluminação PBR (DirectionalLight, AmbientLight, Shadows)]
  [Alocação Contínua de Geometrias e Malhas de Vértices Desperdiçadas]
       │
       ├── ❌ Penalização severa de First Contentful Paint (FCP) e TBT
       ├── ❌ Garbage Collection agressivo gerado por instâncias de objetos efêmeros
       └── ❌ Complexidade desmedida para desenhar um simples retângulo de pixels
```

Em contraste absoluto, o Paper Shaders reconhece uma verdade fundamental da computação gráfica na web: **se o objetivo é renderizar um efeito de superfície, ruído fractal, distorção de imagem ou gradiente contínuo, a geometria tridimensional é inteiramente supérflua**.

```
┌────────────────────────────────────────────────────────────────────────┐
│             PARADIGMA PAPER SHADERS (ZERO-DEPENDENCY WEBGL2)           │
└────────────────────────────────────────────────────────────────────────┘
  [Bundle Size: ~30 KB (Zero Dependências Externas)]
       │
       ▼ Primitiva Elementar: Fullscreen Quad (2 Triângulos / 4 Vértices)
  [Vertex Shader Ultraleve: Mapeia Resolução, Pixel Ratio e UV Coordinates]
       │
       ▼ Computação Paralela Pura no Fragment Shader (GLSL ES 3.00)
  [Cálculo Analítico de Ruído Procedural (Simplex, Perlin, Voronoi)]
  [Distorção de Domínio (Domain Warping), Cáusticas e Refração Per-Pixel]
       │
       ├── ✅ Zero dependências de terceiros (WebGL2 nativo do navegador)
       ├── ✅ Consumo irrisório de CPU: lógica inteiramente transferida para os núcleos da GPU
       ├── ✅ Antialiasing automático e adaptação sub-pixel contínua
       └── ✅ Ciclo de vida com descarte de recursos de GPU determinístico (dispose)
```

---

### A Sensação Cinestésica (Feel): Da Estática Plástica à Matéria Digital Viva

O gradiente CSS tradicional (`linear-gradient` ou `radial-gradient`) padece de limitações ópticas crônicas:
- **Banding de 8 bits**: Degraus visuais perceptíveis entre bandas de cores similares devido à quantização cromática do navegador.
- **Linearidade Rígida**: Transições matemáticas estáticas, uniformes e sem vida orgânica, transmitindo a sensação de um plástico inanimado colado à tela.

O Paper Shaders substitui o conceito de "cor estática" pelo de **"matéria dinâmica ativa"**:
1. **Distorção de Domínio e Convecção Térmica**: Efeitos como `MeshGradient`, `Warp` e `Swirl` não apenas interpolam tonalidades; eles perturbam as coordenadas UV locais por meio de campos de ruído fractal entrelaçados. O resultado visual evoca convecção atmosférica, tinta a óleo expandindo-se em água morna ou plasma luminoso em equilíbrio metaestável.
2. **Textura Tátil e Grão Analógico**: As primitivas `GrainGradient`, `PaperTexture` e `Dithering` reintroduzem deliberadamente o ruído estocástico de alta frequência (ruído azul, matrizes de Bayer e fibras vegetais). Essa micro-textura quebra a assepsia estéril dos displays OLED ultra-nítidos, conferindo peso tátil, calor editorial e sensação de materialidade física.
3. **Comportamento Óptico Fiel**: Modelos como `FlutedGlass` (vidro canelado/ondulado), `Water` (cáusticas hidrodinâmicas) e `LiquidMetal` (cromo líquido com dispersão cromática R/B) calculam vetores de refração reais da lei de Snell e curvas de reflexão de Fresnel diretamente no fragment shader, fazendo o usuário sentir a tela como uma lente de cristal ou uma lâmina de mercúrio.

---

### Governança de Hardware Consciente (Eco-WebGL & Zero-Waste Rendering)

Diferente de muitas soluções de shaders amadoras que mantêm laços de renderização perpétuos consumindo ciclos de GPU desnecessariamente, o Paper Shaders implementa no núcleo do seu componente `ShaderMount` uma arquitetura sofisticada de contenção energética:

1. **Throttling Automático por `IntersectionObserver`**:
   O elemento monitora seu enquadramento na janela de visualização (`isInViewport`). Quando o usuário rola a página e o canvas sai do viewport, o laço de animação `requestAnimationFrame` (RAF) é **imediatamente suspenso**. O consumo de processamento da GPU cai a zero até que o elemento retorne à vista.
2. **Pausa Instantânea em Abas Inativas (`DocumentVisibilityChange`)**:
   Ao alternar de aba ou minimizar a janela (`document.hidden === true`), o motor congela instantaneamente o avanço temporal (`currentSpeed = 0`). Usuários com 50 abas abertas não sofrem perda de bateria ou aquecimento térmico.
3. **Modo Estático Sem Custo Contínuo (`speed = 0`)**:
   Ao configurar `speed={0}`, o motor desenha o quadro único no canvas e cancela a inscrição no laço RAF. O shader atua como uma obra gráfica gerada proceduralmente de altíssima definição com **custo de GPU contínuo rigorosamente nulo**. Caso alguma propriedade mude no React, o método `renderUnlessAnimating()` executa um repasse pontual único.
4. **Controle Estrito de Fill-Rate (`maxPixelCount` e `minPixelRatio`)**:
   Em monitores 5K/6K ou dispositivos móveis Retina com escalas de pixel de 3x, renderizar fragment shaders complexos em tela cheia pode saturar a largura de banda de memória da GPU. O Paper Shaders estabelece por padrão um teto protetor de `maxPixelCount = 8.294.400` pixels (equivalente a uma tela 4K a 2x DPI), adaptando a resolução interna de forma imperceptível ao olho humano e salvaguardando taxas estáveis de 60/120fps.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Interface e Casos de Uso Críticos

1. **Hero Sections Cinematográficas e Portais de Marca (Brand Anchors)**:
   Aberturas de páginas de alta conversão para produtos digitais premium, estúdios criativos, SaaS de ponta e fintechs. Componentes como `MeshGradient`, `GodRays` e `LiquidMetal` estabelecem autoridade estética instantânea, transformando a primeira impressão em um momento memorável de design.
2. **Backdrops Editoriais Sutis e Texturas Analógicas**:
   Plataformas de publicação, blogs técnicos sofisticados, relatórios anuais corporativos e portfólios de tipografia. Utilizando `PaperTexture` ou `GrainGradient` com velocidade desacelerada (`speed={0.15}`), a página adquire a densidade tátil de papel couchê ou linho impresso, eliminando a sensação genérica de "fundo cinza neutro".
3. **Cards Interativos, Contornos Vivos e Micro-Superfícies**:
   Contêineres de cartões de preço, modais de destaque e badges de status utilizando `PulsingBorder` ou `FlutedGlass`. O efeito delimita a hierarquia visual por meio de luminosidade difusa e distorção óptica localizada, guiando o olhar do usuário sem exigir alertas agressivos.
4. **Visualização de Dados Futurista, Cibersegurança & Interfaces de IA**:
   Telas de processamento de modelos neurais, dashboards de segurança e métricas biométricas com `NeuroNoise`, `Heatmap` e `Voronoi`. A visualização evoca conexões sinápticas ativas e fluxos contínuos de informação quântica.
5. **Destaque e Revelação de Logotipos Tridimensionais**:
   Marcas que buscam transpor seu símbolo gráfico para uma estética metálica ou de joalheria digital utilizando `LiquidMetal` ou `GemSmoke`. Ao fornecer a imagem vetorial ou PNG do logo, o shader aplica relevo de borda por transformada de distância (Poisson) e anima reflexos cromáticos dinâmicos.
6. **Tratamento de Mídia e Imagens Retrô / Cyberpunk**:
   Galerias fotográficas e avatares que aplicam `ImageDithering`, `HalftoneDots` ou `LensDistortion`. Permite renderizar fotos em tempo real com matrizes estocásticas de pontilhismo de jornal antigo ou aberrações esféricas de lentes anamórficas de cinema.

---

### A Regra 60-30-10 da Harmonia Visual

Na aplicação do Paper Shaders, a distribuição proporcional da interface deve seguir um controle estrito para evitar poluição sensorial:

| Proporção | Papel no Sistema de Design | Implementação com Paper Shaders |
| :--- | :--- | :--- |
| **60% (Base Estrutural)** | Calma, espaço negativo e legibilidade pura | DOM semântico HTML/Tailwind, fundo neutro ou escurecido sob o canvas, tipografia sólida e espaços em branco amplos. |
| **30% (Ambiência e Textura)** | Identidade, profundidade e sensação física contínua | Shaders ambientais (`MeshGradient`, `GrainGradient`, `SimplexNoise`) configurados com `speed: 0.1 ~ 0.3`, distorções suaves (`distortion: 0.4`) e sobreposição de grão fino (`grainOverlay: 0.12`). Atua como atmosfera subjacente. |
| **10% (Ponto Focal de Espetáculo)** | Foco de conversão, fascínio e pico visual | Elementos de alto contraste e energia: contorno do card de conversão com `PulsingBorder`, logo hero com `LiquidMetal` reagindo ao cursor ou botão CTA com `GodRays` radiante no estado de hover. |

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Quando Evitar
- **Tabelas de Dados Densas e Dashboards Transacionais**: Interfaces utilitárias com dezenas de linhas de dados dinâmicos, terminais de trading financeiro ou planilhas corporativas. A oscilação contínua de cores e gradientes compete com a atenção visual do operador e induz fadiga cognitiva precoce.
- **Proliferação Descontrolada de Contextos WebGL (O Limite de 8-16 Contextos)**:
  Navegadores como Google Chrome, Apple Safari e Mozilla Firefox impõem um limite físico rigoroso de **8 a 16 instâncias simultâneas de WebGLRenderingContext por aba**. Criar 30 cartões em um feed onde cada cartão monta sua própria tag `<MeshGradient>` causará a perda silenciosa de contexto (`webglcontextlost`), transformando os primeiros cartões em blocos pretos ou travando a GPU.
  > **Regra de Engenharia**: Nunca monte mais de 2 a 3 instâncias de shaders WebGL ativas concorrentemente na mesma tela. Utilize instâncias únicas para fundos globais e reutilize o mesmo canvas para múltiplas seções via scroll, ou opte por renderização estática (`speed={0}`).
- **Dispositivos Móveis de Entrada com Bateria Fraca**: Dispositivos com chipsets gráficos básicos (ex: Mali-G52 ou Adreno de série 600 em aparelhos low-end) sofrerão queda drástica de framerate caso shaders com ruído procedural de múltiplos passos rodem em tela inteira.

---

### ⚠️ Regras de Acessibilidade & GPU

1. **Acessibilidade Vestibular (`prefers-reduced-motion`)**:
   Usuários com distúrbios vestibulares, epilepsia fotossensível ou sensibilidade a movimento sentem vertigem e enxaqueca diante de campos fluidos contínuos. É **mandatório** detectar a preferência de sistema e configurar `speed={0}`:
   ```tsx
   import { useReducedMotion } from 'framer-motion';
   import { MeshGradient } from '@paper-design/shaders-react';

   export function AccessibleShader() {
     const shouldReduceMotion = useReducedMotion();
     return <MeshGradient speed={shouldReduceMotion ? 0 : 0.4} colors={['#0F172A', '#1E293B', '#334155']} />;
   }
   ```
2. **Garantia de Contraste Tipográfico WCAG AAA (Scrim de Proteção)**:
   Gradientes procedurais contêm pontos flutuantes de luminância imprevisível. Colocar texto branco diretamente sobre um `MeshGradient` sem tratamento levará a falhas de contraste quando áreas claras convergirem sob o texto. É obrigatório aplicar uma camada de scrim protetor (`bg-black/40 backdrop-blur-sm` ou máscara de gradiente CSS radial) separando o canvas do texto.
3. **Resiliência e Prevenção de Cumulative Layout Shift (CLS)**:
   Como o WebGL é inicializado assincronamente durante a montagem do lado do cliente (`useEffect`/`requestAnimationFrame`), garanta que o contêiner do componente tenha proporção e dimensões explícitas no CSS (`w-full h-[600px] relative overflow-hidden`), evitando saltos estruturais de página.
4. **Fallback Transparente para SSR (Server-Side Rendering)**:
   O código do `@paper-design/shaders-react` é seguro para SSR (aceita propriedades `undefined` e não toca no objeto `window` durante a compilação do servidor), gerando um `<div>` reservatório de espaço até a hidratação no cliente.

---

## 4. Catálogo Detalhado de Componentes, Efeitos & Primitivas Notáveis

A suíte `@paper-design/shaders` disponibiliza mais de 25 componentes e filtros especializados. Abaixo estão detalhadas as **12 primitivas mais expressivas e tecnicamente relevantes** para o design moderno:

---

### 1. `MeshGradient` & `StaticMeshGradient`
- **Comportamento Visual**: Renderiza uma composição líquida e contínua de até 10 pontos de cor móveis, impulsionados por trajetórias senoidais assíncronas e deformados por distorção de ruído orgânico e vórtice (*swirl*). Inclui pós-processamento de grão analógico.
- **Anatomia & Uniforms Chave**:
  - `u_colors` (`vec4[]`): Matriz de até 10 cores em formato RGBA.
  - `u_distortion` (`float`, 0 a 1): Força da deformação orgânica por ruído.
  - `u_swirl` (`float`, 0 a 1): Intensidade do turbilhão rotacional no centro.
  - `u_grainMixer` (`float`, 0 a 1): Grão procedimental misturado às bordas cromáticas.
  - `u_grainOverlay` (`float`, 0 a 1): Camada de grão preto e branco em modo de sobreposição.
- **Gatilho de Animação**: Loop contínuo temporal normalizado por `speed`. Reage a mudanças reativas de paleta de cores.
- **Presets Nativos Disponíveis**: `defaultPreset`, `purplePreset`, `beachPreset`, `inkPreset`.

---

### 2. `NeuroNoise`
- **Comportamento Visual**: Teia bioluminescente e pulsante de filamentos e sinapses neurais fluidas com intersecções orgânicas brilhantes. Evoca atividade biológica submicroscópica ou redes de dados cibernéticas. Baseado no aclamado algoritmo procedural de Arthur Zouaoui (*zozuar*).
- **Anatomia & Uniforms Chave**:
  - `u_colorFront` (`vec4`): Tonalidade das linhas de crista e pontos focais luminosos.
  - `u_colorMid` (`vec4`): Cor corporal das ramificações intermediárias.
  - `u_colorBack` (`vec4`): Fundo profundo do abismo espacial.
  - `u_brightness` (`float`, 0 a 1): Luminosidade e incandescência nos nós de cruzamento sináptico.
  - `u_contrast` (`float`, 0 a 1): Nitidez e gradiente de transição entre o meio e o fundo.
- **Gatilho de Animação**: Pulso contínuo temporal; ideal para hero sections com tema de IA ou biotecnologia.

---

### 3. `LiquidMetal`
- **Comportamento Visual**: Simula mercúrio líquido, titânio derretido ou cromo holográfico refletindo faixas de luz e cores dinâmicas. Pode ser aplicado a formas geométricas elementares (`circle`, `daisy`, `diamond`, `metaballs`) ou a um logotipo vetorial/PNG carregado pelo usuário, com cálculo de gradiente de borda via processador Poisson.
- **Anatomia & Uniforms Chave**:
  - `u_colorBack` & `u_colorTint`: Tonalidades de reflexão e luz ambiente.
  - `u_repetition` (`float`, 1 a 10): Densidade das faixas especulares de reflexo.
  - `u_softness` (`float`, 0 a 1): Transição entre reflexo nítido de espelho e alumínio acetinado.
  - `u_shiftRed` & `u_shiftBlue` (`float`, -1 a 1): Dispersão cromática (aberração prismática).
  - `u_contour` (`float`, 0 a 1): Curvatura da distorção ao redor das bordas da silhueta.
- **Gatilho de Animação**: Movimento oscilatório contínuo com direção de ângulo ajustável (`u_angle`).

---

### 4. `GodRays`
- **Comportamento Visual**: Feixes de luz volumétrica (crepuscular rays) irradiando a partir de um núcleo central ou ponto de fuga, fundindo até 5 camadas de cores com dispersão atmosférica e efeito de bloom aditivo.
- **Anatomia & Uniforms Chave**:
  - `u_colors` (`vec4[]`): Até 5 cores de feixe solar distribuídas angularmente.
  - `u_bloom` (`float`, 0 a 1): Modo de mesclagem (0 = transparência alfa suave, 1 = adição espectral intensa).
  - `u_density` (`float`, 0 a 1): Quantidade e frequência de feixes de luz.
  - `u_spotty` (`float`, 0 a 1): Comprimento dos feixes (valores altos criam partículas fragmentadas).
  - `u_midSize` & `u_midIntensity`: Diâmetro e incandescência da estrela/centro emissor.
- **Gatilho de Animação**: Rotação e emissão contínua; perfeito para revelações cinematográficas e portais místicos ou cósmicos.

---

### 5. `Metaballs`
- **Comportamento Visual**: Até 20 esferas viscosas e deformáveis que orbitam suavemente no espaço bidimensional e se fundem como gotas de óleo ou mercúrio quando aproximadas, através de campos escalares com suavização polinomial (*smooth minimum* / `smin`).
- **Anatomia & Uniforms Chave**:
  - `u_colors` (`vec4[]`): Até 8 cores distribuídas sequencialmente pelas esferas.
  - `u_count` (`float`, 1 a 20): Quantidade exata de esferas (valores fracionários reduzem suavemente a escala da última esfera).
  - `u_size` (`float`, 0 a 1): Raio individual de atração e fusão de cada núcleo.
  - `u_noiseTexture` (`sampler2D`): Textura de ruído de alta velocidade para perturbação de borda.
- **Gatilho de Animação**: Trajetórias orbitais contínuas em RAF; ideal para loaders sofisticados ou fundos dinâmicos lúdicos.

---

### 6. `FlutedGlass`
- **Comportamento Visual**: Filtro de distorção óptica que replica o efeito de vidros canelados, frisados ou prismáticos (vidro morroquino, canelado arquitetônico e estriado). Pode distorcer uma imagem fornecida ou texturas sob a camada de renderização, criando uma sensação luxuosa de privacidade e mistério.
- **Anatomia & Uniforms Chave**:
  - `u_image` (`sampler2D`): Imagem ou textura de entrada a ser refratada.
  - `GlassDistortionShapes`: Perfis de curvatura do friso (ondulado, triangular, quadrado).
  - `GlassGridShapes`: Orientação e geometria do relevo (linhas verticais, horizontais ou malhas cruzadas).
- **Gatilho de Animação**: Estático ou acoplado ao deslocamento do cursor e scroll da página.

---

### 7. `GrainGradient`
- **Comportamento Visual**: Gradiente fluido multifacetado impregnado com estática e grão orgânico em 7 topologias abstratas geométricas distintas: onda (`wave`), pontos (`dots`), mosaico de Truchet (`truchet`), cantos (`corners`), ondulação radial (`ripple`), gota viscosa (`blob`) e esfera volumétrica (`sphere`).
- **Anatomia & Uniforms Chave**:
  - `u_colors` (`vec4[]`): Até 7 cores saturadas ou tonais.
  - `u_shape` (`float`, 1 a 7): Seleciona a topologia matemática de distribuição.
  - `u_intensity` (`float`, 0 a 1): Distorção e tensão superficial entre as faixas de cor.
  - `u_noise` (`float`, 0 a 1): Densidade e aspereza do grão tátil.
- **Gatilho de Animação**: Movimento ondulatório fluido e estocástico per-pixel.

---

### 8. `PulsingBorder`
- **Comportamento Visual**: Rastro luminoso pulsante que percorre o contorno de uma moldura geométrica arredondada (card ou modal), fundindo até 5 cores em um feixe de neon dinâmico com cauda de fumaça suave e efeito de bloom expansivo.
- **Anatomia & Uniforms Chave**:
  - `u_roundness` (`float`, 0 a 1): Raio de curvatura dos cantos (border-radius proporcional).
  - `u_thickness` (`float`, 0 a 1): Espessura base da trilha de contorno.
  - `u_spots` (`float`, 1 a 4) & `u_spotSize`: Número de focos luminosos e sua extensão angular.
  - `u_pulse` (`float`, 0 a 1): Força da oscilação rítmica de respiração de luz.
  - `u_smoke` & `u_smokeSize`: Dispersão de névoa luminosa expandindo-se além do vetor da borda.
- **Gatilho de Animação**: Órbita luminosa contínua ao redor da moldura; ideal para cards "Featured", caixas de planos e botões de chamada.

---

### 9. `Dithering` & `ImageDithering`
- **Comportamento Visual**: Converte gradientes contínuos ou imagens fotográficas em padrões gráficos pontilhados retrô de duas ou múltiplas cores, emulando impressões de fotolito, telas de Game Boy ou estética computacional do início dos anos 1990 com matrizes ordenadas (Bayer 2x2, 4x4, 8x8) ou ruído azul disperso.
- **Anatomia & Uniforms Chave**:
  - `DitheringShapes`: Base matemática subjacente (ruído, ondas, ondulação, vórtice, esfera).
  - `DitheringTypes`: Algoritmo de quantização e padrão da matriz estocástica.
  - `colors`: Duas cores contrastantes de alto impacto (ex: preto e amarelo elétrico).
- **Gatilho de Animação**: Ondulação fluida das matrizes de dispersão sob passagem de tempo.

---

### 10. `PaperTexture`
- **Comportamento Visual**: Renderização procedural multicamada de superfícies físicas de papel kraft, papelão prensado ou folhas de aquarela, reproduzindo dobras estruturais (`crumples`), rugas microscópicas (`wrinkles`), sombras de relevo e absorção de luz difusa.
- **Anatomia & Uniforms Chave**:
  - `colorPaper`, `colorShadow`, `colorBack`: Paleta tricromática de iluminação difusa e oclusão de sulcos.
  - `crumples` & `crumpleCount`: Grandes dobras de amassamento estrutural do papel.
  - `wrinkles` & `wrinkleSize`: Fibras têxteis e microporosidades táteis.
  - `blending` & `distortion`: Taxa de adesão e dobra caso uma imagem esteja sendo impressa sobre o papel.
- **Gatilho de Animação**: Normalmente estático (`speed: 0`), conferindo realismo físico estático a páginas editoriais.

---

### 11. `SimplexNoise`
- **Comportamento Visual**: Campo contínuo de ruído Simplex multidimensional sem costuras, que mapeia faixas tonais em curvas sinuosas que deslizam como dunas de areia líquida ou camadas geológicas iluminadas.
- **Anatomia & Uniforms Chave**:
  - `colors` (`string[]`): Paleta de tons interpolados.
  - `stepsPerColor` (`number`): Quantidade de subdivisões tonais intermediárias entre cada cor base.
  - `softness` (`number`, 0 a 1): Grau de difusão entre as curvas de nível do relevo de ruído.
  - `scale` (`number`): Escala de zoom espacial do campo de ruído.
- **Gatilho de Animação**: Deriva contínua no espaço tridimensional de ruído procedural.

---

### 12. `Water`
- **Comportamento Visual**: Simulação óptica de superfície aquática em movimento, modelando refração de luz subaquática, faixas de reflexão cáustica com distorção tridimensional e atenuação por profundidade.
- **Anatomia & Uniforms Chave**:
  - Operação com imagem ou gerador puro de malha de água.
  - Distorção vetorial e cálculo de ângulo de incidência solar.
- **Gatilho de Animação**: Turbulência hidrodinâmica contínua; ideal para seções de luxo, temas de sustentabilidade e ambientes serenos.

---

## 5. Arquitetura Técnica, Física de Movimento & Receitas de Código

### Parâmetros Globais de Geometria, Escala e Movimento

Todos os componentes da suíte Paper Shaders compartilham uma estrutura matemática unificada gerenciada pelo `ShaderSizingParams` e `ShaderMotionParams`:

| Uniform / Propriedade | Tipo | Intervalo Típico | Papel no Pipeline WebGL2 |
| :--- | :--- | :--- | :--- |
| **`speed`** | `float` | `-2.0` a `2.0` (Default: `0.5 ~ 1.0`) | Multiplicador de tempo `u_time`. Valores negativos revertem o fluxo. Se `0`, congela o loop RAF. |
| **`frame`** | `number` | Inteiro em milissegundos | Define o ponto de partida temporal. Permite renderizações estáticas determinísticas idênticas. |
| **`fit`** | `string` | `'cover'` \| `'contain'` \| `'none'` | Normalização de enquadramento da textura no canvas (0 = none, 1 = contain, 2 = cover). |
| **`scale`** | `float` | `0.01` a `4.0` (Default: `1.0`) | Nível de zoom óptico global das coordenadas UV antes da avaliação do fragment shader. |
| **`rotation`** | `float` | `0.0` a `360.0` graus | Rotação vetorial aplicada ao espaço de coordenadas UV em torno da origem configurada. |
| **`originX` / `originY`** | `float` | `0.0` a `1.0` (Default: `0.5`) | Âncora de referência para posicionamento e rotação no plano cartesiano do canvas. |
| **`offsetX` / `offsetY`** | `float` | `-1.0` a `1.0` | Translação espacial da textura em relação ao centro de projeção da tela. |
| **`minPixelRatio`** | `number` | `1.0` a `2.0` (Default: `2.0`) | Garante amostragem sub-pixel de alta fidelidade mesmo em telas com densidade de 1x. |
| **`maxPixelCount`** | `number` | Padrão: `8.294.400` | Teto físico de pixels renderizados para impedir degradação de performance em monitores 5K+. |

---

### Integração Física: Interpolação de Uniforms com Molas (Springs)

Ao criar reatividade ao cursor (ex: o mouse deforma o `distortion` ou o `swirl` do shader), evite passar valores brutos de eventos de ponteiro para o componente React. A resposta mecânica direta parece truncada. Utilize molas físicas amortecidas com **Motion.dev** ou **Framer Motion**:

```ts
// Configuração recomendada de física elástica para modulação de shaders:
const shaderSpringConfig = {
  stiffness: 120, // Firmeza do retorno elástico
  damping: 18,    // Amortecimento sem oscilação excessiva (critically damped feel)
  mass: 1.0,      // Peso inercial moderado
  restDelta: 0.001
};
```

---

### Receita de Código 1: Hero Section Cinematográfica com `MeshGradient` (React 19 + Tailwind v4)

Esta implementação demonstra a criação de uma seção hero completa de estúdio criativo, com suporte integral a `prefers-reduced-motion`, scrim protetor para acessibilidade de contraste, design tokens mapeados e montagem performática.

```tsx
'use client';

import React, { useId, useState, useEffect } from 'react';
import { MeshGradient, defaultPreset } from '@paper-design/shaders-react';

export interface HeroCinematicProps {
  headline: string;
  subheadline: string;
  ctaText: string;
  onCtaClick?: () => void;
}

export function HeroCinematic({
  headline,
  subheadline,
  ctaText,
  onCtaClick,
}: HeroCinematicProps) {
  const [prefersReducedMotion, setPrefersReducedMotion] = useState(false);
  const [isMounted, setIsMounted] = useState(false);

  // Paleta de alta sofisticação cromática (Índigo Profundo, Violeta Noturno e Brilho Esmeralda)
  const palette = [
    '#0B0C10', // Preto grafite de fundo
    '#1F2833', // Azul aço profundo
    '#45A29E', // Ciano petróleo atenuado
    '#66FCF1', // Ponto focal luminoso elétrico
    '#1B1534', // Sombra ultravioleta
  ];

  useEffect(() => {
    setIsMounted(true);
    const mediaQuery = window.matchMedia('(prefers-reduced-motion: reduce)');
    setPrefersReducedMotion(mediaQuery.matches);

    const handleChange = (e: MediaQueryListEvent) => setPrefersReducedMotion(e.matches);
    mediaQuery.addEventListener('change', handleChange);
    return () => mediaQuery.removeEventListener('change', handleChange);
  }, []);

  return (
    <section 
      aria-label="Apresentação Principal"
      className="relative flex min-h-[90vh] w-full items-center justify-center overflow-hidden bg-[#0B0C10]"
    >
      {/* Camada do Shader WebGL2 Zero-Dependency */}
      {isMounted && (
        <div 
          className="absolute inset-0 z-0 pointer-events-none opacity-90 transition-opacity duration-1000"
          aria-hidden="true"
        >
          <MeshGradient
            colors={palette}
            distortion={0.65}
            swirl={0.35}
            grainMixer={0.25}
            grainOverlay={0.12}
            speed={prefersReducedMotion ? 0 : 0.45}
            scale={1.1}
            fit="cover"
            style={{ width: '100%', height: '100%' }}
            minPixelRatio={1.5}
            maxPixelCount={4147200} // Limite de 2K para economia energética máxima
          />
        </div>
      )}

      {/* Scrim Óptico: Máscara radial e escurecimento para contraste WCAG AAA */}
      <div 
        className="absolute inset-0 z-10 bg-gradient-to-b from-[#0B0C10]/40 via-transparent to-[#0B0C10] backdrop-blur-[2px]" 
        aria-hidden="true" 
      />

      {/* Conteúdo Tipográfico e Chamadas de Ação */}
      <div className="relative z-20 mx-auto max-w-5xl px-6 py-24 text-center">
        <span className="inline-flex items-center gap-2 rounded-full border border-white/10 bg-white/5 px-4 py-1.5 text-xs font-medium tracking-wide text-cyan-300 backdrop-blur-md">
          <span className="h-1.5 w-1.5 rounded-full bg-cyan-400 animate-pulse" />
          WebGL2 Generative Architecture
        </span>

        <h1 className="mt-8 text-5xl font-extrabold tracking-tight text-white sm:text-7xl lg:text-8xl">
          {headline}
        </h1>

        <p className="mx-auto mt-6 max-w-2xl text-lg font-light leading-relaxed text-slate-300 sm:text-xl">
          {subheadline}
        </p>

        <div className="mt-10 flex flex-wrap items-center justify-center gap-4">
          <button
            type="button"
            onClick={onCtaClick}
            className="group relative inline-flex items-center justify-center rounded-xl bg-cyan-400 px-8 py-4 text-sm font-semibold text-slate-950 shadow-lg shadow-cyan-500/25 transition-all duration-300 hover:bg-cyan-300 hover:shadow-cyan-500/40 focus:outline-none focus:ring-2 focus:ring-cyan-400 focus:ring-offset-2 focus:ring-offset-[#0B0C10]"
          >
            {ctaText}
            <span className="ml-2 transition-transform duration-200 group-hover:translate-x-1" aria-hidden="true">
              →
            </span>
          </button>
        </div>
      </div>
    </section>
  );
}
```

---

### Receita de Código 2: Card de Preço/Destaque com `PulsingBorder` Dinâmico

Este exemplo ilustra como encapsular um cartão interativo com moldura viva de neon gerada pelo shader WebGL2 `PulsingBorder`, sem dependências pesadas de Three.js:

```tsx
'use client';

import React, { useState } from 'react';
import { PulsingBorder } from '@paper-design/shaders-react';

interface PricingTierCardProps {
  title: string;
  price: string;
  features: string[];
  isPopular?: boolean;
}

export function PricingTierCard({
  title,
  price,
  features,
  isPopular = false,
}: PricingTierCardProps) {
  const [isHovered, setIsHovered] = useState(false);

  return (
    <div 
      className="relative w-full max-w-sm rounded-3xl p-1 transition-transform duration-300 hover:-translate-y-1"
      onMouseEnter={() => setIsHovered(true)}
      onMouseLeave={() => setIsHovered(false)}
    >
      {/* Moldura de Shader WebGL2 Pulsante */}
      {isPopular && (
        <div className="absolute inset-0 z-0 pointer-events-none overflow-hidden rounded-3xl">
          <PulsingBorder
            colors={['#3B82F6', '#8B5CF6', '#EC4899', '#06B6D4']}
            roundness={0.88}
            thickness={isHovered ? 0.08 : 0.04}
            bloom={isHovered ? 0.9 : 0.5}
            pulse={0.3}
            smoke={0.15}
            smokeSize={0.4}
            spots={3}
            spotSize={0.3}
            speed={isHovered ? 0.9 : 0.4}
            style={{ width: '100%', height: '100%' }}
          />
        </div>
      )}

      {/* Conteúdo do Card em DOM Semântico */}
      <div className="relative z-10 flex h-full flex-col justify-between rounded-[22px] bg-slate-900/90 p-8 backdrop-blur-xl border border-white/10 shadow-2xl">
        <div>
          {isPopular && (
            <span className="inline-block rounded-full bg-indigo-500/20 px-3 py-1 text-xs font-semibold text-indigo-300 mb-4">
              Mais Recomendado
            </span>
          )}
          <h3 className="text-xl font-bold text-white">{title}</h3>
          <div className="mt-4 flex items-baseline gap-1">
            <span className="text-4xl font-extrabold text-white">{price}</span>
            <span className="text-sm font-medium text-slate-400">/mês</span>
          </div>

          <ul className="mt-6 space-y-3">
            {features.map((feat, idx) => (
              <li key={idx} className="flex items-center text-sm text-slate-300">
                <svg className="mr-3 h-4 w-4 flex-shrink-0 text-indigo-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M5 13l4 4L19 7" />
                </svg>
                {feat}
              </li>
            ))}
          </ul>
        </div>

        <button
          type="button"
          className="mt-8 w-full rounded-xl bg-white/10 py-3 text-sm font-semibold text-white transition-colors duration-200 hover:bg-white/20 focus:outline-none focus:ring-2 focus:ring-indigo-400"
        >
          Iniciar Período Gratuito
        </button>
      </div>
    </div>
  );
}
```

---

### Receita de Código 3: Integração Vanilla JavaScript / TypeScript Direta (`ShaderMount`)

Se você está construindo uma aplicação em Astro, Vanilla JS, Svelte ou Vue, pode utilizar o motor principal `@paper-design/shaders` diretamente sem qualquer camada React:

```ts
import { ShaderMount, meshGradientFragmentShader } from '@paper-design/shaders';

// 1. Obtenha a referência ao elemento contêiner do DOM
const container = document.getElementById('shader-hero') as HTMLDivElement;

// 2. Converta cores hexadecimais para vec4 normalizado [r, g, b, a] entre 0.0 e 1.0
function hexToVec4(hex: string, alpha = 1.0): [number, number, number, number] {
  const cleaned = hex.replace('#', '');
  const r = parseInt(cleaned.substring(0, 2), 16) / 255;
  const g = parseInt(cleaned.substring(2, 4), 16) / 255;
  const b = parseInt(cleaned.substring(4, 6), 16) / 255;
  return [r, g, b, alpha];
}

// 3. Monte o pipeline WebGL2 com zero dependências
const shader = new ShaderMount(
  container,
  meshGradientFragmentShader,
  {
    u_colors: [
      hexToVec4('#0F172A'),
      hexToVec4('#3B82F6'),
      hexToVec4('#8B5CF6'),
      hexToVec4('#06B6D4')
    ],
    u_colorsCount: 4,
    u_distortion: 0.7,
    u_swirl: 0.4,
    u_grainMixer: 0.2,
    u_grainOverlay: 0.15,
    u_fit: 2, // 2 = Cover
    u_scale: 1.0,
    u_rotation: 0,
    u_originX: 0.5,
    u_originY: 0.5,
    u_offsetX: 0,
    u_offsetY: 0,
    u_worldWidth: container.clientWidth,
    u_worldHeight: container.clientHeight
  },
  { antialias: true, alpha: true },
  0.5, // speed
  0,   // frame offset
  2.0, // minPixelRatio
  8294400 // maxPixelCount (teto de 4K)
);

// 4. Atualização dinâmica de uniforms (exemplo: reagindo a evento de mouse)
window.addEventListener('mousemove', (e) => {
  const normX = (e.clientX / window.innerWidth) * 2 - 1; // -1 a 1
  shader.setUniforms({
    u_offsetX: normX * 0.1,
    u_distortion: 0.5 + Math.abs(normX) * 0.4
  });
});

// 5. Descarte estrito de memória ao desmontar a visualização
window.addEventListener('beforeunload', () => {
  shader.dispose();
});
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao arquitetar o plano técnico de uma nova interface ou redesign que utilize **Paper Design Shaders**, a IA e o Líder Técnico devem incorporar as seguintes diretrizes normativas na seção de Creative Technology:

### 1. Declaração de Governança de Contextos WebGL (Canvas Budgeting)
- **Teto Estrito**: A página nunca deve instanciar mais do que **2 contextos WebGL concorrentes**.
- **Estratégia de Singleton**: Para múltiplos elementos de destaque (ex: seções que entram e saem no scroll), declare no Blueprint uma estratégia de **Viewport-Driven Unmounting** ou utilize um único canvas fixo no fundo da página (`position: fixed; inset: 0; z-index: -1`) cujos uniforms (`u_colors`, `u_distortion`) são reconfigurados suavemente conforme o gatilho de scroll ativa novas seções.

### 2. Mapeamento Semântico de Cores & Design Tokens
- Documente formalmente a correspondência entre os tokens de cor do Tailwind CSS / tema da marca e os arrays hexadecimais repassados para a prop `colors`:
  - `brand-primary` (`var(--color-primary)`) ➔ Cor 1 do Shader.
  - `brand-secondary` (`var(--color-accent)`) ➔ Cor 2 do Shader.
  - `surface-canvas` (`var(--color-background)`) ➔ Fundo do Shader (`colorBack`).
- É proibido utilizar paletas arbitrárias descoladas dos tokens de marca declarados em `globals.css` ou `tailwind.config`.

### 3. Matriz de Acessibilidade & Acomodação Sensorial
- Todo componente que renderiza um shader do Paper deve ter declarada a regra de congelamento vestibular:
  - `prefers-reduced-motion: reduce` ➔ `speed: 0` (obrigatório).
  - Em telas de leitor de tela, adicione `aria-hidden="true"` e `tabIndex={-1}` aos contêineres de canvas.
  - Exigência de máscara de contraste: nenhum texto deve ter relação de contraste inferior a **4.5:1 (WCAG AA)** ou **7:1 (WCAG AAA)** contra o canvas. Documente a obrigatoriedade do scrim (`backdrop-blur` ou camada `bg-black/50`).

### 4. Controle de Fill-Rate da GPU em Dispositivos Móveis
- No plano técnico, determine que em viewports mobile (`max-width: 768px`), as seguintes props devem ser ajustadas:
  - `minPixelRatio={1.0}` (em vez de `2.0`).
  - `maxPixelCount={2073600}` (equivalente a 1080p, poupando a bateria de aparelhos com alta densidade de tela).
  - `grainOverlay={0}` (o grão por pixel consome instruções matemáticas extras no fragment shader desnecessárias em telas pequenas).

### 5. Checklist de Verificação Pré-Deploy (Definition of Done)
- [ ] O pacote `@paper-design/shaders-react` ou `@paper-design/shaders` está pinado na versão mais recente compatível.
- [ ] Nenhuma instância de Three.js ou R3F foi importada acidentalmente para backgrounds 2D.
- [ ] O teste com `prefers-reduced-motion: reduce` ativado congela o movimento sem quebrar a estética.
- [ ] O teste de alternância de aba (`document.hidden`) confirma que o uso de GPU zera imediatamente no Activity Monitor / Gerenciador de Tarefas.
- [ ] Não há erro de `webglcontextlost` no console ao navegar em rota dinâmica com Next.js App Router.
- [ ] O tempo de First Contentful Paint (FCP) permanece abaixo de 1.2 segundos no Lighthouse.
