# Полный сквозной аудит: «Кошки»

Препаратов с видом «Кошки»: **797** из 2401. 
Статус «ТРЕБУЕТ ИСТОЧНИКА» означает: официальная инструкция под конкретную запись в наших аудитах **не подтверждена**. Это не AUTO и не «норма» — запись подлежит проверке.

Статусы: ОТКРЫТЫЙ ВОПРОС — 8, ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО — 17, ТРЕБУЕТ ИСТОЧНИКА — 772

## Флаги

| Код | ЧтоMeans | Количество |
|---|---|---|
| CALC_OFF_DOSE | калькулятор выключен, но числовая доза есть (нужен явный источник) | 107 |
| DB_ANIMALS_MISMATCH | список видов не совпадает между calc и verified | 350 |
| DB_CONC_MISMATCH | концентрация/единица не совпадают между calc и verified | 54 |
| DB_DOSE_MISMATCH | видовая доза не совпадает между calc и verified | 7 |
| DB_FREQ_MISMATCH | частота не совпадает между calc и verified | 29 |
| DUPLICATE_NAME | несколько записей с одним названием | 23 |
| EXTERNAL_NUMERIC | наружный путь при включённом численном расчёте | 97 |
| GHOST_SPECIES | вид есть в animals, но нет в animal_specific (или наоборот) | 94 |
| INDICATION_NO_SPECIES | в показаниях реестра названы другие виды, а этот нет | 17 |
| INVALID_RANGE | dose_min > dose_max или доза вне диапазона | 2 |
| ME_NO_ACTIVITY | доза в МЕ/кг, но активность МЕ/мл не задана | 10 |
| ML_PER_KG_ON | доза в мл/кг при включённом калькуляторе (движок берёт глобальную единицу) | 16 |
| NO_OFFICIAL_SOURCE | в наших аудитах нет подтверждающей официальной инструкции | 772 |
| REG_ANIMALS_EMPTY | в реестре поле animals пустое (нет данных, не противоречие) | 505 |
| REG_ANIMALS_INCOMPLETE | вида нет в animals реестра, но он назван в показаниях (метаданные) | 99 |
| REG_CONTRADICTION | реестр явно сужает вид: нет в animals и нет в показаниях | 10 |
| REG_SPECIES_MISSING | в реестре явно указаны другие виды, а этот отсутствует | 277 |
| ZERO_CONC_WITH_DOSE | есть масса-доза, но концентрации нет | 11 |

## Подозрительные по виду (реестр/показания ужесточают): 10

| id | Препарат | Статус | Флаги | Показания реестра |
|---|---|---|---|---|
| 15 | Марбофлоксацин 10% | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION | Назначают КРС при заболеваниях органов дыхания и маститах, вызванных чувствительными к марбофлоксацину штаммами микроорганизмов, свиньям при респираторных заболеваниях бактериальной этиологии и синдроме ММА |
| 102 | Бофлокс | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE | Для лечения КРС при патологии органов дыхания, пищеварительной системы, маститах |
| 207 | Зуратрол® | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE | назначают поросятам и молодняку КРС с лечебной и лечебно-профилактической целью при кокцидозе |
| 439 | Марботим | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE | назначают с лечебной целью КРС и свиньям при респираторных заболеваниях бактериальной этиологии, маститах и синброме ММА, возбудители которых чувствительны к марбофлоксацину |
| 457 | Энростин® Макс | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE | назначают КРС и свиньям для лечения колибактериоза, сальмонеллеза, атрофического ринита, стрептококкоза, септицемии, синдрома ММА, мастита, микоплазмоза и других инфекций, возбудители которых чувствительны к энрофлоксацину |
| 530 | Трисульф ВС | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION | применяют молодняку КРС при колисептицемии, сальмонеллезе, пастереллезе, бронхопневмонии, абсцессах, вызванных стафилококками, полиартритах, вызванных стрептококками; свиньям при колибактериозе, атрофическом рините, сальмонеллезе, пастерелл |
| 558 | Миксоферон® | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE | применяют с профилактической и лечебной целью при желудочно-кишечных и острых респираторных заболеваниях вирусной и смешанной этиологии у крупного рогатого скота, свиней, лошадей, овец и их молодняка (парагрипп-3, инфекционный ринотрахеит,  |
| 757 | Марбоцин | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE | для лечения КРС при заболеваниях органов дыхания и маститах, свиней при респираторных заболеваниях и ММА синдроме вызванных микроорганизмами, чувствительными к марбофлоксацину |
| 854 | Цефтиосан® Форте | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE | назначают КРС при бактериальных инфекциях, вызванных возбудителями, чувствительными к цефтиофуру |
| 864 | Туламицин-АВЗ | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE | для лечения бактериальных инфекций органов дыхания у КРС и свиней, вызванных микроорганизмами, чувствительными к тулатромицину |

## Все препараты вида

| id | Препарат | Доза | Ед. | Конц. | Кальк. | Фикс | Статус | Флаги |
|---|---|---|---|---|---|---|---|---|
| 1 | Мариния® | 1 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 5 | Ноземацид® | 10 | мг/кг | 600 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 7 | БАРС® капли инсектоакарицидные | 15 | мг/кг | 150 | да | капли: наносить по инструкции, 1 раз в сутки | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC |
| 8 | Биофертагил | 0.01 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 9 | Фунгин® таблетки | 5 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 14 | Бонхакан | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 15 | Марбофлоксацин 10% | 2 | мг/кг | 100 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION |
| 16 | Сурфагон Ультра | 0.01 | мг/кг | 0.05 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 19 | Эмпазекс | 1 | мг/кг | 3 | да | 2 мг/кг (3.0 мг/табл) ≈ 2.7 табл на 4кг. 1 раз в 3 дня | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 20 | Робексера® | 1 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 25 | Марбопрайм® | 2 | мг/кг | 100 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY |
| 29 | Силта® | 1 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 30 | Фениквантел® | 5 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 31 | Сульф-комплекс АВЗ | 10 | мг/кг | 178 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 32 | Зинтирил | 1 | мг/кг | 2 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 34 | Дехиспот® | 5 | мг/кг | 85.8 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 40 | АКВАСУЛЬФ® | 5 | мг/кг | 400 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 43 | Полимиксин 6 млн. МЕ и 12 млн. МЕ | 50000 | МЕ/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ME_NO_ACTIVITY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 55 | Вемелкам® 2% | 0.2 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 61 | Нефопам-ВЕТ | 0.5 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 63 | ОФТАЛЬМИКА® мазь глазная | 5 | мг/кг | 15 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 64 | Флексонорм®Кэт | 1 | мг/кг | 6 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 76 | Бутал® | 5 | мг/кг | 100 | да | 2.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 83 | Конафлион | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 84 | Петмелокс VETЗАБОТА® | 0.05 | мг/кг | 0.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 86 | Робенекс® | 1 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 93 | Менбутил | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 95 | Фенпраз Форте суспензия | 2.88 | мг/кг | 28.8 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 96 | OKVET® Шампунь лечебный с хлоргексидином | 0.1 | мг/кг | 50 | да | шампунь: наносить по инструкции, 2-3 раза в день, курс 3-5 дней | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 97 | Фенпраз Форте таблетки | 2.88 | мг/кг | 28.8 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 98 | Уристоп | 2 | мг/кг | 40.28 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 102 | Бофлокс | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE |
| 103 | Марботим таблетки | 2 | мг/кг | 5 | да | 2 мг/кг (5.0 мг/табл) ≈ 1.6 табл на 4кг. 1 раз в день | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 107 | Мелоксикам Апиценна раствор для инъекций | 0.05 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 112 | Оноксеб® | 1 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 113 | Инсектал® комбо таблетки | 0.006 | мг/кг | 0.4 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 122 | ВИНСУВЕТ Гларгин | 0.3 | МЕ/кг | 50 МЕ/мл | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 123 | Энроксил® 10% раствор для инъекций | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 124 | Бравуланер | 40 | мг/кг | 112.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 125 | БлохНэт® next капли | 10 | мг/кг | 100 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 127 | ФЛУВЕТОН | 28 | мг/кг | 280 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 130 | Тиломакс | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 131 | Дезацид Форте | 10 | мг/кг | 5 | да | 1 капля в глаз | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 132 | АМОКСИСТИМ V-15% | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 138 | БАРС® капли ушные | 0.05 | мг/кг | 0.3 | да | 2-3 капли в ухо | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 140 | Энросепт раствор для инъекций 5% и 10% | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 145 | ЛОПЕРАВЕТ | — | мг/кг | 0.13 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 155 | Полицефур | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 156 | Синклавир порошок | 12.5 | мг/кг | 575 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 160 | Ветспокоин Трио таблетки | 5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 161 | Дирофен® Макс | 6 | мг/кг | 60 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 167 | Ветспокоин Трио суспензия | 5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 168 | Супрамил би макс таблетки | 0.5 | мг/кг | 5 | нет | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 169 | Тразапентин® таблетки | 5 | мг/кг | 36 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 171 | Мираклав® порошок для приготовления раствора для внутривенного введения | 12.5 | мг/кг | 250 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 172 | Отидез Форте | 2 | мг/кг | 5 | да | по инструкции: 1-3 капли в каждое ухо 2 раза в сутки | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC |
| 175 | ЛоксикVet суспензия | 0.1 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, INVALID_RANGE, NO_OFFICIAL_SOURCE |
| 176 | ЛоксикVet таблетки | 0.1 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, INVALID_RANGE, NO_OFFICIAL_SOURCE |
| 179 | Ветгаба таблетки | 5 | мг/кг | 60 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 181 | Нейрокард | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 186 | Бимаксгард® КОМПЛЕКС для собак | 0.003 | мг/кг | 25 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 187 | Флорикол® 30% | 15 | мг/кг | 300 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 190 | НаноТим | 5 | мг/кг | 450 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 193 | УльтраСелл-Кэт® | — | мг/кг | 0.4 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 194 | Фипритика | 7.5 | мг/кг | 10 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 200 | Бимаксгард® КОМПЛЕКС для кошек | 1 | мг/кг | 10 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 201 | Димоксан WS | 12.5 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 204 | Мазь левомицетиновая | 50 | мг/кг | 4000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 207 | Зуратрол® | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE |
| 209 | Доксатиб® | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, INDICATION_NO_SPECIES, NO_OFFICIAL_SOURCE |
| 210 | САЛЬМОГИР® | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 211 | СЕКС БАРЬЕР® капли | 2 | мг/кг | 1 | да | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 229 | Разбавитель для вакцин против дерматофитозов животных | — | мг/кг | 2 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 230 | Слипофол | 4 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 232 | Тилозин ТАБ | 10 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 234 | Ипекон® | 375 | fixed | 80 | нет | По схеме вакцинации | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 238 | ЗоозащитаVet | 20 | мг/кг | 200 | да | по инструкции препарата: схема применения указана в инструкции, 1 раз в сутки | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 241 | БАРС® форте спрей инсектоакарицидный | 6.7 | мг/кг | 3.1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 249 | АЙСИДИВИТ® | 10 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 252 | Лонтривет | 2 | мг/кг | 2 | да | 1 мг/кг (2.0 мг/табл) ≈ 2 табл на 4кг. 1-2 раза в день | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 253 | Нефрокэт/дог | 3.5 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 254 | Интерспектин WS | 15 | мг/кг | 444 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 255 | Синклавир таблетки | 12.5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 258 | ЦИПРОВЕТ® капли глазные | 5 | мг/кг | 4.5 | да |  | ОТКРЫТЫЙ ВОПРОС | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY |
| 262 | Сангвения | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 264 | Фуросенит-вет | 1 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 266 | Ветгаба | 5 | мг/кг | 60 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 268 | ОФТАЛЬМИКА® капли глазные | 0.5 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 273 | Гонавет Вейкс® | 0.01 | мг/кг | 0.0524 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 274 | Окситрит | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 275 | Толфемакс 4%, 8% | 2 | мг/кг | 80 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 284 | Мильмакс-Нита для кошек | 5 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 285 | Мильмакс-Нита для собак | 5 | мг/кг | 2.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 286 | Отосур® | 2.3 | мг/кг | 23 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 289 | Неотерика Протекто 12 | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 292 | Айнил | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 296 | ПимХарт | 0.25 | мг/кг | 1.25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 298 | Энралонг® 100 LA | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 300 | Алмексил® 20 | 0.2 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 302 | Цефалекс-50 | 15 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 304 | Ветодиметин® спрей | 0.1 | мг/кг | 1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 305 | Диазепам-ЭНДОФАРМ | 0.5 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 306 | Мильбецин Нео спот-он | 2 | мг/кг | 25 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 308 | Метоклопрамид-ЭНДОФАРМ | 0.2 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 309 | Кинорон® | 1 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 310 | Кетамин-ЭНДОФАРМ | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 313 | Трамвет® | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 314 | Гепарин натрия-ЭНДОФАРМ | 0.1 | мг/кг | 5000 МЕ/мл | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 319 | Фипронника | 5 | мг/кг | 7.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 320 | Доксипул | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 322 | АМОКСИСТИМ порошок | 12.5 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 323 | Окситоцин | — | fixed | 10 МЕ/мл | нет | 3-5 МЕ (0,3-0,5 мл) на животное в/м | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 324 | РанодезВЕТ спрей | — | мг/кг | 40 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 325 | Гапентин | 5 | мг/кг | 80 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 333 | Селамигор® | 6 | мг/кг | 60 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 335 | VETOKO капли глазные для собак и кошек VETЗАБОТА® | 5 | мг/кг | 4.5 | да | 1 капля в глаз | ОТКРЫТЫЙ ВОПРОС | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY |
| 336 | Кеситая® | 0.08 | мг/кг | 1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 339 | Окситетрациклина гидрохлорид 1000 | 10 | мг/кг | 950 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 342 | Карнифел PCHR | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 344 | Интракокс Памп | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 345 | Фуросенит-вет® ТАБ | 1 | мг/кг | 8 | да | 2 мг/кг (8.0 мг/табл) ≈ 1 табл на 4кг. 2 раза в день | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 347 | Соладокси | 10 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 351 | МаксиДропс® | 10 | мг/кг | 100 | да | по инструкции препарата: схема применения указана в инструкции, 1 раз в сутки, к | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 353 | Но-презан® ТАБ | 10 | мг/кг | 4 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 357 | Толтрекс 5% | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 359 | Энроксил® таблетки  со вкусом мяса | 5 | мг/кг | 15 | да | 5 мг/кг (15.0 мг/табл) ≈ 1.3 табл на 4кг. 1 раз в день | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 363 | Оксибактонид | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 365 | Гиалувит Хондро | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 366 | Принокат® | 0.003 | мг/кг | 25 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 370 | Но-презан | 2 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 371 | Принокат® кошки | 1 | мг/кг | 10 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 376 | ДаДокси С+ | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 377 | Холликалм® раствор для инъекций | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 383 | Серинебс | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 388 | Интракокс Орал | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 389 | Вимелексин 50 % | 15 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 390 | Фунгивет Rus крем | 30 | fixed | 10 | да | По инструкции (наружное применение) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 391 | Фунгивет Rus спрей | 30 | fixed | 10 | да | По инструкции (наружное применение) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 393 | Тиломаг® | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 394 | Неомиксин | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 395 | Везотил® | 10 | мг/кг | 250 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 408 | Лидоканит Вет | 2 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 410 | Флорфеникол гранулы | 15 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 411 | Декеситая® | 0.04 | мг/кг | 0.1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 419 | Хетгард | 0.5 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 420 | АЛЬБЕН® С | 5 | мг/кг | 250 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 421 | Фунгивет Rus таблетки | 5 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 423 | Аквеллиум | 0.5 | мг/кг | 4.84 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 425 | Пинпрамиль® для кошек | 5 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 427 | Синклавир для инъекций | 12.5 | мг/кг | 161 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 434 | Коликвинол® С | 15 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 436 | Бимаксгард ТАБС для кошек | 5 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 437 | Бимаксгард ТАБС для собак | 5 | мг/кг | 2.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 438 | Флоксаген S | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, INDICATION_NO_SPECIES, NO_OFFICIAL_SOURCE |
| 439 | Марботим | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE |
| 441 | Зоокард Rus суспензия | 0.06 | мг/кг | 0.625 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 443 | Зоокард Rus таблетки | 0.06 | мг/кг | 1.25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 448 | Мелоксигард | 0.05 | мг/кг | 0.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 454 | Азинокс для собак и кошек | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 457 | Энростин® Макс | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE |
| 458 | Докси WS | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, INDICATION_NO_SPECIES, NO_OFFICIAL_SOURCE |
| 460 | Азинокс плюс | 5 | мг/кг | 50 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 462 | Доксин-200 WS | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 464 | Кетотрит 2,5%, 10% | 1 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 468 | ОКСИТРОН® 200 | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 470 | Преднифарм | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 472 | Преднифарм® ТАБ | 2 | мг/кг | 4 | да | 1 мг/кг (4.0 мг/табл) ≈ 1 табл на 4кг. 1-2 раза в день | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 473 | Азитронит® ТАБ | 5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 474 | ФЛУВЕКТО® жевательные таблетки | 25 | мг/кг | 112.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 475 | Энрофаст | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 477 | Окситетрациклин 200 | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 481 | Солютистин® | 10 | мг/кг | 450 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 482 | Толтрекс 2,5% | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 483 | Гельминтал Мини Табс | 7.5 | fixed | 9 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 488 | Цимифур® | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 496 | Вемелкам | 0.05 | мг/кг | 2 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 499 | Вемелкам® ТАБ | 0.05 | мг/кг | 0.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 502 | Фалена | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 504 | ИН-АП спрей | 7.5 | мг/кг | 2.2 | да | спрей: наносить по инструкции, 1 раз в месяц, курс однократно | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 505 | Мильбемакс® для собак | 5 | мг/кг | 2.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 506 | Натрия хлорид АРМ | 0.1 | мл/кг | 9 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 509 | Эктогардика | 10 | мг/кг | 12 | да | 10 мг/кг (12.0 мг/табл) ≈ 3.3 табл на 4кг. ежемесячно | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 512 | Раствор Рингера-Локка | 0.15 | мл/кг | 9 | да |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, ML_PER_KG_ON, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 514 | Мильбемакс® для кошек | 5 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 515 | ФОРСЕКТО® | — | мг/кг | 66.7 | нет | по инструкции препарата: схема применения указана в инструкции | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 520 | Адвокат® | 0.003 | мг/кг | 25 | да |  | ОТКРЫТЫЙ ВОПРОС | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 521 | ЭкспрессТабс® | 0.05 | мг/кг | 150 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 524 | Пинпрамиль® для собак | 5 | мг/кг | 2.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 525 | Телмигард | 1 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 527 | Доксигор 50% | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 529 | Тилодокс-200 | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 530 | Трисульф ВС | 15 | мг/кг | 400 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION |
| 539 | Неотерика Протекто ошейник | 10 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 540 | Натрия хлорид изотонический 0,9% раствор для инъекций | 0.1 | мл/кг | 9 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 542 | Амоксимаг® | 12.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 548 | Кофеин-бензоат натрия 20% раствор для инъекций | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 554 | Энромаг® | 5 | мг/кг | 50 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 557 | Уротропин® | 10 | мг/кг | 400 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 558 | Миксоферон® | 1 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 561 | Фелидерм | — | мг/кг | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 562 | Цианокобаламин | 0.05 | мг/кг | 0.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 564 | Триховет® | 15 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 565 | Цефтимаг® | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 569 | Миксоферон® раствор для инъекций | — | МЕ/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, ME_NO_ACTIVITY, NO_OFFICIAL_SOURCE |
| 570 | Колингор 12М | 50000 | МЕ/кг | 510 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, ME_NO_ACTIVITY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 572 | Эндометрамаг-Грин® | 0.75 | мг/кг | 15 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 584 | Витамин D3 масляный раствор | — | МЕ/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, ME_NO_ACTIVITY, NO_OFFICIAL_SOURCE |
| 589 | Ципрофлоксацин 10% | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, INDICATION_NO_SPECIES, NO_OFFICIAL_SOURCE |
| 590 | Линкомицин 10 % раствор | 15 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 591 | Гентамицина сульфат 4 % раствор | 3 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 594 | Супримицин® | 3 | мг/кг | 40 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 596 | ЛЕОМИНОР | — | мг/кг | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 597 | Кальция борглюконат | 0.75 | мл/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, ML_PER_KG_ON, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 598 | Бактимаг®-О | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 601 | Окситетрамаг 20® | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 606 | Доксимаг®-О | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 607 | Кальция хлорид 10% раствор для инъекций | 0.15 | мл/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 609 | Энрофлок-Э | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 610 | Метронид-Э | 15 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 611 | Левофлок-Э-10 | 7.5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 615 | Тилодокс Р | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 619 | МИРТАЦЕН® | 1 | мг/кг | 1.88 | да | 2 мг/кг (1.88 мг/табл) ≈ 4.3 табл на 4кг. 1 раз в 3 дня | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 620 | Адвокат® кошки | 0.25 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 621 | Форесто® | 10 | мг/кг | 1250 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 625 | Курс Успокоин таблетки | 2 | мг/кг | 28 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 626 | Адвантейдж® | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 628 | Дронтал® плюс | 5 | мг/кг | 504 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 629 | Байкокс® 5% | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 630 | БАРС® классик капли против блох и клещей | 6.7 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 633 | Профендер® | 5 | мг/кг | 85.75 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 635 | Байкокс® 2,5% | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 637 | Дронтал® | 5 | мг/кг | 230 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 638 | Катозал® | 10 | мг/кг | 100 | нет | 0.5-2.5 мл в/м, п/к или в/в 1 р/сут 4-5 дней | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 642 | Сыворотка "Витафел-С" | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 645 | Глобулин "Витафел" | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 646 | ТИАСТИМ 10% К | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 653 | Линко-Фуд 15% | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 657 | КОЛИФЛОКС® оральный | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 659 | Чеми спрей | — | мг/кг | 2000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 660 | Тилво ВЛ 625 | 15 | мг/кг | 625 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 663 | Амино-Solvo | 0.1 | мл/кг | 72 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 669 | Спрей Фолайн® | 0.01 | мг/кг | 0.1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 672 | АМОКСИСТИМ К | 12.5 | мг/кг | 250 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 677 | Марбовитрил 100 | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 680 | Тетравет® L.A. | 10 | мг/кг | 200 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 681 | Ветримоксин L.A. | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 682 | Supramil® эмульсия | 5 | мг/кг | 2.5 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 683 | Инсектал шампунь | 7.5 | мг/кг | 1.04 | да | шампунь: наносить по инструкции, 1 раз в месяц, курс однократно | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 686 | ЭнтероЗоо® | — | мг/кг | 60000 | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 687 | Мелоксидил® | 0.2 | мг/кг | 1.5 | да |  | ОТКРЫТЫЙ ВОПРОС | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING |
| 694 | Ветопрофен | 1 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 695 | Празицид®-комплекс НЕО | 5 | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 698 | Мелоксиприм | 0.2 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 702 | Аквидокс 750 | 10 | мг/кг | 750 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 704 | Эйметерм раствор 2,5% | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 714 | Эпримек® | 0.5 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 715 | Докситрон жевательные таблетки | 10 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 724 | Окситетрациклина гидрохлорид для инъекций | 10 | мг/кг | 860 | нет |  | ОТКРЫТЫЙ ВОПРОС | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, DUPLICATE_NAME |
| 735 | ГЛОБФЕЛ | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 739 | МУЛЬТИФЕЛ | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 752 | Тилвагор WS | 15 | мг/кг | 625 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 754 | ДОКСИСТИМ К | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 755 | КОЛИСТИМ К | 50000 | МЕ/кг | 50 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, ME_NO_ACTIVITY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 757 | Марбоцин | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE |
| 770 | Экспресс Успокоин® таблетки | 2 | мг/кг | 24 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 774 | Мильпро® кэт | 5 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 775 | Мильпро® дог | 5 | мг/кг | 2.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 784 | Амоксиянтарь гранулы | 12.5 | мг/кг | 115 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 789 | Докситарт 500 | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 794 | Празицид®-суспензия НЕО | 5 | мг/кг | 15 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 801 | Кетовет 100 | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 803 | Локсик 2% | 0.2 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 807 | Виметрил 100 | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 808 | Стоп-кокцид® 2,5% | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 817 | Амоксиянтарь 150 | 12.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 821 | Амоксиянтарь | 12.5 | мг/кг | 574 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | REG_SPECIES_MISSING |
| 823 | Шиерия® | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 826 | Инсектал комбо С | 0.003 | мг/кг | 107.5 | да |  | ОТКРЫТЫЙ ВОПРОС | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 829 | Аподерм | 15 | fixed | 21.5 | да | По инструкции (наружное применение) | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 830 | Шампунь VETЗАБОТА® с хлоргексидином 5% | 0.1 | мг/кг | 50 | да | шампунь: наносить по инструкции, 2-3 раза в день, курс 3-5 дней | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 832 | НЕФРОСПАС® | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 833 | Неотерика Протекто таблетки | 0.1 | мг/кг | 7.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 836 | ВЕТКОЛ ВС 6 и ВЕТКОЛ ВС 12 | 50000 | МЕ/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, ME_NO_ACTIVITY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 840 | Польодоксин | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 843 | Антравак - СТИ жидкая | — | мг/кг | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 845 | Канинсулин | 0.3 | МЕ/кг | 40 МЕ/мл | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 854 | Цефтиосан® Форте | 2 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE |
| 856 | Энрофлоксацин 50 раствор для инъекций | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 858 | Окситетрациклин 200 LA | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 862 | Линкопрем 150 | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 864 | Туламицин-АВЗ | 2 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE |
| 872 | Гельмимакс®-2 | 2 | мг/кг | 10 | нет | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 877 | Форцерис | 10 | мг/кг | 133.4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 880 | ДОКСИ АВЗ 500 | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 881 | БАРС® спрей инсектоакарицидный | 6.7 | мг/кг | 3 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 884 | Азилон® | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 886 | Тиамулин 45%, 80% | 5 | мг/кг | 800 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 887 | Курацеф Дуо | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 889 | Эймерал® 25 | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 890 | Алцефур® 50 | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 891 | Оксал® 200 ЛА | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 896 | Амоксилонг® 150 ЛА | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 904 | Триметин | 15 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 905 | Антигрибковый и противоаллергический шампунь для животных | 10 | мг/кг | 0.1 | нет | По инструкции (наружное применение) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 908 | Триметин таблетки | 15 | мг/кг | 400 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 916 | Доксипрем 200 | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 917 | Дитрим® OR | 5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 924 | Ветцифлин | — | мг/кг | 10 | нет | по инструкции препарата: схема применения указана в инструкции, 1 раз в месяц, к | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 926 | Амоксоил Ретард | 15 | мг/кг | 150 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 931 | Тиалонг® 80% Feed | 3 | мг/кг | 800 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 933 | Инсектал комбо К | 0.003 | мг/кг | 107.5 | да |  | ОТКРЫТЫЙ ВОПРОС | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 937 | Тиалонг® 45% WS | 3 | мг/кг | 450 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 938 | Гепатолюкс PROtect суспензия | 1.5 | мг/кг | 15 | да | 0.8 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 941 | Фоллигон | — | МЕ/кг | 5000 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 944 | Таблетки тетрациклина | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 946 | Чистотел Максимум спрей | 7.5 | мг/кг | 3.32 | да | спрей: наносить по инструкции, 1 раз в месяц, курс однократно | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 947 | Инспектор Мини | 0.1 | мг/кг | 5.2 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 948 | Гепатолюкс PROtect таблетки | 1.5 | мг/кг | 15 | да | 0.5-1 таблетка | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 949 | Марбофлоцин®10% | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 950 | ЦИПРОСТИМ 10% | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 955 | Детокс | 0.1 | мл/кг | 50 | да | по инструкции: 1 мл/10 кг, внутривенно (медленно) или подкожно | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 957 | БлохНэт® max | 0.5 | мг/кг | 1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 958 | Катобевит® | 5 | мг/кг | 100 | да | 2.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 962 | Амоксипрем 200 | 12.5 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 963 | Кетопроф | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 965 | Кайод таблетки | 5 | мг/кг | 3 | да | 5 мг/кг (3.0 мг/табл) ≈ 6.7 табл на 4кг. 1 раз в день | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 969 | Септо-спрей | — | мг/кг | 30 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 970 | Мазь ихтиоловая 10% | — | мг/кг | 10000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 972 | БАРС® ошейник инсектоакарицидный | 7.5 | мг/кг | 40 | да | ошейник: надеть на животное, заменять по инструкции (1 раз в месяц) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 974 | Веткокцин | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 975 | Амоксициллин 15% ЛА | 12.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 982 | Бутастим | 1.5 | fixed | 100 | нет | 0,5-2,5 мл на животное | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 986 | Пуревакс RCP Rabies | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 987 | Пуревакс RCPCh Rabies | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 989 | Фелиген® CRP/R | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 991 | Лиарсин раствор для перорального применения | — | мг/кг | — | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 992 | Сультеприм® раствор для орального применения | 5 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 994 | ДОКСИСТИМ 10% | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 995 | Инсектал ошейник | 6.7 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1004 | Празител® Особый суспензия | 5 | мг/кг | 1.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1007 | Репарин-Хелпер® | — | fixed | 0.05 | нет | наружно на повреждённый участок 1-2 раза в сутки | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1008 | Тулатрин® | 2.5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1010 | Нобивак® Ducat | — | мг/кг | 0.5 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1011 | Гельмимакс® | 2 | мг/кг | 20 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1012 | Сульфадокс | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1015 | Дана® Ультра спрей | 7.5 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1021 | Ветэприн | 0.5 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1026 | Авертель | 5 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1027 | Анальгивет | 1 | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1031 | СЕКС БАРЬЕР® таблетки для кошек и сук | 2 | мг/кг | 0.1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1034 | Семинтра® 10 мг/мл | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1036 | ЦЕФТИСИЛ® гидро | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1037 | СексКонтроль спот-он | — | мг/кг | 24.75 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1038 | ЦЕФТИСИЛ® | 2 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1040 | Гамавит | 0.5 | мл/кг | 0.02 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 1043 | ГЕНТАФЛОКС® инъекционный | 5 | мг/кг | 65 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1048 | Риботан | 0.1 | мл/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 1055 | ОВОСТОП®-К | 2 | мг/кг | 11 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1056 | Фиприст® Комбо | 6.7 | мг/кг | 120 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1058 | Тиеркал | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1062 | Оксилонг® ретард | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1066 | СЕКС БАРЬЕР® таблетки для котов и кобелей | 2 | мг/кг | 0.4 | да | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1075 | Фронтлайн Комбо | 5 | мг/кг | 100 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC |
| 1078 | Мильбецин Нео для кошек | 5 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1079 | Цефтонит® Форте | 2 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1086 | Бинакар Форте | 10 | мг/кг | 80 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1087 | Мильбецин Нео для собак | 5 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1090 | РольфКлуб 3D ошейник для кошек | 7.5 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1092 | Кокцидикс® | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1094 | Неодиар | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1097 | Фронтлайн Спот Он | 6.7 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1099 | Фронтлайн Спрей | 6.7 | мг/кг | 250 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC |
| 1100 | ЭНРОСОЛ® 10% раствор для орального применения | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1103 | Неотерика Протекто сироп | 0.1 | мг/кг | 1.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1104 | Фоспренил | 0.1 | мг/кг | 4 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1107 | Максидин 0,15 | 0.15 | мг/кг | 1.5 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1112 | Доксициклин-комплекс | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1115 | ЭНРОСОЛ® 5% , 10% раствор для инъекций | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1119 | Левоксивет | 5 | мг/кг | 125 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1121 | Биоциллин-150 LA | 12.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1122 | Нобивак® Tricat Trio с растворителем Нобивак® Дилуент | — | мг/кг | 0.5 | нет | 0.5 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1127 | Келапрофен | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1128 | Глистогон Плюс суспензия | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1129 | Инспектор ошейник | 7.5 | мг/кг | — | нет | ошейник: надеть на животное, заменять по инструкции (1 раз в месяц) | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1130 | Инспектор спрей | 7.5 | мг/кг | 3.46 | да | спрей: наносить по инструкции, 1 раз в месяц, курс однократно | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1131 | Антивир | 15 | мг/кг | 90 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1132 | Докси ВС 50 | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1138 | Ривициклин® А | 15 | мг/кг | 125 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1142 | РольфКлуб 3D спрей для собак | 6.7 | мг/кг | 3.3 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1144 | Колимиксол® 6 млн МЕ и 12 млн МЕ | 50000 | МЕ/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ME_NO_ACTIVITY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1145 | Пеникел 15+15 ЛА | 25000 | МЕ/кг | 300000 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1148 | Иноксел | 2 | мг/кг | 60 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1150 | Террамицин Аэрозоль Спрей | 10 | мг/кг | 4000 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1154 | ДОКСИОР® 10% | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1165 | Докси ВЛ 50 | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, INDICATION_NO_SPECIES, NO_OFFICIAL_SOURCE |
| 1175 | Куртикол® раствор для перорального применения | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1176 | ИН-АП комплекс® | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1178 | Незамин | 3 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1180 | Празител® таблетки | 5 | мг/кг | 20 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1186 | Мекситар | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1190 | КонтрСекс Neo®  таблетки для кошек и сук | 0.5 | мг/кг | 0.12 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1191 | Стоморджил 2, 10, 20 | 15 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1192 | КонтрСекс Neo®  таблетки для котов и кобелей | 0.5 | мг/кг | 0.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1199 | Бродлайн Спот-Он | 5 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1201 | Селафорт® | 6 | мг/кг | 60 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1205 | Нефроантитокс | 0.75 | мл/кг | 80 | да | по инструкции (внутрь) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 1211 | Витаминно-аминокислотный комплекс "ВИТАМ" | — | мг/кг | 1000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1212 | Вермидин® таблетки | 5 | мг/кг | 15 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1213 | Празител® суспензия | 5 | мг/кг | 3 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1215 | Нозевир | 15 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1223 | Энрофлон®-К | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1240 | Тилдокс АВЗ | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, INDICATION_NO_SPECIES, NO_OFFICIAL_SOURCE |
| 1244 | Энроколи инъекционный | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1248 | Докси-фуд® | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1250 | АЙВЛОЗИН® 42,5 мг/г | 15 | мг/кг | 250 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1252 | 4Хувс | — | мг/кг | 24.12 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1256 | Анти-тикс | 7.5 | мг/кг | 85 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1258 | Комбикел 40 ЛА | 20 | мг/кг | 120 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1262 | Арбимектин | 0.075 | мг/кг | 0.75 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1263 | Санакард шампунь | 7.5 | мг/кг | 2 | да | шампунь: наносить по инструкции, 1 раз в месяц, курс однократно | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1267 | Догферон® раствор для инъекций | 0.8 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1268 | Санакард | 9 | мг/кг | 90 | нет | по инструкции препарата: схема применения указана в инструкции, 1 раз в сутки, к | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1269 | Шампунь хлоргексидиновый с антибактериальным эффектом для животных | 0.1 | мг/кг | 50 | да | шампунь: наносить по инструкции, 2-3 раза в день, курс 3-5 дней | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1280 | Х-ГИА | — | мг/кг | 950 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1288 | Амокси ВЛ 80 | 12.5 | мг/кг | 800 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, INDICATION_NO_SPECIES, NO_OFFICIAL_SOURCE |
| 1295 | Дана® Ультра | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1296 | Дана® Спот-он | 6.7 | мг/кг | 50 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1302 | БлохНэт® спрей | 0.5 | мг/кг | 1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1308 | Вакдерм-F | — | мг/кг | 3 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1311 | Празицид® таблетки | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1313 | Дирофен® таблетки | 15 | мг/кг | 120 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1318 | Энрофлокс 10% инъекционный | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1319 | Фунгин® Форте | 0.1 | мг/кг | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1320 | Плацента денатурированная эмульгированная (ПДЭ) | — | мг/кг | 250 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1324 | КАРДАНОН® | 0.1 | мл/кг | 125 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1325 | Зоосорб® | 1 | мл/кг | 920 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 1328 | Стоп-интим® капли | 5 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1329 | Амоксисан | 12.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1333 | Стоп-Интим® таблетки для кошек | 0.5 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1334 | Стоп-стресс® таблетки 2 и 5 | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1337 | Фелиферон® раствор для инъекций | 1 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1345 | Дезацид | — | fixed | 1 | нет | 1 капля в глаз/нос | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1346 | БАРС® форте капли для кошек против блох и клещей | 6.7 | мг/кг | 10 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1350 | Пиро-Стоп® | 2 | мг/кг | 120 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1351 | БлохНэт® Форте | 7.5 | мг/кг | 75 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1355 | Ципроген | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1359 | Декта® Форте | 0.5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1360 | РольфКлуб 3D ошейник для собак | 6.7 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1362 | РольфКлуб 3D спрей для кошек | 6.7 | мг/кг | 3.3 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1363 | Фенпраз суспензия | 25 | мг/кг | 6 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1365 | Гельминтал сироп | 0.1 | мг/кг | 0.3 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1366 | Доксициклин 20% | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1367 | Нитокс® Форте | 10 | мг/кг | 340 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1370 | Фенпраз таблетки | 5 | мг/кг | 75 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1372 | Доксилокс® WS | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1374 | Отоксолан® | 2 | мг/кг | 3 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1375 | Маропиталь | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1376 | Кетопрофен 10% | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1387 | Кетоджект® | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1395 | Инспектор Квадро Табс | 10 | мг/кг | 20 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1398 | Празител®  плюс суспензия | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1400 | Амоксилонг™ 150 LA | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1403 | Фронтлайн Три-Акт | 6.7 | мг/кг | 67.6 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1406 | Оксицивен LA 200 | 10 | мг/кг | 200 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1410 | Глистогон суспензия | 5 | мг/кг | 10 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1415 | Окситоцин | — | fixed | 10 МЕ/мл | нет | 3-5 МЕ (0,3-0,5 мл) на животное в/м | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1417 | Линдокс | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1419 | Празител® плюс таблетки | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1420 | Раствор Рингера-Локка | 0.15 | мл/кг | 9 | да |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, ML_PER_KG_ON, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1422 | Аквадокс | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1423 | Инспектор ушные капли | 0.003 | мг/кг | 0.11 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1431 | Зоодерм® | 7.5 | мг/кг | 200 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1436 | Клиодезив | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1437 | КОЛИФЛОКС® инъекционный | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1440 | Празицид®-суспензия Плюс | 7.5 | мг/кг | 45 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1441 | Медитин® | 0.08 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1443 | Интекол | 3.75 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1444 | Гентам® | 2.4 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1446 | Стоп-кокцид® | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1447 | Дана® шампунь | 10 | мг/кг | 5 | да | шампунь: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1448 | Вазосан® | 0.125 | мг/кг | 1.25 | да | 0.25 мг/кг (1.25 мг/табл) ≈ 0.8 табл на 4кг. 1 раз в день | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1451 | Раносан® порошок | 15 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1452 | Стоп-зуд® спрей | 15 | мг/кг | 0.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1453 | Цефтиосан® | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1454 | Дирофен®-суспензия 20 и 60 | 7.5 | мг/кг | 15 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1455 | Раносан® мазь | 2 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1456 | Гепатоджект® | — | мг/кг | 40 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1457 | Сульфетрисан® | 0.1 | мг/кг | 0.1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1458 | Дирофен® -паста 20 и 60 | 7.5 | мг/кг | 15 | да |  | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1462 | АПСАМИКС ОКСИТЕТРАЦИКЛИН 20% | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1464 | СексКонтроль капли | 0.5 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1465 | Чистотел пудра | 10 | fixed | 4 | да | пудра: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1466 | Неотерика Протекто 4 | 10 | мг/кг | 94.6 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1467 | Чистотел глистогон | 5 | мг/кг | 25 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1468 | Суролан | 1 | мг/кг | 23 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1470 | Инсектал капли | 6.7 | мг/кг | 99 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1471 | РольфКлуб ошейник антипаразитарный | 0.006 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1472 | РольфКлуб 3D капли для кошек | 6.7 | мг/кг | 101 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1473 | Чистотел зоошампунь | 10 | мг/кг | 4.2 | да | шампунь: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1475 | Чистотел Максимум капли | 6.7 | мг/кг | 47.5 | да | капли: наносить по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1478 | РольфКлуб 3D капли для собак | 6.7 | мг/кг | 101 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1479 | Секс-контроль С | 5 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1482 | Секс-контроль К | 0.5 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1485 | РольфКлуб 3D шампунь | 1.89 | мг/кг | 2.1 | да | шампунь: наносить по инструкции, 1 раз в сутки, курс ежемесячно | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1486 | Чистотел Максимум ошейник | 6.7 | мг/кг | — | да | ошейник: надеть на животное, заменять по инструкции (1 раз в месяц) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1488 | Гельминтал Т | 0.1 | мг/кг | 0.4 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1489 | Гельминтал К | 0.1 | мл/кг | 10 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1490 | Чистотел зооспрей | 10 | мг/кг | 3 | да | спрей: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1492 | Инспектор Квадро К | 5 | мг/кг | 10.7 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1494 | Цитодерм® капли ушные антибактериальные | 5 | мг/кг | 1.11 | да | 2-3 капли в ухо | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1495 | Инспектор Квадро С | 5 | мг/кг | 21.4 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1496 | Настойка полыни | — | мг/кг | 20000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1498 | Оксибактоцид® пластины | 10 | мг/кг | 30 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1500 | Оксибактоцид® порошок | 10 | мг/кг | 800 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1506 | Кетоквин®  1%, 10% | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1510 | Эйметерм суспензия 5% | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1511 | Вазотоп Р | 0.125 | мг/кг | 0.625 | да | 0.25 мг/кг (0.625 мг/табл) ≈ 1.6 табл на 4кг. 1 раз в день | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1515 | АМОКСИСТИМ 15% | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1518 | Милпразон® таблетки для кошек | 5 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1519 | Милпразон® таблетки для собак | 5 | мг/кг | 2.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1522 | Макродокс 200® | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1523 | Капли Фолайн® | 0.01 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1524 | Дитрим® порошок | 5 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1525 | Диазинон-С | — | мг/кг | 60000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1526 | Вирусан | 3 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1532 | КонтрСекс Neo® капли для кошек и сук | 0.5 | мг/кг | 1.2 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1534 | КонтрСекс Neo® капли для котов и кобелей | 0.5 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1536 | Гестренол® таблетки | 0.035 | мг/кг | 0.15 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1537 | Гестренол® капли | 0.035 | мг/кг | 1.5 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1548 | Амоксигард® | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1549 | Колистин 2 млн. | 50000 | МЕ/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ME_NO_ACTIVITY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1558 | Марфлоксин® 10% раствор для инъекций | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1559 | Марфлоксин® таблетки | 2 | мг/кг | 5 | да | 2 мг/кг (5.0 мг/табл) ≈ 1.6 табл на 4кг. 1 раз в день | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1568 | Пропалин® | 2 | мг/кг | 50 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1569 | Ауризон® | 2 | мг/кг | 3 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1570 | Азоксивет® | 0.5 | мг/кг | 1.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1571 | Веракол® раствор для перорального применения | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1576 | Доксилокс® ОR | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1577 | Кофеин-бензоат натрия 20% раствор для инъекций | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1585 | Амоксициллин 15% LA | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1587 | Доксициклин 200 | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1588 | Мексидол-Вет® | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1591 | ЧЕТЫРЕ С ХВОСТИКОМ® таблетки | 0.5 | мг/кг | 5 | да | 5 мг/кг (5.0 мг/табл) ≈ 4 табл на 4кг. по схеме | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1594 | ФЕБТАЛ® таблетки | 50 | мг/кг | 150 | да | 50 мг/кг (150.0 мг/табл) ≈ 1.3 табл на 4кг. 1 раз в день, 3 дня | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1596 | Соладокси® 500 | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1598 | Бутофан® | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1610 | Ноземат® | 10 | мг/кг | 400 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1613 | Оксивит® порошок | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1615 | Оксивит® полоски | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1617 | Энрофлон® 2,5%, 5% и 10% раствор для инъекций | 5 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1618 | Флексопрофен® 2,5%, 5% и 10% | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1627 | Мелапол | 3 | мг/кг | 8 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1632 | Линковик | 15 | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1635 | Тиоцефур® | 2 | мг/кг | 50 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING |
| 1636 | Долинк | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1637 | Тиланик 5% и 20% раствор для инъекций | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1639 | Эмидонол 20% | 3.5 | мг/кг | 200 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1640 | Квантум | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1641 | Гентамицин 4% и 5% раствор для инъекций | 3 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1644 | Мизоксин® | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1646 | Флорикол® | 15 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1647 | БАЦИЛИХИН® | 15 | мг/кг | 90000 | да | по инструкции (внутрь) | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1649 | Фенбенгран® | 50 | мг/кг | 222 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1654 | Тиациклин® | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1656 | Сультеприм® | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1660 | Неомицина сульфат | 10 | мг/кг | 680 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1666 | Ветбензицин-5 | 25000 | МЕ/кг | 1.2e+06 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1668 | ФЕБТАЛ® гранулы | 50 | мг/кг | 222 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1675 | Терраветин-500 | 10 | мг/кг | 500 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING |
| 1676 | Касептурин® | — | мг/кг | 500 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1683 | ПЕДИЛАЙН ХУФКЕА | — | мг/кг | 17.72 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1684 | Кальция борглюконат | 0.75 | мл/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, ML_PER_KG_ON, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1685 | Мазь тетрациклиновая 3% | 10 | мг/кг | 3000 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1686 | Мазь Яхалимп® | — | мг/кг | 10000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1687 | Гликосан® | — | мг/кг | 3000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1689 | Мазь ихтиоловая 10% и 20% | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1690 | Мазь серная простая | — | мг/кг | 33000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1691 | Мазь цинковая | 3 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1695 | Мазь Экзеконт | 2 | мг/кг | 5000 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1696 | Серения | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1697 | Альбамелин® | 25 | мг/кг | 100 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | REG_ANIMALS_EMPTY |
| 1701 | Эксенел стерильный порошок | 2 | мг/кг | 60 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1704 | Дексафорт | 0.2 | мг/кг | 3 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1709 | Йод однохлористый | — | мг/кг | 3000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1710 | РЕПТИЛАЙФ® суспензия | 5 | мг/кг | 25 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1717 | Кламоксил LA | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1723 | Линимент синтомицина 1%, 5%, 10% | 25 | мг/кг | 10000 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1724 | Ковинавет | 0.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1729 | Энроксил® 5% раствор для инъекций | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1733 | Синулокс RTU | 12.5 | мг/кг | 140 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1734 | Наксел | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1735 | Эксид | 2 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1738 | Пихтоин® | — | мг/кг | 20000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1746 | Вирусвакцина против чумы мелких жвачных культуральная сухая | — | мг/кг | 2 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1751 | Амоксициллин 150 | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1754 | Мазь салициловая 2%, 5%, 10% | 1 | мг/кг | 2000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1758 | Ронколейкин® | 10000 | МЕ/кг | 50000 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1767 | Пигфен® 40 | 50 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1780 | Панакур® Паста | 50 | мг/кг | 187.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1782 | Имозимаза | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1783 | Мазь стрептоцидовая | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1786 | Мазь серно-дегтярная | — | мг/кг | 5000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1794 | Эффитикс® | 6.7 | мг/кг | 61 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1799 | Террамицин LA | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1801 | Лобелон® | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1804 | Гидродокс® 50% | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1809 | Азитронит® М | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1810 | Гидродокс® 10% оральный раствор | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1811 | Гидродокс® 10% | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1816 | Азинокс® ветеринарный | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1819 | Семинтра® | 1 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1820 | Фелоцел 4 | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1823 | Фелоцел CVR | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1829 | Дехинел® таблетки для кошек | 5 | мг/кг | 230 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1844 | Мазь стрептоцидовая 10% | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1845 | Мазь цинковая 10% | 3 | мг/кг | 10000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1847 | Цемай | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1853 | Кетомай | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1854 | Кафорсен® раствор для перорального применения | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1858 | Доксмай | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1860 | ВИТАМЭЛАМ | 0.1 | мл/кг | 0.1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 1861 | Мазь ихтиоловая 10% | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1864 | Деликс капли инсектоакарицидные | 10 | мг/кг | 50 | да | капли: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1866 | Цефтонит® | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1868 | Актионис | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1871 | Капли инсектоакарицидные для кошек Мисс Кисс | 6.7 | мг/кг | 110 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1877 | Спрей инсектоакарицидный Мистер Бруно Плюс - Интенсивная защита/ Мисс Кисс - Интенсивная защита | 6.7 | мг/кг | 3 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1878 | Спрей инсектоакарицидный Мистер Бруно Плюс - Бережная защита/  Мисс Кисс - Бережная защита | 7.5 | мг/кг | 1 | да | спрей: наносить по инструкции, 1 раз в месяц, курс однократно | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1887 | Фебтал®-комбо | 5 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1889 | Метакам® | 0.2 | мг/кг | 20 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1891 | Капли инсектоакарицидные БАРС® форте | 6.7 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1895 | Фармазин® 50 и 200 | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1897 | Капли инсектоакарицидные Мистер Бруно Плюс - Интенсивная защита | 6.7 | мг/кг | 110 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1906 | Гентаприм | 3 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1909 | Фортиклин Ретард | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1912 | Родотет® | 20 | мг/кг | 33 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1924 | Ализин® | 10 | мг/кг | 30 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1936 | Неозидин® М | — | мг/кг | 57.5 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1942 | Альфакаин 2%+адреналин | 2 | мг/кг | 20 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1944 | Мазь ихтиоловая 10% и 20% | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1946 | Бензилпенициллина натриевая соль для инъекций | 25000 | МЕ/кг | 1e+06 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1949 | Неомицина сульфат | 10 | мг/кг | 1000 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1950 | Доксипрекс | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1955 | Деликс-Ф капли инсектоакарицидные | 6.7 | мг/кг | 80 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1957 | Неозидин® | — | мг/кг | 450 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1958 | Неуротранк | 0.05 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1959 | Гликопин® | — | мг/кг | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1962 | Стрептопен 20/20 | 25000 | МЕ/кг | 200000 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1963 | Доксикел 75 | 10 | мг/кг | 750 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1964 | Амоксициллин 20% LA | 15 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1966 | Прокпен 30 | 25000 | МЕ/кг | 300000 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1970 | Тривитамин (раствор витаминов А, Д3, Е в масле) | 0.1 | мл/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 1974 | Окситетрациклин 20% LA | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1975 | Линкомицин+спектиномицин 5/10 | 15 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1976 | Метронид 50 | 15 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1977 | Докси-500 WS | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1978 | Фуросемид 5% | 1 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1979 | Лиарсин | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1982 | Мазь ихтиоловая 10% | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1986 | Раствор гентамицина сульфата 4% | 3 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1987 | Тетрацилин | — | мг/кг | 40000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1991 | Мазь "Левомеколь-вет" | 50 | мг/кг | 750 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1992 | Ксилазин 2% | 1 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1996 | Кофеин-бензоат натрия 20% | 0.1 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1998 | Кальция борглюконат | 0.75 | мл/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, ML_PER_KG_ON, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 2002 | Тетраметр | 10 | мг/кг | 1000 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2005 | Дексаметазон 2 мг/см³ | 0.1 | мг/кг | 2 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2007 | Диастоп | 10 | мг/кг | 1 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING |
| 2012 | Разбавитель для вакцины Вермет против дерматофитозов животных | — | мг/кг | 5 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2015 | Кальфосет® | 50 | мг/кг | 820 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2016 | Е-селен® | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2017 | Е-селен® OR | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2020 | Глюкортин-20 | 0.1 | мг/кг | 2 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2026 | Супервитасол | 2.5e-06 | мг/кг | 1e+06 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2028 | Доксилокс® | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2035 | Дехинел® Плюс | 5 | мг/кг | 525 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2037 | Дехинел ® Плюс таблетки со вкусом мяса | 5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2038 | Тиамокс | 10 | мг/кг | 250 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2043 | Клинексин 5% | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2047 | Ивермек®-спрей | — | мг/кг | 2.5 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 2048 | Авидокс | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2050 | Эгоцин® 20 порошок | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2053 | Доксигор 10% | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2055 | Мазь фармайодная® антисептическая | — | мг/кг | 5 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2058 | Фиприст® Спот Он | 7.5 | мг/кг | 100 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2059 | Каридокс | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2063 | Энровек 5% и 10% | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 2068 | Амоксивек-форте | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 2069 | Энроксил® Макс | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2070 | Форвет® | — | мг/кг | 0.04 | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2071 | Гентамицина сульфат 4% раствор для инъекций | 3 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2078 | Тилозин 50 и Тилозин 200 | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2079 | Дитрим® | 5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2082 | Эфикур | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2084 | Ализерил WS | 10 | мг/кг | 35 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2085 | Толтарокс® | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2087 | Амоксициллин 15% | 10 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 2090 | Мазь Левомеколь | 50 | мг/кг | 750 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2093 | Энромокс® | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2094 | Антиовод | — | мг/кг | 12 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2095 | Энронит ®OR | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2098 | Веракол® | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2102 | Геомицин® Ф | 10 | мг/кг | 1000 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2105 | Лучший друг гельмистоп | 50 | мг/кг | 250 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2106 | Лучший друг вермистоп | 5 | мг/кг | 45 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2108 | Мазь тетрациклиновая глазная 1% | 10 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2110 | Нитокс® 200 | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2113 | Бальзам ДОРОГОВОЙ® | — | мг/кг | 20 | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2114 | Гентамицина сульфат 4% | 3 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2116 | Травматин® | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2118 | Бактил 5% инъекционный | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 2120 | Эндотил-форте | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2121 | Мастометрин® | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2124 | Фоспасим® | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2126 | Кафорсен® | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2128 | Гентамицина раствор 4% | 3 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2129 | Ипакитине | 1 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, ZERO_CONC_WITH_DOSE, NO_OFFICIAL_SOURCE |
| 2130 | Ковертал | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2133 | Ксиланит® | 1 | мг/кг | 20 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2136 | Зооксилазин | 1 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 2138 | Гемобаланс | 5 | мг/кг | 1 | нет | 0.25-0.5 мл по массе (<5 кг: 0.25; 5-15: 0.5), 2-3 р/нед | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2141 | Фелиген® CRP | — | мг/кг | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2142 | Кубатол® Пикс Аэрозоль | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2143 | Амоксициллин инъекционный | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 2145 | Энронит® | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2148 | Присыпка Эдис | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2160 | Иноксел RTU | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2161 | Окситетрациклин ЛА | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2162 | Глюкэтин | — | мг/кг | 20 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2172 | Мультивек | 0.0325 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2179 | Вакцина против хламидиоза животных "ХламидиоВак" | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2181 | АД3EF | — | fixed | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2183 | АД3Евит | 7.75 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2189 | Докси Форте | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2191 | Бимоксил LA | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 2201 | Скавон Вет Крем | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2208 | Гонасил | 0.01 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2213 | Фебрин Порцино | 10 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, ZERO_CONC_WITH_DOSE, NO_OFFICIAL_SOURCE |
| 2222 | 30%-ный раствор глицерина для разбавления вакцин против сибирской язвы животных | — | мг/кг | 300 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2225 | Тромексин | 5 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ZERO_CONC_WITH_DOSE, NO_OFFICIAL_SOURCE |
| 2227 | Квинокол 10 | 5 | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2228 | Фипрекс спрей форте | 6.7 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2229 | Биофел® PCHR | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2231 | Айнил 1% | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 2233 | Фипрекс 75 спот-он | 6.7 | мг/кг | 75 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2234 | Биофел® PCH | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2239 | Линкоспектин | 15 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 2240 | Геставет-GnRH | 0.01 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2249 | Дюфалайт | 0.075 | мл/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2256 | Окситетра 50% W.S. | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2259 | Линимент синтомицина 5% | 25 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2266 | Нуклеопептид | 0.1 | мл/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2267 | Энтероспорин | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2270 | Амит форте | 6.7 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2271 | Интерспектин-L | 15 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2275 | Зинаприм | 5 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 2276 | Лигфол | 0.1 | мг/кг | 6 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2282 | Мазь цинковая 10% | 3 | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 2285 | Окситетрациклин 100 | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2287 | Гидроксин | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2288 | Монклавит-1 | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2292 | Квинокол Гидро | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2294 | Квинокол Плюс | 5 | мг/кг | 65 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2296 | Колмик-Е | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2298 | Тетралонг-20 | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2303 | Настойка боярышника | — | мг/кг | 65 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2308 | Экстракт прополиса спиртовый | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2309 | Мазь прополисная | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2310 | Водная суспензия прополиса | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2321 | Витафлеш Амино WSP | 0.1 | мг/кг | 30 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2322 | Пенстреп-400 | 12500 | МЕ/кг | 200000 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2324 | Нео-Окси WSP | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2325 | Мультивитамин инъекции | — | мг/кг | 3 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2327 | Кепроцерил WSP | 10 | мг/кг | 30 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2328 | Лимоксин-200 LA | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2331 | Ветбицин-5 | 25000 | МЕ/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, ME_NO_ACTIVITY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2333 | Ветбицин-3 | 25000 | МЕ/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, ME_NO_ACTIVITY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2337 | Лимоксин-25 спрей | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2338 | Окситетрациклина гидрохлорид для инъекций | 10 | мг/кг | 100 | нет |  | ОТКРЫТЫЙ ВОПРОС | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, DUPLICATE_NAME |
| 2339 | Ксила | 1 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2341 | Мазь ихтиоловая 10% и 20% | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 2343 | Докси-10 | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2351 | Алюспрей | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2352 | Вакцина против ящура универсальная сорбированная моно- и поливалентная (из вируса, выращенного в клетках ВНК-21) | — | мг/кг | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2356 | ПЕЦИВЕТ | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2357 | Ранозоль | — | мг/кг | 0.31 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2359 | Абивертин® | 0.2 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2362 | Амитан | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2364 | Диазинон-Евровет | — | мг/кг | 60 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2367 | Галастоп | 0.005 | мг/кг | 0.05 | да | 0,1 мл (3 капли) на 1 кг массы внутрь, 4-6 дней | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2378 | Ферроцин | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2379 | Бифеж | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2380 | Гентамокс | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2384 | Мазь Анандин | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2387 | Шустрик суспензия | 5 | мг/кг | 50 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2388 | Антибак ПРО | 5 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_SPECIES_MISSING, ZERO_CONC_WITH_DOSE, NO_OFFICIAL_SOURCE |
| 2391 | Септифорт спрей | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
