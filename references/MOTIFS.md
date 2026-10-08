# Візуальні мотиви Keep (A–C)

> Окремий digests від [`INDEX.md`](INDEX.md).  
> Джерело: 68 рефів у `keep/` → кластери A/B/C.  
> **D (product-UI)** тут майже відсутній — додати після synthetic Astra.

**Як читати:** мотиви = що *брати в UI* (колір, світло, матеріал, метафора розділення).  
Не брати: літеральний fantasy layout, gothic ornament як систему, ангелів/демонів.

---

## 1. Карта зверху вниз

| Група мотивів | Суть | Де сильніше | Для UI |
|---------------|------|-------------|--------|
| **Вертикальна подорож** | Світло вгору / спуск униз / стовп світла | A, B | Ієрархія зон на Home; scroll story |
| **Шари / кільця / диски** | Кілька рівнів реальності один над одним | A | 3 зони як «шари», не як 3 однакові картки |
| **Портал / двері / арка** | Поріг між станами | C, частково A | CTA-входи, переходи між модулями |
| **Дерево / знання / ріст** | World tree, бібліотека в дереві | B | Рай / теорія / «збір» ачівок (м’яко) |
| **Прірва / падіння / тиск** | Спуск, вузька ущелина, червоне сяйво | B | Пекло / інтенсивність — тон, не «вогонь скрізь» |
| **Сцена / подія / кільце** | Spotlight, процесія, oculus | A | Чистилище / турнір |
| **Сучасний міф** | Звичайний об’єкт + епічне небо | C | «Не середньовічний Данте» — головний вайб сучасності |
| **Темна розкіш (матеріали)** | Оксамит, золото, кристал — інтер’єр | C (мало) | Обережно: лише матеріали кнопок/поверхонь |

---

## 2. Палітри (повторювані)

### 2.1 Cosmic gold on void (A-dominant)

- **Фон:** deep charcoal / space black / midnight blue  
- **Акцент:** amber–gold–champagne light  
- **Другорядне:** cool blue nebula, soft white rim light  
- **UI-переклад:** dark mode + один теплий акцент; зони різнити температурою, не неоном

**Якірні рефи:** nebula mountain (`a0c21961…`), light pillar coast (`43fc0c97…`), golden river canyon (`19fdef39…`), stacked rings (`ccb88160…`)

### 2.2 Teal + amber biophilic (B-dominant)

- **Фон:** deep teal / indigo shadow  
- **Акцент:** candle amber / warm wood glow  
- **Другорядне:** cream book spines, soft particles  
- **UI-переклад:** «знання / колекція» без angel kitsch; хороше для ачівок і теорії

**Якірні рефи:** tree library (`03d9c40b…`), luminous world tree (`c4d6148a…`), carved wood library PNG

### 2.3 Infernal red–black (B, частково C)

- **Фон:** near-black, rock, mist  
- **Акцент:** crimson / molten orange (внутрішнє світло, не neon pink)  
- **UI-переклад:** Пекло / інтенсив practice — темніша поверхня + теплий warning-акцент; **не** lakes of fire fullscreen

**Якірні рефи:** red pit (`36460536…`), monoliths red mist (`406d80a7…`), infernal labyrinth (`e4c64338…`)  
**Reject-risk high:** thorn hell gothic (`1a27fb3b…`) — анти-реф

### 2.4 Soft gold–cloud paradise (A)

- **Фон:** mist, cloud sea, pale stone  
- **Акцент:** white-gold god rays  
- **UI-переклад:** Рай — світліші поверхні / більше повітря; обережно з «ангельським» кітчем (`png-3834679` — medium)

### 2.5 Warm surreal dusk (C)

- **Фон:** burnt orange / sepia / reflective water  
- **Акцент:** soft specular highlights  
- **UI-переклад:** Чистилище / promo — «golden hour» без fantasy tower

**Якір:** reflective rocks (`15902797…`)

### 2.6 Monochrome noir drama (C)

- **Ч/б або near-mono**, високий контраст  
- **UI-переклад:** рідко як ціла тема; можна для photo treatments / promo slides

**Якір:** chess queens storm (`12d6160e…`) — medium gothic ornament risk

---

## 3. Композиційні патерни

### M1 — Vertical axis / god-ray pillar
Світло ріже кадр зверху вниз.  
→ Home promo або зона Чистилище: сильний вертикальний акцент; у UI — не обов’язково промінь, а **чітка вісь ієрархії**.

### M2 — Stacked realms / plates / rings
Кілька горизонтальних «світів» або концентричних кілець.  
→ **Три зони продукту** як три шари з різною температурою (не три клони карток).

### M3 — Threshold / portal / door row
Двері, арки, stained glass, skull-arch.  
→ Кожен модуль = «вхід»; на Home — кілька CTA всередині зони, не один «Перейти».

### M4 — World tree / library growth
Дерево як вісь + знання / сходи / полиці.  
→ Рай (збір) і Пекло/теорія (ріст навички); матеріал wood/teal.

### M5 — Abyss / descent
Падіння, вузька ущелина, червоний тунель.  
→ Пекло: глибший contrast, менше «милого»; без horror-spam.

### M6 — Shattered / fragmented sky
Сучасний предмет + розірване небо.  
→ Найкращий аргумент «сучасний міф» проти old Dante.

### M7 — Endless stair / Escher path
Сходи в хмарах, подорож без фінішу.  
→ Імпро / practice flow (без фінального подіуму) — процес, не перемога.

### M8 — Event plaza / oculus / procession
Натовп, сцена, кільце світла.  
→ Турнір / афіша: «подія», не «данж».

### M9 — Intimate garden / glasshouse / roses
Туман, рослини, камінь.  
→ М’який ліричний тон (обережно — не wedding gothic).

### M10 — Baroque dark luxury interior
Оксамит, золота рама, кристал.  
→ Лише **матеріали** (surface, accent metal); не як chrome всього UI (`36088aed…` medium/SKIP-кандидат).

---

## 4. Мотиви → зони продукту

| Зона | Брати з рефів | Не брати |
|------|---------------|----------|
| **Рай** | 2.2 teal+amber; M4 tree/library; світліший air з 2.4 | Ангели, херувими, «райська» кітч-золота ікона |
| **Чистилище** | 2.1 gold void; M1 pillar; M8 event/oculus; 2.5 dusk | Esports neon bracket, середньовічний пергамент |
| **Пекло** | 2.3 red-black; M5 abyss; dark studio | Fullscreen lava, skull spam, thorn cathedral як UI |
| **Home promo** | M6 modern myth; M1/M8 event energy; slider як «афіша» | Fantasy poster на весь viewport без UI chrome |
| **Ачівки** | Grid-friendly calm з 2.2; collectible, не loot | RPG inventory rarity glow |
| **Лобі / live** | Читабельність, contrast з 2.1; «show console» | Arcade HUD |

---

## 5. Текстури й матеріали (для Style Lock)

| Матеріал | Звідки | UI-застосування |
|----------|--------|-----------------|
| Matte charcoal / void | A | App background |
| Soft gold glow (internal light) | A, B | Accent, focus, CTA hover |
| Wood / bark / paper grain | B | Cards? краще обмежити — або лише illustration slots |
| Stone / carved rib | B | Anti-pattern якщо стає chrome |
| Mist / film grain / particles | A, B | Atmosphere behind UI, low opacity |
| Glass / stained portal | C | Optional modal / zone divider metaphor |
| Velvet + gilt | C interior | Max as button metal / divider — не меблі на екрані |

---

## 6. «Так / ні» для Astra і Figma

### Так (повторювати)
- Dark base + **один** теплий світловий акцент  
- Вертикальна ієрархія / шари зон  
- Поріг-вхід як CTA  
- Сучасний предмет + епічне світло (міф без середньовіччя)  
- Різна **температура** зон при одній системі компонентів  

### Ні (reject-патерни з Keep)
- Neon / cyber glow  
- Angels, demons, skulls як бренд  
- Gothic ornament як UI kit  
- Fantasy map / D&D planes як головний layout  
- Baroque room як весь продукт  
- Три однакові картки «Рай / Пекло / Чистилище» без внутрішніх дій  

---

## 7. Кластери A/B/C одним абзацом

- **A Cosmic** — епічний масштаб, золоте світло в порожнечі, кільця й стовпи, «шари світів». База для dark + gold і для Чистилища/promo.  
- **B Organic** — дерево, бібліотека, прірва, кістка/сад: тіло й земля. База для Раю (збір/знання) і Пекла (спуск/інтенсив).  
- **C Modern-surreal** — двері-портали, shattered sky, Escher, інколи матеріали luxury. База для «це 2026, не ілюмінований манускрипт».  

---

## 8. Короткий словник для промптів

Копіюй фрагментами в Astra:

```text
Motif pack (atmosphere only):
- dark matte void + soft amber/gold internal light
- vertical hierarchy / layered zones with different color temperature
- portal-as-entry metaphor for CTAs
- modern-myth feel (everyday + epic light), no medieval Dante chrome
- zone Рай: gold tree on void as page atmosphere + amber progress (PO 2026-10-08); not teal-air, not angel kitsch
- zone Чистилище: stage/event gold spotlight
- zone Пекло: deeper red-black focus studio, no literal fire UI
```

---

## 9. Що оновити пізніше

- [ ] Після synthetic D — додати § «Motifs from product-UI density»
- [x] Home UX LOCKED (PO): header brand+avatar → slider → 3 equal columns — `briefs/home-ux-locked.md`; next iters = art direction only (`d01-hub.md` v4)
- [ ] Після Style Lock — викреслити відхилені мотиви, залишити 1 «locked pack»
- [ ] При бажанні: 1 колаж на мотив M1–M6 у `moodboards/motifs/`  

Пов’язано: [`INDEX.md`](INDEX.md) · [`../moodboards/README.md`](../moodboards/README.md) · [`../style-lock/STYLE-LOCK.md`](../style-lock/STYLE-LOCK.md)
