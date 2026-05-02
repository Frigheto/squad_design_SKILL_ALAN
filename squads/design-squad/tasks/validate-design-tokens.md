---
task: Validate Design Tokens
responsavel: "@design-token-manager"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - tokens_json_path: caminho para tokens.json (obrigatório)
Saida: |
  - validation_report: relatório com tokens inválidos ou ausentes
Checklist:
  - "[ ] Verificar existência do tokens.json"
  - "[ ] Parsear frontmatter YAML"
  - "[ ] Validar campos obrigatórios (colors, typography, spacing)"
  - "[ ] Verificar níveis de confiança (high/medium/low)"
  - "[ ] Gerar validation-report.json"
---

# *validate-tokens

Valida tokens.json extraído pela skill design-md.

## Uso

```bash
@design-token-manager
*validate-tokens --file ./outputs/design-md/exemplo/tokens.json
```
