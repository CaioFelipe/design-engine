---
id: "siteinspire"
name: "Siteinspire"
url: "https://www.siteinspire.com/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico:
  - "Swiss International Typographic Style"
  - "Austere Architectural Grid & 1px Hairline Systems"
  - "Quiet Luxury & High-Fashion Editorial Curation"
  - "Extreme Negative Space & Visual Breathing Room"
  - "Subdued Monochromatic & Warm Gallery Stone Canvas"
  - "Anti-Gimmick Functional Craftsmanship"
  - "Dual-View Archival Navigation (Grid vs. Dense Index Table)"
densidade_informacao: "Baixa/Contemplativa a Media/Narrativa"
impacto_visual: "Minimalista/Silencioso & Editorial/Sofisticado"
custo_computacional: "Baixo a Moderado (Zero WebGL, CSS Grid nativo, Flexbox, SSR/SSG, tipografia WOFF2 otimizada, micro-interações de 150-250ms com aceleração por GPU, zero layout shifts)"
stack_frameworks:
  - "Next.js (App Router / SSR / SSG)"
  - "React 19 / TypeScript"
  - "Tailwind CSS v3/v4 (arbitrary values, subgrid, hair-lines)"
  - "Framer Motion / Motion.dev (molas com alto damping, transições instantâneas de opacidade)"
  - "Radix UI / Headless UI (estruturas despidas de ornamentos)"
  - "Shopify Storefront API / Sanity.io / Craft CMS (para catálogos editoriais de luxo)"
compatibilidade:
  fontes_ideais:
    - "Grotesk Suíço Autêntico & Neo-Grotesk Arquitetural: Neue Haas Grotesk, PP Neue Montreal, Univers, Helvetica Now, Suisse Int'l, Akzidenz-Grotesk, Folio, Söhne"
    - "Serif Clássico Editorial & Tipografia de Fundação: Bradford, Lyon Display, Caslon, Garamond Premier Pro, Plantin, GT Sectra, Ogg, Cormorant Garamond"
    - "Monoespaçada de Colofão & Catalogação Técnica: PP Neue Machina, Aperçu Mono, GT America Mono, Geist Mono, Pitch, Courier Prime, Space Mono"
  paletas_ideais:
    - "Warm Gallery Stone & Museum Paper: #FFFFFF (White Pure), #FBFBFA (Warm Alabaster), #F4F3EF (Museum Linen), #E8E7E1 (Hairline Border), #111111 (Carbon Ink), #666665 (Muted Caption)"
    - "Obsidian Monograph / Deep Gallery Noir: #0B0B0C (Deep Canvas), #141416 (Surface Card), #222226 (Hairline Divider), #EAEAEB (High Contrast Type), #8E8E93 (Secondary Metadata)"
    - "Raw Architectural Concrete: #E5E5E5 (Canvas Light Grey), #D4D4D4 (Structural Rule), #171717 (Foreground Solid), #525252 (Body Copy)"
    - "Monocromático Puro com Acento Zero ou Cirúrgico: Ausência deliberada de cores saturadas — a única cor permitida vem estritamente da fotografia do produto/obra de arte ou de um micro-acento pontual de 10% (ex: Vermelho Editorial #E63946 ou Azul Galeria #1D3557)"
  combinacoes_recomendadas:
    - "CSS Grid nativo de 12 ou 16 colunas com `grid-template-rows: subgrid` e borders de 1px sólidos para criar partições modulares rígidas estilo Josef Müller-Brockmann"
    - "Next.js App Router com Server Components e ISR para renderização ultrarrápida (TTFB < 80ms) e carregamento de imagens com Next/Image priorizado e `sizes` cirúrgicos"
    - "Tailwind CSS customizado com `letter-spacing: -0.03em` para títulos gigantes e `letter-spacing: +0.05em` para metadados em caixa alta monoespaçada"
    - "Framer Motion com transições de opacidade puras (`duration: 0.2`, `ease: [0.16, 1, 0.3, 1]`) e zoom de imagem em escala quase imperceptível (`1.015` a `1.02` no hover)"
  conflitos_esteticos:
    - "Sombras projetadas difusas, coloridas ou borradas (Drop shadows, glow effects, prismas de luz e neumorfismo)"
    - "Bordas excessivamente arredondadas (Border-radius acima de 4px destrói a disciplina arquitetural modernista; o estilo exige raio 0px rígido)"
    - "Gradientes multicoloridos neon, fundos cósmicos, malhas de gradiente (mesh gradients) ou elementos 'playful/gamificados'"
    - "Badges chamativos de premiação, popups de marketing intrusivos, contadores regressivos de urgência de e-commerce e banners promocionais flutuantes"
    - "Animações circenses ou 'scrolljacking' descalibrado com inércia forçada que atrasa a leitura do usuário e compromete a acessibilidade"
    - "Tipografia desproporcional sem baseline rígido, fontes display infantis (ex: Comic, bubble, rounded sans) ou excesso de pesos conflitantes na mesma tela"
---

# Siteinspire — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
███████╗██╗████████╗███████╗██╗███╗   ██╗███████╗██████╗ ██╗██████╗ ███████╗
██╔════╝██║╚══██╔══╝██╔════╝██║████╗  ██║██╔════╝██╔══██╗██║██╔══██╗██╔════╝
███████╗██║   ██║   █████╗  ██║██╔██╗ ██║███████╗██████╔╝██║██████╔╝█████╗  
╚════██║██║   ██║   ██╔══╝  ██║██║╚██╗██║╚════██║██╔═══╝ ██║██╔══██╗██╔══╝  
███████║██║   ██║   ███████╗██║██║ ╚████║███████║██║     ██║██║  ██║███████╗
╚══════╝╚═╝   ╚═╝   ╚══════╝╚═╝╚═╝  ╚═══╝╚══════╝╚═╝     ╚═╝╚═╝  ╚═╝╚══════╝
```

---

## 1. DNA Estético & Filosofia de Curadoria

Fundado em 2009 pelo designer e diretor criativo britânico **Daniel Howells** (co-fundador ao lado de Sean Hamlin e líder do prestigiado estúdio londrino *Howells*), o **Siteinspire** (`https://www.siteinspire.com/`) consolidou-se como o arquivo de referência mais respeitado, rigoroso e atemporal da indústria global de design digital. Enquanto plataformas como Awwwards ou FWA celebram o espetáculo cinemático, a computação gráfica WebGL, a física de partículas 3D e a pirotecnia tecnológica de curta vida útil, o Siteinspire atua como o **antídoto absoluto ao ruído digital**: uma curadoria que reverencia a pureza do design gráfico modernista, o respeito intransigente pela tipografia, o uso disciplinado do espaço negativo e o poder estrutural de grades suíças rigorosas.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        THE SITEINSPIRE CURATORIAL MANIFESTO                            │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  [ Swiss Modernism ]  ──►  [ Quiet Craftsmanship ]  ──►  [ Enduring Usability ]       │
│   • Asymmetrical Grids      • 1px Hairline Dividers      • Real, Live URLs Only        │
│   • Architectural Whitespace• Subdued Color Palettes     • Anti-Award Badge Filter     │
│   • Pure Typographic Hierarchy • Zero Gratuitous WebGL   • Timeless 10-Year Shelf Life │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  THE 4-AXIS TAXONOMY: Styles (Visuals) × Types (Layout) × Subjects (Niche) × Platforms │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 A Filosofia Central de Daniel Howells: "Simplicity Always Wins Over Novelty"

A longevidade e a autoridade inquestionável do Siteinspire decorrem de um conjunto inabalável de princípios curatoriais desenvolvidos por Daniel Howells ao longo de mais de uma década e meia:

1. **O Filtro do "If I wish I had made it" (O Teste da Inveja Criativa)**:
   A régua de corte para inclusão no Siteinspire não depende de votações públicas de popularidade, campanhas virais em redes sociais ou patrocínios de agências. Daniel Howells realiza uma triagem manual implacável: se, ao navegar por um site ativo, o sentimento imediato for *"eu gostaria de ter desenhado e codificado isso"*, a obra é selecionada. É um filtro de gosto autoral baseado na erudição visual e no discernimento de um designer sênior praticante.

2. **A Vitória da Simplicidade sobre o Efêmero ("Simplicity Wins")**:
   Howells observou historicamente que projetos repletos de "gimmicks" visuais — transições que sequestram o scroll do usuário, modelos 3D que aquecem a GPU sem adicionar valor semântico e loaders intermináveis — envelhecem como leite. Em contraste, websites fundamentados em grids consistentes, tipografia de proporções clássicas e layouts silenciosos mantêm seu frescor visual mesmo após 10 ou 15 anos. Navegar pelo arquivo do Siteinspire de 2011 e 2012 revela projetos que poderiam ser lançados hoje sem qualquer sensação de defasagem.

3. **"A Solid Grid Will Always Beat a Trendy Layout Gimmick"**:
   Esta célebre máxima de Howells sintetiza a essência estrutural do site. Truques de layout passam com as estações da moda; a solidez de um sistema de colunas ordenado (herança direta de Massimo Vignelli, Josef Müller-Brockmann e Otl Aicher) confere clareza cognitiva imediata, imponência institucional e harmonia geométrica inabalável.

4. **Real, Live Web Only (Apenas a Web Real em Produção)**:
   O Siteinspire possui uma aversão explícita ao que a indústria chama de "Dribbble fantasy UI" — conceitos puramente ilustrativos, telas no Figma sem dados reais ou experimentos que nunca enfrentaram a complexidade de rodar em navegadores heterogêneos, telas móveis e conexões lentas. **Para estar no Siteinspire, o site DEVE existir em produção**.

5. **Anti-Award Badgeism & Anti-Clutter**:
   Howells descarta ativamente websites que poluem suas interfaces com selos gigantes de prêmios ("SOTD Winner", "FWA of the Day"), banners intrusivos de cookies mal projetados, popups invasivos de newsletter ou caixas de chat agressivas. O design deve falar por si mesmo, sem implorar por validação externa.

6. **Rejeição ao Dogma do "Mobile-First Lazy Desktop"**:
   Embora o Siteinspire exija responsividade impecável, Howells sempre criticou a tendência de estúdios que projetam exclusivamente para telas de 375px e depois apenas "esticam" o layout para o desktop de 1440px ou 2560px, gerando oceanos de vazio acidental e componentes gigantistas desajeitados. No ecossistema Siteinspire, a tela de desktop é tratada como uma **página de monografia arquitetural**, tirando proveito pleno de grades multidimensionais, tipografia de grande porte e diagramação editorial sofisticada.

---

### 1.2 A Taxonomia de 4 Dimensões do Siteinspire

A arquitetura de informação do Siteinspire é uma das mais influentes da história da web, estruturando milhares de estudos de caso sob quatro eixos ortogonais:

```
                  ┌───────────────────────────────────────────────┐
                  │          SITEINSPIRE TAXONOMY MATRIX          │
                  └──────────────────────┬────────────────────────┘
                                         │
       ┌──────────────────┬──────────────┴─────┬──────────────────┐
       ▼                  ▼                    ▼                  ▼
┌──────────────┐   ┌──────────────┐    ┌──────────────┐   ┌──────────────┐
│    STYLES    │   │    TYPES     │    │   SUBJECTS   │   │  PLATFORMS   │
├──────────────┤   ├──────────────┤    ├──────────────┤   ├──────────────┤
│ • Minimal    │   │ • Portfolio  │    │ • Fashion    │   │ • Shopify    │
│ • Clean      │   │ • E-Commerce │    │ • Architec.  │   │ • Webflow    │
│ • Typography │   │ • Editorial  │    │ • Art/Cult.  │   │ • WordPress  │
│ • Grid       │   │ • Corporate  │    │ • Photo      │   │ • Craft CMS  │
│ • Monochrome │   │ • Directory  │    │ • Furniture  │   │ • Sanity/Next│
│ • Brutalist  │   │ • SinglePage │    │ • Publishing │   │ • Bespoke/JS │
└──────────────┘   └──────────────┘    └──────────────┘   └──────────────┘
```

| Eixo | O que Categoriza | Exemplos Chave no Acervo |
| :--- | :--- | :--- |
| **Styles** | A linguagem visual, o tom estético e o tratamento gráfico do layout. | *Minimal, Clean, Typography-focused, Grid, Monochrome, Dark, Brutalist, Unusual Layout, Flat, Industrial.* |
| **Types** | O modelo funcional de arquitetura de informação e interação do projeto. | *Portfolio, E-Commerce, Editorial / Magazine, Corporate, Archive / Directory, Studio, Single Page, Event.* |
| **Subjects** | O domínio de negócio, nicho de mercado ou vertical cultural do cliente. | *Architecture, Fashion, Art & Culture, Photography, Furniture & Interiors, Graphic Design, Food & Drink, Luxury.* |
| **Platforms** | A tecnologia de back-end, CMS ou plataforma de publicação utilizada. | *Custom / Bespoke, Shopify, Webflow, Craft CMS, WordPress, Cargo, Squarespace, Sanity.* |

Essa categorização permite que engenheiros de UI e diretores de arte cruzem especificações precisas — por exemplo: `Style: Minimal` + `Subject: Architecture` + `Type: Portfolio` + `Platform: Next.js/Custom` — isolando com rigor matemático as melhores soluções mundiais para aquele exato desafio.

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

O Siteinspire é o **padrão-ouro absoluto** quando o briefing do projeto exige sobriedade, sofisticação intelectual, prestígio institucional e o que a indústria contemporânea define como **Quiet Luxury (Luxo Silencioso)**.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                          SITEINSPIRE: THE 60-30-10 HARMONY                             │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  60% — ARCHITECTURAL CANVAS & NEGATIVE SPACE                                           │
│  Fundos puros (#FFFFFF, #FBFBFA, #0B0B0C). Margens monumentais de 4vw a 8vw.           │
│  Espaço de respiro que confere nobreza, calma e respeito sacro ao conteúdo.            │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  30% — TYPOGRAPHIC DISCIPLINE & EDITORIAL MEDIA                                        │
│  Tipografia monumental em grotesco suíço ou serif clássico. Curadoria fotográfica      │
│  sem filtros coloridos. Grades de 12 colunas com hairline dividers de 1px.             │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  10% — SURGICAL ACCENT & MICRO-FEEDBACK                                                │
│  Ausência deliberada de cores berrantes. O acento é a própria nitidez da foto ou um    │
│  único detalhe funcional: micro-bullets pretos, links sublinhados com hair-line de 1px.│
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 2.1 As 7 Verticais de Ouro

1. **Moda de Luxo, Alta-Costura & Casas de Perfumaria de Nicho**:
   - Referências estéticas no padrão *Céline (era Phoebe Philo / Peter Miles), The Row, Lemaire, Bottega Veneta, Khaite, Jil Sander*.
   - Tratamento onde a fotografia de passarela ou estúdio domina o espaço com bordas vivas (raio zero), títulos em caixa-baixa refinada ou caixa-alta espaçada (`tracking-widest`) e metadados discretos de tecido e coleção.

2. **Arquitetura, Urbanismo & Portfólios de Interiores de Alto Padrão**:
   - Escritórios de renome internacional (*David Chipperfield, John Pawson, Studio Mumbai, Olson Kundig, Herzog & de Meuron*).
   - Onde o layout se comporta como uma monografia impressa encadernada em linho: pranchas técnicas, fotografias em grande formato com proporções 4:5 ou 3:2, plantas baixas vetoriais de traço fino e fichas técnicas monospaçadas (Ano, Localização, Metragem, Estrutura).

3. **Arte Contemporânea, Museus, Fundações Culturais & Galerias Internacionais**:
   - Plataformas no patamar de *Hauser & Wirth, Gagosian, David Zwirner, Pace Gallery, Fondation Beyeler*.
   - Canvas ultralimpo que simula a experiência das paredes brancas de um museu ("White Cube"), garantindo que a paleta do site nunca compita com as cores das pinturas, esculturas ou instalações.

4. **Editoras Independentes, Revistas Culturais & Monografias Digitais**:
   - Publicações literárias, ensaios teóricos, jornais de design (*Apartamento Magazine, The Gentlewoman, 032c, Disegno Journal*).
   - Tipografia de leitura imersiva com colunas de texto de 45 a 65 caracteres por linha, capitulares elegantes, notas de rodapé numeradas com precisão e citações recuadas em grids suíços.

5. **Estúdios de Design Gráfico, Agências de Branding & Typographic Foundries**:
   - Estúdios do calibre de *Spin, Studio Frith, Made Thought, Bureau Borsche, OK-RM, Dinamo, Pangram Pangram*.
   - Interfaces auto-reflexivas que usam a própria tela como prova de rigor projetual, com índices alternáveis entre Thumbnail Grid e Tabela de Texto densa.

6. **Mobiliário de Design Industrial & Objetos de Arquitetura**:
   - Marcas históricas e contemporâneas (*Vitsœ de Dieter Rams, USM Haller, Artek, Muuto, Hay, Cassina*).
   - Exaltação do produto funcional através de grids modulares rígidos que espelham o próprio sistema construtivo dos móveis.

7. **E-Commerce de Luxo e Curação Editorial ("Gallery-Style Commerce")**:
   - Lojas online que rejeitam o visual de "supermercado de ofertas". Produtos fotografados isoladamente sobre superfícies neutras, sem crachás de desconto ou contadores de escassez; botões monospaçados simples ("Inquire" ou "Add to Bag").

### 2.2 Emoção e Posicionamento de Marca

Ao projetar uma interface sob a influência do Siteinspire, a mensagem emocional transmitida ao usuário é:
- **Autoridade Inquestionável**: Não há necessidade de gritar, piscar ou implorar pela atenção do visitante. A excelência do trabalho é autoevidente.
- **Calma e Clareza Intelectual**: A mente do usuário descansa da sobrecarga sensorial cotidiana da web moderna.
- **Atemporalidade e Durabilidade**: A sensação de estar interagindo com um artefato digital construído para durar uma década, não para uma campanha descartável de 15 dias.

---

## 3. Contraindicações Estéticas (Quando NÃO Usar & Anti-Padrões)

Adotar a estética do Siteinspire no contexto errado é um erro grave de engenharia de produto e estratégia de negócios.

### 3.1 Em Quais Cenários NÃO Usar

- ⚠️ **SaaS B2B Operacional Denso (Dashboards de Monitoramento e Ferramentas Analíticas)**:
  Sistemas como Datadog, AWS Console, Grafana ou plataformas de CRM financeiro exigem densidade de dados altíssima, visualizações tabulares compactas, gráficos multicoloridos para telemetria em tempo real e dezenas de controles simultâneos. Aplicar margens monumentais de 8vw e tipografia de 72px nesse contexto inutilizaria a ferramenta.
- ⚠️ **Marketplaces de Massa & E-Commerce Promocional Agressivo**:
  Supermercados digitais, varejistas de moda rápida (Fast Fashion) ou marketplaces de alto volume dependem de tags de desconto ("50% OFF"), badges de frete grátis, banners rotativos e gatilhos de urgência para conversão impulsiva. O público desses setores interpreta o minimalismo silencioso como "caro", "distante" ou "vazio de opções".
- ⚠️ **Jogos, Games de Ação & Experiências de Entretenimento Sci-Fi**:
  Ambientes que demandam interfaces imersivas com shaders GLSL, áudio diegético interativo, menus com estética cyberpunk ou fantasia visual.
- ⚠️ **Produtos Infantis ou de Gamificação Educacional**:
  Públicos jovens respondem a cores primárias saturadas, personagens lúdicos, animações exuberantes de recompensa e feedback tátil sonoro imediato.

---

### 3.2 As 5 Armadilhas Fatais de Imitação (Anti-Padrões do "Fake Minimalism")

Muitos desenvolvedores e designers tentam copiar o visual do Siteinspire e criam experiências desastrosas. Estes são os erros críticos a evitar:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                      THE 5 DEADLY TRAPS OF PSEUDO-MINIMALISM                           │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ 1. DESERT MINIMALISM    │ Remover conteúdo relevante e achar que "vazio = sofisticação"│
│ 2. LOW-CONTRAST SNOBBERY│ Texto cinza claro (#A0A0A0) em fundo branco (WCAG Failed)   │
│ 3. MYSTERY MEAT UX      │ Botões sem label, ícones crípticos, ausência de hover state  │
│ 4. ASSET BLOAT DISASTER │ Imagens RAW de 12MB sem WebP/AVIF gerando LCP de 8 segundos  │
│ 5. MOBILE COLLAPSE      │ Pilha infinita de cards no celular sem ritmo ou paginação     │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

1. **O "Minimalismo Vazio" (Desert Minimalism)**:
   Achar que minimalismo é simplesmente retirar informações essenciais. O verdadeiro minimalismo suíço é **rigor estrutural**, não ausência de conteúdo. Ele organiza dados complexos com extrema elegância, fornecendo metadados técnicos precisos (datas, categorias, especificações) sem ruído gráfico.
2. **O Esnobismo do Baixo Contraste (WCAG Violations)**:
   Utilizar fontes ultrafinas em corpo 10px com cor cinza claro sobre fundo branco, tornando o texto invisível para pessoas com deficiência visual moderada ou sob iluminação solar direta. No bom design suíço, o contraste entre a tinta preta (#111111) e o papel (#FBFBFA) é **nítido, incisivo e perfeitamente legível**.
3. **Navegação "Mystery Meat"**:
   Esconder menus inteiros atrás de ícones abstratos de um único ponto (`•`) ou três traços sem rótulo textual, forçando o usuário a adivinhar onde clicar. O Siteinspire utiliza palavras completas em tipografia limpa ("Index", "Filter", "About", "Contact"), sem enigmas.
4. **Desastre de Performance com Mídias Pesadas**:
   Subir fotografias editoriais não comprimidas de câmeras Hasselblad de 50MB, causando travamentos de rolagem e tempos de carregamento exasperantes. A sofisticação da imagem exige engenharia de ponta: compressão AVIF/WebP responsiva, lazy-loading inteligente e placeholders de desfoque sutil (*blur-up*).
5. **Colapso Estrutural em Dispositivos Móveis**:
   Projetar uma grade deslumbrante de 16 colunas no desktop e, na versão mobile, simplesmente empilhar 40 cards idênticos numa única coluna vertical sem respiro, sem filtros colapsáveis e sem divisão por seções.

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo

A estrutura que sustenta os sites do ecossistema Siteinspire repousa em três pilares matemáticos:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        16-COLUMN SWISS ARCHITECTURAL GRID                              │
├────┬────┬────┬────┬────┬────┬────┬────┬────┬────┬────┬────┬────┬────┬────┬─────────────┤
│ 1  │ 2  │ 3  │ 4  │ 5  │ 6  │ 7  │ 8  │ 9  │ 10 │ 11 │ 12 │ 13 │ 14 │ 15 │ 16 (4vw)   │
├────┴────┴────┴────┴────┴────┴────┴────┴────┴────┴────┴────┴────┴────┴────┴─────────────┤
│ [ 01 / MASTHEAD: Studio Name ]                 [ INDEX ] [ ABOUT ] [ 18:42 GMT+1 ]    │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ ── 1px solid #E8E7E1 (Full-Bleed Structural Hairline) ──────────────────────────────── │
├────────────────────────────────────────┬───────────────────────────────────────────────┤
│ [ HERO STATEMENT: 8 Cols ]             │ [ FEATURED ARTIFACT: 8 Cols ]                 │
│ Display Typography 64px / -0.03em      │ Aspect Ratio 4:5 / Precision Studio Image     │
│ "Architectural rigor applied to        │ No border-radius / Crisp 1px outline          │
│ contemporary digital systems."         │                                               │
├────────────────────────────────────────┴───────────────────────────────────────────────┤
│ ── 1px solid #E8E7E1 (Full-Bleed Structural Hairline) ──────────────────────────────── │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

1. **Grids Modulares de 12 ou 16 Colunas com Hairline Rules**:
   - O layout é particionado por linhas divisórias estritas de `1px solid var(--border-hairline)`. Não há sombras ou relevos: a hierarquia é puramente linear e posicional.
   - O uso de `subgrid` do CSS permite que metadados internos de cards diferentes alinhem seus textos perfeitamente ao longo de toda a viewport horizontal.
2. **Espaçamento e Proporções Assimétricas**:
   - Assimetria calculada: blocos de 7 colunas dedicados à fotografia e 5 colunas para o bloco conceitual tipográfico, criando tensão dinâmica sem perder o equilíbrio.
   - Viewport Margins (Gutter de borda de tela): espaçamento lateral generoso, tipicamente `clamp(24px, 4vw, 64px)`.
3. **Escala Tipográfica Hiper-Contrastada**:
   - Coexistência de tamanhos extremos: títulos monumentais (`clamp(48px, 6vw, 110px)`) com tracking negativo estreito (`-0.03em`), emparelhados com legendas monospaçadas minúsculas (`11px` ou `12px`) com tracking expandido (`+0.06em`).

---

### 4.2 Sistemas de Cores, Superfícies & Texturas

| Token | Código HEX | Função no Sistema | Sensação Perceptiva |
| :--- | :---: | :--- | :--- |
| `--canvas-primary` | `#FBFBFA` | Fundo principal da página (Warm Alabaster). | Papel de algodão de galeria de arte europeia. |
| `--canvas-pure` | `#FFFFFF` | Superfície de cartões fotográficos ou modais. | Pureza óptica imaculada. |
| `--canvas-dark` | `#0B0B0C` | Fundo principal em paletas noturnas / Dark Monograph. | Carvão mineral mate, absorvedor de reflexos. |
| `--text-ink` | `#111111` | Cor primária para títulos e corpos de texto. | Tinta tipográfica preta profunda (*Carbon Black*). |
| `--text-muted` | `#666665` | Metadados, datas, legendas de fotos e colofão. | Grafite nobre, legível e submisso ao título. |
| `--border-hairline`| `#E8E7E1` | Linhas estruturais de 1px entre seções e cards. | Fio de navalha arquitetônico imperceptível. |
| `--border-hairline-dark`| `#222226` | Linhas estruturais em temas escuros. | Grafite escovado sobre ardósia. |
| `--accent-surgical`| `#E63946` | Micro-pontos de status, bullets ou links ativos (10%). | Carimbo editorial de validação. |

**Superfícies e Curvatura**:
- `border-radius: 0px` é a regra padrão absoluta. Quando um raio é estritamente necessário para botões de pílula, ele é mantido integralmente circular (`rounded-full`), sem formatos intermediários "arredondados de app infantil" (`rounded-lg` de 8px ou 12px são proibidos).

---

### 4.3 Catálogo de 8 Arquétipos Concretos do Siteinspire

#### Arquétipo 1: O "Masthead Editorial & Studio Telemetry Header"
- **Anatomia**: Barra superior horizontal que se estende por 100% da viewport, fixada ou estática. Dividida em 4 quadrantes por linhas de 1px:
  1. Quadrante 1: Nome do Estúdio / Marca em fonte Grotesk ou Serif pura.
  2. Quadrante 2: Manifesto ou status operacional ("Independent Architecture Studio based in Zurich").
  3. Quadrante 3: Telemetria em tempo real com relógio do fuso horário local e temperatura ("17:42 CET — Available for Q3").
  4. Quadrante 4: Navegação compacta ("Index", "Archive", "Contact") com contador numérico em sobrescrito (`[14]`).
- **Gatilho de Interação**: Hover discreto com transição de cor do texto de cinza para preto em 150ms.

#### Arquétipo 2: A "Dual-View Archival Grid & Table Toggle"
- **Anatomia**: O controle clássico que define o Siteinspire e estúdios vanguardistas. Um alternador de visualização minimalista composto por duas palavras ou ícones geométricos puros:
  - `Grid View`: Exibe o acervo em cartões fotográficos grandes (2, 3 ou 4 colunas).
  - `Index View / Table View`: Transforma instantaneamente a página em uma tabela tipográfica de alta densidade estilo catálogo de museu (Colunas: Número, Projeto, Cliente, Setor, Ano).
- **Gatilho de Interação**: Troca sem recarregamento de página via estado local com animação suave de opacidade (`fade: 200ms`). No modo Tabela, passar o cursor sobre qualquer linha revela uma miniatura fotográfica flutuante que acompanha o ponteiro do mouse (*cursor-following image thumbnail*).

#### Arquétipo 3: O "Asymmetric Project Showcase Card com Metadados em Hairline"
- **Anatomia**: Cartão de projeto desprovido de caixas sombreadas ou cantos redondos:
  - Área visual superior: Fotografia em proporção 4:5 ou 16:10 com overflow oculto.
  - Linha divisória de 1px horizontal colada diretamente na base da imagem.
  - Rodapé de metadados de 2 linhas dividido por uma linha de 1px vertical: Título do Projeto e Cliente em grotesk 14px à esquerda; Ano e Disciplina em tipografia monoespaçada 11px à direita.
- **Gatilho de Interação**: Ao passar o cursor, a imagem realiza um zoom quase imperceptível de escala `1.015` com transição cúbica suave de 500ms, enquanto o texto do título assume um sublinhado fino de 1px.

#### Arquétipo 4: A "Hero Monograph Split: Typographic Statement + Singular Focus"
- **Anatomia**: Hero section sem carrosséis ou vídeos bombásticos automáticos:
  - Coluna Esquerda (50% de largura): Título editorial de escala monumental (72px) estruturado em múltiplas linhas curtas, acompanhado de um parágrafo conceitual em 16px e um link de ação monospaçado com seta direcional (`Explore Work →`).
  - Coluna Direita (50% de largura): Uma única fotografia emblemática em alta definição, perfeitamente emoldurada pela grade, ancorada na base da tela.
- **Gatilho de Interação**: Entrada com fade-in escalonado (*staggered opacity*) de 0.4s sem translações exageradas de eixo Y.

#### Arquétipo 5: O "Editorial Case Study Multi-Cadence Layout"
- **Anatomia**: Páginas de detalhe de projeto que alternam o ritmo visual como páginas de um livro de arte:
  1. Bloco 1: Imagem de impacto de sangria total (*full-bleed*, 100vw).
  2. Bloco 2: Grade de 2 colunas com uma imagem vertical 4:5 à esquerda e um bloco de texto explicativo estreito à direita.
  3. Bloco 3: Dupla de imagens em proporção 1:1 lado a lado com linha de 1px entre elas.
  4. Bloco 4: Citação conceitual em serifa display centralizada, ocupando 8 das 12 colunas da grade com enorme respiro vertical acima e abaixo (padding-y: 120px).
- **Gatilho de Interação**: Rolagem fluida com ancoragem visual nos detalhes dos acabamentos.

#### Arquétipo 6: O "Minimalist High-End E-Commerce Product Card & Drawer"
- **Anatomia**: Produto isolado em fundo plano neutro (#F7F6F2) com iluminação difusa natural:
  - Sem banners de porcentagem ou selos de "Promoção".
  - Nome do produto em serifa elegante ou grotesco neutro, seguido do valor monetário sem centavos supérfluos ("€ 420").
  - Botão de compra reduzido a uma linha de texto ou botão pílula austero ("Order Edition").
  - Painel lateral (Drawer) deslizante em 1px solid border com seleção de variações e resumo textual de materiais de fabricação.
- **Gatilho de Interação**: Abertura do drawer lateral através de mola altamente amortecida (`stiffness: 320, damping: 32`) sem backdrop embaçado artificial (fundo preserva transparência límpida com 20% de escurecimento).

#### Arquétipo 7: O "Swiss Columnar Colophon & Index Footer"
- **Anatomia**: Rodapé de encerramento monumental estruturado em 4 a 6 colunas rigorosas delimitadas por bordas de 1px:
  - Coluna 1: Índice completo de navegação do site em lista vertical.
  - Coluna 2: Informações de contato direto, e-mails específicos por setor e endereços físicos com links para mapas.
  - Coluna 3: Prêmios, imprensa e publicações selecionadas (ano a ano).
  - Coluna 4: O "Colofão" (créditos detalhados: tipografias licenciadas, equipe de desenvolvimento, stack de software e direitos autorais).
- **Gatilho de Interação**: Links textuais limpos com efeito hover de mudança de contraste.

#### Arquétipo 8: O "Taxonomy Filtering Matrix"
- **Anatomia**: Barra de navegação secundária expansível que replica a essência do Siteinspire:
  - 4 pilares expostos em texto: `Styles [6]`, `Types [4]`, `Subjects [12]`, `Platforms [5]`.
  - Ao clicar em qualquer pilar, uma gaveta sutil se abre abaixo da barra sem empurrar o conteúdo de forma brusca, exibindo tags selecionáveis em tipografia monoespaçada.
  - Um contador no canto direito exibe a quantidade exata de resultados correspondentes ("Showing 28 Projects").
- **Gatilho de Interação**: Filtro instantâneo reativo sem refresh de tela com animação de reordenação de elementos em CSS Grid.

---

## 5. Arquitetura Técnica, Física de Movimento & Receita de Código Funcional

### 5.1 Física de Movimento: A Dinâmica da Contenção Silenciosa

O Siteinspire e os projetos sob sua égide repudiam solenemente qualquer animação acrobática, elástica ou exagerada (*bouncy springs*). O movimento é utilizado exclusivamente para conferir **fidelidade física de papel e mecânica óptica de precisão**.

- **Curvas de Bézier Primárias**:
  - `cubic-bezier(0.16, 1, 0.3, 1)`: O "Expo Out" quintessencial. Rápido na aceleração inicial, desaceleração prolongada e suave, conferindo elegância aerodinâmica.
  - `cubic-bezier(0.25, 1, 0.5, 1)`: Curva suave de aproximação para transições de cor e opacidade de texto.
- **Configurações de Mola Framer Motion (`type: "spring"`)**:
  - `stiffness: 300`, `damping: 35`, `mass: 0.8`: Resposta instantânea sem oscilação ou ressalto para abertura de painéis laterais e alternância de abas.
  - `stiffness: 450`, `damping: 40`: Para o seguidor de cursor (Floating Image Thumbnail Preview), garantindo que a imagem acompanhe o mouse com um atraso inercial orgânico mínimo (menos de 40ms de lag percebido).
- **Durações Temporais**:
  - Micro-interações de hover em texto e links: **120ms a 180ms**.
  - Transições de imagem e zoom de escala: **500ms a 700ms**.
  - Troca de visualização (Grid ↔ Tabela): **200ms**.

---

### 5.2 Tokens de Design em CSS (CSS Custom Properties)

```css
:root {
  /* Espaço e Margens Estruturais */
  --space-gutter: clamp(1.25rem, 3.5vw, 3.5rem);
  --space-grid-gap: clamp(0.75rem, 1.5vw, 1.5rem);
  --hairline-width: 1px;

  /* Cores: Canvas & Superfícies (Warm Gallery Alabaster) */
  --canvas-base: #FBFBFA;
  --canvas-surface: #FFFFFF;
  --canvas-elevated: #F5F4F0;
  
  /* Cores: Tipografia & Tinta */
  --ink-primary: #111111;
  --ink-secondary: #555554;
  --ink-tertiary: #888886;
  --ink-accent: #E63946;

  /* Cores: Linhas Estruturais */
  --line-structural: #E8E7E1;
  --line-strong: #111111;

  /* Famílias Tipográficas */
  --font-grotesk: "Neue Haas Grotesk", "PP Neue Montreal", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  --font-serif: "Bradford", "GT Sectra", "Lyon Display", "Cormorant Garamond", Georgia, serif;
  --font-mono: "PP Neue Machina", "Geist Mono", "JetBrains Mono", Menlo, monospace;

  /* Físicas de Transição */
  --ease-editorial: cubic-bezier(0.16, 1, 0.3, 1);
  --ease-subtle: cubic-bezier(0.25, 1, 0.5, 1);
  --duration-hover: 160ms;
  --duration-panel: 320ms;
}

/* Dark Mode Suíço Monográfico (Ativado por classe ou preferência de sistema) */
[data-theme="dark"] {
  --canvas-base: #0B0B0C;
  --canvas-surface: #141416;
  --canvas-elevated: #1B1B1E;
  
  --ink-primary: #F4F4F5;
  --ink-secondary: #A1A1A6;
  --ink-tertiary: #636366;
  --ink-accent: #FF453A;

  --line-structural: #242428;
  --line-strong: #F4F4F5;
}
```

---

### 5.3 Receita de Código Funcional e Completa

O componente React 19 / Next.js a seguir materializa a essência do Siteinspire:
1. **Masthead Suíço** com relógio em tempo real e alternador instantâneo entre **Grid** e **Tabela/Índice**.
2. **Barra de Taxonomia** com contadores e filtros multidimensionais.
3. **Visão em Grade** com cartões delimitados por bordas hairline de 1px e tipografia rigorosa.
4. **Visão em Tabela** com **Floating Image Preview** interativo que segue as coordenadas do ponteiro do mouse via Framer Motion.

```tsx
"use client";

import React, { useState, useEffect, useRef } from "react";
import { motion, AnimatePresence } from "framer-motion";

interface ProjectItem {
  id: string;
  number: string;
  title: string;
  client: string;
  subject: "Architecture" | "Fashion" | "Editorial" | "Industrial";
  year: string;
  location: string;
  image: string;
  platform: string;
}

const PROJECTS_DATA: ProjectItem[] = [
  {
    id: "proj-01",
    number: "001",
    title: "Atelier Lemaire Monograph",
    client: "Christophe Lemaire",
    subject: "Fashion",
    year: "2025",
    location: "Paris, FR",
    image: "https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?q=80&w=1000&auto=format&fit=crop",
    platform: "Custom Next.js",
  },
  {
    id: "proj-02",
    number: "002",
    title: "Brutalist Pavilion Archive",
    client: "David Chipperfield Architects",
    subject: "Architecture",
    year: "2024",
    location: "Berlin, DE",
    image: "https://images.unsplash.com/photo-1600585154340-be6161a56a0c?q=80&w=1000&auto=format&fit=crop",
    platform: "Craft CMS",
  },
  {
    id: "proj-03",
    number: "003",
    title: "Vitsœ Systems & Principles",
    client: "Vitsœ Furniture",
    subject: "Industrial",
    year: "2025",
    location: "Leamington Spa, UK",
    image: "https://images.unsplash.com/photo-1538688525198-9b88f6f53126?q=80&w=1000&auto=format&fit=crop",
    platform: "Shopify Hydrogen",
  },
  {
    id: "proj-04",
    number: "004",
    title: "Disegno Quarterly No. 34",
    client: "Disegno Publications",
    subject: "Editorial",
    year: "2024",
    location: "London, UK",
    image: "https://images.unsplash.com/photo-1544716278-ca5e3f4abd8c?q=80&w=1000&auto=format&fit=crop",
    platform: "Sanity.io",
  },
];

export default function SiteinspireArchiveShowcase() {
  const [viewMode, setViewMode] = useState<"grid" | "table">("grid");
  const [activeSubject, setActiveSubject] = useState<string>("All");
  const [currentTime, setCurrentTime] = useState<string>("");
  const [hoveredProject, setHoveredProject] = useState<ProjectItem | null>(null);
  const [mousePosition, setMousePosition] = useState<{ x: number; y: number }>({ x: 0, y: 0 });

  // Relógio do Estúdio em Tempo Real (Fuso Horário Europeu / GMT)
  useEffect(() => {
    const updateTime = () => {
      const now = new Date();
      setCurrentTime(
        now.toLocaleTimeString("en-GB", {
          timeZone: "Europe/London",
          hour: "2-digit",
          minute: "2-digit",
          second: "2-digit",
        })
      );
    };
    updateTime();
    const interval = setInterval(updateTime, 1000);
    return () => clearInterval(interval);
  }, []);

  // Rastreamento do mouse para o Floating Thumbnail Preview na visualização em Tabela
  const handleMouseMove = (e: React.MouseEvent) => {
    setMousePosition({ x: e.clientX, y: e.clientY });
  };

  const filteredProjects = activeSubject === "All"
    ? PROJECTS_DATA
    : PROJECTS_DATA.filter((p) => p.subject === activeSubject);

  return (
    <div
      onMouseMove={handleMouseMove}
      className="min-h-screen bg-[#FBFBFA] text-[#111111] font-sans antialiased selection:bg-[#111111] selection:text-[#FFFFFF]"
      style={{
        fontFamily:
          '"Neue Haas Grotesk", "PP Neue Montreal", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif',
      }}
    >
      {/* 1. MASTHEAD TELEMÉTRICO SUÍÇO (1px border-b rígida) */}
      <header className="w-full border-b border-[#E8E7E1] px-6 lg:px-12 py-5 grid grid-cols-1 md:grid-cols-4 gap-4 items-baseline text-xs uppercase tracking-wider text-[#666665]">
        <div className="font-semibold text-[#111111] tracking-normal text-sm flex items-center gap-2">
          <span className="w-2 h-2 bg-[#111111] inline-block rounded-none"></span>
          SITEINSPIRE ARCHIVE
        </div>

        <div className="hidden md:block">
          CURATED ESSENTIALS / REAL PRODUCTION
        </div>

        <div className="hidden md:block font-mono text-[11px]">
          LONDON [GMT] {currentTime || "12:00:00"}
        </div>

        {/* Alternador Grid vs. Table */}
        <div className="flex justify-start md:justify-end items-center gap-6 text-[11px] font-mono">
          <button
            onClick={() => setViewMode("grid")}
            className={`transition-colors duration-150 flex items-center gap-1.5 ${
              viewMode === "grid" ? "text-[#111111] font-bold" : "text-[#888886] hover:text-[#111111]"
            }`}
          >
            <span>[+]</span> GRID VIEW
          </button>
          <span className="text-[#E8E7E1]">/</span>
          <button
            onClick={() => setViewMode("table")}
            className={`transition-colors duration-150 flex items-center gap-1.5 ${
              viewMode === "table" ? "text-[#111111] font-bold" : "text-[#888886] hover:text-[#111111]"
            }`}
          >
            <span>[=]</span> INDEX TABLE
          </button>
        </div>
      </header>

      {/* 2. MATRIZ DE TAXONOMIA E FILTRO DE 4 EIXOS */}
      <section className="border-b border-[#E8E7E1] px-6 lg:px-12 py-3.5 flex flex-wrap justify-between items-center text-xs">
        <div className="flex items-center gap-4 flex-wrap">
          <span className="font-mono text-[11px] text-[#888886] uppercase mr-2">
            SUBJECT FILTER:
          </span>
          {["All", "Architecture", "Fashion", "Editorial", "Industrial"].map((subject) => (
            <button
              key={subject}
              onClick={() => setActiveSubject(subject)}
              className={`px-2.5 py-1 text-xs transition-all duration-150 border ${
                activeSubject === subject
                  ? "bg-[#111111] text-[#FFFFFF] border-[#111111]"
                  : "bg-transparent text-[#555554] border-transparent hover:border-[#E8E7E1] hover:text-[#111111]"
              }`}
            >
              {subject}
            </button>
          ))}
        </div>

        <div className="font-mono text-[11px] text-[#888886] mt-2 sm:mt-0">
          SHOWING {filteredProjects.length} OF {PROJECTS_DATA.length} ENTRIES
        </div>
      </section>

      {/* 3. CONTEÚDO PRINCIPAL (ALTERNÂNCIA GRID / TABLE COM ANIMAÇÃO) */}
      <main className="px-6 lg:px-12 py-10">
        <AnimatePresence mode="wait">
          {viewMode === "grid" ? (
            /* VISÃO EM GRADE (GRID VIEW) */
            <motion.div
              key="grid-view"
              initial={{ opacity: 0 }}
              animate={{ opacity: 1 }}
              exit={{ opacity: 0 }}
              transition={{ duration: 0.2, ease: [0.16, 1, 0.3, 1] }}
              className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-x-8 gap-y-12"
            >
              {filteredProjects.map((project) => (
                <article
                  key={project.id}
                  className="group flex flex-col cursor-pointer"
                >
                  {/* Contêiner da Imagem */}
                  <div className="relative w-full aspect-[4/5] bg-[#EAE8E1] overflow-hidden mb-3.5 border border-[#E8E7E1]">
                    <img
                      src={project.image}
                      alt={project.title}
                      loading="lazy"
                      className="w-full h-full object-cover transition-transform duration-700 ease-[cubic-bezier(0.16,1,0.3,1)] group-hover:scale-[1.02]"
                    />
                    <div className="absolute top-3 left-3 bg-[#111111] text-white text-[10px] font-mono px-2 py-0.5 tracking-wider">
                      {project.number}
                    </div>
                  </div>

                  {/* Metadados Estruturados em Hairline */}
                  <div className="pt-2 border-t border-[#E8E7E1] flex flex-col gap-1">
                    <div className="flex justify-between items-baseline">
                      <h3 className="text-sm font-medium text-[#111111] group-hover:underline underline-offset-4 decoration-1">
                        {project.title}
                      </h3>
                      <span className="font-mono text-[11px] text-[#888886]">
                        {project.year}
                      </span>
                    </div>

                    <div className="flex justify-between items-center text-xs text-[#666665] font-mono text-[11px]">
                      <span>{project.client}</span>
                      <span className="text-[#888886]">{project.subject}</span>
                    </div>
                  </div>
                </article>
              ))}
            </motion.div>
          ) : (
            /* VISÃO EM TABELA / ÍNDICE (TABLE INDEX VIEW) */
            <motion.div
              key="table-view"
              initial={{ opacity: 0 }}
              animate={{ opacity: 1 }}
              exit={{ opacity: 0 }}
              transition={{ duration: 0.2, ease: [0.16, 1, 0.3, 1] }}
              className="w-full border-t border-[#E8E7E1]"
            >
              <div className="hidden md:grid grid-cols-12 py-3 text-[11px] font-mono text-[#888886] border-b border-[#E8E7E1] uppercase">
                <div className="col-span-1">No.</div>
                <div className="col-span-4">Project & Archive Title</div>
                <div className="col-span-3">Client / Commission</div>
                <div className="col-span-2">Subject Vertical</div>
                <div className="col-span-1">Location</div>
                <div className="col-span-1 text-right">Year</div>
              </div>

              {filteredProjects.map((project) => (
                <div
                  key={project.id}
                  onMouseEnter={() => setHoveredProject(project)}
                  onMouseLeave={() => setHoveredProject(null)}
                  className="grid grid-cols-1 md:grid-cols-12 py-4 border-b border-[#E8E7E1] items-baseline text-xs transition-colors duration-150 hover:bg-[#F3F2EE] cursor-pointer px-2 -mx-2"
                >
                  <div className="col-span-1 font-mono text-[11px] text-[#888886]">
                    {project.number}
                  </div>
                  <div className="col-span-4 font-medium text-sm text-[#111111]">
                    {project.title}
                  </div>
                  <div className="col-span-3 text-[#555554] font-mono text-[11px]">
                    {project.client}
                  </div>
                  <div className="col-span-2 text-[#555554]">
                    <span className="border border-[#DCDAD2] px-2 py-0.5 text-[10px] font-mono uppercase bg-[#FFFFFF]">
                      {project.subject}
                    </span>
                  </div>
                  <div className="col-span-1 text-[#888886] font-mono text-[11px]">
                    {project.location}
                  </div>
                  <div className="col-span-1 text-right font-mono text-[11px] text-[#111111] font-semibold">
                    {project.year}
                  </div>
                </div>
              ))}
            </motion.div>
          )}
        </AnimatePresence>
      </main>

      {/* 4. FLOATING IMAGE THUMBNAIL PREVIEW (Exclusivo da Visão em Tabela) */}
      <AnimatePresence>
        {viewMode === "table" && hoveredProject && (
          <motion.div
            initial={{ opacity: 0, scale: 0.95 }}
            animate={{
              opacity: 1,
              scale: 1,
              x: mousePosition.x + 24,
              y: mousePosition.y - 120,
            }}
            exit={{ opacity: 0, scale: 0.95 }}
            transition={{
              type: "spring",
              stiffness: 450,
              damping: 38,
              mass: 0.5,
            }}
            className="fixed pointer-events-none z-50 w-64 aspect-[4/5] bg-white border border-[#111111] shadow-2xl overflow-hidden p-1.5"
            style={{ left: 0, top: 0 }}
          >
            <div className="relative w-full h-full bg-[#EAE8E1] overflow-hidden">
              <img
                src={hoveredProject.image}
                alt={hoveredProject.title}
                className="w-full h-full object-cover"
              />
              <div className="absolute bottom-2 left-2 right-2 bg-[#111111]/90 text-white p-2 text-[10px] font-mono flex justify-between">
                <span>{hoveredProject.platform}</span>
                <span>{hoveredProject.year}</span>
              </div>
            </div>
          </motion.div>
        )}
      </AnimatePresence>

      {/* 5. COLOFÃO & RODAPÉ SUÍÇO ARQUITETURAL (4 Colunas) */}
      <footer className="mt-20 border-t border-[#E8E7E1] px-6 lg:px-12 py-16 grid grid-cols-1 md:grid-cols-4 gap-12 text-xs text-[#555554] bg-[#F8F7F3]">
        <div className="flex flex-col gap-3">
          <div className="font-semibold text-[#111111] uppercase tracking-wider text-[11px]">
            Curatorial Mission
          </div>
          <p className="leading-relaxed text-[#666665]">
            Siteinspire selects digital craft based on typographical purity, structural honesty, and functional restraint. Founded by Daniel Howells.
          </p>
        </div>

        <div className="flex flex-col gap-3">
          <div className="font-semibold text-[#111111] uppercase tracking-wider text-[11px]">
            Taxonomy Breakdown
          </div>
          <ul className="flex flex-col gap-1.5 font-mono text-[11px]">
            <li>Styles: Minimal, Clean, Grid, Typographic</li>
            <li>Types: Portfolio, Editorial, Luxury Commerce</li>
            <li>Subjects: Architecture, Fashion, Arts</li>
            <li>Platforms: Bespoke, Shopify, Next.js</li>
          </ul>
        </div>

        <div className="flex flex-col gap-3">
          <div className="font-semibold text-[#111111] uppercase tracking-wider text-[11px]">
            Colophon & Mechanics
          </div>
          <p className="leading-relaxed text-[#666665] font-mono text-[11px]">
            Typeset in Neue Haas Grotesk. Structural 1px hairline rules. Zero WebGL overhead. Built for longevity.
          </p>
        </div>

        <div className="flex flex-col justify-between items-start md:items-end gap-3 font-mono text-[11px]">
          <span className="text-[#888886]">© 2009–2026 SITEINSPIRE ARCHIVE</span>
          <span className="text-[#111111] font-semibold underline underline-offset-2">
            ALL SITES VERIFIED LIVE
          </span>
        </div>
      </footer>
    </div>
  );
}
```

---

### 5.4 Como a IA Deve Pesquisar ao Vivo no Siteinspire

Quando o agente precisar buscar referências visuais em tempo real para um novo projeto, ele deve montar requisições baseadas na sintaxe taxonômica do Siteinspire.

#### Estrutura Canônica de URLs e Filtros

A URL raiz do arquivo principal é:
```
https://www.siteinspire.com/websites
```

Os parâmetros de busca combinam os 4 eixos taxonômicos via query string ou rotas de categoria:

| Eixo de Busca | Rota Direta | Parâmetro de Query | Exemplos Práticos de Slugs |
| :--- | :--- | :--- | :--- |
| **Styles** | `/styles/<slug>` | `?style=<slug>` | `minimal`, `clean`, `typography`, `grid`, `monochrome`, `dark`, `unusual-layout`, `brutalist` |
| **Types** | `/types/<slug>` | `?type=<slug>` | `portfolio`, `ecommerce`, `editorial`, `corporate`, `archive`, `single-page` |
| **Subjects** | `/subjects/<slug>` | `?subject=<slug>` | `architecture`, `fashion`, `art-culture`, `photography`, `furniture-interior`, `publishing` |
| **Platforms** | `/platforms/<slug>` | `?platform=<slug>` | `shopify`, `webflow`, `wordpress`, `craft-cms`, `squarespace` |

#### Exemplos de Queries Prontas para o Agente de IA:
- **E-Commerce Minimalista de Moda**:  
  `https://www.siteinspire.com/websites?style=minimal&subject=fashion&type=ecommerce`
- **Portfólio Monográfico de Arquitetura**:  
  `https://www.siteinspire.com/websites?style=grid&subject=architecture&type=portfolio`
- **Publicação Cultural / Revista Tipográfica**:  
  `https://www.siteinspire.com/websites?style=typography&type=editorial`
- **Estúdio de Design Gráfico em Shopify**:  
  `https://www.siteinspire.com/websites?style=clean&subject=art-culture&platform=shopify`

---

## 6. Diretrizes Prescritivas para o DESIGN_BLUEPRINT.md

Ao gerar o documento `DESIGN_BLUEPRINT.md` para qualquer produto digital cuja direção de arte tenha como referência o **Siteinspire**, a IA deve seguir rigorosamente as regras abaixo:

### 6.1 Checklist de Conformidade Inegociável

- [ ] **Canvas e Paleta Neutra**: O fundo base DEVE ser um tom neutro calmo (#FFFFFF, #FBFBFA ou #0B0B0C). Cores vibrantes só entram através da fotografia do produto/obra ou em micro-detalhes pontuais de 10%.
- [ ] **Rigor de Borda Hairline**: Todas as divisões de seções e cartões DEVEM utilizar `1px solid var(--border-hairline)`. Proibido o uso de box-shadows difusas ou bordas grossas coloridas.
- [ ] **Raio de Borda Zero (Border Radius 0px)**: Componentes, imagens, cards e inputs mantêm cantos retos (`rounded-none`). Pílulas circulares (`rounded-full`) são reservadas exclusivamente para badges de status ou botões secundários específicos.
- [ ] **Tipografia Hierárquica Suíça**: Combinar apenas duas famílias: um Grotesk Neo-Suíço neutro (para navegação e títulos) e uma Monoespaçada técnica refinada (para metadados, datas e índices). Em projetos de luxo/editorial, admitir uma Serif clássica de alto contraste para citações ou logotipia.
- [ ] **Espaço Negativo Intencional**: Aplicar margens de tela (`padding-x`) de no mínimo 4vw no desktop e respiros verticais de `80px` a `140px` entre grandes seções narrativas.
- [ ] **Dual-View Index Capability**: Em páginas de listagem de projetos, catálogo de arte ou produtos, oferecer sempre a alternância entre a visualização de **Grade Fotográfica** e a **Tabela Tipográfica de Índice**.
- [ ] **Física de Movimento Silenciosa**: Usar acelerações cúbicas secas (`cubic-bezier(0.16, 1, 0.3, 1)`) com durações entre 150ms e 250ms. Zero efeitos elásticos de "bounce", zero distorções líquidas e zero atrasos artificiais de rolagem.

### 6.2 O Que é Terminantemente Proibido

- ❌ Sombras coloridas, gradientes de fundo no estilo "mesh neon" ou efeitos de vidro com desfoque excessivo (*glassmorphism* sujo).
- ❌ Badges de "Site of the Day", selos com estrelas ou selos de premiações embutidos no layout.
- ❌ Carrosséis automáticos com rotação de 3 segundos que tiram o controle de leitura do usuário.
- ❌ Fontes cômicas, infantis, arredondadas ou mais de 3 pesos de fonte diferentes na mesma visão.
- ❌ Popups de newsletter agressivos com cronômetros de urgência ("Compre agora ou perca!").

### 6.3 Guia de Tom e Voz da UI (Clean UI Copy)

O estilo textual em interfaces inspiradas no Siteinspire deve espelhar a sobriedade de um curador de arte ou arquiteto sênior:
- **Precisão Cirúrgica**: Em vez de *"Conheça nossa seleção incrível de peças exclusivas"*, use *"Spring/Summer 2026 Collection — 14 Items"*.
- **Rótulos Funcionais Neutros**: Use *"Index"*, *"Filter"*, *"About"*, *"Contact"*, *"Colophon"*, *"Inquire"*.
- **Silêncio Verbal**: Menos adjetivos superlativos ("inovador", "líder de mercado", "revolucionário"); mais substantivos e dados factuais ("Concrete & Glass Pavilion, Zurich, 2024").
