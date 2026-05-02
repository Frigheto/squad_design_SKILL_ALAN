---
task: Drift Report Summary
responsavel: "@design-drift-detector"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - drift_report_path: caminho para drift-report.json (obrigatório)
Saida: |
  - readable_report: relatório legível com tokens divergentes agrupados por categoria
Checklist:
  - "[ ] Verificar existência do drift-report.json"
  - "[ ] Ler verdict geral"
  - "[ ] Agrupar divergências por categoria (colors, typography, spacing...)"
  - "[ ] Exibir tabela com token, valor esperado e valor atual"
  - "[ ] Exibir recomendação baseada no verdict"
---

# *drift-report

Gera relatório legível a partir de um drift-report.json existente.

## Uso

```bash
@design-drift-detector
*drift-report --file ./outputs/design-md/exemplo/drift-report.json
```

## Output esperado

```
Verdict: notable-drift

Divergências por categoria:
  Colors (3)
    --color-primary    esperado: #0052CC   atual: #0066FF
    --color-bg         esperado: #FFFFFF   atual: #F8F9FA
    --color-accent     esperado: —         atual: #FF5630  [ADDED]

  Typography (1)
    --font-body-size   esperado: 16px      atual: 14px

Recomendação: Atualizar DESIGN.md local ou alinhar implementação com a spec.
```
