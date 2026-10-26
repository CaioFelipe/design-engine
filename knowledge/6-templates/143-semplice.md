---
id: "semplice"
name: "Semplice"
url: "https://www.semplice.com/"
category: "6-templates"
schema_type: "C-galleries"
dna_estetico: ["Swiss Editorial Modernism", "High-Craft Designer Portfolios", "Uncompromising Typographic Hierarchy", "Fluid Drag-and-Drop Grid System", "Minimalist White/Dark Space", "Cinematic Media Storytelling", "Organic Micro-Interactions"]
densidade_informacao: "Media/Narrativa"
impacto_visual: "Editorial/Sofisticado"
custo_computacional: "Baixo a Medio (CSS Grid nativo, CSS Transforms acelerados por hardware e GSAP/Framer Motion otimizados)"
stack_frameworks: ["WordPress (Headless-like Visual Canvas)", "Vanilla JS / ESNext", "GSAP / Framer Motion", "Tailwind CSS", "CSS Grid Level 2", "Custom Web Fonts"]
compatibilidade:
  fontes_ideais: ["Maison Neue (Book, Demi, Bold, Extended Extra Bold)", "NB Architekt", "Saol Display", "Cosi Times", "Avenir Next", "Roboto Mono", "Instrument Serif", "Neue Haas Grotesk"]
  paletas_ideais:
    - "Canvas Puro Studio: #ffffff (White Light) e #000000 (Absolute Pitch Black)"
    - "Superfícies Secundárias Sóbrias: #f5f5f5, #ececec e #111111"
    - "Acento Icônico Semplice Vermilion: #E54927 (Warm Electric Tangerine / Semplice Red)"
    - "Neutros Tipográficos de Apoio: #666666, #999999 e #aaaaaa"
    - "Bordas de Alta Precisão: 1px solid rgba(0, 0, 0, 0.08) em Light / rgba(255, 255, 255, 0.12) em Dark"
  combinacoes_recomendadas:
    - "Tailwind CSS + Framer Motion (ou Motion.dev) para recriar as físicas de cursor follower, reveal de texto e transições de página"
    - "Lenis Smooth Scroll para rolagem inercial luxuosa típica dos sites da Showcase"
    - "Next.js / Vite React com `<smp-container>` custom layouts espelhando a modularidade do Semplice 7"
    - "Self-hosted WOFF2 webfonts otimizadas com preload de subtipos e font-display swap"
  conflitos_esteticos:
    - "Templates pré-fabricados genéricos com cards arredondados infantis (border-radius > 24px) e sombras difusas artificiais"
    - "Layouts caóticos que desrespeitam o alinhamento de 12 colunas ou espaçamentos proporcionais em rem"
    - "Sobrecarga de badges, gradientes neon saturados e micro-cards de features estilo SaaS corporativo"
    - "Scroll hijacking que trava a inércia nativa do usuário de forma invasiva"
    - "Imagens de baixa resolução ou sem tratamento cromático profissional que diminuem o apelo de estúdio de arte"
---

# Semplice — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
███████╗███████╗███╗   ███╗██████╗ ██╗     ██╗ ██████╗███████╗
██╔════╝██╔════╝████╗ ████║██╔══██╗██║     ██║██╔════╝██╔════╝
███████╗█████╗  ██╔████╔██║██████╔╝██║     ██║██║     █████╗  
╚════██║██╔══╝  ██║╚██╔╝██║██╔═══╝ ██║     ██║██║     ██╔══╝  
███████║███████╗██║ ╚═╝ ██║██║     ███████╗██║╚██████╗███████╗
╚══════╝╚══════╝╚═╝     ╚═╝╚═╝     ╚══════╝╚═╝ ╚═════╝╚══════╝
```

---

## 1. DNA Estético & Filosofia de Curadoria (Assinatura Visual & O Que Torna Único)

O **Semplice** (`https://www.semplice.com/`) é a principal plataforma mundial de criação de portfólios e experiências visuais desenvolvida especificamente **"por designers, para designers"**. Fundado pelo designer e diretor de arte austro-alemão **Tobias van Schneider** (ex-Lead Product Designer e Art Director do Spotify em Nova York, fundador do estúdio House of van Schneider e da newsletter *DESK*) em conjunto com o engenheiro **Mike Potter**, o Semplice nasceu como uma resposta de rejeição radical aos construtores visuais padronizados (como Squarespace, Wix ou temas genéricos de WordPress) que aprisionavam criativos em modelos rígidos e composições previsíveis.

Ao contrário de agregadores automáticos de links ou galerias comerciais, o **Semplice Showcase** (`https://www.semplice.com/showcase`) funciona como um museu digital vivo e handpicked curado semanalmente. Nele figuram os portfólios, estúdios independentes, diretores de cinema, fotógrafos conceituais, designers de tipografia e artistas de efeitos visuais mais prestigiados da indústria global — incluindo lendas como **Ash Thorp** (designer e diretor cinematográfico em *The Batman*, *Ghost in the Shell*), **Verena Michelitsch**, estúdio **NotReal**, **Cait Oppermann**, **Daniel Lepik**, **Make Haste Corp**, **Acasso Studio** e ex-designers da Apple, Nike, Google e Pentagram.

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                    THE SEMPLICE CREATIVE CURATION ENGINE                     │
├──────────────────────────────────────────────────────────────────────────────┤
│  [ Elite Global Talent ] ──► [ Curatorial Quality Gate ] ──► [ Showcase Hub ]│
│   • Motion Directors           • Uncompromising Typography    • Site of Week │
│   • Art Directors (NY/Berlin)  • Custom Grid Mastery (12-col) • Live Preview │
│   • Industrial & 3D Studios    • Kinetic Craft & Hover Finesse• Case Studies │
│   • High-Fashion Photographers • Editorial Storytelling Depth • S7 Innovators│
├──────────────────────────────────────────────────────────────────────────────┤
│  PHILOSOPHY: "The portfolio is the designer's ultimate commercial artwork"   │
│  CORE TECH: Headless-like Visual Canvas atop WordPress + Modular Grid Engine │
└──────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 O Que Torna o Semplice Único (Assinatura de Marca)
A assinatura do Semplice reside no **respeito sagrado ao espaço visual e à integridade tipográfica**. O software e os sites gerados por sua comunidade compartilham traços inconfundíveis:

1. **Ruptura Completa com "Templates Prontos"**: No ecossistema Semplice, não existem templates estáticos com dados fictícios onde o usuário troca fotos e textos. Cada página é composta a partir de uma folha em branco estruturada por um grid livre de 12 colunas, blocos mestres (*Master Blocks*) e módulos atômicos (`<smp-container>`, `<smp-row>`, `<smp-column>`).
2. **Tipografia Como Elemento Primário de Arquitetura**: O Semplice trata o texto como uma peça escultórica. Letras com peso estendido (*Extended Extra Bold*), contrastes titânicos entre display serifs elegantes (*Saol Display*, *Cosi Times*) e grotescas neo-suíças (*Maison Neue*, *NB Architekt*, *Neue Haas Grotesk*), e micro-legendas em caixa-alta espaçada com referências técnicas.
3. **Padrões de Portfólio de Alta Frequência (Advanced Portfolio Grids - APG)**: Introduziu convenções universais hoje copiadas por toda a web, como o **Text Grid** (lista de títulos de projetos que revela instantaneamente um canvas de vídeo/imagem fluida ao passar o cursor), o **Split Screen Grid** (coluna de texto descritivo ancorada enquanto os assets visuais deslizam na coluna adjacente), e o **CoverSlider** (apresentações em tela cheia com transições cinematográficas).
4. **Acabamento Artesanal de Estúdio de Design**: Detalhes como divisórias de `1px` pretas sólidas ou sutis, ausência de cantos arredondados excessivos, cursores magnéticos personalizados que exibem mensagens dinâmicas ("VIEW CASE", "DRAG", "SOUND ON") e módulos de comparação *Before/After* para comprovar o rigor do processo criativo.
5. **Autonomia de Código e Propriedade Intelectual**: Sendo auto-hospedado sobre infraestrutura WordPress, liberta os criadores dos ecossistemas fechados (walled gardens) de SaaS, permitindo injeção irrestrita de CSS customizado, shaders WebGL, JavaScript e controle absoluto de dados.

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

### 2.1 Papel Estratégico na Regra 60-30-10 de Design & Movimento
O padrão estético do ecossistema Semplice equilibra os três eixos da regra 60-30-10 com maestria editorial:

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                60-30-10 ARCHITECTURAL BALANCE (SEMPLICE CRAFT)               │
├──────────────────────────────────────────────────────────────────────────────┤
│  60%  SUBSTRATO ESTRUTURAL & ESPAÇO RESPIRÁVEL (The Gallery Floor)           │
│       Fundos monocromáticos absolutos (#ffffff ou #000000), margens de       │
│       3.33rem+, ausência de elementos decorativos supérfluos, ar puro.       │
├──────────────────────────────────────────────────────────────────────────────┤
│  30%  ARQUITETURA DE GRID & PESO TIPOGRÁFICO (Editorial Structural Cadence)  │
│       Blocos de 12 colunas assimétricos, títulos monumentais em Maison Neue  │
│       ou Saol Display, linhas divisórias finas (1px solid), metadados mono.  │
├──────────────────────────────────────────────────────────────────────────────┤
│  10%  CINÉTICA DE ASSINATURA & ACENTO CROMÁTICO (Kinetic Signature)          │
│       Toque vibrante Semplice Vermilion (#E54927), cursor follower magnético,│
│       revelação fluida no hover do Text Grid, máscaras de imagem exponenciais│
└──────────────────────────────────────────────────────────────────────────────┘
```

- **60% da Interface (Substrato Estrutural)**: O fundo atua como o piso imaculado de uma galeria de arte contemporânea em Chelsea ou Berlim. Não existem fundos com ruído caótico ou gradientes arco-íris concorrendo com a obra; a cor predominante é o branco óptico (`#ffffff`) ou o preto breu (`#000000`), garantindo 100% de contraste e foco visual nas peças.
- **30% da Interface (Arquitetura de Grid & Tipografia)**: O ritmo visual é conduzido pela tipografia dramática e pelos alinhamentos milimétricos. Colunas de larguras variadas (ex: 4 colunas para contextualização textual e 8 colunas para exibição do asset em alta resolução), tabelas com bordas nítidas de 1px e metadados técnicos formatados em caixas utilitárias.
- **10% da Interface (Cinética de Assinatura & Acento de Cor)**: O acento inconfundível Semplice Tangerine/Vermilion (`#E54927`), botões de ação com cantos vivos ou pílulas sóbrias, e as microinterações cinéticas calculadas: hover com zoom suave de 1.03x em imagens, cursor dinâmico que rastreia as coordenadas do ponteiro e transições de página fluidas sem flash branco.

### 2.2 Nichos e Tipologias de Projeto Onde Semplice é a Referência Primária
A direção de arte baseada no Semplice deve ser convocada como **Referência Primária de Direção de Arte** nas seguintes situações:

1. **Portfólios de Diretores Criativos, Art Directors & Líderes de Design**: Criativos sêniores que necessitam demonstrar autoridade, bom gosto inatacável e maturidade de portfólio para contratação em agências globais (Wieden+Kennedy, Pentagram, Droga5, R/GA) ou gigantes de tecnologia.
2. **Estúdios de Design de Marca, Identidade Visual & Tipografia**: Empresas que vendem branding de luxo, embalagens artesanais e design de fontes personalizadas, onde a tipografia do próprio site precisa atestar o calibre do serviço.
3. **Escritórios de Arquitetura, Interiores e Design Espacial**: Sites que exibem projetos construídos em fotografias de altíssima escala, necessitando de módulos full-bleed, grades de galeria livres de distrações e plantas técnicas bem diagramadas.
4. **Estúdios de Animação 3D, CGI, VFX & Direção de Cinema**: Profissionais (estilo Ash Thorp ou NotReal) que trabalham com renderizações hiper-realistas, telas em loop de vídeo sem controles intrusivos e case studies em estilo "Behind The Scenes".
5. **Apresentações de Case Studies de UX/UI Profundo**: Narrativas estruturadas que contam o processo completo de uma aplicação, desde a pesquisa e wireframes até o produto final, intercaladas com sliders de *Before/After* e comparações em abas.

### 2.3 Ressonância Emocional & Posicionamento de Marca Percepcionado
Ao navegar em uma interface moldada pelos padrões Semplice, o visitante experimenta:
- **Autoridade Silenciosa**: A marca não precisa gritar ou usar truques visuais baratos para convencer; a qualidade do trabalho e o rigor do layout falam por si.
- **Sofisticação Sem Esforço (*Effortless Luxury*)**: Sensação comparável à leitura de revistas de design de alta categoria (como *Kinfolk*, *Cereal*, *Eye Magazine* ou *Idea Magazine*).
- **Controle Artesanal Absoluto**: Transmite a certeza de que cada espaçamento de 1px, cada entrelinha e cada transição foram meticulosamente afinados à mão por mestres do ofício.

---

## 3. Contraindicações Estéticas & Anti-Padrões (Quando NÃO Usar)

### 3.1 Incompatibilidades Setoriais & Funcionais Críticas
⚠️ **Não utilize a linguagem visual Semplice nos seguintes contextos**:

| Cenário Incompatível | Razão da Rejeição / Perda de Conversão |
| :--- | :--- |
| **Dashboards SaaS & B2B Analytics** | Interfaces analíticas (Datadog, PowerBI, CRM) exigem densidade informacional compacta, tabelas condensadas com dezenas de métricas e botões utilitários de alta densidade; a generosidade de espaço do Semplice tornaria a ferramenta lenta e ineficiente. |
| **E-Commerce de Massa com Catálogo Massivo** | Varejistas com centenas de SKUs (eletrodomésticos, farmácias, supermercados) necessitam de filtros facetados densos, ordenação imediata e cards padronizados compactos; o foco contemplativo do Semplice destruiria a taxa de conversão. |
| **Portais de Notícias Diárias e Tabloides** | Ambientes de jornalismo em tempo real demandam atualização contínua, banners de breaking news e grids utilitários de texto denso, incompatíveis com a pureza minimalista. |
| **Público Não-Iniciado em Convenções Digitais** | Usuários corporativos tradicionais ou públicos com baixa literacia digital podem não compreender o comportamento de um *Text Grid* (onde é preciso passar o mouse para ver o projeto) ou a ausência de botões explícitos com bordas convencionais. |

### 3.2 Armadilhas de Imitação & Anti-Padrões Notórios ("Portfolio Syndrome")
Para evitar uma reprodução caricata ou disfuncional da estética Semplice:

1. **"Portfolio Syndrome" (A Moldura Ofuscando a Pintura)**: Usar transições, tipografias monumentais de 120px e cursores magnéticos tão caóticos que o visitante presta atenção no efeito do site e ignora o trabalho ou produto real do cliente.
2. **Gigantismo Tipográfico Sem Hierarquia**: Adotar tamanhos gigantescos de fonte (`font-size: 8rem`) sem ajustar a altura de linha (`line-height: 0.9` a `0.95`) e o espaçamento negativo entre letras (`letter-spacing: -0.05em`), resultando em quebras de palavras horríveis em telas medianas.
3. **Dependência Crítica de Hover sem Fallback Mobile**: Criar menus e listas onde a informação visual só aparece no evento `onMouseEnter`. Em dispositivos touchscreen (smartphones e tablets), onde o ponteiro físico não existe, a interface se torna muda ou inacessível.
4. **Assets Não Otimizados em Full-Bleed**: Carregar arquivos JPEG/PNG não comprimidos de 15MB sob o pretexto de "qualidade máxima de estúdio", provocando Largest Contentful Paint (LCP) desastroso (> 4.5s) e travando navegadores móveis.
5. **Abuso de Máscaras e Modais**: Forçar o usuário a clicar em dezenas de modais ou transições lentas para obter informações básicas de contato ou ficha técnica do projeto.

---

## 4. Catálogo Detalhado de Componentes, Padrões & Efeitos Notáveis

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo
O motor de layout do Semplice (especialmente na geração **Semplice 7**) é fundamentado em regras geométricas precisas:

- **Largura Base do Container**: Padrão clássico de `1440px` com variações para telas ultrawide (`1680px` ou `100vw` em seções full-bleed).
- **Gutter e Margens Externas**:
  - Gutter de colunas no desktop: `2.222rem` (aproximadamente `40px` em base de 18px).
  - Margem externa de respiro (*outer padding*): `3.333rem` (`60px`).
  - Gutter no mobile: `1.666rem` (`30px`), com margem externa de `1.111rem` (`20px`).
- **Sistema de 12 Colunas Flexíveis**: As colunas Semplice admitem frações inteiras (`col-1` até `col-12`), permitindo combinações assimétricas icônicas (ex: `col-3` para título lateral fixo + `col-9` para galeria deslizante, ou `col-5` / `col-7` para quebrar a simetria monótona).
- **Ritmo Vertical Desacoplado**: Seções nunca usam margens fixas em pixels; utilizam multiplicadores proporcionais em `rem` ou `vh` (`padding-top: 10vh`, `padding-bottom: 12vh`), criando uma respiração quase cinematográfica entre um projeto e o próximo.

```
┌── smp-container (max-width: 1440px / outer: 3.333rem) ────────────────────────┐
│                                                                               │
│  ┌── smp-row (gap: 2.222rem) ──────────────────────────────────────────────┐  │
│  │ ┌── smp-column (col-4) ───────┐ ┌── smp-column (col-8) ──────────────┐  │  │
│  │ │ Project Title & Metadata     │ │ Full-Bleed 16:9 Kinetic Video Loop │  │  │
│  │ │ • Year: 2026                 │ │ or Master Case Study Carousel      │  │  │
│  │ │ • Role: Art Direction        │ │                                    │  │  │
│  │ │ • Client: Nike Special Proj  │ │                                    │  │  │
│  │ └──────────────────────────────┘ └────────────────────────────────────┘  │  │
│  └─────────────────────────────────────────────────────────────────────────┘  │
│                                                                               │
└───────────────────────────────────────────────────────────────────────────────┘
```

### 4.2 Sistemas de Cores, Superfícies, Materiais & Iluminação
A cartela cromática do Semplice privilegia contrastes puros e ausência de ruído:

- **Fundo Canônico**: `#ffffff` (White Mode) ou `#000000` (Pitch Dark Mode). Variações contemplativas usam off-whites minerais como `#fbfbfb` ou `#f5f5f5` para suavizar a luz azul em monitores OLED.
- **Cor de Acento de Marca Semplice**: `#E54927` (International Vermilion / Tangerine Flame). Utilizado estrategicamente em botões de ação primária, bullets selecionados, marcas de categoria ativa e links em hover.
- **Tratamento de Superfícies & Bordas**: Ao contrário de sistemas que aplicam gradientes volumétricos ou sombras difusas, o Semplice adota linhas ortogonais de separação com espessura de exatamente `1px` (`border-bottom: 1px solid #e0e0e0` ou `rgba(255, 255, 255, 0.12)`).
- **Texturas & Mídia**: A única textura tolerada é o grain sutil de película analógica (35mm film grain em 3-5% de opacidade) aplicado sobre fotografias editoriais ou vídeos em loop, conferindo calor humano à precisão digital suíça.

---

### 4.3 Catálogo de Arquétipos Concretos (8 Padrões Estruturais Reais)

#### Arquétipo 1: The Interactive Text Grid (Typographic List with Mouse-Follower Media)
- **Anatomia**: Lista vertical de projetos com títulos em caixa alta ou baixa em escala monumental (ex: `font-size: clamp(2.5rem, 5vw, 6rem)`). Cada item exibe o nome do projeto e sua categoria alinhada à direita. Ao pairar o ponteiro do mouse sobre o texto, um card flutuante contendo imagem ou vídeo em loop de altíssima qualidade é renderizado exatamente nas coordenadas do cursor, acompanhando-o com interpolação inercial elástica (*spring physics*). O texto inativo tem sua opacidade reduzida para `0.25`.
- **Gatilho / Interação**: `onMouseEnter` ativa o `opacity: 1` e `scale(1)` do floating thumbnail; `onMouseMove` repassa as coordenadas com lerp (linear interpolation de 0.08 a 0.12); `onMouseLeave` oculta com desvanecimento suave.
- **Onde Encaixar**: Homepages de estúdios e portfólios que desejam apresentar entre 6 e 15 projetos sem poluir a tela com dezenas de miniaturas estáticas simultâneas.

#### Arquétipo 2: The Advanced Split-Screen Grid (Dual Synchronous Scroll)
- **Anatomia**: Divisão precisa de 50/50 na viewport (`w-full grid grid-cols-1 md:grid-cols-2`). O lado esquerdo permanece colado à viewport (`position: sticky; top: 0; height: 100vh`), apresentando o título tipográfico gigante, sinopse, créditos técnicos e links de navegação entre projetos. O lado direito é uma coluna de rolagem infinita e suave contendo uma cascata de renders, fotografias macro e detalhes do projeto.
- **Gatilho / Interação**: Conforme o usuário rola a coluna da direita, pontos de gatilho (*ScrollTrigger*) no lado direito enviam eventos para o lado esquerdo alterar suavemente o texto ativo ou indicador de progresso através de transições de fade cruzado.
- **Onde Encaixar**: Páginas de projetos profundos (*In-depth Case Studies*) de arquitetura, design industrial ou branding abrangente.

#### Arquétipo 3: The Full-Bleed CoverSlider (Cinematic Fullscreen Hero)
- **Anatomia**: Módulo que ocupa 100% da largura e altura da viewport (`100vw` x `100vh`). Exibe uma mídia imersiva de alta resolução em segundo plano (vídeo MP4 h.264 silencioso ou imagem panorâmica), sobreposta por uma tipografia escultural centralizada ou alinhada ao rodapé. Nas laterais ou canto inferior, números em estilo mono (`01 / 07`) e setas de navegação minimalistas guiam a transição.
- **Gatilho / Interação**: Arrastar com mouse/touch (*drag*) ou scroll horizontal inercial. A transição entre slides utiliza máscaras de corte horizontal (*clip-path wipe*) ou transição com curva `cubic-bezier(0.16, 1, 0.3, 1)`.
- **Onde Encaixar**: Capas de landing pages para produtoras de vídeo, diretores de cinema, estúdios de pós-produção 3D e fotógrafos de moda.

#### Arquétipo 4: The Modular Case Study Breakdown ("Director's Cut" Flow)
- **Anatomia**: Sequenciamento canônico de seções que define os melhores portfólios mundiais:
  1. *Hero Viewport*: Título em 1 linha, subtítulo com a tese do projeto e asset âncora.
  2. *Meta & Role Grid*: 4 colunas (`Role`, `Client`, `Year`, `Impact/Outcome`) separadas por linha de `1px`.
  3. *Full-Width Visual Break*: Imagem panorâmica de 100% de largura que quebra a barreira do container.
  4. *Double Column Zoom*: Dois assets complementares lado a lado com proporções idênticas (`aspect-square` ou `aspect-4/5`).
  5. *Process Commentary*: Bloco editorial estreito (largura máxima de `680px` centralizado ou deslocado) focado na resolução do problema de design.
  6. *Interactive Before/After*: Módulo interativo comparativo.
- **Gatilho / Interação**: Elementos de imagem revelam-se com efeito de máscara suave subindo (`clip-path: inset(100% 0% 0% 0%)` para `inset(0% 0% 0% 0%)`) ao atingirem 20% da janela visível.
- **Onde Encaixar**: Estrutura padrão para páginas de projetos individuais em design digital, branding e arquitetura.

#### Arquétipo 5: The Multi-Column Portfolio Grid with Custom Aspect Ratio
- **Anatomia**: Grid flexível que intercala cards com diferentes razões de aspecto (ex: imagem vertical 4:5 seguida de vídeo horizontal 16:9 e um bloco quadrado 1:1) respeitando a matriz ortogonal de 12 colunas sem gerar desalinhamentos desleixados.
- **Gatilho / Interação**: Ao passar o cursor (*hover*), a imagem sofre um zoom micro-artesanal de `scale(1.025)` com duração de `600ms` e surge um overlay escurecido suave de 15% a 25% revelando título e tags técnicas sem cobrir a beleza da foto.
- **Onde Encaixar**: Vitrines de trabalhos em agências multidisciplinares e portfólios com grande variedade de linguagens visuais (editorial, embalagem, interface, motion).

#### Arquétipo 6: The Interactive Before/After Comparison Module (Studio Edition)
- **Anatomia**: Container de imagem com duas camadas sobrepostas pixel a pixel: a camada base (ex: "Wireframe / Identidade Antiga / Render Cru") e a camada superior (ex: "Interface Final / Nova Identidade / Pós-Produção Finalizada"). Uma linha vertical divisória de `1px` em `#ffffff` com um identificador circular translúcido divide as duas metades.
- **Gatilho / Interação**: O usuário arrasta a barra divisória horizontalmente ou move o mouse sobre o container; a propriedade CSS `clip-path: inset(0 0 0 calc(100% - X%))` atualiza em tempo real a 60/120fps sem engasgos.
- **Onde Encaixar**: Demonstração de processos de redesign, retoque fotográfico de alta precisão, gradação de cor de cinema e modelagem 3D.

#### Arquétipo 7: The Dynamic Header & Fullscreen Floating Split Navigation
- **Anatomia**: Navegação flutuante minimalista composta por uma barra de cabeçalho estreita (`h-16`) com logotipo em tipografia pura ou monograma vetorial à esquerda, links de navegação em caixa alta com micro-tracking (`letter-spacing: 0.1em`) no centro, e botão de ação contrastante Semplice Red (`#E54927`) ou ícone de menu hambúrguer de duas linhas retas à direita.
- **Gatilho / Interação**: Ao clicar no menu, um overlay em tela cheia (`bg-black text-white` ou `bg-white text-black`) surge com revelação em cascata de links gigantescos (`font-size: 4rem`), acompanhados de informações de contato direto e fuso horário do estúdio.
- **Onde Encaixar**: Estrutura global de navegação para qualquer projeto editorial que busque elegância contemporânea.

#### Arquétipo 8: The Infinite Project Footer & Dual-Pane Next/Previous
- **Anatomia**: Rodapé de final de página de case study que elimina becos sem saída na navegação. Divide-se em duas colunas simétricas de altura generosa (`160px` a `240px`): "← PREVIOUS PROJECT" e "NEXT PROJECT →", separadas por uma linha vertical nítida de `1px`.
- **Gatilho / Interação**: Passar o mouse sobre uma das metades transiciona a cor de fundo suavemente (de neutro para o tom de marca do projeto seguinte) e expande o título do próximo case, convidando o visitante a uma jornada contínua e ininterrupta.
- **Onde Encaixar**: Rodapé de todos os projetos detalhados para maximizar a retenção e profundidade de visitação.

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Mapeamento para as Camadas de Design Engine
Para materializar a direção visual e as microinterações do Semplice no ecossistema moderno:

- **Camada 1 (Fundação de Tokens & CSS)**: Tailwind CSS v3/v4 configurado com tokens tipográficos estendidos, escalas modulares e ausência de sombras falsas.
- **Camada 2 (Primitivas & Composição de Layout)**: Componentes modulares `<SmpContainer>`, `<SmpRow>`, `<SmpColumn>` reproduzindo o sistema de 12 colunas e gutters de `2.222rem`.
- **Camada 3 (Orquestração de Micro-Interações & Física)**: **Framer Motion** (ou `motion.dev`) e **GSAP ScrollTrigger** para orquestrar as físicas de inércia, transições de opacidade desacopladas e o cursor follower interativo.
- **Camada 4 (Efeitos Visuais Especializados)**: Shaders de distorção de imagem sutis em Three.js / WebGL para transições entre projetos ou loops de vídeo HTML5 silenciosos.
- **Camada 7 (Performance & Entrega)**: Preload de fontes WOFF2 locais, Next.js Image com WebP otimizado e lazy loading de alta precisão para garantir LCP < 1.2s.

---

### 5.2 Sistema de Variáveis & Tokens CSS Canônicos (Semplice Design Engine Tokens)

```css
:root {
  /* ==========================================================================
     SEMPLICE 7 CORE DESIGN TOKENS
     ========================================================================== */
  
  /* Paleta Cromática Canônica */
  --smp-color-bg: #ffffff;
  --smp-color-bg-alt: #f5f5f5;
  --smp-color-text-primary: #000000;
  --smp-color-text-secondary: #666666;
  --smp-color-text-muted: #999999;
  --smp-color-accent: #E54927; /* Semplice Signature Vermilion */
  --smp-color-border: rgba(0, 0, 0, 0.08);
  --smp-color-border-solid: #000000;

  /* Modificadores para Dark Canvas */
  --smp-color-dark-bg: #000000;
  --smp-color-dark-bg-alt: #111111;
  --smp-color-dark-text-primary: #ffffff;
  --smp-color-dark-text-secondary: #999999;
  --smp-color-dark-border: rgba(255, 255, 255, 0.12);

  /* Arquitetura de Grid & Espaçamento Semplice */
  --smp-grid-width-desktop: 1440px;
  --smp-grid-width-wide: 1680px;
  --smp-grid-outer-desktop: 3.33333rem; /* 60px base 18px */
  --smp-grid-outer-mobile: 1.11111rem;  /* 20px */
  --smp-grid-gap-desktop: 2.22222rem;   /* 40px */
  --smp-grid-gap-mobile: 1.66667rem;    /* 30px */

  /* Tipografia Suíça de Precisão */
  --smp-font-primary: "Maison Neue", "Neue Haas Grotesk", -apple-system, sans-serif;
  --smp-font-display: "Saol Display", "Cosi Times", "Instrument Serif", Georgia, serif;
  --smp-font-mono: "NB Architekt", "Roboto Mono", SFMono-Regular, monospace;

  /* Escala Modular Tipográfica Proporcional */
  --smp-type-h1: clamp(3.5rem, 8vw, 8.5rem);
  --smp-type-h2: clamp(2.5rem, 5.5vw, 5.5rem);
  --smp-type-h3: clamp(1.8rem, 3.2vw, 3rem);
  --smp-type-body: 1.11111rem;
  --smp-type-meta: 0.77778rem;

  /* Físicas de Movimento & Curvas Exponenciais */
  --smp-ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);
  --smp-ease-in-out-smooth: cubic-bezier(0.65, 0, 0.35, 1);
  --smp-spring-stiffness: 280;
  --smp-spring-damping: 24;
}
```

---

### 5.3 Curvas de Interpolação & Parâmetros de Física de Mola (Motion Specifications)

1. **Transição de Revelação de Imagem (Image Mask Reveal)**:
   - Curva: `cubic-bezier(0.16, 1, 0.3, 1)` (*Ease Out Expo*).
   - Duração: `900ms`.
   - Propriedade: `clip-path: inset(0 0 0% 0)` a partir de `clip-path: inset(100% 0 0% 0)`.
2. **Cursor Follower Elástico (Mouse-Tracking Floating Preview)**:
   - Tipo de Motor: Mola amortecida criticamente (*Damped Spring Physics*).
   - `stiffness`: `250` (rigidez suficiente para resposta ágil sem parecer robótica).
   - `damping`: `22` (amortecimento que previne oscilações elásticas exageradas).
   - `mass`: `0.6` (sensação de leveza tátil).
3. **Hover nos Itens de Texto da Lista (Text Grid Focus Effect)**:
   - Elemento Focado: `opacity: 1`, `transform: translateX(12px)`.
   - Elementos Irmãos Desfocados (*Siblings Dimming*): `opacity: 0.2`.
   - Duração: `350ms` via `var(--smp-ease-out-expo)`.

---

### 5.4 Receita de Código Funcional: Componente `SempliceTextGridPortfolio.tsx`
Código completo, modular, responsivo e em produção utilizando **React**, **Tailwind CSS** e **Framer Motion**:

```tsx
import React, { useState, useRef, useEffect } from "react";
import { motion, useSpring, useMotionValue } from "framer-motion";

interface ProjectItem {
  id: string;
  number: string;
  title: string;
  category: string;
  year: string;
  image: string;
  aspect: "landscape" | "portrait";
}

const PROJECTS_DATA: ProjectItem[] = [
  {
    id: "nike-acg",
    number: "01",
    title: "Nike ACG Expedition",
    category: "Art Direction / Spatial Identity",
    year: "2026",
    image: "https://images.unsplash.com/photo-1542291026-7eec264c27ff?auto=format&fit=crop&w=1200&q=85",
    aspect: "landscape",
  },
  {
    id: "monolith-sound",
    number: "02",
    title: "Monolith Acoustic Engine",
    category: "Industrial Design & CGI",
    year: "2025",
    image: "https://images.unsplash.com/photo-1505740420928-5e560c06d30e?auto=format&fit=crop&w=1200&q=85",
    aspect: "portrait",
  },
  {
    id: "kyoto-retreat",
    number: "03",
    title: "Sylvan Residence Kyoto",
    category: "Architecture & Editorial Photography",
    year: "2025",
    image: "https://images.unsplash.com/photo-1493976040374-85c8e12f0c0e?auto=format&fit=crop&w=1200&q=85",
    aspect: "landscape",
  },
  {
    id: "polestar-hmi",
    number: "04",
    title: "Autonomous Vehicle HMI",
    category: "Product Architecture & Typography",
    year: "2024",
    image: "https://images.unsplash.com/photo-1552519507-da3b142c6e3d?auto=format&fit=crop&w=1200&q=85",
    aspect: "landscape",
  },
  {
    id: "verve-magazine",
    number: "05",
    title: "Verve Biannual Issue #04",
    category: "Editorial Design & Custom Type",
    year: "2024",
    image: "https://images.unsplash.com/photo-1544717305-2782549b5136?auto=format&fit=crop&w=1200&q=85",
    aspect: "portrait",
  },
];

export const SempliceTextGridPortfolio: React.FC = () => {
  const [activeProject, setActiveProject] = useState<ProjectItem | null>(null);
  const containerRef = useRef<HTMLDivElement>(null);

  // Coordenadas brutas do mouse
  const mouseX = useMotionValue(0);
  const mouseY = useMotionValue(0);

  // Molas com física amortecida Semplice
  const springConfig = { stiffness: 280, damping: 24, mass: 0.5 };
  const springX = useSpring(mouseX, springConfig);
  const springY = useSpring(mouseY, springConfig);

  const handleMouseMove = (e: React.MouseEvent) => {
    if (containerRef.current) {
      const rect = containerRef.current.getBoundingClientRect();
      mouseX.set(e.clientX - rect.left);
      mouseY.set(e.clientY - rect.top);
    }
  };

  return (
    <section
      ref={containerRef}
      onMouseMove={handleMouseMove}
      className="relative w-full min-h-screen bg-[#ffffff] text-[#000000] py-24 px-6 md:px-14 overflow-hidden select-none font-sans"
    >
      {/* Top Header & Architectural Meta */}
      <header className="max-w-[1440px] mx-auto pb-16 flex flex-col md:flex-row md:items-end justify-between border-b border-black/10 gap-6">
        <div>
          <span className="text-[12px] uppercase tracking-[0.15em] font-mono text-[#E54927] font-semibold">
            [ Semplice Showcase Reference ]
          </span>
          <h1 className="text-4xl md:text-6xl font-normal tracking-[-0.03em] mt-2">
            Selected Works & Direction
          </h1>
        </div>
        <div className="flex items-center gap-8 text-[13px] font-mono text-[#666666]">
          <span>INDEX (05)</span>
          <span>CURATED 2024–2026</span>
          <span className="hidden md:inline">BERLIN / NYC</span>
        </div>
      </header>

      {/* Main Interactive Typographic Text Grid */}
      <div className="max-w-[1440px] mx-auto pt-4 relative">
        <div className="flex flex-col">
          {PROJECTS_DATA.map((project) => {
            const isHovered = activeProject?.id === project.id;
            const isAnyHovered = activeProject !== null;

            return (
              <div
                key={project.id}
                onMouseEnter={() => setActiveProject(project)}
                onMouseLeave={() => setActiveProject(null)}
                className={`group relative py-7 md:py-10 border-b border-black/10 transition-all duration-300 ease-[cubic-bezier(0.16,1,0.3,1)] cursor-pointer flex flex-col md:flex-row md:items-baseline justify-between gap-4 ${
                  isAnyHovered && !isHovered ? "opacity-20 blur-[0.3px]" : "opacity-100"
                }`}
              >
                {/* Left: Project Number + Title */}
                <div className="flex items-baseline gap-6 md:gap-12 transition-transform duration-300 group-hover:translate-x-3">
                  <span className="text-sm md:text-base font-mono text-[#999999] tracking-wider">
                    {project.number}
                  </span>
                  <h2 className="text-3xl sm:text-5xl md:text-7xl font-normal tracking-[-0.04em] leading-[1.05]">
                    {project.title}
                  </h2>
                </div>

                {/* Right: Category, Year & Action Indicator */}
                <div className="flex items-center justify-between md:justify-end gap-6 md:gap-10 text-xs md:text-sm font-mono text-[#666666] transition-transform duration-300 group-hover:-translate-x-2">
                  <span className="uppercase tracking-[0.08em]">{project.category}</span>
                  <span className="text-[#999999]">{project.year}</span>
                  <span className="w-2 h-2 rounded-full bg-[#E54927] opacity-0 group-hover:opacity-100 transition-opacity duration-200" />
                </div>
              </div>
            );
          })}
        </div>
      </div>

      {/* Floating Spring-Interpolated Media Preview (Desktop Cursor Follower) */}
      <motion.div
        aria-hidden="true"
        className="pointer-events-none fixed top-0 left-0 z-50 hidden md:block"
        style={{
          x: springX,
          y: springY,
          translateX: "-50%",
          translateY: "-50%",
        }}
      >
        {activeProject && (
          <motion.div
            initial={{ opacity: 0, scale: 0.85, filter: "blur(6px)" }}
            animate={{ opacity: 1, scale: 1, filter: "blur(0px)" }}
            exit={{ opacity: 0, scale: 0.85, filter: "blur(6px)" }}
            transition={{ duration: 0.35, ease: [0.16, 1, 0.3, 1] }}
            className={`overflow-hidden shadow-2xl bg-black rounded-none border border-black/10 ${
              activeProject.aspect === "portrait"
                ? "w-[300px] h-[400px]"
                : "w-[440px] h-[280px]"
            }`}
          >
            <img
              src={activeProject.image}
              alt={activeProject.title}
              className="w-full h-full object-cover transform scale-105 transition-transform duration-700 ease-out"
            />
            <div className="absolute bottom-3 left-4 right-4 flex justify-between items-center text-[11px] font-mono uppercase tracking-wider text-white bg-black/60 backdrop-blur-md px-3 py-1.5 border border-white/10">
              <span>EXPLORE CASE STUDY</span>
              <span>↗</span>
            </div>
          </motion.div>
        )}
      </motion.div>

      {/* Footer Navigation Bar */}
      <footer className="max-w-[1440px] mx-auto mt-24 pt-8 flex flex-col sm:flex-row items-center justify-between text-xs font-mono text-[#999999] border-t border-black/10 gap-4">
        <div>© 2026 CRAFTED IN ALIGNMENT WITH SEMPLICE 7 SPECIFICATIONS</div>
        <div className="flex gap-6">
          <a href="#about" className="hover:text-black transition-colors">ABOUT STUDIO</a>
          <a href="#contact" className="hover:text-[#E54927] transition-colors">START A PROJECT ↗</a>
        </div>
      </footer>
    </section>
  );
};

export default SempliceTextGridPortfolio;
```

---

### 5.5 Como a IA Deve Pesquisar ao Vivo no Ecossistema Semplice

Quando o agente necessitar pesquisar ao vivo no portal do Semplice para colher referências de projetos específicos, novas edições ou tutoriais técnicos de arquitetura, deve utilizar os seguintes pontos de acesso estruturados:

1. **Galeria Curada de Portfólios Vivos (Showcase Hub)**:
   - URL canônica: `https://www.semplice.com/showcase`
   - Critério de Navegação: O Showcase exibe os projetos destacados semanalmente como *Site of the Week*. Para buscar portfólios de um nicho específico, a busca contextual via web deve cruzar o domínio com a disciplina:
     - `site:semplice.com/showcase "art direction"`
     - `site:semplice.com/showcase "architecture"`
     - `site:semplice.com/showcase "branding"`
     - `site:semplice.com/showcase "motion"`
2. **Especificações Técnicas de Módulos & Features (Edição Semplice 7)**:
   - Visão Geral de Recursos: `https://www.semplice.com/features`
   - Guia de Versão S7: `https://www.semplice.com/v7`
   - O Módulo Advanced Portfolio Grid: `https://www.semplice.com/advanced-portfolio-grid`
   - Sistema de Tipografia Customizada: `https://www.semplice.com/custom-typography`
   - O Módulo Before & After: `https://www.semplice.com/before-after`
   - O Módulo Gallery Grid: `https://www.semplice.com/gallery-grid`
   - Sistema de Blocos Prontos (*Pre-made Blocks*): `https://www.semplice.com/blocks`
   - Construtor de Navegações Personalizadas: `https://www.semplice.com/navigations`
3. **Estudos & Guias de Boas Práticas Editoriais (DESK / Semplice Guides)**:
   - Como Escrever Case Studies de Alto Impacto: `https://www.semplice.com/how-to-write-case-studies-for-your-portfolio`
   - Checklist de Lançamento de Portfólios: `https://www.semplice.com/portfolio-building-checklist`
   - Curadoria das Melhores Foundries Tipográficas: `https://www.semplice.com/favorite-type-foundries`
   - Central de Suporte & Documentação Técnica: `https://help.semplice.com/`

---

## 6. Diretrizes para o DESIGN_BLUEPRINT.md

Ao elaborar um plano de arquitetura de interface e design system que incorpore a identidade e a maturidade de exibição do Semplice, as seguintes diretrizes normativas devem ser seguidas:

### 6.1 Princípios de Decisão de Layout e Grid
- **Adote a Matriz de 12 Colunas com Margens Externas Generosas**: Estabeleça uma largura máxima de container de `1440px` com `outer padding` mínimo de `3.33rem` (`60px`) e gutters de `2.22rem` (`40px`).
- **Respeite o Vazio (Negative Space)**: O espaço negativo nunca é considerado "área vazia a ser preenchida", mas sim o substrato estrutural ativo que confere prestígio e foco às peças exibidas.
- **Evite Contêineres de Vidro Concorrentes**: Dispense o uso excessivo de glassmorphism opaco quando estiver projetando um portfólio editorial; prefira fundos sólidos translúcidos ou superfícies monocromáticas com divisórias de `1px`.

### 6.2 Regras de Tipografia e Escala Proporcional
- **Contraste de Extremos**: Combine um peso tipográfico monumental para títulos (`H1` em `font-size: clamp(3rem, 7vw, 7.5rem)` com `letter-spacing: -0.04em`) com micro-metadados funcionais (`font-size: 0.75rem` em fonte Mono com `letter-spacing: 0.12em`).
- **Altura de Linha Tensa (*Tight Leading*)**: Títulos gigantes devem adotar `line-height` entre `0.9` e `1.05`, evitando vácuos verticais entre linhas quebradas.
- **Tipografia Secundária Neutra**: Textos corridos e parágrafos de contextualização devem limitar-se a uma largura máxima de `680px` (`max-w-prose`) para manter a ergonomia visual de leitura.

### 6.3 Regras de Animação e Comportamento Tátil
- **Curvas Exponenciais Exclusivas**: Proíba terminantemente transições com `ease`, `linear` ou `ease-in-out` convencionais. Utilize sempre a curva `cubic-bezier(0.16, 1, 0.3, 1)` (*Ease Out Expo*) para movimentos refinados que desaceleram suavemente ao chegar ao destino.
- **Molas Amortecidas sem Ressalto Caricato**: Ao configurar o cursor follower ou cards flutuantes, utilize valores de amortecimento crítico (`damping: 24`, `stiffness: 280`, `mass: 0.5`), garantindo que o elemento acompanhe o cursor com fluidez inercial sem chacoalhar de forma descontrolada.
- **Garantia de Paridade Mobile**: Qualquer interação disparada no hover (como a revelação de imagens no Text Grid) deve possuir um layout alternativo estático e elegante no mobile, onde miniaturas reduzidas ou carrosséis touch substituem o tracking do mouse.

### 6.4 Matriz de Decisão: Quando Adotar a Linguagem Semplice no Blueprint
- **Recomendado**: Portfólios pessoais de designers seniores, estúdios de arte e branding, galerias de fotografia arquitetônica, vitrines de direção cinematográfica e apresentações de produtos físicos premium.
- **Desaconselhado**: Sistemas de gestão de banco de dados, painéis de controle hospitalares/financeiros, plataformas de e-commerce transacional de alto volume e ferramentas com exigência prioritária de formulários densos.
