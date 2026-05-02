# design-squad

Squad de extração, análise e gestão de sistemas de design a partir de URLs públicas.

Baseado na skill `design-md` — extrai DESIGN.md, tokens.json e preview.html via análise estática de HTML/CSS.

## Agentes

| Agente | Persona | Responsabilidade |
|--------|---------|-----------------|
| `@design-extractor` | Pixel | Pipeline de extração URL → DESIGN.md |
| `@design-token-manager` | Token | Validação e gestão de tokens.json |
| `@design-drift-detector` | Drift | Comparação URL ao vivo vs DESIGN.md local |
| `@design-quality-reviewer` | Qualia | Lint, quality-score e aprovação |

## Uso rápido

```bash
# 1. Extrair sistema de design de uma URL
@design-extractor
*extract --url https://www.exemplo.com/

# 2. Verificar qualidade do DESIGN.md gerado
@design-quality-reviewer
*review --file ./outputs/design-md/exemplo/DESIGN.md

# 3. Detectar drift em relação a spec local
@design-drift-detector
*detect-drift --url https://www.exemplo.com/ --compare ./meu-app/DESIGN.md
```

## Pré-requisitos

- Node.js 18+
- Skill `design-md` instalada (pasta `design-md/` na raiz do projeto)
- Claude Code CLI (`claude`) no PATH
- (Opcional) `OPENROUTER_API_KEY` para provider alternativo

## Gerado por

`@squad-creator *design-squad` — Synkra AIOS
