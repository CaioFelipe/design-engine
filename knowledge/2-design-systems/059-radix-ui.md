---
id: "radix-ui"
name: "Radix UI"
url: "https://www.radix-ui.com/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Headless WAI-ARIA Primitives", "Perceptually Calibrated 12-Step Colors", "Polymorphic Slot Composition (asChild)", "WorkOS Enterprise Craft & macOS Density", "State-Driven Attribute Styling (data-state)"]
densidade_informacao: "Flexivel"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS/Headless)"
stack_frameworks: ["React 19 / 18", "Next.js (App Router / RSC)", "Radix Primitives (@radix-ui/react-*)", "Radix Themes (@radix-ui/themes)", "Radix Colors (@radix-ui/colors)", "Radix Icons (@radix-ui/react-icons)", "Tailwind CSS v4 & v3", "TypeScript", "Framer Motion"]
compatibilidade:
  fontes_ideais: ["Inter", "Geist Sans", "SF Pro Text / Display", "Plus Jakarta Sans", "JetBrains Mono"]
  paletas_ideais: ["Radix 12-Step Scales (Slate, Iris, Jade, Ruby, Amber)", "Display P3 Wide Gamut Accents", "Translucent Glassmorphic Frost & Dark Canvas", "Enterprise High-Contrast Monochromes"]
  combinacoes_recomendadas: ["shadcn/ui", "Tailwind CSS", "Kibo UI", "Tremor", "Vaul", "Sonner", "cmdk", "Framer Motion"]
  conflitos_esteticos: ["Neumorfismo skeuomórfico pesado com relevos plásticos", "Material Design 2 com elevações e sombras excessivas de cor primária", "Brutalismo destrutivo caótico sem alinhamento e sem estados de foco claros"]
---

# Radix UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Radix UI** (`radix-ui.com`) é a infraestrutura de engenharia e a pedra fundamental sobre a qual foi erguida a era moderna das interfaces de usuário em React. Desenvolvido originalmente pela equipe da **Modulz** (liderada por Pedro Duarte, Benoit Grelard, Colm Tuite e Stephen Haney) e adquirido em 2022 pela **WorkOS** (fundada por Michael Grinich), o Radix não é apenas uma biblioteca; é o ecossistema que estabeleceu os padrões contemporâneos de arquitetura headless, acessibilidade nativa WAI-ARIA, composição polimórfica e calibração colorimétrica perceptual.

O ecossistema Radix estrutura-se sobre uma tríade técnica coesa:
1. **Radix Primitives**: Conjunto de componentes desprovidos de estilos (100% headless), focados em lógica de estado complexa, gerenciamento de foco por teclado (*roving tabindex*), armadilhas de foco (*focus trapping*), posicionamento em camadas com colisão inteligente (*floating / collision detection*) e conformidade integral com as especificações W3C WAI-ARIA. É a fundação direta de frameworks populares globais, incluindo `shadcn/ui`, `kibo-ui` e dezenas de design systems corporativos.
2. **Radix Themes**: Biblioteca de componentes pré-estilizada e opinativa que traduz a ergonomia visual do macOS e iPadOS para a web enterprise moderna. Focada em velocidade de entrega, traz layout primitives (`Box`, `Flex`, `Grid`, `Container`, `Section`), componentes de densidade elevada (`DataList`, `SegmentedControl`, `Callout`) e superfícies translúcidas com desfoque de fundo (*backdrop blur*).
3. **Radix Colors**: Um sistema matemático de 12 passos cromáticos projetado especificamente para interfaces digitais, calibrado perceptualmente com suporte ao espaço de cores de ampla gama **Display-P3**, gerando paridade óptica impecável entre os modos Claro e Escuro e fornecendo variantes alfa (`a1` a `a12`) para sobreposições realistas sem perda de croma.

```
+-------------------------------------------------------------------------+
|                              RADIX UI                                   |
+------------------------------------+------------------------------------+
|         RADIX PRIMITIVES           |            RADIX THEMES            |
|  - 100% Headless & Desestilizado   |  - Componentes Pré-estilizados     |
|  - WAI-ARIA & Roving Tabindex      |  - Layout Primitives (Flex, Grid)  |
|  - Prop `asChild` & Radix Slot     |  - Densidade & Scaling (90%-110%)  |
|  - Atributos `data-state` / `side` |  - Ergonomia Tátil macOS / WorkOS  |
+------------------------------------+------------------------------------+
|                            RADIX COLORS                                 |
|  - Escala Funcional de 12 Passos (Steps 1 a 12)                        |
|  - Suporte Nativo Display-P3 & Variantes Alfa (a1-a12)                  |
|  - Simetria Óptica e Perceptual Light/Dark Mode                        |
+-------------------------------------------------------------------------+
```

---

### A Tríade da Inovação Técnica: Como o Radix Redefiniu a Web

#### 1. A Invenção do Padrão `Slot` e a Revolução da Prop `asChild`
Antes do Radix, os componentes React tentavam resolver polimorfismo via a prop `as` (ex: `<Button as="a" href="...">` ou `<Button as={Link} to="...">`). Esse modelo histórico gerava graves problemas:
- **Colapso de Tipagem no TypeScript**: A inferência genérica das props do elemento repassado tornava o autocomplete lento e gerava tipos complexos demais (`PolymorphicComponentPropsWithRef`).
- **Wrapper Div Hell**: Quando não era possível injetar o elemento raiz, bibliotecas criavam elementos intermediários (`<div>` ou `<span>`), quebrando layouts CSS baseados em Flexbox (`gap`), CSS Grid e acessibilidade de leitores de tela.
- **Conflito de Event Handlers**: Ao encapsular um botão interno, cliques podiam disparar múltiplos handlers redundantes ou suprimir eventos essenciais da aplicação.

O Radix solucionou este enigma da computação gráfica no navegador criando o pacote `@radix-ui/react-slot` e generalizando a prop **`asChild`**:
Quando `asChild={true}` é declarado em um componente Radix, ele **não renderiza nenhum nó HTML próprio**. Em vez disso, através de manipulação controlada de VDOM (`React.cloneElement` customizado), ele injeta diretamente no seu único elemento filho:
1. Todos os atributos de acessibilidade (`role`, `aria-*`, `id`, `tabIndex`).
2. Os seletores de estado orientados a dados (`data-state`, `data-disabled`, `data-orientation`).
3. Uma fusão inteligente de propriedades: classes CSS (`className`) são concatenadas, referências DOM (`ref`) são unificadas via `composeRefs`, e handlers de eventos (`onClick`, `onKeyDown`) são encadeados de forma cooperativa — o handler do filho é executado primeiro; se o filho chamar `event.preventDefault()`, o handler interno do Radix interrompe sua ação padrão de forma graciosa.

```tsx
// Sem div extra, sem tag button aninhada em <a>: o Link do Next.js herda
// o comportamento WAI-ARIA, o foco e os dados de estado do Dialog Trigger:
<Dialog.Trigger asChild>
  <button type="button" className="btn-primary">
    Abrir Modal de Configurações
  </button>
</Dialog.Trigger>
```

#### 2. Arquitetura Orientada a Estado via Atributos `data-*`
Ao invés de obrigar desenvolvedores a utilizarem classes CSS utilitárias acopladas ou styled-components pesados, o Radix Primitives comunica todas as mudanças de estado interno e de geometria física através de atributos padronizados no elemento DOM:
- `data-state`: `"open"` | `"closed"` | `"checked"` | `"unchecked"` | `"indeterminate"` | `"active"` | `"inactive"` | `"on"` | `"off"`.
- `data-side`: `"top"` | `"right"` | `"bottom"` | `"left"`.
- `data-align`: `"start"` | `"center"` | `"end"`.
- `data-orientation`: `"horizontal"` | `"vertical"`.
- `data-disabled`: presente quando o item estiver desabilitado.
- `data-highlighted`: presente quando o item estiver selecionado via navegação por teclado ou hover ativo.

Essa convenção permitiu o nascimento de seletores modernos e declarativos em Tailwind CSS v3 e v4, como `data-[state=open]:animate-in` e `data-[side=bottom]:slide-in-from-top-2`, transformando a estilização de menus suspensos em código limpo, sem dependência de estados React externos ou re-renderizações desnecessárias da árvore.

#### 3. Radix Colors: A Ciência Cromática da Escala de 12 Passos
A maioria das bibliotecas de UI adotava escalas arbitrárias de 50 a 950 herdadas do Tailwind. O Radix Colors introduziu uma escala de **12 passos matematicamente mapeados para papéis semânticos de interface**, calibrados para atingir contrastes adequados tanto no modo claro quanto no escuro:

| Passo / Step | Papel Semântico de Interface | Comportamento no Design System |
| :--- | :--- | :--- |
| **Passo 1** | Fundo da Aplicação (*App Background*) | Tela principal, canvas de menor contraste. |
| **Passo 2** | Fundo de Superfícies Sutis (*Subtle Background*) | Cards, headers, containers secundários, barras laterais. |
| **Passo 3** | Elemento Interativo em Repouso (*UI Element Normal*) | Fundo de inputs, botões neutros secundários desativados. |
| **Passo 4** | Elemento Interativo em Hover (*UI Element Hover*) | Feedback de passagem de mouse para cartões interativos. |
| **Passo 5** | Elemento Interativo em Clique (*UI Element Active/Pressed*) | Estado ativo de abas, botões pressionados. |
| **Passo 6** | Bordas e Separadores Sutis (*Subtle Borders*) | Linhas de divisão (`Separator`), bordas internas de tabelas. |
| **Passo 7** | Bordas de Componentes (*UI Element Border*) | Contorno de caixas de entrada, botões de contorno, anéis. |
| **Passo 8** | Bordas em Hover (*UI Element Hover Border*) | Realce de contorno em foco/hover. |
| **Passo 9** | Fundo Sólido de Ênfase (*Solid Accent Background*) | Botões de ação primária, botões selecionados, crachás. |
| **Passo 10** | Fundo Sólido em Hover (*Solid Accent Hover*) | Hover no botão primário de maior contraste visual. |
| **Passo 11** | Texto de Baixo Contraste (*Low-Contrast Text*) | Legendas, placeholders, timestamps, textos secundários. |
| **Passo 12** | Texto de Alto Contraste (*High-Contrast Text*) | Títulos (`h1-h6`), rótulos obrigatórios, números primários. |

Adicionalmente, cada matiz possui a sua contraparte **Alpha** (ex: `slate-a1` a `slate-a12`, `iris-a1` a `iris-a12`), permitindo que modais, menus suspensos e cartões de vidro translúcido se sobreponham a fundos complexos preservando a luminescência e a matiz natural, sem o aspecto "esbranquiçado" ou "acinzentado" gerado por opacidades RGBA convencionais.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto

1. **SaaS B2B Mission-Critical & Developer Tools**:
   Aplicações corporativas que exigem fluxos de navegação densos, suporte implacável a atalhos de teclado, acessibilidade auditável e alta velocidade de resposta (ex: Linear, Supabase, Neon, Vercel Dashboard, WorkOS Admin Portal).
2. **Fundação e Criação de Design Systems Proprietários**:
   Startups e empresas de tecnologia em crescimento que precisam de um sistema de componentes com identidade própria e customização visual absoluta. Ao usar Radix Primitives como camada de comportamento, a equipe economiza centenas de horas de engenharia dedicadas a calcular colisões de janelas flutuantes, gerenciar armadilhas de foco (*focus traps*) e lidar com especificações ARIA para leitores de tela como NVDA, JAWS e VoiceOver.
3. **Plataformas de Produtividade em Estilo Desktop (Web OS / macOS-like)**:
   Aplicações ricas em janelas flutuantes, paletas de comando, menus de contexto com clique com o botão direito, painéis laterais deslizantes (*sheets*) e áreas roláveis com barras de rolagem nativas estilizadas.
4. **Produtos com Conformidade Rigorosa de Acessibilidade (WCAG 2.1 / 2.2 AA e AAA)**:
   Setores regulamentados (bancos, fintechs, governos, saúde e grandes empresas públicas americanas/europeias que exigem relatórios VPAT de conformidade com a Seção 508). O Radix Primitives implementa os padrões de teclado estabelecidos pelo WAI-ARIA Authoring Practices Guide (APG) de ponta a ponta.

---

### Momento do Fluxo e a Regra 60-30-10

Na engenharia de design de alto nível, a harmonia de uma tela decorre da divisão matemática do foco e da carga cognitiva:

```
+-------------------------------------------------------------------------+
|                  DISTRIBUIÇÃO DA REGRA 60-30-10 COM RADIX              |
+-------------------------------------------------------------------------+
| [========================= 60% =========================]               |
| ESPINHA DORSAL ESTRUTURAL (Radix Primitives & Themes Layout)            |
| -> Superfícies neutras (Steps 1 e 2), Tipografia estrutural             |
| -> Componentes de Dados (DataList, Flex, Grid, Separator, Inset)        |
+----------------------------------------+--------------------------------+
| [=========== 30% ===========]          | [==== 10% ====]                |
| CAMADA DE OVERLAYS & NAVEGAÇÃO         | ACENTO E FEEDBACK CRÍTICO      |
| -> Dialogs, Popovers, Menus            | -> Solid Buttons (Step 9/10)   |
| -> Tabs, SegmentedControl, ScrollArea  | -> Callouts semânticos, Toasts |
+----------------------------------------+--------------------------------+
```

- **60% — Espinha Dorsal Absoluta da Interface (Superfícies e Estrutura Neutra)**:
  O Radix fornece os fundos de tela (`step-1`), cartões (`step-2`), grades responsivas (`Grid`, `Flex`, `Container`), separadores e elementos de formulário neutros (`TextField`, `TextArea`). Nesta camada, não existem gradientes luminosos nem animações distrativas; a prioridade é a clareza de leitura e a precisão do alinhamento.
- **30% — Camada Dinâmica de Navegação, Orquestração e Overlays**:
  Onde o Radix demonstra sua força arquitetural. Componentes como `Dialog`, `DropdownMenu`, `ContextMenu`, `Popover`, `HoverCard`, `Tabs` e `SegmentedControl` orquestram o fluxo de trabalho do usuário. Eles abrem com suavidade, respeitam as bordas da tela sem vazar para fora da viewport e posicionam setas indicativas milimetricamente calculadas.
- **10% — Efeitos Protagonistas e Acentos de Foco**:
  Reservado para botões de ação primária que utilizam os passos sólidos da escala Radix Colors (`step-9` em repouso e `step-10` em hover), alertas contextuais com o componente `Callout` (em matizes `ruby` para erros ou `jade` para sucesso) e indicadores de estado em tempo real.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

1. **Websites Institucionais Estáticos sem JavaScript (Zero-JS SSG / Astro sem Hidratação)**:
   O Radix Primitives baseia sua mecânica em manipuladores de eventos e no ciclo de vida do React para calcular coordenadas do DOM (`getBoundingClientRect`), interceptar teclas do teclado e controlar acessibilidade. Em páginas de marketing puro geradas em HTML estático sem hidratação de cliente, o Radix não funcionará como esperado.
2. **Ambientes e Frameworks Não-React (sem wrappers especializados)**:
   Tentar importar pacotes `@radix-ui/*` em ambientes Svelte, Vue ou Solid é incompatível. Nesses casos, deve-se recorrer a bibliotecas irmãs portadas pela comunidade, como **bits-ui** (para Svelte) ou **radix-vue** (para Vue).
3. **Experiências Cinematográficas 3D e Shaders WebGL (Three.js / React Three Fiber)**:
   Projetos cujo foco reside em cenas 3D interativas em tela cheia e transições de câmera cinemáticas não se beneficiam de uma infraestrutura baseada em caixas retangulares de layout HTML tradicional.

---

### ⚠️ Anti-padrões e Erros Críticos de Engenharia

1. **Anti-padrão dos Múltiplos Filhos no `asChild` (Erro Fatal de VDOM)**:
   O componente `Slot` do Radix exige estritamente **um único nó React válido** como filho direto. Se você passar texto solto, múltiplos nós adjacentes ou fragmentos sem encapsulamento, o React quebrará a renderização em tempo de execução:
   ```tsx
   // ❌ QUEBRA CRÍTICA: Múltiplos filhos dentro de asChild
   <Dialog.Trigger asChild>
     <span>Texto</span>
     <button>Clique aqui</button>
   </Dialog.Trigger>

   // ✅ CORRETO: Apenas um elemento filho direto
   <Dialog.Trigger asChild>
     <button type="button">
       <span>Texto</span>
       <span>Clique aqui</span>
     </button>
   </Dialog.Trigger>
   ```

2. **Supressão Inadvertida de Props e Refs ao Criar Componentes Reutilizáveis**:
   Ao criar um wrapper em torno de uma primitiva Radix usando `asChild`, é mandatório repassar a `ref` e todas as props (`...props`) para o nó subjacente. Do contrário, os event listeners internos do Radix (como fechamento via ESC ou navegação por setas) serão perdidos silenciosamente.
   ```tsx
   // ❌ QUEBRA DE ACESSIBILIDADE: Ref e props não repassadas
   const CustomTrigger = ({ children }: { children: React.ReactNode }) => (
     <button>{children}</button>
   );

   // ✅ ENGENHARIA ROBUSTA: Uso de React.forwardRef e repasse total de props
   const CustomTrigger = React.forwardRef<HTMLButtonElement, React.ButtonHTMLAttributes<HTMLButtonElement>>(
     ({ children, ...props }, ref) => (
       <button ref={ref} {...props}>
         {children}
       </button>
     )
   );
   ```

3. **Inversão Cromática na Escala Radix Colors**:
   Utilizar a cor sólida do **Passo 9** como fundo de contêineres ou cartões inteiros resulta em poluição visual e fadiga ocular. O Passo 9 foi projetado especificamente para elementos pontuais de alto impacto (botões primários e seletores ativos). As superfícies e fundos devem sempre habitar os **Passos 1 e 2**, enquanto os elementos em repouso pertencem aos **Passos 3, 4 e 5**.

4. **Desmonte Abrupto sem Animação de Saída**:
   Muitos desenvolvedores reclamam que o Radix "desaparece da tela de forma seca" ao fechar um diálogo ou menu. Isso ocorre porque o componente desocupa o nó DOM imediatamente a menos que uma animação CSS esteja associada ao atributo `data-[state=closed]` ou o usuário declare a propriedade `forceMount` para delegação a bibliotecas de animação como o Framer Motion.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo está o inventário técnico com os 12 componentes mais emblemáticos do ecossistema Radix UI, abrangendo o núcleo de Primitivas Headless e os componentes refinados do Radix Themes.

---

### 1. `Dialog` & `AlertDialog` (Radix Primitives)
- **Anatomia Visual & Comportamento**:
  Composto por `<Dialog.Root>`, `<Dialog.Trigger>`, `<Dialog.Portal>`, `<Dialog.Overlay>`, `<Dialog.Content>`, `<Dialog.Title>`, `<Dialog.Description>` e `<Dialog.Close>`.
  Renderiza o conteúdo dentro de um Portal desacoplado no `document.body`. Ao abrir, bloqueia a rolagem do corpo da página (`scroll-lock`), captura o foco do teclado internamente (*focus trapping*) e restaura o foco cirurgicamente no elemento disparador quando fechado. O `AlertDialog` força a confirmação de ações destrutivas impedindo o fechamento acidental por clique externo.
- **Gatilho de Interação**:
  Click no disparador, clique na tecla `Enter`/`Space`. Fechamento via clique na sobreposição escura (*backdrop*), tecla `Escape` ou acionamento do botão `<Dialog.Close>`.
- **Onde Encaixar na Página**:
  Modais de criação de recursos em Dashboards, confirmações de deleção crítica, fluxos de autenticação, telas de configurações profundas e diálogos de checkout.

---

### 2. `DropdownMenu` & `ContextMenu` (Radix Primitives)
- **Anatomia Visual & Comportamento**:
  Arquitetura baseada no padrão de acessibilidade *Menu APG*. Possui `<DropdownMenu.Root>`, `<Trigger>`, `<Portal>`, `<Content>`, `<Item>`, `<CheckboxItem>`, `<RadioGroup>`, `<Sub>`, `<SubTrigger>`, `<SubContent>` e `<Arrow>`.
  Oferece navegação contínua por setas do teclado (*roving tabindex*), digitação direta para saltar para itens pelo primeiro caractere (*typeahead*), suporte nativo a submenus em cascata com atraso de ponteiro para evitar fechamento acidental (*pointer intent detection*) e cálculo dinâmico de espaço livre na tela.
- **Gatilho de Interação**:
  - `DropdownMenu`: Click no disparador ou seta para baixo.
  - `ContextMenu`: Clique com o botão direito do mouse ou combinação de toque longo em dispositivos móveis.
- **Onde Encaixar na Página**:
  Barra de navegação superior (menu de perfil do usuário), cabeçalhos de colunas em tabelas de dados (ordenar, filtrar, ocultar colunas), botões de ação rápida em linhas de tabela e menus de arquivos em editores de código.

---

### 3. `Popover` & `HoverCard` (Radix Primitives)
- **Anatomia Visual & Comportamento**:
  - `Popover`: Camada flutuante rica projetada para comportar formulários e controles interativos (como seletores de data, painéis de cores ou filtros avançados).
  - `HoverCard`: Cartão de pré-visualização instantânea desenhado para links e menções de usuários (estilo Twitter/GitHub profile cards), dotado de gerenciamento milimétrico de zonas de tolerância do ponteiro (*hit-testing*) para permitir que o usuário deslize o mouse do gatilho para dentro do cartão sem que ele se feche.
- **Gatilho de Interação**:
  - `Popover`: Click no botão gatilho.
  - `HoverCard`: Passagem do mouse (*hover*) com temporizador de entrada (*openDelay*) e saída (*closeDelay*), além de foco via teclado.
- **Onde Encaixar na Página**:
  Seletor de filtros no topo de dashboards, cartões de pré-visualização de autores em feeds de artigos, seletores de datas em formulários de agendamento e explicações de métricas complexas.

---

### 4. `Select` (Radix Primitives)
- **Anatomia Visual & Comportamento**:
  Substituto acessível para o elemento nativo HTML `<select>`. Suporta `<Select.ScrollUpButton>` e `<Select.ScrollDownButton>` quando a lista ultrapassa o tamanho da janela, garantindo rolagem visual elegante. Implementa alinhamento dinâmico do item atualmente selecionado diretamente sobre o botão disparador (reproduzindo com fidelidade a experiência dos menus de seleção nativos do macOS e iOS).
- **Gatilho de Interação**:
  Click, `Space` ou `ArrowDown`/`ArrowUp` para abrir; navegação por setas e seleção com `Enter`.
- **Onde Encaixar na Página**:
  Formulários densos de checkout, seleção de país/moeda, filtros de dados em cabeçalhos de tabela e painéis de configuração de ambiente.

---

### 5. `Tabs` (Radix Primitives)
- **Anatomia Visual & Comportamento**:
  Composto por `<Tabs.Root>`, `<Tabs.List>`, `<Tabs.Trigger>` e `<Tabs.Content>`.
  Oferece suporte total a orientação horizontal e vertical. O gerenciamento de foco por teclado (*roving focus*) permite alternar entre abas utilizando unicamente as setas direcionais, atualizando o conteúdo associado com suporte nativo a leitores de tela via atributos recíprocos `aria-controls` e `aria-labelledby`.
- **Gatilho de Interação**:
  Click direto ou navegação por setas (opção de ativação manual com `Enter` ou automática ao focar).
- **Onde Encaixar na Página**:
  Divisão de categorias em páginas de configurações, alternância entre blocos de código com linguagens distintas na documentação técnica e navegação secundária em dashboards operacionais.

---

### 6. `NavigationMenu` (Radix Primitives)
- **Anatomia Visual & Comportamento**:
  A solução definitiva para os mega-menus de navegação comuns em websites corporativos (estilo Stripe). Possui uma janela de exibição única compartilhada (`<NavigationMenu.Viewport>`) que redimensiona dinamicamente sua largura e altura através de transições suaves à medida que o usuário passa o mouse entre diferentes itens de menu de tamanhos variados, evitando o efeito indesejado de menus piscando ou sobrepondo elementos da página.
- **Gatilho de Interação**:
  Hover com detecção inteligente de intenção de movimento (*pointer-intent algorithm*) ou foco por teclado com `Tab`.
- **Onde Encaixar na Página**:
  Header principal (Navbar) de plataformas SaaS, portais corporativos complexos e plataformas de comércio eletrônico com grandes árvores de categorias de produtos.

---

### 7. `ScrollArea` (Radix Primitives)
- **Anatomia Visual & Comportamento**:
  Composto por `<ScrollArea.Root>`, `<ScrollArea.Viewport>`, `<ScrollArea.Scrollbar>`, `<ScrollArea.Thumb>` e `<ScrollArea.Corner>`.
  Substitui as barras de rolagem nativas do navegador (que variam de forma discrepante entre Windows, macOS e Linux) por uma barra de rolagem minimalista, fluida e totalmente estilizável via CSS. Suporta modos de auto-ocultação (`hover`, `scroll`, `auto` ou `always`), sem quebrar a aceleração nativa de hardware do motor de rolagem do navegador.
- **Gatilho de Interação**:
  Rolagem do mouse (*wheel*), toque gestual em trackpads/telas táteis ou arrasto direto do indicador (*thumb*).
- **Onde Encaixar na Página**:
  Barras laterais longas (*sidebars*), terminais de log em tempo real, painéis de chat com mensagens contínuas e listas suspensas com grande quantidade de itens.

---

### 8. `Slider` (Radix Primitives)
- **Anatomia Visual & Comportamento**:
  Composto por `<Slider.Root>`, `<Slider.Track>`, `<Slider.Range>` e um ou múltiplos `<Slider.Thumb>`.
  Permite controle univariado ou intervalos com múltiplos cursores (*multi-thumb range slider*). Suporta passos incrementais (`step`), orientação horizontal e vertical e inversão de direção (*inverted*). Implementa suporte total a teclado: setas ajustam valores em incrementos finos, enquanto `PageUp`/`PageDown` e `Home`/`End` saltam valores expressivos ou vão aos extremos.
- **Gatilho de Interação**:
  Arrastar com o ponteiro do mouse ou toque, cliques na trilha para posicionamento direto e ajuste via teclado.
- **Onde Encaixar na Página**:
  Controles de volume e reprodução em players de mídia, filtros de faixa de preço em e-commerces e ajustes de sensibilidade e limites numéricos em painéis analíticos.

---

### 9. `DataList` (Radix Themes)
- **Anatomia Visual & Comportamento**:
  Arquitetura semântica para renderização de pares chave-valor baseada na tag HTML `<dl>`: `<DataList.Root>`, `<DataList.Item>`, `<DataList.Label>` e `<DataList.Value>`.
  Oferece alinhamento horizontal ou vertical com densidade ajustável, permitindo encaixar ícones, badges, botões de cópia rápida e links sem quebrar o ritmo tipográfico e o espaçamento vertical.
- **Gatilho de Interação**:
  Exibição estática com interação focada nos elementos de ação internos (ex: clique para copiar hash de transação, botão de editar).
- **Onde Encaixar na Página**:
  Páginas de detalhes de transação em fintechs, resumos de perfis de usuário, painéis de auditoria e inspeção de recursos em nuvem (ex: instâncias de banco de dados, chaves de API).

---

### 10. `SegmentedControl` (Radix Themes)
- **Anatomia Visual & Comportamento**:
  Composto por `<SegmentedControl.Root>` e `<SegmentedControl.Item>`.
  Componente visual clássico do ecossistema Apple (iOS/macOS), desenhado para alternância mútua entre opções exclusivas em um trilho encapsulado. Apresenta fundo atenuado com um marcador ativo elevado por uma leve sombra de superfície e cantos arredondados, garantindo feedback tátil imediato.
- **Gatilho de Interação**:
  Click direto ou navegação horizontal por setas do teclado.
- **Onde Encaixar na Página**:
  Alternadores de período temporal (Dia / Semana / Mês / Ano) em gráficos analíticos, seletores de modo de visualização (Lista / Tabela / Galeria) e alternadores de status de filtros.

---

### 11. `Callout` (Radix Themes)
- **Anatomia Visual & Comportamento**:
  Composto por `<Callout.Root>`, `<Callout.Icon>` e `<Callout.Text>`.
  Bloco estruturado para comunicação de mensagens de contexto crítico (avisos, dicas técnicas, restrições e confirmações). Oferece três variantes de acabamento:
  - `soft`: fundo preenchido suave com o Passo 3 da escala de cores selecionada e texto no Passo 11.
  - `surface`: fundo translúcido no Passo 2 com borda no Passo 7.
  - `outline`: fundo transparente delimitado por borda nítida de alta visibilidade.
- **Gatilho de Interação**:
  Leitura informativa passiva com foco de acessibilidade; pode conter links contextuais ou botões de ação corretiva.
- **Onde Encaixar na Página**:
  Alertas de vencimento de plano ou pagamento em atraso, notas explicativas de segurança em configurações de autenticação de dois fatores e avisos de depreciação em documentação técnica.

---

### 12. `Inset` (Radix Themes)
- **Anatomia Visual & Comportamento**:
  Componente utilitário que anula cirurgicamente as margens internas (*padding*) do seu contêiner pai (normalmente um `<Card>` ou `<Dialog.Content>`), permitindo que imagens, tabelas de dados ou blocos de código se estendam até a borda externa (*bleed*), criando uma transição visual de acabamento industrial de alta fidelidade.
- **Gatilho de Interação**:
  Passivo / Layout estrutural.
- **Onde Encaixar na Página**:
  Imagens de capa em cartões de produtos ou artigos de blog, tabelas de dados que ocupam a largura total de um card sem margens duplas e visualizadores de mapas ou gráficos embutidos.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

O ecossistema do Radix é distribuído em pacotes atômicos e modulares. É possível adotar apenas as primitivas necessárias de forma desvinculada ou o sistema de temas completo da WorkOS:

```bash
# 1. Instalação das Primitivas Headless do Radix (Abordagem shadcn / Personalizada)
npm install @radix-ui/react-dialog @radix-ui/react-dropdown-menu @radix-ui/react-popover @radix-ui/react-slot @radix-ui/react-tabs @radix-ui/react-scroll-area lucide-react clsx tailwind-merge

# 2. Instalação do Radix Themes (Abordagem Pronta e Opinativa com Design macOS)
npm install @radix-ui/themes

# 3. Instalação do Sistema de Cores Independente
npm install @radix-ui/colors
```

---

### Física de Movimento, Curvas de Easing & Variáveis CSS do Radix

O Radix Primitives foi projetado para integrar-se ao CSS puro e a bibliotecas de animação através de propriedades customizadas injetadas dinamicamente durante a renderização:

1. **Variáveis Dinâmicas de Origem e Dimensões**:
   - `--radix-popover-content-transform-origin`: Calcula o ponto de origem exato da animação com base no lado onde o balão se posicionou em relação ao gatilho (`top`, `bottom`, `left`, `right`).
   - `--radix-accordion-content-height` e `--radix-collapsible-content-height`: Contêm a altura exata do conteúdo em pixels medida pelo motor interno, possibilitando animações perfeitas de sanfona sem o clássico bug de altura engessada com `max-height: 1000px`.
   - `--radix-popover-trigger-width`: Permite que o menu suspenso ou popover herde exatamente a mesma largura do botão que o abriu via CSS (`width: var(--radix-popover-trigger-width)`).

2. **Curva de Easing Padrão Apple / WorkOS**:
   As animações de abertura de modais e menus devem usar uma curva de saída suave e contida, simulando inércia física sem oscilações artificiais:
   ```css
   /* Curva de desaceleração elástica suave para interfaces desktop */
   transition-timing-function: cubic-bezier(0.16, 1, 0.3, 1);
   ```

3. **Física de Spring para Microinterações (Framer Motion)**:
   Para alternadores de estado como `Switch` e `SegmentedControl`:
   ```ts
   export const radixSpringPhysics = {
     type: "spring",
     stiffness: 400,
     damping: 30,
     mass: 0.8
   };
   ```

---

### Receitas de Código em Produção

Abaixo estão três implementações completas, realistas e prontas para uso em produção com TypeScript, Tailwind CSS e as convenções oficiais do Radix.

---

#### Receita 1: Componente Polimórfico `Button` com `@radix-ui/react-slot` e `cva`
Esta receita demonstra a arquitetura exata que consolidou a fama do `asChild`: um componente que pode se comportar visualmente como botão, mas renderizar um link sem wrappers desnecessários no DOM.

```tsx
// components/ui/button.tsx
import * as React from "react";
import { Slot } from "@radix-ui/react-slot";
import { cva, type VariantProps } from "class-variance-authority";
import { clsx } from "clsx";
import { twMerge } from "tailwind-merge";

function cn(...inputs: any[]) {
  return twMerge(clsx(inputs));
}

const buttonVariants = cva(
  "inline-flex items-center justify-center whitespace-nowrap rounded-md text-sm font-medium transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50 select-none",
  {
    variants: {
      variant: {
        default:
          "bg-slate-900 text-white hover:bg-slate-800 focus-visible:ring-slate-950 dark:bg-slate-50 dark:text-slate-900 dark:hover:bg-slate-200",
        destructive:
          "bg-red-600 text-white hover:bg-red-700 focus-visible:ring-red-600 dark:bg-red-900 dark:text-red-100",
        outline:
          "border border-slate-200 bg-transparent hover:bg-slate-100 hover:text-slate-900 focus-visible:ring-slate-400 dark:border-slate-800 dark:hover:bg-slate-800 dark:hover:text-slate-50",
        secondary:
          "bg-slate-100 text-slate-900 hover:bg-slate-200 focus-visible:ring-slate-400 dark:bg-slate-800 dark:text-slate-50 dark:hover:bg-slate-700",
        ghost:
          "hover:bg-slate-100 hover:text-slate-900 focus-visible:ring-slate-400 dark:hover:bg-slate-800 dark:hover:text-slate-50",
        link: "text-slate-900 underline-offset-4 hover:underline dark:text-slate-50",
      },
      size: {
        default: "h-9 px-4 py-2",
        sm: "h-8 rounded-md px-3 text-xs",
        lg: "h-10 rounded-md px-8",
        icon: "h-9 w-9",
      },
    },
    defaultVariants: {
      variant: "default",
      size: "default",
    },
  }
);

export interface ButtonProps
  extends React.ButtonHTMLAttributes<HTMLButtonElement>,
    VariantProps<typeof buttonVariants> {
  asChild?: boolean;
}

export const Button = React.forwardRef<HTMLButtonElement, ButtonProps>(
  ({ className, variant, size, asChild = false, ...props }, ref) => {
    // Se asChild for true, Slot transfere as classes e comportamento ao filho direto
    const Comp = asChild ? Slot : "button";
    return (
      <Comp
        className={cn(buttonVariants({ variant, size, className }))}
        ref={ref}
        {...props}
      />
    );
  }
);
Button.displayName = "Button";
```

---

#### Receita 2: `Dialog` Modal Acessível com Radix Primitives & Tailwind
Esta implementação utiliza as classes orientadas a dados (`data-[state=open]`) do Tailwind para orquestrar uma abertura suave com desfoque de fundo e animação a partir da escala matemática.

```tsx
// components/ui/dialog.tsx
"use client";

import * as React from "react";
import * as DialogPrimitive from "@radix-ui/react-dialog";
import { X } from "lucide-react";
import { clsx } from "clsx";
import { twMerge } from "tailwind-merge";

function cn(...inputs: any[]) {
  return twMerge(clsx(inputs));
}

export const Dialog = DialogPrimitive.Root;
export const DialogTrigger = DialogPrimitive.Trigger;
export const DialogPortal = DialogPrimitive.Portal;
export const DialogClose = DialogPrimitive.Close;

export const DialogOverlay = React.forwardRef<
  React.ElementRef<typeof DialogPrimitive.Overlay>,
  React.ComponentPropsWithoutRef<typeof DialogPrimitive.Overlay>
>(({ className, ...props }, ref) => (
  <DialogPrimitive.Overlay
    ref={ref}
    className={cn(
      "fixed inset-0 z-50 bg-black/60 backdrop-blur-sm",
      "data-[state=open]:animate-in data-[state=closed]:animate-out",
      "data-[state=closed]:fade-out-0 data-[state=open]:fade-in-0",
      className
    )}
    {...props}
  />
));
DialogOverlay.displayName = DialogPrimitive.Overlay.displayName;

export const DialogContent = React.forwardRef<
  React.ElementRef<typeof DialogPrimitive.Content>,
  React.ComponentPropsWithoutRef<typeof DialogPrimitive.Content>
>(({ className, children, ...props }, ref) => (
  <DialogPortal>
    <DialogOverlay />
    <DialogPrimitive.Content
      ref={ref}
      className={cn(
        "fixed left-[50%] top-[50%] z-50 grid w-full max-w-lg translate-x-[-50%] translate-y-[-50%] gap-4 border border-slate-200 bg-white p-6 shadow-xl duration-200 rounded-xl dark:border-slate-800 dark:bg-slate-950",
        "data-[state=open]:animate-in data-[state=closed]:animate-out",
        "data-[state=closed]:fade-out-0 data-[state=open]:fade-in-0",
        "data-[state=closed]:zoom-out-95 data-[state=open]:zoom-in-95",
        "data-[state=closed]:slide-out-to-left-1/2 data-[state=closed]:slide-out-to-top-[48%]",
        "data-[state=open]:slide-in-from-left-1/2 data-[state=open]:slide-in-from-top-[48%]",
        className
      )}
      {...props}
    >
      {children}
      <DialogPrimitive.Close className="absolute right-4 top-4 rounded-sm opacity-70 transition-opacity hover:opacity-100 focus:outline-none focus:ring-2 focus:ring-slate-400 focus:ring-offset-2 disabled:pointer-events-none">
        <X className="h-4 w-4" />
        <span className="sr-only">Fechar</span>
      </DialogPrimitive.Close>
    </DialogPrimitive.Content>
  </DialogPortal>
));
DialogContent.displayName = DialogPrimitive.Content.displayName;

export const DialogHeader = ({
  className,
  ...props
}: React.HTMLAttributes<HTMLDivElement>) => (
  <div className={cn("flex flex-col space-y-1.5 text-center sm:text-left", className)} {...props} />
);

export const DialogTitle = React.forwardRef<
  React.ElementRef<typeof DialogPrimitive.Title>,
  React.ComponentPropsWithoutRef<typeof DialogPrimitive.Title>
>(({ className, ...props }, ref) => (
  <DialogPrimitive.Title
    ref={ref}
    className={cn("text-lg font-semibold leading-none tracking-tight text-slate-900 dark:text-slate-50", className)}
    {...props}
  />
));
DialogTitle.displayName = DialogPrimitive.Title.displayName;

export const DialogDescription = React.forwardRef<
  React.ElementRef<typeof DialogPrimitive.Description>,
  React.ComponentPropsWithoutRef<typeof DialogPrimitive.Description>
>(({ className, ...props }, ref) => (
  <DialogPrimitive.Description
    ref={ref}
    className={cn("text-sm text-slate-500 dark:text-slate-400", className)}
    {...props}
  />
));
DialogDescription.displayName = DialogPrimitive.Description.displayName;
```

---

#### Receita 3: Dashboard Card com Radix Themes (`Theme`, `Card`, `Inset`, `DataList`, `Callout`)
Exemplo utilizando a biblioteca oficial de temas do Radix com estilização semântica de alta densidade e tipografia automática:

```tsx
// app/dashboard/page.tsx
import "@radix-ui/themes/styles.css";
import { Theme, Card, Inset, Heading, Text, Badge, DataList, Callout, Flex, Button } from "@radix-ui/themes";
import { Info, Copy, CheckCircle2 } from "lucide-react";

export default function InfrastructureDetailsCard() {
  return (
    <Theme accentColor="iris" grayColor="slate" radius="large" scaling="95%">
      <div className="p-8 max-w-xl mx-auto">
        <Card size="3" variant="surface">
          {/* O componente Inset expande a imagem de topo até a borda do Card */}
          <Inset clip="padding-box" side="top" pb="current">
            <div className="h-32 bg-gradient-to-r from-indigo-900 via-purple-900 to-slate-900 flex items-center justify-center">
              <Heading size="5" style={{ color: "white" }}>
                Instância de Produção AWS
              </Heading>
            </div>
          </Inset>

          <Flex direction="column" gap="4" mt="2">
            <Flex justify="between" align="center">
              <Text size="2" color="gray" weight="medium">
                Identificador: prod-cluster-us-east-1
              </Text>
              <Badge color="jade" variant="soft" radius="full">
                <CheckCircle2 className="w-3 h-3 mr-1 inline" /> Operacional
              </Badge>
            </Flex>

            {/* Componente DataList semântico para metadados técnicos */}
            <DataList.Root orientation="horizontal" size="2">
              <DataList.Item>
                <DataList.Label minWidth="120px">Região Primária</DataList.Label>
                <DataList.Value>us-east-1 (N. Virginia)</DataList.Value>
              </DataList.Item>

              <DataList.Item>
                <DataList.Label minWidth="120px">IP Público</DataList.Label>
                <DataList.Value>
                  <Flex align="center" gap="2">
                    <code>198.51.100.42</code>
                    <Button variant="ghost" size="1" highContrast>
                      <Copy className="w-3 h-3" />
                    </Button>
                  </Flex>
                </DataList.Value>
              </DataList.Item>

              <DataList.Item>
                <DataList.Label minWidth="120px">Capacidade</DataList.Label>
                <DataList.Value>16 vCPU • 64 GB RAM</DataList.Value>
              </DataList.Item>
            </DataList.Root>

            {/* Componente Callout informativo com variante de superfície */}
            <Callout.Root color="amber" size="1" variant="soft">
              <Callout.Icon>
                <Info className="w-4 h-4" />
              </Callout.Icon>
              <Callout.Text>
                Janela de manutenção programada para hoje às 03:00 UTC. Reinicializações automáticas habilitadas.
              </Callout.Text>
            </Callout.Root>
          </Flex>
        </Card>
      </div>
    </Theme>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao arquitetar um novo produto no ecossistema React utilizando referências do Radix UI, a inteligência artificial ou o arquiteto de software deve registrar as diretrizes abaixo dentro do arquivo de especificação técnica do projeto:

### 1. Declaração Obrigatória da Camada de Componentes
- **Abordagem Headless + Tailwind (Padrão shadcn/ui)**:
  Se o objetivo do projeto for personalização estética radical, paleta proprietária e ownership de código total, declare a dependência direta dos pacotes atômicos `@radix-ui/react-*` associados ao utilitário `@radix-ui/react-slot`. Todos os componentes devem ser salvos na árvore de código local (`src/components/ui/`).
- **Abordagem Radix Themes**:
  Se o objetivo do projeto for um aplicativo de gerenciamento de dados de alta densidade no estilo macOS/Linear com entrega ultra-rápida, declare `@radix-ui/themes` como a camada visual oficial e configure o componente mestre `<Theme>` no arquivo de layout raiz (`layout.tsx`).

### 2. Mapeamento das Variáveis Radix Colors no Tailwind
Configure o arquivo de estilos globais ou o `tailwind.config.ts` respeitando os papéis funcionais dos 12 passos da escala:
```css
/* Definições de superfícies mapeadas para a escala Radix Colors */
:root {
  --canvas-app: var(--slate-1);
  --canvas-card: var(--slate-2);
  --ui-interactive-normal: var(--slate-3);
  --ui-interactive-hover: var(--slate-4);
  --ui-interactive-active: var(--slate-5);
  --line-subtle: var(--slate-6);
  --line-element: var(--slate-7);
  --line-element-hover: var(--slate-8);
  --accent-solid: var(--iris-9);
  --accent-solid-hover: var(--iris-10);
  --text-muted: var(--slate-11);
  --text-primary: var(--slate-12);
}
```

### 3. Checklist Estrito de Implementação no Blueprint
- [ ] **Acessibilidade WAI-ARIA**: Todo modal, menu suspenso ou aba deve possuir título (`DialogTitle`) e descrição legível (`DialogDescription`) para garantir que os leitores de tela anunciem o contexto no momento em que o foco for capturado.
- [ ] **Uso Consciente do `asChild`**: Garantir que o componente encapsulado por `<Slot>` ou recebendo `asChild` possua apenas um nó filho direto e implemente `React.forwardRef` com propagação de props.
- [ ] **Gerenciamento de Colisões e Viewport**: Configurar sempre `collisionPadding={16}` e `sideOffset={8}` em popovers, tooltips e menus suspensos para evitar que o conteúdo encoste abruptamente nas margens do navegador mobile.
- [ ] **Respeito à Curva de Animação**: Usar exclusivamente `cubic-bezier(0.16, 1, 0.3, 1)` para aberturas e fechamentos de overlays e transições de abas, assegurando a assinatura tátil de alto padrão da WorkOS e da Apple.
