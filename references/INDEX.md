# References INDEX

> Оновлено: 2026-10-08 — + спіраль Раю (desktop/mobile) — атмосфера категорій F-4.3 / F-4.6 / F-4.10 (F-4.2 лишається на дереві). Раніше 2026-10-08 — + дерево Раю (desktop/mobile) і D03 product-UI реф PO. Попередньо 2026-10-07 — + фон Home-порталу (`home-portal-bg.png`, кластер C).
> `references/keep/` — source of truth. У `clusters/` — **копії**.
> Візуальні мотиви (згруповано): [`MOTIFS.md`](MOTIFS.md).

## Підсумок

| Кластер | Папка | К-сть | Роль |
|---------|-------|------:|------|
| **A** | `clusters/A-atmosphere-cosmic/` | 30 | mood — шари світів, nebula, золоті кільця, світлові стовпи |
| **B** | `clusters/B-atmosphere-organic/` | 27 | mood — world tree, бібліотеки, прірва, земля/кістка/сад + дерево Раю (PO) |
| **C** | `clusters/C-atmosphere-modern-surreal/` | 14 | mood — портали, shattered/modern surreal, матеріали інтер’єру |
| **D** | `clusters/D-product-ui/` | **3** | UI — D03 Paradise desktop/mobile + D03 spiral (PO 2026-10-08); треба ще ≥6 |

Keep total: **75** зображень. Unmapped: **0**.

## Gap: product-UI (D)

D03 (Досягнення / Paradise) закрито PO-рефом. Решта D-слотів — ще synthetic / порожньо.

**Шляхх зараз:** згенерувати synthetic D через Astra —
промпти в [`prompts/03-d-product-ui/`](../prompts/03-d-product-ui/README.md)
(порядок: D01 → D10 materials → destinations → session). Character: Stage Absurd.
Зберігати сюди з префіксом `dNN-…-synth-`.

Пізніше бажано замінити/доповнити 4–6 **реальними** скрінами (Jackbox/Kahoot/event pages).

Слоти:

- [x] D01 hub / home (locked IA) — PO-макет portal-v1: [`../concepts/d01-hub/2026-10-07-portal-v1.png`](../concepts/d01-hub/2026-10-07-portal-v1.png)
- [ ] D10 character materials (Stage Absurd)
- [ ] D02 events / tournaments index
- [x] D03 achievements grid — PO-реф Paradise: [`../clusters/D-product-ui/d03-achievements-paradise-desktop.png`](clusters/D-product-ui/d03-achievements-paradise-desktop.png) (без підзаголовка в продукті — spec C-5)
- [ ] D04 games catalog
- [ ] D05 lobby host
- [ ] D06 lobby player mobile
- [ ] D07 active game
- [ ] D08 tournament poster (detail)
- [ ] D09 training / practice formats

## Правила

- **mood (A–C)** → палітра, світло, матеріали. Не копіювати fantasy layout у продукт.
- **UI (D)** → ієрархія, spacing, компоненти.
- **reject-risk: high** — тримати як «анти-реф» або слабкий mood; не тягнути в Style Lock як основу.

---

## A — atmosphere-cosmic (30)

| Файл | Нотатка | reject-risk |
|------|---------|-------------|
| `a0c2196140fed15ce84a8b3a6030fa5c.jpg` | Nebula mountain | low |
| `e09e770335aa63a4fa4adbea31ea8d69.jpg` | Три плато Heaven/Purgatory/Hell | medium |
| `9a2e1b9494313174ac9af3d0279463a6.jpg` | Стек дисків / astrolabe | medium |
| `43fc0c97f13130c2482f0bd40051c394.jpg` | Стовп світла над узбережжям | low |
| `71542069efddea5329bb52609800a669.jpg` | Золоте місто + кільця хмар | medium |
| `05de1752ae2c660a1d4dcca5bfcc8da7.jpg` | Nested realms map + classical gate | medium |
| `14ff3a41862e14c819d8f9abafd60ea4.jpg` | Babel tower, golden ascent | low |
| `19fdef39c80f076143e503f73de46773.jpg` | Golden river canyon glow | low |
| `27f8623de7f93df14bfe064b7d81509e.jpg` | Arches into nebula | low |
| `2af1f8afc0b8a26ffaa33fac01cc65b4.jpg` | Celestial imperial plaza | medium |
| `36e69e1679b508b170cbeaa6d1cccb45.jpg` | Planet gold cracks + nebula | low |
| `3489cd36bff134fda3f7189a82f31376.jpg` | Gothic corridor in clouds | medium |
| `4716ceb5ed7433f46359df2139b6f970.jpg` | Golden pillar through ringed sky | low |
| `510fa4d3812755a0334f1ca3d4196f52.jpg` | Golden disc path + portal windows | low |
| `756aaa35ab29bfc95e08d33d793f517d.jpg` | Eclipse vortex / ziggurat | low |
| `7e98f2910c3cdc47587b4317a274cedf.jpg` | Throne hall + rose oculus | medium |
| `8c1226ad7e1499adef1e6da717d950a7.jpg` | Nebula fused with world-tree | high |
| `93fdd3f3039ab7e0096717e730dd1578.jpg` | Floating golden ring city | low |
| `9d5c00ea1d7c271e130c80fb57635da9.jpg` | Towers rising through cloud sea | low |
| `a0987c62ac7bae44ca7ed129e75bdd75.jpg` | Cliff under layered cosmic rings | low |
| `b794466e7ef8fceff56df0289aa399c7.jpg` | Stacked planes / celestial rings map | low |
| `ccb88160cc10997057e646c252e8d42c.jpg` | Stacked golden rings + cities | low |
| `df31035db5af0c1375c1a3bd58f6f1b4.jpg` | Monumental stair to radiant arch | medium |
| `e2c6128a83c91f85f3f17e0b23c44732.jpg` | Tiered tower to oculus | low |
| `e72423af722094328b0b91f4a182e926.jpg` | Vertical god-ray pillars | low |
| `ec738ba6b69391f07b35144413527079.jpg` | Golden stardust rivers | low |
| `fe5c6626672779fd3f41b2a37cfe4b34.jpg` | Nave + nebula vault + red portal | low |
| `png-2770369.png` | Classical figure ascending / void light | high |
| `png-3834679.png` | Armored angel on clouds, god rays | medium |
| `png-3978325.png` | Gothic castle + giant red moon | medium |

## B — atmosphere-organic (27)

| Файл | Нотатка | reject-risk |
|------|---------|-------------|
| `03d9c40b2d5d4311a4f107a7da27decb.jpg` | Tree library, teal + amber | low |
| `c4d6148a1d91914546f744cf3a56e7b7.jpg` | Luminous world tree + figure | low |
| `41fa27792ea7740852c507a1c14546ec.jpg` | Falling figure through abyss | medium |
| `0389ca321c53a614d331765a82d2889f.jpg` | Cosmic tree on mountain shore | low |
| `168eaf11a3d981e8fce632af6c03fe11.jpg` | Golden tree on floating island | low |
| `1a27fb3bfd0cca5d7d9ea47a194ca878.jpg` | Hell thorns / gothic castle | high |
| `2d71451c1cfa59ad8faf1ca83841b912.jpg` | Organic dark DNA helix | low |
| `3646053655124b88abf67442142a6fb3.jpg` | Falling figures in red pit | medium |
| `36d98ec01d2789691847ceca24531395.jpg` | Yggdrasil + waterfalls | low |
| `482f84bb2990b9a23e72b7814a73b062.jpg` | Flooded gothic aisle / red portal | medium |
| `4b1c400775a41bf30da178103eab6edc.jpg` | Stairs into misty abyss | low |
| `520c19ad4d1580def606e2a28b44e0b1.jpg` | Conservatory spa / rock waterfall | low |
| `6c17ebe8d68630923f952aaca0f9b126.jpg` | World tree → golden nebula canopy | medium |
| `73dfab69a373edd6409375d5f0f7c19b.jpg` | Carved stone gothic lounge | high |
| `73f0963d30b485f1f857a5cf5aacfc29.jpg` | Gothic hall + reflective pool | medium |
| `85e3a9dda632dc88297efd0ade5423a2.jpg` | Misty glasshouse + roses | low |
| `88b852433225fb20a894466d5caeef39.jpg` | Infernal citadel / lava falls | medium |
| `8cd6ef216973adf4c47ddef196a5eab6.jpg` | Figures around central void | low |
| `aaf76b79f175069f19ae069dce004ee8.jpg` | Dark gothic spires on cliffs | medium |
| `b104826f610aefbce4272a02dd443b0c.jpg` | Misty rose garden + statues | low |
| `c73defb400422020dd1c175d19bb63cb.jpg` | Colossal bone-rib hall | low |
| `e4c64338dc017b49813442acf0112e2e.jpg` | Infernal stone labyrinth | low |
| `ed6e65df5dfdb9f41fcbce68454c6e27.jpg` | Gothic silhouette + tree collage | medium |
| `fb43ead47932fd4860fb8156d3944116.jpg` | Ornate mirror portal in forest | medium |
| `png-3004151.png` | Multi-tier carved wood library | low |
| `paradise-tree-bg-desktop.png` | **Фон Раю (PO 2026-10-08):** золоте дерево на порожнечі, desktop 1440. Page atmosphere F-4.2 / `DC-ACH-010` | low |
| `paradise-tree-bg-mobile.png` | Той самий мотив, mobile 390 crop | low |
| `sinners-bg-desktop.png` | **Фон Грішників (PO 2026-10-08):** кривавий місяць, замок, троянди, desktop. Page atmosphere F-4.13 / `DC-ACH-012` | low |
| `sinners-bg-mobile.png` | Той самий мотив, mobile 390 crop | low |
| `paradise-spiral-bg-desktop.png` | **Фон категорій Раю (PO 2026-10-08):** золота спіраль-гелікс на nebula, desktop 1440. Page atmosphere F-4.3 / F-4.6 / F-4.10 (нова `DC-ACH` атмосфера; F-4.2 лишається на дереві) | low |
| `paradise-spiral-bg-mobile.png` | Той самий мотив, mobile 390 crop | low |

## C — atmosphere-modern-surreal (13)

| Файл | Нотатка | reject-risk |
|------|---------|-------------|
| `25e1b0dc379c0cbd5eb0858363e4860a.jpg` | Utility pole + shattered sky | low |
| `a606f2e15d5674b29bd8f4c783cd6a80.jpg` | Portal doors / elemental gates | low |
| `12d6160e7b1d40c29913dd311dd0cc33.jpg` | Chess queens on storm shore | medium |
| `15902797e3699c2a2f6cde388770362b.jpg` | Warm reflective surreal rocks | low |
| `237fccb4795222a8d3498254d43a7ad9.jpg` | Escher stairs in golden sky | low |
| `3264e7cb47281b8c38f1a480fb165112.jpg` | Portal collage / multi-realm strips | medium |
| `36088aedbf06129a6fb7a795152e455e.jpg` | Dark baroque luxury interior (materials) | medium |
| `406d80a7e0fa87034bee4b50f7ac4f7a.jpg` | Black monoliths + red mist | low |
| `4e554007ceb3b131f69fc2efef3674cd.jpg` | Figure + glowing tablet / golden spiral | medium |
| `a18c6a8cab44df475eca4586f12fae95.jpg` | Statues + floating debris / shattered light | medium |
| `a31aebfdc9658e1a01df48556d2d1b79.jpg` | Skull-arch portal to underworld | medium |
| `cbc73f3032e0a25db9409dd3be454ede.jpg` | Stained-glass portal doors | low |
| `ee73a8550ecc742c1928b245d2b65acf.jpg` | Ornate fantasy card frame (не product UI) | medium |
| `home-portal-bg.png` | **Фон Home (PO 2026-10-07):** зал із трьома дверима — вогняні / холодні небесні сходи / золоті хмари. У продукті дзеркалити по горизонталі (світлі двері зліва, вогонь справа) — див. `briefs/home-ux-locked.md` | low |

## D — product-ui (2)

| Файл | Нотатка | reject-risk |
|------|---------|-------------|
| `d03-achievements-paradise-desktop.png` | **PO 2026-10-08:** Досягнення на дереві Раю — H1, pill «Грішники», сітка 4×, прогрес-бар. Підзаголовок у рефі **не брати** (F-4.2 C-5) | low |
| `d03-achievements-paradise-mobile.png` | Той самий клімат, 2 колонки, pill під H1 | low |
| `d03-achievements-paradise-spiral-desktop.png` | **PO 2026-10-08:** F-4.3 на золотій спіралі — H1 «Fun & Party» + прогрес, пошук + фільтри, pill «Запропонувати ачівку», сітка 3× з inline confirm/cancel. Атмосфера категорій (≠ дерево F-4.2) | low |

## Топ для moodboard (рекомендація)

Перед Astra візьми **по 4** з low reject-risk:

- **A:** `a0c21961…`, `43fc0c97…`, `19fdef39…`, `ccb88160…`
- **B:** `03d9c40b…`, `c4d6148a…`, `36d98ec0…`, `png-3004151.png`
- **C:** `25e1b0dc…`, `a606f2e1…`, `237fccb4…`, `cbc73f30…`

Потім — [`../moodboards/README.md`](../moodboards/README.md) і [`../checklists/step-1-triage.md`](../checklists/step-1-triage.md) §3 (добрати D).
