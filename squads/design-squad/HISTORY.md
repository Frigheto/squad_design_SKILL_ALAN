# HISTORY.md — design-squad

Registro completo da criação do `design-squad` via fluxo guiado `@squad-creator *design-squad`.

---

## Contexto inicial

**Data:** 2026-05-02
**Projeto:** `skill squad desing` (greenfield — sem repositório git)
**Agente orquestrador:** `@aios-master` (Orion)
**Agente executor:** `@squad-creator` (Craft)
**Skill de origem:** `design-md` (criada por Alan Nicolas)

O projeto continha apenas dois artefatos:
- `AGENTS.md` — configuração de shortcuts do AIOS para Codex CLI
- `design-md/` — skill autônoma de extração de sistemas de design via análise estática de HTML/CSS

---

## O que é a skill `design-md`

Skill que extrai um sistema de design completo de qualquer URL pública usando **análise estática de HTML/CSS** — sem headless browser, sem Playwright. O motor de cognição é o `claude -p` (Claude Code CLI) ou OpenRouter.

**Pipeline de 8 fases:**
1. `axios.get(url)` → HTML
2. Coleta de todos os CSS (`<link>`, `<style>`, `@import`)
3. Regex detecta cores, fontes, espaçamentos, border-radius, stacks (Tailwind, Next.js, Radix…)
4. `turndown` converte HTML → Markdown
5. Monta prompt com todos os inputs para o LLM
6. LLM escreve `DESIGN.md` no formato Google-spec + lint automático
7. Gera `tokens.json`, `extraction-log.yaml`, quality-score
8. Renderiza `preview.html` standalone

**Outputs gerados por extração:**
```
outputs/design-md/{slug}/
├── DESIGN.md
├── tokens.json
├── extraction-log.yaml
├── lint-report.json
├── quality-score.json
├── preview.html
├── style-fingerprint.json
├── agent-prompt.txt
└── inputs/
```

**Providers suportados:**
- `claude-cli` (padrão) — Opus 4.7
- `openrouter` — Haiku 4.5, requer `OPENROUTER_API_KEY`

---

## Fluxo de criação do squad

### Etapa 1 — Análise de domínio (`*design-squad`)

O agente `@squad-creator` executou a task `squad-creator-design.md` com o `SKILL.md` como documentação de entrada.

**Domínio identificado:** `design-system-extraction`

**Entidades extraídas:**
- URL, DESIGN.md, tokens.json, style-fingerprint, preview.html, drift-report, lint-report, quality-score, extraction-log

**Workflows detectados:**
1. `url-to-design-extraction`
2. `css-token-detection`
3. `design-drift-detection`
4. `quality-validation`
5. `phase-reuse-management`

**Integrações mapeadas:**
- Claude CLI (`claude -p`)
- OpenRouter API
- `@google/design.md` spec

**Stakeholders identificados:**
- `designer` — consume outputs para decisões visuais
- `developer` — consome `tokens.json` e `DESIGN.md`
- `ci-system` — executa headless via OpenRouter

---

### Etapa 2 — Definição dos agentes (Phase 3)

4 agentes foram recomendados e aceitos pelo usuário:

| ID | Persona | Papel | Confiança |
|----|---------|-------|-----------|
| `design-extractor` | Pixel | Pipeline completo URL → DESIGN.md (8 fases) | 95% |
| `design-token-manager` | Token | Gestão de tokens.json (validar, exportar, diff, merge) | 88% |
| `design-drift-detector` | Drift | Comparação URL ao vivo vs DESIGN.md local | 91% |
| `design-quality-reviewer` | Qualia | Lint, quality-score e aprovação Google-spec | 87% |

---

### Etapa 3 — Definição das tasks (Phase 4)

14 tasks foram recomendadas e aceitas:

**design-extractor (3 tasks):**
- `extract-design-system.md` — extração completa de uma URL
- `reextract-design-system.md` — re-extração forçando cache bypass (`--no-reuse`)
- `list-extraction-outputs.md` — listagem de extrações disponíveis localmente

**design-token-manager (4 tasks):**
- `validate-design-tokens.md` — validação de tokens.json contra spec DTCG
- `export-design-tokens.md` — exportação para `dtcg | css-vars | json`
- `diff-design-tokens.md` — comparação entre dois tokens.json
- `merge-design-tokens.md` — mesclagem com estratégia `merge | override`

**design-drift-detector (3 tasks):**
- `detect-design-drift.md` — detecção de drift URL viva vs DESIGN.md local
- `drift-report-summary.md` — relatório legível de um drift-report.json
- `drift-history.md` — histórico cronológico de drifts por slug

**design-quality-reviewer (4 tasks):**
- `lint-design-md.md` — lint `@google/design.md` em um DESIGN.md
- `quality-score-report.md` — nota A-F em 7 categorias
- `confidence-report.md` — breakdown de tokens por nível (high/medium/low)
- `approve-design-spec.md` — decisão APPROVED | NEEDS_REVISION com justificativa

---

### Etapa 4 — Adições customizadas (Phase 5)

Nenhuma adição customizada. Usuário optou por continuar com as recomendações.

---

### Etapa 5 — Geração do blueprint (Phase 6)

Blueprint gerado e salvo em:
```
squads/.designs/design-squad-design.yaml
```

```
Agentes:            4  (4 recomendados, 0 adicionados)
Tasks:             14  (14 recomendadas, 0 adicionadas)
User adjustments:   0
Overall confidence: 88%
```

---

### Etapa 6 — Criação da estrutura (`*create-squad`)

Task `squad-creator-create.md` executada com `--from-design`.

**Estrutura gerada:**
```
squads/design-squad/
├── squad.yaml
├── README.md
├── HISTORY.md
├── config/
│   ├── coding-standards.md
│   ├── tech-stack.md
│   └── source-tree.md
├── agents/
│   ├── design-extractor.md
│   ├── design-token-manager.md
│   ├── design-drift-detector.md
│   └── design-quality-reviewer.md
├── tasks/
│   ├── extract-design-system.md
│   ├── reextract-design-system.md
│   ├── list-extraction-outputs.md
│   ├── validate-design-tokens.md
│   ├── export-design-tokens.md
│   ├── diff-design-tokens.md
│   ├── merge-design-tokens.md
│   ├── detect-design-drift.md
│   ├── drift-report-summary.md
│   ├── drift-history.md
│   ├── lint-design-md.md
│   ├── quality-score-report.md
│   ├── confidence-report.md
│   └── approve-design-spec.md
├── workflows/       (vazio — pendente de testes)
├── checklists/
├── templates/
├── tools/
├── scripts/
└── data/
```

---

### Etapa 7 — Validação (`*validate-squad`)

Task `squad-creator-validate.md` executada.

**Resultado inicial:**
```
Errors:   0
Warnings: 2
  - [TASK_FILE_NOT_FOUND]: 9 tasks declaradas no squad.yaml sem arquivo criado
  - [MISSING_WORKFLOWS]: Nenhum workflow definido
Result: VALID (with warnings)
```

**Ação tomada:** 9 tasks faltantes foram criadas para zerar os warnings.

**Resultado final:**
```
Errors:   0
Warnings: 0
Result: VALID
```

---

## Decisões tomadas durante a criação

| Decisão | Motivo |
|---------|--------|
| Usar fluxo guiado `@squad-creator *design-squad` | Segue padrão AIOS, gera blueprint validado |
| 4 agentes ao invés de 1 monolítico | Separação de responsabilidades: extração, tokens, drift, qualidade |
| `config_mode: extend` | Squad herda regras core do AIOS sem sobrescrever |
| Workflow adiado para após testes | Evitar trabalho prematuro — workflow será baseado nos outputs reais |
| Tasks criadas antes dos testes | Completar a estrutura declarada no squad.yaml (evitar warnings) |

---

## Pendências

- [ ] **Testar** `@design-extractor *extract` em URLs reais
- [ ] **Validar** outputs gerados (DESIGN.md, tokens.json, preview.html)
- [ ] **Criar workflow** `extract-and-approve.yaml` após consolidação dos testes
- [ ] **Inicializar** repositório git (`*environment-bootstrap`)

---

## Referências

| Artefato | Caminho |
|----------|---------|
| Blueprint | `squads/.designs/design-squad-design.yaml` |
| Skill de origem | `design-md/SKILL.md` |
| Manifest do squad | `squads/design-squad/squad.yaml` |
| Documentação da skill | `design-md/README.md` |
