# Полный сквозной аудит: «Собаки»

Препаратов с видом «Собаки»: **1088** из 2401. 
Статус «ТРЕБУЕТ ИСТОЧНИКА» означает: официальная инструкция под конкретную запись в наших аудитах **не подтверждена**. Это не AUTO и не «норма» — запись подлежит проверке.

Статусы: ОТКРЫТЫЙ ВОПРОС — 8, ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО — 19, ТРЕБУЕТ ИСТОЧНИКА — 1061

## Флаги

| Код | ЧтоMeans | Количество |
|---|---|---|
| CALC_OFF_DOSE | калькулятор выключен, но числовая доза есть (нужен явный источник) | 133 |
| DB_ANIMALS_MISMATCH | список видов не совпадает между calc и verified | 392 |
| DB_CONC_MISMATCH | концентрация/единица не совпадают между calc и verified | 72 |
| DB_DOSE_MISMATCH | видовая доза не совпадает между calc и verified | 11 |
| DB_FREQ_MISMATCH | частота не совпадает между calc и verified | 38 |
| DUPLICATE_NAME | несколько записей с одним названием | 29 |
| EXTERNAL_NUMERIC | наружный путь при включённом численном расчёте | 135 |
| GHOST_SPECIES | вид есть в animals, но нет в animal_specific (или наоборот) | 102 |
| INDICATION_NO_SPECIES | в показаниях реестра названы другие виды, а этот нет | 16 |
| ME_NO_ACTIVITY | доза в МЕ/кг, но активность МЕ/мл не задана | 12 |
| ML_PER_KG_ON | доза в мл/кг при включённом калькуляторе (движок берёт глобальную единицу) | 25 |
| NO_OFFICIAL_SOURCE | в наших аудитах нет подтверждающей официальной инструкции | 1061 |
| REG_ANIMALS_EMPTY | в реестре поле animals пустое (нет данных, не противоречие) | 519 |
| REG_ANIMALS_INCOMPLETE | вида нет в animals реестра, но он назван в показаниях (метаданные) | 11 |
| REG_CONTRADICTION | реестр явно сужает вид: нет в animals и нет в показаниях | 10 |
| REG_SPECIES_MISSING | в реестре явно указаны другие виды, а этот отсутствует | 189 |
| ZERO_CONC_WITH_DOSE | есть масса-доза, но концентрации нет | 25 |

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
| 1 | Мариния® | 2 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 5 | Ноземацид® | 10 | мг/кг | 600 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 7 | БАРС® капли инсектоакарицидные | 15 | мг/кг | 150 | да | по инструкции (наружно), 1 раз в сутки, курс однократно | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | EXTERNAL_NUMERIC |
| 8 | Биофертагил | 0.001 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 9 | Фунгин® таблетки | 5 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 10 | Изофлуран Миралек | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 14 | Бонхакан | 2 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 15 | Марбофлоксацин 10% | 2 | мг/кг | 100 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION |
| 16 | Сурфагон Ультра | 0.001 | мг/кг | 0.05 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 17 | МУЛЬТИКАН-L | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 18 | МУЛЬТИКАН-LR | — | мг/кг | 0.5 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 19 | Эмпазекс | 0.5 | мг/кг | 3 | да | 0.5 мг/кг (3.0 мг/табл) ≈ 1.7 табл на 10кг. 1 раз в день | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 20 | Робексера® | 1 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 22 | Гатилон® ТАБ | 0.5 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 23 | Триладикс | 3 | мг/кг | 10 | да | 3 мг/кг (10.0 мг/табл) ≈ 3 табл на 10кг. 1 раз в день | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 24 | ПИМОКАРДИН® | 0.25 | мг/кг | 1.25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 25 | Марбопрайм® | 2 | мг/кг | 100 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY |
| 27 | Кормедан-S | 0.25 | мг/кг | 1.25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 29 | Силта® | 1 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 30 | Фениквантел® | 5 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 32 | Зинтирил | 1 | мг/кг | 2 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 33 | МУЛЬТИКАН-DP | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 34 | Дехиспот® | 5 | мг/кг | 85.8 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 35 | МУЛЬТИКАН-DHP | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 36 | ЭприЛюкс 0,5% Пур-он | 0.5 | мг/кг | 5 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | GHOST_SPECIES, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 45 | ТРАНЕКСАМ-ВЕТ | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 47 | Изофлуран | — | мг/кг | 1000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 48 | Виратек R | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 49 | Веприпак® | 25 | мг/кг | 112.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 55 | Вемелкам® 2% | 0.2 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 56 | Виратек 9 | — | мг/кг | 1 | нет | 2.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 60 | Адексме® | 0.015 | мг/кг | 0.1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 61 | Нефопам-ВЕТ | 0.75 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 62 | Флексонорм® | 1 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 63 | ОФТАЛЬМИКА® мазь глазная | 5 | мг/кг | 15 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 65 | Рабектра® | 25 | мг/кг | 112.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 69 | Ливеразол-ИЗ | — | мг/кг | 100 | нет | по инструкции (наружно), ванночки, курс 3-7 дней | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 76 | Бутал® | 5 | мг/кг | 100 | да | 5.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 77 | ГОНАХОРИЛ®-ВЕТ | 0.02 | мг/кг | 500 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 83 | Конафлион | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 84 | Петмелокс VETЗАБОТА® | 0.1 | мг/кг | 0.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 86 | Робенекс® | 1 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 89 | Кардимекс® | 0.25 | мг/кг | 1.25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 92 | Карникан Puppy DP | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 93 | Менбутил | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 95 | Фенпраз Форте суспензия | 2.88 | мг/кг | 28.8 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 96 | OKVET® Шампунь лечебный с хлоргексидином | 0.1 | мг/кг | 50 | да | шампунь: наносить по инструкции, 1 раз в сутки, курс 3-5 дней | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 97 | Фенпраз Форте таблетки | 2.88 | мг/кг | 28.8 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 98 | Уристоп | 2 | мг/кг | 40.28 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 102 | Бофлокс | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE |
| 103 | Марботим таблетки | 2 | мг/кг | 5 | да | 2 мг/кг (5.0 мг/табл) ≈ 4 табл на 10кг. 1 раз в день | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 107 | Мелоксикам Апиценна раствор для инъекций | 0.1 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 111 | Амклав®Вет | 12.5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 112 | Оноксеб® | 1 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 113 | Инсектал® комбо таблетки | 0.006 | мг/кг | 0.4 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 119 | Карнивак Flu | — | мг/кг | 0.5 | нет | 5.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 121 | ВИНСУВЕТ микс 30/70 | 0.5 | МЕ/кг | 100 МЕ/мл | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 123 | Энроксил® 10% раствор для инъекций | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 124 | Бравуланер | 25 | мг/кг | 112.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 125 | БлохНэт® next капли | 10 | мг/кг | 100 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 127 | ФЛУВЕТОН | 25 | мг/кг | 280 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 130 | Тиломакс | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 131 | Дезацид Форте | 10 | мг/кг | 5 | да | 1-2 капли в глаз | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 132 | АМОКСИСТИМ V-15% | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 138 | БАРС® капли ушные | 0.05 | мг/кг | 0.3 | да | 3-5 капель в ухо | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 140 | Энросепт раствор для инъекций 5% и 10% | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 144 | Сенсиверин | 0.04 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 145 | ЛОПЕРАВЕТ | — | мг/кг | 0.13 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 147 | БАРС® капли глазные | 0.25 | мг/кг | 2.5 | да | 1-2 капли в глаз | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 155 | Полицефур | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 156 | Синклавир порошок | 12.5 | мг/кг | 575 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 158 | Ципрозол-200 Орал | 5 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 160 | Ветспокоин Трио таблетки | 5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 161 | Дирофен® Макс | 6 | мг/кг | 60 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 165 | Флурасейв спот-он | 25 | мг/кг | 280 | да |  | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 167 | Ветспокоин Трио суспензия | 5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 168 | Супрамил би макс таблетки | 0.5 | мг/кг | 5 | нет | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 169 | Тразапентин® таблетки | 5 | мг/кг | 36 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 171 | Мираклав® порошок для приготовления раствора для внутривенного введения | 12.5 | мг/кг | 250 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 172 | Отидез Форте | 2 | мг/кг | 5 | да | 3-5 капель в каждое ухо 2 раза в сутки | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | EXTERNAL_NUMERIC |
| 175 | ЛоксикVet суспензия | 0.1 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 176 | ЛоксикVet таблетки | 0.1 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 177 | Кормедан | 0.25 | мг/кг | 0.75 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 179 | Ветгаба таблетки | 5 | мг/кг | 60 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 181 | Нейрокард | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 185 | Ципровентор | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 186 | Бимаксгард® КОМПЛЕКС для собак | 2.5 | мг/кг | 25 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 189 | Зотрикс® | 25 | мг/кг | 112.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 194 | Фипритика | 6.7 | мг/кг | 10 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 195 | Бимаксгард® ПЛЮС | 50 | мг/кг | 500 | да | по инструкции: 0,1 мл/кг, пипетка по массе тела | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 200 | Бимаксгард® КОМПЛЕКС для кошек | 0.003 | мг/кг | 10 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 204 | Мазь левомицетиновая | 50 | мг/кг | 4000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 207 | Зуратрол® | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE |
| 209 | Доксатиб® | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, INDICATION_NO_SPECIES, NO_OFFICIAL_SOURCE |
| 210 | САЛЬМОГИР® | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 214 | Антибак 500 | 5 | мг/кг | 500 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 219 | Феномикс | 50 | мг/кг | 80 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 229 | Разбавитель для вакцин против дерматофитозов животных | — | мг/кг | 2 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 230 | Слипофол | 4 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 232 | Тилозин ТАБ | 10 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 233 | Афокса® | 3 | мг/кг | 11.3 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 237 | ДЕМЕТОВЕТ® | 0.015 | мг/кг | 0.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 238 | ЗоозащитаVet | 20 | мг/кг | 200 | да | по инструкции препарата: схема применения указана в инструкции | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 241 | БАРС® форте спрей инсектоакарицидный | 6.7 | мг/кг | 3.1 | да | спрей: наносить по инструкции, 1 раз в месяц, курс однократно | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 249 | АЙСИДИВИТ® | 10 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 251 | Флурасейв жевательные таблетки | 25 | мг/кг | 112.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 252 | Лонтривет | 1 | мг/кг | 2 | да | 0.5 мг/кг (2.0 мг/табл) ≈ 2.5 табл на 10кг. 1-2 раза в день | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 253 | Нефрокэт/дог | 2 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 255 | Синклавир таблетки | 12.5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 258 | ЦИПРОВЕТ® капли глазные | 5 | мг/кг | 4.5 | да | 1-2 капли в глаз | ОТКРЫТЫЙ ВОПРОС | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY |
| 261 | БРИЛЛИАНТОВЫЕ ГЛАЗА® капли глазные | — | мг/кг | 0.15 | нет | капли в глаз: по инструкции, 2-3 раза в день, курс 3 дня | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 262 | Сангвения | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 264 | Фуросенит-вет | 2 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 266 | Ветгаба | 5 | мг/кг | 60 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 268 | ОФТАЛЬМИКА® капли глазные | 0.5 | мг/кг | 5 | да | 1-2 капли в глаз | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 270 | Сенсиблекс® Вейкс | 0.04 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 271 | Мелоксикам Апиценна | 0.1 | мг/кг | 0.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 273 | Гонавет Вейкс® | 0.01 | мг/кг | 0.0524 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 274 | Окситрит | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 275 | Толфемакс 4%, 8% | 2 | мг/кг | 80 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 280 | Клозальбен®-10 | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 282 | ЦИПРОВЕТ®-пульмо | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 284 | Мильмакс-Нита для кошек | 5 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 285 | Мильмакс-Нита для собак | 5 | мг/кг | 2.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 286 | Отосур® | 2.3 | мг/кг | 23 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 289 | Неотерика Протекто 12 | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 290 | Маведин® | 0.25 | мг/кг | 1.25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 292 | Айнил | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 296 | ПимХарт | 0.25 | мг/кг | 1.25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 298 | Энралонг® 100 LA | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 300 | Алмексил® 20 | 0.2 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 304 | Ветодиметин® спрей | 0.1 | мг/кг | 1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 305 | Диазепам-ЭНДОФАРМ | 0.5 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 306 | Мильбецин Нео спот-он | 0.5 | мг/кг | 25 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 308 | Метоклопрамид-ЭНДОФАРМ | 0.5 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 309 | Кинорон® | 1 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 310 | Кетамин-ЭНДОФАРМ | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 311 | Эпинефрин-ЭНДОФАРМ | 0.01 | мг/кг | 1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 313 | Трамвет® | 3 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 314 | Гепарин натрия-ЭНДОФАРМ | 0.1 | мг/кг | 5000 МЕ/мл | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 318 | Рабиков | — | мг/кг | 1 | нет | 5.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 319 | Фипронника | 5 | мг/кг | 7.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 320 | Доксипул | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 323 | Окситоцин | — | fixed | 10 МЕ/мл | нет | 5-10 МЕ (0,5-1 мл) на животное в/м | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 324 | РанодезВЕТ спрей | — | мг/кг | 40 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 325 | Гапентин | 5 | мг/кг | 80 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 326 | Клавуксицин® таблетки | 12.5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 328 | "БИОНОР" | — | мг/кг | 200 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 330 | "БИОВАК" | — | мг/кг | 1 | нет | 2.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 333 | Селамигор® | 6 | мг/кг | 60 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 335 | VETOKO капли глазные для собак и кошек VETЗАБОТА® | 5 | мг/кг | 4.5 | да | 1-2 капли в глаз | ОТКРЫТЫЙ ВОПРОС | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY |
| 336 | Кеситая® | 0.03 | мг/кг | 1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 339 | Окситетрациклина гидрохлорид 1000 | 10 | мг/кг | 950 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 341 | Стоп-цистит® таблетки | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 344 | Интракокс Памп | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 345 | Фуросенит-вет® ТАБ | 2 | мг/кг | 8 | да | 2 мг/кг (8.0 мг/табл) ≈ 2.5 табл на 10кг. 2 раза в день | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 346 | Робексера® жевательные таблетки | 1 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 347 | Соладокси | 10 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 348 | Денаверин АВЗ | 0.04 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 351 | МаксиДропс® | 10 | мг/кг | 100 | да | по инструкции (наружно), 1 раз в сутки, курс однократно | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 353 | Но-презан® ТАБ | 10 | мг/кг | 4 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 356 | Сенсипол | 0.04 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 357 | Толтрекс 5% | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 359 | Энроксил® таблетки  со вкусом мяса | 5 | мг/кг | 15 | да | 5 мг/кг (15.0 мг/табл) ≈ 3.3 табл на 10кг. 1-2 раза в день | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 362 | Бактолевонид | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 363 | Оксибактонид | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 365 | Гиалувит Хондро | 2 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 366 | Принокат® | 2.5 | мг/кг | 25 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 368 | Калоксо® | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 370 | Но-презан | 2 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 371 | Принокат® кошки | 0.003 | мг/кг | 10 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 376 | ДаДокси С+ | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 377 | Холликалм® раствор для инъекций | 2 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 383 | Серинебс | 2 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 388 | Интракокс Орал | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 390 | Фунгивет Rus крем | 3 | мг/кг | 10 | да | По инструкции (наружное применение) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 391 | Фунгивет Rus спрей | 3 | мг/кг | 10 | да | По инструкции (наружное применение) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 393 | Тиломаг® | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 394 | Неомиксин | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 395 | Везотил® | 5 | мг/кг | 250 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 396 | Амокситрон жевательные таблетки | 12.5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 398 | Фирококсиб-АСТРА таблетки | 5 | мг/кг | 57 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 408 | Лидоканит Вет | 2 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 411 | Декеситая® | 0.015 | мг/кг | 0.1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 412 | Авекардит® | 0.25 | мг/кг | 1.25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 419 | Хетгард | 0.25 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 420 | АЛЬБЕН® С | 25 | мг/кг | 250 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 421 | Фунгивет Rus таблетки | 5 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 423 | Аквеллиум | 0.5 | мг/кг | 4.84 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 425 | Пинпрамиль® для кошек | 5 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 427 | Синклавир для инъекций | 12.5 | мг/кг | 161 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 436 | Бимаксгард ТАБС для кошек | 5 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 437 | Бимаксгард ТАБС для собак | 5 | мг/кг | 2.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 439 | Марботим | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE |
| 441 | Зоокард Rus суспензия | 0.06 | мг/кг | 0.625 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 442 | Акаромектин | 0.006 | мг/кг | 0.1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 443 | Зоокард Rus таблетки | 0.06 | мг/кг | 1.25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 448 | Мелоксигард | 0.1 | мг/кг | 0.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 449 | Диугард | 0.2 | мг/кг | 0.75 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 450 | Эктонеогид | 10 | мг/кг | 50 | да | по инструкции препарата: схема применения указана в инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 453 | Алевокса® | 5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 454 | Азинокс для собак и кошек | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 455 | Бинакар Rus | 10 | мг/кг | 80 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 457 | Энростин® Макс | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE |
| 458 | Докси WS | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, INDICATION_NO_SPECIES, NO_OFFICIAL_SOURCE |
| 460 | Азинокс плюс | 5 | мг/кг | 50 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 462 | Доксин-200 WS | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 464 | Кетотрит 2,5%, 10% | 1 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 468 | ОКСИТРОН® 200 | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 470 | Преднифарм | 0.5 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 471 | Канидерм | — | мг/кг | 1 | нет | 5.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 472 | Преднифарм® ТАБ | 1 | мг/кг | 4 | да | 0.5 мг/кг (4.0 мг/табл) ≈ 1.2 табл на 10кг. 1-2 раза в день | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 473 | Азитронит® ТАБ | 5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 474 | ФЛУВЕКТО® жевательные таблетки | 25 | мг/кг | 112.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 475 | Энрофаст | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 477 | Окситетрациклин 200 | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 480 | Зинаприм | 15 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_SPECIES_MISSING, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 482 | Толтрекс 2,5% | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 483 | Гельминтал Мини Табс | 5 | мг/кг | 9 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 488 | Цимифур® | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 490 | Холликалм® | 2 | мг/кг | 16 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 491 | Фироко® | 5 | мг/кг | 57 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 496 | Вемелкам | 0.1 | мг/кг | 2 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 499 | Вемелкам® ТАБ | 0.1 | мг/кг | 0.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 502 | Фалена | 2 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 504 | ИН-АП спрей | 6.7 | мг/кг | 2.2 | да | спрей: наносить по инструкции, 1 раз в месяц, курс однократно | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 505 | Мильбемакс® для собак | 5 | мг/кг | 2.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 506 | Натрия хлорид АРМ | 0.1 | мл/кг | 9 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 509 | Эктогардика | 20 | мг/кг | 12 | да | 10 мг/кг (12.0 мг/табл) ≈ 8.3 табл на 10кг. ежемесячно | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 512 | Раствор Рингера-Локка | 0.15 | мл/кг | 9 | да |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, ML_PER_KG_ON, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 514 | Мильбемакс® для кошек | 5 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 515 | ФОРСЕКТО® | — | мг/кг | 66.7 | нет | по инструкции препарата: схема применения указана в инструкции | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 521 | ЭкспрессТабс® | 75 | мг/кг | 150 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 524 | Пинпрамиль® для собак | 5 | мг/кг | 2.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 525 | Телмигард | 1 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 527 | Доксигор 50% | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 529 | Тилодокс-200 | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 530 | Трисульф ВС | 15 | мг/кг | 400 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION |
| 532 | Синуксол-Нита® | 12.5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 534 | Карникан-5R | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 536 | ПРОСПЕКТА®-ВЕТ | 12.5 | мг/кг | — | да | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | ZERO_CONC_WITH_DOSE, NO_OFFICIAL_SOURCE |
| 539 | Неотерика Протекто ошейник | 10 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 540 | Натрия хлорид изотонический 0,9% раствор для инъекций | 0.1 | мл/кг | 9 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 542 | Амоксимаг® | 12.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 546 | Ивермаг® | 0.006 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 548 | Кофеин-бензоат натрия 20% раствор для инъекций | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 554 | Энромаг® | 5 | мг/кг | 50 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 556 | Ципромаг®-О | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 557 | Уротропин® | 10 | мг/кг | 400 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 558 | Миксоферон® | 1 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 562 | Цианокобаламин | 0.05 | мг/кг | 0.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 564 | Триховет® | 15 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 565 | Цефтимаг® | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 566 | Тетрамаг® | — | мг/кг | 5 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 567 | Тривит® раствор для инъекций | 0.05 | мл/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 569 | Миксоферон® раствор для инъекций | — | МЕ/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, ME_NO_ACTIVITY, NO_OFFICIAL_SOURCE |
| 571 | Ципромаг® | 5 | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 572 | Эндометрамаг-Грин® | 3 | мг/кг | 15 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 577 | Тривит® | 0.05 | мл/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 578 | Карникан-4 | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 584 | Витамин D3 масляный раствор | — | МЕ/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, ME_NO_ACTIVITY, NO_OFFICIAL_SOURCE |
| 587 | Витамин А масляный раствор | 0.2 | мг/кг | 100000 МЕ/мл | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 588 | МУЛЬТИКАН-8 | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 589 | Ципрофлоксацин 10% | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, INDICATION_NO_SPECIES, NO_OFFICIAL_SOURCE |
| 590 | Линкомицин 10 % раствор | 15 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 591 | Гентамицина сульфат 4 % раствор | 3 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 594 | Супримицин® | 4 | мг/кг | 40 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 596 | ЛЕОМИНОР | — | мг/кг | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 597 | Кальция борглюконат | 0.75 | мл/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, ML_PER_KG_ON, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 601 | Окситетрамаг 20® | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 606 | Доксимаг®-О | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 607 | Кальция хлорид 10% раствор для инъекций | 15 | мл/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, REG_ANIMALS_EMPTY, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 608 | Метрамаг® | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 610 | Метронид-Э | 15 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 615 | Тилодокс Р | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 618 | Килтикс® ошейник | — | мг/кг | 22.5 | нет | ошейник: надеть на животное, заменять по инструкции (1 раз в сутки) | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 619 | МИРТАЦЕН® | 0.5 | мг/кг | 1.88 | да | 0.5 мг/кг (1.88 мг/табл) ≈ 2.7 табл на 10кг. 1 раз в день | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 620 | Адвокат® кошки | 0.003 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 621 | Форесто® | 10 | мг/кг | 1250 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 623 | Фоксорал | — | мг/кг | 20 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 625 | Курс Успокоин таблетки | 3 | мг/кг | 28 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 626 | Адвантейдж® | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 627 | Адвантикс® | 50 | мг/кг | 500 | да | по инструкции: 0,1 мл/кг, пипетка по массе тела | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | EXTERNAL_NUMERIC |
| 628 | Дронтал® плюс | 15 | мг/кг | 504 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 629 | Байкокс® 5% | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 630 | БАРС® классик капли против блох и клещей | 6.7 | мг/кг | 10 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 631 | Больфо® ошейник | — | мг/кг | — | нет | ошейник: надеть на животное, заменять по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 633 | Профендер® | 5 | мг/кг | 85.75 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 635 | Байкокс® 2,5% | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 636 | Уролитин-С | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 637 | Дронтал® | 5 | мг/кг | 230 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 638 | Катозал® | 10 | мг/кг | 100 | нет | 2.5-5 мл в/м, п/к или в/в 1 р/сут 4-5 дней | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 656 | Кладакса® жевательные таблетки | 12.5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 657 | КОЛИФЛОКС® оральный | 7.5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 659 | Чеми спрей | — | мг/кг | 2000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 663 | Амино-Solvo | 0.1 | мл/кг | 72 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 669 | Спрей Фолайн® | 0.01 | мг/кг | 0.1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 677 | Марбовитрил 100 | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 678 | Дексодия | 0.015 | мг/кг | 0.1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 680 | Тетравет® L.A. | 10 | мг/кг | 200 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 681 | Ветримоксин L.A. | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 682 | Supramil® эмульсия | 0.5 | мг/кг | 2.5 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 683 | Инсектал шампунь | 6.7 | мг/кг | 1.04 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 687 | Мелоксидил® | 0.1 | мг/кг | 1.5 | да |  | ОТКРЫТЫЙ ВОПРОС | DB_ANIMALS_MISMATCH |
| 690 | ФИТОЭЛИТА® ЧИСТАЯ КОЖА | — | мг/кг | — | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 691 | ЦИПРОВЕТ® таблетки | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 693 | Кот Баюн® таблетки | — | мг/кг | — | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 694 | Ветопрофен | 1 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 695 | Празицид®-комплекс НЕО | 5 | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 696 | Чистотел ушные капли | 10 | мг/кг | 8.6 | да | капли в ухо: по инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 697 | ФИТОЭЛИТА® ЗДОРОВЫЕ ПОЧКИ | — | мг/кг | — | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 698 | Мелоксиприм | 0.2 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 702 | Аквидокс 750 | 10 | мг/кг | 750 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 704 | Эйметерм раствор 2,5% | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 707 | АСТЕРИОН DHPPiL | — | мг/кг | 1 | нет | 2.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 708 | АСТЕРИОН DHPPiLR | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 714 | Эпримек® | 0.5 | мг/кг | 10 | да | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 715 | Докситрон жевательные таблетки | 10 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 716 | Армаваб-2МЕ | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 724 | Окситетрациклина гидрохлорид для инъекций | 10 | мг/кг | 860 | нет |  | ОТКРЫТЫЙ ВОПРОС | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, DUPLICATE_NAME |
| 738 | МУЛЬТИКАН-6 | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 744 | РАБИКС | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 747 | ГИСКАН | — | мг/кг | 2 | нет | по инструкции (профилактика/лечение) | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 749 | ГЛОБКАН | — | мг/кг | 2 | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 751 | МУЛЬТИКАН-4 | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 753 | Фаговет | — | мг/кг | 1000 | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 754 | ДОКСИСТИМ К | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 757 | Марбоцин | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE |
| 762 | Иверсект ® | 0.006 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 764 | Мазь аверсектиновая® | 0.2 | мг/кг | 0.5 | да | По инструкции (наружное применение) | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 765 | Антибак 100 | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 770 | Экспресс Успокоин® таблетки | 3 | мг/кг | 24 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 774 | Мильпро® кэт | 5 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 775 | Мильпро® дог | 5 | мг/кг | 2.5 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 777 | Рабикан | — | мг/кг | 2 | нет | 5.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 778 | Вакцина против лептоспироза животных концентрированная масляная | — | мг/кг | 20 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 779 | Вакцина антирабическая инактивированная сухая культуральная из штамма "Щелково-51" | — | мг/кг | 10 | нет | 5.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 780 | ДИРОНЕТ® суспензия | 15 | мг/кг | 0.006 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 789 | Докситарт 500 | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 791 | ГАБИТАБС | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 793 | Антимедин® | 0.1 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 794 | Празицид®-суспензия НЕО | 15 | мг/кг | 15 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 796 | РольфКлуб 3D ушные капли | 5 | мг/кг | 11.2 | да | 3-5 капель в ухо | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 801 | Кетовет 100 | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 803 | Локсик 2% | 0.2 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 806 | Аверсект® К&С | 0.2 | мг/кг | 2 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 807 | Виметрил 100 | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 808 | Стоп-кокцид® 2,5% | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 817 | Амоксиянтарь 150 | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 822 | ЛАПУШКА шампунь инсектицидный для собак и кошек | 10 | мг/кг | 4.14 | да | шампунь: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 823 | Шиерия® | 2 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 824 | Сульф гранулы | 7.5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 825 | "Оралрабивак" | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 826 | Инсектал комбо С | 0.003 | мг/кг | 107.5 | да |  | ОТКРЫТЫЙ ВОПРОС | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 827 | ИРИС капли глазные | 3 | мг/кг | 4 | да | 1-2 капли в глаз | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 828 | УльтраСелл-Дог® | — | мг/кг | 0.4 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 829 | Аподерм | 15 | fixed | 21.5 | да | По инструкции (наружное применение) | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 830 | Шампунь VETЗАБОТА® с хлоргексидином 5% | 0.1 | мг/кг | 50 | да | по инструкции (наружно), 1 раз в сутки, курс 3-5 дней | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 833 | Неотерика Протекто таблетки | 0.025 | мг/кг | 7.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 840 | Польодоксин | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 843 | Антравак - СТИ жидкая | — | мг/кг | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 845 | Канинсулин | 0.5 | МЕ/кг | 40 МЕ/мл | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 854 | Цефтиосан® Форте | 2 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE |
| 856 | Энрофлоксацин 50 раствор для инъекций | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 858 | Окситетрациклин 200 LA | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 861 | Раствор йода спиртовой 5% | — | мг/кг | 5000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 864 | Туламицин-АВЗ | 2 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, INDICATION_NO_SPECIES, REG_CONTRADICTION, NO_OFFICIAL_SOURCE |
| 872 | Гельмимакс®-2 | 0.5 | мг/кг | 10 | нет | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 877 | Форцерис | 10 | мг/кг | 133.4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 880 | ДОКСИ АВЗ 500 | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 881 | БАРС® спрей инсектоакарицидный | 6.7 | мг/кг | 3 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 884 | Азилон® | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 887 | Курацеф Дуо | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 889 | Эймерал® 25 | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 890 | Алцефур® 50 | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 891 | Оксал® 200 ЛА | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 892 | ФИТОЭЛИТА® ЦИТОСТАТ | — | мг/кг | — | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 896 | Амоксилонг® 150 ЛА | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 897 | ФИТОЭЛИТА® МЕТАСТОП | — | мг/кг | — | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 900 | ЦИПРОВЕТ® гранулы | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 904 | Триметин | 15 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 905 | Антигрибковый и противоаллергический шампунь для животных | 10 | мг/кг | 0.1 | нет | По инструкции (наружное применение) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 908 | Триметин таблетки | 15 | мг/кг | 400 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 916 | Доксипрем 200 | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 917 | Дитрим® OR | 5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 919 | Ферран® | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 926 | Амоксоил Ретард | 15 | мг/кг | 150 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 927 | Флунивит | 1 | мг/кг | 83 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 930 | Хорулон | 0.02 | мг/кг | 1500 МЕ/мл | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 933 | Инсектал комбо К | 0.003 | мг/кг | 107.5 | да |  | ОТКРЫТЫЙ ВОПРОС | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC |
| 934 | Ветмедин® S | 0.25 | мг/кг | 1.25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 938 | Гепатолюкс PROtect суспензия | 1.5 | мг/кг | 15 | да | 2.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 941 | Фоллигон | — | МЕ/кг | 5000 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 942 | Элеовит | 0.2 | мг/кг | 0.2 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 944 | Таблетки тетрациклина | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 945 | Тетравитам | 300 | fixed | 0.15 | нет | 0.8 мл | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 946 | Чистотел Максимум спрей | 6.7 | мг/кг | 3.32 | да | спрей: наносить по инструкции, 1 раз в месяц, курс однократно | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 947 | Инспектор Мини | 0.025 | мг/кг | 5.2 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 948 | Гепатолюкс PROtect таблетки | 1.5 | мг/кг | 15 | да | 1-2 таблетки | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 949 | Марбофлоцин®10% | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 950 | ЦИПРОСТИМ 10% | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 952 | Вакцина против болезни Ауески инактивированная эмульгированная маркированная | — | мг/кг | 2 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 955 | Детокс | 0.1 | мл/кг | 50 | да | по инструкции: 1 мл/10 кг, внутривенно (медленно), подкожно | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 957 | БлохНэт® max | 0.5 | мг/кг | 1 | да | по инструкции (наружно), 1 раз в сутки, курс однократно | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 958 | Катобевит® | 5 | мг/кг | 100 | да | 5.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 959 | Топ Дог | 5 | мг/кг | 36 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 960 | Ферарабивак | — | мг/кг | 20 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 961 | Кардалис | 0.25 | мг/кг | 2.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 963 | Кетопроф | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 965 | Кайод таблетки | 5 | мг/кг | 3 | да | 5 мг/кг (3.0 мг/табл) ≈ 16.7 табл на 10кг. 1 раз в день | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 969 | Септо-спрей | — | мг/кг | 30 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 970 | Мазь ихтиоловая 10% | — | мг/кг | 10000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 972 | БАРС® ошейник инсектоакарицидный | 6.7 | мг/кг | 40 | да | ошейник: надеть на животное, заменять по инструкции (1 раз в месяц) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 974 | Веткокцин | 7.5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 975 | Амоксициллин 15% ЛА | 12.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 979 | Кантарен® раствор для перорального применения | — | мг/кг | — | нет | 2.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 980 | Габивит®-Se | 300 | fixed | 10 | да | 1.5 мл | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 982 | Бутастим | 2.75 | fixed | 100 | нет | 0,5-5 мл на животное | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 988 | Рабиген Моно | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 991 | Лиарсин раствор для перорального применения | — | мг/кг | — | нет | 2.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 994 | ДОКСИСТИМ 10% | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 995 | Инсектал ошейник | 6.7 | мг/кг | — | да | ошейник: надеть на животное, заменять по инструкции (1 раз в месяц) | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 997 | Кальфотон | 50 | мг/кг | 330 | да | 20.0 мл | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1003 | Гельминпраз | 0.006 | мг/кг | 30 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1004 | Празител® Особый суспензия | 5 | мг/кг | 1.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1007 | Репарин-Хелпер® | — | fixed | 0.05 | нет | наружно на повреждённый участок 1-2 раза в сутки | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1011 | Гельмимакс® | 0.5 | мг/кг | 20 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1012 | Сульфадокс | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1013 | Рабивак Vn-32/L | — | мг/кг | 1 | нет | 5.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1015 | Дана® Ультра спрей | 6.7 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1018 | Неомектин 1 % | 0.006 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1021 | Ветэприн | 0.5 | мг/кг | 5 | да | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1026 | Авертель | 5 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1027 | Анальгивет | 1 | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1028 | Аргумистин® 0,001% и 0,005% | — | мг/кг | 0.01 | нет | по инструкции (наружно), 2-3 раза в день, курс по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1030 | Аргумистин® раствор | — | мг/кг | 0.01 | нет | по инструкции (наружно), 2-3 раза в день, курс по инструкции | ОТКРЫТЫЙ ВОПРОС |  |
| 1031 | СЕКС БАРЬЕР® таблетки для кошек и сук | 2 | мг/кг | 0.1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1034 | Семинтра® 10 мг/мл | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1036 | ЦЕФТИСИЛ® гидро | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1037 | СексКонтроль спот-он | — | мг/кг | 24.75 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1038 | ЦЕФТИСИЛ® | 2 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1039 | ИВЕРСАН® | 0.006 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1040 | Гамавит | 0.5 | мл/кг | 0.02 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 1043 | ГЕНТАФЛОКС® инъекционный | 5 | мг/кг | 65 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1044 | Армаваб | — | мг/кг | 10 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1047 | Каниген® DHA2PPi/L | — | мг/кг | 1 | нет | 2.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1048 | Риботан | 0.1 | мл/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 1056 | Фиприст® Комбо | 6.7 | мг/кг | 120 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1057 | Ганаминовит | — | fixed | 0.1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1058 | Тиеркал | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1059 | Мультивит | 0.2 | мг/кг | 600 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1062 | Оксилонг® ретард | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1063 | Панкреалекс | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1065 | Ганамектин | 0.006 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1070 | Пенбекс | — | МЕ/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, ME_NO_ACTIVITY, NO_OFFICIAL_SOURCE |
| 1072 | Нобивак® КС | — | мг/кг | 0.5 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1073 | ЭМИЦИДИН® 2,5% раствор для инъекций | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1074 | Домитор® | 0.03 | мг/кг | 1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1075 | Фронтлайн Комбо | 6.7 | мг/кг | 100 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC |
| 1078 | Мильбецин Нео для кошек | 5 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1079 | Цефтонит® Форте | 2 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1086 | Бинакар Форте | 10 | мг/кг | 80 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1087 | Мильбецин Нео для собак | 5 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1090 | РольфКлуб 3D ошейник для кошек | 6.7 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1092 | Кокцидикс® | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1094 | Неодиар | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1095 | Нобивак® Puppy DP | — | мг/кг | 0.5 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1097 | Фронтлайн Спот Он | 6.7 | мг/кг | 50 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1099 | Фронтлайн Спрей | 6.7 | мг/кг | 250 | да | по инструкции: спрей, 3-6 мл/кг в зависимости от длины шерсти | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC |
| 1101 | Дексдомитор® | 0.01 | мг/кг | 0.1 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1103 | Неотерика Протекто сироп | 0.025 | мг/кг | 1.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1104 | Фоспренил | 0.1 | мг/кг | 4 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1105 | Анти-Фли спрей | 10 | мг/кг | 2 | да | спрей: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1106 | Максидин 0,4 | 0.15 | мг/кг | 4 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1107 | Максидин 0,15 | 0.15 | мг/кг | 1.5 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1110 | Нобивак® DHP | — | мг/кг | 0.5 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1112 | Доксициклин-комплекс | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1114 | ЧЕТЫРЕ С ХВОСТИКОМ® капли для регуляции половой охоты | 0.5 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1115 | ЭНРОСОЛ® 5% , 10% раствор для инъекций | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1119 | Левоксивет | 5 | мг/кг | 125 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1121 | Биоциллин-150 LA | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1123 | Нитамин | — | МЕ/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, ME_NO_ACTIVITY, NO_OFFICIAL_SOURCE |
| 1125 | Эвинтон® раствор для перорального применения | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1127 | Келапрофен | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1128 | Глистогон Плюс суспензия | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1129 | Инспектор ошейник | 6.7 | мг/кг | — | нет | ошейник: надеть на животное, заменять по инструкции (1 раз в месяц) | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1130 | Инспектор спрей | 6.7 | мг/кг | 3.46 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1131 | Антивир | 15 | мг/кг | 90 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1132 | Докси ВС 50 | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1136 | Нобивак® DHPPi | — | мг/кг | 0.5 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1138 | Ривициклин® А | 15 | мг/кг | 125 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1142 | РольфКлуб 3D спрей для собак | 6.7 | мг/кг | 3.3 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1148 | Иноксел | 2 | мг/кг | 60 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1150 | Террамицин Аэрозоль Спрей | 10 | мг/кг | 4000 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1151 | Неострепин™ 200/200 | 20 | МЕ/кг | 200000 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1154 | ДОКСИОР® 10% | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1156 | Антиседан® | 0.1 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1165 | Докси ВЛ 50 | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, INDICATION_NO_SPECIES, NO_OFFICIAL_SOURCE |
| 1166 | Гексидерм | 0.1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1167 | Фронтлайн НексгарД | 3 | мг/кг | 11.3 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1168 | Превикокс таблетки 57 мг и 227 мг | 5 | мг/кг | 57 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1175 | Куртикол® раствор для перорального применения | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1176 | ИН-АП комплекс® | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1180 | Празител® таблетки | 5 | мг/кг | 20 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1186 | Мекситар | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1191 | Стоморджил 2, 10, 20 | 15 | мг/кг | 25 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1193 | Карнивак-Ков | — | мг/кг | 1 | нет | 5.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1198 | Биопротектин® | — | мг/кг | — | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1199 | Бродлайн Спот-Он | 5 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1201 | Селафорт® | 6 | мг/кг | 60 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1205 | Нефроантитокс | 0.75 | мл/кг | 80 | да | по инструкции (с кормом) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 1211 | Витаминно-аминокислотный комплекс "ВИТАМ" | — | мг/кг | 1000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1212 | Вермидин® таблетки | 5 | мг/кг | 15 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1213 | Празител® суспензия | 5 | мг/кг | 3 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1214 | Эурикан DHPPI2-L | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1215 | Нозевир | 15 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1217 | Алезан крем для суставов | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1218 | Апоквел | 0.5 | мг/кг | 3.6 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1219 | СЕКС БАРЬЕР® капли для собак | — | мг/кг | 2 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1222 | Форвет® капли глазные 0,004% | 50 | мг/кг | 0.04 | да | 1-2 капли в глаз | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1240 | Тилдокс АВЗ | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, INDICATION_NO_SPECIES, NO_OFFICIAL_SOURCE |
| 1243 | Шампунь противомикробный с хлоргексидином 4 % | — | мг/кг | 40 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1244 | Энроколи инъекционный | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1246 | Рабизин | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1248 | Докси-фуд® | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1252 | 4Хувс | — | мг/кг | 24.12 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1256 | Анти-тикс | 6.7 | мг/кг | 85 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1260 | ДИРОНЕТ® джуниор | 5 | мг/кг | 15 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1262 | Арбимектин | 0.075 | мг/кг | 0.75 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1263 | Санакард шампунь | 6.7 | мг/кг | 2 | да | шампунь: наносить по инструкции, 1 раз в месяц, курс однократно | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1264 | Празивер® | 0.006 | мг/кг | 5 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1267 | Догферон® раствор для инъекций | 0.8 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1268 | Санакард | 9 | мг/кг | 90 | нет | по инструкции (наружно), 1 раз в сутки, курс однократно | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1269 | Шампунь хлоргексидиновый с антибактериальным эффектом для животных | 0.1 | мг/кг | 50 | да | шампунь: наносить по инструкции, 1 раз в сутки, курс 3-5 дней | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1271 | ВитОкей® | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1279 | Гельминтал Мини сироп | 7.5 | мг/кг | 18 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1280 | Х-ГИА | — | мг/кг | 950 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1281 | Эурикан Primo | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1291 | Гептролюкс таблетки | 0.1 | мл/кг | 66.5 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 1292 | Диаркан | 50 | мг/кг | 300 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1293 | Эурикан DHPPI2-LR | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1294 | Поливеркан | 50 | мг/кг | 200 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1295 | Дана® Ультра | 10 | мг/кг | 50 | да | по инструкции (наружно), 1 раз в сутки, курс однократно | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1296 | Дана® Спот-он | 6.7 | мг/кг | 50 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1297 | ВЕТАЛЬГИН® | 3.5 | fixed | 2 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1299 | Фортекор® | 0.25 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1300 | Прак-тик® | 6 | мг/кг | 500 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в 4-6 недель | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1302 | БлохНэт® спрей | 0.5 | мг/кг | 1 | да | спрей: наносить по инструкции, 1 раз в сутки, курс однократно | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1305 | Мазь "Ям БК"® | 0.05 | мг/кг | 10000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1307 | Дипентавак | — | мг/кг | 1.5 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1308 | Вакдерм-F | — | мг/кг | 3 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1310 | Гексаканивак | — | мг/кг | 1 | нет | 2.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1311 | Празицид® таблетки | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1312 | Вакдерм | — | мг/кг | 3 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1313 | Дирофен® таблетки | 15 | мг/кг | 120 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1314 | Декта®-2 | 3 | мг/кг | 5 | да | 1-2 капли в глаз | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1315 | Офтальмосан® | 0.01 | мг/кг | 1 | да | капли в глаз: по инструкции, 2-3 раза в день, курс 3 дня | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1318 | Энрофлокс 10% инъекционный | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1319 | Фунгин® Форте | 0.1 | мг/кг | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1320 | Плацента денатурированная эмульгированная (ПДЭ) | — | мг/кг | 250 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1322 | АНАНДИН® 10% раствор для инъекций | 2 | мг/кг | 100 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1323 | АНАНДИН® плюс капли ушные | 0.05 | мг/кг | 0.5 | да | капли в ухо: по инструкции, 1 раз в сутки | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1324 | КАРДАНОН® | 0.1 | мл/кг | 125 | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1325 | Зоосорб® | 1 | мл/кг | 920 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 1326 | АНАНДИН® капли ушные | 2 | мг/кг | 20 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1328 | Стоп-интим® капли | 2 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1329 | Амоксисан | 12.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1332 | АНАНДИН® капли глазные и интраназальные | 2 | мг/кг | 20 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1334 | Стоп-стресс® таблетки 2 и 5 | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1337 | Фелиферон® раствор для инъекций | 1 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1340 | Экзекан | 75 | fixed | 1 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1345 | Дезацид | — | fixed | 1 | нет | 1-2 капли в глаз/нос | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1346 | БАРС® форте капли для кошек против блох и клещей | 6.7 | мг/кг | 10 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1347 | Атакса® | 0.1 | мг/кг | 500 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1349 | Ципрон | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1350 | Пиро-Стоп® | 3 | мг/кг | 120 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1351 | БлохНэт® Форте | 6.7 | мг/кг | 75 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1353 | Нобивак® Lepto | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1355 | Ципроген | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1359 | Декта® Форте | 0.5 | мг/кг | 50 | да | по инструкции (наружно), 1 раз в сутки, курс однократно | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1360 | РольфКлуб 3D ошейник для собак | 6.7 | мг/кг | — | да | ошейник: надеть на животное, заменять по инструкции (1 раз в месяц) | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1362 | РольфКлуб 3D спрей для кошек | 6.7 | мг/кг | 3.3 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1363 | Фенпраз суспензия | 5 | мг/кг | 6 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1365 | Гельминтал сироп | 0.025 | мг/кг | 0.3 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1366 | Доксициклин 20% | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1367 | Нитокс® Форте | 10 | мг/кг | 340 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1368 | Чистотел Плюс ошейник | — | мг/кг | 65 | нет | ошейник: надеть на животное, заменять по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1370 | Фенпраз таблетки | 5 | мг/кг | 75 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1372 | Доксилокс® WS | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1374 | Отоксолан® | 0.2 | мг/кг | 3 | нет | капли в ухо: по инструкции, 1 раз в день, курс 2-4 недели | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1375 | Маропиталь | 2 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1376 | Кетопрофен 10% | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1377 | Бравекто® | 25 | мг/кг | 112.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1379 | Неофлокс таблетки | 5 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1381 | OKVET® Шампунь профилактический с хлоргексидином | 0.1 | мг/кг | 1 | да | шампунь: наносить по инструкции, 1 раз в сутки, курс 3-5 дней | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1387 | Кетоджект® | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1388 | Флуниджект® | 1 | мг/кг | 83 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1391 | АРРИАХ-Рабивак | — | мг/кг | 1 | нет | 5.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1394 | Микродерм | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1395 | Инспектор Квадро Табс | 10 | мг/кг | 20 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1398 | Празител®  плюс суспензия | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1400 | Амоксилонг™ 150 LA | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1402 | Цималджекс | 2 | мг/кг | 8 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1403 | Фронтлайн Три-Акт | 6.7 | мг/кг | 67.6 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1406 | Оксицивен LA 200 | 10 | мг/кг | 200 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1410 | Глистогон суспензия | 5 | мг/кг | 10 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1413 | Отидез® | — | fixed | 0.3 | нет | 3-5 капель в каждое ухо | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1414 | Тетраспазвит | 0.2 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1415 | Окситоцин | — | fixed | 10 МЕ/мл | нет | 5-10 МЕ (0,5-1 мл) на животное в/м | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1417 | Линдокс | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1419 | Празител® плюс таблетки | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1420 | Раствор Рингера-Локка | 0.15 | мл/кг | 9 | да |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, ML_PER_KG_ON, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1422 | Аквадокс | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1423 | Инспектор ушные капли | 25 | мг/кг | 0.11 | нет | 3-5 капель в ухо | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1427 | Дана® Ультра ошейник инсектоакарицидный | 0.006 | мг/кг | 40 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1428 | Капли ушные Отоферонол Голд | 6 | ме/кг | 1 | нет | капли в ухо: по инструкции, 1-2 раза в день, курс 3-5 дней | ТРЕБУЕТ ИСТОЧНИКА | ME_NO_ACTIVITY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1429 | Капли ушные Отоферонол® | — | мг/кг | 4 | нет | 3-5 капель в ухо | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1430 | Капли глазные Лакрикан | 2.5 | fixed | 2 | нет | 1-2 капли в глаз | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1431 | Зоодерм® | 7.5 | мг/кг | 200 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1432 | Капли ушные Отоферонол Плюс | 6 | ме/кг | 0.5 | нет | капли в ухо: по инструкции | ТРЕБУЕТ ИСТОЧНИКА | ME_NO_ACTIVITY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1433 | Полисептин® | 2 | мг/кг | 50 | да | по инструкции: 2-4 мг/кг, внутрь | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1434 | Амитразин® | — | мг/кг | 25 | нет | наружно spot-on: пипетка по массе тела по инструкции, 1 раз | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1435 | Отоферонол Премиум | 0.1 | мг/кг | 20 | да | капли в ухо: по инструкции | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1436 | Клиодезив | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1437 | КОЛИФЛОКС® инъекционный | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1439 | Нобивак® L4 | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1440 | Празицид®-суспензия Плюс | 15 | мг/кг | 45 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1441 | Медитин® | 0.03 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1442 | Стоп-зуд® суспензия | 2 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1444 | Гентам® | 2.4 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1445 | Неомек | 0.006 | мг/кг | 10 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1446 | Стоп-кокцид® | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1447 | Дана® шампунь | 6.7 | мг/кг | 5 | да | шампунь: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1448 | Вазосан® | 0.1 | мг/кг | 1.25 | да | 0.25 мг/кг (1.25 мг/табл) ≈ 2 табл на 10кг. 1 раз в день | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1450 | Лакто-Стоп® | 0.005 | мг/кг | 0.05 | да | 0.005 мг/кг (0.05 мг/табл) ≈ 1 табл на 10кг. однократно | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1451 | Раносан® порошок | 25 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1452 | Стоп-зуд® спрей | 25 | мг/кг | 0.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1453 | Цефтиосан® | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1454 | Дирофен®-суспензия 20 и 60 | 5 | мг/кг | 15 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1455 | Раносан® мазь | 2 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1456 | Гепатоджект® | — | мг/кг | 40 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1457 | Сульфетрисан® | 0.1 | мг/кг | 0.1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1458 | Дирофен® -паста 20 и 60 | 5 | мг/кг | 15 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1460 | Виттри-3 | 0.05 | мл/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 1462 | АПСАМИКС ОКСИТЕТРАЦИКЛИН 20% | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1465 | Чистотел пудра | 10 | fixed | 4 | да | пудра: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1466 | Неотерика Протекто 4 | 10 | мг/кг | 94.6 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1467 | Чистотел глистогон | 5 | мг/кг | 25 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1468 | Суролан | 2.3 | мг/кг | 23 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1469 | Чистотел Максимум шампунь | 10 | мг/кг | 4.24 | да | шампунь: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1470 | Инсектал капли | 6.7 | мг/кг | 99 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1471 | РольфКлуб ошейник антипаразитарный | 0.006 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1472 | РольфКлуб 3D капли для кошек | 6.7 | мг/кг | 101 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1473 | Чистотел зоошампунь | 10 | мг/кг | 4.2 | да | шампунь: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1475 | Чистотел Максимум капли | 6.7 | мг/кг | 47.5 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1477 | Гельминтал С | 0.1 | мл/кг | 25 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1478 | РольфКлуб 3D капли для собак | 6.7 | мг/кг | 101 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1479 | Секс-контроль С | 2 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1484 | Цитодерм капли ушные комплексные | 5 | мг/кг | 0.11 | нет | 3-5 капель в ухо | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1485 | РольфКлуб 3D шампунь | 1.89 | мг/кг | 2.1 | да | по инструкции (наружно), 1 раз в сутки, курс ежемесячно | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1486 | Чистотел Максимум ошейник | 6.7 | мг/кг | — | да | ошейник: надеть на животное, заменять по инструкции (1 раз в месяц) | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1487 | Инсектин шампунь инсектицидный | 10 | мг/кг | 5.2 | да | шампунь: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1488 | Гельминтал Т | 0.025 | мг/кг | 0.4 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1490 | Чистотел зооспрей | 10 | мг/кг | 3 | да | спрей: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1492 | Инспектор Квадро К | 5 | мг/кг | 10.7 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1493 | Цитодерм капли ушные противогрибковые+ | 5 | мг/кг | 1.11 | да | 3-5 капель в ухо | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1494 | Цитодерм® капли ушные антибактериальные | 5 | мг/кг | 1.11 | да | 3-5 капель в ухо | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1495 | Инспектор Квадро С | 6.7 | мг/кг | 21.4 | нет | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1496 | Настойка полыни | — | мг/кг | 20000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1498 | Оксибактоцид® пластины | 10 | мг/кг | 30 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1500 | Оксибактоцид® порошок | 10 | мг/кг | 800 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1506 | Кетоквин®  1%, 10% | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1510 | Эйметерм суспензия 5% | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1511 | Вазотоп Р | 0.1 | мг/кг | 0.625 | да | 0.25 мг/кг (0.625 мг/табл) ≈ 4 табл на 10кг. 1 раз в день | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1514 | Толфедин® 4% | 2 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1515 | АМОКСИСТИМ 15% | 12.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1518 | Милпразон® таблетки для кошек | 5 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1519 | Милпразон® таблетки для собак | 5 | мг/кг | 2.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1522 | Макродокс 200® | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1523 | Капли Фолайн® | 0.01 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1524 | Дитрим® порошок | 5 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1525 | Диазинон-С | — | мг/кг | 60000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1529 | ЭКС®-5, ЭКС®-7,5 | 0.5 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1538 | Куртикол® | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1548 | Амоксигард® | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1556 | Кот Баюн® настой | — | мг/кг | — | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1558 | Марфлоксин® 10% раствор для инъекций | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1559 | Марфлоксин® таблетки | 2 | мг/кг | 5 | да | 2 мг/кг (5.0 мг/табл) ≈ 4 табл на 10кг. 1 раз в день | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1560 | Нобивак® RL | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1565 | Оридэрмил® | 20 | мг/кг | 10 | нет | капли в ухо: по инструкции | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1568 | Пропалин® | 2 | мг/кг | 50 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1569 | Ауризон® | 2 | мг/кг | 3 | нет | капли в ухо: по инструкции, 2 раза в день, курс 2-4 недели | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1570 | Азоксивет® | 0.5 | мг/кг | 1.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1571 | Веракол® раствор для перорального применения | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1575 | Триспазвит | 750 | fixed | — | нет | дозирование на животное по инструкции (комплексный состав) | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1576 | Доксилокс® ОR | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1577 | Кофеин-бензоат натрия 20% раствор для инъекций | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1582 | Оптиммун® | 5 | мг/кг | 2 | да | 1 см полоски мази за нижнее веко | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1585 | Амоксициллин 15% LA | 12.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1586 | ШУСТРИК® поливитамины | 0.2 | мг/кг | 220 МЕ/мл | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1587 | Доксициклин 200 | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1588 | Мексидол-Вет® | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1589 | Мексидол-Вет® | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1590 | Биопирокс спрей | — | мг/кг | 1000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, NO_OFFICIAL_SOURCE |
| 1591 | ЧЕТЫРЕ С ХВОСТИКОМ® таблетки | 0.5 | мг/кг | 5 | да | 2 мг/кг (5.0 мг/табл) ≈ 4 табл на 10кг. по схеме | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1593 | Ветмедин® | 0.25 | мг/кг | 1.25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1594 | ФЕБТАЛ® таблетки | 50 | мг/кг | 150 | да | 50 мг/кг (150.0 мг/табл) ≈ 3.3 табл на 10кг. 1 раз в день, 3 дня | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1595 | ЭКС®-5Т, ЭКС®-20Т | 0.5 | мг/кг | 5 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1596 | Соладокси® 500 | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1598 | Бутофан® | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1600 | Микросал | 50 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_SPECIES_MISSING, ZERO_CONC_WITH_DOSE, NO_OFFICIAL_SOURCE |
| 1606 | Антибак 250 | 5 | мг/кг | 250 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1607 | ЦИПРОВЕТ® 10% | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1610 | Ноземат® | 10 | мг/кг | 400 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1613 | Оксивит® порошок | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1615 | Оксивит® полоски | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1616 | ЭМИЦИДИН® капсулы | 10 | мг/кг | 15 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1617 | Энрофлон® 2,5%, 5% и 10% раствор для инъекций | 5 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1618 | Флексопрофен® 2,5%, 5% и 10% | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1619 | Флексиэктив® | — | мг/кг | 250 | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1622 | Ивертин | 0.006 | мг/кг | 10 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1623 | Фортикарб® 5% и 10% раствор для инъекций | 6 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1624 | МИГСТИМ® | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1632 | Линковик | 15 | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1635 | Тиоцефур® | 2 | мг/кг | 50 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH |
| 1636 | Долинк | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1637 | Тиланик 5% и 20% раствор для инъекций | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1639 | Эмидонол 20% | 3.5 | мг/кг | 200 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1640 | Квантум | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1641 | Гентамицин 4% и 5% раствор для инъекций | 4 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1643 | ДИРОНЕТ® таблетки | 15 | мг/кг | 150 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1644 | Мизоксин® | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1645 | Вектра 3D® | 10 | мг/кг | 54 | да | по инструкции препарата: схема применения указана в инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1649 | Фенбенгран® | 50 | мг/кг | 222 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1654 | Тиациклин® | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1656 | Сультеприм® | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1661 | Пульмокит® | 7.5 | мг/кг | 30 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, INDICATION_NO_SPECIES, NO_OFFICIAL_SOURCE |
| 1664 | Отибиовин | 3 | мг/кг | 2 | да | 3-5 капель в ухо | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1665 | Хондартрон® раствор для перорального применения | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1666 | Ветбензицин-5 | 25000 | МЕ/кг | 1.2e+06 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1668 | ФЕБТАЛ® гранулы | 50 | мг/кг | 222 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1669 | ДЕЛЬЦИД® | 6 | ме/кг | 40 | нет | по инструкции (наружно), курс 3-7 дней | ТРЕБУЕТ ИСТОЧНИКА | ME_NO_ACTIVITY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1670 | Конвения | 8 | мг/кг | 852 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1671 | Гепасейф® | 10 | мг/кг | 12 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1673 | Римадил Р | 4 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1675 | Терраветин-500 | 10 | мг/кг | 500 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING |
| 1676 | Касептурин® | — | мг/кг | 500 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1677 | Димцип® | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1682 | Вангард 7 | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1683 | ПЕДИЛАЙН ХУФКЕА | — | мг/кг | 17.72 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1684 | Кальция борглюконат | 0.75 | мл/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, ML_PER_KG_ON, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1685 | Мазь тетрациклиновая 3% | 10 | мг/кг | 3000 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1686 | Мазь Яхалимп® | — | мг/кг | 10000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1687 | Гликосан® | — | мг/кг | 3000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1689 | Мазь ихтиоловая 10% и 20% | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1690 | Мазь серная простая | — | мг/кг | 33000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1691 | Мазь цинковая | 10 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1692 | Ивермек® | 0.006 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1695 | Мазь Экзеконт | 2 | мг/кг | 5000 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1696 | Серения | 2 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1697 | Альбамелин® | 25 | мг/кг | 100 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | REG_ANIMALS_EMPTY |
| 1698 | Синулокс | 12.5 | мг/кг | 12.5 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1701 | Эксенел стерильный порошок | 2 | мг/кг | 60 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1704 | Дексафорт | 0.2 | мг/кг | 3 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, REG_ANIMALS_INCOMPLETE, NO_OFFICIAL_SOURCE |
| 1709 | Йод однохлористый | — | мг/кг | 3000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1710 | РЕПТИЛАЙФ® суспензия | 5 | мг/кг | 25 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1711 | Римадил 5% раствор для инъекций | 4 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1712 | Креолин-Х® | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1713 | Биорекс-ГХ® | 10 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1716 | Креолин бесфенольный каменноугольный® | 12.5 | мг/кг | 100 | да | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1717 | Кламоксил LA | 12.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1723 | Линимент синтомицина 1%, 5%, 10% | 50 | мг/кг | 10000 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1724 | Ковинавет | 0.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1728 | Трококсил | 2 | мг/кг | 6 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1729 | Энроксил® 5% раствор для инъекций | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1733 | Синулокс RTU | 12.5 | мг/кг | 140 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1734 | Наксел | 2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1735 | Эксид | 2 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1738 | Пихтоин® | — | мг/кг | 20000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1739 | Вакцина антирабическая инактивированная культуральная жидкая (ВНИИЗЖ) | — | мг/кг | 1 | нет | 5.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1741 | Зоошампунь инсектицидный Луговой | 6 | ме/кг | 0.1 | нет | шампунь: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | ME_NO_ACTIVITY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1742 | Стронгхолд | 6 | мг/кг | 60 | да |  | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1746 | Вирусвакцина против чумы мелких жвачных культуральная сухая | — | мг/кг | 2 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1747 | Веторил | 3 | мг/кг | 10 | да | По инструкции (дозировка в таблетках, зависит от веса) | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1749 | Ветмедин® | 0.25 | мг/кг | 0.75 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1751 | Амоксициллин 150 | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1752 | Монизен | 0.006 | мг/кг | 40 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1754 | Мазь салициловая 2%, 5%, 10% | 25 | мг/кг | 2000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1758 | Ронколейкин® | 10000 | МЕ/кг | 50000 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1760 | Симпарика | 2 | мг/кг | 120 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1764 | Натрия нуклеинат | 2 | мг/кг | 2 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1767 | Пигфен® 40 | 50 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1770 | ЦИПРОВЕТ® 5% для инъекций | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1780 | Панакур® Паста | 50 | мг/кг | 187.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1782 | Имозимаза | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1783 | Мазь стрептоцидовая | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1786 | Мазь серно-дегтярная | — | мг/кг | 5000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1788 | РАДОСТИН® Витасил | 0.05 | мл/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 1793 | Хелсивит | 1 | мг/кг | 50 | да | 3.5 мл | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1794 | Эффитикс® | 6.7 | мг/кг | 61 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1798 | Сыворотка "Витакан-С" | — | мг/кг | 3 | нет | по инструкции (профилактика/лечение) | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1799 | Террамицин LA | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1800 | Глобулин "Витакан" | — | мг/кг | 3 | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1801 | Лобелон® | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1804 | Гидродокс® 50% | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1807 | Зитрококс | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1809 | Азитронит® М | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1810 | Гидродокс® 10% оральный раствор | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1811 | Гидродокс® 10% | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1812 | Иммунофан® | — | мг/кг | 0.05 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1813 | АпКард | 0.2 | мг/кг | 0.75 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1814 | Клавасептин | 12.5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1816 | Азинокс® ветеринарный | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1817 | Дефенсор-3 | — | мг/кг | 1 | нет | 5.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1818 | ФИТЭКС® капли успокаивающие | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1819 | Семинтра® | 1 | мг/кг | 4 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1821 | Сафродерм гель | — | мг/кг | 100 | нет | по инструкции (наружно), 1–2 раза в сутки, курс по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1824 | Петкам | 0.1 | мг/кг | 0.5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1825 | Сафродерм настойка | — | мг/кг | — | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1829 | Дехинел® таблетки для кошек | 5 | мг/кг | 230 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1834 | Липотон 500 | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1837 | Ассоциированная вакцина против болезни Ауески и болезни Тешена инактивированная эмульгированная | — | мг/кг | 4 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1844 | Мазь стрептоцидовая 10% | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1845 | Мазь цинковая 10% | 10 | мг/кг | 10000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1847 | Цемай | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1850 | Виттри-1 | 0.05 | мл/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ML_PER_KG_ON, ZERO_CONC_WITH_DOSE, NO_OFFICIAL_SOURCE |
| 1852 | Пексион® | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1853 | Кетомай | 1 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1854 | Кафорсен® раствор для перорального применения | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1858 | Доксмай | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1859 | Деликс шампунь инсектицидный | 10 | мг/кг | 3.5 | да | шампунь: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1860 | ВИТАМЭЛАМ | 0.1 | мл/кг | 0.1 | да | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 1861 | Мазь ихтиоловая 10% | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1863 | Деликс ошейник инсектоакарицидный | 10 | мг/кг | — | да | ошейник: надеть на животное, заменять по инструкции | ТРЕБУЕТ ИСТОЧНИКА | ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1864 | Деликс капли инсектоакарицидные | 10 | мг/кг | 50 | да | капли: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1865 | Владикан | — | мг/кг | 5 | нет | по инструкции (профилактика/лечение) | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1866 | Цефтонит® | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1868 | Актионис | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1869 | Деликс спрей инсектоакарицидный | 10 | мг/кг | 3 | да | спрей: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1870 | Шампунь инсектицидный для кошек Мисс Кисс | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1871 | Капли инсектоакарицидные для кошек Мисс Кисс | 6.7 | мг/кг | 110 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1872 | Капли ушные Барс® форте | 5 | мг/кг | 20 | да | 3-5 капель в ухо | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1877 | Спрей инсектоакарицидный Мистер Бруно Плюс - Интенсивная защита/ Мисс Кисс - Интенсивная защита | 6.7 | мг/кг | 3 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1878 | Спрей инсектоакарицидный Мистер Бруно Плюс - Бережная защита/  Мисс Кисс - Бережная защита | 6.7 | мг/кг | 1 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1880 | Иммуновет 3Ин | — | мг/кг | 2 | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1881 | Иммуновет 3Сн | — | мг/кг | 2 | нет | по инструкции (профилактика/лечение) | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1887 | Фебтал®-комбо | 5 | мг/кг | 5 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1889 | Метакам® | 0.2 | мг/кг | 20 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1891 | Капли инсектоакарицидные БАРС® форте | 6.7 | мг/кг | 50 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1895 | Фармазин® 50 и 200 | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1897 | Капли инсектоакарицидные Мистер Бруно Плюс - Интенсивная защита | 6.7 | мг/кг | 110 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1904 | Капли инсектоакарицидные Мистер Бруно Экстра | — | мг/кг | 270 | нет | по инструкции (наружно), 1 раз в месяц, курс ежемесячно | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 1905 | AD3Евит раствор для перорального применения | 0.2 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1906 | Гентаприм | 4 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1907 | Комплекс витаминов А, D3, Е в масле | 0.05 | мл/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 1908 | Зоомикол® | 7.5 | мг/кг | 677 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1909 | Фортиклин Ретард | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1911 | Шампунь инсектицидный Мистер Бруно для собак | 10 | мг/кг | 500 | да | шампунь: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1914 | Ошейник инсектоакарицидный Мистер Бруно для собак | 10 | мг/кг | 100 | да | ошейник: надеть на животное, заменять по инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1919 | СПОРОВИТ (сухой) | — | мг/кг | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1921 | Диронет® спот-он | 0.5 | мг/кг | 85 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1922 | СПОРОВИТ (жидкий) | — | мг/кг | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1924 | Ализин® | 10 | мг/кг | 30 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 1927 | Беафар ошейник инсектоакарицидный для собак | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1929 | Беафар ошейник инсектоакарицидный для кошек | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1932 | Нитамин OR | 0.2 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1936 | Неозидин® М | — | мг/кг | 57.5 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1939 | Вакцина поливалентная "ВГНКИ" против лептоспироза животных | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1941 | Фитодок®-Иммуностим | 12.5 | мг/кг | — | да | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | ZERO_CONC_WITH_DOSE, NO_OFFICIAL_SOURCE |
| 1942 | Альфакаин 2%+адреналин | 2 | мг/кг | 20 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1943 | Фитодок®-Нефроспас | 12.5 | мг/кг | — | да | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | ZERO_CONC_WITH_DOSE, NO_OFFICIAL_SOURCE |
| 1944 | Мазь ихтиоловая 10% и 20% | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1946 | Бензилпенициллина натриевая соль для инъекций | 25000 | МЕ/кг | 1e+06 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1947 | Стрептомицина сульфат для инъекций | — | мг/кг | 1000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1948 | Экофлис | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1949 | Неомицина сульфат | 10 | мг/кг | 1000 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_DOSE_MISMATCH, DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1950 | Доксипрекс | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1955 | Деликс-Ф капли инсектоакарицидные | 6.7 | мг/кг | 80 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 1957 | Неозидин® | — | мг/кг | 450 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1958 | Неуротранк | 0.05 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1959 | Гликопин® | — | мг/кг | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1960 | Травма-гель | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1962 | Стрептопен 20/20 | 25000 | МЕ/кг | 200000 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1963 | Доксикел 75 | 10 | мг/кг | 750 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1964 | Амоксициллин 20% LA | 15 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1966 | Прокпен 30 | 25000 | МЕ/кг | 300000 МЕ/мл | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1967 | Канамицин 25% | — | мг/кг | 250 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1970 | Тривитамин (раствор витаминов А, Д3, Е в масле) | 0.1 | мл/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 1972 | Альфамек | 0.006 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1974 | Окситетрациклин 20% LA | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1975 | Линкомицин+спектиномицин 5/10 | 15 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1976 | Метронид 50 | 15 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1977 | Докси-500 WS | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 1978 | Фуросемид 5% | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1979 | Лиарсин | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1982 | Мазь ихтиоловая 10% | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 1986 | Раствор гентамицина сульфата 4% | 4 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1987 | Тетрацилин | — | мг/кг | 40000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1991 | Мазь "Левомеколь-вет" | 50 | мг/кг | 750 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 1992 | Ксилазин 2% | 1 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1996 | Кофеин-бензоат натрия 20% | 0.1 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 1998 | Кальция борглюконат | 0.75 | мл/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, ML_PER_KG_ON, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 2002 | Тетраметр | 10 | мг/кг | 1000 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2005 | Дексаметазон 2 мг/см³ | 0.1 | мг/кг | 2 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2007 | Диастоп | 10 | мг/кг | 1 | да |  | ПОДТВЕРЖДЕНО/ИСПРАВЛЕНО | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING |
| 2008 | Диоксинор оральный раствор | 10 | мг/кг | 90 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2010 | Диоксинор | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2012 | Разбавитель для вакцины Вермет против дерматофитозов животных | — | мг/кг | 5 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2015 | Кальфосет® | 50 | мг/кг | 820 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2016 | Е-селен® | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2017 | Е-селен® OR | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2019 | Хондартрон®-гель | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2020 | Глюкортин-20 | 0.1 | мг/кг | 2 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2022 | Уролекс капли урологические | — | мг/кг | 25 | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2024 | Энтомозан®-С | 10 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2026 | Супервитасол | 2.5e-06 | мг/кг | 1e+06 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2027 | Витаминоацид | 75 | мг/кг | 400 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2028 | Доксилокс® | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2030 | Стрептомицина сульфат | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2032 | Бабезан 4% и 12% раствор для инъекций | 6 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2035 | Дехинел® Плюс | 15 | мг/кг | 525 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2037 | Дехинел ® Плюс таблетки со вкусом мяса | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 2038 | Тиамокс | 10 | мг/кг | 250 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2041 | Нороклав инъекционный | 12.5 | мг/кг | 140 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, NO_OFFICIAL_SOURCE |
| 2042 | Ивермек®-гель | 0.1 | мг/кг | 15 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2043 | Клинексин 5% | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2044 | Норокарп таблетки | 4 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2047 | Ивермек®-спрей | — | мг/кг | 2.5 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2048 | Авидокс | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2050 | Эгоцин® 20 порошок | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2053 | Доксигор 10% | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2055 | Мазь фармайодная® антисептическая | — | мг/кг | 5 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2056 | Тривитамин А, Д3, Е для инъекций (раствор витаминов А, Д3, Е в масле) | 0.05 | мл/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 2057 | Тривитамин А, Д3, Е для орального применения (раствор витаминов Тривитамин А, Д3, Е в масле) | 0.05 | мл/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ML_PER_KG_ON, NO_OFFICIAL_SOURCE |
| 2058 | Фиприст® Спот Он | 6.7 | мг/кг | 100 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2059 | Каридокс | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2060 | Тетрагидровит | — | МЕ/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, ME_NO_ACTIVITY, NO_OFFICIAL_SOURCE |
| 2061 | Тетравит (комплекс витаминов А, D3, Е, F в масле) | — | МЕ/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, ME_NO_ACTIVITY, NO_OFFICIAL_SOURCE |
| 2062 | Фенилбутазон | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2063 | Энровек 5% и 10% | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 2064 | Канигард спот он | 10 | мг/кг | 400 | да | наружно spot-on: пипетка по массе тела по инструкции | ТРЕБУЕТ ИСТОЧНИКА | EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2068 | Амоксивек-форте | 12.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 2069 | Энроксил® Макс | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2070 | Форвет® | — | мг/кг | 0.04 | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2071 | Гентамицина сульфат 4% раствор для инъекций | 4 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2075 | Вакцина ПОЛИВАК-ТМ | — | мг/кг | 0.5 | нет | 2.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2076 | Фоспасим® раствор для перорального применения | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2078 | Тилозин 50 и Тилозин 200 | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2079 | Дитрим® | 5 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2081 | Гексадог | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2082 | Эфикур | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2083 | Рикарфа® таблетки со вкусом мяса | 4 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2084 | Ализерил WS | 10 | мг/кг | 35 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2085 | Толтарокс® | 10 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2087 | Амоксициллин 15% | 12.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 2090 | Мазь Левомеколь | 50 | мг/кг | 750 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2093 | Энромокс® | 5 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2094 | Антиовод | — | мг/кг | 12 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2098 | Веракол® | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2101 | Хондартрон® | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2102 | Геомицин® Ф | 10 | мг/кг | 1000 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2105 | Лучший друг гельмистоп | 50 | мг/кг | 250 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2106 | Лучший друг вермистоп | 5 | мг/кг | 45 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2108 | Мазь тетрациклиновая глазная 1% | 10 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2110 | Нитокс® 200 | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2113 | Бальзам ДОРОГОВОЙ® | — | мг/кг | 20 | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2114 | Гентамицина сульфат 4% | 4 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2115 | Кантарен® | — | мг/кг | — | нет | 2.0 мл | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, NO_OFFICIAL_SOURCE |
| 2116 | Травматин® | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2118 | Бактил 5% инъекционный | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 2120 | Эндотил-форте | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2121 | Мастометрин® | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2122 | Овариовит | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, NO_OFFICIAL_SOURCE |
| 2124 | Фоспасим® | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2126 | Кафорсен® | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2128 | Гентамицина раствор 4% | 4 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2129 | Ипакитине | 1 | мг/кг | — | да | по инструкции (с кормом) | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, ZERO_CONC_WITH_DOSE, NO_OFFICIAL_SOURCE |
| 2130 | Ковертал | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2133 | Ксиланит® | 1 | мг/кг | 20 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2134 | Сарколитин® К-9 | 0.2 | мг/кг | 0.6 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2136 | Зооксилазин | 1 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 2137 | Микодемоцид | — | мг/кг | 12 | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2138 | Гемобаланс | 5 | мг/кг | 1 | нет | 0.25-1 мл по массе (<5 кг: 0.25; 5-15: 0.5; >15: 1), 2-3 р/нед | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2140 | Каниген® DHA2PPi/LR | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2142 | Кубатол® Пикс Аэрозоль | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2143 | Амоксициллин инъекционный | 12.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 2145 | Энронит® | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2148 | Присыпка Эдис | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2152 | Эпацид-альфа | 10 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2159 | Отибиовет | 3 | мг/кг | 40 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2160 | Иноксел RTU | 2 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2161 | Окситетрациклин ЛА | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2172 | Мультивек | 0.0325 | мг/кг | — | нет | дозирование на животное по инструкции (комплексный состав) | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2179 | Вакцина против хламидиоза животных "ХламидиоВак" | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2180 | Эльвита-Удивит | 0.1 | мл/кг | — | нет | дозирование на животное по инструкции (комплексный состав) | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2181 | АД3EF | — | fixed | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2183 | АД3Евит | 7.75 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2189 | Докси Форте | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2191 | Бимоксил LA | 12.5 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 2196 | Электро-Декс | 0.15 | мл/кг | — | нет | дозирование на животное по инструкции (комплексный состав) | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2201 | Скавон Вет Крем | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2203 | Феникс | 25 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2204 | Легафитон 50, 200 | — | мг/кг | 50 | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2205 | Ошейник инсектоакарицидный Беафар для собак и кошек С.О.С. | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2208 | Гонасил | 0.001 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2213 | Фебрин Порцино | 10 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, ZERO_CONC_WITH_DOSE, NO_OFFICIAL_SOURCE |
| 2214 | Бивермектин | 0.006 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2222 | 30%-ный раствор глицерина для разбавления вакцин против сибирской язвы животных | — | мг/кг | 300 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2223 | Досалид | 5 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, ZERO_CONC_WITH_DOSE, NO_OFFICIAL_SOURCE |
| 2225 | Тромексин | 5 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, ZERO_CONC_WITH_DOSE, NO_OFFICIAL_SOURCE |
| 2227 | Квинокол 10 | 5 | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2228 | Фипрекс спрей форте | 6.7 | мг/кг | — | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2231 | Айнил 1% | 1 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 2232 | Биокан® LR | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2233 | Фипрекс 75 спот-он | 6.7 | мг/кг | 75 | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2236 | Биокан® Puppy | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2237 | Серения таблетки | 2 | мг/кг | 16 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2239 | Линкоспектин | 15 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, NO_OFFICIAL_SOURCE |
| 2240 | Геставет-GnRH | 0.001 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2244 | Мизофен® | 7.5 | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2249 | Дюфалайт | 0.075 | мл/кг | — | нет | до 50 мл на 5 кг массы в/в медленно | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2256 | Окситетра 50% W.S. | 10 | мг/кг | 500 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2259 | Линимент синтомицина 5% | 50 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2265 | Золетил 50 и 100 | 5 | мг/кг | 50 | да |  | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2266 | Нуклеопептид | 0.1 | мл/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2267 | Энтероспорин | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2269 | Дюрамун Макс 5/4L | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2270 | Амит форте | 6.7 | мг/кг | — | да | наружно spot-on: пипетка по массе тела по инструкции, 1 раз в месяц | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2271 | Интерспектин-L | 15 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2272 | Вангард 5/L | — | мг/кг | — | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2273 | Дюрамун Макс 5-CvK/4L | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2275 | Зинаприм | 5 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_DOSE_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 2276 | Лигфол | 0.1 | мг/кг | 6 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2282 | Мазь цинковая 10% | 10 | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 2285 | Окситетрациклин 100 | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2286 | Вирусвакцина для оральной  иммунизации диких плотоядных животных против бешенства "Синраб" | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2288 | Монклавит-1 | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2289 | Ципам | 10 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2290 | Инсектицидный шампунь Беафар | 10 | мг/кг | — | да | шампунь: наносить по инструкции | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2294 | Квинокол Плюс | 5 | мг/кг | 65 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2298 | Тетралонг-20 | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2299 | Ошейник против блох и клещей ДокторZOO | — | мг/кг | 15 | нет | ошейник: надеть на животное, заменять по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2302 | Настойка березовых почек | — | мг/кг | 90 | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2303 | Настойка боярышника | — | мг/кг | 65 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2305 | Настойка перца стручкового | — | мг/кг | 65 | нет | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2308 | Экстракт прополиса спиртовый | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2309 | Мазь прополисная | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2310 | Водная суспензия прополиса | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2321 | Витафлеш Амино WSP | 0.1 | мг/кг | 30 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2324 | Нео-Окси WSP | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2325 | Мультивитамин инъекции | — | мг/кг | 3 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2327 | Кепроцерил WSP | 10 | мг/кг | 30 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2328 | Лимоксин-200 LA | 10 | мг/кг | 200 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2329 | Ошейник антипаразитарный Мультикс | 0.006 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2331 | Ветбицин-5 | 25000 | МЕ/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, ME_NO_ACTIVITY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2333 | Ветбицин-3 | 25000 | МЕ/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, ME_NO_ACTIVITY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2337 | Лимоксин-25 спрей | 10 | мг/кг | 25 | да |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2338 | Окситетрациклина гидрохлорид для инъекций | 10 | мг/кг | 100 | нет |  | ОТКРЫТЫЙ ВОПРОС | DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, CALC_OFF_DOSE, DUPLICATE_NAME |
| 2339 | Ксила | 1 | мг/кг | 20 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2340 | Стрептомицина сульфат для инъекций | — | мг/кг | 1000 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 2341 | Мазь ихтиоловая 10% и 20% | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
| 2343 | Докси-10 | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2347 | Тетравит (раствор витаминов А, Д3, Е, F в масле для инъекций) | — | мг/кг | 3 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2351 | Алюспрей | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2352 | Вакцина против ящура универсальная сорбированная моно- и поливалентная (из вируса, выращенного в клетках ВНК-21) | — | мг/кг | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2356 | ПЕЦИВЕТ | 10 | мг/кг | 100 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2357 | Ранозоль | — | мг/кг | 0.31 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2359 | Абивертин® | 0.2 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2360 | Декор | 1.5 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, ZERO_CONC_WITH_DOSE, EXTERNAL_NUMERIC, NO_OFFICIAL_SOURCE |
| 2362 | Амитан | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2364 | Диазинон-Евровет | — | мг/кг | 60 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2367 | Галастоп | 0.005 | мг/кг | 0.05 | да | 0,1 мл (3 капли) на 1 кг массы внутрь, 4-6 дней | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2378 | Ферроцин | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2379 | Бифеж | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2380 | Гентамокс | 15 | мг/кг | 150 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2384 | Мазь Анандин | — | мг/кг | 100 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2386 | Стоп-стресс капли | 10 | мг/кг | 100 | да | по инструкции | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2387 | Шустрик суспензия | 5 | мг/кг | 50 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | REG_ANIMALS_EMPTY, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2388 | Антибак ПРО | 5 | мг/кг | — | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, REG_SPECIES_MISSING, ZERO_CONC_WITH_DOSE, NO_OFFICIAL_SOURCE |
| 2389 | Новомек | 0.006 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2391 | Септифорт спрей | — | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | GHOST_SPECIES, DB_CONC_MISMATCH, REG_ANIMALS_EMPTY, NO_OFFICIAL_SOURCE |
| 2394 | Дермацин инъекционный | 0.006 | мг/кг | 10 | да |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, NO_OFFICIAL_SOURCE |
| 2395 | Отодектин | 0.006 | мг/кг | 1 | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_ANIMALS_MISMATCH, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2397 | Амит | — | мг/кг | 2.5 | нет | наружно spot-on: пипетка по массе тела по инструкции, 1 раз | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2398 | Биокан® DHPPi+L | — | мг/кг | 1 | нет | 2.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2399 | Биокан® DHPPi+LR | — | мг/кг | 1 | нет | 1.0 мл | ТРЕБУЕТ ИСТОЧНИКА | NO_OFFICIAL_SOURCE |
| 2400 | Витамин А ацетат 1000 | 0.2 | мг/кг | — | нет |  | ТРЕБУЕТ ИСТОЧНИКА | DB_CONC_MISMATCH, DB_ANIMALS_MISMATCH, REG_SPECIES_MISSING, CALC_OFF_DOSE, NO_OFFICIAL_SOURCE |
| 2401 | Настойка чемерицы | — | мг/кг | — | нет | по инструкции препарата | ТРЕБУЕТ ИСТОЧНИКА | DB_FREQ_MISMATCH, DB_ANIMALS_MISMATCH, REG_ANIMALS_EMPTY, DUPLICATE_NAME, NO_OFFICIAL_SOURCE |
