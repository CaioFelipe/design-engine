---
id: "minimal-gallery"
name: "Minimal Gallery"
url: "https://minimal.gallery/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico:
  - "Minimalismo Suíço & International Typographic Style"
  - "Espaço Negativo Ativo como Elemento Estrutural Primário"
  - "Design Silencioso & Anti-Decoração (Quiet Digital Craft)"
  - "Monocromatismo Estrito com Contraste Cirúrgico"
  - "Curadoria Intransigente & Não Paga (100% Merit-Based, Max 1 Post/Dia)"
  - "Inspeção Dual-Device (Desktop 1440x800 vs Mobile 375x667 com DPR Real)"
  - "Bookmark Engine Client-Side com Coleções Customizadas"
densidade_informacao: "Baixa/Contemplativa a Media/Narrativa"
impacto_visual: "Minimalista/Silencioso & Editorial/Sofisticado"
custo_computacional: "Baixo (HTML Semântico, CSS Puro, Fontes WOFF2 Pré-carregadas, Speculation Rules API, Zero WebGL Pesado, Carregamento Instantâneo de Imagens)"
stack_frameworks:
  - "WordPress Engine Customizado & Headless Architecture"
  - "WP Rocket + RocketCDN + Speculation Rules API (Prefetch preditivo de links)"
  - "Plausible Analytics (Telemetria leve, privacy-first e cookieless)"
  - "Vanilla JavaScript / jQuery 3.7.1 modular"
  - "CSS Grid nativo & Flexbox utilitário sem frameworks inflados"
  - "Inter Display Font (v5.3.0 WOFF2 com preload de alta prioridade)"
compatibilidade:
  fontes_ideais:
    - "Neo-Grotesque Pura & Geométrica: Inter, Neue Haas Grotesk, PP Neue Montreal, Helvetica Neue, SF Pro, Suisse Int'l, Univers, General Sans"
    - "Serif Editorial Clássica & Refinada: EB Garamond, Cormorant Garamond, GT Sectra, Ogg, Freight Text, Newsreader, Times Now"
    - "Monoespaçada Funcional e Precisa: Geist Mono, SF Mono, Fragment Mono, IBM Plex Mono, Space Mono, Aperçu Mono"
  paletas_ideais:
    - "Monocromático Puro Minimal (Light Core): #FFFFFF (Canvas Pure Light), #F8F8F8 (Surface Off-White), #EAEAEA (Hairline Border 1px), #111111 (High-Contrast Ink Primary), #767676 (Subtle Muted Meta)"
    - "Dark Obsidian Minimal (Dark Mode Alt+M): #000000 (Void Base), #0D0D0D (Card Surface), #222222 (Hairline Muted Border), #FFFFFF (Primary White Type), #888888 (Secondary Zinc Type)"
    - "Warm Paper Minimalist (Japanese Editorial): #FBFBFA (Warm Linen), #F2F1ED (Muted Cream), #E3E1DA (Soft Rule Border), #1A1A1A (Carbon Black), #6E6D67 (Stone Meta)"
    - "Nordic Alabaster & Slate: #FAFAFB, #F0F1F3, #DCDFE4, #12151A, #5F6773"
  combinacoes_recomendadas:
    - "Tailwind CSS com `border-zinc-200 dark:border-zinc-800` + `bg-white dark:bg-black` + `text-zinc-900 dark:text-zinc-100` para grids puros e contrastes afiados"
    - "Framer Motion com transições sutis de opacidade (`duration: 0.18, ease: [0.16, 1, 0.3, 1]`) ou alternâncias de estado sem atraso artificial para sensação analógica instantânea"
    - "Next.js / Astro com renderização estática SSG e `speculationrules` para navegação com zero milissegundos de latência"
    - "Lucide React / Radix Icons com espessura fina (`strokeWidth={1.5}` ou `strokeWidth={2}`) e dimensões contidas de 18px a 24px"
  conflitos_esteticos:
    - "Efeitos de iluminação teatral exagerada (Glow neon, cones radiais cósmicos, border-beams fluorescentes tipo Cyberpunk/Crypto)"
    - "Sombras projetadas volumosas ou difusas (`box-shadow: 0 20px 50px rgba(0,0,0,0.2)`); o minimalismo autêntico exige bordas hairline de 1px ou planaridade pura"
    - "Tipografias decorativas extravagantes, fontes 3D, bolhas ou script informais infantis (ex: Comic Sans, Lobster, Pacifico, Poppins gordinha)"
    - "Gradientes multicoloridos espalhafatosos (arco-íris, roxo-magenta saturado sobrepostos a textos sem propósito funcional)"
    - "Scrolljacking agressivo, animações acrobáticas (cards girando 360 graus, zooms vertiginosos) que atrasam o acesso ao conteúdo"
    - "Popups intrusivos, modais bloqueantes de newsletter logo no primeiro segundo de visualização"
---

# Minimal Gallery — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
███╗   ███╗██╗███╗   ██╗██╗███╗   ███╗ █████╗ ██╗         ██████╗  █████╗ ██╗     ██╗     ███████╗██████╗ ██╗   ██╗
████╗ ████║██║████╗  ██║██║████╗ ████║██╔══██╗██║        ██╔════╝ ██╔══██╗██║     ██║     ██╔════╝██╔══██╗╚██╗ ██╔╝
██╔████╔██║██║██╔██╗ ██║██║██╔████╔██║███████║██║        ██║  ███╗███████║██║     ██║     █████╗  ██████╔╝ ╚████╔╝ 
██║╚██╔╝██║██║██║╚██╗██║██║██║╚██╔╝██║██╔══██║██║        ██║   ██║██╔══██║██║     ██║     ██╔══╝  ██╔══██╗  ╚██╔╝  
██║ ╚═╝ ██║██║██║ ╚████║██║██║ ╚═╝ ██║██║  ██║███████╗    ╚██████╔╝██║  ██║███████╗███████╗███████╗██║  ██║   ██║   
╚═╝     ╚═╝╚═╝╚═╝  ╚═══╝╚═╝╚═╝     ╚═╝╚═╝  ╚═╝╚══════╝     ╚═════╝ ╚═╝  ╚═╝╚══════╝╚══════╝╚══════╝╚═╝  ╚═╝   ╚═╝   
             FOR THE LOVE OF BEAUTIFUL & FUNCTIONAL WEBSITES — SINCE 2013
```

---

## 1. DNA Estético & Filosofia de Curadoria

Fundado em 2013 pelo designer independente alemão **Piet Terheyden**, o **Minimal Gallery** (`https://minimal.gallery/`) representa um dos mais longevos, influentes e respeitados templos da cultura digital minimalista global. O projeto nasceu de uma necessidade funcional concreta: aos 15 anos de idade, fascinado pelo design visual e pela arquitetura da web, Terheyden acumulava centenas de links de websites refinados em seus favoritos de navegador. A lista tornou-se caótica, desorganizada e visualmente cega. Para solucionar o problema, ele abriu um blog simples na plataforma Tumblr para guardar capturas de tela dos layouts que admirava — sem nome de marca, sem modelo de negócios e sem audiência premeditada.

O que era um arquivo pessoal transformou-se organicamente em um dos destinos mais consultados por directores de arte, tipógrafos e engenheiros de interface em todo o mundo. Sob o manifesto expresso em seu cabeçalho — **"For the love of beautiful & functional websites"** —, o Minimal Gallery construiu uma reputação inabalável fundamentada em três pilares curatoriais rigorosos:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                    THE MINIMAL GALLERY CURATORIAL FOUNDATION                           │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  [ STRICT DAILY CADENCE ]  ──►  [ ZERO PAID INFLUENCE ]  ──►  [ LIVING PRODUCTION CODE]│
│   • Max 1 website per day       • 100% Free submissions       • Real in-the-wild URLs  │
│   • 95%+ rejection rate         • Zero "pay-to-feature"       • Desktop + Mobile view  │
│   • Human-curated poise         • Equal merit for students    • High typographic craft │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  AESTHETIC PILLARS: Swiss Grid • Intentional Whitespace • Quiet Craft • High Restraint │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 As Três Leis Inquebráveis de Piet Terheyden

1. **A Regra do "Nunca Mais de Um Post por Dia"**:
   Enquanto agregadores automatizados e portais comerciais publicam dezenas de links diários via web scraping ou parcerias comerciais inflacionadas, o Minimal Gallery adota uma cadência deliberadamente lenta e meditativa. Terheyden instituiu o teto de **um único website selecionado a cada 24 horas**. Essa restrição forçou um funil de qualidade extremo, onde centenas de submissões semanais são sumariamente rejeitadas para dar destaque apenas ao design que atinge maturidade tipográfica, clareza espacial e equilíbrio estético inquestionáveis.

2. **O Princípio de Submissão 100% Gratuita e Meritocrática**:
   Em um ecossistema digital corrompido por modelos do tipo *"Pague US$ 50 para pular a fila de avaliação"* ou *"Patrocine um post para aparecer na home"*, o Minimal Gallery manteve-se obstinadamente gratuito por mais de 13 anos. A visibilidade nunca pôde ser comprada. Esse princípio garantiu que o portfólio de um estudante recém-formado em Zurique ou Tóquio competisse em condições de igualdade absoluta com a campanha milionária da maior agência de publicidade de Londres ou Nova York.

3. **A Exigência do "Código Vivo em Produção"**:
   Diferente de redes sociais conceituais (como Dribbble ou Behance) onde conceitos não codificáveis e maquetes tridimensionais fantasiosas geram expectativas irrealistas, o Minimal Gallery cataloga exclusivamente **interfaces reais, online e operacionais**. O foco reside em inspecionar como a tipografia se comporta na renderização nativa de fontes web, como o grid responde ao redimensionamento de viewport e como os dados reais ocupam o espaço.

### 1.2 A Linhagem Visual: Do Modernismo Suíço ao "Quiet Digital Craft"

O DNA visual do Minimal Gallery e dos projetos selecionados em suas páginas descende diretamente da tradição do **International Typographic Style** (Estilo Tipográfico Suíço, consolidado nas décadas de 1950 e 1960 por figuras como Josef Müller-Brockmann, Max Bill e Emil Ruder) mesclado aos preceitos de **Dieter Rams** (*"Weniger, aber besser"* — Menos, porém melhor):

- **Espaço Negativo como Matéria Estrutural**: O espaço em branco (ou negro) não é ausência de design; é o elemento ativo mais poderoso da composição. Ele define o ritmo respiratório do leitor, isola a informação crítica e confere gravidade quase cerimonial a cada bloco de texto ou imagem.
- **Tipografia como Elemento Construtivo Primário**: No design minimalista genuíno, a tipografia não apenas rotula a interface — ela **é** a interface. O contraste entre peso visual (Bold vs. Regular vs. Light), a escala proporcional disciplinada e o tracking micrométrico substituem adornos gráficos, ilustrações coloridas ou caixas coloridas.
- **Linhas Hairline e Planaridade Concreta**: Recusa sistemática de sombras difusas vulgares ou gradientes de simulação de relevo pesado. A geometria é delimitada por linhas horizontais e verticais finas de `1px` (`#EAEAEA` no light, `#222222` no dark) ou repousa em planaridade pura, respeitando a bidimensionalidade natural da tela de cristal líquido.
- **Sobriedade Cromática Monocromática**: A paleta de sustentação gravita entre o branco linho/papel e o preto profundo, utilizando a fotografia ou as obras em exibição como o único ponto de calor visual (*color accent* orgânico).

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        MINIMAL GALLERY ARCHITECTURAL ENGINE                            │
├────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                        │
│  [ TRI-SPLIT HEADER ] ──► [Left: Websites/Templates/Tools] [Center: Logotype]          │
│                           [Right: Search Modal / About / Submit CTA / Bookmarks Count] │
│                                                                                        │
│  [ EDITORIAL INTRO ]  ──► H1: "For the love of beautiful & functional websites"        │
│                           Integrated Compact Weekly Digest Form                        │
│                                                                                        │
│  [ TAG FILTER PILLS]  ──► AI • Portfolio (986) • Personal (810) • Agency (763) • ...   │
│                           "All types" Button ──► Full-Screen Search Modal (ESC)        │
│                                                                                        │
│  [ MODULAR GRID ]     ──► Responsive 3-Col / 2-Col / 1-Col Grid of 1.8:1 Cards         │
│                           Hover Actions: Direct Visit ↗ & Add to Bookmark Collection   │
│                                                                                        │
│  [ DUAL INSPECTOR ]   ──► Single Post View: Desktop 1440x800 vs Mobile 375x667 (DPR)  │
│                           Submitter Credit • Type Taxonomy • Direct Outbound Link      │
│                                                                                        │
│  [ CLIENT STORAGE ]   ──► LocalStorage Bookmarks Engine (Collections: Create/Edit)     │
│  [ THEME BAR (Alt+M)] ──► Native Dark/Light Toggle with Keyboard Shortcut & Speculation│
│                                                                                        │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

O Minimal Gallery é a **Referência Primária de Direção de Arte** sempre que o objetivo do projeto for transmitir autoridade intelectual, sofisticação discreta (*quiet luxury*), transparência funcional e máxima economia de meios expressivos.

### 2.1 Matriz de Arquétipos de Projeto & Posicionamento

| Arquétipo de Projeto | Por Que o Minimal Gallery é a Referência Suprema | Emoção / Mensagem Comunicada |
| :--- | :--- | :--- |
| **Portfólios de Designers, Arquitetos & Curadores** | A interface recua inteiramente para o segundo plano, transformando-se em uma parede de galeria de arte imaculada onde o trabalho do criador brilha sem ruído competitivo. | "Meu trabalho fala por si mesmo; tenho confiança absoluta e não preciso de truques visuais." |
| **Estúdios de Arquitetura & Design de Interiores** | Grids assimétricos rigorosos, tipografia sóbria e proporções generosas que ecoam o planejamento espacial e a pureza estrutural da própria arquitetura física. | Precisão milimétrica, elegância atemporal, respeito pelos materiais e pelo espaço. |
| **Type Foundries & Vitrines de Tipografia** | Foco obsessivo no detalhe do glifo, entrelinhas generosas, tamanhos de fonte monumentais alternados com metadados minúsculos de alta precisão. | Excelência artesanal, rigor tipográfico histórico, maestria na forma da letra. |
| **SaaS de Produtividade Silenciosa & DevTools** | Aplicações focadas em fluxo de trabalho profundo (*deep work*), editores de texto markdown, blocos de notas minimalistas e consoles de dados (ex: Raycast, iA Writer, Cron, Caudal). | "Zero distrações, velocidade relâmpago, foco absoluto no seu pensamento e execução." |
| **Marcas de Moda de Luxo Discreto & Joalheria** | E-commerces que rejeitam a agressividade promocional tradicional em favor de uma experiência editorial silenciosa (estilo The Row, Lemaire, Aesop, Kinfolk). | Exclusividade, refinamento artesanal, maturidade estética e alta classe sem ostentação. |
| **Editoras Independentes & Plataformas de Leitura** | Hierarquia de leitura confortável, proporções áureas de texto, margens que protegem o olhar e transições instantâneas entre ensaios e artigos. | Respeito pelo intelecto do leitor, foco na profundidade do pensamento e na palavra escrita. |

### 2.2 O Minimal Gallery e a Regra Proporcional 60-30-10

A harmonia visual do minimalismo de linhagem europeia depende de uma distribuição de massa visual matematicamente equilibrada:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                     A REGRA 60-30-10 NA ESTÉTICA MINIMAL GALLERY                       │
├────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                        │
│   ████████████████████████████████████████████   ░░░░░░░░░░░░░░░░░░░░░   ▓▓▓▓▓▓▓       │
│   [ 60% ESPAÇO NEGATIVO / CANVAS PURO ]         [ 30% TIPOGRAFIA / GRID] [ 10% ACENTO ]│
│   • Fundo branco puro ou negro absoluto         • Tipografia Neo-Grotesk • Badge sutil │
│   • Margens de respiro desimpedidas             • Linhas Hairline 1px    • Seta link ↗ │
│   • Silêncio visual contemplativo               • Rótulos de metadados   • Bookmark    │
│                                                                                        │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

1. **60% — O Canvas Desobstruído & Espaço Negativo Ativo (Dominante)**:
   - A fundação é construída sobre um vazio intencional. No modo claro, utiliza-se branco puro `#FFFFFF` ou linho suave `#FBFBFA`; no modo escuro, o preto mineral `#000000` ou grafite `#0A0A0A`.
   - O padding lateral e vertical é generoso (`clamp(2rem, 5vw, 6rem)`), garantindo que os elementos nunca toquem as bordas da tela nem disputem atenção entre si.

2. **30% — A Estrutura do Grid Tipográfico & Hairlines de Precisão (Secundário)**:
   - Toda a ordem visual deriva da tipografia: títulos em tamanhos display com kerning apertado, corpos de texto com excelente proporção x-height e metadados auxiliares em caixa-alta minúscula (`uppercase tracking-wider text-[11px]`).
   - As divisórias são estritamente de `1px solid` com opacidade reduzida (`#EAEAEA` no light, `#222222` no dark), criando uma malha ortogonal invisível que guia os olhos.

3. **10% — O Acento Funcional & O Conteúdo Emoldurado (Acento)**:
   - O acento nunca é uma explosão neon arbitrária. O foco colorido ou magnético é fornecido exclusivamente pelas imagens dos trabalhos em exibição, pelo botão de pílula preta com texto branco invertido (`bg-black text-white hover:bg-neutral-800`), pela seta de link externo diagonal (`lucide:arrow-up-right`) ou pelo badge de contagem de bookmarks (`<em>`).

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

Tentar impor o minimalismo radical do Minimal Gallery a contextos inadequados pode resultar em catástrofes de conversão, confusão operacional e exclusão de públicos.

### 3.1 Cenários de Incompatibilidade Crítica

- ⚠️ **E-Commerce Tradicional de Alto Volume & Varejo Popular (Black Friday, Liquidações, Supermercados)**:
  Consumidores em busca de descontos esperam estímulos de urgência: tags de porcentagem vermelhas chamativas, contadores regressivos dinâmicos, selos de frete grátis coloridos e banners de oferta. Um design silencioso estilo Minimal Gallery comunica preço alto, frieza ou escassez desfavorável, desestimulando a compra impulsiva.
- ⚠️ **Produtos Digitais Infantis & Ferramentas Gamificadas (Duolingo, Jogos Casuais, Plataformas Educacionais Kids)**:
  Exigem dinamismo lúdico, cantos arredondados gigantescos (raios de 24px a 40px), paletas multicoloridas de alta saturação, mascotes expressivos e feedback sonoro expansivo. O ascetismo suíço é recebido pelo público jovem como algo enfadonho, punitivo ou burocrático.
- ⚠️ **Web3 Degen, Memecoins & Comunidades de Alta Adrenalina**:
  Ambientes movidos a especulação e cultura de meme prosperam na saturação visual: WebGL holográfico, partículas flutuantes, tipografia retro-brutalista caótica, gifs animados e gráficos fluorescentes. A sobriedade do Minimal Gallery anula o efeito psicológico de hype coletivo.
- ⚠️ **Portais Governamentais e Serviços Cívicos de Consulta Complexa**:
  Cidadãos de diferentes níveis de alfabetização digital precisam de affordances óbvias, botões tridimensionais reconhecíveis e caminhos hiper-visíveis. O minimalismo excessivo, que esconde ações sob hover ou reduz ícones a traços ultra-finos, cria barreiras severas de acessibilidade cognitiva.

### 3.2 Armadilhas de Imitação ("The Void Trap", "Micro-Font Arrogance" & "Zero Affordance")

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                       ARMADILHAS DE IMITAÇÃO DO MINIMALISMO RADICAL                     │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  1. THE VOID TRAP         ──►  Espalhar quilômetros de espaço vazio sem tensão         │
│                                tipográfica interna, transformando o site num deserto.   │
│  2. MICRO-FONT ARROGANCE  ──►  Usar fontes de 10px cinza-claro sobre fundo branco,     │
│                                violando WCAG e tornando o texto ilegível para humanos. │
│  3. ZERO AFFORDANCE       ──►  Esconder todos os links e botões até que o usuário      │
│                                adivinhe onde passar o mouse (hover hunting às cegas).  │
│  4. FLAT LAZINESS         ──►  Ignorar estados interativos de foco, erro e loading em  │
│                                nome de uma suposta "pureza estética imóvel".           │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

1. **A Armadilha do Vazio Estéril ("The Void Trap")**:
   Colocar apenas uma linha de texto centralizada cercada por 1000px de espaço vazio não é minimalismo suíço — é falta de substância. O minimalismo autêntico vive da **tensão relacional**: o choque formal entre um cabeçalho grande e uma coluna compacta de texto, ou entre uma imagem estrita de proporção 1.8:1 e um alinhamento assimétrico no grid.
2. **A Arrogância da Micro-Tipografia Ilegível**:
   Reduzir metadados e textos de apoio para 9px ou 10px com cor cinza `#B0B0B0` sobre fundo `#FFFFFF`. Isso fere brutalmente as diretrizes WCAG AA de contraste (mínimo de 4.5:1 para texto normal) e torna a experiência inacessível em telas com baixa densidade de pixels ou sob iluminação solar direta.
3. **A Caça ao Clique às Cegas ("Zero Affordance")**:
   Esconder completamente setas, indicadores de link ou ícones interativos, forçando o visitante a varrer a tela com o ponteiro do mouse para descobrir o que é clicável. As affordances no Minimal Gallery são discretas, porém imediatamente compreensíveis via cursores adequados (`cursor: pointer`), sublinhados sutis ou micro-badges de endereço externo (`↗`).

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

A dissecação arquitetural do portal do Minimal Gallery revela uma aula magna de engenharia de layout:

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        MINIMAL GALLERY 3-COLUMN MODULAR GRID                           │
├────────────────────────┬────────────────────────┬──────────────────────────────────────┤
│ COLUNA 1               │ COLUNA 2               │ COLUNA 3                             │
│ ┌────────────────────┐ │ ┌────────────────────┐ │ ┌────────────────────┐               │
│ │ Media (1.8:1)      │ │ │ Media (1.8:1)      │ │ │ Media (1.8:1)      │               │
│ │ [Thumb 900x500]    │ │ │ [Thumb 900x500]    │ │ │ [Thumb 900x500]    │               │
│ ├────────────────────┤ │ ├────────────────────┤ │ ├────────────────────┤               │
│ │ H3 Site Title      │ │ │ H3 Site Title      │ │ │ H3 Site Title      │               │
│ │ time: "today"      │ │ │ time: "1 day ago"  │ │ │ time: "2 days ago" │               │
│ └────────────────────┘ │ └────────────────────┘ │ └────────────────────┘               │
│ [gap-x: 24px-32px]     │ [gap-x: 24px-32px]     │ [gap-y: 40px-48px]                   │
└────────────────────────┴────────────────────────┴──────────────────────────────────────┘
```

- **Malha Responsiva de Cards**: No desktop (telas `> 1024px`), os projetos são distribuídos em 3 colunas rigorosas com largura flexível calculada via CSS Grid (`grid-template-columns: repeat(3, minmax(0, 1fr))`). Em tablets (`768px - 1024px`), colapsa graciosamente para 2 colunas; em smartphones (`< 768px`), assume 1 coluna única centralizada.
- **Aspect Ratio Imutável**: Todas as miniaturas de exibição seguem a proporção rigorosa de **1.8:1** (dimensões base de `900x500` pixels), capturando exatamente a dobra superior e o horizonte visual do site analisado.
- **Ritmo Vertical Desacelerado**: Os cartões mantêm um espaçamento vertical generoso (`margin-bottom: 2.5rem` a `3rem`), permitindo que cada trabalho seja contemplado como uma peça isolada, sem sensação de amontoamento visual.
- **Linhas Hairline de Contorno**: As seções do site são delimitadas por divisórias ultra-finas de `1px solid rgba(0, 0, 0, 0.08)` (no modo claro) e `1px solid rgba(255, 255, 255, 0.1)` (no modo escuro), sem gradientes ou sombras emuladas.

### 4.2 Sistemas de Cores, Superfícies & Texturas

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        MINIMAL GALLERY DUAL-SURFACE MATRIX                             │
├────────────────────────┬───────────────────────────┬───────────────────────────────────┤
│ TOKEN SEMÂNTICO        │ LIGHT MODE (DEFAULT)      │ DARK MODE (ALT + M)               │
├────────────────────────┼───────────────────────────┼───────────────────────────────────┤
│ Canvas Background      │ #FFFFFF (Pure White)      │ #000000 (Pure Obsidian)           │
│ Card Surface / Media   │ #F5F5F5 (Paper Tint)      │ #0E0E0E (Sub-black Charcoal)      │
│ Border Hairline        │ #EAEAEA (Neutral Rule)    │ #222222 (Deep Grey Rule)          │
│ Border Active/Hover    │ #111111 (Solid Black)     │ #FFFFFF (Solid White)             │
│ Text Primary (H1/H3)   │ #000000 / #111111         │ #FFFFFF / #F4F4F6                 │
│ Text Secondary (Meta)  │ #767676 (Muted Zinc)      │ #888888 (Muted Titanium)          │
│ Pill Accent Badge      │ #000000 (Fill) / #FFF (Tx)│ #FFFFFF (Fill) / #000 (Tx)        │
│ Bookmark Icon Fill     │ #000000 (Active State)    │ #FFFFFF (Active State)            │
└────────────────────────┴───────────────────────────┴───────────────────────────────────┘
```

---

### 4.3 Padrões de Seções / Fluxos (Arquétipos Concretos Extraídos)

Abaixo estão detalhados os **8 arquétipos estruturais mais emblemáticos** extraídos da anatomia técnica do Minimal Gallery:

#### Arquétipo 1: Tri-Split Balanced Header with Live Bookmarks Counter
- **Anatomia**: Barra de navegação horizontal dividida em três blocos de mesma relevância visual:
  - *Esquerda (`header-menu-left`)*: Navegação taxonômica primária (`Websites`, `Templates`, `Tools`).
  - *Centro (`header-menu-center`)*: O logotipo textual institucional em peso médio (`Minimal Gallery`), agindo como âncora de retorno à home.
  - *Direita (`header-menu-right`)*: Ações do usuário organizadas por prioridade decrescente: botão de busca com ícone de lupa SVG, link `About`, botão CTA com pílula de alto contraste `Submit` e link `Bookmarks` com badge numérico interativo (`<em id="header-menu-bookmarks-count">`).
- **Micro-interações**: No desktop, os links possuem transição sutil de opacidade no hover (`opacity: 1 -> 0.6`). O contador de bookmarks anima discretamente sua contagem via JavaScript sempre que um novo item é adicionado à coleção local.
- **Onde Aplicar**: Cabeçalho de plataformas de curadoria, publicações digitais culturais, portfólios corporativos e diretórios de alta patente.

#### Arquétipo 2: Editorial Intro with Seamless Inline Weekly Digest Box
- **Anatomia**: Seção de abertura composta por um título H1 editorial sóbrio em tipografia de impacto legível (`For the love of beautiful & functional websites`), acompanhado imediatamente por um bloco horizontal de inscrição de newsletter embutido. O formulário não polui com bordas volumosas: traz campos limpos de Nome e Email, botão de envio com seta linear minimalista (`->`) e nota de compromisso ético de envio semanal com link de cancelamento simples.
- **Micro-interações**: Ao submeter o formulário, o bloco realiza uma transição de opacidade sem recarregamento de página, exibindo a mensagem: *"Thanks, please confirm via email."*.
- **Onde Aplicar**: Heróis de publicações autorais, blogs técnicos de prestígio e plataformas independentes que valorizam a captação de audiência qualificada sem popups intrusivos.

#### Arquétipo 3: Horizontal Tag Carousel Bar with "All Types" Modal Anchor
- **Anatomia**: Barra horizontal de filtros rápidos posicionada imediatamente acima da galeria. Apresenta uma sequência rolável horizontalmente de tags em formato de pílula limpa (`AI`, `Portfolio`, `Personal`, `Startup`, `One page`, `Agency`, `E-commerce`, `Branding`, `Tools`, etc.), com barra de rolagem invisível. Na extremidade direita, repousa um botão estático fixo: `All types`.
- **Micro-interações**: Rolagem lateral suave com inércia nativa. Ao clicar em `All types`, o modal completo de busca taxonômica se abre instantaneamente.
- **Onde Aplicar**: Galerias com taxonomias extensas, catálogos de componentes, índices de documentação técnica e lojas virtuais refinadas.

#### Arquétipo 4: High-Restraint Showcase Card with Concealed Media Overlay
- **Anatomia**: Cartão retangular com proporção rígida de `1.8:1` (900x500px). Em estado de repouso, a imagem do site aparece limpa, sem qualquer elemento visual intrusivo por cima. Ao passar o cursor (*hover*), surge suavemente no canto superior direito uma caixa com dois botões circulares ou arredondados: o botão de bookmark (para salvar localmente) e o botão com ícone de link diagonal (`↗`) para visita externa imediata com parâmetro `?ref=minimal.gallery`. Abaixo da mídia, repousa o título H3 com link para o dossiê interno e um marcador temporal relativo (`today`, `2 days ago`, `3 weeks ago`).
- **Micro-interações**: Transição suave de opacidade no container de botões (`opacity: 0 -> 1` em 180ms), com zoom microscópico na imagem (`transform: scale(1.008)`), mantendo estabilidade física sem trepidação.
- **Onde Aplicar**: Vitrines de trabalhos, estudos de caso, catálogos de projetos e feeds de inspiração.

#### Arquétipo 5: Dual-Device Viewport Inspector (Desktop 1440x800 vs Mobile 375x667)
- **Anatomia**: Na página de detalhamento do projeto (`/atomicdust/`, `/bleibtgleich-2026/`), o layout divide-se em duas colunas:
  - *Coluna Esquerda*: Painel de metadados contendo botão de retorno (`<- Back`), título H1, botão de visita externa, botão de bookmark e lista de metadados: Tipo (`Agency`, `Branding`), Submitter (nome do criador) e Data de Publicação.
  - *Coluna Direita*: O visualizador principal com uma chave seletora (*segmented tabs*): `Desktop` (emulando viewport 1440x800 com DPR 1.33) e `Mobile` (emulando 375x667 com DPR 2). Abaixo, ferramentas de expansão (*lightbox expand/shrink*), menu de cópia rápida de URL com toast de confirmação (*"Copied!"*) e download direto do snapshot em alta resolução.
- **Micro-interações**: Alternância instantânea entre as capturas de tela Desktop e Mobile sem recarregamento, redimensionando o frame do visualizador com transição suave de opacidade.
- **Onde Aplicar**: Páginas de estudo de caso de agências digitais, documentação de design systems responsivos e plataformas de avaliação de UX.

#### Arquétipo 6: Full-Screen Modal Filter with Live Scope Switcher & Exact Post Counts
- **Anatomia**: Modal de busca acionado pela tecla universal `ESC` ou pelo botão de filtros. Divide-se em: campo de busca superior com botão de limpeza (`clear`), chave de escopo em 3 modos (`Websites`, `Templates`, `Tools`) e uma listagem alfabética de tags organizadas em colunas compactas. Cada tag traz uma linha divisória pontilhada ou sólida (`<hr>`) e a quantidade exata de websites cadastrados (`<em>986</em>`, `<em>763</em>`, etc.).
- **Micro-interações**: Filtro em tempo real via JavaScript com renderização instantânea de resultados enquanto o usuário digita. Fechamento imediato ao pressionar `ESC` ou clicar fora do painel.
- **Onde Aplicar**: Mecanismos de busca interna em sites de acervo denso, ferramentas de documentação técnica de API e bibliotecas de componentes.

#### Arquétipo 7: Client-Side LocalStorage Bookmark Engine with Custom Collections
- **Anatomia**: Sistema soberano de favoritos que não exige criação de conta, login social ou banco de dados em nuvem. Utiliza o `localStorage` do navegador para armazenar IDs de websites, miniaturas e títulos. Permite ao usuário criar coleções personalizadas (*"Add collection"*, *"Edit collection"*), renomeá-las e deletá-las localmente.
- **Micro-interações**: Adição instantânea com feedback visual no botão de marcador (ícone SVG preenchido solidamente) e atualização imediata do contador no cabeçalho.
- **Onde Aplicar**: Plataformas que prezam pela privacidade do usuário (*zero tracking / local-first*), ferramentas de ideação e dashboards pessoais.

#### Arquétipo 8: Keyboard-Accessible Theme Switcher Footer Bar (`Alt + M`)
- **Anatomia**: Barra de rodapé elegante e completa contendo aviso de copyright histórico (`© Minimal Gallery 2013-2026`), créditos explícitos (*"A project founded by Piet"*), links organizados em 3 colunas hierárquicas (`Site`, `Resources`, `Social`) e um botão de alternância de tema no canto inferior direito que exibe explicitamente o atalho de teclado: `Alt + M` em elementos `<kbd>`.
- **Micro-interações**: O atalho `Alt + M` alterna globalmente as classes `.light` e `.dark` no elemento `<html>` e persiste a preferência em `localStorage.getItem("mg_theme")`, garantindo que na próxima visita a renderização inicial não cause efeito indesejado de flash (*FOUC*).
- **Onde Aplicar**: Rodapé de aplicações web orientadas a desenvolvedores, sites editoriais e ferramentas de produtividade acessíveis por teclado.

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Calibração de Física de Movimento & Transições Silenciosas

Na filosofia do Minimal Gallery, animações bombásticas, elásticas ou lentas são tratadas como aberrações de usabilidade. A interface deve ser ágil, silenciosa e objetiva:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                   MINIMAL GALLERY MOTION PHYSICS CALIBRATION                           │
├────────────────────────┬────────────────────────────────┬──────────────────────────────┤
│ TIPO DE TRANSIÇÃO      │ DURAÇÃO / TIMING               │ CUBIC-BEZIER EQUIVALENTE     │
├────────────────────────┼────────────────────────────────┼──────────────────────────────┤
│ Hover em Miniatura     │ 180ms - 220ms                  │ cubic-bezier(0.16, 1, 0.3, 1)│
│ Ações Flutuantes       │ 150ms                          │ ease-out                     │
│ Abertura de Modal ESC  │ 200ms                          │ cubic-bezier(0, 0, 0.2, 1)   │
│ Alternância Dark/Light │ Instantânea (0ms a 100ms)      │ linear                       │
│ Segmented Control Tab  │ 160ms                          │ ease-in-out                  │
└────────────────────────┴────────────────────────────────┴──────────────────────────────┘
```

---

### 5.2 Tokens CSS & Variáveis de Sistema (Minimal Gallery Preset)

Abaixo está o conjunto canônico de variáveis CSS para criar um ambiente visual idêntico ao Minimal Gallery, com suporte completo ao tema claro (padrão) e escuro:

```css
:root {
  /* ==========================================================================
     MINIMAL GALLERY DESIGN TOKENS — LIGHT MODE (DEFAULT)
     ========================================================================== */
  --mg-canvas-bg: #ffffff;
  --mg-surface-subtle: #f8f8f8;
  --mg-surface-card: #f3f3f3;
  --mg-surface-overlay: rgba(255, 255, 255, 0.96);

  /* Hairlines & Bordas */
  --mg-border-hairline: #eaeaea;
  --mg-border-hover: #111111;
  --mg-border-active: #000000;

  /* Tipografia & Tinta */
  --mg-text-primary: #111111;
  --mg-text-secondary: #767676;
  --mg-text-muted: #999999;
  --mg-text-inverse: #ffffff;

  /* Botões & Ações Primárias */
  --mg-button-bg: #111111;
  --mg-button-text: #ffffff;
  --mg-button-hover-bg: #333333;

  /* Dimensões & Proporções */
  --mg-max-width: 1440px;
  --mg-gutter: clamp(1.25rem, 4vw, 3rem);
  --mg-card-ratio: 1.8 / 1;
}

/* ==========================================================================
   MINIMAL GALLERY DESIGN TOKENS — DARK MODE (.dark / Alt+M)
   ========================================================================== */
html.dark, body.dark {
  --mg-canvas-bg: #000000;
  --mg-surface-subtle: #0d0d0d;
  --mg-surface-card: #141414;
  --mg-surface-overlay: rgba(0, 0, 0, 0.96);

  --mg-border-hairline: #222222;
  --mg-border-hover: #ffffff;
  --mg-border-active: #ffffff;

  --mg-text-primary: #f4f4f6;
  --mg-text-secondary: #888888;
  --mg-text-muted: #666666;
  --mg-text-inverse: #000000;

  --mg-button-bg: #ffffff;
  --mg-button-text: #000000;
  --mg-button-hover-bg: #e0e0e0;
}
```

---

### 5.3 Código Funcional Completo: Componente React "MinimalGalleryCard"

Este componente implementa em padrão de produção o card oficial do Minimal Gallery: miniatura com proporção rígida de 1.8:1, ações de bookmark e link externo reveladas suavemente no hover, metadados com marcador temporal relativo e integração completa com Tailwind CSS e React:

```tsx
import React, { useState } from "react";
import { Bookmark, ArrowUpRight } from "lucide-react";

export interface MinimalCardProps {
  id: string | number;
  title: string;
  slug: string;
  externalUrl: string;
  thumbnailUrl: string;
  publishedRelativeTime: string;
  isBookmarked?: boolean;
  onToggleBookmark?: (id: string | number) => void;
}

export const MinimalGalleryCard: React.FC<MinimalCardProps> = ({
  id,
  title,
  slug,
  externalUrl,
  thumbnailUrl,
  publishedRelativeTime,
  isBookmarked = false,
  onToggleBookmark,
}) => {
  const [bookmarked, setBookmarked] = useState(isBookmarked);
  const [isHovered, setIsHovered] = useState(false);

  const handleBookmarkClick = (e: React.MouseEvent) => {
    e.preventDefault();
    e.stopPropagation();
    const newState = !bookmarked;
    setBookmarked(newState);
    if (onToggleBookmark) {
      onToggleBookmark(id);
    }
  };

  return (
    <article
      className="group flex flex-col w-full"
      onMouseEnter={() => setIsHovered(true)}
      onMouseLeave={() => setIsHovered(false)}
    >
      {/* Container de Mídia com Proporção Rígida de 1.8:1 */}
      <div className="relative aspect-[1.8/1] w-full overflow-hidden bg-neutral-100 dark:bg-neutral-900 border border-neutral-200/60 dark:border-neutral-800/80 transition-colors duration-200">
        <a
          href={`/websites/${slug}`}
          className="block h-full w-full"
          aria-label={`View details for ${title}`}
        >
          <img
            src={thumbnailUrl}
            alt={`${title} website preview`}
            width={900}
            height={500}
            loading="lazy"
            decoding="async"
            className="h-full w-full object-cover transition-transform duration-300 ease-out group-hover:scale-[1.008]"
          />
        </a>

        {/* Botões de Ação Revelados no Hover (Canto Superior Direito) */}
        <div
          className={`absolute top-3 right-3 flex items-center gap-1.5 transition-opacity duration-200 ease-out ${
            isHovered ? "opacity-100 pointer-events-auto" : "opacity-0 pointer-events-none"
          }`}
        >
          {/* Botão Salvar Bookmark */}
          <button
            type="button"
            onClick={handleBookmarkClick}
            title={bookmarked ? "Remove from bookmarks" : "Bookmark website"}
            aria-label={bookmarked ? "Remove from bookmarks" : "Bookmark website"}
            className="flex h-8 w-8 items-center justify-center rounded-full bg-white/90 dark:bg-neutral-900/90 text-neutral-900 dark:text-neutral-100 shadow-sm backdrop-blur-sm border border-neutral-200 dark:border-neutral-700 hover:scale-105 active:scale-95 transition-all duration-150"
          >
            <Bookmark
              size={15}
              strokeWidth={2}
              className={bookmarked ? "fill-neutral-900 dark:fill-neutral-100" : ""}
            />
          </button>

          {/* Botão Visita Direta ao Site Externo */}
          <a
            href={`${externalUrl}${externalUrl.includes("?") ? "&" : "?"}ref=minimal.gallery`}
            target="_blank"
            rel="noopener noreferrer"
            title="Visit live website"
            aria-label={`Visit ${title} website in new tab`}
            className="flex h-8 w-8 items-center justify-center rounded-full bg-white/90 dark:bg-neutral-900/90 text-neutral-900 dark:text-neutral-100 shadow-sm backdrop-blur-sm border border-neutral-200 dark:border-neutral-700 hover:scale-105 active:scale-95 transition-all duration-150"
          >
            <ArrowUpRight size={15} strokeWidth={2} />
          </a>
        </div>
      </div>

      {/* Bloco de Texto & Metadados Abaixo da Mídia */}
      <div className="mt-3 flex items-baseline justify-between gap-2 px-0.5">
        <h3 className="text-[15px] font-medium tracking-tight text-neutral-900 dark:text-neutral-100">
          <a
            href={`/websites/${slug}`}
            className="hover:underline underline-offset-4 decoration-neutral-300 dark:decoration-neutral-700 transition-colors"
          >
            {title}
          </a>
        </h3>

        <time
          dateTime={new Date().toISOString()}
          className="text-[12px] font-normal text-neutral-500 dark:text-neutral-400 whitespace-nowrap"
        >
          {publishedRelativeTime}
        </time>
      </div>
    </article>
  );
};
```

---

### 5.4 Código Funcional Completo: Header Tri-Partite do Minimal Gallery

```tsx
import React, { useState, useEffect } from "react";
import { Search, Bookmark } from "lucide-react";

interface MinimalHeaderProps {
  activeTab?: "websites" | "templates" | "tools";
  bookmarksCount?: number;
  onOpenSearchModal?: () => void;
  onToggleTheme?: () => void;
}

export const MinimalGalleryHeader: React.FC<MinimalHeaderProps> = ({
  activeTab = "websites",
  bookmarksCount = 0,
  onOpenSearchModal,
  onToggleTheme,
}) => {
  const [count, setCount] = useState(bookmarksCount);

  // Escuta atalho Alt + M para alternar tema
  useEffect(() => {
    const handleKeyDown = (e: KeyboardEvent) => {
      if (e.altKey && (e.key === "m" || e.key === "M")) {
        e.preventDefault();
        if (onToggleTheme) onToggleTheme();
        else document.documentElement.classList.toggle("dark");
      }
    };
    window.addEventListener("keydown", handleKeyDown);
    return () => window.removeEventListener("keydown", handleKeyDown);
  }, [onToggleTheme]);

  return (
    <header className="sticky top-0 z-40 w-full border-b border-neutral-200/80 dark:border-neutral-800/80 bg-white/95 dark:bg-black/95 backdrop-blur-md transition-colors duration-200">
      <div className="mx-auto flex h-14 max-w-[1440px] items-center justify-between px-4 sm:px-6 lg:px-8">
        
        {/* Bloco Esquerda: Navegação Taxonômica */}
        <nav className="flex items-center gap-6">
          <a
            href="/websites/"
            className={`text-sm font-medium transition-colors ${
              activeTab === "websites"
                ? "text-neutral-900 dark:text-neutral-100"
                : "text-neutral-500 hover:text-neutral-900 dark:text-neutral-400 dark:hover:text-neutral-100"
            }`}
          >
            Websites
          </a>
          <a
            href="/templates/"
            className={`text-sm font-medium transition-colors ${
              activeTab === "templates"
                ? "text-neutral-900 dark:text-neutral-100"
                : "text-neutral-500 hover:text-neutral-900 dark:text-neutral-400 dark:hover:text-neutral-100"
            }`}
          >
            Templates
          </a>
          <a
            href="/tools/"
            className={`text-sm font-medium transition-colors ${
              activeTab === "tools"
                ? "text-neutral-900 dark:text-neutral-100"
                : "text-neutral-500 hover:text-neutral-900 dark:text-neutral-400 dark:hover:text-neutral-100"
            }`}
          >
            Tools
          </a>
        </nav>

        {/* Bloco Central: Logotipo Tipográfico */}
        <div className="text-center">
          <a
            href="/"
            className="text-[15px] font-semibold tracking-tight text-neutral-900 dark:text-neutral-100 hover:opacity-80 transition-opacity"
          >
            Minimal Gallery
          </a>
        </div>

        {/* Bloco Direita: Ações Utilitárias */}
        <div className="flex items-center gap-4">
          {/* Botão de Busca */}
          <button
            type="button"
            onClick={onOpenSearchModal}
            className="flex items-center gap-1.5 text-sm font-normal text-neutral-600 hover:text-neutral-900 dark:text-neutral-400 dark:hover:text-neutral-100 transition-colors"
          >
            <Search size={16} strokeWidth={2} />
            <span className="hidden sm:inline">Search</span>
          </button>

          <a
            href="/about/"
            className="hidden sm:inline text-sm font-normal text-neutral-600 hover:text-neutral-900 dark:text-neutral-400 dark:hover:text-neutral-100 transition-colors"
          >
            About
          </a>

          {/* Botão CTA Submit em Pílula */}
          <a
            href="/submit/"
            className="rounded-full bg-neutral-950 dark:bg-neutral-100 px-3.5 py-1 text-xs font-medium text-white dark:text-neutral-950 hover:bg-neutral-800 dark:hover:bg-neutral-200 transition-colors"
          >
            Submit
          </a>

          {/* Bookmarks com Contador */}
          <a
            href="/bookmarks/"
            className="flex items-center gap-1.5 text-sm font-normal text-neutral-600 hover:text-neutral-900 dark:text-neutral-400 dark:hover:text-neutral-100 transition-colors"
          >
            <Bookmark size={16} strokeWidth={2} />
            <span className="hidden sm:inline">Bookmarks</span>
            {count > 0 && (
              <span className="flex h-4 min-w-[1rem] items-center justify-center rounded-full bg-neutral-200 dark:bg-neutral-800 px-1 text-[10px] font-semibold text-neutral-900 dark:text-neutral-100">
                {count}
              </span>
            )}
          </a>
        </div>
      </div>
    </header>
  );
};
```

---

### 5.5 Como a IA Deve Pesquisar ao Vivo no Minimal Gallery

O Minimal Gallery possui uma arquitetura de rotas limpa baseada em taxonomias do WordPress, além de expor endpoints REST nativos (`/wp-json/`) que permitem que agentes inteligentes façam consultas programáticas em formato JSON estruturado com zero latência:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                     MINIMAL GALLERY REAL-TIME ROUTE & API MAP                          │
├────────────────────────┬───────────────────────────────────────────────────────────────┤
│ OBJETIVO DE BUSCA      │ ROTA DE URL DIRETA (PARA NAVEGADOR OU CURL)                   │
├────────────────────────┼───────────────────────────────────────────────────────────────┤
│ Catálogo Principal     │ https://minimal.gallery/websites/                             │
│ Paginação Específica   │ https://minimal.gallery/websites/page/<N>/                    │
│ Filtro: Portfólios     │ https://minimal.gallery/tag/portfolio/                        │
│ Filtro: Agências       │ https://minimal.gallery/tag/agency/                           │
│ Filtro: E-Commerce     │ https://minimal.gallery/tag/e-commerce/                       │
│ Filtro: Arquitetura    │ https://minimal.gallery/tag/architecture-interior-design/      │
│ Filtro: SaaS B2B       │ https://minimal.gallery/tag/saas/                             │
│ Filtro: Inteligência AI│ https://minimal.gallery/tag/ai/                               │
│ Filtro: Type Foundry   │ https://minimal.gallery/tag/type-foundry/                     │
│ Filtro: Páginas Únicas │ https://minimal.gallery/tag/one-page/                         │
│ Diretório de Templates │ https://minimal.gallery/templates/                            │
│ Templates por Stack    │ https://minimal.gallery/platform/framer/ ou /webflow/         │
│ Diretório Ferramentas  │ https://minimal.gallery/tools/                                │
│ REST API: Busca JSON   │ https://minimal.gallery/wp-json/wp/v2/posts?search=<query>    │
│ REST API: Tags JSON    │ https://minimal.gallery/wp-json/wp/v2/tags?per_page=100       │
│ Ficha de Detalhe       │ https://minimal.gallery/<slug-do-site>/                       │
└────────────────────────┴───────────────────────────────────────────────────────────────┘
```

> **Protocolo Operacional para Agentes de IA**: Ao buscar inspiração para um nicho específico solicitado pelo usuário, o agente deve acessar diretamente a tag taxonômica correspondente (ex: `/tag/architecture-interior-design/` para arquitetura ou `/tag/portfolio/` para portfólios autorais). Quando precisar extrair dados em massa sem efetuar parsing de páginas HTML com imagens pesadas, utilize a query direta na REST API: `curl -sL "https://minimal.gallery/wp-json/wp/v2/posts?per_page=10&search=<termo>"`.

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma interface cuja direção de arte tenha sido pautada pelo **Minimal Gallery**, o arquiteto de frontend e design system deve registrar no `DESIGN_BLUEPRINT.md` as seguintes definições normativas obrigatórias:

### 6.1 Filosofia Visual & Posicionamento de Marca
- Declarar o estilo oficial como **"Swiss Minimalist Editorial / Quiet Digital Craft"**.
- Estabelecer o compromisso de criar uma interface serena, onde o espaço em branco atua como o principal condutor visual e nenhuma decoração gráfica sem função é tolerada.

### 6.2 Estrutura de Grids & Superfícies
- Limitar o container principal em `max-w-[1440px]` com margens automáticas (`mx-auto`).
- Definir o espaçamento lateral flexível: `px-4 sm:px-6 lg:px-8`.
- Estruturar a exibição de itens em malha de 3 colunas no desktop (`grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 lg:gap-8`).
- Proporção obrigatória das mídias em **1.8:1** ou **16:9** com corte cirúrgico no topo (`object-cover object-top`).
- Proibir sombras projetadas difusas (`box-shadow: none`); separar elementos exclusivamente através de linhas hairline de `1px solid` (`border-neutral-200 dark:border-neutral-800`).

### 6.3 Tipografia & Escala Hierárquica
- **Família Display & Corpo**: Sans-serif Neo-Grotesca contemporânea com alta densidade tipográfica (Inter, Geist, PP Neue Montreal ou Neue Haas Grotesk).
- **Título Hero H1**: `text-2xl sm:text-3xl lg:text-4xl font-normal tracking-tight text-neutral-900 dark:text-neutral-100`.
- **Títulos de Cartão H3**: `text-[15px] font-medium tracking-tight text-neutral-900 dark:text-neutral-100`.
- **Metadados & Tempo Relativo**: `text-xs text-neutral-500 dark:text-neutral-400 font-normal`.
- **Rótulos de Tags e Badges**: `text-[11px] font-medium tracking-wider uppercase text-neutral-600 dark:text-neutral-400`.

### 6.4 Paleta de Cores & Tokens Normativos
- **Canvas Base**: `--bg-canvas: #FFFFFF` (Light) e `#000000` (Dark).
- **Superfície Secundária**: `--bg-surface: #F8F8F8` (Light) e `#0D0D0D` (Dark).
- **Linhas Divisórias**: `--border-hairline: #EAEAEA` (Light) e `#222222` (Dark).
- **Tinta Tipográfica Primária**: `--text-primary: #111111` (Light) e `#F4F4F6` (Dark).
- **Tinta Tipográfica Secundária**: `--text-secondary: #767676` (Light) e `#888888` (Dark).
- **Acento Primário (10%)**: Monocromático de alto contraste: pílulas pretas sólidas com texto branco no modo claro, e pílulas brancas com texto preto no modo escuro.

### 6.5 Checklist de Componentes Obrigatórios
- [ ] Header tri-partido com navegação taxonômica à esquerda, logo centralizado e ações à direita.
- [ ] Barra horizontal de tags rolável com indicador de quantidade e botão para modal completo.
- [ ] Cartões de projeto com proporção 1.8:1 e botões de ação flutuantes revelados no hover.
- [ ] Visualizador de detalhe com alternância entre viewports Desktop e Mobile com indicação de DPR.
- [ ] Alternador de tema Light/Dark acessível por atalho de teclado global (`Alt + M`).
- [ ] Sistema de bookmarks client-side utilizando `localStorage` sem exigência de login.
- [ ] Rodapé com aviso de copyright, links categorizados e indicação do atalho `<kbd>Alt</kbd> + <kbd>M</kbd>`.
- [ ] Diretriz de pré-carregamento com `<script type="speculationrules">` para navegação instantânea com latência zero.
