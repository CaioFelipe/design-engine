---
id: "skiper-ui"
name: "Skiper UI"
url: "https://skiper-ui.com/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Dark Canvas & High-Contrast Craft", "View-Transitions Cinematic Reveals", "Depth-Layered 3D Perspective Carousels", "Scroll-Driven Kinetic Typography"]
densidade_informacao: "Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Framer Motion/JS) a Alto (Swiper 3D/View Transitions/Canvas)"
stack_frameworks: ["React", "Next.js 14/15 (App Router)", "Tailwind CSS (v3/v4)", "Motion (Framer Motion)", "Swiper", "View Transitions API", "Radix UI", "Lucide React"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Geist Mono", "Inter", "Plus Jakarta Sans", "Cabinet Grotesk"]
  paletas_ideais: ["Pitch Black & Deep Zinc (#000000 / #09090b)", "Monochrome High-Contrast White/Silver", "Electric Sky Blue (#0ea5e9 / #38bdf8) AI & Status Accents"]
  combinacoes_recomendadas: ["Shadcn UI", "Magic UI", "Cult UI", "Aceternity UI", "Vaul"]
  conflitos_esteticos: ["Flat Retro Brutalism com cantos vivos sem easing", "Corporate Memphis hiper-colorido e lúdico", "Skeuomorfismo pesado pré-iOS 7 com bevels metálicos e texturas de couro"]
---

# Skiper UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo engenheiro frontend e designer **Gxuri** (@Gur__vi / @gxuri__), o **Skiper UI** (`skiper-ui.com`) consolidou-se como um dos ecossistemas de componentes animados mais arrojados do ecossistema React/Next.js moderno. Sob a bandeira de *"Un-common Components for shadcn/ui"*, a biblioteca foi concebida com um propósito cirúrgico: libertar aplicações web de landing pages genéricas e clones monótonos de SaaS, introduzindo componentes que normalmente exigiriam dias de engenharia criativa com matemática de coordenadas, shaders ou manipuladores de canvas.

A identidade estética e funcional do Skiper UI repousa sobre quatro pilares distintivos:

1. **Adoção Pioneira da View Transitions API Nativa**:
   Diferente de bibliotecas que simulam transições com invólucros `div` opacos ou sobreposições absolutas pesadas, o Skiper UI é uma das primeiras suítes a integrar a **View Transitions API** nativa dos navegadores (`document.startViewTransition`) com o ecossistema `next-themes`. O efeito de alternância de tema escuro/claro (*Theme Toggle / skiper26*) não é uma simples troca abrupta de classe Tailwind: ele gera uma frente de onda circular (`clip-path: circle(...)`) que se expande a partir do botão ou do cursor do usuário até as bordas da viewport, calculando o raio máximo por hipotenusa geométrica (`Math.hypot`). O resultado é uma transição cinematográfica fluida em 60fps sem repinturas custosas de layout.

2. **Carrosséis Tridimensionais com Profundidade de Campo & Perspectiva**:
   Enquanto sliders convencionais apenas deslocam cartões no eixo $X$, os carrosséis do Skiper UI (*Creative Carousels*, *Dia Browser Carousel*, *Apple Feature Showcase*) introduzem matrizes de perspectiva 3D (`perspective(1000px) rotateY(...) scale(...) translateZ(...)`), desfoques seletivos de profundidade (*depth of field blur*) e barras de progresso lineares segmentadas sincronizadas ao ciclo de autoplay. Cada slide inativo recua no espaço tridimensional com gradiente de opacidade, enquanto o item central salta em direção ao usuário com precisão tátil.

3. **Tipografia Cinética Conduzida por Rolagem (Scroll-Driven Kinetic Typography)**:
   A tipografia no Skiper UI deixa de ser estática para se transformar em um elemento de narrativa interativa. Por meio de componentes como *Text Reveal Box* e *Horizontal Text Reveal*, sentenças são decompostas em palavras e caracteres que sofrem rotação angular (*skew* de $2^{\circ}$ a $6^{\circ}$), translação vertical progressiva e saturação de cor vinculada diretamente à posição de rolagem (`useScroll` e `useTransform`), gerando a experiência imersiva de leitura editorial de estúdios de vanguarda como Apple, Linear e Loom.

4. **Distribuição Aberta e Agnóstica via shadcn CLI 3.0**:
   Seguindo o padrão de ouro da indústria, o Skiper UI não força pacotes NPM proprietários ou dependências fechadas. Cada componente vive como um arquivo TypeScript/TSX autocontido que é injetado diretamente na pasta `@/components/v1/...` do projeto através do comando `npx shadcn@latest add @skiper-ui/...`. O desenvolvedor mantém 100% de controle sobre o código-fonte, podendo editar estados, estilizações Tailwind e dinâmicas de mola sem camadas de abstração ocultas.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **Landing Pages de Alto Impacto para Produtos de IA & DevTools**:
   Onde a percepção de ponta tecnológica precisa ser instantânea. Componentes como o *Dynamic Island*, *Image Reveal* e *Horizontal Text Reveal* comunicam sofisticação técnica imediata para plataformas de infraestrutura em nuvem, terminais inteligentes e interfaces conversacionais.
2. **Portfólios Criativos, Estúdios Digitais & Design Engineers**:
   Para criadores que precisam provar domínio estético e técnico. Efeitos como *Image Cursor Trail*, *Things Drag and Scroll* e *Dia Browser Showcase* transformam listas de cases em experiências tridimensionais memoráveis.
3. **Plataformas Web3, Fintechs & Dashboards Cripto**:
   Aplicações financeiras que exigem fluxos de alta conversão beneficiam-se diretamente de componentes dedicados, como o *Aave Token Swap Card*, que unifica campos de valor, taxas e alternadores de rede com micro-interações de clique e feedback visual imediato.
4. **Onboarding Interativo & Telas de Autenticação Premium**:
   Em fluxos onde a primeira impressão determina a retenção, o modal *Devouring Details Sign In* eleva o login convencional a uma experiência lúdica, com campos de texto que se expandem conforme a entrada de dados.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Neutra e Sólida)**:
  Estrutura base orientada pelo `shadcn/ui` padrão: fundos pretos absolutos (`bg-black` ou `bg-zinc-950`), divisores finos (`border-zinc-800/50`), tipografia neutra em `Geist Sans` ou `Inter` e cartões utilitários sem motion excessivo.
- **30% (Camada Tátil e Micro-interações do Skiper UI)**:
  Aqui entram os botões animados, o *View Transitions Theme Toggle*, *Hover Members* nas seções de equipe ou prova social, e os *Vercel Tooltips* para contextualização de dados em tabelas ou cartões Bento.
- **10% (Showstoppers Protagonistas & Hero Highlights)**:
  Reserve rigorosamente apenas **um** showstopper por viewport: o *Creative 3D Carousel* na seção de recursos principais, ou a *Dynamic Island* fixa no topo, ou o *Horizontal Text Reveal* como divisor dramático entre a Hero e os planos de preço. A coexistência de dois carrosséis 3D ou um cursor trail competindo com texto rotativo destrói a hierarquia cognitiva da página.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Painéis Administrativos com Alta Densidade de Dados (ERPs & B2B Tradicionais)**:
  Em interfaces que exibem planilhas financeiras, auditorias fiscais ou centenas de registros em grade, efeitos cinéticos de texto (*Text Reveal*), rotações tridimensionais e carrosséis com autoplay adicionam atraso perceptual e atrapalham a varredura visual do operador.
- **Dispositivos Móveis de Baixa Potência com Bateria Degradada**:
  Efeitos que manipulam simultaneamente `useScroll`, loops de animação com `requestAnimationFrame` contínuo (como o *Image Cursor Trail*) e instâncias múltiplas de Swiper 3D consomem intensamente a GPU/CPU de aparelhos modestos, causando aquecimento térmico e quedas para 20-30 fps.
- **Aplicações Estritamente Governamentais ou de Saúde Pública (WCAG AAA)**:
  O texto revelado por desfoque ou variação de opacidade enquanto o usuário rola a página pode violar normas de leitura contínua para usuários com deficiências cognitivas ou baixa visão, a menos que um fallback completo para `prefers-reduced-motion` esteja ativado.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **Multiplicação de Trails de Cursor e Partículas**: Habilitar *Image Cursor Trail* globalmente em toda a aplicação. O efeito se torna invasivo e cobre botões de ação essenciais (`CTA`), irritando o visitante. Ele deve ser restrito a uma área de vitrine ou galeria isolada.
- **Transições de View Transitions Concorrentes**: Disparar um tema com *View Transitions API* ao mesmo tempo em que um modal com Framer Motion está em fase de abertura, travando o pipeline de renderização do motor Chromium.
- **Texto Cinético Inlegível em Rápida Rolagem**: Configurar limiares de translação (`y: [100, 0]`) com intervalos de rolagem muito curtos, fazendo o texto "piscar" ou passar rápido demais antes de o usuário conseguir completar a leitura.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 12 componentes mais emblemáticos do ecossistema Skiper UI:

### 1. View Transitions Circular Theme Switcher (`@skiper-ui/skiper26`)
- **Anatomia Visual**: Botão em pílula ou círculo compacto (`bg-muted/80 backdrop-blur-md border`) contendo ícones vetoriais de Sol/Lua. Ao ser clicado, não ocorre repintura súbita: o navegador captura snapshots do estado atual e do próximo, aplicando uma máscara `clip-path: circle(0px at X Y)` que se abre para `circle(R_max at X Y)` varrendo toda a viewport como uma lente de câmera analógica.
- **Gatilho de Interação**: Clique do mouse; captura as coordenadas exatas do clique (`event.clientX`, `event.clientY`) para definir o centro focal da expansão circular via CSS pseudo-elementos `::view-transition-old(root)` e `::view-transition-new(root)`.
- **Onde encaixar**: Navbar global no canto superior direito, menu flutuante ou barra de rodapé utilitária.

### 2. Horizontal Text Reveal Box (`@skiper-ui/skiper70` / `@skiper-ui/skiper72`)
- **Anatomia Visual**: Bloco de texto tipográfico em corpo avantajado (`text-4xl md:text-7xl font-bold tracking-tight`) contido em uma seção travada com `sticky top-0`. Conforme o usuário rola a página verticalmente, as palavras deslizam no eixo horizontal e sofrem transição contínua de um tom acinzentado de baixa opacidade (`text-zinc-600`) para o branco luminescente (`text-white`), com leve inclinação (*skewX: -4deg* a *0deg*).
- **Gatilho de Interação**: Rolagem da página mapeada com `useScroll({ target: containerRef, offset: ["start end", "end start"] })` e transformações interpoladas linearmente via `useTransform`.
- **Onde encaixar**: Seção de manifesto da empresa, transição dramática da Hero para a grade de recursos, ou chamada institucional de missão.

### 3. Creative Carousel 001/002 — 3D Perspective (`@skiper-ui/skiper50`)
- **Anatomia Visual**: Grade de slides com visualização centralizada em deck. O slide ativo projeta-se para a frente com escala total (`scale: 1`, `z-index: 20`), sombras profundas (`shadow-2xl`) e cores vívidas. Os slides laterais recuam no eixo $Z$ com rotação angular (`rotateY(25deg)`), desfoque gaussiano suave (`blur-sm`) e opacidade reduzida (`opacity-50`), criando uma ilusão de cilindro de exibição ou carrossel de vinis.
- **Gatilho de Interação**: Arrastar com mouse/touch (*touch-drag*), clique nos cartões laterais para centralização imediata, ou setas de navegação com transições de mola acopladas ao Swiper/Motion.
- **Onde encaixar**: Vitrine de recursos do produto, galeria de depoimentos visuais de clientes ou showcase de telas de software.

### 4. Apple Product Showcase Carousel (`@skiper-ui/skiper77`)
- **Anatomia Visual**: Slider horizontal minimalista diretamente inspirado no design de marketing da Apple para iPhone e MacBook. Combina um palco principal com imagem fotográfica de alta definição, seletores circulares de cor (*color swatches*) na base e especificações textuais dinâmicas. Ao selecionar uma cor ou avançar o slide, a imagem do produto sofre um cross-fade suave enquanto os textos técnicos deslizam verticalmente com efeito de rolagem de cassete numérico.
- **Gatilho de Interação**: Clique nas amostras de cor ou nas setas de avanço; suporte a deslizamento tátil em smartphones.
- **Onde encaixar**: Seção de hardware, apresentação de planos de assinatura ou página de produto em e-commerces de alto padrão.

### 5. Dia Browser Showcase Carousel (`@skiper-ui/skiper78`)
- **Anatomia Visual**: Réplica refinada da vitrine interativa utilizada pelo navegador Dia. Apresenta uma sequência de slides com cantos amplamente arredondados (`rounded-3xl`), cercados por bordas sutis e barras de progresso lineares individuais na base. Cada barra enche-se gradativamente ao longo de 5 segundos; ao completar, o carrossel dispara uma animação de slide direcional suave.
- **Gatilho de Interação**: Autoplay sincronizado com pausa ao passar o mouse (*hover pause*), além de cliques diretos nas abas de progresso para salto imediato entre slides.
- **Onde encaixar**: Demonstração de fluxo de trabalho passo-a-passo (Step-by-step feature walkthrough) na Hero ou no meio da landing page.

### 6. Image Reveal on Scroll (`@skiper-ui/skiper71`)
- **Anatomia Visual**: Cartão de mídia que se inicia como uma máscara comprimida em formato de fenda estreita ou pílula central. Conforme a rolagem atinge o componente, as dimensões da máscara expandem-se dinamicamente (`clip-path: inset(0% 0% round 24px)`) revelando uma imagem ou vídeo em loop em tela cheia com efeito de desaceleração elástica.
- **Gatilho de Interação**: Scroll progressivo com threshold de entrada calculado pelo Intersection Observer ou `useScroll`.
- **Onde encaixar**: Clímax visual entre a apresentação de um problema e a introdução da solução de software.

### 7. Inertial Image Cursor Trail (`@skiper-ui/skiper18`)
- **Anatomia Visual**: Sistema de partículas de cursor onde o movimento do ponteiro do usuário emite réplicas flutuantes de miniaturas de imagens ou capas de projetos. Cada elemento emitido surge nas coordenadas do cursor e desvanece suavemente ao longo de 800ms com leve amortecimento inercial e rotação aleatória calculada por semente (`rotate(-6deg to +6deg)`).
- **Gatilho de Interação**: Listener contínuo de `pointermove` com controle de taxa (*throttling* a cada 50ms ou limiar de distância de 40px percorrida).
- **Onde encaixar**: Portfólios de estúdios criativos, vitrines de trabalhos selecionados e seções experimentais.

### 8. Dynamic Island Morphing Pill (`@skiper-ui/skiper2`)
- **Anatomia Visual**: Container flutuante em preto absoluto (`bg-black text-white rounded-full border border-zinc-800/80 shadow-2xl`) fixo no topo da viewport. Transiciona fluidamente entre múltiplos estados geométricos: pílula compacta mínima (`h-10 w-32`), reprodutor de áudio expandido (`h-16 w-80`), ou cartão de notificação completo (`h-32 w-96 rounded-3xl`), sem quebras de layout.
- **Gatilho de Interação**: Disparado por eventos de sistema (upload concluído, cópia de código para a área de transferência, aviso de status de API) ou clique de expansão.
- **Onde encaixar**: Topo central fixo da viewport em aplicações de monitoramento em tempo real ou cabeçalho global interativo.

### 9. Things Drag & Scroll Canvas (`@skiper-ui/skiper5`)
- **Anatomia Visual**: Superfície bidimensional infinita ou grade livre de cartões onde elementos da interface podem ser clicados, elevados do plano (`z-index: 50`, elevação de sombra) e arrastados livremente pela tela com física inercial de amortecimento (*elastic bounce*).
- **Gatilho de Interação**: Eventos de arrasto `drag` do Framer Motion com `dragConstraints` e `dragElastic={0.2}`.
- **Onde encaixar**: Moodboards de design, murais de inspiração interativos ou seções "About Us" lúdicas.

### 10. Devouring Details Sign-In (`@skiper-ui/skiper56`)
- **Anatomia Visual**: Cartão de autenticação minimalista que inicia como um botão compacto ou campo único de email. Conforme o usuário preenche o dado e pressiona `Enter`, o cartão expande sua própria geometria com animação de desdobramento, revelando o campo de senha, biometria ou código de uso único (OTP), sem redirecionamentos de rota.
- **Gatilho de Interação**: Foco em input e submissão parcial de etapas com morphing estrutural via `layout` do Framer Motion.
- **Onde encaixar**: Modais de autenticação rápida, captura de leads em waitlists ou finalização de checkout em uma etapa.

### 11. Hover Members Avatar Stack (`@skiper-ui/skiper6`)
- **Anatomia Visual**: Agrupamento sobreposto de avatares de equipe ou colaboradores (`flex -space-x-4`). Ao passar o mouse sobre qualquer avatar, os irmãos adjacentes abrem espaço organicamente com repulsão magnética elástica, enquanto o avatar sob o cursor ganha escala (`scale-125`), traz à tona um tooltip com nome, cargo e redes sociais, e eleva seu `z-index`.
- **Gatilho de Interação**: Hover do mouse rastreado com `layoutId` e física de mola balanceada.
- **Onde encaixar**: Seção de prova social na Hero ("Confiado por mais de 10.000 engenheiros"), rodapé de páginas de comunidade ou página de equipe.

### 12. Aave Token Swap Interface (`@skiper-ui/skiper22`)
- **Anatomia Visual**: Card refinado de conversão de criptoativos e tokens. Apresenta superfícies em cinza escuro translúcido com acabamento de vidro, seletores de token em pílula com ícones vetoriais de redes (Ethereum, Polygon, Arbitrum), botão central de inversão de rota com rotação de 180 graus elástica e display numérico com formatação contínua de slippage.
- **Gatilho de Interação**: Clique no botão central de troca com giro vetorial animado e atualização em tempo real de taxas.
- **Onde encaixar**: Landing pages de protocolos Web3, dApps de finanças descentralizadas (DeFi) e simuladores de câmbio fintech.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Ambiente

O Skiper UI opera perfeitamente sobre a infraestrutura do ecossistema shadcn/ui. Para inicializar um ambiente compatível em Next.js 14/15:

```bash
# 1. Dependências centrais de animação e utilitários
npm install framer-motion clsx tailwind-merge lucide-react next-themes swiper

# 2. Adicionar componente diretamente via shadcn CLI (Exemplo: Theme Switcher skiper26)
npx shadcn@latest add @skiper-ui/skiper26
```

Configuração necessária do utilitário `cn` em `@/lib/utils.ts`:
```ts
import { clsx, type ClassValue } from "clsx";
import { twMerge } from "tailwind-merge";

export function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs));
}
```

---

### Física de Movimento, Interpolações & View Transitions

1. **Parâmetros de Mola (Spring Physics) no Framer Motion**:
   - **Transições de Carrossel e Expansão de Modais**:
     `{ type: "spring", stiffness: 320, damping: 28, mass: 0.8 }`
     *Garante que os cartões cheguem à posição final sem oscilações repetitivas incômodas, mas com resposta tátil firme.*
   - **Repulsão e Hover Magnético (Hover Members)**:
     `{ type: "spring", stiffness: 450, damping: 22, mass: 0.5 }`
     *Propicia uma resposta ultrarrápida aos gestos do mouse.*

2. **Curvas de Bézier Cúbico para Rolagem Cinética**:
   - Para revelação de texto e imagens por scroll:
     `transition: { ease: [0.16, 1, 0.3, 1], duration: 0.8 }` (*easeOutExpo*)

3. **Fórmula Geométrica de Raio Máximo para View Transitions**:
   Ao alternar o tema com a View Transitions API, o círculo de revelação precisa cobrir o canto mais distante da tela a partir da coordenada $(X, Y)$ do clique:
   $$R_{\max} = \sqrt{\max(X, W - X)^2 + \max(Y, H - Y)^2}$$
   Onde $W$ é `window.innerWidth` e $H$ é `window.innerHeight`.

---

### Receita de Código Funcional 1: Circular View Transition Theme Switcher (`skiper26`)

Abaixo está a implementação completa e pronta para produção do alternador de tema com expansão circular nativa:

```tsx
"use client";

import React, { useRef } from "react";
import { useTheme } from "next-themes";
import { Sun, Moon } from "lucide-react";

export function SkiperThemeToggle() {
  const { theme, setTheme, resolvedTheme } = useTheme();
  const buttonRef = useRef<HTMLButtonElement>(null);

  const toggleTheme = (e: React.MouseEvent<HTMLButtonElement>) => {
    const isDark = resolvedTheme === "dark";
    const nextTheme = isDark ? "light" : "dark";

    // Fallback gracioso caso o navegador não suporte View Transitions
    if (!document.startViewTransition) {
      setTheme(nextTheme);
      return;
    }

    // Coordenadas da origem do clique para expansão circular
    const x = e.clientX;
    const y = e.clientY;

    // Distância máxima até o canto mais distante da tela
    const endRadius = Math.hypot(
      Math.max(x, window.innerWidth - x),
      Math.max(y, window.innerHeight - y)
    );

    const transition = document.startViewTransition(() => {
      setTheme(nextTheme);
    });

    transition.ready.then(() => {
      // Dispara a animação nativa do pseudo-elemento do navegador
      document.documentElement.animate(
        {
          clipPath: [
            `circle(0px at ${x}px ${y}px)`,
            `circle(${endRadius}px at ${x}px ${y}px)`,
          ],
        },
        {
          duration: 550,
          easing: "cubic-bezier(0.4, 0, 0.2, 1)",
          pseudoElement: "::view-transition-new(root)",
        }
      );
    });
  };

  const isCurrentDark = resolvedTheme === "dark";

  return (
    <button
      ref={buttonRef}
      onClick={toggleTheme}
      aria-label="Alternar modo de cor"
      className="relative flex size-10 items-center justify-center rounded-2xl border border-zinc-200 bg-white text-zinc-900 shadow-sm transition-transform active:scale-95 dark:border-zinc-800 dark:bg-zinc-950 dark:text-zinc-100 hover:border-zinc-300 dark:hover:border-zinc-700"
    >
      <Sun className="size-4 rotate-0 scale-100 transition-all dark:-rotate-90 dark:scale-0" />
      <Moon className="absolute size-4 rotate-90 scale-0 transition-all dark:rotate-0 dark:scale-100" />
      <span className="sr-only">Alternar tema</span>
    </button>
  );
}
```

Configuração de CSS necessária no arquivo global (`globals.css`):
```css
/* Permite que o pseudo-elemento da View Transitions não seja sobrescrito */
::view-transition-old(root),
::view-transition-new(root) {
  animation: none;
  mix-blend-mode: normal;
}
::view-transition-old(root) {
  z-index: 1;
}
::view-transition-new(root) {
  z-index: 9999;
}
.dark::view-transition-old(root) {
  z-index: 9999;
}
.dark::view-transition-new(root) {
  z-index: 1;
}
```

---

### Receita de Código Funcional 2: Horizontal Scroll Text Reveal Box (`skiper70`)

```tsx
"use client";

import React, { useRef } from "react";
import { motion, useScroll, useTransform } from "framer-motion";

interface TextRevealProps {
  text: string;
}

export function SkiperTextReveal({ text }: TextRevealProps) {
  const containerRef = useRef<HTMLDivElement>(null);
  const { scrollYProgress } = useScroll({
    target: containerRef,
    offset: ["start 0.9", "start 0.25"],
  });

  const words = text.split(" ");

  return (
    <div ref={containerRef} className="relative z-10 py-24 md:py-36">
      <div className="mx-auto max-w-5xl px-6">
        <p className="flex flex-wrap text-3xl font-semibold leading-tight tracking-tight sm:text-5xl md:text-6xl text-zinc-800 dark:text-zinc-200">
          {words.map((word, index) => {
            const start = index / words.length;
            const end = start + 1 / words.length;
            return (
              <Word
                key={index}
                progress={scrollYProgress}
                range={[start, end]}
              >
                {word}
              </Word>
            );
          })}
        </p>
      </div>
    </div>
  );
}

function Word({
  children,
  progress,
  range,
}: {
  children: React.ReactNode;
  progress: any;
  range: [number, number];
}) {
  const opacity = useTransform(progress, range, [0.15, 1]);
  const y = useTransform(progress, range, [12, 0]);
  const skewX = useTransform(progress, range, [-3, 0]);

  return (
    <span className="relative mr-3 mt-2 inline-block overflow-hidden">
      <motion.span
        style={{ opacity, y, skewX }}
        className="inline-block transition-colors"
      >
        {children}
      </motion.span>
    </span>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma nova interface e incorporar referências do **Skiper UI**, a IA e o Arquiteto Frontend devem aderir estritamente às seguintes diretrizes no `DESIGN_BLUEPRINT.md`:

1. **Declaração de Pacotes e Instalação Descentralizada**:
   - Especifique componentes sob a taxonomia de registry `@skiper-ui`:
     `Component Registry: npx shadcn@latest add @skiper-ui/skiper26 @skiper-ui/skiper70`
   - Sinalize no Blueprint que os componentes são adicionados diretamente em `@/components/v1/...` e nunca via dependência fechada de NPM.

2. **Atribuição da Hierarquia Visual 60-30-10**:
   - Defina explicitamente no Blueprint qual componente atuará como o **Showstopper (10%)**. Se o *Creative Carousel 001 (skiper50)* for escolhido para a vitrine principal, nenhum outro carrossel ou efeito de canvas expansivo deve ser colocado na mesma viewport.
   - Designe o *SkiperThemeToggle (skiper26)* na camada de **30% de Micro-Interações**, garantindo que as regras CSS da View Transitions API estejam declaradas em `app/globals.css`.

3. **Checklist de Performance & Acessibilidade**:
   - Todo componente derivado do Skiper UI que envolva transformações de `skew`, translações em scroll ou loops de partículas deve obrigatoriamente invocar `useReducedMotion()` do `framer-motion`:
     ```tsx
     const prefersReducedMotion = useReducedMotion();
     // Se true, desabilitar skew e translação, utilizando apenas alternância de opacidade simples
     ```
   - No caso de carrosséis automáticos (*Dia Browser Carousel* ou *Creative Carousel*), declare no Blueprint a inclusão obrigatória de listeners `onMouseEnter` e `onMouseLeave` para pausar o timer e evitar desorientação de usuários navegando via teclado.

4. **Harmonia Tipográfica e Paleta**:
   - O Skiper UI alcança sua excelência visual em combinação com fontes neo-grotescas modernas como **Geist Sans** ou **Inter**, mantendo espaçamento de letras ajustado (`tracking-tight` ou `tracking-[-0.03em]`).
   - Fundos recomendados: preto profundo absoluto (`#000000`) com acentos em ciano elétrico ou azul sky (`#0ea5e9`), preservando o contraste ótico estrito de interfaces de ponta.
