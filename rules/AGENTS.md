# Design Engine — Diretrizes Globais de Direção de Arte e Engenharia de UI

Sempre que o usuário solicitar a criação, redesign ou planejamento de um site, landing page, aplicativo ou interface gráfica:

## 1. Proibição Absoluta de "AI Slop" (Design Genérico)
- **NUNCA** gere código de interface imediatamente após um pedido inicial sem antes alinhar a direção estética, a menos que o usuário peça explicitamente para pular o planejamento.
- **PROIBIDO** usar o clichê padrão de IA: fundo escuro com gradientes roxo/indigo genéricos (`from-purple-500 to-indigo-600`), cards arredondados sem função e sombras borradas mal calibradas.
- **PROIBIDO** misturar bibliotecas ou componentes de DNAs estéticos incompatíveis (sempre verifique a seção **"Contraindicações / Quando NÃO Usar"** nos dossiês em `knowledge/`).

## 2. Funil de Recuperação em 3 Níveis
Para encontrar as referências exatas sem desperdiçar contexto e sem ignorar a cauda longa do catálogo:
1. **Nível 1 (Roteamento)**: Consulte `knowledge/DESIGN_MAP.md` e `knowledge/catalog.json` para filtrar as referências ideais nos 5 eixos (DNA Estético, Densidade, Impacto Visual, Stack e Compatibilidade).
2. **Nível 2 (Curadoria & Discussão)**: Leia os dossiês específicos em `knowledge/<camada>/<slug>.md` (5 a 8 arquivos relevantes) e apresente ao usuário **2 a 3 Direções Estéticas** + um **Cardápio de Componentes e Micro-interações**.
3. **Nível 3 (Implementação)**: Após a escolha do usuário, consulte as receitas técnicas e gere um arquivo `DESIGN_BLUEPRINT.md` no projeto antes de codificar.

## 3. Regra de Orçamento Visual 60-30-10 (Anti-Frankenstein)
Mantenha harmonia visual e performance de 60 FPS aplicando a proporção:
- **60% Estrutura Silenciosa & Tipografia (`2-design-systems` + `7-typography`)**: Grid rigoroso, hierarquia tipográfica com `clamp()`, espaçamento intencional e acessibilidade (Radix, Shadcn, Base UI).
- **30% Fluidez & Micro-interações (`3-motion`)**: Smooth scroll (Lenis), transições de estado rápidas (150ms–220ms) com curvas de easing ou springs naturais.
- **10% Showstoppers / Efeito Uau (`1-components` + `4-shaders-3d`)**: No máximo **1 componente ou efeito protagonista por dobra de tela (viewport)** (ex: Hero com Shader 3D, seção de Features em Bento Grid iluminado, CTA com botão magnético).
