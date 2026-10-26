---
id: "microkit-co"
name: "MicroKit UI"
url: "https://microkit.co/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Micro-Interaction Craft", "Tactile Physics & Springs", "Precision Dark & Light Tokens", "Zero-Bloat Vanilla Tailwind", "Official shadcn Registry"]
densidade_informacao: "Media"
impacto_visual: "Moderado"
custo_computacional: "Baixo a Medio (CSS Hardware-Accelerated / rAF Springs)"
stack_frameworks: ["React 19 / 18", "Next.js (App Router)", "Tailwind CSS v3 / v4", "shadcn/ui Registry CLI", "Lucide React", "Native CSS & rAF"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Geist Mono", "Inter", "Plus Jakarta Sans", "SF Pro Display"]
  paletas_ideais: ["Deep Zinc / Obsidian Dark (#0b0c0e, #121418)", "Pure Crisp Light (#ffffff, #f0f2f5)", "Tactile Orange / Amber Accent (#f97316)", "Emerald / Forest Success (#22c55e)"]
  combinacoes_recomendadas: ["shadcn/ui", "Radix UI", "OriginKit", "Magic UI", "Cult UI"]
  conflitos_esteticos: ["Neubrutalism cru de bordas pretas grossas", "Skeuomorfismo pesado pré-flat com texturas de couro", "Flat design estático sem qualquer transição de estado"]
---

# MicroKit UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **MicroKit UI** (`microkit.co`), concebido e desenvolvido por Henrique Barone, estabelece-se como o catálogo de referência na vanguarda das **microinterações táteis de alta precisão** para a web moderna. Sob a premissa de que *"Details Matter!"*, a biblioteca ataca frontalmente um dos sintomas mais comuns do desenvolvimento contemporâneo: interfaces visualmente polidas mas táteis-estáticas, onde botões e controles parecem pedaços inertes de vidro ou papelão digital que apenas trocam de cor ao hover sem transmitir peso, tração, inércia ou confirmação orgânica.

Enquanto repositórios genéricos dependem de frameworks de animação massivos ou implementam transições CSS lineares genéricas (`transition: all 0.2s ease`), o MicroKit constrói sua assinatura visual sobre cinco pilares fundamentais:

1. **Física Tátil e Feedback Mecânico de Intencionalidade**:
   Cada interação possui uma curva de resposta cinemática deliberada. Ações comuns (como selecionar uma aba ou passar o mouse por um botão) respondem com curvas de aceleração orgânicas (`cubic-bezier(.16, 1, .3, 1)`, a mesma curva de desaceleração suave utilizada pela Apple em transições nativas do iOS). Ações destrutivas ou de confirmação crítica introduzem resistência deliberada — como o *Hold to Delete Button*, que exige uma compressão temporal contínua de 1600ms enquanto uma barra translúcida preenche a superfície com um brilho ascendente e recua imediatamente (*snap-back*) caso o usuário solte o cursor antes da conclusão.

2. **Engenharia Matemática via Spring Physics em `requestAnimationFrame`**:
   Para componentes com rastreamento contínuo de ponteiro (como o *Cursor Edge Glow Button*), o MicroKit rejeita o custo proibitivo de re-renderizações cíclicas do React. Em vez disso, utiliza um oscilador harmônico amortecido em JavaScript nativo rodando dentro de um loop de `requestAnimationFrame` (`FREQUENCY = 3.4`, `DAMPING = 0.78`), atualizando propriedades customizadas no CSS (`--light-x`) diretamente no nó do DOM via `style.setProperty`. O resultado é uma taxa de quadros travada em 60/120 FPS com custo computacional mínimo.

3. **Arquitetura Bimodal Nativa com CSS `light-dark()`**:
   Em vez de depender de seletores de classe duplicados em cascata (`.dark:bg-slate-900 .dark:text-white`), o MicroKit adota a especificação moderna de cores do CSS com `light-dark(#ffffff, #121418)` embutida nas classes de utilitário do Tailwind. Isso garante paridade cromática impecável e alternância instantânea de tema no cliente sem flickers de renderização ou cálculos de re-layout.

4. **Zero-Bloatware & Filosofia Copy-Paste MIT**:
   Nenhum pacote npm proprietário pesado é necessário para usar o MicroKit. Cada componente é autocontido, utilizando React vanilla hooks (`useState`, `useRef`, `useEffect`), classes do Tailwind CSS e ícones do `lucide-react`. O MicroKit é distribuído oficialmente através do **shadcn CLI Registry** (`npx shadcn@latest add @microkit/<component-name>`), permitindo que a equipe de engenharia inspecione, customize e mantenha a propriedade total do código-fonte.

5. **Acessibilidade Universal & Proteção Vestibular (`prefers-reduced-motion`)**:
   Diferente de experimentações criativas que desrespeitam regras de usabilidade, todo componente do MicroKit possui suporte explícito à acessibilidade: classes `motion-reduce:transition-none` desativam transições espaciais para usuários com sensibilidade vestibular, eventos de teclado (`Enter`, `Space`) possuem proteção contra repetição involuntária de buffer (`event.repeat`), e rótulos de acessibilidade semântica (`aria-label`, `aria-hidden`, `aria-live="polite"`, `role="checkbox"`) são rigorosamente incorporados.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
- **SaaS B2B & DevTools de Alta Produtividade (Linear, Raycast, Vercel, Supabase)**:
  Plataformas voltadas a desenvolvedores e profissionais digitais exigem ferramentas que respondam com velocidade e feedback tátil refinado. O MicroKit transmite sofisticação artesanal ("craft") imediata, elevando a percepção de estabilidade e valor do produto.
- **Ferramentas Criativas, Modelagem & Design Systems (Figma, Spline, Rive, Framer)**:
  Controles como o *Scrub Number Field* (ajuste numérico por arraste horizontal com inércia e acelerômetro visual) trazem para a web o comportamento de editores gráficos profissionais, eliminando a digitação manual redundante.
- **Fintechs, Portais de Investimento & Gateways de Pagamento Seguro**:
  Ações financeiras que envolvem movimentação de capital ou contratação de planos anuais ganham segurança psicológica com o *Secure Purchase Button*, *Progress Ring Check* e *Fuse Undo Button*, substituindo modais intrusivos por microconfirmações visuais elegantes.
- **Interfaces de IA Generativa & Agentes Autônomos**:
  Para acionar execuções caras de modelos de linguagem ou exclusão de pipelines de agentes, botões com feedback de carregamento em anel ou retenção evitam disparos acidentais de tokens.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Estrutural Neutra)**:
  Layouts limpos baseados em shadcn/ui e Tailwind CSS, fundos em deep zinc (`#0b0c0e` em dark mode, `#f9fafb` em light mode), malhas tipográficas com `Geist Sans` ou `Inter`, e espaçamentos utilitários padrão.
- **30% (Camada Tátil MicroKit — Protagonista Operacional)**:
  O MicroKit é **a biblioteca quintessencial para a camada de 30%**. Ele preenche exatamente a lacuna entre os blocos estruturais estáticos e os grandes efeitos decorativos: abas que deslizam magneticamente (*Blur Glide Menu*), botões de ação com crossfade de ícone, checkboxes com física de pulso (*Bounce Checkbox*) e inputs com microbordas dinâmicas de foco.
- **10% (Showstoppers Focalizados)**:
  Reservado para o *Cursor Edge Glow Button* ou *Aurora Download Button* aplicado como o único e definitivo Call-To-Action da tela de boas-vindas, e o *Hold to Delete Button* como barreira tátil máxima de destruição em gavetas ou modais de configurações.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

- ⚠️ **Proibido em Aplicações de Densidade Numérica Extrema (Bloomberg Terminals, ERPs Maciços)**:
  Em telas com grades de dados exibindo centenas de células e dezenas de botões por centímetro quadrado, adicionar efeitos de rastreamento de cursor por mola e sombras reativas gera poluição visual, satura o processamento da thread de animação e distrai o operador financeiro.
- ⚠️ **Proibido em Ações Triviais e Repetitivas de Alta Frequência**:
  Nunca aplique o *Hold to Delete Button* para fechar abas de navegação, remover filtros temporários de busca ou apagar itens de um rascunho rápido. Obrigar o usuário a reter o clique por 1.6 segundos em tarefas triviais causa atrito cognitivo e irritabilidade aguda.
- ⚠️ **Erros Comuns de Exagero (Anti-Padrões)**:
  - **Sobrecarga de Glows Concorrentes**: Ter mais de um botão com rastreamento luminoso (*Cursor Edge Glow*) no mesmo campo de visão divide a atenção e desvaloriza a hierarquia da página.
  - **Quebra de Consistência nos Tempos de Retenção**: Se um projeto adotar *Hold to Delete*, mantenha rigorosamente a constante temporal padrão de 1600ms (`HOLD_MS = 1600`) em todas as instâncias da aplicação. Modificar a duração de forma arbitrária entre telas quebra a memória muscular do usuário.
  - **Inclusão em Ambientes Sem Suporte a Pointer Events**: Embora funcione com toque mobile (`PointerEvent`), microinterações baseadas em hover e rastreamento de cursor contínuo perdem seu brilho em dispositivos estritamente touch se não houver adaptação de estado ativo.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

O catálogo oficial do MicroKit conta com mais de 54 microinterações especializadas. Abaixo detalham-se os 12 componentes mais emblemáticos para a engenharia de software moderno:

### 1. Cursor Edge Glow Button
- **Anatomia Visual**: Botão em formato de pílula escura com iluminação de borda espelhada. Ao aproximar o mouse, um feixe interno de fótons segue horizontalmente as coordenadas do ponteiro enquanto uma auréola periférica (*rim glow*) acende na borda oposta via reflexão óptica simulada.
- **Gatilho de Interação**: `PointerMove` com interpolação física por oscilador harmônico (Spring math) em `requestAnimationFrame`.
- **Onde encaixar na página**: Hero CTA principal de produtos SaaS premium ou botão de checkout final.

### 2. Hold to Delete Button
- **Anatomia Visual**: Botão arredondado com ícone de lixeira (`Trash2`) e texto "Hold to delete". Ao pressionar continuamente, uma camada interna laranja vibrante preenche a superfície da esquerda para a direita via máscara `clip-path: inset(0 100% 0 0) -> inset(0)`. Se completado, o ícone e o texto realizam um morphing instantâneo para um `Check` e "Deleted" acompanhados de uma onda de choque expansiva (`@keyframes hold-delete-pulse`).
- **Gatilho de Interação**: `PointerDown` / `PointerUp` contínuo por 1600ms, com suporte a `Space` e `Enter` no teclado.
- **Onde encaixar na página**: Modais de exclusão permanente de repositórios, cancelamento de assinaturas ou exclusão de bancos de dados.

### 3. Fuse Undo Button
- **Anatomia Visual**: Pílula compacta de ação rápida (ex: "Archive"). Ao clicar, o estado muda imediatamente para "Undo" enquanto a borda do botão — construída através de um retângulo SVG com `stroke-dasharray` calibrado — queima progressivamente como um pavio aceso (*burning fuse*), permitindo que o usuário clique em desfazer antes que o pavio expire.
- **Gatilho de Interação**: Clique inicial disparando temporizador visual de contagem regressiva linear vetorial.
- **Onde encaixar na página**: Barra de status de ações de caixa de entrada, painéis de e-mail e gerenciadores de arquivos.

### 4. Scrub Number Field
- **Anatomia Visual**: Campo numérico refinado que substitui os spinners tradicionais do HTML. Ao posicionar o cursor sobre o rótulo ou o campo e arrastar para os lados, o cursor muda para um indicador bidirecional e o valor numérico é incrementado ou decrementado suavemente com aceleração proporcional à velocidade de arraste.
- **Gatilho de Interação**: `PointerDown` + `Drag Horizontal` com captura de ponteiro (`setPointerCapture`).
- **Onde encaixar na página**: Inspetores laterais de propriedades, editores de CSS/dimensões, controles de opacidade e dashboards de configuração de IA (temperatura, top_p).

### 5. Progress Ring Check
- **Anatomia Visual**: Linhas de checklist minimalistas contendo um anel de progresso circular SVG de 22px (`--prc-size: 22px`). O anel suporta estados tridimensionais: `pending` (borda fina cinza), `running` (arco girando com gradiente) e `done` (anel fechando em verde esmeralda com animação vetorial do checkmark e linha de corte estendendo-se sobre a tipografia).
- **Gatilho de Interação**: Clique direto ou disparo de evento assíncrono via props.
- **Onde encaixar na página**: Onboarding checklists, etapas de deploy contínuo, verificação de ambiente e tarefas diárias.

### 6. Bounce Checkbox
- **Anatomia Visual**: Caixa de marcação quadrada com bordas levemente suavizadas (`rounded-[9px]`). Ao ser acionada, a superfície sofre uma compressão rápida para `scale(0.85)` seguida de uma distensão elástica para `scale(1.08)` e assentamento em `scale(1)`, enquanto o traço do checkmark é desenhado via `stroke-dashoffset: 0` e uma linha de strike-through corta o texto.
- **Gatilho de Interação**: Clique do mouse ou ativação por barra de espaço.
- **Onde encaixar na página**: Formulários de cadastro avançado, concordância de termos de uso e to-do lists integradas a dashboards.

### 7. Cursor Follow Share Button
- **Anatomia Visual**: Botão com bordas circulares contendo um ícone de compartilhamento/flecha que habita uma órbita gravitacional magnética. O ícone se desloca em relação ao centro acompanhando o ângulo do cursor enquanto a tipografia desliza suavemente em um stack de crossfade.
- **Gatilho de Interação**: `PointerEnter` e `PointerMove` delimitados pelo raio de influência do elemento.
- **Onde encaixar na página**: Barras de compartilhamento em blogs técnicos, páginas de documentação e botões de convite em SaaS colaborativos.

### 8. Focus Field / Focus Input
- **Anatomia Visual**: Campo de entrada tipográfico ultra-minimalista. Ao receber foco, uma borda interior de 1px acende com gradiente sutil enquanto uma sutil iluminação difusa envolve o contorno sem gerar qualquer tremor de layout (*zero layout shift*). O placeholder se dissolve enquanto uma indicação de atalho de teclado (`⌘K`) se transforma em ícone de ação.
- **Gatilho de Interação**: `FocusVisible` / `Blur`.
- **Onde encaixar na página**: Barras de busca global em navbars, modais de command-palette e formulários de login.

### 9. Blur Glide Menu
- **Anatomia Visual**: Barra de navegação flutuante onde a pílula de seleção ativa consiste em uma camada com `backdrop-blur-md` e borda translúcida que desliza suavemente entre os links de menu através de transições com física de mola, evitando que a pílula "teleporte" entre os itens.
- **Gatilho de Interação**: `PointerEnter` e clique de seleção em rotas.
- **Onde encaixar na página**: Header principal, barras de navegação secundária em dashboards e filtros de catálogo.

### 10. Expanding Icon Tabs
- **Anatomia Visual**: Grupo de abas compacto que, em seu estado de repouso, exibe apenas os glifos de ícone minimalistas. Ao selecionar ou passar o cursor sobre uma aba, o container se expande horizontalmente de forma suave, revelando o rótulo tipográfico correspondente sem quebrar o alinhamento das abas vizinhas.
- **Gatilho de Interação**: `Click` e `Hover` com interpolação de largura e opacidade.
- **Onde encaixar na página**: Barras laterais retráteis, seletores de modo em editores e barras inferiores mobile.

### 11. Sliding Content Tabs
- **Anatomia Visual**: Sistema de abas com duas camadas sincronizadas: um indicador inferior deslizante (*sliding underline*) que se move sob o texto ativo, e um container de painel de conteúdo que realiza um fade-slide imperceptível ao trocar de contexto.
- **Gatilho de Interação**: Clique direto do usuário.
- **Onde encaixar na página**: Seções de Pricing (Alternância Mensal / Anual), abas de configurações de conta e documentação de APIs.

### 12. Aurora Download Button
- **Anatomia Visual**: Botão de alta conversão envelopado por um gradiente iridescente dinâmico (tons de azul ciano, violeta e esmeralda) que se desloca lentamente ao longo de uma máscara elíptica, criando a ilusão ótica de luzes polares em movimento sob uma superfície fosca de vidro negro.
- **Gatilho de Interação**: Hover e repouso com gradiente CSS infinito animado por GPU.
- **Onde encaixar na página**: Botão de download de instalador desktop (Electron/Tauri/Mac), botão de checkout premium ou call-to-action em páginas de produto de inteligência artificial.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

O MicroKit integra-se perfeitamente ao ecossistema moderno do React através do shadcn CLI. Para adicionar qualquer componente do MicroKit:

```bash
# Instalação automatizada via shadcn CLI oficial
npx shadcn@latest add @microkit/hold-to-delete-button
npx shadcn@latest add @microkit/cursor-edge-glow-button
```

Para instalação manual, as dependências são mínimas:
```bash
npm install lucide-react clsx tailwind-merge
```

### Física de Movimento, Curvas de Transição & Equações de Mola

O MicroKit padroniza suas transições em dois modelos matemáticos rigorosos:

1. **Curva Bezier de Alta Desaceleração (Apple Spring Easing)**:
   ```css
   cubic-bezier(0.16, 1, 0.3, 1)
   ```
   Esta curva atinge 80% do seu percurso nos primeiros 20% do tempo total da animação, gerando sensação imediata de resposta tátil enquanto suaviza milimetricamente a chegada ao destino final.

2. **Equação do Oscilador Harmônico Amortecido (Spring Math em JS)**:
   Utilizado em componentes como o `CursorEdgeGlowButton` para rastreamento de ponteiro:
   ```typescript
   // Parâmetros de física harmônica do MicroKit
   const FREQUENCY = 3.4; // Rigidez natural do movimento da mola
   const DAMPING = 0.78;  // Fator de amortecimento subcrítico (evita tremores)

   // Integração de Euler executada a cada frame do rAF:
   const dt = Math.min((currentTime - lastTime) / 1000, 0.032);
   const force = (targetX - currentX) * (FREQUENCY * FREQUENCY);
   const drag = 2 * DAMPING * FREQUENCY * velocity;
   velocity += (force - drag) * dt;
   currentX += velocity * dt;
   ```

---

### Receita de Código Funcional 1: `HoldToDeleteButton` (Completo & Pronto para Produção)

Implementação autônoma do botão de retenção destrutiva com teclado acessível, pulso vetorial e animação por máscara `clip-path`:

```tsx
"use client";

import { Check, Trash2 } from "lucide-react";
import { useEffect, useState, useRef } from "react";
import type { KeyboardEvent, PointerEvent } from "react";

type DeleteState = "idle" | "holding" | "deleted";

interface HoldToDeleteButtonProps {
  onConfirm?: () => void;
  holdDurationMs?: number;
  label?: string;
  confirmedLabel?: string;
  className?: string;
}

const pulseKeyframes = `
@keyframes hold-delete-pulse {
  from { outline: 1px solid rgba(249, 115, 22, 0.9); outline-offset: 0px; }
  to { outline: 1px solid rgba(249, 115, 22, 0); outline-offset: 14px; }
}
`;

function ButtonContent({ deleted, label, confirmedLabel }: { deleted: boolean; label: string; confirmedLabel: string }) {
  return (
    <span className="inline-flex items-center gap-[10px] select-none">
      <span className="grid shrink-0" aria-hidden="true">
        <Trash2
          className="[grid-area:1/1] [transition:opacity_.24s_ease,transform_.32s_cubic-bezier(.16,1,.3,1)] data-[active=false]:opacity-0 data-[active=false]:[transform:scale(.5)] motion-reduce:transition-none"
          data-active={!deleted}
          size={20}
          strokeWidth={2}
        />
        <Check
          className="[grid-area:1/1] [transition:opacity_.24s_ease,transform_.32s_cubic-bezier(.16,1,.3,1)] data-[active=false]:opacity-0 data-[active=false]:[transform:scale(.5)] motion-reduce:transition-none"
          data-active={deleted}
          size={20}
          strokeWidth={2.4}
        />
      </span>
      <span className="grid">
        <span
          className="justify-self-start whitespace-nowrap [grid-area:1/1] [transition:opacity_.24s_ease,transform_.32s_cubic-bezier(.16,1,.3,1),filter_.24s_ease,visibility_.24s] data-[active=false]:invisible data-[active=false]:opacity-0 data-[active=false]:[transform:translateY(6px)] data-[active=false]:[filter:blur(2px)] motion-reduce:transition-none"
          data-active={!deleted}
        >
          {label}
        </span>
        <span
          className="justify-self-start whitespace-nowrap [grid-area:1/1] [transition:opacity_.24s_ease,transform_.32s_cubic-bezier(.16,1,.3,1),filter_.24s_ease,visibility_.24s] data-[active=false]:invisible data-[active=false]:opacity-0 data-[active=false]:[transform:translateY(6px)] data-[active=false]:[filter:blur(2px)] motion-reduce:transition-none"
          data-active={deleted}
        >
          {confirmedLabel}
        </span>
      </span>
    </span>
  );
}

export function HoldToDeleteButton({
  onConfirm,
  holdDurationMs = 1600,
  label = "Hold to delete",
  confirmedLabel = "Deleted",
  className = "",
}: HoldToDeleteButtonProps) {
  const [state, setState] = useState<DeleteState>("idle");
  const onConfirmRef = useRef(onConfirm);
  onConfirmRef.current = onConfirm;

  useEffect(() => {
    if (state === "idle") return;

    if (state === "holding") {
      const timer = window.setTimeout(() => {
        setState("deleted");
        if (onConfirmRef.current) {
          onConfirmRef.current();
        }
      }, holdDurationMs);
      return () => window.clearTimeout(timer);
    }

    if (state === "deleted") {
      const resetTimer = window.setTimeout(() => {
        setState("idle");
      }, 2000);
      return () => window.clearTimeout(resetTimer);
    }
  }, [state, holdDurationMs]);

  const startHolding = () => setState((curr) => (curr === "idle" ? "holding" : curr));
  const cancelHolding = () => setState((curr) => (curr === "holding" ? "idle" : curr));

  const handlePointerDown = (e: PointerEvent<HTMLButtonElement>) => {
    if (e.button === 0) startHolding();
  };

  const handleKeyDown = (e: KeyboardEvent<HTMLButtonElement>) => {
    if (e.key !== " " && e.key !== "Enter") return;
    e.preventDefault();
    if (!e.repeat) startHolding();
  };

  const handleKeyUp = (e: KeyboardEvent<HTMLButtonElement>) => {
    if (e.key === " " || e.key === "Enter") cancelHolding();
  };

  return (
    <>
      <style>{pulseKeyframes}</style>
      <button
        type="button"
        data-state={state}
        onPointerDown={handlePointerDown}
        onPointerUp={cancelHolding}
        onPointerLeave={cancelHolding}
        onPointerCancel={cancelHolding}
        onKeyDown={handleKeyDown}
        onKeyUp={handleKeyUp}
        onBlur={cancelHolding}
        onContextMenu={(e) => e.preventDefault()}
        className={`group relative inline-flex h-[52px] cursor-pointer appearance-none items-center justify-center overflow-hidden rounded-full border-0 px-[24px] text-[16px] font-medium tracking-tight text-[light-dark(#14181e,#f2f4f6)] bg-[light-dark(#ffffff,#121418)] [box-shadow:inset_0_0_0_1px_light-dark(#dfe3ea,#2b2f36),0_8px_20px_light-dark(rgba(0,0,0,.06),rgba(0,0,0,.35))] [transition:transform_.25s_cubic-bezier(.16,1,.3,1),background-color_.2s_ease,box-shadow_.5s_cubic-bezier(.16,1,.3,1)] hover:data-[state=idle]:bg-[light-dark(#f4f6f8,#1b1e23)] motion-safe:data-[state=holding]:[transform:scale(.97)] data-[state=deleted]:cursor-default motion-safe:data-[state=deleted]:[animation:hold-delete-pulse_.8s_cubic-bezier(.16,1,.3,1)] focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-[#f97316] select-none touch-manipulation motion-reduce:transition-none ${className}`}
        aria-label={state === "deleted" ? confirmedLabel : label}
      >
        {/* Camada Neutra Inferior */}
        <ButtonContent deleted={state === "deleted"} label={label} confirmedLabel={confirmedLabel} />

        {/* Camada Ativa de Preenchimento e Alerta (Clip-Path progressivo) */}
        <span
          className="pointer-events-none absolute inset-0 flex items-center justify-center bg-[#f97316] text-white [clip-path:inset(0_100%_0_0)] [transition:clip-path_.4s_cubic-bezier(.16,1,.3,1)] group-data-[state=holding]:[clip-path:inset(0)] group-data-[state=holding]:[transition:clip-path_1.6s_linear] group-data-[state=deleted]:[clip-path:inset(0)] motion-reduce:group-data-[state=idle]:[transition:none] motion-reduce:group-data-[state=deleted]:[transition:none]"
          aria-hidden="true"
        >
          <ButtonContent deleted={state === "deleted"} label={label} confirmedLabel={confirmedLabel} />
        </span>
      </button>
    </>
  );
}
```

---

### Receita de Código Funcional 2: `CursorEdgeGlowButton` (Simulador Físico rAF)

Implementação do botão luminoso de ponta a ponta com oscilação harmônica e propriedades dinâmicas:

```tsx
"use client";

import { useEffect, useRef } from "react";
import type { PointerEvent, ReactNode } from "react";

interface CursorEdgeGlowButtonProps {
  children?: ReactNode;
  onClick?: () => void;
  className?: string;
}

const FREQUENCY = 3.4;
const DAMPING = 0.78;

export function CursorEdgeGlowButton({
  children = "See in Action",
  onClick,
  className = "",
}: CursorEdgeGlowButtonProps) {
  const containerRef = useRef<HTMLDivElement>(null);
  const lightTrackRef = useRef<HTMLSpanElement>(null);
  const animationFrameRef = useRef<number | null>(null);

  useEffect(() => {
    const container = containerRef.current;
    const lightTrack = lightTrackRef.current;
    if (!container || !lightTrack) return;

    let bound = container.getBoundingClientRect().width / 2 + 12;
    let x = bound;
    let velocity = 0;
    let target = bound;
    let inside = false;
    let lastTime = 0;

    const measure = () => {
      bound = container.getBoundingClientRect().width / 2 + 12;
    };

    const paint = () => {
      lightTrack.style.setProperty("--light-x", `${x.toFixed(2)}px`);
    };

    const tick = (now: number) => {
      if (!lastTime) lastTime = now;
      const dt = Math.min((now - lastTime) / 1000, 0.033);
      lastTime = now;

      // Cálculo do Oscilador Harmônico
      const force = (target - x) * (FREQUENCY * FREQUENCY);
      const drag = 2 * DAMPING * FREQUENCY * velocity;
      velocity += (force - drag) * dt;
      x += velocity * dt;

      paint();

      const settled = !inside && Math.abs(velocity) < 0.2 && Math.abs(target - x) < 0.2;
      if (!settled) {
        animationFrameRef.current = requestAnimationFrame(tick);
      } else {
        x = target;
        velocity = 0;
        paint();
        animationFrameRef.current = null;
      }
    };

    const startLoop = () => {
      if (animationFrameRef.current === null) {
        lastTime = performance.now();
        animationFrameRef.current = requestAnimationFrame(tick);
      }
    };

    const handlePointerMove = (e: globalThis.PointerEvent) => {
      inside = true;
      const rect = container.getBoundingClientRect();
      target = e.clientX - rect.left;
      startLoop();
    };

    const handlePointerLeave = () => {
      inside = false;
      target = bound;
      startLoop();
    };

    container.addEventListener("pointermove", handlePointerMove);
    container.addEventListener("pointerleave", handlePointerLeave);
    window.addEventListener("resize", measure);

    measure();
    paint();

    return () => {
      container.removeEventListener("pointermove", handlePointerMove);
      container.removeEventListener("pointerleave", handlePointerLeave);
      window.removeEventListener("resize", measure);
      if (animationFrameRef.current !== null) {
        cancelAnimationFrame(animationFrameRef.current);
      }
    };
  }, []);

  return (
    <div
      ref={containerRef}
      className={`relative inline-flex items-center justify-center p-[2px] rounded-full overflow-hidden [contain:paint] select-none ${className}`}
    >
      {/* Auréola de Glow Periférico */}
      <span
        ref={lightTrackRef}
        className="pointer-events-none absolute inset-0 -z-10 rounded-full transition-opacity duration-300 [background:radial-gradient(120px_circle_at_var(--light-x,_50%)_50%,rgba(249,115,22,0.45),transparent_70%)]"
        aria-hidden="true"
      />

      {/* Botão Frontal Tátil */}
      <button
        type="button"
        onClick={onClick}
        className="relative z-10 flex h-[48px] items-center gap-2 rounded-full bg-[light-dark(#ffffff,#0e1013)] px-6 text-[15px] font-medium tracking-tight text-[light-dark(#121417,#f1f3f5)] shadow-sm border border-[light-dark(#e2e6eb,#22262d)] transition-transform duration-200 active:scale-[0.98] hover:border-[#f97316]/50 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-[#f97316]"
      >
        <span>{children}</span>
        <svg
          className="h-3.5 w-3.5 transition-transform duration-200 group-hover:translate-x-0.5"
          viewBox="0 0 17 9"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill="currentColor"
            fillRule="evenodd"
            d="m12.495 0 4.495 4.495-4.495 4.495-.99-.99 2.805-2.805H0v-1.4h14.31L11.505.99z"
            clipRule="evenodd"
          />
        </svg>
      </button>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao conceber a arquitetura técnica de uma nova interface no documento `DESIGN_BLUEPRINT.md`, a inteligência artificial deve seguir as seguintes diretrizes para especificar e declarar componentes baseados no MicroKit UI:

1. **Declaração Formal de Registro e Escopo**:
   - Mapeie o MicroKit como o **provedor primário de microinterações táteis e feedback mecânico** da camada de 30% da regra 60-30-10.
   - Organize os componentes na pasta `@/components/ui/microkit/` ou instale via shadcn CLI sob `@microkit/*`.

2. **Convenções de Estados e Atributos HTML `data-[state]`**:
   - Utilize semântica orientada a dados em vez de classes condicionais caóticas. Componentes interativos do MicroKit devem operar estritamente via atributos `data-state="idle" | "holding" | "deleted" | "running" | "pending" | "done"`, permitindo que o CSS e o Tailwind modulem os seletores com clareza declarativa (`data-[state=holding]:...`).

3. **Padronização Temporal e Regra de Memória Muscular**:
   - Para interações de confirmação crítica por retenção (*Hold to Delete*), fixe a constante `HOLD_MS` impreterivelmente em **1600ms**. Nunca reduza para menos de 1000ms (risco de falso positivo por clique longo) nem aumente para mais de 2200ms (fadiga tátil do usuário).
   - Para animações de transição espacial e morphing de ícones, aplique a curva `cubic-bezier(.16, 1, .3, 1)` com duração balizada entre **240ms e 320ms**.

4. **Diretriz de Cores e Suporte Bimodal (`light-dark()`)**:
   - Assegure que os estilos globais suportem tokens bimodais nativos ou configure o Tailwind para resolver classes com suporte estrito a `color-scheme: dark light`. O fundo dos botões táteis deve navegar entre `#ffffff` (light mode) e `#121418` / `#0b0c0e` (dark mode), com contornos em `#dfe3ea` / `#2b2f36` e acentos táteis no tom `#f97316` (laranja de alta visibilidade) ou `#22c55e` (verde de confirmação).

5. **Cláusula Inegociável de Acessibilidade Vestibular**:
   - No blueprint, estipule que qualquer componente com transformações espaciais ou animações contínuas contenha as classes `motion-reduce:transition-none` e `motion-reduce:[animation:none]`. Se o usuário possuir a flag do sistema operacional ativa para redução de movimento, o feedback deve ser instantâneo e discreto, preservando o conforto neurológico.
