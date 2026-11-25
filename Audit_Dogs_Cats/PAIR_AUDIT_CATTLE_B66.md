# Аудит пар «КРС × препарат» — батч 66 (10 пар)

Данные из `drugs_calc.json`/`verified_dosages.json`; источники по доступным страницам — не подтверждены; правки по подтверждённым дозам в батчах по собакам/кошкам (по аналогии).

| id | Препарат | Было (КРС) | calc/ver | Доаудитные расхождения | Концентрация |
|---:|---|---|---|---|---|
| 1686 | Мазь Яхалимп® | calc=null | ver=null | доаудитных расхождений нет | conc=10000.0 | global: мг/мл 0 (0–0) |
| 1688 | Эструмейт® | calc={"dose_per_kg": 0.01, "dose_unit": "мг/кг", "frequency": "1 раз в сутки", "notes": "Из файла: Лютеос | ver={"dose_per_kg": 0.01, "dose_unit": "мг/кг", "frequency": "1 раз в сутки", "notes": "Из файла: Лютеос | доаудитных расхождений нет | conc=0.25 | global: мг/мл 0.0077 (0.0061–0.0092) |
| 1689 | Мазь ихтиоловая 10% и 20% | calc=null | ver=null | доаудитных расхождений нет | conc=None | global: мг/мл 0 (0–0) |
| 1690 | Мазь серная простая | calc=null | ver=null | доаудитных расхождений нет | conc=33000.0 | global: мг/мл 0 (0–0) |
| 1691 | Мазь цинковая | calc=null | ver=null | доаудитных расхождений нет | conc=None | global: мг/мл 3.0 (2.4–3.6) |
| 1692 | Ивермек® | calc={"dose_per_kg": 0.2, "dose_min": 0.1, "dose_max": 0.3, "method": "подкожно", "frequency": "однократн | ver={"dose_per_kg": 0.2, "dose_min": 0.1, "dose_max": 0.3, "method": "подкожно", "frequency": "однократн | доаудитных расхождений нет | conc=10.0 | global: мг/мл 0.3 (0.3–0.3) |
| 1694 | ФЛАЙБЛОК® | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "frequency": "1 раз в месяц", | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "dose_unit": "fixed", "method": "наружно", "f | method: calc=None ver='наружно', route: calc='наружно' ver=None | conc=10.0 | global: мг/мл 0 (0–0) |
| 1697 | Альбамелин® | calc={"dose_per_kg": 7.5, "dose_min": 6.0, "dose_max": 9.0, "dose_unit": "мг/кг", "method": "Перорально", | ver={"dose_per_kg": 7.5, "dose_min": 6.0, "dose_max": 9.0, "dose_unit": "мг/кг", "method": "Перорально", | доаудитных расхождений нет | conc=100.0 | global: мг/г 7.5 (6.0–9.0) |
| 1700 | "ТРИВАК" | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "frequency": "по схеме вакцин | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "dose_unit": "fixed", "method": "внутримышечн | method: calc=None ver='внутримышечно или подкожно', route: calc='внутримышечно или подкожно' ver=None | conc=5.0 | global: мг/мл 0 (0–0) |
| 1701 | Эксенел стерильный порошок | calc={"dose_per_kg": 2.2, "dose_min": 1.76, "dose_max": 2.64, "dose_unit": "мг/кг", "method": "Инъекционн | ver={"dose_per_kg": 2.2, "dose_min": 1.76, "dose_max": 2.64, "dose_unit": "мг/кг", "method": "Инъекционн | доаудитных расхождений нет | conc=60.0 | global: мг/мл 1 (0.8–1.2) |
