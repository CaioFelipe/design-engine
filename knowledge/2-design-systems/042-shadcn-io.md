---
id: "042-shadcn-io"
name: "Shadcn.io"
url: "https://www.shadcn.io/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Modern Clean Craft", "Precision Enterprise SaaS", "Agentic MCP-Native", "Adaptive OKLCH Theming", "Linear & Vercel Polished Aesthetic"]
densidade_informacao: "Flexivel"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS/Headless) a Medio (Framer Motion/JS/Recharts)"
stack_frameworks: ["React", "Next.js", "Vue", "Svelte", "Solid", "Tailwind CSS", "Radix UI", "Base UI", "Ark UI", "React Aria", "Recharts", "Framer Motion", "Lucide React"]
compatibilidade:
  fontes_ideais: ["Hanken Grotesk", "Geist Sans", "Inter", "Plus Jakarta Sans", "JetBrains Mono"]
  paletas_ideais: ["Neutral OKLCH Dark & Light", "Deep Slate & Zinc 950", "Stone Warm Minimalist", "Monochrome High-Contrast com Acentos Especulares"]
  combinacoes_recomendadas: ["ui.shadcn.com (oficial)", "Magic UI", "Aceternity UI", "Radix UI Primitives", "Base UI", "Lucide React", "Recharts"]
  conflitos_esteticos: ["Brutalismo Y2K desordenado e cru", "Neumorfismo skeuomórfico pesado", "Corporate Memphis pastel plano anos 2010", "Glassmorphism turvo saturado"]
---

# Shadcn.io — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Shadcn.io** é a maior infraestrutura de expansão, catalogação e orquestração autônoma construída sobre o ecossistema `shadcn/ui`. Enquanto a biblioteca original (`ui.shadcn.com`) foca na oferta de primitivas atômicas de UI distribuídas via código-fonte aberto, o **Shadcn.io** opera como uma macro-plataforma com mais de 6.200 blocos prontos, 14 templates completos de nível de produção e 175 componentes estendidos para múltiplos frameworks (**React, Vue, Svelte e Solid**), com suporte nativo a múltiplos motores de acessibilidade headless (**Radix UI, Base UI, Ark UI e React Aria**).

A assinatura visual e técnica do Shadcn.io é caracterizada por quatro pilares essenciais:

1. **A Era dos "Blocos Organísmicos" (Block-First Design Architecture)**:
   Em vez de forçar o engenheiro de produto a montar telas complexas do zero elemento por elemento (compondo botões, cartões, inputs e modais manualmente), o Shadcn.io padroniza o conceito de **Blocos de UI completos**: seções inteiras de Dashboard analítico, fluxos de autenticação em múltiplas etapas, matrizes de precificação com toggles dinâmicos, terminais de chat para IA e seções Hero completas com Bento Grids e prova social. Todos os blocos compartilham a mesma gramática visual e tokens atômicos do ecossistema shadcn.

2. **Desacoplamento entre Estilo Estrutural (Styles) e Tema Cromático (Themes)**:
   O Shadcn.io implementa uma divisão formal que eleva o design system a outro nível:
   - **Styles Estruturais (`nova`, `lyra`, `sera`, `rhea`)**: Governam a densidade, ritmo vertical, proporções de padding/margin, formato de cantos (`--radius`) e sensação geométrica do componente (ex: o estilo *Nova* oferece uma abordagem moderna e compacta para produtos SaaS; *Lyra* entrega cantos vivos e estética ultra-estruturada com fontes monoespaçadas; *Sera* foca em tipografia editorial refinada).
   - **Temas & Tokens em Espaço OKLCH**: As variáveis de cor utilizam o modelo de cor perceptual `oklch()`, garantindo uniformidade matemática de luminosidade e contraste tanto no tema claro quanto no tema escuro (`--background: oklch(0.145 0 0)`, `--border: oklch(1 0 0 / 10%)`).

3. **Arquitetura Agêntica Nativa com Model Context Protocol (MCP)**:
   O grande diferencial do Shadcn.io é seu pioneirismo na era dos agentes autônomos de software. A plataforma oferece um servidor oficial MCP (`https://www.shadcn.io/api/mcp`) que se conecta diretamente a editores e ambientes assistidos por IA (como **Claude Code, Cursor, VS Code, Windsurf e OpenAI Codex**). O agente de IA não adivinha classes Tailwind desatualizadas: ele consulta a API do registro em tempo real, obtém o JSON do bloco solicitado e injeta código limpo, tipado e perfeitamente ajustado ao tema do repositório local.

4. **Multi-Framework e Agnóstico de Primitivas**:
   A plataforma rompe o monopólio exclusivo do React no ecossistema shadcn, fornecendo versões oficiais equivalentes para Svelte (via Bits UI), Vue (via Radix Vue / shadcn-vue) e Solid JS, permitindo que times que operam stacks políglotas compartilhem rigorosamente a mesma consistência visual e comportamento tátil.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto
- **SaaS B2B, Ferramentas de Produtividade & Workspaces**: Interfaces que exigem alta densidade funcional, legibilidade impecável e comandos de teclado acessíveis (ex: Linear, Notion, Raycast).
- **Plataformas de IA, Orquestradores de Agentes & Chatbots Cognitivos**: O Shadcn.io possui categorias exclusivas de blocos para IA (threads de chat com suporte a streaming de markdown, cards de chamada de ferramentas/MCP, terminais de prompt flutuantes).
- **Developer Tools, Painéis de Observabilidade & Infraestrutura Cloud**: Integração fluida com gráficos Recharts e tabelas avançadas com ordenação, filtros e paginação nativas.
- **Fintechs, Painéis de Billing & Gateways de Pagamento**: Blocos de checkout, faturamento recorrente, histórico de faturas e cartões de gerenciamento de assinatura pré-configurados.
- **Landing Pages de Produtos Digitais e Startups**: Hero sections, tabelas de preço comparativas, seções de recursos com Bento Grids e footers estruturados.

### Papel no Ritmo Visual (A Aplicação da Regra 60-30-10)

- **60% — Fundação Neutra e Estrutura Utilitária (A Espinha Dorsal do Sistema)**:
  O Shadcn.io brilha com maestria neste papel. A base visual (`bg-background`, `border-border`, `text-foreground`, `bg-card`) deve constituir os 60% da página. Ela fornece a neutralidade necessária para que o usuário navegue sem atrito cognitivo.
- **30% — Componentes Interativos e Feedback Tátil**:
  Menus contextuais suspensos (`DropdownMenu`), diálogos modais acessíveis (`Dialog`), seletores dinâmicos (`Combobox`), gavetas laterais (`Sheet`), abas (`Tabs`) e tabelas expansíveis.
- **10% — Efeitos Protagonistas e Micro-Delícias**:
  O Shadcn.io fornece botões animados (`Animated Buttons`), fundos com shaders GLSL/CSS (`Shaders`, `Backgrounds`), efeitos sutis em textos e gráficos interativos com tooltips dinâmicos e cursores magnéticos.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Projetos Artísticos de Anti-Design / Brutalismo Caótico**: Se o projeto busca desconstrução intencional, tipografia sobreposta ilegível, cores neon saturadas sem contraste e layout assimétrico disfuncional, o rigor do Shadcn.io neutralizará o apelo estético proposto.
- **Interfaces com Requisitos Esqueléticos / Sem Camada de Build**: Aplicações em HTML estático legado que não suportam Tailwind CSS v3.4+/v4 ou empacotamento moderno de módulos (Vite, Next.js, Nuxt, Astro).
- **Aplicações Ultra-Miniaturizadas com Restrição Extrema de Pacote (< 5KB Total)**: Embora headless e modular, o uso de primitivas Radix/Base UI adiciona uma pequena sobrecarga no bundle JavaScript (especialmente em componentes de data picker ou combobox).

### ⚠️ A Síndrome do "Template Genérico de IA" & Como Evitar
Com o advento da geração de código por IA, tornou-se comum ver páginas montadas por agentes sem critério:
> *Hero padrão com fundo cinza neutro + 3 cartões de features com ícones Lucide azuis centralizados + Tabela de preços de 3 colunas copiada sem nenhum ajuste de marca.*

#### Como Preservar a Originalidade ao Utilizar o Shadcn.io:
1. **Defina a Assinatura Estrutural do Projeto**: Escolha ativamente entre os estilos `nova`, `lyra`, `sera` ou `rhea`. Não fique preso ao padrão neutro tradicional.
2. **Personalize os Tokens OKLCH de Marca**: Substitua o preto/branco puro (`oklch(0 0 0)` / `oklch(1 0 0)`) por uma matiz cromática calculada (ex: um tom grafite com leve infusão de azul meia-noite ou ardósia quente).
3. **Harmonize com Bibliotecas de Movimento Protagonista**: Quando o projeto precisar de um "uau" imediato, combine a estabilidade funcional dos blocos do Shadcn.io com um showstopper único da **Magic UI** ou da **Aceternity UI** na seção Hero.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão 10 dos componentes e blocos mais emblemáticos e avançados do ecossistema Shadcn.io:

### 1. Interactive Analytics Dashboard Block
- **Anatomia Visual**: Painel de alta densidade composto por um grid de 4 cartões de KPIs (com indicadores de tendência positiva/negativa com setas de variação percentual), acompanhado de um gráfico de área temporal interativo (Recharts) com seletor de granularidade (7 dias, 30 dias, 12 meses) e tabela de eventos recentes.
- **Gatilho de Interação**: Hover com tooltip magnético no gráfico, tabs com transição suave para alternar visualizações, dropdowns para exportar dados (CSV/JSON).
- **Onde encaixar**: Dashboard principal de SaaS B2B, painéis financeiros e consoles administrativos.

### 2. Conversational AI Chat Interface Block
- **Anatomia Visual**: Interface de chat conversacional completa estilo Claude/ChatGPT. Possui feed de mensagens com bolhas diferenciadas de usuário e assistente, formatação automática de blocos de código com botão de cópia, visualização de chamadas de ferramentas (*tool calling badges*) e barra de prompt inferior flutuante com auto-resize e botões de anexo.
- **Gatilho de Interação**: Input expansível ao digitar, scroll automático para o final da conversa, hover em ações da mensagem (copiar, regenerar, feedback positivo/negativo).
- **Onde encaixar**: Módulos de assistentes inteligentes, painéis de suporte técnico, ferramentas de busca semântica em bases de conhecimento.

### 3. Tiered Pricing Matrix Block with Annual/Monthly Toggle
- **Anatomia Visual**: Tabela de preços com 3 ou 4 planos (Starter, Pro, Enterprise). O plano Pro é visualmente destacado com borda luminosa primária (`ring-2 ring-primary`) e badge flutuante "Mais Popular". Possui um switch toggle no topo com desconto percentual destacado (ex: "Economize 20%").
- **Gatilho de Interação**: Click no toggle de periodicidade alternando os valores com animação numérica rápida via Motion; hover cards com elevação sutil no eixo Y (`-translate-y-1`).
- **Onde encaixar**: Página dedicada de `/pricing` ou seção de conversão na Landing Page.

### 4. Hero Section with Glow Shader & Video Dialog Modal
- **Anatomia Visual**: Título balanceado em escala tipográfica monumental (`text-5xl md:text-7xl tracking-tighter`), pílula de novidade no topo com link interativo, CTAs duplos (Primary com raio completo + Outline secundário) e mockup central do produto com borda reflexiva e fundo em gradiente cônico sutil (*Glow Shader*).
- **Gatilho de Interação**: Click no mockup ou botão de play abre um modal imersivo (`Dialog`) com backdrop escuro (`backdrop-blur-md`) exibindo o vídeo de demonstração do software.
- **Onde encaixar**: Seção Hero principal de landing pages de produtos e aplicativos de tecnologia.

### 5. Multi-Level Responsive App Navigation Shell (Sidebar + GlobalNav)
- **Anatomia Visual**: Barra de navegação global superior de 56px (`h-14`) com menus suspensos acionados por hover (*flyout menus* com suporte a grid de 3 colunas) combinada a uma barra lateral dobrável (`Sidebar`) com estados colapsado/expandido persistidos via cookie.
- **Gatilho de Interação**: Hover com delay calculado para flyouts superiores; atalho de teclado `⌘B` ou botão toggle para recolher a sidebar lateral; indicador ativo de rota com pílula de contraste.
- **Onde encaixar**: Espinha dorsal da aplicação em áreas logadas e páginas de documentação técnica.

### 6. Command Palette (Global Search ⌘K Dialog)
- **Anatomia Visual**: Modal flutuante central com input de pesquisa instantânea, categorização em grupos de itens (Ações Rápidas, Navegação, Documentação, Configurações) com atalhos de teclado renderizados em tags de tecla estilizadas (`<kbd>`).
- **Gatilho de Interação**: Acionado globalmente via atalho `⌘K` (Mac) ou `Ctrl+K` (Windows). Navegação por setas do teclado (cima/baixo) e seleção com `Enter`.
- **Onde encaixar**: Presente em todas as páginas da aplicação, acessível pela navbar ou atalho global.

### 7. Modern Auth & Onboarding Flow Block
- **Anatomia Visual**: Cartão centralizado com cabeçalho de boas-vindas, botões de autenticação social com provedores (GitHub, Google, Apple) com ícones SVG inline, divisor horizontal com texto central "ou continue com e-mail", campo de e-mail estilizado e suporte a código de verificação OTP de 6 dígitos separados por slots individuais.
- **Gatilho de Interação**: Foco automático entre slots de código OTP conforme os dígitos são inseridos; validação de formulário em tempo real; feedback visual de carregamento nos botões com spinners fluídos.
- **Onde encaixar**: Páginas de Login (`/sign-in`), Cadastro (`/sign-up`) e recuperação de senha.

### 8. Interactive Area Chart with Tooltip Cursor
- **Anatomia Visual**: Gráfico de área construído sobre Recharts com gradiente vertical na área preenchida (`opacity-40` para `opacity-5`). O eixo X exibe formatação de datas compacta e o grid é renderizado com traços pontilhados discretos (`stroke-muted`).
- **Gatilho de Interação**: Movimento do cursor sobre o gráfico revela uma linha vertical pontilhada e um cartão flutuante de tooltip formatado com os valores monetários ou numéricos exatos de cada série temporal.
- **Onde encaixar**: Cartões de relatórios, monitoramento de servidores e resumos de vendas.

### 9. Animated Glow Button with Border Trail
- **Anatomia Visual**: Botão de chamada para ação com efeito visual avançado onde uma partícula ou feixe de luz translúcido percorre o perímetro da borda arredondada em loop suave, sem obstruir o texto ou o ícone interno.
- **Gatilho de Interação**: Efeito contínuo em CSS puro (`conic-gradient` animado via `@property --angle`) ou intensificado no evento `:hover`.
- **Onde encaixar**: CTA principal da seção Hero ou botão de upgrade para o plano Pro.

### 10. High-Performance Dynamic Data Table
- **Anatomia Visual**: Tabela densa com cabeçalho fixo, suporte a checkboxes para seleção múltipla de linhas, seletor de visibilidade de colunas (*Column Toggle*), campo de busca rápida com debounce e barra de paginação com informações de registros exibidos.
- **Gatilho de Interação**: Click no cabeçalho para ordenar (crescente/decrescente); seleção de linhas para exibir barra de ações em massa (*Floating Action Bar*); paginação instantânea.
- **Onde encaixar**: Módulos de clientes, transações financeiras, catálogos de produtos e logs de auditoria.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### 1. Dependências & Setup de Ambiente

Para projetos React / Next.js que utilizam Tailwind CSS v3 ou v4:

```bash
# 1. Instalar dependências utilitárias e headless essenciais
npm install clsx tailwind-merge class-variance-authority lucide-react framer-motion recharts

# 2. Inicializar o CLI oficial do shadcn
npx shadcn@latest init

# 3. Adicionar blocos e componentes
npx shadcn@latest add button card dialog dropdown-menu input table
```

### 2. Configuração do Servidor MCP (Model Context Protocol)

O Shadcn.io permite que assistentes de IA (Cursor, Claude Code, Windsurf, VS Code) instalem e configurem componentes diretamente. Exemplo de configuração em `.vscode/mcp.json` ou arquivo de configuração do Cursor:

```json
{
  "mcpServers": {
    "shadcnio": {
      "type": "http",
      "url": "https://www.shadcn.io/api/mcp",
      "headers": {
        "Authorization": "Bearer SEU_TOKEN_SHADCN_IO"
      }
    }
  }
}
```

### 3. Tokens OKLCH no `globals.css` (Padrão Shadcn.io)

O Shadcn.io padroniza as variáveis de cor com o modelo de cor OKLCH para garantir transições suaves e contraste perceptivo:

```css
@layer base {
  :root {
    --radius: 0.625rem;
    --background: oklch(1 0 0);
    --foreground: oklch(0.145 0 0);
    --card: oklch(1 0 0);
    --card-foreground: oklch(0.145 0 0);
    --popover: oklch(1 0 0);
    --popover-foreground: oklch(0.145 0 0);
    --primary: oklch(0.205 0 0);
    --primary-foreground: oklch(0.985 0 0);
    --muted: oklch(0.97 0 0);
    --muted-foreground: oklch(0.556 0 0);
    --accent: oklch(0.97 0 0);
    --accent-foreground: oklch(0.205 0 0);
    --border: oklch(0.922 0 0);
    --input: oklch(0.922 0 0);
    --ring: oklch(0.708 0 0);
  }

  .dark {
    --background: oklch(0.145 0 0);
    --foreground: oklch(0.985 0 0);
    --card: oklch(0.175 0 0);
    --card-foreground: oklch(0.985 0 0);
    --popover: oklch(0.175 0 0);
    --popover-foreground: oklch(0.985 0 0);
    --primary: oklch(0.985 0 0);
    --primary-foreground: oklch(0.145 0 0);
    --muted: oklch(0.245 0 0);
    --muted-foreground: oklch(0.65 0 0);
    --accent: oklch(0.245 0 0);
    --accent-foreground: oklch(0.985 0 0);
    --border: oklch(1 0 0 / 10%);
    --input: oklch(1 0 0 / 12%);
    --ring: oklch(0.5 0 0);
  }
}
```

### 4. Física de Movimento & Transições

- **Curvas de Bézier Padrão**:
  - Transições de Interface e Modais: `cubic-bezier(0.16, 1, 0.3, 1)` (curva rápida de aceleração com acomodação suave e natural).
  - Hover e Microinterações: `cubic-bezier(0.4, 0, 0.2, 1)`.
- **Molas Framer Motion (Spring Physics)**:
  - Dropdowns e Popovers: `{ type: "spring", stiffness: 350, damping: 28, mass: 0.8 }`.
  - Hover de Cards e Elevação: `{ type: "spring", stiffness: 400, damping: 30 }`.

---

### 5. Receita de Código Funcional: Bloco de Métrica com Gráfico Interativo & Ação Rápida

Abaixo está a implementação completa e modular de um bloco de métricas de alta densidade no padrão Shadcn.io, com suporte a tema dark/light, tokens OKLCH e animação de entrada com Framer Motion:

```tsx
"use client";

import * as React from "react";
import { motion } from "framer-motion";
import { 
  TrendingUp, 
  ArrowUpRight, 
  MoreHorizontal, 
  Sparkles,
  Calendar
} from "lucide-react";
import { 
  ResponsiveContainer, 
  AreaChart, 
  Area, 
  XAxis, 
  Tooltip 
} from "recharts";

// Dados simulados da métrica semanal
const analyticsData = [
  { day: "Seg", revenue: 4200, users: 240 },
  { day: "Ter", revenue: 5800, users: 310 },
  { day: "Qua", revenue: 5100, users: 290 },
  { day: "Qui", revenue: 7300, users: 440 },
  { day: "Sex", revenue: 6900, users: 410 },
  { day: "Sáb", revenue: 8400, users: 520 },
  { day: "Dom", revenue: 9800, users: 610 },
];

export function AnalyticsMetricCard() {
  const [activeMetric, setActiveMetric] = React.useState<"revenue" | "users">("revenue");

  return (
    <motion.div
      initial={{ opacity: 0, y: 12 }}
      animate={{ opacity: 1, y: 0 }}
      transition={{ duration: 0.35, ease: [0.16, 1, 0.3, 1] }}
      className="w-full max-w-xl rounded-xl border border-border bg-card p-6 text-card-foreground shadow-sm transition-all"
    >
      {/* Header do Card com Título e Ação */}
      <div className="flex items-start justify-between pb-4">
        <div className="space-y-1">
          <div className="flex items-center gap-2 text-xs font-medium text-muted-foreground">
            <span className="flex size-2 rounded-full bg-emerald-500 ring-2 ring-emerald-500/20" />
            <span>Desempenho Semanal</span>
          </div>
          <h3 className="text-2xl font-semibold tracking-tight">
            {activeMetric === "revenue" ? "R$ 47.500" : "2.820 novos usuários"}
          </h3>
        </div>

        <div className="flex items-center gap-1.5">
          <button
            onClick={() => setActiveMetric(activeMetric === "revenue" ? "users" : "revenue")}
            className="inline-flex h-8 items-center gap-1.5 rounded-lg border border-border bg-muted/50 px-2.5 text-xs font-medium text-foreground transition-colors hover:bg-muted focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring"
          >
            <Sparkles className="size-3.5 text-primary" />
            <span>{activeMetric === "revenue" ? "Ver Usuários" : "Ver Receita"}</span>
          </button>
          <button 
            aria-label="Mais opções"
            className="flex size-8 items-center justify-center rounded-lg text-muted-foreground hover:bg-muted hover:text-foreground transition-colors"
          >
            <MoreHorizontal className="size-4" />
          </button>
        </div>
      </div>

      {/* Indicador de Crescimento */}
      <div className="flex items-center gap-2 pb-6 text-xs">
        <span className="inline-flex items-center gap-0.5 rounded-md bg-emerald-500/10 px-1.5 py-0.5 font-medium text-emerald-600 dark:text-emerald-400">
          <TrendingUp className="size-3" />
          +18.4%
        </span>
        <span className="text-muted-foreground">em relação à semana anterior</span>
      </div>

      {/* Gráfico Recharts de Área */}
      <div className="h-44 w-full">
        <ResponsiveContainer width="100%" height="100%">
          <AreaChart data={analyticsData} margin={{ top: 4, right: 4, left: 4, bottom: 0 }}>
            <defs>
              <linearGradient id="colorMetric" x1="0" y1="0" x2="0" y2="1">
                <stop offset="5%" stopColor="var(--primary)" stopOpacity={0.3} />
                <stop offset="95%" stopColor="var(--primary)" stopOpacity={0.0} />
              </linearGradient>
            </defs>
            <XAxis 
              dataKey="day" 
              stroke="currentColor" 
              className="text-[11px] text-muted-foreground"
              tickLine={false} 
              axisLine={false} 
            />
            <Tooltip
              content={({ active, payload }) => {
                if (active && payload && payload.length) {
                  return (
                    <div className="rounded-lg border border-border bg-popover px-3 py-1.5 shadow-md">
                      <p className="text-[11px] font-medium text-muted-foreground">
                        {payload[0].payload.day}
                      </p>
                      <p className="text-xs font-semibold text-popover-foreground">
                        {activeMetric === "revenue" 
                          ? `R$ ${payload[0].value?.toLocaleString("pt-BR")}` 
                          : `${payload[0].value} usuários`}
                      </p>
                    </div>
                  );
                }
                return null;
              }}
            />
            <Area
              type="monotone"
              dataKey={activeMetric}
              stroke="var(--primary)"
              strokeWidth={2}
              fillOpacity={1}
              fill="url(#colorMetric)"
            />
          </AreaChart>
        </ResponsiveContainer>
      </div>

      {/* Rodapé Informativo */}
      <div className="mt-4 flex items-center justify-between border-t border-border pt-4 text-xs text-muted-foreground">
        <div className="flex items-center gap-1.5">
          <Calendar className="size-3.5" />
          <span>Últimos 7 dias sincronizados</span>
        </div>
        <a 
          href="/analytics" 
          className="inline-flex items-center gap-1 font-medium text-foreground hover:underline"
        >
          <span>Relatório completo</span>
          <ArrowUpRight className="size-3.5" />
        </a>
      </div>
    </motion.div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar o ecossistema **Shadcn.io** como a espinha dorsal de um novo projeto no blueprint de arquitetura, siga estritamente estas diretrizes:

1. **Definição Explícita de Estilo de Base (`Base Style`)**:
   - Declare se o projeto utilizará `nova` (SaaS enxuto, cantos arredondados balanceados), `lyra` (estilo técnico com cantos vivos `radius: none` e fontes monoespaçadas) ou `sera` (orientado a tipografia e editoriais).
2. **Declaração de Tokens de Cor em OKLCH**:
   - Inclua no blueprint a tabela de tokens com matizes calibradas no espaço de cor OKLCH para evitar discordâncias entre temas claro e escuro.
3. **Mapeamento de Blocos por Página**:
   - No blueprint, não liste apenas primitivas soltas (`Button`, `Card`). Liste os **Blocos Shadcn.io** específicos necessários para cada rota da aplicação:
     - `/dashboard`: `Analytics Metric Grid`, `Interactive Area Chart`, `Recent Transactions Table`.
     - `/auth`: `Multi-provider OAuth + 6-digit OTP Input Form`.
     - `/pricing`: `Annual/Monthly Pricing Matrix with Feature Comparison`.
4. **Instruções para Agentes de IA via MCP**:
   - Quando o projeto contar com suporte a agentes de desenvolvimento (Cursor / Claude Code), documente a instrução para o agente consultar a API de registros e schemas do Shadcn.io antes de gerar qualquer novo componente de tela, garantindo a perfeita reusabilidade de tokens.
