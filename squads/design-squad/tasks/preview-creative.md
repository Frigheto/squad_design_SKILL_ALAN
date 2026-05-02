---
task: Preview Creative
responsavel: "@visual-designer"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - html_path: caminho para o arquivo HTML a visualizar (obrigatório)
Saida: |
  - browser_preview: criativo aberto no browser padrão do sistema
Checklist:
  - "[ ] Verificar existência do arquivo HTML"
  - "[ ] Abrir no browser padrão"
  - "[ ] Confirmar abertura bem-sucedida"
---

# *preview

Abre o criativo HTML no browser para revisão visual.

## Uso

```bash
@visual-designer
*preview --html ./squads/design-squad/outputs/zentgrowth-banner/banner-1200x628.html
```

## Execução

```powershell
Start-Process "caminho/para/arquivo.html"
```
