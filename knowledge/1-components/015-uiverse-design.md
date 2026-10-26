---
id: "uiverse-design"
name: "Uiverse Design Gallery & Systems"
url: "https://uiverse.io/design/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["CSS-First Craft", "Glassmorphic Compositions", "Cyberpunk & Neon Shimmer", "Retro Brutalism & Soft Neumorphism", "Framework-Agnostic Design Systems"]
densidade_informacao: "Media"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Baixo (CSS Puro) a Medio (Motion/Transforms)"
stack_frameworks: ["HTML5 / CSS3 Puro", "Tailwind CSS", "React", "Next.js", "Vue.js", "Svelte"]
compatibilidade:
  fontes_ideais: ["Inter", "Space Grotesk", "Outfit", "JetBrains Mono", "Syne"]
  paletas_ideais: ["Obsidian Neon Void (#0b0c10, #1f2833, #66fcf1)", "Frosted Deep Glass (#0f172a, #1e293b, #38bdf8)", "Retro Electric Monolith (#000000, #ffffff, #ffe600, #ff0055)"]
  combinacoes_recomendadas: ["Shadcn UI", "Tailwind CSS", "Lucide React", "Framer Motion", "Magic UI"]
  conflitos_esteticos: ["Mistura caótica de estilos discordantes (ex: Neumorfismo fofo com Cyberpunk neon e Brutalismo flat na mesma tela)", "Superpopulação de loaders animados e botões brilhantes concorrendo por atenção"]
---

# Uiverse Design Gallery & Systems — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Uiverse.io** consolidou-se como o maior ecossistema global open-source orientado à comunidade para micro-componentes de interface, contabilizando dezenas de milhares de elementos compartilhados sob licença MIT. No entanto, a sua divisão **Uiverse Design Gallery** (`https://uiverse.io/design/`) e seus **Design Systems orientados a IA** representam uma evolução conceitual determinante: a transição de botões e switches avulsos para **composições completas, widgets integrados, cartões holográficos e sistemas de design portáteis com contratos semânticos (`DESIGN.md` e `system.css`)**.

A assinatura e os pilares de design do ecossistema Uiverse Design caracterizam-se por:

- **Soberania do CSS Puro (Zero Runtime Overhead)**: Quase a totalidade dos efeitos visuais mais impressionantes — reflexos holográficos, feixes cônicos rotativos, deformações tridimensionais, iluminação de bordas e scanlines de CRT — é computada puramente pela engine de renderização CSS nativa do navegador (`@property`, `conic-gradient`, `backdrop-filter`, `transform-style: preserve-3d`). Isso garante 60 a 120 FPS sem inflar o bundle JavaScript com bibliotecas externas de física ou renderização 3D.
- **Ecletismo Estético Curado**: Diferente de bibliotecas corporativas monocórdicas, a galeria Uiverse compõe uma ponte viva entre os estilos de vanguarda do design digital:
  - *Advanced Glassmorphism*: Cartões fumê translúcidos com refração, dispersão de luz em gradiente radial e bordas de 1px com transparência calculada.
  - *Cyberpunk & Dark Sci-Fi*: Estruturas com corte chanfrado (`clip-path`), grades de dados, indicadores de status com brilho de néon e micro-detalhes técnicos inspirados em telemetria espacial.
  - *Neo-Brutalism High Contrast*: Traços pretos pesados (`border-4 border-black`), sombras sólidas deslocadas (`box-shadow: 6px 6px 0px #000`), cores de preenchimento elétricas e tipografia em alto impacto.
  - *Tactile Neumorphism & Soft UI*: Relevos de plástico macio esculpidos com duplas de sombras côncavas e convexas milimetricamente balanceadas.
- **Packs Machine-Readable para AI Agents (`DESIGN.md` + `system.css`)**: O Uiverse Design introduziu especificações estruturadas para ambientes de desenvolvimento assistidos por Inteligência Artificial (Cursor, Windsurf, Claude Code). O arquivo `DESIGN.md` serve como contrato unificado de verdade estética (regras de espaçamento, tipografia, contraste e papéis de componentes), enquanto o `system.css` encapsula os tokens como variáveis CSS universais, prevenindo o fenômeno comum de "AI visual drift" (onde a IA gera componentes heterogêneos e desconexos).
- **Abordagem Copy-Paste Universal**: Cada layout, card composto ou widget da galeria é disponibilizado em código aberto desimpedido (HTML/CSS nativo ou classes Tailwind CSS), permitindo que engenheiros de interface inspecionem, adaptem e acoplem o padrão a qualquer framework moderno (React, Next.js, Vue, Svelte, Astro).

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados
1. **Web3, Criptoeconomia & Protocolos Descentralizados**: Cartões holográficos de colecionáveis, banners de staking, visualizadores de transações e dashboards de liquidez que demandam acabamento lumínico futurista.
2. **Plataformas de IA, DevTools & Infraestrutura Cloud**: Terminais com estética hacker/cyberpunk, barras de status de agentes autônomos, monitores de latência e painéis operacionais de alta fidelidade visual.
3. **Startups B2C, D2C & Produtos Digitais de Consumo**: Landing pages voltadas para público jovem e criativo (apps de áudio/música, redes sociais de nicho, plataformas de streaming e gaming hubs).
4. **Indie Hackers & Lançamentos Rápidos de Alto Impacto**: Projetos solo que necessitam de uma estética imediatamente impactante e memorável sem a necessidade de uma equipe dedicada de design de produto durante a fase de validação.
5. **Portfólios Pessoais de Criativos e Engenheiros de Frontend**: Vitrines digitais onde a excelência visual do código e a mestria em animações CSS servem como cartão de visitas profissional.

### Papel no Ritmo Visual (Regra 60-30-10)
- **60% (Fundação Estrutural e Tipográfica)**: Mantenha a carcaça do layout limpa e consistente utilizando as variáveis do `system.css` ou classes neutras do Tailwind (`bg-slate-950`, `text-slate-100`, tipografia `Inter` ou `Space Grotesk` legível). Não polua fundos nem textos principais com efeitos exuberantes.
- **30% (Camada Tátil e Cartões Compostos)**: Utilize os cards compostos da galeria Uiverse (como Glass Bento Cards, formulários de autenticação flutuantes e painéis de estatísticas) para construir as seções de funcionalidades e os blocos de conteúdo principais.
- **10% (Showstoppers e Pontos de Clímax)**: Reserve os componentes de altíssimo impacto sensorial (cartão holográfico com tilt 3D, botão de plasma neon na Hero, widget de áudio interativo ou badge de status com scanline pulsante) estritamente para o botão de ação principal (Hero CTA) ou para o card protagonista da página.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Aplicações Médicas, Financeiras Tradicionais e Contábeis (Sistemas Críticos de Auditoria)**: Nesses domínios, a menor perda de contraste em decorrência de vidros translúcidos ou bordas luminosas gera desconfiança institucional e compromete a legibilidade de dados numéricos densos.
- **Portais Governamentais e Serviços sob WCAG AAA Mandatório**: Efeitos de texto com brilho difuso, sombras suaves de baixo contraste e fundos transparentes móveis geram reprovações automáticas em testes estritos de acessibilidade.
- **Interfaces com Alta Densidade de Dados Concorrentes (Data Tables / BI Corporativo)**: Adicionar animações complexas em tabelas de 5.000 linhas ou cartões repetitivos em massa degrada severamente a GPU do usuário e desvia a atenção da análise analítica.

### ⚠️ Erros Comuns de Exagero (Anti-Padrões & "AI Slop"):
- **Colcha de Retalhos Visual (Frankenstein Syndrome)**: O erro mais comum ao usar o Uiverse é copiar um botão brutalista amarelo vibrante, inseri-lo dentro de um card neumórfico cinza fofo e posicionar ao lado um widget cyberpunk roxo neon. Cada projeto deve selecionar **um único DNA visual** e harmonizar todos os elementos importados com a mesma paleta de tokens.
- **Looping Desenfreado de Animações CSS**: Ter 12 elementos na tela piscando, rodando gradientes cônicos e flutuando ao mesmo tempo. Isso causa sobrecarga cognitiva no usuário e esgota a bateria de smartphones.
- **Falta de Fallback para `@media (prefers-reduced-motion)`**: Não desativar animações infinitas de rotação e pulso para usuários com sensibilidade vestibular.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 10 padrões compostos mais influentes e representativos do ecossistema Uiverse Design:

### 1. Composed Holographic Glass Card (Cartão Holográfico Multicamada)
- **Anatomia Visual**: Cartão com fundo escuro semi-translúcido (`background: rgba(18, 18, 24, 0.6)`), desfoque traseiro (`backdrop-filter: blur(20px)`), borda com gradiente linear sutil e uma sobreposição reflexiva (*sheen overlay*) que simula a física de refração de um cartão holográfico de platina.
- **Gatilho de Interação**: `onMouseMove` que calcula o ângulo tridimensional de rotação (`rotateX`, `rotateY`) e move a coordenada do gradiente reflexivo em sincronia com o ponteiro.
- **Onde encaixar**: Cartões de planos de preços premium (Tier Pro), cartões de apresentação de membro/perfil, ou cartão de destaque na Hero.

### 2. Cyberpunk Telemetry & AI Status Widget (Widget de Status com Glow Reativo)
- **Anatomia Visual**: Caixa geométrica com cantos cortados a 45 graus via `clip-path: polygon(...)`, linhas de varredura CRT horizontais sutis, indicador LED pulsante em ciano/lima elétrico e tipografia técnica monoespaçada.
- **Gatilho de Interação**: Pulso contínuo do indicador de conexão, scanline suave em loop de 3 segundos, e expansão de aura fluorescente ao passar o mouse (`box-shadow: 0 0 20px rgba(102, 252, 241, 0.4)`).
- **Onde encaixar**: Painéis de monitoramento de agentes de IA, status de API em tempo real na Hero de DevTools, ou rodapé de console.

### 3. Tactile Audio Visualizer & Media Hub (Widget de Mídia Tátil)
- **Anatomia Visual**: Widget composto contendo carrossel de capa de álbum com borda acetinada, equalizador gráfico com 5 a 8 barras verticais oscilantes animadas via CSS puro, controle deslizante de volume personalizado e botões táteis de ação com micro-sombras chanfradas.
- **Gatilho de Interação**: Clique para alternar entre reprodução e pausa (pausando as animações CSS via `animation-play-state: paused`), e hover reativo com aumento de escala das barras sonoras.
- **Onde encaixar**: Portfólios de produtores e artistas, landing pages de podcasts/streaming, ou widgets laterais de dashboards de entretenimento.

### 4. Neo-Brutalist Callout / Action Banner (Banner de Alto Impacto e Contraste)
- **Anatomia Visual**: Superfície amarela neon (`#ffe600`) ou verde menta vibrante contornada por bordas pretas densas de 3px a 4px, acompanhada por sombra sólida preta com deslocamento diagonal de 6px sem qualquer desfoque gaussiano. Tipografia em caixa alta condensada com badges angulares.
- **Gatilho de Interação**: No hover, o elemento se translada levemente (`transform: translate(-2px, -2px)`) e a sombra cresce para 8px; no clique (`:active`), o elemento se desloca na direção da sombra (`transform: translate(4px, 4px)`) com a sombra encolhendo para 2px, gerando resposta tátil de botão mecânico real.
- **Onde encaixar**: Banners de anúncio no topo da página (Announcement Bar), blocos de cupom/desconto, ou cartões de conversão final (Pre-footer CTA).

### 5. Multi-Step Glassmorphic Auth / Checkout Container (Card de Autenticação Flutuante)
- **Anatomia Visual**: Modal/card flutuante com camadas empilhadas de vidro fosco, inputs estilizados com o padrão de rótulo flutuante (*floating label* que migra para o topo ao receber foco) e divisores com gradiente que desvanece nas extremidades.
- **Gatilho de Interação**: `:focus-within` nos campos de entrada que acende a borda com um anel lumínico suave, e botão de envio com efeito contínuo de varredura luminosa (*shimmer sweep*).
- **Onde encaixar**: Telas de login/registro flutuantes, checkout rápido em 1 clique, ou modais de assinatura de newsletter.

### 6. Neumorphic Soft Switch & Segmented Control (Seletor Tátil Macio)
- **Anatomia Visual**: Base em tom off-white ou cinza profundo com cavidade esculpida na superfície através de sombras internas (`box-shadow: inset 3px 3px 6px ...`). O botão interno repousa elevado com sombras externas suaves, criando a ilusão tátil de borracha ou plástico texturizado.
- **Gatilho de Interação**: Clique que inverte as sombras de côncavas para convexas com transição amortecida de 250ms, transmitindo a sensação de um interruptor físico afundando.
- **Onde encaixar**: Alternadores de faturamento (Mensal vs Anual) na tabela de preços, seletores de tema (Dark/Light) e abas de configuração em painéis de preferências.

### 7. Bento Grid Card com Dynamic Conic Border (Borda de Plasma Rotativa)
- **Anatomia Visual**: Cartão retangular com cantos generosos (`rounded-2xl`) onde a borda externa não é estática, mas sim um feixe luminoso colorido que percorre o contorno em rotação suave de 360 graus, utilizando a API CSS `@property --angle` para garantir aceleração por GPU.
- **Gatilho de Interação**: Aceleração da rotação da luz e desfoque luminoso expandido ao passar o mouse.
- **Onde encaixar**: Grade Bento central na seção de diferenciais (Features Bento Grid), destacando o produto principal ou funcionalidade estrela.

### 8. Radial Gamification & Tier Progress Badge (Emblema de Conquista Circular)
- **Anatomia Visual**: Emblema circular com anel SVG graduado representando progresso percentual (`stroke-dashoffset`), centro com ícone tridimensional translúcido e partículas estáticas em gradiente que sugerem nível avançado ou desbloqueio de conquista.
- **Gatilho de Interação**: Animação de entrada fluida revelando o percentual de 0 a 100%, com efeito de pulso reflexivo (*ping animation*) quando o cursor repousa sobre a insígnia.
- **Onde encaixar**: Painéis de perfil de usuário em SaaS, telas de retenção e dashboards de pontuação/gamificação.

### 9. Shimmer Skeleton Loader com Gradiente Angular (Placeholder de Alta Fidelidade)
- **Anatomia Visual**: Bloco placeholder com cantos arredondados que substitui imagens e blocos de texto durante a requisição de dados. Uma onda luminosa de 45 graus atravessa continuamente a superfície do elemento, evitando a sensação de lentidão ou tela em branco.
- **Gatilho de Interação**: Execução automática contínua (`animation: shimmer 1.8s infinite linear`) até a hidratação completa dos dados da API, com transição de dissolução (*cross-fade*) para o conteúdo final.
- **Onde encaixar**: Telas de carregamento de feeds, grids de cards de produtos em e-commerce e seções de relatórios durante a compilação de dados.

### 10. Floating Glass Command Dock (Dock Flutuante de Atalhos Rápidos)
- **Anatomia Visual**: Barra flutuante em formato de cápsula com acabamento vítreo espesso, atalhos de teclado minimalistas gravados em badges translúcidas (`kbd`) e botões de comando agrupados organicamente.
- **Gatilho de Interação**: Expansão magnética sutil dos botões no hover, com tooltips táteis instantâneos que despontam no topo com física de mola elástica.
- **Onde encaixar**: Barra de navegação inferior em aplicações web orientadas à produtividade, consoles de edição ou barra de busca global de documentações.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup Recomendado
A maior vantagem da abordagem Uiverse é que ela não exige a instalação de pacotes NPM proprietários ou dependências pesadas. No entanto, para integração profissional com ecossistemas React / Next.js e Tailwind CSS, recomenda-se:

```bash
# Dependências utilitárias de estilo e ícones
npm install clsx tailwind-merge lucide-react

# Opcional para física de mola avançada e orquestração de layout
npm install framer-motion
```

### Configuração de CSS Moderno (`@property` para Bordas Cônicas)
Para reproduzir efeitos de borda rotativa fluida sem gargalos de CPU, adicione as propriedades CSS tipadas no seu arquivo de estilos global (`globals.css`):

```css
@property --border-angle {
  syntax: "<angle>";
  inherits: false;
  initial-value: 0deg;
}

@keyframes spin-border {
  to {
    --border-angle: 360deg;
  }
}
```

### Física de Movimento & Curvas de Transição
A curadoria do Uiverse Design baseia-se em curvas de aceleração refinadas para transições puramente em CSS e parâmetros de física de mola quando acoplado ao Framer Motion:

1. **Transição de Cartões e Hover Macio (Smooth Easing)**:
   - CSS: `transition: all 400ms cubic-bezier(0.16, 1, 0.3, 1);` (curva inspirada nas animações de sistema do iOS/macOS).
2. **Micro-interações de Clique e Interruptores (Elastic Spring)**:
   - CSS: `transition: transform 250ms cubic-bezier(0.34, 1.56, 0.64, 1);` (leve recuo com overshoot elástico).
   - Framer Motion: `{ type: "spring", stiffness: 350, damping: 25, mass: 0.8 }`.
3. **Cartões com Tilt Tridimensional Reativo**:
   - Framer Motion: `{ type: "spring", stiffness: 200, damping: 20, mass: 0.5 }`.

---

### Receita de Código / Estrutura: Composed Bento Holographic Glass Card

Abaixo está a implementação completa e pronta para produção de um **Bento Card Holográfico** inspirado na galeria Uiverse, utilizando React, Tailwind CSS e aceleração por CSS puro:

```tsx
"use client";

import React, { useRef, useState, useCallback } from "react";
import { cn } from "@/lib/utils";
import { Sparkles, ArrowUpRight } from "lucide-react";

interface UiverseGlassCardProps extends React.HTMLAttributes<HTMLDivElement> {
  title: string;
  category: string;
  description: string;
  badge?: string;
  glowColor?: string;
}

export function UiverseGlassCard({
  title,
  category,
  description,
  badge = "Feature",
  glowColor = "rgba(56, 189, 248, 0.35)", // Tom padrão: Sky Blue
  className,
  ...props
}: UiverseGlassCardProps) {
  const cardRef = useRef<HTMLDivElement>(null);
  const [coords, setCoords] = useState({ x: 0, y: 0, percentX: 0.5, percentY: 0.5 });
  const [isHovered, setIsHovered] = useState(false);

  const handleMouseMove = useCallback((e: React.MouseEvent<HTMLDivElement>) => {
    if (!cardRef.current) return;
    const rect = cardRef.current.getBoundingClientRect();
    const x = e.clientX - rect.left;
    const y = e.clientY - rect.top;
    const percentX = x / rect.width;
    const percentY = y / rect.height;

    setCoords({ x, y, percentX, percentY });
  }, []);

  const handleMouseEnter = useCallback(() => setIsHovered(true), []);
  const handleMouseLeave = useCallback(() => {
    setIsHovered(false);
    setCoords({ x: 0, y: 0, percentX: 0.5, percentY: 0.5 });
  }, []);

  // Cálculo de rotação 3D suave baseado no quadrante do cursor
  const rotateX = isHovered ? (0.5 - coords.percentY) * 14 : 0;
  const rotateY = isHovered ? (coords.percentX - 0.5) * 14 : 0;

  return (
    <div
      style={{ perspective: "1000px" }}
      className="inline-block w-full max-w-md"
    >
      <div
        ref={cardRef}
        onMouseMove={handleMouseMove}
        onMouseEnter={handleMouseEnter}
        onMouseLeave={handleMouseLeave}
        style={{
          transform: `rotateX(${rotateX}deg) rotateY(${rotateY}deg)`,
          transformStyle: "preserve-3d",
          transition: isHovered
            ? "transform 100ms ease-out"
            : "transform 500ms cubic-bezier(0.16, 1, 0.3, 1)",
        }}
        className={cn(
          "group relative flex flex-col justify-between overflow-hidden rounded-3xl",
          "border border-white/10 bg-slate-900/60 p-7 backdrop-blur-xl",
          "shadow-2xl shadow-black/40 will-change-transform",
          className
        )}
        {...props}
      >
        {/* Camada 1: Brilho Dinâmico Radial que Acompanha o Cursor */}
        <div
          className="pointer-events-none absolute -inset-px rounded-3xl opacity-0 transition-opacity duration-300 group-hover:opacity-100"
          style={{
            background: `radial-gradient(400px circle at ${coords.x}px ${coords.y}px, ${glowColor}, transparent 80%)`,
          }}
        />

        {/* Camada 2: Reflexo Holográfico Angular (Sheen Especular) */}
        <div
          className="pointer-events-none absolute inset-0 opacity-0 transition-opacity duration-500 group-hover:opacity-100 mix-blend-overlay"
          style={{
            background: `linear-gradient(
              ${120 + coords.percentX * 60}deg,
              transparent 20%,
              rgba(255, 255, 255, 0.15) 45%,
              rgba(255, 255, 255, 0.3) 50%,
              rgba(255, 255, 255, 0.15) 55%,
              transparent 80%
            )`,
          }}
        />

        {/* Cabeçalho do Card */}
        <div className="relative z-10 flex items-center justify-between">
          <div className="flex items-center gap-2">
            <span className="flex h-7 items-center gap-1.5 rounded-full border border-sky-400/20 bg-sky-500/10 px-3 text-xs font-medium text-sky-300">
              <Sparkles className="h-3 w-3" />
              {badge}
            </span>
            <span className="text-xs uppercase tracking-wider text-slate-400">
              {category}
            </span>
          </div>

          <div className="flex h-9 w-9 items-center justify-center rounded-full border border-white/10 bg-white/5 text-slate-300 transition-transform duration-300 group-hover:scale-110 group-hover:border-sky-400/30 group-hover:text-white">
            <ArrowUpRight className="h-4 w-4" />
          </div>
        </div>

        {/* Conteúdo Textual */}
        <div className="relative z-10 my-8 flex flex-col gap-2">
          <h3 className="text-xl font-semibold tracking-tight text-white transition-colors duration-200 group-hover:text-sky-100">
            {title}
          </h3>
          <p className="text-sm leading-relaxed text-slate-300/90">
            {description}
          </p>
        </div>

        {/* Rodapé Tátil com Indicador de Ação */}
        <div className="relative z-10 flex items-center justify-between border-t border-white/5 pt-4">
          <div className="flex items-center gap-2 text-xs text-slate-400">
            <span className="inline-block h-2 w-2 rounded-full bg-emerald-400 animate-pulse" />
            <span>Sistema Operacional Ativo</span>
          </div>

          <button className="relative overflow-hidden rounded-xl bg-white/10 px-4 py-2 text-xs font-medium text-white transition-all duration-200 hover:bg-sky-500 hover:shadow-lg hover:shadow-sky-500/25 active:scale-95">
            Explorar Módulo
          </button>
        </div>
      </div>
    </div>
  );
}
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao integrar elementos da **Uiverse Design Gallery** ou um dos seus **Design Systems** no `DESIGN_BLUEPRINT.md` de um novo projeto, siga as seguintes especificações arquiteturais:

1. **Adoção do Padrão `DESIGN.md` como Fonte Única da Verdade**:
   - Inclua no blueprint a diretriz expressa: *"Este projeto adota a arquitetura de tokens e especificações do `DESIGN.md` originário do Uiverse Design Systems"*.
   - Todas as regras de tipografia, escalas modulares de espaçamento (`4px, 8px, 16px, 24px, 32px, 48px`), e raios de borda (`rounded-xl: 12px`, `rounded-2xl: 16px`, `rounded-3xl: 24px`) devem ser espelhadas nas configurações do Tailwind ou nas variáveis do `system.css`.

2. **Isolamento de Estilos (Evitar o Anti-Padrão Frankenstein)**:
   - Defina categoricamente no blueprint qual **único dialeto visual** do Uiverse será utilizado no projeto:
     - Ou *Glassmorphic Dark Mode* (tons slate/zinc, reflexos translúcidos, acentos azuis/violetas);
     - Ou *Neo-Brutalist High Contrast* (bordas pretas grossas, sombras duras deslocadas, tons primários saturados);
     - Ou *Cyberpunk Terminal* (cortes chanfrados, tons obsidiana, acentos fluorescentes).
   - **É terminantemente vedado** importar simultaneamente componentes de categorias estéticas conflitantes na mesma aplicação.

3. **Padronização de Tokens de Cores e Gradientes**:
   - Nunca copie código do Uiverse contendo valores hexadecimais arbitrários embutidos nas classes (ex: `bg-[#241a3e]`).
   - Refatore todo e qualquer elemento importado para utilizar as classes utilitárias semânticas do projeto (`bg-card`, `text-card-foreground`, `border-border`, `bg-primary/10`).

4. **Diretriz de Budget de Performance e Acessibilidade**:
   - Limite animações de gradiente cônico rotativo (`@property`) a no máximo 2 componentes visíveis simultaneamente na viewport.
   - Forneça sempre suporte à diretiva `@media (prefers-reduced-motion: reduce)`:
     ```css
     @media (prefers-reduced-motion: reduce) {
       *, ::before, ::after {
         animation-duration: 0.01ms !important;
         animation-iteration-count: 1 !important;
         transition-duration: 0.01ms !important;
       }
     }
     ```
   - Em dispositivos móveis (telas `< 768px`), desative a inclinação tridimensional contínua em eventos de `mousemove`, substituindo-a por elevação estática elegante com sombra suave.
