---
id: "jitter-video"
name: "Jitter (Jitter.video — Motion Design Engine & UI Animation Platform)"
url: "https://jitter.video/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["Bento Grid Product Demos", "Snappy Overshoot & Impulse Curves", "Morphing UI Cards", "Kinetic Typography Waves", "Vector Lottie & Transparent WebM Alpha", "Choreographed Micro-Interactions"]
densidade_informacao: "Media a Alta"
impacto_visual: "Moderado a Cinematografico/Showstopper"
custo_computacional: "Baixo (Lottie/CSS/WebM) a Medio (Framer Motion Timeline & Canvas Loops)"
stack_frameworks: ["React 19 / 18", "Framer Motion (Motion.dev)", "DotLottie / Lottie Web", "Tailwind CSS v3 / v4", "HTML5 Transparent WebM (VP9 Alpha) / MP4", "TypeScript"]
compatibilidade:
  combinacoes_recomendadas: ["Shadcn UI", "Tailwind CSS v4", "Lenis Smooth Scroll", "Next.js App Router", "Lucide React", "DotLottie React"]
  conflitos_esteticos: ["Aplicações corporativas ultra-sóbrias sem suporte a elementos dinâmicos", "Interfaces com sobrecarga de animações concorrentes sem hierarquia temporal", "Layouts onde loops infinitos de alta frequência causem fadiga atencional ou concorrência com leitura de dados críticos"]
---

# Jitter — Dossiê de Física de Movimento, Transições & UI Motion Design

## 1. Filosofia de Movimento & Sensação Física (Feel)

O **Jitter** (`https://jitter.video/`), fundado em 2020 por **Sébastien Robaszkiewicz** e **Etienne Albert** (acelerado pelo Y Combinator na turma W21), estabeleceu-se no ecossistema global de design de produto como o "Figma para Motion Design". A plataforma resolveu um gargalo histórico que separava a concepção vetorial de interfaces da sua execução fluida na web moderna.

### A Metáfora do "Figma para Motion": Quebrando a Barreira do After Effects

Historicamente, motion design de interfaces digitais oscilava entre dois extremos problemáticos:
1. **O Monólito do Adobe After Effects**: Uma ferramenta projetada para pós-produção audiovisual e cinema linear, com curvas de aprendizado íngremes, arquivos pesados e um pipeline de exportação tortuoso e propenso a desvios no renderizador web.
2. **O Smart Animate Estático das Ferramentas de Design**: Recursos nativos de prototipagem em pranchetas estáticas que apenas interpolam estados entre quadros discretos (`Screen A` para `Screen B`), sem controle fino de linhas do tempo escalonadas (*stagger*), desacelerações assimétricas ou micro-interações internas em sub-camadas.

O Jitter redefiniu esse fluxo ao construir uma ferramenta **100% web-native, colaborativa em tempo real e baseada em pranchetas vetoriais**, na qual cada elemento de UI retém sua identidade vetorial (camadas, caixas de texto com auto-layout, ícones SVG e propriedades de raio de borda) enquanto ganha uma linha do tempo granular de animação.

```
┌────────────────────────────────────────────────────────────────────────┐
│                   PIPELINE DE MOTION DO DESIGN AO CÓDIGO               │
└────────────────────────────────────────────────────────────────────────┘
                                   │
              Figma Design Canvas (Vetores & Auto-Layout)
                                   │
                    Jitter Figma Plugin (Cmd+C / Cmd+V)
                                   │
                                   ▼
         ┌──────────────────────────────────────────────────────┐
         │ Jitter Motion Engine (jitter.video)                  │
         │ • Orquestração em Linha do Tempo Multi-Camada        │
         │ • Curvas Especiais: Snappy Overshoot & Impulse       │
         │ • Presets Modulares: Entrada (In), Loop, Saída (Out) │
         └──────────────────────────────────────────────────────┘
                                   │
       ┌───────────────────────────┼───────────────────────────┐
       ▼                           ▼                           ▼
┌──────────────┐            ┌──────────────┐            ┌──────────────┐
│ Lottie JSON  │            │ WebM Alpha   │            │ MP4 / ProRes │
│ (Micro-UI)   │            │ (60fps Hero) │            │ (SaaS Promo) │
└──────────────┘            └──────────────┘            └──────────────┘
       │                           │                           │
       ▼                           ▼                           ▼
Engenharia Web:              Engenharia Web:             Marketing / UI:
DotLottie / React            <video> Transparente        Social Teasers
```

---

### A Assinatura de Movimento do Jitter: Snappy, Elástico e "Product-Led"

O diferencial estético do Jitter não reside na pirotecnia visual gratuita, mas no **Product-Led Motion** — uma linguagem de movimento orientada a demonstrar com precisão cirúrgica a utilidade, a velocidade e o valor tangível de um software:

1. **Snappy Overshoot (Overshoot Controlado)**:
   Em vez de transições lineares ou de curvas lentas `ease-in-out` padrão do CSS antigo, o Jitter utiliza curvas com aceleração inicial agressiva e uma projeção elástica que ultrapassa ligeiramente a coordenada final (cerca de 3% a 6% do valor de destino), estabilizando-se em seguida sem oscilações residuais indesejadas. A sensação neurológica transmitida é de alta responsividade e firmeza física.

2. **Impulse Wind-Up (Antecipação Inversa)**:
   Antes de disparar um elemento para a frente ou ampliá-lo, o motor aplica uma sutil contração na direção oposta (dip reverso). Isso imita a física biológica e mecânica (como o ato de flexionar os joelhos antes de saltar), preparando o olho do observador para o deslocamento iminente.

3. **Layered Staggering (Cascata Rítmica de Sub-Camadas)**:
   Nenhum painel ou card de produto no Jitter se abre como uma peça única e homogênea. A moldura do cartão surge primeiro, o título desdobra-se 60ms depois, seguido pelos botões e indicadores com intervalos calculados entre 60ms e 120ms. Essa cadência temporal confere profundidade hierárquica e guia o olhar humano pela narrativa do recurso.

---

### A Tríade Funcional de Animação

No modelo arquitetural do Jitter, qualquer animação aplicada a um componente de interface se decompõe em três estágios temporais independentes:

* **Entrada (In)**: A transição de nascimento do elemento no palco. Exemplos: *Mask Wipe*, *Scale-Up Spring*, *Slide-Down Fade*, *Kinetic Word Reveal*.
* **Ênfase / Atenção (Attention / Loop)**: O comportamento contínuo enquanto o elemento permanece visível. Exemplos: *Heartbeat Pulse*, *Subtle Breathing Glow*, *Continuous Marquee*, *Badge Float*.
* **Saída (Out)**: O encerramento elegante da visibilidade, garantindo que o elemento libere a atenção do usuário para a próxima etapa sem atrair foco excessivo. Exemplos: *Scale-Down Dissolve*, *Directional Wipe-Out*, *Fast Blur Fade*.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

O ecossistema visual inaugurado e propagado pelo Jitter tornou-se a linguagem padrão das landing pages de produtos de ponta (como Notion, Linear, Raycast, Vercel e Framer).

### Casos de Uso Críticos

1. **Bento Grids Dinâmicos de Apresentação de Features**:
   - Grades modulares assimétricas onde cada bloco retangular demonstra uma funcionalidade específica do software em ação: um card simulando cursores colaborativos ao vivo; outro mostrando um toggle de permissão alternando entre estados; outro exibindo métricas numéricas subindo dinamicamente.
2. **Hero Sections com Mockups Cinematográficos (Product in Action)**:
   - Apresentação do núcleo do produto no topo da página através de loops suaves que simulam a interação humana real (digitação, seleção de comandos por teclado `Cmd+K`, arrastar e soltar de cartões Kanban).
3. **Micro-Interações Táteis de Alta Fidelidade**:
   - Estados de sucesso em transações (ícone de check animado com desdobramento de traçado vetorial), interruptores de tema (sol morphing para lua), botões de ação que colapsam temporariamente em spinners e retornam com feedback tátil.
4. **Onboarding Walkthroughs e Empty States Educativos**:
   - Telas vazias que utilizam animações Lottie vetoriais compactas para instruir o usuário sobre como dar o primeiro passo na plataforma sem recorrer a blocos de texto denso.

---

### A Regra 60-30-10 no Ecossistema Jitter

```
┌────────────────────────────────────────────────────────────────────────┐
│                   DISTRIBUIÇÃO DA REGRA 60-30-10                       │
├────────────────────────┬───────────────────────┬───────────────────────┤
│    60% DO SISTEMA      │     30% DO SISTEMA    │     10% DO SISTEMA    │
│  ESTRUTURA ESTÁVEL     │   FLUIDEZ INVISÍVEL   │   SHOWSTOPPER HERO    │
├────────────────────────┼───────────────────────┼───────────────────────┤
│ • Layout base do SaaS  │ • Toggles de status   │ • Bento Grid Demos    │
│ • Tipografia estática  │ • Dropdowns com mola  │ • Hero Product Teaser │
│ • Grids de alinhamento │ • Hover em cartões    │ • Loops Lottie de alto│
│ • Fundos neutros/base  │ • Modais com ease out │   impacto conceitual  │
└────────────────────────┴───────────────────────┴───────────────────────┘
```

* **60% — Estrutura e Estabilidade**: O layout permanece rígido, confiável e ancorado. Textos de documentação, dados analíticos e tabelas operam com estabilidade visual absoluta para garantir legibilidade imediata.
* **30% — Fluidez Invisível (Micro-Physics)**: O sistema de UI adota as curvas de desaceleração rápida e as molas do Jitter para transições funcionais cotidianas: menus que abrem com `cubic-bezier(0.16, 1, 0.3, 1)`, abas que deslizam sem pulos e botões que registram clique físico por escala micro de 0.97.
* **10% — Espetáculo Visual (Showstopper Moments)**: O mockup animado na seção Hero ou a grade Bento onde múltiplos módulos interagem de forma coreografada, estabelecendo a proposta de valor do software em segundos.

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Quando Evitar

1. **Aplicações Transacionais Críticas e Cockpits Financeiros**:
   - Em terminais de trading, consoles de gerenciamento hospitalar ou painéis de infraestrutura de nuvem com fluxos de telemetria em tempo real, animações no estilo overshoot causam ruído cognitivo e fadiga visual rápida. O operador precisa de dados instantâneos sem atrasos de 300ms a 600ms.
2. **Loops Visuais Concorrentes no Mesmo Viewport**:
   - Ter 5 ou 6 cards dentro de uma tela executando animações contínuas desincronizadas cria um efeito de "árvore de natal", fragmentando a atenção do usuário e destruindo a hierarquia de conversão da página.
3. **Fluxos de Checkout e Confirmação de Pagamento**:
   - Botões de pagamento com efeitos elásticos exagerados ou atrasos na confirmação transmitem sensação de instabilidade ou fragilidade no processamento financeiro. A resposta deve ser sóbria, rápida e inequívoca.

---

### ⚠️ Regras Estritas de Acessibilidade & GPU

1. **Respeito Obrigatório a `prefers-reduced-motion`**:
   - Usuários com transtornos vestibulares são gravemente afetados por animações contínuas de escala, rotação e deslocamentos com overshoot. É mandatório detectar a preferência de acessibilidade:
     ```css
     @media (prefers-reduced-motion: reduce) {
       *, *::before, *::after {
         animation-duration: 0.01ms !important;
         animation-iteration-count: 1 !important;
         transition-duration: 0.01ms !important;
         scroll-behavior: auto !important;
       }
       video[autoplay] {
         display: none !important;
       }
     }
     ```
   - No React/Framer Motion, sempre envolva animações com `useReducedMotion()`.

2. **Sobrecarga de Renderização: Lottie vs. WebM vs. Framer Motion**:
   - **Lottie (SVG)**: Manipula elementos reais dentro da árvore DOM do navegador. Executar mais de 3 instâncias Lottie simultâneas com dezenas de formas vetoriais no mesmo viewport provoca alto consumo de CPU e constantes recálculos de estilo (*recalc style*).
   - **WebM com Alpha Channel (VP9)**: Desloca o trabalho de rasterização inteiramente para a GPU através do hardware video decoder nativo do sistema operacional. Para loops complexos com sombras e desfoques, o WebM consome consideravelmente menos CPU do que renderizadores de Canvas/SVG baseados em JavaScript.
   - **Framer Motion / CSS Transforms**: Ideal para elementos interativos nativos que precisam responder ao foco de teclado, cliques e leitura de acessibilidade (*screen readers*).

3. **Uso Disciplinado de `will-change` e `contain`**:
   - Nunca aplique `will-change: transform, opacity` globalmente no CSS. Aplique-o dinamicamente apenas durante a janela ativa de interpolação e remova-o quando o elemento estiver em repouso para evitar o consumo descontrolado de VRAM da GPU.
   - Utilize `contain: paint` ou `contain: layout` nos cards modulares para isolar o repaint dentro da caixa delimitadora do componente.

---

## 4. Catálogo Detalhado de Componentes / Padrões / Efeitos Notáveis

Abaixo estão os 10 padrões de movimento mais icônicos originados e popularizados pela estética de produto do Jitter:

```
┌────────────────────────────────────────────────────────────────────────┐
│                 CATÁLOGO DE PADRÕES DE MOVIMENTO JITTER                 │
├─────┬───────────────────────────────┬──────────────────────────────────┤
│ #   │ PADRÃO / EFEITO               │ GATILHO & COMPORTAMENTO          │
├─────┼───────────────────────────────┼──────────────────────────────────┤
│ 01  │ Bento Choreographed Entry     │ Scroll Into View / Cascata (In)  │
│ 02  │ Morphing UI Action Card       │ Pointer Hover / Layout Toggle    │
│ 03  │ Kinetic Typography Wave       │ Viewport Mount / Stagger Words   │
│ 04  │ Snappy Overshoot Switch       │ User Toggle / Elastic Spring     │
│ 05  │ Impulse Wind-Up Button        │ Pointer Press / Micro-Anticipate │
│ 06  │ Geometry Mask Wipe            │ Scroll Scrub / Slide Reveal      │
│ 07  │ Simulated Multi-User Cursors  │ Loop Contínuo / Motion Path      │
│ 08  │ Live Telemetry Pulse Badge    │ Loop Permanente / Heartbeat      │
│ 09  │ Metric Counter & SVG Progress │ In-View Trigger / Ease-Out Expo  │
│ 10  │ Stacking Notification Drawer  │ Event Trigger / Spring Gravity   │
└─────┴───────────────────────────────┴──────────────────────────────────┘
```

### 1. Bento Choreographed Entry
- **Comportamento Visual**: Uma grade assimétrica com 3 a 5 cartões surge na tela em sequência rítmica. Cada cartão inicia em escala `0.94`, transladado em Y por `24px` e com opacidade `0`. A entrada utiliza a curva *Snappy Overshoot* com um atraso (*stagger*) de `80ms` entre cada item. Dentro de cada cartão, os elementos internos (ícones, títulos e botões) desdobram-se com um segundo nível de cascata interna de `40ms`.
- **Gatilho**: Entrada no viewport (`whileInView` com viewport margin de `-80px`).
- **Onde Encaixar**: Seções de recursos principais de landing pages de SaaS B2B e plataformas de desenvolvedor.

### 2. Morphing UI Action Card
- **Comportamento Visual**: O cartão de tarefa encontra-se inicialmente colapsado com um badge e texto simples. Ao receber foco ou hover, a moldura expande suas dimensões de altura e largura suavemente através de interpolação fluida de layout (`layoutId` no Framer Motion), revelando avatares de participantes, botões de ação secundária e uma linha divisória que desenha seu traço da esquerda para a direita.
- **Gatilho**: `onHoverStart` ou alternância de estado de seleção (`onClick`).
- **Onde Encaixar**: Cards de gerenciadores de projetos, cartões de planos de preços expansíveis e itens de lista interativos.

### 3. Kinetic Typography Wave
- **Comportamento Visual**: Títulos de impacto têm suas palavras ou caracteres divididos em nós individuais dentro de contêineres de overflow oculto (`overflow-hidden`). Cada palavra sobe da borda inferior invisível (`translateY(100%)`) para a posição zero com ligeira inclinação angular (`rotate(3deg)` para `rotate(0deg)`) e opacidade crescente. O espaçamento rítmico entre as palavras é fixado em `45ms`.
- **Gatilho**: Montagem da Hero Section ou transição de slide no carrossel de produto.
- **Onde Encaixar**: Headlines de topo em páginas de apresentação de marca e aberturas de artigos editoriais técnicos.

### 4. Snappy Overshoot Switch (Toggle Mecânico)
- **Comportamento Visual**: A chave alternadora (toggle switch) reage com um estalo mecânico: a bolha interna (`thumb`) não desliza com velocidade constante; ela acelera instantaneamente, expande sua largura horizontalmente em 25% durante o percurso (simulando deformação elástica por aceleração / *stretch*) e, ao colidir com o limite da caixa, ultrapassa o ponto final por `3px` antes de retornar e reassumir a forma circular perfeita. Ao mesmo tempo, o fundo transita de cor com curva cúbica sincronizada.
- **Gatilho**: Clique do usuário ou ativação por teclado (`Space` / `Enter`).
- **Onde Encaixar**: Painéis de configurações, alternadores de cobrança mensal/anual e seletores de tema dark/light.

### 5. Impulse Wind-Up Button
- **Comportamento Visual**: Ao ser pressionado, o botão não apenas afunda: ele retrai levemente a sua escala para `0.95` com ligeiro recuo na posição espacial (`translateY(2px)`). No momento da soltura, ele dispara para frente ultrapassando a escala neutra (`1.02`) e acomoda-se com amortecimento rápido em `1.0`. Esse padrão cria a sensação tátil de um interruptor mecânico sob forte pressão de mola.
- **Gatilho**: Eventos de ponteiro `pointerdown` e `pointerup`.
- **Onde Encaixar**: Botões primários de conversão (*Call to Action*), botões de disparo de fluxo e ações de compra.

### 6. Geometry Mask Wipe (Clip-Path Reveal)
- **Comportamento Visual**: Uma captura de tela de alta resolução da aplicação surge na tela através de uma máscara geométrica com `clip-path: inset(0% 0% 100% 0% round 16px)`. A máscara desliza de baixo para cima revelando a interface interna enquanto o conteúdo dentro dela faz um sutil contramovimento de paralaxe vertical descendente de `30px` para `0px`, criando a percepção de uma lente óptica revelando uma superfície física.
- **Gatilho**: Rolagem da página atrelada à posição do elemento ou trigger de entrada.
- **Onde Encaixar**: Demonstrações de telas de dashboard e transições antes/depois em páginas de produtos digitais.

### 7. Simulated Multi-User Cursors
- **Comportamento Visual**: Três cursores vetorizados coloridos (com nomes flutuantes como "Sarah", "Alex", "Dev") deslocam-se pelo mockup da interface seguindo caminhos de Bézier contínuos e orgânicos. Um cursor clica em um elemento gerando um círculo de ripple translúcido; outro arrasta um card de uma coluna para outra; e o terceiro digita um comentário simulado com indicador de digitação pulsante.
- **Gatilho**: Loop contínuo com ciclo temporal de 8 a 12 segundos, sincronizado ou via gatilho de hover no cartão.
- **Onde Encaixar**: Cards de apresentação de colaboração em tempo real (estilo Figma, Miro ou Linear).

### 8. Live Telemetry Pulse Badge
- **Comportamento Visual**: Um chip arredondado exibindo o status do sistema (ex: "All Systems Normal" ou "AI Worker Ready"). Ao lado do texto, um círculo verde esmeralda de `8px` pulsa em dois níveis: o núcleo sólido permanece estável, enquanto uma aura externa concêntrica se expande em escala de `1.0` para `2.4` e dissolve sua opacidade de `0.75` para `0` em um ciclo sinusoidal infinito de 2 segundos.
- **Gatilho**: Montagem de status ativo (loop contínuo via CSS keyframes).
- **Onde Encaixar**: Indicadores de status de servidores, badges de disponibilidade de produto e selos de garantia em tempo real.

### 9. Metric Counter & SVG Progress Ring
- **Comportamento Visual**: Um indicador numérico (ex: "99.9% Uptime" ou "3.8x Faster") roda seus dígitos de `0` até o valor final em `1.2s` através de uma interpolação desacelerada com curva exponencial. Simultaneamente, um anel vetorial SVG circundante preenche sua borda com a propriedade `stroke-dashoffset` calculada, finalizando com um sutil efeito de brilho na ponta do traçado.
- **Gatilho**: `whileInView` com 20% de visibilidade no viewport.
- **Onde Encaixar**: Estatísticas de desempenho, cards de eficiência e métricas de impacto empresarial.

### 10. Stacking Notification Drawer
- **Comportamento Visual**: Notificações flutuantes simuladas caem do topo da prancheta e acomodam-se na base da tela. Conforme uma nova mensagem chega com mola elástica descendente, as mensagens anteriores recuam ligeiramente em escala (`0.95`, `0.90`), aplicam desfoque gaussiano suave (`blur(2px)`) e deslocam-se para trás no eixo Z com opacidade atenuada, demonstrando profundidade de pilha física.
- **Gatilho**: Ciclo intervalado simulado em showcase de produto.
- **Onde Encaixar**: Demos de produtos de mensageria, sistemas de alerta e central de notificações.

---

## 5. Arquitetura Técnica, Física de Movimento & Receitas de Código Funcional

### Parâmetros Físicos & Curvas Exatas de Bézier

O segredo da estética do Jitter reside em suas curvas de tempo proprietárias e na calibração precisa das molas amortecidas:

```
┌────────────────────────────────────────────────────────────────────────┐
│                   CURVAS DE TEMPO MATEMÁTICAS DO JITTER                │
├────────────────────────┬───────────────────────────────────────────────┤
│ CURVA                  │ ESPECIFICAÇÃO & EQUAÇÃO                       │
├────────────────────────┼───────────────────────────────────────────────┤
│ Snappy Overshoot       │ cubic-bezier(0.34, 1.56, 0.64, 1)             │
│ Smooth Product Ease    │ cubic-bezier(0.16, 1, 0.3, 1) (Quartic Out)   │
│ Impulse Wind-Up Launch │ cubic-bezier(0.6, -0.28, 0.735, 0.045)        │
│ Kinetic Text Ease      │ cubic-bezier(0.25, 1, 0.5, 1)                 │
└────────────────────────┴───────────────────────────────────────────────┘
```

#### Equivalência em Molas Harmônicas (Framer Motion / Motion.dev)

Quando implementadas no React através de sistemas de física de molas (*spring physics*), as configurações equivalentes para atingir o feel do Jitter são:

```typescript
// 1. Snappy Elastic Spring (Ideal para Toggles, Botões e Badges)
export const snappySpring = {
  type: "spring" as const,
  stiffness: 420,
  damping: 28,
  mass: 0.8,
  restDelta: 0.001,
};

// 2. Smooth Product Morph (Ideal para Expansão de Cards e Modais)
export const smoothMorphSpring = {
  type: "spring" as const,
  stiffness: 240,
  damping: 24,
  mass: 1.0,
  restDelta: 0.001,
};

// 3. High-Mass Mechanical Bounce (Para Notificações Caindo)
export const heavyDropSpring = {
  type: "spring" as const,
  stiffness: 300,
  damping: 20,
  mass: 1.2,
};
```

---

### Tabela Decisória de Formato de Exportação

| Cenário de Uso | Formato Recomendado | Justificativa Técnica | Alternativa Fallback |
| :--- | :--- | :--- | :--- |
| **Micro-interações no App (Toggles, Ícones, Checkmarks)** | **DotLottie (.lottie / .json)** | Vetorial puro, escala para qualquer DPR sem pixelização, peso < 30KB, interativo via código. | Framer Motion nativo em nós SVG. |
| **Hero Sections com Mockup 3D / Sombras complexas** | **Transparent WebM (VP9 com Alpha)** | 60fps constantes sem sobrecarregar a CPU com centenas de nós SVG no DOM; aceita canal alfa real sobre fundos CSS dinâmicos. | MP4 H.264 em container fechado com fundo sólido compatível. |
| **Grades Bento Interativas e Responsivas** | **React + Framer Motion (Código)** | Permite que o texto seja selecionável e indexável (SEO), botões sejam acessíveis por teclado e o layout se adapte dinamicamente à tela. | WebM cortado por CSS grid responsivo. |
| **Vídeos de Divulgação Social e Email Marketing** | **MP4 H.264 (60fps) / GIF Otimizado** | Compatibilidade universal em navegadores, clientes de email e reprodutores de mídia de terceiros. | Loop estático com botão de play. |

---

### Código Funcional Completo: Bento Grid Feature Showcase no Estilo Jitter

Abaixo está a implementação completa e em nível de produção de um **Bento Feature Showcase** desenvolvido em **React 19, TypeScript, Tailwind CSS e Framer Motion**, incorporando:
- Card 1: Simulação interativa de cursores de usuários colaborativos em tempo real.
- Card 2: Toggle mecânico com física Snappy Overshoot e badge de telemetria ativo.
- Card 3: Contador numérico dinâmico sincronizado com círculo de progresso SVG.
- Suporte integral a `useReducedMotion()`.

```tsx
import React, { useState, useEffect } from "react";
import { motion, useReducedMotion, AnimatePresence } from "framer-motion";
import {
  Sparkles,
  CheckCircle2,
  Users,
  Sliders,
  Activity,
  ArrowUpRight,
  MousePointer2,
} from "lucide-react";

// ============================================================================
// CURVAS E MOLAS NO ESTILO JITTER
// ============================================================================
const JITTER_EASINGS = {
  snappyOvershoot: [0.34, 1.56, 0.64, 1] as const,
  smoothProduct: [0.16, 1, 0.3, 1] as const,
};

const snappySpringConfig = {
  type: "spring" as const,
  stiffness: 420,
  damping: 26,
  mass: 0.8,
};

export const JitterBentoShowcase: React.FC = () => {
  const shouldReduceMotion = useReducedMotion();

  // Estados dos cartões interativos
  const [isFeatureActive, setIsFeatureActive] = useState<boolean>(true);
  const [metricProgress, setMetricProgress] = useState<number>(0);

  // Gatilho animado de métrica contínua
  useEffect(() => {
    if (shouldReduceMotion) {
      setMetricProgress(99.4);
      return;
    }
    const timer = setTimeout(() => {
      setMetricProgress(99.4);
    }, 400);
    return () => clearTimeout(timer);
  }, [shouldReduceMotion]);

  // Variantes para orquestração da grade com stagger
  const containerVariants = {
    hidden: { opacity: 0 },
    visible: {
      opacity: 1,
      transition: {
        staggerChildren: shouldReduceMotion ? 0 : 0.09,
        delayChildren: 0.1,
      },
    },
  };

  const cardVariants = {
    hidden: {
      opacity: 0,
      y: shouldReduceMotion ? 0 : 28,
      scale: shouldReduceMotion ? 1 : 0.96,
    },
    visible: {
      opacity: 1,
      y: 0,
      scale: 1,
      transition: {
        duration: 0.65,
        ease: JITTER_EASINGS.snappyOvershoot,
      },
    },
  };

  return (
    <section className="relative w-full max-w-6xl mx-auto px-4 py-16 bg-neutral-950 text-neutral-100 font-sans antialiased overflow-hidden selection:bg-indigo-500/30">
      {/* Luz ambiente de fundo */}
      <div
        className="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[600px] h-[300px] bg-gradient-to-tr from-indigo-500/15 via-purple-500/10 to-transparent blur-[120px] pointer-events-none rounded-full"
        aria-hidden="true"
      />

      {/* Cabeçalho da Seção com Revelação Cinética */}
      <div className="relative z-10 max-w-2xl mb-12">
        <motion.div
          initial={{ opacity: 0, y: shouldReduceMotion ? 0 : 12 }}
          whileInView={{ opacity: 1, y: 0 }}
          viewport={{ once: true, margin: "-40px" }}
          transition={{ duration: 0.5, ease: JITTER_EASINGS.smoothProduct }}
          className="inline-flex items-center gap-2 px-3 py-1 mb-4 rounded-full border border-neutral-800 bg-neutral-900/60 backdrop-blur-md text-xs font-medium text-neutral-400"
        >
          <Sparkles className="w-3.5 h-3.5 text-indigo-400" />
          <span>Product-Led Motion System</span>
        </motion.div>

        <motion.h2
          initial={{ opacity: 0, y: shouldReduceMotion ? 0 : 18 }}
          whileInView={{ opacity: 1, y: 0 }}
          viewport={{ once: true, margin: "-40px" }}
          transition={{
            duration: 0.6,
            delay: 0.08,
            ease: JITTER_EASINGS.smoothProduct,
          }}
          className="text-3xl md:text-5xl font-semibold tracking-tight text-neutral-100 leading-[1.15]"
        >
          Experiências de software que{" "}
          <span className="text-transparent bg-clip-text bg-gradient-to-r from-indigo-400 via-violet-300 to-purple-400">
            parecem vivas.
          </span>
        </motion.h2>

        <motion.p
          initial={{ opacity: 0, y: shouldReduceMotion ? 0 : 14 }}
          whileInView={{ opacity: 1, y: 0 }}
          viewport={{ once: true, margin: "-40px" }}
          transition={{
            duration: 0.6,
            delay: 0.16,
            ease: JITTER_EASINGS.smoothProduct,
          }}
          className="mt-4 text-base md:text-lg text-neutral-400 leading-relaxed font-normal"
        >
          Micro-interações de 60fps com curvas elásticas milimetricamente
          calibradas para demonstrar o valor e o ritmo do seu produto digital.
        </motion.p>
      </div>

      {/* Bento Grid Coreografado */}
      <motion.div
        variants={containerVariants}
        initial="hidden"
        whileInView="visible"
        viewport={{ once: true, margin: "-60px" }}
        className="relative z-10 grid grid-cols-1 md:grid-cols-3 gap-5"
      >
        {/* ============================================================== */}
        {/* CARD 1 (Largo): Simulação de Cursores Colaborativos            */}
        {/* ============================================================== */}
        <motion.div
          variants={cardVariants}
          className="group relative md:col-span-2 rounded-2xl border border-neutral-800/80 bg-neutral-900/40 p-6 md:p-8 backdrop-blur-md overflow-hidden flex flex-col justify-between hover:border-neutral-700/80 transition-colors duration-300"
        >
          {/* Palco interativo de simulação de cursores */}
          <div className="relative w-full h-56 md:h-64 rounded-xl border border-neutral-800/60 bg-neutral-950/70 overflow-hidden flex items-center justify-center p-6">
            {/* Grade pontilhada de prancheta */}
            <div
              className="absolute inset-0 opacity-[0.12]"
              style={{
                backgroundImage:
                  "radial-gradient(circle, #a1a1aa 1px, transparent 1px)",
                backgroundSize: "20px 20px",
              }}
              aria-hidden="true"
            />

            {/* Elemento central selecionado por múltiplos usuários */}
            <motion.div
              layout
              className="relative z-10 px-6 py-4 rounded-xl border-2 border-indigo-500/80 bg-neutral-900/90 shadow-2xl shadow-indigo-500/10 flex items-center gap-4"
              whileHover={shouldReduceMotion ? {} : { scale: 1.02 }}
              transition={snappySpringConfig}
            >
              <div className="w-10 h-10 rounded-lg bg-indigo-500/20 border border-indigo-500/40 flex items-center justify-center text-indigo-400">
                <Users className="w-5 h-5" />
              </div>
              <div>
                <p className="text-sm font-medium text-neutral-200">
                  Global State Sync
                </p>
                <p className="text-xs text-neutral-400">
                  Real-time multi-agent sync
                </p>
              </div>
              <div className="ml-2 w-2 h-2 rounded-full bg-emerald-400 animate-pulse" />
            </motion.div>

            {/* Cursor Simulado 1: Sarah (Indigo) */}
            {!shouldReduceMotion && (
              <motion.div
                className="absolute z-20 pointer-events-none flex items-center gap-1.5"
                animate={{
                  x: [-60, 40, -20, -60],
                  y: [-30, 20, -40, -30],
                }}
                transition={{
                  duration: 8,
                  repeat: Infinity,
                  ease: "easeInOut",
                }}
              >
                <MousePointer2 className="w-4 h-4 text-indigo-400 fill-indigo-400 drop-shadow-md" />
                <span className="px-2 py-0.5 rounded-md bg-indigo-500 text-white text-[10px] font-semibold tracking-wide shadow-lg">
                  Sarah
                </span>
              </motion.div>
            )}

            {/* Cursor Simulado 2: Alex (Violeta) */}
            {!shouldReduceMotion && (
              <motion.div
                className="absolute z-20 pointer-events-none flex items-center gap-1.5"
                animate={{
                  x: [80, -30, 50, 80],
                  y: [40, -50, 10, 40],
                }}
                transition={{
                  duration: 9.5,
                  repeat: Infinity,
                  ease: "easeInOut",
                  delay: 0.8,
                }}
              >
                <MousePointer2 className="w-4 h-4 text-violet-400 fill-violet-400 drop-shadow-md" />
                <span className="px-2 py-0.5 rounded-md bg-violet-500 text-white text-[10px] font-semibold tracking-wide shadow-lg">
                  Alex
                </span>
              </motion.div>
            )}
          </div>

          <div className="mt-6 flex items-end justify-between">
            <div>
              <span className="text-xs font-semibold tracking-wider text-indigo-400 uppercase">
                Colaboração Real-Time
              </span>
              <h3 className="text-xl font-semibold text-neutral-100 mt-1">
                Sincronização de Pranchetas Vivas
              </h3>
              <p className="text-sm text-neutral-400 mt-1.5 max-w-md">
                Edite timelines com múltiplos designers ao vivo. Nenhuma colisão
                de estado, suporte a histórico vetorial com auto-layout.
              </p>
            </div>
            <div className="w-8 h-8 rounded-full border border-neutral-800 flex items-center justify-center text-neutral-400 group-hover:text-neutral-100 group-hover:border-neutral-700 transition-colors">
              <ArrowUpRight className="w-4 h-4" />
            </div>
          </div>
        </motion.div>

        {/* ============================================================== */}
        {/* CARD 2: Toggle Mecânico com Snappy Overshoot                   */}
        {/* ============================================================== */}
        <motion.div
          variants={cardVariants}
          className="group relative rounded-2xl border border-neutral-800/80 bg-neutral-900/40 p-6 md:p-8 backdrop-blur-md overflow-hidden flex flex-col justify-between hover:border-neutral-700/80 transition-colors duration-300"
        >
          <div>
            <div className="flex items-center justify-between mb-6">
              <div className="w-10 h-10 rounded-xl bg-neutral-800/80 border border-neutral-700/60 flex items-center justify-center text-neutral-300">
                <Sliders className="w-5 h-5" />
              </div>
              {/* Badge de Telemetria com Heartbeat Pulse */}
              <div className="flex items-center gap-1.5 px-2.5 py-1 rounded-full border border-emerald-500/30 bg-emerald-500/10 text-emerald-400 text-xs font-medium">
                <span className="relative flex h-2 w-2">
                  <span className="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75" />
                  <span className="relative inline-flex rounded-full h-2 w-2 bg-emerald-500" />
                </span>
                Active 60fps
              </div>
            </div>

            <span className="text-xs font-semibold tracking-wider text-neutral-400 uppercase">
              Micro-Mecânica
            </span>
            <h3 className="text-xl font-semibold text-neutral-100 mt-1">
              Snappy Switch
            </h3>
            <p className="text-sm text-neutral-400 mt-1.5">
              Física de mola com rebote que ultrapassa o limite antes de ancorar.
            </p>
          </div>

          {/* Área Interativa com Interruptor Tátil */}
          <div className="mt-8 pt-6 border-t border-neutral-800/60 flex items-center justify-between">
            <span className="text-sm font-medium text-neutral-300">
              {isFeatureActive ? "Física Ativada" : "Movimento Rígido"}
            </span>

            {/* Toggle Button com AnimatePresence e Spring */}
            <button
              type="button"
              role="switch"
              aria-checked={isFeatureActive}
              onClick={() => setIsFeatureActive(!isFeatureActive)}
              className={`relative inline-flex h-8 w-14 shrink-0 cursor-pointer rounded-full border-2 border-transparent transition-colors duration-300 focus:outline-none focus-visible:ring-2 focus-visible:ring-indigo-500 ${
                isFeatureActive ? "bg-indigo-600" : "bg-neutral-800"
              }`}
            >
              <span className="sr-only">Alternar física mecânica</span>
              <motion.span
                layout
                transition={snappySpringConfig}
                className={`pointer-events-none block h-7 w-7 rounded-full bg-white shadow-lg ring-0 ${
                  isFeatureActive ? "translate-x-6" : "translate-x-0"
                }`}
              />
            </button>
          </div>
        </motion.div>

        {/* ============================================================== */}
        {/* CARD 3: Métricas Numéricas & SVG Progress Ring                 */}
        {/* ============================================================== */}
        <motion.div
          variants={cardVariants}
          className="group relative rounded-2xl border border-neutral-800/80 bg-neutral-900/40 p-6 md:p-8 backdrop-blur-md overflow-hidden flex flex-col justify-between hover:border-neutral-700/80 transition-colors duration-300"
        >
          <div>
            <div className="w-10 h-10 rounded-xl bg-neutral-800/80 border border-neutral-700/60 flex items-center justify-center text-neutral-300 mb-6">
              <Activity className="w-5 h-5 text-indigo-400" />
            </div>

            <span className="text-xs font-semibold tracking-wider text-purple-400 uppercase">
              Telemetria & Performance
            </span>
            <h3 className="text-xl font-semibold text-neutral-100 mt-1">
              Zero Frame Drop
            </h3>
            <p className="text-sm text-neutral-400 mt-1.5">
              Renderizado por hardware diretamente na GPU com canal alfa
              transparente.
            </p>
          </div>

          {/* Gráfico Circular SVG com Traçado Animado */}
          <div className="mt-8 pt-6 border-t border-neutral-800/60 flex items-center justify-between">
            <div className="relative flex items-center justify-center">
              <svg className="w-20 h-20 -rotate-90" viewBox="0 0 72 72">
                {/* Trilha de fundo */}
                <circle
                  cx="36"
                  cy="36"
                  r="30"
                  className="stroke-neutral-800"
                  strokeWidth="5"
                  fill="transparent"
                />
                {/* Arco animado */}
                <motion.circle
                  cx="36"
                  cy="36"
                  r="30"
                  className="stroke-indigo-500"
                  strokeWidth="5"
                  strokeDasharray="188.4"
                  fill="transparent"
                  strokeLinecap="round"
                  initial={{ strokeDashoffset: 188.4 }}
                  whileInView={{
                    strokeDashoffset: 188.4 * (1 - metricProgress / 100),
                  }}
                  viewport={{ once: true }}
                  transition={{
                    duration: 1.4,
                    ease: JITTER_EASINGS.smoothProduct,
                  }}
                />
              </svg>
              <div className="absolute flex flex-col items-center">
                <span className="text-sm font-bold text-neutral-100 font-mono">
                  {metricProgress > 0 ? `${metricProgress}%` : "0%"}
                </span>
              </div>
            </div>

            <div className="text-right">
              <div className="flex items-center gap-1.5 justify-end text-emerald-400 text-xs font-semibold">
                <CheckCircle2 className="w-3.5 h-3.5" />
                <span>VP9 Alpha</span>
              </div>
              <p className="text-[11px] text-neutral-500 mt-0.5">
                4K a 60fps constantes
              </p>
            </div>
          </div>
        </motion.div>

        {/* ============================================================== */}
        {/* CARD 4 (Largo): Export Engine — Lottie & WebM Pipeline         */}
        {/* ============================================================== */}
        <motion.div
          variants={cardVariants}
          className="group relative md:col-span-2 rounded-2xl border border-neutral-800/80 bg-neutral-900/40 p-6 md:p-8 backdrop-blur-md overflow-hidden flex flex-col justify-between hover:border-neutral-700/80 transition-colors duration-300"
        >
          <div className="flex flex-col md:flex-row md:items-center justify-between gap-6 mb-6">
            <div>
              <span className="text-xs font-semibold tracking-wider text-indigo-400 uppercase">
                Export Matrix
              </span>
              <h3 className="text-xl font-semibold text-neutral-100 mt-1">
                Da Prancheta para Produção
              </h3>
              <p className="text-sm text-neutral-400 mt-1.5 max-w-md">
                Exporte diretamente para pacotes Lottie ultraleves de 20KB ou
                vídeos WebM transparentes sem sobrecarga no DOM.
              </p>
            </div>

            {/* Badges de Formatos com Hover Reativo */}
            <div className="flex flex-wrap gap-2">
              {["Lottie JSON", "WebM Alpha", "MP4 60fps", "ProRes 4444"].map(
                (fmt, index) => (
                  <motion.span
                    key={fmt}
                    whileHover={shouldReduceMotion ? {} : { scale: 1.05, y: -2 }}
                    transition={snappySpringConfig}
                    className={`px-3 py-1 rounded-lg text-xs font-mono font-medium border ${
                      index === 0
                        ? "border-indigo-500/40 bg-indigo-500/10 text-indigo-300"
                        : index === 1
                        ? "border-emerald-500/40 bg-emerald-500/10 text-emerald-300"
                        : "border-neutral-800 bg-neutral-950/60 text-neutral-400"
                    }`}
                  >
                    {fmt}
                  </motion.span>
                )
              )}
            </div>
          </div>

          {/* Terminal / Code Snippet Preview */}
          <div className="w-full rounded-xl border border-neutral-800/70 bg-neutral-950 p-4 font-mono text-xs text-neutral-300 overflow-x-auto">
            <div className="flex items-center gap-2 mb-2 pb-2 border-b border-neutral-800/60 text-neutral-500 text-[11px]">
              <div className="w-2.5 h-2.5 rounded-full bg-neutral-700" />
              <div className="w-2.5 h-2.5 rounded-full bg-neutral-700" />
              <div className="w-2.5 h-2.5 rounded-full bg-neutral-700" />
              <span className="ml-2">production-export.ts</span>
            </div>
            <code className="text-neutral-400">
              <span className="text-purple-400">import</span> &#123; DotLottieReact &#125;{" "}
              <span className="text-purple-400">from</span>{" "}
              <span className="text-emerald-400">
                &apos;@lottiefiles/dotlottie-react&apos;
              </span>
              ;<br />
              <span className="text-neutral-500">// Payload < 24KB com curvas Jitter preservadas</span>
              <br />
              &lt;<span className="text-indigo-400">DotLottieReact</span> src=
              <span className="text-emerald-400">
                &quot;/assets/jitter-switch.lottie&quot;
              </span>{" "}
              autoplay loop /&gt;
            </code>
          </div>
        </motion.div>
      </motion.div>
    </section>
  );
};
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao integrar o motor de design e a física visual do **Jitter** nas especificações do `DESIGN_BLUEPRINT.md` de qualquer produto digital, a inteligência artificial ou a equipe de design de produto deve documentar expressamente os seguintes tópicos antes de redigir o código:

### Matriz Obrigatória de Especificação de Motion

```markdown
### Motion Architecture Specification (Jitter Standard)

| Componente de UI | Curva / Easing | Duração (ms) | Stagger (ms) | Fallback Acessibilidade | Formato de Render |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Hero Title Kinetic** | `cubic-bezier(0.25, 1, 0.5, 1)` | 550ms | 45ms / palavra | Opacidade simples (0 -> 1) | Framer Motion (SplitText) |
| **Bento Grid Cards** | `cubic-bezier(0.34, 1.56, 0.64, 1)` | 650ms | 80ms / card | Posição estática imediata | CSS Grid + Tailwind |
| **Micro Toggles / Chaves** | Spring: `{stiffness: 420, damping: 26}` | ~320ms | 0ms | Sem elasticidade | Framer Motion / WAAPI |
| **Mockup 3D Hero Loop** | Linear ou 60fps frame cycle | 8000ms loop | N/A | Imagem WebP estática | `<video>` WebM Alpha |
| **Notificação Drawer** | Spring: `{stiffness: 300, damping: 20}` | ~450ms | 100ms / item | Slide Y direto | Radix Dialog / Framer |
```

---

### Tokens de Animação para Tailwind CSS (V3 / V4)

Para garantir consistência rigorosa em todo o repositório, inclua a extensão de tokens do Jitter no arquivo `tailwind.config.ts`:

```typescript
// tailwind.config.ts
export default {
  theme: {
    extend: {
      transitionTimingFunction: {
        'jitter-snappy': 'cubic-bezier(0.34, 1.56, 0.64, 1)',
        'jitter-product': 'cubic-bezier(0.16, 1, 0.3, 1)',
        'jitter-impulse': 'cubic-bezier(0.6, -0.28, 0.735, 0.045)',
      },
      transitionDuration: {
        'micro': '180ms',
        'layout': '320ms',
        'choreography': '650ms',
      },
    },
  },
};
```

---

### Checklist de Engenharia Pré-Deploy

- [ ] **Auditoria de `prefers-reduced-motion`**: Todos os componentes dinâmicos utilizam o hook `useReducedMotion()` do Framer Motion ou as classes CSS `@media (prefers-reduced-motion: reduce)`.
- [ ] **Isolamento de Pintura (`contain`)**: Elementos com transformações ativas em loop utilizam `contain: paint` ou `contain: layout` para evitar recalcular os nós da árvore principal.
- [ ] **Desligamento Fora do Viewport**: Players de Lottie ou tags `<video>` transparentes monitoram a interseção com o viewport através de `IntersectionObserver`, pausando loops imediatamente quando saem da tela.
- [ ] **Controle de Payload de Mídia**: Nenhuma animação em formato de vídeo transparente ultrapassa 1.5MB; animações Lottie vetoriais são compactadas via formato `.lottie` (DotLottie), garantindo payloads abaixo de 40KB.
