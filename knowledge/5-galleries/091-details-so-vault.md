---
id: "details-so-vault"
name: "Details.so Vault"
url: "https://www.details.so/vault"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico: ["Precision Tactile Craft", "Warm Obsidian Dark UI", "Layered Micro-Shadows & Inset Glows", "Superellipse Geometry (Squircle)", "Kinetic Spring Feedback & Micro-Interactions", "AI-Native Component Vault"]
densidade_informacao: "Alta/Utilitaria"
impacto_visual: "Editorial/Sofisticado"
custo_computacional: "Baixo a Moderado (CSS Nativo, GPU Transforms, WebGL Shaders pontuais)"
stack_frameworks: ["Astro v6", "React 19 / 18", "Tailwind CSS v4", "Motion (Framer Motion) / Motion One", "Swup Page Transitions", "Vanilla JS / Webflow", "Model Context Protocol (MCP)"]
compatibilidade:
  fontes_ideais: ["Season Collection (Variable Serif/Sans)", "Geist Sans", "PP Neue Montreal", "SF Pro Display", "JetBrains Mono", "Berkeley Mono"]
  paletas_ideais: ["Warm Obsidian Black (hsl(20, 14%, 4%))", "Molten Neon Amber / Tangerine (#f25500 / #e06500)", "CIE Lab Crisp Whites (lab(96.5% -0.1 0.36))", "Graphite Hairline Alpha (border-1: hsl(30, 6%, 15%), white/10)", "Warm Cream Alabaster (hsl(30, 7%, 95%))"]
  combinacoes_recomendadas: ["Radix UI / Shadcn UI (fundação semântica e de acessibilidade)", "Lucide Icons", "Motion (Framer Motion)", "Tailwind CSS v4", "Details MCP Server"]
  conflitos_esteticos: ["Flat Design sem profundidade de luz (sombras duras em bloco ou elevações planas)", "Bordas pretas pesadas de 3px típicas de Neo-brutalismo", "Paletas pastéis dessaturadas do Corporate Memphis", "Bordas arredondadas circulares genéricas sem suavização de curvatura (superellipse)"]
---

# Details.so Vault — Dossiê Estético, Anatomia de Layout & Padrões de Micro-Interação

## 1. DNA Estético & Filosofia de Curadoria

O **Details.so Vault** (`https://www.details.so/vault`) representa o ápice da escola de **Craft UI & Precision Engineering** no ecossistema web contemporâneo. Sob o lema fundador *"Copy-paste animations and interaction code, crafted by hand for production. The details AI can't replicate"*, o Vault não opera como uma galeria estática tradicional de capturas de tela (como Mobbin ou Dribbble), mas sim como um **cofre ativo de soluções de engenharia tátil de alta fidelidade**, dissecadas até o nível de micro-tokens CSS, físicas de mola (`springs`), shaders pontuais e conexões nativas via **Model Context Protocol (MCP)** para agentes autônomos de código (Claude Code, Cursor, Codex e v0).

### Pilares Fundamentais do DNA Visual:

1. **A Estética "Warm Obsidian" e Luz Microscópica**:
   Diferente do modo escuro monocromático industrial frio (`#000000` puro com tons de cinza azulados frios), o Vault ancora sua paleta em tons quentes de obsidiana: o fundo base opera em `hsl(20, 14%, 4%)` e as superfícies elevadas transitam em camadas graduais (`hsl(20, 5%, 12%)`, `hsl(20, 5%, 17%)`, `hsl(20, 5%, 25%)`). O branco tipográfico não é um `#FFFFFF` estourado, mas calculado no espaço perceptivo CIE Lab (`lab(96.5% -0.1 0.36)`), eliminando fadiga visual enquanto realça micro-contrastes.

2. **Hierarquia Tátil Subpixel (Layered Shadows & Inset Highlights)**:
   A sensação de profundidade de hardware físico é obtida pela combinação de duas camadas simultâneas:
   - Uma sombra ambiente suave e difusa de dispersão vertical (`0px 8px 12px 0px hsla(0, 0%, 0%, .04)`).
   - Um contorno de oclusão subpixel (`0px 0px 1px 0px hsl(0, 0%, 29%)` no dark mode ou `hsla(0, 0%, 0%, .62)` no light mode), simulando a quina refratada de um vidro chanfrado ou de uma carcaça de alumínio anodizado.

3. **Geometria de Superelipse (Squircle Craft)**:
   A interface rejeita o raio de curvatura circular clássico (`border-radius` padrão de quadrante circular) em favor de curvaturas contínuas de superelipse (`corner-shape: superellipse(1.2)` e raios modulares de 8px, 18px, 24px, 28px até 34px), proporcionando uma transição orgânica entre retas e cantos curva-a-curva idêntica à do hardware da Apple e do design de produto industrial premium.

4. **Física Cinética Mecânica (Mechanical Compress & Linear Spring Approximation)**:
   Cada interação possui peso e amortecimento inercial. O feedback tátil ao pressionar botões ativa uma escala imediata (`transform: scale(0.97)`) com duração ultra-curta (`0.15s ease`), enquanto elementos flutuantes de navegação (como a Dynamic Island central) utilizam a função CSS `linear(...)` de aproximação de mola contínua com mais de 50 pontos de amostragem (`--elastic`), entregando a sensação de mola física sem a necessidade de importar runtimes JS pesados.

5. **AI-Ready Context Protocol (A Biblioteca Viva para Agentes)**:
   O Details.so implementa uma arquitetura inédita: todo recurso do Vault possui uma versão markdown gêmea pública (`/vault/<slug>.md`) e um endpoint de MCP Streamable HTTP (`https://api.details.so/mcp`), permitindo que assistentes de IA busquem o código-fonte exato, especificações de timing e vídeos de teste em tempo real.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários

1. **Ferramentas de Desenvolvedor e Plataformas SaaS de Vanguarda**:
   Produtos onde a audiência é formada por engenheiros, fundadores técnicos e designers criteriosos (ex: Linear, Supabase, Raycast, Vercel, Resend). A estética transmite solidez arquitetônica, respeito à latência e maestria de código.
2. **Estúdios de Design Digital, Creative Agencies e Portfólios de Elite**:
   Aplicações onde o próprio acabamento da interface é a prova de competência técnica e refinamento de direção de arte da equipe.
3. **Fintechs de Nova Geração e Wealth Management de Alto Padrão**:
   Aplicações que exigem densidade funcional, cartões de alta precisão, toggles de moeda/período e microinterações que passam a segurança de um cofre bancário suíço modernizado.
4. **Command Bars, Menus Flutuantes e Interfaces Espaciais**:
   Painéis de comando flutuantes (Dynamic Islands, drawers com slide amortecido, popovers que respeitam colisão de viewport).

### Aplicação na Regra 60-30-10

- **60% (Superfície Primária / Canvas)**:
  - **Dark Mode**: Fundo em Warm Obsidian profundo (`hsl(20, 14%, 4%)` / `#0d0b0a`) com margens laterais de ancoragem de 8px (`.app:before`, `.app:after`).
  - **Light Mode**: Superfície Alabaster natural (`hsl(30, 10%, 100%)` / `#ffffff` / `--surface-1`).
- **30% (Superfície Secundária, Cartões e Estrutura Tipográfica)**:
  - Painéis elevados em `--surface-2` (`hsl(20, 5%, 12%)`) e `--surface-3` (`hsl(20, 5%, 17%)`).
  - Hairline borders ultrafinas em `1px solid hsl(30, 6%, 15%)` ou `border-white/10`.
  - Tipografia de leitura em branco perceptual (`lab(96.5% -0.1 0.36)`) e texto de apoio em grafite mineral (`lab(66.2% 1.88 3.2)`).
- **10% (Acentos de Alta Intensidade & Micro-Feedback)**:
  - **Molten Neon Tangerine** (`--accent: #f25500` no dark, `#e06500` no light), reservado com extrema disciplina para: anéis de foco (`:focus-visible`), badges de novidade (`--accent-10: #f255001a`), seleções de texto (`::selection`), e micro-indicadores luminosos.
  - Efeito glint metálico em badges (`card-badge-shimmer-text`) com deslocamento horizontal de gradiente em 1.8s.

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

### ⚠️ Incompatível com:
- **Sistemas Corporativos Legados ou Intranets de Baixo Suporte Tecnológico**: O sistema depende de recursos modernos da especificação CSS (tais como `color-mix(in srgb, ...)`, `superellipse()`, valores de cor em `lab()`, e pseudo-classes `@starting-style` para animação de abertura de drawers/dropdowns nativos). Em navegadores desatualizados, o design degrada severamente.
- **Interfaces Infantis, Jogos Casuais ou Produtos Populares Lúdicos**: A austeridade geométrica, o contraste rigoroso e o peso metálico do design colidem diretamente com estéticas coloridas, arredondadas estilo chiclete ("bubblegum") ou ilustrações volumétricas 3D cartunescas.
- **Portais de Conteúdo Massivo e Noticiosos com Textos Extensos**: O uso intenso de superfícies obsidian e micro-bordas luminescentes é otimizado para densidade de ferramentas e seções de conversão, podendo fatigar o leitor em artigos de 10.000 palavras onde um fundo editorial neutro é mais adequado.

### ⚠️ Armadilhas de Imitação (Anti-Padrões):
1. **Excesso de Backdrop Blur Desenfreado**: Aplicar `backdrop-filter: blur(20px)` em dezenas de cartões ao mesmo tempo destrói a taxa de quadros (FPS) da GPU em dispositivos móveis. O padrão do Vault aplica desfoques escopados (Progressive Blur com máscara gradiente) apenas em elementos flutuantes de cabeçalho (`island`) e modais.
2. **Sombras Pesadas em Bloco (Heavy Drop-Shadows)**: Tentar simular profundidade usando sombras escuras de 30px com alta opacidade sem o hairline border de 1px transforma a interface em um neumorfismo sujo e datado. A assinatura do Vault é a precisão cirúrgica de sombras de 4px a 8px com opacidade ultra-baixa (3% a 4%) ancoradas por um fio de contorno subpixel.
3. **Ignorar o Estado Ativo de Pressão (`:active`)**: Criar botões que têm hover bonito mas não respondem com encolhimento físico (`scale(0.97)`) na pressão mecânica remove toda a identidade tátil do sistema.
4. **Violar a Acessibilidade de Foco**: Tentar esconder anéis de foco para manter o visual "limpo". O Vault prescreve obrigatoriamente um anel de foco visível de 2px na cor de acento tangerina (`--focus-ring-color: var(--accent)`) com deslocamento de 2px (`--focus-ring-offset: 2px`).

---

## 4. Anatomia Estrutural & Catálogo Detalhado de Componentes

### 1. Arquitetura de Grid, Espaçamento & Ritmo
- **Contêiner Canônico**: Largura máxima restrita a `1400px` (`max-w-[1400px]`), com padding inline responsivo de `40px` no desktop e `24px` no mobile (`px-6 md:px-10`).
- **Margens de Borda da Aplicação (App Frame Bounds)**: A janela inteira do navegador é emoldurada por duas faixas estáticas laterais de 8px (`.app:before` e `.app:after`), conferindo a sensação de um console de hardware ou viewport contido.
- **Grade de Elevação Modular**:
  - `Surface-0`: `#000000` (Fundo absoluto)
  - `Surface-1`: `hsl(20, 14%, 4%)` (Piso da aplicação)
  - `Surface-2`: `hsl(20, 5%, 12%)` (Cartões e botões neutros)
  - `Surface-3`: `hsl(20, 5%, 17%)` (Superfícies ativas, hover e badges)
  - `Surface-4`: `hsl(20, 5%, 25%)` (Foco elevado e divisores interativos)

---

### Catálogo de Padrões Notáveis do Details Vault

#### 1. Morphing Dynamic Island (Header Navigation Pill)
- **Anatomia**: Barra de cabeçalho em formato de pílula flutuante (`clamp(320px, 31.25vw, 400px)`), contida em `border-radius: 9999px` com `corner-shape: var(--corner-shape)`. Contém painéis intercambiáveis com posicionamento absoluto (`data-island-pane="default"`, `data-island-pane="vault-detail"`, `data-island-pane="pricing"`).
- **Gatilho / Comportamento**: Ao transicionar de listagem geral para um recurso detalhado, o container expande ou contrai sua largura máxima suavemente via transição elástica (`transition: max-width .8s var(--elastic)`), enquanto o painel anterior desvanece com desfoque transitório (`filter: blur(6px); opacity: 0`) e os botões de ação lateral ("Voltar" e "Atualizar") deslizam para fora com translação de `100% + 6px`.
- **Onde Encaixar**: Cabeçalho global de navegação, status bar de ferramentas de produtividade, reprodutores multimídia e assistentes de IA flutuantes.

#### 2. Moving Highlight Indicator (Nav Pills & Theme Switcher)
- **Anatomia**: Elemento de realce flutuante (`.ui-dropdown__highlight` ou `.theme-switcher__highlight`) posicionado atrás dos itens de menu, com `pointer-events: none` e background em `--floating-surface-2`.
- **Gatilho / Comportamento**: Ao mover o mouse sobre os itens de navegação, um script mede o `getBoundingClientRect` do elemento alvo e injeta as variáveis CSS `--moving-highlight-x`, `--moving-highlight-y`, `--moving-highlight-width` e `--moving-highlight-height`. O elemento se move suavemente com curva quântica (`transform .24s var(--ease-out-quart), width .24s var(--ease-out-quart)`), dando a ilusão de um raio magnético líquido que abraça o item ativo.
- **Onde Encaixar**: Segmented controls de alternância de tema (Light/Dark/System), barras de abas superiores e menus suspensos de opções.

#### 3. Tactile Press Button (`.press:active`)
- **Anatomia**: Botão com background sólido de alto contraste (`--text-1`), texto invertido em `--surface-1`, raio de curvatura total (`rounded-full`) ou superelipse de 18px (`--border-radius-xs`).
- **Gatilho / Comportamento**: No estado `:active`, o botão contrai mecanicamente para `transform: scale(0.97)` através de `transition: transform .15s ease`. Ao soltar, restaura instantaneamente à escala 1.0 sem salto visual. Em caso de carregamento, o rótulo desvanece com `blur(4px)` e um spinner vetorial em SVG rotaciona suavemente no mesmo envelope de espaço.
- **Onde Encaixar**: Ações primárias de conversão, gatilhos de cópia de código ("Get Code", "Copy for AI") e modais de confirmação.

#### 4. Dual-Layer Shadow & Hairline Inset Border
- **Anatomia**: Composição CSS que dispensa bordas grossas através da fórmula:
  ```css
  box-shadow: 0px 8px 12px 0px hsla(0, 0%, 0%, 0.04), 0px 0px 1px 0px hsl(0, 0%, 29%);
  border: 1px solid hsl(30, 6%, 15%);
  ```
- **Gatilho / Comportamento**: Em repouso, o componente parece esculpido no próprio painel com um filete luminoso de 1px. No hover, o contorno pode aumentar sutilmente a reflectância misturando `border-color: color-mix(in srgb, var(--surface-2) 94%, var(--text-3))`.
- **Onde Encaixar**: Cartões de produto, popovers de comando, caixas de diálogo modais e painéis de precificação.

#### 5. Card Badge Shimmer & Glint Text
- **Anatomia**: Badge ou texto secundário com largura de gradiente definida (`--card-badge-shimmer-width: 96px`) usando `background-clip: text` e `color: transparent`.
- **Gatilho / Comportamento**: Uma animação em loop linear de 1.8s (`@keyframes card-badge-text-shimmer`) move a posição do fundo de `0 50%` para `96px 50%`, produzindo um brilho cintilante contínuo de platina sobre o grafite, indicando frescor ou status ativo ("NEW", "LIVE", "Understanding your query...").
- **Onde Encaixar**: Tags de status de release, chips de IA em execução e avisos de novos recursos.

#### 6. Progressive Blur Mask (Multi-Stop Falloff)
- **Anatomia**: Camada estática sobreposta na base ou topo de contêineres de scroll que utiliza `mask-image` com múltiplos stops suaves (`linear-gradient(to bottom, black 0%, transparent 100%)`) combinada com `backdrop-filter: blur(12px)`.
- **Gatilho / Comportamento**: Conforme os elementos de lista e cartões rolam para baixo do cabeçalho flutuante, eles não são cortados bruscamente por uma borda reta; em vez disso, dissolvem-se progressivamente em um gradiente de difusão de luz.
- **Onde Encaixar**: Rodapés de modais com rolagem interna, cabeçalho da Dynamic Island e carrosséis com overflow horizontal.

#### 7. Command Bar & Instant Search Expander
- **Anatomia**: Input integrado diretamente no núcleo da Dynamic Island com atalho de tecla visível (`aria-keyshortcuts="F"`), ícone de lupa SVG de traço 2.4 e botão de limpeza circular (`.search-clear`) posicionado à direita.
- **Gatilho / Comportamento**: Ao clicar ou pressionar a tecla de atalho, o placeholder transiciona suavemente; quando um termo é digitado, o ícone de lupa é substituído por um spinner de status com fade de opacidade e o botão `X` de limpeza surge com escala inercial.
- **Onde Encaixar**: Busca global de recursos, filtros de galeria e inputs de busca semântica para IA.

#### 8. Precision Gate Card & Pricing Modal
- **Anatomia**: Diálogo modal centrado (`width: min(480px, 100vw - 24px)`) com raio de curvatura de 34px (`rounded-[34px]`), topo com ilustração artística mascarada em degradê descendente (`height: 70%; mask-image: linear-gradient(to bottom, black 0%, transparent 100%)`) e botão de fechar circular flutuante de 40px com efeito pressed.
- **Gatilho / Comportamento**: Abre via `@starting-style` com transição de opacidade e escala suave de `0.96` para `1.0`. O botão primário "Upgrade" possui preenchimento total e contraste invertido, enquanto o secundário mantém fundo transparente com borda fina de 1px.
- **Onde Encaixar**: Paywalls de conversão, telas de checkout e modais de desbloqueio de recursos PRO.

---

## 5. Arquitetura Técnica, Física de Movimento & Receitas de Código

### 1. Física de Movimento & Tokens de Aceleração

O Details.so Vault padroniza três classes de movimento fundamentais:

```css
/* ==========================================================================
   DETAILS.SO VAULT — CURVAS DE ACELERAÇÃO & FÍSICA INERCIAL
   ========================================================================== */
:root {
  /* Curvas Quânticas de Saída (Entrada de Modais, Dropdowns e Tooltips) */
  --ease-out-cubic: cubic-bezier(0.215, 0.61, 0.355, 1);
  --ease-out-quart: cubic-bezier(0.165, 0.84, 0.44, 1);
  --ease-out-quint: cubic-bezier(0.23, 1, 0.32, 1);
  --ease-out-expo: cubic-bezier(0.19, 1, 0.22, 1);

  /* Curva de Deslizamento para Folhas Móveis (Drawers e Bottom Sheets) */
  --mobile-sheet-ease: cubic-bezier(0.32, 0.72, 0, 1);

  /* Curva de Mola Linear Amortecida (Elastic Physics em CSS Puro) */
  /* Equivalência: Spring com Stiffness ~340, Damping ~28, Mass ~0.8 */
  --elastic: linear(
    0, 0.0004, 0.0017, 0.0039, 0.0068, 0.0107, 0.0154, 0.0208, 0.0272 2.12%,
    0.0424 2.69%, 0.0613 3.29%, 0.084 3.92%, 0.1104 4.58%, 0.1333 5.11%,
    0.1589 5.67%, 0.2195, 0.2831 8.14%, 0.4799 11.85%, 0.541 13.05%,
    0.5955 14.17%, 0.6526 15.41%, 0.7041 16.61%, 0.751, 0.7936 18.96%,
    0.8139, 0.8332, 0.8515, 0.8687, 0.8852, 0.9008, 0.9155, 0.9292,
    0.9422, 0.9542, 0.9654, 0.9759, 0.9856, 0.9944, 1.0026 28.38%,
    1.01 29.08%, 1.0146, 1.0189, 1.0228, 1.0264, 1.0297, 1.0327,
    1.0353, 1.0377, 1.0397, 1.0415, 1.0429, 1.0441, 1.045, 1.0456,
    1.0459 37.27%, 1.046 37.94%, 1.0455 38.95%, 1.0445 40.02%,
    1.0429 41.18%, 1.0406 42.45%, 1.0356 44.73%, 1.0244 49.36%,
    1.0196 51.45%, 1.015 53.6%, 1.0112 55.65%, 1.008, 1.0054 59.6%,
    1.0032 61.63%, 1.0014 63.72%, 0.9999 66.02%, 0.9989 68.48%,
    0.9982 71.15%, 0.9979 74.13%, 0.998 79.03%, 0.9994 91.93%, 0.9999
  );

  /* Configuração de Compressão Mecânica Tátil */
  --press-scale: 0.97;
  --press-transition: transform 0.15s ease;
}

@media (prefers-reduced-motion: reduce) {
  :root {
    --press-scale: 1;
    --elastic: linear;
  }
}
```

---

### 2. Tokens de Cor & Variáveis CSS do Sistema

```css
/* ==========================================================================
   TOKENS DE SUPERFÍCIE & CORES PERCEPTIVAS DO VAULT
   ========================================================================== */
[data-theme="dark"], :root {
  color-scheme: dark;

  /* Superfícies em Warm Obsidian */
  --surface-0: hsl(0, 0%, 0%);
  --surface-1: hsl(20, 14%, 4%);        /* Fundo principal da página */
  --surface-2: hsl(20, 5%, 12%);        /* Fundo de cartões e Dynamic Island */
  --surface-3: hsl(20, 5%, 17%);        /* Botões secundários e inputs */
  --surface-4: hsl(20, 5%, 25%);        /* Hover de componentes elevados */
  --floating-surface: hsl(20, 9%, 6%);  /* Fundo de modais e painéis suspensos */

  /* Tipografia Perceptual CIE Lab */
  --text-1: lab(96.5286% -0.0991821 0.364268);  /* Branco puro de leitura */
  --text-2: lab(66.2166% 1.88044 3.20326);      /* Grafite mineral neutro */
  --text-3: hsl(24, 3%, 53%);                   /* Legendas e atalhos */

  /* Acento Neon Energizado */
  --accent: #f25500;
  --accent-10: #f255001a;
  --accent-50: #f255007a;
  --focus-ring-color: var(--accent);
  --focus-ring-width: 2px;
  --focus-ring-offset: 2px;

  /* Micro-Bordas de Precisão */
  --border-1: hsl(30, 6%, 15%);
  --border-2: hsl(30, 6%, 20%);

  /* Sombras de Dupla Camada (Ambient + Subpixel Inset) */
  --box-shadow: 0px 8px 12px 0px hsla(0, 0%, 0%, 0.04), 0px 0px 1px 0px hsl(0, 0%, 29%);
  --box-shadow-modal: 0 20px 40px -15px rgba(0, 0, 0, 0.7), 0 0 0 1px hsl(30, 6%, 20%);

  /* Geometria de Superelipse */
  --corner-shape: superellipse(1.2);
  --border-radius-xs: 18px;
  --border-radius-sm: 24px;
  --border-radius-md: 28px;
  --border-radius-lg: 34px;
}
```

---

### 3. Receita de Componentes Funcionais em React + Tailwind CSS + Framer Motion

Abaixo está a implementação completa dos componentes mais icônicos do Details.so Vault: o **TactileButton** com compressão mecânica e estado de carregamento com desfoque, e a **DetailsMorphingIsland** com navegação flutuante elástica.

```tsx
// components/vault/TactileButton.tsx
import React, { useState } from "react";
import { motion, AnimatePresence } from "framer-motion";
import { Loader2, ArrowRight } from "lucide-react";

interface TactileButtonProps extends React.ButtonHTMLAttributes<HTMLButtonElement> {
  variant?: "primary" | "secondary" | "accent";
  size?: "sm" | "md" | "lg";
  isLoading?: boolean;
  children: React.ReactNode;
}

export const TactileButton: React.FC<TactileButtonProps> = ({
  variant = "primary",
  size = "md",
  isLoading = false,
  children,
  className = "",
  disabled,
  ...props
}) => {
  const baseStyles =
    "relative inline-flex items-center justify-center font-medium transition-colors select-none outline-none focus-visible:ring-2 focus-visible:ring-[#f25500] focus-visible:ring-offset-2 focus-visible:ring-offset-[#0c0a09]";

  const variantStyles = {
    primary:
      "bg-[lab(96.5%_-0.1_0.36)] text-[hsl(20,14%,4%)] hover:bg-white active:bg-[hsl(0,0%,90%)] shadow-[0px_0px_1px_0px_rgba(255,255,255,0.4)]",
    secondary:
      "bg-[hsl(20,5%,17%)] text-[lab(96.5%_-0.1_0.36)] hover:bg-[hsl(20,5%,22%)] active:bg-[hsl(20,5%,25%)] border border-[hsl(30,6%,20%)] shadow-[0px_4px_4px_0px_rgba(0,0,0,0.04),0px_0px_1px_0px_hsl(0,0%,29%)]",
    accent:
      "bg-[#f25500] text-white hover:bg-[#e05000] active:bg-[#c94500] shadow-[0_0_16px_rgba(242,85,0,0.35)]",
  };

  const sizeStyles = {
    sm: "h-8 px-3 text-xs rounded-full gap-1.5",
    md: "h-10 px-4 text-sm rounded-full gap-2",
    lg: "h-12 px-6 text-base rounded-[24px] gap-2.5",
  };

  return (
    <motion.button
      whileTap={{ scale: disabled || isLoading ? 1 : 0.97 }}
      transition={{ duration: 0.12, ease: [0.165, 0.84, 0.44, 1] }}
      disabled={disabled || isLoading}
      className={`${baseStyles} ${variantStyles[variant]} ${sizeStyles[size]} ${className}`}
      {...props}
    >
      {/* Rótulo com transição de desfoque durante loading */}
      <span
        className={`inline-flex items-center gap-2 transition-all duration-200 ${
          isLoading ? "opacity-0 blur-sm" : "opacity-100 blur-0"
        }`}
      >
        {children}
      </span>

      {/* Spinner posicionado em overlay absoluto */}
      <AnimatePresence>
        {isLoading && (
          <motion.span
            initial={{ opacity: 0, filter: "blur(4px)" }}
            animate={{ opacity: 1, filter: "blur(0px)" }}
            exit={{ opacity: 0, filter: "blur(4px)" }}
            transition={{ duration: 0.2 }}
            className="absolute inset-0 grid place-items-center"
          >
            <Loader2 className="w-4 h-4 animate-spin text-current" />
          </motion.span>
        )}
      </AnimatePresence>
    </motion.button>
  );
};
```

```tsx
// components/vault/DetailsMorphingIsland.tsx
import React, { useState, useRef, useEffect } from "react";
import { motion, AnimatePresence } from "framer-motion";
import { Search, X, Copy, Check, ArrowLeft, RefreshCw } from "lucide-react";

export type IslandMode = "search" | "resource-detail";

interface DetailsMorphingIslandProps {
  currentResource?: {
    id: string;
    title: string;
    category: string;
    badge?: string;
  };
  onBack?: () => void;
  onRefresh?: () => void;
}

export const DetailsMorphingIsland: React.FC<DetailsMorphingIslandProps> = ({
  currentResource,
  onBack,
  onRefresh,
}) => {
  const [mode, setMode] = useState<IslandMode>(currentResource ? "resource-detail" : "search");
  const [searchQuery, setSearchQuery] = useState("");
  const [copied, setCopied] = useState(false);

  useEffect(() => {
    if (currentResource) {
      setMode("resource-detail");
    } else {
      setMode("search");
    }
  }, [currentResource]);

  const handleCopyPrompt = () => {
    setCopied(true);
    navigator.clipboard.writeText(`Implement interaction for ${currentResource?.title || "vault resource"}`);
    setTimeout(() => setCopied(false), 2000);
  };

  return (
    <div className="relative flex items-center justify-center w-full px-4 py-2">
      {/* Botão de Ação Lateral Esquerdo (Voltar para o Vault) */}
      <AnimatePresence>
        {mode === "resource-detail" && (
          <motion.button
            initial={{ opacity: 0, scale: 0.8, x: 20 }}
            animate={{ opacity: 1, scale: 1, x: 0 }}
            exit={{ opacity: 0, scale: 0.8, x: 20 }}
            transition={{ type: "spring", stiffness: 350, damping: 28 }}
            onClick={onBack}
            className="mr-2 grid place-items-center w-10 h-10 rounded-full bg-[hsl(20,5%,12%)] text-[lab(96.5%_-0.1_0.36)] hover:bg-[hsl(20,5%,17%)] active:scale-95 transition-transform"
            aria-label="Back to Vault"
          >
            <ArrowLeft className="w-4 h-4" />
          </motion.button>
        )}
      </AnimatePresence>

      {/* Pílula Central Elástica (Dynamic Island Core) */}
      <motion.div
        layout
        transition={{ type: "spring", stiffness: 320, damping: 28 }}
        className="relative flex items-center h-12 bg-[hsl(20,5%,12%)] border border-[hsl(30,6%,16%)] shadow-[0px_8px_12px_0px_hsla(0,0%,0%,0.04),0px_0px_1px_0px_hsl(0,0%,29%)] rounded-full overflow-hidden px-3"
        style={{
          width: mode === "search" ? "clamp(320px, 32vw, 420px)" : "clamp(360px, 38vw, 460px)",
        }}
      >
        <AnimatePresence mode="wait">
          {mode === "search" ? (
            /* Painel 1: Barra de Busca */
            <motion.div
              key="search-pane"
              initial={{ opacity: 0, filter: "blur(6px)" }}
              animate={{ opacity: 1, filter: "blur(0px)" }}
              exit={{ opacity: 0, filter: "blur(6px)" }}
              transition={{ duration: 0.2 }}
              className="flex items-center w-full gap-2.5"
            >
              <Search className="w-4 h-4 text-[hsl(24,3%,53%)] shrink-0" />
              <input
                type="text"
                placeholder="Search the Vault... 'liquid popover'"
                value={searchQuery}
                onChange={(e) => setSearchQuery(e.target.value)}
                className="w-full bg-transparent text-sm text-[lab(96.5%_-0.1_0.36)] placeholder-[hsl(24,2%,41%)] outline-none"
              />
              {searchQuery && (
                <button
                  onClick={() => setSearchQuery("")}
                  className="grid place-items-center w-5 h-5 rounded-full bg-[hsl(20,5%,17%)] text-[hsl(24,3%,53%)] hover:text-white"
                >
                  <X className="w-3 h-3" />
                </button>
              )}
              <kbd className="hidden md:inline-flex items-center justify-center px-1.5 py-0.5 text-[10px] font-mono text-[hsl(24,3%,53%)] bg-[hsl(20,5%,17%)] rounded border border-[hsl(30,6%,20%)]">
                F
              </kbd>
            </motion.div>
          ) : (
            /* Painel 2: Detalhes do Recurso e Gatilhos de Ação */
            <motion.div
              key="detail-pane"
              initial={{ opacity: 0, filter: "blur(6px)" }}
              animate={{ opacity: 1, filter: "blur(0px)" }}
              exit={{ opacity: 0, filter: "blur(6px)" }}
              transition={{ duration: 0.2 }}
              className="flex items-center justify-between w-full gap-3"
            >
              <div className="flex items-center gap-2 min-w-0">
                <span className="text-sm font-medium text-[lab(96.5%_-0.1_0.36)] truncate">
                  {currentResource?.title || "Resource"}
                </span>
                <span className="px-2 py-0.5 text-[10px] uppercase tracking-wider font-semibold bg-[#f255001a] text-[#f25500] rounded-full shrink-0">
                  {currentResource?.category || "UI Detail"}
                </span>
              </div>

              <div className="flex items-center gap-1.5 shrink-0">
                {/* Botão Copiar Prompt para IA */}
                <button
                  onClick={handleCopyPrompt}
                  className="grid place-items-center w-8 h-8 rounded-full bg-[hsl(20,5%,17%)] text-[lab(96.5%_-0.1_0.36)] hover:bg-[hsl(20,5%,22%)] active:scale-95 transition-transform"
                  title="Copy for AI"
                >
                  {copied ? (
                    <Check className="w-3.5 h-3.5 text-emerald-400" />
                  ) : (
                    <Copy className="w-3.5 h-3.5" />
                  )}
                </button>

                {/* Botão Obter Código */}
                <button
                  className="h-8 px-3 text-xs font-semibold bg-[lab(96.5%_-0.1_0.36)] text-[hsl(20,14%,4%)] rounded-full hover:bg-white active:scale-95 transition-transform"
                >
                  Get Code
                </button>
              </div>
            </motion.div>
          )}
        </AnimatePresence>
      </motion.div>

      {/* Botão de Ação Lateral Direito (Atualizar Preview) */}
      <AnimatePresence>
        {mode === "resource-detail" && (
          <motion.button
            initial={{ opacity: 0, scale: 0.8, x: -20 }}
            animate={{ opacity: 1, scale: 1, x: 0 }}
            exit={{ opacity: 0, scale: 0.8, x: -20 }}
            transition={{ type: "spring", stiffness: 350, damping: 28 }}
            onClick={onRefresh}
            className="ml-2 grid place-items-center w-10 h-10 rounded-full bg-[hsl(20,5%,12%)] text-[lab(96.5%_-0.1_0.36)] hover:bg-[hsl(20,5%,17%)] active:scale-95 transition-transform"
            aria-label="Refresh preview"
          >
            <RefreshCw className="w-4 h-4" />
          </motion.button>
        )}
      </AnimatePresence>
    </div>
  );
};
```

---

### 4. Como a IA Deve Pesquisar ao Vivo no Details.so

A infraestrutura do Details.so foi desenhada especificamente para interação com modelos de linguagem e agentes autônomos.

#### 1. Endpoints de Markdown Público Gêmeo
Toda URL pública do Vault possui um espelho em Markdown puro, eliminando a sobrecarga de parsing de HTML pesado:
- **Índice Global do Vault**: `https://www.details.so/vault.md`
- **Por Categoria Específica**:
  - Botões animados: `https://www.details.so/vault/category/button.md`
  - Detalhes de UI / Microinterações: `https://www.details.so/vault/category/miscellaneous.md`
  - Transições de Página: `https://www.details.so/vault/category/page-transition.md`
  - Navegações e Menus: `https://www.details.so/vault/category/navigation.md`
  - Transições de Seção: `https://www.details.so/vault/category/section-transition.md`
  - Revelações Tipográficas (Text Reveal): `https://www.details.so/vault/category/text-reveal.md`
  - Carrosséis e Galerias: `https://www.details.so/vault/category/carousels-galleries.md`
- **Ficha Técnica Individual de Componente**: `https://www.details.so/vault/<slug>.md` (ex: `https://www.details.so/vault/blur-01.md`, `https://www.details.so/vault/range-slider.md`).

#### 2. Integração com Servidor MCP Oficial
- **URL do Servidor**: `https://api.details.so/mcp`
- **Ferramentas MCP Disponíveis**:
  - `search_vault`: Pesquisa de componentes por restrições naturais de design.
  - `get_vault_resource`: Retorna o prompt canônico de implementação (`content: "implementation"`), documentação detalhada e arquivos de código prontos.

---

## 6. Diretrizes para o DESIGN_BLUEPRINT.md

Quando o projeto especificar o **Details.so Vault** como diretriz de arte ou banco de componentes primário:

1. **Tokens de Curvatura Obrigatórios**:
   - Proibir `rounded-md` (6px) ou `rounded-lg` (8px) soltos sem contexto.
   - Adotar exclusivamente os raios do Vault: `rounded-[18px]` para cartões compactos e inputs, `rounded-[28px]` para cartões médios, `rounded-[34px]` para modais de destaque e `rounded-full` para botões táteis e pílulas de navegação.

2. **Prescrição de Bordas e Oclusão de Luz**:
   - Nunca aplicar sombras pretas puras difusas sem o contorno subpixel.
   - Declarar explicitamente a classe Tailwind:
     ```html
     border border-[hsl(30,6%,15%)] shadow-[0px_8px_12px_0px_hsla(0,0%,0%,0.04),0px_0px_1px_0px_hsl(0,0%,29%)]
     ```

3. **Interatividade Mecânica em Botões e Ações**:
   - Todos os elementos clicáveis (`<button>`, `<a>`, `.card-interactive`) devem incorporar a classe `.press` ou o equivalente em Framer Motion (`whileTap={{ scale: 0.97 }}`).
   - Anéis de foco devem sempre adotar o Neon Tangerine: `focus-visible:ring-2 focus-visible:ring-[#f25500] focus-visible:ring-offset-2 focus-visible:ring-offset-[#0c0a09]`.

4. **Tratamento de Transições de Página e Scroll**:
   - Usar `Progressive Blur` no topo e base de áreas roláveis com máscaras lineares para evitar cortes bruscos de conteúdo contra o cabeçalho.
   - Manter os layouts de Dynamic Island com curvas amortecidas elásticas para transições de largura e conteúdo.
