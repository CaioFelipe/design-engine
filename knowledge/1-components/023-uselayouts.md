---
id: "uselayouts"
name: "UseLayouts"
url: "https://uselayouts.com/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Modern Tactile Craft", "iOS/macOS Skeuomorphic Physics", "Layout Morphing & Shared Projections", "Liquid Glass & Progressive Speculars", "Physical Paper & Spatial Metaphors"]
densidade_informacao: "Flexivel"
impacto_visual: "Moderado a Alto/Showstopper"
custo_computacional: "Medio (Motion/React Layout Projections & CSS 3D Transforms)"
stack_frameworks: ["React 19 / React 18", "Next.js (App Router)", "Motion (Framer Motion)", "Tailwind CSS (v3 / v4)", "TypeScript", "shadcn/ui Registry Architecture"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Geist Mono", "Inter", "SF Pro Display", "JetBrains Mono"]
  paletas_ideais: ["Warm Neutral Sand & Porcelain (#F5F3EE / #071A31)", "Deep Metallic Zinc & Matte Glass", "Skeuomorphic Chrome & Amber Specular Glow", "Subtle Alpha Inset Highlights (white/70, white/10)"]
  combinacoes_recomendadas: ["shadcn/ui", "Motion Primitives", "Cult UI", "Radix UI Primitives", "Hugeicons", "Lucide React"]
  conflitos_esteticos: ["Brutalismo cru sem suavização física", "Flat design plano monocromático dos anos 2010", "Neumorfismo plástico hiper-saturado sem profundidade óptica", "Animações lineares sem inércia ou amortecimento"]
---

# UseLayouts — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo engenheiro de design **Urvish Mali** (conhecido na comunidade de desenvolvimento web como **@0xUrvish** / **@iurvish**, criador de `urvish.in` e apoiado oficialmente pelo programa **Vercel Open Source Software**), o **UseLayouts** (`uselayouts.com`) consolidou-se como a biblioteca de vanguarda no renascimento da **física tátil (*tactile craft*)** e das micro-interações inspiradas na elegância mecânica do hardware físico e nos sistemas operacionais da Apple (iOS, iPadOS e macOS).

Enquanto grande parte das bibliotecas modernas de React aposta em gradientes fluorescentes estáticos ou bibliotecas 3D WebGL pesadas, o UseLayouts ocupa uma posição única e refinada no design craft: **dar peso, inércia, tridimensionalidade tátil e continuidade espacial a componentes do cotidiano** (botões, abas, inputs, pastas de arquivos, joysticks e galerias de fotos) utilizando exclusivamente **React**, **Tailwind CSS** e **Motion (Framer Motion)**.

### Os Pilares da Assinatura Visual do UseLayouts:

1. **Skeuomorfismo Tátil de Nova Geração (*Tactile Rocker & Sockets*)**:
   Diferente do neumorfismo de 2020 — que frequentemente causava problemas severos de contraste e acessibilidade visual —, o acabamento do UseLayouts utiliza **camadas sobrepostas de sombras internas (`box-shadow: inset`)**, chanfros angulares de 45° a 90°, soquetes embutidos usinados na superfície (*recessed sockets*) e reflexos especulares em degradê (*liquid glass sheen*). Botões como o `tactile-button` inclinam-se fisicamente no eixo Z como um interruptor balancim mecânico verdadeiro (`rotate: -8.5deg`, `y: -12px`, `x: 3px`), acompanhados por um LED esférico de vidro que se acende com brilho volumétrico difuso.

2. **Projeções de Layout e Metamorfose Espacial (`layoutId` & `layout`)**:
   O UseLayouts domina o motor de projeção de layout do Framer Motion. Em componentes como o `discrete-tabs`, a alternância entre abas não utiliza crossfades banais: a pílula do botão expande suavemente sua largura de forma elástica (`px-3` para `px-4`), empurrando os elementos vizinhos de forma orgânica, enquanto o ícone e o texto sofrem uma sutil transição óptica de desfoque fracionado (`filter: blur(4px) -> blur(0px)`).

3. **Metáforas Físicas Literais (*Tangible UI Metaphors*)**:
   A biblioteca desafia a abstração puramente digital trazendo interações do mundo analógico para o navegador com fidelidade extraordinária:
   - O `paper-shred-button` puxa uma folha de formulário e a desce fatiando fisicamente em tiras de papel animadas ao confirmar uma exclusão.
   - O `confidential-folder` simula um envelope de arquivos classificados: ao passar o cursor, a aba superior se abre, o documento interno é sacado para fora e sofre uma rotação tridimensional de 180° no espaço para revelar o conteúdo confidencial.
   - O `analog-stick` reproduz um analógico emborrachado com cúpula de controle direcional quádruplo, reagindo à posição do mouse com iluminação âmbar retroiluminada.
   - O `polaroid-stack` e o `polaroid-drag` recriam o fanning natural e o empilhamento desordenado de fotografias instantâneas Polaroid reais.

4. **Distribuição Registro-Nativa Shadcn (`@uselayouts` Registry)**:
   O UseLayouts não impõe pacotes monolíticos opacos em `node_modules`. Seguindo a arquitetura moderna de registros do `shadcn/ui`, os desenvolvedores configuram o endpoint do UseLayouts no `components.json` e importam o código-fonte puro em TypeScript via CLI (`npx shadcn@latest add @uselayouts/<component-name>`). Isso garante que todo o CSS em Tailwind, os hooks e os parâmetros de física pertençam integralmente à aplicação consumidora.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários

1. **Ferramentas de Produtividade & SaaS B2B de Alto Craft (Estilo Linear, Raycast, Cron, Reflect)**:
   Aplicações onde o prazer tátil da navegação diária é um diferencial de retenção. O uso de `discrete-tabs` na barra de status superior, `dynamic-toolbar` para paletas contextuais de comandos, e `client-card` para dashboards de CRM transforma operações rotineiras em momentos de alta satisfação tátil.
2. **Interfaces de IA Generativa & Agentes Autônomos**:
   O componente `prompt-box` e o `morphing-input` são escolhas imbatíveis para caixas de entrada de modelos de linguagem: a caixa de prompt expande sua altura organicamente, revela seletores de modelos (`Claude 3.5`, `GPT-4o`) e transmuta o placeholder letra por letra com efeito escalonado (*staggered text blur*).
3. **Portfólios de Design Engineers & Creative Technologists**:
   Criadores que desejam demonstrar domínio avançado de física interativa, micro-interações de ponta e fluidez espacial encontram no `analog-stick`, `tactile-button`, `3d-book` e `polaroid-drag` componentes de impacto imediato (*showstoppers*).
4. **E-commerce Premium, Marcas D2C & Estúdios Criativos**:
   Vitrines digitais de luxo onde os detalhes construtivos comunicam valor: o `accordionos` para apresentação detalhada de processos artesanais (ex: cerâmica, relojoaria, alfaiataria), `drawer-buttons` para gavetas sanfonadas de checkout físico e `coverflow-drag` para catálogos visuais envolventes.
5. **Dashboards Financeiros e Painéis de Controle Físico (IoT / Smart Home)**:
   Interfaces para automação residencial, instrumentação digital de estúdio e sistemas de áudio onde botões de pressão táctil (`tactile-button`), chaves de alternância (`theme-toggle` com trilho usinado) e botões de estado triplo (`save-button` / Status Button) fornecem feedback auditivo e visual incomparável.

---

### Papel no Ritmo Visual (Regra 60-30-10)

- **60% — Fundação Neutra e Silenciosa (Base Estrutural)**:
  Superfícies em tons quentes de papel ou ardósia fosca (`#F5F3EE` em light mode ou `#030202` / `bg-zinc-950` em dark mode), tipografia minimalista e legível (`Geist Sans` para corpo, `Geist Mono` para metadados e tags técnicas), espaçamentos arejados e bordas sutis com baixa opacidade (`border-white/10` ou `border-black/5`).
- **30% — Camada de Fluidez e Navegação Orgânica (Micro-Interações Estruturais)**:
  - *Discrete Tabs*: Navegação entre seções sem travamentos, com a pílula ativa expandindo e acomodando o texto dinamicamente.
  - *Dynamic Toolbar*: Barras de ferramentas que calculam seu próprio volume e se adaptam à quantidade de ações presentes.
  - *Smooth Dropdown*: Menus contextuais que abrem suas opções com interpolação de mola sem saltos de renderização (*no-layout-jump*).
  - *Multi Step Form*: Formulários que deslizam etapas horizontalmente com amortecimento crítico.
- **10% — Efeitos Protagonistas / Showstoppers (Momentos Memoráveis)**:
  - *Tactile Button*: O botão primário de conversão ("Get Started", "Deploy", "Checkout") na Hero Section, comportando-se como um interruptor físico de vidro usinado.
  - *AccordionOS*: O bloco central de features da Landing Page, combinando accordion de pílulas fosco, crossfade de fotos em alta velocidade via GPU e controle por teclado.
  - *Paper Shred Button*: Ação de cancelamento ou destruição de chave de API em um painel de desenvolvedor, triturando o card em tiras.
  - *Confidential Folder*: Caixa de convite exclusivo ou relatório de inteligência que ejeta e gira um documento confidencial em 3D.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Telas Densas de Telemetria e Terminais de Trading de Alta Frequência**:
  Sistemas financeiros (ex: Bloomberg Terminal, painéis de trading cripto) com milhares de cotações atualizadas em tempo real a 60 FPS não devem incorporar botões com rotações tridimensionais, sombras quádruplas em `box-shadow` e máscaras de desfoque por CPU. Nesses casos, prefira componentes leves e estáticos em CSS puro.
- **Sistemas Governamentais ou Portais de Serviços Públicos Universais**:
  Aplicações que atendem a populações heterogêneas e equipamentos de altíssima obsolescência (monitores com fidelidade de cores precária ou computadores sem aceleração de GPU) sofrerão com o peso visual de sombras sutis e possíveis ambiguidades de clique em botões skeuomórficos.
- **Formulários Críticos de Saúde ou Emergência**:
  Interfaces hospitalares ou de suporte emergencial exigem clareza absoluta e máxima velocidade de leitura; animações de folhas de papel sendo trituradas ou pastas sendo desdobradas introduzem atraso cognitivo inaceitável.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **Saturação de Fidget Toys na Mesma Tela**:
  Inserir simultaneamente em uma mesma página um `analog-stick`, três `tactile-button`, dois `card-folder` e uma pilha de `polaroid-stack`. A interface se degenera em um parque de diversões infantilizado, retirando a seriedade do produto. O encanto tátil exige contraste com superfícies calmas.
- **Esquecer o Suporte a Redução de Movimento (`prefers-reduced-motion`)**:
  Componentes como `analog-stick` e `tactile-button` devem sempre declarar a variante `motion-reduce:transition-none` e `motion-reduce:[transform:none]`, garantindo que usuários propensos a náusea vestibular recebam estados estáticos instantâneos.
- **Ausência de Estados de Acessibilidade por Teclado (`focus-visible`)**:
  Ao criar botões tácteis personalizados com wrappers decorativos de soquete (`div > motion.button`), é crucial preservar atributos ARIA (`aria-label`, `aria-pressed`, `role="button"`), o tabIndex e os anéis nativos de foco do Tailwind (`focus-visible:ring-2 focus-visible:ring-offset-2`).

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão descritos **12 componentes emblemáticos** do catálogo oficial do UseLayouts, detalhando sua anatomia de camadas, física de interação e recomendação técnica de encaixe:

```
+-----------------------------------------------------------------------------------------+
|                               CATÁLOGO SHOWSTOPPERS USELAYOUTS                          |
+--------------------+------------------------------------+-------------------------------+
| Componente         | Anatomia Visual e Física           | Encaixe no Layout             |
+--------------------+------------------------------------+-------------------------------+
| 1. Tactile Button  | Soquete rebaixado + capa balancim  | CTA da Hero Section / Ação    |
|                    | de vidro + LED indicador esférico  | Principal de Compra           |
| 2. AccordionOS     | Pílulas fosco-vidro + crossfade de | Seção de Features / Vitrine   |
|                    | imagens GPU + teclado 1-5 / arrows | de Casos de Estudo            |
| 3. Discrete Tabs   | Pílula elástica com layoutId +     | Navbar Superior / Filtros de  |
|                    | blur progressivo em texto ativo    | Categoria / Abas de Dashboard |
| 4. Morphing Input  | Switch de ícone com AnimatePresence| Search Central / Prompt de IA |
|                    | + digitação escalonada caractere   | com seleção de modelo         |
| 5. Analog Stick    | Cúpula direcional 3D com 4 zonas   | Seção de Hardware / Gaming /  |
|                    | hover e LED âmbar integrado        | Easter Eggs / Controles IoT   |
| 6. Paper Shred     | Botão de deleção que divide o card | Diálogo de Exclusão Crítica / |
|    Button          | em tiras com queda por gravidade   | Cancelamento de Assinatura    |
| 7. Confidential    | Envelope com aba que abre em 3D e  | Card de Recursos Secretos /   |
|    Folder          | ejeta documento com flip a 180°    | Convites VIP / Waitlists      |
| 8. Dynamic Toolbar | Pílula flutuante que calcula bounding| Dock de Ações Flutuante /     |
|                    | box e se redimensiona por mola     | Editor de Texto / Canvas      |
| 9. Polaroid Stack  | Pilha de fotografias que se abre   | Depoimentos / Equipe /        |
|                    | em leque radial sob o cursor       | Galeria de Momentos           |
| 10. Shake Card     | Card com amortecimento e pulso de  | Grid de Depoimentos Sociais / |
|                    | mola com inércia angular           | Cartões de Avaliação          |
| 11. Bottom Menu    | Dock inferior expansível com       | Navegação Mobile / Ações      |
|                    | morphing de sub-menus fluidos      | Fixas de Rodapé               |
| 12. Fluid Grid     | Grade responsiva cujas células     | Bento Grid de Funcionalidades |
|                    | respiram e redimensionam irmãs     | Principais do Produto         |
+--------------------+------------------------------------+-------------------------------+
```

### 1. Tactile Button (`tactile-button`)
- **Anatomia Visual**: Composto por duas camadas sobrepostas com precisão micrométrica:
  1. *Recessed Socket Well (`Button Base`)*: Camada em baixo-relevo (`bg-[#cbcbcb]/90 backdrop-blur-md`) com sombras internas profundas que simulam um soquete usinado em alumínio ou acrílico fosco.
  2. *3D Liquid Glass Plunger Cap (`Button Box`)*: A capa móvel em degradê de vidro (`bg-gradient-to-b from-white/95 via-white/85 to-white/90 border border-white/60`) que repousa sobre molas virtuais.
  3. *Bead LED Indicator*: Pílula circular com brilho difuso multicolorido (`blue`, `green`, `amber`, `red`) contendo ponto de reflexo especular de 2px no canto superior esquerdo.
- **Gatilho de Interação**:
  - `Hover`: O balancim eleva-se levemente (`y: -2px`) e acentua a sombra projetada.
  - `MouseDown / TouchStart`: Inclina-se bruscamente no ângulo negativo (`rotate: -8.5deg`, `y: -12px`, `x: 3px`) simulando o afundamento assimétrico de uma tecla física.
  - `MouseUp / Release`: Mola com leve ressalto elástico (`bounce: 0.45, duration: 0.55s`) que restaura o estado inicial.
- **Onde Encaixar**: Botão principal da Hero Section (*Primary Call To Action*), acionamento de checkout final ou ativação de modo de produção.

### 2. AccordionOS (`accordionos`)
- **Anatomia Visual**: Módulo widescreen estruturado com container de 36px de raio de curvatura. A coluna esquerda abriga uma pilha vertical de pílulas semi-translúcidas (`backdrop-filter: blur(16px)` com bordas sutis `rgba(255, 255, 255, 0.7)`). Ao expandir, o botão giratório com cruz central gira de `0°` para `135°`, o texto de explicação expande sua altura com desfoque óptico de 4px para 0px, e o deck inferior flutuante exibe a contagem formatada (`01 / 05`) com botões táteis de avançar/voltar. A coluna direita projeta as imagens em tela cheia com crossfade instantâneo acelerado por GPU (`opacity` e `scale: 1.05 -> 1`).
- **Gatilho de Interação**: Click do mouse, hover com interrupção de autoplay, e controle global por teclado (`ArrowDown`, `ArrowUp`, teclas `W`/`S`, dígitos numéricos de `1` a `5` e tecla `Escape` para fechar).
- **Onde Encaixar**: Seção principal de Features da Landing Page, vitrines de produto ou demonstrações de produto em 5 etapas sequenciais.

### 3. Discrete Tabs (`discrete-tabs`)
- **Anatomia Visual**: Conjunto de botões de cantos curvos (`rounded-[25px]`) em fonte monoespaçada com caixa alta (`font-mono uppercase`). O botão inativo exibe apenas o ícone centralizado com dimensões compactas (`px-3 py-3`). Ao ser clicado, a pílula dispara uma projeção espacial contínua via `layout` e `layoutId`, expandindo a largura para acomodar o texto descritivo (`px-4`) e disparando um reflexo de luz temporário (*shine pulse* de 800ms).
- **Gatilho de Interação**: Click com mola encorpada (`stiffness: 230, damping: 20, mass: 1.2`) e entrada de texto com `filter: blur(4px) -> blur(0px)` em curva cúbica `[0.86, 0, 0.07, 1]`.
- **Onde Encaixar**: Barra de navegação do topo (Navbar), filtros de categoria em e-commerce, ou chaveador de modos em dashboards de controle.

### 4. Morphing Input (`morphing-input`)
- **Anatomia Visual**: Cápsula de entrada única com bordas arredondadas totais (`rounded-full bg-muted`). À esquerda, um botão circular independente abriga o ícone da ferramenta atual (ex: `SparklesIcon` para busca por IA, `Album02Icon` para geração de imagens) acompanhado por um seletor visual sutil (`UnfoldMoreIcon`). Ao lado, o placeholder anima a troca de texto caractere por caractere com atraso progressivo (*stagger delay* de 20ms por glifo).
- **Gatilho de Interação**: Click no botão de alternância de modo aciona o `AnimatePresence` com rotação e escala elástica no ícone, e aciona a cascata de letras no placeholder.
- **Onde Encaixar**: Caixa central de busca em homepages inteligentes, input principal de chatbots e agentes de IA, ou barra de ferramentas de comandos (*Omnibar*).

### 5. Analog Stick (`analog-stick`)
- **Anatomia Visual**: Módulo circular skeuomórfico inspirado no analógico emborrachado de controles clássicos de console. Possui carcaça em degradê radial de alumínio (`bg-[linear-gradient(0deg,#f5f8fa,#9da4a8)]`), anel interno usinado com sombras embutidas profundas (`inset_0_0_16px_rgba(0,0,0,0.85)`), e cúpula central com textura côncava de quatro pontos em relevo.
- **Gatilho de Interação**: Sistema engenhoso em Tailwind puro com detecção de quadrante via `:has(.t1:hover)`, `:has(.t2:hover)`, etc. Ao posicionar o cursor em um dos 4 quadrantes, a cúpula central inclina 8 graus no eixo correspondente (`rotateX(8deg)` ou `rotateY(8deg)` com `transform-style: preserve-3d`), a sombra é redistribuída e a seta direcional acende em tom âmbar luminoso (`#eaa75d`) com brilho duplo em `drop-shadow`.
- **Onde Encaixar**: Showcases de produtos de hardware, interfaces temáticas de gaming, painéis de ajuste de câmera robótica / drones ou easter eggs interativos de portfólio.

### 6. Paper Shred Button (`paper-shred-button`)
- **Anatomia Visual**: Botão de deleção que, ao invés de um modal de confirmação estático convencional, contém uma miniatura de documento empoleirada sobre uma fenda de triturador.
- **Gatilho de Interação**: Ao clicar para deletar, o documento é puxado para baixo em velocidade contínua enquanto saem tiras verticais finas de papel retalhado na base inferior, desvanecendo com rotações assimétricas antes do reset do botão para o estado concluído.
- **Onde Encaixar**: Diálogos de deleção permanente (ex: "Excluir conta", "Revogar credenciais de produção", "Limpar histórico").

### 7. Confidential Folder (`confidential-folder`)
- **Anatomia Visual**: Uma pasta de arquivo manila ou preta com carimbo tipográfico de "Confidencial". A textura externa apresenta borda de costura reforçada e textura de papel fosco.
- **Gatilho de Interação**: No hover, a aba frontal se desdobra para baixo, expondo uma folha de papel com dados sigilosos que desliza 60px para cima e gira em torno do eixo Y em 180°, permitindo a leitura da mensagem interna.
- **Onde Encaixar**: Seção de revelação de benefícios exclusivos em waitlists de startups, cartões de convite VIP ou páginas de apresentação de segurança criptográfica.

### 8. Dynamic Toolbar (`dynamic-toolbar`)
- **Anatomia Visual**: Barra de ações flutuante inspirada no Dynamic Island do iOS. Apresenta fundo em vidro escurecido fosco com anel de reflexo sutil. Ao transitar entre ferramentas (ex: "Editar", "Comentar", "Exportar"), a barra recalcula dinamicamente sua caixa delimitadora (*bounding box*).
- **Gatilho de Interação**: Mudança de estado ativa o recálculo do container via `layout` com mola sem solavancos, acomodando botões adicionais sem cortes secos.
- **Onde Encaixar**: Editores de conteúdo WYSIWYG, barras flutuantes em canvas de design ou menus contextuais em tabelas administrativas.

### 9. Polaroid Stack (`polaroid-stack`)
- **Anatomia Visual**: Três a quatro impressões fotográficas estilo Polaroid com bordas brancas espessas e textura fosca, empilhadas com pequenas variações aleatórias de rotação (-4° a +6°).
- **Gatilho de Interação**: No hover do container, as fotos se abrem em um leque radial harmonioso, revelando as imagens ocultas com profundidade de campo e sombras projetadas dinâmicas.
- **Onde Encaixar**: Seção "Sobre Nós / A Equipe", prova social com fotos reais de clientes, ou galerias visuais em landing pages criativas.

### 10. Shake Testimonial Card (`shake-testimonial-card`)
- **Anatomia Visual**: Card de depoimento com foto do autor, nome, cargo e citação. Possui acabamento com borda reflexiva de 1px e backdrop translúcido.
- **Gatilho de Interação**: Ao ser focado ou acionado via clique/hover, o cartão executa uma oscilação física rápida amortecida (*damping oscillation*), transmitindo a sensação de um cartão de visita sólido preso em uma mola flexível.
- **Onde Encaixar**: Grade de depoimentos em landing pages B2B ou carrossel de recomendações de produto.

### 11. Bottom Menu (`bottom-menu`)
- **Anatomia Visual**: Menu em dock fixado na base da viewport, com cantos arredondados generosos (`rounded-2xl`) e acabamento em vidro translúcido escuro.
- **Gatilho de Interação**: O botão principal "+" expande a pílula em um menu sanfonado vertical contendo ícones secundários e atalhos com stagger de revelação.
- **Onde Encaixar**: Navegação principal para visualizações mobile ou barra de comandos rápidos em aplicações desktop web.

### 12. Fluid Expanding Grid (`fluid-expanding-grid`)
- **Anatomia Visual**: Grid estilo Bento onde as proporções das colunas não são rígidas. Células adjacentes respiram em conjunto através de proporções flexíveis ponderadas.
- **Gatilho de Interação**: Ao passar o cursor ou selecionar um card, a célula selecionada expande de `1fr` para `2fr`, enquanto as irmãs contraem suavemente para `0.8fr` usando transições de layout do Framer Motion.
- **Onde Encaixar**: Seções de demonstração de pilares de produto em páginas institucionais de startups de tecnologia.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Registro Shadcn

O UseLayouts utiliza uma abordagem moderna e descentralizada através do sistema de registros do Shadcn. Para configurar o UseLayouts em um projeto React / Next.js existente:

#### 1. Configurar o Registro no `components.json`

```json
{
  "$schema": "https://ui.shadcn.com/schema.json",
  "style": "default",
  "rsc": true,
  "tsx": true,
  "tailwind": {
    "config": "tailwind.config.ts",
    "css": "app/globals.css",
    "baseColor": "zinc",
    "cssVariables": true
  },
  "registries": {
    "@uselayouts": "https://uselayouts.com/r/{name}.json"
  },
  "aliases": {
    "components": "@/components",
    "utils": "@/lib/utils"
  }
}
```

#### 2. Instalação de Componentes via CLI

```bash
# Instalar componentes diretamente via CLI do shadcn
npx shadcn@latest add @uselayouts/discrete-tabs
npx shadcn@latest add @uselayouts/tactile-button
npx shadcn@latest add @uselayouts/accordionos
npx shadcn@latest add @uselayouts/morphing-input
```

#### 3. Dependências de Pacote (`package.json`)

```bash
npm install motion clsx tailwind-merge @radix-ui/react-tooltip @hugeicons/react @hugeicons/core-free-icons
```

---

### Física de Movimento, Constantes de Mola e Easing

O refinamento das micro-interações do UseLayouts decorre de valores de mola calibrados para evitar tanto o efeito "gelatina infantil" quanto a rigidez artificial de transições lineares de CSS:

| Padrão de Movimento | Tipo | Configuração de Parâmetros | Sensação Tátil Percebida |
|---|---|---|---|
| **Layout Pill Expansion** (`discrete-tabs`) | `spring` | `stiffness: 230`, `damping: 20`, `mass: 1.2` | Peso mecânico sólido, com desaceleração firme ao expandir a pílula. |
| **Tactile Rocker Tilt** (`tactile-button`) | `spring` | `bounce: 0.45`, `duration: 0.55s` | Clique de balancim mecânico com leve ressalto instantâneo. |
| **AccordionOS Expansion** | `spring` | `stiffness: 340`, `damping: 28`, `mass: 0.8` | Resposta ágil de sistema operacional de desktop, sem oscilação residual. |
| **Navigation Bouncy Deck** | `spring` | `stiffness: 400`, `damping: 22` | Salto dinâmico e responsivo em contadores e setas de navegação. |
| **Glyph Stagger Transition** (`morphing-input`) | `cubic-bezier` | `ease: [0.32, 0.72, 0, 1]`, `stagger: 0.02s` | Entrada fluida de texto em cascata com suavização exponencial Apple. |

---

### Receita de Código Funcional: Tactile Rocker Switch com Socket Usinado e Discrete Layout Pill

Abaixo está uma implementação completa, autônoma, tipada em TypeScript e otimizada para produção, fundindo a assinatura skeuomórfica do balancim físico (`TactileButton`) com a expansão orgânica de abas com projeção de layout (`DiscreteTabSelector`):

```tsx
"use client";

import * as React from "react";
import { motion, AnimatePresence, type HTMLMotionProps } from "motion/react";
import { cn } from "@/lib/utils";

// ============================================================================
// 1. TACTILE ROCKER BUTTON (Skeuomorphic Liquid Glass with Recessed Socket)
// ============================================================================

export interface TactileRockerProps
  extends Omit<HTMLMotionProps<"button">, "children"> {
  children?: React.ReactNode;
  showIndicator?: boolean;
  indicatorColor?: "blue" | "green" | "amber" | "red";
  size?: "sm" | "default" | "lg";
  fullWidth?: boolean;
  className?: string;
}

const springPhysics = {
  type: "spring" as const,
  bounce: 0.45,
  duration: 0.55,
};

export const TactileRocker = React.forwardRef<
  HTMLButtonElement,
  TactileRockerProps
>(
  (
    {
      className,
      children = "Activate System",
      showIndicator = true,
      indicatorColor = "blue",
      size = "default",
      fullWidth = false,
      onClick,
      ...props
    },
    ref
  ) => {
    const [isPressed, setIsPressed] = React.useState(false);
    const [isHovered, setIsHovered] = React.useState(false);

    const sizeConfig = {
      sm: {
        container: "min-h-[44px] min-w-[130px]",
        base: "inset-[3px] rounded-[13px]",
        box: "px-3.5 py-1.5 text-sm gap-2 rounded-[12px]",
        indicator: "w-2.5 h-2.5",
        text: "text-sm leading-tight",
        pressedY: -8,
        pressedX: 2,
        rotate: -7.5,
      },
      default: {
        container: "min-h-[54px] min-w-[160px]",
        base: "inset-[4px] rounded-[16px]",
        box: "px-5 py-2.5 text-base gap-3 rounded-[15px]",
        indicator: "w-3 h-3",
        text: "text-base font-semibold tracking-tight leading-snug",
        pressedY: -11,
        pressedX: 3,
        rotate: -8.5,
      },
      lg: {
        container: "min-h-[64px] min-w-[190px]",
        base: "inset-[5px] rounded-[19px]",
        box: "px-6 py-3.5 text-lg gap-3.5 rounded-[18px]",
        indicator: "w-3.5 h-3.5",
        text: "text-lg font-semibold tracking-tight leading-normal",
        pressedY: -14,
        pressedX: 4,
        rotate: -9.0,
      },
    }[size];

    const getIndicatorBg = () => {
      if (!isPressed && !isHovered) return "rgb(209, 215, 222)";
      switch (indicatorColor) {
        case "green":
          return "rgb(16, 185, 129)";
        case "amber":
          return "rgb(245, 158, 11)";
        case "red":
          return "rgb(239, 68, 68)";
        case "blue":
        default:
          return "rgb(0, 102, 255)";
      }
    };

    const getIndicatorGlow = () => {
      if (!isPressed && !isHovered) {
        return "0px 2px 2px 0px rgb(255, 255, 255), inset 0px 1px 2px 0px rgba(0, 0, 0, 0.08)";
      }
      return "0px 2px 2px 0px rgba(255, 255, 255, 0.9), inset 0px 1px 2px 0px rgba(0, 0, 0, 0.1), 0px 0px 10px 2px rgba(0, 102, 255, 0.8), 0px 0px 20px 4px rgba(59, 130, 246, 0.4)";
    };

    return (
      <div
        className={cn(
          "relative inline-flex items-center justify-center select-none overflow-visible touch-manipulation cursor-pointer",
          fullWidth ? "w-full" : "w-auto max-w-full",
          sizeConfig.container,
          className
        )}
      >
        {/* Usinado Recessed Socket (Well Base) */}
        <motion.div
          aria-hidden="true"
          className={cn(
            "absolute bg-[#d6d6d8] dark:bg-[#1c1c1f] backdrop-blur-md pointer-events-none transition-shadow",
            sizeConfig.base
          )}
          initial={false}
          animate={{
            boxShadow: isPressed
              ? "inset 0px 2px 4px 0px rgba(0, 0, 0, 0.45), inset 4px 7px 6px 0px rgba(0, 0, 0, 0.35), inset -1px -1px 2px 0px rgba(255, 255, 255, 0.4)"
              : "inset 0px 1px 3px 0px rgba(0, 0, 0, 0.28), inset -1px -1px 2px 0px rgba(255, 255, 255, 0.25)",
          }}
          transition={springPhysics}
        />

        {/* 3D Liquid Glass Rocker Plunger */}
        <motion.button
          ref={ref}
          type="button"
          onMouseDown={() => setIsPressed(true)}
          onMouseUp={() => setIsPressed(false)}
          onMouseLeave={() => {
            setIsPressed(false);
            setIsHovered(false);
          }}
          onTouchStart={() => setIsPressed(true)}
          onTouchEnd={() => setIsPressed(false)}
          onTouchCancel={() => setIsPressed(false)}
          onHoverStart={() => setIsHovered(true)}
          onHoverEnd={() => setIsHovered(false)}
          onClick={onClick}
          className={cn(
            "relative z-10 flex items-center justify-center outline-none cursor-pointer overflow-hidden",
            "bg-gradient-to-b from-white/95 via-white/85 to-white/90 dark:from-[#2c2c31] dark:via-[#222226] dark:to-[#1a1a1c]",
            "border border-white/70 dark:border-white/10",
            "focus-visible:ring-2 focus-visible:ring-blue-500 focus-visible:ring-offset-2",
            fullWidth ? "w-full" : "w-auto",
            sizeConfig.box
          )}
          initial={false}
          animate={{
            rotate: isPressed ? sizeConfig.rotate : 0,
            y: isPressed ? sizeConfig.pressedY : isHovered ? -2 : 0,
            x: isPressed ? sizeConfig.pressedX : 0,
            boxShadow: isPressed
              ? "rgba(0, 0, 0, 0.25) -2px -6px 1px 0px inset, rgba(255, 255, 255, 0.9) 0.5px 1.5px 2px 0px inset, rgba(0, 0, 0, 0.12) 8px 10px 14px 0px"
              : isHovered
              ? "rgba(0, 0, 0, 0.20) -2px -7px 1px 0px inset, rgba(255, 255, 255, 0.95) 0.5px 2px 2px 0px inset, rgba(0, 0, 0, 0.12) 4px 6px 12px 0px, rgba(255, 255, 255, 0.7) 0px 1px 0px 0px inset"
              : "rgba(0, 0, 0, 0.20) -2px -6px 1px 0px inset, rgba(255, 255, 255, 0.9) 0.5px 1.5px 1px 0px inset, rgba(0, 0, 0, 0.10) 2px 3px 8px 0px, rgba(255, 255, 255, 0.5) 0px 1px 0px 0px inset",
          }}
          transition={springPhysics}
          {...props}
        >
          {/* Glass Specular Reflection Sheen */}
          <div
            aria-hidden="true"
            className="pointer-events-none absolute inset-x-0 top-0 h-[45%] rounded-t-[14px] bg-gradient-to-b from-white/70 via-white/20 to-transparent dark:from-white/15 dark:to-transparent"
          />

          {/* Liquid Glass Bead LED Indicator */}
          {showIndicator && (
            <motion.span
              aria-hidden="true"
              className={cn(
                "relative z-10 shrink-0 rounded-full",
                sizeConfig.indicator
              )}
              initial={false}
              animate={{
                backgroundColor: getIndicatorBg(),
                boxShadow: getIndicatorGlow(),
              }}
              transition={springPhysics}
            >
              <span
                aria-hidden="true"
                className="absolute top-[1.5px] left-[1.5px] h-[2px] w-[2px] rounded-full bg-white/95"
              />
            </motion.span>
          )}

          {/* Button Text */}
          <span
            className={cn(
              "relative z-10 font-sans text-neutral-800 dark:text-neutral-100 whitespace-nowrap",
              sizeConfig.text
            )}
          >
            {children}
          </span>
        </motion.button>
      </div>
    );
  }
);
TactileRocker.displayName = "TactileRocker";

// ============================================================================
// 2. DISCRETE TAB SELECTOR (Expanding Pill with Shared Layout Projection)
// ============================================================================

export interface TabItem {
  id: string;
  label: string;
  icon?: React.ReactNode;
}

export function DiscreteTabSelector({
  tabs,
  activeId,
  onChange,
  className,
}: {
  tabs: TabItem[];
  activeId: string;
  onChange: (id: string) => void;
  className?: string;
}) {
  return (
    <div
      role="tablist"
      className={cn(
        "inline-flex items-center gap-2 p-1.5 rounded-[30px] bg-neutral-200/80 dark:bg-neutral-900/80 backdrop-blur-md border border-neutral-300 dark:border-neutral-800",
        className
      )}
    >
      {tabs.map((tab) => {
        const isActive = activeId === tab.id;
        return (
          <motion.button
            key={tab.id}
            role="tab"
            aria-selected={isActive}
            onClick={() => onChange(tab.id)}
            layout
            transition={{
              layout: {
                type: "spring",
                damping: 20,
                stiffness: 230,
                mass: 1.2,
              },
            }}
            className={cn(
              "relative flex items-center justify-center gap-2 py-2 cursor-pointer select-none rounded-[24px] outline-none transition-colors duration-150",
              isActive
                ? "bg-white dark:bg-neutral-800 text-neutral-900 dark:text-white px-4 shadow-sm font-medium"
                : "text-neutral-600 dark:text-neutral-400 hover:text-neutral-900 dark:hover:text-white px-3"
            )}
            style={{ willChange: "transform" }}
          >
            {tab.icon && <span className="shrink-0">{tab.icon}</span>}
            <AnimatePresence mode="popLayout" initial={false}>
              {isActive && (
                <motion.span
                  initial={{ opacity: 0, filter: "blur(4px)", scale: 0.95 }}
                  animate={{ opacity: 1, filter: "blur(0px)", scale: 1 }}
                  exit={{ opacity: 0, filter: "blur(4px)", scale: 0.95 }}
                  transition={{
                    duration: 0.22,
                    ease: [0.32, 0.72, 0, 1],
                  }}
                  className="text-xs font-mono uppercase tracking-wider whitespace-nowrap"
                >
                  {tab.label}
                </motion.span>
              )}
            </AnimatePresence>
          </motion.button>
        );
      })}
    </div>
  );
}

// ============================================================================
// 3. COMPLETE DEMO SHOWCASE COMPONENT
// ============================================================================

export default function UseLayoutsShowcaseDemo() {
  const [activeTab, setActiveTab] = React.useState("overview");

  const sampleTabs: TabItem[] = [
    {
      id: "overview",
      label: "Overview",
      icon: (
        <svg className="size-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M4 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2V6zM14 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V6zM4 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2v-2zM14 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2v-2z" />
        </svg>
      ),
    },
    {
      id: "analytics",
      label: "Analytics",
      icon: (
        <svg className="size-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z" />
        </svg>
      ),
    },
    {
      id: "settings",
      label: "Settings",
      icon: (
        <svg className="size-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z" />
          <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
        </svg>
      ),
    },
  ];

  return (
    <div className="flex flex-col items-center justify-center min-h-[460px] p-8 gap-10 bg-[#F5F3EE] dark:bg-[#030202] rounded-3xl border border-neutral-300 dark:border-neutral-800">
      <div className="flex flex-col items-center gap-2 text-center">
        <span className="font-mono text-xs uppercase tracking-widest text-neutral-500">
          Craft &amp; Micro-Interactions
        </span>
        <h3 className="text-2xl font-semibold text-neutral-900 dark:text-white">
          UseLayouts Physicality Demo
        </h3>
      </div>

      {/* Discrete Tabs Demonstration */}
      <DiscreteTabSelector
        tabs={sampleTabs}
        activeId={activeTab}
        onChange={setActiveTab}
      />

      {/* Tactile Rocker Switch Demonstration */}
      <div className="flex flex-wrap items-center justify-center gap-6">
        <TactileRocker size="default" indicatorColor="blue">
          Deploy to Production
        </TactileRocker>
        <TactileRocker size="default" indicatorColor="green">
          System Operational
        </TactileRocker>
      </div>
    </div>
  );
}
