---
id: "<slug-do-recurso>"
name: "<Nome Oficial>"
url: "<URL Exata>"
category: "7-typography"
schema_type: "D-typography"
dna_estetico: ["<Ex: Editorial Serif>", "<Ex: Neo-Grotesque Precision>", "<Ex: Technical Monospace>"]
densidade_informacao: "<Flexivel>"
impacto_visual: "<Estrutural & Identitario (60% da interface)>"
custo_computacional: "<Baixo (Webfonts / Variable Fonts)>"
stack_frameworks: ["<CSS>", "<Next/Font>", "<Google Fonts>", "<Fontshare>"]
compatibilidade:
  combinacoes_recomendadas: ["<Estilos e galerias onde essas combinacoes brilham>"]
  conflitos_esteticos: ["<Erros tipográficos a evitar>"]
---

# <Nome Oficial> — Dossiê de Tipografia, Pares de Fontes & Hierarquia Visual

## 1. Papel da Referência & Filosofia Tipográfica
O que torna este recurso essencial para a escolha tipográfica? Como ele organiza e cura fontes em uso real na web, imprensa e produtos digitais?

## 2. Quando Consultar (Cenários de Aplicação)
- Como usar esta fonte de conhecimento para definir os **60% de Estrutura e Identidade** de um projeto?
- Quais problemas de legibilidade, personalidade ou autoridade de marca ela resolve?

## 3. Contraindicações Tipográficas (O Que Evitar)
- ⚠️ **Clichês e Erros**: Pares de fontes batidos ou mal contrastados (ex: combinar duas serifadas quase iguais, usar tracking largo em fontes display pesadas, usar Inter sem ajustes ópticos em projetos editoriais de luxo).

## 4. Matriz de Pares Tipográficos Curados (Prontos para Uso)
Forneça pelo menos **8 combinações tipográficas completas (Display/Headline + Body + Monospace)** inspiradas nos padrões desta referência, divididas por DNA Estético:
1. **SaaS Moderno / DevTools / IA de Precisão**
2. **Editorial de Luxo / Moda / Arquitetura**
3. **Fintech / Alta Densidade / Dados Tabulares**
4. **Criativo / Experimental / Brutalista**
5. **Orgânico / Sustentabilidade / Artesanal**
6. **Publicação Digital / Long-form Reading**
7. **Web3 / Futurista Industrial**
8. **Minimalismo Suíço / Institucional Moderno**
*(Para cada par, inclua a opção Premium de estúdio e a alternativa Gratuita/Open-Source de alta qualidade via Google Fonts, Fontshare ou Geist).*

## 5. Engenharia Tipográfica em CSS (Receitas Técnicas)
- **Escala Fluida com `clamp()`**: Fórmula exata para `h1`, `h2`, `h3`, `body` e `caption`.
- **Ajustes Ópticos Mandatórios**:
  - `letter-spacing` (`tracking`) por faixa de tamanho (negativo em títulos grandes `-0.03em`, neutro ou levemente positivo em caps `0.06em`).
  - `line-height` (`leading`) por função (`1.05`–`1.15` para headlines, `1.5`–`1.65` para leitura).
  - `font-feature-settings` / `font-variant-numeric: tabular-nums` / `text-wrap: balance` e `pretty`.
