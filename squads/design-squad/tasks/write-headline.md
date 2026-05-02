---
task: Write Headline
responsavel: "@copy-writer"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - page_copy: caminho para page-copy.json (obrigatório)
  - objective: objetivo do criativo (obrigatório)
  - max_words: limite de palavras (default: 8)
Saida: |
  - headlines: lista de 3 variações de headline
Checklist:
  - "[ ] Analisar tom de voz do page-copy.json"
  - "[ ] Identificar palavras-chave do site"
  - "[ ] Gerar 3 variações de headline dentro do limite"
  - "[ ] Verificar alinhamento com objetivo do criativo"
---

# *write-headline

Gera variações de headline para um criativo.

## Uso

```bash
@copy-writer
*write-headline \
  --page-copy ./outputs/design-md/zentgrowth/inputs/page-copy.json \
  --objective "converter visitantes em leads" \
  --max-words 8
```
