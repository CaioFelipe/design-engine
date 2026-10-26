---
id: "ark-ui"
name: "Ark UI"
url: "https://www.ark-ui.com/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Finite State Machine Architecture (Zag.js)", "Universal Multi-Framework Parity (React, Vue, Svelte, Solid)", "Headless Functional Anatomy (data-scope & data-part)", "High-Fidelity Complex Primitives (Tour, SignaturePad, QR, ColorPicker)", "Zero-Runtime Unstyled Infrastructure", "Enterprise W3C WAI-ARIA APG Compliance"]
densidade_informacao: "Flexivel"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS/Headless)"
stack_frameworks: ["React 19 / 18 (@ark-ui/react)", "Vue 3 (@ark-ui/vue)", "Svelte 5 / 4 (@ark-ui/svelte)", "SolidJS (@ark-ui/solid)", "Zag.js (@zag-js/*)", "Panda CSS", "Park UI", "Tailwind CSS v4 & v3", "TypeScript", "Framer Motion"]
compatibilidade:
  fontes_ideais: ["Inter", "Geist Sans", "Plus Jakarta Sans", "SF Pro Text / Display", "JetBrains Mono", "IBM Plex Sans"]
  paletas_ideais: ["Monochrome Industrial Dark & Light", "Deep Slate & Indigo Neutral", "Modern High-Contrast Zinc", "Tailwind Modern Neutral Scales", "Radix/Panda CSS 12-Step Tokens"]
  combinacoes_recomendadas: ["Park UI (Estilização pré-construída com Panda/Tailwind)", "Panda CSS (CSS-in-JS estático em tempo de build)", "Tailwind CSS v4 / v3", "Framer Motion", "Lucide React / Tabler Icons", "Chakra UI v3 (Arquitetado nativamente sobre Ark UI)"]
  conflitos_esteticos: ["Bibliotecas com acoplamento estético rígido (Bootstrap, Ant Design, Material UI legado)", "Neumorfismo plástico com sombras multidirecionais conflitantes", "Abordagens CSS imperativas legadas baseadas em seletores globais sem escopo de atributos"]
---

# Ark UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Ark UI** (`ark-ui.com`) é uma biblioteca headless de componentes de interface de usuário de última geração, concebida e desenvolvida por **Segun Adebayo** (criador do *Chakra UI* e *Zag.js*) em conjunto com o time do Chakra. Representa um marco arquitetural na engenharia de front-end ao dissociar de maneira radical a lógica de comportamento, a máquina de estados, a acessibilidade nativa e a renderização do framework hospedeiro.

Diferente da quase totalidade das bibliotecas headless contemporâneas — que ou são restritas ao ecossistema React (como Radix Primitives clássico) ou possuem implementações divergentes e fragmentadas mantidas por comunidades distintas em cada framework —, o Ark UI alcança uma **paridade de API 1:1 rigorosa e universal entre React, Vue 3, Svelte (4 e 5) e SolidJS**.

```
+-----------------------------------------------------------------------------------+
|                                 ARK UI ECOSYSTEM                                  |
+-----------------------------------------------------------------------------------+
|                               CHAKRA UI v3 / PARK UI                              |
|           Camada de Componentes Estilizados, Design Tokens & Presets              |
+-----------------------------------------------------------------------------------+
|                           PANDA CSS / TAILWIND CSS v4                             |
|          Camada de Estilização em Build-Time & Variantes (data-scope / part)      |
+-----------------------------------------------------------------------------------+
|                                    ARK UI                                         |
|      Adaptadores Nativos Headless com Paridade 1:1 de API e Nomes de Props:       |
|      - @ark-ui/react   - @ark-ui/vue   - @ark-ui/svelte   - @ark-ui/solid         |
|      (Renderização Declarativa, Composição via asChild, Portals e Presença)       |
+-----------------------------------------------------------------------------------+
|                                   ZAG.JS ENGINE                                   |
|      Máquinas de Estados Finitos (FSM) & Statecharts Puros em TypeScript          |
|      (W3C WAI-ARIA APG, Roving Tabindex, Focus Traps, Teclado & Gestos)           |
+-----------------------------------------------------------------------------------+
```

### A Tríade Tecnológica Distintiva do Ark UI

#### 1. A Fundação em Máquinas de Estados Finitos (Finite State Machines — Zag.js)
Tradicionalmente, componentes de interface acumulam dezenas de `useState`, `useEffect` e flags booleanas (`isOpen`, `isLoading`, `isFocused`, `isClosing`), criando uma explosão combinatória de estados impossíveis (por exemplo, um modal simultaneamente abrindo e fechando, ou um dropdown congelado entre hover e teclado).

O Ark UI elimina essa classe inteira de erros arquiteturais construindo cada componente sobre o **Zag.js**:
- Cada componente é governado por um **Statechart** formal com estados finitos discretos (`idle`, `focused`, `open`, `closing`, `dragging`).
- Transições de estado ocorrem estritamente em resposta a eventos bem definidos (`TRIGGER_CLICK`, `KEYDOWN_ESCAPE`, `POINTER_ENTER`, `DOC_POINTER_DOWN`).
- Toda a lógica de foco (*roving tabindex*, *focus trapping*), posicionamento flutuante colisional (*floating-ui* integrado) e anúncios para leitores de tela (*aria-live regions*) é calculada em nível puramente matemático no Zag.js e transmitida deterministicamente para a camada de visualização.

#### 2. Arquitetura de Seleção DOM: `data-scope` e `data-part`
Enquanto sistemas antigos dependiam de classes CSS específicas (como `.ark-dialog-content`) ou injeção de classes inline complexas, o Ark UI padroniza a anatomia visual de cada elemento DOM através de atributos de dados semânticos:
- **`data-scope`**: Identifica qual máquina/componente controla aquele nó DOM (ex: `data-scope="menu"`, `data-scope="color-picker"`, `data-scope="splitter"`).
- **`data-part`**: Identifica o papel atômico específico daquele elemento na árvore (ex: `data-part="root"`, `data-part="trigger"`, `data-part="positioner"`, `data-part="content"`, `data-part="thumb"`, `data-part="dropzone"`).
- **Atributos de Estado Auxiliares**: `data-state` (`"open"` | `"closed"` | `"checked"`), `data-focus`, `data-hover`, `data-active`, `data-disabled`, `data-placement`, `data-orientation`, `data-invalid`.

Essa convenção viabiliza um desacoplamento completo entre engenharia estrutural e folha de estilos: com Tailwind CSS ou Panda CSS, o desenvolvedor pode estilizar o componente inteiro mirando diretamente `[data-scope="dialog"][data-part="content"]` ou usando seletores utilitários modernos sem nunca precisar espalhar classes fragmentadas em nós internos.

#### 3. Catálogo Além do Convencional: Primitivas Ultra-Complexas
A maioria das bibliotecas headless encerra sua oferta no básico (Dialog, Dropdown, Tabs, Accordion). O Ark UI oferece mais de **45 componentes**, incluindo primitivas de altíssima complexidade de engenharia que outras bibliotecas evitam implementar:
- **`Tour`**: Guia passo a passo de onboarding com spotlight dinâmico, backdrop, gerenciamento de foco sequencial e cálculo de colisão ao redor de elementos alvos dinâmicos.
- **`SignaturePad`**: Captura de assinatura digital baseada em HTML5 `<canvas>` com cálculo de curvas Bezier vetoriais, sensibilidade à velocidade de traço, limpeza e serialização PNG/SVG nativa.
- **`ColorPicker`**: Seletor profissional completo com área 2D de saturação/valor, sliders de canal alfa/matiz, seletor de formato (HEX, RGBA, HSLA, HSBA), suporte à API nativa EyeDropper do navegador e grupos de swatches.
- **`Splitter`**: Layout de múltiplos painéis redimensionáveis estilo VS Code ou Figma, com arraste fluído por mouse/touch, navegação e redimensionamento por setas do teclado e colapso inteligente.
- **`QrCode`**: Gerador vetorial de QR Code acessível com controle de níveis de correção de erro (L, M, Q, H), suporte a logotipo central (`Overlay`) e gatilho de download direto em SVG ou PNG.
- **`TreeView`**: Árvore de arquivos e hierarquias aninhadas com navegação ARIA completa por teclado, suporte a seleção múltipla, guias visuais de indentação e provedores de nós modulares.
- **`Timer`**: Contador decrescente e cronômetro com máquina temporal desacoplada e controles granulares de pausa, reinício e formatação.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto

1. **Plataformas Multi-Framework & Organizações com Micro-Frontends**:
   Empresas com múltiplas equipes de engenharia onde um squad utiliza **React / Next.js**, outro adota **Vue 3 / Nuxt**, e ferramentas de alta performance usam **SolidJS** ou **Svelte 5**. O Ark UI permite a criação de um único Design System Corporativo canônico com a mesma árvore de tokens, os mesmos nomes de componentes (`<Dialog.Root>`, `<Dialog.Trigger>`) e o mesmo comportamento WCAG em todos os frameworks, eliminando o custo de reescrever lógica acessível em cada tecnologia.
2. **SaaS B2B Complexos & Ferramentas Estilo Desktop (Canvas, Editores, IDEs Web)**:
   Aplicações de edição gráfica, ferramentas de low-code/no-code, dashboards de observabilidade e painéis analíticos que demandam componentes avançados como painéis redimensionáveis (`Splitter`), seleção precisa de cores (`ColorPicker`), assinatura de contratos eletrônicos (`SignaturePad`) e diretórios de arquivos profundos (`TreeView`).
3. **Aplicações com Fluxos Ricos de Onboarding & Product-Led Growth (PLG)**:
   Produtos que necessitam guiar o usuário de forma imersiva por novidades da interface através do componente nativo `Tour`, sem depender de bibliotecas pesadas de terceiros (como Intro.js ou Shepherd.js) que introduzem vazamento de memória e estilos obsoletos.
4. **Design Systems Proprietários Construídos sobre Panda CSS ou Tailwind v4**:
   Equipes de produto que desejam um design system sob medida com zero runtime de CSS, onde componentes primitivos expõem APIs limpas e composáveis sem impor nenhuma decisão visual inicial.
5. **Autenticação, Fintechs e Pagamentos Seguros**:
   Aplicações financeiras que exigem campos particionados de código de autenticação multifator (`PinInput` / OTP), validação de upload de documentos fiscais (`FileUpload`), geração de chaves PIX/Crypto em tela (`QrCode`) e cópia segura de chaves com confirmação visual (`Clipboard`).

### Momento do Fluxo e Regra 60-30-10

- **Como Espinha Dorsal Funcional (60%)**:
  O Ark UI deve ser a infraestrutura de acessibilidade e ciclo de vida de todos os elementos interativos do sistema (Dialogs, Menus, Accordions, Tabs, Tooltips, Modais, Sliders). Ele gerencia o estado no nível do Zag.js e emite os atributos DOM semânticos.
- **Como Camada de Estilização Atômica & Tokens (30%)**:
  O Tailwind CSS v4, Panda CSS ou Park UI consome os atributos `data-scope` e `data-part` para aplicar as classes visuais, bordas, cores de superfície, tipografia e sombras calculadas.
- **Como Efeito Protagonista / Showstopper (10%)**:
  Componentes de alto impacto tátil — o `Tour` com seu spotlight iluminando a interface, o `SignaturePad` traçando assinaturas em tempo real, ou o `ColorPicker` manipulando gradientes no espaço Display-P3 — atuam como o centro das atenções nos momentos cruciais da jornada do usuário.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

1. **Desenvolvedores que Buscam "Componentes Prontos de Copiar e Colar sem Estilizar"**:
   O Ark UI é **100% headless (sem qualquer estilo CSS embutido)**. Se um time espera que `<Button>` ou `<Dialog.Content>` venha com cantos arredondados, fundo azul e sombras bonitas sem configuração prévia, a experiência causará frustração imediata. Para componentes prontos e pré-estilizados construídos sobre o Ark UI, o caminho correto é adotar o **Park UI** (`park-ui.com`) ou o **Chakra UI v3**.
2. **Landing Pages Estáticas Simples de Conversão Única**:
   Para uma página institucional ou portfólio minimalista de 3 seções sem modais ou formulários interativos, importar adaptadores de máquinas de estado introduz complexidade estrutural desnecessária quando tags HTML nativas (`<details>`, `<dialog>`, `<form>`) ou utilitários CSS puros bastam.
3. **Projetos com Mistura Híbrida Desorganizada de Bibliotecas Headless**:
   Misturar Ark UI e Radix UI dentro do mesmo padrão composto (por exemplo, envolver um `Ark.Menu` dentro de um `Radix.Dialog`) gera conflitos graves de *event bubbling*, captura de cliques externos (*pointerdown outside handlers*) e armadilhas de foco concorrentes no DOM. Defina uma única fundação headless para o produto.
4. **Sistemas com Restrição Crítica de Não Utilizar JavaScript para Renderização**:
   Como o Zag.js opera interpretando o ciclo de vida e eventos de ponteiro/teclado no cliente, o Ark UI requer execução de JavaScript no navegador para que a máquina de estados responda a interações dinâmicas (embora suporte SSR de markup inicial).

### ⚠️ Erros Comuns de Exagero & Anti-Padrões:

- **Ignorar os Contêineres de Posicionamento (`Positioner`)**:
  Em componentes flutuantes (Dialog, Popover, Menu, Tooltip, ColorPicker), o Ark UI separa explicitamente o nó estrutural `Positioner` do visual `Content`. Um erro clássico é aplicar estilos de fundo, bordas ou animações diretamente no `Positioner`, quebrando o cálculo de colisão e translação do Floating UI. O `Positioner` gerencia coordenadas absolutas; o `Content` recebe o estilo e as animações.
- **Estilização Frágil por Classes em vez de Seletores de Atributos**:
  Criar classes customizadas repetitivas (ex: `.my-tour-title`, `.my-tour-backdrop`) em vez de mapear regras reutilizáveis baseadas em `[data-scope="tour"][data-part="title"]` e `[data-part="backdrop"]`.
- **Desprezar o Tratamento de Saída (`Presence` e `unmountOnExit`)**:
  Animar o fechamento de modais apenas com transições CSS sem coordenar com as props `lazyMount` e `unmountOnExit`. O nó visual tentará desaparecer enquanto a máquina do Ark UI já destruiu o foco ou desancorou o elemento, causando saltos visuais (*layout flicker*).

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

O Ark UI oferece mais de 45 primitivas completas. A seguir estão catalogados os **12 componentes mais emblemáticos, poderosos e diferenciados** da biblioteca:

```
+----------------------------------------------------------------------------------------------------+
|                                    CATÁLOGO DE SHOWSTOPPERS ARK UI                                 |
+------------------------------------+----------------------------------+----------------------------+
| 1. Tour (Onboarding Guiado)        | 5. QrCode (Gerador Vetorial)     | 9. Timer (Máquina Temporal)|
| 2. SignaturePad (Assinatura HTML5) | 6. TreeView (Hierarquia Arquivos)| 10. Clipboard (Cópia Tátil)|
| 3. ColorPicker (Color Grading 2D)  | 7. PinInput (OTP Multifator)     | 11. Carousel (Touch Slider)|
| 4. Splitter (Multi-Painéis IDE)    | 8. FileUpload (Dropzone Visual)  | 12. Dialog / Sheet Modal   |
+------------------------------------+----------------------------------+----------------------------+
```

---

### 1. `Tour` (Showstopper Absoluto: Onboarding de Produto Guiado)
* **Anatomia Visual**:
  - `Tour.Root`: Controlador da máquina de estados com a lista de passos (`steps`), índice ativo e progresso.
  - `Tour.Backdrop`: Cortina escura semitransparente que bloqueia interação com o resto da tela.
  - `Tour.Spotlight`: Máscara SVG/CSS que recorta um retângulo ou círculo transparente com borda destacada e contorno iluminado exatamente sobre o elemento alvo (`target`), acompanhando sua posição e redimensionamento em tempo real.
  - `Tour.Positioner`: Contêiner flutuante calculado dinamicamente em relação ao elemento alvo.
  - `Tour.Content`: Balão de diálogo com cabeçalho, indicador de passos (`3 de 7`), corpo explicativo e rodapé de ações.
  - `Tour.Arrow` & `Tour.ArrowTip`: Seta pontiaguda que conecta o balão ao alvo.
  - `Tour.ProgressText`, `Tour.CloseTrigger`, `Tour.Actions`, `Tour.ActionTrigger`: Elementos de controle para pular, retroceder ou avançar.
* **Gatilho de Interação**: Disparado programaticamente (`tour.start()`) no primeiro login do usuário, ao liberar uma nova funcionalidade no produto ou via clique em "Fazer Tour Guiado". Suporta navegação por setas do teclado, tecla Escape para sair e clique fora configurável.
* **Onde Encaixar**: No nível global da aplicação (`App Root` / layout principal do dashboard), ancorando dinamicamente em botões da Navbar, filtros de tabelas, painéis laterais ou editores.

---

### 2. `SignaturePad` (Showstopper Corporativo: Assinatura Digital Vetorial)
* **Anatomia Visual**:
  - `SignaturePad.Root`: Contêiner pai com estados `data-disabled` e `data-empty`.
  - `SignaturePad.Label`: Rótulo de instrução ("Assine aqui com o mouse ou caneta").
  - `SignaturePad.Control`: Superfície delimitada com borda sutil, canto arredondado e plano de fundo neutro.
  - `SignaturePad.Segment`: Nó de renderização do elemento `<canvas>` interativo de alta resolução (calibrado para telas Retina com `devicePixelRatio`).
  - `SignaturePad.Guide`: Linha pontilhada horizontal sutil servindo como guia de base para a escrita da assinatura.
  - `SignaturePad.ClearTrigger`: Botão embutido com ícone de borracha/lixeira para limpar a área e reiniciar a máquina.
* **Gatilho de Interação**: Interação contínua de arrasto (*pointerdown*, *pointermove*, *pointerup*). Calcula a velocidade do traço para modular suavemente a espessura da linha (caligrafia orgânica).
* **Onde Encaixar**: Modais de fechamento de contratos jurídicos, fluxos de checkout B2B, aprovação de ordens de serviço em tablets industriais e formulários de conformidade fiscal.

---

### 3. `ColorPicker` (Showstopper Técnico: Seletor de Cores Profissional)
* **Anatomia Visual**:
  - `ColorPicker.Root`: Controlador principal do espaço de cor (HEX, RGBA, HSLA, HSBA).
  - `ColorPicker.Control` & `ColorPicker.Trigger`: Botão de acionamento exibindo a cor ativa em um pequeno círculo/quadrado (`ValueSwatch`) e o código textual.
  - `ColorPicker.Positioner` & `ColorPicker.Content`: Painel flutuante com sombra de elevação alta.
  - `ColorPicker.Area`, `AreaBackground` & `AreaThumb`: Área 2D gradiente contínua (saturação no eixo X, brilho/valor no eixo Y) com thumb circular arrastável.
  - `ColorPicker.ChannelSlider` (com `Track` e `Thumb`): Barras de deslizamento unidimensionais para ajuste do canal de Matiz (*Hue*) de 0 a 360° e Canal Alfa (*Opacidade*) de 0 a 100%.
  - `ColorPicker.EyeDropperTrigger`: Botão com ícone de conta-gotas que ativa a API nativa do navegador para capturar qualquer pixel da tela do sistema operacional.
  - `ColorPicker.SwatchGroup` & `ColorPicker.Swatch`: Paleta de cores predefinidas da marca para seleção instantânea.
  - `ColorPicker.FormatSelect` & `ColorPicker.ChannelInput`: Campos numéricos para digitação manual exata dos valores RGB/HSL.
* **Gatilho de Interação**: Clique no gatilho para abrir o painel, arraste no plano 2D ou sliders com feedback óptico contínuo em 60 FPS, seleção de amostras e conta-gotas via atalho.
* **Onde Encaixar**: Editores visuais estilo Canva/Figma, configuradores de temas e marcas em SaaS white-label, painéis de personalização de formulários e ferramentas de design system.

---

### 4. `Splitter` (Showstopper de Layout: Divisor de Painéis Redimensionáveis)
* **Anatomia Visual**:
  - `Splitter.Root`: Contêiner com orientação flexível (`orientation="horizontal"` ou `"vertical"`).
  - `Splitter.Panel`: Seções de conteúdo com propriedades de dimensionamento declarativas (`defaultSize`, `minSize`, `maxSize`, `collapsible`).
  - `Splitter.ResizeTrigger`: Barra divisora fina e interativa localizada entre dois painéis. Exibe feedback de cor sutil em repouso e realce dinâmico em hover/arraste.
  - `Splitter.ResizeTriggerIndicator`: Ícone de pegador visual opcional (3 pontos ou linha dupla) centrado na divisória.
* **Gatilho de Interação**: Arraste contínuo com mouse ou toque (*drag*), clique duplo para colapsar/expandir instantaneamente o painel, e navegação via teclado através das setas direcionais (`ArrowLeft`, `ArrowRight`, `ArrowUp`, `ArrowDown`) com suporte às teclas `Home` e `End` para limites máximos.
* **Onde Encaixar**: Layouts de produtividade estilo IDE (VS Code Web), painéis de pré-visualização de código/markdown, dashboards com árvore lateral e terminal inferior recolhível.

---

### 5. `QrCode` (Primitiva Utilitária: Gerador de Códigos QR Acessível)
* **Anatomia Visual**:
  - `QrCode.Root`: Contêiner com o valor textual/URL a ser codificado e nível de correção de erro configurável.
  - `QrCode.Frame`: Elemento SVG estrutural de tamanho fixo ou responsivo com fundo de alto contraste.
  - `QrCode.Pattern`: Malha de módulos (pontos/quadrados) gerados matematicamente sem distorção óptica.
  - `QrCode.Overlay`: Elemento visual centralizado projetado para receber o logotipo ou ícone da empresa, com cálculo de margem segura para não corromper a leitura do scanner.
  - `QrCode.DownloadTrigger`: Botão de utilidade integrado para baixar diretamente o arquivo nos formatos `.png` ou `.svg`.
* **Gatilho de Interação**: Renderização reativa a alterações de estado de dados; clique no gatilho para download imediato.
* **Onde Encaixar**: Telas de pagamento instantâneo via PIX ou Crypto, autenticação multifator com pareamento de aplicativo autenticador (Google Authenticator / 1Password) e compartilhamento rápido de links em eventos.

---

### 6. `TreeView` (Primitiva Densa: Árvore Hierárquica de Arquivos)
* **Anatomia Visual**:
  - `TreeView.Root`: Estrutura mãe com rótulo semântico e suporte a seleção única ou múltipla.
  - `TreeView.Tree`: Contêiner da lista aninhada com suporte a virtualização de linhas.
  - `TreeView.Branch`: Nó pai que contém sub-elementos (pastas ou categorias).
  - `TreeView.BranchControl`: Linha clicável contendo `BranchIndicator` (seta de expansão que rotaciona suavemente 90°), ícone de pasta e `BranchText`.
  - `TreeView.BranchContent`: Lista interna retrátil de nós filhos.
  - `TreeView.BranchIndentGuide`: Linha vertical sutil que guia o olho do usuário pela profundidade hierárquica do aninhamento.
  - `TreeView.Item`: Nó folha (arquivo ou item terminal) com `ItemIndicator` e `ItemText`.
* **Gatilho de Interação**: Clique para expandir/recolher pastas, clique duplo para abrir arquivos, navegação fluída por teclado seguindo o padrão WAI-ARIA Tree (`ArrowDown`, `ArrowUp`, `ArrowRight` para expandir, `ArrowLeft` para recolher, `*` para expandir todos os irmãos).
* **Onde Encaixar**: Barras laterais de navegação em documentações complexas, gerenciadores de arquivos de nuvem (estilo Google Drive / Dropbox), exploradores de repositórios Git e estruturas organizacionais de empresas.

---

### 7. `PinInput` (Primitiva de Segurança: Campo de Código OTP Segmentado)
* **Anatomia Visual**:
  - `PinInput.Root`: Controlador com contagem de dígitos (`length={6}`), tipo de dado (`numeric` ou `alphanumeric`) e propriedade `mask` (para ocultar dígitos sensíveis como pontos redondos).
  - `PinInput.Label`: Instrução acessível do campo.
  - `PinInput.Control`: Linha horizontal contendo as caixas de entrada separadas com espaçamento regular (`gap-2` ou `gap-3`).
  - `PinInput.Input`: Cada caixa de entrada individual, exibindo um único caractere com tipografia monospace de tamanho grande, borda nítida de foco e realce com anel de destaque.
* **Gatilho de Interação**: Digitação avança o foco instantaneamente para o próximo campo; tecla `Backspace` apaga o dígito atual e retorna o foco para o anterior; colar (`Ctrl+V` ou `Cmd+V`) distribui os 6 caracteres automaticamente através dos campos individuais em um único frame.
* **Onde Encaixar**: Telas de login com autenticação de dois fatores (2FA), confirmação de transações bancárias e validação de e-mail/SMS em fluxos de cadastro.

---

### 8. `FileUpload` (Primitiva de Upload: Zona de Arraste com Lista de Arquivos)
* **Anatomia Visual**:
  - `FileUpload.Root`: Gerenciador de restrições (tamanho máximo de arquivo, tipos MIME aceitos, limite de quantidade).
  - `FileUpload.Dropzone`: Superfície ampla com borda tracejada (`border-dashed`), fundo sutil e ícone de upload convidativo. Altera para estado ativo (`data-dragging="true"`) com destaque luminoso de cor ao aproximar arquivos.
  - `FileUpload.Trigger`: Botão secundário acessível para abrir a janela de diálogo do explorador de arquivos do sistema operacional.
  - `FileUpload.ItemGroup`: Lista ordenada contendo os arquivos selecionados ou em envio.
  - `FileUpload.Item`: Card compacto exibindo ícone de tipo de arquivo, `ItemName`, `ItemSizeText`, miniatura de pré-visualização (`ItemPreview` com imagem ou ícone) e `ItemDeleteTrigger` para remoção instantânea.
* **Gatilho de Interação**: Arrastar e soltar arquivos sobre a zona (*drag-and-drop*), clique no gatilho para seleção manual e navegação por teclado nos itens da lista com tecla `Delete` para exclusão.
* **Onde Encaixar**: Formulários de envio de anexos, upload de avatares de perfil, importação de planilhas CSV/Excel em painéis analíticos e envio de documentos para verificação KYC.

---

### 9. `Timer` (Primitiva Temporal: Máquina de Contagem Regressiva e Cronômetro)
* **Anatomia Visual**:
  - `Timer.Root`: Contêiner com propriedades de duração inicial, contagem regressiva (`countdown={true}`), auto-início e eventos (`onComplete`).
  - `Timer.Area`: Área tipográfica formatada em display digital.
  - `Timer.Item`: Segmentos temporais desacoplados (`type="days"`, `"hours"`, `"minutes"`, `"seconds"`, `"milliseconds"`).
  - `Timer.Separator`: Caractere divisor (`:`) estático ou piscante entre os segmentos.
  - `Timer.Control`: Barra de controle contendo `Timer.ActionTrigger` com ações declarativas (`action="start"`, `"pause"`, `"reset"`).
* **Gatilho de Interação**: Disparado automaticamente no carregamento ou acionado por cliques do usuário nos botões de controle de fluxo de tempo.
* **Onde Encaixar**: Banners de ofertas com tempo limitado em e-commerce (Black Friday / Flash Sales), contadores regressivos para reenvio de código SMS (ex: "Aguarde 45s"), plataformas de exames/testes online e temporizadores de sessões expirando por inatividade.

---

### 10. `Clipboard` (Micro-Primitiva: Cópia Tátil com Feedback Visual)
* **Anatomia Visual**:
  - `Clipboard.Root`: Controlador que armazena a string a ser copiada e a duração do estado de confirmação (`timeout={2000}`).
  - `Clipboard.Control`: Layout agrupando o valor visível e o botão.
  - `Clipboard.Input`: Campo de texto somente leitura com estilo visual limpo exibindo a chave ou link.
  - `Clipboard.Trigger`: Botão interativo que recebe foco e clique.
  - `Clipboard.Indicator`: Componente polimórfico de troca de ícone — exibe o ícone de copiar (`Copy`) em repouso e alterna automaticamente para o ícone de confirmação (`Check`) com animação de escala quando o texto é enviado com sucesso à área de transferência do sistema.
* **Gatilho de Interação**: Clique no botão ou pressionamento das teclas `Enter` / `Space` no foco. Executa a API assíncrona `navigator.clipboard.writeText` com fallback seguro.
* **Onde Encaixar**: Chaves de API e tokens de autenticação em Developer Settings, links de convite de equipes em painéis SaaS, chaves públicas de carteiras de criptomoedas e snippets de código de instalação em documentações técnicas.

---

### 11. `Carousel` (Primitiva de Conteúdo: Sliders Acessíveis por Gestos e Teclado)
* **Anatomia Visual**:
  - `Carousel.Root`: Gerenciador de slides com parâmetros de paginação contínua (*loop*), espaçamento e orientação.
  - `Carousel.ItemGroup`: Contêiner rolável com aceleração gráfica e física de atrito de arraste.
  - `Carousel.Item`: Cada slide individual com atribuição de índice (`index={i}`).
  - `Carousel.Control`: Barra de controle com botões direcionais (`PrevTrigger` e `NextTrigger`).
  - `Carousel.IndicatorGroup` & `Carousel.Indicator`: Barra de pontos (*dots*) de paginação que refletem o slide atual e permitem salto direto para qualquer tela.
* **Gatilho de Interação**: Deslize por toque no mobile (*touch swipe*), arraste de mouse com inércia no desktop, clique nos botões/indicadores e navegação completa por setas do teclado com atributo `aria-roledescription="slide"`.
* **Onde Encaixar**: Carrosséis de depoimentos em páginas de conversão, galerias de fotos de produtos em e-commerce, cards de cases de clientes e seções de visualização de métricas em dashboards móveis.

---

### 12. `Dialog` & `Popover` (Primitivas Modais com Posicionamento Inteligente)
* **Anatomia Visual**:
  - `Dialog.Root`: Controlador de abertura e fechamento modal.
  - `Dialog.Trigger`: Elemento de disparo associado via `asChild`.
  - `Portal`: Renderizador desacoplado que teleporta a árvore modal para a raiz do documento (`document.body`), impedindo problemas de `z-index` e `overflow: hidden`.
  - `Dialog.Backdrop`: Cortina de desfoque (`backdrop-blur-sm`) e escurecimento.
  - `Dialog.Positioner`: Contêiner flexível de centralização óptica no viewport.
  - `Dialog.Content`: Superfície principal do modal com elevação, bordas, cabeçalho (`Dialog.Title`), descrição acessível (`Dialog.Description`) e `Dialog.CloseTrigger`.
* **Gatilho de Interação**: Clique no trigger, atalho de teclado `Escape` para fechar, clique fora do conteúdo (*pointerdown outside*), restauração instantânea do foco ao elemento original que abriu o modal após o fechamento.
* **Onde Encaixar**: Telas de confirmação de ações destrutivas, modais de configurações complexas, painéis laterais de detalhes (*sheets*) e popovers contextuais de ajuda.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

O Ark UI fornece pacotes independentes para cada ecossistema de framework, todos consumindo a mesma engine lógica do Zag.js:

```bash
# Para projetos React (Next.js, Vite, Remix):
npm install @ark-ui/react lucide-react clsx tailwind-merge

# Para projetos Vue 3 (Nuxt 3, Vite):
npm install @ark-ui/vue lucide-vue-next

# Para projetos Svelte (SvelteKit, Svelte 5):
npm install @ark-ui/svelte lucide-svelte

# Para projetos SolidJS (SolidStart):
npm install @ark-ui/solid lucide-solid
```

### O Modelo de Execução das Máquinas de Estado Zag.js

O diagrama a seguir sintetiza como um componente do Ark UI processa intenções do usuário em eventos e estados no DOM:

```
[ Usuário: Clique / Tecla / Arraste ]
                |
                v
+-------------------------------+
|  Ark UI Component Adapter     | (JSX / Template Declarativo)
|  (ex: @ark-ui/react)          |
+---------------+---------------+
                | Dispara Evento (send("TRIGGER_CLICK"))
                v
+-------------------------------+
|  Zag.js State Machine         | -> Avalia Transição de Estado
|  (Pure TypeScript FSM)        | -> Executa Ações (ex: calcular foco, calcular colisão)
+---------------+---------------+
                | Emite Prop Getters e Atributos de Estado
                v
+-------------------------------+
|  DOM Real Renderizado         |
|  - data-scope="tour"          |
|  - data-part="content"        | -> Estilizado por Tailwind / Panda CSS
|  - data-state="open"          | -> Animado por CSS Transitions ou Motion
+-------------------------------+
```

### Física de Movimento, Transições e Curvas

O Ark UI utiliza atributos nativos como `data-state="open"` e `data-state="closed"`. Para animações perfeitas sem layout shift, a melhor prática é combinar os seletores de atributos com curvas de aceleração do sistema:

| Tipo de Movimento | Curva / Parâmetro | Duração / Configuração | Aplicação Recomendada |
| :--- | :--- | :--- | :--- |
| **Abertura de Diálogos & Modais** | `cubic-bezier(0.16, 1, 0.3, 1)` (Deceleração Fluida) | `240ms` | Escala de `96%` para `100%`, opacidade de `0` para `1`. |
| **Fechamento de Diálogos** | `cubic-bezier(0.4, 0, 1, 1)` (Aceleração Rápida) | `160ms` | Escala de `100%` para `97%`, opacidade de `1` para `0`. |
| **Menu Popover / Tooltips** | `cubic-bezier(0.2, 0, 0, 1)` | `150ms` | Deslocamento de `Y: -4px` para `0px` com fade. |
| **Spotlight do Tour (Spring)** | `stiffness: 300, damping: 28, mass: 0.8` | Física Contínua | Transição suave da máscara ao saltar entre elementos de tamanhos diferentes. |
| **Thumb do Slider / Splitter** | `cubic-bezier(0.25, 1, 0.5, 1)` | `120ms` | Efeito de escala ao pressionar (`scale-110`). |

---

### Receita 1: Implementação de Onboarding Interativo com `Tour` em React + Tailwind CSS

O exemplo a seguir ilustra um fluxo de onboarding completo com máscara de spotlight, cálculo de passos, backdrop e balão posicionado com navegação acessível:

```tsx
"use client"

import * as React from "react"
import { Tour, createTour } from "@ark-ui/react/tour"
import { Portal } from "@ark-ui/react/portal"
import { 
  Sparkles, 
  ChevronRight, 
  ChevronLeft, 
  X, 
  CheckCircle2 
} from "lucide-react"

// 1. Definição declarativa dos passos do Tour
const tourConfig = createTour({
  id: "app-onboarding",
  steps: [
    {
      id: "step-metrics",
      title: "Painel de Métricas em Tempo Real",
      description: "Acompanhe seus dados de conversão e faturamento diário atualizados a cada 3 segundos.",
      target: () => document.getElementById("analytics-card"),
    },
    {
      id: "step-export",
      title: "Exportação Segura de Relatórios",
      description: "Gere arquivos em formato CSV, Excel e PDF assinados digitalmente com apenas um clique.",
      target: () => document.getElementById("export-button"),
    },
    {
      id: "step-settings",
      title: "Controle de Permissões Granulares",
      description: "Configure papéis de acesso (RBAC), chaves de API criptografadas e webhooks seguros.",
      target: () => document.getElementById("settings-tab"),
    },
  ],
})

export function ProductTourGuide() {
  const [tour] = React.useState(() => tourConfig)

  return (
    <Tour.Root tour={tour}>
      <Portal>
        {/* Cortina escura semitransparente */}
        <Tour.Backdrop className="fixed inset-0 z-50 bg-black/60 backdrop-blur-[2px] transition-opacity duration-300 data-[state=open]:animate-in data-[state=closed]:animate-out data-[state=closed]:fade-out-0 data-[state=open]:fade-in-0" />

        {/* Máscara de recorte do Spotlight iluminando o elemento alvo */}
        <Tour.Spotlight className="fixed z-50 rounded-xl ring-4 ring-indigo-500/80 shadow-[0_0_40px_rgba(99,102,241,0.4)] transition-all duration-300 ease-out" />

        {/* Posicionador flutuante conectado ao alvo com detecção de colisão */}
        <Tour.Positioner className="z-50 focus:outline-none">
          <Tour.Content className="relative w-84 sm:w-96 rounded-2xl border border-zinc-200 bg-white p-5 shadow-2xl dark:border-zinc-800 dark:bg-zinc-950 text-zinc-900 dark:text-zinc-50 transition-all duration-200">
            {/* Seta indicadora apontando para o alvo */}
            <Tour.Arrow className="fill-white dark:fill-zinc-950">
              <Tour.ArrowTip className="border-t border-l border-zinc-200 dark:border-zinc-800" />
            </Tour.Arrow>

            {/* Cabeçalho do Card */}
            <div className="flex items-start justify-between gap-3">
              <div className="flex items-center gap-2">
                <span className="flex h-7 w-7 items-center justify-center rounded-lg bg-indigo-50 text-indigo-600 dark:bg-indigo-950 dark:text-indigo-400">
                  <Sparkles className="h-4 w-4" />
                </span>
                <Tour.Title className="text-base font-semibold leading-tight tracking-tight" />
              </div>
              <Tour.CloseTrigger className="rounded-lg p-1 text-zinc-400 hover:bg-zinc-100 hover:text-zinc-700 dark:hover:bg-zinc-800 dark:hover:text-zinc-200 transition-colors">
                <X className="h-4 w-4" />
              </Tour.CloseTrigger>
            </div>

            {/* Descrição do Passo */}
            <Tour.Description className="mt-2.5 text-xs sm:text-sm leading-relaxed text-zinc-600 dark:text-zinc-400" />

            {/* Rodapé com Indicador de Progresso e Ações */}
            <div className="mt-5 flex items-center justify-between border-t border-zinc-100 pt-3 dark:border-zinc-800/80">
              <Tour.ProgressText className="text-xs font-medium text-zinc-500 dark:text-zinc-400" />

              <Tour.Actions className="flex items-center gap-2">
                <Tour.ActionTrigger
                  action="prev"
                  className="inline-flex items-center gap-1 rounded-lg border border-zinc-200 px-2.5 py-1.5 text-xs font-medium text-zinc-700 hover:bg-zinc-50 dark:border-zinc-800 dark:text-zinc-300 dark:hover:bg-zinc-900 transition-colors disabled:opacity-40"
                >
                  <ChevronLeft className="h-3.5 w-3.5" />
                  Voltar
                </Tour.ActionTrigger>

                <Tour.ActionTrigger
                  action="next"
                  className="inline-flex items-center gap-1 rounded-lg bg-indigo-600 px-3 py-1.5 text-xs font-medium text-white shadow hover:bg-indigo-500 active:scale-95 transition-all"
                >
                  Próximo
                  <ChevronRight className="h-3.5 w-3.5" />
                </Tour.ActionTrigger>
              </Tour.Actions>
            </div>
          </Tour.Content>
        </Tour.Positioner>
      </Portal>
    </Tour.Root>
  )
}
```

---

### Receita 2: Implementação de um `ColorPicker` Profissional em React + Tailwind CSS

Um seletor de cores completo com área 2D de saturação/valor, sliders de matiz e opacidade, conta-gotas e swatches predefinidos:

```tsx
"use client"

import { ColorPicker, parseColor } from "@ark-ui/react/color-picker"
import { Pipette, Check } from "lucide-react"

const brandPresets = [
  "#09090b", "#64748b", "#3b82f6", 
  "#6366f1", "#10b981", "#f59e0b", "#ef4444"
]

export function AdvancedColorPicker({ 
  value = "#6366f1", 
  onChange 
}: { 
  value?: string; 
  onChange?: (color: string) => void 
}) {
  return (
    <ColorPicker.Root
      value={parseColor(value)}
      onValueChange={(details) => onChange?.(details.valueAsString)}
      className="flex flex-col gap-1.5 font-sans"
    >
      <ColorPicker.Label className="text-xs font-medium text-zinc-700 dark:text-zinc-300">
        Cor Primária de Destaque
      </ColorPicker.Label>

      <ColorPicker.Control className="flex items-center gap-2">
        {/* Gatilho visual com a cor selecionada */}
        <ColorPicker.Trigger className="inline-flex h-9 items-center gap-2.5 rounded-lg border border-zinc-200 bg-white px-3 text-xs shadow-sm dark:border-zinc-800 dark:bg-zinc-900 hover:border-zinc-300 dark:hover:border-zinc-700 transition-colors">
          <ColorPicker.ValueSwatch className="h-4 w-4 rounded-full border border-black/10 shadow-inner" />
          <span className="font-mono text-zinc-800 dark:text-zinc-200 uppercase">
            {value}
          </span>
        </ColorPicker.Trigger>
      </ColorPicker.Control>

      <ColorPicker.Positioner className="z-50">
        <ColorPicker.Content className="w-64 rounded-2xl border border-zinc-200 bg-white p-3.5 shadow-xl dark:border-zinc-800 dark:bg-zinc-950 flex flex-col gap-3">
          {/* Área 2D para saturação e brilho */}
          <ColorPicker.Area className="relative h-36 w-full rounded-lg overflow-hidden border border-zinc-200 dark:border-zinc-800 cursor-crosshair">
            <ColorPicker.AreaBackground className="h-full w-full" />
            <ColorPicker.AreaThumb className="h-4 w-4 -translate-x-1/2 -translate-y-1/2 rounded-full border-2 border-white shadow-md focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-indigo-500" />
          </ColorPicker.Area>

          {/* Slider de Matiz (Hue) */}
          <div className="flex flex-col gap-1">
            <ColorPicker.ChannelSlider channel="hue" className="relative flex h-3 w-full items-center">
              <ColorPicker.ChannelSliderTrack className="h-2.5 w-full rounded-full" />
              <ColorPicker.ChannelSliderThumb className="h-4 w-4 -translate-x-1/2 rounded-full border-2 border-white bg-white shadow focus-visible:outline-none" />
            </ColorPicker.ChannelSlider>
          </div>

          {/* Slider de Transparência (Alpha) */}
          <div className="flex flex-col gap-1">
            <ColorPicker.ChannelSlider channel="alpha" className="relative flex h-3 w-full items-center">
              <ColorPicker.ChannelSliderTrack className="h-2.5 w-full rounded-full" />
              <ColorPicker.ChannelSliderThumb className="h-4 w-4 -translate-x-1/2 rounded-full border-2 border-white bg-white shadow focus-visible:outline-none" />
            </ColorPicker.ChannelSlider>
          </div>

          {/* Ferramentas: Conta-Gotas e Input Hex */}
          <div className="flex items-center gap-2 pt-1 border-t border-zinc-100 dark:border-zinc-800">
            <ColorPicker.EyeDropperTrigger className="inline-flex h-8 w-8 items-center justify-center rounded-lg border border-zinc-200 text-zinc-600 hover:bg-zinc-100 dark:border-zinc-800 dark:text-zinc-400 dark:hover:bg-zinc-900 transition-colors">
              <Pipette className="h-4 w-4" />
            </ColorPicker.EyeDropperTrigger>

            <ColorPicker.ChannelInput
              channel="hex"
              className="h-8 flex-1 rounded-lg border border-zinc-200 bg-zinc-50 px-2.5 font-mono text-xs uppercase text-zinc-800 dark:border-zinc-800 dark:bg-zinc-900 dark:text-zinc-200 focus:outline-none focus:ring-1 focus:ring-indigo-500"
            />
          </div>

          {/* Swatches de Cores Predefinidas */}
          <ColorPicker.SwatchGroup className="flex items-center justify-between gap-1 pt-1">
            {brandPresets.map((hex) => (
              <ColorPicker.SwatchTrigger key={hex} value={hex} className="group relative">
                <ColorPicker.Swatch
                  value={hex}
                  className="h-6 w-6 rounded-md border border-black/10 shadow-sm transition-transform group-hover:scale-110"
                />
              </ColorPicker.SwatchTrigger>
            ))}
          </ColorPicker.SwatchGroup>
        </ColorPicker.Content>
      </ColorPicker.Positioner>
    </ColorPicker.Root>
  )
}
```

---

### Receita 3: Implementação de `PinInput` (Código de Autenticação 2FA / OTP)

Campo particionado de alta fidelidade para códigos de segurança com auto-foco e distribuição de caracteres colados:

```tsx
"use client"

import { PinInput } from "@ark-ui/react/pin-input"

export function TwoFactorAuthInput({ onComplete }: { onComplete?: (pin: string) => void }) {
  return (
    <PinInput.Root
      length={6}
      otp
      autoFocus
      onValueComplete={(details) => onComplete?.(details.valueAsString)}
      className="flex flex-col items-center gap-3"
    >
      <PinInput.Label className="text-sm font-medium text-zinc-700 dark:text-zinc-300">
        Digite o código de verificação de 6 dígitos
      </PinInput.Label>

      <PinInput.Control className="flex items-center gap-2 sm:gap-3">
        {[0, 1, 2, 3, 4, 5].map((id, index) => (
          <PinInput.Input
            key={id}
            index={index}
            className="h-12 w-10 sm:h-14 sm:w-12 rounded-xl border border-zinc-300 bg-white text-center font-mono text-lg font-semibold text-zinc-900 shadow-sm transition-all focus:border-indigo-600 focus:ring-2 focus:ring-indigo-500/20 focus:outline-none dark:border-zinc-700 dark:bg-zinc-900 dark:text-zinc-100 dark:focus:border-indigo-400"
          />
        ))}
      </PinInput.Control>
    </PinInput.Root>
  )
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar a arquitetura técnica de uma nova interface que utilizará o **Ark UI**, o Agente de Arquitetura deve incluir e validar os seguintes itens estruturais:

### 1. Declaração de Stack & Camada Headless
- Registrar no blueprint:
  ```markdown
  - **Headless Engine**: Ark UI (`@ark-ui/react` v3+ ou adaptador do framework escolhido).
  - **State Machine Engine**: Zag.js (`@zag-js/*`).
  - **Styling Architecture**: Tailwind CSS v4 / v3 com seletores de atributos (`data-scope`, `data-part`, `data-state`).
  - **Design System Bridge (Opcional)**: Park UI (`park-ui.com`) para blocos de cópia rápida.
  ```

### 2. Mapeamento de Componentes Críticos
- Sempre que a especificação exigir funcionalidades avançadas, priorizar os componentes nativos do Ark UI antes de instalar bibliotecas pontuais e pesadas:
  - Para onboarding passo a passo: usar `Tour` (dispensa Intro.js, Shepherd ou react-joyride).
  - Para captura de assinaturas: usar `SignaturePad` (dispensa react-signature-canvas).
  - Para seleção de cores corporativas: usar `ColorPicker` (dispensa react-color).
  - Para layout com painéis redimensionáveis: usar `Splitter` (dispensa react-resizable-panels).
  - Para código de verificação de 2 fatores: usar `PinInput` (dispensa react-otp-input).
  - Para geração de códigos PIX/URL: usar `QrCode` (dispensa qrcode.react).

### 3. Convenção de Seletores e Nomenclatura CSS
- Adotar expressamente a convenção de atributos do Ark UI nos tokens e estilos:
  - Usar `[data-scope="..."][data-part="..."]` para escopo de elementos atômicos.
  - Para estados dinâmicos, utilizar `data-[state=open]`, `data-[state=closed]`, `data-[disabled]`, `data-[active]`.
  - Nunca estilizar o contêiner `Positioner` com decorações visuais (fundos, sombras ou bordas). Manter o `Positioner` estritamente como agente de coordenadas flutuantes e aplicar estilos no nó `Content`.

### 4. Gestão de Ciclo de Vida e Acessibilidade W3C
- Declarar o uso obrigatório de `Portal` em todos os elementos flutuantes (`Dialog`, `Menu`, `Tour`, `Popover`) para evitar armadilhas de contexto de empilhamento (`z-index`) e estouro de contêiner (`overflow-hidden`).
- Habilitar `lazyMount` e `unmountOnExit` para componentes pesados com conteúdo volumoso (como modais de formulário, abas secundárias e tabelas embutidas) visando manter a árvore do DOM enxuta e a pontuação do Google Lighthouse no nível máximo.
