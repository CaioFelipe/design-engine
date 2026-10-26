---
id: "transitions-dev"
name: "Transitions.dev (UI Transitions & View Transitions Architecture)"
url: "https://transitions.dev/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["Micro-Focal Cross-Blur", "Asymmetric Timing & Easing", "Origin-Aware Spatial Anchoring", "Hardware-Accelerated View Transitions", "FLIP Surface Morphing", "Craft Kinetic Physics"]
densidade_informacao: "Alta"
impacto_visual: "Moderado a Cinematografico/Showstopper"
custo_computacional: "Baixo (CSS Nativo, GPU Compositor & View Transitions API)"
stack_frameworks: ["CSS Nativo (CSS Custom Properties & Tokens)", "View Transitions API (Level 1 & Level 2)", "Vanilla TypeScript / JavaScript", "React 19 / 18", "Next.js / Astro / Remix", "Tailwind CSS (v3 / v4)", "AI Agent Skill (transitions-dev)"]
compatibilidade:
  combinacoes_recomendadas: ["Transitions.dev Motion Tokens + Tailwind CSS Design System", "W3C View Transitions API + React Router / Next.js App Router", "Cross-Blur Microinteractions + Radix UI / Shadcn Primitives", "FLIP Surface Morphing + CSS Grid Template Rows (0fr -> 1fr)", "Transitions.dev + Lenis Smooth Scroll para orquestração de página inteira"]
  conflitos_esteticos: ["Animação simultânea de layout (width/height brutos sem transform/grid) gerando continuous reflow e layout thrashing", "Filtros de blur excessivos (>10px) acumulados em listas densas em telas de baixa potência", "Simetria temporal artificial (mesma duração e curva para abrir e fechar popups)", "Ignorar media query prefers-reduced-motion em animações com escala e translação abruptas"]
---

# Transitions.dev — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)

Na engenharia moderna de interfaces, a maioria das bibliotecas de animação cai em um de dois extremos problemáticos: de um lado, bibliotecas com runtimes JavaScript pesados que tentam controlar o loop de renderização via *main thread*, gerando atrasos (*input latency*) e *frame drops*; do outro, implementações CSS genéricas com transições lineares simétricas (`ease-in-out` de 300ms idêntico para abrir e fechar), que conferem à interface uma sensação plástica, estéril e desajeitada.

O projeto **Transitions.dev**, idealizado e desenvolvido pelo *design engineer* **Jakub Antalík**, introduz uma abordagem artesanal de nível *high-end craft* aliada à máxima eficiência de hardware. O ecossistema foi construído sobre uma premissa fundamental: **o movimento de excelência não busca chamar atenção para si, mas fornecer pistas táteis e espaciais intuitivas que confirmem a intenção do usuário antes que o cérebro processe o atraso cognitivo**.

```
+---------------------------------------------------------------------------------------------------+
|                            TRANSITIONS.DEV — FILOSOFIA DE MOVIMENTO CRAFT                         |
+-------------------------------------------------+-------------------------------------------------+
|          MICRO-FOCAL CROSS-BLUR                 |       ASSIMETRIA TEMPORAL & ESPACIAL            |
| - Interpolação óptica de 1px a 3px de blur      | - Entrada: Intencional, elástica e expressiva   |
| - Mascara artefatos de renderização de subpixel |   (~250-400ms, overshoot, anticipation)        |
| - Simula persistência retiniana e foco de lente | - Saída: Rápida, concisa e desvanecente         |
|                                                 |   (~150-250ms, desaceleração suave sem rebote)  |
+-------------------------------------------------+-------------------------------------------------+
|       ORIGIN-AWARE ANCHORING                    |      VIEW TRANSITIONS API & FLIP NATIVO         |
| - Elementos flutuantes nascem do ponto de clique| - Morphing contínuo de superfícies (FAB -> Menu)|
| - Transform-origin dinâmico (top-center, etc.)  | - Transição entre telas com 0 KB de runtime JS  |
| - Continuidade da matéria (sem teleportes)      | - Renderização direta na Compositor Thread      |
+-------------------------------------------------+-------------------------------------------------+
```

### Os 4 Pilares da Engenharia Sensorial do Transitions.dev:

1. **Micro-Focal Cross-Blur (A Dissolução Óptica Suave)**:
   Em vez de transições secas de opacidade (`0 -> 1`), o Transitions.dev combina微-translações espaciais (de 4px a 12px) com um leve desfoque gaussiano de transição (`blur(1px)` a `blur(3px)`). Esse padrão simula a física de uma lente óptica ajustando seu foco de profundidade (*rack-focus*). O resultado elimina o efeito estroboscópico de textos ou ícones trocando bruscamente, transformando mudanças de estado num deslize contínuo e sedoso para o olho humano.

2. **Assimetria Temporal Rigorosa (Entrada vs. Saída)**:
   Na natureza, objetos levam tempo e energia para acelerar e chegar a um ponto de repouso, mas a gravidade ou uma colisão os retira rapidamente. No Transitions.dev, **aberturas e fechamentos nunca compartilham a mesma curva nem a mesma duração**:
   - **Abertura / Entrada**: Leva de 250ms a 400ms, utilizando curvas de desaceleração suave com amortecimento ou leve overshoot (`cubic-bezier(0.22, 1, 0.36, 1)` ou `cubic-bezier(0.34, 1.25, 0.64, 1)`). O usuário acabou de clicar e está esperando o conteúdo aparecer, apreciando a continuidade espacial.
   - **Fechamento / Saída**: Leva de 150ms a 250ms, com saída limpa e sem oscilações (`cubic-bezier(0.22, 1, 0.36, 1)` ou saída direta com escala sutil de 0.99). O usuário já cumpriu sua tarefa e quer a tela limpa imediatamente; animações de saída lentas criam frustração e sensação de lentidão no sistema.

3. **Ancoragem Espacial Ciente da Origem (*Origin-Aware Growth*)**:
   Menús suspensos, popovers e diálogos contextuais não surgem aleatoriamente do centro da tela. O ponto de escala (`transform-origin`) é rigidamente alinhado com o elemento gatilho (por exemplo, `top center` ou `top right`). Quando o menu se expande de `scale(0.97)` para `scale(1.0)`, a ilusão física transmitida é a de que a nova superfície de material foi fisicamente projetada pelo próprio botão gatilho.

4. **Transição de Superfície Contínua (Morphing & View Transitions)**:
   Em fluxos de navegação (como lista para detalhe, ou botão FAB circular que se desdobra em painel), a interface rejeita a destruição e reconstrução cega de nós DOM. Através da **View Transitions API (W3C)** e de técnicas avançadas de FLIP em CSS (`grid-template-rows: 0fr -> 1fr`, interpolação de `border-radius: 40px -> 20px`), o contêiner se metamorfoseia enquanto o conteúdo interno faz cross-fade, garantindo que o cérebro do usuário nunca perca o fio condutor da navegação.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários

1. **Aplicações Web B2B & Ferramentas SaaS de Alta Densidade (Linear, Raycast, Vercel, Supabase)**:
   - **Command Menus & Origin-Aware Dropdowns**: Menus contextuais e seletores que se expandem instantaneamente sem bloquear a thread principal.
   - **Segmented Controls & Tabs com Pill Deslizante**: Alternância entre abas de projeto, filtros de tabela e visualizações analíticas com feedback cinético preciso.
   - **Input Shake & Feedback de Validação com Auto-Reversão**: Alertas de erro em formulários de autenticação ou chaves de API onde o input oscila elasticamente e decai de volta ao estado neutro de forma orgânica.
2. **Interfaces Centradas em IA e Agentes Autônomos (Chatbots, Reasoning Canvases, Workflows IA)**:
   - **AI Thinking States com Shimmer Sweep**: Linhas de status de raciocínio de agentes ("Pensando...", "Indexando base vetorial...", "Escrevendo código...") com gradiente reluzente contínuo e troca suave de frases via *text-swap blur*.
   - **Streaming Text Token Reveal**: Renderização de tokens e palavras de modelos de linguagem (LLMs) surgindo com micro-blur individual de 1px a cada 60ms, eliminando o piscar agressivo do streaming em texto puro.
   - **Reasoning Stream Transcript**: Janela de histórico de pensamentos do agente que rola fluidamente 2 linhas por ciclo, mascarando bordas superior e inferior com gradientes alfa (*mask-image*).
3. **E-commerce Flagship, FinTech & Dashboards Financeiros**:
   - **Odometer / Spinning Reel Counter**: Contadores numéricos que giram como roletas mecânicas com desfoque de movimento vertical (`spin blur`) ao atualizar saldos bancários, cotações ou métricas em tempo real.
   - **Card-to-Page View Transitions**: Ao clicar em um produto na vitrine, o cartão expande suavemente suas dimensões até cobrir a tela inteira, fundindo o título e a imagem na página de checkout.
4. **Sistemas de Notificação & Centrais de Atividade**:
   - **Sonner-Style Banner Stacking**: Notificações empilhadas em profundidade z-index, onde novos avisos empurram os antigos para o fundo com escala reduzida (`0.94`, `0.88`), opacidade decrescente e desfoque óptico progressivo (`1px`, `2px`).

### Papel no Ritmo Visual (Regra 60-30-10)

```
+---------------------------------------------------------------------------------------------------+
|                            DISTRIBUIÇÃO CINÉTICA — REGRA 60-30-10                                 |
+-----------------------------------+-----------------------------------+---------------------------+
|      60% — ESTRUTURA ESTÁVEL      |    30% — MICRO-FLUIDEZ TÁTIL      |  10% — SHOWSTOPPER MORPH  |
| - Layout neutro e descansado      | - Dropdowns origin-aware (250ms)  | - FAB expandindo em Menu  |
| - Tipografia fixa e legível       | - Pill de abas deslizante         | - View Transition Card-Pág|
| - Sem transformações parasitas    | - Cross-blur text swaps (150ms)   | - Odometer reel counter   |
| - Foco na leitura sem distração   | - Toasts com elevação de 16px     | - Avatar group spring-wave|
+-----------------------------------+-----------------------------------+---------------------------+
```

- **60% — Estrutura Estática e Arquitetura Neutra**:
  A base da interface. Superfícies sólidas (`bg-zinc-950` / `bg-white`), grids bem estruturados, textos de parágrafo e botões secundários em estado de repouso absoluto. A interface não deve tremer ou vibrar sem uma ação humana expressa.
- **30% — Fluidez Funcional e Micro-Feedback (Invisível aos Olhos, Sentido nos Dedos)**:
  O coração do Transitions.dev. Transições imperceptíveis que operam abaixo do limiar de distração consciente:
  - Expansão de dropdowns com `transform-origin` ciente do gatilho (250ms);
  - Deslizamento elástico da pílula ativa em abas de navegação;
  - Micro-blur de 2px na transição de textos em botões ("Salvar" para "Salvo");
  - Subida suave de toasts com elevação de 16px e desfoque inicial de 2px;
  - Troca de ícone de check/copiar com escala de 0.25 e desfoque suave.
- **10% — Espetáculo Visual & Morphing Estrutural (Showstopper)**:
  Momentos de alta densidade cinemática reservados para transições de estado profundas:
  - O botão de ação flutuante (+) que se expande organicamente em um painel de criação completo;
  - A View Transition que transforma um card da listagem na página interna de detalhes;
  - A explosão radial com física de molas do botão de Like e o contador slot-machine.

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Quando Evitar (Anti-Padrões de Movimento)

1. **Animação Contínua de Propriedades de Layout (Reflow / Layout Thrashing)**:
   - **PROIBIÇÃO ABSOLUTA**: Nunca anime diretamente `width`, `height`, `top`, `left`, `margin` ou `padding` utilizando `transition: all` ou seletores genéricos em elementos que possuam nós filhos com textos ou imagens pesadas. Fazer isso obriga o navegador a recalcular a geometria da árvore inteira a cada frame.
   - **Solução Transitions.dev**: Para expansão de altura (como em accordions e gavetas), utilize **CSS Grid** com interpolação de `grid-template-rows: 0fr -> 1fr`, que é processada de maneira otimizada pelo motor de layout sem medir alturas via JavaScript (`element.scrollHeight`). Para caixas com dimensões flexíveis, empregue matrizes de escala composta em GPU (`transform: scale(...)`).
2. **Abuso de Filtros Gráficos em Listas Extensas (GPU Fill-Rate Exhaustion)**:
   - O uso de `filter: blur(...)` é a marca registrada do visual Transitions.dev, mas seu custo de fragment shader na GPU é considerável em telas de alta densidade (Retina/OLED móvel).
   - **Diretriz**: Mantenha o blur estritamente contido entre `1px` e `3px` e com duração máxima de 250ms. Nunca aplique classes de blur permanente ou em listas com centenas de linhas renderizadas simultaneamente.
3. **Simetria Temporal em Diálogos e Modais**:
   - Configurar o modal para fechar com a mesma velocidade ou com rebote elástico na saída gera a sensação de "software teimoso", onde o usuário precisa esperar a interface sumir para retomar o raciocínio.
4. **Falta de Desacoplamento em View Transitions com Scroll Ativo**:
   - Ao disparar `document.startViewTransition()`, o navegador captura snapshots da raiz ou dos elementos nomeados. Se houver rolagem intensa ou animações de fundo em loop durante o congelamento do snapshot, o usuário notará um congelamento momentâneo de 1 frame.

### ⚠️ Regras de Acessibilidade & GPU

1. **Blindagem Rigorosa contra Cinetose (`prefers-reduced-motion`)**:
   - Cada um dos componentes e utilitários deve respeitar a preferência de redução de movimento do sistema operacional. As transformações geométricas (escalas, translações, rotações e blurs) devem ser instantaneamente zeradas, mantendo exclusivamente um fade rápido de opacidade ou transição imediata de estado:
   ```css
   @media (prefers-reduced-motion: reduce) {
     *,
     *::before,
     *::after {
       animation-duration: 0.01ms !important;
       animation-iteration-count: 1 !important;
       transition-duration: 0.01ms !important;
       scroll-behavior: auto !important;
     }
     
     .t-morph,
     .t-dropdown,
     .t-page-slide,
     .t-banner-stack {
       transform: none !important;
       filter: none !important;
     }
   }
   ```
2. **Controle de `will-change` e Isolamento de Camadas**:
   - Não adicione `will-change: transform, opacity` globalmente na folha de estilos. Isso consome a memória de textura da GPU desnecessariamente.
   - Aplique `will-change` apenas durante o estado ativo de transição (ex: `.is-animating { will-change: transform, opacity, filter; }`) e remova-o assim que a animação entrar em repouso.

---

## 4. Catálogo Detalhado de Componentes, Padrões & Efeitos Notáveis

Abaixo estão especificados **12 padrões fundamentais** do ecossistema Transitions.dev e da arquitetura de View Transitions modernas, detalhando anatomia, curvas, gatilhos e integração.

```
+---------------------------------------------------------------------------------------------------+
|                           CATÁLOGO DE COMPONENTES & PADRÕES TRANSITIONS.DEV                       |
+----+-------------------------------+---------------------------+----------------------------------+
| #  | PADRÃO / COMPONENTE           | MECÂNICA PRINCIPAL        | GATILHO & APLICAÇÃO              |
+----+-------------------------------+---------------------------+----------------------------------+
| 01 | View Transitions Card-to-Page | Shared-Element Snapshot   | Navegação de Rota / Click Card   |
| 02 | Origin-Aware Menu Dropdown    | Anchored Scale + Blur     | Click em Botão / Menu de Opções  |
| 03 | Plus-to-Menu Morph (FAB)      | Surface Box & Radius FLIP | Click no FAB de Criação (+)      |
| 04 | Fluid Card Resize             | Grid 0fr->1fr & Smooth Max| Toggle de Detalhes / Expansão    |
| 05 | Soft Text States Swap         | Optical Micro Cross-Blur  | Ação de Botão (Save -> Saved)    |
| 06 | Orchestrated Success Check    | 5-Phase Staggered Entrance| Confirmação de Sucesso / Pagto   |
| 07 | Sonner-Style Banner Stacking  | Receding Depth Z-Queue    | Notificação / Toast Disparado    |
| 08 | Dynamic Error Input Shake     | Multi-Phase Decay Wave    | Falha de Validação de Input      |
| 09 | Segmented Sliding Tabs        | Continuous Pill Physics   | Alternância de Abas / Filtros    |
| 10 | AI Thinking & Shimmer Stream  | Linear Gradient Mask Run  | Estados de Raciocínio de Agentes |
| 11 | Avatar Group Falloff Spring   | Radial Neighbor Wave Lift | Hover em Lista de Usuários       |
| 12 | Kinetic Spinning Counter      | Slot-Machine Strip Reel   | Atualização de Saldo ou Métricas |
+----+-------------------------------+---------------------------+----------------------------------+
```

---

### 1. View Transitions API: Card-to-Page Morphing (Same-Document & Cross-Document)
- **Comportamento Visual**: Ao clicar em um card em uma grade de conteúdo, a imagem e o título do card não são destruídos: eles se expandem continuamente no espaço euclidiano até assumirem a largura total e a tipografia de destaque da página de destino. O restante do conteúdo da página anterior desvanece suavemente enquanto os novos parágrafos emergem com um leve desfoque óptico ascendente.
- **Anatomia & Especificação**:
  - CSS Property: `view-transition-name: hero-card-image` e `view-transition-name: hero-card-title`.
  - Pseudo-elementos W3C: `::view-transition-group(*)`, `::view-transition-old(*)`, `::view-transition-new(*)`.
  - Suporte Cross-Document (MPA): `@view-transition { navigation: auto; }`.
- **Gatilho**: Disparo programático via `document.startViewTransition(() => updateDOM())` em SPAs ou transição automática entre páginas no Chrome/Edge/Safari Technology Preview.

### 2. Origin-Aware Menu Dropdown (`t-dropdown`)
- **Comportamento Visual**: O menu suspenso não salta abruptamente para a tela; ele "cresce" diretamente do botão que o disparou. A escala inicia em `0.97`, a opacidade em `0` e há um desfoque de `2px`. À medida que abre, ele viaja para a posição final com `cubic-bezier(0.22, 1, 0.36, 1)` em `250ms`. Ao fechar, ele contrai suavemente para `0.99` e desaparece em apenas `150ms`.
- **Anatomia**:
  - `transform-origin: top center` (ou `top right` de acordo com a posição do trigger).
  - Camada de material com sombra de três níveis: `0 4px 42px rgba(0,0,0,0.06)`, `0 2px 6px rgba(0,0,0,0.05)`, anel de `1px rgba(0,0,0,0.06)`.
- **Gatilho**: Evento de click ou toggle de `aria-expanded="true"` com atributo `data-open="true"`.

### 3. Plus-to-Menu Surface Morph (`t-morph`)
- **Comportamento Visual**: Um botão de ação flutuante (+) circular (`40x40px`, `border-radius: 40px`) é clicado. Em vez de abrir um menu separado, **o próprio botão se transforma no menu**: suas dimensões expandem para `183x172px`, seu raio suaviza para `20px` com uma curva elástica com overshoot (`cubic-bezier(0.34, 1.25, 0.64, 1)` em `350ms`), enquanto o ícone central de cruz rotaciona `45deg` e se dissolve, dando lugar aos itens de ação que deslizam de baixo para cima com desfoque de `2px`.
- **Anatomia**: Elemento pai relativo que atua como máscara de transição para o estado fechado e aberto, orquestrado puramente via CSS Custom Properties.
- **Gatilho**: Clique do usuário em botões de "Novo Item", "Criar" ou Floating Action Buttons.

### 4. Fluid Card Resize sem Layout Thrashing (`t-card-resize`)
- **Comportamento Visual**: Uma área de card ou painel de tarefas muda de tamanho quando o usuário aciona uma visualização expandida ou insere dados adicionais. O contêiner interpola sua altura e largura com amortecimento `smooth-out` de `300ms`, sem saltos abruptos de scroll e sem quebras visuais nos componentes adjacentes.
- **Anatomia**: Implementação baseada em `grid-template-rows: 0fr -> 1fr` em conjunto com `transition: grid-template-rows 300ms cubic-bezier(0.22, 1, 0.36, 1)`.
- **Gatilho**: Abertura de gavetas internas, seções sanfonadas ou filtros avançados em tabelas.

### 5. Soft Text States Swap & Text Morph (`t-text-morph` / `t-text-swap-soft`)
- **Comportamento Visual**: Quando o texto de um botão ou badge muda (por exemplo, de "Copiar Código" para "Copiado!"), o texto antigo não é substituído abruptamente. O valor antigo viaja `-4px` para cima enquanto desfoca `2px` e se dissolve; simultaneamente, o novo texto emerge de `+4px` abaixo com o mesmo desfoque, estabilizando no centro em `150ms`. No modo `text-morph`, letras que ambos os textos compartilham permanecem paradas no lugar, enquanto apenas os caracteres divergentes realizam o cross-blur.
- **Anatomia**: Dois elementos `span` absolutos sobrepostos dentro de um wrapper relativo com `inline-flex` e overflow controlado.
- **Gatilho**: Disparo de ação do usuário (cópia de link, salvamento assíncrono, troca de unidade de medida em tabelas).

### 6. Orchestrated Success Check (`t-success-check`)
- **Comportamento Visual**: Padrão de celebração de fechamento de tarefa (pagamento aprovado, commit enviado, deploy concluído). Compõe 5 micro-transições paralelas na entrada:
  1. *Fade de Opacidade*: `0 -> 1` em `500ms`.
  2. *Rotação Angular*: Inicia em `80deg` e trava em `0deg`.
  3. *Salto Balístico Vertical (Y-bob)*: Sobe `-40px` com curva elástica de overshoot (`cubic-bezier(0.34, 1.35, 0.64, 1)`).
  4. *Focal De-Blur*: Desfoque de `10px` decai até `0px`.
  5. *Desenho Vetorial do SVG*: O traço da marca de verificação desenha-se via `stroke-dasharray` e `stroke-dashoffset` com atraso de `80ms`.
  - *Saída*: Utiliza apenas 3 sub-transições (fade suave, leve blur de 4px e recolhimento do traço), desvanecendo calmamente sem rebote.
- **Gatilho**: Conclusão de uma promise assíncrona com status 200/OK.

### 7. Sonner-Style Banner Stacking (`t-banner-stack`)
- **Comportamento Visual**: Notificações empilhadas na base da tela. Quando chega uma nova notificação, ela sobe de baixo com elevação de `60px` e escala inicial de `0.97`. As notificações anteriores não desaparecem: elas recuam em profundidade. O segundo banner recua `-12px`, reduz escala para `0.94`, recebe `opacity: 0.8` e desfoque óptico de `1px`. O terceiro recua `-24px`, escala para `0.88`, opacidade `0.6` e desfoque de `2px`.
- **Efeito Hover Interativo**: Ao passar o cursor sobre a pilha, os banners se desdobram verticalmente em uma lista separada por `8px`, restaurando escala `1.0`, opacidade total e nitidez óptica imediata.
- **Gatilho**: Disparo de evento do sistema (`toast.success()`, `toast.error()`).

### 8. Dynamic Error Input Shake com Auto-Reversão (`t-shake`)
- **Comportamento Visual**: Ao submeter um formulário inválido, o campo de entrada não exibe apenas um texto estático vermelho: ele oscila horizontalmente em uma coreografia de 4 fases com durações decrescentes (`80ms + 80ms + 60ms + 60ms = 280ms total`), utilizando amplitudes de `6px` e `4px`. Simultaneamente, a borda do input e a mensagem de erro assumem a tonalidade de erro (`#e23014`). Após `3000ms`, a borda e a mensagem revertem sozinhas para as cores neutras ao longo de `280ms`.
- **Anatomia**: Keyframe `translateX` com controle de suavização per-segmento e classe de transição temporizada via CSS/JS.
- **Gatilho**: Validação com falha no submit ou evento `onInvalid`.

### 9. Segmented Sliding Tabs com Indicador Ativo (`t-tabs-sliding`)
- **Comportamento Visual**: Em controles segmentados e abas de navegação, a pílula de destaque de fundo nunca pisca ou recria a si mesma ao alternar de aba. Ela desliza horizontalmente de uma aba para a outra com a curva `cubic-bezier(0.22, 1, 0.36, 1)` em `250ms`, ajustando dinamicamente sua largura conforme o tamanho do rótulo de texto. O texto da aba ativa transiciona de cor escura para alto contraste.
- **Anatomia**: Elemento `.pill` posicionado de forma absoluta por trás dos botões das abas, orientado pelas coordenadas de `offsetLeft` e `offsetWidth` ou implementado via View Transitions `view-transition-name: active-tab-pill`.
- **Gatilho**: Clique em aba ou navegação pelo teclado (`ArrowLeft` / `ArrowRight`).

### 10. AI Thinking & Reasoning Shimmer Stream (`t-ai-thinking` / `t-reasoning-stream`)
- **Comportamento Visual**: Para agentes de inteligência artificial, o Transitions.dev define dois padrões complementares:
  1. *Thinking States Shimmer*: A linha de texto ("Lendo repositório...") mantém um gradiente mascarado que viaja infinitamente a cada `2000ms`, transitando entre `#7c7c7c` e `#0d0d0d`. Ao trocar de estado mental, a frase inteira executa um *text-swap blur* de `150ms` e continua reluzindo.
  2. *Reasoning Stream Window*: Uma caixa compacta com máscaras de desfoque alfa no topo e na base (`mask-image: linear-gradient(...)`) que rola duas linhas de raciocínio por ciclo com pausas rítmicas de `840ms` e passos de interpolação suave de `500ms`.
- **Gatilho**: Execução em segundo plano de LLMs e chamadas de ferramentas de agentes autônomos.

### 11. Avatar Group Hover Spring com Atenuação Radial (`t-avatar-group`)
- **Comportamento Visual**: Em uma fila horizontal de avatares sobrepostos (como membros de uma equipe ou colaboradores de um documento), ao passar o cursor sobre qualquer avatar, este se eleva verticalmente `-4px` e expande em `1.05`. Crucialmente, os avatares vizinhos não ficam estáticos: eles recebem uma onda de elevação proporcional à sua distância $d$, calculada pela fórmula de atenuação física $\text{lift} \times (0.45)^d$. Ao retirar o mouse, o retorno utiliza uma mola com forte rebote elástico (`cubic-bezier(0.34, 3.85, 0.64, 1)`).
- **Gatilho**: Evento `pointerenter` e `pointerleave` no elemento filho da pilha de avatares.

### 12. Kinetic Spinning Counter (Odometer / Slot-Machine - `t-spinning-counter`)
- **Comportamento Visual**: Ao atualizar valores monetários ou contadores de métricas, cada dígito é representado por uma coluna vertical com algarismos de `0` a `9`. A coluna roda velozmente por 3 voltas completas (`--spins: 3`) e desacelera suavemente até travar no número alvo com a curva de amortecimento exponencial `cubic-bezier(0.16, 1, 0.3, 1)`. Durante o pico de rotação, um desfoque direcional vertical de `3px` é aplicado na coluna e desaparece gradualmente quando cada reel estaciona. As colunas aterrissam com um escalonamento da esquerda para a direita de `90ms`.
- **Gatilho**: Mutação de valores de props em dashboards ou conclusão de transações bancárias.

---

## 5. Matemática do Movimento & Receitas de Código

### Parâmetros Físicos & Curvas Exatas do Transitions.dev

A consistência de um design system de movimento depende da padronização matemática de suas curvas de Bézier e tempos de resposta. O Transitions.dev define um conjunto semântico estrito de constantes:

```css
:root {
  /* ========================================================================= */
  /* ESCALA TEMPORAL PRIMÁRIA                                                  */
  /* ========================================================================= */
  --duration-stagger:   40ms;   /* Escalonamento fino entre linhas de texto     */
  --duration-micro:     80ms;   /* Delay de path SVG, micro-shake de erro       */
  --duration-quick:     150ms;  /* Fechamento de modal, text-swap, saída rápida */
  --duration-fast:      250ms;  /* Abertura de dropdown, troca de abas, páginas */
  --duration-medium:    350ms;  /* Fechamento de painel lateral, subida toast   */
  --duration-slow:      400ms;  /* Abertura de painéis, revelação de skeleton   */
  --duration-very-slow: 500ms;  /* Momentos de celebração, badge pop-in         */

  /* ========================================================================= */
  /* CURVAS DE BÉZIER & FÍSICA CINÉTICA                                        */
  /* ========================================================================= */
  /* Smooth Out Canônico: Usado em 80% das transições de entrada e posicionamento */
  --ease-smooth-out: cubic-bezier(0.22, 1, 0.36, 1);

  /* Bounce Elástico Suave: Usado em badges, pops de notificação e ícones */
  --ease-bounce: cubic-bezier(0.34, 1.36, 0.64, 1);

  /* Bounce Forte de Retorno: Usado no retorno de avatares e molas táteis */
  --ease-bounce-strong: cubic-bezier(0.34, 3.85, 0.64, 1);

  /* Snappy Surface Expansion: Usado na metamorfose do botão FAB em painel */
  --ease-morph-open: cubic-bezier(0.34, 1.25, 0.64, 1);

  /* Desaceleração Exponencial de Inércia: Usada nas roletas do Odometer */
  --ease-reel-decelerate: cubic-bezier(0.16, 1, 0.3, 1);

  /* Transição de Fechamento: Saída sem atraso cognitivo */
  --ease-close-clean: cubic-bezier(0.4, 0, 0.2, 1);

  /* ========================================================================= */
  /* MATRIZ ÓPTICA DE DESFOQUE & DISTÂNCIAS                                    */
  /* ========================================================================= */
  --blur-micro:  1px;   /* Streaming de tokens LLM                             */
  --blur-small:  2px;   /* Troca de texto, ícones, menus e painéis              */
  --blur-medium: 3px;   /* Deslizamento de tela e desfoque vertical de rotação  */
  --blur-large:  8px;   /* Checkmark de celebração de sucesso                   */

  --distance-micro:  4px;   /* Micro-deslocamento de texto                      */
  --distance-small:  6px;   /* Balanço de erro em inputs                        */
  --distance-base:   8px;   /* Deslocamento de páginas e números                */
  --distance-medium: 12px;  /* Revelação de blocos e títulos                    */
  --distance-large:  30px;  /* Elevação de modais e badges                      */
}
```

---

### Receita de Código 1: Arquitetura W3C View Transitions API (Same-Document & Card-to-Page Morphing)

Este componente demonstra a integração moderna da **View Transitions API** no React 19 / TypeScript, permitindo o morphing de um card de catálogo para a página de detalhes com fallback gracioso para navegadores que não suportam a API nativa.

```tsx
import React, { useState } from 'react';

interface ArticleItem {
  id: string;
  title: string;
  category: string;
  summary: string;
  image: string;
}

const SAMPLE_DATA: ArticleItem[] = [
  {
    id: "motion-arch",
    title: "Arquitetura de View Transitions em Alta Fidelidade",
    category: "Design Engineering",
    summary: "Como eliminar o jank de navegação web descarregando animações para o compositor gráfico da GPU.",
    image: "https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?w=800&q=80"
  },
  {
    id: "cross-blur",
    title: "O Segredo Óptico do Micro Cross-Blur",
    category: "Percepção Visual",
    summary: "Simulando profundidade de campo cinematográfica em microinterações cotidianas de UI.",
    image: "https://images.unsplash.com/photo-1634017839464-5c339ebe3cb4?w=800&q=80"
  }
];

export function ViewTransitionShowcase() {
  const [activeArticle, setActiveArticle] = useState<ArticleItem | null>(null);

  // Helper que dispara a View Transition se o browser suportar
  const navigateWithTransition = (article: ArticleItem | null) => {
    if (!document.startViewTransition) {
      // Fallback para navegadores sem suporte nativo
      setActiveArticle(article);
      return;
    }

    // Executa a transição de estado encapsulada na View Transitions API
    document.startViewTransition(() => {
      setActiveArticle(article);
    });
  };

  return (
    <div className="min-h-[500px] w-full bg-[#fdfdfd] dark:bg-[#121212] p-8 text-[#0d0d0d] dark:text-[#ffffff] font-sans antialiased">
      <style>{`
        /* Configuração de Nomes de View Transition Declarativos */
        .vt-image {
          view-transition-name: var(--vt-tag-img, none);
        }
        .vt-title {
          view-transition-name: var(--vt-tag-title, none);
        }

        /* Estilização Customizada dos Pseudo-Elementos da API */
        ::view-transition-group(article-img-active),
        ::view-transition-group(article-title-active) {
          animation-duration: 350ms;
          animation-timing-function: cubic-bezier(0.22, 1, 0.36, 1);
        }

        ::view-transition-old(article-img-active),
        ::view-transition-new(article-img-active) {
          /* Garante que o aspecto da imagem não seja distorcido no morph */
          object-fit: cover;
          height: 100%;
        }

        /* Cross-blur suave na transição de saída e entrada da raiz */
        ::view-transition-old(root) {
          animation: 200ms cubic-bezier(0.22, 1, 0.36, 1) both vt-fade-out;
        }
        ::view-transition-new(root) {
          animation: 250ms cubic-bezier(0.22, 1, 0.36, 1) both vt-fade-in;
        }

        @keyframes vt-fade-out {
          from { opacity: 1; filter: blur(0px); }
          to { opacity: 0; filter: blur(2px); }
        }
        @keyframes vt-fade-in {
          from { opacity: 0; filter: blur(2px); }
          to { opacity: 1; filter: blur(0px); }
        }

        @media (prefers-reduced-motion: reduce) {
          ::view-transition-group(*),
          ::view-transition-old(*),
          ::view-transition-new(*) {
            animation: none !important;
          }
        }
      `}</style>

      {!activeArticle ? (
        <div className="max-w-4xl mx-auto">
          <header className="mb-8">
            <span className="text-xs uppercase tracking-widest text-[#767676] font-mono">Transitions.dev Showroom</span>
            <h1 className="text-3xl font-medium tracking-tight mt-1">Galeria de Artigos & View Transitions</h1>
          </header>

          <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
            {SAMPLE_DATA.map((article) => (
              <div
                key={article.id}
                onClick={() => navigateWithTransition(article)}
                className="group cursor-pointer rounded-2xl border border-black/5 dark:border-white/5 bg-white dark:bg-[#181818] p-4 shadow-sm hover:shadow-md transition-shadow duration-200"
              >
                <div className="overflow-hidden rounded-xl aspect-[16/10] mb-4 bg-zinc-100 dark:bg-zinc-800">
                  <img
                    src={article.image}
                    alt={article.title}
                    style={{ '--vt-tag-img': `article-img-${article.id}` } as React.CSSProperties}
                    className="vt-image w-full h-full object-cover group-hover:scale-[1.02] transition-transform duration-300 ease-out"
                  />
                </div>
                <span className="text-xs font-mono text-[#767676]">{article.category}</span>
                <h3
                  style={{ '--vt-tag-title': `article-title-${article.id}` } as React.CSSProperties}
                  className="vt-title text-lg font-medium tracking-tight mt-1 group-hover:text-blue-600 dark:group-hover:text-blue-400 transition-colors"
                >
                  {article.title}
                </h3>
                <p className="text-sm text-[#6c6c6c] dark:text-[#a0a0a0] mt-2 line-clamp-2">
                  {article.summary}
                </p>
              </div>
            ))}
          </div>
        </div>
      ) : (
        <article className="max-w-3xl mx-auto">
          <button
            onClick={() => navigateWithTransition(null)}
            className="mb-6 inline-flex items-center gap-2 text-sm font-medium text-[#767676] hover:text-[#0d0d0d] dark:hover:text-white transition-colors"
          >
            ← Voltar para listagem
          </button>

          <div className="overflow-hidden rounded-3xl aspect-[21/9] mb-8 bg-zinc-100 dark:bg-zinc-800 shadow-xl">
            <img
              src={activeArticle.image}
              alt={activeArticle.title}
              style={{ '--vt-tag-img': `article-img-active` } as React.CSSProperties}
              className="vt-image w-full h-full object-cover"
            />
          </div>

          <span className="text-xs font-mono uppercase tracking-widest text-blue-600 dark:text-blue-400 font-semibold">
            {activeArticle.category}
          </span>
          <h1
            style={{ '--vt-tag-title': `article-title-active` } as React.CSSProperties}
            className="vt-title text-4xl font-semibold tracking-tight mt-2 mb-6"
          >
            {activeArticle.title}
          </h1>

          <div className="prose dark:prose-invert text-[#4a4a4a] dark:text-[#cacaca] leading-relaxed space-y-4">
            <p className="text-lg leading-relaxed">{activeArticle.summary}</p>
            <p>
              Ao utilizar a View Transitions API nativa, o navegador captura o estado visual dos elementos marcados
              com <code>view-transition-name</code> antes da mutação do DOM e interpola geometricamente sua posição,
              escala e propriedades no compositor gráfico da GPU, operando a 120 FPS sem depender de runtimes JS pesados.
            </p>
          </div>
        </article>
      )}
    </div>
  );
}
```

---

### Receita de Código 2: Plus-to-Menu Surface Morph & Soft Text Swap

Esta receita implementa a transição de metamorfose onde um botão circular (+) se transforma em um menu de ações em conformidade estrita com os tokens do Transitions.dev, incluindo o micro cross-blur de texto.

```tsx
import React, { useState } from 'react';

export function PlusToMenuMorph() {
  const [isOpen, setIsOpen] = useState(false);
  const [copiedState, setCopiedState] = useState(false);

  const handleCopy = () => {
    setCopiedState(true);
    setTimeout(() => setCopiedState(false), 2000);
  };

  return (
    <div className="flex flex-col items-center justify-center min-h-[380px] w-full bg-[#f9f9f9] dark:bg-[#131313] p-8 rounded-3xl border border-black/[0.04] dark:border-white/[0.02]">
      <style>{`
        /* ======================================================== */
        /* TOKENS TRANSITIONS.DEV - MORPH & TEXT SWAP               */
        /* ======================================================== */
        .t-morph-container {
          --morph-open-dur: 350ms;
          --morph-close-dur: 250ms;
          --morph-ease: cubic-bezier(0.34, 1.25, 0.64, 1);
          --morph-close-ease: cubic-bezier(0.22, 1, 0.36, 1);

          --morph-w-closed: 44px;
          --morph-h-closed: 44px;
          --morph-r-closed: 22px;

          --morph-w-open: 200px;
          --morph-h-open: 180px;
          --morph-r-open: 16px;

          position: relative;
          width: var(--morph-w-closed);
          height: var(--morph-h-closed);
          border-radius: var(--morph-r-closed);
          background: #ffffff;
          box-shadow: 0 4px 42px 0 rgba(0, 0, 0, 0.06), 0 2px 6px 0 rgba(0, 0, 0, 0.05), 0 0 0 1px rgba(0, 0, 0, 0.06);
          transition: 
            width var(--morph-close-dur) var(--morph-close-ease),
            height var(--morph-close-dur) var(--morph-close-ease),
            border-radius var(--morph-close-dur) var(--morph-close-ease),
            box-shadow 200ms ease;
          overflow: hidden;
        }

        :root.dark .t-morph-container {
          background: #181818;
          box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.4), inset 0 0 0 1px rgba(255, 255, 255, 0.08);
        }

        .t-morph-container[data-open="true"] {
          width: var(--morph-w-open);
          height: var(--morph-h-open);
          border-radius: var(--morph-r-open);
          transition: 
            width var(--morph-open-dur) var(--morph-ease),
            height var(--morph-open-dur) var(--morph-ease),
            border-radius var(--morph-open-dur) var(--morph-ease);
        }

        /* Ícone do Gatilho (+) */
        .t-plus-icon {
          position: absolute;
          inset: 0;
          display: flex;
          align-items: center;
          justify-content: center;
          transition: transform 300ms cubic-bezier(0.22, 1, 0.36, 1), opacity 200ms ease;
          cursor: pointer;
        }

        .t-morph-container[data-open="true"] .t-plus-icon {
          transform: rotate(45deg) scale(0.85);
          opacity: 0;
          pointer-events: none;
        }

        /* Conteúdo do Menu Interno */
        .t-menu-content {
          opacity: 0;
          transform: translateY(12px) scale(0.97);
          filter: blur(2px);
          transition: opacity 150ms ease, transform 200ms ease, filter 200ms ease;
          pointer-events: none;
        }

        .t-morph-container[data-open="true"] .t-menu-content {
          opacity: 1;
          transform: translateY(0) scale(1);
          filter: blur(0px);
          transition: 
            opacity 250ms var(--ease-smooth-out) 100ms,
            transform 300ms var(--ease-smooth-out) 80ms,
            filter 250ms var(--ease-smooth-out) 80ms;
          pointer-events: auto;
        }

        /* Text Swap com Micro Cross-Blur */
        .t-swap-wrapper {
          position: relative;
          display: inline-flex;
          align-items: center;
          justify-content: center;
        }
        .t-swap-item {
          transition: transform 180ms cubic-bezier(0.22, 1, 0.36, 1), opacity 180ms ease, filter 180ms ease;
        }
      `}</style>

      <div className="relative">
        <div className="t-morph-container" data-open={isOpen ? "true" : "false"}>
          {/* Botão Gatilho Inicial */}
          <button
            onClick={() => setIsOpen(true)}
            aria-label="Abrir Menu de Criação"
            className="t-plus-icon text-zinc-900 dark:text-zinc-100 hover:bg-black/[0.03] dark:hover:bg-white/[0.04] rounded-full"
          >
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2.2" strokeLinecap="round">
              <line x1="12" y1="5" x2="12" y2="19"></line>
              <line x1="5" y1="12" x2="19" y2="12"></line>
            </svg>
          </button>

          {/* Conteúdo Expandido do Menu */}
          <div className="t-menu-content p-3 flex flex-col justify-between h-full text-xs">
            <div className="flex items-center justify-between pb-2 border-b border-black/5 dark:border-white/5">
              <span className="font-medium text-zinc-500 font-mono">AÇÕES RÁPIDAS</span>
              <button
                onClick={() => setIsOpen(false)}
                className="p-1 hover:bg-black/5 dark:hover:bg-white/5 rounded-md text-zinc-400 hover:text-zinc-700 dark:hover:text-zinc-200"
              >
                ✕
              </button>
            </div>

            <div className="flex flex-col gap-1 py-1">
              <button
                onClick={handleCopy}
                className="w-full flex items-center justify-between px-2.5 py-1.5 rounded-lg hover:bg-black/[0.04] dark:hover:bg-white/[0.06] text-zinc-800 dark:text-zinc-200 transition-colors"
              >
                <span>Chave de Acesso</span>
                <span className="t-swap-wrapper font-mono text-[10px] text-zinc-400">
                  {copiedState ? (
                    <span className="t-swap-item text-emerald-600 dark:text-emerald-400 font-semibold animate-in">
                      Copiado!
                    </span>
                  ) : (
                    <span className="t-swap-item">Copiar</span>
                  )}
                </span>
              </button>

              <button className="w-full text-left px-2.5 py-1.5 rounded-lg hover:bg-black/[0.04] dark:hover:bg-white/[0.06] text-zinc-800 dark:text-zinc-200 transition-colors">
                Novo Documento
              </button>
              <button className="w-full text-left px-2.5 py-1.5 rounded-lg hover:bg-black/[0.04] dark:hover:bg-white/[0.06] text-zinc-800 dark:text-zinc-200 transition-colors">
                Compartilhar Link
              </button>
            </div>

            <div className="pt-2 border-t border-black/5 dark:border-white/5 flex justify-end">
              <button
                onClick={() => setIsOpen(false)}
                className="text-[11px] text-zinc-400 hover:text-zinc-700 dark:hover:text-zinc-200"
              >
                Fechar
              </button>
            </div>
          </div>
        </div>
      </div>

      <span className="mt-8 text-xs text-[#767676] font-mono">
        Clique no (+) para testar a expansão elástica e o fechamento snappier.
      </span>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao conceber um projeto técnico ou arquitetar o design system no arquivo `DESIGN_BLUEPRINT.md`, a inteligência artificial ou engenheiro responsável deve declarar as diretrizes de movimento do **Transitions.dev** conforme as seguintes seções estruturais:

### 1. Declaração Obrigatória de Tokens de Movimento no CSS Global
O `DESIGN_BLUEPRINT.md` deve listar explicitamente a injeção dos tokens de tempo, curvas e desfoque:
```markdown
### Motion Tokens (Transitions.dev Foundation)
- `--ease-smooth-out: cubic-bezier(0.22, 1, 0.36, 1)` (Transições padrão de entrada)
- `--ease-bounce: cubic-bezier(0.34, 1.36, 0.64, 1)` (Badges e realces táteis)
- `--ease-morph: cubic-bezier(0.34, 1.25, 0.64, 1)` (Metamorfoses de superfícies)
- `--duration-enter: 250ms` / `--duration-exit: 150ms` (Assimetria temporal estrita)
- `--blur-optical: 2px` (Micro cross-blur em trocas de texto e ícones)
```

### 2. Mapeamento de Padrões por Elemento de Interface
O plano técnico deve cruzar os componentes da aplicação com os padrões canônicos da tabela do catálogo:
- **Gatilho de Dropdown / Menus Flutuantes** -> Padrão `02-origin-aware-dropdown` com `transform-origin` orientado à coordenada do botão.
- **Transição de Rotas e Telas de Detalhe** -> Padrão `01-view-transitions-morph` com atribuição de `view-transition-name` e fallback condicional.
- **Notificações e Alertas** -> Padrão `07-sonner-stacking` com recuo em escala e desfoque progressivo na fila de profundidade.
- **Validação de Formulários** -> Padrão `08-error-shake-decay` com oscilação em 4 passos e reversão temporizada de 3000ms.
- **Indicadores de Carregamento e IA** -> Padrão `10-ai-thinking-shimmer` com máscara de gradiente de 400% e ciclo de 2000ms.

### 3. Matriz de Auditoria de Acessibilidade & Desempenho
Antes de aprovar o blueprint para codificação, o arquiteto deve validar:
- [ ] Todos os componentes possuem bloco `@media (prefers-reduced-motion: reduce)` anulando translações, escalas e blurs.
- [ ] Nenhum componente realiza `transition: height` ou `transition: width` sem o uso de CSS Grid (`grid-template-rows: 0fr -> 1fr`) ou escala geométrica via GPU.
- [ ] Nenhuma transição de saída possui duração superior a `200ms` em componentes modais ou popovers de produtividade.
- [ ] O uso de filtros de `blur` está limitado ao limiar de `1px` a `3px`, evitando exaustão de GPU fillrate em dispositivos móveis.
