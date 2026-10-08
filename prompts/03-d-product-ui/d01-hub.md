# D01 — Головна (Home)

**UX / IA: LOCKED** → [`../../briefs/home-ux-locked.md`](../../briefs/home-ux-locked.md)  
Наступні генерації = **лише UI / character**, не перебудова блоків.

Файл виходу: `d01-hub-synth-v6-portal.png` · Desktop **1440×900** (або **1440×1200**).  
База (PO 2026-10-07): [`../../concepts/d01-hub/2026-10-07-portal-v1.png`](../../concepts/d01-hub/2026-10-07-portal-v1.png) · фон [`../../references/keep/home-portal-bg.png`](../../references/keep/home-portal-bg.png) — **дзеркалити по горизонталі** (світлі двері зліва, вогняні справа).

### Astra seed
Див. [`ASTRA-WORKAROUNDS.md`](ASTRA-WORKAROUNDS.md).

---

## Один суцільний промпт — копіюй в Astra

```text
ROLE
You are an art director + product UI designer for a comedy platform with bite:
satire, stage energy, absurd self-irony, theatrical controlled chaos —
NOT a quiet luxury museum app, NOT a solemn “premium culture” dashboard,
NOT a fantasy Dante landing page.

Generate ONE high-fidelity desktop web-app screenshot (2025–2026).
Ukrainian UI copy. Product name: «Божественна комедія».

SEED IMAGE RULE
Attached image (if any) = technical seed only. Do not copy its layout or art.
Generate immediately. Do not ask questions. Do not propose a different IA.

════════════════════════════════════════════════════════
LOCKED INFORMATION ARCHITECTURE — DO NOT CHANGE
════════════════════════════════════════════════════════
Reproduce EXACTLY this structure and content inventory.
Do NOT reorder blocks. Do NOT add widgets. Do NOT invent new content types.

This is the site root and the ONLY start page — there is no separate marketing landing.
The same screen serves guests and signed-in users.

1) HEADER
   - Left ONLY: wordmark «Божественна комедія»
   - Right ONLY: profile — signed-in: user avatar; guest: neutral profile icon (it leads to sign-in)
   - NO nav links (no Ігри/Події/Досягнення/Профіль, no Рай/Чистилище/Пекло sections in header)
   - NO search, NO «Увійти» button, NO left sidebar
   - NO create-game / join-code buttons in the header

2) EVENT BANNER SLIDER (content width, directly under header) — REQUIRED
   - The ONLY place that actively promotes specific events/tournaments/new drops/challenges
   - ONE large rotating poster (~5s) + dots + prev/next arrows (admin-fed: image + link)
   - Each slide: poster image, optional date pill, short title, 1–2 lines, «Деталі» button
   - Not a slogan-only hero; not a journey progress bar
   - Sits over the portal panorama as a separate promo layer

3) THE PORTAL — THREE EQUAL DOORS (same visual weight)
   - One continuous hall with three doors; the doors ARE the navigation
   - Left door = warm gold light / clouds; center door = cool sky with stairs; right door = fire
   - NO labels «Рай» / «Чистилище» / «Пекло»
   - NO service titles «Соціальне» / «Події» / «Тренування»
   - NO bottom «path continues» timeline / Dante progress bar
   - Each entry = a floating pill node next to ITS door: icon + label + arrow

   LEFT DOOR (warm gold) — exactly two nodes:
     a) «Досягнення» (optional tiny progress like «124 з 400» — NOT a stats dashboard)
     b) «Усі ігри»
   CENTER DOOR (cool sky) — exactly two nodes:
     a) «Турніри»
     b) «Події»
   RIGHT DOOR (fire) — exactly three nodes:
     a) «Стендап»
     b) «Імпровізація»
     c) «Теорія»
   - Do NOT feature one concrete game or event inside the doors (promo lives in the banner)
   - Nodes must be functional product labels — NOT poetic Dante virtues
   - NO checklists, NO “practice today”, NO training progress bars

DENSITY
Home is a light navigation hub — not a dashboard.
Do NOT add: KPIs, friend activity, recommendations shelf, recent games,
leaderboards, badge walls, left sidebar, search, extra CTAs, or new modules.
Optional ONLY below the portal: «Популярні ігри» — never instead of the three doors.

Hierarchy the user must feel:
brand + profile → event banner → three equal doors
(achievements & games | tournaments & events | standup, improv, theory).

════════════════════════════════════════════════════════
ART DIRECTION — CHANGE THIS (the real job of this run)
════════════════════════════════════════════════════════
Previous concepts looked too serious, elegant, and “premium-cultural”.
That misses the product character.

PO KEEP signals (reuse the idea, not a specific past PNG):
- seamless climate blend across three zones (map / panorama)
- three unlabeled portals (cool / gold / dark) — very strong
- spatial functional nodes on a map-like surface

Target character for «Божественна комедія»:
- satire and comedy, not solemn luxury
- absurdity and self-irony
- theatrical / stage presence
- controlled chaos (alive, witty, a bit dangerous — still readable UI)
- modern 2025 product craft (usable components), but with comedic voltage

You MAY reinvent:
- color system, type pairing, textures, illustration accents
- how the three zones “feel” different without renaming them
- poster / slider visual language
- micro easter-eggs (tiny only — never the design system)
- Propose a DISTINCT visual take — diversity is wanted; do not clone one card template

You may use motifs from Divina Commedia ONLY as atmosphere:
light temperature, material, witty detail — NEVER medieval chrome,
angels/demons mascots, skull gothic kits, neon cyberpunk, or purple SaaS.
NEVER put «Пекло/Чистилище/Рай» labels or journey-path chrome in the UI.

AVOID
- museum / quiet-luxury / editorial-serious Apple-TV solemnity as the main mood
- identical boring rounded SaaS cards with yellow CTAs everywhere
- redesigning the IA “to make it cooler”
- left sidebar, search chrome, bottom path progress bar

SUCCESS
Same locked UX skeleton.
Completely different personality: funny, scenic, satirical, controlled chaos —
and still a clear modern web app.

Generate the image NOW.
```

---

## Версії

| Файл | Фокус |
|------|--------|
| v1–v3 | пошук UX (застарілі для генерації) |
| v4 | UX locked + character / art direction |
| v5 | PO feedback 2026-10-07: poster required, no sidebar/search, map/portals KEEP, diversity |
| **v6** | PO portal-v1 2026-10-07: `/` без лендінгу, двері = навігація (світлі: Досягнення · Усі ігри · холодні: Турніри · Події · вогняні: Стендап · Імпровізація · Теорія), два стани профілю, фон дзеркальний |

Ітерації після v6: міняй лише абзац ART DIRECTION (або короткий follow-up), **не** блок LOCKED IA.

### Mobile 390 (окремий кадр)
Той самий IA, композиція з `home-ux-locked.md` § Адаптив: header → банер (картинка 16:9, текст під нею) → три секції дверей стовпчиком (світлі → холодні → вогняні), у кожній шапка-кроп своїх дверей + вузли на всю ширину. Follow-up до промпту: `Same screen as mobile web 390×844, vertical stack: banner, then three door sections top-to-bottom (gold, sky, fire), full-width pill buttons.`  
Like/dislike: [`../../briefs/home-concepts-feedback.md`](../../briefs/home-concepts-feedback.md).
