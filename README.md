# Design Engine 🎨⚡
### AI Art Director & UI Intelligence Plugin for Antigravity & AI Coding Agents

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Knowledge Base](https://img.shields.io/badge/Knowledge%20Base-150%20Curated%20Links-green.svg)](#-arquitetura-em-7-camadas-150-referências-curadas)
[![Anti-AI Slop](https://img.shields.io/badge/Anti--AI%20Slop-Enforced-orange.svg)](#-o-manifesto-anti-ai-slop)
[![Antigravity Plugin](https://img.shields.io/badge/Antigravity-Plugin%20v1.0.0-purple.svg)](https://github.com/CaioFelipe/design-engine)

O **Design Engine** é um plugin de Direção de Arte e Engenharia de UI de alta precisão projetado para erradicar o "AI Slop" (interfaces genéricas, fundos escuros clichês com gradientes roxos e cards flutuantes sem propósito).

Ele transforma qualquer agente de IA (Google Antigravity, Claude Code, Cursor, Windsurf) em um **Diretor de Arte Sênior e Engenheiro Front-end de Elite**, combinando uma base de conhecimento curada de **150 referências técnicas aprofundadas** com um **fluxo rigoroso de co-criação em 7 fases** e acompanhamento contínuo via `PROJECT_CHECKLIST.md`.

---

## 🚫 O Manifesto Anti-AI Slop

Interfaces geradas por IA costumam cair em armadilhas previsíveis que denunciam a falta de intenção humana. O **Design Engine** aplica regras de produção estritas:

1. **Zero Emojis em UI Profissional**: Proibido o uso de emojis (`🚀`, `✨`, `🔥`, `💡`) como substitutos de ícones em botões, badges e cards. Utilize ícones vetoriais SVG nítidos e monocromáticos (ex: Lucide React).
2. **Zero Telemetria Falsa ("AI Slop" Decorativo)**: Banidos badges como `"Streaming WebSocket Ativo"`, `"99.9% Uptime"`, `"Rich UI"`, `"IA Integrada"` ou `"Online"` sem função operacional real no produto.
3. **Mascotes e Grafismos em SVG Vetorial Modular**: NUNCA utilize recortes rasterizados gerados por IA (PNGs com artefatos, bordas duras ou fundos pixelados). Mascotes e ilustrações centrais devem ser criados como componentes SVG modulares (`<MascotParts.tsx>`), com anatomia separável (olhos, expressões, cauda, asas, barbatanas) permitindo Brand Kits editáveis e animações fluidas.
4. **Hierarquia Espacial Rigorosa na Primeira Dobra (Above the Fold)**:
   - O H1, subtítulo e botões de ação (CTAs) devem estar **imediatamente visíveis** sem que o usuário precise rolar a tela.
   - Cards flutuantes laterais devem **flanquear as margens da viewport**, emoldurando o centro sem empurrar a tipografia para fora da dobra.
5. **Auditoria de Paleta 100% Intencional**: Todas as cores oficiais estabelecidas no briefing (Base Neutra, Contraste Profundo Corporativo, Acento e Sucesso) devem ter aplicação funcional comprovada já na primeira dobra.
6. **Disciplina de Empilhamento CSS (Stacking Context)**: Nunca use `-z-10` em camadas atmosféricas ou fundos decorativos — eles somem atrás do background principal. Use `z-0` para a atmosfera de fundo e `relative z-10` / `z-20` para containers e conteúdos interativos.

---

## 🏛 Arquitetura em 7 Camadas (150 Referências Curadas)

A pasta `knowledge/` armazena 150 dossiês técnicos detalhados com **DNA Estético**, **Casos de Uso**, **Contraindicações Explícitas (Quando NÃO Usar)**, **Inventário de Componentes** e **Receitas de CSS & Física de Animação**:

| Camada | Escopo | Referências Notáveis |
| :--- | :--- | :--- |
| **`1-components`** (40 links) | Componentes UI, Microinterações e Showstoppers | 21st.dev, Cult-UI, Skiper-UI, Aceternity UI, MagicUI, ReactBits, KokonutUI, Animata, EldoraUI, SmoothUI |
| **`2-design-systems`** (24 links) | Sistemas Base, Acessibilidade e Headless | Shadcn UI, Radix UI, Base UI, Kibo-UI, Tremor, HeroUI, Melt-UI, Preline, Float UI, DaisyUI, Skeleton |
| **`3-motion`** (19 links) | Motores de Animação, Física e Smooth Scroll | Motion.dev, GSAP Showcase, Lenis Scroll, React-Spring, Codrops Playground, Hover.dev, Eased.dev, 60fps.design |
| **`4-shaders-3d`** (5 links) | WebGL, Shaders de Superfície e 3D Interativo | Shaders Paper Design, Shaders.com, ShaderGradient, Three.js Examples, VFX-JS |
| **`5-galleries`** (51 links) | Galerias de Inspiração, Anatomia e Padrões Globais | Godly, Awwwards, Siteinspire, Mobbin, Refero, 81-web (Japão), Land-book, Dark Design, BrutalistWebsites |
| **`6-templates`** (7 links) | Ecossistemas de Templates e Canvas Modernos | Framer Gallery, Made in Webflow, Readymag Examples, Semplice Showcase, Useplanes, 21st Libraries |
| **`7-typography`** (4 links) | Sistemas Tipográficos, Pareamento e Fontes em Uso | Typewolf, Fonts In Use, Typ.io, FontPair |

> Todo o catálogo é indexado em `knowledge/catalog.json` e possui roteamento heurístico em `knowledge/DESIGN_MAP.md`.

---

## 🔄 O Fluxo de Co-Criação em 7 Fases

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                       FLUXO DE VIDA DO DESIGN ENGINE                        │
└─────────────────────────────────────────────────────────────────────────────┘
  [1. Briefing & Checklist] ──> [2. Curadoria Catálogo] ──> [3. SECTIONS.md]
                                                                    │
  [6. Verificação Visual]  <── [5. Header + Hero]      <── [4. Dev Server]
            │
  [7. Cascata Modular]
```

### 1. Diagnóstico Real & Checklist do Projeto (`PROJECT_CHECKLIST.md`)
O agente inicializa o arquivo `PROJECT_CHECKLIST.md` na raiz do projeto. Ele alinha a verdadeira entidade do produto (ex: diferenciar uma API/plataforma de mensageria dos agentes finais das empresas atendidas) e estabelece a paleta estrita de cores.

### 2. Curadoria de Referências & Orçamento Visual 60-30-10
O agente apresenta de **2 a 3 Direções Estéticas Contrastantes** e balanceia o projeto com a **Regra 60-30-10**:
- **60% Estrutura Silenciosa & Tipografia**: Grid rigoroso, fontes com escala fluida `clamp()`, contraste acessível.
- **30% Fluidez & Micro-interações**: Smooth scroll (Lenis), estados de hover rápidos (150ms–220ms), feedback tátil.
- **10% Showstoppers / Efeito Uau**: No máximo **1 protagonista por viewport** (ex: Shader 3D ou Hero com física interativa).

### 3. Planejamento de Seções para Revisão (`SECTIONS.md`)
Gera a estrutura anatômica completa da página em `SECTIONS.md` para que o usuário aprove a ordem, narrativa e objetivos de conversão antes da escrita de qualquer código.

### 4. Dev Server Contínuo (Live Preview)
Inicializa o servidor de desenvolvimento (Vite, Next.js, etc.) como um processo de fundo contínuo (`IsDaemon: true`). Fornece a URL local (`http://localhost:5173`) imediatamente para testes interativos.

### 5. Construção Exclusiva de Header + Hero Section
Foco total na primeira dobra:
- Header conciso com navegação clara (ex: "Documentação" em vez de links genéricos).
- Tipografia H1 legível e CTAs acima da linha de dobra.
- Elemento central ou mascote vetorizado em SVG modular com partes separadas.
- Atmosfera conectada à narrativa (ex: gradiente celestial com nuvens discretas no topo e base oceânica fluida com ondas orgânicas).

### 6. Verificação Visual Obrigatória (Chrome DevTools MCP)
O agente utiliza ferramentas de automação e inspeção (como o `chrome-devtools-mcp`) para capturar screenshots de página inteira, inspecionar alinhamentos, contrastes, ausência de bugs de overflow e renderização visual antes de avançar.

### 7. Cascata Modular das Demais Seções
Com a identidade visual e o Hero 100% aprovados, o agente avança para as seções seguintes uma a uma, marcando o progresso em `PROJECT_CHECKLIST.md`.

---

## 📋 Modelo Oficial: `PROJECT_CHECKLIST.md`

Todo projeto gerenciado pelo Design Engine contém este checklist ativo na raiz:

```markdown
# Checklist de Acompanhamento do Projeto — [Nome do Projeto]

## Fase 1: Diagnóstico & Briefing do Produto
- [ ] Entidade do Produto definida (Não confundir plataforma/API com o agente final)
- [ ] Público-alvo e Proposta de Valor central estabelecidos
- [ ] Paleta de Cores Oficial estabelecida (Base, Contraste Profundo, Acento e Sucesso)

## Fase 2: Curadoria de Referências & DNA Estético
- [ ] 3 a 5 referências mapeadas no catálogo (`knowledge/`)
- [ ] Efeitos de assinatura e materiais definidos (Glassmorphism, Shaders, Caustics, etc.)
- [ ] Sistema Tipográfico (Display + Body + Mono) selecionado

## Fase 3: Planejamento de Seções (`SECTIONS.md`)
- [ ] Estrutura de seções gerada em `SECTIONS.md` para aprovação do usuário
- [ ] Wireframe conceitual e objetivos de conversão alinhados

## Fase 4: Infraestrutura & Live Preview Contínuo
- [ ] Servidor local (Vite/Next) rodando em background daemon (`IsDaemon: true`)
- [ ] Porta e URL ativa compartilhada com o usuário (`http://localhost:...`)

## Fase 5: Header + Hero Section (Exclusivo)
- [ ] Header limpo: Logo + Marca sem subtítulos desnecessários + Links sem ruído
- [ ] Hero dentro da primeira dobra (Above the fold: Título e CTAs visíveis sem rolagem)
- [ ] Flanqueamento espacial de cards (Laterais emolduram o centro sem comprimir)
- [ ] Mascote/Grafismo em SVG Vetorial Modular (anatomia separável em componentes)
- [ ] Purificação de AI Slop (Zero emojis, zero fake pills de telemetria)
- [ ] Auditoria de Paleta: 100% das cores oficiais aplicadas funcionalmente
- [ ] Camadas de fundo com empilhamento correto (`z-0` na atmosfera, `relative z-10` no conteúdo)

## Fase 6: Verificação Visual (Screenshots & Auditoria)
- [ ] Screenshot de página inteira capturado via DevTools
- [ ] Contraste, alinhamentos e ausência de bugs de overflow validados visualmente
- [ ] Aprovação formal do usuário para o Hero

## Fase 7: Cascata Modular das Demais Seções
- [ ] Seção 2 construída e aprovada
- [ ] Seção 3 construída e aprovada
- [ ] Seção 4 (Pricing/Demonstração) construída e aprovada
- [ ] Footer arquitetado e aprovado
- [ ] Revisão final de responsividade (Mobile / Tablet / Desktop)
```

---

## 🚀 Como Instalar e Utilizar

### 1. No Google Antigravity (Plugin Oficial)

Para instalar o plugin no seu ambiente do Antigravity:

```bash
# Clone o repositório na sua pasta de plugins do Antigravity:
git clone https://github.com/CaioFelipe/design-engine.git ~/.gemini/antigravity/plugins/design-engine
```

Ou no Windows (PowerShell):
```powershell
git clone https://github.com/CaioFelipe/design-engine.git "$HOME\.gemini\antigravity\plugins\design-engine"
```

Reinicie o Antigravity IDE ou recarregue a janela. O plugin estará imediatamente ativo com suas skills e regras globais.

### 2. No Claude Code, Cursor, Windsurf ou Copilot

O Design Engine é agnóstico e funciona perfeitamente em qualquer agente de código:

1. Clone o repositório no seu ambiente de trabalho ou adicione-o como submódulo Git:
   ```bash
   git submodule add https://github.com/CaioFelipe/design-engine.git .design-engine
   ```
2. Adicione ao seu arquivo de regras (`.cursorrules`, `CLAUDE.md` ou `.windsurfrules`):
   ```markdown
   Siga as diretrizes de design, fluxo de trabalho e regras Anti-AI Slop documentadas em:
   - .design-engine/rules/AGENTS.md
   Consulte os 150 dossiês técnicos e receitas de componentes em:
   - .design-engine/knowledge/
   ```

---

## 📂 Estrutura do Repositório

```
design-engine/
├── .gitignore                      # Proteção de testes locais, dist, logs e envs
├── LICENSE                         # Licença de Código Aberto MIT
├── README.md                       # Documentação mestre do plugin
├── plugin.json                     # Manifesto do plugin Antigravity
├── rules/
│   └── AGENTS.md                   # Diretrizes globais de UI e Anti-AI Slop
├── skills/
│   ├── design-director/
│   │   └── SKILL.md                # Skill de co-criação em 7 fases e checklist
│   └── design-ingest/
│       └── SKILL.md                # Pipeline de ingestão e análise de novas referências
└── knowledge/
    ├── 1-components/               # 40 dossiês de bibliotecas de componentes UI
    ├── 2-design-systems/           # 24 dossiês de design systems e headless
    ├── 3-motion/                   # 19 dossiês de motores de motion e física
    ├── 4-shaders-3d/               # 5 dossiês de WebGL e shaders 3D
    ├── 5-galleries/                # 51 dossiês de landing pages e galerias de arte
    ├── 6-templates/                # 7 dossiês de templates e canvas
    ├── 7-typography/               # 4 dossiês de pareamento e sistemas tipográficos
    ├── templates/                  # 4 Schemas padronizados de análise técnica
    ├── catalog.json                # Banco de dados central indexado de 150 links
    ├── DESIGN_MAP.md               # Matriz de roteamento heurístico em 5 eixos
    └── INGESTION_TRACKER.md        # Histórico de ingestão e status dos dossiês
```

---

## 🛠 Tecnologias e Padrões Suportados

- **CSS & Frameworks**: Tailwind CSS v3 / v4, Vanilla CSS Custom Properties, OKLCH Color Space, Fluid Clamp Scales.
- **Motion & Física**: Motion (Framer Motion), GSAP, Lenis Smooth Scroll, React-Spring, Eased Curves.
- **Gráficos & 3D**: SVG Vetorial Modular, Three.js, WebGL Shaders, Canvas API.
- **Design Systems**: Shadcn UI, Radix Primitives, Base UI, Ark UI, HeroUI, Tremor.

---

## 📄 Licença

Distribuído sob a licença MIT. Veja [`LICENSE`](LICENSE) para mais detalhes.

Criado e mantido por [Caio Felipe](https://github.com/CaioFelipe).
