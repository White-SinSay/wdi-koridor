### DIY контролер для умного дома
Данный контролер был разработан под мои нуждны. Но я решил поделиться наработками. Вдруг комуто будет полездно
Данный контролер на базе ESP32, прошика ESPHome, расчитан для интеграции в Home Assistant


### ВОЗМОЖНОСТИ УСТРОЙСТВА:
* Управление RGB (или 3 незасисемых одноцветных канала) лентой.
* Подключение до 4 датчиков движения.
* Подключение датчика температуры и влажности
* Подключение 2 кнопок или герконов
* Подключение DFplayer mini (для воспроизведения mp3 с флешки).


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

### Внешний вид платы
![Схема](https://github.com/White-SinSay/wdi-koridor/blob/main/images/PCB_UP.png)
![Схема](https://github.com/White-SinSay/wdi-koridor/blob/main/images/PCB_down.png)
### 3D вид
![Схема](https://github.com/White-SinSay/wdi-koridor/blob/main/images/PCB_3D.png)
### СХЕМА
![Схема](https://github.com/White-SinSay/wdi-koridor/blob/main/images/Schematic.png)

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
