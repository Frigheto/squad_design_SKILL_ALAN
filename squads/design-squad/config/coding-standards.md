# Coding Standards — design-squad

## Geral
- Extends: AIOS core coding standards
- Linguagem: JavaScript (Node.js 18+)
- Formato de arquivos de config: YAML
- Formato de tokens: JSON (DTCG compatible)

## Nomenclatura
- Slugs de URL: kebab-case, subdomain-aware
- Arquivos de output: snake_case (ex: `quality-score.json`)
- Tasks: kebab-case (ex: `extract-design-system.md`)

## Outputs
- Sempre salvar em `outputs/design-md/{slug}/`
- Manter `history/` com runs anteriores
- Nunca sobrescrever se quality-score for inferior ao anterior

## Tratamento de erros
- Verificar exit codes da skill antes de processar outputs
- Não processar DESIGN.md com lint errors CRITICAL
- Logar proveniência em `extraction-log.yaml`
