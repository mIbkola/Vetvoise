# Аудит пар «Свиньи × препарат» — батч 92 (10 пар)

Данные из `drugs_calc.json`/`verified_dosages.json`; источники не подтверждены; расхождения calc/ver зафиксированы в сводке `SWINE_DIFF_SUMMARY.md`.

| id | Препарат | Было (Свиньи) | calc/ver | Расхождения | Концентрация |
|---:|---|---|---|---|---|
| 2308 | Экстракт прополиса спиртовый | calc=null | ver=null | доаудитных расхождений нет | conc=None | global: мг/мл 0 (0–0) |
| 2312 | Тенальбен | calc={"dose_per_kg": 10, "dose_min": 5, "dose_max": 10, "method": "перорально", "frequency": "однократно" | ver={"dose_per_kg": 10.0, "dose_min": 5.0, "dose_max": 10.0, "method": "перорально", "frequency": "однок | доаудитных расхождений нет | conc=10.0 | global: мг/мл 7.5 (5–10) |
| 2316 | Колистин 4800 WSP | calc={"dose_per_kg": 50000, "dose_min": 25000, "dose_max": 100000, "method": "перорально (с водой)", "fre | ver={"dose_per_kg": 50000.0, "dose_min": 25000.0, "dose_max": 100000.0, "method": "перорально (с водой)" | доаудитных расхождений нет | conc=None | global: МЕ/мл 50000 (40000.0–60000.0) |
| 2319 | Ганасупервит | calc={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "method": "внутрь (с кормом/в | ver={"dose_per_kg": 0, "dose_min": 0, "dose_max": 0, "dose_unit": "fixed", "method": "внутрь (с кормом/в | course_days: calc='5-10 дней' ver=None | conc=3.0 | global: мг/мл 0 (0–0) |
| 2322 | Пенстреп-400 | calc={"dose_per_kg": 8000, "dose_min": 6400.0, "dose_max": 9600.0, "dose_unit": "МЕ/кг", "method": "Инъек | ver={"dose_per_kg": 8000.0, "dose_min": 6400.0, "dose_max": 9600.0, "dose_unit": "МЕ/кг", "method": "Инъ | dose_me_max: calc=9600.0 ver=None, dose_me_min: calc=6400.0 ver=None, dose_me_per_kg: calc=8000 ver=None | conc=200.0 | global: мг/мл 8000 (6400.0–9600.0) |
| 2323 | Витафлеш для инъекций | calc={"dose_per_kg": 7.0, "dose_unit": "мг/кг", "frequency": "1 раз в сутки", "notes": "Из файла: Аквитин | ver={"dose_per_kg": 7.0, "dose_unit": "мг/кг", "frequency": "1 раз в сутки", "notes": "Из файла: Аквитин | доаудитных расхождений нет | conc=100.0 | global: мг/мл 7.0 (5.6–8.4) |
| 2325 | Мультивитамин инъекции | calc=null | ver=null | доаудитных расхождений нет | conc=3.0 | global: мг/мл 0 (0–0) |
| 2327 | Кепроцерил WSP | calc={"dose_per_kg": 50000, "dose_min": 40000.0, "dose_max": 60000.0, "dose_unit": "МЕ/кг", "method": "Пе | ver={"dose_per_kg": 50000.0, "dose_min": 40000.0, "dose_max": 60000.0, "dose_unit": "МЕ/кг", "method": " | доаудитных расхождений нет | conc=30.0 | global: мг/мл 7.5 (5.0–10.0) |
| 2328 | Лимоксин-200 LA | calc={"dose_per_kg": 10, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "Инъекционно" | ver={"dose_per_kg": 10.0, "dose_min": 8.0, "dose_max": 12.0, "dose_unit": "мг/кг", "method": "Инъекционн | доаудитных расхождений нет | conc=200.0 | global: мг/мл 10 (8.0–12.0) |
| 2329 | Ошейник антипаразитарный Мультикс | calc={"dose_per_kg": 0.3, "dose_min": 0.2, "dose_max": 0.3, "method": "наружно", "frequency": "однократно | ver={"dose_per_kg": 0.3, "dose_min": 0.2, "dose_max": 0.3, "method": "подкожно", "frequency": "однократн | method: calc='наружно' ver='подкожно' | conc=None | global: мг/мл 0.2 (0.1–0.3) |
