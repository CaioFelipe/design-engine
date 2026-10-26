---
id: "uinice"
name: "UINice"
url: "https://uinice.com/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Vibe Coder Craft", "Modern Minimalist", "Curated Ecosystem", "Terminal & AI Conversational"]
densidade_informacao: "Flexivel"
impacto_visual: "Moderado a Alto/Showstopper"
custo_computacional: "Baixo (CSS/Headless) a Medio (Framer Motion/JS)"
stack_frameworks: ["React", "Next.js", "Tailwind CSS", "Framer Motion", "shadcn/ui", "Radix UI", "Model Context Protocol (MCP)"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Geist Mono", "Inter", "JetBrains Mono"]
  paletas_ideais: ["Deep Neutral Zinc (Zinc 950/900/50)", "High-Contrast Monochrome with Pure Black Accents", "Subtle Code Syntax Highlights (Emerald, Violet, Amber)"]
  combinacoes_recomendadas: ["shadcn/ui", "prompt-kit", "Streamdown", "Lucide React", "Animata", "Dice UI", "Achromatic", "Unlumen UI"]
  conflitos_esteticos: ["Corporate Memphis saturado", "Neumorfismo pastel clássico", "Skeuomorfismo pesado dos anos 2010"]
---

# UINice — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **UINice** (`uinice.com`) representa a evolução definitiva dos diretórios de interface na era da **Inteligência Artificial Generativa e do Vibe Coding**. Enquanto diretórios tradicionais como Dribbble ou Behance exibem renders estáticos sem código, e registros como o ecossistema shadcn/ui e NPM ficam pulverizados em dezenas de repositórios isolados, o UINice consolida uma curadoria rigorosamente humana de kits de UI, bibliotecas de movimento, sistemas de design, ícones e templates de produção — onde **100% dos recursos catalogados contam com código-fonte funcional, comando de instalação em linha única e prompt contextual calibrado para assistentes de IA**.

### Assinatura e Filosofia Visual
A identidade visual do UINice é a materialização do **"Vibe Coder Craft"**: uma estética limpa, técnica e focada no desenvolvedor que constrói com ferramentas modernas (Cursor, Claude Code, Windsurf, VS Code). Seus elementos distintivos incluem:

- **Espinha Dorsal Neutra com Espaçamento Generoso**: Fiel ao manifesto *"No gradients, generous whitespace, one accent color"*, o UINice rejeita a sobrecarga de gradientes multicoloridos em favor de superfícies monocromáticas de alta precisão (`zinc-950` / `zinc-900` em Dark Mode e brancos imaculados com toques neutros em Light Mode).
- **Tratamento de Superfícies & Dot Matrix Backdrops**: Emprega painéis translúcidos de vidro suave (`.wb-panel` com bordas sutis `border-zinc-200/80 dark:border-zinc-800/80`), suportados por malhas de pontos procedurais (`.wb-dots`) com mascaramento radial que conferem profundidade tridimensional sem roubar o protagonismo dos componentes.
- **Triple-Layer Asynchronous Marquee (Paredão Infinito)**: Uma das assinaturas mais marcantes da plataforma é a esteira contínua de screenshots de componentes em três faixas paralelas com velocidades descompassadas (`64s`, `74s`, `84s`), com a linha central invertida (`rev`). Esse ritmo assimétrico elimina a sensação mecânica de repetição em loop.
- **Micro-ecossistema de Terminal & Conversação AI**: Elementos gráficos que emulam a linha de comando (`$ npx shadcn@latest add ... -> ✓ Added components/ui/button.tsx`) e balões de diálogo com ferramentas MCP (`search_kits`, `get_kit`), unificando o visual do design de produto com a ergonomia do terminal de desenvolvimento.
- **Integração Nativa com o Model Context Protocol (MCP)**: É pioneiro ao transformar o diretório visual em um servidor MCP consumível diretamente por agentes em IDEs, permitindo que a IA busque, inspecione e instale componentes sem que o desenvolvedor precise alternar de contexto.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados
1. **Aplicações de Inteligência Artificial & Agentes Conversacionais**: Plataformas de chat multimodal, assistentes autônomos e estúdios de prompt que demandam áreas de entrada dedicadas, streaming de markdown em tempo real e feedback de processamento de alta fidelidade.
2. **Developer Tools & Infraestrutura Cloud**: Portais de documentação interativa, painéis de monitoramento, dashboards de APIs e interfaces com microinterações orientadas a atalhos de teclado e terminal.
3. **SaaS B2B Moderno & FinTechs de Nova Geração**: Produtos que buscam a precisão minimalista de referências como Linear, Vercel e Stripe, utilizando sistemas de design comprovados e de baixa manutenção.
4. **Prototipagem de Altíssima Fidelidade (Vibe Coding)**: Projetos acelerados com Cursor e Claude Code, onde componentes inteiros precisam ser montados a partir de receitas prontas com comandos `npx` e prompts cirúrgicos.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Neutra & Primitivas)**: Utilize a base sólida do `shadcn/ui` ou sistemas de design neutros curados pelo UINice (ex: `Studio Admin`, `Lexington Themes`), estabelecendo superfícies sóbrias, tipografia neutra (`Geist Sans` ou `Inter`) e grid modular estrito.
- **30% (Camada Tátil, Microinterações & Recipes)**: Aplique os padrões especializados e componentes de interação recomendados pelo UINice — inputs compostos com atalhos de teclado (ex: `prompt-kit`), renderizadores de streaming (`Streamdown`), breadcrumbs fluidos e painéis de terminal de feedback.
- **10% (Showstoppers & Elementos de Deslumbramento)**: Reserve os efeitos visuais de alto impacto (ex: Marquee triplo infinito, micro-animações de morphing com `Morphicons`, ícones 3D com `3dicons` ou transições orgânicas de `Animata`) estritamente para a seção Hero de landing pages, modais de onboarding ou o cartão de destaque da funcionalidade principal.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Interfaces Corporativas Legadas / ERPs Ultra-densos**: Sistemas com formulários contínuos de centenas de campos não devem adotar layouts arejados de vibe coding com espaçamentos generosos e esteiras infinitas, sob risco de quebrar o fluxo de trabalho de digitação rápida.
- **Portais Governamentais / Serviços Públicos com Restrições Estritas de WCAG**: O uso de contrastes sutis em bordas cinza claro sobre fundo branco ou tons de cinza muito próximos (`zinc-800` sobre `zinc-900`) pode não atender aos critérios mais rígidos de contraste AA/AAA sem ajustes explícitos de paleta.
- **Ambientes Offline ou Sem Conectividade Externa**: O ecossistema UINice depende de CLI registries e ferramentas MCP dinâmicas; ecossistemas air-gapped com restrição a registros externos de pacotes demandam espelhamento prévio de código.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **Colagem Incoerente de Bibliotecas ("Dependency Frankenstein")**: Combinar componentes de 5 bibliotecas distintas sem unificar os tokens de design (ex: um botão com `rounded-full` de uma lib, um input com `rounded-none` de outra, e bordas com espessuras conflitantes).
- **Sobrecarga de Efeitos de Movimento**: Adicionar esteiras infinitas de logos, terminais com texto animado e botões pulsantes em uma mesma tela, gerando poluição cognitiva e fadiga visual.
- **Execução Cega de Prompts sem Higienização de Tokens**: Gerar interfaces via Cursor/Claude Code a partir de prompts do UINice sem revisar se as cores semânticas (`primary`, `accent`, `muted`) estão mapeadas para o `tailwind.config.ts` do projeto local.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 10 componentes e padrões de arquitetura visual mais emblemáticos inspirados e catalogados pela curadoria do UINice:

### 1. Triple-Layer Desynchronized Infinite Marquee (`.lp-wall` & `.lp-track`)
- **Anatomia Visual**: Composição de 3 fileiras horizontais contínuas contendo miniaturas de interfaces e cartões de componentes. Cada fileira move-se com uma duração distinta (`64s`, `74s`, `84s`), com a linha central deslocando-se no sentido reverso (`rev`). Cada cartão possui cantos arredondados (`rounded-xl`), sombra suave e efeito de zoom com atenuação ao hover.
- **Gatilho de Interação**: Animação contínua e autônoma baseada em transformações de GPU (`transform: translate3d`). Pausa suave sob foco ou cursor (`hover:pause`).
- **Onde encaixar**: Seção Hero de landing pages, vitrines de portfólio e cabeçalhos de galerias de recursos.

### 2. Interactive CLI Terminal Badge (`.lp-term`)
- **Anatomia Visual**: Container estilizado que evoca uma janela de linha de comando minimalista. Exibe o prompt com símbolo de cifrão colorido (`$`), comando de instalação de pacote (`npx shadcn@latest add button`), linha divisória sutil e status de verificação verde (`✓ Added components/ui/button.tsx`).
- **Gatilho de Interação**: Clique para copiar o comando com micro-feedback de confirmação animado ("Copied!" ou transição do ícone de clipboard para check mark).
- **Onde encaixar**: Cards explicativos de componentes, seções "How to Install" de documentação e blocos de instrução técnica para desenvolvedores.

### 3. AI Conversational Preview Bubble (`.lp-chat`)
- **Anatomia Visual**: Bloco de mensagem com balão de comando do usuário em linguagem natural ("Find me a dark dashboard template for Next.js") e resposta instantânea do agente MCP com indicador circular de status (`⏺ uinice · search_kits`), acompanhado da lista categorizada de opções disponíveis.
- **Gatilho de Interação**: Animação de digitação escalonada (typing text reveal) ou exibição estática interativa que demonstra as capacidades de integração com agentes de IA.
- **Onde encaixar**: Seção de apresentação de recursos inteligentes, páginas de introdução ao protocolo MCP e demonstrações de ferramentas integradas a LLMs.

### 4. Interactive Action Pill Badge (`.lp-pill`)
- **Anatomia Visual**: Pílula flutuante arredondada (`rounded-full`) com fundo semitranslúcido e borda em gradiente sutil. Contém um marcador em negrito com fundo escuro invertido ("No design skills"), texto explicativo ("One line of code, designer-grade UI") e um glifo de seta direcional (`→`).
- **Gatilho de Interação**: Hover com expansão de padding milimétrica e translação horizontal do glifo de seta (`translate-x-1`) através de curva de mola rápida.
- **Onde encaixar**: Topo da seção Hero (acima do título H1) para anúncios, novidades e direcionamento para a navegação principal.

### 5. Multi-Kit Recipe Blueprint Card (`.hm-recipe`)
- **Anatomia Visual**: Card arquitetural de receitas completas que combina diferentes kits de UI em uma solução pronta de tela (ex: "Calm AI chat"). Apresenta screenshot da composição montada, descrição da estética ("No gradients, generous whitespace, one accent color") e a lista discriminada de kits constituintes: Base (`shadcn/ui`), Input (`prompt-kit`), Streaming Text (`Streamdown`) e Ícones (`Lucide`).
- **Gatilho de Interação**: Expansão de detalhes com um clique para revelar os 4 comandos de terminal consecutivos e o prompt pronto para o agente de IA.
- **Onde encaixar**: Seções de Templates e Casos de Uso, onboarding de arquitetura de novos projetos e dashboards de templates prontos.

### 6. MCP Setup Stepper with Segmented Control (`.mcp-steps`)
- **Anatomia Visual**: Sequenciador numérico de 4 etapas (`1. Pick your editor`, `2. Get your key`, `3. Connect`, `4. Try it`). Inclui controle segmentado (`.seg`) para alternar instantaneamente entre editores (Cursor, Claude Code, VS Code, Other) sem recarregar a tela.
- **Gatilho de Interação**: Alternância de abas por clique com indicador deslizante de fundo e blocos de teste rápido com botões dedicados de cópia de prompt.
- **Onde encaixar**: Telas de configuração técnica, guias de integração de desenvolvedores e páginas de extensões para IDEs.

### 7. Weekly Hot 100 Leaderboard Row (`.ranking-row`)
- **Anatomia Visual**: Item de lista horizontal contendo número da posição (#1, #2), miniatura widescreen do componente/kit, título em semibold, badges de categoria (`components`, `motion`, `systems`), contagem de saves comunitários com ícone de bookmark e botão de acesso direto.
- **Gatilho de Interação**: Hover com leve elevação do container (`translate-y-[-2px]`), realce de borda e preview flutuante da miniatura da interface.
- **Onde encaixar**: Páginas de ranking de popularidade, seções de destaques semanais em portais de conteúdo e feeds comunitários.

### 8. Dot-Matrix Depth Panel (`.wb-panel` + `.wb-dots`)
- **Anatomia Visual**: Painel de conteúdo com cantos arredondados generosos (`rounded-2xl` a `rounded-3xl`), borda sutil de 1px e padrão de pontos geométricos de fundo com máscara radial gradiente (`mask-image: radial-gradient(...)`), criando a sensação de um tecido tecnológico flutuante.
- **Gatilho de Interação**: Efeito estático com alta performance renderizado em CSS puro, que pode responder suavemente à proximidade do cursor com leve ganho de iluminação.
- **Onde encaixar**: Containers de blocos centrais de landing page, seções de newsletter/inscrição e containers de chamada final para ação (Final CTA).

### 9. Multi-Lingual Popover Trigger (`.top-lang`)
- **Anatomia Visual**: Botão compacto com ícone vetorial de globo terráqueo, label de idioma atual ("English"), e micro-seta em chevron. Ao clicar, projeta um menu suspenso flutuante com elevação, sombra difusa e suporte a troca instantânea entre idiomas (Inglês, Japonês, Chinês simplificado).
- **Gatilho de Interação**: Clique ou foco via teclado abrindo popover posicionado via Radix UI/Floating UI com transição de opacidade e escala (`scale: 0.95 -> 1.0`).
- **Onde encaixar**: Canto superior direito da barra de navegação global (Navbar).

### 10. Floating Stacked Toast Notification Region (`.toast-region`)
- **Anatomia Visual**: Container flutuante ancorado na parte inferior central da viewport (`bottom-6 inset-x-0`). Exibe notificações em pilha tridimensional com fator de escala decrescente para itens em segundo plano (`--scale-factor: 0.05`), largura padronizada de 460px e espaçamento vertical milimétrico.
- **Gatilho de Interação**: Entrada automática com efeito de mola rápida (`spring`), deslocamento suave para cima ao surgir novo toast e descarte lateral com gesto de arrastar (`drag-to-dismiss`).
- **Onde encaixar**: Camada global de feedback do sistema para confirmação de cópia de comandos CLI, chaveamento de tema e sincronização de conta.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Pacotes
Para reproduzir a interface, as esteiras de marquee contínuas, os painéis de terminal interativo e as receitas do ecossistema UINice:

```bash
npm install framer-motion lucide-react clsx tailwind-merge
npx shadcn@latest init
npx shadcn@latest add button card badge
```

### Física de Movimento e Transições
- **Loop do Marquee Infinito**: Utiliza translação linear pura sem acelerações internas (`ease: "linear"`) via CSS Keyframes ou Framer Motion, garantindo que o movimento horizontal seja perfeitamente contínuo e sem solavancos nas costuras da esteira duplicada.
- **Física de Mola para Interação de Cards e Badges**:
  - `stiffness: 300`, `damping: 24`, `mass: 0.8` (rápido e responsivo, sem oscilação excessiva).
- **Transição de Feedback do Terminal e Copiador**:
  - `duration: 0.2s`, curva `ease: [0.16, 1, 0.3, 1]` (estilo Apple/Linear para micro-feedbacks táteis).

---

### Receita de Código: UINice Marquee & AI Recipe Explorer

O componente abaixo reproduz a essência arquitetural do UINice: uma esteira de marquee infinito com pause-on-hover, um card de receita de AI com terminal de comandos integrado e suporte a cópia instantânea:

```tsx
"use client";

import React, { useState } from "react";
import { motion } from "framer-motion";
import { 
  Terminal, 
  Check, 
  Copy, 
  ExternalLink, 
  Sparkles, 
  ArrowRight,
  Layers,
  Bot
} from "lucide-react";
import { cn } from "@/lib/utils";

// Interface para um item de componente ou kit
interface UIComponentShot {
  id: string;
  name: string;
  category: string;
  imageUrl: string;
  installCommand: string;
}

// Interface para a receita de composição (Recipe)
interface UIRecipe {
  title: string;
  concept: string;
  prompt: string;
  kits: {
    role: "Base" | "Input" | "Streaming" | "Icons";
    name: string;
    url: string;
    command: string;
  }[];
}

const SAMPLE_SHOTS_ROW_1: UIComponentShot[] = [
  { id: "shadcn-ui", name: "shadcn/ui", category: "systems", imageUrl: "https://images.unsplash.com/photo-1555066931-4365d14bab8c?w=600&auto=format&fit=crop&q=80", installCommand: "npx shadcn@latest init" },
  { id: "prompt-kit", name: "Prompt Kit", category: "components", imageUrl: "https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?w=600&auto=format&fit=crop&q=80", installCommand: "npx shadcn@latest add https://prompt-kit.com/c/prompt-input.json" },
  { id: "streamdown", name: "Streamdown", category: "components", imageUrl: "https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?w=600&auto=format&fit=crop&q=80", installCommand: "npm i streamdown" },
  { id: "lucide", name: "Lucide Icons", category: "icons", imageUrl: "https://images.unsplash.com/photo-1555066931-4365d14bab8c?w=600&auto=format&fit=crop&q=80", installCommand: "npm i lucide-react" },
];

const SAMPLE_SHOTS_ROW_2: UIComponentShot[] = [
  { id: "animata", name: "Animata UI", category: "motion", imageUrl: "https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?w=600&auto=format&fit=crop&q=80", installCommand: "npx animata add" },
  { id: "dice-ui", name: "Dice UI", category: "components", imageUrl: "https://images.unsplash.com/photo-1555066931-4365d14bab8c?w=600&auto=format&fit=crop&q=80", installCommand: "npx shadcn@latest add dice-ui" },
  { id: "unlumen-ui", name: "Unlumen UI", category: "systems", imageUrl: "https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?w=600&auto=format&fit=crop&q=80", installCommand: "npm i unlumen-ui" },
  { id: "morphicons", name: "Morphicons", category: "icons", imageUrl: "https://images.unsplash.com/photo-1555066931-4365d14bab8c?w=600&auto=format&fit=crop&q=80", installCommand: "npm i morphicons" },
];

const SAMPLE_RECIPE: UIRecipe = {
  title: "Calm AI Chat Screen",
  concept: "One centered conversation column, pinned prompt input with attachments, streaming markdown renderer and Lucide icons. Zero gradients, generous whitespace, one accent color.",
  prompt: `Build a calm AI chat screen with shadcn/ui on the neutral theme:
- Base: Theme Neutral from shadcn/ui (npx shadcn@latest init)
- Input: Prompt Input from prompt-kit (npx shadcn@latest add https://prompt-kit.com/c/prompt-input.json)
- Streaming: Streamdown (npm i streamdown)
- Icons: Lucide (npm i lucide-react)`,
  kits: [
    { role: "Base", name: "shadcn/ui Neutral", url: "https://ui.shadcn.com", command: "npx shadcn@latest init" },
    { role: "Input", name: "Prompt Input", url: "https://prompt-kit.com", command: "npx shadcn@latest add https://prompt-kit.com/c/prompt-input.json" },
    { role: "Streaming", name: "Streamdown", url: "https://streamdown.ai", command: "npm i streamdown" },
    { role: "Icons", name: "Lucide Icons", url: "https://lucide.dev", command: "npm i lucide-react" }
  ]
};

export function UINiceHeroSection() {
  const [copiedText, setCopiedText] = useState<string | null>(null);

  const handleCopy = (text: string, id: string) => {
    navigator.clipboard.writeText(text);
    setCopiedText(id);
    setTimeout(() => setCopiedText(null), 2200);
  };

  return (
    <section className="relative w-full overflow-hidden bg-zinc-950 py-24 text-zinc-100 antialiased selection:bg-zinc-800 selection:text-white">
      {/* 1. Malha de Fundo Pontilhada com Máscara Radial (.wb-dots) */}
      <div 
        className="pointer-events-none absolute inset-0 opacity-20 [background-image:radial-gradient(#a1a1aa_1px,transparent_1px)] [background-size:24px_24px] [mask-image:radial-gradient(ellipse_60%_50%_at_50%_40%,#000_70%,transparent_100%)]" 
        aria-hidden="true" 
      />

      <div className="relative mx-auto flex max-w-6xl flex-col items-center px-6 text-center">
        {/* 2. Action Pill Badge (.lp-pill) */}
        <motion.a
          href="#browse"
          initial={{ opacity: 0, y: -10 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.4, ease: [0.16, 1, 0.3, 1] }}
          className="group mb-8 inline-flex items-center gap-3 rounded-full border border-zinc-800 bg-zinc-900/90 px-3.5 py-1.5 text-xs text-zinc-300 shadow-inner backdrop-blur hover:border-zinc-700 hover:text-white transition-colors"
        >
          <span className="rounded-full bg-zinc-100 px-2 py-0.5 font-semibold text-zinc-950 text-[11px]">
            No design skills
          </span>
          <span className="font-medium">One line of code, designer-grade UI</span>
          <ArrowRight className="h-3.5 w-3.5 text-zinc-400 group-hover:translate-x-0.5 transition-transform" />
        </motion.a>

        {/* 3. Título Principal Hero */}
        <motion.h1 
          initial={{ opacity: 0, y: 14 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.5, delay: 0.1 }}
          className="max-w-3xl text-4xl font-semibold tracking-tight sm:text-6xl text-zinc-100"
        >
          Beautiful UI, <span className="italic font-serif font-normal text-zinc-300">ready to reuse.</span>
        </motion.h1>

        {/* 4. Descrição / Subtítulo */}
        <motion.p 
          initial={{ opacity: 0, y: 14 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.5, delay: 0.2 }}
          className="mt-6 max-w-2xl text-base text-zinc-400 sm:text-lg"
        >
          A hand-picked directory of UI kits for vibe coders. Every one comes with real code and is reviewed by a person.
        </motion.p>

        {/* 5. Painéis de Prova de Valor: Terminal Interativo + AI Prompt (.wb-panel) */}
        <div className="mt-14 grid w-full grid-cols-1 gap-6 md:grid-cols-2 text-left">
          {/* Card Esquerdo: Terminal Real com Cópia Rápida */}
          <div className="flex flex-col justify-between rounded-2xl border border-zinc-800/80 bg-zinc-900/40 p-6 backdrop-blur-sm">
            <div>
              <div className="flex items-center justify-between border-b border-zinc-800/80 pb-4">
                <div className="flex items-center gap-2 text-xs font-mono text-zinc-400">
                  <Terminal className="h-4 w-4 text-emerald-400" />
                  <span>Terminal Execution</span>
                </div>
                <button
                  onClick={() => handleCopy("npx shadcn@latest add button", "btn-install")}
                  className="inline-flex items-center gap-1.5 rounded-md border border-zinc-700/60 bg-zinc-800/60 px-2.5 py-1 text-xs text-zinc-300 hover:bg-zinc-700 hover:text-white transition-colors"
                >
                  {copiedText === "btn-install" ? (
                    <>
                      <Check className="h-3 w-3 text-emerald-400" />
                      <span>Copied</span>
                    </>
                  ) : (
                    <>
                      <Copy className="h-3 w-3" />
                      <span>Copy</span>
                    </>
                  )}
                </button>
              </div>

              {/* Simulação Visual do Terminal */}
              <div className="mt-4 rounded-xl bg-zinc-950 p-4 font-mono text-xs">
                <div className="flex items-center gap-2 text-zinc-300">
                  <span className="text-emerald-400 select-none">$</span>
                  <span>npx shadcn@latest add button</span>
                </div>
                <div className="mt-2 flex items-center gap-2 text-emerald-400/90">
                  <span className="select-none">✓</span>
                  <span className="text-zinc-400">Added components/ui/button.tsx</span>
                </div>
              </div>
            </div>

            <div className="mt-6">
              <h3 className="text-sm font-semibold text-zinc-200">Real code you can reuse</h3>
              <p className="mt-1 text-xs text-zinc-400">
                Every kit has an install line and a ready prompt for your AI. Copy one line and it's in your project.
              </p>
            </div>
          </div>

          {/* Card Direito: Conversação MCP com Cursor / Claude Code */}
          <div className="flex flex-col justify-between rounded-2xl border border-zinc-800/80 bg-zinc-900/40 p-6 backdrop-blur-sm">
            <div>
              <div className="flex items-center justify-between border-b border-zinc-800/80 pb-4">
                <div className="flex items-center gap-2 text-xs font-mono text-zinc-400">
                  <Bot className="h-4 w-4 text-violet-400" />
                  <span>Model Context Protocol (MCP)</span>
                </div>
                <span className="inline-flex items-center rounded-full bg-violet-950/80 px-2 py-0.5 text-[10px] font-medium text-violet-300 border border-violet-800/50">
                  Cursor & Claude
                </span>
              </div>

              {/* Balão de Diálogo de IA (.lp-chat) */}
              <div className="mt-4 rounded-xl bg-zinc-950 p-4 font-mono text-xs space-y-2.5">
                <div className="text-zinc-300">
                  <span className="text-zinc-500 select-none">Prompt: </span>
                  Find me a calm chat kit for Next.js
                </div>
                <div className="border-t border-zinc-800/60 pt-2 text-violet-300">
                  <span className="text-zinc-500 select-none">Response: </span>
                  ⏺ uinice · search_kits → 1. Prompt-Kit 2. Streamdown
                </div>
              </div>
            </div>

            <div className="mt-6">
              <h3 className="text-sm font-semibold text-zinc-200">Works in Cursor and Claude Code</h3>
              <p className="mt-1 text-xs text-zinc-400">
                Connect the UINice MCP and your AI editor discovers kits, reads their schemas and installs components autonomously.
              </p>
            </div>
          </div>
        </div>
      </div>

      {/* 6. Asynchronous Infinite Marquee Wall (.lp-wall) */}
      <div className="mt-20 w-full overflow-hidden border-y border-zinc-800/80 bg-zinc-950/80 py-8">
        {/* Linha 1: Movimento para a Esquerda (60s loop) */}
        <div className="flex w-max gap-6 hover:[animation-play-state:paused] animate-[marquee_60s_linear_infinite]">
          {[...SAMPLE_SHOTS_ROW_1, ...SAMPLE_SHOTS_ROW_1, ...SAMPLE_SHOTS_ROW_1].map((shot, idx) => (
            <div 
              key={`row1-${shot.id}-${idx}`}
              className="group relative h-48 w-80 flex-shrink-0 overflow-hidden rounded-xl border border-zinc-800 bg-zinc-900 transition-all duration-300 hover:border-zinc-600 hover:shadow-lg hover:shadow-zinc-950/50"
            >
              <img 
                src={shot.imageUrl} 
                alt={shot.name}
                className="h-full w-full object-cover transition-transform duration-500 group-hover:scale-105"
                loading="lazy"
              />
              <div className="absolute inset-0 bg-gradient-to-t from-zinc-950/90 via-zinc-950/20 to-transparent p-4 flex flex-col justify-end">
                <span className="text-xs font-mono text-zinc-400 uppercase tracking-wider">{shot.category}</span>
                <span className="text-sm font-semibold text-white">{shot.name}</span>
              </div>
            </div>
          ))}
        </div>

        {/* Linha 2: Movimento Reverso para a Direita (74s loop) */}
        <div className="mt-6 flex w-max gap-6 hover:[animation-play-state:paused] animate-[marquee-reverse_74s_linear_infinite]">
          {[...SAMPLE_SHOTS_ROW_2, ...SAMPLE_SHOTS_ROW_2, ...SAMPLE_SHOTS_ROW_2].map((shot, idx) => (
            <div 
              key={`row2-${shot.id}-${idx}`}
              className="group relative h-48 w-80 flex-shrink-0 overflow-hidden rounded-xl border border-zinc-800 bg-zinc-900 transition-all duration-300 hover:border-zinc-600 hover:shadow-lg hover:shadow-zinc-950/50"
            >
              <img 
                src={shot.imageUrl} 
                alt={shot.name}
                className="h-full w-full object-cover transition-transform duration-500 group-hover:scale-105"
                loading="lazy"
              />
              <div className="absolute inset-0 bg-gradient-to-t from-zinc-950/90 via-zinc-950/20 to-transparent p-4 flex flex-col justify-end">
                <span className="text-xs font-mono text-zinc-400 uppercase tracking-wider">{shot.category}</span>
                <span className="text-sm font-semibold text-white">{shot.name}</span>
              </div>
            </div>
          ))}
        </div>
      </div>

      {/* 7. Bloco da Receita Completa (Recipe Architecture Blueprint) */}
      <div className="mx-auto mt-24 max-w-4xl px-6">
        <div className="rounded-3xl border border-zinc-800 bg-zinc-900/60 p-8 backdrop-blur-md">
          <div className="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-4 border-b border-zinc-800 pb-6">
            <div>
              <div className="inline-flex items-center gap-2 text-xs font-mono text-zinc-400">
                <Sparkles className="h-4 w-4 text-amber-400" />
                <span>Recipe #001 · Multi-Kit Composition</span>
              </div>
              <h2 className="mt-1 text-2xl font-semibold text-zinc-100">{SAMPLE_RECIPE.title}</h2>
            </div>
            <button
              onClick={() => handleCopy(SAMPLE_RECIPE.prompt, "recipe-prompt")}
              className="inline-flex items-center justify-center gap-2 rounded-xl bg-white px-4 py-2.5 text-xs font-medium text-zinc-950 hover:bg-zinc-200 transition-colors self-start sm:self-auto"
            >
              {copiedText === "recipe-prompt" ? (
                <>
                  <Check className="h-4 w-4 text-emerald-600" />
                  <span>AI Prompt Copied</span>
                </>
              ) : (
                <>
                  <Copy className="h-4 w-4" />
                  <span>Copy AI Prompt</span>
                </>
              )}
            </button>
          </div>

          <p className="mt-4 text-sm text-zinc-400 leading-relaxed">
            {SAMPLE_RECIPE.concept}
          </p>

          {/* Grid de Dependências da Receita */}
          <div className="mt-6 grid grid-cols-1 gap-3 sm:grid-cols-2">
            {SAMPLE_RECIPE.kits.map((kit) => (
              <div 
                key={kit.role}
                className="flex items-center justify-between rounded-xl border border-zinc-800/80 bg-zinc-950/60 p-3.5 text-xs"
              >
                <div>
                  <span className="font-mono text-zinc-500 uppercase text-[10px] block">{kit.role}</span>
                  <span className="font-semibold text-zinc-200">{kit.name}</span>
                </div>
                <button
                  onClick={() => handleCopy(kit.command, kit.name)}
                  className="flex items-center gap-1 rounded bg-zinc-800/80 px-2 py-1 font-mono text-[11px] text-zinc-300 hover:bg-zinc-700 hover:text-white transition-colors"
                  title={kit.command}
                >
                  {copiedText === kit.name ? <Check className="h-3 w-3 text-emerald-400" /> : <Copy className="h-3 w-3" />}
                  <span>Install</span>
                </button>
              </div>
            ))}
          </div>
        </div>
      </div>
    </section>
  );
}
```

### Configuração de Keyframes no `tailwind.config.ts`
Para garantir a execução contínua com zero recálculos de layout das esteiras:

```ts
// tailwind.config.ts
export default {
  theme: {
    extend: {
      keyframes: {
        marquee: {
          "0%": { transform: "translateX(0%)" },
          "100%": { transform: "translateX(-50%)" },
        },
        "marquee-reverse": {
          "0%": { transform: "translateX(-50%)" },
          "100%": { transform: "translateX(0%)" },
        },
      },
      animation: {
        marquee: "marquee var(--duration, 60s) linear infinite",
        "marquee-reverse": "marquee-reverse var(--duration, 60s) linear infinite",
      },
    },
  },
};
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao selecionar o **UINice** como referência ou arquétipo de componentes e curadoria no documento de arquitetura de um novo projeto:

1. **Declaração do Ecossistema no Blueprint**:
   ```markdown
   ### UI Architecture & Component Hub
   - **Curadoria & Archetype**: UINice (Vibe Coder Craft / Hand-picked kits with real code)
   - **Design System Base (60%)**: shadcn/ui Neutral Mode (Zinc 950/900/50)
   - **Microinterações & Componentes Táticos (30%)**: Curadoria UINice (Prompt-Kit, Streamdown, Animata)
   - **Showstopper Visual (10%)**: Asynchronous Infinite Marquee + Interactive Terminal CLI Execution
   ```

2. **Adoção do Padrão "Recipe-First"**:
   - Em vez de descrever componentes soltos e desarticulados, estruture cada tela do projeto como uma **Receita Composta do UINice** (Base + Input + Feedback + Ícones).
   - Registre os comandos de instalação exatos (`npx shadcn@latest add ...`) e a dependência de ícones unificada (`lucide-react`).

3. **Padronização do Protocolo MCP**:
   - Recomende formalmente aos desenvolvedores da equipe ou ao agente de IA o uso do servidor MCP do UINice para inspeção de esquemas de novos componentes em tempo real durante sessões de codificação no Cursor ou Claude Code.

4. **Regras de Ouro de Consistência**:
   - **Unificação de Raio**: Travar `border-radius` em todas as bibliotecas compostas (ex: `rounded-xl` para containers, `rounded-lg` para inputs e botões).
   - **Monocromia Dominante**: Rejeitar gradientes arco-íris concorrentes; permitir apenas uma cor de destaque funcional (ex: `emerald-400` para status de sucesso do terminal, `violet-400` para ações de IA).
   - **Performance em Movimento**: O Marquee deve ser implementado estritamente via `transform: translate3d` com duplicação de itens estáticos e pausa ao hover, evitando listeners de mouse pesados na thread de renderização principal.
