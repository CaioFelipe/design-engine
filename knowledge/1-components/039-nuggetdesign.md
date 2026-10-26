---
id: "nuggetdesign"
name: "Nugget Design"
url: "https://www.nuggetdesign.dev/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Design Engineering Craft", "OKLCH Perceptual Amber & Multi-tier Surface Scale", "Tactile Pill Chips with Tabular Badges", "Bespoke Collection Mosaics", "Arcade Easter Egg Kinetics", "Clean Editorial Directory"]
densidade_informacao: "Alta"
impacto_visual: "Moderado a Alto/Showstopper"
custo_computacional: "Baixo a Medio (CSS OKLCH Nativo / Fast Client-side Filtering / Canvas 2D Arcade)"
stack_frameworks: ["React 19 / 18", "Vite", "CSS Custom Properties (OKLCH, LightningCSS)", "Framer Motion", "HTML5 Canvas (Stacker Arcade Engine)", "Clerk Authentication", "Neon Serverless Postgres", "Lucide React"]
compatibilidade:
  fontes_ideais: ["Cute Dino (Display Wordmark)", "Inter", "Geist Sans", "-apple-system / SF Pro Display", "ui-monospace / SF Mono"]
  paletas_ideais: ["Amber / Gold Accent (oklch(52% .19 82) / #f4b720)", "Multi-Surface Dark Scale (oklch(13% .012 260) to oklch(30% .012 260))", "Pristine Light Surface (oklch(98.5% .003 260) to oklch(100% 0 0))", "Subtle High-Fidelity Hairlines (oklch(34% .012 260))"]
  combinacoes_recomendadas: ["shadcn/ui", "Radix UI", "Motion Primitives", "21st.dev", "NumberFlow", "Fancy Components", "Skiper UI"]
  conflitos_esteticos: ["Brutalismo neo-punk saturado e estridente", "Neumorfismo plástico com sombras gaussianas pesadas", "Glassmorphism turvo desmedido sem nitidez tipográfica", "Interfaces corporativas legadas sem micro-estados táteis"]
---

# Nugget Design — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado, curado e codificado pelo **Diya Design Studio**, o **Nugget Design** (`nuggetdesign.dev`) representa o ápice da interseção entre o design editorial refinado e a engenharia de software front-end moderna (*Design Engineering*). Projetado como um diretório vivo e toolkit de ferramentas, recursos e inspirações para design engineers, o produto transcende a ideia comum de um mero agregador de links ao implementar uma arquitetura de componentes nativa de altíssima precisão técnica, paleta perceptual baseada no espaço de cor **OKLCH**, micro-interações táteis e detalhes lúdicos (*craft delights*).

```
╭────────────────────────────────────────────────────────────────────────╮
│                             Nugget Design                              │
│         The Curated Design-Engineering Toolkit & Component Craft       │
├────────────────────────────────────────────────────────────────────────┤
│  [ OKLCH Color Token Engine ] ──► 4 Camadas de Superfície + Âmbar Real │
│  [ Category Pill Chips ]      ──► Badges com Números Tabulares Ativos  │
│  [ Natural Language Search ]  ──► Filtro Stop-word em Memória (Client) │
│  [ 2x2 Collection Mosaics ]   ──► Miniaturas Reais com Hover Lift      │
│  [ Book Specimen Cards ]      ──► Grid Proporcional 2:3 para 100 Livros│
│  [ Stacker Canvas Arcade ]    ──► Easter Egg acionado por 3 toques     │
╰────────────────────────────────────────────────────────────────────────╯
```

### Os Pilares da Assinatura Visual do Nugget Design:

1. **Espaço de Cor Perceptual OKLCH & Sistema de Superfícies em 4 Camadas**:
   Ao contrário de designs convencionais construídos em Hexadecimal ou HSL, o Nugget Design fundamenta toda a sua identidade visual em **OKLCH**, garantindo uniformidade perceptual de luminosidade e croma tanto em temas claros quanto escuros:
   - **Camadas de Superfície Light Mode**: `--surface-0` (`oklch(98.5% .003 260)`), `--surface-1` (`oklch(100% 0 0)`), `--surface-2` (`oklch(96% .004 260)`), `--surface-3` (`oklch(100% 0 0)`).
   - **Camadas de Superfície Dark Mode**: `--surface-0` (`oklch(13% .012 260)` — fundo profundo com leve matiz índigo/ardósia a 260°), subindo gradualmente para `--surface-1` (`21%`), `--surface-2` (`26%`) e `--surface-3` (`30%`).
   - **O Ouro do Nugget (*Golden Amber Accent*)**: O acento de assinatura não é um amarelo comum, mas uma pepita de ouro luminosa: Light Mode `oklch(52% .19 82)` com halo `--accent-tint` a 10% de opacidade; Dark Mode `oklch(78% .16 82)` com contraste nítido contra superfícies escuras e halo suave `--glow-accent`.

2. **Tipografia de Dupla Personalidade (Carisma Playful vs. Precisão Científica)**:
   A identidade tipográfica equilibra calor humano e rigor matemático:
   - **Wordmark Display**: Uso da fonte customizada `Cute Dino` (`/fonts/Cute-Dino.ttf`), que introduz um tom simpático, artesanal e memorável à marca.
   - **Interface & Corpo de Texto**: A robustez limpa de `--font-sans` (`-apple-system`, `system-ui`, `Segoe UI`, `Roboto`, `Geist Sans`), com tamanho padrão em `15px` e `line-height: 1.6`.
   - **Metadados Numéricos**: Uso mandatório de `--font-mono` e `font-variant-numeric: tabular-nums` em contadores, badges de chips, placares e pontuações, prevenindo qualquer layout shift durante transições numéricas.

3. **Glass Panel com Gradiente Radial Fixo (`ellipse 100% 100% at top`)**:
   Em vez de recorrer a borrões genéricos opacos, os painéis superiores utilizam:
   ```css
   background-image: radial-gradient(ellipse 100% 100% at top, var(--accent-tint), transparent 65%);
   backdrop-filter: blur(12px);
   background-attachment: fixed;
   transform: translateZ(0);
   ```
   Isso produz uma iluminação difusa estática no topo da viewport com aceleração de hardware que confere atmosfera orgânica sem degradação de frames por segundo.

4. **Motor de Busca Semântica em Tempo Real com Dicionário de Stop-Words**:
   O Nugget Design inclui um parser semântico in-browser baseado em um dicionário estrito de termos conversacionais (`i`, `im`, `i'm`, `trying`, `want`, `looking`, `for`, `inspo`, `cool`, `best`, `ideas`). Quando um usuário digita frases completas (ex: *"i want some cool about me pages"*), o sistema limpa a query instantaneamente e faz o match com a coleção temática `about` ou com as tags dos 279 recursos catalogados.

5. **Mosaicos de Coleção Temáticos (2x2 Grid Mosaics)**:
   A seção de coleções organiza páginas de referência reais em grids de miniaturas 2x2 com `aspect-ratio: 16/10`, bordas sutis de `gap: 3px` e elevação física no hover (`transform: translateY(-3px)` + `box-shadow: var(--shadow-card-hover)`), permitindo inspecionar visualmente a qualidade dos sites curados antes de clicar.

6. **Lúdico Oculto: O Mini-Arcade Stacker & Mascot Easter Egg**:
   Celebrando a cultura hacker/craft, clicar três vezes consecutivas no mascote na newsletter (`/nugget-pointing-left.webp`) abre o modal do **Nugget Stacker**: um jogo arcade retrô completo codificado em HTML5 Canvas e controlado por molas de Framer Motion (`damping: 28, stiffness: 340`), com controles via teclado e touch.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários

1. **Diretórios de Design Systems, UI Kits e Ferramentas para Desenvolvedores**:
   - Plataformas que reúnem centenas de recursos técnicos se beneficiam imensamente da hierarquia de chips, busca filtrada com ponto de estado ativo e cards de aspect-ratio 16:10.
2. **Hubs de Conteúdo Curado, Acervos Digitais & Bibliotecas de Referência**:
   - Os cards específicos para livros (`card--book` com aspect-ratio 2:3) e os mosaicos de coleções (`collection-mosaic`) são a referência definitiva para bibliotecas de leitura, galerias de design e repositórios de conhecimento.
3. **Portais de Design Engineering & Creative Coding**:
   - Times que buscam passar uma imagem de "craft refinado" encontram no sistema de superfícies OKLCH e nas micro-interações táteis uma linguagem profissional e contemporânea.
4. **Marketplaces de Componentes e Prompts de IA**:
   - A combinação de busca semântica, contadores tabulares em tempo real e visualização de domínios/autores cria clareza imediata para navegação massiva.

### Papel no Ritmo Visual (Regra 60-30-10)

- **60% — Fundação Neutra e Silenciosa (Superfícies OKLCH)**:
  - Fundo `--surface-0` (`oklch(13% .012 260)` no tema escuro ou `oklch(98.5% .003 260)` no claro).
  - Linhas divisórias extremamente finas `--line` (`oklch(34% .012 260)`), criando contenção espacial sem poluição.
  - Tipografia neutra e legível com espaçamento modular de 4px (`--space-1` a `--space-24`).
- **30% — Camada de Fluidez e Feedback Tátil (Chips, Filtros e Cards)**:
  - `.home-chip` com badges de números tabulares (`--font-mono`), bordas dinâmicas e transições de hover de 120ms (`--motion-fast`).
  - `.search-box` com borda e halo âmbar ao focar (`box-shadow: 0 0 0 4px var(--accent-tint)`).
  - Cards com micro-elevações, monogramas de fallback quando não há imagem e hover em `--surface-2`.
- **10% — Efeitos Protagonistas / Showstoppers (Acentos de Assinatura)**:
  - O brilho radial dourado no topo do `.glass-panel`.
  - Mosaicos 2x2 com hover translateY e halos dourados de foco.
  - O modal interativo do mini-arcade Stacker com física de mola viva.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

- ⚠️ **Proibido em Aplicações Financeiras Tradicionais ou B2B Legadas**:
  - A combinação do mascote ilustrado, tipografia display lúdica (`Cute Dino`) e acento âmbar pode ser interpretada como informal em softwares hospitalares, ERPs bancários rígidos ou sistemas jurídicos.
- ⚠️ **Proibido em Ambientes sem Suporte a Espaços de Cor Modernos**:
  - Se a aplicação precisar rodar em webviews corporativas desatualizadas que não suportam CSS Color Module Level 4 (`oklch()`), o sistema exigirá transpilação ou fallbacks hexadecimais manuais via PostCSS/LightningCSS.
- ⚠️ **Anti-padrão: Poluição de Acentos Cromáticos Múltiplos**:
  - O sistema visual do Nugget foi rigorosamente orquestrado para um único tom de acento dourado (`oklch(52% .19 82)` / `oklch(78% .16 82)`). Adicionar simultaneamente botões roxos, badges azuis e gradientes arco-íris destrói a coesão estética e o senso de curadoria do design.
- ⚠️ **Anti-padrão: Negligenciar `tabular-nums` nos Contadores**:
  - Usar contadores numéricos sem a classe `.tabular` ou sem `font-variant-numeric: tabular-nums` causa trepidação horizontal do layout quando os dígitos mudam, quebrando a sensação de precisão do craft.
- ⚠️ **Anti-padrão: Remover Monogramas de Fallback em Cards**:
  - Carregar favicons ou imagens externas sem o fallback atômico de monograma tipográfico (`.card-monogram`) resulta em quebras visuais graves quando links externos falham.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

### 1. `HomeChip` & `HomeChipsBar` (Pílulas de Categoria com Contador Tabular)
- **Anatomia Visual**: Pílula horizontal (`border-radius: 999px`) em `--surface-1` com borda fina de 1px `--line`. Contém o rótulo da categoria em 13px (font-weight 500) e um mini-badge aninhado (`.home-chip-count`) com fundo `--surface-2`, texto em 11px semi-bold e números tabulares (`tabular-nums`). No estado ativo, ganha fundo translúcido âmbar (`#f4b7202e`) e borda dourada vívida (`#f4b720`).
- **Gatilho de Interação**: Hover (transição rápida de 120ms para `--accent-tint` e texto `--text-1`), Click (toggle da categoria com re-cálculo instantâneo da contagem).
- **Onde encaixar na página**: Logo abaixo da barra de busca principal, servindo como seletor primário de taxonomia da plataforma.

### 2. `GlassPanelHeader` (Cabeçalho com Iluminação Radial Difusa)
- **Anatomia Visual**: Barra de navegação com altura fixa, `backdrop-filter: blur(12px)` e um gradiente elíptico fixo no topo (`radial-gradient(ellipse 100% 100% at top, var(--accent-tint), transparent 65%)`). Incorpora o wordmark em `Cute Dino`, botão de extensão do Chrome, alternador de tema e link de submissão.
- **Gatilho de Interação**: Scroll contínuo (permanece fixo no topo com aceleração `transform: translateZ(0)`).
- **Onde encaixar na página**: Topo absoluto da aplicação (`sticky` ou `fixed`).

### 3. `PrecisionSearchBox` (Campo de Busca com Filtro Aninhado & Halo Dourado)
- **Anatomia Visual**: Pílula de 60px de altura, largura máxima de 520px, com padding interno generoso, ícone de lupa minimalista, campo de texto sem borda de 17px e botão de filtro aninhado com ponto de estado ativo (`.search-box-filter-dot`). Ao focar, o anel de foco não usa outline áspero, mas sim: `border-color: var(--accent); box-shadow: 0 0 0 4px var(--accent-tint)`.
- **Gatilho de Interação**: Focus (expansão do halo), Input (acionamento do filtro semântico client-side em tempo real), Botão Clear `×` (limpeza imediata).
- **Onde encaixar na página**: Hero central de páginas de exploração ou cabeçalho colapsado em navegação secundária.

### 4. `ResourceCard` (Card Padrão de Recurso com Aspect Ratio 16:10)
- **Anatomia Visual**: Card vertical de raio 14px (`--radius-card`) com mídia de topo em proporção 16:10 (`.card-media`), screenshot de alta fidelidade e monograma SVG de fallback. No corpo (`.card-body`), apresenta título em negrito sutil, descrição editorial em duas linhas com ellipsis e tag de domínio (`.card-domain`) com ícone de link externo.
- **Gatilho de Interação**: Hover com elevação sutil de borda para `--line-strong`, transição de fundo para `--surface-2` e sombra suave `0 8px 20px oklch(0% 0 0 / .08)`.
- **Onde encaixar na página**: Grids de conteúdo principal de 2 a 4 colunas (`.card-grid`).

### 5. `BookSpecimenCard` (Card Editorial para Livros de Craft Proporção 2:3)
- **Anatomia Visual**: Variação `.card--book` especialmente calibrada para capas de livros físicos. O contêiner de mídia adota proporção estrita de 2:3 com fundo `--surface-2`. Apresenta autor do livro em tipografia secundária e selo de afiliação ou link para leitura.
- **Gatilho de Interação**: Hover idêntico ao card base com animação suave de imagem via object-fit.
- **Onde encaixar na página**: Seção de livros recomendados e biblioteca de teoria de design.

### 6. `CollectionMosaicCard` (Mosaico 2x2 com Elevação Cinética)
- **Anatomia Visual**: Grade de 2 colunas e 2 linhas com `gap: 3px`, preenchida com as quatro primeiras páginas reais da coleção (ex: 4 capturas reais de páginas de Preços do Linear, Stripe, Raycast e PostHog). Bordas arredondadas e metadados na base com contagem de sites (`X sites curados`).
- **Gatilho de Interação**: Hover com elevação tridimensional `transform: translateY(-3px)`, alteração de borda e sombra profunda. Foco com halo dourado `0 0 0 4px var(--accent-tint)`.
- **Onde encaixar na página**: Galeria temática de coleções (`/collections`).

### 7. `ArcadeStackerModal` (Modal do Jogo Retrô com Molas Framer Motion)
- **Anatomia Visual**: Modal de 340px de largura com fundo `#15171d`, borda fina escura e sombra profunda de sobreposição. Contém HUD no topo com `Score` e `Level` em números tabulares, canvas HTML5 central com grade de blocos que oscilam e painel de controle com botões direcionais e queda rápida (`⤓`).
- **Gatilho de Interação**: Gatilho oculto por 3 cliques no mascote. Entrada suave via mola Framer Motion (`type: "spring", damping: 28, stiffness: 340`). Controle por teclado (`ArrowLeft`, `ArrowRight`, `ArrowUp` para girar, `Space` para travar/cair).
- **Onde encaixar na página**: Easter egg integrado ao rodapé ou menu de desenvolvedor.

### 8. `MascotEasterEggTrigger` (Mascote Reativo com Contador de Toques)
- **Anatomia Visual**: Ilustração do mascote apontando para o formulário de newsletter (`/nugget-pointing-left.webp`).
- **Gatilho de Interação**: Toque/Clique com micro-escala física `whileTap={{ scale: 0.92 }}` e mola com curva `[0.16, 1, 0.3, 1]`. Um contador interno rastreia 3 cliques num intervalo de tempo; ao atingir o terceiro clique, abre o modal do Stacker Arcade.
- **Onde encaixar na página**: Ao lado de formulários de newsletter ou seções de fechamento de página.

### 9. `MicroVoteButton` (Botão de Upvote/Downvote com Escala no Toque)
- **Anatomia Visual**: Par de setas minimalistas SVG com contador numérico no centro em `--font-mono`.
- **Gatilho de Interação**: Hover para clarear de `--text-3` para `--text-1`; `:active` com compressão elástica `transform: scale(0.9)`; no clique positivo, ganha a classe `.active-up` com coloração verde esmeralda perceptual `--success: oklch(74% .12 155)`.
- **Onde encaixar na página**: Listas de recursos contribuídos pela comunidade (`crowd-favorites`).

### 10. `MobileSearchSheet` (Drawer Inferior de Busca para Dispositivos Móveis)
- **Anatomia Visual**: Gaveta inferior que sobe com fundo `--surface-1`, borda superior arredondada de 20px, backdrop escurecido e área de toque mínima garantida de 44px para dedos (`min-height: 44px`).
- **Gatilho de Interação**: Tap no botão flutuante de busca móvel (`.mobile-search-fab`).
- **Onde encaixar na página**: Viewports menores que 640px.

### 11. `SubmitToolSheet` (Formulário Elegante com Selects Customizados)
- **Anatomia Visual**: Painel de submissão em grid de 2 colunas com inputs de texto, labels pequenas em 12px semi-bold (`--text-2`), textareas sem resize manual e selects com seta vetorial SVG inline embutida via `background-image` e padding dinâmico compensado.
- **Gatilho de Interação**: Foco de inputs com troca de cor para `--accent` e transição rápida de 120ms.
- **Onde encaixar na página**: Modal ou gaveta lateral para contribuição comunitária de ferramentas.

### 12. `NewTabExtensionHero` (Módulo de Apresentação da Extensão de Navegador)
- **Anatomia Visual**: Mockup imersivo da interface da extensão de aba do navegador (`Nugget Tab`), apresentando a barra de busca e a grade de inspiração do dia diretamente renderizada.
- **Gatilho de Interação**: Botão primário dourado com link direto para a Chrome Web Store e badges de avaliação.
- **Onde encaixar na página**: Seção de rodapé promocional ou rota dedicada `/nugget-tab`.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

```bash
# Dependências essenciais no ecossistema React / Tailwind
npm install framer-motion lucide-react clsx tailwind-merge canvas-confetti
npm install -D @tailwindcss/postcss postcss
```

### Configuração de Design Tokens OKLCH (CSS Global / Tailwind)

```css
/* styles/tokens.css */
:root {
  /* Fontes */
  --font-wordmark: "Cute Dino", var(--font-sans);
  --font-sans: -apple-system, system-ui, "Segoe UI", Roboto, "Geist Sans", sans-serif;
  --font-mono: ui-monospace, "SF Mono", Consolas, monospace;

  /* Superfícies - Tema Claro */
  --surface-0: oklch(98.5% 0.003 260);
  --surface-1: oklch(100% 0 0);
  --surface-2: oklch(96% 0.004 260);
  --surface-3: oklch(100% 0 0);

  /* Linhas & Bordas */
  --line: oklch(91% 0.006 260);
  --line-strong: oklch(83% 0.008 260);

  /* Tipografia */
  --text-1: oklch(20% 0.012 260);
  --text-2: oklch(42% 0.012 260);
  --text-3: oklch(52% 0.012 260);

  /* Acento Dourado Nugget */
  --accent: oklch(52% 0.19 82);
  --accent-hover: oklch(46% 0.19 82);
  --accent-tint: oklch(52% 0.19 82 / 0.1);
  --accent-tint-strong: oklch(52% 0.19 82 / 0.18);
  --on-accent: oklch(99% 0.01 90);

  /* Estados */
  --success: oklch(48% 0.13 155);
  --warning: oklch(54% 0.15 55);
  --danger: oklch(50% 0.19 25);

  /* Raios e Sombras */
  --radius-input: 8px;
  --radius-card: 14px;
  --radius-modal: 20px;
  --radius-pill: 999px;
  --shadow-overlay: 0 0 0 1px oklch(0% 0 0 / 0.08), 0 24px 60px oklch(0% 0 0 / 0.16);
  --shadow-card-hover: 0 8px 20px oklch(0% 0 0 / 0.08);

  /* Cinética & Easing */
  --motion-fast: 0.12s;
  --motion-base: 0.2s;
  --motion-slow: 0.32s;
  --ease-out: cubic-bezier(0.16, 1, 0.3, 1);
}

/* Tema Escuro Automático e por Atributo */
[data-theme="dark"],
:root:not([data-theme="light"]) {
  @media (prefers-color-scheme: dark) {
    --surface-0: oklch(13% 0.012 260);
    --surface-1: oklch(21% 0.012 260);
    --surface-2: oklch(26% 0.012 260);
    --surface-3: oklch(30% 0.012 260);
    --line: oklch(34% 0.012 260);
    --line-strong: oklch(42% 0.014 260);
    --text-1: oklch(93% 0.005 260);
    --text-2: oklch(70% 0.01 260);
    --text-3: oklch(65% 0.012 260);
    --accent: oklch(78% 0.16 82);
    --accent-hover: oklch(83% 0.16 82);
    --accent-tint: oklch(78% 0.16 82 / 0.12);
    --accent-tint-strong: oklch(78% 0.16 82 / 0.22);
    --on-accent: oklch(14% 0.02 78);
    --shadow-overlay: 0 0 0 1px oklch(0% 0 0 / 0.3), 0 24px 60px oklch(0% 0 0 / 0.45);
    --shadow-card-hover: 0 8px 20px oklch(0% 0 0 / 0.35);
  }
}
```

### Física de Movimento e Transições

- **Curva Suave Quintic Out**: `cubic-bezier(0.16, 1, 0.3, 1)` para todas as transições de cor, borda, sombra e elevação.
- **Mola de Abertura de Modais e Easter Eggs**:
  - `type: "spring"`
  - `damping: 28`
  - `stiffness: 340`
  - `mass: 1`
- **Micro-toques Táteis (Active State)**:
  - `whileTap={{ scale: 0.92 }}` com duração de 150ms.

---

### Receita de Código Funcional 1: Pílulas de Categoria & Motor de Busca com Stop-Words

```tsx
import React, { useState, useMemo } from "react";
import { Search, X, SlidersHorizontal } from "lucide-react";

// Dicionário de stop-words semânticas extraído da engenharia do Nugget Design
const STOP_WORDS = new Set([
  "i", "im", "i'm", "am", "is", "are", "was", "trying", "try", "want", "wanna",
  "need", "needs", "looking", "look", "to", "for", "of", "on", "in", "at", "a",
  "an", "the", "my", "our", "me", "us", "you", "your", "some", "any", "good",
  "great", "nice", "cool", "best", "beautiful", "awesome", "amazing", "inspiring",
  "ideas", "idea", "inspiration", "inspo", "examples", "example"
]);

export interface Category {
  slug: string;
  label: string;
  count: number;
}

interface SearchFilterProps {
  categories: Category[];
  selectedCategory: string | null;
  onSelectCategory: (slug: string | null) => void;
  searchQuery: string;
  onSearchChange: (query: string) => void;
}

export function NuggetSearchFilter({
  categories,
  selectedCategory,
  onSelectCategory,
  searchQuery,
  onSearchChange,
}: SearchFilterProps) {
  const [filterActive, setFilterActive] = useState(false);

  // Limpeza semântica da busca
  const cleanTokens = useMemo(() => {
    return searchQuery
      .toLowerCase()
      .split(/\s+/)
      .filter((word) => word.length > 0 && !STOP_WORDS.has(word));
  }, [searchQuery]);

  return (
    <div className="w-full flex flex-col items-center gap-6 py-8">
      {/* Search Box Principal */}
      <div className="relative w-full max-w-[540px]">
        <div
          className="flex items-center gap-3 w-full h-[60px] px-5 rounded-full transition-all duration-150"
          style={{
            backgroundColor: "var(--surface-1)",
            border: "1px solid var(--line)",
            boxShadow: searchQuery ? "0 0 0 4px var(--accent-tint)" : "none",
          }}
        >
          <Search className="w-5 h-5 flex-none" style={{ color: "var(--text-3)" }} />
          <input
            type="text"
            value={searchQuery}
            onChange={(e) => onSearchChange(e.target.value)}
            placeholder="Search tools, components, or ask for inspiration..."
            className="flex-1 bg-transparent border-none outline-none text-[16px] text-ellipsis overflow-hidden"
            style={{ color: "var(--text-1)" }}
          />

          {searchQuery && (
            <button
              type="button"
              onClick={() => onSearchChange("")}
              className="w-6 h-6 flex items-center justify-center rounded-full hover:opacity-75 transition-opacity"
              style={{ color: "var(--text-3)" }}
              aria-label="Clear search"
            >
              <X className="w-4 h-4" />
            </button>
          )}

          <button
            type="button"
            onClick={() => setFilterActive(!filterActive)}
            className="relative flex items-center justify-center w-9 h-9 rounded-full transition-colors"
            style={{
              backgroundColor: filterActive ? "var(--accent-tint)" : "var(--surface-2)",
              color: filterActive ? "var(--accent)" : "var(--text-2)",
            }}
            aria-label="Filter options"
          >
            <SlidersHorizontal className="w-4 h-4" />
            {filterActive && (
              <span
                className="absolute top-1.5 right-1.5 w-2 h-2 rounded-full"
                style={{ backgroundColor: "var(--accent)" }}
              />
            )}
          </button>
        </div>

        {cleanTokens.length > 0 && cleanTokens.join(" ") !== searchQuery.toLowerCase().trim() && (
          <p className="absolute -bottom-5 left-6 text-[11px] font-mono tracking-tight" style={{ color: "var(--text-3)" }}>
            semantic matching: <span style={{ color: "var(--accent)" }}>{cleanTokens.join(", ")}</span>
          </p>
        )}
      </div>

      {/* Pílulas de Categoria (Category Chips) */}
      <div className="flex flex-wrap items-center justify-center gap-2 max-w-4xl px-4">
        {categories.map((cat) => {
          const isActive = selectedCategory === cat.slug;
          return (
            <button
              key={cat.slug}
              type="button"
              onClick={() => onSelectCategory(isActive ? null : cat.slug)}
              className="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full text-[13px] font-medium transition-all"
              style={{
                backgroundColor: isActive ? "oklch(52% 0.19 82 / 0.18)" : "var(--surface-1)",
                borderColor: isActive ? "var(--accent)" : "var(--line)",
                borderWidth: "1px",
                borderStyle: "solid",
                color: isActive ? "var(--text-1)" : "var(--text-2)",
                transitionDuration: "var(--motion-fast)",
                transitionTimingFunction: "var(--ease-out)",
              }}
            >
              <span>{cat.label}</span>
              <span
                className="px-1.5 py-0.5 rounded-full text-[11px] font-mono font-semibold"
                style={{
                  backgroundColor: isActive ? "var(--accent)" : "var(--surface-2)",
                  color: isActive ? "var(--on-accent)" : "var(--text-3)",
                  fontVariantNumeric: "tabular-nums",
                }}
              >
                {cat.count}
              </span>
            </button>
          );
        })}
      </div>
    </div>
  );
}
```

---

### Receita de Código Funcional 2: Card de Recurso & Mosaico de Coleção 2x2

```tsx
import React from "react";
import { ExternalLink, Bookmark } from "lucide-react";

export interface ResourceItem {
  id: string;
  name: string;
  description: string;
  url: string;
  imageUrl?: string;
  category: string;
  domain: string;
  isBook?: boolean;
}

export function NuggetResourceCard({ item }: { item: ResourceItem }) {
  return (
    <article
      className="group flex flex-col rounded-[14px] overflow-hidden transition-all duration-200"
      style={{
        backgroundColor: "var(--surface-1)",
        border: "1px solid var(--line)",
      }}
      onMouseEnter={(e) => {
        e.currentTarget.style.borderColor = "var(--line-strong)";
        e.currentTarget.style.backgroundColor = "var(--surface-2)";
        e.currentTarget.style.boxShadow = "var(--shadow-card-hover)";
      }}
      onMouseLeave={(e) => {
        e.currentTarget.style.borderColor = "var(--line)";
        e.currentTarget.style.backgroundColor = "var(--surface-1)";
        e.currentTarget.style.boxShadow = "none";
      }}
    >
      {/* Contêiner de Imagem com proporção 16:10 ou 2:3 para Livros */}
      <div
        className="w-full relative flex items-center justify-center overflow-hidden"
        style={{
          aspectRatio: item.isBook ? "2/3" : "16/10",
          backgroundColor: "var(--surface-2)",
        }}
      >
        {item.imageUrl ? (
          <img
            src={item.imageUrl}
            alt={item.name}
            loading="lazy"
            decoding="async"
            className="w-full h-full object-cover group-hover:scale-[1.02] transition-transform duration-300"
          />
        ) : (
          <div
            className="w-12 h-12 rounded-xl flex items-center justify-center font-bold text-xl uppercase"
            style={{
              backgroundColor: "var(--surface-3)",
              color: "var(--accent)",
              border: "1px solid var(--line)",
            }}
          >
            {item.name.slice(0, 2)}
          </div>
        )}
      </div>

      {/* Corpo do Card */}
      <div className="p-4 flex flex-col gap-2 flex-1 justify-between">
        <div>
          <h3 className="text-[16px] font-semibold tracking-tight" style={{ color: "var(--text-1)" }}>
            {item.name}
          </h3>
          <p className="text-[13px] leading-relaxed line-clamp-2 mt-1" style={{ color: "var(--text-2)" }}>
            {item.description}
          </p>
        </div>

        <div className="flex items-center justify-between pt-2 border-t mt-2" style={{ borderColor: "var(--line)" }}>
          <span className="text-[12px] font-mono tracking-tight" style={{ color: "var(--text-3)" }}>
            {item.domain}
          </span>
          <a
            href={item.url}
            target="_blank"
            rel="noopener noreferrer"
            className="p-1 rounded-md hover:opacity-75 transition-opacity"
            style={{ color: "var(--text-3)" }}
            aria-label={`Open ${item.name}`}
          >
            <ExternalLink className="w-3.5 h-3.5" />
          </a>
        </div>
      </div>
    </article>
  );
}

// Mosaico 2x2 para Coleções Temáticas
export function NuggetCollectionMosaicTile({
  title,
  siteCount,
  previews,
  onClick,
}: {
  title: string;
  siteCount: number;
  previews: string[];
  onClick?: () => void;
}) {
  return (
    <div
      onClick={onClick}
      className="cursor-pointer group flex flex-col gap-2 transition-transform duration-200"
    >
      <div
        className="w-full grid grid-cols-2 gap-[3px] rounded-[14px] overflow-hidden p-[2px] transition-all duration-200 group-hover:-translate-y-1"
        style={{
          aspectRatio: "16/10",
          backgroundColor: "var(--surface-2)",
          border: "1px solid var(--line)",
        }}
      >
        {previews.slice(0, 4).map((src, i) => (
          <img
            key={i}
            src={src}
            alt=""
            loading="lazy"
            className="w-full h-full object-cover object-top"
            style={{ backgroundColor: "var(--surface-1)" }}
          />
        ))}
      </div>
      <div className="px-1 flex items-center justify-between">
        <h4 className="text-[15px] font-semibold" style={{ color: "var(--text-1)" }}>
          {title}
        </h4>
        <span className="text-[12px] font-mono" style={{ color: "var(--text-3)", fontVariantNumeric: "tabular-nums" }}>
          {siteCount} sites
        </span>
      </div>
    </div>
  );
}
```

---

### Receita de Código Funcional 3: Mascot Trigger & Easter Egg Stacker Modal (Framer Motion)

```tsx
import React, { useState } from "react";
import { motion, AnimatePresence } from "framer-motion";
import { X } from "lucide-react";

interface StackerModalProps {
  isOpen: boolean;
  onClose: () => void;
}

export function NuggetStackerModal({ isOpen, onClose }: StackerModalProps) {
  const [score, setScore] = useState(0);
  const [level, setLevel] = useState(1);

  return (
    <AnimatePresence>
      {isOpen && (
        <>
          {/* Backdrop Escurecido */}
          <motion.div
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            exit={{ opacity: 0 }}
            transition={{ duration: 0.2 }}
            onClick={onClose}
            className="fixed inset-0 z-50 bg-black/60 backdrop-blur-sm"
          />

          {/* Modal Central com Mola Viva */}
          <motion.div
            role="dialog"
            aria-modal="true"
            aria-label="Nugget Stacker Easter Egg"
            initial={{ opacity: 0, scale: 0.94, y: 12 }}
            animate={{ opacity: 1, scale: 1, y: 0 }}
            exit={{ opacity: 0, scale: 0.94, y: 12 }}
            transition={{ type: "spring", damping: 28, stiffness: 340 }}
            className="fixed inset-0 m-auto z-51 w-[min(360px,100vw-32px)] h-fit max-h-[calc(100dvh-32px)] p-6 rounded-[20px] text-center shadow-2xl flex flex-col items-center"
            style={{
              backgroundColor: "#15171d",
              border: "1px solid oklch(30% 0.014 260)",
            }}
          >
            <button
              type="button"
              onClick={onClose}
              aria-label="Close"
              className="absolute top-4 right-4 text-zinc-400 hover:text-white text-lg"
            >
              <X className="w-5 h-5" />
            </button>

            <h2 className="text-[19px] font-bold text-zinc-100">You found Nugget Stacker</h2>
            <p className="text-[13px] text-zinc-400 mt-1 mb-4">
              An easter egg. Stack the nuggets, clear the rows.
            </p>

            {/* HUD */}
            <div className="flex items-center justify-between w-full px-4 py-2 mb-3 bg-zinc-900/80 rounded-lg text-xs font-mono text-zinc-300">
              <span>Score: <strong className="text-amber-400 font-mono">{score}</strong></span>
              <span>Level: <strong className="text-amber-400 font-mono">{level}</strong></span>
            </div>

            {/* Canvas Placeholder para o Arcade Game */}
            <div className="w-[280px] h-[320px] bg-black/80 rounded-lg border border-zinc-800 flex items-center justify-center text-zinc-500 font-mono text-xs">
              [Canvas Arcade Engine]
            </div>

            <p className="text-[11px] text-zinc-500 mt-3 font-mono">
              Press Space to drop, Arrow keys to steer.
            </p>
          </motion.div>
        </>
      )}
    </AnimatePresence>
  );
}

// Mascote com gatilho de 3 toques
export function NuggetNewsletterWithEasterEgg() {
  const [clickCount, setClickCount] = useState(0);
  const [modalOpen, setModalOpen] = useState(false);

  const handleMascotClick = () => {
    const next = clickCount + 1;
    if (next >= 3) {
      setClickCount(0);
      setModalOpen(true);
    } else {
      setClickCount(next);
    }
  };

  return (
    <section className="relative w-full max-w-xl mx-auto p-6 rounded-2xl flex items-center justify-between" style={{ backgroundColor: "var(--surface-1)", border: "1px solid var(--line)" }}>
      <div>
        <h3 className="font-semibold text-lg" style={{ color: "var(--text-1)" }}>Stay in the loop</h3>
        <p className="text-sm" style={{ color: "var(--text-2)" }}>Hand-picked updates on design-engineering craft.</p>
      </div>

      <motion.img
        src="/nugget-pointing-left.webp"
        alt="Nugget Mascot"
        onClick={handleMascotClick}
        whileTap={{ scale: 0.92 }}
        className="w-16 h-16 cursor-pointer select-none"
        title="What happens if you click 3 times?"
      />

      <NuggetStackerModal isOpen={modalOpen} onClose={() => setModalOpen(false)} />
    </section>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar e especificar a estética do **Nugget Design** no documento de arquitetura de um novo projeto, a IA deve seguir as diretrizes rigorosas abaixo:

1. **Declaração Formal de Identidade**:
   - `Visual Archetype`: *Design-Engineering Curated Directory & Modern Craft Feed*.
   - `Color Engine`: *OKLCH Perceptual Spectrum* com luminosidade calibrada e acento dourado âmbar (`oklch(52% .19 82)` para Light e `oklch(78% .16 82)` para Dark).
   - `Display Identity`: Wordmark lúdico contrastado com corpo de texto técnico e números mono tabulares.

2. **Checklist de Regras de Implementação**:
   - [ ] **Proibição de Hexadecimais em Superfícies**: Todas as superfícies devem usar os 4 níveis de elevação `--surface-0` a `--surface-3` para assegurar transições coerentes de tema.
   - [ ] **Obrigatoriedade de `tabular-nums`**: Todo badge numérico, contador de filtros, contador de votos ou pontuação deve ter a classe `.tabular` aplicada.
   - [ ] **Fallback de Monograma para Mídias**: Todo card que dependa de screenshots de URLs de terceiros deve conter fallback de monograma SVG com as duas primeiras iniciais em `--surface-3`.
   - [ ] **Curva de Transição Global**: Usar estritamente `cubic-bezier(0.16, 1, 0.3, 1)` para transições de 120ms (`--motion-fast`) e 200ms (`--motion-base`).
   - [ ] **Gradiente Fixo Superior**: Na navbar ou no hero principal, aplicar o gradiente elíptico fixo com `backdrop-filter: blur(12px)` e aceleração `translateZ(0)`.
   - [ ] **Parser de Stop-Words na Busca**: Em diretórios ou buscadores, implementar a remoção em tempo real de termos como *"i want"*, *"cool"*, *"best"*, conectando a intenção do usuário aos dados indexados.
