---
task: Detect Design Drift
responsavel: "@design-drift-detector"
responsavel_type: agent
atomic_layer: task
elicit: true
Entrada: |
  - url: URL pública ao vivo (obrigatório)
  - local_design_md: caminho para DESIGN.md local (obrigatório)
Saida: |
  - drift-report.json: detalhes das divergências por token
  - verdict: in-sync | minor-drift | notable-drift | major-drift
Checklist:
  - "[ ] Validar existência do DESIGN.md local"
  - "[ ] Executar skill com --compare"
  - "[ ] Verificar exit code"
  - "[ ] Ler verdict do drift-report.json"
  - "[ ] Exibir resumo de tokens divergentes"
---

# *detect-drift

Compara sistema de design ao vivo com DESIGN.md local e detecta divergências.

## Uso

```bash
@design-drift-detector
*detect-drift --url https://www.exemplo.com/ --compare ./outputs/design-md/exemplo/DESIGN.md
```

## Execução

```bash
node design-md/run.cjs --url {url} --compare {local_design_md}
```

## Verdicts

| Verdict | Significado |
|---------|-------------|
| in-sync | Sem divergências relevantes |
| minor-drift | Pequenas variações em tokens secundários |
| notable-drift | Divergências em tokens principais |
| major-drift | Sistema de design significativamente diferente |
