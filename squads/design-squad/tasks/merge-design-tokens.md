---
task: Merge Design Tokens
responsavel: "@design-token-manager"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - tokens_base: tokens.json base (obrigatório)
  - tokens_override: tokens.json com valores que sobrescrevem (obrigatório)
  - strategy: merge | override (default: merge)
  - output_path: onde salvar tokens-merged.json (opcional)
Saida: |
  - tokens_merged: arquivo tokens.json resultante da mesclagem
  - conflict_log: lista de conflitos resolvidos com estratégia aplicada
Checklist:
  - "[ ] Verificar existência dos dois arquivos"
  - "[ ] Parsear ambos os tokens.json"
  - "[ ] Aplicar estratégia de mesclagem"
  - "[ ] Registrar conflitos resolvidos"
  - "[ ] Salvar tokens-merged.json"
  - "[ ] Exibir resumo de conflitos"
---

# *merge-tokens

Mescla dois arquivos tokens.json com estratégia configurável.

## Uso

```bash
@design-token-manager
*merge-tokens --base ./tokens-base.json --override ./tokens-brand.json --strategy merge
```

## Estratégias

| Estratégia | Comportamento |
|------------|--------------|
| `merge` | Override adiciona/sobrescreve tokens; base mantém os não conflitantes |
| `override` | Override substitui completamente o base |
