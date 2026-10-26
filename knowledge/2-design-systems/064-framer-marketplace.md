---
id: "framer-marketplace"
name: "Framer Marketplace"
url: "https://www.framer.com/marketplace/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["High-End Motion Craft", "Dark Polish & Glass Radiance", "Interactive Bento Architectures", "Spring-Driven Physics", "WebGL Shader Integration"]
densidade_informacao: "Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Framer Motion/JS) a Alto (Canvas/3D/WebGL)"
stack_frameworks: ["React 19 / 18", "Framer Motion", "Framer Canvas Engine", "Framer Plugin API", "Tailwind CSS", "TypeScript", "Three.js / WebGL", "Rive Runtime", "Spline Web"]
compatibilidade:
  fontes_ideais: ["Inter", "Geist Sans", "Plus Jakarta Sans", "Satoshi", "PP Neue Montreal", "Instrument Serif", "JetBrains Mono"]
  paletas_ideais: ["Obsidian Dark Mode (#050505 a #0d0d11)", "Zinc & Slate Monochromes", "Deep Violet & Indigo Luminescence", "Reflective Silver & Chrome Hairlines", "Subtle OKLCH Radial Glows"]
  conflitos_esteticos: ["Brutalismo Y2K caótico sem grid", "Neumorfismo skeuomórfico de plástico opaco", "Design corporativo chapado sem física de movimento (Bootstrap 3 / Flat 2.0)", "Material Design 2 com elevações desbalanceadas"]
---

# Framer Marketplace — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Framer Marketplace** (`framer.com/marketplace`) consolidou-se como o centro nevrálgico da vanguarda visual e interativa da web moderna. Diferente de repositórios convencionais de templates (como ThemeForest, WordPress Marketplace ou Envato), o Framer Marketplace não opera como um mero depósito de layouts estáticos empacotados em HTML/CSS genérico. Ele é uma plataforma onde o **código executável em React, o canvas vetorial de alta fidelidade e a física de animação de nível de produção (Framer Motion) são exatamente a mesma coisa**.

### A Dissolução da Fronteira Entre Design e Código

A assinatura técnica fundamental do ecossistema Framer repousa no fato de que **não há processo de "tradução" imperfeita entre o protótipo do Figma e a implementação do desenvolvedor**:
1. **O Canvas é um Runtime React**: Cada retângulo, quadro (*Frame*) e pilha de layout (*Stack*) desenhado no Framer é uma árvore de componentes React real com renderização via CSS Flexbox/Grid nativo e transforms acelerados por GPU (`transform: translate3d(...)`).
2. **Física de Molas Nativas (`spring`) em Substituição a Curvas Duras**: A identidade tátil dos componentes do marketplace é definida por inércia, massa e amortecimento (`stiffness`, `damping`, `mass`). Não existem transições lineares ou "ease" robóticos; elementos reagem como matéria física real em repouso e sob tração.
3. **Luz Focal, Hairlines Translúcidas e Efeitos Cáusticos**: Os artefatos do marketplace são marcados pelo acabamento artesanal apelidado pela indústria de *"Linear/Vercel Craft Aesthetic"*: bordas de 1 pixel semitransparentes (`rgba(255, 255, 255, 0.08)` a `0.12`), reflexos especulares radiais que perseguem as coordenadas cartesianas do ponteiro do mouse, camadas de desfoque de fundo quádruplas (`backdrop-filter: blur(16px) saturate(180%)`) e sobreposição de gradientes em malha WebGL.

### A Tríade Estrutural do Marketplace: Templates, Plugins e Componentes

O Framer Marketplace divide seu ecossistema em três pilares sinérgicos de altíssimo valor de engenharia:

```
                          ┌─────────────────────────────────────┐
                          │         FRAMER MARKETPLACE          │
                          └──────────────────┬──────────────────┘
                                             │
         ┌───────────────────────────────────┼───────────────────────────────────┐
         ▼                                   ▼                                   ▼
┌──────────────────┐               ┌──────────────────┐                ┌──────────────────┐
│    TEMPLATES     │               │     PLUGINS      │                │   COMPONENTES    │
│  (Sistemas &     │               │ (Workflow, Sync  │                │  (Code Comps,    │
│  Landing Pages)  │               │  & Runtimes)     │                │   Vectors & UI)  │
├──────────────────┤               ├──────────────────┤                ├──────────────────┤
│ • SaaS B2B / AI  │               │ • Framer Plugin  │                │ • Bento Grids    │
│ • DevTools Dark  │               │   API (Sandboxed)│                │ • Island Navbars │
│ • Portfólios     │               │ • Notion / Air-  │                │ • Property-      │
│ • Breakpoints    │               │   table CMS Sync │                │   Controls       │
│ • Layouts fluidos│               │ • ShaderGradient │                │ • Magnetic CTAs  │
│ • CMS Collections│               │ • Spline / Rive  │                │ • Code Overrides │
└──────────────────┘               └──────────────────┘                └──────────────────┘
```

1. **Templates de Produção**: Sistemas completos e responsivos concebidos para SaaS, startups de Inteligência Artificial, estúdios criativos e lançamentos de produtos digitais. Trazem de fábrica hierarquias de páginas, breakpoints calibrados (Desktop 1200px+, Tablet 810px, Mobile 390px), tipografia responsiva via CSS clamp, coleções de CMS prontas e transições orquestradas de entrada de página (*page-load animations*).
2. **Plugins de Workflow, Sincronização & Runtimes Gráficos**: Extensões construídas com a **Framer Plugin API** que rodam em sandbox seguro dentro do editor. Permitem conectar bases de dados externas diretamente ao CMS do site (sincronização bidirecional com Notion, Airtable, Google Sheets e Shopify), além de injetar motores gráficos de terceiros no próprio canvas (como os plugins **ShaderGradient** para WebGL dinâmico, **ASCII** para texturização lo-fi, **Spline** para objetos 3D e **Rive** para state-machines vetoriais interativas).
3. **Componentes Modulares & Vectors**: Blocos isolados de UI de arrastar e soltar (*drag-and-drop*) que empacotam comportamentos complexos com **Property Controls** (painéis visuais onde designers configuram variáveis do React sem abrir o editor de código) e **Code Overrides** (funções de alta ordem em TypeScript que interceptam props de renderização e injetam física de interação refinada).

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados

1. **Landing Pages de Startups de Inteligência Artificial & SaaS B2B High-Growth**:
   Para produtos de tecnologia que precisam comunicar autoridade técnica instantânea, sofisticação de produto e validação de capital de risco (valuation de Tier-1). O acabamento visual refinado do Framer Marketplace transmite confiabilidade técnica superior à de sites convencionais.
2. **Developer Tools, Cloud Infrastructure & Plataformas de Dados**:
   Ferramentas voltadas para programadores (estilo Supabase, Neon, Cloudflare, Resend, Vercel) demandam interfaces escuras, com grids de alta precisão técnica, atalhos de teclado e visualizadores de código interativos. Os templates e componentes do ecossistema Framer são o padrão de referência para esse nicho.
3. **Portfólios de Designers de Produto, Engenheiros Criativos e Diretores de Arte**:
   Projetos que exigem transições de página cinematográficas, mockups interativos de aplicativos, micro-interações táteis e rolagem controlada por inércia (*momentum scrolling*).
4. **Agências Digitais & Estúdios de Branding**:
   Casas de design que precisam de velocidade extrema de entrega mantendo uma estética proprietária que impressione os clientes, aproveitando integrações CMS com Notion ou Airtable para que equipes editoriais atualizem cases sem depender de desenvolvimento contínuo.

### Papel no Ritmo Visual (A Regra 60-30-10)

```
        ┌────────────────────────────────────────────────────────┐
        │  60% — FUNDAÇÃO ESTRUTURAL & SUPERFÍCIES NEUTRAS       │
        │  Canvas escuro profundo (#050505), grid de layout,     │
        │  tipografia escalonada, containers e hairlines neutras │
        └───────────────────────────┬────────────────────────────┘
                                    │
        ┌───────────────────────────┴────────────────────────────┐
        │  30% — ORQUESTRAÇÃO DINÂMICA & NAVEGAÇÃO FLUIDA        │
        │  Island navbars com layoutId, bento grids reativos,    │
        │  carrosséis táteis, switches de pricing com spring     │
        └───────────────────────────┬────────────────────────────┘
                                    │
        ┌───────────────────────────┴────────────────────────────┐
        │  10% — SHOWSTOPPERS PROTAGONISTAS DO MARKETPLACE       │
        │  WebGL Mesh Gradient (ShaderGradient), Objeto 3D       │
        │  Spline/Rive interativo ou ASCII shader localizado     │
        └────────────────────────────────────────────────────────┘
```

- **60% — Fundação Estrutural & Superfícies Neutras**:
  O fundo da página e os containers de conteúdo. Deve adotar paletas neutras profundas (Obsidian `#050505`, Charcoal `#0d0d11`, ou Off-White `#fafafa` em temas claros), tipografia legível e estruturada com kerning afinado (`letter-spacing: -0.02em`) e grids consistentes. Esta camada garante legibilidade e sustentação sem disputar a atenção do usuário.
- **30% — Orquestração Dinâmica & Navegação Fluida**:
  Componentes funcionais com reatividade tátil: a barra de navegação flutuante (*Floating Island*), os cards de Bento Grid com *hover reveal*, carrosséis acionados por arrasto (*drag*) com inércia, caixas colapsáveis de FAQ com interpolação de altura suave e seletores de precificação com spring physics.
- **10% — Showstoppers Protagonistas do Ecossistema**:
  O elemento visual dominante da página (o *"hero hook"*). No Framer Marketplace, esse papel é frequentemente preenchido por um plugin de renderização WebGL (como uma malha orgânica do **ShaderGradient** no fundo da Hero), um asset 3D interativo via **Spline**, ou um efeito tipográfico dinâmico com **ASCII art** reativo ao mouse. **Regra de ouro**: nunca use mais de um showstopper dessa magnitude na mesma dobra visual.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

1. **Aplicações Web Transacionais Complexas e Dashboards Operacionais (SaaS Interior)**:
   O Framer é primariamente uma plataforma para sites de marketing, landing pages de alta conversão, portfólios e CMS institucionais. **Não tente construir o interior de uma aplicação corporativa** (com autenticação OAuth granular, controle de acessos RBAC, tabelas com dezenas de filtros relacionais e centenas de rotas mutáveis) dentro do Framer. Para o dashboard interno, utilize uma stack nativa em React/Next.js com **Shadcn UI** ou **HeroUI**.
2. **Aplicações Offline-First ou Plataformas Web para Mercados de Baixa Conectividade (Redes 2G/3G)**:
   Templates do Framer carregam runtimes de renderização vetorial, módulos do Framer Motion e assets otimizados para navegadores modernos e GPUs dedicadas. Em ambientes corporativos ultra-restritos ou conexões móveis lentas de mercados emergentes, a carga inicial de JavaScript pode comprometer os índices de First Contentful Paint (FCP) e Interaction to Next Paint (INP).
3. **Sistemas de Informação Pública e Portais Governamentais de Acessibilidade Estrita**:
   Portais governamentais que exigem conformidade legal rigorosa com WCAG AAA, navegação estritamente textual sem animações e compatibilidade total com navegadores legados (como leitores de tela em linha de comando) entram em conflito direto com as animações contínuas, gradientes em canvas e renderizações com opacidade atenuada típicas do marketplace.

---

### ⚠️ A Síndrome do "Framer Cookie-Cutter / AI Startup Template Clichê" & Como Escapar

Devido à popularidade avassaladora de certos templates campeões de vendas no Framer Marketplace, a web foi inundada por landing pages indistinguíveis. Uma página cai no clichê pejorativo de **"AI Slop Template"** quando reúne os seguintes vícios repetitivos:
> *Fundo preto absoluto `#000000` + Um grande glow radial roxo ou azul elétrico centralizado atrás do título + Bento Grid de 6 cartões idênticos com borda de 1px com gradiente translúcido + Título dizendo "Supercharge your workflow with next-gen AI" + Botão com reflexo de luz infinito girando no contorno.*

Esse visual padronizado grita falta de originalidade e transmite a percepção imediata de um produto embrionário sem substância real.

#### 5 Estratégias Mandatórias para Personalizar Recursos do Framer Marketplace e Torná-los Únicos:

1. **Subversão da Paleta de Iluminação (Abandone o Roxo / Índigo Clichê)**:
   Troque o onipresente gradiente roxo/ciano por atmosferas cromáticas autorais:
   - *Tons Minerais e Terrosos*: Ocre profundo, argila queimada, cinza basalto e reflexos em âmbar quente.
   - *Estética Industrial / Cyber Monocromática*: Elimine qualquer cor de destaque; utilize variações estritas de prata, titânio, grafite fosco e preto profundo, utilizando apenas o branco puro nos pontos de conversão.
   - *Verde Florestal Profundo / Oliva Escuro*: Uma paleta muito sofisticada e rara em SaaS de tecnologia.
2. **Quebra da Simetria do Bento Grid**:
   Fuja do grid uniforme de caixas retangulares simétricas de 2x3. Combine um módulo super denso de texto editorial com um módulo super aberto de respiração visual, integrando elementos que quebram o limite da caixa (*overflow visible*) ou que se sobrepõem geometricamente aos eixos do grid.
3. **Tipografia de Alto Contraste Intelectual**:
   Substitua a escolha genérica da fonte *Inter* pura por contrastes com personalidade:
   - Combine títulos em serif contemporânea de alto impacto (*Instrument Serif*, *Fraunces*, *Newsreader*) com textos de suporte em grotescas neutras (*PP Neue Montreal*, *Satoshi*, *Geist Sans*).
   - Incorpore labels e metadados estruturados em fontes monoespaçadas técnicas (*JetBrains Mono*, *Geist Mono*), gerando um contraste de engenharia refinada.
4. **Calibração de Física Desacelerada (Menos Pipoca, Mais Gravidade)**:
   Templates clichês costumam abusar de molas com salto excessivo (*bouncy*). Ajuste a física para molas com amortecimento elevado (`damping: 40`, `stiffness: 250`, `mass: 1.2`), criando uma sensação de peso nobre, como a porta de um cofre ou um equipamento de som analógico de luxo.
5. **Substituição de Efeitos Cosméticos por Micro-Interações Contextuais**:
   Remova bordas giratórias estéreis e substitua-as por dados reais: cursores colaborativos simulados, preview de código ao vivo, seletores interativos funcionais que recalculam métricas de economia financeira ou calculadoras de ROI dinâmicas.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 10 componentes, padrões e integrações mais emblemáticos do ecossistema do Framer Marketplace:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. Dynamic Shader Hero (ShaderGradient WebGL Integration)             │
│ 2. Spotlight Interactive Bento Grid (Pointer Vector Coordinates)       │
│ 3. Floating Island Navbar (LayoutId Sliding Marker)                   │
│ 4. Live CMS Sync Gallery (Notion / Airtable Plugin Pipeline)          │
│ 5. Dynamic ASCII Retro-Filter (Canvas Post-Processing)                │
│ 6. Interactive 3D / State-Machine Widget (Spline / Rive Runtime)      │
│ 7. Spring-Calibrated Pricing Switcher with Elastic Badges              │
│ 8. Sticky Scroll Storytelling Deck (Scroll-Linked Overrides)           │
│ 9. Magnetic Physics CTA Button (Radial Distance Attractor)             │
│ 10. Liquid Metal / Blur-Reveal Immersive Footer                        │
└────────────────────────────────────────────────────────────────────────┘
```

### 1. Dynamic Shader Hero (ShaderGradient WebGL Integration)
- **Anatomia Visual**: Pano de fundo da dobra principal (Hero) composto por uma malha fluida de gradientes calculados via shaders GLSL em WebGL. Apresenta movimento orgânico perpétuo com três ou quatro focos de cor que se fundem com ruído Perlin/Simplex sutil e iluminação cáustica, sem qualquer quebra de compressão (sem banding de cor) mesmo em monitores 4K HDR.
- **Gatilho de Interação**: Animação contínua em loop a 60 FPS com desaceleração quando em repouso; sutil distorção de rotação de câmera tridimensional orientada pela posição `(x, y)` do cursor na janela.
- **Onde encaixar na página**: Hero Section de landing pages institucionais, backgrounds de seções de encerramento (Pre-footer) e painéis de demonstração de produto de IA.

### 2. Spotlight Interactive Bento Grid (Pointer Vector Coordinates)
- **Anatomia Visual**: Composição modular assimétrica de cartões escuros (`#0b0b0f`), separados por espaçamentos precisos de 16px ou 24px com cantos arredondados generosos (`rounded-3xl` / 24px). Cada cartão possui uma hairline translúcida de 1px. Ao mover o cursor sobre a área do grid, um cone de luz radial gradiente suave (`radial-gradient(600px circle at x y, rgba(255,255,255,0.06), transparent 40%)`) ilumina contextualmente as superfícies e destaca as bordas dos cartões próximos ao ponteiro.
- **Gatilho de Interação**: `onMouseMove` contínuo interceptado via `useMotionValue` e suavizado por amortecedores de mola, evitando re-renderizações no ciclo React.
- **Onde encaixar na página**: Seção de Funcionalidades Principais (Feature Showcase / Why Choose Us).

### 3. Floating Island Navbar (LayoutId Sliding Marker)
- **Anatomia Visual**: Barra de navegação em forma de pílula flutuante (`rounded-full`) suspensa a 24px do topo da viewport com largura contida (máximo 640px a 720px). Utiliza fundo em vidro fosco (`backdrop-blur-md bg-black/40 border border-white/10`). Ao navegar ou passar o mouse sobre os links de texto, uma cápsula de destaque com fundo acinzentado (`bg-white/10`) desliza organicamente por baixo do texto selecionado utilizando a primitiva `layoutId` do Framer Motion.
- **Gatilho de Interação**: `onMouseEnter` / `onMouseLeave` entre os itens de menu e scroll de página (a barra pode recolher para uma versão compacta ao rolar para baixo e expandir ao rolar para cima).
- **Onde encaixar na página**: Topo fixo global (Global Header).

### 4. Live CMS Sync Gallery (Notion / Airtable Plugin Pipeline)
- **Anatomia Visual**: Coleção dinâmica de cartões em grid com paginação virtual e filtros contextuais por tags (ex: categorias de blog, diretório de ferramentas ou cases de clientes). Os dados (textos, imagens em alta resolução, tags e metadados) são sincronizados em tempo real via plugins de CMS com bases de dados no Notion ou tabelas no Airtable, sem necessidade de deploy manual a cada atualização editorial.
- **Gatilho de Interação**: Clique nas tags de filtro que reorganizam os cartões na tela com animação fluida de reposicionamento automático (`layout` animation do Framer Motion) sem recarregar a página.
- **Onde encaixar na página**: Blog / Changelog, Diretório de Ferramentas / Integrações, Galeria de Estudos de Caso.

### 5. Dynamic ASCII Retro-Filter (Canvas Post-Processing)
- **Anatomia Visual**: Componente baseado em elemento `<canvas>` que recebe uma imagem, vetor ou texto renderizado e converte a densidade de luminosidade dos pixels em uma matriz de caracteres ASCII monoespaçados (`@`, `%`, `#`, `*`, `+`, `=`, `:`, `.`). Proporciona uma estética retro-futurista, de alta densidade técnica, típica de terminais Unix e ambientes de cibersegurança.
- **Gatilho de Interação**: Hover do mouse que altera a escala da grade de caracteres (*font-size* da matriz) ou scroll que modula a densidade e o brilho dos caracteres conforme o elemento entra no campo de visão.
- **Onde encaixar na página**: Seção de Segurança / Criptografia, Demonstração de Terminal para Desenvolvedores, Elemento decorativo de fundo de rodapé.

### 6. Interactive 3D / State-Machine Widget (Spline / Rive Runtime)
- **Anatomia Visual**: Objeto tridimensional volumétrico (renderizado via WebGL pela engine do Spline) ou animação vetorial com rig e interpolação de ossos (via engine do Rive). Apresenta materiais fisicamente realistas (PBR) com reflexos metálicos, vidros translúcidos ou iluminação dinâmica que reage ao cursor.
- **Gatilho de Interação**: Rotação orbital automática contínua que pode ser agarrada e girada livremente pelo usuário via drag (`pointerdown` + `pointermove`), ou máquinas de estado que alteram posturas com base em cliques em botões externos da página.
- **Onde encaixar na página**: Dobra principal da Hero (lado direito em split layout), cartão de destaque em Bento Grid ou ilustração interativa de checkout.

### 7. Spring-Calibrated Pricing Switcher with Elastic Badges
- **Anatomia Visual**: Chave de seleção Mensal / Anual ergonomicamente otimizada com indicador deslizante de mola e um badge flutuante anexado à opção anual ("Pague anual e economize 20%"). Quando o switch é alternado, os valores numéricos dos planos disparam uma animação de rotação vertical de números (*number ticker/counter*) e o badge executa um sutil salto elástico (*spring overshoot*) com brilho pulsante (*shimmer*).
- **Gatilho de Interação**: Clique no toggle com resposta auditiva ou tátil imediata e transição física suave dos valores monetários.
- **Onde encaixar na página**: Seção de Planos & Preços (Pricing Table).

### 8. Sticky Scroll Storytelling Deck (Scroll-Linked Overrides)
- **Anatomia Visual**: Seção vertical de alta estatura (ex: `height: 300vh`) onde a tela se fixa (*sticky*) no topo da viewport. À esquerda, textos explicativos e etapas avançam sequencialmente; à direita, um container com a interface do produto transiciona dinamicamente entre diferentes abas, alterando zoom de câmera, destaques de luz e dados em tela à medida que o usuário rola a página.
- **Gatilho de Interação**: Rolagem contínua governada pelo hook `useScroll` e valores interpolados via `useTransform`, garantindo sincronia absoluta entre a mão do usuário e a narrativa visual na tela.
- **Onde encaixar na página**: Seção "Como Funciona" / Passo a Passo do Produto / Tour da Interface.

### 9. Magnetic Physics CTA Button (Radial Distance Attractor)
- **Anatomia Visual**: Botão de conversão de alto calibre com fundo escuro acetinado, borda interna iluminada (*inset hairline*) e gradiente de reflexo que acompanha a direção de aproximação do cursor. Quando o ponteiro entra em uma zona de atração de ~40px ao redor do botão, o botão inteiro se desloca elasticamente em direção às coordenadas do cursor, como se estivesse sob a influência de um ímã físico.
- **Gatilho de Interação**: Evento `onMouseMove` com cálculo de vetor euclidiano de distância e retorno amortecido ao centro (`x: 0, y: 0`) no `onMouseLeave`.
- **Onde encaixar na página**: Botão de Ação Primário na Hero Section e Chamada de Ação Final (Pre-Footer Banner).

### 10. Liquid Metal / Blur-Reveal Immersive Footer
- **Anatomia Visual**: Encerramento cinematográfico do site com tipografia de marca em escala colossal (preenchendo 100% da largura da viewport), preenchida por um gradiente que simula metal líquido ou chrome reflexivo. Ao rolar até o final da página, os links de navegação, termos legais e créditos são desvendados através de uma transição combinada de remoção de desfoque progressivo (`filter: blur(12px) -> blur(0px)`) e elevação vertical sutil.
- **Gatilho de Interação**: Disparado via `IntersectionObserver` quando o rodapé atinge 20% de visibilidade na viewport.
- **Onde encaixar na página**: Rodapé Global da Aplicação (Footer).

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Produção

Para recriar a fidelidade estética, a física de movimento e os padrões do Framer Marketplace fora do ambiente proprietário do Framer (isto é, em uma aplicação React 19 / Next.js com Tailwind CSS), instale as seguintes dependências centrais:

```bash
# Núcleo de animação, utilitários de classe e ícones
npm install framer-motion clsx tailwind-merge lucide-react

# Opcionais para runtimes 3D e Shaders avançados
npm install @rive-app/react-canvas @splinetool/react-spline three
```

### Física de Movimento, Amortecimento & Curvas do Ecossistema Framer

A assinatura de movimento do ecossistema Framer é categoricamente dividida em presets padronizados de molas (`spring`) e curvas bezier refinadas:

```typescript
// Presets de Física Oficiais do Framer Motion para o Ecossistema
export const framerPhysics = {
  // Mola rápida e tátil para botões, switches e tooltips
  snappy: {
    type: "spring",
    stiffness: 400,
    damping: 30,
    mass: 0.8,
  },
  // Mola suave e fluida para modais, gavetas e menus
  smooth: {
    type: "spring",
    stiffness: 220,
    damping: 26,
    mass: 1.0,
  },
  // Mola com inércia lenta e pesada para containers de storytelling e cards
  gravitas: {
    type: "spring",
    stiffness: 120,
    damping: 20,
    mass: 1.2,
  },
  // Mola com overshoot lúdico para badges e reações
  bouncy: {
    type: "spring",
    stiffness: 320,
    damping: 14,
    mass: 0.6,
  },
  // Curvas Cubic-Bezier para transições contínuas sem física de mola
  easings: {
    easeOutCubic: [0.215, 0.61, 0.355, 1.0],
    framerCinematic: [0.16, 1.0, 0.3, 1.0],
    framerInOut: [0.65, 0.0, 0.35, 1.0],
  },
} as const
```

---

### Como o Framer Funciona Sob o Capô: Code Components & Property Controls

Para desenvolvedores que criam componentes modulares destinados ao Framer Marketplace, a API `addPropertyControls` expõe controles visuais nativos no painel lateral do Framer, permitindo que qualquer designer parametrize componentes React complexos:

```tsx
import { addPropertyControls, ControlType } from "framer"

// Exemplo da interface técnica de um Code Component do Framer
export function BadgePill({ title, active, color }) {
  return (
    <div style={{ backgroundColor: color, opacity: active ? 1 : 0.5 }}>
      {title}
    </div>
  )
}

// Configuração dos controles que o designer verá no painel direito do Framer
addPropertyControls(BadgePill, {
  title: {
    type: ControlType.String,
    title: "Texto do Badge",
    defaultValue: "Novo Recurso",
  },
  active: {
    type: ControlType.Boolean,
    title: "Ativo",
    defaultValue: true,
  },
  color: {
    type: ControlType.Color,
    title: "Cor de Destaque",
    defaultValue: "#6366f1",
  },
})
```

---

### Receitas de Código Funcionais e Prontas para Produção

#### Receita 1: Bento Grid Card com Spotlight Radial que Persegue o Cursor
Esta receita implementa a icônica iluminação interativa em cartões escuros com tracking vetorial ultra-otimizado (sem jank ou lag no ponteiro do mouse):

```tsx
"use client"

import * as React from "react"
import { motion, useMotionTemplate, useMotionValue } from "framer-motion"
import { Sparkles } from "lucide-react"

interface SpotlightCardProps {
  title: string
  description: string
  tag: string
  children?: React.ReactNode
}

export function SpotlightBentoCard({
  title,
  description,
  tag,
  children,
}: SpotlightCardProps) {
  // Coordenadas de mouse puras em MotionValues (evita re-renders de estado React)
  const mouseX = useMotionValue(0)
  const mouseY = useMotionValue(0)

  function handleMouseMove({
    currentTarget,
    clientX,
    clientY,
  }: React.MouseEvent<HTMLDivElement>) {
    const { left, top } = currentTarget.getBoundingClientRect()
    mouseX.set(clientX - left)
    mouseY.set(clientY - top)
  }

  return (
    <div
      onMouseMove={handleMouseMove}
      className="group relative flex flex-col justify-between overflow-hidden rounded-3xl border border-white/10 bg-[#0c0d12] p-8 text-white shadow-2xl transition-colors duration-300 hover:border-white/20"
    >
      {/* Camada 1: Brilho Focal Radial de Fundo que segue o mouse */}
      <motion.div
        className="pointer-events-none absolute -inset-px rounded-3xl opacity-0 transition-opacity duration-300 group-hover:opacity-100"
        style={{
          background: useMotionTemplate`
            radial-gradient(
              550px circle at ${mouseX}px ${mouseY}px,
              rgba(99, 102, 241, 0.15),
              transparent 80%
            )
          `,
        }}
      />

      {/* Camada 2: Hairline especular destacando a borda superior interna */}
      <div className="pointer-events-none absolute inset-0 rounded-3xl shadow-[inset_0_1px_0_0_rgba(255,255,255,0.12)]" />

      {/* Cabeçalho do Card */}
      <div className="relative z-10 flex items-center justify-between">
        <span className="inline-flex items-center gap-1.5 rounded-full border border-white/10 bg-white/5 px-3 py-1 text-xs font-medium tracking-wide text-zinc-300 backdrop-blur-md">
          <Sparkles className="h-3.5 w-3.5 text-indigo-400" />
          {tag}
        </span>
        <span className="text-xs font-mono text-zinc-500">PROD // 064</span>
      </div>

      {/* Área Central / Conteúdo Gráfico */}
      <div className="relative z-10 my-8 flex min-h-[140px] items-center justify-center">
        {children || (
          <div className="flex h-24 w-full items-center justify-center rounded-2xl border border-dashed border-white/10 bg-white/[0.02]">
            <span className="text-xs font-mono text-zinc-500">Interactive Canvas Slot</span>
          </div>
        )}
      </div>

      {/* Textos Informativos */}
      <div className="relative z-10 space-y-2">
        <h3 className="text-xl font-semibold tracking-tight text-zinc-100">
          {title}
        </h3>
        <p className="text-sm leading-relaxed text-zinc-400">
          {description}
        </p>
      </div>
    </div>
  )
}
```

---

#### Receita 2: Floating Island Navbar com Indicador Deslizante via `layoutId`
O padrão definitivo de navegação dos principais templates de SaaS e Portfólio do Framer Marketplace:

```tsx
"use client"

import * as React from "react"
import { motion } from "framer-motion"
import { cn } from "@/lib/utils"

interface NavItem {
  id: string
  label: string
}

const navItems: NavItem[] = [
  { id: "features", label: "Recursos" },
  { id: "templates", label: "Templates" },
  { id: "plugins", label: "Plugins" },
  { id: "pricing", label: "Preços" },
]

export function FloatingIslandNavbar() {
  const [activeTab, setActiveTab] = React.useState(navItems[0].id)
  const [hoveredTab, setHoveredTab] = React.useState<string | null>(null)

  return (
    <header className="fixed top-6 inset-x-0 z-50 flex justify-center px-4">
      <nav className="flex items-center gap-1 rounded-full border border-white/10 bg-black/60 p-1.5 shadow-[0_16px_32px_-8px_rgba(0,0,0,0.5),inset_0_1px_0_0_rgba(255,255,255,0.1)] backdrop-blur-xl">
        {navItems.map((item) => {
          const isSelected = activeTab === item.id
          const isHovered = hoveredTab === item.id

          return (
            <button
              key={item.id}
              onClick={() => setActiveTab(item.id)}
              onMouseEnter={() => setHoveredTab(item.id)}
              onMouseLeave={() => setHoveredTab(null)}
              className={cn(
                "relative rounded-full px-4 py-2 text-sm font-medium transition-colors duration-200 outline-none focus-visible:ring-2 focus-visible:ring-indigo-500",
                isSelected ? "text-white" : "text-zinc-400 hover:text-zinc-200"
              )}
            >
              {/* Efeito 1: Indicador deslizante de seleção ativa (layoutId) */}
              {isSelected && (
                <motion.div
                  layoutId="active-island-pill"
                  className="absolute inset-0 rounded-full bg-white/15 border border-white/20 shadow-sm"
                  transition={{
                    type: "spring",
                    stiffness: 380,
                    damping: 30,
                  }}
                />
              )}

              {/* Efeito 2: Destaque de hover suave compartilhado */}
              {isHovered && !isSelected && (
                <motion.div
                  layoutId="hover-island-pill"
                  className="absolute inset-0 rounded-full bg-white/5"
                  transition={{
                    type: "spring",
                    stiffness: 400,
                    damping: 35,
                  }}
                />
              )}

              <span className="relative z-10">{item.label}</span>
            </button>
          )
        })}

        {/* Botão de Ação CTA Embutido */}
        <div className="ml-2 pl-2 border-l border-white/10">
          <button className="relative overflow-hidden rounded-full bg-indigo-600 px-4 py-2 text-sm font-medium text-white shadow-md transition-all duration-200 hover:bg-indigo-500 active:scale-95">
            Começar Agora
          </button>
        </div>
      </nav>
    </header>
  )
}
```

---

#### Receita 3: Magnetic Physics Action Button
Reprodução fiel do botão de atração magnética e física elástica:

```tsx
"use client"

import * as React from "react"
import { motion, useMotionValue, useSpring } from "framer-motion"
import { ArrowUpRight } from "lucide-react"

export function MagneticButton({
  children = "Explorar Marketplace",
  onClick,
}: {
  children?: React.ReactNode
  onClick?: () => void
}) {
  const ref = React.useRef<HTMLButtonElement>(null)

  // Coordenadas com amortecimento por mola suave
  const mouseX = useMotionValue(0)
  const mouseY = useMotionValue(0)

  const springConfig = { damping: 20, stiffness: 200, mass: 0.6 }
  const x = useSpring(mouseX, springConfig)
  const y = useSpring(mouseY, springConfig)

  function handleMouseMove(e: React.MouseEvent<HTMLButtonElement>) {
    if (!ref.current) return
    const { clientX, clientY } = e
    const { left, top, width, height } = ref.current.getBoundingClientRect()
    const centerX = left + width / 2
    const centerY = top + height / 2

    // Deslocamento limitado a 35% do tamanho do botão
    const distanceX = (clientX - centerX) * 0.35
    const distanceY = (clientY - centerY) * 0.35

    mouseX.set(distanceX)
    mouseY.set(distanceY)
  }

  function handleMouseLeave() {
    mouseX.set(0)
    mouseY.set(0)
  }

  return (
    <motion.button
      ref={ref}
      style={{ x, y }}
      onMouseMove={handleMouseMove}
      onMouseLeave={handleMouseLeave}
      onClick={onClick}
      whileTap={{ scale: 0.94 }}
      className="group relative inline-flex items-center gap-2 rounded-full border border-white/15 bg-zinc-950 px-6 py-3.5 text-sm font-medium text-zinc-100 shadow-[0_12px_24px_-6px_rgba(0,0,0,0.6),inset_0_1px_0_0_rgba(255,255,255,0.2)] transition-colors duration-200 hover:border-white/30 hover:bg-zinc-900 focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-indigo-400"
    >
      <span className="relative z-10 tracking-tight">{children}</span>
      <ArrowUpRight className="relative z-10 h-4 w-4 text-zinc-400 transition-transform duration-200 group-hover:translate-x-0.5 group-hover:-translate-y-0.5 group-hover:text-white" />

      {/* Reflexo radial especular sutil na base do botão */}
      <div className="pointer-events-none absolute inset-0 rounded-full opacity-0 transition-opacity duration-300 group-hover:opacity-100 bg-[radial-gradient(circle_at_top,_rgba(255,255,255,0.12),_transparent_70%)]" />
    </motion.button>
  )
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao arquitetar uma nova aplicação e referenciar padrões, componentes ou templates derivados do **Framer Marketplace**, as inteligências artificiais e os arquitetos de software devem aderir às seguintes diretrizes mandatórias no `DESIGN_BLUEPRINT.md`:

```
┌────────────────────────────────────────────────────────────────────────┐
│                   CHECKLIST DO DESIGN BLUEPRINT                        │
├────────────────────────────────────────────────────────────────────────┤
│ 1. Delimitação de Papel: Marketing / Landing vs. Core App Dashboard     │
│ 2. Parâmetros de Física: Molas declaradas no Theme Motion Tokens       │
│ 3. Guardrail de Showstoppers: Máximo de 1 WebGL Shader por dobra       │
│ 4. Anti-Clichê Mandatório: Paleta não-roxa e tipografia diferenciada   │
│ 5. Performance Budget: 60 FPS garantidos via MotionValues isolados     │
└────────────────────────────────────────────────────────────────────────┘
```

1. **Separação Clara de Domínios (Marketing vs. Dashboard Interno)**:
   - Declarar expressamente que os componentes inspirados no Framer Marketplace pertencem à camada de **Aquisição, Conversão e Storytelling de Produto (Marketing Site / Landing Pages / Docs públicas)**.
   - Declarar que o interior autenticado do produto (Core Web App / Dashboard Operacional) deve utilizar **Shadcn UI** ou **HeroUI**, preservando a coerência ergonômica de formulários densos e tabelas de dados.
2. **Declaração Formal de Tokens de Movimento (`framerPhysics`)**:
   - Registrar no documento os valores numéricos exatos de amortecimento de mola (`stiffness`, `damping`, `mass`) a serem aplicados em cada família de componentes (ex: `snappy` para botões e links de navegação; `smooth` para modais e switches; `gravitas` para storytelling com scroll).
   - Proibir o uso de durações temporais arbitrárias (`transition: all 0.3s ease`) em elementos de interação direta do usuário.
3. **Governança de Showstoppers & WebGL (A Regra de Ouro do 10%)**:
   - Limitar rigorosamente o uso de plugins WebGL/3D (como **ShaderGradient**, **Spline** ou **Rive**) a **no máximo um elemento protagonista por viewport**.
   - Garantir que qualquer renderizador em Canvas WebGL possua mecanismo de pausa automática (`cancelAnimationFrame` ou observador de interseção) quando o componente rolar para fora da tela, eliminando desperdício de bateria e processamento em dispositivos móveis.
4. **Mandato Anti-Clichê no Blueprint**:
   - O Blueprint deve especificar uma paleta cromática singular (ex: Obsidian `#050505` com acentos em Cobre Refinado ou Esmeralda Escuro), banindo terminantemente o fundo preto liso com orbes roxos descentralizados sem contexto de marca.
   - A especificação tipográfica deve definir o emparelhamento com ao menos uma família com forte personalidade (ex: títulos em *Instrument Serif* ou *PP Neue Montreal* com corpo técnico em *Geist Sans*).
5. **Auditoria de Performance e Orçamento de Layout Shift**:
   - Todo componente com rastreamento de cursor (como o `SpotlightBentoCard` ou o `MagneticButton`) deve ser implementado via `useMotionValue` ou CSS Custom Properties inline, sendo estritamente proibido o uso de `useState` no evento `onMouseMove` para evitar re-renderizações desnecessárias da árvore React.
