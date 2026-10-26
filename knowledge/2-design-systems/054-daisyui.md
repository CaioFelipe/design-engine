---
id: "daisyui"
name: "daisyUI"
url: "https://daisyui.com/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Semantic Utility Hybrid", "OKLCH Perceptual Theming", "Pure CSS Zero-JS Primitives", "Clean Modern SaaS", "Multi-Theme Expressive"]
densidade_informacao: "Flexivel"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS/Headless)"
stack_frameworks: ["Tailwind CSS v4 & v3", "Pure CSS / Semantic Classes", "HTML5 Native Dialog", "React", "Next.js", "Vue 3", "Svelte", "Astro", "HTMX", "Ruby on Rails", "Laravel / Blade", "Phoenix / LiveView"]
compatibilidade:
  fontes_ideais: ["Inter", "Geist Sans", "Plus Jakarta Sans", "Outfit", "Space Grotesk", "Fira Code"]
  paletas_ideais: ["OKLCH Dynamic Themes (Light/Dark)", "Modern Slate & Emerald", "Synthwave & Cyberpunk Neon", "High-Contrast Monochrome Minimal"]
  combinacoes_recomendadas: ["Lucide Icons", "Heroicons", "Framer Motion (para transições orquestradas de página)", "TanStack Table", "ApexCharts / Recharts"]
  conflitos_esteticos: ["Brutalismo Y2K cru com bordas pesadas e sombras duras sem suavização", "Neumorfismo skeuomórfico denso com relevos iluminados bilaterais"]
---

# daisyUI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **daisyUI** (`daisyui.com`), idealizado e mantido pelo engenheiro **Pouya Saadeghi**, é o mais utilizado e influente plugin de componentes semânticos do ecossistema mundial de **Tailwind CSS**. Com dezenas de milhões de downloads e presença consolidada em centenas de milhares de repositórios de código em produção, o daisyUI nasceu para solucionar a principal dor crônica da metodologia utilitária: a **poluição extrema de marcação HTML ("class soup")**.

Enquanto o Tailwind CSS canônico exige que o desenvolvedor declare entre 15 e 30 classes atômicas para compor um único botão interativo com estados de hover, foco, loading e disabled, o daisyUI introduz uma camada semântica limpa e elegante (`btn`, `card`, `modal`, `drawer`), mantendo intacta a capacidade de estender ou sobrescrever qualquer estilo através de utilitários nativos do Tailwind.

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                       ARQUITETURA NÚCLEO DAISYUI V5                         │
├──────────────────────┬───────────────────────────┬──────────────────────────┤
│   SEMANTIC CLASSES   │   ZERO-JS CSS PRIMITIVES  │   OKLCH COLOR ENGINE     │
│ Abstrações limpas    │ Modais via <dialog>,      │ +35 temas calibrados no  │
│ como btn, card,      │ gavetas via drawer-toggle,│ espaço perceptual OKLCH, │
│ drawer, input, chat  │ alternadores via swap     │ sem distorção cromática  │
└──────────────────────┴───────────────────────────┴──────────────────────────┘
```

### O Salto Evolutivo da Versão 5 (Tailwind CSS v4 Ready)

Com a chegada da **versão 5**, o daisyUI foi completamente reescrito para acompanhar a revolução de arquitetura do **Tailwind CSS v4**:
1. **Configuração CSS-First (Adeus `tailwind.config.js`):** O daisyUI v5 não requer mais o legado arquivo de configuração JavaScript. Ele é injetado diretamente no arquivo de estilos principal (`app.css` ou `globals.css`) por meio da diretiva nativa `@plugin "daisyui"`.
2. **Zero Dependências de Terceiros:** O núcleo do pacote foi despojado de qualquer biblioteca auxiliar, resultando em um tempo de compilação instantâneo e um pacote ultraleve.
3. **Migração Universal para o Espaço de Cores OKLCH:** Todas as paletas de cores padrão foram calibradas no espaço de cores perceptual OKLCH, garantindo uniformidade óptica em diferentes monitores, contraste WCAG matematicamente garantido e transições tonais sem a perda de saturação típica do sRGB.
4. **Nomenclatura Semântica de Variáveis CSS Modernizadas:** As antigas variáveis abreviadas da v4 (`--p`, `--b1`, `--n`) deram lugar a um padrão explícito e autoexplicativo: `--color-primary`, `--color-primary-content`, `--color-base-100`, `--color-base-200`, `--color-base-300`, `--color-neutral`, além de variáveis de geometria global como `--radius-box`, `--radius-field`, `--radius-selector` e `--border`.
5. **Novas Variantes Estéticas `soft` e `dash`:** Introdução de modificadores visuais de acabamento editorial: `btn-soft`, `badge-soft` e `alert-soft` (gerando fundos translúcidos de baixo contraste e alto refinamento visual sem a agressividade de blocos de cor sólida) e `btn-dash` (bordas pontilhadas/tracejadas modernas).
6. **Novas Primitivas:** Inclusão de componentes de ponta como o **Dock** (barra de navegação inspirada em macOS e iOS) e o efeito visual **Aura** para contornos iluminados.

---

### A Assinatura Visual: "Tactile Semantic Geometry & Theme Freedom"

A assinatura do daisyUI reside no equilíbrio perfeito entre **clareza geométrica imediata** e **maleabilidade temática expressiva**:

1. **A Cura da Síndrome do Botão de 20 Classes:**
   Em vez de:
   ```html
   <!-- Tailwind Canônico Puro -->
   <button class="inline-flex items-center justify-center px-4 py-2 text-sm font-semibold text-white bg-blue-600 rounded-lg hover:bg-blue-700 active:bg-blue-800 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2 disabled:opacity-50 disabled:pointer-events-none transition-all duration-200 shadow-sm">
     Salvar
   </button>
   ```
   No daisyUI v5 escreve-se simplesmente:
   ```html
   <!-- daisyUI v5 -->
   <button class="btn btn-primary">Salvar</button>
   <!-- Ou com acabamento suave moderno: -->
   <button class="btn btn-primary btn-soft">Salvar</button>
   ```

2. **Arquitetura Zero-JS com Primitivas HTML5 Nativas:**
   O daisyUI não exige rumbas de scripts para comportamentos triviais. 
   - Modais utilizam o elemento nativo do navegador `<dialog class="modal">`, aproveitando a API nativa `.showModal()` e o fechamento automático por tecla `ESC` ou clique no backdrop (`<form method="dialog">`).
   - Drawers (gavetas laterais) e Swaps (alternadores de ícones) operam via o truque semântico de checkbox (`<input type="checkbox" class="drawer-toggle" />`), permitindo navegação funcional mesmo em navegadores com JavaScript desativado ou em arquiteturas puramente SSR/HTML.

3. **O Maior Ecossistema de Temas Nativos (+35 Temas Prontos):**
   O daisyUI oferece suporte imediato a 35+ temas integrados com curadoria de contraste visual: desde o clássico corporativo `light` e `dark`, até propostas especializadas como `synthwave`, `cyberpunk`, `retro`, `cupcake`, `nord`, `forest`, `dracula`, `dim` e `sunset`. A transição entre temas é realizada dinamicamente alternando o atributo `data-theme="nord"` na tag `<html>`, sem requisições de rede ou re-renderizações destrutivas de componentes.

4. **Curvatura e Ritmo Tátil Calibrados:**
   O daisyUI estabelece uma relação harmônica entre o tamanho dos elementos e seus raios de curvatura através das variáveis globais `--radius-selector` (para tags, badges e pequenos seletores), `--radius-field` (para inputs e botões) e `--radius-box` (para cards, modais e containers). Ao alterar um único token no CSS do tema, toda a aplicação transiciona de um estilo ultra-arredondado amigável para um estilo afiado e técnico.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados

1. **Micro-SaaS, Startups Early-Stage e Boilerplates ("ShipFast Architecture"):**
   É a biblioteca padrão número 1 para fundadores solo e desenvolvedores de produtos digitais que precisam lançar interfaces polidas em dias, não meses. A velocidade de prototipagem combinada com a densidade de componentes elimina centenas de horas de layout.
2. **Aplicações Server-Side Rendered (HTMX, Laravel Blade, Ruby on Rails, Django, Go Templ, Phoenix LiveView):**
   Como os componentes interativos do daisyUI (modais, drawers, accordions, tabs, swaps) não exigem dependências de bibliotecas de componentes React/Vue/Svelte, ele é a ferramenta perfeita para pilhas backend onde a interface é gerada no servidor e entregue como HTML puro com HTMX ou Alpine.js.
3. **Dashboards Multi-Tenant com Suporte a Custom Themes (White-Label):**
   Plataformas B2B onde cada cliente institucional pode escolher ou configurar seu próprio esquema de cores e densidade visual. O motor de variáveis OKLCH do daisyUI permite que um tema de cliente seja gerado dinamicamente com pouquíssimas linhas de CSS.
4. **DevTools, Portais de API e Ambientes Técnicos:**
   Componentes especializados nativos como `mockup-code` (janelas de terminal com prefixo de comandos e linhas destacadas), `mockup-browser` e `kbd` (atalhos de teclado estruturados) fornecem identidade visual imediata para ferramentas de desenvolvedores.
5. **Aplicações de Mensageria e Interfaces de Chat Conversacional (AI Interfaces):**
   Com os componentes semânticos `chat`, `chat-start`, `chat-end` e `chat-bubble`, construir feeds de interação de modelos de linguagem (LLMs) torna-se uma tarefa trivial de poucos elementos HTML.

---

### Papel no Ritmo Visual (A Regra 60-30-10)

```
┌────────────────────────────────────────────────────────────────────────┐
│                    DISTRIBUIÇÃO RÍTMICA DAISYUI V5                     │
├────────────────────────────────┬───────────────────────┬───────────────┤
│              60%               │          30%          │      10%      │
│     FUNDAÇÃO & ESTRUTURA       │ INTERAÇÃO & NAVEGAÇÃO │ SHOWSTOPPERS  │
│  Botões semânticos (btn),      │  Drawer responsivo,   │ Mockup-browser│
│  cards de conteúdo, inputs,    │  modal HTML5 nativo,  │ e window, pure│
│  joins de agrupamento, badges, │  accordion collapse,  │ CSS diff view,│
│  navbars e superfícies base    │  tabs, dropdowns      │ dock macOS    │
└────────────────────────────────┴───────────────────────┴───────────────┘
```

- **60% — Fundação Neutra e Estrutural:**
  O daisyUI provê a sintaxe utilitária essencial de botões (`btn btn-primary`, `btn-soft`), inputs de formulário (`input input-bordered`), agrupadores (`join`), cards limpos (`card bg-base-100 shadow-sm`) e grids de páginas.
- **30% — Camada de Navegação, Orquestração e Micro-interações:**
  A fluidez funcional da aplicação: gavetas laterais de menu (`drawer`), caixas de diálogo modais nativas com foco gerenciado pelo navegador (`modal`), abas de alternância de visualização (`tabs tabs-lifted`) e expansores de conteúdo sanfona (`collapse collapse-arrow`).
- **10% — Showstoppers e Primitivas Visuais:**
  Elementos visuais com personalidade imediata que ancoram a identidade: o comparador antes/depois pure-CSS (`diff`), as molduras de hardware e navegadores (`mockup-browser`, `mockup-phone`), os componentes de dock de navegação flutuante (`dock`) e o alternador de temas com rotação de ícone (`swap swap-rotate`).

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

1. **Aplicações Corporativas com Look & Feel "Strict Enterprise Sóbrio" sem Customização:**
   Se deixado em sua configuração padrão sem calibração de raios e cores, o daisyUI pode passar uma impressão demasiadamente lúdica ou informal (o infame "template genérico de hackathon"). Em sistemas bancários ou regulados, é mandatória a criação de um tema neutro customizado com `--radius-field: 4px` e remoção dos efeitos de bounce de botão.
2. **Interfaces que Exigem Acessibilidade Complexa WAI-ARIA em Menus/Comboboxes Virtualizados:**
   Embora o daisyUI utilize HTML5 semântico nativo de excelência (`<dialog>`, `<details>`), ele não fornece lógica interna para padrões complexos de acessibilidade ARIA como Comboboxes com autocompletar dinâmico, multiselect virtualizado ou menus de contexto com navegação por setas complexas. Nestes cenários, primitivas headless como **Radix UI** ou **React Aria** devem ser adotadas.
3. **Projetos com Especificações Milimétricas de Figma Conflitantes:**
   Se uma equipe de design criou um Design System do zero no Figma cujos estados, paddings e alturas de componentes diferem por 2 pixels do padrão do daisyUI, tentar lutar contra as regras CSS de base do daisyUI usando dezenas de `!important` ou overrides extensivos resultará em dívida técnica massiva. Nesses casos, o Tailwind puro ou shadcn/ui é preferível.

---

### ⚠️ Erros Comuns de Exagero & Anti-Padrões:

1. **O Estigma "ShipFast Look" (Falta de Curadoria Temática):**
   Utilizar o tema `light`/`dark` padrão ou o tema `cupcake` sem qualquer alteração de tipografia ou proporção visual. Para transformar o daisyUI em uma experiência de estúdio moderno, substitua as fontes padrão por *Geist Sans* ou *Inter*, adote o modificador `btn-soft` em vez de botões sólidos saturados em excesso, e afine as bordas com `--border: 1px`.
2. **Guerra de Especificidade CSS com Utilitários Tailwind:**
   Tentar sobrescrever propriedades fundamentais do componente daisyUI declarando utilitários conflitantes sem compreender a cascata CSS. Exemplo: adicionar `p-1` a um `btn` pode gerar distorção óptica de alinhamento com ícones, pois o botão possui alturas mínimas e line-heights embutidos. Deve-se usar as variantes nativas de dimensionamento do daisyUI (`btn-sm`, `btn-xs`).
3. **Abuso de Checkbox Hacks em Formulários com Gerenciamento de Estado Reativo:**
   Usar `drawer-toggle` ou `collapse` baseado em `<input type="checkbox">` dentro de formulários controlados por React Hook Form ou Formik sem desacoplar o input do estado do formulário pode gerar submissões acidentais de campos booleanos indesejados. Em React/Vue, use o elemento `<details>` para collapses ou controle o estado via props reativas.
4. **Poluição por Múltiplos Mockups na Mesma Tela:**
   Inserir `mockup-browser`, `mockup-code` e `mockup-phone` simultaneamente na mesma página inicial. Mockups funcionam como âncoras focais únicas; usá-los em repetição destrói a sofisticação da landing page.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

### 1. Button (`btn` & Variantes Modernas `soft` e `dash`)
- **Anatomia Visual:** O pilar de interação do daisyUI. Conta com micro-animação tátil de clique (`active:scale-95`), cantos proporcionais e variantes de preenchimento (`btn-primary`, `btn-secondary`, `btn-accent`, `btn-neutral`, `btn-ghost`, `btn-link`, `btn-outline`). Na v5, ganha as variantes editoriais `btn-soft` (fundo suave sem contraste agressivo) e `btn-dash` (bordas pontilhadas/tracejadas modernas).
- **Gatilho de Interação:** Hover com escurecimento automático de tom OKLCH, Active com efeito de clique tátil de 0.25s e foco acessível com anel calibrado.
- **Onde encaixar na página:** Ações primárias no Hero, cabeçalhos de formulário, botões de submissão e barras de ferramentas agrupadas com o componente `join`.

### 2. Native Modal (`<dialog class="modal">`)
- **Anatomia Visual:** Caixa de diálogo centralizada flutuante sobre backdrop com desfoque e escurecimento óptico. Possui modificadores de alinhamento como `modal-bottom sm:modal-middle`.
- **Gatilho de Interação:** Disparado nativamente via JavaScript moderno através de `my_modal.showModal()`. O fechamento é 100% nativo via tecla `ESC` ou clique fora da caixa através do formulário `<form method="dialog" class="modal-backdrop"><button>close</button></form>`.
- **Onde encaixar na página:** Confirmações destrutivas, modais de convite de equipe, visualização ampliada de registros e wizards rápidos.

### 3. Drawer Responsivo Pure-CSS (`drawer` & `lg:drawer-open`)
- **Anatomia Visual:** Contêiner completo de layout composto por uma área de conteúdo central (`drawer-content`) e um painel lateral deslizante (`drawer-side`) que se oculta em telas móveis e se ancora fixo em telas desktop com a classe `lg:drawer-open`.
- **Gatilho de Interação:** Operado via `<input id="my-drawer" type="checkbox" class="drawer-toggle" />` com transição suave CSS `translate-x` sem uma única linha de JavaScript.
- **Onde encaixar na página:** Estrutura mestre de Dashboards, navegação mobile principal de sites institucionais e carrinhos de compras laterais (offcanvas).

### 4. Swap (`swap`, `swap-rotate` e `swap-flip`)
- **Anatomia Visual:** Micro-componente alternador composto por dois elementos visuais filhos (`swap-on` e `swap-off`) que alternam visibilidade com animações cinemáticas de rotação de 45° a 180° ou rotação 3D em torno do eixo Y (`swap-flip`).
- **Gatilho de Interação:** Alternado via clique sobre checkbox embutido ou controlado por classe de ativação `.swap-active`.
- **Onde encaixar na página:** Botão de alternância Dark/Light mode (ícone de Sol e Lua), botão de mudo/áudio, alternador de reproduzir/pausar vídeo e switches de expansão visual.

### 5. Diff (`diff`)
- **Anatomia Visual:** Componente de comparação visual de duas camadas (duas imagens, duas telas ou dois blocos de código) dispostos em formato split-screen lado a lado.
- **Gatilho de Interação:** Um divisor central arrastável nativamente baseado em um elemento `<input type="range" class="diff-resizer">`, permitindo arrastar suavemente a linha divisória com suporte total a telas de toque.
- **Onde encaixar na página:** Landing pages de produtos demonstrando "Antes vs. Depois", comparações de código legadas vs. modernas e demonstrações de edição de imagem/vídeo.

### 6. Mockups de Hardware e Ambiente (`mockup-browser`, `mockup-window`, `mockup-code`, `mockup-phone`)
- **Anatomia Visual:** Contêineres estilizados que emulam fielmente o acabamento de navegadores web modernos (com barra de URL e três botões de controle de janela), terminais Unix (com prefixos de linha de comando `data-prefix="$"`), molduras de janelas de sistema operacional e carcaças de smartphones com câmera notch superior.
- **Gatilho de Interação:** Visual e estático; suporta rolagem interna suave e micro-interações de cópia de código.
- **Onde encaixar na página:** Seção de destaque do Hero de Landing Pages de SaaS, demonstrações de comandos de instalação em documentações técnicas e vitrines de produtos mobile.

### 7. Chat Feed (`chat`, `chat-start`, `chat-end`, `chat-bubble`)
- **Anatomia Visual:** Layout completo de mensageria com suporte a avatar do emissor, nome, carimbo de data/hora (`chat-header`), balão de mensagem estilizado (`chat-bubble chat-bubble-primary`) e status de entrega ou leitura (`chat-footer`).
- **Gatilho de Interação:** Renderização reativa de histórico de conversação com micro-transições de surgimento de novas mensagens.
- **Onde encaixar na página:** Interfaces de IA conversacional (chatbots, assistentes virtuais), suporte ao cliente integrado, painéis de mensageria interna e telas de fórum social.

### 8. Dock (`dock` — Novidade v5)
- **Anatomia Visual:** Barra de ancoragem inferior inspirada no dock do macOS e nas barras de navegação flutuantes do iOS. Contém botões circulares ou arredondados com ícone central e legenda textual sutil (`dock-label`), além de indicador de nó ativo (`dock-active`).
- **Gatilho de Interação:** Hover com elevação de escala e clique com resposta tátil; ajusta-se automaticamente entre dispositivos móveis e desktops.
- **Onde encaixar na página:** Navegação primária mobile de Progressive Web Apps (PWAs), barra rápida de atalhos em interfaces web ricas e docking de ferramentas criativas.

### 9. Timeline (`timeline`)
- **Anatomia Visual:** Linha cronológica modular que pode ser exibida na orientação vertical ou horizontal responsiva (`timeline-vertical lg:timeline-horizontal`). Composta por slots simétricos: `timeline-start`, o nó gráfico intermediário `timeline-middle` e o cartão de conteúdo `timeline-end timeline-box`.
- **Gatilho de Interação:** Visual e estático; estados concluídos utilizam `bg-primary` nas linhas conectivas `<hr>`.
- **Onde encaixar na página:** Rastreamento de entregas logísticas, históricos de auditoria em dashboards, roadmaps de produtos públicos e linhas do tempo de carreira/empresa.

### 10. Collapse / Accordion (`collapse`, `collapse-arrow`)
- **Anatomia Visual:** Painel retrátil expansível com indicador sutil de seta que rotaciona suavemente 180° durante a abertura. Suporta implementação puramente semântica através da tag HTML5 `<details>` e `<summary class="collapse-title">` ou através do seletor radio para acordes mutuamente exclusivos.
- **Gatilho de Interação:** Clique de mouse ou ativação por teclado nativa do elemento `<details>`.
- **Onde encaixar na página:** Seções de Perguntas Frequentes (FAQ), painéis laterais de filtros avançados e configurações divididas por tópicos em dashboards.

### 11. Radial Progress & Stats (`radial-progress` & `stats`)
- **Anatomia Visual:** `radial-progress` gera gráficos circulares SVG/CSS parametrizados puramente via variável inline `style="--value:70;"`, enquanto `stats` organiza KPIs de alto impacto com títulos, valores proeminentes (`stat-value`) e descrições contextuais (`stat-desc`).
- **Gatilho de Interação:** Atualizações reativas de porcentagem animadas via transição CSS do token `--value`.
- **Onde encaixar na página:** Visão geral de métricas em Dashboards analíticos, indicadores de progresso de upload e barras de conclusão de perfil de usuário.

### 12. Theme Controller (`theme-controller`)
- **Anatomia Visual:** Controle interativo embutido (checkbox, toggle, radio ou dropdown) que manipula diretamente o tema global da aplicação sem depender de scripts externos.
- **Gatilho de Interação:** Ao alternar o valor do input (ex: `value="synthwave"`), o daisyUI atualiza o tema CSS da página dinamicamente.
- **Onde encaixar na página:** Cantos de navegação superior (Navbar), rodapés de documentação e painéis de preferências do usuário.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

#### Instalação no Tailwind CSS v4 (Padrão daisyUI v5):
No Tailwind CSS v4, o daisyUI v5 é configurado como um plugin puramente CSS, sem a necessidade de arquivos JavaScript intermediários:

```bash
npm install -D daisyui@latest
```

No seu arquivo principal de estilos CSS (`src/app.css` ou `src/globals.css`):
```css
@import "tailwindcss";

/* Injeção oficial do plugin daisyUI v5 com declaração dos temas */
@plugin "daisyui" {
  themes: light --default, dark --prefersdark, cupcake, synthwave, nord;
}
```

---

#### Criação de Temas Customizados em OKLCH (daisyUI v5):
Para criar um tema exclusivo com acabamento de estúdio de design, declare a extensão `@plugin "daisyui/theme"` diretamente no CSS:

```css
@import "tailwindcss";

@plugin "daisyui" {
  themes: custom-dark --default;
}

@plugin "daisyui/theme" {
  name: "custom-dark";
  default: true;
  prefersdark: true;
  color-scheme: "dark";
  
  /* Paleta Base OKLCH */
  --color-base-100: oklch(14% 0.012 260);     /* Fundo principal profundo */
  --color-base-200: oklch(18% 0.015 260);     /* Fundo secundário elevado */
  --color-base-300: oklch(23% 0.020 260);     /* Bordas e divisores */
  --color-base-content: oklch(98% 0.005 260); /* Texto principal de altíssimo contraste */

  /* Cores de Ação e Destaque */
  --color-primary: oklch(65% 0.220 260);      /* Roxo elétrico vibrante */
  --color-primary-content: oklch(99% 0 0);
  --color-secondary: oklch(72% 0.180 160);    /* Verde menta suave */
  --color-secondary-content: oklch(14% 0.02 160);
  --color-accent: oklch(75% 0.170 65);        /* Âmbar dourado */
  --color-accent-content: oklch(14% 0.02 65);

  /* Tons Neutros e Feedback */
  --color-neutral: oklch(25% 0.018 260);
  --color-neutral-content: oklch(92% 0.005 260);
  --color-info: oklch(70% 0.160 230);
  --color-success: oklch(72% 0.190 145);
  --color-warning: oklch(82% 0.170 85);
  --color-error: oklch(65% 0.230 25);

  /* Variáveis de Geometria e Acabamento Tátil */
  --radius-selector: 0.375rem; /* 6px */
  --radius-field: 0.5rem;      /* 8px */
  --radius-box: 0.75rem;       /* 12px */
  --border: 1px;
  --depth: 1;
  --noise: 0;
}
```

---

### Física de Movimento, Variáveis de Timing & Curvas CSS

O daisyUI controla suas animações através de variáveis CSS integradas ao tema, permitindo acelerar ou desacelerar transições globalmente:

```css
:root {
  --animation-btn: 0.25s;   /* Duração da compressão tátil ao clicar em botões */
  --animation-input: 0.2s;  /* Duração do anel de foco e transições de borda */
}
```

As curvas de aceleração padrão aplicadas nos estados interativos do daisyUI são baseadas na curva canônica de resposta humana:
```css
/* Curva de Resposta Tátil para Modais e Drawers */
transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
```

---

### Receitas de Implementação

#### Receita 1: Hero Section SaaS com Mockup Browser, Botões `btn-soft` e Indicadores de Status

```html
<section class="relative overflow-hidden bg-base-100 py-20 lg:py-32">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <!-- Cabeçalho Central -->
    <div class="mx-auto max-w-3xl text-center">
      <div class="inline-flex items-center gap-2 rounded-full bg-base-200 px-3 py-1 text-xs font-medium text-base-content mb-6 border border-base-300">
        <span class="inline-block h-2 w-2 rounded-full bg-success animate-pulse"></span>
        Versão 5.0 Lançada com Tailwind v4
      </div>
      <h1 class="text-4xl font-extrabold tracking-tight text-base-content sm:text-6xl">
        Componentes Semânticos. <br/>
        <span class="text-primary">Velocidade Absoluta.</span>
      </h1>
      <p class="mt-6 text-lg leading-8 text-base-content/70">
        Elimine centenas de classes utilitárias desnecessárias. Crie interfaces modernas, acessíveis e totalmente customizáveis em segundos.
      </p>
      
      <!-- Ações Primárias -->
      <div class="mt-10 flex flex-wrap items-center justify-center gap-4">
        <button class="btn btn-primary btn-lg shadow-lg hover:shadow-primary/25">
          Começar Gratuitamente
          <svg class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/>
          </svg>
        </button>
        <button class="btn btn-primary btn-soft btn-lg">
          Ver Demonstração
        </button>
      </div>
    </div>

    <!-- Mockup de Navegador com Showcase de Produto -->
    <div class="mt-16 mx-auto max-w-5xl">
      <div class="mockup-browser border border-base-300 bg-base-200 shadow-2xl rounded-2xl">
        <div class="mockup-browser-toolbar">
          <div class="input text-xs text-base-content/60">https://app.seudominio.com/dashboard</div>
        </div>
        <div class="bg-base-100 p-8 min-h-[320px] flex flex-col gap-6">
          <!-- Widget de Estatísticas Interno -->
          <div class="stats stats-vertical lg:stats-horizontal shadow bg-base-200 border border-base-300">
            <div class="stat">
              <div class="stat-title text-base-content/60">Novos Usuários</div>
              <div class="stat-value text-primary">31.2K</div>
              <div class="stat-desc text-success">↗︎ 14% mais que o mês anterior</div>
            </div>
            <div class="stat">
              <div class="stat-title text-base-content/60">Taxa de Conversão</div>
              <div class="stat-value text-secondary">4.8%</div>
              <div class="stat-desc text-base-content/60">Benchmark do setor: 2.5%</div>
            </div>
            <div class="stat">
              <div class="stat-title text-base-content/60">Tempo Médio de Sessão</div>
              <div class="stat-value">6m 42s</div>
              <div class="stat-desc text-base-content/60">Engajamento orgânico</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
```

---

#### Receita 2: Modal Nativo HTML5 com Backdrop Clicável e Fechamento com ESC

```html
<!-- Botão Disparador do Modal -->
<button class="btn btn-primary" onclick="invite_team_modal.showModal()">
  Convidar Membro da Equipe
</button>

<!-- Diálogo Modal Nativo -->
<dialog id="invite_team_modal" class="modal modal-bottom sm:modal-middle">
  <div class="modal-box bg-base-100 border border-base-300 shadow-2xl p-6">
    <h3 class="text-lg font-bold text-base-content">Novo Convite de Acesso</h3>
    <p class="py-2 text-sm text-base-content/70">
      Insira o endereço de e-mail institucional do colaborador para conceder acesso imediato ao workspace.
    </p>

    <!-- Formulário de Submissão -->
    <form method="dialog" class="mt-4 flex flex-col gap-4">
      <div>
        <label class="label text-xs font-semibold text-base-content/80">E-mail Profissional</label>
        <input 
          type="email" 
          placeholder="colaborador@empresa.com" 
          class="input input-bordered w-full bg-base-200 focus:input-primary"
          required
        />
      </div>

      <div>
        <label class="label text-xs font-semibold text-base-content/80">Nível de Permissão</label>
        <select class="select select-bordered w-full bg-base-200 focus:select-primary">
          <option>Editor de Conteúdo</option>
          <option>Desenvolvedor / API</option>
          <option>Administrador Global</option>
        </select>
      </div>

      <div class="modal-action flex items-center justify-end gap-2 mt-6">
        <!-- O botão de fechar submete com method="dialog" dispensando JS -->
        <button class="btn btn-ghost">Cancelar</button>
        <button class="btn btn-primary" type="submit">Enviar Convite</button>
      </div>
    </form>
  </div>

  <!-- Backdrop clicável que fecha a caixa de diálogo -->
  <form method="dialog" class="modal-backdrop">
    <button>close</button>
  </form>
</dialog>
```

---

#### Receita 3: Layout Responsivo com Drawer, Navbar e Theme Switcher

```html
<div class="drawer lg:drawer-open min-h-screen bg-base-100">
  <input id="main-drawer" type="checkbox" class="drawer-toggle" />

  <!-- Conteúdo Principal da Aplicação -->
  <div class="drawer-content flex flex-col">
    <!-- Navbar Superior -->
    <header class="navbar bg-base-100 border-b border-base-300 px-4">
      <!-- Botão Hambúrguer Mobile -->
      <div class="flex-none lg:hidden">
        <label for="main-drawer" aria-label="Abrir Menu" class="btn btn-square btn-ghost">
          <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
          </svg>
        </label>
      </div>

      <div class="flex-1 px-2 font-bold text-lg text-base-content">
        Workspace Console
      </div>

      <!-- Alternador de Tema Pure-CSS -->
      <div class="flex-none">
        <label class="swap swap-rotate btn btn-ghost btn-circle">
          <!-- O daisyUI detecta input com theme-controller e altera o tema -->
          <input type="checkbox" class="theme-controller" value="dark" />
          <!-- Ícone Sol (quando tema light ativo) -->
          <svg class="swap-off h-5 w-5 fill-current" viewBox="0 0 24 24">
            <path d="M5.64,17l-.71.71a1,1,0,0,0,0,1.41,1,1,0,0,0,1.41,0l.71-.71A1,1,0,0,0,5.64,17ZM5,12a1,1,0,0,0-1-1H3a1,1,0,0,0,0,2H4A1,1,0,0,0,5,12Zm7-7a1,1,0,0,0,1-1V3a1,1,0,0,0-2,0V4A1,1,0,0,0,12,5ZM5.64,7A1,1,0,0,0,7.05,5.64l-.71-.71A1,1,0,0,0,4.93,6.34Zm12.02,10a1,1,0,0,0-.7.29l-.71.71a1,1,0,1,0,1.41,1.41l.71-.71A1,1,0,0,0,17.66,17ZM21,11H20a1,1,0,0,0,0,2h1a1,1,0,0,0,0-2Zm-3.34-6.07-.71.71A1,1,0,0,0,18.36,7l.71-.71a1,1,0,0,0-1.41-1.41ZM12,6.5A5.5,5.5,0,1,0,17.5,12,5.51,5.51,0,0,0,12,6.5Zm0,9A3.5,3.5,0,1,1,15.5,12,3.5,3.5,0,0,1,12,15.5Z"/>
          </svg>
          <!-- Ícone Lua (quando tema dark ativo) -->
          <svg class="swap-on h-5 w-5 fill-current" viewBox="0 0 24 24">
            <path d="M21.64,13a1,1,0,0,0-1.05-.14,8.05,8.05,0,0,1-3.37.73A8.15,8.15,0,0,1,9.08,5.49a8.59,8.59,0,0,1,.25-2A1,1,0,0,0,8,2.36,10.14,10.14,0,1,0,22,14.05,1,1,0,0,0,21.64,13Zm-9.5,6.69A8.14,8.14,0,0,1,7.08,5.22v.27A10.15,10.15,0,0,0,17.22,15.63a9.79,9.79,0,0,0,2.1-.22A8.11,8.11,0,0,1,12.14,19.69Z"/>
          </svg>
        </label>
      </div>
    </header>

    <!-- Área de Conteúdo Central -->
    <main class="flex-1 p-6 lg:p-10">
      <h2 class="text-2xl font-bold text-base-content mb-4">Painel Geral</h2>
      <div class="card bg-base-200 border border-base-300 p-6 rounded-box">
        <p class="text-base-content/80">O layout se adapta automaticamente a telas desktop fixando a sidebar sem overhead de JavaScript.</p>
      </div>
    </main>
  </div>

  <!-- Sidebar Lateral do Drawer -->
  <aside class="drawer-side z-40">
    <label for="main-drawer" aria-label="Fechar Sidebar" class="drawer-overlay"></label>
    <div class="menu bg-base-200 min-h-full w-72 p-4 text-base-content border-r border-base-300 flex flex-col justify-between">
      <ul class="space-y-1">
        <li class="menu-title text-xs uppercase tracking-wider text-base-content/50">Navegação</li>
        <li><a class="active font-medium">Dashboard</a></li>
        <li><a>Projetos</a></li>
        <li><a>Análises de IA</a></li>
        <li><a>Configurações</a></li>
      </ul>
      <div class="p-2 border-t border-base-300 text-xs text-base-content/50">
        Workspace v2.4 • daisyUI v5
      </div>
    </div>
  </aside>
</div>
```

---

#### Receita 4: Interactive Diff Viewer Pure-CSS (Antes / Depois)

```html
<div class="mx-auto max-w-4xl p-6">
  <div class="mb-4">
    <h3 class="text-lg font-bold text-base-content">Comparador Visual em Tempo Real</h3>
    <p class="text-sm text-base-content/60">Arraste a linha central para visualizar a transformação entre as versões.</p>
  </div>

  <!-- Contêiner do Componente Diff -->
  <div class="diff aspect-16/9 rounded-box border border-base-300 shadow-xl overflow-hidden">
    <!-- Camada 1: Estado Original / Antes -->
    <div class="diff-item-1">
      <div class="bg-primary text-primary-content grid place-content-center text-4xl font-black">
        ANTES (LEGADO)
      </div>
    </div>
    
    <!-- Camada 2: Estado Novo / Depois -->
    <div class="diff-item-2">
      <div class="bg-base-200 text-base-content grid place-content-center text-4xl font-black">
        DEPOIS (DAISYUI V5)
      </div>
    </div>

    <!-- Divisor Arrastável Pure-CSS -->
    <div class="diff-resizer"></div>
  </div>
</div>
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao planejar a arquitetura de interface de um projeto no documento de especificação (`DESIGN_BLUEPRINT.md`), siga este roteiro de decisões estruturais:

### 1. Critérios de Seleção do daisyUI
- **Quando adotar daisyUI como espinha dorsal:**
  - O projeto utiliza **Tailwind CSS v4** e o objetivo prioritário é velocidade extrema de entrega com marcação limpa.
  - A pilha é orientada a renderização no servidor (Next.js SSR, Astro, HTMX, Laravel, Django, Rails) e deve minimizar JavaScript client-side desnecessário.
  - A interface exige suporte nativo a múltiplos temas (Dark/Light + temas estéticos para o usuário escolher nas preferências).
- **Quando NÃO adotar:**
  - Se a interface requer componentes de acessibilidade complexos baseados em árvore de nós virtualizados (ex: selects aninhados com filtro de pesquisa pesada) — nesse caso, integre **shadcn/ui** ou **Radix UI**.

### 2. Declaração Obrigatória no `DESIGN_BLUEPRINT.md`
Selecione e registre os tokens semânticos no blueprint com o seguinte formato padronizado:

```markdown
### Design System Base: daisyUI v5 (Tailwind CSS v4)
- **Modo de Instalação**: `@plugin "daisyui"` direto no CSS global.
- **Temas Habilitados**: `light --default, dark --prefersdark, nord, synthwave`.
- **Variantes de Componente Primárias**:
  - Botões de Ação Principal: `btn btn-primary btn-md`
  - Botões de Ação Secundária: `btn btn-primary btn-soft btn-md`
  - Modais: Native HTML5 `<dialog class="modal">`
  - Painéis de Layout: `drawer lg:drawer-open`
  - Feedbacks de Status: `badge badge-soft badge-success`
- **Geometria de Tokens**:
  - `--radius-field: 0.5rem` (8px para botões e inputs)
  - `--radius-box: 0.75rem` (12px para cards e modais)
  - `--border: 1px`
```

### 3. Diretrizes de Refinamento Anti-Cookie-Cutter
Para que o projeto com daisyUI não pareça um "boilerplate genérico":
1. **Evite botões sólidos agressivos em todo lugar:** Use extensivamente a variante `btn-soft` em ações secundárias e badges (`badge-soft`).
2. **Substitua a tipografia padrão do navegador:** Declare fontes modernas de nível editorial como *Geist Sans*, *Plus Jakarta Sans* ou *Inter* nas classes raiz.
3. **Harmonize as superfícies:** Em modo escuro, utilize `bg-base-100` para a página, `bg-base-200` para painéis agrupados e `bg-base-300` estritamente para bordas divisórias sutis.
4. **Validação de Acessibilidade:** Nunca desative o outline de foco do daisyUI; garanta que os botões mantenham anéis nítidos ao navegar via tecla `TAB`.
