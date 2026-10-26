---
id: "cult-ui"
name: "Cult UI"
url: "https://www.cult-ui.com/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Dark Craft & Neumorphic Tactility", "Fluid Morphing & Spring Physics", "Generative & AI-Native UI", "Micro-Layered Borders & Glassmorphism"]
densidade_informacao: "Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Framer Motion/JS) a Alto (Canvas/Shaders)"
stack_frameworks: ["React", "Next.js 15", "Tailwind CSS (v3 & v4)", "Motion (Framer Motion)", "Radix UI", "Vaul"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Geist Mono", "Geist Pixel", "Inter", "Plus Jakarta Sans"]
  paletas_ideais: ["Deep Neutral Stone/Zinc (Stone 950 / Zinc 950)", "Subtle Skeuomorphic Monochrome", "Cyan & Electric Violet AI Accents"]
  combinacoes_recomendadas: ["Shadcn UI", "21st.dev", "Magic UI", "Aceternity UI", "Vaul"]
  conflitos_esteticos: ["Flat Retro Brutalism sem easing", "Corporate Memphis hiper-saturado", "Material Design 2 com sombras primárias duras"]
---

# Cult UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo engenheiro de design **Jordan Gilliam** (sob a bandeira do coletivo **NewCult / Nolly Studio**), o **Cult UI** (`cult-ui.com`) é uma das referências mais cultuadas da engenharia de design frontend contemporânea. A biblioteca transcende os kits de interface utilitários tradicionais ao focar obsessivamente em **micro-interações de altíssima fidelidade tátil**, **transições de estado com física orgânica** e **componentes especializados para aplicações de Inteligência Artificial**.

A assinatura visual do Cult UI é definida por quatro pilares arquiteturais e estéticos:

1. **Neumorfismo Tátil em Camadas (Layered Step-Down Bezels)**:
   Em vez do neumorfismo clássico desbotado ou do flat design excessivamente frio, o Cult UI utiliza técnicas de **bordas aninhadas em camadas concêntricas**. Em componentes como o *Texture Card* e o *Texture Button*, múltiplos invólucros `div` aplicam raios de curvatura decrescentes milimetricamente calculados (`rounded-[24px]` → `rounded-[23px]` → `rounded-[22px]` → `rounded-[21px]` → `rounded-[20px]`). Cada borda varia em opacidade (`border-white/60`, `border-black/10`, `border-white/50`, `border-neutral-950/20`), acompanhada de sombras internas e externas compostas (`inset 0 1px 1px 0 rgba(255,252,240,0.5)`). O resultado simula a textura física e a usinagem de um hardware analógico de luxo (lembrando a estética industrial da Teenage Engineering e Braun).

2. **Morfologia Fluida Inspirada no Hardware da Apple & Emil Kowalski**:
   O Cult UI é amplamente celebrado por introduzir implementações de referência do **Dynamic Island** e de **Family Drawers/Popovers** para a web. Em vez de abrir modais ou popovers que simplesmente alternam opacidade, o container físico sofre deformação contínua (*morphing*): a pílula compacta do Dynamic Island estica-se organicamente para formatos `tall`, `long`, `compactLong` e `massive`, utilizando clip-paths em formato *squircle* e curvas de mola balanceadas (`stiffness: 400, damping: 30`).

3. **Arquitetura de Entrada Direcionada (Direction-Aware Kinetics)**:
   Componentes de navegação, como as *Direction-Aware Tabs*, rastreiam o vetor de navegação do usuário. Se o usuário clica em uma aba à direita da atual, o conteúdo sai para a esquerda (`-300px`) com desfoque de movimento (`blur(4px)`), enquanto o novo entra pela direita (`+300px`). A altura do container recalcula-se e anima-se dinamicamente via `react-use-measure`, eliminando saltos rígidos de layout.

4. **Distribuição Aberta e Integração com Servidores MCP (Model Context Protocol)**:
   Seguindo o paradigma desacoplado do `shadcn/ui`, o Cult UI não é uma dependência fechada instalada como pacote opaco via NPM. É um registro público acessível via CLI (`npx shadcn@latest add @cult-ui/...`). Além disso, o projeto foi pioneiro em fornecer suporte a **servidores MCP**, permitindo que assistentes de IA (como Claude Code, Cursor e Copilot) pesquisem, leiam os esquemas de componentes e instalem o código diretamente nas bases de código dos desenvolvedores via linguagem natural.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **Aplicações de IA Generativa & Agentes Autônomos (AI Copilots & Workspaces)**:
   É a escolha definitiva para interfaces conversacionais com IA. Possui componentes nativos como *Prompt Composer*, *Halo Search*, *Halo Dropzone*, *AI Blob Warp* e *Agent Suggest Card Stack*, projetados especificamente para estados de inferência, streaming de tokens e arrasto de arquivos contextuais.
2. **Produtos SaaS B2B de Próxima Geração & DevTools**:
   Plataformas para engenheiros, designers e fundadores técnicos que exigem interfaces sofisticadas com atalhos de teclado, paletas de comando, docks magnéticos e painéis de configurações expansíveis (*Wizard Expandable*, *Toolbar Expandable*).
3. **Estúdios de Criação, Agências Digitais & Portfólios de Design Engineers**:
   Projetos que necessitam estabelecer autoridade visual imediata com mockups de hardware fotorrealistas (*Apple iPhone 17 Pro*, *Pro Display XDR*, *Mac Screen*), efeitos de vidro canelado (*Fluted Glass*, *Distorted Glass*) e tipografia animada (*Pixel Heading*, *Rolling Number*).
4. **Micro-interações de Onboarding & Feedback Rápido**:
   Fluxos de coleta de feedback, inscrição em waitlist e login social através de *Popover Form* e *Family Drawer*, onde o formulário emerge fluidamente do botão disparador sem desviar o usuário da tarefa principal.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Neutra e Estrutural)**:
  Superfícies sóbrias baseadas em tokens padrão do `shadcn/ui` (`bg-background`, `bg-card`, `text-foreground`, `border-border/40`), com tipografia limpa como `Geist Sans` ou `Inter` e espaçamento uniforme.
- **30% (Camada Tátil e Micro-interações do Cult UI)**:
  É onde o Cult UI brilha com mais força: *Direction Aware Tabs* em alternadores de seção, *Texture Buttons* e *Texture Cards* para formulários de autenticação/checkout, *Shift Cards* em grades de produto e *Family Drawer* para configurações em dispositivos móveis.
- **10% (Showstoppers Protagonistas)**:
  Reserve componentes como o *Dynamic Island* (no topo como hub de status/notificação), *Dock* magnético na base, ou o shader *AI Blob Warp* / *Hero Liquid Metal* estritamente para o clímax da página (Hero section ou Floating Header). Evite a coexistência de dois componentes com distorção por shader ou múltiplos loops de mola contínuos na mesma tela.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Tabelas de Dados Densas e ERPs Operacionais (B2B Legado)**:
  Grades de auditoria com centenas de linhas e colunas não comportam o overhead de transições de mola (*spring*) e sombras aninhadas; o uso de bordas com camadas múltiplas consome espaço útil de tela e distrai a atenção do operador.
- **Portais Institucionais com Requisitos de Acessibilidade Rigorosos (WCAG AAA)**:
  Efeitos de *Distorted Glass*, gradientes tênues de baixa opacidade e textos com desfoque transitório durante animação de entrada podem falhar em critérios rígidos de contraste estático caso não sejam acompanhados por fallbacks estritos de `prefers-reduced-motion`.
- **Projetos Mobile de Extrema Restrição de Banda / Dispositivos Low-End**:
  Renderizações que combinam `react-use-measure`, `AnimatePresence mode="popLayout"`, listeners de mouse no Dock e canvas de shaders exigem processamento contínuo de JavaScript, reduzindo a vida útil da bateria em dispositivos modestos.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **Multiplicação de Bordas Texturizadas**: Utilizar *Texture Card* com 5 sub-camadas de borda em todos os cartões de uma página, criando uma estética pesada e claustrofóbica. O efeito é indicado para cartões isolados de destaque ou modais focais.
- **Conflito de Física entre Animações Concorrentes**: Disparar um *Popover Form* expansível sobre um *Dock* que também responde ao cursor, gerando concorrência no event loop e perda de suavidade nos frames (jank).
- **Abandono do Hook de Redução de Movimento**: Omitir verificações de acessibilidade; todo componente complexo do Cult UI deve integrar `useReducedMotion()` para substituir animações cinéticas por alternâncias instantâneas de opacidade.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 12 componentes mais emblemáticos do catálogo Cult UI:

### 1. Dynamic Island (`dynamic-island`)
- **Anatomia Visual**: Pílula flutuante centralizada em preto profundo (`bg-black`), com bordas arredondadas que assumem geometrias squircle (`clipPath: url(#squircle-...)`). Suporta presets de dimensão calculados (`compact`, `compactLong`, `medium`, `large`, `tall`, `ultra`, `massive`), acomodando desde ícones de status mínimos até cartões ricos de onboarding e player multimídia.
- **Gatilho de Interação**: Disparado programaticamente via `useDynamicIslandSize().setSize(...)`, por fila de animação agendada (`useScheduledAnimations`) ou por eventos de clique/hover do usuário.
- **Onde encaixar**: Topo central fixo da viewport (Hero ou Header global), atuando como centro de notificações de agentes de IA, feedback de uploads assíncronos e controle de mídia.

### 2. Family Drawer (`family-drawer`)
- **Anatomia Visual**: Painel deslizante inferior (*bottom sheet*) inspirado no aplicativo Family e nos estudos de Emil Kowalski. Utiliza uma máquina de estados de visualizações (`viewsRegistry`), onde ao clicar em botões secundários (ex: "Configurações", "Perfil"), o conteúdo transiciona internamente enquanto a altura total do drawer expande ou contrai com fluidez milimétrica sem "pular".
- **Gatilho de Interação**: Abertura por botão gatilho (`FamilyDrawerTrigger`), arrasto tátil para fechar (via Vaul) e navegação entre sub-telas por `setView("settings")`.
- **Onde encaixar**: Menu principal em interfaces responsivas/mobile, modais de configurações multi-etapas e fluxos de checkout em painéis administrativos.

### 3. Direction Aware Tabs (`direction-aware-tabs`)
- **Anatomia Visual**: Barra de abas com fundo fosco e pílula ativa deslizante compartilhada (`layoutId="bubble"`). Os conteúdos associados contêm variantes de animação sensíveis ao índice numérico da aba clicada: deslizam de/para `+/-300px` combinados com `blur(4px)` e fade. O container mede sua própria altura automaticamente via `useMeasure()`.
- **Gatilho de Interação**: Clique em abas adjacentes; calcula `newTabId > activeTab ? 1 : -1` para definir o vetor vetorial de transição.
- **Onde encaixar**: Alternadores de planos no Pricing (Mensal / Anual / Enterprise), visualizadores de amostras de código em páginas de produto e navegação interna em Dashboards.

### 4. Popover Form (`popover-form`)
- **Anatomia Visual**: Um botão de ação padrão (ex: "Deixar Feedback" ou "Inscrever-se") que, ao ser clicado, não abre um modal intrusivo centralizado, mas sim expande fisicamente as próprias bordas (`layoutId={`${title}-wrapper`}`) transformando-se em um formulário estruturado com campos de texto e botão de envio, finalizando em um estado de sucesso animado (`PopoverFormSuccess`). Inclui ícones de corte geométrico (*cut-out icons*) para conexão visual com o botão de fechar.
- **Gatilho de Interação**: Clique no botão gatilho, submissão de formulário e clique externo (*click outside*) com tecla `Escape` para recolhimento.
- **Onde encaixar**: Canto inferior direito flutuante de web apps (Widget de Feedback), rodapés de blog (Newsletter Signup) e cabeçalhos de Landing Pages (Waitlist rápida).

### 5. Shift Card (`shift-card`)
- **Anatomia Visual**: Cartão composto por quatro zonas modulares (`topContent`, `topAnimateContent`, `middleContent`, `bottomContent`). Em repouso, exibe apenas título e ícone conciso. Ao entrar em hover, o cabeçalho sofre deslocamento vertical suave e o miolo expande de 38px para 194px, revelando prévias visuais, badges e botões de compartilhamento social.
- **Gatilho de Interação**: `onMouseEnter` / `onMouseLeave` acionando transições com easing `circIn` e `circOut` em Framer Motion.
- **Onde encaixar**: Grades de catálogo de produtos digitais, seções de equipe (*Team Showcase*) e vitrines de funcionalidades em Bento Grids.

### 6. Texture Card & Texture Button (`texture-card` / `texture-button`)
- **Anatomia Visual**: Estrutura de cartão baseada em cinco invólucros `div` concêntricos, cada um com raio calculado (`calc(var(--radius) - n*px)`) e bordas translúcidas invertidas (luz no topo, sombra na base). Os botões de textura acompanham sombras internas duplas e reflexos chanfrados que reproduzem botões de maquinários e sintetizadores analógicos.
- **Gatilho de Interação**: Estados de foco, hover e pressionamento com afundamento físico sutil (`active:scale-[0.98]`).
- **Onde encaixar**: Cartão central de login/cadastro, painéis de configurações de tokens de API e cartões de planos de assinatura de alto ticket.

### 7. Halo Search & Halo Input (`halo-search` / `halo-input`)
- **Anatomia Visual**: Campo de busca com anel luminoso de gradiente sutil contornando o perímetro do input. Inclui um avatar interativo animado por shader de distorção (*Warp Blob*), indicador de carregamento de busca com rotação precisa e botão de limpeza suave em crossfade.
- **Gatilho de Interação**: Foco do teclado (`focus-visible`), digitação com animação escalonada dos caracteres de loading e atalho `Enter`.
- **Onde encaixar**: Seção Hero de documentações técnicas, centros de busca global (Command Bar / Spotlight) e interfaces de consulta de bases de dados vetoriais.

### 8. Magnified Dock (`dock`)
- **Anatomia Visual**: Barra de ferramentas flutuante baseada no dock do macOS. Conforme o cursor se move sobre os ícones, os elementos próximos sofrem ampliação proporcional contínua baseada em uma função cossenoidal de expoente 12 (`Math.cos(...)**12`), interpolada por física de mola com baixíssima inércia (`mass: 0.1, stiffness: 150, damping: 12`).
- **Gatilho de Interação**: `onMouseMove` contínuo alimentando um `MotionValue` de coordenadas X absolutas.
- **Onde encaixar**: Barra de ferramentas inferior em aplicações web criativas (estúdios de design, editores de nós de IA, dashboards imersivos).

### 9. Morph Surface & Expandable Screen (`morph-surface` / `expandable-screen`)
- **Anatomia Visual**: Primitiva de transição que permite que um elemento compacto (como um chip, badge ou cartão resumido) expanda suas dimensões para preencher a tela inteira ou um modal expandido, mantendo continuidade vetorial e espacial dos elementos internos através de `layoutId` compartilhado.
- **Gatilho de Interação**: Clique no cartão gatilho e botão de retorno/fechamento.
- **Onde encaixar**: Visualização expandida de cartões de tarefas no Kanban, inspeção de logs de agentes e galerias de projetos.

### 10. Sortable List (`sortable-list`)
- **Anatomia Visual**: Lista de itens reordenáveis via arrastar e soltar (*drag and drop*). Conforme o usuário arrasta um item, os itens irmãos deslizam suavemente com física de amortecimento para ceder espaço, com sombras elevadas e rotação leve no item ativo.
- **Gatilho de Interação**: `drag="y"` do Framer Motion com `dragConstraints` e reordenação imutável de arrays de dados.
- **Onde encaixar**: Priorização de prompts em pipelines de IA, organizadores de tarefas e listas de reprodução.

### 11. Distorted Glass & Fluted Glass (`distorted-glass` / `fluted-glass`)
- **Anatomia Visual**: Filtros visuais aplicados a imagens e vídeos de fundo que simulam vidro estriado/canelado e lentes de dispersão óptica através de filtros SVG e máscaras CSS compostas, conferindo sofisticação sem o peso de um motor 3D completo.
- **Gatilho de Interação**: Passivo (renderização gráfica de backdrop) ou reativo à posição do ponteiro do mouse.
- **Onde encaixar**: Pano de fundo da seção Hero, divisores de seção institucionais e overlays de modais decorativos.

### 12. Text Animate & Pixel Heading (`text-animate` / `pixel-heading-character`)
- **Anatomia Visual**: Tipografia que se desdobra letra por letra ou palavra por palavra com efeitos de revelação por pixels estilizados, escala vertical ou transições de máquina de escrever analógica, casando perfeitamente com fontes da família `Geist Pixel` e `Geist Mono`.
- **Gatilho de Interação**: Disparado ao entrar na viewport (`whileInView={{ once: true }}`) com intervalos escalonados (*staggerChildren* de 0.03s a 0.08s).
- **Onde encaixar**: Título principal da página (H1 da Hero), slogans de lançamento e indicadores numéricos com contagem progressiva (*Rolling Number*).

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Ambiente

O Cult UI é totalmente aderente ao ecossistema moderno de React 19 / Next.js 15 e Motion (a nova geração do Framer Motion):

```bash
# 1. Dependências fundamentais de animação, medição e ícones
npm install motion react-use-measure vaul lucide-react clsx tailwind-merge cva

# 2. Instalação individual via shadcn registry do Cult UI
npx shadcn@latest add @cult-ui/dynamic-island
npx shadcn@latest add @cult-ui/direction-aware-tabs
npx shadcn@latest add @cult-ui/popover-form
npx shadcn@latest add @cult-ui/texture-card
npx shadcn@latest add @cult-ui/dock
```

Configuração essencial de utilitários de classe (`lib/utils.ts`):
```typescript
import { type ClassValue, clsx } from "clsx";
import { twMerge } from "tailwind-merge";

export function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs));
}
```

---

### Constantes de Física de Movimento & Transições do Cult UI

O Cult UI fundamenta suas micro-interações em perfis de molas (*spring physics*) cirurgicamente afinados:

```typescript
// Configurações de Física canônicas extraídas dos componentes do Cult UI
export const CULT_PHYSICS = {
  // 1. Dynamic Island Morphing: Retorno firme, sem oscilações excessivas
  dynamicIsland: {
    type: "spring" as const,
    stiffness: 400,
    damping: 30,
  },

  // 2. Direction Aware Tabs: Leve elasticidade tátil para indicar direção
  directionTabs: {
    type: "spring" as const,
    duration: 0.4,
    bounce: 0.19,
  },

  // 3. Popover Form Expansion: Estabilidade precisa para manter legibilidade de texto
  popoverForm: {
    type: "spring" as const,
    duration: 0.4,
    bounce: 0,
  },

  // 4. Magnified Dock Proximity Curve: Agilidade ultraleve para rastreamento a 60fps
  dockItem: {
    mass: 0.1,
    stiffness: 150,
    damping: 12,
  },

  // 5. Dock Opacity & Background Transitions
  dockFade: {
    stiffness: 300,
    damping: 20,
  },
} as const;
```

---

### Receita de Código Funcional 1: Dynamic Island Reativo

Implementação completa e auto-contida do padrão **Dynamic Island** com suporte a estados polimórficos e morphing por mola:

```tsx
"use client";

import React, { createContext, useContext, useState, useId } from "react";
import { AnimatePresence, motion } from "motion/react";
import { Sparkles, CheckCircle2, AlertCircle } from "lucide-react";
import { cn } from "@/lib/utils";

type IslandState = "idle" | "thinking" | "success" | "error";

interface IslandContextType {
  state: IslandState;
  setState: (s: IslandState) => void;
}

const IslandContext = createContext<IslandContextType | null>(null);

const PRESETS = {
  idle: { width: 160, height: 44, radius: 24 },
  thinking: { width: 280, height: 52, radius: 26 },
  success: { width: 320, height: 68, radius: 30 },
  error: { width: 300, height: 64, radius: 28 },
};

export function DynamicIslandRoot({ children }: { children: React.ReactNode }) {
  const [state, setState] = useState<IslandState>("idle");
  return (
    <IslandContext.Provider value={{ state, setState }}>
      <div className="relative flex flex-col items-center justify-center py-6">
        {children}
      </div>
    </IslandContext.Provider>
  );
}

export function DynamicIslandDisplay() {
  const context = useContext(IslandContext);
  if (!context) throw new Error("DynamicIslandDisplay deve estar dentro de DynamicIslandRoot");
  const { state } = context;
  const config = PRESETS[state];

  return (
    <motion.div
      layout
      animate={{
        width: config.width,
        height: config.height,
        borderRadius: config.radius,
      }}
      transition={{
        type: "spring",
        stiffness: 400,
        damping: 30,
      }}
      className={cn(
        "relative overflow-hidden bg-black text-white shadow-2xl",
        "border border-white/10 dark:border-white/15",
        "flex items-center justify-center px-4 select-none"
      )}
    >
      <AnimatePresence mode="popLayout" initial={false}>
        {state === "idle" && (
          <motion.div
            key="idle"
            initial={{ opacity: 0, scale: 0.85 }}
            animate={{ opacity: 1, scale: 1 }}
            exit={{ opacity: 0, scale: 0.85 }}
            transition={{ duration: 0.2 }}
            className="flex items-center gap-2 font-mono text-xs text-neutral-400"
          >
            <span className="size-2 rounded-full bg-emerald-500 animate-pulse" />
            <span>AI Copilot Ready</span>
          </motion.div>
        )}

        {state === "thinking" && (
          <motion.div
            key="thinking"
            initial={{ opacity: 0, y: 10, filter: "blur(4px)" }}
            animate={{ opacity: 1, y: 0, filter: "blur(0px)" }}
            exit={{ opacity: 0, y: -10, filter: "blur(4px)" }}
            transition={{ duration: 0.25 }}
            className="flex items-center gap-3 text-sm text-cyan-300 font-medium"
          >
            <Sparkles className="size-4 animate-spin text-cyan-400" />
            <span>Processando raciocínio...</span>
          </motion.div>
        )}

        {state === "success" && (
          <motion.div
            key="success"
            initial={{ opacity: 0, scale: 0.9, filter: "blur(4px)" }}
            animate={{ opacity: 1, scale: 1, filter: "blur(0px)" }}
            exit={{ opacity: 0, scale: 0.9 }}
            transition={{ duration: 0.25 }}
            className="flex items-center gap-3 text-sm text-white"
          >
            <CheckCircle2 className="size-5 text-emerald-400 shrink-0" />
            <div className="flex flex-col text-left">
              <span className="font-semibold text-xs leading-none">Deploy Concluído</span>
              <span className="text-[11px] text-neutral-400">Ambiente pronto para tráfego</span>
            </div>
          </motion.div>
        )}

        {state === "error" && (
          <motion.div
            key="error"
            initial={{ opacity: 0, scale: 0.9 }}
            animate={{ opacity: 1, scale: 1 }}
            exit={{ opacity: 0, scale: 0.9 }}
            transition={{ duration: 0.25 }}
            className="flex items-center gap-2 text-rose-400 text-sm font-medium"
          >
            <AlertCircle className="size-4 shrink-0" />
            <span>Falha na compilação</span>
          </motion.div>
        )}
      </AnimatePresence>
    </motion.div>
  );
}
```

---

### Receita de Código Funcional 2: Texture Card com Bordas em Camadas

Exemplo fiel da técnica assinatura do Cult UI para cartões com acabamento escultural e chanfro tátil:

```tsx
import * as React from "react";
import { cn } from "@/lib/utils";

interface TextureCardProps extends React.HTMLAttributes<HTMLDivElement> {
  children: React.ReactNode;
}

/**
 * TextureCard: Construção de bordas concêntricas decrescentes (24px a 20px)
 * que simula a precisão e chanfros de hardware físico moderno.
 */
export const TextureCard = React.forwardRef<HTMLDivElement, TextureCardProps>(
  ({ className, children, ...props }, ref) => {
    return (
      <div
        ref={ref}
        className={cn(
          "rounded-[24px] border border-white/60 dark:border-stone-900/80",
          "bg-gradient-to-b from-neutral-100 to-white/70 dark:from-neutral-900 dark:to-neutral-950",
          "shadow-[0_1px_1px_rgba(0,0,0,0.05),0_10px_25px_-5px_rgba(0,0,0,0.1)]",
          className
        )}
        {...props}
      >
        {/* Camada 2: Chanfro de sombra fina */}
        <div className="rounded-[23px] border border-black/10 dark:border-neutral-900/80">
          {/* Camada 3: Reflexo de luz especular interno */}
          <div className="rounded-[22px] border border-white/50 dark:border-neutral-950">
            {/* Camada 4: Borda de contraste escuro */}
            <div className="rounded-[21px] border border-neutral-950/20 dark:border-neutral-900/70">
              {/* Camada 5: Invólucro de conteúdo final */}
              <div className="w-full rounded-[20px] border border-white/50 dark:border-neutral-800/50 p-6 text-foreground">
                {children}
              </div>
            </div>
          </div>
        </div>
      </div>
    );
  }
);
TextureCard.displayName = "TextureCard";
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar e especificar componentes do **Cult UI** no documento de arquitetura de um novo projeto, siga rigorosamente as diretrizes abaixo:

1. **Declaração Semântica e Papel Hierárquico**:
   - Defina claramente em qual fatia da regra 60-30-10 o componente atuará. Nunca marque mais de um componente como *Showstopper (10%)* na mesma página.
   - *Exemplo de Declaração*:
     ```markdown
     - Componente: `DynamicIsland` (Cult UI)
       - Categoria: Showstopper (10%)
       - Posição: Topo fixo da viewport (Sticky Header)
       - Estados suportados: `idle`, `processing`, `streaming`, `success`
       - Física de Transição: Spring (stiffness: 400, damping: 30)
     ```

2. **Isolamento de Estado e Performance**:
   - Componentes táteis como `DirectionAwareTabs` e `ShiftCard` realizam medições em tempo real via `useMeasure` e manipulam propriedades de filtro CSS (`blur(4px)`). Certifique-se de que a árvore de componentes filhos não dispare re-renderizações desnecessárias em listas grandes sem memoização (`React.memo` / `useMemo`).

3. **Fallback para Acessibilidade Obrigatório (`useReducedMotion`)**:
   - Toda declaração de blueprint contendo componentes do Cult UI deve exigir compatibilidade com redução de movimento. Se o usuário tiver `prefers-reduced-motion` ativado no sistema operacional, a física de mola e os deslocamentos de eixo X/Y devem ser desativados, mantendo apenas a transição de opacidade com duração `0s` ou `0.15s`.

4. **Harmonização de Temas e Tokens de Estilo**:
   - Os componentes do Cult UI foram calibrados para casar com paletas profundas de `zinc` e `stone`. Quando aplicados em temas claros (*light mode*), mantenha as camadas de borda com opacidade atenuada (`border-white/60`) e fundos em `bg-white/80` com `backdrop-blur-md` para preservar a tridimensionalidade tátil sem gerar ruído visual excessivo.
