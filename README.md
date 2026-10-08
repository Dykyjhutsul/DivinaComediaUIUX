# DivinaComedia UX/UI — design pipeline

Операторський репозиторій для візуального напрямку продукту **Божествена комедія**.
Тут живуть референси, moodboards, Astra-промпти, концепти екранів і Style Lock.
Продуктова поведінка — у BA-репо (`DivinaComedia/docs/ba/`); цей репо її **не дублює**.

## Швидкий старт

1. Пройди [`checklists/step-1-triage.md`](checklists/step-1-triage.md) (Keep ≤30 + кластери A–C).
2. Заповни **D (product-UI)** — реальні скріни або synthetic Astra: [`prompts/03-d-product-ui/`](prompts/03-d-product-ui/README.md) → `references/clusters/D-product-ui/`.
3. Збери колажі за [`moodboards/README.md`](moodboards/README.md) (обовʼязково moodboard-D).
4. У ChatGPT Astra: [`prompts/00-base.md`](prompts/00-base.md) + [`prompts/01-style-exploration.md`](prompts/01-style-exploration.md).
5. Зафіксуй вибір у [`style-lock/STYLE-LOCK.md`](style-lock/STYLE-LOCK.md) (з template).
6. Генеруй екрани по одному з [`prompts/02-screens/`](prompts/02-screens/) → зберігай у `concepts/screens/`.
7. Після вибору напрямку — [`design-system/DESIGN.template.md`](design-system/DESIGN.template.md) → `DESIGN.md`, далі Figma.
8. UI Kit у Figma ([DivinaComediaUIKit](https://www.figma.com/design/7VS64TZ3mjVvxoaYF6ZHDk/DivinaComediaUIKit?node-id=0-1)) збирається за реєстром [`design-system/COMPONENT-IDS.md`](design-system/COMPONENT-IDS.md) і ledger [`design-system/figma-uikit-ledger.json`](design-system/figma-uikit-ledger.json): Variables зі Style Lock → Base → Feedback → Navigation/Home → Domain → Blocks → Examples.

**Не тягни всі 158 пінів у Figma.** У Figma йдуть лише winners після Style Lock.

## Дерево

```
references/     triage + clusters (mood vs UI) + INDEX + MOTIFS
moodboards/     колажі 3×3 для Astra
style-lock/     зафіксований візуальний контракт
prompts/        copy-paste промпти (EN) для Astra
briefs/         UX must-show по екранах (з BA)
concepts/       згенеровані моки
design-system/  DESIGN.md після lock · COMPONENT-IDS.md · figma-uikit-ledger.json
checklists/     протоколи кроків
```

Візуальний digest рефів: [`references/MOTIFS.md`](references/MOTIFS.md).  
**Home UX LOCKED:** [`briefs/home-ux-locked.md`](briefs/home-ux-locked.md) — далі лише UI/характер.

## Hard constraints (продукт)

- Сучасний веб 2025–2026: social / culture / comedy club — **не** середньовічний Данте.
- Без неону, cyberpunk glow, purple-on-white SaaS.
- Зони Рай / Чистилище / Пекло — **навігаційна метафора**, не літеральний fantasy HUD.
- Atmosphere refs = палітра і настрій; layout — з product-UI + [`briefs/screens-ux.md`](briefs/screens-ux.md).
- UI copy в макетах — українською, тон **«ти»** (PO 2026-10-07).

## Брейкпоінти

| Поверхня | Viewport |
|----------|----------|
| Host / desktop | 1440×900 |
| Player / mobile | 390×844 |

## Статус зараз

- [ ] Keep re-dropped у `references/keep/` (див. `references/INDEX.md`)
- [ ] Кластери A–C заповнені топ-рефами
- [ ] Кластер D (product-UI) має ≥8 рефів
- [ ] Style exploration зроблено
- [x] `style-lock/STYLE-LOCK.md` заповнено (Dark App + тон «ти» + pressed-токени)
- [x] UI Kit MVP (P1) зібрано у Figma — node id у [`design-system/COMPONENT-IDS.md`](design-system/COMPONENT-IDS.md)
- [x] UI Kit P2 зібрано (BASE/FB/NAV/HOME/ROOM/TRN/STD/ACH/AUTH/MISC + smoke D01/D05–D08) — ledger [`design-system/figma-uikit-ledger.json`](design-system/figma-uikit-ledger.json)
- [ ] Концепти ключових екранів у `concepts/screens/`

## Windows caveat

На NTFS імена `References` і `references` — **той самий шлях**. Не створюй другу папку з іншим регістром; використовуй лише `references/`.
