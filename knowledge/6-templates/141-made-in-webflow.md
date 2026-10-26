---
id: "141-made-in-webflow"
name: "Made in Webflow"
url: "https://webflow.com/made-in-webflow"
category: "6-templates"
schema_type: "C-galleries"
dna_estetico: ["Client-First Semantic Architecture", "Timeline Scrub & Parallax (IX2/IX3)", "Dynamic CMS Filtering & Attributes", "Bento Grid SaaS & Editorial Showcases", "Kinetic Micro-Interactions", "Open-Source Cloneable Ecosystem", "No-Code High-Fidelity Engineering"]
densidade_informacao: "Media/Narrativa"
impacto_visual: "Editorial/Sofisticado"
custo_computacional: "Medio (CSS Transforms & IX2) a Alto (Spline 3D Canvas / Three.js / GSAP Scrub)"
stack_frameworks: ["Webflow", "Webflow Interactions 2.0 / IX3", "Finsweet Attributes (Client-First)", "Relume Library", "GSAP / ScrollTrigger", "Lenis Smooth Scroll", "Spline / Three.js", "Lottie / DotLottie", "Tailwind CSS / React (Porting)"]
compatibilidade:
  fontes_ideais: ["Inter", "Plus Jakarta Sans", "Syne", "Cabinet Grotesk", "Clash Display", "General Sans", "Satoshi", "Geist Sans", "Instrument Serif"]
  paletas_ideais:
    - "Dark Craft SaaS: #08080a (Canvas Void), #121216 (Card Surface), #1f1f26 (Elevated Border), #6366f1 (Indigo Accent), #ffffff (High-Contrast Text)"
    - "Clean Enterprise Studio: #fcfcfd (Background Neutral), #ffffff (Pure White Surface), #e5e7eb (Subtle Border), #09090b (Ink Heavy), #2563eb (Royal Blue Callout)"
    - "Warm Editorial Archetype: #0d0d0d (Obsidian), #f4f1ea (Warm Paper White), #d97706 (Amber Spark), rgba(255, 255, 255, 0.08) (Fine Dividers)"
    - "Cyber Glass & Neon Aurora: #050508 (Deep Space), rgba(255, 255, 255, 0.04) (Glass Surface), linear-gradient(135deg, #a855f7, #ec4899, #3b82f6) (Accent Glow)"
  combinacoes_recomendadas:
    - "Finsweet Client-First Style System para nomenclatura estruturada e escalável em projetos complexos"
    - "Webflow Interactions IX2/IX3 sincronizadas com Lenis Smooth Scroll para desaceleração natural de rolagem"
    - "Finsweet Attributes (`fs-cmsfilter`, `fs-cmssort`, `fs-cmsnest`) para manipulação dinâmica de CMS sem recarregar a página"
    - "GSAP + ScrollTrigger via custom code para animações de pin, horizontal scroll e scrub tridimensional de alta precisão"
    - "Spline WebGL / Three.js 3D embeds responsivos integrados com interações de mouse hover e camera rotation"
  conflitos_esteticos:
    - "Divitis crônica: aninhamento excessivo e desordenado de containers (`div-block-1`, `div-block-2`) sem semântica e sem convenções de classe"
    - "Scroll hijacking abrupto que destrói a inércia nativa de navegação em trackpads de alta resolução"
    - "Arquivos Lottie JSON brutos e não otimizados (sem compactação DotLottie) que travam a main thread durante o scroll"
    - "Animações com valores estáticos em pixels (`px`) em vez de unidades relativas (`rem`, `vh`, `vw`, `dvh`), quebrando em telas ultrawide ou mobile"
    - "Ocultação de conteúdo com `opacity: 0` ou `display: none` sem atributos ARIA adequados e sem fallback para `prefers-reduced-motion`"
---

# Made in Webflow — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
 ███╗   ███╗ █████╗ ██████╗ ███████╗    ██╗███╗   ██╗    ██╗    ██╗███████╗██████╗ ███████╗██╗      ██████╗ ██╗    ██╗
 ████╗ ████║██╔══██╗██╔══██╗██╔════╝    ██║████╗  ██║    ██║    ██║██╔════╝██╔══██╗██╔════╝██║     ██╔═══██╗██║    ██║
 ██╔████╔██║███████║██║  ██║█████╗      ██║██╔██╗ ██║    ██║ █╗ ██║█████╗  ██████╔╝█████╗  ██║     ██║   ██║██║ █╗ ██║
 ██║╚██╔╝██║██╔══██║██║  ██║██╔══╝      ██║██║╚██╗██║    ██║███╗██║██╔══╝  ██╔══██╗██╔══╝  ██║     ██║   ██║██║███╗██║
 ██║ ╚═╝ ██║██║  ██║██████╔╝███████╗    ██║██║ ╚████║    ╚███╔███╔╝███████╗██████╔╝██║     ███████╗╚██████╔╝╚███╔███╔╝
 ╚═╝     ╚═╝╚═╝  ╚═╝╚═════╝ ╚══════╝    ╚═╝╚═╝  ╚═══╝     ╚══╝╚══╝ ╚══════╝╚═════╝ ╚═╝     ╚══════╝ ╚═════╝  ╚══╝╚══╝ 
```

## 1. DNA Estético & Filosofia de Curadoria

O **Made in Webflow** (`https://webflow.com/made-in-webflow`) é a galeria oficial, vitrine global e repositório descentralizado de templates, componentes e experiências imersivas desenvolvidas pela comunidade internacional da plataforma Webflow. Mais do que uma simples exibição passiva de screenshots ou protótipos de Figma, a galeria se destaca como uma **plataforma viva de engenharia de software visual aberta (Open-Source Visual Development)**.

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                    THE MADE IN WEBFLOW OPEN-SOURCE ECOSYSTEM                 │
├──────────────────────────────────────────────────────────────────────────────┤
│  [ Visual Design Canvas ] ──► [ Semantic Box Model ] ──► [ 1-Click Clone ]   │
│   • Pixel-Perfect CSS          • Client-First System      • Full Structure   │
│   • Keyframe Timelines         • HTML5 Semantic Tags      • Interactions IX2 │
│   • CMS Collections Data       • Accessible Hierarchy     • Production Code  │
├──────────────────────────────────────────────────────────────────────────────┤
│  RESULT: Inspectable, fully functional production layouts ready for remix    │
└──────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 Critérios de Curadoria & Identidade de Ecossistema
A curadoria do Made in Webflow é impulsionada por uma combinação de moderação técnica pela equipe oficial da Webflow (*Staff Picks*, *Featured Sites*) e relevância algorítmica da comunidade (*Popular*, *Trending*, *Most Cloned*). Os princípios que definem os projetos mais reverenciados da plataforma são:

1. **A Cultura do "Cloneable" (Transparência de Código e Estrutura)**: O grande diferencial que consolidou o Made in Webflow como padrão na indústria é a funcionalidade de clonagem imediata. Profissionais podem abrir qualquer projeto cloneable diretamente dentro do Webflow Designer, inspecionando cada nó do DOM, cada estilo de classe CSS, cada curva de transição de interação (IX2/IX3) e a arquitetura das coleções de CMS dinâmicas.
2. **Sistematização Rigorosa via Frameworks Comunitários**: Os melhores projetos não são construídos com estilos aleatórios. O ecossistema padronizou metodologias globais de desenvolvimento visual, como o **Finsweet Client-First**, o **Lumos Framework** e a **Relume Library**. Esses sistemas impõem regras semânticas de nomenclatura de classes (BEM adaptado para visual dev), réguas universais de espaçamento em unidades relativas (`rem`) e tipografia fluida via `clamp()`.
3. **Motion Baseado em Linha do Tempo e Scroll Scrubbing**: A assinatura visual dos sites da plataforma reside na sincronização milimétrica de elementos com a rolagem do usuário. Usando o motor de interações nativo (Interactions 2.0 / IX3) ou integrações via código com **GSAP ScrollTrigger**, os layouts apresentam *sticky stacking cards*, rotação 3D de elementos de produto, revelação sequencial de tipografia (*staggered character splits*) e transformações tridimensionais em perspectiva.
4. **Hibridismo No-Code / Custom Code Avançado**: Embora concebido em uma interface gráfica de design, o topo da arte no Made in Webflow integra injeções de código customizado: bibliotecas como **Lenis** para suavização cinemática de scroll, **Spline** ou **Three.js** para renderização WebGL em tempo real, **Lottie** para vetores animados e **Finsweet Attributes** para manipulação avançada de dados no cliente sem latência de backend.

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

### 2.1 Papel na Regra 60-30-10 de Design & Movimento
O catálogo do Made in Webflow demonstra a maestria entre rigor estrutural de layout, consistência de componentes de design system e o tempero de movimento interativo:

```
┌──────────────────────────────────────────────────────────────────────────────┐
│             60-30-10 ARCHITECTURAL BALANCE (MADE IN WEBFLOW)                 │
├──────────────────────────────────────────────────────────────────────────────┤
│  60%  ESTRUTURA SEMÂNTICA & BOX MODEL (Semantic Skeleton)                    │
│       Layout em CSS Grid/Flexbox, container-large (max-w: 1280px-1440px),     │
│       padding-global fluído, tipografia base legível com hierarquia H1-H6.   │
├──────────────────────────────────────────────────────────────────────────────┤
│  30%  SISTEMA MODULAR & CARDS (Design System Components)                     │
│       Bento boxes modulares, micro-bisel de 1px, segmented pills, tabs de    │
│       navegação, chips de filtros dinâmicos de CMS, cartões de produto.      │
├──────────────────────────────────────────────────────────────────────────────┤
│  10%  CINÉTICA DE INTERAÇÃO & CLÍMAX (Interaction Delight)                   │
│       Scroll scrub progressivo, sticky pinning cards, hover magnético com    │
│       cursor follower, rotação de 3D embeds e máscaras de revelação de texto.│
└──────────────────────────────────────────────────────────────────────────────┘
```

- **60% da Interface (O Esqueleto Semântico & Box Model)**: Uma fundação de tags semânticas (`<header>`, `<main>`, `<section>`, `<article>`, `<footer>`) montadas sobre um grid padronizado. Espaçamentos consistentes que respeitam o ritmo vertical da página garantem que o conteúdo permaneça perfeitamente legível antes de qualquer efeito visual.
- **30% da Interface (Sistemas Modulares de Componentes & Superfícies)**: Componentes atômicos reutilizáveis construídos sobre convenções como Client-First (`card_component`, `navbar_component`, `button_primary`). As superfícies utilizam fundos neutros com microbordas de `1px solid rgba(255, 255, 255, 0.08)` (em dark mode) ou `1px solid rgba(0, 0, 0, 0.06)` (em light mode), garantindo profundidade sutil e separação tátil.
- **10% da Interface (Cinética de Interação & Ponto Focal)**: As interações que transformam a navegação em uma experiência memorável: revelação sequencial de texto em máscaras de overflow, cartões que empilham com efeito de escala e desfoque à medida que a página rola, e botões magnéticos que atraem o cursor do mouse em áreas interativas.

### 2.2 Cenários Ideais de Projeto
- **Landing Pages de SaaS B2B e Soluções Tecnológicas**: Páginas de conversão que precisam de demonstrações interativas de recursos de software, tabelas comparativas interativas e seções de prova social dinâmicas.
- **Portfólios de Estúdios Criativos, Agências e Diretores de Arte**: Plataformas que demandam transições de tela cinematográficas, navegação horizontal contínua e visualização de estudos de caso ricos em mídia.
- **Diretórios de Conteúdo, Hubs de Recursos e Marketplaces**: Interfaces orientadas a filtros instantâneos sem recarregar a tela, buscas dinâmicas em coleções e paginações contínuas (*infinite scroll*).
- **Apresentação e Lançamento de Hardware / Tech Consumer**: Páginas orientadas a produto com visualização 3D interativa de múltiplos ângulos (Spline), desmontagem de componentes (*exploded view*) vinculada à rolagem do scroll e estatísticas animadas com contadores numéricos.

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

### 3.1 Incompatibilidades de Projeto
- ⚠️ **Portais Governamentais & Serviços Públicos de Alta Acessibilidade (WCAG AAA)**: Projetos que exigem conformidade estrita de baixo consumo de largura de banda, compatibilidade com leitores de tela em modo de alto contraste nativo e operação 100% livre de JavaScript funcional. O excesso de transformações CSS e nós do DOM pode degradar a experiência em tecnologias assistivas mais antigas.
- ⚠️ **Dashboards Analíticos Densos & Aplicações de Entrada de Dados (Data-Entry B2B)**: Ferramentas operacionais de contabilidade, ERPs e consoles de infraestrutura (AWS/GCP-style) onde a prioridade é densidade extrema de informação (linhas compactas de tabelas, atalhos de teclado instantâneos) e onde animações de scroll ou transições de layout causam distração e perda de produtividade.
- ⚠️ **Sistemas Bancários Corporativos e Intranets com CSP Ultra-Restritiva**: Ambientes que barram a execução de scripts em linha (*inline scripts*), fontes de terceiros em CDNs e bibliotecas WebGL em browsers travados por políticas corporativas de segurança de rede.

### 3.2 Armadilhas de Imitação & Anti-Padrões
- ⚠️ **"Divitis" Caótica sem Metodologia de Nomenclatura**: Criar hierarquias com 8 a 12 níveis de `<div>` aninhadas com nomes genéricos gerados automaticamente (`div-block-1`, `div-block-2`, `div-block-3`), tornando a manutenção do código um pesadelo e destruindo a semântica da página.
- ⚠️ **Scroll Hijacking Punitivo**: Forçar a parada do scroll do usuário com *pinning* mal calibrado, impedindo a rolagem suave com trackpad ou criando "dead zones" em telas com alturas reduzidas (notebooks de 13 polegadas).
- ⚠️ **Lotties e Vetores Não Otimizados**: Exportar animações do After Effects com caminhos vetoriais excessivos e imagens bitmap embutidas em JSON de 10MB+, provocando engasgos (*frame drops*) de 60fps para 15fps durante a rolagem mobile.
- ⚠️ **Invisibilidade por Falta de Fallback**: Deixar blocos inteiros de conteúdo com estilo inline `opacity: 0` aguardando um gatilho de scroll JS. Se o JavaScript falhar, for bloqueado ou demorar a carregar em redes 3G, o usuário visualiza uma tela em branco.
- ⚠️ **Ignorar `prefers-reduced-motion`**: Construir transições com deslocamentos em eixos X e Y de centenas de pixels sem fornecer estilos alternativos com foco em simples fade para usuários sensíveis ao movimento vestibular.

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo
A estrutura dos projetos no Made in Webflow é dominada pelo **Client-First Style System** (criado pela Finsweet), que padroniza as convenções de layout da seguinte forma:

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                    CLIENT-FIRST LAYOUT SYSTEM HIERARCHY                      │
├──────────────────────────────────────────────────────────────────────────────┤
│  .page-wrapper                                                               │
│    ├── .main-wrapper                                                         │
│    │     └── .section_[section-name]                                         │
│    │           └── .padding-global                                           │
│    │                 └── .container-large (max-width: 80rem / 1280px)        │
│    │                       └── .padding-section-large (padding y: 7rem)      │
│    │                             └── .layout-grid (12 cols / Bento / 2 cols) │
│    └── .footer                                                               │
└──────────────────────────────────────────────────────────────────────────────┘
```

- **Containers e Margens Laterais Fluidas**: Utilização de `.padding-global` com valores parametrizados em viewport units ou `clamp()`:
  ```css
  .padding-global {
    padding-left: clamp(1.25rem, 5vw, 4rem);
    padding-right: clamp(1.25rem, 5vw, 4rem);
    width: 100%;
  }
  .container-large {
    width: 100%;
    max-width: 80rem; /* 1280px */
    margin-left: auto;
    margin-right: auto;
  }
  ```
- **Escala de Espaçamento Vertical**: Espaçamentos definidos por classes utilitárias semânticas desacopladas da cor de fundo:
  * `.padding-section-small`: `clamp(2.5rem, 5vw, 4rem)` (40px a 64px)
  * `.padding-section-medium`: `clamp(4rem, 8vw, 6rem)` (64px a 96px)
  * `.padding-section-large`: `clamp(6rem, 12vw, 10rem)` (96px a 160px)
- **Grid Modular Assimétrico**: Preferência por CSS Grid com `grid-template-columns: repeat(12, 1fr)` com `gap: 1.5rem` a `2rem`, permitindo composições flexíveis de 8+4 colunas para áreas editoriais, 4+4+4 para recursos e matrizes bento com áreas dinâmicas `span 2` ou `span 3`.

### 4.2 Sistemas de Cores, Superfícies & Texturas
- **Paleta de Base & Contraste**: Em esquemas escuros (*Dark Craft*), o fundo nunca é preto absoluto `#000000`, mas sim tons com matiz frio ou neutro como `#09090b` (Zinc 950), `#08080a` ou `#0e0f12`. Em esquemas claros, adota-se um tom marfim suave (`#faf9f6`) ou cinza suave (`#f8fafc`) para evitar fadiga ocular.
- **Micro-Bisel e Luz Direcional (Craft Elevation)**: Cartões e containers utilizam uma linha sutil de iluminação superior que simula chanfro mecânico de precisão:
  ```css
  .craft-card {
    background: #121215;
    border: 1px solid rgba(255, 255, 255, 0.08);
    box-shadow: 
      inset 0 1px 0 0 rgba(255, 255, 255, 0.12),
      0 12px 32px -8px rgba(0, 0, 0, 0.5);
    border-radius: 1.25rem;
  }
  ```
- **Texturas Orgânicas Sutis**: Camadas de ruído monocromático com opacidade de 2% a 4% (`background-image: url('noise.png'); mix-blend-mode: overlay; pointer-events: none;`) para conferir textura tátil e eliminar bandas em gradientes lineares.

---

### 4.3 Padrões de Seções / Fluxos (8 Arquétipos Reais do Ecossistema)

#### Arquétipo 1: Hero Cinético com Parallax Multi-Layer, Badges Flutuantes e Text Reveal
- **Anatomia**:
  - Eyebrow Badge com gradiente suave e ponto pulsante de status (*Live/Active*).
  - Título H1 imponente em tipografia condensada (Satoshi/Clash Display) com efeito de máscara de revelação sequencial de linha por linha (`overflow: hidden` com spans deslocando de `y: 100%` para `0%`).
  - Parágrafo de apoio equilibrado em 2 colunas responsivas.
  - Dupla de CTAs (Primário com brilho sutil e Secundário com contorno translúcido).
  - Preview de interface ou modelo 3D posicionado em perspectiva isométrica leve com parallax reativo ao movimento do cursor do mouse.
- **Gatilho de Animação**: Gatilho no carregamento da página (*Page Load*) com delay escalonado de 0.08s entre elementos, seguido por listener de `mousemove` com amortecimento suave.
- **Onde Encaixar**: Viewport inicial de SaaS de alta conversão e agências de tecnologia interativa.

#### Arquétipo 2: Sticky Stacking Cards on Scroll (Cartões Empilháveis com Escala Progressiva)
- **Anatomia**:
  - Container pai com altura calculada proporcional ao número de itens (ex: `height: 400vh` para 4 cartões).
  - Wrapper sticky posicionado a `top: 10vh` ou `top: 15vh`.
  - Pilha de 3 a 5 cartões com layouts modulares ricos.
  - Conforme o usuário rola, o cartão ativo fixa no topo da pilha, enquanto os cartões anteriores reduzem suavemente de escala (`scale(0.95)`, `scale(0.90)`), aumentam o desfoque (`filter: blur(4px)`) e escurecem gradualmente.
- **Gatilho de Animação**: Scroll progress scrub (`ScrollTrigger` ou Webflow IX2 scrub vinculado à posição da seção na viewport).
- **Onde Encaixar**: Seções de "Como Funciona", pilares de tecnologia ou apresentação de casos de uso de produtos complexos.

#### Arquétipo 3: Horizontal Scroll Showcase com Scrubbing Vinculado
- **Anatomia**:
  - Container externo de altura estendida (`height: 300vh`).
  - Container interno com `position: sticky; top: 0; width: 100vw; height: 100vh; overflow: hidden;`.
  - Trilho horizontal contínuo (`display: flex; flex-direction: row; width: max-content; gap: 3rem;`).
  - Cards de alta resolução de estudos de caso, métricas de resultados e mockups de tela.
- **Gatilho de Animação**: Mapeamento do scroll vertical do documento para uma translação negativa no eixo X (`transform: translateX(-X%)`).
- **Onde Encaixar**: Galerias de portfólio de projetos, linha do tempo histórica de uma marca ou demonstração sequencial de funcionalidades.

#### Arquétipo 4: Dynamic CMS Filter & Live Search Hub (Finsweet Attributes System)
- **Anatomia**:
  - Barra de busca com input estilizado e debounce de 250ms (`fs-cmsfilter-field="*"`, `fs-cmsfilter-debounce="250"`).
  - Barra de pílulas de categorias horizontais roláveis no mobile com badges indicando a contagem de itens em cada tag.
  - Painel de ordenação com menu dropdown customizado (Mais recentes, Mais populares, A-Z).
  - Coleção de itens em CSS Grid responsivo com transição de opacidade suave e layout recalculado automaticamente.
  - Estado vazio (*Empty State*) elegante exibido quando a combinação de filtros não encontra correspondência, oferecendo botão de reset instantâneo.
- **Gatilho de Animação**: Input change e clique nas tags; animação de transição CSS de cards de entrada/saída.
- **Onde Encaixar**: Bibliotecas de templates, repositórios de artigos, diretórios de vagas e vitrines de produtos.

#### Arquétipo 5: Bento Grid Interativo com Spotlight Hover e Glow Radial
- **Anatomia**:
  - Grid assimétrico de 3 colunas e 2 linhas com spans variados:
    * Card 1 (Span 2 colunas, 1 linha): Destaque principal com vídeo loop ou gráfico interativo.
    * Card 2 (Span 1 coluna, 1 linha): Métrica de alta performance com contador numérico animado.
    * Card 3 (Span 1 coluna, 1 linha): Card de integração com ícones de ferramentas conectadas.
    * Card 4 (Span 2 colunas, 1 linha): Interface simulada de produto com abas ativas.
  - Efeito de iluminação radial: Um pseudo-elemento `::before` ou gradiente dinâmico posicionado nas coordenadas exatas `(clientX, clientY)` do mouse relativo ao card, iluminando as bordas e a superfície no cursor.
- **Gatilho de Animação**: Evento `onMouseMove` com variáveis CSS `--mouse-x` e `--mouse-y`.
- **Onde Encaixar**: Seção central de funcionalidades de plataformas SaaS e produtos digitais modernos.

#### Arquétipo 6: Walkthrough Interativo com Sticky Visual e Steps Acionados por Scroll
- **Anatomia**:
  - Layout dividido em 2 colunas:
    * Coluna Esquerda (ou Direita): Conteúdo textual com 3 a 4 blocos de etapas numeradas, cada uma com altura de `80vh` a `100vh`.
    * Coluna Oposta: Painel fixo (`sticky; top: 20vh; height: 60vh;`) exibindo o preview dinâmico da interface.
  - Conforme a etapa de texto cruza a linha de leitura da viewport (ex: 50% da altura da tela), a tela sticky transiciona de estado de maneira fluida (troca de tela do app, animação de dados ou rotação de elemento).
- **Gatilho de Animação**: Gatilho de visibilidade de scroll (*In View Trigger*) que ativa classes de estado ou aciona timeline de animação.
- **Onde Encaixar**: Demonstrações guiadas de fluxos de usuário, pipelines de automação ou tour de recursos de software.

#### Arquétipo 7: Fullscreen Navigation Overlay com Staggered Menu Links & Media Hover Preview
- **Anatomia**:
  - Botão de acionamento do menu (hamburger com transformação geométrica de 2 linhas para 'X').
  - Overlay de tela cheia com fundo escuro profundo e efeito de desfoque de fundo (`backdrop-filter: blur(20px)`).
  - Coluna de links de navegação em caixa alta com tipografia display generosa (`clamp(2.5rem, 6vw, 5rem)`).
  - Área lateral dedicada a um container de imagem que altera instantaneamente o preview de mídia de acordo com o link sobre o qual o cursor do usuário passa.
- **Gatilho de Animação**: Clique no botão menu aciona timeline de abertura; hover sobre os links aciona transição de imagem com máscara rápida e fade suave.
- **Onde Encaixar**: Sites de estúdios criativos, agências de branding e sites institucionais de alto padrão estético.

#### Arquétipo 8: Magnetic CTA Footer com Micro-Interações Líquidas e FAQ em Acordeão
- **Anatomia**:
  - Seção superior com lista expansível de perguntas frequentes (FAQ em acordeão) com animação suave de altura de `0` a `auto` e rotação do ícone em 45°.
  - Grande bloco de chamada para ação com título persuasivo e botão magnético central de dimensões expressivas. O botão desloca sutilmente em direção ao ponteiro do mouse quando o cursor se aproxima a menos de 50px de sua borda.
  - Rodapé inferior com links utilitários, indicação de timezone/status de disponibilidade de trabalho e copyright com tipografia monoespaçada discreta.
- **Gatilho de Animação**: Interação magnética baseada na distância euclidiana do mouse e transições de acordeão via CSS transitions com `grid-template-rows: 0fr -> 1fr`.
- **Onde Encaixar**: Fechamento de página em landing pages de produtos e páginas de serviços profissionais.

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Como Traduzir Usando as Camadas do Ecossistema
- **Camada 1 (CSS Tokens / Tailwind)**: O sistema de classes semânticas do Client-First é traduzido diretamente para configurações do Tailwind com tokens estritos para containers, paddings de seção e tipografia fluida.
- **Camada 2 (Framer Motion / Motion.dev)**: Substitui as interações do Webflow IX2 com muito maior performance, fornecendo controle por `useScroll`, `useTransform` e `springs` com amortecimento crítico sem a sobrecarga do runtime do Webflow.
- **Camada 3 (Lenis Smooth Scroll)**: Provê a suavidade de inércia essencial que torna os efeitos de *scrubbing* e *pinning* idênticos aos melhores sites premiados desenvolvidos na plataforma.
- **Camada 4 & 7 (Three.js / Spline & Ícones Lucide)**: Fornece componentes 3D interativos e ícones com proporção precisa de traço de 1.5px a 2px.

### 5.2 Tokens CSS & Layout Recipe (Client-First Webflow Architecture)

```css
:root {
  /* Escala de Containers & Espaçamentos Globais */
  --container-max-width: 80rem; /* 1280px */
  --container-large-width: 90rem; /* 1440px */
  --padding-global: clamp(1.25rem, 5vw, 4rem);
  --section-padding-large: clamp(5rem, 10vw, 8rem);
  --section-padding-medium: clamp(3.5rem, 7vw, 5rem);
  --section-padding-small: clamp(2rem, 4vw, 3rem);

  /* Superfícies & Cores Dark Craft */
  --bg-void: #08080a;
  --bg-surface: #121215;
  --bg-elevated: #1a1a20;
  --border-subtle: rgba(255, 255, 255, 0.08);
  --border-highlight: rgba(255, 255, 255, 0.16);
  --text-primary: #ffffff;
  --text-secondary: #9ca3af;
  --text-tertiary: #6b7280;
  --accent-primary: #6366f1;
  --accent-glow: rgba(99, 102, 241, 0.25);

  /* Curvas de Animação de Assinatura Webflow */
  --ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);
  --ease-in-out-circ: cubic-bezier(0.85, 0, 0.15, 1);
  --spring-snappy: cubic-bezier(0.34, 1.56, 0.64, 1);
}

/* Utilitários de Estrutura Client-First */
.page-wrapper {
  position: relative;
  width: 100%;
  min-height: 100vh;
  background-color: var(--bg-void);
  color: var(--text-primary);
  overflow-x: clip;
}

.padding-global {
  padding-left: var(--padding-global);
  padding-right: var(--padding-global);
  width: 100%;
}

.container-large {
  width: 100%;
  max-width: var(--container-max-width);
  margin-left: auto;
  margin-right: auto;
}

.padding-section-large {
  padding-top: var(--section-padding-large);
  padding-bottom: var(--section-padding-large);
}

/* Micro-Bisel de Borda Elevada */
.craft-border {
  border: 1px solid var(--border-subtle);
  box-shadow: inset 0 1px 0 0 var(--border-highlight);
}
```

---

### 5.3 Receita de Código Funcional em React + Tailwind CSS + Framer Motion
Abaixo está a implementação de produção do padrão mais icônico do ecossistema Webflow: o **Sticky Stacking Cards on Scroll**, que empilha cartões modulares com redução proporcional de escala, aplicação de desfoque progressivo e efeito de profundidade conforme o usuário rola a página.

```tsx
import React, { useRef } from "react";
import { motion, useScroll, useTransform, MotionValue } from "framer-motion";
import { ArrowUpRight, Sparkles, Layers, Cpu, ShieldCheck } from "lucide-react";

interface CardData {
  id: number;
  title: string;
  tagline: string;
  description: string;
  icon: React.ElementType;
  badge: string;
  stats: { label: string; value: string };
  gradient: string;
}

const CARDS_DATA: CardData[] = [
  {
    id: 1,
    title: "Client-First Architecture",
    tagline: "Padronização de Classes & Tokens Globais",
    description:
      "Construção modular baseada no padrão semântico mais respeitado do ecossistema visual. Nomenclatura previsível, tipografia fluida e responsividade nativa sem classes caóticas.",
    icon: Layers,
    badge: "System Core",
    stats: { label: "Consistência de CSS", value: "100%" },
    gradient: "from-indigo-500/20 via-purple-500/10 to-transparent",
  },
  {
    id: 2,
    title: "Scrubbed Timeline Motion",
    tagline: "Interações Vinculadas ao Scroll da Viewport",
    description:
      "Transformações cinemáticas em 60fps sincronizadas com a inércia do scroll. Sem pulos de renderização, com aceleração suave e desaceleração exponencial para máximo conforto de leitura.",
    icon: Sparkles,
    badge: "Physics Engine",
    stats: { label: "Frame Rate", value: "60 FPS" },
    gradient: "from-blue-500/20 via-cyan-500/10 to-transparent",
  },
  {
    id: 3,
    title: "Dynamic Attributes Engine",
    tagline: "Filtragem e Busca em Tempo Real no Cliente",
    description:
      "Manipulação de coleções de dados sem necessidade de recarregar a tela. Filtros combinados, ordenação instantânea e estados de carregamento imperceptíveis.",
    icon: Cpu,
    badge: "Data Layer",
    stats: { label: "Latência de Busca", value: "< 16ms" },
    gradient: "from-emerald-500/20 via-teal-500/10 to-transparent",
  },
  {
    id: 4,
    title: "Accessible Motion Fallbacks",
    tagline: "Respeito Estrito a Prefers-Reduced-Motion",
    description:
      "Arquitetura de acessibilidade que desativa deslocamentos volumétricos e substitui animações cinéticas por transições de opacidade instantâneas para navegação segura e inclusiva.",
    icon: ShieldCheck,
    badge: "Accessibility",
    stats: { label: "Conformidade", value: "WCAG AA" },
    gradient: "from-amber-500/20 via-orange-500/10 to-transparent",
  },
];

interface CardProps {
  card: CardData;
  index: number;
  totalCards: number;
  progress: MotionValue<number>;
}

const StackingCard: React.FC<CardProps> = ({ card, index, totalCards, progress }) => {
  const cardRef = useRef<HTMLDivElement>(null);

  // Intervalo do scroll correspondente a este cartão
  const cardStart = index / totalCards;
  const cardEnd = (index + 1) / totalCards;

  // Escala decrescente à medida que os cartões subsequentes chegam ao topo
  const scale = useTransform(
    progress,
    [cardStart, cardEnd],
    [1, 1 - (totalCards - index - 1) * 0.04]
  );

  // Desfoque progressivo para criar profundidade de campo nos cartões anteriores
  const blur = useTransform(
    progress,
    [cardStart, cardEnd],
    [0, (totalCards - index - 1) * 2]
  );

  // Escurecimento sutil
  const opacity = useTransform(
    progress,
    [cardStart, cardEnd],
    [1, index === totalCards - 1 ? 1 : 0.85]
  );

  const IconComponent = card.icon;

  return (
    <div
      ref={cardRef}
      className="sticky top-28 w-full flex items-center justify-center mb-12 last:mb-0"
    >
      <motion.div
        style={{
          scale,
          opacity,
          filter: `blur(${blur}px)`,
        }}
        className={`relative w-full max-w-4xl rounded-3xl bg-[#121216] border border-white/10 p-8 sm:p-12 shadow-2xl overflow-hidden transition-colors duration-300`}
      >
        {/* Luz Direcional de Borda Superior (Micro-Bisel) */}
        <div className="absolute inset-x-0 top-0 h-px bg-gradient-to-r from-transparent via-white/20 to-transparent" />

        {/* Gradiente de Fundo do Card */}
        <div
          className={`absolute inset-0 bg-gradient-to-br ${card.gradient} pointer-events-none opacity-40`}
        />

        <div className="relative z-10 flex flex-col md:flex-row md:items-center justify-between gap-8">
          {/* Coluna de Conteúdo */}
          <div className="space-y-4 max-w-xl">
            <div className="flex items-center gap-3">
              <span className="inline-flex items-center gap-1.5 px-3 py-1 rounded-full text-xs font-medium tracking-wide uppercase bg-white/5 border border-white/10 text-indigo-300">
                <IconComponent className="w-3.5 h-3.5 text-indigo-400" />
                {card.badge}
              </span>
              <span className="text-xs font-mono text-zinc-500">
                0{card.id} / 0{totalCards}
              </span>
            </div>

            <h3 className="text-2xl sm:text-3xl font-bold tracking-tight text-white">
              {card.title}
            </h3>

            <p className="text-sm font-medium text-indigo-400">
              {card.tagline}
            </p>

            <p className="text-sm leading-relaxed text-zinc-400">
              {card.description}
            </p>

            <div className="pt-2 flex items-center gap-6">
              <div>
                <div className="text-xl font-bold font-mono text-white">
                  {card.stats.value}
                </div>
                <div className="text-xs text-zinc-500">
                  {card.stats.label}
                </div>
              </div>
            </div>
          </div>

          {/* Coluna Visual / Ação */}
          <div className="flex flex-col items-end justify-between self-stretch">
            <div className="w-14 h-14 rounded-2xl bg-white/5 border border-white/10 flex items-center justify-center text-white/70 group-hover:text-white transition-colors">
              <IconComponent className="w-7 h-7" />
            </div>

            <button className="mt-8 md:mt-0 inline-flex items-center gap-2 px-5 py-2.5 rounded-full text-xs font-semibold text-white bg-white/10 hover:bg-white/20 border border-white/10 transition-all hover:scale-105 active:scale-95">
              <span>Explorar Arquitetura</span>
              <ArrowUpRight className="w-3.5 h-3.5" />
            </button>
          </div>
        </div>
      </motion.div>
    </div>
  );
};

export const WebflowStackingCardsSection: React.FC = () => {
  const containerRef = useRef<HTMLDivElement>(null);
  const { scrollYProgress } = useScroll({
    target: containerRef,
    offset: ["start start", "end end"],
  });

  return (
    <section
      ref={containerRef}
      className="relative w-full bg-[#08080a] py-24 sm:py-32 px-4 sm:px-6 lg:px-8"
      style={{ height: `${CARDS_DATA.length * 100}vh` }}
    >
      <div className="max-w-7xl mx-auto">
        {/* Header Fixo / Seção Introdutória */}
        <div className="text-center max-w-2xl mx-auto mb-16 space-y-4">
          <div className="inline-flex items-center gap-2 px-3 py-1 rounded-full text-xs font-medium text-zinc-400 bg-zinc-900 border border-zinc-800">
            <span className="w-2 h-2 rounded-full bg-indigo-500 animate-pulse" />
            Padrões de Engenharia Visual
          </div>
          <h2 className="text-3xl sm:text-5xl font-extrabold tracking-tight text-white">
            Padrões de Referência Made in Webflow
          </h2>
          <p className="text-base text-zinc-400">
            Desconstrução técnica dos componentes mais clonados da comunidade,
            traduzidos para arquitetura React moderna e motion sustentável.
          </p>
        </div>

        {/* Pilha de Cartões Fixos com Scrubbing */}
        <div className="relative">
          {CARDS_DATA.map((card, index) => (
            <StackingCard
              key={card.id}
              card={card}
              index={index}
              totalCards={CARDS_DATA.length}
              progress={scrollYProgress}
            />
          ))}
        </div>
      </div>
    </section>
  );
};

export default WebflowStackingCardsSection;
```

---

### 5.4 Como a IA Deve Pesquisar ao Vivo no Made in Webflow

Para obter inspirações em tempo real, examinar novos cloneables ou pesquisar componentes específicos durante a geração de interfaces, a IA deve utilizar a estrutura semântica de URLs do Webflow:

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                    MADE IN WEBFLOW URL QUERY BLUEPRINT                       │
├──────────────────────────────────────────────────────────────────────────────┤
│  Base URL: https://webflow.com/made-in-webflow                               │
│                                                                              │
│  1. BUSCA POR CLONEABLES COM TERMO ESPECÍFICO:                               │
│     https://webflow.com/made-in-webflow/search?query=[termo]&cloneable=true  │
│                                                                              │
│  2. FILTROS POR TAGS ESSENCIAIS DE ENGENHARIA VISUAL:                        │
│     • Interactions / Motion:   /made-in-webflow/tag/interactions             │
│     • Client-First System:     /made-in-webflow/tag/client-first             │
│     • Dynamic CMS Filters:     /made-in-webflow/tag/cms-filter               │
│     • GSAP Scroll Animations:  /made-in-webflow/tag/gsap                     │
│     • Bento Grid Layouts:      /made-in-webflow/tag/bento-grid               │
│     • 3D Spline Embeds:        /made-in-webflow/tag/spline                   │
│     • Mega Menus:              /made-in-webflow/tag/mega-menu                │
│                                                                              │
│  3. ORDENAÇÃO DE RELEVÂNCIA & POPULARIDADE:                                  │
│     • Mais Clonados / Populares:  ?sort=popular                              │
│     • Seleção da Equipe Webflow:  ?sort=featured                             │
│     • Últimos Lançamentos:        ?sort=recent                               │
└──────────────────────────────────────────────────────────────────────────────┘
```

- **Query Recomendada para Componentes Específicos**:
  * Para Sticky Cards: `https://webflow.com/made-in-webflow/search?query=stacking%20cards&cloneable=true`
  * Para Marquee Infinito: `https://webflow.com/made-in-webflow/search?query=infinite%20marquee&cloneable=true`
  * Para Filtros de CMS: `https://webflow.com/made-in-webflow/search?query=finsweet%20attributes&cloneable=true`
  * Para Portfólios Editoriais: `https://webflow.com/made-in-webflow/search?query=editorial%20portfolio&sort=featured`

---

## 6. Diretrizes para o DESIGN_BLUEPRINT.md

Ao incorporar a estética e a mentalidade do **Made in Webflow** em um projeto:

1. **Adote o Princípio da Transparência Estrutural (Box Model First)**:
   - Toda seção deve começar com um container semântico e estruturado (`padding-global` e `container-large`).
   - Evite margens flutuantes arbitrárias; dimensione espaçamentos em blocos consistentes de 4px/8px convertidos para `rem`.
2. **Sistematize o Motion com Respeito à Física**:
   - Animações de entrada e transições de cards devem usar curvas exponenciais de desaceleração (`cubic-bezier(0.16, 1, 0.3, 1)`).
   - Movimentos vinculados ao scroll devem empregar bibliotecas com suavização inercial (como Lenis) para evitar a sensação de "travamento" mecânico.
3. **Mantenha os Componentes Modulares & Cloneáveis**:
   - Separe cada componente de forma autônoma: separe estilo estrutural, lógica de microinteração e dados injetados.
   - Forneça sempre atributos de acessibilidade (ARIA labels, focus outlines, roles de botão e suporte obrigatório a `prefers-reduced-motion`).
4. **Equilíbrio Entre Sofisticação Visual e Desempenho (60fps Target)**:
   - Prefira manipular propriedades aceleradas por GPU (`transform`, `opacity`, `filter`).
   - Evite animar propriedades de layout (`width`, `height`, `top`, `left`, `margin`), que provocam reflows custosos na renderização da página.
