---
task: Create Card HTML
responsavel: "@visual-designer"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - design_md: caminho para DESIGN.md (obrigatório)
  - tokens_json: caminho para tokens.json (obrigatório)
  - card_type: feature | testimonial | pricing | product | profile
  - copy_md: caminho para copy.md (opcional)
Saida: |
  - card_html: componente card HTML reutilizável
Checklist:
  - "[ ] Ler spec do card no DESIGN.md (bg, border, radius, shadow, padding)"
  - "[ ] Montar HTML do card com tokens como CSS vars"
  - "[ ] Aplicar variante conforme card_type"
  - "[ ] Garantir responsividade do componente"
  - "[ ] Salvar card-{type}.html"
---

# *create-card

Gera componente card HTML baseado nos tokens extraídos do DESIGN.md.

## Uso

```bash
@visual-designer
*create-card \
  --design ./outputs/design-md/zentgrowth/DESIGN.md \
  --tokens ./outputs/design-md/zentgrowth/tokens.json \
  --type feature
```
