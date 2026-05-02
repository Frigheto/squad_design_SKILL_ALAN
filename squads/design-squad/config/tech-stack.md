# Tech Stack — design-squad

## Runtime
- Node.js 18+
- skill `design-md` (local, `design-md/run.cjs`)

## Providers LLM
- `claude-cli` (padrão) — `claude -p`, modelo Opus 4.7
- `openrouter` — Haiku 4.5, requer `OPENROUTER_API_KEY`

## Dependências Node
- `axios` — HTTP fetch
- `cheerio` — HTML parsing
- `turndown` — HTML → Markdown

## Ferramentas externas
- `@google/design.md@0.1.0` — lint e validação de spec

## Formatos de output
- DESIGN.md (Google-spec)
- tokens.json (DTCG compatible)
- CSS custom properties
