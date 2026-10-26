---
id: "framer-gallery"
name: "Framer Gallery"
url: "https://www.framer.com/gallery/"
category: "6-templates"
schema_type: "C-galleries"
dna_estetico: ["Modern Web Craft", "Kinetic Spring Micro-Interactions", "Fluid Viewport Transitions", "Editorial Typography Contrast", "Bento Grid Modularity", "Dark & Light Glassmorphism", "Designer-Developer Convergence"]
densidade_informacao: "Media/Narrativa"
impacto_visual: "Editorial/Sofisticado"
custo_computacional: "Medio (CSS Transforms & Spring Physics) a Alto (Loops Mux/Video & Canvas WebGL)"
stack_frameworks: ["React", "Framer Motion / Motion.dev", "Next.js", "Tailwind CSS", "Vercel Edge", "Mux Video", "Lucide Icons", "Radix UI"]
compatibilidade:
  fontes_ideais: ["Inter", "Plus Jakarta Sans", "Syne", "Cabinet Grotesk", "Clash Display", "Geist Sans", "Satoshi", "Instrument Serif"]
  paletas_ideais:
    - "Dark Craft Canvas: #050505 a #0d0d11 com elevações de cartão #141418 e #1c1c24"
    - "Pure Light Editorial: #ffffff a #f7f7f8 com cartões #ffffff e bordas #e5e5ea"
    - "Micro-Bordas Biseladas: rgba(255, 255, 255, 0.08) em dark / rgba(0, 0, 0, 0.06) em light"
    - "Acentos Vibrantes Framer: #0055ff (Electric Blue), #ff3366 (Framer Berry), #ff9900 (Amber Glow)"
    - "Gradientes de Mesh Suave: radial-gradient de iluminação volumétrica com blur de 60px a 120px"
  combinacoes_recomendadas:
    - "Motion.dev (Framer Motion v11/v12) + Tailwind CSS para orquestração de transições sem reflow de layout"
    - "Lenis Smooth Scroll + Framer Motion Scroll Hooks (`useScroll`, `useTransform`) para animações vinculadas à rolagem"
    - "Mux Animated WebP / H.264 mp4 loops para hero previews de alto framerate com lazy loading e shimmer placeholder"
    - "Radix UI Primitives + Lucide React para dropdowns acessíveis, tooltips e segmented controls"
  conflitos_esteticos:
    - "Animações lineares sem curvas de desaceleração (cubic-bezier exponencial) ou molas sem amortecimento crítico"
    - "Scroll hijacking agressivo que bloqueia a inércia nativa do trackpad e mouse wheel"
    - "Bordas sólidas espessas (>1.5px) com cores saturadas que destroem o refinamento artesanal de 1px"
    - "Saturação excessiva de efeitos concorrentes (blur + tilt + 3D + marquee simultâneos) gerando fadiga cognitiva"
    - "Desconsideração de preferências de redução de movimento (`prefers-reduced-motion: reduce`)"
---

# Framer Gallery — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
 ███████╗██████╗  █████╗ ███╗   ███╗███████╗██████╗      ██████╗  █████╗ ██╗     ██╗     ███████╗██████╗ ██╗   ██╗
 ██╔════╝██╔══██╗██╔══██╗████╗ ████║██╔════╝██╔══██╗    ██╔════╝ ██╔══██╗██║     ██║     ██╔════╝██╔══██╗╚██╗ ██╔╝
 █████╗  ██████╔╝███████║██╔████╔██║█████╗  ██████╔╝    ██║  ███╗███████║██║     ██║     █████╗  ██████╔╝ ╚████╔╝ 
 ██╔══╝  ██╔══██╗██╔══██║██║╚██╔╝██║██╔══╝  ██╔══██╗    ██║   ██║██╔══██║██║     ██║     ██╔══╝  ██╔══██╗  ╚██╔╝  
 ██║     ██║  ██║██║  ██║██║ ╚═╝ ██║███████╗██║  ██║    ╚██████╔╝██║  ██║███████╗███████╗███████╗██║  ██║   ██║   
 ╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝╚═╝     ╚═╝╚══════╝╚═╝  ╚═╝     ╚═════╝ ╚═╝  ╚═╝╚══════╝╚══════╝╚══════╝╚═╝  ╚═╝   ╚═╝   
```

## 1. DNA Estético & Filosofia de Curadoria

O **Framer Gallery** (`https://www.framer.com/gallery/` ou `/community/gallery/`) representa o epicentro contemporâneo do que se consolidou na indústria como **"Web Craft"**: a transição definitiva de websites estáticos convencionais para superfícies digitais imersivas, altamente cinéticas e visualmente sofisticadas. Mantido e curado diretamente pela equipe de design da **Framer** (liderada conceitualmente pelos fundadores Koen Bok e Jorn van Dijk, juntamente com o criador do motor de física Matt Perry), o portal funciona simultaneamente como vitrine de elite, benchmarking de performance e motor de inspiração viva para designers de produto, engenheiros de frontend e diretores de arte em todo o mundo.

Diferente de agregadores generalistas ou galerias baseadas exclusivamente em capturas de tela congeladas (screenshots PNG estáticos), o Framer Gallery é um showcase de **sites vivos e operacionais em produção**. Cada projeto listado é submetido pela comunidade de criadores globais, passa por um rigoroso crivo editorial e técnico, e permite acesso imediato tanto à URL em tempo real quanto aos templates duplicáveis (*Remix links*).

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                    THE FRAMER GALLERY CURATION ECOSYSTEM                     │
├──────────────────────────────────────────────────────────────────────────────┤
│  [ Creator Submissions ] ──► [ Curatorial Quality Gate ] ──► [ Framer Gallery]│
│   • Global Studios             • Spatial Rhythm & Layout      • Trending / New│
│   • SaaS Startups              • Spring Physics Naturalness   • Vibe Engine   │
│   • Independent Designers      • Typographic Rigor (Contrast) • Category Tree │
│   • Template Creators          • Zero-CLS Responsive Polish   • Framer Awards │
├──────────────────────────────────────────────────────────────────────────────┤
│  OUTPUT: Live Production Sites + Duplicable Templates + Engineering Blueprints│
└──────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 Critérios de Curadoria & Identidade de Marca
A curadoria do Framer Gallery apoia-se em cinco dimensões estéticas e operacionais fundamentais:

1. **Física de Mola Natural (*True Spring Physics*)**: Nenhum movimento na galeria se comporta com interpolações lineares mecânicas (`linear`) ou acelerações abruptas. Todas as transições de microinteração (hover em cartões, revelação de acordeões, modais e tooltips) espelham a elasticidade orgânica do mundo real, parametrizadas através de rigidez (*stiffness*) e amortecimento (*damping*).
2. **Harmonia de Espaço Negativo & Grid Invisível**: A galeria celebra a tipografia helvética/grotesca contemporânea com contrastes dramáticos entre títulos monumentais e micro-legendas técnicas, estruturados por sistemas de auto-layout e bento grids modulares com margens milimetricamente calculadas.
3. **Bisel de Precisão & Iluminação Direcional**: Tanto no modo escuro (*Dark Craft*) quanto no modo claro (*Swiss Precision*), as superfícies não utilizam sombras difusas antiquadas; em seu lugar, adotam linhas divisórias de `1px` com gradientes alfa (`rgba(255, 255, 255, 0.08)` a `0.15`) que simulam a refração de luz em bordas de vidro usinado ou alumínio aeroespacial.
4. **Mídia Fluida com Streaming de Baixa Latência**: A navegação pelo catálogo combina imagens WebP de altíssima densidade de pixels com loops de vídeo silenciosos em streaming dinâmico via infraestrutura **Mux Video**, viabilizando pré-visualizações ricas sem atraso de renderização.
5. **Classificação Multidimensional (Indústria + "Vibe")**: Em sua atualização mais recente, a galeria adicionou o filtro por **"Vibe"** (Dark & Moody, Editorial, Minimalist, Playful, Brutalist, High-Tech SaaS), permitindo que designers pesquisem não apenas pela função prática do produto (ex: Fintech, Portfólio, AI), mas pela ressonância emocional e tom artístico da interface.

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

### 2.1 Papel na Regra 60-30-10 de Design & Movimento
O catálogo do Framer Gallery é a maior autoridade mundial na execução equilibrada da regra áurea de design visual e movimento:

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                 60-30-10 ARCHITECTURAL BALANCE (FRAMER CRAFT)                │
├──────────────────────────────────────────────────────────────────────────────┤
│  60%  TELA ESTRUTURAL & ESPAÇO RESPIRÁVEL (The Canvas Substrate)             │
│       Fundos neutros profundos (#050505 a #0d0d11 ou #ffffff a #f7f7f8),     │
│       grid modular ortogonal, tipografia primária limpa (Inter/Geist/Satoshi).│
├──────────────────────────────────────────────────────────────────────────────┤
│  30%  SURFÁCIES TÁTEIS & MICRO-BISEL (Modular Precision)                     │
│       Bento cards modulares, divisórias de 1px translúcidas, dock flutuante  │
│       com backdrop-blur, tags monocromáticas e botões secundários sóbrios.    │
├──────────────────────────────────────────────────────────────────────────────┤
│  10%  O IMPACTO CINÉTICO DE ASSINATURA (Kinetic Delight & Accents)           │
│       Acentos de cor intensos (#0055ff, #ff3366, #ff9900), cursor follower,   │
│       scroll-driven sticky cards, tipografia cinética com split-text e molas.│
└──────────────────────────────────────────────────────────────────────────────┘
```

- **60% da Interface (Substrato Estrutural)**: O fundo atua como palco silencioso. Seja no dark mode profundo ou no light mode editorial, a ausência de texturas caóticas permite que o conteúdo e os produtos sejam os protagonistas absolutos.
- **30% da Interface (Superfícies & Cartões Modulares)**: Cartões com cantos arredondados generosos (`rounded-2xl` a `rounded-3xl`), pílulas de navegação segmentadas com bordas de dupla densidade e containers com desfoque de fundo (`backdrop-filter: blur(16px)`).
- **10% da Interface (Assinatura Cinética & Acentos de Cor)**: O toque inesquecível de sofisticação: botões magnéticos que atraem o cursor, transições elásticas de seleção de abas (`layoutId`), títulos com máscara de revelação progressiva e acentos de cores puras da paleta Framer.

### 2.2 Nichos de Projeto Ideais
- **Startups de IA, Ferramentas Criativas & DevTools**: Plataformas que precisam demonstrar excelência técnica, velocidade e refinamento de produto logo no primeiro viewport.
- **Portfólios de Diretores de Arte & Designers de Produto**: Profissionais que competem no mercado internacional de alto nível e necessitam de uma vitrine com padrão de premiação (Framer Awards, Awwwards Site of the Day).
- **Agências Digitais & Estúdios de Branding**: Empresas que vendem soluções criativas e usam seu próprio site como prova inequívoca de domínio técnico e refinamento tipográfico.
- **SaaS B2B de Próxima Geração**: Produtos de software corporativo moderno (estilo Linear, Raycast, Supabase, Vercel) que buscam fugir da mesmice dos templates corporativos antiquados.
- **Marcas de Moda, Arquitetura & Produtos de Luxo**: Marcas que exigem um layout editorial contemplativo, com imagens em grande formato e tipografia refinada.

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

### 3.1 ⚠️ Setores Incompatíveis
- **ERPs Corporativos de Alta Densidade Numérica & Finanças Transacionais**: Telas operacionais que exibem tabelas com 50+ colunas e milhares de registros por visualização não se beneficiam de cantos hiper-arredondados (`rounded-3xl`), animações de entrada elásticas ou espaçamentos verticais dilatados.
- **Portais Governamentais & Serviços Públicos Universais**: Interfaces públicas que exigem suporte a navegadores legados, conexões de banda ultralimitada e conformidade estrita com padrões WCAG AAA não devem adotar microinterações que dependem de hardware acceleration intensivo.
- **Grandes Varejistas / E-commerce de Massa (Multi-SKU)**: Lojas virtuais com milhões de itens (como marketplaces de eletrônicos ou supermercados) dependem de densidade máxima de inventário por pixel e carregamento instantâneo sem efeitos visuais ricos.

### 3.2 ⚠️ Armadilhas de Imitação Comuns
1. **Fadiga de Movimento (*Motion Fatigue*)**: Animar todos os elementos da página simultaneamente. Quando títulos, cards, imagens e ícones se movem o tempo todo, o olho humano perde o ponto focal e a usabilidade é arruinada.
2. **Scroll Hijacking Agressivo**: Substituir o comportamento de rolagem nativo do sistema operacional por scripts pesados de rolagem forçada, gerando atraso de resposta (*input lag*) e frustração imediata no usuário.
3. **Abuso de Blur & Filtros de Backdrop**: Empilhar múltiplas camadas com `backdrop-filter: blur(24px)` e sombras complexas em telas mobile de entrada, causando queda severa de framerate (< 30fps) e consumo excessivo de bateria.
4. **Quebra de Acessibilidade em Hover**: Ocultar informações críticas (como preços, especificações ou botões primários) exclusivamente atrás de estados de `:hover`, tornando o site inoperável em dispositivos móveis touch-screen.
5. **Inobservância de `prefers-reduced-motion`**: Ignorar a diretiva de acessibilidade para usuários propensos a náuseas e distúrbios vestibulares, deixando de desligar ou atenuar molas e transições contínuas.

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                 FRAMER GALLERY SHOWCASE STRUCTURAL ANATOMY                   │
├──────────────────────────────────────────────────────────────────────────────┤
│ [ HEADER: Global Sticky Pill Nav / Framer Logo / Direct Links / CTA Launch ] │
│                                                                              │
│ [ HERO MASTHEAD: Title "Gallery" / Editorial Subtitle / Submission Counter ] │
│                                                                              │
│ [ DIRECTORY TREE BAR: Group Categories (Business / Agency / Software / etc.)]│
│                                                                              │
│ [ CONTROL DOCK: Sorting Tabs (Trending / Recent) ────► Vibe Dropdown Filter ]│
│                                                                              │
│ [ VIRTUALIZED CARD GRID: 3-Column Responsive Canvas (Desktop) ]              │
│   ├── Interactive Media Container (Mux Stream / WebP / Shimmer Skeleton)    │
│   ├── Card Footer: Site Title + Creator Subline + Floating Action Pill       │
│   └── Hover Lift State with Spring Damping & Soft Glow Border                │
│                                                                              │
│ [ SHOWCASE FOOTER: Editorial Directory, Community Links & Copyright Notice ] │
└──────────────────────────────────────────────────────────────────────────────┘
```

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo
- **Grid Virtualizado Responsivo**: Layout ortogonal estruturado em colunas modulares com transição fluida:
  - Mobile: 1 coluna com espaçamento vertical de `20px` e horizontal de `15px` (`--virtual-grid-mobile-row-gap: 20px`).
  - Tablet: 2 colunas proporcionais com gap de `24px`.
  - Desktop: 3 colunas balanceadas com gap horizontal de `32px` e vertical de `40px` para telas de alta resolução (`max-w-[1400px]`).
- **Aspect Ratio Imersivo de Card**: Os cartões de exibição adotam preferencialmente proporções cinematográficas de `16:10` ou `4:3`, garantindo que o viewport do site catalogado apareça completo, sem distorção ou cortes indevidos.
- **Hierarquia Tipográfica Suíça**: Emprego de títulos condensados ou sans-serif com tracking sutilmente negativo (`tracking-[-0.03em]`), contrastando com legendas em fontes monoespaçadas com tracking aberto (`tracking-wider` de `0.05em`) para dados técnicos e autoria.
- **Margens de Respiro (*Breathing Room*)**: Blocos de introdução e seções com espaçamentos verticais generosos (`py-20` a `py-32`), criando um ritmo contemplativo que prepara a mente do visitante para avaliar o design com calma.

### 4.2 Sistemas de Cores, Superfícies & Texturas
- **Fundo do Canvas Primário**: `#050505` ou `#0a0a0c` no modo escuro; `#ffffff` com tonalidades quentes sutis (`#fbfbfa`) no modo claro.
- **Cartões & Superfícies**: Fundo `#121216` com opacidade calibrada (`bg-zinc-900/60` ou `rgba(18, 18, 22, 0.7)`), reforçado por desfoque ótico (`backdrop-blur-md`).
- **Micro-Bisel de Borda**: Aplicação sistemática de bordas de 1px com gradiente translúcido:
  - Topo: `border-t: 1px solid rgba(255, 255, 255, 0.12)` (ponto de incidência de luz zenital).
  - Laterais e Base: `border: 1px solid rgba(255, 255, 255, 0.05)`.
- **Efeito Shimmer de Carregamento**: Gradiente linear animado em tons de cinza escuro (`linear-gradient(90deg, #18181b 0%, #27272a 50%, #18181b 100%)`) que desliza horizontalmente até que o streaming de mídia seja estabilizado.

---

### 4.3 Catálogo Detalhado de Componentes / Padrões Notáveis

Abaixo estão os 10 padrões de componentes mais expressivos e recorrentes extraídos diretamente da curadoria do Framer Gallery:

| # | Arquétipo / Componente | Anatomia & Comportamento | Gatilho & Física de Interação | Onde Encaixar no Projeto |
|---|------------------------|--------------------------|--------------------------------|--------------------------|
| 1 | **Floating Island Header (Pill Nav)** | Barra em formato de pílula flutuante suspensa no topo com backdrop-blur de 16px, borda de 1px biselada e logotipo integrado. | Scroll down oculta ou recolhe a navegação; scroll up restaura a barra com spring elástica (`stiffness: 400, damping: 30`). | Navegação global de qualquer website de alto padrão ou portfólio. |
| 2 | **Directory Category Ribbon** | Menu horizontal segmentado por grupos de indústria (Business, Agency, Software, Portfolio) com subcategorias acessíveis. | Hover expande dropdown flutuante; clique filtra o grid sem recarregamento de página. | Cabeçalho de galerias, seções de documentação ou índices de blog. |
| 3 | **Segmented Control Tabs (Trending/Recent)** | Contêiner em cápsula oval contendo botões de estado binário com fundo deslizante animado via `layoutId`. | Clique transiciona o indicador de seleção através de física de mola sem qualquer salto visual (FLIP transition). | Barra de ferramentas de controle, seletores de filtros ou planos de faturamento. |
| 4 | **Showcase Media Card with Shimmer & Video Stream** | Cartão modular composto por thumbnail WebP de alta definição que transita suavemente para loop de vídeo Mux após hover. | Hover com mola eleva o cartão em `-4px`, intensifica a borda translúcida e dispara o vídeo silencioso. | Vitrine principal de portfólios, galeria de produtos e estudos de caso. |
| 5 | **Sticky Stacking Cards (Scroll Reveal)** | Conjunto de seções empilhadas verticalmente que fixam no topo do viewport (`sticky top-24`) e diminuem de escala gradualmente conforme a próxima seção sobe. | Vinculado à porcentagem de scroll do viewport (`useScroll` + `useTransform` com escala de `1` para `0.92`). | Seções de features principais, depoimentos ou passos de produto. |
| 6 | **Magnetic Spring Button** | Botão interativo que se desloca fisicamente em direção às coordenadas do cursor do mouse quando o ponteiro se aproxima do seu raio de atração. | Movimento com mola suave (`stiffness: 250, damping: 15`), retornando à posição zero no `onMouseLeave`. | Botões primários de chamada para ação (CTA), links de contato ou botões de compra. |
| 7 | **Vibe Dropdown Filter Pill** | Botão compacto com ícone de filtro e texto "Vibe" acompanhado de caret animado que abre um menu popover suspenso com chips visuais. | Clique dispara transição de escala de entrada (`scale: 0.95 -> 1.0, opacity: 0 -> 1`) com física out-back. | Barra de ferramentas de busca rápida em catálogos e filtros dinâmicos. |
| 8 | **Split-Text Heading Reveal** | Título monumental onde cada palavra ou linha está envolvida por uma máscara (`overflow: hidden`), subindo de baixo para cima. | Gatilho de scroll viewport (`whileInView`) com transição stagger de `0.04s` entre palavras e curva cúbica exponencial. | Hero Sections e cabeçalhos de capítulos em páginas institucionais. |
| 9 | **Interactive Bento Spec Sheet Card** | Cartão bento assimétrico com dados técnicos, badges monocromáticos e gráficos vetoriais com animação de traço (`pathLength: 0 -> 1`). | Entra em visualização ativando a renderização progressiva dos elementos internos. | Seções de especificações técnicas, comparativos e métricas de desempenho. |
| 10 | **Monochrome Studio Footer** | Rodapé editorial silencioso com grid de 4 colunas, tipografia de baixo contraste (`text-zinc-500` para `text-zinc-100` em hover) e carimbo de direitos autorais. | Hover sutil sobre links com transição de opacidade de `150ms`. | Fechamento institucional de sites premium e landing pages. |

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Tokens CSS & Variáveis de Assinatura
O trecho abaixo estabelece a base de variáveis necessárias para replicar fielmente a estética do Framer Gallery no ecossistema de desenvolvimento contemporâneo:

```css
:root {
  /* Canvas Substrate */
  --fg-bg-canvas: #08080a;
  --fg-bg-surface: #121216;
  --fg-bg-card: #18181e;
  --fg-bg-pill: #1f1f26;

  /* Bisel & Micro-Bordas */
  --fg-border-dim: rgba(255, 255, 255, 0.07);
  --fg-border-medium: rgba(255, 255, 255, 0.12);
  --fg-border-highlight: rgba(255, 255, 255, 0.22);
  --fg-border-light-mode: rgba(0, 0, 0, 0.08);

  /* Acentos Framer */
  --fg-accent-blue: #0055ff;
  --fg-accent-berry: #ff3366;
  --fg-accent-amber: #ff9900;

  /* Tipografia */
  --fg-text-primary: #f5f5f7;
  --fg-text-secondary: #a1a1aa;
  --fg-text-muted: #71717a;

  /* Sombras & Profundidade */
  --fg-shadow-card: 0 10px 30px -10px rgba(0, 0, 0, 0.6);
  --fg-shadow-hover: 0 20px 40px -15px rgba(0, 85, 255, 0.15);
}

/* Utilitários de Mídia e Shimmer */
@keyframes fgShimmer {
  0% {
    background-position: -200% 0;
  }
  100% {
    background-position: 200% 0;
  }
}

.fg-shimmer {
  background: linear-gradient(
    90deg,
    rgba(255, 255, 255, 0.03) 0%,
    rgba(255, 255, 255, 0.08) 50%,
    rgba(255, 255, 255, 0.03) 100%
  );
  background-size: 200% 100%;
  animation: fgShimmer 2s infinite ease-in-out;
}
```

### 5.2 Física de Movimento & Transições
- **Curva de Easing Primária (Exponential Out)**: `cubic-bezier(0.16, 1, 0.3, 1)` — Ideal para transições de layout, abertura de gavetas e modais.
- **Configuração de Mola Tátil Primária (Cartões & Controles)**:
  - `stiffness: 380`, `damping: 30`, `mass: 0.8` (Resposta rápida, firme e sem oscilações excessivas).
- **Configuração de Mola Orgânica (Hover & Seleção)**:
  - `stiffness: 450`, `damping: 35`, `mass: 1.0` (Sensação elástica e imediata para abas e botões).
- **Transição de Layout FLIP**:
  - `transition={{ type: "spring", stiffness: 500, damping: 40 }}`.

---

### 5.3 Implementação Funcional Completa em React + Tailwind + Framer Motion

O componente a seguir reproduz a experiência completa do **Framer Gallery Showcase**: a barra de navegação em ilha flutuante, o diretório de categorias, as abas de ordenação com mola FLIP, o filtro dinâmico de "Vibe" e o grid responsivo de cartões com preview de mídia, shimmer e botão externo com feedback imediato:

```tsx
import React, { useState } from "react";
import { motion, AnimatePresence } from "framer-motion";
import {
  ExternalLink,
  Sparkles,
  SlidersHorizontal,
  ChevronDown,
  Layers,
  ArrowUpRight,
  TrendingUp,
  Clock,
  Check
} from "lucide-react";

// Tipos estruturais da Galeria
export type GalleryCategory = "All" | "Software" | "Agency" | "Portfolio" | "Ecommerce";
export type GalleryVibe = "All Vibes" | "Dark & Moody" | "Editorial" | "Minimalist" | "High-Tech SaaS";
export type SortOption = "Trending" | "Recent";

export interface GalleryItem {
  id: string;
  title: string;
  creator: string;
  category: GalleryCategory;
  vibe: GalleryVibe;
  url: string;
  imageThumbnail: string;
  videoPreviewUrl?: string;
  badge?: string;
  views: string;
}

// Dados realistas inspirados na curadoria oficial da Framer
const SAMPLE_GALLERY_ITEMS: GalleryItem[] = [
  {
    id: "torso-electronics",
    title: "Torso Electronics",
    creator: "Torso Design Lab",
    category: "Software",
    vibe: "High-Tech SaaS",
    url: "https://torsoelectronics.com/",
    imageThumbnail: "https://images.unsplash.com/photo-1550745165-9bc0b252726f?auto=format&fit=crop&w=800&q=80",
    badge: "Framer Award Winner",
    views: "24.8k"
  },
  {
    id: "studio-noun",
    title: "Studio Noun",
    creator: "Noun Studio Amsterdam",
    category: "Agency",
    vibe: "Editorial",
    url: "https://studionoun.com/",
    imageThumbnail: "https://images.unsplash.com/photo-1507238691740-187a5b1d37b8?auto=format&fit=crop&w=800&q=80",
    badge: "Site of the Month",
    views: "18.2k"
  },
  {
    id: "jason-ng",
    title: "Jason Ng Portfolio",
    creator: "Jason Nguyen",
    category: "Portfolio",
    vibe: "Dark & Moody",
    url: "https://jason-ng.space/",
    imageThumbnail: "https://images.unsplash.com/photo-1518770660439-4636190af475?auto=format&fit=crop&w=800&q=80",
    views: "31.4k"
  },
  {
    id: "finite-os",
    title: "Finite OS",
    creator: "Finite Labs Zurich",
    category: "Software",
    vibe: "High-Tech SaaS",
    url: "https://finite.design/",
    imageThumbnail: "https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?auto=format&fit=crop&w=800&q=80",
    badge: "Featured",
    views: "15.9k"
  },
  {
    id: "plein-produce",
    title: "Plein Produce Co.",
    creator: "Bureau Plein",
    category: "Ecommerce",
    vibe: "Minimalist",
    url: "https://pleinproduce.com/",
    imageThumbnail: "https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=800&q=80",
    views: "12.7k"
  },
  {
    id: "kogaa-architecture",
    title: "KOGAA Urban Design",
    creator: "Stepan Osada",
    category: "Agency",
    vibe: "Editorial",
    url: "https://kogaa.eu/",
    imageThumbnail: "https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?auto=format&fit=crop&w=800&q=80",
    views: "21.1k"
  }
];

export const FramerGalleryShowcase: React.FC = () => {
  const [selectedCategory, setSelectedCategory] = useState<GalleryCategory>("All");
  const [selectedVibe, setSelectedVibe] = useState<GalleryVibe>("All Vibes");
  const [currentSort, setCurrentSort] = useState<SortOption>("Trending");
  const [isVibeMenuOpen, setIsVibeMenuOpen] = useState(false);
  const [hoveredCardId, setHoveredCardId] = useState<string | null>(null);

  // Lista de categorias principais
  const categories: GalleryCategory[] = ["All", "Software", "Agency", "Portfolio", "Ecommerce"];
  
  // Lista de Vibes estéticos
  const vibes: GalleryVibe[] = [
    "All Vibes",
    "Dark & Moody",
    "Editorial",
    "Minimalist",
    "High-Tech SaaS"
  ];

  // Filtragem combinada
  const filteredItems = SAMPLE_GALLERY_ITEMS.filter((item) => {
    const matchesCategory = selectedCategory === "All" || item.category === selectedCategory;
    const matchesVibe = selectedVibe === "All Vibes" || item.vibe === selectedVibe;
    return matchesCategory && matchesVibe;
  });

  return (
    <div className="min-h-screen bg-[#070709] text-zinc-100 selection:bg-[#0055ff] selection:text-white font-sans antialiased">
      {/* 1. Header Flutuante em Cápsula (Framer Signature Floating Nav) */}
      <header className="sticky top-4 z-50 max-w-5xl mx-auto px-4">
        <nav className="relative flex items-center justify-between px-5 py-3 rounded-full bg-[#111116]/80 backdrop-blur-xl border border-white/[0.08] shadow-[0_8px_32px_rgba(0,0,0,0.5)]">
          <div className="flex items-center gap-3">
            <div className="w-8 h-8 rounded-lg bg-[#0055ff] flex items-center justify-center font-black text-white text-sm tracking-tighter shadow-sm">
              F
            </div>
            <div className="flex flex-col">
              <span className="text-sm font-semibold tracking-tight text-white flex items-center gap-1.5">
                Framer Gallery
                <span className="text-[10px] font-mono uppercase px-1.5 py-0.5 rounded-full bg-white/[0.08] text-zinc-300">
                  Showcase
                </span>
              </span>
            </div>
          </div>

          <div className="hidden md:flex items-center gap-6 text-xs text-zinc-400 font-medium">
            <a href="#browse" className="hover:text-white transition-colors">Explorar</a>
            <a href="#awards" className="hover:text-white transition-colors">Prêmios & Destaques</a>
            <a href="#templates" className="hover:text-white transition-colors">Templates Oficiais</a>
          </div>

          <div className="flex items-center gap-2">
            <a
              href="https://www.framer.com/community/gallery/"
              target="_blank"
              rel="noreferrer"
              className="inline-flex items-center gap-1.5 px-3.5 py-1.5 rounded-full bg-white text-zinc-900 font-medium text-xs hover:bg-zinc-200 transition-colors shadow-sm"
            >
              <span>Submeter Site</span>
              <ArrowUpRight className="w-3.5 h-3.5" />
            </a>
          </div>
        </nav>
      </header>

      {/* 2. Hero Masthead Editorial */}
      <section className="pt-24 pb-12 px-6 max-w-6xl mx-auto text-center">
        <motion.div
          initial={{ opacity: 0, y: 15 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.6, ease: [0.16, 1, 0.3, 1] }}
          className="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-white/[0.04] border border-white/[0.08] text-xs text-zinc-400 mb-6"
        >
          <Sparkles className="w-3.5 h-3.5 text-[#0055ff]" />
          <span>Curadoria Viva dos Melhores Sites Feitos no Framer</span>
        </motion.div>

        <motion.h1
          initial={{ opacity: 0, y: 20 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.7, ease: [0.16, 1, 0.3, 1], delay: 0.1 }}
          className="text-4xl sm:text-6xl md:text-7xl font-extrabold tracking-[-0.04em] text-white max-w-3xl mx-auto leading-[1.08]"
        >
          Design sem limites. <br />
          <span className="text-transparent bg-clip-text bg-gradient-to-r from-zinc-200 via-zinc-400 to-zinc-600">
            Executado no Canvas.
          </span>
        </motion.h1>

        <motion.p
          initial={{ opacity: 0, y: 20 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.7, ease: [0.16, 1, 0.3, 1], delay: 0.2 }}
          className="mt-6 text-sm sm:text-base text-zinc-400 max-w-xl mx-auto leading-relaxed"
        >
          Explore produções reais de estúdios globais, interações com física de mola e arquiteturas
          visuais premiadas criadas diretamente na plataforma.
        </motion.p>
      </section>

      {/* 3. Barra de Controles, Categorias & Vibe Filters */}
      <section className="sticky top-20 z-40 bg-[#070709]/90 backdrop-blur-xl border-y border-white/[0.06] py-3 px-6">
        <div className="max-w-6xl mx-auto flex flex-col md:flex-row items-center justify-between gap-4">
          
          {/* Segmented Category Buttons */}
          <div className="flex items-center gap-1.5 overflow-x-auto w-full md:w-auto pb-1 md:pb-0 scrollbar-none">
            {categories.map((cat) => {
              const isActive = selectedCategory === cat;
              return (
                <button
                  key={cat}
                  onClick={() => setSelectedCategory(cat)}
                  className={`relative px-3.5 py-1.5 rounded-full text-xs font-medium transition-colors ${
                    isActive ? "text-white" : "text-zinc-400 hover:text-zinc-200"
                  }`}
                >
                  {isActive && (
                    <motion.div
                      layoutId="activeCategoryPill"
                      transition={{ type: "spring", stiffness: 450, damping: 35 }}
                      className="absolute inset-0 rounded-full bg-white/[0.12] border border-white/[0.15]"
                    />
                  )}
                  <span className="relative z-10">{cat}</span>
                </button>
              );
            })}
          </div>

          {/* Ferramentas de Ordenação & Vibe Filter */}
          <div className="flex items-center gap-3 w-full md:w-auto justify-end">
            {/* Sorting Tabs (Trending / Recent) */}
            <div className="flex items-center p-0.5 rounded-full bg-zinc-900 border border-white/[0.08]">
              <button
                onClick={() => setCurrentSort("Trending")}
                className={`flex items-center gap-1 px-3 py-1 rounded-full text-[11px] font-medium transition-colors ${
                  currentSort === "Trending"
                    ? "bg-[#1d1d24] text-white shadow-sm"
                    : "text-zinc-400 hover:text-zinc-200"
                }`}
              >
                <TrendingUp className="w-3 h-3 text-[#0055ff]" />
                <span>Trending</span>
              </button>
              <button
                onClick={() => setCurrentSort("Recent")}
                className={`flex items-center gap-1 px-3 py-1 rounded-full text-[11px] font-medium transition-colors ${
                  currentSort === "Recent"
                    ? "bg-[#1d1d24] text-white shadow-sm"
                    : "text-zinc-400 hover:text-zinc-200"
                }`}
              >
                <Clock className="w-3 h-3 text-zinc-400" />
                <span>Recent</span>
              </button>
            </div>

            {/* Vibe Dropdown Button */}
            <div className="relative">
              <button
                onClick={() => setIsVibeMenuOpen(!isVibeMenuOpen)}
                className="flex items-center gap-1.5 px-3 py-1.5 rounded-full bg-zinc-900 hover:bg-zinc-800 border border-white/[0.08] text-xs font-medium text-zinc-300 transition-colors"
              >
                <SlidersHorizontal className="w-3 h-3 text-[#0055ff]" />
                <span>{selectedVibe === "All Vibes" ? "Vibe" : selectedVibe}</span>
                <ChevronDown className="w-3 h-3 text-zinc-400" />
              </button>

              <AnimatePresence>
                {isVibeMenuOpen && (
                  <motion.div
                    initial={{ opacity: 0, scale: 0.95, y: 8 }}
                    animate={{ opacity: 1, scale: 1, y: 0 }}
                    exit={{ opacity: 0, scale: 0.95, y: 8 }}
                    transition={{ type: "spring", stiffness: 450, damping: 30 }}
                    className="absolute right-0 mt-2 w-48 rounded-2xl bg-[#141419] border border-white/[0.12] p-1.5 shadow-[0_12px_36px_rgba(0,0,0,0.8)] z-50 backdrop-blur-2xl"
                  >
                    <div className="px-2 py-1.5 text-[10px] font-mono uppercase tracking-wider text-zinc-500">
                      Filtrar por Vibe
                    </div>
                    {vibes.map((vibe) => (
                      <button
                        key={vibe}
                        onClick={() => {
                          setSelectedVibe(vibe);
                          setIsVibeMenuOpen(false);
                        }}
                        className={`w-full flex items-center justify-between px-2.5 py-1.5 rounded-lg text-xs font-medium text-left transition-colors ${
                          selectedVibe === vibe
                            ? "bg-white/[0.08] text-white"
                            : "text-zinc-400 hover:text-white hover:bg-white/[0.04]"
                        }`}
                      >
                        <span>{vibe}</span>
                        {selectedVibe === vibe && <Check className="w-3.5 h-3.5 text-[#0055ff]" />}
                      </button>
                    ))}
                  </motion.div>
                )}
              </AnimatePresence>
            </div>
          </div>
        </div>
      </section>

      {/* 4. Grid de Cartões da Galeria com Spring Hover & Badges */}
      <main className="max-w-6xl mx-auto px-6 py-10" id="browse">
        {filteredItems.length === 0 ? (
          <div className="py-20 text-center">
            <Layers className="w-10 h-10 text-zinc-600 mx-auto mb-3" />
            <p className="text-zinc-400 text-sm">Nenhum projeto encontrado para os filtros selecionados.</p>
            <button
              onClick={() => {
                setSelectedCategory("All");
                setSelectedVibe("All Vibes");
              }}
              className="mt-4 text-xs font-medium text-[#0055ff] hover:underline"
            >
              Resetar filtros
            </button>
          </div>
        ) : (
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            {filteredItems.map((item) => {
              const isHovered = hoveredCardId === item.id;
              return (
                <motion.article
                  key={item.id}
                  onHoverStart={() => setHoveredCardId(item.id)}
                  onHoverEnd={() => setHoveredCardId(null)}
                  whileHover={{ y: -4 }}
                  transition={{ type: "spring", stiffness: 380, damping: 25 }}
                  className="group relative flex flex-col rounded-3xl bg-[#121217]/70 border border-white/[0.08] hover:border-white/[0.2] overflow-hidden transition-colors shadow-sm"
                >
                  {/* Container de Mídia e Imagem */}
                  <div className="relative aspect-[16/10] w-full bg-zinc-900 overflow-hidden">
                    <img
                      src={item.imageThumbnail}
                      alt={item.title}
                      className="w-full h-full object-cover transition-transform duration-500 ease-out group-hover:scale-105"
                      loading="lazy"
                    />

                    {/* Gradient Overlay */}
                    <div className="absolute inset-0 bg-gradient-to-t from-[#121217] via-transparent to-transparent opacity-60" />

                    {/* Badge de Reconhecimento (se houver) */}
                    {item.badge && (
                      <div className="absolute top-3 left-3 px-2.5 py-1 rounded-full bg-black/60 backdrop-blur-md border border-white/10 text-[10px] font-medium tracking-wide text-white">
                        {item.badge}
                      </div>
                    )}

                    {/* Badge de Vibe */}
                    <div className="absolute top-3 right-3 px-2 py-0.5 rounded-md bg-black/40 backdrop-blur-md text-[10px] font-mono text-zinc-300">
                      {item.vibe}
                    </div>
                  </div>

                  {/* Informações do Rodapé do Cartão */}
                  <div className="p-4 flex items-center justify-between">
                    <div className="min-w-0 pr-3">
                      <h3 className="font-semibold text-sm text-white group-hover:text-[#0055ff] transition-colors truncate">
                        {item.title}
                      </h3>
                      <p className="text-xs text-zinc-500 truncate mt-0.5">
                        Por <span className="text-zinc-400">{item.creator}</span>
                      </p>
                    </div>

                    <a
                      href={item.url}
                      target="_blank"
                      rel="noopener noreferrer"
                      className="flex-shrink-0 inline-flex items-center gap-1.5 px-3 py-1.5 rounded-full bg-white/[0.06] hover:bg-white text-zinc-300 hover:text-zinc-900 text-xs font-medium transition-all"
                    >
                      <span>Abrir</span>
                      <ExternalLink className="w-3 h-3" />
                    </a>
                  </div>
                </motion.article>
              );
            })}
          </div>
        )}
      </section>

      {/* 5. Footer Técnico Editorial */}
      <footer className="border-t border-white/[0.06] mt-20 py-12 px-6">
        <div className="max-w-6xl mx-auto flex flex-col md:flex-row items-center justify-between gap-6 text-xs text-zinc-500">
          <div className="flex items-center gap-2">
            <span className="w-2 h-2 rounded-full bg-emerald-500 animate-pulse" />
            <span>Framer Gallery Blueprint Specification — Engenharia de Design Systems 2026</span>
          </div>

          <div className="flex items-center gap-6">
            <a href="https://www.framer.com/gallery/" target="_blank" rel="noreferrer" className="hover:text-zinc-300 transition-colors">
              Galeria Oficial
            </a>
            <a href="https://www.framer.com/templates/" target="_blank" rel="noreferrer" className="hover:text-zinc-300 transition-colors">
              Templates & Remix
            </a>
            <a href="https://motion.dev/" target="_blank" rel="noreferrer" className="hover:text-zinc-300 transition-colors">
              Motion.dev Engine
            </a>
          </div>
        </div>
      </footer>
    </div>
  );
};

export default FramerGalleryShowcase;
```

---

### 5.4 Como a IA Deve Pesquisar ao Vivo no Framer Gallery
Quando um agente de IA ou pipeline automatizado precisar inspecionar sites de referência em tempo real no Framer Gallery, deve utilizar as rotas canônicas e parâmetros de taxonomia oficiais:

1. **Estrutura Canônica de URLs por Categoria e Subcategoria**:
   - Raiz da Galeria: `https://www.framer.com/community/gallery/`
   - Softwares & Inteligência Artificial: `https://www.framer.com/community/gallery/categories/ai/`
   - Softwares SaaS Gerais: `https://www.framer.com/community/gallery/categories/saas/`
   - Agências de Branding & Design: `https://www.framer.com/community/gallery/categories/agency/` e `/branding/`
   - Portfólios de Design: `https://www.framer.com/community/gallery/categories/portfolio-design/`
   - Arquitetura & Espaços: `https://www.framer.com/community/gallery/categories/architecture/`
2. **Parâmetros de Ordenação & Filtros**:
   - Ordenação Trending: `?sort=trending` (padrão baseado em visualizações e engajamento recente)
   - Ordenação Recentes: `?sort=recent` (ordem cronológica estrita de publicação)
   - Filtro de Vibe: `?vibe=<dark-moody | editorial | minimalist | playful | high-tech>`
3. **Seletores DOM Notáveis para Scraping/Extração Semântica**:
   - Container do Grid: `div._0a1O3q_grid` ou `div._9i8ZIW_virtualGridContainer`
   - Cartão Individual: `div.tPr4JW_tile` ou `article`
   - Título do Projeto: `span.tPr4JW_name`
   - Nome do Criador: `span.tPr4JW_resourceType`
   - Link de Pré-visualização ao Vivo: `a.tPr4JW_button[href^="http"]`
   - Elemento de Mídia Dinâmica: `video[poster*="mux.com"]` ou `img[srcset*="vercel-storage.com"]`

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao adotar o **Framer Gallery** como a referência de direção de arte para novos projetos digitais, cumpra o seguinte checklist executável:

### Checklist de Implementação & Direção de Arte
- [ ] **Definição da Cor do Substrato**:
  - Dark Mode: Canvas em `#070709` ou `#0a0a0c`, cartões em `#121217` e bordas semitransparentes de 1px (`rgba(255, 255, 255, 0.08)` a `0.12`).
  - Light Mode: Canvas em `#ffffff` a `#fbfbfa`, cartões com fundo branco puro e borda `rgba(0, 0, 0, 0.06)`.
- [ ] **Bisel e Iluminação Direcional**:
  - Evitar sombras chapadas ou bordas espessas. Adicionar realce sutil no topo de cartões e pílulas (`border-t: 1px solid rgba(255, 255, 255, 0.15)`).
- [ ] **Física de Molas em Toda Microinteração**:
  - Configurar todas as animações táteis com molas amortecidas do Framer Motion / Motion.dev (`stiffness: 380`, `damping: 30`, `mass: 0.8`), eliminando transições puramente lineares.
- [ ] **Tipografia com Contraste Editorial**:
  - Parear títulos monumentais em fontes grotescas de alto impacto (`Inter`, `Geist Sans`, `Clash Display` ou `Plus Jakarta Sans`) com tracking condensado (`-0.03em`) e legendas monoespaçadas com tracking expandido (`+0.05em`).
- [ ] **Navegação em Ilha Flutuante (Floating Pill Nav)**:
  - Implementar barra de cabeçalho com cantos totalmente arredondados (`rounded-full`), desfoque de fundo ótico (`backdrop-blur-xl`) e elevação flutuante acima do canvas principal.
- [ ] **Otimização de Mídia Hero & Zero CLS**:
  - Reservar o espaço dos containers de mídia com proporções fixas (`aspect-[16/10]` ou `aspect-[4/3]`).
  - Incluir animação de placeholder shimmer antes do carregamento completo de vídeos ou imagens para garantir Cumulative Layout Shift (CLS = 0).
- [ ] **Conformidade com Acessibilidade**:
  - Fornecer suporte rigoroso à media query `@media (prefers-reduced-motion: reduce)`, desativando deslocamentos de mola e garantindo legibilidade imediata para todos os usuários.
