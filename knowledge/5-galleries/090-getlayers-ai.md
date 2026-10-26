---
id: "getlayers-ai"
name: "GetLayers AI & Layers Community (High-Craft UI Design)"
url: "https://www.getlayers.ai/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico: ["High-Craft UI Design", "Modern Tactile Skeuomorphism", "Layered Bento Grids", "Cinematic AI WebGL", "OKLCH Obsidian & Specular Hairlines"]
densidade_informacao: "Media/Narrativa"
impacto_visual: "Editorial/Sofisticado"
custo_computacional: "Moderado a Alto (Shaders WebGL, Stacking Shadows e Backdrop Filters)"
stack_frameworks: ["React 19 / 18", "Next.js (App Router)", "Tailwind CSS v4 & v3", "Framer Motion", "Three.js / React Three Fiber", "GLSL Shaders", "GetLayers MCP (`https://mcp.getlayers.ai/mcp`)"]
compatibilidade:
  fontes_ideais: ["Geist Sans & Geist Mono", "Satoshi", "General Sans", "Inter Tight", "Roobert", "PP Neue Montreal", "JetBrains Mono"]
  paletas_ideais: ["Obsidian High-Contrast OKLCH (`oklch(0.12 0.01 260)`)", "Specular Rim Light (`oklch(0.98 0 0 / 0.12)`)", "Satin Pearl Light Mode (`oklch(0.97 0.005 250)`)", "Deep Cosmic Indigo & Aurum Amber"]
  combinacoes_recomendadas: ["Aceternity UI", "Magic UI", "Cult UI", "Motion Primitives", "Radix UI", "Lucide React", "Sonner"]
  conflitos_esteticos: ["Neumorfismo de plástico borrado (soft-drop shadow sem aresta)", "Material Design 2 genérico com sombras primárias difusas", "Flat Design 1.0 monocromático sem relevo e sem luz física"]
---

# GetLayers AI & Layers Community — Dossiê Estético, Anatomia de Layout & Padrões de Alta Precisão (High-Craft UI)

---

## 1. Identidade Visual & O Que Torna Único (Assinatura)

### O Manifesto Contra o "AI Slop" & O Retorno do High-Craft
O ecossistema **GetLayers** (`getlayers.ai`) — concebido pelo estúdio de vanguarda digital **Textura** — aliado à comunidade de criadores de elite **Layers** (`layers.to`), representa o movimento contemporâneo mais incisivo de resistência contra a pasteurização estética da web. Na era pós-2023, a proliferação desregulada de interfaces geradas por modelos de linguagem saturou o mercado com produtos visivelmente homogêneos: blocos neutros desprovidos de intenção tátil, tipografia mecânica sem ritmo e layouts previsíveis ("AI Slop").

A filosofia fundadora do GetLayers e da comunidade Layers é expressa em uma premissa clara: **a engenharia de software impulsionada por IA não deve nivelar o design por baixo, mas sim democratizar a estética de estúdios de primeiro escalão.**

```
┌────────────────────────────────────────────────────────────────────────┐
│                   A EVOLUÇÃO DA FÍSICA DE INTERFACES                  │
├────────────────────┬────────────────────┬──────────────────────────────┤
│ Skeuomorfismo 2012 │  Flat Design 2016  │ Modern High-Craft UI (Layers)│
├────────────────────┼────────────────────┼──────────────────────────────┤
│ Couro com costura  │ 0px de profundidade│ Precisão ótica sub-pixel     │
│ Gradiente bevel 90s│ Cores sólidas/opacas│ Arestas especulares de 1px   │
│ Simulação mimética │ Vetorização fria   │ Luz física, peso e inércia  │
│ Textura pesada     │ Ausência de física │ Micro-detalhes táteis OKLCH  │
└────────────────────┴────────────────────┴──────────────────────────────┘
```

### A Assinatura Visual: "Modern Tactile Skeuomorphism"
Diferente do skeuomorfismo hiper-literal da virada de década de 2010 (que reproduzia texturas de madeira envernizada e costuras de couro), o estilo imortalizado no Layers é o **Modern Tactile Skeuomorphism** (ou *Neo-Tactile High-Craft*). Trata-se da transposição da física de manufatura industrial de hardware premium (alumínio usinado anodizado da Apple, policarbonato jateado da Teenage Engineering, mostradores da Braun de Dieter Rams) para o DOM web:

1. **Arestas Especulares de 1px (Specular Rim Highlights)**:
   Containers, botões e cartões nunca utilizam bordas simples de uma única cor sólida. Em vez disso, aplicam uma técnica ótica de "luz de teto": a aresta superior e esquerda do elemento recebe um filete de luz especular (`inset 0 1px 0 rgba(255, 255, 255, 0.15)` no dark mode), simulando uma fonte de luz zenital incidindo no chanfro chanfrado do objeto, enquanto as bordas inferiores e a sombra de gota aterram a peça na profundidade da tela.
2. **Superfícies Escuras OKLCH Não-Negras (Obsidian & Slate Depth)**:
   A paleta noturna rejeita o `#000000` estéril. Adota-se o espaço de cor perceptual **OKLCH**, modulando superfícies com sutis matizes cósmicos (tons de obsidiana azulada `oklch(0.12 0.015 260)` e grafite de carbono `oklch(0.16 0.01 260)`). A percepção de contraste preserva a luminância linear sem esmagar os tons médios.
3. **Layered Bento Grids com Profundidade Modular**:
   A arquitetura visual organiza a narrativa em módulos geométricos interligados ("Bento Boxes"), onde cada módulo opera como uma gaveta física usinada com cantos arredondados cirurgicamente proporcionais (`calc(var(--radius) - 2px)` para aninhamento perfeito).
4. **Cinematic WebGL & Shaders de Refração**:
   O GetLayers AI introduz o conceito de *Spatial Anchors*: pontos focais 3D (como os famosos presets *Rift Stone*, *Halcyon Gate*, *Aurum Peak*, *Pinwheel Galaxy* e *Pixel Glass*) que reagem suavemente ao cursor e ao scroll da página, conferindo à aplicação o peso cenográfico de uma produção cinematográfica interativa.
5. **Injeção de IA via Protocolo Aberto (MCP Server)**:
   O GetLayers disponibiliza um endpoint de **Model Context Protocol (MCP)** (`https://mcp.getlayers.ai/mcp`), permitindo que agentes de engenharia (como Claude Code, Cursor e Gemini) consultem e importem em tempo de compilação templates hand-crafted, shaders GLSL e layouts de bento prontos, sem o atrito de cópia manual de prompts.

---

## 2. Cenários Ideais de Aplicação (Quando Usar como Direção Visual)

### Nichos de Produto de Alta Conversão & Prestígio
- **SaaS B2B de Desenvolvedores e Infraestrutura (DevTools / Cloud Platforms)**:
  Plataformas inspiradas no padrão Linear, Raycast, Supabase, Neon, Clerk e Vercel, onde a percepção de precisão técnica do software é comunicada diretamente pelo rigor visual da interface.
- **Plataformas de IA Generativa & Agentes Autônomos (AI Copilots & Workbenches)**:
  Aplicações que orquestram fluxos de raciocínio complexos, onde cards modulares colapsáveis, nós de grafos, sidebars de comandos com teclas usinadas e visualizadores de streaming de dados geram confiança institucional.
- **Fintechs Institucionais, Neobanks de Alta Renda & Web3 de Elite**:
  Produtos financeiros que exigem a sofisticação tátil de cartões de crédito de titânio (Black Cards), gráficos em tempo real com sparklines de precisão cirúrgica e botões com sensação háptica de acionamento mecânico.
- **Landing Pages Cinematográficas de Lançamento de Hardware e Software**:
  Páginas de apresentação de produto em que a narrativa visual utiliza iluminação atmosférica, sombras de contato, efeitos de vidro fosco (frosted glass) e WebGL para gerar desejo imediato.

### Papel no Ritmo Visual (A Aplicação Rigorosa da Regra 60-30-10)

```
┌────────────────────────────────────────────────────────────────────────┐
│               DISTRIBUIÇÃO HARMONIOSA DE CAMADAS VISUAIS               │
├────────────────────────────────────────────────────────────────────────┤
│ 60% — Fundação Estrutural (Obsidian Surfaces, Grids & Tipografia Mono) │
├────────────────────────────────────────────────────────────────────────┤
│ 30% — Componentes Táteis (Bento Modules, Botões Chanfrados, Docks)    │
├────────────────────────────────────────────────────────────────────────┤
│ 10% — Showstoppers Especiais (Shaders WebGL 3D, Mesh Glow, Rim Lights) │
└────────────────────────────────────────────────────────────────────────┘
```

- **60% — A Fundação Neutra Estrutural (Canvas Profundo & Tipografia Rigorosa)**:
  O fundo da página em obsidiana OKLCH com ruído micro-texturizado quase imperceptível (`opacity: 0.025`), linhas de grid cinza translúcidas (`oklch(1 0 0 / 0.06)`) e tipografia estrutural neutra (Geist Sans para corpo de texto, Geist Mono para métricas e atalhos). Esta camada não grita: ela estabelece o palco escuro de um museu moderno.
- **30% — A Camada Tátil de Interação (Módulos Bento & Controles de Hardware)**:
  Os cartões com chanfros de 1px, botões usinados com efeito de relevo e clique mecânico, sidebars retráteis com acentos de cor atenuados e barras de navegação estilo dock flutuante suspensas com `backdrop-blur-xl`.
- **10% — O Showstopper Magnético (O Foco Cinematográfico)**:
  O elemento protagonista que fixa a retenção do visitante: uma cena WebGL de vidro óptico refrativo (ex: *Pixel Glass*), uma luminária de gradiente dinâmico com dispersão radial (ex: *Pharos Gradient*), ou um botão de ação primária (CTA) cercado por um feixe de luz perimetral animado (*border-beam*).

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

### ⚠️ Proibido em:
1. **Sistemas Críticos de Alta Densidade com Requisito Estrito WCAG AAA Governamental**:
   Interfaces governamentais, sistemas médicos de monitoramento de leitos ou formulários tributários públicos não devem adotar micro-contrastes de 1px translúcidos e superfícies escuras com iluminação atmosférica. Nesses cenários, o utilitarismo plano de alto contraste puro e a tipografia padrão de sistema têm precedência absoluta.
2. **E-commerces B2C de Varejo de Massa / Produtos de Baixo Ticket**:
   Plataformas que vendem produtos populares de giro rápido se beneficiam de cores vivas e contrastantes (amarelo, verde, vermelho vibrante), banners promocionais agressivos e botões grandes e planos. A estética refinada e escura do High-Craft pode ser percebida como excludente, solene ou "cara demais" pelo consumidor comum.
3. **Aplicações para Dispositivos de Baixa Capacidade de Hardware (IoT / Navegadores Embarcados)**:
   A sobreposição simultânea de múltiplos `box-shadow` inset, filtros `backdrop-filter: blur(24px)` e canvases WebGL degradam drasticamente o framerate (FPS) em celulares de entrada e telas automotivas de baixo processamento gráfico.

### ⚠️ Armadilhas de Imitação ("High-Craft Anti-Patterns"):
- **O Anti-padrão do "Skeuomorphic Slop"**: Tentar adicionar relevo a cada ícone, linha e texto simultaneamente, transformando a interface em um amontoado confuso de plásticos brilhantes sem hierarquia de profundidade. Apenas os elementos interativos primários recebem propriedades táteis.
- **Bordas Grossas ou Iluminação Desalinhada**: Usar bordas de 2px ou aplicar highlights em direções conflitantes (ex: luz vindo da esquerda no card A e da direita no card B). Toda a iluminação do ecossistema Layers obedece a uma **fonte de luz consistente a 90° zenital** (luz vindo do topo).
- **Sombras com Preto Puro (`rgba(0, 0, 0, 1)`)**: O uso de preto estéril gera sombras "sujas" e opacas. Sombras no design de alta precisão devem utilizar matizes colorizados em baixa opacidade modulados no espaço OKLCH (`box-shadow: 0 12px 32px -4px oklch(0.08 0.02 260 / 0.45)`).

---

## 4. Catálogo Detalhado de Componentes & Padrões Visuais Notáveis

A seguir, a dissecação técnica dos 8 componentes mais influentes extraídos das galerias do GetLayers AI e da comunidade Layers:

```
┌────────────────────────────────────────────────────────────────────────┐
│          ANATOMIA DE UM BENTO CARD TÁTIL COM DESTAQUE ESPECULAR        │
│                                                                        │
│ ┌────────────────────────────────────────────────────────────────────┐ │
│ │ [1] Rim Light Superior: 1px linear highlight (oklch 1 0 0 / 0.15) │ │
│ │ ┌────────────────────────────────────────────────────────────────┐ │ │
│ │ │ [2] Glow Radial Contextual (Segue a coordenada do mouse)      │ │ │
│ │ │                                                                │ │ │
│ │ │ [3] Tipografia Titular com Máscara de Gradiente Vertical       │ │ │
│ │ │                                                                │ │ │
│ │ │ [4] Botão Táteis Usinado com Chanfro Inset e Curso Mecânico   │ │ │
│ │ └────────────────────────────────────────────────────────────────┘ │ │
│ │ [5] Sombra de Contato Aterrada (oklch 0.05 0.02 260 / 0.60)      │ │
│ └────────────────────────────────────────────────────────────────────┘ │
└────────────────────────────────────────────────────────────────────────┘
```

### 1. Tactile Specular Button (Botão Táteis Usinado)
- **Anatomia**: Estrutura retangular com `rounded-xl`, gradiente de superfície sutil de cima para baixo (`from-white/[0.08] to-transparent`), borda perimetral de 1px com highlight luminoso superior (`box-shadow: inset 0 1px 0 oklch(1 0 0 / 0.20)`), e sombra rebaixada inferior que simula a espessura da tecla.
- **Gatilho / Comportamento**: No hover, o highlight superior intensifica suavemente; no active (clique), a tecla sofre translação de `translate-y-[1px]` e a sombra inferior colapsa instantaneamente, transmitindo o clique mecânico de um microswitch tátil.
- **Onde Encaixar**: Botões de ação primária (CTA), chaves de envio em modais e gatilhos de checkout.

### 2. Layered Bento Card com Cursor-Tracking Spotlight
- **Anatomia**: Painel com fundo escuro acetinado (`bg-zinc-950/80` com `backdrop-blur-md`), borda perimetral de `border-white/[0.08]`. Um listener de mouse rastreia as coordenadas `(x, y)` relativas ao container, projetando um cone de luz especular radial de 400px de diâmetro na borda e no fundo.
- **Gatilho / Comportamento**: Conforme o usuário navega pelo grid, a borda do card revela seu relevo metálico exatamente onde o cursor se aproxima, revelando o contorno chanfrado de maneira reativa.
- **Onde Encaixar**: Seções de Features, cards demonstrativos de produto e vitrines de planos de assinatura.

### 3. Machined Hardware Segmented Switch
- **Anatomia**: Trilho externo rebaixado (`bg-black/60` com `box-shadow: inset 0 2px 4px rgba(0,0,0,0.8)`), dentro do qual repousa uma pastilha deslizante metálica com cantos arredondados, chanfro especular superior e rótulo tipográfico nítido.
- **Gatilho / Comportamento**: Transição com física de mola elástica (*spring physics* com overshoot mínimo) ao alternar entre as abas (ex: "Mensal" vs "Anual", ou visualizações de gráficos).
- **Onde Encaixar**: Seletores de frequência de cobrança, filtros de categoria e toggles de visualização de painéis analíticos.

### 4. Floating Island Glass Dock (Barra de Ações Flutuante)
- **Anatomia**: Pílula flutuante suspensa acima da margem inferior (`bottom-8`), munida de `backdrop-blur-2xl`, fundo em vidro negro semi-translúcido (`oklch(0.12 0.01 260 / 0.70)`), anel perimetral com gradiente de luz e atalhos de teclado encapsulados em micro-tags usinadas (`<kbd>` com borda de relevo).
- **Gatilho / Comportamento**: Efeito de aproximação magnética nos ícones conforme o mouse se aproxima do dock, com tooltip descritivo emergindo em spring physics de 150ms.
- **Onde Encaixar**: Navegação principal de web apps produtivos, barras de ferramentas de canvas e consoles de gerenciamento.

### 5. High-Density Instrumental Metric Cell
- **Anatomia**: Módulo de exibição numérica para SaaS enterprise. Apresenta label em caixa-alta reduzida (`text-[11px] font-mono tracking-wider text-zinc-400`), valor métrico principal com tipografia tabular (`tabular-nums font-semibold`), sparkline de vetor SVG de 1.5px de espessura e badge com micro-indicador de status em LED pulsante.
- **Gatilho / Comportamento**: Ao pairar sobre a sparkline, um cursor vertical guia revela tooltips dinâmicos com a data e valor em micro-segundos sem recalcular o layout.
- **Onde Encaixar**: Painéis analíticos, monitoramento de servidores, fluxos de faturamento e telemetria de modelos de IA.

### 6. Liquid Mesh Gradient Canvas (Aura Atmosférica)
- **Anatomia**: Fundo com camadas de gradientes radiais sobrepostos e desfocados (`filter: blur(100px)`) com interpolações orgânicas de matizes complementares (ex: cobalto cósmico `#1e1b4b`, âmbar sutil `#78350f` e obsidiana `#09090b`), animadas continuamente via keyframes CSS ou canvas WebGL.
- **Gatilho / Comportamento**: Deslocamento suave e infinito de rotação e escala (ciclo de 20 a 30 segundos), criando uma sensação de respiração espacial no fundo da página sem disputar a legibilidade do texto.
- **Onde Encaixar**: Hero sections imersivas, fundos de cartões de conversão e estados de "pensamento" de agentes de IA.

### 7. Refractive Spatial Anchor (Cena WebGL 3D Estilo Rift Stone / Aurum)
- **Anatomia**: Canvas Three.js/R3F renderizando uma geometria tridimensional com shaders customizados (materiais dielétricos, reflexão Fresnel, micro-rugosidade e dispersão cromática no vidro óptico).
- **Gatilho / Comportamento**: A rotação da geometria orbita suavemente com a interpolação do cursor do usuário (lerp damping de 0.05) e reage ao scroll da página com translação em profundidade Z.
- **Onde Encaixar**: Ponto focal de Hero de páginas de lançamento institucional de marcas e ferramentas de engenharia de software.

### 8. Micro-Grain Noise Substratum
- **Anatomia**: Camada global fixa (`pointer-events-none fixed inset-0 z-50`) alimentada por um SVG inline com filtro `<feTurbulence>` e `<feColorMatrix>` em opacidade ultra-reduzida (`opacity-[0.025]`) com modo de mesclagem `mix-blend-overlay`.
- **Gatilho / Comportamento**: Elimina as bandas de cor (*color banding*) causadas pelos gradientes em telas de 8 bits e concede à interface digital a tatilidade de um papel de alta gramatura ou titânio polido.
- **Onde Encaixar**: Camada raiz de todo o layout (`app/layout.tsx` ou wrapper principal).

---

## 5. Arquitetura Técnica, Física de Movimento & Receita de Código Funcional

### A Física do Movimento: Especificações Rigorosas

No universo de High-Craft do Layers, animações "lineares" ou elásticas exageradas no estilo desenho animado são terminantemente banidas. O movimento simula a inércia, o atrito e a massa de peças físicas de precisão:

```
┌────────────────────────────────────────────────────────────────────────┐
│                    PARÂMETROS DE FÍSICA DE MOVIMENTO                   │
├─────────────────────┬──────────────┬───────────────────┬───────────────┤
│ Interação           │ Tipo         │ Valores / Curva   │ Duração       │
├─────────────────────┼──────────────┼───────────────────┼───────────────┤
│ Clique / Pressão    │ Damping      │ stiffness: 500    │ ~100ms - 150ms│
│                     │ Spring       │ damping: 35       │               │
├─────────────────────┼──────────────┼───────────────────┼───────────────┤
│ Bento Expand / Open │ Cubic-Bezier │ (0.16, 1, 0.3, 1) │ 350ms - 450ms │
│                     │ Expo Out     │                   │               │
├─────────────────────┼──────────────┼───────────────────┼───────────────┤
│ Modal / Flyout      │ Spring       │ stiffness: 280    │ ~250ms        │
│                     │ c/ Overshoot │ damping: 24       │               │
├─────────────────────┼──────────────┼───────────────────┼───────────────┤
│ Spotlight Cursor    │ Linear Lerp  │ factor: 0.08      │ Contínuo      │
└─────────────────────┴──────────────┴───────────────────┴───────────────┘
```

- **Transição de Pressão Mecânica (Button Press)**:
  `cubic-bezier(0.2, 0.8, 0.2, 1)` ou Framer Motion Spring `{ stiffness: 500, damping: 35, mass: 0.5 }`. O retorno do botão precisa ser quase imperceptível em sua rapidez, sem oscilação secundária perceptível.
- **Revelação de Módulos (Bento Card Expansion)**:
  Curva de aceleração abrupta com desaceleração longa (`cubic-bezier(0.16, 1, 0.3, 1)` — variação de quintic/exponential out). A gaveta abre com rapidez de resposta e acomoda-se com peso nos últimos 15% do curso.

---

### Tokens de Design em CSS / OKLCH (Design Engine High-Craft)

Copie e integre estes tokens em seu arquivo global de CSS (`globals.css` ou Tailwind v4 `@theme`):

```css
@layer base {
  :root {
    /* Superfícies OKLCH de Alta Fidelidade (Dark High-Craft Default) */
    --surface-canvas: oklch(0.12 0.012 260);
    --surface-subtle: oklch(0.15 0.015 260);
    --surface-elevated: oklch(0.18 0.018 260);
    --surface-card: oklch(0.14 0.014 260 / 0.85);
    
    /* Tipografia de Precisão */
    --text-primary: oklch(0.98 0 0);
    --text-secondary: oklch(0.72 0.01 260);
    --text-tertiary: oklch(0.50 0.015 260);
    
    /* Arestas Especulares e Filetes de Luz */
    --border-specular-top: oklch(1 0 0 / 0.16);
    --border-subtle: oklch(1 0 0 / 0.07);
    --border-hairline: oklch(1 0 0 / 0.04);
    
    /* Acentos & Iluminação Tátil */
    --accent-glow: oklch(0.65 0.22 265);
    --accent-glow-subtle: oklch(0.65 0.22 265 / 0.12);
    
    /* Sombras Físicas Estruturadas (Multi-Camada) */
    --shadow-machined: 
      0 1px 0 0 var(--border-specular-top) inset,
      0 2px 4px 0 oklch(0 0 0 / 0.40),
      0 12px 24px -4px oklch(0 0 0 / 0.55);
      
    --shadow-button-press:
      0 1px 0 0 oklch(1 0 0 / 0.08) inset,
      0 1px 2px 0 oklch(0 0 0 / 0.60);
  }
}
```

---

### Receita de Código Funcional: Bento Spotlight Card com Botão Táteis Usinado

O código React a seguir é uma implementação completa, autocontida e funcional demonstrando os padrões de **Layered Bento Card com Cursor-Tracking Spotlight**, **Aresta Especular de 1px** e **Botão Táteis Mecânico**:

```tsx
"use client";

import React, { useRef, useState } from "react";
import { motion, useMotionValue, useSpring, useTransform } from "framer-motion";
import { ArrowUpRight, Cpu, Sparkles, Terminal } from "lucide-react";

/**
 * BentoCardHighCraft
 * Componente insígnia da estética Layers:
 * - 1px Specular Border no topo
 * - Rastreamento de cursor para cone de luz radial dinâmico
 * - Botão usinado com feedback mecânico de clique
 */
export function BentoCardHighCraft({
  title = "Motor Neural Autônomo",
  description = "Orquestração determinística de agentes cognitivos com telemetria em tempo real e tempo de resposta sub-milissegundo.",
  badge = "v2.4 High-Craft",
}) {
  const cardRef = useRef<HTMLDivElement>(null);
  const [isHovered, setIsHovered] = useState(false);

  // Coordenadas relativas do cursor para o spotlight
  const mouseX = useMotionValue(-500);
  const mouseY = useMotionValue(-500);

  // Amortecimento físico para a luz seguir suavemente o mouse
  const smoothX = useSpring(mouseX, { stiffness: 350, damping: 28 });
  const smoothY = useSpring(mouseY, { stiffness: 350, damping: 28 });

  function handleMouseMove(e: React.MouseEvent<HTMLDivElement>) {
    if (!cardRef.current) return;
    const rect = cardRef.current.getBoundingClientRect();
    mouseX.set(e.clientX - rect.left);
    mouseY.set(e.clientY - rect.top);
  }

  function handleMouseEnter() {
    setIsHovered(true);
  }

  function handleMouseLeave() {
    setIsHovered(false);
    mouseX.set(-500);
    mouseY.set(-500);
  }

  return (
    <div
      ref={cardRef}
      onMouseMove={handleMouseMove}
      onMouseEnter={handleMouseEnter}
      onMouseLeave={handleMouseLeave}
      className="group relative w-full max-w-md rounded-2xl p-px transition-all duration-300"
      style={{
        // Fundo com borda sutil combinada ao gradiente de borda dinâmica
        background: `linear-gradient(180deg, rgba(255, 255, 255, 0.12) 0%, rgba(255, 255, 255, 0.03) 100%)`,
      }}
    >
      {/* 1. Camada de Borda Especular Dinâmica (Spotlight no Contorno) */}
      <motion.div
        className="pointer-events-none absolute -inset-px rounded-2xl opacity-0 transition-opacity duration-300 group-hover:opacity-100"
        style={{
          background: useTransform(
            [smoothX, smoothY],
            ([x, y]) =>
              `radial-gradient(350px circle at ${x}px ${y}px, rgba(255, 255, 255, 0.35), transparent 80%)`
          ),
          maskImage:
            "linear-gradient(black, black) content-box, linear-gradient(black, black)",
          maskComposite: "exclude",
          WebkitMaskComposite: "xor",
          padding: "1px",
        }}
      />

      {/* 2. Corpo do Cartão Bento com Fundo de Obsidiana */}
      <div className="relative flex flex-col justify-between overflow-hidden rounded-[15px] bg-[#0c0d12]/95 p-6 backdrop-blur-xl">
        {/* Luz Ambiente Interna Seguindo o Cursor */}
        <motion.div
          className="pointer-events-none absolute -inset-px opacity-0 transition-opacity duration-300 group-hover:opacity-100"
          style={{
            background: useTransform(
              [smoothX, smoothY],
              ([x, y]) =>
                `radial-gradient(280px circle at ${x}px ${y}px, rgba(99, 102, 241, 0.12), transparent 80%)`
            ),
          }}
        />

        {/* Linha de Destaque Zenital Fixo de 1px (Rim Light) */}
        <div className="absolute inset-x-0 top-0 h-px bg-gradient-to-r from-transparent via-white/20 to-transparent" />

        {/* Topo do Card: Badge de Hardware & Ícone de Precisão */}
        <div className="relative z-10 flex items-center justify-between">
          <div className="flex items-center gap-2 rounded-full border border-white/10 bg-white/[0.03] px-2.5 py-1 text-[11px] font-mono font-medium text-zinc-300 shadow-[inset_0_1px_0_rgba(255,255,255,0.1)]">
            <span className="h-1.5 w-1.5 rounded-full bg-emerald-400 animate-pulse" />
            {badge}
          </div>

          <div className="flex h-9 w-9 items-center justify-center rounded-xl border border-white/10 bg-white/[0.04] text-zinc-300 shadow-[inset_0_1px_0_rgba(255,255,255,0.15)] transition-transform duration-200 group-hover:scale-105">
            <Cpu className="h-4 w-4" />
          </div>
        </div>

        {/* Centro do Card: Tipografia Esculpida */}
        <div className="relative z-10 my-6">
          <h3 className="text-xl font-semibold tracking-tight text-white">
            {title}
          </h3>
          <p className="mt-2 text-sm leading-relaxed text-zinc-400">
            {description}
          </p>
        </div>

        {/* Base do Card: Célula Instrumental & Botão Táteis Usinado */}
        <div className="relative z-10 flex items-center justify-between border-t border-white/[0.06] pt-4">
          <div className="flex items-center gap-2 text-xs font-mono text-zinc-500">
            <Terminal className="h-3.5 w-3.5" />
            <span>LATÊNCIA: 0.42ms</span>
          </div>

          {/* Botão Táteis Usinado (Tactile Specular Button) */}
          <motion.button
            whileHover={{ scale: 1.02 }}
            whileTap={{ scale: 0.97, y: 1 }}
            transition={{ type: "spring", stiffness: 500, damping: 30 }}
            className="relative inline-flex items-center gap-1.5 overflow-hidden rounded-lg border border-white/15 bg-gradient-to-b from-white/10 to-white/[0.02] px-3.5 py-1.5 text-xs font-medium text-white shadow-[inset_0_1px_0_rgba(255,255,255,0.25),0_2px_4px_rgba(0,0,0,0.5)] transition-colors hover:from-white/15 hover:to-white/[0.05]"
          >
            <span>Explorar</span>
            <ArrowUpRight className="h-3.5 w-3.5 text-zinc-400 transition-transform group-hover:translate-x-0.5 group-hover:-translate-y-0.5" />
          </motion.button>
        </div>
      </div>
    </div>
  );
}

/**
 * Exemplo de Switch Usinado (Machined Hardware Toggle)
 */
export function MachinedSegmentedSwitch({
  options = ["Produção", "Homologação"],
  activeIndex = 0,
  onChange,
}: {
  options?: string[];
  activeIndex?: number;
  onChange?: (index: number) => void;
}) {
  const [selected, setSelected] = useState(activeIndex);

  return (
    <div className="relative inline-flex rounded-xl border border-white/10 bg-black/60 p-1 shadow-[inset_0_2px_4px_rgba(0,0,0,0.8)]">
      {options.map((option, idx) => {
        const isCurrent = selected === idx;
        return (
          <button
            key={option}
            onClick={() => {
              setSelected(idx);
              onChange?.(idx);
            }}
            className="relative z-10 rounded-lg px-4 py-1.5 text-xs font-medium font-mono transition-colors duration-200"
            style={{
              color: isCurrent ? "#ffffff" : "#a1a1aa",
            }}
          >
            {isCurrent && (
              <motion.div
                layoutId="machined-active-pill"
                className="absolute inset-0 rounded-lg border border-white/20 bg-gradient-to-b from-white/15 to-white/5 shadow-[inset_0_1px_0_rgba(255,255,255,0.3),0_2px_6px_rgba(0,0,0,0.6)]"
                transition={{ type: "spring", stiffness: 450, damping: 32 }}
              />
            )}
            <span className="relative z-10">{option}</span>
          </button>
        );
      })}
    </div>
  );
}
```

---

### Como a IA Deve Pesquisar ao Vivo no GetLayers AI e no Layers

Quando o agente precisar inspecionar padrões específicos em tempo real:

1. **GetLayers AI — Consulta de Templates e Shaders (`getlayers.ai`)**:
   - Templates Completos: `https://www.getlayers.ai/templates` (pesquise por *Nexus*, *Seed*, *Vesper*, *Stride*, *AI Studio*, *Creative Director*, *Dantora*, *Clarix*).
   - Cenas 3D WebGL / Shaders: `https://www.getlayers.ai/3d` (pesquise por *Rift Stone*, *Halcyon Gate*, *Orb*, *Epoxy Drift*, *Pinwheel Galaxy*, *Aurum Peak*, *Pixel Glass*, *Argent Massif*).
   - Seções de Movimento: `https://www.getlayers.ai/sections` (pesquise por *Colonnade*, *Carousel Spotlight*, *Showcase Equator*).
   - Gradientes Líquidos e de Malha: `https://www.getlayers.ai/gradients` (pesquise por *Strigil*, *Pharos*, *Laminar*, *Komorebi*, *Antipode*, *Ichor*, *Kindle*, *Shoal*, *Tress*, *Tombac*, *Serigraph*, *Quicksilver*).
   - **MCP Endpoint Oficial**: `https://mcp.getlayers.ai/mcp` (permite que clientes compatíveis busquem metadados de código e estruturas completas diretamente via chamadas de tool).

2. **Layers Community (`layers.to`) — Consulta de Referências de UI e Componentes**:
   - Feed Principal de Elite: `https://layers.to/explore`
   - Componentes e Micro-interações: `https://layers.to/components`
   - Dashboards SaaS e B2B: `https://layers.to/tags/saas` ou `https://layers.to/tags/dashboard`
   - Design Systems & Mobile iOS: `https://layers.to/tags/mobile` e `https://layers.to/tags/design-system`

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir o documento de arquitetura de interface (`DESIGN_BLUEPRINT.md`) de qualquer projeto que invoque o DNA visual do **GetLayers / Layers**, incorpore obrigatoriamente as seguintes diretivas técnicas:

### Checklist de Implementação "High-Craft"
1. **Luz Zenital Consistente (The Universal 90° Rule)**:
   Todos os cards, botões, modais e containers devem herdar a mesma fonte de iluminação zenital. Proibido aplicar sombras laterais ou luzes invertidas que quebrem a percepção de uma bancada física iluminada de cima.
2. **Dupla Borda com Highlight Especular**:
   Nunca aplique um `border: 1px solid #333` plano. Use o padrão composto: `border: 1px solid rgba(255, 255, 255, 0.08)` complementado por `box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.16)` no topo.
3. **Aninhamento Matemático de Cantos Arredondados**:
   O raio de curvatura de elementos filhos aninhados deve seguir a fórmula de concentricidade ótica:
   $$\text{Raio}_{\text{filho}} = \text{Raio}_{\text{pai}} - \text{Padding}$$
   Exemplo: Se o card pai possui `rounded-[16px]` e `p-2` (8px), o elemento filho interno deve ter impreterivelmente `rounded-[8px]`. Cantos concêntricos errados destroem imediatamente a autenticidade do High-Craft.
4. **Reserva Proporcional de Showstoppers (10%)**:
   Limite o uso de shaders WebGL pesados (como o *Rift Stone* do GetLayers) a **uma única âncora visual por viewport**. O restante da página deve ser sustentado pela sobriedade instrumental dos Bento Cards e da tipografia tabular.
5. **Acessibilidade e Fallbacks**:
   Garanta que todo texto sobre superfícies com gradientes ou iluminação radial mantenha contraste mínimo de **4.5:1** contra o fundo de canvas. Em dispositivos com `prefers-reduced-motion: reduce`, desative as rotações contínuas de shaders e reduza os springs para crossfades opacos de 100ms.
