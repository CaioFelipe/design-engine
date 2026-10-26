---
id: "heroui"
name: "HeroUI (anteriormente NextUI)"
url: "https://www.heroui.com/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Modern Polished Glass", "Tactile Spring Motion", "React Aria Accessible", "Tailwind Variants Slotted", "Vibrant Luminescent SaaS"]
densidade_informacao: "Flexivel"
impacto_visual: "Moderado"
custo_computacional: "Medio (Framer Motion/JS) / Baixo (CSS Transitions v3)"
stack_frameworks: ["React 19 / 18", "Next.js (App Router / Pages)", "Vite", "Remix", "Astro", "Tailwind CSS v3 & v4", "React Aria (Adobe)", "Tailwind Variants (tv)", "Framer Motion", "HeroUI CLI", "TypeScript"]
compatibilidade:
  fontes_ideais: ["Inter", "Geist Sans", "Plus Jakarta Sans", "Satoshi", "Outfit", "JetBrains Mono"]
  paletas_ideais: ["Vibrant Indigo & Violet SaaS", "Luminescent Cyan & Emerald", "Monochrome Obsidian with Glow Accents", "Warm Amber & Sunset Gradient"]
  combinacoes_recomendadas: ["Lucide React", "Tabler Icons", "Framer Motion", "Aceternity UI (para Hero showstoppers)", "Magic UI", "TanStack React Table", "Recharts"]
  conflitos_esteticos: ["Brutalismo Y2K cru / high-contrast sem suavização", "Neumorfismo skeuomórfico denso e pesado", "Interfaces industriais estáticas estilo Windows 95 ou Bloomberg Terminal"]
---

# HeroUI (anteriormente NextUI) — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **HeroUI** (originalmente lançado e consagrado mundialmente como **NextUI** por Junior García e a equipe core) representa o auge da sofisticação e do refinamento visual "out-of-the-box" no ecossistema React. Enquanto bibliotecas utilitárias puras exigem dias de calibração manual de classes CSS para atingir um acabamento moderno, o HeroUI entrega uma estética deslumbrante, tátil e organicamente polida imediatamente no primeiro render.

### A Evolução: De NextUI para HeroUI
O renomeamento histórico de NextUI para **HeroUI** resolveu a maior ambiguidade da história da biblioteca: a falsa impressão de que a suíte estava atrelada exclusivamente ao framework Next.js. O HeroUI é uma solução agnóstica para todo o universo React — operando com a mesma excelência no Vite, Remix/React Router v7, Astro, Gatsby ou em arquiteturas monorepo corporativas, e expandindo sua visão para o **HeroUI Native** (React Native).

### A Assinatura Visual: "Tactile Luminescence & Polished Glass"
A linguagem gráfica do HeroUI é reconhecível instantaneamente por um conjunto distinto de características visuais e de interação física:

1. **Feedback Háptico Visual (O Efeito Ripple):**
   Ao pressionar botões, chips ou cards interativos, o HeroUI calcula dinamicamente as coordenadas exatas do clique (`clientX`, `clientY`) relativas ao container e propaga uma onda radial suave (*ripple*) de luz ou transparência que expande do ponto de toque até desvanecer nas bordas. Isso confere à interface uma sensação quase tátil de dispositivo móvel moderno no desktop.

2. **Tratamento de Superfícies Translúcidas e Glassmorphism Controlado:**
   Diferente de interfaces opacas convencionais, o HeroUI faz uso extensivo de `backdrop-filter: blur(...)` calibrado cirurgicamente. Modais, gavetas (*Drawers*), navbars e menus suspensos utilizam planos de fundo semitransparentes com dispersão de desfoque suave (`backdrop-blur-md` com `bg-background/70`), integrando o elemento flutuante harmoniosamente ao conteúdo subjacente sem sacrificar a legibilidade.

3. **Arquitetura de Variantes Baseada em Slots (`tailwind-variants`):**
   O HeroUI foi o berço da criação do **`tailwind-variants` (`tv`)**, a ferramenta que redefiniu o gerenciamento de estilos no Tailwind CSS. Ao contrário do CVA tradicional que foca em um único nó HTML, o `tailwind-variants` do HeroUI introduziu a arquitetura de **Slots**: cada componente complexo expõe uma anatomia estruturada (ex: `base`, `wrapper`, `input`, `innerWrapper`, `label`, `helperWrapper`), permitindo customizações granulares via a prop `classNames={{ ... }}` com tipagem estrita no TypeScript e resolução automática de conflitos via `tailwind-merge`.

4. **Fundação Headless de Acessibilidade: React Aria (Adobe):**
   A beleza visual do HeroUI não é meramente cosmética; ela é erguida sobre as primitivas de acessibilidade do **React Aria** da Adobe. Cada componente satisfaz rigorosamente os critérios WAI-ARIA (WCAG AA/AAA):
   - Gerenciamento impecável de foco e focus-trap em camadas modais e popovers.
   - Navegação por teclado completa com setas dimensionais, `Home`, `End`, `PageUp/Down` e busca incremental rápida em selects e menus.
   - Anúncios de leitor de tela nativos e controle semântico de estados de validação (`aria-invalid`, `aria-describedby`).

5. **Transição de Motion: De Framer Motion (v2) para CSS Transitions Nativas (v3):**
   Na versão 2.x, o HeroUI utilizava o `framer-motion` como motor de animações para quase todos os estados de montagem/desmontagem. Na evolução v3, o design system priorizou a máxima performance e redução de bundle, migrando as transições estruturais para **CSS Transitions nativas e Keyframes acelerados por hardware via GPU** através de data-attributes (`[data-entering]`, `[data-exiting]`, `[data-pressed]`, `[data-hovered]`), mantendo suporte total ao Framer Motion para layouts com interpolação de física avançada.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados

1. **SaaS B2B Modernos, Plataformas de IA e Agentes Autônomos:**
   Aplicações onde a percepção de produto premium, rápido e futurista é um diferencial competitivo decisivo. Startups competindo em mercados saturados utilizam o HeroUI para transmitir solidez de engenharia e polimento visual desde o MVP inicial.
2. **Web3, DeFi & Plataformas de Criptoativos:**
   Dashboards financeiros descentralizados e plataformas de negociação que demandam componentes visuais luminosos, tabelas de dados dinâmicas com paginação visual suave, badges de status vibrantes e modais de assinatura de carteira com estética translúcida.
3. **Developer Experience (DevTools), Ferramentas de Nuvem & Portais de API:**
   Interfaces que combinam blocos de código formatados com cópia instantânea (`Snippet`), atalhos de teclado integrados (`Kbd`), visualização de métricas e formulários com validações assíncronas em tempo real.
4. **Dashboards Executivos de Alta Gestão e BI Interativo:**
   Painéis de controle onde a densidade precisa ser equilibrada com elegância: uso de `ScrollShadow` em listas longas, `DatePicker` internacionalizado com seleção de intervalos e gráficos emoldurados por cards estilizados.

---

### Papel no Ritmo Visual (A Aplicação Rigorosa da Regra 60-30-10)

```
┌────────────────────────────────────────────────────────────────────────┐
│                   DISTRIBUIÇÃO HARMONIOSA HEROUI                       │
├────────────────────────────────┬───────────────────────┬───────────────┤
│              60%               │          30%          │      10%      │
│     FUNDAÇÃO & ESTRUTURA       │ INTERAÇÃO & NAVEGAÇÃO │ SHOWSTOPPERS  │
│  Superfícies neutras, cards,   │   Navbar translúcida, │ Ripple effect │
│  inputs, tabelas de dados,     │  tabs com spring,     │ nos cliques,  │
│  tipografia estruturada e      │  modais com backdrop  │ badges de pulso│
│  divisores sutis               │  blur e dropdowns     │ e snippets    │
└────────────────────────────────┴───────────────────────┴───────────────┘
```

- **60% — Fundação Neutra e Estruturas de Dados:**
  O HeroUI assume o papel de gerenciar o layout, os painéis e o fluxo de dados: `Card` com bordas semânticas, `Input` com floating labels e mensagens de erro integradas, `Table` com zebra striping sutil e paginação limpa. Nesta camada, evita-se cores saturadas gratuitas; a prioridade é o contraste legível e a consistência espacial.
- **30% — Camada de Navegação, Orquestração e Micro-interações:**
  A fluidez operacional do sistema. A `Navbar` fixa no topo com blur translúcido adaptativo em scroll, o componente `Tabs` onde o indicador de seleção ("cursor") desliza fisicamente de uma aba para outra simulando um trilho mecânico elástico, gavetas laterais de configurações (`Drawer`) e `DropdownMenu` com transição de escala pop.
- **10% — Showstoppers Protagonistas e Acentos Táteis:**
  O acento visual dinâmico que converte a ação do usuário em prazer tátil: o efeito de onda radial **Ripple** no momento do clique do botão, o anel luminoso do `CircularProgress` calculando status percentuais, o badge pulsante sobre avatares em tempo real e o `ScrollShadow` dinâmico revelando profundidade quando uma lista possui itens fora de vista.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

1. **Aplicações Estáticas Ultraleves de Limite Rígido de Bundle (< 15kB JS total):**
   Projetos como widgets de chat embutidos em sites de terceiros, micro-scripts de checkout injetáveis ou blogs markdown ultra-estáticos gerados com zero JS não devem importar o runtime do HeroUI/React Aria, cujo bundle inicial reflete uma arquitetura completa de estados e eventos de acessibilidade.
2. **Ambientes de Ultra-Alta Densidade Informacional Bruta (Estilo Excel / Bloomberg):**
   ERPs industriais ou interfaces de trading de alta frequência que necessitam exibir 100 linhas por viewport sem espaçamentos confortáveis entram em atrito com a ergonomia espaçosa e cantos arredondados generosos (`rounded-xl` / `rounded-2xl`) característicos do HeroUI.
3. **Estéticas Brutalistas Radicais ou Y2K Anti-Design:**
   Projetos artísticos concebidos sobre bordas duras de 3px pretas puras, sombras duras sem difusão (`shadow-[4px_4px_0px_#000]`) e tipografia intencionalmente desordenada entram em contradição direta com o polimento curvilíneo e translúcido do HeroUI.

---

### ⚠️ Erros Comuns de Exagero & Anti-Padrões de Implementação

- **A Síndrome da "Discoteca de Ripples":** Ativar o efeito Ripple em todos os links, ícones, linhas de tabela e tags de uma única página. O Ripple deve ser reservado prioritariamente para ações de relevância tátil (botões primários/secundários e cards de seleção).
- **Abuso de Múltiplas Camadas de Backdrop Blur:** Renderizar simultaneamente 4 a 5 elementos com `backdrop-filter: blur(16px)` (ex: Navbar + Modal + Popover + Tooltip + Drawer) gera sobrecarga severa de repintura na GPU de aparelhos móveis intermediários, resultando em quedas de framerate de 60fps para 25fps.
- **Manter as Cores Padrão de Fábrica ("Default NextUI Vibe"):** Deixar o tema padrão roxo (`#7828c8`) e azul elétrico sem remapear os tokens semânticos (`primary`, `secondary`, `success`, `warning`, `danger`) no plugin do `tailwind.config.js`. A aplicação fica com cara de template pré-moldado genérico.
- **Sobrescrita Forçada com `!important` ou Classes sem Respeito aos Slots:** Tentar estilizar um `Input` aplicando `className="bg-red-500"` no nó raiz, gerando quebras de layout interno. O HeroUI exige o uso correto da prop `classNames={{ inputWrapper: "bg-red-500/10", input: "text-red-500" }}`.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

O ecossistema HeroUI reúne mais de 40 componentes modulares. Abaixo estão catalogados os 12 componentes mais emblemáticos, sua anatomia técnica, gatilhos de interação e recomendações de posicionamento:

```
┌───────────────────────────────────────────────────────────────────────────────────┐
│                       CATÁLOGO DE COMPONENTES NOTÁVEIS                            │
├────┬──────────────────────┬──────────────────────────┬────────────────────────────┤
│ #  │ COMPONENTE           │ MECANISMO CHAVE          │ POSIÇÃO IDEAL              │
├────┼──────────────────────┼──────────────────────────┼────────────────────────────┤
│ 01 │ Button               │ Click Ripple + Spinner   │ CTA Principal, Hero, Ações │
│ 02 │ Tabs                 │ Moving Spring Indicator  │ Navegação de Dashboard     │
│ 03 │ ScrollShadow         │ Intersection Detection   │ Feeds, Menus, Bento Lists  │
│ 04 │ Modal                │ Backdrop Blur + Scale    │ Confirmações, Auth, Setup  │
│ 05 │ Table                │ Accessible Sort + Select │ Relatórios, Gestão SaaS    │
│ 06 │ Autocomplete/Select  │ Virtualized Combobox     │ Filtros Densos, Checkout   │
│ 07 │ DateRangePicker      │ I18n Calendar Popover    │ Analytics, Reservas, BI    │
│ 08 │ Card                 │ Slotted Header/Body/Foot │ Bento Grids, Vitrines      │
│ 09 │ CircularProgress     │ Dynamic SVG Dashoffset   │ Status de Upload, Quotas   │
│ 10 │ Snippet              │ Copy-to-Clipboard Tátil  │ Documentação, DevTools     │
│ 11 │ AvatarGroup          │ Cascading Ring Overlap   │ Social Proof, Colaboração  │
│ 12 │ Navbar               │ Sticky Adaptive Blur     │ Topo Fixo Global           │
└────┴──────────────────────┴──────────────────────────┴────────────────────────────┘
```

### 1. `Button` (com Efeito Ripple & Spinner Integrado)
- **Anatomia Visual:** Base elipsoidal ou retangular com raio configurável (`none`, `sm`, `md`, `lg`, `full`). Suporta variantes visuais ricas: `solid`, `faded`, `bordered`, `light`, `flat`, `ghost` e `shadow` (que projeta uma sombra brilhante com a cor semântica do próprio botão).
- **Gatilho de Interação:** No evento `onPointerDown`/`onClick`, instancia um elemento `<Ripple />` posicionado exatamente nas coordenadas relativas do clique, animando escala de `0%` a `250%` com atenuação de opacidade de `0.35` a `0` em 400ms. Suporta `isLoading` com substituição fluida por spinner sem alterar o tamanho do botão.
- **Onde encaixar:** Hero sections (CTAs principais em variante `shadow`), cabeçalhos de dashboards e barras de ferramentas.

### 2. `Tabs` (com Moving Spring Indicator)
- **Anatomia Visual:** Trilha de navegação horizontal ou vertical contendo abas estilizadas nas variantes `solid`, `bordered`, `light` e `underlined`.
- **Gatilho de Interação:** Ao alternar abas via clique ou setas de teclado, o elemento visual indicador de seleção (o "cursor") não desaparece para reaparecer no novo destino; ele desliza continuamente pela trilha usando layout compartilhado (`layoutId`) e uma física de spring calibrada, esticando suavemente durante o deslocamento.
- **Onde encaixar:** Alternadores de visualização em Dashboards, configurações de conta, filtros de catálogo e tabelas de preços mensais/anuais.

### 3. `ScrollShadow` (A Assinatura Silenciosa do HeroUI)
- **Anatomia Visual:** Um container de rolagem inteligente que detecta a posição interna do scroll e projeta dinamicamente gradientes suaves de sombra nas bordas superior/inferior (ou esquerda/direita) para indicar visualmente que há mais conteúdo oculto.
- **Gatilho de Interação:** Acionado via listener passivo de `scroll` e `ResizeObserver`. Assim que o usuário atinge o topo ou o final do container, a respectiva sombra desaparece de forma gradual (`transition-opacity duration-300`).
- **Onde encaixar:** Listas de mensagens em chats de IA, gavetas laterais de histórico, tabelas com overflow horizontal e caixas de código longo.

### 4. `Modal` (com Backdrop Blur, Escala Spring & Focus Trap)
- **Anatomia Visual:** Estruturado em 6 slots: `base` (o painel de diálogo com cantos arredondados generosos), `backdrop` (a cortina de fundo), `header`, `body`, `footer` e `closeButton`.
- **Gatilho de Interação:** Acionado programmaticamente por hook (`useDisclosure()`) ou evento declarativo. O backdrop oferece modos `opaque`, `transparent` ou `blur` (`backdrop-blur-md bg-black/50`). O diálogo executa animação combinada de escala (`scale(0.95) -> scale(1)`) e opacidade (`0 -> 1`) com física amortecida e intercepta tecla `Escape`.
- **Onde encaixar:** Telas de autenticação rápida, confirmações críticas de deleção, formulários de criação de recursos e visualizadores de mídia.

### 5. `Table` (com Ordenação, Paginação e Seleção em Checkboxes)
- **Anatomia Visual:** Tabela semântica WAI-ARIA com slots independentes para `base`, `table`, `thead`, `tbody`, `tr`, `th`, `td` e `sortIcon`. Permite linhas zebra (`isStriped`), cabeçalho flutuante travado (`isHeaderSticky`) e seleção visual com borda ativa.
- **Gatilho de Interação:** Clique no cabeçalho dispara ordenação tri-state (`ascending`, `descending`, `none`) com animação fluida do ícone de direção. Suporta paginação nativa integrada através do componente `Pagination` do HeroUI.
- **Onde encaixar:** Centrais de faturamento, gerenciamento de usuários corporativos, registros de auditoria e inventários de produtos.

### 6. `Autocomplete` & `Select` (Combobox Virtualizado com React Aria)
- **Anatomia Visual:** Campo de seleção com suporte a itens simples ou com riqueza gráfica (ícones, avatares e descrições secundárias). Exibe menu dropdown flutuante posicionado por cálculo de colisão de tela.
- **Gatilho de Interação:** No foco ou digitação, abre a lista animada com transição de cascata suave. Suporta filtragem assíncrona com estado de carregamento nativo, rolagem virtualizada para suportar milhares de itens sem engasgos de render e fechamento suave via clique fora ou `Tab`.
- **Onde encaixar:** Seletores de moeda e países em checkouts, filtros dinâmicos de pesquisa, e atribuição de permissões em plataformas SaaS.

### 7. `DatePicker` & `DateRangePicker` (Internacionalização com Timezone)
- **Anatomia Visual:** Entrada com segmentação automática para Dia, Mês, Ano e Horário, acompanhada por botão de gatilho que abre um calendário de dupla página (no caso do RangePicker) com células arredondadas e realce de intervalo conectado.
- **Gatilho de Interação:** O usuário navega via teclado digitando números ou utilizando as setas de cursor dentro de cada segmento. O calendário flutuante destaca o intervalo selecionado com cor contínua e transição de meses via slide. Suporta fusos horários complexos através da biblioteca `@internationalized/date`.
- **Onde encaixar:** Filtros de relatórios de métricas (ex: "Últimos 30 dias"), reservas de quartos/voos e agendamento de eventos em calendários.

### 8. `Card` (com Suporte a Interatividade e Layouts Complexos)
- **Anatomia Visual:** Container de agrupamento com slots `base`, `header`, `body` e `footer`. Possui as props utilitárias `isPressable` (transforma o card em botão interativo com ripple effect) e `isHoverable` (elevação de sombra e transição de escala no hover).
- **Gatilho de Interação:** Hover desencadeia transição suave de `box-shadow` e micro-deslocamento no eixo Y (`-translate-y-1`). Suporta imagem de fundo preenchendo 100% da área com blur overlay no footer (`isFooterBlurred`).
- **Onde encaixar:** Bento Grids em páginas de produto, vitrines de e-commerce, cards de precificação e resumos de métricas principais (KPIs).

### 9. `CircularProgress` & `Progress` (com SVG Dashoffset Animado)
- **Anatomia Visual:** Indicador de progresso linear ou circular com arco vetorial SVG dinâmico, suportando rótulo de percentual customizado no centro, cores semânticas e espessura de traço configurável (`strokeWidth`).
- **Gatilho de Interação:** Atualizações do valor `value={75}` recalculam matematicamente a propriedade CSS `stroke-dashoffset` animando o preenchimento de forma contínua em 500ms. No modo `isIndeterminate`, executa rotação contínua e expansão harmônica do arco.
- **Onde encaixar:** Indicadores de consumo de plano (ex: "82% de armazenamento usado"), medidores de força de senha, barras de upload de arquivos e painéis de saúde de servidores.

### 10. `Snippet` (Caixa de Comando Shell com Cópia Tátil)
- **Anatomia Visual:** Bloco retangular monolítico exibindo um comando de terminal (ex: `npx heroui-cli init`), prefixo de prompt de comando (`$`), e ícone lateral de prancheta de cópia.
- **Gatilho de Interação:** O clique no ícone ou no próprio bloco copia a cadeia de texto diretamente para o clipboard do sistema operacional através da API `navigator.clipboard`, alternando instantaneamente o ícone para uma marca de verificação (*check*) animada e disparando tooltip de confirmação ("Copiado!").
- **Onde encaixar:** Seções de Quickstart em páginas iniciais de ferramentas para desenvolvedores, modais de chaves de API e instruções de instalação de bibliotecas.

### 11. `AvatarGroup` (Agrupamento com Efeito Cascata e Overflow)
- **Anatomia Visual:** Pilha horizontal de fotos de perfil circulares com anéis de contorno que evitam colisão visual com o fundo, exibindo automaticamente um avatar contador no final (ex: `+12`) quando o total excede a propriedade `max`.
- **Gatilho de Interação:** Hover sobre um avatar individual eleva seu `z-index` e aplica micro-escala (`scale-110`), permitindo inspeção rápida do nome do usuário via tooltip integrado.
- **Onde encaixar:** Seção de Prova Social ("Usado por mais de 10.000 engenheiros"), cabeçalhos de workspaces colaborativos e cards de atribuição de tarefas.

### 12. `Navbar` (com Efeito Dinâmico de Blur no Scroll)
- **Anatomia Visual:** Barra horizontal dividida em seções `NavbarBrand`, `NavbarContent` e `NavbarItem`, integrando botões de navegação, alternador de tema e avatar de usuário.
- **Gatilho de Interação:** Suporta comportamento `shouldHideOnScroll` (recolhe automaticamente ao rolar para baixo e reaparece ao rolar para cima) e `isBordered`. O fundo translúcido ativa desfoque dinâmico assim que a página sai da posição `scrollY: 0`.
- **Onde encaixar:** Cabeçalho global permanente em todas as páginas da aplicação.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup Moderno

O HeroUI pode ser consumido como um pacote monolítico unificado (`@heroui/react`) ou através de pacotes individuais escopados por componente (ex: `@heroui/button`, `@heroui/modal`) para maximizar o tree-shaking:

```bash
# Instalação do pacote principal do HeroUI + motor de ícones
npm install @heroui/react framer-motion lucide-react clsx tailwind-variants
```

#### 1. Configuração do Plugin no `tailwind.config.js`
O plugin oficial `heroui()` do pacote `@heroui/react` injeta os tokens de cor, sombras, raios e classes utilitárias no Tailwind:

```javascript
// tailwind.config.js
import { heroui } from "@heroui/react";

/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
    // Linha mandatória para carregar os estilos compilados dos componentes:
    "./node_modules/@heroui/theme/dist/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  darkMode: "class",
  plugins: [
    heroui({
      prefix: "heroui", // Prefixo para variáveis CSS customizadas
      addCommonColors: false, // Desativa cores genéricas redundantes
      defaultTheme: "dark", // Tema padrão
      defaultExtendTheme: "dark",
      layout: {
        radius: {
          small: "8px",
          medium: "12px",
          large: "16px",
        },
        borderWidth: {
          small: "1px",
          medium: "1px",
          large: "2px",
        },
      },
      themes: {
        dark: {
          colors: {
            background: "#09090b", // Deep Zinc
            foreground: "#f4f4f5",
            primary: {
              50: "#eef2ff",
              100: "#e0e7ff",
              200: "#c7d2fe",
              300: "#a5b4fc",
              400: "#818cf8",
              500: "#6366f1", // Indigo vívido
              600: "#4f46e5",
              700: "#4338ca",
              800: "#3730a3",
              900: "#312e81",
              DEFAULT: "#6366f1",
              foreground: "#ffffff",
            },
            focus: "#6366f1",
          },
        },
      },
    }),
  ],
};
```

#### 2. Injeção do `HeroUIProvider` na Raiz da Aplicação
Em aplicações Next.js (App Router), configure o provider no `app/providers.tsx`:

```tsx
// app/providers.tsx
"use client";

import { HeroUIProvider } from "@heroui/react";
import { useRouter } from "next/navigation";

export function Providers({ children }: { children: React.ReactNode }) {
  const router = useRouter();

  return (
    // A prop navigate garante que os componentes <Link> internos usem o router do Next.js
    <HeroUIProvider navigate={router.push}>
      {children}
    </HeroUIProvider>
  );
}
```

---

### Física de Movimento, Transições e Curvas

O HeroUI baseia seu ritmo dinâmico em parâmetros cinéticos altamente refinados:

1. **Curvas de Bézier Cúbicas (Transições de Entrada/Saída):**
   - **Popovers e Menus (`scale-fade`):** `cubic-bezier(0.16, 1, 0.3, 1)` com duração de `200ms` a `250ms`. Essa curva (conhecida como *Custom Spring-Out*) projeta o elemento rapidamente para frente, desacelerando com maciez no fim sem rebotes exagerados.
   - **Backdrops Translúcidos:** `cubic-bezier(0.4, 0, 0.2, 1)` (padrão `ease-in-out` do Tailwind) com duração de `300ms` para garantir que o escurecimento e desfoque da tela pareçam graduais.

2. **Parâmetros de Spring do `Framer Motion` (Tabs Cursor & Modais):**
   ```javascript
   export const heroSpringTransition = {
     type: "spring",
     stiffness: 400,
     damping: 30,
     mass: 0.8,
   };
   ```
   *Efeito:* Fornece ao cursor deslizante das abas uma sensação de tração metálica firme, onde a massa leve (`0.8`) assegura resposta imediata à troca de abas, sem atraso perceptível de clique.

---

### Receita de Código Funcional em React

O exemplo a seguir demonstra a construção de um painel de configuração moderno utilizando a arquitetura de **Slots**, o componente `Modal` com backdrop blur, `Tabs` deslizantes com indicador elástico, `ScrollShadow` e `Button` com efeito Ripple e sombra luminosa:

```tsx
"use client";

import React, { useState } from "react";
import {
  Modal,
  ModalContent,
  ModalHeader,
  ModalBody,
  ModalFooter,
  Button,
  Tabs,
  Tab,
  Input,
  ScrollShadow,
  Chip,
  useDisclosure,
} from "@heroui/react";
import { Shield, Key, Bell, Sparkles, CheckCircle2 } from "lucide-react";

export function SecuritySettingsModal() {
  const { isOpen, onOpen, onOpenChange } = useDisclosure();
  const [selectedTab, setSelectedTab] = useState("api-keys");

  return (
    <div className="flex flex-col items-center justify-center p-8 bg-zinc-950 min-h-[400px]">
      {/* Botão Gatilho com Sombra Primária Luminosa e Ripple */}
      <Button
        onPress={onOpen}
        color="primary"
        variant="shadow"
        size="lg"
        startContent={<Shield className="w-5 h-5" />}
        className="font-medium tracking-wide text-white transition-transform active:scale-95"
      >
        Configurações de Segurança
      </Button>

      {/* Modal com Backdrop Blur e Escala Suave */}
      <Modal
        isOpen={isOpen}
        onOpenChange={onOpenChange}
        backdrop="blur"
        size="2xl"
        classNames={{
          backdrop: "bg-black/60 backdrop-blur-md",
          base: "border border-zinc-800/80 bg-zinc-900/95 text-zinc-100 shadow-2xl rounded-2xl",
          header: "border-b border-zinc-800/60 pb-3 pt-5 px-6",
          body: "py-6 px-6",
          footer: "border-t border-zinc-800/60 py-4 px-6",
          closeButton: "hover:bg-zinc-800 active:bg-zinc-700 text-zinc-400 hover:text-zinc-100",
        }}
      >
        {(onClose) => (
          <>
            <ModalHeader className="flex items-center gap-3">
              <div className="p-2 rounded-xl bg-indigo-500/10 text-indigo-400 border border-indigo-500/20">
                <Shield className="w-5 h-5" />
              </div>
              <div className="flex flex-col">
                <span className="text-lg font-semibold tracking-tight">Central de Segurança</span>
                <span className="text-xs text-zinc-400 font-normal">
                  Gerencie credenciais, webhooks e alertas de integridade
                </span>
              </div>
            </ModalHeader>

            <ModalBody>
              {/* Tabs com Indicador de Spring Deslizante */}
              <Tabs
                selectedKey={selectedTab}
                onSelectionChange={(key) => setSelectedTab(String(key))}
                color="primary"
                variant="solid"
                classNames={{
                  tabList: "bg-zinc-950/60 border border-zinc-800/80 p-1 rounded-xl w-full",
                  cursor: "bg-indigo-600 shadow-lg shadow-indigo-500/30 rounded-lg",
                  tab: "h-9 text-sm font-medium text-zinc-400 data-[selected=true]:text-white",
                }}
              >
                <Tab
                  key="api-keys"
                  title={
                    <div className="flex items-center gap-2">
                      <Key className="w-4 h-4" />
                      <span>Chaves de API</span>
                    </div>
                  }
                />
                <Tab
                  key="notifications"
                  title={
                    <div className="flex items-center gap-2">
                      <Bell className="w-4 h-4" />
                      <span>Notificações</span>
                    </div>
                  }
                />
                <Tab
                  key="audit"
                  title={
                    <div className="flex items-center gap-2">
                      <Sparkles className="w-4 h-4" />
                      <span>Logs de Auditoria</span>
                    </div>
                  }
                />
              </Tabs>

              {/* ScrollShadow Dinâmico Protegendo o Conteúdo com Overflow */}
              <ScrollShadow className="w-full h-[220px] mt-4 pr-2 space-y-4">
                {selectedTab === "api-keys" && (
                  <div className="space-y-4">
                    <Input
                      label="Nome da Chave"
                      placeholder="Ex: Production Service Worker"
                      labelPlacement="outside"
                      variant="bordered"
                      classNames={{
                        inputWrapper:
                          "border-zinc-800 hover:border-zinc-700 focus-within:!border-indigo-500 bg-zinc-950/40 rounded-xl",
                        label: "text-zinc-300 font-medium text-xs",
                        input: "text-zinc-100 placeholder:text-zinc-600 text-sm",
                      }}
                    />

                    <div className="p-3 rounded-xl bg-zinc-950/60 border border-zinc-800/60 flex items-center justify-between">
                      <div className="flex flex-col">
                        <span className="text-xs font-mono text-indigo-400">sk_live_948f98...e1a2</span>
                        <span className="text-[11px] text-zinc-500 mt-0.5">Criada há 2 dias • Acesso Root</span>
                      </div>
                      <Chip color="success" variant="flat" size="sm" startContent={<CheckCircle2 className="w-3.5 h-3.5" />}>
                        Ativa
                      </Chip>
                    </div>

                    <div className="p-3 rounded-xl bg-zinc-950/60 border border-zinc-800/60 flex items-center justify-between">
                      <div className="flex flex-col">
                        <span className="text-xs font-mono text-zinc-400">sk_test_128b77...00bc</span>
                        <span className="text-[11px] text-zinc-500 mt-0.5">Criada há 3 semanas • Acesso Somente Leitura</span>
                      </div>
                      <Chip color="default" variant="flat" size="sm">
                        Sandbox
                      </Chip>
                    </div>
                  </div>
                )}

                {selectedTab !== "api-keys" && (
                  <div className="flex flex-col items-center justify-center h-full text-zinc-500 text-sm">
                    Módulo em sincronização de telemetria...
                  </div>
                )}
              </ScrollShadow>
            </ModalBody>

            <ModalFooter className="flex justify-between items-center">
              <span className="text-xs text-zinc-500">Criptografia AES-256 habilitada</span>
              <div className="flex gap-2">
                <Button variant="light" color="default" onPress={onClose} className="text-zinc-400 hover:text-white">
                  Cancelar
                </Button>
                <Button color="primary" onPress={onClose} className="font-medium bg-indigo-600 text-white">
                  Salvar Alterações
                </Button>
              </div>
            </ModalFooter>
          </>
        )}
      </Modal>
    </div>
  );
}
```

---

### Como Criar Componentes Personalizados usando `tailwind-variants` (`tv`)

O HeroUI popularizou o padrão de criação de componentes via `tv()`. Esse mesmo padrão deve ser utilizado para estender o sistema com novos componentes customizados:

```typescript
// components/custom-kpi-card.ts
import { tv } from "tailwind-variants";

export const kpiCardVariants = tv({
  slots: {
    base: "relative overflow-hidden rounded-2xl border p-5 transition-all duration-300",
    header: "flex items-center justify-between pb-2",
    title: "text-xs font-medium tracking-wide uppercase",
    value: "text-2xl font-bold tracking-tight mt-1",
    badge: "inline-flex items-center gap-1 rounded-full px-2 py-0.5 text-xs font-medium",
  },
  variants: {
    intent: {
      default: {
        base: "bg-zinc-900/50 border-zinc-800 hover:border-zinc-700",
        title: "text-zinc-400",
        value: "text-zinc-100",
      },
      featured: {
        base: "bg-indigo-950/20 border-indigo-500/30 hover:border-indigo-500/60 shadow-lg shadow-indigo-500/10",
        title: "text-indigo-300",
        value: "text-indigo-100",
      },
    },
    trend: {
      up: { badge: "bg-emerald-500/10 text-emerald-400 border border-emerald-500/20" },
      down: { badge: "bg-rose-500/10 text-rose-400 border border-rose-500/20" },
    },
  },
  defaultVariants: {
    intent: "default",
    trend: "up",
  },
});
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma nova aplicação que utiliza o **HeroUI** como biblioteca primária de componentes, a inteligência artificial ou o arquiteto de front-end deve observar as seguintes regras e declarações no `DESIGN_BLUEPRINT.md`:

### 1. Declaração do Design System & Framework Base
- **Stack Obrigatória:** `React 19 / 18` + `@heroui/react` + `tailwind-variants` + `lucide-react`.
- **Estratégia de Theming:** Declarar expressamente os pares de cores semânticas dentro da chave `heroui()` do `tailwind.config.js`. **Nunca utilizar as cores hexadecimais nativas soltas diretamente nos componentes**; referenciar sempre as variáveis semânticas do tema (`primary`, `secondary`, `success`, `warning`, `danger`, `background`, `foreground`).

### 2. Especificação de Tokens de Geometria e Superfície
- **Raio de Borda (Radius Matrix):**
  - Botões, Inputs e Chips: `radius="md"` (12px) ou `radius="lg"` (16px).
  - Cards e Painéis Modais: `rounded-2xl` (16px a 20px).
  - Elementos Circulares / Pílulas: `radius="full"`.
- **Superfícies Flutuantes (Backdrop Policy):**
  - Modais, Drawers e Navbars devem sempre declarar `backdrop="blur"` com intensidade calibrada para evitar perda de performance (`backdrop-blur-md` com fundo semitransparente escuro `bg-black/60`).

### 3. Convenção Mandatória de Customização por Slots (`classNames`)
- **Proibição de Conflitos em Nós Raiz:** Para componentes compostos (`Input`, `Modal`, `Tabs`, `Table`, `Select`), é expressamente vetado tentar injetar estilos internos diretamente na propriedade genérica `className`. Deve-se utilizar obrigatoriamente a prop estruturada `classNames={{ slotName: "..." }}` para garantir especificidade limpa e suporte a responsividade.

### 4. Gestão do Efeito Ripple e Acessibilidade
- **Moderação Tátil:** Manter a prop `disableRipple={false}` nos botões de CTA primários e seletores de cards; ativar `disableRipple={true}` em botões de tabelas repetitivas, paginação e itens de menu de densidade alta para preservar a fluidez do cursor.
- **Navegação SPA:** Sempre passar a função de navegação do framework router para o `HeroUIProvider` (`navigate={router.push}`), permitindo que todos os links, botões e breadcrumbs façam pré-carregamento e transição client-side sem recarregar a página.

---

### Resumo Executivo da Biblioteca

| Critério | Avaliação | Justificativa |
| :--- | :--- | :--- |
| **Ergonomia de Desenvolvimento** | ⭐⭐⭐⭐⭐ (5/5) | Documentação impecável, CLI automatizada e arquitetura de slots com tipagem TypeScript estrita. |
| **Acessibilidade (A11y)** | ⭐⭐⭐⭐⭐ (5/5) | Construído nativamente sobre o React Aria da Adobe; atende integralmente às normas WCAG AA/AAA. |
| **Polimento Visual Imediato** | ⭐⭐⭐⭐⭐ (5/5) | O design system mais bonito e tátil do ecossistema React logo na primeira linha de código. |
| **Overhead de Bundle** | ⭐⭐⭐⭐☆ (4/5) | Médio na v2 com Framer Motion; excelente na v3 com a migração para CSS Transitions nativas. |
| **Customização Avançada** | ⭐⭐⭐⭐⭐ (5/5) | Liderado pelo `tailwind-variants`, permitindo sobrescrever qualquer camada interna via slots. |
