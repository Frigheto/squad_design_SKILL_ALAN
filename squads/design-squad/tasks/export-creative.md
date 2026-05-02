---
task: Export Creative
responsavel: "@visual-designer"
responsavel_type: agent
atomic_layer: task
elicit: false
Entrada: |
  - html_path: caminho para o arquivo HTML (obrigatório)
  - format: png | pdf | jpg (default: png)
  - scale: fator de escala para resolução (default: 2 — retina)
  - output_path: onde salvar o arquivo exportado (opcional)
Saida: |
  - exported_file: imagem ou PDF do criativo
Checklist:
  - "[ ] Verificar existência do HTML"
  - "[ ] Capturar screenshot via Playwright ou equivalente"
  - "[ ] Aplicar fator de escala para resolução adequada"
  - "[ ] Salvar no formato solicitado"
  - "[ ] Confirmar dimensões do arquivo exportado"
---

# *export

Exporta criativo HTML para PNG, JPG ou PDF.

## Uso

```bash
@visual-designer
*export \
  --html ./squads/design-squad/outputs/zentgrowth-banner/banner-1200x628.html \
  --format png \
  --scale 2
```

## Método de exportação

```javascript
// Via Playwright (recomendado)
const { chromium } = require('playwright');
const browser = await chromium.launch();
const page = await browser.newPage();
await page.setViewportSize({ width: W, height: H });
await page.goto('file://' + path.resolve(htmlPath));
await page.screenshot({ path: outputPath, fullPage: false });
await browser.close();
```

## Dependência opcional

```bash
npm install playwright
npx playwright install chromium
```
