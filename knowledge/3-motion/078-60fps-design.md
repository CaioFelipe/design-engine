---
id: "60fps-design"
name: "60fps Design"
url: "https://www.60fps.design/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["Native Mobile Physics", "60fps/120fps Fluidity", "Spring-Driven Micro-Interactions", "Tactile Gesture Mechanics", "Zero-Jank Compositor Animations", "Choreographed Transitions"]
densidade_informacao: "Independente"
impacto_visual: "Sutil/Invisivel (Feel) a Moderado (com picos de Espetáculo em Onboardings e Confirmações)"
custo_computacional: "Baixo (CSS/WAAPI) a Medio (Motion Springs/RAF Gesture Tracking/GPU Layering)"
stack_frameworks: ["React", "Motion.dev / Framer Motion", "Tailwind CSS", "SwiftUI / React Native", "Web Animations API (WAAPI)", "Lucide Icons"]
compatibilidade:
  combinacoes_recomendadas: ["Motion.dev + Tailwind CSS + Radix Primitives", "Lenis Scroll + Spring Physics Layout", "Lucide React + SVG Path Morphing", "Web Audio API / Haptic Vibration API + Spring Sliders", "Shadcn UI + 60fps Native Sheet Gestures"]
  conflitos_esteticos: ["Animação de propriedades de layout (width, height, top, margin) que causam reflow e jank", "Interpolações lineares frias em botões e gavetas que quebram o feel nativo", "Durações arbitrárias acima de 400ms em ações repetitivas de trabalho", "Ignorar prefers-reduced-motion e causar cinetose em usuários sensíveis", "Gestos de toque na web sem desativação de scroll conflitante (touch-action)"]
---

# 60fps Design — Dossiê de Física de Movimento, Transições & Microinterações Nativas

## 1. Filosofia de Movimento & Sensação Física (Feel)

O **60fps Design** (`https://www.60fps.design/`), fundado pelo designer e educador **Abhinav Chhikara**, é a principal referência global e biblioteca de curadoria em câmera lenta e alta taxa de quadros (60fps e 120fps) dedicada a dissecar a mecânica interna de animações, transições e microinterações de aplicativos móveis e web de classe mundial (tais como **Apple iOS**, **Linear**, **Cash App**, **Family**, **Duolingo**, **Airbnb**, **Luma**, **Things 3** e **Raycast**).

A plataforma transcende a mera galeria estética: funciona como um laboratório de engenharia reversa de cinemática digital. Ao gravar e decompor interações nativas quadro a quadro (*frame-by-frame scrubbing* a 0.25x e 0.5x), o 60fps.design revela com rigor matemático como a percepção humana de qualidade, confiabilidade e prazer tátil é construída por meio de física de molas reais, inércia de gestos e eliminação absoluta de travamentos (*zero jank*).

```
┌────────────────────────────────────────────────────────────────────────┐
│                   THE 60FPS / 120FPS TIMING BUDGET                     │
├────────────────────────────────────────────────────────────────────────┤
│  60 FPS (Standard Display)  │ [ 16.6ms Total Window per Frame ]        │
│                             │   ├── Input & JS Engine : ≤ 6ms          │
│                             │   ├── Style & Layout    : ≤ 4ms          │
│                             │   └── GPU Paint/Composite: ≤ 6.6ms       │
├────────────────────────────────────────────────────────────────────────┤
│  120 FPS (ProMotion/High-Hz)│ [ 8.3ms Total Window per Frame ]         │
│                             │   └── Exige Zero-Reflow (Compositor Only)│
└────────────────────────────────────────────────────────────────────────┘
```

### 1.1 O Abismo do "Native Feel" (The Web-to-Native Gap)
A web tradicional frequentemente transmite uma sensação "plástica", rígida e desarticulada quando comparada ao ecossistema nativo do iOS (**CoreAnimation**, **UIKit Dynamics**, **SwiftUI Springs**). Esse abismo sensorial decorre de três falhas estruturais comuns no frontend web:

1. **Uso de Interpolações Temporais Estáticas em vez de Molas Dinâmicas**:
   Curvas bezier tradicionais (`transition: all 0.3s ease-in-out`) possuem duração rígida e velocidade inicial zero ($v_0 = 0$). Na física real, se o usuário arrasta um elemento com velocidade de $1200\text{ px/s}$ e o solta, o elemento deve continuar se movendo com essa velocidade inicial exata até que o amortecedor viscoso e a mola o desacelerem. A quebra de conservação de momento destrói a ilusão de tangibilidade.
2. **Queda de Quadros por Layout Thrashing**:
   Animar propriedades que afetam a geometria da árvore de renderização (`top`, `left`, `width`, `height`, `margin`) força o navegador a recalcular estilos e refazer o layout em cada quadro (*reflow*), estourando o orçamento de $16.6\text{ ms}$ e gerando engasgos (*stutter/jank*). Aplicações de classe 60fps operam exclusivamente na camada do Compositor da GPU via `transform` e `opacity`.
3. **Falta de Resistência Elástica de Limite (Rubber-Banding)**:
   Em sistemas nativos, puxar um elemento além de seu limite físico produz uma resistência não linear proporcional à distância do arraste. Na web comum, o elemento simplesmente para de forma abrupta contra uma parede invisível, gerando atrito cognitivo.

### 1.2 O Ecossistema MCP & Integração com Engenharia de Software
O 60fps.design consolidou-se também como ferramenta de automação de desenvolvimento ao lançar seu servidor oficial de **Model Context Protocol (MCP)** (`https://mcp.60fps.design/mcp`). Esse protocolo permite que ambientes de desenvolvimento assistidos por IA (como Cursor, Claude Code e Grok) realizem buscas semânticas em mais de 2.000 gravações reais de interações móveis por descrição em linguagem natural e traduzam a intenção de movimento diretamente em código reativo compilável para SwiftUI ou React/Motion.dev.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### 2.1 Papel na Regra 60-30-10 de Design de Movimento
O catálogo do 60fps.design ensina a dosar o movimento em camadas funcionais para evitar a saturação sensorial:

```
┌────────────────────────────────────────────────────────────────────────┐
│               THE 60-30-10 HIERARCHY OF INTERACTIVE MOTION             │
├────────────────────────────────────────────────────────────────────────┤
│  60%  A BASE ESTÁVEL (Neutral Foundation)                              │
│       Tipografia estável, layout previsível, grids sem sobressaltos.   │
├────────────────────────────────────────────────────────────────────────┤
│  30%  MOVIMENTO ESTRUTURAL INVISÍVEL (The Invisible Feel)              │
│       Transições de estado com amortecimento crítico (FLIP), drawer    │
│       com snap points, tabs magnéticas sem tremor de renderização.     │
├────────────────────────────────────────────────────────────────────────┤
│  10%  MICROINTERAÇÃO DE ASSINATURA & DELIGHT (The 60fps Signature)     │
│       Choreographed Onboarding, Slide-to-Pay tátil, Ilha Dinâmica      │
│       elástica, Card Fling com inércia balística real.                 │
└────────────────────────────────────────────────────────────────────────┘
```

- **60% da Interface (Base Estável)**: Telas com contraste nítido, hierarquia tipográfica sólida e carregamento assíncrono determinístico onde nenhum elemento salta sem intervenção do usuário.
- **30% da Interface (Movimento Invisível)**: O "feel" nativo que o usuário não nota conscientemente, mas sente falta se ausente. Ocorre quando menus deslizam com amortecimento crítico ($\zeta \approx 1$), abas se adaptam com projeção dimensional instantânea e modais abrem acompanhando a inércia do clique.
- **10% da Interface (O Momento de Assinatura)**: As microinterações memoráveis que viram virais na comunidade técnica e fixam a identidade da marca — como o slider de confirmação de envio de dinheiro do Cash App ou a coreografia de recompensa do Duolingo.

### 2.2 Nichos de Produto de Altíssimo Retorno
1. **Fintechs & Carteiras Digitais (Cash App, Family, Revolut)**:
   Transações financeiras lidam com patrimônio real e geram apreensão no usuário. O feedback tátil, sliders de confirmação com mola firme e números que rolam como odômetros transmitem solidez institucional e transparência mecânica.
2. **Ferramentas Snappy de Alta Performance (Linear, Amie, Things 3, Raycast)**:
   Profissionais de tecnologia navegam por atalhos e toques rápidos. Menus contextuais e painéis que respondem em $<16\text{ ms}$ com física de mola aumentam a produtividade percebida e eliminam o estresse do trabalho diário.
3. **Plataformas de Eventos, Estilo de Vida & Social (Luma, Airbnb, Duolingo)**:
   Fluxos de convite, check-in e celebração de tarefas diárias exigem gamificação e sensação física com curvas subamortecidas que proporcionam micro-recompensas de dopamina.
4. **Onboarding & Aquisição de Novos Usuários**:
   A taxa de conversão no primeiro minuto de uso de um produto mobile/web aumenta drasticamente quando o onboarding apresenta entrada coreografada (*staggered entrance*) de ilustrações e botões, comunicando requinte técnico.

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### 3.1 ⚠️ Quando Evitar Estritamente
- **Tabelas de Dados em Massa e Planilhas Operacionais**:
  Em interfaces administrativas com grades de centenas de células editáveis simultâneas (ex: back-offices logísticos, terminais Bloomberg, painéis contábeis), aplicar física de molas individuais causa gargalo no loop de eventos do JavaScript e atrasa a digitação.
- **Formulários Burocráticos de Alta Frequência**:
  Se o operador precisa preencher 80 cadastros por hora, cada animação que bloqueie o próximo campo de texto por mais de $100\text{ ms}$ é considerada um defeito de usabilidade gravíssimo.
- **Molas Não Canceláveis / Animações de Bloqueio**:
  Nunca impeça o usuário de clicar em "Voltar" ou selecionar outro item enquanto uma transição está em andamento. Toda física de 60fps deve ser **interrompível** (*interruptible*): um novo toque deve assumir o controle do objeto no estado vetorial exato em que ele se encontra.

### 3.2 ⚠️ Anti-Padrões Técnicos que Destroem a Taxa de Quadros
- **Layout Thrashing por Leitura e Escrita Cruzada no DOM**:
  Executar `element.getBoundingClientRect()` ou `element.offsetHeight` dentro de um listener de `touchmove` ou `pointermove` força o motor do navegador a sincronizar o layout síncrono no meio do quadro, derrubando a taxa de 60fps para menos de 20fps.
- **Vazamento de Memória por Camadas de GPU Não Coletadas**:
  Adicionar a propriedade CSS `will-change: transform` indiscriminadamente em centenas de itens de uma lista cria centenas de camadas de textura na VRAM do dispositivo. Em smartphones intermediários, isso aciona o coletor de memória do sistema operacional e encerra o processo do navegador (*OOM Crash*). O uso de `will-change` deve ser temporário (ativado no `pointerdown` e removido no `pointerup`).
- **Conflito de Gestos de Toque no Navegador**:
  Implementar gestos de arrasto horizontais ou verticais na web sem especificar a regra CSS `touch-action: pan-y` ou `touch-action: none` faz com que o navegador dispute o controle do gesto com sua própria rolagem nativa, gerando travamentos imediatos.

### 3.3 ⚠️ Acessibilidade & Gestão de Cinetose
- **Respeito Absoluto a `prefers-reduced-motion`**:
  Usuários com disfunções no sistema vestibular (labirintite, epilepsia fotossensível, cinetose digital) podem sofrer náuseas reais com efeitos de elástico (*rubber-banding*), balanços de ilha dinâmica ou giros tridimensionais de cartões. Nesses cenários, as animações devem ser reconfiguradas para crossfades simples de opacidade ($0 \to 1$) em $100\text{ ms}$, sem deslocamento nos eixos $X$, $Y$ ou $Z$.

---

## 4. Catálogo Detalhado de Componentes & Padrões Nativos

Abaixo estão dissecados os **10 padrões cinemáticos fundamentais** catalogados e reverenciados na biblioteca do 60fps.design:

```
┌────────────────────────────────────────────────────────────────────────┐
│                   60FPS DESIGN CORE PATTERNS SUITE                     │
├────────────────────────────────────────────────────────────────────────┤
│  01. Onboarding Stagger Choreography │ 06. Dynamic Island Pill Morph   │
│  02. Elastic Pull-to-Refresh         │ 07. Springy Tab Bar Bounce      │
│  03. Velocity Bottom Sheet Detents   │ 08. Card Stack Fling & Dismiss  │
│  04. Tactile Slide-to-Pay Lock       │ 09. Segmented Magnetic Pill     │
│  05. Expandable Card to Full Modal   │ 10. Kinetic Odometer Roll       │
└────────────────────────────────────────────────────────────────────────┘
```

### 1. Onboarding Stagger Choreography (Padrão Duolingo / Linear)
- **Comportamento Visual**: Na transição entre telas de apresentação, os elementos não entram em bloco monolítico. A ilustração principal surge com leve escala ($0.85 \to 1.0$) e mola suave; o título entra $60\text{ ms}$ depois; os benefícios secundários entram em cascata sequencial escalonada (*stagger* de $40\text{ ms}$ entre itens); por fim, o botão de chamada para ação (*CTA*) surge com um pulso tátil de atenção.
- **Gatilho Físico**: Mudança de passo de rota ou conclusão de carregamento de recursos.
- **Onde Encaixar**: Telas de boas-vindas, conclusão de cadastro e ativação de planos pagos.

### 2. Elastic Rubber-Band Pull-to-Refresh (Padrão iOS Mail / Airbnb)
- **Comportamento Visual**: O usuário puxa o topo da lista para baixo. O deslocamento do conteúdo não é linear com o dedo: ele segue uma curva logarítmica de resistência elástica ($\Delta y_{\text{visual}} = d \cdot (1 - \frac{1}{\alpha \cdot d + 1})$). Um indicador radial SVG gira proporcionalmente ao deslocamento. Ao ultrapassar o limite de gatilho ($70\text{ px}$), uma leve vibração tátil é acionada. Ao soltar, a lista retorna com mola amortecida para um patamar de $50\text{ px}$ enquanto os novos dados são recebidos. Ao terminar, a lista sobe suavemente de volta a zero.
- **Gatilho Físico**: Gesto de `pointerdown` + `pointermove` vertical com coordenadas no topo do container.
- **Onde Encaixar**: Feeds de notícias, caixas de entrada de e-mail e listagens de transações financeiras.

### 3. Velocity-Driven Bottom Sheet Morphing (Padrão Family / Apple Maps)
- **Comportamento Visual**: Um painel deslizante inferior (*bottom sheet*) que repousa em pontos de parada predefinidos (*detents* de 25%, 50% e 90% da altura da tela). O painel rastreia o dedo do usuário em tempo real. No momento em que o dedo é liberado, o sistema calcula a velocidade instantânea do lançamento ($v_y$). Se a velocidade for alta, o painel salta para o próximo nível mesmo que tenha percorrido apenas 10% da distância. Os cantos arredondados e a opacidade da cortina de fundo (*backdrop*) são interpolados dinamicamente em sincronia com a altura.
- **Gatilho Físico**: Arrasto vertical contínuo com projeção balística no evento de soltura (`onPointerUp`).
- **Onde Encaixar**: Seleção de opções contextuais, visualização rápida de detalhes de produto e filtros de busca.

### 4. Tactile Slide-to-Pay / Hold-to-Confirm Slider (Padrão Cash App / Luma)
- **Comportamento Visual**: Um trilho horizontal com uma maçaneta circular. Conforme o usuário desliza a maçaneta em direção à direita, o fundo preenche-se com um degradê de progresso e o rótulo de instrução dissolve sua opacidade. Caso o usuário solte a maçaneta antes de atingir 90% do percurso, uma mola firme a puxa instantaneamente de volta ao início com um leve ressalto elástico (*bounce-back*). Se atingir os 100%, a maçaneta se expande, os cantos do trilho se fundem em um círculo central e um ícone de verificação (*checkmark*) salta em escala com mola subamortecida.
- **Gatilho Físico**: Arrasto horizontal restrito aos limites da trilha, com bloqueio condicional de liberação.
- **Onde Encaixar**: Confirmação irreversível de transferências PIX/cripto, exclusão de contas e publicação de eventos públicos.

### 5. Dynamic Island Morphing & Pill Notification (Padrão Apple iOS / Fluid Pill)
- **Comportamento Visual**: Uma pequena cápsula flutuante (*pill*) de $120\text{ px} \times 36\text{ px}$ repousa no topo da tela. Quando um evento assíncrono ocorre (ex: download concluído, áudio em reprodução), a pílula expande sua largura e altura para $340\text{ px} \times 84\text{ px}$ por meio de uma mola de alta rigidez e baixo amortecimento, exibindo capa do álbum, ondas sonoras ativas e botões de controle sem causar nenhum reflow no restante da página. Ao terminar, ela encolhe de volta ao tamanho compacto ou dissolve-se em escala.
- **Gatilho Físico**: Eventos de websocket, conclusão de tarefas em segundo plano ou chamadas ativas de áudio.
- **Onde Encaixar**: Notificações globais de sistema (*toasts* modernos), players de podcast minimizados e status de upload de arquivos.

### 6. Springy Tab Bar Icon Bounce & Haptic Squash (Padrão Luma / Instagram)
- **Comportamento Visual**: Ao tocar em um ícone da barra de navegação inferior, o elemento sofre uma deformação elástica instantânea (*squash & stretch*): no instante do toque ele comprime em $Y$ para $0.85$ e expande em $X$ para $1.15$; na liberação, salta verticalmente para cima com mola viva antes de se assentar. Simultaneamente, o traço SVG do ícone desenha um preenchimento interno com transição de máscara e o indicador magnético da barra desliza suavemente até a nova posição com transição FLIP.
- **Gatilho Físico**: Clique/toque direto no item de navegação primária.
- **Onde Encaixar**: Barra de navegação inferior de aplicações móveis e barras laterais de dashboards web modernos.

### 7. Physics-Based Card Stack Swipe & Fling Dismissal (Padrão Family / Linear Task Deck)
- **Comportamento Visual**: Uma pilha de cartões sobrepostos. O cartão superior pode ser arrastado em qualquer direção do plano bidimensional ($X, Y$). Conforme é afastado do centro, ele rotaciona sutilmente com base no deslocamento horizontal ($\text{rotação} = \Delta x \times 0.08^\circ$). Os cartões situados logo abaixo aumentam de escala e sobem na profundidade de forma proporcional ao deslocamento do cartão ativo. Se o cartão for lançado com alta velocidade angular, ele é ejetado para fora da tela com inércia contínua, e o próximo cartão da pilha assume a liderança instantaneamente com mola receptiva.
- **Gatilho Físico**: Arrasto multidirecional livre com cálculo de inércia balística.
- **Onde Encaixar**: Triagem rápida de tarefas em fila de espera, aprovação de despesas e seleção rápida de perfis.

### 8. Segmented Control Magnetic Spring Pill (Padrão iOS Settings / Apple Music)
- **Comportamento Visual**: Uma barra segmentada com múltiplas opções de filtro (ex: "Dia", "Semana", "Mês", "Ano"). O fundo selecionador (uma cápsula branca com leve sombra) desliza de um botão para outro com uma mola rápida e precisa. Durante o deslocamento rápido entre extremos distantes, a cápsula estica levemente no eixo $X$ na direção do movimento (*velocity stretching*) e se contrai ao atingir o alvo final, simulando a fluidez de uma gota líquida magnética.
- **Gatilho Físico**: Clique ou arraste horizontal com o polegar sobre as opções do seletor.
- **Onde Encaixar**: Chaves de visualização de relatórios, alternadores de período e filtros de feed.

### 9. Expandable Card to Full-Screen Modal (Padrão App Store Today / Luma Events)
- **Comportamento Visual**: Um cartão compacto de evento em uma lista se expande até ocupar a tela inteira quando tocado. A imagem de capa, o título e os botões morpham continuamente para suas posições de cabeçalho na tela cheia por meio de projeção geométrica FLIP (*shared element transition*). O texto detalhado adicional surge por fade suave logo abaixo. Ao puxar o cabeçalho para baixo com o polegar, o modal reduz proporcionalmente de escala ($1.0 \to 0.92$) e, ao ser solto, retorna com mola perfeita para o seu lugar exato dentro da lista original.
- **Gatilho Físico**: Clique para expansão e gesto de *pull-down-to-dismiss* para retorno.
- **Onde Encaixar**: Abertura de artigos detalhados, páginas de checkout de eventos e visualização de perfis a partir de grades.

### 10. Kinetic Odometer / Numeric Spring Roll (Padrão Fintech Balance Update)
- **Comportamento Visual**: Quando o saldo financeiro do usuário ou uma métrica de contagem é atualizada, os dígitos numéricos não realizam um corte seco. Cada coluna decimal rola verticalmente de forma independente dentro de uma máscara de corte (*overflow hidden*), acompanhada por molas com amortecimento calibrado. Dígitos mais significativos rolam com ligeiro atraso em relação aos centavos, gerando um efeito de cascata mecânica que expressa precisão matemática e vitalidade orgânica.
- **Gatilho Físico**: Atualização de saldo em tempo real, recebimento de juros ou cálculo dinâmico de carrinho.
- **Onde Encaixar**: Saldos de contas correntes, contadores de engajamento social e placares de jogos.

---

## 5. Matemática do Movimento & Receitas de Código Funcionais

### 5.1 A Física das Molas Reais (Damped Harmonic Oscillator)
No desenvolvimento de software nativo e na biblioteca Motion.dev, a física de uma mola é governada pela equação diferencial clássica:

$$m \frac{d^2 x}{dt^2} + c \frac{dx}{dt} + k x = 0$$

Onde:
- $m$: **Massa** (*mass*) — a inércia do componente. Quanto maior a massa, mais lento o início do movimento e maior o ímpeto final.
- $k$: **Rigidez** (*stiffness*) — a força com que a mola puxa o objeto de volta ao repouso. Valores altos produzem transições extremamente rápidas e secas.
- $c$: **Amortecimento** (*damping*) — o atrito viscoso que consome energia do sistema.
- $\zeta = \frac{c}{2 \sqrt{k m}}$: **Razão de Amortecimento** (*damping ratio*).
  - Se $\zeta < 1$: Sistema **Subamortecido** (*Underdamped*). Ocorre oscilação e ultrapassagem (*overshoot*). Ideal para sensações lúdicas e botões de micro-satisfação.
  - Se $\zeta = 1$: Sistema **Criticamente Amortecido** (*Critically Damped*). O objeto retorna ao repouso no menor tempo possível sem oscilar nem ultrapassar a borda. Ideal para painéis de navegação sérios e modais corporativos.
  - Se $\zeta > 1$: Sistema **Superamortecido** (*Overdamped*). Movimento lento e pesado, sem qualquer ressalto.

```
┌────────────────────────────────────────────────────────────────────────┐
│                   SPRING PROFILES REFERENCE TABLE                      │
├─────────────────────┬───────────┬─────────┬──────┬────────┬────────────┤
│ Perfil de Movimento │ Stiffness │ Damping │ Mass │ Damping│ Aplicação  │
│                     │    (k)    │   (c)   │ (m)  │ Ratio ζ│ Típica     │
├─────────────────────┼───────────┼─────────┼──────┼────────┼────────────┤
│ 1. Snappy Quartz    │    500    │   35    │ 0.8  │ 0.87   │ Tab Bar,   │
│    (Subamortecido)  │           │         │      │        │ Toggles    │
├─────────────────────┼───────────┼─────────┼──────┼────────┼────────────┤
│ 2. Gentle Structural│    320    │   32    │ 1.0  │ 0.89   │ Bottom     │
│    (Suave e Fluido) │           │         │      │        │ Sheets     │
├─────────────────────┼───────────┼─────────┼──────┼────────┼────────────┤
│ 3. Critical Flow    │    400    │   40    │ 1.0  │ 1.00   │ Dropdowns, │
│    (Zero Overshoot) │           │         │      │        │ Modais     │
├─────────────────────┼───────────┼─────────┼──────┼────────┼────────────┤
│ 4. Playful Delight  │    380    │   18    │ 1.0  │ 0.46   │ Badges,    │
│    (Alto Overshoot) │           │         │      │        │ Conquistas │
└─────────────────────┴───────────┴─────────┴──────┴────────┴────────────┘
```

### 5.2 Curvas de Bezier Equivalentes para WAAPI e CSS Puro
Para interações que operam exclusivamente no motor CSS nativo através da Web Animations API (WAAPI):
- **iOS Snappy Exit (Ease-Out-Expo)**: `cubic-bezier(0.16, 1, 0.3, 1)`
- **Native Modal Presentation**: `cubic-bezier(0.32, 0.72, 0, 1)`
- **Dynamic Fluid Deceleration**: `cubic-bezier(0.22, 1, 0.36, 1)`

---

### 5.3 Componentes Prontos para Produção

Abaixo estão três componentes completos, robustos e autocontidos escritos em **React**, **Motion.dev (Framer Motion)** e **Tailwind CSS**, implementando os padrões centrais do 60fps.design com rigor matemático.

#### Componente 1: `TactileSlideToConfirm.tsx` (Slide-to-Pay / Confirmação Tátil com Mola Reativa)

```tsx
import React, { useState, useRef } from "react";
import { motion, useMotionValue, useTransform, useSpring } from "framer-motion";
import { Check, ChevronRight, Lock } from "lucide-react";

interface SlideToConfirmProps {
  label?: string;
  confirmedLabel?: string;
  onConfirm?: () => Promise<void> | void;
  width?: number;
}

export const TactileSlideToConfirm: React.FC<SlideToConfirmProps> = ({
  label = "Deslize para Confirmar",
  confirmedLabel = "Pagamento Realizado",
  onConfirm,
  width = 340,
}) => {
  const [isConfirmed, setIsConfirmed] = useState(false);
  const [isLoading, setIsLoading] = useState(false);
  const trackRef = useRef<HTMLDivElement>(null);

  const knobSize = 56;
  const padding = 4;
  const maxDrag = width - knobSize - padding * 2;

  // Valor bruto do arrasto em X
  const dragX = useMotionValue(0);

  // Mola para suavizar o retorno físico caso solto antes de completar
  const springConfig = { stiffness: 450, damping: 32, mass: 0.8 };
  const smoothX = useSpring(dragX, springConfig);

  // Interpolações de estilo baseadas na posição física da maçaneta
  const progress = useTransform(smoothX, [0, maxDrag], [0, 1]);
  const textOpacity = useTransform(progress, [0, 0.6], [1, 0]);
  const trackBackgroundOpacity = useTransform(progress, [0, 1], [0.15, 0.95]);

  const triggerHaptic = () => {
    if (typeof navigator !== "undefined" && "vibrate" in navigator) {
      navigator.vibrate([15, 30, 20]); // Feedback tátil nativo
    }
  };

  const handleDragEnd = async () => {
    const currentX = dragX.get();
    if (currentX >= maxDrag * 0.9) {
      // Gatilho de sucesso alcançado
      dragX.set(maxDrag);
      setIsLoading(true);
      triggerHaptic();

      try {
        if (onConfirm) await onConfirm();
        setIsConfirmed(true);
      } catch (err) {
        dragX.set(0); // Em caso de erro na transação, retorna com mola
      } finally {
        setIsLoading(false);
      }
    } else {
      // Retorno elástico imediato ao repouso inicial
      dragX.set(0);
    }
  };

  return (
    <div
      ref={trackRef}
      role="button"
      aria-label={isConfirmed ? confirmedLabel : label}
      tabIndex={0}
      style={{ width }}
      className={`relative h-[64px] rounded-full p-1 select-none overflow-hidden transition-colors duration-300 ${
        isConfirmed
          ? "bg-emerald-500 shadow-[0_10px_25px_-5px_rgba(16,185,129,0.4)]"
          : "bg-neutral-900 border border-neutral-800 shadow-inner"
      }`}
    >
      {/* Camada Dinâmica de Preenchimento de Progresso */}
      {!isConfirmed && (
        <motion.div
          style={{ opacity: trackBackgroundOpacity, width: smoothX }}
          className="absolute inset-y-0 left-0 bg-neutral-700/50 rounded-full pointer-events-none"
        />
      )}

      {/* Rótulo de Instrução Central */}
      <div className="absolute inset-0 flex items-center justify-center pointer-events-none">
        {!isConfirmed ? (
          <motion.span
            style={{ opacity: textOpacity }}
            className="text-xs font-semibold tracking-wider uppercase text-neutral-400 pl-8 flex items-center gap-1.5"
          >
            <Lock className="w-3.5 h-3.5 text-neutral-500" />
            {label}
          </motion.span>
        ) : (
          <motion.span
            initial={{ scale: 0.8, opacity: 0 }}
            animate={{ scale: 1, opacity: 1 }}
            transition={{ type: "spring", stiffness: 400, damping: 25 }}
            className="text-sm font-semibold tracking-wide text-white flex items-center gap-2"
          >
            <Check className="w-4 h-4 stroke-[3]" />
            {confirmedLabel}
          </motion.span>
        )}
      </div>

      {/* Maçaneta Deslizante com Rastreamento de Inércia */}
      {!isConfirmed && (
        <motion.div
          drag="x"
          dragConstraints={{ left: 0, right: maxDrag }}
          dragElastic={{ left: 0.05, right: 0.15 }}
          dragMomentum={false}
          onDragEnd={handleDragEnd}
          style={{ x: smoothX }}
          whileTap={{ scale: 0.96 }}
          className="relative z-10 w-[56px] h-[56px] rounded-full bg-white text-neutral-950 flex items-center justify-center shadow-[0_4px_12px_rgba(0,0,0,0.35)] cursor-grab active:cursor-grabbing touch-none"
        >
          {isLoading ? (
            <motion.div
              animate={{ rotate: 360 }}
              transition={{ repeat: Infinity, duration: 0.8, ease: "linear" }}
              className="w-5 h-5 border-2 border-neutral-300 border-t-neutral-900 rounded-full"
            />
          ) : (
            <ChevronRight className="w-6 h-6 stroke-[2.5] text-neutral-900 ml-0.5" />
          )}
        </motion.div>
      )}
    </div>
  );
};
```

---

#### Componente 2: `DynamicIslandNotification.tsx` (Ilha Dinâmica com Expansão Elástica)

```tsx
import React, { useState } from "react";
import { motion, AnimatePresence } from "framer-motion";
import { Bell, CheckCircle2, X } from "lucide-react";

interface NotificationPayload {
  title: string;
  subtitle: string;
  timestamp: string;
}

export const DynamicIslandNotification: React.FC = () => {
  const [isExpanded, setIsExpanded] = useState(false);
  const [notification, setNotification] = useState<NotificationPayload | null>({
    title: "Transferência Recebida",
    subtitle: "+ R$ 1.450,00 de Acervo Criativo",
    timestamp: "Agora",
  });

  if (!notification) return null;

  return (
    <div className="w-full flex justify-center py-6">
      <motion.div
        layout
        onClick={() => setIsExpanded(!isExpanded)}
        transition={{
          type: "spring",
          stiffness: 450,
          damping: 34,
          mass: 0.9,
        }}
        style={{
          borderRadius: isExpanded ? 28 : 24,
        }}
        className={`bg-black text-white shadow-[0_20px_40px_rgba(0,0,0,0.6)] cursor-pointer select-none overflow-hidden border border-neutral-800 ${
          isExpanded
            ? "w-[360px] p-4 flex flex-col gap-3"
            : "w-[190px] h-[44px] px-3.5 py-2 flex items-center justify-between"
        }`}
      >
        <AnimatePresence mode="popLayout" initial={false}>
          {!isExpanded ? (
            // Modo Compacto (Pílula em Repouso)
            <motion.div
              key="compact"
              initial={{ opacity: 0, scale: 0.9 }}
              animate={{ opacity: 1, scale: 1 }}
              exit={{ opacity: 0, scale: 0.9 }}
              transition={{ duration: 0.15 }}
              className="w-full flex items-center justify-between"
            >
              <div className="flex items-center gap-2">
                <span className="w-2.5 h-2.5 rounded-full bg-emerald-400 animate-pulse" />
                <span className="text-xs font-medium tracking-tight text-neutral-300">
                  PIX Recebido
                </span>
              </div>
              <CheckCircle2 className="w-4 h-4 text-emerald-400 stroke-[2.5]" />
            </motion.div>
          ) : (
            // Modo Expandido (Morphing com Detalhes Coreografados)
            <motion.div
              key="expanded"
              initial={{ opacity: 0, y: -4 }}
              animate={{ opacity: 1, y: 0 }}
              exit={{ opacity: 0, y: -4 }}
              transition={{ duration: 0.2, delay: 0.05 }}
              className="flex flex-col gap-3"
            >
              <div className="flex items-center justify-between">
                <div className="flex items-center gap-2">
                  <div className="w-7 h-7 rounded-full bg-emerald-500/20 text-emerald-400 flex items-center justify-center">
                    <Bell className="w-4 h-4 stroke-[2]" />
                  </div>
                  <div>
                    <h4 className="text-xs font-semibold text-white tracking-wide">
                      {notification.title}
                    </h4>
                    <span className="text-[10px] text-neutral-400">
                      {notification.timestamp}
                    </span>
                  </div>
                </div>
                <button
                  onClick={(e) => {
                    e.stopPropagation();
                    setNotification(null);
                  }}
                  className="w-6 h-6 rounded-full hover:bg-neutral-800 flex items-center justify-center text-neutral-400 transition-colors"
                >
                  <X className="w-3.5 h-3.5" />
                </button>
              </div>

              <div className="p-2.5 rounded-xl bg-neutral-900/90 border border-neutral-800 text-xs font-medium text-emerald-400">
                {notification.subtitle}
              </div>
            </motion.div>
          )}
        </AnimatePresence>
      </motion.div>
    </div>
  );
};
```

---

#### Componente 3: `ElasticPullToRefresh.tsx` (Container com Resistência Elástica e Spin Inercial)

```tsx
import React, { useState, useRef } from "react";
import { motion, useMotionValue, useTransform, useSpring } from "framer-motion";
import { RefreshCw } from "lucide-react";

interface PullToRefreshProps {
  onRefresh: () => Promise<void>;
  children: React.ReactNode;
}

export const ElasticPullToRefresh: React.FC<PullToRefreshProps> = ({
  onRefresh,
  children,
}) => {
  const [isRefreshing, setIsRefreshing] = useState(false);
  const containerRef = useRef<HTMLDivElement>(null);

  const rawY = useMotionValue(0);
  const threshold = 72;

  // Curva de resistência logarítmica elástica (Rubber-Banding)
  // Desacelera conforme o usuário puxa mais para baixo
  const elasticY = useTransform(rawY, (latest) => {
    if (latest <= 0) return 0;
    return Math.pow(latest, 0.82) * 2.2;
  });

  const smoothY = useSpring(elasticY, { stiffness: 420, damping: 30 });
  const iconRotate = useTransform(rawY, [0, threshold * 2], [0, 360]);
  const iconOpacity = useTransform(rawY, [10, threshold], [0.2, 1]);

  const handlePointerMove = (e: React.PointerEvent<HTMLDivElement>) => {
    if (isRefreshing || e.buttons !== 1) return;
    if (containerRef.current && containerRef.current.scrollTop === 0) {
      const delta = e.movementY;
      if (delta > 0 || rawY.get() > 0) {
        rawY.set(Math.max(0, rawY.get() + delta));
      }
    }
  };

  const handlePointerUp = async () => {
    if (rawY.get() >= threshold && !isRefreshing) {
      setIsRefreshing(true);
      rawY.set(threshold * 0.85); // Ponto de repouso enquanto carrega

      try {
        await onRefresh();
      } finally {
        setIsRefreshing(false);
        rawY.set(0);
      }
    } else {
      rawY.set(0); // Retorno suave se não atingiu o limite
    }
  };

  return (
    <div
      ref={containerRef}
      onPointerMove={handlePointerMove}
      onPointerUp={handlePointerUp}
      className="relative w-full h-[480px] overflow-y-auto bg-neutral-950 rounded-2xl border border-neutral-800 touch-pan-y"
    >
      {/* Indicador Flutuante Superior com Rotação Inercial */}
      <motion.div
        style={{
          y: smoothY,
          opacity: iconOpacity,
        }}
        className="absolute top-2 inset-x-0 flex justify-center pointer-events-none z-20"
      >
        <div className="w-10 h-10 rounded-full bg-neutral-900 border border-neutral-700 shadow-lg flex items-center justify-center text-neutral-300">
          <motion.div
            style={{ rotate: isRefreshing ? undefined : iconRotate }}
            animate={
              isRefreshing
                ? {
                    rotate: 360,
                    transition: { repeat: Infinity, duration: 0.8, ease: "linear" },
                  }
                : {}
            }
          >
            <RefreshCw className="w-4 h-4 stroke-[2.2]" />
          </motion.div>
        </div>
      </motion.div>

      {/* Conteúdo Deslocado pela Mola */}
      <motion.div style={{ y: smoothY }} className="relative z-10 w-full p-4">
        {children}
      </motion.div>
    </div>
  );
};
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir o plano arquitetural de interface e design tokens no `DESIGN_BLUEPRINT.md`, a inteligência artificial ou engenheiro de frontend deve obedecer às diretrizes estruturadas abaixo:

### 6.1 Matriz de Especificação de Tokens Físicos (Motion Primitives)
Nunca declare animações como valores pontuais dispersos no código (`duration: 0.3s`). Centralize o sistema em uma tabela de tokens canônicos:

```typescript
// tokens/motion.ts
export const MOTION_TOKENS = {
  // Molas Físicas (Spring Physics)
  spring: {
    snappy: { stiffness: 500, damping: 35, mass: 0.8 },      // Tabs, toggles, micro-botões
    gentle: { stiffness: 320, damping: 30, mass: 1.0 },      // Bottom sheets, gavetas
    critical: { stiffness: 400, damping: 40, mass: 1.0 },    // Modais sem ressalto (ζ = 1)
    bouncy: { stiffness: 380, damping: 18, mass: 1.0 },      // Badges, confetes, gamificação
  },
  // Curvas Bezier para WAAPI / CSS Compositor
  bezier: {
    snappyExit: "cubic-bezier(0.16, 1, 0.3, 1)",
    modalPresentation: "cubic-bezier(0.32, 0.72, 0, 1)",
    fluidDecel: "cubic-bezier(0.22, 1, 0.36, 1)",
  },
  // Escalonamento Temporal de Entrada (Stagger)
  stagger: {
    micro: 0.035, // 35ms entre itens em listas compactas
    normal: 0.06,  // 60ms entre seções em onboardings
  },
} as const;
```

### 6.2 Protocolo de Interrupção de Gestos (Interruptibility Contract)
- Todo componente de arrasto (`drag`, `pull`, `swipe`) **deve herdar a velocidade instantânea do ponteiro** no momento da liberação (`velocity inheritance`).
- O usuário pode interromper a transição em voo tocando no elemento novamente antes que a mola chegue ao repouso final.
- O limiar de disparo de ações de sucesso (`threshold`) deve ser calibrado entre **70% e 90%** da distância máxima, acompanhado de feedback tátil imperceptível ao olhar mas nítido ao toque.

### 6.3 Checklist de Auditoria de Performance (60fps/120fps Profiling)
Antes de homologar qualquer tela inspirada no 60fps.design, valide os seguintes pontos no **Chrome DevTools Performance**:

1. **Zero Layout Thrashing**: Nenhuma barra vermelha de *Forced Reflow* durante interações de arrasto contínuo.
2. **Propriedades Animadas Estritamente Restritas à GPU**: Verificação de que apenas `transform` e `opacity` sofrem mutação no loop de renderização.
3. **Budget de 16.6ms / 8.3ms**: Nenhum frame demorando mais do que a cota do monitor no histograma de quadros.
4. **Isolamento de Toque**: Presença da regra `touch-action: pan-y` ou `touch-action: none` em todos os nós com manipuladores de gestos.
5. **Fallback de Acessibilidade**: Testar o comportamento da interface alternando a flag de sistema `prefers-reduced-motion: reduce`. Os deslocamentos devem ser convertidos em crossfades instantâneos de opacidade.
