# D07 — Почата гра (Host · live round)

Після Start (`F-5.9`) → Host desktop/TV in-session. Каркас сесії + game-round plug-in.  
Файл: `d07-active-game-synth-v1.png` · Desktop **1440×900**  
Spec: **F-5.16** (host in-session shell) · **F-6.1** V-5 Question round host (**VS-13**) · Live Reactions (**F-6.30** / BR-GAME-015)  
Mock state: **round_in_progress** — Never Have I Ever, раунд 2/10, таймер іде, Host ще не відповів.

Пара до **D05** (Host lobby): той самий character family і кімната `ABC123` / гра NHIE — тепер уже **active session**, не waiting room.  
Не плутати з Player mobile round (`F-5.17` / F-6.1 V-4) — той окремий телефонний кадр; цей слот = **TV/stream ведучого**.

```text
ROLE
Art director + product UI for «Божественна комедія»: live comedy-night round on the host screen / TV.
ONE desktop web-app screenshot 1440×900. Ukrainian UI.
Readable from a distance (TV / stream / projector) — PROMPT dominates, not chrome.
NOT arcade HUD. NOT Twitch overlay pack. NOT fantasy battle UI. NOT Discord admin.
NOT quiet luxury. NOT medieval Dante.

SEED: technical only if attached. Generate now. Do not change IA.

════════════════════════════════════════════════════════
LOCKED INFORMATION ARCHITECTURE — DO NOT CHANGE
════════════════════════════════════════════════════════

Mock = Host in-session dashboard + NHIE round plug-in (Room status: active).
Route vibe: /room/ABC123/session (host) — game already started.
NOT lobby (D05). NOT player phone round. NOT round results. NOT final leaderboard.
NOT fullscreen “TV-only code” mode (out of MVP).

1) HEADER (light chrome)
   - Left: wordmark «Божественна комедія» OR minimal session context
     (game name chip OK: «Never Have I Ever»)
   - Right: host profile avatar (subtle)
   - NO main-site nav (no Ігри / Події / Досягнення mega-nav)
   - Quiet secondary host action: «Завершити гру» / «End Game»
     (destructive-soft, confirm-implied — NOT competing with the prompt)
   - NO «Закрити кімнату» as primary (lobby-era). NO kick chrome as main UI

2) SESSION META STRIP (secondary — scannable, not the hero)
   Must be readable but NEVER overpower the prompt:
   a) Round counter: «Раунд 2 / 10» (current / total — totalRounds = questionCount)
   b) Timer: visible countdown, e.g. «0:42» or circular/linear residual —
      THIS MOCK has timer ON (questionTimerSec = 60). Soft urgency, NOT arcade bomb.
      Do NOT invent a huge FPS-style HUD timer.
   c) Participant count: e.g. «6 учасників» (or compact avatar stack)
   d) Late-join invite tools — Host-only, compact (not lobby-hero scale):
      - Room CODE «ABC123» (6 chars A–Z/0–9) + copy affordance
      - Small QR or «Копіювати посилання» — smaller than D05 invite zone
   - Phase label optional/quiet: «Раунд у прогресі»
   - Do NOT show «Перемкнути гру» enabled — switch is ONLY between rounds
   - Do NOT show lobby Ready check / Start CTA (game already live)

3) PROMPT ZONE — the hero of the screen (spotlight)
   Must dominate visual hierarchy from across the room:
   - Prefix locked by product: «Я ніколи…»
   - Then ONE Achievement statement (readable large type)
     Example OK: «Я ніколи… не співав караоке до ранку»
     (or similar adult-party Ukrainian line — one clear sentence)
   - This is the game-round plug-in content — theatrical focus light on the text
   - Optional quiet meta under prompt: category / difficulty — tiny, not competing
   - Do NOT show full answer reveal / who said what (that is Round Results — not this mock)
   - Do NOT invent multi-choice Quiz cards or vote grids as the main pattern

4) HOST ACTION ZONE (Yes / No — Host plays too)
   Host is an active player and answers the same way as Players:
   - TWO clear actions: «Так» | «Ні»
   - THIS MOCK: Host has NOT answered yet → both enabled / inviting
   - After answer (not this frame): would lock + wait for others —
     do NOT invent a second competing primary
   - Optional quiet progress: «Відповіли 2 з 6» or nicknames still waiting —
     subtle, not a CRM table
   - NO «Наступне питання» / Next Question on THIS mock
     (Next Question appears only after Round Results — Host-only then)

5) LIVE REACTIONS (optional thin strip — keep subtle)
   - Small emoji reaction tray / floating chips from CMS catalog
   - Ambient comedy energy — reactions do NOT change score or Так/Ні
   - Do NOT make this a Twitch donation overlay or sticker spam wall
   - Karma cost chrome may be tiny or omitted in this synth frame

6) WHAT MUST NOT APPEAR
   - Lobby Ready / Start / «Змінити гру» catalog grid / settings steppers
   - Round Results full reveal (yesCount/noCount per nickname as the main screen)
   - Final leaderboard / Play Again
   - Player-only mobile chrome as the whole composition
   - Enabled «Перемкнути гру» during round_in_progress
   - Dense admin tables, KPI cards, friend activity, purple SaaS glow
   - Medieval / angel-demon mascots as UI chrome
   - Neon arcade health bars, combo meters, boss HP

Hierarchy the room must feel from across the stage:
PROMPT («Я ніколи…») → Так/Ні → round+timer meta → quiet host end + compact code.

════════════════════════════════════════════════════════
ART DIRECTION
════════════════════════════════════════════════════════
Same stage/show climate as Host lobby (D05) — matte dark + warm accent —
but higher tension: spotlight on the prompt, controlled chaos in atmosphere.
Comedy night mid-show energy; still crystal-clear readability under pressure.
No neon arcade. No quiet-luxury museum calm. No Twitch streamer HUD.

Generate NOW.
```
