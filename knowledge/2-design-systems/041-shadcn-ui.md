---
id: "shadcn-ui"
name: "Shadcn UI"
url: "https://ui.shadcn.com/"
category: "2-design-systems"
schema_type: "A-components"
dna_estetico: ["Modern Craft Minimal", "Radix Headless Architecture", "Semantic Token Theming", "Tailwind v4 Native", "Precision Utility Enterprise"]
densidade_informacao: "Flexivel"
impacto_visual: "Utilitario/Base"
custo_computacional: "Baixo (CSS/Headless)"
stack_frameworks: ["React 19 / 18", "Next.js (App Router / RSC)", "Tailwind CSS v4 & v3", "Radix UI Primitives", "TypeScript", "Lucide React", "React Hook Form", "Zod", "TanStack Table", "Recharts", "Sonner", "Vaul", "cmdk"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "Plus Jakarta Sans", "Satoshi", "General Sans", "JetBrains Mono"]
  paletas_ideais: ["OKLCH Semantic Palettes", "Zinc & Slate Monochromes", "Warm Neutral (Stone/Amber)", "Deep Cobalt & Titanium Gray", "Obsidian Dark Mode"]
  combinacoes_recomendadas: ["Aceternity UI", "Magic UI", "Cult UI", "Motion Primitives", "Kibo UI", "Framer Motion", "Tailwind Animate"]
  conflitos_esteticos: ["Neumorfismo skeuomórfico pesado", "Material Design 2 com sombras primárias excessivas", "Brutalismo Y2K desordenado sem alinhamento de grid"]
---

# Shadcn UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Shadcn UI**, concebido e mantido pelo engenheiro Shadcn (@shadcn), é o marco divisor mais relevante da engenharia de front-end contemporânea pós-2022. Mais do que uma biblioteca de componentes convencional, o Shadcn UI redefiniu fundamentalmente a relação entre desenvolvedores e seus componentes de interface através de dois conceitos revolucionários: **Propriedade Total do Código (Code Ownership / Copy-Paste Architecture)** e o **Protocolo Aberto de Registries (Registry CLI)**.

### A Ruptura com o Modelo Monolítico de Componentes
Historicamente, bibliotecas de UI corporativas (como Material-UI/MUI, Ant Design e Chakra UI) eram consumidas como pacotes monolíticos de terceiros via NPM. Esse modelo aprisionava as equipes em abstrações opacas:
- Alterar comportamentos internos ou customizar o markup exigia batalhas desgastantes com seletores CSS de especificidade artificialmente inflada (`!important`, styled-components aninhados, APIs de temas engessadas).
- Atualizações de versão frequentemente quebravam componentes inteiros do sistema.
- A árvore de dependências do NPM acumulava peso morto e dependências legadas que o projeto jamais utilizava.

O Shadcn UI subverteu esse paradigma: **não existe o pacote `npm install @shadcn/ui`**. Em vez disso, o desenvolvedor utiliza uma CLI de distribuição de código (`npx shadcn@latest add <component>`) que injeta o código-fonte puro em TypeScript, estilizado com Tailwind CSS e alimentado por primitivas headless acessíveis (principalmente Radix UI), diretamente na pasta local do projeto (`components/ui/`). O código torna-se integralmente seu: totalmente editável, auditável, livre de dependências ocultas e adaptável às particularidades exatas do produto.

### A Assinatura Visual: "Craft Minimalism" & Precisão de Tokens
A estética padrão do Shadcn UI — muitas vezes rotulada como "Modern Vercel / Linear Aesthetic" — caracteriza-se pelo equilíbrio cirúrgico entre sofisticação visual e sobriedade utilitária:
1. **Camada de Superfície & Tokens Semânticos OKLCH**:
   Toda a paleta de cores é governada por pares semânticos estritos (`background` / `foreground`, `card` / `card-foreground`, `popover` / `popover-foreground`, `primary` / `primary-foreground`, `muted` / `muted-foreground`, `accent` / `accent-foreground`, `destructive` / `destructive-foreground`, `border`, `input`, `ring`). No Tailwind CSS v4, o sistema adota nativamente o espaço de cor **OKLCH** (`oklch(0.145 0 0)`), garantindo uniformidade perceptual de luminosidade e cromatismo entre diferentes tonalidades e prevenindo a descoloração cinzenta típica do espaço sRGB ao alternar temas Claro/Escuro.
2. **Hairlines, Anéis de Foco & Hierarquia Geométrica**:
   Em vez de bordas espessas ou sombras artificiais carregadas, o Shadcn emprega bordas ultrafinas ("hairlines" de 1px com tons atenuados via `--border`), anéis de foco acessíveis baseados em `ring-offset` (`focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2`) e sombras estruturais discretas (`shadow-xs`, `shadow-sm`). O raio de curvatura é padronizado por uma variável mestre (`--radius`), com subdivisões matemáticas rigorosas para containers aninhados (`calc(var(--radius) - 2px)` para botões internos, evitando cantos que vazam fora da curvatura do pai).
3. **Atributos de Slot (`data-slot`) & Arquitetura Tailwind v4**:
   Na sua evolução mais recente para Tailwind v4 e React 19, os componentes utilizam atributos semânticos `data-slot="card-header"`, `data-slot="button"`, permitindo estilização contextual limpa e extensões via CSS moderno com `@theme inline` sem inflar a lista de classes utilitárias diretas.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados
1. **SaaS B2B, Plataformas Enterprise & Backoffices Operacionais**:
   Aplicações corporativas que exigem centenas de formulários, validações complexas, modais aninhados, tabelas com paginação e menus densos. A solidez de acessibilidade (WCAG AA/AAA via Radix UI) e a previsibilidade estrutural tornam o Shadcn a espinha dorsal padrão da indústria.
2. **Developer Tools, Bancos de Dados & Painéis de Infraestrutura Cloud**:
   Ambientes de alta intensidade técnica (no padrão Vercel, Supabase, Neon, Cloudflare, Resend) onde comandos via teclado (`Cmd+K`), menus contextuais de clique direito, sidebars retráteis com atalhos e tooltips precisos são indispensáveis.
3. **Plataformas de IA, Chat Interfaces & Agentes Autônomos**:
   Interfaces conversacionais onde componentes de formulário, streaming de markdown via typography/typeset, barras laterais com histórico de sessões e cards colapsáveis de raciocínio lógico precisam de renderização limpa e fluida.
4. **Design Systems Proprietários de Grande Porte (White-Label)**:
   Empresas que precisam criar seu próprio sistema corporativo (ex: "Acme Design System"). Em vez de reinventar primitives acessíveis do zero, utilizam o Shadcn como camada base, publicando seu próprio registro privado via especificação de Registry aberta.

### Papel no Ritmo Visual (A Aplicação Rigorosa da Regra 60-30-10)

- **60% — Espinha Dorsal Absoluta da Interface (A Fundação Neutra)**:
  O Shadcn UI foi desenhado especificamente para cumprir com maestria o papel de **fundação estrutural de 60%**. Ele gerencia todas as superfícies estáticas e formulários: fundos de página, cartões de agrupamento, inputs de texto, botões neutros, tabelas, tipografia estrutural, badges informativos e separadores. Nenhuma animação invasiva ou efeito de luz deve existir nesta camada.
- **30% — Camada de Navegação, Orquestração e Micro-interações**:
  Os componentes dinâmicos do Shadcn (a `Sidebar` colapsável com persistência via cookie, a paleta `Command` acionada por `Cmd+K`, o `DropdownMenu`, o `Sheet` lateral e os toasts do `Sonner`) conduzem a experiência de navegação e fornecem feedback instantâneo de transição.
- **10% — Showstoppers Protagonistas (Bibliotecas Satélites)**:
  O Shadcn UI **não é** e **nunca deve ser** tratado como o showstopper (o 10%). A sua beleza reside justamente na sobriedade que permite que componentes showstopper reais (efeitos de partículas do Aceternity UI, gradientes vivos do Magic UI ou shaders WebGL) brilhem sem sobrecarregar a cognição do usuário.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Websites Cinematográficos & Experiências 3D Imersivas (WebGL / Three.js / GSAP)**:
  Portfólios de alta arte, campanhas publicitárias de moda ou lançamentos de carros focados em transições contínuas de câmera 3D e tipografia destrutiva não se beneficiam de uma biblioteca orientada a caixas retangulares e formulários de produtividade.
- **Projetos sem Pipeline de Build Moderno / Monólitos Legados**:
  Tentativas de importar Shadcn em ecossistemas legados sem suporte a bundlers modernos (ex: templates PHP/Django puros sem Vite/Next.js/Tailwind) geram atrito desnecessário.
- **Aplicações onde o cliente exige look-and-feel 100% nativo de uma plataforma fechada**:
  Se o projeto exige cópia idêntica do Human Interface Guidelines da Apple (iOS nativo) ou do Material You puro da Google (Android nativo), bibliotecas especializadas naquelas plataformas são mais indicadas.

---

### ⚠️ A Síndrome do "Default Shadcn" & Como Fugir do Clichê Genérico

O sucesso monumental do Shadcn UI gerou um efeito colateral evidente na web global: a proliferação massiva de centenas de produtos que parecem cópias idênticas e indistinguíveis uns dos outros. Um projeto cai na armadilha do **"Default Shadcn Slop"** quando mantém a tríade padrão:
> *Fundo `#09090b` (Zinc 950) + Fonte Geist Sans/Inter + Border radius de 0.5rem + Botão primário preto sólido com texto branco sem textura.*

Esse visual passa a percepção de ser um mero protótipo automatizado por ferramentas de IA generativa (como v0 ou Bolt) sem acabamento humano ou identidade de marca autêntica.

#### 5 Estratégias Mandatórias para Personalizar o Shadcn e Torná-lo Único:

1. **Manipulação Radical de Border Radius (`--radius`)**:
   - Para uma estética **Technical / High-Density Swiss Architecture**: Reduza o `--radius` para `0rem` ou `0.125rem` (cantos quase vivos ou 100% retos, bordas de 1px sólidas, aparência de terminal financeiro ou blueprint).
   - Para uma estética **Warm Consumer / Modern Neo-Bank**: Aumente o `--radius` para `1rem` ou `1.25rem` (superfícies orgânicas, botões em estilo "pill" de alta ergonomia tátil).
2. **Engenharia de Sombras Volumétricas (Substituindo o Shadow Padrão)**:
   Substitua as sombras cinzas genéricas por pilhas multicamadas afinadas com matizes quentes ou frias:
   ```css
   /* Shadow Stack Artesanal para Cards Shadcn */
   --shadow-craft: 
     0 1px 2px oklch(0 0 0 / 4%),
     0 4px 8px -2px oklch(0 0 0 / 6%),
     0 12px 24px -4px oklch(0 0 0 / 8%);
   ```
3. **Substituição Tipográfica de Caráter**:
   Abandone a combinação preguiçosa `Inter + Inter`. Adote contrastes intencionais:
   - *Editorial / Finanças*: Títulos em serif contemporânea (`Newsreader`, `Fraunces` ou `Instrument Serif`) combinados com corpo em `Satoshi` ou `General Sans`.
   - *Futurista / Cyber*: Títulos em `Space Grotesk` ou `PP Neue Montreal` com monoespaçada `JetBrains Mono` em labels e tabelas.
4. **Superfícies Texturizadas & Inner Hairlines (Inset Borders)**:
   Em temas escuros, adicione bordas internas reflexivas usando sombras internas em vez de apenas `border-border`:
   ```css
   /* Efeito de Vidro Fosco Tátil */
   box-shadow: inset 0 1px 0 0 oklch(1 0 0 / 10%), 0 1px 2px oklch(0 0 0 / 30%);
   ```
5. **Cromas Vivos com Paletas OKLCH Autenticadas**:
   Troque o cinza monocromático sem vida por bases com matiz sutil: base ardósia nórdica (leve tom azulado), base carvão florestal (leve matiz esmeralda profundo) ou base terracota desaturada.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 10 componentes mais fundamentais e avançados da arquitetura do Shadcn UI:

### 1. Sidebar 2.0 (Sistema Modular de Navegação Enterprise)
- **Anatomia Visual**: Arquitetura modular composta por `<SidebarProvider>`, `<Sidebar>`, `<SidebarHeader>`, `<SidebarContent>`, `<SidebarGroup>`, `<SidebarMenu>`, `<SidebarMenuItem>`, `<SidebarMenuButton>`, `<SidebarFooter>` e `<SidebarRail>`. Suporta três modos de exibição: `sidebar` clássica, `floating` (cartão destacado que flutua a 8px da borda) e `inset` (onde a sidebar emoldura a área de conteúdo como uma prancheta de design).
- **Gatilho de Interação**: Atalho de teclado global (`Cmd+B` / `Ctrl+B`), clique no `<SidebarTrigger>`, transição para versão recolhida apenas com ícones com suporte a tooltips automáticos e persistência de estado via cookie no servidor (zero layout shift em Next.js SSR). No mobile, abre automaticamente como uma gaveta lateral fluida.
- **Onde encaixar na página**: Estrutura mestre de SaaS, painéis administrativos, consoles de banco de dados e IDEs web.

### 2. Command Palette (`cmdk` Headless Integration)
- **Anatomia Visual**: Modal flutuante suspenso com backdrop blur escuro. Possui um campo de busca centralizado com ícone de lupa, divisor sutil e lista agrupada categoricamente (`CommandGroup`, `CommandItem`, `CommandSeparator`). Itens contêm ícone à esquerda, rótulo textual e tags de atalho de teclado estilizadas (`<kbd className="bg-muted text-muted-foreground ...">Cmd+P</kbd>`) alinhadas à direita.
- **Gatilho de Interação**: Tecla de atalho global `Cmd+K` / `Ctrl+K` ou clique em botão simulador de busca no cabeçalho. Navegação completa via setas do teclado com scroll automático e seleção com `Enter`.
- **Onde encaixar na página**: Barra de navegação superior (Navbar global), central de comando de SaaS ou atalho rápido de busca em documentações.

### 3. Responsive Dialog / Drawer Híbrido (Vaul + Radix Dialog)
- **Anatomia Visual**: Padrão arquitetural adaptativo de alta ergonomia. Em telas desktop (`md: min-width: 768px`), renderiza um `Dialog` flutuante centralizado com backdrop escurecido e escala sutil de entrada. Em telas mobile, alterna automaticamente para um `Drawer` inferior (bottom sheet baseado no Vaul) com alça tátil no topo (`<div className="mx-auto h-1.5 w-12 rounded-full bg-muted" />`), permitindo arrasto por gesto físico com snap points.
- **Gatilho de Interação**: Clique em botões de ação ("Editar Configurações", "Criar Novo Projeto", "Visualizar Detalhes").
- **Onde encaixar na página**: Modais de edição de perfil, wizards de configuração, fluxos de checkout e formulários contextuais responsivos.

### 4. Data Table TanStack (Headless Enterprise Grid)
- **Anatomia Visual**: Tabela de dados de nível profissional construída sobre `@tanstack/react-table`. Inclui barra superior com input de busca com debounce, filtros facetados em popover com contadores numéricos, botão de alternância de visibilidade de colunas (`DropdownMenu`), cabeçalhos clicáveis com ícones de ordenação ascendente/descendente (`ArrowUpDown`), seleção em lote via checkboxes, e barra de rodapé com paginação e seletor de quantidade de itens por página.
- **Gatilho de Interação**: Digitação no filtro, clique no cabeçalho para ordenar, clique nas checkboxes para seleção em massa, botões de próxima página.
- **Onde encaixar na página**: Painéis de gestão de usuários, extratos financeiros, registros de auditoria, catálogo de produtos em e-commerce.

### 5. Form Engine (React Hook Form + Zod + Accessibility Primitives)
- **Anatomia Visual**: Sistema declarativo composto por `<Form>`, `<FormField>`, `<FormItem>`, `<FormLabel>`, `<FormControl>`, `<FormDescription>` e `<FormMessage>`. Integração nativa de acessibilidade: vincula automaticamente IDs exclusivos com atributos `aria-describedby` e define `aria-invalid="true"` dinamicamente. Mensagens de erro surgem com animação de expansão de altura suave e cor semântica destrutiva.
- **Gatilho de Interação**: Validação em tempo real no evento `onChange` ou `onBlur` com feedback visual imediato e bloqueio de submissão incorreta no `onSubmit`.
- **Onde encaixar na página**: Telas de login e registro, formulários de cobrança, onboarding em etapas e telas de configurações de conta.

### 6. Charts & Visualização de Dados (Recharts + Tokens CSS Semânticos)
- **Anatomia Visual**: Camada de abstração sobre Recharts (`<ChartContainer>`, `<ChartTooltip>`, `<ChartTooltipContent>`, `<ChartLegend>`). Resolve o maior defeito do Recharts (estilos inline hardcoded) permitindo que as cores das linhas, barras e áreas venham diretamente de tokens CSS (`--chart-1` a `--chart-5` ou variáveis de tema) compatíveis com modo Claro/Escuro sem re-renderização de canvas. Tooltips dinâmicos exibem indicadores circulares coloridos e valores devidamente formatados.
- **Gatilho de Interação**: Movimento do cursor (hover) sobre barras ou pontos da linha; o cursor projeta uma linha de mira vertical e dispara o tooltip com animação de fade.
- **Onde encaixar na página**: Dashboard de métricas financeiras, gráficos de faturamento mensal, telemetria de servidores e uso de cotas de API.

### 7. Sonner Toast System (Notificações Flutuantes por Emil Kowalski)
- **Anatomia Visual**: Pilha de toasts flutuantes posicionada nos cantos da tela (`top-right`, `bottom-right`, etc.). Suporta empilhamento tridimensional com efeito sanfona tátil (quando múltiplos toasts acumulam, eles se recolhem em camadas com escala reduzida e deslocamento Y, expandindo-se suavemente ao passar o mouse). Inclui suporte a ícones semânticos (sucesso, erro, alerta), barra de progresso de auto-fechamento e botões de ação integrados.
- **Gatilho de Interação**: Disparado programmaticamente via `toast.success("Salvo com sucesso")`, `toast.error()` ou `toast.promise(promessa, { loading: 'Carregando...', success: 'Pronto!' })`.
- **Onde encaixar na página**: Provedor global no root layout da aplicação (`<Toaster />`); acionado em respostas de mutações de banco de dados, cópia para a área de transferência e alertas de conexão.

### 8. Navigation Menu (Menu com Viewport Compartilhado Flutuante)
- **Anatomia Visual**: Menu horizontal de alta elegância onde múltiplos itens com dropdown compartilham um único container flutuante (`NavigationMenuViewport`). Quando o usuário move o cursor de uma aba para outra, o container não desaparece e reaparece: ele desliza fisicamente no eixo X e redimensiona suavemente sua largura e altura para acomodar o novo conteúdo sem saltos bruscos.
- **Gatilho de Interação**: Hover sobre itens principais do menu com temporizador de tolerância de saída (evitando fechamento acidental) e navegação completa por teclado.
- **Onde encaixar na página**: Cabeçalho de navegação (Header / Navbar) de landing pages ricas, marketplaces e plataformas de documentação.

### 9. Sheet (Gaveta Lateral / Slide-over Panel)
- **Anatomia Visual**: Painel lateral que desliza a partir de qualquer borda da tela (`right`, `left`, `top`, `bottom`) com backdrop escuro e desfoque gaussiano suave. Possui cabeçalho fixo com botão de fechar (X), área de rolagem interna (`overflow-y-auto`) e rodapé fixo para botões de confirmação/cancelamento.
- **Gatilho de Interação**: Clique em botões como "Filtros Avançados", "Ver Detalhes do Pedido" ou carrinho de compras lateral em e-commerce.
- **Onde encaixar na página**: Carrinho lateral ("Slide-in Cart"), painel de filtros de catálogo, pré-visualização rápida de documentos sem sair da tela principal.

### 10. Dropdown Menu & Context Menu
- **Anatomia Visual**: Menus flutuantes calculados geometricamente para evitar vazamentos fora da viewport. Apresentam agrupamentos semânticos com divisores sutis, suporte a atalhos de teclado alinhados à direita, submenus aninhados que deslizam lateralmente e suporte a checkboxes e radio buttons selecionáveis com ícones de verificação.
- **Gatilho de Interação**: O `DropdownMenu` abre com clique esquerdo em botões como "Ações (...)" ou menu de usuário. O `ContextMenu` abre ao pressionar o botão direito do mouse em qualquer área demarcada da interface.
- **Onde encaixar na página**: Botão de opções em linhas de tabelas, avatar de perfil de usuário com opções de Logout/Configurações, e áreas interativas de editores/dashboards.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Configuração de Arquitetura (`components.json`)
O coração do Shadcn UI em qualquer projeto é o seu arquivo de manifesto na raiz:
```json
{
  "$schema": "https://ui.shadcn.com/schema.json",
  "style": "new-york",
  "rsc": true,
  "tsx": true,
  "tailwind": {
    "config": "tailwind.config.js",
    "css": "app/globals.css",
    "baseColor": "neutral",
    "cssVariables": true,
    "prefix": ""
  },
  "aliases": {
    "components": "@/components",
    "utils": "@/lib/utils",
    "ui": "@/components/ui",
    "lib": "@/lib",
    "hooks": "@/hooks"
  },
  "iconLibrary": "lucide-react"
}
```

### O Utilitário Central: `cn()` (`lib/utils.ts`)
Toda a composição de classes utilitárias no ecossistema Shadcn depende exclusivamente da fusão inteligente entre `clsx` (condicionais booleanos limpos) e `tailwind-merge` (resolução correta de conflitos de precedência de classes):
```typescript
import { clsx, type ClassValue } from "clsx"
import { twMerge } from "tailwind-merge"

export function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs))
}
```

---

### Física de Movimento & Curvas de Transição
Diferente de bibliotecas com animações extravagantes, o Shadcn prioriza a velocidade de percepção do usuário e a acessibilidade. As transições CSS nativas usam a curva de aceleração de decaimento rápido:
- **Curva Predileta Radix / Shadcn**: `cubic-bezier(0.16, 1, 0.3, 1)` (curva elástica de resposta imediata com amortecimento elegante, típica de interfaces Apple e Raycast).
- **Duração Padrão**: `150ms` para micro-interações de botões e tooltips; `200ms` a `300ms` para diálogos, gavetas e acordeões.
- **Variáveis Radix para Acordeões & Colapsáveis**:
  ```css
  /* Animação com altura dinâmica precisa sem salto de frame */
  @keyframes accordion-down {
    from { height: 0; }
    to { height: var(--radix-accordion-content-height); }
  }
  @keyframes accordion-up {
    from { height: var(--radix-accordion-content-height); }
    to { height: 0; }
  }
  ```
- **Configuração de Mola Recomendada para Framer Motion Acoplado**:
  ```typescript
  export const subtleSpring = {
    type: "spring",
    stiffness: 400,
    damping: 30,
    mass: 0.8
  }
  ```

---

### Receitas de Código Funcionais

#### Receita 1: Design Tokens Modernos em Tailwind v4 com OKLCH & Overrides Anti-Default
Exemplo de configuração no arquivo de estilos globais (`app/globals.css`) que substitui a estética cinzenta genérica por uma paleta sofisticada com matiz quente de grafite e âmbar sutil:

```css
@import "tailwindcss";

@layer base {
  :root {
    --background: oklch(0.99 0.002 90);
    --foreground: oklch(0.14 0.01 60);
    --card: oklch(1 0 0);
    --card-foreground: oklch(0.14 0.01 60);
    --popover: oklch(1 0 0);
    --popover-foreground: oklch(0.14 0.01 60);
    --primary: oklch(0.25 0.03 50);
    --primary-foreground: oklch(0.98 0 0);
    --secondary: oklch(0.95 0.005 60);
    --secondary-foreground: oklch(0.2 0.02 50);
    --muted: oklch(0.94 0.005 60);
    --muted-foreground: oklch(0.48 0.01 60);
    --accent: oklch(0.92 0.02 85);
    --accent-foreground: oklch(0.2 0.02 50);
    --destructive: oklch(0.58 0.22 25);
    --destructive-foreground: oklch(0.98 0 0);
    --border: oklch(0.88 0.008 60);
    --input: oklch(0.88 0.008 60);
    --ring: oklch(0.4 0.05 50);
    --radius: 0.625rem;
    
    /* Tokens dedicados para Sidebar corporativa */
    --sidebar: oklch(0.97 0.003 70);
    --sidebar-foreground: oklch(0.25 0.01 60);
    --sidebar-primary: oklch(0.25 0.03 50);
    --sidebar-primary-foreground: oklch(0.98 0 0);
    --sidebar-accent: oklch(0.93 0.01 70);
    --sidebar-accent-foreground: oklch(0.15 0.01 60);
    --sidebar-border: oklch(0.90 0.005 70);
  }

  .dark {
    --background: oklch(0.12 0.01 60);
    --foreground: oklch(0.94 0.005 60);
    --card: oklch(0.15 0.01 60);
    --card-foreground: oklch(0.94 0.005 60);
    --popover: oklch(0.16 0.01 60);
    --popover-foreground: oklch(0.94 0.005 60);
    --primary: oklch(0.96 0.01 80);
    --primary-foreground: oklch(0.12 0.01 60);
    --secondary: oklch(0.20 0.01 60);
    --secondary-foreground: oklch(0.92 0 0);
    --muted: oklch(0.19 0.01 60);
    --muted-foreground: oklch(0.60 0.01 60);
    --accent: oklch(0.24 0.02 70);
    --accent-foreground: oklch(0.96 0 0);
    --destructive: oklch(0.55 0.2 25);
    --destructive-foreground: oklch(0.98 0 0);
    --border: oklch(0.22 0.01 60);
    --input: oklch(0.22 0.01 60);
    --ring: oklch(0.70 0.03 70);

    --sidebar: oklch(0.10 0.01 60);
    --sidebar-foreground: oklch(0.85 0.01 60);
    --sidebar-primary: oklch(0.96 0.01 80);
    --sidebar-primary-foreground: oklch(0.10 0.01 60);
    --sidebar-accent: oklch(0.16 0.01 60);
    --sidebar-accent-foreground: oklch(0.96 0 0);
    --sidebar-border: oklch(0.18 0.01 60);
  }
}
```

---

#### Receita 2: Componente Híbrido Responsivo (Dialog no Desktop / Drawer no Mobile + Validação Zod + Sonner)
Este padrão unifica o `Dialog` do Radix UI com o `Drawer` do Vaul, criando uma experiência tátil impecável em qualquer resolução:

```tsx
"use client"

import * as React from "react"
import { useMediaQuery } from "@/hooks/use-media-query"
import { Button } from "@/components/ui/button"
import {
  Dialog,
  DialogContent,
  DialogDescription,
  DialogHeader,
  DialogTitle,
  DialogTrigger,
} from "@/components/ui/dialog"
import {
  Drawer,
  DrawerClose,
  DrawerContent,
  DrawerDescription,
  DrawerFooter,
  DrawerHeader,
  DrawerTitle,
  DrawerTrigger,
} from "@/components/ui/drawer"
import { Input } from "@/components/ui/input"
import { Label } from "@/components/ui/label"
import { toast } from "sonner"
import { z } from "zod"
import { useForm } from "react-hook-form"
import { zodResolver } from "@hookform/resolvers/zod"

const projectSchema = z.object({
  name: z.string().min(3, "O nome deve ter no mínimo 3 caracteres"),
  slug: z.string().min(2, "Slug inválido").regex(/^[a-z0-9-]+$/, "Apenas letras minúsculas e hífens"),
})

type ProjectFormValues = z.infer<typeof projectSchema>

export function ResponsiveProjectModal() {
  const [open, setOpen] = React.useState(false)
  const isDesktop = useMediaQuery("(min-width: 768px)")

  const form = useForm<ProjectFormValues>({
    resolver: zodResolver(projectSchema),
    defaultValues: { name: "", slug: "" },
  })

  function onSubmit(data: ProjectFormValues) {
    setOpen(false)
    toast.success(`Projeto "${data.name}" criado com sucesso!`, {
      description: `Identificador único: ${data.slug}`,
    })
    form.reset()
  }

  const FormContent = (
    <form onSubmit={form.handleSubmit(onSubmit)} className="grid items-start gap-4 px-4 sm:px-0">
      <div className="grid gap-2">
        <Label htmlFor="name">Nome do Projeto</Label>
        <Input id="name" placeholder="Ex: Motor de Análise IA" {...form.register("name")} />
        {form.formState.errors.name && (
          <p className="text-xs text-destructive">{form.formState.errors.name.message}</p>
        )}
      </div>
      <div className="grid gap-2">
        <Label htmlFor="slug">Slug do Repositório</Label>
        <Input id="slug" placeholder="motor-de-analise-ia" {...form.register("slug")} />
        {form.formState.errors.slug && (
          <p className="text-xs text-destructive">{form.formState.errors.slug.message}</p>
        )}
      </div>
      <Button type="submit" disabled={form.formState.isSubmitting} className="w-full mt-2">
        Criar Espaço de Trabalho
      </Button>
    </form>
  )

  if (isDesktop) {
    return (
      <Dialog open={open} onOpenChange={setOpen}>
        <DialogTrigger asChild>
          <Button variant="default">Novo Projeto</Button>
        </DialogTrigger>
        <DialogContent className="sm:max-w-[425px]">
          <DialogHeader>
            <DialogTitle>Criar Novo Projeto</DialogTitle>
            <DialogDescription>
              Configure o ambiente de trabalho inicial para o seu time.
            </DialogDescription>
          </DialogHeader>
          {FormContent}
        </DialogContent>
      </Dialog>
    )
  }

  return (
    <Drawer open={open} onOpenChange={setOpen}>
      <DrawerTrigger asChild>
        <Button variant="default">Novo Projeto</Button>
      </DrawerTrigger>
      <DrawerContent>
        <DrawerHeader className="text-left">
          <DrawerTitle>Criar Novo Projeto</DrawerTitle>
          <DrawerDescription>
            Configure o ambiente de trabalho inicial para o seu time.
          </DrawerDescription>
        </DrawerHeader>
        {FormContent}
        <DrawerFooter className="pt-2">
          <DrawerClose asChild>
            <Button variant="outline">Cancelar</Button>
          </DrawerClose>
        </DrawerFooter>
      </DrawerContent>
    </Drawer>
  )
}
```

---

#### Receita 3: Botão de Ação com Efeito "Tactile Craft" Anti-Default
Como transformar o botão clássico do Shadcn em uma peça de design tátil refinado, com borda interna iluminada (hairline highlight) e micro-rebaixamento físico ao clicar:

```tsx
import * as React from "react"
import { Slot } from "@radix-ui/react-slot"
import { cva, type VariantProps } from "class-variance-authority"
import { cn } from "@/lib/utils"

const craftButtonVariants = cva(
  "inline-flex items-center justify-center gap-2 whitespace-nowrap rounded-[var(--radius)] text-sm font-medium transition-all duration-150 focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50 active:scale-[0.98]",
  {
    variants: {
      variant: {
        craftPrimary:
          "bg-foreground text-background shadow-[0_1px_2px_rgba(0,0,0,0.1),inset_0_1px_0_0_rgba(255,255,255,0.2)] hover:bg-foreground/90 active:shadow-[inset_0_2px_4px_rgba(0,0,0,0.2)]",
        craftElevated:
          "bg-card text-card-foreground border border-border shadow-[0_1px_1px_rgba(0,0,0,0.05),0_4px_6px_-2px_rgba(0,0,0,0.05),inset_0_1px_0_0_rgba(255,255,255,0.1)] hover:bg-accent hover:border-border/80 hover:shadow-[0_2px_4px_rgba(0,0,0,0.08)]",
        craftSubtle:
          "hover:bg-muted/80 text-muted-foreground hover:text-foreground",
      },
      size: {
        default: "h-9 px-4 py-2",
        sm: "h-8 rounded-md px-3 text-xs",
        lg: "h-10 rounded-md px-8",
        icon: "h-9 w-9",
      },
    },
    defaultVariants: {
      variant: "craftPrimary",
      size: "default",
    },
  }
)

export interface CraftButtonProps
  extends React.ButtonHTMLAttributes<HTMLButtonElement>,
    VariantProps<typeof craftButtonVariants> {
  asChild?: boolean
}

export const CraftButton = React.forwardRef<HTMLButtonElement, CraftButtonProps>(
  ({ className, variant, size, asChild = false, ...props }, ref) => {
    const Comp = asChild ? Slot : "button"
    return (
      <Comp
        className={cn(craftButtonVariants({ variant, size, className }))}
        ref={ref}
        {...props}
      />
    )
  }
)
CraftButton.displayName = "CraftButton"
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao arquitetar uma nova aplicação e documentar suas especificações no `DESIGN_BLUEPRINT.md`, a inteligência artificial e os arquitetos de software devem seguir estas regras estritas para componentes baseados em Shadcn UI:

1. **Declaração do Registro & Estrutura de Diretórios**:
   - Registrar expressamente o Shadcn UI como a **Camada Base de Sistema (Nível 60%)**.
   - Garantir que o `components.json` aponte aliases claros (`@/components/ui` para primitivas Shadcn e `@/components/craft` ou `@/components/features` para componentes de negócio).
2. **Mandato Anti-Default (Cláusula de Personalização)**:
   - **Proibição expressa**: É terminantemente proibido manter o tema padrão com fundo `zinc-950` e fonte `Inter` pura sem justificativa explícita no Blueprint.
   - Definir obrigatoriamente a família tipográfica alternativa (ex: Geist Sans + JetBrains Mono, ou Satoshi + Newsreader).
   - Definir expressamente o valor numérico de `--radius` (ex: `0.125rem` para estética técnica/blueprint, ou `0.75rem` para estética fluida/moderna).
   - Especificar a paleta de tokens com coordenadas OKLCH em `globals.css`.
3. **Matriz de Responsabilidade de Componentes**:
   - *Estrutura de Aplicação*: Utilizar `Sidebar 2.0` (com `SidebarProvider`) com cookies de sessão para persistir estado entre páginas no Next.js.
   - *Interações de Busca*: Declarar a `Command Palette` (`cmdk`) com listener de evento `Cmd+K`.
   - *Formulários & Mutações*: Obrigatoriedade do trio `react-hook-form` + `zod` + `FormItem` para qualquer entrada de dados, acompanhado do `sonner` para feedback de submissão.
   - *Modais Mobile-First*: Empregar a receita híbrida `ResponsiveDialogDrawer` para formulários e telas secundárias em vez de modais desktop rígidos que quebram no celular.
4. **Governança de Showstoppers (Regra 60-30-10)**:
   - O Shadcn fornece os 60% neutros e os 30% de navegação fluida.
   - Os 10% de showstopper devem ser delegados a bibliotecas dedicadas (Aceternity UI, Magic UI, Shaders) e isolados em no máximo **1 elemento protagonista por dobra visual**.
