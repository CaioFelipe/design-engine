---
id: "serenity-ui"
name: "Serenity UI"
url: "https://www.serenity-ui.com/"
category: "1-components"
schema_type: "A-components"
dna_estetico: ["Tactile Neomorphism", "Skeuomorphic Modern Craft", "Multi-Sensory Audio-Visual", "Organic 3D Physicality", "Luminescent Warmth"]
densidade_informacao: "Media"
impacto_visual: "Alto/Showstopper"
custo_computacional: "Medio (Framer Motion / CSS 3D) a Alto (Web Audio Synthesis / Canvas WebGL)"
stack_frameworks: ["React 18/19", "Next.js (App & Pages Router)", "Tailwind CSS (v3/v4)", "Framer Motion", "TypeScript", "Lucide React", "React Icons"]
compatibilidade:
  fontes_ideais: ["Inter", "Geist Sans", "Plus Jakarta Sans", "Patrick Hand / Gaegu (para elementos analógicos)", "JetBrains Mono"]
  paletas_ideais: ["Warm Neutral & Amber Flame (#FF6B35, #EA4E15)", "Obsidian & Deep Charcoal (#121214, #18181b)", "Vintage Parchment & Cream (#f7f1e6, #f6eedf)", "Tubelight Monochrome (Zinc/Neutral 900 com Glow Branco Especular)"]
  combinacoes_recomendadas: ["shadcn/ui (para formulários e primitivas utilitárias)", "Magic UI", "Aceternity UI", "Radix UI Primitives", "Lucide React"]
  conflitos_esteticos: ["Brutalismo Y2K cru de alto contraste sem transições", "Material Design 2 (sombras chapadas e cores primárias saturadas)", "Flat Corporate Memphis estático", "Minimalismo suíço estritamente tipográfico sem texturas"]
---

# Serenity UI — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)

O **Serenity UI**, idealizado e desenvolvido pelo engenheiro de software e designer indiano **Ayushmaan Singh** (`@ayushmxxn`), é uma das coleções de componentes abertos mais originais e instigantes do ecossistema React contemporâneo. Enquanto a vasta maioria das bibliotecas de micro-interações modernas orbita em torno do "Dark Craft" homogêneo da escola Vercel/Linear, o Serenity UI estabelece um manifesto visual distinto sob o lema: *"Components that make the web feel alive"* (Componentes que fazem a web parecer viva).

A assinatura do Serenity UI diferencia-se radicalmente de componentes utilitários genéricos através de quatro pilares técnicos e estéticos:

1. **Fusão Multissensorial & Áudio Nativo (Web Audio API Synthesis)**:
   O Serenity UI rompe a barreira puramente visual da tela ao incorporar síntese sonora programática e reprodução acústica contextual. Em componentes como o *Vintage Keyboard*, não há mero carregamento de arquivos MP3 pesados: o componente instancia nós de áudio em tempo real via Web Audio API (`AudioContext`, osciladores e ruído branco filtrado) para recriar o impacto acústico de interruptores mecânicos (*clicky* e *thocky*) com variação tonal estocástica. Em blocos de prova social (*Testimonial* e *Typewriter Testimonial*), ondas sonoras reativas e gravações vocais transformam depoimentos estáticos em experiências humanas tangíveis.

2. **Esqueumorfismo Tátil Modernizado & Texturas Analógicas**:
   Diferente do esqueumorfismo nostálgico dos anos 2010, o Serenity UI emprega um "Craft Analógico de Precisão". Componentes como o *Portfolio Book* usam shaders procedurais via filtros SVG de turbulência fractal (`feTurbulence`), granulação de papel rústico, fita adesiva washi tape semitransparente com bordas tracejadas e dobras de página tridimensionais com iluminação direcional. Os elementos parecem objetos físicos dotados de massa, inércia e rugosidade microscópica.

3. **Iluminação Volumétrica Incandescente & Gradientes Térmicos**:
   O controle de luz virtual no Serenity UI afasta-se dos gradientes roxo/ciano clichês de IA. A biblioteca prioriza fontes de calor e luminescência orgânica: o *Tubelight Navbar* emula o acendimento de uma lâmpada fluorescente tubular clássica com cones de desfoque duplo gaussiano (`blur-md` e `blur-lg`), enquanto o *Flame Button* rastreia a posição instantânea do mouse para calcular um núcleo térmico de plasma incandescente com gradientes térmicos calibrados em camadas de branco nuclear (`#FFFFF5`), laranja âmbar (`#FF5A1F`) e bordas carmesim (`#FF2D55`).

4. **Distribuição Aberta e Compatibilidade Zero-Monolith (`shadcn registry`)**:
   Seguindo a convenção moderna da arquitetura modular de UI, o Serenity UI não impõe um pacote NPM fechado que incha o `node_modules` com estilos imutáveis. Todos os componentes são expostos através do protocolo de registro oficial do shadcn (`npx shadcn@latest add ayushmxxn/serenity-ui/[component]`). O código-fonte TypeScript + Tailwind + Framer Motion é injetado diretamente no repositório do desenvolvedor, permitindo parametrização irrestrita de molas, paletas e lógica de renderização.

---

## 2. Cenários Ideais de Aplicação (Quando Usar)

### Nichos de Produto Recomendados
1. **SaaS B2B & Ferramentas Modernas de Produtividade**:
   Onde a navegação primária precisa de uma presença marcante e altamente polida (utilizando o *Tubelight Navbar* como âncora fixa ou o *Brand Marquee* para validação de clientes enterprise).
2. **Portfólios de Creative Technologists, Designers de Produto & Engenheiros Front-End**:
   Casos de uso em que o visitante avalia o nível de artesanato técnico e atenção aos detalhes. O *Portfolio Book* ou o *Carousel 360* funcionam como cartões de visita interativos incomparáveis.
3. **Plataformas de IA Conversacional, Agentes Autônomos & Aplicativos de Voz**:
   Produtos que operam com processamento de linguagem natural ou síntese vocal encontram no *Voice Testimonial Block* e no *Typewriter Testimonial* a metáfora visual perfeita para demonstrar respostas geradas e prova social auditiva.
4. **Landing Pages de Produtos Físicos, Hardware & Teclados Customizados**:
   Marcas de periféricos, produtos analógicos ou itens de estilo de vida que exigem demonstração interativa de toque, textura e sonoridade (*Vintage Keyboard*, *3D Flip Card*).

### Papel no Ritmo Visual (A Aplicação Rigorosa da Regra 60-30-10)

Para manter a interface coesa, funcional e responsiva, os componentes do Serenity UI devem ser governados pela matriz de proporções 60-30-10:

- **60% — Fundação Estrutural Neutra (shadcn/ui + Tailwind puro)**:
  Superfícies de leitura, formulários convencionais, cartões de métricas e tipografia hierárquica clara (Inter ou Geist Sans em fundos `bg-[var(--bg-primary)]` ou `dark:bg-[#121214]`). A fundação deve ser silenciosa e estável.
- **30% — Camada de Navegação & Fluidez Tátil (Micro-interações Serenity)**:
  Componentes de controle e engajamento recorrente: o *Tubelight Navbar* na extremidade superior ou flutuante inferior, o *Brand Marquee* contínuo com máscaras de borda gradativa e o *Typewriter Testimonial* integrado no bloco de depoimentos da página.
- **10% — Efeitos Showstoppers Protagonistas (Apenas 1 por Dobra Visual)**:
  Elementos de alta energia física ou sonora: o *Portfolio Book* na seção de casos de estudo, o *Vintage Keyboard* no Hero de um produto de escrita ou digitação, ou o *Carousel 360* no carrossel de recursos principais. **Regra mandatória**: nunca empilhe dois showstoppers táteis na mesma dobra de visualização para não sobrecarregar a cognição e os recursos de renderização da GPU.

---

## 3. Contraindicações Explícitas (Quando NÃO Usar)

### ⚠️ Proibido em:
- **Painéis Financeiros Densos, Terminais de Trading & Backoffices Operacionais**:
  Inserir botões com rastro de plasma térmico, sons mecânicos a cada clique ou carrosséis 3D circulares em ferramentas onde o operador precisa processar dados tabulares com agilidade introduz latência perceptiva, distração e fadiga sensorial imediata.
- **Aplicações Médicas, Governamentais e Ambientes com Requisito Estrito WCAG AAA**:
  Efeitos de virada de página complexa com perspectiva acelerada e animações contínuas sem opção de pausa imediata podem induzir desconforto vestibular ou violar critérios de contraste e acessibilidade motora.
- **Sistemas com Restrição Severa de Áudio (Ambientes Corporativos Silenciosos)**:
  Embora componentes com Web Audio API devam inicializar mutados por padrão, confiar em áudio como elemento crítico de feedback em ambientes de escritório corporativo ou hospitais é uma falha grave de usabilidade.

### ⚠️ A Síndrome do "AI Slop" & Como Evitar o Exagero Estético
O visual artesanal do Serenity UI perde todo o seu requinte quando aplicado sem parcimônia:
> *Hero com Laser Canvas piscando no fundo + Tubelight Navbar neon no topo + Flame Button pegando fogo no centro + Teclado mecânico fazendo barulho ao lado + Carrossel 3D girando logo abaixo.*

Esse acúmulo transforma uma aplicação refinada em uma demonstração confusa e ruidosa.

#### Diretrizes para Aplicação com Máxima Elegância:
1. **Respeito Religioso ao `prefers-reduced-motion`**:
   O Serenity UI possui suporte a `useReducedMotion()`. Quando ativado pelo sistema operacional do usuário, desative rotações de 360°, arremessos de cartas e transições em leque, substituindo-os por transições de opacidade instantâneas de 1ms.
2. **Moderação Acústica (Opt-in Explícito)**:
   Qualquer som sintetizado (*Vintage Keyboard* ou *Voice Testimonial*) deve iniciar no estado silencioso ou com controle claro de volume/mute, respeitando a privacidade e o foco do usuário.
3. **Calibração de Iluminação Sutil**:
   No *Flame Button* e no *Tubelight Navbar*, mantenha a luminância contida. O reflexo deve lembrar um indicador LED sutil ou filamento aquecido, não um clarão ofuscante.
4. **Isolamento de Estado de Foco**:
   Garanta que todos os botões e cartões mantenham anéis de foco acessíveis (`focus-visible:ring-2 focus-visible:ring-orange-500` ou similar), preservando a navegabilidade via teclado.

---

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)

Abaixo estão os 12 componentes mais emblemáticos da arquitetura do Serenity UI:

### 1. Tubelight Navbar (A Barra Flutuante com Lâmpada Tubelight Fluorescente)
- **Anatomia Visual**: Barra de navegação em ilha flutuante com cantos completamente arredondados (`rounded-full`), borda fina translúcida e sombra de contato. O diferencial é o indicador de aba ativa: além da pastilha fluida sob o texto (`layoutId="liquid-pill"`), há um pequeno filamento horizontal (`tubelight-lamp`) que projeta dois halos de desfoque esféricos gaussianos sobre a aba selecionada, simulando perfeitamente a luminescência de um tubo fluorescente em miniatura.
- **Gatilho de Interação**: Clique ou navegação por teclado entre abas com transição elástica guiada por mola (`spring`). Adaptação responsiva instantânea que exibe ícones em telas móveis e rótulos tipográficos em desktops.
- **Onde Encaixar**: Header fixo global da aplicação ou barra de navegação flutuante inferior para dashboards e landing pages modernas.

### 2. Vintage Keyboard (Teclado Mecânico Fotorealista com Síntese Sonora Web Audio API)
- **Anatomia Visual**: Recriação dimensional de um teclado analógico de alto padrão com acabamento em madeira nobre (usando múltiplas camadas de texturas procedurais SVG e gradientes de luz angular). Teclas tridimensionais com chanfros superiores, chanfros inferiores e sombras volumétricas projetadas sobre a placa de montagem (*plate*).
- **Gatilho de Interação**: Clique do mouse em cada tecla ou digitação real via teclado do usuário (`keydown`). Cada batida aciona uma depressão visual da tecla e dispara o sintetizador Web Audio interno (`AudioContext`), gerando um estalo mecânico com variação acústica realista.
- **Onde Encaixar**: Seções Hero de produtos de escrita, DevTools, editores de código, landing pages de hardware ou páginas interativas 404/easter-eggs.

### 3. Portfolio Book (Caderno Sketchbook 3D com Física de Virada de Página)
- **Anatomia Visual**: Livro de esboços tridimensional aberto em perspectiva isométrica (2400px de perspectiva). Possui textura tátil de papel envelhecido (`feTurbulence`), detalhes em washi tape tracejada, clip-arts ilustrativos e sombras projetadas no chão que se alargam conforme as páginas se movem.
- **Gatilho de Interação**: Clique nas abas laterais ou nas pontas dobradas (*cornerHint*) da folha. A folha executa uma rotação no eixo Y de `0deg` até `-180deg` via curva cúbica proprietária (`cubic-bezier(0.45, 0, 0.2, 1)`), com inversão instantânea de face (*backface-visibility*).
- **Onde Encaixar**: Seções de Portfólio, *About Us*, Estudos de Caso Narrativos ou Mostruários de Design em agências digitais.

### 4. Flame Button (O Botão de Plasma Térmico com Rastreamento de Proximidade)
- **Anatomia Visual**: Botão em cápsula metálica suave com tipografia monoespaçada/sans e ícone direcional. Em repouso, exibe uma borda neutra limpa. Ao receber interação, um anel térmico incandescente projeta um brilho de plasma que segue as coordenadas exatas do cursor do mouse.
- **Gatilho de Interação**: Movimento do mouse sobre o invólucro (`onMouseMove`). Um loop `requestAnimationFrame` desacoplado calcula a proximidade do cursor em relação às extremidades e renderiza múltiplos círculos concêntricos de calor (núcleo branco puro, anel laranja e borda carmesim difusa).
- **Onde Encaixar**: Botão de CTA primário na seção Hero principal, chamada final de conversão na página de preços ou inscrição em newsletters exclusivas.

### 5. Carousel 360 (Carrossel Cilíndrico Tridimensional Contínuo)
- **Anatomia Visual**: Estrutura orbital onde múltiplos cartões de imagens flutuam dispostos radialmente em torno de um cilindro virtual no espaço 3D (`perspective: radius * 3.5`, `transformStyle: preserve-3d`). O cartão atualmente alinhado ao centro é espelhado em um display de destaque ampliado com transição suave.
- **Gatilho de Interação**: Rotação automática suave por intervalo de tempo somada a controles manuais de avançar/retroceder. Ao girar, cada miniatura ajusta sua rotação no eixo Y em tempo real com atenuação elástica via Framer Motion.
- **Onde Encaixar**: Demonstração de templates, mostruários de fotos de produto, galerias de temas ou exibição de funcionalidades chave.

### 6. Voice & Video Testimonials Block (Mural de Prova Social com Waveforms de Áudio)
- **Anatomia Visual**: Grade de cartões de depoimento organizada em esteiras rolantes infinitas bidirecionais (linhas superior e inferior em sentidos opostos com máscaras graduais laterais). Cada cartão integra foto do cliente, depoimento textual, métricas de cargo e um reprodutor de áudio nativo com barras de onda sonora dinâmicas ou modal de vídeo integrado.
- **Gatilho de Interação**: Marquee contínuo com desaceleração e pausa instantânea no hover (`animation-play-state: paused`). Clique no botão play anima as barras da waveform via Framer Motion em ciclo rítmico enquanto o áudio real é executado.
- **Onde Encaixar**: Seção de Prova Social (*Social Proof*) logo após a primeira dobra de recursos ou antes da seção de precificação.

### 7. Typewriter Testimonial (Depoimento com Digitação Datilográfica & Avatar Stack)
- **Anatomia Visual**: Pilha horizontal compacta de avatares com sobreposição negativa (`-10px`). Acima da pilha, um balão flutuante de design clean exibe o depoimento do cliente selecionado. Conforme o texto é revelado caractere por caractere, um ícone de caneta oscila ritmicamente como se estivesse redigindo a mensagem à mão.
- **Gatilho de Interação**: Hover ou foco em qualquer avatar da pilha interrompe a reprodução anterior, carrega o clipe de voz associado e inicia a revelação tipográfica animada em intervalos de 60ms.
- **Onde Encaixar**: Barras laterais, seções de validação de comunidade no rodapé da página Hero ou blocos compactos de conversão.

### 8. 3D Flip Card (Pilha em Leque com Dinâmica de Peso Físico)
- **Anatomia Visual**: Pilha compacta de fotografias em repouso com inclinações estocásticas individuais (`[-3deg, 4deg, -2.5deg, 3deg]`) simulando fotos reais empilhadas sobre uma mesa.
- **Gatilho de Interação**: Ao passar o mouse sobre a pilha (*hover*), os cartões abrem-se em leque lateral com rotação tridimensional no eixo Y (`rotateY: -45deg`). Ao clicar em qualquer cartão, ele salta para frente com escala ampliada (`scale: 1.18`), enquanto os cartões secundários recuam com desfoque de 5px e opacidade atenuada. A mola possui massa reforçada (`mass: 1.6`) para transmitir sensação de inércia física real.
- **Onde Encaixar**: Destaques de equipe, portfólio visual, seleção de temas ou vitrine de recursos de produto.

### 9. Swipe Card Stack (Pilha Gestual Estilo Tinder com Física de Arremesso)
- **Anatomia Visual**: Cartões empilhados com rotação gradual e escalonamento decrescente (`scale: 1 - index * 0.035`). O cartão frontal responde a arrasto direto no espaço bidimensional.
- **Gatilho de Interação**: Arrasto livre com o mouse ou toque táctil (`drag={isFront}`). O deslocamento nos eixos X e Y é mapeado via `useTransform` em uma inclinação 3D dinâmica (`rotateX` e `rotateY`). Ao cruzar o limiar de arrasto (120px), o cartão é arremessado para o final da pilha com animação de encaixe elástica.
- **Onde Encaixar**: Mecânicas de curadoria rápida, cartões de onboarding gamificado, testes de preferência de usuário ou galerias interativas para mobile.

### 10. Brand Marquee with Edge Fade (Faixa Contínua de Logotipos)
- **Anatomia Visual**: Faixa contínua de logotipos de clientes e parceiros com espaçamento milimétrico e máscaras gradativas lineares (`mask-image: linear-gradient(to right, transparent, black 10%, black 90%, transparent)`), evitando cortes abruptos nas bordas da tela.
- **Gatilho de Interação**: Rolagem fluida contínua acelerada por GPU, com congelamento suave ao passar o cursor (`group-hover:pause`).
- **Onde Encaixar**: Logo após a dobra principal do Hero para validação imediata de autoridade e credibilidade.

### 11. Interactive Image Gallery & Lightbox (Galeria Masonry com Layout Compartilhado)
- **Anatomia Visual**: Galeria estilo alvenaria (*masonry layout*) onde cada miniatura exibe efeito de aproximação suave e revelação de legenda em gradiente escuro. Ao clicar, o elemento expande-se fluidamente para um modal em tela cheia através de morphing de geometria contínuo (`layoutId`).
- **Gatilho de Interação**: Clique na imagem abre o modal com mola de alta precisão (`stiffness: 260, damping: 28`). O componente calcula a largura da barra de rolagem do sistema e aplica compensação de preenchimento (`paddingRight`) no elemento `body`, eliminando qualquer salto visual na tela.
- **Onde Encaixar**: Páginas de projetos, arquivos fotográficos, changelogs visuais e galerias de inspiração.

### 12. Hero Laser & Canvas Background (Malha de Feixes Laser Reativa)
- **Anatomia Visual**: Pano de fundo dinâmico gerado em Canvas 2D/WebGL onde linhas de luz e partículas de dispersão projetam feixes diagonais que cruzam a grade da página, reagindo ao deslocamento da rolagem e transmitindo sensação de profundidade ótica.
- **Gatilho de Interação**: Animação em loop executada via renderizador atrelado ao `requestAnimationFrame`. Interrompe a execução automaticamente quando a viewport se desloca para fora do Hero, preservando 100% dos ciclos de CPU.
- **Onde Encaixar**: Pano de fundo exclusivo da seção Hero de produtos de alta tecnologia, IA e plataformas de nuvem.

---

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação

### Dependências & Setup
O Serenity UI opera sob o paradigma de distribuição direta em TypeScript. Não há dependências proprietárias pesadas. As bibliotecas fundamentais são:

```bash
# Instalação dos motores de animação e ícones
npm install framer-motion lucide-react react-icons clsx tailwind-merge
```

### Instalação via CLI Oficial do shadcn
Para adicionar qualquer componente diretamente à sua árvore de código:

```bash
# Exemplo 1: Adicionar a barra Tubelight
npx shadcn@latest add ayushmxxn/serenity-ui/tubelight-navbar

# Exemplo 2: Adicionar o botão com efeito de plasma
npx shadcn@latest add ayushmxxn/serenity-ui/flame-button

# Exemplo 3: Adicionar o carrossel 360
npx shadcn@latest add ayushmxxn/serenity-ui/carousel-360

# Exemplo 4: Adicionar o bloco de depoimentos com áudio
npx shadcn@latest add ayushmxxn/serenity-ui/testimonial
```

### Física de Movimento, Parâmetros de Molas & Curvas de Transição
A física do Serenity UI baseia-se em parâmetros estritos de rigidez (*stiffness*), amortecimento (*damping*) e massa (*mass*) no Framer Motion, evitando transições lineares artificiais:

| Componente / Elemento | Tipo de Transição | Parâmetros de Física | Sensação Perceptiva |
| :--- | :--- | :--- | :--- |
| **Tubelight (Liquid Pill)** | `spring` | `stiffness: 350`, `damping: 28`, `mass: 0.9` | Ágil, orgânico, deslizamento líquido |
| **Tubelight (Lamp Filamento)** | `spring` | `stiffness: 300`, `damping: 30` | Estável, sem oscilações residuais |
| **3D Flip Card (Descanso)** | `spring` | `stiffness: 300`, `damping: 22` | Retorno elástico sutil |
| **3D Flip Card (Leque)** | `spring` | `stiffness: 280`, `damping: 26` | Abertura coordenada e macia |
| **3D Flip Card (Pop Destaque)** | `spring` | `stiffness: 180`, `damping: 24`, `mass: 1.6` | Peso inercial acentuado, impacto tátil |
| **Swipe Card (Retorno)** | `spring` | `stiffness: 300`, `damping: 30` | Snap-back imediato ao soltar |
| **Portfolio Book (Virada 3D)** | `cubic-bezier` | `cubic-bezier(0.45, 0, 0.2, 1)`, `900ms` | Resistência inicial de folha e pouso suave |
| **Flame Button (Inércia Térmica)**| `RAF Easing` | `diff * 0.15` por frame | Dissipação térmica fluida sem saltos |

---

### Receita de Código: Tubelight Navbar com Luminescência Tubular Completa

Abaixo está a implementação funcional e autônoma do icônico **Tubelight Navbar**, incluindo a animação compartilhada de abas via `layoutId` e os difusores de luz em cascata:

```tsx
"use client";

import React, { useState } from "react";
import { motion } from "framer-motion";
import Link from "next/link";
import { LucideIcon, Home, User, Briefcase, FileText } from "lucide-react";

interface NavItem {
  name: string;
  url: string;
  icon: LucideIcon;
}

interface TubelightNavbarProps {
  items?: NavItem[];
  defaultActive?: string;
  className?: string;
}

const DEFAULT_ITEMS: NavItem[] = [
  { name: "Início", url: "#home", icon: Home },
  { name: "Sobre", url: "#about", icon: User },
  { name: "Projetos", url: "#projects", icon: Briefcase },
  { name: "Currículo", url: "#resume", icon: FileText },
];

export function TubelightNavbar({
  items = DEFAULT_ITEMS,
  defaultActive = "Início",
  className = "",
}: TubelightNavbarProps) {
  const [activeTab, setActiveTab] = useState(defaultActive);

  return (
    <nav
      aria-label="Navegação Principal"
      className={`fixed top-6 left-0 right-0 z-50 flex justify-center select-none px-4 ${className}`}
    >
      <div
        className="flex items-center gap-1 sm:gap-2 bg-white/90 dark:bg-neutral-900/90 backdrop-blur-md border border-black/10 dark:border-white/10 py-1.5 px-2 rounded-full shadow-[0_1px_2px_rgba(0,0,0,0.05),0_8px_20px_rgba(0,0,0,0.08)] dark:shadow-[0_4px_24px_rgba(0,0,0,0.5)] transition-all"
      >
        {items.map((tab) => {
          const isActive = activeTab === tab.name;
          const Icon = tab.icon;

          return (
            <Link
              key={tab.name}
              href={tab.url}
              onClick={() => setActiveTab(tab.name)}
              className={`relative cursor-pointer text-xs sm:text-sm px-4 sm:px-5 py-2 rounded-full transition-colors duration-200 outline-none focus-visible:ring-2 focus-visible:ring-orange-500 ${
                isActive
                  ? "text-neutral-950 dark:text-white font-semibold"
                  : "text-neutral-500 hover:text-neutral-900 dark:text-neutral-400 dark:hover:text-white"
              }`}
            >
              {/* Pastilha líquida elástica sob o item ativo */}
              {isActive && (
                <motion.div
                  layoutId="liquid-pill"
                  className="absolute inset-0 bg-neutral-100 dark:bg-neutral-800/80 rounded-full"
                  transition={{
                    type: "spring",
                    stiffness: 350,
                    damping: 28,
                    mass: 0.9,
                  }}
                />
              )}

              {/* Rótulo em desktop e ícone em telas menores */}
              <span className="relative z-10 hidden sm:inline">{tab.name}</span>
              <span className="relative z-10 sm:hidden flex items-center justify-center">
                <Icon className="w-4 h-4" />
              </span>

              {/* Simulação física da lâmpada fluorescente (Tubelight) */}
              {isActive && (
                <motion.div
                  layoutId="tubelight-lamp"
                  className="absolute -top-1.5 left-1/2 -translate-x-1/2 w-8 h-1 bg-neutral-900 dark:bg-white rounded-t-full pointer-events-none"
                  initial={false}
                  transition={{
                    type: "spring",
                    stiffness: 300,
                    damping: 30,
                  }}
                >
                  {/* Halo primário de difusão de luz */}
                  <div
                    className="absolute left-1/2 -translate-x-1/2 -top-1.5 w-6 h-6 bg-neutral-900 dark:bg-white rounded-full pointer-events-none"
                    style={{ filter: "blur(6px)", opacity: 0.2 }}
                  />
                  {/* Halo secundário volumétrico amplo */}
                  <div
                    className="absolute left-1/2 -translate-x-1/2 -top-2.5 w-10 h-8 bg-neutral-900 dark:bg-white rounded-full pointer-events-none"
                    style={{ filter: "blur(12px)", opacity: 0.1 }}
                  />
                </motion.div>
              )}
            </Link>
          );
        })}
      </div>
    </nav>
  );
}

export default TubelightNavbar;
```

---

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`

Ao projetar uma interface que aproveite os recursos do **Serenity UI**, declare as seguintes diretrizes explícitas na arquitetura do projeto:

1. **Definição de Papel do Sistema no Blueprint**:
   - Classifique o Serenity UI como **"Camada Tátil e Micro-interações de Prova Social"** (papel nos 30% ou 10% da regra 60-30-10).
   - Defina o `shadcn/ui` padrão como o alicerce estrutural dos 60% (inputs de formulário, modais utilitários, tabelas e menus contextuais).

2. **Protocolo de Integração via CLI**:
   - Instrua explicitamente o uso do prefixo de registro:
     ```markdown
     ### Dependências de UI
     - Base: `npx shadcn@latest add [component]`
     - Efeitos Táteis: `npx shadcn@latest add ayushmxxn/serenity-ui/[component]`
     ```

3. **Governança de Áudio & Acessibilidade**:
   - Componentes que executam som (*Vintage Keyboard*, *Voice Testimonial*) devem obrigatoriamente possuir um prop `enableAudio={false}` como padrão em ambientes de produção, com controle de ativação explícito fornecido ao usuário final.
   - Sempre encapsular animações gestuais e translacionais com `useReducedMotion()` para respeitar os parâmetros de acessibilidade do sistema operacional.

4. **Hierarquia de Viewport (Anti-Clutter Protocol)**:
   - Limitar rigorosamente a apenas **1 efeito cinemático ou 3D** por seção visível do layout:
     - *Dobra 1 (Hero)*: Tubelight Navbar + Headline limpa + Flame Button CTA.
     - *Dobra 2 (Logos)*: Brand Marquee com máscara suave de borda.
     - *Dobra 3 (Social Proof)*: Voice Testimonial Block em duas esteiras alternadas.
     - *Dobra 4 (Showcase)*: 3D Flip Card ou Carousel 360 isolado em fundo escuro limpo.
