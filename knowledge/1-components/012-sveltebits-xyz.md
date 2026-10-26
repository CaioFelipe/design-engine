---
id: "sveltebits-xyz"
name: "Svelte Bits"
url: "https://sveltebits.xyz/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Creative Coding & WebGL Shaders", "Cyberpunk Kinetic Typography", "Fine-Grained Reactive Micro-Interactions", "Svelte 5 Runes & Spring Physics", "Dark Craft Tactile Surfaces"]
densidade_informacao: "Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Runes/Springs) a Alto (WebGL Shaders/OGL)"
stack_frameworks: ["Svelte 5 (Runes)", "SvelteKit", "Tailwind CSS (v3 & v4)", "TypeScript", "svelte/motion (Spring/Tween)", "OGL (WebGL)", "Three.js (opcional)"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Geist Mono", "JetBrains Mono", "Inter", "Syne", "Space Grotesk"]
  paletas_ideais: ["Deep Space Zinc (Zinc 950 / #09090b)", "Bioluminescent Cyan & Emerald Glow", "Holographic Violet / Prismatic Neon", "High-Contrast Monochrome with Radial Highlights"]
  combinacoes_recomendadas: ["shadcn-svelte (Bits UI)", "Skeleton UI", "Melt UI", "Tailwind CSS v4", "Lucide Svelte"]
  conflitos_esteticos: ["Corporate Memphis pastel infantil", "Neobrutalism cru e estático sem easing", "Material Design 2 com sombras drop-shadow duras e primárias saturadas"]
---

# Svelte Bits — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo engenheiro de software e designer **David Haz** (`@DavidHDev`), autor original do conceituado *React Bits*, o **Svelte Bits** (`sveltebits.xyz` / repositório `DavidHDev/svelte-bits`) é a transposição e evolução técnica das bibliotecas de ponta de Creative Coding para a arquitetura reativa moderna do **Svelte 5**.

Com um acervo superior a **130 componentes animados, shaders WebGL de alto impacto, tipografia cinética e micro-interações táteis**, o Svelte Bits resolve uma carência histórica no ecossistema Svelte: a disponibilidade de elementos de "design de premiação" (estilo Awwwards, FWA e lançamentos da Apple/Linear/Vercel) construídos nativamente para a linguagem, dispensando adaptações improvisadas de bibliotecas React ou hacks pesados de wrappers imperativos.

### Os Quatro Pilares da Assinatura Visual & Técnica

1. **Reatividade Cirúrgica via Svelte 5 Runes (Zero Virtual DOM Overhead)**:
   Em ecossistemas baseados em Virtual DOM (como React), animações atreladas a eventos de alta frequência (movimento do cursor, coordenadas euclidianas, física de atração magnética, scroll suave contínuo) exigem constantes cuidados com re-renderizações acidentais em árvore, funções `useCallback`, refs mutáveis e hooks de memoização. No Svelte Bits, todas as interações são orquestradas pelas novas **Runes do Svelte 5** (`$state`, `$derived`, `$effect`, `$props`):
   - Cada coordenada de mouse atualiza unicamente a propriedade CSS ou a variável de transformação do elemento exato, sem renderizar novamente o componente pai ou os nós adjacentes.
   - O resultado é uma taxa de quadros travada em **60/120 FPS**, com consumo de memória e latência de entrada perceptivelmente inferiores aos equivalentes em frameworks VDOM.

2. **Creative Technology & Shaders WebGL com OGL Ultraleve**:
   Em vez de sobrecarregar o bundle da aplicação com instâncias colossais do Three.js para efeitos bidimensionais ou de pós-processamento, o Svelte Bits utiliza primariamente **OGL** (uma biblioteca WebGL minimalista e de alta performance) e APIs nativas de **Canvas 2D / WebGL2**. Isso viabiliza fundos com profundidade hipnótica:
   - *Aurora* e *Soft Aurora*: gradientes bioluminescentes contínuos calculados por fragment shaders matemáticos de ruído simplex/perlin.
   - *Balatro*: distorções psicodélicas procedurais com rotação de vórtices e modulação cromática inspiradas na atmosfera visual do cultuado jogo indie.
   - *Hyperspeed* & *Liquid Chrome*: túneis estelares de alta aceleração e superfícies cromadas de metal líquido reflexivo com renderização por pixel em tempo real.

3. **Tipografia Cinética de Alta Precisão (Kinetic Typography)**:
   O texto não atua meramente como canal de leitura estática; ele se comporta como organismo responsivo:
   - *Decrypted Text*: decodificação criptográfica progressiva onde glifos aleatórios (ASCII, hex, binário) convergem deterministicamente para os caracteres reais ao scrollar ou receber hover.
   - *Variable Proximity*: cálculo em tempo real da distância euclidiana entre a ponta do cursor e o centro delimitador (*bounding box*) de cada glifo individual de uma fonte OpenType variável, interpolando suavemente os eixos `wght` (peso), `wdth` (largura) ou `slnt` (inclinação).
   - *Split Text & Blur Text*: quebra semântica de frases em nós atômicos de palavras e letras com revelação escalonada (*stagger*) e desfoque gaussiano inverso (`filter: blur(10px)` descendo para `blur(0px)`).

4. **Micro-interações Táteis & Deformação Elástica ("Micro Components")**:
   O Svelte Bits introduz uma categoria especializada de micro-componentes com física de deformação visual (*squash & stretch*):
   - *Sling Button*, *Squish Switch*, *Jelly Radio*, *Pulse Heart* e *Tear Ticket*.
   - Esses componentes utilizam modelos matemáticos de mola amortecida através de `svelte/motion` (`Spring`) para produzir uma sensação tátil orgânica, lembrando borracha, vidro e silicone quando clicados ou arrastados.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários

1. **Plataformas de IA Generativa & Agentes Autônomos em SvelteKit**:
   Aplicações de IA requerem feedback constante de "computação profunda" enquanto o modelo realiza inferência, streaming de tokens ou chamadas de ferramentas. Componentes como *Decrypted Text*, *True Focus*, *Shiny Text* e planos de fundo como *Aurora* ou *Particles* transmitem sofisticação algorítmica e inteligência ativa.
2. **DevTools, Cloud Observability & Cybersec**:
   Para ferramentas de infraestrutura, terminais web e painéis de telemetria, componentes como *Decrypted Text*, *Grid Scan*, *Dot Field*, *Dither* e *Spotlight Card* criam a atmosfera técnica, sóbria e blindada esperada por engenheiros sêniores e operadores de cibersegurança.
3. **Landing Pages de Hardware, Áudio e Tecnologias High-End (Dark Craft)**:
   Produtos físicos sofisticados (computação espacial, fones de estúdio, periféricos customizados, sintetizadores) demandam texturas de metal escovado, vidro translúcido e iluminação posicional. A integração de *Spotlight Card*, *Tilted Card*, *Glass Surface* e *Liquid Chrome* replica digitalmente o acabamento industrial de hardware premium.
4. **Portfólios de Design Engineers, Creative Technologists & Estúdios Web**:
   Sites que precisam comprovar domínio técnico e refinamento estético logo no primeiro segundo de interação, valendo-se de *Circular Gallery*, *Dome Gallery*, *Flowing Menu*, *Variable Proximity* e *Balatro*.
5. **Aplicações Web com Foco Extremo em Eficiência Mobile**:
   Projetos que desejam animações de nível cinematográfico sem o peso de múltiplos bundles pesados, aproveitando a compilação cirúrgica do Svelte 5 e a ausência de runtime virtual.

### Papel no Ritmo Visual (Regra 60-30-10)

- **60% (Fundação Estrutural e Arquitetura Neutra)**:
  Superfícies sóbrias, layout em Bento Grid ou colunas canônicas com tokens de `shadcn-svelte` / `Bits UI` ou Tailwind CSS padrão (`bg-zinc-950`, `border-zinc-800/80`, tipografia `Geist Sans` ou `Inter`, contraste e legibilidade estritos sem ruídos).
- **30% (Camada Tátil e Micro-interações Svelte Bits)**:
  Respostas de feedback direto aos gestos do usuário: botões com micro-elasticidade (*Sling Button*, *Spring Check*), cards que refletem a posição do cursor com feixes radiais de lanterna (*Spotlight Card*), caixas com inclinação tridimensional suave (*Tilted Card*) e navegações contextuais (*Dock*, *Pill Nav*).
- **10% (Showstopper / Efeito Protagonista Único)**:
  Restrito a **apenas um grande efeito de vanguarda por página**:
  - Ou o fundo WebGL na Hero Section (*Aurora*, *Balatro*, *Hyperspeed* ou *Waves*);
  - Ou o título principal em tipografia cinética de impacto (*Decrypted Text* em tamanho display ou *Variable Proximity* interativo).
  *Regra de Ouro*: Nunca empilhe dois efeitos protagonistas na mesma viewport visível.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

1. **Grids Analíticos Densos & Backoffices Operacionais (Data Tables B2B)**:
   Em tabelas financeiras com 500+ linhas, interfaces de conciliação bancária ou painéis hospitalares, o uso de cards com *Spotlight*, textos com decodificação atrasada ou fundos dinâmicos polui a percepção cognitiva do operador e reduz a taxa de processamento de informação.
2. **Fluxos Transacionais Críticos & Checkout Financeiro**:
   Telas de pagamento, campos de cartão de crédito, assinaturas de contratos e formulários de autenticação exigem tempo de resposta determinístico de 0 milissegundos e clareza visual impecável. Textos com efeito de embaralhamento criptográfico ou botões que se deformam elasticamente passam insegurança e infantilizam uma etapa séria.
3. **Páginas sem Observação de Visibilidade (Scroll sem Pausa de Shaders)**:
   Instanciar shaders de WebGL (*Aurora*, *Hyperspeed*, *Balatro*, *Liquid Chrome*) sem acoplar um `IntersectionObserver` que pause o loop de renderização (`cancelAnimationFrame`) quando o elemento rolar para fora da tela drena a bateria de notebooks e aquece processadores de smartphones desnecessariamente.
4. **Acessibilidade Negligenciada (`prefers-reduced-motion`)**:
   Componentes como *Hyperspeed* (túnel com efeito de estroboscópio e aceleração), *Letter Glitch* e *Balatro* podem desencadear crises vestibulares ou fotossensibilidade em usuários vulneráveis. É obrigatório desativar animações contínuas quando o usuário sinalizar preferência por redução de movimento.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):

- **"Shader Carnival"**: Colocar o fundo *Aurora* no Hero, *Liquid Chrome* dentro dos cards do Bento Grid, e *Splash Cursor* seguindo o mouse. O projeto se torna um parque de diversões kitsch e amador, perdendo qualquer respeito profissional.
- **Decrypted Text em Parágrafos Corridos**: Aplicar animação de caracteres criptográficos em blocos de texto explicativo, legendas ou termos de serviço. O usuário quer consumir o conteúdo imediatamente; o efeito deve ser reservado exclusivamente a palavras-chave heroicas, badges de status técnico ou valores numéricos resumidos.
- **Ignorar o Ciclo de Vida do SvelteKit**: Deixar de implementar funções de limpeza em runas `$effect` ao navegar entre rotas (Client-Side Navigation do SvelteKit), mantendo instâncias de WebGL, listeners de `mousemove` ou `window.requestAnimationFrame` ativos em segundo plano e causando severos memory leaks.
- **Raio de Ação Excessivo no Componente Magnet**: Configurar o `Magnet` com alcance maior que 120px, capturando o cursor do usuário quando ele estava apenas tentando passar o ponteiro em direção a outro link, criando a sensação irritante de "ímã invisível desgovernado".

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão destacados **12 componentes essenciais** do ecossistema Svelte Bits:

```
┌────────────────────────────────────────────────────────────────────────┐
│                      SVELTE BITS COMPONENT MATRIX                      │
├──────────────────────┬──────────────────────┬──────────────────────────┤
│   TEXT ANIMATIONS    │     BACKGROUNDS      │     UI & MICRO-UNITS     │
├──────────────────────┼──────────────────────┼──────────────────────────┤
│ 1. Decrypted Text    │ 3. Aurora (WebGL)    │ 6. Spotlight Card        │
│ 2. Variable Proximity│ 4. Balatro (Shader)  │ 7. Dock (Spring Physics) │
│ 12. Split Text       │ 5. Hyperspeed        │ 8. Tilted Card           │
│                      │                      │ 9. Magnet / Lines        │
│                      │                      │ 10. Sling Button / Squish│
│                      │                      │ 11. Magic Bento Grid     │
└──────────────────────┴──────────────────────┴──────────────────────────┘
```

### 1. Decrypted Text (`decrypted-text`)
- **Categoria**: *Text Animations*
- **Anatomia Visual**: Exibe um conjunto de glifos arbitrários em constante mutação (ASCII estendido, símbolos matemáticos, caracteres hexadecimais ou binários). Conforme o temporizador avança, os caracteres são resolvidos da esquerda para a direita (ou aleatoriamente), fixando as letras da frase original com uma transição suave de cor de destaque para a cor primária da tipografia.
- **Gatilho de Interação**: Disparo ao entrar na viewport (`animateOn="view"`) ou na passagem do cursor (`animateOn="hover"`).
- **Onde encaixar na página**: Título principal de Hero de produtos técnicos/DevTools, badges de status de clusters de IA ("STATUS: 128 AGENTS ACTIVE"), e títulos de seções de arquitetura de software.

### 2. Variable Proximity (`variable-proximity`)
- **Categoria**: *Text Animations*
- **Anatomia Visual**: Divide a frase ou parágrafo em spans contendo glifos isolados. Mede a distância espacial (em pixels euclidianos) entre a posição instantânea do mouse e o centróide de cada glifo. Conforme o cursor se aproxima, os eixos de variação da fonte tipográfica (ex: peso `wght` de 100 a 900, largura `wdth` de 75% a 125%) se alteram dinamicamente, gerando uma onda de densidade que segue o dedo ou mouse.
- **Gatilho de Interação**: `mousemove` / `touchmove` contínuo com interpolação suave via `$derived` e Runes do Svelte 5.
- **Onde encaixar na página**: Frase de manifesto criativo no meio da página de apresentação de produto, cabeçalho de portfólio de design engineer ou chamada de impacto no rodapé/CTA.

### 3. Aurora & Soft Aurora (`aurora`)
- **Categoria**: *Backgrounds*
- **Anatomia Visual**: Plano de fundo animado em tela cheia com gradientes de três a cinco cores que se mesclam organicamente em ondas bioluminescentes sem costuras ou blocos duros. Utiliza shaders WebGL via OGL, gerando fluidos luminosos etéreos com ruído procedural de baixa carga computacional.
- **Gatilho de Interação**: Animação em loop contínuo baseada em tempo (`uniform float uTime`), com opções de interação sutil ao movimento do ponteiro.
- **Onde encaixar na página**: Plano de fundo exclusivo da Hero Section de SaaS B2B moderno, produtos de inteligência artificial ou cabeçalho de documentação técnica de luxo.

### 4. Balatro (`balatro`)
- **Categoria**: *Backgrounds*
- **Anatomia Visual**: Efeito psicodélico procedural diretamente inspirado no estilo visual hipnótico das cartas do jogo Balatro. Cria espirais, vórtices de cores quentes e frias, distorções radiais e variações de contraste cromático através de um fragment shader altamente otimizado.
- **Gatilho de Interação**: Auto-play contínuo com controle de velocidade, saturação, frequência de onda e pixelation configuráveis via props reativas.
- **Onde encaixar na página**: Banners de anúncio especial, seções de gamificação, landing pages de entretenimento digital, Web3 de vanguarda ou portfólios autorais expressivos.

### 5. Hyperspeed (`hyperspeed`)
- **Categoria**: *Backgrounds*
- **Anatomia Visual**: Simulação tridimensional de um túnel de velocidade interestelar / cibernética, com linhas de laser que se estendem rumo ao ponto de fuga central, efeito de profundidade focal e aceleração contínua, lembrando o salto para o hiperespaço de naves estelares ou feixes de fibra óptica em altíssima velocidade.
- **Gatilho de Interação**: Auto-play contínuo com opções de aceleração no scroll da página ou aumento de velocidade durante cliques prolongados.
- **Onde encaixar na página**: Hero Section de plataformas de infraestrutura de rede ultrarrápida, bancos de dados em tempo real ou ferramentas de build de alta velocidade.

### 6. Spotlight Card (`spotlight-card`)
- **Categoria**: *UI Components*
- **Anatomia Visual**: Cartão com fundo escuro semi-transparente (`bg-zinc-900/60` com `backdrop-blur-sm`), bordas sutis de 1px e um feixe de luz radial suave posicionado exatamente sob as coordenadas do cursor. O brilho ilumina tanto o fundo quanto a borda do cartão de forma pontual, criando a ilusão tátil de apontar uma lanterna de precisão sobre uma superfície de grafite polido.
- **Gatilho de Interação**: Eventos locais de `mousemove` e `mouseleave`.
- **Onde encaixar na página**: Bento Grid de features principais de um SaaS, cards de planos de preços (Pricing), ou lista de módulos técnicos de um SDK.

### 7. Dock (`dock`)
- **Categoria**: *UI Components*
- **Anatomia Visual**: Barra flutuante de navegação inspirada na Dock do macOS. Ao aproximar o cursor de um ícone, o elemento em foco e os ícones vizinhos aumentam de escala proporcionalmente de acordo com uma curva de distribuição gaussiana. O movimento é amortecido com parâmetros de mola (`Spring` do `svelte/motion`), garantindo retorno instantâneo e orgânico.
- **Gatilho de Interação**: `mousemove` com medição de distância linear no eixo horizontal.
- **Onde encaixar na página**: Navbar flutuante inferior em aplicações web orientadas a ferramentas, painel rápido de atalhos em dashboards operacionais ou navegação alternativa para tablets e desktops.

### 8. Tilted Card (`tilted-card`)
- **Categoria**: *UI Components*
- **Anatomia Visual**: Superfície de cartão com perspectiva 3D configurada (`perspective: 1000px`). Ao mover o mouse sobre o cartão, ele se inclina suavemente nos eixos X e Y acompanhando o ângulo de inclinação do ponto de contato, acompanhado de um reflexo translúcido na camada superior que desliza proporcionalmente à inclinação.
- **Gatilho de Interação**: Hover do mouse e movimento relativo `(offsetX / width, offsetY / height)`.
- **Onde encaixar na página**: Card de produto físico em destaque, exibição de planos "Enterprise / Pro" no topo da tabela de preços, ou apresentação de membros-chave da equipe.

### 9. Magnet & Magnet Lines (`magnet`, `magnet-lines`)
- **Categoria**: *Animations & Effects*
- **Anatomia Visual**: No componente *Magnet*, o botão ou elemento gráfico é atraído fisicamente na direção do cursor do mouse assim que este penetra sua zona de atração gravitacional, desacelerando suavemente de volta à posição de repouso ao afastar o mouse. Já em *Magnet Lines*, uma malha de linhas geométricas orienta seus ângulos vetoriais em direção à coordenada exata do ponteiro.
- **Gatilho de Interação**: Rastreamento de proximidade com interpolação de física elástica.
- **Onde encaixar na página**: Botão principal de conversão (CTA) na Hero Section, ícones interativos de redes sociais no footer, ou malha de linhas interativas em seções divisórias.

### 10. Sling Button & Squish Switch (`sling-button`, `squish-switch`)
- **Categoria**: *Micro Components*
- **Anatomia Visual**: Micro-interações táteis de alta especificidade física. O *Sling Button* se deforma na direção do arraste antes de disparar o clique com rebote elástico. O *Squish Switch* simula uma chave de alternância que sofre compressão física no momento do toggle antes de se expandir com suavidade na posição ativada.
- **Gatilho de Interação**: `mousedown`, `drag` e `click` com amortecimento físico via Runes reativas.
- **Onde encaixar na página**: Controles de alternância de tema (Dark/Light Mode), toggles de planos mensais/anuais em Pricing, e botões de confirmação rápida de ações críticas.

### 11. Magic Bento Grid (`magic-bento`)
- **Categoria**: *UI Components*
- **Anatomia Visual**: Grade modular moderna cujos cartões internos compartilham o contexto da posição do cursor. Quando o mouse percorre a grade, o feixe luminoso transita perfeitamente entre os limites de cartões adjacentes, iluminando as bordas limítrofes sem quebras abruptas de continuidade.
- **Gatilho de Interação**: Rastreamento compartilhado em container pai via Svelte Context ou variáveis reativas.
- **Onde encaixar na página**: Seção central de "Core Features" e "Capabilities" de landing pages de produtos tecnológicos.

### 12. Split Text & Blur Text (`split-text`, `blur-text`)
- **Categoria**: *Text Animations*
- **Anatomia Visual**: Decomposição estrutural de frases em spans encapsulados por linha, palavra ou caractere. Na animação *Blur Text*, cada palavra transita de opacidade 0 com filtro de desfoque gaussiano de 12px e deslocamento vertical negativo para opacidade 100% e nitidez cristalina (`blur: 0px`), criando uma sensação visual cinematográfica de foco óptico de câmera.
- **Gatilho de Interação**: Disparado via `IntersectionObserver` assim que o bloco textual atinge o percentual definido de visibilidade na janela.
- **Onde encaixar na página**: Títulos de depoimentos (Social Proof), citações de imprensa, chamadas de seção e declarações de visão da empresa.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Ambiente

O Svelte Bits foi projetado especificamente para ecossistemas modernos baseados em **Svelte 5** (com suporte total ao SvelteKit) e **Tailwind CSS** (v3 ou v4).

#### Instalação via CLI

A distribuição dos componentes segue o modelo moderno de componentes clonados no repositório local do projeto (adotado pelo ecossistema shadcn), garantindo propriedade total sobre o código-fonte:

```bash
# Método 1: Adicionar componente diretamente via shadcn CLI (suporta svelte-bits registry)
pnpm dlx shadcn@latest add https://sveltebits.xyz/r/spotlight-card.json
pnpm dlx shadcn@latest add https://sveltebits.xyz/r/aurora.json
pnpm dlx shadcn@latest add https://sveltebits.xyz/r/decrypted-text.json

# Método 2: Inicializar e gerenciar via jsrepo
pnpm dlx jsrepo init https://sveltebits.xyz/r
pnpm dlx jsrepo add spotlight-card
pnpm dlx jsrepo add decrypted-text
```

#### Dependências Nucleares

No arquivo `package.json` de um projeto SvelteKit, assegure-se de possuir:

```json
{
  "dependencies": {
    "clsx": "^2.1.1",
    "tailwind-merge": "^2.5.4",
    "lucide-svelte": "^0.454.0",
    "ogl": "^1.0.11"
  },
  "devDependencies": {
    "@sveltejs/kit": "^2.6.0",
    "svelte": "^5.0.0",
    "tailwindcss": "^3.4.14",
    "typescript": "^5.6.3"
  }
}
```

> [!NOTE]
> A biblioteca **OGL** é necessária apenas para os componentes que operam WebGL Shaders (*Aurora*, *Hyperspeed*, *Balatro*, *Liquid Chrome*, *Waves*). Componentes de tipografia e UI utilizam exclusivamente Svelte nativo e Tailwind.

#### Utilitário de Classes (`cn`)

Em `src/lib/utils.ts`:

```typescript
import { type ClassValue, clsx } from "clsx";
import { twMerge } from "tailwind-merge";

export function cn(...inputs: ClassValue[]): string {
  return twMerge(clsx(inputs));
}
```

---

### Física de Movimento: Runes do Svelte 5 e `svelte/motion`

Diferente do React Bits que depende do motor Framer Motion, o Svelte Bits baseia sua cinemática nas primitivas reativas do Svelte 5 e na classe `Spring` de `svelte/motion`:

```typescript
import { Spring } from "svelte/motion";

// Configuração canônica de Spring Physics para micro-interações táteis
const coords = new Spring(
  { x: 0, y: 0 },
  {
    stiffness: 0.15, // Rigidez da mola (quanto maior, mais rápida a resposta)
    damping: 0.75,   // Amortecimento (evita oscilação infinita e traz parada suave)
    precision: 0.001 // Limite de corte numérico para economizar ciclos de CPU
  }
);
```

#### Parâmetros Canônicos de Interação

| Tipo de Componente | Mola (`stiffness`) | Amortecimento (`damping`) | Curva Easing / CSS Equivalente |
| :--- | :--- | :--- | :--- |
| **Magnet Button** | `0.18` | `0.65` | `cubic-bezier(0.25, 1, 0.5, 1)` |
| **Dock Icon Hover** | `0.22` | `0.70` | `cubic-bezier(0.34, 1.56, 0.64, 1)` (elástica) |
| **Spotlight Card Glow** | `0.30` | `0.85` | `cubic-bezier(0.16, 1, 0.3, 1)` |
| **Decrypted Text Interval**| N/A | N/A | Intervalo linear de 30ms a 50ms por iteração |
| **Blur Text Stagger** | N/A | N/A | `cubic-bezier(0.2, 0.8, 0.2, 1)` com 60ms delay |

---

### Receita de Código 1: Componente `SpotlightCard.svelte` com Svelte 5 Runes

Abaixo está a implementação de nível de produção do componente **Spotlight Card**, destacando o uso das novas Runes (`$state`, `$props`) e vinculação direta de variáveis CSS:

```svelte
<!-- src/lib/components/svelte-bits/SpotlightCard.svelte -->
<script lang="ts">
  import { cn } from "$lib/utils";
  import type { Snippet } from "svelte";

  interface Props {
    children?: Snippet;
    class?: string;
    spotlightColor?: string;
    spotlightRadius?: number;
  }

  // Declaração de propriedades via Rune $props() do Svelte 5
  let {
    children,
    class: className = "",
    spotlightColor = "rgba(255, 255, 255, 0.08)",
    spotlightRadius = 320
  }: Props = $props();

  // Estados reativos internos via Rune $state()
  let mouseX = $state(0);
  let mouseY = $state(0);
  let isHovered = $state(false);
  let cardElement: HTMLDivElement | null = $state(null);

  function handleMouseMove(e: MouseEvent) {
    if (!cardElement) return;
    const rect = cardElement.getBoundingClientRect();
    mouseX = e.clientX - rect.left;
    mouseY = e.clientY - rect.top;
  }

  function handleMouseEnter() {
    isHovered = true;
  }

  function handleMouseLeave() {
    isHovered = false;
  }
</script>

<div
  bind:this={cardElement}
  onmousemove={handleMouseMove}
  onmouseenter={handleMouseEnter}
  onmouseleave={handleMouseLeave}
  class={cn(
    "relative overflow-hidden rounded-2xl border border-zinc-800/80 bg-zinc-950/80 p-6 transition-colors duration-300",
    className
  )}
>
  <!-- Camada de Iluminação Radial Dinâmica (Spotlight) -->
  <div
    class="pointer-events-none absolute -inset-px transition-opacity duration-300"
    style:opacity={isHovered ? 1 : 0}
    style:background="radial-gradient({spotlightRadius}px circle at {mouseX}px {mouseY}px, {spotlightColor}, transparent 80%)"
  ></div>

  <!-- Borda Reflexiva Suave com Máscara Gradiente -->
  <div
    class="pointer-events-none absolute -inset-px rounded-2xl border border-white/20 transition-opacity duration-300"
    style:opacity={isHovered ? 0.6 : 0}
    style:mask-image="radial-gradient({spotlightRadius * 0.75}px circle at {mouseX}px {mouseY}px, black, transparent)"
    style:-webkit-mask-image="radial-gradient({spotlightRadius * 0.75}px circle at {mouseX}px {mouseY}px, black, transparent)"
  ></div>

  <!-- Conteúdo do Cartão -->
  <div class="relative z-10">
    {@render children?.()}
  </div>
</div>
```

---

### Receita de Código 2: Componente `DecryptedText.svelte` com Runes & Timer Reativo

Abaixo está a implementação estrutural completa de **Decrypted Text**, utilizando `$effect` para orquestração precisa do ciclo de vida e limpeza de temporizadores:

```svelte
<!-- src/lib/components/svelte-bits/DecryptedText.svelte -->
<script lang="ts">
  import { cn } from "$lib/utils";

  interface Props {
    text: string;
    speed?: number;
    maxIterations?: number;
    sequential?: boolean;
    revealDirection?: "start" | "end" | "center";
    characters?: string;
    class?: string;
    encryptedClass?: string;
  }

  let {
    text,
    speed = 40,
    maxIterations = 10,
    sequential = true,
    revealDirection = "start",
    characters = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz!@#$%^&*()_+~`|}{[]:;?><,./-=",
    class: className = "",
    encryptedClass = "text-emerald-400 font-mono"
  }: Props = $props();

  let displayText = $state(text);
  let isHovered = $state(false);
  let iteration = $state(0);
  let isAnimating = $state(false);

  function getRandomChar() {
    return characters[Math.floor(Math.random() * characters.length)];
  }

  function scramble() {
    if (isAnimating) return;
    isAnimating = true;
    iteration = 0;

    const interval = setInterval(() => {
      displayText = text
        .split("")
        .map((char, index) => {
          if (char === " ") return " ";
          
          if (sequential) {
            if (index < iteration) {
              return text[index];
            }
          } else {
            if (iteration >= maxIterations) {
              return text[index];
            }
          }
          return getRandomChar();
        })
        .join("");

      iteration += 1;

      if (iteration > (sequential ? text.length : maxIterations)) {
        clearInterval(interval);
        displayText = text;
        isAnimating = false;
      }
    }, speed);

    return () => clearInterval(interval);
  }

  // Efeito disparado na montagem ou na alteração do texto via Runes
  $effect(() => {
    const cleanup = scramble();
    return () => {
      cleanup?.();
    };
  });
</script>

<!-- svelte-ignore a11y_no_static_element_interactions -->
<span
  class={cn("inline-block cursor-default select-none", className)}
  onmouseenter={() => scramble()}
>
  {#each displayText.split("") as char, i}
    <span class={char !== text[i] ? encryptedClass : ""}>
      {char}
    </span>
  {/each}
</span>
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao arquitetar um novo projeto fundamentado em **Svelte 5 / SvelteKit** utilizando o **Svelte Bits**, a Inteligência Artificial deve declarar e respeitar as seguintes diretrizes de engenharia e governança de design:

### 1. Declaração de Stack & Runes Paradigm
- **Versão Mandatória**: Svelte 5 com modo de Runes (`$state`, `$derived`, `$props`, `$effect`). É estritamente proibido o uso da sintaxe legada de Svelte 3/4 (`export let`, `$: reatividade`, `beforeUpdate`).
- **Framework Web**: SvelteKit com Server-Side Rendering (SSR) consciente. Shaders e componentes que tocam APIs de navegador (`window`, `document`, `WebGLRenderingContext`) devem ser encapsulados por `$effect` ou checados via `browser` de `$app/environment`:
  ```svelte
  <script lang="ts">
    import { browser } from '$app/environment';
    
    $effect(() => {
      if (browser) {
        // Inicialização de Shaders OGL / WebGL
      }
    });
  </script>
  ```

### 2. Estrutura Canônica de Diretórios
```
src/
├── lib/
│   ├── components/
│   │   ├── ui/                    # Componentes base (shadcn-svelte / Bits UI)
│   │   │   ├── button.svelte
│   │   │   ├── card.svelte
│   │   │   └── dialog.svelte
│   │   └── svelte-bits/           # Componentes de alto impacto do Svelte Bits
│   │       ├── backgrounds/
│   │       │   ├── Aurora.svelte
│   │       │   └── Balatro.svelte
│   │       ├── text/
│   │       │   ├── DecryptedText.svelte
│   │       │   └── VariableProximity.svelte
│   │       └── ui/
│   │           ├── SpotlightCard.svelte
│   │           ├── Dock.svelte
│   │           └── TiltedCard.svelte
│   └── utils.ts                   # Utilitário cn (clsx + tailwind-merge)
```

### 3. Governança de Performance & Limpeza de Memória
- **Pausa Automática fora da Viewport**: Qualquer componente de fundo baseado em Canvas ou WebGL (*Aurora*, *Hyperspeed*, *Waves*) DEVE conter um `IntersectionObserver`. Quando o container da seção atingir `intersectionRatio === 0`, o loop `requestAnimationFrame` deve ser cancelado imediatamente.
- **Limpeza no `$effect`**: Todo listener adicionado ao `window` (`resize`, `scroll`, `mousemove`) DEVE retornar sua respectiva função de remoção (`removeEventListener`) no retorno da Rune `$effect`.

### 4. Acessibilidade Mandatória (WCAG AAA)
- Sempre honrar `prefers-reduced-motion`. O blueprint deve prever uma classe auxiliar que desative animações de shader e renderize um gradiente CSS estático:
  ```css
  @media (prefers-reduced-motion: reduce) {
    .svelte-bits-shader {
      display: none !important;
    }
    .svelte-bits-fallback {
      display: block !important;
    }
  }
  ```

### 5. Checklist de Dosagem Estética (Regra 60-30-10)
- [ ] **Apenas 1 Showstopper por Viewport**: Se o Hero possui *Aurora* no fundo, o título é sóbrio ou apenas com *Shiny Text* sutil. Se o título usa *Decrypted Text* em tamanho display, o fundo deve ser um grid estático ou neutro escuro (`bg-zinc-950`).
- [ ] **Consistência de Raios de Borda**: Padronizar `rounded-2xl` (16px) ou `rounded-3xl` (24px) para todos os cartões interativos do Bento Grid.
- [ ] **Tipografia Monoespaçada de Apoio**: Acompanhar efeitos de *Decrypted Text* e métricas de infraestrutura com fontes consagradas como `Geist Mono` ou `JetBrains Mono`.
