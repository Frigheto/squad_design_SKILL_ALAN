---
task: Quality Score Report
responsavel: "@design-quality-reviewer"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - design_md_path: caminho para DESIGN.md (obrigatório)
  - extraction_log: caminho para extraction-log.yaml (opcional, enriquece o relatório)
Saida: |
  - quality_score: nota geral A-F
  - visual_summary: breakdown por categoria com notas individuais
Checklist:
  - "[ ] Verificar existência do DESIGN.md"
  - "[ ] Ler quality-score.json se já existir"
  - "[ ] Se não existir, calcular com base em: seções presentes, tokens completos, proveniência"
  - "[ ] Exibir nota geral e breakdown por categoria"
---

# *quality-score

Exibe o quality-score de um DESIGN.md em 7 categorias.

## Uso

```bash
@design-quality-reviewer
*quality-score --file ./outputs/design-md/exemplo/DESIGN.md
```

## Categorias avaliadas

| Categoria | Peso | Critério |
|-----------|------|---------|
| Completude | 20% | Todas as seções obrigatórias presentes |
| Tokens de cor | 20% | Paleta completa com variantes |
| Tipografia | 15% | Família, tamanho, peso, line-height |
| Espaçamento | 15% | Escala de spacing e radius |
| Proveniência | 15% | % de tokens com confiança `high` |
| Lint | 10% | Zero erros críticos no @google/design.md |
| Consistência | 5% | Tokens referenciados vs declarados |
