---
id: "animate-ui"
name: "Animate UI"
url: "https://animate-ui.com/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Modern Micro-Motion", "Drop-in Fluid Kinetics", "Subtle Organic Springs", "Kinetic Typography & Data-Odometers", "Generative Interactive Backdrops"]
densidade_informacao: "Flexivel"
impacto_visual: "Moderado a Alto/Showstopper"
custo_computacional: "Medio (Motion/Framer Motion JS) a Baixo (Headless CSS Springs)"
stack_frameworks: ["React 19 / 18", "Vue 3", "Next.js", "Tailwind CSS (v3 & v4)", "Motion (Framer Motion v11/12)", "Radix UI", "Base UI", "React Aria", "Reka UI", "Lucide React"]
compatibilidade:
  fontes_ideais: ["Outfit", "Geist Sans", "Inter", "Plus Jakarta Sans", "JetBrains Mono"]
  paletas_ideais: ["Modern Neutral Monochromatic (Zinc/Neutral 950)", "High-Tech Dark Glows (Cyan 500, Electric Violet, Emerald)", "Clean Crisp Light Surface"]
  combinacoes_recomendadas: ["Shadcn UI", "Magic UI", "Cult UI", "Aceternity UI", "Radix UI", "Base UI"]
  conflitos_esteticos: ["Brutalismo Cru sem Easing", "Corporate Memphis 2D Estático", "Skeuomorfismo pesado com texturas analógicas de couro/madeira"]
---

# Animate UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e arquitetado pelo engenheiro frontend **Sky Leen** (`imskyleen`), o **Animate UI** (`animate-ui.com`) resolve uma das maiores dores da era moderna do design de interfaces web: o abismo entre bibliotecas de componentes estáticos (como `shadcn/ui`, `Radix UI` e `Base UI`) e a fluidez orgânica dos ecossistemas de motion design contemporâneos. Enquanto a maioria das bibliotecas de UI exige que o desenvolvedor reescreva seus componentes, adote wrappers engessados ou instale megapacotes proprietários para obter animações fluidas, o Animate UI introduziu o paradigma inovador de **"Animated Drop-in Primitives" (Primitivas Animadas Substitutivas)**.

A assinatura visual e técnica do Animate UI se fundamenta em cinco pilares singulares:

1. **Injeção Transparente de Movimento (Swap the Import, Keep the API)**:
   Em vez de substituir o seu componente `Accordion` ou `Dialog` do `shadcn/ui` por outro componente visual com classes pré-fixadas, o Animate UI atua na raiz do componente: as primitivas headless (`@radix-ui/react-*`, `@base-ui/react` ou `react-aria-components`). Ao trocar apenas a linha de importação (ou acionar o comando automatizado da CLI), o componente existente herda animações calibradas com física de mola (`Motion`), preservando 100% da sua estrutura JSX, estilização Tailwind CSS, estados de acessibilidade WAI-ARIA e propriedades customizadas.

2. **Acabamento Óptico com Gradientes de Máscara (Panel Content Masking)**:
   Um dos defeitos mais incômodos em acordões e menus expansíveis da web tradicional é o corte abrupto de texto ou a deformação de layout quando o container colapsa. O Animate UI resolve isso aplicando máscaras alfa CSS dinâmicas (`mask-image: linear-gradient(to bottom, black max(100% - 16px, 200% - var(--animate-ui-panel-content, 100%)), transparent)`). Conforme o conteúdo desliza ou a altura se recalcula, a extremidade inferior sofre um desfoque óptico gradual, eliminando cortes duros e conferindo um aspecto tátil refinado de hardware de luxo.

3. **Arquitetura de Destaque Flutuante Compartilhado (`Motion Highlight`)**:
   Em componentes de navegação, abas, sidebars e grupos de botões, o Animate UI emprega o padrão de realce deslizante compartilhado. Um indicador de fundo único (`data-slot="motion-highlight"`) calcula bounding boxes e desliza suavemente sob o cursor ou sob a aba ativa usando transições de layout contínuas do `Motion`, conferindo uma sensação de continuidade espacial idêntica à do macOS e iOS.

4. **Micromovimento Reativo em Vetores SVG (Motion Icons)**:
   O projeto transcendeu ícones estáticos criando versões cinéticas do acervo do **Lucide Icons** e **Hugeicons**. Em vez de aplicar giros ou pulsações genéricas no container SVG inteiro, o Animate UI manipula vetores internos individuais via coordenadas de `pathLength`, rotações parciais de ponteiros, desdobramentos de checklists e vibrações magnéticas disparadas por eventos granulares (`hover`, `click`, `tap`, `in-view` ou programmatic triggers).

5. **Dualidade Equilibrada entre Utilidade e Efeito Cenográfico (Showstoppers)**:
   O catálogo transita com maestria entre a discrição operacional de formulários corporativos (inputs OTP com escala elástica, badges de status, botões de cópia que transicionam o ícone sem salto) e efeitos visuais imersivos de landing page (como o fundo topográfico interativo `Topography`, o túnel gravitacional `Hole`, `Glyph Matrix` e botões líquidos deformáveis `Liquid Button`).

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **Aplicações SaaS B2B e B2C Construídas sobre Shadcn / Radix / Base UI**:
   É a escolha número 1 absoluta para qualquer produto que já utiliza o ecossistema `shadcn/ui` e quer elevar o nível de polimento visual para o padrão de empresas como Vercel, Linear, Raycast e Cron, sem refatorar o design system existente.
2. **Produtos de Inteligência Artificial, DevTools e Workspaces Técnicos**:
   Interfaces que exigem feedback contínuo em streaming de texto, execução de código e tokens. Componentes como *Code Block* com digitação automatizada caractere a caractere (`typing-effect`), *Copy Button* reativo com morphing de ícone, *Input OTP* animado para autenticação de 2 fatores e *Sliding Numbers* para métricas de computação em tempo real.
3. **Landing Pages de Produtos High-Tech & Portfólios de Creative Engineers**:
   Seções de Hero e apresentação visual que precisam capturar a atenção imediata através de *Topography Background*, *Hole Tunnel*, *Glyph Matrix*, *Rotating Text* e cartões com perspectiva 3D (*Tilt* e *Magnetic*).
4. **Interfaces Mobile-First e Web Apps PWA**:
   Aplicações que requerem barras de navegação inferiores móveis (*Bottom Navigation*) que recolhem automaticamente com o scroll para maximizar a área útil da tela, além de drawers e modais elásticos que respondem a gestos táteis sem atraso de renderização.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Neutra e Primitivas Estruturais)**:
   Superfícies de leitura sóbrias estruturadas em `bg-background`, `border-border/40` e tipografia `Geist Sans` ou `Outfit`. As primitivas funcionais do Animate UI (*Accordion*, *Collapsible*, *Dialog*, *Dropdown Menu*, *Select*, *Tabs*, *Switch*, *Checkbox*) atuam nesta camada garantindo que cada interação de rotina ocorra sem cortes secos, mas com transições ágeis (entre 150ms e 250ms).
- **30% (Camada Tátil, Micro-interações e Feedback Sensorial)**:
   A camada onde o Animate UI mais se destaca:
   - *Motion Icons* que reagem com microanimações de traço ao passar o mouse.
   - *Copy Button* que substitui o ícone com fade/blur suave ao copiar chaves de API.
   - *Motion Highlight* deslizando suavemente entre abas e rotas da navbar.
   - *Theme Toggler* utilizando a View Transitions API para transicionar do claro para o escuro como uma onda circular.
   - *Auto Height* em formulários multi-etapas para prevenir saltos de layout.
- **10% (Showstoppers Protagonistas)**:
   Reserve componentes teatrais estritamente para os momentos de impacto máximo:
   - Um único background interativo no Hero (*Topography*, *Gravity Stars* ou *Hole*).
   - Um *Rotating Text* ou *Morphing Text* no título principal da página.
   - Um *Liquid Button* ou *Flip Button* no botão de Call to Action (CTA) central da conversão.
   - *Nunca* acumule dois backgrounds procedurais ou múltiplos botões com explosão de partículas na mesma viewport.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Tabelas de Dados Densas de Alta Frequência (Data Grids Financeiros & Trading)**:
   Em telas com centenas de células renderizando cotações em milissegundos (order books, telemetria em tempo real), instanciar instâncias do `motion.div` para cada número causa acúmulo no garbage collector do navegador e perda de frames. Nestes casos, prefira CSS puro com transições de opacidade ou WebGL nativo.
- **Documentação Técnica Estática & Portais de Leitura Pura (Wikis/Blogs Minimalistas)**:
   Páginas voltadas à leitura longa onde animações de entrada de texto (*Splitting Text*, *Typing Text*) tornam a leitura frustrante, obrigando o usuário a esperar as letras aparecerem para conseguir ler o conteúdo.
- **Ambientes Corporativos com Restrições Estritas de Acessibilidade ou Conexão Lenta**:
   Sistemas com suporte legado que desabilitam JavaScript ou em dispositivos móveis ultra-básicos, onde os ouvintes de coordenadas de mouse para efeitos como *Tilt*, *Magnetic* e partículas contínuas esgotam recursos da CPU e bateria.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **Sobrecarga de Fontes e Efeitos Cinéticos de Texto Simultâneos**:
   Combinar *Rotating Text*, *Gradient Text* animado e *Shimmering Text* em parágrafos adjacentes. Efeitos de texto devem ser aplicados a uma única palavra-chave ou frase curta em toda a página.
- **Inércia Excessiva em Componentes Críticos de Decisão (Slow Springs)**:
   Configurar molas com `damping` muito baixo em modais de confirmação, selects ou formulários de checkout, fazendo com que o menu "quique" por 600ms antes de estabilizar. Componentes de entrada e saída devem resolver em menos de 200ms.
- **Omissão da Regra de Redução de Movimento (`prefers-reduced-motion`)**:
   Implementar backgrounds com partículas ativas ou rotações sem o hook `useReducedMotion()` ou a diretiva Tailwind `motion-reduce:hidden`. O Animate UI inclui suporte nativo a acessibilidade, e ignorar essa diretiva quebra conformidade com WCAG 2.2 AA.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 12 componentes e famílias de recursos mais importantes do acervo do Animate UI:

### 1. Animated Accordion & Collapsible (`primitives/base-ui/accordion` / `radix-ui`)
- **Anatomia Visual**: Painéis colapsáveis verticais com tipografia limpa, separadores discretos e chevron giratório com amortecimento `cubic-bezier(0.215, 0.61, 0.355, 1)`. O diferencial marcante é a aplicação interna de máscara linear CSS (`mask-image`), fazendo o texto desvanecer sutilmente na base durante o recolhimento, sem cortes abruptos.
- **Gatilho de Interação**: Clique no cabeçalho ou navegação via teclado (`Enter`/`Espaço`).
- **Onde encaixar**: Seção de FAQ em landing pages, seções colapsáveis em painéis de configurações e filtros avançados de busca em e-commerce.

### 2. Motion Highlight & Gliding Tabs (`primitives/animate-ui/highlight` + `tabs`)
- **Anatomia Visual**: Conjunto de abas horizontais encapsuladas em uma pílula externa fosca (`bg-accent/50`). O elemento selecionado recebe um invólucro de destaque flutuante (`data-slot="motion-highlight"`) que desliza fisicamente de um item para outro com física de mola suave (`layoutId`). Os painéis de conteúdo realizam transições de slide e fade acompanhadas pelo ajuste automático de altura do container.
- **Gatilho de Interação**: Clique em abas adjacentes ou hover em menus de navegação.
- **Onde encaixar**: Header principal de navegação, alternador de periodicidade em tabelas de preços (Mensal / Anual), e alternador de views em dashboards.

### 3. Animated Input OTP (`primitives/animate-ui/input-otp`)
- **Anatomia Visual**: Conjunto de caixas de entrada de código numérico de alta precisão. À medida que o usuário digita, cada dígito entra com um efeito sutil de escala e subida (`scale: 0.8 -> 1`, `opacity: 0 -> 1`). Ao colar um código completo da área de transferência, os números entram em sequência escalonada (*staggered pop-in* de 40ms por dígito) com um cursor de foco pulsante. Drop-in replacement para o pacote `input-otp` tradicional.
- **Gatilho de Interação**: Digitação via teclado ou evento de colar (`Ctrl+V` / `Cmd+V`).
- **Onde encaixar**: Modais de autenticação de dois fatores (2FA), verificação de e-mail e telas de confirmação de transferência bancária/PIX.

### 4. Rotating Text & Morphing Text (`primitives/animate-ui/rotating-text` / `morphing-text`)
- **Anatomia Visual**:
  - *Rotating Text*: Um carrossel vertical de palavras que se alternam no mesmo ponto da frase, com máscara de corte superior e inferior (`overflow: clip`). A palavra anterior sobe e desvanece enquanto a nova surge da base com desfoque de movimento transitório (`filter: blur(8px) -> none`).
  - *Morphing Text*: As letras individuais de uma palavra deslizam vetorialmente até suas novas posições para formar a próxima palavra, mantendo letras coincidentes intactas.
- **Gatilho de Interação**: Ciclo temporal automático (*auto-play* com intervalo configurável de 2.5s a 4s).
- **Onde encaixar**: Título principal da Hero Section ("Desenvolva interfaces para [SaaS / IA / Mobile / Web] com velocidade").

### 5. Sliding & Scrolling Number Tickers (`primitives/animate-ui/sliding-number` / `scrolling-number`)
- **Anatomia Visual**: Dígitos numéricos inspirados em hodômetros mecânicos e placares analógicos. Cada casa decimal (unidades, dezenas, centenas, milhares) é uma coluna vertical de algarismos (0 a 9) que rola independentemente com aceleração e desaceleração inercial suave até ancorar no valor correto.
- **Gatilho de Interação**: Atualização de estado reativo de valor (`count` state change) ou gatilho de visibilidade ao entrar na viewport (`inView`).
- **Onde encaixar**: Métricas de prova social no Hero ("+45.890 usuários ativos"), contadores de faturamento em dashboards e contadores de estrelas no GitHub.

### 6. Micro-Animated Copy Button (`primitives/animate-ui/copy-button`)
- **Anatomia Visual**: Botão compacto utilitário que exibe o ícone clássico de duas folhas sobrepostas. Ao clicar, o ícone sofre um encolhimento com rotação sutil (`scale: 0.7, opacity: 0`), dando lugar instantaneamente a um ícone de verificação (*check*) verde ou branco que surge com um leve pulso elástico. Após 2 segundos, o estado reverte suavemente.
- **Gatilho de Interação**: Clique no botão ou atalho de teclado.
- **Onde encaixar**: Caixas de código Shiki/Prism em documentações, blocos de comandos de terminal no Hero (`npx @animate-ui/cli...`) e campos de chave de API em dashboards.

### 7. Liquid & Ripple Buttons (`primitives/animate-ui/liquid-button` / `ripple-button`)
- **Anatomia Visual**:
  - *Liquid Button*: Um botão cujos cantos e preenchimento de fundo se comportam como um fluido sob tensão superficial. Ao passar o mouse, uma onda de cor emerge da base ou do ponto de entrada do cursor, preenchendo o botão com uma curva orgânica.
  - *Ripple Button*: Dispara uma onda de dispersão radial a partir das coordenadas exatas do clique (`clientX`, `clientY`), expandindo-se até os limites da borda com desvanecimento exponencial.
- **Gatilho de Interação**: Hover e clique do ponteiro do mouse ou toque.
- **Onde encaixar**: Botões de Call to Action (CTA) principais em landing pages de vendas ou botões de checkout.

### 8. Motion Lucide Icons (`icons/lucide-icons`)
- **Anatomia Visual**: Ícones vetoriais familiares do catálogo Lucide redesenhados como componentes reativos do `Motion`. Ícones como `Check` desenham o traço do início ao fim; `Bell` oscila em pêndulo como um sino real; `Settings` gira suas engrenagens; e `Chevron` flexiona seus vértices.
- **Gatilho de Interação**: Hover no elemento pai (`group-hover`), evento de clique ou propriedade booleana controlada (`isHovered`, `active`).
- **Onde encaixar**: Menus laterais de sidebar, botões de ação em barras de ferramentas e cartões de lista de recursos (Bento Grid).

### 9. Topography Background (`backgrounds/topography`)
- **Anatomia Visual**: Malha gerada proceduralmente de linhas de contorno topográficas que lembram cartas geográficas militares ou mapas de altitude. As curvas respiram lentamente em segundo plano com variações de seno e cosseno. Conforme o mouse se desloca, a topografia reage criando uma elevação sob o cursor, e um clique emite uma onda sísmica expansiva que reverbera pela tela.
- **Gatilho de Interação**: Movimento contínuo do mouse e cliques na tela.
- **Onde encaixar**: Fundo da seção Hero em produtos de infraestrutura de dados, computação em nuvem, geo-localização e IA avançada.

### 10. Gravitational Hole & Glyph Backgrounds (`backgrounds/hole` / `backgrounds/glyph`)
- **Anatomia Visual**:
  - *Hole*: Uma lente gravitacional que simula a dobra do espaço-tempo em torno de um orifício central com anéis concêntricos em perspectiva e partículas que convergem para o centro.
  - *Glyph*: Uma matriz densa de caracteres alfanuméricos e glifos tipográficos que permanecem em repouso monocromático tênue. A passagem do cursor acende um rastro luminoso que desperta os caracteres adjacentes em brilho dinâmico, evocando a estética visual da ficção científica e do terminal cyberpunk.
- **Gatilho de Interação**: Coordenadas do ponteiro e animação contínua em loop leve.
- **Onde encaixar**: Banners de produtos de cibersegurança, criptografia, modelos de linguagem e plataformas para desenvolvedores.

### 11. Preview Link Card (`primitives/base-ui/preview-link-card`)
- **Anatomia Visual**: Um hiperlink textual inteligente que, ao receber foco ou hover, projeta um popover flutuante contendo o thumbnail ou screenshot real da página de destino, acompanhado de título, metadados e favicon. O card surge com escala sutil e desfoque reverso (`blur(4px) -> blur(0px)`).
- **Gatilho de Interação**: Hover do mouse com delay intencional de 150ms (para evitar disparos acidentais na rolagem).
- **Onde encaixar**: Artigos de documentação, referências externas em posts de blog técnico e feeds de links recomendados em comunidades.

### 12. 3D Tilt Card & Magnetic Element (`primitives/animate-ui/tilt` / `magnetic`)
- **Anatomia Visual**:
  - *Tilt*: Cartão que se inclina tridimensionalmente (`perspective: 1000px`, `rotateX`, `rotateY`) em direção ao cursor, gerando sensação de relevo e profundidade com brilho especular dinâmico na borda.
  - *Magnetic*: Elemento (como um botão flutuante ou badge) que é magneticamente atraído pelas coordenadas do cursor quando ele se aproxima do seu raio de atração, retornando à posição original com mola inercial ao sair.
- **Gatilho de Interação**: Movimento do ponteiro sobre a área do componente.
- **Onde encaixar**: Cartões de destaque do Bento Grid, botões flutuantes de suporte/chat e avatares de equipe.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Pacotes
O ecossistema Animate UI opera tanto via registro de componentes distribuídos no estilo `shadcn` quanto via pacote de primitivas:

```bash
# Instalação do pacote principal e do motor de animação
npm install motion clsx tailwind-merge lucide-react

# Ou com pnpm
pnpm add motion clsx tailwind-merge lucide-react
```

### Instalação via CLI Inteligente do Animate UI
O Animate UI oferece uma CLI dedicada que pode analisar o seu diretório de componentes existente e injetar motion automaticamente em todas as primitivas instaladas:

```bash
# Animar todas as primitivas existentes no projeto de uma só vez
npx @animate-ui/cli@latest animate all

# Adicionar componentes específicos via CLI do Animate UI
npx @animate-ui/cli@latest add accordion tabs button

# Ou adicionar diretamente via registro público shadcn
npx shadcn@latest add "https://animate-ui.com/r/accordion"
npx shadcn@latest add "https://animate-ui.com/r/copy-button"
npx shadcn@latest add "https://animate-ui.com/r/topography"
```

### Parâmetros de Física de Movimento (Motion Springs & Bezier Curves)
O Animate UI padroniza transições com base no equilíbrio entre responsividade tátil e naturalidade física:

```typescript
// Configurações padrão de mola (Spring) do Animate UI
export const defaultSpring = {
  type: "spring",
  stiffness: 400,
  damping: 30,
  mass: 0.8,
};

// Mola suave para transições de layout compartilhado (Motion Highlight)
export const glideSpring = {
  type: "spring",
  stiffness: 350,
  damping: 28,
};

// Curva cúbica para recolhimento e expansão sem overshoot
export const smoothEase = [0.215, 0.61, 0.355, 1]; // cubic-bezier(0.215, 0.61, 0.355, 1)
```

---

### Receita de Código Funcional: Abas com Realce Flutuante (`Motion Highlight`) e Conteúdo com Altura Animada

Abaixo está uma implementação realista e autocontida que demonstra o padrão de **Motion Highlight** e **Auto-Height** do Animate UI para abas de navegação:

```tsx
"use client";

import React, { useState } from "react";
import { motion, AnimatePresence } from "motion/react";
import { cn } from "@/lib/utils";

interface TabItem {
  id: string;
  label: string;
  badge?: string;
  content: {
    title: string;
    description: string;
    tag: string;
  };
}

const TABS: TabItem[] = [
  {
    id: "overview",
    label: "Visão Geral",
    badge: "v2.3",
    content: {
      title: "Primitivas de Alta Performance",
      description: "Todas as primitivas mantêm total conformidade WAI-ARIA com zero perda de acessibilidade estrutural.",
      tag: "Radix & Base UI Compatible",
    },
  },
  {
    id: "motion",
    label: "Física de Movimento",
    content: {
      title: "Molas Orgânicas com Motion",
      description: "Elimine transições lineares duras usando curvas de relaxamento inercial calculadas por mola.",
      tag: "Framer Motion 12",
    },
  },
  {
    id: "cli",
    label: "Automação CLI",
    badge: "Novo",
    content: {
      title: "Transformação em um Comando",
      description: "Substitua imports legados por primitivas animadas instantaneamente via @animate-ui/cli sem quebrar o JSX.",
      tag: "Zero-Refactor",
    },
  },
];

export function AnimateUITabsShowcase() {
  const [activeTab, setActiveTab] = useState(TABS[0].id);
  const activeContent = TABS.find((t) => t.id === activeTab)!.content;

  return (
    <div className="w-full max-w-xl mx-auto rounded-2xl border border-neutral-200 bg-white/80 p-4 shadow-xl backdrop-blur-md dark:border-neutral-800 dark:bg-neutral-900/80">
      {/* Tablist com Motion Highlight Compartilhado */}
      <div
        role="tablist"
        aria-orientation="horizontal"
        className="relative flex items-center gap-1 rounded-xl bg-neutral-100 p-1 dark:bg-neutral-800/60"
      >
        {TABS.map((tab) => {
          const isActive = activeTab === tab.id;
          return (
            <button
              key={tab.id}
              role="tab"
              aria-selected={isActive}
              onClick={() => setActiveTab(tab.id)}
              className={cn(
                "relative z-10 flex flex-1 items-center justify-center gap-1.5 py-2 px-3 text-xs font-medium transition-colors duration-200 outline-none select-none",
                isActive
                  ? "text-neutral-900 dark:text-neutral-50"
                  : "text-neutral-600 hover:text-neutral-900 dark:text-neutral-400 dark:hover:text-neutral-200"
              )}
            >
              {/* O Indicador Flutuante Deslizante */}
              {isActive && (
                <motion.div
                  layoutId="active-tab-highlight"
                  data-slot="motion-highlight"
                  className="absolute inset-0 z-0 rounded-lg bg-white shadow-sm dark:bg-neutral-700/80"
                  transition={{
                    type: "spring",
                    stiffness: 400,
                    damping: 30,
                  }}
                />
              )}
              <span className="relative z-10">{tab.label}</span>
              {tab.badge && (
                <span
                  className={cn(
                    "relative z-10 rounded-full px-1.5 py-0.2 text-[10px] font-semibold tracking-wide",
                    isActive
                      ? "bg-neutral-900 text-white dark:bg-neutral-100 dark:text-neutral-900"
                      : "bg-neutral-200 text-neutral-600 dark:bg-neutral-700 dark:text-neutral-300"
                  )}
                >
                  {tab.badge}
                </span>
              )}
            </button>
          );
        })}
      </div>

      {/* Painel de Conteúdo com Auto-Height e Transição Direcional */}
      <motion.div
        layout
        className="relative mt-4 overflow-hidden rounded-xl border border-neutral-200/60 bg-neutral-50/50 p-5 dark:border-neutral-800/60 dark:bg-neutral-950/40"
        transition={{ type: "spring", stiffness: 350, damping: 30 }}
      >
        <AnimatePresence mode="wait">
          <motion.div
            key={activeTab}
            initial={{ opacity: 0, y: 10, filter: "blur(4px)" }}
            animate={{ opacity: 1, y: 0, filter: "blur(0px)" }}
            exit={{ opacity: 0, y: -10, filter: "blur(4px)" }}
            transition={{ duration: 0.22, ease: [0.215, 0.61, 0.355, 1] }}
            className="flex flex-col gap-2"
          >
            <div className="flex items-center justify-between">
              <h4 className="text-sm font-semibold text-neutral-900 dark:text-neutral-100">
                {activeContent.title}
              </h4>
              <span className="rounded-md border border-neutral-200 bg-neutral-100 px-2 py-0.5 text-[10px] font-mono text-neutral-600 dark:border-neutral-800 dark:bg-neutral-800 dark:text-neutral-400">
                {activeContent.tag}
              </span>
            </div>
            <p className="text-xs leading-relaxed text-neutral-600 dark:text-neutral-400">
              {activeContent.description}
            </p>
          </motion.div>
        </AnimatePresence>
      </motion.div>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma nova interface ou design system que utilize o **Animate UI**, inclua as instruções abaixo nas seções de Arquitetura de Componentes e Motion Guidelines:

1. **Declaração de Pacotes & Ferramental**:
   ```yaml
   motion_layer:
     engine: "motion/react (Framer Motion v12)"
     primitives_provider: "Animate UI (v2.3+)"
     cli_migration_command: "npx @animate-ui/cli@latest animate all"
     registry_url: "https://animate-ui.com/r/{component}"
   ```

2. **Princípio do "Drop-in Replacement"**:
   - É expressamente proibido reescrever a hierarquia de componentes ou perder classes do Tailwind para acomodar animação.
   - Em vez de `<motion.div>` manuais em volta de cada acordeão ou menu, utilize as primitivas nativas do Animate UI que já encapsulam a lógica de `mask-image` e amortecimento de altura.

3. **Padronização de Tokens de Física de Mola**:
   - **Micro-interações (hover de ícones, botões, checkboxes)**: `stiffness: 450, damping: 30, mass: 0.6` (duração aparente ~150ms).
   - **Navegação & Destaque Flutuante (`motion-highlight`)**: `stiffness: 400, damping: 30` (duração aparente ~250ms).
   - **Expansão de Conteúdo (Acordeões, Drawers, Modais)**: Curva cúbica `[0.215, 0.61, 0.355, 1]` com tempo limite de 280ms.

4. **Regras de Limpeza Visual & Guardrails de Performance**:
   - Não combine mais de 1 background gerado (ex: *Topography*) com textos animados simultâneos na mesma seção.
   - Sempre envolva animações contínuas com a classe Tailwind `motion-reduce:hidden` ou condicional `useReducedMotion()`.
   - Utilize o `CopyButton` do Animate UI como padrão obrigatório para todos os blocos de código e comandos de terminal da interface.
