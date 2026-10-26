---
id: "050-mambaui"
name: "Mamba UI"
url: "https://www.mambaui.com/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Modern Tailwind Utility", "Zero-Dependency Modular UI", "Multi-Syntax Markup (HTML/Vue/JSX)", "Dynamic Color Theming", "Responsive Clean Editorial"]
densidade_informacao: "Media"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS/Headless)"
stack_frameworks: ["Tailwind CSS v3 / v4", "HTML5 Semântico", "React 18 / 19 (JSX/TSX)", "Vue.js 3 / 2", "Next.js (App Router)", "Vite"]
compatibilidade:
  fontes_ideais: ["Inter", "Plus Jakarta Sans", "Outfit", "Public Sans", "Roboto"]
  paletas_ideais: ["Tailwind 17-Palette Spectrum (Violet, Sky, Emerald, Amber, Rose)", "Neutral Slate Dark Mode (`dark:bg-gray-900` / `dark:text-gray-100`)", "High-Legibility Modern Contrast"]
  combinacoes_recomendadas: ["shadcn/ui (para estados interativos complexos e acessibilidade WAI-ARIA)", "Lucide React (para extensão de iconografia vetorial)", "Framer Motion (para elevação de micro-interações)", "@tailwindcss/typography", "@tailwindcss/forms"]
  conflitos_esteticos: ["Neo-brutalismo cru com bordas pretas de 4px e sombras duras deslocadas", "Interfaces 3D WebGL / Canvas pesadas", "Skeuomorfismo excessivo ou Neumorfismo difuso"]
---

# Mamba UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Mamba UI**, concebido e mantido pelo desenvolvedor e arquiteto de software **Mirko Nowak** (sob a organização open-source **Microwawe**), estabeleceu-se como uma das mais eficientes e acessíveis bibliotecas de componentes e blocos de página modulares construídos inteiramente sobre o **Tailwind CSS**. 

Distribuído sob licença MIT livre, o projeto reúne mais de **150 componentes e templates responsivos completos** projetados sob uma premissa fundamental de engenharia de software: **Zero Overhead de Runtime, Zero Dependências Externas Obrigatórias e Portabilidade Universal de Código**.

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    FILOSOFIA ARQUITETURAL DO MAMBA UI                       │
├───────────────────┬─────────────────────────────────────────────────────────┤
│ 1. Zero-Runtime   │ Sem arquivos JS pesados empacotados no bundle inicial.  │
│                   │ 100% dependente do motor CSS utilitário do Tailwind.   │
├───────────────────┼─────────────────────────────────────────────────────────┤
│ 2. Tri-Syntax     │ Exportação nativa instantânea com 1 clique para:        │
│    Engine         │ HTML5 puro, React / Next.js (JSX) e Vue.js (Templates). │
├───────────────────┼─────────────────────────────────────────────────────────┤
│ 3. 17-Color Grid  │ Customização cromática in-browser em tempo real sobre   │
│    Matrix         │ as 17 paletas oficiais do Tailwind CSS.                 │
├───────────────────┼─────────────────────────────────────────────────────────┤
│ 4. Native Dark    │ Dual-theming estruturado via classes atômicas           │
│    Parity         │ (`dark:bg-gray-900`, `dark:text-gray-100`, etc.).      │
└───────────────────┴─────────────────────────────────────────────────────────┘
```

---

### 1.1. O Manifesto "Zero-Runtime & Pure Utility"
Ao contrário dos ecossistemas modernos baseados em empacotamentos NPM complexos (`npm install @heavy-ui/core`) que injetam megabytes de JavaScript, wrappers de elementos invisíveis e estilos CSS-in-JS em tempo de execução, o Mamba UI baseia-se no princípio clássico do **Copy-Paste Arquitetural**:
- **Nenhum nó artificial no DOM**: A marcação reflete exatamente a semântica do HTML5 (`<header>`, `<main>`, `<article>`, `<section>`, `<aside>`, `<footer>`).
- **Resolução Estática**: Todo o design é resolvido pelo compilador do Tailwind CSS em tempo de build (`JIT - Just-In-Time Engine`), resultando em arquivos CSS finais ultra-otimizados e minificados, frequentemente inferiores a 25 KB gzipped.
- **Transparência de Código**: O desenvolvedor retém 100% de controle sobre o markup. Não há componentes "caixa-preta" nem abstrações fechadas de design token que impeçam alterações pontuais de padding, border-radius ou espaçamento flex.

---

### 1.2. O Mecanismo de Tematização Cromática Dinâmica (The 17-Color Matrix)
Uma das assinaturas mais notáveis da experiência Mamba UI em seu portal oficial (`mambaui.com`) é a barra de ferramentas superior de customização ao vivo:
- O sistema permite ao desenvolvedor alternar a **Cor Primária** entre 17 escalas de cores nativas do Tailwind CSS: `Slate`, `Gray`, `Zinc`, `Neutral`, `Stone`, `Red`, `Orange`, `Amber`, `Yellow`, `Lime`, `Green`, `Emerald`, `Teal`, `Cyan`, `Sky`, `Blue`, `Indigo`, `Violet`, `Purple`, `Fuchsia`, `Pink`, `Rose`.
- Quando uma cor é selecionada (ex: `Violet`), todos os mais de 150 blocos da página têm suas classes de destaque remapeadas instantaneamente:
  - Planos de fundo primários: `bg-violet-600` / `hover:bg-violet-700`.
  - Bordas de foco e anéis: `border-violet-600`, `focus:ring-violet-600`.
  - Realces tipográficos: `text-violet-600` / `dark:text-violet-400`.
  - Marcadores de progresso e ícones: `fill-violet-600`, `stroke-violet-600`.
- Essa lógica permite aos desenvolvedores visualizarem imediatamente como os templates irão se integrar à identidade visual de sua marca antes mesmo de copiar a marcação para o editor de código.

---

### 1.3. O Triplo Exportador de Sintaxe (HTML5, React JSX e Vue)
O Mamba UI resolve uma das maiores fricções no desenvolvimento multiplataforma: a tradução manual de atributos HTML para sintaxes de frameworks reativos. A interface provê alternância em tempo real com sanitização automática:
1. **HTML5 Semântico**: Utiliza `class="..."`, atributos padrão de acessibilidade (`aria-*`, `for="..."`) e elementos auto-fecháveis tradicionais (`<input>`, `<img>`, `<hr>`).
2. **React (JSX / TSX)**: Converte automaticamente `class` para `className`, `for` para `htmlFor`, converte atributos de SVG de kebab-case para camelCase (`stroke-width` ➔ `strokeWidth`, `stroke-linecap` ➔ `strokeLinecap`, `fill-rule` ➔ `fillRule`) e assegura o fechamento rigoroso de todas as tags vazias (`<input />`, `<img />`, `<br />`).
3. **Vue.js**: Gera templates compatíveis com Vue 2 e Vue 3, mantendo a diretiva `class="..."` nativa e estruturando seções prontas para receberem bindings reativos (`:class`, `v-for`, `@click`).

---

### 1.4. Sensação Tátil, Acabamento e Ritmo Visual
A estética do Mamba UI é caracterizada pela sobriedade e legibilidade moderna:
- **Curvatura e Raios de Borda**: Predominância de `rounded-md` (6px) para botões e inputs de formulário, e `rounded-lg` (8px) a `rounded-xl` (12px) para cartões de conteúdo e containers de seção. Evita cantos circulares extremos (`rounded-full`) exceto para avatares, tags de status pill e botões de ação flutuantes.
- **Profundidade e Sombreamento**: Uso econômico de sombras. Privilegia bordas de 1px (`border border-gray-200 dark:border-gray-800`) com fundos sólidos ou sombras muito suaves (`shadow-sm`, `shadow-md`), evitando elevações exageradas que poluem a hierarquia de leitura.
- **Ilustrações e Ícones em SVG Inline**: Todos os ícones de setas, checkmarks, estrelas e ilustrações temáticas são codificados como SVGs puros e inline nas classes do Tailwind (`h-5 w-5 fill-current text-violet-600`), garantindo nitidez vetorial imediata sem necessidade de requisições de rede ou dependência de pacotes adicionais.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados
1. **Landing Pages de Lançamento & MVPs Rápidos (Go-To-Market em Horas)**:
   Projetos que precisam validar propostas de valor rapidamente. Com os blocos de Hero, Features, Social Proof e Pricing do Mamba UI, um desenvolvedor solo ou equipe ágil monta uma página institucional completa e responsiva em poucas horas sem abrir o Figma.
2. **Portais Editoriais, Blogs Corporativos e Plataformas de Notícias**:
   O Mamba UI oferece uma rica coleção de layouts de artigos, cartões com autores, grids editoriais de revistas, feeds de artigos com paginação e breadcrumbs que garantem excelente experiência de leitura.
3. **Portfólios de Desenvolvedores, Designers e Agências Digitais**:
   Templates de páginas pessoais elegantes com seções dedicadas para exibição de cases de sucesso, stacks tecnológicas, depoimentos de clientes e formulários de contato integrados.
4. **Dashboards Administrativos Iniciais e Painéis Operacionais**:
   Aplicações web que necessitam de tabelas limpas, cartões de métricas estatísticas (`Stats`), barras de progresso (`Progress`), passos de onboarding (`Steps`) e timelines operacionais sem a sobrecarga de um design system empresarial massivo.
5. **E-commerce Inicial & Catálogos de Produtos (Showcase)**:
   Vitrines comerciais leves com cards de produto, seletores de cor, avaliações em estrelas, filtros por categoria e módulos de carrinho de compras básico.

---

### O Papel no Ritmo Visual (A Aplicação da Regra 60-30-10)

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                  DISTRIBUIÇÃO ARQUITETURAL (REGRA 60-30-10)                 │
├───────────────────┬─────────────────────────────────────────────────────────┤
│ 60% — Estrutura   │ Espinha dorsal do layout: Containers `container mx-auto`│
│ (Mamba UI)        │ Heros, Grids de Features, Pricing Tables, Footers.      │
├───────────────────┼─────────────────────────────────────────────────────────┤
│ 30% — Fluidez     │ Camada de dados e interação: Formulários, Steppers,     │
│ (Mamba UI + Form) │ Timelines, Cartões de Artigo, Skeletons de Loading.     │
├───────────────────┼─────────────────────────────────────────────────────────┤
│ 10% — Protagonista│ Elementos de Alto Impacto: Micro-interações táteis via   │
│ (Framer / Magic)  │ Framer Motion, partículas, botões interativos e badges. │
└───────────────────┴─────────────────────────────────────────────────────────┘
```

- **Espinha Dorsal Estrutural (60%)**: O Mamba UI brilha como a fundação estrutural completa da página. Os espaçamentos responsivos padronizados (`py-12 sm:py-24`, `px-6 md:px-12`), grids fluidos (`grid-cols-1 md:grid-cols-2 lg:grid-cols-3`) e contrastes semânticos servem como a base sólida do produto.
- **Camada de Fluidez e Conteúdo (30%)**: Responsável pelos componentes informativos intermediários — formulários com validações nativas, tabelas zebradas, cartões de depoimentos em alvenaria (*masonry grid*) e timelines de entregas.
- **Efeito Protagonista / Showstopper (10%)**: O Mamba UI **não tenta ser uma biblioteca de efeitos visuais extravagantes** (como Aceternity ou Magic UI). Os 10% de refinamento visual e impacto máximo devem ser atingidos enriquecendo os componentes do Mamba UI com transições suaves via Framer Motion, micro-efeitos de gradiente no mouse hover ou iconografia customizada do Lucide React.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
1. **Aplicações Empresariais com Requisitos Críticos de Acessibilidade WAI-ARIA (Nível AAA)**:
   Os componentes nativos do Mamba UI são construídos predominantemente em HTML e CSS puros. Elementos de alta complexidade interativa (como *Dropdowns com navegação por setas*, *Comboboxes com busca assíncrona*, *Date Pickers*, *Modais aninhados com Focus-Trap* e *Menus de Contexto*) **não possuem a máquina de estados necessária** para conformidade acessível total. Para esses casos, utilize **shadcn/ui**, **Radix UI** ou **Base UI**.
2. **Dashboards de Alta Densidade de Dados em Tempo Real (Fintech Trading / NOC Telemetria)**:
   A densidade visual do Mamba UI é média/editorial. Ambientes de trading ou monitoramento de servidores exigem tipografia tabular ultracompacta (11px-12px), virtualização de linhas de tabela (`TanStack Virtual`) e zero margens ociosas.
3. **Experiências 3D Imersivas e Portfólios WebGL Experimentais**:
   Produtos que dependem de Canvas 3D (Three.js, React Three Fiber), shaders GLSL e física gravitacional não se beneficiam de uma biblioteca orientada a grids clássicos e seções de landing page.

---

### ⚠️ Erros Comuns de Exagero & Anti-padrões:
- **A "Salada Cromática"**: Tentar utilizar a versatilidade de 17 cores do Mamba UI alternando a cor primária a cada seção (ex: Hero em violeta, Features em esmeralda, Pricing em rosa e Footer em azul). O design system deve escolher **uma única cor de destaque (Primary Accent)** e no máximo uma secundária complementar para estados de alerta/sucesso.
- **Tentativa de Usar Accordions e Modais Sem JavaScript**: Copiar o markup de uma FAQ ou Modal do Mamba UI em um projeto Vanilla ou React estático e esperar que ele abra/feche sem implementar um manipulador de estado reativo (`useState`, `details/summary` ou script de classe `.hidden`).
- **Incompatibilidade do Dark Mode**: Esquecer de configurar a diretiva `darkMode: 'class'` no `tailwind.config.js`. Sem essa declaração, as classes `dark:*` embutidas em todos os componentes do Mamba UI não responderão à alternância de tema no elemento raiz `<html>`.
- **Textos "AI Slop" & Manutenção de Conteúdo Genérico**: Deixar os títulos e parágrafos padrão ("Lorem ipsum dolor sit amet, consectetur adipiscing elit") sem refinamento de copywriting. O visual limpo do Mamba UI ganha autoridade quando o texto é direto, conciso e orientado a benefícios claros.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

O Mamba UI oferece uma suíte balanceada cobrindo desde primitivas estruturais até blocos de página completos. A seguir, destacam-se os 12 componentes mais emblemáticos da biblioteca:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                 CATÁLOGO DE COMPONENTES CHAVE DO MAMBA UI                   │
├───────────────────────────────────┬─────────────────────────────────────────┤
│ 01. Hero com Split Content & Mídia│ 07. Team & Contributor Profile Grid     │
│ 02. Tiered Pricing Matrix         │ 08. Pulsing Skeleton Content Loaders    │
│ 03. Testimonials Grid & Quotes    │ 09. Newsletter & Lead Capture Banner    │
│ 04. Feature Bento Grid Alternado  │ 10. High-Impact Stats Counter Display   │
│ 05. Multi-Step Form Stepper       │ 11. FAQ Accordion Clean Section         │
│ 06. Interactive Vertical Timeline │ 12. Sticky Responsive Header & Navbar   │
└───────────────────────────────────┴─────────────────────────────────────────┘
```

---

### 4.1. Hero Section com Split Content & Visual Preview
- **Anatomia Visual**: Seção de duas colunas balanceadas em desktop (`lg:flex-row`). No lado esquerdo, badge pill no topo com status de lançamento, headline de alto impacto (`text-4xl sm:text-6xl font-bold tracking-tight`), parágrafo explicativo de alto contraste e dupla de botões de ação (botão primário sólido com cor de marca + botão secundário outline neutro com ícone). No lado direito, container de mídia com proporção 4:3 ou 16:9, cantos arredondados (`rounded-2xl`), borda sutil e sombra profunda (`shadow-2xl`) com gradiente de fundo que simula profundidade.
- **Gatilho de Interação**: Hover sobre os botões com leve elevação (`hover:shadow-lg transition-all duration-200`) e transição suave no botão secundário com preenchimento sutil de fundo.
- **Onde Encaixar**: Topo absoluto da Landing Page (Fold 1).

---

### 4.2. Pricing Matrix com Tier de Destaque ("Most Popular")
- **Anatomia Visual**: Grade de 3 cartões de preços (`grid-cols-1 lg:grid-cols-3 gap-8`). O cartão central (plano recomendado) apresenta elevação superior (`scale-105 shadow-xl`), borda colorida na cor primária (`border-2 border-violet-600`), badge superior absoluto com a etiqueta *"Most Popular"* ou *"Recomendado"*, tipografia de preço destacada (`text-5xl font-extrabold`) com indicação clara de frequência (`/mês` ou `/ano`), lista de recursos com ícones de checkmark verdes em SVG e botão de contratação de alta prioridade. Os cartões laterais mantêm acabamento neutro em cinza escuro/claro.
- **Gatilho de Interação**: Hover com leve transição de escala e foco do cursor; interação com toggle de faturamento (mensal vs anual).
- **Onde Encaixar**: Seção intermediária inferior da página de conversão, imediatamente antes das FAQs e do rodapé.

---

### 4.3. Testimonials Grid & Blockquote Showcase
- **Anatomia Visual**: Arranjo em grade de alvenaria (*masonry*) ou grid de 3 colunas. Cada cartão apresenta:
  - Grupo de 5 estrelas em vetor SVG com preenchimento na cor de destaque.
  - Citação em bloco (`<blockquote>`) com tipografia itálica ou semi-bold de alto conforto de leitura.
  - Rodapé do cartão com avatar circular do cliente (`w-12 h-12 rounded-full object-cover`), nome completo em fonte bold e cargo/empresa em texto muted (`text-sm text-gray-500 dark:text-gray-400`).
- **Gatilho de Interação**: Transição de elevação de borda ao passar o mouse (`hover:border-violet-500/50 transition-colors`).
- **Onde Encaixar**: Seção de Prova Social (Social Proof) posicionada após a demonstração dos recursos principais do produto.

---

### 4.4. Feature Bento Grid Alternado
- **Anatomia Visual**: Sistema modular de exibição de funcionalidades que quebra a monotonia de listas lineares. Alterna entre blocos de largura dupla (2 colunas) e cartões verticais individuais. Cada cartão inclui um ícone vetorial encapsulado em um quadrado de cantos arredondados com fundo na cor de destaque atenuada (`bg-violet-100 dark:bg-violet-900/40 text-violet-600 dark:text-violet-300`), título H3 assertivo e micro-parágrafo explicativo.
- **Gatilho de Interação**: Hover com deslocamento sutil de 2px no ícone e acentuação de borda.
- **Onde Encaixar**: Seção de Proposta de Valor / Como Funciona (Logo abaixo do Hero e da barra de logotipos de clientes).

---

### 4.5. Multi-Step Form Stepper (Progresso Sequencial)
- **Anatomia Visual**: Barra de navegação horizontal com passos numerados para fluxos de onboarding ou checkout. Cada etapa é representada por um círculo numerado:
  - *Etapa Concluída*: Preenchimento sólido na cor primária com ícone de checkmark.
  - *Etapa Ativa*: Círculo com borda dupla ou anel de destaque pulsante (`ring-4 ring-violet-500/20`) e texto em negrito.
  - *Etapa Futura*: Círculo neutro com texto em cinza atenuado.
  - Entre os círculos, barras de conexão finas que mudam de cor conforme o progresso do usuário.
- **Gatilho de Interação**: Click para retornar a passos previamente preenchidos e transição suave de estado no avanço do formulário.
- **Onde Encaixar**: Topo de telas de cadastro progressivo, fluxos de checkout ou assistentes de configuração inicial.

---

### 4.6. Interactive Vertical Timeline
- **Anatomia Visual**: Eixo vertical contínuo de 2px de espessura (`bg-gray-200 dark:bg-gray-700`) com pontos nodais circulares ancorando cartões de eventos alternados à esquerda e à direita em telas grandes (ou alinhados à direita do eixo em mobile). Cada evento exibe uma tag de data/hora destacada, título do marco de entrega, descrição técnica e badges de tecnologias envolvidas.
- **Gatilho de Interação**: Scroll reveal ou acentuação de cor do nó circular ao focar no evento.
- **Onde Encaixar**: Páginas de Roadmap de Produto, Histórico da Empresa / Sobre Nós ou Linha do Tempo de Carreiras.

---

### 4.7. Team & Contributor Profile Grid
- **Anatomia Visual**: Grade de cartões de membros de equipe (`grid-cols-1 sm:grid-cols-2 md:grid-cols-4`). Cartão com imagem de perfil em alta definição com enquadramento quadrado ou circular, tratamento em escala de cinza com retorno a cores no hover (`grayscale hover:grayscale-0 transition-all duration-300`), nome, especialidade técnica e conjunto de links para GitHub, LinkedIn e X (Twitter) com ícones vetoriais padronizados.
- **Gatilho de Interação**: Hover na foto ativa a saturação de cor e destaca os ícones sociais com a cor primária.
- **Onde Encaixar**: Seção "Quem Somos" / Equipe ou Comunidade de Contribuidores Open-Source.

---

### 4.8. Pulsing Skeleton Content Loaders
- **Anatomia Visual**: Conjunto de formas geométricas neutras cinzas (`bg-gray-300 dark:bg-gray-700`) com a classe utilitária de pulso contínuo do Tailwind (`animate-pulse`). O Mamba UI oferece templates pré-montados de skeletons para:
  - Cartão de Artigo (Bloco de imagem superior + linha de título longa + duas linhas curtas de parágrafo).
  - Linha de Tabela de Dados (Avatar circular + 3 blocos retangulares de largura variável).
  - Feed de Comentários / Usuário (Círculo de 40px + duas barras horizontais).
- **Gatilho de Interação**: Auto-play contínuo enquanto dados assíncronos (`fetch` / SWR / TanStack Query) estão pendentes.
- **Onde Encaixar**: Estados de carregamento de páginas dinâmicas, dashboards e feeds de blog.

---

### 4.9. Newsletter & Lead Capture Banner
- **Anatomia Visual**: Banner de largura total ou cartão flutuante em container com fundo escuro de alto contraste (`bg-gray-900 text-white`) ou gradiente suave. Contém chamada urgente para inscrição, texto de privacidade em microtipografia ("Sem spam. Cancele quando quiser.") e um formulário inline flexível: campo de entrada com cantos arredondados à esquerda e botão de submissão colado à direita ou adjacente.
- **Gatilho de Interação**: Foco no campo de input com realce do anel de seleção (`focus:ring-2 focus:ring-violet-500`) e clique no botão com feedback de carregamento.
- **Onde Encaixar**: Fim de artigos de blog ou imediatamente acima do rodapé da página inicial.

---

### 4.10. High-Impact Stats Counter Display
- **Anatomia Visual**: Faixa horizontal com 3 a 4 colunas de métricas-chave de produto. Números em escala monumental (`text-4xl md:text-5xl font-black text-violet-600 dark:text-violet-400`), acompanhados por rótulos descritivos de alta clareza em caixa-alta atenuada (`text-xs font-semibold tracking-wider uppercase text-gray-500`).
- **Gatilho de Interação**: Animação de contagem numérica ao entrar na viewport (quando pareado com micro-hooks de contagem).
- **Onde Encaixar**: Logo abaixo da Hero Section para validação imediata de escala (ex: "10M+ requisições diárias", "99.99% uptime", "150+ componentes").

---

### 4.11. FAQ Accordion Clean Section
- **Anatomia Visual**: Lista vertical de perguntas frequentes com divisores sutis de 1px (`divide-y divide-gray-200 dark:divide-gray-800`). Cada item contém uma pergunta em texto semi-bold de 18px, um ícone de chevron indicador de abertura à direita e uma área de resposta com espaçamento confortável e contraste suave.
- **Gatilho de Interação**: Click no cabeçalho da pergunta expande/recolhe o conteúdo com rotação do chevron em 180 graus (`transform transition-transform duration-200`).
- **Onde Encaixar**: Seção final de páginas de vendas para sanar dúvidas de faturamento, segurança e implantação.

---

### 4.12. Sticky Responsive Header & Navbar
- **Anatomia Visual**: Barra superior fixa com suporte a transparência e desfoque (`sticky top-0 z-50 backdrop-blur-md bg-white/80 dark:bg-gray-900/80 border-b border-gray-100 dark:border-gray-800`). Apresenta logotipo institucional à esquerda, links de navegação centralizados com micro-hover sutil e agrupamento de ações à direita (botão de alternância de Dark Mode, botão de Sign In e botão de CTA principal). No mobile, ícone de menu hambúrguer que aciona menu colapsável.
- **Gatilho de Interação**: Transição suave de fundo ao rolar a página; hover nos links com sublinhado ou mudança de cor; clique no menu mobile.
- **Onde Encaixar**: Topo de todas as páginas da aplicação.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### 5.1. Instalação & Configuração de Ambiente
O Mamba UI não necessita de pacotes npm proprietários. O único requisito é um ambiente configurado com **Tailwind CSS**.

#### Instalação do Tailwind CSS (Vite / Next.js)
```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

#### Pacotes Utilitários Complementares Recomendados
Para garantir formatação consistente e manipulação limpa de classes condicionais:
```bash
npm install clsx tailwind-merge lucide-react framer-motion
```

#### Configuração Completa do `tailwind.config.js`
Para habilitar o suporte completo aos componentes Mamba UI com Dark Mode por classe e paleta rica:

```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  // Habilita o controle do tema escuro via classe .dark no elemento raiz <html>
  darkMode: 'class',
  content: [
    './pages/**/*.{js,ts,jsx,tsx,mdx}',
    './components/**/*.{js,ts,jsx,tsx,mdx}',
    './app/**/*.{js,ts,jsx,tsx,mdx}',
    './src/**/*.{js,ts,jsx,tsx,mdx}',
  ],
  theme: {
    extend: {
      colors: {
        // Mapeamento da cor primária de destaque (ex: Violeta do Mamba UI)
        brand: {
          50: '#f5f3ff',
          100: '#ede9fe',
          200: '#ddd6fe',
          300: '#c4b5fd',
          400: '#a78bfa',
          500: '#8b5cf6',
          600: '#7c3aed',
          700: '#6d28d9',
          800: '#5b21b6',
          900: '#4c1d95',
          950: '#2e1065',
        },
      },
      fontFamily: {
        sans: ['Inter', 'system-ui', '-apple-system', 'sans-serif'],
      },
    },
  },
  plugins: [
    require('@tailwindcss/forms'),
    require('@tailwindcss/typography'),
  ],
};
```

---

### 5.2. Comparativo de Portabilidade de Sintaxe (HTML vs JSX vs Vue)

O Mamba UI destaca-se por fornecer snippets idênticos adaptados às regras de compilação de cada ecossistema:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                   DIFERENÇAS DE MARCAÇÃO ENTRE FRAMEWORKS                   │
├─────────────────┬─────────────────────┬─────────────────────────────────────┤
│ Recurso         │ HTML5 Tradicional   │ React (JSX / TSX)                   │
├─────────────────┼─────────────────────┼─────────────────────────────────────┤
│ Atributo Classe │ class="bg-gray-100" │ className="bg-gray-100"             │
│ Associação Form │ for="email"         │ htmlFor="email"                     │
│ Tags Vazias     │ <input type="text"> │ <input type="text" /> (Self-closing)│
│ Atributos SVG   │ stroke-width="2"    │ strokeWidth={2} (CamelCase)         │
│ Comentários     │ <!-- Comentário --> │ {/* Comentário JSX */}              │
└─────────────────┴─────────────────────┴─────────────────────────────────────┘
```

---

### 5.3. Física de Movimento, Curvas de Transição & Elevação com Framer Motion
Embora o Mamba UI utilize transições CSS nativas do Tailwind (`transition-all duration-300 ease-in-out`), a melhor prática para projetos modernos é adotar o **Framer Motion** para enriquecer a experiência nos componentes-chave com física de mola (*spring physics*):

```typescript
// Constantes de física de movimento recomendadas para componentes Mamba UI
export const mambaMotion = {
  // Transição rápida para botões, toggles e micro-interações
  quickSpring: {
    type: "spring",
    stiffness: 400,
    damping: 30,
    mass: 0.8,
  },
  // Transição suave para cartões, heros e gavetas de menu
  smoothCard: {
    type: "spring",
    stiffness: 260,
    damping: 24,
  },
  // Curva cúbica para expansão de accordions e listas colapsáveis
  accordionBezier: {
    duration: 0.35,
    ease: [0.16, 1, 0.3, 1], // Apple-style ease out
  },
};
```

---

### 5.4. Receitas de Código em Produção (React + Tailwind + TypeScript)

Abaixo estão três implementações completas, funcionais e prontas para uso corporativo, adaptadas dos melhores padrões do Mamba UI:

---

#### Receita 1: Hero Section de Alta Conversão com Split Content & Dark Mode
Componente responsivo completo com headline marcante, chamada dupla para ação, métricas integradas e preview visual flutuante:

```tsx
// components/mamba/HeroSplit.tsx
"use client";

import React from "react";
import { motion } from "framer-motion";
import { ArrowRight, CheckCircle2, Play } from "lucide-react";

interface HeroSplitProps {
  badgeText?: string;
  headline?: string;
  highlightWord?: string;
  description?: string;
  primaryCtaText?: string;
  primaryCtaHref?: string;
  secondaryCtaText?: string;
  onSecondaryClick?: () => void;
  imageUrl?: string;
}

export function HeroSplit({
  badgeText = "Versão 3.0 Disponível",
  headline = "Construa interfaces modernas sem complexidade de",
  highlightWord = "código.",
  description = "Acelere a entrega dos seus produtos digitais utilizando componentes modulares, limpos e acessíveis, estilizados com a pura elegância do Tailwind CSS.",
  primaryCtaText = "Começar Agora Gratuitamente",
  primaryCtaHref = "#pricing",
  secondaryCtaText = "Ver Demonstração",
  onSecondaryClick,
  imageUrl = "https://images.unsplash.com/photo-1551288049-bebda4e38f71?auto=format&fit=crop&w=1200&q=80",
}: HeroSplitProps) {
  return (
    <section className="relative overflow-hidden bg-white py-16 dark:bg-gray-900 md:py-24">
      {/* Luz ambiente de fundo sutil */}
      <div 
        aria-hidden="true" 
        className="pointer-events-none absolute -top-40 right-0 -z-10 h-96 w-96 rounded-full bg-violet-500/10 blur-3xl dark:bg-violet-600/20"
      />

      <div className="container mx-auto flex flex-col justify-between gap-12 px-6 lg:flex-row lg:items-center">
        {/* Coluna Esquerda: Conteúdo & Ações */}
        <motion.div 
          initial={{ opacity: 0, y: 20 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.5, ease: "easeOut" }}
          className="flex flex-col text-left lg:max-w-xl"
        >
          {/* Badge Pill */}
          {badgeText && (
            <div className="mb-6 inline-flex items-center gap-2 self-start rounded-full border border-violet-200 bg-violet-50 px-3 py-1 text-xs font-semibold text-violet-700 dark:border-violet-900/60 dark:bg-violet-950/50 dark:text-violet-300">
              <span className="flex h-2 w-2 rounded-full bg-violet-600 animate-pulse" />
              {badgeText}
            </div>
          )}

          {/* Headline Principal */}
          <h1 className="text-4xl font-extrabold tracking-tight text-gray-900 dark:text-gray-50 sm:text-5xl lg:text-6xl">
            {headline}{" "}
            <span className="text-violet-600 dark:text-violet-400">
              {highlightWord}
            </span>
          </h1>

          {/* Descrição */}
          <p className="mt-6 text-lg leading-relaxed text-gray-600 dark:text-gray-300">
            {description}
          </p>

          {/* Botões de Ação */}
          <div className="mt-8 flex flex-col gap-4 sm:flex-row">
            <a
              href={primaryCtaHref}
              className="inline-flex items-center justify-center gap-2 rounded-lg bg-violet-600 px-6 py-3.5 text-base font-semibold text-white shadow-md shadow-violet-500/20 transition-all duration-200 hover:bg-violet-700 hover:shadow-lg focus:outline-none focus:ring-2 focus:ring-violet-600 focus:ring-offset-2 dark:focus:ring-offset-gray-900"
            >
              {primaryCtaText}
              <ArrowRight className="h-5 w-5" />
            </a>

            <button
              type="button"
              onClick={onSecondaryClick}
              className="inline-flex items-center justify-center gap-2 rounded-lg border border-gray-300 bg-white px-6 py-3.5 text-base font-semibold text-gray-700 transition-all duration-200 hover:bg-gray-50 hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-gray-300 dark:border-gray-700 dark:bg-gray-800 dark:text-gray-200 dark:hover:bg-gray-750 dark:hover:text-white"
            >
              <Play className="h-4 w-4 fill-current text-violet-600 dark:text-violet-400" />
              {secondaryCtaText}
            </button>
          </div>

          {/* Garantias / Micro Prova Social */}
          <div className="mt-10 flex flex-wrap items-center gap-6 text-sm text-gray-500 dark:text-gray-400">
            <div className="flex items-center gap-2">
              <CheckCircle2 className="h-4 w-4 text-emerald-500" />
              <span>Sem cartão de crédito</span>
            </div>
            <div className="flex items-center gap-2">
              <CheckCircle2 className="h-4 w-4 text-emerald-500" />
              <span>Configuração em 5 minutos</span>
            </div>
            <div className="flex items-center gap-2">
              <CheckCircle2 className="h-4 w-4 text-emerald-500" />
              <span>Código 100% aberto</span>
            </div>
          </div>
        </motion.div>

        {/* Coluna Direita: Mockup Visual Flutuante */}
        <motion.div 
          initial={{ opacity: 0, scale: 0.95 }}
          animate={{ opacity: 1, scale: 1 }}
          transition={{ duration: 0.6, delay: 0.1, ease: "easeOut" }}
          className="relative lg:max-w-xl"
        >
          <div className="relative overflow-hidden rounded-2xl border border-gray-200 bg-gray-50 p-2 shadow-2xl dark:border-gray-800 dark:bg-gray-800/80">
            <div className="flex items-center gap-2 border-b border-gray-200 px-4 py-3 dark:border-gray-700">
              <div className="h-3 w-3 rounded-full bg-red-400" />
              <div className="h-3 w-3 rounded-full bg-yellow-400" />
              <div className="h-3 w-3 rounded-full bg-green-400" />
              <span className="ml-2 font-mono text-xs text-gray-400">preview-app.tsx</span>
            </div>
            <img
              src={imageUrl}
              alt="Dashboard de Demonstração"
              className="h-auto w-full rounded-b-xl object-cover"
              loading="lazy"
            />
          </div>
        </motion.div>
      </div>
    </section>
  );
}
```

---

#### Receita 2: Matriz de Preços com Toggle Anual/Mensal & Tier de Destaque
Tabela completa de precificação de 3 planos com alternância de frequência de pagamento e cálculo dinâmico de economia:

```tsx
// components/mamba/PricingMatrix.tsx
"use client";

import React, { useState } from "react";
import { Check, Sparkles } from "lucide-react";

interface PlanFeature {
  text: string;
  included: boolean;
}

interface PricingTier {
  id: string;
  name: string;
  description: string;
  monthlyPrice: number;
  annualPrice: number;
  highlighted?: boolean;
  badge?: string;
  ctaText: string;
  features: PlanFeature[];
}

const defaultTiers: PricingTier[] = [
  {
    id: "starter",
    name: "Starter",
    description: "Perfeito para desenvolvedores solo, criadores e projetos pessoais em validação.",
    monthlyPrice: 0,
    annualPrice: 0,
    ctaText: "Começar Grátis",
    features: [
      { text: "Até 3 projetos simultâneos", included: true },
      { text: "Acesso a 50+ componentes base", included: true },
      { text: "Exportação em HTML e JSX", included: true },
      { text: "Suporte da comunidade Discord", included: true },
      { text: "Atualizações prioritárias", included: false },
      { text: "Consultoria arquitetural mensal", included: false },
    ],
  },
  {
    id: "pro",
    name: "Professional",
    description: "Para equipes que precisam de velocidade extrema e suporte dedicado em produção.",
    monthlyPrice: 29,
    annualPrice: 22,
    highlighted: true,
    badge: "Mais Popular",
    ctaText: "Assinar Plano Pro",
    features: [
      { text: "Projetos ilimitados", included: true },
      { text: "Biblioteca completa com 150+ blocos", included: true },
      { text: "Exportação em HTML, JSX e Vue", included: true },
      { text: "Templates de páginas completas", included: true },
      { text: "Suporte prioritário via e-mail e SLA", included: true },
      { text: "Templates de Admin Dashboards", included: true },
    ],
  },
  {
    id: "enterprise",
    name: "Enterprise",
    description: "Para grandes empresas com exigências rígidas de segurança, governança e SLA.",
    monthlyPrice: 99,
    annualPrice: 79,
    ctaText: "Falar com Vendas",
    features: [
      { text: "Tudo do plano Professional", included: true },
      { text: "Acessibilidade WAI-ARIA personalizada", included: true },
      { text: "Auditoria de Design System sob medida", included: true },
      { text: "Onboarding técnico para a equipe", included: true },
      { text: "SLA garantido de 99.9% de resposta", included: true },
      { text: "Faturamento personalizado via fatura", included: true },
    ],
  },
];

export function PricingMatrix() {
  const [isAnnual, setIsAnnual] = useState(true);

  return (
    <section className="bg-gray-50 py-20 dark:bg-gray-950 sm:py-28">
      <div className="container mx-auto px-6">
        {/* Cabeçalho da Seção */}
        <div className="mx-auto max-w-2xl text-center">
          <h2 className="text-3xl font-extrabold tracking-tight text-gray-900 dark:text-white sm:text-4xl">
            Preços simples e transparentes para qualquer escala
          </h2>
          <p className="mt-4 text-base text-gray-600 dark:text-gray-400">
            Escolha o plano ideal para a sua equipe. Troque ou cancele quando quiser.
          </p>

          {/* Toggle Mensal / Anual */}
          <div className="mt-8 flex items-center justify-center gap-3">
            <span className={`text-sm font-medium ${!isAnnual ? "text-gray-900 dark:text-white" : "text-gray-500"}`}>
              Faturamento Mensal
            </span>
            <button
              type="button"
              role="switch"
              aria-checked={isAnnual}
              onClick={() => setIsAnnual(!isAnnual)}
              className="relative inline-flex h-6 w-11 flex-shrink-0 cursor-pointer rounded-full border-2 border-transparent bg-gray-300 transition-colors duration-200 ease-in-out focus:outline-none focus:ring-2 focus:ring-violet-600 focus:ring-offset-2 dark:bg-gray-700"
              style={{ backgroundColor: isAnnual ? "#7c3aed" : undefined }}
            >
              <span
                aria-hidden="true"
                className={`pointer-events-none inline-block h-5 w-5 transform rounded-full bg-white shadow ring-0 transition duration-200 ease-in-out ${
                  isAnnual ? "translate-x-5" : "translate-x-0"
                }`}
              />
            </button>
            <span className={`flex items-center gap-1.5 text-sm font-medium ${isAnnual ? "text-gray-900 dark:text-white" : "text-gray-500"}`}>
              Faturamento Anual
              <span className="rounded-full bg-emerald-100 px-2 py-0.5 text-xs font-semibold text-emerald-800 dark:bg-emerald-950/80 dark:text-emerald-300">
                Economize 25%
              </span>
            </span>
          </div>
        </div>

        {/* Grade de Cartões */}
        <div className="mt-16 grid grid-cols-1 items-stretch gap-8 lg:grid-cols-3">
          {defaultTiers.map((tier) => {
            const price = isAnnual ? tier.annualPrice : tier.monthlyPrice;

            return (
              <div
                key={tier.id}
                className={`relative flex flex-col justify-between rounded-2xl border p-8 transition-all duration-200 ${
                  tier.highlighted
                    ? "border-2 border-violet-600 bg-white shadow-xl dark:bg-gray-900 lg:-translate-y-2"
                    : "border-gray-200 bg-white shadow-sm dark:border-gray-800 dark:bg-gray-900/60 hover:shadow-md"
                }`}
              >
                {/* Badge Destaque */}
                {tier.badge && (
                  <div className="absolute -top-3.5 left-1/2 -translate-x-1/2">
                    <span className="inline-flex items-center gap-1 rounded-full bg-violet-600 px-4 py-1 text-xs font-bold uppercase tracking-wider text-white shadow-sm">
                      <Sparkles className="h-3 w-3" />
                      {tier.badge}
                    </span>
                  </div>
                )}

                <div>
                  <h3 className="text-xl font-bold text-gray-900 dark:text-white">
                    {tier.name}
                  </h3>
                  <p className="mt-2 text-sm text-gray-500 dark:text-gray-400">
                    {tier.description}
                  </p>

                  <div className="my-6 border-b border-gray-100 pb-6 dark:border-gray-800">
                    <div className="flex items-baseline">
                      <span className="text-5xl font-black tracking-tight text-gray-900 dark:text-white">
                        ${price}
                      </span>
                      <span className="ml-2 text-sm font-medium text-gray-500 dark:text-gray-400">
                        /mês
                      </span>
                    </div>
                    {isAnnual && price > 0 && (
                      <p className="mt-1 text-xs text-emerald-600 dark:text-emerald-400">
                        Cobrado anualmente (${price * 12}/ano)
                      </p>
                    )}
                  </div>

                  {/* Lista de Funcionalidades */}
                  <ul className="space-y-3.5">
                    {tier.features.map((feat, idx) => (
                      <li key={idx} className="flex items-start gap-3 text-sm">
                        {feat.included ? (
                          <Check className="h-5 w-5 flex-shrink-0 text-violet-600 dark:text-violet-400" />
                        ) : (
                          <span className="h-5 w-5 flex-shrink-0 text-gray-300 dark:text-gray-600">
                            —
                          </span>
                        )}
                        <span
                          className={
                            feat.included
                              ? "text-gray-700 dark:text-gray-200"
                              : "text-gray-400 line-through dark:text-gray-500"
                          }
                        >
                          {feat.text}
                        </span>
                      </li>
                    ))}
                  </ul>
                </div>

                {/* Botão de Contratação */}
                <div className="mt-8 pt-4">
                  <button
                    type="button"
                    className={`w-full rounded-lg px-4 py-3 text-center text-sm font-semibold transition-all duration-200 focus:outline-none focus:ring-2 focus:ring-offset-2 ${
                      tier.highlighted
                        ? "bg-violet-600 text-white shadow-md shadow-violet-500/20 hover:bg-violet-700 focus:ring-violet-600 dark:focus:ring-offset-gray-900"
                        : "border border-gray-300 bg-white text-gray-700 hover:bg-gray-50 dark:border-gray-700 dark:bg-gray-800 dark:text-gray-200 dark:hover:bg-gray-750"
                    }`}
                  >
                    {tier.ctaText}
                  </button>
                </div>
              </div>
            );
          })}
        </div>
      </div>
    </section>
  );
}
```

---

#### Receita 3: Skeleton Loader Modular com Animação de Pulso Suave
Componente de feedback visual instantâneo para carregamento assíncrono de feeds de artigos e listas de produtos:

```tsx
// components/mamba/SkeletonFeed.tsx
import React from "react";

interface SkeletonCardProps {
  hasImage?: boolean;
}

export function SkeletonCard({ hasImage = true }: SkeletonCardProps) {
  return (
    <div 
      role="status" 
      aria-label="Carregando conteúdo..."
      className="flex flex-col overflow-hidden rounded-xl border border-gray-200 bg-white p-5 shadow-sm animate-pulse dark:border-gray-800 dark:bg-gray-900"
    >
      {/* Imagem de Capa Placeholder */}
      {hasImage && (
        <div className="mb-4 h-48 w-full rounded-lg bg-gray-200 dark:bg-gray-800" />
      )}

      {/* Tag ou Categoria */}
      <div className="mb-3 h-4 w-20 rounded bg-violet-200 dark:bg-violet-900/40" />

      {/* Linhas de Título */}
      <div className="space-y-2">
        <div className="h-5 w-5/6 rounded bg-gray-200 dark:bg-gray-800" />
        <div className="h-5 w-3/5 rounded bg-gray-200 dark:bg-gray-800" />
      </div>

      {/* Linhas de Descrição */}
      <div className="mt-4 space-y-2">
        <div className="h-3.5 w-full rounded bg-gray-100 dark:bg-gray-850" />
        <div className="h-3.5 w-11/12 rounded bg-gray-100 dark:bg-gray-850" />
        <div className="h-3.5 w-2/3 rounded bg-gray-100 dark:bg-gray-850" />
      </div>

      {/* Rodapé com Avatar e Autor */}
      <div className="mt-6 flex items-center gap-3 pt-4 border-t border-gray-100 dark:border-gray-800">
        <div className="h-10 w-10 flex-shrink-0 rounded-full bg-gray-200 dark:bg-gray-800" />
        <div className="flex-1 space-y-1.5">
          <div className="h-3.5 w-28 rounded bg-gray-200 dark:bg-gray-800" />
          <div className="h-3 w-16 rounded bg-gray-100 dark:bg-gray-850" />
        </div>
      </div>
      <span className="sr-only">Carregando dados do artigo...</span>
    </div>
  );
}

export function SkeletonGrid({ count = 3 }: { count?: number }) {
  return (
    <div className="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-3">
      {Array.from({ length: count }).map((_, index) => (
        <SkeletonCard key={index} />
      ))}
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao declarar o **Mamba UI** como a biblioteca base ou inspiração de design system em um projeto através do `DESIGN_BLUEPRINT.md`, a inteligência artificial e os engenheiros devem respeitar as diretrizes de governança técnica abaixo:

### 1. Declaração Formal no Blueprint
```markdown
## Design System & Component Library
- **Biblioteca Base**: Mamba UI (`https://www.mambaui.com/` / `Microwawe/mamba-ui`)
- **Estética Predominante**: Modern Tailwind Utility + Clean Editorial Layouts
- **Estratégia de Integração**: Copiar e colar modular (Zero-Runtime NPM overhead)
- **Paleta de Destaque Oficial**: Tailwind `Violet` (`brand-600: #7c3aed`) + `Slate` neutro
- **Dark Mode Strategy**: `.dark` class no elemento `<html>` com `dark:bg-gray-900`
- **Camada de Interação**: React Hooks (`useState`) + Framer Motion nos componentes de 10%
```

### 2. Checklist de Governança de Código
1. **Configuração Obrigatória do Purge/Content**: Assegure que o array `content` no `tailwind.config.js` faça a varredura correta dos diretórios de componentes para evitar que classes copiadas do Mamba UI sejam expurgadas no build de produção.
2. **Harmonização com shadcn/ui**: Se o projeto utilizar simultaneamente componentes do Mamba UI (para blocos de landing page) e **shadcn/ui** (para diálogos, comboboxes e popovers), unifique as variáveis de cor no CSS global mapeando `--primary` para a mesma tonalidade (`#7c3aed` / violet-600) para garantir continuidade estética perfeita.
3. **Substituição de SVGs Inline por Lucide React**: Embora os SVGs embutidos do Mamba UI sejam excelentes para prototipagem rápida, em bases de código de médio a grande porte, substitua os vetores manuais por componentes do `lucide-react` (`ArrowRight`, `Check`, `Menu`, etc.) para melhorar a manutenibilidade e padronização de tamanhos (`size={20}`).
4. **Copywriting Realista & Sem Meta-texto**: Elimine completamente textos genéricos de preenchimento ("Lorem ipsum dolor", "Component description here"). Adote linguagem clara de produto focada no usuário final (*"Experimente grátis por 14 dias"*, *"Documentação da API"*, *"Acessar painel"*).
5. **Acessibilidade Semântica de Formulários**: Ao transpor formulários do Mamba UI para React, certifique-se de que cada `<input>` possua um `id` único conectado ao `htmlFor` de seu respectivo `<label>`, mantendo os atributos `aria-describedby` para mensagens de erro ou validação.
