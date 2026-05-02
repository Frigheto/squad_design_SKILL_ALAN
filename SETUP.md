# Setup — Como usar após clonar

## Pré-requisitos

- Node.js >= 18 instalado
- Conta no OpenRouter com API Key: https://openrouter.ai/keys
- Claude Code (CLI) instalado e autenticado

---

## Passos obrigatórios após clonar

### 1. Instalar dependências da skill design-md

```bash
cd design-md
npm install
cd ..
```

### 2. Criar o arquivo .env com sua API Key

```bash
# Copiar o template
cp .env.example .env
```

Abrir o `.env` e preencher:
```
OPENROUTER_API_KEY=sk-or-v1-SUA_CHAVE_AQUI
```

> A chave pode ser obtida em: https://openrouter.ai/keys
> O modelo padrão usado é `google/gemini-2.5-flash-preview` via OpenRouter.

---

## Como usar o fluxo completo

### Passo 1 — Extrair o design system de um site

```bash
# Carregar a API key no terminal (Windows PowerShell)
$line = Get-Content ".env" | Where-Object { $_ -match "^OPENROUTER_API_KEY=.+" }
$env:OPENROUTER_API_KEY = $line.Split("=", 2)[1]

# Rodar a extração
node design-md/run.cjs --url https://seusite.com --provider openrouter --max-tokens 32768
```

O output é gerado em: `outputs/design-md/{slug}/`
- `DESIGN.md` — sistema de design completo
- `tokens.json` — tokens CSS estruturados
- `style-fingerprint.json` — arquétipo visual detectado

### Passo 2 — Criar o brief criativo (via Claude Code)

```
@creative-director
*brief --type post --channel instagram --objective "gerar reconhecimento de marca"
```

### Passo 3 — Gerar o copy

```
@copy-writer
*write-copy --brief ./squads/design-squad/outputs/{slug}/creative-brief.md
```

### Passo 4 — Gerar o criativo HTML

```
@visual-designer
*create-post \
  --brief ./squads/design-squad/outputs/{slug}/creative-brief.md \
  --copy ./squads/design-squad/outputs/{slug}/copy.md \
  --design ./outputs/design-md/{slug}/DESIGN.md \
  --tokens ./outputs/design-md/{slug}/tokens.json \
  --format portrait
```

### Passo 5 — Revisar e aprovar

```
@creative-director
*review-creative \
  --html ./squads/design-squad/outputs/{slug}/post-portrait.html \
  --brief ./squads/design-squad/outputs/{slug}/creative-brief.md \
  --design ./outputs/design-md/{slug}/DESIGN.md
```

---

## Estrutura do projeto

```
.
├── design-md/          ← Skill de extração de design systems
│   ├── run.cjs         ← Ponto de entrada (node design-md/run.cjs --url ...)
│   └── package.json    ← Dependências: axios, cheerio, js-yaml, turndown
│
├── squads/
│   └── design-squad/   ← Squad de criação de criativos
│       ├── agents/     ← 7 agentes (creative-director, visual-designer, etc.)
│       ├── tasks/      ← 33 tasks com qualidade mínima enforçada
│       ├── config/
│       │   └── creative-quality-standard.md  ← Piso de qualidade (6 layers, score ≥75)
│       └── outputs/    ← Criativos gerados ficam aqui
│
└── outputs/
    └── design-md/      ← Outputs da extração (DESIGN.md, tokens, fingerprint)
```

---

## Troubleshooting

| Erro | Causa | Solução |
|------|-------|---------|
| `Cannot find module 'axios'` | npm install não foi rodado | `cd design-md && npm install` |
| `OPENROUTER_API_KEY not set` | .env não criado ou key vazia | Criar `.env` com a key preenchida |
| `exit code 5` (token limit) | Prompt muito longo | Adicionar `--max-tokens 32768` |
| `exit code null` (claude subprocess) | Claude CLI não funciona como subprocess | Usar `--provider openrouter` sempre |
| `tokens.json vazio` | LLM retornou DESIGN.md com ```markdown fences | Ignorar — o DESIGN.md em si está correto e usável |
