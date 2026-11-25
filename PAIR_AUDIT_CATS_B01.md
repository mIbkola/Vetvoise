# Точечная проверка пар «Кошки × препарат» — батч 01 (10 пар)

Источник ищется **под каждую пару отдельно**. Статус «ПОДТВЕРЖДЕНО» означает,
что найдена инструкция с дозой для кошек и она совпадает с базой. «ПРОТИВОРЕЧИЕ
ВИДА» — инструкция не допускает кошек; дозу **не меняем**, потому что удаление
вида выходит за рамки проверки доз и требует отдельного решения.

| id | Препарат | Доза в базе | Что говорит инструкция | Статус | Источник |
|---:|---|---|---|---|---|
| 14 | Бонхакан | 1 мг/кг (conc 10 мг/мл) | Кошкам 0,1 мл/кг = 1 мг/кг гиалуроната натрия | ПОДТВЕРЖДЕНО | https://galen.vetrf.ru/files/348cec18-19b3-4d3c-8b37-f34d4c35b4c0 |
| 15 | Марбофлоксацин 10% | 2 мг/кг | Показания: КРС, свиньи; кошки не указаны | ПРОТИВОРЕЧИЕ ВИДА — не меняли | https://www.vidal.ru/veterinar/marbofloksatsin_10_-31753 ; https://askont.ru/catalog/marbofloxacin-10/instruction |
| 16 | Сурфагон Ультра | 0,01 мг/кг | Инструкция: коровы, свиньи, лошади; кошек нет | ПРОТИВОРЕЧИЕ ВИДА — не меняли | https://askont.ru/catalog/surfagon-ultra-10-mkg/instruction |
| 19 | Эмпазекс | 1 мг/кг, min 0,8, «каждые 3 дня», fixed «2 мг/кг … 1 раз в 3 дня» | Кошкам 0,5–1 мг/кг 1 раз в 24–48 ч; при патологиях почек/печени 48–72 ч | **ИСПРАВЛЕНО** | https://pets.nita-farm.ru/catalog/empazeks-3-ml/ ; https://zoopt.ru/upload/yadisk/2x1LACbwOF6Xig.pdf |
| 20 | Робексера® | 1 мг/кг | Раствор для инъекций: подкожно 1 мл на 10 кг = 2 мг/кг | **ИСПРАВЛЕНО** | https://storage.yandexcloud.net/4lapy-strapi/instr_Robeksera_1_858ab67287.pdf |
| 25 | Марбопрайм® | 2 мг/кг | Показания: КРС, свиньи; кошек нет | ПРОТИВОРЕЧИЕ ВИДА — не меняли | https://www.vidal.ru/veterinar/marbopraim-31752 ; https://vetsnab.info/vetpreparaty/marboprajm-rastvor-dlya-inekczij/ |
| 29 | Силта® | 1 мг/кг (conc 4 мг/мл) | Кошкам 1 мг телмисартана/кг = 0,25 мл/кг | ПОДТВЕРЖДЕНО | https://www.vidal.ru/veterinar/silta-31725 ; https://www.markvet.ru/upload/iblock/74b/9knurr5zs91jo9hiuh5w3i4hp6zvdaxt.pdf |
| 30 | Фениквантел® | 5 мг/кг | Инструкция описывает собак; кошки в найденной инструкции не указаны | ПРОТИВОРЕЧИЕ ВИДА — не меняли | https://pets.nita-farm.ru/catalog/fenikvantel-20-mg/ ; https://www.zoovetumka.ru/Фениквантел_таб.pdf |
| 31 | Сульф-комплекс АВЗ | 10 мг/кг | Раствор: свиньи и сельхозптица. Для кошек — отдельный препарат «Сульф 120» (1 табл/4 кг) | ПРОТИВОРЕЧИЕ ВИДА — не меняли | https://www.vidal.ru/veterinar/sulf-kompleks_avz-31726 ; https://zoo-galereya.ru/vetapteka/antibakterialnye-sredstva/avz-sulf-120-6-tabletok-dlya-koshek-pri-bakterialnykh-infektsiyakh.html |
| 32 | Зинтирил | 1 мг/кг | Кошкам 1 мг/кг 1 раз в сутки | ПОДТВЕРЖДЕНО | https://www.vetlek.ru/directions/?id=1493 ; https://pets.nita-farm.ru/catalog/zintiril-15-ml/ |

Итого: подтверждено 3, исправлено 2, противоречие вида (открытый вопрос) 5.
Правки applies `scripts/fix_pair_cats_b01.py`; лог — `PAIR_FIXES_CATS_B01.md`.
