---
id: "bencho-dev"
name: "Bencho.dev"
url: "https://bencho.dev/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Playful Tactility & Haptic Micro-Interactions", "Skeuomorphic Motion & Physics-Driven UI", "Sensory Audio-Visual Feedback (Web Audio API)", "Craft Digital & Organic Fluidity"]
densidade_informacao: "Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Framer Motion/JS) a Alto (Web Audio/Canvas/Physics)"
stack_frameworks: ["React", "Next.js", "Tailwind CSS", "Motion (Framer Motion)", "Web Audio API", "Lucide React"]
compatibilidade:
  fontes_ideais: ["Instrument Sans", "Google Sans", "Inter", "Geist Sans"]
  paletas_ideais: ["Deep Graphite & Warm Charcoal (Stone 950 / Zinc 950)", "Apple Minimalist Neutral (Pure White / Black / Slate)", "Electric Accent Highlights (Neon Orange, Cyber Lime, Cyan)"]
  combinacoes_recomendadas: ["Shadcn UI", "Cult UI", "21st.dev", "Skiper UI", "Vaul"]
  conflitos_esteticos: ["Brutalismo cru sem transições elásticas", "Material Design corporativo padronizado sem física de mola", "Interfaces estáticas de alta densidade estilo terminal monolítico"]
---

# Bencho.dev — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e conduzido pelo engenheiro de design e animador de produto **Lorenzo Cabra** (`@cabralorenzo`), o **Bencho.dev** representa uma das vanguardas mais sofisticadas da *Creative UI Engineering* contemporânea. Trata-se de um laboratório vivo de blocos interativos, micro-interações de altíssima fidelidade e primitivas de movimento que resgatam o prazer sensorial do artesanato digital (*digital craft*).

Diferente de bibliotecas utilitárias genéricas que tratam componentes como caixas estáticas retangulares alternando opacidade em 200ms, o Bencho concebe cada elemento da interface como um **objeto físico dotado de massa, inércia, elasticidade, tensão superficial e feedback acústico**.

A assinatura visual do Bencho é sustentada por quatro pilares técnicos e sensoriais:

1. **Física Cinética Orgânica & Pseudo-Esqueumorfismo Tátil**:
   O Bencho não copia o esqueumorfismo visual datado dos anos 2000 (texturas de couro sintético ou brilhos excessivos), mas reinventa o **esqueumorfismo de comportamento**. Componentes como o *Crumpled Receipt*, o *Slingshot*, o *Option Wheel* e o *Folding Bill* simulam as propriedades físicas do papel amassado, da borracha tensionada, da gravidade, da inércia mecânica de tambores giratórios e do desdobramento de cédulas. A sensação é de manipular elementos analógicos de alta precisão através do vidro de um display.

2. **Feedback Auditivo Integrado (Web Audio API Micro-Soundscapes)**:
   Uma das características mais marcantes e raras no ecossistema web moderno é a presença da seção **Sounds** e a integração nativa com sintetizadores em tempo de execução via Web Audio API. O Bencho trata o som não como um artifício invasivo, mas como uma extensão tátil (*haptic audio cue*): pequenos "clicks" secos, estalos de catraca mecânica ao rolar tambores numéricos, estalos suaves de sucção em botões de ação e "thuds" graves de amortecimento quando uma mola chega ao repouso. Isso fecha o ciclo perceptivo de causa e efeito na interação.

3. **Arquitetura de "Bancada Viva" (The Bench & Live-Tuned Primitives)**:
   Sob a premissa de que *"Everything is live, not mocked"*, os blocos no Bencho operam com sliders e seletores em tempo real que permitem ao desenvolvedor e ao designer ajustar valores de rigidez de mola (`stiffness`), coeficiente de amortecimento (`damping`), atrito de arrasto e tempos de decaimento sonoro antes de copiar o código para seu projeto.

4. **Distribuição Copy-and-Paste & Integração com Protocolos de IA (MCP)**:
   Alinhado à filosofia moderna inaugurada pelo `shadcn/ui`, os componentes não impõem uma dependência rígida de biblioteca via npm que encapsula a lógica em uma caixa preta. Os blocos são exportados como arquivos limpos em React + Tailwind + Motion, prontos para modificação no diretório local do projeto. Adicionalmente, o ecossistema Bencho introduziu conectores **MCP (Model Context Protocol)**, permitindo que ferramentas assistidas por IA (como Cursor e Claude Code) leiam a geometria e as curvas de mola diretamente para compor interfaces contextualmente.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **Aplicações Consumer Tech, Fintechs Inovadoras & Neobanks**:
   Fluxos de transferência bancária, autenticação de transações, limites de crédito e parcelamento encontram no Bencho soluções perfeitas: *Slide to Confirm* (para aprovação de pagamentos sem cliques acidentais), *Budget Slider* com *Rolling Counter* para seleção de valores, e *Receipt Crumple* para arquivamento ou descarte de comprovantes.
2. **Produtos de Produtividade Moderna & Ferramentas Criativas (estilo Raycast, Linear, Craft)**:
   Aplicações onde a fluidez da navegação é um dos maiores diferenciais competitivos. O uso de *Dynamic Island*, *Magnifying Dock*, *Liquid Toggle* e *Action Nodes* eleva a percepção de refinamento e velocidade operacional.
3. **E-Commerces de Luxo, Moda e Cultura Sneaker/Streetwear**:
   Experiências de compra onde a interatividade direta gera valor emocional e engajamento: arrastar cartões de lookbook (*Swipe Deck*, *Card Fan*), selecionar tamanhos através de um cilindro giratório háptico (*Picker Wheel*) e inspecionar detalhes com *Image Compare* ou *Glass Bubble*.
4. **Portfólios de Design Engineers, Estúdios Criativos e Startups em Lançamento**:
   Superfícies de alto impacto visual para prender a atenção de investidores e clientes no Hero ou em seções interativas de apresentação de funcionalidades do produto.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Neutra e Estrutural)**:
  Superfícies sóbrias, tipografia neutra em escala geométrica (`Instrument Sans` ou `Inter`), grids CSS regulares, espaçamentos sem deformação e paleta monocromática de base (`zinc-900`/`stone-900` para dark mode ou `white`/`slate-50` para light mode).
- **30% (Camada Tátil e Micro-interações do Bencho)**:
  Onde os padrões utilitários refinados do Bencho operam com discrição: *Pill Accordion*, *Tab Bar* com indicador deslizante suave, *Command Bar*, *Copy Field* com feedback de mola, e *Time Scrubber* em formulários de agendamento.
- **10% (Showstoppers Protagonistas)**:
  O componente heroico da tela. Apenas **um** por página: um *Dynamic Island* flutuante no topo de uma dashboard, um *Slingshot* ou *Liquid Arrange* em uma tela de gamificação/onboarding, ou um *Slosh Slider* viscoso para ajuste de uma variável central do sistema.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Painéis de Alta Densidade de Dados & ERPs Corporativos Tradicionais**:
  Telas com centenas de registros por página, grades contábeis densas e relatórios de auditoria não toleram molas com oscilação elástica longa. Nesses contextos, cada milissegundo de atraso perceptual ou movimento supérfluo prejudica a produtividade de operadores diários.
- **Ambientes Estritamente Corporativos com Áudio Não-Silenciado por Padrão**:
  Nunca inicialize micro-sons de feedback ativados sem prévia autorização ou opt-in claro do usuário. O áudio deve ser uma camada de aprimoramento progressivo (*opt-in delightful layer*), mantendo um botão de mute visível e respeitando o estado mudo do sistema.
- **Aplicações com Restrições Críticas de Hardware / WebViews Embarcadas Lentas**:
  Dispositivos low-end e browsers embarcados com núcleos de renderização limitados sofrerão com cálculos matemáticos concorrentes de molas no JavaScript combinados com filtros SVG pesados (`feColorMatrix` ou `feGaussianBlur`).

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **Saturação de Áudio e Fadiga Sensorial**: Configurar cliques sonoros em cada `hover` de link ou botão. Isso transforma a interface em um brinquedo irritante. O feedback acústico deve ser reservado exclusivamente para eventos de confirmação física conclusiva (ex: soltar um slider, travar uma seleção, aprovar um envio).
- **Física Concorrente Sem Amortecimento Centralizado**: Posicionar cards com efeito `Tilt 3D`, um `Magnifying Dock` no rodapé e partículas magnéticas no fundo na mesma tela. O navegador entrará em sobrecarga de paint/composite e o usuário sentirá enjoo visual (*motion sickness*).
- **Ignorar `prefers-reduced-motion`**: Todo componente físico deve obrigatoriamente fornecer uma ramificação sem movimento cinético para usuários com distúrbios vestibulares, substituindo a física de arrasto e mola por transições discretas de opacidade.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão 12 dos blocos e padrões mais emblemáticos catalogados no ecossistema Bencho.dev:

### 1. Slingshot (`slingshot`)
- **Anatomia Visual**: Um nó interativo central preso a vetores elásticos virtuais (renderizados via SVG dinâmico `<path>`). À medida que o usuário clica e arrasta o nó para trás, a tensão da corda se acentua, deformando a curvatura de Bézier das linhas tensoras.
- **Gatilho de Interação**: Arrastar livremente com o ponteiro (`drag`, `dragConstraints`). No instante do soltar (`onDragEnd`), o nó dispara para a direção oposta com conservação de momento vetorial e ricochete elástico via mola subamortecida.
- **Onde encaixar**: Hero section interativa, onboarding gamificado, ou botão de envio de mensagens criativas ("disparar ideia / enviar convite").

### 2. Crumpled Receipt (`crumple`)
- **Anatomia Visual**: Um comprovante fiscal ou fatura realista renderizado com divisões de facetas poligonais e textura de papel reciclado. Inicialmente comprimido como uma bola de papel amassada em 3D, ele se desdobra progressivamente revelando o extrato detalhado de itens e valores.
- **Gatilho de Interação**: Arrastar horizontal ou verticalmente com o cursor (`drag="y"`). O percentual de deformação física mapeia diretamente o desdobramento das facetas e rotações no eixo Z.
- **Onde encaixar**: Telas de checkout bem-sucedido em e-commerce, histórico de transações de neobanks ou descarte/arquivamento de tarefas finalizadas.

### 3. Liquid UI Suite (`liq-toggle`, `liq-create`, `liq-arrange`)
- **Anatomia Visual**: Conjunto de elementos gelatinosos que utilizam filtros SVG compostos (`filter: url(#gooey)` com `feGaussianBlur` e `feColorMatrix`). Ao separar um botão em dois ou arrastar um item de uma lista, a "ponte líquida" se estica viscosamente antes de se romper, unindo-se novamente quando aproximada.
- **Gatilho de Interação**: Clique para expansão de menu (`liq-create`), toggle de estados (`liq-toggle`) ou arrasto e reordenação de itens (`liq-arrange`).
- **Onde encaixar**: Alternadores de modo em ferramentas de design, menus de ação rápida tipo Floating Action Button (FAB) e reordenação tátil de itens favoritos.

### 4. Slosh Slider (`slosh` / `wake-slider`)
- **Anatomia Visual**: Barra de progresso ou controle deslizante preenchido com líquido dinâmico. O fluido interno possui física de onda (*slosh physics*): ao mover rapidamente o slider para a direita e parar bruscamente, o líquido sobe pela parede lateral e oscila em ondas amortecidas até estabilizar no novo nível.
- **Gatilho de Interação**: Arrastar o controle deslizante (`drag="x"`). A derivada da velocidade do cursor calcula a aceleração da crista da onda.
- **Onde encaixar**: Controles de volume em players musicais, seletores de metas financeiras ou medidores de capacidade de armazenamento em SaaS.

### 5. Dynamic Island Suite (`dynamic-island`, `flight-island`, `music-island`, `call-island`)
- **Anatomia Visual**: Pílula flutuante preta fosca com raio de curvatura squircle de alta precisão. Transiciona organicamente entre estados mínimos (apenas ícones e pulsos de status) e expansões detalhadas (painel de voo com barra de progresso, player musical com ondas sonoras ou cartão de chamada com botões táteis).
- **Gatilho de Interação**: Clique para alternar expansão, eventos de WebSocket em tempo real para alertas do sistema ou hover discreto para preview.
- **Onde encaixar**: Cabeçalho flutuante global no topo da tela, atuando como o centro de notificações e status de processos em segundo plano de uma aplicação web.

### 6. Magnifying Dock (`dock`)
- **Anatomia Visual**: Barra de navegação horizontal com ícones contidos em recipientes circulares ou quadrados arredondados. À medida que o ponteiro do mouse se aproxima no eixo X, uma função gaussiana contínua calcula a proximidade e amplia proporcionalmente o tamanho dos ícones adjacentes, gerando a clássica curva de onda do macOS Dock.
- **Gatilho de Interação**: Movimento do ponteiro no eixo X (`useMotionValue` + `useTransform`).
- **Onde encaixar**: Rodapé flutuante de aplicativos desktop web, barra de ferramentas de editores gráficos ou navegação principal de portfólios imersivos.

### 7. Picker Wheel / Country Wheel (`picker-wheel` / `country-wheel`)
- **Anatomia Visual**: Tambor giratório cilíndrico renderizado com perspectiva 3D (`transform-style: preserve-3d` e `rotateX`). O texto curva-se suavemente para o fundo conforme se afasta da linha de centro ativa, com desvanecimento de opacidade e gradiente de sombra côncava.
- **Gatilho de Interação**: Arrastar vertical com inércia cinemática (*momentum scrolling*). A cada item que cruza o centro focal, o componente emite um micro-som mecânico de dente de engrenagem.
- **Onde encaixar**: Seletores de data/hora, seletores de código de país em formulários de telefone e filtros de atributos em e-commerce.

### 8. Slide to Confirm (`slide-confirm`)
- **Anatomia Visual**: Trilha horizontal contendo um botão deslizante circular ou pílula com ícone de seta ou cadeado. O trilho exibe um texto com efeito de brilho metálico deslizante (*shimmer*). Conforme o usuário arrasta o gatilho em direção ao final, a cor do trilho se preenche gradualmente e o texto desaparece em fade out.
- **Gatilho de Interação**: Arrastar com restrição horizontal (`drag="x"`, `dragConstraints={{ left: 0, right: maxDistance }}`). Se o usuário soltar antes de atingir 95% do curso, o botão ricocheteia elasticamente para o início; se atingir o limiar, trava na extremidade e dispara a ação.
- **Onde encaixar**: Confirmação final de ordens de pagamento, exclusão irreversível de bancos de dados ou assinatura de contratos eletrônicos.

### 9. Skeleton Morph (`skeleton-morph`)
- **Anatomia Visual**: Bloco de carregamento com brilho de pulso suave. Diferente dos skeletons convencionais que desaparecem instantaneamente com um piscar ao carregar os dados, o esqueleto do Bencho sofre deformação contínua de bordas e altura via `layoutId`, abrindo espaço para os elementos reais sem quebras ou repaints abruptos.
- **Gatilho de Interação**: Transição de estado assíncrono (Promise resolvida / carregamento de API).
- **Onde encaixar**: Feeds de conteúdo dinâmico, dashboards de métricas em tempo real e visualizadores de perfil de usuário.

### 10. Glass Bubble (`glass-bubble`)
- **Anatomia Visual**: Esfera translúcida com refração de fundo hiper-realista construída via múltiplas camadas de `backdrop-filter: blur()`, sombras especulares internas compostas (`box-shadow: inset ...`) e reflexo de luz superior simulando vidro curvo orgânico.
- **Gatilho de Interação**: Arraste livre em duas dimensões (`drag`) com física de colisão contra as bordas do container pai e atrito de ar simulado.
- **Onde encaixar**: Elemento decorativo interativo em páginas de manifesto de marca, visualizadores 3D interativos e Hero sections de produtos premium.

### 11. Rolling Counter / Budget Slider (`rolling-counter` / `budget-slider`)
- **Anatomia Visual**: Exibição numérica formatada (moedas, métricas, porcentagens) onde cada dígito ocupa uma coluna vertical independente. Ao alterar o valor, os números rolam verticalmente como as engrenagens de um odômetro analógico com amortecimento de mola individual para cada casa decimal.
- **Gatilho de Interação**: Alteração contínua disparada por um slider de arrasto ou por atualização de stream numérico.
- **Onde encaixar**: Calculadoras de retorno sobre investimento (ROI) em páginas de Pricing, displays de métricas financeiras de fintechs e contadores de saldo.

### 12. Audio Feedback Primitives (`Sound / sound-engine`)
- **Anatomia Visual**: Módulo invisível ou representado por um botão de controle tátil (`Sound` toggle com ondas de áudio animadas). Internamente, compõe uma cadeia de áudio do Web Audio API com nós de oscilador (`OscillatorNode`), curvas exponenciais de ganho (`GainNode.gain.exponentialRampToValueAtTime`) e filtros passa-baixa (`BiquadFilterNode`) para gerar sons orgânicos sem dependência de arquivos WAV/MP3 externos pesados.
- **Gatilho de Interação**: Disparado programaticamente via hooks de interação (`onPress`, `onSnap`, `onRelease`, `onSuccess`).
- **Onde encaixar**: Camada global de áudio de micro-interações em toda a aplicação.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup
Os componentes do Bencho são desenhados para rodar em ecossistemas modernos baseados em React 18/19, Next.js (App Router) e Tailwind CSS v3 ou v4.

```bash
# Dependências essenciais de animação, ícones e utilitários
npm install motion lucide-react clsx tailwind-merge
```

### Física de Movimento e Constantes de Mola
Para reproduzir com precisão a sensação mecânica e tátil do Bencho, utilize as seguintes configurações de mola no Motion:

| Finalidade | Configuração de Mola (`transition`) | Efeito Perceptual |
| :--- | :--- | :--- |
| **Snap Tátil Rápido** (Toggles, Abas, Docks) | `type: "spring", stiffness: 500, damping: 30, mass: 0.8` | Resposta instantânea com parada limpa sem oscilação excessiva |
| **Arraste e Ricochete** (Slingshot, Sliders) | `type: "spring", stiffness: 350, damping: 20, mass: 1` | Retorno elástico evidente com peso e balanço orgânico |
| **Morfologia de Containers** (Dynamic Island) | `type: "spring", stiffness: 400, damping: 28, mass: 0.9` | Deformação contínua de largura e altura sem vibração incômoda |
| **Fluidos e Ondas** (Slosh, Balanço) | `type: "spring", stiffness: 180, damping: 12, mass: 1.2` | Oscilação prolongada de líquido viscoso amortecendo gradualmente |

---

### Receita de Código Funcional 1: `SlideToConfirm` com Feedback Tátil Completo

Abaixo está a implementação completa e realista do componente **Slide to Confirm** do Bencho, contendo restrição de arrasto, cálculo percentual, efeito visual de shimmer e retorno elástico com mola:

```tsx
"use client";

import React, { useState, useRef } from "react";
import { motion, useMotionValue, useTransform, animate } from "motion/react";
import { ArrowRight, CheckCircle2, Lock } from "lucide-react";
import { clsx, type ClassValue } from "clsx";
import { twMerge } from "tailwind-merge";

function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs));
}

// Utilitário de sintetizador Web Audio para haptic clicks sem carregar arquivos de mídia
function playHapticTone(frequency: number = 800, duration: number = 0.05, type: OscillatorType = "sine") {
  if (typeof window === "undefined") return;
  try {
    const audioCtx = new (window.AudioContext || (window as unknown as { webkitAudioContext: typeof AudioContext }).webkitAudioContext)();
    const osc = audioCtx.createOscillator();
    const gain = audioCtx.createGain();

    osc.type = type;
    osc.frequency.setValueAtTime(frequency, audioCtx.currentTime);

    gain.gain.setValueAtTime(0.12, audioCtx.currentTime);
    gain.gain.exponentialRampToValueAtTime(0.0001, audioCtx.currentTime + duration);

    osc.connect(gain);
    gain.connect(audioCtx.destination);

    osc.start();
    osc.stop(audioCtx.currentTime + duration);
  } catch {
    // Ignora se o navegador bloquear o contexto de áudio
  }
}

interface SlideToConfirmProps {
  onConfirm: () => Promise<void> | void;
  label?: string;
  confirmedLabel?: string;
  className?: string;
}

export function SlideToConfirm({
  onConfirm,
  label = "Deslize para autorizar",
  confirmedLabel = "Autorizado com sucesso",
  className,
}: SlideToConfirmProps) {
  const [isConfirmed, setIsConfirmed] = useState(false);
  const [isPending, setIsPending] = useState(false);
  const trackRef = useRef<HTMLDivElement>(null);

  const x = useMotionValue(0);
  const [maxDrag, setMaxDrag] = useState(200);

  React.useEffect(() => {
    if (trackRef.current) {
      // Largura da trilha menos a largura do polegar (52px) menos o padding (8px)
      setMaxDrag(trackRef.current.clientWidth - 60);
    }
  }, []);

  // Transforma o deslocamento em progresso de opacidade e cor
  const progress = useTransform(x, [0, maxDrag], [0, 1]);
  const textOpacity = useTransform(x, [0, maxDrag * 0.5], [1, 0]);
  const fillScale = useTransform(x, [0, maxDrag], [0, 1]);

  const handleDragEnd = async () => {
    const currentX = x.get();
    if (currentX >= maxDrag * 0.9) {
      // Limiar atingido: completa o curso e confirma
      animate(x, maxDrag, { type: "spring", stiffness: 450, damping: 30 });
      playHapticTone(1050, 0.12, "triangle");
      setIsPending(true);
      try {
        await onConfirm();
        setIsConfirmed(true);
        playHapticTone(1320, 0.18, "sine");
      } catch {
        // Em caso de falha, reseta
        animate(x, 0, { type: "spring", stiffness: 350, damping: 25 });
        setIsConfirmed(false);
      } finally {
        setIsPending(false);
      }
    } else {
      // Não alcançou: ricochete de retorno
      playHapticTone(320, 0.06, "sine");
      animate(x, 0, { type: "spring", stiffness: 400, damping: 24 });
    }
  };

  return (
    <div
      ref={trackRef}
      className={cn(
        "relative select-none overflow-hidden rounded-full p-1 border",
        "bg-neutral-900/90 border-neutral-800 shadow-inner backdrop-blur-md",
        "h-[60px] w-full max-w-sm flex items-center justify-start",
        className
      )}
    >
      {/* Camada de preenchimento dinâmico de progresso */}
      <motion.div
        className="absolute left-0 top-0 bottom-0 bg-emerald-500/20 rounded-full origin-left"
        style={{
          width: "100%",
          scaleX: fillScale,
        }}
      />

      {/* Rótulo central com efeito de reflexo */}
      <motion.span
        style={{ opacity: textOpacity }}
        className="absolute inset-0 flex items-center justify-center text-xs font-semibold uppercase tracking-wider text-neutral-400 pointer-events-none"
      >
        {label}
      </motion.span>

      {/* Botão circular deslizante com física de mola */}
      {!isConfirmed ? (
        <motion.div
          drag="x"
          dragConstraints={{ left: 0, right: maxDrag }}
          dragElastic={0.08}
          dragMomentum={false}
          onDragStart={() => playHapticTone(520, 0.04, "sine")}
          onDragEnd={handleDragEnd}
          style={{ x }}
          whileHover={{ scale: 1.04 }}
          whileTap={{ scale: 0.96 }}
          className={cn(
            "relative z-10 flex h-[50px] w-[50px] cursor-grab active:cursor-grabbing items-center justify-center rounded-full shadow-lg border",
            "bg-gradient-to-b from-white to-neutral-200 text-neutral-900 border-white/60",
            isPending && "opacity-80 pointer-events-none"
          )}
        >
          {isPending ? (
            <div className="size-4 rounded-full border-2 border-neutral-800 border-t-transparent animate-spin" />
          ) : (
            <ArrowRight className="size-5 transition-transform" />
          )}
        </motion.div>
      ) : (
        <motion.div
          initial={{ opacity: 0, scale: 0.8 }}
          animate={{ opacity: 1, scale: 1 }}
          className="absolute inset-0 flex items-center justify-center gap-2 bg-emerald-500 text-neutral-950 font-medium text-sm rounded-full"
        >
          <CheckCircle2 className="size-5" />
          <span>{confirmedLabel}</span>
        </motion.div>
      )}
    </div>
  );
}
```

---

### Receita de Código Funcional 2: `MagnifyingDock` (Dock Mac com Ampliação Gaussiana)

Exemplo de implementação da barra tátil de ferramentas com interpolação de escala baseada no cursor do mouse:

```tsx
"use client";

import React, { useRef } from "react";
import { motion, useMotionValue, useSpring, useTransform } from "motion/react";
import { Terminal, Code2, Compass, Layers, Sparkles, Settings } from "lucide-react";

interface DockIconProps {
  mouseX: ReturnType<typeof useMotionValue<number>>;
  children: React.ReactNode;
  label: string;
  onClick?: () => void;
}

function DockItem({ mouseX, children, label, onClick }: DockIconProps) {
  const ref = useRef<HTMLDivElement>(null);

  // Distância do centro do ícone ao cursor do mouse no eixo X
  const distance = useTransform(mouseX, (val) => {
    const bounds = ref.current?.getBoundingClientRect() ?? { x: 0, width: 0 };
    return val - bounds.x - bounds.width / 2;
  });

  // Curva de ampliação proporcional: raio de 120px, escala vai de 44px a 72px
  const widthSync = useTransform(distance, [-120, 0, 120], [44, 72, 44]);
  const width = useSpring(widthSync, { mass: 0.1, stiffness: 380, damping: 22 });

  return (
    <motion.div
      ref={ref}
      style={{ width, height: width }}
      onClick={onClick}
      whileTap={{ scale: 0.9 }}
      className="group relative flex aspect-square items-center justify-center rounded-2xl bg-neutral-800/80 border border-white/10 text-white backdrop-blur-md shadow-md cursor-pointer transition-colors hover:bg-neutral-700/90"
    >
      {/* Tooltip com animação suave */}
      <span className="absolute -top-9 select-none rounded-md bg-neutral-950 px-2 py-1 text-[11px] font-medium text-neutral-200 opacity-0 shadow-lg border border-neutral-800 transition-opacity group-hover:opacity-100 pointer-events-none whitespace-nowrap">
        {label}
      </span>
      {children}
    </motion.div>
  );
}

export function MagnifyingDock() {
  const mouseX = useMotionValue(Infinity);

  return (
    <div className="flex w-full items-center justify-center py-6">
      <motion.div
        onMouseMove={(e) => mouseX.set(e.pageX)}
        onMouseLeave={() => mouseX.set(Infinity)}
        className="flex h-16 items-end gap-3 rounded-3xl border border-neutral-800/80 bg-neutral-950/70 p-2.5 backdrop-blur-xl shadow-2xl"
      >
        <DockItem mouseX={mouseX} label="Editor">
          <Code2 className="size-5" />
        </DockItem>
        <DockItem mouseX={mouseX} label="Terminal">
          <Terminal className="size-5" />
        </DockItem>
        <DockItem mouseX={mouseX} label="Explorar">
          <Compass className="size-5" />
        </DockItem>
        <DockItem mouseX={mouseX} label="Camadas">
          <Layers className="size-5" />
        </DockItem>
        <DockItem mouseX={mouseX} label="Agente IA">
          <Sparkles className="size-5 text-amber-400" />
        </DockItem>
        <div className="h-8 w-px bg-neutral-800 self-center mx-1" />
        <DockItem mouseX={mouseX} label="Preferências">
          <Settings className="size-5" />
        </DockItem>
      </motion.div>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao declarar componentes baseados na filosofia e biblioteca do **Bencho.dev** na arquitetura de um novo projeto, siga os seguintes parâmetros normativos:

1. **Equilíbrio Sensorial & Regra de Um Único Protagonista Tátil**:
   - Defina com clareza a hierarquia de protagonismo. Em nenhuma página devem coexistir dois componentes de manipulação contínua pesada (ex: nunca utilize um *Slingshot* e um *Slosh Slider* na mesma tela).
   - O *Slide to Confirm* deve ser reservado estritamente para ações críticas irrevogáveis (checkout, deleção em massa, publish de release), preservando seu valor de peso e compromisso.

2. **Isolamento de Áudio e Governança de Permissões**:
   - Qualquer componente que execute micro-sons através do Web Audio API deve ser obrigatoriamente envolto por um contexto provedor `SoundProvider`.
   - O usuário deve dispor de uma chave de desativação global (`isMuted: boolean`) persistida no `localStorage`, garantindo silêncio imediato caso navegue em ambiente compartilhado.

3. **Arquitetura de Arrasto Responsiva em Telas Touch**:
   - Componentes que usam `drag="x"` ou `drag="y"` devem incluir a propriedade `touch-action: none` ou `touch-action: pan-y` em CSS nas áreas de arrasto, evitando conflitos acidentais com a rolagem vertical de página nativa dos sistemas operacionais móveis (iOS Safari / Android Chrome).

4. **Tratamento Estrito de Acessibilidade (`prefers-reduced-motion`)**:
   - Para usuários com sensibilidade vestibular que tenham sinalizado redução de movimento no sistema operacional, a física de mola oscilatória deve ser convertida para transições lineares rápidas (`duration: 0.15s, ease: "easeOut"`), e componentes de arraste de impacto (como *Crumpled Receipt* ou *Slingshot*) devem oferecer botões equivalentes de clique simples com estados visuais estáticos.
