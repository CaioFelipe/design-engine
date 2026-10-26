---
name: design-ingest
description: Analisa, disseca e documenta profundamente links de design (bibliotecas de componentes, design systems, motores de motion, shaders 3D, galerias de inspiração e tipografia) gerando dossiês padronizados em knowledge/ e atualizando o índice central.
---

# Design Ingest — Pipeline de Análise e Catalogação de Referências

Esta skill governa a criação de dossiês técnicos profundos para cada link do catálogo do **Design Engine**.

## Regras de Ouro da Ingestão
1. **Isolamento de Contexto (1 Subagente = 1 Link)**:
   - Cada link deve ser analisado por um **novo subagente dedicado** (modelo `flash`), que analisa apenas aquele único link, escreve o relatório completo e encerra.
   - Nunca reutilize o mesmo subagente para múltiplos links para evitar poluição de contexto e perda de profundidade analítica.
2. **Profundidade Técnica e Heurística (Proibido Resumos Rasos)**:
   - O relatório deve funcionar como um **mapa guia literal para a IA**: deve explicar o DNA estético, o que torna o recurso único, quando usar, **quando NÃO usar (Contraindicações explícitas)**, inventário detalhado de componentes/padrões e **receitas técnicas / parâmetros matemáticos de animação**.
3. **Seleção do Schema Correto**:
   - **Schema A (`knowledge/templates/schema-a-components.md`)**: Para `1-components` e `2-design-systems`.
   - **Schema B (`knowledge/templates/schema-b-motion-shaders.md`)**: Para `3-motion` e `4-shaders-3d`.
   - **Schema C (`knowledge/templates/schema-c-galleries.md`)**: Para `5-galleries` e `6-templates`.
   - **Schema D (`knowledge/templates/schema-d-typography.md`)**: Para `7-typography`.

## Fluxo Passo a Passo por Link
1. **Identificar o próximo link pendente** em `knowledge/INGESTION_TRACKER.md`.
2. **Invocar um subagente novo (`Model: "flash"`)** passando:
   - O link exato, nome, categoria e o caminho de saída (`knowledge/<camada>/<id-slug>.md`).
   - O template do Schema correspondente (`A`, `B`, `C` ou `D`).
   - Instrução para pesquisar profundamente na web sobre o site/biblioteca, seus componentes, animações, stack, casos de uso e gerar o dossiê completo em português.
3. **Revisão pelo Agente Principal**:
   - Ler o arquivo `.md` gerado pelo subagente.
   - Verificar se todas as seções obrigatórias (Frontmatter YAML, Identidade, Quando Usar, Contraindicações/Quando NÃO Usar, Catálogo/Padrões e Receitas Técnicas/Física) estão completas, ricas e precisas.
   - Atualizar `knowledge/INGESTION_TRACKER.md` marcando `[x]` e `knowledge/catalog.json` / `knowledge/DESIGN_MAP.md`.
   - Partir imediatamente para o próximo link com um novo subagente.
