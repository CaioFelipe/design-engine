---
id: "magic-ui"
name: "Magic UI"
url: "https://magicui.design/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["SaaS Landing Page Craft", "Luminous Edge Tracing & Glows", "Asymmetric Bento Architecture", "Motion-Driven Conversion Hooks", "Dynamic SVG Pathflows"]
densidade_informacao: "Media"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Framer Motion/CSS) a Alto (Canvas/WebGL cobe)"
stack_frameworks: ["React 19 / 18", "Next.js 15 (App Router)", "Tailwind CSS (v3.4 & v4)", "Motion (Framer Motion)", "Lucide React", "Radix UI", "cobe (WebGL)"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "Plus Jakarta Sans", "Cabinet Grotesk", "Satoshi", "Geist Mono"]
  paletas_ideais: ["Deep Neutral Zinc/Slate (Zinc 950 / Slate 950)", "High-Contrast Monochrome com Acentos Violet/Indigo/Cyan", "Subtle Dark Glass com Bordas Luminescentes"]
  combinacoes_recomendadas: ["Shadcn UI", "Cult UI", "21st.dev", "Aceternity UI", "Vaul"]
  conflitos_esteticos: ["Neumorfismo pastel desbotado", "Brutalismo cru sem suavização de curvas", "Material Design 2 com sombras duras primárias"]
---

# Magic UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo engenheiro de software e empreendedor **Dillion Verma**, o **Magic UI** (`magicui.design`) estabeleceu-se como a biblioteca de design de componentes de maior impacto para o ecossistema de landing pages e sites de marketing de SaaS modernos. Projetado deliberadamente como o "irmão de marketing" do `shadcn/ui`, o Magic UI preenche a lacuna crítica existente entre sistemas de design utilitários operacionais (focados em formulários, modais, tabelas e botões corporativos) e as necessidades cênicas de altíssima conversão de produtos tecnológicos modernos.

A assinatura estética do Magic UI é caracterizada pela transposição dos padrões visuais mais cobiçados de gigantes como Apple, Linear, Raycast, Vercel e Stripe em primitivas modulares prontas para produção. Essa assinatura repousa sobre quatro pilares visuais e de engenharia:

1. **Iluminação Direcional Perimetral e Feixes Laser (Edge Tracing & Luminous Conduction)**:
   Em vez de bordas estáticas monótonas (`border-neutral-800`), o Magic UI introduziu uma obsessão por feixes luminosos itinerantes (*Border Beam*, *Shine Border*, *Neon Gradient Card*). Através de gradientes angulares cônicos (`conic-gradient`) e manipulações de máscaras SVG/CSS, feixes de luz concentrados percorrem o contorno de cartões e botões a velocidades calculadas, simulando condutividade elétrica ou lasers que atraem o olhar do visitante para o elemento central de conversão.

2. **Fluxos de Conectividade Vetorial Dinâmica (SVG Dynamic Pathing & Beams)**:
   Um dos desafios mais recorrentes em landing pages de SaaS de IA e infraestrutura é representar como dados, prompts ou integrações viajam entre serviços heterogêneos. O Magic UI resolveu esse problema de engenharia com o *Animated Beam*: um componente que rastreia programaticamente as coordenadas de elementos DOM arbitrários via referências React e renderiza curvas Bézier suaves em SVG com gradientes lineares em movimento perpétuo, transformando integrações abstratas em uma metáfora visual tangível.

3. **Arquitetura Assimétrica Bento com Profundidade em Camadas (Bento Grid)**:
   Inspirado pela apresentação de hardware da Apple e interfaces contemporâneas, o padrão de *Bento Grid* do Magic UI combina células de tamanhos variados (`col-span-1`, `col-span-2`, `col-span-3`) com fundos texturizados dinâmicos (efeitos de partículas, grades de perspectiva retro, gráficos simulados e botões de chamada de ação que deslizam no hover). Cada célula funciona como um micro-ecossistema visual que comunica uma funcionalidade de software de forma independente, mas harmônica.

4. **Cinética Contínua e Revelação Óptica (Continuous Loops & Blur Transitions)**:
   A sensação de dinamismo da interface é mantida por animações em loop infinito suaves como seda — como o *Marquee* infinito com desfoque de borda suave (*fade masks* laterais), *Meteors* que cortam o plano de fundo em ângulos diagonais precisos de 215°, e o *Blur Fade*, que substitui transições bruscas de entrada por uma interpolação simultânea de deslocamento espacial e remoção progressiva de desfoque gaussiano (`filter: blur(6px)` para `blur(0px)`).

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **Landing Pages de Startups de IA, LLMs e Agentes Autônomos**:
   Plataformas que precisam comunicar pipelines complexos (ex: entrada de dados → vetorização → inferência de modelo → entrega em múltiplos canais). O *Animated Beam*, o *Hyper Text* (simulando decodificação de tokens) e o *Bento Grid* são os componentes ideais para este propósito.
2. **Produtos SaaS B2B e Plataformas de DevTools**:
   Empresas com múltiplos parceiros e integrações (GitHub, Slack, AWS, Linear, Notion, Discord). O *Marquee* exibe logotipos de clientes e parceiros sem interromper a leitura, enquanto o *Border Beam* destaca o cartão de assinatura "Pro / Enterprise" nas tabelas de preços.
3. **Páginas de Lançamento de Produto, Waitlist e Financiamento**:
   Interfaces de alta urgência onde cada milissegundo de atenção conta. O uso de *Safari Mockup* ou *iPhone 15 Pro Mockup* enquadra o software em molduras de hardware de luxo, acompanhado por *Number Ticker* para demonstrar volume de usuários inscritos em tempo real.
4. **Infraestrutura Global e Plataformas de Rede Edge**:
   Projetos de computação distribuída, bancos de dados globais ou CDNs que precisam demonstrar presença planetária. O componente *Globe 3D* (baseado na biblioteca ultraleve WebGL `cobe`) cria autoridade visual instantânea.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Estrutural e Tipografia)**:
  Superfícies limpas, neutras e altamente legíveis construídas com componentes base do `shadcn/ui` (botões neutros, tipografia com `Geist Sans` ou `Inter`, tabelas, acordeões de FAQ e grades com espaçamento generoso `gap-4` a `gap-8`).
- **30% (Camada de Estruturação Dinâmica do Magic UI)**:
  Componentes de estruturação cênica: o container de *Bento Grid* organizando os recursos do produto, o carrossel infinito *Marquee* exibindo validação social e avaliações de clientes, e o *Blur Fade* gerenciando a orquestração de entrada de cada seção conforme o usuário rola a página.
- **10% (Showstoppers Protagonistas de Alta Energia)**:
  Pontos de clímax visual cuidadosamente posicionados: um feixe *Animated Beam* conectando ícones na seção de integrações, um *Border Beam* cintilando ao redor do card de plano mais vendido no Pricing, ou o *Shimmer Button* no botão de ação principal do Hero. **Regra de ouro**: nunca colocar dois efeitos luminosos contínuos disputando o mesmo campo de visão imediato.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Painéis Internos de Gestão de Dados e ERPs (Dashboards Analíticos)**:
  Grades de auditoria financeira, telas de emissão de notas fiscais ou interfaces operacionais densas. A inclusão de efeitos como feixes de luz itinerantes (*Border Beam*), partículas flutuantes ou textos com embaralhamento dinâmico (*Hyper Text*) desvia a atenção da tarefa analítica e gera sobrecarga cognitiva severa.
- **Aplicações Críticas com Hardware Restrito ou Baixa Largura de Banda**:
  Dispositivos industriais, PDVs móveis ou smartphones de entrada em redes 3G/4G instáveis. Componentes baseados em canvas contínuo (como *Globe 3D* com WebGL ou *Particles* com centenas de vetores reagindo ao ponteiro do mouse) consomem ciclos de GPU e drenam bateria excessivamente.
- **Portais Governamentais e Ambientes de Acessibilidade Estrita (WCAG AAA)**:
  Interfaces onde animações contínuas sem mecanismo de pausa imediata infringem diretrizes de acessibilidade para usuários com distúrbios vestibulares ou TDAH.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **"Neon Overload" (Efeito Cassino)**: Colocar simultaneamente um *Border Beam* cintilando no navbar, um *Retro Grid* no fundo, *Meteors* caindo na lateral e um *Shimmer Button* pulsando no centro. O design deixa de parecer sofisticado e passa a transmitir amadorismo e ruído ("AI template slop").
- **Marquee Acelerado e sem Pausa**: Configurar a velocidade da esteira rolante (*Marquee*) em menos de 20 segundos para textos ou depoimentos, forçando os olhos do leitor a perseguirem as palavras. Todo marquee deve incluir a propriedade `pauseOnHover={true}` e velocidade moderada (`--duration: 40s`).
- **Negligência do Suporte a Movimento Reduzido (`prefers-reduced-motion`)**:
  Falhar em congelar as animações contínuas de SVG beams, bordas giratórias e rotações de palavras quando o sistema operacional do usuário sinaliza preferência por redução de movimento.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 12 componentes mais emblemáticos da biblioteca Magic UI:

### 1. Animated Beam (`@magicui/animated-beam`)
- **Anatomia Visual**: Gera um feixe vetorial bidirecional ou unidirecional que corre ao longo de uma curva Bézier suave desenhada entre dois nós HTML arbitrários. O feixe é composto por um caminho base sutil (`stroke-neutral-800`) e um feixe luminoso animado que transita através de gradientes em movimento (`linearGradient` com offsets animados).
- **Gatilho de Interação**: Animação contínua em loop autônomo (*auto-play*); suporta reversão de sentido (`reverse={true}`), curvatura paramétrica ajustável (`curvature`) e atraso inicial escalonado.
- **Onde encaixar**: Seção de "Integrações", "Como Funciona" ou "Arquitetura do Sistema", conectando ícones de ferramentas externas (Slack, Discord, GitHub, Notion) a um nó central do produto.

### 2. Border Beam (`@magicui/border-beam`)
- **Anatomia Visual**: Uma linha luminosa concentrada que viaja perpetuamente pelo contorno externo de um contêiner retangular com bordas arredondadas. Utiliza propriedades de gradiente cônico ou caminhos com coordenadas normalizadas, gerando a ilusão de um traçado laser de alta precisão.
- **Gatilho de Interação**: Loop contínuo infinito com tempo de ciclo configurável (`duration`, ex: 12s); acelera ou intensifica no hover quando desejado.
- **Onde encaixar**: No contêiner de pré-visualização de vídeo/produto do Hero, no cartão de assinatura mais popular (Tier Pro/Enterprise) na tabela de Pricing, ou no modal de checkout final.

### 3. Bento Grid & Bento Card (`@magicui/bento-grid`)
- **Anatomia Visual**: Grade assimétrica modular composta por contêineres de alta densidade estética (`BentoGrid` e `BentoCard`). Cada cartão incorpora uma área de background visual imersivo (efeito de código, gráfico, simulação interativa), ícone com acabamento tátil, título, descrição concisa e um botão de ação com ícone de seta que desliza elegantemente para dentro da visualização ao passar o mouse.
- **Gatilho de Interação**: Hover do mouse, disparando transições de escala sutil no background, fade-in da ação primária e aumento de contraste de borda.
- **Onde encaixar**: Seção principal de "Features" ou "Capacidades da Plataforma", imediatamente após o bloco de validação social do Hero.

### 4. Marquee (`@magicui/marquee`)
- **Anatomia Visual**: Esteira rolante infinita de elementos (logotipos, depoimentos, tweets, crachás) que desliza horizontalmente ou verticalmente sem engasgos de frame. É tradicionalmente envolvida por uma máscara de gradiente CSS lateral (`[mask-image:linear-gradient(...)]`) que faz os elementos surgirem e desaparecerem em névoa suave nas extremidades.
- **Gatilho de Interação**: Movimento contínuo linear via CSS; pausa suavemente ao passar o cursor (`pauseOnHover={true}`).
- **Onde encaixar**: Faixa de clientes e parceiros (Social Proof) logo abaixo do Hero, e mural de depoimentos de clientes em várias colunas com direções opostas.

### 5. Orbiting Circles (`@magicui/orbiting-circles`)
- **Anatomia Visual**: Círculos orbitais concêntricos concêntricos desenhados com traços tênues pontilhados ou semitransparentes, sobre os quais múltiplos ícones ou avatares orbitam em torno de um núcleo central. A física matemática cancela a rotação no elemento filho, mantendo os ícones perfeitamente verticais durante toda a revolução circular.
- **Gatilho de Interação**: Rotação orbital perpétua baseada em tempo (`duration`), com raios variáveis (`radius: 80`, `190`, `300`) e suporte a reversão de sentido de órbita.
- **Onde encaixar**: Ilustração gráfica principal do Hero ou da seção de ecossistema, demonstrando plugins ou inteligências orbitando a plataforma central.

### 6. Shimmer Button (`@magicui/shimmer-button`)
- **Anatomia Visual**: Botão de alta fidelidade visual com contorno arredondado, fundo escuro profundo e um reflexo cintilante (*shimmer*) que circula em alta velocidade ao redor do perímetro interno, criando um brilho dinâmico contínuo sob a camada de texto.
- **Gatilho de Interação**: Rotação autônoma do gradiente; elevação de escala e brilho ao receber hover ou foco por teclado.
- **Onde encaixar**: O botão de Ação Primária (CTA) mais importante da página inteira (ex: "Começar Gratuitamente", "Solicitar Acesso Antecipado" no Hero e no rodapé final).

### 7. Blur Fade (`@magicui/blur-fade`)
- **Anatomia Visual**: Primitiva de animação de entrada que orquestra a aparição de elementos através da interpolação harmônica de três parâmetros: opacidade (`opacity: 0` → `1`), translação no eixo Y (`y: 6px` → `0px`) e remoção progressiva de desfoque (`filter: blur(6px)` → `blur(0px)`).
- **Gatilho de Interação**: Disparado pela rolagem do usuário ao cruzar o limiar de visibilidade na viewport (`useInView`), com suporte a atrasos em cascata calculados (`delay = 0.05 * index`).
- **Onde encaixar**: Como envelope de orquestração para todos os títulos de seção, grades de cartões, listas de preços e blocos de depoimentos da página.

### 8. Globe 3D (`@magicui/globe`)
- **Anatomia Visual**: Esfera tridimensional fotorrealista renderizada através de WebGL ultraleve (alimentada pelo motor `cobe`), mapeando pontos geográficos brilhantes, arcos de conexão entre cidades e rotação suave do globo terrestre com baixa pegada de memória.
- **Gatilho de Interação**: Rotação automática suave por inércia matemática; permite arrasto com o mouse para inspecionar regiões específicas do planeta.
- **Onde encaixar**: Cartão central de infraestrutura dentro de um Bento Grid, ou em seções que destacam distribuição de servidores globais, latência zero e conformidade regional.

### 9. Number Ticker (`@magicui/number-ticker`)
- **Anatomia Visual**: Contador numérico fluido que roda valores decimais ou inteiros de zero até a meta estipulada, utilizando física de mola amortecida que desacelera com precisão mecânica ao se aproximar do número final.
- **Gatilho de Interação**: Disparado no instante em que o container entra no campo de visão do navegador (`viewport in-view`).
- **Onde encaixar**: Seções de métricas de impacto no Hero ou no meio da página (ex: "10M+ requisições diárias", "99.99% de uptime", "45.000 desenvolvedores").

### 10. Dock (`@magicui/dock`)
- **Anatomia Visual**: Barra de navegação flutuante inspirada no Dock do macOS, com acabamento em vidro fosco (*frosted glass*), bordas com micro-reflexo e ícones que aumentam de escala proporcionalmente à proximidade do cursor do mouse, calculando uma curva de dispersão gaussiana de tamanho.
- **Gatilho de Interação**: Movimento do ponteiro do mouse (`onMouseMove`), calculando a distância euclidiana para cada item do dock via `useMotionValue` e transformações em mola.
- **Onde encaixar**: Barra de ferramentas de navegação flutuante inferior, alternador de visualizações em demos interativas de produto ou rodapé de portfólio.

### 11. Safari Mockup & iPhone 15 Pro Mockup (`@magicui/safari`, `@magicui/iphone-15-pro`)
- **Anatomia Visual**: Molduras de hardware fotorrealistas desenhadas inteiramente em SVG e classes utilitárias de Tailwind CSS. O Safari Mockup reproduz a barra de navegação moderna com botões de controle de janela (vermelho, amarelo, verde) e barra de URL; o iPhone 15 Pro Mockup reproduz a Dynamic Island, o botão de ação e o acabamento de borda em titânio escovado.
- **Gatilho de Interação**: Contêineres responsivos prontos para receber imagens, vídeos em autoplay ou iframes interativos; respondem com efeitos de inclinação tridimensional (*3D tilt*) quando combinados com listeners de ponteiro.
- **Onde encaixar**: O mockup central de demonstração do software no topo da Hero Section, comprovando imediatamente a existência e o polimento do produto.

### 12. Hyper Text & Word Rotate (`@magicui/hyper-text`, `@magicui/word-rotate`)
- **Anatomia Visual**: Componentes tipográficos de alta atratividade. O *Hyper Text* embaralha caracteres aleatórios rapidamente antes de fixar o texto real (efeito de descriptografia cyberpunk/terminal); o *Word Rotate* realiza um carrossel vertical deslizante com fade para alternar adjetivos ou verbos centrais dentro de um título.
- **Gatilho de Interação**: Disparado no carregamento da página ou ao passar o mouse sobre a palavra; o Word Rotate opera em intervalo periódico fixo (ex: a cada 2500ms).
- **Onde encaixar**: No subtítulo ou na palavra-chave de destaque do título H1 do Hero (ex: "Construa interfaces [ Rápidas | Inteligentes | Lindas ]").

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Ecossistema

O Magic UI adota o mesmo paradigma arquitetural do `shadcn/ui`: o código-fonte dos componentes pertence ao seu repositório local, evitando pacotes NPM engessados e permitindo customização profunda de estilos.

Para instalar qualquer componente do Magic UI em um projeto configurado com `shadcn/ui` e Tailwind CSS:

```bash
# Instalação direta via registro oficial shadcn
npx shadcn@latest add @magicui/border-beam
npx shadcn@latest add @magicui/animated-beam
npx shadcn@latest add @magicui/bento-grid
npx shadcn@latest add @magicui/marquee
npx shadcn@latest add @magicui/shimmer-button
npx shadcn@latest add @magicui/blur-fade
```

**Dependências estruturais básicas** instaladas no `package.json`:
```json
{
  "dependencies": {
    "clsx": "^2.1.1",
    "tailwind-merge": "^2.5.4",
    "motion": "^12.0.0",
    "lucide-react": "^0.460.0",
    "cobe": "^0.6.3"
  }
}
```

### Configuração de Animações no Tailwind CSS (v3 / v4)

No arquivo `tailwind.config.ts`, o Magic UI adiciona keyframes essenciais para o funcionamento dos feixes e esteiras:

```typescript
// tailwind.config.ts (extensão do theme)
export default {
  theme: {
    extend: {
      animation: {
        "border-beam": "border-beam calc(var(--duration)*1s) infinite linear",
        "marquee": "marquee var(--duration) linear infinite",
        "marquee-vertical": "marquee-vertical var(--duration) linear infinite",
        "shimmer": "shimmer 8s infinite",
        "meteor": "meteor 5s linear infinite",
        "orbit": "orbit calc(var(--duration)*1s) linear infinite",
      },
      keyframes: {
        "border-beam": {
          "100%": {
            "offset-distance": "100%",
          },
        },
        "marquee": {
          from: { transform: "translateX(0)" },
          to: { transform: "translateX(calc(-100% - var(--gap)))" },
        },
        "marquee-vertical": {
          from: { transform: "translateY(0)" },
          to: { transform: "translateY(calc(-100% - var(--gap)))" },
        },
        "orbit": {
          "0%": {
            transform: "rotate(0deg) translateY(calc(var(--radius) * 1px)) rotate(0deg)",
          },
          "100%": {
            transform: "rotate(360deg) translateY(calc(var(--radius) * 1px)) rotate(-360deg)",
          },
        },
      },
    },
  },
};
```

---

### Física de Movimento e Transições

O Magic UI calibra rigorosamente suas curvas de interpolação e parâmetros de física de mola (*springs*) para equilibrar energia e refinamento corporativo:

1. **Entradas Suaves e Revelações Ópticas (`Blur Fade`)**:
   - Curva de Bezier Cúbica: `cubic-bezier(0.16, 1, 0.3, 1)` (conhecida como `easeOutExpo`).
   - Duração: `0.4s` a `0.6s`.
   - Variação do desfoque: `blur(6px)` para `blur(0px)`.
   - Deslocamento Y: `+6px` para `0px` (evita saltos bruscos comuns de 20px+).

2. **Física de Mola do Dock e Interações Magnéticas**:
   - `stiffness: 400`
   - `damping: 30`
   - `mass: 0.8`
   - Permite que os ícones do Dock cresçam e encolham sob o cursor sem oscilações gelatinosas residuais indesejadas.

3. **Física Numérica Contínua (`Number Ticker`)**:
   - `stiffness: 100`
   - `damping: 30`
   - Configurada via `useSpring` da Motion, desacelerando a rolagem do valor à medida que converge para o total numérico final.

---

### Receita de Código Funcional 1: O Efeito Emblemático `BorderBeam`

Implementação profissional e desacoplada do feixe de borda itinerante, compatível com qualquer cartão retangular:

```tsx
"use client";

import React from "react";
import { cn } from "@/lib/utils";

interface BorderBeamProps {
  className?: string;
  size?: number; // Comprimento do feixe em pixels
  duration?: number; // Duração do ciclo completo em segundos
  borderWidth?: number; // Espessura da borda
  anchor?: number; // Ponto de partida percentual
  colorFrom?: string; // Cor inicial do feixe
  colorTo?: string; // Cor final do feixe
  delay?: number; // Atraso de início
}

export function BorderBeam({
  className,
  size = 200,
  duration = 14,
  anchor = 90,
  borderWidth = 1.5,
  colorFrom = "#ffaa40",
  colorTo = "#9c40ff",
  delay = 0,
}: BorderBeamProps) {
  return (
    <div
      style={
        {
          "--size": size,
          "--duration": duration,
          "--anchor": anchor,
          "--border-width": borderWidth,
          "--color-from": colorFrom,
          "--color-to": colorTo,
          "--delay": `-${delay}s`,
        } as React.CSSProperties
      }
      className={cn(
        "pointer-events-none absolute inset-0 rounded-[inherit]",
        "[border:calc(var(--border-width)*1px)_solid_transparent]",
        // Máscara composta para exibir apenas o contorno da borda
        "![mask-clip:padding-box,border-box]",
        "![mask-composite:intersect]",
        "[mask:linear-gradient(transparent,transparent),linear-gradient(white,white)]",
        // Efeito de pseudo-elemento itinerante
        "after:absolute after:aspect-square after:w-[calc(var(--size)*1px)]",
        "after:animate-border-beam after:[animation-delay:var(--delay)]",
        "after:[background:linear-gradient(to_left,var(--color-from),var(--color-to),transparent)]",
        "after:[offset-anchor:calc(var(--anchor)*1%)_50%]",
        "after:[offset-path:rect(0_auto_auto_0_round_calc(var(--size)*1px))]",
        className
      )}
    />
  );
}
```

---

### Receita de Código Funcional 2: Conexão Dinâmica de Nós com `AnimatedBeam`

Implementação técnica simplificada de rastreamento de coordenadas e renderização de feixes de dados SVG dinâmicos entre dois elementos:

```tsx
"use client";

import React, { useEffect, useId, useState } from "react";
import { motion } from "framer-motion";
import { cn } from "@/lib/utils";

export interface AnimatedBeamProps {
  className?: string;
  containerRef: React.RefObject<HTMLElement | null>;
  fromRef: React.RefObject<HTMLElement | null>;
  toRef: React.RefObject<HTMLElement | null>;
  curvature?: number;
  reverse?: boolean;
  pathColor?: string;
  pathWidth?: number;
  pathOpacity?: number;
  gradientStartColor?: string;
  gradientStopColor?: string;
  delay?: number;
  duration?: number;
}

export function AnimatedBeam({
  className,
  containerRef,
  fromRef,
  toRef,
  curvature = 0,
  reverse = false,
  duration = 4,
  delay = 0,
  pathColor = "rgba(255, 255, 255, 0.12)",
  pathWidth = 2,
  pathOpacity = 0.2,
  gradientStartColor = "#38bdf8",
  gradientStopColor = "#818cf8",
}: AnimatedBeamProps) {
  const id = useId();
  const [pathD, setPathD] = useState("");
  const [svgDimensions, setSvgDimensions] = useState({ width: 0, height: 0 });

  useEffect(() => {
    const updatePath = () => {
      if (!containerRef.current || !fromRef.current || !toRef.current) return;

      const containerRect = containerRef.current.getBoundingClientRect();
      const rectA = fromRef.current.getBoundingClientRect();
      const rectB = toRef.current.getBoundingClientRect();

      const svgWidth = containerRect.width;
      const svgHeight = containerRect.height;
      setSvgDimensions({ width: svgWidth, height: svgHeight });

      const startX = rectA.left - containerRect.left + rectA.width / 2;
      const startY = rectA.top - containerRect.top + rectA.height / 2;
      const endX = rectB.left - containerRect.left + rectB.width / 2;
      const endY = rectB.top - containerRect.top + rectB.height / 2;

      const controlX = (startX + endX) / 2;
      const controlY = (startY + endY) / 2 + curvature;

      setPathD(`M ${startX} ${startY} Q ${controlX} ${controlY} ${endX} ${endY}`);
    };

    updatePath();
    const resizeObserver = new ResizeObserver(updatePath);
    if (containerRef.current) resizeObserver.observe(containerRef.current);

    window.addEventListener("resize", updatePath);
    return () => {
      resizeObserver.disconnect();
      window.removeEventListener("resize", updatePath);
    };
  }, [containerRef, fromRef, toRef, curvature]);

  return (
    <svg
      fill="none"
      width={svgDimensions.width}
      height={svgDimensions.height}
      xmlns="http://www.w3.org/2000/svg"
      className={cn("pointer-events-none absolute left-0 top-0 transform-gpu stroke-2", className)}
      viewBox={`0 0 ${svgDimensions.width} ${svgDimensions.height}`}
    >
      <path
        d={pathD}
        stroke={pathColor}
        strokeWidth={pathWidth}
        strokeOpacity={pathOpacity}
        strokeLinecap="round"
      />
      <path
        d={pathD}
        stroke={`url(#${id})`}
        strokeWidth={pathWidth}
        strokeLinecap="round"
      />
      <defs>
        <motion.linearGradient
          id={id}
          gradientUnits="userSpaceOnUse"
          initial={{
            x1: "0%",
            x2: "0%",
            y1: "0%",
            y2: "0%",
          }}
          animate={{
            x1: reverse ? ["90%", "-10%"] : ["-10%", "90%"],
            x2: reverse ? ["100%", "0%"] : ["0%", "100%"],
          }}
          transition={{
            repeat: Infinity,
            ease: "linear",
            duration,
            delay,
          }}
        >
          <stop stopColor={gradientStartColor} stopOpacity="0" />
          <stop stopColor={gradientStartColor} />
          <stop offset="32.5%" stopColor={gradientStopColor} />
          <stop offset="100%" stopColor={gradientStopColor} stopOpacity="0" />
        </motion.linearGradient>
      </defs>
    </svg>
  );
}
```

---

### Receita de Código Funcional 3: Estrutura Completa de `BentoGrid` com Cartões Interativos

```tsx
import React, { ReactNode } from "react";
import { ArrowRightIcon } from "lucide-react";
import { cn } from "@/lib/utils";

export function BentoGrid({
  children,
  className,
}: {
  children: ReactNode;
  className?: string;
}) {
  return (
    <div
      className={cn(
        "grid w-full auto-rows-[22rem] grid-cols-1 md:grid-cols-3 gap-4",
        className
      )}
    >
      {children}
    </div>
  );
}

export function BentoCard({
  name,
  className,
  background,
  Icon,
  description,
  href,
  cta,
}: {
  name: string;
  className?: string;
  background: ReactNode;
  Icon: React.ElementType;
  description: string;
  href: string;
  cta: string;
}) {
  return (
    <div
      key={name}
      className={cn(
        "group relative col-span-3 flex flex-col justify-between overflow-hidden rounded-2xl",
        // Superfície em Dark Mode profundo
        "bg-neutral-950 [box-shadow:0_0_0_1px_rgba(255,255,255,0.08)]",
        "transform-gpu transition-all duration-300 hover:[box-shadow:0_0_0_1px_rgba(255,255,255,0.2)]",
        className
      )}
    >
      {/* Background Dinâmico / Gráfico */}
      <div className="absolute inset-0 transition-transform duration-500 ease-out group-hover:scale-105">
        {background}
      </div>

      {/* Gradiente de escurecimento para leitura do texto */}
      <div className="pointer-events-none absolute inset-0 bg-gradient-to-t from-neutral-950 via-neutral-950/60 to-transparent" />

      {/* Conteúdo textual e ícone */}
      <div className="relative z-10 flex flex-col gap-2 p-6 transition-all duration-300">
        <div className="flex h-11 w-11 items-center justify-center rounded-xl border border-white/10 bg-white/5 text-white shadow-inner">
          <Icon className="h-5 w-5" />
        </div>
        <h3 className="text-xl font-semibold text-neutral-100 tracking-tight">
          {name}
        </h3>
        <p className="max-w-lg text-sm text-neutral-400 leading-relaxed">
          {description}
        </p>
      </div>

      {/* Botão de Chamada com revelação no hover */}
      <div className="relative z-10 flex items-center p-6 pt-0">
        <a
          href={href}
          className="inline-flex items-center gap-2 text-sm font-medium text-white/80 transition-colors hover:text-white"
        >
          {cta}
          <ArrowRightIcon className="h-4 w-4 transition-transform duration-200 group-hover:translate-x-1" />
        </a>
      </div>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma nova interface e especificar componentes do **Magic UI** no blueprint de design arquitetural, a inteligência artificial deve seguir as seguintes diretrizes estritas:

### 1. Declaração e Alocação por Seção da Página
- **Hero Section**:
  - Envelopar títulos e subtítulos com `<BlurFade delay={0.1}>`.
  - Usar `<WordRotate>` ou `<HyperText>` apenas na palavra-chave transformadora do H1.
  - Alocar um `<Safari>` ou `<IPhone15Pro>` com screenshot de alta fidelidade do produto.
  - Inserir um `<ShimmerButton>` exclusivamente no CTA principal de conversão primária.
- **Social Proof / Parcerias**:
  - Declarar um `<Marquee pauseOnHover={true} className="[--duration:35s]">` com máscara lateral gradiente para logotipos de clientes.
- **Seção de Recursos (Features)**:
  - Estruturar em um `<BentoGrid>` composto por 4 a 5 cartões com variação de largura (`md:col-span-2` e `md:col-span-1`).
  - Utilizar efeitos de fundo sutilmente distintos por cartão (ex: um com `<Particles>`, um com preview de código e um com estatística em `<Number Ticker>`).
- **Seção de Integrações**:
  - Centralizar o logotipo do produto e conectar serviços terceiros via `<AnimatedBeam>`.
- **Tabela de Preços (Pricing)**:
  - Aplicar `<BorderBeam size={250} duration={12}>` **estritamente no cartão do plano Pro / Recomendado** para maximizar a taxa de clique.

### 2. Guardrails Estéticos e de Performance para Geração de Código
- **Máximo de 1 Border Beam Visível Simultaneamente**: Nunca aplicar `BorderBeam` em todos os três cards de preço ou em todos os cards do grid; o feixe deve ser um holofote de decisão, não uma decoração genérica.
- **Obrigatoriedade de Máscaras em Marquees**: Todo marquee horizontal deve conter a classe de máscara `[mask-image:linear-gradient(to_right,transparent,white_20%,white_80%,transparent)]` para evitar cortes secos nos limites da viewport.
- **Suporte Nativo a Redução de Movimento**: Garantir que as animações de `motion` possuam fallbacks quando `window.matchMedia('(prefers-reduced-motion: reduce)')` estiver ativo.
- **Stack Técnica Padrão**: Importar Motion via `motion/react` ou `framer-motion`, respeitando a convenção do projeto sem colisões de versão.
