---
id: "scroll-driven-animations"
name: "Scroll-Driven Animations (W3C CSS & WAAPI Spec)"
url: "https://scroll-driven-animations.style/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["Compositor-Thread Native Scrubbing", "Zero-JS Kinetic Feedback", "Off-Main-Thread Parallax & Stacking", "Declarative Viewport Intersections", "GPU Hardware-Accelerated Timelines"]
densidade_informacao: "Alta"
impacto_visual: "Moderado a Cinematografico/Showstopper"
custo_computacional: "Baixo (CSS/WAAPI Off-Main-Thread no Compositor de GPU)"
stack_frameworks: ["CSS Nativo (W3C CSS Animations Level 2 & Scroll-driven Animations Level 1)", "Web Animations API (WAAPI ScrollTimeline / ViewTimeline)", "Vanilla JS / TypeScript", "React 19 / 18", "Tailwind CSS (v3 / v4)", "Polyfill (flackr/scroll-timeline)"]
compatibilidade:
  combinacoes_recomendadas: ["CSS Scroll-Driven Animations + Tailwind CSS (Arbitrary Values & Custom Directives)", "CSS animation-timeline + CSS Container Queries (Style Queries via @container style())", "Scroll-driven ViewTimeline + CSS 3D Transforms (preserve-3d / perspective)", "Progressive Enhancement (@supports (animation-timeline: scroll())) + Lenis / Motion.dev fallback", "CSS scroll-timeline + native CSS scroll-snap-type / scroll-snap-align"]
  conflitos_esteticos: ["Animação contínua de propriedades de layout (width, height, top, left, margin, padding) causando continuous layout thrashing no scroll", "Filtros pesados (filter: blur(), backdrop-filter) interpolados continuamente no scroll em dispositivos móveis (GPU fillrate exhaustion)", "Concorrência de smooth scrolling via JS agressivo (wheel interception) com timelines nativas de scroll assíncrono", "Parallax caótico com velocidades relativas desproporcionais provocando cinetose (motion sickness) sem suporte a prefers-reduced-motion"]
---

# Scroll-Driven Animations — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)

Durante mais de duas décadas de desenvolvimento web, qualquer animação atrelada ao deslocamento do scroll dependia fundamentalmente de **JavaScript executando na thread principal** (*main thread*). Desenvolvedores conectavam listeners passivos ao evento `window.addEventListener('scroll', ...)`, computavam offsets via `getBoundingClientRect()` e atualizavam estilos em `requestAnimationFrame()`. 

Esse paradigma sofria de um defeito arquitetural intransponível: **o desacoplamento temporal e o Scroll Jank**. Quando a *main thread* é sobrecarregada por hidratação de componentes, processamento de dados JSON, renderizações complexas de React/Vue ou scripts analíticos de terceiros, a thread principal engasga. No entanto, o motor de rolagem moderno dos navegadores opera em uma thread dedicada — a **Compositor Thread** da GPU —, o que fazia com que o scroll físico da página continuasse rolando a 60/120Hz enquanto as animações em JavaScript ficavam congeladas ou saltavam bruscamente, quebrando a ilusão cinemática da interface.

O projeto **Scroll-Driven Animations** (`https://scroll-driven-animations.style/`), liderado pelo engenheiro de Developer Relations do Google Chrome **Bramus Van Damme** em conjunto com o **W3C CSS Working Group (CSSWG)** (especificação `scroll-animations-1`), representa a maior mudança de paradigma na engenharia de movimento web desde o advento das CSS Transitions e da Web Animations API (WAAPI):

### Os Pilares Arquiteturais do Movimento Scroll-Driven Nativo:

```
+---------------------------------------------------------------------------------------+
|                                NAVEGADOR MODERNO                                      |
+-------------------------------------------+-------------------------------------------+
|      MAIN THREAD (JavaScript & DOM)       |       COMPOSITOR THREAD (GPU / Off-Main)  |
|                                           |                                           |
| - Parse HTML & Execução de JS             | - Processa entrada de Mouse / Touch / Roda|
| - Recálculo de Estilos & Layout (Reflow)  | - Calcula deslocamento de Scroll          |
| - Árvore de Camadas (Paint / PaintOps)    | - Avalia animation-timeline: scroll/view  |
|                                           | - Interpola matrizes de transform/opacity |
| [SE A MAIN THREAD CONGELAR COM SCRIPTS]    | [O SCROLL E A ANIMAÇÃO CONTINUAM A 120FPS]|
+-------------------------------------------+-------------------------------------------+
```

1. **Scrubbing 100% Off-Main-Thread no Compositor**:
   Ao vincular uma regra `@keyframes` a um `animation-timeline: scroll()` ou `animation-timeline: view()`, o motor de layout do Chromium/WebKit/Gecko descarrega todo o ciclo de vida da animação diretamente para a *Compositor Thread*. O ponteiro temporal da animação deixa de ser o relógio universal em milissegundos (`document.timeline`) e passa a ser a **posição vetorial do scroll container** ou a **porcentagem geométrica de intersecção do elemento no scrollport**. O resultado é uma fidelidade tátil sem precedentes: a cada pixel que o dedo do usuário move no trackpad ou tela sensível ao toque, a animação avança com atraso zero (latência ultra-baixa).
2. **Dualidade de Timelines Declarativas**:
   - **Scroll Progress Timeline (`scroll()`)**: Acompanha o progresso global de rolagem de um contêiner de rolagem (por padrão, a raiz do documento `root block`). Vai de `0%` (topo máximo do scroll) até `100%` (fundo do documento).
   - **View Progress Timeline (`view()`)**: Acompanha o elemento sujeito conforme ele cruza a janela de visualização do contêiner de rolagem (*scrollport*), fracionando a viagem em zonas geométricas precisas (`entry`, `contain`, `cover`, `exit`, `entry-crossing`, `exit-crossing`).
3. **Zero Overhead de Runtime (0 KB de JavaScript)**:
   Elimina bibliotecas pesadas de terceiros (como ScrollMagic, plugins legados de scroll trigger ou scripts volumosos de monitoramento de intersecção). Todas as curvas, pontos de parada e interpolações rodam no motor C++ do navegador, preservando a vida útil da bateria de smartphones e eliminando o consumo de memória RAM do motor V8.
4. **Resolução de Fórmulas Dinâmicas em CSS (`timeline-scope`)**:
   Historicamente, elementos fora do contêiner de scroll não tinham conhecimento da rolagem de contêineres irmãos ou filhos. A especificação introduziu a propriedade `timeline-scope`, que permite elevar (*hoist*) o escopo de uma timeline nomeada para um ancestral comum, permitindo que cabeçalhos fixos, barras laterais independentes e marcadores globais reajam à rolagem de listas aninhadas sem uma única linha de JavaScript.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários

1. **Documentações Técnicas, Guias de Engenharia & Portais Editoriais de Long-Form**:
   - **Reading Progress Indicator**: Barra superior de leitura milimétrica atrelada ao scroll do documento via `scroll(root block)`.
   - **Contextual Article Progress Nav / Stepper**: Painel lateral onde títulos e seções ativas sofrem mutação visual de destaque à medida que o leitor atravessa seus limites de leitura.
2. **Landing Pages High-End & Apresentação de Produtos Flagship (Estilo Apple, Porsche, Stripe)**:
   - **Stacking Cards (Cartões Empilháveis)**: Seção de recursos onde cada card se fixa no topo via `position: sticky` e sofre contração em escala gradual (`scale(0.9)`) à medida que o card seguinte o sobrepõe, criando uma sensação física tridimensional de baralho tátil.
   - **Horizontal Pinned Section**: Travamento da viewport vertical enquanto uma esteira horizontal de especificações ou imagens técnicas corre da direita para a esquerda de maneira perfeitamente sincronizada com a rolagem vertical.
   - **3D Product Explorer / Cover Flow**: Rotação tridimensional de modelos em perspectiva ou embalagens de produtos à medida que cruzam o centro da tela.
3. **Aplicações Web B2B & Dashboards Analíticos com Tabelas Densas**:
   - **Scroll Shadows Dinâmicas**: Injeção de sombras sutis de gradiente nas bordas superior/inferior de contêineres com `overflow-y: auto`, alertando visualmente que ainda há conteúdo a ser explorado e ocultando-se sozinhas quando o fim da lista é atingido.
   - **Header Shrink com Elevação de Sombra**: O cabeçalho de navegação inicia amplo com banner e detalhes do usuário e, ao ultrapassar os primeiros 100px de scroll, contrai tipografia e aplica sombra de elevação sem nenhum listener JS.
4. **Galerias Fotográficas, Portfólios de Design & Lookbooks**:
   - **Cinematic Curtain Reveal**: Imagens que se revelam de dentro de máscaras de corte dinâmicas (`clip-path: inset(...)`) à medida que entram no viewport.

### Papel no Ritmo Visual (Regra 60-30-10)

- **60% — Estrutura e Fundo Neutro (Fundação Estática)**:
  Layouts limpos baseados em CSS Grid/Flexbox, tipografia sólida legível, superfícies estáveis (`bg-zinc-950` / `bg-white`). A imensa maioria dos blocos de texto não deve ser movida ou distorcida pelo scroll, mantendo o contraste e a densidade de leitura intocados.
- **30% — Fluidez Funcional e Micro-Feedback (Invisível aos Olhos, Sentido nos Dedos)**:
  Interações de scroll que orientam o usuário sem chamar atenção para si:
  - Transição de sombra e contração de altura do cabeçalho fixo (`animation-range: 0px 150px`);
  - Sombras de aviso de rolagem pendente em tabelas com scroll horizontal;
  - Barra de progresso discreta de 2px no topo de artigos extensos;
  - Fade-in sutil (`opacity: 0 -> 1` e `translateY(20px -> 0)`) de cartões de conteúdo à medida que entram nos primeiros 20% da janela.
- **10% — Espetáculo Visual (Showstopper / Experiência Cinematográfica)**:
  Momentos pontuais de narrativa guiada pelo scroll:
  - Uma seção única de Stacking Cards no meio da página;
  - Uma esteira de rolagem horizontal travada (`pinned horizontal strip`);
  - Vitrine central estilo Cover Flow 3D navegando pelo portfólio.

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Quando Evitar (Anti-Padrões de Movimento)

1. **Animação Contínua de Propriedades de Layout (Reflow / Layout Thrashing)**:
   - **PROIBIÇÃO ABSOLUTA**: Jamais atrele timelines de scroll a propriedades que acionem recálculo de geometria do DOM: `width`, `height`, `top`, `left`, `margin`, `padding` ou `font-size` em elementos com muitos nós descendentes. Fazer isso forçará o navegador a reexecutar o Layout e Paint em todas as passagens da thread principal, destruindo o ganho de desempenho da Compositor Thread e gerando travamentos brutais.
   - **Solução Canônica**: Utilize exclusivamente propriedades compostas na GPU: `transform` (para escala, translação e rotação) e `opacity`. Para transições de altura perceptíveis, estruture wrappers com `position: sticky` e anime a escala interna.
2. **Filtros Gráficos Pesados em Scrubbing Contínuo no Mobile**:
   - Aplicar `filter: blur(10px)` ou `backdrop-filter` sincronizado ao scroll em dispositivos de média e baixa potência satura a taxa de preenchimento da GPU (*fillrate exhaustion*), provocando superaquecimento do aparelho e queda brusca de taxa de quadros de 60fps para menos de 25fps.
3. **Parallax Agressivo Multi-Camadas com Velocidades Desproporcionais (Cinetose)**:
   - Mover planos de fundo com velocidades inversas extremas ou profundidades falsas de grande amplitude gera **vestibular disorientation** (enjoo de movimento) em uma fração significativa de usuários, além de prejudicar gravemente a legibilidade textual.
4. **Substituição Forçada do Scroll Nativo (Scroll Hijacking)**:
   - A beleza do Scroll-Driven Animations nativo reside na preservação integral da física natural do dispositivo do usuário (aceleração balística do macOS, inércia touch do iOS/Android). Nunca combine timelines de scroll com bibliotecas destrutivas que tentam interceptar `wheel` para alterar a posição física do scrollbar de forma artificial e linearizada.

### ⚠️ Regras de Acessibilidade & GPU

1. **Respeito Irrestrito a `prefers-reduced-motion`**:
   - É obrigatório encapsular animações substanciais de movimento sob a media query de acessibilidade. Caso o usuário solicite redução de movimento, as propriedades dinâmicas devem ser desativadas ou reduzidas a simples opacidades estáticas:
   ```css
   @media (prefers-reduced-motion: reduce) {
     .card__content,
     .revealing-image,
     .pin-wrap {
       animation: none !important;
       transform: none !important;
       opacity: 1 !important;
     }
   }
   ```
2. **Progressive Enhancement com `@supports`**:
   - Nem todos os navegadores legados suportam a sintaxe nativa simultaneamente. O código deve ser sempre estruturado sob `@supports (animation-timeline: scroll())` ou `@supports (animation-timeline: view())`. Em navegadores incompatíveis, a interface deve se manter 100% legível, estática e funcional, sem conteúdo cortado ou invisível.
3. **Controle Consciente de Memória de Textura (`will-change`)**:
   - O uso de `will-change: transform` deve ser limitado estritamente aos elementos principais que sofrem rotação ou translação contínua no viewport. Aplicar `will-change` indiscriminadamente em dezenas de elementos de uma lista longa causa explosão de consumo de memória VRAM da GPU, levando o navegador a fechar a aba inesperadamente em smartphones (*crash out-of-memory*).
4. **Trade-offs do Polyfill (`scroll-timeline.js`)**:
   - Caso decida usar o polyfill mantido pela equipe de Chrome DevRel (`@flackr/scroll-timeline`), certifique-se de carregá-lo de forma assíncrona e condicional apenas nos navegadores que não reportarem suporte nativo:
   ```html
   <script>
     if (!('animationTimeline' in document.documentElement.style)) {
       const script = document.createElement('script');
       script.src = 'https://flackr.github.io/scroll-timeline/dist/scroll-timeline.js';
       document.head.appendChild(script);
     }
   </script>
   ```

---

## 4. Catálogo de Efeitos, Primitivas e Padrões de Animação

Abaixo estão detalhados **10 padrões de movimento canônicos** extraídos diretamente do laboratório oficial de Scroll-Driven Animations:

```
+---------------------------------------------------------------------------------------+
|                VIEW TIMELINE RANGES (ZONAS DE COBERTURA GEOMÉTRICA)                   |
+---------------------------------------------------------------------------------------+
|                                                                                       |
|   SCROLLPORT (Viewport do Contêiner)                                                 |
|   +-------------------------------------------------------------------------------+   |
|   | [Borda Superior / Exit Edge]                                                  |   |
|   |  ... [EXIT RANGE: Do início da saída até deixar o scrollport por completo]   ... |   |
|   |                                                                               |   |
|   |  ... [CONTAIN RANGE: Entre estar 100% visível e começar a sair do topo]    ... |   |
|   |                                                                               |   |
|   |  ... [COVER RANGE: De tocar a borda inferior até deixar a borda superior]   ... |   |
|   |                                                                               |   |
|   |  ... [ENTRY RANGE: De tocar a borda inferior até estar 100% visível]       ... |   |
|   | [Borda Inferior / Entry Edge]                                                 |   |
|   +-------------------------------------------------------------------------------+   |
|                                                                                       |
+---------------------------------------------------------------------------------------+
```

---

### 1. Reading Progress Bar (`scroll(root block)`)
- **Comportamento Visual**: Uma linha de acento de 2 a 4px de espessura afixada no topo da tela inicia com escala horizontal zero e se estende proporcionalmente à medida que a página é lida, atingindo 100% de largura no final do documento.
- **Mecanismo Técnico**: Utiliza `transform: scaleX(0)` para `scaleX(1)` com `transform-origin: 0 50%` (evitando tocar na propriedade `width` para garantir execução 100% na GPU).
- **Gatilho**: Anonymous Scroll Timeline na raiz: `animation-timeline: scroll()`.
- **Onde Aplicar**: Topo de artigos de blog, documentações técnicas, páginas de termos legais e contratos.

---

### 2. Stacking Cards Pin & Scale
- **Comportamento Visual**: Uma série de cartões dispostos em sequência vertical. Ao atingirem a linha superior de rolagem, fixam-se temporariamente na tela enquanto sofrem uma contração de escala progressiva (`scale(0.92)` e `translateY(15px)`), permitindo que o próximo cartão deslize por cima dele, criando uma sensação tátil de empilhamento de baralho.
- **Mecanismo Técnico**: Combinação de `position: sticky` no contêiner interno `.card__content` com uma `view-timeline` acoplada ao contêiner pai `#cards`. O range de cada cartão é fragmentado com base em CSS Custom Properties (`--start-range` e `--end-range`) mapeando o intervalo `exit-crossing`.
- **Gatilho**: View Progress Timeline com `animation-range: exit-crossing var(--start-range) exit-crossing var(--end-range)`.
- **Onde Aplicar**: Seções "Como Funciona", etapas de onboarding, planos de preços ou pilares de marca.

---

### 3. Horizontal Scroll Pin Section
- **Comportamento Visual**: O usuário continua rolando a página na direção vertical tradicional com a roda do mouse ou trackpad, mas a seção congela no viewport enquanto uma esteira de cartões horizontais desliza da direita para a esquerda de maneira perfeitamente sincronizada.
- **Mecanismo Técnico**: Um elemento container estendido artificialmente (ex: `height: 500vh`) com `overflow: visible`. Um filho imediato com `position: sticky; top: 0; height: 100vh; overflow-x: hidden`. Um elemento neto de largura ampla (ex: `width: 400vw`) animado por `translateX(calc(-100% + 100vw))` vinculado à timeline do container pai.
- **Gatilho**: View Progress Timeline: `animation-timeline: --section-pin-tl; animation-range: contain 0% contain 100%`.
- **Onde Aplicar**: Vitrine de recursos inovadores de produto, linha do tempo histórica de uma empresa, portfólio visual com imagens ultra-wide.

---

### 4. Apple-style 3D Cover Flow Carousel
- **Comportamento Visual**: Uma esteira horizontal de elementos (álbuns, telas de aplicativo ou cartões de produto) disposta em espaço tridimensional. Conforme o usuário rola, o item central projeta-se para a frente do observador voltado para a tela com escala 1.3x, enquanto os itens à esquerda e à direita inclinam-se em ângulos opostos de 45 graus no eixo Y.
- **Mecanismo Técnico**: Contêiner com `perspective: 50em` e `transform-style: preserve-3d`. Os elementos filhos possuem `animation-timeline: view(inline)` com `@keyframes` que operam rotações `rotateY(-45deg) -> rotateY(0deg) -> rotateY(45deg)` combinadas com `translateZ(1em)`.
- **Gatilho**: Anonymous View Timeline no eixo horizontal: `view(inline)` associado a `scroll-snap-type: x mandatory`.
- **Onde Aplicar**: Seletores de temas, prateleiras de capas de mídia, lookbooks de coleções de moda.

---

### 5. Shrinking Nav Header & Dynamic Elevation Shadow
- **Comportamento Visual**: O cabeçalho de navegação inicia espaçoso no topo da página. Ao longo dos primeiros 100 a 150px de rolagem, contrai gradualmente sua altura, reduz a dimensão do logotipo e revela suavemente uma sombra difusa de elevação (`box-shadow`), sinalizando visualmente a separação física entre o cabeçalho e o conteúdo rolado.
- **Mecanismo Técnico**: `header` com `position: fixed`. Múltiplos seletores internos associados à mesma timeline global de scroll, com um intervalo rígido de atuação: `animation-range: 0px 150px`. A animação congela no estado final (`animation-fill-mode: both`) após os 150px.
- **Gatilho**: Anonymous Scroll Timeline com corte em pixels: `animation-timeline: scroll(); animation-range: 0px 150px`.
- **Onde Aplicar**: Cabeçalho principal de qualquer website institucional moderno, portais de notícias e lojas virtuais.

---

### 6. Dynamic Scroll Overflow Shadows com `--can-scroll` (Zero JS)
- **Comportamento Visual**: Caixas com rolagem interna (como caixas de código ou tabelas) exibem uma sombra discreta no topo e na base para avisar que há texto oculto. Conforme o usuário rola até a borda, a respectiva sombra desaparece. Se a caixa tiver conteúdo curto e não for rolável, as sombras nunca aparecem.
- **Mecanismo Técnico**: Criação de pseudo-elementos `::before` e `::after` com gradientes radiais opacos. O `::before` anima a opacidade no range `1em 2em`, e o `::after` no range `calc(100% - 2em) calc(100% - 1em)`. A genialidade de Bramus: utiliza a propriedade `--can-scroll: ;` (Space Toggle) dentro de um `@keyframes` vinculado à `scroll-timeline`. Se o contêiner não tem overflow, a animação não inicializa e a variável CSS cai no valor de fallback `hidden`.
- **Gatilho**: Named Scroll Timeline em contêiner com `overflow-y: auto`.
- **Onde Aplicar**: Blocos de código syntax-highlighted, tabelas de dados em dashboards, gavetas modais com termos de uso.

---

### 7. Cinematic Curtain Image Reveal (`clip-path: inset()`)
- **Comportamento Visual**: Imagens e fotografias entram na tela como se uma cortina opaca invisível estivesse se abrindo do centro para as bordas externas, acompanhada de um suave fade de opacidade.
- **Mecanismo Técnico**: Uso da função CSS `clip-path: inset(...)`. No início (`from`), a imagem está contida em `inset(45% 20% 45% 20%)` com `opacity: 0`. No ponto final (`to`), expande-se para `inset(0% 0% 0% 0%)` com `opacity: 1`.
- **Gatilho**: View Progress Timeline com `animation-timeline: view()` e corte de entrada calibrado em `animation-range: entry 25% cover 50%`.
- **Onde Aplicar**: Seções de storytelling de estúdios de arquitetura, estúdios criativos, páginas de fotografia e apresentações de hardware.

---

### 8. Faux Scroll-Triggered Animation via Container Style Queries
- **Comportamento Visual**: Um elemento que se anima de forma clássica com transição temporal fluida (por exemplo, `transition: all 0.6s cubic-bezier(0.16, 1, 0.3, 1)`), mas cujo gatilho de disparo é a sua primeira entrada no viewport, sem desanimar ao rolar de volta para cima.
- **Mecanismo Técnico**: A especificação de Scroll-Driven Animations foi desenhada para *scrubbing* contínuo (vai e volta com a rolagem). No entanto, combinando um `@keyframes flipthebit` que comuta uma variável CSS `--bit: 1;` com CSS Container Style Queries (`@container style(--bit: 1)`), o elemento pai altera permanentemente o token de estilo no momento da intersecção, disparando uma `transition` puramente temporal via CSS nativo sem uma única linha de `IntersectionObserver`.
- **Gatilho**: `animation-timeline: view()` disparando a virada de bit com `animation-fill-mode: forwards`.
- **Onde Aplicar**: Cards de depoimentos, selos de certificação, estatísticas que precisam de animação única ao entrar na tela.

---

### 9. Reverse-Scrolling Multi-Column Parallax
- **Comportamento Visual**: Um layout em 3 colunas onde a coluna central acompanha a rolagem descendente natural, enquanto as colunas laterais deslizam na direção contrária (ascendente), criando uma dinâmica cinematográfica de galeria caleidoscópica.
- **Mecanismo Técnico**: As colunas laterais recebem `@keyframes` com `transform: translateY(0)` para `transform: translateY(-50%)` ou valores calculados em `calc()`, acoplados à `scroll-timeline` global do documento.
- **Gatilho**: Anonymous Scroll Timeline na raiz: `animation-timeline: scroll()`.
- **Onde Aplicar**: Galerias de pôsteres, vitrines de agências de publicidade e páginas de eventos culturais.

---

### 10. Cross-Component Timeline Scope Binding (`timeline-scope`)
- **Comportamento Visual**: Um menu de navegação flutuante externo ou indicador de etapas localizado fora do carrossel principal sincroniza rigorosamente seu estado visual com a posição de rolagem de um contêiner irmão distante na árvore DOM.
- **Mecanismo Técnico**: O contêiner de rolagem declara um nome via `scroll-timeline-name: --my-scroller-tl`. O ancestral comum declara `timeline-scope: --my-scroller-tl;`. O elemento de controle externo conecta-se declarando `animation-timeline: --my-scroller-tl;`.
- **Gatilho**: Named Scroll Timeline com escopo expandido para ancestrais comuns.
- **Onde Aplicar**: Carrosséis complexos com indicadores externos de paginação, sliders de comparação de imagens antes/depois.

---

## 5. Matemática do Movimento & Receitas de Código

### A Matemática das Timeline Ranges:

Para dominar o Scroll-Driven Animations nativo, é indispensável compreender a álgebra das 4 zonas geométricas e seus pontos de corte no scrollport:

```
[Distância total da zona COVER] = Altura do Scrollport + Altura do Elemento
[Distância total da zona CONTAIN] = Altura do Scrollport - Altura do Elemento (se elemento < scrollport)
[Distância total da zona ENTRY] = Altura do Elemento
[Distância total da zona EXIT] = Altura do Elemento
```

- **Curvas de Interpolação**: Em animações tradicionais baseadas em tempo, a curva padrão é `ease` ou `cubic-bezier`. Em animações scroll-driven, a propriedade `animation-timing-function` aplicada à regra `@keyframes` dita **como o progresso da interpolação varia em relação à porcentagem linear do scroll**. Utilizar `linear` cria um espelhamento direto 1:1 com o deslocamento do mouse/dedo. Utilizar uma curva como `cubic-bezier(0.25, 1, 0.5, 1)` no `@keyframes` faz com que a animação acelere rapidamente no início da rolagem daquela zona e desacelere suavemente ao final, permitindo amortecimentos sofisticados puramente em CSS.

---

### Receita 1: Padrão Completo de Stacking Cards & Header Contraction (CSS Puro)

Esta receita demonstra a arquitetura de produção do efeito Stacking Cards com cabeçalho que se contrai e projeta sombra, 100% livre de JavaScript:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Scroll-Driven Architecture: Stacking Cards & Header</title>
  <style>
    /* -------------------------------------------------------------
       1. TOKENS E CONFIGURAÇÃO ESTRUTURAL
       ------------------------------------------------------------- */
    :root {
      --bg-canvas: #09090b;
      --bg-card: #18181b;
      --border-card: #27272a;
      --accent: #6366f1;
      --text-main: #fafafa;
      --text-muted: #a1a1aa;
      --card-height: 480px;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      background-color: var(--bg-canvas);
      color: var(--text-main);
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
      overflow-x: hidden;
      line-height: 1.5;
    }

    /* -------------------------------------------------------------
       2. CABEÇALHO REATIVO AO SCROLL (HEADER SHRINK + SHADOW)
       ------------------------------------------------------------- */
    @keyframes shrink-header {
      to {
        height: 60px;
        background-color: rgba(9, 9, 11, 0.85);
        backdrop-filter: blur(12px);
        box-shadow: 0 10px 30px -10px rgba(0, 0, 0, 0.8);
        border-bottom: 1px solid var(--border-card);
      }
    }

    @keyframes scale-logo {
      to {
        transform: scale(0.85);
      }
    }

    header.site-header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 96px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 2rem;
      z-index: 100;
      transform-origin: center top;
      /* Conecta à timeline anônima do documento com range de 0 a 120px */
      animation: shrink-header linear both;
      animation-timeline: scroll();
      animation-range: 0px 120px;
    }

    .site-header .logo {
      font-size: 1.25rem;
      font-weight: 700;
      letter-spacing: -0.03em;
      transform-origin: left center;
      animation: scale-logo linear both;
      animation-timeline: scroll();
      animation-range: 0px 120px;
    }

    /* Barra de progresso de leitura embutida no cabeçalho */
    @keyframes reading-progress {
      from { transform: scaleX(0); }
      to { transform: scaleX(1); }
    }

    .reading-bar {
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 2px;
      background: var(--accent);
      transform-origin: 0 50%;
      animation: reading-progress linear both;
      animation-timeline: scroll(root block);
    }

    /* Espaçamento para o conteúdo não nascer sob o header fixo */
    main {
      padding-top: 140px;
      max-width: 900px;
      margin: 0 auto;
      padding-bottom: 200px;
    }

    .hero {
      padding: 4rem 1rem;
      text-align: center;
    }

    .hero h1 {
      font-size: 3rem;
      letter-spacing: -0.04em;
      margin-bottom: 1rem;
    }

    /* -------------------------------------------------------------
       3. STACKING CARDS (ALGORITMO DE EMPILHAMENTO TÁTIL)
       ------------------------------------------------------------- */
    #cards-list {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 2rem;
      --numcards: 4;
      view-timeline-name: --cards-timeline;
      view-timeline-axis: block;
    }

    .card-item {
      position: relative;
    }

    /* Cálculo das variáveis de índice inverso para escala matemática */
    .card-item:nth-child(1) { --index: 1; }
    .card-item:nth-child(2) { --index: 2; }
    .card-item:nth-child(3) { --index: 3; }
    .card-item:nth-child(4) { --index: 4; }

    .card-item {
      --index0: calc(var(--index) - 1);
      --reverse-index: calc(var(--numcards) - var(--index0));
    }

    /* Animação que comprime a escala do cartão quando o próximo o atinge */
    @keyframes stack-scale {
      to {
        transform: scale(calc(1.05 - calc(0.05 * var(--reverse-index))));
        filter: brightness(0.7);
      }
    }

    .card-surface {
      position: sticky;
      top: 100px; /* Alinhamento logo abaixo do header contraído */
      height: var(--card-height);
      background-color: var(--bg-card);
      border: 1px solid var(--border-card);
      border-radius: 24px;
      padding: 3rem;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      transform-origin: 50% 0%;
      box-shadow: 0 20px 40px -15px rgba(0, 0, 0, 0.7);
      will-change: transform;

      /* Mapeia a animação na timeline do container pai */
      --start-range: calc(var(--index0) / var(--numcards) * 100%);
      --end-range: calc(var(--index) / var(--numcards) * 100%);

      animation: stack-scale linear forwards;
      animation-timeline: --cards-timeline;
      animation-range: exit-crossing var(--start-range) exit-crossing var(--end-range);
    }

    .card-surface h3 {
      font-size: 1.75rem;
      letter-spacing: -0.02em;
    }

    .card-surface p {
      color: var(--text-muted);
      font-size: 1.1rem;
      max-width: 500px;
    }

    /* Fallback gracioso para navegadores legados */
    @supports not (animation-timeline: scroll()) {
      .card-surface {
        position: relative;
        top: 0;
      }
      header.site-header {
        border-bottom: 1px solid var(--border-card);
        background-color: rgba(9, 9, 11, 0.95);
      }
    }

    /* Respeito a utilizadores com sensibilidade a movimento */
    @media (prefers-reduced-motion: reduce) {
      .card-surface,
      header.site-header,
      .site-header .logo,
      .reading-bar {
        animation: none !important;
        transform: none !important;
      }
    }
  </style>
</head>
<body>

  <header class="site-header">
    <div class="logo">Kinetic.Engine</div>
    <div class="reading-bar"></div>
  </header>

  <main>
    <section class="hero">
      <h1>Arquitetura de Alta Densidade</h1>
      <p>Demonstração pura de Scroll-Driven Animations rodando 100% na GPU.</p>
    </section>

    <ul id="cards-list">
      <li class="card-item">
        <div class="card-surface">
          <div>
            <span>01 / ESTRUTURA</span>
            <h3>Compositor Thread Execution</h3>
          </div>
          <p>O scroll físico nunca é bloqueado por execuções síncronas de JavaScript. A rolagem permanece a 120Hz sob qualquer carga da main thread.</p>
        </div>
      </li>
      <li class="card-item">
        <div class="card-surface">
          <div>
            <span>02 / FLUIDEZ</span>
            <h3>Zero Layout Thrashing</h3>
          </div>
          <p>Todas as interpolações afetam matrizes de transformação de GPU e opacidades, sem tocar na árvore de Layout do navegador.</p>
        </div>
      </li>
      <li class="card-item">
        <div class="card-surface">
          <div>
            <span>03 / PERFORMANCE</span>
            <h3>0 KB de Sobrecarga de Bundle</h3>
          </div>
          <p>Elimina completamente a necessidade de carregar bibliotecas de dezenas de kilobytes de scroll trigger para efeitos nativos de viewport.</p>
        </div>
      </li>
      <li class="card-item">
        <div class="card-surface">
          <div>
            <span>04 / ACESSIBILIDADE</span>
            <h3>Integração Nativa OS</h3>
          </div>
          <p>Respeita nativamente preferências de acessibilidade e redução de movimento com desativação simplificada em CSS puro.</p>
        </div>
      </li>
    </ul>
  </main>

</body>
</html>
```

---

### Receita 2: Componente React 19 + TypeScript com Tailwind CSS e Progressive Enhancement

Esta receita implementa uma galeria de imagens cinemática em React 19 aproveitando os recursos nativos de Scroll-Driven Animations através de estilos modernos de Tailwind CSS:

```tsx
import React, { useId } from 'react';

interface ProjectCardProps {
  index: number;
  title: string;
  category: string;
  imageUrl: string;
}

export const ScrollDrivenProjectCard: React.FC<ProjectCardProps> = ({
  index,
  title,
  category,
  imageUrl,
}) => {
  const timelineId = `--project-reveal-${index}`;

  return (
    <article
      style={{
        // Define a View Timeline com nome exclusivo para este elemento
        viewTimelineName: timelineId,
        viewTimelineAxis: 'block',
      } as React.CSSProperties}
      className="relative mb-24 overflow-hidden rounded-3xl border border-zinc-800 bg-zinc-900/60 p-6 backdrop-blur-md"
    >
      <div
        style={{
          // Conecta a animação ao cruzamento deste próprio card no scrollport
          animationTimeline: timelineId,
          animationRange: 'entry 15% cover 45%',
          animationFillMode: 'both',
        } as React.CSSProperties}
        className="group animate-[project-enter_linear_both] will-change-transform"
      >
        <div className="relative aspect-[16/9] w-full overflow-hidden rounded-2xl bg-zinc-950">
          <img
            src={imageUrl}
            alt={title}
            className="h-full w-full object-cover transition-transform duration-700 ease-out group-hover:scale-105"
            loading="lazy"
          />
          <div className="absolute inset-0 bg-gradient-to-t from-zinc-950/80 via-transparent to-transparent" />
        </div>

        <div className="mt-6 flex items-baseline justify-between">
          <div>
            <span className="text-xs font-semibold tracking-wider text-indigo-400 uppercase">
              {category}
            </span>
            <h3 className="mt-1 text-2xl font-bold tracking-tight text-white">
              {title}
            </h3>
          </div>
          <span className="font-mono text-sm text-zinc-500">
            [0{index + 1}]
          </span>
        </div>
      </div>
    </article>
  );
};

// Keyframes injetados ou adicionados ao Tailwind CSS config / globals.css:
/*
@keyframes project-enter {
  from {
    opacity: 0;
    transform: translateY(60px) scale(0.94);
    clip-path: inset(10% 5% 10% 5% round 24px);
  }
  to {
    opacity: 1;
    transform: translateY(0px) scale(1);
    clip-path: inset(0% 0% 0% 0% round 24px);
  }
}
*/
```

---

### Receita 3: Implementação Programática via Web Animations API (WAAPI Modern JS)

Quando a interface necessita de controle dinâmico via código (por exemplo, conectar modelos Three.js, Canvas WebGL ou sincronizar elementos instanciados em tempo de execução), a especificação disponibiliza as interfaces JavaScript nativas `ScrollTimeline` e `ViewTimeline`:

```typescript
/**
 * Inicializa scrubbing off-main-thread em nós DOM arbitrários via WAAPI nativa
 */
export function initScrollDrivenHero(element: HTMLElement, scrollContainer?: HTMLElement): Animation {
  // 1. Cria a timeline associada ao contêiner de rolagem
  const scrollTimeline = new ScrollTimeline({
    source: scrollContainer || document.documentElement,
    axis: 'block',
  });

  // 2. Cria a animação declarativa vinculada à timeline de scroll
  const animation = element.animate(
    [
      {
        transform: 'translate3d(0, 0, 0) scale(1)',
        opacity: 1,
        filter: 'blur(0px)',
      },
      {
        transform: 'translate3d(0, -150px, 0) scale(0.92)',
        opacity: 0.2,
        filter: 'blur(8px)',
      },
    ],
    {
      // Passa a timeline nativa como motor temporal
      timeline: scrollTimeline,
      fill: 'both',
      // Define a zona exata de início e término em pixels de scroll
      rangeStart: new CSSNumericValue ? CSS.px(0) : '0px',
      rangeEnd: new CSSNumericValue ? CSS.px(300) : '300px',
    } as KeyframeAnimationOptions
  );

  return animation;
}

/**
 * Vincula a intersecção de um elemento à sua ViewTimeline nativa via WAAPI
 */
export function initViewProgressParallax(subjectElement: HTMLElement): Animation {
  const viewTimeline = new ViewTimeline({
    subject: subjectElement,
    axis: 'block',
    // Inset opcional para criar margens seguras na borda do scrollport
    inset: [CSS.px(0), CSS.px(0)],
  });

  const animation = subjectElement.animate(
    [
      { transform: 'translateY(100px)', opacity: 0 },
      { transform: 'translateY(0px)', opacity: 1 },
    ],
    {
      timeline: viewTimeline,
      rangeStart: 'entry 0%',
      rangeEnd: 'cover 50%',
      fill: 'both',
    } as KeyframeAnimationOptions
  );

  return animation;
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir a especificação cinemática de um novo produto ou projeto, a equipe de engenharia e a IA devem formalizar a estratégia de movimento respondendo aos seguintes pontos de controle:

### 1. Matriz de Decisão: CSS Scroll-Driven vs. Bibliotecas JS (Motion / GSAP)

| Cenário de Interface | Escolha Recomendada | Motivo Técnico Arquitetural |
| :--- | :--- | :--- |
| **Reading Progress Bar** | `CSS animation-timeline: scroll()` | Zero overhead JS; roda a 120fps mesmo durante congelamento de scripts. |
| **Stacking Cards / Sticky Overlap** | `CSS view-timeline` + `position: sticky` | Execução pura no compositor de GPU; física de inércia nativa intocada. |
| **Header Shrink + Elevation** | `CSS animation-range: 0 120px` | Previne re-renderizações no React e elimina debounce de listeners de scroll. |
| **Scroll Shadows em Caixas de Código** | CSS Scroll-Timeline + `--can-scroll` | Técnica Space Toggle com zero nós adicionais e zero watchers de resize. |
| **Smooth Scroll Customizado + Canvas 3D** | `Lenis` + `Three.js` (rAF WebGL) | Necessário quando o próprio render loop do WebGL depende do frame temporal. |
| **Animações com Interrupção Física** | `Motion` (Framer Motion) com Springs | Casos onde gestos de arrasto touch precisam soltar em molas dinâmicas. |

### 2. Checklist Técnico para Especificação no Blueprint:
- [ ] **Mapeamento de Eixos e Escopos**: Declarar explicitamente se as timelines são globais (`scroll(root block)`), anônimas locais (`view()`) ou se exigem elevação de escopo com `timeline-scope`.
- [ ] **Definição Estrita de Ranges**: Nunca deixar ranges ambíguos. Especificar sempre a zona e a porcentagem (`entry 10% cover 50%` ou `0px 150px`).
- [ ] **Garantia de Isolamento de GPU**: Confirmar que apenas `transform`, `opacity` e `clip-path` (com polígonos simples) estão sendo manipulados no `@keyframes`.
- [ ] **Cláusula de Acessibilidade Mandatória**: Incluir a regra de desativação ou simplificação sob `@media (prefers-reduced-motion: reduce)`.
- [ ] **Estratégia de Fallback Gracioso**: Declarar o estado da interface quando `@supports not (animation-timeline: scroll())` for acionado (layout estático funcional sem sobreposições indevidas).
