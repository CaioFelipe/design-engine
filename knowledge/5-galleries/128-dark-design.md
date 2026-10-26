---
id: "128-dark-design"
name: "Dark Mode Design"
url: "https://www.dark.design/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico:
  - "Obsidian & Deep Charcoal Luminance Hierarchy"
  - "Elevação por Opacidade de Luz Branca (Additive Light Layering) e Zero Sombras Pretas"
  - "Contraste Cirúrgico & Prevenção de Halation Tipográfica (WCAG AAA/AA)"
  - "Estética B2B DevTools, High-Tech Cloud & AI Modernism (Linear/Raycast lineage)"
  - "Bordas Hairline Translúcidas de 1px (white/10 e white/5)"
  - "Tipografia Display Geométrica Técnica (Aeonik Pro Bold + Aeonik Fono Regular)"
  - "Atmosfera Cinematográfica com Fog Gradients (Bottom Void Overlays)"
  - "Cards Modulares em Proporção Estrita 3:2 com Micro-Iluminação de Borda no Hover"
densidade_informacao: "Media/Narrativa a Alta/Utilitaria"
impacto_visual: "Editorial/Sofisticado & Experimental/Imersivo"
custo_computacional: "Baixo a Moderado (Next.js SSR/RSC estático, imagens otimizadas WebP/AVIF via Supabase CDN, CSS utilitário Tailwind compilado, zero dependência pesada de Three.js no core)"
stack_frameworks:
  - "Next.js 15+ (App Router, React Server Components)"
  - "Tailwind CSS v3 / v4 com utilitários de opacidade dinâmica"
  - "Supabase (PostgreSQL + CDN Storage para screenshots de alta resolução)"
  - "Plausible Analytics (Telemetria leve privacy-first sem cookies)"
  - "Radix UI / Shadcn UI (Primitivos de interface acessíveis com foco em teclado)"
  - "Lucide Icons (Ícones lineares 1.5px / 2px)"
  - "Aeonik Pro Bold + Aeonik Fono Regular (Tipografia proprietária WOFF2)"
compatibilidade:
  fontes_ideais:
    - "Neo-Grotesques Técnicas: Aeonik Pro, Geist Sans, Inter, General Sans, Neue Haas Grotesk, PP Neue Montreal, SF Pro Text"
    - "Monospace de Alta Precisão: Aeonik Fono, Geist Mono, JetBrains Mono, Fragment Mono, IBM Plex Mono, SF Mono"
    - "Display Futuristas/Brutalistas: Uncut Sans, Clash Display, Syne, Monument Extended"
  paletas_ideais:
    - "Obsidian Core: #000000 (Pure Canvas), #080808 (Surface Base), #111111 (Card Body), #1A1A1A (Elevated Popover), #FFFFFF (Primary Ink), rgba(255,255,255,0.7) (Secondary Text), rgba(255,255,255,0.1) (Hairline Border)"
    - "Onyx Zinc (Linear Tone): #0B0C0E (Base), #12151A (Surface), #1C2028 (Hover Surface), #2E3642 (Subtle Border), #F1F3F5 (Text White)"
    - "Deep Space / DevTools Blue: #05070B (Base Navy Noir), #0D1117 (GitHub Dark Surface), #161B22 (Card Layer), #30363D (Border), #58A6FF (Electric Accent)"
    - "Neon Terminal (Phosphor Accent): #000000 (Base), #0D100D (Card), #00FF66 (Phosphor Green Accent), #22C55E (Emerald CTA)"
  combinacoes_recomendadas:
    - "Next.js App Router + Tailwind CSS (`bg-black text-white border-white/10 hover:border-white/20`)"
    - "Framer Motion com física overdamped (`stiffness: 400, damping: 30`) e fade-in de luminância"
    - "Shadcn UI adaptado com cores CSS personalizadas e `backdrop-blur-md`"
    - "Supabase Storage com imagens WebP e `blurDataURL` para transição imperceptível"
  conflitos_esteticos:
    - "Sombras escuras projetadas tradicionais (`box-shadow: 0 10px 25px rgba(0,0,0,0.5)`) que desaparecem no canvas preto"
    - "Superfícies cinza-claras desbotadas ou 'leitosas' (`#444444`) que quebram o contraste e geram aspecto amador"
    - "Cores saturadas primárias de light mode (ex: azul puro `#0000FF` ou vermelho puro `#FF0000`) sem calibração de luminância (provocam aberração cromática e vibração nos olhos)"
    - "Halation extrema: blocos imensos de texto corrido em `#FFFFFF` puro sobre `#000000` absoluto sem ajuste de peso ou atenuação para cinza `#E2E8F0` ou `#A1A1AA`"
    - "Bordas grossas coloridas sem transparência (`border: 2px solid cyan` ao invés de `border-white/10` ou gradiente de luz direcional)"
    - "Gradientes arco-íris saturados sem máscara de opacidade ou modo de mistura suave"
---

# Dark Mode Design — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
██████╗  █████╗ ██████╗ ██╗  ██╗    ██████╗ ███████╗███████╗██╗ ██████╗ ███╗   ██╗
██╔══██╗██╔══██╗██╔══██╗██║ ██╔╝    ██╔══██╗██╔════╝██╔════╝██║██╔════╝ ████╗  ██║
██║  ██║███████║██████╔╝█████╔╝     ██║  ██║█████╗  ███████╗██║██║  ███╗██╔██╗ ██║
██║  ██║██╔══██║██╔══██╗██╔═██╗     ██║  ██║██╔══╝  ╚════██║██║██║   ██║██║╚██╗██║
██████╔╝██║  ██║██║  ██║██║  ██╗    ██████╔╝███████╗███████║██║╚██████╔╝██║ ╚████║
╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝    ╚═════╝ ╚══════╝╚══════╝╚═╝ ╚═════╝ ╚═╝  ╚═══╝
               HANDPICKED WEBSITES FROM THE DARK SIDE — CURATED WITH LOVE
```

---

## 1. DNA Estético & Filosofia de Curadoria

Fundado pelo renomado designer de marcas e interfaces belga **Ruben Daems** (em parceria com a iniciativa criativa **Y5K LLC** — `https://y5k.design`), o **Dark Mode Design** (`https://www.dark.design/`) consolidou-se como o catálogo de maior prestígio e autoridade técnica na curadoria de experiências digitais imersivas em tema escuro. O projeto surge como resposta direta a um dos maiores dilemas da engenharia de interface contemporânea: o fato de que desenhar uma interface escura verdadeiramente elegante, acessível e funcional é exponencialmente mais complexo do que produzir seu equivalente em fundo claro.

Sob o lema central gravado em sua home — *"Handpicked websites from the dark side. From designers for designers. Curated with love"* —, a plataforma opera uma seleção impiedosa de websites em produção. Ela não agrega conceitos estáticos de Dribbble ou maquetes conceituais irrealistas; seu acervo foca em produtos digitais reais, SaaS de alta performance, plataformas de computação em nuvem, ferramentas para desenvolvedores (*DevTools*), estúdios de tecnologia criativa e portfólios que dominam a física da luz e a arquitetura tonal em monitores OLED e LCD modernos.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                   THE DARK MODE DESIGN CURATORIAL FRAMEWORK                            │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  [ ZERO CRUDE INVERSIONS ] ──► [ ADDITIVE LIGHT ELEVATION ] ──► [ REAL-WORLD CODE ONLY ]│
│   • Proibição de inversões      • Elevação por opacidade       • Produtos em produção  │
│     mecânicas Light->Dark       • Luz direcional e bordas      • SaaS, DevTools, AI &  │
│   • Controle estrito de halação • Hairlines translúcidas       • Estúdios criativos    │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  AESTHETIC PILLARS: Pure Obsidian • 1px White/10 Rules • Deep Zinc • High Restraint    │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 A Tríade da Luz Invertida: Por que o Dark Mode Não é Light Invertido

O diferencial que torna o acervo do Dark Mode Design único no ecossistema global é a compreensão visceral de que interfaces escuras obedecem a uma física óptica oposta à do mundo físico iluminado pelo sol:

1. **A Falência da Sombra Projetada (`The Shadow Paradox`)**:
   No design em fundo branco, a elevação é comunicada por dispersão de sombra escura (`box-shadow: 0 10px 30px rgba(0,0,0,0.08)`). No fundo preto ou carvão profundo (`#000000` ou `#050505`), sombras pretas tornam-se completamente invisíveis. O Dark Mode Design cataloga interfaces que substituíram o conceito de *sombra projetada* por **elevação por luminescência aditiva** (*Additive Luminance Elevation*): quanto mais próximo o elemento está dos olhos do usuário (maior o z-index), mais luz ele reflete e maior é a opacidade da superfície ou de suas bordas.

2. **O Combate Cirúrgico à Halatofia (`Halation Prevention`)**:
   Quando texto em branco puro (`#FFFFFF`) é colocado sobre fundo preto absoluto (`#000000`) com alto contraste, o olho humano sofre de *astigmatismo funcional temporário* ou halação (as letras parecem vibrar, sangrar ou emitir um clarão ofuscante, cansando o leitor em segundos). As referências selecionadas pelo Dark Mode Design demonstram como atenuar o corpo do texto para cinzas de alta fidelidade (`#D4D4D8`, `#A1A1AA` ou `rgba(255,255,255,0.7)`), reservando o branco puro de 100% estritamente para títulos monumentais e pontos nodais de interação.

3. **A Geometria das Bordas de Luz (`Hairline Luminescence`)**:
   Sem sombras pretas para separar planos, as referências de Dark Mode utilizam divisórias de `1px` ultra-refinadas com transparência de branco calculada matematicamente: `border-white/10` (10% de opacidade de branco sobre fundo escuro) para delimitação de módulos, e `border-white/20` para estados de foco ou hover interativo.

### 1.2 A Linhagem Visual: De Linear e Raycast aos Grandes Estúdios de Creative Dev

O acervo do Dark Mode Design funciona como o museu vivo da revolução estética inaugurada pela "Linear Aesthetic" e pelo modernismo do ecossistema Next.js/Vercel:

- **A Influência B2B SaaS de Alta Performance**: Produtos como Linear, Raycast, Supabase, Resend, Warp e Railway redefiniram a linguagem do software corporativo. O Dark Mode deixou de ser um recurso para jogos ou nichos "nerds" para se tornar o padrão visual supremo de sofisticação tecnológica e foco cognitivo.
- **Os Grandes Estúdios de Creative Development**: Estúdios de vanguarda como Basement Studio, TRIONN, Makepill e Griflan demonstram no acervo como combinar tipografia monumental (Aeonik, PP Neue Montreal, General Sans), renders 3D em WebGL monocromático e micro-animações táteis sobre bases escuras imersivas.
- **O Design Silencioso da Y5K LLC e Ruben Daems**: A própria interface do `dark.design` reflete a visão de Ruben Daems: estética brutalista limpa, sem poluição de popups ou elementos decorativos desnecessários, tipografia display em corte geométrico (`Aeonik Pro Bold`) e dados técnicos em proporção monospaçada (`Aeonik Fono`).

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

O Dark Mode Design é a **Referência Primária de Direção de Arte** para projetos que exigem transmitir autoridade técnica, precisão matemática, elegância cinematográfica e imersão profunda:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        CORE APPLICATION SCENARIOS                                      │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  [ DEVELOPER TOOLS & CLOUD ]  ──►  [ AI PLATFORMS & AGENTS ] ──► [ CREATIVE STUDIOS ]  │
│   • IDEs, Terminais & CLI          • Interfaces de LLMs          • Portfólios de Agência│
│   • Infraestrutura de Nuvem        • Automação de Agentes        • Showcases de WebGL   │
│   • Dashboards de Engenharia       • Canvas de IA Generativa     • Estúdios de Branding │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  [ WEB3 & CRYPTO PROTOCOLS ] ──►  [ AUDIO/VIDEO PRO APPS ]   ──► [ LUXURY HARDWARE ]   │
│   • DePIN, DeFi Terminals          • DAWs & NLEs Web             • Áudio de Alta Fide-  │
│   • Smart Contract Analytics       • Editores de Motion & VFX    • lidade & Gadgets     │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 2.1 Posicionamento de Marca & Impacto Psicológico

- **Autoridade e Maestria Técnica**: O preto e o carvão comunicam imediatamente que o software é voltado para profissionais experientes que valorizam eficiência, velocidade e silêncio visual sobre decorações coloridas superficiais.
- **Redução de Fadiga em Sessões Longas**: Para desenvolvedores, designers e traders que passam de 8 a 14 horas diárias diante de múltiplos monitores, a paleta dark com superfícies de baixa emissão de lúmens preserva o conforto visual.
- **Destaque Cromático Máximo para Conteúdo Rico**: Em interfaces de edição de vídeo, áudio ou render 3D, a casca escura desaparece no ambiente físico, permitindo que a mídia em foco brilhe com contraste nativo sem interferência da carcaça do software.

### 2.2 A Regra 60-30-10 Aplicada ao Dark Mode de Alta Fidelidade

Em uma interface inspirada pela curadoria do Dark Mode Design, a harmonia visual é governada estritamente pela proporção áurea de cores:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                   THE 60-30-10 DARK MODE COLOR DISTRIBUTION                            │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  60% — THE OBSIDIAN CANVAS (Fundo Primário)                                            │
│  • #000000 (Pure OLED Black) ou #080808 / #0A0A0A (Deep Charcoal Base)                 │
│  • Função: Absorve a luz ambiente, elimina ruído e define o espaço negativo ativo.     │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  30% — STRUCTURAL SURFACES & MONOCHROME TYPE (Superfícies & Estrutura)                 │
│  • Superfícies elevadas: #111111, #161616, #1C1C1C ou rgba(255,255,255,0.03 - 0.06)    │
│  • Hairlines de 1px: rgba(255,255,255,0.1) e rgba(255,255,255,0.05)                   │
│  • Tipografia: #FFFFFF (Headings 100%), rgba(255,255,255,0.7) (Labels & Body)          │
│  • Função: Desenha a arquitetura do grid e organiza os blocos de dados.                │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  10% — FOCAL LUMINESCENCE & ACCENT SPARKS (Acento Cirúrgico)                           │
│  • Branco puro em alto brilho (#FFFFFF em botões invertidos sólidos com texto #000000) │
│  • Ou um único acento cromático neon (ex: Verde Terminal #00FF66, Ciano Dev #38BDF8)   │
│  • Função: Conduz o olhar para a ação primária (CTA), status ativo ou métrica crítica. │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

Nem todo produto tolera a solenidade do tema escuro. O uso inadequado resulta em taxas de rejeição desastrosas, ilegibilidade e quebra de conversão:

### 3.1 Incompatibilidades Setoriais

- ⚠️ **E-commerce de Produtos Naturais, Alimentos Orgânicos e Moda Diurna**: Marcas que dependem de frescor, pureza solar, luz natural e tons pastéis (ex: cosméticos orgânicos, padarias artesanais, vestuário infantil) geram sensação de toxicidade, frieza ou peso sepulcral quando forçadas a um dark mode.
- ⚠️ **Documentação Jurídica Extensa e Artigos Longform Diurnos**: Leitura de blocos maciços de texto corrido por mais de 30 minutos em ambientes externos ou escritórios hiper-iluminados com luz solar direta causa fadiga ocular severa em temas escuros. Nesses cenários, papéis quentes off-white (`#FBFBFA` ou `#F4F4F0`) são superiores.
- ⚠️ **Aplicações para Ambientes Externos Sob Sol Intenso**: Terminais de logística de campo, aplicativos agrícolas ou apps para motoristas sob incidência solar direta sofrem com reflexos em telas pretas.

### 3.2 Os Seis Pecados Capitais na Imitação do Dark Mode

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        THE 6 FATAL DARK MODE ANTI-PATTERNS                             │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  1. THE GHOST SHADOW          ──► Aplicar sombras pretas (rgba(0,0,0,0.5)) em telas    │
│                                   pretas. Resultado: invisibilidade e desperdício de GPU│
├────────────────────────────────────────────────────────────────────────────────────────┤
│  2. BLINDING HALATION         ──► Corpo de texto longo em #FFFFFF 100% sobre #000000.  │
│                                   Resultado: letras parecem vibrar e cegam o leitor.   │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  3. CHROMATIC VIBRATION       ──► Usar cores de Light Mode saturadas (ex: Azul #0000FF │
│                                   ou Vermelho #FF0000) no escuro. Causa aberração crom. │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  4. MILKY WASHED-OUT GRAYS    ──► Cinzas desbotados e opacos (#3A3A3C sem contraste).   │
│                                   Resultado: aparência de poeira ou tela LCD barata.   │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  5. FLAT LACK OF Z-ELEVATION  ──► Manter cards e modais na mesma cor do fundo sem luz  │
│                                   nem borda. O usuário perde a noção de profundidade.  │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  6. NEON OVERDOSE             ──► Bordas e botões brilhando em 5 cores fluorescentes.  │
│                                   Resultado: estética de cassino barato ou NFT spam.   │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

O exame aprofundado da arquitetura visual de `dark.design` revela uma engenharia milimétrica de proporção, tipografia e luz:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                   DARK.DESIGN INTERFACE ARCHITECTURE BREAKDOWN                         │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ [STICKY BLUR NAVBAR] Max-w: 1600px | bg-black/80 | backdrop-blur-md | border-b white/10│
├────────────────────────────────────────────────────────────────────────────────────────┤
│ [HERO UNIT]                                                                            │
│  • Left: H1 uppercase font-black Aeonik Pro (3xl -> 6xl)                               │
│    "HANDPICKED WEBSITES FROM THE DARK SIDE"                                            │
│  • Right: Integrated Sponsor Card (Billow / Supabase / Jitter)                         │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ [SHOWCASE GRID] grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 3xl:grid-cols-5│
│  • Cards: aspect-[3/2] | border-white/10 | bg-white/[0.03] | rounded-[8px]             │
│  • Hover: border-white/20 | scale-[1.01] | smooth luminance transition                │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ [ATMOSPHERIC VOID OVERLAY] fixed bottom-0 h-48 bg-gradient-to-t from-black to-transpar.│
├────────────────────────────────────────────────────────────────────────────────────────┤
│ [OBSIDIAN FOOTER] border-t white/10 | py-8 pb-48 | text-white/30 & text-white/50       │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo

1. **Grid Responsivo de 1 a 5 Colunas**:
   A galeria emprega um sistema de layout expansivo que aproveita viewports ultra-largos sem deformação:
   - Mobile (`< 640px`): `grid-cols-1` com espaçamento `gap-4` (16px).
   - Tablet (`sm: 640px`): `grid-cols-2`.
   - Desktop Standard (`lg: 1024px`): `grid-cols-3`.
   - Desktop Widescreen (`xl: 1280px`): `grid-cols-4`.
   - Telas Ultra-Wide (`3xl: 1920px+`): `grid-cols-5`.
2. **Proporção Estrita 3:2 dos Cards de Exibição**:
   Ao contrário de galerias com proporções 16:9 (que comprimem o conteúdo do site) ou 4:3 (que alongam excessivamente o scroll vertical), o Dark Mode Design padroniza todos os screenshots na proporção clássica de fotografia **3:2** (`aspect-[3/2]`). Isso oferece a área de visualização ideal para capturas de dobra superior (*above the fold*) de páginas web.
3. **Contenção Máxima de 1600px**:
   O container central adota `max-w-[1600px]` com padding horizontal fluido `px-4`, garantindo que o conteúdo respire sem tocar as bordas físicas do monitor em monitores ultrawide.
4. **Vazio Atmosférico Inferior (`Bottom Fog Fade`)**:
   Uma barra translúcida fixa de 192px (`h-48`) no rodapé com gradiente `from-black to-transparent` (`pointer-events-none`) cria a sensação cinematográfica de que a lista de sites emerge e se dissolve na escuridão do espaço infinito.

### 4.2 Sistemas de Cores, Superfícies & Materiais

O ecossistema tonal é calibrado com precisão cirúrgica:

| Token / Elemento | Valor Hex / RGBA | Classe Tailwind | Função Semântica |
| :--- | :--- | :--- | :--- |
| **Canvas Base** | `#000000` | `bg-black` | Fundo principal da tela, absorção total |
| **Surface Alpha 1** | `rgba(255, 255, 255, 0.03)` | `bg-white/[0.03]` | Superfície de repouso dos cards |
| **Surface Alpha 2** | `rgba(255, 255, 255, 0.05)` | `bg-white/5` | Barras de skeleton loader e elementos neutros |
| **Surface Hover** | `rgba(255, 255, 255, 0.08)` | `hover:bg-white/10` | Realce tátil de botões e links |
| **Hairline Border** | `rgba(255, 255, 255, 0.10)` | `border-white/10` | Divisórias estruturais e contornos de cards |
| **Interactive Border**| `rgba(255, 255, 255, 0.20)` | `border-white/20` | Borda de botões e hover de cards |
| **Focus Border** | `rgba(255, 255, 255, 0.40)` | `focus:border-white/40`| Estado ativo e anel de acessibilidade |
| **Text Primary (Ink)**| `#FFFFFF` | `text-white` | Títulos h1, botões sólidos e branding |
| **Text Secondary** | `rgba(255, 255, 255, 0.70)` | `text-white/70` | Navegação, subtítulos e labels ativos |
| **Text Muted** | `rgba(255, 255, 255, 0.50)` | `text-white/50` | Links de rodapé e categorias secundárias |
| **Text Faint** | `rgba(255, 255, 255, 0.30)` | `text-white/30` | Copyright, metadados de sistema e timestamps |
| **Action Solid** | `#FFFFFF` (texto `#000000`)| `bg-white text-black` | Botão primário com alto contraste ("Create Account")|

### 4.3 Tipografia: O Equilíbrio entre Aeonik Pro e Aeonik Fono

A assinatura tipográfica do Dark Mode Design reside no pareamento entre a geometria suíça contemporânea e a precisão da engenharia:

- **Aeonik Pro (Bold)**: Tipografia display sem serifa, de traços afiados, proporções geométricas rigorosas e aberturas amplas. Usada em caixa alta monumentais (`text-3xl sm:text-5xl lg:text-6xl font-black uppercase leading-none tracking-tight`). Constrói uma presença imponente que ancora a tela escura.
- **Aeonik Fono (Regular)**: Variação monospaçada técnica de proporções mecânicas consistentes. Empregada para badges numéricas, contadores de cliques, metadados de autoria e rótulos de sistema.
- **Substitutos de Código Aberto (Alternativas de Produção)**:
  - Para Aeonik Pro: **Geist Sans**, **General Sans** ou **Inter Display**.
  - Para Aeonik Fono: **Geist Mono**, **JetBrains Mono** ou **Fragment Mono**.

---

### 4.4 Catálogo de 10 Arquétipos & Componentes Notáveis

Abaixo estão os 10 padrões de componentes extraídos diretamente da produção de `dark.design`:

#### 1. The Obsidian Sticky Navbar with Frosted Blur
- **Anatomia**: Barra de navegação fixada no topo (`sticky top-0 z-50`), altura compacta de 52px, divisória inferior `border-b border-white/10`, superfície em `bg-black/80 backdrop-blur-md`.
- **Comportamento**: À medida que os cards sobem no scroll, eles passam por trás da barra com desfoque gaussiano suave, mantendo legibilidade total dos links e do logotipo.
- **Onde Encaixar**: Header global de qualquer aplicação dark modernista.

#### 2. The Brutalist Low-Light Display Hero
- **Anatomia**: Título monumental h1 em duas linhas com quebra controlada (`text-balance text-3xl font-black uppercase leading-none tracking-tight text-white sm:text-5xl lg:text-6xl`).
- **Gatilho**: Transmite imediatamente o manifesto do produto ("Handpicked websites from the dark side") sem ilustrações ou fotos competindo por atenção.
- **Onde Encaixar**: Dobra inicial de landing pages, galerias e plataformas SaaS orientadas a desenvolvedores.

#### 3. The Integrated Monochrome Sponsor Unit
- **Anatomia**: Slot comercial contextual de 280x80px embutido no lado direito do Hero, alinhado à grelha. Borda `border-white/10`, cantos `rounded-[8px]`, imagem com tratamento monocromático ou de baixa saturação para não romper a estética noturna do produto.
- **Onde Encaixar**: Monetização não-invasiva em diretórios e ferramentas gratuitas para desenvolvedores.

#### 4. The 3:2 Aspect Framed Showcase Card
- **Anatomia**: Card modular com proporção fixa `aspect-[3/2]`, contorno em `1px solid rgba(255,255,255,0.1)`, cantos arredondados contidos `rounded-[8px]`, fundo `bg-white/[0.03]`.
- **Gatilho de Interação**: No hover, a borda faz fade suave para `border-white/20`, a imagem executa uma sutil elevação e uma camada de metadados exibe o título da plataforma e a contagem de cliques.
- **Onde Encaixar**: Grids de portfólio, catálogo de templates, vitrines de produtos e listas de projetos.

#### 5. The Luminance Pulse Skeleton Loader
- **Anatomia**: Esqueleto de carregamento com `animate-pulse` construído com retângulos em `bg-white/5` sobre superfícies em `bg-white/[0.03]`.
- **Por que é Vital**: Em temas escuros, loaders cinza-claros convencionais causam clarões ofuscantes na tela. O loader de luminância mantém o nível de cinza abaixo de 5% de luz, prevenindo qualquer choque no usuário.
- **Onde Encaixar**: Estados de carregamento de páginas Next.js com Suspense boundaries.

#### 6. The Atmospheric Bottom Void Gradient
- **Anatomia**: Camada fixa na base da viewport (`pointer-events-none fixed bottom-0 left-0 right-0 z-10 h-48 bg-gradient-to-t from-black to-transparent`).
- **Efeito Visual**: Cria um desvanecimento atmosférico misterioso, onde os cards inferiores parecem emergir da escuridão do abismo conforme o usuário realiza o scroll.
- **Onde Encaixar**: Feeds infinitos, galerias de imagens e dashboards imersivos.

#### 7. The Dark Micro-Tag Pill
- **Anatomia**: Pílula ultra-compacta com cantos totalmente arredondados (`rounded-full`), fundo translúcido `bg-white/10`, texto em `text-white/60 text-[10px] font-semibold uppercase tracking-wider px-1.5 py-0.5`.
- **Variações**: Utilizada para marcar itens gratuitos ("FREE"), categorias ("AI", "AGENCY", "DEVTOOLS") ou status ("NEW").
- **Onde Encaixar**: Emblemas de status em navbars, tags de cards e tabelas de preços.

#### 8. The High-Contrast Action Inversion Button
- **Anatomia**: Botão compacto com altura contida de 28px (`h-7`) a 32px (`h-8`), tipografia de 12px a 14px com peso médio, bordas arredondadas suaves (`rounded-[10px]`).
- **Contraste de Ação**: Fundo branco puro `#FFFFFF` com texto preto absoluto `#000000` (`bg-white text-black hover:bg-white/90`). Por estar em uma interface 90% escura, esse elemento atrai o foco visual com força magnética instantânea sem precisar de cores neon gritantes.
- **Onde Encaixar**: Call to Action primário, "Create Account", "Submit Site" ou "Deploy Now".

#### 9. The Category Taxonomy Matrix
- **Anatomia**: Sistema de filtragem horizontal ou em menu suspenso composto por 8 pilares ontológicos estritos: `AI`, `Agency`, `Culture`, `Education`, `Hardware`, `Personal`, `Software` e `Web3`.
- **Onde Encaixar**: Filtros de diretórios técnicos e taxonomias de blog.

#### 10. The Minimalist Obsidian Footer
- **Anatomia**: Rodapé de fundo preto puro com divisória superior `border-t border-white/10`, tipografia atenuada `text-white/30` para créditos autorais e links em `text-white/50 hover:text-white transition-colors`. Em dispositivos móveis, os links se transformam em linhas horizontais expansíveis com ícones de chevron sutis (`lucide-chevron-right text-[#666666]`).
- **Onde Encaixar**: Encerramento de páginas SaaS e portfólios institucionais.

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Stack Tecnológica Mapeada

A engenharia de `dark.design` é um exemplo canônico de modernidade no ecossistema JavaScript/React:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        DARK.DESIGN PRODUCTION STACK                                    │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ • Framework: Next.js 15+ (App Router, React Server Components com Turbopack)           │
│ • Estilização: Tailwind CSS (Configuração dark estrita, utilitários arbitrários)       │
│ • Infraestrutura de Mídia: Supabase Storage CDN (Screenshots WebP com cache global)    │
│ • Banco de Dados: Supabase PostgreSQL (Tabelas de Sites, Categorias, Sponsors)        │
│ • Telemetria: Plausible Analytics (Script assíncrono cookieless pa-z5dU6Z6zQ3x8wqQ1)   │
│ • Ícones: Lucide React (Ícones lineares com espessura 1.5px e 2px)                     │
│ • UI Primitives: Radix UI / Shadcn UI Button Group e Toaster                           │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 5.2 Física de Movimento & Transições

Interfaces dark exigem animações **rápidas, amortecidas e táteis**. Qualquer delay excessivo ou oscilação saltitante ("bouncy") parece infantil e quebra a gravidade do design:

- **Transições de Luminância (Hover em Cards e Botões)**:
  ```css
  transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
  ```
- **Física de Spring para Framer Motion**:
  ```ts
  const darkSpringTransition = {
    type: "spring",
    stiffness: 400,
    damping: 30,
    mass: 0.8
  };
  ```
- **Abertura de Menus Mobile e Modais**:
  Curva `cubic-bezier(0.16, 1, 0.3, 1)` com duração de `240ms` e deslocamento vertical reduzido (de `translate-y-2` para `translate-y-0`) para evitar sensação de lentidão.

---

### 5.3 Tokens CSS Globais (Design Tokens para Obsidian Dark Mode)

```css
:root {
  /* ==========================================================================
     OBSIDIAN DARK ENGINE DESIGN TOKENS (Baseado em dark.design)
     ========================================================================== */
  
  /* Canvas & Superfícies */
  --dark-canvas-base: #000000;
  --dark-canvas-surface: #080808;
  --dark-card-idle: rgba(255, 255, 255, 0.03);
  --dark-card-hover: rgba(255, 255, 255, 0.06);
  --dark-card-elevated: #111111;
  --dark-popover-base: #141414;

  /* Bordas de Luz Aditiva */
  --dark-border-subtle: rgba(255, 255, 255, 0.08);
  --dark-border-default: rgba(255, 255, 255, 0.12);
  --dark-border-hover: rgba(255, 255, 255, 0.22);
  --dark-border-focus: rgba(255, 255, 255, 0.45);

  /* Tipografia & Hierarquia de Brilho */
  --dark-text-primary: #FFFFFF;
  --dark-text-secondary: rgba(255, 255, 255, 0.70);
  --dark-text-muted: rgba(255, 255, 255, 0.50);
  --dark-text-faint: rgba(255, 255, 255, 0.30);

  /* Acentos de Ação Invertida */
  --dark-action-bg: #FFFFFF;
  --dark-action-text: #000000;
  --dark-action-hover: #EAEAEA;

  /* Geometria */
  --dark-radius-card: 8px;
  --dark-radius-pill: 9999px;
  --dark-radius-button: 10px;

  /* Timing & Física */
  --dark-ease-snappy: cubic-bezier(0.16, 1, 0.3, 1);
  --dark-duration-fast: 180ms;
}
```

---

### 5.4 Componente React Completo: Arquitetura da Galeria Dark Mode

Abaixo está o componente funcional em React, Tailwind CSS e Lucide Icons, reproduzindo com fidelidade a arquitetura de layout, o card aspect 3:2, a elevação por luz, a navbar com blur e o fog atmosférico de `dark.design`:

```tsx
import React, { useState } from "react";
import { ExternalLink, Sparkles, ChevronRight, Menu, X } from "lucide-react";

// Tipagem de dados extraída da estrutura de produção do dark.design
interface DarkSiteItem {
  id: string;
  title: string;
  url: string;
  slug: string;
  description: string;
  screenshotUrl: string;
  category: "AI" | "Agency" | "Culture" | "Education" | "Hardware" | "Personal" | "Software" | "Web3";
  clicks: number;
}

const SAMPLE_SITES: DarkSiteItem[] = [
  {
    id: "site-1",
    title: "Basement",
    url: "https://basement.studio/",
    slug: "basement",
    description: "Digital studio crafting bold brands, 3D experiences, and high-performance WebGL platforms.",
    screenshotUrl: "https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?auto=format&fit=crop&w=800&q=80",
    category: "Agency",
    clicks: 1999
  },
  {
    id: "site-2",
    title: "Railway",
    url: "https://railway.com/",
    slug: "railway",
    description: "Full-stack cloud infrastructure designed to instantly provision, build, and scale code.",
    screenshotUrl: "https://images.unsplash.com/photo-1620641788421-7a1c342ea42e?auto=format&fit=crop&w=800&q=80",
    category: "Software",
    clicks: 1845
  },
  {
    id: "site-3",
    title: "TRIONN",
    url: "https://trionn.com/",
    slug: "trionn",
    description: "AI-powered creative agency delivering high-impact brand identities and dark-mode digital craft.",
    screenshotUrl: "https://images.unsplash.com/photo-1550745165-9bc0b252726f?auto=format&fit=crop&w=800&q=80",
    category: "Agency",
    clicks: 1420
  },
  {
    id: "site-4",
    title: "xAI",
    url: "https://x.ai/",
    slug: "xai",
    description: "Building Grok and frontier artificial intelligence models to accelerate human scientific discovery.",
    screenshotUrl: "https://images.unsplash.com/photo-1634017839464-5c339ebe3cb4?auto=format&fit=crop&w=800&q=80",
    category: "AI",
    clicks: 2890
  },
  {
    id: "site-5",
    title: "OXI Instruments",
    url: "https://oxiinstruments.com/",
    slug: "oxi",
    description: "Innovative boutique hardware sequencers and audio performance synthesizers from Spain.",
    screenshotUrl: "https://images.unsplash.com/photo-1598488035139-bdbb2231ce04?auto=format&fit=crop&w=800&q=80",
    category: "Hardware",
    clicks: 980
  },
  {
    id: "site-6",
    title: "Linear",
    url: "https://linear.app/",
    slug: "linear",
    description: "The purpose-built issue tracker for modern software teams with lightning keyboard shortcuts.",
    screenshotUrl: "https://images.unsplash.com/photo-1507238691740-187a5b1d37b8?auto=format&fit=crop&w=800&q=80",
    category: "Software",
    clicks: 3420
  }
];

export const DarkModeDesignGallery: React.FC = () => {
  const [selectedCategory, setSelectedCategory] = useState<string>("All");
  const [mobileMenuOpen, setMobileMenuOpen] = useState<boolean>(false);

  const categories = ["All", "AI", "Agency", "Software", "Hardware", "Web3"];

  const filteredSites = selectedCategory === "All"
    ? SAMPLE_SITES
    : SAMPLE_SITES.filter(s => s.category === selectedCategory);

  return (
    <div className="min-h-screen bg-black text-white selection:bg-white selection:text-black font-sans antialiased">
      {/* 1. STICKY FROSTED NAVBAR */}
      <nav className="sticky top-0 z-50 border-b border-white/10 bg-black/80 backdrop-blur-md">
        <div className="mx-auto flex max-w-[1600px] items-center justify-between px-4 py-3">
          {/* Logo & Navigation Links */}
          <div className="flex items-center gap-6">
            <a href="/" className="flex items-center gap-2 group">
              <div className="h-6 w-6 rounded bg-white text-black font-black flex items-center justify-center text-xs tracking-tighter">
                D
              </div>
              <span className="font-extrabold uppercase tracking-tight text-lg text-white">
                Dark
              </span>
            </a>

            <div className="hidden md:flex items-center gap-1 text-sm">
              <button 
                onClick={() => setSelectedCategory("All")}
                className={`px-3 py-1 rounded-md text-xs font-medium transition-colors ${
                  selectedCategory === "All" ? "text-white bg-white/10" : "text-white/70 hover:text-white"
                }`}
              >
                Sites
              </button>
              <a 
                href="#templates" 
                className="flex items-center gap-1.5 px-3 py-1 rounded-md text-xs font-medium text-white/70 hover:text-white transition-colors"
              >
                Templates
                <span className="rounded-full bg-white/10 px-1.5 py-0.5 text-[9px] font-semibold uppercase tracking-wider text-white/70">
                  Free
                </span>
              </a>
              <a 
                href="#sponsor" 
                className="px-3 py-1 rounded-md text-xs font-medium text-white/70 hover:text-white transition-colors"
              >
                Sponsor
              </a>
            </div>
          </div>

          {/* Action Buttons */}
          <div className="hidden md:flex items-center gap-2">
            <button className="h-7 px-3 rounded-[10px] border border-white/20 bg-transparent text-xs font-medium text-white hover:bg-white/10 transition-colors">
              Submit
            </button>
            <button className="h-7 px-3 rounded-[10px] text-xs font-medium text-white/70 hover:text-white hover:bg-white/10 transition-colors">
              Sign in
            </button>
            <button className="h-7 px-3 rounded-[10px] bg-white text-black text-xs font-semibold hover:bg-white/90 transition-all shadow-[0_0_15px_rgba(255,255,255,0.15)]">
              Create Account
            </button>
          </div>

          {/* Mobile Menu Toggle */}
          <button 
            onClick={() => setMobileMenuOpen(!mobileMenuOpen)} 
            className="md:hidden p-1.5 text-white/70 hover:text-white"
            aria-label="Toggle menu"
          >
            {mobileMenuOpen ? <X size={20} /> : <Menu size={20} />}
          </button>
        </div>

        {/* Mobile Dropdown Menu */}
        {mobileMenuOpen && (
          <div className="md:hidden border-b border-white/10 bg-black px-4 py-4 space-y-3">
            <div className="flex flex-col gap-2">
              {categories.map(cat => (
                <button
                  key={cat}
                  onClick={() => { setSelectedCategory(cat); setMobileMenuOpen(false); }}
                  className="text-left text-sm py-1.5 text-white/70 hover:text-white"
                >
                  {cat}
                </button>
              ))}
            </div>
            <div className="pt-3 border-t border-white/10 flex flex-col gap-2">
              <button className="w-full h-8 rounded-lg border border-white/20 text-xs font-medium text-white">
                Submit Site
              </button>
              <button className="w-full h-8 rounded-lg bg-white text-black text-xs font-semibold">
                Create Account
              </button>
            </div>
          </div>
        )}
      </nav>

      {/* 2. MAIN SHOWCASE CONTENT */}
      <main className="mx-auto max-w-[1600px] px-4 pt-10 pb-28">
        {/* HERO SECTION WITH BRUTALIST DISPLAY TYPE */}
        <section className="mb-10 flex flex-col md:flex-row md:items-end md:justify-between gap-6">
          <div className="space-y-4 max-w-2xl">
            <h1 className="text-3xl sm:text-5xl lg:text-6xl font-black uppercase leading-none tracking-tight text-white text-balance">
              Handpicked websites <br />
              <span className="text-white/40">from the dark side</span>
            </h1>
            <p className="text-sm text-white/60 font-mono flex items-center gap-2">
              <Sparkles size={14} className="text-white/80" />
              Excellence in low-light digital craft & additive light interfaces.
            </p>
          </div>

          {/* INTEGRATED SPONSOR BANNER UNIT */}
          <div className="w-full md:w-72 p-3 rounded-[8px] border border-white/10 bg-white/[0.02] hover:border-white/20 transition-all flex items-center gap-3">
            <div className="h-10 w-10 rounded bg-white/10 flex items-center justify-center font-mono text-[10px] text-white/60">
              AD
            </div>
            <div className="flex-1 min-w-0">
              <div className="flex items-center gap-1.5">
                <span className="text-xs font-bold text-white truncate">Billow Studio</span>
                <span className="text-[9px] uppercase tracking-wider px-1 bg-white/10 rounded text-white/60">Sponsor</span>
              </div>
              <p className="text-[11px] text-white/50 truncate">Modern WebGL design systems.</p>
            </div>
          </div>
        </section>

        {/* CATEGORY FILTER PILL MATRIX */}
        <div className="mb-8 flex items-center gap-2 overflow-x-auto pb-2 scrollbar-none">
          {categories.map((cat) => (
            <button
              key={cat}
              onClick={() => setSelectedCategory(cat)}
              className={`px-3 py-1 rounded-full text-xs font-mono uppercase tracking-wider transition-all ${
                selectedCategory === cat
                  ? "bg-white text-black font-bold shadow-[0_0_12px_rgba(255,255,255,0.2)]"
                  : "bg-white/[0.04] text-white/60 border border-white/5 hover:border-white/20 hover:text-white"
              }`}
            >
              {cat}
            </button>
          ))}
        </div>

        {/* 3. SHOWCASE GRID (3:2 ASPECT RATIO CARDS) */}
        <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 3xl:grid-cols-5 gap-4">
          {filteredSites.map((site) => (
            <article
              key={site.id}
              className="group relative flex flex-col rounded-[8px] border border-white/10 bg-white/[0.02] overflow-hidden transition-all duration-200 ease-out hover:border-white/25 hover:bg-white/[0.04]"
            >
              {/* Screenshot Media Container (Strict 3:2 Ratio) */}
              <div className="relative aspect-[3/2] w-full overflow-hidden bg-black/60">
                <img
                  src={site.screenshotUrl}
                  alt={site.title}
                  loading="lazy"
                  className="h-full w-full object-cover transition-transform duration-500 ease-out group-hover:scale-[1.03]"
                />
                <div className="absolute inset-0 bg-gradient-to-t from-black/80 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-200 flex items-end p-3">
                  <a
                    href={site.url}
                    target="_blank"
                    rel="noopener noreferrer"
                    className="inline-flex items-center gap-1.5 px-2.5 py-1 rounded bg-white text-black text-xs font-medium shadow-md hover:bg-white/90 transition-colors"
                  >
                    Visit Site <ExternalLink size={12} />
                  </a>
                </div>
              </div>

              {/* Card Metadata & Description */}
              <div className="p-3 flex flex-col justify-between flex-1 gap-2">
                <div>
                  <div className="flex items-center justify-between gap-2">
                    <h2 className="font-bold text-sm text-white group-hover:text-white transition-colors truncate">
                      {site.title}
                    </h2>
                    <span className="font-mono text-[10px] uppercase tracking-wider text-white/50 px-1.5 py-0.5 rounded bg-white/[0.05] border border-white/5">
                      {site.category}
                    </span>
                  </div>
                  <p className="mt-1 text-xs text-white/60 line-clamp-2 leading-relaxed">
                    {site.description}
                  </p>
                </div>

                <div className="pt-2 border-t border-white/5 flex items-center justify-between text-[11px] text-white/40 font-mono">
                  <span>{site.clicks.toLocaleString()} clicks</span>
                  <span className="text-white/20 group-hover:text-white/60 transition-colors">inspect →</span>
                </div>
              </div>
            </article>
          ))}
        </div>
      </main>

      {/* 4. ATMOSPHERIC BOTTOM VOID GRADIENT */}
      <div 
        aria-hidden="true" 
        className="pointer-events-none fixed bottom-0 left-0 right-0 z-20 h-44 bg-gradient-to-t from-black via-black/80 to-transparent" 
      />

      {/* 5. MINIMALIST OBSIDIAN FOOTER */}
      <footer className="relative z-30 border-t border-white/10 bg-black">
        <div className="mx-auto flex max-w-[1600px] flex-col sm:flex-row sm:items-center sm:justify-between px-4 py-8 pb-32 gap-6">
          <div className="space-y-1">
            <div className="flex items-center gap-2">
              <div className="h-4 w-4 rounded bg-white text-black font-black flex items-center justify-center text-[10px]">
                D
              </div>
              <span className="font-bold text-sm text-white">Dark Mode Design</span>
            </div>
            <p className="text-xs text-white/30">
              © 2026 Dark – Handcrafted by Ruben Daems. Product by Y5K LLC.
            </p>
          </div>

          <nav className="flex flex-wrap items-center gap-6 text-xs text-white/50 font-mono">
            <a href="#sites" className="hover:text-white transition-colors">Sites</a>
            <a href="#templates" className="hover:text-white transition-colors">Templates</a>
            <a href="#sponsor" className="hover:text-white transition-colors">Sponsor</a>
            <a href="#submit" className="hover:text-white transition-colors">Submit</a>
            <a href="#privacy" className="hover:text-white transition-colors">Privacy</a>
          </nav>
        </div>
      </footer>
    </div>
  );
};

export default DarkModeDesignGallery;
```

---

### 5.5 Como a IA Deve Pesquisar ao Vivo no Site (Live Search & URL Patterns)

Quando um agente inteligente ou subagente precisar consultar referências em tempo real no `dark.design` para inspirar um projeto em andamento, as seguintes estruturas de rota e parâmetros devem ser utilizados:

- **Catálogo Geral de Sites**:
  `https://www.dark.design/`
- **Filtros Diretos por Categoria**:
  - Inteligência Artificial e Agentes: `https://www.dark.design/?category=ai`
  - Agências & Estúdios Criativos: `https://www.dark.design/?category=agency`
  - Ferramentas de Software & SaaS: `https://www.dark.design/?category=software`
  - Infraestrutura & Hardware: `https://www.dark.design/?category=hardware`
  - Projetos Pessoais & Portfólios: `https://www.dark.design/?category=personal`
  - Web3, DePIN e Cripto: `https://www.dark.design/?category=web3`
  - Cultura, Editorial & Mídia: `https://www.dark.design/?category=culture`
  - Educação & Tutoriais: `https://www.dark.design/?category=education`
- **Catálogo de Templates Gratuitos**:
  `https://www.dark.design/templates`
- **Detalhes Específicos de um Site Indexado**:
  `https://www.dark.design/sites/[slug]` (ex: `https://www.dark.design/sites/basement-1786786858853`)
- **Padrão de API / Supabase Assets**:
  Imagens de alta resolução são servidas a partir do endpoint de CDN da Supabase:
  `https://sidhvpjhuucqcehkevrl.supabase.co/storage/v1/object/public/screenshots/[filename].webp`

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar a direção estética **Dark Mode Design** para um novo produto de software, os agentes devem injetar compulsoriamente os seguintes parâmetros na blueprint de design:

```markdown
### DIRETRIZES DE DIREÇÃO DE ARTE: OBSIDIAN DARK ENGINE (#128)

1. ARQUITETURA TONAL & LUZ ADITIVA:
   - Canvas Base: #000000 absoluto para fundo global (OLED Pure).
   - Superfície de Cartões / Paineis: rgba(255, 255, 255, 0.03) a 0.06. Nunca use cinzas chapados (#333333).
   - Elevação Z-Index: Quanto mais alto o elemento na camada (modal, popover, dropdown), maior a luminância da superfície (#141414 -> #1A1A1A).
   - Zero Sombras Pretas: É estritamente proibido o uso de `box-shadow` escura em fundos escuros. Substitua por bordas hairline de 1px com transparência de branco (rgba(255, 255, 255, 0.1)).

2. COMBATE À HALAÇÃO & HIERARQUIA TIPOGRÁFICA:
   - Headings Monumentais (H1/H2): #FFFFFF puro (100% lúmens), tracking negativo (-0.02em a -0.04em), pesos Bold ou Black.
   - Textos de Apoio / Subtítulos: rgba(255, 255, 255, 0.70) (#B3B3B3 aproximado).
   - Texto Corrido Longo (Body Text): #D4D4D8 (Zinc-300) para eliminar ofuscamento e fadiga visual.
   - Metadados, Badges e Legendas: rgba(255, 255, 255, 0.40) em tipografia monospace (Geist Mono ou JetBrains Mono).

3. PROPORÇÃO & COMPOSIÇÃO DE CARDS:
   - Use proporção 3:2 (aspect-[3/2]) para exibição de capturas de tela e interfaces.
   - Cantos arredondados contidos: `rounded-[8px]` para cards e `rounded-[10px]` para botões. Evite arredondamentos excessivos tipo squircle iOS (24px+) em layouts de ferramentas técnicas.

4. CALL TO ACTION & CONTRASTE MAGNÉTICO:
   - O botão de ação principal deve usar a regra da "Inversão Sólida": Fundo branco puro (#FFFFFF) com texto preto puro (#000000). Hover com opacidade 90% e leve brilho difuso `rgba(255,255,255,0.15)`.

5. OVERLAY ATMOSFÉRICO DE RODAPÉ:
   - Aplique uma barra gradiente fixa na base (`h-44 bg-gradient-to-t from-black to-transparent pointer-events-none`) para suavizar a transição de rolagem contínua.
```

---
*Dossiê compilado e homologado para a Biblioteca de Padrões e Referências de Design Systems do Design Engine.*
