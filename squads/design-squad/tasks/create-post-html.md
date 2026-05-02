---
task: Create Post HTML
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
  - format: square (1080x1080) | landscape (1200x628) | portrait (1080x1350)
Saida: |
  - post_html: arquivo HTML standalone do post (score mínimo 75/100)
Checklist:
  - "[ ] Ler creative-quality-standard.md — internalizar os 6 layers obrigatórios"
  - "[ ] Montar :root completo com TODOS os tokens de tokens.json como CSS custom properties"
  - "[ ] Definir dimensões exatas do canvas (width/height fixos no body e .canvas)"
  - "[ ] LAYER 1 — Construir fundo com: base dark + mesh gradient (2-4 radial-gradients) + texture ::before"
  - "[ ] LAYER 2 — Adicionar ≥2 orbs de luz com filter:blur + accent line decorativa"
  - "[ ] LAYER 3 — Headline com gradient text (-webkit-background-clip) + ≥72px + letter-spacing negativo"
  - "[ ] LAYER 4 — Inserir ≥1 proof element (stat cards, mockup, pills, chart) com glassmorphism"
  - "[ ] LAYER 5 — CTA com gradiente + glow (box-shadow 40px+) + inner shine (::after)"
  - "[ ] LAYER 6 — Logo, bordas rgba, z-index em 3 níveis, handle no footer"
  - "[ ] Calcular score contra creative-quality-standard.md — mínimo 75/100"
  - "[ ] Se score < 75: iterar adicionando complexity antes de salvar"
  - "[ ] Salvar post-{format}.html"
---

# *create-post

Gera post HTML para redes sociais com fidelidade ao sistema de design extraído.
**Complexidade mínima obrigatória:** 6 layers conforme `creative-quality-standard.md` — score ≥ 75/100.

## Uso

```bash
@visual-designer
*create-post \
  --brief ./squads/design-squad/outputs/zentgrowth-post/creative-brief.md \
  --copy ./squads/design-squad/outputs/zentgrowth-post/copy.md \
  --design ./outputs/design-md/zentgrowth/DESIGN.md \
  --tokens ./outputs/design-md/zentgrowth/tokens.json \
  --format portrait
```

## Template de estrutura mínima (portrait 1080x1350)

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>{brand} — Post</title>
  <link href="https://fonts.googleapis.com/css2?family={font}:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">
  <style>
    /* ── LAYER 0: Tokens ── */
    :root {
      --color-primary:   {hex};
      --color-secondary: {hex};
      --color-tertiary:  {hex};
      --color-accent:    {hex};
      --font-family:     '{font}', system-ui, sans-serif;
      --radius-xl: 12px; --radius-full: 9999px;
      --space-sm: 8px; --space-md: 16px; --space-lg: 24px; --space-xl: 32px; --space-2xl: 48px;
    }
    * { margin:0; padding:0; box-sizing:border-box; }
    body { width:1080px; height:1350px; overflow:hidden; background:#07071a; display:flex; align-items:center; justify-content:center; font-family:var(--font-family); }

    /* ── LAYER 1: Background Rich ── */
    .canvas {
      width:1080px; height:1350px; position:relative; overflow:hidden;
      background: #07071a;
      background-image:
        radial-gradient(ellipse 60% 50% at 80% 10%, rgba({r1},0.45) 0%, transparent 65%),
        radial-gradient(ellipse 50% 60% at 10% 80%, rgba({r2},0.3)  0%, transparent 60%),
        radial-gradient(ellipse 40% 40% at 50% 50%, rgba({r3},0.2)  0%, transparent 70%);
      display:flex; flex-direction:column; align-items:center; justify-content:space-between;
      padding: 64px 72px;
    }
    /* Texture overlay (dot grid) */
    .canvas::before {
      content:''; position:absolute; inset:0; pointer-events:none; z-index:1;
      background-image: radial-gradient(circle, rgba(255,255,255,0.06) 1px, transparent 1px);
      background-size: 28px 28px;
    }

    /* ── LAYER 2: Orbs + Accent ── */
    .orb { position:absolute; border-radius:50%; filter:blur(80px); pointer-events:none; }
    .orb-1 { width:500px; height:500px; top:-120px; right:-100px; background:rgba({r1},0.4); }
    .orb-2 { width:400px; height:400px; bottom:80px; left:-80px; background:rgba({r2},0.3); }
    .orb-3 { width:280px; height:280px; bottom:-40px; right:80px; background:rgba({r3},0.25); }
    .accent-line { width:100%; height:2px; background:linear-gradient(90deg, transparent, var(--color-primary), transparent); position:absolute; top:0; left:0; z-index:5; }

    /* ── LAYER 3: Tipografia Premium ── */
    .headline {
      font-size: 88px; font-weight: 900; line-height: 1.0; letter-spacing: -0.04em;
      font-feature-settings: 'ss01';
      background: linear-gradient(135deg, #ffffff 0%, rgba(255,255,255,0.7) 100%);
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    }
    .subheadline {
      font-size: 26px; font-weight: 400; color: rgba(255,255,255,0.75);
      line-height: 1.5; letter-spacing: -0.01em;
    }

    /* ── LAYER 4: Proof Element (glassmorphism) ── */
    .proof-card {
      background: rgba(255,255,255,0.08); backdrop-filter: blur(12px);
      border: 1px solid rgba(255,255,255,0.15); border-radius: var(--radius-xl);
    }

    /* ── LAYER 5: CTA Premium ── */
    .cta-button {
      background: linear-gradient(135deg, var(--color-primary), var(--color-secondary));
      box-shadow: 0 0 40px rgba({r1},0.5), 0 8px 32px rgba(0,0,0,0.3);
      border-radius: var(--radius-full); border: none; cursor: pointer;
      font-family: var(--font-family); font-weight: 700;
      color: #ffffff; position: relative; overflow: hidden;
    }
    .cta-button::after {
      content:''; position:absolute; top:0; left:0; right:0; height:45%;
      background: linear-gradient(180deg, rgba(255,255,255,0.2) 0%, transparent 100%);
      border-radius: inherit;
    }

    /* ── LAYER 6: Polish ── */
    .logo-icon { background:rgba(255,255,255,0.15); backdrop-filter:blur(8px); border:1px solid rgba(255,255,255,0.2); border-radius:var(--radius-xl); }
    .handle { font-size:15px; color:rgba(255,255,255,0.45); letter-spacing:0.02em; }
  </style>
</head>
<body>
  <div class="canvas">
    <div class="accent-line"></div>
    <div class="orb orb-1"></div>
    <div class="orb orb-2"></div>
    <div class="orb orb-3"></div>

    <!-- LAYER 6: Header/Logo -->
    <header>...</header>

    <!-- LAYER 3 + LAYER 4: Content -->
    <main>
      <h1 class="headline">{headline}</h1>
      <p class="subheadline">{subheadline}</p>
      <!-- LAYER 4: proof element -->
      <div class="proof-card">...</div>
    </main>

    <!-- LAYER 5 + LAYER 6: Footer -->
    <footer>
      <button class="cta-button">{cta}</button>
      <span class="handle">@{handle}</span>
    </footer>
  </div>
</body>
</html>
```

## Onde salvar

```
squads/design-squad/outputs/{slug}-post-{format}/post-{format}.html
```

## Scoring automático antes de salvar

Antes de salvar, o @visual-designer deve verificar internamente:

| Layer | Check | Pts |
|-------|-------|-----|
| Background Rich | mesh gradient + texture ::before | 20 |
| Depth & Atmosphere | ≥2 orbs + accent line | 15 |
| Typography Premium | gradient text + ≥72px + letter-spacing neg. | 20 |
| Proof Element | ≥1 glassmorphism element | 25 |
| CTA Premium | gradient + glow + ::after shine | 10 |
| Polish & Finish | logo, bordas rgba, z-index, handle | 10 |

**Score < 75 → não salvar, adicionar elementos faltantes e recalcular.**
