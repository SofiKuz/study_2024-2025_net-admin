---
## Front matter
title: "Отчёт по лабораторной работе №15"
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

Настроить динамическую маршрутизацию между территориями организации.

# Выполнение лабораторной работы

Откроем проект с названием lab_PT-14.pkt и сохраним под названием lab_PT-15.pkt. После чего откроем его для дальнейшего редактирования.

![Открытие проекта lab_PT-15.pkt](image/1.png){#fig:001 width=70%}

Для начала настроим OSPF на маршрутизаторе msk-donskaya-svkuznecova-gw-1. Включим OSPF на маршрутизаторе предполагает, во-первых,
включение процесса OSPF командой router ospf , во-вторых — назначение областей (зон) интерфейсам с помощью команды
network area.

Идентификатор процесса OSPF (process-id) по сути идентифицирует маршрутизатор в автономной системе, и, вообще говоря, он не должен совпадать с идентификаторами процессов на других маршрутизаторах.

Значение идентификатора области (area-id) может быть целым числом от 0 до 4294967295 или может быть представлено в виде IP-адреса: A.B.C.D. Область 0 называется магистралью, области с другими идентификаторами должны подключаться к магистрали.

![Настройка OSPF на маршрутизаторе msk-donskaya-svkuznecova-gw-1](image/2.png){#fig:002 width=70%}

Проверим состояния протокола OSPF на маршрутизаторе msk-donskaya-svkuznecova-gw-1. Маршрутизаторы с общим сегментом являются соседями в этом сегменте. Соседи выбираются с помощью протокола Hello. Команда show ip ospf neighbor показывает статус всех соседей в заданном сегменте. Команда show ip ospf route (или show ip route) выводит информацию из таблицы маршрутизации.

![Проверка состояния протокола OSPF на маршрутизаторе msk-donskaya-svkuznecova-gw-1](image/3.png){#fig:003 width=70%}

Далее приступим к настройке: маршрутизатора msk-q42-svkuznecova-gw-1, маршрутизирующего коммутатора msk-hostel-svkuznecova-gw-1, маршрутизатора sch-sochi-svkuznecova-gw-1.

![Маршрутизатор msk-q42-svkuznecova-gw-1](image/4.png){#fig:004 width=70%}

![Маршрутизирующий коммутатор msk-hostel-svkuznecova-gw-1](image/5.png){#fig:005 width=70%}

![Маршрутизатор sch-sochi-svkuznecova-gw-1](image/6.png){#fig:006 width=70%}

Теперь проверим состояние OSPF на всех вышеперечисленных устройствах.

![Маршрутизатор msk-q42-svkuznecova-gw-1](image/7.png){#fig:007 width=70%}

![Маршрутизатор msk-hostel-svkuznecova-gw-1](image/8.png){#fig:008 width=70%}

![Маршрутизатор sch-sochi-svkuznecova-gw-1](image/9.png){#fig:009 width=70%}

Перейдём к настройке линка 42-й квартал–Сочи.

![Настройка интерфейсов коммутатора provider-svkuznecova-sw-1](image/10.png){#fig:010 width=70%}

![Настройка маршрутизатора msk-q42-svkuznecova-gw-1](image/11.png){#fig:011 width=70%}

![Настройка коммутатора sch-sochi-svkuznecova-sw-1](image/12.png){#fig:012 width=70%}

![Настройка маршрутизатора sch-sochi-vkuznecova-gw-1](image/13.png){#fig:013 width=70%}

# Выводы

В ходе выполнения лабораторной работы мы настроили динамическую маршрутизацию между территориями организации.

# Ответы на контрольные вопросы:
1. Какие протоколы относятся к протоколам динамической маршрутизации? 
- OSPF, RIP, EIGRP.

2. Охарактеризуйте принципы работы протоколов динамической маршрутизации. 
- Маршрутизаторы по протоколу делятся между собой информацией из своих таблиц маршрутизации и корректируют их в соответствии с остальными.

3. Опишите процесс обращения устройства из одной подсети к устройству из другой подсети по протоколу динамической маршрутизации. 
– Вектор-Расстояние — маршрутизатор рассылает список адресов со сборным параметром расстояния (кол-во маршрутизаторов, производительность и т. д.) из доступных сетей. Состояние канала — маршрутизаторы обмениваются топологической (связи маршрутизаторов) информацией.

4. Опишите выводимую информацию при просмотре таблицы маршрутизации. 
- Протокол Тип маршрута Адрес удаленной сети [Административная дистанция источника/Метрика маршрута]. Следующий маршрутизатор Время последнего обновления маршрута Интерфейс.
