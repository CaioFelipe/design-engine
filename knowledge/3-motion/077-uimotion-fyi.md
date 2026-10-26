---
id: "uimotion-fyi"
name: "UI Motion (.fyi)"
url: "https://uimotion.fyi/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["Spatial Continuity", "Direct Manipulation & Real-Time Inertia", "Tactile Micro-Interactions", "Physical Spring Dynamics", "Contextual Shared Morphing", "High-End Product Decoding"]
densidade_informacao: "Alta"
impacto_visual: "Moderado a Cinematografico/Showstopper"
custo_computacional: "Baixo (CSS Transforms/Hardware Composing) a Medio (JS Springs/Pointer Tracking)"
stack_frameworks: ["CSS3 Moderno", "Framer Motion / Motion.dev", "React", "Vanilla JavaScript (WAAPI)", "Tailwind CSS"]
compatibilidade:
  combinacoes_recomendadas: ["Radix UI / Shadcn + Motion.dev", "Tailwind CSS + CSS Custom Properties Tracking", "Lenis Smooth Scroll + Layout Projection", "Lucide Icons + SVG Path Morphing"]
  conflitos_esteticos: ["Animações puramente lineares sem massa ou inércia", "Delays em cascata (>300ms) em ferramentas de produtividade intensa", "Distorções de layout forçando reflow em cascata via width/height", "Ignorar prefers-reduced-motion em usuários com sensibilidade vestibular"]
---

# UI Motion (.fyi) — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)

O **UI Motion** (`https://uimotion.fyi/`, criado e curado pelo designer e engenheiro de produto **Nikhil Dussa**) consolidou-se como o arquivo vivo definitivo de desconstrução e engenharia reversa das microinterações, transições de estado e coreografias físicas que definem os produtos digitais mais prestigiados do mundo (Linear, Stripe, Apple iOS/macOS, Raycast, Slack, Notion, Framer, Vercel e Perplexity).

Diferente de catálogos superficiais de "inspiração visual" baseados em GIFs ou vídeos estáticos do Dribbble, o UI Motion aborda o design de movimento a partir de um prisma estritamente operacional e biomecânico: **a interface digital como uma extensão espacial do mundo físico**. Cada elemento visual na tela deve comportar-se como um objeto tangível dotado de massa, atrito, momento angular e continuidade cartesiana.

### A Trindade Analítica do UI Motion: Feeling, Why & Values

O arcabouço conceitual do UI Motion analisa cada padrão sob três dimensões inseparáveis:

1. **The Feeling (A Percepção Sensorial)**:
   A sensação cinestésica transmitida ao cérebro do usuário. Em vez de uma transição mecânica fria, o movimento comunica estabilidade, velocidade, leveza ou solidez tátil. O modal do Raycast "parece uma carta de baralho cortando o ar e pousando pesada sobre uma mesa de feltro"; o botão magnético do Framer "inicia uma conversa silenciosa ao se inclinar em direção ao ponteiro antes mesmo do clique".

2. **The Why (A Justificativa Cognitiva e Biomecânica)**:
   A razão pela qual a animação existe no fluxo. O movimento nunca é decorativo; ele serve para:
   - **Preservar a Continuidade Espacial (Spatial Continuity)**: evitar quebras abruptas de contexto quando o usuário navega entre visualizações ou estados.
   - **Confirmar Intenção (Tactile Confirmation)**: dar feedback instantâneo sobre a aceitação de um comando antes mesmo da resposta assíncrona do servidor.
   - **Guiar a Fóvea Visual (Visual Anchoring)**: conduzir o olho humano para o próximo ponto de decisão sem sobrecarregar a atenção periférica.

3. **The Values (A Cinética Paramétrica Real)**:
   A tradução matemática exata das propriedades físicas: curvas de Bézier cúbicas personalizadas (`cubic-bezier(x1, y1, x2, y2)`), coeficientes de mola (`stiffness`, `damping`, `mass`), offsets vetoriais em coordenadas de tela e durações calibradas ao milissegundo.

### Física de Molas vs. Curvas Cúbicas no UI Motion

O ecossistema decodificado no UI Motion divide o universo cinético da interface em duas filosofias complementares:

- **Sistemas Baseados em Molas (Spring Physics - Lei de Hooke com Amortecimento)**:
  Utilizados em gestos táteis diretos e microinterações táteis (Bottom Sheets, Pull-to-Refresh, Magnetic Buttons, Toasts). Em vez de uma duração temporal engessada (ex: `300ms`), a duração é consequência direta da massa do elemento, da tensão da mola (`stiffness`) e da resistência viscosa (`damping`). Se o usuário arremessa uma gaveta modal rapidamente, a velocidade do arremesso é injetada na equação, permitindo interrupção fluida sem engasgos de interpolação.
  
- **Curvas Snappy Asimétricas (Fast-Attack Ease-Outs)**:
  Utilizadas em ferramentas de alta densidade e produtividade (Command Palettes, Tooltips, Menus de Contexto, Toggles de Preço). Caracterizam-se por aceleração quase instantânea nos primeiros 15% da trajetória seguida por uma cauda longa de desaceleração suave (exemplo canônico: `cubic-bezier(0.16, 1, 0.3, 1)` da Linear e Raycast), conferindo uma sensação de "velocidade com elegância" sem o salto seco e artificial de uma curva linear.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto e Superfícies Críticas

1. **SaaS B2B, DevTools e Workspaces de Produtividade (Padrão Raycast / Linear / Notion)**:
   - *Command Palettes*: Abertura e fechamento em 220ms com escala sutil de 0.98 para 1.0 e curva `cubic-bezier(0.16, 1, 0.3, 1)`.
   - *Abas Deslizantes (Sliding Underlines)*: Indicadores ativos magnéticos que se deslocam sem reconstruir o elemento no DOM (`layoutId`), mantendo a âncora espacial.
   - *Tooltips de Baixa Latência*: Aparição suave com 180ms de fade + transladação ascendente de 4px, sem tremulação.

2. **Fintech, Gateways de Pagamento e Dashboards Críticos (Padrão Stripe)**:
   - *Number Counters (Odômetros)*: Animação de rolagem vertical de dígitos em métricas de faturamento e taxas de conversão (`cubic-bezier(0.16, 1, 0.3, 1)`), transformando dados estáticos em marcos comemorativos vivos.
   - *Cartões com Borda Lanterna (Flashlight Glow Border)*: Realce dinâmico por gradiente radial ancorado no ponteiro do mouse sem re-renders de JavaScript.
   - *Toggles de Faturamento Mensal/Anual*: Deslizamento mecânico sincronizado com a rolagem vertical de preços de assinatura.

3. **Aplicações Mobile & Web Apps Responsivos (Padrão Apple iOS / macOS)**:
   - *Bottom Sheets com Física de Arremesso*: Folhas contextuais que acompanham a ponta do dedo em tempo real (0ms de latência) e se encaixam no ponto de ancoragem (*snap point*) via molas amortecidas.
   - *Wiggle Error Feedback*: Recuo elástico horizontal em campos de formulário inválidos, comunicando erro através de linguagem corporal biofísica sem a necessidade de textos de aviso invasivos imediatos.
   - *Backdrop Blurs com Profundidade*: Desfoques progressivos que isolam a hierarquia modal mantendo o plano de fundo discernível.

4. **Experiências com Inteligência Artificial Generativa (Padrão Perplexity / Gemini)**:
   - *Answer Streaming com Chips Flutuantes*: Revelação tipográfica contínua combinada com aparição suave de chips de fontes citadas.
   - *Botões de Assistente com Aura Mutável*: Gradientes cônicos e radiais de baixa frequência que respiram sob repouso e ganham pulsação elástica no hover.

### O Papel do Catálogo na Regra 60-30-10

- **60% — Fundação Estática & Silêncio Cinético (Repouso Estrutural)**:
  A maioria dos blocos de uma aplicação séria (layouts de leitura, tipografia de parágrafos, grids estruturais, tabelas densas em repouso) não deve conter movimentos autônomos contínuos. A estabilidade visual é o alicerce indispensável para a usabilidade e a prevenção de sobrecarga cognitiva.

- **30% — Fluidez Invisível & Conectividade Espacial (O "Feel" Subconsciente)**:
  A camada intermediária onde os padrões de UI Motion operam com máxima maestria:
  - Micro-amortecimento ao clicar em botões (`scale: 0.98` com spring ágil).
  - Deslizamento orgânico da pílula indicadora entre abas.
  - Abertura de gavetas e popovers com aceleração rápida e desaceleração elástica.
  - O usuário não repara explicitamente na animação; ele apenas percebe que o sistema responde de modo "instantâneo, refinado e sólido".

- **10% — Momentos Culminantes & "Delight" Emocional (Showstoppers)**:
  Reservado para gatilhos de alto valor de negócio e marcos psicológicos:
  - *Confetti Burst* ao concluir um ciclo árduo de tarefas (Duolingo / Linear).
  - *Payment Success Checkmark* desenhando vetores elásticos após um checkout bem-sucedido (Stripe).
  - *Flashlight Glow Border* exploratório no grid de planos de preços em landing pages institucionais.
  - *Radial FAB Fan-Out* explodindo opções criativas com efeito cascata milimetricamente sincronizado (Notion).

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Armadilhas Comuns Decodificadas pelo UI Motion (Common Mistakes)

1. **Atrasos Cumulativos Excessivos em Cascatas (Stagger Overdose)**:
   Em listas ou tabelas com mais de 10 itens, programar intervalos de cascata de `100ms` por item faz o último elemento surgir 1 segundo após o primeiro. Em interfaces de trabalho, isso transmite lentidão extrema. A regra de ouro do UI Motion é: cascata máxima de 30ms a 50ms por item, limitada a um teto cumulativo absoluto de 250ms.

2. **Molas com Oscilação Excessiva (Underdamped Springs / "Jelly UI")**:
   Configurar molas com amortecimento insuficiente (`damping: 5` ou `bounciness: 0.8`) faz elementos utilitários vibrarem repetidamente após atingir a posição final. Em interfaces corporativas ou financeiras, isso quebra a sensação de precisão e gera a impressão de uma interface de brinquedo. Use amortecimento crítico ou quase crítico (`damping: 15-25`).

3. **Animações Bloqueantes de Interação (Interaction Lock)**:
   Nunca impeça o clique ou a rolagem enquanto uma transição decorativa está em execução. O usuário deve ser capaz de clicar no botão de confirmação ou fechar o popover no meio do caminho, aproveitando a natureza interruptível do motor.

4. **Reflows Forçados no Thread Principal (Layout Thrashing)**:
   Jamais anime propriedades como `width`, `height`, `top`, `left` ou `margin` em cascata. O UI Motion prega o uso estrito de aceleração de hardware: `transform (translate3d, scale3d, rotate3d)` e `opacity`. Quando a mutação de layout for indispensável, use a técnica FLIP (*First, Last, Invert, Play*) ou projeção de layout acelerada por GPU.

### ⚠️ Regras de Acessibilidade & Higiene de Hardware

1. **Respeito Absoluto a `prefers-reduced-motion`**:
   Usuários com distúrbios vestibulares podem sofrer náuseas e desorientação com zooms rápidos, movimentos de paralaxe e translações amplas. Toda diretriz de UI Motion exige fallback imediato para transições sutis de opacidade ou desativação completa do movimento:
   ```css
   @media (prefers-reduced-motion: reduce) {
     *, *::before, *::after {
       animation-duration: 0.01ms !important;
       animation-iteration-count: 1 !important;
       transition-duration: 0.01ms !important;
       scroll-behavior: auto !important;
     }
   }
   ```

2. **Isolamento de Camadas de GPU sem Estouro de VRAM**:
   O uso indiscriminado de `will-change: transform` em dezenas de cartões simultâneos força o navegador a alocar texturas dedicadas na placa de vídeo, consumindo centenas de megabytes de VRAM em celulares. Aplique `will-change` apenas durante o estado ativo de interação (`:hover`, `:focus-within` ou gestos ativos) e remova-o quando o elemento estiver em repouso.

---

## 4. Catálogo de Efeitos, Primitivas e Padrões de Animação

Abaixo estão decodificados **10 padrões emblemáticos** presentes e sistematizados no acervo do UI Motion:

### 1. Command Palette Snappy Entry (Referência: Raycast)
- **Anatomia & Comportamento**: O modal emerge do centro superior da tela com deslocamento vertical rápido de 12px para cima e escala partindo de 0.98 para 1.0, acompanhado por um salto de opacidade de 0 a 1.
- **Cinética & Duração**: 220ms com `cubic-bezier(0.16, 1, 0.3, 1)`. Desaceleração ultrarrápida que ancora o modal com firmeza instantânea.
- **Gatilho**: Tecla de atalho global (`Cmd+K` / `Ctrl+K`) ou clique no gatilho de busca.
- **Onde Aplicar**: Paletas de comando, modais rápidos de busca, atalhos de navegação profunda.

### 2. Tactile Magnetic Button (Referência: Framer)
- **Anatomia & Comportamento**: O botão retangular arredondado percebe a proximidade do cursor em um raio de até 40px e inclina/translada seu centro em direção ao vetor do ponteiro (deslocamento proporcional atenuado a 20-30%). Ao sair, o botão retorna à posição original com um leve rebote elástico.
- **Cinética & Duração**: Física de mola real com `stiffness: 150`, `damping: 15` e massa reduzida.
- **Gatilho**: Evento `pointermove` com cálculo vetorial cartesiano local.
- **Onde Aplicar**: CTAs primários de Landing Pages, botões de checkout, seletores de modo hero.

### 3. Flashlight Glow Border Card (Referência: Stripe)
- **Anatomia & Comportamento**: O card possui uma borda sutilmente escura em repouso. Conforme o cursor percorre a superfície do grid, um gradiente radial colorido segue exatamente o ponto de contato, iluminando a borda periférica como um feixe de lanterna direcionado no escuro.
- **Cinética & Duração**: 0ms no rastreamento de posição (acompanhamento direto via variáveis CSS customizadas `--mouse-x`, `--mouse-y`) e fade de 200ms `ease-out` na entrada e saída.
- **Gatilho**: `mousemove` na div circundante com atualização via CSS variables.
- **Onde Aplicar**: Cards de precificação, vitrines de recursos tecnológicos, módulos de dashboards analíticos.

### 4. Sliding Pill Tab Underline / Spatial Continuity (Referência: Twitter / X & Arc)
- **Anatomia & Comportamento**: Em uma barra de navegação por abas, a linha ou pílula de seleção não desaparece para reaparecer em outro lugar. Ela desliza horizontalmente de forma contínua, esticando levemente sua largura durante o trânsito e encolhendo ao ancorar na nova aba ativa.
- **Cinética & Duração**: 240ms com `cubic-bezier(0.34, 1.56, 0.64, 1)` ou spring equivalente `stiffness: 400`, `damping: 30`.
- **Gatilho**: Clique em nova aba ou gesto de swipe horizontal no viewport de conteúdo.
- **Onde Aplicar**: Navegações por abas primárias e secundárias, filtros de tabelas, seletores de segmentação.

### 5. Spring Drag Bottom Sheet (Referência: Apple iOS)
- **Anatomia & Comportamento**: Folha modal acoplada à base da tela. Ao ser arrastada para baixo, acompanha o dedo com proporção 1:1. Se solta além do limiar de 40% da altura ou com velocidade descendente alta (*flick*), fecha completamente; caso contrário, é ejetada de volta ao topo com mola elástica.
- **Cinética & Duração**: 340ms, motor de molas calibrado em `spring(mass: 1, stiffness: 80, damping: 20)`.
- **Gatilho**: Gesto de arrastar vertical (`pan`/`drag`) ou botão de abertura/fechamento.
- **Onde Aplicar**: Menus móveis de ações, seletores de opções, visualizações detalhadas em telas compactas.

### 6. Wiggle Error Rebound (Referência: iOS Keychain / macOS)
- **Anatomia & Comportamento**: Quando um valor inválido (como senha incorreta ou código 2FA com erro) é submetido, o contêiner do input oscila horizontalmente em uma sequência amortecida de 4 a 5 ciclos: `0 -> -8px -> +8px -> -5px -> +5px -> 0`.
- **Cinética & Duração**: 400ms com curva balanceada `ease-in-out` ou oscilação rápida senoidal amortecida.
- **Gatilho**: Rejeição de formulário na validação síncrona ou assíncrona.
- **Onde Aplicar**: Telas de login, campos de PIN/OTP, cupons de desconto inválidos.

### 7. Odometer Rolling Number Counter (Referência: Stripe Dashboard & Pricing)
- **Anatomia & Comportamento**: Cada algarismo do número é envolvido em uma coluna vertical de dígitos (0 a 9). Ao mudar o valor (ex: de $49/mês para $39/mês ou contador de receita aumentando), as colunas rolam verticalmente com velocidades ligeiramente defasadas até acomodar o novo dígito.
- **Cinética & Duração**: 400ms a 1200ms com `cubic-bezier(0.16, 1, 0.3, 1)`.
- **Gatilho**: Mudança de estado em switches de faturamento, montagem de dashboards com carregamento de métricas.
- **Onde Aplicar**: Painéis de faturamento em tempo real, calculadoras de ROI, alternadores de ciclo de pagamento.

### 8. Skeleton-to-Content Shimmer Reveal (Referência: YouTube & Linear)
- **Anatomia & Comportamento**: Antes do carregamento dos dados, blocos neutros recebem uma onda de gradiente translúcido em ângulo de 90° que se desloca da esquerda para a direita em loop contínuo de 1200ms. Na chegada dos dados, a estrutura esqueletal transita por cross-fade atômico (180ms) diretamente para os nós reais sem nenhum salto de layout.
- **Cinética & Duração**: Loop do shimmer a 1.2s linear contínuo; reveal de conteúdo em 180ms `ease-out`.
- **Gatilho**: Ciclo de vida da requisição assíncrona (Promise pendente -> resolvida).
- **Onde Aplicar**: Feeds de conteúdo, cards de produtos, tabelas com paginação assíncrona.

### 9. Radial FAB Fan-Out (Referência: Notion)
- **Anatomia & Comportamento**: Um botão de ação flutuante (FAB) rotaciona 45° seu ícone central (de cruz para "X") enquanto 3 a 5 botões satélites são ejetados radialmente em arco parabólico com rotação e escala elástica progressiva.
- **Cinética & Duração**: 380ms de expansão total com defasagem (*stagger*) de 50ms entre cada chip filho; curva `cubic-bezier(0.34, 1.2, 0.64, 1)`.
- **Gatilho**: Clique ou toque no botão central flutuante.
- **Onde Aplicar**: Criação de novos documentos, menus de atalho rápido em interfaces móveis, inserção de blocos ricos.

### 10. AI Aura Glow & Responsive Shimmer (Referência: Google Gmail Gemini / Perplexity)
- **Anatomia & Comportamento**: O gatilho de inteligência artificial permanece discreto em repouso (ícone monocromático com brilho estático de 10%). Ao passar o cursor ou ao receber o foco, um anel gradiente multicromático (lilás, azul cobalto e âmbar) acorda em rotação fluida enquanto o ícone sofre uma ligeira distorção elástica de escala e desfoque luminoso periférico.
- **Cinética & Duração**: Transição de hover em 1s `ease-out`, ciclo do gradiente em rotação contínua de 3.5s a 5s `linear`.
- **Gatilho**: Hover do cursor, foco de teclado ou estado de raciocínio de IA ativo.
- **Onde Aplicar**: Botões de "Pergunte à IA", geradores de resumo, barras de prompt generativo.

---

## 5. Matemática do Movimento & Receitas de Código

### Parâmetros Físicos e Curvas Exatas Homologadas

```
+----------------------------------------------------------------------------------------------------+
| IDENTIFICADOR DA CURVA       | FÓRMULA / BÉZIER / PARÂMETROS           | USO RECOMENDADO           |
+----------------------------------------------------------------------------------------------------+
| Fast-Attack Linear/Raycast   | cubic-bezier(0.16, 1, 0.3, 1)           | Modais, Paletas, Menus    |
| Overshoot Bouncy Elastic     | cubic-bezier(0.34, 1.56, 0.64, 1)       | Toggles, Badges, Toasts   |
| Apple Fluid Sheet Ease       | cubic-bezier(0.32, 0.72, 0, 1)          | Bottom Sheets, Painéis    |
| Soft Radial Fan Out          | cubic-bezier(0.34, 1.2, 0.64, 1)        | Radial FAB, Menus Fan     |
| Spring: Tactile Responsive   | { stiffness: 400, damping: 28, mass: 1} | Tabs, Underlines, Toggles |
| Spring: Floating Magnetic    | { stiffness: 150, damping: 15, mass: 1} | Magnetic Buttons, Cards   |
| Spring: Heavy Bottom Sheet   | { stiffness: 80,  damping: 20, mass: 1} | Drag Sheets, Drawers      |
+----------------------------------------------------------------------------------------------------+
```

---

### Receita 1: Botão Magnético Tátil em React & Framer Motion (Padrão Framer / UI Motion)

Esta receita calcula a posição relativa do cursor em relação ao centro da caixa delimitadora do botão e aplica uma força de atração suave com retorno elástico inercial desacoplado:

```tsx
import React, { useRef } from "react";
import { motion, useMotionValue, useSpring, useTransform } from "framer-motion";

interface MagneticButtonProps {
  children: React.ReactNode;
  className?: string;
  onClick?: () => void;
  magneticPull?: number; // Fator de atração (ex: 0.35)
}

export const MagneticButton: React.FC<MagneticButtonProps> = ({
  children,
  className = "",
  onClick,
  magneticPull = 0.35,
}) => {
  const ref = useRef<HTMLButtonElement>(null);

  // Valores brutos do deslocamento relativo
  const mouseX = useMotionValue(0);
  const mouseY = useMotionValue(0);

  // Calibração física de mola idêntica ao acervo UI Motion
  const springConfig = { stiffness: 150, damping: 15, mass: 0.8 };
  const smoothX = useSpring(mouseX, springConfig);
  const smoothY = useSpring(mouseY, springConfig);

  // Leve rotação 3D complementar proporcional à distância
  const rotateX = useTransform(smoothY, [-30, 30], [8, -8]);
  const rotateY = useTransform(smoothX, [-30, 30], [-8, 8]);

  const handleMouseMove = (e: React.MouseEvent<HTMLButtonElement>) => {
    if (!ref.current) return;
    const rect = ref.current.getBoundingClientRect();
    const centerX = rect.left + rect.width / 2;
    const centerY = rect.top + rect.height / 2;

    const distanceX = (e.clientX - centerX) * magneticPull;
    const distanceY = (e.clientY - centerY) * magneticPull;

    mouseX.set(distanceX);
    mouseY.set(distanceY);
  };

  const handleMouseLeave = () => {
    // Retorno automático à posição de repouso
    mouseX.set(0);
    mouseY.set(0);
  };

  return (
    <motion.button
      ref={ref}
      onClick={onClick}
      onMouseMove={handleMouseMove}
      onMouseLeave={handleMouseLeave}
      style={{
        x: smoothX,
        y: smoothY,
        rotateX,
        rotateY,
        transformStyle: "preserve-3d",
      }}
      whileTap={{ scale: 0.96 }}
      className={`relative inline-flex items-center justify-center px-6 py-3.5 rounded-full font-medium text-sm text-neutral-100 bg-neutral-900 border border-neutral-800 shadow-xl transition-colors duration-200 hover:border-neutral-700 hover:bg-neutral-850 cursor-pointer select-none ${className}`}
    >
      <span className="relative z-10 pointer-events-none">{children}</span>
      {/* Efeito de brilho de fundo reativo */}
      <motion.div
        className="absolute inset-0 rounded-full opacity-0 hover:opacity-100 transition-opacity duration-300 pointer-events-none bg-[radial-gradient(circle_at_center,rgba(255,255,255,0.08)_0%,transparent_70%)]"
      />
    </motion.button>
  );
};
```

---

### Receita 2: Flashlight Glow Border Card sem Re-renders em React + CSS Custom Properties (Padrão Stripe)

O padrão mais eficiente da web para cartões com iluminação direcional: a posição do mouse é propagada unicamente via variáveis CSS customizadas no contêiner pai, eliminando re-renderizações no ciclo do React:

```tsx
import React, { useRef } from "react";

interface FlashlightCardProps {
  title: string;
  description: string;
  badge?: string;
}

export const FlashlightCard: React.FC<FlashlightCardProps> = ({
  title,
  description,
  badge = "Feature",
}) => {
  const cardRef = useRef<HTMLDivElement>(null);

  const handleMouseMove = (e: React.MouseEvent<HTMLDivElement>) => {
    if (!cardRef.current) return;
    const rect = cardRef.current.getBoundingClientRect();
    const x = e.clientX - rect.left;
    const y = e.clientY - rect.top;

    // Atualização atômica em nível de CSS
    cardRef.current.style.setProperty("--mouse-x", `${x}px`);
    cardRef.current.style.setProperty("--mouse-y", `${y}px`);
  };

  return (
    <div
      ref={cardRef}
      onMouseMove={handleMouseMove}
      className="group relative rounded-2xl p-[1px] bg-neutral-800/60 overflow-hidden transition-all duration-300 hover:shadow-2xl"
      style={
        {
          "--mouse-x": "0px",
          "--mouse-y": "0px",
        } as React.CSSProperties
      }
    >
      {/* Camada do Feixe de Luz da Borda (Flashlight Beam) */}
      <div
        className="pointer-events-none absolute -inset-px rounded-2xl opacity-0 transition-opacity duration-300 group-hover:opacity-100"
        style={{
          background: `radial-gradient(400px circle at var(--mouse-x) var(--mouse-y), rgba(99, 102, 241, 0.4), rgba(168, 85, 247, 0.2), transparent 70%)`,
        }}
      />

      {/* Conteúdo Interno com Máscara Sólida */}
      <div className="relative h-full w-full rounded-[15px] bg-neutral-950/90 backdrop-blur-xl p-7 flex flex-col justify-between">
        {/* Glow de Superfície Suave */}
        <div
          className="pointer-events-none absolute inset-0 rounded-[15px] opacity-0 transition-opacity duration-300 group-hover:opacity-100"
          style={{
            background: `radial-gradient(600px circle at var(--mouse-x) var(--mouse-y), rgba(255, 255, 255, 0.03), transparent 60%)`,
          }}
        />

        <div className="relative z-10">
          <span className="inline-block px-3 py-1 rounded-full text-xs font-semibold tracking-wider uppercase text-indigo-400 bg-indigo-500/10 border border-indigo-500/20 mb-4">
            {badge}
          </span>
          <h3 className="text-xl font-medium tracking-tight text-neutral-100 mb-2">
            {title}
          </h3>
          <p className="text-sm leading-relaxed text-neutral-400">
            {description}
          </p>
        </div>

        <div className="relative z-10 mt-6 pt-4 border-t border-neutral-900 flex items-center justify-between text-xs text-neutral-500">
          <span>Interação 0ms Latência</span>
          <span className="text-indigo-400 font-medium group-hover:translate-x-1 transition-transform duration-200">
            Explorar &rarr;
          </span>
        </div>
      </div>
    </div>
  );
};
```

---

### Receita 3: Command Palette Snappy Modal com Acessibilidade e Radix/Framer Motion (Padrão Raycast)

```tsx
import React, { useEffect } from "react";
import { motion, AnimatePresence } from "framer-motion";

interface CommandPaletteProps {
  isOpen: boolean;
  onClose: () => void;
  items: Array<{ id: string; label: string; icon?: string }>;
}

export const CommandPalette: React.FC<CommandPaletteProps> = ({
  isOpen,
  onClose,
  items,
}) => {
  useEffect(() => {
    const handleKeyDown = (e: KeyboardEvent) => {
      if (e.key === "Escape" && isOpen) onClose();
      if ((e.metaKey || e.ctrlKey) && e.key === "k") {
        e.preventDefault();
        isOpen ? onClose() : null;
      }
    };
    window.addEventListener("keydown", handleKeyDown);
    return () => window.removeEventListener("keydown", handleKeyDown);
  }, [isOpen, onClose]);

  return (
    <AnimatePresence>
      {isOpen && (
        <div className="fixed inset-0 z-50 flex items-start justify-center pt-[15vh] px-4">
          {/* Backdrop com Blur Suave */}
          <motion.div
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            exit={{ opacity: 0 }}
            transition={{ duration: 0.2, ease: "easeOut" }}
            onClick={onClose}
            className="fixed inset-0 bg-neutral-950/70 backdrop-blur-md"
          />

          {/* Janela Principal: Curva Snappy Raycast 220ms */}
          <motion.div
            initial={{ opacity: 0, scale: 0.97, y: -10 }}
            animate={{ opacity: 1, scale: 1, y: 0 }}
            exit={{ opacity: 0, scale: 0.98, y: -6 }}
            transition={{
              duration: 0.22,
              ease: [0.16, 1, 0.3, 1], // Assinatura Raycast / Linear
            }}
            className="relative w-full max-w-xl bg-neutral-900 border border-neutral-800 rounded-xl shadow-2xl overflow-hidden flex flex-col"
          >
            {/* Input de Busca */}
            <div className="flex items-center px-4 py-3.5 border-b border-neutral-800">
              <svg
                className="w-4 h-4 text-neutral-500 mr-3"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  strokeLinecap="round"
                  strokeLinejoin="round"
                  strokeWidth={2}
                  d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
                />
              </svg>
              <input
                autoFocus
                placeholder="Digite um comando ou busque uma ação..."
                className="w-full bg-transparent text-sm text-neutral-100 placeholder-neutral-500 focus:outline-none"
              />
              <kbd className="px-2 py-0.5 text-[10px] font-mono bg-neutral-800 text-neutral-400 rounded border border-neutral-700">
                ESC
              </kbd>
            </div>

            {/* Lista de Ações com Stagger Mínimo */}
            <div className="p-2 max-h-72 overflow-y-auto space-y-1">
              {items.map((item, idx) => (
                <motion.div
                  key={item.id}
                  initial={{ opacity: 0, x: -4 }}
                  animate={{ opacity: 1, x: 0 }}
                  transition={{
                    duration: 0.15,
                    delay: Math.min(idx * 0.02, 0.15), // Limite rígido anti-lag
                    ease: "easeOut",
                  }}
                  className="flex items-center justify-between px-3 py-2.5 rounded-lg text-sm text-neutral-300 hover:bg-neutral-800 hover:text-white cursor-pointer transition-colors"
                >
                  <span>{item.label}</span>
                  <span className="text-xs text-neutral-600 font-mono">Executar &crarr;</span>
                </motion.div>
              ))}
            </div>
          </motion.div>
        </div>
      )}
    </AnimatePresence>
  );
};
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma interface que utilize os padrões decodificados no UI Motion, a IA deve registrar formalmente as seguintes especificações no plano técnico antes de iniciar a codificação:

1. **Tabela de Tokens de Movimento & Física do Projeto**:
   - Defina os tokens padrão de aceleração nos estilos globais ou Tailwind config:
     ```css
     :root {
       --ease-snappy: cubic-bezier(0.16, 1, 0.3, 1);
       --ease-bounce: cubic-bezier(0.34, 1.56, 0.64, 1);
       --ease-sheet:  cubic-bezier(0.32, 0.72, 0, 1);
       --spring-tactile-stiffness: 400;
       --spring-tactile-damping: 28;
       --spring-floating-stiffness: 150;
       --spring-floating-damping: 15;
     }
     ```

2. **Orçamento Temporal Rígido (Latency Budget)**:
   - Toda microinteração com finalidade produtiva (fechar modal, alternar aba, acionar comando) deve ter duração total entre **180ms e 240ms**.
   - Animações comemorativas (*Confetti*, celebrações de pagamento) possuem teto de **600ms**.
   - O intervalo cumulativo de animações em cascata (*stagger*) nunca pode ultrapassar **250ms**.

3. **Checklist de Conformidade de Performance & GPU**:
   - [ ] As animações utilizam exclusivamente `transform` e `opacity`?
   - [ ] Em cartões interativos (Flashlight Borders, Parallax), as coordenadas são atualizadas via CSS Custom Properties sem disparar re-render no React?
   - [ ] Todos os componentes animados incluem suporte explícito à media query `prefers-reduced-motion` com atenuação instantânea?
   - [ ] As propriedades `will-change` são aplicadas estritamente durante estados ativos de hover/focus e liberadas em repouso para evitar estouro de memória de textura na GPU?
