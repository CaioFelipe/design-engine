---
id: "shadergradient"
name: "ShaderGradient"
url: "https://shadergradient.co/"
category: "4-shaders-3d"
schema_type: "B-motion-shaders"
dna_estetico: ["Organic WebGL Surface", "Parametric Fluid Dynamics", "Ray-Lit Chromatic Iridescence", "Perlin Vertex Displacement", "Cinematic Grain Texturing"]
densidade_informacao: "Baixa a Independente (Camada de Fundo & Objeto Escultural)"
impacto_visual: "Cinematografico/Showstopper"
custo_computacional: "Alto (WebGL / Three.js / Custom GLSL Vertex-Fragment Shaders)"
stack_frameworks: ["React (@shadergradient/react)", "Three.js", "@react-three/fiber", "@react-spring/three", "Next.js (Dynamic SSR: false)", "Framer (ShaderGradient Component)", "Figma"]
compatibilidade:
  combinacoes_recomendadas: ["ShaderGradient + Tailwind CSS v4 (Overlays & Blend Modes)", "ShaderGradient + Motion.dev / Framer Motion (Transitions)", "ShaderGradient + Lenis Smooth Scroll (Camera Scrubbing)", "ShaderGradient + Lucide Icons / Clean UI Copy"]
  conflitos_esteticos: ["Textos densos sem backdrop-filter / scrim escurecedor sobreposto", "Múltiplas instâncias simultâneas de WebGL Canvas na mesma viewport", "Interfaces analíticas hiperdensas com tabelas financeiras de alto contraste", "Layouts com excesso de sombras skeumórficas concorrendo com a iluminação 3D"]
---

# ShaderGradient — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)

O **ShaderGradient** (`https://shadergradient.co/`), arquitetado e desenvolvido pelo designer e engenheiro criativo **Ruucm** (Donghoon Seo), representa uma das transformações estéticas mais marcantes da web contemporânea: a transição de gradientes CSS estáticos lineares/radiais para **superfícies tridimensionais paramétricas em movimento fluido contínuo**.

Durante anos, a indústria da web de alto nível enfrentou uma dicotomia limitante para implementar fundos orgânicos e coloridos:
1. **Gradientes CSS (`linear-gradient`, `radial-gradient`, `conic-gradient`)**: Computacionalmente levíssimos, porém geometricamente planos, rígidos e desprovidos de profundidade táctil ou iluminação especular.
2. **Vídeos em Loop (MP4/WebM)**: Capazes de exibir renderizações 3D luxuosas criadas em Cinema 4D ou Blender, mas extremamente pesados em termos de banda (10MB a 30MB), com resolução fixa propensa a pixelização em telas 4K/Retina, sem reatividade a eventos do usuário e com artefatos de compressão em blocos escuros.
3. **Canvas 2D / CSS Mesh Gradient**: Simulações de malha vetorial que sofrem com gargalos de repintura da CPU e falta de shading físico real.

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                       A TRANSIÇÃO DE PARADIGMA CROMÁTICO                    │
└─────────────────────────────────────────────────────────────────────────────┘
  [CSS Gradiente 2D Tradicional]           [ShaderGradient 3D Paramétrico]
  - Interpolação cartesiana estática       - Malha poligonal densa (Plane, Sphere, Water)
  - Zero percepção de relevo ou luz       - Deformação de vértices via Ruído Simplex 3D
  - Mudanças de cor previsíveis e duras    - Shading com reflexão física e iluminação de estúdio
  - CPU-bound em transformações contínuas  - 100% acelerado por hardware GPU (WebGL / GLSL)
```

### A Sensação Cinestésica (Feel): Liquidez Paramétrica e Luz de Estúdio

A sensação táctil do ShaderGradient decorre da combinação de três pilares de física gráfica:
1. **Deslocamento Orgânico de Vértices (Vertex Displacement)**: Em vez de apenas mesclar cores em uma imagem 2D, o motor eleva e afunda os vértices de uma malha 3D real no espaço tridimensional com base em funções trigonométricas e algoritmos de ruído fractal de Perlin/Simplex. A malha comporta-se como um tecido de seda esticado ou a superfície de um lago sob brisa suave.
2. **Iluminação Dinâmica e Mapas de Reflexão (PBR & Studio Lighting)**: As cristas e vales da geometria reagem a fontes de luz direcionais (`lightType="3d"`) ou a mapas esféricos de ambiente HDRI (`lightType="env"` com presets como `'studio'`, `'city'`, `'sunset'`). Isso gera reflexos especulares acetinados, sensação metálica líquida ou translucidez gelatinosa.
3. **Difusão Analógica com Granulação Cinemática (Procedural Film Grain)**: O fragment shader injeta uma micro-camada de ruído procedural de grão de filme 35mm (`grain="on"`), rompendo o aspecto plástico ou excessivamente computadorizado do WebGL puro e conferindo uma textura visual de alta costura e papel editorial impresso.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Interface e Casos de Uso Críticos

1. **Hero Sections de Produtos Digitais Visionários (AI, SaaS, FinTech, DevTools)**:
   A tela inicial de produtos tecnológicos contemporâneos (como plataformas de inteligência artificial, interfaces de agentes ou ferramentas de design) exige uma declaração visual de futuro e inovação. O ShaderGradient cria um pano de fundo vivo que respira discretamente sem distrair da proposta de valor.
2. **Floating Orbs & Avatares de Inteligência Artificial (`type="sphere"`)**:
   A geometria esférica deformada por ruído atua perfeitamente como a representação visual de um assistente de IA em estado de escuta, processamento de raciocínio ou síntese de resposta, comunicando estado e energia computacional através de variações em `uSpeed`, `uFrequency` e `uAmplitude`.
3. **Storytelling Imersivo e Portfólios de Luxo / Agências Criativas**:
   Em sites premiados (Awwwards / FWA / Webby), fundos com topografia líquida (`type="waterPlane"`) ancoram tipografia editorial de alta escala (Grotesk condensada ou Serif de contraste alto), transmitindo exclusividade estética inalcançável por templates genéricos.
4. **Páginas de Lançamento de Hardware, FinTech ou Web3**:
   A alusão a metais líquidos, piscinas de liquidez ("liquidity pools") ou refrações prismáticas de silício e vidro fortalece temas de sofisticação financeira ou precisão de engenharia.

### A Regra 60-30-10 no Design Visual

O ShaderGradient desempenha papéis vitais e distintos dependendo da sua escala e intensidade na paleta global da interface:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                 O PAPEL DO SHADERGRADIENT NA REGRA 60-30-10                 │
└─────────────────────────────────────────────────────────────────────────────┘

  MODALIDADE A: COMO OS 60% (AMBIENTAÇÃO CROMÁTICA DE FUNDO)
  ├─ 60% Cor Dominante: Gradiente tridimensional esmaecido em baixa opacidade 
  │   (30-50%), com velocidade sutil (uSpeed: 0.1 a 0.2) e overlay dark/light
  ├─ 30% Cor Secundária: Cards em glassmorphism fosco (bg-black/60 backdrop-blur-xl),
  │   estruturas de layout neutras, botões secundários em slate/zinc
  └─ 10% Cor de Destaque: Botão primário CTA (botão branco puro ou accent neon)

  MODALIDADE B: COMO OS 10% (PONTO FOCAL SHOWSTOPPER)
  ├─ 60% Cor Dominante: Fundo minimalista neutro (Dark #09090b ou Light #fafafa)
  ├─ 30% Cor Secundária: Tipografia estruturada, grids técnicos, linhas de contorno finas
  └─ 10% Cor de Destaque: Esfera 3D ShaderGradient orgânica (type="sphere") viva no
      centro do viewport, servindo como o objeto de atração visual instantânea
```

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Quando Evitar (Anti-padrões)

1. **UIs Densas de Dados, Dashboards Críticos e Tabelas Operacionais**:
   - *Motivo*: Interfaces corporativas que exigem análise intensiva (planilhas financeiras, consoles AWS, terminais de telemetria) demandam contraste visual estático e foco absoluto em números. Fundos em movimento degradam a acuidade visual e geram fadiga cognitiva severa.
2. **Superposição de Texto Longo sem Camada Scrim/Backdrop**:
   - *Anti-padrão*: Renderizar blocos de texto corrido (artigos de blog, documentação técnica, formulários de cadastro) diretamente sobre a malha 3D em movimento. A variação constante dos picos de cor destrói o contraste cromático exigido pelas diretrizes WCAG 2.1 (mínimo de 4.5:1 para texto normal).
3. **Múltiplos Canvases WebGL Concorrentes na Mesma Viewport**:
   - *Anti-padrão*: Instanciar três ou quatro `<ShaderGradientCanvas />` em cards individuais de uma grade. Cada canvas aloca um contexto WebGL distinto, consome texturas de buffer dedicadas na GPU e pode ultrapassar o limite máximo de contextos WebGL do navegador móvel (frequentemente limitado a 8 ou 16 contextos antes de travar o motor gráfico).
4. **Dispositivos Móveis de Baixo Desempenho em Modo de Economia de Bateria**:
   - O loop de renderização a 60fps/120fps em fragment shaders complexos com cálculo de ruído procedural pode acelerar o dreno de bateria e gerar superaquecimento térmico (*thermal throttling*).

### ⚠️ Regras Mandatórias de Acessibilidade & Gestão de GPU

1. **Respeito Irrestrito a `prefers-reduced-motion`**:
   - Usuários com distúrbios vestibulares ou sensibilidade a cinetose sofrem enjoos ao visualizar superfícies tridimensionais ondulantes.
   - *Ação Técnica*: Inspecionar `prefers-reduced-motion: reduce`. Quando ativado, fixar `animate="off"` ou congelar a velocidade do tempo em `uSpeed={0}`, mantendo o gradiente como uma escultura 3D estática de extrema beleza.
2. **Capagem Inteligente do Pixel Ratio (`pixelDensity`)**:
   - Dispositivos modernos de alta densidade (iPhones com Retina Display 3x ou monitores 4K) tentam renderizar o canvas em 300% de resolução, multiplicando por 9 o número de pixels sombreados por frame.
   - *Ação Técnica*: Sempre restringir o renderizador a `pixelDensity={Math.min(window.devicePixelRatio, 1.5)}`. Acima de 1.5x, o ganho de nitidez visual em shaders orgânicos é imperceptível para o olho humano, mas o custo em milissegundos de GPU cai pela metade.
3. **Interrupção de Renderização Fora do Viewport (Intersection Observer)**:
   - Quando o usuário rola a página e a seção do ShaderGradient sai do campo de visão, a animação WebGL **deve ser pausada** ou o componente desmontado, liberando 100% dos ciclos de clock da GPU para o restante da aplicação.
4. **Fallback SSR e Prevenção de CLS (Cumulative Layout Shift)**:
   - Como o WebGL requer acesso a objetos do navegador (`window`, `HTMLCanvasElement`, `WebGLRenderingContext`), o componente não pode ser renderizado no servidor (Node.js SSR).
   - *Ação Técnica*: Empregar `dynamic(() => import(...), { ssr: false })` em conjunto com um container com dimensões fixas e um gradiente CSS estático como placeholder suave, impedindo o salto de layout (CLS = 0).

---

## 4. Catálogo de Efeitos, Primitivas e Padrões de Animação

O ecossistema ShaderGradient disponibiliza 8 padrões fundamentais de geometria, cinemática e iluminação:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                 CATÁLOGO DE PRIMITIVAS E COMPORTAMENTOS 3D                  │
└─────────────────────────────────────────────────────────────────────────────┘
  [1. Plane]              [2. Sphere]             [3. WaterPlane]
  ┌──────────────┐        ┌──────────────┐        ┌──────────────┐
  │ ~ ~ ~ ~ ~ ~  │        │    ╭────╮    │        │  ≈ ≈ ≈ ≈ ≈   │
  │~ ~ ~ ~ ~ ~ ~ │        │   │ 3D   │   │        │ ≈ ≈ ≈ ≈ ≈ ≈  │
  │ ~ ~ ~ ~ ~ ~  │        │    ╰────╯    │        │  ≈ ≈ ≈ ≈ ≈   │
  └──────────────┘        └──────────────┘        └──────────────┘
  Hero Backdrop           Floating AI Orb         Liquid Fluid
```

### 1. Ethereal Backdrop Ribbon (`type="plane"`)
- **Comportamento Visual**: Uma malha retangular plana altamente subdividida, posicionada perpendicular ou diagonalmente à câmera, com vértices oscilando em ondas senoidais amplas e suaves. Lembra um lençol de seda levitando em gravidade zero.
- **Gatilho**: Loop temporal contínuo (`animate="on"`, `uSpeed: 0.2 - 0.4`), com pequenas reações a micro-deslocamentos do cursor do mouse.
- **Onde Encaixar**: Hero sections em tela cheia (100vw x 100vh) com texto principal e CTAs flutuando no primeiro plano.

### 2. Cosmic Morphing Sphere (`type="sphere"`)
- **Comportamento Visual**: Uma esfera 3D fechada cujos raios radiais são modulados tridimensionalmente por ruído Simplex. As cores orbitam a superfície da esfera enquanto sua carcaça expande e contrai de maneira orgânica e biológica, como uma gota de plasma estelar.
- **Gatilho**: Estado contínuo autônomo, variando sua velocidade (`uSpeed`) e frequência (`uFrequency`) ao alternar estados de aplicação (ex: idle vs. listening vs. thinking).
- **Onde Encaixar**: Elemento de identidade de produtos de Inteligência Artificial, cabeçalhos de perfil de usuário ou mascote conceitual de branding interativo.

### 3. WaterPlane Liquid Topography (`type="waterPlane"`)
- **Comportamento Visual**: Configuração especializada de malha plana horizontal que emula a dinâmica de superfície da água em repouso sob ondas capilares direcionais. As cores fluem em faixas transversais suaves que se dissolvem umas nas outras sem descontinuidades abruptas.
- **Gatilho**: Loop contínuo com `cPolarAngle` baixo (~60° a 80°), criando um horizonte que se estende em direção ao infinito no eixo Z.
- **Onde Encaixar**: Seções de "Liquidity Pools" em FinTech, interfaces de meditação / mindfulness, rodapés monumentais imersivos.

### 4. Grain-Infused Analog Film (`grain="on"`)
- **Comportamento Visual**: Uma camada pós-processada no fragment shader que injeta micro-grãos estáticos/dinâmicos em escala sub-pixel. Rompe o banding típico de gradientes digitais (os degraus de quantização de 8-bits por canal RGB) e confere um visual tátil analógico.
- **Gatilho**: Ativação booleana estática no pipeline de fragmentação.
- **Onde Encaixar**: Marcas de design editorial, estúdios de arquitetura, galerias de arte contemporânea e interfaces de moda/lifestyle.

### 5. Studio Environment Specular Sheen (`lightType="env"`, `envPreset="studio"`)
- **Comportamento Visual**: A superfície da malha 3D reflete uma imagem de alta faixa dinâmica (HDRI) de caixas de luz de estúdio fotográfico, gerando faixas de reflexão branca pura e realces metálicos acetinados nas cristas das ondas.
- **Gatilho**: Iluminação global e orientação do vetor normal da geometria em relação à câmera virtual.
- **Onde Encaixar**: Sites de produtos de hardware, relógios, dispositivos tecnológicos de precisão e interfaces de áudio profissional.

### 6. High-Frequency Kinetic Turbulence (`uFrequency: 6.0 - 10.0`, `uSpeed: 0.6+`)
- **Comportamento Visual**: As ondas da malha tornam-se densas, espiraladas e rápidas. As três cores da paleta misturam-se com bordas mais estreitas, transmitindo sensação de vórtice de alta energia, velocidade de processamento ou atividade intensa.
- **Gatilho**: Disparado temporariamente durante eventos de carregamento crítico, processamento de transações ou transições de rota.
- **Onde Encaixar**: Indicadores visuais de processamento ("Processing AI weights..."), telas de splash ou seções de benchmarks de performance.

### 7. Camera Polar Orbit Scrubbing (`cPolarAngle` & `cDistance` via Scroll)
- **Comportamento Visual**: A câmera que observa o ShaderGradient desloca sua altitude (ângulo polar) e proximidade (distância focal) conforme o usuário rola a página, permitindo ver a malha "de cima" em um momento e "rente ao chão" em outro.
- **Gatilho**: Evento de rolagem normalizado via Lenis ou GSAP ScrollTrigger mapeado para as propriedades da câmera.
- **Onde Encaixar**: Narrativas do tipo Scrollytelling onde a paisagem cromática se transforma dramaticamente à medida que os capítulos avançam.

### 8. Wireframe Holographic Topology (`wireframe={true}`)
- **Comportamento Visual**: O material opaco é substituído pela renderização pura das arestas dos polígonos da malha tridimensional, revelando a complexidade da grade de vértices que dança no espaço.
- **Gatilho**: Modo estético selecionável pelo usuário (ex: botão de alternância "Inspect Shader Mesh" ou tema Cypherpunk/Técnico).
- **Onde Encaixar**: Portfólios de desenvolvedores WebGL, ferramentas de infraestrutura de nuvem, plataformas de cibersegurança ou consoles de depuração.

---

## 5. Matemática do Movimento & Receitas de Código

### A Matemática dos Shaders no ShaderGradient

O núcleo de deformação do ShaderGradient fundamenta-se na manipulação de coordenadas no **Vertex Shader** antes da rasterização dos fragmentos:

$$\vec{P}_{final} = \vec{P}_{base} + \vec{N} \cdot \left[ \text{noise3D}\left(\vec{P}_{base} \cdot uDensity \cdot uFrequency + uTime \cdot uSpeed\right) \cdot uAmplitude \cdot uStrength \right]$$

Onde:
- $\vec{P}_{base}$: Posição original do vértice na geometria não deformada.
- $\vec{N}$: Vetor normal unitário da superfície no vértice.
- $uTime$: Uniforme de tempo acumulado no frame loop (em segundos).
- $uSpeed$: Fator de dilatação temporal da animação.
- $uDensity$: Compactação da distribuição espacial dos nós de ruído.
- $uFrequency$: Multiplicador de periodicidade espacial (espiralização das cristas).
- $uAmplitude$: Elevação máxima de deslocamento ao longo da normal.
- $uStrength$: Força de acoplamento entre a distorção física e a rotação cromática.

No **Fragment Shader**, as cores $\vec{C}_1, \vec{C}_2, \vec{C}_3$ são interpoladas trilateralmente usando uma função de mapeamento de ruído com ruído de granulação injetado:

$$\vec{C}_{final} = \text{mix}\left(\text{mix}(\vec{C}_1, \vec{C}_2, f_{noise}(uv)), \vec{C}_3, g_{noise}(uv)\right) + \text{grain}_{val}$$

---

### Parâmetros Físicos e Limites Recomendados

| Parâmetro | Tipo | Faixa Segura | Valor Padrão | Impacto Sensorial |
| :--- | :--- | :--- | :--- | :--- |
| `type` | string | `'plane'` \| `'sphere'` \| `'waterPlane'` | `'plane'` | Define a topologia estrutural da malha tridimensional. |
| `uSpeed` | number | `0.05` a `0.8` | `0.3` | Velocidade da correnteza. Valores > 0.8 tornam-se agitados e estressantes. |
| `uStrength` | number | `1.0` a `5.0` | `2.4` | Profundidade da mistura das cores e vigor do deslocamento. |
| `uDensity` | number | `0.5` a `3.5` | `1.3` | Densidade das dobras. Valores altos criam rugas microscópicas. |
| `uFrequency` | number | `1.0` a `8.0` | `4.0` | Ritmo espiral das dobras. |
| `uAmplitude` | number | `0.5` a `5.0` | `2.0` | Altura física das ondas (relevo no eixo da normal). |
| `cDistance` | number | `2.0` a `45.0` | `3.6` (water) / `28` (plane) | Distância focal da câmera em relação ao centro da cena. |
| `cPolarAngle` | number | `30` a `150` | `80` a `125` | Inclinação vertical da câmera (em graus ou radianos). |
| `lightType` | string | `'3d'` \| `'env'` | `'3d'` | Modelo de iluminação (Phong direcionado vs. Reflexão HDRI). |
| `envPreset` | string | `'city'` \| `'dawn'` \| `'lobby'` \| `'studio'` | `'city'` | Mapa HDRI em caso de `lightType="env"`. |
| `reflection` | number | `0.0` a `1.0` | `0.2` | Brilho especular e resposta metálica à luz. |
| `grain` | string | `'on'` \| `'off'` | `'on'` | Grão de filme analógico para eliminação de color banding. |
| `pixelDensity` | number | `1.0` a `2.0` | `1.5` | Ratio de renderização do canvas (preserva GPU móvel). |

---

### Receita de Código Funcional: Hero Section Moderna em Next.js (App Router)

A implementação a seguir resolve de forma elegante e robusta todos os desafios de SSR, detecção de `prefers-reduced-motion`, cap de pixel ratio e contraste tipográfico:

```tsx
// components/HeroShaderBackground.tsx
'use client'

import React, { useState, useEffect } from 'react'
import dynamic from 'next/dynamic'

// 1. Dynamic Import com ssr: false para evitar incompatibilidade do WebGL com Node SSR
const ShaderGradientCanvas = dynamic(
  () => import('@shadergradient/react').then((mod) => mod.ShaderGradientCanvas),
  { ssr: false }
)
const ShaderGradient = dynamic(
  () => import('@shadergradient/react').then((mod) => mod.ShaderGradient),
  { ssr: false }
)

export function HeroShaderBackground() {
  const [mounted, setMounted] = useState(false)
  const [reducedMotion, setReducedMotion] = useState(false)

  useEffect(() => {
    setMounted(true)
    const mediaQuery = window.matchMedia('(prefers-reduced-motion: reduce)')
    setReducedMotion(mediaQuery.matches)

    const handler = (e: MediaQueryListEvent) => setReducedMotion(e.matches)
    mediaQuery.addEventListener('change', handler)
    return () => mediaQuery.removeEventListener('change', handler)
  }, [])

  return (
    <div className="relative min-h-screen w-full overflow-hidden bg-zinc-950 text-zinc-100 flex flex-col justify-between">
      {/* Camada 1: WebGL ShaderGradient Canvas */}
      <div className="absolute inset-0 z-0 pointer-events-none">
        {mounted ? (
          <ShaderGradientCanvas
            style={{
              position: 'absolute',
              top: 0,
              left: 0,
              width: '100%',
              height: '100%',
            }}
            pixelDensity={typeof window !== 'undefined' ? Math.min(window.devicePixelRatio, 1.5) : 1}
            fov={45}
          >
            <ShaderGradient
              type="waterPlane"
              animate={reducedMotion ? 'off' : 'on'}
              uSpeed={reducedMotion ? 0 : 0.25}
              uStrength={2.8}
              uDensity={1.2}
              uFrequency={4.5}
              uAmplitude={2.2}
              color1="#3b82f6"
              color2="#8b5cf6"
              color3="#06b6d4"
              lightType="3d"
              cPolarAngle={95}
              cDistance={4.2}
              grain="on"
              reflection={0.15}
            />
          </ShaderGradientCanvas>
        ) : (
          /* Placeholder CSS Mesh Gradient durante SSR / Hydration inicial */
          <div 
            className="absolute inset-0 bg-gradient-to-tr from-blue-900 via-indigo-950 to-zinc-950 opacity-80" 
            aria-hidden="true"
          />
        )}
      </div>

      {/* Camada 2: Scrim de Contraste, Vignette e Ruído Textural */}
      <div 
        className="absolute inset-0 z-1 pointer-events-none bg-radial from-transparent via-zinc-950/40 to-zinc-950/90"
        aria-hidden="true"
      />

      {/* Camada 3: Header de Navegação com Glassmorphism Fosco */}
      <header className="relative z-10 flex items-center justify-between px-8 py-6 max-w-7xl mx-auto w-full">
        <div className="flex items-center gap-3">
          <div className="h-8 w-8 rounded-lg bg-white/10 backdrop-blur-md border border-white/20 flex items-center justify-center font-bold tracking-tight text-white shadow-sm">
            ∇
          </div>
          <span className="font-semibold text-lg tracking-tight text-white/90">
            Kinetics Studio
          </span>
        </div>

        <nav className="hidden md:flex items-center gap-8 text-sm font-medium text-zinc-300">
          <a href="#features" className="hover:text-white transition-colors">Tecnologia</a>
          <a href="#showcase" className="hover:text-white transition-colors">Aplicações</a>
          <a href="#pricing" className="hover:text-white transition-colors">Planos</a>
        </nav>

        <button className="px-4 py-2 text-sm font-medium rounded-full bg-white/10 hover:bg-white/20 backdrop-blur-md border border-white/20 transition-all text-white">
          Acessar Console
        </button>
      </header>

      {/* Camada 4: Conteúdo Tipográfico Hero com Legibilidade Garantida */}
      <main className="relative z-10 max-w-5xl mx-auto px-6 py-20 text-center flex flex-col items-center">
        <div className="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-white/10 backdrop-blur-md border border-white/15 text-xs font-medium text-cyan-300 mb-8 shadow-sm">
          <span className="h-1.5 w-1.5 rounded-full bg-cyan-400 animate-pulse" />
          WebGL 3D Surface Engine v2.4
        </div>

        <h1 className="text-5xl sm:text-7xl font-extrabold tracking-tight text-white leading-[1.08] max-w-4xl drop-shadow-sm">
          Superfícies vivas para interfaces extraordinárias.
        </h1>

        <p className="mt-6 text-lg sm:text-xl text-zinc-200/90 max-w-2xl font-normal leading-relaxed drop-shadow-sm">
          Aceleração gráfica de alta fidelidade que transforma gradientes estáticos 
          em tecidos paramétricos interativos e responsivos à física.
        </p>

        <div className="mt-10 flex flex-wrap items-center justify-center gap-4">
          <button className="px-7 py-3.5 rounded-full bg-white text-zinc-950 font-semibold text-sm hover:bg-zinc-100 hover:scale-[1.02] active:scale-[0.98] transition-all shadow-lg shadow-white/10">
            Começar Gratuitamente
          </button>
          <button className="px-7 py-3.5 rounded-full bg-zinc-900/80 hover:bg-zinc-800 text-white font-medium text-sm border border-white/15 backdrop-blur-md transition-all">
            Ver Demonstração Interativa
          </button>
        </div>
      </main>

      {/* Camada 5: Barra de Métricas Inferiores */}
      <footer className="relative z-10 border-t border-white/10 bg-zinc-950/60 backdrop-blur-lg px-8 py-4">
        <div className="max-w-7xl mx-auto flex flex-col sm:flex-row items-center justify-between gap-4 text-xs text-zinc-400">
          <div>Renderizado em GPU a 60 FPS com precisão sub-pixel.</div>
          <div className="flex items-center gap-6">
            <span>DPR Travado em 1.5x</span>
            <span>Acessibilidade WCAG 2.1 AA</span>
            <span>Zero CLS Garantido</span>
          </div>
        </div>
      </footer>
    </div>
  )
}
```

---

### Receita Alternativa: Integração por Query URL do Customizer

O ShaderGradient oferece uma funcionalidade produtiva: o designer ajusta todos os parâmetros na interface gráfica visual (`https://shadergradient.co/customize`), copia a URL resultante e o desenvolvedor a consome diretamente usando o modo `control="query"`:

```tsx
import { ShaderGradientCanvas, ShaderGradient } from '@shadergradient/react'

export function FastPresetHero() {
  return (
    <ShaderGradientCanvas 
      style={{ position: 'absolute', inset: 0 }}
      pixelDensity={1.5}
    >
      <ShaderGradient 
        control="query" 
        urlString="https://www.shadergradient.co/customize?animate=on&cDistance=3.6&cPolarAngle=90&color1=%2352ff89&color2=%23dbba95&color3=%23d0bce1&lightType=3d&shader=defaults&type=waterPlane&uFrequency=5.5&uSpeed=0.3&uStrength=3.5&grain=on" 
      />
    </ShaderGradientCanvas>
  )
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao planejar a inclusão de um componente ou plano de fundo baseado no **ShaderGradient** no plano de arquitetura de interface (`DESIGN_BLUEPRINT.md`), a IA e a equipe de engenharia devem seguir este checklist mandatório:

### 1. Declaração Formal da Geometria e Papel Estrutural
- Especificar no blueprint a topologia exata:
  - `type: "waterPlane"` para fundos expansivos de sensação calma e horizontal.
  - `type: "plane"` para fundos com drapeado diagonal agressivo.
  - `type: "sphere"` para orbs flutuantes e pontos focais de IA.
- Declarar se o componente atua nos **60%** (fundo escurecido por scrim) ou nos **10%** (escultura 3D centralizada).

### 2. Especificação da Tríade Cromática e Contraste
- Definir as três cores hexadecimais obrigatórias (`color1`, `color2`, `color3`).
- **Verificação WCAG**: Toda camada de tipografia que sobrevoe o gradiente deve possuir um scrim de fundo declarado (ex: `bg-radial from-transparent to-black/80` ou cards com `backdrop-blur-xl bg-zinc-950/70`) para garantir relação de contraste mínima de 4.5:1 em todos os ciclos temporais do shader.

### 3. Matriz de Performance e Responsividade Móvel
- **Cap de Densidade de Pixels**: Registrar expressamente `pixelDensity={Math.min(window.devicePixelRatio, 1.5)}`.
- **Dimensões e Fallback**: Conter o canvas dentro de um container com `position: relative` e dimensões explicitadas (ex: `h-[600px] w-full` ou `min-h-screen`), com um gradiente CSS correspondente renderizado no SSR para anular o CLS (Cumulative Layout Shift).
- **Desligamento Fora do Viewport**: Incluir a instrução de suspender o loop de animação via Intersection Observer quando o componente estiver fora da área visível.

### 4. Política de Acessibilidade (Reduced Motion)
- Documentar no blueprint que o componente escutará a media query `(prefers-reduced-motion: reduce)`. Quando verdadeira, definir `animate="off"` e `uSpeed={0}`, assegurando conformidade estrita com o Critério de Sucesso 2.3.3 da WCAG (Animação a partir de Interações).

### 5. Configuração no Next.js App Router
- Marcar o componente com `'use client'`.
- Carregar via `next/dynamic` com `{ ssr: false }` para blindar o build de produção contra erros de execução no ambiente Node.js.
