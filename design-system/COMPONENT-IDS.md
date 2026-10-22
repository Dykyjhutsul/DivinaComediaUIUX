# COMPONENT-IDS — реєстр компонентів UI Kit

> Version: 1.12 · 2026-10-09 (лобі F-5.2: ROOM-028…029, 031, 032 зібрані локально) · попередньо 1.11 (028…031 ще без Figma node) · Figma: [DivinaComediaUIKit](https://www.figma.com/design/7VS64TZ3mjVvxoaYF6ZHDk/DivinaComediaUIKit?node-id=0-1) (`fileKey 7VS64TZ3mjVvxoaYF6ZHDk`)
> Джерела: BA [`docs/design/figma-make-moodboards-uikit.md`](../../DivinaComedia/docs/design/figma-make-moodboards-uikit.md) · [`briefs/screens-ux.md`](../briefs/screens-ux.md) · [`briefs/home-ux-locked.md`](../briefs/home-ux-locked.md) · D-промпти [`prompts/03-d-product-ui/`](../prompts/03-d-product-ui/)
> Поверхня: **Front (Web)** — desktop 1440 (host / TV) · mobile 390 (player). CMS — поза kit (збирається з бібліотеки компонентів).

## Правила

- **ID:** `DC-{LAYER}-{NNN}`. Номер ніколи не перевикористовується; виведений компонент лишається в таблиці з `Priority = retired`.
- **Новий компонент** — наступний вільний номер у шарі + рядок тут у тій самій сесії, що й збірка у Figma.
- **Ім'я у Figma:** `DC-BASE-001 / Button` (ID + англійська назва з колонки `Name`). Component Set на ID; варіанти — через properties, не дублікати фреймів.
- **Properties:** `variant` · `size` · `state` (+ доменні, напр. `zone`, `ready`). Стани інтерактивних: `default / hover / focus / pressed / disabled / loading / error`.
- **Токени:** у компонентах лише bound Variables — без hex. Значення приходять зі [`style-lock/STYLE-LOCK.md`](../style-lock/STYLE-LOCK.md).
- **Копірайт у прикладах:** українською.
- **Композити** збираються з інстансів BASE, не з копій.
- **Priority:** `P1` — MVP-хвиля · `P2` — друга хвиля після затвердження напряму · `retired` — не будувати.
- **Figma node** — заповнюється після збірки (`node-id`).

## Шари

| Префікс | Шар | Сторінка Figma |
|---------|-----|----------------|
| `DC-FND` | Foundations (Variables / styles) | `00 Foundations` |
| `DC-BASE` | Атоми | `01 Base` |
| `DC-FB` | Feedback / overlays | `02 Feedback` |
| `DC-NAV` | Shell / навігація | `03 Navigation` |
| `DC-HOME` | Home-композити (Home LOCK) | `03 Navigation` |
| `DC-AUTH` | Auth & profile | `04 Domain` |
| `DC-ACH` | Досягнення | `04 Domain` |
| `DC-ROOM` | Кімната / лобі / сесія | `04 Domain` |
| `DC-STD` | Стендап / теорія / імпро | `04 Domain` |
| `DC-TRN` | Турнір | `04 Domain` |
| `DC-MISC` | Спільні патерни | `05 Blocks` |

## План сторінок Figma

| Сторінка | Вміст |
|----------|-------|
| `00 Foundations` | Variable collections (`Primitives`, `Color` (mode `Dark`), `Zone` з modes `Default` / `Paradise` / `Purgatory` / `Inferno`, `Spacing`, `Radius`, `Size`), text styles, effect styles, specimen-фрейми, іконки |
| `01 Base` | `DC-BASE-*` |
| `02 Feedback` | `DC-FB-*` |
| `03 Navigation` | `DC-NAV-*` + `DC-HOME-*` |
| `04 Domain` | секції `AUTH` · `ACH` · `ROOM` · `STD` · `TRN` |
| `05 Blocks` | готові складені ряди / кластери (`DC-MISC-*`, повторювані комбінації) — не екрани |
| `99 Examples` | smoke-екрани лише з інстансів: D05 Host lobby · D06 Player lobby · D07 Host session · D07 Player answer · D08 Tournament · D01 Home |

---

## DC-FND — Foundations

| ID | Name | Що містить | Priority | Source | Figma node |
|----|------|-----------|----------|--------|------------|
| DC-FND-001 | Color | bg · surface · elevated · border · text primary/secondary/disabled · primary · danger · success · warning; P2: `accent/pressed` `20:222` · `bg/pressed` `20:223` (похідні, не зі styleguide) | P1 | BA kit §1 | `3:2 ? 3:24` |
| DC-FND-002 | Zone accents | клімат Рай · Чистилище · Пекло як modes `Zone` (`zone/accent`, `zone/accent-subtle`, `zone/void`, `zone/card`, `zone/card-border`); одна система кнопок/радіусів/типу | P1 | BA kit §1 · CLAUDE.md #4 · Paradise PO 2026-10-08 | `3:48` |
| DC-FND-003 | Typography | Display · H1–H3 · Body L/M · Label · Caption · Mono (код кімнати, таймер, рахунок) | P1 | BA kit §1 | `4:2` |
| DC-FND-004 | Spacing | 4 · 8 · 12 · 16 · 24 · 32 · 48 | P1 | BA kit §1 | `3:51` |
| DC-FND-005 | Radius | кнопка · інпут · картка · pill | P1 | BA kit §1 | `3:59` |
| DC-FND-006 | Elevation | card · modal · toast · host overlay | P1 | BA kit §1 | `4:2` |
| DC-FND-007 | Icons | P2+ (F-2.2, лише локальна копія `8itQZ…`): pause `318:135` · play `318:139`; nav · close · search · filter · vote · timer · copy · QR · leave · settings · arrow · check; P2: eye `21:5` · eye-off `21:11` · chevron-down `21:14` · settings `21:20` · mail `21:24` · edit `21:28` · trash `21:34` · lock `21:38` · mic `21:42` · heart `21:45` · smile `21:51` · crown `21:54` · refresh `21:58` · shuffle `21:65` · send `21:69` · link `21:73` · more `21:78` · flag `21:82` | P1 | BA kit §1 | `5:2` |
| DC-FND-008 | Motion | press · focus ring · timer tick · toast in/out — правила | P2 | BA kit §1 | `25:2` |
| DC-FND-009 | Breakpoints | 1440 host / 390 player — правила масштабування | P2 | BA kit §1 | `25:39` |

## DC-BASE — Base

| ID | Name | Variants / properties | Priority | Source | Figma node |
|----|------|----------------------|----------|--------|------------|
| DC-BASE-001 | Button | `variant` primary/secondary/ghost/danger · `size` sm/md/lg · `state` default/hover/focus/pressed/disabled/loading | P1 | BA kit §2 | `6:2` |
| DC-BASE-002 | Icon Button | `variant` ghost/secondary · `size` · `state` · icon swap | P1 | BA kit §2 | `7:122` |
| DC-BASE-003 | Link | inline / standalone · `state` | P2 | BA kit §2 | `22:283` |
| DC-BASE-004 | Input | label · hint · error text · `state` default/focus/error/disabled | P1 | BA kit §2 | `8:222` |
| DC-BASE-005 | Textarea | + лічильник символів · `state` | P1 | BA kit §2 · F-7.7 · F-9.9 | `8:253` |
| DC-BASE-006 | Email / Password Field | auth-варіанти Input | P2 | F-1.1 · F-1.2 | `22:308` |
| DC-BASE-007 | Select | closed/open · `state` | P2 | BA kit §2 | `22:375` |
| DC-BASE-008 | Checkbox | checked/unchecked · `state` | P2 | BA kit §2 | `22:407` |
| DC-BASE-009 | Radio | selected/unselected · `state` | P2 | BA kit §2 | `22:435` |
| DC-BASE-010 | Switch | on/off · `state` | P1 | F-9.5 | `9:194` |
| DC-BASE-011 | Tabs | segmented / underline · active | P1 | BA kit §2 | `9:214 (+ Tab 9:207)` |
| DC-BASE-012 | Chip | filter/tag/status · selected · `zone` | P1 | BA kit §2 · D04 | `7:234` |
| DC-BASE-013 | Badge | live/new/count/neutral | P1 | BA kit §2 | `7:219` |
| DC-BASE-014 | Avatar | image / initials fallback · `size` | P1 | F-5.3 EC-06 | `8:170` |
| DC-BASE-015 | Avatar Stack | 3/5/+N | P1 | BA kit §2 · D07 | `8:213` |
| DC-BASE-016 | List Row | leading · title + meta · trailing action | P1 | BA kit §2 | `9:221` |
| DC-BASE-017 | Divider | horizontal / vertical | P2 | BA kit §2 | `22:457` |
| DC-BASE-018 | Skeleton | text / block / avatar | P1 | VS Loading у всіх спеках | `9:264` |
| DC-BASE-019 | Spinner | inline / page | P1 | BA kit §2 | `9:269` |
| DC-BASE-020 | Tooltip | top/bottom | P2 | BA kit §2 | `22:460` |

## DC-FB — Feedback & overlays

| ID | Name | Variants / properties | Priority | Source | Figma node |
|----|------|----------------------|----------|--------|------------|
| DC-FB-001 | Toast | success/error/info · close; поява 400ms ease-out · hold 2.4s · зникнення 150ms ease-in; F-4.6 write = toast, не банер | P1 | BA kit §3 · F-4.6 | kit `12:2` · local `395:9642` |
| DC-FB-002 | Banner | info/warning/danger (18+, Sinners, untranslated, GA down) | P1 | BA kit §3 · F-11.2 | `12:40` |
| DC-FB-003 | Dialog | confirm / destructive | P1 | BA kit §3 · F-9.4 | `12:89` |
| DC-FB-004 | Bottom Sheet | 390: фільтри, налаштування | P2 | BA kit §3 | `23:84` |
| DC-FB-005 | Empty State | icon · title · text · CTA | P1 | VS Empty у спеках | `12:136` |
| DC-FB-006 | Error State | title · text · retry | P1 | VS System error у спеках | `12:154` |
| DC-FB-007 | Loading Overlay | lobby sync / reconnect | P2 | BA kit §3 | `23:124` |

## DC-NAV — Navigation & shell

| ID | Name | Variants / properties | Priority | Source | Figma node |
|----|------|----------------------|----------|--------|------------|
| DC-NAV-001 | Top Bar / Home | wordmark «Божественна комедія» + avatar; `Size` 1440/390 · `Surface` Solid/Ghost (Ghost — на атмосфері Раю / порталі) | P1 | home-ux-locked §1 · Paradise PO 2026-10-08 | `14:2` |
| DC-NAV-002 | Top Bar / Inner | back + context title + avatar · `size` 1440/390 | P1 | screens-ux | `14:19` |
| DC-NAV-003 | Top Bar / Host | wordmark або room context + avatar + quiet destructive action | P1 | D05 · D07 | `14:40` |
| DC-NAV-004 | Mobile Action Bar | player 390, sticky bottom CTA | P2 | D06 | `24:182` |
| DC-NAV-005 | Back Link | drill → hub · `Label` (F-4.3: «Досягнення») | P2 | BA kit §4 · F-4.3 | `24:206` |
| DC-NAV-006 | Account Menu | profile · logout · delete account | P2 | BA kit §4 | `24:217` |
| DC-NAV-007 | Zone Nav Pills | — | retired | Home LOCK: зони = клімат, не tabs | |

## DC-HOME — Home composites

| ID | Name | Variants / properties | Priority | Source | Figma node |
|----|------|----------------------|----------|--------|------------|
| DC-HOME-001 | Featured Poster | single large (ротація ≈5 с) / strip ~3 · заголовок + 1–2 рядки + «Деталі» | P1 | home-ux-locked §2 | `15:44` |
| DC-HOME-002 | Carousel Controls | dots · arrows · pause / play (F-2.2 C-5) | P2 | home-ux-locked §2 · F-2.2 | `24:247` (pause — лише локальна копія `8itQZ…` `319:272`) |
| DC-HOME-003 | Zone Column / Left | Досягнення (± «124 з 400») + Ігри | P1 | home-ux-locked §3 · F-2.3 | `15:108 (+ Zone Entry 14:61)` |
| DC-HOME-003a | Zone Entry | icon · назва · опис · ± progress micro · arrow; колір = `zone/accent` батька | P1 | home-ux-locked §3 · styleguide §04 | `14:61` |
| DC-HOME-004 | Zone Column / Center | турніри (назва · дата · Деталі) + «Усі турніри» | P1 | home-ux-locked §3 · F-2.3 | `15:145` |
| DC-HOME-005 | Zone Column / Right | Стендап · Імпровізація · Теорія | P1 | home-ux-locked §3 · F-2.3 | `15:173` |
| DC-HOME-006 | Tournament Teaser Row | назва · дата · «Деталі» | P1 | home-ux-locked §3 | `14:79` |
| DC-HOME-007 | Progress Micro | «X з Y» | P2 | home-ux-locked §3 | `24:289` |
| DC-HOME-008 | Popular Games Strip | лише під трьома зонами | P2 | home-ux-locked (опційно) | `24:296` |
| DC-HOME-009 | Portal Node | плашка-перехід на фоні порталу: icon у колі `zone/accent` · label · arrow; `Icon` swap · `Label` · `Show arrow` (вимкнено = неактивний перехід, F-2.2 C-14) | P1 | home-ux-locked (portal-v1) · F-2.2 | у kit ще немає — лише локальна копія `8itQZ…` `320:218` |

## DC-AUTH — Auth & profile

| ID | Name | Variants / properties | Priority | Source | Figma node |
|----|------|----------------------|----------|--------|------------|
| DC-AUTH-001 | Auth Form | OAuth buttons · errors | P2 | F-1.1 · F-1.2 | `40:1274` |
| DC-AUTH-002 | Nickname Field | правила унікальності | P2 | F-1.1 | `40:1350` |
| DC-AUTH-003 | Profile Header | own (з email); праворуч «Вийти» + «Деактивувати акаунт»; без edit CTA | P2 | F-3.1 | kit `40:1386` · local `401:1316` |
| DC-AUTH-004 | Profile Stats Strip | вечори · drills · турніри | P2 | BA kit §5 | `40:1397` |
| DC-AUTH-005 | Public Profile Header | без email | P2 | BA kit §5 | `40:1392` |
| DC-AUTH-006 | Achievement Showcase Grid | Completed на профілі: title · category · difficulty · «Виконали N%»; `State` Filled/Empty · `Size` Desktop/Mobile; без «Усі ачівки» і без write. Картка `Showcase Item` (`401:1332`): опційні `Date` + `Show date` (default off — F-3.1 без дати) | P2 | F-3.1 C-3/C-6 · F-4.7 | kit `40:1407` · local `401:1535` |
| DC-AUTH-007 | Avatar Preset Picker | preset-only (6 кіл); `State` Default / Selected / Error; без upload у v1 | P2 | F-3.2 C-7 | local `405:1769` (у kit ще немає) |

## DC-ACH — Achievements

| ID | Name | Variants / properties | Priority | Source | Figma node |
|----|------|----------------------|----------|--------|------------|
| DC-ACH-001 | Category Card | без стрілки · icon 24 у wrap 32 (без clip) · назва (max 2 рядки) · «X з Y» + bar FILL · Compact 390: 4:3 (173×130), icon → назва → meta по центру · `State` Auth/Guest · `Size` Default/Compact | P1 | F-4.2 · D03 · Paradise PO 2026-10-08 | `17:195` |
| DC-ACH-002 | Achievement Item | title на всю ширину · meta-ряд: складність · «Виконали N%» · spacer FILL · статус/дія справа; `State` Not Confirmed / Confirmed / Guest | P2 | BA kit §6 · F-4.3 · F-4.6 | `38:1216` |
| DC-ACH-003 | Achievement Action | у meta-рядку справа: «Підтвердити» / Confirmed = лише галочка + icon cancel (без тексту «Підтверджено», без модалки); Confirming / Cancelling = spinner | P2 | BA kit §6 · F-4.3 C-12 · F-4.6 | `38:1155` |
| DC-ACH-004 | Difficulty Filter | dropdown Closed/Open; `Show caption`; Field FILL (не FIXED 200); 1440 = caption + HUG 200; 390 = без caption, два FILL у рядку з gap 10 | P2 | BA kit §6 · F-4.3 | `70:1398` |
| DC-ACH-005 | Status Filter | dropdown Closed/Open; `Show caption`; Field FILL; 390 = без caption, FILL у парі (value truncate ENDING) | P2 | BA kit §6 · F-4.3 | `70:1399` |
| DC-ACH-006 | Scoped Search | у категорії / теорії; не на Home | P2 | BA kit §6 · F-8.1 | `38:1275` |
| DC-ACH-007 | Suggestion Form | `State` Default / Loading / Prefill / NewCategory / Validation / SystemError / Success · наявна або нова категорія · textarea ≤200 · складність · CTA Size L «Надіслати» / «Скасувати»; SystemError: банер стовпчиком | P2 | BA kit §6 · F-4.10 | kit `98:3365` · local `388:1423` |
| DC-ACH-008 | Sinners Entry | pill: зірка · «Грішники» · стрілка; `accent/default` червоний (навпаки від ACH-011); не картка в сітці | P2 | F-4.2 · screens-ux §05 · Paradise PO 2026-10-08 | `38:1355` |
| DC-ACH-009 | Swipe Card | confirm / reject | P2 | BA kit §6 | `38:1366` |
| DC-ACH-010 | Atmosphere Field | `Crop` Desktop 1440 / Mobile 390 — дерево Раю на `zone/void`; абсолютний page bg, не chrome | P1 | F-4.2 · STYLE-LOCK Paradise | `76:2909` |
| DC-ACH-011 | Suggest Entry | pill: plus · «Запропонувати ачівку» (390: «Запропонувати») · `text/primary` кремовий → F-4.10 | P2 | F-4.2 · F-4.3 toolbar · F-4.10 T-1 | `80:1382` |
| DC-ACH-012 | Atmosphere Sinners | `Crop` Desktop 1440 / Mobile 390 — кривавий місяць, замок, троянди; абсолютний page bg категорії «Грішники», не chrome | P1 | F-4.13 · PO 2026-10-08 | local `435:1386` |
| DC-ACH-013 | Atmosphere Paradise Spiral | `Crop` Desktop 1440 / Mobile 390 — золота спіраль-гелікс на `zone/void`; абсолютний page bg категорій Раю F-4.3 / F-4.6 / F-4.10 (≠ дерево DC-ACH-010, що лишається для F-4.2) | P1 | F-4.3 · PO 2026-10-08 | kit `106:2249` · local `444:1383` |

## DC-ROOM — Game framework

| ID | Name | Variants / properties | Priority | Source | Figma node |
|----|------|----------------------|----------|--------|------------|
| DC-ROOM-001 | Room Code | 6 символів A–Z/0–9 · copy · `size` hero/compact | P1 | F-5.2 · D05 | `16:2` |
| DC-ROOM-002 | QR Block | QR + caption · `size` hero/compact | P1 | F-5.2 · F-5.5 · D05 | `16:23` |
| DC-ROOM-003 | Join Link Row | short URL + copy | P2 | F-5.2 | `26:284` |
| DC-ROOM-004 | Join By Code Form | input + submit + error | P2 | F-5.4 | `26:296` |
| DC-ROOM-005 | Join Landing State | in progress/invalid/not found/full/auth/blocked/error | P2 | F-5.5 VS-01…09 | `26:352` |
| DC-ROOM-006 | Player Chip | avatar + nickname · host marker · `ready` ready/waiting · offline. Лобі F-5.2/F-5.3 більше не чіпом — картка сітки це ROOM-029 | P1 | F-5.2 · F-5.3 | `16:49` |
| DC-ROOM-007 | Player Roster | заголовок + лічильник + Player Chip list · empty. Лобі F-5.2 — секція ROOM-030, без порожнього абзацу | P1 | F-5.2 · F-5.3 · D05 · D06 | `16:88` |
| DC-ROOM-008 | Ready Indicator | ready / not ready. У сітці лобі F-5.2 стан показує `DC-ROOM-029`: іконка `DC-ROOM-027` Ready або Waiting і слово «Готовий» / «Готова» / «Очікує» | P2 | D05 | `26:477` |
| DC-ROOM-009 | Game Card | назва · опис · min–max гравців · теги · selected | P1 | F-5.8 · D04 | `17:107` |
| DC-ROOM-010 | Selected Game Summary | назва + meta + «Змінити гру» / «Гру не обрано». У лобі F-5.2 назва гри в заголовку, не в цій картці | P2 | F-5.8 V-2 · D05 | `26:484` |
| DC-ROOM-011 | Lobby Settings Panel | таймер · кількість питань. Замінено на ROOM-031: набір полів бере гра | P2 | F-5.7 | `26:521` |
| DC-ROOM-012 | Host Control Bar | lobby (Start disabled/enabled) · session (Next / End). Старт лобі — нижня смуга: підказка хто не готовий і «Почати гру». Неактивний — `DC-BASE-001` Secondary Size L, усі готові і ≥3 — Primary Size L | P1 | F-5.9 · D05 · D07 | `16:142` |
| DC-ROOM-013 | Host Session Shell | TV 1440 frame | P2 | F-5.16 · D07 | `31:546` |
| DC-ROOM-014 | Player Session Shell | mobile 390 frame | P2 | F-5.17 | `31:732` |
| DC-ROOM-015 | Prompt Card | prefix + statement · meta · `size` host/player. Локальне дзеркало для F-6.1: «Я ніколи…» + формулювання + meta | P1 | F-6.1 · D07 | kit `17:186` · local `584:1430` |
| DC-ROOM-016 | Answer Control | yes/no · options · A/B · free text. Локально для NHIE: Yes No `584:1434` (Так / Ні) і Locked `584:1447` | P2 | BA kit §7 · F-6.1 | kit `28:446` · local `584:1434` |
| DC-ROOM-017 | Vote Control | pick player / funnier / rank | P2 | BA kit §7 | `28:507` |
| DC-ROOM-018 | Live Reactions Strip | реакції під час раунду. Локально чотири чіпи 😂 🔥 👏 💀 | P2 | F-6.30 · D07 · F-6.1 | kit `28:557` · local `584:1470` |
| DC-ROOM-019 | Session Results | podium | P2 | BA kit §7 | `30:533` |
| DC-ROOM-020 | Leaderboard Row | rank · avatar · score. Локально: місце, ім’я, рахунок | P2 | BA kit §7 · F-6.1 | kit `30:520` · local `584:1466` |
| DC-ROOM-021 | Reconnect Overlay | player / host | P2 | BA kit §7 | `28:606` |
| DC-ROOM-022 | Round Progress | «Раунд N / M» | P2 | D07 · F-6.1 | kit `28:633` · local `584:1464` |
| DC-ROOM-023 | Late Join Invite | compact code + QR / copy link | P2 | D07 | `28:646` |
| DC-ROOM-024 | Catalog Game Card | назва · опис · діапазон · мініатюра · 18+ (`Show adult`); тег у властивостях є, на каталозі прихований; `State` Default/Selected. Публічний каталог, не лобі (лобі лишається ROOM-009) | P1 | F-6.53 | kit `105:1622` · local `444:13837` |
| DC-ROOM-025 | Selected Catalog Game | «Обрана гра» + мініатюра + чотири дії (створити кімнату, долучитися по коду, історія ігор, детальніше правила); `Size` Desktop/Mobile; тег прихований, як у ROOM-024 | P1 | F-6.53 | kit `105:1735` · local `444:14444` |
| DC-ROOM-026 | Catalog Atmosphere | `Crop` Desktop 1440 / Mobile 390 — райські арки в хмарах, низ темний; абсолютний фон каталогу, не дерево досягнень (ACH-010) і не спіраль категорій (ACH-013) | P1 | F-6.53 | kit `105:1738` · local `444:13808` |
| DC-ROOM-027 | Lobby Icon | `Icon` Copy / Share / Kick / Ready / Waiting. На картці лобі Ready і Waiting стоять поруч зі словом стану. Share у запрошці лобі не використовується | P1 | F-5.2 · F-5.3 · F-5.19 | kit `111:1594` · local `482:2121` |
| DC-ROOM-028 | Lobby Invite | `Size=Desktop`: вертикальна картка. QR на всю ширину блоку, код + Copy, Telegram і WhatsApp (`DC-BASE-001` Secondary S), знизу на всю ширину червоне Primary L «Скасувати кімнату». Без системного поширення. `Size=Mobile`: компактний ряд «Код кімнати» + ABC123 + Copy + кнопка QR. Скасування на мобільному не в цій картці — червоний текст біля заголовка | P1 | F-5.2 · F-5.3 · F-5.12 · F-5.18 | local `510:1751` |
| DC-ROOM-029 | Lobby Player Tile | `Who=Host`: аватар `DC-BASE-014` Ring On, ім'я, мітка «ведучий», стан без кіка. `Who=Player`: той самий ряд, кік `DC-ROOM-027` справа. Стан — іконка Ready/Waiting і слово «Готовий» / «Готова» / «Очікує». Сітка desktop — 3 колонки (~348), mobile — вертикальний список | P1 | F-5.2 · F-5.3 · F-5.19 | local `510:1752` |
| DC-ROOM-030 | Lobby Shell | Не спліт «гравці зліва / налаштування справа». Desktop: колонка запрошення `DC-ROOM-028` і основна колонка — лічильники «Учасники N / max» і «Готові M / N», сітка `DC-ROOM-029`, картка правил `DC-ROOM-032`, картка параметрів `DC-ROOM-031`, знизу смуга старту `DC-ROOM-012`. Mobile: заголовок + скасування, компактне запрошення, список, знизу «Запросити» і старт. Фон сторінки — шахова партія на штормі (CROP, верх-право), не `DC-ROOM-026`. Текст на фото сидить на картці `#1D2022` / бордер `#3D4246`; мобільна шапка — `#121212` | P1 | F-5.2 · F-5.9 | — |
| DC-ROOM-031 | Lobby Settings Summary | Картка surface: заголовок «Параметри гри» + secondary «Налаштування» (лише Host) і read-only поля. `Game=NHIE`: Категорії (без «Грішники»), Складність (Усі / Легко / Середньо / Важко), Питань ∈ {5, 10, 15, 20}, Таймер ∈ {0, 5, 10, 15, 30, 60}, 0 = «Без таймера». `Game=Quiz`: Питань 5–20, Таймер ∈ {0, 30, 60, 120, 300}. Гравець бачить ті самі рядки без кнопки | P1 | F-5.7 · F-6.1 · F-6.2 | local `510:1750` |
| DC-ROOM-032 | Lobby Rules | Картка surface «Як грати» і короткий текст правил (1–500 символів). Той самий фон і бордер, що в ROOM-031, щоб рядок не зливався з фото | P1 | F-5.2 · F-5.3 | local `510:1732` |

## DC-STD — Standup / theory / improv

| ID | Name | Variants / properties | Priority | Source | Figma node |
|----|------|----------------------|----------|--------|------------|
| DC-STD-001 | Practice Entry Card | Стендап · Імпро · Теорія | P2 | F-7.1 · D09 | `35:1014` |
| DC-STD-002 | Timer | MM:SS · `state` running/warning/expired · `size`. Локально пігулка `0:15` | P1 | F-7.2 · F-9.9 · D07 · F-6.1 | kit `17:232` · local `584:1462` |
| DC-STD-003 | Triple Prompt | 1 prompt + 3 answer fields | P1 | F-7.2 · F-7.3 | `18:192` |
| DC-STD-004 | Best Answer Picker | вибір 1 з 3 | P2 | F-7.4 | `35:1064` |
| DC-STD-005 | Drill Summary | підсумок · disabled AI CTA | P2 | BA kit §8 | `35:1090` |
| DC-STD-006 | Notebook Item | дата + preview | P2 | F-7.6 | `35:1110` |
| DC-STD-007 | Notebook Editor | create / edit / delete confirm | P2 | F-7.7 | `35:1113` |
| DC-STD-008 | Theory Article Row | title · tags | P2 | F-8.1 | `35:1187` |
| DC-STD-009 | Tag Filter | chips group | P2 | F-8.2 | `35:1205` |
| DC-STD-010 | Improv Format Picker | список форматів + «Почати» | P2 | F-8.4 · D09 | `35:1227` |
| DC-STD-011 | Improv Live Cues | підказки без scoreboard | P2 | F-8.6 | `35:1259` |

## DC-TRN — Humor tournament

| ID | Name | Variants / properties | Priority | Source | Figma node |
|----|------|----------------------|----------|--------|------------|
| DC-TRN-001 | Tournament Poster | місяць · дати · правила · призи · CTA · preview учасників | P1 | F-9.1 · D08 | `18:342` |
| DC-TRN-002 | Tournament Map Item | поточний / минулий | P2 | F-9.2 · D02 | `33:883` |
| DC-TRN-003 | Registration CTA | `state` ready/registered/closed/auth required · cancel | P1 | F-9.3 · F-9.4 | `18:234` |
| DC-TRN-004 | Reminder Controls | email · Telegram · calendar | P2 | F-9.5 · F-9.6 · F-9.7 | `33:914` |
| DC-TRN-005 | Participants List | публічні нікнейми · empty | P2 | F-9.8 | `33:961` |
| DC-TRN-006 | Round Answer Form | setup/punch · per-answer timer | P2 | F-9.9 | `33:1004` |
| DC-TRN-007 | Pairwise Vote Card | дві анонімні відповіді · pick one | P1 | BA kit §9 | `18:269` |
| DC-TRN-008 | Round Result | passed / eliminated | P2 | BA kit §9 | `33:1086` |
| DC-TRN-009 | Public Results Board | загальні результати | P2 | BA kit §9 | `33:1102` |
| DC-TRN-010 | Awards Block | 1–3 · top-10 · task tops | P2 | BA kit §9 | `33:1126` |
| DC-TRN-011 | Phase Banner | registration/answering/voting/closed | P2 | BA kit §9 | `33:1164` |
| DC-TRN-012 | Karma Indicator | optional | P2 | BA kit §9 | `33:1196` |

## DC-MISC — Shared patterns

| ID | Name | Variants / properties | Priority | Source | Figma node |
|----|------|----------------------|----------|--------|------------|
| DC-MISC-001 | Adult Content Warning | перед adult modes | P2 | BA kit §10 | `43:2` |
| DC-MISC-002 | Untranslated Marker | оригінал + позначка | P2 | BA kit §10 | `43:23` |
| DC-MISC-003 | Media Placeholder | картки без арту | P2 | BA kit §10 | `43:37` |
| DC-MISC-004 | Age Gate Copy | 18+ на реєстрації | P2 | BA kit §10 | `43:50` |
| DC-MISC-005 | Landing Hero | hero + CTA cluster | P2 | BA kit §10 | `43:83` |

---

## MVP-хвиля (P1) — порядок збірки

1. **3a** `00 Foundations` → `01 Base` (BASE-001, 002, 004, 005, 010, 011, 012, 013, 014, 015, 016, 018, 019) → `02 Feedback` (FB-001, 002, 003, 005, 006)
2. **3b** `03 Navigation` (NAV-001, 002, 003) + HOME-001, 003, 004, 005, 006
3. **3c** `04 Domain`: ROOM-001, 002, 006, 007, 009, 012, 015 · ACH-001 · TRN-001, 003, 007 · STD-002, 003
4. `99 Examples`: smoke-екран Host lobby (D05) лише з інстансів — `18:428`

**Стан MVP-хвилі (2026-10-07):** усі P1 зібрані, Figma node проставлено. Спрощення MVP, закриті в P2: Button / Icon Button отримали `Pressed` і `Loading` (текст `Loading` / `Pressed` прив'язаний до властивості `Label`); HOME-002 Carousel Controls — окремий set `24:247`.

## P2-хвилі — порядок збірки

1. **Хвиля 1 — база й оболонка:** Button / Icon Button `Pressed` + `Loading` · FND-008 Motion, FND-009 Breakpoints · 18 нових іконок у FND-007 · токени `accent/pressed`, `bg/pressed` · BASE-003, 006, 007, 008, 009, 017, 020 · FB-004, 007 · NAV-004, 005, 006 · HOME-002, 007, 008
2. **Хвиля 2 — ROOM:** вхід (003–005) → лобі (008, 010, 011) → сесія (016–018, 021–023) → результати (019, 020) → оболонки (013, 014)
3. **Хвиля 3 — TRN + STD:** TRN-002, 004–006, 008–012 (zone mode `Purgatory`) · STD-001, 004–011 (zone mode `Inferno`)
4. **Хвиля 4 — ACH + AUTH + MISC:** ACH-002–009 і AUTH-006 (zone mode `Paradise`) · AUTH-001–005 · MISC-001–005 на `05 Blocks`
5. **Хвиля 5 — smoke-екрани в `99 Examples`, лише з інстансів:** D06 Player lobby `44:219` · D07 Host session `44:333` · D07 Player answer `44:647` · D08 Tournament `44:678` (zone mode `Purgatory`) · D01 Home `44:967`

**Стан P2 (2026-10-07):** усі P2 з реєстру зібрані, Figma node проставлено. Оболонки сесії (ROOM-013 / 014) у zone mode `Default` — зону задає гра, а не оболонка. ROOM-014 має стани VS-01–06, VS-08, VS-09; VS-07 — це редирект, тому окремого фрейму немає. Таймера в оболонці гравця немає.

**Відомі спрощення:**

- **Похідні значення (не зі styleguide):** `accent/pressed` (#B51D08) і `bg/pressed` (gray/700); значення Motion (FND-008) і Breakpoints (FND-009) — пропозиція kit, не затверджена.
- **Візуальні недоліки:** стрілка Tooltip трохи зміщена від центру; у Featured Poster зник верхній відступ 24 px над Carousel Controls; Mobile Action Bar (NAV-004) має фон `bg/base` і зливається з фоном set — у D-екранах видно нормально; іконка `settings` схожа на `filter`.
- **Заглушки:** QR у QR Block і Late Join Invite — іконка, а не справжній код; іконки Live Reactions (ROOM-018) — тимчасові, бо набір реакцій береться з CMS-каталогу (F-6.30); в Auth Form (AUTH-001) кнопки Google / Apple без логотипів провайдерів, лише текст.
- **Тексти-зразки:** заголовок Landing Hero (MISC-005), текст попередження 18+ (MISC-001), нікнейми, сетапи, дати й назви турнірів у прикладах — чернетка, не узгоджена копія.
- **Прибрано те, чого немає в BA:** лічильники символів у вільній відповіді (ROOM-016) і в панчі (TRN-006) приховано — ліміту в специфікаціях немає. В Account Menu (NAV-006) немає пункту «Налаштування» — його немає в специфікації.

**Рішення PO (зафіксовано):**

- **Тон звертання — «ти»** (2026-10-07). Уся подальша UI-копія в kit, smoke-екранах і Astra-промптах — на «ти», не на «Ви». Див. також `style-lock/STYLE-LOCK.md` § UI copy.

**Рішення без PO (перевірити):**

- **ACH-003** у реєстрі історично названо «Achievement Detail», але окремої сторінки й модалки confirm/cancel немає (F-4.3). Дія живе в meta-рядку картки: «Підтвердити» або галочка + тиха icon-кнопка скасування справа.
- **ROOM-017 Vote Control:** «ранжування» зібрано як оцінку 1–10 (Roast Rap Battle), поряд із Pick Player і Funnier.
- **ROOM-019 Session Results:** дію «Повернутися в лобі» бачить лише хост (AC-RES-05).
- **DC-TRN-012 Karma Indicator** (також у D08): підписи «Карма раю / Карма пекла» — синоніми GL-045 / GL-046. Це назви валют, не лейбли зон у навігації; чи лишаємо ці формулювання — ще відкрито.
- **TRN, Round Result:** у тексті 30% + 2% wildcard (F-9.16). Таймери R1 — 10 хв на раунд і 1,5 хв на відповідь.
- **STD-010 Improv formats:** назви форматів (Офіціант / Барабан / Монолог) взято з прикладів глосарію, описи — зразки. Кнопку «Завершити» виведено зі статусу `ended`.
- **STD Notebook:** заголовок необов'язковий, до 200 символів; текст до 10 000 символів (F-7.7).

Свідомо поза kit: CMS-екрани, повні екрани 28 ігор, ілюстрації зон, email / Telegram шаблони.
