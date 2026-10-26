---
id: "coss-ui"
name: "Coss UI (Origin UI)"
url: "https://coss.com/ui"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Base UI Headless Architecture", "Micro-Craft Form Precision", "Tailwind CSS v4 Native", "Commercial Open Source (COSS)", "Tactile Bevel & Depth Layering", "AI-First Component Particles"]
densidade_informacao: "Alta"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS nativo / Base UI unstyled headless)"
stack_frameworks: ["React 19 / 18", "Base UI (@base-ui/react)", "Radix UI Primitives (Origin Legacy)", "Tailwind CSS v4", "TypeScript", "Lucide React", "Motion / Framer Motion", "Tailwind Animate"]
compatibilidade:
  fontes_ideais: ["Cal Sans VF", "Geist Sans", "Inter", "Paper Mono", "JetBrains Mono", "Plus Jakarta Sans"]
  paletas_ideais: ["OKLCH Zinc & Sidebar Subtle Tint", "Deep Slate Monochrome", "Warm Industrial Stone", "Cal.com Production Dark/Light Theme"]
  combinacoes_recomendadas: ["shadcn/ui", "Aceternity UI", "Magic UI", "Sonner", "Vaul", "cmdk", "Tremor"]
  conflitos_esteticos: ["Neumorfismo difuso com blur excessivo", "Material Design 2 com elevações primárias pesadas", "Brutalismo Y2K sem alinhamento de grid e com tipografia caótica"]
---

# Coss UI (Origin UI) — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Coss UI** (hospedado oficialmente em `coss.com/ui` e mantido sob a infraestrutura da organização **Cal.com** e da iniciativa **COSS — Commercial Open Source Software**, sob liderança de Peer Richelsen com legado técnico originado no **Origin UI** criado por Davide Pacilio e Cruip) representa a fronteira mais avançada na convergência entre **design systems de altíssima precisão micro-visual ("Craft")**, **primitivas headless de última geração (Base UI)** e **ecossistemas orientados a desenvolvedores e agentes de Inteligência Artificial**.

Para compreender o impacto e a assinatura do Coss UI, é necessário analisar as quatro forças estruturais que compõem seu DNA:

### 1.1. A Evolução de Origin UI para Coss UI: Do Monocromático ao Padrão COSS
O Origin UI consagrou-se na comunidade global de desenvolvimento frontend como o catálogo definitivo de variações de micro-componentes. Enquanto bibliotecas tradicionais disponibilizavam apenas um botão ou um input genérico de texto, o Origin UI catalogou e refinou centenas de variações práticas para cada componente de formulário (inputs numéricos com steppers inline, caixas de busca com atalhos de teclado integrados, medidores de força de senha, campos de cartão de crédito formatados, etc.). 

Com a aquisição e transição pelo Cal.com, essa vasta experiência em micro-interações foi refinada e rebatizada como **Coss UI**, integrando uma arquitetura unificada de tokens modernos, novas primitivas de **Chat UI** para interfaces conversacionais de IA e um catálogo de mais de **529 "Particles"** (partículas de componentes prontas para cópia ou consumo por LLMs).

### 1.2. A Transição Histórica para Base UI (`@base-ui/react`)
Enquanto a maioria esmagadora das bibliotecas da era shadcn/ui permanece ancorada no Radix UI, o Coss UI lidera pioneiramente a adoção do **Base UI** — a biblioteca de componentes headless de última geração desenvolvida por engenheiros de renome da comunidade (incluindo membros chave vindos do Radix, Material UI e Floating UI, agora sob o ecossistema `@base-ui/react`).

Essa transição confere vantagens técnicas cruciais:
- **Alinhamento com APIs Modernas da Web**: Suporte de primeira classe à Popover API nativa do navegador, CSS Anchor Positioning e transições de entrada/saída mais leves.
- **Formulários e Campos Robustos**: Primitivas como `<Field.Root>`, `<Field.Control>`, `<Field.Label>`, `<Field.Description>` e `<Field.Error>` tratam acessibilidade, anúncios para leitores de tela e validações com semântica de formulário nativa sem a fragilidade de hacks de terceiros.
- **Desempenho e Menor Overhead de Nós DOM**: Base UI foi concebido especificamente para evitar wrappers desnecessários na árvore React, garantindo tempos de renderização reduzidos em telas de altíssima densidade.

### 1.3. A Assinatura Tátil: "Micro-Beveling", Dupla Camada e Sombras Perceptuais
A textura visual do Coss UI diferencia-se imediatamente de designs "planos" convencionais através de uma engenharia geométrica e lumínica meticulosa:
1. **Bordas Chanfradas Táteis (Micro-Beveling)**:
   Em vez de simples bordas uniformes de 1px, os componentes do Coss UI utilizam pseudo-elementos (`before:` e `after:`) com sombras internas e externas que simulam o reflexo de luz natural em arestas usinadas:
   - No Light Mode: `not-disabled:not-active:not-data-pressed:before:shadow-[0_1px_--theme(--color-black/4%)]`.
   - No Dark Mode: `dark:not-disabled:not-active:not-data-pressed:before:shadow-[0_-1px_--theme(--color-white/6%)]`.
   Isso gera uma suave linha de luz no topo do botão/card no modo escuro e uma sombra de assentamento no modo claro, conferindo peso tátil sem parecer skeuomórfico.
2. **Compressão Mecânica Ativa**:
   Ao clicar em botões e controles, o sistema simula o deslocamento físico de uma tecla mecânica via:
   `[:active,[data-pressed]]:inset-shadow-[0_1px_--theme(--color-black/8%)]` combinado a sutis compensações de profundidade.
3. **Cromatismo Perceptual com `color-mix`**:
   O sistema abandona opacidades cruas do CSS clássico em favor de interpolações em espaço perceptual:
   `bg-linear-to-b from-[color-mix(in_srgb,var(--card)_96%,var(--color-white))] to-[color-mix(in_srgb,var(--card)_99%,var(--color-black))]`.
4. **Ergonomia Tátil WCAG Invisível (`pointer-coarse`)**:
   Um dos maiores diferenciais técnicos do Coss UI está em sua atenção cirúrgica a dispositivos móveis. Em telas sensíveis ao toque, onde os dedos exigem áreas de toque de pelo menos 44x44px (WCAG 2.5.5), o Coss UI não deforma o tamanho visual do botão; ele injeta uma pseudo-área invisível via CSS:
   `pointer-coarse:after:absolute pointer-coarse:after:size-full pointer-coarse:after:min-h-11 pointer-coarse:after:min-w-11`.
   O botão mantém sua densidade visual compacta de 32px para o usuário, mas o leitor de toques expande o alvo físico para 44px (11 rems/unidades Tailwind).

### 1.4. A Camada "Particles": Atomização Extrema & Prontidão para IA
O Coss UI introduz o conceito formal de **Particles**: receitas de código atômicas altamente especializadas. Não se trata de uma coleção teórica de estilos, mas de 529+ variações funcionais prontas para casos de uso do mundo real. O repositório conta com integração direta com arquivos `llms.txt` e manifestos de contexto para que assistentes de codificação com IA gerem formulários complexos e interações completas sem alucinar dependências.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### 2.1. Nichos de Produto Recomendados

1. **SaaS B2B de Agendamento, Produtividade & Coordenação de Fluxos (Cal.com-Class)**:
   Sistemas onde a eficiência do usuário depende de agilidade em inputs de data/hora, fusos horários, caixas de seleção rápida de horários, botões divididos de confirmação e controles de alternância rápida de disponibilidade.
2. **Developer Tools, Portais Cloud, Consoles de API & Painéis de Infraestrutura**:
   Ambientes densos que necessitam de inputs de tokens de API com botão de revelação e cópia em um clique, seletores de ambiente com badges de status embutidas, sliders de alocação de memória/CPU com marcações de intervalo precisas e atalhos globais de teclado (`⌘K`).
3. **Fintechs, Checkout de Alta Conversão & Formulários de Pagamento**:
   Campos especializados com detecção visual de bandeiras de cartão de crédito, formatação automática de moeda, máscara de código de segurança (CVV), seletores de parcelamento em formato de cards de rádio e botões com transição de loading suave para evitar duplo envio acidental.
4. **Aplicações de Inteligência Artificial & Agentes Conversacionais**:
   Com o módulo nativo de **Chat UI**, o Coss UI é perfeito para produtos que integram LLMs, interfaces de chat interativo com cards colapsáveis de raciocínio lógico, botões de ação contextuais em respostas de agentes e sugestões rápidas de prompts em estilo "pills".
5. **Formulários de Autenticação Segura & Onboarding Complexo**:
   Inputs de código OTP/PIN multi-célula com preenchimento automático via clipboard, medidores visuais de força de senha que reagem a regex em tempo real e steppers de múltiplas etapas com navegação fluida.

### 2.2. Papel no Ritmo Visual (A Aplicação Rigorosa da Regra 60-30-10)

- **60% — Fundação Operacional e Camada de Entrada de Dados (A Alma do Coss UI)**:
  O Coss UI brilha principalmente como a espinha dorsal de formulários e controles da aplicação. Todos os campos de texto, áreas de texto, selects nativos/customizados, tabelas com filtros e separadores devem ser derivados de suas primitivas. A neutralidade monocromática de seus tons Zinc/Slate garante que o usuário mantenha o foco na tarefa cognitiva.
- **30% — Feedback Tátil e Navegação Dinâmica**:
  As micro-interações do Coss UI (abas com indicador deslizante, acordeões com animação CSS suave, drawers laterais, menus suspensos posicionados via Base UI Floating engine e tooltips de sliders com valor dinâmico) compõem a camada de resposta sensorial da interface.
- **10% — Partículas Protagonistas de Entrada de Dados (Showstoppers de Precisão)**:
  Ao contrário de outras bibliotecas cujos showstoppers são efeitos visuais de fundo ou animações 3D extravagantes, no Coss UI o protagonismo de 10% é exercido pelas suas **Partículas Especiais de Formulário**: um medidor de força de senha tridimensional com 4 barras animadas e checklist de requisitos dinâmicos, ou um seletor visual de planos em cards interativos com bordas de realce e micro-animação no check.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Portfólios Artísticos, Narrativas Editoriais Imersivas & Sites 3D/WebGL**:
  Sites institucionais que dependem de tipografia destrutiva gigante, animações de câmera 3D (Three.js/Spline) ou rolagem horizontal contínua não se beneficiam de uma biblioteca otimizada para formulários, botões de precisão e produtividade de dados.
- **Projetos Legados sem Pipeline de Build Moderno ou Presos a Tailwind v3 Antigo**:
  O Coss UI faz uso intensivo das novidades do **Tailwind CSS v4** (`@theme`, sintaxe de espaçamento CSS funcional `--spacing(x)`, filtros e gradientes com `bg-linear-to-*`, `color-mix(in srgb, ...)` e `inset-shadow`). Tentar compilá-lo em setups legados do Webpack com Tailwind v2 ou v3 sem configuração de compatibilidade gerará erros de parsing CSS.
- **Aplicações que Exigem Look-and-Feel Idêntico a Plataformas Mobile Nativas Estritas**:
  Se o cliente corporativo exige fidelidade absoluta ao Material You da Google (com suas superfícies de elevação com tons de cor primária saturada) ou ao UIKit nativo da Apple (iOS nativo estrito), adaptar o visual de usinagem e micro-bevel do Coss UI exigirá refatorações estruturais de classes.

---

### ⚠️ Erros Comuns de Exagero & Como Evitar o Efeito "Component Showcase Clichê"

1. **A Armadilha do "Showcase Slop" (Misturar 10 Partículas Diferentes na Mesma Página)**:
   O maior perigo ao utilizar uma biblioteca com centenas de variantes fascinantes é transformar o formulário de login em uma vitrine caótica: colocar um input com ícone à esquerda, outro com stepper numérico à direita, outro com badge superior e outro com ação inline transparente. 
   *Diretriz*: Escolha **um único padrão consistente de input** por fluxo de formulário. Se adotar labels superiores com borda suave, mantenha todos os campos sob essa mesma anatomia.
2. **Ignorar a Escala de Densidade e Quebrar a Ergonomia Mobile**:
   Tentar forçar botões compactos (`sm:h-8` ou `h-7`) sem manter a classe utilitária `pointer-coarse:after:min-h-11` fará com que usuários em smartphones enfrentem frustração ao tentar tocar em botões minúsculos. Nunca remova as pseudo-classes `pointer-coarse`.
3. **Reimplementação Redundante de Estado Nativo**:
   O Base UI gerencia automaticamente estados como `data-pressed`, `data-hover`, `data-disabled`, `data-open` e `data-focus-visible`. Tentar controlar esses estados manualmente via React `useState` ou classes manuais no clique cria conflitos de renderização e desativa o suporte a leitores de tela.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão detalhados **10 dos componentes e partículas mais emblemáticos** do ecossistema Coss UI (Origin UI):

### 4.1. Input: Password Strength Meter & Interactive Validator
- **Anatomia Visual**: Campo de senha de alta segurança acompanhado por um botão de alternância de visibilidade do tipo "olho" no canto direito. Abaixo do campo, exibe 4 barras segmentadas de progresso que mudam dinamicamente de tom (vermelho carmim, âmbar, amarelo ouro e verde esmeralda) conforme o cálculo de entropia da senha (comprimento, letras minúsculas, maiúsculas, números e caracteres especiais), acompanhado por um checklist dinâmico com micro-ícones de verificação.
- **Gatilho de Interação**: Digitação contínua no teclado com debounce nulo para transições cromáticas instantâneas; clique no ícone para alternar o tipo de input entre `password` e `text`.
- **Onde Encaixar**: Telas de cadastro (Sign Up), modais de redefinição de credenciais corporativas e painéis de segurança de conta.

### 4.2. Input: Inline Action & Instant Search com Kbd Shortcut (`⌘K`)
- **Anatomia Visual**: Campo de busca horizontal elegante com ícone de lupa na extremidade esquerda e um bloco compacto de teclas emuladas (`<kbd>⌘</kbd><kbd>K</kbd>`) na extremidade direita. Ao digitar, o atalho é substituído suavemente por um botão circular de limpeza rápida (`X`) e um indicador de loading rotativo sutil caso haja debounce assíncrono.
- **Gatilho de Interação**: Foco automático via atalho de teclado global (`keydown` ouvindo `Meta+K` ou `Ctrl+K`), digitação e clique de limpeza.
- **Onde Encaixar**: Header principal da aplicação, topo de tabelas com filtros complexos e barras de ferramentas de produtividade.

### 4.3. Input: OTP / PIN Verification Matrix (Células Segmentadas)
- **Anatomia Visual**: Conjunto de 4 a 6 caixas quadradas perfeitamente proporcionais, com cantos arredondados, fundo suavemente escurecido e borda de destaque ativo com anel luminescente de 2px. Apresenta um cursor piscante customizado centralizado em cada célula.
- **Gatilho de Interação**: Foco sequencial automático à medida que cada dígito é digitado; deleção com recuo de foco no `Backspace`; suporte completo a colar (`paste`) que distribui instantaneamente todos os dígitos entre as células.
- **Onde Encaixar**: Fluxos de autenticação multifator (2FA/MFA), confirmação de transações financeiras e validação de e-mail por código numérico.

### 4.4. Slider: Dual-Thumb Range com Tooltip de Valor Dinâmico Flutuante
- **Anatomia Visual**: Trilha horizontal fina com preenchimento da área ativa entre dois cursores circulares táteis. Cada thumb possui um anel de foco refinado e projeta uma sombra nítida de 1px. Ao interagir, emerge acima de cada cursor um balão de tooltip com o valor numérico exato formatado (ex: `$50` a `$500`).
- **Gatilho de Interação**: Arraste por ponteiro (`drag`), clique direto na trilha para reposicionamento e navegação de precisão via setas do teclado (`ArrowLeft` / `ArrowRight`).
- **Onde Encaixar**: Filtros de faixa de preço em e-commerces, seletores de capacidade computacional em consoles de nuvem e controles de intervalo de data/duração.

### 4.5. Button: Tactile Push & Micro-Beveled Action Button
- **Anatomia Visual**: Botão primário construído com bordas micro-chanfradas (`before:shadow` superior no dark mode e inferior no light mode), gradiente linear sutil de cima para baixo e estado de loading que substitui o conteúdo por um spinner mantendo as dimensões exatas do botão sem saltos de layout (*layout shift*).
- **Gatilho de Interação**: Hover com iluminação suave; clique ativo que aciona o afundamento visual (`inset-shadow`); suporte a toque mobile com ampliação da área de captura para 44px via `pointer-coarse`.
- **Onde Encaixar**: Botões de chamada para ação principal (CTA), gatilhos de submissão de formulários críticos e ações de salvar alterações.

### 4.6. Checkbox & Radio: Interactive Selection Cards (Pricing & Tier Matrix)
- **Anatomia Visual**: Em vez de pequenas caixas de seleção isoladas, o componente engloba um card interativo completo com título, descrição resumida, valor monetário e um indicador visual de seleção (círculo com ponto ou quadrado com check) no canto superior. Quando ativo, o card recebe uma borda primária com leve gradiente de preenchimento e um anel sutil de realce.
- **Gatilho de Interação**: Clique em qualquer área do card; foco via teclado com transição de anel via `focus-visible`; suporte a múltiplos estados selecionados (Checkbox) ou seleção mutuamente exclusiva (Radio).
- **Onde Encaixar**: Seleção de planos de assinatura em páginas de checkout, escolha de métodos de pagamento e seleção de papéis de permissão de usuário (RBAC).

### 4.7. Tabs: Sliding Indicator / Segmented Control
- **Anatomia Visual**: Barra de abas compacta com fundo neutro atenuado e uma "pílula" de seleção ativa que desliza de forma contínua por trás do texto da aba selecionada, proporcionando um efeito de seleção física fluida.
- **Gatilho de Interação**: Clique de seleção ou navegação via setas direcionais do teclado (`ArrowLeft`/`ArrowRight`), com interpolação de largura e deslocamento horizontal calculado matematicamente.
- **Onde Encaixar**: Alternância de visualizações em dashboards (ex: "Gráfico" vs "Tabela"), painéis de configurações e filtros de período temporal (Diário, Semanal, Mensal).

### 4.8. Accordion: Animated Hairline Panel com Rotação de Chevrons
- **Anatomia Visual**: Lista de seções expansíveis delimitadas por separadores de 1px (`divide-y divide-border`). Cada cabeçalho possui tipografia estruturada e um ícone de chevron que rotaciona 180 graus com suavidade calculada. O conteúdo expande-se sem saltos através de animação CSS Grid pura (`grid-template-rows: 0fr -> 1fr`).
- **Gatilho de Interação**: Clique no cabeçalho ou navegação via teclado com abertura por `Enter`/`Space`.
- **Onde Encaixar**: Seções de perguntas frequentes (FAQ), formulários longos divididos em passos colapsáveis e detalhes complementares de transações financeiras.

### 4.9. Stepper: Multi-Step Progress Tracker
- **Anatomia Visual**: Indicador horizontal de etapas conectadas por linhas de progresso sólidas. Cada etapa é representada por um nó circular contendo o número da etapa ou um ícone de "check" caso concluída. O nó atual exibe um anel de destaque pulsante suave e o rótulo semântico da etapa logo abaixo.
- **Gatilho de Interação**: Atualização do estado do formulário; clique em etapas anteriores para revisão rápida e bloqueio de etapas futuras inacessíveis.
- **Onde Encaixar**: Fluxos de onboarding com múltiplos passos, finalização de compra com etapas de frete/pagamento e assistentes de configuração de servidores.

### 4.10. Chat UI: Conversational Bubble, Prompt Pills & Action Bar
- **Anatomia Visual**: Módulo nativo especializado em interfaces conversacionais de IA. Inclui balões de mensagem com renderização tipográfica limpa, painéis de pensamento colapsáveis (*reasoning cards*), barras de ação flutuantes com botões de cópia em um clique e feedback de utilidade (thumbs up/down), e uma barra inferior com chips de sugestões rápidas de comandos.
- **Gatilho de Interação**: Envio de mensagens via teclado (`Enter` com `Shift+Enter` para quebra de linha), clique nos chips de sugestão e expansão dos detalhes de raciocínio.
- **Onde Encaixar**: Co-pilotos de IA em plataformas SaaS, assistentes de atendimento automatizado e interfaces de geração de código ou texto.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### 5.1. Dependências & Setup de Ambiente

O Coss UI utiliza como fundamento as primitivas unstyled do **Base UI** (`@base-ui/react`), ícones do **Lucide React** e estilização via **Tailwind CSS v4**:

```bash
# Instalação das dependências fundamentais
pnpm add @base-ui/react lucide-react clsx tailwind-merge
pnpm add -D tailwindcss @tailwindcss/vite # ou postcss setup para Tailwind v4
```

Caso deseje adicionar partículas via CLI compatível com Shadcn/Registry:
```bash
# Adicionando um componente do registry Coss UI
pnpm dlx shadcn@latest add @coss/ui/button
pnpm dlx shadcn@latest add @coss/ui/slider
```

### 5.2. O Helper Canônico `cn` (`lib/utils.ts`)

```typescript
import { clsx, type ClassValue } from "clsx";
import { twMerge } from "tailwind-merge";

export function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs));
}
```

### 5.3. Física de Movimento, Interpolações & Timing

O Coss UI prioriza **transições via CSS moderno de alta eficiência** para a grande maioria das interações diárias, recorrendo a transições com aceleração cúbica personalizada que imitam a dinâmica de molas mecânicas:

- **Curva de Easing Padrão Coss UI**:
  ```css
  --ease-coss: cubic-bezier(0.16, 1, 0.3, 1);
  --duration-quick: 150ms;
  --duration-normal: 250ms;
  ```
- **Configuração de Spring para Componentes Animados (Motion / Framer Motion)**:
  Quando há necessidade de interpolação física contínua (como o indicador deslizante de Abas ou painéis de Sheet):
  ```typescript
  export const cossSpringConfig = {
    type: "spring",
    stiffness: 450,
    damping: 32,
    mass: 0.8,
  };
  ```
- **Técnica de Acordeão com CSS Grid (Zero Javascript para Cálculo de Altura)**:
  Em vez de calcular `scrollHeight` via JS, o Coss UI anima a propriedade de grid fracionário:
  ```css
  .accordion-content {
    display: grid;
    grid-template-rows: 0fr;
    transition: grid-template-rows 250ms cubic-bezier(0.16, 1, 0.3, 1);
  }
  .accordion-content[data-open] {
    grid-template-rows: 1fr;
  }
  .accordion-inner {
    overflow: hidden;
  }
  ```

---

### 5.4. Receitas de Código Realistas & Funcionais

#### Receita 1: Micro-Craft Beveled Button (Botão Chanfrado com Suporte a Toque Mobile)

Este componente demonstra a anatomia exata de botões do Coss UI: iluminação superior no dark mode, sombreamento no light mode, compressão no clique e área de toque WCAG invisível para telas sensíveis ao toque (`pointer-coarse`).

```tsx
import * as React from "react";
import { cn } from "@/lib/utils";
import { Loader2 } from "lucide-react";

export interface CossButtonProps
  extends React.ButtonHTMLAttributes<HTMLButtonElement> {
  variant?: "primary" | "secondary" | "outline" | "ghost" | "destructive";
  size?: "sm" | "md" | "lg" | "icon";
  isLoading?: boolean;
}

export const Button = React.forwardRef<HTMLButtonElement, CossButtonProps>(
  (
    {
      className,
      variant = "primary",
      size = "md",
      isLoading = false,
      disabled,
      children,
      ...props
    },
    ref
  ) => {
    // Variantes de preenchimento e camadas de chanfro (micro-bevel)
    const variantStyles = {
      primary: cn(
        "border-primary bg-primary text-primary-foreground shadow-xs shadow-primary/25",
        "hover:bg-primary/90 data-pressed:bg-primary/90",
        // Inset shadow de topo simulando iluminação direta
        "not-disabled:inset-shadow-[0_1px_--theme(--color-white/16%)]",
        // Inset shadow de base quando comprimido
        "[:active,[data-pressed]]:inset-shadow-[0_1px_--theme(--color-black/12%)]"
      ),
      secondary: cn(
        "border-input bg-popover text-foreground shadow-xs/5",
        "hover:bg-accent/60 data-pressed:bg-accent/60",
        // Micro-bevel frontal duplo (light vs dark)
        "not-disabled:not-active:not-data-pressed:before:shadow-[0_1px_--theme(--color-black/4%)]",
        "dark:bg-input/30 dark:hover:bg-input/60 dark:data-pressed:bg-input/60",
        "dark:not-disabled:not-active:not-data-pressed:before:shadow-[0_-1px_--theme(--color-white/6%)]"
      ),
      outline: cn(
        "border-border bg-transparent text-foreground hover:bg-accent hover:text-accent-foreground",
        "data-pressed:bg-accent"
      ),
      ghost: cn(
        "border-transparent text-foreground hover:bg-accent data-pressed:bg-accent"
      ),
      destructive: cn(
        "border-destructive bg-destructive text-destructive-foreground shadow-xs shadow-destructive/25",
        "hover:bg-destructive/90 data-pressed:bg-destructive/90",
        "not-disabled:inset-shadow-[0_1px_--theme(--color-white/16%)]"
      ),
    };

    const sizeStyles = {
      sm: "h-8 px-3 text-xs gap-1.5 [&_svg]:size-3.5",
      md: "h-9 px-4 text-sm gap-2 [&_svg]:size-4",
      lg: "h-10 px-5 text-base gap-2.5 [&_svg]:size-4.5",
      icon: "size-9 p-0 [&_svg]:size-4",
    };

    return (
      <button
        ref={ref}
        disabled={disabled || isLoading}
        data-loading={isLoading ? "" : undefined}
        className={cn(
          // Estrutura física base
          "relative inline-flex shrink-0 cursor-pointer items-center justify-center whitespace-nowrap",
          "rounded-lg border font-medium outline-none transition-all duration-150 select-none",
          // Pseudo-elemento de anel chanfrado
          "before:pointer-events-none before:absolute before:inset-0 before:rounded-[calc(var(--radius-lg,8px)-1px)]",
          // ERGONOMIA TÁTIL WCAG: expande o hitbox físico em telas touch sem alterar o visual
          "pointer-coarse:after:absolute pointer-coarse:after:size-full pointer-coarse:after:min-h-11 pointer-coarse:after:min-w-11",
          // Acessibilidade de foco
          "focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-1 focus-visible:ring-offset-background",
          // Estados desabilitados e de carregamento
          "disabled:pointer-events-none disabled:opacity-50",
          "data-loading:select-none data-loading:text-transparent",
          // Aplicação de variantes
          variantStyles[variant],
          sizeStyles[size],
          className
        )}
        {...props}
      >
        {isLoading && (
          <span className="absolute inset-0 flex items-center justify-center text-current">
            <Loader2 className="size-4 animate-spin" />
          </span>
        )}
        {children}
      </button>
    );
  }
);
Button.displayName = "CossButton";
```

---

#### Receita 2: Password Strength Input Particle com Indicador de Entropia

Esta receita reproduz a partícula clássica de validação visual de senha do ecossistema Origin/Coss UI, utilizando cálculo reativo de segurança e transição de cores.

```tsx
import * as React from "react";
import { Eye, EyeOff, Check, X } from "lucide-react";
import { cn } from "@/lib/utils";

export function PasswordStrengthInput() {
  const [password, setPassword] = React.useState("");
  const [isVisible, setIsVisible] = React.useState(false);

  // Requisitos e validação
  const requirements = [
    { label: "Pelo menos 8 caracteres", met: password.length >= 8 },
    { label: "Contém letra maiúscula", met: /[A-Z]/.test(password) },
    { label: "Contém número", met: /[0-9]/.test(password) },
    { label: "Contém caractere especial (@$!%*?&)", met: /[^A-Za-z0-9]/.test(password) },
  ];

  const score = requirements.filter((r) => r.met).length;

  // Mapa de cores e rótulos de entropia
  const getStrengthMeta = () => {
    switch (score) {
      case 0:
        return { label: "Muito fraca", color: "bg-muted" };
      case 1:
        return { label: "Fraca", color: "bg-red-500" };
      case 2:
        return { label: "Razoável", color: "bg-amber-500" };
      case 3:
        return { label: "Boa", color: "bg-yellow-500" };
      case 4:
        return { label: "Excelente", color: "bg-emerald-500" };
      default:
        return { label: "", color: "bg-muted" };
    }
  };

  const strengthMeta = getStrengthMeta();

  return (
    <div className="w-full max-w-sm space-y-3 font-sans">
      <div className="flex items-center justify-between">
        <label className="text-xs font-medium text-foreground">
          Senha Segura
        </label>
        {password && (
          <span className="text-xs font-medium text-muted-foreground transition-opacity">
            {strengthMeta.label}
          </span>
        )}
      </div>

      {/* Caixa do Input com Bevel e Ação Inline */}
      <div className="relative flex items-center">
        <input
          type={isVisible ? "text" : "password"}
          value={password}
          onChange={(e) => setPassword(e.target.value)}
          placeholder="Digite sua senha..."
          className={cn(
            "h-9 w-full rounded-lg border border-input bg-popover px-3 pr-10 text-sm text-foreground shadow-xs/5",
            "outline-none transition-all placeholder:text-muted-foreground/60",
            "focus-visible:border-ring focus-visible:ring-2 focus-visible:ring-ring/20",
            "dark:bg-input/30"
          )}
        />
        <button
          type="button"
          onClick={() => setIsVisible(!isVisible)}
          className="absolute right-2.5 text-muted-foreground/70 hover:text-foreground focus:outline-none"
          title={isVisible ? "Ocultar senha" : "Ver senha"}
        >
          {isVisible ? <EyeOff className="size-4" /> : <Eye className="size-4" />}
        </button>
      </div>

      {/* 4 Barras de Progresso Segmentadas */}
      <div className="grid grid-cols-4 gap-1.5 pt-1" aria-hidden="true">
        {[0, 1, 2, 3].map((index) => (
          <div
            key={index}
            className={cn(
              "h-1.5 rounded-full transition-all duration-300",
              index < score ? strengthMeta.color : "bg-muted/60"
            )}
          />
        ))}
      </div>

      {/* Checklist Dinâmico de Requisitos */}
      <ul className="space-y-1 pt-1 text-xs text-muted-foreground">
        {requirements.map((req, i) => (
          <li key={i} className="flex items-center gap-2">
            {req.met ? (
              <Check className="size-3.5 text-emerald-500" />
            ) : (
              <X className="size-3.5 text-muted-foreground/40" />
            )}
            <span className={req.met ? "text-foreground font-medium" : ""}>
              {req.label}
            </span>
          </li>
        ))}
      </ul>
    </div>
  );
}
```

---

#### Receita 3: Dual-Thumb Range Slider com Base UI (`@base-ui/react/slider`)

Esta receita demonstra a integração autêntica com o pacote oficial de primitivas **Base UI**, criando um controle de faixa dupla com tooltips táteis e manipulação fluida.

```tsx
import * as React from "react";
import { Slider } from "@base-ui/react/slider";
import { cn } from "@/lib/utils";

interface PriceRangeSliderProps {
  min?: number;
  max?: number;
  step?: number;
  defaultValue?: [number, number];
  onValueChange?: (val: [number, number]) => void;
}

export function PriceRangeSlider({
  min = 0,
  max = 1000,
  step = 10,
  defaultValue = [150, 650],
  onValueChange,
}: PriceRangeSliderProps) {
  const [values, setValues] = React.useState<[number, number]>(defaultValue);

  const handleValueChange = (newValues: number[]) => {
    const tuple: [number, number] = [newValues[0], newValues[1]];
    setValues(tuple);
    onValueChange?.(tuple);
  };

  return (
    <div className="w-full max-w-sm space-y-4 font-sans">
      <div className="flex items-center justify-between text-xs font-medium text-foreground">
        <span>Faixa de Preço</span>
        <span className="font-mono tabular-nums text-muted-foreground">
          ${values[0]} — ${values[1]}
        </span>
      </div>

      <Slider.Root
        value={values}
        onValueChange={handleValueChange}
        min={min}
        max={max}
        step={step}
        className="relative flex w-full touch-none select-none items-center py-2"
      >
        {/* Trilha do Slider */}
        <Slider.Track className="relative h-1.5 w-full grow rounded-full bg-muted overflow-hidden">
          {/* Indicador de Preenchimento Ativo */}
          <Slider.Indicator className="absolute h-full bg-primary" />
        </Slider.Track>

        {/* Primeiro Thumb (Mínimo) */}
        <Slider.Thumb
          index={0}
          className={cn(
            "group relative block size-4.5 rounded-full border border-border/80 bg-background shadow-xs",
            "outline-none transition-transform hover:scale-110",
            "focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 focus-visible:ring-offset-background",
            "cursor-grab active:cursor-grabbing active:scale-95"
          )}
        >
          {/* Tooltip Dinâmico ao Passar o Mouse ou Foco */}
          <div className="pointer-events-none absolute -top-7 left-1/2 -translate-x-1/2 opacity-0 group-hover:opacity-100 group-focus-visible:opacity-100 transition-opacity duration-150">
            <span className="rounded bg-popover px-1.5 py-0.5 font-mono text-[10px] font-semibold text-popover-foreground shadow-xs border border-border">
              ${values[0]}
            </span>
          </div>
        </Slider.Thumb>

        {/* Segundo Thumb (Máximo) */}
        <Slider.Thumb
          index={1}
          className={cn(
            "group relative block size-4.5 rounded-full border border-border/80 bg-background shadow-xs",
            "outline-none transition-transform hover:scale-110",
            "focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 focus-visible:ring-offset-background",
            "cursor-grab active:cursor-grabbing active:scale-95"
          )}
        >
          <div className="pointer-events-none absolute -top-7 left-1/2 -translate-x-1/2 opacity-0 group-hover:opacity-100 group-focus-visible:opacity-100 transition-opacity duration-150">
            <span className="rounded bg-popover px-1.5 py-0.5 font-mono text-[10px] font-semibold text-popover-foreground shadow-xs border border-border">
              ${values[1]}
            </span>
          </div>
        </Slider.Thumb>
      </Slider.Root>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao arquitetar um novo projeto ou declarar o **Coss UI (Origin UI)** dentro do documento de especificação (`DESIGN_BLUEPRINT.md`), os agentes e arquitetos devem seguir rigorosamente as seguintes diretrizes:

### 6.1. Declaração Formal da Camada no Blueprint

```markdown
### Design System & Component Foundation: Coss UI (Base UI + Tailwind v4)
- **Biblioteca Primária de Formulários e Controles**: Coss UI (Origin UI evolution)
- **Camada Headless**: `@base-ui/react` (Base UI) para novos componentes; Radix UI Primitives para utilitários legados compatíveis.
- **Estilização**: Tailwind CSS v4 com `@theme` semântico, variáveis OKLCH e gradientes direcionais modernos (`bg-linear-to-*`).
- **Padrão de Propriedade**: Código local direto em `components/ui/` (Copy-Paste / Registry CLI).
- **Proporção na Regra 60-30-10**:
  - 60% Estrutura (Coss UI Inputs, Buttons, Form Fields, Popovers).
  - 30% Micro-interações (Abas deslizantes, Acordeões em CSS Grid, Sliders de intervalo).
  - 10% Showstoppers de Dados (Password Entropy Meter, OTP Matrix, Chat UI Agents).
```

### 6.2. Regras de Tokens & Tipografia Mandatórias
1. **Tipografia de Cabeçalhos e Código**:
   - Utilize fontes com alto suporte geométrico e tabular: **Cal Sans VF**, **Geist Sans** ou **Inter** para títulos e corpo; **Paper Mono** ou **JetBrains Mono** para rótulos de valores, atalhos de teclado (`<kbd>`) e dados financeiros tabulares.
2. **Tokens de Superfície e Efeito Bevel**:
   - Manter obrigatoriamente as classes de chanfro duplo nos botões e cartões (`before:shadow` sutil invertido entre dark e light mode), preservando a identidade visual tátil característica do Cal.com.
3. **Salvaguarda de Acessibilidade Móvel**:
   - É proibido remover a classe `pointer-coarse:after:min-h-11` de botões compactos. Todo componente interativo compacto deve manter sua área tátil de 44px garantida para smartphones.
4. **Matriz de Decisão: Base UI vs Coss UI Particles vs Shadcn UI Tradicional**:
   - Se o requisito for um componente genérico básico de layout (ex: Avatar, Separator simples): use o padrão canônico do Shadcn UI.
   - Se o requisito for um **formulário rico com interação específica** (ex: campo de busca com atalho embutido, seletor de faixa dupla, entrada de código OTP, validação em tempo real de senha, ou interface conversacional de IA): **deve-se adotar compulsoriamente a Partícula correspondente do Coss UI**.
