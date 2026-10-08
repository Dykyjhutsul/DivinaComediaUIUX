# D08 — Афіша турніру (Tournament Poster)

Destination з Home (центр → «Деталі» на рядку турніру / slider) або з індексу подій (D02).  
Файл: `d08-tournament-poster-synth-v1.png` · Desktop **1440×900**  
Spec: **F-9.1** (view poster · VS-02 populated) · nav seeds **F-9.2** (map) · **F-9.3** (register) · **F-9.8** (participants list)  
Mock state: **VS-02 Poster populated** — місячний гумор-турнір «Жовтень 2026», статус `registration_open`, `registeredCount = 42`.

Пара до **D02** (індекс турнірів): D02 = список / мапа-вхід; D08 = **одна** публічна афіша конкретного Tournament.  
Не плутати з write-поверхнею реєстрації (`/purgatory/t/{id}/register` · F-9.3), списком ніків (F-9.8), раундами / голосуванням / результатами.

```text
ROLE
Art director + product UI for «Божественна комедія»: satirical monthly humor-tournament poster as a product page.
ONE desktop web-app screenshot 1440×900. Ukrainian UI.
Editorial stage / event energy — NOT esports neon brackets, NOT quiet luxury gala, NOT fantasy Dante, NOT admin CMS.

SEED: technical only if attached. Generate now. Do not change IA.

════════════════════════════════════════════════════════
LOCKED INFORMATION ARCHITECTURE — DO NOT CHANGE
════════════════════════════════════════════════════════

Mock = public Tournament Poster for ONE published platform tournament (monthly humor tournament).
Route vibe: /purgatory/t/{tournamentId} — featured or deep-linked.
THIS MOCK = registration_open, ready to navigate to register.
NOT registration form. NOT participants nickname roster as the main content.
NOT round answers / pairwise voting / results / awards. NOT CMS admin.

Public read — visitor may see the same poster without login.
Do NOT invent partner sponsor slots (out of v1).
Do NOT label the page «Чистилище» / «Рай» / «Пекло» as chrome (product language only).

1) HEADER (light chrome — same family as Home / D02)
   - Left: wordmark «Божественна комедія»
   - Right: profile avatar/icon (subtle; visitor-OK empty/guest vibe fine)
   - NO dense mega-nav of games/achievements
   - Quiet secondary nav OK:
     • «Назад» / «Усі турніри» → events index / map entry (F-9.2)
     • optional breadcrumb feel — keep light

2) POSTER HERO — title + status + key dates (dominates first scroll)
   Must include:
   a) Tournament TITLE — example locked for this mock: «Жовтень 2026»
      (month/season name OK; theatrical poster type)
   b) Status chip / label: «Реєстрація відкрита» (status = registration_open)
      Do NOT invent esports “LIVE BRACKET” chrome
   c) Schedule block — dates in UI form DD.MM.YYYY HH:mm (Kyiv vibe), compact:
      - Відкриття реєстрації
      - Закриття реєстрації
      - Старт турніру
   - This is a discovery poster, not a calendar app

3) CONTENT BLOCKS (CMS-fed copy — scannable sections, not a novel)
   Show these as clear sections (short Ukrainian copy OK — invent plausible comedy-night tone):
   a) Формати — short format description (how the tournament works)
   b) Правила перемоги — how winners are determined
      (advancement vibe OK at high level: e.g. відсів ~30% + wildcard —
       do NOT build a rules wiki or formula spreadsheet)
   c) Призи — compact prizes blurb (places / recognition — not a shop)
   d) Етапи — stages R1 · R2 · R3 as a timeline / list
      Each stage: title + optional date window
      Example OK: R1 «Панчі до сетапів» · R2 «Сетапи до панчів» · R3 «Фінал»
   - If a block feels optional/empty — omit the empty section; do NOT show error shells
   - NO partner logo row

4) REGISTERED COUNT + participants entry (aggregate only on poster)
   - Show public count: e.g. «42 зареєстрованих» (registeredCount)
   - Affordance to open the public participants list: «Список учасників» / «Хто вже в грі»
     (navigation to F-9.8 — NOT a faces strip owning the page)
   - Do NOT render a full nickname roster / avatar wall as the hero
   - Do NOT invent places/ranks on this mock (history awards = other surfaces)

5) PRIMARY CTA ZONE (navigation only — this feature does not write)
   - Primary: «Зареєструватись» — enabled because status = registration_open
     (navigates to registration surface F-9.3; does NOT complete register on this screen)
   - Secondary quiet links OK:
     • «Мапа турнірів» / «Усі турніри» (F-9.2)
     • «Список учасників» (F-9.8) if not already next to the count
   - Do NOT put «Скасувати участь», «Нагадування», «Додати в календар»
     as poster-owned primary chrome on THIS mock
     (those live in the registration contour after the user is registered — F-9.4 / F-9.5 / F-9.7)
   - Do NOT invent login modal as the whole composition
     (auth gate belongs to register write, not poster read)

6) WHAT MUST NOT APPEAR
   - Full participants nickname grid / face strip as main content (F-9.8 owns that)
   - Registration confirmation form / “you are registered” success state (F-9.3)
   - Cancel / email reminder / Telegram / .ics calendar as poster primary actions
   - Answer session, pairwise vote UI, round results, final awards podium
   - Partner sponsor slots, UGC “create your tournament”
   - Esports bracket tree, neon tournament HUD, medieval Dante zone titles
   - Dense admin metrics, KPI cards, friend activity feed

Hierarchy the user must feel:
TITLE + status → key dates → formats / rules / prizes / R1–R3 stages →
registered count → «Зареєструватись» → quiet back to all tournaments / map.

════════════════════════════════════════════════════════
ART DIRECTION
════════════════════════════════════════════════════════
Warm amber / theatrical poster climate (Home center column energy).
Strong typography — almost no borders. Comedy + self-irony in copy tone;
still a clear modern product page (usable sections, obvious CTA).
Spotlight / stage / event ring atmosphere OK as texture —
NOT gothic angels, NOT purple SaaS glow, NOT esports neon.

Generate NOW.
```
