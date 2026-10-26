---
id: "eldora-ui"
name: "Eldora UI"
url: "https://www.eldoraui.site/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["SaaS & DevTools Hero Motion", "Houdini Conic Luminous Accents", "WebGL & Three.js Atmospheric Shaders", "Interactive Micro-App Simulations", "Kinetic Variable Typography"]
densidade_informacao: "Media"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Motion/CSS) a Alto (Three.js UnrealBloom / OGL WebGL)"
stack_frameworks: ["React 19 / 18", "Next.js 15 (App Router) / 14", "Tailwind CSS (v4 & v3.4)", "Motion (motion/react / Framer Motion)", "Three.js & OGL", "Lucide React", "Shadcn CLI / Fumadocs"]
compatibilidade:
  fontes_ideais: ["Geist Sans", "Inter", "Plus Jakarta Sans", "Geist Mono", "JetBrains Mono"]
  paletas_ideais: ["Deep Neutral Zinc (Zinc 950 / Zinc 900 / Zinc 800)", "Cyber Cyan Glow (#06b6d4 / #67e8f9 em fundo escuro)", "High-Tech Obsidian Dark com Acentos Esmeralda ou Violeta"]
  combinacoes_recomendadas: ["Shadcn UI", "Magic UI", "Aceternity UI", "Cult UI", "Kokonut UI"]
  conflitos_esteticos: ["Neumorfismo pastel de baixa densidade", "Brutalismo plano sem bordas reflexivas ou suavização", "Material Design 2 com sombras drop duras saturadas"]
---

# Eldora UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

Criado e mantido pelo engenheiro de software e designer indiano **Karthik Mudunuri** (`@karthikmudunuri`), o **Eldora UI** (`eldoraui.site`) consolidou-se rapidamente como uma das mais expressivas coleções abertas de componentes reativos e blocos animados para o ecossistema Next.js, React e Tailwind CSS. Nascido da convergência deliberada entre a arquitetura componível do `shadcn/ui`, a dramaticidade cênica do `Aceternity UI` e a elegância de marketing do `Magic UI`, o Eldora UI encontrou uma voz própria ao posicionar-se como um acelerador de **confiança visual e autoridade técnica para produtos SaaS e DevTools modernos**.

A premissa fundamental do Eldora UI é que interfaces de marketing não devem apenas *descrever* um produto, mas *simular a experiência viva* do software antes mesmo do usuário criar uma conta. Enquanto bibliotecas tradicionais oferecem cartões estáticos e botões com hovers triviais, o Eldora UI desenvolve **micro-ecossistemas táteis de alta fidelidade**.

Sua assinatura estética assenta-se sobre cinco pilares distintivos:

1. **Iluminação Conica via CSS Houdini & Feixes Ópticos Matemáticos**:
   Diferente de abordagens puramente baseadas em `box-shadow` ou bordas estáticas, o Eldora UI explora recursos modernos de CSS nativo como `@property --gradient-angle` e `@property --gradient-shine`, combinados com `conic-gradient` e máscaras de corte (`padding-box` vs `border-box`). Em componentes como o *Animated Shiny Button* e o *Live Button*, o reflexo percorre o perímetro do botão com interpolações temporais não-lineares (`cubic-bezier(0.25, 1, 0.5, 1)`), conferindo um aspecto de acabamento em titânio polido ou cristal reflexivo de nível Apple/Linear.

2. **Cenografia de Fundo de Alta Densidade com WebGL (Three.js & OGL)**:
   A biblioteca não hesita em elevar o teto gráfico do navegador quando o objetivo é impressionar no primeiro impacto (*first fold*). Com implementações como o **Photon Beam** (usando Three.js, `UnrealBloomPass` e `EffectComposer` para feixes ópticos que simulam condução de dados em fibras luminosas) e o **Novatrix Background** (utilizando shaders de fragmento GLSL de ondas de interferência trigonométrica com a biblioteca ultraleve `ogl`), o Eldora UI entrega atmosferas cósmicas e cibernéticas que retêm a atenção visual sem poluir a leitura do texto.

3. **Simulações Interativas de Padrões Reais de Produto (Product Mock Simulators)**:
   A assinatura mais inovadora do Eldora UI reside em seus componentes de "prova funcional":
   - O **Clerk OTP**: simula visualmente a digitação autônoma de um código de verificação de autenticação de dois fatores (MFA), com micro-pulsos de anel e transições numéricas em tempo real.
   - O **GitHub Inline Comments**: replica integralmente a experiência de visualização de diff de código do GitHub, permitindo criar fios de discussão, alternar status de resolução de tarefas (*Resolve/Unresolve*) e adicionar comentários em linhas específicas diretamente na landing page.
   - O **Animated Frameworks**: cartões isométricos com perspectiva tridimensional (`[perspective:1000px]`) que rotacionam em loop sutil para evidenciar interoperabilidade entre plataformas.

4. **Tipografia Cinética com Fontes Variáveis (Kinetic Variable Typography)**:
   Em vez de limitar animações de texto a opacidades e deslocamentos triviais, o Eldora UI manipula diretamente eixos de fontes variáveis através do componente **Font Weight Text** (alterando programaticamente o eixo `"wght"` via CSS animation de 0 a 840 em cadência harmônica radial) e o **Dock Text**, que aplica a lendária física de magnificação do Dock do macOS a cabeçalhos tipográficos, reagindo à proximidade do cursor com curvas de mola amortecidas.

5. **Pioneirismo em Integração Nativa com IA via Servidor MCP (Model Context Protocol)**:
   O Eldora UI foi uma das primeiras coleções da comunidade a disponibilizar um servidor oficial de MCP (`@karthikmudunuri/cli`), permitindo que IDEs assistidas por inteligência artificial (Cursor, Windsurf, Claude Code, Cline, Roo-Cline) leiam em tempo real o catálogo de componentes, seus tipos TypeScript, parâmetros de animação e dependências de registro para geração autônoma de telas sem quebras de sintaxe.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Prioritários

1. **SaaS para Desenvolvedores (DevTools), CI/CD e Infraestrutura de Nuvem**:
   Produtos que vendem pipelines, APIs, compiladores ou ferramentas de colaboração de código encontram no Eldora UI uma linguagem sob medida. O uso conjugado do *GitHub Inline Comments*, do *Terminal interativo* e do *Animated Frameworks* comunica imediatamente que o produto foi concebido por e para engenheiros.
2. **Plataformas de Cibersegurança, Autenticação e IAM**:
   Startups de gestão de acesso, criptografia ou login sem senha (passkeys). O *Clerk OTP* serve como visualização imediata da simplicidade de autenticação, o *Hacker Background* (Matrix rain) contextualiza operações de segurança em segundo plano, e o *Holographic Card* simula crachás ou identidades digitais infalsificáveis.
3. **Plataformas de Inteligência Artificial, LLMs e Agentes Autônomos**:
   Sistemas com processamento massivo de tokens, pipelines RAG e redes neurais. O fundo *Photon Beam* expressa a velocidade e o trânsito de dados em feixes concentrados, enquanto o *Novatrix Background* gera um senso de sofisticação fluida em heroes de produtos de IA generativa.
4. **Landing Pages de Apps Mobile e Aplicativos Nativos**:
   A biblioteca inclui mockups vetoriais ultra-precisos e responsivos de hardware contemporâneo (*iPhone 17 Pro*, *iPad*, *MacBook Pro* e *Safari Browser*), permitindo emoldurar capturas de telas de produtos com sombras de profundidade real sem exigir arquivos pesados de imagem rasterizada.
5. **Portfólios de Engenharia de Design e Tech Lead**:
   O template oficial de portfólio da Eldora UI oferece uma estrutura completa para engenheiros que desejam exibir histórico de projetos, timeline de logos de stacks tecnológicas e changelogs visuais elegantes.

### Papel no Ritmo Visual (Regra 60-30-10)

- **60% — Fundação Estrutural Neutra e Tipografia Limpa**:
  A base da aplicação deve manter sobriedade absoluta com fundos escuros profundos (`bg-neutral-950` ou `bg-zinc-950`), bordas discretas (`border-neutral-800/60`), tipografia corporativa de alta legibilidade (`Geist Sans` ou `Inter`) e leiaute construído com primitivas do `shadcn/ui` (botões neutros, separadores, acordeões de FAQ).
- **30% — Camada de Estruturação Cênica e Prova Funcional do Eldora UI**:
  Blocos de arquitetura visual que organizam a mensagem: o *Animated Frameworks* e o *Bento Grid* organizando os diferenciais técnicos, o *Interactive Map with Avatar Pins* comprovando alcance geográfico e latência global, o *Terminal* com tabs demonstrando comandos de CLI, e a esteira infinita de logos (*Marquee* / *Logo Timeline*).
- **10% — Showstoppers Protagonistas de Alta Energia**:
  O clímax visual da tela reservado para pontos focais estratégicos: o *Photon Beam* ou o shader *Novatrix* atuando como plano de fundo exclusivo do Hero, o *Animated Shiny Button* no Call to Action mais relevante da página ("Start Free Trial" ou "Get API Key"), ou um *Holographic Card* em 3D tilt destacando o plano de assinatura Enterprise no Pricing.
  > [!IMPORTANT]
  > **Regra de Ouro**: Nunca execute dois efeitos gráficos contínuos de alto consumo (como *Photon Beam* e *Novatrix*) simultaneamente na mesma página. Mantenha no máximo um efeito de iluminação WebGL no topo e restrinja as demais seções a micro-interações vetoriais acionadas por hover ou scroll.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:

- **Painéis Operacionais Críticos e Dashboards ERP de Alta Densidade**:
  Telas de preenchimento fiscal, conciliação contábil, prontuários médicos ou dashboards com dezenas de tabelas de métricas. Elementos como *Font Weight Text* pulsando, planos de fundo em movimento perpétuo ou cartões com giro 3D no hover geram fadiga visual imediata e atrasam a produtividade operacional.
- **Aplicações para Dispositivos Móveis de Baixo Custo em Redes Lentas**:
  Efeitos WebGL baseados em Three.js com bloom passivo demandam alto processamento de fragmentos de pixel (*fill rate* da GPU). Em dispositivos móveis de entrada, isso resulta em queda de framerate (inferior a 30 FPS) e drenagem acelerada de bateria caso os loops de `requestAnimationFrame` não sejam pausados.
- **Portais Governamentais e Ambientes de Acessibilidade Estrita (WCAG 2.2 AAA)**:
  Animações que deslocam caracteres ou geram cintilações contínuas sem gatilho explícito de pausa infringem os critérios de sucesso 2.2.2 (*Pause, Stop, Hide*) e 2.3.1 (*Three Flashes or Below Threshold*).

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):

1. **"Sci-Fi Cliché Syndrome"**: Agrupar em um único Hero o *Hacker Background* com chuva verde estilo Matrix, um *Photon Beam* ciano e um *Dock Text* com letras crescendo. A interface deixa de parecer um produto de tecnologia confiável e se torna um clichê de ficção científica dos anos 90 sem credibilidade de mercado.
2. **Abuso de Tipografia Dinâmica no Mesmo Título**: Misturar *FontWeightText*, *WavyText* e *BlurInText* em uma única frase. Títulos de landing page precisam ser absorvidos em frações de segundo; distorcer letras ou atrasar a renderização via múltiplos delays compromete a taxa de conversão.
3. **Ausência de Fallback para `prefers-reduced-motion`**:
   Ignorar a verificação de preferência de movimento reduzido do sistema operacional. Em botões cintilantes, banners de frameworks em rotação e shaders WebGL, é mandatório congelar os loops e exibir um gradiente estático elegante quando o usuário solicitar menos movimento.
4. **Shaders Desgovernados sem IntersectionObserver**:
   Manter o loop de renderização do WebGL ativo mesmo após o usuário ter rolado 2.000 pixels para baixo na página, sobrecarregando a GPU do cliente sem benefício visual algum.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão descritos os 12 componentes mais emblemáticos da biblioteca Eldora UI, selecionados a partir do registro oficial:

### 1. Photon Beam (`@eldoraui/photon-beam`)
- **Anatomia Visual**: Renderizador 3D em Three.js que traça uma malha de até 80 a 100 linhas em curva no espaço, sobre as quais viajam pacotes concentrados de luz (*signals* ou fótons) com cauda luminescente (*trails*). O componente emprega pós-processamento com `EffectComposer` e `UnrealBloomPass` para gerar um brilho estelar orgânico com difusão radial customizável.
- **Gatilho de Interação**: Loop perpétuo de animação em tempo real com controle de velocidade global, amplitude de onda e densidade de linhas; reage à rotação de câmera ou ângulos globais.
- **Onde encaixar na página**: Fundo protagonista da seção Hero de produtos de computação em nuvem, IA generativa, processamento quântico ou redes de alta velocidade.

### 2. Animated Shiny Button (`@eldoraui/animated-shiny-button`)
- **Anatomia Visual**: Botão de alta elegância construído com CSS Houdini (`@property --gradient-angle` e `@property --gradient-shine`). Apresenta um feixe cônico ultrafino que contorna o contorno do botão em loop de 3 segundos, revelando gradientes ciano/turquesa (`#67e8f9` a `#06b6d4`), acompanhado por ícone `ChevronRight` e transição de escala de 800ms.
- **Gatilho de Interação**: Animação contínua de contorno em repouso; no hover, acelera e intensifica a dispersão de luz; reage a clique com micro-afundamento tátil (`active:scale-95`).
- **Onde encaixar na página**: O Call-to-Action (CTA) número 1 da página inteira (Hero principal e seção final de fechamento pré-rodapé).

### 3. Clerk OTP Card (`@eldoraui/clerk-otp`)
- **Anatomia Visual**: Cartão de autenticação multifator (MFA) simulado, estilizado com a estética do Clerk Auth. Exibe 6 slots numéricos individuais com foco ativo, bordas iluminadas e preenchimento procedural de dígitos aleatórios a intervalos controlados (ex: 3.500ms), seguido por animação de fade e reinicialização fluida.
- **Gatilho de Interação**: Execução autônoma em loop com temporizador configurável ou acionamento condicional exclusivo ao passar o mouse (`whileHover={true}`).
- **Onde encaixar na página**: Célula de destaque no Bento Grid na seção de "Segurança Empresarial", "Autenticação Moderna" ou "Conformidade SOC2".

### 4. GitHub Inline Comments (`@eldoraui/github-inline-comments`)
- **Anatomia Visual**: Visualizador de diferenças de código (*diff viewer*) completo e interativo com linhas de adição (verde), deleção (vermelho) e contexto neutro. Inclui botões flutuantes para iniciar threads de revisão em qualquer linha, campo de texto expansível para comentários com Markdown, avatares de colaboradores e botão de status de resolução com ícone de verificação.
- **Gatilho de Interação**: Clique no gutter da linha para abrir a caixa de comentários; clique em "Resolve thread" para recolher e arquivar a discussão; hover nas linhas de código com destaque de sintaxe.
- **Onde encaixar na página**: Seção de "Colaboração em Equipe", "Code Review Automatizado" ou "DevTools / CI/CD Pipeline" de plataformas SaaS de engenharia.

### 5. Novatrix Background Shader (`@eldoraui/novatrix-background`)
- **Anatomia Visual**: Fundo atmosférico em WebGL executado com a biblioteca compacta `ogl`. Utiliza um shader de fragmento GLSL que calcula interferências trigonométricas iterativas (8 iterações de `cos` e `sin` combinados), criando ondulações de seda líquida e gradientes policromáticos profundos com resolução dinâmica.
- **Gatilho de Interação**: Ondulação contínua orientada a tempo (`uTime` e `uSpeed`); suporta distorção elástica opcional orientada pelo ponteiro do mouse (`mouseReact={true}` e `uAmplitude`).
- **Onde encaixar na página**: Hero background de startups de IA, produtos criativos digitais, plataformas de áudio ou agências de tecnologia de ponta.

### 6. Holographic Card (`@eldoraui/holographic-card`)
- **Anatomia Visual**: Cartão interativo com efeito holográfico de cartas colecionáveis de luxo. Combina matriz de micro-pontos de fundo, camadas de tipografia vertical nas margens e uma sobreposição de gradiente iridescente reativo que reflete comprimentos de onda magenta e ciano conforme o ângulo de incidência da luz varia.
- **Gatilho de Interação**: Rastreamento vetorial contínuo do mouse via `useMotionValue` e `useSpring` (física `stiffness: 200, damping: 25`), gerando inclinação tridimensional de `[-12deg, 12deg]` em X e Y, além de translação do foco luminoso.
- **Onde encaixar na página**: Cartão de plano "Enterprise / VIP" na tabela de Pricing, destaque de Founder/Speaker em conferências de tecnologia, ou cartão de produto em destaque.

### 7. Animated Frameworks (`@eldoraui/animated-frameworks`)
- **Anatomia Visual**: Bloco de compatibilidade tecnológica composto por cartões em relevo isométrico suspensos no espaço virtual (`[perspective:1000px]`). Cada cartão ostenta o logotipo em alta resolução de uma ferramenta (React, Next.js, OpenAI, HTML5, Apple) com gradiente suave do fundo e sombra difusa profunda.
- **Gatilho de Interação**: Ciclo autônomo e orquestrado em que cada cartão é elevado sequencialmente através de `translateY(-3.71px) rotateX(10.71deg) translateZ(20px)` durante 1.200ms com pausa harmônica, simulando gravidade zero controlada.
- **Onde encaixar na página**: Bento Grid na seção de "Ecossistema & Integrações", comprovando que o produto se acopla nativamente a qualquer stack tecnológica do cliente.

### 8. Interactive Map with Avatar Drop Pins (`@eldoraui/map`)
- **Anatomia Visual**: Mapa-múndi escurecido com máscara de gradiente linear suave para as bordas inferiores, sobre o qual múltiplos marcadores com agulhas SVG vetorizadas em gota abrigam avatares fotográficos de usuários reais ou nós de servidores.
- **Gatilho de Interação**: Disparado no hover do contêiner (`whileHover="active"`): os marcadores caem do topo com física elástica em cascata (`y: [-20, 0, 4, 0]`, `scale: [0.75, 1]`) com delays calculados para cada localidade geográfica.
- **Onde encaixar na página**: Seção de "Infraestrutura Global", "Baixa Latência Multi-Região" ou "Comunidade Mundial de Usuários" imediatamente antes do Pricing.

### 9. Dock Text Magnifier (`@eldoraui/dock-text`)
- **Anatomia Visual**: Título de alto impacto visual em caixa alta com estilo minimalista elegante. Conforme o cursor navega sobre a frase, os caracteres sofrem expansão vertical suave e dinâmica, inspirada na barra Dock do macOS.
- **Gatilho de Interação**: Rastreamento de proximidade horizontal do mouse em relação ao centro de cada caractere: as letras vizinhas sofrem magnificação proporcional calculada pela fórmula `Math.max(1, 1.3638 - Math.abs(index - hoveredIndex) * 0.1)` com física de mola (`stiffness: 150, damping: 20, mass: 0.5`).
- **Onde encaixar na página**: Título principal de seção de Manifesto de Produto, cabeçalho de Portfólio de Designer ou chamada cênica no início da página.

### 10. Font Weight Variable Breath (`@eldoraui/font-weight-text`)
- **Anatomia Visual**: Texto monumental que aproveita os eixos contínuos de fontes variáveis modernas (como Inter Variable ou Geist Sans). As letras respiram continuamente, variando sua espessura tipográfica de peso ultrafino (`wght: 0`) para negrito pesado (`wght: 840`).
- **Gatilho de Interação**: Animação cíclica contínua via CSS `@keyframes breath` com timing `cubic-bezier(0.37, 0, 0.63, 1)`, com atraso de fase distribuído radialmente a partir do centro da palavra (`mappedIndex = i - numLetters / 2`).
- **Onde encaixar na página**: Frase de slogan conceitual em páginas de lançamento de produto ("Waitlist"), palavras-chave de transição entre seções longas ou página 404 criativa.

### 11. Hacker Background Matrix Rain (`@eldoraui/hacker-background`)
- **Anatomia Visual**: Chuva cibernética de caracteres alfanuméricos e glifos especiais renderizada diretamente em elemento HTML5 Canvas com buffer otimizado. Possui cor configurável (verde esmeralda `#0F0`, azul ciano ou monocromático cinza), rastro de fade progressivo (`rgba(0, 0, 0, 0.05)`) e controle de densidade por tamanho de fonte.
- **Gatilho de Interação**: Loop contínuo com limitador de taxa de quadros (30 FPS constante para preservação de CPU) e redimensionamento automático via listener na janela.
- **Onde encaixar na página**: Seção de "Terminal de Comandos", "Segurança Ofensiva / Penetration Testing" ou plano de fundo do modal de documentação de chaves de API.

### 12. Hardware Mockup Suite (`macbook-pro`, `iphone-17-pro`, `safari-browser`, `ipad`)
- **Anatomia Visual**: Coleção completa de molduras de dispositivos físicos modeladas em SVG vetorial de altíssima precisão. Inclui o notch/Dynamic Island do iPhone 17 Pro, teclado retroiluminado e trackpad do MacBook Pro, botões de janela do Safari com suporte a temas claro/escuro e proporções perfeitas para acomodar vídeos ou iframes de demonstração de produto.
- **Gatilho de Interação**: Apresentação estática ou combinada com scroll reveal e perspective tilt; slots internos responsivos que preservam aspect ratio com `object-cover`.
- **Onde encaixar na página**: Demonstração de interface do produto logo abaixo do cabeçalho do Hero ("See it in action") e nas abas de recursos por dispositivo.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup

O Eldora UI opera sob a arquitetura de **código aberto e cópia direta (copy & paste / CLI registry)** no padrão Shadcn. Não é um monólito NPM empacotado que engessa o projeto, mas sim arquivos TypeScript modulares que passam a viver diretamente dentro do diretório `@/components/eldoraui/` da sua aplicação.

#### Instalação via Shadcn CLI
O Eldora UI disponibiliza compatibilidade nativa com o CLI do Shadcn através de rotas diretas de registro:

```bash
# Adicionar componentes específicos via CLI do Shadcn
npx shadcn@latest add "https://eldoraui.site/r/animated-shiny-button"
npx shadcn@latest add "https://eldoraui.site/r/clerk-otp"
npx shadcn@latest add "https://eldoraui.site/r/github-inline-comments"
npx shadcn@latest add "https://eldoraui.site/r/photon-beam"
npx shadcn@latest add "https://eldoraui.site/r/novatrix-background"
npx shadcn@latest add "https://eldoraui.site/r/holographic-card"
npx shadcn@latest add "https://eldoraui.site/r/dock-text"
npx shadcn@latest add "https://eldoraui.site/r/map"
```

#### Pacotes Base Necessários no `package.json`
Dependendo dos componentes selecionados, os seguintes pacotes devem estar instalados no projeto Next.js / React:

```bash
npm install motion clsx tailwind-merge lucide-react
# Para os componentes cênicos avançados (Photon Beam e Novatrix):
npm install three @types/three ogl
# Para o Cobe Globe e Map:
npm install cobe react-spring
```

---

### Física de Movimento, Parâmetros de Mola & Curvas Bézier

O Eldora UI adota convenções precisas de engenharia de movimento calibradas para transmitir solidez e elegância tátil:

| Componente | Tipo de Animação | Parâmetros de Física / Curva | Propósito Visual |
| :--- | :--- | :--- | :--- |
| **Holographic Card** | Spring Motion (`motion/react`) | `stiffness: 200, damping: 25` | Inclinação 3D realista sem oscilação excessiva após o cursor parar. |
| **Dock Text** | Spring Motion (`motion/react`) | `stiffness: 150, damping: 20, mass: 0.5` | Expansão rápida e leve com retorno elástico orgânico ao deselecionar. |
| **Animated Shiny Button** | CSS Conic Transition | `800ms cubic-bezier(0.25, 1, 0.5, 1)` | Rotação fluida da luz na borda com desaceleração suave nas curvas. |
| **Font Weight Text** | CSS Keyframes Alternate | `1.5s cubic-bezier(0.37, 0, 0.63, 1) infinite` | Respiração orgânica contínua da espessura tipográfica da fonte variável. |
| **Animated Frameworks** | CSS 3D Keyframe Transition | `1000ms ease-out` com ciclo de `1200ms` | Elevação de cartas isométricas em gravidade zero suave. |
| **Map Drop Pins** | Keyframe Spring Easing | `y: [-20, 0, 4, 0], scale: [0.75, 1], ease: "easeOut"` | Efeito de impacto tátil de pino caindo no mapa e assentando com quique. |

---

### Receitas de Implementação em Código Real

Abaixo estão duas receitas de alta fidelidade extraídas e calibradas a partir da engenharia do Eldora UI:

#### Receita 1: Animated Shiny Button com CSS Houdini & Gradiente Conico

Este componente reproduz o botão de conversão mais emblemático do Eldora UI, combinando CSS `@property` nativo para rotação suave de ângulos de gradiente com Tailwind CSS e suporte a modo escuro/claro:

```tsx
"use client"

import React from "react"
import { ChevronRight } from "lucide-react"

interface ShinyButtonProps extends React.ButtonHTMLAttributes<HTMLButtonElement> {
  children: React.ReactNode
  url?: string
  className?: string
}

export function AnimatedShinyButton({
  children,
  url,
  className = "",
  ...props
}: ShinyButtonProps) {
  const content = (
    <>
      <style jsx>{`
        @property --gradient-angle {
          syntax: "<angle>";
          initial-value: 0deg;
          inherits: false;
        }

        @property --gradient-angle-offset {
          syntax: "<angle>";
          initial-value: 0deg;
          inherits: false;
        }

        @property --gradient-percent {
          syntax: "<percentage>";
          initial-value: 5%;
          inherits: false;
        }

        @property --gradient-shine {
          syntax: "<color>";
          initial-value: white;
          inherits: false;
        }

        @keyframes gradient-angle {
          to {
            --gradient-angle: 360deg;
          }
        }

        .shiny-cta {
          --shiny-cta-bg: #09090b;
          --shiny-cta-bg-subtle: #18181b;
          --shiny-cta-fg: #ffffff;
          --shiny-cta-highlight: #06b6d4;
          --shiny-cta-highlight-subtle: #0891b2;
          --animation: gradient-angle 3.5s linear infinite;

          isolation: isolate;
          position: relative;
          overflow: hidden;
          cursor: pointer;
          outline-offset: 4px;
          padding: 0.75rem 1.75rem;
          font-family: var(--font-sans, system-ui);
          font-size: 0.95rem;
          font-weight: 500;
          border: 1px solid transparent;
          border-radius: 9999px;
          color: var(--shiny-cta-fg);
          background:
            linear-gradient(var(--shiny-cta-bg), var(--shiny-cta-bg)) padding-box,
            conic-gradient(
                from calc(var(--gradient-angle) - var(--gradient-angle-offset)),
                transparent,
                var(--shiny-cta-highlight) var(--gradient-percent),
                var(--gradient-shine) calc(var(--gradient-percent) * 2),
                var(--shiny-cta-highlight) calc(var(--gradient-percent) * 3),
                transparent calc(var(--gradient-percent) * 4)
              )
              border-box;
          box-shadow: inset 0 0 0 1px var(--shiny-cta-bg-subtle), 0 10px 25px -5px rgba(6, 182, 212, 0.25);
          animation: var(--animation);
          transition: transform 0.2s cubic-bezier(0.25, 1, 0.5, 1), box-shadow 0.3s ease;
        }

        .shiny-cta:hover {
          transform: scale(1.02);
          box-shadow: inset 0 0 0 1px var(--shiny-cta-highlight), 0 15px 30px -5px rgba(6, 182, 212, 0.4);
        }

        .shiny-cta:active {
          transform: scale(0.98);
        }
      `}</style>
      <button className={`shiny-cta inline-flex items-center gap-2 group ${className}`} {...props}>
        <span>{children}</span>
        <ChevronRight className="w-4 h-4 transition-transform duration-300 group-hover:translate-x-1 text-cyan-400" />
      </button>
    </>
  )

  if (url) {
    return (
      <a href={url} className="inline-block no-underline">
        {content}
      </a>
    )
  }

  return content
}
```

---

#### Receita 2: Micro-Simulador Clerk OTP para Apresentação de Segurança

Este componente demonstra a capacidade do Eldora UI de construir cards de autoridade técnica com digitação autônoma e anéis de foco pulsantes:

```tsx
"use client"

import React, { useEffect, useState } from "react"
import { motion, AnimatePresence } from "motion/react"
import { ShieldCheck } from "lucide-react"

interface ClerkOTPProps {
  cardTitle?: string
  cardDescription?: string
  delay?: number
}

const generateDigits = () =>
  Array.from({ length: 6 }, () => Math.floor(Math.random() * 10).toString())

export function SimulatedClerkOTP({
  cardTitle = "Two-Factor Verification",
  cardDescription = "Hardware keys, biometric passkeys, and time-based OTP codes verified sub-millisecond.",
  delay = 3800,
}: ClerkOTPProps) {
  const [digits, setDigits] = useState<string[]>(generateDigits)
  const [activeIndex, setActiveIndex] = useState(0)

  useEffect(() => {
    const cycle = setInterval(() => {
      setDigits(generateDigits())
      setActiveIndex(0)
    }, delay)

    return () => clearInterval(cycle)
  }, [delay])

  useEffect(() => {
    if (activeIndex >= 6) return
    const timer = setTimeout(() => {
      setActiveIndex((prev) => prev + 1)
    }, 280)
    return () => clearTimeout(timer)
  }, [activeIndex])

  return (
    <div className="relative w-full max-w-md p-6 bg-zinc-950/90 border border-zinc-800 rounded-2xl shadow-2xl backdrop-blur-md overflow-hidden">
      {/* Luz ambiente ciano difusa no topo */}
      <div className="absolute -top-12 left-1/2 -translate-x-1/2 w-48 h-20 bg-cyan-500/15 rounded-full blur-2xl pointer-events-none" />

      <div className="flex items-center gap-3 mb-4">
        <div className="flex items-center justify-center w-9 h-9 rounded-lg bg-zinc-900 border border-zinc-700/60 text-cyan-400 shadow-inner">
          <ShieldCheck className="w-5 h-5" />
        </div>
        <div>
          <h3 className="text-sm font-semibold text-zinc-100">{cardTitle}</h3>
          <p className="text-xs text-zinc-400">{cardDescription}</p>
        </div>
      </div>

      {/* Grade de 6 slots OTP */}
      <div className="grid grid-cols-6 gap-2 my-6">
        {Array.from({ length: 6 }).map((_, i) => {
          const isFilled = i < activeIndex
          const isCurrent = i === activeIndex

          return (
            <div
              key={i}
              className={`relative flex items-center justify-center h-14 rounded-xl border text-xl font-mono font-bold transition-all duration-200 ${
                isFilled
                  ? "border-cyan-500/80 bg-cyan-950/20 text-cyan-300 shadow-[0_0_15px_rgba(6,182,212,0.2)]"
                  : isCurrent
                  ? "border-zinc-500 bg-zinc-900/80 text-white ring-2 ring-cyan-500/40"
                  : "border-zinc-800/80 bg-zinc-900/40 text-zinc-600"
              }`}
            >
              <AnimatePresence mode="popLayout">
                {isFilled && (
                  <motion.span
                    key={digits[i]}
                    initial={{ opacity: 0, y: 10, scale: 0.5 }}
                    animate={{ opacity: 1, y: 0, scale: 1 }}
                    exit={{ opacity: 0, scale: 0.8 }}
                    transition={{ type: "spring", stiffness: 350, damping: 25 }}
                  >
                    {digits[i]}
                  </motion.span>
                )}
              </AnimatePresence>

              {/* Cursor piscante no slot ativo */}
              {isCurrent && (
                <motion.div
                  animate={{ opacity: [1, 0, 1] }}
                  transition={{ duration: 0.8, repeat: Infinity, ease: "linear" }}
                  className="w-0.5 h-6 bg-cyan-400 rounded-full"
                />
              )}
            </div>
          )
        })}
      </div>

      <div className="flex items-center justify-between text-[11px] text-zinc-500 font-mono">
        <span>ENCRYPTION: TLS 1.3 + AES-256</span>
        <span className="text-emerald-400 flex items-center gap-1.5">
          <span className="w-1.5 h-1.5 rounded-full bg-emerald-400 animate-pulse" />
          ACTIVE GUARDIAN
        </span>
      </div>
    </div>
  )
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao compor a arquitetura de interface e a especificação de design systems em projetos que utilizam o **Eldora UI**, a inteligência artificial deve seguir rigorosamente as seguintes diretrizes:

### 1. Declaração de Stack & Registro Shadcn
- Declarar o Eldora UI como o fornecedor primário de **efeitos cênicos de conversão e simulações DevTools**, atuando em perfeita harmonia com o `shadcn/ui` utilitário.
- Registrar os componentes usando a convenção de imports modulares locais:
  ```ts
  import { AnimatedShinyButton } from "@/components/eldoraui/animated-shiny-button"
  import { SimulatedClerkOTP } from "@/components/eldoraui/clerk-otp"
  import { Map } from "@/components/eldoraui/map"
  import { DockText } from "@/components/eldoraui/dock-text"
  ```
- Para instalação em novos repositórios, declarar o comando via URL direta:
  `npx shadcn@latest add "https://eldoraui.site/r/<component-name>"`

### 2. Orquestração de Performance & Ciclo de Vida do WebGL
- **Pausar Shaders fora da Viewport**: Sempre que incluir `PhotonBeam` ou `Novatrix`, envolva o canvas em um container monitorado por `useInView` ou `IntersectionObserver`. Quando a seção sair da viewport, pause o loop do `requestAnimationFrame` para zerar o uso de GPU durante a navegação pelo restante da página.
- **Respeito ao `prefers-reduced-motion`**:
  ```tsx
  // Diretriz mandatória no blueprint
  const prefersReducedMotion = useReducedMotion()
  // Se true, renderize o layout estático sem rotação 3D ou conic gradients contínuos
  ```

### 3. Paleta de Cores e Tipografia Recomendada
- **Background Principal**: Tons profundos de zinco/obsidiana (`#09090b` / `bg-zinc-950`).
- **Acentos Primários (Glow & Conic)**: Turquesa e Ciano de alta saturação (`#06b6d4`, `#67e8f9`) ou Violeta Elétrico (`#8b5cf6`).
- **Superfícies de Cartão**: `bg-zinc-900/50` com bordas `border-zinc-800/80` e `backdrop-blur-md`.
- **Tipografia**: `Geist Sans` para o corpo e títulos gerais; `Geist Mono` ou `JetBrains Mono` em números, OTPs, terminals e dados técnicos de engenharia.

### 4. Distribuição Cênica por Seções (Blueprint Template)
- **Hero Section**: Título limpo com `Geist Sans` + subtítulo persuasivo + `AnimatedShinyButton` como CTA primário + plano de fundo sutil `Novatrix` com opacidade reduzida ou `SafariBrowser` enquadrando o produto.
- **Social Proof / Parcerias**: `LogoTimeline` ou `Marquee` com logos monocromáticos (`opacity-60 hover:opacity-100`).
- **Bento Grid de Funcionalidades**:
  - Célula 1: `ClerkOTP` (Segurança e Autenticação).
  - Célula 2: `GitHubInlineComments` (Revisão e DevTools).
  - Célula 3: `AnimatedFrameworks` (Compatibilidade e APIs).
  - Célula 4: `Map` com Avatar Pins (Presença e Latência Global).
- **Pricing**: Cartão central destacado com contorno de reflexo sutil ou `HolographicCard`.
- **Footer CTA**: Fechamento dramático com `AnimatedShinyButton` reiterando o valor da solução.
