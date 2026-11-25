# Аудит пар «КРС × препарат» — батч 24 (10 пар)

Данные из `drugs_calc.json`/`verified_dosages.json`; источники по доступным страницам — не подтверждены; правки по подтверждённым дозам в батчах по собакам/кошкам (по аналогии).

| id | Препарат | Было (КРС) | calc/ver | Доаудитные расхождения | Концентрация |
|---:|---|---|---|---|---|
| 591 | Гентамицина сульфат 4 % раствор | calc={"dose_per_kg": 3, "dose_min": 2.4, "dose_max": 3.6, "dose_unit": "мг/кг", "method": "Инъекционно",  | ver={"dose_per_kg": 3.0, "dose_min": 2.4, "dose_max": 3.6, "dose_unit": "мг/кг", "method": "Инъекционно" | доаудитных расхождений нет | conc=40.0 | global: мг/мл 1.7 (1.36–2.04) |
| 594 | Супримицин® | calc={"dose_per_kg": 4, "dose_min": 2, "dose_max": 6, "method": "внутримышечно", "frequency": "2 раза в с | ver={"dose_per_kg": 4.0, "dose_min": 2.0, "dose_max": 6.0, "method": "внутримышечно", "frequency": "2 ра | доаудитных расхождений нет | conc=40.0 | global: мг/мл 4 (2–6) |
| 596 | ЛЕОМИНОР | calc=null | ver=null | доаудитных расхождений нет | conc=1.0 | global: мг/мл 0 (0–0) |
| 597 | Кальция борглюконат | calc={"dose_per_kg": 1, "dose_unit": "мл/кг", "dose_min": 0.5, "dose_max": 1, "method": "внутривенно (мед | ver={"dose_per_kg": 1.0, "dose_min": 0.5, "dose_max": 1.0, "dose_unit": "мл/кг", "method": "внутривенно  | доаудитных расхождений нет | conc=100.0 | global: мг/мл 0.75 (0.25–1) |
| 600 | Магэстрофан® | calc={"dose_per_kg": 0.003, "dose_min": 0.002, "dose_max": 0.004, "dose_unit": "мг/кг", "method": "Инъекц | ver={"dose_per_kg": 0.003, "dose_min": 0.002, "dose_max": 0.004, "dose_unit": "мг/кг", "method": "Инъекц | доаудитных расхождений нет | conc=0.25 | global: мг/мл 0.01 (0.008–0.012) |
| 601 | Окситетрамаг 20® | calc={"dose_per_kg": 10, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "Инъекционно" | ver={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "Инъекционн | доаудитных расхождений нет | conc=200.0 | global: мг/мл 10 (8.0–12.0) |
| 602 | Карнифел PCH | calc=null | ver=null | доаудитных расхождений нет | conc=1.0 | global: мг/мл 0 (0–0) |
| 606 | Доксимаг®-О | calc={"dose_per_kg": 10, "dose_min": 5, "dose_max": 10, "method": "перорально", "frequency": "1 раз в сут | ver={"dose_per_kg": 10.0, "dose_min": 5.0, "dose_max": 10.0, "method": "перорально", "frequency": "1 раз | доаудитных расхождений нет | conc=100.0 | global: мг/мл 10.0 (8.0–12.0) |
| 607 | Кальция хлорид 10% раствор для инъекций | calc={"dose_per_kg": 0.2, "dose_unit": "мл/кг", "dose_min": 0.1, "dose_max": 0.3, "method": "внутривенно  | ver={"dose_per_kg": 0.2, "dose_min": 0.1, "dose_max": 0.3, "dose_unit": "мл/кг", "method": "внутривенно  | доаудитных расхождений нет | conc=100.0 | global: мг/мл 0.15 (0.1–0.5) |
| 608 | Метрамаг® | calc={"dose_per_kg": 5, "dose_min": 5, "dose_max": 10, "method": "перорально", "frequency": "1 раз в сутк | ver={"dose_per_kg": 5.0, "dose_min": 5.0, "dose_max": 10.0, "method": "перорально", "frequency": "1 раз  | доаудитных расхождений нет | conc=100.0 | global: МЕ/мл 10.0 (8.0–12.0) |
