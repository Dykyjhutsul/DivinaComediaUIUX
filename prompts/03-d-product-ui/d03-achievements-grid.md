# D03 — Досягнення (категорії)

Destination з Home (ліва колонка → «Досягнення»).  
Файл: `d03-achievements-grid-synth-v1.png` · Desktop 1440×900  
Spec: **F-4.2** · логіка: `achievements-business-logic` + UX review 2026-08-28 · BR-ACH-003/014/017

```text
ROLE
Art director + product UI for «Божественна комедія»: satire, comedy, self-irony, controlled chaos.
ONE desktop web-app screenshot. Ukrainian UI chrome. Modern usable product — with comedic voltage.
NOT quiet luxury museum. NOT RPG loot inventory. NOT medieval Dante.

SEED: technical only if attached. Generate now. Do not change IA.

════════════════════════════════════════════════════════
LOCKED INFORMATION ARCHITECTURE — DO NOT CHANGE
════════════════════════════════════════════════════════

1) HEADER
   - Left: wordmark «Божественна комедія»
   - Right: profile avatar
   - Same shell as Home. No extra nav links.

2) TITLE ROW
   - Title ONLY: «Досягнення»
   - NO subtitles, NO «Рай» / Heaven / hell / «Категорії досягнень»
   - Near title (right of title): tiny easter-egg control → «Грішники»
     (devil/imp motif OK; subtle; NOT a 21st category card; NOT in the grid)

3) CATEGORY GRID — exactly 20 heaven tiles, ~4 per row desktop
   Each tile MUST show only:
   - icon (CMS-style illustration — not letter avatar, not rarity frame)
   - category name (use the English catalog names below; UA chrome OK)
   - personal progress X/Y  (e.g. 7/24)
   NO user-count. NO «N achievements» label. NO locked/Premium badges.
   NO search. NO filter chips. NO stats dashboard chrome.
   NO heaven/hell labels on cards. «Грішники» NEVER appears in the grid.

4) PROGRESS LOGIC (X/Y) — authenticated user state for this mock
   - X = how many achievements in THIS category the current user confirmed
   - Y = total active achievements in that category
   - Vary X/Y across tiles (some low, some mid, one near-complete). Example: Fun & Party → 7/24
   - Do NOT invent global «users completed» counts on cards

5) EXACT 20 CATEGORY NAMES (in this order, 5 rows × 4)
   1. Fun & Party
   2. Social Life
   3. Friends & Communication
   4. Food & Drinks
   5. Travel
   6. School & University
   7. Work & Career
   8. Sports & Physical Activity
   9. Music
   10. Movies & Series
   11. Personal Habits
   12. Childhood & Memories
   13. Love & Romance
   14. Relationships
   15. Sexual Experience
   16. Extreme & Risk
   17. Deep Travel
   18. Luxury & Status
   19. Altered States
   20. Power & Influence

ART DIRECTION
Paradise page climate (PO 2026-10-08): luminous gold tree on void as PAGE BACKGROUND
(`paradise-tree-bg-desktop.png` / mobile crop). Cards float on `zone/card` #14110D
with gold/300@16% border and gold progress bar. Ghost header — do not cover the tree
with a solid #121212 bar. Large H1 «Досягнення»; Sinners = compact pill (star + arrow),
not a 21st card. Same button/radius/type system as the rest of the kit.
NO subtitle (spec C-5). NO neon/cyberpunk glow. NO rarity/loot frames.
Dense calm catalog — scannable web app, not gamer HUD.

Generate NOW.
```
