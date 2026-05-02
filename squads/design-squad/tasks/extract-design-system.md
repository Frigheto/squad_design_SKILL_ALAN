---
task: Extract Design System
responsavel: "@design-extractor"
responsavel_type: agent
atomic_layer: task
elicit: true
Entrada: |
  - url: URL pública a ser analisada (obrigatório)
  - provider: claude-cli | openrouter (default: claude-cli)
  - output_dir: diretório de saída (default: outputs/design-md/{slug}/)
Saida: |
  - DESIGN.md: spec Google-spec com tokens extraídos
  - tokens.json: frontmatter parseado
  - preview.html: preview visual standalone
  - extraction-log.yaml: proveniência e confiança
Checklist:
  - "[ ] Validar URL acessível (HTTP 200, não é SPA pura)"
  - "[ ] Executar skill: node design-md/run.cjs --url {url}"
  - "[ ] Verificar exit code (0 = sucesso)"
  - "[ ] Confirmar DESIGN.md gerado"
  - "[ ] Confirmar tokens.json gerado"
  - "[ ] Confirmar preview.html gerado"
  - "[ ] Exibir quality-score e confidence summary"
---

# *extract

Executa o pipeline completo de extração de sistema de design a partir de uma URL pública.

## Uso

```bash
@design-extractor
*extract --url https://www.exemplo.com/
*extract --url https://brand.empresa.com/ --provider openrouter
```

## Execução

```bash
node design-md/run.cjs --url {url} [--provider {provider}] [--out {output_dir}]
```

## Exit Codes

| Code | Significado |
|------|-------------|
| 0 | Sucesso — DESIGN.md e preview gerados |
| 4 | URL com bot protection / SPA shell — usar --no-content-gate |
| 5 | LLM falhou após retry |
| 6 | OpenRouter key ausente |
