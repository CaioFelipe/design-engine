---
id: "hyperui-dev"
name: "HyperUI"
url: "https://www.hyperui.dev/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Modern Clean Utility", "Retro Neobrutalism", "Zero-JS Semantic HTML", "Tailwind CSS v4 Native", "Radical Copy-Paste Agility"]
densidade_informacao: "Flexivel"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS/Headless)"
stack_frameworks: ["Tailwind CSS v4 & v3", "HTML5 Semântico", "React (JSX / TSX)", "Vue.js", "Alpine.js (HyperUX)", "Astro / Laravel Blade / Rails ERB"]
compatibilidade:
  fontes_ideais: ["Inter", "Plus Jakarta Sans", "Cabinet Grotesk", "Space Grotesk", "Public Sans", "JetBrains Mono"]
  paletas_ideais: ["Neobrutalist Pop (Canary Yellow, Bubblegum Pink, Neo-Mint + Pure Black)", "Neutral Slate & Zinc Enterprise", "High-Contrast Monochrome", "Emerald & Crimson Financial Metrics"]
  combinacoes_recomendadas: ["Shadcn UI", "Lucide React / Heroicons", "Alpine.js", "Tailwind Forms Plugin", "Tailwind Typography Plugin", "Motion Primitives"]
  conflitos_esteticos: ["Glassmorfismo pesado translúcido com blur excessivo", "Skeuomorfismo brilhante iOS 6", "Dark Mode ultra-saturado com neons cyberpunk conflitantes com Neobrutalismo"]
---

# HyperUI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **HyperUI**, criado e mantido pelo engenheiro britânico **Mark Mead** (@markmead), é uma das bibliotecas de componentes de código aberto baseadas em Tailwind CSS mais populares, respeitadas e pragmáticas da web contemporânea. Concebido sob o lema da máxima eficiência para o desenvolvedor, o HyperUI resolve a fricção fundamental do ecossistema de front-end: a complexidade desnecessária de dependências NPM, configurações pesadas de bundler e amarras a frameworks específicos de JavaScript.

Enquanto a maioria das bibliotecas modernas obriga o desenvolvedor a adotar ecossistemas inteiros de gerenciamento de estado e bibliotecas headless (como Radix UI, React Aria ou Ark UI), o HyperUI opera no princípio da **Elegância Primitiva do HTML5 Semântico potencializado pelo Tailwind CSS puro (v3 e v4)**. O resultado é uma biblioteca verdadeiramente *agnóstica de framework* que pode ser incorporada instantaneamente em projetos Next.js, Remix, Astro, SvelteKit, Vue, Nuxt, Laravel Blade, Ruby on Rails ERB, Django Templates ou arquivos HTML estáticos.

### A Dualidade Estética Distinta de Mark Mead

Diferente de repositórios convencionais de UI que seguem uma única linha monolítica, o HyperUI consolidou sua assinatura de design dividindo seu acervo em duas frentes complementares e altamente refinadas:

1. **A Vertente Modern Clean / SaaS Utility**:
   - Voltada para produtos digitais modernos, painéis administrativos, plataformas de e-commerce e páginas de conversão corporativas.
   - Caracteriza-se pelo uso comedido de superfícies brancas e neutras (`bg-white`, `border-gray-100`, `dark:border-gray-800`), tipografia estruturada com pesos equilibrados (`font-medium text-gray-900` sobre `text-gray-500`), raios de curvatura orgânicos (`rounded-lg`, `rounded-md`) e micro-interações táteis sutis via estados `:hover`, `:focus-visible` e `:active`.
   - Estrutura de dados organizada em grids responsivos rigorosos, listas de detalhes (`<dl>`, `<dt>`, `<dd>`) e cartões de estatísticas com indicadores visuais de crescimento percentual.

2. **A Linha Especializada em Neobrutalism (Retro-Pop High Contrast)**:
   - Uma das maiores contribuições autorais do HyperUI para a comunidade foi ser pioneiro em transformar o estilo **Neobrutalista** — originado no design gráfico contemporâneo, no design editorial de vanguarda e na identidade de plataformas como Figma e Gumroad — em componentes Tailwind CSS prontos para produção.
   - Sua assinatura física é imediatamente reconhecível:
     - **Bordas Espessas de Alto Contraste**: Uso sistemático de `border-2 border-black` (ou `dark:border-white`), demarcando silhuetas nítidas e geométricas que rejeitam o degradê suave e o blur difuso.
     - **Sombras Duras de Bloco (Hard Drop Shadows)**: Em vez de sombras Gaussianas difusas (`shadow-md`), emprega sombras de projeção ortogonal com offset sólido: `shadow-[4px_4px_0_0] shadow-black` ou `shadow-[6px_6px_0_0] shadow-black`.
     - **Mecânica Tátil de Afundamento Físico**: Quando o usuário interage via hover ou clique, o elemento sofre uma translação geométrica compensatória (`hover:translate-x-1 hover:translate-y-1 hover:shadow-none` ou `active:translate-1`), simulando com perfeição mecânica o ato de pressionar um botão mecânico físico real ou um carimbo sobre papel.
     - **Paleta Pastel Ácida**: Fundos contrastantes com cores primárias e secundárias dessaturadas em tom pastel (`bg-yellow-200`, `bg-pink-300`, `bg-teal-200`, `bg-emerald-300`, `bg-amber-100`), equilibrados contra preto absoluto (`#000000`) e branco puro (`#ffffff`).

### A Filosofia "Zero-JS by Default" & Acessibilidade Nativa

Um dos pilares técnicos mais impressionantes do HyperUI é a exploração exaustiva das capacidades nativas do HTML5 e dos seletores modernos de CSS3 / Tailwind CSS:
- **Sanfonas e Accordions sem JavaScript**: Uso inteligente da tag nativa `<details class="group">` e `<summary>`, manipulando a rotação de ícones de chevron exclusivamente via `group-open:-rotate-180` ou estados do Tailwind.
- **Toggles e Checkboxes Personalizados via CSS**: Uso de inputs nativos ocultos com classes `peer` e seletores modernos como `peer-checked:bg-blue-600` e `:has()`, garantindo compatibilidade total com formulários HTML padrão sem necessidade de listeners de evento JS.
- **Acessibilidade Universal (a11y)**: Todos os componentes trazem embutidos atributos `aria-hidden="true"` em SVGs decorativos, textos ocultos para leitores de tela via `sr-only` ("Increase: ", "Decrease: ", "Close modal"), estados de foco acessíveis com `focus:ring-2 focus:ring-offset-2` e consideração para navegação bidirecional (RTL).
- **Extensão HyperUX**: Para padrões que inevitavelmente exigem manipulação de DOM (como aberturas de modal com focus trap, tabs com sincronização de hash ou menus dropdown suspensos com fechamento ao clicar fora), Mark Mead mantém o ecossistema satélite **HyperUX** (`js.hyperui.dev`), fornecendo snippets minimalistas em **Alpine.js** ou JavaScript Vanilla puro, mantendo o bundle leve e sem lock-in.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados

1. **Aplicações Server-Side Rendered (SSR) & Monólitos Modernos (Laravel, Rails, Django, Phoenix)**:
   Aplicações em Laravel (Blade), Ruby on Rails (ViewComponent/ERB) ou Django onde a arquitetura não justifica o peso de um SPA complexo em React/Vue. O desenvolvedor copia e cola o markup semântico diretamente nos templates do servidor, obtendo interfaces de acabamento profissional com zero linhas de build de JavaScript de front-end.
2. **E-Commerce Direct-to-Consumer (D2C) & Lojas Shopify / Hydrogen / Medusa**:
   O HyperUI possui um dos conjuntos mais ricos e acessíveis de blocos de e-commerce da web livre: cartões de produto com alternância de imagem em hover, galerias com carrossel, seletores de grade de tamanhos, drawers de carrinho lateral (`carts`), formulários de checkout e tabelas de frete.
3. **SaaS B2B, Painéis Administrativos & Backoffices Operacionais**:
   Dashboards corporativos que demandam rápida montagem de métricas de negócio, sidebars com navegação colapsável em árvore (`vertical-menu`), tabelas com paginação e badges de status operacional (`badges`, `tables`, `stats`).
4. **Produtos com Personalidade Neobrutalista, Web3, Criadores & Ferramentas Dev**:
   Aplicações que buscam fugir da mesmice do "minimalismo asséptico corporativo" e desejam transmitir energia, irreverência e alta taticidade visual — como plataformas para criadores de conteúdo, portfólios de design, newsletters pagas e ferramentas para desenvolvedores independentes (indie hackers).
5. **Hackathons, MVPs & Prototipagem de Alta Velocidade**:
   Quando a velocidade de entrega é o fator crítico. Em vez de gastar horas configurando pacotes de componentes, dependências transitivas e temas no `tailwind.config.js`, o engenheiro copia o componente funcional diretamente da documentação do HyperUI para a tela em menos de 10 segundos.

### Papel no Ritmo Visual (A Aplicação da Regra 60-30-10)

O HyperUI se adapta com flexibilidade cirúrgica aos três papéis visuais, a depender do estilo escolhido:

- **60% — Fundação Neutra & Esqueleto Estrutural (Linha Clean / Application UI)**:
  Quando se utiliza a coleção clássica do HyperUI, ele cumpre com perfeição o papel de base funcional de 60%: cartões de agrupamento, fundos de tela, barras de navegação superiores e inferiores, formulários de entrada de dados e tabelas administrativas sóbrias.
- **30% — Camada de Navegação & Micro-interações Nativas**:
  As sanfonas baseadas em `<details>`, os menus suspensos, os breadcrumbs responsivos, os toggles de alternância de estado e as barras de progresso orquestram o ritmo do fluxo sem roubar a cena nem degradar a taxa de quadros (60/120 FPS cravados via aceleração por hardware do browser).
- **10% — Efeito Showstopper / Ponto Focal (Linha Neobrutalism)**:
  Quando um projeto adota a linha Neobrutalista nos elementos de conversão (botões de Call-To-Action com sombras de 4px, badges com contornos grossos e cards de precificação com cores ácidas de contraste), o HyperUI assume com autoridade o papel do **10% de impacto visual**. O olhar do usuário é imediatamente atraído para o elemento tátil de borda preta espessa e projeção ortogonal.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

1. **Aplicações Enterprise com Necessidade Crítica de Focus Management Complexo (Sem Wrapper JS)**:
   Embora os modais e dropdowns em CSS puro do HyperUI sejam ideais para protótipos e telas simples, utilizá-los em aplicações bancárias ou fluxos clínicos sem adicionar uma camada robusta de Focus Trap (retorno de foco ao botão de abertura após fechar o modal, navegação bidirecional por setas de teclado em menus WAI-ARIA) fere os critérios estritos de conformidade WCAG AAA. Nesses casos, o markup do HyperUI deve ser envelopado por primitivas headless (como Radix UI ou Headless UI).
2. **Experiências Imersivas 3D / WebGL / Canvas**:
   Projetos cinematográficos governados por Three.js, shaders GLSL ou transições de scroll contínuas com GSAP não se beneficiam de uma biblioteca baseada no modelo tradicional de caixa de fluxo de documento HTML.
3. **Design Systems com Tokenização Rigorosa Automatizada via Figma Tokens**:
   Se uma empresa exige que cada classe CSS seja gerada a partir de tokens atômicos com nomes semânticos corporativos proprietários (ex: `var(--ds-spacing-squish-sm)`), o copy-paste de classes Tailwind canônicas (`p-6`, `gap-4`, `border-gray-100`) exigirá refatoração manual para alinhar-se à taxonomia da empresa.

---

### ⚠️ Erros Comuns de Exagero & Anti-Padrões:

1. **A Salada Mista: Neobrutalismo Híbrido com Glassmorfismo Suave**:
   O erro visual mais grave ao usar o HyperUI é misturar em uma mesma tela elementos neobrutalistas (bordas pretas de 2px, sombras duras sem blur) com cartões translúcidos com `backdrop-blur-md` e sombras suaves de 20px. Isso quebra a física do mundo visual criado pela interface: ou a página é de papel impresso e blocos físicos sólidos, ou é de vidro óptico translúcido. Nunca misture os dois.
2. **Poluição Cromática Neobrutalista ("A Síndrome do Parque de Diversões")**:
   O Neobrutalismo é impactante quando aplicado com parcimônia. Usar 6 cores ácidas simultâneas (botão amarelo, card rosa, input ciano, banner verde-limão, badge laranja e footer roxo) gera sobrecarga cognitiva severa e aparência amadora. A regra de ouro é escolher **uma única cor pastel de destaque** (ex: amarelo `bg-yellow-200`) e manter o restante em preto, cinza e branco.
3. **Abandono de Validações em Inputs Apenas Estilizados**:
   O HyperUI oferece dezenas de variações visuais de inputs (floating label, under-border, inset label, prefix icons). Nunca confie apenas nas classes Tailwind para sinalizar estados de erro; sempre implemente atributos `aria-invalid="true"`, mensagens de erro com IDs vinculados via `aria-describedby` e contraste de cores adequado em modo escuro.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

O HyperUI organiza seu catálogo em centenas de componentes divididos em categorias estratégicas. Abaixo estão **12 componentes emblemáticos** criteriosamente selecionados, cobrindo o melhor do Neobrutalismo, Application UI, E-Commerce e Marketing:

### 1. Neobrutalist Pressed Action Button
- **Anatomia Visual**: Botão retangular delimitado por borda sólida de 2px em preto absoluto (`border-2 border-black`), fundo com contraste vibrante (`bg-white` ou `bg-yellow-200`) e projeção ortogonal estática de 4px (`shadow-[4px_4px_0_0] shadow-black`). Ao receber o foco do teclado, revela anel de foco de alta visibilidade (`focus:ring-2 focus:ring-yellow-300 focus:outline-0`).
- **Gatilho de Interação**:
  - `Hover`: O elemento se desloca fisicamente 1 unidade para baixo e para a direita (`hover:translate-1`), enquanto a sombra é simultaneamente eliminada (`hover:shadow-none`). O efeito visual resultante é a perfeita ilusão de que a tecla física foi pressionada contra a superfície da tela.
- **Onde encaixar na página**: Hero CTA principal, botões de ação em modais críticos, botões de envio em formulários de conversão.

### 2. Semantic Financial / Growth Stat Card
- **Anatomia Visual**: Contêiner semântico `<article>` com cantos arredondados suaves (`rounded-lg border border-gray-100 bg-white p-6 dark:border-gray-800 dark:bg-gray-900`). Na porção superior direita, exibe um badge compacto temático com ícone SVG de tendência (seta para cima/baixo), fundo suave (`bg-green-100 text-green-600` ou `bg-red-100 text-red-600`) e texto descritivo para leitores de tela (`<span class="sr-only">Increase:</span>`). Na parte inferior, tipografia em dois níveis com rótulo (`text-sm text-gray-500`) e valor absoluto em destaque tipográfico (`text-2xl font-medium text-gray-900`).
- **Gatilho de Interação**: Estático ou com leve realce de borda ao passar o cursor (`hover:border-gray-200 transition-colors`).
- **Onde encaixar na página**: Painéis analíticos, topo de páginas de faturamento, painel de administração de SaaS e relatórios de métricas.

### 3. Zero-JS Collapsible Accordion (`<details class="group">`)
- **Anatomia Visual**: Painel de perguntas frequentes estruturado puramente nas tags nativas do HTML5 `<details>` e `<summary>`. No estado fechado, exibe apenas a pergunta com cursor pointer e ícone de seta voltado para baixo. Possui bordas limpas e fundo sutil (`border border-gray-200 rounded-lg p-4`).
- **Gatilho de Interação**:
  - `Click`: O navegador gerencia a abertura nativa do conteúdo sem tocar em JavaScript. A classe utilitária do Tailwind `group-open:-rotate-180` inverte suavemente o ícone do SVG através de `transition-transform duration-300`, revelando o corpo da resposta com tipografia suave e margem superior ajustada.
- **Onde encaixar na página**: Seção de FAQ em landing pages, seções colapsáveis de configurações avançadas e menus de documentação técnica.

### 4. Floating Label Animated Input
- **Anatomia Visual**: Campo de formulário moderno onde o `<label>` repousa visualmente dentro do campo de input quando vazio, funcionando como um placeholder estilizado.
- **Gatilho de Interação**:
  - `Focus / Input Text`: Através do seletor CSS avançado `peer-placeholder-shown` e `peer-focus`, quando o campo recebe foco ou ganha texto, o rótulo reduz seu tamanho de fonte (`text-xs`), translada para a borda superior (`-top-2.5`) e adota a cor primária de destaque da marca (`text-blue-600 dark:text-blue-400`), liberando o espaço de digitação de forma orgânica e fluida sem requerer controle de estado em React.
- **Onde encaixar na página**: Telas de login/registro, formulários de captura de leads e finalização de pedido em e-commerce.

### 5. Multi-Column Responsive Mega-Footer (24 Variantes)
- **Anatomia Visual**: Seção estrutural de rodapé com hierarquia complexa: grade de 4 a 6 colunas de links institucionais, área de inscrição de newsletter em linha única (`inline input + button`), linha inferior com direitos autorais, links legais e links sociais com ícones em SVGs otimizados.
- **Gatilho de Interação**: Hover com transição de cor suave nos links (`hover:text-gray-700 transition-colors dark:hover:text-gray-200`) e foco visível em todos os elementos interativos.
- **Onde encaixar na página**: Rodapé global da aplicação ou portal institucional.

### 6. Neobrutalist Badge with Hard Border & Contrast Pill
- **Anatomia Visual**: Etiqueta inline com espessura marcante (`border-2 border-black bg-white px-3 py-1 text-xs font-bold uppercase tracking-wider text-black shadow-[2px_2px_0_0] shadow-black`). Variações coloridas aplicam preenchimentos em tons pop (`bg-emerald-300`, `bg-rose-300`, `bg-amber-300`).
- **Gatilho de Interação**: Estático ou com leve rotação lúdica em hover (`hover:-rotate-2 transition-transform`).
- **Onde encaixar na página**: Tags de categoria em posts de blog, badges de status em pedidos ("PAGO", "PENDENTE", "NOVO"), selos de desconto ("50% OFF") em vitrines.

### 7. E-Commerce Product Card with Dynamic Image Flip
- **Anatomia Visual**: Card retangular com proporção vertical (`aspect-[3/4]` ou `aspect-square`). O contêiner pai recebe a classe `group relative block overflow-hidden`. Exibe a imagem principal do produto e, por baixo, a imagem secundária (ex: modelo vestindo a peça por outro ângulo). Na base, exibe título em tipografia limpa, avaliações em estrelas e preço destacado.
- **Gatilho de Interação**:
  - `Hover`: A imagem frontal transiciona sua opacidade para zero (`group-hover:opacity-0 transition-opacity duration-500`), revelando a imagem alternativa subjacente de forma cinematográfica e instantânea. Botões de adição rápida ao carrinho deslizam suavemente a partir da base do card (`translate-y-full group-hover:translate-y-0`).
- **Onde encaixar na página**: Vitrines de produtos, catálogos de moda, listagens de merchandising e seções de itens recomendados.

### 8. Collapsible Hierarchical Vertical Dashboard Menu
- **Anatomia Visual**: Navegação vertical lateral (`<aside class="flex h-screen flex-col justify-between border-e border-gray-100 bg-white dark:border-gray-800 dark:bg-gray-900">`). Os itens de navegação são organizados em categorias com ícones alinhados, contadores numéricos de notificação (`badge`) e submenus colapsáveis com linhas guias verticais sutis.
- **Gatilho de Interação**: Hover com destaque em cinza suave (`hover:bg-gray-100 dark:hover:bg-gray-800 rounded-lg`) e rotação de chevrons ao expandir submenus.
- **Onde encaixar na página**: Sidebar principal de aplicações SaaS, plataformas de CMS e ferramentas analíticas internas.

### 9. Modern Tiered Pricing Table with Feature Matrix
- **Anatomia Visual**: Grid comparativo de planos de assinatura (Free, Pro, Enterprise). O plano Pro (destaque) recebe elevação visual através de borda destacada com anel de cor (`border-2 border-blue-600 shadow-xl`), fita de recomendação ("Mais Popular") e botão de CTA de alta ênfase. Cada plano lista seus recursos com ícones de checagem verdes (`text-green-600`) ou cruz de indisponibilidade cinza (`text-gray-400`).
- **Gatilho de Interação**: Efeito sutil de elevação em hover no card inteiro (`hover:-translate-y-1 transition-transform`).
- **Onde encaixar na página**: Seção de precificação de landing pages de SaaS e páginas de upgrade de assinatura.

### 10. Sliding E-Commerce Cart Drawer
- **Anatomia Visual**: Painel lateral deslizante de alta fidelidade para visualização de carrinho de compras. Apresenta lista de itens adicionados com miniaturas quadradas, controles de incremento de quantidade (`+ / -`), cálculo de subtotal e botão de checkout direto para finalização.
- **Gatilho de Interação**: Transição suave de entrada e saída a partir da borda direita da viewport (`translate-x-full` para `translate-x-0` com `transition-transform duration-300 ease-in-out`), apoiada por overlay escurecido de fundo.
- **Onde encaixar na página**: Overlay global disparado ao clicar no ícone de sacola/carrinho na barra de navegação.

### 11. Multi-Step Form Stepper / Progress Indicator
- **Anatomia Visual**: Barra horizontal de progresso em múltiplos passos para processos sequenciais (ex: 1. Informações Pessoais, 2. Endereço de Envio, 3. Pagamento, 4. Confirmação). Passos concluídos recebem círculo preenchido com ícone de visto; o passo atual exibe anel de foco destacado com texto em negrito; passos futuros permanecem em tom neutro atenuado com conector em linha contínua.
- **Gatilho de Interação**: Atualização contextual reativa via classes de estado condicional.
- **Onde encaixar na página**: Fluxos de onboarding de usuários, checkout de e-commerce e assistentes de configuração de projeto (wizards).

### 12. Neobrutalist Notification Alert Banner
- **Anatomia Visual**: Caixa de alerta com contorno agressivo (`border-2 border-black bg-white p-4 shadow-[4px_4px_0_0] shadow-black`). Incorpora ícone de advertência com contorno rígido e tipografia expressiva em caixa alta (`font-bold text-black`), acompanhado de botão de fechar (`x`) que afunda ao clique.
- **Gatilho de Interação**: Fechamento tátil e feedback imediato de atenção visual.
- **Onde encaixar na página**: Avisos de manutenção do sistema, comunicados de cookies de privacidade e notificações de erro crítico de formulário.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

O HyperUI é intencionalmente livre de lock-in de biblioteca NPM. Para utilizá-lo em qualquer projeto moderno (Tailwind CSS v4 ou v3), a configuração base consiste em ter o Tailwind instalado no pipeline do projeto.

#### Setup Recomendado com Tailwind CSS v4:
No Tailwind CSS v4, o sistema adota configuração orientada a CSS (`@theme`), eliminando a necessidade de arquivos `tailwind.config.js` legados.

```css
/* app/globals.css ou src/index.css */
@import "tailwindcss";

@theme {
  /* Tokens de Apoio para a Linha Neobrutalista do HyperUI */
  --shadow-neobrutal: 4px 4px 0px 0px #000000;
  --shadow-neobrutal-lg: 6px 6px 0px 0px #000000;
  --shadow-neobrutal-dark: 4px 4px 0px 0px #ffffff;
  
  /* Curvas de transição táteis */
  --ease-snappy: cubic-bezier(0.2, 0, 0, 1);
}
```

Para projetos que utilizam formulários complexos e tipografia editorial, recomenda-se ter os utilitários de apoio:
```bash
# Ícones de padrão da indústria recomendados para casar com HyperUI
npm install lucide-react clsx tailwind-merge
```

---

### Física de Movimento, Parâmetros e Transições

O HyperUI opera em duas físicas de movimento diametralmente opostas e complementares:

#### 1. A Física Tátil do Neobrutalismo (Snappy & Instantânea):
- **Tempo de Duração**: Extremamente curto (`100ms` a `150ms`). Não há desaceleração suave, pois simula o clique seco de um interruptor mecânico ou carimbo industrial.
- **Curva de Transição**: `cubic-bezier(0, 0, 0.2, 1)` ou linear com corte súbito.
- **Parâmetros de Spring equivalentes em Framer Motion**:
  ```ts
  const neobrutalSpring = {
    type: "spring",
    stiffness: 700, // Altíssima rigidez mecânica
    damping: 35,    // Amortecimento firme sem oscilação elástica
    mass: 0.8
  };
  ```

#### 2. A Física Suave do Modern Clean / Application UI:
- **Tempo de Duração**: Padrão de interface moderna (`200ms` a `300ms`).
- **Curva de Transição**: `cubic-bezier(0.4, 0, 0.2, 1)` (`ease-in-out` nativo do browser).
- **Parâmetros de Spring equivalentes**:
  ```ts
  const modernSmoothSpring = {
    type: "spring",
    stiffness: 260,
    damping: 20
  };
  ```

---

### Receitas de Código Estrutural Funcional

Abaixo estão três implementações completas, realistas e prontas para uso em produção, ilustrando a versatilidade do HyperUI:

#### Receita 1: Card & Botão Neobrutalista Interativo (HTML + Tailwind Puro)
Este exemplo demonstra como obter a estética neobrutalista tátil com suporte a Modo Escuro e zero JavaScript.

```html
<!-- Componente: Neobrutalist Feature Card com Botão de Ação Físico -->
<div 
  class="relative max-w-sm border-2 border-black bg-white p-6 shadow-[6px_6px_0_0] shadow-black transition-all hover:-translate-x-0.5 hover:-translate-y-0.5 hover:shadow-[8px_8px_0_0] hover:shadow-black dark:border-white dark:bg-gray-900 dark:shadow-white dark:hover:shadow-white"
>
  <!-- Badge Superior Neobrutalista em Amarelo Pastel -->
  <span 
    class="inline-block border-2 border-black bg-yellow-200 px-3 py-1 text-xs font-bold uppercase tracking-wider text-black shadow-[2px_2px_0_0] shadow-black dark:border-white"
  >
    Destaque Pro
  </span>

  <h3 class="mt-4 text-xl font-bold text-black dark:text-white">
    Automação Sem Fricção
  </h3>

  <p class="mt-2 text-sm leading-relaxed text-gray-700 dark:text-gray-300">
    Componentes semânticos construídos para velocidade máxima de entrega. Sem dependências pesadas, sem quebra de build.
  </p>

  <!-- Botão Tátil com Efeito Físico de Afundamento ao Clicar -->
  <div class="mt-6">
    <button
      type="button"
      class="group inline-flex items-center gap-2 border-2 border-black bg-emerald-300 px-5 py-3 text-sm font-bold text-black shadow-[4px_4px_0_0] shadow-black transition-all hover:translate-x-1 hover:translate-y-1 hover:shadow-none focus:outline-none focus:ring-2 focus:ring-black dark:border-white dark:bg-emerald-400 dark:shadow-white dark:hover:shadow-none dark:focus:ring-white"
    >
      <span>Explorar Módulos</span>
      <svg 
        class="size-4 transition-transform group-hover:translate-x-1" 
        fill="none" 
        viewBox="0 0 24 24" 
        stroke="currentColor" 
        stroke-width="2.5"
        aria-hidden="true"
      >
        <path stroke-linecap="round" stroke-linejoin="round" d="M14 5l7 7m0 0l-7 7m7-7H3" />
      </svg>
    </button>
  </div>
</div>
```

---

#### Receita 2: Versão React / TypeScript Acessível do Card Financeiro de Métricas
Este componente traduz o padrão de métricas de Application UI do HyperUI em um componente React reutilizável, tipado e com suporte total a leitores de tela.

```tsx
// components/ui/MetricCard.tsx
import React from "react";
import { ArrowUpRight, ArrowDownRight, DollarSign } from "lucide-react";
import { clsx, type ClassValue } from "clsx";
import { twMerge } from "tailwind-merge";

function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs));
}

export interface MetricCardProps {
  title: string;
  value: string;
  previousValue?: string;
  percentageChange: number;
  timeframe?: string;
  icon?: React.ReactNode;
  className?: string;
}

export const MetricCard: React.FC<MetricCardProps> = ({
  title,
  value,
  previousValue,
  percentageChange,
  timeframe = "em relação ao mês anterior",
  icon = <DollarSign className="size-5" aria-hidden="true" />,
  className,
}) => {
  const isPositive = percentageChange >= 0;

  return (
    <article
      className={cn(
        "flex flex-col justify-between rounded-xl border border-gray-100 bg-white p-6 shadow-sm transition-all duration-200 hover:border-gray-200 hover:shadow-md dark:border-gray-800 dark:bg-gray-900",
        className
      )}
    >
      <div className="flex items-center justify-between">
        <div className="flex items-center gap-3">
          <span className="flex size-10 items-center justify-center rounded-lg bg-gray-50 text-gray-700 dark:bg-gray-800 dark:text-gray-300">
            {icon}
          </span>
          <p className="text-sm font-medium text-gray-500 dark:text-gray-400">
            {title}
          </p>
        </div>

        {/* Delta Tag de Crescimento */}
        <div
          className={cn(
            "inline-flex items-center gap-1 rounded-full px-2.5 py-0.5 text-xs font-semibold",
            isPositive
              ? "bg-emerald-50 text-emerald-700 dark:bg-emerald-950/50 dark:text-emerald-400"
              : "bg-rose-50 text-rose-700 dark:bg-rose-950/50 dark:text-rose-400"
          )}
        >
          {isPositive ? (
            <ArrowUpRight className="size-3.5 stroke-[2.5]" aria-hidden="true" />
          ) : (
            <ArrowDownRight className="size-3.5 stroke-[2.5]" aria-hidden="true" />
          )}
          <span className="sr-only">
            {isPositive ? "Aumento de: " : "Redução de: "}
          </span>
          <span>{Math.abs(percentageChange).toFixed(1)}%</span>
        </div>
      </div>

      <div className="mt-4">
        <p className="text-3xl font-semibold tracking-tight text-gray-900 dark:text-white">
          {value}
        </p>
        {previousValue && (
          <p className="mt-1 text-xs text-gray-500 dark:text-gray-400">
            de {previousValue} <span className="text-gray-400 dark:text-gray-500">({timeframe})</span>
          </p>
        )}
      </div>
    </article>
  );
};
```

---

#### Receita 3: Accordion Zero-JS em `<details>` com Chevron Animado
Demonstra como o HyperUI resolve acordeões complexos sem uma única linha de JavaScript, aproveitando seletores modernos de grupo do Tailwind.

```html
<!-- Componente: Accordion Zero-JS puro em HTML5 + Tailwind -->
<div class="space-y-4 max-w-xl mx-auto">
  <details 
    class="group rounded-lg border border-gray-200 bg-white p-5 [&_summary::-webkit-details-marker]:hidden dark:border-gray-800 dark:bg-gray-900"
    open
  >
    <summary class="flex cursor-pointer items-center justify-between gap-1.5 text-gray-900 dark:text-white">
      <h4 class="text-base font-semibold">
        Como o HyperUI garante compatibilidade com qualquer framework?
      </h4>

      <span class="relative size-5 shrink-0">
        <!-- Ícone SVG de Chevron que rotaciona via CSS com aceleração por hardware -->
        <svg
          class="size-5 transition-transform duration-300 ease-out group-open:-rotate-180 text-gray-500 dark:text-gray-400"
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
          aria-hidden="true"
        >
          <path stroke-linecap="round" stroke-linejoin="round" d="M19 9l-7 7-7-7" />
        </svg>
      </span>
    </summary>

    <p class="mt-4 leading-relaxed text-sm text-gray-700 dark:text-gray-300 border-t border-gray-100 pt-3 dark:border-gray-800">
      Por utilizar HTML5 semântico nativo e classes utilitárias canônicas do Tailwind CSS, não há dependência de hooks do React, reatividade do Vue ou runtime adicional. Você copia o código e ele funciona de imediato em qualquer servidor ou pipeline.
    </p>
  </details>
</div>
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir o documento de arquitetura de UI/UX de um novo projeto (`DESIGN_BLUEPRINT.md`), utilize as seguintes diretrizes para declarar componentes derivados do **HyperUI**:

### 1. Declaração de Stack & Papel Arquitetural
```markdown
### Component Layer: HyperUI Pattern Architecture
- **Origem dos Padrões**: HyperUI (Mark Mead) — Application UI & Marketing Suites.
- **Estratégia de Implementação**: Pure Utility Copy-Paste (sem dependências NPM proprietárias).
- **Diretriz de Runtime**: Zero-JS prioritário para componentes informativos e de layout; Alpine.js ou wrappers leves React/Radix exclusivamente onde focus trapping WAI-ARIA for exigido por compliance.
```

### 2. Definição da Estética Canônica do Projeto
No blueprint, declare explicitamente se o projeto adota o perfil **Clean Modern** ou **Neobrutalism**:

- **Opção A — Se o projeto for Clean Modern (SaaS B2B, Fintech, Analytics)**:
  - Backgrounds: `bg-white` e `dark:bg-gray-900`
  - Bordas: `border-gray-100` / `dark:border-gray-800`
  - Sombras: `shadow-sm` e `hover:shadow-md`
  - Proibição: Nunca injetar `shadow-[4px_4px_0_0]` nesta variante para manter a sobriedade.

- **Opção B — Se o projeto for Neobrutalista (DevTools, Plataformas Criativas, Web3, Indie Hacker MVPs)**:
  - Bordas: `border-2 border-black` / `dark:border-white`
  - Sombras Duras: `shadow-[4px_4px_0_0] shadow-black`
  - Físicas de Ação: `hover:translate-1 hover:shadow-none`
  - Paleta de Acento: 1 cor pastel de destaque (ex: `bg-yellow-200` para botões principais, `bg-white` para fundos).

### 3. Checklist de Validação para a IA antes de Entregar Código Baseado no HyperUI
Antes de finalizar qualquer tela ou componente extraído do HyperUI, a IA deve verificar obrigatoriamente:
- [ ] O componente inclui rótulos ocultos para leitores de tela (`sr-only`) em indicadores visuais (ex: percentual positivo/negativo, botões com apenas ícones)?
- [ ] O modo escuro (`dark:`) foi devidamente validado com contraste mínimo de 4.5:1 (WCAG AA)?
- [ ] No caso de formulários, todos os inputs possuem `id` correlato ao atributo `for` do `<label>`?
- [ ] Se o componente for um Accordion `<details>`, foi verificado se o contexto exige suporte a navegação por teclado avançada ou se a solução nativa é suficiente?
- [ ] Foram removidas classes legadas de Tailwind v2/v3 caso o projeto já esteja configurado em Tailwind CSS v4?
