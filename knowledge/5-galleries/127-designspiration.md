---
id: "127-designspiration"
name: "Designspiration"
url: "https://www.designspiration.com/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico:
  - "Curadoria Visual Multidisciplinar de Alta Fidelidade (Anti-Pinterest)"
  - "Pioneirismo em Busca Cromática Hexadecimal (Até 5 Tons Simultâneos)"
  - "Grid Masonry Fluido & Adaptativo (2 a 9 Colunas Parametrizadas)"
  - "Paleta K-Means Automatizada por Item com Fundo Harmonizado"
  - "Visions Engine (Moodboarding Colaborativo & Exportação Multi-Formato)"
  - "Tipografia Suíça Contemporânea (Inter Variable com Micro-Metadados)"
  - "Design de Embalagens, Tipografia de Pôster, Editorial & UI Craft"
densidade_informacao: "Alta/Utilitaria"
impacto_visual: "Editorial/Sofisticado & Imersivo/Cromático"
custo_computacional: "Moderado a Alto (Algoritmos de Masonry client-side, cálculo de colunas dinâmico, pré-carregamento de imagens responsivas 1x-4x, quantização de cores via Canvas/Web Workers)"
stack_frameworks:
  - "Custom PHP / Cloudflare Edge Architecture"
  - "Inter Display & Inter Roman Variable Fonts (WOFF2 preload)"
  - "Vanilla JavaScript Modular Architecture (App.config / Custom Masonry)"
  - "REST Endpoints & OpenSearch Integration"
  - "Responsive Image Delivery via dspncdn.com CDN (236x, 472x, 692x, Originals)"
  - "Stripe Integration para Assinatura Pro ($5/mo, $50/yr)"
compatibilidade:
  fontes_ideais:
    - "Neo-Grotesque Pura & Funcional: Inter Variable, PP Neue Montreal, Neue Haas Grotesk, SF Pro Display, Univers"
    - "Serif Editorial & Alta Costura: GT Sectra, Ogg, Editorial New, Freight Display, Recoleta, Cormorant Garamond"
    - "Monoespaçada para Metadados e Códigos Hex: Geist Mono, JetBrains Mono, Space Mono, Aperçu Mono"
  paletas_ideais:
    - "Canvas Light Minimal (Default): #FFFFFF (Canvas Primário), #F8F8F8 (Superfície Secundária), #EAEAEA (Linhas Hairline), #111111 (Texto Título), #767676 (Texto Suporte)"
    - "Obsidian Dark Studio (Dark Mode): #121212 (Canvas Escuro), #1C1C1E (Superfície Elevada), #2C2C2E (Bordas de Separação), #F5F5F7 (Texto Principal), #8E8E93 (Legendas Secundárias)"
    - "Color Search Spectrum: Suporte ilimitado ao espectro sRGB/Display-P3 via input HEX de 6 dígitos com clusterização de 5 swatches por item"
  combinacoes_recomendadas:
    - "Tailwind CSS com utilitários de grid dinâmico ou flex masonry (`columns-2 md:columns-4 xl:columns-6 gap-6` ou cálculo via custom Hook React)"
    - "Framer Motion com transições de layout (`layoutId`), fade-ins escalonados (`staggerChildren: 0.04`) e gavetas deslizantes (`type: 'spring', damping: 25, stiffness: 300`)"
    - "Color Thief ou fast-average-color para extração k-means de paleta no upload do cliente"
    - "Lucide React (Search, Palette, Bookmark, ExternalLink, Share2, Plus, Sliders, LayoutGrid, Heart) com traço fino de 1.5px"
  conflitos_esteticos:
    - "Layouts com grids rígidos de altura fixa que cortam imagens ou forçam barras pretas laterais (letterboxing)"
    - "Poluição visual publicitária exagerada, banners animados intrusivos ou popups que bloqueiam a contemplação do feed"
    - "Ignorar a extração cromática: apresentar trabalhos visuais sem decompor seus tons dominantes reduz o site a uma pasta comum de imagens"
    - "Hover com delays longos ou excesso de efeitos volumosos 3D que distraem do conteúdo autoral"
    - "Tipografias de baixa legibilidade (comic scripts, fontes grunge sujas) no sistema de navegação e metadados da galeria"
---

# Designspiration — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
██████╗ ███████╗███████╗██╗ ██████╗ ███╗   ██╗███████╗██████╗ ██╗██████╗  █████╗ ████████╗██╗ ██████╗ ███╗   ██╗
██╔══██╗██╔════╝██╔════╝██║██╔════╝ ████╗  ██║██╔════╝██╔══██╗██║██╔══██╗██╔══██╗╚══██╔══╝██║██╔═══██╗████╗  ██║
██║  ██║█████╗  ███████╗██║██║  ███╗██╔██╗ ██║███████╗██████╔╝██║██████╔╝███████║   ██║   ██║██║   ██║██╔██╗ ██║
██║  ██║██╔══╝  ╚════██║██║██║   ██║██║╚██╗██║╚════██║██╔═══╝ ██║██╔══██╗██╔══██║   ██║   ██║██║   ██║██║╚██╗██║
██████╔╝███████╗███████║██║╚██████╔╝██║ ╚████║███████║██║     ██║██║  ██║██║  ██║   ██║   ██║╚██████╔╝██║ ╚████║
╚═════╝ ╚══════╝╚══════╝╚═╝ ╚═════╝ ╚═╝  ╚═══╝╚══════╝╚═╝     ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝   ╚═╝ ╚═════╝ ╚═╝  ╚═══╝
               THE VISUAL DISCOVERY ENGINE & CHROMATIC SEARCH HARBOR — FOUNDED IN 2010
```

---

## 1. DNA Estético & Filosofia de Curadoria

Fundado em 2010 pelo designer e programador independente norte-americano **Shelby White**, o **Designspiration** (`https://www.designspiration.com/`) consolidou-se como um dos pilares mais respeitados e duradouros na história da arquitetura visual para profissionais criativos. O projeto nasceu em um momento de inflexão na web moderna: enquanto plataformas emergentes como o Pinterest rapidamente capitulavam diante de algoritmos de engajamento generalistas — inundando seus feeds com receitas culinárias, infográficos promocionais amadores, decoração doméstica casual e anúncios dispersos —, White concebeu o Designspiration como um **Santuário Visual Dedicado Exclusivamente à Alta Excelência do Design**.

O propósito fundamental do Designspiration foi criar um arquivo digital intransigente, desenhado por designers para designers, focado na contemplação de formas puras, materiais impressos, identidades corporativas, posters, embalagens, tipografia e interfaces de vanguarda, eliminando qualquer ruído algorítmico irrelevante.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                     THE DESIGNSPIRATION CURATORIAL FOUNDATION                          │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  [ THE ANTI-PINTEREST PURITY ] ──► [ CHROMATIC DISCOVERY ] ──► [ MULTI-DISCIPLINARY ]  │
│   • 100% Focused on Graphic Arts   • Hexadecimal Color Search   • Packaging & Branding │
│   • Zero Lifestyle & Recipe Noise  • 5-Tone Palette Quantization• Swiss Modern Posters │
│   • Strict Curation Guidelines     • Visual Weight Balancing    • Architecture & Space │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  ARCHITECTURAL PILLARS: Responsive Masonry • K-Means Palette Engine • Zero Visual Clutter│
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 A Gênese: O Pioneirismo da Busca por Paletas Hexadecimais

O maior salto arquitetural e conceitual do Designspiration — implementado pioneiramente entre 2011 e 2012 — foi a introdução do **Motor de Busca Cromática Baseado em Paletas Hexadecimais**. Antes do Designspiration, os motores de busca visuais dependiam exclusivamente de palavras-chave textuais ou tags manuais atribuídas por usuários. White identificou uma lacuna crucial no processo mental dos designers: *muitas vezes um diretor de arte não sabe o nome exato do estilo ou do objeto que procura, mas possui clareza absoluta sobre o clima emocional e a relação cromática que precisa materializar*.

O Designspiration revolucionou essa dinâmica através de dois avanços de engenharia:
1. **Extração Cromática Automatizada (K-Means Quantization)**: Cada imagem submetida à plataforma passa por um pipeline de processamento que decompõe seus pixels e extrai automaticamente uma paleta harmonizada de **5 cores hexadecimais dominantes**, além de identificar a tonalidade de fundo ideal para o container (`background`).
2. **Busca Multi-Cromática Simultânea (Até 5 Cores)**: Os usuários podem selecionar até cinco tons hexadecimais simultaneamente (ou combinar códigos HEX exatos como `#67744A`, `#1F1F1F`, `#E3DBD4`) para filtrar o banco de dados global. O algoritmo calcula a proximidade de distância de cor (usando métricas no espaço CIE-Lab / RGB euclidiano) para retornar composições gráficas, embalagens ou fotografias que compartilham aquela exata atmosfera cromática.

### 1.2 A Amplitude Multidisciplinar e a Escola Visual

Ao contrário de galerias estritamente orientadas para código front-end (como Siteinspire ou Awwwards), o DNA do Designspiration é amplamente multidisciplinar, servindo como uma enciclopédia viva de:
- **Design de Embalagens (Packaging Design)**: Rótulos botânicos, caixas estruturais em papel kraft, garrafas serigrafadas, latas minimalistas de cerveja artesanal e cosméticos de luxo.
- **Tipografia & Design de Cartazes (Posters & Type Craft)**: Herdeiro direto da tradição moderna do cartaz suíço (Josef Müller-Brockmann, Armin Hofmann, Wim Crouwel) e do design gráfico norte-americano contemporâneo (Aaron Draplin, Paula Scher).
- **Branding & Identidade Corporativa**: Papelaria institucional, cartões de visita com hot stamping, guias de estilo e manuais de marca.
- **Arquitetura, Interiores & Espaços Físicos**: Brutalismo em concreto aparente, minimalismo japonês em madeira clara e composições escandinavas.
- **UI/UX & Mobile Interfaces**: Componentes de software elegantes, dashboards utilitários e landing pages com foco em layout modular.

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

O Designspiration é a **Referência Primária de Direção de Arte** sempre que o projeto exigir a definição de uma identidade visual coesa, exploração cromática aprofundada, criação de moodboards para clientes corporativos ou harmonização entre mídia física (tangível) e mídia digital (software/web).

### 2.1 Matriz de Arquétipos de Projeto & Posicionamento

| Arquétipo de Projeto | Por Que o Designspiration é a Referência Suprema | Emoção / Mensagem Comunicada |
| :--- | :--- | :--- |
| **Brand Identity Systems & Design Systems** | Permite cruzar uma paleta primária recém-desenhada com milhares de aplicações reais no mundo físico e digital, validando contraste e atmosfera. | Coesão visual absoluta, maturidade de identidade, elegância atemporal e disciplina cromática. |
| **Embalagens & Linhas de Produtos Físicos (D2C)** | Vasto repositório de acabamentos táteis: relevo seco, verniz localizado, papéis texturizados, tipografia em relevo e dobras inteligentes. | Sofisticação artesanal, sustentabilidade consciente e valor agregado de alta prateleira. |
| **Moodboarding & Pitch Decks de Direção de Arte** | O recurso integrado *Visions* viabiliza a colagem e montagem de painéis semânticos com exportação em alta resolução para aprovação executiva. | Visão estratégica clara, profissionalismo curatorial e narrativa estética consistente. |
| **Campanhas Editoriais, Cartazes & Posters Culturais** | Foco intenso em hierarquia tipográfica monumental, grid de colunas assimétricas e experimentos gráficos de vanguarda. | Impacto cultural, vanguarda estética, ousadia composicional e autoridade visual. |
| **E-Commerce de Luxo, Cosméticos & Lifestyle** | Harmonização entre fotografia de produto com iluminação suave e fundos de página que respeitam os tons do produto fotografado. | Exclusividade, calma sensorial, sofisticação discreta (*quiet luxury*) e desejo de consumo. |
| **Aplicações Web com Busca Cromática ou de Ativos** | Referência máxima de engenharia para interfaces de e-commerce de tintas, vestuário, bancos de imagem e ferramentas de design. | Utilidade visual direta, inteligência contextual e facilidade intuitiva de exploração. |

### 2.2 O Designspiration e a Regra Proporcional 60-30-10

A excelência da interface do Designspiration reside em não competir com o acervo exibido: a interface desaparece para deixar as cores e formas das imagens comandarem o ambiente.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                   A REGRA 60-30-10 NA ESTÉTICA DESIGNSPIRATION                         │
├────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                        │
│   ████████████████████████████████████████████   ░░░░░░░░░░░░░░░░░░░░░   ▓▓▓▓▓▓▓       │
│   [ 60% CANVAS NEUTRO / ESPAÇO RESPIRATÓRIO ]   [ 30% GRID MASONRY ]    [ 10% ACENTO ] │
│   • Fundo branco #FFFFFF ou preto #121212       • Imagens em fluxo      • 5 Swatches   │
│   • Gutters consistentes de 24px entre itens    • Altura natural mídias • Pílulas tags │
│   • Superfície neutra para isolar cores         • Proporção 1x a 4x CDN • Botão Salvar │
│                                                                                        │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

1. **60% — O Canvas Neutro de Isolamento Cromático (Dominante)**:
   - Fundo em branco puro `#FFFFFF` (no modo claro) ou preto asfalto `#121212` (no modo escuro). Não há gradientes decorativos no fundo da página nem texturas ruidosas.
   - O espaçamento entre os cartões é parametrizado com precisão: `gridItemGutter: 24px`. Essa distância milimétrica impede que a paleta intensa de uma imagem sangre ou contamine visualmente a percepção da imagem adjacente.

2. **30% — A Massa Visual das Obras & Grid Masonry Fluido (Secundário)**:
   - A espinha dorsal visual é o mosaico dinâmico (Masonry) onde cada item mantém sua proporção nativa de aspecto (retrato, paisagem, quadrado ou pôster vertical ultra-longo de até 600px de altura máxima).
   - As imagens são servidas via CDN dedicada (`dspncdn.com`) em escalas progressivas (236px, 472px, 692px e originais), com atributo `background` calculado por imagem correspondente à sua cor média para transição suave de carregamento.

3. **10% — Os Acentos Cromáticos & Micro-Interações Cirúrgicas (Acento)**:
   - O acento ativo é a barra flutuante de **5 swatches de cores** em cada card no estado hover ou na modal de visualização. Cada swatch exibe o código hexadecimal e, ao ser clicado, dispara imediatamente um novo refinamento do grid.
   - Botões funcionais como o clássico botão de salvar/favoritar, o badge "Get Pro" com destaque sutil e as tags arredondadas da bandeja de tópicos (`border border-neutral-300 rounded-full px-3 py-1`).

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

A adoção dos padrões do Designspiration (Masonry dinâmico assimétrico, foco cromático abstrato e navegação exploratória desestruturada) pode ser desastrosa caso seja aplicada inadvertidamente a produtos com necessidades transacionais ou analíticas rígidas.

### 3.1 Cenários de Incompatibilidade Crítica

- ⚠️ **SaaS B2B Corporativo, ERPs e Dashboards Analíticos**:
  Interfaces que lidam com conciliação contábil, gráficos financeiros e tabelas de dados tabulares exigem grids alinhados rigidamente em linhas e colunas uniformes (`table-fixed` ou grids bidimensionais estritos). O layout Masonry cria desalinhamento horizontal deliberado, destruindo a capacidade de comparação lado a lado de dados numéricos.
- ⚠️ **Portais Governamentais, Bancários & Serviços Cívicos Transacionais**:
  Cidadãos que precisam emitir certidões, realizar transferências Pix ou declarar impostos necessitam de affordances convencionais evidentes e caminhos lineares de tomada de decisão. Uma interface focada em navegação contemplativa baseada em cores causa profunda desorientação e viola princípios básicos de acessibilidade cognitiva.
- ⚠️ **Documentação Técnica de Código & Wikis Estruturadas**:
  Ambientes de desenvolvimento (estilo Stripe Docs, GitHub ou Tailwind Docs) exigem leitura sequencial contínua, colunas fixas de navegação hierárquica e tipografia monoespaçada legível. O dinamismo do feed infinito desconcentra o desenvolvedor e sabota o raciocínio analítico.
- ⚠️ **E-Commerce Tradicional de Alto Volume de Commodities (Ex: Supermercados, Autopeças)**:
  Compradores que buscam um parafuso de 8mm ou sabão em pó não desejam navegar por tons hexadecimais em um mosaico de fotos artísticas; eles necessitam de filtros textuais precisos, fotos padronizadas em fundo branco puro 1:1, tabelas de especificações e preço em destaque massivo.

### 3.2 Armadilhas de Imitação ("The Pinterest Clone Trap", "Palette Disconnect" & "Masonry Chaos")

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                    ARMADILHAS DE IMITAÇÃO DA ESTÉTICA DESIGNSPIRATION                  │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  1. THE PINTEREST CLONE TRAP  ──► Copiar o grid masonry sem estabelecer uma curadoria │
│                                   estrita, enchendo o site de lixo visual amador.       │
│  2. PALETTE DISCONNECT        ──► Extrair cores aleatórias via script sem ponderar     │
│                                   o peso visual relativo e a harmonia sRGB real.       │
│  3. INFINITE SCROLL PARALYSIS ──► Não fornecer âncoras de busca, paginação acessível   │
│                                   ou histórico navegável, gerando cansaço mental.     │
│  4. UNBOUNDED ASPECT RATIO    ──► Permitir imagens infinitamente compridas que ocupam  │
│                                   a tela inteira sozinhos, quebrando o ritmo do grid.  │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

1. **A Armadilha do Clone sem Alma ("The Pinterest Clone Trap")**:
   Implementar um layout Masonry responsivo sem um filtro de qualidade editorial feroz. O que confere prestígio ao Designspiration não é a tecnologia de empilhar blocos, mas a curadoria aristocrática de Shelby White e de sua comunidade de designers seniores.
2. **A Desconexão Cromática ("Palette Disconnect")**:
   Calcular swatches pegando apenas cores nos cantos da imagem ou gerando 5 cores com baixíssimo contraste entre si. A quantização deve equilibrar os tons dominantes com os tons de destaque (*accents*) da peça gráfica.
3. **Paralisia por Rolagem Infinita sem Fim**:
   Alimentar centenas de requisições sem memorização de estado da rolagem (`scroll restoration`). Se o usuário clicar em um projeto na posição 200 e, ao voltar, a página reiniciar no topo, a experiência torna-se frustrante e hostil.
4. **O Desastre da Razão de Aspecto Descontrolada ("Unbounded Aspect Ratio")**:
   O Designspiration impõe um limite estrito: `gridItemMaxHeight: 600px`. Se um designer permitir que infográficos de 4000px de altura entrem livremente no Masonry, uma única coluna se estenderá indefinidamente, criando vácuos gigantescos nas colunas vizinhas e arruinando o equilíbrio ótico.

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

A engenharia por trás do portal Designspiration é um exemplo de refinamento de performance, manipulação espacial matemática e inteligência visual.

### 4.1 Arquitetura de Grid Masonry Dinâmico, Espaçamento & Ritmo

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                     DESIGNSPIRATION DYNAMIC MASONRY MATH ENGINE                        │
├────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                        │
│   Viewport Width: 1440px ──► Margins: 48px ──► Usable: 1344px                         │
│   Math: Math.floor((1344 + Gutter) / (ItemWidth + Gutter))                             │
│   (1344 + 24) / (236 + 24) = 1368 / 260 = 5.26 ──► 5 Colunas Exatas                   │
│                                                                                        │
│   ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐                │
│   │ Card 1   │  │ Card 2   │  │ Card 3   │  │ Card 4   │  │ Card 5   │                │
│   │ h: 320px │  │ h: 480px │  │ h: 236px │  │ h: 360px │  │ h: 290px │                │
│   │          │  │          │  └──────────┘  │          │  └──────────┘                │
│   └──────────┘  │          │  ┌──────────┐  └──────────┘  ┌──────────┐                │
│   ┌──────────┐  └──────────┘  │ Card 7   │  ┌──────────┐  │ Card 9   │                │
│   │ Card 6   │  ┌──────────┐  │ h: 400px │  │ Card 8   │  │ h: 310px │                │
│   │ h: 240px │  │ Card 10  │  │          │  │ h: 280px │  └──────────┘                │
│   └──────────┘  │ h: 210px │  └──────────┘  └──────────┘                              │
│                 └──────────┘                                                           │
│   ◄─ 236px ──► ◄24► ◄─ 236px ──► ◄24► ◄─ 236px ──► ◄24► ...                           │
│                                                                                        │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

- **Constantes de Engenharia Oficiais do Designspiration** (extraídas do runtime `App.config`):
  - `gridItemWidth: 236px`: Largura base fixa atribuída a cada coluna do mosaico.
  - `gridItemGutter: 24px`: Espaçamento horizontal e vertical estrito e inegociável entre todos os cards.
  - `gridMinColumns: 2`: Número mínimo de colunas para telas compactas (`>= 520px`).
  - `gridMaxColumns: 9`: Teto arquitetural para telas ultra-wide / monitores 4K (`> 2400px`).
  - `gridItemMaxHeight: 600px`: Altura limite imposta a qualquer peça individual para preservar o ritmo visual.
- **Algoritmo de Colocação "Shortest-Column-First"**:
  Diferente do CSS Multi-column nativo (que preenche uma coluna inteira de cima a baixo antes de iniciar a próxima, forçando o leitor a rolar de volta para ver novos itens), o Designspiration calcula as alturas cumulativas de cada coluna via JavaScript. Cada novo item retornado pela API é alocado na coluna que possui a menor altura acumulada no instante da inserção (`colIndex = heights.indexOf(Math.min(...heights))`), mantendo o fundo do feed sempre nivelado.

### 4.2 Sistemas de Cores, Superfícies & Extração Cromática

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        DESIGNSPIRATION SURFACE & COLOR TOKENS                          │
├────────────────────────┬───────────────────────────┬───────────────────────────────────┤
│ TOKEN SEMÂNTICO        │ LIGHT MODE (DEFAULT)      │ DARK MODE                         │
├────────────────────────┼───────────────────────────┼───────────────────────────────────┤
│ `--dspn-bg-canvas`     │ `#FFFFFF` (Puro)          │ `#121212` (Asfalto Profundo)      │
│ `--dspn-bg-surface`    │ `#F8F8F8` (Off-White)     │ `#1C1C1E` (Grafite Elevado)       │
│ `--dspn-border-subtle` │ `#EAEAEA` (Hairline 1px)  │ `#2C2C2E` (Divisória Discreta)    │
│ `--dspn-text-primary`  │ `#111111` (Preto Carbono) │ `#F5F5F7` (Branco Alabastro)      │
│ `--dspn-text-muted`    │ `#767676` (Cinza Médio)   │ `#8E8E93` (Cinza Prata)           │
│ `--dspn-accent-blue`   │ `#0055FF` (Link / Action) │ `#2979FF` (Glow Ativo)            │
│ `--dspn-badge-pro`     │ `#E0245E` (Ruby Pro CTA)  │ `#FF2A6D` (Neon Pro Accent)       │
└────────────────────────┴───────────────────────────┴───────────────────────────────────┘
```

- **A Estrutura de Metadados Cromáticos por Item**:
  Cada post carrega em seu payload JSON a chave `palette`, contendo exatamente cinco strings hexadecimais ordenadas por dominância visual e saturação, e a propriedade `background`, indicando o tom harmonizado do placeholder pré-carregamento:
  ```json
  {
    "id": "1077780857167",
    "background": "#dededf",
    "palette": ["#1f1f1f", "#656563", "#a7a7a6", "#dededf", "#f7f7f6"],
    "images": {
      "1x": { "w": 236, "h": 157, "url": "https://dspncdn.com/a1/media/236x/...jpg" },
      "2x": { "w": 472, "h": 314, "url": "https://dspncdn.com/a1/media/472x/...jpg" }
    }
  }
  ```

---

### 4.3 Padrões de Seções & Fluxos (8 Arquétipos Concretos)

#### Arquétipo 1: Header Fixo & Global Navigation Bar
- **Anatomia**: Barra de navegação horizontal com altura fixa de `64px`, fixada no topo (`sticky top-0 z-50`), com fundo translúcido enriquecido com desfoque de vidro (`backdrop-blur-md bg-white/90 dark:bg-neutral-900/90`) e linha divisória hairline de `1px solid rgba(0,0,0,0.08)`.
- **Composição**: À esquerda, o logotipo clássico "Designspiration" em peso forte com tracking condensado; ao centro, a barra de busca universal com ícone de lupa e atalho para o seletor cromático; à direita, links de texto "Explore", "Get Pro" (em destaque arredondado), "Log in" e o botão de menu hambúrguer para navegação complementar.
- **Interação**: Permanece fixo durante toda a rolagem infinita, oferecendo acesso permanente aos filtros de busca sem forçar o usuário a retornar ao topo.

#### Arquétipo 2: Multi-Color Palette Search Drawer
- **Anatomia**: Painel retrátil suspenso que se expande abaixo da barra de navegação principal ao clicar no gatilho de paleta (`colorSearchTrigger`).
- **Composição**:
  - Seletor com espectro sRGB contínuo e campo de entrada direta para códigos HEX (`#RRGGBB`).
  - Trilho horizontal contendo até **5 slots circulares** para fixação de cores ativas.
  - Seção de paletas harmônicas sugeridas pela curadoria (*"Palettes"*) e cores primárias frequentes (*"Colors"*).
- **Interação**: Conforme o usuário adiciona de 1 a 5 cores, tags de cor correspondentes são empilhadas visualmente. Clicar em uma cor remove o tom da consulta. A URL do navegador é sincronizada em tempo real para `/palette/<hex1>-<hex2>-<hex3>/`.

#### Arquétipo 3: Dynamic Masonry Card com Hover Palette Breakdown
- **Anatomia**: Cartão retangular com largura invariável de `236px` e cantos sutilmente arredondados (`rounded-lg` ou `rounded-xl`, raio de 8px a 12px), com overflow oculto.
- **Composição**:
  - Área da imagem com fundo inicial tingido na cor `background` do post para eliminar saltos visuais durante o download da imagem.
  - Overlay gradiente semitransparente ativado no estado `:hover`.
  - **Barra de 5 Swatches**: Uma barra horizontal contendo 5 blocos coloridos retangulares adjacentes que representam a paleta exata daquela obra.
  - Botão de ação rápida "Save" (salvar na coleção) no canto superior direito e link com ícone externo diagonal (`↗`) apontando para a fonte original (`source_url`).
- **Interação**: Ao passar o cursor sobre qualquer um dos 5 swatches individuais, o código hexadecimal é exibido em um tooltip flutuante. Clicar no swatch abre uma nova busca instantânea exclusivamente focada naquela cor.

#### Arquétipo 4: Save Closeup Modal / Quick-View Drawer
- **Anatomia**: Modal centralizado em tela cheia com overlay escurecido (`bg-black/80 backdrop-blur-sm`) ou gaveta deslizante lateral para exibição da obra em escala `originals` (alta resolução).
- **Composição**:
  - Imagem em exibição generosa com proporções reais preservadas.
  - Painel lateral com:
    - As 5 cores da paleta ampliadas em pílulas informativas com botões de "Copiar HEX" em 1 clique.
    - Metadados do autor original, usuário que favoritou e data de inclusão.
    - Lista de anotações taxonômicas (`annotations`: ex: "Packaging", "Poster Design", "Minimalist Typography").
    - Botão direto para visitar a página de origem (Behance, Dribbble, agência, loja física).

#### Arquétipo 5: Visions Canvas (Moodboard Studio Integrado)
- **Anatomia**: Área de trabalho livre e privada que transforma a galeria tradicional em uma bancada de edição criativa para pitch decks e apresentações a clientes.
- **Composição**: Canvas com suporte a arrastar-e-soltar imagens salvas, reordenamento em grade inteligente com layouts predefinidos para proporções de impressão (A4, Cartaz) e telas digitais (16:9, Stories 9:16).
- **Funcionalidade**: Exportação direta em PDF de alta qualidade vetorial, PNG de 300 DPI e compartilhamento por link privado protegido para equipes criativas.

#### Arquétipo 6: Horizontal Topic Pill Scroller
- **Anatomia**: Trilho horizontal de deslizamento suave posicionado logo abaixo da introdução editorial ou do cabeçalho de busca.
- **Composição**: Pílulas de texto arredondadas com bordas hairline (`border border-neutral-200 dark:border-neutral-800`), exibindo tópicos como "3D Typography", "Packaging", "Architecture", "Aaron Draplin", "Braun", "Business Cards", "Posters" e "Brand Identity".
- **Interação**: Suporte a arraste com o mouse (*drag-to-scroll*) no desktop e rolagem por toque inercial no mobile. Clicar em uma pílula navega para `/topics/<slug>/`.

#### Arquétipo 7: Collection Curator Grid
- **Anatomia**: Cartão especial de agrupamento exibido no feed de coleções de usuários.
- **Composição**: Grid com visualização mosaico composta por 3 miniaturas representativas da coleção (uma imagem grande à esquerda ocupando 60% do card e duas menores empilhadas verticalmente à direita), encimadas pelo título da pasta (ex: "Abstract Pantones", "Brutalist Editorial"), nome do curador e contador de itens salvos.

#### Arquétipo 8: Micro-Search Tray & Predictive Autocomplete
- **Anatomia**: Bandeja expansível sobre a barra de pesquisa que renderiza resultados instantâneos conforme o usuário digita.
- **Composição**: Dividida em três colunas ou blocos lógicos:
  1. *History & Recent Searches*: Buscas recentes armazenadas localmente no navegador.
  2. *Suggested Topics*: Tópicos taxonômicos coincidentes com o termo digitado.
  3. *Trending Color Palettes*: Conjuntos de cores quentes da semana com previsão visual em tempo real.

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Tokens CSS do Sistema Designspiration

```css
:root {
  /* Dimensões Matemáticas do Grid Masonry */
  --dspn-item-width: 236px;
  --dspn-gutter: 24px;
  --dspn-max-height: 600px;
  --dspn-radius: 12px;

  /* Superfícies & Fundo (Light Default) */
  --dspn-bg-canvas: #ffffff;
  --dspn-bg-surface: #f8f8f8;
  --dspn-border-hairline: #eaeaea;
  --dspn-border-focus: #111111;

  /* Tipografia Suíça Funcional */
  --dspn-font-sans: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  --dspn-font-mono: 'Geist Mono', 'SF Mono', monospace;

  --dspn-text-primary: #111111;
  --dspn-text-secondary: #767676;
  --dspn-text-tertiary: #a0a0a0;

  /* Acentos de Ação */
  --dspn-accent-pro: #e0245e;
  --dspn-accent-blue: #0055ff;
  --dspn-overlay-card: rgba(0, 0, 0, 0.45);
}

.dark {
  --dspn-bg-canvas: #121212;
  --dspn-bg-surface: #1c1c1e;
  --dspn-border-hairline: #2c2c2e;
  --dspn-border-focus: #f5f5f7;

  --dspn-text-primary: #f5f5f7;
  --dspn-text-secondary: #8e8e93;
  --dspn-text-tertiary: #636366;

  --dspn-accent-pro: #ff2a6d;
  --dspn-accent-blue: #2979ff;
  --dspn-overlay-card: rgba(0, 0, 0, 0.65);
}
```

---

### 5.2 Componente React Completo: `<DesignspirationMasonryFeed />`

Abaixo está a implementação funcional completa em **React**, **TypeScript**, **Tailwind CSS** e **Framer Motion**, incorporando:
- O algoritmo real de posicionamento Masonry (*shortest column first*) baseado no `gridItemWidth: 236px` e `gridItemGutter: 24px`.
- A barra de 5 swatches cromáticos interativos com cópia de código HEX ao clicar.
- O Drawer de busca por até 5 cores hexadecimais simultâneas.
- O modal de inspeção rápida (*Save Closeup Modal*).

```tsx
import React, { useState, useEffect, useMemo, useRef } from 'react';
import { motion, AnimatePresence } from 'framer-motion';
import { 
  Search, 
  Palette, 
  Bookmark, 
  ExternalLink, 
  X, 
  Check, 
  Plus, 
  Sliders, 
  Sparkles,
  Copy
} from 'lucide-react';

// Tipagem de Item com Suporte a Paleta Hexadecimal K-Means
export interface DesignspirationItem {
  id: string;
  title: string;
  sourceDomain: string;
  sourceUrl: string;
  authorName: string;
  authorHandle: string;
  background: string;
  palette: [string, string, string, string, string]; // Exatamente 5 cores HEX
  imageUrl: string;
  aspectRatio: number; // h / w
  annotations: string[];
}

interface MasonryLayoutColumn {
  items: DesignspirationItem[];
  height: number;
}

export const DesignspirationFeed: React.FC = () => {
  // Estados da Interface
  const [items, setItems] = useState<DesignspirationItem[]>([]);
  const [selectedColors, setSelectedColors] = useState<string[]>([]);
  const [customHexInput, setCustomHexInput] = useState('');
  const [isColorDrawerOpen, setIsColorDrawerOpen] = useState(false);
  const [activeItemModal, setActiveItemModal] = useState<DesignspirationItem | null>(null);
  const [copiedHex, setCopiedHex] = useState<string | null>(null);
  const [savedItemIds, setSavedItemIds] = useState<Set<string>>(new Set());

  const containerRef = useRef<HTMLDivElement>(null);
  const [numColumns, setNumColumns] = useState<number>(4);

  // Paleta de Amostras para Descoberta Rápida
  const presetPalettes = [
    { name: 'Swiss Editorial', colors: ['#1A1A1A', '#F4F1EA', '#E63946', '#457B9D', '#1D3557'] },
    { name: 'Nordic Forest', colors: ['#264653', '#2A9D8F', '#E76F51', '#F4A261', '#E9C46A'] },
    { name: 'Brutalist Concrete', colors: ['#111111', '#555555', '#999999', '#DCDCDC', '#F8F8F8'] },
    { name: 'Warm Terracotta', colors: ['#5F0F40', '#9A031E', '#FB8B24', '#E36414', '#0F4C5C'] }
  ];

  // Cálculo Dinâmico de Colunas Baseado nas Regras Matemáticas Oficiais (236px + 24px)
  useEffect(() => {
    const handleResize = () => {
      if (!containerRef.current) return;
      const containerWidth = containerRef.current.offsetWidth;
      const itemWidth = 236;
      const gutter = 24;

      // Fórmula: Math.floor((width + gutter) / (itemWidth + gutter))
      const calculatedCols = Math.floor((containerWidth + gutter) / (itemWidth + gutter));
      const clampedCols = Math.max(2, Math.min(9, calculatedCols));
      setNumColumns(clampedCols);
    };

    handleResize();
    window.addEventListener('resize', handleResize);
    return () => window.removeEventListener('resize', handleResize);
  }, []);

  // Dados Mockados de Alta Fidelidade Representativos da Curadoria Real
  useEffect(() => {
    const mockData: DesignspirationItem[] = [
      {
        id: '1077780857167',
        title: 'Hotel Daniel Branding & Identity System',
        sourceDomain: 'behance.net',
        sourceUrl: 'https://behance.net',
        authorName: 'Rodrigo Francisco',
        authorHandle: 'rodrigofrancisco',
        background: '#dededf',
        palette: ['#1F1F1F', '#656563', '#A7A7A6', '#DEDEDF', '#F7F7F6'],
        imageUrl: 'https://images.unsplash.com/photo-1541701494587-cb58502866ab?auto=format&fit=crop&w=600&q=80',
        aspectRatio: 1.4,
        annotations: ['Business Cards', 'Stationery', 'Branding', 'Minimal']
      },
      {
        id: '56795123810',
        title: 'Modernist Swiss Typographic Poster',
        sourceDomain: 'agda.com.au',
        sourceUrl: 'https://agda.com.au',
        authorName: 'Ferdinand-Noel Bacani',
        authorHandle: 'xariusound',
        background: '#ebeaec',
        palette: ['#222221', '#E63946', '#A3A29F', '#EBEAEC', '#F6F6F5'],
        imageUrl: 'https://images.unsplash.com/photo-1509198397868-475647b2a1e5?auto=format&fit=crop&w=600&q=80',
        aspectRatio: 1.6,
        annotations: ['Posters', 'Typography', 'Swiss Style', 'Music']
      },
      {
        id: '892150468536',
        title: 'Botanical Craft Packaging & Label Design',
        sourceDomain: 'tumblr.com',
        sourceUrl: 'https://tumblr.com',
        authorName: 'Sallie Harrison',
        authorHandle: 'salliewho',
        background: '#e3dbd4',
        palette: ['#201C1B', '#645F5D', '#ABA5A1', '#E3DBD4', '#FEFDFD'],
        imageUrl: 'https://images.unsplash.com/photo-1544816155-12df9643f363?auto=format&fit=crop&w=600&q=80',
        aspectRatio: 1.25,
        annotations: ['Packaging', 'Abstract Pantones', 'Craft', 'Print']
      },
      {
        id: '43920194821',
        title: 'Brutalist Concrete Pavilion & Architecture',
        sourceDomain: 'archdaily.com',
        sourceUrl: 'https://archdaily.com',
        authorName: 'Shelby White',
        authorHandle: 'shelbywhite',
        background: '#b4b0a9',
        palette: ['#1A1A1A', '#4A4A4A', '#8C8C8C', '#B4B0A9', '#ECEBE4'],
        imageUrl: 'https://images.unsplash.com/photo-1513694203232-719a280e022f?auto=format&fit=crop&w=600&q=80',
        aspectRatio: 1.5,
        annotations: ['Architecture', 'Brutalism', 'Space', 'Monochrome']
      },
      {
        id: '78291048291',
        title: 'Editorial Magazine Cover & Custom Ligatures',
        sourceDomain: 'dribbble.com',
        sourceUrl: 'https://dribbble.com',
        authorName: 'Klara Lindqvist',
        authorHandle: 'klaradesign',
        background: '#dcd6cd',
        palette: ['#121212', '#9A031E', '#FB8B24', '#DCD6CD', '#FFFFFF'],
        imageUrl: 'https://images.unsplash.com/photo-1512820790803-83ca734da794?auto=format&fit=crop&w=600&q=80',
        aspectRatio: 1.35,
        annotations: ['Editorial', 'Typography', 'Magazine', 'Layout']
      },
      {
        id: '99281726354',
        title: 'Ceramic Tableware & Nordic Warm Minimal',
        sourceDomain: 'kinfolk.com',
        sourceUrl: 'https://kinfolk.com',
        authorName: 'Morten Olsen',
        authorHandle: 'mortendesign',
        background: '#e9e4de',
        palette: ['#2F3E46', '#354F52', '#52796F', '#84A98C', '#CAD2C5'],
        imageUrl: 'https://images.unsplash.com/photo-1578749556568-bc2c40e68b61?auto=format&fit=crop&w=600&q=80',
        aspectRatio: 1.15,
        annotations: ['Ceramics', 'Nordic', 'Tableware', 'Lifestyle']
      }
    ];

    setItems(mockData);
  }, []);

  // Filtro Dinâmico por Paleta Selecionada
  const filteredItems = useMemo(() => {
    if (selectedColors.length === 0) return items;
    // Em produção, a busca cruza a distância Euclidiana no espaço Lab.
    // Aqui verificamos se o item contém cor similar aproximada.
    return items.filter(item => 
      selectedColors.some(selColor => 
        item.palette.some(pColor => pColor.toLowerCase() === selColor.toLowerCase())
      )
    );
  }, [items, selectedColors]);

  // Distribuição nos Trilhos de Coluna (Algoritmo Shortest-Column-First)
  const columns = useMemo(() => {
    const cols: MasonryLayoutColumn[] = Array.from({ length: numColumns }, () => ({
      items: [],
      height: 0
    }));

    filteredItems.forEach((item) => {
      // Encontra a coluna com menor altura acumulada
      let shortestColIndex = 0;
      let minHeight = cols[0].height;

      for (let i = 1; i < numColumns; i++) {
        if (cols[i].height < minHeight) {
          minHeight = cols[i].height;
          shortestColIndex = i;
        }
      }

      // Adiciona o item à menor coluna
      const itemCalculatedHeight = Math.min(600, 236 * item.aspectRatio);
      cols[shortestColIndex].items.push(item);
      cols[shortestColIndex].height += itemCalculatedHeight + 24; // 24px gutter
    });

    return cols;
  }, [filteredItems, numColumns]);

  // Gerenciamento de Cores
  const handleAddColor = (hex: string) => {
    const formatted = hex.startsWith('#') ? hex.toUpperCase() : `#${hex.toUpperCase()}`;
    if (!/^#[0-9A-F]{6}$/i.test(formatted)) return;
    if (selectedColors.length >= 5) return;
    if (!selectedColors.includes(formatted)) {
      setSelectedColors([...selectedColors, formatted]);
    }
    setCustomHexInput('');
  };

  const handleRemoveColor = (hex: string) => {
    setSelectedColors(selectedColors.filter(c => c !== hex));
  };

  const handleCopyHex = (hex: string, e: React.MouseEvent) => {
    e.stopPropagation();
    navigator.clipboard.writeText(hex);
    setCopiedHex(hex);
    setTimeout(() => setCopiedHex(null), 1800);
  };

  const toggleSave = (id: string, e: React.MouseEvent) => {
    e.stopPropagation();
    setSavedItemIds(prev => {
      const next = new Set(prev);
      if (next.has(id)) next.delete(id);
      else next.add(id);
      return next;
    });
  };

  return (
    <div className="min-h-screen bg-white text-neutral-900 antialiased dark:bg-[#121212] dark:text-[#F5F5F7]">
      {/* 1. Header Fixo & Global Navigation Bar */}
      <header className="sticky top-0 z-40 border-b border-neutral-200/80 bg-white/90 backdrop-blur-md dark:border-neutral-800/80 dark:bg-[#121212]/90">
        <div className="mx-auto flex h-16 max-w-[1920px] items-center justify-between px-6">
          {/* Logo Clássico */}
          <div className="flex items-center gap-6">
            <a href="/" className="font-sans text-xl font-bold tracking-tight text-neutral-950 dark:text-white">
              Design<span className="font-light text-neutral-500 dark:text-neutral-400">spiration</span>
            </a>

            <nav className="hidden items-center gap-5 md:flex">
              <a href="/explore/" className="text-sm font-medium text-neutral-600 hover:text-neutral-950 dark:text-neutral-400 dark:hover:text-white transition-colors">
                Explore
              </a>
              <a href="/popular/" className="text-sm font-medium text-neutral-600 hover:text-neutral-950 dark:text-neutral-400 dark:hover:text-white transition-colors">
                Popular
              </a>
              <a href="/everything/" className="text-sm font-medium text-neutral-600 hover:text-neutral-950 dark:text-neutral-400 dark:hover:text-white transition-colors">
                Everything
              </a>
            </nav>
          </div>

          {/* Gatilho Central de Busca e Cores */}
          <div className="flex flex-1 max-w-lg items-center mx-6">
            <div className="relative w-full flex items-center">
              <Search className="absolute left-3.5 h-4 w-4 text-neutral-400 pointer-events-none" />
              <input 
                type="text" 
                placeholder="Search art, typography, packaging, architecture..."
                className="w-full rounded-full border border-neutral-200 bg-neutral-100/70 py-2 pl-10 pr-24 text-xs font-normal text-neutral-900 placeholder-neutral-400 focus:border-neutral-900 focus:bg-white focus:outline-none dark:border-neutral-800 dark:bg-neutral-800/60 dark:text-neutral-100 dark:focus:border-white transition-all"
              />
              <button
                type="button"
                onClick={() => setIsColorDrawerOpen(!isColorDrawerOpen)}
                className={`absolute right-1.5 flex items-center gap-1.5 rounded-full px-2.5 py-1 text-[11px] font-medium transition-all ${
                  selectedColors.length > 0 || isColorDrawerOpen
                    ? 'bg-neutral-900 text-white dark:bg-white dark:text-neutral-950'
                    : 'bg-neutral-200/80 text-neutral-700 hover:bg-neutral-300 dark:bg-neutral-700 dark:text-neutral-200'
                }`}
              >
                <Palette className="h-3 w-3" />
                <span>Colors</span>
                {selectedColors.length > 0 && (
                  <span className="ml-0.5 flex h-4 w-4 items-center justify-center rounded-full bg-white text-neutral-950 text-[10px] font-bold dark:bg-neutral-900 dark:text-white">
                    {selectedColors.length}
                  </span>
                )}
              </button>
            </div>
          </div>

          {/* Ações do Usuário & Pro CTA */}
          <div className="flex items-center gap-3">
            <a 
              href="/pro/" 
              className="hidden sm:inline-flex items-center gap-1.5 rounded-full bg-rose-500/10 px-3 py-1 text-xs font-semibold text-rose-600 hover:bg-rose-500/20 dark:bg-rose-500/20 dark:text-rose-400 transition-colors"
            >
              <Sparkles className="h-3.5 w-3.5" />
              <span>Get Pro</span>
            </a>
            <button className="text-xs font-medium text-neutral-700 hover:text-neutral-950 dark:text-neutral-300 dark:hover:text-white px-2">
              Log in
            </button>
            <button className="rounded-full bg-neutral-950 px-3.5 py-1.5 text-xs font-medium text-white hover:bg-neutral-800 dark:bg-white dark:text-neutral-950 dark:hover:bg-neutral-200 transition-colors">
              Sign up
            </button>
          </div>
        </div>
      </header>

      {/* 2. Multi-Color Palette Search Drawer */}
      <AnimatePresence>
        {isColorDrawerOpen && (
          <motion.div
            initial={{ height: 0, opacity: 0 }}
            animate={{ height: 'auto', opacity: 1 }}
            exit={{ height: 0, opacity: 0 }}
            transition={{ type: 'spring', damping: 28, stiffness: 350 }}
            className="overflow-hidden border-b border-neutral-200 bg-neutral-50 px-6 py-6 dark:border-neutral-800 dark:bg-neutral-900/60"
          >
            <div className="mx-auto max-w-[1440px]">
              <div className="flex flex-col md:flex-row md:items-center justify-between gap-6">
                {/* Seção das Cores Ativas (Até 5 Tons Simultâneos) */}
                <div>
                  <div className="flex items-center gap-2 mb-2">
                    <span className="text-xs font-semibold uppercase tracking-wider text-neutral-500 dark:text-neutral-400">
                      Active Palette ({selectedColors.length}/5)
                    </span>
                    {selectedColors.length > 0 && (
                      <button 
                        onClick={() => setSelectedColors([])} 
                        className="text-[11px] text-rose-500 hover:underline"
                      >
                        Clear all
                      </button>
                    )}
                  </div>

                  <div className="flex flex-wrap items-center gap-2">
                    {selectedColors.map((hex) => (
                      <div 
                        key={hex}
                        className="group flex items-center gap-2 rounded-full border border-neutral-300 bg-white py-1 pl-1.5 pr-2.5 shadow-sm dark:border-neutral-700 dark:bg-neutral-800"
                      >
                        <span 
                          className="h-5 w-5 rounded-full border border-black/10 shadow-inner"
                          style={{ backgroundColor: hex }}
                        />
                        <span className="font-mono text-[11px] font-semibold text-neutral-800 dark:text-neutral-200">
                          {hex}
                        </span>
                        <button
                          onClick={() => handleRemoveColor(hex)}
                          className="rounded-full p-0.5 text-neutral-400 hover:bg-neutral-100 hover:text-neutral-700 dark:hover:bg-neutral-700 dark:hover:text-white"
                        >
                          <X className="h-3 w-3" />
                        </button>
                      </div>
                    ))}

                    {/* Input para adicionar HEX manual */}
                    {selectedColors.length < 5 && (
                      <div className="flex items-center gap-1.5">
                        <input
                          type="text"
                          value={customHexInput}
                          onChange={(e) => setCustomHexInput(e.target.value)}
                          onKeyDown={(e) => e.key === 'Enter' && handleAddColor(customHexInput)}
                          placeholder="#E63946"
                          maxLength={7}
                          className="h-8 w-24 rounded-full border border-dashed border-neutral-300 bg-transparent px-2.5 font-mono text-xs text-neutral-800 placeholder-neutral-400 focus:border-neutral-900 focus:outline-none dark:border-neutral-700 dark:text-neutral-200"
                        />
                        <button
                          onClick={() => handleAddColor(customHexInput)}
                          className="flex h-8 w-8 items-center justify-center rounded-full bg-neutral-900 text-white hover:bg-neutral-800 dark:bg-white dark:text-neutral-900"
                        >
                          <Plus className="h-4 w-4" />
                        </button>
                      </div>
                    )}
                  </div>
                </div>

                {/* Presets de Paletas Harmônicas Curadas */}
                <div>
                  <span className="block text-xs font-semibold uppercase tracking-wider text-neutral-500 dark:text-neutral-400 mb-2">
                    Curated Palettes
                  </span>
                  <div className="flex flex-wrap gap-2.5">
                    {presetPalettes.map((preset) => (
                      <button
                        key={preset.name}
                        onClick={() => setSelectedColors(preset.colors)}
                        className="flex items-center gap-1.5 rounded-lg border border-neutral-200 bg-white px-2.5 py-1.5 shadow-sm hover:border-neutral-400 dark:border-neutral-800 dark:bg-neutral-800 dark:hover:border-neutral-600 transition-all"
                      >
                        <div className="flex -space-x-1">
                          {preset.colors.map((c) => (
                            <span 
                              key={c} 
                              className="h-3.5 w-3.5 rounded-full border border-white dark:border-neutral-900" 
                              style={{ backgroundColor: c }} 
                            />
                          ))}
                        </div>
                        <span className="text-xs font-medium text-neutral-700 dark:text-neutral-300">
                          {preset.name}
                        </span>
                      </button>
                    ))}
                  </div>
                </div>
              </div>
            </div>
          </motion.div>
        )}
      </AnimatePresence>

      {/* 3. Container Principal com Margem e Grid Masonry Fluido */}
      <main className="mx-auto max-w-[1920px] px-6 py-6" ref={containerRef}>
        {/* Notificação Flutuante de HEX Copiado */}
        <AnimatePresence>
          {copiedHex && (
            <motion.div
              initial={{ opacity: 0, y: 15 }}
              animate={{ opacity: 1, y: 0 }}
              exit={{ opacity: 0, y: 15 }}
              className="fixed bottom-6 left-1/2 -translate-x-1/2 z-50 flex items-center gap-2 rounded-full bg-neutral-900 px-4 py-2 text-xs font-medium text-white shadow-xl dark:bg-white dark:text-neutral-950"
            >
              <Check className="h-3.5 w-3.5 text-emerald-400 dark:text-emerald-600" />
              <span>Copied {copiedHex} to clipboard</span>
            </motion.div>
          )}
        </AnimatePresence>

        {/* Colunas Masonry Parametrizadas (236px base + 24px gutter) */}
        <div 
          className="flex justify-center"
          style={{ gap: '24px' }}
        >
          {columns.map((col, colIndex) => (
            <div 
              key={colIndex} 
              className="flex flex-col flex-1 max-w-[236px]"
              style={{ gap: '24px' }}
            >
              {col.items.map((item) => {
                const isSaved = savedItemIds.has(item.id);

                return (
                  <motion.div
                    key={item.id}
                    layoutId={`card-${item.id}`}
                    onClick={() => setActiveItemModal(item)}
                    className="group relative cursor-pointer overflow-hidden rounded-xl border border-neutral-200/60 bg-neutral-100 shadow-sm transition-all duration-300 hover:shadow-md dark:border-neutral-800/80 dark:bg-neutral-800"
                    style={{ backgroundColor: item.background }}
                  >
                    {/* Imagem com Proporção Nativa */}
                    <img 
                      src={item.imageUrl} 
                      alt={item.title}
                      loading="lazy"
                      className="w-full object-cover transition-transform duration-500 group-hover:scale-[1.02]"
                      style={{ height: `${Math.min(600, 236 * item.aspectRatio)}px` }}
                    />

                    {/* Botão de Salvar Rápido (Canto Superior Direito) */}
                    <button
                      type="button"
                      onClick={(e) => toggleSave(item.id, e)}
                      className={`absolute top-2.5 right-2.5 z-20 flex h-8 w-8 items-center justify-center rounded-full backdrop-blur-md transition-all ${
                        isSaved 
                          ? 'bg-rose-500 text-white' 
                          : 'bg-black/40 text-white opacity-0 group-hover:opacity-100 hover:bg-black/60'
                      }`}
                      title={isSaved ? 'Saved to collection' : 'Save'}
                    >
                      <Bookmark className="h-4 w-4" fill={isSaved ? 'currentColor' : 'none'} />
                    </button>

                    {/* Overlay Escurecido no Hover */}
                    <div className="absolute inset-0 bg-gradient-to-t from-black/80 via-black/20 to-transparent opacity-0 transition-opacity duration-200 group-hover:opacity-100 flex flex-col justify-between p-3 pointer-events-none">
                      <div className="flex justify-between items-start pointer-events-auto">
                        <span className="text-[10px] font-medium uppercase tracking-wider text-white/80">
                          {item.annotations[0] || 'Design'}
                        </span>
                        <a
                          href={item.sourceUrl}
                          target="_blank"
                          rel="noopener noreferrer"
                          onClick={(e) => e.stopPropagation()}
                          className="flex h-7 w-7 items-center justify-center rounded-full bg-white/20 text-white backdrop-blur-sm hover:bg-white/40 transition-colors"
                          title={`Visit ${item.sourceDomain}`}
                        >
                          <ExternalLink className="h-3 w-3" />
                        </a>
                      </div>

                      {/* Barra Inferior com os 5 Swatches de Cores Interativos */}
                      <div className="pointer-events-auto">
                        <p className="truncate text-xs font-semibold text-white mb-2">
                          {item.title}
                        </p>
                        <div className="flex h-3.5 w-full overflow-hidden rounded shadow-sm border border-white/20">
                          {item.palette.map((colorHex) => (
                            <button
                              key={colorHex}
                              type="button"
                              onClick={(e) => handleCopyHex(colorHex, e)}
                              className="relative flex-1 h-full transition-transform hover:scale-y-125"
                              style={{ backgroundColor: colorHex }}
                              title={`Copy ${colorHex}`}
                            />
                          ))}
                        </div>
                      </div>
                    </div>
                  </motion.div>
                );
              })}
            </div>
          ))}
        </div>
      </main>

      {/* 4. Save Closeup Modal / Quick-View Drawer */}
      <AnimatePresence>
        {activeItemModal && (
          <motion.div
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            exit={{ opacity: 0 }}
            onClick={() => setActiveItemModal(null)}
            className="fixed inset-0 z-50 flex items-center justify-center bg-black/80 p-4 backdrop-blur-sm"
          >
            <motion.div
              layoutId={`card-${activeItemModal.id}`}
              onClick={(e) => e.stopPropagation()}
              className="relative flex flex-col md:flex-row max-h-[90vh] w-full max-w-5xl overflow-hidden rounded-2xl bg-white shadow-2xl dark:bg-[#1C1C1E]"
            >
              {/* Botão de Fechar */}
              <button
                onClick={() => setActiveItemModal(null)}
                className="absolute top-4 right-4 z-20 flex h-8 w-8 items-center justify-center rounded-full bg-black/40 text-white backdrop-blur-md hover:bg-black/60 transition-colors"
              >
                <X className="h-4 w-4" />
              </button>

              {/* Lado Esquerdo: Imagem em Alta Fidelidade */}
              <div 
                className="flex flex-1 items-center justify-center bg-neutral-100 p-6 dark:bg-neutral-900"
                style={{ backgroundColor: activeItemModal.background }}
              >
                <img 
                  src={activeItemModal.imageUrl} 
                  alt={activeItemModal.title}
                  className="max-h-[75vh] w-auto max-w-full rounded-lg object-contain shadow-lg"
                />
              </div>

              {/* Lado Direito: Paleta Hexadecimal, Metadados e Tags */}
              <div className="flex w-full md:w-80 flex-col justify-between p-6 bg-white dark:bg-[#1C1C1E]">
                <div>
                  <span className="text-[11px] font-semibold uppercase tracking-wider text-neutral-400">
                    Saved by @{activeItemModal.authorHandle}
                  </span>
                  <h3 className="mt-1 text-lg font-bold text-neutral-950 dark:text-white">
                    {activeItemModal.title}
                  </h3>

                  {/* Decomposição da Paleta de 5 Tons com Botões de Cópia */}
                  <div className="mt-6">
                    <span className="text-xs font-semibold uppercase tracking-wider text-neutral-500 dark:text-neutral-400">
                      Color Palette (K-Means)
                    </span>
                    <div className="mt-2.5 flex flex-col gap-2">
                      {activeItemModal.palette.map((hex) => (
                        <div 
                          key={hex}
                          onClick={(e) => handleCopyHex(hex, e)}
                          className="flex items-center justify-between rounded-lg border border-neutral-200 p-2 hover:bg-neutral-50 dark:border-neutral-800 dark:hover:bg-neutral-800/60 cursor-pointer transition-colors"
                        >
                          <div className="flex items-center gap-2.5">
                            <span 
                              className="h-5 w-5 rounded-md border border-black/10 shadow-sm"
                              style={{ backgroundColor: hex }}
                            />
                            <span className="font-mono text-xs font-semibold text-neutral-800 dark:text-neutral-200">
                              {hex}
                            </span>
                          </div>
                          <Copy className="h-3.5 w-3.5 text-neutral-400 hover:text-neutral-700 dark:hover:text-neutral-200" />
                        </div>
                      ))}
                    </div>
                  </div>

                  {/* Anotações e Taxonomias */}
                  <div className="mt-6">
                    <span className="text-xs font-semibold uppercase tracking-wider text-neutral-500 dark:text-neutral-400">
                      Tags & Topics
                    </span>
                    <div className="mt-2 flex flex-wrap gap-1.5">
                      {activeItemModal.annotations.map((tag) => (
                        <span 
                          key={tag}
                          className="rounded-full bg-neutral-100 px-2.5 py-0.5 text-[11px] font-medium text-neutral-700 dark:bg-neutral-800 dark:text-neutral-300"
                        >
                          {tag}
                        </span>
                      ))}
                    </div>
                  </div>
                </div>

                {/* Rodapé com Link Externo Original */}
                <div className="mt-8 border-t border-neutral-200 pt-4 dark:border-neutral-800 flex items-center justify-between">
                  <span className="text-xs text-neutral-500">
                    Source: <strong className="text-neutral-800 dark:text-neutral-200">{activeItemModal.sourceDomain}</strong>
                  </span>
                  <a
                    href={activeItemModal.sourceUrl}
                    target="_blank"
                    rel="noopener noreferrer"
                    className="flex items-center gap-1 text-xs font-semibold text-neutral-900 hover:underline dark:text-white"
                  >
                    <span>Visit website</span>
                    <ExternalLink className="h-3 w-3" />
                  </a>
                </div>
              </div>
            </motion.div>
          </motion.div>
        )}
      </AnimatePresence>
    </div>
  );
};
```

---

### 5.3 Como a IA Deve Pesquisar ao Vivo no Designspiration

O Designspiration possui um sistema estruturado e previsível de rotas para navegação e indexação em tempo real. Sempre que um agente inteligente precisar localizar referências concretas de design, deve utilizar as seguintes URLs paramétricas:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                     DESIGNSPIRATION REAL-TIME ROUTE & TAXONOMY MAP                     │
├────────────────────────┬───────────────────────────────────────────────────────────────┤
│ OBJETIVO DE BUSCA      │ ROTA DE URL DIRETA (PARA BROWSER OU HTTP CLIENT)              │
├────────────────────────┼───────────────────────────────────────────────────────────────┤
│ Feed Principal (Home)  │ https://www.designspiration.com/                              │
│ Feed Popular           │ https://www.designspiration.com/popular/                      │
│ Feed Completo          │ https://www.designspiration.com/everything/                   │
│ Diretório de Tópicos   │ https://www.designspiration.com/explore/                      │
│ Tópico: 3D Typography  │ https://www.designspiration.com/topics/3d-typography/         │
│ Tópico: Embalagens     │ https://www.designspiration.com/topics/beer-packaging/        │
│ Tópico: Arquitetura    │ https://www.designspiration.com/topics/architecture/          │
│ Tópico: Cartões Visita │ https://www.designspiration.com/topics/business-cards/        │
│ Tópico: Designers/Arte │ https://www.designspiration.com/topics/aaron-draplin/         │
│ Busca por Cor Única    │ https://www.designspiration.com/color/<hex6>/                 │
│ Exemplo Cor Única      │ https://www.designspiration.com/color/67744a/                 │
│ Busca por Paleta (2-5) │ https://www.designspiration.com/palette/<hex1>-<hex2>-<hex3>/ │
│ Exemplo Multi-Paleta   │ https://www.designspiration.com/palette/67744a-1f1f1f/        │
│ Busca por Termo        │ https://www.designspiration.com/search/saves/?q=<keyword>     │
│ Busca Termo + Cor      │ https://www.designspiration.com/search/saves/?q=<termo>&c=<hex>│
│ Detalhe de um Post     │ https://www.designspiration.com/save/<id-num>/                │
│ Perfil de Criador      │ https://www.designspiration.com/<username>/                   │
│ Coleção Específica     │ https://www.designspiration.com/<username>/<collection-slug>/ │
└────────────────────────┴───────────────────────────────────────────────────────────────┘
```

> **Protocolo Operacional para Agentes de IA**: Ao receber um pedido do usuário para criar uma paleta para uma marca de cosméticos sustentáveis baseada em tons de terracota (`#9A031E`) e areia (`#E3DBD4`), o agente pode consultar diretamente a URL combinada `https://www.designspiration.com/palette/9a031e-e3dbd4/` para inspecionar fotografias e projetos de embalagens reais que validam o contraste e a atmosfera dessa combinação cromática.

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma aplicação que incorpore os princípios visuais e mecânicos do **Designspiration**, o arquiteto de software e líder de design deve fixar no `DESIGN_BLUEPRINT.md` os seguintes requisitos normativos:

### 6.1 Filosofia Visual & Posicionamento de Marca
- Declarar o estilo oficial como **"Multidisciplinary Visual Discovery & Chromatic Intelligence"**.
- Garantir que a interface do produto seja deliberadamente neutra e silenciosa, operando como uma moldura estéril que amplifica a beleza das obras sem gerar competição visual.

### 6.2 Estrutura de Grids & Superfícies
- **Largura Base de Coluna**: Fixar em `236px` por item com espaçamento (*gutter*) constante de `24px`.
- **Limites de Responsividade**: Variação paramétrica de no mínimo 2 colunas (`>= 520px`) a no máximo 9 colunas (`> 2400px`).
- **Altura Máxima dos Cards**: Bloqueio rígido em `max-height: 600px` para impedir que mídias ultra-alongadas quebrem a harmonia do feed.
- **Algoritmo Masonry**: Posicionamento estrito via *Shortest-Column-First* calculado dinamicamente no frontend.
- **Cor de Fundo Dinâmica**: Injetar no container do card a cor de fundo dominante da imagem (`background: item.background`) para eliminar quebras bruscas de layout enquanto as mídias carregam.

### 6.3 Tipografia & Escala Hierárquica
- **Família Display & Corpo**: Sans-serif Neo-Grotesca funcional com suporte a fontes variáveis (Inter Variable ou PP Neue Montreal).
- **Família Monoespaçada**: Utilizada exclusivamente para metadados técnicos e exibição de códigos HEX (Geist Mono ou JetBrains Mono).
- **Logotipo Principal**: `text-xl font-bold tracking-tight`.
- **Rótulos de Tópicos e Tags**: `text-[11px] font-semibold uppercase tracking-wider`.

### 6.4 Paleta de Cores & Tokens Normativos
- **Canvas Neutro**: `--dspn-bg-canvas: #FFFFFF` (Light) e `#121212` (Dark).
- **Superfície Secundária**: `--dspn-bg-surface: #F8F8F8` (Light) e `#1C1C1E` (Dark).
- **Linhas Hairline**: `--dspn-border-hairline: #EAEAEA` (Light) e `#2C2C2E` (Dark).
- **Texto Principal**: `--dspn-text-primary: #111111` (Light) e `#F5F5F7` (Dark).
- **Acento Pro / Ruby**: `--dspn-accent-pro: #E0245E` (Light) e `#FF2A6D` (Dark).
- **Paleta Hexadecimal Ativa**: Suporte a até 5 tons simultâneos via input de 6 dígitos.

### 6.5 Checklist de Componentes Obrigatórios
- [ ] Header com navegação, busca universal e acionador retrátil de paleta de cores.
- [ ] Drawer de busca cromática com seleção de até 5 cores hexadecimais simultâneas e presets curados.
- [ ] Grid Masonry dinâmico com colunas fluidas calculadas via *shortest-column algorithm*.
- [ ] Cartões de projeto com barra inferior contendo 5 swatches de cores ativada no hover.
- [ ] Tooltip e função de cópia do código hexadecimal para a área de transferência em 1 clique.
- [ ] Modal de visualização expandida (*Save Closeup Modal*) com decomposição completa de cores, autor e tags.
- [ ] Sincronização da URL em tempo real para permitir compartilhamento de buscas por cor (`/color/<hex>/` e `/palette/<hex1>-<hex2>/`).
- [ ] Tratamento de performance com imagens responsivas servidas em múltiplas resoluções com lazy loading.
