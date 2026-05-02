---
task: Write Caption
responsavel: "@copy-writer"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - creative_brief: caminho para creative-brief.md (obrigatório)
  - channel: instagram | linkedin | twitter (obrigatório)
  - page_copy: caminho para page-copy.json (obrigatório)
Saida: |
  - caption: legenda completa com hashtags para o canal especificado
Checklist:
  - "[ ] Adaptar tom de voz para o canal"
  - "[ ] Escrever abertura (hook nas primeiras 2 linhas)"
  - "[ ] Desenvolver corpo da legenda"
  - "[ ] Adicionar CTA textual"
  - "[ ] Adicionar hashtags relevantes"
---

# *write-caption

Cria legenda otimizada para redes sociais.

## Uso

```bash
@copy-writer
*write-caption \
  --brief ./squads/design-squad/outputs/zentgrowth-post/creative-brief.md \
  --channel instagram \
  --page-copy ./outputs/design-md/zentgrowth/inputs/page-copy.json
```
