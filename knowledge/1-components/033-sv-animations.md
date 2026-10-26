---
id: "sv-animations"
name: "Svelte Animations (sv-animations)"
url: "https://sv-animations.vercel.app/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Dark Craft & High-Tech Glow", "Svelte 5 Runes Reactive Motion", "Bioluminescent Lineage & Laser Beams", "Kinetic Typography & Grapheme Segmenting", "Modern SaaS Hero Polish"]
densidade_informacao: "Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (motion-sv & CSS Transitions) a Alto (Cobe 3D WebGL Globe & Canvas Shaders)"
stack_frameworks: ["Svelte 5 (Runes)", "SvelteKit", "Tailwind CSS v4", "TypeScript", "motion-sv", "bits-ui", "shadcn-svelte CLI", "cobe (WebGL Globe)", "runed"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Geist Mono", "Figtree", "Inter", "JetBrains Mono", "Space Grotesk"]
  paletas_ideais: ["Deep Zinc Dark Mode (#09090b / zinc-950)", "Neon Glow Prismatic (Amber #ffaa40 to Violet #9c40ff)", "Bioluminescent Cyan & Emerald Accent", "High-Contrast Monochrome with Radial Flash"]
  combinacoes_recomendadas: ["shadcn-svelte (Bits UI)", "Svelte Bits (WebGL shaders)", "Skeleton UI", "Tailwind CSS v4", "Lucide Svelte", "Lenis Smooth Scroll"]
  conflitos_esteticos: ["Corporate Memphis pastel infantil", "Neobrutalism cru com bordas pretas grossas e sem easing", "Material Design 2 com sombras primárias difusas e botões arredondados flutuantes"]
---

# Svelte Animations (sv-animations) — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo engenheiro de software e designer **Sikandar Bhide** (`@SikandarJODD` / `bhide.dev`), o **Svelte Animations** (`sv-animations.vercel.app` / repositório `SikandarJODD/animations`) é o principal centro de gravidade para animações de interface de vanguarda no ecossistema do **Svelte 5**.

Historicamente, o mundo de animações web sofisticadas no estilo "Linear, Vercel, Apple e Raycast" era dominado pelo ecossistema React, impulsionado por bibliotecas como *Magic UI* (de Dillon Verma), *Spell UI* (de Tom / `@tomm_ui`) e *Fancy Components* (de Daniel Petho / `@nonzeroexitcode`). O projeto Svelte Animations realiza uma missão ambiciosa e cirúrgica: unificar e portar fielmente essas três coleções lendárias para a sintaxe reativa moderna do **Svelte 5 (Runes)**, em conjunto com **Tailwind CSS v4** e o motor de física **`motion-sv`** (criado por Hanielu).

Com mais de **88 componentes animados prontos para produção**, o Svelte Animations não é uma biblioteca empacotada monolítica (*npm package bloat*), mas um catálogo distribuído via **shadcn-svelte Registry CLI**, permitindo aos desenvolvedores copiar código-fonte TypeScript limpo diretamente para dentro de seus projetos.

```
┌────────────────────────────────────────────────────────────────────────┐
│                   SV-ANIMATIONS ARSENAL (88+ COMPONENTES)             │
├──────────────────────────┬─────────────────────────┬───────────────────┤
│    Svelte Magic UI       │     Svelte Spell UI     │ Svelte Fancy Comp │
│     (Registry: /r/)      │     (Registry: /s/)     │  (Registry: /f/)  │
├──────────────────────────┼─────────────────────────┼───────────────────┤
│ • 57 Componentes         │ • 21 Componentes        │ • 10+ Componentes │
│ • Border Beam, Anim Beam │ • Words Stagger (Intl)  │ • Scramble Hover  │
│ • Bento Grid, Dock       │ • Perspective Book      │ • Vertical Cut    │
│ • Globe 3D, Meteors      │ • Exploding Input       │ • Parallax Float  │
│ • Shimmer/Ripple Button  │ • Tilt Card, Spotify    │ • Letter 3D Swap  │
│ • Dither Shader, Matrix  │ • Gradient Wave Text    │ • Pixel Trail     │
└──────────────────────────┴─────────────────────────┴───────────────────┘
```

### Os Quatro Pilares da Assinatura Visual & Técnica

1. **Reatividade Cirúrgica via Svelte 5 Runes (Zero Virtual DOM)**:
   Enquanto animações intensivas de mouse e física no React exigem constante preocupação com rerenderizações de árvores virtuais, hooks de memoização (`useMemo`, `useCallback`) e refs mutáveis, no Svelte 5 cada componente do Svelte Animations é estruturado sobre Runes:
   - `$props()` para propriedades tipadas com defaults desestruturados;
   - `$state()` para nós reativos locais que não disparam atualizações desnecessárias em irmãos;
   - `$derived()` para cálculos cinemáticos imediatos (como transformações angulares e coordenadas vetoriais);
   - `$props.id()` para geração determinística e única de IDs de gradientes SVG;
   - Módulos reativos universais `.svelte.ts` (ex: `use-path-calculator.svelte.ts`, `use-resize-observer.svelte.ts`), permitindo que a lógica matemática seja desacoplada da marcação HTML.

2. **O Motor `motion-sv` (A Semântica do Framer Motion em Svelte Nativo)**:
   Para manter a familiaridade intuitiva da física de molas declarativa, o Svelte Animations adota o `motion-sv`. Isso permite expressar componentes utilizando nós `<motion.div>`, `useMotionValue()`, `useTransform()` e `useSpring()` com a precisão do ecossistema Motion, porém compilados diretamente para mutações DOM de altíssima frequência (60 a 120 FPS cravados), sem o runtime de conciliação do React.

3. **Arquitetura Visual "Dark Craft & Bioluminescent Glow"**:
   A biblioteca possui um acabamento visual meticuloso voltado para produtos de alta tecnologia:
   - *Border Beam*: feixes de luz que contornam o perímetro de cartões através de propriedades modernas de `offsetPath: rect(...)` e máscaras de recorte CSS com gradientes angulares.
   - *Animated Beam*: feixes elétricos baseados em curvas de Bézier cúbicas SVG que viajam entre dois elementos da tela dinamicamente calculados em tempo real via ResizeObserver.
   - *Globe 3D*: esfera planetária renderizada via WebGL com a biblioteca ultraleve `cobe`, com rotação suave e pontos bioluminescentes interativos.
   - Texturas táteis de granularidade com *dither-shader* e *noise-texture* que quebram a esterilidade digital de telas planas.

4. **Tipografia Cinética com Segmentação Internacionalizada (`Intl.Segmenter`)**:
   Componentes como *Words Stagger* e *Slide Up Text* abandonam o ingênuo `text.split(" ")` (que quebra com quebras de linha CRLF, emojis com modificadores de tom de pele e idiomas não latinos) e adotam a API nativa do navegador `Intl.Segmenter(undefined, { granularity: "word" | "grapheme" })`, garantindo que revelações tipográficas escalonadas sejam visual e semanticamente perfeitas em qualquer língua.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários

1. **Plataformas de Inteligência Artificial & Agentes Autônomos em SvelteKit**:
   Em ferramentas de IA onde agentes operam em background, componentes como *Animated Beam* (conectando agentes a ferramentas e bancos de vetores), *Typing Animation*, *Terminal* e *Animated Shiny Text* tangibilizam visualmente o fluxo de processamento e dados em tempo real.
2. **DevTools, Infraestrutura em Nuvem & Observabilidade**:
   Projetos voltados para engenheiros sêniores exigem interfaces sóbrias, escuras e densas com feedback preciso. A combinação de *Bento Grid*, *File Tree*, *Arc Timeline*, *Kbd* e *Dotted Map* cria o ecossistema perfeito para documentações interativas, consoles e dashboards de telemetria.
3. **Landing Pages de Alto Impacto para Startups de Tecnologia**:
   Páginas de lançamento que competem por conversão de investidores e adoção rápida de early-adopters encontram no Svelte Animations componentes "showstopper" prontos: *Hero Video Dialog*, *Border Beam*, *Shimmer Button*, *Interactive Hover Button*, *Marquee* e *Globe*.
4. **Portfólios de Design Engineers & Creative Technologists em Svelte**:
   Profissionais que desejam demonstrar domínio das novidades do Svelte 5 e WebGL sem abrir mão da consistência com o padrão shadcn, integrando componentes conceituais do Spell UI e Fancy Components como *Scramble Hover*, *Perspective Book*, *Vertical Cut Reveal* e *Spotify Card*.

### Papel no Ritmo Visual (Regra 60-30-10)

```
┌────────────────────────────────────────────────────────────────────────┐
│                     DISTRIBUIÇÃO DE RITMO VISUAL                      │
├────────────────────────────────────────────────────────────────────────┤
│ 60% FUNDAÇÃO ESTRUTURAL NEUTRA (Base Sóbria)                           │
│     • Superfícies sólidas em Zinc 950 / Slate 950                      │
│     • Bordas sutis em zinc-800/80 e tipografia Geist Sans / Inter       │
│     • Componentes funcionais e sem animação contínua (Bits UI)         │
├────────────────────────────────────────────────────────────────────────┤
│ 30% CAMADA TÁTIL & MICRO-INTERAÇÕES (sv-animations)                    │
│     • Border Beam no card de plano recomendado (Pricing)               │
│     • Dock flutuante inferior para navegação de aplicativo             │
│     • Interactive Hover Button ou Shimmer Button no CTA principal      │
│     • Marquee contínuo de logotipos de clientes parceiros              │
│     • Scramble Hover em palavras de destaque secundário                │
├────────────────────────────────────────────────────────────────────────┤
│ 10% SHOWSTOPPER PROTAGONISTA ÚNICO (O Foco da Viewport)                │
│     • Ou o Globe 3D WebGL no centro da Hero Section                    │
│     • Ou o Animated Beam conectando nós no diagrama de arquitetura     │
│     • Ou Stacking Cards cinematográficos em scroll contínuo            │
│     (ATENÇÃO: Nunca ative dois protagonistas simultaneamente!)         │
└────────────────────────────────────────────────────────────────────────┘
```

- **60% (Fundação Neutra)**: A estrutura da página é limpa, estática e sólida, mantendo foco na legibilidade e no contraste WCAG AA+. O layout é mantido por tokens do Tailwind v4 (`bg-zinc-950 text-zinc-100`).
- **30% (Micro-interações e Camada Tátil)**: Componentes com resposta de feedback de alta fidelidade que reagem ao mouse e ao toque: cards que revelam contornos de luz ao focar, botões que emitem brilho direcional ao hover, e tabs fluidas.
- **10% (Showstopper / Protagonista)**: Apenas **um** grande efeito cenográfico por tela ou seção visível. Se o Hero possui o *Globe 3D*, nenhum outro elemento naquela dobra deve ter animação complexa concorrente.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

1. **Sistemas de Gestão Hospitalar, Financeira Crítica e Conciliação Bancária**:
   Em telas de conciliação de pagamentos com tabelas de 100+ linhas, terminais de ponto de venda ou prontuários médicos, qualquer animação contínua de borda giratória (*Border Beam*) ou efeito de texto embaralhado (*Scramble Hover*) é uma distração imperdoável que gera estresse cognitivo e atrasa decisões operacionais.
2. **Formulários Burocráticos e Telas de Checkout Estritas**:
   Campos de cartão de crédito, telas de autenticação multifator (MFA) e formulários de cadastro governamentais exigem previsibilidade determinística. Botões pulsantes com faíscas (*Rainbow Button*, *Pulsating Button*) em checkouts transmitem instabilidade e falta de maturidade de segurança.
3. **Sistemas Corporativos Tradicionais (LegalTech, Órgãos Públicos, Contabilidade)**:
   A estética Dark Craft com reflexos bioluminescentes e néons colide diretamente com a expectativa sóbria de clientes tradicionais que utilizam temas claros diurnos e tipografias serifadas formais.
4. **Navegadores ou Dispositivos em Modo de Economia de Bateria Sem Detecção**:
   Implementar telas com múltiplos loops de requestAnimationFrame (ex: *Meteors* + *Particles* + *Globe 3D*) sem verificar o status da bateria ou a redução de movimento drena a carga de dispositivos móveis velozmente.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):

- **"Laser Circus" (Sobrecarga de Luzes)**: Incluir na mesma seção um card com `Border Beam`, outro com `Shine Border`, um botão com `Rainbow Button` e o fundo preenchido com `Meteors`. O site se transforma em uma árvore de natal amadora que esgota a atenção do visitante.
- **Scramble Hover em Parágrafos Corridos**: Aplicar o efeito alfanumérico em textos descritivos, termos de serviço ou descrições de produtos. O usuário é forçado a esperar a animação decodificar para conseguir ler o conteúdo básico.
- **Molas sem Amortecimento Adequado (Jelly UI)**: Ajustar parâmetros de `stiffness` baixos demais com `damping` ínfimo no componente `Dock` ou `Tilt Card`, fazendo o cursor parecer atolado em uma gelatina trêmula.
- **Ignorar `@media (prefers-reduced-motion)`**: Não encapsular as animações do `motion-sv` em condições de acessibilidade, provocando náuseas em usuários com distúrbios vestibulares.
- **Esquecer de Destruir Observadores e Loops WebGL**: Deixar de desalocar listeners de mouse ou instâncias de canvas WebGL (como o Cobe Globe) na desmontagem do componente do SvelteKit, causando vazamento de memória (*memory leaks*) ao navegar entre páginas.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

O repositório do Svelte Animations é estruturado em três namespaces oficiais. A seguir estão os 12 componentes mais emblemáticos da biblioteca:

### 1. Border Beam (`static/r/border-beam.json`)
- **Origem**: Magic UI port para Svelte 5.
- **Anatomia Visual**: Uma linha luminosa com gradiente colorido (ex: de `#ffaa40` a `#9c40ff`) que percorre suavemente o perímetro exterior de um cartão arredondado. Utiliza `offset-path: rect(0 auto auto 0 round ...)` e máscara CSS com modo de composição `mask-intersect` para desenhar o feixe exclusivamente dentro da borda de 1px do elemento.
- **Gatilho de Interação**: Animação contínua e infinita (com suporte a delay, duração e inversão de sentido), ativando-se opcionalmente sob foco ou hover.
- **Onde encaixar**: No cartão central e prioritário da seção de **Pricing** (o plano "Pro" ou "Mais Popular") e em cards de destaque do Bento Grid.

### 2. Animated Beam (`static/r/animated-beam.json`)
- **Origem**: Magic UI port para Svelte 5.
- **Anatomia Visual**: Linhas de conexão vetoriais SVG curvas (Bézier cúbica com controle de curvatura) que interligam dois nós ou ícones HTML na página. Um feixe de luz com gradiente viaja pelo interior do traçado SVG, simulando pacotes de dados fluindo entre sistemas.
- **Gatilho de Interação**: Movimento contínuo e sincronizado, acionado dinamicamente via `useResizeObserver.svelte.ts` para recalcular as âncoras mesmo com resize de janela.
- **Onde encaixar**: Seções de **Arquitetura de Dados**, diagramas de integrações de API, páginas de fluxos de IA (conectando LLM, vector database e usuário) na Hero Section ou no Bento Grid.

### 3. Dock & DockIcon (`static/r/dock.json`)
- **Origem**: Magic UI port para Svelte 5.
- **Anatomia Visual**: Barra de navegação inspirada no macOS Dock com cantos arredondados, fundo de vidro fosco (`backdrop-blur-md`) e borda suave. Conforme o mouse se desloca horizontalmente, os ícones mais próximos aumentam de escala progressivamente de acordo com uma curva de distribuição gaussiana.
- **Gatilho de Interação**: Coordenada `mouseX` rastreada via `useMotionValue` e interpolada por física de mola amortecida `useSpring(sizeTransform, { mass: 0.1, stiffness: 150, damping: 12 })`.
- **Onde encaixar**: Como barra de navegação flutuante inferior fixa (*Floating Bottom Navigation*) em Web Apps, painéis de produtividade e portfólios interativos.

### 4. Interactive Hover Button & Shimmer Button (`static/r/interactive-hover-button.json` / `shimmer-button.json`)
- **Origem**: Magic UI port para Svelte 5.
- **Anatomia Visual**: 
  - *Interactive Hover Button*: Um botão circular/retangular em que uma bolha de cor sólida se expande do centro ou da lateral no hover, empurrando o texto e revelando uma seta direcional com física elástica.
  - *Shimmer Button*: Botão com um reflexo de luz linear de 45 graus que desliza periodicamente pela superfície, simulando um acabamento de titânio acetinado.
- **Gatilho de Interação**: Hover do mouse com transição suave e feedback tátil de escala ao clique.
- **Onde encaixar**: No **Call To Action (CTA) principal** da Hero Section e no botão de conversão final da Landing Page.

### 5. Bento Grid & BentoCard (`static/r/bento-grid.json`)
- **Origem**: Magic UI port para Svelte 5.
- **Anatomia Visual**: Grid CSS responsivo e assimétrico com cantos arredondados generosos (`rounded-3xl`), cartões escuros com sobreposição de elementos interativos ao fundo (marques, gráficos, códigos) que reagem ao hover com revelação de CTAs secundários e iluminação sutil.
- **Gatilho de Interação**: Hover sobre os cartões eleva a profundidade z-index visual, ilumina a borda e translada ícones auxiliares.
- **Onde encaixar**: Na seção de **Features Principais (Recursos do Produto)** imediatamente após a Hero Section.

### 6. Interactive 3D Globe via Cobe (`static/r/globe.json`)
- **Origem**: Magic UI port para Svelte 5 (baseado em WebGL `cobe`).
- **Anatomia Visual**: Uma esfera planetária 3D renderizada em Canvas WebGL de alta fidelidade e baixíssimo consumo de memória (menos de 5KB de runtime). Possui rotação automática e marcas bioluminescentes pontuais que representam servidores, nós de rede ou clientes globais.
- **Gatilho de Interação**: Rotação contínua com desaceleração inercial e capacidade de rotação manual por drag do usuário com o cursor.
- **Onde encaixar**: Como plano de fundo tridimensional na **Hero Section** de plataformas de Cloud Global, CDNs, Fintechs internacionais ou plataformas de IA distribuída.

### 7. Scramble Hover (`static/f/scramble-hover.json`)
- **Origem**: Fancy Components port para Svelte 5 (criado originalmente por Daniel Petho).
- **Anatomia Visual**: Ao passar o cursor por uma palavra ou frase, seus caracteres são substituídos rapidamente por glifos e caracteres especiais criptográficos aleatórios (`!@#$%^&*()_+`) em ciclos de alta frequência, estabilizando sequencialmente de volta no texto original.
- **Gatilho de Interação**: Disparado pelo evento `onmouseenter` e cancelado suavemente no `onmouseleave`.
- **Onde encaixar**: Em títulos de seção de DevTools, badges de status "Cybersecurity Certified", botões de terminal e links de navegação secundária.

### 8. Vertical Cut Reveal & Letter 3D Swap (`static/f/vertical-cut-reveal.json` / `letter-3d-swap.json`)
- **Origem**: Fancy Components port para Svelte 5.
- **Anatomia Visual**: 
  - *Vertical Cut Reveal*: O texto é recortado horizontalmente ao meio como por uma navalha; no hover ou entrada em tela, a metade superior sobe e a metade inferior desce, revelando um novo texto ou cor por dentro com corte de máscara perfeito (`overflow-hidden`).
  - *Letter 3D Swap*: Cada caractere gira em um eixo 3D X (`rotateX(90deg)`) individualmente escalonado com delay (*stagger*), simulando um painel de partidas de aeroporto futurista.
- **Gatilho de Interação**: Entrada em tela (*in-view*) com threshold de scroll ou hover.
- **Onde encaixar**: No **H1 Principal da Hero Section** ou em cabeçalhos de casos de sucesso de portfólios criativos.

### 9. Words Stagger & Blur Reveal (`static/s/words-stagger.json` / `blur-reveal.json`)
- **Origem**: Spell UI port para Svelte 5 (inspirado no trabalho de Tom).
- **Anatomia Visual**: Frases que surgem na tela palavra por palavra utilizando `Intl.Segmenter` nativo para quebra gramatical correta. Cada palavra emerge com translação vertical suave (`translateY(20px) -> 0px`), opacidade (`0 -> 1`) e desfoque gaussiano inverso (`filter: blur(8px) -> blur(0px)`).
- **Gatilho de Interação**: Disparo automático quando o elemento entra no campo de visão do usuário (`useInView`).
- **Onde encaixar**: Subtítulo explicativo do Hero, citações de depoimentos de clientes e frases de manifesto de produto.

### 10. Perspective Book & Tilt Card (`static/s/perspective-book.json` / `tilt-card.json`)
- **Origem**: Spell UI port para Svelte 5.
- **Anatomia Visual**:
  - *Perspective Book*: Renderização 3D CSS pura de um livro físico com espinha dorsal, capa e páginas internas com textura de sombra realista que se abre ou se inclina no espaço tridimensional conforme o ponteiro se move.
  - *Tilt Card*: Cartão com perspectiva CSS (`perspective: 1000px`) que calcula o ângulo de inclinação vetorial baseado na distância euclidiana do mouse até o centro da caixa, gerando reflexos dinâmicos.
- **Gatilho de Interação**: Eventos `mousemove` locais convertidos para rotações nos eixos `rotateX` e `rotateY`.
- **Onde encaixar**: Apresentação de e-books técnicos, guias de documentação em PDF, vitrines de livros e cartões de planos anuais.

### 11. Marquee & Logo Carousel (`static/r/marquee.json` / `static/s/logo-carousel.json`)
- **Origem**: Magic UI e Spell UI ports para Svelte 5.
- **Anatomia Visual**: Faixa contínua com deslocamento horizontal infinito e suave de cartões, depoimentos ou logotipos em escala de cinza com máscaras de gradiente nas bordas esquerda e direita (`mask-image: linear-gradient(...)`).
- **Gatilho de Interação**: Movimento contínuo acelerado por hardware via CSS translate puro, pausando suavemente quando o usuário posiciona o cursor sobre o carrossel (`hover:pause`).
- **Onde encaixar**: Seção de **Social Proof (Logotipos de Clientes e Parceiros)** e carrossel de depoimentos do Twitter/X.

### 12. Dither Shader & Noise Texture (`static/r/dither-shader.json` / `noise-texture.json`)
- **Origem**: Creative Coding & Shaders port para Svelte 5.
- **Anatomia Visual**: Filtro de pós-processamento gráfico que aplica uma matriz de pontilhado retrô monocromático (*ordered dithering* estilo Macintosh dos anos 80 ou GameBoy) sobre imagens ou vídeos, gerando um contraste gráfico tátil inconfundível.
- **Gatilho de Interação**: Renderização contínua com modulação de intensidade via props de brilho e densidade de matriz.
- **Onde encaixar**: Fundos de cartões técnicos de engenharia, imagens de apresentação de hardware e cabeçalhos de artigos de blog técnico.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Ambiente

O Svelte Animations foi desenhado especificamente para o stack moderno de ponta do SvelteKit com Tailwind CSS v4.

```bash
# 1. Criação do projeto moderno com SvelteKit (Svelte 5)
pnpm dlx sv create meu-app-svelte
# Selecione: SvelteKit minimal, TypeScript, Tailwind CSS

# 2. Inicialização do Shadcn Svelte
pnpm dlx shadcn-svelte@latest init

# 3. Instalação das dependências centrais de animação
pnpm add motion-sv runed bits-ui clsx tailwind-merge
pnpm add -D @lucide/svelte @tailwindcss/vite
```

### Instalação de Componentes via Shadcn Registry CLI

Cada sub-biblioteca possui seu endpoint dedicado no servidor Vercel do autor:
- Para componentes **Magic UI**: `/r/<componente>.json`
- Para componentes **Spell UI**: `/s/<componente>.json`
- Para componentes **Fancy Components**: `/f/<componente>.json`

```bash
# Instalando o Border Beam (Magic UI port)
pnpm dlx shadcn-svelte@latest add https://sv-animations.vercel.app/r/border-beam.json

# Instalando o Dock (Magic UI port)
pnpm dlx shadcn-svelte@latest add https://sv-animations.vercel.app/r/dock.json

# Instalando o Words Stagger (Spell UI port)
pnpm dlx shadcn-svelte@latest add https://sv-animations.vercel.app/s/words-stagger.json

# Instalando o Scramble Hover (Fancy Components port)
pnpm dlx shadcn-svelte@latest add https://sv-animations.vercel.app/f/scramble-hover.json
```

---

### Física de Movimento & Curvas Matemáticas

| Padrão de Movimento | Motor | Parâmetros de Física / Curva | Sensação Tátil / Propósito |
| :--- | :--- | :--- | :--- |
| **Dock Icon Hover** | `motion-sv` Spring | `mass: 0.1, stiffness: 150, damping: 12` | Mola rápida e amortecida, zero oscilação excessiva (sensação Apple macOS) |
| **Tactile Button Press** | `motion-sv` Spring | `mass: 0.05, stiffness: 350, damping: 25` | Clique seco, mecânico e preciso (teclado mecânico tactile switch) |
| **Border Beam Track** | CSS Moderno | `linear`, `duration: 6s - 12s`, `repeat: Infinity` | Fluxo orbital contínuo de energia sem desaceleração |
| **Slide Up / Blur In** | CSS / `motion-sv` | `cubic-bezier(0.16, 1, 0.3, 1)` (Quart Out) | Revelação "snappy" com desaceleração rápida e suave |
| **Tilt Card Rotation** | Svelte Derived | Linear clamped com limite angular de `±15deg` | Superfície tridimensional pesada sob controle do usuário |

---

### Receitas de Código em Svelte 5

#### Receita 1: `BorderBeam.svelte` (Anatomia do Efeito de Borda Neon)

Este componente demonstra o uso avançado das Runes do Svelte 5 com `motion-sv` e CSS Masking com coordenadas `offsetPath`:

```svelte
<!-- src/lib/components/magic/border-beam.svelte -->
<script lang="ts">
	import { motion, type Transition } from "motion-sv";
	import { cn } from "$lib/utils";

	interface BorderBeamProps {
		size?: number;
		duration?: number;
		delay?: number;
		colorFrom?: string;
		colorTo?: string;
		transition?: Transition;
		class?: string;
		style?: string;
		reverse?: boolean;
		initialOffset?: number;
		borderWidth?: number;
	}

	let {
		class: className,
		size = 60,
		delay = 0,
		duration = 8,
		colorFrom = "#ffaa40",
		colorTo = "#9c40ff",
		transition,
		reverse = false,
		initialOffset = 0,
		borderWidth = 1.5,
	}: BorderBeamProps = $props();

	// Variáveis CSS calculadas reativamente via Runes do Svelte 5
	const containerStyle = $derived(`--border-beam-width: ${borderWidth}px;`);

	const beamStyle = $derived({
		width: size,
		offsetPath: `rect(0 auto auto 0 round ${size}px)`,
		"--color-from": colorFrom,
		"--color-to": colorTo,
	} as any);

	const animateConfig = $derived({
		offsetDistance: reverse
			? [`${100 - initialOffset}%`, `${-initialOffset}%`]
			: [`${initialOffset}%`, `${100 + initialOffset}%`],
	});

	const transitionConfig = $derived({
		repeat: Infinity,
		ease: "linear" as const,
		duration,
		delay: -delay,
		...transition,
	} as any);
</script>

<div
	class="pointer-events-none absolute inset-0 rounded-[inherit] border-(length:--border-beam-width) border-transparent [mask-clip:padding-box,border-box] [mask-composite:intersect] mask-[linear-gradient(transparent,transparent),linear-gradient(#000,#000)]"
	style={containerStyle}
>
	<motion.div
		class={cn(
			"absolute aspect-square bg-gradient-to-l from-(--color-from) via-(--color-to) to-transparent",
			className
		)}
		style={beamStyle}
		initial={{ offsetDistance: `${initialOffset}%` }}
		animate={animateConfig}
		transition={transitionConfig}
	/>
</div>
```

---

#### Receita 2: `Dock.svelte` & `DockIcon.svelte` (Menu Estilo macOS com Física de Mola)

Exemplo de arquitetura com Contexto Svelte 5 e interpolação por molas amortecidas via `motion-sv`:

```svelte
<!-- src/lib/components/magic/dock.svelte -->
<script lang="ts" module>
	import type { MotionValue } from "motion-sv";
	import type { Snippet } from "svelte";

	export interface DockProps {
		class?: string;
		iconSize?: number;
		iconMagnification?: number;
		iconDistance?: number;
		children: Snippet;
	}

	export interface DockContext {
		mouseX: MotionValue<number>;
		iconSize: number;
		iconMagnification: number;
		iconDistance: number;
	}
</script>

<script lang="ts">
	import { useMotionValue } from "motion-sv";
	import { setContext } from "svelte";
	import { cn } from "$lib/utils";

	let {
		class: className,
		iconSize = 40,
		iconMagnification = 64,
		iconDistance = 140,
		children,
	}: DockProps = $props();

	const mouseX = useMotionValue(Infinity);

	setContext<DockContext>("dock", {
		mouseX,
		iconSize,
		iconMagnification,
		iconDistance,
	});

	function handleMouseMove(e: MouseEvent) {
		mouseX.set(e.pageX);
	}

	function handleMouseLeave() {
		mouseX.set(Infinity);
	}
</script>

<nav
	onmousemove={handleMouseMove}
	onmouseleave={handleMouseLeave}
	class={cn(
		"flex h-[58px] items-end gap-3 rounded-2xl border border-zinc-800/80 bg-zinc-950/70 px-4 pb-2 backdrop-blur-xl shadow-2xl shadow-black/60",
		className
	)}
>
	{@render children()}
</nav>
```

```svelte
<!-- src/lib/components/magic/dock-icon.svelte -->
<script lang="ts">
	import { motion, useTransform, useSpring } from "motion-sv";
	import { getContext, type Snippet } from "svelte";
	import { cn } from "$lib/utils";
	import type { DockContext } from "./dock.svelte";

	interface DockIconProps {
		class?: string;
		children: Snippet;
	}

	let { class: className, children }: DockIconProps = $props();
	const dockContext = getContext<DockContext>("dock");

	let el: HTMLDivElement | null = $state(null);

	// Distância euclidiana horizontal entre cursor e o centro do ícone
	const distanceCalc = useTransform(dockContext.mouseX, (val: number) => {
		const bounds = el?.getBoundingClientRect() ?? { x: 0, width: 0 };
		return val - bounds.x - bounds.width / 2;
	});

	// Transformação progressiva de diâmetro
	const sizeTransform = useTransform(distanceCalc, (dist: number) => {
		const size = dockContext.iconSize;
		const mag = dockContext.iconMagnification;
		const maxDist = dockContext.iconDistance;

		if (Math.abs(dist) >= maxDist) return size;
		const progress = 1 - Math.abs(dist) / maxDist;
		return size + (mag - size) * progress;
	});

	// Mola amortecida de alta precisão
	const scaleSize = useSpring(sizeTransform, {
		mass: 0.1,
		stiffness: 150,
		damping: 12,
	});
</script>

<motion.div
	bind:ref={el}
	style={{ width: scaleSize, height: scaleSize }}
	class={cn(
		"flex aspect-square cursor-pointer items-center justify-center rounded-xl bg-zinc-900 border border-zinc-800 text-zinc-300 hover:text-white transition-colors",
		className
	)}
>
	{@render children()}
</motion.div>
```

---

#### Receita 3: Aplicação na Hero Section (Composição Realista)

```svelte
<!-- src/routes/+page.svelte -->
<script lang="ts">
	import BorderBeam from "$lib/components/magic/border-beam.svelte";
	import Dock from "$lib/components/magic/dock.svelte";
	import DockIcon from "$lib/components/magic/dock-icon.svelte";
	import { Terminal, Cpu, Database, Cloud, Sparkles, ArrowRight } from "lucide-svelte";
</script>

<main class="relative min-h-screen bg-zinc-950 text-zinc-100 flex flex-col items-center justify-between p-8 overflow-hidden">
	<!-- Background Grid Sutil -->
	<div class="pointer-events-none absolute inset-0 bg-[linear-gradient(to_right,#27272a15_1px,transparent_1px),linear-gradient(to_bottom,#27272a15_1px,transparent_1px)] bg-[size:32px_32px]"></div>

	<!-- Hero Center: Headline & Showstopper Card -->
	<section class="relative z-10 max-w-4xl w-full flex flex-col items-center text-center mt-16 space-y-8">
		<div class="inline-flex items-center gap-2 rounded-full border border-zinc-800 bg-zinc-900/60 px-4 py-1.5 text-xs text-zinc-400 backdrop-blur-md">
			<Sparkles class="size-3.5 text-amber-400" />
			<span>Arquitetura Reativa Svelte 5 + motion-sv</span>
		</div>

		<h1 class="text-5xl sm:text-7xl font-semibold tracking-tight text-white max-w-3xl leading-[1.1]">
			Orquestre agentes de IA com <span class="bg-gradient-to-r from-amber-400 via-rose-400 to-violet-500 bg-clip-text text-transparent">precisão atômica</span>.
		</h1>

		<!-- Card de Destaque com Border Beam -->
		<div class="relative w-full max-w-2xl rounded-2xl border border-zinc-800 bg-zinc-900/40 p-8 shadow-2xl backdrop-blur-md">
			<BorderBeam size={100} duration={8} colorFrom="#f59e0b" colorTo="#8b5cf6" />
			
			<div class="flex flex-col items-center text-center space-y-4">
				<p class="text-zinc-400 text-sm sm:text-base leading-relaxed">
					Infraestrutura compilada sem Virtual DOM. Respostas com latência inferior a 12ms e consumo de CPU reduzido em 68%.
				</p>
				<button class="inline-flex items-center gap-2 px-6 py-3 rounded-xl bg-white text-zinc-950 font-medium text-sm hover:bg-zinc-200 transition-all shadow-lg shadow-white/10 active:scale-95">
					Iniciar Integração Gratuita
					<ArrowRight class="size-4" />
				</button>
			</div>
		</div>
	</section>

	<!-- Floating Dock de Navegação Inferior -->
	<div class="fixed bottom-6 z-50">
		<Dock>
			<DockIcon><Terminal class="size-5" /></DockIcon>
			<DockIcon><Cpu class="size-5" /></DockIcon>
			<DockIcon><Database class="size-5" /></DockIcon>
			<DockIcon><Cloud class="size-5" /></DockIcon>
		</Dock>
	</div>
</main>
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma nova interface de software que utilize o **Svelte Animations (sv-animations)**, a IA deve incorporar estritamente as seguintes regras arquiteturais e de especificação:

### 1. Declaração do Stack de Animação no Blueprint
- **Framework Principal**: `Svelte 5` com `SvelteKit 2`.
- **Motor de Física**: `motion-sv` para primitivas declarativas (`<motion.div>`, `useSpring`, `useMotionValue`).
- **Framework de Estilos**: `Tailwind CSS v4` com suporte a variáveis de interpolação CSS modernas (`border-(length:...)`).
- **CLI de Registro**: shadcn-svelte (`https://sv-animations.vercel.app/r/...`).

### 2. Mapeamento de Rotas dos Registries por Intenção de Design
- Para **elementos de estrutura, heróis e conversão (Magic UI)**: utilizar a raiz `/r/` (ex: `border-beam.json`, `animated-beam.json`, `dock.json`, `shimmer-button.json`).
- Para **micro-interações táteis e componentes conceituais (Spell UI)**: utilizar o namespace `/s/` (ex: `words-stagger.json`, `perspective-book.json`, `tilt-card.json`).
- Para **tipografia cinética e efeitos de corte de texto (Fancy Components)**: utilizar o namespace `/f/` (ex: `scramble-hover.json`, `vertical-cut-reveal.json`).

### 3. Matriz de Governança 60-30-10
- **Regra de Ouro**: É expressamente proibido combinar mais de um efeito com animação contínua (*infinite loops*) na mesma viewport. Se o `Globe` 3D for ativado na Hero Section, proíba o uso de `Meteors`, `Particles` e `Animated Beam` na mesma área visível.
- **Acessibilidade Obrigatória**: Sempre declarar suporte ao modo `prefers-reduced-motion: reduce`, desligando translações contínuas e mantendo estados finais estáticos de opacidade 100%.
- **Performance de Memória**: Todos os componentes baseados em canvas WebGL ou escuta de eventos globais de ponteiro (`mousemove`) devem conter rotinas explícitas de cancelamento e desmontagem no ciclo de vida do SvelteKit para evitar memory leaks em navegações do lado do cliente.
