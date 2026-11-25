# Аудит пар «КРС × препарат» — батч 74 (10 пар)

Данные из `drugs_calc.json`/`verified_dosages.json`; источники по доступным страницам — не подтверждены; правки по подтверждённым дозам в батчах по собакам/кошкам (по аналогии).

| id | Препарат | Было (КРС) | calc/ver | Доаудитные расхождения | Концентрация |
|---:|---|---|---|---|---|
| 1843 | АСД® -3Ф - Антисептик-стимулятор Дорогова фракция 3 | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "frequency": "1-2 раза в день | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "dose_unit": "fixed", "method": "внутрь, нару | course_days: calc='3-5 дней' ver='3-5', method: calc=None ver='внутрь, наружно', route: calc='внутрь, наружно' ver=None | conc=None | global: мг/мл 0 (0–0) |
| 1844 | Мазь стрептоцидовая 10% | calc=null | ver=null | доаудитных расхождений нет | conc=None | global: мг/мл 0 (0–0) |
| 1845 | Мазь цинковая 10% | calc=null | ver=null | доаудитных расхождений нет | conc=10000.0 | global: мг/мл 3.0 (2.4–3.6) |
| 1847 | Цемай | calc={"dose_per_kg": 2.2, "dose_min": 1.76, "dose_max": 2.64, "dose_unit": "мг/кг", "method": "Инъекционн | ver={"dose_per_kg": 2.2, "dose_min": 1.76, "dose_max": 2.64, "dose_unit": "мг/кг", "method": "Инъекционн | доаудитных расхождений нет | conc=50.0 | global: мг/мл 1 (0.8–1.2) |
| 1853 | Кетомай | calc={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "frequency": "1 раз в | ver={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "frequency": "1 раз в | доаудитных расхождений нет | conc=100.0 | global: мг/мл 10.0 (8.0–12.0) |
| 1855 | Стенорол® 0,6% | calc={"dose_per_kg": 0.001, "dose_unit": "мг/кг", "method": "перорально", "frequency": "1 раз в день", "n | ver={"dose_per_kg": 0.001, "dose_unit": "мг/кг", "method": "перорально", "frequency": "1 раз в день", "n | доаудитных расхождений нет | conc=6.0 | global: мг/г 0.001 (0.0008–0.0012) |
| 1856 | Цифлунит® | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "frequency": "1 раз в месяц", | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "dose_unit": "fixed", "method": "наружно", "f | method: calc=None ver='наружно', route: calc='наружно' ver=None | conc=10.0 | global: мг/мл 0 (0–0) |
| 1858 | Доксмай | calc={"dose_per_kg": 10, "dose_min": 5, "dose_max": 10, "method": "перорально", "frequency": "1 раз в сут | ver={"dose_per_kg": 10.0, "dose_min": 5.0, "dose_max": 10.0, "method": "перорально", "frequency": "1 раз | доаудитных расхождений нет | conc=100.0 | global: мг/мл 10.0 (8.0–12.0) |
| 1860 | ВИТАМЭЛАМ | calc={"dose_per_kg": 0.05, "dose_unit": "мл/кг", "dose_min": 0.03, "dose_max": 0.05, "method": "внутримыш | ver={"dose_per_kg": 0.05, "dose_min": 0.03, "dose_max": 0.05, "dose_unit": "мл/кг", "method": "внутримыш | доаудитных расхождений нет | conc=0.1 | global: мг/мл 0.075 (0.03–0.1) |
| 1861 | Мазь ихтиоловая 10% | calc=null | ver=null | доаудитных расхождений нет | conc=None | global: мг/мл 0 (0–0) |
