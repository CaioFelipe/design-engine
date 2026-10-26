---
id: "spell-sh"
name: "Spell UI"
url: "https://spell.sh/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Tactile Micro-Interactions", "Creative Engineering & Shader Magic", "Dynamic Typographic Motion", "Polished Dark/Light Craft"]
densidade_informacao: "Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Motion/Canvas) a Alto (WebGL Shaders com Three.js)"
stack_frameworks: ["React 19", "Next.js 15/16 (App Router)", "Tailwind CSS v4", "Motion 12 (motion/react)", "Three.js", "Radix UI", "opentype.js", "Lucide React"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "Plus Jakarta Sans", "JetBrains Mono", "Cabinet Grotesk"]
  paletas_ideais: ["Zinc Dark Craft (#09090b / #18181b)", "Pure Clean White (#ffffff / #f4f4f5)", "Electric Indigo & Violet (#6366f1 / #8b5cf6)", "Amber & Emerald Tactile Accents"]
  combinacoes_recomendadas: ["Shadcn UI", "Magic UI", "Cult UI", "Skiper UI", "Number Flow"]
  conflitos_esteticos: ["Brutalismo cru sem suavização", "Corporate Memphis bidimensional ingênuo", "Skeuomorfismo pesado pré-iOS 7"]
---

# Spell UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo designer e creative engineer **Tom** (`@xxtomm`), o **Spell UI** (`spell.sh`) estabelece uma nova fronteira no ecossistema de componentes para React e Tailwind CSS: a transição de interfaces meramente funcionais para experiências de software táteis, lúdicas e ricas em engenharia criativa (*creative engineering*). Enquanto a maioria dos registros baseados em `shadcn/ui` replica padrões convencionais de caixas de diálogo, menus suspensos e botões cinzentos, o Spell UI investiga o que acontece quando o design de interação incorpora **física de partículas em tempo real**, **traçados caligráficos vetoriais derivados de fontes tipográficas**, **shaders GLSL/WebGL volumétricos** e **efeitos 3D com luzes reativas**.

A assinatura visual do Spell UI é reconhecível por quatro traços fundamentais:

1. **Micro-interações Físicas de Alta Fidelidade (Tactile Delight)**:
   Em vez de transições lineares genéricas (`transition: all 150ms ease`), o Spell UI projeta componentes que reagem com massa, gravidade e elasticidade. O *Pop Button* simula um botão físico com relevo biselado na base (`border-b-4 origin-bottom`) que afunda realisticamente sob pressão (`active:border-b-2 active:scale-y-95`). O *Animated Checkbox* não apenas troca de cor: a marca de verificação desenha seu traçado SVG (`pathLength: 0 -> 1`) simultaneamente ao surgimento de uma linha de rasura (*strike-through*) elástica no texto adjacente, gerando uma gratificação sensorial instantânea no usuário.

2. **Engenharia de Partículas Acoplada ao Cursor e Teclado**:
   Um dos exemplos mais notáveis de design engineering é o *Exploding Input*. Longe de ser um efeito pré-renderizado ou um GIF em loop, o componente calcula a largura do texto digitado via API `measureText` de um elemento `<canvas>` fora da tela, identifica as coordenadas geométricas exatas do cursor (*caret position*) e instancia partículas dinâmicas no DOM com forças de impulso vetorial, gravidade contínua e decaimento em tempo real via `requestAnimationFrame`.

3. **Caligrafia Vetorial Dinâmica via Análise de Tipografia (Font Path Tracing)**:
   O componente *Signature* resolve de forma engenhosa o problema de assinaturas digitais autênticas. Utilizando a biblioteca `opentype.js`, o Spell UI decodifica arquivos de fontes cursivas OpenType/TrueType (`.otf` / `.ttf`), extrai as curvas de Bézier nativas dos glifos individuais e as converte em caminhos `<motion.path />`. A renderização calcula as larguras de avanço e desenha a assinatura letra por letra com efeito de revelação progressiva por máscara SVG, emulando perfeitamente o fluxo de tinta de uma caneta-tinteiro.

4. **Iluminação Volumétrica e Shaders GLSL em WebGL (Three.js)**:
   Para seções de cabeçalho (*hero sections*) e planos de fundo de alta conversão, o Spell UI fornece componentes como *Light Rays* e *Animated Gradient*. Em vez de sobrecarregar o CSS com gradientes radiais pesados ou vídeos de fundo estáticos, ele renderiza shaders GLSL customizados diretamente na GPU via Three.js, gerando feixes de luz volumétricos cáusticos, distorções cromáticas senoidais e movimentos de plasma líquido com consumo inteligente de ciclos de máquina.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **Produtos de Inteligência Artificial & Ferramentas de Criação**:
   Interfaces de prompts geradores, agentes autônomos e estúdios criativos beneficiam-se intensamente de componentes que demonstram "magia visual". O efeito de partículas no campo de digitação (*Exploding Input*) ou o fundo luminescente (*Light Rays*) transmitem a sensação de um motor inteligente e vivo operando sob o capô.
2. **Landing Pages de SaaS B2B Moderno & DevTools de Vanguarda**:
   Plataformas que competem por desenvolvedores e designers (como ferramentas de observabilidade, infraestrutura em nuvem e APIs) utilizam componentes como *Tilt Card*, *Perspective Book* e *Words Stagger* para criar páginas de produto que se destacam de clones corporativos genéricos.
3. **Fluxos de Fechamento de Contrato, Assinaturas Digitais & Onboarding**:
   O componente *Signature* é a solução perfeita para termos de aceite, finalizações de contrato de trabalho, certificações online ou telas de checkout de assinaturas executivas, transformando um momento burocrático em uma celebração visual memorável.
4. **Portfólios de Creative Technologists & Engenheiros Frontend**:
   Desenvolvedores que precisam comunicar domínio estético e capacidade técnica encontram no catálogo do Spell UI o repertório exato de cartões 3D, badges interativos e tipografia dinâmica para estruturar cases de alto nível.
5. **Widgets de Mídia e Prova Social Estilizada**:
   Aplicações que integram consumo musical (*Spotify Card* com desfoque de capa dinâmico) ou prova social de influenciadores (*Tweet Card* reestilizado) contam com soluções prontas, sem a rigidez dos iframes padrão de terceiros.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Neutra e Sólida)**:
   Telas limpas com Tailwind CSS v4 e Shadcn UI: fundos `bg-zinc-950` ou `bg-white`, hierarquia tipográfica padrão com `Geist Sans` ou `Inter`, bordas sutis `border-zinc-800/60` e grades utilitárias bem espaçadas.
- **30% (Camada Tátil e Micro-interações do Spell UI)**:
   Utilização frequente e distribuída de elementos com física: *Pop Button* para botões primários e de ação positiva, *Animated Checkbox* em listas de tarefas/features, *Copy Button* com desfoque suave para blocos de código e comandos de terminal, e *Tilt Card* com spotlight radial em grades de funcionalidades (Bento Grids).
- **10% (Showstoppers Protagonistas & Efeitos de Destaque)**:
   Limite rigoroso de **um** showstopper por dobra visual: ou os *Light Rays* volumétricos como fundo do Hero, ou a *Signature* desenhada no manifesto final de encerramento, ou o *Exploding Input* como a caixa de pesquisa central da página inicial. A sobreposição simultânea de dois showstoppers gera saturação sensorial e destrói o refinamento estético da interface.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Painéis Financeiros de Auditoria, ERPs e Tabelas de Alta Densidade**:
   Em ferramentas de gestão contábil, prontuários eletrônicos ou terminais de trading, efeitos táteis de partículas (*Exploding Input*) ou rotações 3D distorcem o alinhamento visual e aumentam a latência perceptiva do usuário durante operações repetitivas em lote.
- **Formulários Extensos com Dezenas de Campos**:
   Adicionar física de partículas a múltiplos inputs em um mesmo formulário consome recursos excessivos de CPU/GPU, dispara mutações DOM desnecessárias e distrai o usuário do preenchimento dos dados.
- **Aplicações Estritamente Críticas com Baixa Capacidade de Hardware (Thin Clients / PDVs)**:
   Os componentes WebGL baseados em Three.js (`Light Rays` e `Animated Gradient`) demandam contexto de aceleração gráfica por hardware. Em navegadores embarcados ou dispositivos com GPUs desprovidas de suporte WebGL robusto, isso pode provocar travamentos no pipeline de pintura do navegador.
- **Cenários de Acessibilidade Rigorosa sem Gestão de Movimento Reduzido**:
   Tipografias cinéticas (*Words Stagger*, *Gradient Wave Text*) e animações com rotação tridimensional contínua exigem fallback obrigatório com `@media (prefers-reduced-motion: reduce)`. Sem essa salvaguarda, usuários propensos a distúrbios vestibulares podem sofrer náuseas e desorientação visual.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **Multiplicação de Botões 3D Coloridos**: Usar dezenas de *Pop Buttons* com cores berrantes na mesma visualização, fazendo a interface parecer uma vitrine infantil ou um jogo de brinquedo desorganizado.
- **Light Rays Descalibrados sem Máscara de Contraste**: Configurar intensidade de luz acima de `0.3` no componente *Light Rays* sem uma camada de escurecimento sobreposta, tornando o texto principal do Hero completamente ilegível.
- **Ignorar o Tamanho de Download de Fontes no Componente Signature**: Carregar fontes `.otf` completas de 5MB sem subsetting de glifos na rede móvel do usuário apenas para desenhar uma frase de três palavras.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 12 componentes mais emblemáticos do registro oficial do **Spell UI** (`xxtomm/spell-ui` / `spell.sh`):

### 1. Light Rays (`light-rays.tsx`)
- **Anatomia Visual**: Plano de fundo volumétrico atmosférico gerado via Three.js e shaders GLSL. Dois eixos de projeção luminosa (`u_rayPos1`, `u_rayPos2`) emitem raios cáusticos diagonais que se entrelaçam suavemente sobre uma superfície escura ou colorida, com gradiente de atenuação configurável e taxa de propagação orgânica.
- **Gatilho de Interação**: Animação contínua baseada em `requestAnimationFrame` com cálculo de tempo decorrido (`u_time`), reagindo estaticamente ou dinamicamente aos parâmetros de alcance (`reach`), intensidade e velocidade.
- **Onde encaixar**: Plano de fundo do *Hero*, seção de demonstração principal de produto ou banner comemorativo de lançamento.

### 2. Signature (`signature.tsx`)
- **Anatomia Visual**: Assinatura caligráfica vetorial executada com precisão tipográfica. Ao invés de uma imagem vetorial estática, o componente recebe uma string textual, decodifica a geometria dos caracteres via `opentype.js`, gera os dados de caminho (`d="M..."`) e desenha cada glifo progressivamente utilizando máscaras SVG dinâmicas com traços arredondados (`strokeLinecap: round`).
- **Gatilho de Interação**: Disparado ao entrar no campo de visão (`whileInView`) com controle de disparo único (`once: true`) ou na montagem do componente, com suporte a atrasos escalonados por caractere (`PATH_DELAY_STEP = 0.2s`).
- **Onde encaixar**: Rodapé institucional, manifesto de fundadores, cartão de garantia de qualidade ou fluxo de conclusão de assinatura contratual.

### 3. Exploding Input (`exploding-input.tsx`)
- **Anatomia Visual**: Campo de entrada de texto comum enriquecido com uma explosão vetorial de partículas. Conforme o usuário tecla qualquer letra, pequenos blocos coloridos ou nós React customizados são projetados a partir do ponto focal exato do cursor de texto, subindo e caindo em arco parabólico com rotação angular e desvanecimento gradual de opacidade.
- **Gatilho de Interação**: Evento nativo `input` do elemento `<input />` do HTML. Mede a largura das letras via contexto de canvas 2D (`measureText`), calcula a coordenada $X$ e $Y$ do cursor e injeta partículas no container flutuante.
- **Onde encaixar**: Barra de pesquisa principal da página inicial, campo de comando/prompt de agentes de IA ou formulário de newsletter no rodapé.

### 4. Pop Button (`pop-button.tsx`)
- **Anatomia Visual**: Botão com forte fisicalidade tridimensional inspirado em teclas de teclado mecânico e botões tácteis de alta precisão. Apresenta bordas laterais e superiores de 2px (`border-x-2 border-t-2`) com borda inferior acentuada de 4px (`border-b-4 origin-bottom`) em tons mais escuros. Sob clique, a borda inferior diminui para 2px e o elemento sofre compressão elástica no eixo $Y$ (`active:scale-y-95`).
- **Gatilho de Interação**: Estado ativo (`:active`) acionado por mouse down ou toque tátil, operando via Tailwind CSS nativo e utilitário `Slot` do Radix UI para polimorfismo.
- **Onde encaixar**: Botão principal de chamada para ação (*CTA*), botões de confirmação de compra, botões de ação gamificados ou seletores de plano em páginas de preço.

### 5. Tilt Card (`tilt-card.tsx`)
- **Anatomia Visual**: Cartão tridimensional interativo que reage à posição do cursor do usuário no espaço euclidiano. À medida que o ponteiro se move sobre a superfície, a matriz `transform: perspective(1200px) rotateX(...) rotateY(...) scale3d(...)` inclina a peça para frente ou para longe, acompanhada por uma lanterna difusa (*radial-gradient spotlight*) que ilumina a textura superficial.
- **Gatilho de Interação**: Eventos contínuos de ponteiro (`onPointerMove`, `onPointerLeave`) com interpolação suave via `transition: transform 0.2s ease-out` e controle de modo ("gravitate" ou "evade").
- **Onde encaixar**: Cartões de funcionalidades no *Bento Grid*, cartões de precificação de nível Pro/Enterprise ou vitrines de portfólio.

### 6. Perspective Book (`perspective-book.tsx`)
- **Anatomia Visual**: Reconstrução tridimensional purista de um livro ou manual físico fechado. Possui capa frontal com espessura translúcida, lombada lateral chanfrada (`rotateY(90deg)`) com textura linear acetinada e contracapa traseira profundizada em `translateZ(-25px)`. Ao passar o mouse, a estrutura gira sutilmente em perspectiva axial revelando seu volume tridimensional.
- **Gatilho de Interação**: Transições CSS puras acionadas por `:hover` e estilos de perspectiva 3D (`transform-style: preserve-3d`).
- **Onde encaixar**: Seções de guias e documentação, vitrine de e-books técnicos, relatórios de mercado para download ou manuais de marca.

### 7. Animated Checkbox (`animated-checkbox.tsx`)
- **Anatomia Visual**: Caixa de seleção compacta com cantos arredondados de 6px (`rounded-[6px]`) acompanhada de um rótulo tipográfico legível. Ao ser alternada, o ícone de marcação desenha sua linha SVG de forma progressiva com suavização `easeOut`, enquanto uma linha horizontal de rasura (*strike-through*) corta o texto lateral simultaneamente através de uma mola elástica com leve amortecimento (`bounce: 0.2`).
- **Gatilho de Interação**: Clique do mouse ou evento de toque no container pai, emitindo o novo booleano via callback `onCheckedChange`.
- **Onde encaixar**: Listas de tarefas em dashboards, caixas de aceite de termos, listas de pré-requisitos em onboarding de usuários ou tabelas comparativas de recursos.

### 8. Words Stagger & Blur Reveal (`words-stagger.tsx` / `blur-reveal.tsx`)
- **Anatomia Visual**: Animação de revelação tipográfica na qual o texto fornecido é fragmentado em palavras ou caracteres individuais. Cada palavra emerge de uma posição deslocada em 10px no eixo vertical (`y: 10 -> 0`), transitando de um desfoque de 10px para foco nítido (`filter: blur(10px) -> blur(0px)`) e opacidade zero para 100%, em cascata com atraso escalonado (`staggerChildren: 0.1s`).
- **Gatilho de Interação**: Disparado ao rolar a página até a visibilidade do elemento (`whileInView`) com retenção permanente (`viewport: { once: true }`).
- **Onde encaixar**: Títulos principais e subtítulos de impacto na seção Hero, frases de manifesto corporativo ou citações em destaque.

### 9. Copy Button com Desfoque Fluido (`copy-button.tsx`)
- **Anatomia Visual**: Botão utilitário em pílula ou quadrado discreto com ícone de prancheta (`Copy`). Quando acionado, o ícone sofre uma transição rápida com desfoque e rotação suave enquanto o ícone de confirmação (`Check`) surge em verde esmeralda ou branco luminar, revertendo ao estado inicial após um temporizador de 2 segundos.
- **Gatilho de Interação**: Clique do mouse; aciona a Clipboard API do navegador e executa o feedback visual de transição de estado.
- **Onde encaixar**: Linhas de comando de instalação via terminal (`npx ...`), blocos de código com destaque de sintaxe, ou campos de chave de API em dashboards de desenvolvedor.

### 10. Spotify Card (`spotify-card.tsx`)
- **Anatomia Visual**: Cartão de mídia imersivo que extrai metadados em tempo real de faixas e álbuns do Spotify. Exibe a capa em alta definição com cantos arredondados, título da canção, artista, logotipo oficial da plataforma e um plano de fundo gerado a partir do desfoque gaussiano da própria capa do álbum, criando uma atmosfera visual coesa e sofisticada.
- **Gatilho de Interação**: Hover com leve escala e clique que redireciona diretamente para a reprodução nativa na plataforma de streaming.
- **Onde encaixar**: Páginas de perfil pessoal ("Sobre mim"), seções de preferências culturais em portfólios, ou integrações de reprodução sonora em comunidades web.

### 11. Animated Gradient Swirl (`animated-gradient.tsx`)
- **Anatomia Visual**: Malha cromática contínua acelerada por GPU que projeta vórtices e redemoinhos fluidos de cores complementares. Ao contrário de animações CSS comuns com `background-position`, este componente calcula a difusão e convecção dos fluidos matematicamente, resultando em misturas orgânicas sem repetição perceptível de ciclos.
- **Gatilho de Interação**: Loop procedural contínuo com opções de controle para velocidade, turbulência e suavidade das ondas cromáticas.
- **Onde encaixar**: Fundo de cartões de conversão (Pricing Cards destacados), fundos de modais de boas-vindas ou banners promocionais de rodapé.

### 12. QR Code com Módulos Arredondados (`qr-code.tsx`)
- **Anatomia Visual**: Gerador vetorial de códigos QR que rompe com a estética rígida e pixelada tradicional. Os localizadores angulares (*finder patterns*) e os módulos individuais de dados recebem cantos perfeitamente arredondados em formato de pastilha ou círculo suave, harmonizando com interfaces modernas e elegantes.
- **Gatilho de Interação**: Renderização dinâmica baseada no parâmetro textual/URL de entrada, com suporte a download em PNG/SVG e alteração de cor de preenchimento.
- **Onde encaixar**: Modais de autenticação de dois fatores (2FA), transições para aplicativos mobile em landing pages desktop ou doações em cripto.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Ambiente

O **Spell UI** opera segundo o padrão de arquitetura modular distribuída inaugurado pelo `shadcn/ui`. Não existe uma biblioteca empacotada monolítica instalada via `npm install spell-ui`; em vez disso, cada componente é importado diretamente como código-fonte TypeScript para a pasta `@/components/spell-ui` ou `@/components/ui` do projeto consumidor.

Para inicializar o suporte completo aos componentes do Spell UI em uma aplicação Next.js (App Router) com Tailwind CSS v4, configure as dependências essenciais:

```bash
# 1. Dependências centrais de animação e utilitários
npm install motion clsx tailwind-merge @radix-ui/react-slot lucide-react

# 2. Dependências para componentes visuais avançados (Three.js / OpenType / Mídia)
npm install three opentype.js @types/opentype.js qrcode @types/qrcode @icons-pack/react-simple-icons

# 3. Adicionar componentes diretamente via Shadcn CLI a partir do registro do Spell UI
npx shadcn@latest add "https://spell.sh/r/pop-button.json"
npx shadcn@latest add "https://spell.sh/r/animated-checkbox.json"
npx shadcn@latest add "https://spell.sh/r/words-stagger.json"
npx shadcn@latest add "https://spell.sh/r/tilt-card.json"
```

---

### Física de Movimento, Equações & Curvas de Transição

O refinamento das animações do Spell UI provém da combinação precisa de parâmetros de molas elásticas (*spring physics*), equações diferenciais de movimento e interpolação procedural:

1. **Física Tátil em Checkboxes e Controles (Springs Suaves)**:
   ```ts
   const springTransition = {
     type: "spring" as const,
     duration: 0.4, // Duração de 400ms para resposta ágil
     bounce: 0.2,   // Reversão elástica de 20%, garantindo retorno natural sem trepidação
   };
   ```

2. **Equações Cinemáticas do Motor de Partículas (`ExplodingInput`)**:
   O cálculo de deslocamento das partículas a cada quadro de animação segue a integração linear simplificada de Euler sobre o delta de tempo medido:
   $$\Delta t = \frac{\min(32, \Delta t_{\text{real}})}{1000}$$
   $$v_y(t + \Delta t) = v_y(t) + g \cdot \Delta t \quad \text{onde } g \in [-2000, 2000] \text{ px/s}^2$$
   $$x(t + \Delta t) = x(t) + v_x \cdot \Delta t$$
   $$y(t + \Delta t) = y(t) + v_y \cdot \Delta t$$
   O decaimento de opacidade é postergado para os últimos 30% do tempo de vida da partícula ($progress > 0.7$), garantindo visibilidade nítida antes da desintegração.

3. **Cálculo Angular de Perspectiva 3D (`TiltCard`)**:
   Ao capturar a coordenada normalizada do ponteiro $P_x, P_y \in [0, 1]$ em relação à caixa delimitadora do cartão:
   $$\theta_{\text{rotX}} = (P_y - 0.5) \cdot (2 \cdot \theta_{\text{limit}}) \cdot d$$
   $$\theta_{\text{rotY}} = -(P_x - 0.5) \cdot (2 \cdot \theta_{\text{limit}}) \cdot d$$
   Onde $d \in \{-1, 1\}$ determina se o elemento foge da direção do mouse (*evade*) ou se inclina em sua direção (*gravitate*).

---

### Receitas de Código Funcionais

Abaixo estão as implementações completas e prontas para produção de dois dos componentes mais expressivos da biblioteca:

#### Receita 1: `PopButton.tsx` (Botão com Física Mecânica 3D e Polimorfismo Radix)

```tsx
"use client";

import * as React from "react";
import { Slot } from "@radix-ui/react-slot";
import { cn } from "@/lib/utils";

type ButtonColor =
  | "default"
  | "primary"
  | "indigo"
  | "emerald"
  | "rose"
  | "amber";

type ButtonSize = "sm" | "default" | "lg";

export interface PopButtonProps
  extends React.ButtonHTMLAttributes<HTMLButtonElement> {
  color?: ButtonColor;
  size?: ButtonSize;
  children: React.ReactNode;
  asChild?: boolean;
}

export const PopButton = React.forwardRef<HTMLButtonElement, PopButtonProps>(
  (
    {
      className,
      color = "default",
      size = "default",
      children,
      asChild = false,
      ...props
    },
    ref
  ) => {
    const Comp = asChild ? Slot : "button";

    const baseClasses =
      "inline-flex select-none transition-all duration-100 ease-out items-center justify-center font-medium whitespace-nowrap rounded-xl ring-offset-background focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50 border-x-2 border-t-2 border-b-4 origin-bottom active:border-b-2 active:scale-y-95 active:translate-y-[2px]";

    const colorVariants: Record<ButtonColor, string> = {
      default:
        "bg-white hover:bg-neutral-50 border-neutral-300 text-neutral-900 shadow-sm dark:bg-neutral-800 dark:hover:bg-neutral-700 dark:border-neutral-950 dark:text-neutral-100",
      primary:
        "bg-zinc-900 hover:bg-zinc-800 border-black text-white dark:bg-zinc-100 dark:hover:bg-white dark:border-zinc-400 dark:text-zinc-950",
      indigo:
        "bg-indigo-600 hover:bg-indigo-500 border-indigo-900 text-white shadow-indigo-500/20",
      emerald:
        "bg-emerald-600 hover:bg-emerald-500 border-emerald-900 text-white shadow-emerald-500/20",
      rose:
        "bg-rose-600 hover:bg-rose-500 border-rose-900 text-white shadow-rose-500/20",
      amber:
        "bg-amber-500 hover:bg-amber-400 border-amber-800 text-amber-950 shadow-amber-500/20",
    };

    const sizeVariants: Record<ButtonSize, string> = {
      sm: "h-9 px-3 text-xs gap-1.5",
      default: "h-11 px-5 text-sm gap-2",
      lg: "h-14 px-8 text-base gap-2.5",
    };

    return (
      <Comp
        ref={ref}
        className={cn(baseClasses, colorVariants[color], sizeVariants[size], className)}
        {...props}
      >
        {children}
      </Comp>
    );
  }
);

PopButton.displayName = "PopButton";
```

---

#### Receita 2: `AnimatedCheckbox.tsx` (Caixa de Seleção com Strikethrough Elástico e Traçado SVG)

```tsx
"use client";

import * as React from "react";
import { motion, type Transition } from "motion/react";
import { cn } from "@/lib/utils";

interface AnimatedCheckboxProps {
  label: string;
  defaultChecked?: boolean;
  className?: string;
  onCheckedChange?: (checked: boolean) => void;
}

const springConfig: Transition = {
  type: "spring",
  duration: 0.35,
  bounce: 0.2,
};

export function AnimatedCheckbox({
  label,
  defaultChecked = false,
  className,
  onCheckedChange,
}: AnimatedCheckboxProps) {
  const [checked, setChecked] = React.useState<boolean>(defaultChecked);

  const toggleState = () => {
    const nextState = !checked;
    setChecked(nextState);
    onCheckedChange?.(nextState);
  };

  return (
    <div
      role="checkbox"
      aria-checked={checked}
      tabIndex={0}
      onKeyDown={(e) => {
        if (e.key === " " || e.key === "Enter") {
          e.preventDefault();
          toggleState();
        }
      }}
      onClick={toggleState}
      className={cn(
        "group flex items-center gap-3.5 cursor-pointer select-none py-1.5 px-2 rounded-lg transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-indigo-500",
        className
      )}
    >
      {/* Box do Checkbox */}
      <div
        className={cn(
          "relative flex items-center justify-center size-5 rounded-md border transition-all duration-200 ease-out",
          checked
            ? "bg-indigo-600 border-indigo-600 shadow-sm"
            : "bg-transparent border-zinc-400/60 dark:border-zinc-600 group-hover:border-zinc-500 dark:group-hover:border-zinc-400"
        )}
      >
        <svg
          viewBox="0 0 20 20"
          className="size-3.5 text-white pointer-events-none"
          fill="none"
        >
          <motion.path
            d="M 3 10.5 L 7.5 15 L 17 5"
            stroke="currentColor"
            strokeWidth={2.2}
            strokeLinecap="round"
            strokeLinejoin="round"
            initial={false}
            animate={{
              pathLength: checked ? 1 : 0,
              opacity: checked ? 1 : 0,
            }}
            transition={{
              pathLength: { duration: 0.25, ease: "easeOut" },
              opacity: { duration: 0.1 },
            }}
          />
        </svg>
      </div>

      {/* Rótulo com Risca Elástica */}
      <div className="relative inline-block">
        <span
          className={cn(
            "text-sm font-medium transition-colors duration-200",
            checked
              ? "text-zinc-400 dark:text-zinc-500"
              : "text-zinc-800 dark:text-zinc-200"
          )}
        >
          {label}
        </span>
        <motion.div
          className="absolute left-0 top-1/2 h-[1.5px] bg-zinc-400 dark:bg-zinc-500 origin-left -translate-y-1/2 pointer-events-none"
          initial={false}
          animate={{
            width: checked ? "100%" : "0%",
            opacity: checked ? 0.8 : 0,
          }}
          transition={springConfig}
        />
      </div>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar o **Spell UI** para compor o ecossistema de interface de um projeto, a IA deve transcrever e aplicar as seguintes diretrizes na seção de Arquitetura de UI e Frontend:

### Declaração de Stack & Dependências
- **Motion Engine**: Utilizar estritamente o pacote `motion` versão 12+ (`import { motion } from "motion/react"`), evitando versões obsoletas de `framer-motion` v10/v11 para garantir compatibilidade com React 19 e App Router do Next.js.
- **CSS Framework**: Integrar plenamente com `@tailwindcss/postcss` versão 4 e utilitários auxiliares `clsx` e `tailwind-merge` através do helper padrão `cn(...)`.

### Governança Visual & Prevenção de Fadiga (Anti-Slop Guardrails)
- **Regra de Unicidade de Showstopper**: O blueprint deve vetar a presença concomitante de múltiplos efeitos imersivos pesados na mesma seção. Se a Hero declarar `Light Rays` via Three.js, os botões secundários devem ser minimalistas e os títulos devem adotar animações suaves de opacidade, sem misturar partículas ou distorções caleidoscópicas.
- **Isolamento de Partículas**: Componentes que disparam partículas em tempo real (`ExplodingInput`) devem ser instanciados com moderação. Declarar seu uso prioritário na barra de pesquisa principal ou no terminal de comandos rápidos, nunca em formulários tabulares densos.
- **Respeito à Preferência do Usuário (`Reduced Motion`)**: Todo componente tipográfico do Spell UI (`WordsStagger`, `SlideUpText`, `RandomizedText`) deve possuir a cláusula de conformidade de acessibilidade:
  ```tsx
  // Diretriz mandatória no Blueprint
  const shouldReduceMotion = useReducedMotion();
  const transition = shouldReduceMotion ? { duration: 0 } : defaultTransition;
  ```

### Integração no Sistema de Design (Tokenização)
- No `DESIGN_BLUEPRINT.md`, definir as cores dos botões táteis (`PopButton`) alinhadas às variáveis CSS semânticas do Shadcn (`--primary`, `--ring`, `--muted`), preservando a consistência cromática entre componentes padrão e as peças com física 3D do Spell UI.
