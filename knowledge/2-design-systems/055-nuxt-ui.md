---
id: "nuxt-ui"
name: "Nuxt UI"
url: "https://ui.nuxt.com/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Clean Nuxt Emerald Modernism", "Reka UI Headless Precision", "Tailwind CSS v4 Native OKLCH", "Tailwind Variants Component Slots", "Keyboard-Driven Power User UX"]
densidade_informacao: "Flexivel"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS/Headless)"
stack_frameworks: ["Nuxt 3 / 4", "Vue 3 (Composition API / Script Setup)", "Tailwind CSS v4 & v3", "Reka UI (antigo Radix Vue)", "Tailwind Variants (tv)", "TanStack Table (@tanstack/vue-table)", "Zod / Valibot", "Iconify (@nuxt/icon)", "TypeScript", "Vite"]
compatibilidade:
  fontes_ideais: ["Public Sans", "Inter", "Geist Sans", "Plus Jakarta Sans", "JetBrains Mono"]
  paletas_ideais: ["Nuxt Emerald Glow (#00DC82 / OKLCH)", "Slate / Zinc Clean Neutral", "Monochrome Obsidian Enterprise", "Cyberpunk Violet & Emerald"]
  combinacoes_recomendadas: ["@nuxt/icon (Iconify)", "@vueuse/core", "TanStack Vue Table", "Zod", "Valibot", "Nuxt Content", "Pinia", "ECharts / Tremor Vue"]
  conflitos_esteticos: ["Brutalismo Y2K sem bordas arredondadas e com cores dessincronizadas do espaço OKLCH", "Neumorfismo pastoso com sombras analógicas pesadas", "Frameworks legados de CSS global baseados em jQuery/Bootstrap"]
---

# Nuxt UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Nuxt UI** (evoluído para a geração v3/v4) é o design system canônico do ecossistema Vue e Nuxt, concebido por Benjamin Canac (@benjamincanac) e Sébastien Chopin (@Atinux) dentro da NuxtLabs (posteriormente unida à Vercel). Ao contrário de suítes de componentes genéricas portadas mecanicamente do ecossistema React, o Nuxt UI foi arquitetado de ponta a ponta para extrair a máxima sinergia com a reatividade do Vue 3, o compilador Vite e as convenções de Server-Side Rendering (SSR) e geração estática (SSG) do Nuxt.

### A Revolução Arquitetural: A Transição para o Nuxt UI v3/v4
Historicamente, o Nuxt UI v1/v2 dependia do *Headless UI* do Tailwind Labs. Com o surgimento da v3, a biblioteca passou por uma reengenharia holística fundamental:

1. **Migração para o Reka UI (anteriormente Radix Vue):**
   A base sem cabeça do Nuxt UI foi totalmente transferida para o **Reka UI**, mantido por Zernonia e pela comunidade open-source de Vue. O Reka UI oferece paridade funcional rigorosa com o Radix UI do React, garantindo conformidade WAI-ARIA integral, gerenciamento determinístico de foco (`focus-trap`), restauração de foco em desmontagem, suporte bidirecional de texto (RTL/LTR) e controle por teclado avançado em cada elemento interativo.
2. **Adoção Nativa do Tailwind CSS v4 e Espaço de Cor OKLCH:**
   O Nuxt UI v3 é um dos primeiros grandes design systems desenhados para o Tailwind CSS v4. Ele abandona arquivos de configuração JavaScript monolíticos (`tailwind.config.js`) em favor do paradigma CSS-first baseado na diretiva `@theme` e na especificação de cores perceptualmente lineares em **OKLCH**. Isso elimina bandas de distorção cromática em tons escuros e claros, permitindo paletas com contraste matematicamente calibrado (`oklch(72.3% 0.219 149.579)` para o verde esmeralda primário).
3. **Fusão e Abertura Integral do Nuxt UI Pro:**
   Com a entrada da equipe NuxtLabs na Vercel, todos os componentes e blocos anteriormente restritos à licença comercial do *Nuxt UI Pro* (estruturas completas de Dashboard, blocos de documentação, headers SaaS, grids de precificação e seções institucionais) foram incorporados diretamente ao repositório público e lançados 100% sob licença **MIT**, democratizando templates corporativos de alto escalão.
4. **Independência de Framework (Nuxt, Vue Puro, Laravel & AdonisJS):**
   Embora ofereça auto-imports e módulos nativos para o Nuxt (`@nuxt/ui`), a suíte agora funciona perfeitamente em aplicações Vue 3 puras com Vite (`@nuxt/ui/vite`), bem como em arquiteturas híbridas modernas com backends em **Laravel (Inertia.js)** e **AdonisJS**.

### A Assinatura Visual: "Emerald Craft & High-Density Ergonomics"
A assinatura estética do Nuxt UI combina sobriedade corporativa moderna com ergonomia cirúrgica para aplicações ricas em dados:

- **O Esmeralda Luminoso Nuxt (`--ui-primary`):** A cor de destaque padrão herda a vibrante tonalidade verde esmeralda do Nuxt (`#00DC82`), tratada em gradientes OKLCH que criam destaques sutis de foco (`ring-2 ring-primary-500/20`) e acentos luminosos discretos sem ofuscar o conteúdo.
- **Arquitetura de Slots Estruturados via `tailwind-variants` (`tv`):** Assim como os mais avançados sistemas de componentes modernos, cada componente do Nuxt UI decompõe sua anatomia em slots explícitos (ex: `root`, `base`, `header`, `body`, `footer`, `leading`, `trailing`, `label`, `error`). Isso permite que os desenvolvedores alterem classes granulares via a propriedade `ui` ou de forma global via `app.config.ts`, sem quebras de especificidade CSS graças ao `tailwind-merge`.
- **Raio de Borda Paramétrico (`--ui-radius`):** Toda a curvatura da interface responde dinamicamente à variável CSS `--ui-radius` (padrão `0.25rem` / `0.375rem`), permitindo transicionar a identidade inteira de uma aplicação entre um estilo ultra-técnico e angular (0px) e um estilo arredondado e amigável (12px-16px) alterando uma única linha de configuração.
- **Universalidade de Ícones com `@nuxt/icon`:** Através do mecanismo de renderização dinâmica do Iconify, qualquer ícone entre centenas de milhares de conjuntos abertos (Lucide, Heroicons, Phosphor, Simple Icons) pode ser declarado diretamente por nome de classe sem custos adicionais de bundle (`icon="i-lucide-sparkles"`).

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados

1. **SaaS B2B Full-Stack e Ferramentas Internas (Nuxt / Vue 3):**
   É a escolha indiscutível para equipes construindo plataformas corporativas sobre o Nuxt. Com validação integrada de formulários, data-grids virtuais e componentes de dashboard prontos, a velocidade de desenvolvimento para times Vue é até 3x superior ao uso de bibliotecas desacopladas.
2. **Plataformas de IA Generativa & Agentes Autônomos com Streaming Server-Side:**
   O modelo de execução híbrido do Nuxt (SSR/Nitro) aliado à reatividade refinada do Nuxt UI permite streaming fluido de tokens de modelos de linguagem, tooltips interativos de raciocínio, listas de passos colapsáveis (`UAccordion`) e painéis de prompt com atalhos de teclado ágeis.
3. **Developer Portals, Documentação Técnica & CMS Headless:**
   Integração nativa com o módulo `@nuxt/content`. O Nuxt UI fornece componentes tipados de documentação (`UPage`, `UPageHeader`, `UContentSearch`, `UPageAccordion`), caixas de callout estilizadas e blocos de código com destaque de sintaxe e botão de cópia instantânea.
4. **Dashboards Financeiros, FinTechs & BIs Interativos:**
   Aplicações onde o componente `UTable` (motorizado pelo TanStack Table) assume o controle: suporte a paginação assíncrona, ordenação multi-coluna, filtros compostos, seleção de linhas em lote e expansão hierárquica.

---

### Papel no Ritmo Visual (A Aplicação da Regra 60-30-10)

```
┌────────────────────────────────────────────────────────────────────────┐
│                    RITMO VISUAL COM NUXT UI (60-30-10)                 │
├────────────────────────────────┬───────────────────────┬───────────────┤
│              60%               │          30%          │      10%      │
│     FUNDAÇÃO & ESTRUTURA       │ INTERAÇÃO & NAVEGAÇÃO │ SHOWSTOPPERS  │
│  Superfícies de tela neutras,  │  Navbar colapsável,   │ CommandPalette│
│  cards de borda sutil, tables, │  slideovers laterais, │ spotlight,    │
│  inputs tipados e tipografia   │  tabs com transição e │ toasts com    │
│  homogênea em OKLCH neutral    │  dropdowns acessíveis │ timer e badges│
└────────────────────────────────┴───────────────────────┴───────────────┘
```

- **60% — Fundação Neutra e Superfícies de Trabalho:**
  O Nuxt UI orquestra as cores neutras de fundo e borda (`--ui-bg`, `--ui-bg-muted`, `--ui-border`, `--ui-border-muted`). `UCard`, `UTable`, `UFormField` e `USeparator` constituem a espinha dorsal do layout, mantendo um cinza ardósia balanceado (`Slate` ou `Zinc`) que valoriza os dados e a tipografia.
- **30% — Camada de Navegação, Orquestração e Modais:**
  Elementos de orientação espacial do usuário: `UDashboardLayout`, `UDashboardPanel` com redimensionamento dinâmico e colapso suave, `UNavigationMenu` com indicadores de foco, `USlideover` deslizando da margem direita para edição rápida e `UTabs` com navegação contínua.
- **10% — Showstoppers de Produtividade e Feedback Visual:**
  O toque "power-user": a ativação instantânea da barra de comando via atalho global `Cmd+K` / `Ctrl+K` (`UCommandPalette`), o anel pulsante de status de servidores (`UBadge color="primary" variant="subtle"`), os banners de notificação reativos empilhados no canto inferior (`useToast().add(...)`) e atalhos de teclado renderizados fisicamente com teclas gráficas (`UKbd`).

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

1. **Aplicações React ou Angular Puras:**
   O Nuxt UI é estruturado exclusivamente sobre a reatividade do Vue 3 (`ref`, `computed`, `<script setup>`) e primitivas Reka UI. Forçar o Nuxt UI em ecossistemas React através de pontes de compilação ou web-components gera atrito desnecessário; para React, utilize Shadcn UI ou HeroUI.
2. **Websites Institucionais 3D / Experiências Artísticas High-Motion Imersivas:**
   Sites com foco primordial em WebGL, Canvas 3D (Three.js), shaders pesados e tipografia kinetic experimental não encontram utilidade em um design system desenhado para formulários, dashboards e tabelas. Nesses cenários, bibliotecas como Three.js/TresJS com CSS sob medida são superiores.
3. **Projetos Brutalistas Cruos (Neobrutalism / Y2K Sem Curvatura):**
   Embora o Nuxt UI suporte `--ui-radius: 0`, sua linguagem padrão adota bordas finas com tons translúcidos, anéis de foco delicados e elevações discretas. Forçar contornos pretos rígidos de 3px com sombras diagonais duras entra em conflito com a semântica nativa dos componentes.
4. **Bypass de Tokens via Cores Hexadecimais Aleatórias:**
   Um anti-padrão comum é ignorar as propriedades de cor semânticas do Nuxt UI (`primary`, `neutral`, `success`, `error`) e aplicar classes como `bg-[#22c55e]` ou `text-[#1e293b]`. Isso anula a calibração de contraste no Dark Mode e quebra as variáveis de tema globais.

### ⚠️ Erros Comuns de Implementação & Exageros

- **Não envolver a aplicação no componente raiz `<UApp>`:**
  No Nuxt UI v3/v4, o componente `<UApp>` é o provedor de contexto global para injeção de modais, gavetas (`useOverlay`), toasts (`useToast`) e tooltips. Esquecer de colocá-lo no `app.vue` faz com que notificações e popups deixem de funcionar silenciosamente.
- **Conflito Desordenado de Atalhos de Teclado (`defineShortcuts`):**
  Definir teclas de letra simples (como `d`, `s`, `e`) globalmente sem verificar se o foco do usuário está dentro de um `<input>` ou `<textarea>`. O Nuxt UI filtra nativamente inputs de texto, mas criar atalhos não intuitivos sem exibi-los via `<UKbd>` cria uma experiência frustrante para o usuário.
- **Empilhar múltiplos Slideovers e Modais simultaneamente:**
  Utilizar `USlideover` para abrir outro `USlideover` sobreposto a um `UModal`. A interface perde ancoragem visual e pode causar contenção de rolagem na janela subjacente.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

### 1. `UCommandPalette` (Central de Comandos & Spotlight Fuzzy Search)
- **Anatomia Visual:** Caixa modal flutuante centralizada com desfoque de fundo escurecido. Possui campo de busca no topo com ícone de lupa expansível, indicador de tecla `Esc`, categorização de resultados em grupos divididos por cabeçalhos sutis (`Recentes`, `Navegação`, `Ações`, `Projetos`), badges de atalhos (`UKbd`) alinhados à direita e suporte a estados vazios customizáveis.
- **Gatilho de Interação:** Disparado globalmente por teclado (`meta_k` ou `ctrl_k`) ou via clique em botões de busca na barra de topo. O teclado navega pelos itens com setas dimensionais (`ArrowUp`/`ArrowDown`) e executa com `Enter`.
- **Onde Encaixar:** Na raiz do aplicativo (`app.vue`), invocado sob demanda em qualquer página como ferramenta primária de produtividade de usuários de SaaS.

### 2. `UTable` (Data Grid Headless com TanStack Table)
- **Anatomia Visual:** Tabela de dados moderna com tipografia tabular monoespaçada opcional, suporte a ordenação nas colunas com setas indicativas de direção (`asc`/`desc`), seleção de linhas via checkboxes com estilo primário, linhas divisórias finas e zebra striping opcional.
- **Gatilho de Interação:** Clique nos cabeçalhos para alternar estados de ordenação; checkboxes de seleção única ou "selecionar todos"; paginação responsiva no rodapé.
- **Onde Encaixar:** Visões principais de dashboards operacionais, listagem de clientes, inventários, relatórios de faturamento e painéis de auditoria.

### 3. `USlideover` (Painel Lateral de Drawer Deslizante)
- **Anatomia Visual:** Painel lateral flutuante que emerge com fluidez da borda direita (ou esquerda/topo/base) da tela, ocupando toda a altura do viewport. Conta com backdrop semitransparente escurecido, cabeçalho com título, descrição e botão de fechar com hover suave, corpo scrollável independente e rodapé fixo para botões de ação ("Salvar", "Cancelar").
- **Gatilho de Interação:** Invocado programaticamente via `useOverlay().open()` ou condicionalmente via `v-model:open`. Pode ser configurado como modal bloqueante (`modal: true`) ou não-bloqueante (`modal: false`), permitindo interagir com o conteúdo ao lado.
- **Onde Encaixar:** Edição rápida de entidades, visualização detalhada de dados de uma linha da tabela, formulários de criação complexos e configurações de usuário.

### 4. `UModal` (Janela de Diálogo Acessível Reka UI)
- **Anatomia Visual:** Janela de diálogo com cantos arredondados (`--ui-radius`), sombra dimensional profunda (`shadow-2xl`), bordas finas com contraste suave contra o backdrop (`border border-neutral-200 dark:border-neutral-800`), e contenção estrita de rolagem interna.
- **Gatilho de Interação:** Clique em botões de confirmação/gatilhos ou ativação programática imperativa. Suporta fechamento via tecla `Esc` ou clique fora da área útil.
- **Onde Encaixar:** Confirmações destrutivas de exclusão, diálogos de checkout, importação em lote de arquivos e autenticação modal.

### 5. `UForm` & `UFormField` (Validação Isomórfica Type-Safe com Zod / Valibot)
- **Anatomia Visual:** Formulário corporativo com rótulos semânticos (`label`), indicadores de obrigatoriedade opcionais, textos descritivos de ajuda (`description`), ícones de leading/trailing e renderização instantânea de mensagens de erro (`error`) com transição suave de altura e coloração de alerta.
- **Gatilho de Interação:** Validação reativa em tempo real com debounce, ao desfocar o campo (`blur`) ou na submissão (`submit`), integrando schemas de validação Zod no cliente e no servidor Nitro sem duplicação de lógica.
- **Onde Encaixar:** Telas de cadastro, onboarding, edição de preferências, fluxos de pagamento e formulários de suporte.

### 6. `UDashboardLayout`, `UDashboardPanel` & `UDashboardNavbar` (Arquitetura Pro de Workspace)
- **Anatomia Visual:** Estrutura modular em colunas divididas por barras de ferramentas com altura uniforme (`--ui-header-height: 4rem`). O painel lateral (`UDashboardSidebar`) suporta colapso fluido entre modo estendido (com ícone e texto) e modo compacto (apenas ícones com tooltips flutuantes automáticos). Suporta divisores arrastáveis para redimensionamento manual pelo usuário.
- **Gatilho de Interação:** Botão toggle de gaveta, atalhos de teclado (ex: `[` para recolher a sidebar) e manipulação por drag nos manipuladores de borda.
- **Onde Encaixar:** Layout padrão de plataformas corporativas SaaS, portais administrativos e backoffices modernos.

### 7. `UNavigationMenu` & `UDropdownMenu` (Navegação Hierárquica Reka UI)
- **Anatomia Visual:** Itens de menu com estados visuais refinados: foco com fundo sutil (`bg-neutral-100 dark:bg-neutral-800`), ícones temáticos alinhados à esquerda, atalhos de teclado (`UKbd`) à direita e suporte a badges de notificação e submenus em cascata com setas de orientação.
- **Gatilho de Interação:** Hover ou clique para expansão, navegação por setas do teclado com suporte a busca rápida de itens digitando a primeira letra (typeahead).
- **Onde Encaixar:** Menus contextuais de linha de tabela, menu de perfil do usuário na barra de topo e menus de navegação primária.

### 8. `UToast` / `useToast` (Sistema Reativo de Notificações Empilhadas)
- **Anatomia Visual:** Cards flutuantes compactos com ícone de status colorido (sucesso, erro, alerta, info), título em negrito, descrição de suporte, botão de ação embutido (ex: "Desfazer") e barra de progresso horizontal linear animada indicando o tempo restante até a expiração automática.
- **Gatilho de Interação:** Invocado a partir de qualquer composable ou componente via chamada de função reativa `toast.add({ title: '...', color: 'success' })`.
- **Onde Encaixar:** Feedback imediato de ações assíncronas (salvamento de dados, falha de rede, cópia de link para o clipboard).

### 9. `UInputMenu` & `USelectMenu` (Seleção Rica com Busca Integrada)
- **Anatomia Visual:** Campo seletor moderno que combina a ergonomia de um dropdown com o poder de filtragem em tempo real de uma caixa de pesquisa. Suporta avatares de usuários, ícones de status, chips de seleção múltipla e renderização virtual para milhares de opções.
- **Gatilho de Interação:** Clique para abrir a lista suspensa; digitação para filtrar imediatamente itens na memória ou consultar endpoints remotos de forma assíncrona.
- **Onde Encaixar:** Atribuição de responsáveis por tarefas, seleção de tags em posts, busca de países/moedas e filtros compostos de pesquisa.

### 10. `defineShortcuts` & `UKbd` (Orquestração Háptica de Produtividade Global)
- **Anatomia Visual:** O componente `UKbd` simula visualmente uma tecla física de teclado: fundo elevado, borda inferior sutil simulando profundidade tridimensional (`border-b-2`), cantos suavemente arredondados e tipografia monoespaçada limpa. O composable `defineShortcuts` gerencia os gatilhos no sistema sem poluir listeners manuais.
- **Gatilho de Interação:** Pressionamento físico de teclas no hardware, com detecção automática do sistema operacional do usuário (exibe o símbolo `⌘` no macOS e `Ctrl` no Windows/Linux).
- **Onde Encaixar:** Ao lado de itens de menu, botões de ação do dashboard, barras de pesquisa e cards de ajuda do sistema.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup Oficial

Para projetos Nuxt 3 ou 4, a instalação e integração ocorrem através do módulo oficial:

```bash
# Instalação no ecossistema Nuxt
npx nuxi@latest module add ui

# Para projetos Vue 3 puros com Vite
npm install @nuxt/ui @vueuse/core zod
```

Configuração mínima no arquivo `nuxt.config.ts`:

```typescript
// nuxt.config.ts
export default defineNuxtConfig({
  modules: ['@nuxt/ui'],
  css: ['~/assets/css/main.css'],
  compatibilityDate: '2026-10-26'
})
```

Configuração de temas e tokens no arquivo `app.config.ts`:

```typescript
// app.config.ts
export default defineAppConfig({
  ui: {
    primary: 'emerald', // Define a cor primária global
    neutral: 'slate',   // Define a escala neutra (slate, zinc, gray, neutral)
    card: {
      slots: {
        root: 'border border-neutral-200 dark:border-neutral-800 shadow-sm transition-all duration-200',
        header: 'p-4 sm:px-6 font-semibold border-b border-neutral-100 dark:border-neutral-800',
        body: 'p-4 sm:p-6'
      }
    },
    button: {
      defaultVariants: {
        size: 'md',
        color: 'primary',
        variant: 'solid'
      }
    }
  }
})
```

---

### Física de Movimento, Animações e Data-Attributes

O Nuxt UI v3 implementa um motor de animações ultra-eficiente que minimiza o uso de JavaScript para montagem visual, confiando em **CSS Transitions nativas e Data-Attributes do Reka UI**:

- **Estados de Transição Reka UI:**
  - `[data-state="open"]` / `[data-state="closed"]`
  - `[data-highlighted]` / `[data-disabled]`
  - `[data-side="top"]` / `[data-side="bottom"]`
- **Curvas de Animação Recomendadas:**
  - **Abertura de Overlays (Pop/Scale):**
    ```css
    cubic-bezier(0.16, 1, 0.3, 1) /* Spring de desaceleração suave, duração 200ms */
    ```
  - **Deslize de Slideovers:**
    ```css
    cubic-bezier(0.25, 1, 0.5, 1) /* Duração 300ms */
    ```
  - **CSS `@starting-style` (Tailwind v4):** Permite animar elementos a partir de `display: none` para `display: block` de forma declarativa e acelerada por GPU sem quebras de layout.

---

### Receita de Código Funcional: Dashboard Enterprise com Table, Form, Modal e Shortcuts

Abaixo está uma implementação completa e funcional em formato Single File Component (`.vue`) demonstrando o padrão arquitetural profissional do Nuxt UI:

```vue
<!-- components/EnterpriseManagementDashboard.vue -->
<script setup lang="ts">
import { z } from 'zod'
import type { FormSubmitEvent } from '#ui/types'

// 1. Definição do Schema de Validação via Zod
const userSchema = z.object({
  name: z.string().min(3, 'O nome deve conter ao menos 3 caracteres'),
  email: z.string().email('E-mail institucional inválido'),
  role: z.enum(['admin', 'editor', 'viewer'], {
    errorMap: () => ({ message: 'Selecione uma função válida' })
  }),
  notifications: z.boolean().default(true)
})

type UserSchema = z.output<typeof userSchema>

// 2. Estado Reativo da Aplicação
const isCreateModalOpen = ref(false)
const isCommandPaletteOpen = ref(false)
const searchQuery = ref('')
const toast = useToast()

const users = ref([
  { id: '1', name: 'Guilherme Castro', email: 'guilherme@acme.inc', role: 'admin', status: 'Ativo' },
  { id: '2', name: 'Beatriz Vasconcelos', email: 'beatriz@acme.inc', role: 'editor', status: 'Ativo' },
  { id: '3', name: 'Rodrigo Medeiros', email: 'rodrigo@acme.inc', role: 'viewer', status: 'Pendente' }
])

// 3. Colunas da Tabela TanStack
const tableColumns = [
  { accessorKey: 'name', header: 'Nome do Membro' },
  { accessorKey: 'email', header: 'E-mail Corporativo' },
  { accessorKey: 'role', header: 'Função' },
  { accessorKey: 'status', header: 'Status' },
  { id: 'actions', header: '' }
]

// 4. Formulário e Submissão Isomórfica
const formData = reactive<UserSchema>({
  name: '',
  email: '',
  role: 'editor',
  notifications: true
})

async function onUserSubmit(event: FormSubmitEvent<UserSchema>) {
  const newUser = {
    id: String(Date.now()),
    ...event.data,
    status: 'Ativo'
  }
  
  users.value.push(newUser)
  isCreateModalOpen.value = false
  
  // Feedback com Toast Reativo
  toast.add({
    title: 'Usuário Criado',
    description: `${event.data.name} foi adicionado à organização.`,
    color: 'success',
    icon: 'i-lucide-check-circle'
  })

  // Limpeza do formulário
  formData.name = ''
  formData.email = ''
  formData.role = 'editor'
}

// 5. Orquestração de Atalhos de Teclado Globais
defineShortcuts({
  meta_k: {
    usingInput: true,
    handler: () => {
      isCommandPaletteOpen.value = !isCommandPaletteOpen.value
    }
  },
  n: () => {
    isCreateModalOpen.value = true
  }
})

// 6. Dados para a Command Palette
const commandGroups = computed(() => [
  {
    id: 'actions',
    label: 'Ações Rápidas',
    items: [
      {
        id: 'new-user',
        label: 'Convidar Novo Usuário',
        icon: 'i-lucide-user-plus',
        kbds: ['n'],
        onSelect: () => {
          isCommandPaletteOpen.value = false
          isCreateModalOpen.value = true
        }
      },
      {
        id: 'export-csv',
        label: 'Exportar Relatório CSV',
        icon: 'i-lucide-download',
        onSelect: () => {
          isCommandPaletteOpen.value = false
          toast.add({ title: 'Exportação iniciada', color: 'info', icon: 'i-lucide-file-spreadsheet' })
        }
      }
    ]
  }
])
</script>

<template>
  <div class="min-h-screen bg-neutral-50 dark:bg-neutral-950 text-neutral-900 dark:text-neutral-100 p-6 sm:p-10">
    <div class="max-w-6xl mx-auto space-y-8">
      
      <!-- Cabeçalho com Barra de Ferramentas -->
      <div class="flex flex-col sm:flex-row justify-between items-start sm:items-center gap-4 border-b border-neutral-200 dark:border-neutral-800 pb-6">
        <div>
          <div class="flex items-center gap-2">
            <h1 class="text-2xl font-bold tracking-tight">Equipe & Governança</h1>
            <UBadge variant="subtle" color="primary" class="font-mono">v4.0</UBadge>
          </div>
          <p class="text-sm text-neutral-500 dark:text-neutral-400 mt-1">
            Gerencie credenciais de acesso, permissões e status dos membros do time.
          </p>
        </div>

        <div class="flex items-center gap-3">
          <!-- Botão Gatilho do Command Palette com Tecla Física -->
          <UButton
            variant="outline"
            color="neutral"
            icon="i-lucide-search"
            class="hidden sm:inline-flex text-xs"
            @click="isCommandPaletteOpen = true"
          >
            Comandos
            <template #trailing>
              <UKbd value="meta" />
              <UKbd value="k" />
            </template>
          </UButton>

          <!-- Botão Principal de Criação -->
          <UButton
            color="primary"
            icon="i-lucide-plus"
            @click="isCreateModalOpen = true"
          >
            Novo Usuário
          </UButton>
        </div>
      </div>

      <!-- Card com a Tabela de Dados TanStack -->
      <UCard>
        <template #header>
          <div class="flex items-center justify-between">
            <h2 class="text-base font-semibold">Membros Ativos ({{ users.length }})</h2>
            <UInput
              v-model="searchQuery"
              icon="i-lucide-filter"
              placeholder="Filtrar por nome..."
              size="sm"
              class="w-64"
            />
          </div>
        </template>

        <UTable :data="users" :columns="tableColumns">
          <!-- Customização do Slot de Status -->
          <template #status-cell="{ row }">
            <UBadge
              :color="row.original.status === 'Ativo' ? 'success' : 'warning'"
              variant="subtle"
              size="sm"
            >
              {{ row.original.status }}
            </UBadge>
          </template>

          <!-- Customização do Slot de Ações -->
          <template #actions-cell="{ row }">
            <div class="text-right">
              <UDropdownMenu
                :items="[
                  [
                    { label: 'Editar Membro', icon: 'i-lucide-edit-2' },
                    { label: 'Revogar Acesso', icon: 'i-lucide-trash', color: 'error' }
                  ]
                ]"
              >
                <UButton variant="ghost" color="neutral" icon="i-lucide-more-horizontal" size="xs" />
              </UDropdownMenu>
            </div>
          </template>
        </UTable>
      </UCard>

      <!-- Modal de Criação de Usuário com UForm e Zod -->
      <UModal v-model:open="isCreateModalOpen" title="Convidar Novo Membro">
        <template #content>
          <UForm :schema="userSchema" :state="formData" class="space-y-4 p-6" @submit="onUserSubmit">
            
            <UFormField label="Nome Completo" name="name" required>
              <UInput v-model="formData.name" placeholder="Ex: Lucas Silveira" icon="i-lucide-user" />
            </UFormField>

            <UFormField label="E-mail Corporativo" name="email" required>
              <UInput v-model="formData.email" type="email" placeholder="lucas@acme.inc" icon="i-lucide-mail" />
            </UFormField>

            <UFormField label="Função Organizacional" name="role" required>
              <USelect
                v-model="formData.role"
                :items="[
                  { label: 'Administrador Geral', value: 'admin' },
                  { label: 'Editor de Conteúdo', value: 'editor' },
                  { label: 'Visualizador Somente Leitura', value: 'viewer' }
                ]"
              />
            </UFormField>

            <UFormField name="notifications">
              <div class="flex items-center gap-2">
                <USwitch v-model="formData.notifications" />
                <span class="text-sm text-neutral-600 dark:text-neutral-400">
                  Enviar e-mail automático com instruções de onboarding
                </span>
              </div>
            </UFormField>

            <div class="flex justify-end gap-3 pt-4 border-t border-neutral-100 dark:border-neutral-800">
              <UButton variant="ghost" color="neutral" @click="isCreateModalOpen = false">
                Cancelar
              </UButton>
              <UButton type="submit" color="primary">
                Confirmar Convite
              </UButton>
            </div>
          </UForm>
        </template>
      </UModal>

      <!-- Spotlight Command Palette Modal -->
      <UModal v-model:open="isCommandPaletteOpen">
        <template #content>
          <UCommandPalette :groups="commandGroups" placeholder="Digite uma ação ou pesquise..." />
        </template>
      </UModal>

    </div>
  </div>
</template>
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar e especificar o **Nuxt UI** dentro de um `DESIGN_BLUEPRINT.md`, a inteligência artificial deve seguir as seguintes diretrizes normativas:

1. **Declaração do Componente Raiz de Contexto (`<UApp>`):**
   - No blueprint, o arquivo raiz (`app.vue`) deve ser expressamente especificado com a tag `<UApp>` contendo o slot de páginas (`<NuxtPage />`). Sem `<UApp>`, recursos essenciais como `useToast()`, `useOverlay()` e popovers são bloqueados.
2. **Definição Explícita de Tokens de Cor e Escala Neutra:**
   - Especifique a cor de realce primária (`primary: 'emerald' | 'indigo' | 'violet' | 'amber' | 'cyan'`) e a família de neutros (`neutral: 'slate' | 'zinc' | 'neutral'`). Exemplo:
     ```yaml
     theme_tokens:
       framework: "Nuxt UI v3/v4"
       primary_color: "emerald" # oklch(72.3% 0.219 149.579)
       neutral_color: "slate"   # slate-50 to slate-950
       border_radius: "0.375rem" # 6px moderno
       icon_provider: "@nuxt/icon (Lucide set)"
     ```
3. **Padrão Obrigatório de Formulários com Validação Isomórfica:**
   - Proibir a manipulação manual de erros de input via tags genéricas `<span>`. Todo formulário deve ser documentado utilizando o par composicional `<UForm>` + `<UFormField>` associado a um schema tipado de validação **Zod** ou **Valibot**.
4. **Mapeamento de Atalhos de Produtividade (`defineShortcuts`):**
   - Para aplicações operacionais ou dashboards complexos, declare explicitamente no blueprint a matriz de atalhos globais, sempre vinculando os gatilhos a indicadores visuais com `<UKbd>` para garantir a descoberta intuitiva pelos usuários.
5. **Estratégia de Gestão de Overlays (Evitar `v-if` e `v-show` Manuais):**
   - Recomende o uso do padrão declarativo `v-model:open` nos componentes `<UModal>` e `<USlideover>` ou, em fluxos desacoplados, a injeção via o composable `useOverlay()`.
