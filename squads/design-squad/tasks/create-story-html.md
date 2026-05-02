---
task: Create Story HTML
responsavel: "@visual-designer"
responsavel_type: agent
atomic_layer: task
elicit: true
quality_standard: squads/design-squad/config/creative-quality-standard.md
Entrada: |
  - creative_brief: caminho para creative-brief.md (obrigatório)
  - copy_md: caminho para copy.md (obrigatório)
  - design_md: caminho para DESIGN.md (obrigatório)
  - tokens_json: caminho para tokens.json (obrigatório)
  - animated: true | false (default: true — usa motion tokens extraídos)
Saida: |
  - story_html: arquivo HTML standalone 1080x1920 com animações CSS (score mínimo 75/100)
Checklist:
  - "[ ] Ler creative-quality-standard.md — todos os 6 layers obrigatórios para story"
  - "[ ] Montar :root completo com todos os tokens extraídos"
  - "[ ] Definir dimensões 1080x1920px no body e .canvas"
  - "[ ] LAYER 1 — Fundo dark + mesh gradient (3-4 radial-gradients) + texture ::before"
  - "[ ] LAYER 2 — ≥2 orbs de luz + accent line no topo ou lateral"
  - "[ ] LAYER 3 — Headline com gradient text + ≥80px + letter-spacing negativo"
  - "[ ] LAYER 4 — Proof element OU animação CSS com @keyframes (substituto aceito para story)"
  - "[ ] LAYER 5 — CTA com gradiente + glow + inner shine"
  - "[ ] LAYER 6 — Logo, handle, safe zone respeitada (elemento clicável acima de 250px do fundo)"
  - "[ ] Se animated=true: aplicar @keyframes em ≥3 elementos (fade-in, slide-up, float)"
  - "[ ] Calcular score — mínimo 75/100"
  - "[ ] Salvar story.html"
---

# *create-story

Gera story vertical HTML 1080x1920 com animações CSS baseadas nos motion tokens extraídos.
**Complexidade mínima obrigatória:** 6 layers conforme `creative-quality-standard.md`.
Para stories: animações @keyframes são aceitas como substituto de Proof Element no Layer 4.

## Uso

```bash
@visual-designer
*create-story \
  --brief ./squads/design-squad/outputs/zentgrowth-story/creative-brief.md \
  --copy ./squads/design-squad/outputs/zentgrowth-story/copy.md \
  --design ./outputs/design-md/zentgrowth/DESIGN.md \
  --tokens ./outputs/design-md/zentgrowth/tokens.json \
  --animated true
```

## Animações obrigatórias (animated=true)

```css
/* Mínimo 3 keyframes aplicados a elementos distintos */
@keyframes fadeInUp {
  from { opacity:0; transform:translateY(30px); }
  to   { opacity:1; transform:translateY(0); }
}
@keyframes floatOrb {
  0%,100% { transform:translateY(0) scale(1); }
  50%     { transform:translateY(-20px) scale(1.05); }
}
@keyframes glowPulse {
  0%,100% { box-shadow: 0 0 30px rgba({r1},0.4); }
  50%     { box-shadow: 0 0 60px rgba({r1},0.8), 0 0 100px rgba({r1},0.3); }
}

/* Aplicação em sequência (staggered) */
.headline    { animation: fadeInUp 0.8s ease 0.2s both; }
.subheadline { animation: fadeInUp 0.8s ease 0.5s both; }
.proof-card  { animation: fadeInUp 0.8s ease 0.8s both; }
.cta-button  { animation: fadeInUp 0.8s ease 1.1s both, glowPulse 3s ease 2s infinite; }
.orb-1       { animation: floatOrb 8s ease infinite; }
```

## Safe zone para stories

```
┌──────────────────────┐ ← topo 1920px
│   zona de interface  │ ← 0-100px: reservada para barra de status
├──────────────────────┤
│      logo / badge    │ ← 100-200px
│                      │
│      headline        │ ← 200-600px: zona principal
│      subheadline     │
│                      │
│    proof element     │ ← 600-1200px: zona de conteúdo
│    ou animação       │
│                      │
│      CTA button      │ ← 1200-1650px: zona de ação
│                      │
├──────────────────────┤
│  handle / swipe up   │ ← 1650-1920px: zona segura de rodapé
└──────────────────────┘
```

## Onde salvar

```
squads/design-squad/outputs/{slug}-story/story.html
```
