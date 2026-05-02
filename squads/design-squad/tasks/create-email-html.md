---
task: Create Email HTML
responsavel: "@visual-designer"
responsavel_type: agent
atomic_layer: task
elicit: true
Entrada: |
  - creative_brief: caminho para creative-brief.md (obrigatório)
  - copy_md: caminho para copy.md (obrigatório)
  - design_md: caminho para DESIGN.md (obrigatório)
  - tokens_json: caminho para tokens.json (obrigatório)
  - width: largura do email em px (default: 600)
Saida: |
  - email_html: template de e-mail HTML compatível com principais clientes
Checklist:
  - "[ ] Usar layout em tabela (compatibilidade com Outlook)"
  - "[ ] Inline CSS (sem folha de estilos externa)"
  - "[ ] Largura máxima 600px"
  - "[ ] Aplicar cores via tokens (inline style)"
  - "[ ] Fontes web-safe com fallback (Arial, Georgia)"
  - "[ ] Imagens com alt text"
  - "[ ] CTA como botão com link href"
  - "[ ] Testar estrutura antes de entregar"
  - "[ ] Salvar email.html"
---

# *create-email

Gera template de e-mail HTML compatível com Gmail, Outlook e Apple Mail.

## Uso

```bash
@visual-designer
*create-email \
  --brief ./squads/design-squad/outputs/zentgrowth-email/creative-brief.md \
  --copy ./squads/design-squad/outputs/zentgrowth-email/copy.md \
  --design ./outputs/design-md/zentgrowth/DESIGN.md \
  --tokens ./outputs/design-md/zentgrowth/tokens.json \
  --width 600
```
