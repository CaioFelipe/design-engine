---
id: "floatui"
name: "Float UI"
url: "https://www.floatui.com/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["SaaS Modern Clean", "Ambient Mesh Aura / Glow Gradients", "Accessible Headless Primitives", "Bilingual LTR/RTL Native", "Fluid Copy-Paste Agility"]
densidade_informacao: "Media"
impacto_visual: "Moderado"
custo_computacional: "Baixo (CSS/Headless)"
stack_frameworks: ["Tailwind CSS v3 & v4", "React / Next.js", "Radix UI", "Vue.js (Radix Vue)", "Svelte (Melt UI)", "HTML5 Semântico / Alpine.js"]
compatibilidade:
  fontes_ideais: ["Inter", "Plus Jakarta Sans", "Geist Sans", "Outfit", "DM Sans"]
  paletas_ideais: ["Indigo & Violet SaaS Accents (Indigo 600 / Violet 500)", "Sky Blue Ambient Glows (Sky 500 / Cyan 400)", "Slate & Zinc Monochromes (Gray 900 / Slate 800)", "Emerald Status Greens (Emerald 500 / 600)"]
  combinacoes_recomendadas: ["Lucide React / Heroicons", "Radix UI Primitives", "Framer Motion", "Tailwind Forms Plugin", "Tailwind Typography Plugin", "Shadcn UI (hibridização estética)"]
  conflitos_esteticos: ["Neobrutalismo agressivo com bordas pretas grossas de 3px e sombras duras sem blur", "Skeuomorfismo retro anos 2000 com chanfros plásticos", "Cyberpunk ultra-saturado com neons ácidos conflitantes com os gradientes suaves"]
---

# Float UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Float UI** (`floatui.com`), concebido e desenvolvido pela organização de tecnologia e produtos digitais **MarsX** (fundada pelo empreendedor em série **John Rush** e liderada tecnicamente no ecossistema de UI por **Mohamed Aït Aider**), consolidou-se como uma das mais expressivas, modernas e acessíveis bibliotecas de componentes e seções completas de código aberto (licença MIT) para **Tailwind CSS**.

Surgindo em um cenário dominado por bibliotecas pagas com assinaturas caras ou ferramentas amarradas a um único ecossistema monolítico de JavaScript, o Float UI propôs uma ruptura estratégica: fornecer blocos de **Application UI** e **Marketing UI** com qualidade visual de nível sênior, **100% gratuitos**, com suporte nativo multi-framework (**React, Vue, Svelte, HTML puro**) e construídos sobre a robustez de acessibilidade das primitivas headless líderes da indústria (**Radix UI** para React, **Radix Vue** para Vue, e **Melt UI** para Svelte).

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                       ARQUITETURA NÚCLEO DO FLOAT UI                        │
├──────────────────────┬───────────────────────────┬──────────────────────────┤
│    TAILWIND UTILITY  │    HEADLESS PRIMITIVES    │   BILINGUAL LTR / RTL    │
│  Classes padronizadas│ Radix UI (React), Radix   │ Arquitetura espelhada    │
│  em Tailwind CSS v3  │ Vue (Vue.js), Melt UI     │ nativa para internacional│
│  e v4 sem lock-in    │ (Svelte) e WAI-ARIA nativo│ ização global completa   │
├──────────────────────┴───────────────────────────┴──────────────────────────┤
│                          FLOAT UI SIGNATURE EFFECTS                         │
│   • Ambient Mesh Glows (back-light blur-[118px] com gradientes angulares)   │
│   • Peer-checked custom controls (CSS puro sem runtime adicional)           │
│   • Micro-interações táteis ágeis (duration-150 com focus rings compensados) │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

### A Assinatura Visual: "Modern Clean SaaS & Ambient Mesh Aura"

A identidade do Float UI diferencia-se imediatamente de soluções genéricas por um equilíbrio cirúrgico entre sofisticação visual e leveza de execução:

1. **O Famoso "Ambient Mesh Glow" (Gradiente Atmosférico Difuso):**
   A marca registrada visual mais imitada do Float UI é o uso pioneiro de orbes e malhas de gradiente difuso posicionadas estrategicamente como back-light sob seções de Hero, Banners e CTAs:
   ```html
   <div 
     class="absolute inset-0 m-auto max-w-xs h-[357px] blur-[118px] sm:max-w-md md:max-w-lg pointer-events-none"
     style="background: linear-gradient(106.89deg, rgba(192, 132, 252, 0.11) 15.73%, rgba(14, 165, 233, 0.41) 15.74%, rgba(232, 121, 249, 0.26) 56.49%, rgba(79, 70, 229, 0.4) 115.91%)"
   ></div>
   ```
   Esse efeito projeta uma iluminação suave e etérea por trás da tipografia em negrito e dos formulários, conferindo às interfaces uma atmosfera "high-tech" e moderna sem a penalidade de processamento de shaders WebGL ou arquivos de vídeo pesados.

2. **Suporte Nativo a LTR e RTL (Right-to-Left) de Primeira Classe:**
   Diferente da esmagadora maioria das bibliotecas ocidentais, o Float UI foi desenhado desde o primeiro dia com suporte bidirecional rigoroso. Chevrons, ícones de navegação, alinhamento de texto e margens contextuais utilizam propriedades e estruturação adequadas para funcionar sem esforço em mercados do Oriente Médio e Norte da África (como Árabe, Hebraico e Farsi), permitindo expansão global imediata sem reescrever estilos.

3. **Primitivas Headless Radix UI Integradas com Estilização Elegante:**
   Componentes interativos complexos (como Menus de Contexto, Diálogos Modais, Selects pesquisáveis, Tabs e Popovers) não utilizam scripts manuais frágeis; eles delegam o foco, o teclado (`ArrowUp`, `ArrowDown`, `Escape`) e os papéis ARIA para **Radix UI** (em React) ou **Radix Vue** / **Melt UI**, enquanto o Tailwind cuida do acabamento visual tátil.

4. **Taticidade de Controles Customizados via CSS Puro (`peer-checked`):**
   Em grupos de seleção (Radio Groups, Checkbox Cards, Toggles), o Float UI domina a técnica de esconder o input real (`sr-only peer`) e estilizar o container visual adjacente através de `peer-checked:ring-2 peer-checked:ring-indigo-600 peer-checked:border-indigo-600`, criando cartões clicáveis elegantes com zero JavaScript para gerenciamento de estado visual.

5. **Ergonomia Cromática e Foco Acessível:**
   A paleta padrão é centrada em tons de azul corporativo e anil (`indigo-600`, `sky-500`), equilibrados contra escalas neutras refinadas (`gray-900`, `gray-800`, `gray-50`). Os anéis de foco adotam a fórmula de alta visibilidade `focus:ring-2 focus:ring-indigo-600 focus:ring-offset-2`, assegurando conformidade estrita com as normas WCAG 2.1 AA.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados

1. **Startups de SaaS B2B, DevTools e Plataformas de IA:**
   Produtos que precisam transmitir autoridade tecnológica e modernidade instantânea em suas páginas públicas e painéis de produto. Os blocos de Hero com Ambient Glow, tabelas de planos comparativas e grades de funcionalidades modulares reduzem semanas de desenvolvimento de front-end para horas.
2. **Produtos Globais com Requisito Bilíngue LTR/RTL:**
   Projetos que necessitam de internacionalização real, especialmente em regiões que demandam escrita da direita para a esquerda (árabe, hebraico). O Float UI é uma das poucas bibliotecas onde cada bloco foi validado em ambas as direções.
3. **Dashboards Administrativos, Portais de Conta & Faturamento:**
   Áreas autenticadas de software que exigem formulários ergonômicos, wizards passo a passo (`steps`), tabelas de gerenciamento de usuários com avatares e seletores de planos com cartões interativos.
4. **Landing Pages de Alta Conversão & Lançamentos Rápidos (MVPs):**
   Empreendedores, agências e desenvolvedores independentes (*indie hackers*) que necessitam montar páginas de vendas completas (Hero + Prova Social + Features + Depoimentos + FAQ + Pricing + Newsletter Footer) com consistência estética impecável e velocidade recorde de copy-paste.
5. **Arquiteturas Multi-Framework Dentro da Mesma Organização:**
   Empresas que possuem partes do ecossistema em React/Next.js e outras em Vue/Nuxt ou SvelteKit podem unificar a linguagem de design utilizando o mesmo código-fonte Tailwind com os equivalentes headless do Float UI.

---

### Papel no Ritmo Visual (A Aplicação da Regra 60-30-10)

O Float UI organiza a hierarquia visual do sistema de maneira clara entre os três pilares da composição:

- **60% — Esqueleto Estrutural & Neutro de Aplicação (A Base Estrutural):**
  Constituído pelos fundos de página neutros (`bg-white` e `bg-gray-900`), sidebars sóbrias, tabelas com linhas divisórias discretas (`divide-y divide-gray-200`), tipografia estruturada (`text-gray-800` / `text-gray-200`) e grids regulares de conteúdo. Cria estabilidade e clareza de leitura.
- **30% — Camada de Navegação, Formulários e Modais (A Taticidade do Fluxo):**
  Composto pelas barras de navegação responsivas (`navbars`), steppers de progresso numerados (`steps`), grupos de radio buttons em cartões, menus dropdown suspensos e modais de diálogo. Fornece ritmo e respostas táteis imediatas às decisões do usuário.
- **10% — Efeito Showstopper / Ambient Glow de Alta Conversão (O Ponto Focal):**
  Reservado para os gradientes ambientais difusos com `blur-[118px]`, botões principais de ação com transições `duration-150` em `bg-indigo-600` ou `bg-sky-500`, badges de versão/lançamento e cartões de preço com destaque de "Popular Plan". Esse ponto de 10% direciona o foco da conversão sem ofuscar as informações essenciais.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

1. **Terminais Financeiros de Altíssima Densidade Numérica (Estilo Bloomberg):**
   O espaçamento arejado, os cantos arredondados (`rounded-lg`) e os paddings generosos do Float UI são otimizados para legibilidade e conversão humana; em sistemas de trading onde centenas de linhas de cotações precisam caber em uma única tela sem rolagem, uma biblioteca utilitária de densidade compacta pura (como Tremor ou data-grids virtuais) é superior.
2. **Identidades Brutalistas ou Neobrutalistas Rígidas:**
   Tentar aplicar os componentes do Float UI em interfaces que exigem contornos pretos grossos de 3px, sombras sólidas sem difusão (`shadow-[4px_4px_0_0]`) e paletas ácidas colide frontalmente com a estética refinada, translúcida e suave da biblioteca.
3. **Aplicações Imersivas 3D / Shaders WebGL / Canvas Contínuos:**
   Aplicações inteiramente orquestradas por Three.js, Canvas 2D ou animações contínuas de viewport com GSAP não se beneficiam de uma estrutura de caixas de fluxo de layout tradicional baseada em seções de marketing e cartões modulares.
4. **Projetos Legados sem Pipeline de Tailwind CSS:**
   Como todo o design system do Float UI se apoia nas classes utilitárias do Tailwind e em seus modificadores dinâmicos, utilizá-lo com CSS manual tradicional exigiria transcrição manual inviável de centenas de utilitários.

---

### ⚠️ Erros Comuns de Exagero & Anti-Padrões:

1. **Multiplicação de Blurs Ambientais Pesados na Mesma Viewport:**
   O efeito `blur-[118px]` com gradientes angulares multicamadas é deslumbrante no Hero, mas empilhar três ou quatro elementos desse tipo ao longo de uma mesma tela em dispositivos móveis modestos pode causar queda sensível na taxa de quadros (FPS) devido ao custo de rasterização de filtros CSS pesados. Restrinja o glow a no máximo 1 ou 2 pontos estratégicos por página.
2. **Quebra de Suporte RTL por Classes de Margem Hardcoded:**
   Ao customizar os componentes do Float UI para mercados multilíngues, evite inserir utilitários físicos fixos como `ml-4` ou `pr-6`. Empregue sempre utilitários lógicos do Tailwind (`ms-4` para margin-start, `pe-6` para padding-end) ou os seletores direcionais adequados para não quebrar a simetria no modo árabe/hebraico.
3. **Abandono de Acessibilidade ao Customizar Inputs Semânticos:**
   Ao adaptar os componentes de formulário com estados `peer`, certifique-se de que os elementos `<input>` mantenham atributos `id` vinculados aos respectivos `<label htmlFor="...">`, e nunca remova a classe `sr-only` sem fornecer outro mecanismo visual acessível para leitores de tela.
4. **Falta de Fallback em Modais sem Focus Trap:**
   Ao utilizar as variações simples de modal que não dependem do Radix UI, certifique-se de implementar o bloqueio de rolagem do body (`overflow-hidden`) e o gerenciamento de retorno de foco ao elemento disparador quando o modal for dispensado.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão **12 componentes emblemáticos** do acervo do Float UI, distribuídos entre as suítes de **Application UI** e **Marketing UI**, demonstrando sua variedade e rigor técnico:

---

### 1. Ambient Glow Hero Section with Inline CTA
- **Anatomia Visual**: Seção de abertura com fundo escuro (`bg-gray-900`), tipografia display centralizada em negrito (`text-4xl text-white font-extrabold md:text-5xl`), texto de apoio em cinza médio (`text-gray-400`), formulário de captura rápida de e-mail integrado e indicador de prova social com estrelas amarelas e contagem de avaliações. Sob o conteúdo, flutua a icônica esfera difusa de luz com `blur-[118px]` e gradiente angular multicamadas (`rgba(192, 132, 252, 0.11)` até `rgba(79, 70, 229, 0.4)`).
- **Gatilho de Interação**:
  - `Input Focus`: Campo de e-mail altera o fundo suavemente de `bg-gray-700` para `bg-gray-900` com transição `duration-150`.
  - `Button Hover/Active`: Botão de Call-To-Action em azul-celeste (`bg-sky-500`) escurece suavemente para `hover:bg-sky-400 active:bg-sky-600`.
- **Onde encaixar na página**: Hero principal de landing pages de SaaS, lançamentos de produtos e ferramentas de inteligência artificial.

---

### 2. Context Menu with Multi-Level Submenus & Keybindings
- **Anatomia Visual**: Construído sobre o `@radix-ui/react-context-menu`. Uma área disparadora sutil com borda tracejada (`border-dashed bg-gray-50`) que, ao receber o clique do botão direito do mouse, projeta um menu flutuante suspenso com cantos arredondados (`rounded-lg bg-white shadow-md border text-[13px] text-gray-800`), ícones SVG embutidos, separadores horizontais (`h-px bg-gray-200`) e atalhos de teclado renderizados à direita (`Ctrl+M`, `Ctrl+C`, `Ctrl+D`). Suporta flyouts laterais para submenus (como listas de plugins).
- **Gatilho de Interação**:
  - `Right-Click / Context Event`: Abre o menu exatamente na coordenada do cursor com offset suave.
  - `Arrow Keys / Hover`: Seleção rápida com destaque azul instantâneo (`data-[highlighted]:bg-blue-600 data-[highlighted]:text-white`).
- **Onde encaixar na página**: Dashboards de gerenciamento de arquivos, ferramentas criativas baseadas em canvas, listas de documentos e gerenciadores de projetos.

---

### 3. Chevrons & Numbers Responsive Step Indicator
- **Anatomia Visual**: Stepper horizontal flexível para processos de onboarding e checkout. Cada etapa é composta por uma esfera circular numerada (`w-8 h-8 rounded-full border-2`), rótulo textual e conectores visuais. No desktop, as etapas são unidas por chevrons SVG horizontais centralizados; no mobile, os conectores alternam automaticamente para setas verticais ou linhas verticais contínuas.
- **Gatilho de Interação**:
  - Estados dinâmicos: Etapas concluídas ganham fundo sólido em anil (`bg-indigo-600 border-indigo-600`) com ícone de checkmark; etapa atual exibe contorno e texto com cor de destaque (`border-indigo-600 text-indigo-600`); etapas futuras permanecem neutras (`text-gray-400`).
- **Onde encaixar na página**: Fluxos de assinatura, processos de KYC/validação de identidade, onboarding de usuários e wizards de configuração de software.

---

### 4. Custom Pricing Cards Radio Group
- **Anatomia Visual**: Grupo de opções de planos apresentado em cartões clicáveis empilhados. Cada item possui uma caixa envolvente com borda suave e fundo branco (`rounded-lg border bg-white shadow-sm p-5`). À esquerda, um indicador circular de rádio customizado em CSS; à direita, título em negrito e descrição do plano.
- **Gatilho de Interação**:
  - `Selection via Peer`: O input de rádio nativo permanece invisível (`sr-only peer`), mas ao ser selecionado aciona no container as classes `peer-checked:ring-2 peer-checked:ring-indigo-600 peer-checked:border-indigo-600`, enquanto o círculo central ganha preenchimento imediato via `peer-checked:border-[5px] peer-checked:border-indigo-600` sem delay de runtime.
- **Onde encaixar na página**: Checkout de assinaturas, modais de upgrade de plano, seleção de métodos de pagamento e formulários de contratação.

---

### 5. Centered Notification & Changelog Banner
- **Anatomia Visual**: Barra horizontal compacta posicionada no topo da página ou da viewport. Fundo neutro com borda inferior sutil ou fundo colorido suave. Apresenta uma pílula de novidade (`badge`) com texto em caixa alta ("NEW", "UPDATE"), frase concisa com o anúncio e um link com sublinhado animado, acompanhado de botão de fechar (`dismiss`) acessível.
- **Gatilho de Interação**:
  - `Hover on Link`: Sublinhado estende-se suavemente ou ganha opacidade total.
  - `Dismiss Click`: Fecha o banner com animação de fade-out e remove o elemento do fluxo de layout.
- **Onde encaixar na página**: Topo absoluto da aplicação ou landing page (acima da Navbar principal) para anúncios de novos recursos, promoções sazonais ou avisos de manutenção.

---

### 6. Multi-Select Menu with Avatars & Search Input
- **Anatomia Visual**: Dropdown de seleção ergonômico construído com Radix UI Select. No estado fechado, exibe o avatar do usuário selecionado com nome e endereço de e-mail. Ao abrir, revela uma janela suspensa com campo de busca no topo (`input` com lupa SVG integrada), permitindo filtrar colaboradores em tempo real. Cada linha da lista exibe avatar circular, nome, e-mail e ícone de checkmark no item ativo.
- **Gatilho de Interação**:
  - `Click / Trigger`: Expande com animação de fade e escala sutil.
  - `Type to Search`: Filtra a lista instantaneamente com debounce visual.
- **Onde encaixar na página**: Painéis de atribuição de tarefas, seletor de responsáveis em cartões de Kanban, compartilhamento de pastas e gerenciamento de equipes.

---

### 7. Interactive Data Table with Avatar Profiles & Manage Modals
- **Anatomia Visual**: Tabela de administração tabular com cabeçalhos alinhados em caixa alta e cinza claro (`text-xs font-semibold uppercase text-gray-600 bg-gray-50`). As linhas de dados contêm fotos de perfil acompanhadas de nome completo e e-mail em tipografia hierárquica, colunas de data formatada, status operacional em badges coloridos (`bg-emerald-50 text-emerald-700` ou `bg-amber-50 text-amber-700`) e coluna lateral com ações rápidas ("Edit", "Delete", "Manage").
- **Gatilho de Interação**:
  - `Row Hover`: Fundo da linha transiciona sutilmente para `hover:bg-gray-50/80`.
  - `Action Click`: Aciona modais de confirmação ou drawers laterais sem desconfigurar a largura das colunas.
- **Onde encaixar na página**: Telas principais de dashboards, gerenciamento de usuários, listagem de clientes e inventário de produtos.

---

### 8. Accessible Modal Dialog with Backdrop Dimming
- **Anatomia Visual**: Diálogo centralizado com overlay escurecido translúcido (`fixed inset-0 bg-black/40 backdrop-blur-xs`), caixa modal com cantos arredondados (`rounded-lg bg-white shadow-xl max-w-lg w-full`), cabeçalho demarcado com botão de fechar ("X"), corpo com texto formatado e rodapé com botões de ação primária e secundária alinhados.
- **Gatilho de Interação**:
  - `Escape Key & Backdrop Click`: Fecha o modal e devolve o foco do teclado para o disparador.
  - `Trap Focus`: O tabulador de teclado navega estritamente entre os botões internos do modal enquanto ele estiver aberto.
- **Onde encaixar na página**: Confirmações de exclusão irreversível, aceite de termos de serviço, formulários de edição rápida e convites de membros para workspace.

---

### 9. Underlined & Sliding Tab Navigation with Count Badges
- **Anatomia Visual**: Barra de abas horizontais com separação limpa. A aba ativa destaca-se por uma linha sólida inferior em azul ou anil (`border-b-2 border-indigo-600 text-indigo-600`), enquanto as inativas permanecem neutras (`text-gray-500 hover:text-gray-700`). Cada aba suporta um pequeno badge numérico ovalado (`rounded-full bg-gray-100 px-2 py-0.5 text-xs text-gray-600`) para indicar contagem de itens não lidos ou tarefas pendentes.
- **Gatilho de Interação**:
  - `Click / Tab Key`: Alterna o conteúdo com transição suave e foca acessivelmente na aba selecionada.
- **Onde encaixar na página**: Cabeçalhos de perfil de usuário, páginas de configurações com múltiplas categorias, visualizações de relatórios (Geral, Faturamento, Segurança).

---

### 10. Social Proof Logo Cloud Grid with Partner Stats
- **Anatomia Visual**: Seção horizontal dedicada a exibir marcas parceiras ou clientes de destaque. Composta por um grid responsivo (`grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-8 items-center justify-center`), com logos vetorizados em SVG monocromático com opacidade calibrada (`opacity-60 hover:opacity-100 transition-opacity`), acompanhados por métricas de autoridade (ex: "Mais de 10.000 equipes confiam na plataforma").
- **Gatilho de Interação**:
  - `Hover`: Logo transiciona de escala ou opacidade com micro-interação sutil.
- **Onde encaixar na página**: Logo abaixo da Hero Section principal ou imediatamente antes da seção de Preços para reforçar credibilidade.

---

### 11. Split Authentication Card with OAuth Integrations
- **Anatomia Visual**: Layout de login/registro limpo. Centraliza um cartão branco sobre fundo neutro ou divide a tela em duas colunas (uma com formulário e outra com depoimento e imagem conceitual). O formulário traz botões de autenticação social em um clique (Google, GitHub, Apple) com borda neutra e SVGs das marcas, divisor com texto "OU", campos de e-mail/senha com validação e botão de envio em destaque.
- **Gatilho de Interação**:
  - `Input Focus`: Bordas dos inputs ativam anel de foco em anil (`focus:border-indigo-600 focus:ring-1 focus:ring-indigo-600`).
- **Onde encaixar na página**: Páginas dedicadas de `/login`, `/register`, `/forgot-password` e modais de login rápido.

---

### 12. Global Responsive Navbar with Mobile Expandable Drawer
- **Anatomia Visual**: Barra de navegação superior fixa ou flutuante com logo da marca, links de navegação com menus dropdown integrados, seletor de idioma/tema e botões de ação ("Entrar", "Criar Conta"). Em telas móveis, oculta os links e exibe um botão de menu hamburguer que se transforma com animação de SVG em um "X" de fechamento, expandindo um menu vertical com espaçamento generoso.
- **Gatilho de Interação**:
  - `Toggle Menu`: Abre e fecha o drawer móvel instantaneamente com transição suave de altura e opacidade.
- **Onde encaixar na página**: Topo absoluto de todas as páginas públicas e da documentação técnica.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup Recomendado

Para utilizar os componentes do Float UI com máxima fidelidade e acessibilidade, o ambiente de desenvolvimento moderno (React 18/19, Next.js 14/15, Vite) deve conter as seguintes dependências instaladas:

```bash
# Primitivas Headless para React (Radix UI)
npm install @radix-ui/react-dialog @radix-ui/react-context-menu @radix-ui/react-select @radix-ui/react-tabs @radix-ui/react-avatar @radix-ui/react-dropdown-menu

# Ícones e utilitários de animação/classes
npm install @heroicons/react lucide-react clsx tailwind-merge framer-motion

# Plugins oficiais do Tailwind CSS
npm install -D @tailwindcss/forms @tailwindcss/typography
```

No arquivo `tailwind.config.js`:
```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./src/**/*.{js,ts,jsx,tsx,mdx}",
    "./components/**/*.{js,ts,jsx,tsx,mdx}",
  ],
  theme: {
    extend: {
      colors: {
        brand: {
          50: '#eef2ff',
          500: '#6366f1',
          600: '#4f46e5',
          700: '#4338ca',
        }
      }
    },
  },
  plugins: [
    require('@tailwindcss/forms'),
    require('@tailwindcss/typography'),
  ],
}
```

---

### Física de Movimento e Parâmetros de Transição

O Float UI adota uma filosofia de animações táteis, eficientes e sem travamento de renderização:
- **Transições de Micro-interação (Botões, Links, Badges):**
  - Duração: `duration-150` ou `duration-200`
  - Curva: `ease-out` (aceleração inicial suave com frenagem natural)
  - Propriedades afetadas: `transition-colors`, `transition-all`, `transition-opacity`
- **Diálogos Modais e Menus de Contexto (Radix UI):**
  - Curva de entrada: `cubic-bezier(0.16, 1, 0.3, 1)` (resposta elástica sutil)
  - Keyframes de abertura:
    - Escala: de `scale-95` para `scale-100`
    - Opacidade: de `opacity-0` para `opacity-100`
    - Duração: `150ms`

---

### Receitas de Código Estruturais e Prontas para Produção

Abaixo estão três receitas completas, testadas e representativas da assinatura do Float UI:

---

#### Receita 1: Ambient Glow Hero Section com Efeito Mesh Blur de Alta Fidelidade
Demonstra como reproduzir com perfeição a atmosfera luminosa e o formulário de conversão característicos do Float UI.

```tsx
import React, { useState } from "react";
import { ArrowRight, Star } from "lucide-react";

export const FloatHeroWithAmbientGlow: React.FC = () => {
  const [email, setEmail] = useState("");

  const handleSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    console.log("Email submetido:", email);
  };

  return (
    <section className="relative overflow-hidden bg-gray-900 py-24 sm:py-32">
      {/* Container de Conteúdo */}
      <div className="relative z-10 mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
        <div className="mx-auto max-w-3xl text-center">
          {/* Badge de Lançamento */}
          <div className="inline-flex items-center gap-x-2 rounded-full border border-gray-700 bg-gray-800/80 px-3 py-1 text-xs font-medium text-gray-300 backdrop-blur-sm">
            <span className="h-1.5 w-1.5 rounded-full bg-sky-400"></span>
            Versão 3.0 lançada oficialmente
            <ArrowRight className="h-3 w-3 text-gray-400" aria-hidden="true" />
          </div>

          {/* Título Principal de Impacto */}
          <h1 className="mt-6 text-4xl font-extrabold tracking-tight text-white sm:text-6xl">
            Construa e dimensione seu SaaS com as melhores ferramentas
          </h1>

          {/* Subtítulo Descritivo */}
          <p className="mt-6 text-lg leading-relaxed text-gray-300">
            Acelere sua engenharia com componentes acessíveis, responsivos e prontos
            para produção. Economize semanas de desenvolvimento de interface.
          </p>

          {/* Formulário Inline de Captura */}
          <form
            onSubmit={handleSubmit}
            className="mt-8 flex flex-col items-center justify-center gap-3 sm:flex-row"
          >
            <input
              type="email"
              required
              value={email}
              onChange={(e) => setEmail(e.target.value)}
              placeholder="Digite seu e-mail corporativo"
              className="w-full max-w-sm rounded-lg border border-gray-700 bg-gray-800/90 px-4 py-3 text-sm text-white placeholder-gray-400 shadow-inner outline-none transition-colors duration-150 focus:border-sky-500 focus:bg-gray-900 focus:ring-2 focus:ring-sky-500/20"
            />
            <button
              type="submit"
              className="inline-flex w-full items-center justify-center gap-x-2 rounded-lg bg-sky-500 px-6 py-3 text-sm font-semibold text-white shadow-md transition-colors duration-150 hover:bg-sky-400 active:bg-sky-600 sm:w-auto"
            >
              Começar Agora
              <ArrowRight className="h-4 w-4" aria-hidden="true" />
            </button>
          </form>

          {/* Prova Social de Avaliações */}
          <div className="mt-8 flex items-center justify-center gap-x-3 text-sm text-gray-400">
            <div className="flex text-amber-400" aria-label="Avaliação 5 estrelas">
              {[...Array(5)].map((_, i) => (
                <Star key={i} className="h-4 w-4 fill-current" aria-hidden="true" />
              ))}
            </div>
            <p>
              <strong className="font-semibold text-white">4.9/5</strong> por mais de 2.500 engenheiros
            </p>
          </div>
        </div>
      </div>

      {/* Assinatura Visual: The Signature Ambient Mesh Glow Orbe */}
      <div
        aria-hidden="true"
        className="pointer-events-none absolute inset-0 m-auto h-[360px] max-w-xs blur-[118px] sm:max-w-md md:max-w-lg lg:max-w-xl"
        style={{
          background:
            "linear-gradient(106.89deg, rgba(192, 132, 252, 0.14) 15.73%, rgba(14, 165, 233, 0.42) 20.74%, rgba(232, 121, 249, 0.28) 56.49%, rgba(79, 70, 229, 0.45) 115.91%)",
        }}
      />
    </section>
  );
};
```

---

#### Receita 2: Custom Pricing Plan Radio Group com Estados `peer-checked`
Demonstra a técnica de controles semânticos de alta performance via Tailwind puro (`peer-checked`), eliminando renderizações pesadas de React.

```tsx
import React, { useState } from "react";
import { Check } from "lucide-react";

interface PricingPlan {
  id: string;
  name: string;
  description: string;
  price: string;
  features: string[];
}

const plans: PricingPlan[] = [
  {
    id: "hobby",
    name: "Hobby Starter",
    description: "Ideal para protótipos, validações rápidas e projetos pessoais.",
    price: "Grátis",
    features: ["Até 3 projetos ativos", "Suporte da comunidade", "Deploy ilimitado"],
  },
  {
    id: "pro",
    name: "Professional Team",
    description: "Para equipes em expansão com demandas avançadas de colaboração.",
    price: "R$ 89/mês",
    features: ["Projetos ilimitados", "Suporte prioritário 24/7", "Analytics em tempo real", "Domínios customizados"],
  },
  {
    id: "enterprise",
    name: "Enterprise Custom",
    description: "Para grandes empresas que exigem SLA dedicado, compliance e segurança.",
    price: "Sob consulta",
    features: ["SSO / SAML 2.0", "Auditoria de logs", "Gerente de contas dedicado", "SLA garantido de 99.9%"],
  },
];

export const FloatPricingRadioGroup: React.FC = () => {
  const [selectedPlan, setSelectedPlan] = useState<string>("pro");

  return (
    <div className="mx-auto max-w-xl px-4 py-12">
      <div className="text-center">
        <h2 className="text-2xl font-bold tracking-tight text-gray-900">
          Escolha o plano ideal para sua infraestrutura
        </h2>
        <p className="mt-2 text-sm text-gray-600">
          Alterne de plano a qualquer momento sem taxas adicionais.
        </p>
      </div>

      <ul className="mt-8 space-y-4" role="radiogroup" aria-label="Opções de Plano">
        {plans.map((plan) => (
          <li key={plan.id}>
            <label
              htmlFor={plan.id}
              className="relative block cursor-pointer select-none"
            >
              {/* Radio Input oculto mas acessível */}
              <input
                type="radio"
                id={plan.id}
                name="pricing_plan"
                value={plan.id}
                checked={selectedPlan === plan.id}
                onChange={() => setSelectedPlan(plan.id)}
                className="peer sr-only"
              />

              {/* Cartão de Fundo Estilizado Reativo */}
              <div className="flex items-start justify-between rounded-xl border border-gray-200 bg-white p-5 shadow-sm transition-all duration-200 peer-checked:border-indigo-600 peer-checked:ring-2 peer-checked:ring-indigo-600 peer-focus-visible:ring-2 peer-focus-visible:ring-offset-2">
                <div className="flex gap-x-4">
                  {/* Custom Dot Indicator em CSS puro */}
                  <div className="relative mt-1 flex h-5 w-5 shrink-0 items-center justify-center rounded-full border border-gray-300 transition-colors peer-checked:border-indigo-600">
                    <span
                      className={`h-2.5 w-2.5 rounded-full bg-indigo-600 transition-transform duration-150 ${
                        selectedPlan === plan.id ? "scale-100" : "scale-0"
                      }`}
                    />
                  </div>

                  <div>
                    <h3 className="font-semibold text-gray-900">{plan.name}</h3>
                    <p className="mt-1 text-sm text-gray-500">{plan.description}</p>
                    
                    <ul className="mt-3 space-y-1.5">
                      {plan.features.map((feature, idx) => (
                        <li key={idx} className="flex items-center gap-x-2 text-xs text-gray-600">
                          <Check className="h-3.5 w-3.5 text-indigo-600" aria-hidden="true" />
                          <span>{feature}</span>
                        </li>
                      ))}
                    </ul>
                  </div>
                </div>

                {/* Preço em Destaque */}
                <span className="shrink-0 text-base font-bold text-gray-900">
                  {plan.price}
                </span>
              </div>
            </label>
          </li>
        ))}
      </ul>
    </div>
  );
};
```

---

#### Receita 3: Context Menu Acessível com Radix UI, Atalhos e Submenus
Demonstra como utilizar as primitivas headless do Radix UI com a assinatura visual refinada do Float UI para menus de contexto de alta ergonomia.

```tsx
import React from "react";
import * as ContextMenu from "@radix-ui/react-context-menu";
import { 
  Share2, 
  Copy, 
  FolderPlus, 
  Trash2, 
  ChevronRight, 
  Layers, 
  ExternalLink 
} from "lucide-react";

export const FloatContextMenuExample: React.FC = () => {
  return (
    <div className="flex h-64 items-center justify-center p-6">
      <ContextMenu.Root>
        {/* Área Disparadora de Contexto */}
        <ContextMenu.Trigger className="flex h-40 w-full max-w-md select-none flex-col items-center justify-center rounded-xl border-2 border-dashed border-gray-300 bg-gray-50/80 p-6 text-center text-sm font-medium text-gray-600 transition-colors duration-150 hover:bg-gray-100">
          <Layers className="mb-2 h-6 w-6 text-gray-400" />
          <span>Clique com o botão direito nesta área</span>
          <span className="text-xs text-gray-400">para abrir o menu de ações</span>
        </ContextMenu.Trigger>

        {/* Portal de Renderização do Menu */}
        <ContextMenu.Portal>
          <ContextMenu.Content
            sideOffset={4}
            align="start"
            className="z-50 min-w-[220px] overflow-hidden rounded-xl border border-gray-200 bg-white p-1.5 text-xs text-gray-800 shadow-lg animate-in fade-in-80 zoom-in-95"
          >
            {/* Item Simples: Compartilhar */}
            <ContextMenu.Item className="group flex cursor-pointer select-none items-center justify-between rounded-lg px-2.5 py-1.5 outline-none transition-colors duration-150 data-[highlighted]:bg-indigo-600 data-[highlighted]:text-white">
              <span className="flex items-center gap-x-2">
                <Share2 className="h-3.5 w-3.5" />
                Compartilhar
              </span>
              <span className="text-[10px] text-gray-400 group-data-[highlighted]:text-indigo-200">
                ⌘S
              </span>
            </ContextMenu.Item>

            {/* Item Simples: Copiar Link */}
            <ContextMenu.Item className="group flex cursor-pointer select-none items-center justify-between rounded-lg px-2.5 py-1.5 outline-none transition-colors duration-150 data-[highlighted]:bg-indigo-600 data-[highlighted]:text-white">
              <span className="flex items-center gap-x-2">
                <Copy className="h-3.5 w-3.5" />
                Copiar Link Público
              </span>
              <span className="text-[10px] text-gray-400 group-data-[highlighted]:text-indigo-200">
                ⌘C
              </span>
            </ContextMenu.Item>

            <ContextMenu.Separator className="my-1 h-px bg-gray-100" />

            {/* Submenu de Exportação / Integrações */}
            <ContextMenu.Sub>
              <ContextMenu.SubTrigger className="group flex cursor-pointer select-none items-center justify-between rounded-lg px-2.5 py-1.5 outline-none transition-colors duration-150 data-[highlighted]:bg-indigo-600 data-[highlighted]:text-white">
                <span className="flex items-center gap-x-2">
                  <FolderPlus className="h-3.5 w-3.5" />
                  Mover para Projeto
                </span>
                <ChevronRight className="h-3.5 w-3.5 text-gray-400 group-data-[highlighted]:text-white" />
              </ContextMenu.SubTrigger>

              <ContextMenu.Portal>
                <ContextMenu.SubContent
                  sideOffset={4}
                  className="z-50 min-w-[180px] overflow-hidden rounded-xl border border-gray-200 bg-white p-1.5 text-xs text-gray-800 shadow-lg animate-in fade-in-80"
                >
                  <ContextMenu.Item className="flex cursor-pointer select-none items-center rounded-lg px-2.5 py-1.5 outline-none transition-colors duration-150 data-[highlighted]:bg-indigo-600 data-[highlighted]:text-white">
                    Design System 2026
                  </ContextMenu.Item>
                  <ContextMenu.Item className="flex cursor-pointer select-none items-center rounded-lg px-2.5 py-1.5 outline-none transition-colors duration-150 data-[highlighted]:bg-indigo-600 data-[highlighted]:text-white">
                    Marketing Q4
                  </ContextMenu.Item>
                  <ContextMenu.Item className="flex cursor-pointer select-none items-center justify-between rounded-lg px-2.5 py-1.5 outline-none transition-colors duration-150 data-[highlighted]:bg-indigo-600 data-[highlighted]:text-white">
                    <span>Novo Workspace</span>
                    <ExternalLink className="h-3 w-3" />
                  </ContextMenu.Item>
                </ContextMenu.SubContent>
              </ContextMenu.Portal>
            </ContextMenu.Sub>

            <ContextMenu.Separator className="my-1 h-px bg-gray-100" />

            {/* Item Destrutivo */}
            <ContextMenu.Item className="group flex cursor-pointer select-none items-center justify-between rounded-lg px-2.5 py-1.5 text-red-600 outline-none transition-colors duration-150 data-[highlighted]:bg-red-600 data-[highlighted]:text-white">
              <span className="flex items-center gap-x-2">
                <Trash2 className="h-3.5 w-3.5" />
                Excluir Registro
              </span>
              <span className="text-[10px] text-red-400 group-data-[highlighted]:text-red-200">
                ⌫
              </span>
            </ContextMenu.Item>
          </ContextMenu.Content>
        </ContextMenu.Portal>
      </ContextMenu.Root>
    </div>
  );
};
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir o documento de especificação e arquitetura de front-end (`DESIGN_BLUEPRINT.md`) para projetos que adotarem padrões derivados do **Float UI**, a IA deve seguir as diretrizes normativas abaixo:

### 1. Declaração Formal da Camada de Componentes
```markdown
### Component System: Float UI Architecture
- **Origem Estética & Padrões**: Float UI (MarsX / Mohamed Aït Aider).
- **Primitivas Interativas**: Radix UI (React) / Melt UI (Svelte) / WAI-ARIA Headless.
- **Abordagem de Estilo**: Tailwind CSS nativo v3/v4 com micro-interações semânticas (`peer-checked`).
- **Suporte de Idioma**: Arquitetura bilíngue simétrica com conformidade nativa LTR / RTL.
```

### 2. Definição do Token de Ambient Mesh Glow
No blueprint do projeto, declare explicitamente a classe e o estilo canônico para o backlight atmosférico da aplicação:
```markdown
### Ambient Lighting Tokens:
- **Hero Mesh Glow**:
  - Container: `pointer-events-none absolute inset-0 m-auto h-[360px] max-w-lg blur-[118px]`
  - Gradiente Canônico: `linear-gradient(106.89deg, rgba(192, 132, 252, 0.12) 15%, rgba(14, 165, 233, 0.40) 20%, rgba(232, 121, 249, 0.25) 55%, rgba(79, 70, 229, 0.42) 115%)`
  - Restrição de Performance: Permitido no máximo 1 instância por viewport para manter 60 FPS estáveis em telas mobile.
```

### 3. Checklist de Validação para a IA antes de Entregar Código
Antes de disponibilizar qualquer tela ou componente construído com padrões do Float UI, verifique obrigatoriamente:
- [ ] **Acessibilidade dos Rádios/Checkboxes**: Se utilizou a técnica `sr-only peer`, todos os inputs contêm atributo `id` estritamente correspondente ao `htmlFor` do `<label>`?
- [ ] **Anéis de Foco Visíveis**: Os botões e elementos interativos possuem `focus:ring-2 focus:ring-indigo-600 focus:ring-offset-2` (ou token correspondente do projeto)?
- [ ] **Conformidade RTL**: As margens e alinhamentos utilizam propriedades lógicas (`ms-*`, `pe-*`, `start-*`, `end-*`) ou chevrons espelháveis caso a aplicação ofereça suporte a idiomas árabes/hebraicos?
- [ ] **Focus Management em Modais**: Se o modal for aberto, o foco inicial vai para o primeiro elemento interativo e o botão de fechar possui `aria-label="Fechar modal"`?
- [ ] **Contraste de Modo Escuro**: Os textos sobre fundos escuros (`bg-gray-900`) mantêm taxa de contraste mínima de 4.5:1 em relação ao cinza de suporte (`text-gray-400` para legendas e `text-white` para títulos)?
