---
task: Review Creative Output
responsavel: "@creative-director"
responsavel_type: agent
atomic_layer: task
elicit: false
quality_standard: squads/design-squad/config/creative-quality-standard.md
Entrada: |
  - creative_html: caminho para o HTML gerado pelo @visual-designer (obrigatório)
  - creative_brief: caminho para o brief original (obrigatório)
  - design_md: caminho para DESIGN.md (obrigatório)
Saida: |
  - review_result: APPROVED | NEEDS_REVISION | BLOCKED
  - quality_score: número de 0-100
  - feedback: lista detalhada de ajustes necessários se NEEDS_REVISION ou BLOCKED
Checklist:
  - "[ ] Ler creative-quality-standard.md — carregar critérios de scoring"
  - "[ ] Verificar LAYER 1: fundo dark + mesh gradient (≥2 radial-gradients) + texture overlay"
  - "[ ] Verificar LAYER 2: ≥2 orbs com blur + accent element (line, border, dot)"
  - "[ ] Verificar LAYER 3: headline com gradient text + ≥72px + letter-spacing negativo"
  - "[ ] Verificar LAYER 4: ≥1 proof element com glassmorphism (ou animação para stories)"
  - "[ ] Verificar LAYER 5: CTA com gradiente + box-shadow glow (≥30px spread) + ::after shine"
  - "[ ] Verificar LAYER 6: logo presente, bordas rgba (não sólidas), handle no footer"
  - "[ ] Verificar tokens: :root presente com tokens extraídos do DESIGN.md"
  - "[ ] Verificar copy: headline, subheadline e CTA batem com copy.md"
  - "[ ] Verificar dimensões: canvas com width/height corretos e overflow:hidden"
  - "[ ] Calcular score total (ver tabela abaixo)"
  - "[ ] Emitir decisão baseada no score"
---

# *review-creative

Revisa o criativo gerado contra o brief, o DESIGN.md original e o **creative-quality-standard.md**.
Esta é a única gate entre o @visual-designer e a entrega final.

## Uso

```bash
@creative-director
*review-creative \
  --html ./squads/design-squad/outputs/zentgrowth-banner/banner.html \
  --brief ./squads/design-squad/outputs/zentgrowth-banner/creative-brief.md \
  --design ./outputs/design-md/zentgrowth/DESIGN.md
```

## Scoring Matrix (100 pontos)

| Layer | Critério | Pts máx | PASS quando |
|-------|----------|---------|------------|
| **Layer 1** Background Rich | mesh gradient (≥2 radial-gradients) + texture overlay (::before) | 20 | Ambos presentes |
| **Layer 2** Depth & Atmosphere | ≥2 orbs `filter:blur` + 1 accent element | 15 | Todos presentes |
| **Layer 3** Typography Premium | gradient text + ≥72px + letter-spacing negativo + font-feature-settings | 20 | Todos os 4 itens |
| **Layer 4** Proof Element | ≥1 elemento glassmorphism (stat, mockup, pill, chart, testimonial, animação para story) | 25 | Pelo menos 1 |
| **Layer 5** CTA Premium | gradient background + box-shadow glow ≥30px + ::after inner shine | 10 | Todos os 3 itens |
| **Layer 6** Polish & Finish | logo + bordas rgba + handle + z-index em ≥3 níveis | 10 | Todos os 4 itens |

## Tabela de decisão

| Score | Decisão | Ação |
|-------|---------|------|
| 90-100 | ✅ **APPROVED** — Premium | Entregável sem ressalvas |
| 75-89 | ⚠️ **APPROVED** — Acceptable | Entregável com nota de melhorias sugeridas |
| 60-74 | 🔄 **NEEDS_REVISION** | Retornar ao @visual-designer com lista de layers faltantes |
| < 60 | ❌ **BLOCKED** | Não sai do fluxo — revisão completa necessária |

## Critérios de brand fidelity (adicionais, não pontuados)

| Critério | Verificação |
|----------|------------|
| Paleta de cores | Cores usadas existem nos tokens do DESIGN.md |
| Tipografia | Família e pesos batem com DESIGN.md |
| Copy | Headline/CTA batem com copy.md aprovado |
| Do's & Don'ts | Restrições do DESIGN.md respeitadas |

## Output do review (formato obrigatório)

```markdown
# Review — {nome do criativo}

**Score:** {X}/100
**Decisão:** {APPROVED | NEEDS_REVISION | BLOCKED}

## Layers verificados

| Layer | Score | Status |
|-------|-------|--------|
| Background Rich | {X}/20 | ✅/❌ |
| Depth & Atmosphere | {X}/15 | ✅/❌ |
| Typography Premium | {X}/20 | ✅/❌ |
| Proof Element | {X}/25 | ✅/❌ |
| CTA Premium | {X}/10 | ✅/❌ |
| Polish & Finish | {X}/10 | ✅/❌ |

## Brand Fidelity
- Cores: {OK | DIVERGENTE — detalhar}
- Tipografia: {OK | DIVERGENTE — detalhar}
- Copy: {OK | DIVERGENTE — detalhar}

## Feedback para revisão (se NEEDS_REVISION)
- {item específico a corrigir}
- {item específico a corrigir}
```
