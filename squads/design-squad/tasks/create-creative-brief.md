---
task: Create Creative Brief
responsavel: "@creative-director"
responsavel_type: agent
atomic_layer: task
elicit: true
Entrada: |
  - design_md: caminho para DESIGN.md aprovado (obrigatório)
  - agent_prompt: caminho para agent-prompt.txt (obrigatório)
  - style_fingerprint: caminho para style-fingerprint.json (obrigatório)
  - creative_type: banner | post | story | landing | presentation | email | card
  - channel: web | instagram | linkedin | twitter | email | ads
  - objective: objetivo do criativo (ex: "converter visitantes em leads")
Saida: |
  - creative_brief: arquivo creative-brief.md com spec completa do criativo
quality_standard: squads/design-squad/config/creative-quality-standard.md
Checklist:
  - "[ ] Ler creative-quality-standard.md — internalizar os 6 layers antes de escrever o brief"
  - "[ ] Ler DESIGN.md — extrair paleta, tipografia, componentes, tom visual"
  - "[ ] Ler agent-prompt.txt — absorver DNA visual para direção criativa"
  - "[ ] Ler style-fingerprint.json — confirmar arquétipo visual"
  - "[ ] Definir tipo e dimensões do criativo"
  - "[ ] Definir hierarquia visual (o que vai em destaque)"
  - "[ ] Definir mensagem principal e objetivo"
  - "[ ] Especificar no brief: cor e tipo do mesh gradient do fundo"
  - "[ ] Especificar no brief: qual Proof Element usar (stat card, mockup, pills, chart, testimonial)"
  - "[ ] Especificar no brief: cor e efeito do CTA (gradiente, glow color)"
  - "[ ] Definir tom de voz e restrições de copy"
  - "[ ] Salvar creative-brief.md"
---

# *brief

Cria um brief criativo completo a partir do sistema de design extraído.

## Uso

```bash
@creative-director
*brief --type banner --channel instagram --objective "gerar leads"
```

## Output — creative-brief.md

```markdown
# Creative Brief — {tipo} {canal}

## Objetivo
{objetivo do criativo}

## Formato & Dimensões
- Tipo: {banner | post | story | landing | email}
- Dimensões: {ex: 1080x1080px}
- Canal: {instagram | web | email | ads}

## Direção Visual
- Arquétipo: {polaris-friendly | shadcn-neutral | ...}
- Cor dominante: {token + hex}
- Cor de destaque (CTA): {token + hex}
- Fundo: dark base {hex} com mesh gradient {cor1} → {cor2} → {cor3}
- Tipografia principal: {família + peso + tamanho}
- Radius: {valor dos tokens}
- Tratamento de superfície: {gradient | glassmorphism | solid}
- Espaçamento: {very-roomy | roomy | compact}
- Sombras: {strong | moderate | subtle}

## Complexity Blueprint (obrigatório)
- **Layer 1 — Background:** base {hex} + radial-gradient de {cor} e {cor} + texture {dots | lines | noise}
- **Layer 2 — Atmosphere:** orbs em {posições} com blur {px} + accent {line | border | dot}
- **Layer 3 — Headline:** gradient de {cor} a {cor} + {tamanho}px + weight {peso}
- **Layer 4 — Proof Element:** {stat cards | dashboard mockup | feature pills | testimonial | chart | animação}
- **Layer 5 — CTA:** gradient {cor1} → {cor2} + glow {cor} + inner shine
- **Layer 6 — Polish:** logo {estilo} + bordas rgba({opacidade}) + handle {formato}

## Hierarquia de Conteúdo
1. {elemento principal — ex: headline}
2. {elemento secundário — ex: subheadline}
3. {elemento de suporte — ex: body}
4. {CTA — ex: botão}

## Restrições
- NÃO usar: {lista do Don'ts do DESIGN.md}
- SEMPRE usar: {lista do Do's do DESIGN.md}

## Referência de Componentes
- Botão primário: {spec do DESIGN.md}
- Card: {spec do DESIGN.md}
```

## Onde salvar

```
squads/design-squad/outputs/{slug}-{tipo}-{data}/creative-brief.md
```
