---
task: Approve Design Spec
responsavel: "@design-quality-reviewer"
responsavel_type: agent
atomic_layer: task
elicit: true
Entrada: |
  - design_md: caminho para DESIGN.md (obrigatório)
  - quality_score: caminho para quality-score.json (obrigatório)
  - lint_report: caminho para lint-report.json (obrigatório)
Saida: |
  - decision: APPROVED | NEEDS_REVISION
  - justification: explicação da decisão com critérios atendidos/não-atendidos
Checklist:
  - "[ ] Ler quality-score.json (nota geral >= B para APPROVED)"
  - "[ ] Ler lint-report.json (zero erros CRITICAL para APPROVED)"
  - "[ ] Verificar confidence_high >= 60% nos tokens"
  - "[ ] Emitir decisão com justificativa documentada"
---

# *approve

Emite decisão de aprovação ou revisão para um DESIGN.md.

## Uso

```bash
@design-quality-reviewer
*approve \
  --design ./outputs/design-md/exemplo/DESIGN.md \
  --quality ./outputs/design-md/exemplo/quality-score.json \
  --lint ./outputs/design-md/exemplo/lint-report.json
```

## Critérios de Aprovação

| Critério | Threshold |
|----------|-----------|
| Quality score | >= B |
| Lint errors críticos | 0 |
| Confidence high tokens | >= 60% |
