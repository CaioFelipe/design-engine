---
id: "luxe-ui"
name: "Luxe UI"
url: "https://www.luxeui.com/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Dark Luxury Minimal", "Directional Lighting & Shines", "Precision Craft", "OKLCH Monochromatic Depth", "Spring Magnetic Haptics", "Variant-Driven Architecture"]
densidade_informacao: "Media"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Baixo (CSS/Headless) a Medio (Motion/Springs)"
stack_frameworks: ["React 19 / 18", "Next.js 15 (App Router)", "Tailwind CSS v4 & v3", "Motion (motion/react)", "Radix UI Primitives", "input-otp", "react-use-measure", "TypeScript"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "Plus Jakarta Sans", "SF Pro Display", "Söhne"]
  paletas_ideais: ["OKLCH Pure Pitch Black (#000000 / oklch(0.145 0 0))", "Obsidian & Deep Zinc Matrix", "Monochrome Metallic Silver & Platinum", "Luminous Cold White Glows"]
  combinacoes_recomendadas: ["shadcn/ui (fundação primária de formulários)", "Radix UI Primitives (acessibilidade headless)", "Magic UI / Cult UI (para partículas e grids complementares)", "Lucide React"]
  conflitos_esteticos: ["Neumorfismo pastel com relevos plásticos embaçados", "Corporate Memphis saturado com ilustrações planas coloridas", "Brutalismo Y2K caótico com bordas pretas grossas e cores fluorescentes ácidas", "Material Design 2 com elevações de sombra difusa e botões flutuantes FAB"]
---

# Luxe UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Luxe UI** (`luxeui.com`), concebido e desenvolvido pelo designer e engenheiro de software brasileiro **Gustavo Rodrigues** (@guhrodrrigues), é uma biblioteca de componentes de alto luxo visual para o ecossistema React, Next.js e Tailwind CSS. Enquanto grande parte das bibliotecas contemporâneas de código aberto se perde em demonstrações espalhafatosas de shaders 3D ou se restringe ao padrão minimalista utilitário desprovido de atmosfera, o Luxe UI define uma linguagem própria sintetizada em seu manifesto: *"Illuminate your applications with elegance and sophistication"*.

A assinatura visual do Luxe UI não reside no excesso de ornamentos, mas na **modulação cirúrgica da luz sobre superfícies escuras profundas**. Ele transforma elementos de interface corriqueiros — como botões, badges, inputs e cartões — em peças táteis que aparentam ter sido lapidadas em obsidiana polida, grafite metálico ou titânio aeroespacial.

Essa identidade única assenta-se sobre quatro pilares técnicos fundamentais:

### 1. A Engenharia da Luz Sutil (Shine 110º, Skewed Brightness & Conic Borders)
Ao contrário do clichê de degradês estáticos ou halos neon superdimensionados que poluem a tela, o Luxe UI desenvolveu uma suíte de técnicas de iluminação vetorial e rasterizada de alta performance:
- **Feixes Angulares Contínuos (`animate-shine`)**: Gradientes lineares projetados a 110 graus (`linear-gradient(110deg, #000000, 45%, #303030, 55%, #000000)`) com largura de 400% transladando em ciclos lentos de 6 segundos, gerando um brilho metálico que varre a superfície de modo orgânico e hipnótico.
- **Bordas em Rotação Contínua (`rotate-border`)**: O uso de um invólucro externo com padding milimétrico de 1 pixel (`p-px`) abrigando um elemento em giro infinito (`animate-[spin_2s_linear_infinite]`) preenchido por um `conic-gradient` de altíssimo contraste entre grafites e platinas (`#c2c2c2` a `#505050`), criando um contorno de luz líquida que contorna o perímetro com efeito de lente reflexiva.
- **Trajetórias Orbitais em Máscara CSS (`animated-border` via `offset-path`)**: Utilização pioneira de propriedades modernas de CSS Motion (`offset-path: rect(...)` e `offset-distance`) combinadas com máscaras de recorte (`[mask-clip:padding-box,border-box] [mask-composite:intersect]`), permitindo que um cometa de luz viaje ao longo do contorno arredondado do elemento sem vazar para o corpo do botão ou card.
- **Feixe Glitch com Inclinação Angular (`skew(-13deg) translateX`)**: Feixes luminosos translúcidos de 32px com desfoque gaussiano que cortam elementos em ângulos oblíquos de -13 graus, emulando flashes de refletores de estúdio.

### 2. Arquitetura Orientada a Variantes Unificadas (Luxe 2.0 Variant System)
A evolução do Luxe para a versão 2.0 eliminou a fragmentação comum em bibliotecas de animação (onde o desenvolvedor precisava importar `ButtonShine`, `ButtonBorder`, `ButtonMagnetic` como componentes separados). No Luxe UI, a API é centralizada e polimórfica:
```tsx
<Button variant="shine" isMagnetic>Action</Button>
<Button variant="rotate-border">Deploy</Button>
<Card variant="revealed-pointer">...</Card>
<Badge variant="animated-border">New Feature</Badge>
```
Essa padronização simplifica radicalmente a manutenção de Design Systems enterprise, permitindo alternar comportamentos e atmosferas visuais com uma única propriedade, preservando a semântica de acessibilidade e a herança de propriedades nativas do HTML.

### 3. Sensação Tátil e Física Háptica (Magnetic Springs & Clip-Path Reveals)
O Luxe UI complementa o acabamento visual com uma camada física tangível:
- **Propriedade Magnética (`isMagnetic`)**: Qualquer botão pode ser convertido em um alvo elástico que persegue o cursor do usuário quando o ponteiro invade seu raio de proximidade, sustentado por amortecimento de mola (`type: 'spring', damping: 15, stiffness: 150, mass: 0.1`).
- **Aberturas Cinemáticas via `clip-path`**: Menus dropdown e abas animadas abandonam simples transições de opacidade em favor de cortes geométricos calculados (`clip-path: inset(10% 50% 90% 50% round 12px)` para `inset(0% 0% 0% 0% round 12px)`), acompanhados por um escalonamento de desfoque progressivo (`blur(20px)` para `blur(0px)` com escala `0.3` para `1.0`), produzindo uma transição digna de interfaces cinematográficas de ficção científica de alta precisão.
- **Tabs em Clip-Path Contínuo**: No componente `AnimatedTabs`, em vez de renderizar um indicador flutuante com `layoutId` sujeito a glitches de repintura em telas complexas, o Luxe duplica o cabeçalho e aplica um recorte vetorial dinâmico de 60fps calculado via `container.style.clipPath = inset(0 right% 0 left% round 17px)` com `[transition:clip-path_0.25s_ease]`.

### 4. Design Tokens OKLCH Monocromáticos de Pureza Absoluta
O Luxe UI adota nativamente o espaço de cores **OKLCH** com Tailwind CSS v4 (`@theme inline`), garantindo linearidade perceptual de brilho e eliminando desvios cromáticos indesejados no modo escuro. O preto de fundo (`oklch(0.145 0 0)`) e as superfícies elevadas (`oklch(0.178 0 0)` e `oklch(0.205 0 0)`) mantêm saturação zero absoluta (`chroma: 0`), o que permite que os feixes luminosos contrastem sem reflexos esverdeados, arroxeados ou amarronzados típicos de paletas hexadecimais descuidadas.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados

1. **SaaS Developer Tools & Infraestrutura em Nuvem de Nova Geração**:
   Plataformas como Vercel, Supabase, Railway, Neon e Resend exigem uma estética sóbria, elegante e técnica. Os botões de brilho sutil, cartões com contorno de luz reativa ao cursor (`revealed-pointer`) e inputs com placeholders com blur conferem imediatamente o selo de produto premium e maduro.
2. **Fintechs Institucionais, WealthTech & Private Banking**:
   Sistemas de gestão de ativos, mesas de operações quantitativas e cartões de crédito corporativos pretos (estilo Black/Metal Card). A paleta de materiais nobres (obsidiana, titânio, platina) e a física de precisão transmitem estabilidade, exclusividade e segurança inquebrantável.
3. **Plataformas de Inteligência Artificial & Agentes Autônomos de Alto Valor**:
   Interfaces de modelos fundacionais e agentes cognitivos que precisam se distanciar dos layouts genéricos e demonstrar refinamento de ponta. O efeito `Text` variante `generate-effect` (com rotação 3D de caracteres e blur progressivo) e o `InputOTP` com indicadores deslizantes criam uma experiência de onboarding e autenticação impecável.
4. **Landing Pages de Alto Impacto para Produtos Enterprise (B2B)**:
   Páginas de apresentação de soluções com ticket médio elevado, onde o primeiro scroll do tomador de decisão técnica (CTO/VP de Engenharia) define o fechamento do contrato.
5. **Portfólios de Design Engineers e Creative Technologists**:
   Profissionais que desejam demonstrar domínio cirúrgico de micro-interações, Tailwind CSS avançado e CSS Motion sem parecer amadores ou dependentes de bibliotecas infladas.

### Papel no Ritmo Visual (A Regra 60-30-10)

Para manter o ar aristocrático e evitar que a interface se transforme em um espetáculo caótico de luzes piscantes, a biblioteca Luxe UI deve ser orquestrada sob a clássica proporção de equilíbrio:

- **60% — Fundação Neutra e Profunda (Base OKLCH Obsidian Dark & Tipografia)**:
  Superfícies em preto puro (`bg-main-background` / `oklch(0.145 0 0)`), com bordas finas monocromáticas (`border-border` / `oklch(0.26 0 0)`). A tipografia deve permanecer predominantemente Geist Sans ou Inter com hierarquias de cinza refinadas (`text-primary-foreground` para leitura nítida e `text-primary-muted` para metadados).
- **30% — Camada de Navegação & Micro-interações de Precisão (Componentes Estruturais Luxe)**:
  Controles de fluxo que respondem ao usuário com elegância sutil: o `AnimatedTabs` alternando sessões com corte milimétrico, o `DropdownMenu` revelando itens sob blur progressivo, o `Input` com placeholder que desliza com amortecimento de mola quando focado, o `Switch` com atrito limpo e o `NavigationMenu` com backdrop ativo deslizante via `layoutId="background"`.
- **10% — Efeitos Protagonistas e Feixes de Luz (Showstoppers Luminosos)**:
  Exclusivamente para pontos de conversão culminantes da página: **um único** `Button variant="rotate-border"` ou `variant="shine"` no Call to Action principal da Hero Section; cartões de precificação Tier Pro com `Card variant="revealed-pointer"`; ou um `Badge variant="animated-border"` anunciando a versão mais recente do software.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

- **Sistemas Operacionais Internos de Altíssima Densidade de Dados (Data Grids, ERPs, Faturamento em Massa)**:
  Em telas com planilhas de centenas de linhas contendo dezenas de botões e células interativas por centímetro quadrado, bordas rotativas e feixes luminosos contínuos competem com a leitura rápida dos números e causam sobrecarga cognitiva e processamento desnecessário na GPU do operador.
- **Interfaces Infantis, Jogos Casuais ou Produtos Populares Vistosos**:
  A linguagem do Luxe UI foi calibrada para a elegância austera e o luxo sombrio. Usá-la em produtos com cores quentes saturadas (amarelo canário, laranja cítrico, rosa choque) destrói a harmonia ótica e soa deslocado.
- **Aplicações com Restrições Críticas de Bateria e Hardware Ultra-Legado**:
  Embora o Luxe UI seja otimizado, o uso simultâneo de múltiplos loops de CSS (`animate-[spin_2s]`, gradientes cônicos de tamanho 1000% e `offset-path`) em aparelhos móveis de baixo custo pode aquecer a GPU e drenar a bateria se não houver parcimônia.

### ⚠️ Erros Comuns de Exagero (A Síndrome do "AI Slop" Luminoso)

1. **A Armadilha da "Las Vegas Strip"**:
   Colocar na mesma viewport um botão com `rotate-border`, outro com `shine`, três cartões com `animated-border` e badges piscando simultaneamente. Isso transforma um design de luxo em um clichê brega e confuso. Lembre-se: **se tudo brilha, nada se destaca**.
2. **Uso Indiscriminado de `isMagnetic` em Elementos Agrupados**:
   Ativar atração magnética em botões que ficam muito próximos uns dos outros (ex: botões "Salvar" e "Cancelar" lado a lado num modal pequeno). O cursor é puxado erraticamente entre os dois polos de força, frustrando a coordenação motora fina do usuário. Reserve o efeito magnético para botões isolados ou de ação primária heroica.
3. **Ignorar Preferências de Movimento Reduzido (`prefers-reduced-motion`)**:
   Componentes como `rotate-border` possuem loops contínuos de rotação. Sempre assegure que a diretiva `motion-safe:` do Tailwind CSS ou o hook `useReducedMotion()` do Framer Motion estejam ativos para cessar rotações contínuas para usuários com distúrbios vestibulares.
4. **Sobrecarga de Fontes Fantasiosas**:
   O design system do Luxe UI exige fontes limpas, geométricas ou neo-grotescas (Geist, Inter, Söhne). Aplicar fontes display ornamentadas, serifadas de jornal ou caligráficas junto com efeitos de feixe de luz quebra a coerência técnica do minimalismo dark craft.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão catalogados os 12 componentes essenciais que formam o núcleo da arquitetura do Luxe UI:

---

### 1. Button (`button.tsx`)
- **Anatomia Visual**: Botão multifacetado baseado em Radix Slot com suporte nativo a variantes exclusivas:
  - `shine`: Varredura luminosa contínua em ângulo de 110º com `animate-shine` e fundo estendido em 400%.
  - `rotate-border`: Borda externa de 1px com degradê cônico girando a 360º de forma perpétua sobre fundo com backdrop-blur.
  - `animated-border`: Ponto de luz orbital que percorre o perímetro do botão através de `offset-path: rect(...)`.
  - `glitch-brightness`: Efeito duplo com texto que rola verticalmente no hover (`TextGlitch`) e feixe de brilho angular de 32px com desfoque (`animate-brightness`).
  - `default` / `outline`: Acabamento sóbrio em cinza profundo com sombra interna milimétrica (`shadow-inner shadow-main-foreground/70`).
- **Gatilho de Interação**: Hover (deslocamento de texto, aceleração de brilho) e suporte opcional à prop `isMagnetic` (atração elástica física ao mouse via `useMagnetic`).
- **Onde Encaixar**: Botão principal da Hero Section, botão "Get Started / Deploy" na barra de navegação, botão de ação culminante em modais de pagamento.

---

### 2. Card (`card.tsx`)
- **Anatomia Visual**: Container modular com acabamento de precisão em 4 variantes:
  - `revealed-pointer`: Superfície em preto fosco envolta por borda de 1px com máscara reativa que ilumina um círculo radial suave (`radial-gradient(200px circle at mouseX mouseY)`) exatamente na posição em que o cursor passa, revelando a borda sob o ponteiro com transição suave.
  - `animated-border`: Cometa luminoso de 42px percorrendo o contorno do card em loop de 5 segundos via `offset-path`.
  - `shine`: Superfície inteira com textura metálica angular pulsante.
  - `default`: Painel minimalista com borda em `border-primary/10` e fundo `bg-main-background`.
- **Gatilho de Interação**: Movimento do ponteiro do mouse (`onMouseMove` capturando coordenadas locais e atualizando `useMotionValue`).
- **Onde Encaixar**: Cards de Bento Grid de recursos, cards de planos de precificação (especialmente destacando o plano "Enterprise"), painéis de métricas em dashboards de luxo.

---

### 3. Animated Tabs (`animated-tabs.tsx`)
- **Anatomia Visual**: Seletor de abas em formato pílula (`rounded-full`) com indicador de seleção de alta fidelidade visual. O diferencial técnico reside no fato de não utilizar translações com repintura de DOM: ele renderiza duas camadas completas idênticas e utiliza um recorte vetorial CSS dinâmico (`clip-path: inset(0 right% 0 left% round 17px)`) ajustado em milissegundos via JavaScript conforme a aba clicada.
- **Gatilho de Interação**: Clique na aba desejada, disparando o cálculo imediato de `offsetLeft` e `offsetWidth` com transição suave CSS `[transition:clip-path_0.25s_ease]`.
- **Onde Encaixar**: Alternadores de plano de pagamento (Mensal / Anual), alternador de visualização de código em blocos de documentação, seletor de filtros no topo de dashboards analíticos.

---

### 4. Dropdown Menu (`dropdown-menu.tsx`)
- **Anatomia Visual**: Menu suspenso com estética cinematográfica. Quando fechado, permanece comprimido numa fita horizontal oculta por máscara vetorial (`clip-path: inset(10% 50% 90% 50% round 12px)`). Ao ser ativado, o painel se expande com física de mola (`bounce: 0, duration: 0.5s`), enquanto cada item interno surge com efeito stagger em cascata de desfoque e escala (`opacity: 0, scale: 0.3, filter: blur(20px)` para `opacity: 1, scale: 1, filter: blur(0px)`).
- **Gatilho de Interação**: Clique no botão disparador (`DropdownMenuTrigger`), com rotação fluida de 180 graus do chevron indicativo.
- **Onde Encaixar**: Menu de perfil de usuário na Navbar, seletores de organização/workspace, menus contextuais de ações rápidas.

---

### 5. Multi-Step Modal (`multi-step-modal.tsx`)
- **Anatomia Visual**: Modal de múltiplos passos com integração profunda entre Radix Dialog e Framer Motion. Possui detecção automática de altura em tempo real através do hook `useMeasure`, adaptando a altura do container dinamicamente sem solavancos conforme o conteúdo de cada etapa se altera. As etapas deslizam lateralmente com respeito à direção de navegação (`direction: 1` para avançar, `-1` para recuar).
- **Gatilho de Interação**: Botões "Back" e "Continue" no rodapé fixo, orquestrados por `MotionConfig` com molas calibradas (`type: 'spring', duration: 0.6, bounce: 0`).
- **Onde Encaixar**: Fluxos de onboarding guiado, assistentes de configuração de API / chaves de acesso, formulários de migração de banco de dados e checkout estruturado.

---

### 6. Input OTP (`input-otp.tsx`)
- **Anatomia Visual**: Campo de inserção de código de verificação one-time password (OTP) dividido em grupos de slots com separador em pílula (`InputOTPSeparator`). Cada slot exibe bordas nítidas em cinza grafite, cursor piscante simulado (`FakeCaret`) com animação CSS calibrada e um anel de foco dinâmico que desliza entre os slots via `layoutId="indicator"`.
- **Gatilho de Interação**: Digitação numérica direta; cada caractere inserido sobe verticalmente com efeito de mola rápida (`initial: { opacity: 0.2, y: 20 }` para `{ opacity: 1, y: 0 }` em 90ms).
- **Onde Encaixar**: Telas de login com autenticação de dois fatores (2FA), validação de e-mail de segurança, confirmação de transferências bancárias ou chaves de API.

---

### 7. Text (`text.tsx`)
- **Anatomia Visual**: Primitiva tipográfica com seis variantes de acabamento e micro-animação:
  - `shine`: Texto metálico com gradiente de luz refletida que se desloca horizontalmente em loop infinito.
  - `generate-effect`: Texto com revelação caractere a caractere, onde cada letra surge rotacionando em torno do eixo X (`rotateX: 90` para `0`) com desfoque saindo de 4px para 0px e delay escalonado de 15ms.
  - `hover-enter`: Efeito de letras rolantes bipartidas em duas linhas sobrepostas que sobem sincronizadas no hover com delay sequencial de 25ms.
  - `glitch`: Rolagem vertical completa de linha de texto duplicada no hover.
  - `hover-decoration`: Linha sublinhada minimalista que cresce da direita para a esquerda e recua no sentido inverso com alternância de origem geométrica.
  - `shake`: Micro-vibração de erro suave ao passar o cursor.
- **Gatilho de Interação**: Entrada na viewport (`whileInView` para `generate-effect`), hover do cursor (`hover-enter`, `glitch`) ou auto-play infinito (`shine`).
- **Onde Encaixar**: Título da Hero Section, cabeçalhos de seções de recursos, links de navegação secundários e feedbacks de digitação em copilotos.

---

### 8. Input (`input.tsx`)
- **Anatomia Visual**: Campo de formulário de perfil esbelto (`h-11`) em fundo `bg-main-secondary`, com bordas sutis e foco luminoso de baixa opacidade (`focus-within:border-primary/20`). A grande assinatura visual é o **Animated Placeholder**: o texto de espaço reservado não apenas desaparece bruscamente, mas flutua e se dissolve lateralmente com desfoque progressivo (`x: 28, opacity: 0, filter: blur(var(--blur-xs))`) sustentado por `AnimatePresence mode="popLayout"`.
- **Gatilho de Interação**: Digitação do usuário (detecção de comprimento do texto alternando o estado de `idle` para `filled` instantaneamente).
- **Onde Encaixar**: Barra de pesquisa global, inputs de e-mail de lista de espera na Hero, campos de login e formulários de contato de luxo.

---

### 9. Navigation Menu (`navigation-menu.tsx`)
- **Anatomia Visual**: Menu de navegação horizontal com arquitetura Radix UI e abas suspensas. Ao passar o mouse sobre os itens de submenu (`NavigationMenuContentItem`), um indicador de fundo cinza translúcido (`bg-main-foreground`) desliza suavemente sob os itens utilizando `layoutId="background"`, eliminando os saltos visuais bruscos de hovers tradicionais.
- **Gatilho de Interação**: Hover e foco de teclado nos itens, com transições condicionais que respeitam automaticamente `useReducedMotion()`.
- **Onde Encaixar**: Navbar principal de landing pages institucionais e portais corporativos complexos.

---

### 10. Badge (`badge.tsx`)
- **Anatomia Visual**: Pílula indicativa de status micro-compacta (`text-xs`) com suporte a variantes idênticas às do botão: `rotate-border`, `animated-border` (com mini-cometa de luz circulando a borda), `shine`, `success` e `destructive`.
- **Gatilho de Interação**: Exibição estática com animações contínuas sutis de iluminação de borda.
- **Onde Encaixar**: Anúncio de novidades ("New Feature", "v2.0 Released") ancorado acima do título da Hero Section, tags de status de servidores em dashboards ("Operational"), selos de versão em documentações.

---

### 11. Switch (`switch.tsx`)
- **Anatomia Visual**: Alternador de estado binário (liga/desliga) com raio pílula perfeito (`h-6 w-10.5`), construído sobre o Radix Switch. O trilho utiliza a tonalidade cinza neutra de alta densidade `bg-main-foreground` que transita suavemente para `bg-primary` quando ativo. O botão esférico interno (`RadixSwitch.Thumb`) translada 18px (`translate-x-4.5`) com amortecimento de atrito mecânico.
- **Gatilho de Interação**: Clique ou tecla de espaço, com feedback tátil de deslocamento instantâneo.
- **Onde Encaixar**: Painéis de preferências de usuário, alternador de modo Dark/Light, toggles de notificações e configurações de privacidade.

---

### 12. Tooltip (`tooltip.tsx`)
- **Anatomia Visual**: Balão de dica flutuante com raio de curvatura de 8px, borda refinada em cinza escuro e espaçamento de deslocamento preciso de 6px (`sideOffset = 6`). Apresenta micro-animações de entrada e saída com zoom leve (`motion-safe:zoom-in-95` para `100%`) e deslocamento direcional de 2 pixels de acordo com a face de ancoragem (`slide-in-from-bottom-2` para topo, etc.).
- **Gatilho de Interação**: Hover com atraso zero (`delayDuration = 0`), ideal para interfaces técnicas onde a agilidade de leitura é primordial.
- **Onde Encaixar**: Ícones de barras de ferramentas, botões de ação com apenas ícones (ex: copiar código, tela cheia, configurações), badges de status com detalhes adicionais.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Pacotes

O ecossistema Luxe UI é construído sobre a versão mais recente do ecossistema React. Para incorporar os componentes em um projeto Next.js (App Router) ou Vite com React 19/18 e Tailwind CSS v4 ou v3, execute:

```bash
npm install motion/react @radix-ui/react-slot @radix-ui/react-dialog @radix-ui/react-navigation-menu @radix-ui/react-tooltip @radix-ui/react-accordion @radix-ui/react-switch @radix-ui/react-avatar input-otp react-use-measure clsx tailwind-merge
```

### O CLI Oficial Luxe

O Luxe UI possui seu próprio utilitário de linha de comando para configuração de tokens e injeção direta de componentes no projeto:

```bash
# Inicialização do projeto (cria utils, instala dependências e configura variáveis)
npx luxe init

# Adição seletiva de componentes individuais
npx luxe add button card animated-tabs dropdown-menu multi-step-modal
```

### Tokens OKLCH & Keyframes CSS no Tailwind CSS v4 (`luxe.css`)

Para que os componentes do Luxe UI operem com a fidelidade cromática e os ciclos de iluminação nativos, importe as definições de variáveis OKLCH e os keyframes no seu arquivo CSS global (ex: `app/globals.css` ou `styles/luxe.css`):

```css
@import "tailwindcss";

:root {
  --main: oklch(0.97 0 0);
  --main-secondary: oklch(97% 0 0);
  --main-foreground: oklch(0.925 0 0);
  --main-muted: oklch(0.96 0 0);
  --main-background: oklch(0.97 0 0);
  --main-invert: oklch(0.205 0 0);

  --primary: oklch(0 0 0);
  --primary-invert: oklch(1 0 0);
  --primary-foreground: oklch(37.1% 0 0);
  --primary-muted: oklch(0.556 0 0);

  --border: oklch(0.885 0 0);
}

.dark {
  --main: oklch(0.178 0 0);
  --main-secondary: oklch(0.205 0 0);
  --main-foreground: oklch(0.269 0 0);
  --main-muted: oklch(0.168 0 0);
  --main-background: oklch(0.145 0 0);
  --main-invert: oklch(0.8 0 0);

  --primary: oklch(1 0 0);
  --primary-invert: oklch(0 0 0);
  --primary-foreground: oklch(0.97 0 0);
  --primary-muted: oklch(0.708 0 0);

  --border: oklch(0.26 0 0);
}

@theme inline {
  --color-main: var(--main);
  --color-main-secondary: var(--main-secondary);
  --color-main-foreground: var(--main-foreground);
  --color-main-muted: var(--main-muted);
  --color-main-background: var(--main-background);
  --color-main-invert: var(--main-invert);

  --color-primary: var(--primary);
  --color-primary-foreground: var(--primary-foreground);
  --color-primary-muted: var(--primary-muted);
  --color-primary-invert: var(--primary-invert);

  --color-border: var(--border);

  --animate-shine: shine 6s linear infinite;
  --animate-text-gradient: text-gradient 2s linear infinite;
  --animate-text-shake: text-shake 1s ease 1;
  --animate-brightness: brightness 2.2s linear infinite;
  --animate-caret-blink: caret-blink 1.25s ease-out infinite;

  @keyframes caret-blink {
    0%, 70%, 100% { opacity: 1; }
    20%, 50% { opacity: 0; }
  }

  @keyframes shine {
    from { background-position: 0 0; }
    to { background-position: -400% 0; }
  }

  @keyframes text-gradient {
    to { background-position: 200% center; }
  }

  @keyframes text-shake {
    15% { transform: translateX(5px); }
    30% { transform: translateX(-5px); }
    50% { transform: translateX(3px); }
    80% { transform: translateX(2px); }
    100% { transform: translateX(0); }
  }

  @keyframes brightness {
    0% { transform: skew(-13deg) translateX(-100%); }
    100% { transform: skew(-13deg) translateX(100%); }
  }
}
```

---

### Física de Movimento e Transições

O Luxe UI baseia suas dinâmicas físicas em configurações precisas de molas (`spring`) e curvas contínuas:

1. **Física Magnética (`useMagnetic` do Button)**:
   - `type`: `'spring'`
   - `damping`: `15` (resistência moderada à oscilação)
   - `stiffness`: `150` (rigidez suave que atrai com gravidade palpável)
   - `mass`: `0.1` (massa ínfima, permitindo resposta imediata ao movimento rápido do mouse)

2. **Física do Modal & Multi-Step Transitions (`MultiStepModal`)**:
   - `type`: `'spring'`
   - `duration`: `0.6s`
   - `bounce`: `0` (amortecimento crítico perfeito, sem ressaltos, conferindo tom executivo sóbrio)

3. **Física da Revelação de Menus (`DropdownMenu`)**:
   - `type`: `'spring'`
   - `duration`: `0.5s`
   - `bounce`: `0`
   - `delayChildren`: `0.15s` (pausa microscópica antes de iniciar o surgimento dos itens)
   - `staggerChildren`: `0.1s` (deslocamento progressivo em cascata de cada item da lista)

---

### Receitas de Código Completas e Funcionais

#### Receita 1: Botão de Luxo Multidimensional (Rotate Border + Efeito Magnético)

Este componente reproduz o ápice do design craft do Luxe UI: uma moldura de luz cônica rotativa em 360º abraçando um núcleo de vidro escuro fosco com resposta física magnética ao cursor:

```tsx
'use client'

import React, { useRef, useState } from 'react'
import { motion } from 'motion/react'
import { clsx, type ClassValue } from 'clsx'
import { twMerge } from 'tailwind-merge'

function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs))
}

interface LuxeRotateButtonProps extends React.ComponentProps<'button'> {
  isMagnetic?: boolean
  children: React.ReactNode
}

export function LuxeRotateButton({
  isMagnetic = true,
  className,
  children,
  ...props
}: LuxeRotateButtonProps) {
  const content = (
    <button
      {...props}
      className={cn(
        'group relative inline-flex items-center justify-center overflow-hidden rounded-xl p-px font-medium text-sm outline-none',
        'focus-visible:ring-1 focus-visible:ring-white/40 active:scale-[0.98] transition-transform duration-150',
        className
      )}
    >
      {/* Feixe cônico em rotação perpétua */}
      <span
        aria-hidden="true"
        className={cn(
          'absolute inset-[-1000%] animate-[spin_2.5s_linear_infinite]',
          'bg-[conic-gradient(from_90deg_at_50%_50%,#4e4e4e_0%,#d4d4d4_50%,#414141_100%)]',
          'dark:bg-[conic-gradient(from_90deg_at_50%_50%,#202020_0%,#ffffff_50%,#202020_100%)]'
        )}
      />

      {/* Superfície interna acetinada com backdrop blur */}
      <span
        className={cn(
          'inline-flex size-full items-center justify-center gap-2 rounded-[11px] px-5 py-2.5',
          'bg-neutral-950 text-neutral-200 backdrop-blur-3xl transition-colors',
          'group-hover:bg-neutral-900 group-hover:text-white'
        )}
      >
        {children}
      </span>
    </button>
  )

  if (isMagnetic) {
    return <MagneticWrapper>{content}</MagneticWrapper>
  }

  return content
}

function MagneticWrapper({ children }: { children: React.ReactNode }) {
  const ref = useRef<HTMLDivElement>(null)
  const [position, setPosition] = useState({ x: 0, y: 0 })

  function handleMouseMove(e: React.MouseEvent) {
    if (!ref.current) return
    const { clientX, clientY } = e
    const { height, width, left, top } = ref.current.getBoundingClientRect()
    const middleX = clientX - (left + width / 2)
    const middleY = clientY - (top + height / 2)
    setPosition({ x: middleX * 0.35, y: middleY * 0.35 })
  }

  function handleMouseLeave() {
    setPosition({ x: 0, y: 0 })
  }

  return (
    <motion.div
      ref={ref}
      onMouseMove={handleMouseMove}
      onMouseLeave={handleMouseLeave}
      animate={{ x: position.x, y: position.y }}
      transition={{
        type: 'spring',
        damping: 15,
        stiffness: 150,
        mass: 0.1,
      }}
      className="inline-block"
    >
      {children}
    </motion.div>
  )
}
```

---

#### Receita 2: O Card Revealed Pointer (Spotlight Reativo ao Mouse)

Este componente demonstra a assinatura de cartões do Luxe UI: a borda externa e a superfície respondem em tempo real ao movimento do mouse, acendendo um halo de luz difusa exatamente sob a ponta da seta:

```tsx
'use client'

import React from 'react'
import { motion, useMotionTemplate, useMotionValue } from 'motion/react'
import { clsx, type ClassValue } from 'clsx'
import { twMerge } from 'tailwind-merge'

function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs))
}

interface LuxeRevealedCardProps extends React.ComponentProps<'div'> {
  title: string
  description: string
  badgeText?: string
}

export function LuxeRevealedCard({
  title,
  description,
  badgeText,
  className,
  children,
  ...props
}: LuxeRevealedCardProps) {
  const mouseX = useMotionValue(0)
  const mouseY = useMotionValue(0)

  function handleMouseMove(e: React.MouseEvent<HTMLDivElement>) {
    const { left, top } = e.currentTarget.getBoundingClientRect()
    mouseX.set(e.clientX - left)
    mouseY.set(e.clientY - top)
  }

  return (
    <div
      onMouseMove={handleMouseMove}
      className={cn(
        'group relative overflow-hidden rounded-2xl bg-neutral-800/40 p-px transition-colors duration-300 hover:bg-neutral-800/80',
        className
      )}
      {...props}
    >
      {/* Halo de luz reativo que acende a borda no ponto de contato */}
      <motion.div
        className="pointer-events-none absolute -inset-px rounded-2xl opacity-0 transition-opacity duration-300 group-hover:opacity-100"
        style={{
          background: useMotionTemplate`radial-gradient(220px circle at ${mouseX}px ${mouseY}px, rgba(255,255,255,0.18), transparent 80%)`,
        }}
      />

      {/* Corpo principal do cartão em preto fosco */}
      <div className="relative flex h-full flex-col justify-between rounded-[15px] bg-[#0c0c0c] p-6 text-neutral-300">
        <div>
          {badgeText && (
            <span className="mb-4 inline-flex items-center rounded-full border border-neutral-800 bg-neutral-900/80 px-2.5 py-0.5 font-medium text-[11px] text-neutral-400">
              {badgeText}
            </span>
          )}
          <h3 className="font-semibold text-lg text-white tracking-tight">
            {title}
          </h3>
          <p className="mt-2 text-neutral-400 text-sm leading-relaxed">
            {description}
          </p>
        </div>

        {children && <div className="mt-6">{children}</div>}
      </div>
    </div>
  )
}
```

---

#### Receita 3: AnimatedTabs com Recorte Vetorial `clip-path` (60 FPS)

Implementação exata da mecânica de abas em alta fidelidade do Luxe UI, garantindo performance pura sem layout recalculado:

```tsx
'use client'

import React, { useEffect, useRef, useState } from 'react'

interface LuxeAnimatedTabsProps {
  tabs: string[]
  onChange?: (activeTab: string) => void
}

export function LuxeAnimatedTabs({ tabs, onChange }: LuxeAnimatedTabsProps) {
  const [activeTab, setActiveTab] = useState(tabs[0])

  const containerRef = useRef<HTMLDivElement>(null)
  const activeTabRef = useRef<HTMLButtonElement>(null)

  useEffect(() => {
    const container = containerRef.current
    const activeElement = activeTabRef.current

    if (container && activeElement) {
      const { offsetLeft, offsetWidth } = activeElement
      const clipLeft = offsetLeft
      const clipRight = offsetLeft + offsetWidth

      const leftPercent = Number(((clipLeft / container.offsetWidth) * 100).toFixed(2))
      const rightPercent = Number((100 - (clipRight / container.offsetWidth) * 100).toFixed(2))

      container.style.clipPath = `inset(0 ${rightPercent}% 0 ${leftPercent}% round 9999px)`
    }

    onChange?.(activeTab)
  }, [activeTab, onChange])

  return (
    <div className="relative mx-auto flex w-fit items-center rounded-full border border-neutral-800 bg-neutral-950 p-1">
      {/* Camada ativa recortada dinamicamente via clip-path */}
      <div
        ref={containerRef}
        aria-hidden="true"
        className="pointer-events-none absolute inset-0 z-10 w-full overflow-hidden transition-[clip-path] duration-300 ease-out"
      >
        <div className="flex w-full justify-center bg-white">
          {tabs.map((tab, idx) => (
            <button
              key={idx}
              type="button"
              tabIndex={-1}
              className="flex h-8 items-center px-4 font-semibold text-black text-xs tracking-wide"
            >
              {tab}
            </button>
          ))}
        </div>
      </div>

      {/* Camada base de botões estáticos */}
      <div className="relative flex w-full justify-center">
        {tabs.map((tab, idx) => {
          const isActive = activeTab === tab
          return (
            <button
              key={idx}
              type="button"
              ref={isActive ? activeTabRef : null}
              onClick={() => setActiveTab(tab)}
              className="flex h-8 items-center rounded-full px-4 font-medium text-neutral-400 text-xs tracking-wide transition-colors hover:text-neutral-200"
            >
              {tab}
            </button>
          )
        })}
      </div>
    </div>
  )
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir o documento de especificação técnica e arquitetura de interface (`DESIGN_BLUEPRINT.md`) para projetos que incorporem o Luxe UI, a Inteligência Artificial deve seguir estritamente as diretrizes abaixo:

1. **Declaração Formal de Estilo**:
   Defina o arquétipo visual do projeto como:
   `"Estética Dark Luxury Minimal / Craft Precision baseada em Luxe UI e tokens monocromáticos OKLCH"`.
2. **Orquestração de Iluminação no Hero Block**:
   - Determine **apenas um elemento** com animação contínua de luz visível na primeira tela (`Button variant="rotate-border"` no CTA ou `Badge variant="animated-border"` no anúncio).
   - O título principal (`H1`) deve utilizar o degradê metálico suave em tons de prata/grafite (`Text variant="shine"` ou gradiente `from-white via-neutral-200 to-neutral-500 bg-clip-text text-transparent`).
3. **Mapeamento de Componentes por Função**:
   - **Navegação Superior**: `NavigationMenu` do Luxe com backdrop ativo via `layoutId="background"`.
   - **Alternadores de Modo/Período**: `LuxeAnimatedTabs` em substituição aos Tabs pesados do Radix tradicional.
   - **Cartões de Destaque Técnico**: `LuxeRevealedCard` com spotlight sensível ao cursor.
   - **Campos de Verificação**: `InputOTP` com indicadores deslizantes e animação de mola vertical a cada dígito.
   - **Fluxos Modais Guiados**: `MultiStepModal` com auto-resize via `react-use-measure`.
4. **Tratamento de Acessibilidade Obrigatório**:
   - Sempre declare o suporte explícito a `prefers-reduced-motion`. O blueprint deve instruir o descarte de loops de rotação de borda (`animate-[spin]`) e substituição por bordas sutis estáticas de 1px (`border-neutral-700`) quando o usuário sinalizar restrição de movimento.
5. **Configuração de Tailwind CSS**:
   - Exija a importação dos keyframes `@keyframes shine`, `@keyframes brightness` e `@keyframes caret-blink` no arquivo CSS mestre, garantindo compatibilidade direta com Tailwind CSS v4 (`@theme inline`).
