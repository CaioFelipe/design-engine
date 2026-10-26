---
id: "merakiui"
name: "Meraki UI"
url: "https://www.merakiui.com/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Clean Functional Minimalism", "Native Bi-Directional RTL", "Accessible Dual Dark Mode", "Alpine.js Headless Micro-Interactions", "Semantic Utility Spacing"]
densidade_informacao: "Flexivel"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS/Headless)"
stack_frameworks: ["Tailwind CSS v3 / v4", "Alpine.js", "HTML5 Semântico", "React / Next.js compatible", "Laravel Blade compatible", "Vue / Nuxt compatible", "Heroicons", "Coolicons"]
compatibilidade:
  fontes_ideais: ["Inter", "Plus Jakarta Sans", "IBM Plex Sans Arabic", "Cairo", "Tajawal", "Readex Pro", "Rubik", "Geist Sans"]
  paletas_ideais: ["Classic Sapphire Blue & Slate", "Emerald Growth & Neutral Charcoal", "Deep Zinc / Gray Dark Mode (gray-900 / gray-800)", "High-Contrast Accessible Monochrome"]
  combinacoes_recomendadas: ["Heroicons", "Lucide React", "Alpine.js", "Tailwind Forms Plugin", "Tailwind Typography Plugin", "TanStack Table", "ApexCharts / Recharts"]
  conflitos_esteticos: ["Brutalismo Y2K cru com bordas pretas duras de 3px e sombras sem difusão", "Skeuomorfismo pesado / Glassmorphism extremo fluorescente", "Cyberpunk neon com aberração cromática"]
---

# Meraki UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Meraki UI** (`https://www.merakiui.com/`), idealizado e mantido por **Khatab Wedatalla** (`@khatabwedaa`) e **Mosab Ibrahim** (`@miaababikir`) sob a chancela da organização **Meraki UI Labs**, é uma das coleções de componentes Tailwind CSS open-source mais influentes e adotadas globalmente. Enquanto grande parte das bibliotecas modernas foca exclusivamente em ecossistemas fechados de JavaScript (como suítes pesadas atreladas a Next.js ou React), o Meraki UI propõe um retorno pragmático e elegante à web modular, combinando marcação HTML5 semântica, utilitários puros de **Tailwind CSS (v3 e v4)** e micro-interatividade declarativa ultraleve via **Alpine.js**.

### O Pilar Diferencial: Bi-direcionalidade Nativa (RTL First-Class)
A imensa maioria dos design systems ocidentais trata a escrita da direita para a esquerda (RTL — *Right-to-Left*) como uma reflexão tardia (*afterthought*), resultando em interfaces desconfiguradas quando traduzidas para o árabe, hebraico, farsi ou urdu. 

O Meraki UI nasceu com **RTL como requisito arquitetural nativo de primeira classe**. Cada bloco, navbar, tabela e card foi concebido para espelhar perfeitamente seu fluxo visual com a simples inclusão do atributo `dir="rtl"` no elemento raiz ou ancestral:
- Alinhamentos dinâmicos declarados com pares `text-left rtl:text-right`.
- Espaçamentos e margens que respeitam o sentido de leitura ou utilizam classes lógicas.
- Inversão geométrica automática de iconografia direcional (como setas de navegação e botões anterior/próximo) através do utilitário Tailwind `rtl:-scale-x-100`.

### A Assinatura Visual: "Clean Functional Minimalism & Cohesive Dual Mode"
O Meraki UI não busca o espetáculo pirotécnico de shaders 3D ou animações exageradas; sua assinatura reside no acabamento impecável, legível e ergonômico:

1. **Dual Dark Mode de Alta Fidelidade Sem Ruído:**
   Ao contrário de implementações descuidadas que aplicam preto puro `#000000` em tudo, o Meraki UI calibra uma hierarquia cromática de tons de cinza frios: superfícies principais em `dark:bg-gray-900`, containers e cards em `dark:bg-gray-800`, bordas sutis de delimitação em `dark:border-gray-700` e tipografia secundária legível em `dark:text-gray-400` / `dark:text-gray-300`.
2. **Acento Lateral de Ênfase Tátil (Barra de Destaque Semântica):**
   Um dos padrões mais copiados da web: cards de notificação e alertas do Meraki UI empregam uma haste vertical rígida na extremidade (`w-2 bg-blue-600 dark:bg-blue-500` ou `w-2 bg-emerald-500`), gerando uma âncora visual instantânea sem poluir a área central de leitura.
3. **Anéis de Foco Acessíveis com Atenuação de Opacidade:**
   Em vez de outlines ruidosos do navegador, os elementos interativos adotam anéis de foco suaves e bem contrastados: `focus:outline-none focus:ring focus:ring-blue-300 focus:ring-opacity-40 dark:focus:ring-blue-400 dark:focus:ring-opacity-40`.
4. **Micro-interatividade Desacoplada (O Modelo Alpine.js):**
   Dropdowns, gavetas laterais de navegação, modais e abas funcionam através de diretivas imperceptíveis no HTML (`x-data`, `x-show`, `x-transition`, `@click.away`). O desenvolvedor ganha uma interface totalmente interativa sem a sobrecarga de 200kB de runtime React e sem necessidade de compilação JS pesada.
5. **Filosofia Copy-Paste de Zero Fricção:**
   Não há CLIs proprietárias obrigatórias, nem dependências de pacotes NPM fechados. O desenvolvedor copia o bloco HTML pronto, insere no seu projeto (seja ele Laravel Blade, Django, Rails, Astro, Nuxt ou Next.js) e tem um componente em produção em segundos.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados

1. **Aplicações Globais e Bilíngues com Suporte a MENA e Israel (Árabe, Hebraico, Farsi, Urdu):**
   Qualquer plataforma SaaS, portal governamental ou e-commerce com audiência no Oriente Médio e Norte da África encontra no Meraki UI a fundação mais madura do ecossistema Tailwind para alternar entre `dir="ltr"` e `dir="rtl"` sem refatorar o CSS.
2. **SaaS B2B, Painéis Administrativos e CRMs Corporativos:**
   Aplicações onde a produtividade do usuário final depende de clareza, tabelas com checkbox, paginação confiável, sidebars com submenus agrupados e formulários com validações limpas.
3. **Aplicações Monolíticas Modernas e Server-Driven UI:**
   Projetos baseados em **Laravel (Blade / Livewire)**, **Ruby on Rails (Hotwire / Stimulus)**, **Django / Flask**, **Elixir Phoenix (LiveView)** e **Go Templates**. A integração do Meraki UI com Tailwind + Alpine.js casa perfeitamente com a filosofia dessas stacks, garantindo interatividade sem precisar criar uma SPA em React.
4. **Micro-frontends, Landing Pages e MVPs de Alta Velocidade:**
   Projetos que precisam ser lançados em questão de dias. Com mais de 200 blocos prontos divididos entre Application UI e Marketing UI (Heros, Pricing, Testimonials, FAQ, Footers, Contact, 404), o tempo de design para código é virtualmente reduzido a zero.

---

### Papel no Ritmo Visual (A Aplicação Rigorosa da Regra 60-30-10)

```
┌────────────────────────────────────────────────────────────────────────┐
│                   DISTRIBUIÇÃO HARMONIOSA MERAKI UI                    │
├────────────────────────────────┬───────────────────────┬───────────────┤
│              60%               │          30%          │      10%      │
│     FUNDAÇÃO & ESTRUTURA       │ NAVEGAÇÃO & TRANSIÇÃO │ SHOWSTOPPERS  │
│  Superfícies neutras, tabelas, │   Navbars responsivas,│ Modais com    │
│  cards de conteúdo, grids      │  sidebars agrupadas,  │ backdrop blur,│
│  flexbox/CSS grid e tipografia │  dropdowns animados e │ pop alerts com│
│  legível em dual mode          │  paginação com flip   │ barra lateral │
└────────────────────────────────┴───────────────────────┴───────────────┘
```

- **60% — Fundação Neutra e Superfícies Estruturais:**
  O Meraki UI gerencia a malha de layout: fundos `bg-white dark:bg-gray-900`, cartões `bg-white dark:bg-gray-800 border border-gray-200 dark:border-gray-700`, inputs de dados com tipografia regular e tabelas bem divididas (`divide-y divide-gray-200 dark:divide-gray-700`). Essa base garante estabilidade visual e alta legibilidade.
- **30% — Camada de Navegação, Orquestração e Micro-interações:**
  A navegação fluida: a `Navbar` com menu hambúrguer responsivo para telas pequenas, a `Sidebar` com ícones alinhados e rótulos de seção (`LabelSection`), o componente `Dropdown` com transição de escala de 90% para 100%, e o sistema de `Pagination` com inversão direcional.
- **10% — Showstoppers Protagonistas e Acentos de Foco:**
  O impacto focal de alta semântica: o `Modal` que surge com transição suave `translate-y-4` para `translate-y-0` e alinhamento centrado; os `Notification Pop Alerts` com a barra lateral em cor de alta saturação; e os botões de conversão e badges de status pulsantes.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

1. **Portfólios Artísticos Experimentais e Experiências 3D/WebGL:**
   Projetos focados em premiar no Awwwards, repletos de shaders Three.js, partículas interativas no mouse e tipografia monumental desestruturada. O Meraki UI possui DNA utilitário e estruturado; usá-lo em uma experiência puramente artística parecerá engessado.
2. **Terminais Financeiros de Densidade Extrema (Estilo Bloomberg / FactSet):**
   Sistemas de trading de alta frequência onde 120 linhas precisam caber em uma única tela de 1080p sem paddings generosos entram em conflito com o espaçamento confortável do Meraki UI (`px-4 py-3.5`, `rounded-md`, `rounded-lg`).
3. **Projetos Brutalistas Radicais (Neo-brutalism / Y2K Anti-Design):**
   Estéticas que exigem bordas pretas grossas de 3px a 4px, sombras projetadas duras sem difusão (`shadow-[4px_4px_0px_#000]`) e ângulos retos sem curvatura contrastam diretamente com as curvas suaves (`rounded-md`, `rounded-xl`) e sombras difusas (`shadow-md`, `shadow-xl`) do Meraki UI.

### ⚠️ Erros Comuns de Exagero & Anti-padrões:

1. **Carregar o Alpine.js Dentro de Projetos React / Next.js / Vue:**
   Copiar cegamente trechos com diretivas `x-data`, `x-show`, `x-transition` e `@click` para dentro de arquivos JSX/TSX causa erros de compilação ou comportamentos anômalos. Em projetos React, deve-se converter as diretivas do Alpine para hooks nativos (`useState`, `useTransition`) ou bibliotecas acessíveis como Radix UI / Headless UI.
2. **Quebra de RTL por Uso de Classes Absolutas Não-Lógicas:**
   Ao customizar componentes do Meraki UI, substituir classes como `mx-1 rtl:-scale-x-100` ou `text-left rtl:text-right` por classes unilaterais rígidas (como `ml-6` ou `pl-8`) destrói a bi-direcionalidade no modo árabe/hebraico. Sempre utilize classes do modificador `rtl:` ou utilitários lógicos do Tailwind CSS v3.3+ (`ms-`, `me-`, `ps-`, `pe-`, `start-`, `end-`).
3. **Acúmulo de Múltiplos Estilos de Card na Mesma Visão:**
   O Meraki UI oferece mais de 10 variações de cards (com imagem de cabeçalho, com avatar flutuante, com borda lateral, com background escuro). Misturar três padrões diferentes na mesma tela gera fadiga cognitiva e desarmonia.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

O repositório do Meraki UI é estruturado em blocos de **Application UI** e **Marketing UI**. A seguir, detalhamos os 10 componentes mais emblemáticos da biblioteca:

```
┌────────────────────────────────────────────────────────────────────────┐
│                   CATÁLOGO DE COMPONENTES MERAKI UI                    │
├───────────────────────────────┬────────────────────────────────────────┤
│ COMPONENTE                    │ CATEGORIA & ASSINATURA TÉCNICA         │
├───────────────────────────────┼────────────────────────────────────────┤
│ 1. Invoices & Files Table     │ App UI / Checkbox + Badges + Sort RTL  │
│ 2. Dual-Tone Sidebar          │ App UI / Multi-Level + Label Sections  │
│ 3. Directional Icon Pager     │ App UI / SVG Flip rtl:-scale-x-100     │
│ 4. Pop & Full-Width Alerts    │ App UI / Lateral Semantic Accent Bar   │
│ 5. Smooth Transition Modal    │ App UI / Alpine Dialog + Scale Easing  │
│ 6. Origin-Anchored Dropdown   │ App UI / Focus Ring + Click.Away       │
│ 7. App Store & Market CTA     │ Marketing / Dual OS App Conversion     │
│ 8. Multi-Tier Pricing Matrix  │ Marketing / Highlight Tier + Checkmarks│
│ 9. Responsive Mobile Navbar   │ Marketing & App / Hamburger Drawer     │
│ 10. Floating Cookie Banner    │ App UI / Dismissible Privacy Floating  │
└───────────────────────────────┴────────────────────────────────────────┘
```

### 1. Invoices & Files Table (`components/tables/Invoices.html`)
- **Anatomia Visual:** Uma tabela corporativa completa envolvida por container com scroll horizontal suave (`overflow-x-auto sm:-mx-6 lg:-mx-8`). Cabeçalho em `bg-gray-50 dark:bg-gray-800` com tipografia semântica em caixa baixa/alta `font-normal text-sm text-gray-500 dark:text-gray-400`. Linhas separadas por `divide-y divide-gray-200 dark:divide-gray-700`, com checkboxes estilizados (`rounded text-blue-500`) e badges arredondados (`rounded-full`) para status ("Paid", "Pending", "Failed").
- **Gatilho de Interação:** Hover nas linhas com troca sutil de cor (`hover:bg-gray-50 dark:hover:bg-gray-700`), clique nas caixas de seleção e clique nas setas de ordenação com feedback visual.
- **Onde encaixar na página:** Dashboards de faturamento, painéis de gestão financeira, listagens de arquivos e áreas administrativas B2B.
- **Destaque RTL:** As colunas utilizam rigorosamente `text-left rtl:text-right`, garantindo alinhamento imediato sem desalinhamento dos números e textos em árabe.

### 2. Dual-Tone Responsive Sidebar com Submenus (`components/sidebar/SubMenu.html`)
- **Anatomia Visual:** Barra vertical de 64 a 72 unidades de largura (`w-64`), com divisão clara entre a marca/logotipo superior, uma área de busca integrada com ícone de lupa SVG, seções rotuladas (`LabelSection` com títulos em caixa alta e tracking aberto `text-xs font-semibold text-gray-400 uppercase`) e links de navegação com cantos arredondados (`rounded-lg`). No rodapé, um cartão de perfil de usuário com avatar e e-mail.
- **Gatilho de Interação:** Hover nos itens com `hover:bg-gray-100 dark:hover:bg-gray-700`, transição de cor suave em 300ms e colapsamento dinâmico em telas mobile através de alternância de visibilidade.
- **Onde encaixar na página:** Layout mestre de aplicações web autenticadas (SaaS Shell).

### 3. Directional Icon Pagination com Inversão RTL (`components/pagination/Icons.html`)
- **Anatomia Visual:** Uma barra horizontal de páginas contendo botões para "Previous" e "Next" com ícones vetoriais de seta e botões numéricos com destaque na página ativa (`bg-blue-500 text-white` vs `bg-white dark:bg-gray-800 text-gray-700 dark:text-gray-200`).
- **Gatilho de Interação:** Hover com efeito de elevação cromática (`hover:bg-blue-500 hover:text-white transition-colors duration-300 transform`) e cursor de bloqueio (`cursor-not-allowed`) no estado desabilitado.
- **Onde encaixar na página:** Rodapé de tabelas, catálogos de e-commerce e listagens de artigos de blog.
- **Destaque RTL (A Assinatura Técnica):** Os ícones de seta contêm a classe mágica `rtl:-scale-x-100`. Em leitura LTR, a seta de anterior aponta para a esquerda; quando o documento muda para `dir="rtl"`, a mesma seta inverte horizontalmente em 180° pelo CSS do Tailwind sem necessidade de trocar o SVG ou criar lógicas de renderização condicional.

### 4. Pop & Full-Width Alert Cards com Lateral Accent Bar (`components/alerts/NotificationPop.html`)
- **Anatomia Visual:** Container flutuante ou full-width com cantos arredondados (`rounded-lg shadow-md bg-white dark:bg-gray-800`). Na extremidade lateral oposta ao texto, uma coluna de acento visual com largura fixa (`w-2 bg-gray-800 dark:bg-gray-900` para notificações neutras; `w-2 bg-emerald-500` para sucesso; `w-2 bg-amber-500` para alerta; `w-2 bg-red-500` para erro). Conteúdo interno com avatar de 40px ou ícone de status e texto descritivo com link de ação.
- **Gatilho de Interação:** Entrada via animação de transição, hover no link com sublinhado (`hover:underline`) e botão de fechar (`dismiss`).
- **Onde encaixar na página:** Toast notifications no canto superior/inferior direito, alertas de sistema no topo da viewport ou mensagens de validação em formulários.

### 5. Alpine Transition Dialog / Modal de Confirmação (`components/modals/Confirm.html`)
- **Anatomia Visual:** Camada de sobreposição (*backdrop*) fixa cobrindo toda a janela (`fixed inset-0 z-10 overflow-y-auto bg-black/50`). Caixa de diálogo centralizada contendo imagem ilustrativa no topo, título semântico (`text-lg font-medium text-gray-800 dark:text-white`), corpo de texto explicativo, campo de link rápido com botão de cópia com ícone de prancheta e duas ações claras na base (Cancelar e Confirmar).
- **Gatilho de Interação:** Clique no botão de gatilho ativa `isOpen = true`; clique fora da caixa ou no botão de cancelamento ativa `isOpen = false`.
- **Física de Transição:** 
  - Entrada: `transition duration-300 ease-out` com `translate-y-4 opacity-0 sm:translate-y-0 sm:scale-95` expandindo para `translate-y-0 opacity-100 sm:scale-100`.
  - Saída: `transition duration-150 ease-in` revertendo o estado de escala e opacidade.
- **Onde encaixar na página:** Confirmações destrutivas (excluir conta), compartilhamento de links, fluxo de publicação e formulários multi-step.

### 6. Origin-Anchored Animated Dropdown Menu (`components/dropdowns/Simple.html`)
- **Anatomia Visual:** Gatilho com botão quadrado ou circular com ícone chevron ou três pontos, seguido por menu suspenso flutuante de largura definida (`w-48 py-2 mt-2`) posicionado absolutamente com ancoragem superior direita (`origin-top-right absolute right-0 z-20 bg-white rounded-md shadow-xl dark:bg-gray-800`). Itens de menu com espaçamento generoso (`px-4 py-3 text-sm`) e separadores semânticos opcionais.
- **Gatilho de Interação:** Clique no botão alterna visibilidade (`@click="isOpen = !isOpen"`), e clique fora fecha automaticamente via diretiva nativa `@click.away="isOpen = false"`.
- **Onde encaixar na página:** Menus de usuário no topo da Navbar, menus de opções em linhas de tabelas e filtros rápidos.

### 7. App Store & Google Play Action CTA Showcase (`components/cta/Image.html`)
- **Anatomia Visual:** Seção de Call to Action em grid/flexbox responsivo com duas metades: à esquerda, imagem de alta resolução emoldurada com cantos totalmente arredondados (`rounded-full h-80 w-80 sm:w-[28rem] sm:h-[28rem] object-cover`); à direita, título com tracking refinado (`tracking-tight text-gray-800 xl:text-3xl dark:text-white`), texto persuasivo e grupo de botões de conversão estilizados para a Apple App Store e Google Play Store com SVGs vetoriais dos logos oficiais.
- **Gatilho de Interação:** Hover com escurecimento suave (`hover:bg-gray-700 transition-colors duration-300`) e foco com anel translúcido (`focus:ring focus:ring-gray-300 focus:ring-opacity-80`).
- **Onde encaixar na página:** Seção de encerramento antes do rodapé em landing pages institucionais e páginas promocionais de aplicativos móveis.

### 8. Responsive Multi-Tier Pricing Matrix (`components/pricing`)
- **Anatomia Visual:** Grade com 3 a 4 colunas de precificação (`grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4`). O plano intermediário (popular/pro) recebe destaque visual com borda colorida (`border-blue-500 dark:border-blue-400`), badge de recomendação ("Most Popular") e botão de chamada com cor primária sólida contra botões secundários com contorno nos outros planos.
- **Gatilho de Interação:** Alternância entre faturamento mensal e anual (*toggle switch*) e hover com ligeira elevação dos cartões.
- **Onde encaixar na página:** Seção central de páginas de conversão de planos SaaS e e-commerce de assinaturas.

### 9. Dual-Layout Responsive Navbar com Mobile Hamburger (`components/navbars/Simple.html` & `Search.html`)
- **Anatomia Visual:** Barra superior de navegação com fundo `bg-white dark:bg-gray-800 shadow`, flexbox horizontal com logotipo à esquerda, links centrais com borda inferior ativa (`border-b-2 border-blue-500` vs `border-b-2 border-transparent hover:border-blue-500`) e ícones de perfil/ações à direita. Em dispositivos móveis, um botão hambúrguer revela uma gaveta vertical expansível sem travar a rolagem.
- **Gatilho de Interação:** Transição de cor em 300ms nos links de navegação (`transition-colors duration-300 transform`) e animação suave de abertura do menu mobile.
- **Onde encaixar na página:** Cabeçalho global fixo ou flutuante de qualquer aplicação web.

### 10. Cookie & Privacy Floating Banner (`components/cookies`)
- **Anatomia Visual:** Caixa flutuante fixada na parte inferior da tela (`fixed bottom-0 start-0 z-50 m-4 max-w-md bg-white rounded-lg shadow-xl dark:bg-gray-800 border border-gray-200 dark:border-gray-700 p-6`). Contém ícone temático de cookie ou cadeado de privacidade, explicação concisa sobre a LGPD/GDPR e botões horizontais estilizados para "Accept All" e "Preferences/Decline".
- **Gatilho de Interação:** Clique em aceitar ou recusar despacha o evento e executa a transição de saída do container via Alpine.js ou CSS transition.
- **Onde encaixar na página:** Camada global de consentimento de privacidade exibida na primeira visita do usuário.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

O Meraki UI não requer instalação via gerenciador de pacotes para seus estilos; ele depende unicamente da presença do **Tailwind CSS** (v3 ou v4) devidamente configurado e, opcionalmente, do **Alpine.js** para interatividade de tela sem React.

#### 1. Configuração do Tailwind CSS (`tailwind.config.js`):
Para habilitar todas as capacidades do Meraki UI (em especial o Dark Mode por classe e os modificadores de RTL), configure o arquivo de tema:

```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./src/**/*.{html,js,jsx,ts,tsx,vue,blade.php}",
    "./components/**/*.{html,js,blade.php}",
  ],
  darkMode: 'class', // Essencial para alternância dinâmica via classe no <html>
  theme: {
    extend: {
      colors: {
        // Paleta semântica primária recomendada pelo Meraki UI
        brand: {
          50: '#eff6ff',
          100: '#dbeafe',
          500: '#3b82f6',
          600: '#2563eb',
          700: '#1d4ed8',
        }
      }
    },
  },
  plugins: [
    require('@tailwindcss/forms'),      // Normalização refinada de formulários
    require('@tailwindcss/typography'), // Tipografia de artigos e posts
  ],
}
```

#### 2. Configuração do Suporte a RTL (Direção de Leitura):
No HTML raiz ou no wrapper da aplicação, declare dinamicamente a direção:

```html
<!-- Para idiomas ocidentais (Inglês, Português, Espanhol) -->
<html lang="pt-BR" dir="ltr" class="dark">

<!-- Para idiomas orientais (Árabe, Hebraico, Farsi, Urdu) -->
<html lang="ar" dir="rtl" class="dark">
```

O Tailwind CSS reconhece nativamente os modificadores `rtl:` e `ltr:`. O Meraki UI faz uso intensivo desses seletores para inversões pontuais.

#### 3. Inclusão do Alpine.js:
Se estiver trabalhando em projetos sem framework JavaScript pesado (HTML puro, Laravel, Django, Rails):

```html
<!-- Inclusão via CDN com defer (aproximadamente ~10kB gzipped) -->
<script src="//unpkg.com/alpinejs" defer></script>
```

---

### Física de Movimento e Curvas de Transição

O Meraki UI utiliza transições CSS puras aceleradas por hardware (GPU) via propriedades `transform`, `opacity` e `color`. A temporização dos componentes obedece a um ritmo estrito:

- **Entrada de Diálogos e Modais:**
  - Curva: `ease-out` — `cubic-bezier(0, 0, 0.2, 1)`
  - Duração: `300ms`
  - Variação espacial: `translate-y-4` para `translate-y-0`, combinado com escala de `scale-95` para `scale-100` e opacidade de `0` para `100`.
- **Saída de Diálogos e Menus:**
  - Curva: `ease-in` — `cubic-bezier(0.4, 0, 1, 1)`
  - Duração: `150ms` a `100ms` (saídas devem ser o dobro da velocidade das entradas para conferir sensação de agilidade e resposta instantânea).
- **Hover de Links e Botões:**
  - Duração: `300ms`
  - Classes: `transition-colors duration-300 transform`

#### Equivalente em Spring Physics (Framer Motion / React 19):
Para equipes que desejam portar a física do Meraki UI para React com Framer Motion:

```typescript
export const merakiModalSpring = {
  type: "spring",
  stiffness: 320,
  damping: 28,
  mass: 0.85,
};

export const merakiDropdownTransition = {
  type: "tween",
  duration: 0.15,
  ease: [0, 0, 0.2, 1],
};
```

---

### Receitas de Código Funcionais

#### Receita 1: Padrão Oficial Meraki UI (HTML5 + Tailwind CSS + Alpine.js com Suporte Completo a RTL e Dark Mode)

Este exemplo implementa um componente completo de **Dropdown com Menu de Usuário, Alerta com Barra Lateral e Paginação com Inversão RTL**:

```html
<!DOCTYPE html>
<html lang="ar" dir="rtl" class="dark">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Meraki UI Pattern Showcase</title>
  <!-- Tailwind CSS CDN (para testes rápidos) -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      darkMode: 'class',
    }
  </script>
  <!-- Alpine.js -->
  <script src="//unpkg.com/alpinejs" defer></script>
</head>
<body class="bg-gray-100 dark:bg-gray-900 min-h-screen p-8 text-gray-800 dark:text-gray-100 flex flex-col gap-8 items-center">

  <!-- 1. POP ALERT COM BARRA LATERAL COLORIDA DE ACENTO -->
  <div class="flex w-full max-w-md overflow-hidden bg-white rounded-lg shadow-md dark:bg-gray-800 border border-gray-200 dark:border-gray-700">
    <!-- Barra vertical de acento semântico -->
    <div class="w-2 bg-blue-600 dark:bg-blue-500"></div>

    <div class="flex items-center px-4 py-3">
      <img class="object-cover w-10 h-10 rounded-full flex-shrink-0" alt="Avatar do usuário" src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&auto=format&fit=crop&w=128&q=80">

      <div class="mx-3 text-sm">
        <p class="text-gray-600 dark:text-gray-300">
          <span class="font-semibold text-gray-800 dark:text-white">Fatima Al-Mansoor</span> adicionou um novo relatório ao projeto.
        </p>
        <span class="text-xs text-blue-500 dark:text-blue-400 hover:underline cursor-pointer">Ver documento</span>
      </div>
    </div>
  </div>

  <!-- 2. DROPDOWN ANIMADO COM ANCORAGEM ORIGIN E CLICK-AWAY -->
  <div x-data="{ isOpen: false }" class="relative inline-block">
    <!-- Botão Gatilho -->
    <button 
      @click="isOpen = !isOpen" 
      class="flex items-center gap-x-2 px-4 py-2 text-sm font-medium text-gray-700 bg-white border border-gray-200 rounded-md dark:bg-gray-800 dark:text-gray-200 dark:border-gray-700 hover:bg-gray-50 dark:hover:bg-gray-700 focus:outline-none focus:ring focus:ring-blue-300 focus:ring-opacity-40 transition-colors duration-300"
      aria-haspopup="true"
      :aria-expanded="isOpen"
    >
      <span>Minha Conta</span>
      <svg class="w-4 h-4 text-gray-500 transition-transform duration-200" :class="{ 'rotate-180': isOpen }" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
        <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
      </svg>
    </button>

    <!-- Menu Suspenso -->
    <div 
      x-show="isOpen" 
      @click.away="isOpen = false"
      x-transition:enter="transition ease-out duration-150"
      x-transition:enter-start="opacity-0 scale-95"
      x-transition:enter-end="opacity-100 scale-100"
      x-transition:leave="transition ease-in duration-100"
      x-transition:leave-start="opacity-100 scale-100"
      x-transition:leave-end="opacity-0 scale-95" 
      class="absolute right-0 rtl:right-auto rtl:left-0 z-20 w-56 py-2 mt-2 origin-top-right rtl:origin-top-left bg-white rounded-md shadow-xl dark:bg-gray-800 border border-gray-200 dark:border-gray-700"
      style="display: none;"
    >
      <div class="px-4 py-2 border-b border-gray-100 dark:border-gray-700">
        <p class="text-xs text-gray-400">Conectado como</p>
        <p class="text-sm font-semibold text-gray-800 dark:text-white truncate">tariq@empresa.com</p>
      </div>

      <a href="#" class="block px-4 py-2.5 text-sm text-gray-600 capitalize transition-colors duration-200 dark:text-gray-300 hover:bg-gray-100 dark:hover:bg-gray-700 dark:hover:text-white">Perfil</a>
      <a href="#" class="block px-4 py-2.5 text-sm text-gray-600 capitalize transition-colors duration-200 dark:text-gray-300 hover:bg-gray-100 dark:hover:bg-gray-700 dark:hover:text-white">Configurações</a>
      
      <div class="border-t border-gray-100 dark:border-gray-700 my-1"></div>
      
      <a href="#" class="block px-4 py-2.5 text-sm text-red-600 capitalize transition-colors duration-200 dark:text-red-400 hover:bg-red-50 dark:hover:bg-red-900/20">Encerrar Sessão</a>
    </div>
  </div>

  <!-- 3. PAGINAÇÃO COM INVERSÃO AUTOMÁTICA DE ÍCONES EM RTL (rtl:-scale-x-100) -->
  <nav class="flex items-center space-x-1 rtl:space-x-reverse" aria-label="Paginação">
    <!-- Botão Anterior -->
    <a href="#" class="px-4 py-2 text-gray-500 capitalize bg-white rounded-md cursor-not-allowed dark:bg-gray-800 dark:text-gray-500 border border-gray-200 dark:border-gray-700">
      <div class="flex items-center">
        <!-- Ícone que inverte automaticamente quando em RTL -->
        <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 mx-1 rtl:-scale-x-100" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16l-4-4m0 0l4-4m-4 4h18" />
        </svg>
        <span class="mx-1 text-sm font-medium">Anterior</span>
      </div>
    </a>

    <!-- Páginas -->
    <a href="#" class="px-4 py-2 text-sm font-medium text-white transition-colors duration-300 transform bg-blue-600 rounded-md">1</a>
    <a href="#" class="px-4 py-2 text-sm font-medium text-gray-700 transition-colors duration-300 transform bg-white rounded-md dark:bg-gray-800 dark:text-gray-200 hover:bg-blue-600 hover:text-white dark:hover:bg-blue-600 border border-gray-200 dark:border-gray-700">2</a>
    <a href="#" class="px-4 py-2 text-sm font-medium text-gray-700 transition-colors duration-300 transform bg-white rounded-md dark:bg-gray-800 dark:text-gray-200 hover:bg-blue-600 hover:text-white dark:hover:bg-blue-600 border border-gray-200 dark:border-gray-700">3</a>

    <!-- Botão Próximo -->
    <a href="#" class="px-4 py-2 text-gray-700 capitalize bg-white rounded-md dark:bg-gray-800 dark:text-gray-200 hover:bg-blue-600 hover:text-white dark:hover:bg-blue-600 border border-gray-200 dark:border-gray-700 transition-colors duration-300">
      <div class="flex items-center">
        <span class="mx-1 text-sm font-medium">Próximo</span>
        <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 mx-1 rtl:-scale-x-100" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
        </svg>
      </div>
    </a>
  </nav>

</body>
</html>
```

---

#### Receita 2: Versão Portada para React 19 / Next.js (TypeScript + Tailwind CSS + Framer Motion)

Para desenvolvedores que desejam a estética, as proporções e o comportamento bi-direcional do Meraki UI em projetos React corporativos sem carregar o runtime do Alpine.js:

```tsx
"use client";

import React, { useState, useRef, useEffect } from "react";
import { motion, AnimatePresence } from "framer-motion";

interface MerakiConfirmModalProps {
  isOpen: boolean;
  onClose: () => void;
  onConfirm: () => void;
  title: string;
  description: string;
  confirmLabel?: string;
  cancelLabel?: string;
  imageUrl?: string;
}

export const MerakiConfirmModal: React.FC<MerakiConfirmModalProps> = ({
  isOpen,
  onClose,
  onConfirm,
  title,
  description,
  confirmLabel = "Confirmar",
  cancelLabel = "Cancelar",
  imageUrl,
}) => {
  const modalRef = useRef<HTMLDivElement>(null);

  // Fecha o modal ao pressionar tecla Escape
  useEffect(() => {
    const handleKeyDown = (e: KeyboardEvent) => {
      if (e.key === "Escape") onClose();
    };
    if (isOpen) {
      window.addEventListener("keydown", handleKeyDown);
    }
    return () => window.removeEventListener("keydown", handleKeyDown);
  }, [isOpen, onClose]);

  return (
    <AnimatePresence>
      {isOpen && (
        <div
          className="fixed inset-0 z-50 overflow-y-auto"
          role="dialog"
          aria-modal="true"
          aria-labelledby="modal-headline"
        >
          {/* Backdrop escuro com transição de opacidade */}
          <motion.div
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            exit={{ opacity: 0 }}
            transition={{ duration: 0.2 }}
            onClick={onClose}
            className="fixed inset-0 bg-black/60 backdrop-blur-sm"
          />

          {/* Wrapper flexível para centralização vertical */}
          <div className="flex items-end justify-center min-h-screen px-4 pt-4 pb-20 text-center sm:block sm:p-0">
            {/* Truque do zero-width space para alinhamento vertical exato */}
            <span
              className="hidden sm:inline-block sm:align-middle sm:h-screen"
              aria-hidden="true"
            >
              &#8203;
            </span>

            {/* Caixa de Diálogo do Modal (Física Meraki UI) */}
            <motion.div
              ref={modalRef}
              initial={{ opacity: 0, scale: 0.95, y: 16 }}
              animate={{ opacity: 1, scale: 1, y: 0 }}
              exit={{ opacity: 0, scale: 0.95, y: 16 }}
              transition={{
                type: "spring",
                stiffness: 350,
                damping: 25,
                mass: 0.8,
              }}
              className="relative inline-block w-full max-w-sm p-6 my-8 overflow-hidden text-left rtl:text-right align-middle transition-all bg-white rounded-xl shadow-2xl dark:bg-gray-900 border border-gray-200 dark:border-gray-800 sm:max-w-md"
            >
              {imageUrl && (
                <div className="flex items-center justify-center mx-auto mb-4">
                  <img
                    className="object-cover w-full h-44 rounded-lg"
                    src={imageUrl}
                    alt="Ilustração do modal"
                  />
                </div>
              )}

              <div className="text-center sm:text-start">
                <h3
                  className="text-lg font-semibold text-gray-800 dark:text-white"
                  id="modal-headline"
                >
                  {title}
                </h3>

                <p className="mt-2 text-sm text-gray-500 dark:text-gray-400 leading-relaxed">
                  {description}
                </p>
              </div>

              {/* Botões de Ação com suporte a RTL e Focus Ring atenuado */}
              <div className="mt-6 flex flex-col sm:flex-row sm:justify-end gap-3">
                <button
                  type="button"
                  onClick={onClose}
                  className="w-full sm:w-auto px-4 py-2.5 text-sm font-medium text-gray-700 capitalize transition-colors duration-300 transform bg-white border border-gray-200 rounded-md dark:bg-gray-800 dark:text-gray-200 dark:border-gray-700 hover:bg-gray-100 dark:hover:bg-gray-700 focus:outline-none focus:ring focus:ring-gray-300 focus:ring-opacity-40"
                >
                  {cancelLabel}
                </button>

                <button
                  type="button"
                  onClick={onConfirm}
                  className="w-full sm:w-auto px-4 py-2.5 text-sm font-medium text-white capitalize transition-colors duration-300 transform bg-blue-600 rounded-md hover:bg-blue-500 focus:outline-none focus:ring focus:ring-blue-300 focus:ring-opacity-40"
                >
                  {confirmLabel}
                </button>
              </div>
            </motion.div>
          </div>
        </div>
      )}
    </AnimatePresence>
  );
};
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar o **Meraki UI** como referência arquitetural ou catálogo de componentes dentro do `DESIGN_BLUEPRINT.md`, a inteligência artificial arquiteta deve seguir as seguintes diretrizes normativas:

### 1. Declaração Formal da Stack e Regras de Internacionalização (i18n)
- **Token de Direção Bi-direcional:** É mandatório estabelecer no blueprint que todo componente estrutural deve suportar a alternância entre `dir="ltr"` e `dir="rtl"`.
- **Regra de Classes Utilitárias:** Nunca utilizar propriedades direcionais absolutas (`pl-*`, `pr-*`, `ml-*`, `mr-*`, `left-*`, `right-*`) sem a contraparte correspondente do modificador `rtl:`, ou preferir sempre as classes lógicas do Tailwind v3.3+ (`ps-*`, `pe-*`, `ms-*`, `me-*`, `start-*`, `end-*`).
- **Inversão de Iconografia Vetorial:** Todo elemento SVG com sentido de leitura ou fluxo temporal (anterior/próximo, voltar/avançar, setas de paginação) deve conter a classe `rtl:-scale-x-100`.

### 2. Padrão de Superfícies para Dark Mode
- Evitar preto absoluto (`#000000`). Utilizar a escala neutra do Meraki UI:
  - Fundo geral: `bg-gray-100 dark:bg-gray-900`
  - Painéis, tabelas e cards: `bg-white dark:bg-gray-800`
  - Divisores e bordas: `border-gray-200 dark:border-gray-700`
  - Textos principais: `text-gray-800 dark:text-white`
  - Textos secundários: `text-gray-500 dark:text-gray-400`

### 3. Regra de Separação de Runtime (Alpine.js vs React)
- Se o projeto for arquitetado em **Laravel Blade, Django, Rails ou Astro Estático**, adote o padrão original do Meraki UI com **Alpine.js** (`x-data`, `x-show`, `x-transition`), garantindo interatividade com zero build overhead.
- Se o projeto for em **Next.js, Remix, Vite React ou Vue 3**, instrua a IA a **eliminar as diretivas do Alpine.js** e substituir os estados e transições por hooks reativos padrão (`useState`, `useTransition`) ou Framer Motion, preservando 100% da anatomia das classes Tailwind.

### 4. Gestão de Acessibilidade e Foco
- Todos os botões, links de ação e inputs de formulário devem conter a assinatura de anel de foco calibrado:
  `focus:outline-none focus:ring focus:ring-blue-300 focus:ring-opacity-40 dark:focus:ring-blue-400 dark:focus:ring-opacity-40`.

---
*Dossiê compilado e calibrado com rigor técnico para o repositório de Design Systems e Engenharia de UI/UX.*
