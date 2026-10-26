---
id: "<slug-do-recurso>"
name: "<Nome Oficial>"
url: "<URL Exata>"
category: "<3-motion | 4-shaders-3d>"
schema_type: "B-motion-shaders"
dna_estetico: ["<Ex: Fluid Physics>", "<Ex: Organic WebGL>", "<Ex: Kinetic Typography>"]
densidade_informacao: "<Baixa | Media | Alta | Independente>"
impacto_visual: "<Sutil/Invisivel (Feel) | Moderado | Cinematografico/Showstopper>"
custo_computacional: "<Baixo (CSS/WAAPI) | Medio (JS RAF/Springs) | Alto (WebGL/GLSL/Three.js)>"
stack_frameworks: ["<Vanilla JS>", "<React>", "<Vue>", "<Svelte>", "<WebGL/GLSL>", "<CSS>"]
compatibilidade:
  combinacoes_recomendadas: ["<Ex: Lenis + GSAP ScrollTrigger>", "<Ex: Shadcn + Motion.dev>"]
  conflitos_esteticos: ["<Onde ou com o que não misturar>"]
---

# <Nome Oficial> — Dossiê de Física de Movimento, Transições & Shaders

## 1. Filosofia de Movimento & Sensação Física (Feel)
Explique como este motor/recurso altera a percepção sensorial da interface. É sobre inércia de rolagem, física de molas reais, linhas do tempo coreografadas, shaders generativos ou micro-transições de 60fps?

## 2. Cenários Ideais de Aplicação (Quando Usar)
- Em quais seções ou fluxos de usuário esta ferramenta é insubstituível?
- Como ela entra na **Regra 60-30-10** (como os 30% de fluidez invisível ou como os 10% de espetáculo visual)?

## 3. Contraindicações & Limites de Performance (Quando NÃO Usar)
- ⚠️ **Quando Evitar**: Contextos onde prejudica a leitura, causa motion sickness, drena bateria mobile ou atrasa a tarefa do usuário.
- ⚠️ **Regras de Acessibilidade & GPU**: Uso obrigatório de `prefers-reduced-motion`, controle de `will-change`, fallback mobile para WebGL/Shaders.

## 4. Catálogo de Efeitos, Primitivas e Padrões de Animação
Liste e descreva profundamente **6 a 10 padrões de movimento, efeitos ou shaders** presentes ou viabilizados por esta referência:
1. **Nome do Efeito / Primitiva**:
   - *Comportamento Visual*: O que acontece no estado inicial, durante a transição e no repouso.
   - *Gatilho*: Scroll progress, pointer move, layout change, mount/unmount, loop contínuo.

## 5. Matemática do Movimento & Receitas de Código
- **Parâmetros Físicos / Curvas Exatas**:
  - Curvas `cubic-bezier(x1, y1, x2, y2)` recomendadas (ex: Ease-Out-Expo, Snappy Quartz).
  - Configurações de Spring (`stiffness`, `damping`, `mass`, `restDelta`).
  - Parâmetros de Smooth Scroll (`lerp`, `duration`, `wheelMultiplier`) ou Uniforms de Shader (`uTime`, `uNoiseScale`, `uColorPalette`).
- **Boilerplate / Receita Pronta**: Código funcional (React/JS/CSS/GLSL) demonstrando a implementação limpa e performática do padrão principal.

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`
Como a IA deve especificar este motor/efeito no plano técnico do projeto antes de codificar.
