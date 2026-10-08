# STYLE-LOCK

> Вставляй paste block у **кожний** наступний Astra-промпт. Цей файл — джерело значень для Figma Variables у [DivinaComediaUIKit](https://www.figma.com/design/7VS64TZ3mjVvxoaYF6ZHDk/DivinaComediaUIKit?node-id=0-1) і для реєстру [`../design-system/COMPONENT-IDS.md`](../design-system/COMPONENT-IDS.md).

## Status

- [x] Locked
- Date: 2026-10-07 · amended 2026-10-08 (Paradise page atmosphere)
- Chosen direction: **Dark App** — матовий темний продуктовий UI, один червоний бренд-акцент, три зони як температура кольору (styleguide-канвас v1: [`styleguide-dark-app-v1.png`](styleguide-dark-app-v1.png))
- Rejected: quiet luxury / museum, medieval Dante chrome, neon / cyberpunk glow, purple SaaS

## Atmosphere (1–2 речення)

Темна сцена comedy-клубу: матові графітові поверхні, один гарячий червоний промінь для дії. Зони ділять одну систему кнопок / радіусів / типу; клімат — температура акценту **і** (де є реф) атмосферний фон сторінки. Рай: золоте дерево на порожнечі ([`paradise-tree-bg-desktop.png`](../references/keep/paradise-tree-bg-desktop.png)) — як портал на Home, не як орнамент chrome.

## Palette

| Role | Hex / token | Notes |
|------|-------------|-------|
| Background | `#121212` · `color/bg/base` | Фон сторінки |
| Surface | `#1D2022` · `color/bg/surface` | Картки, хедер, nav-картки |
| Raised | `#282C2F` · `color/bg/raised` | Hover secondary, поля, skeleton |
| Border | `#3D4246` · `color/border/default` | Контур карток і secondary-кнопок |
| Text primary | `#F7F7F5` · `color/text/primary` | Також focus ring |
| Text muted | `#B8BBC0` · `color/text/secondary` | Підписи, meta |
| Accent | `#D92309` · `color/accent/default` | Primary CTA, активна точка каруселі, date-badge |
| Accent hover | `#EF3B22` · `color/accent/hover` | Похідне від styleguide (світліший червоний) |
| Accent pressed | `#B51D08` · `color/accent/pressed` | Похідне (P2 UI Kit); темніший червоний для Pressed |
| Accent disabled | `#D92309` @ 40% | Вимкнена primary |
| Surface pressed | gray/700 · `color/bg/pressed` | Похідне (P2 UI Kit); Pressed secondary / ghost |
| Success | `#3CCB7F` · `color/status/success` | Крапка «Відкрито» (похідне; у канвасі без hex) |
| Zone Рай tint | `#F5D778` · `zone/accent` (mode Paradise) | Досягнення · Ігри · прогрес-бар |
| Zone Чистилище tint | `#8DB8D8` · `zone/accent` (mode Purgatory) | Турніри · Події |
| Zone Пекло tint | `#ED645B` · `zone/accent` (mode Inferno) | Стендап · Імпровізація · Теорія |
| Zone void (Рай) | `#070604` · `zone/void` (mode Paradise) | Підклад під дерево; Default = `#121212` |
| Zone card (Рай) | `#14110D` · `zone/card` (mode Paradise) | Картка на атмосфері; Default = surface `#1D2022` |
| Zone card border (Рай) | gold/300 @ 16% · `zone/card-border` | Теплий контур на атмосфері; Default = `#3D4246` |

## Typography

- Display: **Montserrat ExtraBold 48** (wordmark, hero-заголовки афіші)
- Heading: **Montserrat Bold 32** (H1); H2 24 Bold, H3 20 SemiBold — похідні шкали
- Body: **Montserrat Regular 16**; Body S 14 Regular
- Action (кнопки, nav-картки): **Montserrat SemiBold 16** (S-кнопка 14)
- Caption / UI labels: **Montserrat Medium 12**
- Mono (код кімнати, таймер, рахунок): **JetBrains Mono Bold** (fallback Space Mono)
- Avoid: Inter / Roboto / Arial як display; serif-«манускрипт»; декоративні gothic-шрифти

> Гарнітура в канвасі не підписана — Montserrat обрано як найближчу геометричну гротеск-гарнітуру з повною кирилицею, доступну в Figma. Якщо в оригінальному канвасі інший шрифт — замінити тут і в text styles.

## Materials & depth

Матові плоскі поверхні без glassmorphism. Глибина — зміною тону (`bg → surface → raised`) і тонким контуром; тінь лише для overlay (modal, toast, dropdown). Фото / арт — сторінковий фон (Home-портал, дерево Раю) або всередині афіші з темним градієнтом до краю. Не робити з арту другу систему кнопок чи рамок.

## Component feel

- Corners: **8** (S-кнопки, бейджі-квадрати, поля) · **12** (кнопки M/L, nav-картки) · **16** (картки-контейнери, афіша) · **full** (pills-бейджі, аватар, кнопки-стрілки каруселі)
- Spacing: **4 · 8 · 12 · 16 · 24 · 32** (+48 для секцій)
- Borders / dividers: 1px `#3D4246`; секційні лейбли — 2px кольорова вертикальна риска зони зліва
- Buttons: висоти **S 36 · M 44 · L 52**; Primary — червона заливка + стрілка «→»; Secondary — контур на фоні; Text action — без рамки. Стани: Default · Hover · Focus (2px ring `#F7F7F5`) · Pressed (`accent/pressed` / `bg/pressed`) · Loading · Disabled (40%)
- Nav card: іконка зони + підпис + «→», surface + контур, радіус 12
- Badges: date (accent tint + accent контур), neutral (surface + контур), status (крапка + текст)
- Header: золота 4-кінцева зірка + wordmark зліва, аватар з тонким золотим кільцем справа
- Carousel: стрілки-кола, dots (активна — accent)
- Cards: лише інтерактивні контейнери — без декоративних карток
- Paradise destination (каталог Досягнень, F-4.2): `DC-ACH-010` дерево на `zone/void`; картка `DC-ACH-001` = `zone/card` + золотий прогрес; «Грішники» = pill `DC-ACH-008` (зірка + стрілка), не картка в сітці
- Paradise category screens (F-4.3 / F-4.6 / F-4.10): `DC-ACH-013` золота спіраль-гелікс на `zone/void` — окрема атмосфера категорій (PO 2026-10-08); перехід із каталогу (дерево) у категорію (спіраль). Та сама система карток / кнопок / типу
- Sinners page (F-4.13 only): `DC-ACH-012` blood-moon atmosphere; Color mode `Sinners` (`bg/surface` wine/900 `#14080E`, `border/default` red/600 at 40%). Same buttons, radii, and type as the rest of the kit. Not the Standup Inferno zone.
- Header на атмосфері: ghost / прозорий, не суцільний `#121212` брус, що ріже дерево

## UI copy

- **Тон звертання: «ти»** (PO 2026-10-07). Не «Ви».
- Мова інтерфейсу — українська.
- Назви валют «Карма раю / Карма пекла» (GL-045 / GL-046) у `DC-TRN-012` — **тимчасово** як у глосарії; фінальні підписи ще не затверджені PO.

## Hard bans (keep forever)

- No medieval Dante ornament as system
- No neon / cyberpunk glow
- No Inter / Roboto / Arial as brand display
- No purple-on-white SaaS default
- Atmosphere art = page background only (Home portal, Paradise tree) — never chrome ornament, never a second layout system
- Warm gold light on the Paradise tree ≠ neon / cyberpunk glow
- Лейбли «Пекло / Чистилище / Рай» — лише як документаційні підписи в UI Kit (styleguide §04); на Home та в продуктовій навігації їх **немає** (Home LOCK)
- Не звертатися на «Ви» у продуктовій UI-копії

## Attachments for Astra

- Styleguide: [`styleguide-dark-app-v1.png`](styleguide-dark-app-v1.png)
- Paradise page atmosphere (каталог F-4.2): [`../references/keep/paradise-tree-bg-desktop.png`](../references/keep/paradise-tree-bg-desktop.png) · mobile [`../references/keep/paradise-tree-bg-mobile.png`](../references/keep/paradise-tree-bg-mobile.png)
- Paradise category atmosphere (F-4.3 / F-4.6 / F-4.10): [`../references/keep/paradise-spiral-bg-desktop.png`](../references/keep/paradise-spiral-bg-desktop.png) · mobile [`../references/keep/paradise-spiral-bg-mobile.png`](../references/keep/paradise-spiral-bg-mobile.png)
- Paradise product-UI ref (IA + climate; **no subtitle** — spec C-5): [`../references/clusters/D-product-ui/d03-achievements-paradise-desktop.png`](../references/clusters/D-product-ui/d03-achievements-paradise-desktop.png)
- Moodboard file(s): —
- Product-UI moodboard: —

## Paste block for prompts

```text
STYLE LOCK (do not drift):
- Direction: Dark App — matte graphite product UI, single hot red brand accent, comedy-club stage mood
- Palette: bg #121212, surface #1D2022, raised #282C2F, border #3D4246, text #F7F7F5, muted #B8BBC0, accent red #D92309 (CTA only)
- Zones (no zone labels in UI): Inferno #ED645B, Purgatory #8DB8D8, Paradise #F5D778
- Paradise page climate (PO 2026-10-08): void #070604, card #14110D, gold/300@16% card border; luminous tree as page background (DC-ACH-010)
- Type: Montserrat — Display 48/800, Heading 32/700, Body 16/400, Action 16/600, Caption 12/500; mono for room code / timer
- Shape: radius 8/12/16/full, spacing 4/8/12/16/24/32, 1px borders, buttons S36/M44/L52 with trailing arrow
- Materials: flat matte chrome; page atmosphere allowed on Home + Paradise destinations; no glassmorphism, no neon
- Bans: no medieval Dante UI, no cyberpunk glow, no purple SaaS, no Inter/Roboto display, no yellow CTA spam, no subtitle on Досягнення
- Same button/radius/type system in every zone; atmosphere ≠ layout
- Ukrainian UI copy: informal «ти» (never formal «Ви»); no zone name labels in product navigation
```
