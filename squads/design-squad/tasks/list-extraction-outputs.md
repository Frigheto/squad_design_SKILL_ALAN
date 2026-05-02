---
task: List Extraction Outputs
responsavel: "@design-extractor"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - slug: filtro por slug específico (opcional)
  - output_dir: diretório raiz dos outputs (default: outputs/design-md/)
Saida: |
  - outputs_list: lista de extrações disponíveis
  - quality_scores: nota de cada extração
  - dates: data de cada extração
Checklist:
  - "[ ] Escanear diretório outputs/design-md/"
  - "[ ] Ler quality-score.json de cada slug"
  - "[ ] Ler extraction-log.yaml para data e modelo usado"
  - "[ ] Exibir tabela com slug, quality-score, data, provider"
---

# *list-outputs

Lista todos os sistemas de design extraídos disponíveis localmente.

## Uso

```bash
@design-extractor
*list-outputs
*list-outputs --slug anthropic
```

## Output esperado

```
Slug              Quality   Data              Provider
────────────────  ───────   ───────────────   ──────────
anthropic         A         2026-05-01        claude-cli
linear-app        B+        2026-04-28        openrouter
shopify           A-        2026-04-20        claude-cli
```
