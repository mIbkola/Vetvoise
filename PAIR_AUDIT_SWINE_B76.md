# Аудит пар «Свиньи × препарат» — батч 76 (10 пар)

Данные из `drugs_calc.json`/`verified_dosages.json`; источники не подтверждены; расхождения calc/ver зафиксированы в сводке `SWINE_DIFF_SUMMARY.md`.

| id | Препарат | Было (Свиньи) | calc/ver | Расхождения | Концентрация |
|---:|---|---|---|---|---|
| 1938 | Левамизол 75 | calc={"dose_per_kg": 7.5, "dose_unit": "мг/кг", "method": "перорально", "frequency": "1 раз"} | ver={"dose_per_kg": 7.5, "dose_unit": "мг/кг", "method": "перорально", "frequency": "1 раз"} | доаудитных расхождений нет | conc=75.0 | global: мг/мл 10.625 (8.5–12.75) |
| 1939 | Вакцина поливалентная "ВГНКИ" против лептоспироза животных | calc=null | ver=null | доаудитных расхождений нет | conc=100.0 | global: мг/мл 0 (0–0) |
| 1940 | Туберкулин очищенный (ППД) для млекопитающих | calc=null | ver=null | доаудитных расхождений нет | conc=5.0 | global: мг/мл 0 (0–0) |
| 1945 | Порцилис Ery | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "frequency": "по схеме вакцин | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "dose_unit": "fixed", "method": "внутримышечн | method: calc=None ver='внутримышечно', route: calc='внутримышечно' ver=None | conc=50.0 | global: мг/мл 0 (0–0) |
| 1946 | Бензилпенициллина натриевая соль для инъекций | calc={"dose_per_kg": 10000, "dose_unit": "МЕ/кг", "method": "инъекционно", "frequency": "2 раза в день",  | ver={"dose_per_kg": 10000.0, "dose_unit": "МЕ/кг", "method": "инъекционно", "frequency": "2 раза в день" | dose_me_max: calc=10000 ver=None, dose_me_min: calc=10000 ver=None, dose_me_per_kg: calc=10000 ver=None | conc=1.0 | global: мг/мл 16000.0 (12800.0–19200.0) |
| 1948 | Экофлис | calc={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "frequency": "1 раз в | ver={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "frequency": "1 раз в | доаудитных расхождений нет | conc=100.0 | global: мг/мл 10.0 (8.0–12.0) |
| 1950 | Доксипрекс | calc={"dose_per_kg": 5, "dose_min": 4.0, "dose_max": 6.0, "dose_unit": "мг/кг", "method": "Перорально", " | ver={"dose_per_kg": 5.0, "dose_min": 4.0, "dose_max": 6.0, "dose_unit": "мг/кг", "method": "Перорально", | доаудитных расхождений нет | conc=100.0 | global: мг/мл 10.0 (8.0–12.0) |
| 1951 | Полиплевросин APX IM | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "frequency": "по схеме вакцин | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "dose_unit": "fixed", "method": "внутримышечн | method: calc=None ver='внутримышечно или подкожно', route: calc='внутримышечно или подкожно' ver=None | conc=100.0 | global: мг/мл 0 (0–0) |
| 1953 | Адилин-супер | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "frequency": "1 раз в сутки", | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "dose_unit": "fixed", "method": "внутримышечн | method: calc=None ver='внутримышечно (после растворения)', route: calc='внутримышечно (после растворения)' ver=None | conc=100.0 | global: мг/мл 0 (0–0) |
| 1959 | Гликопин® | calc=null | ver=null | доаудитных расхождений нет | conc=1.0 | global: мг/мл 0 (0–0) |
