---
id: "motion-primitives"
name: "Motion Primitives"
url: "https://motion-primitives.com/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Modern Minimal Motion", "Typography Kinetics", "Micro-Interactions de Alta Fidelidade", "Layout Morphing & Shared Elements", "Apple-Grade Glass & Progressive Blurs"]
densidade_informacao: "Flexivel"
impacto_visual: "Moderado a Alto/Showstopper"
custo_computacional: "Medio (Motion/React Layout Projections & Spring Physics)"
stack_frameworks: ["React 19 / React 18", "Next.js (App Router & Pages Router)", "Motion (anteriormente Framer Motion)", "Tailwind CSS (v3 / v4)", "TypeScript"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "Plus Jakarta Sans", "SF Pro Display", "JetBrains Mono"]
  paletas_ideais: ["Deep Neutral Zinc (Zinc 950 / Zinc 50)", "High-Contrast Monochrome", "Subtle Alpha Borders (zinc-950/10, white/10)", "Muted Slate / Stone Gradients"]
  combinacoes_recomendadas: ["Shadcn UI", "Cult UI", "Magic UI", "Radix UI Primitives", "Lucide React"]
  conflitos_esteticos: ["Brutalismo cru sem easing ou molas", "Neumorfismo plástico pesado e hiper-saturado", "Corporate Memphis com vetores estáticos infantis", "Transições lineares duras de CSS puro"]
---

# Motion Primitives — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo engenheiro de design francês **Julien Thibeaut** (amplamente reconhecido na comunidade como **@ibelick**, também autor de projetos inovadores como *Prompt Kit* e *Mesurer*), o **Motion Primitives** (`motion-primitives.com`) consolidou-se como o padrão de ouro para componentes animados no ecossistema moderno de React, Next.js e Tailwind CSS.

Enquanto muitas bibliotecas de animação oferecem blocos visuais prontos e saturados que engessam o layout ou exigem shaders WebGL pesados, o Motion Primitives adota uma abordagem cirúrgica e minimalista: **primitivas atômicas desacopladas, focadas na física de movimento natural e na continuidade espacial de layout**.

### Os Pilares da Assinatura Visual do Motion Primitives:

1. **Continuidade de Superfície por Projeção de Layout (`layoutId` & Shared Elements)**:
   A marca registrada visual do Motion Primitives — personificada no *Morphing Dialog* e no *Morphing Popover* — reside na eliminação dos cortes secos e do fade clássico de caixas modais. Em vez de uma janela que surge repentinamente sobre um backdrop escurecido, o próprio gatilho (um card de produto, avatar ou botão de ação) sofre uma metamorfose fluida: suas dimensões, raio de curvatura (`border-radius`), imagens e tipografia interna expandem-se de maneira matematicamente coordenada para a posição final do modal. A ilusão criada é a de um único objeto físico contínuo, espelhando a linguagem de design do iOS e macOS.

2. **Tipografia Cinética Micro-Calculada (Character-Level Kinetics)**:
   Em componentes como *Text Morph*, *Text Loop*, *Text Roll*, *Text Scramble* e *Text Shimmer*, a tipografia deixa de ser um bloco estático de texto para se tornar um elemento dinâmico e expressivo. O algoritmo proprietário de *Text Morph*, por exemplo, decompõe as palavras em caracteres individuais indexados (`character.id`), preservando posições de letras idênticas enquanto projeta e desliza os caracteres comuns e desvanece suavemente as novas letras via `AnimatePresence mode="popLayout"`. O resultado é uma transição tipográfica orgânica comparável à das interfaces de IA e dashboards de ponta como Linear e Raycast.

3. **Desfoques Graduais de Nível Óptico (*Progressive Blur*)**:
   Tradicionalmente na web, o desfoque de fundo (`backdrop-filter: blur()`) sofre de uma limitação técnica gritante: a borda do desfoque é cortada de forma abrupta e retangular. O Motion Primitives resolve isso no componente *Progressive Blur* empilhando de 6 a 8 sub-camadas de desfoque fracionadas (`blurIntensity`), cada uma ponderada por uma máscara vetorial linear com interpolação de gradiente (`[mask-clip:padding-box]` e `linear-gradient`). Isso produz a mesma difusão gradual e suave de luz observada nas lentes de câmeras analógicas e nos menus suspensos do visionOS da Apple.

4. **Física de Molas de Resposta Instantânea (*Low-Mass Springs*)**:
   As animações da biblioteca evitam o rebote caricato ("bouncy cartoon"). Os parâmetros padrão de mola empregados por Thibeaut utilizam massa reduzida (`mass: 0.1` a `0.3`) combinada a rigidez equilibrada (`stiffness: 150` a `280`) e amortecimento crítico (`damping: 12` a `18`). O movimento transmite peso e inércia física sem retardar o tempo de percepção do usuário (mantendo o Time-to-Interactive abaixo de 300ms).

5. **Filosofia Copy-Paste & CLI Desacoplada (Shadcn Architecture)**:
   Assim como o `shadcn/ui`, o Motion Primitives não distribui componentes através de um pacote opaco em node_modules que restringe a estilização. Cada componente é injetado diretamente no projeto do desenvolvedor via CLI (`npx motion-primitives@latest add <component>`) ou através do registro do Shadcn, garantindo total soberania do código-fonte, compatibilidade com o Tailwind CSS v3/v4 e tipagem estrita com TypeScript.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **Interfaces de IA Generativa & Agentes Autônomos**:
   Ambientes onde estados transitórios mudam em tempo real (ex: "Pensando..." → "Pesquisando base..." → "Sintetizando resposta"). O uso de *Text Morph*, *Text Loop* e *Border Trail* comunica processamento contínuo com elegância, sem poluir a visão do usuário.
2. **Produtos SaaS B2B Premium & DevTools (Linear/Vercel/Raycast Style)**:
   Plataformas focadas em produtividade, onde cada micro-interação precisa transmitir robustez e precisão tátil. *Sliding Number* para métricas financeiras/tokens, *Animated Background* para abas de navegação, e *Toolbar Dynamic* para barras de ação contextuais.
3. **Showcases de Produto & Portfólios de Design Engineers**:
   Galerias de imagens, catálogos de arquitetura, estúdios de moda ou hardware de luxo onde os detalhes visuais precisam se expandir fluidamente via *Morphing Dialog*, preservando contexto visual e qualidade de imagem.
4. **Landing Pages de Alto Impacto & Waitlists de Startups**:
   Páginas de conversão que requerem diferenciação visual refinada sem recorrer a animações 3D pesadas que penalizam o Core Web Vitals e o LCP (Largest Contentful Paint).

### Papel no Ritmo Visual (Regra 60-30-10)

- **60% — Fundação Neutra e Estrutural (Tokens Padrão)**:
  Superfícies limpas, paleta monocromática neutra (`bg-zinc-950` / `bg-white`), bordas sutis com baixa opacidade (`border-zinc-200 dark:border-white/10`), tipografia estruturada (`Geist Sans` ou `Inter`) e grids consistentes.
- **30% — Camada de Fluidez e Feedback Tátil (Motion Primitives Estruturais)**:
  - *Animated Background*: Deslocamento suave da pílula ativa em navegações de abas, seletores de planos e menus superiores.
  - *Disclosure & Accordion*: Abertura e fechamento de seções com cálculo automático de altura natural (`height: 'auto'`).
  - *Transition Panel*: Transição entre etapas de formulários (multi-step wizards) ou abas de visualização de código.
  - *In View*: Revelação progressiva de elementos conforme o scroll da página atinge o viewport.
- **10% — Efeitos Protagonistas / Showstoppers (Micro-Momentos Memoráveis)**:
  - *Morphing Dialog*: Um card de galeria focal que se expande para tela cheia ocupando o centro da atenção.
  - *Sliding Number*: Métrica de destaque no Hero ou painel de pricing que rola organicamente até o valor selecionado.
  - *Text Morph*: Título principal do Hero com palavras mutáveis sincronizadas ou botão de call-to-action dinâmico.
  - *Progressive Blur*: Rodapé de viewport flutuante que funde o conteúdo rolado com a barra de ferramentas inferior.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Tabelas de Dados Densas de Alta Frequência (ERPs & Terminais de Trading)**:
  Em tabelas financeiras ou de telemetria com milhares de linhas atualizadas via WebSocket a 60 FPS, disparar projeções de layout e cálculos de mola com *Sliding Number* ou *Text Morph* em cada célula causará sobrecarga de CPU e perda severa de frames (*frame drop*). Nestes cenários, utilize tabelas virtualizadas puras em CSS ou Canvas.
- **Projetos com Suporte Obrigatório a Navegadores Legados sem CSS Moderno**:
  Recursos como *Border Trail* dependem de propriedades modernas como `offset-path: rect(...)` e `mask-composite: intersect`. Em browsers obsoletos que não suportam a especificação de CSS Motion Path ou CSS Masks compostas, o visual falhará silenciosamente sem o efeito luminoso.
- **Formulários Críticos de Checkout em Dispositivos de Baixa Potência**:
  Evite aninhar múltiplos componentes com `useMeasure()` ou detectores de mouse globais (*Spotlight*, *Magnetic*, *Cursor*) em telas mobile lentas, para não drenar desnecessariamente a bateria do usuário e evitar latência de clique (*tap delay*).

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **Sobrecarga de Gatilhos Concorrentes no Bento Grid**:
  Colocar em cada cartão de uma grade de 4 colunas um *Spotlight*, uma borda com *Border Trail*, um cursor customizado e tipografia com *Text Shimmer*. O excesso de movimento periférico distrai o olhar, enfraquece a hierarquia visual e cria uma sensação de amadorismo ("template de IA saturado").
- **Conflito de Teclado e Foco Acessível em Morphings**:
  Utilizar *Morphing Dialog* sem garantir o aprisionamento de foco (*focus trap*) e navegação por teclado (`Escape` para fechar, `Tab` cíclico). No Motion Primitives, a acessibilidade deve ser mantida utilizando atributos ARIA adequados e ouvintes de teclado.
- **Ignorar a Preferência de Movimento Reduzido (`prefers-reduced-motion`)**:
  Nunca force animações cinéticas intensas em usuários que configuraram redução de movimento no sistema operacional. Sempre adicione fallbacks de transição de opacidade simples quando `useReducedMotion()` estiver ativo.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 12 componentes mais representativos da biblioteca Motion Primitives, detalhando sua anatomia, física de interação e pontos ótimos de inserção no layout:

### 1. Morphing Dialog (`morphing-dialog`)
- **Anatomia Visual**: Composto por `MorphingDialog`, `MorphingDialogTrigger`, `MorphingDialogContainer`, `MorphingDialogContent`, `MorphingDialogImage`, `MorphingDialogTitle`, `MorphingDialogSubtitle`, `MorphingDialogDescription` e `MorphingDialogClose`. Em repouso, parece um card estático ou miniatura. Ao abrir, o container projeta suas bordas e imagem fluidamente para uma janela centralizada ou modal expandido, acompanhado de backdrop fosco e desfoque suave de fundo.
- **Gatilho de Interação**: Clique no trigger; fecha com clique fora (via `useClickOutside`), tecla `Escape` ou clique no botão fechar.
- **Onde encaixar**: Vitrines de produtos de design, cards de equipe/membros, galerias de portfólio criativo e cartões de depoimento detalhado.

### 2. Morphing Popover (`morphing-popover`)
- **Anatomia Visual**: Composto por `MorphingPopover`, `MorphingPopoverTrigger` e `MorphingPopoverContent`. Um botão de ação compacto (ex: "Adicionar nota", "Filtrar", "Compartilhar") que, ao ser acionado, expande geometricamente sua própria cápsula (`layoutId`) para se transformar em um popover flutuante com inputs, checkboxes ou opções de menu, sem sobreposição rígida.
- **Gatilho de Interação**: Clique no botão disparador; fecha ao clicar fora ou via tecla `Escape`.
- **Onde encaixar**: Ações contextuais em tabelas administrativas, botões de busca rápida no topo da aplicação, seletores de tags e botões de compartilhamento social.

### 3. Animated Background (`animated-background`)
- **Anatomia Visual**: Componente wrapper que encapsula múltiplos elementos filhos (botões, links ou cards) que contêm o atributo `data-id`. Renderiza uma pílula de fundo compartilhada com `layoutId` (`absolute inset-0`) que desliza magneticamente entre os itens conforme o usuário interage.
- **Gatilho de Interação**: Hover do mouse (`enableHover={true}`) ou clique de seleção ativa (`defaultValue="..."`).
- **Onde encaixar**: Barras de navegação primárias (Navbar), alternadores de abas (Tabs), filtros de categoria em e-commerce e seletores de período em dashboards analíticos.

### 4. Text Morph (`text-morph`)
- **Anatomia Visual**: Transição tipográfica de nível atômico. Ao alterar a string fornecida via `children`, o componente mapeia os caracteres, mantendo as letras comuns vivas e animando sua transição de posição linear enquanto descarta ou insere novos caracteres com fade e escala orgânicos via mola (`stiffness: 280, damping: 18, mass: 0.3`).
- **Gatilho de Interação**: Reativo a mudanças de estado em tempo real (ex: contadores, status de tarefas, alternância de palavras no Hero).
- **Onde encaixar**: Títulos dinâmicos no Hero, botões de ação com estados mutáveis ("Salvar" → "Salvando..." → "Salvo!"), chips de status de agentes de IA.

### 5. Text Effect (`text-effect`)
- **Anatomia Visual**: Mecanismo de revelação tipográfica com suporte a presets (`blur`, `fade-in-blur`, `scale`, `fade`, `slide`) e segmentação granular por caractere (`char`), palavra (`word`) ou linha (`line`). Cada fragmento entra com atraso sequencial (*staggerChildren*), criando uma cascata cinematográfica com desfoque de movimento. Inclui `aria-hidden` nos fragmentos visuais e um elemento com classe `sr-only` contendo o texto integral para acessibilidade impecável.
- **Gatilho de Interação**: Carregamento da página, gatilho por visibilidade no scroll (`trigger={isInView}`) ou alternância programática.
- **Onde encaixar**: Headline principal do Hero, subtítulos de impacto, declarações de missão em seções institucionais e quotes de clientes em Social Proof.

### 6. Sliding Number (`sliding-number`)
- **Anatomia Visual**: Odômetro numérico de alta precisão. Decompõe números inteiros e fracionários em colunas individuais de dígitos de largura fixa (`w-[1ch]`). Cada coluna contém um trilho vertical com números de 0 a 9 que desliza com física de mola pura (`useSpring`) de acordo com o valor matemático exato do dígito.
- **Gatilho de Interação**: Atualizações no valor numérico (`value: number`).
- **Onde encaixar**: Painéis de precificação (preço mensal vs. anual recalculado), métricas de tração no Hero (ex: "14,892 usuários ativos"), contadores de carrinho de compras e placares em tempo real.

### 7. Progressive Blur (`progressive-blur`)
- **Anatomia Visual**: Barra de desfoque atmosférico com transição suave contínua. Em vez de uma máscara sólida, gera um conjunto configurável de camadas (padrão 8 camadas) aplicando gradientes lineares rotacionados (`direction='top'|'bottom'|'left'|'right'`) com intensidades escalonadas de `backdropFilter: blur(...)`.
- **Gatilho de Interação**: Passivo (acompanha o scroll ou repousa fixo sobre o conteúdo).
- **Onde encaixar**: Rodapés de tela flutuantes, cabeçalhos fixos com efeito de desfoque orgânico, limites superior e inferior de listas roláveis e bordas de carrosséis de imagens.

### 8. Border Trail (`border-trail`)
- **Anatomia Visual**: Um cometa ou feixe luminoso discreto que percorre perfeitamente o contorno perimetral de um container retangular ou arredondado (`rounded-[inherit]`). Utiliza CSS `offset-path: rect(...)` com `offsetDistance` animado de 0% a 100% sob uma máscara composta (`mask-composite: intersect`), garantindo que o brilho se curve com exatidão matemática nas esquinas sem vazar para o centro do elemento.
- **Gatilho de Interação**: Animação contínua em loop (`repeat: Infinity`) ou disparada em hover / foco ativo.
- **Onde encaixar**: Cartão de plano "Mais Popular" na tabela de Pricing, input de busca de IA ativo, badges de destaque de novidades e cards de destaque no Bento Grid.

### 9. Dock (`dock`)
- **Anatomia Visual**: Barra de inicialização inspirada no dock do macOS. Itens organizados horizontalmente em uma barra com cantos arredondados (`rounded-2xl`). À medida que o ponteiro do mouse se aproxima, a distância euclidiana é calculada em tempo real via `MotionValue`, inflando progressivamente a largura e altura do ícone mais próximo e de seus vizinhos adjacentes com mola suave (`mass: 0.1, stiffness: 150, damping: 12`). Inclui tooltip integrado via `DockLabel`.
- **Gatilho de Interação**: Movimento do cursor do mouse ao longo do eixo horizontal do dock (`onMouseMove`).
- **Onde encaixar**: Barra de navegação flutuante inferior em aplicações web, menu de ferramentas rápidas em editores gráficos e atalhos globais de sistemas operacionais na web.

### 10. Magnetic (`magnetic`)
- **Anatomia Visual**: Efeito de atração física onde um elemento (botão, badge ou ícone) é atraído na direção do ponteiro do mouse quando este se aproxima dentro de um raio de ação pré-determinado (`range`, padrão 100px), retornando elasticamente à posição original quando o cursor se afasta.
- **Gatilho de Interação**: Movimento do mouse (`mousemove`) com escopo no próprio elemento (`self`), elemento pai (`parent`) ou viewport (`global`).
- **Onde encaixar**: Botão principal de Call-to-Action (CTA) no Hero, botão flutuante de chat/suporte, ícones de redes sociais e botões de reprodução de vídeo.

### 11. Cursor (`cursor`)
- **Anatomia Visual**: Substitui ou complementa o ponteiro nativo do sistema operacional por um elemento visual dinâmico (uma pílula de texto "Arrastar", ícone de lupa, play de vídeo ou ponto de luz). Desloca-se sincronizado com as coordenadas do mouse amortecido por `useSpring`.
- **Gatilho de Interação**: Movimento do mouse sobre a página ou especificamente restrito a um elemento pai com `attachToParent={true}` (onde o cursor só aparece e substitui o mouse dentro do container do projeto).
- **Onde encaixar**: Carrosséis de imagens interativos, áreas de visualização de vídeo, canvas de desenho e áreas interativas de "clique e arraste".

### 12. Transition Panel & Disclosure (`transition-panel` / `disclosure`)
- **Anatomia Visual**: 
  - *Transition Panel*: Gerencia a transição de visualizações em pilha com `mode="popLayout"`, permitindo trocar painéis filhos (`children[activeIndex]`) com animações de deslizamento ou desfoque sem quebrar o fluxo de layout.
  - *Disclosure*: Primitiva de expansão vertical com medição fluida. Diferente de sanfonas rígidas, expande e contrai o conteúdo interno com física natural de mola e suporte total a atalhos de teclado (`Enter`, `Espaço`).
- **Gatilho de Interação**: Clique no gatilho ou mudança programática de índice (`activeIndex`).
- **Onde encaixar**: Sanfonas de Perguntas Frequentes (FAQ), formulários multi-etapas de checkout/onboarding e alternadores de código (TypeScript / JavaScript / cURL).

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

O Motion Primitives utiliza o pacote oficial moderno **`motion`** (a nova geração consolidada do Framer Motion a partir da v11/v12):

```bash
# Instalação das dependências essenciais
npm install motion react-use-measure lucide-react clsx tailwind-merge
```

Instalação de componentes via CLI oficial do Motion Primitives:
```bash
# Exemplo: Adicionando componentes individuais ao seu projeto
npx motion-primitives@latest add morphing-dialog
npx motion-primitives@latest add animated-background
npx motion-primitives@latest add text-morph
npx motion-primitives@latest add sliding-number
npx motion-primitives@latest add progressive-blur
```

Estrutura de utilitário recomendada (`src/lib/utils.ts`):
```typescript
import { clsx, type ClassValue } from 'clsx';
import { twMerge } from 'tailwind-merge';

export function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs));
}
```

---

### Física de Movimento, Molas & Constantes de Transição

O Motion Primitives fundamenta sua excelência nos seguintes perfis matemáticos de amortecimento:

| Componente | Tipo | Parâmetros de Mola / Duração | Comportamento Perceptivo |
| :--- | :--- | :--- | :--- |
| **Text Morph** | `spring` | `stiffness: 280, damping: 18, mass: 0.3` | Resposta rápida e ágil, com deslizamento cirúrgico de letras |
| **Sliding Number** | `spring` | `stiffness: 280, damping: 18, mass: 0.3` | Rotação inercial como odômetro mecânico Suíço |
| **Dock Item** | `spring` | `stiffness: 150, damping: 12, mass: 0.1` | Inflação elástica ultra-responsiva que segue o ponteiro sem arrasto |
| **Magnetic Effect** | `spring` | `stiffness: 26.7, damping: 4.1, mass: 0.2` | Atração viscosa e magnética suave, simulando campo gravitacional |
| **Morphing Popover** | `spring` | `bounce: 0.1, duration: 0.4` | Expansão de superfície amortecida com micro-rebote imperceptível |
| **Text Effect (Stagger)**| `tween` | `staggerChildren: 0.03` (char) / `0.05` (word) | Cascata sequencial cinematográfica em leitura progressiva |
| **Border Trail** | `linear` | `duration: 5s, repeat: Infinity, ease: 'linear'` | Movimento perimétrico uniforme em velocidade constante |

---

### Receitas de Código Funcional

#### Receita 1: Botão de Ação Dinâmico com `TextMorph` (Feedback de IA/Salvar)
Este padrão substitui spinners de carregamento genéricos por transições de estado fluidas no próprio rótulo do botão.

```tsx
'use client';

import React, { useState } from 'react';
import { TextMorph } from '@/components/motion-ui/text-morph';
import { Loader2, Check, Sparkles } from 'lucide-react';
import { cn } from '@/lib/utils';

type ActionState = 'idle' | 'generating' | 'success';

export function AIActionButton() {
  const [state, setState] = useState<ActionState>('idle');

  const handleClick = () => {
    if (state !== 'idle') return;
    setState('generating');
    setTimeout(() => {
      setState('success');
      setTimeout(() => setState('idle'), 2500);
    }, 1800);
  };

  const labels: Record<ActionState, string> = {
    idle: 'Gerar com Inteligência Artificial',
    generating: 'Sintetizando modelo de dados...',
    success: 'Fluxo concluído com êxito!',
  };

  return (
    <button
      onClick={handleClick}
      disabled={state === 'generating'}
      className={cn(
        'relative inline-flex h-11 items-center justify-center gap-2.5 rounded-xl px-5 text-sm font-medium transition-all duration-300',
        'border border-zinc-950/10 bg-zinc-900 text-zinc-50 shadow-sm hover:bg-zinc-800 dark:border-white/10 dark:bg-zinc-100 dark:text-zinc-950 dark:hover:bg-white',
        state === 'success' && 'border-emerald-500/30 bg-emerald-950/20 text-emerald-400 dark:bg-emerald-500/10 dark:text-emerald-300'
      )}
    >
      {state === 'idle' && <Sparkles className="h-4 w-4 text-amber-400" />}
      {state === 'generating' && <Loader2 className="h-4 w-4 animate-spin text-zinc-400" />}
      {state === 'success' && <Check className="h-4 w-4 text-emerald-400" />}
      
      <TextMorph className="font-medium tracking-tight">
        {labels[state]}
      </TextMorph>
    </button>
  );
}
```

---

#### Receita 2: Navegação com Pílula Elástica via `AnimatedBackground`
Implementação de abas de controle de visualização com rastreamento contínuo de foco.

```tsx
'use client';

import React, { useState } from 'react';
import { AnimatedBackground } from '@/components/motion-ui/animated-background';

const TABS = [
  { id: 'overview', label: 'Visão Geral' },
  { id: 'analytics', label: 'Métricas & Telemetria' },
  { id: 'integrations', label: 'Conexões de API' },
  { id: 'settings', label: 'Configurações' },
];

export function SegmentedTabs() {
  const [activeTab, setActiveTab] = useState('overview');

  return (
    <div className="flex w-fit items-center rounded-xl border border-zinc-200 bg-zinc-100/80 p-1 backdrop-blur-md dark:border-zinc-800 dark:bg-zinc-900/80">
      <AnimatedBackground
        defaultValue={activeTab}
        onValueChange={(id) => id && setActiveTab(id)}
        className="rounded-lg bg-white shadow-xs dark:bg-zinc-800 dark:shadow-none"
        transition={{
          type: 'spring',
          stiffness: 350,
          damping: 25,
        }}
      >
        {TABS.map((tab) => (
          <button
            key={tab.id}
            data-id={tab.id}
            type="button"
            className="px-3.5 py-1.5 text-xs font-medium text-zinc-600 transition-colors hover:text-zinc-950 dark:text-zinc-400 dark:hover:text-zinc-100 data-[checked=true]:text-zinc-950 dark:data-[checked=true]:text-white"
          >
            {tab.label}
          </button>
        ))}
      </AnimatedBackground>
    </div>
  );
}
```

---

#### Receita 3: Card com Expansão Contínua de Imagem via `MorphingDialog`
Este exemplo demonstra a metamorfose espacial completa de um card para um modal detalhado sem corte de imagem.

```tsx
'use client';

import React from 'react';
import {
  MorphingDialog,
  MorphingDialogTrigger,
  MorphingDialogContainer,
  MorphingDialogContent,
  MorphingDialogClose,
  MorphingDialogImage,
  MorphingDialogTitle,
  MorphingDialogSubtitle,
  MorphingDialogDescription,
} from '@/components/motion-ui/morphing-dialog';
import { Plus, X } from 'lucide-react';

export function ProductShowcaseCard() {
  return (
    <MorphingDialog
      transition={{
        type: 'spring',
        stiffness: 260,
        damping: 22,
      }}
    >
      {/* Gatilho em Repouso */}
      <MorphingDialogTrigger className="group relative flex w-full max-w-[280px] flex-col overflow-hidden rounded-2xl border border-zinc-950/10 bg-white p-2.5 text-left transition-shadow hover:shadow-md dark:border-white/10 dark:bg-zinc-900">
        <div className="overflow-hidden rounded-xl">
          <MorphingDialogImage
            src="https://images.unsplash.com/photo-1507473885765-e6ed057f782c?q=80&w=800&auto=format&fit=crop"
            alt="Luminária de Mesa Minimalista"
            className="h-44 w-full object-cover transition-transform duration-500 group-hover:scale-105"
          />
        </div>
        <div className="mt-3 flex items-center justify-between px-1">
          <div>
            <MorphingDialogTitle className="text-sm font-medium text-zinc-900 dark:text-zinc-50">
              Luminária Arcos EB-27
            </MorphingDialogTitle>
            <MorphingDialogSubtitle className="text-xs text-zinc-500 dark:text-zinc-400">
              Design Industrial • 1925
            </MorphingDialogSubtitle>
          </div>
          <span className="flex h-7 w-7 items-center justify-center rounded-lg border border-zinc-200 bg-zinc-50 text-zinc-600 transition-colors group-hover:bg-zinc-100 dark:border-zinc-800 dark:bg-zinc-800 dark:text-zinc-300">
            <Plus className="h-3.5 w-3.5" />
          </span>
        </div>
      </MorphingDialogTrigger>

      {/* Container Expandido em Modal */}
      <MorphingDialogContainer>
        <MorphingDialogContent className="relative flex max-w-lg flex-col overflow-hidden rounded-3xl border border-zinc-950/10 bg-white p-6 shadow-2xl dark:border-white/10 dark:bg-zinc-900">
          <MorphingDialogClose className="absolute right-4 top-4 z-10 flex h-8 w-8 items-center justify-center rounded-full bg-zinc-100 text-zinc-700 transition-colors hover:bg-zinc-200 dark:bg-zinc-800 dark:text-zinc-300">
            <X className="h-4 w-4" />
          </MorphingDialogClose>

          <div className="overflow-hidden rounded-2xl">
            <MorphingDialogImage
              src="https://images.unsplash.com/photo-1507473885765-e6ed057f782c?q=80&w=1200&auto=format&fit=crop"
              alt="Luminária de Mesa Minimalista Detalhe"
              className="h-64 w-full object-cover"
            />
          </div>

          <div className="mt-5 space-y-2">
            <div className="flex items-baseline justify-between">
              <MorphingDialogTitle className="text-xl font-semibold text-zinc-950 dark:text-zinc-50">
                Luminária Arcos EB-27
              </MorphingDialogTitle>
              <span className="text-lg font-mono font-semibold text-zinc-900 dark:text-zinc-100">
                $480
              </span>
            </div>
            <MorphingDialogSubtitle className="text-sm text-zinc-500 dark:text-zinc-400">
              Edição Limitada em Latão Maciço & Madeira Envernizada
            </MorphingDialogSubtitle>
            <MorphingDialogDescription className="pt-2 text-sm leading-relaxed text-zinc-600 dark:text-zinc-300">
              Concebida originalmente em 1925 pelo designer francês Édouard-Wilfrid Buquet, a peça apresenta um mecanismo de contrapeso balanceado que permite ajuste milimétrico em qualquer ângulo espacial sem parafusos de aperto manual.
            </MorphingDialogDescription>
          </div>

          <div className="mt-6 flex gap-3">
            <button className="flex-1 rounded-xl bg-zinc-900 py-2.5 text-sm font-medium text-white transition-opacity hover:opacity-90 dark:bg-zinc-50 dark:text-zinc-900">
              Adicionar à Coleção
            </button>
          </div>
        </MorphingDialogContent>
      </MorphingDialogContainer>
    </MorphingDialog>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma interface moderna referenciando o **Motion Primitives**, a IA deve seguir as regras estritas de integração arquitetural abaixo:

### 1. Declaração de Stack & Dependências
- Declare o pacote oficial `motion` (evite imports legados de `framer-motion` a menos que o projeto especifique versão 10 ou inferior).
- Todos os componentes devem utilizar `'use client';` no topo de seus respectivos módulos quando operando no Next.js App Router.
- Para componentes com medição geométrica em tempo real (*Sliding Number*, *Transition Panel*), declare explicitamente `react-use-measure`.

### 2. Atribuição de Funções de Layout (Regra de Ouro da Sobriedade)
- **Hero Section**: Máximo de 1 efeito tipográfico protagonista (*Text Morph* para títulos mutáveis ou *Text Effect* com preset `fade-in-blur` para a entrada do H1) combinado a 1 micro-interação magnética no botão CTA principal (*Magnetic*).
- **Barra de Navegação / Header**: Utilize exclusivamente *Animated Background* para o indicador de aba selecionada. Evite sobrecarregar o header com bordas giratórias ou brilhos pulsantes.
- **Grades de Cartões (Bento Grid)**: Aplique *Spotlight* sutil com baixa opacidade para guiar o mouse e reserve o *Border Trail* estritamente para o cartão que contém a funcionalidade ou plano central de conversão.
- **Modais e Detalhes**: Substitua modais tradicionais que abrem via fade seco por *Morphing Dialog* ou *Morphing Popover* sempre que houver um elemento disparador visual claro (miniatura ou botão proeminente).

### 3. Acessibilidade & Guardrails de Performance
- Todo componente de texto (*Text Effect*, *Text Morph*) deve manter intacto o texto semântico em `aria-label` ou `<span className="sr-only">`, prevenindo que leitores de tela soletrem cada caractere individual fragmentado pela animação.
- Sempre envolva efeitos contínuos de mouse (*Cursor*, *Spotlight*, *Magnetic*) com suporte a verificação de dispositivo móvel ou suspensão em viewports abaixo de 768px (onde eventos de `mousemove` não existem e degradam a rolagem touch).
