# 03 — Synthetic Product-UI (кластер D)

Astra генерує **тимчасові** D-рефи. Це **не** Style Lock і не фінальні екрани — layout + character + компонентна мова.

Усі `d01`–`d10` — **self-contained**. Character: Stage Absurd (сатира / комедія / controlled chaos).  
Home IA locked → див. `briefs/home-ux-locked.md` і `d01-hub.md`.

## Як ганяти

1. [`ASTRA-WORKAROUNDS.md`](ASTRA-WORKAROUNDS.md) — SEED IMAGE + новий чат.
2. Прикріпи 1 mood/seed jpg (технічний seed).
3. Скопіюй **весь** промпт зі слота.
4. Один слот = одне зображення.
5. Збережи в `references/clusters/D-product-ui/` як `d0N-…-synth-v1.png`.
6. Допиши рядок у `references/INDEX.md` § D.
7. Moodboard D → Style exploration.

## Слоти (після Home lock)

| Slot | Екран | Destination з Home |
|------|--------|--------------------|
| D01 | Home hub | — |
| D02 | Усі турніри / події (індекс) | центр → Усі турніри |
| D03 | Досягнення grid | ліва → Досягнення |
| D04 | Каталог соціальних ігор | ліва → Усі соціальні ігри |
| D05 | Лобі Host 1440 | після create room |
| D06 | Лобі Player 390 | join flow |
| D07 | Live round | після Start |
| D08 | Турнір афіша (деталі) | центр → Деталі |
| D09 | Тренування / формати | права → Стендап/Імпро/Теорія |
| D10 | Character materials sheet | для Style Lock |

## Порядок (рекомендований)

1. **D01** (locked Home) — якір
2. **D10** materials — закріпити character
3. D03 · D04 · D02 · D08 · D09 — destinations
4. D05 · D06 · D07 — session

Мінімум для Style Lock: **D01, D03, D05, D07, D08, D10**. Краще всі 10.

## Hard rule

Якщо Astra малює fantasy / quiet luxury / космос замість UI:
`Regenerate: keep STAGE ABSURD character, but this must look like a real web app screenshot. UI chrome first. No quiet luxury. No Dante fantasy art.`
