---
task: Diff Design Tokens
responsavel: "@design-token-manager"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - tokens_a: caminho para tokens.json base (obrigatório)
  - tokens_b: caminho para tokens.json comparado (obrigatório)
Saida: |
  - diff_report: tokens adicionados, removidos e alterados entre A e B
Checklist:
  - "[ ] Verificar existência dos dois arquivos"
  - "[ ] Parsear ambos os tokens.json"
  - "[ ] Comparar chave a chave"
  - "[ ] Classificar diferenças: added | removed | changed"
  - "[ ] Exibir diff com valores antigos e novos"
---

# *diff-tokens

Compara dois arquivos tokens.json e exibe as diferenças.

## Uso

```bash
@design-token-manager
*diff-tokens --a ./outputs/design-md/site-v1/tokens.json --b ./outputs/design-md/site-v2/tokens.json
```

## Output esperado

```
Token                  Status     Antes           Depois
─────────────────────  ─────────  ──────────────  ──────────────
colors.primary         CHANGED    #0052CC         #0066FF
colors.accent          ADDED      —               #FF5630
typography.body.size   REMOVED    16px            —
```
