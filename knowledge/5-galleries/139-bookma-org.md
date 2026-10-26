---
id: "bookma-org"
name: "Bookma!"
url: "https://bookma.org/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico:
  - "Japanese Contemporary Multi-Device Responsive Craft"
  - "Side-by-Side Dual-Screen Comparison (Simultaneous PC & Mobile/SP First-View Inspection)"
  - "Integrated Chromatic Taxonomy (Corner Palette Swatches & Color Scanning)"
  - "Bilingual Typographic Harmony (Kanji/Kana CJK + Latin Typography Pairing)"
  - "Micro-Grid Modularity & Asymmetric Japanese Editorial Layouts"
  - "Functional Minimalist Portfolio & Agency Directory"
  - "Tactile UI Navigation & Device-Adaptive Architecture"
densidade_informacao: "Alta/Utilitaria (Inspeção Técnica Comparativa Multi-Breakpoint)"
impacto_visual: "Editorial/Sofisticado & Pragmático/Analítico"
custo_computacional: "Baixo na galeria base (Imagens otimizadas WebP, lazy loading responsivo, CSS leve); Médio a Alto nos sites curados (Motion GSAP, WebGL, Smooth Scroll, Responsive Typography)"
stack_frameworks:
  - "WordPress / Headless REST API (Motor original do repositório bookma! v3)"
  - "Modern Responsive CSS Grid & Flexbox Layouts"
  - "Vanilla JavaScript / Vue.js / React nos ecossistemas de referência"
  - "Tailwind CSS & Utility-First Responsive Breakpoints"
  - "Next.js / Astro / Nuxt 3 (Nos projetos corporativos e de branding curados)"
compatibilidade:
  fontes_ideais:
    - "Fontes Japonesas Gothic (Sans): Noto Sans JP, Zen Kaku Gothic New, Hiragino Sans, Yu Gothic, LINE Seed JP"
    - "Fontes Japonesas Mincho (Serif): Shippori Mincho, Tsukushi Mincho, Yu Mincho, Noto Serif JP, Hina Mincho"
    - "Fontes Latinas Geométricas & Neo-Grotescas: Inter, Plus Jakarta Sans, Poppins, Outfit, Space Grotesk, Syne"
    - "Fontes Latinas Editoriais e Serifadas: Playfair Display, Cinzel, Cormorant Garamond, Newsreader"
    - "Fontes Monoespaçadas Técnicas: Geist Mono, JetBrains Mono, Space Mono, IBM Plex Mono"
  paletas_ideais:
    - "Washi Paper & Obsidian Ink (Light Core): #F8F9FA (Background Canvas), #FFFFFF (Surface Card), #E5E7EB (Hairline Border), #1A1A1A (Deep Sumi Ink), #6B7280 (Slate Subtext)"
    - "Japanese Indigo & Digital Cyan: #1B365D (Deep Aizome Indigo), #2563EB (Electric Blue Accent), #EBF2FE (Ice Blue Tint), #0F172A (Navy Carbon Base)"
    - "Matcha Herbal & Earth Warmth: #2D3A30 (Dark Moss), #5A6D5E (Botanical Sage), #F4F6F4 (Pale Green Tint), #DCE4DD (Soft Border)"
    - "Vermilion & Shuin Seal: #C82424 (Traditional Japanese Vermilion), #FA5252 (Coral Crimson), #FEF2F2 (Soft Rose Wash)"
    - "Amber Tea & Roasted Sencha: #92400E (Warm Ochre), #D97706 (Amber Spark), #FFFBEB (Pale Warm Linen)"
  combinacoes_recomendadas:
    - "Framer Motion com transições responsivas adaptadas e layout springs (`{ type: 'spring', stiffness: 300, damping: 30 }`)"
    - "Tailwind CSS com containers com `aspect-ratio` fixos para mockups PC (16:10 / 16:9) e SP (9:19.5)"
    - "Lucide React com ícones de traço fino (`strokeWidth={1.5}`) para seletores de viewport e tags"
    - "Radix UI / Headless UI para alternância fluida de abas e drawers de filtros taxonômicos"
  conflitos_esteticos:
    - "Design desktop centrado que ignora completamente a usabilidade e a ergonomia de toque em smartphones"
    - "Uso descuidado de fontes CJK pesadas não otimizadas que causam layout shifts agressivos (FOIT/FOUT severo)"
    - "Falta de hierarquia responsiva (apenas encolher elementos no mobile sem reestruturar o first-view)"
    - "Overlays intrusivos, modais bloqueantes de newsletter e pop-ups com contadores regressivos agressivos"
    - "Gradientes neon saturados genéricos de SaaS ocidental que colidem com a sutileza gráfica e o equilíbrio orgânico japonês"
---

# Bookma! (bookma.org) — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
██████╗  ██████╗  ██████╗ ██╗  ██╗███╗   ███╗ █████╗     ██╗
██╔══██╗██╔═══██╗██╔═══██╗██║ ██╔╝████╗ ████║██╔══██╗    ██║
██████╔╝██║   ██║██║   ██║█████═╝ ██╔████╔██║███████║    ██║
██╔══██╗██║   ██║██║   ██║██╔═██╗ ██║╚██╔╝██║██╔══██║    ╚═╝
██████╔╝╚██████╔╝╚██████╔╝██║ ╚██╗██║ ╚═╝ ██║██║  ██║    ██╗
╚═════╝  ╚═════╝  ╚═════╝ ╚═╝  ╚═╝╚═╝     ╚═╝╚═╝  ╚═╝    ╚═╝
     DUAL-SCREEN RESPONSIVE ARCHIVE & JAPANESE DESIGN CURATION
                 PLATFORM: BOOKMA! (BOOKMA.ORG)
```

---

## 1. DNA Estético & Filosofia de Curadoria

O **Bookma!** (`https://bookma.org/`), consolidado em sua versão de referência como **bookma! v3**, é uma das mais prestigiadas e funcionais plataformas japonesas de bookmarking, curadoria e análise de web design contemporâneo. Criado para atender às demandas de diretores de arte, designers de interface (UI) e engenheiros frontend de agências digitais no Japão, o Bookma! se estabeleceu como o padrão ouro na análise de **Web Design Responsivo Simultâneo**.

Enquanto a imensa maioria dos repositórios globais de design (como Awwwards, Siteinspire e Land-book) prioriza capturas de tela isoladas da visualização desktop widescreen — relegando a versão mobile a uma consideração secundária —, o **Bookma!** introduziu uma filosofia radicalmente pragmática: **o First View (FV / ファーストビュー) de um projeto contemporâneo só pode ser compreendido através da justaposição simultânea de suas interfaces Desktop (PC) e Smartphone (SP)**.

```
┌──────────────────────────────────────────────────────────────────────────────────────────────────┐
│                             THE BOOKMA! DUAL-SCREEN CURATORIAL PARADIGM                          │
├──────────────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                                  │
│   DESKTOP VIEW (PC)                      SMARTPHONE VIEW (SP)        CHROMATIC SWATCHES          │
│   ┌──────────────────────────────┐       ┌──────────────┐            ┌───┬───┬───┬───┐           │
│   │  Header / Full Nav / Hero    │       │ ☰  Logo  CTA │            │   │   │   │   │           │
│   │  Asymmetric Grid & Media     │       │ [Hero Media] │            └───┴───┴───┴───┘           │
│   │  Bilingual Tate-Gaki Type    │       │ Condensed CJK│            Extracted Primary &         │
│   │  Expansive White Space (Ma)  │       │ Bottom Nav   │            Accent Colors per Site      │
│   └──────────────────────────────┘       └──────────────┘                                        │
│                 ▲                                ▲                               ▲               │
│                 └────────────────────────────────┴───────────────────────────────┘               │
│                             SYNCHRONIZED MULTI-BREAKPOINT INSPECTION                             │
└──────────────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 Os Pilares Filosóficos da Curadoria Bookma!

1. **A Paridade Multi-Breakpoint (PC ↔ SP Synchronicity)**:
   No mercado japonês, onde mais de 80% do tráfego em e-commerce, recrutamento, serviços e entretenimento provém de dispositivos móveis, a transição entre telas não é um detalhe de responsividade técnica: é o próprio cerne da estratégia de design. O Bookma! documenta como layouts complexos, amplos e contemplativos no desktop se condensam de forma elegante e ultra-funcional no smartphone sem perder o DNA estético da marca.

2. **Identificação Cromática Instantânea (Corner Swatch Architecture)**:
   Cada card de projeto no Bookma! traz no rodapé ou no canto de sua moldura a paleta de cores dominante do site (geralmente de 3 a 5 hexadecimais principais). Isso permite que designers façam varreduras visuais ultra-rápidas para identificar combinações de cores bem-sucedidas em produção real, categorizadas por tom (monocromático, pastel, vívido, terra, escuro).

3. **Taxonomia Rigorosa Tripartite (Tipo de Site, Indústria e Estilo Visual)**:
   Ao contrário de galerias baseadas exclusivamente em curtidas de usuários, o Bookma! organiza seu acervo sob uma taxonomia estruturada de três eixos:
   - **Site Type (サイトタイプ)**: Corporate, EC, Portfolio, Brand, Media, Campaign/LP, Recruitment.
   - **Industry (業種)**: TI/Web, Gastronomia/Alimentos, Moda/Beleza, Saúde/Medicina, Educação, Imobiliário/Arquitetura, Cultura/Entretenimento.
   - **Taste & Aesthetic (テイスト)**: Simples, Flat, Elegante/Moderno, Pop/Colorido, Wa-fu (和風 - Tradicional Nipônico), Focado em Foto, Focado em Ilustração.

4. **Curadoria Focada em Produção Comercial Real e Alta Qualidade**:
   Diferente de plataformas de conceitos não implementados (como Dribbble), 100% dos sites listados no Bookma! são websites comerciais vivos, encomendados por marcas reais e produzidos por estúdios de ponta japoneses (como Garden Eight, SHIFTBRAIN, Mount Inc., BIRDMAN, baqemono.inc e homunculus).

5. **A Prevenção do "Layout Shift" Conceitual**:
   A visualização lado a lado do Bookma! educa o mercado sobre como evitar o erro de criar uma versão desktop magnífica que se transforma em uma lista genérica e sem alma no mobile. Ele destaca projetos que mantêm a inventividade tipográfica, micro-animações táteis e ritmo espacial em ambas as telas.

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

O **Bookma!** é a **Referência Primária de Direção de Arte e Arquitetura Frontend** sempre que o projeto exigir consistência multi-dispositivo irrepreensível, tipografia multilíngue refinada e ergonomia mobile nativa.

```
┌──────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                   IDEAL APPLICATION MATRIX                                       │
├────────────────────────────┬────────────────────────────────────┬────────────────────────────────┤
│ TIPO DE PROJETO            │ PAPEL NA REGRA 60-30-10            │ EFEITO PSICOLÓGICO NO USUÁRIO  │
├────────────────────────────┼────────────────────────────────────┼────────────────────────────────┤
│ E-Commerce D2C & Lifestyle │ 60% Fundo Washi / 30% Fotografia   │ Sofisticação sem fricção;      │
│ e Cosméticos               │ editorial / 10% Micro-CTA de cor   │ desejo de toque e compra fluida│
├────────────────────────────┼────────────────────────────────────┼────────────────────────────────┤
│ Landing Pages Corporativas │ 60% Grid Branco / 30% Tipografia   │ Alta credibilidade institucional│
│ & Portais de Recrutamento  │ CJK+Latin / 10% Acento Indigo/Selo │ e clareza informativa absoluta │
├────────────────────────────┼────────────────────────────────────┼────────────────────────────────┤
│ Portfólios de Estúdios e   │ 60% Espaço Negativo (Ma) / 30%     │ Vanguarda criativa silenciosa, │
│ Tecnologias Criativas      │ Mockups responsivos / 10% Motion   │ atenção extrema ao craft       │
├────────────────────────────┼────────────────────────────────────┼────────────────────────────────┤
│ Gastronomia, Hospitalidade │ 60% Tons Terrosos/Carvão / 30%     │ Conexão sensorial profunda com │
│ & Herança Cultural         │ Textura orgânica / 10% Vermilion   │ a tradição e o refinamento     │
└────────────────────────────┴────────────────────────────────────┴────────────────────────────────┘
```

### 2.1 Projetos de Aplicação Preferencial
- **Projetos Mobile-First de Alto Valor**: Projetos cujo público consome primariamente em telas verticais de smartphones (iOS/Android), mas que necessitam de uma presença de impacto em monitores widescreen de alta resolução (4K / Retina).
- **Sistemas de Recrutamento Corporativo (採用サイト)**: O Japão é pioneiro em criar sites de recrutamento imersivos, combinando entrevistas com funcionários, cronogramas de carreira, infográficos interativos e depoimentos fotográficos. O Bookma! é o melhor acervo para esse padrão.
- **Plataformas de E-Commerce Especializadas (ECサイト)**: Marcas de moda de autor, cerâmica, chás especiais, cutelaria e tecnologia pessoal que necessitam de checkout fluido sem perder o ritmo editorial de uma revista de luxo.
- **Sites com Escrita Vertical Híbrida (Tate-gaki)**: Projetos que incorporam títulos na vertical (`writing-mode: vertical-rl`) no desktop e precisam resolver com perfeição o colapso e o fluxo dessa tipografia em telas de 375px a 430px de largura.

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

⚠️ **Incompatível com**:
- **Dashboards SaaS B2B de Alta Densidade Numérica Ocidentais**: Aplicações de compliance, painéis de logs em tempo real (Datadog/AWS) e planilhas densas de trading financeiro não se beneficiam da contemplação espacial ou do ritmo editorial do estilo Bookma!.
- **Sites de Entretenimento Gamificado Full 3D / WebGL Exclusivo**: Experiências interativas que demandam acelerômetro, canvas em tela cheia sem texto ou games 3D nativos não cabem na matriz de comparação responsiva 2D documental do Bookma!.
- **Marketing de Afiliados e Infoprodutos de Venda Agressiva**: Páginas que utilizam táticas de escassez artificial (cronômetros vermelhos piscantes, botões gigantes com efeito de tremor contínuo, vídeo de vendas bloqueado sem barra de progresso) têm sua taxa de conversão prejudicada quando vestidas com a contenção minimalista japonesa.

⚠️ **Armadilhas de Imitação**:
- **Truncamento Categórico de Tipografia CJK**: Importar fontes japonesas completas (que possuem mais de 3.000 ideogramas kanji) via webfont sem configurar subsetting ou carregamento assíncrono causa travamentos graves de rendering e páginas em branco no primeiro carregamento.
- **"Mobile Shrinking" Mecânico**: Pegar uma composição desktop elaborada e simplesmente reduzir a escala (transform: scale) ou forçar 100% de largura sem repensar a ordem do DOM resulta em blocos de texto ilegíveis e botões com alvos de toque inferiores a 44x44px.
- **Uso Excessivo de Cores da Paleta Sem Hierarquia**: O fato do Bookma! documentar paletas cromáticas com 4 ou 5 cores não autoriza o uso caótico de todas elas em uma mesma dobra. O equilíbrio japonês exige a regra 60-30-10 rígida: 60% base neutra, 30% estrutura secundária e 10% acento pontual.

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

```
┌──────────────────────────────────────────────────────────────────────────────────────────────────┐
│                             ANATOMIA DA GRADE RESPONSIVA BOOKMA!                                 │
├──────────────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                                  │
│   DESKTOP (1440px Viewport)                   MOBILE BREAKPOINT (390px Viewport)                 │
│   ├── Outer Margin: 64px ──┤                  ├── Outer Margin: 20px ──┤                         │
│   ┌──────────────────────────────┐            ┌───────────────────────┐                          │
│   │ Col 1  Col 2  Col 3 ... Col12│            │ Col 1   Col 2   Col 3 │  (3-4 Col Fluid Grid)    │
│   │ ◄── Gutter: 24px/32px ─────► │            │ ◄─ Gutter: 12px ────► │                          │
│   │ [Brand]       [Nav Links]    │            │ [Brand]           [☰] │  Fixed App-like Bar      │
│   │ [Large Asymmetric Headline]  │            │ [Stacked Title]       │  Compact Typographic Lead│
│   │ [Hero Banner (16:10)]        │            │ [Hero Banner (4:5)]   │  Optimized Vertical Ratio│
│   └──────────────────────────────┘            └───────────────────────┘                          │
│                                                                                                  │
└──────────────────────────────────────────────────────────────────────────────────────────────────┘
```

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo

1. **Relação de Aspect Ratio Diferenciada por Breakpoint**:
   - No desktop, imagens heróicas adotam proporções cinematográficas horizontais (`16:10` ou `21:9`), permitindo que a tipografia respire ao lado ou em sobreposição parcial sutil.
   - No mobile, as mesmas imagens alternam inteligentemente para proporções verticais (`4:5`, `1:1` ou `9:16`), ocupando a área útil do polegar e garantindo legibilidade do produto sem exigir zoom.

2. **Espaçamento Negativo Deliberado (*Ma*)**:
   - Padding vertical generoso em seções de desktop (`py-24` a `py-36` / 96px a 144px), que se contrai proporcionalmente no mobile para (`py-12` a `py-16` / 48px a 64px) sem causar sensação de claustrofobia.
   - Separações estruturais feitas com linhas ultra-finas de 1 pixel (`border-t border-neutral-200/60` ou `#EBEBEB`), preservando a leveza arquitetônica sem recorrer a divisores pesados.

3. **Alinhamento Híbrido Horizontal-Vertical**:
   - Títulos de seção que utilizam `writing-mode: vertical-rl` no desktop se ancoram à direita ou à margem superior externa de blocos de imagem, enquanto no mobile passam por uma rotação fluida para horizontal ou formam uma coluna lateral de ícone e kanji minimalista.

---

### 4.2 Sistemas de Cores, Superfícies & Texturas

```
┌──────────────────────────────────────────────────────────────────────────────────────────────────┐
│                               THE BOOKMA! CHROMATIC SPECTRUM                                     │
├──────────────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                                  │
│   SURFACE / WASHI CANVAS      INK / CONTRAST TEXT        TRADITIONAL ACCENT   DIGITAL ACCENT     │
│   ┌─────────────────────┐    ┌─────────────────────┐    ┌─────────────────┐  ┌─────────────────┐ │
│   │ #F8F9FA             │    │ #1A1A1A             │    │ #C82424         │  │ #2563EB         │ │
│   │ Soft Off-White Silk │    │ Deep Charcoal Sumi  │    │ Shuin Stamp Red │  │ Indigo Electric │ │
│   └─────────────────────┘    └─────────────────────┘    └─────────────────┘  └─────────────────┘ │
│                                                                                                  │
│   SECONDARY MUTED SLATE       CARD CONTAINER BG          HAIRLINE DIVIDER     EARTH WARMTH       │
│   ┌─────────────────────┐    ┌─────────────────────┐    ┌─────────────────┐  ┌─────────────────┐ │
│   │ #6B7280             │    │ #FFFFFF             │    │ #E5E7EB         │  │ #92400E         │ │
│   │ Neutral Caption Gray│    │ Pure White Plate    │    │ 1px Border Line │  │ Roasted Tea/Soil│ │
│   └─────────────────────┘    └─────────────────────┘    └─────────────────┘  └─────────────────┘ │
│                                                                                                  │
└──────────────────────────────────────────────────────────────────────────────────────────────────┘
```

- **Fundo Principal (Canvas)**: O branco absoluto (`#FFFFFF`) é frequentemente substituído por tons suaves de papel washi ou névoa leve (`#F8F9FA`, `#F5F5F3` ou `#FAFAFA`), reduzindo o cansaço visual e criando um fundo acolhedor.
- **Tipografia e Contraste**: O texto corrido nunca é preto 100% puro (#000000), mas um carvão escuro natural (*Sumi Ink* `#1A1A1A` ou `#222222`), evitando contraste estourado e valorizando a suavidade do antialiasing.
- **Sombras Físicas**: Ausência quase total de sombras difusas exageradas. Utiliza-se planaridade refinada (*flat design* contemporâneo) com elevações resolvidas por linhas divisórias sutis de 1px ou sombras ultra-rasas (`box-shadow: 0 1px 3px rgba(0, 0, 0, 0.04)`).

---

### 4.3 Catálogo de 8 Arquétipos Concretos Extraídos do Bookma!

#### Arquétipo 1: Dual-Screen First View Hero (PC widescreen + SP vertical side-by-side)
- **Anatomia**: Bloco comparativo que apresenta o viewport desktop (proporção 16:10 em moldura de laptop ou browser minimalista) emparelhado com o viewport mobile (proporção 9:19.5 com cantos arredondados simulando smartphone moderno).
- **Gatilho de Interação**: Toggle interativo no topo da galeria ("Both" / "PC Only" / "SP Only") com transição de opacidade e escala em Framer Motion.
- **Onde Encaixar**: Hero de páginas de apresentação de cases, portfólios de design responsivo e landing pages de auditoria de UX.

#### Arquétipo 2: Responsive Navigation Morph (Desktop Spread ↔ Mobile Bottom Sheet)
- **Anatomia**: Barra de navegação que no desktop distribui categorias horizontalmente com tipografia bilíngue (Kanji principal + Katakana/English em subscrito de 10px), e no mobile se transforma em um dock inferior flutuante ou botão flutuante com abertura de *bottom sheet* ergonômico acessível ao polegar.
- **Gatilho de Interação**: Click no acionador com animação fluida de mola (`damping: 25, stiffness: 280`).
- **Onde Encaixar**: Header global e sistema de navegação de portais de conteúdo ou lojas virtuais.

#### Arquétipo 3: Chromatic Swatch Corner Badge (Palette Cards)
- **Anatomia**: Card de exibição do projeto contendo miniatura com cantos levemente arredondados (`rounded-md` de 6px), acompanhado por uma barra horizontal inferior ou flutuante no canto superior direito contendo de 3 a 5 pastilhas circulares ou retangulares com os códigos hexadecimais dominantes do site curado.
- **Gatilho de Interação**: Hover na pastilha exibe tooltip com o código HEX e botão "Copiar"; hover no card executa zoom suave na imagem (`scale: 1.03`).
- **Onde Encaixar**: Listagens de portfólio, catálogos de componentes, guias de estilo e galerias de inspiração visual.

#### Arquétipo 4: Tate-Gaki Vertical Headline Adaptativa
- **Anatomia**: Bloco tipográfico que no desktop renderiza título na vertical (`writing-mode: vertical-rl`) com caracteres kanji elegantes e letras latinas rotacionadas em `text-orientation: mixed`, e no mobile quebra suavemente para texto horizontal com barra lateral indicativa vermelha (*Shuin* accent).
- **Gatilho de Interação**: Scroll reveal sincronizado via Intersection Observer (`translateY: 0, opacity: 1`).
- **Onde Encaixar**: Aberturas de artigos editoriais, manifestos corporativos e seções "Sobre a Empresa".

#### Arquétipo 5: Multi-Device Product / Showcase Carousel
- **Anatomia**: Seção de showcase que no desktop apresenta grid assimétrico de 3 a 4 colunas com alturas variadas (*masonry* sutil), enquanto no smartphone converte-se automaticamente em um carrossel horizontal com deslizamento por toque (*CSS scroll-snap-type: x mandatory*).
- **Gatilho de Interação**: Arraste por toque no mobile com indicador de paginação em linha contínua progressiva.
- **Onde Encaixar**: Vitrines de produtos, seleção de estudos de caso e depoimentos de clientes.

#### Arquétipo 6: Asymmetric Japanese Editorial Spread
- **Anatomia**: Composição com imagem principal ocupando 7 colunas, bloco de texto explicativo sobreposto com fundo semi-transparente washi ocupando 5 colunas, e numeração serial técnica em fonte monoespaçada (`01 // CONCEPT`, `02 // EXECUTION`) posicionada nas calhas externas.
- **Gatilho de Interação**: Efeito parallax suave entre o plano da imagem e a caixa de texto durante a rolagem.
- **Onde Encaixar**: Seções de narrativa de marca (*Brand Story*), filosofia de produto e apresentação de liderança.

#### Arquétipo 7: Sticky Bottom Action Dock para Smartphones
- **Anatomia**: Barra de ação persistente na base da viewport mobile com altura ergonômica (64px), botão primário de conversão (ex: "Entrar em Contato" / "Comprar Agora") ocupando 75% da largura e botões de ação rápida (WhatsApp/Linha/Telefone) ocupando os 25% restantes com divisão de 1px.
- **Gatilho de Interação**: Ocultação automática suave no scroll para baixo e reaparição imediata no scroll para cima.
- **Onde Encaixar**: Fluxos de conversão mobile em landing pages comerciais e lojas online.

#### Arquétipo 8: Bilingual Micro-Footer com Ficha Técnica
- **Anatomia**: Rodapé de extrema leveza com divisão superior de 1px, contendo colunas para créditos de desenvolvimento, tipografias em uso, paleta de cores e links de navegação com tracking expandido (`letter-spacing: 0.1em`).
- **Gatilho de Interação**: Links com sublinhado animado que surge do centro para as extremidades no hover.
- **Onde Encaixar**: Rodapé institucional de portfólios, sites de estúdios criativos e plataformas de design.

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Tokens CSS & Design System Variables

Abaixo está o conjunto canônico de tokens CSS que materializa com fidelidade o ecossistema estético do **Bookma!**:

```css
:root {
  /* ==========================================================================
     BOOKMA! CHROMATIC TOKENS (LIGHT CORE & CONTEMPORARY WASHI)
     ========================================================================== */
  --bookma-bg-canvas: #f8f9fa;
  --bookma-bg-surface: #ffffff;
  --bookma-bg-surface-subtle: #f3f4f6;
  
  --bookma-text-primary: #1a1a1a;       /* Sumi Black Puro */
  --bookma-text-secondary: #4b5563;     /* Carvão Médio */
  --bookma-text-muted: #9ca3af;         /* Grafite Discreto */
  
  --bookma-border-hairline: rgba(229, 231, 235, 0.9);
  --bookma-border-focus: #1a1a1a;
  
  /* Cores de Destaque Típicas da Curadoria */
  --bookma-accent-indigo: #1b365d;      /* Aizome tradicional */
  --bookma-accent-blue: #2563eb;        /* Azul elétrico contemporâneo */
  --bookma-accent-vermilion: #c82424;   /* Selo Imperial Shuin */
  --bookma-accent-sage: #4a5d4e;        /* Verde musgo */
  --bookma-accent-ochre: #d97706;       /* Âmbar / Chá verde torrado */

  /* ==========================================================================
     TYPOGRAPHIC TOKENS (BILINGUAL CJK + LATIN SYSTEM)
     ========================================================================== */
  --bookma-font-sans-cjk: "Noto Sans JP", "Hiragino Sans", "Yu Gothic", sans-serif;
  --bookma-font-serif-cjk: "Shippori Mincho", "Yu Mincho", "Noto Serif JP", serif;
  --bookma-font-latin: "Inter", -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
  --bookma-font-mono: "Geist Mono", "JetBrains Mono", "Space Mono", monospace;

  /* ==========================================================================
     LAYOUT METRICS & RESPONSIVE PROPORTIONS
     ========================================================================== */
  --bookma-ratio-pc: 16 / 10;
  --bookma-ratio-sp: 9 / 19.5;
  --bookma-radius-card: 6px;
  --bookma-radius-pill: 9999px;
  --bookma-shadow-subtle: 0 1px 3px rgba(0, 0, 0, 0.04), 0 1px 2px rgba(0, 0, 0, 0.02);
  --bookma-shadow-hover: 0 10px 25px -5px rgba(0, 0, 0, 0.06), 0 8px 10px -6px rgba(0, 0, 0, 0.03);

  /* ==========================================================================
     MOTION PHYSICS (ORGANIC SENSORY EASING)
     ========================================================================== */
  --bookma-ease-out-cubic: cubic-bezier(0.215, 0.61, 0.355, 1);
  --bookma-ease-out-expo: cubic-bezier(0.19, 1, 0.22, 1);
  --bookma-duration-fast: 200ms;
  --bookma-duration-normal: 350ms;
  --bookma-duration-slow: 600ms;
}
```

---

### 5.2 Física de Movimento & Parâmetros de Interação

O Bookma! e os sites japoneses nele destacados distinguem-se pela rejeição total a movimentos bruscos, quiques artificiais exagerados (*bouncy*) ou transições mecânicas lineares. O movimento expressa polidez e suavidade orgânica:

```typescript
// Configurações de Mola e Transições para Framer Motion no ecossistema Bookma!
export const bookmaMotion = {
  // Transição suave para alternância de viewport (PC <-> SP)
  viewportToggle: {
    type: "spring",
    stiffness: 260,
    damping: 28,
    mass: 0.8
  },
  
  // Entrada suave de cards da galeria (Scroll Reveal)
  cardReveal: {
    duration: 0.55,
    ease: [0.215, 0.61, 0.355, 1] // EaseOutCubic Japonês
  },

  // Efeito sutil de zoom no hover de mockups
  imageZoom: {
    duration: 0.4,
    ease: [0.19, 1, 0.22, 1] // EaseOutExpo Ultra-Polido
  },

  // Flutuação de swatches e tooltips
  tooltipSpring: {
    type: "spring",
    stiffness: 400,
    damping: 30
  }
};
```

---

### 5.3 Implementação Funcional Completa: Componente `BookmaResponsiveShowcase`

O código React a seguir é uma implementação completa, moderna e pronta para produção que replica o padrão mestre do Bookma!: um visualizador simultâneo de viewport (Desktop ↔ Smartphone) com alternância fluida de visualização, inspeção cromática interativa via pastilhas no card, tags taxonômicas e transições orgânicas em Tailwind CSS e Framer Motion.

```tsx
import React, { useState } from 'react';
import { motion, AnimatePresence } from 'framer-motion';
import { Monitor, Smartphone, Layers, ExternalLink, Copy, Check, Filter } from 'lucide-react';

// Tipagem rigorosa da curadoria Bookma!
export interface CuratedSiteItem {
  id: string;
  title: string;
  clientOrAgency: string;
  category: 'Corporate' | 'EC' | 'Portfolio' | 'Brand' | 'Campaign' | 'Recruit';
  industry: 'IT & Web' | 'Fashion & Beauty' | 'Food & Living' | 'Architecture';
  taste: string[];
  url: string;
  pcImage: string;
  spImage: string;
  palette: {
    hex: string;
    role: string;
  }[];
}

interface BookmaResponsiveShowcaseProps {
  items?: CuratedSiteItem[];
}

export const BookmaResponsiveShowcase: React.FC<BookmaResponsiveShowcaseProps> = ({
  items = defaultCuratedItems
}) => {
  // Modos de visualização do Bookma!: 'both' (Dual Screen), 'pc' (Desktop Only), 'sp' (Mobile Only)
  const [viewMode, setViewMode] = useState<'both' | 'pc' | 'sp'>('both');
  const [copiedHex, setCopiedHex] = useState<string | null>(null);
  const [selectedCategory, setSelectedCategory] = useState<string>('All');

  const copyToClipboard = (hex: string) => {
    navigator.clipboard.writeText(hex);
    setCopiedHex(hex);
    setTimeout(() => setCopiedHex(null), 1800);
  };

  const filteredItems = selectedCategory === 'All' 
    ? items 
    : items.filter(item => item.category === selectedCategory);

  return (
    <div className="w-full min-h-screen bg-[#F8F9FA] text-[#1A1A1A] font-sans antialiased py-8 px-4 sm:px-6 lg:px-12">
      {/* ====================================================================
          BARRA DE CONTROLE SUPERIOR (CURATORIAL TOOLBAR ESTILO BOOKMA!)
          ==================================================================== */}
      <header className="max-w-7xl mx-auto mb-10 pb-6 border-b border-neutral-200">
        <div className="flex flex-col md:flex-row md:items-center md:justify-between gap-6">
          <div>
            <div className="flex items-center gap-3">
              <span className="text-xs font-mono tracking-widest uppercase bg-neutral-900 text-white px-2 py-0.5 rounded">
                BOOKMA! ARCHIVE
              </span>
              <span className="text-xs text-neutral-400 font-mono">v3.0 // DUAL-VIEW ENGINE</span>
            </div>
            <h1 className="text-2xl sm:text-3xl font-medium tracking-tight mt-1 text-neutral-900">
              Responsive Design Inspection Gallery
            </h1>
            <p className="text-sm text-neutral-500 mt-1 max-w-xl">
              Análise comparativa de first-view desktop e mobile com taxonomia cromática e tipografia bilíngue.
            </p>
          </div>

          {/* Seletor de Modo de Visualização (Both / PC / SP) */}
          <div className="flex items-center bg-white p-1 rounded-lg border border-neutral-200/80 shadow-sm">
            <button
              onClick={() => setViewMode('both')}
              className={`flex items-center gap-1.5 px-3 py-1.5 text-xs font-medium rounded-md transition-all ${
                viewMode === 'both'
                  ? 'bg-neutral-900 text-white shadow-sm'
                  : 'text-neutral-600 hover:text-neutral-900 hover:bg-neutral-100'
              }`}
            >
              <Layers className="w-3.5 h-3.5" />
              <span>Dual View (PC + SP)</span>
            </button>
            <button
              onClick={() => setViewMode('pc')}
              className={`flex items-center gap-1.5 px-3 py-1.5 text-xs font-medium rounded-md transition-all ${
                viewMode === 'pc'
                  ? 'bg-neutral-900 text-white shadow-sm'
                  : 'text-neutral-600 hover:text-neutral-900 hover:bg-neutral-100'
              }`}
            >
              <Monitor className="w-3.5 h-3.5" />
              <span>PC Only</span>
            </button>
            <button
              onClick={() => setViewMode('sp')}
              className={`flex items-center gap-1.5 px-3 py-1.5 text-xs font-medium rounded-md transition-all ${
                viewMode === 'sp'
                  ? 'bg-neutral-900 text-white shadow-sm'
                  : 'text-neutral-600 hover:text-neutral-900 hover:bg-neutral-100'
              }`}
            >
              <Smartphone className="w-3.5 h-3.5" />
              <span>SP Only</span>
            </button>
          </div>
        </div>

        {/* Filtros de Taxonomia Rápida (Categorias Bookma!) */}
        <div className="flex items-center gap-2 mt-6 overflow-x-auto pb-2 scrollbar-none text-xs">
          <Filter className="w-3.5 h-3.5 text-neutral-400 mr-1 flex-shrink-0" />
          {['All', 'Corporate', 'EC', 'Portfolio', 'Brand', 'Campaign', 'Recruit'].map((cat) => (
            <button
              key={cat}
              onClick={() => setSelectedCategory(cat)}
              className={`px-3 py-1 rounded-full border transition-colors whitespace-nowrap ${
                selectedCategory === cat
                  ? 'bg-neutral-900 text-white border-neutral-900 font-medium'
                  : 'bg-white text-neutral-600 border-neutral-200 hover:border-neutral-400'
              }`}
            >
              {cat}
            </button>
          ))}
        </div>
      </header>

      {/* ====================================================================
          GRID PRINCIPAL DE CARDS COMPARATIVOS (BOOKMA! CARDS)
          ==================================================================== */}
      <main className="max-w-7xl mx-auto space-y-12">
        {filteredItems.map((item) => (
          <article
            key={item.id}
            className="bg-white border border-neutral-200/80 rounded-xl p-5 shadow-[0_1px_3px_rgba(0,0,0,0.04)] hover:shadow-[0_10px_25px_-5px_rgba(0,0,0,0.06)] transition-all duration-300"
          >
            {/* Topo do Card: Informações e Metadados */}
            <div className="flex flex-col sm:flex-row sm:items-center justify-between gap-3 pb-4 mb-4 border-b border-neutral-100">
              <div>
                <div className="flex items-center gap-2">
                  <span className="text-[11px] font-mono uppercase text-neutral-500 bg-neutral-100 px-2 py-0.5 rounded">
                    {item.category}
                  </span>
                  <span className="text-xs text-neutral-400">•</span>
                  <span className="text-xs text-neutral-500">{item.industry}</span>
                </div>
                <h2 className="text-lg font-semibold text-neutral-900 mt-0.5">
                  {item.title}
                </h2>
                <span className="text-xs text-neutral-400 block font-mono">
                  Crafted by: {item.clientOrAgency}
                </span>
              </div>

              {/* Tags de Estilo e Link Externo */}
              <div className="flex items-center gap-3">
                <div className="hidden md:flex items-center gap-1.5">
                  {item.taste.map((tag) => (
                    <span
                      key={tag}
                      className="text-[10px] text-neutral-500 bg-neutral-50 border border-neutral-200/60 px-2 py-0.5 rounded"
                    >
                      #{tag}
                    </span>
                  ))}
                </div>
                <a
                  href={item.url}
                  target="_blank"
                  rel="noopener noreferrer"
                  className="inline-flex items-center gap-1 text-xs text-blue-600 hover:text-blue-800 font-medium ml-2"
                >
                  <span>Visit Site</span>
                  <ExternalLink className="w-3.5 h-3.5" />
                </a>
              </div>
            </div>

            {/* Visualizador Comparativo Dinâmico de Viewport */}
            <div className="bg-[#F3F4F6] rounded-lg p-4 sm:p-6 flex items-center justify-center min-h-[380px] overflow-hidden">
              <div className="flex flex-col lg:flex-row items-center justify-center gap-6 w-full max-w-5xl">
                
                {/* 1. MOCKUP DESKTOP (PC) */}
                <AnimatePresence mode="popLayout">
                  {(viewMode === 'both' || viewMode === 'pc') && (
                    <motion.div
                      layout
                      initial={{ opacity: 0, scale: 0.96 }}
                      animate={{ opacity: 1, scale: 1 }}
                      exit={{ opacity: 0, scale: 0.96 }}
                      transition={{ duration: 0.35, ease: [0.215, 0.61, 0.355, 1] }}
                      className={`relative bg-neutral-900 rounded-lg p-2.5 shadow-xl border border-neutral-800 transition-all ${
                        viewMode === 'pc' ? 'w-full max-w-4xl' : 'w-full lg:w-[68%]'
                      }`}
                    >
                      {/* Top Bar do Navegador Minimalista */}
                      <div className="flex items-center justify-between px-2 pb-2 text-[10px] text-neutral-400 border-b border-neutral-800 mb-2">
                        <div className="flex items-center gap-1.5">
                          <div className="w-2.5 h-2.5 rounded-full bg-neutral-700" />
                          <div className="w-2.5 h-2.5 rounded-full bg-neutral-700" />
                          <div className="w-2.5 h-2.5 rounded-full bg-neutral-700" />
                        </div>
                        <span className="font-mono text-neutral-500 truncate max-w-[200px]">
                          {item.url.replace('https://', '')}
                        </span>
                        <span className="text-[10px] font-mono text-neutral-500">1440 × 900</span>
                      </div>

                      {/* Janela de Conteúdo PC */}
                      <div className="relative aspect-[16/10] overflow-hidden rounded bg-neutral-100 group">
                        <img
                          src={item.pcImage}
                          alt={`${item.title} Desktop View`}
                          className="w-full h-full object-cover object-top transition-transform duration-700 ease-[cubic-bezier(0.19,1,0.22,1)] group-hover:scale-105"
                          loading="lazy"
                        />
                        <div className="absolute inset-0 bg-black/10 opacity-0 group-hover:opacity-100 transition-opacity duration-300 pointer-events-none" />
                      </div>
                    </motion.div>
                  )}
                </AnimatePresence>

                {/* 2. MOCKUP SMARTPHONE (SP) */}
                <AnimatePresence mode="popLayout">
                  {(viewMode === 'both' || viewMode === 'sp') && (
                    <motion.div
                      layout
                      initial={{ opacity: 0, scale: 0.96 }}
                      animate={{ opacity: 1, scale: 1 }}
                      exit={{ opacity: 0, scale: 0.96 }}
                      transition={{ duration: 0.35, ease: [0.215, 0.61, 0.355, 1] }}
                      className={`relative bg-neutral-900 rounded-[28px] p-2.5 shadow-2xl border-2 border-neutral-800 transition-all ${
                        viewMode === 'sp' ? 'w-full max-w-[320px]' : 'w-[240px] sm:w-[260px] flex-shrink-0'
                      }`}
                    >
                      {/* Notch / Dynamic Island */}
                      <div className="absolute top-4 left-1/2 -translate-x-1/2 w-16 h-3.5 bg-neutral-800 rounded-full z-20" />
                      
                      {/* Tela Mobile */}
                      <div className="relative aspect-[9/19.5] overflow-hidden rounded-[20px] bg-neutral-100 group">
                        <img
                          src={item.spImage}
                          alt={`${item.title} Mobile View`}
                          className="w-full h-full object-cover object-top transition-transform duration-700 ease-[cubic-bezier(0.19,1,0.22,1)] group-hover:scale-105"
                          loading="lazy"
                        />
                        <div className="absolute inset-0 bg-black/10 opacity-0 group-hover:opacity-100 transition-opacity duration-300 pointer-events-none" />
                      </div>
                      
                      {/* Barra Inferior de Home */}
                      <div className="w-20 h-1 bg-neutral-700 rounded-full mx-auto mt-2" />
                    </motion.div>
                  )}
                </AnimatePresence>
              </div>
            </div>

            {/* ================================================================
                RODAPÉ DO CARD: PALETA CROMÁTICA INTEGRADA (BOOKMA! SWATCHES)
                ================================================================ */}
            <div className="mt-4 pt-3 flex flex-col sm:flex-row sm:items-center justify-between gap-3">
              <div className="flex items-center gap-3">
                <span className="text-xs font-mono text-neutral-400">Color Palette:</span>
                <div className="flex items-center gap-2">
                  {item.palette.map((color) => (
                    <button
                      key={color.hex}
                      onClick={() => copyToClipboard(color.hex)}
                      title={`${color.role}: ${color.hex} (Click to copy)`}
                      className="group relative flex items-center gap-1.5 py-1 px-2 rounded-md hover:bg-neutral-100 border border-neutral-200/60 transition-colors"
                    >
                      <span
                        className="w-3.5 h-3.5 rounded-full border border-black/10 shadow-inner flex-shrink-0"
                        style={{ backgroundColor: color.hex }}
                      />
                      <span className="text-[11px] font-mono text-neutral-600 group-hover:text-neutral-900">
                        {color.hex}
                      </span>
                      {copiedHex === color.hex ? (
                        <Check className="w-3 h-3 text-emerald-600 animate-in fade-in" />
                      ) : (
                        <Copy className="w-3 h-3 text-neutral-300 group-hover:text-neutral-500 opacity-0 group-hover:opacity-100 transition-opacity" />
                      )}
                    </button>
                  ))}
                </div>
              </div>

              <div className="text-right">
                <span className="text-[11px] font-mono text-neutral-400">
                  Responsive Index: 100% Mobile Optimized
                </span>
              </div>
            </div>
          </article>
        ))}
      </main>
    </div>
  );
};

// ============================================================================
// DADOS DE REFERÊNCIA REALISTAS BASEADOS NO CATÁLOGO DO BOOKMA!
// ============================================================================
const defaultCuratedItems: CuratedSiteItem[] = [
  {
    id: 'shiro-fragrance',
    title: 'SHIRO Fragrance & Skincare',
    clientOrAgency: 'Mount Inc. Tokyo',
    category: 'Brand',
    industry: 'Fashion & Beauty',
    taste: ['Minimal', 'Photo-Driven', 'Clean'],
    url: 'https://shiro-shiro.jp/',
    pcImage: 'https://images.unsplash.com/photo-1522337360788-8b13dee7a37e?w=1200&auto=format&fit=crop&q=80',
    spImage: 'https://images.unsplash.com/photo-1522337360788-8b13dee7a37e?w=600&auto=format&fit=crop&q=80',
    palette: [
      { hex: '#F9F9F8', role: 'Washi Linen Base' },
      { hex: '#222222', role: 'Sumi Charcoal Type' },
      { hex: '#8C9A8E', role: 'Botanical Sage Accent' },
      { hex: '#D1D5DB', role: 'Hairline Divider' }
    ]
  },
  {
    id: 'kyoto-ryokan-zen',
    title: 'Sowaka Kyoto Boutique Luxury Hotel',
    clientOrAgency: 'Garden Eight',
    category: 'Corporate',
    industry: 'Architecture',
    taste: ['Wa-fu', 'Editorial', 'Tate-gaki'],
    url: 'https://sowaka.com/',
    pcImage: 'https://images.unsplash.com/photo-1493976040374-85c8e12f0c0e?w=1200&auto=format&fit=crop&q=80',
    spImage: 'https://images.unsplash.com/photo-1493976040374-85c8e12f0c0e?w=600&auto=format&fit=crop&q=80',
    palette: [
      { hex: '#1C1C1E', role: 'Obsidian Roof Tile' },
      { hex: '#F4EFEA', role: 'Shoji Paper Canvas' },
      { hex: '#C82424', role: 'Vermilion Seal Accent' },
      { hex: '#7C6A59', role: 'Cedar Wood Neutral' }
    ]
  },
  {
    id: 'tokyo-creative-tech',
    title: 'Party Inc. Creative Invention Studio',
    clientOrAgency: 'Party Interactive Lab',
    category: 'Portfolio',
    industry: 'IT & Web',
    taste: ['Stylish', 'Motion', 'Bilingual'],
    url: 'https://prty.jp/',
    pcImage: 'https://images.unsplash.com/photo-1550745165-9bc0b252726f?w=1200&auto=format&fit=crop&q=80',
    spImage: 'https://images.unsplash.com/photo-1550745165-9bc0b252726f?w=600&auto=format&fit=crop&q=80',
    palette: [
      { hex: '#FFFFFF', role: 'Pure Laboratory White' },
      { hex: '#111827', role: 'Black Ink Contrast' },
      { hex: '#2563EB', role: 'Digital Electric Blue' },
      { hex: '#E5E7EB', role: 'Modular Border' }
    ]
  }
];
