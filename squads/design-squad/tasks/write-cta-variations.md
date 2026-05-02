---
task: Write CTA Variations
responsavel: "@copy-writer"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - objective: objetivo do criativo (obrigatório)
  - page_copy: caminho para page-copy.json (obrigatório)
  - num_variations: número de variações (default: 5)
Saida: |
  - cta_list: lista de variações de CTA ordenadas por força
Checklist:
  - "[ ] Identificar verbos de ação usados no site"
  - "[ ] Gerar variações com urgência, benefício e ação"
  - "[ ] Ordenar por força de conversão estimada"
---

# *write-cta

Gera variações de CTA (Call to Action) para um criativo.

## Uso

```bash
@copy-writer
*write-cta \
  --objective "gerar leads" \
  --page-copy ./outputs/design-md/zentgrowth/inputs/page-copy.json
```

## Output esperado

```
1. Comece Agora          ← alta urgência
2. Quero Crescer         ← orientado a benefício
3. Fale com a Equipe     ← baixo risco
4. Ver Como Funciona     ← educacional
5. Acesse Grátis         ← remoção de barreira
```
