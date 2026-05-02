---
task: Re-extract Design System
responsavel: "@design-extractor"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - url: URL pública a ser re-extraída (obrigatório)
  - provider: claude-cli | openrouter (default: claude-cli)
Saida: |
  - DESIGN.md: spec atualizada, ignorando cache anterior
  - tokens.json: tokens frescos
  - preview.html: preview atualizado
Checklist:
  - "[ ] Validar URL"
  - "[ ] Executar skill com --no-reuse para forçar extração fresca"
  - "[ ] Verificar exit code (0 = sucesso)"
  - "[ ] Confirmar que run anterior foi movido para history/"
  - "[ ] Exibir quality-score do novo run vs anterior"
---

# *reextract

Força re-extração completa de uma URL ignorando todas as fases em cache.

## Uso

```bash
@design-extractor
*reextract --url https://www.exemplo.com/
```

## Execução

```bash
node design-md/run.cjs --url {url} --no-reuse
```

## Quando usar

- Site teve atualização visual recente
- Run anterior teve quality-score baixo
- Cache corrompido ou desatualizado (> 24h)
