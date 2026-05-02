---
task: Export Design Tokens
responsavel: "@design-token-manager"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - tokens_json_path: caminho para tokens.json (obrigatório)
  - format: dtcg | css-vars | json (default: css-vars)
  - output_path: onde salvar o arquivo exportado (opcional)
Saida: |
  - exported_tokens: arquivo de tokens no formato solicitado
Checklist:
  - "[ ] Verificar existência do tokens.json"
  - "[ ] Parsear frontmatter YAML do tokens.json"
  - "[ ] Converter para formato solicitado"
  - "[ ] Salvar arquivo exportado"
  - "[ ] Exibir caminho do arquivo gerado"
---

# *export-tokens

Exporta tokens.json para diferentes formatos de consumo.

## Uso

```bash
@design-token-manager
*export-tokens --file ./outputs/design-md/exemplo/tokens.json --format css-vars
*export-tokens --file ./tokens.json --format dtcg --out ./src/tokens/
```

## Formatos disponíveis

| Formato | Extensão | Uso |
|---------|----------|-----|
| `css-vars` | `.css` | Variáveis CSS (`--color-primary: #...`) |
| `dtcg` | `.json` | Design Token Community Group spec |
| `json` | `.json` | JSON plano, sem metadados de confiança |
