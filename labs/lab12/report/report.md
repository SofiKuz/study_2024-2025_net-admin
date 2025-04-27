---
## Front matter
title: "Отчёт по лабораторной работе №12"
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

Приобретение практических навыков по настройке доступа локальной сети к внешней сети посредством NAT.

# Выполнение лабораторной работы

Откроем проект с названием lab_PT-11.pkt и сохраним под названием lab_PT-12.pkt. После чего откроем его для дальнейшего редактирования.

![Открытие проекта lab_PT-12.pkt](image/1.png){#fig:001 width=70%}

Для начала сделаем первоначальную настройку маршрутизатора provider-svkuznecova-gw-1 и коммутатора provider-svkuznecova-sw-1 провайдера: зададим имя, настроим доступ по паролю и т.п.

![Первоначальная настройка маршрутизатора provider-svkuznecova-gw-1](image/2.png){#fig:002 width=70%}

![Первоначальная настройка коммутатора provider-sckuznecova-sw-1](image/3.png){#fig:003 width=70%}

Теперь настроим интерфейсы маршрутизатора provider-svkuznecova-gw-1 и коммутатора provider-svkuznecova-sw-1 провайдера.

![Настройка интерфейсов маршрутизатора provider-svkuznecova-gw-1](image/4.png){#fig:004 width=70%}

![Настройка интерфейсов коммутатора provider-svkuznecova-sw-1](image/5.png){#fig:005 width=70%}

Выполним проверку командой ping с сервера www.rudn.ru на роутер провайдера.

![Проверка командой ping с сервера www.rudn.ru на роутер провайдера](image/6.png){#fig:006 width=70%}

Следующим шагом настроим интерфейсы маршрутизатора сети «Донская» для доступа к сети провайдера.

![Настройка интерфейсов маршрутизатора msk-donskaya-svkuznecova-gw-1 для доступа к сети провайдера](image/7.png){#fig:007 width=70%}

Выполним проверку.

![Проверка](image/8.png){#fig:008 width=70%}

Настроим на маршрутизаторе сети «Донская» NAT с правилами, указанными в лабораторной работе.

![Настройка пула адресов для NAT](image/9.png){#fig:009 width=70%}

![Настройка списка доступа для NAT](image/10.png){#fig:010 width=70%}

![Сеть дисплейных классов(имеют доступ только к сайтам, необходимым для учёбы (www.yandex.ru (192.0.2.11), stud.rudn.university (192.0.2.12))](image/11.png){#fig:011 width=70%}

![Сеть кафедр (работает только с образовательными сайтами (esystem.pfur.ru (192.0.2.13)))](image/12.png){#fig:012 width=70%}

![Сеть администрации (имеет возможность работать только с сайтом университета (www.rudn.ru (192.0.2.14)))](image/13.png){#fig:013 width=70%}

![Доступ для компьютера администратора (в сети для других пользователей компьютер администратора имеет полный доступ в Интернет. Другие не имеют доступа.)](image/14.png){#fig:014 width=70%}

![Настройка NAT (Port Address Translation и интерфейсов для NAT)](image/15.png){#fig:015 width=70%}

![Проверка](image/16.png){#fig:016 width=70%}

![Проверка](image/17.png){#fig:017 width=70%}

На последнем шаге настроим доступ из внешней сети в локальную сеть организации, как указано в лабораторной работе.

![Настройка доступа из Интернета (WWW-сервер)](image/18.png){#fig:018 width=70%}

![Настройка доступа из Интернета (файловый сервер)](image/19.png){#fig:019 width=70%}

![Настройка доступа из Интернета (почтовый сервер)](image/20.png){#fig:020 width=70%}

![Настройка доступа из Интернета (доступ по RDP)](image/21.png){#fig:021 width=70%}

![Проверка](image/22.png){#fig:022 width=70%}

# Выводы

В ходе выполнения лабораторной работы мы приобрели практические навыки по настройке доступа локальной сети к внешней сети посредством NAT.

# Ответы на контрольные вопросы

1. В чём состоит основной принцип работы NAT (что даёт наличие NAT в сети организации)? 
- NAT на устройстве позволяет ему соединять публичные и частные сети между собой с помощью только одного IP-адреса для группы.

2. В чём состоит принцип настройки NAT (на каком оборудовании и что нужно настроить для из локальной сети во внешнюю сеть через NAT)?
- Настроить интерфейсы на внутренних и внешних маршрутизаторах, наборы правил для преобразования IP.

3. Можно ли применить Cisco IOS NAT к субинтерфейсам? 
- Да, поскольку они существуют в энергонезависимой памяти.

4. Что такое пулы IP NAT? 
- Выделяемые для трансляции NAT IP.

5. Что такое статические преобразования NAT? 
- Взаимно однозначное преобразование внутренних IP во внешние.
