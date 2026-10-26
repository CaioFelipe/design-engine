---
id: "originkit-sections"
name: "OriginKit Sections"
url: "https://www.originkit.dev/sections"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Modern Luminescent SaaS", "Dark Craft Sections", "Motion-Driven Landing Blocks", "AI-Native Component Architecture"]
densidade_informacao: "Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Framer Motion / CSS Grid) a Alto (quando acoplado a 3D Canvas / Tunnel Shaders)"
stack_frameworks: ["React 19", "Next.js 15/16 (App Router)", "Tailwind CSS v3/v4", "Motion 12 (motion/react / framer-motion)", "Radix UI", "Lucide React", "Framer Code Components", "OriginKit CLI & MCP Server"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "Plus Jakarta Sans", "SF Pro Display", "JetBrains Mono"]
  paletas_ideais: ["Obsidian & Zinc Dark (#0f0f10, #141415, #1e1e1f)", "Electric Indigo & Violet (#6366f1, #8b5cf6)", "Pure Luminescent White (#ffffff, #f7f7f8)", "Emerald & Cyan Accents (#10b981, #06b6d4)"]
  combinacoes_recomendadas: ["shadcn/ui", "Magic UI", "Cult UI", "Spell UI", "Aceternity UI", "21st.dev"]
  conflitos_esteticos: ["Brutalismo cru sem suavização", "Corporate Memphis bidimensional ingênuo", "Skeuomorfismo pesado pré-iOS 7", "Neomorfismo opaco de baixo contraste"]
---

# OriginKit Sections — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **OriginKit** (`originkit.dev`) representa uma evolução decisiva no ecossistema moderno de engenharia de interface frontend: a transição de coleções de micro-componentes isolados (como botões soltos ou inputs atômicos) para **macro-blocos de arquitetura de landing page inteiramente orquestrados** (*Landing Page Engineering*). Enquanto bibliotecas convencionais forçam desenvolvedores e designers a costurar manualmente dezenas de cartões, transições de scroll e tipografias descompassadas, o catálogo **OriginKit Sections** entrega bandas completas de interface — Hero, Bento Grid, Features, Pricing, Testimonials, FAQ, Call to Action e Footers — já dotadas de coerência cenográfica, física de movimento integrada e responsividade nativa.

A assinatura visual e técnica do OriginKit Sections fundamenta-se em quatro pilares singulares:

1. **A Alma "Dark Craft & Luminescent Precision"**:
   As seções do OriginKit são meticulosamente esculpidas sobre uma escala cromática escura refinada, ancorada no tom de fundo proprietário `#0f0f10` com elevações estruturadas em camadas táteis:
   - Superfície base e corpo de cartões: `bg-[#141415]` e `bg-[#161616]`.
   - Painéis elevados e cabeçalhos de tabela: `bg-[#1e1e1f]` e `bg-[#222425]`.
   - Divisões e molduras de precisão sub-pixel: bordas sólidas em `border-[#373839]` e `border-[#3d3f3f]`, reforçadas por realces internos sutis (`shadow-[inset_0px_0.5px_0px_0px_rgba(255,255,255,0.09)]`).
   - Essa hierarquia impede que temas escuros pareçam blocos pretos indistintos, conferindo uma tridimensionalidade luxuosa e sóbria que remete aos padrões de design de ponta do Vercel, Linear e Raycast.

2. **Composição Hierárquica em Três Níveis (Atomic ➔ Section ➔ Template)**:
   A genialidade do ecossistema reside no acoplamento inteligente de micro-efeitos cinéticos dentro de macro-seções. Em vez de criar seções com ilustrações estáticas genéricas, um bloco como o `Hero 03` incorpora internamente uma primitiva como o `Gallery Tunnel` (túnel 3D com profundidade de perspectiva em WebGL/CSS), e uma seção como o `Pricing 04` integra nativamente o micro-componente `Rolling Letters` para rolagem mecânica e contínua dos valores monetários na alternância mensal/anual.

3. **Arquitetura Dupla: Código Nativo React/Next.js e Framer Visual**:
   Diferente de repositórios que favorecem exclusivamente código ou exclusivamente design visual, o OriginKit foi projetado com uma arquitetura bivalente:
   - **React / Next.js**: Componentes escritos em TypeScript rigoroso, compatíveis com React 19 e Next.js App Router (com diretiva `"use client"` estrita onde há estado ou física de animação), utilizando `motion/react` (Framer Motion v12) e classes Tailwind utilitárias.
   - **Framer Component Bridge**: Cada bloco pode ser copiado diretamente para o Framer (`Insert → Code → New Component`), expondo propriedades de controle visual no painel lateral direito (*Property Controls*), permitindo que designers alterem títulos, gradientes, raios de borda e cadências de animação sem tocar no código-fonte.

4. **Distribuição Nativa por CLI e Protocolo MCP (Model Context Protocol)**:
   O OriginKit rompe com a lentidão do copy-paste manual na web ao oferecer:
   - CLI shadcn-compatible: Comandos como `npx originkit@latest add hero-03` ou `bunx --bun originkit@latest add pricing-04` que baixam automaticamente o componente, suas dependências e atualizam os aliases do projeto de acordo com o `components.json`.
   - Servidor MCP Ativo (`https://mcp.originkit.dev/mcp`): Permite que agentes autônomos de IA (como Claude Desktop, Claude Code ou Cursor) consultem em tempo real o catálogo de seções disponíveis, leiam a árvore de nós e insiram blocos de código completos diretamente na estrutura de rotas do projeto.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários
1. **Landing Pages de SaaS B2B & Ferramentas para Desenvolvedores (DevTools)**:
   Para empresas de computação em nuvem, observabilidade, bancos de dados distribuídos e APIs modernas, as seções de Bento Grid e Hero com estética dark craft comunicam poder computacional, segurança e excelência de engenharia logo na primeira dobra visual.
2. **Startups de Inteligência Artificial & Agentes Autônomos**:
   Interfaces de modelos fundacionais, geradores criativos e plataformas de orquestração de IA encontram nas seções com efeitos luminescentes (como auroras de fundo, feixes cibernéticos e tipografia cinética) a atmosfera futurista ideal para demonstrar disrupção tecnológica.
3. **Páginas de Lançamento de Produto (Waitlist & Product Launch)**:
   Seções compactas de Call to Action (`cta-01`, `cta-04`) com captura instantânea de email, badges de contagem regressiva e efeitos táteis de hover geram taxas elevadas de conversão em campanhas de pré-venda e betas fechados.
4. **Portfólios de Agências Digitais & Creative Technologists**:
   Estúdios de design e consultorias de engenharia de software utilizam os blocos de galeria (`hero-03` com túnel 3D, carrosséis de testemunhos e grades de cases) para apresentar trabalhos com impacto cinematográfico sem precisar reinventar o pipeline de animação do zero.
5. **Páginas de Precificação e Checkout Corporativo**:
   A transição suave entre planos mensais e anuais nas seções `pricing-01` e `pricing-04` reduz o atrito cognitivo do comprador corporativo, destacando limites de assentos, SLAs e tiers enterprise em uma grade bento legível.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Estrutural das Seções)**:
  A espinha dorsal é composta pela geometria e espaçamentos utilitários do Tailwind CSS: containeres padronizados (`max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20 lg:py-32`), fundos escuros profundos (`bg-[#0f0f10]`), tipografia neutra de alta legibilidade (`Geist Sans` ou `Inter` com tracking negativo `tracking-[-0.02em]` a `tracking-[-0.03em]`) e bordas sólidas em escala neutra (`border-[#373839]`).
- **30% (Micro-interações de Seção & Feedback Dinâmico)**:
  A camada de fluidez operacional: alternância animada de abas e toggles de preço com `motion.div layoutId`, acordeões de FAQ com expansão fluida de altura (`height: auto`), badges de novidades com pulsação suave e hovers em cartões bento com realce de borda (`border-white/20`).
- **10% (Macro-Showstopper por Dobra)**:
  Exatamente **um** efeito protagonista por macro-bloco da página:
  - No Hero: O túnel de perspectiva 3D (`gallery-tunnel`) ou o campo de partículas orbitais.
  - No Bento Grid: Um único cartão interativo com canvas reativo ou visualizador de código ao vivo.
  - No CTA Final: A aura luminescente com gradiente radial em rotação lenta. Jamais colocar múltiplos showstoppers disputando a atenção na mesma tela.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Dashboards Operacionais Internos e Tabelas Densas de ERP**:
  Seções completas de landing page com alturas generosas (`py-28`) e animações de scroll de entrada tornam-se obstáculos pesados se inseridas dentro de painéis administrativos, sistemas de backoffice ou consoles analíticos onde a densidade de dados e o tempo de resposta instantâneo são prioritários.
- **Fluxos Finais de Checkout Transacional e Pagamento**:
  Telas de inserção de cartão de crédito e faturamento bancário demandam zero distração. A introdução de planos de fundo com partículas, carrosséis infinitos ou elementos 3D em rotação causa desconfiança, dispersão do pagador e aumenta o abandono de carrinho.
- **Aplicações Estritamente Utilitárias sem Aceleração Gráfica de GPU**:
  Terminais industriais embarcados, quiosques legados ou navegadores móveis sob modo de ultra-economia de energia podem engasgar com múltiplas instâncias de Framer Motion e canvas WebGL rodando simultaneamente.
- **Projetos com Diretrizes Severas de Acessibilidade sem Gestão de Movimento Reduzido**:
  O uso inadvertido de seções como `hero-03` ou `hero-46` sem checagem de `window.matchMedia('(prefers-reduced-motion: reduce)')` pode provocar náusea visual em usuários com sensibilidade vestibular.

### ⚠️ Erros Comuns de Exagero ("AI Slop" & Poluição Visual):
- **Empilhamento de Efeitos Contínuos em Cascata**: Colocar um Hero com túnel 3D, seguido por um Bento Grid com partículas cintilantes, seguido por um Pricing com aurora gradiente pulsante. Isso destrói a elegância da interface e transforma a landing page em uma "árvore de natal" tecnológica amadora.
- **Duração de Transição Excessiva em Elementos de Leitura**: Configurar animações de entrada de texto no Hero com durações superiores a `0.8s` ou atrasos acumulados (*stagger*) que forçam o visitante a esperar 2 segundos para conseguir ler a proposta de valor principal.
- **Inconsistência de Raios de Borda**: Misturar seções do OriginKit com `rounded-[14px]` e `rounded-[20px]` com componentes externos que utilizam cantos retos ou raios minúsculos de `rounded-sm`. O sistema do OriginKit pressupõe raios generosos e contínuos (`rounded-xl` a `rounded-2xl`).

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Macro-Seções)

Abaixo estão 10 das seções e blocos compostos mais emblemáticos do registro oficial do **OriginKit Sections**:

### 1. Hero 03 — Tunnel Perspective Showcase (`hero-03`)
- **Anatomia Visual**: Macro-seção de Hero dominada por uma galeria em túnel de perspectiva tridimensional (`gallery-tunnel`) que converge visualmente para o centro da tela. Acima do túnel repousa uma badge com iluminação sutil ("Introducing v2.0"), um título imponente com tracking comprimido (`text-5xl lg:text-7xl font-semibold tracking-[-0.04em]`), subtítulo em tom grafite neutro (`text-[#a1a1aa]`) e um par de botões de conversão (primário sólido e secundário com borda e ícone).
- **Gatilho de Interação**: Animação de entrada escalonada ao carregar a página; o túnel 3D responde continuamente ao movimento do mouse ou rolagem da página com aceleração elástica.
- **Onde encaixar**: Primeira dobra absoluta de landing pages institucionais de alta tecnologia e produtos digitais inovadores.

### 2. Hero 19 — Cinematic AI Headline & Interactive Badges (`hero-19`)
- **Anatomia Visual**: Hero focado em tipografia cinética de altíssimo contraste e presença minimalista. O headline combina texto branco com palavras-chave envoltas em gradientes radiais suaves e uma badge flutuante interativa com avatar stack de usuários ativos. Na parte inferior da seção, repousa um mockup de produto com efeito de inclinação 3D e borda luminescente de 1px.
- **Gatilho de Interação**: Revelação progressiva de palavras (*text-reveal*) via Framer Motion com `staggerChildren: 0.08`, e efeito de elevação no mockup ao rolar a página para baixo.
- **Onde encaixar**: Hero de startups de inteligência artificial generativa, plataformas de automação e ferramentas de produtividade.

### 3. Hero 46 — Quantum Science Particle Field (`hero-46`)
- **Anatomia Visual**: Hero de estética profunda com um campo de partículas em grade nodal ou hélice quântica que se expande por trás dos textos principais. Linhas tênues conectam os nós de dados conforme a GPU calcula as distâncias euclidianas em tempo real, gerando uma atmosfera de laboratório de pesquisa ou infraestrutura computacional avançada.
- **Gatilho de Interação**: O campo de partículas reage à proximidade do cursor com repulsão vetorial suave e amortecimento dinâmico.
- **Onde encaixar**: Hero para DevTools, bancos de dados em nuvem, plataformas de segurança cibernética e deep tech.

### 4. Pricing 04 — Bento-Tier Dynamic Matrix (`pricing-04`)
- **Anatomia Visual**: Seção de precificação estruturada no formato de grade Bento. Possui um controle centralizado de alternância Mensal/Anual que ativa um badge de economia ("Save 20%"). O cartão principal ("Pro / Growth") ganha destaque através de um contorno luminescente, tag de "Mais Popular", e os valores numéricos são animados pelo micro-componente `Rolling Letters`, rolando verticalmente como os dígitos de um hodômetro analógico de precisão.
- **Gatilho de Interação**: Clique no seletor de ciclo de cobrança (`onClick`), disparo de micro-animações táteis nos botões e realce radial nos cartões ao passar o cursor (`group-hover`).
- **Onde encaixar**: Seção de conversão e planos de assinatura posicionada logo antes do FAQ ou rodapé final.

### 5. Pricing 01 — Clean 3-Tier Enterprise Comparison (`pricing-01`)
- **Anatomia Visual**: Layout clássico e balanceado de três colunas (Starter, Business, Enterprise) com cards delimitados por bordas `#373839`. Cada coluna apresenta hierarquia clara com título do plano, descrição do público-alvo, preço em destaque, lista com ícones de verificação SVG e botão de chamada de largura total com transição de opacidade no hover.
- **Gatilho de Interação**: Hover com leve translação vertical negativa (`translate-y-[-4px]`) e realce de borda com transição CSS suave de 200ms.
- **Onde encaixar**: SaaS B2B com modelo comercial previsível e planos voltados a pequenas e médias empresas.

### 6. Bento Grid Feature Matrix — Modular Software Showcase
- **Anatomia Visual**: Grade bento responsiva composta por cartões de proporções variadas (16:9, 16:10, 4:3) organizados em colunas flexíveis. Cada célula do bento encapsula uma funcionalidade real: um cartão exibe um terminal de código interativo, outro mostra métricas em tempo real com gráfico em sparkline SVG, e um terceiro exibe avatares colaborativos.
- **Gatilho de Interação**: Efeito spotlight radial acoplado às coordenadas `(clientX, clientY)` relativas a cada cartão individual, iluminando suavemente a moldura interna conforme o mouse se desloca.
- **Onde encaixar**: Segunda ou terceira dobra da landing page, imediatamente após o Hero e os logos de clientes.

### 7. Testimonials 01 — Infinite Marquee Review Board (`testimonials-01`)
- **Anatomia Visual**: Seção de prova social montada como um carrossel de rolagem contínua infinita (*infinite marquee*), dividida em duas faixas horizontais que se movem em direções opostas. Os cartões possuem fundo escuro translúcido com `backdrop-blur-md`, foto de perfil em alta resolução, nome, cargo, logo da empresa do cliente e texto com citação curta. As extremidades laterais contam com máscaras gradientes de desvanecimento (*linear-gradient mask*) para ocultar o corte abrupto na tela.
- **Gatilho de Interação**: Auto-play contínuo baseado em `linear` motion; pausa suave da animação quando o usuário passa o mouse por cima (`hover:pause` ou evento de toque).
- **Onde encaixar**: Seção de validação social intermediária, entre a apresentação de funcionalidades e a tabela de preços.

### 8. FAQ 01 — Smooth Accordion Matrix (`faq-01`)
- **Anatomia Visual**: Grade organizada de perguntas frequentes em formato de acordeão de largura controlada (`max-w-3xl mx-auto`). Cada item é separado por divisórias finas em `#3d3f3f`. O gatilho exibe a pergunta em fonte semibold e um ícone de Chevron ou sinal de mais (+) que gira 45 graus para se transformar em um xis de fechamento.
- **Gatilho de Interação**: Clique no item; a resposta se expande com física fluida calculada pela medição automática de altura do Framer Motion (`animate={{ height: "auto", opacity: 1 }}`), sem pulos bruscos de layout.
- **Onde encaixar**: Penúltima dobra da página, resolvendo objeções finais de compra antes do Call to Action definitivo.

### 9. CTA 01 / CTA 04 — Luminescent Aurora Conversion Banner (`cta-01` / `cta-04`)
- **Anatomia Visual**: Bloco de fechamento de alto impacto com formato de cartão flutuante arredondado (`rounded-3xl`). Ao fundo, uma aura luminosa em gradiente radial ciano/índigo com desfoque gaussiano profundo (`blur-3xl`) cria um brilho etéreo. O centro abriga um headline de chamada urgente, campo de inserção de email com botão acoplado internamente e micro-cópias de garantia ("Sem necessidade de cartão de crédito. Cancele quando quiser.").
- **Gatilho de Interação**: Entrada com scale-in suave ao rolar a página até a base; input com anel de foco luminescente (`focus-within:ring-2 focus-within:ring-indigo-500/50`).
- **Onde encaixar**: Bloco final de encerramento da landing page, logo antes do rodapé institucional.

### 10. Contact 01 & System Status Footer Grid (`contact-01` / Footer)
- **Anatomia Visual**: Rodapé multi-colunar arquitetural que integra o bloco de contato. Possui links categorizados hierarquicamente por Produto, Recursos, Desenvolvedores e Jurídico, acompanhado por um indicador de status de sistema com ponto verde pulsante em CSS (`animate-ping`) comunicando "All systems operational 99.99%".
- **Gatilho de Interação**: Links com transição de cor do cinza neutro para o branco puro no hover; campo de newsletter com confirmação de sucesso embutida sem recarregamento de página.
- **Onde encaixar**: Fechamento absoluto no rodapé de todas as páginas da aplicação.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup
Para projetos utilizando o padrão shadcn ou ecossistemas modernos com React 19 / Next.js 15, a instalação das seções e utilitários do OriginKit requer os seguintes pacotes base:

```bash
# Instalação das bibliotecas centrais de suporte
npm install motion lucide-react clsx tailwind-merge @radix-ui/react-accordion @radix-ui/react-slot
```

#### Instalação Direta via CLI Oficial do OriginKit:
O OriginKit disponibiliza uma CLI própria que se integra ao arquivo `components.json` do seu projeto:

```bash
# Inicialização do ambiente OriginKit
npx originkit init

# Adição de seções completas diretamente na pasta de componentes
npx originkit add hero-03
npx originkit add pricing-04
npx originkit add faq-01
npx originkit add cta-01
```

#### Conexão via Model Context Protocol (MCP Server):
Para utilização assistida por IA dentro de editores e assistentes de comando (Claude Code, Claude Desktop, Cursor), o OriginKit fornece o endpoint de MCP oficial:

```bash
# Adicionar o servidor MCP OriginKit no Claude Code CLI
claude mcp add originkit https://mcp.originkit.dev/mcp --transport http --scope user
```

### Física de Movimento e Curvas de Transição
O OriginKit Sections emprega parâmetros de física refinados em Framer Motion para garantir que componentes macro não pareçam lentos nem gerem oscilações exageradas:

1. **Expansão de Acordeões e Toggles (FAQ e Modais)**:
   - Configuração de `spring` responsivo sem oscilação elástica residual:
     - `stiffness: 400`
     - `damping: 30`
     - `mass: 0.8`
2. **Entrada Escalonada de Elementos de Página (Staggered Hero / Bento)**:
   - Curva Bezier de desaceleração suave para evitar paradas mecânicas:
     - `ease: [0.16, 1, 0.3, 1]` (Equivalente ao `easeOutExpo` cinemático).
     - Duração: `0.6s` com intervalo entre filhos `staggerChildren: 0.08s`.
3. **Rolagem Mecânica de Dígitos de Preço (Rolling Letters)**:
   - Curva Bezier com aceleração rápida e chegada macia:
     - `ease: [0.25, 0.1, 0.25, 1]` com duração de `0.45s` por glifo alternado.

---

### Receita de Código Funcional e Completa: Macro-Seção `Pricing04Section`

Abaixo está a implementação completa e realista de uma das seções mais emblemáticas do OriginKit — o bloco de preços com grade bento, toggle mensal/anual e rolagem dinâmica de números (`RollingLetters`):

```tsx
"use client";

import * as React from "react";
import { motion, AnimatePresence } from "framer-motion";
import { Check, Sparkles, ArrowRight } from "lucide-react";
import { cn } from "@/lib/utils";

// --- Sub-componente Tátil: Rolling Letters ---
interface RollingLettersProps {
  value: string;
  className?: string;
}

function RollingLetters({ value, className }: RollingLettersProps) {
  return (
    <div className={cn("inline-flex overflow-hidden font-mono", className)}>
      <AnimatePresence mode="popLayout" initial={false}>
        <motion.span
          key={value}
          initial={{ y: 24, opacity: 0 }}
          animate={{ y: 0, opacity: 1 }}
          exit={{ y: -24, opacity: 0 }}
          transition={{ duration: 0.35, ease: [0.25, 0.1, 0.25, 1] }}
          className="inline-block"
        >
          {value}
        </motion.span>
      </AnimatePresence>
    </div>
  );
}

// --- Definição dos Planos e Dados da Seção ---
interface PricingTier {
  id: string;
  name: string;
  description: string;
  monthlyPrice: string;
  yearlyPrice: string;
  features: string[];
  popular?: boolean;
  ctaText: string;
}

const PRICING_TIERS: PricingTier[] = [
  {
    id: "starter",
    name: "Starter",
    description: "Ideal para desenvolvedores solo, criadores e projetos pessoais em validação.",
    monthlyPrice: "0",
    yearlyPrice: "0",
    features: [
      "Até 3 projetos simultâneos",
      "Acesso completo à biblioteca base",
      "Deploy em edge global com SSL",
      "Comunidade no Discord & suporte fórum",
    ],
    ctaText: "Começar Grátis",
  },
  {
    id: "pro",
    name: "Pro / Growth",
    description: "Potência total para startups e equipes de produto que escalam rápido.",
    monthlyPrice: "49",
    yearlyPrice: "39",
    popular: true,
    features: [
      "Projetos e landing pages ilimitadas",
      "Todas as 70+ seções e componentes premium",
      "Servidor MCP integrado para Cursor e Claude",
      "Exportação nativa Framer e Next.js App Router",
      "Suporte prioritário via canal privado",
    ],
    ctaText: "Iniciar Teste Pro (14 dias)",
  },
  {
    id: "enterprise",
    name: "Enterprise",
    description: "Segurança avançada, governança e design system customizado para corporações.",
    monthlyPrice: "199",
    yearlyPrice: "159",
    features: [
      "SLA garantido de 99.99% com suporte 24/7",
      "Auditoria SOC2 Type II & Single Sign-On (SSO)",
      "Consultoria de engenharia de UI dedicada",
      "Componentes customizados sob demanda",
    ],
    ctaText: "Falar com Vendas",
  },
];

export function OriginPricing04Section() {
  const [isYearly, setIsYearly] = React.useState(true);

  return (
    <section className="relative overflow-hidden bg-[#0f0f10] py-24 sm:py-32 text-white">
      {/* Luz ambiente de fundo (Ambient Glow) */}
      <div
        className="pointer-events-none absolute -top-40 left-1/2 -z-10 h-[500px] w-[800px] -translate-x-1/2 rounded-full bg-indigo-500/10 blur-[140px]"
        aria-hidden="true"
      />

      <div className="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
        {/* Cabeçalho da Seção */}
        <div className="mx-auto max-w-3xl text-center">
          <div className="inline-flex items-center gap-2 rounded-full border border-[#3d3f3f] bg-[#1e1e1f] px-3.5 py-1 text-xs font-medium text-zinc-300">
            <Sparkles className="size-3.5 text-indigo-400" />
            <span>Planos Flexíveis e Transparentes</span>
          </div>

          <h2 className="mt-5 text-4xl font-semibold tracking-[-0.03em] sm:text-5xl text-white">
            Preços simples para produtos extraordinários
          </h2>
          <p className="mt-4 text-lg text-zinc-400">
            Economize semanas de desenvolvimento com seções prontas e código limpo. Cancele quando quiser.
          </p>

          {/* Toggle de Ciclo de Cobrança com Pill Animada */}
          <div className="mt-8 flex items-center justify-center gap-3">
            <span className={cn("text-sm font-medium transition-colors", !isYearly ? "text-white" : "text-zinc-500")}>
              Cobrança Mensal
            </span>

            <button
              type="button"
              role="switch"
              aria-checked={isYearly}
              onClick={() => setIsYearly(!isYearly)}
              className="relative flex h-8 w-14 cursor-pointer items-center rounded-full border border-[#3d3f3f] bg-[#141415] p-1 transition-colors hover:border-[#606364]"
            >
              <motion.div
                layout
                transition={{ type: "spring", stiffness: 500, damping: 30 }}
                className={cn("h-6 w-6 rounded-full bg-indigo-500 shadow-md", isYearly ? "ml-auto" : "ml-0")}
              />
            </button>

            <div className="flex items-center gap-1.5">
              <span className={cn("text-sm font-medium transition-colors", isYearly ? "text-white" : "text-zinc-500")}>
                Cobrança Anual
              </span>
              <span className="rounded-full bg-indigo-500/15 px-2.5 py-0.5 text-xs font-semibold text-indigo-400 border border-indigo-500/30">
                Economize 20%
              </span>
            </div>
          </div>
        </div>

        {/* Grade de Cartões Bento de Precificação */}
        <div className="mt-16 grid grid-cols-1 gap-6 lg:grid-cols-3 lg:gap-8 items-stretch">
          {PRICING_TIERS.map((tier) => {
            const price = isYearly ? tier.yearlyPrice : tier.monthlyPrice;

            return (
              <div
                key={tier.id}
                className={cn(
                  "relative flex flex-col justify-between rounded-[20px] border p-8 transition-all duration-300",
                  tier.popular
                    ? "border-indigo-500/80 bg-[#161618] shadow-[0px_0px_35px_-10px_rgba(99,102,241,0.25)] ring-1 ring-indigo-500/40"
                    : "border-[#373839] bg-[#141415] hover:border-[#4d4f50]"
                )}
              >
                {/* Tag de Destaque no Card Popular */}
                {tier.popular && (
                  <div className="absolute -top-3.5 left-1/2 -translate-x-1/2">
                    <span className="inline-flex items-center gap-1.5 rounded-full bg-gradient-to-r from-indigo-500 to-violet-600 px-3.5 py-1 text-xs font-semibold text-white shadow-sm">
                      <Sparkles className="size-3" /> Mais Escolhido
                    </span>
                  </div>
                )}

                <div>
                  <div className="flex items-center justify-between">
                    <h3 className="text-xl font-semibold text-white">{tier.name}</h3>
                  </div>
                  <p className="mt-3 text-sm leading-relaxed text-zinc-400">{tier.description}</p>

                  {/* Preço com Micro-Componente de Dígitos Rolantes */}
                  <div className="mt-6 flex items-baseline gap-1">
                    <span className="text-2xl font-medium text-zinc-400">R$</span>
                    <RollingLetters
                      value={price}
                      className="text-5xl font-bold tracking-tight text-white"
                    />
                    <span className="text-sm font-normal text-zinc-500">/mês</span>
                  </div>
                  <p className="mt-1 text-xs text-zinc-500">
                    {isYearly ? "Faturado anualmente em parcela única" : "Faturado mês a mês sem fidelidade"}
                  </p>

                  {/* Linha Divisória de Precisão Sub-pixel */}
                  <div className="my-7 h-px w-full bg-[#373839]" />

                  {/* Lista de Funcionalidades */}
                  <ul className="space-y-3.5 text-sm text-zinc-300">
                    {tier.features.map((feature, idx) => (
                      <li key={idx} className="flex items-start gap-3">
                        <div className="flex size-5 shrink-0 items-center justify-center rounded-full bg-indigo-500/10 text-indigo-400">
                          <Check className="size-3.5" />
                        </div>
                        <span className="leading-tight">{feature}</span>
                      </li>
                    ))}
                  </ul>
                </div>

                {/* Botão de Ação CTA */}
                <div className="mt-9">
                  <button
                    type="button"
                    className={cn(
                      "group relative flex w-full items-center justify-center gap-2 rounded-xl px-5 py-3.5 text-sm font-semibold transition-all duration-200 active:scale-[0.98]",
                      tier.popular
                        ? "bg-indigo-600 text-white shadow-[inset_0px_0.5px_0px_0px_rgba(255,255,255,0.25)] hover:bg-indigo-500"
                        : "border border-[#3d3f3f] bg-[#1e1e1f] text-zinc-200 hover:bg-[#282a2c] hover:text-white"
                    )}
                  >
                    <span>{tier.ctaText}</span>
                    <ArrowRight className="size-4 transition-transform group-hover:translate-x-1" />
                  </button>
                </div>
              </div>
            );
          })}
        </div>

        {/* Rodapé de Confiança e Prova Social da Seção */}
        <div className="mt-16 text-center text-xs text-zinc-500">
          Pagamentos seguros processados via Stripe. Todos os planos incluem 14 dias de garantia de reembolso incondicional.
        </div>
      </div>
    </section>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao estruturar a arquitetura de novas aplicações e landing pages utilizando o **OriginKit Sections**, a IA deve aplicar as seguintes regras e diretrizes normativas:

### 1. Declaração no `components.json` e CLI Setup
Configure o arquivo `components.json` do projeto para reconhecer os aliases de diretório padronizados:
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
    "utils": "@/lib/utils",
    "sections": "@/components/sections"
  }
}
```

### 2. Separação Estrita de Diretórios (`ui/` vs `sections/`)
- Mantenha componentes atômicos (como botões, badges, inputs e tooltips) dentro de `@/components/ui/`.
- Mantenha as macro-seções do OriginKit organizadas e isoladas em `@/components/sections/` (ex: `@/components/sections/hero-03.tsx`, `@/components/sections/pricing-04.tsx`). Isso assegura modularidade e facilita substituições completas de dobras visuais sem risco de efeitos colaterais em outros trechos do app.

### 3. Cadência de Dobras da Landing Page (Ritmo Visual Otimizado)
A ordem canônica recomendada para estruturar uma landing page de alta conversão é:
1. **Dobra 1 (Entrada)**: `Hero 03` ou `Hero 19` (com badge de novidade, proposta de valor central e CTA primário).
2. **Dobra 2 (Prova Social de Entrada)**: Faixa de logos de clientes ou `Testimonials 01` (marquee infinito suave).
3. **Dobra 3 (Aprofundamento)**: `Bento Grid Feature Matrix` (resolvendo a pergunta "Como funciona e o que faz?").
4. **Dobra 4 (Monetização)**: `Pricing 04` (com o toggle de desconto anual em destaque).
5. **Dobra 5 (Superação de Objeções)**: `FAQ 01` (com acordeão expansível suave).
6. **Dobra 6 (Encerramento)**: `CTA 01` (com aura luminescente e captura direta de lead).
7. **Dobra 7 (Fundação)**: `Contact / Footer Grid` (com status operacional em tempo real).

### 4. Gestão de Performance e Lazy Loading em Seções com Canvas / 3D
Para seções pesadas que utilizam WebGL, Three.js ou simulação de partículas contínuas (como `Hero 03` com `gallery-tunnel` ou `Hero 46`), a IA deve obrigatoriamente instanciar a importação dinâmica do Next.js com SSR desativado (`ssr: false`), evitando atrasos de First Contentful Paint (FCP) na hidratação da página:
```tsx
import dynamic from "next/dynamic";

const DynamicHeroTunnel = dynamic(
  () => import("@/components/sections/hero-03").then((mod) => mod.Hero03Section),
  { ssr: false, loading: () => <div className="h-screen bg-[#0f0f10] animate-pulse" /> }
);
```

### 5. Blindagem contra "AI Slop" e Checklist de Acessibilidade
- Garanta que todas as animações contínuas respeitem a preferência do sistema operacional por movimento reduzido:
  ```tsx
  const shouldReduceMotion = useReducedMotion();
  const transition = shouldReduceMotion ? { duration: 0 } : { duration: 0.6, ease: [0.16, 1, 0.3, 1] };
  ```
- Nunca alterne mais de três cores de destaque (*accent colors*) na mesma página. Fixe uma cor primária (ex: Indigo `#6366f1`) e uma secundária de apoio (ex: Violet `#8b5cf6`), mantendo 90% da interface ancorada na escala cinza profunda (`#0f0f10`, `#141415`, `#222425`).
