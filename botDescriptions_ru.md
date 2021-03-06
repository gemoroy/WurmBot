# Типы ботов

## ar - ArcherBot
Автоматически стреляет по указанной цели текущим экипированным луком. Если тетива рвется,
пытается натянуть новую. Отключается автоматически после уничтожения указанной цели.

### Команды:
1) s [threshold] - Значение Stamina, ниже которого бот начнет отдыхать. Дробное число от 0 до 1.
2) string - натянуть новую тетиву.

## a - AssistantBot
Помогает игроку во многих аспектах.

### Команды:
1) w - Переключает автоматическое употребление указанной жидкости
2) wid [id] - Переключает автоматическое употребление жидкости с указанным идентификатором
3) ls - Показывает список заклинаний, доступных для автокаста
4) c [spell] - Переключает автокаст заклинаний, при условии что у игрока хватает маны. Список доступных заклинаний доступен по команде ls
5) p [milliseconds] - Переключает автоматические молитвы с заданным интервалом
6) pid [id] - Переключает автоматические молитвы на алтаре с указанным идентификатором
7) s - Переключает автоматические пожертвования. Интервал между пожертвованиями задается отдельно командой st
8) st [milliseconds] - Устанавливает время в миллисекундах между пожертвованиями
9) sid [id] - Переключает автоматические пожертвования на алтаре с указанным идентификатором
10) kb - Переключает автоматическое использование растопки из инвентаря. Растопка будет собираться и сжигаться в указанной печи
11) kbt [milliseconds] - Устанавливает интервал между сжиганием растопки
12) kbid [id] - Переключает автоматическое сжигание растопки в печи с указанным идентификатором
13) cwov - Переключает автокаст Wisdom of Vynora
14) cleanup - Переключает автоматическую очистку свалки. Интервал задается отдельно командой cleanupt
15) cleanupt [milliseconds] - Устанавливает интервал между очисткой свалки
16) cleanupid [id] - Переключает автоматическую очистку свалки с указанным идентификатором
17) l - Переключает автоматический взлом замков. Курсор должен указывать на взламываемый сундук
18) lt [milliseconds] - Устанавливает интервал между взломом замка
19) lid [id] - Переключает автоматический взлом замка на сундуке с указанным идентификатором
20) v - Переключает режим вывода расширенных сообщений о работе бота

## big - BulkItemGetterBot
Перекладывает предметы в инвентарь игрока из указанных _bulk storages_
n-ый предмет источник будет перемещен в n-ый контейнер приемник

### Команды:
1) as - Установить источником предмет, хранящийся в bulk storage, на который указывает курсор
2) at - Установить приемником предмет, на который указывает курсор
3) asid [id] - Установить источником предмет, хранящийся в bulk storage, по его идентификатору
4) atid [id] - Установить приемником предмет по идентификатору
5) ssxy - Установить источником предмет по координатам курсора мыши на экране

## ch - ChopperBot
Рубит поваленные деревья рядом с игроком.

### Команды:
1) s [threshold] - Значение Stamina, ниже которого бот начнет отдыхать. Дробное число от 0 до 1.
2) d [distance] - Расстояние в метрах от игрока, на котором бот ищет поваленные деревья.
3) c [amount] - Количество ударов по поваленному дереву за цикл.
4) area [tiles_ahead] [tiles_to_the_right] - Переключает обрабатываемую область. Указывается размер области в тайлах перед игроком и справа от него.
5) area_speed [speed] - Устанавливает скорость движения. По умолчанию 1.

## c - CrafterBot
Изготавливает предметы, указанные в окне крафта. Новые действия не начинаются, пока не очистится очередь. Данное поведение может быть отключено.

### Команды:
1) r - Автоматически ремонтировать предмет в левой части окна крафта (обычно это инструмент) по достижении им 10% повреждений.
2) st [target_name] - Задать имя предмета, который будет ингредиентом. Бот будет помещать указанные предметы из инвентаря в правую часть окна крафта.
3) stxy - Задать предмет, который будет ингредиентом, по координатам курсора мыши на экране. Бот будет помещать указанные предметы из инвентаря в правую часть окна крафта.
4) ss [source_name] - Задать имя предмета, который будет инструментом. Бот будет помещать указанные предметы из инвентаря в левую часть окна крафта.
5) ssid [id] - Задать предмет, который будет инструментом, по идентификатору.
6) ssxy - Задать предмет, который будет инструментом, по координатам курсора мыши на экране. Бот будет помещать указанные предметы из инвентаря в левую часть окна крафта.
7) nosort - Переключить сортировку предметов. По умолчанию сортировка включена.
8) cs - Объединять предметы в левой части окна крафта.
9) ct - Объединять предметы в правой части окна крафта.
10) ctimeout [milliseconds] - Установить интервал объединения предметов.
11) s [threshold] - Значение Stamina, ниже которого бот начнет отдыхать. Дробное число от 0 до 1.
12) u - Переключает режим, в котором бот будет помещать в правую часть окна крафта предметы, указанные в начале списка требуемых.
13) an [number] - Задать количество действий, выполняемых при каждом нажатии кнопки Continue/Create.
14) noan - Переключает проверку очереди перед следующим действием. Если проверка включена, бот будет выполнять следующее действие только если очередь пуста.
15) s1s - Переключает режим, при котором в слот инструмента будет помещаться только 1 предмет.

## fp - FlowerPlanterBot
Прокачивает навык Gardening, сажая и собирая цветы с окружающих тайлов. Для работы нужны цветы в инвентаре.

### Команды:
1) s [stamina] - Значение Stamina, ниже которого бот начнет отдыхать. Дробное число от 0 до 1.

## i - ImproverBot
Улучшает выбранные предметы в указанных инвентарях используя инструменты из инвентаря игрока. Предметы вроде воды или камня выбираются перед каждый улучшением, в том время как инструменты выбираются единожды перед улучшением первого предмета с помощью этого инструмента. Инструмент определяется по иконке, которую можно видеть справа от самого предмета в инвентаре. У некоторых инструментов (например, Stone Chisel и Carving Knife) иконки могут совпадать, из-за чего бот может выбрать не тот инструмент. В таких ситуациях надо воспользоваться командой -ci чтобы сменить инструмент.

### Команды:
1) s [threshold] - Значение Stamina, ниже которого бот начнет отдыхать. Дробное число от 0 до 1.
2) at - Использовать инвентарь под курсором. Выделенные предметы из этого инвентаря будут улучшаться.
3) ls - Список доступных для улучшения навыков и их сокращения.
4) ss [skill_abbreviation] - Установить используемый для улучшения навык, в дальнейшем будут использованы только относящиеся к нему инструменты. Для просмотра полного перечня навыков используйте команду ls.
5) g - Переключить режим, в котором будут улучшаться выбранные предметы на земле. Перед включением необходимо выбрать навык с помощью команды ss.
6) ci - Заменить ранее выбранный инструмент на указанный в инвентаре игрока.

## fsm - ForageStuffMoverBot
Перемещает предметы, собираемые с помощью фуража или травничества, из инвентаря игрока в указанный инвентарь. Перемещение камней и редких предметов можно переключить.

### Команды:
1) at - Целевой инвентарь или контейнер, в который будут перекладываться предметы.
2) r - Переключить перекладывание редких предметов.
3) mr - Переключить перекладывание камней.

## fr - ForesterBot
Собирает и сажает саженцы, подрезает деревья/кусты и собирает урожай в области 3х3 вокруг игрока. Бот может быть настроен для обработки прямоугольной площади любого размера. Саженцы, во избежание переполнения инвентаря, будут выкладываться в контейнер, которым по умолчанию является Backpack. Контейнер должен быть в корне инвентаря. Так же могут быть указаны дополнительные предметы, перекладываемые в контейнер (например, собранные фрукты). Тайла типа степь (steppe) и тундра (moss) будут обрабатываться если посадка растений разрешена и у игрока есть лопата в инвентаре.

### Команды:
1) s [threshold] - Значение Stamina, ниже которого бот начнет отдыхать. Дробное число от 0 до 1.
2) ca - Переключить срезание саженцев со всех деревьев.
3) cs - Переключить вырубку высохших (shriveled) деревьев.
4) df - Переключить вырубку всех деревьев.
5) h - Переключить сбор урожая.
6) p - Переключить посадку саженцев.
7) scn [container_name] - Задать новое имя контейнера для складывания урожая.
8) na [number] - Установить количество действий, выполняемых ботом подряд.
9) aim [item_name] - Добавить новый предмет для перемещения в контейнер.
10) area [tiles_ahead] [tiles_to_the_right] - Переключает обрабатываемую область. Указывается размер области в тайлах перед игроком и справа от него.
11) area_speed [speed] - Устанавливает скорость движения. По умолчанию 1.

## fg - ForagerBot
Занимается фуражом, травничеством, сбором травы и цветов в области вокруг игрока. Бот может быть настроен для обработки прямоугольной области любого размера. Собираемые предметы, для предотвращения переполнения инвентаря, будут складываться в контейнеры, имя которых может быть настроено. По умолчанию используется контейнер "backpack". Используемый контейнер должен быть расположен в корневом каталоге инвентаря (не должен входить в группу или быть внутри другого контейнера). Бот может быть настроен для сброса собираемых предметов на землю.

### Команды:
1) s [threshold] - Значение Stamina, ниже которого бот начнет отдыхать. Дробное число от 0 до 1.
2) g - Переключить сбор травы.
3) f - Переключить фураж.
4) ftl - Показать список типов фуража и их сокращений.
5) ft [type] - Установить тип фуража.
6) b - Переключить травничество.
7) btl - Показать список типов травничества.
8) bt - Установить тип травничества.
9) d - Переключить сброс собираемых предметов на землю.
10) v - Переключить режим вывода расширенных сообщений для вывода дополнительной информации о работе бота.
11) scn [container_name] - Установить новое имя для контейнера, в который буду складываться ростки (sprouts) и урожай.
12) na [number] - Установить количество действий, выполняемых ботом подряд.
13) area [tiles_ahead] [tiles_to_the_right] - Переключить обрабатываемую область. Указывается размер области в тайлах перед игроком и справа от него.
14) area_speed [speed] - Установить скорость движения. По умолчанию 1.

## gig - GroundItemGetterBot
Подбирает с земли вокруг игрока предметы из списка.

### Команды
1) d [distance] - Установить расстояние (в метрах, 1 тайл = 4 метра), на котором бот будет искать предметы.
2) a [item_name] - Добавить в список имя подбираемого предмета.

## g - GuardBot
Отслеживает сообщения в закладках Event и Combat. Если в течение заданного времени нет никаких сообщений - поднимает тревогу. Реагирует на сообщения, содержащие указанные ключевые слова. Если таковых нет, то реагирует на все сообщения.

### Команды
1) at [timeout] - Установить таймер (в миллисекундах), по истечении которого поднимается тревога.
2) a [keyword] - Добавить ключевое слово.
3) cs [path] - Установить путь к .wav-файлу со звуком тревоги.
4) soundtest - Проиграть звук тревоги.

## im - ItemMoverBot
Перемещает предметы из инвентаря в указанное место назначения.

### Команды
1) st - Установить место назначения (под курсором мыши). Предметы из инвентаря будут перемещены в этот предмет, если он является контейнером, или рядос с ним если нет.
2) stid [id] - Установить идентификатор места назначения. Предметы из инвентаря будут перемещены в этот предмет, если он является контейнером, или рядос с ним если нет.
3) str - Установить целевой контейнер (под курсором мыши). Предметы из инвентаря будут помещены в корневой каталог этого контейнера.
4) stcn [number] - Установить количество, которое требуется переместить в каждый контейнер. Используется с командой "stc".
6) stc [container_name] - Установить целевой контейнер (под курсором мыши) с другими контейнерами внутри. Предметы из инвентаря буду перемещены в эти вложенные контейнеры. Бот будет пытаться положить по 100 предметов в каждый из них, но это количество может быть изменено командой "stcn".
7) sw [weight] - Установить максимальный вес перемещаемых предметов. Действует только на последнее указанное имя предмета.
8) a [name] - Добавить имя предмета к списку перемещаемых. Максимальный вес этого предмета может быть установлен командой "sw".
9) r - Переключить перемещение редких предметов. Отключено по умолчанию.
10) fl - Переключить перемещение предметов только из корневого каталога инвентаря. Предметы, расположенные в группе или внутри контейнера, затронуты не будут. Включено по умолчанию.

## m - MinerBot
Добывает горные породы и плавит руду.

### Команды
1) s [threshold] - Значение Stamina, ниже которого бот начнет отдыхать. Дробное число от 0 до 1.
2) c [amount] - Установить количество действий, выполняемых ботом подряд. По умолчанию 3.
3) sc - Переключить объединение осколков (shard), лежащих в кучах вокруг игрока.
4) scn [name] - Установить имя комбинируемых осколков. Используется с командой "sc".
5) fixed - Установить режим работы с фиксированным тайлом. Бот запомнит его и будет работать только с ним.
6) st - Установить ражим работы с текущим выбранным тайлом.
7) area - Установить режим работы с тайлами, окружающими игрока в области 3х3.
8) ft - Установить режим работы, в котором бот будет добывать тайл перед игроком.
9) o - Переключить добычу руды. Включено по умолчанию.
10) m - Переключить автоматическое движение вперед, если в текущем тайле больше нечего делать.
11) sm - Переключить переплавку руды из указанной кучи.
12) at [min_quality] - Установить цель (под курсором мыши) для переплавленной руды не ниже указанного качества (0-100).
13) ati [min_quality] - Установить целевой инвентарь (под курсором мыши) для переплавленной руды не ниже указанного качества (0-100).
14) atid [id] [min_quality] - Установить цель (по идентификатору) для переплавленной руды не ниже указанного качества (0-100).
15) sp - Установить кучу с рудой (под курсором мыши) для переплавки.
16) ssm - Установить плавильню (под курсором мыши) для переплавки руды.
17) sft [timeout] - Установить периодичность заправки плавильни горючим (в миллисекундах).
18) sfn [name] - Установить имя топлива для плавильни.
19) v - Переключает режим вывода расширенных сообщений о работе бота.

## md - MeditationBot
Медитирует на коврике. Предполагается, что нет никаких ограничений в навыке медитации.

### Команды
1) s [threshold] - Значение Stamina, ниже которого бот начнет отдыхать. Дробное число от 0 до 1.
2) c [amount] - Установить количество действий, выполняемых ботом подряд. По умолчанию 3.
3) rt [timeout] - Установить период починки коврика (в миллисекундах).

## h - HealingBot
Перевязывает раны хлопком из инвентаря.

### Команды
1) md [min_damage] - Установить минимальный урон раны, который будет обрабатываться.

## f - FarmerBot
Ухаживает за полями, сажает семена, обрабатывает землю, собирает урожай.

### Команды
1) s [threshold] - Значение Stamina, ниже которого бот начнет отдыхать. Дробное число от 0 до 1.
2) r - Переключает ремонт инструментов.
3) ft - Переключить прополку (tending).
4) h - Переключить сбор урожая (harvesting).
5) p [seeds_name] - Переключить посадку семян с указанным наименование.
6) c - Переключить вспахивание поля (cultivation).
7) and [name] - Добавить предмет с указанным наименованием к списку выбрасываемых. Используется с командой "d".
8) d - Переключить выбрасывание собранных предметов на землю. Имена выбрасываемых предметов добавляются командой "and".
9) dl [number] - Установить лимит сохраняемых предметов.
10) area [tiles_ahead] [tiles_to_the_right] - Переключить обрабатываемую область. Указывается размер области в тайлах перед игроком и справа от него.
11) area_speed [speed] - Установить скорость движения. По умолчанию 1.

## d - DiggerBot
Копает землю, песок, глину и прочее в том же духе.

### Команды
1) s [threshold] - Значение Stamina, ниже которого бот начнет отдыхать. Дробное число от 0 до 1.
2) d [height] - Установить абсолютную высоту угла, до которой необходимо копать.
3) dtile [height] - Установить абсолютную высоту всех углов текущего тайла, до которой необходимо копать.
4) dtp - Переключить складывание выкопанной земли в кучу. По умолчанию включено.
2) c [amount] - Установить количество действий, выполняемых ботом подряд. По умолчанию 3.
6) l - Переключить выравнивание выбранного тайла.
7) la [height] - Переключить выравнивание области вокруг игрока до указанной высоты.
8) tr - Переключить ремонт инструментов.
9) sm - Переключить поверхностную добычу (mining). Работает только по области с командой "area".
10) area [tiles_ahead] [tiles_to_the_right] - Переключить обрабатываемую область. Указывается размер области в тайлах перед игроком и справа от него.
11) area_speed [speed] - Установить скорость движения. По умолчанию 1.

## pc - PileCollector
Собирает предметы из куч в контейнеры.

### Команды
1) stn [name] - Установить имя собираемых предметов. По умолчанию "dirt".
2) st [name] - Установить контейнер, в который будут собираться предметы. По умолчанию "large crate".
3) stcc [capacity] - Установить вместимость контейнера. По умолчанию 300.

## fsh - FisherBot
Ловит и разделывает рыбу.

### Команды
2) r - Переключает ремонт инструментов.
2) line - Переключить установку новой лески.

## pr - ProspectorBot
Исследует выбранный тайл.

### Команды
1) s [threshold] - Значение Stamina, ниже которого бот начнет отдыхать. Дробное число от 0 до 1.
2) c [amount] - Установить количество действий, выполняемых ботом подряд. По умолчанию 3.
