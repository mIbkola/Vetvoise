# Аудит пар «КРС × препарат» — батч 75 (10 пар)

Данные из `drugs_calc.json`/`verified_dosages.json`; источники по доступным страницам — не подтверждены; правки по подтверждённым дозам в батчах по собакам/кошкам (по аналогии).

| id | Препарат | Было (КРС) | calc/ver | Доаудитные расхождения | Концентрация |
|---:|---|---|---|---|---|
| 1866 | Цефтонит® | calc={"dose_per_kg": 2.2, "dose_min": 1.76, "dose_max": 2.64, "dose_unit": "мг/кг", "method": "Инъекционн | ver={"dose_per_kg": 2.2, "dose_min": 1.76, "dose_max": 2.64, "dose_unit": "мг/кг", "method": "Инъекционн | доаудитных расхождений нет | conc=50.0 | global: мг/мл 1 (0.8–1.2) |
| 1868 | Актионис | calc={"dose_per_kg": 2.2, "dose_min": 1.76, "dose_max": 2.64, "dose_unit": "мг/кг", "method": "Инъекционн | ver={"dose_per_kg": 2.2, "dose_min": 1.76, "dose_max": 2.64, "dose_unit": "мг/кг", "method": "Инъекционн | доаудитных расхождений нет | conc=50.0 | global: мг/мл 1 (0.8–1.2) |
| 1870 | Шампунь инсектицидный для кошек Мисс Кисс | calc=null | ver=null | доаудитных расхождений нет | conc=500.0 | global: мг/мл 10 (5–10) |
| 1875 | КРУСТАЦИД® | calc={"dose_per_kg": 0.75, "dose_unit": "мг/кг", "frequency": "1 раз в сутки", "notes": "Из файла: ДЕЛЬЦИ | ver={"dose_per_kg": 0.75, "dose_unit": "мг/кг", "frequency": "1 раз в сутки", "notes": "Из файла: ДЕЛЬЦИ | доаудитных расхождений нет | conc=10.0 | global: мг/мл 0.75 (0.6–0.9) |
| 1876 | Трисульфон® | calc={"dose_per_kg": 25, "dose_unit": "мг/кг", "dose_min": 20, "dose_max": 25, "method": "перорально", "f | ver={"dose_per_kg": 25.0, "dose_min": 20.0, "dose_max": 25.0, "dose_unit": "мг/кг", "method": "пероральн | доаудитных расхождений нет | conc=40.0 | global: мг/мл 26.6667 (20–30) |
| 1879 | Иммуновет 1Ин | calc=null | ver=null | доаудитных расхождений нет | conc=2.0 | global: мг/мл 0 (0–0) |
| 1883 | Флоридокс® | calc={"dose_per_kg": 5, "dose_min": 4.0, "dose_max": 6.0, "dose_unit": "мг/кг", "method": "Инъекционно",  | ver={"dose_per_kg": 5.0, "dose_min": 4.0, "dose_max": 6.0, "dose_unit": "мг/кг", "method": "Инъекционно" | доаудитных расхождений нет | conc=50.0 | global: мг/мл 5 (4.0–6.0) |
| 1886 | Туберкулин очищенный (ППД) для птиц | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "frequency": "3 раза", "route | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "dose_unit": "fixed", "method": "внутрикожно" | course_days: calc='в течение 21 дн' ver='21', method: calc=None ver='внутрикожно', route: calc='внутрикожно' ver=None | conc=5.0 | global: мг/мл 0 (0–0) |
| 1889 | Метакам® | calc={"dose_per_kg": 0.5, "dose_min": 0.2, "dose_max": 0.5, "method": "внутримышечно / подкожно", "freque | ver={"dose_per_kg": 0.5, "dose_min": 0.2, "dose_max": 0.5, "method": "внутримышечно / подкожно", "freque | доаудитных расхождений нет | conc=20.0 | global: мг/мл 0.2 (0.1–0.2) |
| 1892 | Аправет® водорастворимый порошок | calc={"dose_per_kg": 20.0, "dose_min": 16.0, "dose_max": 24.0, "dose_unit": "мг/кг", "frequency": "1 раз  | ver={"dose_per_kg": 20.0, "dose_min": 16.0, "dose_max": 24.0, "dose_unit": "мг/кг", "frequency": "1 раз  | доаудитных расхождений нет | conc=500.0 | global: мг/мл 20.0 (16.0–24.0) |
