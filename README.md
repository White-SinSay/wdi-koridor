### АВТОМАТИЧЕСКОЕ ВЫКЛЮЧЕНИЕ И КОНТРОЛЬ ТЕМПЕРАТУР 3Д ПРИНТЕРА или ИНЫХ УСТРОЙСТВ
Независимое устройство для отключения 3д принтеров и CNC по температуре и другим событиям.
Работает через <a href="https://blynk.io/">BLYNK</a>.
Устройство для сборки на платформе ESP8266, подойдут платы NodeMCU или Wemos D1 mini.
Скетч подготовлен для VSCode, при желании можно работать с ним и в ARDUINO IDE, поменяв расширение main.cpp на .ino и загрузив указанные в platformio.ini библиотеки (чего в VSCode делать не нужно).

### ВОЗМОЖНОСТИ УСТРОЙСТВА:
* Контроль температуры и вывод в приложение на смартфон.
* Push-уведомления, когда температура поднимается выше указанных в скетче пороговых значений.
* Автоматическое отключение устройства при превышении установленных пороговых значений (иных от уведомлений)
* Автоматическое отключение с задержкой по времени, если температура не поднимается или достигает заданного предела, по истечении указанной задержки нагрузка будет отключена
* Принудительное отключение из приложения по желанию.
* Возможна работа до 6 датчиков температуры и различной логикой работы по ним (в том числе режимы нагрева или охлаждения) с добавлением дополнительных реле

### ПЛАНИРУЕТСЯ:
* Добавить зуммер либо изменение логики на какой-либо пин для оповещения состояний
* Добавить возможность подключения датчика филамента. Уведомление в приложении при срабатывании.
* Сборка устройства на готовой заводской плате с нормальными разъемами для датчиков
* Перевод на работу с MQTT для интеграции с платформами автоматизации
* Другое (учту ваши пожелания и предложения).

### СПИСОК ЖЕЛЕЗА:
* Wemos D1 mini: http://alli.pub/5mdxgv ИЛИ NodeMCU V3 и шилды к нему: http://ali.pub/3zoiql РЕЛЕ
* Активные модули реле: http://alli.pub/5mdxnv
* ИЛИ подойдет релейный модуль для Wemos: http://alli.pub/5mdxk6
* ИЛИ Твердотельное реле: http://alli.pub/5mdzqj
* Модули питания 220-12/5/3.3 в: http://alli.pub/5mdxsx
* ИЛИ (лучше) DC-DC преобразователь без ШИМ: http://alli.pub/5mdzo0
* DC-DC с ШИМом: http://alli.pub/5me018 Кнопка 220в: http://alli.pub/5mg55w http://alli.pub/5mg59z
* Разъемы KF141 (зеленые, планируется разводить плату с ними): http://alli.pub/5mdwp9
* Термистор: Термисторы 5шт: http://got.by/45wjbz
* Датчики Dallas (нормальные): http://alli.pub/5mdx8i
* Комплект сопротивлений 0,25Вт от 1Ом до 1МОм: http://ali.pub/3zp04i
* Печатная плата: http://alli.pub/5mlqm3

### ПОЛЕЗНОЕ НАЧИНАЮЩИМ
* Макетная плата: http://got.by/442q43
* Перемычки для сборки на макетке: http://got.by/442pbw  http://got.by/442pqo  http://got.by/442qfr
* Компактный тестер Richmeters 102: http://ali.pub/3zozp5
* USB паяльник: http://ali.pub/3zoldv
* Паяльник 12-24 SH72: http://alli.pub/5mg4b6
* Очиститель жала: http://ali.pub/3zomzf
* Отличный припой: http://ali.pub/3zoq47
* Флюс-гель для пайки SMD-компонентов: http://ali.pub/3zp64x
* Термоклей: http://got.by/4jvb0y
* Набор клемм: http://got.by/45wgqn
* Термоусадочные трубки, набор: http://got.by/4bhwuc

### КАК СОБРАТЬ
* На монтажной плате подходящего размера, навесной монтаж, элементов не так много, пайка
* ВНИМАНИЕ! Выводы контактов реле подключаются в разрыв N или L 3д принтера ПОСЛЕ предохранителя.
* Пример сборки, какое железо нужно купить и подробно об устройстве и его настройке в видео: 

### СХЕМА
![Схема](https://github.com/Technarrus/3d_print_control/blob/master/scheme.jpg)

### КАК НАСТРОИТЬ
Пользуясь преимуществами библиотеки 1-Wire для цифровых датчиков задействован только один пин, для возможности подключения дополнительных реле и перефирии.
Минут столько в том, что нужно предварительно указать адрес подключаемых датчиков в скетче. Найти адрес можно с помощью этого скетча- <a href="https://github.com/Technarrus/Dallas_Adress">Dallas Adress</a>, как - на странице подробно расписано.
Далее нужно откалибровать показания термистора, путем изменения #define REFERENCE_RESISTANCE, что бы температура была более менее равна показаниям далласов.

 
### РЕЛИЗЫ
Сюда будут добавляться старые версии

### ВИДЕО

* <a href="https://youtu.be/zlENMWZuub8"> Видео про данный проект</a>
* <a href="https://www.youtube.com/channel/UCzI016x7MItBtQCJiSWI7yA">Канал YouTube</a>
* <a href=" ">-</a>

### Связь
Вопросы, обсуждения, предложения через следующие сообщества:
* [Telegram группа](https://t.me/technarr)
* [Группа в VK](https://vk.com/technarrus)
