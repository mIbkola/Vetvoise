# Точечная проверка пар «Кошки × препарат» — батч 33 (10 пар)

| id | Препарат | Доза в базе | Что говорит инструкция | Статус | Источник |
|---:|---|---|---|---|---|
| 931 | Тиалонг® 80% Feed | 3 мг/кг | Только свиньи, 5–10 мг/кг с кормом | ПРОТИВОРЕЧИЕ ВИДА — не меняли | https://www.nita-farm.ru/instrukcii/instr-tialong-80-feed/ |
| 933 | Инсектал комбо К | 0,003 мг/кг | Капли 0,4 / 0,8 / 1,5 мл по массе; <1 кг — 0,05 мл/0,5 кг; 1 раз в 4–6 недель | **ИСПРАВЛЕНО** — fixed_dose | https://www.sibagrotrade.com/catalogzoo/preparaty_dlya_mdzh/protivoparazitarnye_sredstva_mdzh/zashchita_ot_blokh_kleshchey_i_dr_mdzh/68163/ |
| 937 | Тиалонг® 45% WS | 3 мг/кг | Свиньи и птица; кошек нет | ПРОТИВОРЕЧИЕ ВИДА — не меняли | https://www.nita-farm.ru/instrukcii/instr-tialong-45-ws/ |
| 938 | Гепатолюкс PROtect суспензия | 1,5 мг/кг, 3 дня | 1 мл на 5 кг, 2 раза/сут, 20–60 дней | **ИСПРАВЛЕНО** — fixed_dose | https://vetsnab.info/vetpreparaty/gepatolyuks-protect-suspenziya/ |
| 941 | Фоллигон | «— МЕ/кг» | ГСЖК 1000/5000 МЕ во флаконе; дозы абсолютные, МЕ/кг нет; кошек нет | ПРОТИВОРЕЧИЕ ВИДА — не меняли | https://vetsnab.info/vetpreparaty/folligon/ |
| 944 | Таблетки тетрациклина | 10 мг/кг | Только молодняк сельхозживотных; кошек нет | ПРОТИВОРЕЧИЕ ВИДА — не меняли | https://vetsnab.info/vetpreparaty/tabletki-tetracziklina/ |
| 946 | Чистотел Максимум спрей | 7,5 мг/кг | Наружно 1,5–3,0 мл/кг; 1 нажатие = 0,13 мл; повторно ≤1 раза/мес | **ИСПРАВЛЕНО** — fixed_dose | https://vetsnab.info/vetpreparaty/chistotel-maksimum-sprej/ |
| 947 | Инспектор Мини | 0,1 мг/кг | 0,5–2 кг — 0,4 мл; >2 кг — 0,2 мл/кг; 1 раз в месяц | **ИСПРАВЛЕНО** — fixed_dose | https://vetsnab.info/vetpreparaty/inspektor-mini/ |
| 948 | Гепатолюкс PROtect таблетки | 1,5 мг/кг | 1 таблетка на 5 кг, 2 раза/сут, 20–60 дней | **ИСПРАВЛЕНО** — fixed_dose | https://vetsnab.info/vetpreparaty/gepatolyuks-protect-tabletki/ |
| 949 | Марбофлоцин®10% | 2 мг/кг перорально | КРС и свиньи 2 мг/кг в/м; кошек нет | ПРОТИВОРЕЧИЕ ВИДА — не меняли | https://vetsnab.info/vetpreparaty/marbofloczin10/ |

Правки применяет `scripts/fix_pair_cats_b33.py`; лог — `PAIR_FIXES_CATS_B33.md`.
