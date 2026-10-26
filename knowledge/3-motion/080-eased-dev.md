---
id: "eased-dev"
name: "Eased (Eased.dev)"
url: "https://eased.dev/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["Mathematical Easing Curvature", "Native CSS linear() Springs", "Asymmetric Enter/Exit Physics", "Micro-Interaction Tactility", "Zero-JS Compositor Transitions", "Hydration-Safe Dynamic Orchestration"]
densidade_informacao: "Alta"
impacto_visual: "Sutil/Invisivel (Feel) a Moderado"
custo_computacional: "Baixo (CSS linear() / WAAPI Off-Main-Thread no Compositor e Motion Springs Leves)"
stack_frameworks: ["React 19", "Tailwind CSS v4 (@theme inline & @utility)", "Motion (motion/react v12)", "Base UI (@base-ui/react)", "CSS Animations & Transitions Level 2", "Shadcn CLI Registry", "MCP (Model Context Protocol)"]
compatibilidade:
  combinacoes_recomendadas: ["Eased Tokens + Tailwind CSS v4 (@theme inline + OKLCH colors)", "Motion (motion/react) + Base UI Primitives (@base-ui/react)", "CSS linear() spring variables + CSS transition / animation nativos", "Eased useSafeReducedMotion + Next.js App Router (Zero SSR hydration mismatch)", "Eased TextSwap + Framer Motion layoutId Gliding Indicators"]
  conflitos_esteticos: ["Uso indiscriminado de transition: all em nós complexos (layout thrashing e atraso de renderização)", "Molas com overshoot (bounce/back) em animações de saída ou fechamento de modais/menus", "Interpolação de propriedades geométricas de layout (width, height, top, left, margin) sem técnicas FLIP", "Animação de microinterações com durações superiores a 200ms para feedback de toque/clique", "Concorrência de smooth scrolling via JS agressivo com springs nativas de layout"]
---

# Eased (Eased.dev) — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)

A esmagadora maioria das interfaces digitais contemporâneas falha em proporcionar uma sensação tátil de solidez porque trata a animação como um mero efeito cosmético adicionado a posteriori. Desenvolvedores costumam aplicar valores arbitrários como `transition: all 0.3s ease` ou exagerar em efeitos de rebote (*bounces*) cartunescos que atrasam a cognição do usuário. 

O projeto **Eased** (`https://eased.dev/`), idealizado como um sistema de engenharia de movimento e biblioteca de componentes React 19 para o ecossistema `shadcn/ui` e agentes autônomos de IA, adota uma postura diametralmente oposta: **o movimento como extensão da inércia mecânica e da percepção biológica humana**. 

```
+--------------------------------------------------------------------------------------------------+
|                                    A TRÍADE DE MOVIMENTO DO EASED                                |
+------------------------------------+------------------------------------+------------------------+
|             SNAPPY                 |               SMOOTH               |         BOUNCY         |
+------------------------------------+------------------------------------+------------------------+
| stiffness: 520, damping: 38        | visualDuration: 0.4s, bounce: 0    | stiffness: 400, damp: 26|
| Duração: 350ms (linear())          | Duração: 450ms (linear())          | Duração: 600ms (linear)|
| Press, toggles, focus, text swap   | Layout FLIP, painéis, toasts, pos  | Revelações lúdicas     |
| [Micro-tátil, retorno instantâneo] | [Crítico: ZERO overshoot / calmo]  | [Nunca usado em saídas]|
+------------------------------------+------------------------------------+------------------------+
```

### 1.1. O Colapso do Paradigma das Curvas Bézier Clássicas

Durante mais de duas décadas, a função de interpolação canônica da web foi `cubic-bezier(x1, y1, x2, y2)`. Geometricamente, uma curva Bézier cúbica é uma curva paramétrica de 3º grau ancorada em $(0,0)$ e $(1,1)$, com dois pontos de controle vetoriais $P_1(x_1, y_1)$ e $P_2(x_2, y_2)$. 

Embora seja possível criar um efeito de antecipação ou um leve overshoot elevando $y_2 > 1.0$ (como na curva clássica `cubic-bezier(0.34, 1.56, 0.64, 1)`), **uma curva Bézier cúbica só consegue cruzar o limite de repouso uma única vez**. Ela é matematicamente incapaz de modelar a equação diferencial de uma mola real:

$$m \frac{d^2x}{dt^2} + c \frac{dx}{dt} + k x = 0$$

Em um oscilador harmônico amortecido, a massa $m$ oscila repetidas vezes em torno do ponto de equilíbrio com amplitude decrescente regulada pelo amortecimento $c$. Para replicar esse comportamento no navegador, equipes de engenharia eram forçadas a recorrer a runtimes pesados em JavaScript (`react-spring`, `framer-motion`, `gsap`) que interceptam a thread principal a cada 16ms (`requestAnimationFrame`) para computar coordenadas cartesianas e sobrescrever estilos inline.

### 1.2. A Revolução do CSS Nativo `linear(...)`

O Eased resolve essa fratura arquitetural adotando a especificação **CSS Values and Units Module Level 4: A função `linear(...)`**. 

A função `linear()` do CSS moderno permite mapear uma função de temporização poligonal com dezenas de paradas de interpolação afim. Ao amostrar matematicamente a trajetória física de uma mola harmônica real e codificá-la em uma cadeia de pontos percentuais, o navegador Chromium/WebKit/Gecko executa a física de molas **diretamente na Compositor Thread da GPU**, sem nenhuma execução de script JS em tempo de execução:

```css
/* Amostragem do oscilador amortecido (stiffness: 520, damping: 38) */
--eased-spring-snappy: linear(
  0, 0.0347, 0.1182, 0.2269, 0.3441, 0.4591, 0.5654, 0.6594, 0.7398, 0.8064,
  0.8603, 0.9028, 0.9355, 0.96, 0.9778, 0.9902, 0.9986, 1.0039, 1.007,
  1.0084, 1.0088, 1.0084, 1.0077, 1.0067, 1.0057, 1.0047, 1.0038, 1.0029, 1
);
```

### 1.3. O Espelho Bilateral: CSS Nativo ↔ Motion Object

No Eased, não existe descompasso sensorial entre estilos estáticos e componentes dinâmicos. Todo token de movimento existe em duplicata simétrica:
1. **Como Variável CSS Global**: Para transições CSS nativas ultra-rápidas em classes do Tailwind CSS v4 (`--eased-spring-snappy`, `--eased-ease-enter`, etc.).
2. **Como Objeto de Configuração Motion**: No módulo `motion.ts`, para transições declarativas em componentes `motion/react` (`snappy`, `smooth`, `enter`, `exit`).

Ambos são gerados a partir dos mesmos parâmetros de física. Uma transição de cor disparada por `:hover` via CSS e uma reorganização de lista FLIP via Framer Motion possuem rigorosamente a mesma resposta de aceleração e repouso.

### 1.4. A Assinatura Gráfica: "The Eased Curve"

A própria identidade visual da plataforma Eased (seu logotipo e monograma minimalista) é o traçado exato da sua curva de entrada padrão:

$$\text{Ease Enter} = \text{cubic-bezier}(0.16, 1, 0.3, 1)$$

Essa curva é uma variação hiper-acelerada da família **Ease-Out-Expo**. Ela atinge 80% do seu deslocamento total no primeiro quarto de sua duração, desacelerando com extrema sutileza no terço final. Isso cria uma sensação de resposta instantânea (*snappiness*) combinada a um pouso almofadado imperceptível.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários

1. **Aplicações de Alta Frequência Operacional (B2B SaaS, IDEs, Painéis Analíticos & FinTech)**:
   - Em ferramentas financeiras, trocas de dígitos e indicadores de lucro/prejuízo exigem tipografia tabular rigorosa e animação em mola contida (`NumberRoll`).
   - Botões de confirmação que mudam de estado sem causar pulo de layout horizontal ("Save" → "Saved") via interpolação de largura elástica.
2. **Interfaces Conversacionais & Sistemas Guiados por Agentes de IA**:
   - Componentes que exibem raciocínio sintético em tempo real sem estresse visual: *shimmer text sweeps* de baixa frequência, badges de status pulsantes em ritmo orgânico e balões de diálogo que crescem a partir do ponto de ancoragem do prompt.
3. **Design Systems Corporativos Escaláveis Baseados em Tailwind v4 e Shadcn/UI**:
   - Como substituição direta e refinamento cinético sobre o `shadcn/ui` tradicional, injetando microinterações táteis padronizadas em botões, campos de texto, tabs deslizantes e gavetas (*sheets*).
4. **Sistemas de Navegação Guiada e Onboarding (Spotlight Tours & Command Palettes)**:
   - Transições de foco elástico onde o anel de foco (*focus ring*) desliza suavemente entre controles interativos usando física de mola sem ultrapassar as bordas concêntricas (`radius-nested`).

### Papel no Ritmo Visual (Regra 60-30-10)

```
+--------------------------------------------------------------------------------------------------+
|                              DISTRIBUIÇÃO CINÉTICA NA REGRA 60-30-10                             |
+--------------------------------------------------------------------------------------------------+
| 60% — ESTRUTURA NEUTRA & REPOUSO ABSOLUTO                                                        |
| Superfícies sólidas em OKLCH, grid geométrico imutável, textos de leitura estáticos.             |
| Zero animações contínuas de fundo; ausência total de distração visual passiva.                   |
+--------------------------------------------------------------------------------------------------+
| 30% — MICRO-FEEDBACK TÁTIL INVISÍVEL (THE "FEEL")                                                |
| - Pressionamento de botão em 100ms e retorno elástico em mola snappy (350ms);                    |
| - Transições de cor e opacidade em 150ms (ease-standard);                                        |
| - Anel de foco elástico transitando em 180ms;                                                    |
| - TextSwap sutil com blur de 4px na troca de rótulos funcionais.                                 |
+--------------------------------------------------------------------------------------------------+
| 10% — MOMENTOS DE DESTAQUE & SHOWPIECES                                                          |
| - Gliding Indicator que desliza fisicamente entre abas (Tabs) via layoutId de mola smooth;       |
| - Spotlight Tour que mascara a interface e viaja entre painéis do dashboard;                     |
| - NumberRoll rolando dígitos tabulares na atualização de saldos ou métricas chave.               |
+--------------------------------------------------------------------------------------------------+
```

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Quando Evitar (Anti-Padrões de Movimento)

1. **PROIBIÇÃO ABSOLUTA: Molas com Overshoot em Animações de Saída (*Exit Bounce*)**:
   - **Regra Fundamental do Eased**: Um elemento que entra está chegando para ser visto; um elemento que sai está no caminho do usuário. Elementos em saída **nunca devem ter rebote ou desaceleração prolongada**. 
   - A saída deve durar no máximo **75% do tempo da entrada** (ex: entrada em 200ms → saída em 150ms ou 100ms) e deve obrigatoriamente utilizar curvas de aceleração contínua (**Ease-In-Expo**, `cubic-bezier(0.7, 0, 0.84, 0)`). Fazer um modal ou menu quicar ao fechar transmite sensação de software quebrado e lento.
2. **O Erro Mortal de `transition: all`**:
   - Nunca declare `transition: all`. Isso força o navegador a rastrear dezenas de propriedades computadas a cada mutação de pseudo-classe (`:hover`, `:active`, `:focus`), incluindo propriedades que provocam recálculo de layout (*reflow*). Declare explicitamente apenas os canais transformados:
   ```css
   /* Anti-padrão condenado */
   transition: all 0.2s;

   /* Padrão canônico do Eased */
   transition: color 150ms var(--eased-ease-standard),
               background-color 150ms var(--eased-ease-standard),
               scale var(--eased-duration-spring-snappy) var(--eased-spring-snappy);
   ```
3. **Animação Contínua de Propriedades de Layout sem FLIP**:
   - Jamais anime `width`, `height`, `top`, `left`, `margin` ou `padding` diretamente via CSS transitions quadro a quadro em nós que possuam filhos complexos. Se um botão precisa acomodar um rótulo mais largo, utilize a técnica FLIP automatizada da biblioteca Motion (`layoutId` ou `layout="size"`), mantendo a renderização restrita à GPU via transforms vetoriais.
4. **Over-Animation em Ações Acionadas por Teclado**:
   - Ações de alta frequência orientadas por atalhos de teclado (como navegar em listas de um Command Palette com as setas para cima/baixo, fechar janelas com Esc ou digitar em campos) **não devem conter animação de transição**. O atraso sensorial prejudica a digitação cega de desenvolvedores e *power-users*.
5. **Hover Alterando Tamanho, Peso ou Posição Estrutural**:
   - Pseudo-classes `:hover` devem alterar unicamente cores, contraste ou elevação de sombra em uma única etapa discreta. Mudar o peso da fonte (`font-weight: 500` → `600`) ou a escala no hover gera oscilação perceptiva e fadiga ocular.

### ⚠️ Regras de Acessibilidade & GPU

1. **Prevenção de Hydration Mismatch em `prefers-reduced-motion`**:
   - O hook padrão `useReducedMotion()` de bibliotecas como Framer Motion avalia a media query no primeiro frame do cliente, o que provoca erros frequentes de hidratação (*hydration mismatch*) no SSR do Next.js / React 19 se o servidor tiver emitido HTML para movimento padrão.
   - O Eased introduz a primitiva **`useSafeReducedMotion()`**, implementada com a API nativa `useSyncExternalStore`:
     - No servidor e durante o primeiro render de hidratação: retorna consistentemente `false`.
     - Imediatamente após a montagem segura: sincroniza com `window.matchMedia("(prefers-reduced-motion: reduce)").matches` e ouve eventos em tempo real.
2. **Fallback Gradual via Token `reducedFade`**:
   - Sob movimento reduzido, componentes não devem subitamente "desaparecer no escuro" sem nenhum sinal tátil. As transições de translação espacial e escala são desarmadas (`scale: 1`, `y: 0`), sendo substituídas por um *fade* suave de opacidade em exatamente 100ms (`--eased-duration-instant`).
3. **Gestão Estrita de `will-change` na VRAM**:
   - O atributo CSS `will-change: transform` consome fatias dedicadas de memória VRAM na placa de vídeo. Aplicar `will-change` permanentemente em dezenas de cartões ou botões causa esgotamento de memória em dispositivos móveis (*GPU VRAM thrashing*). No Eased, o isolamento de camada é injetado estritamente durante o gesto ativo (`pointerdown` ou `drag`) e descartado imediatamente após o repouso mecânico da mola.

---

## 4. Catálogo de Efeitos, Primitivas e Padrões de Animação

### 1. Width-Springing Text Swap (`TextSwap` Primitive)
- **Comportamento Visual**: Quando o texto interno de uma ação muda (ex: "Copy" → "Copied" ou "Save" → "Saved"), o rótulo antigo sobe 3px e desaparece com um leve desfoque gaussiano suave (`blur(4px)`). Simultaneamente, o novo rótulo emerge de 4px abaixo com desfoque e pousa no centro. Crucialmente, o canal de desfoque (*blur*) é desacoplado da mola espacial e roda em uma curva temporal separada (`fade`), limpando a visão antes que o deslocamento físico termine de assentar. A largura do contêiner expande ou contrai via mola `snappy`, eliminando pulos de layout.
- **Gatilho**: Mutação da prop `children` ou da chave declarativa `swapKey`.
- **Onde Encaixar**: Botões de ação, chips de status, badges reativos, controles de cópia em blocos de código.

### 2. Width-Adaptive Button Press Feedback (`press`, `pressIcon`, `pressWide`)
- **Comportamento Visual**: Ao ser pressionado via clique de mouse ou toque, o botão contrai dimensionalmente em exatamente 100ms (`--eased-duration-instant`) usando a curva `ease-standard`. Ao liberar, o botão salta de volta para a escala unitária com a mola de alta rigidez `snappy` (350ms). A magnitude da contração adapta-se geometricamente à largura do componente para evitar que botões largos pareçam "afundar no abismo":
  - Ícones quadrados (≤ 48px): escala `0.96` (`pressIcon`);
  - Botões de texto convencionais: escala `0.97` (`press`);
  - Barras, banners e cartões largos (> 220px): escala `0.985` (`pressWide`).
  - *Gatilhos com menus suspensos* (`aria-haspopup`): escala travada em `1.0` (o feedback é puramente por transição de cor para não quebrar o alinhamento da âncora do popover).
- **Gatilho**: Eventos `:active`, `pointerdown` e `pointerup`.
- **Onde Encaixar**: Toda a hierarquia de botões primários, secundários e ícones da aplicação.

### 3. Zero-Layout-Shift Loading Overlay
- **Comportamento Visual**: Quando a prop `loading` é ativada em um botão, o texto funcional sofre uma transição de opacidade para `0` via mola `swapOut`, mas permanece presente no fluxo de dimensões para travar a largura física original. Um spinner minimalista surge sobreposto absolutamente no centro geométrico. Ao concluir a requisição, o spinner desvanece e o rótulo reaparece sem que o botão altere um único pixel de tamanho nem perca o foco do teclado (evitando que o foco caia no `body`).
- **Gatilho**: Mutação da flag assíncrona `loading={true}`.
- **Onde Encaixar**: Botões de checkout, formulários de submissão, botões de autenticação.

### 4. Concentric Corner Squircle Indicator (`radius-nested` + Gliding Pill)
- **Comportamento Visual**: Em componentes de abas (`Tabs`) ou grupos segmentados (`Segmented`), o indicador visual ativo desliza entre os botões como uma pílula sólida flutuante. O raio de curvatura (*border-radius*) do indicador adapta-se concentricamente ao contêiner pai através da fórmula matemática implementada na utility `@utility radius-nested`:
  
  $$\text{radius-nested} = \max\left(0\text{px}, r_{\text{pai}} - \text{padding} - \text{border-width}\right)$$
  
  Isso garante concavidade geométrica perfeita de squircles, sem o defeito clássico de cantos que parecem colidir com o contorno externo.
- **Gatilho**: Seleção de nova aba ou clique em item segmentado.
- **Onde Encaixar**: Navegações secundárias, alternadores de período em gráficos analíticos, filtros rápidos.

### 5. Tabular Number Roll with True Minus (`NumberRoll`)
- **Comportamento Visual**: Na atualização de valores numéricos ou percentuais, cada coluna de dígitos rola verticalmente de forma desacoplada com inércia harmônica `snappy`. Para evitar que o alinhamento horizontal das colunas estremeça, os números utilizam `tabular-nums` e a biblioteca substitui o hífen padrão do teclado (U+002D, estreito) pelo caractere tipográfico matemático verdadeiro **True Minus** (`−`, U+2212), que possui exatamente a mesma largura física do sinal de adição (`+`).
- **Gatilho**: Mutação de valores monetários, cotações de criptoativos ou percentuais de performance.
- **Onde Encaixar**: Dashboards financeiros, métricas de MRR/ARR, indicadores de contagem regressiva.

### 6. Origin-Aware Anchor Expansion (Popovers, Tooltips & Menus)
- **Comportamento Visual**: Janelas de sobreposição (*overlays*) nunca emergem do centro geométrico da tela e nunca escalam a partir de zero (`scale: 0`). Em vez disso, fixam seu `transform-origin` no gatilho de ancoragem (*trigger*) e surgem com escala inicial de `0.97` deslocadas em 6px na direção do gatilho (`y: 6`), expandindo em 200ms na curva `ease-enter` (`cubic-bezier(0.16, 1, 0.3, 1)`).
- **Gatilho**: Disparo de tooltip (`hover`), clique em gatilho de popover ou abertura de menu suspenso.
- **Onde Encaixar**: Tooltips contextuais, menus dropdown de navegação, seletores de perfil.

### 7. Asymmetric Enter/Exit Kinetic Engine
- **Comportamento Visual**: A coreografia de entrada e saída é assimetricamente calibrada para a psicologia humana:
  - **Entrada (200ms a 300ms)**: Curva `ease-enter` com desaceleração prolongada que convida o olho a examinar o novo conteúdo.
  - **Saída (100ms a 150ms)**: Curva `ease-exit` (`cubic-bezier(0.7, 0, 0.84, 0)`), sem nenhum rebote, limpando a tela instantaneamente antes que o usuário sinta qualquer atraso.
- **Gatilho**: Montagem e desmontagem controladas por `<AnimatePresence>`.
- **Onde Encaixar**: Diálogos modais, gavetas laterais (*sheets*), alertas e toasts funcionais.

### 8. Dynamic Scroll Edge Feathers (`useScrollFades` + `fade-x`)
- **Comportamento Visual**: Em contêineres com estouro de conteúdo (*scroll containers* verticais ou horizontais), uma máscara de gradiente CSS dinâmico (`mask-image: linear-gradient(...)`) suaviza as bordas em 20px, indicando visualmente que há mais dados a serem revelados. O hook `useScrollFades` monitora a posição via listeners passivos e zera a máscara correspondente assim que o usuário atinge o limite do topo ou da base da lista.
- **Gatilho**: Eventos de rolagem (*scroll*) e alterações dimensionais detectadas por `ResizeObserver`.
- **Onde Encaixar**: Tabelas densas com scroll horizontal em mobile, barras laterais de navegação, painéis de logs.

### 9. Elastic Focus Ring with Standard Damping (`focus-ring` Utility)
- **Comportamento Visual**: Ao navegar via teclado (Tab / Shift+Tab), a marcação de acessibilidade não projeta um contorno pixelado seco. A utility `focus-ring` projeta um anel duplo suave com sombra calibrada em OKLCH que se expande radialmente em 180ms (`--eased-duration-focus`) sob a curva `ease-standard`, garantindo conformidade estrita com as diretrizes WCAG 2.2 AA sem degradar o design cinético.
- **Gatilho**: Disparo da pseudo-classe `:focus-visible`.
- **Onde Encaixar**: Em absolutamente todos os controles interativos (botões, inputs, switches, checkboxes).

### 10. Curated Staggered Cascade
- **Comportamento Visual**: Ao renderizar grupos de dados ou listas de pesquisa, os itens são revelados em cascata rítmica escalonada. Para evitar a sensação de lentidão, o atraso entre elementos consecutivos obedece a regras de densidade temporal rígidas, mantendo o tempo total da cascata sempre abaixo de 400ms:
  - Caracteres tipográficos: `16ms` por caractere;
  - Itens de lista ou cartões: `35ms` por item;
  - Palavras: `40ms` por palavra;
  - Linhas de texto: `80ms` por linha.
- **Gatilho**: Montagem inicial da coleção de dados (nunca disparado em re-renders secundários).
- **Onde Encaixar**: Resultados de busca rápida, listas de notificações, cartões de onboarding inicial.

---

## 5. Matemática do Movimento & Receitas de Código

### 5.1. A Enciclopédia Matemática de Curvas Bézier Clássicas

Para compreender a precisão cirúrgica dos tokens do Eased, é indispensável examinar a tabela matemática das famílias clássicas de interpolação paramétrica:

| Família Matemática | Curva `easeIn` | Curva `easeOut` | Curva `easeInOut` | Assinatura Sensorial & Inércia |
|---|---|---|---|---|
| **Sine** | `(0.12, 0, 0.39, 0)` | `(0.61, 1, 0.88, 1)` | `(0.37, 0, 0.63, 1)` | Quase linear, transições imperceptíveis e extremamente brandas. |
| **Quad** | `(0.11, 0, 0.5, 0)` | `(0.5, 1, 0.89, 1)` | `(0.45, 0, 0.55, 1)` | Aceleração suave de 2º grau ($t^2$); micro-ajustes de cor. |
| **Cubic** | `(0.32, 0, 0.67, 0)` | `(0.33, 1, 0.68, 1)` | `(0.65, 0, 0.35, 1)` | **Canônica do Eased (`ease-in-out`)**. Perfeita para mudanças de posição na tela. |
| **Quart** | `(0.5, 0, 0.75, 0)` | `(0.25, 1, 0.5, 1)` | `(0.76, 0, 0.24, 1)` | Inércia acentuada de 4º grau ($t^4$). Deslocamentos de média distância. |
| **Quint** | `(0.64, 0, 0.78, 0)` | `(0.22, 1, 0.36, 1)` | `(0.83, 0, 0.17, 1)` | **Canônica do Eased (`ease-standard`)**. Ritmo elegante para opacidades e cores. |
| **Expo** | `(0.7, 0, 0.84, 0)` | `(0.16, 1, 0.3, 1)` | `(0.87, 0, 0.13, 1)` | **Canônica do Eased (`ease-exit` e `ease-enter`)**. Aceleração/desaceleração explosiva. |
| **Circ** | `(0.55, 0, 1, 0.45)` | `(0, 0.55, 0.45, 1)` | `(0.85, 0, 0.15, 1)` | Movimento circular hiper-abrupto; parada quase perpendicular. |
| **Back** (Overshoot) | `(0.36, 0, 0.66, -0.56)` | `(0.34, 1.56, 0.64, 1)` | `(0.68, -0.6, 0.32, 1.6)` | Antecipação ou rebote único artificial (restrito a micro-detalhes). |

#### As Regras Cardeais de Aplicação:
1. **Entradas (*Enter*) usam SEMPRE Ease-Out**: O elemento chega em alta velocidade e gasta a maior parte do seu tempo desacelerando suavemente até o ponto de repouso no palco. O Eased emprega **Ease-Out-Expo** (`cubic-bezier(0.16, 1, 0.3, 1)`).
2. **Saídas (*Exit*) usam SEMPRE Ease-In**: O elemento começa em repouso e ganha velocidade acelerada em direção ao infinito para sair do campo de visão o mais rápido possível. O Eased emprega **Ease-In-Expo** (`cubic-bezier(0.7, 0, 0.84, 0)`).
3. **Mutações Visuais no Palco usam Ease-In-Out**: Elementos que iniciam e terminam a transição visíveis na tela (como movimentação entre colunas) aceleram no início e desaceleram no final via **Ease-In-Out-Cubic** (`cubic-bezier(0.65, 0, 0.35, 1)`).

---

### 5.2. As Receitas Nativas de CSS `linear(...)` das Molas Eased

Abaixo encontram-se as fórmulas de discretização das três molas universais codificadas como variáveis nativas de CSS:

```css
:root {
  /* =========================================================================
     MOLA 1: SNAPPY (Stiffness 520, Damping 38, Duration 350ms)
     Uso: Pressionamento de botões, switches, thumbs, anel de foco, TextSwap
     ========================================================================= */
  --eased-duration-spring-snappy: 350ms;
  --eased-spring-snappy: linear(
    0, 0.0347, 0.1182, 0.2269, 0.3441, 0.4591, 0.5654, 0.6594, 0.7398, 0.8064,
    0.8603, 0.9028, 0.9355, 0.96, 0.9778, 0.9902, 0.9986, 1.0039, 1.007,
    1.0084, 1.0088, 1.0084, 1.0077, 1.0067, 1.0057, 1.0047, 1.0038, 1.0029, 1
  );

  /* =========================================================================
     MOLA 2: SMOOTH (Visual Duration 0.4s, Bounce 0.0, Duration 450ms)
     Uso: Layouts FLIP, expansão de painéis, posição de tooltips e toasts
     Característica: Rigorosamente ZERO overshoot; amortecimento crítico puro
     ========================================================================= */
  --eased-duration-spring-smooth: 450ms;
  --eased-spring-smooth: linear(
    0, 0.0323, 0.1079, 0.2039, 0.3059, 0.4053, 0.4974, 0.5799, 0.6519, 0.7138,
    0.7661, 0.8099, 0.8462, 0.8761, 0.9006, 0.9205, 0.9366, 0.9495, 0.9599,
    0.9683, 0.9749, 0.9802, 0.9844, 0.9877, 0.9904, 0.9924, 0.9941, 0.9954, 1
  );

  /* =========================================================================
     MOLA 3: BOUNCY (Stiffness 400, Damping 26, Duration 600ms)
     Uso: Metamorfoses de formas lúdicas e revelações em celebrações
     Característica: Oscilação visível e divertida (PROIBIDA EM SAÍDAS)
     ========================================================================= */
  --eased-duration-spring-bouncy: 600ms;
  --eased-spring-bouncy: linear(
    0, 0.0758, 0.2474, 0.4501, 0.6424, 0.8022, 0.9212, 1.0003, 1.0455, 1.0651,
    1.0673, 1.0593, 1.0464, 1.0326, 1.0202, 1.0103, 1.0032, 0.9987, 0.9963,
    0.9954, 0.9956, 0.9963, 0.9972, 0.9981, 0.9989, 0.9995, 1, 1.0002, 1
  );
}
```

---

### 5.3. Implementação Pronta em Código: O Módulo Core de Física (`motion.ts`)

Abaixo está o arquivo TypeScript canônico que unifica a física de movimento com segurança completa de SSR e acessibilidade:

```typescript
// components/eased/lib/motion.ts
import { useSyncExternalStore } from "react";

/**
 * Definições de molas para a biblioteca Motion (motion/react),
 * perfeitamente sincronizadas com as variáveis CSS em linear().
 */
export const snappy = { type: "spring", stiffness: 520, damping: 38 } as const;
export const smooth = { type: "spring", visualDuration: 0.4, bounce: 0 } as const;
export const bouncy = { type: "spring", stiffness: 400, damping: 26 } as const;

/** Curvas cubic-bezier padronizadas */
export const ease = {
  enter: [0.16, 1, 0.3, 1],       // Ease-Out-Expo (logo signature)
  standard: [0.22, 1, 0.36, 1],   // Ease-Out-Quint
  exit: [0.7, 0, 0.84, 0],        // Ease-In-Expo
  inOut: [0.65, 0, 0.35, 1],      // Ease-In-Out-Cubic
} as const;

/** Durações em segundos */
export const duration = {
  instant: 0.1,    // 100ms - cliques e acessibilidade reduzida
  fast: 0.15,      // 150ms - hovers e mutações de cor
  standard: 0.2,   // 200ms - popovers e tooltips
  slow: 0.3,       // 300ms - diálogos modais
  sheet: 0.5,      // 500ms - gavetas laterais
  fallback: 0.4,   // 400ms - atraso de avatares para evitar flash
} as const;

/** Escalonamento de grupos (stagger) mantido sob o limite de 400ms */
export const stagger = {
  char: 0.016,     // 16ms/char
  item: 0.035,     // 35ms/item
  word: 0.04,      // 40ms/palavra
  line: 0.08,      // 80ms/linha
} as const;

/** Raios de desfoque cinético */
export const blur = {
  subtle: "2px",
  soft: "4px",
  text: "8px",
} as const;

/** Transições compostas fundamentais */
export const enter = { duration: duration.standard, ease: ease.enter } as const;
export const fade = { duration: duration.fast, ease: ease.standard } as const;
export const exit = { duration: duration.fast, ease: ease.exit } as const;
export const exitFast = { duration: duration.instant, ease: ease.exit } as const;
export const reducedFade = { duration: duration.instant } as const;
export const instant = { duration: 0 } as const;

/** Padrão TextSwap: saída para cima em 3px, entrada de baixo em 4px com desfoque desacoplado */
export const swapIn = { opacity: 0, y: 4, filter: `blur(${blur.soft})` } as const;
export const swapShown = { opacity: 1, y: 0, filter: "blur(0px)" } as const;
export const swapOut = { opacity: 0, y: -3, filter: `blur(${blur.soft})` } as const;
export const swap = { ...snappy, opacity: fade, filter: fade } as const;

const REDUCE_QUERY = "(prefers-reduced-motion: reduce)";

function subscribeReduced(onChange: () => void) {
  if (typeof window === "undefined") return () => {};
  const mq = window.matchMedia(REDUCE_QUERY);
  mq.addEventListener("change", onChange);
  return () => mq.removeEventListener("change", onChange);
}

/**
 * Hook universal de movimento reduzido imune a Hydration Mismatches em SSR (React 19 / Next.js).
 * Retorna false durante a hidratação e sincroniza em tempo real com o sistema operacional.
 */
export function useSafeReducedMotion(): boolean {
  return useSyncExternalStore(
    subscribeReduced,
    () => window.matchMedia(REDUCE_QUERY).matches,
    () => false
  );
}
```

---

### 5.4. Componente Completo: Botão Tátil com TextSwap e Dynamic Scale

Abaixo está o componente representativo de alta fidelidade que exemplifica toda a arquitetura de física de movimento do Eased:

```tsx
// components/eased/button/interactive-button.tsx
"use client";

import React, { useState, useRef, useId } from "react";
import { motion, AnimatePresence } from "motion/react";
import {
  snappy,
  swap,
  swapIn,
  swapShown,
  swapOut,
  fade,
  exitFast,
  reducedFade,
  useSafeReducedMotion,
} from "../lib/motion";

export interface InteractiveButtonProps {
  children: React.ReactNode;
  variant?: "primary" | "secondary" | "danger";
  size?: "sm" | "md" | "lg";
  loading?: boolean;
  onClick?: () => void;
  className?: string;
}

const WIDE_THRESHOLD_PX = 220;

export function InteractiveButton({
  children,
  variant = "primary",
  size = "md",
  loading = false,
  onClick,
  className = "",
}: InteractiveButtonProps) {
  const reduced = useSafeReducedMotion();
  const buttonRef = useRef<HTMLButtonElement>(null);
  const [pressScale, setPressScale] = useState<number>(0.97);

  // Calibra a intensidade da contração de acordo com a largura física do elemento
  const handlePointerDown = () => {
    if (!buttonRef.current) return;
    const width = buttonRef.current.offsetWidth;
    // Elementos com largura > 220px contraem apenas 1.5% para não parecerem desmoronar
    setPressScale(width > WIDE_THRESHOLD_PX ? 0.985 : 0.97);
  };

  const sizeClasses = {
    sm: "h-8 px-3 text-xs rounded-lg gap-1.5",
    md: "h-9 px-3.5 text-sm rounded-xl gap-2",
    lg: "h-10 px-4 text-base rounded-2xl gap-2.5",
  }[size];

  const variantClasses = {
    primary: "bg-zinc-100 text-zinc-950 hover:bg-white shadow-sm border-transparent",
    secondary: "bg-zinc-900 text-zinc-200 hover:bg-zinc-800 border-zinc-800",
    danger: "bg-red-500/10 text-red-400 hover:bg-red-500/20 border-red-500/30",
  }[variant];

  return (
    <motion.button
      ref={buttonRef}
      type="button"
      disabled={loading}
      onPointerDown={handlePointerDown}
      onClick={onClick}
      aria-busy={loading || undefined}
      whileTap={reduced || loading ? undefined : { scale: pressScale }}
      transition={reduced ? reducedFade : snappy}
      className={`
        relative inline-flex items-center justify-center font-medium
        border select-none outline-none cursor-pointer
        transition-colors duration-150 ease-[cubic-bezier(0.22,1,0.36,1)]
        focus-visible:ring-2 focus-visible:ring-zinc-400 focus-visible:ring-offset-2
        focus-visible:ring-offset-zinc-950 disabled:cursor-not-allowed
        ${sizeClasses} ${variantClasses} ${className}
      `}
    >
      {/* Texto com morph de largura e transição em mola suave */}
      <motion.span
        className="inline-flex items-center justify-center gap-[inherit]"
        initial={false}
        animate={
          loading
            ? reduced
              ? { opacity: 0 }
              : swapOut
            : reduced
              ? { opacity: 1 }
              : swapShown
        }
        transition={
          reduced
            ? reducedFade
            : loading
              ? { ...swap, opacity: exitFast, filter: exitFast }
              : swap
        }
      >
        <AnimatePresence mode="popLayout" initial={false}>
          <motion.span
            key={String(children)}
            initial={reduced ? { opacity: 0 } : swapIn}
            animate={reduced ? { opacity: 1 } : swapShown}
            exit={reduced ? { opacity: 0 } : swapOut}
            transition={reduced ? reducedFade : swap}
          >
            {children}
          </motion.span>
        </AnimatePresence>
      </motion.span>

      {/* Spinner posicionado absolutamente para zero deslocamento estrutural */}
      <AnimatePresence initial={false}>
        {loading && (
          <motion.span
            key="spinner"
            aria-hidden="true"
            className="absolute inset-0 flex items-center justify-center"
            initial={reduced ? { opacity: 0 } : swapIn}
            animate={reduced ? { opacity: 1 } : swapShown}
            exit={
              reduced
                ? { opacity: 0, transition: reducedFade }
                : { ...swapIn, transition: { ...swap, opacity: exitFast, filter: exitFast } }
            }
            transition={reduced ? reducedFade : swap}
          >
            <svg
              className="size-4 animate-spin text-current"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              strokeWidth="2.5"
            >
              <circle className="opacity-25" cx="12" cy="12" r="10" />
              <path className="opacity-75" d="M4 12a8 8 0 018-8v8H4z" />
            </svg>
          </motion.span>
        )}
      </AnimatePresence>
    </motion.button>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao planejar a implementação técnica de interfaces inspiradas nos princípios e na física do **Eased**, o arquiteto de software ou agente de IA deve formalizar os seguintes parâmetros dentro do `DESIGN_BLUEPRINT.md` antes da escrita de qualquer código:

### 1. Declaração do Vocabulário Físico do Projeto
- **Proibição de Valores Mágicos de Duração**: O blueprint deve proibir expressamente durações arbitrárias soltas no código (ex: proibir `300ms` ou `500ms` inline). Toda animação deve ser referenciada por um dos tokens nominais: `instant` (100ms), `fast` (150ms), `standard` (200ms), `slow` (300ms) ou `sheet` (500ms).
- **Mapeamento Exato das Três Molas**:
  - `snappy` para resposta tátil e elementos pequenos;
  - `smooth` para mudanças estruturais de layout e FLIP sem qualquer overshoot;
  - `bouncy` para transições cosméticas em celebrações isoladas (nunca em saídas).

### 2. Matriz de Decisão de Movimento por Categoria de Componente

| Categoria de UI | Mecanismo de Animação | Curva / Mola Obrigatória | Duração Alvo |
|---|---|---|---|
| **Press Feedback (Botões/Cards)** | CSS `scale` + CSS `linear()` | `--eased-spring-snappy` (scale 0.97) | 100ms down / 350ms release |
| **Troca de Rótulo (TextSwap)** | Motion `AnimatePresence` | `swap` (`y: 4px → 0 → -3px` + blur) | 350ms mola / 150ms fade |
| **Abas & Indicadores Deslizantes** | Motion `layoutId` | `smooth` (`visualDuration: 0.4`, bounce 0) | 450ms sem overshoot |
| **Entrada de Modais e Diálogos** | WAAPI / CSS Keyframes | `ease-enter` (`cubic-bezier(0.16,1,0.3,1)`) | 200ms a 300ms |
| **Saída de Modais e Diálogos** | WAAPI / CSS Keyframes | `ease-exit` (`cubic-bezier(0.7,0,0.84,0)`) | 100ms a 150ms (≤ 0.75× enter) |
| **Hover e Foco de Acessibilidade** | CSS Transitions puras | `ease-standard` (`cubic-bezier(0.22,1,0.36,1)`)| 150ms (cor) / 180ms (anel) |

### 3. Protocolo de Auditoria e Conformidade Técnica
1. **Regra dos 200ms**: Nenhuma resposta tátil direta a uma interação do usuário pode demandar mais de 200ms para fornecer feedback visível perceptível.
2. **Auditoria de `prefers-reduced-motion`**: Todos os componentes dinâmicos devem possuir um ramo de teste automatizado verificando se o hook `useSafeReducedMotion` colapsa as transições espaciais em uma transição pura de opacidade de 100ms (`reducedFade`).
3. **Compositor Verification**: Propriedades animadas no CSS devem ser restritas exclusivamente a `transform`, `opacity`, `filter` e `clip-path`. Qualquer tentativa de animar `width`, `height`, `left` ou `margin` frame a frame deve ser rejeitada na revisão de código do blueprint.
4. **Respeito aos Squircles**: Elementos aninhados dentro de painéis com bordas arredondadas devem utilizar a classe `@utility radius-nested` para preservar a concentricidade geométrica e a proporção de ouro dos cantos.
