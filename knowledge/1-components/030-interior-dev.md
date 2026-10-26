---
id: "interior-dev"
name: "Interior.dev"
url: "https://www.interior.dev/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Invisible Craft", "Tactile Micro-interactions", "Refined Neutral Minimal", "Sub-pixel Precision"]
densidade_informacao: "Media"
impacto_visual: "Utilitario/Base"
custo_computacional: "Medio (Framer Motion/JS)"
stack_frameworks: ["React", "Next.js", "Tailwind CSS", "Motion (Framer Motion)", "TypeScript", "shadcn/ui Registry"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "SF Pro Display / Text", "JetBrains Mono"]
  paletas_ideais: ["Stone Neutral (Stone 50 a 900)", "Zinc Subdued Dark Mode", "Monochrome High-Precision", "Muted Accent Status (Emerald/Amber/Rose)"]
  combinacoes_recomendadas: ["Shadcn UI", "Radix UI Primitives", "Origin UI", "Cult UI", "Sonner"]
  conflitos_esteticos: ["Brutalismo Hiper-Saturado", "Neumorfismo Pesado / Soft-UI", "Maximalismo 3D Distrativo", "Corporate Memphis Colorido"]
---

# Interior.dev — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Interior.dev** (criado por Ozzy / `@ozzyxs1a`) aborda uma das maiores deficiências silenciosas das aplicações web contemporâneas: a sensação de "software barato" nos **500 milissegundos que sucedem uma interação física do usuário** (*"Software feels cheap in the half-second after a click"*). Enquanto a maioria das bibliotecas de UI foca em efeitos pirotécnicos de entrada (*hero transitions*, auroras, *shimmer borders*), o Interior.dev é um laboratório de alta precisão focado na **física do feedback tátil e no *invisible craft***.

Sua assinatura estética e de engenharia é definida por quatro pilares técnicos:

1. **Eliminação Sistemática do Layout Shift (Zero-Jank Transitions)**:
   Em botões de ação assíncrona tradicionais, alternar o texto de *"Salvar"* para *"Salvando..."* expande a largura do botão, desloca os elementos vizinhos e faz o cursor perder o foco. No Interior.dev, todos os estados (`idle`, `pending`, `success`, `error`) compartilham o mesmo contêiner em grid CSS sobreposto (`col-start-1 row-start-1`), reservando espaço e estabilizando a geometria do layout milimetricamente antes mesmo do gatilho ocorrer.
2. **Interrompibilidade Físico-Mecânica (Physics Interruptibility)**:
   Diferente de transições baseadas em curvas estáticas de CSS onde um clique repetido reinicia a animação bruscamente ou enfileira eventos indesejados, o Interior.dev utiliza **simulação física contínua via Motion (Framer Motion)**. Se um usuário aborta um clique longo (*Hold to Confirm*), solta o mouse no meio do caminho ou clica repetidamente num gatilho, a mola (*spring*) recupera a velocidade escalar e desacelera suavemente a partir do ponto espacial exato onde foi interrompida (`ease: [0.23, 1, 0.32, 1]`).
3. **Acessibilidade Incondicional (Reduced Motion como Canal Semântico)**:
   A biblioteca rejeita a prática preguiçosa de ocultar animações quando `prefers-reduced-motion: reduce` está ativo. Em vez disso, cada componente preserva a chegada integral da informação sem a latência visual: o trajeto de interpolação é colapsado para duração instantânea (`duration: 0`), mantendo mensagens sonoras em regiões acessíveis (`aria-live="polite"` e `.sr-only`).
4. **Arquitetura Desacoplada: Headless Hook + Primitiva Estilizada**:
   Cada componente é disponibilizado em arquivo único TypeScript (`components/interior/[nome].tsx`), compatível com o CLI oficial do shadcn (`npx shadcn@latest add https://www.interior.dev/r/[component].json`). Essa arquitetura exporta separadamente um **hook de comportamento puro** (ex: `useAsyncAction`, `useHoldToConfirm`, `useDetentSlider`, `useValueFlash`) e uma camada de renderização visual em Tailwind CSS, garantindo total liberdade para adaptação a qualquer design system corporativo.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados
- **Developer Tools & Painéis Cloud**: Onde a latência percebida e a previsibilidade mecânica de comandos via mouse ou teclado ditam a percepção de poder da ferramenta (ex: consoles de banco de dados, painéis de build, terminais web).
- **Fintechs, Criptoativos & Plataformas de Trading**: Ambientes com atualização de cotações em tempo real e ações irreversíveis (transferências, liquidações, ordens a mercado), onde o componente `ValueFlash` sinaliza oscilações de preço com micro-pulsos verdes/vermelhos e o `HoldToConfirm` previne ordens acidentais sem a fricção excessiva de modais invasivos.
- **SaaS B2B de Alta Complexidade & Edição Colaborativa**: Interfaces densas (estilo Linear, Notion, Figma) que exigem tooltips com inteligência de grupo (`TooltipGroup` que compartilha estado quente/frio) e alternadores de modo sem salto visual (`SegmentedControl`).
- **Configurações Críticas & "Danger Zones"**: Zonas destrutivas onde exclusão de workspaces, revogação de chaves de API e wipeout de tenants exigem confirmação deliberada com feedback haptic (`navigator.vibrate`) e medição de abandono de clique.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Neutra e Estrutural)**: Utilize a paleta sóbria de `stone` ou `zinc`, tipografia sans neutra (`Geist Sans` ou `Inter`) com tracking levemente negativo (`tracking-[-0.01em]`), raios de curvatura refinados (`rounded-[9px]` e `rounded-[6px]`) e bordas translúcidas sutis (`border-stone-200` / `dark:border-white/[0.16]`).
- **30% (A Especialidade do Interior.dev — Camada Tátil de Resposta)**: É exatamente aqui que o Interior.dev governa com supremacia absoluta. Ele preenche toda a camada de feedback contextual da interface: inputs que alertam sobre forças de senha, botões que comunicam status assíncrono internamente, controles deslizantes com pontos de parada magnéticos (*detents*) e abas com revelação invertida de texto.
- **10% (Showstoppers Focados em Segurança e Conclusão)**: Elementos de confirmação de alto risco (`HoldToConfirm` preenchendo a superfície do botão com máscara de corte dinâmica) e celebrações comedidas (`LikeBurst` com dispersão física de partículas elásticas em conclusões de fluxo).

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Landing Pages Teatrais / Marketing de Efeito Visual Puro**: O Interior.dev não foi concebido para criar backgrounds 3D hipnóticos, distorções de lente WebGL ou textos orbitais. Aplicá-lo como "atração visual de topo de funil" descaracteriza sua proposta de valor ergonômica.
- **Aplicações Web com Restrição Crítica de Bundle Zero-JS**: Páginas geradas puramente via HTML estático / SSG ultra-minimalista sem runtime React/Motion (ex: documentação Markdown pura ou blogs sem script), onde o overhead do pacote `motion` não é justificável.
- **Modos de Exibição com Alta Densidade Contínua Não Virtualizada**: Utilizar micro-animações complexas com múltiplos ouvintes de pointer capture em tabelas com milhares de linhas renderizadas simultaneamente no DOM sem virtualização (`@tanstack/react-virtual`), o que pode sobrecarregar o garbage collector em navegadores mobile antigos.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões):
- **Remoção das Classes de Live Region Acessível**: Apagar os contêineres `.sr-only` com `role="status"` e `aria-live="polite"` fornecidos pelo componente, privando usuários de leitores de tela de saberem se uma requisição foi concluída ou falhou.
- **Multiplicação de Tempos de Espera Excessivos**: Configurar o `duration` do `HoldToConfirm` para mais de 2500ms em tarefas corriqueiras, transformando o mecanismo de segurança em um gargalo de frustração e atrito cognitivo.
- **Desativação Arbitrária da Física de Retorno**: Tentar substituir o cálculo dinâmico de recuo (`releaseRate = 2.5`) do `HoldToConfirm` por transições fixas de CSS `transition: all 0.3s ease`, o que reintroduz o efeito de "corte seco" caso o usuário hesite antes de soltar o botão.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 12 componentes mais emblemáticos do catálogo de 54 itens do Interior.dev:

### 1. Loading Button (Botão Assíncrono com Zero Layout Shift)
- **Anatomia Visual**: Botão compacto com bordas esculpidas (`rounded-[9px]`, relevo interno sutil `shadow-[inset_0_1.5px_0_rgba(255,255,255,0.95)]`). Em vez de empurrar o conteúdo, os quatro estados (`idle`, `pending`, `success`, `error`) coexistem em uma grade `grid place-items-center`. O texto em repouso se dissolve com blur direcional (`filter: blur(3px)`, `y: 3`) enquanto o spinner customizado SVG de 12px entra suavemente.
- **Gatilho de Interação**: Clique do usuário que dispara uma `Promise`. Se rejeitada, assume o tom `text-red-600` com ícone de alerta; se resolvida, assume `text-emerald-600` com checkmark e retorna ao estado inicial após `resetAfter` (1400ms padrão).
- **Onde encaixar**: Ações principais de formulários, botões de publicação de release, checkout e salvamento de configurações.

### 2. Hold to Confirm (Barreira Tátil para Ações Destrutivas)
- **Anatomia Visual**: Um botão de aparência limpa que, ao ser pressionado continuamente, preenche progressivamente seu fundo por meio de uma máscara de recorte dinâmica (`clipPath: inset(0 ${(1 - v) * 100}% 0 0)`). Ao atingir 100%, o rótulo inverte de contraste, emite pulso tátil (`navigator.vibrate(14)`) e dispara a confirmação.
- **Gatilho de Interação**: `onPointerDown` com captura de ponteiro (`setPointerCapture`) e rastreamento contínuo em `requestAnimationFrame`. Se o ponteiro for liberado antes do tempo ou sair do limite de tolerância (`moveTolerance: 10px`), a barra retrocede com curva de amortecimento fluida (`ease: [0.23, 1, 0.32, 1]`) a uma taxa acelerada de 2.5x.
- **Onde encaixar**: Zona de perigo de workspaces, exclusão irreversível de bancos de dados, cancelamento de assinaturas e revogação de tokens de segurança.

### 3. Segmented Control com Inversão de Máscara (Dual-Layer Text Reveal)
- **Anatomia Visual**: Seletor segmentado com trilho cinza fosco (`bg-stone-100/70 dark:bg-[#1D1D1A]`). O elemento deslizante (*thumb*) desliza horizontalmente com mola de alta rigidez (`stiffness: 520, damping: 34`). O diferencial técnico está no interior do thumb: ele renderiza uma réplica exata e espelhada do texto com deslocamento vetorial inverso (`x: maskX`), criando a famosa revelação de texto em alto contraste estilo Apple macOS/iOS.
- **Gatilho de Interação**: Clique em qualquer segmento ou navegação nativa de acessibilidade via setas direcionais do teclado (`ArrowLeft`, `ArrowRight`, `Home`, `End`), pulando automaticamente segmentos desabilitados.
- **Onde encaixar**: Seletores de visualização de painéis (ex: Lista / Kanban / Calendário), filtros de tempo (Dia / Mês / Ano) e configurações de tema.

### 4. Tooltip Group com Gerenciador de Temperatura (Warm/Cool State)
- **Anatomia Visual**: Micro-balão de dica com tipografia em 12px, renderizado rente ao elemento alvo sem jitter visual de posicionamento.
- **Gatilho de Interação**: O primeiro hover exige paciência do usuário (delay de ~400ms para evitar poluição visual durante o movimento comum do mouse). Uma vez que o grupo fica no estado "quente" (*warm*), o mouse ao deslizar para botões irmãos adjacentes abre os novos tooltips **instantaneamente** (sem delay). Ao remover o mouse de todo o grupo, um temporizador de resfriamento (*cooldown*) desativa o grupo após ~300ms.
- **Onde encaixar**: Barras de ferramentas densas com botões de ícone (ex: editores de texto rico, réguas de ferramentas do Figma, barras de atalhos de dashboards).

### 5. Slider Detents (Controle Deslizante com Paradas Magnéticas & Haptic)
- **Anatomia Visual**: Barra de controle deslizante com indicadores visuais sutis (*notches*) nas posições chave.
- **Gatilho de Interação**: `pointermove` com atração gravitacional matemática para paradas pré-configuradas (*detents*). Ao passar por um ponto de ancoragem, o thumb "engata" magneticamente e aciona um micro-pulso tátil (`navigator.vibrate(6)`), reproduzindo a sensação tátil de um potenciômetro mecânico de equipamento de áudio analógico.
- **Onde encaixar**: Ajustes de zoom, seleção de planos/limites de cobrança, granularidade de tempo de logs e ajustes de sensibilidade.

### 6. Value Flash (Micro-Pulso de Atualização em Tempo Real)
- **Anatomia Visual**: Rótulo numérico tabular (`tabular-nums`) que mantém seu tamanho estático, mas ao sofrer mutação de valor, projeta um leve pico de escala (`scale: 1.05`) combinado com background translúcido e tonalidade direcional: verde suave para aumentos (`bg-emerald-500/12 text-emerald-600`) e vermelho suave para reduções (`bg-red-500/12 text-red-600`).
- **Gatilho de Interação**: Detecção reativa de alteração de prop numérica em hook `useValueFlash`, com dissipação controlada após `hold` (900ms) e anúncio de áudio acessível sincronizado via timeout com leitor de tela (`announceAfter: 700ms`).
- **Onde encaixar**: Cotações de cripto/ações, contadores de usuários ativos em tempo real, telemetria de CPU/RAM em servidores e feeds de pedidos de e-commerce.

### 7. OTP Input (Autenticação de 2 Fatores sem Fricção)
- **Anatomia Visual**: Grupo de 6 inputs segmentados com indicação de foco luminoso em anel interno (`focus-visible:shadow-[inset_0_0_0_1px_#4568FF]`).
- **Gatilho de Interação**: Captura eventos de colar (`onPaste`) dividindo a string automaticamente em todas as células, avanço automático do foco ao digitar dígitos, retrocesso com `Backspace` reposicionando o cursor na célula anterior e tratamento inquebrável para cliques desordenados.
- **Onde encaixar**: Modais de autenticação em duas etapas (2FA), verificação de e-mail e desbloqueio de chaves de hardware.

### 8. Live Activity / Status Pill (Indicador de Tarefas em Background)
- **Anatomia Visual**: Pílula flutuante compacta (`h-7 px-2.5 rounded-full`) com micro-indicador de pulso luminoso e contador de tempo decorrido.
- **Gatilho de Interação**: Animação de respiração controlada via opacidade e escala suave, reagindo a transições de status da API (ex: *Uploading* -> *Processing* -> *Ready*).
- **Onde encaixar**: Cabeçalho de dashboards de IA durante geração de modelos, rodapé de ferramentas de exportação de vídeo e sincronizadores de dados em nuvem.

### 9. Like Burst (Reação com Física de Partículas Elásticas)
- **Anatomia Visual**: Ícone de coração ou estrela que sofre contração elástica seguida de expansão explosiva, acompanhado de um halo de partículas vetoriais microscópicas que se dispersam radialmente e evaporam.
- **Gatilho de Interação**: Clique rápido do usuário, projetado com resiliência a toques múltiplos subsequentes sem engasgar o render loop.
- **Onde encaixar**: Botões de favoritar em feeds de comunidade, aprovação de comentários e reações rápidas em workspaces colaborativos.

### 10. Skeleton Swap (Transição de Conteúdo sem Clarão)
- **Anatomia Visual**: Bloco de esqueleto em cinza suave com cintilação monocromática contida.
- **Gatilho de Interação**: Ao finalizar o carregamento assíncrono dos dados, o esqueleto não "desaparece" bruscamente gerando pulo de layout; ele se dissolve com *cross-fade* direto para a imagem/texto final, eliminando clarões em conexões rápidas.
- **Onde encaixar**: Cartões de usuário, feeds de listagem, painéis de faturamento e visualizadores de métricas.

### 11. Expanding Search (Campo de Busca Expansível)
- **Anatomia Visual**: Botão de busca compacto com ícone de lupa em repouso que, ao ser focado ou clicado, expande horizontalmente com mola elástica, preservando os alinhamentos dos botões vizinhos sem colisão.
- **Gatilho de Interação**: `onFocus` expandindo suavemente a largura calculada, com fechamento automático em `onBlur` caso o campo esteja vazio e atalho de teclado `Esc` para cancelamento rápido.
- **Onde encaixar**: Barras de navegação superiores com espaço horizontal concorrido.

### 12. Floating Label (Entrada de Texto com Rótulo Flutuante Óptico)
- **Anatomia Visual**: Campo de formulário onde o placeholder repousa no centro vertical e, ao receber foco ou preenchimento, migra para a borda superior reduzindo de escala tipográfica, mantendo legibilidade sem desalinhar a linha de base dos caracteres.
- **Gatilho de Interação**: Rastreamento de estado de foco e preenchimento (`hasValue || isFocused`) via interpolação CSS de alta taxa de quadros.
- **Onde encaixar**: Formulários de cadastro de novos usuários, checkout de cartão de crédito e telas de login empresariais.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup
O Interior.dev adota uma política estrita de **dependência única**: necessita exclusivamente da biblioteca `motion` (o novo pacote unificado do Framer Motion):

```bash
# Instalação do runtime de animação
npm install motion
# ou via Bun
bun add motion
```

Para integrar componentes diretamente no seu projeto no formato shadcn:

```bash
# Exemplo: Adicionar o Loading Button
npx shadcn@latest add https://www.interior.dev/r/loading-button.json

# Exemplo: Adicionar o Hold to Confirm
npx shadcn@latest add https://www.interior.dev/r/hold-to-confirm.json

# Exemplo: Adicionar o Segmented Control
npx shadcn@latest add https://www.interior.dev/r/segmented-control.json
```

### Física de Movimento, Molas & Curvas
Os componentes do Interior.dev padronizam constantes de física para garantir uniformidade tátil em toda a aplicação:

- **Mola Rápida de Célula / Elementos Táteis (`CELL`)**:
  ```ts
  export const CELL_SPRING = {
    type: "spring",
    stiffness: 520,
    damping: 34,
    mass: 0.45,
  } as const;
  ```
  *Uso*: Toque de botões, deslocamento do cursor no Segmented Control, seleção de abas. Resposta imediata com ausência quase total de oscilação excessiva (*low overshoot*).

- **Mola de Transição Facial / Crossfade (`FACE` / `CROSSFADE`)**:
  ```ts
  export const FACE_SPRING = {
    type: "spring",
    stiffness: 260,
    damping: 34,
    mass: 0.8,
  } as const;
  ```
  *Uso*: Alternância entre ícones e rótulos de texto dentro de botões, revelação de mensagens de sucesso ou erro.

- **Curva de Aborto / Desaceleração Dinâmica**:
  ```ts
  export const ABORT_EASE = [0.23, 1, 0.32, 1] as const;
  ```
  *Uso*: Retorno acelerado e amortecido quando o usuário interrompe uma ação contínua (ex: soltar o clique no *Hold to Confirm*).

- **Fallback para Movimento Reduzido (`INSTANT`)**:
  ```ts
  export const INSTANT_TRANSITION = { duration: 0 } as const;
  ```

---

### Receita de Código Funcional: Hold to Confirm com Feedback Tátil Completo

Abaixo está a implementação integral de nível de produção do componente **HoldToConfirm**, ilustrando a separação entre o Headless Hook (`useHoldToConfirm`) e a primitiva com máscara dinâmica e acessibilidade:

```tsx
"use client";

import React, {
  useCallback,
  useEffect,
  useId,
  useRef,
  useState,
} from "react";
import {
  animate,
  motion,
  useMotionValue,
  useReducedMotion,
  useTransform,
} from "motion/react";

// Constantes de física do Interior.dev
const FACE_SPRING = {
  type: "spring",
  stiffness: 260,
  damping: 34,
  mass: 0.8,
} as const;

export type HoldPhase = "idle" | "holding" | "releasing" | "committed";

export type UseHoldToConfirmOptions = {
  onConfirm: () => void;
  onAbort?: () => void;
  duration?: number;
  steps?: number;
  releaseRate?: number;
  moveTolerance?: number;
  haptic?: boolean;
  disabled?: boolean;
};

/**
 * Headless Hook que controla o ciclo de vida e física temporal do pressionamento contínuo
 */
export function useHoldToConfirm({
  onConfirm,
  onAbort,
  duration = 1800,
  steps = 20,
  releaseRate = 2.5,
  moveTolerance = 10,
  haptic = true,
  disabled = false,
}: UseHoldToConfirmOptions) {
  const [step, setStep] = useState(0);
  const [phase, setPhase] = useState<HoldPhase>("idle");
  const phaseRef = useRef<HoldPhase>("idle");
  const isDown = useRef(false);
  const elapsed = useRef(0);
  const lastTime = useRef(0);
  const rafHandle = useRef(0);
  const touchOrigin = useRef<{ x: number; y: number } | null>(null);

  const confirmCb = useRef(onConfirm);
  confirmCb.current = onConfirm;
  const abortCb = useRef(onAbort);
  abortCb.current = onAbort;

  const updatePhase = useCallback((next: HoldPhase) => {
    phaseRef.current = next;
    setPhase(next);
  }, []);

  const reset = useCallback(() => {
    cancelAnimationFrame(rafHandle.current);
    rafHandle.current = 0;
    isDown.current = false;
    elapsed.current = 0;
    touchOrigin.current = null;
    setStep(0);
    updatePhase("idle");
  }, [updatePhase]);

  const begin = useCallback(
    (point?: { x: number; y: number }) => {
      if (disabled) return;
      if (phaseRef.current === "committed" || phaseRef.current === "holding") {
        return;
      }
      touchOrigin.current = point ?? null;
      isDown.current = true;
      updatePhase("holding");

      if (rafHandle.current) return;
      lastTime.current = performance.now();

      const loop = (now: number) => {
        const dt = Math.min(64, now - lastTime.current);
        lastTime.current = now;

        elapsed.current += isDown.current ? dt : -dt * releaseRate;

        if (elapsed.current >= duration) {
          rafHandle.current = 0;
          elapsed.current = duration;
          isDown.current = false;
          touchOrigin.current = null;
          setStep(steps);
          updatePhase("committed");
          if (haptic && typeof navigator !== "undefined") {
            navigator.vibrate?.(14);
          }
          confirmCb.current();
          return;
        }

        if (elapsed.current <= 0) {
          rafHandle.current = 0;
          elapsed.current = 0;
          touchOrigin.current = null;
          setStep(0);
          updatePhase("idle");
          return;
        }

        const currentStep = Math.min(
          steps,
          Math.floor((elapsed.current / duration) * steps)
        );
        setStep((prev) => (prev === currentStep ? prev : currentStep));
        rafHandle.current = requestAnimationFrame(loop);
      };

      rafHandle.current = requestAnimationFrame(loop);
    },
    [disabled, duration, steps, releaseRate, haptic, updatePhase]
  );

  const release = useCallback(() => {
    if (phaseRef.current !== "holding") return;
    isDown.current = false;
    touchOrigin.current = null;
    updatePhase("releasing");
    abortCb.current?.();
  }, [updatePhase]);

  useEffect(() => {
    const handleBail = () => release();
    const handleVisibility = () => {
      if (document.hidden) release();
    };

    window.addEventListener("blur", handleBail);
    document.addEventListener("visibilitychange", handleVisibility);

    return () => {
      window.removeEventListener("blur", handleBail);
      document.removeEventListener("visibilitychange", handleVisibility);
      cancelAnimationFrame(rafHandle.current);
      rafHandle.current = 0;
    };
  }, [release]);

  const bind = {
    onPointerDown: (e: React.PointerEvent) => {
      if (e.pointerType === "mouse" && e.button !== 0) return;
      e.currentTarget.setPointerCapture?.(e.pointerId);
      begin({ x: e.clientX, y: e.clientY });
    },
    onPointerMove: (e: React.PointerEvent) => {
      const from = touchOrigin.current;
      if (phaseRef.current !== "holding" || !from) return;
      if (Math.hypot(e.clientX - from.x, e.clientY - from.y) > moveTolerance) {
        release();
      }
    },
    onPointerUp: release,
    onPointerCancel: release,
    onPointerLeave: release,
    onKeyDown: (e: React.KeyboardEvent) => {
      if (e.key === "Escape") {
        if (phaseRef.current === "holding" || phaseRef.current === "releasing") {
          e.preventDefault();
          reset();
        }
        return;
      }
      if (e.repeat) return;
      if (e.key === " " || e.key === "Enter") {
        e.preventDefault();
        begin();
      }
    },
    onKeyUp: (e: React.KeyboardEvent) => {
      if (e.key === " " || e.key === "Enter") release();
    },
    onBlur: release,
    onClick: (e: React.MouseEvent) => {
      e.preventDefault();
      if (phaseRef.current === "committed") e.stopPropagation();
    },
    onContextMenu: (e: React.MouseEvent) => e.preventDefault(),
  };

  return {
    bind,
    step,
    steps,
    phase,
    progress: step / steps,
    reset,
  };
}

export type HoldToConfirmProps = {
  onConfirm: () => void;
  children: React.ReactNode;
  onAbort?: () => void;
  confirmLabel?: string;
  duration?: number;
  resetAfter?: number;
  steps?: number;
  releaseRate?: number;
  disabled?: boolean;
  className?: string;
};

/**
 * Componente Visual estilizado com máscara vetorial e compatibilidade dark/light mode
 */
export function HoldToConfirm({
  onConfirm,
  children,
  onAbort,
  confirmLabel = "Confirmed",
  duration = 1800,
  resetAfter = 1600,
  steps = 20,
  releaseRate = 2.5,
  disabled = false,
  className = "",
}: HoldToConfirmProps) {
  const { bind, phase, reset } = useHoldToConfirm({
    onConfirm,
    onAbort,
    duration,
    steps,
    releaseRate,
    disabled,
  });

  const reducedMotion = useReducedMotion();
  const hintId = useId();
  const isCommitted = phase === "committed";
  const secondsDisplay = Math.round(duration / 100) / 10;

  const sweptProgress = useMotionValue(0);
  const clipMask = useTransform(
    sweptProgress,
    (v) => `inset(0 ${(1 - v) * 100}% 0 0)`
  );

  useEffect(() => {
    if (phase !== "committed" || resetAfter <= 0) return;
    const timeout = setTimeout(reset, resetAfter);
    return () => clearTimeout(timeout);
  }, [phase, resetAfter, reset]);

  useEffect(() => {
    if (reducedMotion) {
      sweptProgress.set(phase === "holding" || phase === "committed" ? 1 : 0);
      return;
    }

    if (phase === "committed") {
      const controls = animate(sweptProgress, 1, { duration: 0.12, ease: "linear" });
      return () => controls.stop();
    }

    const currentVal = sweptProgress.get();

    if (phase === "holding") {
      const controls = animate(sweptProgress, 1, {
        duration: (duration * (1 - currentVal)) / 1000,
        ease: "linear",
      });
      return () => controls.stop();
    }

    // Fase de liberação / aborto antecipado
    const controls = animate(sweptProgress, 0, {
      duration: (duration * currentVal) / releaseRate / 1000,
      ease: [0.23, 1, 0.32, 1],
    });
    return () => controls.stop();
  }, [phase, duration, releaseRate, reducedMotion, sweptProgress]);

  return (
    <button
      type="button"
      aria-disabled={disabled || isCommitted}
      aria-describedby={hintId}
      {...bind}
      style={{ touchAction: "manipulation", WebkitTouchCallout: "none" }}
      className={`relative isolate inline-grid h-10 select-none place-items-center overflow-hidden rounded-[9px] border border-stone-200 bg-white px-4 text-[13px] font-medium text-stone-700 outline-none focus-visible:ring-2 focus-visible:ring-stone-400 dark:border-white/[0.16] dark:bg-[#1D1D1A] dark:text-stone-200 dark:focus-visible:ring-stone-500 ${
        disabled ? "cursor-not-allowed opacity-50" : "cursor-pointer"
      } ${className}`}
    >
      {/* Camada de repouso padrão */}
      <LabelFaces committed={isCommitted} confirmLabel={confirmLabel}>
        {children}
      </LabelFaces>

      {/* Camada ativa revelada pela máscara de corte */}
      <motion.span
        aria-hidden
        style={{ clipPath: clipMask }}
        className="absolute inset-0 grid place-items-center bg-stone-800 px-4 text-white dark:bg-stone-100 dark:text-stone-900"
      >
        <LabelFaces committed={isCommitted} confirmLabel={confirmLabel}>
          {children}
        </LabelFaces>
      </motion.span>

      {/* Instruções acessíveis para leitor de tela */}
      <span id={hintId} className="sr-only">
        Mantenha pressionado por {secondsDisplay} segundos para confirmar. Soltar antes cancela a ação.
      </span>
      <span role="status" aria-live="polite" className="sr-only">
        {isCommitted ? confirmLabel : ""}
      </span>
    </button>
  );
}

function LabelFaces({
  committed,
  confirmLabel,
  children,
}: {
  committed: boolean;
  confirmLabel: string;
  children: React.ReactNode;
}) {
  return (
    <span className="col-start-1 row-start-1 grid">
      <motion.span
        initial={false}
        animate={{ opacity: committed ? 0 : 1 }}
        transition={FACE_SPRING}
        className="col-start-1 row-start-1 flex items-center justify-center whitespace-nowrap"
      >
        {children}
      </motion.span>
      <motion.span
        initial={false}
        animate={{ opacity: committed ? 1 : 0 }}
        transition={FACE_SPRING}
        className="col-start-1 row-start-1 flex items-center justify-center gap-1.5 whitespace-nowrap"
      >
        <svg
          width="12"
          height="12"
          viewBox="0 0 12 12"
          fill="none"
          stroke="currentColor"
          strokeWidth="1.7"
          strokeLinecap="round"
          strokeLinejoin="round"
          aria-hidden="true"
        >
          <path d="M2.5 6.4 4.7 8.6 9.5 3.5" />
        </svg>
        {confirmLabel}
      </motion.span>
    </span>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar ou estender uma aplicação com base nos princípios do Interior.dev, o agente de arquitetura de UI deve obedecer às seguintes diretrizes:

1. **Declaração Explícita de Regra de Ausência de Layout Shift**:
   - Todo componente com múltiplos estados visuais (ex: botões assíncronos, painéis expansíveis, filtros de dados) **deve** usar a estratégia de grid sobreposto (`col-start-1 row-start-1`) ou `min-w` baseado no maior rótulo possível, impedindo oscilação de largura durante estados transitórios.
2. **Separação Obrigatória entre Lógica (Hook) e Visual (Tailwind)**:
   - Nunca embutir a máquina de estados diretamente nas tags visuais. Crie ou importe o hook headless correspondente (`useHoldToConfirm`, `useAsyncAction`, `useDetentSlider`), mantendo a lógica de pointer-capture, timers e haptics testável e reutilizável.
3. **Parametrização Estrita de Física Spring**:
   - Utilize rigorosamente as constantes `CELL_SPRING` (`stiffness: 520, damping: 34, mass: 0.45`) para componentes táticos e `FACE_SPRING` (`stiffness: 260, damping: 34, mass: 0.8`) para mutações de rótulo e ícones. Curvas lineares ou eases lentos são proibidos na camada de feedback tátil.
4. **Respeito aos Critérios de Acessibilidade & Reduced Motion**:
   - Quando `useReducedMotion()` retornar verdadeiro, **não remova o componente nem o texto**. Substitua a transição de mola por `{ duration: 0 }`, mantendo todos os spans acessíveis `.sr-only` e atributos ARIA intactos.
5. **Combinação Harmoniosa no Design System**:
   - Integre o Interior.dev como a camada de **30% de micro-feedback** sobre uma base de Shadcn UI ou Radix UI (60%). Deixe efeitos de alto impacto luminoso (10%) para a dobra Hero de bibliotecas como 21st.dev ou Magic UI.
