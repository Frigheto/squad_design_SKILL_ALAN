---
task: Plan Creative Campaign
responsavel: "@creative-director"
responsavel_type: agent
atomic_layer: task
elicit: true
Entrada: |
  - design_md: caminho para DESIGN.md aprovado (obrigatório)
  - campaign_objective: objetivo geral da campanha
  - channels: lista de canais (ex: instagram, web, email)
  - num_pieces: número de peças a criar
Saida: |
  - campaign_plan: arquivo campaign-plan.md com todos os briefs da campanha
Checklist:
  - "[ ] Definir objetivo geral da campanha"
  - "[ ] Listar canais e formatos necessários"
  - "[ ] Criar brief individual para cada peça"
  - "[ ] Definir sequência de produção (copy → visual)"
  - "[ ] Salvar campaign-plan.md"
---

# *plan-campaign

Planeja uma série de criativos para uma campanha completa.

## Uso

```bash
@creative-director
*plan-campaign --objective "lançamento de produto" --channels "instagram,web,email" --pieces 6
```

## Output

Gera um `campaign-plan.md` com briefs individuais para cada peça da campanha, priorizados por canal e sequência de produção.
