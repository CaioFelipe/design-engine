---
id: "fancycomponents-dev"
name: "Fancy Components"
url: "https://www.fancycomponents.dev/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Creative Motion & Playful Engineering", "Kinetic Variable Typography", "2D Rigid-Body Physics (Matter.js)", "Tactile Awwwards-Grade Micro-Interactions", "SVG Masking & Organic Gooey Shaders"]
densidade_informacao: "Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Motion/Springs) a Alto (Matter.js 2D Physics Loop / SVG Matrix Filters)"
stack_frameworks: ["React 19 / 18", "Next.js (App Router)", "Tailwind CSS (v3 & v4)", "Motion (Framer Motion 12)", "Matter.js (v0.20+)", "Poly-decomp", "SVG Path Commander", "Flubber"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter Variable", "Roboto Flex", "Space Grotesk", "Clash Display", "Syne", "Cabinet Grotesk"]
  paletas_ideais: ["Editorial Dark Craft (Zinc 950 / Black #080808 / Chalk White)", "Playful High-Contrast (Electric Yellow #FFE600 / Neon Lime / Obsidian)", "Creative Studio Monochrome with Saturated Accents", "Deep Slate & Cyan Glow"]
  combinacoes_recomendadas: ["Shadcn UI", "Magic UI", "React Bits", "Cult UI", "Aceternity UI", "Lenis Scroll"]
  conflitos_esteticos: ["Corporativo Rígido/Estático estilo Enterprise ERP sem micro-interações", "Material Design 2 arcaico com elevações estáticas pesadas", "Flat Neobrutalism cru sem easing ou aceleração elástica"]
---

# Fancy Components — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo conceituado design engineer **Daniel Petho**, o **Fancy Components** (`fancycomponents.dev`) nasceu com uma declaração de missão explícita: **"Make the web fun again"** (Tornar a web divertida novamente). A gênese do projeto surge como um contraponto deliberado à crescente comoditização e homogeneização do design visual contemporâneo. Embora a padronização trazida por bibliotecas convencionais tenha elevado a consistência e a acessibilidade da web, ela também introduziu uma estética previsível e monótona ("corporate clean").

O Fancy Components opera na fronteira entre a **Engenharia de Interação de Alta Fidelidade** e o **Creative Coding**, reengenheirando em componentes modulares e acessíveis as técnicas interativas que antes ficavam confinadas a sites premiados do Awwwards e FWA (estúdios como Active Theory, Dogstudio ou Locomotive).

A identidade visual e arquitetura estética do Fancy Components destacam-se por cinco assinaturas exclusivas:

1. **Física 2D de Corpos Rígidos no DOM (Matter.js + Poly-Decomp Integration)**:
   Ao contrário da vasta maioria das bibliotecas de UI que limitam animações a transições CSS ou interpolações lineares de opacidade/escala, o Fancy Components integra nativamente o motor físico bidimensional **Matter.js** diretamente com elementos HTML e componentes React. Através de abstrações como `<Gravity>` e `<MatterBody>`, tags semânticas, botões, chips e ícones tornam-se entidades dinâmicas dotadas de massa, atrito, restituição (quique), momento angular e gravidade vetorial. Corpos não-convexos complexos são decompostos em tempo real via `poly-decomp`, permitindo que formas SVG recortadas colidam e respondam a forças magnéticas de atração ou repulsão pelo cursor do mouse com precisão física tangível.

2. **Tipografia Cinética Reativa a Proximidade Euclidiana (Variable Font Dynamics)**:
   O Fancy Components explora os recursos mais avançados do padrão OpenType de **Fontes Variáveis** (`font-variation-settings`). Em vez de limitar o peso tipográfico a estados binários (`font-normal` vs `font-bold`), o componente *Variable Font Cursor Proximity* calcula em tempo real a distância euclidiana radial entre a posição instantânea do cursor do usuário e o centroide de cada glifo de texto. À medida que o mouse desliza, os caracteres individuais expandem seu peso (`wght`), largura (`wdth`) ou inclinação (`slnt`) através de funções de decaimento matemático (linear, exponencial ou gaussiano), criando a sensação visceral de que o texto respira e reage magneticamente ao observador.

3. **Geometria Paramétrica ao Longo de Paths SVG (`Marquee Along SVG Path`)**:
   Diferente dos tradicionais marquees e tickers horizontais de texto que se deslocam rigidamente em linha reta, o Fancy Components introduziu uma infraestrutura baseada em `svg-path-commander` que calcula tangentes e normais vetoriais ao longo de qualquer curva Bézier arbitrária (`<path d="..." />`). Textos, avatares, selos e elementos de marca fluem e dobram-se organicamente ao longo de arcos, espirais, senoides ou contornos customizados, acelerando ou desacelerando com base na velocidade inercial do scroll da página.

4. **Filtros Matriciais SVG Nativos & Efeitos Metaball / Gooey**:
   A biblioteca rejeita texturas genéricas pré-renderizadas, aproveitando primitivas gráficas nativas do navegador via SVG Filters (`feGaussianBlur`, `feColorMatrix` e `feComposite`). Ao manipular as matrizes de canal alfa dos elementos, o Fancy Components produz o famoso efeito orgânico "Gooey", onde botões, abas e gotas fundem-se plasticamente como mercúrio ou fluidos viscerais antes de se desmembrarem, mantendo resolução vetorial perfeita em qualquer densidade de pixels (Retina/4K).

5. **Distribuição Aberta e Agnóstica via Registro Shadcn**:
   Alinhado com a evolução dos ecossistemas modernos de front-end, o Fancy Components não impõe um pacote monolítico fechado via `npm install`. Ele adota a arquitetura de código-fonte aberto distribuído através do protocolo de registros do shadcn (`@fancy/component-name`). Isso permite que os desenvolvedores importem e personalizem diretamente o código TypeScript/Tailwind em suas árvores de componentes locais, assegurando controle absoluto sobre o bundle e a estilização.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **Portfólios de Creative Technologists, Design Engineers & Estúdios Criativos**:
   Para designers e desenvolvedores que precisam provar proficiência técnica excepcional e domínio de micro-interações na primeira dobra da página. Recursos como *Elastic Line*, *Variable Font Cursor Proximity*, *Box Carousel* e *Pixel Trail* estabelecem uma autoridade estética imediata.
2. **Landing Pages de Startups de Inteligência Artificial & Computação Espacial**:
   Empresas que constroem o futuro (agentes autônomos, infraestrutura de hardware, interfaces neurais) precisam de uma presença digital que fuja das convenções antiquadas de templates SaaS genéricos. O uso de *Gravity* para exibir stacks de integrações ou modelos disponíveis cria momentos inesquecíveis de descoberta.
3. **Campanhas de Lançamento de Hardware & Produtos Premium D2C**:
   Apresentação de periféricos, vestíveis inteligentes, instrumentos musicais ou vestuário de luxo. A rotação prismática tridimensional do *Box Carousel* e a animação editorial de *Media Between Text* conferem uma atmosfera cinematográfica de catálogo de alta costura.
4. **DevTools, Plataformas de Nuvem & Produtos "Craft-First"**:
   Ferramentas voltadas a desenvolvedores que valorizam detalhamento artesanal (como Linear, Raycast ou Supabase). Detalhes como o *Scramble Hover* em barras de navegação ou códigos promocionais, e *Vertical Cut Reveal* em chamadas de atualização de versão trazem requinte e entusiasmo técnico.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Estrutural e Neutra)**:
  Layouts limpos baseados em CSS Grid/Flexbox, tipografia neutra altamente legível (`Geist Sans` ou `Inter`), espaçamentos generosos, paleta sóbria (zinc, slate ou monochrome profundo) e componentes utilitários estáveis (Shadcn UI padrão para inputs, tabelas e diálogos).
- **30% (Micro-interações de Fluidez & Feedback Físico do Fancy Components)**:
  Elementos interativos de toque leve que enriquecem a exploração sem obstruir tarefas: separadores com cordas elásticas interativas (*Elastic Line*), botões com tipografia decodificada ao passar o cursor (*Scramble Hover*), transições de revelação tipográfica (*Vertical Cut Reveal*) e cards empilhados na rolagem (*Stacking Cards*).
- **10% (Showstoppers Protagonistas de Impacto Viral)**:
  Exclusivamente **um** efeito de alta escala física por página ou seção principal:
  - Uma caixa de gravidade interativa (*Gravity / MatterBody*) na Hero Section ou no Footer, onde os usuários podem jogar e arremessar badges de tecnologias; **OU**
  - Um marquee tipográfico curvo (*Marquee Along SVG Path*) que divide a dobra do manifesto da marca; **OU**
  - Um cubo 3D giratório (*Box Carousel*) como centro focal de mídia na vitrine do produto.
  *Regra de Ouro*: Nunca coloque dois showstoppers de física pesada concorrendo no mesmo campo de visão.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Telas Críticas de Checkout, Pagamento e Transações Financeiras**:
  Em fluxos de faturamento, autenticação em duas etapas ou formulários bancários, qualquer atraso perceptível de animação, embaralhamento de caracteres (*Scramble*) ou elementos móveis que alterem suas posições quebra a confiança do usuário e induz erros operacionais graves.
- **Grids de Dados Analíticos & Dashboards ERP Densos**:
  Interfaces com centenas de linhas de métricas, cotações de bolsa ou planilhas operacionais não devem conter físicas de gravidade, trilhas de pixels (*Pixel Trail*) ou linhas elásticas. A densidade e a velocidade de leitura de 0ms são mandatórias.
- **Formulários de Entrada de Texto Primários**:
  Não utilize filtros metaball (*Gooey*) ou fontes variáveis acopladas ao cursor em campos `<input>` ou `<textarea>` comuns. Glifos que tremem ou mudam de peso durante a digitação geram fadiga visual e aumentam erros de digitação.
- **Dispositivos Móveis em Modo de Economia de Energia ou Sem Aceleração GPU**:
  Cálculos de colisão contínua via `Matter.Engine.update` ou filtros SVG aplicados em áreas gigantescas de alta resolução podem causar engasgos (*dropped frames*) e drenar a bateria se não forem mitigados ou desativados em telas pequenas.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **Síndrome do "Playground Incontrolável"**: Transformar botões funcionais de conversão (ex: "Criar Conta Grátis") em corpos rígidos com gravidade no meio do fluxo de compra. O usuário tenta clicar no botão e ele foge ou cai no fundo da tela, destruindo as taxas de conversão. Corpos rígidos devem conter elementos decorativos, selos ou badges de demonstração.
- **Falta de Cleanup no Lifecycle do Matter.js**: Instanciar um motor `Matter.Engine` e esquecer de cancelar o loop do `Runner` e o `Render` no desmonte do componente React (`useEffect` cleanup). Isso gera vazamentos catastróficos de memória e gargalos de CPU no navegador.
- **Sobrecarga de Fontes Variáveis com Centenas de Nós**: Usar *Variable Font Cursor Proximity* em um parágrafo longo de 500 palavras. Dividir cada caractere individual em um elemento `<motion.span>` cria milhares de nós no DOM e centenas de cálculos trigonométricos a cada frame de mouse, levando a interface a engasgar. Reserve o efeito estritamente para títulos concisos (H1/H2) de 2 a 8 palavras.
- **Ignorar `@media (prefers-reduced-motion)`**: Não desativar rotações contínuas, flutuações e explosões de gravidade para usuários com distúrbios vestibulares. O suporte a redução de movimento deve retornar versões estáticas ou simplificadas dos elementos.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão 12 componentes emblemáticos do acervo Fancy Components, cobrindo física 2D, tipografia dinâmica, blocos criativos e filtros ópticos:

```
┌────────────────────────────────────────────────────────────────────────┐
│                        FANCY COMPONENTS SUITE                          │
├──────────────────┬──────────────────┬─────────────────┬────────────────┤
│    PHYSICS 2D    │  KINETIC TYPE    │  CREATIVE BLOCK │ OPTICAL FILTER │
├──────────────────┼──────────────────┼─────────────────┼────────────────┤
│ • Gravity Box    │ • Variable Font  │ • Marquee SVG   │ • Gooey SVG    │
│ • Attractor Ring │ • 3D Letter Swap │ • Stacking Card │ • Pixelate SVG │
│ • Elastic Line   │ • Vertical Cut   │ • Media In Text │ • Pixel Trail  │
│ • Drag Elements  │ • Scramble Hover │ • Box Carousel  │ • 3D Sine Float│
└──────────────────┴──────────────────┴─────────────────┴────────────────┘
```

### 1. Gravity & MatterBody (`@fancy/gravity`)
- **Categoria**: *Physics (Matter.js 2D Rigid Body Engine)*
- **Anatomia Visual**: Um container delimitado por quatro paredes invisíveis (chão, teto e laterais configuráveis). Os elementos filhos envolvidos pela tag `<MatterBody>` comportam-se como objetos sólidos: caem com gravidade vetorial natural, colidem entre si com cálculo elástico e atrito, acumulam-se no chão em pilhas realistas e podem ser pegos e arremessados com o cursor do mouse. Suporta formas geométricas retangulares, circulares ou poligonais derivadas de caminhos SVG via `poly-decomp`.
- **Gatilho de Interação**: Entrada na viewport (autoStart), colisão física interativa, e arrasto com clique contínuo do mouse (`grabCursor`, drag & throw).
- **Onde encaixar na página**: Hero sections de produtos de tecnologia (como um "sandbox" de ferramentas suportadas), seções "About Us" com adesivos interativos da equipe, ou no rodapé (Footer) para entretenimento do usuário.

### 2. Cursor Attractor & Gravity (`@fancy/cursor-attractor-and-gravity`)
- **Categoria**: *Physics (Orbital & Cursor Mechanics)*
- **Anatomia Visual**: Similar ao módulo de gravidade, mas introduz vetores de força dinâmica vinculados a um ponto fixo central ou às coordenadas instantâneas do cursor. Elementos orbitam, são sugados em direção ao ponteiro como em um campo gravitacional de um buraco negro, ou são repelidos violentamente por um campo de força configurável (`cursorStrength`).
- **Gatilho de Interação**: Movimento contínuo do cursor do mouse dentro da área de influência (`cursorFieldRadius`).
- **Onde encaixar na página**: Banners de anúncio de produtos, seções de transição de manifesto ou fundos interativos de apresentações de design.

### 3. Variable Font Cursor Proximity (`@fancy/variable-font-cursor-proximity`)
- **Categoria**: *Kinetic Typography (OpenType Axes)*
- **Anatomia Visual**: Uma frase ou título exibido com uma fonte variável compatível (como *Inter Variable*, *Roboto Flex* ou *Geist*). Conforme o ponteiro se move sobre o container, cada caractere detecta a proximidade milimétrica do cursor e altera suavemente suas propriedades de eixos variáveis: peso (`wght: 100 → 900`), inclinação (`slnt: 0 → -15`), ou largura (`wdth: 75 → 125`). Apresenta decaimento configurável linear, quadrático (exponencial) ou gaussiano tipo curva de sino.
- **Gatilho de Interação**: Evento `onMouseMove` contínuo mapeado via `useAnimationFrame` para garantir 60fps/120fps sem travamentos no render tree.
- **Onde encaixar na página**: Título principal H1 da Hero Section de agências ou criadores independentes, e títulos de chamadas para ação (CTA) em landing pages.

### 4. Elastic Line (`@fancy/elastic-line`)
- **Categoria**: *Physics / Micro-Interactions*
- **Anatomia Visual**: Um divisor de linha aparentemente estático e minimalista (horizontal ou vertical). Quando o cursor do usuário cruza ou arrasta a linha, ela se comporta como uma corda de violão esticada ou elástico físico, deformando-se dinamicamente na direção do mouse até ultrapassar um limiar de soltura (`releaseThreshold`), momento em que vibra e dissipa energia com oscilação harmônica elástica amortecida (`spring: stiffness 300, damping 5`).
- **Gatilho de Interação**: Passagem (hover/cross) ou clique e arraste do ponteiro sobre a trajetória da linha.
- **Onde encaixar na página**: Separadores elegantes entre seções de conteúdo, divisores de itens em listas de cases de portfólio, e rodapé.

### 5. Marquee Along SVG Path (`@fancy/marquee-along-svg-path`)
- **Categoria**: *Blocks & SVG Vector Animation*
- **Anatomia Visual**: Elementos repetidos (textos tipográficos, badges, ícones ou fotos circulares) que navegam de forma fluida ao longo de qualquer geometria SVG arbitrária (uma onda senoidal contínua, uma curva elíptica infinita ou uma espiral decorativa). O cálculo de translação e rotação angular orienta automaticamente o topo do elemento na direção da tangente vetorial do caminho.
- **Gatilho de Interação**: Reprodução automática contínua (`auto-play`) combinada opcionalmente com aceleração/desaceleração proporcional à velocidade de rolagem da página (`useScroll` e `useVelocity`).
- **Onde encaixar na página**: Seção de prova social (Social Proof de logos de parceiros), divisão visual entre blocos de conteúdo e faixas de manifesto de marca.

### 6. Gooey SVG Filter (`@fancy/gooey-svg-filter`)
- **Categoria**: *Optical Filters / Native SVG*
- **Anatomia Visual**: Um filtro vetorial oculto inserido no DOM que transforma elementos filhos adjacentes em substâncias líquidas conectadas. Quando dois botões, círculos de menu ou bolhas se aproximam, uma ponte viscosa se forma entre eles, fundindo-se em uma única massa orgânica contínua, desmembrando-se com tensão superficial quando separados.
- **Gatilho de Interação**: Movimento e sobreposição de nós gráficos (seja via drag, hover expansivo ou transição de abas).
- **Onde encaixar na página**: Seletores de abas (Tabs) com indicador deslizante fluido, menus de navegação flutuantes (FABs) que se expandem em subitens, e micro-interações de curtidas/reações.

### 7. Box Carousel (`@fancy/box-carousel`)
- **Categoria**: *Carousel & 3D CSS Space*
- **Anatomia Visual**: Uma vitrine tridimensional inspirada em um prisma ou cubo poligonal renderizado puramente com transformações CSS 3D (`transform-style: preserve-3d` e perspectiva dinâmica). O usuário navega por slides multimídia (vídeos e imagens de altíssima definição) girando as faces do cubo no espaço cartesiano com amortecimento inercial preciso.
- **Gatilho de Interação**: Clique em botões de navegação lateral, atalhos de teclado, arraste gestual (drag) ou autoplay com parada no hover.
- **Onde encaixar na página**: Demonstração de recursos do produto em Bento Grids, vitrine de screenshots de aplicativos móveis ou galerias de vestuário em e-commerces de vanguarda.

### 8. Pixel Trail (`@fancy/pixel-trail`)
- **Categoria**: *Backgrounds & Interactive Canvases*
- **Anatomia Visual**: Uma grade discreta de micro-quadrantes (pixels) transparentes sobreposta a uma seção. Conforme o mouse se desloca, os pixels individuais tocados pelo raio do cursor acendem com cor vibrante configurável e apagam gradualmente com um rastro de desvanecimento (*decay duration*) temporal. Cria uma estética retrô-futurista de terminal ou display fluorescente.
- **Gatilho de Interação**: Coordenadas instantâneas de movimento do cursor sobre o container delimitador.
- **Onde encaixar na página**: Fundo de Hero Sections com tema DevTools/hacker, cards individuais de Bento Grid como efeito de destaque interno, e seções de código.

### 9. Letter 3D Swap (`@fancy/letter-3d-swap`)
- **Categoria**: *Kinetic Typography*
- **Anatomia Visual**: Ao receber foco ou passagem de mouse, as letras individuais de uma palavra rotacionam em 90 graus no eixo X ou Y em um espaço 3D com perspectiva estrita, trocando uma face frontal por uma face secundária (com cores contrastantes ou estilo tipográfico invertido). Cada caractere gira com um atraso milimétrico escalonado (*stagger duration* de 0.03s a 0.05s).
- **Gatilho de Interação**: Hover do mouse sobre o texto ou clique em botão.
- **Onde encaixar na página**: Links da Navbar principal, botões de Call To Action primários e títulos de serviços.

### 10. Vertical Cut Reveal (`@fancy/vertical-cut-reveal`)
- **Categoria**: *Kinetic Typography & Masking*
- **Anatomia Visual**: O texto é fatiado verticalmente em palavras ou caracteres encapsulados em máscaras de transbordamento oculto (`overflow-hidden`). Os glifos emergem como se estivessem sendo projetados de uma fenda invisível, impulsionados por uma física de mola elástica sutil e ágil (`stiffness: 190, damping: 22`). Permite direção direta ou invertida (*reverse*), e escalonamento a partir do início, centro ou extremidades.
- **Gatilho de Interação**: Disparo automático na entrada da viewport (`whileInView`) ou via controle imperativo (`VerticalCutRevealRef.startAnimation()`).
- **Onde encaixar na página**: Manchetes principais de Landing Pages, slogans de produtos e cabeçalhos de seções editoriais.

### 11. Scramble Hover (`@fancy/scramble-hover`)
- **Categoria**: *Kinetic Typography / Decryption*
- **Anatomia Visual**: Na passagem do cursor, a string original é temporariamente substituída por uma tempestade veloz de glifos criptográficos e símbolos aleatórios (`!@#$%^&*()_+0123456789`). Em questão de milissegundos, as posições convergem ordenadamente a partir da esquerda, direita ou do centro de volta aos caracteres corretos originais.
- **Gatilho de Interação**: Evento `onMouseEnter` / `onMouseLeave`.
- **Onde encaixar na página**: Chips de status, tags de categorias de blog, números de telefone/e-mails de contato e itens de navegação técnica.

### 12. Media Between Text (`@fancy/media-between-text`)
- **Categoria**: *Blocks & Editorial Design*
- **Anatomia Visual**: Uma linha de texto editorial de grande porte onde uma palavra ou espaço entre termos abre espaço suavemente para acomodar uma pílula multimídia dinâmica (um vídeo em loop curto ou imagem em miniatura). Ao interagir ou rolar, a mídia expande sua largura proporcional, unindo a leitura textual à narrativa cinematográfica.
- **Gatilho de Interação**: Scroll na viewport (`useInView`) ou hover sobre o termo conector.
- **Onde encaixar na página**: Títulos de impacto manifesto em páginas corporativas de agências, cases de estudo e introdução de equipes de liderança.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

O Fancy Components integra-se nativamente com a arquitetura do **shadcn/ui**. Para configurar um projeto React / Next.js com suporte total aos componentes da biblioteca:

```bash
# 1. Dependências centrais de animação e estilização
npm install motion clsx tailwind-merge class-variance-authority lucide-react

# 2. Dependências para componentes de física e matemática (se usar Gravity/Physics)
npm install matter-js poly-decomp lodash
npm install -D @types/matter-js @types/lodash

# 3. Dependências para caminhos SVG e curvatura (se usar Marquee Along Path)
npm install svg-path-commander flubber uuid
npm install -D @types/flubber @types/uuid
```

#### Configuração do Registro Shadcn (`components.json`)
Adicione o namespace `@fancy` ao array de registros do seu projeto para permitir a instalação via CLI:

```json
{
  "$schema": "https://ui.shadcn.com/schema.json",
  "style": "default",
  "rsc": true,
  "tsx": true,
  "tailwind": {
    "config": "tailwind.config.ts",
    "css": "src/styles/globals.css",
    "baseColor": "zinc",
    "cssVariables": true
  },
  "aliases": {
    "components": "@/components",
    "utils": "@/lib/utils"
  },
  "registries": {
    "@fancy": "https://fancycomponents.dev/r/{name}.json"
  }
}
```

Para instalar qualquer componente diretamente na base de código via terminal:

```bash
npx shadcn@latest add @fancy/gravity
npx shadcn@latest add @fancy/variable-font-cursor-proximity
npx shadcn@latest add @fancy/elastic-line
npx shadcn@latest add @fancy/gooey-svg-filter
```

---

### Física de Movimento e Constantes de Transição

O Fancy Components baseia sua assinatura tátil em curvas de mola amortecidas meticulosamente afinadas em vez de easings temporais tradicionais (`ease-in-out`):

| Componente | Tipo de Dinâmica | Parâmetros de Configuração | Sensação Sensorial |
| :--- | :--- | :--- | :--- |
| **Vertical Cut Reveal** | Motion Spring | `stiffness: 190, damping: 22, mass: 1` | Elegante, seguro, desaceleração editorial sem oscilações excessivas |
| **Elastic Line** | SVG Spring Oscillator | `stiffness: 300, damping: 5, mass: 0.8` | Altamente elástico, zumbido semelhante a corda de violão esticada |
| **Drag Elements** | Inertia Motion | `bounceStiffness: 200, bounceDamping: 300` | Peso inercial tangível com retorno elástico firme nas bordas |
| **Box Carousel** | Motion Spring 3D | `stiffness: 120, damping: 20, mass: 1.2` | Rotação prismática com peso volumétrico e parada cirúrgica |
| **Matter.js Engine** | Física Newtoniana | `gravity.y: 1.0, friction: 0.1, restitution: 0.6` | Queda de corpos sólidos com quique elástico moderado e colisão realista |

---

### Receitas de Código Funcionais

#### Receita 1: Arena de Física Interativa com Gravidade e Colisão 2D (`GravityPlayground.tsx`)

Abaixo está a implementação completa e modular de um container de física com Matter.js onde tags de habilidades ou tecnologias caem e colidem de maneira orgânica e interativa:

```tsx
"use client"

import React, { useRef, useEffect, useState } from "react"
import Matter, {
  Engine,
  Render,
  Runner,
  Bodies,
  Composite,
  Mouse,
  MouseConstraint,
  Events,
} from "matter-js"
import { Code2, Cpu, Database, Flame, Sparkles, Terminal } from "lucide-react"

interface SkillItem {
  id: string
  label: string
  icon: React.ComponentType<{ className?: string }>
  color: string
}

const SKILLS: SkillItem[] = [
  { id: "1", label: "React 19", icon: Code2, color: "bg-cyan-500/10 text-cyan-400 border-cyan-500/30" },
  { id: "2", label: "Next.js", icon: Terminal, color: "bg-white/10 text-zinc-100 border-white/30" },
  { id: "3", label: "Tailwind CSS", icon: Flame, color: "bg-sky-500/10 text-sky-400 border-sky-500/30" },
  { id: "4", label: "Matter.js", icon: Cpu, color: "bg-amber-500/10 text-amber-400 border-amber-500/30" },
  { id: "5", label: "PostgreSQL", icon: Database, color: "bg-indigo-500/10 text-indigo-400 border-indigo-500/30" },
  { id: "6", label: "Creative Motion", icon: Sparkles, color: "bg-fuchsia-500/10 text-fuchsia-400 border-fuchsia-500/30" },
]

export function GravityPlayground() {
  const sceneRef = useRef<HTMLDivElement>(null)
  const itemRefs = useRef<Map<string, HTMLDivElement>>(new Map())
  const [isReady, setIsReady] = useState(false)

  useEffect(() => {
    const container = sceneRef.current
    if (!container) return

    const { clientWidth: width, clientHeight: height } = container

    // 1. Instanciação da engine e mundo físico Matter.js
    const engine = Engine.create({
      gravity: { x: 0, y: 0.9, scale: 0.001 },
    })
    const world = engine.world

    // 2. Paredes de contenção invisíveis
    const wallThickness = 100
    const ground = Bodies.rectangle(width / 2, height + wallThickness / 2, width * 2, wallThickness, {
      isStatic: true,
      friction: 0.3,
    })
    const leftWall = Bodies.rectangle(-wallThickness / 2, height / 2, wallThickness, height * 2, {
      isStatic: true,
    })
    const rightWall = Bodies.rectangle(width + wallThickness / 2, height / 2, wallThickness, height * 2, {
      isStatic: true,
    })

    Composite.add(world, [ground, leftWall, rightWall])

    // 3. Mapeamento dos corpos físicos associados aos elementos DOM
    const bodyMap = new Map<string, Matter.Body>()

    SKILLS.forEach((skill, index) => {
      const el = itemRefs.current.get(skill.id)
      if (!el) return

      const rect = el.getBoundingClientRect()
      const startX = width * 0.2 + (index % 3) * 160 + (Math.random() * 20 - 10)
      const startY = -60 - index * 70
      const initialAngle = (Math.random() - 0.5) * 0.5

      const body = Bodies.rectangle(startX, startY, rect.width || 140, rect.height || 44, {
        restitution: 0.5, // Coeficiente de quique elástico
        friction: 0.15,  // Atrito com outras superfícies
        density: 0.002,  // Massa proporcional
        angle: initialAngle,
      })

      bodyMap.set(skill.id, body)
      Composite.add(world, body)
    })

    // 4. Integração do cursor com MouseConstraint para arremesso
    const mouse = Mouse.create(container)
    const mouseConstraint = MouseConstraint.create(engine, {
      mouse: mouse,
      constraint: {
        stiffness: 0.2,
        render: { visible: false },
      },
    })
    Composite.add(world, mouseConstraint)

    // 5. Runner e loop de animação sincronizando transforms com a simulação
    const runner = Runner.create()
    Runner.run(runner, engine)

    let animationFrameId: number
    const updateTransforms = () => {
      bodyMap.forEach((body, id) => {
        const el = itemRefs.current.get(id)
        if (!el) return

        const { x, y } = body.position
        const angle = body.angle
        el.style.transform = `translate3d(${x - el.offsetWidth / 2}px, ${y - el.offsetHeight / 2}px, 0) rotate(${angle}rad)`
      })
      animationFrameId = requestAnimationFrame(updateTransforms)
    }

    animationFrameId = requestAnimationFrame(updateTransforms)
    setIsReady(true)

    // 6. Cleanup rigoroso para prevenir memory leaks
    return () => {
      cancelAnimationFrame(animationFrameId)
      Runner.stop(runner)
      Composite.clear(world, false)
      Engine.clear(engine)
    }
  }, [])

  return (
    <div className="relative w-full max-w-3xl h-[420px] mx-auto rounded-3xl border border-zinc-800 bg-zinc-950/80 backdrop-blur-xl overflow-hidden shadow-2xl p-4 select-none">
      <div className="absolute top-4 left-6 pointer-events-none z-10">
        <span className="text-xs font-mono tracking-wider uppercase text-zinc-500">Sandbox Interativo</span>
        <h3 className="text-lg font-semibold text-zinc-200">Arraste e jogue os módulos</h3>
      </div>

      <div ref={sceneRef} className="relative w-full h-full cursor-grab active:cursor-grabbing">
        {SKILLS.map((skill) => {
          const Icon = skill.icon
          return (
            <div
              key={skill.id}
              ref={(el) => {
                if (el) itemRefs.current.set(skill.id, el)
                else itemRefs.current.delete(skill.id)
              }}
              className={`absolute top-0 left-0 inline-flex items-center gap-2.5 px-4 py-2.5 rounded-full border shadow-lg backdrop-blur-md transition-opacity duration-300 will-change-transform ${skill.color} ${isReady ? "opacity-100" : "opacity-0"}`}
            >
              <Icon className="w-4 h-4 shrink-0" />
              <span className="text-sm font-medium whitespace-nowrap">{skill.label}</span>
            </div>
          )
        })}
      </div>
    </div>
  )
}
```

---

#### Receita 2: Variable Font Cursor Proximity Euclidiana (`VariableProximityHeader.tsx`)

Esta receita demonstra a manipulação milimétrica do eixo `wght` (peso de 200 a 850) ao longo de cada caractere de um título, baseado na distância em pixels do mouse:

```tsx
"use client"

import React, { useRef, useMemo, useEffect, useState } from "react"

interface VariableProximityProps {
  label: string
  radius?: number
  minWeight?: number
  maxWeight?: number
  className?: string
}

export function VariableProximityHeader({
  label,
  radius = 120,
  minWeight = 200,
  maxWeight = 850,
  className = "",
}: VariableProximityProps) {
  const containerRef = useRef<HTMLHeadingElement>(null)
  const [weights, setWeights] = useState<number[]>([])

  const characters = useMemo(() => Array.from(label), [label])
  const charRefs = useRef<(HTMLSpanElement | null)[]>([])

  useEffect(() => {
    setWeights(new Array(characters.length).fill(minWeight))
  }, [characters, minWeight])

  useEffect(() => {
    const container = containerRef.current
    if (!container) return

    let rafId: number
    let mouseX = -9999
    let mouseY = -9999

    const handleMouseMove = (e: MouseEvent) => {
      const rect = container.getBoundingClientRect()
      mouseX = e.clientX - rect.left
      mouseY = e.clientY - rect.top

      cancelAnimationFrame(rafId)
      rafId = requestAnimationFrame(() => {
        const newWeights = charRefs.current.map((charEl) => {
          if (!charEl) return minWeight

          // Ponto central do glifo
          const charCenterX = charEl.offsetLeft + charEl.offsetWidth / 2
          const charCenterY = charEl.offsetTop + charEl.offsetHeight / 2

          // Distância euclidiana radial
          const dist = Math.hypot(mouseX - charCenterX, mouseY - charCenterY)

          if (dist >= radius) return minWeight

          // Interpolação quadrática suave (falloff exponencial invertido)
          const factor = Math.cos((dist / radius) * (Math.PI / 2))
          return Math.round(minWeight + (maxWeight - minWeight) * factor)
        })

        setWeights(newWeights)
      })
    }

    const handleMouseLeave = () => {
      cancelAnimationFrame(rafId)
      setWeights(new Array(characters.length).fill(minWeight))
    }

    container.addEventListener("mousemove", handleMouseMove)
    container.addEventListener("mouseleave", handleMouseLeave)

    return () => {
      container.removeEventListener("mousemove", handleMouseMove)
      container.removeEventListener("mouseleave", handleMouseLeave)
      cancelAnimationFrame(rafId)
    }
  }, [characters, minWeight, maxWeight, radius])

  return (
    <h1
      ref={containerRef}
      className={`inline-block cursor-default select-none tracking-tight transition-colors ${className}`}
      style={{ fontOpticalSizing: "auto" }}
    >
      {characters.map((char, i) => (
        <span
          key={i}
          ref={(el) => { charRefs.current[i] = el }}
          className="inline-block transition-[font-variation-settings] duration-75 will-change-[font-variation-settings]"
          style={{
            fontVariationSettings: `'wght' ${weights[i] || minWeight}`,
          }}
        >
          {char === " " ? "\u00A0" : char}
        </span>
      ))}
    </h1>
  )
}
```

---

#### Receita 3: Filtro Metaball/Gooey Nativo em Menu Fluido (`GooeyDockMenu.tsx`)

Implementação prática de um menu flutuante cujos botões conectam-se organicamente via filtro SVG nativo com matriz de canal alfa:

```tsx
"use client"

import React, { useState } from "react"
import { motion } from "motion/react"
import { Home, Compass, Bell, User, Plus } from "lucide-react"

export function GooeyDockMenu() {
  const [isOpen, setIsOpen] = useState(false)

  const items = [
    { icon: Home, label: "Feed" },
    { icon: Compass, label: "Explorar" },
    { icon: Bell, label: "Alertas" },
    { icon: User, label: "Perfil" },
  ]

  return (
    <div className="relative flex items-center justify-center p-12">
      {/* 1. Definição do Filtro SVG Oculto no DOM */}
      <svg className="hidden absolute" aria-hidden="true">
        <defs>
          <filter id="fancy-gooey">
            <feGaussianBlur in="SourceGraphic" stdDeviation="10" result="blur" />
            <feColorMatrix
              in="blur"
              type="matrix"
              values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 19 -9"
              result="goo"
            />
            <feComposite in="SourceGraphic" in2="goo" operator="atop" />
          </filter>
        </defs>
      </svg>

      {/* 2. Container com aplicação do filtro metaball */}
      <div
        className="relative flex items-center justify-center"
        style={{ filter: "url(#fancy-gooey)" }}
      >
        {/* Itens do Menu que emergem da bolha principal */}
        {items.map((item, index) => {
          const Icon = item.icon
          const angle = (index * 90) * (Math.PI / 180)
          const distance = isOpen ? 85 : 0

          return (
            <motion.button
              key={item.label}
              initial={false}
              animate={{
                x: Math.cos(angle) * distance,
                y: Math.sin(angle) * distance,
                scale: isOpen ? 1 : 0.4,
              }}
              transition={{
                type: "spring",
                stiffness: 350,
                damping: 24,
              }}
              aria-label={item.label}
              className="absolute w-12 h-12 rounded-full bg-amber-400 text-zinc-950 flex items-center justify-center shadow-md focus:outline-none"
            >
              <Icon className="w-5 h-5 pointer-events-none" />
            </motion.button>
          )
        })}

        {/* Botão Central de Gatilho (Trigger) */}
        <motion.button
          onClick={() => setIsOpen(!isOpen)}
          whileTap={{ scale: 0.9 }}
          aria-expanded={isOpen}
          className="relative z-10 w-14 h-14 rounded-full bg-amber-400 text-zinc-950 flex items-center justify-center shadow-lg focus:outline-none"
        >
          <motion.div
            animate={{ rotate: isOpen ? 135 : 0 }}
            transition={{ type: "spring", stiffness: 300, damping: 20 }}
          >
            <Plus className="w-6 h-6 stroke-[2.5]" />
          </motion.div>
        </motion.button>
      </div>
    </div>
  )
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar o **Fancy Components** como referência fundamental para o design system do produto no `DESIGN_BLUEPRINT.md`, a inteligência artificial deve seguir as regras de orquestração arquitetural abaixo:

### 1. Declaração de Stack & Registros
Declare formalmente a coexistência do Fancy Components com o ecossistema Shadcn UI no blueprint de arquitetura:
```markdown
### Creative Interaction Layer
- Component Library: Fancy Components (por Daniel Petho)
- Registry Endpoint: `@fancy: https://fancycomponents.dev/r/{name}.json`
- Physics Engine: `matter-js` (v0.20+) + `poly-decomp`
- Typography Engine: Kinetic Variable Typography via `font-variation-settings`
- Vector Tracing: `svg-path-commander` para interpolação de curvas
```

### 2. Estratégia de Isolamento e Performance da Física
Para evitar sobrecarga de CPU e travamentos de thread principal:
- **Viewport Visibility Boundary**: Qualquer componente que inicialize um `Matter.Engine` ou execute cálculos de colisão no DOM DEVE encapsular a execução dentro de um `IntersectionObserver`. A engine física deve ser pausada (`Runner.stop()`) quando o container estiver fora da janela de visualização e reiniciada suavemente ao entrar.
- **Fallbacks para Dispositivos Móveis**: Em telas com largura inferior a `768px` (onde o usuário interage via toque direto com menor precisão vetorial), substitua o container de física por um layout estático em grade (Grid ou Flexwrap) ou reduza o número de corpos simultâneos para no máximo 4 entidades.

### 3. Matriz de Proporção e Hierarquia no Design Blueprint
Ao diagramar a página no blueprint, classifique cada uso de acordo com sua função na regra 60-30-10:
- **Base (60%)**: Estrutura neutra em Zinc/Black, tipografia limpa, navegação sem saltos.
- **Micro-Interação (30%)**: *Elastic Line* em divisores de lista; *Scramble Hover* em links de navegação; *Vertical Cut Reveal* em H2s.
- **Showstopper (10%)**: Exclusivamente UM dos seguintes componentes:
  - Hero Section com *Gravity & MatterBody* interativo; OU
  - Seção Manifesto com *Marquee Along SVG Path*; OU
  - Demonstração central com *Box Carousel 3D*.

### 4. Acessibilidade Mandatória (WCAG AAA & Reduced Motion)
O blueprint deve conter a diretriz de conformidade:
```typescript
// Todo componente Fancy deve respeitar o hook useReducedMotion() do Motion:
const shouldReduceMotion = useReducedMotion();

// Se ativado:
// - Desabilitar gravidade e renderizar elementos posicionados estaticamente.
// - Eliminar Scramble e renderizar texto legível imediato.
// - Desativar rotações no Box Carousel e utilizar carrossel deslizante padrão.
```
