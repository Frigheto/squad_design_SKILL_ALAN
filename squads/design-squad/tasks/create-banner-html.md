---
task: Create Banner HTML
responsavel: "@visual-designer"
responsavel_type: agent
atomic_layer: task
elicit: true
quality_standard: squads/design-squad/config/creative-quality-standard.md
Entrada: |
  - creative_brief: caminho para creative-brief.md (obrigatório)
  - copy_md: caminho para copy.md (obrigatório)
  - design_md: caminho para DESIGN.md (obrigatório)
  - tokens_json: caminho para tokens.json (obrigatório)
  - dimensions: dimensões em px (ex: 1200x628, 300x250, 728x90) (obrigatório)
Saida: |
  - banner_html: arquivo HTML standalone com o banner (score mínimo 75/100; adaptações permitidas por formato)
Checklist:
  - "[ ] Ler creative-quality-standard.md — verificar adaptações permitidas para o formato solicitado"
  - "[ ] Montar :root completo com todos os tokens extraídos"
  - "[ ] Definir dimensões exatas do canvas"
  - "[ ] LAYER 1 — Fundo com base dark + mesh gradient (adaptar opacidade para dimensões menores)"
  - "[ ] LAYER 2 — ≥1 orb de luz + accent element (accent line ou borda gradiente)"
  - "[ ] LAYER 3 — Headline com gradient text + letter-spacing negativo (tamanho adaptado ao formato)"
  - "[ ] LAYER 4 — Proof element se formato ≥ 300x250 (dispensado em 728x90 e similares)"
  - "[ ] LAYER 5 — CTA com gradiente + glow (reduzir glow para formatos compactos)"
  - "[ ] LAYER 6 — Logo compacto, bordas rgba, handle se espaço permitir"
  - "[ ] Calcular score com adaptações do formato — mínimo 75/100 ajustado"
  - "[ ] Salvar banner-{dimensoes}.html"
---

# *create-banner

Gera banner HTML/CSS standalone com fidelidade total ao sistema de design extraído.
**Complexidade mínima obrigatória:** 6 layers conforme `creative-quality-standard.md`, com adaptações por formato.

## Uso

```bash
@visual-designer
*create-banner \
  --brief ./squads/design-squad/outputs/zentgrowth-banner/creative-brief.md \
  --copy ./squads/design-squad/outputs/zentgrowth-banner/copy.md \
  --design ./outputs/design-md/zentgrowth/DESIGN.md \
  --tokens ./outputs/design-md/zentgrowth/tokens.json \
  --dimensions 1200x628
```

## Adaptações obrigatórias por formato

| Formato | Dimensões | Layer 4 | Headline mín. | Orbs |
|---------|-----------|---------|--------------|------|
| Open Graph | 1200x628 | Obrigatório | 60px | 2 |
| Square Feed | 1080x1080 | Obrigatório | 72px | 2-3 |
| Leaderboard | 728x90 | Dispensado | 24px | 1 (opacity baixa) |
| Medium Rect | 300x250 | Dispensado | 32px | 1 |
| Wide Skyscraper | 160x600 | Stat card vertical | 36px | 1-2 |
| Story | 1080x1920 | Obrigatório | 80px | 2-3 |

## Template base (Open Graph 1200x628)

```css
:root {
  --color-primary: {hex};
  --color-secondary: {hex};
  --font-family: '{font}', system-ui, sans-serif;
}

body { width:1200px; height:628px; overflow:hidden; background:#07071a; font-family:var(--font-family); }

.banner {
  width:1200px; height:628px; position:relative; overflow:hidden;
  background: #07071a;
  background-image:
    radial-gradient(ellipse 55% 70% at 75% 20%, rgba({r1},0.5) 0%, transparent 60%),
    radial-gradient(ellipse 50% 60% at 15% 85%, rgba({r2},0.35) 0%, transparent 55%);
  display:flex; align-items:center; gap:60px; padding: 56px 72px;
}
.banner::before {
  content:''; position:absolute; inset:0; pointer-events:none;
  background-image: radial-gradient(circle, rgba(255,255,255,0.05) 1px, transparent 1px);
  background-size: 24px 24px;
}
.headline {
  font-size:60px; font-weight:900; letter-spacing:-0.04em;
  font-feature-settings:'ss01';
  background: linear-gradient(135deg, #fff 0%, rgba(255,255,255,0.7) 100%);
  -webkit-background-clip:text; -webkit-text-fill-color:transparent;
}
.cta-button {
  background: linear-gradient(135deg, var(--color-primary), var(--color-secondary));
  box-shadow: 0 0 30px rgba({r1},0.5), 0 6px 20px rgba(0,0,0,0.3);
  border-radius:9999px; border:none; font-weight:700; color:#fff;
  position:relative; overflow:hidden;
}
.cta-button::after {
  content:''; position:absolute; top:0; left:0; right:0; height:45%;
  background:linear-gradient(180deg, rgba(255,255,255,0.2), transparent);
  border-radius:inherit;
}
```

## Onde salvar

```
squads/design-squad/outputs/{slug}-banner-{dimensoes}/banner-{dimensoes}.html
```
