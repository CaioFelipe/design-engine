---
id: "osmo-supply"
name: "Osmo Supply"
url: "https://www.osmo.supply/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Dutch Creative Engineering", "Awwwards-Grade Motion", "Fluid Inertia & Magnetic Micro-Interactions", "Curved SVG Morphing & Page Transitions", "Kinetic Typography & Smooth Scroll Momentum"]
densidade_informacao: "Media"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (GSAP/DOM QuickTo) a Alto (SVG Path Morphing/Canvas Physics)"
stack_frameworks: ["GSAP 3 (ScrollTrigger, Flip, Draggable, CustomEase)", "Lenis Smooth Scroll", "React / Next.js", "Webflow (Cloneables)", "Tailwind CSS", "Barba.js"]
compatibilidade:
  fontes_ideais: ["PP Neue Montreal", "Syne", "Cabinet Grotesk", "Geist Sans", "Clash Display"]
  paletas_ideais: ["Deep Pitch Dark (#0e0e0e / #141414)", "Monochrome High Contrast (#FFFFFF / #000000)", "Electric Violet & Indigo Accents (#6366F1 / #8B5CF6)", "Muted Warm Neutrals (#EAE7E1 / #1D1D1B)"]
  combinacoes_recomendadas: ["Shadcn UI (estrutural e formulários)", "Motion Primitives", "Cult UI", "Lucide React", "Lenis"]
  conflitos_esteticos: ["Brutalismo rígido sem curvas nem amortecimento", "Neumorfismo plástico saturado", "Corporate Memphis corporativo infantil", "Animações lineares sem easing exponencial"]
---

# Osmo Supply — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e capitaneado pelos engenheiros criativos holandeses **Dennis Snellenberg** e **Ilja van Eck** — duas das figuras mais premiadas na história do *Awwwards* (com múltiplos títulos de *Site of the Year Nominee*, *Site of the Month* e dezenas de *Site of the Day*) —, o **Osmo Supply** (`osmo.supply`), estruturado em torno do seu repositório de elite denominado **The Vault**, é a autoridade máxima mundial em engenharia de interação criativa para a web de alto impacto.

Enquanto a maioria das bibliotecas de UI foca em componentes funcionais cotidianos (modais básicos, tabelas e selects utilitários), o Osmo Supply codifica o segredo dos maiores estúdios digitais do mundo (Locomotive, Media.Monks, Studio Freight, Build in Amsterdam). O objetivo do Osmo é democratizar e transformar técnicas complexas de física vetorial, inércia, distorção tangencial e transições cinemáticas em componentes modulares reutilizáveis tanto em ecossistemas de código puro (**React, Next.js, HTML/JS**) quanto em plataformas de desenvolvimento visual (**Webflow**).

### Os Pilares da Assinatura Visual do Osmo Supply:

1. **A Física Magnética de Dennis Snellenberg (`Magnetic Attraction & Rubber Snapback`)**:
   A marca registrada mais imitada na web contemporânea: botões, avatares e ícones não esperam passivamente o clique. Conforme o cursor entra em uma zona de atração vetorial (bounding box ampliada), o elemento é magneticamente atraído em direção às coordenadas do mouse com um fator de atenuação elástica (*lerp* e amortecimento cúbico). Ao sair da zona de influência, o elemento não volta em linha reta: ele executa um rebote de mola (*rubber snapback*) com coordenadas amortecidas via interpolação de alta precisão.
2. **Continuidade de Superfície por Cortinas SVG Dinâmicas (`Curved Path Morphing`)**:
   Aberturas de menus móveis, painéis laterais (*drawers*) e trocas de página nunca usam cortes retangulares secos. O Osmo popularizou o uso de curvas de Bézier cúbicas e quadráticas em elementos SVG (`<path d="...">`). Quando uma gaveta se abre, a borda dianteira expande-se como uma membrana elástica ou gota de líquido tensionada (`M0,0 Q50,120 100,0`), alinhando-se gradualmente até se tornar uma reta perfeita no final do percurso. O efeito transmite viscosidade e tridimensionalidade táctil orgânica.
3. **Orquestração de Páginas Sem Flash (`Barba.js + GSAP Transitions`)**:
   A quebra do paradigma tradicional de carregamento da web: o Osmo Supply trata a navegação entre rotas como uma coreografia cinematográfica contínua. Por meio de pipelines de ciclo de vida com Barba.js acoplado a timelines do GSAP (`leave` → animação de saída de elementos + cortina de transição → sincronização de DOM → `enter` com revelação progressiva), a troca de páginas ocorre com zero recarregamento visível e preservação total de contexto visual e áudio.
4. **Cinética Tipográfica de Camada Dupla (`Dual-Roll & Character Staggers`)**:
   Em vez de simples mudanças de cor de texto no `:hover`, os rótulos tipográficos são decompostos em dois invólucros sincronizados com máscara de estouro (`overflow: hidden`). No repouso, o primeiro rótulo está visível; no hover, ele sobe 100% no eixo Y enquanto uma réplica idêntica sobe de 100% para 0%, muitas vezes dividida letra por letra com atraso escalonado (*stagger delay* de 0.015s a 0.025s), produzindo um rolo tipográfico impecável de tipografia editorial de alta moda.
5. **Harmonia de Momentum e Rolagem com Lenis + GSAP ScrollTrigger**:
   O Osmo estabelece o padrão da indústria para rolagem desacoplada: utiliza a biblioteca **Lenis** (desenvolvida pela Darkroom Engineering / Studio Freight) acoplada diretamente ao ticker principal do GSAP (`gsap.ticker.add(...)`). Isso permite que parallax, travamentos pegajosos (*sticky pins*), distorções de velocidade (*velocity skews*) e rotações espaciais permaneçam com taxa de quadros travada em 60 a 120 FPS, sem o "jitter" ou atraso de rolagem nativa dos navegadores.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **Portfólios de Diretores de Arte, Creative Technologists & Designers Sênior**:
   É o padrão absoluto de referência para criadores que competem em premiações (Awwwards, FWA, CSS Design Awards). A aplicação de botões magnéticos, sliders com inércia e transições de página coloca o portfólio instantaneamente na divisão de elite internacional.
2. **Agências Digitais de Vanguarda, Boutiques Criativas & Estúdios de Branding**:
   Sites institucionais que vendem criatividade, tecnologia e posicionamento premium. A experiência de navegação do site da agência precisa servir como o próprio cartão de visitas da capacidade técnica da equipe.
3. **Lançamentos de Hardware de Luxo, Moda e Cultura (High-End E-Commerce & Lookbooks)**:
   Marcas de moda experimental, perfumaria, relojoaria, arquitetura e automóveis elétricos onde a compra é movida pelo fascínio estético, exigindo transições fluidas, carrosséis tridimensionais radiais e cursores magnéticos informativos.
4. **Landing Pages "Hero Showstopper" para Startups de IA e Tecnologia Futurista**:
   Startups que querem se distanciar do visual homogêneo de "SaaS azul/cinza" e precisam de uma presença visual imersiva que demonstre inovação em cada micro-interação.

### Papel no Ritmo Visual (Regra 60-30-10)

- **60% — Fundação Tipográfica e Estrutura Neutra**:
  Layout editorial com grids assimétricos calculados, paleta minimalista (preto profundo, branco puro ou off-white quente) e tipografia display refinada com kerning ótico cuidadoso. Toda a base do layout deve funcionar com extrema legibilidade antes do movimento ser ativado.
- **30% — Camada de Fluidez Contínua (Smooth Scroll & Micro-Interações Tácteis)**:
  - *Lenis Scroll*: Rolagem suave com amortecimento inercial em toda a página.
  - *Magnetic Elements*: Botões de navegação, ícones sociais e controles de carrossel respondendo ao raio de aproximação do cursor.
  - *Dual-Text Roll*: Todos os links de navegação e botões secundários executando rotação tipográfica em dois planos.
  - *Dynamic Sticky Cursor*: Cursor customizado que acompanha o ponteiro com interpolação linear (*lerp*) e altera dimensões conforme o contexto.
- **10% — Efeitos Protagonistas / Showstoppers (Momentos de Assombro)**:
  - *Curved SVG Morph Curtain*: Abertura cinematográfica do menu principal preenchendo a tela através de uma curvatura fluida.
  - *Radial Cards Slider*: Galeria de projetos dispostos em arco com arrasto por inércia e rotação 3D de perspectiva.
  - *Velocity-Skew Gallery*: Distorção física tangencial das imagens e tipografia que reage dinamicamente à velocidade de rolagem da página.
  - *Barba.js Route Transition*: Cortina de transição de rota que envelopa a tela e revela a página destino sem interrupção de frames.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Dashboards de Missão Crítica & Telas Administrativas Densas (SaaS B2B, ERPs, Finanças)**:
  Aplicar botões magnéticos em um painel contendo 50 botões de ação ou tabelas de trading causará exaustão cognitiva imediata. O cursor sendo "puxado" constantemente para botões em uma ferramenta de alta velocidade operacional destrói a precisão analítica do operador.
- **Navegadores Touchscreen e Ambientes Mobile sem Verificação de Ponteiro**:
  Efeitos magnéticos e cursores customizados dependem intrinsecamente das coordenadas `clientX` e `clientY` do mouse. Forçar scripts magnéticos ou cursores virtuais em dispositivos móveis touch causa sobrecarga desnecessária na CPU móvel, quebra o comportamento nativo de toques e introduz latência severa (*tap delay*). Em resoluções móveis (`@media (pointer: coarse)`), estes scripts devem ser terminantemente suspensos via `matchMedia`.
- **Sistemas com Requisitos Rigorosos de Acessibilidade Governamental (WCAG AAA)**:
  Se o site precisar cumprir estritamente critérios de conformidade governamental sem exceções, a rolagem suave por hijacking de scroll (Lenis/Locomotive) e o reposicionamento magnético podem interferir com certas tecnologias assistivas e leitores de tela caso não haja uma chave global de desativação acessível.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "Creative Slop"):
- **Raio de Atração Magnética Desproporcional**:
  Definir um raio magnético de 200px para um botão de 40px. O cursor é "sequestrado" pelo botão quando o usuário está apenas tentando passar o mouse perto dele. O raio de atração ideal nunca deve ultrapassar 40% a 60% do tamanho nominal do próprio elemento.
- **Falta de Amortecimento Diferencial entre Container e Conteúdo Interno**:
  Mover o botão magnético e o texto interno com a mesma velocidade linear cria um efeito robótico barato. A assinatura clássica de Dennis Snellenberg reside na **velocidade diferencial**: o container do botão move-se a um multiplicador (ex: `0.35` do deslocamento do mouse), enquanto o texto interno desloca-se a um multiplicador maior (ex: `0.70`), gerando uma sensação de profundidade e paralaxe física tridimensional dentro do próprio botão.
- **Ignorar a Flag `prefers-reduced-motion`**:
  Forçar transições de cortina SVG velozes e distorções por skew em usuários que declararam sensibilidade a movimento no sistema operacional. É mandatório aplicar `gsap.matchMedia()` e desativar interpolações espaciais quando a media query acusar redução de movimento.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 12 componentes mais emblemáticos do universo Osmo Supply e dos estúdios criativos de Dennis Snellenberg e Ilja van Eck:

### 1. Dennis Snellenberg Magnetic Button (`osmo-magnetic-button`)
- **Anatomia Visual**: Composto por um invólucro magnético (`magnet-wrapper`), o corpo do botão arredondado ou pílula (`magnet-button`) e um container interno para texto e ícone (`magnet-content`). Possui uma camada de preenchimento expansiva (*pill expansion*) com `border-radius: 9999px` que cresce a partir do ponto de entrada do mouse.
- **Gatilho de Interação**: Aproximação do mouse dentro de uma margem invisível de detecção. O container translada suavemente em direção ao mouse com fator amortecido (`x * 0.35, y * 0.35`), enquanto o conteúdo interno translada com maior intensidade (`x * 0.7, y * 0.7`). Ao sair da área, dispara um `gsap.to()` com curva de mola elástica retornando a `(0, 0)`.
- **Onde encaixar**: Botões primários de Call to Action no Hero, botões de contato flutuantes, chaveadores de menu e links de navegação de cabeçalho.

### 2. SVG Morphing Curtain Navigation (`osmo-curtain-menu`)
- **Anatomia Visual**: Uma sobreposição de tela cheia que ocupa a viewport (`fixed inset-0`). O segredo visual está na borda inferior (ou lateral), formada por um SVG contendo um elemento `<path>`. O caminho inicial é uma reta plana fechada; ao abrir, uma timeline do GSAP interpola as coordenadas das curvas de controle Bézier gerando uma barriga curva pronunciada que se estende suavemente antes de esticar até a borda da tela.
- **Gatilho de Interação**: Clique no botão "Menu" (hambúrguer ou magnético). A cortina desce, os itens de menu internos realizam um *staggered roll-up* em cascata, e no fechamento a cortina se retrai com a curva invertida.
- **Onde encaixar**: Menu principal de navegação de sites de agência, portfólios autorais e lookbooks imersivos.

### 3. Lenis + GSAP ScrollTrigger Synchronization Engine (`osmo-scroll-engine`)
- **Anatomia Visual**: Invisível aos olhos, mas imediatamente perceptível na ponta dos dedos. Elimina a parada seca da rolagem com rodinha de mouse tradicional, introduzindo um deslizamento com momentum inercial perfeitamente amortecido que não atrasa a resposta do usuário.
- **Gatilho de Interação**: Rolagem via roda do mouse, trackpad ou teclado. Conecta `lenis.on('scroll', ScrollTrigger.update)` e integra o ciclo do Lenis diretamente no `gsap.ticker.add((time) => lenis.raf(time * 1000))`, garantindo que todas as animações dependentes de scroll sincronizem com precisão de microssegundos.
- **Onde encaixar**: Arquitetura raiz de todo o projeto web (wrapper global do layout).

### 4. Radial Cards Slider (GSAP 3D Arc) (`osmo-radial-slider`)
- **Anatomia Visual**: Coleção de cartões de projeto dispostos não em uma linha horizontal plana convencional, mas ao longo de um arco elíptico tridimensional no plano virtual (`transform: rotateZ(...) translateY(...) rotateX(...)`). Os cards centrais ficam perfeitamente verticais e ampliados, enquanto os cards periféricos curvam-se suavemente para fora da tela.
- **Gatilho de Interação**: Arrastar com mouse/touch (*Draggable*) ou rolagem horizontal com inércia. O GSAP calcula o ângulo contínuo de rotação e interpola a escala e opacidade de cada cartão com base na proximidade do ponto central (vértice do arco).
- **Onde encaixar**: Seções de "Featured Works", galerias de cases de sucesso e mostruários de produtos selecionados.

### 5. Liquid Glass & Stacked Cards Carousel (`osmo-stacked-carousel`)
- **Anatomia Visual**: Conjunto de cartões sobrepostos em camadas de profundidade no eixo Z (`translateZ` e escala decrescente: `scale(1)`, `scale(0.95)`, `scale(0.9)`), com bordas finas com acabamento de vidro translúcido (`backdrop-filter: blur(16px)` e gradiente de borda sutil).
- **Gatilho de Interação**: Clique em botões de avanço, drag horizontal ou swipe. O cartão superior é puxado para fora da tela com leve rotação angulada enquanto a pilha traseira avança simultaneamente para a posição de destaque frontal.
- **Onde encaixar**: Vitrines de depoimentos de clientes premium, cartões de planos de preços alternativos ou seções de apresentação de fundadores.

### 6. Directional Hover Tile Grid (`osmo-directional-grid`)
- **Anatomia Visual**: Grid bento ou editorial onde cada card possui uma camada de overlay (normalmente com contraste invertido ou imagem ampliada). Ao entrar com o mouse no cartão, a camada de overlay desliza para dentro a partir exatamente da borda por onde o cursor entrou (Topo, Baixo, Esquerda ou Direita). Ao sair, ela continua seu curso saindo pela borda onde o cursor escapou.
- **Gatilho de Interação**: Cálculo do ângulo do vetor formado entre o centro do elemento e as coordenadas de entrada do mouse via `Math.atan2(y, x)`. Converte o ângulo em 4 quadrantes cardeais (0: Topo, 1: Direita, 2: Baixo, 3: Esquerda) e dispara a timeline de entrada do GSAP.
- **Onde encaixar**: Grids de galeria de portfólio, catálogos de serviços e vitrines de artigos em blogs de design.

### 7. Dual-Layer Character Roll & Split-Text Kinetics (`osmo-dual-roll`)
- **Anatomia Visual**: Bloco de texto tipográfico onde cada linha ou caractere reside dentro de um elemento pai com `overflow: hidden`. Na posição padrão, a linha visível repousa em `y: 0%`. Uma linha clone idêntica é posicionada em `y: 100%`.
- **Gatilho de Interação**: Hover sobre o link/botão ou gatilho de visualização na tela via ScrollTrigger. A linha superior viaja para `y: -100%` enquanto a inferior sobe para `y: 0%`. Quando acionado via SplitText, as letras sobem sequencialmente com curva cúbica acentuada, criando um efeito de letreiro de cinema tátil.
- **Onde encaixar**: Títulos de projetos no Hero, links de rodapé de alta proeminência e itens de lista de serviços.

### 8. Context-Aware Adaptive Magnetic Cursor (`osmo-adaptive-cursor`)
- **Anatomia Visual**: Cursor duplo formado por um ponto focal central (*dot*) de 6px e uma bolha fluida externa (*bubble*) de 32px a 80px que segue o mouse com atraso elástico (*lerp 0.15*). Quando o cursor passa por áreas específicas, a bolha expande-se instantaneamente, troca de cor e exibe rótulos textuais concisos como "VIEW", "DRAG", "EXPLORE", ou ícones de setas vetoriais rotativas.
- **Gatilho de Interação**: `mousemove` global com detecção de atributos de dados (`data-cursor="drag"`, `data-cursor-text="Play"`). Ao encontrar o alvo, a bolha magnetiza-se ao redor do elemento alvo ou assume o estado de badge flutuante.
- **Onde encaixar**: Elemento global em nível de aplicação para desktop, ativado em galerias horizontais, vídeos e botões de chamada.

### 9. Velocity-Skew Parallax Media Grid (`osmo-velocity-skew`)
- **Anatomia Visual**: Seção vertical de galeria onde cards, fotografias e tipografias sofrem uma inclinação tangencial calculada (`transform: skewY(...)`) proporcional à velocidade com que o usuário rola a página. Quanto mais rápido o scroll, mais os elementos se inclinam (até um teto de segurança de ±5 a ±8 graus), retornando organicamente à posição plana quando o scroll desacelera até o repouso.
- **Gatilho de Interação**: Hook no método `lenis.on('scroll', (e) => { ... })` lendo a propriedade de velocidade instantânea `e.velocity`. O valor é interpolado via `gsap.quickTo` para a propriedade `skewY` dos elementos selecionados.
- **Onde encaixar**: Feed vertical de projetos, seções de listagem de clientes e galerias de imagens editoriais.

### 10. Infinite Seamless Marquee & Ticker (GSAP Horizontal Loop) (`osmo-infinite-ticker`)
- **Anatomia Visual**: Faixa contínua de tipografia display em corpo gigante ou logotipos de clientes parceiros que corre horizontalmente sem jamais revelar emendas ou saltos visuais. 
- **Gatilho de Interação**: Execução em loop perpétuo via helper de código `horizontalLoop()` do GSAP. Ao passar o cursor por cima ou arrastar, o ticker desacelera de maneira elástica, permitindo que o usuário interaja ou inverta o sentido da rolagem com o movimento do mouse.
- **Onde encaixar**: Separadores de seção em landing pages, faixas de Social Proof de clientes notáveis e faixas de rodapé.

### 11. Interactive Dots & Displacement Grid Canvas (`osmo-dots-grid`)
- **Anatomia Visual**: Grade de pontos ou pixels geométricos distribuídos uniformemente em um elemento `<canvas>` ou SVG leve como plano de fundo. Em repouso, os pontos são estáticos com baixa opacidade.
- **Gatilho de Interação**: Movimento do ponteiro do mouse. O script calcula a distância euclidiana entre cada ponto da malha e as coordenadas do cursor. Pontos dentro de um raio de 120px são repelidos vetorialmente e aumentam de tamanho e brilho, criando uma onda de deformação elástica que se dissipa quando o cursor se afasta.
- **Onde encaixar**: Fundo da seção Hero de produtos tecnológicos, cabeçalho de contato ou áreas de transição entre seções escuras.

### 12. Barba.js + GSAP Multi-Stage Page Transition Orchestrator (`osmo-page-orchestrator`)
- **Anatomia Visual**: Arquitetura de transição entre rotas que elimina o recarregamento tradicional do navegador. Apresenta diferentes tipos de máscara de saída: cortina em bloco ascendente, múltiplos blocos escalonados (*staggered columns*) ou zoom espacial da imagem clicada em direção ao Hero da página de destino.
- **Gatilho de Interação**: Clique em qualquer link interno com atributo `data-barba-link`. O Barba.js intercepta a requisição HTTP via fetch, o GSAP executa a timeline de saída (`leave`), substitui o container de conteúdo no DOM e dispara a timeline de entrada (`enter`).
- **Onde encaixar**: Infraestrutura de arquitetura global em websites multipágina (MPA ou Next.js com páginas desacopladas).

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

Para integrar os padrões e a física do ecossistema Osmo Supply em um projeto contemporâneo (Next.js App Router / React + Tailwind CSS), instale os pacotes fundamentais:

```bash
npm install gsap @studio-freight/lenis lucide-react clsx tailwind-merge
```

Plugins essenciais do GSAP utilizados:
- `ScrollTrigger`: Controle de animações amarradas ao scroll.
- `CustomEase`: Para curvas de aceleração com assinatura milimétrica.
- `Draggable` & `InertiaPlugin`: Para carrosséis e sliders táteis com momento físico.

---

### Física de Movimento, Curvas de Bézier & Parâmetros

A identidade visual de Dennis Snellenberg e Ilja van Eck apoia-se em curvas de aceleração específicas, caracterizadas por uma saída com aceleração controlada e uma chegada extremamente longa e suave, evitando movimentos mecânicos ou secos:

```javascript
// A curva de assinatura de Dennis Snellenberg e do Osmo Supply:
// Equivalente em CSS: cubic-bezier(0.76, 0, 0.24, 1)
// Em GSAP CustomEase:
CustomEase.create("osmoEase", "M0,0 C0.76,0 0.24,1 1,1");

// Curva para cortinas SVG e expansões de menu de alta amplitude:
// Equivalente em CSS: cubic-bezier(0.85, 0, 0.15, 1)
CustomEase.create("osmoCurtain", "M0,0 C0.85,0 0.15,1 1,1");

// Curva de retorno de mola amortecida para botões magnéticos:
// Easing exponencial com retorno orgânico sem overshoot excessivo:
const magnetEase = "power4.out"; // Duração: 0.8s a 1.0s
```

#### Parâmetros de Interpolação Vetorial:
- **Botão Magnético — Deslocamento do Container**: `x * 0.35`, `y * 0.35`
- **Botão Magnético — Deslocamento do Texto Interno**: `x * 0.70`, `y * 0.70`
- **Cursor — Interpolação Linear (Lerp)**: `0.12` a `0.18` (tempo de resposta tátil entre 80ms e 120ms)
- **Teto Máximo de Distorção por Skew**: `Math.min(Math.max(velocity * 0.08, -7), 7)` graus

---

### Receita de Código 1: O Botão Magnético de Dennis Snellenberg com Duplo Rolo de Texto & Fundo Expansivo (React + GSAP `quickTo`)

Este componente implementa a técnica de máxima performance utilizando `gsap.quickTo` (evitando recriar tweens a cada evento `mousemove` a 120Hz):

```tsx
"use client";

import React, { useRef, useEffect } from "react";
import gsap from "gsap";

interface OsmoMagneticButtonProps {
  children: string;
  onClick?: () => void;
  className?: string;
  magneticStrength?: number;
}

export function OsmoMagneticButton({
  children,
  onClick,
  className = "",
  magneticStrength = 0.35,
}: OsmoMagneticButtonProps) {
  const buttonRef = useRef<HTMLButtonElement>(null);
  const textRef = useRef<HTMLDivElement>(null);
  const fillRef = useRef<HTMLSpanElement>(null);

  useEffect(() => {
    const btn = buttonRef.current;
    const text = textRef.current;
    const fill = fillRef.current;
    if (!btn || !text || !fill) return;

    // quickTo para movimentação ultra fluida a 60-120fps sem sobrecarga de memória
    const xTo = gsap.quickTo(btn, "x", { duration: 0.8, ease: "power3.out" });
    const yTo = gsap.quickTo(btn, "y", { duration: 0.8, ease: "power3.out" });

    const textXTo = gsap.quickTo(text, "x", { duration: 0.8, ease: "power3.out" });
    const textYTo = gsap.quickTo(text, "y", { duration: 0.8, ease: "power3.out" });

    const handleMouseMove = (e: MouseEvent) => {
      const rect = btn.getBoundingClientRect();
      const centerX = rect.left + rect.width / 2;
      const centerY = rect.top + rect.height / 2;

      const deltaX = e.clientX - centerX;
      const deltaY = e.clientY - centerY;

      // O container move com amortecimento
      xTo(deltaX * magneticStrength);
      yTo(deltaY * magneticStrength);

      // O texto move com maior intensidade criando profundidade de paralaxe
      textXTo(deltaX * (magneticStrength * 1.8));
      textYTo(deltaY * (magneticStrength * 1.8));
    };

    const handleMouseEnter = (e: MouseEvent) => {
      const rect = btn.getBoundingClientRect();
      const relX = e.clientX - rect.left;
      const relY = e.clientY - rect.top;

      // Posiciona a cápsula de preenchimento onde o mouse entrou e expande
      gsap.set(fill, { left: relX, top: relY, scale: 0, opacity: 1 });
      gsap.to(fill, {
        scale: 3.5,
        duration: 0.6,
        ease: "power2.out",
      });
    };

    const handleMouseLeave = (e: MouseEvent) => {
      const rect = btn.getBoundingClientRect();
      const relX = e.clientX - rect.left;
      const relY = e.clientY - rect.top;

      // Retorno do botão e do texto com amortecimento elástico
      xTo(0);
      yTo(0);
      textXTo(0);
      textYTo(0);

      // A cápsula de preenchimento recolhe em direção ao ponto de saída
      gsap.to(fill, {
        left: relX,
        top: relY,
        scale: 0,
        opacity: 0,
        duration: 0.5,
        ease: "power2.in",
      });
    };

    btn.addEventListener("mousemove", handleMouseMove);
    btn.addEventListener("mouseenter", handleMouseEnter);
    btn.addEventListener("mouseleave", handleMouseLeave);

    return () => {
      btn.removeEventListener("mousemove", handleMouseMove);
      btn.removeEventListener("mouseenter", handleMouseEnter);
      btn.removeEventListener("mouseleave", handleMouseLeave);
    };
  }, [magneticStrength]);

  return (
    <button
      ref={buttonRef}
      onClick={onClick}
      className={`group relative inline-flex items-center justify-center overflow-hidden rounded-full border border-zinc-800 bg-zinc-950 px-8 py-4 text-sm font-medium tracking-wide text-zinc-100 transition-colors duration-300 hover:border-zinc-700 ${className}`}
      style={{ willChange: "transform" }}
    >
      {/* Camada expansiva de preenchimento elástico */}
      <span
        ref={fillRef}
        className="pointer-events-none absolute h-24 w-24 -translate-x-1/2 -translate-y-1/2 rounded-full bg-white opacity-0"
        style={{ willChange: "transform, left, top" }}
      />

      {/* Rótulo tipográfico com efeito Dual-Roll */}
      <div
        ref={textRef}
        className="pointer-events-none relative z-10 flex h-5 overflow-hidden text-center"
        style={{ willChange: "transform" }}
      >
        <div className="flex flex-col transition-transform duration-500 ease-[cubic-bezier(0.76,0,0.24,1)] group-hover:-translate-y-1/2">
          {/* Texto em repouso (cinza claro) */}
          <span className="flex h-5 items-center justify-center text-zinc-200 group-hover:text-black">
            {children}
          </span>
          {/* Texto duplicado que sobe no hover (preto sobre o fundo branco que expande) */}
          <span className="flex h-5 items-center justify-center font-semibold text-black">
            {children}
          </span>
        </div>
      </div>
    </button>
  );
}
```

---

### Receita de Código 2: Inicialização Global de Lenis + GSAP ScrollTrigger

Para orquestrar todo o ritmo de rolagem da aplicação sem conflitos de frame:

```tsx
"use client";

import { useEffect } from "react";
import Lenis from "@studio-freight/lenis";
import gsap from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

export function OsmoScrollProvider({ children }: { children: React.ReactNode }) {
  useEffect(() => {
    gsap.registerPlugin(ScrollTrigger);

    // Inicializa o motor de momentum scroll
    const lenis = new Lenis({
      duration: 1.2,
      easing: (t) => Math.min(1, 1.001 - Math.pow(2, -10 * t)), // Curva exponencial suave
      orientation: "vertical",
      gestureOrientation: "vertical",
      smoothWheel: true,
      wheelMultiplier: 1.0,
      touchMultiplier: 2.0,
      infinite: false,
    });

    // Sincroniza o ScrollTrigger do GSAP com as atualizações de scroll do Lenis
    lenis.on("scroll", ScrollTrigger.update);

    // Acopla o ticker de renderização do GSAP ao loop do Lenis
    const updateTicker = (time: number) => {
      lenis.raf(time * 1000);
    };

    gsap.ticker.add(updateTicker);
    gsap.ticker.lagSmoothing(0); // Evita pulo de frames ao alternar abas

    return () => {
      gsap.ticker.remove(updateTicker);
      lenis.destroy();
      ScrollTrigger.getAll().forEach((trigger) => trigger.kill());
    };
  }, []);

  return <>{children}</>;
}
```

---

### Receita de Código 3: Transição de Cortina SVG com Curva de Bézier Dinâmica (`SVG Path Morphing`)

A lógica fundamental por trás das cortinas de menu de Dennis Snellenberg e Ilja van Eck:

```tsx
"use client";

import React, { useRef, useState } from "react";
import gsap from "gsap";

export function OsmoCurvedCurtainMenu() {
  const [isOpen, setIsOpen] = useState(false);
  const pathRef = useRef<SVGPathElement>(null);
  const containerRef = useRef<HTMLDivElement>(null);

  // Definições de coordenadas vetoriais SVG da cortina:
  // Inicial: reta no topo (fora da tela)
  const initialPath = "M 0 0 V 0 Q 50 0 100 0 V 0 Z";
  // Intermediário: curva pronunciada descendo (efeito gota líquida elástica)
  const targetCurve = "M 0 0 V 100 Q 50 140 100 100 V 0 Z";
  // Final: tela cheia perfeitamente plana
  const finalFlat = "M 0 0 V 100 Q 50 100 100 100 V 0 Z";

  const toggleMenu = () => {
    const path = pathRef.current;
    const container = containerRef.current;
    if (!path || !container) return;

    if (!isOpen) {
      setIsOpen(true);
      container.style.pointerEvents = "auto";

      const tl = gsap.timeline();
      tl.set(container, { display: "block" })
        .set(path, { attr: { d: initialPath } })
        .to(path, {
          attr: { d: targetCurve },
          duration: 0.6,
          ease: "power3.in",
        })
        .to(path, {
          attr: { d: finalFlat },
          duration: 0.4,
          ease: "power2.out",
        });
    } else {
      setIsOpen(false);
      container.style.pointerEvents = "none";

      const tl = gsap.timeline();
      tl.to(path, {
        attr: { d: "M 0 0 V 0 Q 50 40 100 0 V 0 Z" },
        duration: 0.5,
        ease: "power3.in",
      })
        .set(container, { display: "none" })
        .set(path, { attr: { d: initialPath } });
    }
  };

  return (
    <>
      <button
        onClick={toggleMenu}
        className="fixed right-8 top-8 z-50 rounded-full bg-white px-6 py-3 text-xs font-bold uppercase tracking-widest text-black"
      >
        {isOpen ? "Close" : "Menu"}
      </button>

      <div
        ref={containerRef}
        className="fixed inset-0 z-40 hidden h-screen w-screen overflow-hidden"
        style={{ pointerEvents: "none" }}
      >
        {/* SVG em viewBox 100x100 para coordenadas percentuais universais */}
        <svg
          className="absolute inset-0 h-full w-full fill-zinc-950"
          viewBox="0 0 100 100"
          preserveAspectRatio="none"
        >
          <path ref={pathRef} d={initialPath} />
        </svg>

        {/* Conteúdo interno do Menu revelado após a cortina cobrir a tela */}
        <div
          className={`relative z-10 flex h-full w-full flex-col items-center justify-center transition-opacity duration-300 ${
            isOpen ? "opacity-100 delay-300" : "opacity-0"
          }`}
        >
          <nav className="flex flex-col space-y-6 text-center text-4xl font-light text-white md:text-6xl">
            <a href="#work" className="hover:text-zinc-400">Work</a>
            <a href="#about" className="hover:text-zinc-400">About</a>
            <a href="#contact" className="hover:text-zinc-400">Contact</a>
          </nav>
        </div>
      </div>
    </>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma interface que incorpore a linguagem técnica e estética do **Osmo Supply**, inclua obrigatoriamente as seguintes diretrizes de arquitetura no documento `DESIGN_BLUEPRINT.md`:

### 1. Declaração do Motor de Física e Movimento
- **Engine Primária**: `GSAP 3` com registro obrigatório de `ScrollTrigger` e `CustomEase`.
- **Motor de Rolagem Inercial**: `@studio-freight/lenis` rodando dentro do `gsap.ticker` global para evitar dessincronização de frames em telas de alta taxa de atualização (ProMotion 120Hz).
- **Curva Mestra de Animação**: Declarar `cubic-bezier(0.76, 0, 0.24, 1)` como a variável token `--ease-osmo-signature` no Tailwind e CSS tokens.

### 2. Hierarquia de Interação (Regra 60-30-10)
- **60% (Fundação Estática)**: Tipografia neutra com hierarquia impecável (ex: *PP Neue Montreal* ou *Geist Sans*), espaçamentos amplos (`gap-12`, `p-16` a `p-24`), paleta escura profunda (`#0e0e0e`) com bordas em alfa translúcido (`border-white/10`).
- **30% (Fluidez Contínua)**: Lenis smooth scroll ativo, botões secundários com rotação tipográfica Dual-Roll de 2 camadas, e cursor adaptativo seguindo o mouse com *lerp* suave.
- **10% (Showstoppers Centrais)**: Apenas 1 a 2 componentes complexos do Osmo por página (ex: Botão Magnético no Hero principal + Cortina SVG no Menu de navegação; ou Slider Radial na seção de Projetos). **Nunca** acumular mais de 3 showstoppers na mesma seção.

### 3. Regras de Otimização e Fallback (Performance & Acessibilidade)
- **Desativação Touchscreen Obrigatória**:
  ```javascript
  const isTouchDevice = window.matchMedia("(pointer: coarse)").matches;
  if (isTouchDevice) {
    // Desativar botões magnéticos e cursores virtuais;
    // Recorrer a botões regulares e cursor de sistema nativo.
  }
  ```
- **Respeito ao Modo Reduzido de Movimento**:
  ```javascript
  const prefersReduced = window.matchMedia("(prefers-reduced-motion: reduce)").matches;
  if (prefersReduced) {
    // Desativar Lenis e transições com morph de SVG;
    // Utilizar rolagem nativa e fades de opacidade pura com duração máxima de 0.2s.
  }
  ```
- **Gerenciamento de Memória**: Todos os ouvintes de evento `mousemove` devem ser desacoplados através de `gsap.quickTo` ou requestAnimationFrame com limpeza explícita no unmount do React (`return () => { ... }`) para prevenir vazamentos de memória (memory leaks).
