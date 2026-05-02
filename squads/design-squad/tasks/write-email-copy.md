---
task: Write Email Copy
responsavel: "@copy-writer"
responsavel_type: agent
atomic_layer: task
elicit: true
Entrada: |
  - creative_brief: caminho para creative-brief.md (obrigatório)
  - page_copy: caminho para page-copy.json (obrigatório)
  - email_type: newsletter | promotional | onboarding | transactional
Saida: |
  - email_copy: arquivo com subject line, preheader, headline, body e CTA
Checklist:
  - "[ ] Definir subject line (máx. 50 caracteres)"
  - "[ ] Definir preheader (máx. 90 caracteres)"
  - "[ ] Escrever headline do email"
  - "[ ] Escrever body em blocos curtos (máx. 3 parágrafos)"
  - "[ ] Escrever CTA principal"
  - "[ ] Verificar tom de voz contra o site original"
---

# *write-email

Cria copy completa para template de e-mail.

## Uso

```bash
@copy-writer
*write-email \
  --brief ./squads/design-squad/outputs/zentgrowth-email/creative-brief.md \
  --page-copy ./outputs/design-md/zentgrowth/inputs/page-copy.json \
  --type promotional
```

## Output — email-copy.md

```markdown
# Email Copy

## Subject Line
{subject — máx. 50 chars}

## Preheader
{preheader — máx. 90 chars}

## Headline
{headline principal}

## Body
{parágrafo 1}
{parágrafo 2}
{parágrafo 3}

## CTA
{texto do botão}
```
