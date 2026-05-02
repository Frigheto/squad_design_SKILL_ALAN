# Creative Quality Standard — Nível Mínimo Obrigatório

> Este documento define o **piso de complexidade visual** que TODA produção do design-squad deve atingir.
> Nenhum criativo pode ser entregue abaixo deste padrão. O `@creative-director` é responsável por bloquear
> produções que não atingirem todos os layers abaixo.

---

## Referência de baseline

O design de referência que estabelece este padrão é:
```
squads/design-squad/outputs/zentgrowth-post-1080x1350/post-1080x1350-v2.html
```
Qualquer novo criativo deve ter **complexidade igual ou superior** a esse arquivo.

---

## Os 6 Layers Obrigatórios

### Layer 1 — Background Rich (OBRIGATÓRIO)

Fundo com no mínimo **3 sub-layers empilhados**:

| Sub-layer | Implementação |
|-----------|--------------|
| Base color | `background: #07071a` (dark) ou gradiente de marca |
| Mesh gradient | `2-4 radial-gradient()` em `background` usando cores da marca com opacity `0.3-0.5` |
| Texture overlay | CSS pattern via `::before` — grid de pontos, linhas ou ruído SVG |

**Proibido:** fundo `#ffffff` puro, `#000000` puro, ou cor sólida plana sem camadas.

**CSS mínimo:**
```css
.canvas {
  background: #07071a;
  background-image:
    radial-gradient(ellipse 60% 50% at 80% 10%, rgba(99,102,241,0.45) 0%, transparent 65%),
    radial-gradient(ellipse 50% 60% at 10% 80%, rgba(236,72,153,0.3) 0%, transparent 60%),
    radial-gradient(ellipse 40% 40% at 50% 50%, rgba(139,92,246,0.25) 0%, transparent 70%);
}
.canvas::before {
  content: '';
  position: absolute;
  inset: 0;
  background-image: radial-gradient(circle, rgba(255,255,255,0.06) 1px, transparent 1px);
  background-size: 28px 28px;
}
```

---

### Layer 2 — Depth & Atmosphere (OBRIGATÓRIO)

Mínimo **2 orbs de luz** com `filter: blur()`:

```css
.orb {
  position: absolute;
  border-radius: 50%;
  filter: blur(80px);       /* mínimo 60px */
  pointer-events: none;
}
/* Orb 1 — canto superior oposto ao foco principal */
/* Orb 2 — canto inferior/lateral */
/* Orb 3 (opcional) — central com opacity baixa */
```

Accent line no topo ou divisor decorativo:
```css
.accent-line {
  height: 2px;
  background: linear-gradient(90deg, transparent 0%, var(--color-primary) 50%, transparent 100%);
}
```

---

### Layer 3 — Typography Premium (OBRIGATÓRIO)

| Regra | Valor |
|-------|-------|
| Headline mínimo | `font-size: 72px`, `font-weight: 800` |
| Headline gradient | `-webkit-background-clip: text; -webkit-text-fill-color: transparent` |
| Letter-spacing headline | `-0.03em` ou mais negativo |
| `font-feature-settings` | `'ss01'` sempre no display text |
| Subheadline | `rgba(255,255,255,0.8)`, `font-weight: 400-500` |

**Proibido:** headline com cor sólida opaca sem efeito. Toda headline principal deve ter gradiente de texto.

---

### Layer 4 — Proof Element (OBRIGATÓRIO — pelo menos 1)

O criativo deve conter **ao menos um elemento de prova/credibilidade**:

| Tipo | Quando usar |
|------|------------|
| **Stat cards** | Métricas com número grande + label (ex: R$128k / Clientes / NPS) |
| **Dashboard mockup** | Preview de interface do produto com barra titlebar (traffic lights) |
| **Testimonial card** | Avatar + quote + nome, glassmorphism |
| **Feature pills** | Badges com glowing dot + texto de feature |
| **Before/After split** | Comparativo visual lado a lado |
| **Progress/Chart** | Mini gráfico de barras ou linha animada |

Os elementos de prova devem usar **glassmorphism**:
```css
.proof-element {
  background: rgba(255, 255, 255, 0.08);
  backdrop-filter: blur(12px);
  border: 1px solid rgba(255, 255, 255, 0.15);
  border-radius: 12px;
}
```

---

### Layer 5 — CTA Premium (OBRIGATÓRIO)

O botão CTA **nunca pode ser plano**. Deve ter:

```css
.cta-button {
  /* Gradiente — nunca cor sólida */
  background: linear-gradient(135deg, var(--color-primary), var(--color-secondary));

  /* Glow externo */
  box-shadow:
    0 0 40px rgba(99,102,241,0.5),
    0 8px 32px rgba(0,0,0,0.3);

  /* Inner shine via ::after */
  position: relative;
  overflow: hidden;
}
.cta-button::after {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 40%;
  background: linear-gradient(180deg, rgba(255,255,255,0.18) 0%, transparent 100%);
  border-radius: inherit;
}
```

Alternativa aprovada: botão branco `#ffffff` com texto em `var(--color-primary)` + shadow elevado (válido para arquétipos light-dominant).

---

### Layer 6 — Polish & Finish (OBRIGATÓRIO)

| Item | Requisito |
|------|----------|
| Logo | Deve aparecer com ícone + texto, usar glassmorphism ou gradiente |
| Bordas de elementos | `rgba(255,255,255,0.15-0.25)` — nunca bordas sólidas opacas |
| Z-index layers | Mínimo 3 níveis: fundo (z:1), conteúdo (z:10), CTA/destaque (z:20) |
| Overflow | `overflow: hidden` no canvas principal |
| Handle/marca | `@handle` ou URL no rodapé, `rgba(255,255,255,0.5)` |
| Fontes | Google Fonts CDN ou @font-face inline — nunca depender de fontes do sistema |

---

## Scoring de Qualidade

Antes de entregar, o `@creative-director` deve pontuar o criativo:

| Layer | Peso | Critério de PASS |
|-------|------|-----------------|
| Background Rich | 20pts | 3 sub-layers presentes |
| Depth & Atmosphere | 15pts | ≥ 2 orbs + accent element |
| Typography Premium | 20pts | Gradient text + sizing correto |
| Proof Element | 25pts | ≥ 1 proof element com glassmorphism |
| CTA Premium | 10pts | Gradiente + glow + inner shine |
| Polish & Finish | 10pts | Todos itens da tabela ✓ |
| **TOTAL** | **100pts** | |

| Score | Status |
|-------|--------|
| 90-100 | ✅ PREMIUM — entregável |
| 75-89 | ⚠️ ACCEPTABLE — entregável com nota |
| 60-74 | 🔄 NEEDS_REVISION — retornar ao @visual-designer |
| < 60 | ❌ BLOCKED — não sai do fluxo |

---

## Adaptações por Formato

| Formato | Ajustes permitidos |
|---------|--------------------|
| **Story 1080x1920** | Proof element pode ser substituído por animação CSS (keyframes) |
| **Banner 728x90** | Proof element dispensado; Layer 3 pode usar 36px mínimo; orbs limitados a 1 |
| **Banner 300x250** | Proof element dispensado; headline mínimo 32px |
| **Email** | Sem backdrop-filter (cliente de email); gradientes como imagens inline; glassmorphism substituído por border sólida com rgba |
| **Landing page** | Todos os layers obrigatórios + responsividade |

---

## Tokens obrigatórios no :root

Todo HTML gerado deve abrir com o bloco `:root` completo dos tokens extraídos:

```css
:root {
  /* — extraídos de tokens.json — */
  --color-primary:    {hex};
  --color-secondary:  {hex};
  --color-tertiary:   {hex};  /* se existir */
  --color-pink:       {hex};  /* se existir */
  --color-surface:    {hex};
  --color-text:       {hex};

  --font-family:      '{familia}', system-ui, sans-serif;

  --radius-sm:  {px};
  --radius-md:  {px};
  --radius-lg:  {px};
  --radius-xl:  {px};
  --radius-full: 9999px;

  --space-xs:  4px;
  --space-sm:  8px;
  --space-md:  16px;
  --space-lg:  24px;
  --space-xl:  32px;
  --space-2xl: 48px;

  --shadow-standard:  0px 1px 3px rgba(0,0,0,0.08), 0px 4px 12px rgba(0,0,0,0.06);
  --shadow-elevated:  0px 4px 16px rgba(0,0,0,0.15), 0px 12px 36px rgba(0,0,0,0.12);
}
```
