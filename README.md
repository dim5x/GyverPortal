[![latest](https://img.shields.io/github/v/release/GyverLibs/GyverPortal.svg?color=brightgreen)](https://github.com/GyverLibs/GyverPortal/releases/latest/download/GyverPortal.zip)
[![Foo](https://img.shields.io/badge/Website-AlexGyver.ru-blue.svg?style=flat-square)](https://alexgyver.ru/)
[![Foo](https://img.shields.io/badge/%E2%82%BD$%E2%82%AC%20%D0%9D%D0%B0%20%D0%BF%D0%B8%D0%B2%D0%BE-%D1%81%20%D1%80%D1%8B%D0%B1%D0%BA%D0%BE%D0%B9-orange.svg?style=flat-square)](https://alexgyver.ru/support_alex/)
[![Foo](https://img.shields.io/badge/README-ENGLISH-blueviolet.svg?style=flat-square)](https://github-com.translate.goog/GyverLibs/GyverPortal?_x_tr_sl=ru&_x_tr_tl=en)

[![Foo](https://img.shields.io/badge/ПОДПИСАТЬСЯ-НА%20ОБНОВЛЕНИЯ-brightgreen.svg?style=social&logo=telegram&color=blue)](https://t.me/GyverLibs)

# GyverPortal
### v3.6 (12.03.2023)
Простой конструктор веб интерфейсов для ESP8266 и ESP32
![img](/docs/feature.png)

## Совместимость
> ### ЕСЛИ НЕ КОМПИЛИТСЯ НА ESP32 - ОБНОВИ ЯДРО, УЖЕ ПОРА. ДА, [ВОТ НА ЭТО](https://github.com/espressif/arduino-esp32)
- esp8266 (SDK v2.7+)
- esp32 (SDK v2+)

## Документация
Теперь находится в [Wiki репозитория](https://github.com/GyverLibs/GyverPortal/wiki). Документация на данный момент неполная, на стадии написания!
> [English docs](https://github-com.translate.goog/GyverLibs/GyverPortal/wiki?_x_tr_sl=ru&_x_tr_tl=en)

## Идеи/проблемы/актуальная версия
- Рабочую версию (нестабильную/экспериментальную/ночную) можно скачать [из репозитория](https://github.com/GyverLibs/GyverPortal/archive/refs/heads/main.zip)
- Изменения в следующей версии читать/предлагать в issue https://github.com/GyverLibs/GyverPortal/issues/58
- Также можно [обсудить на форуме](https://community.alexgyver.ru/threads/gyverportal.6632/)

### Известные баги
Некоторые элементы могут некрасиво отображаться на Firefox, т.к. сделаны под Chrome, Safari, Edge, Opera

## Возможности
![demo](/docs/GyverPortal.jpg)  

Универсальный конструктор веб интерфейсов для ESP8266 и ESP32:
- Позволяет быстро создать вебморду для управления и настройки электронного девайса
- Работает на базе стандартных библиотек esp, ничего дополнительно устанавливать не нужно
- Создание многостраничных и динамических веб-интерфейсов в несколько строк кода прямо в скетче
- Не требует знания HTML, CSS и JavaScript: все стили и скрипты уже заложены в библиотеке
- Написано на чистом HTML + CSS + JS, никаких сторонних веб-библиотек
- Не требует подключения к Интернет
- Не требует загрузки файлов в SPIFFS (но стили и скрипты можно загружать оттуда для экономии памяти)
- Относительно стильный дизайн, светлая и тёмная темы + шаблон "панель управления" с выпадающим меню, кастомизация компонентов (размер, цвет)
- Встроенные модули:
  - Взаимодействие с браузером: получение и отправка значений на компонентах, индикация "плата оффлайн", изменение названия страницы
  - Несколько десятков стандартных компонентов, инструментов вёрстки и навигации (кнопки, иконки, графики, слайдеры, таблицы, вкладки...)
  - Автоматизированное скачивание файлов из SPIFFS + кеширование
  - Автоматизированная загрузка файлов в SPIFFS
  - Блок вывода системной информации и файловый менеджер (SD, LittleFS, SPIFFS...)
  - HTML Canvas API с возможностью рисовать из скетча + API рисования как в Processing
  - Часы реального времени (на основе времени браузера)
  - Автоматический опрос и обновление переменных из списка
  - Авторизация на сервере по логину-паролю
  - DNS сервер (для работы как точка доступа)
  - mDNS (для открытия интерфейса по заданному адресу вместо IP)
  - OTA обновление прошивки и памяти через браузер или curl (возможна защита паролем)

![demo](/docs/demoBig.png)  

## Содержание
- [Установка](#install)
- [Версии](#versions)
- [Баги и обратная связь](#feedback)

<a id="install"></a>
## Установка
- Библиотеку можно найти по названию **GyverPortal** и установить через менеджер библиотек в:
    - Arduino IDE
    - Arduino IDE v2
    - PlatformIO
- [Скачать библиотеку](https://github.com/GyverLibs/GyverPortal/archive/refs/heads/main.zip) .zip архивом для ручной установки:
    - Распаковать и положить в *C:\Program Files (x86)\Arduino\libraries* (Windows x64)
    - Распаковать и положить в *C:\Program Files\Arduino\libraries* (Windows x32)
    - Распаковать и положить в *Документы/Arduino/libraries/*
    - (Arduino IDE) автоматическая установка из .zip: *Скетч/Подключить библиотеку/Добавить .ZIP библиотеку…* и указать скачанный архив
- Читай более подробную инструкцию по установке библиотек [здесь](https://alexgyver.ru/arduino-first/#%D0%A3%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0_%D0%B1%D0%B8%D0%B1%D0%BB%D0%B8%D0%BE%D1%82%D0%B5%D0%BA)

### Обновление
- Рекомендую всегда обновлять библиотеку: в новых версиях исправляются ошибки и баги, а также проводится оптимизация и добавляются новые фичи
- Через менеджер библиотек IDE: найти библиотеку как при установке и нажать "Обновить"
- Вручную: **удалить папку со старой версией**, а затем положить на её место новую. "Замену" делать нельзя: иногда в новых версиях удаляются файлы, которые останутся при замене и могут привести к ошибкам!
- **При использовании файлов стилей и скриптов в SPIFFS их тоже нужно заменить на новые**
- После обновления нужно почистить кэш браузера, для Chrome достаточно нажать Ctrl+F5 на загруженной странице портала

<a id="versions"></a>
## Версии
<details>
<summary>Старые</summary>

## v1.1
- улучшил графики и стили

## v1.2
- Блок NUMBER теперь тип number
- Добавил большое текстовое поле AREA
- Добавил GPunix
- Улучшил парсинг
- Добавил BUTTON_MINI
- Кнопки могут передавать данные с других компонентов (кроме AREA и чекбоксов)
- Добавил PLOT_STOCK - статический график с масштабом
- Добавил AJAX_PLOT_DARK
- Изменён синтаксис у старых графиков
- Фичи GPaddUnix и GPaddInt для графиков
- Убрал default тему
- Подкрутил стили
- Добавил окно лога AREA_LOG и функцию лога в целом

## v1.3 
- переделал GPunix, мелкие фиксы, для списков можно использовать PSTR

## v1.4 
- мелкие фиксы, клик по COLOR теперь отправляет цвет

## v1.5 
- добавил блок "слайдер+подпись"

## v1.5.1 
- мелкий фикс копирования строк

## v1.5.2 
- добавлен *meta charset="utf-8"*, английский README (спасибо VerZsuT)

## v1.6 
- добавлены инструменты для работы c цветом. Добавил answer() для даты, времени и цвета

## v1.7 
- поддержка ESP32

## v2.0: 
- Большое обновление! Логика работы чуть изменена, обнови свои скетчи!
- Много оптимизации/облегчения/ускорения
- Полная поддержка ESP32
- Переделана логика опроса действий (более правильно и оптимально + работает на ESP32) с сохранением легаси
- Убран DateTimeP (не используется в библиотеке) и вынес отдельно в библиотеку DatePack
- Переделан и облегчен модуль лога (log)
- Добавлен MDNS, чтобы не искать IP платы в мониторе порта (см. доку)
- Автоопределение режима работы WiFi. Переделан start() с сохранением легаси (см. доку)
- Упрощён билдер, строку создавать и передавать не нужно (см. доку)
- Объект билдера теперь называется GP (вместо add) с сохранением легаси
- Пофикшены варнинги
- Добавлены удобства для работы с цветом GPcolor, датой GPdate и временем GPtime
- Удалены старые функции преобразования цвета и даты-времени (см. доку)
- Портал теперь возвращает цвет в формате GPcolor, автообновление переменных тоже работает с GPcolor
- Все примеры протестированы на esp8266 и esp32

## v2.1
- Вернул функции root() и uri() для удобства создания многостраничности
- Добавлен пример организации многостраничности
- Добавлена кнопка-ссылка BUTTON_LINK
- Добавлена авторизация по логину-паролю (см. доку)
- Добавлено OTA обновление прошивки из браузера, в т.ч. с паролем (см. доку)

## v3.0: Очень много всего нового
- Огромное спасибо DenysChuhlib и DAK85 за идеи и наработки!
- Добавлен "объектный" режим работы, в котором компоненты удобнее конфигурируются, автоматически получают новые значения и код программы становится сильно компактнее
- Полностью переписан механизм конструктора, сборка занимает во много раз меньше памяти в SRAM за счёт отправки страницы частями
- Переделан механизм добавления кастомного кода на страницу
- Аргументы конструктора теперь принимают const String& - можно передавать строки, const строки, F macro строки
- Переделаны строковые утилиты
- Полностью переделан слайдер
- Убран вариант слайдера с текстом и компонент LABEL_MINI
- Добавлена возможность задания ширины некоторым компонентам
- У некоторых компонентов появилась опция "только чтение"
- Редизайн светодиодов LED GREEN/RED, добавлен LED (красно-зелёный)
- Добавлен компонент BOX_BEGIN/BOX_END, позволяющий удобно собирать компоненты в группы с нужным размером и выравниванием
- Добавлен блок LABEL_BLOCK для выделения текста
- Внутренний AJAX_CLICKS заменён на JS_TOP
- Переделан основной контейнер страницы для удобства кастомизации под любую ширину интерфейса
- Добавлен элемент навигации по динамическим вкладкам NAV_TABS (+ NAV_BLOCK_BEGIN и NAV_BLOCK_END)
- Добавлен элемент навигации с кнопками-ссылками NAV_TABS_LINKS
- Добавлена поддержка FontAwesome иконок для кнопок и панели навигации https://fontawesome.com/v4/icons/
- Пофикшена бага при использовании старого сценария опроса действий
- AJAX_UPDATE переименован в UPDATE с сохранением легаси
- Добавлен блок FILE_UPLOAD для загрузки файлов на сервер
- Добавлен удобный механизм скачивания файлов из SPIFFS памяти с поддержкой 33 типов файлов
- Добавлены блоки для вывода изображений, видео и текстовых файлов из SPIFFS
- Примеры переименованы и сгруппированы по смыслу, добавлены новые примеры
- Добавлен механизм request
- Подключаемым функциям добавлены варианты с адресом на GyverPortal
- Добавлены более удобные варианты компонента SELECT и способы его опроса (getSelectedIdx)
- Механизм update теперь работает с SELECT блоками
- Добавлен шаблон для удобного создания кастомных блоков
- Исправлена работа кликов и обновлений на подстраницах
- Добавлена мини кнопка-ссылка + кнопки для скачивания файлов
- Добавлен оффлайн-режим для графиков (не нужно подключение к Интернет)
- Добавлен блок для добавления стилей из spiffs
- SLIDER теперь умеет работать с float, добавлен NUMBER_F для float
- Добавлен элемент SPINNER
- AREA теперь отсылает сигнал click
- Добавлены макросы для удобной сборки блоков
- И прочее прочее

## v3.1 
- пофикшен getBool()

## v3.2
- На этот раз полностью пофикшен getBool()/copyBool() для SWITCH/CHECK
- Полностью переделан механизм update() - теперь он работает в несколько раз быстрее и обновляет одновременно все указанные компоненты!

## v3.3 TABLE UPDATE
- Улучшена работа парсеров
- Улучшены встроенные JS скрипты
- Префикс макросов сокращён с GP_MAKE_ до M_, подсветка синтаксиса заменена на жирную
- GP_EDGES заменён на GP_JUSTIFY, у SPAN выравнивание теперь тоже задаётся через GPalign
- Добавлен url encode, в TEXT теперь можно вставлять текст со "опасными" символами (+#<>` итд)
- Компоненту SWITCH теперь можно задавать цвет
- click/update/copy Int теперь работает со всеми целочисленными типами (int, byte, long...)
- Добавлен FORM_SEND и FORM_SEND_MINI - новый вариант отправки формы без редиректа
- Добавлен RELOAD_CLICK для перезагрузки страницы по клику по указанным компонентам
- Добавлены стили "отключенным" компонентам
- Добавлен SLIDER_C, отправляющий значения в процессе изменения положения
- Нажатие и отпускание кнопки теперь работает со смартфона (тачскрина)
- Переделан стиль SPINNER, теперь он более компактный
- Добавлены таблицы (TABLE_BEGIN, TABLE_END, TD, TR), макросы (GP_MAKE_TABLE, GP_MAKE_TD, GP_MAKE_TR, GP_ALS)
- Ширину лога можно настраивать
- Для TEXT добавлены атрибуты "паттерн" и максимальная длина ввода. **Изменился последний аргумент в функции**
- Добавлен SUBMIT_MINI
- Добавлен модуль реального локального времени (запрос с браузера), функции getSystemDate(), getSystemTime(), а также getUnix()
- Улучшено ОТА обновление, можно шить через curl
- Чуть оптимизирован механизм Update, также сам вырезает лишние пробелы в списке
- FOLDER_UPLOAD() теперь работает на ESP32
- Добавлен FILE_MANAGER() - вывод списка файлов из памяти с кнопками удалить, а также обработчики deleteFile(), deleteAuto(), deletePath()
- Добавлены компоненты PLAIN() и BOLD() для вывода текста
- Добавлен компонент SYSTEM_INFO() - вывод таблицы с системной информацией
- Добавлен "глаз" для поля ввода пароля
- Добавлен цвет GRAY_B
- Блоки BLOCK... теперь создаются одним компонентом. У THIN блока добавилась настройка цвета

## v3.4 UI UPDATE
- Добавлено
  - HTML Canvas (рисование в браузере) + обновление из скетча + Processing API
  - Разметка страницы в стиле панели управления с боковым меню, компоненты UI_BEGIN, UI_MENU, UI_BODY, UI_END, UI_LINK
  - UPDATE_CLICK() - вызывает update у указанных компонентов при клике по указанным компонентам
  - OTA.error() для вывода текста ошибки в любое место на странице
  - EVAL() выполнение отправленного в update js кода
  - GyverPortal::setFS()
  - Выбор цвета для иконок, FILE_UPLOAD, FOLDER_UPLOAD, OTA_FIRMWARE, OTA_FILESYSTEM, TITLE, LABEL, SPAN, PLAIN, BOLD и HR
  - Макс. ширина для GRID
  - JS_BEGIN() и JS_END()
  - В BUILD_BEGIN_FILE() и BUILD_BEGIN() можно передать тему оформления
  - PAGE_TITLE() - смена имени вкладки в браузере, в т.ч. по update
  - Цвет GP_WHITE
  - Иконки-кнопки ICON_BUTTON() и ICON_FILE_BUTTON()
  - ONLINE_CHECK() - отображение состояния соединения с esp
  - Подписи к осям AJAX_PLOT
  - GyverPortal::caching(bool), GyverPortal::clearCache()
  - Обработка удержания кнопок, отдельный обработчик hold()
  - Поддержка ESP32 CAM, вывод стрима с камеры (CamStream.h + GP.CAM_STREAM)
- Исправлено
  - Мелкие баги
  - HINT() для BUTTON, SWITCH и UPLOAD
  - Потенциальный баг в механизме update
  - ICON_FILE()
- Улучшено
  - Оптимизация стилей и скриптов
  - COLOR теперь можно парсить как int
  - Значительно ускорена (кеширование) загрузка страницы без скриптов/стилей в spiffs
  - При обновлении библиотеки не нужно чистить кеш браузера
  - FILE_MANAGER(): удаление файлов теперь не меняет url в браузере + добавлены кнопки скачать и переименовать + выбор директории
  - Улучшена обработка отпускания кнопки
  - SPINNER(): удержание кнопок, настройка скорости в GP.setSpinnerPeriod()
  - Убран перенос строки в последней строке в LOG
  - Актуализированы objects, добавлен пример
- Изменено
  - Логика работы всплывающих окон, УБРАН АРГУМЕНТ ПЕРИОД
  - SPINNER(): УБРАНА ШИРИНА, сделана автоширина, значение по центру
  - Автоматическое скачивание/загрузка/удаление/переименование ТЕПЕРЬ ВКЛЮЧЕНО ПО УМОЛЧАНИЮ!
  - Отсортированы примеры, portal переименован в ui для краткости
  - clickUp и clickDown вынесены в обработчик hold()
  - Убран устаревший код (до v3)
  - Убраны суффиксы Obj у недокументированных функций
  - У CHECK и SWITCH можно выбрать цвет, ПОРЯДОК АРГУМЕНТОВ ИЗМЕНЁН
  - Изменён порядок аргументов у GPlistIdx, сделан более логичным

## v3.5 CHRISTMAS UPDATE

- Добавлено
  - Отображение границ таблицы TABLE_BORDER()
  - Опасные copy- и click-парсеры (для опроса в условии)
  - Ширина для AREA
  - Всплывающее окно с ошибкой, если "клик" не дошёл до сервера
  - Можно получить логин и пароль, которые вводятся при авторизации, login() и pass()
  - Настройка размера/толщины текста и переноса для текстовых подписей TITLE, LABEL, LABEL_BLOCK. Подписи SPAN/BOLD/PLAIN больше не нужны
  - encodeDMY для GPdate (день.месяц.год)
  - Цвет GP_YELLOW_B
  - Настройка цвета для LED
  - RELOAD_CLICK работает с popup (ALERT, PROMPT, CONFIRM)
  - Проверка подключен ли клиент, функции online() и onlineTimeout()
  - У веб-лога добавлены кнопки для очистки и остановки прокрутки
  - Компонент RADIO для списков выбора
- Пофикшено
  - Глаз в PASSWORD() поставлен на место
  - Баг с макросом M_TR10
  - SPINNER() повинуется выравниванию
  - Таблица SYSTEM_INFO вернулась в компактный вид
  - HINT (сломался в v3.4)
  - Невероятный баг с вечной загрузкой CHECK() и проблемой с опросом его значения с формы
- Улучшено
  - Оптимизированы скрипты
  - Автоматическое удаление пробелов в списке UPDATE()
  - Ширину окна CAM_STREAM() и cam_stream_window можно задать стрингой
  - Дизайн таблички FILE_MANAGER
  - Переделан механизм перезагрузки страницы, теперь работает гораздо быстрее и стабильнее
  - UPDATE запрашивает обновления только когда окно браузера активно
  - UPDATE при пропадании связи сигнализирует всплывающим баннером
  - Скрыты пустые ячейки у таблицы с заданными ширинами
- Изменено
  - В SPINNER() вернулась ширина предпоследним аргументом, её установка отключает автоширину
  - ONLINE_CHECK() теперь выдаёт всплывающий баннер вместо иконки в названии страницы
  - Убран setReloadTimeout(), механизм улучшен, задаётся общий таймаут в setTimeout()
  - Дизайн LABEL_BLOCK, чтобы отличался от кнопок
  - Поле пароля с "глазом" теперь вызывается компонентом PASS_EYE

## v3.5.2 FIX
- Добавлено
  - Объект RADIO
- Пофикшено
  - Вернул автоматическую ширину полям ввода текста
  - Принудительное отображение секунд в TIME
  - Ошибка компиляции esp32
  - Пример WiFilogin
- Улучшено
  - Отключен зум на мобильных устройствах
  
## v3.5.3 FIX
- Пофикшено
  - Критический баг в GPfileType и отправке файла на 8266
  - Не работало удаление через менеджер файлов на esp32
- Улучшено
  - Кнопки внутри формы не приводят к сабмиту (багофича html)
  
</details>

## v3.6 MINOR
- Добавлено
    - Опциональное выравнивание по верху у BOX
    - Добавлен тип блока GP_DIV_RAW - без отступов
- Улучшено
    - Декодеры даты и времени
    - Парсеры перенесены в отдельный файл для нужд других библиотек
    
## v3.6.1
- Исправлена ошибка компиляции parsers в IDE v2
- Добавлено больше возможностей отладки для OTA

## v3.6.2
- Исправлены ошибки компиляции:
    - В Arduino IDE v2 для ESP32
    - Для ESP8266 версии SDK ниже 3.1
    
## v3.6.3
- Парсер удержания вынесен в отдельный файл для нужд других библиотек

<a id="feedback"></a>
## Баги и обратная связь
При нахождении багов создавайте **Issue**, а лучше сразу пишите на почту [alex@alexgyver.ru](mailto:alex@alexgyver.ru)
Библиотека открыта для доработки и ваших **Pull Request**'ов!

При сообщении о багах или некорректной работе библиотеки нужно обязательно указывать:
- Версия библиотеки
- Какой используется МК
- Версия SDK (для ESP)
- Версия Arduino IDE
- Корректно ли работают ли встроенные примеры, в которых используются функции и конструкции, приводящие к багу в вашем коде
- Какой код загружался, какая работа от него ожидалась и как он работает в реальности
- В идеале приложить минимальный код, в котором наблюдается баг. Не полотно из тысячи строк, а минимальный код
