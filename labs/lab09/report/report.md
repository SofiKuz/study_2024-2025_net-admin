---
## Front matter
title: "Отчёт по лабораторной работе №9"
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

Изучить возможности протокола STP и его модификаций по обеспечению отказоустойчивости сети, агрегированию интерфейсов и перераспределению нагрузки между ними.

# Выполнение лабораторной работы

Откроем проект с названием lab_PT-08.pkt и сохраним его под названием lab_PT-09.pkt. После чего откроем его для дальнейшего редактирования.

![Открытие проекта lab_PT-09.pkt](image/1.png){#fig:001 width=70%}

Сформируем резервное соединение между коммутаторами msk-donskaya-svkuznecova-sw-1 и msk-donskaya-svkuznecova-sw-3. Для этого заменим соединение между коммутаторами msk-donskaya-svkuznecova-sw-1 (Gig0/2) и msk-donskaya-svkuznecova-sw-4 (Gig0/1) на соединение между коммутаторами msk-donskaya-svkuznecova-sw-1 (Gig0/2) и msk-donskaya-svkuznecova-sw-3 (Gig0/2.

![Резервное соединение](image/2.png){#fig:002 width=70%}

Сделаем порт на интерфейсе Gig0/2 коммутатора msk-donskaya-svkuznecova-sw-3 транковым.

![Транковый порт](image/3.png){#fig:003 width=70%}

Теперь соединение между коммутаторами msk-donskaya-svkuznecova-sw-1 и msk-donskaya-svkuznecova-sw-4 сделаем через интерфейсы Fa0/23, не забыв активировать их в транковом режиме.

![Соединение между коммутаторами msk-donskaya-svkuznecova-sw-1 и msk-donskaya-svkuznecova-sw-4 через интерфейсы Fa0/23](image/4.png){#fig:004 width=70%}

![Активация в транковом режиме](image/5.png){#fig:005 width=70%}

![Активация в транковом режиме](image/6.png){#fig:006 width=70%}

С оконечного устройства dk-donskaya-1 пропингуем серверы mail и web. В режиме симуляции проследим движение пакетов ICMP. Убедимся, что движение пакетов происходит через коммутатор msk-donskaya-svkuznecova-sw-2.

![Пинг](image/7.png){#fig:007 width=70%}

![Режим симуляции](image/8.png){#fig:008 width=70%}

![Режим симуляции](image/9.png){#fig:009 width=70%}

На коммутаторе msk-donskaya-svkuznecova-sw-2 посмотриv состояние протокола STP для vlan 3. В результате увидим информацию, связанную с протоколом STP, в частности то, что данное устройство является корневым.

![Cостояние протокола STP для vlan 3](image/10.png){#fig:010 width=70%}

В качестве корневого коммутатора STP настроим коммутатор msk-donskaya-svkuznecova-sw-1.

![Корневой коммутатор](image/11.png){#fig:011 width=70%}

Используя режим симуляции, убедимся, что пакеты ICMP пойдут от хоста dk-donskaya-1 до mail через коммутаторы msk-donskaya-svkuznecova-sw-1 и msk-donskaya-svkuznecova-sw-3, а от хоста dk-donskaya-1 до web через коммутаторы msk-donskaya-svkuznecova-sw-1 и msk-donskaya-svkuznecova-sw-2.

![Режим симуляции](image/12.png){#fig:012 width=70%}

![Режим симуляции](image/13.png){#fig:013 width=70%}

Настроим режим Portfast на тех интерфейсах коммутаторов, к которым подключены серверы.

![msk-donskaya-svkuznecova-sw-2](image/14.png){#fig:014 width=70%}

![msk-donskaya-svkuznecova-sw-3](image/15.png){#fig:015 width=70%}

Изучим отказоустойчивость протокола STP и время восстановления соединения при переключении на резервное соединение. Для этого используйте команду ping -n 1000 mail.donskaya.rudn.ru на хосте dk-donskaya-1, а разрыв соединения обеспечим переводом соответствующего интерфейса коммутатора в состояние shutdown.

![Отказоустойчивость](image/16.png){#fig:016 width=70%}

![Отказоустойчивость](image/17.png){#fig:017 width=70%}

Далее переключим коммутаторы в режим работы по протоколу Rapid PVST+.

![Протокол Rapid PVST+](image/18.png){#fig:018 width=70%}

Изучим отказоустойчивость протокола Rapid PVST+ и время восстановления соединения при переключении на резервное соединение.

![Отказоустойчивость](image/19.png){#fig:019 width=70%}

![Отказоустойчивость](image/20.png){#fig:020 width=70%}

Сформируем агрегированное соединение интерфейсов Fa0/20 – Fa0/23 между коммутаторами msk-donskaya-svkuznecova-sw-1 и msk-donskaya-svkuznecova-sw-4.

![Агрегированное соединение интерфейсов](image/21.png){#fig:021 width=70%}

![msk-donskaya-svkuznecova-sw-1](image/22.png){#fig:022 width=70%}

![msk-donskaya-svkuznecova-sw-4](image/23.png){#fig:023 width=70%}

# Выводы

В ходе выполнения лабораторной работы изучила возможности протокола STP и его модификаций по обеспечению отказоустойчивости сети, агрегированию интерфейсов и перераспределению нагрузки между ними.

# Ответы на контрольные вопросы

1. Какую информацию можно получить, воспользовавшись командой определения состояния протокола STP для VLAN (на корневом и не на корневом устройстве)? Приведите примеры вывода подобной информации на устройствах.
- VLAN... // Номер VLAN
- STP ... // Тип протокола
- Root ID/Bridge ID // Ближайший коммутатор/Текущий коммутатор
- Priority ... // Приоритет
- Address ... // MAC-адрес
- Cost ... // «Затраты» до этого коммутатора
- Port ... // Порт
- Hello Time ... Max Age ... Forward Delay ... Aging Time ... // Время работы STP // Свойства портов

2. При помощи какой команды можно узнать, в каком режиме, STP или Rapid PVST+, работает устройство? Приведите примеры вывода подобной информации на устройствах 
- sh ru

3. Для чего и в каких случаях нужно настраивать режим Portfast? 
- Он позволяет сразу включать выделенные порты, поскольку они не подключены к коммутаторам и не участвуют во включении STP.

4. В чем состоит принцип работы агрегированного интерфейса? Для чего он используется? 
- Он объединяет параллельные каналы для увеличения пропускной способности, а также не теряет соединение при обрыве одного из каналов, перенаправляя трафик.

5. В чём принципиальные отличия при использовании протоколов LACP (Link Aggregation Control Protocol), PAgP (Port Aggregation Protocol) и статического агрегирования без использования протоколов? 
- LACP общий стандарт IEEE, PAgP — локальный протокол Cisco. Для них обязательна настройка сторон (активная, пассивная, авто). При статическом агрегировании коммутатор обрабатывает данные как с магистрали, даже если она не настроена на другой стороне.

6. При помощи каких команд можно узнать состояние агрегированного канала EtherChannel? 
- show etherchannel
