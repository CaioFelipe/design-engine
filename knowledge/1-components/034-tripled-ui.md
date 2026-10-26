---
id: "tripled-ui"
name: "UI TripleD"
url: "https://ui.tripled.work/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Luminous Frosted Glassmorphism", "Dual-Engine Architecture (Shadcn UI & Base UI)", "Visual Interactive Web Builders (Landing, Background, Grid)", "Typing-Reactive Motion Physics", "Vector Automations & Skeuomorphic Tech Tickets"]
densidade_informacao: "Media a Alta"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Framer Motion / Canvas 2D) a Baixo (Tailwind / CSS)"
stack_frameworks: ["React 19", "Next.js 16 / 15", "Tailwind CSS (v3.4 / v4)", "Framer Motion", "Shadcn UI (Radix UI)", "Base UI (@base-ui-components/react)", "Lucide React", "Turborepo"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Geist Mono", "Inter", "Plus Jakarta Sans", "JetBrains Mono"]
  paletas_ideais: ["Deep Obsidian Glass (Neutral 950 / Zinc 950 com backdrop-blur-xl)", "Emerald Cyber Glow (#10b981 / #34d399 com acentos violeta)", "Monochrome High-Contrast (Branco 90% sobre preto profundo)"]
  combinacoes_recomendadas: ["Shadcn UI", "Base UI", "Magic UI", "Aceternity UI", "Kokonut UI", "ReactBits"]
  conflitos_esteticos: ["Brutalismo plano sem suavização de cantos ou reflexos", "Neumorfismo pastoso com relevos opacos", "Material Design 2 com sombras drop saturadas e cores primárias chapadas"]
---

# UI TripleD — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo engenheiro de software e designer de produtos **Moumen Soliman** (`@moumensoliman`), e respaldado institucionalmente pelo **Vercel Open Source Program**, o **UI TripleD** (`ui.tripled.work`) estabeleceu-se como uma das iniciativas mais inovadoras no ecossistema de interfaces modernas para React e Next.js. O projeto nasceu com o propósito de transcender a mera oferta de cartões e botões isolados, oferecendo uma suíte completa de **blocos cênicos, páginas inteiras e utilitários visuais interativos** desenhados para montar produtos digitais completos com acabamento premium de nível Apple, Linear e Vercel.

A identidade visual e a engenharia do UI TripleD apoiam-se em cinco pilares fundamentais:

1. **Arquitetura Dual-Engine Pioneira (Shadcn UI + Base UI)**:
   Enquanto quase a totalidade das bibliotecas da comunidade atrela-se exclusivamente ao ecossistema `radix-ui` / `shadcn/ui`, o UI TripleD foi um dos primeiros catálogos abertos a fornecer paridade completa de componentes e blocos tanto para **Shadcn UI** quanto para a **Base UI** (a nova biblioteca de primitivas headless ultrarrápidas desenvolvida pela equipe do MUI). Isso permite que equipes de engenharia escolham livremente a base fundamental de acessibilidade de seu projeto sem sacrificar animações refinadas de Framer Motion.

2. **Estética "Luminous Frosted Glass & Precision Depth"**:
   A assinatura visual do TripleD baseia-se em camadas atmosféricas de vidro translúcido (`backdrop-blur-xl` a `backdrop-blur-md`, fundos `bg-background/40` ou `bg-card/30`, e bordas hiperdelicadas `border-border/40` a `border-border/60`). Esse tratamento visual garante profundidade tridimensional suave, integrando-se organicamente a paletas escuras (*Deep Neutral / Zinc 950*) e claras sem sobrecarregar o contraste dos textos corporativos.

3. **Mecânica Reativa de Entrada & Velocidade de Digitação**:
   Componentes como o *AI Glow Input* introduzem uma física de interação inovadora: a intensidade do brilho periférico e as micro-partículas flutuantes não são estáticas ou pré-gravadas, mas sim calculadas em tempo real a partir da cadência e velocidade de digitação do usuário (WPM / intervalos `lastTypingTime`). O componente responde visualmente ao ritmo cognitivo do usuário através de molas amortecidas de alta precisão (`stiffness: 420, damping: 32`).

4. **Simulações de Hardware & Skeuomorfismo Moderno Funcional**:
   O TripleD resgata a tangibilidade do mundo físico em formatos digitais contemporâneos de altíssima fidelidade:
   - A família de bilhetes de conferência (*Conference Ticket*, *Cinema Ticket*, *Theater Ticket*): recria ingressos de eventos com entalhes perfurados semicirculares nas bordas, linhas picotadas dashed, cartões com rotação em perspectiva 3D (`perspective-1000`) e canhoto destacável com código QR que reage a hovers elásticos.
   - O *N8n Workflow Block*: simula um canvas vivo de automações de agentes e pipelines no estilo n8n, permitindo arrastar nós (`motion.div drag`) com recálculo trigonométrico em tempo real de fios de conexão Bezier SVG.

5. **Ferramental Visual Integrado no Navegador (Builders & Generators)**:
   Diferente de repositórios que exigem tentativa e erro via código, o UI TripleD integra utilitários web interativos:
   - **Landing Builder**: construtor drag-and-drop no navegador para posicionar e reordenar blocos cênicos (Hero, Bento Grid, Pricing, Features, FAQ, Footer) e exportar o código JSX/Tailwind pronto.
   - **Background Builder**: gerador visual de fundos dinâmicos baseados em shaders GLSL e Aurora gradients com controles manuais de turbulência, velocidade, opacidade e harmonia cromática.
   - **Grid Generator**: gerador de matrizes complexas de Tailwind CSS Grid com dimensionamento interativo de colunas e linhas.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários

1. **SaaS de Inteligência Artificial, Agentes Autônomos & Workflows**:
   Plataformas que dependem de inputs conversacionais ricos e orquestração de lógica visual. A combinação do *AI Glow Input* com o *N8n Workflow Block* comunica imediatamente capacidade computacional avançada, oferecendo visualizações interativas de pipelines e automações sem exigir a instalação de bibliotecas pesadas de grafos como React Flow.
2. **Eventos de Tecnologia, Conferências & Plataformas de Credenciamento**:
   Startups de eventos, meetups de desenvolvedores e hackathons. O *Conference Ticket* atua como o cartão de visita interativo ideal para compartilhamento social (geração de passports digitais com nome do participante, cargo, avatar do GitHub e QR code dinâmico).
3. **DevTools, Plataformas Cloud & Observabilidade de Infraestrutura**:
   Ferramentas voltadas para desenvolvedores e SREs. O *Interactive Logs Table*, o *Web Performance Page*, o *Command Palette* e as seções de comparação técnica transmitem sobriedade operacional com elegância visual.
4. **Fintechs, Criptoativos & Plataformas de Câmbio**:
   Com o *Currency Converter Card*, *Stocks Dashboard*, *Glass Wallet Card* e o *Drag to Confirm Slider*, a biblioteca fornece padrões seguros e intuitivos para transações monetárias e autorização de pagamentos.
5. **Portfólios de Engenharia de Produto e Design Systems**:
   Templates de páginas completas como *Notion Blog Page*, *Professional Resume* e *Glassmorphism Portfolio Block* proporcionam uma vitrine profissional de altíssimo impacto.

### Papel no Ritmo Visual (Regra 60-30-10)

- **60% — Fundação Estrutural Neutra e Tipografia Limpa**:
  A base do produto deve adotar fundos neutros (`bg-background` / `bg-neutral-950`), divisores sutis (`border-border/40`), fontes mono e semiserifadas legíveis (`Geist Sans` e `Geist Mono`), combinadas com as primitivas básicas de formulários e botões neutros do Shadcn UI ou Base UI.
- **30% — Camada Cênica e Blocos de Narrativa do TripleD**:
  Blocos estruturais de alta densidade que organizam o valor do produto: *Bento Grid Block*, *Feature Comparison Block*, *Interactive Logs Table*, *Stats Counter Block* e *Glassmorphism Pricing Block*.
- **10% — Showstoppers Protagonistas de Alta Energia**:
  O clímax visual focado na conversão ou no diferencial tecnológico: a experiência imersiva de *Glowy Waves Hero* com canvas reativo ao cursor no topo da página, um *N8n Workflow Block* interativo na seção de demonstração do produto, ou o *Drag to Confirm Slider* na finalização de checkout.
  > [!IMPORTANT]
  > **Equilíbrio de Efeitos Contínuos**: Nunca sobreponha o *Liquid Cursor* com o *Glowy Waves Hero* na mesma seção. Efeitos de canvas com renderização por frame devem atuar como pano de fundo exclusivo de um hero ou ponto focal, evitando concorrência pelo processamento da GPU.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

- **Sistemas de Prontuário Médico, Compliance Jurídico e ERPs Contábeis Críticos**:
  Interfaces que demandam preenchimento estático contínuo por horas diárias. Campos de texto com iluminação pulsante proporcional à digitação (*AI Glow Input*) ou botões com rastros líquidos geram distração cognitiva e cansaço ocular em tarefas de alta concentração burocrática.
- **Aplicações para Dispositivos de Baixo Desempenho sem Aceleração de Hardware**:
  O uso de *Liquid Cursor* (que aplica filtros SVG complexos de `feGaussianBlur` e `feColorMatrix` sobre um canvas em tela cheia) pode sofrer degradação acentuada de taxa de quadros (menos de 20 FPS) em dispositivos móveis modestos se renderizado em alta resolução.
- **Ambientes Governamentais e Portais com Restrições Estritas de Acessibilidade (WCAG 2.2 AAA)**:
  Elementos como rastros de cursor líquidos e fundos ondulatórios contínuos sem um interruptor explícito violam os critérios de sucesso 2.2.2 (*Pause, Stop, Hide*), a menos que o hook `useReducedMotion()` esteja ativado para neutralizar os efeitos.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):

1. **"Visual Circus" (Efeitos Competindo Entre Si)**: Inserir simultaneamente no Hero: *Liquid Cursor*, fundo ondulatório *Glowy Waves*, botão com *Shimmer* cintilante e input de IA com partículas. O site perde toda a credibilidade corporativa e passa a parecer um experimento acadêmico desordenado.
2. **Abuso de Glassmorphism sem Fundo Contrastante**: Aplicar `backdrop-blur-xl bg-card/30 border border-border/50` sobre fundos monocromáticos lisos sem elementos por trás. O efeito de vidro perde o sentido se não houver gradientes sutis, luzes ou malhas de pontos para refratar, resultando em um cinza leitoso sujo.
3. **Não Configurar `prefers-reduced-motion` no Framer Motion**: Deixar partículas e ondulações ativas para usuários que configuraram redução de movimento no sistema operacional. No TripleD UI, todos os componentes sérios verificam `useReducedMotion()` para desligar loops contínuos.
4. **Canvas Desconectado de `ResizeObserver`**: Instanciar canvas de fundo como o *Glowy Waves Hero* sem gerenciar o descarte adequado do loop `cancelAnimationFrame` e sem recentralizar as coordenadas do mouse no redimensionamento da janela.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

### 1. `AIGlowInput` (`components/motion-core/ai-glow-input.tsx`)
- **Anatomia Visual**: Campo de prompt inteligente com cantos arredondados generosos (`rounded-2xl`), anel de iluminação radial dinâmica externa, partículas flutuantes sutis e um indicador de status dinâmico na base (*"⚡ Fast typing!"*, *"🎯 Active"*, *"✨ Ready"*).
- **Gatilho de Interação**: Foco do teclado (`onFocus`/`onBlur`) e cadência de digitação calculada em tempo real via `timeSinceLastType` e `useMotionValue`. Quanto mais rápido o usuário digita, mais intenso e vibrante se torna o feixe de luz periférico.
- **Onde Encaixar**: Barra de prompt central em Heroes de ferramentas de IA generativa, assistentes virtuais e caixas de busca semântica inteligente.

### 2. `N8nWorkflowBlock` (`components/sections/n8n-workflow-block.tsx`)
- **Anatomia Visual**: Simulador interativo de automações com estética de estúdio. Contém um canvas com grid pontilhado, cartões móveis de nós representando gatilhos (Webhooks, LLMs, Banco de Dados, Notificações Slack/Email) e conexões curvas conectando as saídas às entradas via curvas Bezier SVG dinâmicas. Inclui cabeçalho com botão "Add Node" e rodapé de métricas ativas.
- **Gatilho de Interação**: Arrastar e soltar nós (`drag` com Framer Motion), clique para adicionar novos nós com scroll automático suave para a nova posição (`canvas.scrollTo`), e hover nos conectores.
- **Onde Encaixar**: Seção de demonstração prática (*Interactive Product Demo*) em landing pages de SaaS de automação, plataformas de orquestração de IA e ferramentas para desenvolvedores.

### 3. `ConferenceTicket` (`components/sections/conference-ticket.tsx`)
- **Anatomia Visual**: Ingresso de conferência com relevo tridimensional (`perspective-1000`, `transformStyle: preserve-3d`). O corpo principal traz badge VIP com brilho animado (*shimmer*), tipografia destacada de data e localização, e cartão de identificação do participante com foto e cargo. A lateral direita forma a canhota destacável com recorte dashed semicircular nos vértices e código QR nítido.
- **Gatilho de Interação**: Hover com rotação e deslocamento elástico na canhota (`whileHover={{ x: 15, rotate: 5, transition: { type: "spring", stiffness: 300, damping: 20 } }}`) e tilt 3D no cartão principal.
- **Onde Encaixar**: Página de inscrição/confirmação de eventos tech, lançamento de produtos, campanhas de acesso antecipado (*Waitlist Confirmation*) ou credencial digital de comunidade.

### 4. `GlowyWavesHero` (`components/sections/glowy-waves-hero.tsx`)
- **Anatomia Visual**: Seção de abertura cinematográfica suportada por um elemento `<canvas>` que desenha 4 a 6 ondas senoidais sobrepostas com gradientes cromáticos, blur óptico de 35px e interpolação de sombras que reagem em tempo real ao movimento do mouse.
- **Gatilho de Interação**: Rastreamento vetorial contínuo do mouse (`mousemove`) com fator de amortecimento suave (`smoothing: 0.1`) e retorno elástico ao centro no `mouseleave`.
- **Onde Encaixar**: Primeiro fold (*Hero Section*) de produtos SaaS modernos, estúdios de design interativo ou plataformas de Web3/IA.

### 5. `LiquidCursor` (`components/liquid-cursor.tsx`)
- **Anatomia Visual**: Efeito de rastro fluido de cursor líquido (*gooey metaballs*) em tela cheia que dispersa gotas coloridas translúcidas que se fundem suavemente antes de evaporar.
- **Gatilho de Interação**: `mousemove` com interpolação linear de pontos intermediários (para evitar descontinuidades em movimentos rápidos) e ciclo de vida com decaimento exponencial (`life -= 0.01`). O visual gelatinoso é gerado por um filtro SVG com matriz de contraste alfa (`feColorMatrix values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 18 -7"`).
- **Onde Encaixar**: Sites de estúdios criativos, lançamentos comemorativos e portfólios visuais inovadores.

### 6. `DragToConfirmSlider` (`components/motion-core/drag-to-confirm-slider.tsx`)
- **Anatomia Visual**: Controle deslizante horizontal em formato de pílula (`rounded-full`) com indicador de tração, texto de orientação em transparência gradativa e transição elástica para estado de sucesso com ícone de verificação (*Checkmark*).
- **Gatilho de Interação**: Arrastar horizontal com limites definidos (`drag="x" dragConstraints={{ left: 0, right: 200 }}`). Ao ultrapassar 180px, o componente dispara o callback `onConfirm` e expande um badge preenchido.
- **Onde Encaixar**: Ações críticas irreversíveis: envio de fundos em carteiras cripto/fintech, exclusão permanente de repositórios/bancos de dados, ou assinatura final de planos Enterprise.

### 7. `InteractiveLogsTable` (`components/sections/interactive-logs-table.tsx`)
- **Anatomia Visual**: Tabela de telemetria moderna com linhas de logs estilizadas, chips de status coloridos (`SUCCESS`, `WARN`, `ERROR`), carimbos de data/hora monoespaçados, filtros instantâneos por severidade e paginação animada.
- **Gatilho de Interação**: Seleção de linhas com visualização detalhada em drawer expansível, filtro por texto com transições staggered de linhas via Framer Motion.
- **Onde Encaixar**: Dashboards operacionais, páginas de documentação de APIs, e seções de prova de confiabilidade em páginas de produtos DevTools.

### 8. `GlassmorphismPricingBlock` (`components/sections/glassmorphism-pricing-block.tsx`)
- **Anatomia Visual**: Matriz de planos de preços construída sobre painéis translúcidos foscos com realce no plano mais popular (*Popular Choice*) através de uma borda iluminada por gradiente cônico e botão principal com micro-brilho reativo.
- **Gatilho de Interação**: Alternância mensal/anual com transição suave de números (`layout` do Framer Motion) e elevação com expansão de sombra no hover dos cartões.
- **Onde Encaixar**: Seção de precificação (*Pricing*) em páginas de produtos comerciais SaaS.

### 9. `CinemaTicket` & `TheaterTicket` (`components/sections/cinema-ticket.tsx`)
- **Anatomia Visual**: Variações temáticas do ingresso interativo com orientação vertical, tipografia de corte retrô, horário de sessão, indicação de fileira/assento e visualização de código de barras vetorial.
- **Gatilho de Interação**: Flip 3D ao clicar para exibir detalhes do verso (regras de acesso, mapa de assento) e hover com micro-zoom.
- **Onde Encaixar**: Aplicações de entretenimento, clubes de cinema, eventos culturais e checkout de bilheteria online.

### 10. `NativeLiquidButton` & `NativeMorphingButton` (`components/micro/buttons/`)
- **Anatomia Visual**: Botões táteis compactos com reflexo líquido interno e capacidade de metamorfose estrutural (o botão se transforma fluidamente em um spinner circular de carregamento e, subsequentemente, em um selo de confirmação com check).
- **Gatilho de Interação**: Clique do mouse (`onClick`) disparando ondas concêntricas de rastro (*ripple effect*) com spring de restauração elástica.
- **Onde Encaixar**: Botões de Call-to-Action primários em formulários, modais de checkout e barras de navegação fixas.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

O UI TripleD é compatível com projetos Next.js 14/15/16 (App Router), Vite e Remix. Ele requer as dependências utilitárias clássicas do ecossistema shadcn/ui e Framer Motion:

```bash
# Dependências essenciais do ecossistema
pnpm add framer-motion lucide-react clsx tailwind-merge next-themes

# Se estiver utilizando a variante Base UI:
pnpm add @base-ui-components/react
```

### Instalação via Shadcn CLI

O TripleD disponibiliza um registro remoto compatível com o CLI oficial do shadcn:

```bash
# Adicionar componente individual diretamente do registry do TripleD
npx shadcn@latest add "https://ui.tripled.work/r/ai-glow-input.json"

# Adicionar bloco de workflow interativo
npx shadcn@latest add "https://ui.tripled.work/r/n8n-workflow-block.json"

# Adicionar bloco de ticket de conferência
npx shadcn@latest add "https://ui.tripled.work/r/conference-ticket.json"
```

---

### Física de Movimento e Constantes de Mola

O TripleD UI calibra suas transições com três regimes distintos de molas matemáticas (`framer-motion`):

1. **Mola Hiper-Responsiva para Digitação & Micro-Feedbacks**:
   ```ts
   // Usado no AI Glow Input para acompanhar cada caractere digitado
   const typingSpringConfig = {
     stiffness: 420,
     damping: 32,
     mass: 0.8
   };
   ```
2. **Mola Elástica para Canhotas & Cartões Destacáveis**:
   ```ts
   // Usado no deslocamento do stub no Conference Ticket
   const ticketStubSpring = {
     type: "spring",
     stiffness: 300,
     damping: 20
   };
   ```
3. **Mola Cinematográfica de Entrada Suave**:
   ```ts
   // Usado na entrada de cartões com perspectiva 3D
   const scenicEntranceSpring = {
     type: "spring",
     stiffness: 90,
     damping: 20,
     bounce: 0.2
   };
   ```

---

### Receita de Código Funcional: `AIGlowInput`

Abaixo está a implementação completa e realista do **AI Glow Input**, demonstrando a arquitetura de cálculo de velocidade de digitação, partículas e adaptação ao tema:

```tsx
"use client";

import React, { useEffect, useMemo, useRef, useState } from "react";
import { motion, useMotionValue, useReducedMotion, useSpring } from "framer-motion";
import { useTheme } from "next-themes";
import { Sparkles } from "lucide-react";
import { clsx, type ClassValue } from "clsx";
import { twMerge } from "tailwind-merge";

function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs));
}

interface Particle {
  left: string;
  top: string;
  delay: number;
}

interface AIGlowInputProps {
  placeholder?: string;
  glowColor?: string;
  onValueChange?: (value: string) => void;
  onSubmit?: (value: string) => void;
}

export function AIGlowInput({
  placeholder = "Pergunte qualquer coisa à IA...",
  glowColor,
  onValueChange,
  onSubmit,
}: AIGlowInputProps) {
  const [value, setValue] = useState("");
  const [glowIntensity, setGlowIntensity] = useState(0.3);
  const [isFocused, setIsFocused] = useState(false);

  const lastTypingTime = useRef(Date.now());
  const typingSpeed = useMotionValue(0);
  const glowIntensityMotion = useMotionValue(0.3);
  const shouldReduceMotion = useReducedMotion();

  const { resolvedTheme } = useTheme();
  const isDarkMode = resolvedTheme === "dark";

  // Cor adaptável ao tema claro ou escuro
  const effectiveGlowColor = useMemo(() => {
    if (glowColor) return glowColor;
    return isDarkMode ? "#38bdf8" : "#0284c7"; // Tom ciano luminoso
  }, [glowColor, isDarkMode]);

  // Conversão hex para RGB para interpolação de opacidade
  const hexToRgb = (hex: string) => {
    const cleanHex = hex.replace("#", "");
    const bigint = parseInt(cleanHex, 16);
    return {
      r: (bigint >> 16) & 255,
      g: (bigint >> 8) & 255,
      b: bigint & 255,
    };
  };

  const rgb = hexToRgb(effectiveGlowColor);

  // Geração de posições pseudo-aleatórias para as micro-partículas
  const particles = useMemo<Particle[]>(
    () =>
      Array.from({ length: 6 }).map(() => ({
        left: `${Math.random() * 90 + 5}%`,
        top: `${Math.random() * 80 + 10}%`,
        delay: Math.random() * 1.8,
      })),
    []
  );

  // Mola ultra-responsiva para o brilho dinâmico
  const springIntensity = useSpring(glowIntensityMotion, {
    stiffness: 420,
    damping: 32,
  });

  useEffect(() => {
    const unsubscribe = springIntensity.on("change", (latest) => {
      setGlowIntensity(latest as number);
    });
    return () => unsubscribe();
  }, [springIntensity]);

  const handleChange = (e: React.ChangeEvent<HTMLInputElement>) => {
    const nextVal = e.target.value;
    setValue(nextVal);
    onValueChange?.(nextVal);

    const now = Date.now();
    const interval = now - lastTypingTime.current;
    lastTypingTime.current = now;

    // Calcula velocidade relativa (pico com intervalos curtos de digitação)
    const speed = Math.min(1, 1000 / (interval || 1));
    typingSpeed.set(speed);

    const baseIntensity = 0.35;
    const dynamicIntensity = baseIntensity + speed * 0.65;
    glowIntensityMotion.set(dynamicIntensity);

    // Retorna gradualmente à intensidade base se parar de digitar por 500ms
    setTimeout(() => {
      if (Date.now() - lastTypingTime.current >= 450) {
        glowIntensityMotion.set(isFocused ? 0.5 : baseIntensity);
      }
    }, 500);
  };

  const handleKeyDown = (e: React.KeyboardEvent<HTMLInputElement>) => {
    if (e.key === "Enter" && value.trim()) {
      onSubmit?.(value);
    }
  };

  const shadowBlur = shouldReduceMotion ? 0 : glowIntensity * 36;
  const glowShadowAlpha = isDarkMode ? glowIntensity * 0.5 : glowIntensity * 0.25;

  return (
    <section className="relative w-full max-w-xl mx-auto">
      {/* Luz difusa atmosférica traseira */}
      <div aria-hidden className="pointer-events-none absolute inset-0 -z-10">
        <motion.div
          className="absolute -top-16 left-1/2 h-36 w-36 -translate-x-1/2 rounded-full blur-[90px]"
          style={{
            backgroundColor: `rgba(${rgb.r}, ${rgb.g}, ${rgb.b}, ${isDarkMode ? 0.35 : 0.2})`,
          }}
          animate={
            shouldReduceMotion
              ? undefined
              : { opacity: [0.3, 0.6, 0.3], scale: [0.95, 1.08, 0.95] }
          }
          transition={{ duration: 6, repeat: Infinity, ease: "easeInOut" }}
        />
      </div>

      <div className="relative rounded-2xl bg-card/60 backdrop-blur-xl border border-border/50 p-1">
        {/* Halo de luz radial reativo interno */}
        <motion.div
          aria-hidden
          className="pointer-events-none absolute inset-0 rounded-2xl"
          style={{
            background: `radial-gradient(circle at 50% 50%,
              rgba(${rgb.r}, ${rgb.g}, ${rgb.b}, ${glowIntensity * 0.4}) 0%,
              transparent 75%)`,
            filter: "blur(18px)",
          }}
          animate={{ opacity: isFocused ? 1 : 0.4 }}
          transition={{ duration: 0.3 }}
        />

        <div className="relative flex items-center overflow-hidden rounded-xl bg-background/80 px-4 py-2">
          <Sparkles
            className="mr-3 h-5 w-5 shrink-0 transition-colors"
            style={{
              color: isFocused
                ? `rgb(${rgb.r}, ${rgb.g}, ${rgb.b})`
                : "var(--muted-foreground)",
            }}
          />

          <input
            type="text"
            value={value}
            onChange={handleChange}
            onKeyDown={handleKeyDown}
            onFocus={() => {
              setIsFocused(true);
              glowIntensityMotion.set(0.6);
            }}
            onBlur={() => {
              setIsFocused(false);
              glowIntensityMotion.set(value ? 0.4 : 0.3);
            }}
            placeholder={placeholder}
            aria-label={placeholder}
            className="w-full bg-transparent text-sm md:text-base text-foreground placeholder:text-muted-foreground focus:outline-none"
            style={{
              boxShadow: `0 0 ${shadowBlur}px rgba(${rgb.r}, ${rgb.g}, ${rgb.b}, ${glowShadowAlpha})`,
            }}
          />
        </div>

        {/* Indicador de status tátil abaixo do campo */}
        {value && isFocused && (
          <motion.div
            initial={{ opacity: 0, y: -4 }}
            animate={{ opacity: 1, y: 0 }}
            exit={{ opacity: 0, y: -4 }}
            className="absolute -bottom-7 left-2 text-[11px] font-mono text-muted-foreground"
          >
            {glowIntensity > 0.75
              ? "⚡ Digitação acelerada!"
              : glowIntensity > 0.5
              ? "🎯 Processando fluxo..."
              : "✨ Pronto"}
          </motion.div>
        )}
      </div>

      {/* Partículas efervescentes em suspensão */}
      <div className="pointer-events-none absolute inset-0 overflow-hidden rounded-2xl">
        {particles.map((particle, idx) => (
          <motion.span
            key={idx}
            className="absolute h-1 w-1 rounded-full"
            style={{
              left: particle.left,
              top: particle.top,
              backgroundColor: `rgba(${rgb.r}, ${rgb.g}, ${rgb.b}, 0.7)`,
            }}
            animate={
              shouldReduceMotion
                ? { opacity: 0.2 }
                : {
                    y: [0, -18, 0],
                    opacity: [0.1, 0.6, 0.1],
                  }
            }
            transition={
              shouldReduceMotion
                ? { duration: 0 }
                : {
                    duration: 2.8,
                    repeat: Infinity,
                    delay: particle.delay,
                    ease: "easeInOut",
                  }
            }
          />
        ))}
      </div>
    </section>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma interface que incorpore blocos ou componentes do **UI TripleD**, declare as especificações estruturais conforme as diretrizes abaixo:

1. **Declaração do Motor Headless (Shadcn vs Base UI)**:
   - Especifique formalmente se a suíte de componentes consumirá as implementações baseadas em `@radix-ui` (Shadcn UI padrão) ou `@base-ui-components/react` (Base UI). Ambas compartilham o mesmo contrato de propriedades, mas exigem instalação de pacotes diferentes.
2. **Registro de Componentes & Dependências**:
   - Declare explicitamente os imports direcionados ao diretório `@/components/uitripled/...` gerados pelo instalador shadcn.
   - Certifique-se de listar `framer-motion` e `lucide-react` no rol de dependências do blueprint.
3. **Mapeamento de Papel na Regra 60-30-10**:
   - Declare o *Glowy Waves Hero* exclusivamente na raiz do viewport (`first fold`).
   - Restrinja o *N8n Workflow Block* a uma seção central de demonstração de produto, limitando sua altura inicial a `h-[500px]` com canvas rolável e nós encapsulados.
   - Aplique o *AI Glow Input* nos pontos neurálgicos de captação de comandos do usuário.
4. **Tratamento Mandatório de Acessibilidade**:
   - Qualquer componente com partículas contínuas ou canvas animado deve ser envolvido ou configurado com o hook `useReducedMotion()`, garantindo que gradientes estáticos elegantes substituam loops visuais quando o usuário solicitar redução de movimento.
