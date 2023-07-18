# Android
## Документация
- [Build location-aware apps ](https://developer.android.com/training/location)
- [Google Play services. Location](https://developers.google.com/android/reference/com/google/android/gms/location/package-summary)
- [android.location](https://developer.android.com/reference/android/location/package-summary)

## Термины
|Термин|Описание|
|-|-|
|GNSS|[Спутниковая система навигации](https://ru.wikipedia.org/wiki/Спутниковая_система_навигации)|
|Альманах|Таблица положений всех спутников, которым должен располагать любой спутниковый приёмник до начала измерений|
|СРНС|Спутниковая радионавигационная система, типа ГЛОНАСС и GPS (NAVSTAR)|
|[DGPS](https://ru.wikipedia.org/wiki/Differential_GPS)|Системы дифференциальной коррекции - система повышения точности сигналов ГНСС заключающаяся в исправлении измеренных приемником псевдодальностей до спутников поправками к ним, полученными извне, от достоверного измерителя (базовая или опорная станция)|

## Спутниковые системы навигации
На 2020 год три спутниковые системы обеспечивали полное покрытие и бесперебойную работу для всего земного шара - [GPS](https://ru.wikipedia.org/wiki/GPS), [ГЛОНАСС](https://ru.wikipedia.org/wiki/ГЛОНАСС), [Бэйдоу](https://ru.wikipedia.org/wiki/Бэйдоу)

### Действующие и создаваемые спутниковые системы
|Система|Точность|Описание|
|-|-|-|
|[GPS](https://ru.wikipedia.org/wiki/GPS)|5 м (без DGPS)|Принадлежит министерству обороны США. <br> Этот факт, по мнению некоторых государств, является её главным недостатком. Устройства, поддерживающие навигацию по GPS, являются самыми распространёнными в мире. <br> Также известна под более ранним названием NAVSTAR.|
|[ГЛОНАСС](https://ru.wikipedia.org/wiki/ГЛОНАСС)|4,5 м - 7,4 м (без DGPS)|Принадлежит министерству обороны РФ. <br> Разработка системы официально началась в 1976 г., полное развёртывание системы завершилось в 1995 г. После 1996 года спутниковая группировка сокращалась и к 2002 году пришла в упадок. Была восстановлена к концу 2011 г. В настоящее время на орбите находится 127 спутников, из которых 122 используется по назначению. К 2025 году предполагается глубокая модернизация системы.|
|[Бэйдоу](https://ru.wikipedia.org/wiki/Бэйдоу)||Китайская глобальная спутниковая система навигации, основанная на геостационарных, геосинхронных спутниках и спутниках со средними орбитами. <br> Реализация программы началась в 1994 году. Первый спутник вышел на орбиту в 2000 году. По состоянию на 2015 год система имела 4 работающих спутников: 2 на геостационарных орбитах, 3 — на геосинхронных и 4 — на средних околоземных. 23 июня 2020 года был запущен 15 спутник системы «Бэйдоу», тем самым было завершено создание глобальной спутниковой системы навигации. 31 июля 2020 года председатель КНР Си Цзиньпин заявил о начале эксплуатации системы «Бэйдоу».|
|[DORIS](https://ru.wikipedia.org/wiki/DORIS)||Французская навигационная система. <br> Принцип работы системы связан с применением эффекта Допплера. В отличие от других спутниковых навигационных систем основана на системе стационарных наземных передатчиков, приёмники расположены на спутниках. После определения точного положения спутника система может установить точные координаты и высоту маяка на поверхности Земли. Первоначально предназначалась для наблюдения за океанами и дрейфом материков.|
|[Galileo](https://ru.wikipedia.org/wiki/Галилео_(спутниковая_система_навигации))|1 м (открытый сигнал), 0,01 м (закрытый)|Европейская система, находящаяся на этапе создания спутниковой группировки. <br> По состоянию на ноябрь 2016 года на орбите находится 16 спутников, 9 действующих и 7 тестируемых. Планируется полностью развернуть спутниковую группировку к 2020 году.|

### Создаваемые региональные спутниковые системы

|Система|Описание|
|-|-|
|[IRNSS](https://ru.wikipedia.org/wiki/IRNSS)|Индийская навигационная спутниковая система, в состоянии разработки. Предполагается для использования только в Индии. Первый спутник был запущен в 2008 году. Общее количество спутников системы IRNSS — 7.|
|[QZSS](https://ru.wikipedia.org/wiki/QZSS)|Японская квази-зенитная спутниковая система (Quasi-Zenith Satellite System, QZSS) была задумана в 2002 г. как коммерческая система с набором услуг для подвижной связи, вещания и широкого использования для навигации в Японии и соседних районах Юго-Восточной Азии. Первый QZSS-спутник был запущен в 2010 г. Предполагается создание группировки из трёх спутников, находящихся на геосинхронных орбитах, а также собственной системы дифференциальной коррекции.|

## Системы дифференциальной коррекции
Отдельные модели спутниковых приёмников позволяют производить т. н. «дифференциальное измерение» расстояний между двумя точками с большой точностью (сантиметры). Для этого измеряется положение навигатора в двух точках с небольшим промежутком времени. При этом, хотя каждое такое измерение имеет погрешность, равную 10-15 метров без наземной системы корректировки и 10-50 см с такой системой, измеренное расстояние имеет погрешность намного меньшую, так как факторы, мешающие измерению (погрешность орбит спутников, неоднородность атмосферы в данном месте Земли и т. д.) в этом случае взаимно вычитаются.

Кроме того, есть несколько систем, которые посылают потребителю уточняющую информацию («дифференциальную поправку к координатам»), позволяющую повысить точность измерения координат приёмника до 10 сантиметров. Дифференциальная поправка пересылается либо с геостационарных спутников, либо с наземных базовых станций, может быть платной (расшифровка сигнала возможна только одним определённым приёмником после оплаты «подписки на услугу») или бесплатной.

На 2009 год имелись следующие бесплатные системы предоставления поправок:
|NGSS|DGPS|Описание|
|-|-|-|
|[WAAS](https://ru.wikipedia.org/wiki/Wide_Area_Augmentation_System)|GPS|американская система|
|[СДКМ](https://ru.wikipedia.org/wiki/СДКМ)|ГЛОНАСС|Система Дифференциальной Коррекции и Мониторинга - широкозонная система дифференциальной коррекции для навигационных спутниковых систем ГЛОНАСС (РФ) и GPS (США). <br> Разработана АО «Российские космические системы»|
|[EGNOS](https://ru.wikipedia.org/wiki/EGNOS)|Galileo|европейская система|
|[MSAS](https://ru.wikipedia.org/wiki/MSAS)|QZSS|японская система|
|[GAGAN](https://ru.wikipedia.org/wiki/GAGAN)|||

Они основаны на нескольких передающих поправки геостационарных спутниках, позволяющих получить высокую точность (до 30 см).

Создание системы коррекции для ГЛОНАСС под названием СДКМ завершено к 2016. 