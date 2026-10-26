---
id: "088-vfx-js"
name: "VFX-JS (@vfx-js/core)"
url: "https://www.vfx-js.com/"
category: "4-shaders-3d"
schema_type: "B-motion-shaders"
dna_estetico: ["DOM-Integrated WebGL Post-Processing", "Single-Canvas Multi-Element Orchestration", "Retro-Digital Glitch & Chromatic Aberration", "Intersection-Driven Shader Transitions", "Hardware-Accelerated HTML Typography"]
densidade_informacao: "Independente"
impacto_visual: "Cinematografico/Showstopper"
custo_computacional: "Medio a Alto (WebGL2 GLSL Shaders sobre DOM Textures com GPU Scissor Culling)"
stack_frameworks: ["Vanilla JS / TypeScript (@vfx-js/core)", "React (@vfx-js/react)", "Vue", "WebGL2 / GLSL 300 es", "CSS3"]
compatibilidade:
  combinacoes_recomendadas: ["VFX-JS + Lenis Smooth Scroll", "VFX-JS + GSAP ScrollTrigger", "VFX-JS + Tailwind CSS", "VFX-JS + Motion.dev / Framer Motion"]
  conflitos_esteticos: ["Múltiplos contextos WebGL simultâneos concorrentes sem coordenação (disputa de limites de contexto e GPU memory)", "Aplicação indiscriminada de glitch e distorção em blocos longos de tipografia editorial de leitura", "Falta de bounding box overflow em elementos contidos por ancestrais com overflow:hidden rígido"]
---

# VFX-JS (@vfx-js/core) — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)

O **VFX-JS** (`https://www.vfx-js.com/` / `https://amagi.dev/vfx-js/`), concebido e mantido pelo engenheiro criativo e shader artist **Amagi Takayosi** (`@fand`), introduz um dos paradigmas mais elegantes e disruptivos no ecossistema de Creative Development moderno: **a fusão direta entre a árvore de elementos do DOM nativo e o pipeline de rasterização por shaders WebGL2**.

Antes do VFX-JS, a aplicação de pós-processamento gráfico de estúdio (como aberrações cromáticas, distorções por ruído simplex, emissão de bloom, retículas de meio-tom e efeitos CRT) exigia que todo o conteúdo visual fosse recriado do zero dentro de uma cena monolítica 3D (Three.js, PixiJS ou Babylon.js). Esse modelo tradicional impunha um fosso intransponível:
- Textos deixavam de ser nós de texto acessíveis pelo navegador;
- Tags semânticas `<img>` e `<video>` perdiam propriedades nativas de streaming, autoplay responsivo, caching e decodificação acelerada por hardware de vídeo do browser;
- Quebrava-se a responsividade do CSS Flexbox e Grid;
- O layout tornava-se opaco a leitores de tela e robôs de indexação SEO.

```
┌────────────────────────────────────────────────────────────────────────┐
│             PARADIGMA MONOLÍTICO TRADICIONAL (THREE.JS / PIXI)         │
└────────────────────────────────────────────────────────────────────────┘
  [HTML / DOM] (Geralmente abandonado para elementos visuais principais)
       │
  [Canvas WebGL Único] <--- Re-implementa Texto, Layout, Carregamento e Câmera
       ├── ❌ Perda de acessibilidade nativa (WCAG) e seleção de texto
       ├── ❌ Redesenho manual do sistema de layout responsivo do CSS
       └── ❌ Custo altíssimo de engenharia para sincronizar coordenadas 3D com o DOM

┌────────────────────────────────────────────────────────────────────────┐
│                   PARADIGMA VFX-JS (DOM-ANCHORED WEBGL)                │
└────────────────────────────────────────────────────────────────────────┘
  [Árvore DOM Nativa: <img>, <video>, <canvas>, <div>, <h1>, <span>]
       │  (Layout, CSS, Tipografia e Acessibilidade 100% nativos)
       ▼
  [VFX Engine: Single Global WebGL2 Canvas Overlay]
       ├── ✅ Bounding Rect Sync: getBoundingClientRect() + IntersectionObserver
       ├── ✅ GPU Scissor Test: renderiza apenas a área visível do nó com 'overflow'
       ├── ✅ Dynamic Texture Ingestion: converte nós HTML em texturas WebGL vivas
       └── ✅ Fragment Pipeline: executa GLSL 300 es de alta performance frame a frame
```

### A Sensação Cinestésica (Feel): Do Digital Frio ao Artefato Físico-Eletrostático

A assinatura cinestésica gerada pelo VFX-JS evoca a materialidade de interfaces eletro-ópticas, monitores de raios catódicos (CRT), lentes prismáticas analógicas e circuitos com defeito controlado (*glitch art*). 

A sensação física transmitida à interface não é de simples "animação de posição" ou "fade suave", mas de **vibração molecular dos pixels**, como se a camada superficial do navegador fosse sensível a campos magnéticos, pulsos de rádio e calor da GPU:
1. **Distorção e Rasgo Eletrostático**: Em transições e estados de hover, os elementos não apenas deslizam; eles quebram em fatias temporais horizontais (*slit scan*), sofrem dispersão refrativa nos canais RGB e recombinam-se de forma magnética.
2. **Reatividade Orgânica ao Ponto de Foco**: Através de uniforms customizados sincronizados com o ponteiro (`pointermove`) ou com a física de rolagem (`scroll velocity`), os elementos comportam-se como líquidos viscosos ou fitas magnéticas submetidas a atrito.
3. **Harmonia Invisível com o Fluxo Web**: Como o elemento real continua sob a projeção do shader, o usuário preserva o tato mecânico dos cliques, a seleção de texto e os formulários reativos.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Interface Insubstituíveis

1. **Portfólios Criativos, Estúdios Digitais & Agências Audiovisuais**:
   Projetos que exigem uma presença visual eletrizante ("showstopper"), onde imagens de capas de cases, logotipos monocromáticos e vídeos em loop necessitam de acabamento de vanguarda com pós-processamento dinâmico sem reescrever a arquitetura Next.js/React.
2. **Apresentação de Produtos de Moda, Luxo Tech e Música/Entretenimento**:
   Lançamentos de calçados, moda conceitual, trailers e festivais musicais onde o apelo estético se ancora no visual *cyberpunk*, *Y2K aesthetic*, distorções de fita VHS, retículas de jornal analógico (*halftone*) e quebras prismáticas de luz.
3. **Transições Narrativas de Scrollytelling e Viewport Reveal**:
   Elementos de mídia (`<img>` e `<video>`) que entram na tela ativando shaders automáticos de transição (`slitScanTransition`, `warpTransition`, `focusTransition`, `pixelateTransition`). O efeito é ativado pelo `IntersectionObserver` interno do VFX-JS, capturando a atenção no exato milissegundo de entrada.
4. **Hero Sections com Tipografia Viva e Reativa**:
   Títulos em `<h1>` e `<span>` que reagem ao mouse com aberração cromática contínua, dispersão de ruído ou pulsação de brilho (*shine*), transformando texto HTML comum em um artefato cinemático vivo.
5. **Painéis Interativos com `<canvas>` 2D e Gráficos de Dados**:
   Dashboards temáticos onde gráficos nativos do Canvas 2D recebem um passe de pós-processamento WebGL do VFX-JS (como scanlines de terminal, fósforo verde e aberração esférica) através de chamadas instantâneas a `vfx.update(canvas)`.

### Enquadramento na Regra 60-30-10

- **Os 60% (Fundação Estrutural Neutra)**: Layout padrão estruturado com Tailwind CSS, grid responsivo, tipografia com alto contraste e legibilidade impecável, sem distorções gráficas contínuas.
- **Os 30% (Identidade de Marca e Fluidez Interativa)**: Cores sólidas de marca, micro-interações mecânicas do sistema e rolagem suave via motor cinético (ex: Lenis Scroll).
- **Os 10% (O Espetáculo Visual com VFX-JS)**: Ponto focal cirúrgico. Aplicação concentrada em:
  - 1 a 2 elementos da Hero Section (o logotipo ou o vídeo hero com `duotone` / `rgbShift`);
  - Hover states nos cards de projetos do portfólio;
  - Transições discretas de entrada de imagens na rolagem.
  *Evita-se cobrir a página inteira com ruído contínuo, preservando a nobreza e o frescor do efeito visual.*

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Quando Evitar Absolutamente

1. **Aplicações de Alta Densidade Utilitária e Produtividade (SaaS B2B, CRMs, FinTechs)**:
   - Interfaces com tabelas densas, gráficos de negociação financeira em tempo real ou formulários de emissão fiscal. Shaders de glitch ou distorções de coordenadas causam fadiga cognitiva severa, aumentam a taxa de erro de leitura de caracteres numéricos e geram desconforto visual.
2. **Longos Blocos de Texto Editorial / Artigos de Blog**:
   - Nunca aplique shaders com deslocamento de canal RGB ou ondulação contínua em parágrafos de texto longo (`<p>`). O efeito borra os contornos dos glifos e causa desconforto visual e dor de cabeça ao leitor.
3. **Dispositivos Móveis de Entrada com Bateria Crítica**:
   - Renderizar fragment shaders complexos a 60-120fps em telas de alta densidade (ex: iPhone Retina 3x) força a GPU móvel a recalcular fragmentos para cada pixel de resolução nativa, acelerando o esgotamento da bateria e ativando *thermal throttling*.

### ⚠️ Regras de Acessibilidade (WCAG), GPU & Fallbacks

1. **Respeito Estrito a `prefers-reduced-motion`**:
   - É obrigatório desativar shaders de distorção oscilatória, glitch frenético e transições espaciais agressivas quando a media query `@media (prefers-reduced-motion: reduce)` estiver ativa:
   ```typescript
   const prefersReducedMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
   if (!prefersReducedMotion) {
     vfx.add(heroElement, { shader: 'rgbShift' });
   }
   ```
2. **Culling Inteligente por Oclusão e Visibilidade de Aba**:
   - O VFX-JS desliga nativamente o loop de renderização para elementos que saem do viewport via `IntersectionObserver`. Garanta que a aba inativa suspenda totalmente o `requestAnimationFrame` para evitar o desperdício de ciclos da GPU.
3. **Degradação Elegante sem WebGL2**:
   - Como o elemento subjacente é um nó DOM comum (`<img>`, `<video>`, `<h1>`), se o dispositivo falhar na inicialização do WebGL2 (context loss ou navegadores bloqueados), o VFX-JS deve degradar silenciosamente mantendo a renderização CSS pura visível.
4. **Gerenciamento de Bounding Box e `overflow`**:
   - Shaders com deslocamento de vértices ou dispersão cromática precisam do parâmetro `overflow` (ex: `overflow: 80`). Caso o elemento pai possua `overflow: hidden` no CSS, os fragmentos gerados pelo shader que extrapolam a caixa serão cortados pelo motor de composição do browser.

---

## 4. Catálogo de Efeitos, Primitivas e Padrões de Animação

Abaixo, detalhamos **10 efeitos e primitivas fundamentais** disponibilizados nativamente ou construídos com a arquitetura do VFX-JS:

### 1. `rgbShift` (Dispersão Cromática Prismática)
- **Comportamento Visual**: Divide a textura do elemento nos canais vermelho, verde e azul (RGB), aplicando um deslocamento vetorial independente em função do tempo, do scroll ou da aceleração do cursor. O elemento adquire um relevo tridimensional similar ao das bordas de lentes analógicas ou falha de convergência de canhões de elétrons.
- **Gatilho**: Loop contínuo sutil ou modulado por velocidade de rolagem (`scrollDelta`) e hover do mouse.
- **Encaixe**: Hero headers tipográficos, imagens de produtos tecnológicos e logos vetoriais.

### 2. `glitch` (Ruptura Eletrostática por Scanlines & Jitter)
- **Comportamento Visual**: Segmenta a imagem horizontalmente em tiras randômicas calculadas por funções pseudo-aleatórias (*hash step*). As fatias sofrem saltos no eixo X sincronizados com inversões temporárias de canal e cintilação de luminância. Exige `overflow: 50` a `100` para que os fragmentos saltem além da caixa original do elemento.
- **Gatilho**: Evento instantâneo de clique, hover rápido ou reveal episódico (1 pulso a cada 3 segundos).
- **Encaixe**: Botões primários "Cyberpunk", logos de marcas de streetwear e seções de encerramento de página.

### 3. `rainbow` (Frequência Espectral & Onda Cromática)
- **Comportamento Visual**: Aplica uma matriz de transformação de espaço de cor HSV/RGB giratória sobre a textura, gerando ondas de iridescência que percorrem as áreas de luminância alta da imagem.
- **Gatilho**: Loop contínuo uniforme com modulação de velocidade angular.
- **Encaixe**: Banners comemorativos, animações em GIF transparentes e crachás visuais holográficos.

### 4. `halftone` / `HalftoneEffect` (Retícula Gráfica de Meio-Tom CMYK / Monocromática)
- **Comportamento Visual**: Converte os gradientes contínuos de uma foto ou vídeo em uma matriz geométrica de pontos circulares cuja área varia proporcionalmente à luminosidade local da cena, emulando impressões de jornais e cartazes de serigrafia dos anos 1960.
- **Gatilho**: Estático para estilização editorial ou dinâmico com escala de pontos modulada pelo scroll.
- **Encaixe**: Fotografias de editoriais de moda, vídeos de arquivo e retratos de membros da equipe.

### 5. `duotone` (Mapeamento Luminescente Bicolor de Gradiente)
- **Comportamento Visual**: Calcula a luminância em escala de cinza de cada fragmento e remapeia linearmente os tons escuros para uma cor primária (`color1`) e os tons claros para uma cor secundária (`color2`), com blending suave e uniforme.
- **Gatilho**: Estado de repouso ou transição cromática suave baseada na troca de paleta do tema (Light/Dark).
- **Encaixe**: Imagens de fundo para preservar legibilidade de textos sobrepostos e thumbnails de vídeos institucionais.

### 6. `sinewave` (Ondulação Líquida Trigonométrica)
- **Comportamento Visual**: Aplica distorção senoidal contínua sobre as coordenadas UV da textura (`uv.y += sin(uv.x * freq + time) * amp`), criando a ilusão ótica de refração sob superfície aquática ou ondulação de fita sob brisa.
- **Gatilho**: Loop contínuo com atenuação de amplitude no repouso do mouse.
- **Encaixe**: Banners de eventos aquáticos, elementos de fundo abstratos e ilustrações orgânicas.

### 7. `slitScanTransition` (Distorção Temporal por Fatiamento de Viewport)
- **Comportamento Visual**: Conforme o elemento entra no viewport, uma linha temporal de corte (*slit scan*) varre o elemento de cima a baixo. Os pixels superiores entram em estado final enquanto os inferiores continuam em distorção de cisalhamento, gerando uma entrada cinemática hipnótica.
- **Gatilho**: `IntersectionObserver` com threshold configurado em `0.2` a `1.0`.
- **Encaixe**: Revelação de imagens de cases na rolagem vertical de portfólios.

### 8. `warpTransition` (Distorção Gravitacional Esférica de Entrada)
- **Comportamento Visual**: No instante de cruzamento do limite da tela, a textura é deformada a partir do centro através de um cálculo de curvatura esférica/lente olho-de-peixe que se contrai progressivamente até atingir coordenadas planas estáveis.
- **Gatilho**: Gatilho de scroll de primeira visualização (`once: true`).
- **Encaixe**: Galerias de fotos com scroll horizontal ou vertical dinâmico.

### 9. `pixelateTransition` / `focusTransition` (Quantização de Resolução & Desfocagem Óptica)
- **Comportamento Visual**: Inicia com uma taxa de subamostragem extrema (blocos de 64px) que converge exponencialmente para a resolução nativa de 1px, acompanhada de ajuste fino de nitidez focal.
- **Gatilho**: Montagem do componente no React ou scroll reveal em seções editoriais.
- **Encaixe**: Imagens de produtos de alta resolução e cartões de mídia.

### 10. `BloomEffect` & `ScanlineEffect` (Emulação CRT de Tubo de Raios Catódicos)
- **Comportamento Visual**: Combina um passe de bloom piramidal de luminância com linhas de varredura horizontais equidistantes (*scanlines*), reproduzindo a fluorescência de telas de computador industriais dos anos 1980.
- **Gatilho**: Composição encadeada em pipeline multi-pass (`@vfx-js/effects`).
- **Encaixe**: Terminais de desenvolvedor interativos, emuladores e interfaces retro-tech.

---

## 5. Matemática do Movimento & Receitas de Código

### A Engenharia Sob o Capô: Mapeamento Global para Local

O núcleo do VFX-JS opera através de um único elemento `<canvas>` WebGL2 posicionado com `position: fixed; inset: 0; pointer-events: none; z-index: ...`. Para mapear múltiplos nós do DOM para o espaço de coordenadas de projeção uniforme do WebGL sem criar múltiplos contextos, a biblioteca adota a seguinte formulação matemática:

$$uv = \frac{gl\_FragCoord.xy - u\_offset}{u\_resolution}$$

Onde:
- $gl\_FragCoord.xy$ são os pixels nativos da janela na convenção do OpenGL (com a origem $(0, 0)$ no canto inferior esquerdo);
- $u\_offset$ representa a coordenada do nó calculada por `getBoundingClientRect()`, convertida para o sistema de coordenadas do WebGL e multiplicada por `window.devicePixelRatio`;
- $u\_resolution$ é a largura e altura do elemento (somadas ao dobro da margem de `overflow`), também escaladas pelo DPR da tela.

```
┌────────────────────────────────────────────────────────────────────────┐
│                   MAPEAMENTO DE COORDENADAS UV DO VFX-JS               │
└────────────────────────────────────────────────────────────────────────┘
  Viewport do Navegador (0,0 no canto superior esquerdo)
  ┌───────────────────────────────────────────────────────┐
  │                                                       │
  │        ┌─────────────────────────┐                    │
  │        │ Elemento HTML Alvo      │                    │
  │        │ [img, video, span]      │                    │
  │        │                         │                    │
  │        │  (offset.x, offset.y)   │                    │
  │        └─────────────────────────┘                    │
  │                                                       │
  └───────────────────────────────────────────────────────┘
                              │
                              ▼ Conversão de Espaço para GLSL
  Sistema OpenGL (0,0 no canto inferior esquerdo da tela)
  gl_FragCoord.y = (window.innerHeight - clientRect.bottom) * DPR
  gl_FragCoord.x = clientRect.left * DPR
```

### Curvas de Movimento e Parâmetros Físicos Recomendados

Para sincronizar shaders com eventos de interface, utilize parâmetros de interpolação e funções de easing físico:

- **Ease-Out-Expo (Interpolação de Fade de Glitch)**:
  $$f(t) = 1.0 - 2.0^{-10t}$$
  CSS correspondente: `cubic-bezier(0.16, 1, 0.3, 1)`. Ideal para retorno rápido do shader ao estado de repouso após um pulso de hover.
- **Amortecimento Exponencial de Mouse / Scroll (LERP Frame a Frame)**:
  ```typescript
  // Atualizado dentro do RAF
  currentVelocity = lerp(currentVelocity, targetVelocity, 1.0 - Math.exp(-12.0 * deltaTime));
  ```
- **Frequência e Harmônicos de Ruído (Simplex / Hash)**:
  - Frequência base: `vec2 freq = uv * 8.0;`
  - Amplitude de deslocamento máximo para texto: $\le 0.02$ (evita quebra total de legibilidade).
  - Amplitude para imagens com `overflow`: até $0.15$.

---

### Receita de Código Funcional em Produção: React 19 + Tailwind CSS + VFX-JS

Abaixo está o componente completo e testado, pronto para ser injetado em projetos corporativos ou portfólios modernos, incluindo controle de `prefers-reduced-motion`, detecção de device pixel ratio, hover interativo e limpeza correta de memória GPU:

```tsx
import React, { useEffect, useRef, useState } from "react";
import { VFX } from "@vfx-js/core";

interface ChromaticHeroProps {
  title: string;
  tagline: string;
  mediaSrc: string;
  mediaAlt: string;
}

export const ChromaticHero: React.FC<ChromaticHeroProps> = ({
  title,
  tagline,
  mediaSrc,
  mediaAlt,
}) => {
  const containerRef = useRef<HTMLDivElement>(null);
  const imageRef = useRef<HTMLImageElement>(null);
  const textRef = useRef<HTMLHeadingElement>(null);
  
  // Controle de intensidade dinâmica baseado em interação
  const [isHovered, setIsHovered] = useState(false);
  const hoverIntensityRef = useRef(0);

  useEffect(() => {
    // 1. Respeito rigoroso às preferências de acessibilidade do usuário
    const prefersReducedMotion = window.matchMedia(
      "(prefers-reduced-motion: reduce)"
    ).matches;

    if (prefersReducedMotion) {
      return; // Mantém a renderização puramente nativa do HTML/CSS
    }

    // 2. Instanciação única do motor VFX gerenciador de canvas global
    const vfx = new VFX();

    // 3. Shader GLSL customizado para o elemento de imagem
    const imageShader = `
      precision highp float;
      uniform vec2 resolution;
      uniform vec2 offset;
      uniform float time;
      uniform float intensity;
      uniform sampler2D src;
      out vec4 outColor;

      // Função de hash pseudo-aleatória
      float hash(vec2 p) {
        return fract(sin(dot(p, vec2(127.1, 311.7))) * 43758.5453123);
      }

      void main() {
        vec2 uv = (gl_FragCoord.xy - offset) / resolution;

        // Ondulação sutil contínua
        float wave = sin(uv.y * 18.0 + time * 2.5) * 0.003 * (0.2 + intensity);
        
        // Fator de dispersão cromática impulsionado pelo hover
        float shift = (0.008 + intensity * 0.025) + wave;

        // Separação de canais RGB
        float r = texture(src, vec2(uv.x + shift, uv.y)).r;
        float g = texture(src, vec2(uv.x, uv.y)).g;
        float b = texture(src, vec2(uv.x - shift, uv.y)).b;
        float a = texture(src, uv).a;

        // Fatias micro-glitch aleatórias quando sob hover intenso
        if (intensity > 0.4) {
          float slice = step(0.96, hash(vec2(floor(uv.y * 40.0), floor(time * 15.0))));
          float glitchShift = slice * 0.04 * (hash(vec2(time, uv.y)) - 0.5);
          r = texture(src, vec2(uv.x + shift + glitchShift, uv.y)).r;
          b = texture(src, vec2(uv.x - shift - glitchShift, uv.y)).b;
        }

        outColor = vec4(r, g, b, a);
      }
    `;

    // 4. Associação da Imagem ao VFX com uniforms dinâmicos reavaliados por frame
    if (imageRef.current) {
      vfx.add(imageRef.current, {
        shader: imageShader,
        overflow: 80, // Permite que a dispersão dos canais transborde 80px sem clipping
        uniforms: {
          intensity: () => hoverIntensityRef.current,
        },
      });
    }

    // 5. Associação do Título Tipográfico ao Preset Nativo 'rgbShift'
    if (textRef.current) {
      vfx.add(textRef.current, {
        shader: "rgbShift",
        overflow: 30,
      });
    }

    // 6. Loop de amortecimento da intensidade física (LERP)
    let animationFrameId: number;
    let lastTime = performance.now();

    const updatePhysics = (now: number) => {
      const dt = (now - lastTime) / 1000;
      lastTime = now;

      const target = isHovered ? 1.0 : 0.0;
      // Amortecimento suave de retorno (decay = 8.0)
      hoverIntensityRef.current +=
        (target - hoverIntensityRef.current) * (1.0 - Math.exp(-8.0 * dt));

      animationFrameId = requestAnimationFrame(updatePhysics);
    };

    animationFrameId = requestAnimationFrame(updatePhysics);

    // 7. Limpeza rigorosa e destruição de recursos ao desmontar o componente
    return () => {
      cancelAnimationFrame(animationFrameId);
      if (imageRef.current) vfx.remove(imageRef.current);
      if (textRef.current) vfx.remove(textRef.current);
      vfx.destroy();
    };
  }, [isHovered]);

  return (
    <section
      ref={containerRef}
      className="relative min-h-[90vh] w-full flex flex-col justify-center items-center px-6 py-24 bg-zinc-950 text-zinc-100 overflow-hidden select-none"
    >
      <div className="max-w-5xl mx-auto flex flex-col items-center text-center z-10 space-y-8">
        {/* Título H1 tipográfico com WebGL Post-Processing */}
        <h1
          ref={textRef}
          className="text-5xl md:text-7xl lg:text-8xl font-black tracking-tighter uppercase font-mono cursor-pointer"
        >
          {title}
        </h1>

        <p className="max-w-xl text-lg md:text-xl text-zinc-400 font-sans font-light leading-relaxed">
          {tagline}
        </p>

        {/* Card de Mídia Interativo que modula o Fragment Shader */}
        <div
          className="relative group cursor-crosshair mt-8 p-3 rounded-2xl bg-zinc-900/60 border border-zinc-800 shadow-2xl backdrop-blur-sm transition-all duration-500 hover:border-zinc-600"
          onMouseEnter={() => setIsHovered(true)}
          onMouseLeave={() => setIsHovered(false)}
        >
          <img
            ref={imageRef}
            src={mediaSrc}
            alt={mediaAlt}
            className="w-[320px] sm:w-[480px] md:w-[640px] h-[360px] md:h-[420px] object-cover rounded-xl transition-transform duration-700 ease-out group-hover:scale-[1.02]"
            loading="eager"
          />

          <div className="absolute bottom-6 left-6 right-6 flex items-center justify-between pointer-events-none">
            <span className="text-xs font-mono tracking-widest text-zinc-300 bg-black/60 px-3 py-1.5 rounded-md backdrop-blur-md uppercase border border-white/10">
              GLSL 300 ES • Multi-Channel
            </span>
            <span className="text-xs font-mono text-emerald-400 flex items-center gap-1.5 bg-black/60 px-3 py-1.5 rounded-md backdrop-blur-md border border-white/10">
              <span className="w-2 h-2 rounded-full bg-emerald-400 animate-pulse" />
              60 FPS GPU
            </span>
          </div>
        </div>
      </div>

      {/* Grid de fundo decorativo neutro (os 60% da fundação estrutural) */}
      <div
        className="absolute inset-0 pointer-events-none opacity-20 bg-[linear-gradient(to_right,#80808012_1px,transparent_1px),linear-gradient(to_bottom,#80808012_1px,transparent_1px)] bg-[size:32px_32px]"
        aria-hidden="true"
      />
    </section>
  );
};
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao arquitetar projetos que utilizem **VFX-JS** (`@vfx-js/core` ou `@vfx-js/react`), a IA ou o Engenheiro Líder deve especificar os seguintes tópicos técnicos no `DESIGN_BLUEPRINT.md`:

### 1. Declaração de Stack & Escopo de Shaders
- **Identificação do Pacote**: `@vfx-js/core` (versão 0.7+ com suporte a GLSL 300 es e classes de efeitos) ou `@vfx-js/react` para aplicações puras React/Next.js Client Components (`"use client"`).
- **Lista de Nós Ancorados**: Especificar com exatidão quais nós do DOM receberão pós-processamento (ex: `#hero-brand-logo`, `.case-study-thumbnail`). Proibir veementemente seletores genéricos como `document.querySelectorAll('*')`.

### 2. Dimensionamento de `overflow` e Camadas de Z-Index
- Para cada nó com shaders de deslocamento (`glitch`, `rgbShift`, `warpTransition`), declarar o valor em pixels de `overflow` (ex: `overflow: 60`).
- Documentar explicitamente que os elementos pais nos containers CSS não devem possuir `overflow: hidden`, sob pena de corte dos pixels deslocados.
- Especificar o `z-index` do canvas do VFX-JS para evitar que ele encubra menus dropdown, modais e tooltips acessíveis.

### 3. Matriz de Acessibilidade & Orçamento de GPU (Performance Budget)
- **Regra de Ouro**: A media query `prefers-reduced-motion` deve anular o registro de nós no `VFX` (`vfx.remove(el)` ou desativação de loops de uniforms).
- **Limite de Nós Concorrentes no Viewport**: No máximo **4 a 6 elementos ativos** simultaneamente na mesma visualização de tela. O `IntersectionObserver` interno do VFX-JS deve suspender nós fora do viewport.
- **Resolução de Renderização**: Em telas móveis com DPR alto (> 2.5), considerar fixar o `pixelRatio` máximo em `2.0` no canvas global para evitar estrangulamento da GPU.

### 4. Estratégia de Fallback e Desmontagem de Memória
- Declarar o padrão de limpeza em hooks `useEffect`: chamada imperativa a `vfx.remove(element)` e `vfx.destroy()` na desmontagem do componente para liberar buffers de textura WebGL e evitar *memory leaks* em aplicações Single Page (SPA).
