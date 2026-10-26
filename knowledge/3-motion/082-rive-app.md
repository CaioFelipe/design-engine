---
id: "rive-app"
name: "Rive (Rive.app — Real-Time Interactive Vector Animation & State Machine Engine)"
url: "https://rive.app/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["State Machine Logic", "Hardware-Accelerated Vector Graphics", "Skeletal Rigging & Inverse Kinematics", "Mesh Deformation & Skinning", "Data-Bound Dynamic Graphics", "Zero-Lag Haptic Micro-Interactions"]
densidade_informacao: "Media a Alta"
impacto_visual: "Moderado a Cinematografico/Showstopper"
custo_computacional: "Baixo a Medio (Rive Renderer GPU nativo C++/Wasm via WebGL2/WebGPU/Metal)"
stack_frameworks: ["React 19 / 18 (@rive-app/react-canvas, @rive-app/react-webgl2)", "Next.js App Router", "TypeScript", "Tailwind CSS v4 / v3", "WebAssembly (Wasm)", "Flutter / iOS / Android / C++ / Unreal / Unity"]
compatibilidade:
  combinacoes_recomendadas: ["Shadcn UI + @rive-app/react-canvas", "Tailwind CSS + Rive Responsive Layouts", "Zustand / TanStack Query + Rive Data Binding View Models", "Lenis Scroll + Rive Scroll Progress Inputs", "Framer Motion (orquestração de layout) + Rive (vetores interativos internos)"]
  conflitos_esteticos: ["Páginas editoriais e tipográficas puras sem elementos dinâmicos", "Interfaces corporativas estáticas onde simples CSS transitions de 150ms resolvem o problema sem necessidade de canvas WebGL", "Instâncias simultâneas desordenadas sem IntersectionObserver causando concorrência desnecessária de WebGL contexts"]
---

# Rive — Dossiê de Física de Movimento, Transições & State Machines Vetoriais

## 1. Filosofia de Movimento & Sensação Física (Feel)

O **Rive** (`https://rive.app/`), criado pelos irmãos **Guido Rosso** e **Luigi Rosso** (fundadores originais da plataforma 2Dimensions), representa a mais profunda mudança de paradigma na história do motion design interativo desde o lançamento do Macromedia Flash e do Airbnb Lottie. O Rive não é uma ferramenta de exportação de vídeo nem um renderizador passivo de animações lineares pré-computadas: ele é um **motor gráfico vetorial e uma linguagem de execução de estados em tempo real baseada em código e física nativa**.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        O PARADIGMA RIVE: ANIMAÇÃO REATIVA vs LINEAR                    │
└────────────────────────────────────────────────────────────────────────────────────────┘

    MODELO TRADICIONAL (Lottie / After Effects / Vídeo):
    ┌───────────────┐        Linha de Tempo Rígida (0s a 3.5s)        ┌───────────────┐
    │  Frame Inicial │ ───────────────────────────────────────────────▶│  Frame Final  │
    └───────────────┘   (Interação exige fatiar em trechos ou loops)   └───────────────┘
                                       ▼
             * Sem noção de lógica interna.
             * Mudança de direção requer reinício abrupto ou saltos de quadro.
             * Alto consumo de CPU parseando JSON frame a frame.

    MODELO RIVE (State Machines & Entradas Contínuas em Tempo Real):
    ┌──────────────────────────────────────────────────────────────────────────────────┐
    │                                RIVE STATE MACHINE                                │
    │                                                                                  │
    │         ┌───────────┐    input: isHover=true    ┌───────────────┐                │
    │         │   IDLE    │ ────────────────────────▶ │   HOVERING    │                │
    │         └───────────┘ ◀──────────────────────── └───────────────┘                │
    │               │          input: isHover=false           │                        │
    │               │                                         │ trigger: onClick       │
    │               │ trigger: onReset                        ▼                        │
    │               │                                 ┌───────────────┐                │
    │               └──────────────────────────────── │    SUCCESS    │                │
    │                                                 └───────────────┘                │
    │                                                         ▲                        │
    │                input: pointerX/Y (0..100)               │                        │
    │         [ 2D Blend Tree: Olhos seguem o cursor ] ───────┘                        │
    └──────────────────────────────────────────────────────────────────────────────────┘
```

### A Ruptura com o Passado: Por que o Lottie e o After Effects Chegaram ao Limite

Durante quase uma década, o padrão da indústria para micro-animações na web e em aplicativos móveis foi a exportação de composições do Adobe After Effects através do plugin Bodymovin para arquivos JSON interpretados pelo player **Lottie**. Embora o Lottie tenha democratizado a fidelidade vetorial, sua arquitetura técnica sofre de deficiências intrínsecas:

1. **Passividade Linear (Timeline Rígida)**: Uma animação Lottie é um rolo de filme digital gravado. Ela não possui inteligência; para fazê-la responder a um clique ou a um hover, o desenvolvedor precisa escrever código imperativo complexo, controlando segmentos de quadros (`playSegments([20, 45], true)`), o que invariavelmente gera pulos visuais (*jitter*), interpolações cortadas e lógica de UI fragmentada.
2. **Gargalo de Performance do Parser JSON**: Arquivos Lottie complexos frequentemente pesam entre centenas de kilobytes e vários megabytes de JSON puro. No carregamento, a CPU principal da thread do JavaScript precisa desserializar árvores profundas de objetos, consumindo memória e causando engasgos na renderização inicial (*Long Tasks* / TBT).
3. **Renderização CPU / Canvas2D Antiga**: O renderizador web tradicional do Lottie depende do Canvas 2D da CPU ou de centenas de nós SVG injetados no DOM. Em gráficos detalhados, o navegador precisa recalcular estilos, recalcular o layout da árvore DOM e realizar redesenhos contínuos, esgotando a bateria de dispositivos móveis.

### Os Pilares Arquiteturais do Rive

O Rive resolveu essas limitações reconstruindo a pilha gráfica do zero:

1. **O Formato Binário Compacto (`.riv`)**:
   Em vez de texto JSON verboso, o Rive compila os vetores, esqueletos, curvas e nós lógicos em um formato binário proprietário ultracompacto (`.riv`), que frequentemente atinge reduções de **80% a 95% em relação ao equivalente Lottie**. Arquivos completos de personagens com dezenas de animações e rigging esquelético chegam a pesar meros 15KB a 60KB. O runtime lê esse fluxo de bytes diretamente na memória linear do WebAssembly sem sobrecarga de parser no JavaScript.

2. **O Rive Renderer (GPU Vector Engine)**:
   A equipe do Rive (incluindo pioneiros em renderização vetorial acelerada por hardware) projetou um renderizador próprio escrito em C++ com binding em WebAssembly. Ao contrário de bibliotecas genéricas, o **Rive Renderer** desenha caminhos vetoriais, curvas de Bézier cúbicas, preenchimentos gradientes e máscaras de corte **diretamente nos shaders da GPU** (utilizando WebGL2, WebGPU, Metal, Vulkan e Direct3D). A GPU computa o preenchimento vetorial de forma paralela, sustentando taxas estáveis de 60 a 120 FPS com consumo insignificante de CPU.

3. **State Machines Nativas no Asset**:
   No Rive, a interatividade não é programada externamente no React ou no Flutter; **ela é projetada pelo designer dentro da State Machine do arquivo `.riv`**. O arquivo exportado já contém a máquina de estados finitos, com suas camadas (*Layers*), transições interpoladas por molas ou curvas cúbicas, nós de mescla (*1D and 2D Blend Trees*) e ouvintes de ponteiro (*Pointer Listeners*). A aplicação hospedeira só precisa enviar valores para entradas estritamente tipadas:
   - **Boolean Inputs** (ex: `isHovered`, `isDarkMode`, `isLoading`)
   - **Number Inputs** (ex: `cursorX`, `cursorY`, `batteryPercent`, `scrollOffset`)
   - **Trigger Inputs** (ex: `submit`, `errorPulse`, `celebrateBurst`)

4. **Rigging Esquelético, Bones & Inverse Kinematics (IK)**:
   Em vez de desenhar e animar caminhos vetoriais ponto a ponto para cada pose, o Rive permite estruturar ilustrações com **ossos (Bones), restrições de Cinemática Inversa (IK Constraints) e deformação de malha (Mesh Skinning)**. Isso permite que um personagem ou braço mecânico aponte para as coordenadas do mouse em tempo real, calculando os ângulos das articulações proceduralmente na GPU com zero custo de armazenamento de frames adicionais.

5. **Data Binding & View Models**:
   As versões modernas do Rive introduziram o conceito de **View Models** desacoplados. Designers definem estruturas de dados reativas (Strings, Numbers, Booleans, Colors) vinculadas a textos dinâmicos (*Dynamic Rive Text*), barras de progresso e temas visuais dentro da própria arte. O frontend simplesmente conecta seu estado (ex: Store do Zustand ou resposta de API) às propriedades do View Model da instância do Rive, atualizando nomes de usuário, valores de moedas ou cores de branding instantaneamente.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

O Rive é o padrão de ouro da indústria quando a interface necessita de dinamismo orgânico que responda a ações do usuário sem a rigidez de animações pré-gravadas.

### Casos Reais de Alto Sucesso na Indústria

* **Duolingo (O Caso Emblemático Mundial)**:
  O Duolingo substituiu toda a sua infraestrutura gráfica móvel e web (antes baseada em sprite sheets e Lottie) pelo Rive. A mascote Duo (a coruja) e todos os avatares do ecossistema agora utilizam State Machines do Rive com rigging esquelético. A mascote olha com curiosidade para onde o estudante toca, celebra com pulos exuberantes quando a resposta está certa e demonstra cansaço sutil quando o tempo está esgotando. Essa transição reduziu o tamanho dos pacotes do aplicativo em dezenas de megabytes e cortou o consumo de bateria em testes contínuos.
* **Figma**:
  Utiliza o Rive para micro-interações internas de alta fidelidade e widgets de comunidade que exigem responsividade vetorial com peso quase nulo.
* **Spotify**:
  Emprega animações interativas e telas comemorativas personalizadas (*Spotify Wrapped*, animações táteis de botões de curtir e carrosséis comemorativos) que reagem dinamicamente à batida da música e aos gestos do usuário.
* **Vercel**:
  Landing pages com diagramas de infraestrutura interativos onde fios luminosos, conexões de servidores e métricas de latência reagem ao scroll e ao ponteiro do desenvolvedor com nitidez vetorial retina.

---

### A Regra 60-30-10 no Ecossistema Rive

A incorporação do Rive em um Design System deve seguir uma disciplina rigorosa de proporção para evitar sobrecarga cognitiva e poluição visual:

```
┌───────────────────────────────────────────────────────────────────────────────────────┐
│                       DISTRIBUIÇÃO DA REGRA 60-30-10 COM O RIVE                       │
├──────────────────────────┬────────────────────────────┬───────────────────────────────┤
│      60% DO SISTEMA      │       30% DO SISTEMA       │        10% DO SISTEMA         │
│     ESTRUTURA BASE       │     MICRO-ESTADOS TÁTEIS   │      SHOWSTOPPER INTERATIVO   │
├──────────────────────────┼────────────────────────────┼───────────────────────────────┤
│ • Layout Shadcn / HTML   │ • Rive Interactive Toggles │ • Mascote / Personagem Hero   │
│ • Tipografia estática    │ • Micro-ícones animados    │ • Onboarding Interativo       │
│ • Espaçamento & Grids    │ • Indicadores de Status    │ • Diagrama de Arquitetura     │
│ • Tabelas e dados puros  │ • Botões de Check/Favorito │ • Dynamic Game HUD            │
└──────────────────────────┴────────────────────────────┴───────────────────────────────┘
```

* **60% — Estrutura e Estabilidade**: A espinha dorsal do software permanece estruturada em nós HTML/CSS acessíveis e estáticos. Menus de navegação primários, textos longos de leitura, formulários convencionais e tabelas analíticas nunca devem ser desenhados dentro de um canvas Rive para não comprometer a acessibilidade do leitor de tela, a cópia de texto e o SEO.
* **30% — Micro-Estados Táteis**: Pequenas instâncias isoladas do Rive substituem componentes de UI que se beneficiam de transições orgânicas contínuas. Exemplos: um botão de alternância *Light/Dark Mode* com morphing físico de sol e lua, um switch de checkout com micro-engrenagens ou um ícone de status de conexão com ondas pulsantes alimentadas por latência real.
* **10% — Showstopper Interativo**: O grande destaque da página ou do fluxo: a mascote de login que reage aos campos preenchidos, o mapa estelar interativo na Hero Section ou a tela de conclusão de onboarding que dispara uma celebração vetorial com física de confetes calculada em tempo real na GPU.

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

Embora o Rive seja extremamente rápido e eficiente, seu uso irrestrito sem governança de engenharia pode degradar a experiência do usuário.

### ⚠️ Quando Evitar (Anti-Padrões Notórios)

1. **Substituição de Tipografia Básica e Conteúdo Textual por Vetores do Rive**:
   Nunca renderize parágrafos de texto corrido, títulos semânticos de SEO (`h1`, `h2`) ou termos de serviço dentro de um canvas Rive. Embora o Rive suporte fontes e textos dinâmicos com *Rive Text*, textos em canvas não são nativamente selecionáveis pelo usuário, quebram comandos nativos de busca na página (`Cmd+F`) e exigem pontes complexas de acessibilidade ARIA.
2. **Proliferação Descontrolada de Contextos WebGL (Canvas Explosion)**:
   Navegadores modernos (especialmente no Safari Mobile / WebKit no iOS) possuem limites estritos para o número de contextos WebGL ativos simultaneamente (frequentemente entre 8 e 16 contextos ativos por página). Criar 40 instâncias de `<canvas>` Rive em uma lista de feed sem virtualização ou pooling fará com que o navegador destrua silenciosamente contextos anteriores (*WebGL Context Lost*), deixando caixas pretas na tela.
3. **Animações Contínuas em Elementos Fora da Tela (Off-Screen Bleed)**:
   Manter um loop de animação do Rive ativo quando o elemento rolou para fora da tela consome ciclos de GPU desnecessários e descarrega a bateria de laptops e celulares. **É obrigatório utilizar `IntersectionObserver` para pausar instâncias invisíveis**.
4. **Sobrecarga de Estado sem Hierarquia Temporal**:
   Criar State Machines com dezenas de transições concorrentes sem controle de estados intermediários pode resultar em animações caóticas, com interpolações conflitantes caso o usuário clique freneticamente no componente.

---

### ⚠️ Regras de Acessibilidade & Gestão de GPU

```tsx
// Diretriz de Segurança: Pausa automática por acessibilidade e visibilidade
import { useEffect } from "react";
import { useRive } from "@rive-app/react-canvas";

export function AccessibleRiveWrapper({ src, stateMachine }: { src: string; stateMachine: string }) {
  const { rive, RiveComponent } = useRive({
    src,
    stateMachines: stateMachine,
    autoplay: true,
  });

  useEffect(() => {
    if (!rive) return;

    // 1. Respeito estrito à preferência do usuário do SO por movimento reduzido
    const mediaQuery = window.matchMedia("(prefers-reduced-motion: reduce)");
    if (mediaQuery.matches) {
      rive.pause();
    }

    const handleChange = (e: MediaQueryListEvent) => {
      if (e.matches) {
        rive.pause();
      } else {
        rive.play();
      }
    };

    mediaQuery.addEventListener("change", handleChange);
    return () => mediaQuery.removeEventListener("change", handleChange);
  }, [rive]);

  return <RiveComponent role="img" aria-label="Animação interativa vetorial" />;
}
```

* **Acessibilidade (`prefers-reduced-motion`)**: Se o usuário declarou no sistema operacional que sofre de sensibilidade vestibular ou enxaqueca com movimentos, a animação deve pausar imediatamente no frame de repouso mais claro, ou alternar para um gráfico estático.
* **Fallback de Canvas**: Adicione tags semânticas acessíveis (`role="img"` e `aria-label` descritivo) no container do canvas para que softwares de tecnologia assistiva compreendam o papel daquele elemento.

---

## 4. Catálogo Detalhado de Componentes / Padrões Notáveis

Abaixo estão descritos **9 componentes e padrões de interação** amplamente viabilizados pelo ecossistema Rive:

### 1. Mascote Interativo com Rastreamento de Ponteiro (IK Tracking)
* **Comportamento Visual**: O personagem mantém um ciclo de respiração sutil (*Idle Breathing*). Quando o cursor do mouse se move pela janela, as pupilas dos olhos e a cabeça giram organicamente para acompanhar a coordenada do ponteiro, mantendo limites anatômicos reais via Inverse Kinematics (IK).
* **Entradas da State Machine**:
  - `mouseX` (Number: 0 a 100)
  - `mouseY` (Number: 0 a 100)
  - `isSurprised` (Trigger: disparado se o cursor se aproximar abruptamente)
* **Onde Usar**: Hero sections de produtos de design/educação, fluxos de onboarding, assistentes virtuais de IA.

### 2. O Switch Físico de Alta Fidelidade (Morphing Light/Dark Mode Toggle)
* **Comportamento Visual**: Um interruptor de tema que não apenas desliza de um lado para o outro: ao ser alternado, o botão esférico do sol estica ligeiramente sob inércia elástica, os raios solares se desprendem e colapsam para dentro formando crateras, enquanto uma lua crescente emerge com estrelas cintilantes ao redor.
* **Entradas da State Machine**:
  - `isDark` (Boolean: true/false)
* **Onde Usar**: Barras de navegação de SaaS modernos, painéis de controle e cabeçalhos de documentação.

### 3. Formulário Sensível a Contexto com Mascote Cego (Login Avatar "Peek & Hide")
* **Comportamento Visual**: Enquanto o usuário digita seu e-mail no formulário, a mascote acompanha a quantidade de caracteres olhando para o campo. Ao focar no campo de senha (onde o texto fica ofuscado com bolinhas), a mascote cobre os olhos com as mãos em um gesto divertido e seguro; ao clicar no botão "Mostrar Senha", a mascote abre uma fresta entre os dedos espiando timidamente.
* **Entradas da State Machine**:
  - `characterCount` (Number: 0 a 50)
  - `isCoveringEyes` (Boolean: true/false)
  - `isPeeking` (Boolean: true/false)
  - `onSuccess` (Trigger)
  - `onError` (Trigger)
* **Onde Usar**: Telas de login de aplicativos mobile e web focados em retenção emocional e redução de ansiedade em autenticação.

### 4. Barra de Progresso Circular Não-Linear com Árvore de Mistura (Radial Gauge)
* **Comportamento Visual**: Um medidor vetorial circular cuja cor, espessura e velocidade das partículas periféricas mudam de forma contínua conforme o percentual avança de 0 a 100. Em vez de saltar entre animações separadas, um *1D Blend Tree* interpola continuamente entre estados: azul calmo (0-40%), âmbar energético (41-79%) e violeta sobrecarregado (80-100%).
* **Entradas da State Machine**:
  - `progressPercent` (Number: 0 a 100)
* **Onde Usar**: Indicadores de armazenamento em nuvem, medidores de segurança de senhas, velocímetros e painéis de telemetria.

### 5. Botão de Ação Primária Reativo com Feedback de Estado Tríplice
* **Comportamento Visual**: Um botão que contém a label "Salvar Alterações". Ao ser clicado, a caixa exterior colapsa em uma pílula compacta de carregamento com uma órbita fluida; se a requisição de rede retornar com sucesso, a pílula explode suavemente em um ícone de marcação verde com ondas concêntricas; se falhar, o botão vibra lateralmente com física elástica em vermelho e reabre o texto com foco de edição.
* **Entradas da State Machine**:
  - `triggerSubmit` (Trigger)
  - `triggerSuccess` (Trigger)
  - `triggerError` (Trigger)
  - `triggerReset` (Trigger)
* **Onde Usar**: Checkouts de e-commerce, botões de pagamento e formulários de envio de arquivos pesados.

### 6. Card com Efeito Parallax Direcional (2D Blend Tree Surface)
* **Comportamento Visual**: Um cartão de apresentação de produto 3D estilizado em vetor. A malha vetorial interna de sombras e realces de reflexo responde à posição angular do cursor do mouse em coordenadas bidimensionais X e Y (`-1.0` a `+1.0`), simulando volume tridimensional através de deformação de vértices na GPU.
* **Entradas da State Machine**:
  - `tiltX` (Number: -100 a +100)
  - `tiltY` (Number: -100 a +100)
  - `isHovered` (Boolean: true/false)
* **Onde Usar**: Bento grids de landing pages, vitrines de itens NFT/colecionáveis digitais ou cartões bancários virtuais em fintechs.

### 7. Pull-to-Refresh Orgânico com Deformação de Malha Líquida
* **Comportamento Visual**: Durante o gesto de puxar a lista de dados para baixo em um dispositivo móvel, um filamento de gota vetorial estica-se gradualmente com tensão de viscosidade. Se o usuário soltar antes da linha de corte, a gota retrai com oscilação amortecida; se ultrapassar a linha, a gota rompe-se em um anel rotativo contínuo que alimenta o ciclo de recarregamento.
* **Entradas da State Machine**:
  - `pullDistance` (Number: 0 a 150)
  - `isRefreshing` (Boolean: true/false)
* **Onde Usar**: Feeds de notícias móveis, carteiras de criptoativos e caixas de entrada de e-mail.

### 8. Visualizador de Áudio e Ondas Frequenciais em Tempo Real
* **Comportamento Visual**: Varetas ou esferas vetoriais flutuantes com malha deformada que alteram sua escala, amplitude e cor de acordo com bandas de frequência de áudio (Bass, Mid, Treble) capturadas via Web Audio API. As transições internas do Rive suavizam os picos sonoros com interpolação contínua.
* **Entradas da State Machine**:
  - `bassIntensity` (Number: 0 a 100)
  - `midIntensity` (Number: 0 a 100)
  - `trebleIntensity` (Number: 0 a 100)
* **Onde Usar**: Mini-players em streaming de música, interfaces de comando de voz e podcasts.

### 9. Dynamic Badge de Notificação com View Model & Text Run
* **Comportamento Visual**: Um crachá flutuante de alertas. Quando o contador de mensagens não lidas sobe de 1 para 12, a badge executa uma mola elástica de pulso, o texto numérico é substituído dinamicamente via *Rive Dynamic Text Binding*, e a cor da borda transita suavemente para vermelho vivo.
* **Propriedades do View Model**:
  - `badgeCount` (String / Number: "12")
  - `urgencyLevel` (Number: 1 a 3)
* **Onde Usar**: Sino de notificações em plataformas de produtividade colaborativa, painéis de mensagens em tempo real e jogos.

---

## 5. Arquitetura Técnica, Física de Movimento & Receitas de Código

### A Comparação Técnica Definitiva: Rive vs Lottie

Para arquitetos de software e líderes de design, a escolha entre Rive e Lottie resume-se a parâmetros objetivos de engenharia:

| Critério Arquitetural | Rive (`.riv`) | Lottie (`.json` / dotLottie) |
| :--- | :--- | :--- |
| **Formato e Tamanho de Arquivo** | Binário ultracompacto (`.riv`), tipicamente **10KB a 80KB**. | JSON hierárquico verboso ou zip `.lottie`, tipicamente **100KB a 5MB**. |
| **Tempo de Parsing e Inicialização** | Zero deserialização no JS; leitura direta em memória linear WebAssembly em **< 2ms**. | Deserialização pesada de JSON na Main Thread do JS (**50ms a 300ms** em mobile fraco). |
| **Motor de Renderização** | **Rive Renderer dedicado em GPU** (Metal, Vulkan, WebGPU, WebGL2) desenhando caminhos e malhas via shaders. | Canvas 2D da CPU (com `clearRect` destrutivo contínuo) ou centenas de nós SVG no DOM do navegador. |
| **Arquitetura de Lógica / Interatividade** | **State Machine nativa embutida**: camadas, inputs de controle, blend trees e listeners vivem dentro do asset. | Nenhuma inteligência nativa; exige código JS externo complexo para tocar trechos de timeline discretos. |
| **Deformação de Malhas & Bones** | **Suporte completo a Rigging, Bones, Pesos e Cinemática Inversa (IK)** calculados na GPU. | Não suportado de forma procedural; cada vértice deformado precisa ter keyframes estáticos salvos no JSON. |
| **Interpolação entre Estados Concorrentes** | Transição fluida contínua sem quebras; interpola suavemente entre qualquer estado de repouso ou animação. | Corta abruptamente para o próximo quadro ou necessita de lógica matemática manual para transicionar. |
| **Data Binding & Texto Dinâmico** | Suporte nativo a **View Models** com tipagem reativa e alteração de texto em tempo de execução sem refazer layout. | Manipulação bruta e arriscada de nós internos no JSON da árvore da animação. |
| **Consumo de Bateria & CPU** | Muito baixo; ciclos de CPU próximos a 0%, processamento puramente vetorial na GPU. | Médio a Alto; constante uso de ciclos de CPU para calcular interpolações de pontos bezier frame a frame. |

---

### Curvas de Interpolação & Parâmetros Físicos no Rive

No Rive, as transições entre estados dentro da State Machine podem ser governadas tanto por curvas de Bézier cúbicas personalizadas quanto por parâmetros de mola (*Spring Physics*):

* **Transição Elástica Snappy (Micro-Interações e Switches)**:
  - Curva Bézier: `cubic-bezier(0.175, 0.885, 0.32, 1.275)` (comportamento de overshoot rápido de 6% e acomodação firme).
* **Transição Suave de Amortecimento (Blend States de Personagens e Olhar)**:
  - Curva Bézier: `cubic-bezier(0.16, 1, 0.3, 1)` (desaceleração exponencial limpa sem oscilações residuais).
* **Parâmetros de Mola (*Spring Transition*)**:
  - `Response` (Tempo até o pico): `0.35s`
  - `Damping` (Fator de amortecimento): `0.72` (evita oscilação infinita mantendo um ressalto tátil agradável).

---

### Receita de Código 1: Componente de Autenticação com Mascote Interativo

O exemplo a seguir implementa em **Next.js / React 19** com `@rive-app/react-canvas` uma tela de login onde um urso mascote reage à digitação do e-mail (seguindo o cursor pelo número de caracteres), cobre os olhos quando o campo de senha ganha foco, e dispara uma celebração ou tremor de erro com base no resultado da autenticação.

```tsx
"use client";

import React, { useState, useRef, useEffect } from "react";
import { useRive, useStateMachineInput, Layout, Fit, Alignment } from "@rive-app/react-canvas";
import { Eye, EyeOff, Lock, Mail, Loader2, CheckCircle2, AlertCircle } from "lucide-react";

interface LoginStatus {
  type: "idle" | "loading" | "success" | "error";
  message?: string;
}

export function InteractiveLoginHero() {
  const [email, setEmail] = useState("");
  const [password, setPassword] = useState("");
  const [showPassword, setShowPassword] = useState(false);
  const [status, setStatus] = useState<LoginStatus>({ type: "idle" });

  const STATE_MACHINE_NAME = "Login_State_Machine";

  // 1. Inicialização do runtime do Rive com layout configurado
  const { rive, RiveComponent } = useRive({
    src: "https://cdn.rive.app/animations/animated_login_character.riv",
    stateMachines: STATE_MACHINE_NAME,
    autoplay: true,
    layout: new Layout({
      fit: Fit.Contain,
      alignment: Alignment.Center,
    }),
  });

  // 2. Mapeamento das entradas da State Machine do Rive
  // O mascote possui: Look (Number), isChecking (Boolean), isHandsUp (Boolean), trigSuccess (Trigger), trigFail (Trigger)
  const lookInput = useStateMachineInput(rive, STATE_MACHINE_NAME, "Look");
  const isCheckingInput = useStateMachineInput(rive, STATE_MACHINE_NAME, "isChecking");
  const isHandsUpInput = useStateMachineInput(rive, STATE_MACHINE_NAME, "isHandsUp");
  const trigSuccessInput = useStateMachineInput(rive, STATE_MACHINE_NAME, "trigSuccess");
  const trigFailInput = useStateMachineInput(rive, STATE_MACHINE_NAME, "trigFail");

  // Atualiza a rotação dos olhos conforme a quantidade de caracteres no input de email
  const handleEmailChange = (e: React.ChangeEvent<HTMLInputElement>) => {
    const val = e.target.value;
    setEmail(val);
    if (lookInput && isCheckingInput) {
      isCheckingInput.value = true;
      // Normaliza o comprimento do texto (0 a 40 caracteres) para a escala 0..100 do Rive
      lookInput.value = Math.min(val.length * 2.5, 100);
    }
  };

  const handleEmailFocus = () => {
    if (isCheckingInput) isCheckingInput.value = true;
    if (isHandsUpInput) isHandsUpInput.value = false;
  };

  const handleEmailBlur = () => {
    if (isCheckingInput) isCheckingInput.value = false;
  };

  const handlePasswordFocus = () => {
    if (isCheckingInput) isCheckingInput.value = false;
    // Quando entra no campo de senha (e não está com showPassword ativo), o mascote tapa os olhos
    if (isHandsUpInput) isHandsUpInput.value = !showPassword;
  };

  const handlePasswordBlur = () => {
    if (isHandsUpInput) isHandsUpInput.value = false;
  };

  const togglePasswordVisibility = () => {
    const nextState = !showPassword;
    setShowPassword(nextState);
    if (isHandsUpInput) {
      isHandsUpInput.value = !nextState; // Se revelou a senha, o mascote abaixa as mãos
    }
  };

  const handleSubmit = async (e: React.FormEvent) => {
    e.preventDefault();
    if (isHandsUpInput) isHandsUpInput.value = false;
    if (isCheckingInput) isCheckingInput.value = false;

    setStatus({ type: "loading" });

    // Simulação de autenticação com a API
    setTimeout(() => {
      if (email === "admin@designsystem.io" && password === "secret123") {
        setStatus({ type: "success", message: "Autenticação bem-sucedida! Redirecionando..." });
        if (trigSuccessInput) trigSuccessInput.fire();
      } else {
        setStatus({ type: "error", message: "Credenciais inválidas. Tente novamente." });
        if (trigFailInput) trigFailInput.fire();
      }
    }, 1200);
  };

  return (
    <div className="w-full max-w-md mx-auto rounded-3xl bg-neutral-900 border border-neutral-800 shadow-2xl p-8 flex flex-col items-center">
      {/* Container do Canvas Rive: Dimensões explícitas são indispensáveis */}
      <div className="w-64 h-56 relative mb-4">
        <RiveComponent
          role="img"
          aria-label="Mascote interativo reagindo aos campos de formulário"
          className="w-full h-full"
        />
      </div>

      <div className="w-full text-center mb-6">
        <h2 className="text-xl font-semibold text-neutral-100 tracking-tight">Bem-vindo de volta</h2>
        <p className="text-xs text-neutral-400 mt-1">Insira suas credenciais corporativas seguras</p>
      </div>

      <form onSubmit={handleSubmit} className="w-full space-y-4">
        {/* Campo E-mail */}
        <div className="space-y-1.5">
          <label className="text-xs font-medium text-neutral-300 flex items-center gap-1.5">
            <Mail className="w-3.5 h-3.5 text-neutral-400" />
            E-mail
          </label>
          <input
            type="email"
            required
            value={email}
            onChange={handleEmailChange}
            onFocus={handleEmailFocus}
            onBlur={handleEmailBlur}
            placeholder="usuario@dominio.com"
            className="w-full px-3.5 py-2.5 rounded-xl bg-neutral-950 border border-neutral-800 text-sm text-neutral-100 placeholder:text-neutral-600 focus:outline-none focus:ring-2 focus:ring-violet-500/50 focus:border-violet-500 transition-all"
          />
        </div>

        {/* Campo Senha com Toggle de Visualização */}
        <div className="space-y-1.5">
          <label className="text-xs font-medium text-neutral-300 flex items-center gap-1.5">
            <Lock className="w-3.5 h-3.5 text-neutral-400" />
            Senha
          </label>
          <div className="relative">
            <input
              type={showPassword ? "text" : "password"}
              required
              value={password}
              onChange={(e) => setPassword(e.target.value)}
              onFocus={handlePasswordFocus}
              onBlur={handlePasswordBlur}
              placeholder="••••••••••••"
              className="w-full px-3.5 py-2.5 pr-10 rounded-xl bg-neutral-950 border border-neutral-800 text-sm text-neutral-100 placeholder:text-neutral-600 focus:outline-none focus:ring-2 focus:ring-violet-500/50 focus:border-violet-500 transition-all"
            />
            <button
              type="button"
              onClick={togglePasswordVisibility}
              tabIndex={-1}
              aria-label={showPassword ? "Ocultar senha" : "Exibir senha"}
              className="absolute right-3 top-1/2 -translate-y-1/2 text-neutral-400 hover:text-neutral-200 transition-colors"
            >
              {showPassword ? <EyeOff className="w-4 h-4" /> : <Eye className="w-4 h-4" />}
            </button>
          </div>
        </div>

        {/* Mensagens de Feedback */}
        {status.type === "error" && (
          <div className="flex items-center gap-2 p-3 rounded-lg bg-red-950/40 border border-red-800/60 text-xs text-red-300 animate-in fade-in slide-in-from-top-1">
            <AlertCircle className="w-4 h-4 shrink-0 text-red-400" />
            <span>{status.message}</span>
          </div>
        )}

        {status.type === "success" && (
          <div className="flex items-center gap-2 p-3 rounded-lg bg-emerald-950/40 border border-emerald-800/60 text-xs text-emerald-300 animate-in fade-in slide-in-from-top-1">
            <CheckCircle2 className="w-4 h-4 shrink-0 text-emerald-400" />
            <span>{status.message}</span>
          </div>
        )}

        {/* Botão de Envio */}
        <button
          type="submit"
          disabled={status.type === "loading"}
          className="w-full py-2.5 px-4 rounded-xl font-medium text-sm text-white bg-violet-600 hover:bg-violet-500 active:scale-[0.98] transition-all duration-150 disabled:opacity-50 disabled:cursor-not-allowed flex items-center justify-center gap-2 shadow-lg shadow-violet-600/20"
        >
          {status.type === "loading" ? (
            <>
              <Loader2 className="w-4 h-4 animate-spin" />
              <span>Verificando...</span>
            </>
          ) : (
            <span>Entrar na Plataforma</span>
          )}
        </button>
      </form>
    </div>
  );
}
```

---

### Receita de Código 2: Componente Reutilizável de Micro-Switch com Gestão de Visibilidade e Fallback

Este componente encapsula as melhores práticas de produção: lazy initialization com `IntersectionObserver`, respeito a `prefers-reduced-motion` e controle de limpeza do contexto WebGL.

```tsx
"use client";

import React, { useRef, useState, useEffect } from "react";
import { useRive, useStateMachineInput, Layout, Fit, Alignment } from "@rive-app/react-canvas";

interface RiveToggleProps {
  id?: string;
  checked: boolean;
  onChange: (nextState: boolean) => void;
  label: string;
  className?: string;
}

export function RiveThemeSwitch({ checked, onChange, label, className = "" }: RiveToggleProps) {
  const containerRef = useRef<HTMLDivElement>(null);
  const [isVisible, setIsVisible] = useState(false);

  // IntersectionObserver: Renderiza o canvas apenas quando visível na viewport
  useEffect(() => {
    const observer = new IntersectionObserver(
      ([entry]) => {
        setIsVisible(entry.isIntersecting);
      },
      { threshold: 0.1 }
    );

    if (containerRef.current) {
      observer.observe(containerRef.current);
    }

    return () => observer.disconnect();
  }, []);

  const STATE_MACHINE = "Switch_SM";

  const { rive, RiveComponent } = useRive({
    src: "https://cdn.rive.app/animations/switch_light_dark.riv",
    stateMachines: STATE_MACHINE,
    autoplay: isVisible,
    layout: new Layout({
      fit: Fit.Contain,
      alignment: Alignment.Center,
    }),
  });

  const toggleInput = useStateMachineInput(rive, STATE_MACHINE, "isDark");

  // Sincroniza a propriedade React com a entrada da State Machine
  useEffect(() => {
    if (toggleInput) {
      toggleInput.value = checked;
    }
  }, [checked, toggleInput]);

  const handleClick = () => {
    const next = !checked;
    onChange(next);
    if (toggleInput) {
      toggleInput.value = next;
    }
  };

  const handleKeyDown = (e: React.KeyboardEvent) => {
    if (e.key === " " || e.key === "Enter") {
      e.preventDefault();
      handleClick();
    }
  };

  return (
    <div
      ref={containerRef}
      role="switch"
      aria-checked={checked}
      aria-label={label}
      tabIndex={0}
      onClick={handleClick}
      onKeyDown={handleKeyDown}
      className={`inline-flex items-center cursor-pointer select-none focus:outline-none focus-visible:ring-2 focus-visible:ring-offset-2 focus-visible:ring-violet-500 rounded-full transition-transform active:scale-95 ${className}`}
    >
      <div className="w-14 h-8 relative">
        {isVisible ? (
          <RiveComponent className="w-full h-full pointer-events-none" />
        ) : (
          // Fallback visual leve enquanto o elemento está fora da tela
          <div
            className={`w-full h-full rounded-full transition-colors ${
              checked ? "bg-violet-600" : "bg-neutral-700"
            }`}
          />
        )}
      </div>
      <span className="sr-only">{label}</span>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir as especificações de design e arquitetura técnica no arquivo `DESIGN_BLUEPRINT.md` de uma nova aplicação, os engenheiros e designers devem formalizar o uso do Rive seguindo este padrão:

### 1. Nomenclatura Padronizada de Artefatos & State Machines
* **Caminho dos Assets**: Todos os arquivos binários devem residir em `/public/assets/rive/*.riv` com nomes semânticos em kebab-case (ex: `auth-mascot.riv`, `theme-switch.riv`, `telemetry-gauge.riv`).
* **Convenção de Artboards e State Machines**:
  - Toda State Machine principal deve se chamar obrigatoriamente `Main_SM` ou `<NomeDoComponente>_SM`.
  - Entradas booleanas devem iniciar com o prefixo `is` ou `has` (ex: `isHovered`, `isActive`, `hasError`).
  - Entradas numéricas devem expressar claramente a escala esperada (ex: `progress_0_100`, `cursorX_norm`, `volume_dB`).
  - Entradas de gatilho devem utilizar o prefixo `trig` (ex: `trigSubmit`, `trigBurst`, `trigReset`).

### 2. Guardrails de Performance no Blueprint
* **Controle de Instâncias WebGL**: O blueprint deve limitar o número de instâncias simultâneas ativas na mesma tela a no máximo **4 componentes Rive em desktop** e **2 componentes em mobile**. Listas infinitas e feeds devem utilizar imagens estáticas ou SVGs leves, hidratando instâncias Rive apenas no item selecionado/expandido.
* **Política de Pausa em Segundo Plano**: Exigir o desligamento do loop de renderização (`rive.pause()`) caso o componente saia da viewport ou caso o documento perca o foco (`document.visibilityState === 'hidden'`).
* **Fallback Acessível Obrigatório**: Todo elemento que utilizar Rive deve possuir descrição textual equivalente nos atributos `aria-label` e suporte total a navegação por teclado (`Tab`, `Space`, `Enter`).
