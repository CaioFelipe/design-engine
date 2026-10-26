---
id: "preline-co"
name: "Preline UI"
url: "https://www.preline.co/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Enterprise Clean SaaS", "Utility-First Headless", "Data-Attribute Micro-Interactions", "Production-Ready Dashboards", "Modular Responsive Blocks"]
densidade_informacao: "Alta"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS/Headless)"
stack_frameworks: ["Tailwind CSS v3 & v4", "Vanilla JS / TypeScript", "React", "Next.js (App Router / Pages)", "Vue 3", "Nuxt", "Astro", "Svelte", "Angular", "ApexCharts", "Dropzone", "noUiSlider"]
compatibilidade:
  fontes_ideais: ["Inter", "Geist Sans", "Plus Jakarta Sans", "Roboto", "IBM Plex Sans", "Fira Code"]
  paletas_ideais: ["Neutral & Slate SaaS (Slate 900 / Zinc 900)", "Enterprise Corporate Blue (Blue 600 / Indigo 600)", "Fintech Emerald (Emerald 600)", "High-Contrast Monochrome Dark Mode"]
  combinacoes_recomendadas: ["Lucide Icons", "Tabler Icons", "ApexCharts", "TanStack Table", "Dropzone.js", "Flatpickr", "noUiSlider", "shadcn/ui (para hibridização de primitivas de diálogo Radix)"]
  conflitos_esteticos: ["Brutalismo Y2K cru com bordas pesadas de 3px e sombras offset duras", "Maximalismo 3D WebGL / Three.js experimental", "Neumorfismo skeuomórfico denso com relevos iluminados"]
---

# Preline UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Preline UI** (`preline.co`), concebido e desenvolvido pela equipe da **Htmlstream** (veteranos com mais de uma década de liderança na criação de temas e templates corporativos como *Unify*, *Space* e *Front*), estabeleceu-se como a mais extensa e estruturada suíte open-source de componentes utilitários, blocos responsivos e plugins interativos headless para **Tailwind CSS**.

Enquanto a maioria das bibliotecas do ecossistema Tailwind divide-se entre repositórios puramente estáticos de classes utilitárias ou pacotes fortemente atrelados a um único runtime reativo (como React ou Vue), o Preline UI consolidou uma terceira via de enorme escala: **componentes baseados em classes utilitárias canônicas combinados com um motor de plugins headless em Vanilla JavaScript / TypeScript orientados a atributos de dados (`data-hs-*`)**.

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                       ARQUITETURA NÚCLEO PRELINE UI                         │
├──────────────────────┬───────────────────────────┬──────────────────────────┤
│    TAILWIND UTILITY  │   HEADLESS PLUGINS TS/JS  │    VARIANT MODIFIERS     │
│   Classes nativas do │ Motor agnóstico leve com  │ Seletores dinâmicos como │
│  Tailwind v3 e v4 sem│ detecção automática de DOM│ hs-overlay-open:opacity  │
│ abstrações opacas    │ (HSStaticMethods.autoInit)│ hs-dropdown-open:rotate  │
└──────────────────────┴───────────────────────────┴──────────────────────────┘
```

### A Assinatura Visual: "Enterprise Clean SaaS & Production Rigor"

A assinatura gráfica do Preline UI não busca choques estéticos espalhafatosos ou experimentalismo vanguardista; seu objetivo é a **impecabilidade utilitária corporativa**. Ela transmite a sensação de um software de nível industrial imediatamente pronto para produção (*battle-tested*):

1. **Bordas Calibradas & Ritmo de Linhas Sutis:**
   As superfícies do Preline utilizam divisão geométrica precisa através de bordas neutras de baixa intensidade (`border-gray-200 dark:border-neutral-700`). Essa contenção visual impede o colapso estrutural de telas com alta densidade de dados, criando contornos firmes para painéis, tabelas, modais e formulários sem gerar poluição sensorial.

2. **Hierarquia Tipográfica Funcional e Ergonomia Espacial:**
   O design system foi desenhado para conviver perfeitamente com tipografias neo-grotescas modernas (como *Inter*, *Geist* e *Plus Jakarta Sans*). Os espaçamentos verticais e horizontais são padronizados em escala harmônica de `4px` (`gap-x-2`, `gap-y-3`, `p-4`, `p-6`), garantindo que formulários complexos de dezenas de campos mantenham um alinhamento óptico impecável.

3. **Estados de Foco de Alta Acessibilidade (Focus Rings Nativos):**
   Diferente de componentes amadores que desativam o outline do navegador (`outline-none`) sem substituição, o Preline implementa anéis de foco nítidos e padronizados em todos os nós interativos: `focus:outline-hidden focus:ring-2 focus:ring-blue-600 focus:ring-offset-2 dark:focus:ring-offset-neutral-800`. Isso garante conformidade estrita com as diretrizes WCAG 2.1 AA sem comprometer a estética moderna.

4. **Variantes e Modificadores Dinâmicos de Estado (`hs-*-open`):**
   O plugin oficial do Preline para Tailwind adiciona pseudo-classes e variantes customizadas diretamente ao compilador (`hs-overlay-open:opacity-100`, `hs-dropdown-open:rotate-180`, `hs-accordion-active:text-blue-600`). Essa inovação permite que transições visuais de abertura, rotação de chevron e exibição de menus sejam declaradas diretamente no HTML via Tailwind, eliminando arquivos CSS paralelos ou código de estilo imperativo em JS.

5. **Dark Mode Integral de Primeira Classe:**
   Praticamente 100% dos mais de 640 componentes e blocos contam com correspondência simétrica de modo escuro (`dark:bg-neutral-900`, `dark:border-neutral-700`, `dark:text-neutral-400`). O Preline inclui seu próprio controlador de aparência (`HSThemeAppearance`) com suporte a sincronização via `localStorage` e detecção de preferências do sistema operacional (`prefers-color-scheme`).

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados

1. **SaaS B2B, ERPs Corporativos & Softwares de Gestão Financeira:**
   Plataformas que exigem tabelas densas, filtros avançados, telas de faturamento, conciliação bancária e cadastros complexos com validação em tempo real. A consistência de formulários e tabelas do Preline elimina semanas de prototipagem.
2. **Dashboards Executivos de BI e Analytics:**
   Com integração nativa documentada para **ApexCharts** e componentes prontos de KPI cards, estatísticas com variação percentual, timelines de auditoria e filtros dinâmicos, o Preline é a escolha de maior velocidade para painéis analíticos.
3. **Plataformas de Infraestrutura, DevTools e Portais de API:**
   Interfaces técnicas que necessitam de wizards de configuração com múltiplos passos (`Stepper`), caixas de código com cópia rápida (`CopyMarkup`), árvores de diretórios hierárquicas (`TreeView`) e entradas de código de autenticação multifator (`PinInput`).
4. **E-Commerce B2B e Portais de Atacado:**
   Sistemas com filtros em cascata, seletores de faixa de preço com slider duplo (`RangeSlider`), galerias de upload de notas fiscais (`FileUpload`) e carrinhos de compras em gavetas deslizantes laterais (*offcanvas*).
5. **Arquiteturas Multi-Framework ou Monorepos Híbridos:**
   Empresas que possuem micro-frontends distribuídos (ex: landing page em Astro/HTML, dashboard principal em Next.js e portal interno em Vue/Nuxt). Por ter uma base Tailwind com plugins JS agnósticos, a mesma identidade visual e as mesmas classes podem ser compartilhadas sem amarras tecnológicas.

---

### Papel no Ritmo Visual (A Regra 60-30-10)

```
┌────────────────────────────────────────────────────────────────────────┐
│                   DISTRIBUIÇÃO RÍTMICA PRELINE UI                      │
├────────────────────────────────┬───────────────────────┬───────────────┤
│              60%               │          30%          │      10%      │
│     FUNDAÇÃO & ESTRUTURA       │ INTERAÇÃO & NAVEGAÇÃO │ SHOWSTOPPERS  │
│  Superfícies de dashboard,     │  Navbars responsivas, │ File Dropzones│
│  sidebars colapsáveis, grids,  │  sidebars offcanvas,  │ drag & drop,  │
│  cards de conteúdo, tabelas de │  steppers de fluxo,   │ range sliders,│
│  dados, formulários e inputs   │  dropdowns e tabs     │ gráficos Apex │
└────────────────────────────────┴───────────────────────┴───────────────┘
```

- **60% — Fundação Neutra e Estrutural:**
  O Preline atua como a espinha dorsal de layout: grids de dashboard, sidebars com links hierárquicos, cabeçalhos de tabela com zebra striping suave, inputs com ícones prefixados e cards estruturados com seções bem demarcadas (`header`, `body`, `footer`). A neutralidade dos tons de cinza garante legibilidade e foco absoluto nos dados de negócio.
- **30% — Camada de Navegação, Orquestração e Micro-interações:**
  A fluidez operacional entre diferentes telas e estados: gavetas laterais que deslizam com `hs-overlay` em visualizações mobile, menus suspensos (`hs-dropdown`) com filtros aninhados, abas dinâmicas (`hs-tab`) alternando visões de gráficos e acordeões colapsáveis para painéis de preferências.
- **10% — Componentes Funcionais Avançados e Gatilhos Visuais:**
  Elementos especializados que entregam alta conveniência e interatividade rica: zonas de arrastar e soltar arquivos com barra de progresso em tempo real (`hs-file-upload`), switches de precificação com cálculo dinâmico (`hs-toggle-count`), sliders de faixa de valor conectados a inputs monetários e gráficos com tooltips interativos calibrados para dark mode.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

1. **Portfólios Artísticos Experimentais e Sites de Agências Criativas (Estilo Awwwards SOTD):**
   Projetos cuja proposta seja quebrar convenções de usabilidade com tipografia rotacionada gigante, shaders WebGL complexos em tela cheia, cursores magnéticos personalizados e distorções líquidas. O Preline é focado em software sério e produtivo.
2. **Estéticas Neo-Brutalistas Y2K Radicais:**
   Interfaces concebidas sobre linhas pretas cruas de 3px, sombras sólidas descoladas (`shadow-[5px_5px_0px_#000]`) e paletas pastel ácidas. A linguagem curvilínea e polida do Preline entra em colisão direta com esse conceito.
3. **Aplicações Estritamente Controladas onde Manipulação Direta de DOM é Bloqueada:**
   Ambientes com políticas de segurança de conteúdo (CSP) ultra-restritas que proíbem execução de scripts externos de terceiros que modifiquem atributos de nós DOM, ou times que impõem arquiteturas 100% controladas via React Context / Redux sem permissão para bibliotecas imperativas de manipulação de classes.
4. **Widgets de Terceiros Ultraleves com Limite Rígido de Script (< 5kB):**
   Se você estiver criando um pequeno botão de chat injetável via script tag em sites externos, importar a biblioteca de plugins do Preline adiciona peso desnecessário comparado a um CSS minúsculo isolado.

---

### ⚠️ Erros Comuns de Exagero & Anti-Padrões de Implementação

- **Omitted Route Re-init no Next.js App Router (O "Bug do Menu Travado"):**
  O erro mais comum ao integrar o Preline no React/Next.js: o desenvolvedor clica em um link de navegação do App Router e, na nova página, os modais e dropdowns não abrem. Isso ocorre porque o Preline precisa re-escanear o DOM após a hidratação do cliente. **Solução obrigatória:** criar um componente cliente que execute `HSStaticMethods.autoInit()` a cada alteração do hook `usePathname()`.
- **Salada de Tons de Cinza do Tailwind:**
  Misturar arbitrariamente classes como `bg-gray-100`, `bg-zinc-100`, `bg-slate-100` e `bg-neutral-100` em diferentes blocos copiados da biblioteca. O Preline adota predominantemente a família `gray` no modo claro e `neutral` no modo escuro. Padronize uma única escala de neutros nas configurações do Tailwind.
- **Conflito de Focus-Trap em Modais Duplos:**
  Abrir um modal do Preline (`hs-overlay`) sobreposto a um modal de outra biblioteca (como shadcn/ui baseado em Radix Dialog). Dois gerenciadores de `focus-trap` competindo travam o teclado e impedem o fechamento via tecla `Escape`.
- **Sobrecarga de ApexCharts sem Limpeza de Instâncias:**
  Renderizar múltiplos gráficos reativos em dashboards com filtros rápidos sem destruir a instância anterior do ApexCharts, gerando vazamento de memória (*memory leaks*) e lentidão no navegador do usuário.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo está o catálogo dos **12 componentes e plugins interativos mais emblemáticos do Preline UI**, detalhando sua anatomia visual, atributos de gatilho e posicionamento arquitetural:

```
┌───────────────────────────────────────────────────────────────────────────────────────┐
│                          CATÁLOGO DE COMPONENTES NOTÁVEIS                             │
├────┬────────────────────────┬───────────────────────────┬─────────────────────────────┤
│ #  │ COMPONENTE / PLUGIN    │ MECANISMO CHAVE           │ POSIÇÃO IDEAL NO LAYOUT     │
├────┼────────────────────────┼───────────────────────────┼─────────────────────────────┤
│ 01 │ HSOverlay (Modais)     │ Focus trap + Backdrop     │ Confirmações, Auth, Edição  │
│ 02 │ HSOverlay (Offcanvas)  │ Deslizamento lateral X    │ Menus Mobile, Filtros, Cart │
│ 03 │ HSStepper              │ Navegação sequencial      │ Checkouts, Onboarding, KYC  │
│ 04 │ HSSelect (Combobox)    │ Live Search + Badges/Tags │ Filtros densos, Seletores   │
│ 05 │ HSFileUpload           │ Dropzone + Progress Bar   │ Anexos, Uploads de Mídia    │
│ 06 │ HSDataTable            │ Client Sort + Pagination  │ Relatórios, Backoffice, CRM │
│ 07 │ HSRangeSlider          │ Duplo Handle + Inputs     │ Filtros de Preço e Range    │
│ 08 │ HSTreeView             │ Pastas aninhadas colapso  │ Navegação de Arquivos, Docs │
│ 09 │ HSToggleCount          │ Recálculo de preços anim. │ Seções de Pricing (Anual)   │
│ 10 │ HSPinInput             │ Auto-focus jump em OTP    │ 2FA, Verificação de E-mail  │
│ 11 │ HSDropdown / Mega Menu │ Nested positioning + Fly  │ Navbar corporativa e Ações  │
│ 12 │ ApexCharts Blocks      │ Data Viz + Theme Switch   │ Cards de Dashboard, KPIs    │
└────┴────────────────────────┴───────────────────────────┴─────────────────────────────┘
```

### 1. `HSOverlay` (Modal Dialog com Backdrop Blur)
- **Anatomia Visual:** Caixa de diálogo centralizada flutuante com bordas sutis (`border border-gray-200 dark:border-neutral-700`), cantos arredondados generosos (`rounded-xl`), sombra de profundidade (`shadow-2xl`) e backdrop semitransparente com desfoque de fundo (`bg-gray-900/50 backdrop-blur-xs`).
- **Gatilho de Interação:** Disparado pelo atributo `data-hs-overlay="#id-do-modal"`. Gerencia transição suave de escala e opacidade via classes `hs-overlay-open:scale-100 scale-95 hs-overlay-open:opacity-100 opacity-0 transition-all duration-200`. Bloqueia o scroll do `body` e intercepta a tecla `Escape`.
- **Onde Encaixar:** Confirmações críticas, formulários de edição rápida, fluxos de autenticação pop-up.

### 2. `HSOverlay` (Offcanvas / Gaveta Lateral Deslizante)
- **Anatomia Visual:** Painel lateral de largura fixa (`w-80` a `w-96`) ancorado na borda esquerda ou direita da viewport, com scroll interno independente e divisores horizontais.
- **Gatilho de Interação:** Configurado com classes de transição de translação (`-translate-x-full hs-overlay-open:translate-x-0`). Abre via clique no gatilho e fecha ao clicar fora ou na tecla `Escape`.
- **Onde Encaixar:** Menu de navegação responsivo em dispositivos móveis, painéis laterais de filtros para e-commerce e gavetas de detalhes de transação em ERPs.

### 3. `HSStepper` (Multi-Step Wizard com Validação)
- **Anatomia Visual:** Trilha sequencial de etapas horizontais ou verticais com círculos numéricos de status (Pendente: cinza com anel; Ativo: azul vibrante com pulso; Concluído: fundo verde ou azul com ícone de checkmark). Conectado por linhas de progresso contínuas.
- **Gatilho de Interação:** Controlado por `data-hs-stepper`. Permite avanço condicional através de botões com `data-hs-stepper-next-btn` e recuo com `data-hs-stepper-back-btn`. Suporta verificação de validação de formulário antes de transicionar para o próximo bloco.
- **Onde Encaixar:** Fluxos de cadastro de clientes (KYC), criação de projetos multi-etapas e checkouts de compra.

### 4. `HSSelect` (Combobox Avançado com Busca & Multi-Seleção)
- **Anatomia Visual:** Campo seletor moderno com renderização customizada que suporta exibição de avatares ao lado de nomes, badges coloridos para tags selecionadas, contador de itens ativos e campo de pesquisa rápida integrado ao topo do menu suspenso.
- **Gatilho de Interação:** Inicializado via `data-hs-select='{"hasSearch": true, "placeholder": "Selecione..."}'`. Filtra itens instantaneamente no evento `input` sem atraso perceptível e fecha com navegação acessível via setas do teclado.
- **Onde Encaixar:** Seleção de responsáveis em gerenciadores de tarefas, filtros por tags e atribuição de permissões em telas de administração.

### 5. `HSFileUpload` (Dropzone com Previews e Progresso)
- **Anatomia Visual:** Área retangular delimitada por bordas pontilhadas (`border-dashed border-2 border-gray-300 dark:border-neutral-700`), ícone central de upload, instruções de formatos suportados e lista dinâmica inferior com cartões individuais de arquivos mostrando thumbnail, nome, tamanho em KB e barra percentual de progresso.
- **Gatilho de Interação:** Suporta eventos nativos de `dragenter`, `dragover`, `dragleave` e `drop` com realce de borda azul (`border-blue-500`). Controlado via `data-hs-file-upload`.
- **Onde Encaixar:** Formulários de envio de comprovantes, anexos em chamados de suporte e painéis de upload de mídia em CMS.

### 6. `HSDataTable` (Tabela de Dados com Ordenação e Paginação)
- **Anatomia Visual:** Tabela com cabeçalho de fundo suave (`bg-gray-50 dark:bg-neutral-800`), ícones bidirecionais de ordenação nas colunas, barra superior unificada com input de busca rápida e seletor de quantidade de linhas (`5, 10, 25, 50`), finalizada por rodapé com contador de registros e botões de paginação limpos.
- **Gatilho de Interação:** Controlado pelo plugin de datatable do Preline. A ordenação é executada client-side com recálculo instantâneo ao clicar nos cabeçalhos; a busca filtra linhas em tempo real com debounce.
- **Onde Encaixar:** Gestão de usuários, extratos financeiros, registros de auditoria e listagens de estoque.

### 7. `HSRangeSlider` (Controle Deslizante com Faixa Dupla)
- **Anatomia Visual:** Barra horizontal cinza neutra com preenchimento colorido azul entre os dois delimitadores circulares (*handles*). Apresenta tooltips flutuantes com o valor atual acima de cada pino e integração direta com inputs numéricos inferiores.
- **Gatilho de Interação:** Mecanismo baseado em toque e arraste com resposta contínua. Dispara eventos de atualização que sincronizam valores mínimos e máximos simultaneamente em tempo real.
- **Onde Encaixar:** Filtros de preço em e-commerce, definição de limites orçamentários e filtros de idade ou distâncias geográficas.

### 8. `HSTreeView` (Explorador Hierárquico de Pastas)
- **Anatomia Visual:** Estrutura em árvore indentada com linhas conectivas pontilhadas, ícones contextuais (pasta fechada, pasta aberta, arquivos de texto, PDF, imagens) e botões discretos de expansão/recolhimento com setas angulares.
- **Gatilho de Interação:** Clique nos nós com filhos alterna a visibilidade com transição fluida de altura. Suporta seleção única ou múltipla de itens e expansão programática.
- **Onde Encaixar:** Gerenciadores de ativos digitais, documentação de repositórios e navegação de estruturas organizacionais.

### 9. `HSToggleCount` (Alternador Dinâmico de Precificação)
- **Anatomia Visual:** Chave seletora (*pill toggle*) cercada por rótulos como "Mensal" e "Anual", frequentemente acompanhada de um badge em destaque como "Economize 20%". Abaixo, os valores monetários nos cards de preço sofrem transição instantânea.
- **Gatilho de Interação:** Atributo `data-hs-toggle-count`. Ao alternar a chave, o plugin busca elementos associados via target e substitui os valores numéricos com transição sutil de opacidade, recalculando termos de contratação.
- **Onde Encaixar:** Seção de *Pricing* em landing pages e páginas de upgrade de planos em SaaS.

### 10. `HSPinInput` (Entrada Segura de Código OTP / 2FA)
- **Anatomia Visual:** Sequência de 4 ou 6 caixas individuais de entrada de texto, de formato quadrado, com borda nítida e tipografia monoespaçada centralizada de grande porte (`text-lg font-semibold`).
- **Gatilho de Interação:** Ao digitar um dígito numérico, o cursor salta automaticamente para a próxima caixa vazia. Ao pressionar `Backspace`, remove o dígito e retorna o foco para a caixa anterior. Suporta colagem direta de códigos de 6 dígitos que preenchem automaticamente todos os campos.
- **Onde Encaixar:** Telas de verificação em duas etapas (2FA), autenticação por SMS/e-mail e transações de segurança bancária.

### 11. `HSDropdown` & Mega Menus Multicolunas
- **Anatomia Visual:** Painel suspenso posicionado dinamicamente com sombra macia e bordas refinadas. Em sua versão Mega Menu, expande-se em uma grade de 3 a 4 colunas com blocos promocionais, listas de links organizadas por categorias e ícones ilustrativos coloridos.
- **Gatilho de Interação:** Suporta modos de ativação por clique ou por hover configurável com atraso de fechamento (*hover bridge*). O chevron indicador rotaciona 180° com suavidade via classe `hs-dropdown-open:rotate-180`.
- **Onde Encaixar:** Navegação principal corporativa (*Navbar* global) e menus de ações contextuais de linha de tabela (botão "...").

### 12. Blocos de Métricas Integrados com ApexCharts
- **Anatomia Visual:** Cartões de métricas SaaS com título de KPI, valor em destaque (`text-3xl font-bold`), badge de variação percentual positiva (verde com seta ascendente) ou negativa (vermelho com seta descendente) e um gráfico de área reduzido (*sparkline*) ou gráfico de barras preenchendo a base do cartão.
- **Gatilho de Interação:** Gráficos interativos com renderização SVG via ApexCharts, equipados com tooltips personalizados formatados com classes Tailwind e sincronização automática com o tema claro/escuro da página.
- **Onde Encaixar:** Cabeçalho de visão geral de dashboards executivos e painéis de faturamento.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

O Preline UI está disponível via NPM e possui suporte nativo tanto para Tailwind CSS v3 quanto para Tailwind CSS v4.

#### Instalação do Pacote
```bash
npm install preline
```

Para componentes específicos que utilizam bibliotecas parceiras integradas:
```bash
npm install apexcharts dropzone nouislider
```

#### 1. Configuração para Tailwind CSS v3 (`tailwind.config.js`)
```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  darkMode: 'class',
  content: [
    './src/**/*.{html,js,jsx,ts,tsx,vue}',
    './node_modules/preline/preline.js',
  ],
  theme: {
    extend: {},
  },
  plugins: [
    require('preline/plugin'),
  ],
};
```

#### 2. Configuração para Tailwind CSS v4 (`src/app.css`)
```css
@import "tailwindcss";
@plugin "preline/plugin";

/* Permite que o compilador do Tailwind v4 leia as classes dos plugins do Preline */
@source "../node_modules/preline/dist/*.js";
```

---

### Integração Impecável com Next.js (App Router)

Para evitar erros de hidratação e garantir que os componentes interativos do Preline funcionem após navegações client-side com Next.js, adote o padrão oficial com `preline/non-auto`:

#### Criação do Componente Inicializador (`src/components/PrelineScript.tsx`)
```tsx
"use client";

import { usePathname } from "next/navigation";
import { useEffect } from "react";
import { HSStaticMethods } from "preline/non-auto";

export default function PrelineScript() {
  const pathname = usePathname();

  useEffect(() => {
    // Limpa registros anteriores para evitar memory leaks e duplicações
    HSStaticMethods.cleanCollection();
    // Reinicializa todos os elementos marcados com atributos 'data-hs-*' no novo DOM
    HSStaticMethods.autoInit();
  }, [pathname]);

  return null;
}
```

#### Inclusão no Layout Raiz (`src/app/layout.tsx`)
```tsx
import type { Metadata } from "next";
import "./globals.css";
import PrelineScript from "@/components/PrelineScript";

export const metadata: Metadata = {
  title: "Enterprise SaaS | Preline UI",
  description: "Modern enterprise dashboard built with Tailwind CSS & Preline UI",
};

export default function RootLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <html lang="pt-BR" className="light">
      <body className="bg-gray-50 text-gray-800 dark:bg-neutral-900 dark:text-neutral-200 antialiased">
        {children}
        <PrelineScript />
      </body>
    </html>
  );
}
```

---

### Física de Movimento, Curvas de Transição & Variantes

O Preline prioriza a máxima performance através de **transições utilitárias CSS nativas aceleradas por hardware** combinadas com modificadores de variantes ativados pelo runtime.

#### Parâmetros de Transição do Design System
- **Curva de Aceleração Primária:** `cubic-bezier(0.4, 0, 0.2, 1)` (o `ease-in-out` padrão do Tailwind, ideal para expansões e gavetas).
- **Curva de Saída Rápida:** `cubic-bezier(0, 0, 0.2, 1)` (o `ease-out`, ideal para modais e popups surgindo em direção ao usuário).
- **Duração Padrão:**
  - Micro-interações (hover de botões, rotação de chevron): `150ms` a `200ms`.
  - Camadas estruturais (Modais e Dropdowns): `200ms` a `300ms`.
  - Deslizamento lateral de Offcanvas: `300ms` a `500ms`.

```
Modo Repouso:              Transição (200ms ease-out):        Modo Ativo:
┌────────────────────┐     ─────────────────────────►     ┌────────────────────┐
│ opacity: 0         │     hs-overlay-open:opacity-100    │ opacity: 1         │
│ transform: scale-95│     hs-overlay-open:scale-100      │ transform: scale-1 │
└────────────────────┘                                    └────────────────────┘
```

---

### Receita de Código Funcional e Realista

Abaixo está a implementação de um **Painel de Gestão de Usuários com Tabela de Dados, Dropdown de Ações Rápidas e Modal de Confirmação (`HSOverlay`)**:

```tsx
"use client";

import React from "react";
import { HSOverlay } from "preline/non-auto";

interface UserItem {
  id: string;
  name: string;
  email: string;
  role: string;
  status: "Ativo" | "Pendente" | "Inativo";
  avatar: string;
}

const mockUsers: UserItem[] = [
  {
    id: "usr_01",
    name: "Helena Soares",
    email: "helena.soares@empresa.com",
    role: "Administradora",
    status: "Ativo",
    avatar: "https://images.unsplash.com/photo-1494790108377-be9c29b29330?w=150&auto=format&fit=crop&q=80",
  },
  {
    id: "usr_02",
    name: "Rodrigo Mendonça",
    email: "rodrigo.m@empresa.com",
    role: "Engenheiro de Dados",
    status: "Ativo",
    avatar: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=150&auto=format&fit=crop&q=80",
  },
  {
    id: "usr_03",
    name: "Camila Duarte",
    email: "camila.d@empresa.com",
    role: "Designer de Produto",
    status: "Pendente",
    avatar: "https://images.unsplash.com/photo-1534528741775-53994a69daeb?w=150&auto=format&fit=crop&q=80",
  },
];

export default function UserManagementSection() {
  const [selectedUser, setSelectedUser] = React.useState<UserItem | null>(null);

  const handleOpenDeleteModal = (user: UserItem) => {
    setSelectedUser(user);
    // Acionamento imperativo do modal via API programática do Preline
    HSOverlay.open("#hs-delete-user-modal");
  };

  const handleConfirmDelete = () => {
    if (selectedUser) {
      console.log(`Usuário ${selectedUser.name} (${selectedUser.id}) removido com sucesso.`);
      HSOverlay.close("#hs-delete-user-modal");
      setSelectedUser(null);
    }
  };

  return (
    <div className="w-full max-w-7xl mx-auto p-4 sm:p-6 lg:p-8 space-y-6">
      {/* Cabeçalho da Seção */}
      <div className="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-4 pb-5 border-b border-gray-200 dark:border-neutral-700">
        <div>
          <h1 className="text-xl sm:text-2xl font-bold text-gray-800 dark:text-neutral-100 tracking-tight">
            Gestão de Integrantes da Equipe
          </h1>
          <p className="text-sm text-gray-500 dark:text-neutral-400 mt-1">
            Gerencie credenciais de acesso, perfis e permissões dos membros da organização.
          </p>
        </div>
        <div className="flex items-center gap-x-3">
          <button
            type="button"
            className="py-2.5 px-4 inline-flex items-center gap-x-2 text-sm font-semibold rounded-lg bg-blue-600 text-white hover:bg-blue-700 focus:outline-hidden focus:ring-2 focus:ring-blue-500 focus:ring-offset-2 dark:focus:ring-offset-neutral-900 transition-colors shadow-sm"
          >
            <svg className="size-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round">
              <path d="M5 12h14" />
              <path d="M12 5v14" />
            </svg>
            Adicionar Membro
          </button>
        </div>
      </div>

      {/* Cartão da Tabela de Dados */}
      <div className="bg-white border border-gray-200 rounded-xl shadow-xs overflow-hidden dark:bg-neutral-800 dark:border-neutral-700">
        <div className="px-6 py-4 border-b border-gray-200 dark:border-neutral-700 flex flex-col sm:flex-row sm:items-center justify-between gap-3">
          <div className="relative max-w-xs w-full">
            <label htmlFor="user-search" className="sr-only">Pesquisar</label>
            <input
              type="text"
              id="user-search"
              placeholder="Buscar por nome ou e-mail..."
              className="py-2 px-3 ps-9 block w-full border-gray-200 rounded-lg text-sm focus:border-blue-500 focus:ring-blue-500 dark:bg-neutral-900 dark:border-neutral-700 dark:text-neutral-300 dark:placeholder-neutral-500"
            />
            <div className="absolute inset-y-0 start-0 flex items-center pointer-events-none ps-3 text-gray-400 dark:text-neutral-500">
              <svg className="size-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round">
                <circle cx="11" cy="11" r="8" />
                <path d="m21 21-4.3-4.3" />
              </svg>
            </div>
          </div>
          <span className="text-xs font-medium text-gray-500 dark:text-neutral-400">
            Total: <strong>3 membros</strong>
          </span>
        </div>

        {/* Tabela de Dados */}
        <div className="overflow-x-auto">
          <table className="min-w-full divide-y divide-gray-200 dark:divide-neutral-700">
            <thead className="bg-gray-50 dark:bg-neutral-800/60">
              <tr>
                <th scope="col" className="px-6 py-3 text-start text-xs font-semibold uppercase tracking-wider text-gray-500 dark:text-neutral-400">
                  Usuário
                </th>
                <th scope="col" className="px-6 py-3 text-start text-xs font-semibold uppercase tracking-wider text-gray-500 dark:text-neutral-400">
                  Cargo / Função
                </th>
                <th scope="col" className="px-6 py-3 text-start text-xs font-semibold uppercase tracking-wider text-gray-500 dark:text-neutral-400">
                  Status
                </th>
                <th scope="col" className="px-6 py-3 text-end text-xs font-semibold uppercase tracking-wider text-gray-500 dark:text-neutral-400">
                  Ações
                </th>
              </tr>
            </thead>
            <tbody className="divide-y divide-gray-200 dark:divide-neutral-700">
              {mockUsers.map((user) => (
                <tr key={user.id} className="hover:bg-gray-50/70 dark:hover:bg-neutral-700/30 transition-colors">
                  <td className="px-6 py-4 whitespace-nowrap">
                    <div className="flex items-center gap-x-3">
                      <img
                        className="inline-block size-9 rounded-full object-cover ring-2 ring-white dark:ring-neutral-800"
                        src={user.avatar}
                        alt={user.name}
                      />
                      <div>
                        <span className="block text-sm font-semibold text-gray-800 dark:text-neutral-200">
                          {user.name}
                        </span>
                        <span className="block text-xs text-gray-500 dark:text-neutral-400">
                          {user.email}
                        </span>
                      </div>
                    </div>
                  </td>
                  <td className="px-6 py-4 whitespace-nowrap text-sm text-gray-600 dark:text-neutral-400">
                    {user.role}
                  </td>
                  <td className="px-6 py-4 whitespace-nowrap">
                    <span
                      className={`inline-flex items-center gap-x-1.5 py-1 px-2.5 rounded-full text-xs font-medium ${
                        user.status === "Ativo"
                          ? "bg-teal-100 text-teal-800 dark:bg-teal-900/30 dark:text-teal-400"
                          : "bg-amber-100 text-amber-800 dark:bg-amber-900/30 dark:text-amber-400"
                      }`}
                    >
                      <span
                        className={`size-1.5 rounded-full ${
                          user.status === "Ativo" ? "bg-teal-500" : "bg-amber-500"
                        }`}
                      />
                      {user.status}
                    </span>
                  </td>
                  <td className="px-6 py-4 whitespace-nowrap text-end text-sm font-medium">
                    {/* Componente HSDropdown do Preline */}
                    <div className="hs-dropdown relative inline-flex">
                      <button
                        id={`hs-user-actions-${user.id}`}
                        type="button"
                        className="hs-dropdown-toggle p-2 inline-flex items-center rounded-lg text-gray-500 hover:bg-gray-100 focus:outline-hidden dark:text-neutral-400 dark:hover:bg-neutral-700 transition-colors"
                        aria-haspopup="menu"
                        aria-expanded="false"
                        aria-label="Opções"
                      >
                        <svg className="size-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round">
                          <circle cx="12" cy="12" r="1" />
                          <circle cx="19" cy="12" r="1" />
                          <circle cx="5" cy="12" r="1" />
                        </svg>
                      </button>

                      <div
                        className="hs-dropdown-menu transition-[opacity,margin] duration-150 hs-dropdown-open:opacity-100 opacity-0 hidden min-w-44 bg-white shadow-md rounded-lg p-1 space-y-0.5 mt-2 z-20 border border-gray-200 dark:bg-neutral-800 dark:border-neutral-700"
                        role="menu"
                        aria-orientation="vertical"
                        aria-labelledby={`hs-user-actions-${user.id}`}
                      >
                        <button
                          type="button"
                          className="w-full flex items-center gap-x-3 py-2 px-3 rounded-md text-xs text-gray-800 hover:bg-gray-100 focus:outline-hidden dark:text-neutral-300 dark:hover:bg-neutral-700 transition-colors"
                        >
                          Editar Informações
                        </button>
                        <button
                          type="button"
                          className="w-full flex items-center gap-x-3 py-2 px-3 rounded-md text-xs text-gray-800 hover:bg-gray-100 focus:outline-hidden dark:text-neutral-300 dark:hover:bg-neutral-700 transition-colors"
                        >
                          Alterar Permissões
                        </button>
                        <div className="my-1 border-t border-gray-200 dark:border-neutral-700" />
                        <button
                          type="button"
                          onClick={() => handleOpenDeleteModal(user)}
                          className="w-full flex items-center gap-x-3 py-2 px-3 rounded-md text-xs text-red-600 hover:bg-red-50 focus:outline-hidden dark:text-red-400 dark:hover:bg-red-900/20 transition-colors"
                        >
                          Remover Membro
                        </button>
                      </div>
                    </div>
                  </td>
                </tr>
              ))}
            </tbody>
          </table>
        </div>
      </div>

      {/* Modal Interativo HSOverlay para Confirmação de Remoção */}
      <div
        id="hs-delete-user-modal"
        className="hs-overlay hidden size-full fixed top-0 start-0 z-80 overflow-x-hidden overflow-y-auto pointer-events-none"
        role="dialog"
        tabIndex={-1}
        aria-labelledby="hs-delete-user-label"
      >
        <div className="hs-overlay-open:mt-7 hs-overlay-open:opacity-100 hs-overlay-open:duration-250 mt-0 opacity-0 ease-out transition-all sm:max-w-lg sm:w-full m-3 sm:mx-auto min-h-[calc(100%-3.5rem)] flex items-center">
          <div className="w-full flex flex-col bg-white border border-gray-200 shadow-2xl rounded-xl pointer-events-auto dark:bg-neutral-800 dark:border-neutral-700">
            <div className="flex justify-between items-center py-3 px-4 border-b border-gray-200 dark:border-neutral-700">
              <h3 id="hs-delete-user-label" className="font-semibold text-gray-800 dark:text-white">
                Confirmar Exclusão de Acesso
              </h3>
              <button
                type="button"
                className="size-8 inline-flex justify-center items-center gap-x-2 rounded-full border border-transparent bg-gray-100 text-gray-800 hover:bg-gray-200 focus:outline-hidden dark:bg-neutral-700 dark:hover:bg-neutral-600 dark:text-neutral-400"
                aria-label="Fechar"
                data-hs-overlay="#hs-delete-user-modal"
              >
                <span className="sr-only">Fechar</span>
                <svg className="size-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round">
                  <path d="M18 6 6 18" />
                  <path d="m6 6 12 12" />
                </svg>
              </button>
            </div>

            <div className="p-4 sm:p-6 overflow-y-auto">
              <p className="text-sm text-gray-600 dark:text-neutral-300">
                Tem certeza que deseja revogar o acesso do membro{" "}
                <strong className="text-gray-900 dark:text-white">
                  {selectedUser?.name || "este usuário"}
                </strong>
                ? Esta ação cancelará imediatamente tokens de API e sessões ativas associadas.
              </p>
            </div>

            <div className="flex justify-end items-center gap-x-2 py-3 px-4 border-t border-gray-200 dark:border-neutral-700 bg-gray-50 dark:bg-neutral-800/50 rounded-b-xl">
              <button
                type="button"
                className="py-2 px-3 inline-flex items-center gap-x-2 text-sm font-medium rounded-lg border border-gray-200 bg-white text-gray-800 shadow-xs hover:bg-gray-50 focus:outline-hidden dark:bg-neutral-800 dark:border-neutral-700 dark:text-white dark:hover:bg-neutral-700 transition-colors"
                data-hs-overlay="#hs-delete-user-modal"
              >
                Cancelar
              </button>
              <button
                type="button"
                onClick={handleConfirmDelete}
                className="py-2 px-3 inline-flex items-center gap-x-2 text-sm font-semibold rounded-lg bg-red-600 text-white hover:bg-red-700 focus:outline-hidden focus:ring-2 focus:ring-red-500 focus:ring-offset-2 dark:focus:ring-offset-neutral-800 transition-colors shadow-xs"
              >
                Sim, Revogar Acesso
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir o documento de arquitetura de UI (`DESIGN_BLUEPRINT.md`) para projetos que adotarem o **Preline UI**, a IA deve seguir rigorosamente as seguintes instruções normativas:

### 1. Declaração de Stack & Dependências
- Declare explicitamente:
  - Pacote core: `preline` (v2.x).
  - Plugin de Tailwind: `require('preline/plugin')` no Tailwind v3 ou `@plugin "preline/plugin";` no Tailwind v4.
  - Atributo de conteúdo no Tailwind: `"./node_modules/preline/preline.js"` (v3) ou `@source "../node_modules/preline/dist/*.js";` (v4).
  - Se houver gráficos: `apexcharts` com wrapper de theme sync.

### 2. Padrão Arquitetural de Hidratação
- Documente obrigatoriamente a criação do componente cliente `<PrelineScript />` ouvindo `usePathname()` para projetos Next.js (App Router), executando:
  ```ts
  HSStaticMethods.cleanCollection();
  HSStaticMethods.autoInit();
  ```
- No Vue 3 / Nuxt 3, configure um plugin em `plugins/preline.client.ts` ouvindo o hook de router `afterEach()`.

### 3. Governança de Tokens e Cores
- Proíba a mistura de escalas de cinza no mesmo projeto: defina uma convenção única para o design system (Recomendado: `gray` para superfícies claras e `neutral` para superfícies escuras).
- Mapeie o foco dos inputs para uma única cor de acento semântico corporativo (`focus:ring-blue-600` ou `focus:ring-indigo-600`).

### 4. Gestão de Z-Index e Modais
- Padronize as camadas de sobreposição para prevenir que sidebars fiquem sobrepostas a modais:
  - Topbar fixa / Navbar: `z-40`
  - Sidebar de dashboard: `z-50`
  - Dropdowns flutuantes: `z-60`
  - Offcanvas lateral: `z-70`
  - Modais (`HSOverlay`): `z-80`
  - Notificações Toasts flutuantes: `z-90`

### 5. Combinação Harmoniosa com Bibliotecas de Terceiros
- **Ícones:** Padronize exclusivamente em **Lucide React** (`lucide-react`) ou **Tabler Icons**. Utilize o modificador utilitário de tamanho do Preline/Tailwind: `size-4` (16px), `size-5` (20px) ou `size-6` (24px).
- **Hibridização Segura:** Se o projeto utilizar `shadcn/ui` para modais e diálogos complexos baseados em Radix UI, reserve o Preline para blocos estruturais (Sidebars, Mega Menus, Steppers, Tabelas e Dropzones), evitando que dois focus-traps imperativos atuem sobre a mesma tela.
