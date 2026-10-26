---
id: "framer-components"
name: "Framer Marketplace Components"
url: "https://www.framer.com/marketplace/components"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["High-End Motion Craft", "Micro-Interaction Polish", "Kinetic Typography", "WebGL & Canvas Shaders", "Inertial Spring Physics", "Canvas-to-Code Bridge"]
densidade_informacao: "Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Framer Motion/JS) a Alto (Canvas/3D/GLSL)"
stack_frameworks: ["React 18 / 19", "Framer Motion (motion/react)", "TypeScript", "Tailwind CSS v4", "Three.js / React Three Fiber", "GLSL / Canvas 2D", "Lucide React"]
compatibilidade:
  fontes_ideais: ["Inter", "Geist Sans", "Instrument Serif", "Clash Display", "Satoshi", "PP Neue Montreal", "Syne"]
  paletas_ideais: ["Obsidian High-Contrast", "Deep Zinc with Neon Accent", "Atmospheric Glassmorphism & Aurora Blurs", "Minimalist Monochromatic Luxury"]
  combinacoes_recomendadas: ["Shadcn UI", "Magic UI", "Aceternity UI", "Motion Primitives", "Kibo UI", "Tailwind CSS v4"]
  conflitos_esteticos: ["Brutalismo Y2K sem easing", "Flat Design 1.0 estático sem resposta háptica", "Skeuomorfismo pesado desprovido de física inercial"]
---

# Framer Marketplace Components — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Framer Marketplace Components** (`https://www.framer.com/marketplace/components`) representa o ponto de convergência definitivo entre o design visual espacial e a engenharia de animação reativa em React. Originalmente concebido como uma ferramenta de prototipagem em código (Framer Classic / Framer X), o Framer evoluiu para uma plataforma de publicação web completa onde os **Code Components** operam como blocos de construção de alto calibre técnico.

Diferente de repositórios de UI puramente visuais (como templates estáticos de Figma ou bibliotecas de CSS utilitário rígidas), os componentes do ecossistema Framer Marketplace possuem uma identidade forjada na interseção entre **física inercial (Spring Physics)**, **manipulação direta de estado visual** e **computação gráfica de baixa latência**.

### A Assinatura Estética: "The Framer Motion Polish"
A estética consagrada pelos melhores criadores do Framer Marketplace define o padrão da web moderna de alta conversão (utilizada por líderes como Vercel, Linear, Raycast, Stripe e agências de design como Studio Freight e Antinomy):

1. **Física Inercial Natural (Zero Easing Linear Rígido)**:
   Nenhum componente do ecossistema Framer se move com curvas de transição mecânicas (`linear` ou transições CSS padrão de 0.2s). O movimento é governado por molas físicas parametrizadas com **stiffness** (rigidez), **damping** (amortecimento) e **mass** (massa), gerando aceleração instantânea com desaceleração amortecida e continuidade de momento (momentum preservation).
2. **Superfícies Atmosféricas e Refrações Ópticas**:
   Uso intensivo de gradientes cônicos, iluminação perimetral de 1px com degradê atenuado (`border: 1px solid rgba(255,255,255,0.08)`), overlays de ruído orgânico (SVG noise texturizado) e desfoques Gaussianos com aceleração de hardware (`backdrop-filter: blur(20px)`).
3. **Fluidez Contínua de Layout (`layoutId` Morphing)**:
   Transições entre estados de componentes — abas ativas, botões colapsáveis, cards expansíveis em modal — não utilizam cortes bruscos. O motor computa o `boundingClientRect` inicial e final através da matemática de FLIP (First, Last, Invert, Play) do Framer Motion, interpolando geometrias, raios de curvatura e opacidades sem deformação visual.
4. **Arquitetura Híbrida: Código TypeScript Exposto via Property Controls**:
   O grande diferencial técnico é a ponte entre o canvas do designer e o código TypeScript: a função `addPropertyControls` com enumerações tipadas `ControlType` permite que programadores construam micro-aplicações complexas (visualizadores de áudio, shaders Three.js, cursores magnéticos, tickers infinitos) enquanto designers ajustam cores, velocidades, gaps e textos via sidebar nativa com visualização em tempo real a 60-120fps.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados
1. **Landing Pages de Alto Impacto para SaaS de IA & DevTools**:
   Onde a percepção de valor e sofisticação técnica do produto é julgada nos primeiros 3 segundos da Hero section (ex: carrosséis de dados volumétricos, bento grids com iluminação dinâmica, botões magnéticos com efeito glow).
2. **Websites Institucionais de Agências Digitais & Estúdios Criativos**:
   Portfólios que necessitam demonstrar maestria visual e tipográfica através de transições de página inerciais, rolagem suave com paralaxe, cursores interativos que reagem a elementos clicáveis e tipografia cinética.
3. **Páginas de Lançamento de Hardware & Produtos Premium (DTC/Luxury)**:
   Apresentação de produtos físicos onde modelos interativos 3D, visualizadores em 360 graus, carrosséis de especificações com profundidade cilíndrica e transições de lente fotográfica traduzem exclusividade.
4. **Fintechs & Bancos Digitais Modernos**:
   Exibição interativa de cartões virtuais com brilho holográfico no hover, simulações de investimento com contadores animados de alta precisão e cards de segurança com shaders de distorção de onda.

### Papel no Ritmo Visual (A Aplicação Rigorosa da Regra 60-30-10)

```
┌─────────────────────────────────────────────────────────────┐
│ 60% — Fundação Estrutural Estática (Shadcn / Tailwind)      │
│  Superfícies neutras, tipografia de leitura, layout grid    │
├─────────────────────────────────────────────────────────────┤
│ 30% — Fluidez & Navegação Interativa (Framer Motion)        │
│  Tabs com pill deslizante (layoutId), accordions elásticos,  │
│  headers retráteis com blur, dropdowns de mola suave         │
├─────────────────────────────────────────────────────────────┤
│ 10% — Showstoppers Protagonistas do Framer Marketplace      │
│  3D perspective carousels, text scramble, magnetic cursor,  │
│  liquid canvas shaders, infinite tickers com pause on hover │
└─────────────────────────────────────────────────────────────┘
```

- **60% — Espinha Dorsal (Base Estática / NÃO usar componentes Framer pesados aqui)**:
  A estrutura de containers, grids de página, fundos neutros (`#09090b` ou `#000000`), tabelas e blocos de texto corrido deve permanecer governada por Tailwind CSS sem sobrecarga de instâncias de motion.
- **30% — Camada de Navegação & Micro-interações do Sistema**:
  Componentes de controle funcional que demandam resposta háptica: tabs com sublinhado magnético (`layoutId`), acordions com interpolação de altura sem salto, barras de navegação flutuantes com efeito "Dynamic Island".
- **10% — Showstoppers Protagonistas (A especialidade do Framer Marketplace)**:
  O elemento focal que converte o visitante: a animação 3D de perspectiva no Hero, o carrossel de depoimentos cilíndrico, o efeito de texto scramble criptográfico no título principal ou o background de shader GLSL interativo ao movimento do mouse.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Painéis Administrativos Densos, ERPs & Backoffices Operacionais**:
  Telas que exibem 1.000 linhas de tabela de banco de dados ou grids contábeis não podem ter componentes com ouvintes de mouse contínuos, spring transitions em cada célula ou efeitos de blur reflexivos. Isso gera degradação do frame rate (jank) e cansaço visual.
- **Aplicações de Alta Frequência de Leitura ou Texto Técnico (Documentações)**:
  Documentações técnicas (como GitBook, Mintlify ou Readme) exigem clareza absoluta e renderização de texto instantânea. Textos com efeito scramble ou reveals por caractere atrapalham a produtividade do leitor.
- **Dispositivos de Baixa Potência, Ambientes Móveis com Restrição de Bateria ou E-readers**:
  Shaders de fragmento WebGL ou múltiplos listeners `requestAnimationFrame` drenam a bateria rapidamente e elevam a temperatura em dispositivos móveis modestos.
- **Fluxos Transacionais Críticos & Checkout**:
  Em etapas de pagamento, formulários de cartão de crédito e confirmação de compra, micro-animações lentas ou botões elásticos que se movem quando o usuário tenta clicar geram frustração imediata e aumentam a taxa de abandono de carrinho.

### ⚠️ A Síndrome do "Framer Slop" & Erros Críticos de Exagero

O fácil acesso a dezenas de componentes impressionantes no Framer Marketplace criou um padrão genérico saturado na web ("Framer Agency Slop"). Evite com rigor:

1. **A Sobrecarga Simultânea de Gatilhos na Mesma Viewport**:
   Colocar na mesma tela um cursor customizado com rastro de partículas, um fundo com shader de líquido rodando a 60fps, um ticker de logos em loop acelerado e um card com inclinação 3D reflexiva destrói a hierarquia visual. A cognição do usuário é fragmentada e a taxa de rejeição aumenta.
2. **Cumulative Layout Shift (CLS) Desastroso**:
   Importar Code Components sem definir previamente suas proporções intrínsecas (`aspect-ratio`, dimensões explícitas de container ou fallbacks de altura/largura). Ao carregar o JavaScript, a página sofre saltos repentinos, penalizando a pontuação de SEO no Google Core Web Vitals.
3. **Cursor Magnético Invasivo que Quebra a Acessibilidade**:
   Forçar cursores personalizados que escondem o cursor nativo do sistema operacional (`cursor: none`) em toda a página. Isso quebra a usabilidade em touchscreens, confunde usuários de leitores de tela e gera latência tátil perceptível. **Regra de Ouro**: Cursores magnéticos só devem ser ativados em elementos pontuais de destaque (ex: dentro de um showreel ou área de visualização de portfólio), nunca de forma global.
4. **Ignorar o `prefers-reduced-motion`**:
   Renderizar animações contínuas de rotação ou tickers sem consultar a preferência de acessibilidade do sistema do usuário, violando as diretrizes WCAG 2.2 Nível AA.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 10 padrões de componentes mais emblemáticos e cobiçados do ecossistema Framer Marketplace, detalhados com sua anatomia técnica, gatilhos e encaixe arquitetural:

### 1. Infinite Smooth Ticker / Marquee (Seamless Momentum Loop)
- **Anatomia Visual**: Faixa contínua e ininterrupta de marcas, testemunhos, métricas ou ícones que desliza com velocidade constante sem qualquer salto ou corte visível entre a duplicação do array de itens. No hover, a velocidade desacelera suavemente por inércia ao invés de congelar bruscamente.
- **Gatilho de Interação**: Auto-play linear contínuo sincronizado via tempo delta (`useAnimationFrame`), com detecção de hover para desaceleração suave e suporte a arraste/drag tátil inercial.
- **Onde Encaixar**: Logo Clouds de prova social imediatamente abaixo do Hero, fitas de anúncio no topo da página ou faixas de certificação no rodapé.

### 2. 3D Perspective Card Carousel (Cylinder / Cover Flow Stack)
- **Anatomia Visual**: Conjunto de cards distribuídos em um arco tridimensional com rotação no eixo Y (`rotateY`), escala proporcional e profundidade Z (`translateZ`), criando um carrossel cilíndrico onde o card central ganha foco nítido e opacidade total enquanto os laterais receding no espaço com desfoque e sombra angular.
- **Gatilho de Interação**: Drag horizontal livre com snap magnético ao card mais próximo usando equações de mola; navegação por setas ou scroll horizontal.
- **Onde Encaixar**: Apresentação de cases de sucesso em portfólios, seleção de planos de assinatura ou galeria de screenshots de produto em SaaS.

### 3. Elastic Magnetic Button com Tração Física
- **Anatomia Visual**: Botão cujo corpo e rótulo de texto são atraídos magneticamente em direção ao ponteiro do mouse quando este se aproxima de um raio de atração (ex: 80px). Ao passar o mouse, o botão se estica levemente no vetor da velocidade do ponteiro e, ao sair, dispara um retorno elástico amortecido com oscilação orgânica.
- **Gatilho de Interação**: Evento `pointermove` em raio estendido com cálculo trigonométrico da distância entre o cursor e o centroide do elemento; `spring` transition no `mouseleave`.
- **Onde Encaixar**: CTA principal no Hero ("Agendar Demonstração", "Começar Gratuitamente") ou botão flutuante de ação rápida (FAB).

### 4. Interactive GLSL Liquid Shader / Wave Mesh Background
- **Anatomia Visual**: Plano de fundo interativo renderizado em WebGL (Three.js ou canvas nativo de shaders de fragmento) gerando gradientes de ruído perlin/simplex que ondulam organicamente. A aproximação do cursor gera uma perturbação de viscosidade líquida que se dissipa gradualmente.
- **Gatilho de Interação**: Uniforms GLSL vinculados a coordenadas normalizadas do mouse (`u_mouse: [x, y]`) e ao relógio contínuo (`u_time: float`), com renderização a 60fps throttled em segundo plano via IntersectionObserver.
- **Onde Encaixar**: Fundo da Hero section ou banner comemorativo de destaque (10% de impacto visual estrito).

### 5. Kinetic Text Scramble & Character Stagger Reveal
- **Anatomia Visual**: Título ou palavra-chave que, ao entrar na viewport ou receber foco, embaralha seus caracteres com glifos alfanuméricos aleatórios ou símbolos matemáticos (ex: `!@#$%¨&*01`) por frações de segundo até decantar na palavra definitiva de forma progressiva (da esquerda para a direita).
- **Gatilho de Interação**: IntersectionObserver (`whileInView`) com threshold de 0.5, ou gatilho de hover em links e botões de cabeçalho.
- **Onde Encaixar**: H1 do Hero de plataformas de cibersegurança, inteligência artificial, engenharia de software e Web3.

### 6. Parallax 3D Tilt Card com Reflexo Holográfico / Gyro
- **Anatomia Visual**: Card multicamada com perspectiva CSS (`perspective: 1000px`) onde o hover calcula a inclinação nos eixos X e Y proporcionalmente à posição do ponteiro em relação ao centro. Um gradiente radial semitransparente ("specular sheen") percorre a superfície acompanhando a fonte de luz simulada, enquanto elementos internos (ícone, badge) possuem profundidade Z real projetando-se à frente do fundo.
- **Gatilho de Interação**: `onMouseMove` local no container do card mapeado para valores de mola `useSpring(useTransform(...))`.
- **Onde Encaixar**: Cards de destaque no Bento Grid, cartões de planos de precificação (plano "Pro / Enterprise") ou vitrine de recursos de IA.

### 7. Floating Dynamic Island / Pill Navigation com `layoutId`
- **Anatomia Visual**: Barra de navegação flutuante minimalista em formato de pílula (`rounded-full`) com fundo escuro semitranslúcido e borda refinada. Ao alternar entre itens de menu, a pastilha de realce ativa desliza suavemente por baixo dos links sem interrupção de renderização. Ao rolar a página, a ilha se contrai em um menu compacto exibindo apenas ícone e CTA de conversão.
- **Gatilho de Interação**: `useScroll` para transição de estado da barra e `onHover` / seleção de link orquestrada por `<motion.div layoutId="nav-pill" />`.
- **Onde Encaixar**: Cabeçalho fixo superior da página (Header/Navbar).

### 8. Bento Grid com Efeito Radial Hover Spotlight
- **Anatomia Visual**: Grade de cards modulares assimétricos (bento grid) onde cada card possui uma borda ultrafina que se ilumina com uma luz radial focada exatamente onde o cursor do usuário está posicionado. A luz transborda suavemente entre cards vizinhos quando o mouse passa próximo às divisórias.
- **Gatilho de Interação**: `pointermove` no grid pai atualizando variáveis CSS de coordenadas (`--mouse-x` e `--mouse-y`) consumidas pelas máscaras de gradiente dos cards filhos.
- **Onde Encaixar**: Seção central de funcionalidades de produto (Product Features / Core Architecture).

### 9. Custom Magnetic Cursor Follower & Contextual Lens
- **Anatomia Visual**: Círculo de precisão ou ponto suave que flutua suavemente acompanhando o mouse com atraso inercial configurado. Ao sobrepor um vídeo, o cursor expande e exibe o texto "Play"; ao sobrepor um link externo, renderiza uma seta diagonal de 45 graus; ao sobrepor uma galeria, transforma-se em "Drag".
- **Gatilho de Interação**: Contexto global de estado React (`useCursorContext`) acionado por `onMouseEnter` e `onMouseLeave` de elementos marcados com atributos de dados (`data-cursor="play"`).
- **Onde Encaixar**: Seções de Portfólio, Showreel multimídia ou galerias imersivas de estúdio.

### 10. Elastic Accordion com Auto-Collapse e Height Spring
- **Anatomia Visual**: Lista de perguntas frequentes ou recursos explicativos onde a abertura de um item expande o container com suavidade orgânica calculada dinamicamente via `height: "auto"` e `opacity: 1`, sem cortes secos e com rotação do ícone de chevron proporcional à aceleração da abertura.
- **Gatilho de Interação**: Evento `onClick` no gatilho do accordion acionando `AnimatePresence` com transição de mola afinada.
- **Onde Encaixar**: Seção de FAQ (Perguntas Frequentes) antes do rodapé ou detalhamento de recursos em landing pages.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Como Funcionam os Code Components no Framer Studio
No ecossistema nativo do Framer, um Code Component é um componente React padrão exportado com a injeção de controles de propriedade via `addPropertyControls`. Isso permite que o código seja manipulado visualmente pelo editor do Framer:

```tsx
// Exemplo de estrutura nativa de Code Component do Framer Marketplace
import * as React from "react"
import { addPropertyControls, ControlType } from "framer"
import { motion } from "framer-motion"

export function FramerBadge(props) {
  const { title, glowColor, isPulsing, speed } = props

  return (
    <motion.div
      style={{
        padding: "6px 14px",
        borderRadius: 9999,
        background: "rgba(255, 255, 255, 0.05)",
        border: `1px solid ${glowColor}`,
        boxShadow: isPulsing ? `0 0 12px ${glowColor}` : "none",
        color: "#ffffff",
        display: "inline-flex",
        alignItems: "center",
        gap: 8,
      }}
      animate={isPulsing ? { scale: [1, 1.04, 1] } : {}}
      transition={{ duration: speed, repeat: Infinity, ease: "easeInOut" }}
    >
      <span style={{ width: 6, height: 6, borderRadius: "50%", background: glowColor }} />
      <span>{title}</span>
    </motion.div>
  )
}

// Configuração visual dos controles na barra lateral do Framer
addPropertyControls(FramerBadge, {
  title: { type: ControlType.String, title: "Texto", defaultValue: "Novo Lançamento" },
  glowColor: { type: ControlType.Color, title: "Cor do Brilho", defaultValue: "#3b82f6" },
  isPulsing: { type: ControlType.Boolean, title: "Pulsar", defaultValue: true },
  speed: { type: ControlType.Number, title: "Velocidade (s)", min: 0.5, max: 5, step: 0.1, defaultValue: 2 },
})
```

---

### Tradução de Componentes Framer para Projetos React / Next.js

Para utilizar os padrões consagrados do Framer Marketplace em projetos Next.js (App Router), React 19 e Tailwind CSS v4 sem depender do ambiente proprietário do Framer:

1. **Eliminar a dependência do pacote fechado `framer`**:
   Substitua as importações de `"framer"` pelo pacote universal **`framer-motion`** (ou a nova API unificada **`motion/react`**).
2. **Converter Property Controls em Props TypeScript Puras**:
   O objeto passado para `addPropertyControls` torna-se uma interface TypeScript rigorosa (`interface ComponentProps`), com valores padrão atribuídos via desestruturação de parâmetros.
3. **Substituir Estilos Inline por Classes Tailwind CSS v4**:
   Migre a estilização estática para classes utilitárias modernas e reserve os atributos `style` apenas para valores dinâmicos de transformação física derivados de `MotionValue`.
4. **Isolar Diretivas de Cliente (`"use client"`)**:
   Como os componentes de motion utilizam hooks de ciclo de vida (`useRef`, `useState`, `useEffect`, `useSpring`), isole-os em arquivos de cliente específicos, permitindo que as páginas e layouts do Next.js continuem sendo Server Components (RSC).

---

### Dependências & Setup Recomendado

Instale os pacotes fundamentais no seu projeto React/Next.js:

```bash
# Dependências essenciais para reproduzir os padrões do Framer Marketplace
npm install motion clsx tailwind-merge lucide-react
```

---

### Física de Movimento: As Fórmulas e Presets Consagrados do Framer

Para reproduzir a sensação tátil inconfundível do Framer, utilize os seguintes parâmetros calibrados de molas e curvas de velocidade:

```typescript
// Presets de Física de Mola (Spring Physics) do Framer
export const framerSprings = {
  // 1. Resposta Rápida / Tátil (Botões, Dropdowns, Toggles)
  snappy: {
    type: "spring",
    stiffness: 400,
    damping: 30,
    mass: 0.8,
  },
  // 2. Orgânica e Elástica (Cards expansíveis, Modais, Gavetas)
  organic: {
    type: "spring",
    stiffness: 260,
    damping: 20,
    mass: 1,
  },
  // 3. Suave e Contínua (Navegação em abas, layoutId pills, cursores)
  smooth: {
    type: "spring",
    stiffness: 180,
    damping: 24,
    mass: 1.2,
  },
  // 4. Efeito Magnético Forte (Magnetic CTA, Ícones puxados pelo cursor)
  magnetic: {
    type: "spring",
    stiffness: 150,
    damping: 15,
    mass: 0.5,
  },
} as const

// Curvas Bézier Oficiais de Alta Aceleração do Framer
export const framerEasings = {
  // Transição cinematográfica com desaceleração profunda
  easeOutQuart: [0.16, 1, 0.3, 1],
  // Transição simétrica fluida para opacidade e fade
  easeInOutSmooth: [0.4, 0, 0.2, 1],
}
```

---

### Receita de Código Funcional 1: Elastic Magnetic Button com Brilho Tátil

Um botão magnético responsivo que atrai seu centro na direção do cursor, com deslocamento independente do texto interno para gerar profundidade de paralaxe.

```tsx
"use client"

import React, { useRef, useState } from "react"
import { motion, useSpring, type SpringOptions } from "motion/react"
import { ArrowUpRight } from "lucide-react"

interface MagneticButtonProps {
  children?: React.ReactNode
  onClick?: () => void
  distanceThreshold?: number
  className?: string
}

const springConfig: SpringOptions = {
  stiffness: 180,
  damping: 18,
  mass: 0.6,
}

export function MagneticButton({
  children = "Explorar Recursos",
  onClick,
  distanceThreshold = 120,
  className = "",
}: MagneticButtonProps) {
  const buttonRef = useRef<HTMLButtonElement | null>(null)
  const [isHovered, setIsHovered] = useState(false)

  // Coordenadas com física de mola para o corpo do botão
  const buttonX = useSpring(0, springConfig)
  const buttonY = useSpring(0, springConfig)

  // Coordenadas com física de mola para o texto (deslocamento mais intenso para criar paralaxe)
  const textX = useSpring(0, { ...springConfig, stiffness: 220 })
  const textY = useSpring(0, { ...springConfig, stiffness: 220 })

  const handleMouseMove = (e: React.MouseEvent<HTMLButtonElement>) => {
    if (!buttonRef.current) return
    const rect = buttonRef.current.getBoundingClientRect()
    const centerX = rect.left + rect.width / 2
    const centerY = rect.top + rect.height / 2

    const deltaX = e.clientX - centerX
    const deltaY = e.clientY - centerY
    const distance = Math.hypot(deltaX, deltaY)

    if (distance < distanceThreshold) {
      // Puxa o botão com amortecimento
      buttonX.set(deltaX * 0.35)
      buttonY.set(deltaY * 0.35)
      // Texto se move com maior tração
      textX.set(deltaX * 0.5)
      textY.set(deltaY * 0.5)
    }
  }

  const handleMouseLeave = () => {
    setIsHovered(false)
    buttonX.set(0)
    buttonY.set(0)
    textX.set(0)
    textY.set(0)
  }

  return (
    <motion.button
      ref={buttonRef}
      onClick={onClick}
      onMouseMove={handleMouseMove}
      onMouseEnter={() => setIsHovered(true)}
      onMouseLeave={handleMouseLeave}
      style={{ x: buttonX, y: buttonY }}
      className={`relative inline-flex items-center justify-center gap-3 px-8 py-4 rounded-full 
        bg-zinc-950 text-white font-medium text-sm transition-colors duration-300
        border border-white/10 shadow-[0_0_20px_rgba(255,255,255,0.05)]
        hover:border-white/30 hover:shadow-[0_0_35px_rgba(255,255,255,0.15)]
        cursor-pointer select-none overflow-hidden ${className}`}
    >
      {/* Luz ambiente de hover */}
      <motion.div
        className="absolute inset-0 bg-radial from-white/15 to-transparent pointer-events-none rounded-full"
        animate={{ opacity: isHovered ? 1 : 0 }}
        transition={{ duration: 0.2 }}
      />

      {/* Conteúdo com paralaxe elástica */}
      <motion.span
        style={{ x: textX, y: textY }}
        className="relative z-10 flex items-center gap-2"
      >
        <span>{children}</span>
        <ArrowUpRight className="w-4 h-4 text-zinc-400 group-hover:text-white transition-colors" />
      </motion.span>
    </motion.button>
  )
}
```

---

### Receita de Código Funcional 2: Infinite Seamless Ticker com Hover Deceleration & Drag

O clássico componente de fita contínua (marquee) do Framer Marketplace, traduzido para React com desaceleração contínua no hover e ausência de salto geométrico.

```tsx
"use client"

import React, { useRef, useEffect } from "react"
import {
  motion,
  useMotionValue,
  useAnimationFrame,
  wrap,
  type MotionValue,
} from "motion/react"

interface InfiniteTickerProps {
  items: string[]
  baseVelocity?: number // pixels por segundo
  direction?: 1 | -1
  className?: string
}

export function InfiniteTicker({
  items = ["Vercel", "Linear", "Raycast", "Stripe", "Supabase", "OpenAI", "Framer"],
  baseVelocity = 60,
  direction = 1,
  className = "",
}: InfiniteTickerProps) {
  const baseX = useMotionValue(0)
  const isHovered = useRef(false)
  const currentSpeed = useRef(baseVelocity)

  // Duplicamos os itens para garantir preenchimento total e loop contínuo
  const displayItems = [...items, ...items, ...items, ...items]

  useAnimationFrame((_, delta) => {
    // Alvo de velocidade: desacelera suavemente para 10px/s no hover em vez de parar bruscamente
    const targetSpeed = isHovered.current ? baseVelocity * 0.15 : baseVelocity
    // Interpolação linear da velocidade (lerp) para suavidade máxima
    currentSpeed.current += (targetSpeed - currentSpeed.current) * 0.08

    const moveBy = direction * currentSpeed.current * (delta / 1000)
    baseX.set(baseX.get() - moveBy)
  })

  // Envelopamento cíclico dos valores no range percentual (-50% a 0%)
  const x = useMotionValue("-0%")
  useEffect(() => {
    return baseX.on("change", (latest) => {
      // Cria o loop sem salto ao atingir o limite
      const wrapped = wrap(-50, 0, latest)
      x.set(`${wrapped}%`)
    })
  }, [baseX, x])

  return (
    <div
      className={`relative w-full overflow-hidden py-6 select-none ${className}`}
      onMouseEnter={() => {
        isHovered.current = true
      }}
      onMouseLeave={() => {
        isHovered.current = false
      }}
    >
      {/* Máscara de gradiente lateral (fade out das pontas) */}
      <div className="absolute left-0 top-0 bottom-0 w-24 bg-gradient-to-r from-zinc-950 to-transparent z-10 pointer-events-none" />
      <div className="absolute right-0 top-0 bottom-0 w-24 bg-gradient-to-l from-zinc-950 to-transparent z-10 pointer-events-none" />

      {/* Faixa contínua em movimento acelerado por GPU */}
      <motion.div
        style={{ x, willChange: "transform" }}
        className="flex gap-12 w-max items-center"
      >
        {displayItems.map((item, index) => (
          <div
            key={index}
            className="flex items-center gap-3 px-6 py-2.5 rounded-full bg-zinc-900/60 border border-white/5 
              text-zinc-300 font-medium text-sm tracking-wide whitespace-nowrap shadow-sm backdrop-blur-xs
              hover:border-white/20 hover:text-white transition-colors duration-200"
          >
            <span className="w-2 h-2 rounded-full bg-emerald-500/80" />
            <span>{item}</span>
          </div>
        ))}
      </motion.div>
    </div>
  )
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao integrar referências e componentes inspirados no **Framer Marketplace** no documento de arquitetura (`DESIGN_BLUEPRINT.md`) de um novo projeto, siga os seguintes princípios e instruções mandatórias:

### 1. Declaração e Alocação dos Componentes no Blueprint
- **Classificação Estrita de Camadas**:
  Declare formalmente quais componentes pertencem à camada de 10% (Showstoppers de alto impacto) e quais pertencem à camada de 30% (Micro-interações do sistema). É expressamente proibido utilizar componentes baseados em canvas ou física contínua na camada de 60%.
  - *Exemplo de Alocação no Blueprint*:
    - **Hero Section**: `1x Kinetic Text Scramble` (H1) + `1x MagneticButton` (CTA primário).
    - **Logo Section**: `1x InfiniteTicker` (Parceiros/Tecnologias) com fade lateral.
    - **Features Grid**: `Bento Grid` com `Hover Radial Spotlight` via CSS variables (baixo custo).
    - **Navegação Global**: `Floating Navbar` com indicador ativo animado via `layoutId="nav-indicator"`.

### 2. Governança de Performance e Otimização de GPU
- **Isolamento de Redesenho**:
  Todo componente que escuta eventos de ponteiro (`pointermove`, `mousemove`) deve armazenar valores em instâncias de `MotionValue` (`useMotionValue`, `useSpring`) e transmiti-los diretamente para a camada de estilo do elemento DOM via `style={{ x, y }}`, **nunca** disparando `setState` a cada pixel de movimento do cursor.
- **Aceleração de Hardware Obrigatória**:
  Elementos que se movem de forma contínua (como tickers e carrosséis) devem conter a classe ou estilo `will-change: transform; transform: translateZ(0);` para evitar repaints desnecessários no thread principal da CPU.
- **Respeito Irrestrito a `prefers-reduced-motion`**:
  O blueprint deve estipular que todos os componentes de motion utilizem o hook `useReducedMotion()` do Framer Motion. Quando ativo, todas as molas e transições contínuas devem degradar elegantemente para `opacity: 1` e transição estática, desativando loops e deslocamentos de coordenadas.

### 3. Matriz de Decisão: Exportação do Framer Studio vs Reimplementação em React Puro
- **Quando importar diretamente ou usar embeds do Framer**:
  Apenas em páginas de marketing puramente estáticas hospedadas no ecossistema Framer, ou ao testar protótipos de alta fidelidade com designers e stakeholders.
- **Quando reimplementar com `motion/react` + Tailwind**:
  Obrigatório em qualquer aplicação web em produção (Next.js, Remix, Vite, Astro). A reimplementação em React puro elimina scripts de rastreamento de terceiros, garante tipagem TypeScript estrita, unifica os tokens com o Shadcn UI e reduz o payload inicial do pacote em mais de 70%.

### 4. Checklist de Validação para a IA de Implementação
Antes de finalizar qualquer página ou tela inspirada no Framer Marketplace, valide:
- [ ] O cursor nativo do usuário foi preservado sem hacks globais de `cursor: none`?
- [ ] A taxa de quadros (FPS) permanece estável em 60fps durante a rolagem da página?
- [ ] Os containers possuem dimensões estáticas mínimas definidas para prevenir Cumulative Layout Shift (CLS)?
- [ ] Há no máximo 1 showstopper visual (GLSL / 3D / Scramble complexo) visível por viewport?
- [ ] Os textos mantiveram contraste WCAG AA contra fundos escuros e gradientes reflexivos?
