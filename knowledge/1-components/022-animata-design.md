---
id: "animata-design"
name: "Animata"
url: "https://animata.design/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["iOS & macOS Native Widget Craft", "Bento Grid Storytelling", "CSS Houdini & Keyframe Micro-interactions", "High-Tactile Physics & Haptics", "Modular Copy-Paste Registry"]
densidade_informacao: "Media"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Baixo (CSS/Headless) a Medio (Framer Motion/JS/Canvas)"
stack_frameworks: ["React 19 / 18", "Next.js 15 / 14 (App Router)", "Tailwind CSS (v3.4 & v4)", "Motion (Framer Motion)", "Lucide React", "shadcn/ui Remote Registry"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "SF Pro Display / Text", "Plus Jakarta Sans", "Geist Mono", "JetBrains Mono"]
  paletas_ideais: ["Apple Neutral Light/Dark (Zinc 50 a Zinc 950)", "Muted Surface Glass com Blur 16px e Borda Sutil", "Warm Minimalist Zinc & Slate com Acentos Amber/Indigo/Sky"]
  combinacoes_recomendadas: ["shadcn/ui", "Magic UI", "Cult UI", "21st.dev", "Aceternity UI"]
  conflitos_esteticos: ["Brutalismo agressivo com bordas pretas 4px e sombras duras sem blur", "Neumorfismo pastel desbotado com relevos pesados"]
---

# Animata — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pela equipe de engenharia e produto da **Codse** (notavelmente pelos desenvolvedores **Hari Lamichhane** e **Sudha Shrestha**, sediados em Pokhara, Nepal) com o apoio de uma comunidade global crescente de criativos, o **Animata** (`animata.design`) estabeleceu-se como a biblioteca de componentes e micro-interações mais especializada na estética de **widgets nativos de sistemas operacionais modernos (estilo iOS/macOS)**, **grades bento narrativas** e **efeitos cinéticos táteis** para React e Tailwind CSS.

Enquanto referências como o *Magic UI* focam primariamente na orquestração dramática de landing pages de SaaS de infraestrutura (com feixes de luz lineares e gradientes escuros) e o *Aceternity UI* destaca-se por canais WebGL/Three.js de alto impacto para telas iniciais (Heros), o Animata preenche um espaço visual único e cobiçado: o **"Widget Garden" de micro-aplicativos funcionais e tangíveis**. A biblioteca transpõe a familiaridade táctil, o acabamento óptico e o encanto das interfaces dos ecossistemas Apple, Raycast e Linear para blocos modulares que podem ser inseridos diretamente em landing pages, seções de features e dashboards.

A assinatura visual e técnica do Animata é alicerçada em quatro pilares fundamentais:

1. **Estética "Skeuo-minimalista" e Metáfora de Micro-Widgets**:
   O Animata entende que produtos digitais modernos não convencem os usuários apenas com listas estáticas de tópicos e ícones abstratos. Em vez disso, comunica capacidades de software através de **widgets operacionais compactos** — cartões meteorológicos que simulam temperatura e previsões atmosféricas, monitores de bateria com gradientes dinâmicos de carga, players de música com barras de equalização oscilantes, cartões de rastreamento de sono, bilhetes aéreos e cartões de telemetria. Cada componente tem raio de borda generoso (`rounded-2xl` a `rounded-3xl`), sombras difusas profundas, tipografia tabular monospaçada para métricas e hierarquia visual rigorosa.

2. **Engenharia Pure CSS First & CSS Houdini (`@property`)**:
   Uma distinção técnica crítica do Animata em relação a concorrentes focados puramente em Framer Motion é o seu pioneirismo na adoção de **CSS Moderno e CSS Houdini**. Efeitos sofisticados como o *Animated Border Trail* utilizam `@property --border-trail-angle` com sintaxe tipada `<angle>` e interpolação nativa de `@keyframes` para girar gradientes cônicos a 60/120 FPS na GPU do navegador com zero custo de bundle de JavaScript e sem sobrecarregar a thread principal. Quando Motion ou Framer Motion é empregado, ele é reservado estritamente para gestos de layout dinâmico e molas físicas.

3. **Arquitetura Narrativa em Bento Grids Modulares**:
   O Animata oferece arranjos de *Bento Grid* (`Three`, `Eight`, `Gradient`) desenhados para contextualizar as capacidades de um produto em compartimentos assimétricos. Em vez de grades genéricas, o layout é concebido para abrigar dados analíticos em um canto, micro-interações de arrastar/soltar no centro, um widget dinâmico de produtividade no topo e uma chamada de ação interativa na base. Isso transforma a seção de recursos do produto em um mostruário vivo.

4. **Micro-interações de Alta Resposta Táctil (Mechanical & Haptic Feel)**:
   A biblioteca inclui uma variedade surpreendente de micro-interações que despertam sensação mecânica física, como o botão *Duolingo* (que utiliza offset tridimensional de `box-shadow` e compressão em profundidade no estado `:active` simulando uma tecla de switch mecânico), menus radiais *Flower Menu*, botões com rastro de luz deslizante e mais de 42 variantes de manipulação tipográfica cinética (*Roll Text*, *Wave Reveal*, *Focus Blur Resolve*, *Typing Text*).

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **Seções de Features e Capacidades em SaaS B2B e B2C**:
   Produtos que precisam comprovar seu valor na prática. Em vez de apenas dizer *"Gerencie suas finanças"* ou *"Automatize seus fluxos"*, o uso de widgets como `ExpenseTracker`, `FundWidget` ou `TransactionList` dentro de uma estrutura `BentoGrid` cria uma demonstração visual instantânea e tangível.
2. **Dashboards de Monitoramento, Produtividade e Ferramentas Internas**:
   Painéis operacionais no estilo Raycast, Notion ou Linear, onde micro-indicadores modulares (`BatteryLevel`, `StorageStatus`, `StudyTimer`, `WeeklyProgress`, `ScoreBoard`) sintetizam telemetria e estado de sistema sem poluição visual.
3. **Aplicativos de Saúde, Bem-Estar e Estilo de Vida (HealthTech & FinTech)**:
   Aplicações focadas em dados de usuários (calorias, passos, sono, hidratação diária, metas semanais) que exigem gráficos de progresso circulares dinâmicos (`RingChart`, `DonutChart`, `WaterTracker`, `SleepTracker`) com transições elegantes de carga.
4. **Páginas de Lançamento de Produto, Waitlists e Aplicativos Mobile-First (PWA)**:
   Interfaces voltadas a dispositivos móveis e desktops premium onde o apelo visual de botões táteis (`Duolingo`, `RippleButton`, `SwipeButton`) e efeitos de entrada de texto aumentam as taxas de conversão e engajamento.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Neutra e Tipografia Estrutural)**:
  Superfícies limpas, neutras e altamente legíveis compostas por primitivas funcionais do `shadcn/ui` (botões neutros, navegação de topo, campos de formulário, modais e fundos em `bg-background` e `bg-surface-card` em tons de Zinc ou Slate).
- **30% (Camada de Estruturação e Narrativa em Widgets do Animata)**:
  Contêineres de *Bento Grid* organizando os tópicos centrais da página, cartões com efeito *Card Spread* ou *Card Stack* para exibir galerias de depoimentos ou integrações, e grids de widgets dinâmicos simulando o ecossistema do produto.
- **10% (Showstoppers Protagonistas e Acentos de Foco)**:
  Um contêiner envolto pelo *Animated Border Trail* circundando o cartão de oferta principal ou o formulário de conversão mais valioso; um título principal do Hero animado com *Roll Text* ou *Wave Reveal*; um menu flutuante *Flower Menu* atuando como ponto de suporte ou feedback do usuário no canto inferior.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Fluxos Transacionais Críticos e Checkouts de Alta Velocidade**:
  Páginas de pagamento com cartão de crédito, telas de checkout e-commerce ou formulários burocráticos onde o foco cognitivo deve ser 100% voltado à conclusão sem distrações visuais. A inclusão de botões que balançam, textos que digitam continuamente ou widgets meteorológicos no checkout eleva a fricção e reduz a taxa de conclusão.
- **Tabelas de Auditoria e Telas Analíticas Densas de ERP Corporativo**:
  Sistemas financeiros onde analistas lidam com milhares de linhas e células de dados em tempo real. O acabamento espesso com cantos arredondados generosos (`rounded-3xl`) e espaçamentos volumosos dos widgets do Animata sacrifica a densidade de informação necessária.
- **Ambientes Governamentais ou Portais com Requisito de Acessibilidade Estrita (WCAG AAA)**:
  Efeitos de texto cinético contínuo como *Glitch Text*, *Gibberish Text* ou rotações de texto em loop infinito sem controle manual de pausa podem gerar severas barreiras para pessoas com distúrbios vestibulares, dislexia ou déficit de atenção caso os gatilhos de `prefers-reduced-motion` não sejam rigorosamente implementados.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **"Widget Soup" (Salada de Widgets Desconexos)**:
  Colocar em uma única página de produto B2B um widget de clima de Tóquio, um player de música lo-fi, um cartão de bateria de iPhone e um rastreador de hidratação. O efeito estético degrada imediatamente para uma página falsa de IA sem coerência temática. Os widgets devem ser customizados para refletir dados estritamente pertinentes ao produto em questão.
- **Conflito de Física de Movimento**:
  Misturar no mesmo campo de visão um botão de desenho animado 3D com efeito de compressão plástica (estilo Duolingo) e um cartão minimalista ultra-sóbrio monocromático com bordas de 1px translúcidas. A interface perde harmonia estilística e parece um amálgama de retalhos.
- **Omissão da Tipografia Tabular em Métricas Numéricas**:
  Utilizar fontes com largura de dígitos proporcional em componentes como contadores, relógios e gráficos. Sem a classe `tabular-nums` do Tailwind, cada mudança de valor provoca oscilação horizontal (*layout shift*) nos elementos vizinhos.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão 12 dos componentes e categorias mais emblemáticos da biblioteca Animata:

### 1. Animated Border Trail (`@/components/animata/container/animated-border-trail`)
- **Anatomia Visual**: Um contêiner refinado com raio de curvatura `rounded-2xl` cuja borda perimetral de 1px é percorrida por um feixe luminoso colorido que gira continuamente em 360°. Utiliza um elemento interno com fundo opaco sobreposto a uma camada inferior de gradiente cônico (`conic-gradient`), revelando apenas uma fita de luz itinerante.
- **Gatilho de Interação**: Animação perpétua executada puramente em CSS via `@property --border-trail-angle` interpolando de `0deg` a `360deg` em GPU.
- **Onde encaixar**: No contêiner de pré-visualização do Hero, no cartão de preços de maior destaque (Tier "Pro/Growth") ou em cards de destaque no Bento Grid.

### 2. Weather Card Widget (`@/components/animata/widget/weather-card`)
- **Anatomia Visual**: Cartão compacto quadrado (`size-52`) com curvatura suave `rounded-3xl`, fundo com gradiente sutil translúcido (`bg-gradient-to-br`), ícone meteorológico vetorial (`CloudSunRain`), temperatura em números gigantes (`text-[34px]`) e rodapé em vidro fosco (`backdrop-blur-sm`) com divisores verticais exibindo máximas e mínimas.
- **Gatilho de Interação**: Estático ou com transições suaves de dados em tempo real; hover sutil com elevação de escala (`scale-102`).
- **Onde encaixar**: Células periféricas de Bento Grids de SaaS, painéis de controle inteligentes ou centrais de dashboards pessoais.

### 3. Music Widget Player (`@/components/animata/widget/music-widget`)
- **Anatomia Visual**: Miniaturização do player nativo do iOS. Exibe capa de álbum com cantos arredondados, título da faixa e artista em tipografia nítida, controles de reprodução (Play/Pause, Skip) e um equalizador de barras vetoriais que pulsa em amplitudes variadas simulando a reprodução sonora.
- **Gatilho de Interação**: Clique nos botões de controle para alternar estado de execução; animação contínua das barras do equalizador enquanto ativo.
- **Onde encaixar**: Demonstrações de ferramentas de áudio, podcasts, criadores de conteúdo e seções de mídia interativa.

### 4. Bento Grid (Modelos `Eight`, `Three` & `Gradient`) (`@/components/animata/bento-grid`)
- **Anatomia Visual**: Sistema de grid assimétrico baseado em `grid-cols-1 md:grid-cols-3` ou `md:grid-cols-4` com espaçamento rigoroso (`gap-4` a `gap-6`). O modelo `Eight` organiza 8 micro-compartimentos funcionais com proporções variadas, permitindo acomodar gráficos, ilustrações, blocos de código e micro-widgets em uma tapeçaria coesa.
- **Gatilho de Interação**: Hover coordenado entre as células com elevação e destaque de borda luminosa sutil.
- **Onde encaixar**: A seção principal de "Capacidades do Produto" / "Por que Nos Escolher", localizada estrategicamente após o Hero.

### 5. Duolingo 3D Button (`@/components/animata/button/duolingo`)
- **Anatomia Visual**: Botão com estética tátil volumétrica. Não utiliza gradientes complexos, mas sim uma camada de fundo sólida deslocada verticalmente (`translate-y-[4px]`) que atua como face inferior da tecla física, combinada com bordas arredondadas e tipografia em caixa alta ou negrito expressivo.
- **Gatilho de Interação**: Ao ser pressionado (`:active`), o corpo superior translada para baixo no eixo Y (`translate-y-[4px]`), colapsando visualmente a profundidade e simulando o clique de uma tecla mecânica com alta satisfação sensorial.
- **Onde encaixar**: Botões de ação em aplicações de aprendizagem, formulários interativos, gamificação ou botões secundários em páginas de conversão de alto engajamento.

### 6. Roll Text (`@/components/animata/text/roll-text`)
- **Anatomia Visual**: Efeito tipográfico inspirado nos letreiros mecânicos de estações de trem clássicas e na interface moderna do próprio site do Animata. Cada caractere de uma palavra é dividido em uma coluna vertical com duplicatas sobrepostas em trilhas isoladas.
- **Gatilho de Interação**: Ao passar o mouse sobre o contêiner (ou em transições de foco), as letras rolam verticalmente em sequência cascata (*staggered delay* de 32ms por letra), criando um efeito de tambor cinético de alta precisão.
- **Onde encaixar**: Links de navegação do Navbar, títulos curtos de cartões e botões com tipografia técnica.

### 7. Typing Text & Wave Reveal (`@/components/animata/text`)
- **Anatomia Visual**: `TypingText` simula a entrada de comandos em terminal ou a geração de tokens de IA caractere por caractere, acompanhado de um cursor pulsante vertical (`|`). `WaveReveal` quebra o parágrafo ou título em palavras/letras individuais e as faz surgir em um movimento ondulatório que combina deslocamento no eixo Y e desfoque óptico gradual.
- **Gatilho de Interação**: Disparado ao entrar no campo de visualização (*viewport scroll*) com auto-execução única.
- **Onde encaixar**: Cabeçalhos principais do Hero, simulações de código interativas e chamadas de destaque para ferramentas de IA.

### 8. Card Stack & Card Spread (`@/components/animata/card`)
- **Anatomia Visual**: `CardStack` organiza múltiplos cartões empilhados fisicamente com rotações angulares sutis (`rotate-2`, `-rotate-2`), escalas decrescentes e desfoque nas camadas traseiras. `CardSpread` mantém os cartões recolhidos como um baralho e os abre em leque uniforme ao interagir.
- **Gatilho de Interação**: Hover no contêiner ou clique para ciclar a ordem dos cartões da pilha para o fundo.
- **Onde encaixar**: Depoimentos de clientes, fluxos de cartão de crédito/fintech, e visualização de etapas de um workflow.

### 9. Boids Ecosystem Background (`@/components/animata/background/boids-ecosystem`)
- **Anatomia Visual**: Plano de fundo interativo baseado no consagrado algoritmo de bandos (*flocking*) de Craig Reynolds. Dezenas de partículas dinâmicas (boids) navegam pelo espaço visual obedecendo às forças físicas de separação, alinhamento e coesão de grupo.
- **Gatilho de Interação**: As partículas reagem continuamente à posição do cursor do mouse, dispersando-se em rota de fuga e reagrupando-se organicamente em correntes fluidas.
- **Onde encaixar**: Planos de fundo de Hero sections em plataformas de inteligência coletiva, redes neurais, agentes autônomos ou páginas de erro 404 lúdicas.

### 10. Ring Chart & Gauge Chart (`@/components/animata/graphs`)
- **Anatomia Visual**: Gráficos circulares de alta precisão construídos sobre vetores SVG puros. O arco de preenchimento é controlado por propriedades de traçado (`stroke-dasharray` e `stroke-dashoffset`), integrando marcadores de porcentagem legíveis e cores dinâmicas de alerta ou conclusão no centro.
- **Gatilho de Interação**: Animação inicial de preenchimento progressivo do arco utilizando curva Bézier de desaceleração suave quando o elemento atinge a tela.
- **Onde encaixar**: Cards analíticos de saúde, armazenamento em nuvem, taxas de conversão ou metas cumpridas em dashboards.

### 11. Flight Widget & Delivery Card (`@/components/animata/widget`)
- **Anatomia Visual**: Metáforas ricas de mobilidade urbana e logística. O `FlightWidget` exibe códigos de aeroportos (ex: JFK ➔ HND), horário de embarque, portão, assento e status de voo com linhas pontilhadas de trajetória aérea. O `DeliveryCard` sintetiza o trajeto de entregas com ícones de encomendas e estimativas em tempo real.
- **Gatilho de Interação**: Hover que acentua a linha de rota e exibe detalhes contextuais em tooltips táteis.
- **Onde encaixar**: Aplicações de viagens, e-commerces com rastreamento logístico avançado ou dashboards operacionais.

### 12. Sibling Focus Nav (`@/components/animata/container/sibling-focus-nav`)
- **Anatomia Visual**: Sistema de navegação onde os itens não selecionados sofrem uma atenuação óptica coordenada (`opacity-40` ou `blur-[1px]`), enquanto o item sob o cursor recebe destaque luminoso e escala imediata.
- **Gatilho de Interação**: Movimento do ponteiro sobre os elementos irmãos (`:has(> a:hover)` em CSS moderno).
- **Onde encaixar**: Navbars minimalistas, seletores de filtros em galerias de projetos e barras de ferramentas secundárias.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

O Animata opera no mesmo paradigma moderno do *shadcn/ui*, disponibilizando componentes prontos para cópia direta ou via CLI através do remote registry nativo:

```bash
# Adicionando componentes via CLI remota do shadcn
pnpm dlx shadcn@latest add https://animata.design/r/container/animated-border-trail.json
pnpm dlx shadcn@latest add https://animata.design/r/widget/weather-card.json
pnpm dlx shadcn@latest add https://animata.design/r/button/duolingo.json

# Dependências utilitárias fundamentais
pnpm add clsx tailwind-merge lucide-react

# Para componentes que empregam física de molas avançadas
pnpm add framer-motion # ou 'motion'
```

Certifique-se de possuir o utilitário padrão `@/lib/utils.ts` configurado:

```typescript
// src/lib/utils.ts
import { type ClassValue, clsx } from "clsx";
import { twMerge } from "tailwind-merge";

export function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs));
}
```

---

### Física de Movimento, CSS Houdini & Transições

1. **CSS Houdini `@property`**:
   Para animações circulares perfeitas de borda sem repintura desnecessária da árvore DOM, o Animata registra propriedades tipadas no CSS global ou local do componente:
   ```css
   @property --border-trail-angle {
     syntax: "<angle>";
     initial-value: 0deg;
     inherits: false;
   }
   ```
2. **Curvas de Bézier e Transições de Layout**:
   - Transições de Hover Táctil: `cubic-bezier(0.16, 1, 0.3, 1)` (Ultra-smooth Apple ease-out).
   - Molas de Expansão (Framer Motion / Motion): `stiffness: 260`, `damping: 20`, `mass: 1`.
   - Stagger em Textos Cinéticos (`RollText`): `delay: index * 0.032s` com duração fixa de `200ms` a `300ms`.

---

### Receitas de Código Completas e Funcionais

#### Receita 1: Animated Border Trail (Pure CSS Houdini + React)

Componente de contêiner de altíssimo impacto visual que circula o elemento com um feixe laser colorido contínuo.

```tsx
// src/components/animata/container/animated-border-trail.tsx
"use client";

import React from "react";
import { cn } from "@/lib/utils";

// Estilos co-localizados ou injetados via globals.css
// Necessário para registrar a propriedade angular do gradiente cônico
const cssStyles = `
@property --border-trail-angle {
  syntax: "<angle>";
  initial-value: 0deg;
  inherits: false;
}

@keyframes border-trail-spin {
  0% {
    --border-trail-angle: 0deg;
  }
  100% {
    --border-trail-angle: 360deg;
  }
}
`;

interface AnimatedBorderTrailProps extends React.HTMLAttributes<HTMLDivElement> {
  duration?: string;
  trailColor?: string;
  trailSize?: "sm" | "md" | "lg";
  contentClassName?: string;
}

const trailSizeMap = {
  sm: 5,   // arco menor e concentrado
  md: 12,  // arco equilibrado padrão
  lg: 25,  // arco longo e difuso
};

export function AnimatedBorderTrail({
  children,
  className,
  contentClassName,
  duration = "8s",
  trailColor = "hsl(262, 83%, 58%)", // Violeta tecnológico vibrante
  trailSize = "md",
  ...props
}: AnimatedBorderTrailProps) {
  const percentage = 100 - trailSizeMap[trailSize];

  return (
    <>
      {/* Injeção inline de segurança dos keyframes tipados */}
      <style dangerouslySetInnerHTML={{ __html: cssStyles }} />

      <div
        {...props}
        className={cn(
          "relative h-fit w-fit overflow-hidden rounded-2xl bg-border p-[1px] shadow-sm",
          className
        )}
      >
        {/* Camada do Feixe Conic Animado */}
        <div
          className="absolute inset-0 h-full w-full pointer-events-none"
          style={{
            animation: `border-trail-spin ${duration} linear infinite`,
            background: `conic-gradient(from var(--border-trail-angle) at 50% 50%, transparent ${percentage}%, ${trailColor})`,
          }}
        />

        {/* Superfície Interna com Recorte Oclusivo */}
        <div
          className={cn(
            "relative h-full w-full overflow-hidden rounded-[15px] bg-card text-card-foreground p-6",
            contentClassName
          )}
        >
          {children}
        </div>
      </div>
    </>
  );
}
```

---

#### Receita 2: Duolingo 3D Tactile Button (Sensação Mecânica de Clique)

Botão tridimensional com resposta mecânica háptica instantânea e feedback no clique.

```tsx
// src/components/animata/button/duolingo-button.tsx
"use client";

import React from "react";
import { cn } from "@/lib/utils";

interface DuolingoButtonProps
  extends React.ButtonHTMLAttributes<HTMLButtonElement> {
  variant?: "primary" | "success" | "danger" | "ghost";
}

export function DuolingoButton({
  children,
  className,
  variant = "primary",
  ...props
}: DuolingoButtonProps) {
  // Paletas de extrusão 3D física
  const colorMap = {
    primary: {
      top: "bg-indigo-600 hover:bg-indigo-500 text-white",
      bottom: "bg-indigo-800",
    },
    success: {
      top: "bg-emerald-500 hover:bg-emerald-400 text-white",
      bottom: "bg-emerald-700",
    },
    danger: {
      top: "bg-rose-500 hover:bg-rose-400 text-white",
      bottom: "bg-rose-700",
    },
    ghost: {
      top: "bg-zinc-100 hover:bg-white text-zinc-900 border border-zinc-200 dark:bg-zinc-800 dark:text-zinc-100 dark:border-zinc-700",
      bottom: "bg-zinc-300 dark:bg-zinc-900",
    },
  };

  const selectedColors = colorMap[variant];

  return (
    <div className={cn("relative inline-block select-none", className)}>
      {/* Camada inferior representando a extrusão 3D */}
      <div
        className={cn(
          "absolute inset-0 translate-y-1.5 rounded-2xl transition-all duration-150",
          selectedColors.bottom
        )}
      />

      {/* Camada superior clicável que translada em profundidade no :active */}
      <button
        {...props}
        className={cn(
          "relative inline-flex items-center justify-center gap-2 rounded-2xl px-6 py-3.5 text-sm font-bold uppercase tracking-wider",
          "transform transition-transform duration-75 active:translate-y-1.5",
          "focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2",
          selectedColors.top
        )}
      >
        {children}
      </button>
    </div>
  );
}
```

---

#### Receita 3: Weather Card Widget (Estilo Apple macOS/iOS)

Widget meteorológico de alta densidade semântica para montagem direta em Bento Grids.

```tsx
// src/components/animata/widget/weather-card.tsx
"use client";

import React from "react";
import { ArrowUp, CloudSunRain, MapPin } from "lucide-react";
import { cn } from "@/lib/utils";

export interface WeatherCardProps extends React.HTMLAttributes<HTMLDivElement> {
  city?: string;
  temperature?: number;
  feelsLike?: number;
  high?: number;
  low?: number;
  condition?: string;
}

export function WeatherCard({
  className,
  city = "San Francisco",
  temperature = 18,
  feelsLike = 17,
  high = 21,
  low = 12,
  condition = "Partly Cloudy",
  ...props
}: WeatherCardProps) {
  return (
    <div
      {...props}
      className={cn(
        "group relative flex size-52 flex-col justify-between overflow-hidden rounded-3xl border border-border/80",
        "bg-gradient-to-br from-card/90 via-card/50 to-muted/40 p-4 font-sans shadow-md backdrop-blur-md",
        "transition-all duration-300 hover:border-foreground/20 hover:shadow-lg",
        className
      )}
    >
      {/* Cabeçalho do Card */}
      <div className="flex flex-col gap-1">
        <div className="flex items-center gap-1.5 text-xs font-semibold text-muted-foreground uppercase tracking-wider">
          <MapPin className="size-3 text-primary shrink-0" />
          <span className="truncate">{city}</span>
        </div>

        {/* Temperatura Principal & Ícone Vetorial */}
        <div className="mt-2 flex items-center justify-between">
          <span className="font-mono text-4xl font-light tracking-tight tabular-nums text-foreground">
            {temperature}°
          </span>
          <CloudSunRain className="size-8 text-amber-500 dark:text-amber-400 drop-shadow-sm transition-transform duration-300 group-hover:scale-110" />
        </div>

        <p className="text-[12px] text-muted-foreground leading-snug">
          {condition} • Sensação {feelsLike}°
        </p>
      </div>

      {/* Rodapé Glass com Máximas e Mínimas */}
      <div className="flex items-center justify-between rounded-xl border border-border/50 bg-background/60 px-3 py-2 text-xs font-medium tabular-nums backdrop-blur-sm">
        <div className="flex items-center gap-1 text-rose-500 dark:text-rose-400">
          <ArrowUp className="size-3" />
          <span>Máx {high}°</span>
        </div>
        <span className="text-border">|</span>
        <div className="flex items-center gap-1 text-sky-500 dark:text-sky-400">
          <ArrowUp className="size-3 rotate-180" />
          <span>Mín {low}°</span>
        </div>
      </div>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar o **Animata** como biblioteca de componentes em um novo projeto, a IA arquiteta de software e design system deve obedecer rigorosamente às seguintes diretrizes operacionais:

1. **Definição de Papel Arquitetural (O "Widget Engine")**:
   - Declare o Animata como a camada de **expressão táctil, micro-widgets e layout bento** do projeto.
   - Use o `shadcn/ui` para a fundação operacional invisível (menus, diálogos, tabelas, formulários corporativos).
   - Use o `Animata` para alimentar os blocos de demonstração prática: seções de Bento Grid onde micro-aplicativos (clima, tarefas, telemetria, finanças, players) comprovam o funcionamento do produto.

2. **Checklist de Registro e Estilização**:
   - Garanta que as propriedades CSS tipadas de `@property` (como `--border-trail-angle`) sejam registradas no arquivo de CSS global da aplicação (`globals.css`) ou em folhas de estilo co-localizadas para prevenir erros de compilação em servidores Node/Next.js SSR.
   - Aplique sempre a classe `tabular-nums` em métricas, placares, horários e contadores dos widgets para neutralizar layout shifts indesejados.

3. **Curadoria de Coerência Visual (Anti-Slop Guardrail)**:
   - **Regra de Ouro**: Limite a presença de micro-widgets a no máximo 3 ou 4 variações tematicamente alinhadas ao propósito do produto. Se o produto é uma ferramenta de produtividade para desenvolvedores, empregue `CodeSkeleton`, `WeeklyProgress`, `StudyTimer` e `StorageStatus`; nunca misture com widgets de saúde física como `CalorieCounter` ou `WaterTracker`.
   - Em dispositivos móveis (`< 640px`), reorganize os Bento Grids para pilhas verticais fluidas (`grid-cols-1`) e garanta que os contêineres de widgets ocupem `w-full` com proporção de aspect ratio mantida.

4. **Tratamento de Acessibilidade & Movimento Reduzido**:
   - Todo componente com loop perpétuo (`AnimatedBorderTrail`, `BoidsEcosystem`, `TypingText`) deve verificar `@media (prefers-reduced-motion: reduce)` ou a classe Tailwind `motion-reduce:animate-none` para congelar o estado visual em uma versão estática elegante quando solicitado pelo usuário.
