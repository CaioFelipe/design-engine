---
id: "lottiefiles"
name: "LottieFiles (dotLottie, WebAssembly/ThorVG Runtime & Interactive Vector Motion)"
url: "https://lottiefiles.com/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["Vector Fidelity Motion", "ThorVG WebAssembly Rendering", "dotLottie ZIP Container", "State Machine Interactivity", "Micro-Interactions & Empty States", "Dynamic Color Slot Theming"]
densidade_informacao: "Media a Alta"
impacto_visual: "Sutil/Invisivel (Feel) a Cinematografico/Showstopper"
custo_computacional: "Baixo (dotLottie WASM / Canvas2D) a Medio (Multiplos Players Simultaneos / State Machines)"
stack_frameworks: ["React 19 / 18", "@lottiefiles/dotlottie-react", "@lottiefiles/dotlottie-web", "ThorVG (C++ / WebAssembly)", "dotlottie-rs (Rust Core)", "Tailwind CSS v4", "TypeScript"]
compatibilidade:
  combinacoes_recomendadas: ["Shadcn UI", "Tailwind CSS", "Framer Motion (Motion.dev)", "Lenis Smooth Scroll", "Next.js App Router", "Lucide React"]
  conflitos_esteticos: ["Substituição inadequada de tipografia semântica e botões nativos por artefatos vetoriais estáticos", "Excesso de loops simultâneos de alta frequência competindo pela atenção primária do usuário", "Renderização indiscriminada de dezenas de instâncias de Canvas sem virtualização e sem pausa fora da viewport"]
---

# LottieFiles — Dossiê de Física de Movimento, Transições & Animação Vetorial de Alta Performance

## 1. Filosofia de Movimento & Sensação Física (Feel)

O **LottieFiles** (`https://lottiefiles.com/`), plataforma fundada em 2017 por **Kshitij Minglani** e **Nattu Adnan** (posteriormente integrada à Design Barn Inc. e investida pela Microsoft M12), transformou a animação vetorial interativa em um padrão de infraestrutura de software mundial. A tecnologia resolveu uma das fissuras mais complexas da engenharia de interface: como transportar a riqueza cinemática e orgânica de ferramentas profissionais de animação (como Adobe After Effects, Cavalry ou Lottie Creator) diretamente para a web e aplicativos nativos sem o peso colossal de vídeos rasterizados (MP4/GIF) e sem a fragilidade de recriar milhares de curvas Bézier manualmente em código CSS imperativo.

---

### A Linhagem do Lottie: De Charlotte Reiniger ao Bodymovin e ao dotLottie

A genealogia do Lottie fundamenta-se em três marcos históricos:
1. **Charlotte "Lottie" Reiniger (1899–1981)**: Cineasta alemã pioneira da animação em silhueta e do teatro de sombras animado. Sua técnica de articular formas recortadas com extrema precisão mecânica inspirou o nome do formato.
2. **Hernan Torrisi & Airbnb (2015–2017)**: Hernan Torrisi desenvolveu o plugin de código aberto **Bodymovin** para o Adobe After Effects, capaz de serializar a árvore de composição, camadas vetoriais, traçados e interpolações em um arquivo estruturado JSON. Em 2017, os engenheiros do Airbnb (Brandon Withrow, Gabriel Peal e Leland Richardson) lançaram as bibliotecas mobile e web de código aberto batizadas de *Lottie*, popularizando o conceito de "JSON como vídeo vetorial".
3. **LottieFiles & O Salto Arquitetural dotLottie (2020–presente)**: Percebendo que o JSON puro era inflacionado, desprovido de empacotamento de assets e custoso de parsear na thread principal, a LottieFiles padronizou a especificação aberta **dotLottie** (`.lottie`). Trata-se de um contêiner ZIP otimizado que agrupa animações, imagens rasterizadas, fontes, arquivos de áudio, esquemas de temas (*theming slots*) e máquinas de estado (*state machines*), reduzindo o payload de rede em até **80%** em relação ao JSON original.

---

### O Salto de Performance: ThorVG + WebAssembly vs. O Legado DOM/SVG

O ecossistema original (`lottie-web`) operava prioritariamente através do renderizador SVG. Embora garantisse nitidez infinita, criava um gargalo de desempenho severo em interfaces complexas:
- **Sobrecarga do DOM**: Um único ícone animado com máscaras complexas, sombras e traçados desmembrava-se em centenas de nós `<path>`, `<g>` e `<mask/>` injetados diretamente na árvore do documento. Em páginas ricas ou listagens virtuais, a contagem de nós DOM explodia, gerando recalculos de estilo contínuos (*style recalculation spikes*) e travamento do *Garbage Collector*.
- **A Solução Moderna: ThorVG compilado para WASM**: No runtime de última geração (`@lottiefiles/dotlottie-react` / `@lottiefiles/dotlottie-web`), o núcleo de renderização é o **ThorVG** (Thor Vector Graphics, motor open-source industrial escrito em C++ nativo e encapsulado em Rust via `dotlottie-rs`), compilado diretamente para **WebAssembly (WASM)**.
- **Renderização Direta em Hardware (Canvas / WebGL2)**: Em vez de manipular o DOM, o runtime WASM processa a matemática vetorial e projeta os pixels diretamente em um único elemento `<canvas>` via Canvas2D ou WebGL2. O consumo de CPU da thread principal cai drasticamente, liberando o navegador para processar a lógica do React e interações de toque a estáveis **60fps / 120fps**.

```
┌────────────────────────────────────────────────────────────────────────┐
│               ARQUITETURA DE EXECUÇÃO MODERNA DOTLOTTIE                │
└────────────────────────────────────────────────────────────────────────┘
                                   │
              Criação (After Effects / Lottie Creator / Figma)
                                   │
                                   ▼
             ┌──────────────────────────────────────────────┐
             │ Pacote .lottie (ZIP Container v2)            │
             │ • manifest.json (Metadata, State Machines)   │
             │ • animations/ (JSONs vetoriais compactados)  │
             │ • states/ (Transições, Inputs, Guards)       │
             │ • themes/ (Color Slots & CSS Token Mappings) │
             └──────────────────────────────────────────────┘
                                   │
                 Streaming de Rede (Payload até 80% menor)
                                   │
                                   ▼
┌────────────────────────────────────────────────────────────────────────┐
│ Browser Client: @lottiefiles/dotlottie-react                           │
│                                                                        │
│   ┌────────────────────────────────────────────────────────────────┐   │
│   │ WebAssembly Sandbox (dotlottie-rs / ThorVG C++ Core)           │   │
│   │ • Descompressão do pacote e leitura de manifest                │   │
│   │ • Resolução de State Machine e interpolação de Bézier          │   │
│   │ • Rasterização vetorial matemática ultra-rápida                │   │
│   └────────────────────────────────────────────────────────────────┘   │
│                                  │                                     │
│                                  ▼                                     │
│   ┌────────────────────────────────────────────────────────────────┐   │
│   │ Hardware Presentation Target (<canvas> / WebGL2 / WebGPU)      │   │
│   │ Zero poluição de nós DOM | Isolamento de repaint | 120 FPS     │   │
│   └────────────────────────────────────────────────────────────────┘   │
└────────────────────────────────────────────────────────────────────────┘
```

---

### A Física Vetorial de Curvas Bézier Nativas

Diferente de sistemas de física puramente baseados em equações diferenciais de molas (*spring physics* em tempo real), o Lottie executa **interpolações temporais e espaciais de curvas Bézier cúbicas herméticas**. 

No formato Lottie, cada ponto chave (*keyframe*) encapsula dois vetores de controle de aceleração:
- `o` (*outTangent*): O vetor de aceleração na saída do keyframe (coordenadas `{ x, y }` entre `0` e `1`).
- `i` (*inTangent*): O vetor de desaceleração na chegada ao keyframe de destino (coordenadas `{ x, y }` entre `0` e `1`).

Isso permite que designers de movimento esculpam curvas de aceleração com extrema fidelidade orgânica:
- **Snappy Ease-Out**: Aceleração instantânea nos primeiros 10% da duração com curva de chegada quase horizontal, conferindo a sensação de um mecanismo tátil que estala na posição com precisão metálica.
- **Anticipation Wind-Up**: O vetor `o` mergulha sutilmente abaixo de zero ou retarda o início, imitando a contração muscular humana antes de um salto expressivo.
- **Elastic Settle & Overshoot**: A trajetória do valor ultrapassa a meta final em até 8% e retorna em oscilação amortecida, calculada de forma vetorial diretamente nas curvas de posição e escala.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

O ecossistema LottieFiles e o formato `.lottie` são a escolha definitiva quando a interface exige **narrativa vetorial, sincronização de múltiplos elementos anatômicos ou interatividade tátil complexa** que seria excessivamente onerosa ou matematicamente impraticável em CSS puro.

---

### Casos de Uso Críticos

1. **Micro-Ícones com Morphing e Feedback Tátil**:
   - Ícones funcionais que deixam de ser pictogramas estáticos e passam a representar estados de transição contínua:
     - Alternância de áudio (Volume mudo para ondas acústicas oscilantes).
     - Menu hambúrguer que se desmonta e se recompõe como um ícone de fechar (`X`).
     - Botão de "Salvar / Favorito" que transita de contorno cinza para preenchimento de coração explodindo em confetes e micro-partículas.
2. **Empty States & Onboarding Educativo**:
   - Telas de boas-vindas e estados vazios (ex: "Nenhum arquivo encontrado", "Caixa de entrada limpa", "Configure sua primeira integração"). Animações em loop sutil humanizam a interface, reduzem a sensação de frustração e comunicam a próxima ação recomendada sem sobrecarga textual.
3. **Milestones de Checkout & Sucesso Transacional**:
   - O clímax de uma experiência transacional (finalização de compra, deploy de código na nuvem, transferência bancária). O traçado de um círculo que se fecha, seguido pelo risco confiante do checkmark e um leve estouro de partículas comemorativas, libera dopamina e ratifica visualmente a segurança da operação.
4. **Demonstrações Interativas em Bento Grids (Product-in-Action)**:
   - Apresentações modulares em páginas de produtos modernos. Em vez de vídeos pesados de 15MB, arquivos `.lottie` de 25KB mostram cursores colaborativos simulando edição simultânea, badges sendo arrastados e filtros sendo aplicados com nitidez vetorial infinita em telas Retina/4K.
5. **Scroll-Driven Storytelling (Animações Scrubbed por Rolagem)**:
   - Narrativas de produtos onde o progresso do scroll do usuário atua como a cabeça de reprodução (*scrubber*) da animação. Conforme o usuário desce a página, uma arquitetura de nuvem se conecta, um hardware se abre em visão explodida ou dados estatísticos se estruturam visualmente.

---

### A Regra 60-30-10 na Cinemática Vetorial

Na arquitetura visual e de movimento de uma aplicação moderna, o Lottie deve ser balanceado cirurgicamente:

```
┌────────────────────────────────────────────────────────────────────────┐
│              DISTRIBUIÇÃO CINEMÁTICA NA REGRA 60-30-10                 │
├────────────────────────────────────────────────────────────────────────┤
│ ████████████████████████████████ 60% ESTABILIDADE & REPOUSO            │
│ Telas, cards, tipografia e layouts estáticos limpos. Lottie 100%       │
│ inativo ou congelado em repouso. Zero fadiga atencional.               │
├────────────────────────────────────────────────────────────────────────┤
│ ████████████████ 30% MICRO-FEEDBACK TÁTIL (DOTLOTTIE)                  │
│ Micro-ícones responsivos a hover/click, spinners funcionais, toggles   │
│ de tema morfológicos (200ms - 400ms). Fluidez funcional invisível.     │
├────────────────────────────────────────────────────────────────────────┤
│ █████ 10% SHOWSTOPPER / ACCENT MOTION                                  │
│ Confetti de checkout, ilustrações interativas com State Machine,       │
│ heróis cinematográficos scrubbed por scroll. O clímax da experiência.  │
└────────────────────────────────────────────────────────────────────────┘
```

- **60% (Repouso e Estabilidade)**: A grande maioria da interface permanece firme. O Lottie nunca deve ser espalhado aleatoriamente em todos os cantos. Se cinco ilustrações estiverem em loop contínuo na mesma tela, o cérebro do usuário entra em sobrecarga sensorial.
- **30% (Micro-Feedback Funcional)**: Ícones de navegação interativos, seletores de modo escuro/claro e botões de alternância. Operam em durações curtas (200ms a 380ms) e apenas disparam sob demanda do usuário.
- **10% (Showstopper / Accent Visual)**: O momento estelar do produto. Uma grande animação de celebração na confirmação de um pedido ou uma ilustração generativa que reage à posição do mouse na Hero Section.

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

A flexibilidade de exportar qualquer composição do After Effects para Lottie induz frequentemente equipes de desenvolvimento a armadilhas críticas de performance e acessibilidade.

---

### ⚠️ Quando Evitar Absolutamente

1. **Substituição de Tipografia e Botões Semânticos**:
   - **Anti-padrão grave**: Criar botões inteiros no After Effects contendo textos e exportá-los em Lottie.
   - **Impacto**: Aniquila a acessibilidade para leitores de tela, destrói a seleção de texto do usuário, impossibilita traduções internacionais (i18n) e impede o redimensionamento fluido em zoom de acessibilidade do navegador.
2. **Listagens Longas e Feeds Virtualizados Sem Virtualização de Player**:
   - Instanciar um player Lottie ativo para cada item em uma tabela ou feed com centenas de linhas. Mesmo com ThorVG WASM, alocar dezenas de contextos de renderização `<canvas>` simultâneos consome a memória gráfica da GPU e drena a bateria de aparelhos móveis.
3. **Animações Vetoriais Hiper-Complexas (Over-Tessellation)**:
   - Ilustrações importadas de vetores complexos do Illustrator com dezenas de milhares de âncoras Bézier, traçados auto-interseccionados ou dezenas de camadas de desfoque gaussiano (*Gaussian Blur*). O motor gastará mais ciclos de CPU calculando máscaras e gradientes por frame do que um vídeo MP4/WebM pré-renderizado.
4. **Dashboards Financeiros e Gráficos de Alta Frequência**:
   - Em telas com atualizações a cada 100ms (como terminais de trading ou telemetria em tempo real), a renderização contínua de ilustrações decorativas compete por ciclos preciosos da CPU/GPU que deveriam ser dedicados a gráficos WebGL analíticos.

---

### ⚠️ Regras Mandatórias de Acessibilidade, Bateria & GPU

* **Respeito Estrito a `prefers-reduced-motion`**:
  O usuário com sensibilidade vestibular ou déficit de atenção pode ter configurado o sistema operacional para reduzir movimentos. Nesses casos, o player Lottie **deve obrigatoriamente pausar de imediato**, saltando diretamente para o frame final (`goToAndStop(totalFrames)`) ou para o frame representativo estático, sem qualquer animação em loop.
* **Ciclo de Vida e Limpeza de Memória (`destroy`)**:
  Em SPAs e frameworks baseados em componentes (React, Next.js, Vue), todo player Lottie que for desmontado (`unmount`) deve invocar explicitamente seu método de descarte (`dotLottie.destroy()`). O não encerramento retém o binário WASM e o contexto do Canvas na memória, gerando vazamentos progressivos de memória (*memory leaks*).
* **Auto-Pausa Baseada em Visibilidade (IntersectionObserver)**:
  Nenhum Lottie deve continuar renderizando frames em loop se estiver fora da área visível (*viewport*) da janela. A biblioteca deve ser integrada a um `IntersectionObserver` que congela o loop quando o elemento sai de vista e o retoma suavemente quando o usuário rola de volta.
* **Acessibilidade Semântica (WAI-ARIA)**:
  O contêiner do Lottie deve conter `role="img"` e um atributo `aria-label` textual descritivo claro. Se a animação for meramente decorativa, aplique explicitamente `aria-hidden="true"` para que os leitores de tela ignorem o Canvas silenciosamente.

---

## 4. Catálogo de Efeitos, Primitivas e Padrões de Animação

Abaixo estão catalogados **10 padrões cinemáticos fundamentais** viabilizados pelo ecossistema LottieFiles e pelo runtime dotLottie moderno:

---

### 1. Interactive Theme Toggle Morph (Sol ↔ Lua)
* **Comportamento Visual**: No estado diurno, o ícone exibe uma esfera solar central com 8 raios radiais projetados. Ao receber o clique do usuário, os raios retraem-se em direção ao centro em um colapso cinético; simultaneamente, uma máscara curva penetra lateralmente na esfera solar, moldando-a organicamente em uma lua crescente enquanto estrelas microscópicas cintilam no fundo escuro. No caminho inverso, a lua se desdobra suavemente e ejeta os raios de luz com overshoot elástico.
* **Gatilho**: Disparo por evento `onClick` ou alternância de estado de tema no React/CSS.
* **Onde Encaixar**: Barra de navegação principal (Navbar), menus de configurações, rodapés de aplicações.
* **Anatomia dos Keyframes**: Duração total de 36 frames (600ms a 60fps). Transição de 0 a 18 (Dia para Noite); de 19 a 36 (Noite para Dia). Curva de aceleração `cubic-bezier(0.34, 1.56, 0.64, 1)` com overshoot de 12% na projeção dos raios.

---

### 2. Scroll-Linked Scrubbing (Choreographed Storytelling)
* **Comportamento Visual**: A cabeça de reprodução da animação vetorial é matematicamente vinculada ao deslocamento de rolagem do usuário (`scrollProgress` normalizado entre `0.0` e `1.0`). O usuário controla o tempo de forma bidirecional: rolar para baixo avança o desmonte tridimensional de um produto (ex: peças de um dispositivo eletrônico se separando em camadas axiais); rolar para cima reconecta instantaneamente os componentes.
* **Gatilho**: Evento contínuo de `scroll` da janela ou gatilho fixado via `position: sticky`.
* **Onde Encaixar**: Seções de apresentação de arquitetura técnica, hardware specs ou storytelling institucional na Hero.
* **Anatomia dos Keyframes**: Sequência contínua de 120 a 240 frames sem marcadores discretos. Interpolação linear controlada diretamente pela função de interpolação `seek(scrollPercentage * totalFrames)`.

---

### 3. Bimodal Milestone Checkmark (Transação Concluída)
* **Comportamento Visual**: No início, o componente exibe um círculo neutro cinza. No disparo da transação, o círculo se contrai em antecipação (*squash*), muda de cor para um verde esmeralda vibrante e sua borda se redesenha com um efeito de traçado vetorial (*trim path*) dinâmico. No instante em que o círculo fecha os 360 graus, uma linha de checkmark dispara do centro para a direita com aceleração de choque e desaceleração suave, enquanto 6 micro-partículas estouram radialmente ao redor do selo e desvanecem com gravidade simulada.
* **Gatilho**: Promessa assíncrona resolvida com sucesso (ex: `paymentPromise.resolve()` ou `git push` completado).
* **Onde Encaixar**: Modais de pagamento, modais de confirmação de cadastro, diálogos de deploy em DevOps.
* **Anatomia dos Keyframes**: Frames 0 a 12 (Contração e fecho do anel); frames 13 a 24 (Desenho do traçado do checkmark com `cubic-bezier(0.16, 1, 0.3, 1)`); frames 20 a 34 (Explosão radial e desvanecimento das partículas com `opacity` indo de 100% a 0%).

---

### 4. LookAt Cursor Tracker (Follow-Focus State Machine)
* **Comportamento Visual**: Um mascote ilustrado ou avatar de segurança vetorial cujas pupilas, sobrancelhas e inclinação sutil da cabeça acompanham a posição exata das coordenadas do cursor do mouse do usuário na tela. Quando o usuário clica em um campo de entrada de senha, a máquina de estado transita imediatamente para uma animação onde as patas ou mãos do mascote sobem rapidamente e cobrem os olhos de forma bem-humorada.
* **Gatilho**: Movimento contínuo do ponteiro (`pointermove`) normalizado em inputs numéricos (`mouseX`, `mouseY`) injetados na State Machine do dotLottie.
* **Onde Encaixar**: Telas de login e autenticação, fluxos de checkout interativos, assistentes de IA e copilotos de software.
* **Anatomia dos Keyframes**: Duas camadas dimensionais independentes: eixos X e Y mapeados para posições relativas de camadas de olho (`-10px` a `+10px`), com um gatilho booleano discreto `isPasswordFocused` que comuta para a máquina de transição "HandsCoverEyes".

---

### 5. Multi-Stage Stepper / Progressive Deployment Rail
* **Comportamento Visual**: Uma barra de progresso visual que não é apenas um retângulo preenchido, mas uma linha viva composta por nós de circuito. À medida que o fluxo do usuário avança entre os passos do assistente (ex: Etapa 1: Dados; Etapa 2: Pagamento; Etapa 3: Ativação), a animação Lottie reproduz exatamente o segmento vetorial delimitado (ex: frames `[0, 45]` para o Passo 1, `[45, 90]` para o Passo 2), preenchendo filamentos de luz e iluminando o nó do próximo estágio com um pulso estroboscópico sutil.
* **Gatilho**: Mudança de rota ou alteração de estado no gerenciador do formulário (`currentStep`).
* **Onde Encaixar**: Carrinhos de compras multi-etapa, formulários de crédito e verificação KYC (*Know Your Customer*).
* **Anatomia dos Keyframes**: Composição segmentada em marcadores (*markers*): `segment1` (frames 0–45), `segment2` (frames 45–90), `segment3` (frames 90–135), com curvas assimétricas de chegada rápida `cubic-bezier(0.2, 0.8, 0.2, 1)`.

---

### 6. Dynamic Theming via Color Slot Swapping
* **Comportamento Visual**: Uma mesma animação complexa (ex: painel com gráficos, ilustrações de gráficos de barras e personagens) adapta suas cores em tempo real sem qualquer recarregamento de rede. Ao alternar entre a paleta corporativa da empresa (Azul Cobalto) e a paleta de alto contraste ou tema escuro (Neon Roxo / Preto Absoluto), as camadas vetoriais remapeiam dinamicamente suas cores internas de preenchimento e contorno diretamente via runtime.
* **Gatilho**: Alteração de variáveis CSS globais ou preferência de tema no sistema de design tokens.
* **Onde Encaixar**: Ilustrações centrais de produtos multi-tenant (SaaS white-label), interfaces com suporte a temas customizados pelo cliente.
* **Anatomia dos Keyframes**: Utilização de *Slots* na especificação dotLottie v2, onde identificadores de cor como `slot_primary_brand` e `slot_accent_glow` recebem novas matrizes RGBA em tempo de execução via API de theming.

---

### 7. Ambient Breathing Empty State (Loop de Baixa Amplitude)
* **Comportamento Visual**: Uma ilustração vetorial estilizada representando um cofre aberto ou uma mesa de trabalho vazia. Elementos secundários flutuam suavemente com uma física senoidal harmoniosa: folhas de papel oscilam verticalmente 4 pixels com períodos desfasados, uma xícara emite uma espiral de vapor sem costura (*seamless loop*) e o fundo pulsa com uma aura luminosa suave.
* **Gatilho**: Montagem inicial da tela com lista vazia (`data.length === 0`).
* **Onde Encaixar**: Caixas de entrada sem e-mails pendentes, pastas de arquivos vazias, resultados de busca não encontrados.
* **Anatomia dos Keyframes**: Loop contínuo de 120 frames (4 segundos a 30fps). Curvas de Bézier perfeitamente simétricas `cubic-bezier(0.45, 0.05, 0.55, 0.95)` para garantir transição suave e imperceptível entre o último frame e o primeiro frame.

---

### 8. Tactile Micro-Icon Burst (Like / Heart / Bookmark)
* **Comportamento Visual**: Ao clicar sobre o ícone desativado, o contorno sofre uma compressão instantânea de 20% no eixo vertical (*squash*). No milissegundo seguinte, o coração expande-se verticalmente para 130% do seu tamanho enquanto seu interior é preenchido com um vermelho carmesim vibrante; um anel de partículas pontiagudas explode ao redor e desaparece em cascata enquanto o corpo do coração assenta na escala 100% com duas pequenas oscilações de amortecimento.
* **Gatilho**: Evento de clique do usuário (`pointerdown` seguido de `pointerup`).
* **Onde Encaixar**: Botões de curtir em feeds sociais, botões de salvar produtos na lista de desejos, avaliações com estrelas.
* **Anatomia dos Keyframes**: Duração ultracompacta de 18 frames (300ms a 60fps). Frames 0 a 3 (Compressão/Squash); frames 4 a 9 (Estouro com escala 1.3x); frames 10 a 18 (Amortecimento elástico final com restDelta nulo).

---

### 9. Bidirectional Hover Rewind (Forward on Enter, Reverse on Leave)
* **Comportamento Visual**: Ao passar o cursor do mouse sobre um card de serviço ou botão de ação, a animação vetorial interna avança fluidamente até o fim (ex: uma chave inglesa se ajusta em um parafuso ou uma engrenagem gira 180 graus). Se o usuário remove o cursor no meio do caminho, a animação não salta nem recomeça: ela inverte a velocidade (`speed = -1` ou `setDirection(-1)`) e retrocede com precisão milimétrica exatamente a partir do frame atual até o repouso inicial.
* **Gatilho**: Eventos de `onMouseEnter` e `onMouseLeave`.
* **Onde Encaixar**: Cards de serviços em landing pages, botões de ação secundária, itens de menus suspensos (*dropdown items*).
* **Anatomia dos Keyframes**: Linha do tempo linear ou levemente desacelerada de 30 frames com direção controlada dinamicamente pelo runtime do player.

---

### 10. State Machine Branching Decision Tree (Botão Interativo de Ação)
* **Comportamento Visual**: Um elemento único que atua como um botão interativo multi-estado. Ele começa em `Idle`. Ao receber o clique, transita automaticamente para `Submitting` (onde se transforma em um anel vetorial girando infinitamente). Se a API externa responder com sucesso, a máquina de estado dispara o evento `onSuccess` e comuta para o ramo `Success` (check verde). Se houver erro de rede, comuta para `Error` (vibração lateral de alerta e triângulo de advertência piscando), retornando após 2 segundos ao estado `Idle`.
* **Gatilho**: Entradas disparadas por eventos de código (`stateMachineFire('success')` ou `stateMachineSetStringInput('state', 'error')`).
* **Onde Encaixar**: Botões de envio de formulários críticos, botões de checkout em um clique, acionadores de backup.
* **Anatomia dos Keyframes**: Grafo de estados gerenciado pelo arquivo `states/button_state_machine.json` dentro do contêiner `.lottie`, isolando toda a lógica de transição cinemática dentro do arquivo vetorial.

---

## 5. Matemática do Movimento & Receitas de Código

### A Matemática das Curvas Bézier Internas do Lottie

No arquivo JSON do Lottie, cada keyframe temporal possui uma estrutura formal que dita a velocidade instantânea do elemento. A conversão de uma curva CSS clássica `cubic-bezier(x1, y1, x2, y2)` para os vetores de tangente do Lottie mapeia-se da seguinte forma:

```json
{
  "t": 30,
  "s": [0],
  "e": [100],
  "o": { "x": [0.16], "y": [1.0] },
  "i": { "x": [0.30], "y": [1.0] }
}
```

* Onde:
  - `t`: Número do quadro (*time frame* em que a chave ocorre).
  - `s`: Valor inicial (*start value* no início do intervalo).
  - `e`: Valor final (*end value* no término do intervalo).
  - `o.x` e `o.y`: Coordenadas do ponto de controle de saída (análogas a `x1, y1` do CSS).
  - `i.x` e `i.y`: Coordenadas do ponto de controle de entrada (análogas a `x2, y2` do CSS).

#### Tabela de Curvas Cinemáticas de Referência

| Nome do Movimento | Expressão CSS Equivalente | Lottie Out (`o`) | Lottie In (`i`) | Sensação Física Transmitida |
| :--- | :--- | :--- | :--- | :--- |
| **Snappy Ease-Out (UI)** | `cubic-bezier(0.16, 1, 0.3, 1)` | `{x: 0.16, y: 1}` | `{x: 0.30, y: 1}` | Resposta tátil instantânea, sem atraso perceptível de clique. |
| **Anticipation Wind-Up** | `cubic-bezier(0.36, -0.2, 0.2, 1)` | `{x: 0.36, y: -0.2}` | `{x: 0.20, y: 1}` | Puxada elástica para trás antes de disparar para a frente. |
| **Elastic Overshoot** | `cubic-bezier(0.34, 1.56, 0.64, 1)` | `{x: 0.34, y: 1.56}`| `{x: 0.64, y: 1}` | Ultrapassa a posição final e retorna com estabilização elástica. |
| **Smooth Ambient Loop** | `cubic-bezier(0.45, 0.05, 0.55, 0.95)` | `{x: 0.45, y: 0.05}` | `{x: 0.55, y: 0.95}` | Harmônico, senoidal, ideal para respiração e flutuação. |

---

### Anatomia Interna do Contêiner `.lottie` (dotLottie v2)

Um arquivo `.lottie` nada mais é do que um arquivo ZIP renomeado contendo a seguinte árvore estrutural:

```
archive.lottie (ZIP Compressed)
├── manifest.json              # Configurações globais, versão do esquema, lista de animações
├── animations/
│   ├── main_animation.json    # Árvore vetorial pura serializada
│   └── alt_variation.json     # Variação alternativa da animação
├── states/
│   └── interaction_graph.json # Máquina de estados com listeners de hover, click e variáveis
├── themes/
│   ├── dark_theme.json        # Remapeamento de cores para modo escuro
│   └── brand_blue.json        # Remapeamento de cores para a identidade da marca
└── images/                    # Imagens rasterizadas embutidas (se houver, WebP/PNG)
    └── texture_alpha.webp
```

---

### Receita 1: Componente de Micro-Ícone Interativo de Produção em React

Este componente implementa:
1. Suporte nativo a `@lottiefiles/dotlottie-react` com ThorVG WebAssembly.
2. Detecção automática de acessibilidade (`prefers-reduced-motion`).
3. Otimização de performance com `IntersectionObserver` (pausa automática quando fora da tela).
4. Reprodução bidirecional inteligente no hover (Forward ao entrar, Reverse ao sair).

```tsx
import React, { useEffect, useRef, useState, useCallback } from 'react';
import { DotLottieReact } from '@lottiefiles/dotlottie-react';
import type { DotLottie } from '@lottiefiles/dotlottie-web';

interface InteractiveLottieIconProps {
  src: string;
  size?: number;
  label: string;
  triggerOnHover?: boolean;
  className?: string;
  onClick?: () => void;
}

export const InteractiveLottieIcon: React.FC<InteractiveLottieIconProps> = ({
  src,
  size = 32,
  label,
  triggerOnHover = true,
  className = '',
  onClick,
}) => {
  const containerRef = useRef<HTMLDivElement | null>(null);
  const dotLottieRef = useRef<DotLottie | null>(null);
  const [prefersReducedMotion, setPrefersReducedMotion] = useState(false);
  const [isIntersecting, setIsIntersecting] = useState(true);

  // 1. Verificação de Acessibilidade (prefers-reduced-motion)
  useEffect(() => {
    if (typeof window === 'undefined') return;
    const mediaQuery = window.matchMedia('(prefers-reduced-motion: reduce)');
    setPrefersReducedMotion(mediaQuery.matches);

    const handler = (event: MediaQueryListEvent) => {
      setPrefersReducedMotion(event.matches);
      if (event.matches && dotLottieRef.current) {
        dotLottieRef.current.pause();
      }
    };

    mediaQuery.addEventListener('change', handler);
    return () => mediaQuery.removeEventListener('change', handler);
  }, []);

  // 2. IntersectionObserver para Economia de CPU/Bateria fora da Viewport
  useEffect(() => {
    const target = containerRef.current;
    if (!target) return;

    const observer = new IntersectionObserver(
      ([entry]) => {
        const inView = entry.isIntersecting;
        setIsIntersecting(inView);
        if (dotLottieRef.current) {
          if (!inView) {
            dotLottieRef.current.pause();
          }
        }
      },
      { threshold: 0.1 }
    );

    observer.observe(target);
    return () => observer.disconnect();
  }, []);

  // 3. Callback de instância do runtime WASM
  const handleDotLottieCallback = useCallback((instance: DotLottie) => {
    dotLottieRef.current = instance;
    if (prefersReducedMotion) {
      // Se acessibilidade ativada, para no frame inicial estático
      instance.pause();
    }
  }, [prefersReducedMotion]);

  // 4. Controle bidirecional de Hover (Forward / Reverse)
  const handleMouseEnter = () => {
    if (!triggerOnHover || prefersReducedMotion || !dotLottieRef.current) return;
    dotLottieRef.current.setMode('forward');
    dotLottieRef.current.setSpeed(1.2);
    dotLottieRef.current.play();
  };

  const handleMouseLeave = () => {
    if (!triggerOnHover || prefersReducedMotion || !dotLottieRef.current) return;
    dotLottieRef.current.setMode('reverse');
    dotLottieRef.current.setSpeed(1.5);
    dotLottieRef.current.play();
  };

  return (
    <div
      ref={containerRef}
      role="button"
      tabIndex={0}
      aria-label={label}
      onClick={onClick}
      onKeyDown={(e) => {
        if (e.key === 'Enter' || e.key === ' ') {
          e.preventDefault();
          onClick?.();
        }
      }}
      onMouseEnter={handleMouseEnter}
      onMouseLeave={handleMouseLeave}
      className={`inline-flex items-center justify-center cursor-pointer select-none transition-transform duration-200 active:scale-95 focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-indigo-500 rounded-lg p-1.5 ${className}`}
      style={{ width: size, height: size }}
    >
      <DotLottieReact
        src={src}
        autoplay={false}
        loop={false}
        dotLottieRefCallback={handleDotLottieCallback}
        style={{ width: '100%', height: '100%' }}
      />
    </div>
  );
};
```

---

### Receita 2: Scroll-Linked Scrubbing com Suporte a Lenis Smooth Scroll

Esta implementação conecta a cabeça de reprodução do player vetorial diretamente à barra de rolagem contínua da página, criando uma experiência imersiva de *storytelling* com sincronização precisa a cada pixel rolado.

```tsx
import React, { useEffect, useRef } from 'react';
import { DotLottieReact } from '@lottiefiles/dotlottie-react';
import type { DotLottie } from '@lottiefiles/dotlottie-web';

interface ScrollScrubLottieProps {
  src: string;
  containerHeight?: string; // ex: "300vh" para scroll expandido
  className?: string;
}

export const ScrollScrubLottie: React.FC<ScrollScrubLottieProps> = ({
  src,
  containerHeight = '250vh',
  className = '',
}) => {
  const sectionRef = useRef<HTMLDivElement | null>(null);
  const dotLottieRef = useRef<DotLottie | null>(null);

  useEffect(() => {
    let animationFrameId: number;

    const handleScroll = () => {
      const element = sectionRef.current;
      const instance = dotLottieRef.current;
      if (!element || !instance) return;

      const rect = element.getBoundingClientRect();
      const windowHeight = window.innerHeight;
      const totalScrollableDistance = rect.height - windowHeight;

      if (totalScrollableDistance <= 0) return;

      // Calcula o progresso relativo do elemento na viewport (0.0 a 1.0)
      const currentScroll = -rect.top;
      const progress = Math.min(Math.max(currentScroll / totalScrollableDistance, 0), 1);

      // Converte o progresso percentual para o frame específico da animação
      const totalFrames = instance.totalFrames;
      if (totalFrames > 0) {
        const targetFrame = progress * totalFrames;
        // seek() posiciona instantaneamente a cabeça de reprodução sem lag
        instance.seek(targetFrame);
      }
    };

    const onScrollTick = () => {
      handleScroll();
      animationFrameId = requestAnimationFrame(onScrollTick);
    };

    // Inicia o loop de monitoramento sincronizado com requestAnimationFrame
    animationFrameId = requestAnimationFrame(onScrollTick);

    return () => {
      cancelAnimationFrame(animationFrameId);
    };
  }, []);

  return (
    <div
      ref={sectionRef}
      style={{ height: containerHeight }}
      className={`relative w-full ${className}`}
    >
      {/* Elemento fixo que permanece no centro da tela enquanto o container desce */}
      <div className="sticky top-0 left-0 w-full h-screen flex flex-col items-center justify-center overflow-hidden">
        <div className="w-full max-w-2xl aspect-square">
          <DotLottieReact
            src={src}
            autoplay={false}
            loop={false}
            dotLottieRefCallback={(instance) => {
              dotLottieRef.current = instance;
            }}
            style={{ width: '100%', height: '100%' }}
          />
        </div>
      </div>
    </div>
  );
};
```

---

### Receita 3: Botão Transacional Acionado por dotLottie State Machine

Esta receita utiliza a biblioteca nativa de **State Machine** contida na especificação `.lottie`, permitindo que o React despache eventos de alto nível (`submit`, `success`, `error`) e o motor WASM resolva as ramificações visuais internamente.

```tsx
import React, { useRef, useState } from 'react';
import { DotLottieReact } from '@lottiefiles/dotlottie-react';
import type { DotLottie } from '@lottiefiles/dotlottie-web';

interface StateMachineButtonProps {
  dotLottieSrc: string;
  stateMachineId: string;
  onConfirm: () => Promise<void>;
  label: string;
}

export const StateMachineTransactionButton: React.FC<StateMachineButtonProps> = ({
  dotLottieSrc,
  stateMachineId,
  onConfirm,
  label,
}) => {
  const dotLottieRef = useRef<DotLottie | null>(null);
  const [status, setStatus] = useState<'idle' | 'loading' | 'success' | 'error'>('idle');

  const handleClick = async () => {
    if (status === 'loading' || !dotLottieRef.current) return;

    try {
      setStatus('loading');
      // Dispara o evento de transição na State Machine interna do arquivo
      dotLottieRef.current.stateMachineFire('onSubmit');

      await onConfirm();

      setStatus('success');
      dotLottieRef.current.stateMachineFire('onSuccess');

      // Retorna para o estado normal após o feedback visual
      setTimeout(() => {
        setStatus('idle');
        dotLottieRef.current?.stateMachineFire('onReset');
      }, 2500);
    } catch {
      setStatus('error');
      dotLottieRef.current?.stateMachineFire('onError');

      setTimeout(() => {
        setStatus('idle');
        dotLottieRef.current?.stateMachineFire('onReset');
      }, 3000);
    }
  };

  return (
    <button
      onClick={handleClick}
      disabled={status === 'loading'}
      className="relative inline-flex items-center gap-3 px-6 py-3 font-semibold text-white bg-slate-900 hover:bg-slate-800 active:scale-98 rounded-xl shadow-lg transition-all duration-200 disabled:opacity-70 disabled:cursor-not-allowed border border-slate-700/60"
    >
      <span className="text-sm font-medium tracking-wide">{label}</span>
      
      {/* Contêiner de renderização da State Machine vetorial */}
      <div className="w-6 h-6 flex items-center justify-center pointer-events-none">
        <DotLottieReact
          src={dotLottieSrc}
          stateMachineId={stateMachineId}
          dotLottieRefCallback={(instance) => {
            dotLottieRef.current = instance;
          }}
          style={{ width: '100%', height: '100%' }}
        />
      </div>
    </button>
  );
};
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma interface que fará uso de animações vetoriais interativas, a Inteligência Artificial ou Engenheiro Líder deve especificar com clareza as fronteiras de tecnologia no documento arquitetural preliminar (`DESIGN_BLUEPRINT.md`).

---

### Matriz de Decisão: Qual Motor Escolher?

```
┌────────────────────────────────────────────────────────────────────────┐
│             ÁRVORE DE DECISÃO TÉCNICA DE MOTION NA WEB                 │
└────────────────────────────────────────────────────────────────────────┘
                                   │
              ¿O que está sendo animado na interface?
                                   │
     ┌─────────────────────────────┼─────────────────────────────┐
     ▼                             ▼                             ▼
Elementos de UI Layout     Ilustração Vetorial         Shaders / Cenas 3D
(Cards, Menus, Modais)     Complexa ou Personagens     (Partículas, Glitch)
     │                             │                             │
     ▼                             ▼                             ▼
Framer Motion / CSS        ¿Qual o formato da arte?      WebGL / Three.js
(Springs, LayoutId)                │
                    ┌──────────────┴──────────────┐
                    ▼                             ▼
             Arte Vetorial                Vídeo Fotorrealista
         com Transições Orgânicas         com Canal Alfa / Transparência
                    │                             │
                    ▼                             ▼
           LottieFiles / dotLottie           HTML5 <video>
            (@lottiefiles/dotlottie)          WebM (VP9) / MP4 (HEVC)
```

1. **Use Tailwind CSS / Framer Motion para**: Transições de layout discreto, modais abrindo, menus acordeão, listas reordenáveis e botões simples.
2. **Use LottieFiles (`.lottie`) para**: Ícones com morphing de traçados (*stroke morphing*), ilustrações contextuais com múltiplos elementos mecânicos sincronizados, mascotes com State Machine, telas de feedback de transação e empty states animados.
3. **Use Vídeo WebM Alpha para**: Cenas de renderização 3D fotorrealistas pré-computadas com sombras de oclusão e reflexos cáusticos que seriam impossíveis em vetores 2D.
4. **Use Three.js / WebGL Nativo para**: Modelos 3D com iluminação dinâmica em tempo real que precisam responder a órbitas livres de câmera.

---

### Orçamento de Performance & Hard Limits (Performance Budgets)

| Critério | Limite Recomendado | Limite Absoluto (Hard Limit) | Justificativa Técnica |
| :--- | :--- | :--- | :--- |
| **Formato de Arquivo** | `.lottie` (dotLottie v2) | JSON Puro (`.json`) | dotLottie reduz o payload em até 80% e suporta State Machines. |
| **Peso do Pacote (Tamanho)** | ≤ 30 KB por arquivo | 80 KB por arquivo | Mantém o tempo de transferência imperceptível em redes 3G/4G. |
| **Complexidade de Traçados** | ≤ 250 vértices Bézier | 600 vértices Bézier | Acima disso, a tesselação em tempo real eleva o tempo de frame. |
| **Instâncias Simultâneas** | 1 a 3 visíveis | Máximo de 5 visíveis | Previne exaustão de contextos gráficos no subsistema GPU do browser. |
| **Taxa de Quadros Base** | 60 FPS nativo | 30 FPS (para loops ambientais) | Reduz o cálculo contínuo de interpolação na CPU/WASM. |
| **Auto-Pausa Obrigatória** | 100% dos loops | Sem exceções | Todo loop contínuo DEVE pausar ao sair da viewport via observer. |

---

### Checklist de Implementação para o Blueprint Técnico

* [ ] **Formato Padronizado**: Todos os artefatos de motion vetorial devem ser fornecidos na extensão `.lottie` compilados com a especificação dotLottie v2.
* [ ] **Biblioteca Homologada**: Uso exclusivo de `@lottiefiles/dotlottie-react` (com runtime ThorVG WASM). Banir expressamente o pacote legado `lottie-react` / `lottie-web` baseado em SVG puro em novas implementações.
* [ ] **Acessibilidade em Primeiro Lugar**:
  - [ ] Implementar verificação de `(prefers-reduced-motion: reduce)`.
  - [ ] Fornecer texto alternativo com `aria-label` e `role="img"`, ou marcar com `aria-hidden="true"` caso decorativo.
* [ ] **Virtualização de Recursos**: Em listagens dinâmicas, players fora da tela devem ser destruídos ou mantidos em pausa via `IntersectionObserver`.
* [ ] **Auditoria de Memória**: Garantir que o `unmount` do componente React acione `dotLottie.destroy()` para evitar fugas de memória na memória linear do WebAssembly.
