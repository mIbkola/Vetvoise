# Аудит пар «Свиньи × препарат» — батч 42 (10 пар)

Данные из `drugs_calc.json`/`verified_dosages.json`; источники не подтверждены; расхождения calc/ver зафиксированы в сводке `SWINE_DIFF_SUMMARY.md`.

| id | Препарат | Было (Свиньи) | calc/ver | Расхождения | Концентрация |
|---:|---|---|---|---|---|
| 952 | Вакцина против болезни Ауески инактивированная эмульгированная маркированная | calc=null | ver=null | доаудитных расхождений нет | conc=2.0 | global: мг/мл 0 (0–0) |
| 955 | Детокс | calc={"dose_per_kg": 0.1, "dose_unit": "мл/кг", "dose_min": 0.1, "dose_max": 0.1, "method": "только внутр | ver={"dose_per_kg": 0.1, "dose_min": 0.1, "dose_max": 0.1, "dose_unit": "мл/кг", "method": "только внутр | доаудитных расхождений нет | conc=50.0 | global: мг/мл 0.1 (0.1–0.1) |
| 958 | Катобевит® | calc={"dose_per_kg": 10, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "Инъекционно" | ver={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "Инъекционн | доаудитных расхождений нет | conc=100.0 | global: мг/мл 10 (8.0–12.0) |
| 962 | Амоксипрем 200 | calc={"dose_per_kg": 10, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "внутрь (с ко | ver={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "внутрь (с  | доаудитных расхождений нет | conc=200.0 | global: мг/мл 10 (8.0–12.0) |
| 963 | Кетопроф | calc={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "frequency": "1 раз в | ver={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "frequency": "1 раз в | доаудитных расхождений нет | conc=100.0 | global: мг/мл 10.0 (8.0–12.0) |
| 966 | Новокаин 0,5%, 2% раствор для инъекций | calc=null | ver=null | доаудитных расхождений нет | conc=20.0 | global: мг/мл 5.0 (2.0–10.0) |
| 967 | Эстрофантин® | calc={"dose_per_kg": 0.005, "dose_min": 0.004, "dose_max": 0.006, "dose_unit": "мг/кг", "method": "Инъекц | ver={"dose_per_kg": 0.005, "dose_min": 0.004, "dose_max": 0.006, "dose_unit": "мг/кг", "method": "Инъекц | доаудитных расхождений нет | conc=0.25 | global: мг/мл 0.01 (0.008–0.012) |
| 968 | Тиаклор | calc={"dose_per_kg": 10, "dose_min": 3, "dose_max": 15, "method": "внутрь", "frequency": "1 раз в сутки", | ver={"dose_per_kg": 10.0, "dose_min": 3.0, "dose_max": 15.0, "method": "внутрь", "frequency": "1 раз в с | доаудитных расхождений нет | conc=50.0 | global: мг/мл 10 (3–15) |
| 974 | Веткокцин | calc={"dose_per_kg": 20, "dose_min": 16.0, "dose_max": 24.0, "dose_unit": "мг/кг", "method": "Перорально" | ver={"dose_per_kg": 20.0, "dose_min": 16.0, "dose_max": 24.0, "dose_unit": "мг/кг", "method": "Пероральн | доаудитных расхождений нет | conc=50.0 | global: мг/мл 15 (12.0–18.0) |
| 975 | Амоксициллин 15% ЛА | calc={"dose_per_kg": 10, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "Инъекционно" | ver={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "Инъекционн | доаудитных расхождений нет | conc=150.0 | global: мг/мл 10 (8.0–12.0) |
