---
id: "motion-ui"
name: "Motion UI"
url: "https://motion.dev/ui/"
category: "3-motion"
schema_type: "B-motion-shaders"
dna_estetico: ["Hardware-Accelerated Physics", "Headless Kinetic Primitives", "Progressive Curtains & Spatial Reveals", "Subtle Magnetic & Tactile Feedback", "Intelligent Typography Morphing"]
densidade_informacao: "Media"
impacto_visual: "Moderado a Cinematografico/Showstopper"
custo_computacional: "Medio (WAAPI + React RAF Spring Engine + Layout Projections)"
stack_frameworks: ["React 19 / React 18", "Vue 3", "Vanilla JS / TypeScript", "Tailwind CSS (v3 / v4)", "Motion (v12 / motion-plus)"]
compatibilidade:
  combinacoes_recomendadas: ["Motion + Shadcn UI", "Next.js App Router (Curtains + Suspense)", "Tailwind CSS v4 + Motion UI", "Lenis Smooth Scroll + Motion Gallery", "Radix UI + Motion Cursor Magnetic"]
  conflitos_esteticos: ["CSS Transitions lineares puras desincronizadas", "Animações caóticas sem hierarquia física", "Overkill de cursores customizados em telas mobile de toque", "Marquees pesadas com dezenas de nós DOM clonados (resolvido pelo algoritmo minimal-clone do Ticker)"]
---

# Motion UI — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)

Desenvolvido pela equipe oficial do **Motion** (anteriormente *Framer Motion* e *Popmotion*), liderada pelo pioneiro da engenharia de animação web **Matt Perry**, o **Motion UI** (`motion.dev/ui` / ecossistema *Motion+*) representa o ápice da maturidade de interfaces animadas no ecossistema moderno de React, Vue e JavaScript puro.

Ao contrário de bibliotecas de componentes tradicionais que entregam componentes pesados e estilisticamente engessados, o Motion UI é estruturado como uma suíte de **primitivas headless de alta engenharia cinemática**. Cada componente resolve problemas físicos e matemáticos notoriamente complexos de implementar do zero — como rotações tridimensionais no espaço do DOM, cursores magnéticos que se adaptam contextualmente a caixas de texto e botões, carrosséis com inércia real de arrasto, marquees contínuos com algoritmo de clonagem mínima e transições completas de rota estilo cortina de palco (*Curtains*).

### Os Pilares da Sensação Física (Feel) do Motion UI:

1. **Dualidade WAAPI & Solver de Molas em Tempo Real**:
   O núcleo de movimento do Motion UI aproveita ao máximo a **Web Animations API (WAAPI)** nativa do navegador para animações baseadas em tempo (transforms, opacidades e offsets), garantindo execução fora da thread principal do JavaScript (na compositor thread da GPU a 60/120fps). Quando a interação humana exige interrupção, inércia dinâmica ou rastreamento contínuo de ponteiro (como no `<Cursor>` e no `<Carousel>`), o motor alterna cirurgicamente para um **solver analítico de molas amortecidas** em `requestAnimationFrame`, preservando momento linear e velocidade angular sem saltos visuais (*zero glitch / zero layout thrashing*).

2. **Continuidade de Estado com `useCurtains` (Anti-White Flash)**:
   A maior quebra de imersão na web contemporânea reside na transição de rotas em Single Page Applications (SPAs) e no Next.js App Router: uma rota é disparada, ocorrem fetches assíncronos e o navegador frequentemente exibe layouts vazios, spinners isolados ou repinturas parciais desincronizadas. A primitiva `useCurtains` estabelece o conceito de **transição em cortina opaca garantida**:
   - A cortina visual (com efeitos geométricos como `wipe`, `iris`, `pixels`, `doors` ou `blinds`) cobre o viewport;
   - A comutação de estado do React e a resolução do React Server Component / Suspense ocorrem no escuro;
   - O Motion segura o início da animação de abertura (*reveal*) até que o React confirme o commit completo da árvore do DOM e o navegador realize o *paint* do novo layout. O usuário nunca testemunha telas inacabadas.

3. **Cadência Orgânica Humana vs. Automação Robótica**:
   No componente `<Typewriter>`, Perry eliminou o clássico `setInterval` mecânico de velocidade fixa. O motor calcula atrasos com variações estocásticas em torno de uma curva gaussiana (simulando a cadência natural dos dedos em um teclado físico) e injeta pausas reflexivas ampliadas sempre que o caractere analisado é um sinal de pontuação (`.`, `,`, `!`, `?`, `;`). No `<ScrambleText>`, a decodificação de strings emula sistemas criptográficos de alta tecnologia via loops de perturbação e resolução progressiva por direção configurável (`left-to-right`, `outside-in` ou `random`).

4. **Algoritmo de Clonagem Mínima para Marquees (`<Ticker>`)**:
   Bibliotecas de marquee comuns sobrecarregam o DOM criando dezenas de cópias estáticas de elementos pesados para preencher telas ultra-wide. O `<Ticker>` do Motion UI executa um cálculo geométrico em tempo de execução: mede a largura do container e do elemento-filho via `ResizeObserver` e gera estritamente a quantidade mínima fracionária de nós virtuais necessária para fechar o ciclo de loop contínuo (`Math.ceil(viewport / itemWidth) + 1`), mantendo a árvore DOM leve e a bateria do dispositivo preservada.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários

1. **SaaS B2B Premium, DevTools & AI Interfaces (Estilo Linear, Stripe, Raycast, Vercel)**:
   - Contadores de créditos, taxas de API, latência em milissegundos e métricas financeiras usando `<AnimateNumber>`. A animação de rolagem vertical dos dígitos individuais com suporte a `Intl.NumberFormat` confere precisão de instrumento cirúrgico à interface.
   - Decodificação de prompts e geração de respostas de modelos de linguagem (LLMs) via `<ScrambleText>` e `<Typewriter>`, fornecendo feedback visual de alta tecnologia enquanto tokens de streaming chegam à tela.
2. **Showcases de Hardware, Estúdios de Arquitetura & Portfólios Criativos**:
   - O `<Gallery>` com arranjos espaciais tridimensionais (`barrel`, `sphere`, `coverflow`, `helix`) transforma listas de projetos em instalações visuais imersivas que reagem à velocidade do mouse ou do touch.
   - O `<Cursor>` magnético permite que o ponteiro do mouse "salte" suavemente para botões primários, sliders e cartões de projeto, aumentando o feedback háptico percebido.
3. **Plataformas de E-Commerce de Luxo & Lookbooks Interativos**:
   - O `<Carousel>` headless permite criar carrosséis de produtos totalmente acessíveis por teclado, suporte a gestos de arrasto touch e física de retorno (elastic snapback) em bordas de lista.
4. **Landing Pages de Produtos Flagship com Navegação Cinematográfica**:
   - Alternância entre capítulos de narrativa visual usando `useCurtains`, criando wipes e aberturas de íris diagonais sincronizadas com trocas de tema Dark/Light.

### Papel no Ritmo Visual (Regra 60-30-10)

- **60% — Fundação Estática & Estrutural (Tokens Neutros)**:
  Tipografia estática clara (Geist, Inter, SF Pro), layout grid com Tailwind CSS, superfícies neutras de alta densidade (`bg-zinc-950`, bordas `border-zinc-800/60`). Nenhuma animação gratuita concorre com a legibilidade da informação.
- **30% — Fluidez Funcional Invisível (Feel de Usabilidade)**:
  As primitivas sutis do Motion UI: `<AnimateNumber>` ao filtrar tabelas ou atualizar dashboards de preços; `<Carousel>` respondendo com amortecimento crítico ao arrasto; `<Ticker>` girando com velocidade constante de 40px/s na seção de logos parceiros; `<Cursor>` ajustando suavemente seu raio ao passar sobre links e inputs de texto.
- **10% — Espetáculo Visual (Showstopper / Destaque de Marca)**:
  Momentos cinematográficos controlados: transição de rota com `useCurtains` disparando um `wipe` geométrico de 12 graus; abertura do catálogo 3D com `<Gallery arrange={barrel()}>` no Hero da landing page; ou o reveal decodificado do título principal via `<ScrambleText>`.

---

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)

### ⚠️ Quando Evitar (Anti-Padrões de Movimento)

1. **Uso de `<Cursor>` em Dispositivos Touch ou Telas Híbridas**:
   - É terminantemente proibido renderizar cursores customizados para usuários em smartphones ou tablets. Além de desnecessário, causa latência e inconsistências de ponteiro. O `<Cursor>` deve ser condicionado por media queries CSS `@media (hover: hover) and (pointer: fine)`.
2. **Marquees em Alta Velocidade (`velocity > 120`) em Ambientes de Alta Densidade de Leitura**:
   - O `<Ticker>` nunca deve conter textos de suporte, tabelas de dados ou links de documentação crítica se o movimento for contínuo, pois provoca fadiga ocular e impede a leitura atenta. Marquees devem ser restritos a logos monocromáticos, cotações resumidas ou tags decorativas.
3. **Curtains em Fluxos Transacionais e Checkouts Críticos**:
   - Não utilize efeitos de cortina (`wipe`, `iris`, `blinds`) em etapas onde o usuário precisa de resposta em milissegundos, como em carrinhos de compras, caixas de diálogo modais ou formulários de autenticação. Nesses pontos, a velocidade de fechamento deve ser instantânea ou com fade simples de 150ms.
4. **Empilhamento Concorrente de Múltiplos Textos Animados**:
   - Jamais combine `<Typewriter>`, `<ScrambleText>` e `splitText` na mesma dobra de visualização. O cérebro humano não consegue fixar múltiplos pontos de mutação tipográfica simultâneos.

### ⚠️ Regras de Acessibilidade & GPU

1. **Respeito Estrito a `prefers-reduced-motion`**:
   - O Motion UI possui integração direta com acessibilidade do sistema operacional. Quando o usuário ativa redução de movimento:
     - O `<Cursor>` deve voltar imediatamente ao ponteiro padrão do sistema;
     - O `<Ticker>` deve pausar automaticamente ou exibir uma lista com rolagem estática nativa;
     - O `useCurtains` deve ignorar wipes complexos e executar um fade simples ou corte direto sem animação;
     - O `<Typewriter>` deve renderizar a string completa instantaneamente, sem digitação gradual.
2. **Isolamento de Pintura e `will-change` Dinâmico**:
   - O Motion UI gerencia dinamicamente `will-change: transform` durante o ciclo de arrasto e transição, liberando a memória de textura da GPU assim que o componente entra em repouso. O desenvolvedor deve evitar aplicar classes globais de `will-change-transform` que consumam VRAM permanentemente no mobile.
3. **Leitores de Tela (`aria-live` e Árvore de Acessibilidade)**:
   - Textos decorativos animados (`ScrambleText` e `Typewriter`) devem sempre manter um elemento de texto acessível via `aria-label` ou `sr-only`, marcando a representação mutável com `aria-hidden="true"`, evitando que leitores de tela vocalizem sequências ininteligíveis de caracteres criptografados ou soletração letra a letra a cada frame.

---

## 4. Catálogo de Efeitos, Primitivas e Padrões de Animação

### 1. `<AnimateNumber>` — Odômetro Numérico Fluido & Contador de Precisão
- **Anatomia & Arquitetura**: Primitiva ultra-leve (apenas 2.5kb sobre o core do Motion). Decompõe internamente qualquer número em quatro nós semânticos estilizados: `.prefix`, `.integer`, `.fraction` e `.suffix`.
- **Comportamento Visual**: Ao sofrer alteração em seu `value` (ex: de 1.450 para 2.890), cada dígito rola individualmente em seu eixo Y vertical simulando um odômetro de precisão mecânica, enquanto o espaçamento horizontal e largura do container se adaptam via projeção de layout (`layoutId` contínuo).
- **Gatilho**: Alteração do valor numérico passado como filho no estado do React.
- **Suporte Internacional**: Totalmente integrado com a API nativa `Intl.NumberFormat`, suportando moedas (`USD`, `EUR`, `BRL`), porcentagens e notação compacta (`compactDisplay: "short"` convertendo 1.250.000 em 1.25M de forma animada).

### 2. `<Cursor>` — Ponteiro Magnético, Contextual & Adaptativo
- **Anatomia & Arquitetura**: Componente inteligente que substitui o cursor nativo (`mode="replace"`) ou adiciona uma cauda cinemática acompanhadora (`mode="follow"`).
- **Comportamento Visual**:
  - *Estado Livre*: Flutua suavemente com amortecimento elástico acompanhando as coordenadas da GPU (`x`, `y`).
  - *Estado Magnético (Magnetic Snap)*: Ao se aproximar de um botão ou link marcado com atributos de destino, o cursor sofre atração vetorial magnética, expande suas bordas para englobar a geometria exata do elemento e alinha o ponto central ao elemento clicável.
  - *Estado Textual*: Transforma-se em um traço vertical estilizado ao pairar sobre áreas de texto editável ou código.
- **Gatilho**: `pointermove`, `pointerenter`, `pointerleave`, `pointerdown`.

### 3. `<Carousel>` — Sliders de Produção Headless com Inércia Real
- **Anatomia & Arquitetura**: Carrossel headless com suporte a múltiplos eixos (`axis="x" | "y"`), loop contínuo infinito, alinhamentos (`align="start" | "center" | "end"`) e controle de overflow.
- **Comportamento Visual**: O movimento combina arrasto por ponteiro (`drag`), rolagem inercial de trackpad (`wheel`) e controle por teclado com transições de mola de alta fidelidade. Possui algoritmos embutidos para layouts tipo *Coverflow* (rotação angular em 3D dos cards adjacentes e redução de escala e opacidade lateral).
- **Gatilho**: Gestos de arrasto, eventos de roda de mouse, cliques em controles de paginação e teclas de navegação (`ArrowLeft` / `ArrowRight`).

### 4. `<Ticker>` — Marquee Infinito com Algoritmo de Clonagem Mínima
- **Anatomia & Arquitetura**: Componente de 2.1kb projetado para criar fitas infinitas de logotipos, notícias ou frases. Diferente de implementações ingênuas de CSS que clonam 20 vezes o conteúdo, o `<Ticker>` calcula a fração exata de nós necessária para cobrir a largura da tela + margem de buffer.
- **Comportamento Visual**: Movimento contínuo hiper-fluido a 60/120fps sem tremor de sub-pixels. Permite aceleração e desaceleração dinâmica em resposta ao hover do usuário, arrasto interativo e reversão de direção (`direction="rtl" | "ltr"`).
- **Gatilho**: Loop temporal em RAF contínuo, scroll progress do viewport ou interatividade por drag.

### 5. `useCurtains` — Transições de Página em Cortina Cinematográfica
- **Anatomia & Arquitetura**: Hook especializado em React (`motion-plus/react` e `motion-plus/curtains`) que implementa transições de rota e comutações de estado de alta escala.
- **Efeitos Disponíveis**:
  - `wipe`: Varredura direcional sólida com suporte a ângulo (`angle: 12`, `direction: "left" | "right" | "up" | "down"`);
  - `clipWipe`: Varredura baseada em `clip-path` poligonal;
  - `iris`: Expansão circular ou elíptica a partir do centro da tela ou do elemento de clique;
  - `doors`: Portas duplas que se fecham a partir das extremidades laterais;
  - `pixels`: Dissolução quadriculada estilizada em blocos digitais de pixel art;
  - `blinds`: Cortina estilo veneziana com persianas horizontais ou verticais giratórias;
  - `shutter`: Fechamento estilo obturador mecânico de câmera fotográfica;
  - `staggerWipe`: Várias lâminas de cor sobrepostas deslizando com atraso sequencial.
- **Gatilho**: Navegação de rota assíncrona (`router.push()`) ou troca de estado de página.

### 6. `<Typewriter>` — Máquina de Escrever com Cadência e Pausas Humanas
- **Anatomia & Arquitetura**: Primitiva de apenas 1.3kb voltada para tipografia cinética expressiva.
- **Comportamento Visual**: Renderiza o texto caractere a caractere aplicando variações aleatórias na velocidade da digitação, evitando o aspecto mecânico artificial. Reconhece vírgulas e pontos finais para introduzir pausas de reflexão. Possui lógica integrada de backspace (`backspace="word" | "character"`), permitindo apagar e reescrever frases alternativas dinamicamente.
- **Gatilho**: Montagem do componente ou transição de frases em um array de strings.

### 7. `<ScrambleText>` — Decodificador Criptográfico Cyberpunk / Terminal
- **Anatomia & Arquitetura**: Componente para animação de decodificação estilo matriz/ficção científica.
- **Comportamento Visual**: O texto original inicia como uma sequência de glifos caóticos (alfanuméricos, binários, caracteres especiais ou conjunto customizado pelo desenvolvedor). Através de funções de `stagger` do Motion, os caracteres vão se estabilizando na palavra final de acordo com a direção configurada (`left-to-right`, `outside-in`, `random`).
- **Gatilho**: Entrada em viewport (`inView`), hover ou disparo manual por trigger de estado.

### 8. `splitText()` — Decomposição Tipográfica Atômica de Alta Performance
- **Anatomia & Arquitetura**: Função utilitária avançada da biblioteca que analisa elementos de texto no DOM e os divide em nós span individuais para caracteres (`chars`), palavras (`words`) e linhas (`lines`), preservando espaços em branco e acessibilidade.
- **Comportamento Visual**: Habilita animações de entrada estagiadas (`stagger(0.03)`), efeitos de queda por gravidade, revelações em máscara por linha (`overflow-hidden`) e interação de hover individual em palavras.
- **Gatilho**: Execução no ciclo de vida de animação via `animate()` ou diretivas de scroll.

### 9. `<Gallery>` — Instalações 3D Espaciais de Mídia
- **Anatomia & Arquitetura**: Componente para galerias de imagens e vídeos que projeta itens em arranjos tridimensionais no espaço visual usando coordenadas de perspectiva CSS:
  - `barrel()`: Projeção cilíndrica horizontal onde os itens curvam-se em torno do espectador;
  - `sphere()`: Esfera geodésica flutuante navegável por rotação em 360 graus;
  - `helix()`: Espiral helicoidal que se estende verticalmente na profundidade do eixo Z;
  - `ring()`: Anel circular fechado;
  - `coverflow()`: Estilo clássico de navegação de álbuns com cards inclinados a 45 graus;
  - `stack()`: Pilha elástica de cartões com descarte por arrasto gestual.
- **Gatilho**: Arrastar com mouse/touch, rotação com inércia, clique para expandir em modal fullscreen.

### 10. `Interactive Bento Grids` — Grids Modulares com Efeito Proximidade
- **Anatomia & Arquitetura**: Padrão de layout em seções de marketing do Motion UI onde múltiplos blocos modulares interagem com a posição global do ponteiro.
- **Comportamento Visual**: Feixes de luz radial acompanham a posição do cursor através de bordas translúcidas de cartões contíguos (`radial-gradient`), enquanto o cartão em foco sofre sutil inclinação 3D elástica (*spring-bound tilt*) baseada na velocidade do mouse.

---

## 5. Matemática do Movimento & Receitas de Código

### Parâmetros Físicos & Curvas Exatas do Motion UI

#### Curvas Bézier Cúbicas de Alta Precisão (WAAPI & Tweens)
```css
/* Snappy Quartz / Fast Out, Slow In — Para modais, reveals e trocas de aba */
--ease-motion-snappy: cubic-bezier(0.16, 1, 0.3, 1);

/* Soft Deceleration — Para desaceleração de carrosséis e cursores de apoio */
--ease-motion-soft: cubic-bezier(0.25, 1, 0.5, 1);

/* Anticipation / Dramatic Acceleration — Para saídas e fechamento de cortinas */
--ease-motion-exit: cubic-bezier(0.7, 0, 0.84, 0);
```

#### Fórmulas de Mola do Motion (Spring Physics Tokens)
A API moderna do Motion utiliza parâmetros orientados tanto pela física clássica (`stiffness`, `damping`, `mass`) quanto pela API de percepção visual (`visualDuration`, `bounce`):

1. **Microinteração Instantânea (AnimateNumber & Toggles)**:
   ```ts
   const snappySpring = {
     type: "spring",
     visualDuration: 0.35,
     bounce: 0.15,
     restDelta: 0.001
   };
   // Equivalente físico: stiffness: 400, damping: 28, mass: 0.8
   ```

2. **Inércia Suave de Superfície (Carousel & Follow Cursor)**:
   ```ts
   const inertialSpring = {
     type: "spring",
     stiffness: 180,
     damping: 24,
     mass: 1.0,
     restDelta: 0.005
   };
   ```

3. **Snap Magnético do Cursor (Tactile Elastic Snap)**:
   ```ts
   const magneticSpring = {
     type: "spring",
     stiffness: 320,
     damping: 22,
     mass: 0.5
   };
   ```

---

### Boilerplate Completo: Dashboard & Showcase Integrando Primitivas Motion UI

O exemplo a seguir demonstra a implementação prática de uma interface de alto nível utilizando **React 19 / TypeScript**, **Tailwind CSS v4** e as primitivas oficiais do ecossistema **Motion+ / Motion UI**:

```tsx
"use client";

import React, { useState, useEffect } from "react";
import { 
  AnimateNumber, 
  Cursor, 
  Carousel, 
  Ticker, 
  Typewriter, 
  ScrambleText 
} from "motion-plus/react";
import { useCurtains } from "motion-plus/react";
import { wipe, iris } from "motion-plus/curtains";
import { motion, AnimatePresence } from "motion/react";

// ==========================================
// DADOS DE DEMONSTRAÇÃO
// ==========================================
const PARTNER_LOGOS = [
  { id: 1, name: "Vercel", symbol: "▲ Vercel" },
  { id: 2, name: "Linear", symbol: "◈ Linear" },
  { id: 3, name: "Stripe", symbol: "/// Stripe" },
  { id: 4, name: "Raycast", symbol: "⬡ Raycast" },
  { id: 5, name: "Supabase", symbol: "⚡ Supabase" },
  { id: 6, name: "OpenAI", symbol: "✹ OpenAI" },
];

const CAROUSEL_CARDS = [
  {
    title: "Algoritmo de Inércia Zero-Glitch",
    desc: "Molas amortecidas em tempo de execução sem dependência de passos fixos.",
    badge: "Physics Engine",
  },
  {
    title: "Minimal-Clone Dom Ticker",
    desc: "Apenas a quantidade exata de nós necessária para preencher o viewport.",
    badge: "Performance",
  },
  {
    title: "useCurtains Router Sync",
    desc: "Transição atômica que segura o reveal até o término do render React.",
    badge: "Next.js Ready",
  },
  {
    title: "Dynamic Cursor Magnetism",
    desc: "Snap contextual sobre botões de comando e campos de digitação.",
    badge: "Tactile UI",
  },
];

export function MotionUIDemoShowcase() {
  const [metricValue, setMetricValue] = useState(14820);
  const [activeTab, setActiveTab] = useState(0);
  const [curtains, isCurtainPending] = useCurtains();

  // Alterna valores para demonstrar a fluidez do AnimateNumber
  const cycleMetric = () => {
    const variance = (Math.random() - 0.5) * 5000;
    setMetricValue((prev) => Math.max(1000, Math.round(prev + variance)));
  };

  // Simulação de transição de rota com useCurtains
  const handleSimulatedNavigation = async (tabIndex: number) => {
    if (tabIndex === activeTab) return;
    
    await curtains(
      () => {
        // Callback assíncrono executado enquanto a cortina cobre totalmente a tela
        setActiveTab(tabIndex);
      },
      {
        effect: wipe({ direction: "right", angle: 8 }),
        transition: { duration: 0.45, ease: [0.16, 1, 0.3, 1] },
      }
    );
  };

  return (
    <div className="relative min-h-screen bg-zinc-950 text-zinc-100 font-sans selection:bg-amber-500/30 selection:text-amber-200 p-6 md:p-12 overflow-x-hidden">
      {/* 1. CURSOR INTELIGENTE (Ativo apenas em dispositivos com mouse) */}
      <div className="hidden md:block">
        <Cursor 
          className="border-2 border-amber-400 bg-amber-400/20 backdrop-blur-xs pointer-events-none rounded-full"
          transition={{ type: "spring", stiffness: 350, damping: 25, mass: 0.6 }}
        />
      </div>

      {/* CABEÇALHO DO PROJETO */}
      <header className="max-w-6xl mx-auto flex flex-col md:flex-row items-start md:items-center justify-between border-b border-zinc-800/80 pb-6 mb-12 gap-6">
        <div>
          <div className="flex items-center gap-2 mb-2">
            <span className="w-2.5 h-2.5 rounded-full bg-emerald-500 animate-pulse" />
            <span className="text-xs font-mono uppercase tracking-widest text-zinc-400">
              Motion UI Primitives v12
            </span>
          </div>
          <h1 className="text-3xl md:text-4xl font-bold tracking-tight text-white flex items-center gap-3">
            <Typewriter backspace="word" className="text-white">
              Sistemas de Movimento em Escala
            </Typewriter>
          </h1>
        </div>

        {/* NAVEGAÇÃO TESTANDO useCurtains */}
        <nav className="flex items-center gap-2 bg-zinc-900/90 border border-zinc-800 p-1.5 rounded-xl">
          {["Painel", "Engenharia", "Configuração"].map((tabName, index) => (
            <button
              key={tabName}
              onClick={() => handleSimulatedNavigation(index)}
              disabled={isCurtainPending}
              className={`px-4 py-1.5 text-xs font-medium rounded-lg transition-colors cursor-pointer ${
                activeTab === index 
                  ? "bg-amber-500 text-zinc-950 font-semibold shadow-sm" 
                  : "text-zinc-400 hover:text-zinc-200 hover:bg-zinc-800/50"
              }`}
            >
              {tabName}
            </button>
          ))}
        </nav>
      </header>

      {/* CONTEÚDO PRINCIPAL */}
      <main className="max-w-6xl mx-auto space-y-16">
        {/* SEÇÃO 1: MÉTRICAS VIVAS COM AnimateNumber & ScrambleText */}
        <section className="grid grid-cols-1 md:grid-cols-3 gap-6">
          {/* Card de Métricas de Transações */}
          <div className="bg-zinc-900/60 border border-zinc-800/80 rounded-2xl p-6 backdrop-blur-md flex flex-col justify-between">
            <div>
              <div className="flex justify-between items-center mb-3">
                <span className="text-xs font-mono text-zinc-400">MÉTRICA EM TEMPO REAL</span>
                <button
                  onClick={cycleMetric}
                  className="text-xs text-amber-400 hover:text-amber-300 font-mono underline cursor-pointer"
                >
                  [Atualizar Valor]
                </button>
              </div>
              <div className="text-4xl md:text-5xl font-black font-mono tracking-tight text-white my-4">
                <AnimateNumber
                  transition={{
                    layout: { duration: 0.35 },
                    y: { type: "spring", visualDuration: 0.4, bounce: 0.15 }
                  }}
                  format={{
                    style: "currency",
                    currency: "USD",
                    maximumFractionDigits: 0
                  }}
                >
                  {metricValue}
                </AnimateNumber>
              </div>
            </div>
            <p className="text-xs text-zinc-400">
              Transições por odômetro digital de dígitos com layout flexível.
            </p>
          </div>

          {/* Card de Decodificação de Status */}
          <div className="bg-zinc-900/60 border border-zinc-800/80 rounded-2xl p-6 backdrop-blur-md flex flex-col justify-between">
            <div>
              <span className="text-xs font-mono text-zinc-400 mb-3 block">TERMINAL HANDSHAKE</span>
              <div className="h-20 flex items-center">
                <span className="text-xl md:text-2xl font-mono text-emerald-400 font-bold">
                  <ScrambleText duration={1.2} delay={0.2}>
                    HASH_ENCRYPTION_VERIFIED_256
                  </ScrambleText>
                </span>
              </div>
            </div>
            <p className="text-xs text-zinc-400">
              Decodificação por entropia com resolução progressiva de caracteres.
            </p>
          </div>

          {/* Card de Micro-interação Magnética */}
          <div className="bg-zinc-900/60 border border-zinc-800/80 rounded-2xl p-6 backdrop-blur-md flex flex-col justify-between">
            <div>
              <span className="text-xs font-mono text-zinc-400 mb-3 block">TESTE DE CAMPO HÁPTICO</span>
              <p className="text-sm text-zinc-300 mb-4">
                Passe o cursor sobre os botões abaixo para sentir a atração magnética de snap:
              </p>
              <div className="flex gap-3">
                <button 
                  className="px-4 py-2 bg-zinc-800 hover:bg-zinc-700 text-zinc-100 rounded-lg text-xs font-semibold cursor-pointer transition-transform active:scale-95"
                  data-cursor-magnetic
                >
                  Ação Alpha
                </button>
                <button 
                  className="px-4 py-2 bg-amber-500 hover:bg-amber-400 text-zinc-950 rounded-lg text-xs font-semibold cursor-pointer transition-transform active:scale-95"
                  data-cursor-magnetic
                >
                  Ação Beta
                </button>
              </div>
            </div>
            <p className="text-xs text-zinc-400 mt-4">
              Ponteiro com molas calibradas e absorção vetorial em alvos.
            </p>
          </div>
        </section>

        {/* SEÇÃO 2: TICKER INFINITO DE LOGOTIPOS */}
        <section className="border-y border-zinc-800/80 py-6 bg-zinc-900/30">
          <div className="mb-3 px-4 text-center">
            <span className="text-xs font-mono uppercase tracking-widest text-zinc-400">
              Algoritmo Minimal-Clone Marquee (Zero Garbage Collection)
            </span>
          </div>
          <Ticker
            velocity={50}
            className="flex items-center gap-12"
            items={PARTNER_LOGOS.map((logo) => (
              <div
                key={logo.id}
                className="flex items-center gap-2 px-6 py-2.5 rounded-lg bg-zinc-900 border border-zinc-800/70 text-zinc-300 font-mono text-sm tracking-wide whitespace-nowrap hover:border-amber-500/50 hover:text-white transition-colors cursor-pointer"
              >
                <span>{logo.symbol}</span>
              </div>
            ))}
          />
        </section>

        {/* SEÇÃO 3: CARROSSEL DE PRODUÇÃO COM MOLA E ARRASTO */}
        <section>
          <div className="flex items-center justify-between mb-6">
            <div>
              <h2 className="text-2xl font-bold tracking-tight text-white">
                Física de Arrasto & Sliders
              </h2>
              <p className="text-xs text-zinc-400 mt-1">
                Suporte total a teclado (Setas), roda de mouse e arrasto inercial com mola.
              </p>
            </div>
          </div>

          <div className="relative">
            <Carousel
              gap={24}
              align="start"
              className="py-4"
              items={CAROUSEL_CARDS.map((card, idx) => (
                <div
                  key={idx}
                  className="w-[320px] md:w-[380px] h-[220px] bg-gradient-to-br from-zinc-900 to-zinc-950 border border-zinc-800 hover:border-zinc-700 p-6 rounded-2xl flex flex-col justify-between select-none shadow-lg cursor-grab active:cursor-grabbing transition-colors"
                >
                  <div>
                    <span className="inline-block px-2.5 py-1 text-[10px] font-mono uppercase bg-amber-500/10 text-amber-400 border border-amber-500/20 rounded-md mb-3">
                      {card.badge}
                    </span>
                    <h3 className="text-lg font-semibold text-white tracking-tight mb-2">
                      {card.title}
                    </h3>
                    <p className="text-xs text-zinc-400 leading-relaxed">
                      {card.desc}
                    </p>
                  </div>
                  <div className="text-[11px] font-mono text-zinc-400">
                    Arrasto de alta precisão #0{idx + 1}
                  </div>
                </div>
              ))}
            />
          </div>
        </section>
      </main>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao planejar e arquitetar um projeto de software ou landing page que utilizará o **Motion UI**, a Inteligência Artificial e os Engenheiros de UI devem seguir as diretrizes rigorosas abaixo antes de iniciar a codificação:

### 1. Declaração do Stack de Animação no Blueprint
- Especificar explicitamente o pacote: `motion` (v12) e a suíte de primitivas `motion-plus` (`motion-plus/react`, `motion-plus/curtains`).
- Deixar claro o papel de cada biblioteca: o Tailwind CSS fornece o layout e estados simples de cor/hover; o Motion UI comanda a física de arrasto, layouts espaciais, cursores e transições contínuas de viewport.

### 2. Tabela de Mapeamento de Primitivas no Blueprint
O blueprint deve conter a matriz exata de atribuição de componentes para cada seção da aplicação:

| Seção do Projeto | Componente Motion UI | Configuração de Efeito / Física | Fallback para Redução de Movimento |
| :--- | :--- | :--- | :--- |
| **Hero Title** | `<Typewriter>` ou `<ScrambleText>` | Cadência humana (`backspace="word"`), duração 1.2s | Renderiza texto estático final sem animação |
| **Parceiros / Clientes** | `<Ticker>` | `velocity: 40`, `axis="x"`, minimal-clone | Grid flexível com overflow-x e scroll nativo |
| **Métricas / Preços** | `<AnimateNumber>` | `visualDuration: 0.35`, `bounce: 0.15`, `Intl.NumberFormat` | Troca instantânea do valor de texto |
| **Galeria / Showcase** | `<Gallery>` ou `<Carousel>` | `arrange={barrel()}`, inércia por mola | Grid responsivo padrão (2 a 3 colunas) |
| **Navegação de Rota** | `useCurtains` | `effect: wipe({ direction: "left", angle: 10 })` | `router.push()` imediato sem cortina visual |
| **Ponteiro Global** | `<Cursor>` | `mode="follow"`, magnético em botões (`data-cursor-magnetic`) | Desativado globalmente em telas sensíveis ao toque |

### 3. Diretriz de Governança de Performance & Core Web Vitals
- **LCP (Largest Contentful Paint)**: Elementos visuais primários (imagens de hero, títulos H1) nunca devem depender de callbacks de animação assíncronos para ficarem visíveis no DOM. Utilize visibilidade padrão e anime a partir do estado inicial.
- **CLS (Cumulative Layout Shift)**: O `<AnimateNumber>` e o `<Typewriter>` devem reservar o espaço dimensional exato do texto final usando containers com `min-height` ou grids de reserva para evitar empurrões bruscos nos elementos irmãos durante a digitação.
- **Isolamento de Redução de Movimento**: Toda chamada a `useCurtains` ou componentes contínuos (`Ticker`) deve validar `useReducedMotion()`.
