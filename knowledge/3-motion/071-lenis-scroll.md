---
id: "lenis-scroll"
name: "Lenis Smooth Scroll"
url: "https://lenis.darkroom.engineering/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["Native-Preserving Smooth Momentum", "Unified Kinetic Physics", "Sub-Pixel LERP Interpolation", "Hardware-Synced Scrolling", "WebGL/DOM Choreography"]
densidade_informacao: "Independente"
impacto_visual: "Sutil/Invisivel (Feel) a Cinematografico"
custo_computacional: "Baixo (JS RAF / Virtual Normalized Scroll sobre Native Window Scroll)"
stack_frameworks: ["Vanilla JS / TypeScript (lenis)", "React (lenis/react)", "Next.js (App Router / RSC)", "Vue (lenis/vue)", "Svelte", "GSAP / ScrollTrigger", "Three.js / React Three Fiber"]
compatibilidade:
  combinacoes_recomendadas: ["Lenis + GSAP ScrollTrigger", "Lenis + Three.js / R3F Canvas", "Lenis + Motion.dev", "Lenis + Tailwind CSS v4", "Lenis + Tempus RAF"]
  conflitos_esteticos: ["Propriedade CSS 'scroll-behavior: smooth' ativa concorrentemente", "Locomotive Scroll legado ou bibliotecas de fake translate3d body wrapper", "Concorrência de loops requestAnimationFrame desregulados sem sincronização de ticker", "Scroll hijacking destrutivo em formulários densos, planilhas ou UIs utilitárias corporativas"]
---

# Lenis Smooth Scroll — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)

O **Lenis** (`https://lenis.darkroom.engineering/`), concebido e arquitetado pelo engenheiro criativo **Clément Roche** e desenvolvido pela **Darkroom Engineering** (antigo **Studio Freight**), consolidou-se como o padrão definitivo e incontestável da indústria web moderna para **rolagem suave (smooth scrolling) de alta precisão**. Sua criação respondeu diretamente a uma crise de usabilidade e integridade arquitetural gerada pela geração anterior de motores de "virtual scroll", restabelecendo a harmonia entre o design cinemático de estúdio e a robustez dos padrões da W3C.

---

### A Ruptura: O Colapso do Paradigma do Locomotive Scroll e Fake Body Wrappers

Durante quase uma década, a busca pela estética de rolagem sedosa ("buttery smooth") em sites premiados pela Awwwards e FWA dependeu de bibliotecas como **Locomotive Scroll (v1-v3)** e **SmoothScrollbar**. Para emular inércia, essas ferramentas recorriam a uma técnica destrutiva conhecida como **Virtual Scroll Hijacking**:

```
┌────────────────────────────────────────────────────────────────────────┐
│             PARADIGMA LEGADO (LOCOMOTIVE SCROLL / FAKE WRAPPER)        │
└────────────────────────────────────────────────────────────────────────┘
  [window: overflow: hidden; height: 100vh]  <-- Rolagem nativa destruída
       │
       ▼ Intercepta 'wheel' / 'touchmove' via preventDefault()
  [fake-scroll-container: transform: matrix3d(1, 0, 0, ..., -yScroll)]
       │
       ├── ❌ Quebra 'position: sticky' nativo (transform cria novo contexto de formatação)
       ├── ❌ Desativa o 'IntersectionObserver' acelerado por hardware
       ├── ❌ Impede busca textual nativa do navegador (Ctrl+F / Cmd+F não rola até o nó)
       ├── ❌ Quebra leitores de tela e navegação por teclado (Tab / PageDown)
       ├── ❌ Elimina a barra de rolagem nativa do sistema operacional
       └── ❌ Causa reflows e invalidações de texturas de GPU em páginas extensas
```

Essa abordagem representava um pacto de Fausto: obtinha-se a rolagem fluida ao custo de quebrar a espinha dorsal do navegador.

#### Por Que o Lenis Substituiu o Locomotive Scroll?

O Lenis resolveu essa dicotomia através de uma virada conceitual brilhante: **abandonar o fake wrapper e operar diretamente sobre a rolagem nativa do navegador (`window.scrollTo` / Native Document Scroll)**.

```
┌────────────────────────────────────────────────────────────────────────┐
│                   PARADIGMA LENIS (NATIVE SMOOTH SCROLL)                │
└────────────────────────────────────────────────────────────────────────┘
  [window: scroll nativo preservado / DOM inalterado na raiz]
       │
       ▼ Normaliza Wheel, Trackpad, Touch & Keyboard em deltas uniformes
  [Motor Físico Lenis: Interpolação Matemática LERP / Ease-Out-Expo no RAF]
       │
       ▼ Aplica window.scrollTo({ top: target, behavior: 'auto' }) frame a frame
  [Documento Web Padrão]
       │
       ├── ✅ 'position: sticky' opera 100% nativo com aceleração por hardware
       ├── ✅ 'IntersectionObserver' dispara nos limiares geométricos corretos do viewport
       ├── ✅ Busca nativa da página (Ctrl+F) localiza termos e rola suavemente até o alvo
       ├── ✅ Total acessibilidade WCAG e suporte a leitores de tela
       ├── ✅ Barra de rolagem nativa reflete a física sem descompasso espacial
       └── ✅ Peso irrisório (~3KB min/gzip) e zero dependências externas
```

---

### A Sensação Cinestésica (Feel): Da Detecção Mecânica à Fita Analógica

A roda física de um mouse tradicional (detent mouse wheel) opera por impulsos discretos mecânicos: a cada "dente" girado, o hardware despacha um evento de rolagem que salta tipicamente 100 pixels instantâneos na tela. O resultado no navegador padrão é uma rolagem truncada, quebrada e com solavancos visuais desagradáveis.

O Lenis atua como um **conversor analógico-digital de amortecimento**:
1. **Normalização Multi-Hardware**: Converte impulsos de rodas dentadas mecânicas de mouses de mesa, gestos contínuos de trackpads de laptops e eventos de toque móvel em uma grandeza vetorial unificada.
2. **Eliminação do Atrito Degrau a Degrau**: Transforma o avanço fragmentado em um vetor contínuo de energia cinética com dissipação exponencial suave, transmitindo a sensação sensorial de deslizar sobre uma película de óleo ou fita analógica de cinema.
3. **Consistência Cross-Platform**: Garante que um usuário no Windows/Linux com mouse genérico de 3 botões experimente a mesma elegância fluida de um usuário no macOS com Magic Trackpad de alta precisão.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Interface e Casos de Uso Críticos

1. **Websites Institucionais e Editoriais de Luxo (Storytelling & Scrollytelling)**:
   Projetos com tipografia editorial marcante, fotografias em alta resolução e transições narrativas onde a velocidade e o ritmo de leitura devem transmitir sofisticação, calma e controle absoluto.
2. **Sincronização Perfeita de Câmeras 3D e Shaders WebGL com o DOM**:
   Ambientes híbridos (onde um `<canvas>` Three.js / R3F roda em tela cheia sob elementos HTML). Como o Lenis normaliza o scroll e expõe o progresso linear no mesmo loop de animação (`requestAnimationFrame`), o mundo 3D e os textos HTML movem-se com sincronia atômica, eliminando por completo o efeito de "tearing", jitter ou descolamento de planos.
3. **Coreografias Cinemáticas com GSAP ScrollTrigger**:
   Timelines complexas de GSAP que utilizam `scrub: true`, seções fixadas via `pin: true` e desdobramentos de layout acoplados ao deslocamento vertical. O Lenis provê um fluxo contínuo de dados sub-pixel, tornando o scrub do GSAP infinitamente mais responsivo e livre de micro-travamentos.
4. **Sistemas de Parallax Multicamadas**:
   Páginas onde diferentes camadas visuais (background, texto, foreground flutuante) movem-se a diferentes velocidades relativas. O cálculo contínuo de sub-pixels do Lenis elimina a trepidação típica do scroll nativo em monitores de alta taxa de atualização (120Hz a 240Hz).
5. **Navegação Intra-Página Suave para Âncoras com Offset**:
   Páginas longas (como termos de serviço, manuais de produto, documentações e landing pages) que dependem de links de sumário. A API `lenis.scrollTo(target, { offset: -80, duration: 1.5 })` executa transições curvas impecáveis com compensação exata para barras de navegação fixas.

---

### O Papel do Lenis na Regra 60-30-10

Na engenharia visual de produtos digitais, o movimento deve obedecer a uma distribuição harmônica para não cansar o usuário:

```
┌────────────────────────────────────────────────────────────────────────┐
│                   A REGRA 60-30-10 DO MOVIMENTO & DESIGN               │
└────────────────────────────────────────────────────────────────────────┘
  60% — ESTRUTURA ESTÁTICA & TIPOGRAFIA (A BASE)
  Espaçamento, grids, contrastes funcionais, hierarquia visual e conteúdo.
       │
  30% — A GRAXA CINÉTICA INVISÍVEL (O LENIS)
  Fluidez de rolagem inercial, resposta elástica nos inputs e continuidade
  espacial. O usuário não deve notar conscientemente "olhe, há um efeito aqui",
  mas sim perceber que o site responde como um material nobre e coeso.
       │
  10% — O ESPETÁCULO VISUAL / SHOWSTOPPER (O CLÍMAX)
  Distorções de shaders GLSL acionadas por velocidade, morphing de malhas 3D,
  explosões tipográficas e pin-scrolls dramáticos acoplados ao Lenis.
```

O Lenis reside nos **30% funcionais**: ele é a graxa que viabiliza os 10% de espetáculo sem degradar os 60% de legibilidade fundamental.

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Quando Evitar Absolutamente

1. **Aplicações de Alta Densidade de Dados & Painéis Transacionais (B2B SaaS / ERP)**:
   Em dashboards financeiros, ferramentas de análise contábil, plataformas de trading ou interfaces semelhantes ao Excel/Airtable, o usuário busca velocidade utilitária imediata. Interpor uma inércia de 1.2 segundos entre a intenção mecânica e o deslocamento da linha de dados gera sensação imediata de atraso ("lag artificial") e fadiga cognitiva.
2. **Interfaces Densas em Formulários Extensos com Auto-Tabulação**:
   Páginas com múltiplos inputs de texto onde o usuário pressiona `Tab` sucessivas vezes. Se o Lenis tentar suavizar cada deslocamento de foco, pode haver desencontro entre o cursor piscante e a área visível da tela.
3. **Dispositivos Móveis sem Calibração Precisa (`syncTouch`)**:
   Sistemas operacionais móveis modernos (especialmente iOS com Safari e Android com Chrome) possuem algoritmos proprietários de aceleração inercial e bounce elástico de toque integrados diretamente ao hardware a 120Hz (ProMotion). Forçar smooth scroll via JavaScript sobre o gesto de arrastar o polegar (`syncTouch: true`) com parâmetros incorretos pode destruir a sensação nativa do smartphone, gerando rejeição motora imediata.
   - *Regra de Ouro*: Mantenha `syncTouch: false` na maioria dos projetos mobile, preservando o scroll nativo de toque e ativando a suavização do Lenis prioritariamente para eventos de roda (`wheel`).

---

### ⚠️ Regras Rígidas de Acessibilidade, GPU e Anti-Padrões Técnicos

#### 1. Respeito Obrigatório a `prefers-reduced-motion`
Usuários com distúrbios vestibulares sofrem de náuseas graves, vertigem e enjoo visual quando a página continua rolando de forma desacelerada após a interrupção do gesto físico. O Lenis **deve** ser destruído ou colocado em modo instantâneo quando o sistema operacional indicar preferência por movimento reduzido:

```javascript
const prefersReducedMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;

const lenis = new Lenis({
  lerp: prefersReducedMotion ? 1.0 : 0.1, // 1.0 = scroll instantâneo (sem LERP)
  duration: prefersReducedMotion ? 0 : 1.2,
  syncTouch: false,
});
```

#### 2. O Anti-Padrão Fatal do CSS `scroll-behavior: smooth`
Nunca mantenha `html { scroll-behavior: smooth; }` ativo no CSS global enquanto o Lenis estiver instanciado. O navegador tentará aplicar sua própria interpolação nativa sobre as coordenadas já interpoladas pelo Lenis a cada frame de `scrollTo`, resultando em uma oscilação catastrófica de trepidação visual (combate de motores). A folha de estilos base do Lenis desativa isso expressamente:

```css
.lenis.lenis-smooth {
  scroll-behavior: auto !important;
}
```

#### 3. Isolamento Obrigatório de Containers Internos (`data-lenis-prevent`)
Se a sua página contiver um elemento com overflow próprio (como um modal de rolagem interna, uma gaveta de checkout, uma caixa de código Markdown ou um dropdown longo), a rotação do mouse dentro dele tentará rolar a página inteira (scroll chaining desastroso). Adicione sempre o atributo demarcador:

```html
<div class="modal-dialog-body" data-lenis-prevent>
  <!-- Rolagem nativa isolada; o Lenis suspende o controle neste nó descendente -->
</div>
```

---

## 4. Catálogo de Efeitos, Primitivas e Padrões de Animação

Abaixo estão detalhados **10 padrões de movimento e arquiteturas de interação** fundamentadas ou potencializadas pelo motor do Lenis:

---

### 1. Parallax Multicamadas Sub-Pixel com Zero Jitter
- **Comportamento Visual**: Três camadas de profundidade espacial deslocam-se verticalmente a razões proporcionais distintas ($\Delta y \times 0.15$ para o horizonte distante, $\Delta y \times 0.5$ para o cenário intermediário, $\Delta y \times 1.0$ para a tipografia e $\Delta y \times 1.35$ para fragmentos suspensos no primeiro plano). Ao parar a rolagem, a inércia faz as camadas acomodarem-se de forma assintótica e sincronizada.
- **Anatomia Técnica**:
  - `lenis.on('scroll', ({ scroll }) => { ... })`
  - Aplicação de `transform: translate3d(0, ${scroll * factor}px, 0)` em elementos acelerados via GPU (`will-change: transform`).
- **Gatilho**: Evento de progresso contínuo de rolagem do Lenis.
- **Onde Encaixar**: Seções Hero de landing pages conceituais, visualizadores de arquitetura e capas de matérias de jornalismo visual.

---

### 2. Pinned Horizontal Section (Scroll Vertical Convertido em Rolagem Lateral)
- **Comportamento Visual**: Conforme o usuário rola a roda vertical do mouse, o documento trava a descida vertical na viewport e desliza uma fileira horizontal de cartões ou imagens em alta resolução do extremo direito até o esquerdo. Uma vez percorrida a largura total da galeria, a descida vertical do documento é destravada organicamente.
- **Anatomia Técnica**:
  - Container mestre com altura expandida (ex: `height: 400vh`).
  - Container interno fixo via `position: sticky; top: 0; width: 100vw; height: 100vh; overflow: hidden;`.
  - Trilho interno com `display: flex; width: max-content;` recebendo `transform: translate3d(-${progress * maxScroll}px, 0, 0)`.
- **Gatilho**: Interpolação contínua da faixa de interseção do scroll vertical.
- **Onde Encaixar**: Galerias de portfólio de projetos, linha do tempo corporativa, catálogo de produtos em e-commerce de moda.

---

### 3. Deformação de Malhas 3D por Inércia de Scroll (Velocity Mesh Shearing)
- **Comportamento Visual**: Conforme o usuário acelera a rolagem, os modelos tridimensionais ou imagens renderizadas em um canvas WebGL/Three.js flexionam-se suavemente como borracha ou tecido sob vento (distorção em arco). Quando a rolagem atinge repouso, a geometria volta ao seu estado plano perfeitamente tensionado.
- **Anatomia Técnica**:
  - Leitura contínua de `lenis.velocity` (vetor instantâneo de velocidade em pixels/ms).
  - Injeção da velocidade normalizada em um uniform de shader GLSL: `material.uniforms.uVelocity.value = THREE.MathUtils.lerp(material.uniforms.uVelocity.value, lenis.velocity * 0.005, 0.1)`.
  - No Vertex Shader: `vPosition.y += sin(uv.x * 3.14159) * uVelocity * 0.5`.
- **Gatilho**: Magnitude escalar do vetor instantâneo de velocidade do Lenis.
- **Onde Encaixar**: Imagens de produtos de calçados/moda, banners conceituais interativos e websites da indústria do entretenimento.

---

### 4. Skew Tipográfico Dinâmico na Interface (Kinetic Shear Effect)
- **Comportamento Visual**: Títulos em fontes pesadas (display serif ou grotesque condensada) sofrem uma inclinação angular sutil em seus eixos horizontais proporcional à velocidade do usuário (`transform: skewY(v * 0.04deg)`). A inclinação transmite a sensação de que as letras possuem massa física e resistem à aceleração da página.
- **Anatomia Técnica**:
  - Atualização no callback de scroll: `const skew = Math.min(Math.max(lenis.velocity * 0.05, -7), 7)`.
  - Elemento estilizado com `transform: skewY(${skew}deg)` e interpolação de amortecimento via mola ou LERP secundário para evitar oscilações de alta frequência.
- **Gatilho**: Leitura direta de `lenis.velocity`.
- **Onde Encaixar**: Títulos de agências de publicidade, páginas de manifestos de marca e catálogos tipográficos.

---

### 5. Sticky Overlapping Stacking Cards (Empilhamento Macio de Cartões)
- **Comportamento Visual**: Uma série de cartões em tela cheia sobe sucessivamente. Cada cartão ancora no topo da viewport via `position: sticky; top: 80px;`, enquanto o cartão seguinte desliza por cima dele cobrindo-o suavemente, com uma leve redução de escala no cartão anterior (`scale: 1 -> 0.95`).
- **Anatomia Técnica**:
  - Estrutura CSS pura com nós filhos contendo `position: sticky; top: calc(60px + ${index * 20}px);`.
  - Como o Lenis preserva a árvore nativa de scroll do navegador, o motor de composição nativo calcula o clipping e o empilhamento sem qualquer polyfill pesado ou atraso de sincronização.
- **Gatilho**: Limiares naturais de `position: sticky` transitados pelo scroll interpolado.
- **Onde Encaixar**: Apresentação de pilares de valor de uma empresa, tabela de planos/preços ou etapas de um processo metodológico.

---

### 6. In-Page Smooth Anchor Scrubbing com Offset Dinâmico
- **Comportamento Visual**: Ao clicar em itens de um sumário ou botão "Explorar Funcionalidades", a tela desliza com uma curva sigmóide ultrassuave até o destino, desacelerando com precisão milimétrica exatamente 96 pixels antes do título, compensando o menu de navegação flutuante.
- **Anatomia Técnica**:
  - Invocação de método de primeira classe:
    ```javascript
    lenis.scrollTo('#secao-destaque', {
      offset: -96,
      duration: 1.4,
      easing: (t) => Math.min(1, 1.001 - Math.pow(2, -10 * t)),
      lock: false,
    });
    ```
- **Gatilho**: Evento de clique do usuário (`onClick`) em elementos com links internos.
- **Onde Encaixar**: Sumários de whitepapers técnicos, navegação de páginas de produto longas (Landing Pages).

---

### 7. Isolamento de Scroll com Prevenção de Chaining (`data-lenis-prevent`)
- **Comportamento Visual**: Dentro de um painel lateral de comentários, gaveta de carrinho de compras ou caixa de snippet de código, o usuário rola o conteúdo interno até o final. Ao atingir o topo ou a base do elemento, a página mestra atrás permanece perfeitamente estática, sem que o scroll salte repentinamente para o documento global.
- **Anatomia Técnica**:
  - Elemento HTML decorado com `data-lenis-prevent="true"`.
  - No CSS: `overscroll-behavior: contain`.
  - O motor do Lenis intercepta a árvore de propagação (`e.composedPath()`) e interrompe sua própria cadeia de acumulação de delta quando um ancestral contém o atributo demarcador.
- **Gatilho**: Eventos de `wheel` e `touchmove` originados dentro da caixa delimitada.
- **Onde Encaixar**: Modais de termos e condições, blocos de código com syntax highlighting, drawers de checkout.

---

### 8. Kinetic Reveal de Tipografia com Scrubbing Contínuo
- **Comportamento Visual**: Grandes frases editoriais permanecem semi-transparentes (`opacity: 0.2`) e, conforme o scroll avança, cada palavra ou linha acende gradualmente para branco sólido (`opacity: 1.0`) e desloca-se 20 pixels para cima, acompanhando o polegar ou a roda do mouse com precisão cirúrgica.
- **Anatomia Técnica**:
  - Integração simbiótica: Lenis + GSAP ScrollTrigger.
  - Sincronização via `gsap.ticker.add((time) => lenis.raf(time * 1000))` permitindo que o GSAP calcule `scrub: 0.5` sem trepidações.
- **Gatilho**: Progresso fracionário ($0.0 \to 1.0$) do ScrollTrigger do elemento.
- **Onde Encaixar**: Declarações de missão corporativa, introduções de artigos e seções de citação editorial.

---

### 9. Infinite Circular Scroll Loop (Carrossel Infinito na Janela)
- **Comportamento Visual**: O usuário pode rolar a página para baixo indefinidamente; após o último item, a interface transiciona sem corte para o primeiro elemento, criando a ilusão espacial de um tambor cilíndrico infinito.
- **Anatomia Técnica**:
  - Configuração da primitiva: `new Lenis({ infinite: true })`.
  - Duplicação lógica do conteúdo no DOM. Quando o scroll atinge o valor de `limit`, o Lenis calcula o módulo da posição: $scroll = scroll \pmod{contentHeight}$, reposicionando as coordenadas virtuais instantaneamente sem disparo de layout shift perceptível.
- **Gatilho**: Ultrapassagem da fronteira máxima/mínima de scroll do documento.
- **Onde Encaixar**: Lookbooks experimentais de moda, galerias conceituais e sites de festivais de design.

---

### 10. Global Scroll Freeze & Restore para Menus Fullscreen
- **Comportamento Visual**: Ao abrir um menu de navegação que cobre toda a tela, o scroll do documento de fundo é paralisado instantaneamente. Diferente do clássico `body { overflow: hidden; }` que faz a barra de rolagem sumir e gera um solavanco de 15 pixels na largura da tela (layout shift), a interface mantém a barra visível e a posição exata de leitura intacta. Ao fechar o menu, a navegação é restaurada sem qualquer salto.
- **Anatomia Técnica**:
  - Invocação de métodos de estado: `lenis.stop()` na abertura e `lenis.start()` no fechamento.
  - O Lenis adiciona internamente a classe CSS `.lenis-stopped` e bloqueia a aceitação de novos eventos de wheel sem resetar o offset acumulado.
- **Gatilho**: Evento de toggle do menu de navegação ou abertura de caixas de diálogo modais.
- **Onde Encaixar**: Menus hamburguer imersivos, painéis de busca global (Command Palette) e lightboxes de mídia.

---

## 5. Matemática do Movimento & Receitas de Código

### A Mecânica Matemática do Lenis: LERP vs Easing Temporal

O Lenis suporta dois modos operacionais matemáticos mutuamente exclusivos:

#### 1. Modo Linear Interpolation (LERP) — Baseado em Taxa de Quadros
No modo `lerp: α` (onde $0 < \alpha \le 1$):
A cada quadro da animação disparado pelo `requestAnimationFrame`, a posição atual de rolagem ($y_t$) converge em direção à posição alvo ($y_{\text{target}}$) pela fração $\alpha$:

$$y_t = y_{t-1} + (y_{\text{target}} - y_{t-1}) \cdot \alpha$$

- **Valor Padrão**: `lerp: 0.1` (produz uma sensação aveludada clássica de estúdio).
- **Valores Menores (`0.04` - `0.07`)**: Criam um efeito pesado, espacial e cinemático (sensação de deslocamento subaquático).
- **Valores Maiores (`0.15` - `0.25`)**: Geram uma sensação ágil e imediata, ideal para sites comerciais e blogs de tecnologia.

*Compensação de Taxa de Quadros (Frame-rate Independence)*: Em telas de 60Hz, 120Hz ou 240Hz, um LERP ingênuo moveria a tela em velocidades físicas distintas. O Lenis ajusta internamente a interpolação com base no delta de tempo decorrido ($\Delta t$) em milissegundos:

$$\alpha_{\text{adjusted}} = 1 - (1 - \alpha)^{(\Delta t / 16.666)}$$

Isso garante que a sensação inercial seja milimetricamente idêntica em qualquer monitor do mundo.

---

#### 2. Modo Duração com Função de Easing — Baseado em Tempo
Se a propriedade `lerp` for omitida da configuração, o Lenis ativa o cálculo baseado em tempo fechado definido por `duration` (segundos) e uma função de curva matemática `easing(t)` (onde $0 \le t \le 1$).

A curva padrão adotada pela Darkroom Engineering para simular o atrito e a desaceleração natural do mundo físico é a **Exponencial Suave (Ease-Out-Expo)**:

$$f(t) = \min\left(1, \; 1.001 - 2^{-10t}\right)$$

```
f(t)
 1.0 ┌──────────────────────────────────────────────────
     │                                     . · · ¯ ¯ ¯
 0.8 │                               . · ¯
     │                          . · ¯
 0.6 │                      . · ¯
     │                  . · ¯
 0.4 │              . · ¯
     │          . · ¯
 0.2 │      . · ¯
     │  . · ¯
 0.0 └─────────────────────────────────────────────────── t
     0.0        0.2        0.4        0.6        0.8   1.0
```

---

### Dicionário Exaustivo de Parâmetros de Configuração

| Parâmetro | Tipo | Padrão | Descrição & Impacto na Interface |
| :--- | :--- | :--- | :--- |
| `lerp` | `number` | `0.1` | Coeficiente de interpolação linear ($0$ a $1$). Se definido, ignora `duration` e `easing`. |
| `duration` | `number` | `1.2` | Duração temporal em segundos para a animação do scroll convergir ao repouso. |
| `easing` | `function` | *EaseOutExpo* | Função matemática de interpolação que mapeia o tempo decorrido ($0 \to 1$) no progresso. |
| `orientation` | `'vertical' \| 'horizontal'` | `'vertical'` | Orientação mestre da rolagem do documento. |
| `gestureOrientation` | `'vertical' \| 'horizontal' \| 'both'` | `'vertical'` | Orientação do gesto físico que é mapeado no scroll (permite mapear rolagem horizontal do mouse para scroll vertical). |
| `wheelMultiplier` | `number` | `1.0` | Multiplicador de escala aplicado aos deltas da roda mecânica do mouse (aumente para $1.2$ - $1.4$ se desejar um avanço mais rápido por rotação). |
| `touchMultiplier` | `number` | `1.5` | Multiplicador aplicado aos gestos de arrasto por toque. |
| `syncTouch` | `boolean` | `false` | Se `true`, força a interpolação suave do Lenis sobre gestos de toque no mobile. Se `false`, preserva a inércia nativa do SO. |
| `syncTouchLerp` | `number` | `0.075` | Valor específico de LERP aplicado exclusivamente a gestos de toque quando `syncTouch: true`. |
| `infinite` | `boolean` | `false` | Se `true`, cria um loop de rolagem contínua infinita sem limites de topo e base. |
| `autoRaf` | `boolean` | `true` | Se `true`, o Lenis inicia seu próprio loop interno de `requestAnimationFrame`. **Deve ser `false` quando sincronizado com o GSAP Ticker.** |
| `smoothWheel` | `boolean` | `true` | Se `true`, aplica a suavização aos eventos de roda mecânica. |

---

### Receitas de Código de Alta Fidelidade

#### Receita 1: Setup Universal com Vanilla JS + GSAP ScrollTrigger + CSS Foundation

Esta é a arquitetura canônica e inviolável recomendada pela Darkroom Engineering para garantir que GSAP e Lenis nunca compitam pela taxa de quadros da GPU:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Lenis + GSAP ScrollTrigger Architecture</title>
  
  <!-- CSS Base Obrigatório do Lenis -->
  <style>
    /* 1. Evita conflitos de altura e reseta behaviors concorrentes */
    html.lenis, html.lenis body {
      height: auto;
    }

    /* 2. Desativa categoricamente o smooth nativo do CSS */
    .lenis.lenis-smooth {
      scroll-behavior: auto !important;
    }

    /* 3. Garante que elementos de rolagem interna não sofram scroll chaining */
    .lenis.lenis-smooth [data-lenis-prevent] {
      overscroll-behavior: contain;
    }

    /* 4. Estado de congelamento total de rolagem (ex: menus modais) */
    .lenis.lenis-stopped {
      overflow: hidden;
    }

    /* 5. Previne perda de frames em mousemove sobre iframes durante o scroll */
    .lenis.lenis-smooth iframe {
      pointer-events: none;
    }
  </style>
</head>
<body>
  <main class="page-content">
    <section class="h-screen flex items-center justify-center">
      <h1 class="text-6xl font-bold">Lenis + ScrollTrigger Synchronized</h1>
    </section>
    
    <!-- Container interno com scroll independente isolado -->
    <div class="code-box h-64 overflow-y-auto" data-lenis-prevent>
      <pre><code>// O scroll aqui dentro não move a página de fundo!</code></pre>
    </div>
  </main>

  <script type="module">
    import Lenis from 'https://cdn.jsdelivr.net/npm/lenis@1.1.18/+esm';
    import { gsap } from 'https://cdn.jsdelivr.net/npm/gsap@3.12.5/+esm';
    import { ScrollTrigger } from 'https://cdn.jsdelivr.net/npm/gsap@3.12.5/ScrollTrigger/+esm';

    // 1. Registra os plugins do GSAP
    gsap.registerPlugin(ScrollTrigger);

    // 2. Instancia o Lenis com autoRaf DESLIGADO (GSAP assumirá o loop)
    const lenis = new Lenis({
      autoRaf: false,           // GSAP Ticker dirigirá a execução
      lerp: 0.1,                // Coeficiente de suavização
      wheelMultiplier: 1.0,     // Sensibilidade padrão da roda
      syncTouch: false,         // Preserva a aceleração de toque nativa do iOS/Android
    });

    // 3. Atualiza o ScrollTrigger a cada evento de rolagem emitido pelo Lenis
    lenis.on('scroll', (e) => {
      ScrollTrigger.update();
    });

    // 4. Conecta o RAF do Lenis ao loop centralizado do GSAP Ticker
    // GSAP passa 'time' em segundos; o Lenis exige milissegundos (* 1000)
    gsap.ticker.add((time) => {
      lenis.raf(time * 1000);
    });

    // 5. Desativa o lagSmoothing do GSAP para evitar saltos visuais após tabs inativas
    gsap.ticker.lagSmoothing(0);

    // Exemplo de Animação com GSAP ScrollTrigger perfeitamente sincronizada
    gsap.to('h1', {
      scrollTrigger: {
        trigger: 'h1',
        start: 'top center',
        end: 'bottom top',
        scrub: true,
      },
      y: -150,
      opacity: 0,
      scale: 0.85,
    });
  </script>
</body>
</html>
```

---

#### Receita 2: Next.js 15 (App Router) & React 19 com `<ReactLenis>` e Hook Customizado

Implementação pronta para produção utilizando a biblioteca oficial `lenis/react`:

```tsx
// components/providers/SmoothScrollProvider.tsx
'use client';

import React, { createContext, useContext, useEffect, useRef } from 'react';
import { ReactLenis, useLenis } from 'lenis/react';
import type { LenisRef } from 'lenis/react';
import 'lenis/dist/lenis.css';

interface SmoothScrollProps {
  children: React.ReactNode;
}

export function SmoothScrollProvider({ children }: SmoothScrollProps) {
  const lenisRef = useRef<LenisRef>(null);

  // Exemplo de escuta reativa usando o hook oficial useLenis
  useLenis(({ scroll, velocity, progress }) => {
    // Pode despachar eventos para analytics, custom cursors ou sound engines
  });

  return (
    <ReactLenis
      ref={lenisRef}
      root
      options={{
        lerp: 0.09,
        duration: 1.2,
        wheelMultiplier: 1.0,
        touchMultiplier: 1.5,
        syncTouch: false, // Mantém a sensação tátil nativa dos dispositivos móveis
        autoRaf: true,    // Quando não se usa GSAP Ticker, manter autoRaf: true
      }}
    >
      {children}
    </ReactLenis>
  );
}
```

```tsx
// app/layout.tsx
import { SmoothScrollProvider } from '@/components/providers/SmoothScrollProvider';
import './globals.css';

export default function RootLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <html lang="pt-BR">
      <body className="bg-neutral-950 text-neutral-100 antialiased">
        <SmoothScrollProvider>
          {children}
        </SmoothScrollProvider>
      </body>
    </html>
  );
}
```

```tsx
// components/sections/ParallaxHero.tsx
'use client';

import React, { useRef } from 'react';
import { useLenis } from 'lenis/react';

export function ParallaxHero() {
  const backgroundRef = useRef<HTMLDivElement>(null);
  const textRef = useRef<HTMLHeadingElement>(null);

  // Sincronização direta de sub-pixels sem reflow via transform matricial
  useLenis(({ scroll }) => {
    if (backgroundRef.current) {
      backgroundRef.current.style.transform = `translate3d(0, ${scroll * 0.35}px, 0)`;
    }
    if (textRef.current) {
      textRef.current.style.transform = `translate3d(0, ${scroll * 0.75}px, 0)`;
    }
  });

  return (
    <section className="relative h-[140vh] overflow-hidden flex items-center justify-center">
      <div
        ref={backgroundRef}
        className="absolute inset-0 bg-cover bg-center will-change-transform"
        style={{ backgroundImage: `url('/images/hero-luxury.webp')` }}
      />
      <div className="absolute inset-0 bg-black/40 backdrop-blur-[2px]" />
      <h1
        ref={textRef}
        className="relative z-10 text-8xl font-black uppercase tracking-tighter text-white will-change-transform"
      >
        Cinematic Motion
      </h1>
    </section>
  );
}
```

---

#### Receita 3: Integração WebGL / Three.js / R3F com Sincronização de Câmera 3D

Demonstração de como sincronizar uma cena tridimensional em tela cheia com a rolagem do Lenis, garantindo que a malha 3D e a câmera respondam frame a frame sem descolamento:

```tsx
// components/canvas/Scene3D.tsx
'use client';

import React, { useRef } from 'react';
import { Canvas, useFrame } from '@react-three/fiber';
import { useLenis } from 'lenis/react';
import * as THREE from 'three';

function KineticPlane() {
  const meshRef = useRef<THREE.Mesh>(null);
  const currentVelocity = useRef(0);

  // Captura contínua de velocidade e progresso do Lenis
  useLenis(({ velocity }) => {
    currentVelocity.current = velocity;
  });

  useFrame((state, delta) => {
    if (!meshRef.current) return;
    
    // Amortecimento suave da velocidade angular
    const targetRotation = currentVelocity.current * 0.002;
    meshRef.current.rotation.x = THREE.MathUtils.lerp(
      meshRef.current.rotation.x,
      targetRotation,
      0.1
    );

    // Ondulação de flutuação independente
    meshRef.current.position.y = Math.sin(state.clock.elapsedTime * 1.5) * 0.15;
  });

  return (
    <mesh ref={meshRef}>
      <planeGeometry args={[4, 6, 32, 32]} />
      <meshStandardMaterial
        color="#22c55e"
        wireframe={false}
        roughness={0.2}
        metalness={0.8}
      />
    </mesh>
  );
}

export function SceneCanvas() {
  return (
    <div className="fixed inset-0 pointer-events-none z-0">
      <Canvas camera={{ position: [0, 0, 8], fov: 45 }}>
        <ambientLight intensity={0.5} />
        <directionalLight position={[10, 10, 5]} intensity={1.5} />
        <KineticPlane />
      </Canvas>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao conceber um plano técnico de arquitetura de software e design system para interfaces ricas, o arquiteto de front-end ou o agente de IA deve especificar o subsistema de rolagem obedecendo ao seguinte roteiro:

### 1. Declaração de Stack & Dependências
- Biblioteca: `lenis` (v1.1+) para projetos Vanilla JS / Next.js com orquestração manual, ou `lenis/react` para aplicações React 19 puras.
- CSS: Importação obrigatória do pacote `lenis/dist/lenis.css` no ponto de entrada global.

### 2. Especificação Numérica de Parâmetros de Fluidez
- Definir explicitamente o valor de `lerp`:
  - **Experiência de Estúdio / Storytelling Editorial**: `lerp: 0.08` a `0.1`.
  - **E-Commerce de Moda / Portfólio de Produto**: `lerp: 0.1` a `0.12`.
  - **Interfaces Web Corporativas / Aplicações SaaS**: **Não utilizar Lenis** ou configurar `lerp: 0.2` com `wheelMultiplier: 1.2`.

### 3. Estratégia de Loop Centralizado de Animação (Single Source of Truth)
- Caso o projeto utilize GSAP ScrollTrigger:
  - Definir obrigatoriamente `autoRaf: false` na inicialização do Lenis.
  - Alocar o `lenis.raf(time * 1000)` dentro de `gsap.ticker.add()`.
  - Aplicar `gsap.ticker.lagSmoothing(0)`.
- Caso o projeto seja React/Next.js sem GSAP:
  - Utilizar `<ReactLenis root options={{ autoRaf: true, lerp: 0.09 }}>`.

### 4. Política de Acessibilidade & Mobile First
- Incluir a checagem obrigatória de `prefers-reduced-motion`: se o usuário solicitar movimento reduzido, forçar `lerp: 1.0` ou destruir o Lenis (`lenis.destroy()`).
- Salvo exigência artística intransigente, manter `syncTouch: false` para salvaguardar a física nativa tátil a 120Hz de dispositivos iOS e Android.

### 5. Auditoria de Contenção e Isolamento DOM
- Mapear no blueprint todos os componentes que contêm rolagem interna (modais, caixas de diálogo, seções com `overflow-y: scroll`) e assinalar a presença mandatória do atributo `data-lenis-prevent`.

---

### Checklist de Validação Técnica e Anti-Bugs

- [ ] A propriedade global CSS `scroll-behavior: smooth` foi completamente erradicada da folha de estilos.
- [ ] O CSS fundamental do Lenis (`html.lenis, html.lenis body { height: auto; }`) está carregado antes da renderização do layout.
- [ ] O GSAP Ticker e o Lenis estão operando sobre o mesmo pulso temporal, sem loops de RAF concorrentes em paralelo.
- [ ] Modais de navegação fullscreen disparam `lenis.stop()` ao abrir e `lenis.start()` ao fechar.
- [ ] Elementos com scroll interno possuem `data-lenis-prevent` e `overscroll-behavior: contain`.
- [ ] Teste de pesquisa na página (`Ctrl+F` / `Cmd+F`) executado com sucesso, comprovando que o navegador rola perfeitamente até o termo buscado.
- [ ] `position: sticky` verificado e validado em menus e cabeçalhos sem requerer `position: fixed` manipulado via script.
