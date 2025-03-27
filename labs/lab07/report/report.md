---
## Front matter
title: "Отчёт по лабораторной работе №7"
subtitle: "дисциплина: Администрирование локальных сетей"
author: "Студент: Кузнецова София Вадимовна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Получить навыки работы с физической рабочей областью Packet Tracer, а также учесть физические параметры сети.

# Выполнение лабораторной работы

Откроем проект с названием lab_PT-06.pkt и сохраним его под названием lab_PT-07.pkt. После чего откроем его для дальнейшего редактирования.

![Открытие проекта lab_PT-07.pkt](image/1.png){#fig:001 width=70%}

Перейдите в физическую рабочую область Packet Tracer. Присвоим название городу — Moscow.

![Открытие физической рабочей области Packet Tracer и присвоим названия городу](image/2.png){#fig:002 width=70%}

Щёлкнув на изображении города, мы увидим изображение здания. Присвоим ему название Donskaya. Добавим здание для территории Pavlovskaya.

![Присвоение зданию названия Donskaya и добавление здания для территории Pavlovskaya](image/3.png){#fig:003 width=70%}

Щёлкнув на изображении здания Donskaya, переместим изображение, обозначающее серверное помещение, в него.

![Перемещение изображения, обозначающее серверное помещение, внутрь здания](image/4.png){#fig:004 width=70%}

Затем щёлкнув на изображении серверной, мы увидим отображение серверных стоек. Переместим коммутатор msk-pavlovskaya-svkuznecova-sw-1 и два оконечных устройства dk-pavlovskaya-1 и other-pavlovskaya-1 на территорию Pavlovskaya, используя меню Move физической рабочей области Packet Tracer.

![Перемещение коммутатора msk-pavlovskaya-svkuznecova-sw-1 на территорию Pavlovskaya](image/5.png){#fig:005 width=70%}

![Перемещение оконечных устройства dk-pavlovskaya-1 и other-pavlovskaya-1 на территорию Pavlovskaya](image/6.png){#fig:006 width=70%}

Вернувшись в логическую рабочую область Packet Tracer, пропингуем с коммутатора msk-donskaya-svkuznecova-sw-1 коммутатор msk-pavlovskaya-svkuznecova-sw-1 и убедимся в работоспособности соединения.

![Пинг с коммутатора msk-donskaya-svkuznecova-sw-1 коммутатор msk-pavlovskaya-svkuznecova-sw-1(проверка работоспособности соединения)](image/7.png){#fig:007 width=70%}

Далее в меню Options, Preferences во вкладке Interface активируем разрешение на учёт физических характеристик среды передачи (Enable Cable Length Effects).

![Активация разрешения на учёт физических характеристик среды передачи](image/8.png){#fig:008 width=70%}

Теперь в физической рабочей области Packet Tracer разместим две территории на расстоянии более 100 м друг от друга.

![Размещение двух территории на расстоянии более 100 м друг от друга](image/9.png){#fig:009 width=70%}

Вернувшись в логическую рабочую область Packet Tracer, пропингуем с коммутатора msk-donskaya-svkuznecova-sw-1 коммутатор msk-pavlovskaya-svkuznecova-sw-1 и убедимся в неработоспособности соединения.

![Пинг с коммутатора msk-donskaya-svkuznecova-sw-1 коммутатор msk-pavlovskaya-svkuznecova-sw-1(проверка неработоспособности соединения)](image/10.png){#fig:010 width=70%}

Далее удалим соединение между msk-donskaya-svkuznecova-sw-1 и msk-pavlovskaya-svkuznecova-sw-1. Добавим в логическую рабочую область два повторителя (Repeater-PT). Присвоим им соответствующие названия msk-donskaya-svkuznecova-mc-1 и msk-pavlovskaya-svkuznecova-mc-1. Заменим имеющиеся модули на PT-REPEATER- NM-1FFE и PT-REPEATER-NM-1CFE для подключения оптоволокна и витой пары по технологии Fast Ethernet.

![Добавление в логическую рабочую область два повторителя (Repeater-PT)](image/11.png){#fig:011 width=70%}

![Замена имеющиеся модули на PT-REPEATER- NM-1FFE и PT-REPEATER-NM-1CFE](image/12.png){#fig:012 width=70%}

Переместим msk-pavlovskaya-svkuznecova-mc-1 на территорию Pavlovskaya (в физиче-ской рабочей области Packet Tracer).

![Перемещение msk-pavlovskaya-svkuznecova-mc-1 на территорию Pavlovskaya](image/13.png){#fig:013 width=70%}

Теперь подключим коммутатор msk-donskaya-svkuznecova-sw-1 к msk-donskaya-svkuznecova-mc-1 по витой паре, msk-donskaya-svkuznecova-mc-1 и msk-pavlovskaya-mc-1 — по оптоволокну, msk-pavlovskaya-svkuznecova-sw-1 к msk-pavlovskaya-svkuznecova-mc-1 — по витой паре.

![Подключение коммутаторов](image/14.png){#fig:014 width=70%}

Убедимся в работоспособности соединения между msk-donskaya-svkuznecova-sw-1 и msk-pavlovskaya-svkuznecova-sw-1.

![Пинг с коммутатора msk-donskaya-svkuznecova-sw-1 коммутатор msk-pavlovskaya-svkuznecova-sw-1(проверка работоспособности соединения)](image/15.png){#fig:015 width=70%}

# Выводы

В ходе выполнения лабораторной работы мы получили навыки работы с физической рабочей областью Packet Tracer, а также научились учитывать физические параметры сети.

# Ответы на контрольные вопросы

1. Перечислите возможные среды передачи данных. На какие характеристики среды передачи данных следует обращать внимание при планировании сети? 
- Коаксиал, витая пара, оптоволокно, беспроводные. Допустимое расстояние, скорость передачи, реальные физические факторы для беспроводных сетей.

2. Перечислите категории витой пары. Чем они отличаются? Какая категория в каких условиях может применяться? 
- Существует несколько категорий кабеля «витая пара», которые нумеруются от 1 до 8 и определяют эффективный пропускаемый частотный диапазон Категории отличаются диапазоном частот, строением кабелей, скоростью передачи. Применяются в зависимости от требуемой скорости передачи/века.

3. В чем отличие одномодового и многомодового оптоволокна? Какой тип кабеля в каких условиях может применяться? 
- В количестве проходящих лучей. Одномодовые — дороже, многомодовые — охватывают меньшее расстояние.

4. Какие разъёмы встречаются на патчах оптоволокна? Чем они отличаются? 
- SC — высокая скорость и плотность коммутации, ненадежный корпус. ST — меньшая плотность коммутации, надежный корпус. FC — большая сложность коммутации.
