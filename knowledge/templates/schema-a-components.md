---
id: "<slug-do-recurso>"
name: "<Nome Oficial>"
url: "<URL Exata>"
category: "<1-components | 2-design-systems>"
schema_type: "A-components"
dna_estetico: ["<Ex: Dark Craft>", "<Ex: Modern Minimal>", "<Ex: High-Impact Motion>"]
densidade_informacao: "<Baixa | Media | Alta | Flexivel>"
impacto_visual: "<Utilitario/Base | Moderado | Alto/Showstopper>"
custo_computacional: "<Baixo (CSS/Headless) | Medio (Framer Motion/JS) | Alto (Canvas/3D)>"
stack_frameworks: ["<React>", "<Next.js>", "<Tailwind CSS>", "<Framer Motion>"]
compatibilidade:
  fontes_ideais: ["<Ex: Geist Sans>", "<Ex: Inter>", "<Ex: Plus Jakarta Sans>"]
  paletas_ideais: ["<Ex: Deep Zinc Dark Mode>", "<Ex: High-Contrast Monochrome>"]
  combinacoes_recomendadas: ["<Outras libs da lista que casam bem>"]
  conflitos_esteticos: ["<Libs ou estilos que brigam visualmente com este>"]
---

# <Nome Oficial> — Dossiê Técnico de Componentes & Design System

## 1. Identidade Visual & O Que Torna Único (Assinatura)
Descreva em detalhes a filosofia visual deste recurso. O que ele faz que o diferencia de um componente genérico? Qual é a sensação tátil, o acabamento de bordas, sombras, luzes e ritmo visual?

## 2. Cenários Ideais de Aplicação (Quando Usar)
- **Nichos de Produto**: Em quais tipos de projetos (ex: SaaS B2B, DevTools, IA, Fintech, E-commerce, Portfólio Criativo) ele é a escolha número 1?
- **Momento do Fluxo**: Deve ser usado como espinha dorsal (60%), como camada de fluidez (30%) ou como efeito protagonista/showstopper (10%)?

## 3. Contraindicações Explícitas (Quando NÃO Usar)
- ⚠️ **Proibido em**: Liste claramente os contextos onde o uso deste recurso estraga o design, parece clichê ("AI slop") ou prejudica a usabilidade/performance.
- ⚠️ **Erros Comuns de Exagero**: O que evitar ao implementar componentes desta biblioteca (ex: colocar 4 efeitos brilhantes na mesma tela).

## 4. Catálogo Detalhado de Componentes Notáveis (Showstoppers & Primitivas)
Liste de **6 a 12 componentes ou categorias de componentes** específicos que existem neste site/biblioteca, explicando para cada um:
1. **Nome do Componente / Padrão**:
   - *Anatomia Visual*: Como ele se parece e se comporta.
   - *Gatilho de Interação*: Hover, Scroll, Click, Drag, Auto-play.
   - *Onde encaixar na página*: Hero, Navbar, Bento Grid, Social Proof, Pricing, CTA, Dashboard.

## 5. Arquitetura Técnica, Instalação & Receitas de Implementação
- **Dependências & Setup**: Pacotes necessários (`framer-motion`, `lucide-react`, `clsx`, `tailwind-merge`, CLI `npx shadcn@latest add ...`).
- **Física de Movimento e Transições**: Parâmetros de `spring` (`stiffness`, `damping`, `mass`) ou curvas `cubic-bezier` usadas nos componentes.
- **Receita de Código / Estrutura**: Forneça um exemplo estrutural realista (código/classes Tailwind/Motion) de como reproduzir o efeito ou padrão mais emblemático deste recurso.

## 6. Diretrizes para o `DESIGN_BLUEPRINT.md`
Instruções diretas para a IA sobre como declarar e configurar componentes desta referência dentro do documento de arquitetura de um novo projeto.
