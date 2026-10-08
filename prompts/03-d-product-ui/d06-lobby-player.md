# D06 — Лобі кімнати (Player)

Після join за QR / deep link (`F-5.5`) → mobile player shell. Чекає старту від ведучого.  
Файл: `d06-lobby-player-synth-v1.png` · Mobile **390×844**  
Spec: **F-5.3** (view) · Ready Check каркаса (**BR-ROOM-017**, гра-плагін) · selected game read-only  
Mock state: **VS-01 Default — очікування зі складом**, гра обрана, цей гравець ще **не Ready**.

Пара до **D05** (Host desktop): той самий character family, інша поверхня — телефон гравця, не TV-консоль ведучого.

```text
ROLE
Art director + product UI for «Божественна комедія»: waiting-to-play comedy energy on a phone in hand.
ONE mobile web-app screenshot 390×844. Ukrainian UI.
Thumb-first. Same character family as Host lobby (D05) — simpler, tighter, no invite theatre.
NOT host console. NOT arcade HUD. NOT Discord admin. NOT solemn premium. NOT fantasy Dante.

SEED: technical only if attached. Generate now. Do not change IA.

════════════════════════════════════════════════════════
LOCKED INFORMATION ARCHITECTURE — DO NOT CHANGE
════════════════════════════════════════════════════════

Mock = Player lobby waiting room (Room status: lobby). Mobile-first player shell.
Route vibe: /room/ABC123/lobby — player already joined.
NOT Host desktop lobby. NOT in-session round UI. NOT join/landing form.

1) HEADER (light chrome)
   - Left: wordmark «Божественна комедія» OR minimal room context
     (optional quiet crumb like «Лобі» — NOT large room CODE)
   - Right: player profile avatar (subtle)
   - NO main-site nav (no Ігри / Події / Досягнення)
   - Optional quiet secondary: «Покинути кімнату» — soft, not competing with Ready
   - NO «Закрити кімнату» (host-only). NO kick / ban chrome

2) WAITING HERO — the emotional center (replaces Host invite zone)
   Must dominate visual hierarchy on the phone:
   - Clear waiting message that Host has not started yet, e.g.:
     «Очікуємо старту» / «Ведучий скоро запустить гру»
   - Optional short supportive line — comedic, not anxious
   - Do NOT show room CODE, QR, or join URL (Host-only invite tools — never on player lobby)
   - Do NOT invent a fake “scan to invite friends” panel

3) SELECTED GAME (read-only)
   - If Host already picked a game: show name + short meta (players min–max)
   - This mock HAS a selected game: «Never Have I Ever» · «3–20 гравців»
     (same game as Host D05 mock — parity)
   - Read-only — NO «Змінити гру», NO catalog CTA, NO settings gear
   - Do NOT show question count / timer fields (Host-only session params)

4) PARTICIPANT ROSTER
   - Title like «Учасники» + live count (this mock: ~4–6 people — phone-friendly, not a 20-card wall)
   - Order: by join time ascending
   - Each row: avatar (or nickname initial fallback) + nickname
   - Host row ALWAYS present with clear label «ведучий»
   - Current user (this phone’s player) clearly marked — «ти» / highlight / isCurrentUser
   - Ready states visible (parity with Host roster — Ready Check before Start):
       · «Готовий» — distinct, scannable
       · «Чекає» / «Не готовий» — distinct from ready
   - This mock: Host + mix of ready / not-ready; CURRENT USER is not ready yet
   - NO remove / kick «X» on rows (host-only)

5) PRIMARY READY CTA (thumb zone)
   - ONE big primary button pinned for thumb: «Готовий» (or «Я готовий»)
   - THIS MOCK: player has NOT marked Ready yet → CTA enabled / inviting
   - After Ready (not this frame): state would flip to waiting-on-host copy —
     do NOT invent a second competing primary
   - NO «Запустити гру» / «Старт» (host-only)
   - NO host settings entry

6) WHAT MUST NOT APPEAR
   - Room code, QR, join link / «Копіювати код|посилання»
   - Session settings (question count, timer steppers)
   - Start / Kick / Close-room / Change-game / Catalog grid
   - Round prompts, scoring, Next Question, host dashboard chrome
   - KPI cards, friend activity, CRM tables, purple SaaS glow
   - Medieval / angel-demon mascots as UI chrome
   - Dense 20-seat grid that belongs on Host TV — keep roster scannable on 390

Hierarchy the player must feel in one thumb-scroll:
WAITING → who’s here + ready → selected game (read-only) → big Ready.

════════════════════════════════════════════════════════
ART DIRECTION
════════════════════════════════════════════════════════
Same stage/show climate as Host lobby — matte dark + warm accent —
but intimate phone scale: spotlight on waiting + Ready, not on code+QR.
Controlled chaos in texture/type; crystal-clear thumb hierarchy.
No neon arcade. No quiet-luxury museum calm.
Comedy night guest seat, not host desk.

Generate NOW.
```
