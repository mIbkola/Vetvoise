# Аудит пар «КРС × препарат» — батч 49 (10 пар)

Данные из `drugs_calc.json`/`verified_dosages.json`; источники по доступным страницам — не подтверждены; правки по подтверждённым дозам в батчах по собакам/кошкам (по аналогии).

| id | Препарат | Было (КРС) | calc/ver | Доаудитные расхождения | Концентрация |
|---:|---|---|---|---|---|
| 1172 | Декокс 6% | calc={"dose_per_kg": 1.0, "dose_min": 1.0, "dose_max": 1.0, "dose_unit": "мг/кг", "method": "Перорально", | ver={"dose_per_kg": 1.0, "dose_min": 1.0, "dose_max": 1.0, "dose_unit": "мг/кг", "method": "Перорально", | доаудитных расхождений нет | conc=60.0 | global: мг/г 2 (1.6–2.4) |
| 1179 | ЛТФ-130 | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "frequency": "по схеме вакцин | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "dose_unit": "fixed", "method": "по инструкци | method: calc=None ver='по инструкции', route: calc='по инструкции' ver=None | conc=2.0 | global: мг/мл 0 (0–0) |
| 1200 | Девастин | calc={"method": "Наружно", "notes": "Водный раствор"} | ver={"method": "Наружно", "notes": "Водный раствор"} | доаудитных расхождений нет | conc=15.0 | global: мг/мл 0 (0–0) |
| 1202 | АЗИФЛУМИН® | calc={"dose_per_kg": 5, "dose_min": 4.0, "dose_max": 6.0, "dose_unit": "мг/кг", "method": "Инъекционно",  | ver={"dose_per_kg": 5.0, "dose_min": 4.0, "dose_max": 6.0, "dose_unit": "мг/кг", "method": "Инъекционно" | доаудитных расхождений нет | conc=100.0 | global: мг/мл 1.65 (1.1–2.2) |
| 1211 | Витаминно-аминокислотный комплекс "ВИТАМ" | calc=null | ver=null | доаудитных расхождений нет | conc=1000.0 | global: мг/мл 0 (0–0) |
| 1216 | Тимпанол | calc=null | ver=null | доаудитных расхождений нет | conc=None | global: мг/мл 0 (0–0) |
| 1221 | ЛТФ-201 Арм | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "frequency": "по схеме вакцин | ver={"dose_per_kg": 0.0, "dose_min": 0.0, "dose_max": 0.0, "dose_unit": "fixed", "method": "внутримышечн | method: calc=None ver='внутримышечно или подкожно', route: calc='внутримышечно или подкожно' ver=None | conc=2.0 | global: мг/мл 0 (0–0) |
| 1233 | "АВИВАК-Марек" | calc=null | ver=null | доаудитных расхождений нет | conc=2.0 | global: мг/мл 0 (0–0) |
| 1237 | Альвет® | calc={"dose_per_kg": 7.5, "dose_min": 5, "dose_max": 10, "method": "перорально", "frequency": "однократно | ver={"dose_per_kg": 7.5, "dose_min": 5.0, "dose_max": 10.0, "method": "перорально", "frequency": "однокр | доаудитных расхождений нет | conc=200.0 | global: мг/мл 7.5 (5–10) |
| 1239 | Метровит | calc={"dose_per_kg": 10, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "внутрь", "fr | ver={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "внутримато | method: calc='внутрь' ver='внутриматочно' | conc=5000.0 | global: мг/мл 10 (8.0–12.0) |
