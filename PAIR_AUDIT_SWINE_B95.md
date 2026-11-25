# Аудит пар «Свиньи × препарат» — батч 95 (8 пар)

Данные из `drugs_calc.json`/`verified_dosages.json`; источники не подтверждены; расхождения calc/ver зафиксированы в сводке `SWINE_DIFF_SUMMARY.md`.

| id | Препарат | Было (Свиньи) | calc/ver | Расхождения | Концентрация |
|---:|---|---|---|---|---|
| 2388 | Антибак ПРО | calc={"dose_per_kg": 2.5, "dose_min": 2.5, "dose_max": 5, "method": "внутрь", "frequency": "1 раз в сутки | ver={"dose_per_kg": 2.5, "dose_min": 2.5, "dose_max": 5.0, "method": "внутрь", "frequency": "1 раз в сут | доаудитных расхождений нет | conc=500 мг | global: мг/мл 5 (2.5–10) |
| 2389 | Новомек | calc={"dose_per_kg": 0.3, "dose_min": 0.24, "dose_max": 0.36, "dose_unit": "мг/кг", "method": "Инъекционн | ver={"dose_per_kg": 0.3, "dose_min": 0.24, "dose_max": 0.36, "dose_unit": "мг/кг", "method": "Инъекционн | доаудитных расхождений нет | conc=10.0 | global: мг/мл 0.2 (0.16000000000000003–0.24) |
| 2390 | Гамапрен | calc=null | ver=null | доаудитных расхождений нет | conc=5.0 | global: мг/мл 0 (0–0) |
| 2392 | Феловакс-4 | calc=null | ver=null | доаудитных расхождений нет | conc=1 мл | global: мг/мл 0 (0–0) |
| 2394 | Дермацин инъекционный | calc={"dose_per_kg": 0.3, "dose_min": 0.2, "dose_max": 0.3, "method": "подкожно", "frequency": "однократн | ver={"dose_per_kg": 0.3, "dose_min": 0.2, "dose_max": 0.3, "method": "подкожно", "frequency": "однократн | доаудитных расхождений нет | conc=10.0 | global: мг/мл 0.2 (0.16000000000000003–0.24) |
| 2395 | Отодектин | calc={"dose_per_kg": 0.3, "dose_min": 0.2, "dose_max": 0.3, "method": "подкожно", "frequency": "однократн | ver={"dose_per_kg": 0.3, "dose_min": 0.2, "dose_max": 0.3, "method": "подкожно", "frequency": "однократн | доаудитных расхождений нет | conc=1.0 | global: мг/мл 0.006 (0.0048000000000000004–0.0072) |
| 2396 | Вакцина против ящура эмульсионная моно- и поливалентная для профилактики ящура свиней (из вируса, выращенного в клетках ВНК-21) | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "frequency": "по схеме вакцин | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "dose_unit": "fixed", "method": "внутримышечн | course_days: calc='3 суток' ver='3', method: calc=None ver='внутримышечно', route: calc='внутримышечно' ver=None | conc=1 | global: доза/флакон 0 (0–0) |
| 2401 | Настойка чемерицы | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "frequency": "1 раз в сутки", | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "dose_unit": "fixed", "method": "по инструкци | method: calc=None ver='по инструкции', route: calc='по инструкции' ver=None | conc=None | global: мг/мл 0 (0–0) |
