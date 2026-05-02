---
task: Drift History
responsavel: "@design-drift-detector"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - slug: identificador da URL (ex: anthropic, linear-app) (obrigatório)
  - date_range: filtro de período (ex: 2026-04, 2026-04/2026-05) (opcional)
  - output_dir: diretório raiz dos outputs (default: outputs/design-md/)
Saida: |
  - drift_history: lista cronológica de verdicts e principais divergências por run
Checklist:
  - "[ ] Localizar diretório outputs/design-md/{slug}/history/"
  - "[ ] Listar runs com drift-report.json"
  - "[ ] Filtrar por date_range se fornecido"
  - "[ ] Ordenar cronologicamente"
  - "[ ] Exibir tabela com data, verdict e quantidade de divergências"
---

# *drift-history

Exibe o histórico de drifts detectados para um slug ao longo do tempo.

## Uso

```bash
@design-drift-detector
*drift-history --slug anthropic
*drift-history --slug linear-app --date-range 2026-04/2026-05
```

## Output esperado

```
Histórico de drift — anthropic

Data              Verdict          Divergências
───────────────   ──────────────   ────────────
2026-05-01        in-sync          0
2026-04-15        minor-drift      2
2026-04-01        notable-drift    5
2026-03-10        major-drift      12
```
