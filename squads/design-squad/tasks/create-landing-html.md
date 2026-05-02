---
task: Create Landing Page HTML
responsavel: "@visual-designer"
responsavel_type: agent
atomic_layer: task
elicit: true
Entrada: |
  - creative_brief: caminho para creative-brief.md (obrigatório)
  - copy_md: caminho para copy.md (obrigatório)
  - design_md: caminho para DESIGN.md (obrigatório)
  - tokens_json: caminho para tokens.json (obrigatório)
  - sections: lista de seções (ex: hero, features, testimonials, cta, footer)
Saida: |
  - landing_html: arquivo HTML responsivo completo
Checklist:
  - "[ ] Montar :root com CSS custom properties"
  - "[ ] Criar seção hero com headline principal"
  - "[ ] Criar seções conforme brief"
  - "[ ] Implementar grid responsivo (breakpoints do DESIGN.md)"
  - "[ ] Aplicar componentes do DESIGN.md (cards, botões, inputs)"
  - "[ ] Adicionar navegação com nav-header tokens"
  - "[ ] Garantir responsividade mobile-first"
  - "[ ] Salvar landing-page.html"
---

# *create-landing

Gera landing page HTML responsiva completa com base no sistema de design extraído.

## Uso

```bash
@visual-designer
*create-landing \
  --brief ./squads/design-squad/outputs/zentgrowth-landing/creative-brief.md \
  --copy ./squads/design-squad/outputs/zentgrowth-landing/copy.md \
  --design ./outputs/design-md/zentgrowth/DESIGN.md \
  --tokens ./outputs/design-md/zentgrowth/tokens.json \
  --sections "hero,features,cta,footer"
```
