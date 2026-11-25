# Аудит пар «КРС × препарат» — батч 40 (10 пар)

Данные из `drugs_calc.json`/`verified_dosages.json`; источники по доступным страницам — не подтверждены; правки по подтверждённым дозам в батчах по собакам/кошкам (по аналогии).

| id | Препарат | Было (КРС) | calc/ver | Доаудитные расхождения | Концентрация |
|---:|---|---|---|---|---|
| 958 | Катобевит® | calc={"dose_per_kg": 10, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "Инъекционно" | ver={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "Инъекционн | доаудитных расхождений нет | conc=100.0 | global: мг/мл 10 (8.0–12.0) |
| 963 | Кетопроф | calc={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "frequency": "1 раз в | ver={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "frequency": "1 раз в | доаудитных расхождений нет | conc=100.0 | global: мг/мл 10.0 (8.0–12.0) |
| 965 | Кайод таблетки | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "frequency": "1-2 раза в день | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "dose_unit": "fixed", "method": "наружно", "f | course_days: calc='3-5 дней' ver='3-5', method: calc=None ver='наружно', route: calc='наружно' ver=None | conc=3.0 | global: мг/мл 6.6667 (5.3333–8.0) |
| 966 | Новокаин 0,5%, 2% раствор для инъекций | calc=null | ver=null | доаудитных расхождений нет | conc=20.0 | global: мг/мл 5.0 (2.0–10.0) |
| 967 | Эстрофантин® | calc={"dose_per_kg": 0.003, "dose_min": 0.002, "dose_max": 0.004, "dose_unit": "мг/кг", "method": "Инъекц | ver={"dose_per_kg": 0.003, "dose_min": 0.002, "dose_max": 0.004, "dose_unit": "мг/кг", "method": "Инъекц | доаудитных расхождений нет | conc=0.25 | global: мг/мл 0.01 (0.008–0.012) |
| 969 | Септо-спрей | calc=null | ver=null | доаудитных расхождений нет | conc=30.0 | global: мг/мл 0 (0–0) |
| 970 | Мазь ихтиоловая 10% | calc=null | ver=null | доаудитных расхождений нет | conc=10000.0 | global: мг/мл 0 (0–0) |
| 973 | Лацилин-нео | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "frequency": "2–3 раза в сутк | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "dose_unit": "fixed", "method": "по инструкци | method: calc=None ver='по инструкции', route: calc='по инструкции' ver=None | conc=None | global: мг/мл 0 (0–0) |
| 974 | Веткокцин | calc={"dose_per_kg": 15, "dose_min": 12.0, "dose_max": 18.0, "dose_unit": "мг/кг", "method": "Перорально" | ver={"dose_per_kg": 15.0, "dose_min": 12.0, "dose_max": 18.0, "dose_unit": "мг/кг", "method": "Пероральн | доаудитных расхождений нет | conc=50.0 | global: мг/мл 15 (12.0–18.0) |
| 975 | Амоксициллин 15% ЛА | calc={"dose_per_kg": 10, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "Инъекционно" | ver={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "Инъекционн | доаудитных расхождений нет | conc=150.0 | global: мг/мл 10 (8.0–12.0) |
