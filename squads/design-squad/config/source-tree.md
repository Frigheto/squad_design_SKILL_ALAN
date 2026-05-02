# Source Tree — design-squad

## Estrutura do squad

```
squads/design-squad/
├── squad.yaml                        # Manifest do squad
├── README.md                         # Documentação
├── config/
│   ├── coding-standards.md
│   ├── tech-stack.md
│   └── source-tree.md
├── agents/
│   ├── design-extractor.md           # Pipeline de extração (Pixel)
│   ├── design-token-manager.md       # Gestão de tokens (Token)
│   ├── design-drift-detector.md      # Detecção de drift (Drift)
│   └── design-quality-reviewer.md    # Validação de qualidade (Qualia)
└── tasks/
    ├── extract-design-system.md
    ├── reextract-design-system.md
    ├── list-extraction-outputs.md
    ├── validate-design-tokens.md
    ├── export-design-tokens.md
    ├── diff-design-tokens.md
    ├── merge-design-tokens.md
    ├── detect-design-drift.md
    ├── drift-report-summary.md
    ├── drift-history.md
    ├── lint-design-md.md
    ├── quality-score-report.md
    ├── confidence-report.md
    └── approve-design-spec.md

## Skill de origem

```
design-md/                            # Skill base (não modificar)
├── run.cjs                           # Entrypoint principal
├── lib/                              # Pipeline interno
├── data/                             # Prompts e dados
└── SKILL.md                          # Documentação
```

## Outputs gerados

```
outputs/design-md/{slug}/
├── DESIGN.md
├── tokens.json
├── preview.html
├── extraction-log.yaml
├── lint-report.json
├── quality-score.json
├── drift-report.json (quando --compare)
└── history/
```
