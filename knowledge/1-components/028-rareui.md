---
id: "rare-ui"
name: "Rare UI"
url: "https://www.rareui.com/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Apple-Inspired Tactile Craft", "Rare & Kinetic Micro-Interactions", "Shadcn Registry Native", "AI Copilot & Multimodal UI", "Squircle Geometry & Flubber Morphing", "Raw WebGL Shaders & Canvas Physics"]
densidade_informacao: "Media a Flexivel"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Baixo (Tailwind/CSS) a Alto (GLSL WebGL / FBM Shaders / SVG Morphing)"
stack_frameworks: ["React 19 / 18", "Next.js 15 (App Router)", "Tailwind CSS v4 & v3", "Motion (motion/react)", "TypeScript", "shadcn CLI Registry", "Model Context Protocol (MCP)"]
compatibilidade:
  fontes_ideais: ["Open Runde (SF Pro Rounded alternative)", "Geist Sans", "Inter", "Geist Mono", "Cal Sans"]
  paletas_ideais: ["Apple Light Studio (Fundo #F5F5F7, Cards #FFFFFF, Linhas rgba(0,0,0,0.04))", "Deep Pitch Dark Mode (Fundo #121212 / #1C1C1E, Bordas #262626, Acento #FC4C01)", "Electric Blaze Accent (#FC4C01 / #e64500)", "iOS Status Accents (Emerald Green #34C759, Crimson Red #FF3B30, Sky Blue #50B1FD)"]
  combinacoes_recomendadas: ["shadcn/ui (fundação primária de formulários e layout)", "Radix UI Primitives", "Kokonut UI (para micro-interações táteis complementares)", "Cult UI / Magic UI (para grids de bento e efeitos de fundo)", "Vaul (para gavetas elásticas estilo iOS)"]
  conflitos_esteticos: ["Brutalismo cru sem suavização de curvas de aceleração", "Neumorfismo plástico com relevos opacos e sombras embaçadas", "Material Design 2 com elevações pesadas em camadas rígidas", "Corporate Memphis genérico em tons pastéis desbotados"]
---

# Rare UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Rare UI**, concebido e mantido pelo engenheiro e designer **Swami Malode** (`@swamimalode`), estabeleceu uma posição de prestígio no cenário contemporâneo de design systems e bibliotecas de interface para React e Next.js. Enquanto o ecossistema foi inundado por coleções repetitivas de botões com borda iluminada (*shimmer border*) e gradientes genéricos, o Rare UI propõe um manifesto deliberado: *"Tasteful Components, Made to Stand Out"*. Trata-se de uma curadoria de interações raras, artesanais e cineticamente sofisticadas que desenvolvedores frequentemente evitam construir por demandarem matemática vetorial complexa, shaders GLSL ou física de deformação elástica.

A assinatura visual do Rare UI apoia-se em cinco pilares conceituais e tecnológicos:

### 1. Filosofia "Apple Craft": Squircles, Tipografia Rounded e Háptica Visual
O acabamento do Rare UI respira a precisão industrial de Cupertino. Ao contrário do padrão convencional de bordas arredondadas com raio fixo (`border-radius: 16px`), o Rare UI emprega **squircles matemáticos** com suavização contínua de curvatura (*curvature continuity* G2), implementados nativamente via `corner-shape: squircle` e a biblioteca `figma-squircle`. O sistema tipográfico padrão adota a família **Open Runde** (ou variantes arredondadas do SF Pro), transmitindo uma sensação convidativa, moderna e tátil, ancorada pelo tom de destaque **Blaze Orange** (`#FC4C01`) sobre fundos neutros em cinza estúdio (`#F5F5F7` no tema claro e `#121212` no tema escuro).

### 2. Micro-Interações Complexas e Recreações de Alta Dificuldade
O Rare UI foca deliberadamente em componentes incomuns no catálogo do mercado:
- O **Folder Component** simula pastas físicas tridimensionais em perspectiva isométrica cujo flap inclinado se abre ao clique e cujas cartas internas se espalham em leque (*fan out*) sob hover.
- O **Duration Picker** utiliza o motor `flubber` para realizar morphing contínuo de caminhos SVG, transformando a ponta de uma caneta em um ícone de confirmação (*check*) através de interpolação não linear.
- O **Delete Button** elimina modais intrusivos através de um mecanismo de confirmação *in-place*: ao clique, a tampa da lixeira levanta em ângulo de `-35°` e o botão expande suavemente sua largura com curvas de amortecimento mecânico.
- O **Rail TOC** conduz um pequeno avião de papel em vetor SVG que voa, freia e gira com inércia física ao longo do trilho lateral conforme a página é rolada.

### 3. Computação Gráfica Pura: WebGL Shaders e Física em Canvas sem Bloatware
Em vez de depender de pacotes volumosos como Three.js ou Matter.js (que frequentemente adicionam centenas de kilobytes ao bundle inicial), o Rare UI constrói seus showstoppers visuais sobre APIs nativas da Web:
- O **Fluid Orb** executa um fragment shader GLSL raw com *Fractional Brownian Motion* (FBM) e interpolação de ruído procedural diretamente sobre um contexto `WebGLRenderingContext`, replicando em tempo real o brilho bioluminescente do modo de voz avançado do ChatGPT.
- O **Gravity Letters** implementa um motor de física estocástica proprietário com heightmaps discretizados (`COL = 8px`), atrito de encosta (`SLOPE = 0.35`), restituição elástica e suporte a sensores de giroscópio de dispositivos móveis via `DeviceOrientationEvent`.

### 4. Vocabulário Nativo para Interfaces de Inteligência Artificial (AI Kit)
O Rare UI é pioneiro em empacotar componentes específicos para copilotos modernos:
- O **Web Search Component** orquestra em tempo real a experiência de busca com citações vivas, anel de progresso estocástico (*creeping progress ring*) e cartões colapsáveis de fontes bibliográficas no padrão Perplexity e SearchGPT.
- O **Grid Reveal** simula a revelação progressiva em grade fracionada de imagens geradas por modelos de difusão (Midjourney / Flux / DALL-E), substituindo skeletons estáticos por uma animação de células em colapso.
- O **Matrix Orb** responde dinamicamente a três estados cognitivos (`idle`, `listening`, `thinking`) modulados por transições de escala e amplitude senoidal.

### 5. Distribuição Sem Dependências Fechadas via Shadcn Registry & MCP
O Rare UI rejeita o modelo de biblioteca NPM fechada. Cada componente é distribuído como um único arquivo TypeScript puro (`components/ui/<component>.tsx`). O desenvolvedor adquire a posse integral do código-fonte através do CLI universal do shadcn (`npx shadcn@latest add swamimalode07/rare-ui/<component>`) ou acoplado diretamente a agentes de inteligência artificial (Claude Code, Cursor, VS Code, Codex) através do **Model Context Protocol (MCP)** configurado no `components.json`.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados
1. **Aplicações de Inteligência Artificial, Agentes Autônomos & Assistentes de Voz**:
   Produtos que necessitam comunicar estados cognitivos complexos (pesquisa em tempo real, geração de imagem, síntese de voz, raciocínio em múltiplos passos). O catálogo do Rare UI fornece componentes emblemáticos como `fluid-orb`, `matrix-orb`, `web-search`, `aistatus` e `grid-reveal`.
2. **SaaS B2B de Alta Categoria ("High-Craft" Software)**:
   Ferramentas nas quais a estética e o refinamento sensorial operam como diferencial competitivo (estilo Linear, Raycast, Cron, Family, Supabase). Recursos como `hook-sidebar`, `bouncesidebar`, `duration-picker` e `code-block` transmitem um nível de polimento artesanal superior.
3. **Plataformas de Conteúdo Técnico, Docs & Manuais de Engenharia**:
   Documentações sofisticadas que exigem navegação lateral de alta precisão. O `railtoc` e o `scrollprogressindicator` transformam a leitura de artigos extensos em uma experiência envolvente.
4. **Portfólios Criativos, Labs de Design e Startups em Estágio de Lançamento**:
   Aplicações que demandam momentos de encantamento visual imediato para investidores e early adopters. O `folder-component` e o `gravity-letters` tornam heróis e seções de projetos inesquecíveis.

### Papel no Ritmo Visual (A Regra 60-30-10)

Para preservar o equilíbrio visual e evitar sobrecarga cognitiva, a orquestração do Rare UI deve obedecer à seguinte proporção:

```
┌─────────────────────────────────────────────────────────────┐
│ 60% — Fundação Estrutural Neutra                           │
│ (shadcn/ui limpo, superfícies #F5F5F7 / #121212, tipografia)│
├─────────────────────────────────────────────────────────────┤
│ 30% — Camada de Navegação & Micro-interações Fluidas        │
│ (Hook Sidebar, Scroll Progress, FAQ Message Thread, Codes)  │
├─────────────────────────────────────────────────────────────┤
│ 10% — Efeitos Protagonistas / Showstoppers Raros            │
│ (Fluid Orb no Hero, Folder Component no Bento, Grid Reveal) │
└─────────────────────────────────────────────────────────────┘
```

- **60% — Fundação Neutra e Estrutural (Base `shadcn/ui` + Open Runde / Geist)**:
  Superfícies limpas com fundos monocromáticos (`#F5F5F7` no light mode, `#121212` no dark mode), bordas sutis com baixa opacidade (`border-black/[0.04]` ou `border-white/[0.08]`) e hierarquia tipográfica consistente sem enfeites desnecessários.
- **30% — Camada de Fluidez e Navegação Tátil (Micro-interações Rare UI)**:
  Navegação de fluxo contínuo: a barra lateral `hook-sidebar` com trilho pontilhado dinâmico, o `scrollprogressindicator` que se expande ao clique em um menu squircle, o `delete-button` com confirmação sem diálogo modal e o `code-block` com troca de tema dinâmico e cópia háptica.
- **10% — Momentos Culminantes & Showstoppers Raros (Máximo de 1 a 2 por tela)**:
  Pontos de ancoragem emocional: o `fluid-orb` operando como orquestrador do modo de voz na interface principal, o `folder-component` destacando os arquivos de projetos dentro de um Bento Grid, ou o `gravity-letters` como elemento interativo em uma seção de boas-vindas.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Painéis Financeiros de Alta Densidade e Telas de Trading (ex: Bloomberg Terminal, Dashboards de Ações)**:
  Em interfaces onde o usuário precisa monitorar dezenas de tabelas de dados numéricos por segundo, elementos lúdicos como o avião do `railtoc` ou letras caindo com física vetorial geram poluição sensorial e distraem de decisões de alto valor monetário.
- **Formulários de Entrada Rápida de Dados em Massa (ERP / Emissão Fiscal)**:
  Operadores que navegam exclusivamente via teclado (`Tab` + `Enter`) em alta cadência são prejudicados por botões expansíveis como o `delete-button` ou seletores de duração que exigem cliques arrastados.
- **Dispositivos Móveis de Baixa Potência com Restrição de Bateria**:
  Embora o `fluid-orb` seja construído em WebGL puro sem bibliotecas pesadas, laços contínuos de fragment shaders executados em resolução nativa (`devicePixelRatio > 2`) consomem ciclos de GPU. Deve-se suspender o loop de animação quando o elemento sair da viewport via `IntersectionObserver`.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões):
1. **O Efeito "Parque de Diversões": Múltiplos Elementos Raros na Mesma Viewport**:
   Nunca posicione o `folder-component`, o `fluid-orb` e o `gravity-letters` simultaneamente no mesmo campo de visão. O Rare UI ganha força pelo contraste: quando tudo salta, gira e morphing ocorre em todo canto, a interface perde sua sofisticação e parece uma colcha de retalhos experimental.
2. **Ignorar `prefers-reduced-motion`**:
   Todos os componentes do Rare UI utilizam `useReducedMotion()`. É terminantemente proibido desativar essa proteção; usuários com sensibilidade vestibular devem receber transições diretas de opacidade em vez de física de ricochete elástico ou morphing de SVG.
3. **Uso Excessivo da Cor Laranja Blaze (`#FC4C01`)**:
   A cor `#FC4C01` é uma tonalidade saturada de alta voltagem visual. Utilize-a com parcimônia cirúrgica (em badges de novo release, estados ativos de foco e ponteiros de interação). Se aplicada em cartões inteiros ou botões secundários, ela anula o contraste e desequilibra a hierarquia.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão detalhados os **12 componentes mais avançados e emblemáticos** do repositório Rare UI:

---

### 1. Folder Component (`folder-component`)
- **Anatomia Visual**: Reconstituição digital hiper-realista de uma pasta física de documentos em perspectiva com iluminação em camadas. Possui três partes estruturais: a base traseira com chanfro de arquivo, um conjunto de 3 cartões internos com linhas e detalhes simulados, e a aba frontal (*flap*) semitransparente (`flapFillOpacity: 0.25`) com efeito de vidro fosco e stroke luminoso (`flapStroke: #979797`).
- **Gatilho de Interação**: No estado de repouso, as cartas descansam protegidas. Ao passar o mouse (*hover*), as 3 cartas internas sobem e se abrem em leque angular. Ao clicar (*click*), a aba frontal inclina-se em 3D e a pasta se abre totalmente, permitindo a seleção individual dos itens.
- **Onde Encaixar**: Bento grids de landing pages (para categorizar módulos ou templates), exploradores de arquivos em aplicações criativas e cards de demonstração de repositórios.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add swamimalode07/rare-ui/folder-component
  ```

---

### 2. Fluid Orb (`fluid-orb`)
- **Anatomia Visual**: Esfera viva em computação gráfica inspirada no modo de voz do ChatGPT. Utiliza um shader de fragmento GLSL executado sobre contexto WebGL nativo. O shader combina 3 oitavas de ruído fractal (*Fractional Brownian Motion* - FBM) com distorções de coordenadas baseadas no tempo para simular a convecção de um fluido brilhante em rotação permanente.
- **Gatilho de Interação**: Animação contínua e autônoma alimentada por `requestAnimationFrame`. Suporta propriedades dinâmicas de tamanho (`size`) e coloração espectral (`color`) em formato hexadecimal que são convertidos em vetores `vec3` normalizados `[0..1]` para o shader.
- **Onde Encaixar**: Centro do Hero em produtos de IA, modal de assistente de voz conversacional, tela de carregamento de processamento cognitivo ou avatar de agente inteligente.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add swamimalode07/rare-ui/fluid-orb
  ```

---

### 3. Gravity Letters (`gravity-letters`)
- **Anatomia Visual**: Campo de física vetorial bidimensional onde caracteres alfanuméricos, palavras completas, emojis ou nós React personalizados caem do topo da viewport e se empilham uns sobre os outros de forma orgânica, respeitando superfícies e declives.
- **Gatilho de Interação**:
  - *Click / Tap*: Faz cair uma nova leva de letras com rotação aleatória.
  - *Hold*: Dispara um fluxo ininterrupto de caracteres (*pour mode* a cada 120ms).
  - *Device Tilt*: Em smartphones com acelerômetro habilitado, inclinar o aparelho faz as letras empilhadas deslizarem e rolarem para os lados em tempo real via `DeviceOrientationEvent`.
- **Onde Encaixar**: Seção Hero de estúdios criativos, páginas de erro 404 interativas, tela de comemoração de onboarding concluído ou rodapés de sites de tipografia.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add swamimalode07/rare-ui/gravity-letters
  ```

---

### 4. Duration Picker (`duration-picker`)
- **Anatomia Visual**: Seletor tátil de horas e minutos encapsulado em um squircle elegante. Integra dois mostradores giratórios com amortecimento elástico e um botão de ação com ícone vetorial duplo.
- **Gatilho de Interação**: Utiliza a biblioteca `flubber` acoplada ao `motion/react` para interpolar suavemente o vetor da caneta de edição (`PEN_PATH`) para a marca de confirmação (*check* `TICK_PATH`) quando o valor é definido. A transição de forma é contínua e sem saltos visuais.
- **Onde Encaixar**: Formulários de agendamento de eventos, cronômetros de produtividade (estilo Pomodoro), configurações de timeout de tarefas em SaaS e editores de vídeo.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add swamimalode07/rare-ui/duration-picker
  ```

---

### 5. Web Search Component (`web-search`)
- **Anatomia Visual**: Módulo avançado de transparência de raciocínio de IA inspirado no Perplexity. Apresenta uma pílula central com indicador de busca em pulsação contínua, uma linha de cartões de fontes indexadas (`WebSource`) com favicons automáticos, e uma área de texto com streaming progressivo e marcações numéricas de citação vinculadas aos cartões.
- **Gatilho de Interação**: Alternância de status entre `searching` e `done`. Enquanto busca, um anel de progresso estocástico não-linear preenche-se rapidamente e desacelera suavemente (`STEP = 0.3`, `START = 0.08`). Ao concluir, as fontes expandem em um layout organizado com prévias de snippets.
- **Onde Encaixar**: Respostas em copilotos de IA, interfaces de busca generativa corporativa, dashboards de inteligência jurídica ou financeira.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add swamimalode07/rare-ui/web-search
  ```

---

### 6. Rail TOC (`railtoc`)
- **Anatomia Visual**: Sumário lateral (*Table of Contents*) fixo em trilho vetorial minimalista. Ao lado dos títulos das seções, corre uma linha guia pontilhada com um pequeno avião de papel em SVG (`M12 2 20.5 21 12 17.5 3.5 21z`).
- **Gatilho de Interação**: Baseado na rolagem da página (*Scroll*). Conforme o usuário passa pelos cabeçalhos `h2`/`h3`, o avião voa até a posição correspondente usando molas físicas afinadas (`TRAVEL_SPRING = { stiffness: 140, damping: 26, mass: 0.6 }`) e inclina o bico em direção ao movimento (`TURN_SPRING = { stiffness: 260, damping: 30 }`), com tolerância contra trepidação (*slack*).
- **Onde Encaixar**: Artigos de blog de engenharia, documentações de produtos técnicos, whitepapers e changelogs detalhados.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add swamimalode07/rare-ui/rail-toc
  ```

---

### 7. In-Place Delete Button (`delete-button`)
- **Anatomia Visual**: Botão de exclusão de alto impacto que elimina a necessidade de modais ou caixas de diálogo adicionais. Consiste em uma caixa compacta de 48px com o ícone de uma lixeira mecânica.
- **Gatilho de Interação**: Ao primeiro clique, o botão se expande horizontalmente de 48px para 84px usando uma curva cúbica ultra-suave (`ease: [0.32, 0.72, 0, 1]`), enquanto a tampa da lixeira levanta em ângulo de `-35°` (`ease: [0.34, 1.1, 0.64, 1]`), revelando os botões integrados "Delete" e "Cancel". Se não houver confirmação em 1400ms, o botão retorna automaticamente ao estado seguro.
- **Onde Encaixar**: Tabelas de gerenciamento de dados, configurações de exclusão de conta, remoção de chaves de API e listas de arquivos.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add swamimalode07/rare-ui/delete-button
  ```

---

### 8. Matrix Orb (`matrix-orb`)
- **Anatomia Visual**: Orbe esférico estilizado em matriz de pontos pontilhados (*dot-matrix*) com perspectiva pseudo-3D, inspirado em interfaces de dispositivos de hardware de áudio e inteligência artificial.
- **Gatilho de Interação**: Responde programaticamente a três estados centrais:
  - `idle`: Respiração lenta e pulsação sutil em escala `0.88`.
  - `listening`: Reatividade sonora com ondas de choque que expandem os pontos da matriz em escala `1.0`.
  - `thinking`: Rotação rápida do anel de pontos em escala `0.92` com atenuação via molas físicas (`stiffness: 180, damping: 26`).
- **Onde Encaixar**: Indicador de gravação de áudio em notas de voz, assistentes de transcrição e status de processamento de LLMs.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add swamimalode07/rare-ui/matrix-orb
  ```

---

### 9. Step Player (`step-player`)
- **Anatomia Visual**: Barra de progresso segmentada de estética iOS com botões integrados de reprodução, pausa e repetição. O passo em andamento estica-se proporcionalmente em largura, enquanto os passos inativos permanecem comprimidos como cápsulas redondas.
- **Gatilho de Interação**: Clique no botão play inicia o enchimento linear da barra ativa. O ícone de Play transiciona para Pause através de morphing vetorial contínuo via `flubber` com amortecimento de mola (`WIDTH_SPRING = { duration: 0.42, bounce: 0.14 }`).
- **Onde Encaixar**: Carrosséis guiados de onboarding, reprodutores de stories em web apps, tutoriais passo a passo de produtos e demos interativas.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add swamimalode07/rare-ui/step-player
  ```

---

### 10. Sliding OTP Input (`otp-input`)
- **Anatomia Visual**: Entrada de código de uso único (One-Time Password / 2FA) de acabamento refinado. Cada caractere repousa em uma caixa squircle com tipografia proeminente, sob a qual corre um cursor (*caret*) cinético que desliza horizontalmente de compartimento em compartimento.
- **Gatilho de Interação**: Conforme o usuário digita ou cola um código de 6 dígitos, os caracteres rolam verticalmente para a posição com amortecimento elástico via `AnimatePresence`. Em caso de sucesso, desenha um círculo em SVG verde Apple (`#34C759`); em caso de erro, a linha inteira vibra com um tremor elástico e contorno vermelho (`#FF3B30`).
- **Onde Encaixar**: Telas de login de autenticação de dois fatores, fluxos de verificação de telefone/e-mail e transações bancárias.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add swamimalode07/rare-ui/otp-input
  ```

---

### 11. Hook Sidebar (`hook-sidebar`)
- **Anatomia Visual**: Barra de navegação vertical de precisão industrial. É composta por uma lista de links de texto alinhados a um trilho esquerdo contendo uma linha tracejada (`repeating-linear-gradient`). Um gancho vetorial em SVG (`M0.5 0a6 6 0 0 0 6 6H12`) conecta a linha tracejada diretamente ao item em foco.
- **Gatilho de Interação**: Ao navegar entre abas ou ao passar o mouse sobre itens diferentes, o gancho viaja verticalmente pelo trilho e engata de forma fluida no novo item com coloração Blaze Orange (`#FC4C01`).
- **Onde Encaixar**: Painéis laterais de documentação, menus de navegação em dashboards densos e barras de configurações de conta.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add swamimalode07/rare-ui/hook-sidebar
  ```

---

### 12. Scroll Progress Squircle (`scroll-progress`)
- **Anatomia Visual**: Pílula flutuante compacta ancorada na base da viewport que exibe a porcentagem exata de leitura do documento e o título da seção atual.
- **Gatilho de Interação**:
  - *Scroll contínuo*: Preenche suavemente o indicador de progresso através do hook `useScroll` do Framer Motion.
  - *Click*: A pílula expande-se elasticamente (`SIZE_SPRING = { bounce: 0.16, duration: 0.5 }`) em um menu squircle completo com a lista de todos os tópicos da página, permitindo saltos instantâneos com scroll suave.
- **Onde Encaixar**: Blogs de artigos longos (*long-form reading*), relatórios anuais de sustentabilidade ou financeiros e páginas de termos de serviço.
- **Instalação CLI**:
  ```bash
  npx shadcn@latest add swamimalode07/rare-ui/scroll-progress
  ```

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup de Pacotes

Para consumir qualquer componente do Rare UI em um projeto React 19 ou Next.js 15 (App Router), instale as dependências fundamentais:

```bash
# 1. Dependências do núcleo de movimento e utilitários
npm install motion clsx tailwind-merge

# 2. Pacotes auxiliares para componentes com morphing e geometria Apple
npm install flubber figma-squircle react-use-measure @radix-ui/react-slot lucide-react

# 3. Tipagens para TypeScript
npm install -D @types/flubber
```

### Configuração do Model Context Protocol (MCP) para Editores de IA

Para habilitar agentes de IA (Claude Code, Cursor, VS Code, OpenAI Codex) a instalarem componentes do Rare UI automaticamente com linguagem natural, adicione o registro ao arquivo `components.json`:

```json
{
  "$schema": "https://ui.shadcn.com/schema.json",
  "style": "default",
  "rsc": true,
  "tsx": true,
  "tailwind": {
    "config": "tailwind.config.ts",
    "css": "app/globals.css",
    "baseColor": "neutral",
    "cssVariables": true
  },
  "aliases": {
    "components": "@/components",
    "utils": "@/lib/utils"
  },
  "registries": {
    "@rare-ui": "https://raw.githubusercontent.com/swamimalode07/rare-ui/main/public/r/{name}.json"
  }
}
```

Após configurar, no **Claude Code** inicialize a conexão via:
```bash
npx shadcn@latest mcp init --client claude
```
A partir desse momento, qualquer comando conversacional como *"Adicione o Fluid Orb do Rare UI no meu projeto"* irá baixar o código diretamente para `@/components/ui/fluid-orb.tsx`.

---

### Física de Movimento: Tabela de Calibração Cinética do Rare UI

O Rare UI estabeleceu um conjunto muito particular de curvas de mola (*spring*) e curvas de Bezier cúbico que diferenciam seu toque visual de transições lineares amadoras:

| Mecanismo / Tipo | Parâmetros de Mola / Curva Bezier | Sensação Visual & Justificativa Mecânica |
| :--- | :--- | :--- |
| **Apple Fluid Transition** | `cubic-bezier(0.32, 0.72, 0, 1)` | Curva canônica da Apple para transições de layout, botões expansíveis e fading de ícones. Rápida no arranque e com parada suave. |
| **Mechanical Lid Overthrow** | `cubic-bezier(0.34, 1.1, 0.64, 1)` | Curva de tampa mecânica (usada no `delete-button`). Apresenta um leve overshoot elástico no topo que simula uma dobradiça física. |
| **TOC Paper Plane Travel** | `stiffness: 140, damping: 26, mass: 0.6` | Mola com massa leve para viagens longas do avião de papel ao longo do trilho, desacelerando com elegância sem tremer. |
| **TOC Plane Angle Turn** | `stiffness: 260, damping: 30` | Mola rígida e sem overshoot para rotação instantânea da proa do avião na direção do scroll. |
| **Matrix Orb Audio Spring** | `stiffness: 180, damping: 26` | Amortecimento tátil de áudio que absorve variações repentinas de decibéis sem estourar o limite gráfico. |
| **In-Place Confirmation Hold** | `HOLD: 1400ms (delete) / 600ms (cancel)` | Janela temporal exata para tomada de decisão sem diálogo intrusivo. |

---

### Receita de Código Funcional 1: O Shader WebGL do `FluidOrb`

Abaixo está a implementação completa e funcional do componente carro-chefe **FluidOrb**, renderizado inteiramente em um elemento `<canvas>` WebGL sem Three.js:

```tsx
"use client";

import React, { useEffect, useRef } from "react";
import { cn } from "@/lib/utils";

export type FluidOrbProps = React.ComponentProps<"div"> & {
  size?: number;
  color?: string; // Formato hex: "#FC4C01" ou "#50B1FD"
};

const VERTEX_SHADER_SOURCE = `
  attribute vec2 a_position;
  void main() {
    gl_Position = vec4(a_position, 0.0, 1.0);
  }
`;

const FRAGMENT_SHADER_SOURCE = `
  #ifdef GL_FRAGMENT_PRECISION_HIGH
  precision highp float;
  #else
  precision mediump float;
  #endif

  uniform vec2 u_resolution;
  uniform float u_time;
  uniform vec3 u_color;

  float hash(vec2 p) {
    return fract(sin(dot(p, vec2(127.1, 311.7))) * 43758.5453123);
  }

  float noise(vec2 p) {
    vec2 i = floor(p);
    vec2 f = fract(p);
    vec2 u = f * f * (3.0 - 2.0 * f);
    return mix(
      mix(hash(i + vec2(0.0, 0.0)), hash(i + vec2(1.0, 0.0)), u.x),
      mix(hash(i + vec2(0.0, 1.0)), hash(i + vec2(1.0, 1.0)), u.x),
      u.y
    );
  }

  float fbm(vec2 p) {
    float total = 0.0;
    float amp = 0.6;
    for (int i = 0; i < 3; i++) {
      total += amp * noise(p);
      p *= 2.0;
      amp *= 0.5;
    }
    return total;
  }

  void main() {
    vec2 uv = (gl_FragCoord.xy - 0.5 * u_resolution.xy) / min(u_resolution.x, u_resolution.y);
    float dist = length(uv);

    // Borda esférica suave com máscara circular
    float circle = smoothstep(0.48, 0.40, dist);
    if (circle <= 0.0) {
      discard;
    }

    // Distorção de coordenadas via Fractional Brownian Motion (FBM)
    vec2 movement = vec2(u_time * 0.15, u_time * 0.08);
    float fluidNoise = fbm(uv * 3.5 + movement + fbm(uv * 4.0 - movement * 0.5));

    // Iluminação do núcleo bioluminescente
    float core = smoothstep(0.45, 0.05, dist);
    vec3 highlight = vec3(1.0, 1.0, 1.0) * pow(fluidNoise, 2.5) * core;
    vec3 baseColor = u_color * (fluidNoise * 1.4 + 0.3) * core;

    gl_FragColor = vec4(baseColor + highlight, circle * core);
  }
`;

function hexToRgb(hex: string): [number, number, number] {
  const sanitized = hex.replace("#", "");
  const num = parseInt(sanitized, 16);
  return [
    ((num >> 16) & 255) / 255,
    ((num >> 8) & 255) / 255,
    (num & 255) / 255,
  ];
}

export function FluidOrb({
  size = 320,
  color = "#FC4C01",
  className,
  ...props
}: FluidOrbProps) {
  const canvasRef = useRef<HTMLCanvasElement | null>(null);

  useEffect(() => {
    const canvas = canvasRef.current;
    if (!canvas) return;

    const gl = canvas.getContext("webgl", { alpha: true, antialias: true });
    if (!gl) return;

    // Compilação de Shaders
    function createShader(glCtx: WebGLRenderingContext, type: number, src: string) {
      const shader = glCtx.createShader(type);
      if (!shader) return null;
      glCtx.shaderSource(shader, src);
      glCtx.compileShader(shader);
      return shader;
    }

    const vertShader = createShader(gl, gl.VERTEX_SHADER, VERTEX_SHADER_SOURCE);
    const fragShader = createShader(gl, gl.FRAGMENT_SHADER, FRAGMENT_SHADER_SOURCE);
    if (!vertShader || !fragShader) return;

    const program = gl.createProgram();
    if (!program) return;
    gl.attachShader(program, vertShader);
    gl.attachShader(program, fragShader);
    gl.linkProgram(program);
    gl.useProgram(program);

    // Buffer de Geometria (Quad plano cobrindo a tela)
    const positionBuffer = gl.createBuffer();
    gl.bindBuffer(gl.ARRAY_BUFFER, positionBuffer);
    gl.bufferData(
      gl.ARRAY_BUFFER,
      new Float32Array([-1, -1, 1, -1, -1, 1, -1, 1, 1, -1, 1, 1]),
      gl.STATIC_DRAW
    );

    const aPos = gl.getAttribLocation(program, "a_position");
    gl.enableVertexAttribArray(aPos);
    gl.vertexAttribPointer(aPos, 2, gl.FLOAT, false, 0, 0);

    const uResolution = gl.getUniformLocation(program, "u_resolution");
    const uTime = gl.getUniformLocation(program, "u_time");
    const uColor = gl.getUniformLocation(program, "u_color");

    let animationId: number;
    let startTime = performance.now();

    function render() {
      if (!gl || !canvas) return;
      const dpr = Math.min(window.devicePixelRatio || 1, 2);
      const width = canvas.clientWidth * dpr;
      const height = canvas.clientHeight * dpr;

      if (canvas.width !== width || canvas.height !== height) {
        canvas.width = width;
        canvas.height = height;
        gl.viewport(0, 0, width, height);
      }

      const elapsed = (performance.now() - startTime) * 0.001;
      const [r, g, b] = hexToRgb(color);

      gl.uniform2f(uResolution, width, height);
      gl.uniform1f(uTime, elapsed);
      gl.uniform3f(uColor, r, g, b);

      gl.clearColor(0, 0, 0, 0);
      gl.clear(gl.COLOR_BUFFER_BIT);
      gl.drawArrays(gl.TRIANGLES, 0, 6);

      animationId = requestAnimationFrame(render);
    }

    render();

    return () => {
      cancelAnimationFrame(animationId);
      gl.deleteProgram(program);
      gl.deleteShader(vertShader);
      gl.deleteShader(fragShader);
      gl.deleteBuffer(positionBuffer);
    };
  }, [color]);

  return (
    <div
      className={cn("relative flex items-center justify-center overflow-hidden", className)}
      style={{ width: size, height: size }}
      {...props}
    >
      <canvas
        ref={canvasRef}
        className="w-full h-full pointer-events-none drop-shadow-[0_0_45px_rgba(252,76,1,0.35)]"
      />
    </div>
  );
}
```

---

### Receita de Código Funcional 2: O `DeleteButton` com Tampa Mecânica e Confirmação In-Place

```tsx
"use client";

import React, { useState, useEffect } from "react";
import { motion, AnimatePresence } from "motion/react";
import { Trash2, X, Check } from "lucide-react";
import { cn } from "@/lib/utils";

interface DeleteButtonProps {
  onConfirm: () => void;
  className?: string;
  label?: string;
}

const APPLE_EASE = [0.32, 0.72, 0, 1] as const;
const LID_EASE = [0.34, 1.1, 0.64, 1] as const;

export function DeleteButton({
  onConfirm,
  className,
  label = "Delete file",
}: DeleteButtonProps) {
  const [isOpen, setIsOpen] = useState(false);

  useEffect(() => {
    if (!isOpen) return;
    const timer = setTimeout(() => setIsOpen(false), 3000);
    return () => clearTimeout(timer);
  }, [isOpen]);

  const handleConfirm = (e: React.MouseEvent) => {
    e.stopPropagation();
    onConfirm();
    setIsOpen(false);
  };

  return (
    <motion.div
      layout
      transition={{ duration: 0.42, ease: APPLE_EASE }}
      className={cn(
        "relative flex items-center overflow-hidden rounded-2xl bg-neutral-100 p-1 dark:bg-neutral-900 border border-black/[0.06] dark:border-white/[0.08]",
        className
      )}
    >
      {!isOpen ? (
        <button
          type="button"
          onClick={() => setIsOpen(true)}
          className="group flex h-10 items-center gap-2 px-3 text-xs font-semibold text-neutral-700 transition-colors hover:text-red-500 dark:text-neutral-300 dark:hover:text-red-400"
        >
          {/* Ícone da Tampa com Rotação Elástica */}
          <div className="relative size-4">
            <motion.div
              animate={{ rotate: 0 }}
              className="origin-bottom-left"
            >
              <Trash2 className="size-4 text-inherit" />
            </motion.div>
          </div>
          <span>{label}</span>
        </button>
      ) : (
        <motion.div
          initial={{ opacity: 0, scale: 0.95 }}
          animate={{ opacity: 1, scale: 1 }}
          exit={{ opacity: 0, scale: 0.95 }}
          transition={{ duration: 0.25, ease: APPLE_EASE }}
          className="flex h-10 items-center gap-1.5 px-1"
        >
          <span className="pl-2 pr-1 text-xs font-medium text-neutral-500 dark:text-neutral-400">
            Sure?
          </span>

          {/* Botão de Cancelar */}
          <button
            type="button"
            onClick={() => setIsOpen(false)}
            aria-label="Cancel delete"
            className="flex size-8 items-center justify-center rounded-xl bg-neutral-200/70 text-neutral-700 hover:bg-neutral-300 dark:bg-neutral-800 dark:text-neutral-300 dark:hover:bg-neutral-700"
          >
            <X className="size-3.5" />
          </button>

          {/* Botão de Confirmar com Destaque Vermelho Apple */}
          <button
            type="button"
            onClick={handleConfirm}
            aria-label="Confirm delete"
            className="flex size-8 items-center justify-center rounded-xl bg-red-600 text-white shadow-sm hover:bg-red-500"
          >
            <Check className="size-3.5" />
          </button>
        </motion.div>
      )}
    </motion.div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao arquitetar uma nova aplicação e selecionar o **Rare UI** como biblioteca de micro-interações e showstoppers cinematográficos no documento `DESIGN_BLUEPRINT.md`, adote estritamente as instruções abaixo:

### Declaração de Stack & Registry
```markdown
### Design System & Kinetic Primitives: Rare UI
- **Filosofia Visual**: Apple-grade tactile craft, squircle geometry e kinetic micro-interactions.
- **Registro Shadcn**: `https://raw.githubusercontent.com/swamimalode07/rare-ui/main/public/r/{name}.json`
- **Protocolo de Agentes**: MCP habilitado via `npx shadcn@latest mcp init --client claude`
- **Pacotes Essenciais**: `motion/react`, `flubber`, `figma-squircle`, `react-use-measure`, `lucide-react`
```

### Regras Mandatórias de Implementação
1. **Atribuição Correta dos Showstoppers**:
   - Use o `fluid-orb` exclusivamente na seção Hero ou no modal ativo do agente conversacional.
   - Use o `folder-component` para ilustrar coleções de itens, diretórios de templates ou seções de bento grid.
   - Use o `railtoc` em páginas de documentação técnica para proporcionar um diferencial tátil de navegação.
2. **Harmonia Cromática**:
   - Mantenha superfícies base em `#F5F5F7` (Light) e `#121212` (Dark).
   - Use a cor de acento Blaze Orange (`#FC4C01`) apenas para foco ativo, trilhos de navegação e badges de destaque.
3. **Guardrails de Performance**:
   - Em componentes com WebGL (`fluid-orb`), utilize sempre `IntersectionObserver` para congelar o loop de renderização caso o elemento role para fora da tela visível.
   - Sempre certifique-se de envolver animações de morphing com verificação de `useReducedMotion()`.
