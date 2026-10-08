# D05 — Лобі кімнати (Host)

Після create room (`F-5.1`) → host shell. Dual-purpose: control panel + TV/stream readable.  
Файл: `d05-lobby-host-synth-v1.png` · Desktop **1440×900**  
Spec: **F-5.2** (view) · **F-5.7** (settings) · **F-5.9** (start) · BR-ROOM-011/013/017 · BR-GAME-006/007  
Mock state: **VS-02 Default — lobby populated**, Start blocked (не всі Ready).

```text
ROLE
Art director + product UI for «Божественна комедія»: theatrical comedy night host console.
ONE desktop web-app screenshot 1440×900. Ukrainian UI.
Readable from a distance (TV / stream / projector) — code & QR dominate.
NOT arcade HUD. NOT admin CRM. NOT quiet luxury dashboard. NOT fantasy Dante.

SEED: technical only if attached. Generate now. Do not change IA.

════════════════════════════════════════════════════════
LOCKED INFORMATION ARCHITECTURE — DO NOT CHANGE
════════════════════════════════════════════════════════

Mock = Host lobby waiting room (Room status: lobby). NOT the in-session dashboard.
NOT fullscreen “TV-only code” mode (out of MVP). NOT player mobile lobby.

1) HEADER (light chrome)
   - Left: wordmark «Божественна комедія» OR minimal room context
   - Right: host profile avatar (subtle)
   - NO main-site nav (no Ігри / Події / Досягнення mega-nav)
   - Optional secondary host action: «Закрити кімнату» (quiet, destructive-soft) — NOT a dense toolbar

2) INVITE ZONE — the hero of the screen (spotlight)
   Must dominate visual hierarchy:
   a) Room CODE — very large, monospace-friendly display
      - Exactly 6 characters, uppercase A–Z / 0–9 only
      - Example for this mock: «ABC123»
      - Affordance: «Копіювати код» (copy)
   b) QR code — large enough to scan from a phone across a table
      - Encodes join deep link (conceptually https://…/room/ABC123)
      - Client-rendered QR — no fake “scan in app” chrome
   c) Join link row (secondary): short URL / «Копіювати посилання»
   - Code + QR are Host-only invite tools (players never see this on their lobby)

3) PARTICIPANT ROSTER
   - Title like «Учасники» + live count (e.g. 5)
   - Order: by join time ascending
   - Each row: avatar (or nickname initial fallback) + nickname
   - Host row ALWAYS present with clear label «ведучий» (not a separate admin panel)
   - Ready states per participant (Ready Check — required before Start):
       · «Готовий» / ready — distinct, scannable
       · «Чекає» or «Не готовий» — distinct from ready
   - This mock: Host ready + mix of ready / not-ready among ~3–4 Players
     (enough people for the selected game’s min, but Start still blocked by Ready)
   - Do NOT invent kick/ban chrome as the main UI
   - Do NOT show empty-error if Host alone — that would be VS-03; this mock is populated

4) SELECTED GAME SUMMARY (not the full catalog)
   - Card / block with: game name + short meta (players min–max)
   - This mock: «Never Have I Ever» · meta like «3–20 гравців»
   - Secondary CTA into catalog: «Змінити гру» or «Каталог ігор»
   - If no game were selected, UI would say «Гру не обрано» + CTA to catalog —
     but THIS mock HAS a selected game
   - NOT a grid of all games. NOT Steam-style store shelf

5) SESSION SETTINGS (Host-editable entry — keep simple)
   Framework lobby params shown (Quiz/Sinner-style каркас; readable on lobby):
   - «Кількість питань»: integer 5–20 — this mock shows e.g. 10
   - «Таймер питання»: discrete values only — 0 / 30 / 60 / 120 / 300 сек
     (0 = без таймера). This mock shows e.g. 60 сек
   - Simple controls (stepper / segmented / select) — NOT a dense form wizard
   - Entry may look like inline controls or «Налаштування» that reveals them
   - Do NOT invent game-specific filters here (NHIE categories live elsewhere)
   - Players never see or edit these fields

6) PRIMARY START
   - One big primary CTA: «Старт» or «Запустити гру»
   - THIS MOCK: Start looks disabled / waiting
   - Visible reason near CTA (one short line), e.g.:
     «Чекаємо, поки всі будуть готові»
   - Do NOT show an enabled green Start that implies the game already began
   - Other block reasons exist in product (no game / too few / too many / empty bank / 18+)
     — do NOT stack all of them; Ready wait is enough for this frame

7) WHAT MUST NOT APPEAR
   - Round prompts, round timer, scoring, Next Question, host dashboard chrome
   - Player-only Ready button as the main CTA (Host console ≠ player phone)
   - Full game catalog grid
   - KPI cards, friend activity, CRM tables, purple SaaS glow
   - Medieval / angel-demon mascots as UI chrome

Hierarchy the user must feel from across the room:
CODE + QR → who’s in + ready → selected game → settings → Start (waiting).

════════════════════════════════════════════════════════
ART DIRECTION
════════════════════════════════════════════════════════
Stage/show energy — spotlight on code+QR.
Controlled chaos in texture/type; still crystal-clear hierarchy.
Matte dark + warm accent. No neon arcade. No quiet-luxury museum calm.
Same character family as Home / catalog — comedy night host desk, not Discord admin.

Generate NOW.
```
