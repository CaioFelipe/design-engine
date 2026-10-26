---
id: "motion-core-dev"
name: "Motion Core"
url: "https://motion-core.dev/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Dark Craft & Inset Precision", "WebGL & OGL Canvas Systems", "GSAP Timeline Choreography", "Svelte 5 Runes & Snippets Native", "Un-Library Copy-Paste Registry"]
densidade_informacao: "Media"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Alto (Canvas/3D WebGL) a Medio (GSAP/CSS)"
stack_frameworks: ["Svelte 5 (Runes & Snippets)", "GSAP 3", "OGL (Minimal WebGL)", "Tailwind CSS v4 (OKLCH)", "TypeScript", "Rust-based CLI (@motion-core/cli)"]
compatibilidade:
  fontes_ideais: ["Berkeley Mono", "Geist Sans", "Inter", "Plus Jakarta Sans", "JetBrains Mono"]
  paletas_ideais: ["Deep Violet-Zinc OKLCH (Hue 265)", "Electric Amber Accent (oklch 0.6996 0.201959 44.4414)", "Monochrome Shimmer / Liquid Chrome", "High-Contrast Inset Dark Mode"]
  combinacoes_recomendadas: ["shadcn/ui (Svelte/React)", "Bits UI", "Lucide Icons", "Lenis Smooth Scroll", "Three.js / ShaderToy Shaders", "Framer Motion (para ports React)"]
  conflitos_esteticos: ["Brutalismo neo-pop espalhafatoso com bordas pretas 4px", "Neumorfismo pastel de baixo contraste", "Layouts corporativos antiquados sem aceleração por hardware", "Sistemas com excesso de sombras difusas coloridas desalinhadas"]
---

# Motion Core — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e concebido pelo engenheiro de software e creative technologist **Marek Jóźwiak** (`kaltwrk`), o **Motion Core** (`motion-core.dev`) é um marco na engenharia de interfaces contemporânea. Nascido da constatação de que o ecossistema Svelte carecia de uma suíte de motion e shaders de padrão *Awwwards/FWA*, o projeto une a revolução reativa do **Svelte 5** (runes e snippets) à potência de motores gráficos consolidados na indústria: **GSAP** para orquestração temporal milimétrica e **OGL** para renderização WebGL ultraleve e de alto desempenho.

Em vez de se fechar em uma dependência monolítica pesada no `npm`, o Motion Core adota com rigor a filosofia da **"Un-Library"** — um registro aberto e distribuído via CLI construída em Rust (`@motion-core/cli`), fortemente inspirado pela arquitetura de cópia e apropriação do `shadcn/ui`. O desenvolvedor não baixa um pacote opaco: ele injeta os componentes diretamente em seu repositório local (tipicamente `$lib/motion-core`), possuindo total soberania sobre o código-fonte, os shaders GLSL e as timelines GSAP.

A assinatura visual do Motion Core distingue-se por quatro pilares técnicos e estéticos:

1. **A Fundamentação Cromática OKLCH Violet-Zinc (`--base-hue: 265`):**
   Diferente de interfaces dark mode que utilizam preto puro (`#000000`) — achatando profundidades — ou cinzas neutros frios genéricos, o Motion Core calibra toda a sua paleta no espaço de cor perceptualmente uniforme **OKLCH**, ancorada em um matiz de base 265 (um violeta profundo quase imperceptível que confere sofisticação de metal trabalhado).
   - `background-inset`: `oklch(0.2099 0.0039 265)` — fundo rebaixado tátil com sensação de cavidade esculpida.
   - `background` (elevado): `oklch(0.2574 0.0056 265)` — placas de conteúdo com elevação suave.
   - `border`: `oklch(0.999 0.013 265 / 0.05)` — micro-bordas translúcidas de precisão cirúrgica de 1px.
   - `accent`: `oklch(0.6996 0.201959 44.4414)` — um âmbar-elétrico quente e vibrante (matiz 44.4), aplicado cirurgicamente em pontos focais de ação, acoplamentos de menu e ênfases tipográficas.

2. **A Assinatura Cinética "Motion Core Ease":**
   Todas as transições de painéis, layouts e navegação do ecossistema operam sob uma curva canônica proprietária:
   $$\text{cubic-bezier}(0.625, 0.05, 0, 1)$$
   Registrada no GSAP através do plugin `CustomEase` como `"motion-core-ease"` e exportada em classes de transição CSS Tailwind (`ease-[cubic-bezier(0.625,0.05,0,1)]`), essa curva oferece um disparo de aceleração inicial explosivo seguido por uma desaceleração viscosa e elegante, eliminando a rigidez mecânica das curvas convencionais de `ease-out`.

3. **A Tríade Svelte 5 + GSAP + OGL:**
   - **Svelte 5 Runes (`$state`, `$derived`, `$props`, `$effect`):** O gerenciamento de estado das interações e ciclo de vida do DOM é instantâneo e livre do overhead de reconciliação de VDOMs tradicionais.
   - **GSAP (GreenSock):** Responsável pelas sequências com múltiplos alvos sincronizados, inversão dinâmica de timelines (`timeline.reverse()`), morphings e reações táteis com `quickTo`.
   - **OGL (Minimal WebGL Library):** Em vez de embutir os mais de 600 KB do Three.js para renderizar um efeito de superfície ou distorção, o Motion Core utiliza a biblioteca OGL (criada por Nathan Gordon / Eugene Zatepyakin), mantendo shaders complexos (refrações, aberrações cromáticas, fluidos) em pacotes mínimos de alta taxa de quadros (60 a 120 FPS).

4. **Acabamento "Craft Hardware" e Micro-Raios:**
   O design system estabelece um raio de borda base de `--radius-base: 0.275rem` (4.4px). Os componentes exibem cantos suavemente aparados (`rounded-sm` a `rounded-md`), conferindo o aspecto de consoles de estúdio ou hardware aeroespacial, fugindo dos raios ultra-arredondados infantis comuns na web contemporânea.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **Landing Pages de Ferramentas para Desenvolvedores (DevTools) & Infraestrutura:**
   Produtos que comunicam alta precisão técnica (consoles de cloud, runtimes, orquestradores de containers, bancos de dados). A paleta escura OKLCH combinada a canvas WebGL como `LiquidMetal` ou `InteractiveGrid` transmite domínio de engenharia.
2. **Plataformas de Inteligência Artificial & Computação Criativa:**
   Interfaces de modelos generativos, estúdios de síntese de mídia e copilots que requerem fundos atmosféricos orgânicos (`FluidSimulation`, `NeuralNoise`, `Halo`) para tangibilizar o processamento autônomo.
3. **Estúdios de Design, Creative Technologists & Portfólios Flagship:**
   Apresentações profissionais onde a sensibilidade do movimento é o próprio produto, utilizando o menu cortina `UnderlayNavigation` e galerias imersivas como `InfiniteGallery` ou `RadialGallery`.
4. **Hardware Tech, Automotivo & E-commerce de Luxo Industrial:**
   Showcases de relógios, dispositivos eletrônicos premium e equipamentos de áudio de alta fidelidade onde efeitos de refração vítrea (`GlassPane`, `GlassLogo`) e luzes especulares (`SpecularBand`, `GodRays`) amplificam o valor percebido do objeto.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Neutra e Estrutura Inset):**
  Paredes de fundo em `oklch(0.2099 0.0039 265)` (`bg-background-inset`), cartões elevados com micro-sombras inset `inset-shadow` e tipografia técnica secundária em fonte monospace (*Berkeley Mono* ou *Geist Mono*). Essa base silenciosa sustenta os gráficos sem poluição visual.
- **30% (Camada de Fluidez e Cinética Interativa):**
  A mecânica tátil de uso contínuo: botões magnéticos com mola elástica (`Magnetic`), rotação de palavras-chave com desfoque e ajuste de largura (`TextLoop`), doc de rodapé com magnificação parabólica (`MacOSDock`) e abertura do menu com retração de primeiro plano (`UnderlayNavigation`).
- **10% (Showstopper de Culminância & Shaders WebGL):**
  O elemento protagonista que fixa a identidade visual na memória do usuário: a simulação de fluidos navegável por cursor (`FluidSimulation`) no topo da dobra, o globo 3D com atmosfera Fresnel (`Globe`) ou o metal líquido refrativo (`LiquidMetal`). Apenas um efeito WebGL dessa magnitude deve dominar a viewport por vez.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Painéis de Controle com Múltiplas Visualizações Simultâneas de Dados (High-Density BI):**
  Em sistemas analíticos com 20 gráficos de telemetria ou tabelas de 50 colunas, instanciar componentes com loops de render WebGL disputa threads da GPU e bateria desnecessariamente.
- **Formulários Críticos de Checkout e Telas Transacionais Reguladas:**
  Em portais de pagamento bancário ou assinaturas contratuais, efeitos magnéticos em botões ou rotações automáticas de texto em títulos provocam ansiedade e sensação de desvio de foco.
- **Dispositivos Móveis de Baixa Potência em Modo de Economia de Energia:**
  Shaders de pós-processamento com múltiplos passes de difusão ou raymarching pesado causam queda térmica (*thermal throttling*) e perda de fluidez.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **Multi-Canvas Explosion (Crash de Contextos WebGL):**
  Adicionar 4 ou 5 componentes de Canvas na mesma página (`Globe`, `LiquidMetal`, `FluidSimulation` e `WaterRipple`). Os navegadores impõem um limite rigoroso de contextos WebGL ativos (geralmente entre 8 e 16 por processo). Ao atingir o limite, o navegador destrói contextos silenciosamente, causando telas pretas e o erro `CONTEXT_LOST_WEBGL`.
- **TextLoop em Chamadas Primárias de Conversão (Hero H1) sem Considerar SEO:**
  Aplicar o componente `TextLoop` no H1 sem fornecer marcação estática legível por rastreadores de busca ou leitores de tela. O texto dinâmico que alterna via animação pode não ser indexado integralmente ou sobrecarregar a leitura de acessibilidade.
- **Botões Magnéticos com Raio de Atração Exagerado:**
  Configurar áreas magnéticas de 150px em torno de botões posicionados lado a lado. O cursor do usuário fica preso em zonas de disputa entre botões adjacentes, prejudicando o apontamento preciso.
- **Falta de Desligamento de Loops de Animação em Abas Ocultas:**
  Deixar o loop do `requestAnimationFrame` ou timelines GSAP rodando continuamente quando a janela perde a visibilidade (`document.hidden`). O Motion Core implementa checagens de visibilidade em seus componentes internos; ao portá-los, esse guardrail nunca deve ser omitido.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão 12 dos componentes mais emblemáticos do ecossistema Motion Core, abrangendo as categorias de Canvas WebGL, Navegação, Tipografia e Micro-Interações de Ponteiro:

### 1. UnderlayNavigation (`Navigation: Underlay Navigation`)
- **Anatomia Visual:** Padrão de navegação cinematográfico de tela cheia. Ao clicar no botão de gatilho, a tela de primeiro plano inteira (`foreground`) encolhe sutilmente em escala proporcional ($scale \approx 0.96$), arredonda seus cantos externos e desliza lateralmente para a esquerda como uma cortina mecânica pesada. Por baixo, o painel de navegação (`underlay`) é revelado na direita, contendo links em tipografia display de grande porte com entrada escalonada (*stagger*).
- **Gatilho de Interação:** Clique no botão de alternância (que faz morphing textual de "Menu" para "Close" enquanto duas linhas finas animam via rotação cruzada). Suporta clique fora para recolher e tecla Escape.
- **Onde encaixar:** Navegação principal global de portfólios imersivos, landing pages de agências criativas e sites de tecnologia experimental.

### 2. LiquidMetal (`Canvas: Liquid Metal`)
- **Anatomia Visual:** Shader WebGL de superfície inteira acionado por OGL. Simula uma película fluida de metal líquido escuro com ondas orgânicas distorcidas. Apresenta refração luminosa em tons claros (`color: #FFFFFF`) sobre fundo profundo (`backgroundColor: #17181A`), com separação física dos canais RGB (aberração cromática sutil nas cristas das dobras).
- **Gatilho de Interação:** Movimento perpétuo com frequência ajustável ($f=3.5$) acelerado sutilmente pelo arraste do cursor ou velocidade de rolagem da página.
- **Onde encaixar:** Fundo de seções Hero de produtos de software avançado, cartões de grande porte em Bento Grids ou backgrounds de seções de encerramento (CTA final).

### 3. Globe (`Canvas: Globe`)
- **Anatomia Visual:** Globo tridimensional completo renderizado em WebGL via OGL. Exibe malha de continentes vetoriais de alta precisão, atmosfera envolvente iluminada por modelo de **Fresnel** (brilho difuso nas bordas externas em gradiente suave), halo atmosférico e marcadores dinâmicos pulsantes com coordenadas de latitude/longitude para narrativa de infraestrutura global.
- **Gatilho de Interação:** Rotação automática suave no eixo Y; controle manual e interativo via arraste com mouse (com amortecimento inercial) e foco cinético em cidades/nós selecionados.
- **Onde encaixar:** Seções de rede de entrega global (Edge CDN), distribuição de datacenters de IA, páginas de clientes internacionais ou seções de segurança/cloud.

### 4. FluidSimulation (`Canvas: Fluid Simulation`)
- **Anatomia Visual:** Simulação de mecânica de fluidos de tempo real baseada nas equações de Navier-Stokes executadas na GPU via fragment shaders. Ao mover o cursor sobre o canvas, filamentos de densidade e cores reativas são injetados no fluido, dissipando-se, colidindo e gerando vórtices turbulentos realistas.
- **Gatilho de Interação:** Rastreamento contínuo de coordenadas $(x, y)$ e velocidade instantânea do ponteiro do mouse ou toques touchscreen.
- **Onde encaixar:** Primeira dobra (Hero) de estúdios interativos, telas de introdução interativas ou experiências imersivas de marca.

### 5. TextLoop (`Typography: Text Loop`)
- **Anatomia Visual:** Primitiva tipográfica de morphing textual. Uma palavra dentro de uma frase é continuamente substituída por termos de uma lista. Ao alternar, o contêiner pai interpola suavemente sua largura via `power2.inOut` para acomodar o comprimento exato da nova palavra sem quebrar a linha. A palavra anterior sobe com desfoque vertical progressivo (`blur(6px)` e `yPercent: -50`), enquanto a nova surge de baixo com `blur(8px)` retornando a zero com easing de retorno elástico suave (`back.out(1.2)`).
- **Gatilho de Interação:** Temporizador automático em loop (intervalo padrão de 2000ms), com pausa instantânea caso a aba fique oculta (`document.hidden`).
- **Onde encaixar:** Título principal do Hero (`H1`), slogans institucionais ("Construa software mais [rápido | seguro | inteligente]"), ou destaques de propostas de valor.

### 6. Magnetic (`Pointer: Magnetic Button`)
- **Anatomia Visual:** Envoltório para elementos interativos (botões, ícones, badges). Ao aproximar o cursor do mouse dentro de uma zona de influência, o elemento é atraído na direção do ponteiro como se estivesse sob a ação de um ímã. O movimento é suavemente amortecido via função `gsap.quickTo` e, ao sair o cursor, retorna ao centro com um estalo elástico suave (`elastic.out(1, 0.3)`).
- **Gatilho de Interação:** Eventos nativos `mousemove` e `mouseleave` sobre a caixa delimitadora com cálculo de offsets em relação ao centro $(x - \text{cx}, y - \text{cy})$.
- **Onde encaixar:** Botões de ação primária (CTA), botões flutuantes de suporte/chat, ícones sociais no rodapé e botões de play em mídias.

### 7. InfiniteGallery (`Canvas: Infinite Gallery`)
- **Anatomia Visual:** Galeria WebGL de planos infinitos em perspectiva 3D. Em vez de elementos DOM pesados que degradam com o número de nós, cada imagem é uma textura mapeada em malha (*mesh plane*) dentro do OGL. As imagens fluem continuamente em um plano tridimensional com deformações de curvatura sutil nas bordas da lente da câmera.
- **Gatilho de Interação:** Rolagem vertical ou horizontal do usuário, com física de inércia e escala dinâmica das imagens mais próximas do centro óptico da câmera.
- **Onde encaixar:** Mostruários de portfólio criativo, galerias de fotos de produtos em vestuário de luxo ou cases de sucesso.

### 8. FloatingMenu (`Navigation: Floating Menu`)
- **Anatomia Visual:** Barra de navegação tipo "ilha flutuante" centralizada na parte inferior ou superior da tela. Construída sobre um gatilho de ativação cruzada: ao expandir, revela opções com efeito cascata (*staggered reveal*), desfoque de fundo em vidro fosco (`backdrop-blur-md`) e micro-bordas iluminadas.
- **Gatilho de Interação:** Hover expansivo ou clique de fixação com timeline GSAP sincronizada.
- **Onde encaixar:** Navbar principal de landing pages modernas, barras de ferramentas flutuantes de editores web ou controles rápidos de mídia.

### 9. MacOSDock (`Pointer: macOS Dock`)
- **Anatomia Visual:** Barra de ícones inspirada no dock do macOS. Conforme o cursor se move horizontalmente sobre os ícones, eles sofrem uma magnificação proporcional calculada por uma curva de Gauss baseada na proximidade física do ponteiro. Os ícones vizinhos elevam-se harmonicamente sem quebras de layout.
- **Gatilho de Interação:** Movimento do ponteiro no eixo X com interpolação contínua de escala e largura.
- **Onde encaixar:** Docks de navegação inferior em aplicações desktop web, barras de ferramentas em workspaces de IA e portfólios pessoais.

### 10. DitheredImage (`Canvas: Dithered Image`)
- **Anatomia Visual:** Shader de pós-processamento WebGL que converte imagens fotográficas comuns em composições estilizadas de pontilhismo ordenado (*Ordered Bayer Dithering*). Confere um acabamento retro-futurista, lembrando telas industriais monocromáticas dos anos 1980 ou consoles estéticos.
- **Gatilho de Interação:** Transição de hover (a imagem dithered se dissolve suavemente revelando a foto nítida colorida ou vice-versa).
- **Onde encaixar:** Cartões de membros de equipe, capas de artigos de blog técnico ou cartões de projetos em Bento Grids.

### 11. TextRepel (`Typography: Text Repel`)
- **Anatomia Visual:** Sistema tipográfico cinético no qual cada caractere de um parágrafo ou título é fragmentado em nós independentes. Conforme o cursor se aproxima, as letras sofrem uma força de repulsão eletrostática, afastando-se radialmente do ponteiro e retornando à sua posição tipográfica exata quando o cursor se distancia.
- **Gatilho de Interação:** Evento contínuo de coordenadas de mouse com interpolação vetorial de retorno.
- **Onde encaixar:** Frases de efeito em seções de manifesto institucional, títulos de projetos em agências ou chamadas experimentais.

### 12. WaterRipple (`Canvas: Water Ripple`)
- **Anatomia Visual:** Simulação de propagação de ondas líquidas na superfície de uma imagem estática ou textura de fundo. Cliques ou passagens do mouse geram perturbações circulares concêntricas que refratam a luz e deformam a textura subjacente realisticamente.
- **Gatilho de Interação:** Clique (*splash*) ou arraste suave com desaceleração exponencial do amortecimento da água.
- **Onde encaixar:** Banners de abertura de campanhas sazonais, fundos interativos de cabeçalho ou botões de experiência imersiva.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Fluxo da CLI

O Motion Core opera com a CLI `@motion-core/cli`, que realiza a leitura do registro oficial e baixa o código-fonte diretamente para o projeto:

```bash
# 1. Inicializar o projeto e configurar o arquivo motion-core.json
npx @motion-core/cli init

# 2. Adicionar componentes individuais ao repositório
npx @motion-core/cli add text-loop
npx @motion-core/cli add magnetic
npx @motion-core/cli add underlay-navigation
npx @motion-core/cli add liquid-metal
npx @motion-core/cli add globe
```

**Dependências essenciais do ecossistema:**
- `gsap` (motor de timelines, interpolações e custom easings)
- `ogl` (biblioteca WebGL ultra-enxuta para shaders de alta velocidade)
- `clsx` e `tailwind-merge` (para composição dinâmica de classes com a utilitária `cn()`)
- `tailwindcss` v4 com suporte à sintaxe de tokens `@theme` e variantes escuras

---

### Tokens Canônicos de Design & Cores em Tailwind CSS v4

As variáveis de estilo oficiais do Motion Core estruturam-se no padrão OKLCH:

```css
@import "tailwindcss";

/* motion-core:tokens:start */
@variant dark (&:where(.dark, .dark *));

:root {
	--base-hue: 265;
	--radius-base: 0.275rem;

	--background-inset: oklch(0.9764 0.0013 var(--base-hue));
	--background: oklch(1 0 0);
	--background-muted: oklch(0.956 0.002 var(--base-hue));
	--fixed-light: oklch(1 0 0);
	--fixed-dark: oklch(0.183 0.006 var(--base-hue));
	--foreground: oklch(0.1881 0.006 var(--base-hue));
	--foreground-muted: oklch(0.5493 0.0081 var(--base-hue));
	--accent: oklch(0.6996 0.201959 44.4414);
	--accent-secondary: oklch(0.5096 0.151959 44.4414);
	--border: oklch(0.4224 0.0013 var(--base-hue) / 0.1);

	--shadow-xs: 0px 1px 1px -0.5px rgba(0, 0, 0, 0.06);
	--shadow-sm: 0px 1px 1px -0.5px rgba(0, 0, 0, 0.06), 0px 3px 3px -1.5px rgba(0, 0, 0, 0.06);
	--shadow-md: 0px 1px 1px -0.5px rgba(0, 0, 0, 0.06), 0px 3px 3px -1.5px rgba(0, 0, 0, 0.06), 0px 6px 6px -3px rgba(0, 0, 0, 0.06);
	--shadow-lg: 0px 1px 1px -0.5px rgba(0, 0, 0, 0.06), 0px 3px 3px -1.5px rgba(0, 0, 0, 0.06), 0px 6px 6px -3px rgba(0, 0, 0, 0.06), 0px 12px 12px -6px rgba(0, 0, 0, 0.06);
}

.dark {
	--background-inset: oklch(0.2099 0.0039 var(--base-hue));
	--background: oklch(0.2574 0.0056 var(--base-hue));
	--background-muted: oklch(0.283 0.0091 var(--base-hue));
	--foreground: oklch(0.9674 0.0013 var(--base-hue));
	--foreground-muted: oklch(0.669 0.0107 var(--base-hue));
	--accent: oklch(0.6996 0.181959 44.4414);
	--accent-secondary: oklch(0.5096 0.131959 44.4414);
	--border: oklch(0.999 0.013 var(--base-hue) / 0.05);
}

@theme {
	--color-background-inset: var(--background-inset);
	--color-background: var(--background);
	--color-background-muted: var(--background-muted);
	--color-foreground: var(--foreground);
	--color-foreground-muted: var(--foreground-muted);
	--color-accent: var(--accent);
	--color-accent-secondary: var(--accent-secondary);
	--color-border: var(--border);

	--radius-xs: calc(var(--radius-base) * 1);
	--radius-sm: calc(var(--radius-base) * 2);
	--radius-md: calc(var(--radius-base) * 3);
	--radius-lg: calc(var(--radius-base) * 4);
}
/* motion-core:tokens:end */
```

---

### Física de Movimento, Variáveis & Easing Canônicos

```typescript
// helper: gsap.ts (Motion Core official easing)
import { gsap } from "gsap";
import { CustomEase } from "gsap/dist/CustomEase";

export const MOTION_CORE_EASE_NAME = "motion-core-ease";
export const MOTION_CORE_EASE_CURVE = "0.625, 0.05, 0, 1";

export function ensureMotionCoreEase() {
  if (!gsap.plugins?.CustomEase) {
    gsap.registerPlugin(CustomEase);
  }
  CustomEase.create(MOTION_CORE_EASE_NAME, MOTION_CORE_EASE_CURVE);
  return MOTION_CORE_EASE_NAME;
}
```

---

### Receita de Código Funcional 1: `TextLoop.svelte` (Svelte 5 Nativo com GSAP)

Abaixo está a implementação exata do componente emblemático de looping de palavras com morphing de largura e desfoque óptico:

```svelte
<script lang="ts">
	import { onMount } from "svelte";
	import { gsap } from "gsap";
	import { cn } from "$lib/utils/cn";

	interface Props {
		/**
		 * Array de strings que serão exibidas em rotação contínua.
		 */
		texts: string[];
		/**
		 * Intervalo em milissegundos entre as trocas de palavra.
		 * @default 2000
		 */
		interval?: number;
		/**
		 * Classes CSS adicionais para o contêiner raiz.
		 */
		class?: string;
	}

	let { texts, interval = 2000, class: className }: Props = $props();
	let currentIndex = $state(0);
	let isFirst = $state(true);

	function gsapTransition(
		node: HTMLElement,
		{ direction }: { direction: "in" | "out" },
	) {
		gsap.killTweensOf(node);
		const parent = node.parentElement;

		if (direction === "in") {
			if (isFirst) {
				gsap.set(node, { yPercent: 0, opacity: 1, filter: "blur(0px)" });
				return { duration: 0, tick: () => {} };
			}

			// Interpolação elástica da largura do contêiner pai
			if (parent) {
				gsap.fromTo(
					parent,
					{ width: parent.offsetWidth },
					{ width: node.offsetWidth, duration: 0.35, ease: "power2.inOut" },
				);
			}

			// Entrada da nova palavra com desfoque de 8px e overshoot back.out
			gsap.fromTo(
				node,
				{ yPercent: 50, opacity: 0, filter: "blur(8px)" },
				{
					yPercent: 0,
					opacity: 1,
					filter: "blur(0px)",
					duration: 0.3,
					delay: 0.25,
					ease: "back.out(1.2)",
				},
			);
			return { duration: 900, tick: () => {} };
		}

		// Saída da palavra anterior com fixação de largura e desfoque vertical
		if (parent) parent.style.width = `${parent.offsetWidth}px`;
		Object.assign(node.style, {
			position: "absolute",
			top: "0",
			left: "0",
			width: "100%",
		});
		gsap.to(node, {
			yPercent: -50,
			opacity: 0,
			filter: "blur(6px)",
			duration: 0.2,
			ease: "power2.in",
		});
		return { duration: 300, tick: () => {} };
	}

	onMount(() => {
		const loopInterval = setInterval(() => {
			if (document.hidden) return;
			isFirst = false;
			currentIndex = (currentIndex + 1) % texts.length;
		}, interval);

		return () => clearInterval(loopInterval);
	});
</script>

<span
	class={cn("font-inherit relative inline-block text-inherit", className)}
	style="clip-path: inset(-100vh 0 -100vh 0);"
>
	<span
		class="font-inherit invisible inline-block w-0 text-inherit"
		aria-hidden="true">&nbsp;</span
	>{#key currentIndex}<span
			class={cn(
				"font-inherit whitespace-nowrap text-inherit",
				isFirst ? "relative inline-block" : "absolute top-0 left-0",
			)}
			in:gsapTransition={{ direction: "in" }}
			out:gsapTransition={{ direction: "out" }}
		>
			{texts[currentIndex]}
		</span>{/key}
</span>
```

---

### Receita de Código Funcional 2: Equivalente Portável React + Framer Motion (`TextLoop.tsx`)

Para equipes trabalhando em ecossistemas React / Next.js que desejam reproduzir a mesma física óptica e calibração de easing do Motion Core:

```tsx
"use client";

import * as React from "react";
import { motion, AnimatePresence } from "framer-motion";
import { cn } from "@/lib/utils";

interface TextLoopProps {
  texts: string[];
  interval?: number;
  className?: string;
}

export function TextLoop({ texts, interval = 2000, className }: TextLoopProps) {
  const [index, setIndex] = React.useState(0);

  React.useEffect(() => {
    const timer = setInterval(() => {
      if (document.hidden) return;
      setIndex((prev) => (prev + 1) % texts.length);
    }, interval);
    return () => clearInterval(timer);
  }, [texts.length, interval]);

  return (
    <span
      className={cn("relative inline-flex items-center overflow-hidden align-baseline", className)}
      style={{ clipPath: "inset(-100vh 0 -100vh 0)" }}
    >
      {/* Contêiner de medição para dimensionamento elástico automático */}
      <motion.span
        layout
        transition={{ duration: 0.35, ease: [0.625, 0.05, 0, 1] }}
        className="relative inline-flex whitespace-nowrap"
      >
        <AnimatePresence mode="popLayout" initial={false}>
          <motion.span
            key={texts[index]}
            initial={{ y: "60%", opacity: 0, filter: "blur(8px)" }}
            animate={{
              y: "0%",
              opacity: 1,
              filter: "blur(0px)",
              transition: {
                y: { type: "spring", stiffness: 350, damping: 26 },
                opacity: { duration: 0.28 },
                filter: { duration: 0.28 },
              },
            }}
            exit={{
              y: "-60%",
              opacity: 0,
              filter: "blur(6px)",
              transition: { duration: 0.2, ease: [0.625, 0.05, 0, 1] },
            }}
            className="inline-block text-accent font-medium"
          >
            {texts[index]}
          </motion.span>
        </AnimatePresence>
      </motion.span>
    </span>
  );
}
```

---

### Receita de Código Funcional 3: Componente `Magnetic.tsx` com Física de Mola GSAP

```tsx
"use client";

import * as React from "react";
import { gsap } from "gsap";
import { cn } from "@/lib/utils";

interface MagneticProps extends React.HTMLAttributes<HTMLDivElement> {
  children: React.ReactNode;
  duration?: number;
  strength?: number;
}

export function Magnetic({
  children,
  duration = 1,
  strength = 1,
  className,
  ...props
}: MagneticProps) {
  const ref = React.useRef<HTMLDivElement>(null);

  React.useEffect(() => {
    const node = ref.current;
    if (!node) return;

    // quickTo permite atualizações de 120 FPS sem overhead de criação de novas instâncias
    const xTo = gsap.quickTo(node, "x", { duration, ease: "elastic.out(1, 0.3)" });
    const yTo = gsap.quickTo(node, "y", { duration, ease: "elastic.out(1, 0.3)" });

    const handleMouseMove = (e: MouseEvent) => {
      const { clientX, clientY } = e;
      const { height, width, left, top } = node.getBoundingClientRect();
      const x = (clientX - (left + width / 2)) * strength;
      const y = (clientY - (top + height / 2)) * strength;
      xTo(x);
      yTo(y);
    };

    const handleMouseLeave = () => {
      xTo(0);
      yTo(0);
    };

    node.addEventListener("mousemove", handleMouseMove);
    node.addEventListener("mouseleave", handleMouseLeave);

    return () => {
      node.removeEventListener("mousemove", handleMouseMove);
      node.removeEventListener("mouseleave", handleMouseLeave);
      gsap.killTweensOf(node);
    };
  }, [duration, strength]);

  return (
    <div ref={ref} className={cn("inline-block will-change-transform", className)} {...props}>
      {children}
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao arquitetar um novo projeto fundamentado nas diretrizes técnicas do **Motion Core**, a IA e o time de engenharia devem formalizar as seguintes decisões estruturais no documento de blueprint:

1. **Declaração de Infraestrutura de Motion & Gráficos:**
   - Declarar explicitamente os runtimes: Svelte 5 / Next.js 15, GSAP 3 (com `CustomEase`), OGL e Tailwind CSS v4.
   - Registrar formalmente a curva de transição primária: `cubic-bezier(0.625, 0.05, 0, 1)` sob o nome canônico `motion-core-ease`.

2. **Governança de Canvas e Limites de GPU:**
   - **Regra de 1 Canvas Ativo:** Proibir terminantemente mais de 1 elemento WebGL ativo na mesma viewport para evitar estouro de limite de contextos do navegador.
   - **IntersectionObserver Lifecycle:** Qualquer componente Canvas (`LiquidMetal`, `Globe`, `FluidSimulation`) deve pausar seu loop de animação (`cancelAnimationFrame`) imediatamente ao sair da viewport via `IntersectionObserver` com limiar `threshold: 0.05`.
   - **Tratamento de Context Lost:** Incluir obrigatoriamente listeners para `webglcontextlost` com `event.preventDefault()` e re-inicialização limpa em `webglcontextrestored`.

3. **Arquitetura Cromática OKLCH Violet-Zinc:**
   - Adotar a variável base `--base-hue: 265` para todas as superfícies neutras de dark mode, rejeitando o uso de preto puro `#000000` em cartões ou fundos.
   - Limitar o acento elétrico `oklch(0.6996 0.201959 44.4414)` (âmbar vibrante) estritamente à cota de 10% da regra 60-30-10 (palavras ativas do `TextLoop`, estados ativos de link no `UnderlayNavigation` e bordas focadas).

4. **Diretrizes de Acessibilidade & Motion Sensitivity:**
   - Respeito mandatório a `@media (prefers-reduced-motion: reduce)`:
     - `TextLoop`: Congelar a exibição na primeira palavra do array sem disparar timers nem transições verticais com blur.
     - `Magnetic`: Desativar o listener de mouse move e manter os elementos em coordenadas estáticas $(x=0, y=0)$.
     - `UnderlayNavigation`: Substituir a animação complexa de encolhimento e slide por um corte de opacidade instantâneo de 150ms.
   - Fornecer sempre textos acessíveis não-fragmentados para leitores de tela em componentes cinéticos com `aria-label` descritivo no contêiner pai e `aria-hidden="true"` nos caracteres ou palavras em animação contínua.
