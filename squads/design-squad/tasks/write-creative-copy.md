---
task: Write Creative Copy
responsavel: "@copy-writer"
responsavel_type: agent
atomic_layer: task
elicit: true
Entrada: |
  - creative_brief: caminho para creative-brief.md (obrigatório)
  - page_copy: caminho para inputs/page-copy.json (obrigatório)
  - design_md: caminho para DESIGN.md (obrigatório)
Saida: |
  - copy_md: arquivo copy.md com todos os textos do criativo
Checklist:
  - "[ ] Ler page-copy.json — absorver tom de voz e vocabulário do site"
  - "[ ] Ler creative-brief.md — entender objetivo e hierarquia de conteúdo"
  - "[ ] Escrever headline principal (máx. 8 palavras)"
  - "[ ] Escrever subheadline (máx. 15 palavras)"
  - "[ ] Escrever body copy (conforme espaço definido no brief)"
  - "[ ] Escrever CTA (máx. 4 palavras, verbo de ação)"
  - "[ ] Verificar tom de voz contra o site original"
  - "[ ] Salvar copy.md"
---

# *write-copy

Cria copy completa para um criativo a partir do brief e do tom de voz extraído do site.

## Uso

```bash
@copy-writer
*write-copy \
  --brief ./squads/design-squad/outputs/zentgrowth-banner/creative-brief.md \
  --page-copy ./outputs/design-md/zentgrowth/inputs/page-copy.json \
  --design ./outputs/design-md/zentgrowth/DESIGN.md
```

## Output — copy.md

```markdown
# Copy — {tipo} {canal}

## Headline
{headline principal}

## Subheadline
{subheadline}

## Body
{body copy}

## CTA
{texto do botão}

## Alternativas
- Headline B: {variação}
- CTA B: {variação}
```
