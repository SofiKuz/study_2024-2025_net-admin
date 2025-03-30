---
## Front matter
title: "Отчёт по лабораторной работе №8"
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

Приобрести практические навыки по настройке динамического распределения IP-адресов посредством протокола DHCP (Dynamic Host Configuration Protocol) в локальной сети.

# Выполнение лабораторной работы

Откроем проект с названием lab_PT-07.pkt и сохраним его под названием lab_PT-08.pkt. После чего откроем его для дальнейшего редактирования.

![Открытие проекта lab_PT-08.pkt](image/1.png){#fig:001 width=70%}

В логическую рабочую область проекта добавим сервер dns и подключим его к коммутатору msk-donskaya-sw-3 через порт Fa0/2.

![Добавление сервера dns и подключение его к коммутатору msk-donskaya-sw-3](image/2.png){#fig:002 width=70%}

Далее активируем порт при помощи соответствующих команд на коммутаторе.

![Активация порта на коммутаторе](image/3.png){#fig:003 width=70%}

В конфигурации сервера укажем в качестве адреса шлюза 10.128.0.1, а в качестве адреса самого сервера — 10.128.0.5 с соответствующей маской 255.255.255.0.

![Настройка конфигурации сервера](image/4.png){#fig:004 width=70%}

Далее настроим сервис DNS:
– в конфигурации сервера выберите службу DNS, активируйте её (выбрав флаг On);
– в поле Type в качестве типа записи DNS выберите записи типа A (A Record);
– в поле Name укажите доменное имя, по которому можно обратиться, например, к web-серверу — www.donskaya.rudn.ru, затем укажите его IP-адрес в соответствующем поле 10.128.0.2;
– нажав на кнопку Add , добавьте DNS-запись на сервер;
– аналогичным образом добавьте DNS-записи для серверов mail, file, dns;
– сохраните конфигурацию сервера.

![Настройка сервиса DNS](image/5.png){#fig:005 width=70%}

Настроим DHCP-сервис на маршрутизаторе, используя приведённые в лабораторной работе команды для каждой выделенной сети(укажем IP-адрес DNS-сервера; затем перейдём к настройке DHCP; зададим название конфигурируемому диапазону адресов (пулу адресов), укажем адрес сети, а также адреса шлюза и DNS-сервера; зададим пулы адресов, исключаемых из динамического распределени).

![Настройка DHCP-сервис на маршрутизаторе](image/6.png){#fig:006 width=70%}

На оконечных устройствах заменим в настройках статическое распределение адресов на динамическое.

![Замена статического распределение адресов на динамическое](image/7.png){#fig:007 width=70%}

Затем проверим, какие адреса выделяются оконечным устройствам.

![Проверка выделения адресов оконечных устройств](image/8.png){#fig:008 width=70%}

Не забываем также проверить доступность устройств из разных подсетей.

![Проверка доступности устройств из разных подсетей](image/9.png){#fig:009 width=70%}

В режиме симуляции изучим, каким образом происходит запрос адреса по протоколу DHCP.

![Режим симуляции](image/10.png){#fig:010 width=70%}

# Выводы

В ходе выполнения лабораторной работы мы приобрели практические навыки по настройке динамического распределения IP адресов посредством протокола DHCP (Dynamic Host Configuration Protocol) в локальной сети.

# Ответы на контрольные вопросы

1. За что отвечает протокол DHCP? 
- За автоматическое получение IP и других параметров.

2. Какие типы DHCP-сообщений передаются по сети?
• DHCPDISCOVER (клиент <> сервер) — начальное сообщение.
• DHCPOFFER (сервер <> клиент) — ответ на начальное сообщение с сетевыми настройками.
• DHCPREQUEST (клиент <> сервер) — настройки приняты.
• DHCPACK (сервер <> клиент) — авторизация клиента, настройки приняты.
• DHCPNAK (сервер <> клиент) — авторизация невозможна.
• DHCPDECLINE (клиент <> сервер) — IP уже используется.
• DHCPINFORM (клиент <> сервер) — присвоен статический IP, а нужен динамический.
• DHCPRELEASE (клиент <> сервер) — завершение использования IP.

3. Какие параметры могут быть переданы в сообщениях DHCP? 
- По умолчанию запросы от клиента делаются к серверу на порт 67, сервер в свою очередь отвечает клиенту на порт 68, выдавая адрес IP и другую необходимую информацию, такую, как сетевую маску, маршрутизатор и серверы DNS.

4. Что такое DNS? 
- Система, ставящая в соответствие доменному имени хоста IP и наоборот.

5. Какие типы записи описания ресурсов есть в DNS и для чего они используются? 
• RR-записи описывают все узлы сети в зоне и помечают делегирование поддоменов.
• SOA-запись — указывает на авторитативность для зоны.
• NS-запись — перечисляет DNS-серверы зоны.
• А — задаёт отображение имени узла в IP.
• PTR — задаёт отображение IP в имя узла.
