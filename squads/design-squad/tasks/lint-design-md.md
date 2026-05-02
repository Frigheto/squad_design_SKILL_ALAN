---
task: Lint Design MD
responsavel: "@design-quality-reviewer"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - design_md_path: caminho para o DESIGN.md a validar (obrigatório)
Saida: |
  - lint-report.json: erros e warnings @google/design.md spec
Checklist:
  - "[ ] Verificar existência do DESIGN.md"
  - "[ ] Executar npx @google/design.md lint"
  - "[ ] Salvar lint-report.json"
  - "[ ] Exibir contagem de erros e warnings"
---

# *lint

Executa lint @google/design.md em um DESIGN.md e gera relatório.

## Uso

```bash
@design-quality-reviewer
*lint --file ./outputs/design-md/exemplo/DESIGN.md
```

## Execução

```bash
npx --yes @google/design.md@0.1.0 lint {design_md_path}
```
