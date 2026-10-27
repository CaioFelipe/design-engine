# Design Engine — Diretrizes Globais de Direção de Arte e Engenharia de UI

Sempre que o usuário solicitar a criação, redesign, estruturação ou implementação de um site, landing page, aplicativo ou interface gráfica, siga este protocolo rigoroso baseado em lições práticas de produção:

---

## 1. O Checklist Obrigatório de Acompanhamento (`PROJECT_CHECKLIST.md`)
Todo projeto de design/UI DEVE iniciar com a criação do arquivo `PROJECT_CHECKLIST.md` na raiz do projeto. Este documento é o mapa vivo do projeto, visível para o usuário, e deve ser atualizado a cada avanço:

```markdown
# Checklist de Acompanhamento do Projeto — [Nome do Projeto]

## Fase 1: Diagnóstico & Briefing do Produto
- [ ] Entidade do Produto definida (Não confundir plataforma/API com o agente final).
- [ ] Público-alvo e Proposta de Valor central (O que o usuário realmente compra/usa).
- [ ] Paleta de Cores Oficial estabelecida (Base, Contraste Profundo, Acento e Sucesso).

## Fase 2: Curadoria de Referências & DNA Estético
- [ ] 3 a 5 referências mapeadas no catálogo (`knowledge/`).
- [ ] Efeitos de assinatura e materiais definidos (Glassmorphism, Shaders, Caustics, etc.).
- [ ] Sistema Tipográfico (Display + Body + Mono) selecionado.

## Fase 3: Planejamento de Seções (`SECTIONS.md`)
- [ ] Estrutura de seções gerada em `SECTIONS.md` para aprovação do usuário.
- [ ] Wireframe conceitual e objetivos de conversão alinhados.

## Fase 4: Infraestrutura & Live Preview Contínuo
- [ ] Servidor local (Vite/Next) rodando em background daemon (`IsDaemon: true`).
- [ ] Porta e URL ativa compartilhada com o usuário (`http://localhost:...`).

## Fase 5: Header + Hero Section (Exclusivo)
- [ ] Header limpo: Logo + Marca sem subtítulos desnecessários + Links sem ruído.
- [ ] Hero dentro da primeira dobra (Above the fold: Título visível sem rolagem).
- [ ] Flanqueamento espacial de cards (Laterais emolduram o centro sem comprimir).
- [ ] Mascote/Grafismo em SVG Vetorial Modular (anatomia separável em componentes).
- [ ] Purificação de AI Slop (Zero emojis, zero fake pills de telemetria).
- [ ] Auditoria de Paleta: 100% das cores oficiais aplicadas intencionalmente.

## Fase 6: Verificação Visual Real (Chrome DevTools MCP)
- [ ] Screenshot de página inteira capturado via ferramenta do navegador.
- [ ] Leitura e inspeção crítica da imagem (`read_file`).
- [ ] Refinamentos de espaçamento, contraste e física aplicados.

## Fase 7: Cascata Modular das Demais Seções
- [ ] Construção incremental (1 seção por vez, com aprovação antes da próxima).
```

---

## 2. Proibição Absoluta de "AI Slop" & Clichês Artificiais
Interfaces de padrão Awwwards e nível de produto enterprise exigem autenticidade:
- **NUNCA USE EMOJIS EM INTERFACES**: É terminantemente **PROIBIDO** utilizar emojis (ex: 🔐, ⚡, 🚀, 🌐, 🎉, 💡) em títulos, cards, botões, badges ou listas de recursos. Sempre utilize **ícones SVG vetoriais autênticos** (Lucide React, Radix, Tabler) com espessuras calibradas (`stroke-width: 1.5` ou `2`).
- **PROIBIDO O USO DE ELEMENTOS DE AI SLOP**:
  - **Fake Status Chips & Telemetria Falsa**: NUNCA crie pílulas artificiais como `v1.0 API`, `99.99% Uptime`, `sandbox-state`, `Online (verde piscando)`, `Streaming WebSocket Ativo`, `Rich UI` ou badges puramente decorativos sem função real no produto.
  - **Overdose de `rounded-full`**: Evite transformar todos os cards e containers em pílulas ovais genéricas. Utilize cantos refinados e proporcionais (`rounded-2xl`, `rounded-3xl`) com bordas translúcidas de 1px (`border-white/[0.08]` a `border-orange-500/20`).
  - **Fundos Planos Sem Profundidade ou Relação com o Tema**: Evite telas brancas chapadas sem atmosfera. Se o produto tem narrativa marinha, use ondas, cáusticas e céus; se for deep tech, use iluminação aditiva, grids suaves e materiais escuros profundos.
  - **Títulos com Tensão Tipográfica Dual-Tone**: Títulos principais devem usar tracking negativo óptico (`-0.03em` a `-0.04em`) e divisão semântica clara (cor neutra sólida + termo de ação no gradiente da marca).

---

## 3. Ativos Visuais: SVG Modular > Imagem Raster de IA
- Quando o projeto demandar um mascote, avatar, ícone temático ou elemento de identidade visual, **NUNCA confie em recortes de imagens raster de IA** (elas produzem bordas quadradas duras, artefatos de fundo e não podem ser animadas de forma limpa).
- **Crie sistemas vetoriais em SVG/React modulares** (`<MascotParts.tsx>`):
  - Camadas anatômicas separáveis (Corpo, Olhos, Bocas, Asas/Braços, Barbatanas, Bochechas).
  - Animações CSS Keyframes fluidas (respiração, bater de asas, piscar de olhos).
  - Resolução infinita (de favicon 16px a display 1024px sem pixelização).
  - Totalmente editável e reutilizável como Brand Kit.

---

## 4. Auditoria de Paleta de Cores (Regra de Ouro)
Se o usuário forneceu uma paleta de cores (ex: Azul Profundo, Laranja Tobiko, Menta/Turquesa, Branco Pérola):
- **100% das cores devem ter função intencional** visível na primeira dobra.
- **Base Neutra (Branco Pérola / Gelo #F8FAFC)**: Canvas limpo e respirável.
- **Base Contraste / Autoridade (Azul Profundo Oceano #0A1128)**: Títulos, tipografia de base, botões primários de conversão.
- **Acento / Energia (Laranja Tobiko #FF6B35)**: Mascote, gradientes de títulos, reflexos quentes, cards translúcidos.
- **Sucesso / Conexão (Toque Menta #2DD4BF)**: Indicadores de ação, setas direcionais, reflexos na água e micro-detalhes.
- Se alguma cor não estiver sendo usada, pause e integre-a antes de continuar.

---

## 5. Arquitetura CSS & Camadas de Profundidade (Sem Bugs de `-z-10`)
- Nunca use `-z-10` em elementos de fundo dentro de containers sem isolamento de stacking context, pois isso oculta o elemento atrás da cor de fundo do `body`/`main`.
- Use sempre:
  - Container da seção: `relative isolation: isolate` (ou `z-0`).
  - Camada de atmosfera / fundo: `absolute inset-0 pointer-events-none z-0`.
  - Conteúdo textual e interativo: `relative z-10`.
  - Cards e modais flutuantes: `relative z-20` (ou `z-50`).

---

## 6. Fluxo de Construção Incremental (Header + Hero Primeiro)
1. **SECTIONS.md Aprovado**: Só inicie código com o plano de seções validado.
2. **Servidor Ativo (`IsDaemon: true`)**: Deixe o frontend rodando para acompanhamento ao vivo.
3. **Exclusividade do Hero**: NUNCA crie a segunda ou terceira seção da página enquanto o Header e a Hero Section não estiverem 100% aprovados visualmente pelo usuário.
4. **Inspeção Visual com Screenshot**: Após cada rodada de alteração, tire screenshot via DevTools MCP, leia o arquivo e audite visualmente alinhamento, contraste e proporção antes de responder.
5. **Cascata**: Com o Hero aprovado, construa as seções seguintes uma a uma.
