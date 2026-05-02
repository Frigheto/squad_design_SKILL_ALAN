---
task: Adapt Copy Format
responsavel: "@copy-writer"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - source_copy: caminho para copy.md existente (obrigatório)
  - target_format: formato de destino (banner | post | story | email | landing)
  - target_channel: canal de destino (obrigatório)
Saida: |
  - adapted_copy: copy adaptada para o novo formato
Checklist:
  - "[ ] Ler copy original"
  - "[ ] Identificar restrições de espaço do formato destino"
  - "[ ] Adaptar headline (comprimir ou expandir)"
  - "[ ] Adaptar body (resumir ou detalhar)"
  - "[ ] Adaptar CTA para o canal"
---

# *adapt-copy

Adapta copy existente para outro formato ou canal sem perder consistência de marca.

## Uso

```bash
@copy-writer
*adapt-copy \
  --source ./squads/design-squad/outputs/zentgrowth-banner/copy.md \
  --target-format story \
  --target-channel instagram
```
