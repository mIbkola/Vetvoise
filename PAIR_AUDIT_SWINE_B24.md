# Аудит пар «Свиньи × препарат» — батч 24 (10 пар)

Данные из `drugs_calc.json`/`verified_dosages.json`; источники не подтверждены; расхождения calc/ver зафиксированы в сводке `SWINE_DIFF_SUMMARY.md`.

| id | Препарат | Было (Свиньи) | calc/ver | Расхождения | Концентрация |
|---:|---|---|---|---|---|
| 595 | ВНИИЗЖ-Свайн-ПС | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "frequency": "по схеме вакцин | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "dose_unit": "fixed", "method": "внутримышечн | course_days: calc='7 суток' ver='7', method: calc=None ver='внутримышечно или подкожно', route: calc='внутримышечно или подкожно' ver=None | conc=50.0 | global: мг/мл 0 (0–0) |
| 597 | Кальция борглюконат | calc=null | ver=null | доаудитных расхождений нет | conc=100.0 | global: мг/мл 0.75 (0.25–1) |
| 598 | Бактимаг®-О | calc={"dose_per_kg": 5, "dose_min": 4.0, "dose_max": 6.0, "dose_unit": "мг/кг", "method": "Перорально", " | ver={"dose_per_kg": 5.0, "dose_min": 4.0, "dose_max": 6.0, "dose_unit": "мг/кг", "method": "Перорально", | доаудитных расхождений нет | conc=100.0 | global: МЕ/мл 10.0 (8.0–12.0) |
| 599 | Бромколин®-О | calc={"dose_per_kg": 0, "dose_min": 1, "dose_max": 1, "dose_unit": "fixed", "method": "перорально (с водо | ver={"dose_per_kg": 0, "dose_min": 1, "dose_max": 1, "dose_unit": "fixed", "method": "перорально (с водо | course_days: calc='3-5 дней' ver=None | conc=100.0 | global: мг/мл 0 (0–0) |
| 601 | Окситетрамаг 20® | calc={"dose_per_kg": 10, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "Инъекционно" | ver={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "Инъекционн | доаудитных расхождений нет | conc=200.0 | global: мг/мл 10 (8.0–12.0) |
| 602 | Карнифел PCH | calc=null | ver=null | доаудитных расхождений нет | conc=1.0 | global: мг/мл 0 (0–0) |
| 605 | ВНИИЗЖ-Свайн-П | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "frequency": "по схеме вакцин | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "dose_unit": "fixed", "method": "внутримышечн | course_days: calc='7 суток' ver='7', method: calc=None ver='внутримышечно или подкожно', route: calc='внутримышечно или подкожно' ver=None | conc=50.0 | global: мг/мл 0 (0–0) |
| 606 | Доксимаг®-О | calc={"dose_per_kg": 5, "dose_min": 4.0, "dose_max": 6.0, "dose_unit": "мг/кг", "method": "Перорально", " | ver={"dose_per_kg": 5.0, "dose_min": 4.0, "dose_max": 6.0, "dose_unit": "мг/кг", "method": "Перорально", | доаудитных расхождений нет | conc=100.0 | global: мг/мл 10.0 (8.0–12.0) |
| 607 | Кальция хлорид 10% раствор для инъекций | calc=null | ver=null | доаудитных расхождений нет | conc=100.0 | global: мг/мл 0.15 (0.1–0.5) |
| 608 | Метрамаг® | calc={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "frequency": "1 раз в | ver={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "frequency": "1 раз в | доаудитных расхождений нет | conc=100.0 | global: МЕ/мл 10.0 (8.0–12.0) |
