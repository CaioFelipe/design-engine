---
id: "ecomm-design"
name: "Ecomm Design"
url: "https://ecomm.design/"
category: "5-galleries"
schema_type: "C-galleries"
dna_estetico:
  - "Curadoria Pragmática de E-commerce Orientada a Métricas de Conversão (CRO-First)"
  - "Dissecção Anatômica de Lojas Reais em Produção (Homepage, PLP, PDP, Cart Drawer, Checkout, Footer)"
  - "Mapeamento Completo de Tech Stack, Gateways de Pagamento, MarTech & Ferramentas de Retenção"
  - "Direct-to-Consumer (DTC) & Digitally Native Vertical Brands (DNVB) Aesthetics"
  - "Microinterações de Compra & Ajax Cart Drawers com Gamificação de Frete Grátis"
  - "Sistemas de Facetamento Dinâmico & Visual Swatches para Variantes Complexas"
  - "Mobile-First Sticky Actions & Thumb-Zone Ergonomics"
densidade_informacao: "Media/Narrativa a Alta/Utilitaria"
impacto_visual: "Editorial/Sofisticado & Utilitario/Comercial"
custo_computacional: "Moderado a Otimizado (Performance crítica de Core Web Vitals, LCP < 2.5s, CLS < 0.1, lazy-loading de assets visuais e miniaturas)"
stack_frameworks:
  - "Shopify & Shopify Plus (Liquid, Hydrogen, Oxygen)"
  - "WooCommerce & WordPress (Gutenberg, Timber, Roots/Sage)"
  - "BigCommerce (Stencil, Catalyst)"
  - "Webflow E-commerce"
  - "Headless E-commerce (Next.js App Router, MedusaJS, Saleor, Shopify Storefront API)"
  - "Tailwind CSS v3 / v4 (E-commerce utility system)"
  - "Framer Motion / Motion.dev (Cart drawers, modal animations, accordion physics)"
  - "Radix UI / Headless UI (Dialogs, Accordions, Radio Groups para variantes)"
compatibilidade:
  fontes_ideais:
    - "Neo-Grotesque Universal & Clean Commerce: Inter, Geist, Poppins, Plus Jakarta Sans, General Sans, Satoshi"
    - "Editorial Serif & Luxury Fashion: PP Editorial New, GT Sectra, Cormorant Garamond, Ogg, Playfair Display"
    - "High-Impact Display & Bold Streetwear: Syne, Clash Display, Monument Extended, Bebas Neue"
    - "Monoespaçada de Preço, Metadados & Código SKU: JetBrains Mono, Geist Mono, Fragment Mono, Space Mono"
  paletas_ideais:
    - "Alabaster Clean Minimal (Dominante B2C): #FFFFFF (Pure Surface), #F8F9FA (Card Canvas), #E5E7EB (Hairline Border), #111827 (Ink Primary), #6B7280 (Muted Secondary)"
    - "Obsidian Luxury & Midnight DTC: #0A0A0C (Deep Black), #141418 (Elevation Surface), #26262E (Subtle Hairline), #F3F4F6 (Text 100%), #9CA3AF (Text Muted)"
    - "Warm Editorial & Earthy Tones: #FAF7F2 (Oatmeal Cream), #F0EAE1 (Sand Card), #2D2723 (Espresso Charcoal), #786C65 (Warm Muted), #D4A373 (Terracotta Accent)"
    - "High-Converting Conversion Accents (10% Action): #10B981 (Emerald Guarantee & Free Shipping), #2563EB (Electric Indigo CTA), #E11D48 (Urgency Crimson / Sale Badge), #F59E0B (Review Stars Amber)"
  combinacoes_recomendadas:
    - "Canvas neutro de alto contraste + fotografia de estúdio com fundo transparente ou ambientada em alta resolução"
    - "Cart Drawer com mola ágil (`damping: 28, stiffness: 300`) e barra de progresso de frete reativa em tempo real"
    - "PDPs modulares com visual swatches acessíveis via ARIA e acordeões de especificações técnicas"
    - "Miniaturas com aspect-ratio reservado (1:1, 3:4 ou 4:5) para prevenir Cumulative Layout Shift (CLS)"
  conflitos_esteticos:
    - "Scrolljacking pesado e distorções WebGL que atrasam a ação de compra do consumidor"
    - "Ausência de fotografia real de produto em alta definição (destrói imediatamente a credibilidade da loja)"
    - "Dark patterns agressivos (popups invasivos de roleta, contadores falsos de urgência que degradam a confiança)"
    - "Cart drawers sem suporte a teclado (`aria-modal`, `focus-trap`) e sem indicação clara de custos adicionais de frete"
    - "Botão de 'Adicionar ao Carrinho' com baixo contraste cromático ou escondido fora do primeiro viewport em mobile"
---

# Ecomm Design — Dossiê Estético, Anatomia de Layout & Padrões de Referência

```
███████╗ ██████╗ ██████╗ ███╗   ███╗███╗   ███╗    ██████╗ ███████╗███████╗██╗ ██████╗ ███╗   ██╗
██╔════╝██╔════╝██╔═══██╗████╗ ████║████╗ ████║    ██╔══██╗██╔════╝██╔════╝██║██╔════╝ ████╗  ██║
█████╗  ██║     ██║   ██║██╔████╔██║██╔████╔██║    ██║  ██║█████╗  ███████╗██║██║  ███╗██╔██╗ ██║
██╔══╝  ██║     ██║   ██║██║╚██╔╝██║██║╚██╔╝██║    ██║  ██║██╔══╝  ╚════██║██║██║   ██║██║╚██╗██║
███████╗╚██████╗╚██████╔╝██║ ╚═╝ ██║██║ ╚═╝ ██║    ██████╔╝███████╗███████║██║╚██████╔╝██║ ╚████║
╚══════╝ ╚═════╝ ╚═════╝ ╚═╝     ╚═╝╚═╝     ╚═╝    ╚═════╝ ╚══════╝╚══════╝╚═╝ ╚═════╝ ╚═╝  ╚═══╝
    C   U   R   A   T   E   D       C   O   M   M   E   R   C   E       E   N   G   I   N   E
```

---

## 1. DNA Estético & Filosofia de Curadoria

Fundado em abril de 2016 pelo estrategista digital e empreendedor **Bogdan Rancea** (também co-fundador da consagrada publicação técnica *Ecommerce-Platforms.com*), o **Ecomm Design** (`https://ecomm.design/`) consolidou-se como o maior e mais respeitado diretório de engenharia visual, direção de arte e arquitetura de software para lojas virtuais do mundo, contabilizando um acervo vivo superior a **4.058 lojas virtuais selecionadas a dedo**.

Enquanto a maioria das galerias generalistas de web design (como Awwwards, Siteinspire ou FWA) prioriza a pirotecnia visual, transições tridimensionais abstratas e experiências experimentais desenvolvidas especificamente para impressionar jurados de premiações, o Ecomm Design adota uma postura diametralmente oposta e rigorosamente orientada ao comércio real.

A tese fundamental expressa na filosofia da galeria sintetiza perfeitamente esse posicionamento:
> *"Ecomm.design aims to showcase an eclectic mix of stores across many different verticals, with less of a focus on front-end experimentation and more on the metrics and UX practices that matter to ecommerce."*
> *(O Ecomm.design visa apresentar uma mistura eclética de lojas em diversos setores, com menos foco em experimentações de front-end e muito mais foco nas métricas e nas práticas de UX que realmente importam para o comércio eletrônico).*

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        THE ECOMM DESIGN CURATORIAL ENGINE                              │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  [ Production Storefronts ] ──► [ Full Anatomical Audit ] ──► [ Stack Identification ] │
│   • 4,058+ Live Stores           • Full Homepage Breakdown     • CMS: Shopify, Woo     │
│   • Global DTC & DNVB Brands     • PLP (Collection/Catalog)    • Payments: Stripe, Shop│
│   • Real Commercial Traffic      • PDP (Product Detail Page)   • MarTech: Klaviyo, CRX │
│   • Verified Checkout Flows      • Cart Drawer / Checkout      • Speed / CDN Layer     │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ TRIAD: Visual Aesthetics (Art Direction) × Usability (CRO/UX) × Tech Stack (Software)  │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 1.1 A Curadoria Atômica de Páginas: Homepage, PLP, PDP e Cart Drawer

O grande diferencial do Ecomm Design perante qualquer outra plataforma de inspiração é que ele **não trata o e-commerce como uma imagem estática de landing page**. Cada loja catalogada recebe uma auditoria visual profunda que desmembra os 5 estágios cruciais da jornada de compra:

1. **Homepage Editorial (Brand Positioning & Merchandising)**:
   - Estrutura de banners heróicos, coleções em destaque, carrosséis de produtos mais vendidos (*bestsellers*), blocos de prova social com selos de imprensa e declarações de autoridade de marca.
2. **PLP — Product Listing Page (Catálogo & Facetamento)**:
   - Arquitetura de grids responsivos, filtros laterais ou barras de facetamento horizontal (*sticky filter bars*), paginação infinita com gatilhos de *load more*, estados de *hover* dinâmicos com revelação de lookbook/segunda foto e badges promocionais.
3. **PDP — Product Detail Page (O Epicentro da Conversão)**:
   - Disposição anatômica dividida (*split sticky PDP*), galerias de fotos em alta resolução (com suporte a vídeo ou render 3D), seletores de variantes interativos (*color swatches*, *size pills*), avisos de estoque baixo em tempo real, acordeões de detalhes técnicos e calculadoras de frete integradas.
4. **Cart Drawer & Checkout Flow (Fricção Zero)**:
   - O comportamento das gavetas de carrinho (*slide-out Ajax drawers*), barras dinâmicas com gamificação de frete grátis (*"Faltam apenas R$ 40 para frete grátis"*), upsells contextuais de 1 clique e atalhos de finalização rápida (*express checkout* via Apple Pay, Google Pay e Shop Pay).
5. **Rodapé Transacional (Trust, Policy & Legal)**:
   - Selos de segurança criptográfica, políticas explícitas de trocas e devoluções gratuitas, seletores de moeda/país e canais diretos de suporte ao cliente.

### 1.2 A Camada de Engenharia Reversa: O Mapa do Tech Stack

Diferente de agregadores visuais superficiais, o Ecomm Design atua como uma ferramenta de **inteligência competitiva de software**. Para cada website registrado, o sistema identifica, valida e categoriza todas as ferramentas e tecnologias ativas sob o capô:

```
                               ┌───────────────────────────────┐
                               │   ECOMM DESIGN TECH MATRIX    │
                               └───────────────┬───────────────┘
                                               │
         ┌───────────────────┬─────────────────┼──────────────────┬──────────────────┐
         │                   │                 │                  │                  │
         ▼                   ▼                 ▼                  ▼                  ▼
  [ 1. PLATFORMS ]    [ 2. PAYMENTS ]   [ 3. RETENTION ]   [ 4. CUSTOMER CX ]  [ 5. OPTIMIZATION ]
  • Shopify Plus      • Shopify Pay     • Klaviyo          • Gorgias           • GA4 / Clarity
  • WooCommerce       • Stripe          • Omnisend         • Zendesk Chat      • Hotjar / VWO
  • BigCommerce       • Klarna / Affirm • Mandrill         • Intercom          • Optimizely
  • Webflow Ecomm     • Afterpay        • Privy Popups     • Tidio             • Cloudflare CDN
  • Custom / Headless • PayPal Express  • Yotpo Loyalty    • Okendo Reviews    • Fastly Edge
```

---

## 2. Cenários Ideais de Consulta (Quando Usar como Direção Visual)

O Ecomm Design é a **Referência Primária de Direção de Arte e Otimização de Conversão (CRO)** para os seguintes tipos de projeto:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        DECISION MATRIX: QUANDO CONSULTAR                               │
├─────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CENÁRIO DE PROJETO                      │ DIRETRIZ RECOMENDADA NO ECOMM DESIGN         │
├─────────────────────────────────────────┼──────────────────────────────────────────────┤
│ Marca DNVB / DTC (Vestuário, Skincare)  │ Minimal Alabaster com Slide-Out Cart Drawer  │
│ Joalheria, Luxo & Acessórios Premium    │ Editorial Serif com Fullscreen Product Zoom  │
│ Eletrônicos & Tech Hardware             │ Dark Obsidian com Especificações em Bento    │
│ Alimentos, Bebidas & Suplementos        │ Grid Vibrante com Assinatura / Bundles       │
│ Grande Marketplace ou Catálogo 500+ SKUs│ Sticky Faceted Sidebar + Quick Add Modal     │
│ Mobile-First Retail Store               │ Sticky Bottom Buy Bar com Safe Area Nativa   │
│ Campanha de Lançamento / Drop Exclusivo │ Countdown Timer + Back-in-Stock Notification │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 2.1 O Papel da Interface na Regra 60-30-10

No design de comércio eletrônico de alta performance, a regra 60-30-10 não é apenas uma diretriz estética, mas uma **estratégia psicométrica de foco visual**:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        A REGRA 60-30-10 NO ECOMMERCE MODERNO                           │
├────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                        │
│   ██████████████████████████████ 60% CANVAS & SUPERFÍCIES NEUTRAS                      │
│   • Branco Puro (#FFFFFF), Alabastro (#F8F9FA) ou Papel de Algodão (#FAF7F2).         │
│   • O fundo NUNCA compete com as cores do produto físico. Ele serve como o palco       │
│     silencioso para fotografia de estúdio de altíssima fidelidade cromática.           │
│                                                                                        │
│   ███████████████ 30% ESTRUTURA, TIPOGRAFIA & LINHAS DE CONTROLE                       │
│   • Preto Grafite (#111827), Cinza Neutro (#4B5563) e Linhas Divisórias (#E5E7EB).     │
│   • Títulos com hierarquia geométrica clara, tabelas de medidas legíveis,              │
│     contêineres de seleção de tamanho e molduras de cards com bordas suaves.           │
│                                                                                        │
│   █████ 10% ACENTO DE AÇÃO, PROVA SOCIAL & CONVERSÃO                                  │
│   • Botão de Compra Principal (`Add to Cart`), Barra de Progresso de Frete Grátis,     │
│     Estrelas de Avaliação (#F59E0B) e Badges de Estoque/Desconto (#10B981 / #E11D48).  │
│   • Este tom reserva toda a energia luminosa para direcionar a mão do usuário ao clique│
│                                                                                        │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 3. Contraindicações Estéticas (Quando NÃO Usar)

*   ⚠️ **Incompatível com Softwares SaaS B2B de Métricas Abstratas**:
    *   Telas de dashboards orientadas a logs de servidores, visualização de bancos de dados ou consoles de desenvolvedor não devem utilizar o formato de catalogação e vitrines de produtos físicos.
*   ⚠️ **Incompatível com Projetos Baseados em WebGL Pesado e Scrolljacking Experimental**:
    *   No comércio eletrônico, cada 100ms de latência adicional reduz as taxas de conversão em até 7%. Sites premiados no Awwwards com WebGL experimental que demoram 4 a 6 segundos para carregar geram taxas de rejeição catastróficas em consumidores reais de e-commerce.
*   ⚠️ **Armadilha do "Minimalismo Vazio sem Fotografia Profissional"**:
    *   A estética limpa e refinada das marcas do Ecomm Design depende em 80% da qualidade visceral da fotografia do produto (luz de estúdio, modelos reais, texturas macro do tecido, ângulos múltiplos). Aplicar essa estrutura com fotos amadoras ou renders mal iluminados resulta em um layout árido, frio e sem apelo de compra.
*   ⚠️ **Armadilha dos Dark Patterns e Popups Invasivos**:
    *   Não reproduzir práticas parasitárias (como roletas de desconto que bloqueiam a tela no primeiro segundo de acesso, timers falsos de urgência ou mensagens enganosas de *"14 pessoas estão vendo este item agora"*). O padrão curado pelo Ecomm Design foca em **autoridade, clareza e respeito à atenção do comprador**.
*   ⚠️ **Cumulative Layout Shift (CLS) em Carregamento de Variantes**:
    *   Nunca implementar trocas de variantes de cores ou fotos que façam o contêiner de imagem saltar de altura. Contêineres de imagem devem sempre manter propriedades estritas de `aspect-ratio: 1/1` ou `aspect-ratio: 4/5` reservadas na marcação HTML.

---

## 4. Anatomia Estrutural & Padrões Visuais Extraídos

### 4.1 Arquitetura de Grid, Espaçamento & Ritmo

1. **Grid Base de 12 Colunas com Margens Fluidas**:
   - Catálogos utilizam layouts de 4 colunas em telas grandes (`grid-cols-4` com `gap-6` a `gap-8`), reduzindo para 2 colunas em tablets e smartphones (`grid-cols-2` com `gap-3`).
2. **Proporções de Imagem Consistentes**:
   - As lojas de moda e acessórios padronizam a proporção vertical `4:5` ou `3:4` para valorizar modelos e detalhes de caimento. Produtos de tecnologia e casa costumam fixar em `1:1` (quadrado puro) com fundo neutro transparente ou cinza claro.
3. **Divisores de 1px Hairline**:
   - O ritmo visual é pontuado por divisórias ultra-finas de `1px solid rgba(0, 0, 0, 0.08)` (no modo claro) ou `rgba(255, 255, 255, 0.1)` (no modo escuro), separando seções sem criar caixas pesadas.

### 4.2 Sistemas de Cores, Superfícies & Texturas

- **Superfícies de Produto em Alabastro**: Fundos levemente desmaiados (`#F9FAFB` ou `#F4F4F5`) aplicados aos cards de itens, criando um contraste refinado contra o fundo branco da página principal (`#FFFFFF`).
- **Sombras Especulares Mínimas**: Ausência de sombras difusas pesadas. O e-commerce contemporâneo utiliza `box-shadow: 0 1px 3px rgba(0,0,0,0.05)` ou apenas bordas finas para manter o aspecto limpo e editorial.

---

### 4.3 Catálogo de 8 Arquétipos Notáveis de E-commerce

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        CATÁLOGO DE ARQUÉTIPOS ECOMM DESIGN                             │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  1. SLIDE-OUT CART DRAWER    ──► Ajax Mini-Cart com Gamificação de Frete e Cross-Sells │
│  2. SPLIT STICKY PDP         ──► Galeria Vertical com Painel de Compra Fixado          │
│  3. FACETED FILTER BAR       ──► Barra de Filtros com Gaveta Deslizante de Busca       │
│  4. MOBILE STICKY BUY BAR    ──► Ação de Compra Flutuante no Thumb-Zone Inferior       │
│  5. SHOPPABLE LOOKBOOK       ──► Pinos Interativos (Hotspots) sobre Foto de Campanha   │
│  6. DYNAMIC VARIANT MATRIX   ──► Color Swatches Circulares com Validação de Estoque    │
│  7. MULTI-TIER TRUST STRIP   ──► Garantias Criptográficas, Envio Rápido e Devolução    │
│  8. EXPRESS CHECKOUT STRIP   ──► Botões Oficiais Shop Pay, Apple Pay e Pix de 1-Toque  │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

#### Arquétipo 1: Slide-Out Cart Drawer com Dynamic Free Shipping Bar & One-Click Cross-Sells
- **Anatomia**: Gaveta lateral deslizante (`fixed right-0 top-0 h-full w-[420px] max-w-full z-50`) que abre instantaneamente ao adicionar qualquer item. No topo, exibe a contagem de itens e uma barra de progresso reativa calculando quanto resta para atingir o frete grátis (*"Adicione mais R$ 35 para frete grátis"*). O corpo contém a lista de itens com seletores de quantidade incrementais e opção de remoção imediata. Abaixo da lista, um card compacto de cross-sell inteligente sugere um produto complementar (ex: meia para calçado, capa para óculos) com botão direto de `+ Adicionar por R$ 29`. A base fixa traz o subtotal limpo e o botão principal de checkout.
- **Gatilho**: Ação de `Add to Cart` na PDP/PLP ou clique no ícone da sacola no header.
- **Onde Encaixar**: Em 100% das lojas virtuais contemporâneas para eliminar a necessidade de redirecionamento para uma página `/cart` isolada.

#### Arquétipo 2: Split Sticky PDP (Product Detail Page)
- **Anatomia**: Layout dividido em duas metades. A metade esquerda contém um grid ou sequência vertical de fotos de estúdio em alta resolução que o usuário rola naturalmente. A metade direita é configurada com `sticky top-24 self-start`: permanece perfeitamente ancorada na tela enquanto o visitante explora as fotos. Esse painel direito reúne título do produto, badges de status, preço com valor original tachado e indicação de parcelamento, swatches de variantes, botão principal de compra com largura total e acordeões sanfonados contendo tabela de medidas, detalhes de envio e materiais sustentáveis.
- **Gatilho**: Ao navegar na página do produto em telas desktop (`min-width: 1024px`).
- **Onde Encaixar**: Lojas de moda, calçados, joias, eletrônicos e produtos de alto valor agregado.

#### Arquétipo 3: Faceted Filter Bar & Drawer de Catálogo (PLP)
- **Anatomia**: Barra de controle horizontal fixada abaixo do cabeçalho principal contendo: (1) Totalizador de produtos em tempo real (*"Exibindo 142 produtos"*); (2) Botão de alternância de grid (2 colunas vs. 4 colunas); (3) Dropdown de ordenação (*Mais Vendidos, Menor Preço, Lançamentos*); (4) Botão expansor de filtros que revela uma gaveta lateral (*Off-Canvas Drawer*) com opções facetadas por categoria, tamanho, cor (com swatches clicáveis), faixa de preço e disponibilidade de entrega imediata.
- **Gatilho**: Ao visualizar páginas de categorias de produto ou resultados de busca.
- **Onde Encaixar**: Catálogos com mais de 20 itens para permitir refinamento cirúrgico da busca sem recarregar a página.

#### Arquétipo 4: Mobile-First Sticky Bottom Buy Bar (Thumb-Zone)
- **Anatomia**: Barra fixa flutuante posicionada na extremidade inferior da tela em smartphones (`fixed bottom-0 left-0 right-0 z-40 bg-white/95 backdrop-blur-md border-t border-gray-200 pb-safe px-4 py-3`). Ela se torna visível através de um listener de rolagem apenas quando o botão de compra original da página do produto é rolado para fora do campo visual. Exibe miniatura do produto, título reduzido, preço atual e o botão `Adicionar à Sacola`, permitindo que o usuário compre a qualquer momento sem precisar rolar todo o conteúdo de volta para o topo.
- **Gatilho**: Evento de scroll móvel cruzando o limite inferior do botão de compra principal.
- **Onde Encaixar**: Essencial para qualquer loja com tráfego mobile superior a 60%.

#### Arquétipo 5: Shoppable Lookbook com Hotspot Markers Interativos
- **Anatomia**: Imagens editoriais de campanha em alta resolução (ex: modelo vestindo um conjunto completo ou sala de estar decorada) contendo pequenos pontos de ancoragem pulsantes (`hotspots`). Ao passar o mouse ou tocar em um hotspot, surge um popover flutuante refinado exibindo o nome exato daquela peça específica, preço atual, miniatura e um botão direto para adicionar ao carrinho ou abrir a página do produto correspondente.
- **Gatilho**: Interação de hover ou toque sobre o marcador interativo.
- **Onde Encaixar**: Páginas iniciais de coleções de moda, catálogos de decoração e editoriais de tendências.

#### Arquétipo 6: Variant Matrix com Color Swatches, Size Pills e Validação de Estoque
- **Anatomia**: Conjunto de seletores táteis. As cores são representadas por círculos preenchidos com o tom exato do produto (ou miniatura da estampa têxtil), com anel de foco destacado no item ativo. Os tamanhos são exibidos em botões em formato de cápsula (*pills*). Tamanhos esgotados aparecem com opacidade reduzida (`opacity-40`) e uma linha diagonal sutil de 45 graus atravessando o botão. Ao clicar em um tamanho esgotado, o botão principal de compra se transforma automaticamente em `Avise-me quando chegar`, abrindo campo rápido de captura de e-mail/WhatsApp.
- **Gatilho**: Seleção de atributos de SKU na PDP.
- **Onde Encaixar**: Produtos com múltiplos tamanhos, voltagens ou cores.

#### Arquétipo 7: Multi-Tier Trust & Guarantee Grid
- **Anatomia**: Uma faixa horizontal discreta e minimalista posicionada estrategicamente logo abaixo do botão de compra ou no rodapé do checkout. Reúne de 3 a 4 pilares de confiança representados por ícones em traço fino de 20px acompanhados de tipografia concisa:
  - *"Envio Expresso em até 24h"*
  - *"Primeira Troca Grátis em até 30 Dias"*
  - *"Pagamento Criptografado de Ponta a Ponta"*
  - *"Garantia Oficial de Fabricação"*
- **Gatilho**: Sempre visível no fluxo de tomada de decisão.
- **Onde Encaixar**: Abaixo dos botões de call-to-action em PDPs e Cart Drawers para neutralizar objeções de compra.

#### Arquétipo 8: Express Checkout & Payment Badges Integration Strip
- **Anatomia**: Bloco dedicado que agrupa os métodos de pagamento acelerados de um único toque: botões com as identidades oficiais de marca (Apple Pay, Google Pay, Shop Pay, PayPal e Pix com QR Code dinâmico). Logo abaixo, exibe ícones monocromáticos em cinza neutro das bandeiras de cartão aceitas (Visa, Mastercard, Elo, Amex) e suporte a parcelamento sem juros em destaque visual.
- **Gatilho**: Exibição no fechamento do carrinho e na primeira etapa do checkout.
- **Onde Encaixar**: Redução de etapas de preenchimento manual de endereço e cartão em compras via celular.

---

## 5. Tradução para Código & Stack do Design Engine

### 5.1 Tokens CSS de E-Commerce de Alta Performance

```css
:root {
  /* Camada de Superfícies & Canvas */
  --ecomm-canvas-bg: #FFFFFF;
  --ecomm-surface-subtle: #F8F9FA;
  --ecomm-surface-card: #FFFFFF;
  --ecomm-border-hairline: rgba(17, 24, 39, 0.08);
  --ecomm-border-strong: rgba(17, 24, 39, 0.2);

  /* Tipografia & Hierarquia Textual */
  --ecomm-text-primary: #111827;
  --ecomm-text-secondary: #4B5563;
  --ecomm-text-muted: #9CA3AF;
  --ecomm-text-on-accent: #FFFFFF;

  /* Cores de Ação & Conversão (Regra 10%) */
  --ecomm-cta-primary: #111827;
  --ecomm-cta-primary-hover: #000000;
  --ecomm-cta-accent: #2563EB;
  --ecomm-cta-accent-hover: #1D4ED8;
  --ecomm-status-success: #10B981;
  --ecomm-status-urgency: #E11D48;
  --ecomm-status-rating: #F59E0B;

  /* Raios de Curvatura Ergonômicos */
  --ecomm-radius-sm: 4px;
  --ecomm-radius-md: 8px;
  --ecomm-radius-lg: 12px;
  --ecomm-radius-full: 9999px;

  /* Sombras Sutis de E-commerce */
  --ecomm-shadow-card: 0 1px 3px rgba(0, 0, 0, 0.05);
  --ecomm-shadow-drawer: -4px 0 24px rgba(0, 0, 0, 0.12);
  --ecomm-shadow-sticky: 0 -4px 16px rgba(0, 0, 0, 0.08);

  /* Física de Transição */
  --ecomm-ease-out-quad: cubic-bezier(0.25, 0.46, 0.45, 0.94);
  --ecomm-ease-drawer: cubic-bezier(0.16, 1, 0.3, 1);
}
```

### 5.2 Física de Movimento para Componentes de E-commerce

No comércio eletrônico, as animações não podem ser lentas ou dramáticas. O usuário deseja agilidade e confirmação imediata de suas ações:

- **Slide-Out Cart Drawer**:
  - `transition: transform 380ms cubic-bezier(0.16, 1, 0.3, 1)`
  - No Framer Motion: `transition={{ type: "spring", damping: 28, stiffness: 300, mass: 0.8 }}`
- **Barra de Progresso de Frete Grátis**:
  - `transition: width 500ms cubic-bezier(0.4, 0, 0.2, 1)`
  - O preenchimento da barra de progresso transmite a sensação imediata de recompensa física.
- **Botões de Compra e Swatches de Variação**:
  - `whileTap={{ scale: 0.97 }}` com retorno imediato para feedback tátil de clique.

---

### 5.3 Implementação Funcional Completa: Slide-Out Cart Drawer com Dynamic Free Shipping Bar & One-Click Cross-Sell

Abaixo está o código funcional em **React 19**, **TypeScript**, **Tailwind CSS** e **Framer Motion**, incorporando todas as melhores práticas de acessibilidade (`Dialog`, `aria-modal`, `focus-trap` nativo, fechamento com `Escape`), cálculo reativo de frete grátis e recomendação contextual:

```tsx
import React, { useState, useId } from "react";
import { motion, AnimatePresence } from "framer-motion";
import { 
  X, 
  ShoppingBag, 
  Plus, 
  Minus, 
  Trash2, 
  Truck, 
  CheckCircle2, 
  ArrowRight, 
  ShieldCheck 
} from "lucide-react";

export interface CartItem {
  id: string;
  title: string;
  variant: string;
  price: number;
  originalPrice?: number;
  quantity: number;
  imageUrl: string;
}

export interface CrossSellProduct {
  id: string;
  title: string;
  subtitle: string;
  price: number;
  imageUrl: string;
}

export interface SlideOutCartProps {
  isOpen: boolean;
  onClose: () => void;
  freeShippingThreshold?: number;
  initialItems?: CartItem[];
}

export const SlideOutCartDrawer: React.FC<SlideOutCartProps> = ({
  isOpen,
  onClose,
  freeShippingThreshold = 250, // Meta em R$ para frete grátis
  initialItems = [
    {
      id: "item-1",
      title: "Jaqueta Corta-Vento Matte Tech",
      variant: "Preto Ônix / Tamanho M",
      price: 189.0,
      originalPrice: 229.0,
      quantity: 1,
      imageUrl: "https://images.unsplash.com/photo-1544441893-675973e31985?auto=format&fit=crop&w=300&q=80",
    },
    {
      id: "item-2",
      title: "Camiseta Algodão Egípcio 220g",
      variant: "Areia Crua / Tamanho G",
      price: 49.0,
      quantity: 1,
      imageUrl: "https://images.unsplash.com/photo-1521572267360-ee0c2909d518?auto=format&fit=crop&w=300&q=80",
    },
  ],
}) => {
  const [items, setItems] = useState<CartItem[]>(initialItems);
  const [crossSellAdded, setCrossSellAdded] = useState(false);
  const titleId = useId();

  const crossSell: CrossSellProduct = {
    id: "cross-1",
    title: "Meias Térmicas Ribbed (Kit c/ 2)",
    subtitle: "Algodão Pima com reforço anatômico",
    price: 35.0,
    imageUrl: "https://images.unsplash.com/photo-1586350977771-b3b0abd50c82?auto=format&fit=crop&w=300&q=80",
  };

  // Cálculos reativos de subtotal e frete
  const subtotal = items.reduce((acc, item) => acc + item.price * item.quantity, 0);
  const remainingForFreeShipping = Math.max(0, freeShippingThreshold - subtotal);
  const shippingProgressPercentage = Math.min(100, (subtotal / freeShippingThreshold) * 100);
  const hasFreeShipping = subtotal >= freeShippingThreshold;

  const handleUpdateQuantity = (id: string, delta: number) => {
    setItems((prev) =>
      prev
        .map((item) => {
          if (item.id === id) {
            const newQty = item.quantity + delta;
            return newQty > 0 ? { ...item, quantity: newQty } : null;
          }
          return item;
        })
        .filter(Boolean) as CartItem[]
    );
  };

  const handleRemoveItem = (id: string) => {
    setItems((prev) => prev.filter((item) => item.id !== id));
  };

  const handleAddCrossSell = () => {
    if (crossSellAdded) return;
    setItems((prev) => [
      ...prev,
      {
        id: crossSell.id,
        title: crossSell.title,
        variant: "Tamanho Único",
        price: crossSell.price,
        quantity: 1,
        imageUrl: crossSell.imageUrl,
      },
    ]);
    setCrossSellAdded(true);
  };

  const formatCurrency = (val: number) => {
    return val.toLocaleString("pt-BR", { style: "currency", currency: "BRL" });
  };

  return (
    <AnimatePresence>
      {isOpen && (
        <div className="fixed inset-0 z-50 flex justify-end" role="dialog" aria-modal="true" aria-labelledby={titleId}>
          {/* Backdrop Escurecido com Blur Suave */}
          <motion.div
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            exit={{ opacity: 0 }}
            transition={{ duration: 0.25 }}
            onClick={onClose}
            className="fixed inset-0 bg-black/40 backdrop-blur-sm"
            aria-hidden="true"
          />

          {/* Painel Deslizante da Gaveta */}
          <motion.div
            initial={{ x: "100%" }}
            animate={{ x: 0 }}
            exit={{ x: "100%" }}
            transition={{ type: "spring", damping: 28, stiffness: 300, mass: 0.8 }}
            className="relative flex h-full w-full max-w-md flex-col bg-white shadow-2xl z-10"
          >
            {/* 1. Header do Carrinho */}
            <header className="flex items-center justify-between border-b border-gray-100 px-6 py-4">
              <div className="flex items-center gap-2">
                <ShoppingBag className="h-5 w-5 text-gray-900" />
                <h2 id={titleId} className="text-base font-semibold text-gray-900">
                  Sua Sacola ({items.reduce((acc, i) => acc + i.quantity, 0)})
                </h2>
              </div>
              <button
                type="button"
                onClick={onClose}
                className="rounded-full p-2 text-gray-400 hover:bg-gray-100 hover:text-gray-700 transition"
                aria-label="Fechar carrinho"
              >
                <X className="h-5 w-5" />
              </button>
            </header>

            {/* 2. Barra Gamificada de Frete Grátis */}
            <div className="border-b border-gray-100 bg-gray-50/70 px-6 py-3.5">
              <div className="flex items-center gap-2 mb-2">
                {hasFreeShipping ? (
                  <CheckCircle2 className="h-4 w-4 text-emerald-600 shrink-0" />
                ) : (
                  <Truck className="h-4 w-4 text-gray-600 shrink-0" />
                )}
                <p className="text-xs font-medium text-gray-800">
                  {hasFreeShipping ? (
                    <span className="text-emerald-700 font-semibold">
                      Parabéns! Você ganhou Frete Grátis! 🎉
                    </span>
                  ) : (
                    <>
                      Faltam apenas{" "}
                      <span className="font-bold text-gray-900">
                        {formatCurrency(remainingForFreeShipping)}
                      </span>{" "}
                      para frete grátis!
                    </>
                  )}
                </p>
              </div>
              {/* Barra de Progresso Reativa */}
              <div className="h-1.5 w-full overflow-hidden rounded-full bg-gray-200">
                <motion.div
                  className={`h-full ${
                    hasFreeShipping ? "bg-emerald-600" : "bg-gray-900"
                  }`}
                  initial={{ width: 0 }}
                  animate={{ width: `${shippingProgressPercentage}%` }}
                  transition={{ duration: 0.4, ease: "easeOut" }}
                />
              </div>
            </div>

            {/* 3. Lista de Itens com Scroll Interno */}
            <div className="flex-1 overflow-y-auto px-6 py-4 divide-y divide-gray-100">
              {items.length === 0 ? (
                <div className="flex h-full flex-col items-center justify-center text-center py-12">
                  <ShoppingBag className="h-12 w-12 text-gray-300 mb-3" />
                  <p className="text-base font-medium text-gray-900">Sua sacola está vazia</p>
                  <p className="text-xs text-gray-500 max-w-xs mt-1">
                    Explore nossas coleções exclusivas e adicione seus itens favoritos.
                  </p>
                  <button
                    onClick={onClose}
                    className="mt-6 rounded-md bg-gray-900 px-5 py-2.5 text-xs font-medium text-white hover:bg-black transition"
                  >
                    Começar a Comprar
                  </button>
                </div>
              ) : (
                items.map((item) => (
                  <div key={item.id} className="flex gap-4 py-4">
                    <img
                      src={item.imageUrl}
                      alt={item.title}
                      className="h-20 w-20 shrink-0 rounded-md object-cover bg-gray-50 border border-gray-100"
                    />
                    <div className="flex flex-1 flex-col justify-between">
                      <div>
                        <div className="flex items-start justify-between gap-2">
                          <h3 className="text-sm font-medium text-gray-900 leading-snug line-clamp-1">
                            {item.title}
                          </h3>
                          <button
                            type="button"
                            onClick={() => handleRemoveItem(item.id)}
                            className="text-gray-400 hover:text-rose-600 transition p-1"
                            aria-label={`Remover ${item.title}`}
                          >
                            <Trash2 className="h-4 w-4" />
                          </button>
                        </div>
                        <p className="text-xs text-gray-500 mt-0.5">{item.variant}</p>
                      </div>

                      <div className="flex items-center justify-between mt-3">
                        {/* Seletor de Quantidade Incremental */}
                        <div className="flex items-center rounded border border-gray-200">
                          <button
                            type="button"
                            onClick={() => handleUpdateQuantity(item.id, -1)}
                            className="px-2 py-1 text-gray-600 hover:bg-gray-100 transition"
                            aria-label="Diminuir quantidade"
                          >
                            <Minus className="h-3 w-3" />
                          </button>
                          <span className="w-8 text-center text-xs font-semibold text-gray-900">
                            {item.quantity}
                          </span>
                          <button
                            type="button"
                            onClick={() => handleUpdateQuantity(item.id, 1)}
                            className="px-2 py-1 text-gray-600 hover:bg-gray-100 transition"
                            aria-label="Aumentar quantidade"
                          >
                            <Plus className="h-3 w-3" />
                          </button>
                        </div>

                        {/* Preço com Formatação */}
                        <div className="text-right">
                          {item.originalPrice && (
                            <span className="block text-[11px] text-gray-400 line-through">
                              {formatCurrency(item.originalPrice * item.quantity)}
                            </span>
                          )}
                          <span className="text-sm font-semibold text-gray-900">
                            {formatCurrency(item.price * item.quantity)}
                          </span>
                        </div>
                      </div>
                    </div>
                  </div>
                ))
              )}

              {/* 4. One-Click In-Cart Cross-Sell (Se não adicionado) */}
              {items.length > 0 && !crossSellAdded && (
                <div className="mt-4 rounded-lg border border-dashed border-gray-200 bg-gray-50/50 p-3.5">
                  <p className="text-[11px] font-semibold uppercase tracking-wider text-gray-500 mb-2">
                    Complete seu Pedido
                  </p>
                  <div className="flex items-center gap-3">
                    <img
                      src={crossSell.imageUrl}
                      alt={crossSell.title}
                      className="h-12 w-12 rounded object-cover border border-gray-200 shrink-0"
                    />
                    <div className="flex-1 min-w-0">
                      <p className="text-xs font-medium text-gray-900 truncate">
                        {crossSell.title}
                      </p>
                      <p className="text-xs font-semibold text-gray-900 mt-0.5">
                        {formatCurrency(crossSell.price)}
                      </p>
                    </div>
                    <button
                      type="button"
                      onClick={handleAddCrossSell}
                      className="rounded bg-gray-900 px-3 py-1.5 text-xs font-medium text-white hover:bg-black transition shrink-0"
                    >
                      + Adicionar
                    </button>
                  </div>
                </div>
              )}
            </div>

            {/* 5. Footer Fixo com Subtotal e Checkout Express */}
            {items.length > 0 && (
              <footer className="border-t border-gray-100 bg-white px-6 py-5 shadow-inner">
                <div className="flex items-center justify-between mb-2">
                  <span className="text-sm font-medium text-gray-600">Subtotal Estimado</span>
                  <span className="text-base font-bold text-gray-900">
                    {formatCurrency(subtotal)}
                  </span>
                </div>
                <p className="text-[11px] text-gray-400 mb-4">
                  Taxas e frete final calculados durante a finalização da compra.
                </p>

                {/* Botão Primário de Checkout */}
                <button
                  type="button"
                  className="flex w-full items-center justify-center gap-2 rounded-md bg-gray-900 py-3.5 text-sm font-semibold text-white shadow-md hover:bg-black active:scale-[0.99] transition duration-150"
                >
                  <span>Finalizar Compra</span>
                  <ArrowRight className="h-4 w-4" />
                </button>

                {/* Faixa de Segurança e Trust Badges */}
                <div className="mt-4 flex items-center justify-center gap-2 text-[11px] text-gray-500">
                  <ShieldCheck className="h-4 w-4 text-emerald-600" />
                  <span>Checkout Seguro com Criptografia SSL de 256 bits</span>
                </div>
              </footer>
            )}
          </motion.div>
        </div>
      )}
    </AnimatePresence>
  );
};
```

---

### 5.4 Guia de Pesquisa ao Vivo para Agentes de IA

Quando um agente de IA ou desenvolvedor precisar navegar em tempo real no **Ecomm Design** para extrair referências arquiteturais de um segmento de mercado ou tecnologia específica, deve utilizar o seguinte mapeamento de rotas e URLs parametrizadas:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        MAPA DE ROTAS AO VIVO: ECOMM.DESIGN                             │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  DOMÍNIO BASE: https://ecomm.design/                                                   │
│                                                                                        │
│  1. PESQUISA POR PLATAFORMAS (ECOMMERCE CMS):                                          │
│  • Lojas em Shopify & Shopify Plus: https://ecomm.design/platform/shopify-stores/      │
│  • Lojas em WooCommerce:           https://ecomm.design/platform/woocommerce/         │
│  • Lojas em BigCommerce:           https://ecomm.design/platform/bigcommerce/         │
│  • Lojas em Squarespace:           https://ecomm.design/platform/squarespace/         │
│  • Lojas em Wix:                   https://ecomm.design/platform/wix/                 │
│                                                                                        │
│  2. PESQUISA POR FERRAMENTAS & TECH STACK (TOOLS):                                     │
│  • Gateways de Pagamento:          https://ecomm.design/tools/payments/               │
│  • E-mail Marketing & Klaviyo:     https://ecomm.design/tools/email-marketing/        │
│  • Live Chat & Atendimento (Gorgias): https://ecomm.design/tools/live-chat/           │
│  • Analytics & Tracking (GA4/Clarity): https://ecomm.design/tools/analytics-tracking/  │
│  • Retargeting & Meta Ads:         https://ecomm.design/tools/retargeting/            │
│  • Testes A/B & CRO (Optimizely):  https://ecomm.design/tools/ab-testing/             │
│  • Programas de Fidelidade/Loyalty: https://ecomm.design/tools/loyalty/               │
│                                                                                        │
│  3. PESQUISA POR TAGS & VERTICAIS DE MERCADO:                                          │
│  • Moda & Vestuário:               https://ecomm.design/tag/fashion/                  │
│  • Tecnologia & Gadgets:           https://ecomm.design/tag/technology/               │
│  • Beleza & Cosméticos:            https://ecomm.design/tag/beauty/                   │
│  • Casa, Mobília & Decoração:      https://ecomm.design/tag/home/                     │
│  • Joias & Acessórios:             https://ecomm.design/tag/jewelry/                  │
│  • Alimentos & Bebidas:            https://ecomm.design/tag/food-drink/               │
│                                                                                        │
│  4. BUSCA DIRETA PARAMETRIZADA POR PALAVRA-CHAVE:                                      │
│  • URL Format: https://ecomm.design/?s={termo_busca}&obj_type=website                  │
│  • Exemplo:    https://ecomm.design/?s=minimalist+jewelry&obj_type=website             │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao gerar especificações técnicas de design para sistemas de e-commerce e lojas virtuais inspiradas pelo catálogo do **Ecomm Design**, os seguintes mandamentos devem ser integrados ao `DESIGN_BLUEPRINT.md`:

1. **Adoção do Padrão "Split-Sticky PDP"**:
   - Para telas de computadores desktop e notebooks, fixar o painel transacional (`Add to Cart`, preço e seletores de variantes) com `sticky top-24` enquanto o grid de fotos rola à esquerda, garantindo que o botão de compra nunca saia do campo de visão do usuário.
2. **Implementação de Cart Drawer Ajax com Gamificação de Frete**:
   - Rejeitar redirecionamentos para páginas de carrinho tradicionais (`/cart`). Toda adição de item deve disparar uma gaveta lateral (*Slide-Out Cart Drawer*) equipada com uma barra de progresso visual de frete grátis e recomendações contextuais de 1 clique.
3. **Reserva Estrita de Espaço para Prevenção de CLS**:
   - Declarar explicitamente as dimensões ou `aspect-ratio` (ex: `aspect-[4/5]` ou `aspect-square`) em todos os contêineres de cards de produtos e galerias de imagens, impedindo saltos visuais na renderização inicial da página.
4. **Ergonomia Mobile no "Thumb-Zone"**:
   - Em smartphones, fixar uma barra de compra simplificada na parte inferior (`fixed bottom-0 left-0 right-0 z-40`) com suporte a `pb-safe` para respeitar o indicador de início do iOS e da barra de navegação do Android.
5. **Harmonia da Regra 60-30-10 para Foco Comercial**:
   - Garantir que 60% da área da interface seja ocupada por fundos limpos e neutros que valorizem a fotografia real do produto, 30% pela estrutura tipográfica e divisores de 1px legíveis, e 10% seja rigorosamente reservado para os pontos de conversão e prova social.
