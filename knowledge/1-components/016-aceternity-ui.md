---
id: "aceternity-ui"
name: "Aceternity UI"
url: "https://ui.aceternity.com/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Sci-Fi Dark Craft", "Cybernetic Minimalism", "High-Impact Kinetic", "Luminescent Gradients", "Linear & Vercel Aesthetic"]
densidade_informacao: "Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Framer Motion/CSS) a Alto (Canvas/WebGL/3D)"
stack_frameworks: ["React", "Next.js", "Tailwind CSS", "Framer Motion / Motion", "TypeScript", "Lucide React"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "Plus Jakarta Sans", "JetBrains Mono", "Space Grotesk"]
  paletas_ideais: ["Obsidian & Slate (Slate 950 / Zinc 950)", "Deep Indigo & Cyber Cyan", "Emerald Glow & Neutral 950", "Monochrome High-Contrast com Acentos Especulares"]
  combinacoes_recomendadas: ["shadcn/ui (para controles funcionais e base)", "Magic UI", "Cult UI", "Radix UI Primitives", "Lucide Icons"]
  conflitos_esteticos: ["Corporate Memphis pastel plano", "Neumorfismo skeuomórfico clássico", "Material Design 2 (sombras elevadas e cores primárias saturadas)", "Brutalismo Y2K cru sem transições"]
---

# Aceternity UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Aceternity UI**, idealizado e desenvolvido pelo engenheiro e designer Manu Arora, é um dos marcos mais influentes na evolução do design de interfaces na era pós-2023. A biblioteca consolidou a democratização da estética **"Dark Craft"** e da linguagem visual de ficção científica corporativa de alto padrão (popularizada globalmente por referências como Linear, Vercel, Supabase, Raycast e Apple), transformando interações complexas antes restritas a estúdios de design de ponta em código modular, legível e reutilizável para o ecossistema React.

A assinatura visual do Aceternity UI é construída sobre quatro pilares intransigentes:

1. **Iluminação Especular Volumétrica & Modelagem de Luz Virtual**:
   O Aceternity trata a tela não como uma superfície bidimensional opaca, mas como um palco escuro com fontes de luz ativas. Elementos como o célebre *Lamp Effect* simulam iluminação zenital através de cones em gradiente cônico (`conic-gradient`) e sombras difusas gaussianas (`blur-3xl`, `blur-[100px]`), criando um foco dramático sobre tipografias e produtos. Cartões e seções utilizam máscaras radiais (`mask-image: radial-gradient`) para revelar grids pontilhados ou lineares apenas nas proximidades do cursor ou do centro visual.

2. **Profundidade Cinemática & Perspectiva 3D Tátil**:
   Diferente de cartões comuns que apenas se elevam no eixo Y via sombras (`box-shadow`), os componentes do Aceternity (como o *3D Card Effect* e o *3D Pin*) operam no espaço de coordenadas tridimensionais do CSS (`transform: perspective(1000px) rotateX(...) rotateY(...)`). O diferencial técnico está no desacoplamento de profundidade em múltiplos níveis: títulos, imagens e botões de chamada possuem valores individuais de `translateZ`, fazendo com que os elementos internos literalmente "flutuem" a diferentes alturas quando o usuário move o mouse sobre o cartão.

3. **Partículas Vivas e Feixes com Simulação Física**:
   A biblioteca introduziu padrões dinâmicos onde a luz e a matéria interagem com o conteúdo. No *Background Beams with Collision*, raios luminosos percorrem uma malha invisível e, ao colidirem com os containers de texto ou elementos de interface, desencadeiam uma explosão estocástica de partículas calculadas via Canvas 2D. No *Sparkles Core*, constelações de micro-estrelas pulsam em escala e opacidade com ciclo orgânico, transmitindo a sensação de software alimentado por computação quântica ou inteligência artificial viva.

4. **Filosofia de Arquitetura Desacoplada (Copy-Paste / Zero Monolith)**:
   Seguindo a revolução originada pelo `shadcn/ui`, o Aceternity UI rejeita o modelo antiquado de dependências monolíticas empacotadas via NPM (que aprisionavam o projeto a temas fechados e dependências engessadas). Cada componente é distribuído como código-fonte aberto TypeScript + Tailwind + Framer Motion. O desenvolvedor copia o arquivo para o seu próprio diretório `components/ui/`, mantendo 100% de controle sobre a física da mola, paleta de cores, otimizações de acessibilidade e extensibilidade de regras de negócio.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados
1. **Startups de Inteligência Artificial, LLMs & Agentes Autônomos**:
   Interfaces conversacionais, plataformas de orquestração de IA e terminais cognitivos onde a identidade visual precisa evocar poder computacional massivo, precisão matemática e estética "next-generation".
2. **Developer Tools, Infraestrutura Cloud & Bancos de Dados Serverless**:
   Landing pages e painéis de observabilidade para engenheiros (no modelo Supabase, Neon, Prisma, Cloudflare). A combinação de tipografia monoespaçada, fundos pretos profundos e luzes especulares cria sintonia imediata com o público técnico sênior.
3. **Fintechs Institucionais, Criptografia & Web3**:
   Aplicações de alto valor transacional onde interfaces escuras imersivas e polidas transmitem sofisticação, estabilidade de nível de missão crítica e solidez tecnológica.
4. **Landing Pages de Lançamento de Alto Impacto & Portfólios de Creative Technologists**:
   Produtos que competem pela atenção imediata do usuário nos primeiros segundos de visita, necessitando de uma seção Hero hipnótica, seções de recursos em Bento Grid e transições de scroll memoráveis.

### Papel no Ritmo Visual (A Aplicação Rigorosa da Regra 60-30-10)

Para evitar que a interface se transforme em uma experiência caótica e cansativa, os componentes do Aceternity UI devem ser distribuídos segundo uma governança de pesos muito estrita:

- **60% — Fundação Neutra e Funcional (Base `shadcn/ui` + Tailwind)**:
  A estrutura de suporte **não deve** conter efeitos visuais complexos. O fundo dominante deve ser neutro profundo (`bg-black`, `bg-neutral-950` ou `bg-zinc-950`), a tipografia limpa e legível (`text-neutral-200`, `text-neutral-400`), os espaçamentos consistentes (`gap-4`, `p-6`, `max-w-7xl`) e a navegação utilitária estável.
- **30% — Camada Tátil de Fluidez e Navegação (Micro-interações Aceternity)**:
  Componentes de suporte contextual que refinam a usabilidade sem roubar a cena: a *Floating Dock* para atalhos de navegação, o *Bento Grid* para estruturar hierarquia visual entre cartões de funcionalidades, o *Animated Tooltip* para exibir avatares de equipe ou clientes, ou o *Placeholders and Vanish Input* em campos de newsletter/busca.
- **10% — Efeitos Showstoppers Protagonistas (Apenas 1 por Viewport)**:
  Os efeitos de choque visual (ex: *Lamp Effect*, *Background Beams*, *Hero Parallax*, *Macbook Scroll* ou *Aurora Background*). **Regra inegociável**: reserve o showstopper exclusivamente para o Hero principal ou para um bloco único de CTA final. Jamais coloque mais de um efeito de iluminação pesada ou colisão visível na mesma dobra da tela.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Painéis Operacionais Diários de Alta Frequência (ERPs, Backoffices, CRMs densos)**:
  Inserir cartões com inclinação 3D, bordas que correm em loop contínuo ou fundos brilhantes em interfaces onde o operador passa 8 horas preenchendo formulários ou lendo tabelas de 1.000 linhas causa fadiga visual extrema e degrada a performance do navegador.
- **Sistemas Governamentais, Saúde & Aplicações com Requisito WCAG AAA**:
  Efeitos de transparência com ruído, bordas sutis com baixa luminância em fundo escuro e animações perpétuas violam diretrizes estritas de contraste e provocam desorientação em usuários com deficiências visuais ou cognitivas.
- **Dispositivos Móveis de Baixo Custo / Ambientes de Economia de Bateria**:
  Múltiplos loops de Canvas 2D/WebGL e dezenas de instâncias de `framer-motion` escutando eventos de mouse ou recalculando posições via JS drenam a bateria rapidamente e derrubam o framerate de smartphones modestos para níveis inaceitáveis (< 20 FPS).

### ⚠️ A Síndrome do "AI Slop" & Como Evitar o Clichê Saturado
O Aceternity UI tornou-se vítima do seu próprio sucesso estrondoso: centenas de geradores de sites com IA e startups amadoras começaram a despejar todos os componentes da biblioteca em uma mesma página:
> *Hero com Lamp Roxo + Sparkles caindo + Background Beams cruzando + Botão com Moving Border + Bento Grid onde todos os cards têm 3D Tilt + Footer com Glowing Stars.*

Esse excesso desordenado é rotulado pejorativamente no mercado como **"AI Slop"** (lixo estético de IA) ou **"Vibe Coder Syndrome"** — uma interface que parece um parque de diversões neon sem substância, credibilidade ou identidade de marca real.

#### Diretrizes para Uso com Extrema Elegância:
1. **Desintoxicação Cromática (Fuja do Roxo/Ciano Padrão)**:
   O gradiente índigo-para-ciano (`#6366f1` / `#06b6d4`) tornou-se a marca registrada de templates genéricos de IA. Substitua-o pela paleta genuína do produto: use monocromia pura (tons de branco puro, prata e chumbo com brilho especular), âmbar/dourado refinado para fintechs, verde esmeralda desaturado para infraestrutura cloud, ou azul cobalto profundo.
2. **Atenuação de Opacidade (Subtle Luminescence)**:
   Reduza a força das máscaras de luz. Em vez de gradientes a 100% de opacidade, configure os feixes e lâmpadas para `opacity-20` ou `opacity-30`. A luz deve parecer um reflexo sutil em vidro escuro fosco, e não um laser de balada.
3. **Respeito Imperativo ao `prefers-reduced-motion`**:
   Sempre implemente verificação de acessibilidade: desative os feixes móveis, rotações 3D contínuas e animações de partículas para usuários que configuraram redução de movimento no sistema operacional.
4. **Isolamento de Showstoppers**:
   Se a dobra Hero usa o *Lamp Effect*, a seção seguinte em Bento Grid deve ser puramente estrutural, com bordas finas sólidas e no máximo um hover sutil de escala ou background tint.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 12 componentes mais emblemáticos da arquitetura do Aceternity UI:

### 1. Lamp Effect (O Abajur Zenital de Luz Linear)
- **Anatomia Visual**: Dois cones de gradiente cônico invertidos posicionados no topo da seção que convergem para uma barra horizontal luminosa central. Uma máscara radial e múltiplas camadas de desfoque (`blur-3xl`, `blur-[100px]`) criam a ilusão física de uma lâmpada arquitetônica projetando um feixe de luz que desce suavemente sobre o título principal e os badges.
- **Gatilho de Interação**: Animação de entrada inicial via `motion.div` (`initial={{ opacity: 0.5, width: "15rem" }}`, `whileInView={{ opacity: 1, width: "30rem" }}` com transição suave). Estático durante a leitura para não dispersar a atenção.
- **Onde encaixar**: Topo exclusivo da seção Hero ou cabeçalho monumental de seções especiais (ex: lançamento de versão principal v2.0).

### 2. Background Beams & Beams with Collision
- **Anatomia Visual**: Linhas de feixes luminosos finos que percorrem trilhas invisíveis em uma grade geométrica de fundo. Na variante *Collision*, os feixes viajam em velocidades variáveis e, ao tocarem as bordas de um container central (onde reside o texto ou mockup do produto), geram uma explosão de pequenas faíscas estocásticas que se dissipam no ar.
- **Gatilho de Interação**: Renderização contínua em Canvas 2D/SVG com animação procedural autônoma (`requestAnimationFrame`). Reage dinamicamente aos limites da caixa alvo calculada via `getBoundingClientRect()`.
- **Onde encaixar**: Fundo da dobra Hero, container de chamada final (Final CTA) ou backdrop da página de registro/login.

### 3. 3D Card Effect (Card Parallax com Perspectiva Multi-nível)
- **Anatomia Visual**: Container de cartão com perspectiva profunda (`perspective: 1000px`). Ao interagir com o ponteiro do mouse, o cartão se inclina nos eixos X e Y. Seus elementos filhos (foto, título, badges e botão) possuem a diretiva `translateZ(50px)` ou `translateZ(100px)`, projetando-se fisicamente para fora do cartão em diferentes camadas de altitude.
- **Gatilho de Interação**: `onMouseMove` que calcula a distância angular relativa ao centro do componente, interpolando valores angulares para rotação com desaceleração de mola (`spring`) e reset automático em `onMouseLeave`.
- **Onde encaixar**: Cards de destaque em Bento Grids, cartões de planos "Enterprise / Pro" na página de preços, ou exibição de projetos em portfólios.

### 4. 3D Pin / Pin Perspective (Marcador Holográfico Flutuante)
- **Anatomia Visual**: Um elemento ou link comum sobre o qual paira um pino de fixação tridimensional. Ao passar o mouse, o container se inclina para trás em perspectiva e projeta um feixe vertical luminoso encimado por uma etiqueta de título e círculos concêntricos pulsantes (ondas de radar) que emanam da base.
- **Gatilho de Interação**: Hover (`onMouseEnter` / `onMouseLeave`) disparando rotação em perspectiva 3D e expansão contínua de anéis de gradiente via CSS Keyframes/Framer Motion.
- **Onde encaixar**: Vitrines de repositórios do GitHub, links externos de documentação, mapa de nós de rede/servidores globais.

### 5. Floating Dock / Island Navigation (Dock estilo macOS com Magnificação)
- **Anatomia Visual**: Barra de ferramentas compacta flutuante com fundo em vidro fosco (`backdrop-blur-md bg-neutral-900/80 border border-white/10`). Inspirada no dock de aplicações da Apple, os ícones mantêm dimensões padrão, mas aumentam de escala fluidamente conforme o cursor se aproxima, contraindo suavemente os ícones vizinhos.
- **Gatilho de Interação**: Cálculo contínuo da distância euclidiana entre as coordenadas do mouse e o centro de cada ícone através de `useMotionValue` e `useTransform`, com física de mola rápida (`mass: 0.1, stiffness: 150, damping: 12`).
- **Onde encaixar**: Barra de navegação inferior permanente em web apps, ferramentas de produtividade, dashboards criativos e visualizadores de mídia.

### 6. Bento Grid (Composição Modular Assimétrica de Features)
- **Anatomia Visual**: Malha responsiva moderna dividida em colunas modulares (`grid-cols-1 md:grid-cols-3`), onde itens estratégicos expandem-se em `md:col-span-2` ou ocupam alturas estendidas. Cada cartão possui acabamento em `bg-neutral-900/50`, bordas tênues `border-white/10` e espaços dedicados para micro-gráficos, ilustrações ou demonstrações interativas.
- **Gatilho de Interação**: `whileHover` nos cartões individuais (leve deslocamento de 2 a 4 pixels no eixo Y ou ativação de iluminação de fundo no cabeçalho do cartão).
- **Onde encaixar**: Seção principal de recursos (Core Features / Platform Capabilities) logo após o Hero.

### 7. Hero Parallax (Perspectiva Tridimensional com Rolagem Assíncrona)
- **Anatomia Visual**: Uma composição monumental de três fileiras de cartões/screenshots de produto dispostas em um plano inclinado em 3D (`rotateX(15deg) rotateZ(-10deg) skewX(20deg)`). Conforme a página é rolada para baixo, as linhas pares e ímpares deslizam horizontalmente em direções opostas enquanto a seção inteira se endireita suavemente.
- **Gatilho de Interação**: Scroll-driven interativo atrelado ao `useScroll` e `useTransform`, mapeando a porcentagem de rolagem da janela diretamente para os deslocamentos `translateX` e a rotação angular.
- **Onde encaixar**: Seções de demonstração visual de múltiplos templates, vitrine de clientes ou seção central de ecossistema de integrações.

### 8. Placeholders and Vanish Input (Campo com Desintegração de Partículas)
- **Anatomia Visual**: Campo de input estilizado em pílula escura com borda fina. Seu placeholder textual alterna periodicamente entre perguntas ou comandos sugeridos através de um efeito sutil de deslizamento vertical. Ao pressionar `Enter` para submeter, o texto digitado é instantaneamente convertido em um mapa de pixels que se dissolve em uma nuvem de partículas que flutua e desaparece.
- **Gatilho de Interação**: Ciclo de tempo automatizado para rotação de placeholders; gatilho `onSubmit` que renderiza o texto em um elemento `<canvas>` invisível para extrair os pixels (`getImageData`) e disparar a animação física de dispersão.
- **Onde encaixar**: Barra de busca global (Cmd+K), campo de cadastro de waitlist no Hero, ou terminal de comandos de assistente de IA.

### 9. Moving Border (Borda com Cometa de Luz Orbitante)
- **Anatomia Visual**: Um botão ou cartão com bordas arredondadas onde um ponto ou segmento em gradiente ultra-brilhante corre continuamente em torno do perímetro, criando a ilusão de um feixe de energia confinado que delineia o formato do componente.
- **Gatilho de Interação**: Loop perpétuo acionado por CSS ou Framer Motion calculando a posição sobre uma rota SVG fechada (`rx`, `ry`), com aceleração ou intensificação de brilho sob o estado de `:hover`.
- **Onde encaixar**: Botão principal de conversão (Primary CTA), cartão do plano de preços mais recomendado ou card de alerta de status crítico.

### 10. Aurora Background (As Luzes do Norte Digitais)
- **Anatomia Visual**: Pano de fundo etéreo onde faixas fluidas de gradientes suaves em tons frios (índigo, ciano, violeta e verde profundo) movem-se lentamente com distorção orgânica sob uma máscara suave, criando uma atmosfera imersiva sem a agressividade de partículas pontuais.
- **Gatilho de Interação**: Animação em loop contínuo e suave (`duration: 20s, ease: "easeInOut", repeat: Infinity`) processada via propriedades de gradiente radial no CSS puro ou Canvas de baixíssimo custo.
- **Onde encaixar**: Background da dobra Hero em produtos voltados para criatividade, design, bem-estar digital ou soluções de IA amigáveis.

### 11. Tracing Beam (O Fio de Prumo de Leitura por Scroll)
- **Anatomia Visual**: Uma linha vertical delgada traçada na lateral esquerda do conteúdo que acompanha o comprimento total do artigo. Uma cabeça de feixe luminosa (com gradiente e indicador circular) corre pela linha sincronizada com o scroll, iluminando o segmento do texto que está atualmente visível na tela.
- **Gatilho de Interação**: Mapeamento do scroll relativo da página via `useScroll` e interpolação de SVG `stroke-dashoffset` através de `useTransform`.
- **Onde encaixar**: Documentações técnicas com passos sequenciais, changelogs de produto, estudos de caso e artigos longos em blogs de engenharia.

### 12. Sparkles Core & Glowing Stars Card (Campos Estelares Dinâmicos)
- **Anatomia Visual**: Camada densa de pequenas partículas quadradas ou circulares que cintilam aleatoriamente. No *Glowing Stars Card*, as estrelas permanecem em repouso e acendem progressivamente à medida que o cursor se aproxima das suas coordenadas na malha.
- **Gatilho de Interação**: Partículas em Canvas 2D de alta taxa de quadros ou matriz de nós DOM leves monitorando proximidade vetorial do mouse.
- **Onde encaixar**: Títulos comemorativos, cartões de conquistas, seções de estatísticas ("10 bilhões de tokens processados") e rodapés conceituais.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Ambiente

O Aceternity UI apoia-se em primitivas sólidas de ecossistema. Para suportar seus componentes em um projeto Next.js / React moderno com Tailwind CSS v3 ou v4:

```bash
# Instalação das dependências essenciais de animação e utilitários
npm install framer-motion clsx tailwind-merge lucide-react

# Para componentes específicos com 3D ou Canvas (opcional, sob demanda):
npm install cobe canvas-confetti simplex-noise @tsparticles/react
npm install -D @types/canvas-confetti
```

#### Utilitário de Interpolação de Classes (`lib/utils.ts`)
Todo componente do Aceternity faz uso da função padronizada `cn`:

```typescript
import { ClassValue, clsx } from "clsx";
import { twMerge } from "tailwind-merge";

export function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs));
}
```

#### Plugin Tailwind para Injeção de Variáveis de Cores (`tailwind.config.ts`)
Muitos efeitos do Aceternity (como feixes e gradientes de fundo) dependem de acessar as variáveis CSS da paleta do Tailwind. Adicione o helper no `tailwind.config.ts`:

```typescript
import type { Config } from "tailwindcss";
const { default: flattenColorPalette } = require("tailwindcss/lib/util/flattenColorPalette");

// Função para adicionar cada cor do Tailwind como variável CSS global (ex: --zinc-900)
function addVariablesForColors({ addBase, theme }: any) {
  const allColors = flattenColorPalette(theme("colors"));
  const newVars = Object.fromEntries(
    Object.entries(allColors).map(([key, val]) => [`--${key}`, val])
  );

  addBase({
    ":root": newVars,
  });
}

const config: Config = {
  content: [
    "./src/**/*.{ts,tsx}",
  ],
  darkMode: "class",
  theme: {
    extend: {},
  },
  plugins: [addVariablesForColors],
};
export default config;
```

---

### Física de Movimento, Molas & Coordenadas 3D

Para garantir a resposta tátil que caracteriza o Aceternity, as configurações de transição seguem valores específicos para cada tipo de componente:

1. **Magnificação Instantânea (Floating Dock)**:
   - Utiliza mola com baixíssima massa para que o ícone acompanhe o ponteiro sem parecer pesado ou arrastado:
   - `transition: { type: "spring", mass: 0.1, stiffness: 150, damping: 12 }`
2. **Amortecimento Tridimensional (3D Card Tilt)**:
   - Requer mola com maior amortecimento para evitar vibrações nas bordas ao mudar rapidamente de direção com o mouse:
   - `transition: { type: "spring", stiffness: 200, damping: 20, mass: 0.5 }`
3. **Revelação Zenital Cinematográfica (Lamp Effect)**:
   - Requer desaceleração gradual e elegante, evitando qualquer ressalto mecânico:
   - `transition: { duration: 0.8, ease: [0.25, 0.1, 0.25, 1.0], delay: 0.2 }`

---

### Receita de Código Funcional: 3D Card Effect com Profundidade Multi-Camada

Abaixo está a implementação de nível de produção do componente **3D Card** do Aceternity UI, demonstrando a arquitetura baseada em React Context, cálculo de rotação normalizada e projeção em profundidade através de `translateZ`:

```tsx
"use client";

import React, {
  createContext,
  useState,
  useContext,
  useRef,
  useEffect,
  useCallback,
} from "react";
import { cn } from "@/lib/utils";

// 1. Contexto para compartilhar o estado de hover e profundidade entre containers e filhos
const MouseEnterContext = createContext<
  [boolean, React.Dispatch<React.SetStateAction<boolean>>] | undefined
>(undefined);

export const CardContainer = ({
  children,
  className,
  containerClassName,
}: {
  children?: React.ReactNode;
  className?: string;
  containerClassName?: string;
}) => {
  const containerRef = useRef<HTMLDivElement>(null);
  const [isMouseEntered, setIsMouseEntered] = useState(false);

  const handleMouseMove = useCallback((e: React.MouseEvent<HTMLDivElement>) => {
    if (!containerRef.current) return;
    const { left, top, width, height } =
      containerRef.current.getBoundingClientRect();
    
    // Normalização das coordenadas (-1 a +1 relativo ao centro do cartão)
    const x = (e.clientX - left - width / 2) / 20; // Rotação máxima aproximada de +/- 15-20deg
    const y = (e.clientY - top - height / 2) / 20;

    containerRef.current.style.transform = `rotateY(${x}deg) rotateX(${-y}deg)`;
  }, []);

  const handleMouseEnter = () => {
    setIsMouseEntered(true);
  };

  const handleMouseLeave = () => {
    if (!containerRef.current) return;
    setIsMouseEntered(false);
    // Reset suave para o plano de repouso bidimensional
    containerRef.current.style.transform = `rotateY(0deg) rotateX(0deg)`;
  };

  return (
    <MouseEnterContext.Provider value={[isMouseEntered, setIsMouseEntered]}>
      <div
        className={cn("flex items-center justify-center py-6", containerClassName)}
        style={{ perspective: "1000px" }}
      >
        <div
          ref={containerRef}
          onMouseEnter={handleMouseEnter}
          onMouseMove={handleMouseMove}
          onMouseLeave={handleMouseLeave}
          className={cn(
            "relative transition-all duration-200 ease-out will-change-transform",
            className
          )}
          style={{ transformStyle: "preserve-3d" }}
        >
          {children}
        </div>
      </div>
    </MouseEnterContext.Provider>
  );
};

export const CardBody = ({
  children,
  className,
}: {
  children: React.ReactNode;
  className?: string;
}) => {
  return (
    <div
      className={cn(
        "h-96 w-96 [transform-style:preserve-3d] [&>*]:[transform-style:preserve-3d]",
        className
      )}
    >
      {children}
    </div>
  );
};

export const CardItem = ({
  as: Component = "div",
  children,
  className,
  translateX = 0,
  translateY = 0,
  translateZ = 0,
  rotateX = 0,
  rotateY = 0,
  rotateZ = 0,
  ...rest
}: {
  as?: React.ElementType;
  children: React.ReactNode;
  className?: string;
  translateX?: number | string;
  translateY?: number | string;
  translateZ?: number | string;
  rotateX?: number | string;
  rotateY?: number | string;
  rotateZ?: number | string;
  [key: string]: any;
}) => {
  const ref = useRef<HTMLDivElement>(null);
  const context = useContext(MouseEnterContext);
  const isMouseEntered = context ? context[0] : false;

  useEffect(() => {
    if (!ref.current) return;
    if (isMouseEntered) {
      ref.current.style.transform = `translateX(${translateX}px) translateY(${translateY}px) translateZ(${translateZ}px) rotateX(${rotateX}deg) rotateY(${rotateY}deg) rotateZ(${rotateZ}deg)`;
    } else {
      ref.current.style.transform = `translateX(0px) translateY(0px) translateZ(0px) rotateX(0deg) rotateY(0deg) rotateZ(0deg)`;
    }
  }, [isMouseEntered, translateX, translateY, translateZ, rotateX, rotateY, rotateZ]);

  return (
    <Component
      ref={ref}
      className={cn("transition-transform duration-200 ease-out will-change-transform", className)}
      {...rest}
    >
      {children}
    </Component>
  );
};
```

#### Exemplo Prático de Consumo:
```tsx
import Image from "next/image";
import { CardContainer, CardBody, CardItem } from "@/components/ui/3d-card";

export function ProductFeatureCard() {
  return (
    <CardContainer className="inter-var">
      <CardBody className="bg-neutral-950 relative group/card border-white/10 w-auto sm:w-[30rem] h-auto rounded-2xl p-6 border">
        {/* Camada 1: Título projetado a 50px de altitude */}
        <CardItem translateZ={50} className="text-xl font-bold text-white tracking-tight">
          Cluster de Inferência Neural
        </CardItem>
        
        {/* Camada 2: Descrição projetada a 60px */}
        <CardItem as="p" translateZ={60} className="text-neutral-400 text-sm max-w-sm mt-2">
          Latência sub-milissegundo com alocação elástica em GPUs H100.
        </CardItem>

        {/* Camada 3: Imagem técnica projetada a 100px */}
        <CardItem translateZ={100} className="w-full mt-4 overflow-hidden rounded-xl">
          <div className="h-44 w-full bg-gradient-to-br from-neutral-900 to-neutral-800 border border-white/5 flex items-center justify-center">
            <span className="text-xs font-mono text-neutral-500">GPU_TOPOLOGY_MATRIX</span>
          </div>
        </CardItem>

        {/* Camada 4: Barra de ação com botão flutuante a 40px */}
        <div className="flex justify-between items-center mt-6">
          <CardItem translateZ={20} as="a" href="#specs" className="text-xs text-neutral-400 hover:text-white transition-colors">
            Ver especificações →
          </CardItem>
          <CardItem translateZ={50} as="button" className="px-4 py-2 rounded-lg bg-white text-black text-xs font-semibold hover:bg-neutral-200 transition-colors">
            Implantar Agora
          </CardItem>
        </div>
      </CardBody>
    </CardContainer>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao redigir o documento de arquitetura de interface (`DESIGN_BLUEPRINT.md`) para uma nova aplicação, o agente ou arquiteto deve obedecer às seguintes diretrizes operacionais:

### 1. Declaração Formal da Biblioteca
```markdown
### Camada de Efeitos Especiais & Componentes Cinéticos
- **Biblioteca Primária**: Aceternity UI (padrão copy-paste sobre Tailwind CSS + Framer Motion).
- **Função no Projeto**: Componentes de alto impacto (Showstoppers - 10%) e transições contextuais (30%).
- **Fundação Estrutural (60%)**: shadcn/ui + Radix UI Primitives (inputs, formulários, tabelas, modais simples).
```

### 2. Matriz de Seleção e Dosagem por Seção
| Seção da Página | Componente Aceternity Recomendado | Papel Visual | Alternativa Leve (Low-Power) |
| :--- | :--- | :--- | :--- |
| **Hero Principal** | `LampEffect` OU `BackgroundBeams` | Showstopper (10%) | Gradiente radial estático com `bg-gradient-to-b` |
| **Navegação Global** | `FloatingDock` | Fluidez Tátil (30%) | Header fixo tradicional com `backdrop-blur-md` |
| **Grid de Recursos** | `BentoGrid` com `3DCard` no destaque | Estrutural + Destaque | Bento Grid com hover sutil de `border-white/20` |
| **Demonstração de Produto** | `MacbookScroll` OU `HeroParallax` | Showstopper Narrativo | Container com mockup estático e leve `fade-in` |
| **Busca / Waitlist** | `PlaceholdersAndVanishInput` | Interação Funcional | Input shadcn padrão com placeholder estático |
| **CTA Final** | `MovingBorder` no botão central | Ponto de Foco | Botão primário com `ring-1 ring-white/20` |

### 3. Checklist de Auditoria Anti-"AI Slop"
Antes de aprovar o layout, verifique os seguintes pontos obrigatórios:
- [ ] **Apenas 1 Showstopper por viewport**: A seção Hero NÃO combina Lamp Effect com Sparkles E Background Beams simultaneamente.
- [ ] **Customização de Cores**: As cores de iluminação foram customizadas para a identidade da marca, banindo o gradiente padrão roxo/ciano não intencional.
- [ ] **Degradação Elegante em Telas Móveis**: Em viewports menores que `768px`, efeitos de `perspective: 1000px` e rotações 3D contínuas são desativados via classes responsivas (`sm:rotate-0`) para poupar bateria e evitar saltos visuais ao toque.
- [ ] **Acessibilidade e Redução de Movimento**: O hook `useReducedMotion()` do Framer Motion está conectado às animações perpétuas, substituindo feixes móveis por layouts estáticos limpos para usuários sensíveis.
- [ ] **Performance de Renderização**: Elementos pesados com Canvas (como *Globe* ou *Beams with Collision*) são encapsulados em `next/dynamic` com `ssr: false` e carregados com `loading="lazy"`.
