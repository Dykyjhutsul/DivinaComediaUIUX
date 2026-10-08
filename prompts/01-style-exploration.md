# 01 — Style exploration

**Коли:** після triage + moodboards; **до** Style Lock.
**Attach:** `moodboard-A`, `B`, `C`, і обовʼязково `moodboard-D-product-ui` (або окремі UI refs).

Скопіюй BASE з `00-base.md`, потім це:

```text
[PASTE BASE FROM 00-base.md]

TASK
Generate 4 separate UI direction concepts for the SAME screen:
Dante Home — authenticated hub with three zone entry areas (Рай / Чистилище / Пекло).

Style A — Warm editorial night: deep charcoal, soft amber accent, film grain,
serif display + clean sans body. Atmosphere from cosmic/organic moodboards,
but layout is modern product UI.

Style B — Soft clay / tactile: muted terracotta + sage + cream, rounded but not bubbly,
paper/cloth textures. Calm, human, adult.

Style C — Quiet luxury social: near-black surfaces, single copper or champagne accent,
generous whitespace, photography-led. Refined nightlife / culture app.

Style D — Bright human comedy club: daylight or soft stage light, pastel but muted
(no neon), bold display type, playful but adult — not childish.

RULES
- For each style: one full-page desktop mockup 1440×900.
- Label A/B/C/D in a corner.
- Same information architecture on all four: top bar + three equal zone entries.
- No stats strips, no secondary marketing clutter.
- After images: briefly recommend which 1–2 styles fit party games + solo training + tournament.

I will pick a direction and lock it before generating other screens.
```

## Після генерації

1. Збережи виходи в `concepts/style-exploration/` як `style-A.png` … `style-D.png`.
2. Обери 1 (або hybrid) → заповни `style-lock/STYLE-LOCK.md`.
3. Далі лише `prompts/02-screens/*` + paste block зі STYLE-LOCK.
