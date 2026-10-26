# Design Engine — AI Art Director & UI Intelligence Plugin

O **Design Engine** é um plugin para agentes de IA que substitui a geração automática de interfaces genéricas ("AI slop") por um processo estruturado de **Direção de Arte, Curadoria Estética e Engenharia Visual de Alta Fidelidade**.

## Arquitetura em 7 Camadas (`knowledge/`)

1. **`1-components/`**: Componentes UI e Microinterações de Destaque (*21st.dev, Cult-UI, Skiper-UI, Aceternity, MagicUI, ReactBits, Uiverse...*)
2. **`2-design-systems/`**: Bibliotecas Base, Headless e Design Systems (*Shadcn, Radix, Base UI, Kibo-UI, Tremor, HeroUI, Melt-UI...*)
3. **`3-motion/`**: Motores de Animação, Física e Transições (*Motion.dev, GSAP, Lenis, React-Spring, Eased.dev, 60fps.design, Codrops...*)
4. **`4-shaders-3d/`**: WebGL, Shaders e Efeitos 3D (*Shaders Paper Design, ShaderGradient, Three.js, VFX-JS...*)
5. **`5-galleries/`**: Inspirações de Sites, Landing Pages e Padrões Anatômicos (*Godly, Awwwards, Siteinspire, Mobbin, Refero, 81-web, BrutalistWebsites...*)
6. **`6-templates/`**: Templates e Experiências Completas (*Framer Gallery, Made-in-Webflow, Readymag, Semplice...*)
7. **`7-typography/`**: Tipografia e Identidade Visual (*Typewolf, FontsInUse, Typ.io, FontPair...*)

## Fluxo de Operação

### 1. Co-Criação de Projetos (`skills/design-director/SKILL.md`)
- **Descoberta & Diagnóstico**: Entende o produto, público-alvo e atmosfera desejada.
- **Roteamento Heurístico (`knowledge/DESIGN_MAP.md`)**: Seleciona 2 a 3 direções visuais contrastantes sem cair no clichê.
- **Cardápio de Componentes (Regra 60-30-10)**: Define a base estrutural (60%), micro-interações funcionais (30%) e componentes protagonistas "showstoppers" (10%).
- **Blueprint Técnico (`DESIGN_BLUEPRINT.md`)**: Documenta paleta de cores, tipografia, anatomia seção por seção e parâmetros de animação antes de iniciar o código.

### 2. Ingestão de Referências (`skills/design-ingest/SKILL.md`)
- Analisa links individualmente usando um dos **4 Schemas Especializados** (`knowledge/templates/`).
- Registra dossiês profundos com **DNA Estético**, **Assinaturas Visuais**, **Contraindicações Explícitas (Quando NÃO Usar)** e **Receitas Técnicas**.
- Mantém o rastreamento em `knowledge/INGESTION_TRACKER.md` e o índice em `knowledge/catalog.json`.
