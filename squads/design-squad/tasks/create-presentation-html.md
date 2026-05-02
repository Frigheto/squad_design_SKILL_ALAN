---
task: Create Presentation HTML
responsavel: "@visual-designer"
responsavel_type: agent
atomic_layer: task
elicit: true
Entrada: |
  - creative_brief: caminho para creative-brief.md (obrigatório)
  - copy_md: caminho para copy.md (obrigatório)
  - design_md: caminho para DESIGN.md (obrigatório)
  - tokens_json: caminho para tokens.json (obrigatório)
  - num_slides: número de slides (obrigatório)
  - ratio: 16:9 | 4:3 (default: 16:9)
Saida: |
  - presentation_html: apresentação HTML com navegação por teclado/clique
Checklist:
  - "[ ] Montar :root com CSS custom properties"
  - "[ ] Criar estrutura de slides (um div por slide)"
  - "[ ] Implementar navegação por seta/clique"
  - "[ ] Aplicar transições CSS entre slides"
  - "[ ] Estilizar cada slide com tokens de tipografia e cor"
  - "[ ] Garantir ratio correto (16:9 ou 4:3)"
  - "[ ] Salvar presentation.html"
---

# *create-presentation

Gera apresentação HTML com slides navegáveis.

## Uso

```bash
@visual-designer
*create-presentation \
  --brief ./squads/design-squad/outputs/zentgrowth-deck/creative-brief.md \
  --copy ./squads/design-squad/outputs/zentgrowth-deck/copy.md \
  --design ./outputs/design-md/zentgrowth/DESIGN.md \
  --tokens ./outputs/design-md/zentgrowth/tokens.json \
  --slides 8 \
  --ratio 16:9
```
