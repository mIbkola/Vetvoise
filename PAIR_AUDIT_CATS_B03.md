# Точечная проверка пар «Кошки × препарат» — батч 03 (5 пар)

| id | Препарат | Доза в базе | Что говорит инструкция | Статус | Источник |
|---:|---|---|---|---|---|
| 63 | ОФТАЛЬМИКА® мазь глазная | 5 мг/кг «перорально», 1 раз в день | Закладывать полоску 0,3 см в конъюнктивальный мешок, 2–3 раза в день, 10 дней | **ИСПРАВЛЕНО** — численный расчёт выключен, текст в `fixed_dose` | https://avzvet.ru/product/oftalmika-maz/ ; https://galen.vetrf.ru/files/6f226fc5-4256-4436-961e-86690e37fab9 |
| 64 | Флексонорм®Кэт | 1 мг/кг, однократно | 6 мг/таб: 1 таб на кошку 2,5–6 кг, 2 таб 6–12 кг (1–2,4 мг/кг); не дробить | **ИСПРАВЛЕНО** | https://vet.promomed.ru/products/flexonormcat/ ; https://vet.promomed.ru/local/templates/amklav/assets/documents/instruction_flexonorm_cat.pdf |
| 76 | Бутал® | 5 мг/кг, «1-3 раза»; фикс 2,0 мл | 0,5–2,5 мл на животное, 1 раз в сутки, 4–5 дней, в/м, п/к или в/в медленно | **ИСПРАВЛЕНО** — текстовый фикс с диапазоном и курсом | https://vetsnab.info/vetpreparaty/butal/ ; https://alpovet.com/files/pdf/71.pdf |
| 83 | Конафлион | 1 мг/кг (min 0,8), 1 раз в день | 0,1–0,5 мл/кг = 1–5 мг/кг; каждые 12 ч, 2–3 дня | **ИСПРАВЛЕНО** — исправлены min/max и частота; доза 1 мг/кг (= нижняя граница) сохранена | https://pets.nita-farm.ru/catalog/konaflion/ ; https://www.vetlek.ru/directions/?id=1476 |
| 84 | Петмелокс VETЗАБОТА® | 0,05 мг/кг | 0,2 мг/кг в 1-й день, затем 0,1 мг/кг; кошкам ≤ 5 дней | **ИСПРАВЛЕНО** | https://vetsnab.info/vetpreparaty/petmeloks-vetzabota/ ; https://galen.vetrf.ru/files/12ac4f99-e2ee-4b32-a3b4-87aaf3996d73 |

Правки применяет `scripts/fix_pair_cats_b03.py`; лог — `PAIR_FIXES_CATS_B03.md`.
