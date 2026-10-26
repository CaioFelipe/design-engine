---
id: "reactbits-dev"
name: "React Bits"
url: "https://reactbits.dev/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Creative Coding & WebGL Shaders", "Cyberpunk Kinetic Typography", "Dark Craft Tactile Micro-Interactions", "Fluid Spring Physics & Cursor Magnetism"]
densidade_informacao: "Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Motion/Springs) a Alto (WebGL Shaders/OGL)"
stack_frameworks: ["React 18/19", "Next.js (App Router)", "Tailwind CSS (v3 & v4)", "Motion (Framer Motion)", "OGL (WebGL)", "Three.js (opcional)"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Geist Mono", "JetBrains Mono", "Inter", "Syne", "Space Grotesk"]
  paletas_ideais: ["Deep Space Black (Zinc 950 / Black #050505)", "Neon Matrix Green / Cyan Bioluminescence", "Electric Violet & Holographic Iridescence", "High-Contrast Monochrome with Radial Glows"]
  combinacoes_recomendadas: ["Shadcn UI", "Magic UI", "Cult UI", "Aceternity UI", "21st.dev"]
  conflitos_esteticos: ["Corporate Memphis pastel infantil", "Flat Retro Neobrutalism estático e sem easing", "Material Design 2 com elevações rígidas e sombras primárias pesadas"]
---

# React Bits — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo engenheiro de software e designer **David Haz** (`@DavidHDev`), o **React Bits** (`reactbits.dev`) é uma das maiores e mais influentes bibliotecas abertas de componentes animados, tipografia cinética e shaders WebGL do ecossistema React contemporâneo. Com mais de 215 componentes e efeitos de plano de fundo prontos para produção, o React Bits preenche a lacuna histórica entre o **Creative Coding** de alta performance (tradicionalmente confinado a estúdios de vanguarda e sites experimentais do Awwwards/FWA) e o desenvolvimento de software corporativo modular baseado no ecossistema `shadcn/ui`.

A assinatura visual do React Bits é definida por quatro pilares técnicos e estéticos:

1. **Fusão entre Creative Technology e Componentização Reutilizável**:
   Diferente de bibliotecas utilitárias estáticas que apenas fornecem containers e botões convencionais, o React Bits introduz renderizadores WebGL baseados em **OGL** (uma biblioteca WebGL ultraleve) e **Canvas 2D**, combinados com a orquestração vetorial do **Motion** (anteriormente Framer Motion). O resultado é uma estética fluida com gradientes bioluminescentes (*Aurora*), superfícies peroladas que distorcem em tempo real (*Iridescence*), campos de velocidade futuristas (*Hyperspeed*) e simulações físicas de colisão (*Ballpit*).

2. **Tipografia Cinética de Alta Precisão (Kinetic Typography)**:
   A tipografia deixa de ser um bloco estático de texto para se tornar uma interface viva. O React Bits é referência mundial em animações de texto granulares:
   - **Decrypted Text**: simulações criptográficas e de decodificação estilo cyberpunk/hacker onde caracteres embaralhados convergem ordenadamente para o destino.
   - **Split Text & Blur Text**: desmontagem de glifos e palavras com transições escalonadas (*stagger*) e desfoque gaussiano progressivo.
   - **Variable Proximity**: manipulação dinâmica das variáveis OpenType de fontes variáveis (`wght`, `wdth`, `slnt`) com base na distância euclidiana do cursor do mouse em tempo real.

3. **Arquitetura Poliglota Quádrupla (4-Flavor Matrix)**:
   Uma das maiores inovações de usabilidade para desenvolvedores é a disponibilização de **cada componente em 4 sabores independentes**:
   - `TypeScript + Tailwind CSS` (`-TS-TW`)
   - `JavaScript + Tailwind CSS` (`-JS-TW`)
   - `TypeScript + Vanilla CSS` (`-TS-CSS`)
   - `JavaScript + Vanilla CSS` (`-JS-CSS`)
   Isso elimina o aprisionamento tecnológico (*vendor lock-in*) e permite que equipes que não utilizam Tailwind ainda desfrutem das matrizes de animação sem atrito.

4. **Integração com Registro Shadcn & Suporte Nativo a Agentes MCP**:
   O React Bits adota o padrão de distribuição aberta via protocolo de registro do shadcn. Não há um pacote pesado e monolítico instalado via `npm install reactbits-everything`. Os componentes são clonados sob demanda via CLI (`npx shadcn@latest add @react-bits/...`). Além disso, o projeto fornece integração nativa com o **shadcn MCP Server**, permitindo que agentes de Inteligência Artificial (Claude Code, Cursor, Copilot Workspace) leiam o catálogo, inspecionem as propriedades e instalem os componentes diretamente nas bases de código dos projetos via instruções em linguagem natural.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **DevTools, Plataformas de Nuvem & Infraestrutura Técnica**:
   É a biblioteca primordial para produtos voltados a desenvolvedores (IDEs na web, terminais em nuvem, ferramentas de observabilidade, bancos de dados). Componentes como *Decrypted Text*, *Squares Background*, *Star Border* e *Spotlight Card* transmitem imediatamente a autoridade técnica de sistemas de alta precisão.
2. **Produtos de Inteligência Artificial Generativa & Workspaces de Agentes**:
   Interfaces conversacionais e copilotos exigem feedback visual durante tarefas demoradas. O uso de *True Focus*, *Shiny Text*, *Hyperspeed* ou o fundo *Aurora* em estados de inferência e geração de tokens cria um senso de computação profunda e inteligência viva.
3. **Landing Pages de Lançamento de Hardware & Produtos Premium (Dark Craft)**:
   Dispositivos físicos de áudio, computação espacial e periféricos demandam uma estética tátil luxuosa. A combinação de *Tilted Card*, *Iridescence*, *Fluid Glass* e *Magnet Buttons* gera uma experiência sensorial próxima a tocar o hardware real.
4. **Portfólios de Creative Technologists, Design Engineers & Estúdios Digitais**:
   Projetos que precisam comunicar maestria técnica logo no primeiro scroll, utilizando *Circular Gallery*, *Flowing Menu*, *Rolling Gallery* e *Variable Proximity* para transformar a navegação em uma obra de arte interativa.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Estrutural e Sóbria)**:
  Superfícies neutras baseadas nos tokens do `shadcn/ui` ou Tailwind padrão (`bg-zinc-950`, `border-zinc-800`, tipografia limpa como `Geist Sans` ou `Inter`, com layout em grade consistente e legibilidade irrestrita).
- **30% (Camada Tátil e Micro-interações do React Bits)**:
  Componentes de resposta direta ao cursor do usuário: botões com atração física (*Magnet*), cartões de recursos com reflexo luminoso posicional (*Spotlight Card*), foco dinâmico em listas (*True Focus*) e textos com brilho sutil (*Shiny Text*).
- **10% (Showstoppers Protagonistas)**:
  Exclusivamente **um** efeito de impacto monumental por página ou seção ativa: o fundo de shader WebGL na Hero Section (*Aurora*, *Hyperspeed* ou *Waves*) **ou** a tipografia heroica animada na entrada da viewport (*Decrypted Text* em tamanho display ou *Split Text* com desfoque). Nunca acumule dois shaders pesados na mesma tela visível.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Tabelas Analíticas Densas e Painéis Operacionais (Data Grids B2B)**:
  Em telas com 100+ células de dados simultâneas, gráficos financeiros em tempo real ou ERPs transacionais, a injeção de efeitos de *Spotlight*, animações de texto escalonadas ou fundos com shaders WebGL sobrecarrega a CPU/GPU e gera ruído visual intolerável para analistas.
- **Formulários Críticos de Checkout, Autenticação e Transações Bancárias**:
  Campos de senha, número de cartão de crédito e botões de "Confirmar Pagamento" não devem usar *Decrypted Text* ou transições com atraso deliberado. A clareza visual e o tempo de resposta determinístico de 0ms são prioridades absolutas de conversão e segurança.
- **Dispositivos Móveis de Baixa Potência com Redes Móveis Limitadas**:
  Shaders WebGL baseados em loops `requestAnimationFrame` contínuos (*Aurora*, *Hyperspeed*, *Liquid Chrome*) drenam rapidamente a bateria e elevam a temperatura de processadores mobile modestos. O fallback para gradientes CSS estáticos em viewports móveis é mandatório.
- **Aplicações sem Suporte a Redução de Movimento (Acessibilidade WCAG AAA)**:
  Usuários com distúrbios vestibulares ou fotossensibilidade sofrem com efeitos de túnel de luz (*Hyperspeed*) ou caracteres piscantes (*Decrypted Text*). Se o projeto não puder honrar a media query `@media (prefers-reduced-motion: reduce)`, esses componentes não devem ser aplicados.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **Síndrome do "Shader Soup"**: Colocar um shader de *Aurora* no fundo do Hero, um cursor *Splash Cursor* que espirra fluidos, e cartões com *Liquid Chrome* na mesma viewport. O site perde credibilidade técnica e se torna um experimento visual poluído e pesado.
- **Decrypted Text em Parágrafos Corridos**: Aplicar o efeito de decodificação criptográfica em blocos de texto explicativo ou subtítulos longos. O usuário deseja ler a informação; o efeito pertence estritamente a palavras-chave (H1, badges técnicos, nomes de planos ou callouts curtos).
- **Raio de Atração Magnética Excessivo no Componente Magnet**: Configurar o `Magnet` com raio de influência superior a 150px, fazendo o botão saltar na direção do mouse muito antes de o usuário realmente desejar interagir, o que "sequestra" a intenção de navegação e frustra a experiência.
- **Falta de Desativação de Shaders fora da Viewport**: Não pausar o render loop WebGL quando o usuário faz scroll e a seção sai da tela. O componente de fundo DEVE utilizar `IntersectionObserver` para interromper o `requestAnimationFrame` quando não estiver visível.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão 12 componentes emblemáticos do ecossistema React Bits:

### 1. Decrypted Text (`decrypted-text`)
- **Categoria**: *Text Animations*
- **Anatomia Visual**: O texto inicia preenchido por glifos aleatórios (caracteres ASCII, hexadecimais, símbolos binários ou alfabetos criptográficos customizáveis). Ao entrar na viewport ou receber hover, os caracteres são sucessivamente decodificados em alta velocidade até revelarem a palavra original. Acompanhado opcionalmente de cor de destaque transitória e estilo monoespaçado.
- **Gatilho de Interação**: Disparado no carregamento/scroll (`animateOn="view"`) ou na passagem do cursor (`animateOn="hover"`).
- **Onde encaixar**: Palavras-chave no H1 de Hero Sections de cibersegurança/DevTools, badges de status do sistema ("SYSTEM ONLINE", "AGENTS DEPLOYED") e cabeçalhos de Bento Grids técnicos.

### 2. Split Text (`split-text`)
- **Categoria**: *Text Animations*
- **Anatomia Visual**: Divide strings de texto em elementos atômicos isolados (caracteres, palavras ou linhas), encapsulados em containers `overflow-hidden`. As letras emergem do fundo através de uma transição vertical suave (`translateY(100%)` → `translateY(0%)`) com escala de opacidade e atraso escalonado milimétrico (*stagger delay*).
- **Gatilho de Interação**: Disparo automático na entrada da viewport via Intersection Observer (`whileInView`).
- **Onde encaixar**: Títulos principais (H1/H2) de Landing Pages SaaS, slogans de posicionamento de produto e frases de manifesto de marca.

### 3. Blur Text (`blur-text`)
- **Categoria**: *Text Animations*
- **Anatomia Visual**: As palavras ou caracteres entram em cena transicionando de um estado difuso de desfoque intenso (`filter: blur(12px)` e `opacity: 0`) para foco cirúrgico nítido (`filter: blur(0px)` e `opacity: 1`), acompanhado de um leve deslocamento vertical negativo. Produz uma sensação etérea de "revelação fotográfica".
- **Gatilho de Interação**: Disparo na visualização de tela com atrasos incrementais configuráveis por palavra.
- **Onde encaixar**: Subtítulos de impacto na Hero Section, depoimentos focais de clientes ou seções de encerramento de página (Call to Action).

### 4. Variable Proximity (`variable-proximity`)
- **Categoria**: *Text Animations*
- **Anatomia Visual**: Um parágrafo ou título renderizado com uma fonte variável OpenType (como *Roboto Flex*, *Inter Variable* ou *Geist Sans*). À medida que o cursor do usuário se desloca sobre o texto, os glifos que estão próximos do ponteiro alteram organicamente seu peso (`wght`), largura (`wdth`) ou inclinação (`slnt`) com base na distância radial contínua.
- **Gatilho de Interação**: Evento contínuo de `onMouseMove` rastreado sobre o container delimitador.
- **Onde encaixar**: Cabeçalhos interativos de portfólios de design, seções de declaração de missão de marcas criativas e blocos de introdução em landing pages de vanguarda.

### 5. Aurora (`aurora`)
- **Categoria**: *Backgrounds*
- **Anatomia Visual**: Um fundo gerado em tempo real via shader WebGL (utilizando a biblioteca ultraleve OGL) que simula o movimento fluido e hipnótico da Aurora Boreal. Ondas suaves de luz bioluminescente em tons de ciano, verde esmeralda, violeta profundo e magenta deslizam suavemente sobre um fundo escuro com ruído de Simplex Noise e mistura de cores de alta fidelidade.
- **Gatilho de Interação**: Animação temporal contínua autônoma (`uTime`), com resposta opcional à posição vetorial do mouse (`uMouse`).
- **Onde encaixar**: Background absoluto de Hero Sections de plataformas de IA, banners de waitlist e cabeçalhos de produtos de software de próxima geração.

### 6. Hyperspeed (`hyperspeed`)
- **Categoria**: *Backgrounds*
- **Anatomia Visual**: Um túnel tridimensional de alta velocidade que projeta rastros de luz e linhas de néon acelerando em direção à câmera, evocando o salto no hiperespaço de espaçonaves de ficção científica. Permite calibrar a distorção da perspectiva de câmera (`fov`), velocidade das partículas, largura das pistas e curvatura da malha de aceleração.
- **Gatilho de Interação**: Renderização contínua com ampliação de velocidade ao pressionar o mouse ou fazer scroll na página.
- **Onde encaixar**: Hero sections de produtos de computação em nuvem de baixa latência, redes blockchain de alta taxa de transferência (TPS) e plataformas de streaming de dados.

### 7. Iridescence (`iridescence`)
- **Categoria**: *Backgrounds*
- **Anatomia Visual**: Uma superfície fluida e líquida gerada por shader que simula o brilho iridescente de madrepérola, superfícies de titânio usinado ou películas de óleo. As cores refratam e produzem reflexos cromados que se transformam de acordo com as coordenadas do ponteiro e ciclos matemáticos de seno/cosseno.
- **Gatilho de Interação**: Interação em tempo real com o ponteiro do mouse e pulsação temporal orgânica.
- **Onde encaixar**: Fundo de cartões de pricing do plano "Pro / Enterprise", seções de produtos de moda digital/Web3 e módulos de revelação de hardware de luxo.

### 8. Squares Background (`squares`)
- **Categoria**: *Backgrounds*
- **Anatomia Visual**: Uma grade matemática minimalista de pequenos blocos quadrados desenhada sobre Canvas 2D. Quando o usuário desliza o cursor sobre a área, os quadrados sob o mouse acendem instantaneamente com uma borda/preenchimento brilhante e depois desvanecem lentamente através de um algoritmo de decaimento de trilha (*trail decay*).
- **Gatilho de Interação**: Rastreamento de `onMouseMove` do cursor, com taxa de decaimento configurável e cor de destaque adaptável.
- **Onde encaixar**: Fundo estrutural de seções de recursos técnicos (Features Grid), dashboards de desenvolvedores e páginas de documentação de APIs.

### 9. Magnet (`magnet`)
- **Categoria**: *Animations / Micro*
- **Anatomia Visual**: Um invólucro de micro-interação que confere comportamento de "atração magnética" a qualquer componente filho (botões, avatares, ícones flutuantes). Quando o cursor entra no raio de influência do elemento, este é suavemente puxado em direção ao ponteiro com física de mola balanceada, liberando-se e retornando à origem com amortecimento realista ao sair.
- **Gatilho de Interação**: Hover e proximidade radial do mouse (`onMouseMove` e `onMouseLeave`).
- **Onde encaixar**: Botões primários de chamada para ação (CTA "Começar Agora"), ícones de redes sociais no footer, botões de reprodução de vídeo e seletores de tema flutuantes.

### 10. Spotlight Card (`spotlight-card`)
- **Categoria**: *Components*
- **Anatomia Visual**: Um cartão em tema escuro (`bg-zinc-900/90`) com bordas sutis. Ao passar o mouse sobre sua superfície, um feixe de luz radial (*spotlight*) suave e translúcido segue o cursor com precisão matemática, iluminando tanto a textura interna quanto a borda externa através de gradientes em coordenadas relativas calculadas via variáveis CSS (`--mouse-x`, `--mouse-y`).
- **Gatilho de Interação**: Movimento do ponteiro sobre a superfície do cartão (`onMouseMove`).
- **Onde encaixar**: Grades de preços (Pricing Tables), Bento Grids de funcionalidades centrais de produto e vitrines de integrações de ecossistema.

### 11. Tilted Card (`tilted-card`)
- **Categoria**: *Components*
- **Anatomia Visual**: Um cartão com perspectiva tridimensional (`perspective: 1000px`) que inclina seus eixos X e Y proporcionalmente ao ângulo de aproximação do cursor. Apresenta uma camada de brilho reflexivo (*glare effect*) que se desloca contra a rotação física, conferindo textura tátil de cartão colecionável ou hardware físico. Suporta tooltip flutuante que acompanha o cursor em uma camada paralela superior.
- **Gatilho de Interação**: Inclinação em tempo real via cálculo de coordenadas `(clientX - rect.left) / width`.
- **Onde encaixar**: Demonstrações visuais de mockups de aplicativos, exibição de planos de assinatura VIP e cartões de membros da equipe fundadora.

### 12. Splash Cursor (`splash-cursor`)
- **Categoria**: *Animations*
- **Anatomia Visual**: Simulação contínua de fluidos e fumaça em tempo real renderizada em Canvas WebGL com base nas equações de Navier-Stokes. À medida que o cursor se move ou clica pela tela, vórtices de cores vibrantes e fluidas explodem e se dissipam com física molecular fotorrealista.
- **Gatilho de Interação**: `mousemove`, `mousedown` e velocidade de deslocamento do cursor do usuário.
- **Onde encaixar**: Aplicações de experiências de marca imersivas, sites de estúdios criativos, lançamentos de festivais/música e páginas "404" interativas memoráveis.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup
O ecossistema React Bits é fundamentado na independência modular. As dependências centrais para suportar a totalidade de seus componentes incluem:

```bash
npm install motion ogl clsx tailwind-merge lucide-react
```

- **`motion`** (versão contemporânea da Framer Motion): Responsável pela cinemática vetorial de layout, springs táteis e transições de entrada/saída.
- **`ogl`**: Biblioteca WebGL minimalista e de baixíssimo consumo de memória (desenvolvida por Nathan Gordon), utilizada pelos shaders de background (*Aurora*, *Iridescence*, *Waves*). Substitui bibliotecas pesadas como Three.js para tarefas puras de renderização de tela cheia.
- **`clsx` & `tailwind-merge`**: Utilitários para concatenação segura e resolução de classes conflitantes do Tailwind CSS.

### Integração com o Registro Shadcn & MCP
Para usufruir da instalação automatizada via CLI e permitir que assistentes de IA instalem componentes do React Bits via linguagem natural, configure o endpoint do registro no arquivo `components.json`:

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
  "registries": {
    "@react-bits": "https://reactbits.dev/r/{name}.json"
  }
}
```

Com o registro cadastrado, a instalação de componentes segue a convenção de nomenclatura declarativa:
```bash
# Instalação com suporte a TypeScript e Tailwind CSS
npx shadcn@latest add @react-bits/SpotlightCard-TS-TW
npx shadcn@latest add @react-bits/DecryptedText-TS-TW
npx shadcn@latest add @react-bits/Magnet-TS-TW
```

Para habilitar agentes autônomos locais (Claude Code, Cursor) via MCP:
```bash
npx shadcn@latest mcp init --client claude
```

---

### Física de Movimento, Curvas de Easing & Shaders

1. **Parâmetros de Molas (Spring Kinetics)**:
   - Para o efeito **Magnet** (atração e estilingue):
     ```typescript
     const springConfig = {
       stiffness: 150, // Resposta elástica imediata
       damping: 15,    // Controle de oscilações residuais
       mass: 0.1       // Leveza para evitar arrasto perceptual
     };
     ```
   - Para o efeito **Tilted Card** (inclinação tridimensional):
     ```typescript
     const tiltSpringConfig = {
       stiffness: 300,
       damping: 30,
       mass: 0.5
     };
     ```

2. **Curvas de Easing de Referência (Cubic-Bezier)**:
   - Para revelação de texto cinético (*Split Text*, *Blur Text*):
     ```css
     transition-timing-function: cubic-bezier(0.16, 1, 0.3, 1); /* Expo Out - acabamento premium */
     ```
   - Para decaimento de luz no *Spotlight Card*:
     ```css
     transition: opacity 0.5s cubic-bezier(0.25, 0.1, 0.25, 1);
     ```

3. **Arquitetura de Shaders WebGL com OGL**:
   Os shaders de background operam com um ciclo de renderização enxuto em `requestAnimationFrame`, enviando uniforms matemáticos para o fragment shader:
   - `uTime`: contador cumulativo de segundos para evolução temporal contínua dos ruídos matemáticos.
   - `uResolution`: vetor bidimensional (`vec2(width, height)`) com correção de densidade de pixels (`Math.min(window.devicePixelRatio, 2)`).
   - `uMouse`: vetor bidimensional normalizado das coordenadas do cursor para distorção reativa.

---

### Receitas de Código Funcionais

#### Receita 1: `SpotlightCard.tsx` (Componente de Superfície Tátil com Borda Iluminada)

```tsx
import React, { useRef, useState } from "react";
import { cn } from "@/lib/utils";

interface SpotlightCardProps extends React.HTMLAttributes<HTMLDivElement> {
  children: React.ReactNode;
  className?: string;
  spotlightColor?: string;
}

export const SpotlightCard: React.FC<SpotlightCardProps> = ({
  children,
  className = "",
  spotlightColor = "rgba(255, 255, 255, 0.12)",
  ...props
}) => {
  const divRef = useRef<HTMLDivElement>(null);
  const [position, setPosition] = useState<{ x: number; y: number }>({ x: 0, y: 0 });
  const [opacity, setOpacity] = useState<number>(0);

  const handleMouseMove = (e: React.MouseEvent<HTMLDivElement>) => {
    if (!divRef.current) return;
    const rect = divRef.current.getBoundingClientRect();
    setPosition({ x: e.clientX - rect.left, y: e.clientY - rect.top });
  };

  const handleMouseEnter = () => setOpacity(1);
  const handleMouseLeave = () => setOpacity(0);

  return (
    <div
      ref={divRef}
      onMouseMove={handleMouseMove}
      onMouseEnter={handleMouseEnter}
      onMouseLeave={handleMouseLeave}
      className={cn(
        "relative rounded-2xl border border-zinc-800 bg-zinc-900/80 p-8 overflow-hidden backdrop-blur-md transition-colors duration-300 hover:border-zinc-700/80",
        className
      )}
      {...props}
    >
      {/* Camada do feixe radial de luz (Spotlight) */}
      <div
        className="pointer-events-none absolute -inset-px rounded-2xl opacity-0 transition-opacity duration-300"
        style={{
          opacity,
          background: `radial-gradient(600px circle at ${position.x}px ${position.y}px, ${spotlightColor}, transparent 70%)`,
        }}
        aria-hidden="true"
      />

      {/* Conteúdo do cartão preservado no plano superior */}
      <div className="relative z-10">{children}</div>
    </div>
  );
};
```

---

#### Receita 2: `DecryptedText.tsx` (Tipografia Cinética Criptográfica Cyberpunk)

```tsx
import React, { useEffect, useState, useRef } from "react";
import { motion, useInView } from "motion/react";
import { cn } from "@/lib/utils";

interface DecryptedTextProps {
  text: string;
  speed?: number;
  maxIterations?: number;
  characters?: string;
  className?: string;
  encryptedClassName?: string;
  animateOn?: "view" | "hover";
}

export const DecryptedText: React.FC<DecryptedTextProps> = ({
  text,
  speed = 50,
  maxIterations = 10,
  characters = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz!@#$%^&*()_+~`|}{[]:;?><,./-=",
  className = "",
  encryptedClassName = "text-emerald-400 font-mono",
  animateOn = "view",
}) => {
  const [displayText, setDisplayText] = useState<string>(text);
  const [isHovering, setIsHovering] = useState<boolean>(false);
  const containerRef = useRef<HTMLSpanElement>(null);
  const isInView = useInView(containerRef, { once: true });

  useEffect(() => {
    // Respeito estrito à preferência do usuário de redução de movimento
    const prefersReducedMotion = window.matchMedia("(prefers-reduced-motion: reduce)").matches;
    if (prefersReducedMotion) {
      setDisplayText(text);
      return;
    }

    if (animateOn === "view" && !isInView) return;
    if (animateOn === "hover" && !isHovering) {
      setDisplayText(text);
      return;
    }

    let iteration = 0;
    const interval = setInterval(() => {
      setDisplayText(() =>
        text
          .split("")
          .map((char, index) => {
            if (char === " ") return " ";
            if (index < iteration) {
              return text[index];
            }
            return characters[Math.floor(Math.random() * characters.length)];
          })
          .join("")
      );

      if (iteration >= text.length) {
        clearInterval(interval);
      }
      iteration += 1 / (maxIterations / 2);
    }, speed);

    return () => clearInterval(interval);
  }, [isInView, isHovering, text, speed, maxIterations, characters, animateOn]);

  return (
    <span
      ref={containerRef}
      onMouseEnter={() => setIsHovering(true)}
      onMouseLeave={() => setIsHovering(false)}
      className={cn("inline-block select-none", className)}
    >
      <span className={displayText !== text ? encryptedClassName : undefined}>
        {displayText}
      </span>
    </span>
  );
};
```

---

#### Receita 3: `Magnet.tsx` (Micro-interação de Atração Magnética)

```tsx
import React, { useRef } from "react";
import { motion, useMotionValue, useSpring } from "motion/react";
import { cn } from "@/lib/utils";

interface MagnetProps extends React.HTMLAttributes<HTMLDivElement> {
  children: React.ReactNode;
  strength?: number;
  className?: string;
}

export const Magnet: React.FC<MagnetProps> = ({
  children,
  strength = 0.35,
  className = "",
  ...props
}) => {
  const ref = useRef<HTMLDivElement>(null);

  const x = useMotionValue(0);
  const y = useMotionValue(0);

  // Configuração balanceada de física elástica
  const springConfig = { damping: 15, stiffness: 160, mass: 0.1 };
  const smoothX = useSpring(x, springConfig);
  const smoothY = useSpring(y, springConfig);

  const handleMouseMove = (e: React.MouseEvent<HTMLDivElement>) => {
    if (!ref.current) return;
    const { left, top, width, height } = ref.current.getBoundingClientRect();
    const centerX = left + width / 2;
    const centerY = top + height / 2;

    const distanceX = (e.clientX - centerX) * strength;
    const distanceY = (e.clientY - centerY) * strength;

    x.set(distanceX);
    y.set(distanceY);
  };

  const handleMouseLeave = () => {
    x.set(0);
    y.set(0);
  };

  return (
    <motion.div
      ref={ref}
      onMouseMove={handleMouseMove}
      onMouseLeave={handleMouseLeave}
      style={{ x: smoothX, y: smoothY }}
      className={cn("inline-block cursor-pointer", className)}
      {...props}
    >
      {children}
    </motion.div>
  );
};
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar o **React Bits** como biblioteca complementar de design em um novo projeto, a IA arquiteta de software deve obedecer estritamente às seguintes instruções formais de configuração:

1. **Declaração de Papel Arquitetural no Blueprint**:
   - Classifique o React Bits como **Camada de Efeitos Notáveis e Micro-interações (Camada 30% e 10%)**.
   - Mantenha a espinha dorsal de 60% alicerçada em componentes estruturais do `shadcn/ui` (inputs, selects, modais acessíveis, data tables). O React Bits nunca deve substituir os elementos de formulário primários da aplicação.

2. **Mapeamento Explícito de Componentes por Seção**:
   - **Hero Section**:
     - *Background*: Inserir apenas **um** shader de plano de fundo (`Aurora` ou `Squares` com `opacity-60`).
     - *Título H1*: Tipografia com `SplitText` ou `BlurText` para a promessa principal de valor.
     - *Badges & Meta-tags*: Rótulos com `DecryptedText` monoespaçado para reforçar a atmosfera técnica.
     - *CTA Primário*: Botão encapsulado por `Magnet` com `strength={0.3}`.
   - **Bento Grid / Features Section**:
     - Envolver todos os cartões de recursos em `SpotlightCard` com reflexo `spotlightColor="rgba(255, 255, 255, 0.08)"` para consistência tátil harmoniosa.
     - Cartões focais interativos podem utilizar `TiltedCard`.
   - **Pricing Table**:
     - O cartão do plano de maior destaque ("Scale" ou "Enterprise") deve receber uma borda animada sutil (*Star Border*) ou reflexo *Iridescence* no fundo do badge de desconto anual.

3. **Diretrizes de Performance e Governança de Hardware**:
   - **Regra de Um Shader por Viewport**: O blueprint deve proibir expressamente mais de um canvas WebGL ativo na mesma seção.
   - **Pausa Automática via Intersection Observer**: Todo componente que renderiza um loop `requestAnimationFrame` deve pausar o ciclo de renderização assim que o elemento sair do campo de visão da viewport (`useInView(ref, { margin: "200px" })`).
   - **Fallback Mobile Obrigatório**: Em telas com largura inferior a 768px (`md:` no Tailwind), shaders intensivos de WebGL devem ser desativados ou substituídos por gradientes radiais estáticos via CSS para preservar a fluidez do scroll de 60fps e economizar bateria.

4. **Sufixos de Instalação e Convenção de Registro**:
   - No documento de blueprint, especifique explicitamente as dependências de instalação via registro shadcn com o sufixo padrão do projeto:
     ```bash
     # Padrão recomendado para Next.js 15 App Router: TypeScript + Tailwind
     npx shadcn@latest add @react-bits/SpotlightCard-TS-TW
     npx shadcn@latest add @react-bits/DecryptedText-TS-TW
     npx shadcn@latest add @react-bits/BlurText-TS-TW
     npx shadcn@latest add @react-bits/Magnet-TS-TW
     ```
