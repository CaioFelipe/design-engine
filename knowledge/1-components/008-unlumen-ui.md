---
id: "unlumen-ui"
name: "Unlumen UI"
url: "https://ui.unlumen.com/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Dark Craft & Vercel Polish", "Restrained Motion & Tactility", "Progressive Blur & Micro-Borders", "Kinetic Typography & Shaders"]
densidade_informacao: "Media"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Framer Motion/JS) a Alto (Canvas/WebGL Shaders)"
stack_frameworks: ["React", "Next.js", "TypeScript", "Tailwind CSS", "Motion (motion/react & framer-motion)", "shadcn CLI"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Geist Mono", "Inter", "Plus Jakarta Sans", "Instrument Serif (Display/Headlines)"]
  paletas_ideais: ["Deep Neutral Zinc / Obsidian (Zinc 950 / Black)", "High-Contrast Monochrome", "Emerald Accent Glow (#34c759 / Emerald 400)", "Subtle Oklch Tint Gradients"]
  combinacoes_recomendadas: ["Shadcn UI", "Magic UI", "Cult UI", "Aceternity UI", "Radix UI Primitives"]
  conflitos_esteticos: ["Neobrutalismo hiper-saturado com contornos grossos de 4px", "Glassmorphism pastel desbotado sem contraste", "Skeuomorfismo pesado desprovido de alinhamento tipográfico"]
---

# Unlumen UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e desenhado pelo designer e desenvolvedor independente **Léo** ([@leouiux](https://x.com/leouiux) / [unlumen.com](https://unlumen.com)), o **Unlumen UI** (`ui.unlumen.com`) é um registro aberto e avançado de componentes React construídos sobre **TypeScript**, **Tailwind CSS**, **Motion (`motion/react`)** e distribuição modular via **shadcn CLI**. A biblioteca parte de um manifesto claro e maduro de engenharia de produto: *"Design is one of the first signals a product sends. Components shaped with care, motion, and restraint"*.

Enquanto muitas bibliotecas modernas de motion pecam pelo exibicionismo tecnológico estridente — enchendo a tela com partículas infinitas, neons concorrentes e delays artificiais —, o Unlumen UI busca a perfeição sóbria da escola **Vercel Dark Craft** e da ergonomia de software da **Apple**. Seus componentes são calibrados para responder na escala dos milissegundos com peso tátil (*haptics visuais*), sensação de matéria física e acabamento cirúrgico de bordas e luz.

A assinatura visual e técnica do Unlumen UI é sintetizada em quatro alicerces fundamentais:

1. **A 'Regra da Contenção' (Restrained Motion & Natural Springs)**:
   A física das animações do Unlumen UI nunca é puramente linear nem teatralmente lenta. Em vez de durações genéricas de `0.3s ease`, o ecossistema é governado por molas de alta precisão (`thumbSpring: stiffness: 700, damping: 48, mass: 0.55`; `grabSpring: stiffness: 500, damping: 25`; `menuSpring: stiffness: 400, damping: 28`). As transições possuem resposta instantânea ao clique ou arraste do ponteiro (`pointer capture`), com efeitos de deformação elástica (*squash & stretch*) e amortecimento sem ressalto excessivo (*overshoot* indesejado).

2. **Progressive Blur & Múltiplas Camadas de Profundidade Óptica**:
   Um dos diferenciais mais emblemáticos do Unlumen UI é o pioneirismo no uso de **Progressive Blur** estrutural (como visto nos headers e footers do site). Em vez de um único elemento com `backdrop-blur-md` estático que corta o conteúdo bruscamente com uma linha dura, o Unlumen empilha camadas vetoriais mascaradas com `maskImage: linear-gradient(...)` e `backdropFilter: blur(...)` gradual escalonado (`0.125rem` → `0.188rem` → `0.25rem` → `0.375rem`), dissolvendo suavemente o conteúdo que rola por baixo sem artefatos visuais.

3. **Micro-Bordas em Luz Difusa & Cores Oklch**:
   As superfícies neutras utilizam tokens refinados baseados no espaço de cores perceptual `oklch`, mesclando fundos com `color-mix(in srgb, var(--background) 82%, transparent)`. As bordas adotam espessuras ultrafinas de 1px (`border-white/10` em dark mode e `border-black/5` em light mode), pontuadas por detalhes especulares via gradientes radiais internos (`inset 0 1px 0 rgba(255,255,255,0.78)` e `box-shadow` multicamada).

4. **Distribuição Nativa shadcn/ui & Arquitetura MCP**:
   O Unlumen UI não impõe um pacote monolítico via NPM. Cada componente é distribuído como código-fonte independente através do schema oficial de registros shadcn (`https://ui.unlumen.com/r/{name}.json`), oferecendo um catálogo gratuito (*Free Tier*) de alta relevância e uma camada profissional (*Pro Tier*) autenticada por chave de licença Polar (`UNLUMEN_LICENSE_KEY`), integrando-se nativamente a ambientes de IA (MCP servers, Claude Code, Cursor e Copilot).

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **SaaS B2B de Alta Performance & Developer Tools (DevTools)**:
   Perfeito para ferramentas de observabilidade, consoles de cloud, plataformas de deploy, terminais web e dashboards de CI/CD que desejam transmitir confiabilidade corporativa através de um padrão estético equiparado a referências como Vercel, Supabase e Raycast.
2. **Plataformas de Inteligência Artificial & AI Workspaces**:
   Ideal para aplicações de agentes generativos, chat multimodal e workspaces de prompt engineering que exigem componentes com estados de feedback interativos, como o *Favicon Search*, *Animated Input*, *AI Chat* e *Matrix*.
3. **Landing Pages Institucionais de Startups Tecnológicas & Seed/Series A**:
   Excelente para sites comerciais que precisam de autoridade visual imediata e diferenciação diante de investidores e early-adopters, alavancando componentes protagonistas como *Dia Text Reveal*, *Hover Feature Cards*, *Stacked Feature Cards* e *Gravity Stars*.
4. **Portfólios de Engenharia de Design (Design Engineers & Creative Techs)**:
   Vitrine ideal para mostrar domínio de interações finas, tipografia editorial mista (serifa contrastada com Geist Sans monoespaçada) e transições sem engasgos de taxa de quadros (60 a 120 FPS).

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Neutra e Estrutural)**:
  Superfícies estáticas em modo escuro profundo (`bg-background` em Stone/Zinc 950 ou Slate 950), tipografia utilitária legível (`Geist Sans` ou `Inter`), bordas discretas (`border-border/50`) e grids alinhados rigorosamente à escala de 8px/4px.
- **30% (Camada Tátil & Micro-Interações do Unlumen UI)**:
  Aqui o Unlumen UI opera como padrão ouro: *Motion Navigation Menu* com pílula de transição contínua, *Apple Switch* em telas de configuração ou toggle de pricing (Mensal/Anual), *Progressive Blur* fixo nas bordas da viewport, *Favicon Search* em inputs de onboarding e *Motion FAQs Accordion* em seções de suporte.
- **10% (Showstoppers Protagonistas)**:
  Limite a 1 (no máximo 2) efeitos de alto impacto por página: use o *Dia Text Reveal* exclusivamente no headline do Hero; utilize o shader *Gravity Stars* ou *Pixel Liquid Bg* no fundo do Hero ou no CTA final de encerramento; ou posicione o *Orbital Image Wheel* no bloco central de social proof ou showcase de ecossistema.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Interfaces Transacionais Hiper-Densas de Alta Frequência (Fintech Trading / Bloomberg-like)**:
  Terminais onde milissegundos contam e centenas de dados atualizam por segundo em tabelas com milhares de nós no DOM não toleram o overhead de transforms 3D ou cálculos de molas por evento de ponteiro.
- **Aplicações com Público de Hardware Legado ou Conexões 2G/3G Restritas**:
  Módulos com shaders WebGL (`Pixel Liquid Bg`, `Gravity Stars`) e múltiplos `backdrop-filter` empilhados exigem aceleração de hardware GPU dedicada; em dispositivos móveis antigos ou navegadores com baixa performance gráfica, podem ocasionar perda drástica de frames.
- **Sites Estritamente Corporativos Tradicionais (Bancos Tradicionais, Portais Jurídicos/Governamentais)**:
  A atmosfera dark craft do Unlumen UI combinada com micro-interações de mola pode parecer excessivamente lúdica ou "hype de startup" em ambientes onde a sobriedade estática burocrática é mandatória.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **Sobrecarga de Shaders no Mesmo Viewport**: Combinar *Gravity Stars* no background com *Pixel Liquid Bg* em um card e *Blob Card* na mesma tela; isso degrada o framerate e resulta no clássico efeito amador de "portfolio showoff" sem foco no produto.
- **Abuso de Text Reveals em Parágrafos Inteiros**: Aplicar *Dia Text Reveal* ou *Vercel Snap Text* em blocos de texto corrido ou FAQs; animações de caracteres devem se limitar a títulos curtos de 2 a 5 palavras. O usuário quer ler, não esperar letras revelarem.
- **Ignorar `prefers-reduced-motion`**: Renderizar componentes táteis com molas de alta oscilação sem prover o fallback para usuários com sensibilidade vestibular.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

### 1. Apple Switch
- **Anatomia Visual**: Toggle hiper-realista com acabamento físico Apple/macOS. Apresenta corpo cilíndrico com chanfro luminoso interno (`border-white/35`, `bg-white/10`, `backdrop-blur-md`), brilho suave difuso (*glow*) ativado dinamicamente na cor de status (esmeralda `#34c759` ou monocromático) e thumb com sombra profunda 3D e reflexo especular na borda superior. Durante o arraste, o thumb se estica fluidamente (*squash and stretch*).
- **Gatilho de Interação**: Click, PointerDown com arrasto livre horizontal (`PointerCapture`), suporte a cancelamento de clique e mola tátil (`stiffness: 700, damping: 48, mass: 0.55`).
- **Onde Encaixar**: Settings / Painéis de Configuração, Modais de Notificação, Billing Toggle (Mensal / Anual) na seção de Preços.

### 2. Progressive Blur (Gradual Blur Page)
- **Anatomia Visual**: Sistema de desfoque progressivo em camadas sobrepostas transparentes que substitui barras de cabeçalho e rodapé rígidas. Utiliza máscaras CSS lineares (`linear-gradient`) combinadas com valores incrementais de `backdrop-filter: blur(...)` e tint suave via `color-mix`.
- **Gatilho de Interação**: Estático / Fixado na janela (`fixed top-0` ou `fixed bottom-0`), respondendo ao scroll da página de forma 100% fluida via aceleração GPU.
- **Onde Encaixar**: Cabeçalho de navegação (Navbar), Barra inferior de status (Footer), gavetas laterais de leitura ou topo de listas com scroll infinito.

### 3. Favicon Search
- **Anatomia Visual**: Input de pesquisa moderno que inspeciona em tempo real a URL digitada pelo usuário, extrai o domínio limpo, faz pré-carregamento do favicon através da API Google S2 e troca o ícone padrão de lupa pelo favicon do domínio com transição de escala, mola e blur. Inclui botão de limpar instantâneo com animação `AnimatePresence`.
- **Gatilho de Interação**: Digitação (`onChange` com debounce de 350ms), tecla Enter (`onSearch`) e hover/focus do cursor.
- **Onde Encaixar**: Hero de ferramentas DevTools/SEO, formulários de onboarding de projetos/domínios, módulos de favoritos e integrações de terceiros.

### 4. Tilt Card
- **Anatomia Visual**: Cartão tridimensional interativo que reage à posição relativa do cursor dentro de sua área. Conforme o ponteiro se move, o cartão calcula ângulos `rotateX` e `rotateY` via perspectiva CSS (`perspective(1000px)`), enquanto uma imagem flutuante interna se desacopla em profundidade angular (`rotate-[-5deg]` para `group-hover:-rotate-3`), acompanhada de um feixe de luz difusa circular (`ClippedCircle`).
- **Gatilho de Interação**: `onMouseMove` contínuo mapeado para valores de mola normalizados `[-0.5, 0.5]` e `onMouseLeave` que retorna suavemente à posição de repouso.
- **Onde Encaixar**: Bento Grid de Funcionalidades, Cartão de Plano de Preços Principal (Plano Pro/Enterprise), Showcase de Projetos em Destaque.

### 5. Motion Navigation Menu & Motion Tabs Menu
- **Anatomia Visual**: Sistema de navegação de alta fidelidade com barra de abas e menus dropdown flutuantes. Apresenta uma pílula de fundo deslizante compartilhada (`HighlightItem`) que acompanha suavemente o item focado ou sob hover, e janelas de conteúdo que realizam transições direcionais cinéticas (deslizam da direita para a esquerda ou vice-versa com base na posição da aba anterior).
- **Gatilho de Interação**: Hover (com tolerância de saída) e clique para fixação, com atualização automática dos limites via `getBoundingClientRect`.
- **Onde Encaixar**: Navbar global do produto, abas internas de dashboards analíticos, alternadores de categoria de documentação técnica.

### 6. Dia Text Reveal (Showstopper - Pro)
- **Anatomia Visual**: Tipografia cinética de elite para títulos de grande formato. Cada caractere ou palavra é encapsulado em nós de renderização independentes que sofrem revelação escalonada (*staggered reveal*) combinando opacidade zero, desfoque gaussiano inicial de `blur(4px)` a `blur(0px)` e translação vertical com easing quintic suave.
- **Gatilho de Interação**: InView (quando a viewport atinge a seção) ou no carregamento inicial da página.
- **Onde Encaixar**: H1 do Hero, Frase de impacto de transição de seções no meio da landing page.

### 7. Hover Feature Cards & Stacked Feature Cards
- **Anatomia Visual**: Conjunto de cards em bento grid onde o elemento gráfico (preview em imagem ou mockup de software) possui proporção geométrica consistente (`aspect-[4/3]`) sobre fundo sutilmente iluminado. No modelo *Stacked*, múltiplos cards repousam empilhados e se abrem em leque tridimensional ao hover ou ao scroll da página.
- **Gatilho de Interação**: Hover de mouse com transição de opacidade da imagem e elevação do container (`hover:scale-[1.02]`).
- **Onde Encaixar**: Seção principal de Features (Bento Grid) da landing page, tours de produto em SaaS.

### 8. Gravity Stars & Pixel Liquid Bg (Shaders)
- **Anatomia Visual**: Canvas interativo em WebGL/2D que projeta campos estelares responsivos a vetores gravitacionais ou distorções de malha líquida com granulação pixelada refinada. Cria uma profundidade espacial imersiva mantendo a estética minimalista dark.
- **Gatilho de Interação**: Posição e velocidade do cursor (`mousemove`), com desaceleração inercial e loop em background via `requestAnimationFrame`.
- **Onde Encaixar**: Hero Section de produtos de IA, infraestrutura de nuvem, criptografia ou CTA final de conversão.

### 9. Notion Floating Action Menu & Notion Mention Link
- **Anatomia Visual**: Menus de contexto ultra-compactos e links de citação visual idênticos ao ecossistema Notion. Ao passar o mouse sobre o mention link, um mini card com thumbnail, metadados do documento e status se expande instantaneamente com escala elástica e sombra suave.
- **Gatilho de Interação**: Hover com delay calculado de 150ms para evitar disparos acidentais; saída fluida com fade out.
- **Onde Encaixar**: Editores rich-text modernos, documentações técnicas interativas, bases de conhecimento e listas de referências.

### 10. Vercel Snap Text & Animate Digits
- **Anatomia Visual**: Contadores numéricos e transições textuais onde cada dígito é disposto em um tambor vertical invisível (`tabular-nums`). Quando o valor é alterado, o dígito antigo rola com desfoque de movimento enquanto o novo dígito encaixa perfeitamente no lugar, evitando que a largura do texto balance o layout ao redor.
- **Gatilho de Interação**: Mudança de estado numérico (ex: estatísticas ao vivo, alternância de preços mensais para anuais, contadores de tração).
- **Onde Encaixar**: Métricas de tração (ex: *"10M+ requisições"*), Tabela de preços, Dashboards financeiros e contadores analíticos em tempo real.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Registro

O Unlumen UI utiliza a distribuição por CLI oficial do **shadcn**. A arquitetura separa componentes entre o registro gratuito e componentes Pro licenciados pela plataforma Polar.

#### Configuração do `components.json`:
```json
{
  "$schema": "https://ui.shadcn.com/schema.json",
  "style": "default",
  "rsc": true,
  "tsx": true,
  "tailwind": {
    "config": "tailwind.config.ts",
    "css": "app/globals.css",
    "baseColor": "zinc",
    "cssVariables": true
  },
  "aliases": {
    "components": "@/components",
    "utils": "@/lib/utils"
  },
  "registries": {
    "@unlumen-ui": {
      "url": "https://ui.unlumen.com/r/{name}.json",
      "headers": {
        "Authorization": "Bearer ${UNLUMEN_LICENSE_KEY}"
      }
    }
  }
}
```

#### Instalação de Dependências Essenciais:
```bash
npm install motion clsx tailwind-merge lucide-react class-variance-authority
# ou via pnpm
pnpm add motion clsx tailwind-merge lucide-react class-variance-authority
```

#### Adicionando Componentes via CLI:
```bash
# Adicionar componente gratuito
npx shadcn@latest add "https://ui.unlumen.com/r/apple-switch.json"
npx shadcn@latest add "https://ui.unlumen.com/r/progressive-blur.json"
npx shadcn@latest add "https://ui.unlumen.com/r/favicon-search.json"
npx shadcn@latest add "https://ui.unlumen.com/r/tilt-card.json"
```

---

### Física de Movimento, Molas & Curvas de Easing

O Unlumen UI padronizou os seguintes perfis físicos em seu ecossistema Motion:

| Perfil de Movimento | Parâmetros Físicos | Caso de Uso Primário | Sensação Tátil |
| :--- | :--- | :--- | :--- |
| **Snappy Switch Spring** | `stiffness: 700`, `damping: 48`, `mass: 0.55` | `AppleSwitch` thumb travel | Resposta instantânea, clique sólido sem eco |
| **Grab / Pointer Spring** | `stiffness: 500`, `damping: 25` | Arraste de ponteiro e deformação de thumb | Plasticidade imediata sob o dedo do usuário |
| **Micro-Icon Spring** | `stiffness: 400`, `damping: 28` | `FaviconSearch` reveal, `Highlight` pills | Fluidez elegante sem atraso perceptível |
| **3D Tilt Spring** | `stiffness: 300`, `damping: 20` | `TiltCard`, perspectiva de imagens | Amortecimento inercial fotorrealista |
| **Cubic-Bezier Quintic** | `cubic-bezier(0.22, 1, 0.36, 1)` | Expansão de largura, fading de abas e menus | Curva Vercel/Apple clássica de desaceleração |

---

### Receitas de Código Estruturais e Prontas para Produção

Abaixo estão duas implementações fiéis à arquitetura do Unlumen UI, documentadas e prontas para uso:

#### 1. `ProgressiveBlur.tsx` (Primitiva de Desfoque Gradual)
```tsx
"use client";

import * as React from "react";
import { cn } from "@/lib/utils";

export type ProgressiveBlurSide = "top" | "bottom" | "left" | "right";

export interface ProgressiveBlurProps extends React.HTMLAttributes<HTMLDivElement> {
  /** Borda de maior intensidade do desfoque. @default "top" */
  side?: ProgressiveBlurSide;
  /** Intensidade do desfoque em pixels. @default 8 */
  strength?: number;
  /** Altura ou largura da área de transição. @default "96px" */
  size?: string | number;
  /** Habilita gradiente de fundo com color-mix. @default true */
  tint?: boolean;
  /** Opacidade da cor de fundo na borda sólida (0 a 1). @default 0.95 */
  tintStrength?: number;
  className?: string;
}

const IS_HORIZONTAL: Record<ProgressiveBlurSide, boolean> = {
  top: false,
  bottom: false,
  left: true,
  right: true,
};

const FADE_DIR: Record<ProgressiveBlurSide, string> = {
  top: "to bottom",
  bottom: "to top",
  left: "to right",
  right: "to left",
};

const POSITION_STYLE: Record<ProgressiveBlurSide, React.CSSProperties> = {
  top: { top: 0, left: 0, right: 0 },
  bottom: { bottom: 0, left: 0, right: 0 },
  left: { top: 0, bottom: 0, left: 0 },
  right: { top: 0, bottom: 0, right: 0 },
};

export const ProgressiveBlur = React.memo(function ProgressiveBlur({
  side = "top",
  strength = 8,
  size = "96px",
  tint = true,
  tintStrength = 0.95,
  className,
  style,
  ...props
}: ProgressiveBlurProps) {
  const isHorizontal = IS_HORIZONTAL[side];
  const fadeDir = FADE_DIR[side];
  const sizeValue = typeof size === "number" ? `${size}px` : size;

  const sizeStyle: React.CSSProperties = isHorizontal
    ? { width: sizeValue, height: "100%" }
    : { height: sizeValue, width: "100%" };

  // Máscara linear que vai da opacidade plena para transparente
  const maskImage = `linear-gradient(${fadeDir}, black 20%, transparent 100%)`;

  const background = tint
    ? `linear-gradient(${fadeDir}, color-mix(in srgb, var(--background) ${Math.round(
        tintStrength * 100
      )}%, transparent) 0%, transparent 100%)`
    : undefined;

  return (
    <div
      aria-hidden="true"
      className={cn("pointer-events-none fixed z-40 select-none", className)}
      style={{
        ...sizeStyle,
        ...POSITION_STYLE[side],
        background,
        maskImage,
        WebkitMaskImage: maskImage,
        backdropFilter: `blur(${strength}px)`,
        WebkitBackdropFilter: `blur(${strength}px)`,
        willChange: "backdrop-filter",
        ...style,
      }}
      {...props}
    />
  );
});
```

#### 2. `AppleSwitch.tsx` (Toggle Háptico de Mola com Pointer Capture)
```tsx
"use client";

import * as React from "react";
import { motion, useMotionValue, useSpring, useTransform } from "motion/react";
import { cn } from "@/lib/utils";

const switchSizes = {
  sm: { trackX: 46, trackY: 24, thumbX: 20, thumbY: 18, padding: 3 },
  md: { trackX: 58, trackY: 30, thumbX: 28, thumbY: 24, padding: 3 },
  lg: { trackX: 72, trackY: 36, thumbX: 34, thumbY: 28, padding: 4 },
} as const;

const thumbSpring = { stiffness: 700, damping: 48, mass: 0.55 };
const grabSpring = { stiffness: 500, damping: 25 };

export interface AppleSwitchProps
  extends Omit<React.ButtonHTMLAttributes<HTMLButtonElement>, "onChange" | "role"> {
  checked?: boolean;
  defaultChecked?: boolean;
  onCheckedChange?: (checked: boolean) => void;
  label?: React.ReactNode;
  size?: keyof typeof switchSizes;
}

export const AppleSwitch = React.forwardRef<HTMLButtonElement, AppleSwitchProps>(
  (
    {
      checked: controlledChecked,
      defaultChecked = false,
      onCheckedChange,
      label,
      size = "md",
      className,
      disabled,
      ...props
    },
    ref
  ) => {
    const isControlled = controlledChecked !== undefined;
    const [uncontrolledChecked, setUncontrolledChecked] = React.useState(defaultChecked);
    const isChecked = isControlled ? controlledChecked : uncontrolledChecked;

    const metrics = switchSizes[size];
    const thumbTravel = metrics.trackX - metrics.thumbX - metrics.padding * 2;

    const targetX = useMotionValue(isChecked ? thumbTravel : 0);
    const thumbX = useSpring(targetX, thumbSpring);

    const grabTarget = useMotionValue(0);
    const grabSpringValue = useSpring(grabTarget, grabSpring);

    // Efeito de esticamento do thumb durante interação
    const thumbWidth = useTransform(grabSpringValue, [0, 1], [metrics.thumbX, metrics.thumbX + 6]);

    React.useEffect(() => {
      targetX.set(isChecked ? thumbTravel : 0);
    }, [isChecked, thumbTravel, targetX]);

    const toggle = () => {
      if (disabled) return;
      const next = !isChecked;
      if (!isControlled) setUncontrolledChecked(next);
      onCheckedChange?.(next);
    };

    return (
      <label className={cn("inline-flex items-center gap-3 select-none cursor-pointer", disabled && "opacity-50 cursor-not-allowed")}>
        <button
          ref={ref}
          type="button"
          role="switch"
          aria-checked={isChecked}
          disabled={disabled}
          onClick={toggle}
          className={cn(
            "relative inline-flex items-center rounded-full transition-colors duration-300 outline-none",
            "border border-white/20 focus-visible:ring-2 focus-visible:ring-emerald-500/50",
            isChecked ? "bg-emerald-500" : "bg-neutral-800",
            className
          )}
          style={{ width: metrics.trackX, height: metrics.trackY }}
          {...props}
        >
          {/* Sombra interna e luz de fundo */}
          <span className="absolute inset-0 rounded-full shadow-inner pointer-events-none" />

          {/* Thumb deslizante com física tátil */}
          <motion.span
            className="absolute block rounded-full bg-white shadow-md pointer-events-none"
            style={{
              x: thumbX,
              left: metrics.padding,
              width: thumbWidth,
              height: metrics.thumbY,
            }}
          />
        </button>
        {label && <span className="text-sm font-medium text-foreground">{label}</span>}
      </label>
    );
  }
);
AppleSwitch.displayName = "AppleSwitch";
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao arquitetar uma nova aplicação ou landing page e eleger o **Unlumen UI** como biblioteca-chave no documento `DESIGN_BLUEPRINT.md`, configure as diretrizes abaixo:

1. **Declaração do Registro de Componentes**:
   - Defina explicitamente no blueprint a adição do registro do Unlumen UI em `components.json`:
     `registries: { "@unlumen-ui": "https://ui.unlumen.com/r" }`.
   - Caso sejam utilizados componentes Pro (`Dia Text Reveal`, `Stacked Feature Cards`, `Social Hover Cards`), declare a dependência da variável de ambiente `UNLUMEN_LICENSE_KEY`.

2. **Arquitetura de Navegação & Viewport**:
   - Substitua o padrão de `header fixed border-b backdrop-blur-md` genérico pela dupla:
     `MotionNavigationMenu` (ou `Floating Navbar` com `@unlumen-ui/highlight`) montado sobre a primitiva `ProgressiveBlur` posicionada em `side="top"`.
   - Adicione `ProgressiveBlur` em `side="bottom"` para páginas com conteúdo de rolagem longa ou leituras de artigos.

3. **Governança de Tipografia & Modos de Cor**:
   - Adote `font-serif` elegante (ex: `Instrument Serif`, `Playfair Display` ou `Newsreader`) para títulos display (`H1`, `H2`), gerando o contraste editorial característico do Unlumen UI com o corpo de texto em `Geist Sans` ou `Inter`.
   - Garanta paleta escura com base em tons de zinco neutro (`bg-[#09090b]`, `surface-[#121215]`), reservando o acento esmeralda (`#34c759` / `emerald-400`) para status online, pills de sucesso e badges de preços.

4. **Regra de Blindagem contra Sobrecarga**:
   - Proíba explicitamente no blueprint o uso de mais de 1 componente baseado em Canvas/Shader WebGL (`Gravity Stars`, `Pixel Liquid Bg`) na mesma página.
   - Restrinja o componente `AppleSwitch` para áreas focais de decisão (tabela de preços ou modal de configurações), mantendo switches simples do Shadcn UI em formulários extensos.
