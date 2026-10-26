---
id: "smoothui-dev"
name: "SmoothUI"
url: "https://smoothui.dev/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Apple/iOS Spatial Motion", "Fluid Micro-Interactions", "AI-Native Conversational UI", "Minimalist Clean Precision", "Shadcn Registry Architecture"]
densidade_informacao: "Flexivel"
impacto_visual: "Moderado a Alto/Showstopper"
custo_computacional: "Medio (Motion/React Layout Projections & Spring Physics)"
stack_frameworks: ["React 19 / React 18", "Next.js (App Router)", "Motion (anteriormente Framer Motion)", "Tailwind CSS (v3 / v4)", "shadcn/ui", "TypeScript", "Lucide React"]
compatibilidade:
  fontes_ideais: ["SF Pro Display", "Geist Sans", "Inter", "Plus Jakarta Sans", "JetBrains Mono"]
  paletas_ideais: ["Deep Neutral Zinc (Zinc 950 / Zinc 50)", "High-Contrast Monochrome", "Apple Glassmorphism (white/10, black/40)", "Subtle Oklab Brand Accents"]
  combinacoes_recomendadas: ["shadcn/ui", "Radix UI Primitives", "Motion Primitives", "Cult UI", "Lucide React", "Number Flow"]
  conflitos_esteticos: ["Brutalismo cru sem suavização de curvas", "Neumorfismo plástico eskeumórfico pesado", "Transições duras em CSS linear sem spring", "Bordas duras sem squircle ou cantos arredondados contínuos"]
---

# SmoothUI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo engenheiro de software e designer espanhol **Eduardo Calvo** (`@educalvolpz` / `educlopez`), o **SmoothUI** (`smoothui.dev`) nasceu para sanar a maior lacuna da interface web contemporânea: **a falta de continuidade física e refinamento gestual no ecossistema de componentes React**.

Enquanto bibliotecas tradicionais tratam componentes como blocos rígidos que saltam ou surgem abruptamente na tela com fades e transições lineares genéricas, o SmoothUI introduz a **linguagem de movimento contínuo inspirada no ecossistema Apple (iOS, iPadOS e macOS)** combinada ao estado da arte em **componentes de inteligência artificial generativa (AI-Native UI)**.

Com mais de 180 componentes atômicos e 34 blocos de página completos, o SmoothUI opera sob o padrão de distribuição do **shadcn/ui registry** (`npx shadcn@latest add https://smoothui.dev/r/[component].json`), garantindo autonomia total de código-fonte, tipagem estrita com TypeScript e integração direta com o Tailwind CSS (v3 e v4).

### Os Pilares da Assinatura Visual do SmoothUI:

1. **Continuidade de Superfície & Metamorfose de Layout (`layoutId` e Morphs)**:
   A sensação visual do SmoothUI simula materiais elásticos de alta precisão. Menus, pílulas de navegação, caixas de diálogo e toolbars não são destruídos e recriados; eles se expandem, recolhem e alteram seu raio de curvatura (`border-radius` dinâmico ou squircle contínuo) através de projeções de layout aceleradas por hardware via Motion. O componente *Dynamic Island* personifica esse princípio: uma pílula compacta de clima no topo da tela expande-se organicamente para um player musical ou notificação de chamada sem cortes secos ou saltos na malha do DOM.

2. **Física de Molas Paramétrica com Amortecimento Crítico (`Custom Spring Physics`)**:
   Ao contrário de bibliotecas com rebotes cartunescos exagerados, o SmoothUI adota calibrações de mola baseadas na inércia tátil do iOS. Cada transição de estado recebe um coeficiente de ressalto específico (`BOUNCE_VARIANTS` variando de `0.1` a `0.5`, `stiffness: 300`, `damping: 30`). O movimento transmite substância, peso e tração mecânica sem comprometer o *Time-to-Interactive* (mantendo a resposta perceptiva abaixo de 250ms).

3. **Design de Estados Funcionais para Agentes e LLMs (AI-Native Scaffolding)**:
   O SmoothUI é pioneiro em estabelecer uma gramática visual completa para interfaces com modelos de linguagem. Componentes como *AI Reasoning*, *AI Approval*, *AI Context Meter*, *AI Diff* e *AI Tool Call* tratam o processo de inferência como um elemento de UI vivo:
   - O efeito luminoso (*shimmer sweep*) em gradiente Oklab só está ativo enquanto o modelo está em streaming; assim que o raciocínio encerra, o brilho cessa e o componente colapsa suavemente após um intervalo calculado (`600ms`), evitando que o conteúdo pareça ter sido arrancado à força do usuário.
   - Em aprovações *Human-in-the-Loop* (*AI Approval*), a opção selecionada expande-se para ocupar o espaço total do card enquanto as alternativas colapsam e desaparecem em escala reduzida.

4. **Progressive Blur Óptico Multicamadas**:
   Para evitar as bordas duras e artefatos de renderização típicos do `backdrop-filter: blur()`, o SmoothUI empilha de 5 a 6 fatias consecutivas de desfoque fracionado (`1px`, `2px`, `3px`, `6px`, `12px`) com máscaras de gradiente vetoriais (`mask-image: linear-gradient(...)`). O resultado óptico é idêntico ao vidro fosco do visionOS e do iOS Control Center.

5. **Acessibilidade Universal & Respeito a `prefers-reduced-motion`**:
   Cada componente SmoothUI consome nativamente o hook `useReducedMotion()`. Usuários com restrições vestibulares ou preferências de acessibilidade ativadas recebem instantaneamente transições instantâneas (`duration: 0`) ou cross-fades lineares suaves, eliminando desorientação espacial sem quebrar a lógica de renderização.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários

1. **Aplicações de Inteligência Artificial Generativa & Plataformas de Agentes (AI Copilots)**:
   Ferramentas conversacionais, assistentes de código, estúdios de geração de imagem e sistemas autônomos que demandam visualização de fluxo de raciocínio (*AI Reasoning*), medidores circulares de janela de contexto (*AI Context Meter*), aprovação de ações com impacto (*AI Approval*) e compositores com transição de botão de envio para parada (*AI Prompt Input*).
2. **Produtos SaaS B2B Premium & DevTools (Linear, Raycast, Vercel Style)**:
   Painéis de controle onde a velocidade perceptiva e a qualidade de acabamento são diferenciais de mercado. Utilização de *Dynamic Island* para notificações de background, *Float Input* para formulários compactos e responsivos, e *Number Flow / Digit Roll* para contadores de receita e consumo de tokens.
3. **Aplicações Mobile-First & PWAs Inspiradas no iOS**:
   Projetos que buscam reproduzir a sensação nativa dos sistemas operacionais da Apple na web: pilhas de cartões estilo *Apple Invites*, carrosséis *Coverflow*, seletores de tempo (*Duration Picker*) e controles de exposição fotográfica (*Exposure Slider*).
4. **Landing Pages de Alto Padrão & Portfólios de Design Engineers**:
   Apresentações corporativas e sites de lançamento de software que necessitam de interações memoráveis de abertura (*Page Preloader*), efeitos de texto tipográfico (*Depth Parallax Words*, *Gravity Letters*) e orbs reativos a áudio (*Siri Orb*).

### Papel no Ritmo Visual (Regra 60-30-10)

- **60% — Fundação Neutra e Estrutural (Tokens Shadcn Padrão)**:
  Superfícies limpas, fundos monocromáticos (`bg-background` / `bg-card`), tipografia sem serifa geométrica (`Geist Sans` ou `Inter`), bordas ultra-finas com baixa opacidade (`border-border` / `ring-foreground/10`) e espaçamentos padronizados do Tailwind.
- **30% — Camada de Fluidez e Feedback Tátil (SmoothUI Operacional)**:
  - *Float Input*: Inputs com elevação de label matematicamente interpolada em curvas cubic-bezier (`[0.4, 0, 0.2, 1]`).
  - *Animated Tabs & Tags*: Pílulas com seleção magnética e deslocamento contínuo de background.
  - *AI Reasoning & Tool Call*: Caixas expansíveis que revelam logs técnicos e traces de pensamento sob demanda sem saltar na página.
  - *Rich Popover & Disclosure*: Menus flutuantes que recalculam altura e largura com amortecimento crítico.
- **10% — Efeitos Protagonistas / Showstoppers (Micro-Momentos Memoráveis)**:
  - *Dynamic Island*: Elemento flutuante de status central que altera morfologia para chamadas ativas, players e timers.
  - *Apple Invites*: Apresentação tridimensional de convites e eventos com rotações assimétricas (`-12deg` / `12deg`) e desfoque progressivo.
  - *Siri Orb*: Esfera tridimensional luminescente que reage ao microfone do usuário ou a tokens gerados pelo assistente.
  - *Shader Reveal Luma Transition*: Trocas de rotas e seções via shaders GLSL baseados em mapas de luminância e ruído 4D.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Tabelas de Dados Densas de Alta Frequência (ERPs Industriais & Terminais de Cripto/Trading)**:
  Em grids com centenas de linhas atualizadas a dezenas de vezes por segundo via WebSocket, aplicar molas e morfos de layout (`layoutId`) causará gargalos drásticos de reflow no navegador e descarte severo de frames (*frame drop*). Nestas instâncias, prefira tabelas virtualizadas estáticas com CSS puro.
- **Ambientes Governamentais ou Utilitários Estritamente Burocráticos**:
  Formulários fiscais, sistemas de folha de pagamento ou portais públicos onde a estética de smartphone ou movimentos lúdicos geram fricção cognitiva ou passam sensação de frivolidade comercial.
- **Sistemas com Restrição Severa de Bundle Size ou Ambientes sem JS**:
  O SmoothUI depende ativamente do motor `motion` e de execução no client (`'use client'`). Ambientes estáticos servidos via Server Components puros sem hidratação não conseguirão executar os springs e listeners de viewport.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **Sobrecarga de Orbs e Morfos na Mesma Viewport**:
  Instanciar um *Siri Orb* animado no Hero, um *Dynamic Island* flutuante no topo e múltiplos *Apple Invites* em rotação simultânea cria poluição visual extrema e competição por atenção periférica. Mantenha no máximo **um showstopper ativo por tela**.
- **Permanência de Shimmers e Loaders Decorativos**:
  Um anti-padrão comum é manter componentes como *AI Reasoning* com animação de shimmer constante mesmo após o término da resposta. No SmoothUI, animações de brilho comunicam estritamente processamento em tempo real; mantê-las em repouso destrói seu valor semântico.
- **Ignorar Focus Management em Layouts Expansíveis**:
  Ao expandir um card de *AI Approval* ou *Expandable Cards*, garantir que o teclado capture o foco adequadamente e permita fechamento com a tecla `Escape`.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão 12 dos componentes e primitivas mais expressivos do ecossistema SmoothUI:

### 1. Dynamic Island (`dynamic-island`)
- **Anatomia Visual**: Pílula negra flutuante centralizada com raio de curvatura contínuo (`border-radius: 32px` ou squircle). Em estado de repouso (*idle*), exibe ícone climático e temperatura que se expande ao hover. Ao transitar para eventos ativos (*ring*, *timer*, *notification*, *music*), o container redimensiona sua largura e altura com física de mola calibrada especificamente para o par de estados de origem e destino, enquanto o conteúdo interno dissolve com desfoque fracionado (`blur(5px) -> blur(0px)`).
- **Gatilho de Interação**: Disparado por eventos de background, cliques em botões de ação ou hover com expansão contextual.
- **Onde encaixar na página**: Barra superior central, navbar flutuante ou como HUD de status em dashboards de produtividade.

### 2. AI Reasoning (`ai-reasoning`)
- **Anatomia Visual**: Linha colapsável com chevron rotativo (`0deg` a `90deg`), badge de contagem temporal (`Thought for 2.4s`) e texto de status com gradiente dinâmico Oklab. O shimmer corre em keyframes contínuos de 1.8s apenas durante o processamento. Ao encerrar, o container expande ou retrai um painel indentado com borda lateral esquerda discreta (`border-l border-border`) contendo a cadeia de pensamento completa (*chain-of-thought*).
- **Gatilho de Interação**: Ativação automática ao iniciar streaming do modelo LLM; clique manual do usuário para alternar estado expandido/fechado com trava de controle manual.
- **Onde encaixar na página**: Imediatamente acima da mensagem de resposta do assistente em interfaces de chat ou consoles de IA.

### 3. Apple Invites (`apple-invites`)
- **Anatomia Visual**: Três cartões em perspectiva tridimensional dispostos em camadas espaciais. O cartão central repousa plano (`scale: 1, rotate: 0, zIndex: 3`), enquanto os cartões periféricos exibem rotações de `-12deg` e `12deg` com deslocamento horizontal e escala reduzida (`scale: 0.9, opacity: 0.8`). A parte inferior de cada cartão incorpora um desfoque progressivo (*progressive blur*) de 5 camadas sobreposto a avatares dos convidados e títulos em tipografia limpa.
- **Gatilho de Interação**: Auto-play contínuo com ciclo de temporizador configurável (`interval: 3000ms`), navegação por swipe/arraste ou paginação manual.
- **Onde encaixar na página**: Hero sections de eventos, seções de prova social, carrossel de recursos em landing pages B2C.

### 4. Siri Orb (`siri-orb`)
- **Anatomia Visual**: Esfera luminescente multifacetada inspirada na identidade do assistente da Apple. Combina gradientes radiais complexos, difusão com desfoque gaussiano de alta saturação e deformação de malha vetorial contínua. Suporta estados visuais distintos: *idle* (pulso suave e lento), *listening* (ondas de escala atreladas à entrada de volume de voz) e *thinking* (rotação cromática rápida).
- **Gatilho de Interação**: Estados reativos a áudio do usuário (via Web Audio API) ou chamadas de função de assistentes virtuais.
- **Onde encaixar na página**: Hero central de assistentes de voz, interfaces de interação hands-free, modal de entrada de comando por voz.

### 5. AI Prompt Input (`ai-prompt-input`)
- **Anatomia Visual**: Barra de composição ergonômica com textarea de expansão vertical automática baseada em quebras de linha (`min-h-[44px]` a `max-h-[200px]`), chips de anexos com botão de remoção e botão de submissão com morph vetorial: a seta ascendente de envio se transforma em um quadrado de parada (*stop generation*) sem recriar o elemento no DOM.
- **Gatilho de Interação**: Digitação, cola de código/imagens por arrasto, pressionamento de `Enter` ou `Shift+Enter`.
- **Onde encaixar na página**: Rodapé fixo de janelas de conversação, barra de prompt central em workspaces generativos.

### 6. AI Approval (`ai-approval`)
- **Anatomia Visual**: Cartão de aprovação humana no fluxo (*Human-in-the-Loop*). Apresenta a ação proposta pelo agente (ex: deletar banco, enviar e-mail em massa ou executar transação). Ao selecionar uma das alternativas (Confirmar / Ajustar / Rejeitar), o botão escolhido expande-se para preencher toda a largura do cartão com spring suave, enquanto as outras opções encolhem e desvanecem.
- **Gatilho de Interação**: Clique do operador em uma das ações primárias ou atalho de teclado (`Y/N`).
- **Onde encaixar na página**: Feeds de agentes autônomos, consoles de execução de pipelines e modais de governança corporativa.

### 7. AI Context Meter (`ai-context-meter`)
- **Anatomia Visual**: Indicador circular compacto de consumo de contexto de tokens. O anel preenche progressivamente seu perímetro com cálculo SVG (`strokeDasharray` e `strokeDashoffset`). Ao ultrapassar 75% da capacidade máxima, o gradiente sofre uma transição suave de cor do tom primário neutro para âmbar, e acima de 90% para vermelho de alerta, sem alterar o tamanho ou layout externo do componente.
- **Gatilho de Interação**: Atualizações reativas conforme o histórico de mensagens acumula tokens.
- **Onde encaixar na página**: Barra de cabeçalho ou rodapé do chat ao lado das configurações de temperatura e modelo.

### 8. Expandable Cards (`expandable-cards`)
- **Anatomia Visual**: Grade de cartões de projeto ou produto que, ao serem selecionados, transformam-se num modal centralizado em tela cheia usando a propriedade `layoutId` do Motion. Título, imagem de capa, badge e descrição textual mantém sincronia espacial perfeita durante o morph, enquanto o restante do fundo desfoca gradualmente com um backdrop opaco.
- **Gatilho de Interação**: Clique no cartão ou navegação por setas com `Enter`.
- **Onde encaixar na página**: Vitrines de portfólio, catálogos de e-commerce, seções de cases de sucesso e galerias de templates.

### 9. Float Input (`float-input`)
- **Anatomia Visual**: Campo de entrada moderno com label flutuante inserida no fluxo. Quando vazio e sem foco, o label atua como placeholder interno; ao receber foco ou conter valor, ele transiciona verticalmente (`y: -24px`), reduz sua escala para `0.85`, e adota a cor primária da marca com uma curva cúbica ultra-suave (`cubic-bezier(0.4, 0, 0.2, 1)`), mantendo bordas perfeitamente alinhadas com o outline do container.
- **Gatilho de Interação**: Foco do teclado (`focusin`), digitação ou desfoque (`blur`).
- **Onde encaixar na página**: Formulários de cadastro, modais de autenticação, telas de checkout e configurações de perfil.

### 10. Wallet Card (`wallet-card`)
- **Anatomia Visual**: Pilha vertical de cartões digitais compactos sobrepostos (estilo Apple Wallet). Em repouso, apenas o topo de cada cartão é visível com seu nome e saldo. Ao passar o mouse ou focar com teclado, a pilha expande-se verticalmente exibindo as informações completas de cada cartão com transições de mola escalonadas.
- **Gatilho de Interação**: Hover ou clique no stack de cartões.
- **Onde encaixar na página**: Dashboards financeiros, carteiras de cartões de crédito em checkouts, visualizadores de planos de assinatura.

### 11. Number Flow / Digit Roll (`number-flow` / `digit-roll`)
- **Anatomia Visual**: Contador numérico odometer de alta fidelidade onde cada algarismo é renderizado em uma coluna vertical independente. Ao alterar o valor (ex: saldo, contagem de usuários ou preço), os dígitos individuais rolam para cima ou para baixo com amortecimento físico e interpolação de largura proporcional para caracteres numéricos tabulares (`font-variant-numeric: tabular-nums`).
- **Gatilho de Interação**: Mudança reativa no estado numérico via props ou scrub manual arrastando horizontalmente com o ponteiro.
- **Onde encaixar na página**: Tabelas de preços (*pricing toggles* anual/mensal), painéis de métricas de SaaS, contadores de estatísticas no Hero.

### 12. Rich Popover (`rich-popover`)
- **Anatomia Visual**: Popover contextual com redimensionamento fluido de altura e largura dependendo da aba ativa ou da etapa interna (ex: menu de perfil que alterna para sub-menu de configurações). O container recalcula sua geometria de contorno sem descontinuidades e projeta uma sombra difusa de nível óptico.
- **Gatilho de Interação**: Clique em gatilhos flutuantes ou ações em tabelas de dados.
- **Onde encaixar na página**: Menus de usuário em navbars, seletores de filtros compostos em dashboards, menus de contexto em botões de ação secundária.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

O ecossistema SmoothUI utiliza como dependência fundamental a versão mais moderna do pacote **Motion** (anteriormente Framer Motion, referenciado como `motion` ou `motion/react`) integrado ao ecossistema Shadcn.

Para adicionar suporte em um projeto React / Next.js com Tailwind CSS:

```bash
# Instalação das dependências centrais
npm install motion lucide-react popmotion clsx tailwind-merge

# Instalação de componentes SmoothUI via CLI oficial do Shadcn
npx shadcn@latest add https://smoothui.dev/r/dynamic-island.json
npx shadcn@latest add https://smoothui.dev/r/ai-reasoning.json
npx shadcn@latest add https://smoothui.dev/r/float-input.json
npx shadcn@latest add https://smoothui.dev/r/apple-invites.json

# Ou usando a CLI nativa do ecossistema SmoothUI
npx smoothui-cli add dynamic-island
```

### Física de Movimento, Parâmetros de Mola & Curvas de Interpolação

O segredo da fluidez visual do SmoothUI repousa no uso rigoroso de parâmetros físicos específicos para cada tipo de transição:

1. **Molas com Bounce Controlado por Matriz de Estados (`Dynamic Island Springs`)**:
   ```typescript
   const BOUNCE_VARIANTS = {
     idle: 0.5,
     "idle-ring": 0.5,
     "idle-timer": 0.3,
     "ring-idle": 0.5,
     "ring-timer": 0.35,
     "timer-idle": 0.3,
     "timer-ring": 0.35,
   } as const;

   const SPRING_TRANSITION = {
     type: "spring",
     bounce: BOUNCE_VARIANTS[currentVariant] ?? 0.4,
     duration: 0.25,
   };
   ```

2. **Molas para Cartões Espaciais 3D (`Apple Invites Stack`)**:
   ```typescript
   const CARD_SPRING = {
     type: "spring",
     stiffness: 300,
     damping: 30,
     duration: 0.25,
   };
   ```

3. **Molas Atômicas Padrão para Elementos de Interface (`General UI Spring`)**:
   ```typescript
   const SPRING_DEFAULT = {
     type: "spring",
     bounce: 0.1,
     duration: 0.25,
   };
   ```

4. **Curvas Cubic-Bezier para Inputs e Rótulos Flutuantes**:
   ```typescript
   // Suavização ultra-calibrada para deslocamento de labels e micro-fades
   const EASE_IN_OUT_CUBIC = [0.4, 0, 0.2, 1] as const;
   const EASE_OUT_EXPO = [0.23, 1, 0.32, 1] as const;
   ```

5. **Camadas de Progressive Blur via Tailwind & CSS puro**:
   ```html
   <div className="fixed inset-x-0 bottom-0 isolate z-10 h-1/2 pointer-events-none">
     <div className="gradient-mask-t-0 absolute inset-0 overflow-hidden backdrop-blur-[1px]" />
     <div className="gradient-mask-t-0 absolute inset-0 overflow-hidden backdrop-blur-[2px]" />
     <div className="gradient-mask-t-0 absolute inset-0 overflow-hidden backdrop-blur-[3px]" />
     <div className="gradient-mask-t-0 absolute inset-0 overflow-hidden backdrop-blur-[6px]" />
     <div className="gradient-mask-t-0 absolute inset-0 overflow-hidden backdrop-blur-[12px]" />
   </div>
   ```

---

### Receita de Código Funcional: Componente `DynamicIsland` Completo

Abaixo está a implementação de alta fidelidade do componente **Dynamic Island**, demonstrando a projeção de layout em mola, controle de estados, animações com desfoque e suporte estrito a `useReducedMotion`:

```tsx
"use client";

import React, { useState, useMemo } from "react";
import { motion, AnimatePresence, useReducedMotion } from "motion/react";
import { 
  CloudLightning, 
  Phone, 
  Timer as TimerIcon, 
  Bell, 
  Music2, 
  Play, 
  Pause, 
  SkipBack, 
  SkipForward, 
  Thermometer 
} from "lucide-react";

export type IslandView = "idle" | "ring" | "timer" | "notification" | "music";

const BOUNCE_VARIANTS: Record<string, number> = {
  idle: 0.5,
  "idle-ring": 0.5,
  "idle-timer": 0.3,
  "ring-idle": 0.5,
  "ring-timer": 0.35,
  "timer-idle": 0.3,
  "timer-ring": 0.35,
};

const DEFAULT_BOUNCE = 0.45;

export interface DynamicIslandProps {
  className?: string;
  defaultView?: IslandView;
}

export function DynamicIsland({
  className = "",
  defaultView = "idle",
}: DynamicIslandProps) {
  const [view, setView] = useState<IslandView>(defaultView);
  const [variantKey, setVariantKey] = useState<string>("idle");
  const shouldReduceMotion = useReducedMotion();

  const handleViewChange = (newView: IslandView) => {
    if (view === newView) return;
    setVariantKey(`${view}-${newView}`);
    setView(newView);
  };

  const renderContent = () => {
    switch (view) {
      case "ring":
        return (
          <div className="flex w-64 items-center gap-3 px-4 py-2 text-white">
            <Phone className="h-5 w-5 text-emerald-400 animate-bounce" />
            <div className="flex-1 min-w-0">
              <p className="font-medium text-xs text-white truncate">Chamada Recebida</p>
              <p className="text-[11px] text-white/70 truncate">Guillermo Rauch</p>
            </div>
            <div className="h-2 w-2 rounded-full bg-emerald-400 animate-ping" />
          </div>
        );
      case "timer":
        return (
          <div className="flex w-64 items-center gap-3 px-4 py-2 text-white">
            <TimerIcon className="h-5 w-5 text-amber-400" />
            <div className="flex-1">
              <p className="font-medium text-xs text-white">Timer de Foco</p>
              <p className="text-[11px] text-white/70">14:59 restantes</p>
            </div>
            <div className="h-1.5 w-16 overflow-hidden rounded-full bg-white/20">
              <div className="h-full bg-amber-400 w-3/4 rounded-full" />
            </div>
          </div>
        );
      case "notification":
        return (
          <div className="flex w-64 items-center gap-3 px-4 py-2 text-white">
            <Bell className="h-5 w-5 text-sky-400" />
            <div className="flex-1 min-w-0">
              <p className="font-medium text-xs text-white truncate">Agente Autônomo</p>
              <p className="text-[11px] text-white/70 truncate">Tarefa #108 concluída com sucesso</p>
            </div>
            <span className="rounded-full bg-sky-400/20 px-2 py-0.5 text-[10px] text-sky-300">
              1 novo
            </span>
          </div>
        );
      case "music":
        return (
          <div className="flex w-72 items-center gap-3 px-4 py-2 text-white">
            <Music2 className="h-5 w-5 text-pink-400" />
            <div className="min-w-0 flex-1">
              <p className="truncate font-medium text-xs text-white">Midnight City</p>
              <p className="truncate text-[11px] text-white/70">M83 — Hurry Up, We're Dreaming</p>
            </div>
            <div className="flex items-center gap-1">
              <button type="button" className="rounded-full p-1 hover:bg-white/10 transition-colors">
                <SkipBack className="h-3.5 w-3.5 text-white" />
              </button>
              <button type="button" className="rounded-full p-1 hover:bg-white/10 transition-colors">
                <Pause className="h-3.5 w-3.5 text-white" />
              </button>
              <button type="button" className="rounded-full p-1 hover:bg-white/10 transition-colors">
                <SkipForward className="h-3.5 w-3.5 text-white" />
              </button>
            </div>
          </div>
        );
      default:
        return (
          <div className="flex items-center gap-2 px-3.5 py-1.5 text-white">
            <CloudLightning className="h-4 w-4 text-amber-300" />
            <span className="text-xs font-medium tracking-tight">21°C Ensolarado</span>
          </div>
        );
    }
  };

  return (
    <div className={`flex flex-col items-center justify-center p-6 ${className}`}>
      {/* Dynamic Island Capsule */}
      <motion.div
        layout
        className="mx-auto w-fit min-w-[120px] overflow-hidden rounded-full bg-zinc-950 shadow-2xl ring-1 ring-white/10"
        style={{ borderRadius: 32 }}
        transition={
          shouldReduceMotion
            ? { duration: 0 }
            : {
                type: "spring",
                bounce: BOUNCE_VARIANTS[variantKey] ?? DEFAULT_BOUNCE,
                duration: 0.28,
              }
        }
      >
        <motion.div
          key={view}
          initial={
            shouldReduceMotion
              ? { opacity: 0 }
              : { opacity: 0, scale: 0.92, filter: "blur(6px)" }
          }
          animate={{ opacity: 1, scale: 1, filter: "blur(0px)" }}
          transition={{
            type: "spring",
            bounce: BOUNCE_VARIANTS[variantKey] ?? DEFAULT_BOUNCE,
          }}
        >
          {renderContent()}
        </motion.div>
      </motion.div>

      {/* Control Switcher Hub */}
      <div className="mt-8 flex items-center gap-1.5 rounded-full border border-zinc-200 dark:border-zinc-800 bg-white/80 dark:bg-zinc-900/80 p-1.5 backdrop-blur-md shadow-sm">
        {[
          { key: "idle", label: "Clima", icon: <CloudLightning className="size-3.5" /> },
          { key: "ring", label: "Chamada", icon: <Phone className="size-3.5" /> },
          { key: "timer", label: "Timer", icon: <TimerIcon className="size-3.5" /> },
          { key: "notification", label: "Alerta", icon: <Bell className="size-3.5" /> },
          { key: "music", label: "Música", icon: <Music2 className="size-3.5" /> },
        ].map(({ key, label, icon }) => (
          <button
            key={key}
            type="button"
            aria-label={label}
            onClick={() => handleViewChange(key as IslandView)}
            className={`flex items-center gap-1.5 px-3 py-1.5 rounded-full text-xs font-medium transition-all ${
              view === key
                ? "bg-zinc-950 text-white dark:bg-white dark:text-zinc-950 shadow-sm"
                : "text-zinc-600 dark:text-zinc-400 hover:text-zinc-950 dark:hover:text-white"
            }`}
          >
            {icon}
            <span className="hidden sm:inline">{label}</span>
          </button>
        ))}
      </div>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao especificar o **SmoothUI** na arquitetura de um novo projeto no arquivo `DESIGN_BLUEPRINT.md`, a IA deve seguir as seguintes diretrizes estritas:

1. **Declaração no Tech Stack**:
   - Registrar no inventário de dependências: `motion` (ou `motion/react`), `lucide-react`, `popmotion`, `clsx`, `tailwind-merge`.
   - Adicionar o registro oficial: `https://smoothui.dev/r` compatível com a CLI do Shadcn.

2. **Atribuição de Papéis na Regra 60-30-10**:
   - **Estrutural (60%)**: Use componentes padrão shadcn/ui estilizados com Tailwind CSS e tokens neutros de tema.
   - **Fluidez (30%)**: Prescreva SmoothUI para inputs táteis (`FloatInput`), abas animadas (`AnimatedTabs`, `AnimatedTags`), feedback de processamento de IA (`AIReasoning`, `AIToolCall`) e diálogos contextuais (`RichPopover`).
   - **Showstopper (10%)**: Escolha **exatamente um** elemento protagonista de alto impacto por fluxo visual (ex: `DynamicIsland` no topo ou `AppleInvites` na seção de destaque do produto). Proíba expressamente a concorrência de múltiplos orbs e morfos na mesma tela.

3. **Diretriz de Acessibilidade & Motion Guardrails**:
   - É obrigatório encapsular ou respeitar `useReducedMotion()`.
   - Garantir que animações de carregamento (*shimmer*, *skeleton*) possuam gatilhos semânticos claros e cessem automaticamente quando a resposta ou dados chegarem, respeitando os atrasos de auto-colapso (`600ms`).

4. **Tratamento de Performance**:
   - Não utilizar morfos de layout do SmoothUI em listas virtualizadas com mais de 50 itens simultâneos visíveis.
   - Preservar o isolamento de renderização através de wrappers `'use client'` nas folhas da árvore de componentes, mantendo as páginas principais como Server Components otimizados para SEO e Core Web Vitals.
