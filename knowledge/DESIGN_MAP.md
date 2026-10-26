# DESIGN MAP — Bússola Heurística e Matriz de Decisão do Agente

Este documento é o **Ponto de Entrada (Nível 1)** para o agente de IA. Antes de sugerir qualquer estilo, biblioteca ou animação, consulte esta matriz para cruzar o pedido do usuário com as 7 camadas do catálogo e evitar escolhas genéricas.

---

## 1. Matriz de Rotas Heurísticas por Arquétipo de Projeto

| Arquétipo de Projeto | DNA Estético Recomendado | Camada 5/6: Inspiração & Layout | Camada 7: Tipografia | Camada 2: Base (60%) | Camada 3: Fluidez (30%) | Camada 1/4: Showstoppers (10%) | Contraindicação Crítica (EVITAR) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **SaaS B2B / DevTools / IA de Precisão** | Dark Craft, Micro-Tátil, Alta Precisão | `godly`, `recent-design`, `saaspo`, `nicelydone` | Geist Sans + Geist Mono (`typewolf`) | `shadcn-ui`, `radix-ui`, `coss-ui` | `motion-dev`, `lenis`, `60fps-design` | `cult-ui`, `magicui`, `skiper-ui`, `21st-dev` | Gradientes roxos saturados, animações lentas (>300ms) |
| **Fintech / Analytics / Dashboard Denso** | Utilitário Cirúrgico, Grid Rigoroso | `refero`, `saasinterface`, `mobbin`, `pageflows` | Inter Display + Inter Tabular (`fontsinuse`) | `tremor`, `kibo-ui`, `shadcn-ui`, `react-aria` | `transitions-dev`, `eased-dev`, `interior-dev` | `microkit`, `uselayouts` (micro-feedbacks discretos) | Shaders 3D de fundo, scroll hijacking, efeitos neon |
| **E-commerce de Luxo / Moda / Arquitetura** | Editorial Suíço, Silêncio Visual | `siteinspire`, `minimal-gallery`, `ecomm-design`, `readymag` | Serif Editorial + Neo-Grotesk (`typ-io`, `fontpair`) | `base-ui`, `ark-ui`, Tailwind puro | `lenis`, `gsap`, `scroll-driven-animations` | `smoothui`, `osmo-supply`, `transitions-dev` | Bordas arredondadas pesadas, badges coloridos de SaaS |
| **Landing Page Criativa / Web3 / Agência** | Imersivo, Cinético, Experimental | `awwwards`, `hoverstates`, `maxibestof`, `dark-design` | Display Expressiva + Mono Industrial (`fontsinuse`) | `radix-ui`, `framer-marketplace` | `gsap`, `lenis`, `codrops` | `shaders-paper`, `shadergradient`, `threejs`, `aceternity`, `vault-hyperiux` | Layouts corporativos engessados de 3 colunas iguais |
| **Design Editorial Japonês / Conceitual** | Assimétrico, Linhas Finas (`1px`), Contemplativo | `81-web`, `muuuuu-org`, `japanwebdesign`, `bm-s5-style` | Mincho Serif + Gothic Sans + Vertical Text (`typewolf`) | CSS Grid nativo, `base-ui` | `lenis`, `eased-dev`, `designspells` | `animata`, `fancycomponents`, `vfx-js` | Sombras pesadas (`box-shadow` difuso), cards estilo Bootstrap |
| **Produto Digital Mobile-First / Consumer App** | Fluidez Física, Feedback Tátil Imediato | `mobbin`, `screenlane`, `details-so`, `uigarage` | SF Pro / Plus Jakarta Sans (`fontpair`) | `heroui`, `vaul`/`shadcn-ui`, `bits-ui` | `react-spring`, `motion-dev`, `rive`, `lottiefiles` | `motion-primitives`, `animate-ui`, `kokonutui` | Hover-only interactions sem equivalente touch |
| **Brutalismo Digital / Indie / Manifesto** | Cru, Tipográfico, Alto Contraste, Honesto | `brutalistwebsites`, `deadsimplesites`, `httpster` | Monospace Crua + Grotesca Pesada (`fontsinuse`) | HTML/CSS semântico, `melt-ui`, `daisyui` (custom) | Transições secas (`steps()` ou `0ms`), `hover-dev` | `uiverse`, `bencho-dev`, `rareui` | Glassmorphism, blur suave, sombras delicadas |

---

## 2. Índice Progressivo de Dossiês Mapeados

Conforme os subagentes concluem a análise profunda de cada um dos 150 links, os dossiês ficam disponíveis nas respectivas pastas:
- `knowledge/1-components/` (Links #001 a #040)
- `knowledge/2-design-systems/` (Links #041 a #064)
- `knowledge/3-motion/` (Links #065 a #083)
- `knowledge/4-shaders-3d/` (Links #084 a #088)
- `knowledge/5-galleries/` (Links #089 a #139)
- `knowledge/6-templates/` (Links #140 a #146)
- `knowledge/7-typography/` (Links #147 a #150)

Consulte `knowledge/INGESTION_TRACKER.md` para verificar o status individual e o caminho exato de cada arquivo `.md`.
