---
id: "inspira-ui"
name: "Inspira UI"
url: "https://www.inspira-ui.com/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Aceternity & Magic UI Aesthetics for Vue", "Dark Mode Micro-Luminescence", "GPU-Accelerated Kinetic Motion", "Tailwind CSS v4 & Vue 3 Composition Architecture"]
densidade_informacao: "Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (CSS Keyframes / Motion-V) a Alto (Cobe / Canvas 2D / Three.js Shaders)"
stack_frameworks: ["Vue 3 (Composition API / `<script setup>`)", "Nuxt 3 / Nuxt 4", "Tailwind CSS v4 (@import 'tailwindcss' / @theme)", "Motion-V (Framer Motion for Vue)", "VueUse (@vueuse/core)", "vue-use-spring", "Cobe", "Three.js / TresJS", "clsx / tailwind-merge"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "Plus Jakarta Sans", "Space Grotesk", "JetBrains Mono"]
  paletas_ideais: ["Deep Dark Mode (Zinc 950 / Slate 950 / Oklch Dark)", "Cyan & Violet Bioluminescence (#18CCFC, #6344F5, #AE48FF)", "Monochrome High Contrast with Subtle Glow"]
  combinacoes_recomendadas: ["shadcn-vue", "Radix Vue", "Nuxt UI v3/v4", "Lucide Vue Next", "@nuxt/image", "@vueuse/core", "Vue Bits"]
  conflitos_esteticos: ["Frameworks CSS utilitários com resets destrutivos", "Aplicações legadas Vue 2 (Options API)", "Design flat sem profundidade de luz e sem suporte a transform 3D"]
---

# Inspira UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo engenheiro frontend **Rahul Vashishtha** (`@rahul-vashishtha` / `rahulv.dev`) e mantido sob a organização aberta **unovue** (`github.com/unovue/inspira-ui`), o **Inspira UI** (`inspira-ui.com`) é a principal e mais abrangente biblioteca de componentes animados do ecossistema **Vue 3** e **Nuxt 3/4**, acumulando mais de 5.000 estrelas no GitHub.

Historicamente, o desenvolvimento de landing pages futuristas com micro-interações de alta voltagem visual esteve aprisionado ao ecossistema React — impulsionado pelo monopólio do *Framer Motion* e pela explosão de bibliotecas como *Aceternity UI* (criada por Manu Arora) e *Magic UI* (criada por Dillion Verma). O ecossistema Vue frequentemente dependia de adaptações manuais imperfeitas ou bibliotecas de animação generalistas sem design opinionated. O Inspira UI nasceu explicitamente com a autorização formal dos criadores originais para portar, reimaginar e expandir esses padrões de vanguarda sob a arquitetura reativa nativa do Vue 3.

A assinatura visual e arquitetural do Inspira UI baseia-se em quatro pilares fundamentais:

1. **Fusão Estética Aceternity + Magic UI em Dialeto Vue Idiomático**:
   O Inspira UI não é um clone superficial: cada componente foi reescrito para explorar os pontos fortes da reatividade do Vue 3 (`<script setup lang="ts">`, `useTemplateRef()`, `defineModel()`, `v-bind()` em blocos `<style scoped>`, composables reativos do `@vueuse/core`). O resultado entrega o acabamento refinado das melhores referências da web: bordas de luz deslizantes (*Border Beam*), backdrops bioluminescentes (*Aurora*, *Lamp Effect*), cartões interativos em perspectiva (*3D Card*, *Glare Card*), barras de atalho elásticas (*macOS Dock*) e grades modulares assimétricas (*Bento Grid*).

2. **Pioneirismo em Tailwind CSS v4 & Paleta Dinâmica Oklch**:
   O Inspira UI v2 é totalmente alinhado à nova arquitetura do Tailwind CSS v4, baseada na diretiva `@theme`, dispensando configurações monolíticas em `tailwind.config.js`. Utiliza nativamente o espaço de cor **Oklch** para interpolações de gradientes sem bandas de descoloração cinzenta ("dead zones"), suportando alternância perfeita entre Dark Mode profundo (`zinc-950` / `slate-950`) e Light Mode límpido.

3. **Arquitetura de Registro Aberto Copy-and-Paste (shadcn Pattern)**:
   Rejeitando o encapsulamento rígido de dependências NPM (`npm install @inspira-ui/core`), o Inspira UI adota o paradigma distributivo do *shadcn-ui*: cada componente é um bloco de código-fonte isolado e transparente, distribuído via registro JSON (`public/r/*.json`) e transferido diretamente para a pasta de componentes da aplicação do desenvolvedor (`components/inspira/ui/...`). Isso assegura total liberdade para auditoria de segurança, otimização de bundle e customização extrema.

4. **Orquestração Híbrida de Performance (CSS Motion Paths + GPU Shaders + VueUse)**:
   Em vez de sobrecarregar a CPU com loops pesados de JavaScript onde CSS puro resolve, o Inspira UI adota uma hierarquia técnica inteligente:
   - Utiliza CSS moderno de alta performance (como CSS Motion Path `offset-path: rect()`, CSS Container Queries `@container`, `mix-blend-difference` e `mask-image`) para efeitos de borda e brilho.
   - Recorre ao **Motion-V** (a transposição oficial do Framer Motion para Vue) e **vue-use-spring** para físicas de mola fluida e tracking inercial.
   - Isola simulações complexas (partículas no Canvas 2D, globos 3D via *Cobe*, e cenas tridimensionais via *Three.js*/*TresJS*) com observadores de interseção e desmontagem estrita (`onBeforeUnmount`) para garantir 60 FPS contínuos.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **Startups de Inteligência Artificial, LLMs & Workspaces Generativos**:
   Aplicações em Nuxt 3/4 que precisam comunicar sofisticação computacional e autonomia em tempo real. Padrões como *LampEffect* (para a hero section), *VanishingInput* (para barras de prompt e chat de agentes autônomos) e *SparklesText* geram o impacto sensorial característico de produtos de ponta em IA.
2. **Plataformas de DevTools, Infraestrutura em Nuvem & Cibersegurança**:
   Produtos técnicos onde métricas globais, telemetria e fluxos de dados são protagonistas. A utilização do *Globe* interativo (Cobe) para distribuição de clusters, *TracingBeam* para documentações de arquitetura e *BentoGrid* para visualização de features complexas estabelece autoridade imediata.
3. **Landing Pages de Alto Impacto & Portfólios de Creative Technologists**:
   Estúdios digitais, agências de tecnologia e desenvolvedores Vue/Nuxt que necessitam romper a monotonia visual dos templates corporativos tradicionais, aplicando componentes como *3D Card*, *Lens* (lupa de ampliação com máscara) e *DirectionAwareHover*.
4. **Produtos SaaS B2B Modernos com Dashboards Interativos**:
   Aplicações que requerem navegação rápida e menus táteis, beneficiando-se do *Dock* elástico para menus flutuantes de atalho, *BorderBeam* para cards de plano Pro/Enterprise em tabelas de preços, e *ShimmerButton* para conversão em CTAs críticos.

### Papel no Ritmo Visual (Regra 60-30-10)

- **60% (Fundação Estrutural Neutra)**:
  Superfícies limpas e acessíveis construídas com componentes primitivos do **shadcn-vue**, **Radix Vue** ou **Nuxt UI**, tipografia funcional (`Geist Sans` ou `Inter`), espaçamentos modulares do Tailwind CSS v4 e paletas de neutralidade máxima (`zinc-900` / `zinc-950`).
- **30% (Camada Tátil de Interação & Ritmo — Inspira UI)**:
  Micro-interações que reagem ao mouse e ao scroll sem gritar pela atenção do usuário: cartões *BentoGrid* com translação de texto no hover, *BorderBeam* animando sutilmente o contorno do card em destaque no pricing, botões *ShimmerButton* nos formulários e barras de comando fluidas.
- **10% (Showstopper Heroico Protagonista)**:
  Exatamente **um** elemento dramático ativo por tela. Na Hero Section: ou um *LampEffect* iluminando a proposta de valor, ou um fundo bioluminescente *AuroraBackground*, ou um *ContainerScroll* inclinando o mock tridimensional do software na rolagem. O restante da interface repousa para manter a hierarquia e evitar sobrecarga cognitiva.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Interfaces Operacionais Densas de ERPs, PDVs e Telas de Trading em Tempo Real**:
  Telas que exigem processamento de milhares de linhas por segundo e foco absoluto em dados (como grids tabulares Bloomberg-style, sistemas de inventário ou prontuários médicos) são severamente prejudicadas por transições de escala, efeitos de desfoque e física de mola.
- **Aplicações Vue 2 Legadas (Options API)**:
  O Inspira UI foi integralmente construído sobre os paradigmas do **Vue 3.5+** (`<script setup lang="ts">`, `useTemplateRef`, `defineModel`, `withDefaults`). Não há suporte ou retrocompatibilidade para Vue 2 ou projetos ancorados na Options API antiga.
- **Páginas Mobile Voltadas para Conexões Críticas (2G/3G) ou Dispositivos de Baixo Desempenho**:
  Cenas com canvas intensivo (*Vortex*, shaders WebGL ou partículas densas) consomem ciclos excessivos de bateria e GPU em smartphones de entrada. Nesses dispositivos, os efeitos devem ser ocultados ou substituídos por gradientes CSS estáticos usando queries `@media (pointer: coarse)`.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **Multiplicação de Showstoppers Concorrentes**:
  Inserir um *LampEffect*, um *Meteors* caindo, um *Globe* girando e um *TracingBeam* disputando o mesmo espaço visual na mesma viewport. Esse acúmulo transforma o design em uma paródia visual ("AI slop"), confunde a hierarquia de leitura e destrói as métricas de Core Web Vitals (LCP/CLS).
- **Abuso do `VanishingInput` em Formulários de Múltiplos Campos**:
  O `VanishingInput` (que explode o texto em partículas de canvas ao submeter) é concebido estritamente para campos de busca de impacto ou caixas de comando de IA única. Usá-lo em campos comuns de cadastro (Nome, Email, Senha) cria frustração imediata e quebra a expectativa de formulários padrão.
- **Esquecimento da Flag `prefers-reduced-motion`**:
  Falhar em desativar animações contínuas de loop (como feixes orbitais e estrelas cadentes) para usuários que configuraram redução de movimento no sistema operacional. No Inspira UI, deve-se sempre utilizar a classe utilitária `motion-reduce:hidden` ou `motion-reduce:transform-none`.
- **Falta de Limpeza de Ciclo de Vida em Nuxt (Vazamento de Memória)**:
  Ao instanciar componentes que criam listeners globais de scroll/redimensionamento ou loops de `requestAnimationFrame` (como *Globe*, *Sparkles* e *TracingBeam*), é imperativo assegurar que o hook `onBeforeUnmount` destrua as instâncias e remova os event listeners, prevenindo vazamentos de memória durante navegações de rota via SPA.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

O catálogo do Inspira UI ultrapassa 140 componentes distribuídos em 11 categorias especializadas. A seguir estão os 12 componentes mais emblemáticos da suíte:

### 1. Bento Grid (`cards/bento-grid`)
- **Anatomia Visual**: Grade modular responsiva de cartões inspirada no design da Apple e Linear. Cada `BentoGridCard` possui acabamento dark mode com sombra interna suave (`box-shadow: 0 -20px 80px -20px #ffffff1f inset`), bordas sutis de 1px e hierarquia de três camadas: background dinâmico no slot de fundo, ícone e texto informático na frente.
- **Gatilho de Interação**: No hover, o bloco de texto translada verticalmente para cima (`-translate-y-10`), o ícone se contrai para 75% da escala original e um botão de chamada à ação ("CTA →") desliza de baixo para cima (`translate-y-0`) com revelação de opacidade total.
- **Onde encaixar**: Seção central de funcionalidades (Features Section) de SaaS e plataformas de nuvem, sintetizando produtos em uma única narrativa visual escaneável.

### 2. Border Beam (`special-effects/border-beam`)
- **Anatomia Visual**: Um raio de luz gradiente brilhante que percorre o perímetro exato de qualquer contêiner retangular ou circular. Implementado com CSS Motion Path nativo (`offset-path: rect(...)`), máscara vetorial com intersecção (`mask-clip: padding-box, border-box`) e gradiente linear que se estende suavemente para a transparência.
- **Gatilho de Interação**: Execução em loop contínuo e suave (velocidade configurável, padrão de 15 segundos), independente de interação do mouse.
- **Onde encaixar**: Destaque de planos "Popular" ou "Enterprise" em tabelas de Pricing, cartões de produto premium na Hero Section e modais de conversão crítica.

### 3. 3D Card (`cards/card-3d`)
- **Anatomia Visual**: Composto pelo trio `CardContainer`, `CardBody` e `CardItem`. O contêiner aplica perspectiva tridimensional (`perspective: 1000px; transform-style: preserve-3d`), enquanto elementos filhos individuais assumem deslocamentos no eixo Z (`translateZ: 50px`, `100px`) gerando sensação tátil de relevo físico e profundidade em camadas.
- **Gatilho de Interação**: O contêiner rastreia as coordenadas do mouse em tempo real, calculando a rotação nos eixos X e Y (`rotateY(x deg) rotateX(y deg)`). No `mouseleave`, retorna suavemente à posição neutra.
- **Onde encaixar**: Showcase do produto principal, cartões de planos anuais ou cartões de apresentação de equipe e palestrantes.

### 4. macOS Dock (`miscellaneous/dock`)
- **Anatomia Visual**: Barra de atalhos e ferramentas com cantos arredondados, backdrop blur com saturação e ícones circulares que emulam o dock do macOS. Suporta orientações horizontal e vertical.
- **Gatilho de Interação**: Conforme o mouse percorre a barra, o ícone sob o cursor e seus vizinhos imediatos aumentam harmonicamente de tamanho com base no raio de distância gaussiano calculado via injeção de dependência reativa (`calculateDistance`).
- **Onde encaixar**: Navegação flutuante inferior em portfolios criativos, barra de ferramentas de editores web, ou barra de atalhos de workspaces SaaS.

### 5. Lamp Effect (`special-effects/lamp-effect`)
- **Anatomia Visual**: Uma lâmpada bioluminescente de neon ciano suspensa no topo da tela, composta por gradientes cônicos espelhados (`conic-gradient`), camadas de difusão de desfoque (`blur-3xl`) e uma linha de neon horizontal que se expande simetricamente de 15rem para 30rem de largura, lançando um cone de luz suave sobre o conteúdo tipográfico.
- **Gatilho de Interação**: Disparado na montagem ou na entrada em viewport via animações CSS sincronizadas com delay e interpolação `ease-in-out`.
- **Onde encaixar**: O showstopper supremo para o topo da Hero Section ou encerramento épico de página no bloco de Call-to-Action final.

### 6. Aurora Background (`backgrounds/aurora-background`)
- **Anatomia Visual**: Fitas orgânicas de luz boreal em movimento contínuo que danificam a escuridão do dark mode com tons de azul celeste, índigo e violeta. Construído inteiramente com gradientes lineares repetidos em CSS, filtro de inversão, desfoque gaussiano de 10px e modo de mesclagem `mix-blend-difference`, sem custo de contexto WebGL.
- **Gatilho de Interação**: Animação contínua e suave em keyframes CSS com ciclo de 60 segundos, opcionalmente delimitada por uma máscara de gradiente elíptico radial.
- **Onde encaixar**: Fundo imersivo para seções de Hero de inteligência artificial, telas de login e onboarding, ou cabeçalhos de novidades de lançamentos.

### 7. Container Scroll Animation (`miscellaneous/container-scroll`)
- **Anatomia Visual**: O mockup ou screenshot do software é apresentado inicialmente deitado sob um ângulo 3D inclinado de 20 graus (`rotateX: 20deg`) com escala reduzida. Conforme o usuário rola a página, o contêiner se desdobra suavemente até ficar perfeitamente alinhado na vertical (`rotateX: 0deg`) e em escala total.
- **Gatilho de Interação**: Scroll contínuo do usuário mapeado reativamente através dos composables `useScroll` e `useElementBounding` do VueUse.
- **Onde encaixar**: Transição entre a Hero Section e a primeira seção de demonstração do produto em landing pages de SaaS moderno.

### 8. Interactive 3D Globe (`visualization/globe`)
- **Anatomia Visual**: Um globo esférico tridimensional renderizado em Canvas de alto desempenho através da biblioteca especializada **Cobe**, apresentando malha pontilhada da Terra, marcadores luminosos de coordenadas geográficas e brilho de atmosfera configurável.
- **Gatilho de Interação**: Rotação orbital inercial automática que pode ser arrastada e girada manualmente pelo usuário via eventos de mouse/touch, amortecida por física de mola real com **vue-use-spring**.
- **Onde encaixar**: Seções de infraestrutura global de nuvem, redes de entrega de conteúdo (CDN), presença internacional de clientes ou mapas de telemetria.

### 9. Vanishing Input (`input-and-forms/vanishing-input`)
- **Anatomia Visual**: Campo de busca elegante com placeholders que alternam ciclicamente com transição de desfoque e deslizamento. Ao teclar Enter ou clicar no botão de submissão, os caracteres digitados são convertidos instantaneamente em uma malha de pixels desenhada no Canvas, que se pulverizam no ar como partículas dissolventes antes de limpar o campo.
- **Gatilho de Interação**: Submissão do formulário via tecla Enter ou clique no botão de envio.
- **Onde encaixar**: Barra de prompt de comando principal em aplicações de IA generativa, busca global do sistema ou campo de inscrição em newsletters exclusivas.

### 10. Tracing Beam (`special-effects/tracing-beam`)
- **Anatomia Visual**: Uma linha vertical guia em SVG que acompanha a leitura lateral de um artigo longo ou documentação técnica. Uma gota de luz com gradiente multicolorido (`#18CCFC` a `#AE48FF`) corre ao longo do traçado SVG conforme o leitor avança pelo texto.
- **Gatilho de Interação**: Vinculado estritamente à posição de rolagem da janela, com posicionamento elástico sincronizado via `vue-use-spring` para garantir que a luz persiga a rolagem sem trepidações.
- **Onde encaixar**: Artigos de blog de engenharia de software, documentação de APIs extensas e seções narrativas de "Como Funciona" ou cronologias (Timelines).

### 11. Lens (`special-effects/lens`)
- **Anatomia Visual**: Uma lente circular de aumento virtual que repousa sobre uma imagem, gráfico ou interface. O interior da lente exibe o conteúdo ampliado (zoom configurável, ex: 1.5x a 2.5x) com foco cristalino delimitado por uma máscara de gradiente radial suave.
- **Gatilho de Interação**: Rastreia a posição do cursor em tempo real com entrada suave via `Motion-V` (`scale: 0.58 -> 1`, fade in com `easeOut`). Suporta também modo estático para destacar detalhes predeterminados.
- **Onde encaixar**: Vitrines de produtos com texturas refinadas (hardware, relojoaria, moda), inspeção de diagramas de arquitetura densos ou capturas de tela de alta resolução.

### 12. Shimmer Button (`buttons/shimmer-button`)
- **Anatomia Visual**: Botão de conversão de alto luxo com bordas arredondadas (`border-radius: 100px`) e uma faixa de brilho perolado cônico que contorna continuamente a silhueta externa do botão, combinada com uma sutil sombra de profundidade interna (`shadow-[inset_0_-8px_10px_#ffffff1f]`).
- **Gatilho de Interação**: Animação angular infinita do feixe cônico com resposta tátil de clique (`active:translate-y-px` e aprofundamento de sombra interna).
- **Onde encaixar**: Botão de Ação Primária (Primary CTA) da Hero Section, botões de upgrade de conta e botões de finalização de checkout.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Ambiente

O Inspira UI opera de forma excelente com **Vue 3 (v3.5+)** e **Nuxt 3 / Nuxt 4**, integrado ao **Tailwind CSS v4**.

```bash
# Instalação das dependências centrais de animação e utilitários
pnpm add @vueuse/core motion-v tw-animate-css @inspira-ui/plugins clsx tailwind-merge

# Pacotes adicionais necessários para componentes de visualização específicos
pnpm add cobe vue-use-spring simplex-noise
```

### Configuração de Estilo (Tailwind CSS v4 & Variáveis de Tema)

Em seu arquivo de estilos global (`main.css` ou `assets/css/main.css`), configure as diretivas do Tailwind CSS v4 integradas às variáveis do ecossistema:

```css
@import "tailwindcss";
@import "tw-animate-css";

@custom-variant dark (&:is(.dark *));

:root {
  --background: oklch(1 0 0);
  --foreground: oklch(0.141 0.005 285.823);
  --card: oklch(1 0 0);
  --card-foreground: oklch(0.141 0.005 285.823);
  --primary: oklch(0.21 0.006 285.885);
  --primary-foreground: oklch(0.985 0 0);
  --border: oklch(0.92 0.004 286.32);
  --radius: 0.625rem;
}

.dark {
  --background: oklch(0.141 0.005 285.823);
  --foreground: oklch(0.985 0 0);
  --card: oklch(0.141 0.005 285.823);
  --card-foreground: oklch(0.985 0 0);
  --primary: oklch(0.985 0 0);
  --primary-foreground: oklch(0.21 0.006 285.885);
  --border: oklch(0.274 0.006 286.033);
}

@theme inline {
  --color-background: var(--background);
  --color-foreground: var(--foreground);
  --color-card: var(--card);
  --color-card-foreground: var(--card-foreground);
  --color-primary: var(--primary);
  --color-primary-foreground: var(--primary-foreground);
  --color-border: var(--border);
}
```

### Física de Movimento, Molas e Interpolação

O Inspira UI calibra rigorosamente suas molas para evitar oscilações borrachudas amadoras, adotando valores matemáticos com amortecimento estrito:

- **Molas de Interação de Cursor & Globos (via `vue-use-spring`)**:
  - `mass`: `1.0`
  - `tension` (stiffness): `280`
  - `friction` (damping): `100`
  - `precision`: `0.001`
  *(Garante que o rastreamento inercial atinja repouso sem tremores perceptíveis)*.
- **Rastreamento de Tracing Beam**:
  - `tension`: `80`
  - `friction`: `26`
  - `precision`: `0.01`
  *(Produz uma desaceleração viscosa ultra-elegante durante scrolls rápidos)*.
- **Transições DOM Cinéticas (via `motion-v`)**:
  - Curva de aceleração: `cubic-bezier(0.16, 1, 0.3, 1)` (Quart Out clássico).
  - Escalas elásticas: `stiffness: 300`, `damping: 30`.

---

### Receita de Código Funcional: Hero Showstopper Integrada (Vue 3 / Nuxt)

Abaixo está uma implementação completa e pronta para produção de uma seção de destaque (Hero Section) unindo o **LampEffect**, tipografia com gradiente cinético e um card em destaque protegido por **BorderBeam**:

```vue
<script setup lang="ts">
import { ref } from "vue";
import { ArrowRight, Sparkles, CheckCircle2 } from "lucide-vue-next";

// Componentes importados do registro Inspira UI
import LampEffect from "@/components/inspira/ui/lamp-effect/LampEffect.vue";
import BorderBeam from "@/components/inspira/ui/border-beam/BorderBeam.vue";
import ShimmerButton from "@/components/inspira/ui/shimmer-button/ShimmerButton.vue";

const activeFeature = ref("Autonomous Dispatch");
</script>

<template>
  <section class="relative min-h-screen w-full overflow-hidden bg-slate-950 text-white">
    <!-- Efeito Protagonista de Iluminação (Showstopper 10%) -->
    <LampEffect :duration="0.9" :delay="0.2">
      <!-- Tipografia e Mensagem Principal -->
      <div class="flex flex-col items-center text-center">
        <div
          class="mb-4 inline-flex items-center gap-2 rounded-full border border-cyan-500/30 bg-cyan-950/40 px-3 py-1 text-xs font-medium text-cyan-300 backdrop-blur-md"
        >
          <Sparkles class="size-3.5 animate-pulse text-cyan-400" />
          <span>Inspira UI para Vue 3 & Nuxt 4</span>
        </div>

        <h1
          class="bg-gradient-to-br from-slate-100 via-slate-200 to-slate-500 bg-clip-text text-4xl font-extrabold tracking-tight text-transparent sm:text-6xl md:text-7xl"
        >
          Engenharia Cinética <br />
          com Elegância Absoluta
        </h1>

        <p class="mt-6 max-w-2xl text-base text-slate-400 sm:text-lg">
          Eleve interfaces construídas em Vue e Nuxt ao mesmo patamar visual das maiores referências do Vale do Silício, combinando Tailwind CSS v4, física de molas e aceleração por GPU.
        </p>

        <!-- Ação Primária com Shimmer Button -->
        <div class="mt-8 flex flex-wrap items-center justify-center gap-4">
          <ShimmerButton
            shimmer-color="#38bdf8"
            background="rgba(2, 6, 23, 0.9)"
            shimmer-duration="2.5s"
            border-radius="9999px"
            class="h-12 px-8 text-sm font-semibold tracking-wide text-white"
          >
            <span>Explorar Componentes</span>
            <ArrowRight class="ml-2 size-4" />
          </ShimmerButton>

          <button
            class="h-12 rounded-full border border-slate-800 bg-slate-900/60 px-6 text-sm font-medium text-slate-300 transition-colors hover:bg-slate-800 hover:text-white"
          >
            Ler a Documentação
          </button>
        </div>
      </div>

      <!-- Card Central de Demonstração Envolvido por Border Beam -->
      <div
        class="relative mt-16 w-full max-w-3xl overflow-hidden rounded-2xl border border-white/10 bg-slate-900/80 p-6 shadow-2xl backdrop-blur-xl md:p-8"
      >
        <!-- Feixe de Borda Dinâmico Contornando o Card -->
        <BorderBeam
          :size="250"
          :duration="12"
          :border-width="2"
          color-from="#06b6d4"
          color-to="#8b5cf6"
        />

        <div class="flex items-center justify-between border-b border-white/10 pb-4">
          <div class="flex items-center gap-2">
            <div class="size-3 rounded-full bg-red-500/80" />
            <div class="size-3 rounded-full bg-yellow-500/80" />
            <div class="size-3 rounded-full bg-green-500/80" />
            <span class="ml-2 text-xs font-mono text-slate-400">agent-orchestrator.vue</span>
          </div>
          <span class="rounded bg-cyan-950/60 px-2 py-0.5 text-xs font-mono text-cyan-400 border border-cyan-800/40">
            Nuxt 4 Ready
          </span>
        </div>

        <div class="mt-6 grid grid-cols-1 gap-4 sm:grid-cols-3">
          <div
            v-for="feature in ['Zero Runtime Bundled', 'Motion-V Springs', 'Full Copy-Paste']"
            :key="feature"
            class="flex items-center gap-2.5 rounded-lg border border-white/5 bg-white/5 p-3"
          >
            <CheckCircle2 class="size-4 shrink-0 text-cyan-400" />
            <span class="text-xs font-medium text-slate-200">{{ feature }}</span>
          </div>
        </div>
      </div>
    </LampEffect>
  </section>
</template>
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma nova aplicação ou landing page no ecossistema Vue 3 / Nuxt utilizando esta referência, a IA orquestradora deve incorporar as seguintes instruções técnicas no `DESIGN_BLUEPRINT.md`:

1. **Declaração de Arquitetura de Componentes**:
   - Registrar no Blueprint que componentes animados do catálogo do Inspira UI serão hospedados localmente sob `@/components/inspira/ui/<component-name>/...`.
   - Assegurar que componentes de apoio estrutural acessível (como diálogos, dropdowns e tooltips) sejam providos via **shadcn-vue** ou **Radix Vue**, evitando redundância.

2. **Gerenciamento de Dependências e Pacotes**:
   - Garantir que `package.json` contenha as bibliotecas de suporte compatíveis com o build do projeto: `@vueuse/core`, `motion-v`, `vue-use-spring`, `tw-animate-css`, `clsx` e `tailwind-merge`.
   - Se o projeto utilizar Nuxt 3 ou 4, confirmar que módulos que requerem contexto de navegador (`cobe`, `three`) sejam declarados com `<ClientOnly>` ou encapsulados em hooks `onMounted`.

3. **Cota Estrita de Showstoppers (Guardrail de Performance)**:
   - Limitar rigorosamente o uso de efeitos pesados a **1 showstopper protagonista por tela**:
     - *Hero Section*: Permitido escolher entre `LampEffect`, `AuroraBackground` ou `ContainerScroll`.
     - *Corpo da Página*: Permitido usar `BentoGrid` (com transições CSS) e `BorderBeam` (limitado a 1 ou 2 cards de pricing ou destaque).
     - *Proibido*: Combinar múltiplos fundos de partículas ou shaders em seções consecutivas.

4. **Tratamento de Desmontagem & Cleanup Reativo**:
   - Todo componente com loop de `requestAnimationFrame` ou listeners de scroll/redimensionamento (`Globe`, `TracingBeam`, `Sparkles`) deve implementar limpeza mandatória em `onBeforeUnmount()`:
     ```typescript
     onBeforeUnmount(() => {
       window.removeEventListener('scroll', updateScroll);
       window.removeEventListener('resize', updateResize);
       globeInstance?.destroy();
     });
     ```

5. **Acessibilidade & Acomodação Sensorial**:
   - Todos os loops contínuos de animação devem ser desativados ou ocultados condicionalmente sob a media query `prefers-reduced-motion: reduce`.
   - Textos cinéticos e efeitos de decodificação devem sempre fornecer alternativas legíveis por leitores de tela utilizando classes `sr-only`.
