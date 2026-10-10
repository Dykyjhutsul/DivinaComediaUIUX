# CLAUDE.md — DivinaComediaUXUI

Інструкції для агента в цьому репозиторії. Читай перед будь-якою зміною.

## Призначення

Design-ops пайплайн: референси → moodboards → Style Lock → Astra-концепти → DESIGN.md.
Не містить feature specs і не є source of truth для поведінки продукту.

BA / поведінка: `../DivinaComedia/docs/ba/` (або абсолютний шлях до BA-репо).
UX must-show екранів: [`briefs/screens-ux.md`](briefs/screens-ux.md).
Home IA lock (головна на `/`, портал з трьох дверей): [`briefs/home-ux-locked.md`](briefs/home-ux-locked.md) · like/dislike концептів: [`briefs/home-concepts-feedback.md`](briefs/home-concepts-feedback.md).

## Доставка

Jira для цього проєкту не використовується (рішення 2026-10-10, те саме в BA і в застосунку). Статус екрана — у Figma і в журналі цього файлу, не в тікетах.

## Hard constraints

1. **No medieval Dante UI** — без ілюмінованих манускриптів, херувимів/демонів як маскотів, gothic ornament як системи.
2. **No neon / cyberpunk glow / purple SaaS default.**
3. **Atmosphere ≠ layout.** Кластери A–C дають світло, палітру, матеріали. Layout і компоненти — з кластера D + briefs.
4. **Зони = навігація.** Рай / Чистилище / Пекло можуть мати різну температуру кольору, але одну систему кнопок / радіусів / типу.
5. **Не вигадуй продуктову поведінку.** Якщо брифу немає — читай BA-спеку або питай; не додавай балів у імпро, guest mode тощо.
6. **Мова:** операторські доки — українською; Astra-промпти — англійською з `Ukrainian UI copy`.
7. **Тон UI-копії — «ти»** (PO 2026-10-07). Не «Ви». Зафіксовано в `style-lock/STYLE-LOCK.md` § UI copy.

## Структура (не ламай)

| Шлях | Роль |
|------|------|
| `references/keep/` | Source of truth Keep |
| `references/clusters/` | Копії топів за mood/UI |
| `references/INDEX.md` | Карта файл → кластер → роль |
| `prompts/` | Промпти; не клади сюди скріни |
| `concepts/` | Виходи Astra; не правити «під фінал» |
| `style-lock/STYLE-LOCK.md` | Контракт після вибору стилю |
| `design-system/COMPONENT-IDS.md` | Реєстр компонентів UI Kit (`DC-{LAYER}-{NNN}`), пріоритети, Figma node |
| `design-system/figma-uikit-ledger.json` | Машинний ledger: variables, icons, component/example node ids |

## Робочий порядок

1. Triage (`checklists/step-1-triage.md`) → оновити `INDEX.md`
2. Moodboard колажі → `moodboards/`
3. Style exploration (`prompts/01-style-exploration.md`) → `concepts/style-exploration/`
4. Заповнити `STYLE-LOCK.md` з template
5. Екрани по одному (`prompts/02-screens/*`) + Style Lock у кожному промпті
6. `design-system/DESIGN.md` з template
7. UI Kit у Figma (`fileKey 7VS64TZ3mjVvxoaYF6ZHDk`) — лише за `COMPONENT-IDS.md`; токени тільки зі `STYLE-LOCK.md` (Variables, без hex у компонентах); перед `use_figma` — skills `figma-use` + `figma-generate-library`

## Windows

Не створюй папку `References` поруч із `references` — NTFS case-insensitive; видалення однієї знесе обидві.

## Що оновлювати в тій самій сесії

| Зміна | Файл |
|-------|------|
| Нові Keep / кластери | `references/INDEX.md` |
| Обрано стиль | `style-lock/STYLE-LOCK.md` |
| Новий екранний промпт | `prompts/02-screens/` + рядок у `briefs/screens-ux.md` якщо треба |
| PO like/dislike по Home-концептах | `briefs/home-concepts-feedback.md` (+ sync `home-ux-locked.md` / `d01-hub.md` якщо IA) |
| Новий / зібраний компонент UI Kit | `design-system/COMPONENT-IDS.md` (наступний вільний ID, `Figma node`) + `figma-uikit-ledger.json` |
| Рішення PO по UI-копії / тону | `style-lock/STYLE-LOCK.md` § UI copy + рядок у COMPONENT-IDS |
| Зміна пайплайну | `README.md` + цей файл |

## Журнал змін

- 2026-10-10 — F-5.6, F-5.13 і F-5.16 на `467:802`: кожен VS окремим кадром desktop 1440 і mobile 390, оболонка лобі (шахи, картка `#1D2022`). F-5.6 — плоский список після гри без фільтрів, поточна гра «Зіграти ще раз», інші «Обрати гру», деталі Quiz. F-5.13 — лідерборд із тай-брейком 1, 2, 2, 4 і підсумок без місць; з історії кнопка «До історії». F-5.16 — код ABC123, фаза раунду, таймер 0:42, між раундами без таймера і без зміни гри. Node-id у `**Design**` cell спек не чіпав — треба `design-links` + Gate 6.
- 2026-10-10 — F-5.9, F-5.11, F-5.12, F-5.15, F-5.18, F-5.19 на `467:802`: кожен VS окремим кадром desktop 1440 і mobile 390, оболонка лобі (шахи, картка `#1D2022`). F-5.14 — лише mobile 390. Підтвердження скасування, виходу і кіка — червона дія + «Назад» / «Скасувати». Node-id у `**Design**` cell спек не чіпав — треба `design-links` + Gate 6.
- 2026-10-09 — F-5.7 на `467:802`: VS-01, VS-03…VS-09 і форми VS-02 (Quiz / Most Likely To), VS-11…VS-29 × desktop 1440 / mobile 390; VS-10 — копія лобі після збереження (`526:4000` / `526:4310`). Картка `#1D2022`, чіп обраного значення, «Скасувати» / «Зберегти». На VS-28 (Дедлайн) і VS-29 (Подія) замість текстового поля — календар місяця + ряд годин; обрані 12.10.2026 19:00 і 24.12.2026 19:00. Node-id у `**Design**` cell спеки не чіпав — треба `design-links` + Gate 6.
- 2026-10-09 — F-5.3, F-5.4 і F-5.5 на сторінці `467:802` перезібрано з оболонки F-5.2 (фон шахів, картка `#1D2022`). Лобі гравця: той самий інвайт без скасування кімнати і без кіка, «Покинути кімнату» (desktop — текст під WhatsApp, mobile — біля заголовка), read-only параметри, «Підтвердити готовність» / «Ти підтвердив готовність» + «Скасувати готовність». Вхід за кодом — одне поле «Введи код», шість позицій, без підказки «6 символів», окремий кадр на кожну відмову, desktop 1440 і mobile 390. Вхід за посиланням — mobile 390, без сканера. Node-id у `**Design**` cell спек не чіпав — треба `design-links` + Gate 6.
- 2026-10-09 — Лобі F-5.2 зібрано в локальний kit (`8itQZGbt…`, сторінка `316:167`): DC-ROOM-028 Invite `510:1751` (Desktop — вертикальна картка, QR на всю ширину, без Share, червоне «Скасувати кімнату» знизу; Mobile — ряд коду), DC-ROOM-029 Tile `510:1752` (Who=Host / Who=Player, слово стану + кік лише в гравця), DC-ROOM-031 Settings `510:1750`, DC-ROOM-032 Rules `510:1732`. ROOM-030 лишається композицією екрана, не компонентом. У головний kit `7VS64…` ще не перенесено.
- 2026-10-09 — Лобі ведучого: коментарі на `467:802` (червоне «Скасувати кімнату» справа, дві секції гравці | налаштування+старт, без чіпа категорії, галочка як у досягненнях, кік через діалог). Реєстр COMPONENT-IDS v1.11: DC-ROOM-028…031 ще без Figma node. Бриф прикладу — `briefs/screens-ux.md` §07.
- 2026-10-09 — F-5 на `467:802` перезібрано після спек, нейтрально, без `DC-ROOM-026`. Вхід за кодом — одне поле «Введи код» і окремий стан на кожну відмову, без підказки «6 символів». Лобі «Лобі Never Have I Ever» і категорія; інвайт: QR, код, іконки копії й поширення, Telegram, WhatsApp, скасування на тому ж рядку; сітка по 3; 20 людей у скролі; старт неактивний, доки гра не дозволяє. Гравець бачить той самий інвайт, «Підтвердити готовність» / «Ти підтвердив готовність». Налаштування — дві форми однієї оболонки (NHIE і Quiz). Підтвердження скасування, кіка й виходу. Іконки `DC-ROOM-027` (Copy / Share / Kick / Ready / Waiting): kit `111:1594`, локально `482:2121`. Атмосферний пас лишається на `473:802`. Node-id у `**Design**` cell спек не чіпав — треба `design-links` + Gate 6.
- 2026-10-08 — F-5.1 у Figma (`8itQZGbt0r9xhmrg4MAouK`, сторінка `99:77`) перезібрано на UI Kit за старою формою створення. Спека 2026-10-08 зняла форму: актуальний дизайн — сторінка `467:802`, не `99:77`.
- 2026-10-08 — F-6.53 mobile: фон `DC-ROOM-026` Crop=Mobile — кадр `arena-mobile-390x4500` (`f561738a…`), притиснутий до верху на довгій сторінці й на коротких станах. Kit `105:1737`, локально `444:13807`.
- 2026-10-08 — F-6.53: фон `DC-ROOM-026` замінено на кадр з арками (desktop `4cbbfdb9…`, mobile `e8f17832…`) у kit `105:1736`/`105:1737` і локально `444:13806`/`444:13807`. Фільтри лишаються суцільними.
- 2026-10-08 — F-6.53: фільтри каталогу суцільні (темна пігулка, «Усі» — акцент), бо на прозорих чипах їх не було видно. Фон `DC-ROOM-026` замінено на тиху золоту спіраль (desktop `c5fae7e0…`, mobile `f8105a2c…`) у kit `105:1736`/`105:1737` і локально `444:13806`/`444:13807`.
- 2026-10-08 — `DC-ACH-013 Atmosphere Paradise Spiral` перенесено в головний UI Kit (`7VS64…`, сторінка `3:94` 04 Domain, set `106:2249`, фони `7b1c…` / `178e…`), поряд із DC-ACH-010. Реєстр COMPONENT-IDS v1.9 (Figma node → kit `106:2249` · local `444:1383`). Робочі екрани F-4.3/4.6/4.10 лишаються на локальному інстансі робочого файлу (kit ще не опубліковано як team library).
- 2026-10-08 — Нова атмосфера категорій Раю `DC-ACH-013 Atmosphere Paradise Spiral` (золота спіраль-гелікс на `zone/void`, Crop Desktop 1440 / Mobile 390; Figma set `444:1383`, фони `7b1c…` / `178e…`). Перекинуто фон із дерева `DC-ACH-010` на спіраль: **F-4.3** (`56:77`, 21 інстанс), **F-4.6** (`63:77`, 18), **F-4.10** (`79:77`, 12). **F-4.2 лишається на дереві.** Референси `paradise-spiral-bg-{desktop,mobile}.png` в Keep; реєстр COMPONENT-IDS v1.8, STYLE-LOCK § Component feel/Attachments. Node-id у `**Design**` cell спеки F-4.3 не чіпав — треба `design-links` + (за потреби) Gate 6.
- 2026-10-08 — F-4.14 у Figma (`8itQZGbt0r9xhmrg4MAouK`, сторінка `439:802`): VS-01–09 × desktop 1440 / mobile 390 на оболонці F-4.13. Картка «Брехав близьким» — `DC-ACH-002` Not Confirmed = «Визнати», Confirmed = галочка + cancel. Успіх і 403/404/500 — toast `DC-FB-001`; сесія і refresh-fail — банер `DC-FB-002`. Без модалки і без карми пекла.
- 2026-10-08 — UI Kit ← F-6.53: DC-ROOM-024 Catalog Game Card (`105:1622`), DC-ROOM-025 Selected Catalog Game (`105:1735`), DC-ROOM-026 Catalog Atmosphere — райські арки (`105:1738`). Локальні дзеркала `444:13837` / `444:14444` / `444:13808`. Екран F-6.53 на новій атмосфері, картки й обрана гра — інстанси.
- 2026-10-08 — F-6.53 desktop: усі 28 ігор F-6.1–F-6.28, теги (Усі · Алкогольні · Icebreaker · Сімейні · Для пар · Для команди · Для колег), обрана гра за замовчуванням перша і закріплена, картки внизу в скролі. Mobile — той самий список і теги, секція обраної гри скролиться разом зі сторінкою.
- 2026-10-08 — F-4.13 клімат Грішників: новий `DC-ACH-012` Atmosphere Sinners (`435:1386`, Crop Desktop/Mobile) на фоні з Keep; Color mode `Sinners` (wine/950–800, бордер red/600 @ 40%). Усі VS на сторінці `93:147`.
- 2026-10-08 — F-4.13 mobile: пошук `DC-ACH-006` висота 44, як фільтри. VS-02b max + lazy (`420:2544` / `420:2564`): 9 гріхів + скелетони, прогрес 3 / 24.
- 2026-10-08 — F-4.13 у Figma (`8itQZGbt0r9xhmrg4MAouK`, сторінка `93:147`) перезібрано на UI Kit: VS-01–07 × desktop 1440 / mobile 390; оболонка F-4.3 (DC-NAV-001 · back «Досягнення» · DC-ACH-010 · DC-ACH-002/003 · DC-ACH-004/005/006). Privacy `DC-FB-002` Info на VS-02–04. Без «Запропонувати». VS-06 — банер сесії, без grid. Старий Variant K — в Archive (`415:802`).
- 2026-10-08 — F-3.2 у Figma (`8itQZGbt0r9xhmrg4MAouK`, сторінка `39:95`) перезібрано на UI Kit: VS-01–08 × desktop 1440 / mobile 390; оболонка DC-NAV-001 · back «← Профіль» · email `DC-BASE-004` Disabled · `DC-AUTH-002` · `DC-AUTH-007` (preset picker) · `DC-BASE-001` Скасувати/Зберегти · toast `DC-FB-001` · banner `DC-FB-002` · error `DC-FB-006`. Локальний AUTH-007 `405:1769`. Старий Variant K — в Archive.
- 2026-10-08 — F-3.1: «Вийти» / «Деактивувати акаунт» у DC-AUTH-003 праворуч від нікнейма й email; confirm VS-06.
- 2026-10-08 — F-3.1 у Figma (`8itQZGbt0r9xhmrg4MAouK`, сторінка `35:77`) перезібрано на UI Kit: VS-01–05 × desktop 1440 / mobile 390; оболонка DC-NAV-001 · DC-AUTH-003 (email, без edit) · DC-AUTH-006 (вітрина Completed: назва · категорія · складність · %; у т.ч. Грішники) · DC-FB-002 / DC-FB-006. Локальні AUTH-003 `401:1316` · AUTH-006 `401:1535`. Старий Variant K (зонне меню, «Редагувати») — в Archive.
- 2026-10-08 — UI Kit ← F-4.6 / F-4.10: ACH-003 без видимого «Підтверджено»; ACH-002 meta HUG + spacer FILL; FB-001 копія write-toast + 400/150 ms; ACH-007 тепер set `98:3365` (7 станів, Size L, банер стовпчиком, zone/card).
- 2026-10-08 — F-4.6 / F-4.3: ACH-002 «Підтвердити» справа (spacer FILL); сітка desktop gap 16, рядки більше не накладаються. Результати write — toast DC-FB-001 (400ms in / 150ms out), не банер. Local toast `395:9642`.
- 2026-10-08 — F-4.6 у Figma (`8itQZGbt0r9xhmrg4MAouK`, сторінка `63:77`) перезібрано на UI Kit: VS-01–09 × desktop 1440 / mobile 390 на оболонці F-4.3 (DC-NAV-001 · DC-ACH-002/003 · DC-FB-002). Write з картки «Зіграти в Overwatch»; Confirmed = галочка + cancel; без модалки й без карми пекла. Старий Variant K (зонне меню, detail-layout, +10 карми) — в Archive.
- 2026-10-08 — F-4.10 адаптив: SystemError банер — текст + «Спробувати ще» стовпчиком; плейсхолдер «Наприклад: зіграти з друзями» 14 px; Скасувати / Надіслати обидві Size=L (52).
- 2026-10-08 — F-4.10 у Figma (`8itQZGbt0r9xhmrg4MAouK`, сторінка `79:77`) перезібрано на UI Kit: VS-01–07 × desktop 1440 / mobile 390; overlay `DC-ACH-007` на F-4.2 / F-4.3 (VS-03) / F-1.2 (VS-05). Старий Variant K — в Archive. CTA «Надіслати» / «Закрити»; SystemError більше не тягне «Код кімнати».
- 2026-10-08 — UI Kit ← F-4.2: ACH-001 без стрілки, Compact колонка + приклад 173×130; ACH-008 червоний / ACH-011 кремовий; ACH-010 stretch-to-frame в описі.
- 2026-10-08 — UI Kit синхрон з F-4.3: ACH-002/003/004/005 уже мали Field FILL, icon-only Confirmed і spacer; дописано descriptions; Cancelling без текстів «Підтверджено»/«Скасувати»; NAV-005 отримав `Label`.
- 2026-10-08 — F-4.2 Compact 4:3: всередині колонка icon → назва → «X з Y»+бар, блок по вертикалі по центру (без порожнечі SPACE_BETWEEN).
- 2026-10-08 — F-4.2 картки: стрілку з ACH-001 прибрано; Compact — icon+назва в ряд (11/14), довгі назви wrap, прогрес знизу; фіксовану висоту заголовка відкочено.
- 2026-10-08 — F-4.2: pills поміняли колір (Suggest — `text/primary` кремовий, Sinners — `zone/accent` червоний); `BG / Paradise tree` натягнуто на висоту кадру (VS-02 desk 1108, mobile tall 1239–1627), короткі кадри clip.
- 2026-10-08 — F-4.2 правки PO: шапка DC-NAV-001 (лого + «Божественна комедія», без back); pill `DC-ACH-011` «Запропонувати ачівку» → F-4.10 біля «Грішників»; ACH-001 `Size=Compact` на 390 (12 px / 2 рядки / бар FILL).
- 2026-10-08 — Paradise climate у UI Kit + F-4.2: токени `zone/void` `#070604` · `zone/card` `#14110D` · `zone/card-border`; `DC-ACH-010` дерево; ACH-001/008 на золотому кліматі; NAV-001 `Surface=Ghost`. F-4.2 VS-01–05 × 1440/390 — атмосфера + H1 «Досягнення» (без підзаголовка). Реф PO в `references/keep/paradise-tree-bg-*.png`. F-4.3 ще на старому графіті.
- 2026-10-08 — F-4.3 Confirmed: текст «Підтверджено» прибрано, лишилась галочка + cancel; кластер притиснутий вправо в meta (desktop і 390).
- 2026-10-08 — F-4.3 chrome як F-4.2: DC-NAV-001 (зірка + «Божественна комедія»), back «Досягнення» під шапкою, DC-ACH-011 справа в рядку пошуку, фон DC-ACH-010. Усі VS-01–10 × 1440/390 + VS-02b.
- 2026-10-08 — F-4.3 desktop VS-02b (`368:4564`): 3 ряди × 3 картки + ряд скелетонів (лінивий рендер решти; A-4 без пагінації API). VS-02 1/3 лишився як AC-приклад.
- 2026-10-08 — F-4.3 mobile фільтри: Field був FIXED 200 у інстансі 175 і зливався в один контрол; Field тепер FILL, ряд gap 10, value truncate. Desktop HUG 200 без змін.
- 2026-10-08 — F-4.3 адаптив: desktop-дропдауни більше не накладаються (HUG 200); mobile — пошук + один ряд фільтрів FILL без caption (влазить «Не підтверджено»); empty/error FILL 358; cancel у meta без clip.
- 2026-10-08 — F-4.3 у Figma (`8itQZGbt0r9xhmrg4MAouK`, сторінка `56:77`) перезібрано на UI Kit: VS-01–10 × desktop 1440 / mobile 390; оболонка DC-NAV-002, картки DC-ACH-002/003, пошук і фільтри DC-ACH-004/005/006 + Chip DC-BASE-012, empty/error DC-FB-005/006, сесія DC-FB-002. Локальні дзеркала ACH-002–006 і Chip — сторінка `316:167`. Старі Variant K — в Archive (`361:802`).
- 2026-10-08 — F-2.2 Gate 6 close-out у Figma (`8itQZGbt0r9xhmrg4MAouK`): «Події» на VS-01–04 × desktop/mobile — `Show arrow=false` + opacity 0.55 (C-14); додано VS-05 single-slide без carousel controls (`355:2197` / `355:2209`). DC-HOME-009 отримав boolean `Show arrow`.
- 2026-10-08 — F-4.2 у Figma (`8itQZGbt0r9xhmrg4MAouK`, сторінка `44:77`) перезібрано на UI Kit: VS-01–05 × desktop 1440 / mobile 390; картки DC-ACH-001 (Auth X/Y · Guest hint), пасхалка DC-ACH-008, empty DC-FB-005, error DC-FB-006. Локальні дзеркала — сторінка `316:167`. Старі Variant K (пошук / VS-06) — в Archive (`353:2056`).
- 2026-10-08 — F-1.1 і F-1.2 у Figma (`8itQZGbt0r9xhmrg4MAouK`) перезібрано на UI Kit: реєстрація VS-01–12 і вхід VS-01–05 × desktop 1440 / mobile 390; шапка DC-NAV-001, форми DC-AUTH-001/002, age gate DC-MISC-004, банери DC-FB-002. Локальні дзеркала kit — сторінка `316:167`. Старі Variant K — в Archive (`341:77`, `335:448`). Node-id desktop у спеках не змінювались.
- 2026-10-07 — F-2.2 у Figma (`8itQZGbt0r9xhmrg4MAouK`, сторінка `23:133`) перезібрано під portal-v1: VS-01–04 × desktop 1440 / mobile 390, фон desktop віддзеркалено за LOCK (світлі двері зліва). Kit не опублікований як team library, тож у файлі F-2 лежить локальна копія kit (сторінка `316:167`, ledger → `localMirrors`); старі фрейми — в секції Archive. Нові: DC-HOME-009 Portal Node, іконки pause/play, кнопка паузи в Carousel Controls — у kit `7VS64…` ще не перенесені.
- 2026-10-07 — Home portal-v1 (PO): головна на `/` без окремого лендінгу, зонових хабів Рай/Чистилище/Пекло немає, переходи в дверях порталу, банер-слайдер з адмінки, два стани профілю, § Адаптив; `home-ux-locked.md` ревізовано, `d01-hub.md` v6, макет у `concepts/d01-hub/`, фон у Keep.
- 2026-10-07 — UI Kit P2 закрито (реєстр v1.1 + ledger); тон UI-копії зафіксовано як «ти»; у STYLE-LOCK додано pressed-токени й § UI copy.

## Чого не робити

- Не імпортувати всю Pinterest-дошку в Figma.
- Не генерувати «весь продукт одним промптом».
- Не комітити секрети / `.env`.
- Не правити BA-артефакти з цього репо без явного запиту.
