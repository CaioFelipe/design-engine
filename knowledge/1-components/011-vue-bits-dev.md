---
id: "vue-bits-dev"
name: "Vue Bits"
url: "https://vue-bits.dev/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Creative Motion & WebGL Shaders", "Physics-Driven Micro-interactions", "Kinetic Typography & Dynamic Text", "Modern Vue 3 Composition Architecture"]
densidade_informacao: "Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Motion-V/JS) a Alto (WebGL Shaders/OGL/Three.js)"
stack_frameworks: ["Vue 3 (Composition API / `<script setup>`)", "Nuxt 3 / Nuxt 4", "Tailwind CSS (v3 & v4)", "Motion-V (Framer Motion for Vue)", "OGL (Minimal WebGL)", "Three.js / TresJS", "Matter-js (2D Physics)", "GSAP"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "Plus Jakarta Sans", "JetBrains Mono", "Space Grotesk", "Syne"]
  paletas_ideais: ["Deep Dark Mode (Zinc 950 / Slate 950)", "High-Contrast Emerald/Cyan Accents (estilo Aurora)", "Cyberpunk Neon Glow", "Clean Modern Monochrome"]
  combinacoes_recomendadas: ["Shadcn Vue", "Radix Vue", "PrimeVue", "Nuxt UI", "Tailwind CSS v4", "Lucide Vue Next", "VueUse"]
  conflitos_esteticos: ["Material Design 2 com elevações duras e sombras estáticas", "Layouts corporativos densos legados em Vue 2 sem animação", "Frameworks CSS legados com resets agressivos que quebram transform-style: preserve-3d"]
---

# Vue Bits — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo engenheiro frontend **David Haz** (`@DavidHDev`), o **Vue Bits** (`vue-bits.dev`) é o port oficial e o ecossistema definitivo dos componentes do aclamado *React Bits* para o ecossistema **Vue 3** e **Nuxt**. Historicamente, o desenvolvimento de interfaces interativas experimentais, tipografia cinética e fundos procedurais com shaders esteve desproporcionalmente concentrado no ecossistema React (impulsionado pela onipresença do Framer Motion). O Vue Bits rompe definitivamente essa assimetria técnica, entregando uma biblioteca com mais de 200 componentes, micro-interações táteis e planos de fundo tridimensionais concebidos sob a arquitetura idiomática do Vue 3.

A assinatura visual e técnica do Vue Bits se ancora em quatro pilares fundamentais:

1. **Simbiose entre Shaders WebGL Leves (`OGL`) e Física Vetorial (`Motion-V`)**:
   Diferente de bibliotecas que carregam monólitos de 600 KB do Three.js para renderizar um simples ruído procedural, o Vue Bits recorre à biblioteca minimalista **OGL** (ou a shaders diretos em WebGL2) para a sua coleção de fundos (como *Aurora*, *Balatro*, *LiquidChrome* e *Dither*). Quando elementos tridimensionais completos são necessários, a suíte orquestra **Three.js** ou **TresJS** de forma modular. Para a física cinética na camada DOM, utiliza **Motion-V** (a transposição oficial do core do Framer Motion para Vue 3), viabilizando molas físicas com amortecimento natural (`damping`, `stiffness`, `mass`) sem saltos mecânicos.

2. **Tipografia Cinética de Alta Densidade (Kinetic Typography)**:
   A suíte de animação textual do Vue Bits é uma das mais ricas da web moderna. Componentes como *DecryptedText*, *TrueFocus*, *BlurText*, *VariableProximity* e *SplitFlapText* tratam texto não como blocos passivos de glifos, mas como entidades dinâmicas responsivas à proximidade do cursor, eventos de viewport e cronômetros de revelação com caracteres aleatórios matriciais.

3. **Arquitetura Aberta Copy-Paste & CLI Desacoplada (`jsrepo`)**:
   Seguindo o paradigma estabelecido pelo `shadcn/ui`, o Vue Bits não impõe dependências de pacotes fechados via NPM (`npm install @vue-bits/core`). Os desenvolvedores instalam o código-fonte puro diretamente em suas árvores de componentes por meio da CLI **jsrepo** (`npx jsrepo add https://vue-bits.dev/r/<Component>`) ou via cópia manual. Cada componente é autocontido em um arquivo `.vue` único, configurado com `<script setup lang="ts">`, facilitando a auditoria de código, a personalização de estilos no Tailwind CSS v3/v4 e o ajuste fino de propriedades.

4. **Acessibilidade Nativa em Efeitos Visuais Disruptivos**:
   Ao contrário de soluções experimentais que degradam a leitura de tecnologia assistiva, o Vue Bits estrutura componentes complexos (como textos cifrados e embaralhados) com espelhamento duplo no DOM: o texto legível original é preservado em elementos com classe `sr-only` para leitores de tela, enquanto os nós com mutação visual contínua são devidamente encapsulados sob `aria-hidden="true"`.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **Startups de Inteligência Artificial, Agentes Autônomos & Workspaces LLM**:
   Aplicações em Nuxt que necessitam transmitir a sensação de computação generativa em tempo real. Efeitos como *DecryptedText* (para status de raciocínio de agentes), *Aurora* (gradientes bioluminescentes para hero sections) e *SpotlightCard* (foco radial em planos de assinatura e recursos) criam o ambiente estético perfeito para produtos de IA contemporâneos.
2. **DevTools, Plataformas Web3, Infraestrutura & Segurança da Informação**:
   Ferramentas voltadas para desenvolvedores e engenheiros de segurança encontram no catálogo de textos técnicos (*TechText*, *ScrambleText*, *ASCIIText*, *FaultyTerminal*, *CRTWarp*) o vocabulário visual ideal para dashboards com estética hacker, monitores de latência e nós de telemetria.
3. **Landing Pages de Alto Impacto & Portfólios de Creative Technologists**:
   Estúdios digitais e desenvolvedores Vue/Nuxt que buscam superar o teto de vidro do "design corporativo genérico", aplicando interações táteis como *TiltedCard* (com profundidade 3D no cursor), *Antigravity* (elementos físicos que caem e colidem via Matter-js) e *SplashCursor*.
4. **Produtos SaaS B2B Modernos com Dashboards Interativos**:
   Uso cirúrgico de cartões iluminados (*BorderGlow*, *SpotlightCard*), barras de comando fluidas e sliders táteis com amortecimento elástico (*ElasticSlider*) para enriquecer formulários e painéis de parametrização.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Neutra e Estrutural)**:
  Estrutura base construída com primitivas acessíveis e limpas (ex: **Shadcn Vue**, **Radix Vue** ou **Nuxt UI**), tipografia neutra (como `Geist Sans` ou `Inter`), espaçamentos modulares do Tailwind e paletas de cinza escuro/zinco (`zinc-900`/`zinc-950`).
- **30% (Camada Tátil e Micro-interações do Vue Bits)**:
  Cartões interativos com iluminação ao hover (*SpotlightCard*), cartões tridimensionais em bento grids (*TiltedCard*), botões magnéticos (*Magnet*) e transições de entrada de texto com desfoque progressivo (*BlurText*) em subtítulos de seções.
- **10% (Showstoppers Protagonistas)**:
  Exatamente **um** fundo shader ativo na viewport (ex: *Aurora*, *LiquidChrome* ou *Balatro* na Hero Section) associado a um título com revelação cinética (*TrueFocus* ou *DecryptedText* no `<h1>`). O restante da página descansa em superfícies estáticas ou com iluminação sutil para evitar poluição visual e saturação cognitiva.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Telas Operacionais de ERPs Legados e Sistemas Bancários de Auditoria**:
  Telas analíticas densas contendo dezenas de tabelas financeiras, auditorias fiscais e campos de inserção contínua não se beneficiam de animações de texto, fundos dinâmicos ou física de mola; qualquer atraso visual induz fadiga no operador.
- **Aplicações Vue 2 Legadas (Options API)**:
  O Vue Bits é construído exclusivamente em torno da **Composition API** do Vue 3, utilizando funcionalidades avançadas como `useTemplateRef()` (introduzido no Vue 3.5), `withDefaults()`, `defineProps()` com tipagem TypeScript e a biblioteca `motion-v`. Tentar retrocompatibilizar esses componentes com Vue 2 é inviável tecnicamente.
- **Páginas Mobile de Alto Alcance em Ambientes de Rede Restrita (2G/3G) ou Dispositivos Low-End**:
  Renderizadores WebGL contínuos (como raymarching shaders e partículas) executam loops de `requestAnimationFrame` que consomem ciclos de GPU e drenam bateria rapidamente em smartphones de entrada. Em dispositivos móveis, fundos em WebGL devem ser desativados ou substituídos por gradientes CSS estáticos.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **Múltiplos Shaders WebGL Concorrentes na Mesma Tela**:
  Instanciar simultaneamente um fundo *Aurora* no Hero, um fundo *Hyperspeed* no meio da página e um fundo *LiquidChrome* no rodapé. Cada instância aloca um contexto WebGL independente; abrir 3 ou 4 contextos WebGL simultâneos frequentemente causa perda de contexto pelo navegador (`webglcontextlost`) e queda drástica de FPS.
- **Tipografia Cifrada em Parágrafos Longos de Texto**:
  Aplicar *DecryptedText* ou *GlitchText* em parágrafos de documentação ou termos de uso. O efeito é espetacular para palavras-chave isoladas (palavras no título, crachás de versão ou alertas de segurança), mas torna a leitura funcional intolerável quando aplicada em blocos de texto contínuos.
- **Omissão do Cleanup de Contexto em SPAs**:
  Esquecer de liberar buffers e perder explicitamente o contexto ao desmontar o componente (`renderer.gl.getExtension('WEBGL_lose_context')?.loseContext()`). Em SPAs e rotas do Nuxt, a navegação contínua entre páginas sem desalocação de WebGL gera vazamento crônico de memória (memory leaks).

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

O repositório do Vue Bits divide seu ecossistema em cinco categorias expressivas: `TextAnimations` (33 componentes), `Backgrounds` (58 componentes), `Components` (44 componentes), `Animations` (40 componentes) e `Micro` (34 componentes). Abaixo estão os 12 componentes mais emblemáticos da biblioteca:

### 1. DecryptedText (`TextAnimations/DecryptedText`)
- **Anatomia Visual**: Exibe um texto que começa como uma sequência de glifos criptografados/embaralhados (`!@#$%^&*()_+`) e é decodificado progressivamente caractere por caractere até revelar a frase final. Suporta direção sequencial (`start`, `end`, `center`) ou revelação simultânea por iterações máximas.
- **Gatilho de Interação**: Disparado ao entrar na viewport (`animateOn="view"`), ao passar o mouse (`hover` com reversão), no clique, ou combinado (`inViewHover`).
- **Onde encaixar**: Títulos de badges de segurança, números de versão de lançamentos de tecnologia, slogans em heros de cibersegurança/DevTools e botões de comando terminal.

### 2. BlurText (`TextAnimations/BlurText`)
- **Anatomia Visual**: Os caracteres ou palavras emergem a partir de uma posição deslocada no eixo vertical (`y: -50px` ou `y: 50px`), com opacidade nula e forte desfoque gaussiano (`filter: blur(10px)`). Os elementos transicionam de forma escalonada (*stagger*) para `blur(0px)` e opacidade total usando curvas de transição suaves calculadas pelo `motion-v`.
- **Gatilho de Interação**: Disparo automático na entrada do elemento no viewport via `IntersectionObserver`.
- **Onde encaixar**: H1 principal em Hero sections, subtítulos explicativos de landing pages de SaaS de IA e títulos de seções institucionais de alto padrão.

### 3. TrueFocus (`TextAnimations/TrueFocus`)
- **Anatomia Visual**: Um bloco de texto corrido onde todas as palavras permanecem sob leve desfoque (`blur(4px)`) e opacidade reduzida, exceto a palavra atualmente em foco. Uma moldura retangular com bordas demarcadas desliza suavemente sobre a palavra ativa através de interpolação física, mudando ciclicamente ou seguindo o cursor do mouse.
- **Gatilho de Interação**: Auto-play cronometrado com alternância de palavras ou tracking interativo por hover.
- **Onde encaixar**: Chamada principal da Hero Section de startups inovadoras, destacando qualidades do produto (ex: "A infraestrutura mais *rápida*, *segura* e *resiliente* para IA").

### 4. VariableProximity (`TextAnimations/VariableProximity`)
- **Anatomia Visual**: Utiliza fontes variáveis (Variable Fonts como *Roboto Flex*, *Inter Variable* ou fontes com eixos `wght`, `wdth` e `opsz`). Conforme o cursor do usuário se desloca pela viewport, os glifos mais próximos ao mouse aumentam instantaneamente de peso tipográfico (font-weight: 100 → 900) e largura, criando uma onda tátil de resposta magnética tipográfica.
- **Gatilho de Interação**: Rastreador de mouse contínuo com raio de proximidade calibrável (`radius: 100px`).
- **Onde encaixar**: Grandes títulos em portfólios de design engineering, banners de apresentação de produto e seções editoriais de revistas digitais.

### 5. Aurora (`Backgrounds/Aurora`)
- **Anatomia Visual**: Shader procedural em WebGL2/OGL que projeta fitas orgânicas de luz boreal em movimento contínuo, utilizando ruído simplex 2D (`snoise`), elevações exponenciais e rampa de cores configurável (`colorStops`) que se mescla de forma fluida com a cor do background do site.
- **Gatilho de Interação**: Loop contínuo renderizado via `requestAnimationFrame` com velocidade e amplitude ajustáveis via props.
- **Onde encaixar**: Fundo global de Hero sections no Dark Mode, cabeçalhos de produtos de IA generativa e backdrops de telas de autenticação e onboarding.

### 6. LiquidChrome (`Backgrounds/LiquidChrome`)
- **Anatomia Visual**: Simulação hiper-realista de metal líquido (mercúrio/cromo fluido) renderizada em fragment shader com mapas de normais, distorções de reflexão especular e refrações dinâmicas que reagem sutilmente ao posicionamento do mouse.
- **Gatilho de Interação**: Auto-play com distorção cinética atrelada à posição normalizada do cursor do usuário.
- **Onde encaixar**: Apresentações de hardware de luxo, landing pages de fintechs de alta sofisticação, capas de lançamentos de software de engenharia criativa.

### 7. Balatro (`Backgrounds/Balatro`)
- **Anatomia Visual**: Fundo procedural psicodélico e nostálgico inspirado na estética visual e nas ondas de cor distorcidas do célebre jogo indie *Balatro*. Desenha espirais orgânicas giratórias com aberração cromática, ruído analógico e deformações esféricas no fragment shader.
- **Gatilho de Interação**: Renderização contínua com controle de contraste, saturação e velocidade angular.
- **Onde encaixar**: Projetos voltados para cultura gamer, plataformas de apostas/fintechs alternativas, portfólios visuais e páginas de erro 404 criativas.

### 8. SpotlightCard (`Components/SpotlightCard`)
- **Anatomia Visual**: Cartão com cantos arredondados (`rounded-3xl`), borda sutil e fundo escuro. Conforme o cursor se move sobre o cartão, uma fonte de luz radial translúcida suave (`radial-gradient`) acompanha as coordenadas exatas do mouse, revelando sutilmente as texturas e o conteúdo interno sem afetar os eventos de clique.
- **Gatilho de Interação**: Eventos de `mousemove`, `mouseenter` e `mouseleave`, além de foco via teclado (`focus`/`blur`) para total acessibilidade.
- **Onde encaixar**: Grades de funcionalidades (Bento Grids), cartões de planos de preços (Pricing Tables) e cartões de depoimentos.

### 9. TiltedCard (`Components/TiltedCard`)
- **Anatomia Visual**: Container com perspectiva CSS ativa (`[perspective:800px]`) e preservação tridimensional (`[transform-style:preserve-3d]`). A imagem principal inclina-se nos eixos X e Y de acordo com a posição do mouse, enquanto elementos sobrepostos (como badges ou textos em slot) são projetados para fora do plano com `transform: translateZ(30px)`, criando efeito de paralaxe 3D real com tooltip flutuante.
- **Gatilho de Interação**: Mousemove com amortecimento físico suave (`Motion-V` spring: `damping: 30`, `stiffness: 100`, `mass: 2`).
- **Onde encaixar**: Vitrines de produtos de e-commerce de ponta, capas de artigos em blogs técnicos e cartões de destaques de projetos.

### 10. ElasticSlider (`Components/ElasticSlider`)
- **Anatomia Visual**: Controle deslizante numérico cujo trilho e botão sofrem deformações elásticas não-lineares durante o arrasto. Ao atingir os limites mínimo e máximo ou ao ser solto com velocidade, o botão ultrapassa o limite (*overshoot*) e vibra até descansar, simulando a tensão física de um elástico.
- **Gatilho de Interação**: Arrasto tátil (*drag*) com física de mola instantânea.
- **Onde encaixar**: Ajuste de volume/brilho em players multimídia, simuladores de investimento em fintechs e sliders de parâmetros em ferramentas de geração de imagem/IA.

### 11. Antigravity (`Animations/Antigravity`)
- **Anatomia Visual**: Um container delimitado por canvas ou nós DOM onde tags, crachás de habilidades (*skill badges*) ou ícones caem sob efeito da gravidade terrestre, colidindo elasticamente entre si e com as paredes do container através do motor de física 2D **Matter-js**. O usuário pode agarrar, jogar e reorganizar os elementos livremente.
- **Gatilho de Interação**: Gravidade automática, colisão em tempo real e arrasto com vetor de inércia do mouse/toque.
- **Onde encaixar**: Seções de tecnologias e linguagens em portfólios, rodapés interativos de agências criativas e seções de "Parceiros / Integrações".

### 12. SquishSwitch & SloshGauge (`Micro`)
- **Anatomia Visual**: 
  - *SquishSwitch*: Interruptor de alternância (toggle) que achata plasticamente sua forma geométrica quando o usuário clica e mantém pressionado, expandindo-se vigorosamente ao ser liberado para o outro estado.
  - *SloshGauge*: Medidor de progresso/capacidade cilíndrico onde o líquido interno oscila e produz ondas dinâmicas (*sloshing*) calculadas por física de fluidos quando o valor numérico é alterado.
- **Gatilho de Interação**: Clique, arrasto e atualizações reativas de estado numérico.
- **Onde encaixar**: Modais de confirmação, seletores de modo escuro/claro e indicadores de uso de cota em planos SaaS de IA.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Ambiente

O Vue Bits foi concebido para o ecossistema moderno do **Vue 3.5+** e **Nuxt 3/4** com suporte nativo ao **Tailwind CSS v3 e v4**.

Para instalar as dependências de runtime mais comuns utilizadas pelos componentes da biblioteca:

```bash
# Dependências fundamentais para Motion e Shaders WebGL
npm install motion-v ogl @vueuse/core lucide-vue-next

# Dependências adicionais para componentes tridimensionais e de física (quando utilizados)
npm install three @types/three matter-js @types/matter-js gsap
```

### Instalação via CLI `jsrepo`

O Vue Bits utiliza o **jsrepo** como seu registro oficial de distribuição no padrão copy-paste:

```bash
# 1. Inicializar o registro do Vue Bits no projeto Vue/Nuxt
npx jsrepo init https://vue-bits.dev/r

# 2. Adicionar componentes específicos diretamente ao seu diretório de componentes
npx jsrepo@latest add https://vue-bits.dev/r/SpotlightCard
npx jsrepo@latest add https://vue-bits.dev/r/DecryptedText
npx jsrepo@latest add https://vue-bits.dev/r/Aurora
npx jsrepo@latest add https://vue-bits.dev/r/BlurText
```

### Nuxt 3 & Nuxt 4: Diretrizes de SSR e Hidratação

Componentes que interagem com a GPU (OGL, Three.js) ou que dependem de dimensões de janela (`window.innerWidth`, `requestAnimationFrame`) precisam ser tratados com precauções de Server-Side Rendering:

1. **Uso de `<ClientOnly>`**:
   Envolva fundos como `Aurora`, `Balatro` e `LiquidChrome` na tag `<ClientOnly>` do Nuxt, fornecendo um gradiente neutro de fallback para evitar flashes de hidratação:
   ```html
   <ClientOnly>
     <Aurora :colorStops="['#09090b', '#10b981', '#09090b']" :amplitude="1.2" />
     <template #fallback>
       <div class="w-full h-full bg-zinc-950" />
     </template>
   </ClientOnly>
   ```
2. **Ciclo de Vida do WebGL (`WEBGL_lose_context`)**:
   Sempre que instanciar um `Renderer` da biblioteca OGL, armazene a referência e invoque a extensão de perda de contexto no hook `onUnmounted` do Vue, liberando texturas e buffers de memória gráfica:
   ```ts
   onUnmounted(() => {
     cancelAnimationFrame(animateId);
     renderer?.gl.getExtension('WEBGL_lose_context')?.loseContext();
   });
   ```

---

### Física de Movimento, Parâmetros e Transições

O Vue Bits padroniza os seguintes parâmetros de mola física (`spring`) através do motor **Motion-V**:

| Cenário de Interação | `stiffness` | `damping` | `mass` | Comportamento Sensorial |
| :--- | :---: | :---: | :---: | :--- |
| **Hover 3D em Cartões (TiltedCard)** | `100` | `30` | `2.0` | Inércia pesada, resistência física elegante, sem oscilações nervosas |
| **Tooltip Flutuante Seguidor** | `150` | `25` | `0.8` | Rastreamento responsivo e ágil, com amortecimento tátil imperceptível |
| **Entrada Escalonada de Texto (BlurText)** | `120` | `18` | `1.0` | Desaceleração orgânica conforme as palavras alcançam nitidez |
| **Sliders Elásticos (ElasticSlider)** | `400` | `28` | `1.2` | Tensão alta de mola com rebote acentuado (*overshoot*) |

---

### Receita de Código Funcional e Completa: `SpotlightCard.vue`

Abaixo está a implementação de referência do **SpotlightCard**, desenvolvida em Vue 3.5 com Composition API idiomática, tipagem TypeScript estrita e compatibilidade total com Tailwind CSS v3 e v4:

```vue
<!-- components/ui/SpotlightCard.vue -->
<template>
  <div
    ref="cardRef"
    @mousemove="handleMouseMove"
    @focus="handleFocus"
    @blur="handleBlur"
    @mouseenter="handleMouseEnter"
    @mouseleave="handleMouseLeave"
    tabindex="0"
    :class="[
      'group relative overflow-hidden rounded-3xl border border-zinc-800 bg-zinc-950/80 p-8 backdrop-blur-md transition-all duration-300 focus:outline-none focus:ring-2 focus:ring-emerald-500/50',
      className
    ]"
  >
    <!-- Camada de Iluminação Radial Dinâmica -->
    <div
      class="pointer-events-none absolute inset-0 transition-opacity duration-500 ease-out will-change-transform"
      :style="{
        opacity: currentOpacity,
        background: `radial-gradient(circle 350px at ${cursorPosition.x}px ${cursorPosition.y}px, ${spotlightColor}, transparent 80%)`
      }"
      aria-hidden="true"
    />

    <!-- Borda reflexiva reativa (Efeito Glow de borda) -->
    <div
      class="pointer-events-none absolute inset-0 rounded-3xl border border-transparent transition-opacity duration-300"
      :style="{
        opacity: isHovered ? 1 : 0,
        background: `radial-gradient(circle 280px at ${cursorPosition.x}px ${cursorPosition.y}px, rgba(255, 255, 255, 0.15), transparent 70%) border-box`,
        WebkitMask: 'linear-gradient(#fff 0 0) padding-box, linear-gradient(#fff 0 0)',
        WebkitMaskComposite: 'destination-out',
        maskComposite: 'exclude'
      }"
      aria-hidden="true"
    />

    <!-- Conteúdo do Cartão -->
    <div class="relative z-10">
      <slot />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, useTemplateRef } from 'vue';

interface Position {
  x: number;
  y: number;
}

interface SpotlightCardProps {
  className?: string;
  spotlightColor?: string;
  maxOpacity?: number;
}

const props = withDefaults(defineProps<SpotlightCardProps>(), {
  className: '',
  spotlightColor: 'rgba(16, 185, 129, 0.18)', // Esmeralda suave ideal para dark mode
  maxOpacity: 0.8
});

// Vue 3.5 useTemplateRef com tipagem
const cardRef = useTemplateRef<HTMLDivElement>('cardRef');

const cursorPosition = ref<Position>({ x: 0, y: 0 });
const currentOpacity = ref<number>(0);
const isFocused = ref<boolean>(false);
const isHovered = ref<boolean>(false);

const handleMouseMove = (event: MouseEvent) => {
  if (!cardRef.value) return;

  const rect = cardRef.value.getBoundingClientRect();
  cursorPosition.value = {
    x: event.clientX - rect.left,
    y: event.clientY - rect.top
  };
};

const handleMouseEnter = () => {
  isHovered.value = true;
  currentOpacity.value = props.maxOpacity;
};

const handleMouseLeave = () => {
  isHovered.value = false;
  if (!isFocused.value) {
    currentOpacity.value = 0;
  }
};

const handleFocus = () => {
  isFocused.value = true;
  currentOpacity.value = props.maxOpacity;
  if (cardRef.value) {
    // Posiciona o ponto de luz no centro do elemento ao focar via teclado
    const rect = cardRef.value.getBoundingClientRect();
    cursorPosition.value = {
      x: rect.width / 2,
      y: rect.height / 2
    };
  }
};

const handleBlur = () => {
  isFocused.value = false;
  if (!isHovered.value) {
    currentOpacity.value = 0;
  }
};
</script>
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar o **Vue Bits** como a biblioteca de animação e componentes criativos para a arquitetura de um novo projeto, declare as seguintes diretivas obrigatórias no documento de blueprint:

### 1. Declaração de Stack & Estrutura de Pastas
- No bloco de dependências, registre:
  - Framework: `Vue 3.5+` ou `Nuxt 3.10+ / Nuxt 4`
  - Core de Física e Animação: `motion-v`
  - Renderizador WebGL: `ogl` (Shader minimalista) e opcionalmente `@tresjs/core`
  - Utilitários: `@vueuse/core`, `clsx`, `tailwind-merge`
- Organize os componentes clonados em subdiretórios coerentes sob `components/ui/vue-bits/`:
  - `components/ui/vue-bits/text/` (ex: `DecryptedText.vue`, `BlurText.vue`, `TrueFocus.vue`)
  - `components/ui/vue-bits/backgrounds/` (ex: `Aurora.vue`, `Balatro.vue`, `LiquidChrome.vue`)
  - `components/ui/vue-bits/cards/` (ex: `SpotlightCard.vue`, `TiltedCard.vue`)
  - `components/ui/vue-bits/animations/` (ex: `Magnet.vue`, `Antigravity.vue`)

### 2. Guardrails de Performance e WebGL Budget
- **Budget de Shaders Ativos**: É estritamente proibido manter mais de **1 (um)** canvas com fragment shader contínuo executando simultaneamente por página. Ao fazer scroll para fora do Hero, pause o renderizador via `IntersectionObserver` ou cancele o `requestAnimationFrame`.
- **Desativação em Telas Mobile**: Configure a prop `showMobileWarning` ou utilize composables do VueUse (`useMediaQuery('(max-width: 768px)')`) para ocultar ou simplificar efeitos pesados de WebGL e 3D em dispositivos portáteis.
- **Acessibilidade e Preferência de Movimento Reduzido**: Todos os componentes animados devem respeitar a preferência do sistema operacional (`prefers-reduced-motion: reduce`). Ao detectar a flag, desative as interpolações de mola e transições de desfoque, exibindo o conteúdo estático imediatamente.

### 3. Checklist de Integração para a IA / Engenheiro
- [ ] O componente clonado usa `useTemplateRef` (Vue 3.5) ou fallback seguro `ref<HTMLElement>()`?
- [ ] Em projetos Nuxt com SSR, os elementos com WebGL estão devidamente envolvidos em `<ClientOnly>`?
- [ ] O cleanup de `requestAnimationFrame` e a liberação de contexto WebGL (`WEBGL_lose_context`) estão configurados no hook `onUnmounted`?
- [ ] Os elementos de texto cinético possuem rótulos acessíveis com classe `sr-only` e `aria-hidden="true"` nas camadas animadas?
- [ ] A iluminação e os contrastes de cor respeitam os níveis mínimos do WCAG AA (proporção 4.5:1) quando o efeito de hover não estiver ativado?
