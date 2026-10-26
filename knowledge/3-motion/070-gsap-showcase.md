---
id: "gsap-showcase"
name: "GSAP Showcase (GreenSock)"
url: "https://gsap.com/showcase/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["Cinematic Scrollytelling", "Deterministic Timeline Orchestration", "Pinned Multi-Axis Choreography", "Kinetic Split Masking", "FLIP Layout Projection", "WebGL Canvas Integration"]
densidade_informacao: "Independente"
impacto_visual: "Cinematografico/Showstopper"
custo_computacional: "Medio a Alto (RAF Timeline + ScrollTrigger Virtualization + WebGL Bridge)"
stack_frameworks: ["GSAP 3", "ScrollTrigger", "Flip", "SplitText", "Observer", "Draggable", "Three.js / WebGL", "React (@gsap/react)", "Lenis / ScrollSmoother", "TypeScript / Tailwind CSS"]
compatibilidade:
  combinacoes_recomendadas: ["Lenis + GSAP ScrollTrigger", "Three.js (R3F) + GSAP useGSAP", "Tailwind CSS + SplitText", "Flip + Radix UI Primitives", "CustomEase + SVG Morphing"]
  conflitos_esteticos: ["Transições CSS puras declaradas simultaneamente nos mesmos nós animados por GSAP (conflito de cascata e render jank)", "Scroll hijacking agressivo sem inércia em dispositivos touch", "Reflow forçado animando propriedades de layout geométricas (width, height, top, left) sem usar transforms acelerados por hardware", "Execução de timelines GSAP sem ciclo de cleanup/revert em montagens reativas (React StrictMode)"]
---

# GSAP Showcase (GreenSock) — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)

O **GSAP Showcase** (`https://gsap.com/showcase/`) é o epicentro global da computação criativa na web moderna. Ele indexa os projetos digitais mais premiados da indústria (vencedores frequentes de *Site of the Year*, *Site of the Month* e *Developer Awards* no Awwwards, FWA e CSS Design Awards), criados por estúdios de vanguarda como Active Theory, Immersive Garden, Resn, Locomotive, Studio Freight, Dogstudio e Merci-Michel. 

Mais do que uma biblioteca de animação, o **GSAP (GreenSock Animation Platform)**, arquitetado por **Jack Doyle**, define a gramática fundamental da narrativa interativa digital através de um paradigma estrutural: a **Linha do Tempo Determinística e Não-Linear**.

```
┌────────────────────────────────────────────────────────────────────────┐
│               GSAP 3 DETERMINISTIC TIMELINE ARCHITECTURE              │
└────────────────────────────────────────────────────────────────────────┘
                                    │
               Virtual Playhead scrub / time() position
                                    │
       ┌────────────────────────────┼────────────────────────────┐
       ▼                            ▼                            ▼
┌──────────────┐             ┌──────────────┐             ┌──────────────┐
│  Timeline A  │             │  Timeline B  │             │ WebGL / R3F  │
│  (DOM Node)  │             │ (SplitText)  │             │ (Uniforms)   │
├──────────────┤             ├──────────────┤             ├──────────────┤
│ xPercent: -50│             │ y: "110%"    │             │ uProgress: 1 │
│ ease: none   │             │ stagger: 0.05│             │ camera.z: 5  │
└──────────────┘             └──────────────┘             └──────────────┘
       ▲                            ▲                            ▲
       └────────────────────────────┼────────────────────────────┘
                                    │
                        ┌───────────────────────┐
                        │     ScrollTrigger     │
                        │  (trigger, pin, lerp) │
                        └───────────────────────┘
                                    ▲
                                    │
                        ┌───────────────────────┐
                        │   Lenis Smooth RAF    │
                        │ (Inertial Scroll Bus) │
                        └───────────────────────┘
```

### O Paradigma da Partitura Musical vs. Eventos Reativos Isolados
Enquanto a maioria das bibliotecas foca em transições isoladas de componentes disparadas por mudanças de estado (`state change -> animation`), o GSAP trata a interface como uma **partitura orquestral contínua**:
- **Playhead Absoluto e Reversibilidade Perfeita**: Uma timeline GSAP (`gsap.timeline()`) calcula interpolações em qualquer ponto do tempo matemático ($t \in [0, T]$). Ela pode ser avançada, retrocedida, pausada, acelerada (`timeScale`), revertida ou scrubbada em sincronia milimétrica com a taxa de rolagem, sem acúmulo de erros de arredondamento de ponto flutuante.
- **Scrubbing Cinematográfico ("A Barra de Rolagem como Agulha de Toca-Discos")**: Com o `ScrollTrigger`, o usuário não está apenas rolando uma página de texto; seu movimento de dedo controla diretamente a agulha de reprodução de uma sequência cinematográfica complexa. O viewport pode congelar no espaço (`pin: true`), enquanto translações multi-eixo, rotações 3D, câmeras WebGL e tipografia cinética desenrolam-se sob o controle total do usuário.
- **Arquitetura de Zero Garbage Collection no Render Loop**: O GSAP foi construído para sobreviver sob condições extremas de estresse gráfico. O core do motor reutiliza instâncias de tweens internas através de pools de memória dedicados, evitando alocações dinâmicas de objetos no `requestAnimationFrame`, prevenindo os temidos "GC pauses" (micropausas de coleta de lixo) que derrubam as taxas de quadro de 120fps/60fps.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Seções e Experiências Insubstituíveis
1. **Brand Flagships & Product Landing Pages de Alto Impacto (Nível Apple / Tesla / Awwwards)**: Apresentação de hardware, moda de luxo, arquitetura e lançamentos de produtos SaaS de ponta onde cada seção precisa contar uma história sequencial com revelações progressivas.
2. **Pinned Horizontal Scroll Storytelling**: Narrativas panorâmicas onde a rolagem vertical tradicional é convertida fluidamente em uma translação horizontal contínua de múltiplos painéis, sem desorientar a navegação do usuário.
3. **Páginas Híbridas DOM + WebGL (Three.js / React Three Fiber)**: Sincronização direta entre o scroll da página HTML e propriedades da cena 3D (posição e rotação da câmera, distorção de shaders via uniforms `uProgress`, abertura de portas ou desmonte de peças mecânicas).
4. **Transições de Estado Complexas (FLIP Gallery-to-Detail)**: Casos em que um elemento da grade precisa se transformar em um visualizador de tela cheia sem jank de repintura do DOM, recalculando deltas de escala e translação instantaneamente.
5. **Tipografia Editorial Cinematográfica**: Portfólios de design e agências onde o texto é o protagonista estético, exigindo máscaras de linha por linha (`SplitText`) e ritmo tipográfico escultural.

### Papel na Regra 60-30-10
- **60% (Estrutura e Legibilidade Limpa)**: O layout do site mantém um grid tipográfico estável, proporções áureas e espaços em branco generosos. O GSAP **não** é usado para enfeitar botões triviais ou menus simples com animações circenses desnecessárias.
- **30% (Fluidez e Inércia Invisível)**: A rolagem ganha inércia suave com `Lenis` ou `ScrollSmoother`, desacoplando a resposta mecânica bruta do mouse/trackpad e convertendo-a em uma curva de desaceleração elástica. Micro-interações de navegação (cursor magnético sutil, hover de links com sublinhado elástico) operam aqui para conferir refinamento tátil sem bloquear o usuário.
- **10% (O Espetáculo Showstopper / Assinatura Visual)**: O Hero reveal com preloader cortina coreografado, a transição entre seções chave com pinning e distorção WebGL, e a expansão de cards FLIP em tela cheia. Este é o ápice memorável da experiência.

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Quando Evitar
- **Sistemas B2B Analíticos e Dashboards Utilitários**: Ambientes de alta produtividade (painéis financeiros, CRMs, tabelas de dados densas, checkout de e-commerce). Nesses contextos, qualquer latência imposta por pins ou delays de timeline frustra o operador humano e prejudica a conversão.
- **Páginas Puramente Textuais de Conteúdo Longo**: Artigos de documentação ou blogs informativos onde o usuário busca velocidade de leitura linear e busca via Ctrl+F (o uso imprudente de SplitText ou pins pode quebrar a experiência nativa do navegador).
- **Dispositivos de Baixa Potência com Bateria Crítica**: Executar animações contínuas em loop sem pausas inteligentes quando o elemento sai da viewport drena drasticamente a bateria em smartphones de entrada.

### ⚠️ Regras Rígidas de GPU, Acessibilidade e Estabilidade Mobile
1. **Regra Absoluta do Transform & Opacity**: Jamais anime propriedades que desencadeiam layout reflow no pipeline do navegador (`top`, `left`, `width`, `height`, `margin`, `padding`). Anime exclusivamente propriedades compostas na GPU: `x`, `y`, `xPercent`, `yPercent`, `scale`, `rotation`, `opacity` e `clip-path`.
2. **Acessibilidade Universal Obrigatória (`prefers-reduced-motion`)**:
   ```javascript
   const prefersReducedMotion = window.matchMedia("(prefers-reduced-motion: reduce)").matches;
   if (prefersReducedMotion) {
     ScrollTrigger.getAll().forEach(t => t.kill());
     gsap.globalTimeline.clear();
   }
   ```
   Quando o usuário solicita redução de movimento, todos os pins e scrubs devem ser neutralizados, exibindo o conteúdo em seu layout natural verticalizado.
3. **Acessibilidade de Tipografia com SplitText**:
   O `SplitText` injeta múltiplos elementos `<div>` para fatiar palavras e caracteres, o que corrompe leitores de tela caso o nó original não seja protegido:
   ```html
   <h1 aria-label="Texto Completo Original Legível para Screen Readers">
     <span aria-hidden="true" class="split-target">Texto Completo Original</span>
   </h1>
   ```
4. **Instabilidade de Viewport Mobile (Safari iOS Address Bar Resize)**:
   A barra de endereços móvel encolhe e expande durante o scroll, disparando eventos de `resize` que recalcula o tamanho da janela e causa saltos bruscos em seções pinadas. Configure sempre:
   ```javascript
   ScrollTrigger.config({ ignoreMobileResize: true });
   ScrollTrigger.normalizeScroll(true); // Opcional para travar overscroll bounce
   ```

---

## 4. Catálogo Detalhado de Efeitos, Primitivas e Padrões Notáveis

Abaixo estão os 10 padrões de animação mais recorrentes e aclamados nos projetos indexados no GSAP Showcase:

### 1. Pinned Horizontal Scroll Storytelling (Container Animation)
- **Comportamento Visual**: O usuário atinge uma seção que é travada na tela (`pin: true`). À medida que continua a rolar a roda do mouse ou arrastar o trackpad para baixo no eixo Y, o container de cards desliza horizontalmente no eixo X até o último painel, momento no qual a página volta a rolar verticalmente. Elementos secundários dentro dos painéis possuem velocidades paralelas independentes via `containerAnimation`.
- **Gatilho**: Progresso do ScrollTrigger associado à distância total em pixels do deslocamento horizontal (`end: () => "+=" + container.scrollWidth`).
- **Onde Encaixar**: Galerias de projetos em portfólios, linhas do tempo históricas de empresas e showrooms de coleções de produtos.

### 2. Preloader Curtain Reveal & Counter Sequence (0-100% Intro)
- **Comportamento Visual**: A página carrega com uma sobreposição escura de tela cheia exibindo uma contagem tipográfica fluida de `00` a `100%`. Ao atingir 100%, a tela se divide vertical ou horizontalmente em "cortinas" (`clip-path: inset(0 0 100% 0)` ou múltiplos painéis escalonados com `yPercent: -100`), revelando o Hero com tipografia em cascata e escala de imagem de $1.2 \to 1.0$.
- **Gatilho**: Disparo na montagem da página (`DOMContentLoaded` ou carregamento de assets críticos Three.js/imagens) seguido de timeline encadeada.
- **Onde Encaixar**: Hero inicial de sites de agências, portfólios e flagships institucionais.

### 3. Kinetic SplitText Line Masking (Editorial Title Reveal)
- **Comportamento Visual**: Títulos e frases de destaque são fatiados em linhas. Cada linha fica envelopada por um elemento pai com `overflow: hidden`. As linhas surgem do fundo com `yPercent: 110%` até `0%`, com uma rotação sutil de $3^\circ$ a $0^\circ$ e um stagger escalonado de 0.08s entre linhas, criando a sensação de tipografia saindo de um fatiador físico de papel.
- **Gatilho**: Entrada do título no viewport (`ScrollTrigger` com `start: "top 80%"`).
- **Onde Encaixar**: Headlines de seções, declarações de manifesto e chamadas de abertura.

### 4. Smooth Scroll Inertial Parallax (Lenis + ScrollTrigger Bridge)
- **Comportamento Visual**: Imagens e cartões flutuam sobre o grid com velocidades relativas distintas. Enquanto a página rola em velocidade base $v$, uma imagem de fundo desloca-se a $0.6v$ e um badge sobreposto a $1.4v$, conferindo profundidade estereoscópica e tridimensional ao layout 2D.
- **Gatilho**: Atualização frame a frame do motor de inércia virtual sincronizado com o `ScrollTrigger.update`.
- **Onde Encaixar**: Mosaicos de fotos editoriais, seções sobre a empresa e grades assimétricas.

### 5. Flip Grid-to-Fullscreen Layout Morphing
- **Comportamento Visual**: Ao clicar em uma miniatura de produto ou case em uma grade, o elemento expande-se suavemente para preencher o viewport inteiro como modal ou detalhe de página. Em vez de recriar o elemento, o plugin `Flip` registra a geometria inicial ($F$), a geometria final ($L$), inverte as coordenadas com transforms ($I$) e reproduz a animação em 60fps sem salto estrutural ($P$).
- **Gatilho**: Evento de clique de usuário com troca de classes de layout ou transição de rota.
- **Onde Encaixar**: Visualizadores de e-commerce de vestuário/tecnologia, galerias de fotografia e cards de cases.

### 6. WebGL Three.js Camera & Shader Uniform Scrubbing
- **Comportamento Visual**: Um canvas 3D ocupa o fundo fixo da página. Conforme o usuário navega pelas seções de texto no DOM HTML, a câmera do Three.js faz um trajeto curvo contínuo ao redor de um modelo 3D (ex: smartphone, relógio ou abstração geométrica), enquanto um shader GLSL altera sua distorção de onda ou mapa de luz proporcionalmente à variável normalizada `progress` (0.0 a 1.0) do ScrollTrigger.
- **Gatilho**: Posição contínua da barra de rolagem associada a um `gsap.timeline({ scrollTrigger: { scrub: true } })`.
- **Onde Encaixar**: Demonstrações técnicas de engenharia, landing pages de carros e experiências imersivas.

### 7. Magnetic Button with QuickTo Physics Tracking
- **Comportamento Visual**: Ao aproximar o cursor do mouse a menos de 60px de um botão de ação primária, o botão é atraído elasticamente em direção às coordenadas $(X, Y)$ do cursor, com o texto interno se deslocando com um fator adicional de deslocamento. Ao afastar o mouse, o botão retorna à posição central com física de inércia suave através de instâncias de `gsap.quickTo`.
- **Gatilho**: Eventos de `mousemove` e `mouseleave` sobre o elemento delimitador.
- **Onde Encaixar**: Botões de Call-to-Action (CTA) flutuantes, gatilhos de menu hambúrguer e controles de navegação de carrossel.

### 8. Card Stacking / Deck Peeling Overlap
- **Comportamento Visual**: Múltiplos cartões de seções sucessivas fixam-se no topo da tela à medida que atingem o topo do viewport. Conforme o próximo cartão sobe, o cartão anterior encolhe suavemente (`scale: 0.92`), escurece (`filter: brightness(0.6)`) e ganha um blur sutil, empilhando-se em profundidade física como um maço de cartas antes que o fluxo normal continue.
- **Gatilho**: `ScrollTrigger` com `pin: true` e `scrub: true` encadeado para cada item da lista.
- **Onde Encaixar**: Apresentação de planos de preços, etapas de um processo ou benefícios centrais de uma tecnologia.

### 9. SVG Morphing & Path Following Choreography
- **Comportamento Visual**: Linhas de conexão ou formas geométricas orgânicas no fundo se transformam fluidamente entre diferentes estados de vetores SVG (ex: de uma gota orgânica para uma elipse técnica) usando `MorphSVGPlugin`. Simultaneamente, elementos gráficos ou indicadores de progresso viajam ao longo do caminho vetorial curvo usando `MotionPathPlugin`.
- **Gatilho**: Scroll progress contínuo ou transição de abas interativas.
- **Onde Encaixar**: Diagramas de fluxo de dados, infográficos dinâmicos e ilustrações decorativas de fundo.

### 10. ScrambleText Terminal Kinetic Decode
- **Comportamento Visual**: Rótulos técnicos, números de versão, metadados e tags de categorias decodificam rapidamente uma série de caracteres alfanuméricos ou símbolos aleatórios (ex: `#$@&%9X...`) até revelarem a palavra final com ritmo ultra-rápido de alta tecnologia.
- **Gatilho**: Hover do mouse sobre badges, revelação de cartões ou troca de filtros.
- **Onde Encaixar**: Interfaces de temática cyberpunk, dados de telemetria em tempo real, credenciais técnicas e cabeçalhos de código.

---

## 5. Matemática do Movimento & Receitas de Código

### Curvas de Easing Canônicas e Parâmetros
No GSAP Showcase, a escolha da curva define a personalidade da marca. Evita-se estritamente o `linear` (exceto em scrubs contínuos de scroll) ou o `ease-in-out` padrão do CSS.

```javascript
import { gsap } from "gsap";
import { CustomEase } from "gsap/CustomEase";

gsap.registerPlugin(CustomEase);

// 1. O Ease do Luxo Suíço (Snappy & Controlled)
// Arrancada rápida com desaceleração prolongada e majestosa, sem overshoot
export const EASE_LUXURY = "power4.out"; // cúbica equivalente a cubic-bezier(0.25, 1, 0.5, 1)

// 2. O Ease "Organic Hop" (Signature Award Winners)
// Leve overshoot elástico calculado matematicamente para cards e overlays
CustomEase.create("hop", "M0,0 C0.05,0 0.133,0.06 0.166,0.208 0.207,0.392 0.297,0.672 0.384,0.784 0.444,0.86 0.542,1 1,1");

// 3. Easing para Parallax / Scrub de Rolo do Mouse
// No ScrollTrigger com scrub, usa-se scrub numérico para amortecimento inercial:
// scrub: 1 significa que o playhead demora 1 segundo para alcançar a posição real da rolagem
```

### Parâmetros Recomendados de Smooth Scroll (Lenis Engine)
```typescript
export const LENIS_CONFIG = {
  lerp: 0.08,             // Fator de interpolação linear (0.05 mais viscoso, 0.12 mais reativo)
  duration: 1.2,          // Duração da inércia
  smoothWheel: true,      // Intercepta e suaviza a roda do mouse
  wheelMultiplier: 0.9,   // Reduz o salto excessivo em mouses de clique mecânico
  touchMultiplier: 1.8,   // Mantém sensibilidade responsiva em touch screens
};
```

---

### Receita de Produção: Pinned Horizontal Scroll Showcase com Lenis, SplitText e Scope Cleanup

O código abaixo é uma implementação em nível de produção utilizando **React 19/18**, **TypeScript**, **Tailwind CSS**, **Lenis**, e o ecossistema oficial do **GSAP com `@gsap/react` (`useGSAP`)**, garantindo que não ocorram vazamentos de memória, quebras no StrictMode ou inconsistências no cálculo de layout:

```tsx
import React, { useEffect, useRef } from "react";
import Lenis from "lenis";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { useGSAP } from "@gsap/react";

// Registra plugins oficiais do GSAP
gsap.registerPlugin(ScrollTrigger, useGSAP);

interface ProjectItem {
  id: string;
  title: string;
  category: string;
  year: string;
  image: string;
}

const PROJECTS: ProjectItem[] = [
  {
    id: "01",
    title: "Aura Kinetic Architecture",
    category: "Spatial Experience",
    year: "2026",
    image: "https://images.unsplash.com/photo-1600585154340-be6161a56a0c?q=80&w=1200&auto=format&fit=crop",
  },
  {
    id: "02",
    title: "Neuro Lumina Shaders",
    category: "Generative Canvas",
    year: "2026",
    image: "https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?q=80&w=1200&auto=format&fit=crop",
  },
  {
    id: "03",
    title: "Chronos Obsidian Studio",
    category: "Interactive Narrative",
    year: "2025",
    image: "https://images.unsplash.com/photo-1550684848-fac1c5b4e853?q=80&w=1200&auto=format&fit=crop",
  },
  {
    id: "04",
    title: "Vortex Sound Synthesis",
    category: "Creative Technology",
    year: "2025",
    image: "https://images.unsplash.com/photo-1518770660439-4636190af475?q=80&w=1200&auto=format&fit=crop",
  },
];

export const GsapHorizontalShowcase: React.FC = () => {
  const containerRef = useRef<HTMLDivElement>(null);
  const trackRef = useRef<HTMLDivElement>(null);
  const titleMaskRef = useRef<HTMLHeadingElement>(null);

  // 1. Orquestração do Motor de Inércia de Scroll (Lenis) sincronizado com ScrollTrigger
  useEffect(() => {
    // Respeita acessibilidade nativa
    if (window.matchMedia("(prefers-reduced-motion: reduce)").matches) {
      return;
    }

    const lenis = new Lenis({
      lerp: 0.08,
      smoothWheel: true,
      wheelMultiplier: 1.0,
    });

    lenis.on("scroll", ScrollTrigger.update);

    const updateLenis = (time: number) => {
      lenis.raf(time * 1000);
    };

    gsap.ticker.add(updateLenis);
    gsap.ticker.lagSmoothing(0); // Evita pulo de tempo após alternar abas

    return () => {
      gsap.ticker.remove(updateLenis);
      lenis.destroy();
    };
  }, []);

  // 2. Animação Coreográfica GSAP com useGSAP (Scoping seguro & Cleanup automático)
  useGSAP(
    () => {
      if (!trackRef.current || !containerRef.current) return;

      const prefersReduced = window.matchMedia("(prefers-reduced-motion: reduce)").matches;
      if (prefersReduced) return;

      const track = trackRef.current;
      const totalWidth = track.scrollWidth;
      const windowWidth = window.innerWidth;
      const xDistance = totalWidth - windowWidth;

      // Timeline 1: Pinned Horizontal Scroll dos Projetos
      const horizontalTl = gsap.timeline({
        scrollTrigger: {
          trigger: containerRef.current,
          pin: true,
          scrub: 1.2, // Amortecimento de 1.2 segundos para fluidez ultra-cinematográfica
          start: "top top",
          end: () => `+=${xDistance}`,
          invalidateOnRefresh: true, // Recalcula responsivamente em resize
        },
      });

      horizontalTl.to(track, {
        x: -xDistance,
        ease: "none", // Scrub linear contínuo subordinado ao controle do scroll
      });

      // Timeline 2: Efeito Parallax Individual nas Imagens dos Cards
      const projectImages = gsap.utils.toArray<HTMLImageElement>(".showcase-image");
      projectImages.forEach((img) => {
        gsap.fromTo(
          img,
          { scale: 1.25, xPercent: -10 },
          {
            scale: 1.0,
            xPercent: 10,
            ease: "none",
            scrollTrigger: {
              trigger: img,
              containerAnimation: horizontalTl, // Sincroniza com a timeline horizontal!
              start: "left right",
              end: "right left",
              scrub: true,
            },
          }
        );
      });

      // Timeline 3: Kinetic Line Mask Reveal no Título da Seção
      if (titleMaskRef.current) {
        gsap.fromTo(
          titleMaskRef.current.querySelectorAll(".mask-line"),
          { yPercent: 120, rotateZ: 3, opacity: 0 },
          {
            yPercent: 0,
            rotateZ: 0,
            opacity: 1,
            stagger: 0.1,
            duration: 1.4,
            ease: "power4.out",
            scrollTrigger: {
              trigger: titleMaskRef.current,
              start: "top 85%",
            },
          }
        );
      }
    },
    { scope: containerRef }
  );

  return (
    <div className="bg-[#0b0c10] text-[#f5f5f7] min-h-screen selection:bg-white selection:text-black font-sans antialiased">
      {/* Seção Superior de Abertura */}
      <section className="h-[80vh] flex flex-col justify-end px-8 md:px-24 pb-16">
        <div ref={titleMaskRef} className="max-w-4xl overflow-hidden">
          <div className="overflow-hidden">
            <span className="mask-line block text-xs md:text-sm font-mono uppercase tracking-[0.3em] text-[#8e8e93] mb-4">
              [ 070 // ARCHITECTURE SHOWCASE ]
            </span>
          </div>
          <div className="overflow-hidden">
            <h1 className="mask-line block text-4xl sm:text-6xl md:text-8xl font-medium tracking-tight leading-[1.05]">
              Curated Digital
            </h1>
          </div>
          <div className="overflow-hidden">
            <h1 className="mask-line block text-4xl sm:text-6xl md:text-8xl font-serif italic text-white/70 tracking-tight leading-[1.05]">
              Visions & Motion
            </h1>
          </div>
        </div>
      </section>

      {/* Container Principal Pinned Horizontal */}
      <div ref={containerRef} className="relative w-full h-screen overflow-hidden bg-[#07080a]">
        {/* Marcador Fixo de Progresso & Metadados */}
        <div className="absolute top-10 left-8 md:left-24 z-20 pointer-events-none flex items-center gap-6">
          <div className="w-2.5 h-2.5 rounded-full bg-emerald-400 animate-pulse" />
          <span className="text-xs font-mono uppercase tracking-widest text-[#a1a1a6]">
            Selected Works // 2025—2026
          </span>
        </div>

        {/* Trilho Horizontal que se move no eixo X */}
        <div
          ref={trackRef}
          className="flex flex-row items-center h-full pl-8 md:pl-24 pr-[25vw] will-change-transform gap-16 md:gap-28"
        >
          {PROJECTS.map((item, index) => (
            <article
              key={item.id}
              className="relative flex-shrink-0 w-[78vw] sm:w-[55vw] md:w-[38vw] lg:w-[32vw] group cursor-pointer"
            >
              {/* Moldura da Imagem com Overflow Hidden para Mascarar o Parallax */}
              <div className="relative aspect-[4/5] w-full overflow-hidden rounded-xl bg-[#1c1c1e] border border-white/10 shadow-2xl transition-colors duration-500 group-hover:border-white/30">
                <img
                  src={item.image}
                  alt={item.title}
                  loading="lazy"
                  className="showcase-image absolute inset-0 w-full h-full object-cover will-change-transform"
                />
                <div className="absolute inset-0 bg-gradient-to-t from-black/80 via-black/20 to-transparent opacity-60 group-hover:opacity-40 transition-opacity duration-500" />
                
                {/* Badge Flutuante Interno */}
                <div className="absolute top-6 right-6 px-3 py-1 rounded-full bg-black/60 backdrop-blur-md border border-white/15 text-[11px] font-mono tracking-wider">
                  {item.year}
                </div>

                <div className="absolute bottom-8 left-8 right-8">
                  <p className="text-xs font-mono uppercase tracking-widest text-emerald-400 mb-2">
                    {item.category}
                  </p>
                  <h3 className="text-2xl md:text-3xl font-medium tracking-tight text-white group-hover:translate-x-1.5 transition-transform duration-300">
                    {item.title}
                  </h3>
                </div>
              </div>

              {/* Numeração de Índice Abaixo do Card */}
              <div className="flex justify-between items-center mt-5 px-1 text-[#86868b] text-xs font-mono">
                <span>INDEX // 0{index + 1}</span>
                <span className="group-hover:text-white transition-colors duration-300">
                  EXPLORE CASE &rarr;
                </span>
              </div>
            </article>
          ))}
        </div>
      </div>

      {/* Seção Subsequente para Retomada do Scroll Vertical */}
      <section className="h-screen flex items-center justify-center px-8 text-center bg-[#0b0c10] border-t border-white/5">
        <div className="max-w-2xl">
          <p className="text-xs font-mono uppercase tracking-[0.25em] text-[#8e8e93] mb-4">
            End of Showcase Sequence
          </p>
          <h2 className="text-3xl sm:text-5xl font-light tracking-tight text-white">
            Transforming interfaces into kinetic brand experiences.
          </h2>
        </div>
      </section>
    </div>
  );
};

export default GsapHorizontalShowcase;
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao arquitetar projetos que utilizem animações avançadas inspiradas no GSAP Showcase, a IA deve incorporar as seguintes especificações técnicas no `DESIGN_BLUEPRINT.md` antes da geração de código:

### 1. Declaração Formal da Pilha de Movimento
- **Motor Primário**: `gsap` (versão 3.12+).
- **Plugins Oficiais Registrados**: Listar explicitamente (`ScrollTrigger`, `Flip`, `SplitText`, `Observer`).
- **Hook Reativo Oficial**: Obrigatório o uso de `@gsap/react` via `useGSAP()` em componentes React, proibindo o uso solto de `useEffect` com instâncias globais que provoquem memory leaks na montagem dupla do React 18/19 StrictMode.
- **Inércia Suave de Rolo**: Declarar a biblioteca de virtual scroll integrada (recomendado: `@studio-freight/lenis` ou `lenis` nativo conectado ao `ScrollTrigger.update`).

### 2. Matriz de ScrollTriggers e Coordenadas
Para cada seção scrollytelling ou pinned da página, preencher uma tabela de parâmetros físicos:
| Seção / Componente | Elemento Trigger | Início (`start`) | Fim (`end`) | Pin (`pin: true`) | Scrub Ratio | Efeito Aplicado |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Hero Title Reveal** | `#hero` | `"top 80%"` | N/A (play once) | `false` | `false` | SplitText Line Mask (`yPercent: 120 -> 0`) |
| **Horizontal Showcase** | `#showcase-container` | `"top top"` | `() => "+=" + trackWidth` | `true` | `1.2` (smooth) | Translação $X$ com containerAnimation nos cards |
| **Card Deck Stacking** | `.stack-card` | `"top 15%"` | `"bottom top"` | `true` | `true` | Escala regressiva (`1.0 -> 0.9`) + Opacidade |
| **WebGL Camera Orbit** | `#canvas-3d-wrapper`| `"top top"` | `"bottom bottom"` | `true` | `1.0` (direct) | Scrub de uniform `uProgress` e posição da câmera |

### 3. Checklist Rígido de Performance & Guardrails
- [ ] **GPU Acceleration**: Todas as propriedades animadas em scroll utilizam exclusivamente `x`, `y`, `xPercent`, `yPercent`, `scale`, `rotation` e `opacity`. Nenhuma propriedade de reflow (`top`, `margin`, `width`) é animada.
- [ ] **Lag Smoothing Config**: Declarado `gsap.ticker.lagSmoothing(0)` ou `gsap.ticker.lagSmoothing(500, 33)` para prevenir congelamento e saltos bruscos após o usuário alternar abas do navegador.
- [ ] **Mobile Resize Shield**: Configuração global `ScrollTrigger.config({ ignoreMobileResize: true })` declarada para evitar o colapso de viewport no Safari iOS.
- [ ] **Acessibilidade Universal (`prefers-reduced-motion`)**: Verificação programática que mata os triggers e limpa as timelines, apresentando o conteúdo em repouso sem travar a navegação para usuários sensíveis a movimento.
- [ ] **Layout Stability (Prevenção de CLS)**: Dimensões fixas, `min-height: 100vh`, ou contêineres com `aspect-ratio` definidos para evitar reflows no momento em que o ScrollTrigger calcula os marcadores de pin.
