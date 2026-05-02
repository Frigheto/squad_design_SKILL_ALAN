---
task: Confidence Report
responsavel: "@design-quality-reviewer"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - tokens_json: caminho para tokens.json (obrigatório)
  - extraction_log: caminho para extraction-log.yaml (obrigatório)
Saida: |
  - confidence_breakdown: breakdown de tokens por nível high/medium/low com lista de tokens em cada nível
Checklist:
  - "[ ] Verificar existência dos arquivos"
  - "[ ] Ler comentários de proveniência do tokens.json"
  - "[ ] Classificar tokens por nível: high | medium | low"
  - "[ ] Calcular percentuais por nível"
  - "[ ] Exibir breakdown com tokens listados por nível"
---

# *confidence-report

Exibe breakdown de confiança dos tokens extraídos por nível (high/medium/low).

## Uso

```bash
@design-quality-reviewer
*confidence-report \
  --tokens ./outputs/design-md/exemplo/tokens.json \
  --log ./outputs/design-md/exemplo/extraction-log.yaml
```

## Output esperado

```
Confidence Report — exemplo

  High   (68%)  → 17 tokens  — fonte: CSS vars / @font-face
  Medium (24%)  →  6 tokens  — fonte: declarações CSS diretas
  Low     (8%)  →  2 tokens  — fonte: inferidos

Tokens LOW (requerem revisão manual):
  - colors.neutral.50   # inferred from background lighter variant
  - spacing.xs          # inferred from padding smaller variant
```

## Níveis de confiança

| Nível | Fonte | Confiabilidade |
|-------|-------|---------------|
| `high` | CSS var ou `@font-face` | Alta — direto do código |
| `medium` | Declaração CSS direta | Média — pode variar por contexto |
| `low` | Inferido pelo LLM | Baixa — requer validação manual |
