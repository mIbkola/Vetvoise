# Аудит пар «Свиньи × препарат» — батч 62 (10 пар)

Данные из `drugs_calc.json`/`verified_dosages.json`; источники не подтверждены; расхождения calc/ver зафиксированы в сводке `SWINE_DIFF_SUMMARY.md`.

| id | Препарат | Было (Свиньи) | calc/ver | Расхождения | Концентрация |
|---:|---|---|---|---|---|
| 1566 | Нобилис® ND Clone 30 | calc=null | ver=null | доаудитных расхождений нет | conc=2.4 | global: мг/мл 0 (0–0) |
| 1569 | Ауризон® | calc={"dose_per_kg": 2, "dose_min": 1, "dose_max": 4, "method": "внутримышечно", "frequency": "1 раз в су | ver=null | dose_max: calc=4 ver=None, dose_min: calc=1 ver=None, dose_per_kg: calc=2 ver=None, dose_unit: calc='мг/кг' ver=None, frequency: calc='1 раз в сутки' ver=None, method: calc='внутримышечно' ver=None | conc=3.0 | global: мг/мл 0.3 (0.24–0.36) |
| 1574 | Парофор® 140 | calc={"dose_per_kg": 25, "dose_min": 20.0, "dose_max": 30.0, "dose_unit": "мг/кг", "method": "Перорально" | ver={"dose_per_kg": 25.0, "dose_min": 20.0, "dose_max": 30.0, "dose_unit": "мг/кг", "method": "Пероральн | доаудитных расхождений нет | conc=200.0 | global: мг/мл 25 (20.0–30.0) |
| 1575 | Триспазвит | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "method": "внутримышечно", "frequency": "по схеме", | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "method": "внутримышечно", "frequency": "по с | notes: calc='на животное по инструкции' ver='дозирование согласно инструкции' | conc=None | global: МЕ/мл 0.05 (0.03–0.1) |
| 1576 | Доксилокс® ОR | calc={"dose_per_kg": 5, "dose_min": 4.0, "dose_max": 6.0, "dose_unit": "мг/кг", "method": "Перорально", " | ver={"dose_per_kg": 5.0, "dose_min": 4.0, "dose_max": 6.0, "dose_unit": "мг/кг", "method": "Перорально", | доаудитных расхождений нет | conc=100.0 | global: мг/мл 10.0 (8.0–12.0) |
| 1577 | Кофеин-бензоат натрия 20% раствор для инъекций | calc=null | ver=null | доаудитных расхождений нет | conc=200.0 | global: мг/мл 10.0 (5–10) |
| 1578 | Новокаин 0,5%, 1%, 2% раствор для инъекций | calc=null | ver=null | доаудитных расхождений нет | conc=20.0 | global: мг/мл 5.0 (2.0–10.0) |
| 1581 | Сульф 120, Сульф 480 | calc={"dose_per_kg": 15, "dose_unit": "мг/кг", "method": "перорально", "frequency": "1 раз в день"} | ver={"dose_per_kg": 15.0, "dose_unit": "мг/кг", "method": "перорально", "frequency": "1 раз в день"} | доаудитных расхождений нет | conc=100.0 | global: мг/мл 15.0 (12.0–18.0) |
| 1584 | Глютанол-С | calc=null | ver=null | доаудитных расхождений нет | conc=20000.0 | global: мг/мл 0 (0–0) |
| 1585 | Амоксициллин 15% LA | calc={"dose_per_kg": 10, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "Инъекционно" | ver={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "Инъекционн | frequency: calc='однократно, при необходимости повторно через 48 часов' ver='1 раз в день' | conc=150.0 | global: мг/мл 10 (8.0–12.0) |
