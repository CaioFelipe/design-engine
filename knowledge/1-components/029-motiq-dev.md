---
id: "motiq-dev"
name: "Motiq"
url: "https://motiq.dev/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Deep Ink + Azure + Coral", "Production-First Motion Registry", "Accessible Kinetic Micro-Interactions", "Container Query Data Ergonomics", "Zero Lock-in Editable Source"]
densidade_informacao: "Media a Alta"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Baixo (CSS/Houdini/WAAPI) a Medio (Motion for React)"
stack_frameworks: ["React 19 / 18.3+", "Next.js 15 / 14 (App Router & RSC)", "Tailwind CSS v4", "Motion for React (motion/react)", "Radix UI Primitives", "shadcn/ui CLI Registry"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "Plus Jakarta Sans", "Geist Mono", "JetBrains Mono", "SF Pro Display"]
  paletas_ideais: ["Deep Ink Neutrals (#080c14 a #243249) com Azure Accent (#4f7cff) e Coral Signature (#ff6b5e)", "Cool Porcelain (#f7f9fc a #e8eef7) com Azure (#315fea) e Coral (#e9564a)"]
  combinacoes_recomendadas: ["shadcn/ui", "Radix UI", "Magic UI", "Aceternity UI", "Cult UI", "Motion Primitives"]
  conflitos_esteticos: ["Brutalismo neo-pop com bordas pretas 4px e sombras duras sem blur", "Neumorfismo pastel desbotado", "Glassmorfismo leitoso excessivo sem contraste AA"]
---

# Motiq — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo engenheiro de software **Mahammad Rustamov** (`RMahammad`), o **Motiq** (`motiq.dev`) estabelece um marco de maturidade no ecossistema de componentes animados para React e Next.js. Enquanto a primeira geração de bibliotecas de animação para Tailwind (como Aceternity e Magic UI) concentrou-se primariamente em efeitos visuais de marketing, fundos de canvas e heros de alto impacto cromático, o Motiq adota uma filosofia radicalmente voltada para a **engenharia de produto em produção** (*"Production readiness is the feature"*).

Distribuído como um registro aberto e compatível nativamente com a CLI do `shadcn/ui` (com mais de 100 itens catalogados entre componentes, blocos compostos, primitivas e packs temáticos), o Motiq não entrega pacotes npm "caixa-preta": ele injeta código-fonte limpo, tipado em TypeScript estrito, com boundaries conscientes de React Server Components (`"use client"` pontual) e posse total pelo desenvolvedor.

A assinatura visual e técnica do Motiq é regida por quatro princípios estruturais:

1. **A Identidade Cromática "Deep Ink + Azure + Coral":**
   Ao contrário de interfaces que recorrem ao preto absoluto (`#000000`) provocando achatamento e perda de profundidade, o Dark Mode padrão do Motiq é esculpido sobre uma escala de cinco camadas em tons de tinta azulada profunda (*Deep Ink*):
   - Fundo base da página: `#080c14`
   - Superfície elevada / bandas secundárias: `#0d1420`
   - Cartões e containers de dados (`surface-1`): `#111827`
   - Superfícies elevadas e popovers (`surface-2 / raised`): `#192337`
   - Estados de hover e destaque ativo: `#202d43` e `#243249`
   
   Sobre essa fundação repousa um sistema hierárquico de cores de ação:
   - **Azure Primary (`#4f7cff` no escuro / `#315fea` no claro):** Canaliza a intenção interativa do usuário (foco, botões primários, seleções).
   - **Cyan Secondary / Data (`#22c7d9` no escuro / `#009fb3` no claro):** Suporta fluxos de dados, pipelines e telemetria.
   - **Coral Signature (`#ff6b5e` no escuro / `#e9564a` no claro):** O elemento de assinatura memorável da marca. Nunca é empregado para indicar perigo (para o qual existe o vermelho semântico `#ff5c70`) nem como ruído decorativo constante: o Coral surge em doses cirúrgicas (10%) para destacar pontos de culminância (pull handles de comparação, ignição de frases de destaque, badges de status vitais).
   
   O modo claro (*Light Theme*) não é uma simples inversão mecânica, mas um sistema autônomo em porcelana fria (*Cool Porcelain* `#f7f9fc`) com cinzas azulados que mantêm as razões de contraste WCAG AA auditadas.

2. **Hierarquia de Motores de Animação (Engine Escalation Protocol):**
   O Motiq rejeita a sobrecarga de importar motores pesados indiscriminadamente. A biblioteca aplica uma regra de escalonamento técnico rigorosa:
   - *CSS Nativo & Keyframes GPU:* Entradas simples de opacidade, rotações perpétuas, transformações lineares e transições de hover (custo de runtime nulo).
   - *WAAPI (`motion/mini` animate):* Animações imperativas "one-shot" acionadas por eventos de leitura (como o *Kinetic Emphasis*), gerando markup estático perfeito em SSR sem layout shift.
   - *Motion for React (`motion/react`):* Reservado para físicas de mola (*springs*), rastreamento gestual (drag, hover com inércia), transições de layout compartilhado (`layoutId`) e montagem/desmontagem elástica (`AnimatePresence`).
   - *rAF Integrado com Delta-Time:* Componentes de alta cinemática (como `VelocitySkewFeed` e `OrbitalGallery`) utilizam equações diferenciais amortecidas por tempo discreto com desligamento autônomo (*sleep threshold*), consumindo zero processamento quando o elemento está em repouso ou fora da tela (`useVisibilityPause`).

3. **Ergonomia de Dados por Container Queries (`@container` & `cqi`):**
   Em vez de forçar componentes de dashboard a reagirem à largura global da janela (`viewport`), os blocos do Motiq utilizam Tailwind CSS v4 Container Queries nativas (`@container/kpi`). Um cartão métrico inserido em uma coluna estreita de 180px ajusta seu espaçamento, reduz o tamanho tipográfico via `text-[clamp(1.7rem,14cqi,2.3rem)]` e quebra rótulos inteligentemente, sem quebrar o layout mesmo em monitores Ultrawide 4K.

4. **Acessibilidade Inegociável (WCAG 2.2 AA & Motion Safety):**
   - Suporte mandatório e testado para `prefers-reduced-motion: reduce`: componentes de morphing numérico congelam na contagem final imediata; carrosséis orbitais passam a responder por cliques e teclas direcionais sem transições cinéticas contínuas; loops infinitos pausam instantaneamente.
   - Respeito a leitores de tela em fluxos de IA: componentes como o `AiResponseStream` anunciam apenas mudanças de ciclo de vida (`aria-live="polite"` no início e no fim da geração), sem nunca disparar leituras token-a-token que bloqueariam o sintetizador de voz.
   - Status e direções (como variações de métricas) utilizam simultaneamente cor, glifos SVG e sinais textuais reais (`+` ou o símbolo matemático de subtração `−` U+2212), permanecendo inequívocos em monitores de alto contraste (*Windows Forced Colors Mode*).

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **Interfaces de Inteligência Artificial & LLMs (AI Workspaces & Copilots):**
   Aplicações que lidam com geração de texto em streaming, orquestração de agentes autônomos e execução de chamadas de ferramentas (*tool calling*). O pacote `AI Interface Pack` fornece primitivas prontas para timelines de raciocínio (`AgentRunTimeline`), trilhos de citações com âncoras bidirecionais (`SourceCitationRail`) e caixas de composição de prompts com expansão elástica (`PromptComposer`).
2. **Plataformas de Engenharia de Software, Cloud & DevOps:**
   Ferramentas como consoles de deploy (estilo Vercel, Railway, Supabase), visualizadores de webhooks e inspetores de requisições HTTP (`ApiRequestInspector`, `DeploymentPipeline`, `LiveLogStream`). Os componentes transmitem a sensação de precisão operacional e controle em tempo real.
3. **Dashboards Financeiros, FinTechs & Telemetria Analítica:**
   Painéis executivos que necessitam de números cinéticos com interpolação suave (`KpiNumberMorph`), tabelas com linhas dinâmicas de streaming (`StreamingDataRows`) e estados elegantes de atualização com preservação de layout (`DataRefreshState`).
4. **Aplicações Colaborativas & Multiplayer (Productivity B2B):**
   Sistemas com presença de usuários em tempo real (estilo Figma/Linear), pilhas de avatares com pulso de atividade (`LivePresenceStack`), fluxos de aprovação em cadeia (`ApprovalWorkflow`) e threads de comentários expansíveis (`CommentThread`).
5. **Landing Pages Tecnológicas de Alto Padrão (Developer Marketing):**
   Páginas de apresentação de frameworks e produtos digitais modernos onde títulos dinâmicos (`KineticEmphasis`), heros com expansão por rolagem (`StickyZoomHero`) e painéis de gradiente atmosférico (`AuroraPanel`, `LuminousTopography`) criam uma narrativa memorável sem cair na armadilha de landing pages genéricas geradas por IA.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Neutra e Estrutura Utilitária):**
  Paredes de fundo em Deep Ink (`#080c14` / `#0d1420`), cartões em superfícies discretas (`#111827`) e tipografia nítida neutra com fontes como *Geist Sans* ou *Inter*. Essa camada garante que a interface seja silenciosa, organizada e livre de fadiga cognitiva.
- **30% (Micro-Interações e Cinética de Produto do Motiq):**
  Os blocos funcionais do Motiq: contadores que sofrem transição ao alterar filtros, pipelines que avançam etapas com indicadores de mola suave, cartões com efeito de inclinação controlada e trilhos de log com rolagem virtualizada.
- **10% (Showstoppers de Culminância & Acento Coral de Assinatura):**
  A aplicação do tom Coral (`#ff6b5e`) na palavra-chave destacada do Hero via `KineticEmphasis`; o puxador tátil no comparador de imagens `CompareReveal`; ou a transição dramática de expansão de tela cheia do `StickyZoomHero` na primeira dobra.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Formulários Críticos de Checkout e Telas Bancárias Reguladas:**
  Em etapas de pagamento via cartão de crédito, transferências Pix/SWIFT ou assinaturas contratuais jurídicas, efeitos de rolagem distorcida (`VelocitySkewFeed`) ou transformações cinéticas em labels provocam sensação de instabilidade ou atraso técnico.
- **Tabelas de Auditoria de Altíssima Densidade (Planilhas ERP de 10.000 Linhas):**
  Apesar do excelente desempenho, componentes com padding generoso e transições de entrada individuais em cada linha não substituem uma tabela virtualizada estrita (como TanStack Table com CSS Grid cru) em sistemas onde corretores ou auditores necessitam visualizar 80 linhas simultâneas na tela.
- **Projetos com Suporte Obrigatório a Navegadores Legados sem Suporte a CSS Container Queries ou WAAPI:**
  Aplicações intranet corporativas presas a navegadores desatualizados anteriores a 2023 perderão as capacidades responsivas inteligentes das unidades `@container` e `cqi`.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **"The Rave Party" (Excesso de Coral e Acentos Concorrentes):**
  Utilizar o Coral de assinatura em todos os botões, bordas e ícones da página. O Coral perde completamente seu valor de pontuação hierárquica e transforma a interface em um mostruário berrante. O Coral deve figurar no máximo em 1 ou 2 pontos por tela.
- **Ativação Simultânea de Múltiplos Backgrounds Vetoriais Dinâmicos:**
  Colocar o fundo `LuminousTopography` atrás de um `VelocitySkewFeed` que por sua vez contém cards com `SpotlightCard`. Embora o navegador processe em GPU, a carga cognitiva sobre o usuário se torna insuportável e a leitura do conteúdo é arruinada.
- **Omissão de Classes `tabular-nums` em Elementos Numéricos:**
  Renderizar contadores dinâmicos sem fontes tabulares. O número oscilará horizontalmente a cada dígito, gerando micro-tremores visuais que desqualificam a percepção de produto refinado.
- **Spamming de Regiões `aria-live` em Fluxos Dinâmicos:**
  Configurar leituras acessíveis para cada frame de transição de um contador ou para cada palavra que surge na tela. O leitor de tela continuará falando minutos após a animação ter terminado.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão 10 dos componentes mais expressivos e arquiteturalmente avançados do ecossistema Motiq:

### 1. Kinetic Emphasis (`@motiq/kinetic-emphasis`)
- **Anatomia Visual:** Componente de tipografia cinética projetado especificamente para títulos de heros. Ao carregar ou entrar na viewport, uma frente invisível de ativação varre o texto na ordem de leitura. As palavras comuns surgem em tom neutro suave, enquanto palavras ou expressões envolvidas pela tag semântica `<em>` "ignitam" com elevação de escala física (`scale(1.03) \to scale(1)`), transição para a cor de destaque (`var(--color-accent-text)`) e o desenho progressivo de uma barra de sublinhado brilhante com difusão suave em gradiente.
- **Gatilho de Interação:** Disparo automático na montagem (`play="mount"`), gatilho ao atingir a viewport via `IntersectionObserver` (`play="in-view"`) ou controle imperativo via propriedade `active`.
- **Onde encaixar:** Título principal (`H1`) do Hero de landing pages, anúncios de grandes recursos de produto ou chamadas finais de conversão (CTA principal).

### 2. AI Response Stream (`@motiq/ai-response-stream`)
- **Anatomia Visual:** Terminal de respostas de agentes de IA com cabeçalho contendo o avatar do assistente, badge de status cromático com ícones específicos (pensando, transmitindo, concluído, erro), corpo em Markdown fluido com blocos de código com realce de sintaxe e botão de cópia com feedback de confirmação, caret pulsante suave e trilho inferior expansível de fontes citadas (`Sources Rail`) com navegação cruzada por âncoras bidirecionais.
- **Gatilho de Interação:** Streaming em tempo real conduzido por array de deltas ou texto integral; botões de parada (*Stop*) e repetição (*Retry*).
- **Onde encaixar:** Workspaces de agentes de IA, janelas de chat conversacional corporativo, assistentes embutidos em painéis analíticos.

### 3. KPI Number Morph (`@motiq/kpi-number-morph`)
- **Anatomia Visual:** Cartão métrico avançado construído sob `@container/kpi`. Possui rótulo superior semântico, número central que realiza interpolação contínua e suave entre valores anteriores e novos através de easing de mola, formatação monetária e notação compacta (`3.1M`, `48.2K`), e indicador de tendência com glifo SVG e caractere matemático explícito (`+` ou `−`).
- **Gatilho de Interação:** Reativo a mudanças de estado controlado (`value`), transição automática ao selecionar novos filtros temporais ou alternar abas de período.
- **Onde encaixar:** Linha de KPIs principais no topo de Dashboards, resumos financeiros de faturamento, painéis de saúde de servidores.

### 4. Velocity Skew Feed (`@motiq/velocity-skew-feed`)
- **Anatomia Visual:** Feed de cartões de atividade que reage fisicamente à velocidade de rolagem da página ou container. Ao rolar velozmente, os cartões sofrem uma inclinação elástica lateral (`skewY` ou `skewX`) proporcional à derivada da posição, alongando-se levemente (`scaleY`). Ao cessar o movimento, uma equação de amortecimento elástico ($s'' = k(\text{target} - s) - c \cdot s'$) faz os cartões retornarem ao formato perfeitamente ortogonal com um único overshoot suave. Inclui velocímetro opcional com agulha em gradiente e indicador em `px/s`.
- **Gatilho de Interação:** Rolagem nativa do usuário (wheel, touch ou barra de rolagem). O motor desativa os cálculos quando a energia da mola fica abaixo do limiar ou quando o feed sai da viewport.
- **Onde encaixar:** Feeds de transações em tempo real, galerias verticais de projetos em portfólios, listas de eventos de auditoria em devtools.

### 5. Compare Reveal (`@motiq/compare-reveal`)
- **Anatomia Visual:** Visualizador comparativo "antes e depois" de alta fidelidade. Uma linha divisória vertical com puxador circular no tom Coral de assinatura do Motiq corta duas camadas de mídia via `clip-path`. O puxador persegue a posição do cursor através de uma mola calibrada ($k=140, c=18, \zeta \approx 0.76$), transmitindo sensação de resistência tátil viscosa.
- **Gatilho de Interação:** Mouse move, arraste de toque, duplo clique para retornar a 50%, e suporte completo por teclado (setas com passos de 2% ou 10% com Shift). Executa uma animação de auto-demonstração suave na primeira visualização.
- **Onde encaixar:** Demonstrações de compressão de imagem, comparativos de refatoração de código, renderizadores 3D ou antes/depois de processos de design.

### 6. Deployment Pipeline (`@motiq/deployment-pipeline`)
- **Anatomia Visual:** Bloco de fluxo de engenharia que retrata as etapas de entrega contínua (Build, Test, Security Scan, Containerize, Deploy to Edge). Cada nó possui linhas conectoras dinâmicas com pulsos luminosos indicando tráfego de dados, ícones animados de status e expansão de detalhes em cascata para logs da etapa ativa.
- **Gatilho de Interação:** Progressão automatizada de pipeline ou clique para inspecionar logs de cada nó individual.
- **Onde encaixar:** Centrais de controle de infraestrutura em plataformas SaaS para desenvolvedores, telas de status de CI/CD.

### 7. Orbital Gallery (`@motiq/orbital-gallery`)
- **Anatomia Visual:** Carrossel de mídia em arranjo tridimensional elíptico. Os cartões giram em um anel de perspectiva no espaço 3D, com escala, luminosidade e desfoque calculados matematicamente em função do cosseno do ângulo ($\cos \theta$). Ao ser arrastado ou lançado com o mouse, preserva inércia real limitada a $\pm 6\text{ rad/s}$ com amortecimento exponencial $v \cdot e^{-2.2t}$.
- **Gatilho de Interação:** Arraste com o ponteiro (drag & flick), roda do mouse (wheel), cliques nas cartas periféricas ou teclas direcionais.
- **Onde encaixar:** Galerias de clientes e estudos de caso em páginas institucionais, mostruários de produtos em e-commerce de design.

### 8. Luminous Topography (`@motiq/luminous-topography`)
- **Anatomia Visual:** Fundo decorativo vetorial em SVG puro constituído por curvas de nível topográficas luminosas. As curvas fluem organicamente ao redor de pontos focais configuráveis, afinando suavemente nas imediações da área de segurança central para não prejudicar a legibilidade dos textos em primeiro plano. Totalmente estático sob `prefers-reduced-motion` e renderizado sem qualquer dependência de WebGL ou Canvas.
- **Gatilho de Interação:** Movimento perpétuo suave de ondulação vetorial em GPU, com pausa automática caso a aba fique inativa (`document.hidden`).
- **Onde encaixar:** Fundo de seções de Hero em landing pages técnicas de IA, Cloud e plataformas de dados.

### 9. Live Presence Stack (`@motiq/live-presence-stack`)
- **Anatomia Visual:** Pilha horizontal de avatares com contornos de separação em ângulo e indicador luminoso de pulso de presença. Ao entrar um novo usuário colaborativo, a pilha expande com mola elástica, acomodando o novo avatar com animação de layout suave (`layoutId`) e tooltip com indicador de digitação ou seleção ativa.
- **Gatilho de Interação:** Conexões e desconexões via WebSocket em ambientes multiplayer; hover sobre o avatar para revelar o card de perfil.
- **Onde encaixar:** Barra superior de navegação de editores em tempo real, cabeçalhos de documentos colaborativos, painéis de suporte ativo.

### 10. Sticky Zoom Hero (`@motiq/sticky-zoom-hero`)
- **Anatomia Visual:** Estrutura de abertura cinematográfica para páginas de produto. Um cartão contendo o preview do aplicativo inicia centralizado com bordas arredondadas generosas (`rounded-3xl`) e margens laterais; conforme o usuário rola a página verticalmente, a imagem sofre escala contínua até preencher 100% da viewport (*full-bleed*), o raio de borda interpola suavemente para zero, a vinheta escura se dissipa e legendas explicativas realizam crossfade sincronizado.
- **Gatilho de Interação:** Rolagem controlada com interpolação linear exponencial (`lerp`) calculada em `requestAnimationFrame`.
- **Onde encaixar:** Seção de abertura de landing pages de lançamento de produtos flagship ou grandes atualizações de versão.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

O Motiq utiliza a especificação moderna de registros do `shadcn/ui`. Para adicionar componentes, é necessário um projeto React configurado com Tailwind CSS v4:

```bash
# Inicialização padrão do shadcn (se não configurado)
npx shadcn@latest init

# Instalação direta do componente desejado via namespace oficial do registro
npx shadcn@latest add @motiq/kinetic-emphasis
npx shadcn@latest add @motiq/kpi-number-morph
npx shadcn@latest add @motiq/velocity-skew-feed

# Ou instalação referenciando o repositório GitHub diretamente
npx shadcn@latest add RMahammad/motiq/ai-response-stream
```

**Dependências essenciais do ecossistema:**
- `motion` (anteriormente `framer-motion`, importando primitivas de `motion/react`)
- `clsx` e `tailwind-merge` (através da função utilitária clássica `cn()`)
- `lucide-react` para iconografia vetorial auxiliar

---

### Física de Movimento, Variáveis & Easing Canônicos

O Motiq baseia toda a sua consistência cinética em um conjunto canônico de tokens de movimento definidos em TypeScript e replicados em variáveis CSS nativas:

```typescript
// Tokens canônicos de física do Motiq
export const motionTokens = {
  duration: {
    instant: 0,
    fast: 120,   // Micro-interações, tooltips, tags
    normal: 220, // Diálogos, transições de estado, seletores
    slow: 360,   // Gavetas, painéis expansíveis, heros
  },
  ease: {
    standard: [0.2, 0, 0, 1],   // cubic-bezier(0.2, 0, 0, 1) — desaceleração orgânica
    emphasized: [0.2, 0, 0, 1], // idêntico para consistência visual na curva de saída
  },
  distance: {
    sm: 8,
    md: 16,
    lg: 32,
  },
  stagger: {
    sm: 0.04, // 40ms entre itens adjacentes em listas
    md: 0.08, // 80ms entre grupos estruturais
  },
  spring: {
    gentle: { stiffness: 200, damping: 30 }, // Cartões, overlays, transições de layout
    snappy: { stiffness: 300, damping: 24 }, // Toggles, botões, ícones táteis
  },
} as const;
```

---

### Variáveis de Cor Semântica (Design Tokens)

Adicione as variáveis canônicas do Motiq ao seu arquivo CSS global (ex: `globals.css` com suporte a Tailwind CSS v4):

```css
@layer base {
  :root {
    --color-bg: #f7f9fc;
    --color-bg-elevated: #f0f4f9;
    --color-surface: #ffffff;
    --color-surface-2: #f8fafd;
    --color-surface-hover: #eef3fa;
    --color-border: #dce4ef;
    --color-border-strong: #c5d1e1;
    --color-fg: #101828;
    --color-muted: #667085;
    
    /* Acentos */
    --color-accent: #315fea;
    --color-accent-text: #244fd1;
    --color-secondary-accent: #009fb3;
    --color-signature: #e9564a;
    
    /* Status */
    --color-success: #128a55;
    --color-warning: #b86e00;
    --color-error: #d92d4a;
    
    /* Sombras azuladas frias */
    --shadow-sm: 0 1px 2px rgba(16, 24, 40, 0.06);
    --shadow-md: 0 8px 24px -6px rgba(16, 24, 40, 0.10);
  }

  .dark,
  [data-theme="dark"] {
    --color-bg: #080c14;
    --color-bg-elevated: #0d1420;
    --color-surface: #111827;
    --color-surface-2: #192337;
    --color-surface-hover: #202d43;
    --color-border: #263449;
    --color-border-strong: #354863;
    --color-fg: #f8fafc;
    --color-muted: #9caabd;
    
    /* Acentos */
    --color-accent: #4f7cff;
    --color-accent-text: #7f9fff;
    --color-secondary-accent: #22c7d9;
    --color-signature: #ff6b5e;
    
    /* Status */
    --color-success: #32d583;
    --color-warning: #f6b94a;
    --color-error: #ff5c70;
    
    /* Sombras profundas em azul-tinta */
    --shadow-sm: 0 1px 2px rgba(0, 3, 10, 0.5);
    --shadow-md: 0 8px 24px -6px rgba(0, 3, 10, 0.62);
  }
}
```

---

### Receita de Código Funcional: Componente `KpiNumberMorph` com Container Queries

Abaixo está uma implementação funcional, estrita e autossuficiente do padrão de cartão métrico cinético do Motiq, incorporando Container Queries, formatação tabular, cálculo de acessibilidade sem ruído e interpolação de mola:

```tsx
"use client";

import * as React from "react";
import { motion, useSpring, useTransform } from "motion/react";
import { cn } from "@/lib/utils";

export interface KpiCardProps {
  value: number;
  label: string;
  prefix?: string;
  suffix?: string;
  decimals?: number;
  change?: number;
  changeLabel?: string;
  changeAsPercent?: boolean;
  className?: string;
}

export function KpiNumberMorphCard({
  value,
  label,
  prefix = "",
  suffix = "",
  decimals = 0,
  change,
  changeLabel,
  changeAsPercent = false,
  className,
}: KpiCardProps) {
  // Mola para interpolação suave do número
  const springValue = useSpring(value, {
    stiffness: 200,
    damping: 30,
    mass: 1,
  });

  React.useEffect(() => {
    springValue.set(value);
  }, [value, springValue]);

  // Transforma o valor contínuo da mola em string numérica formatada
  const formattedDisplay = useTransform(springValue, (current) => {
    return `${prefix}${current.toLocaleString(undefined, {
      minimumFractionDigits: decimals,
      maximumFractionDigits: decimals,
    })}${suffix}`;
  });

  const hasChange = typeof change === "number" && change !== 0;
  const isPositive = (change ?? 0) >= 0;
  const changeFormatted = hasChange
    ? `${isPositive ? "+" : "−"}${Math.abs(change!).toLocaleString(undefined, {
        minimumFractionDigits: changeAsPercent ? 1 : 0,
        maximumFractionDigits: changeAsPercent ? 1 : 2,
      })}${changeAsPercent ? "%" : ""}`
    : null;

  // Rótulo completo para leitores de tela calculado uma única vez
  const screenReaderText = `${label}: ${prefix}${value.toLocaleString()}${suffix}${
    changeFormatted ? `, variação ${isPositive ? "positiva" : "negativa"} de ${changeFormatted} ${changeLabel ?? ""}` : ""
  }`;

  return (
    <div
      role="group"
      aria-label={screenReaderText}
      className={cn(
        // @container/kpi: reage à largura da coluna interna, não da janela global
        "@container/kpi flex min-w-0 flex-col gap-1.5 rounded-2xl border border-[var(--color-border)] bg-[var(--color-surface)] p-4 shadow-[var(--shadow-sm)] transition-colors duration-200 hover:border-[var(--color-border-strong)] @[16rem]/kpi:p-5",
        className
      )}
    >
      {/* Rótulo superior */}
      <span className="text-[12px] font-medium tracking-wide uppercase text-[var(--color-muted)] @[16rem]/kpi:text-[12.5px]">
        {label}
      </span>

      {/* Valor numérico em morphing — aria-hidden para não sobrecarregar leitor de tela */}
      <div className="flex items-baseline gap-1" aria-hidden="true">
        <motion.span className="text-[clamp(1.7rem,14cqi,2.3rem)] font-semibold leading-none tracking-tight text-[var(--color-fg)] tabular-nums [font-variant-numeric:tabular-nums]">
          {formattedDisplay}
        </motion.span>
      </div>

      {/* Linha de tendência com glifo SVG e caractere matemático real */}
      {hasChange ? (
        <div
          aria-hidden="true"
          className="mt-1 flex flex-wrap items-center gap-x-1.5 gap-y-0.5 text-[13px] font-medium"
        >
          <span
            className={cn(
              "inline-flex items-center gap-1 whitespace-nowrap rounded-md px-1.5 py-0.5 text-[12px]",
              isPositive
                ? "bg-[color-mix(in_oklab,var(--color-success)_12%,transparent)] text-[var(--color-success)]"
                : "bg-[color-mix(in_oklab,var(--color-error)_12%,transparent)] text-[var(--color-error)]"
            )}
          >
            <svg
              width="12"
              height="12"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              strokeWidth="2.5"
              strokeLinecap="round"
              strokeLinejoin="round"
              className={cn("shrink-0 transition-transform", !isPositive && "rotate-180")}
            >
              <path d="M12 19V5m0 0l-6 6m6-6l6 6" />
            </svg>
            {changeFormatted}
          </span>
          {changeLabel ? (
            <span className="font-normal text-[var(--color-muted)] text-[12px]">
              {changeLabel}
            </span>
          ) : null}
        </div>
      ) : null}
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma nova interface de software que utilize referências e componentes da biblioteca **Motiq**, a IA deve seguir as seguintes diretrizes estritas:

1. **Declaração do Registro e Pré-requisitos:**
   - Adicionar o registro do Motiq na seção de infraestrutura:
     ```markdown
     ### Component Registry
     - Registries: `shadcn/ui`, `@motiq` (`https://motiq.dev/r`)
     - Animation Runtime: `motion/react` (Motion v12 / Framer Motion core)
     - Styling: Tailwind CSS v4 com Container Queries (`@container`)
     ```

2. **Adoção da Paleta de Tokens Deep Ink:**
   - Especificar a escala de 5 superfícies para o tema escuro (`#080c14`, `#0d1420`, `#111827`, `#192337`, `#202d43`), proibindo o uso de preto `#000000` puro para fundos de página ou cartões.
   - Declarar o acento **Azure** (`#4f7cff`) para interações operacionais e o acento **Coral** (`#ff6b5e`) estritamente como *signature tone* reservado para os 10% de maior impacto.

3. **Mapeamento da Regra 60-30-10:**
   - **60%**: Superfícies estáticas e contêineres estruturais em tons de Deep Ink com bordas de 1px em `#263449`.
   - **30%**: Componentes ativos do Motiq para fluxos do produto (`AiResponseStream`, `KpiNumberMorph`, `DeploymentPipeline`, `LivePresenceStack`).
   - **10%**: Efeito protagonista do Hero (`KineticEmphasis` com sublinhado luminoso em Coral ou `StickyZoomHero`).

4. **Diretrizes de Acessibilidade Obrigatórias (Guardrails de Engenharia):**
   - Todos os dados numéricos animados devem conter a classe `tabular-nums` e atributo `aria-hidden="true"`, fornecendo a string textual completa no container pai via `aria-label`.
   - Incluir verificação obrigatória de `prefers-reduced-motion`: transições de morphing devem renderizar diretamente o estado estático resolvido para usuários com sensibilidade vestibular.
   - Proibir o uso de mais de 1 fundo vetorial animado (`LuminousTopography` ou `WorkflowTopologyField`) por página.
