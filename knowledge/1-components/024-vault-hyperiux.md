---
id: "vault-hyperiux"
name: "Hyperiux Vault"
url: "https://vault.hyperiux.com/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Awwwards-Grade Creative Motion", "Dark High-Contrast Aesthetic", "Physics-Driven Fluidity (Lenis + GSAP)", "WebGL Shader Magic & Particle Depth", "Source-First Kinetic Layer"]
densidade_informacao: "Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio a Alto (Lenis Smooth Scroll + GSAP Timelines / Three.js Shaders)"
stack_frameworks: ["React 19 / 18", "Next.js (App Router)", "GSAP / ScrollTrigger / Flip", "Lenis (@studio-freight/lenis / lenis)", "Motion (Framer Motion)", "Three.js / React Three Fiber", "Tailwind CSS", "TypeScript"]
compatibilidade:
  fontes_ideais: ["Syne", "Clash Display", "Geist Sans", "PP Neue Montreal", "Avenir", "Space Grotesk", "JetBrains Mono"]
  paletas_ideais: ["Deep Void Dark (#111111 / #0a0a0a)", "Hyper Vivid Electric Tangerine (#FF6B00 / #FFB27A)", "Pure High-Contrast Monochrome (#FFFFFF / #000000)", "Muted Industrial Slate & Alpha Wireframes (white/8, white/12)"]
  combinacoes_recomendadas: ["Shadcn UI (primitivas estruturais)", "Motion Primitives", "Radix UI Primitives", "Lucide React", "Lenis Scroll"]
  conflitos_esteticos: ["Corporate Memphis com ilustrações 2D pastéis", "Neumorfismo plástico cinza-claro de baixo contraste", "Transições lineares duras de CSS sem amortecimento inercial", "Dashboards corporativos ultra-densos sem respiro tipográfico"]
---

# Hyperiux Vault — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo estúdio criativo **Hyperiux** (Hyperiux Immersion Labs, com sede em Noida, Índia), o **Hyperiux Vault** (`vault.hyperiux.com`) foi concebido para preencher uma lacuna crítica no desenvolvimento frontend moderno sob o lema: *"The Interaction Layer Your Website Is Missing"*.

Enquanto bibliotecas tradicionais como Shadcn UI, Radix ou Tailwind UI resolvem a geometria estática da interface (botões, modais, formulários, tabelas e grids), o Hyperiux Vault foca exclusivamente na **dimensão temporal da experiência**: como cada nó da árvore DOM entra em cena, reage à velocidade inercial de scroll do usuário, deforma o espaço vetorial com o cursor do mouse e transiciona entre rotas de forma cinematográfica com o acabamento de estúdios vencedores do *Awwwards Site of the Year*, *FWA* e *CSS Design Awards*.

### Pilares da Assinatura Visual do Hyperiux Vault:

1. **Separação Explícita entre Estrutura de UI e Camada Cinética (Interaction-First)**:
   A tese do Vault é que você não deve substituir sua biblioteca de UI favorita por componentes engessados de animação. Mantenha seu design system de base intacto. O Vault atua como uma película invisível de alta sensibilidade tátil sobreposta à sua interface, orquestrando trajetórias espaciais, distorções de lente, revelações de texto por máscara e paralaxes desacoplados.

2. **Arquitetura Multi-Engine com Dependências Escopadas (Scoped Peer Engines)**:
   Diferente de pacotes monolíticos pesados que injetam centenas de kilobytes de WebGL desnecessariamente em páginas simples, o Vault adota um modelo de dependência sob demanda:
   - **Lenis**: Fornece a fundação inercial de rolagem sem atrito (*buttery smooth scroll*), padronizando a velocidade de scroll entre mouses de roda mecânica, trackpads de precisão e telas sensíveis ao toque.
   - **GSAP & ScrollTrigger / Flip**: Assume o controle de timelines determinísticas complexas, pinning de seções, transformações tridimensionais scrubbadas por scroll e recomposição de layouts morfológicos.
   - **Framer Motion (Motion)**: Rege transições declarativas de estado em componentes de interface, microinterações de clique/hover e manipulação de layout animado (`layoutId`, `AnimatePresence`).
   - **Three.js & React Three Fiber (R3F) / Shaders GLSL**: Reservado estritamente para experiências com profundidade volumétrica, renderização em canvas, dither procedural, aberração cromática e partículas magnéticas.

3. **Filosofia Source-First & CLI Autônomo**:
   O código não é distribuído através de um módulo fechado em `node_modules` que engessa tokens e classes. Usando a CLI `npx hyperiux add <effect>`, o código-fonte puro em TypeScript e Tailwind CSS é injetado diretamente em seu repositório local (geralmente sob `components/effects/` ou `components/vault/`). O desenvolvedor detém 100% de controle sobre curvas de aceleração, interpolações, cores e lógica de desmontagem (*cleanup*).

4. **Hardware-Aware Performance Gate & Detecção de GPU de Software**:
   O Vault implementa uma rotina interna de intro-gate que analisa o renderizador WebGL (`WEBGL_debug_renderer_info`). Caso o dispositivo esteja executando rasterização por software (ex: *SwiftShader*, *llvmpipe* em ambientes virtuais ou máquinas modestas) ou caso detecte bots de auditoria do Google Lighthouse/Headless Chrome, os shaders de alto custo e loops de RAF intensos são silenciados automaticamente, trocados por fallbacks leves de CSS. Isso preserva pontuações 95+ de Core Web Vitals (LCP, CLS, INP).

5. **Design Tátil "Dark Craft" & Micro-Feedback Sonoro**:
   A estética base do ecossistema aposta no contraste rigoroso: superfícies pretas puras (`#111111` ou `#0a0a0a`), tipografia agressiva com cortes geométricos (Syne, Clash Display, Geist), acentos fluorescentes (*Electric Tangerine* `#FF6B00`, *Glint Gold* `#FFB27A`), bordas ultrafinas de baixa opacidade (`border-white/8`), e suporte nativo a tags de áudio tátil (`data-sound-kind="primary"`), conferindo uma sensação física de console industrial de luxo.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários

1. **Sites Institucionais e Landing Pages de Estúdios de Design e Agências Criativas**:
   Onde a meta principal é demonstrar excelência técnica, sensibilidade tipográfica e distinção artística imediata para clientes corporativos de alto padrão.
2. **Flagships de Hardware Premium, Moda de Luxo & Automotivo**:
   Produtos que dependem de narrativas imersivas orientadas a scroll (*scrollytelling*), com zoom sliders, máscaras de corte, cards de profundidade e transições de página que emulam câmeras de cinema.
3. **Startups de Inteligência Artificial e Ferramentas para Desenvolvedores de Vanguarda**:
   Empresas que competem no segmento de ponta (como Runway, Linear, Midjourney, Vercel) e necessitam que suas páginas de conversão e waitlists transmitam futurismo, precisão mecânica e alto polimento de software.
4. **Portfólios Pessoais de Design Engineers e Creative Developers**:
   Candidaturas técnicas e mostruários individuais que buscam selos Awwwards ou vagas em laboratórios de inovação digital e creative tech.

### Papel no Ritmo Visual (Regra 60-30-10)

- **60% — Fundação Estrutural Estática e Acessível (UI Primitives)**:
  Primitivas limpas de interface (botões normais, cards de conteúdo, grids tipográficos legíveis, inputs de formulário) usando Shadcn UI / Radix com Tailwind CSS. Paleta monocromática escura, espaçamentos generosos e legibilidade primária preservada.
- **30% — Camada de Fluidez e Conexão Cinética (Vault Transitions & Micro-Motion)**:
  - Integração global do **Lenis** para scroll inercial suave.
  - Botões com efeito de caracteres intercalados (**Char Stagger Button**) no lugar de botões inertes.
  - Menus e barras de navegação flutuantes com animação de expansão e deslocamento (**Displacement Navbar**).
  - Revelação de cabeçalhos e títulos com máscaras dinâmicas (**Mask Text Reveal**).
- **10% — Efeitos Protagonistas / Showstoppers (Visual Anchors)**:
  - Fundo Hero com **Dither Canvas** ou partículas interativas (**Spider Particles**).
  - Apresentação de cases ou produtos com **Arc Flow Carousel** ou **Portal Carousel**.
  - Transição de rota de tela cheia com **Chess Grid Transition** ou **Aperture Transition**.
  - Efeito de rastro sob o cursor na seção de galeria de imagens (**Phantom Image Trail**).

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

- **Sistemas de Informação Crítica, Dashboards ERP e Terminais Financeiros**:
  Em telas de alta densidade de informação onde o usuário precisa ler tabelas de 50 linhas, preencher formulários fiscais ou operar trades com milissegundos de latência, qualquer atraso inercial no scroll (Lenis) ou efeito de rastro de cursor é uma barreira cognitiva agressiva e hostil.
- **Portais Governamentais e Serviços Públicos de Acessibilidade Estrita (WCAG AAA)**:
  Transições com cortes geométricos cegantes, distorções de lente WebGL e textos mascarados violam critérios essenciais de acessibilidade para usuários com deficiência visual, déficits cognitivos ou distúrbios vestibulares.
- **Aplicações Web Mobile Puras com Restrição Severa de Bateria e CPU Fraca**:
  Nunca inicialize múltiplos renderizadores Three.js / Canvas simultâneos em páginas mobile de entrada. O consumo acelerado de GPU causará perda dramática de taxa de quadros (quedas para 15-20 FPS) e superaquecimento do aparelho.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):

- **Acúmulo Tóxico de Efeitos Concorrentes**:
  Inserir em uma única dobra visual: um background com shader GLSL líquido + rastro de borboletas no cursor (`butterfly-trail-cursor`) + título com texto cromático piscante (`chromatic-text`) + botão pulsante metálico. O resultado deixa de ser sofisticado e passa a parecer um protótipo sobrecarregado sem direção de arte ("efeito circo").
- **Sequestro de Scroll sem Fallback Tátil (Scroll-Jacking Destrutivo)**:
  Configurar o Lenis ou timelines do GSAP com valores de inércia excessivamente longos (`duration: 2.5s` ou `lerp: 0.02`), fazendo com que a página pareça estar "afundando em óleo mineral", impedindo o usuário de alcançar o conteúdo desejado com rapidez.
- **Ignorar a Preferência de Movimento Reduzido (`prefers-reduced-motion: reduce`)**:
  Deixar de encapsular animações de escala, rotação e deslocamento em verificações de acessibilidade. Todo efeito do Vault deve desativar interpolações espaciais e limitar-se a crossfades simples de opacidade quando a flag de movimento reduzido estiver habilitada no sistema operacional.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão 12 dos componentes e categorias de efeitos mais emblemáticos do catálogo do **Hyperiux Vault**, selecionados por sua relevância técnica, apelo estético e capacidade de elevar interfaces a nível internacional:

---

### 1. Phantom Image Trail (`/effects/cursor-effects/phantom-image-trail`)
- **Anatomia Visual**: Enquanto o usuário move o ponteiro do mouse sobre uma zona interativa (ou pela tela inteira), uma sequência coreografada de imagens de alta resolução surge na posição exata do cursor e se desfaz em uma esteira inercial suave. Cada imagem sofre uma rotação angular sutil baseada no vetor de velocidade do mouse e desaparece com fade-out gradual e leve escala.
- **Gatilho de Interação**: Evento `pointermove` contínuo ponderado por limiar de distância euclidiana (delta > 40px) para não disparar renderizações redundantes no mesmo pixel.
- **Onde encaixar na página**: Seção de portfólio criativo, listagem de cases de sucesso em agências, galeria de produtos de moda ou catálogo de arquitetura.

---

### 2. Arc Flow Carousel (`/effects/carousels/arc-flow-carousel`)
- **Anatomia Visual**: Um slider tridimensional curvilíneo onde os cartões orbitam ao longo de um arco elíptico espacial (`perspective: 1200px`). Os cards fora de foco sofrem rotação tridimensional no eixo Y, redução de escala progressiva e desfoque óptico gradual, mantendo o card centralizado perfeitamente ortogonal ao observador.
- **Gatilho de Interação**: Drag/Swipe com inércia, clique nas laterais ou scroll wheel sincronizado com o eixo do carrossel.
- **Onde encaixar na página**: Hero de produtos de hardware, vitrine de recursos de planos ou showcase de depoimentos de alto impacto.

---

### 3. Mask Text Reveal (`/effects/text-animations/mask-text-reveal`)
- **Anatomia Visual**: O texto é particionado em linhas e palavras encapsuladas dentro de contêineres com `overflow: hidden`. As palavras deslizam verticalmente a partir do fundo da linha (`translateY(110%)` para `translateY(0%)`), combinando rotação sutil em X (cerca de 5 a 10 graus) com interpolação `power3.out`. Revela a mensagem sem esticar fontes nem causar reflow de texto.
- **Gatilho de Interação**: Ativado via GSAP ScrollTrigger na entrada do viewport (`start: "top 80%"`) ou logo após o encerramento do loader inicial da página.
- **Onde encaixar na página**: Títulos de grande porte (H1 do Hero), declarações de manifesto da marca ou números chave de estatísticas institucionais.

---

### 4. Dither Canvas (`/effects/backgrounds/dither-canvas`)
- **Anatomia Visual**: Fundo gerado proceduralmente via WebGL / Fragment Shader que aplica um algoritmo de meio-tom e dither matricial clássico (Bayer matrix 4x4 ou 8x8) sobre gradientes dinâmicos de cor. O visual evoca interfaces analógicas dos anos 80 e design paramétrico japonês de vanguarda, com textura granular viva que se move sutilmente em tempo real.
- **Gatilho de Interação**: Loop contínuo em RequestAnimationFrame desacoplado, modulado suavemente pela posição normalizada do mouse (`u_mouse`).
- **Onde encaixar na página**: Fundo heroico do topo da página (Hero section) ou backdrop de seções técnicas de terminal e documentação.

---

### 5. Cards Runway & Scroll Stack (`/effects/scroll-effects/cards-runway`)
- **Anatomia Visual**: Uma série de cartões empilhados verticalmente que, conforme a página é rolada, sofrem um travamento temporário (*sticky pin*). O cartão que está abaixo sobe e sobrepõe suavemente o cartão anterior, enquanto o cartão superior sofre leve redução de escala (`scale(0.95)`), escurecimento progressivo de luminosidade (`brightness(0.6)`) e acúmulo de sombra profunda, criando a ilusão tátil de um baralho sendo folheado em mesa.
- **Gatilho de Interação**: GSAP ScrollTrigger com `scrub: 1` ou `scrub: 0.5`, atrelado diretamente ao progresso percentual da rolagem do contêiner pai.
- **Onde encaixar na página**: Seção de "Pilares do Produto", apresentação de 3 a 5 funcionalidades principais de uma suíte ou estudos de caso detalhados.

---

### 6. Chess Grid Transition (`/effects/page-transitions/chess-grid-transition`)
- **Anatomia Visual**: Ao disparar a navegação entre páginas no Next.js App Router, a viewport inteira é coberta por uma malha quadriculada invisível (ex: 8x6 blocos pretos). Os quadrados escalam individualmente de 0 a 1 em uma sequência ondulatória escalonada (*stagger* multidirecional em xadrez), bloqueando o conteúdo antigo, aguardando o carregamento da nova rota e revertendo a animação para revelar a nova página.
- **Gatilho de Interação**: Disparado interceptando o clique em links de navegação (`next/link` com wrapper de transição) ou chamada programática do roteador.
- **Onde encaixar na página**: Transição global entre rotas de nível superior (ex: Home → Works → About → Contact).

---

### 7. Char Stagger Button (`/effects/buttons/char-stagger-button`)
- **Anatomia Visual**: Botão de comando com acabamento refinado. O texto do rótulo é dividido em dois clones idênticos empilhados verticalmente dentro de uma máscara restrita. No estado de repouso, o texto inferior fica oculto. Ao passar o mouse, cada caractere do texto original sobe deslizando para fora enquanto os caracteres da réplica inferior sobem tomando seu lugar com um leve atraso sequencial (*stagger: 0.015s*). Acompanhado por um microícone com rotação sincronizada de 180° ou 90°.
- **Gatilho de Interação**: Eventos `mouseenter` e `mouseleave`.
- **Onde encaixar na página**: Call-To-Action (CTA) principal do Hero, botão de contratação/compra e links primários da barra de navegação.

---

### 8. Liquid Glass Cursor (`/effects/cursor-effects/liquid-glass-cursor`)
- **Anatomia Visual**: O ponteiro padrão do sistema é substituído por uma esfera de vidro líquido flutuante. O elemento aplica um desfoque de fundo refrativo (`backdrop-filter: blur(12px)` com máscara circular e borda iluminada de 1px em gradiente linear). Ao passar por cima de textos ou imagens, o cursor expande seu raio e aplica um filtro SVG de distorção orgânica de turbulência (`feDisplacementMap`), simulando uma gota d'água deslizando sobre uma tela táctil.
- **Gatilho de Interação**: Movimento do mouse interpolado via Spring Physics (`stiffness: 400`, `damping: 28`) para criar arrasto físico natural.
- **Onde encaixar na página**: Portfólios de arte e fotografia, landing pages de estúdios criativos e interfaces de produtos digitais imersivos.

---

### 9. Circular Split Roll (`/effects/scroll-effects/circular-split-roll`)
- **Anatomia Visual**: Um bloco de texto monumental (geralmente uma frase-chave ou slogan) é dividido em duas metades horizontais ou seccionado ao longo de um raio circular. Conforme o usuário rola a tela para baixo, as duas metades giram em direções opostas enquanto se aproximam do centro, travando na posição legível perfeitamente alinhada antes de liberarem a continuidade do scroll.
- **Gatilho de Interação**: GSAP ScrollTrigger com scrub contínuo ligado ao deslocamento vertical do contêiner.
- **Onde encaixar na página**: Transição entre a seção Hero e a seção de Funcionalidades, ou fechamento de página antes do Footer.

---

### 10. Displacement Navbar (`/effects/navigation/displacement-navbar`)
- **Anatomia Visual**: Uma barra de navegação flutuante semi-transparente ancorada no topo da tela com cantos arredondados contínuos. Quando a página inicia, ela surge a partir de um estado comprimido; à medida que o usuário rola, ela contrai dinamicamente sua largura, oculta rótulos de texto secundários deixando apenas ícones geométricos essenciais, e intensifica o desfoque de fundo (`backdrop-blur-xl`), mantendo a hierarquia intacta sem bloquear a leitura.
- **Gatilho de Interação**: Scroll listener passivo baseado em limiares de deslocamento (`scrollY > 80px`).
- **Onde encaixar na página**: Cabeçalho global do site / Header persistente de aplicações desktop e tablets.

---

### 11. Fractal Glass / 3D WebGL Portfolio Slider (`/effects/webgl-effects/fractal-glass`)
- **Anatomia Visual**: Slider de projetos onde a troca entre os slides não ocorre por um simples deslize mecânico lateral. Em vez disso, a imagem em exibição é refratada através de um plano tridimensional em WebGL com efeito de vidro facetado (vidro prismático). Conforme o slide se move, reflexos de luz especular e divisões cromáticas de arco-íris se propagam pela imagem antes de assentarem na textura seguinte.
- **Gatilho de Interação**: Drag do mouse / trackpad com cálculo de aceleração e inércia repassada como uniformes de velocidade ao shader GLSL (`u_velocity`, `u_progress`).
- **Onde encaixar na página**: Slider de projetos em destaque, lookbook de marcas de alta costura ou galeria de arte digital 3D.

---

### 12. Draggable Marquee (`/effects/components/draggable-marquee`)
- **Anatomia Visual**: Uma fita contínua de tipografia ou logomarcas em movimento infinito. Diferente de marquees convencionais em puro CSS que ignoram a interação do usuário, este componente roda em velocidade constante, mas permite que o usuário o arraste para frente ou para trás com o ponteiro do mouse, respondendo à inércia de soltura e acelerando organicamente na direção do scroll da página.
- **Gatilho de Interação**: Auto-play contínuo via RAF combinado com eventos de drag (`pointerdown`, `pointermove`, `pointerup`) e multiplicador de velocidade atrelado à velocidade instantânea do scroll (`lenis.velocity`).
- **Onde encaixar na página**: Seção de prova social com logos de clientes parceiros, fita de novidades do produto ou rodapé de impacto.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup Base

Para utilizar o ecossistema do Hyperiux Vault em um projeto Next.js (App Router), instale as bibliotecas base correspondentes ao conjunto de efeitos que você deseja utilizar:

```bash
# 1. Dependências essenciais de animação e utilitários
npm install gsap @studio-freight/lenis clsx tailwind-merge lucide-react

# 2. Se utilizar componentes declarativos do ecossistema Motion
npm install motion

# 3. Se utilizar os componentes 3D / Shaders do Vault
npm install three @types/three @react-three/fiber @react-three/drei
```

### Inicialização e Uso da CLI do Hyperiux Vault

```bash
# Inicializa as configurações do Vault no seu projeto (cria vault.json e helpers)
npx hyperiux init

# Autenticação (gratuita para Core, ou com chave de licença Pro)
npx hyperiux login

# Adiciona o componente fonte desejado diretamente na pasta components/effects/
npx hyperiux add phantom-image-trail
npx hyperiux add char-stagger-button
npx hyperiux add mask-text-reveal
```

---

### Física de Movimento, Curvas Easing & Parâmetros Recomendados

Para manter a assinatura tátil de estúdios como Hyperiux, as animações nunca devem usar interpolações genéricas como `linear` ou `ease`. Utilize as curvas matemáticas de inércia e molas testadas em produção:

| Engine | Efeito / Aplicação | Parâmetros de Física / Curva | Sensação Visual |
| :--- | :--- | :--- | :--- |
| **Lenis** | Rolagem Global | `lerp: 0.1, duration: 1.2, smoothWheel: true` | Deslizamento inercial macio sem atraso no clique |
| **GSAP** | Máscaras de Texto (`Mask Text`) | `ease: "power4.out", duration: 1.1, stagger: 0.03` | Arrancada rápida com desaceleração precisa de luxo |
| **GSAP** | Carrossel 3D / Pinning | `ease: "expo.out", duration: 1.4` | Sensação de maquinário pesado e sofisticado |
| **Motion** | Cursor Líquido / Rastro | `type: "spring", stiffness: 350, damping: 25, mass: 0.5` | Fluidez tátil orgânica, sem rebote excessivo |
| **Motion** | Botões e Toggles | `type: "spring", stiffness: 500, damping: 30` | Resposta mecânica imediata ao clique do mouse |

---

### Receita de Código Funcional e Completo: Sistema Lenis + Char Stagger Button + Mask Reveal

Abaixo está uma implementação realista em nível de produção contendo o Provedor Global de Scroll Suave do Lenis, o Botão com Rótulo Staggered de Caracteres e a Revelação Tipográfica por Máscara.

#### 1. Provedor de Rolagem Inercial Lenis (`components/providers/lenis-provider.tsx`)

```tsx
"use client";

import React, { createContext, useContext, useEffect, useRef } from "react";
import Lenis from "lenis";

interface LenisContextValue {
  lenis: Lenis | null;
}

const LenisContext = createContext<LenisContextValue>({ lenis: null });

export const useLenis = () => useContext(LenisContext);

interface LenisProviderProps {
  children: React.ReactNode;
}

export function LenisProvider({ children }: LenisProviderProps) {
  const lenisRef = useRef<Lenis | null>(null);

  useEffect(() => {
    // Respeita acessibilidade de usuários com preferência de movimento reduzido
    const prefersReducedMotion = window.matchMedia("(prefers-reduced-motion: reduce)").matches;
    if (prefersReducedMotion) return;

    const lenis = new Lenis({
      duration: 1.2,
      easing: (t) => Math.min(1, 1.001 - Math.pow(2, -10 * t)), // Curva expo out nativa
      orientation: "vertical",
      gestureOrientation: "vertical",
      smoothWheel: true,
      wheelMultiplier: 1.0,
      touchMultiplier: 1.5,
    });

    lenisRef.current = lenis;

    function raf(time: number) {
      lenis.raf(time);
      requestAnimationFrame(raf);
    }

    const rafId = requestAnimationFrame(raf);

    return () => {
      cancelAnimationFrame(rafId);
      lenis.destroy();
      lenisRef.current = null;
    };
  }, []);

  return (
    <LenisContext.Provider value={{ lenis: lenisRef.current }}>
      {children}
    </LenisContext.Provider>
  );
}
```

#### 2. Botão com Caracteres Intercalados (`components/effects/char-stagger-button.tsx`)

```tsx
"use client";

import React from "react";
import { ArrowUpRight } from "lucide-react";
import { cn } from "@/lib/utils";

interface CharStaggerButtonProps extends React.ButtonHTMLAttributes<HTMLButtonElement> {
  label: string;
  variant?: "primary" | "outline";
}

export function CharStaggerButton({
  label,
  variant = "primary",
  className,
  ...props
}: CharStaggerButtonProps) {
  const characters = label.split("");

  return (
    <button
      data-sound-kind="primary"
      className={cn(
        "group relative inline-flex items-center gap-3 overflow-hidden px-6 py-3.5 text-sm font-medium tracking-wide uppercase transition-colors duration-300 focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-primary",
        variant === "primary"
          ? "bg-[#FF6B00] text-black hover:bg-[#FF8533]"
          : "border border-white/15 bg-black/40 text-white backdrop-blur-md hover:border-white/40",
        className
      )}
      {...props}
    >
      {/* Marcador geométrico característico do Hyperiux */}
      <span className="h-1.5 w-1.5 bg-current transition-transform duration-300 group-hover:rotate-90 group-hover:scale-125" />

      {/* Container de tipografia com máscara de transbordamento */}
      <span className="relative inline-block overflow-hidden leading-none">
        {/* Rótulo superior que sobe */}
        <span className="inline-flex">
          {characters.map((char, index) => (
            <span
              key={`top-${index}`}
              className="inline-block transition-transform duration-300 ease-[cubic-bezier(0.16,1,0.3,1)] motion-reduce:transition-none group-hover:-translate-y-full"
              style={{
                transitionDelay: `${index * 15}ms`,
              }}
            >
              {char === " " ? "\u00A0" : char}
            </span>
          ))}
        </span>

        {/* Rótulo inferior que surge da base */}
        <span className="absolute inset-0 inline-flex">
          {characters.map((char, index) => (
            <span
              key={`bot-${index}`}
              className="inline-block translate-y-full transition-transform duration-300 ease-[cubic-bezier(0.16,1,0.3,1)] motion-reduce:transition-none group-hover:translate-y-0"
              style={{
                transitionDelay: `${index * 15}ms`,
              }}
            >
              {char === " " ? "\u00A0" : char}
            </span>
          ))}
        </span>
      </span>

      {/* Ícone de seta com projeção espacial no hover */}
      <div className="relative size-4 overflow-hidden">
        <ArrowUpRight className="size-4 transition-transform duration-300 ease-[cubic-bezier(0.16,1,0.3,1)] group-hover:translate-x-4 group-hover:-translate-y-4" />
        <ArrowUpRight className="absolute inset-0 size-4 -translate-x-4 translate-y-4 transition-transform duration-300 ease-[cubic-bezier(0.16,1,0.3,1)] group-hover:translate-x-0 group-hover:translate-y-0" />
      </div>
    </button>
  );
}
```

#### 3. Título com Revelação por Máscara GSAP (`components/effects/mask-text-reveal.tsx`)

```tsx
"use client";

import React, { useEffect, useRef } from "react";
import gsap from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { cn } from "@/lib/utils";

if (typeof window !== "undefined") {
  gsap.registerPlugin(ScrollTrigger);
}

interface MaskTextRevealProps {
  lines: string[];
  className?: string;
  triggerOnScroll?: boolean;
}

export function MaskTextReveal({
  lines,
  className,
  triggerOnScroll = true,
}: MaskTextRevealProps) {
  const containerRef = useRef<HTMLHeadingElement | null>(null);

  useEffect(() => {
    if (!containerRef.current) return;

    // Respeita preferência de acessibilidade
    const prefersReducedMotion = window.matchMedia("(prefers-reduced-motion: reduce)").matches;
    if (prefersReducedMotion) return;

    const words = containerRef.current.querySelectorAll(".hx-reveal-word");

    if (triggerOnScroll) {
      gsap.fromTo(
        words,
        {
          yPercent: 120,
          rotateX: 12,
          opacity: 0,
        },
        {
          yPercent: 0,
          rotateX: 0,
          opacity: 1,
          duration: 1.1,
          ease: "power4.out",
          stagger: 0.04,
          scrollTrigger: {
            trigger: containerRef.current,
            start: "top 85%",
            toggleActions: "play none none none",
          },
        }
      );
    } else {
      gsap.fromTo(
        words,
        { yPercent: 120, rotateX: 12, opacity: 0 },
        {
          yPercent: 0,
          rotateX: 0,
          opacity: 1,
          duration: 1.1,
          ease: "power4.out",
          stagger: 0.04,
          delay: 0.2,
        }
      );
    }

    return () => {
      ScrollTrigger.getAll().forEach((trigger) => trigger.kill());
    };
  }, [triggerOnScroll]);

  return (
    <h2
      ref={containerRef}
      className={cn("text-3xl font-semibold tracking-tight text-white md:text-6xl", className)}
    >
      {lines.map((line, lineIndex) => (
        <span key={lineIndex} className="block overflow-hidden py-1">
          {line.split(" ").map((word, wordIndex) => (
            <span
              key={wordIndex}
              className="hx-reveal-word inline-block will-change-transform mr-[0.25em]"
            >
              {word}
            </span>
          ))}
        </span>
      ))}
    </h2>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar o **Hyperiux Vault** como referência para o Blueprint de um novo projeto, a IA deve obedecer às seguintes regras de arquitetura:

1. **Separação Obrigatória entre Primitivas de UI e Camada de Efeitos**:
   - Nunca use o Vault para substituir primitivas funcionais de formulário ou tabelas. Declare o **Shadcn UI** como a base de componentes (`60%`) e declare o **Hyperiux Vault** estritamente como a **Camada de Interação & Transições** (`30%` a `10%`).
2. **Definição Clara da Stack de Animação no Blueprint**:
   - Ao adotar o Vault, declare explicitamente no blueprint quais engines serão autorizadas:
     - Para Landing Pages e Portfólios: Ativar `Lenis` (scroll) + `GSAP ScrollTrigger` + `Framer Motion`.
     - Para WebGL/3D: Adicionar `Three.js` e `@react-three/fiber` somente se houver um caso de uso explícito (ex: `DitherCanvas`, `FractalGlass`).
3. **Orçamento Rigoroso de Performance (Performance Budgeting)**:
   - Limite a no máximo **1 efeito WebGL contínuo** por viewport.
   - Proíba o uso de múltiplos rastros de cursor (`phantom-image-trail`, `liquid-glass-cursor`) ativados simultaneamente.
   - Exija verificação sistemática de `prefers-reduced-motion` em qualquer componente instalado via Vault.
4. **Paleta e Tokens Visuais Recomendados no Tailwind**:
   - Fundo Primário: `#111111` ou `#0a0a0a` (preto profundo fosco).
   - Acento Principal: `#FF6B00` (Electric Tangerine) e secundário `#FFB27A`.
   - Superfície de Cartões: `bg-white/[0.03]` com bordas `border-white/10` e desfoque `backdrop-blur-md`.
   - Tipografia de Display: Fontes geométricas brutas de alto impacto como `Syne`, `Clash Display` ou `Geist Sans`.
