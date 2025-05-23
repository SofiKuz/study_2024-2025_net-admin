---
## Front matter
lang: ru-RU
title: Лабораторная работа №12
subtitle: Настройка NAT
author:
  - Кузнецова С. В.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 26 апреля 2025

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Кузнецова София Вадимовна
  * Российский университет дружбы народов

:::
::: {.column width="30%"}


:::
::::::::::::::

# Ход работы

## Создание нового проекта lab_PT-11.pkt

![Создание нового проекта](image/1.png){ #fig:001 width=80% }

## Первоначальная настройка маршрутизатора provider-svkuznecova-gw-1 провайдера (зададим имя, настроим доступ по паролю и т.п.)

![Первоначальная настройка маршрутизатора provider-svkuznecova-gw-1](image/2.png){#fig:002 width=70%}

## Первоначальная настройка коммутатора provider-svkuznecova-sw-1 провайдера (зададим имя, настроим доступ по паролю и т.п.)

![Первоначальная настройка коммутатора provider-sckuznecova-sw-1](image/3.png){#fig:003 width=70%}

## Настройка интерфейса маршрутизатора provider-svkuznecova-gw-1 провайдера

![Настройка интерфейсов маршрутизатора provider-svkuznecova-gw-1](image/4.png){#fig:004 width=50%}

## Настройка интерфейса коммутатора provider-svkuznecova-sw-1 провайдера

![Настройка интерфейсов коммутатора provider-svkuznecova-sw-1](image/5.png){#fig:005 width=50%}

## Проверка

![Проверка командой ping с сервера www.rudn.ru на роутер провайдера](image/6.png){#fig:006 width=70%}

## Настройка интерфейсов маршрутизатора сети «Донская» для доступа к сети провайдера

![Настройка интерфейсов маршрутизатора msk-donskaya-svkuznecova-gw-1 для доступа к сети провайдера](image/7.png){#fig:007 width=50%}

## Проверка

![Выполнение проверки](image/8.png){#fig:008 width=70%}

## Настройка на маршрутизаторе сети «Донская» NAT с правилами, указанными в лабораторной работе

![Настройка пула адресов для NAT](image/9.png){#fig:009 width=70%}

## Настройка на маршрутизаторе сети «Донская» NAT с правилами, указанными в лабораторной работе

![Настройка списка доступа для NAT](image/10.png){#fig:010 width=70%}

## Настройка на маршрутизаторе сети «Донская» NAT с правилами, указанными в лабораторной работе

![Сеть дисплейных классов(имеют доступ только к сайтам, необходимым для учёбы (www.yandex.ru (192.0.2.11), stud.rudn.university (192.0.2.12))](image/11.png){#fig:011 width=70%}

## Настройка на маршрутизаторе сети «Донская» NAT с правилами, указанными в лабораторной работе

![Сеть кафедр (работает только с образовательными сайтами (esystem.pfur.ru (192.0.2.13)))](image/12.png){#fig:012 width=70%}

## Настройка на маршрутизаторе сети «Донская» NAT с правилами, указанными в лабораторной работе

![Сеть администрации (имеет возможность работать только с сайтом университета (www.rudn.ru (192.0.2.14)))](image/13.png){#fig:013 width=70%}

## Настройка на маршрутизаторе сети «Донская» NAT с правилами, указанными в лабораторной работе

![Доступ для компьютера администратора (в сети для других пользователей компьютер администратора имеет полный доступ в Интернет. Другие не имеют доступа.)](image/14.png){#fig:014 width=70%}

## Настройка на маршрутизаторе сети «Донская» NAT с правилами, указанными в лабораторной работе

![Настройка NAT (Port Address Translation и интерфейсов для NAT)](image/15.png){#fig:015 width=60%}

## Проверка работоспособности

![Проверка](image/16.png){#fig:016 width=40%}

## Проверка работоспособности

![Проверка](image/17.png){#fig:017 width=70%}

## Настройка доступа из внешней сети в локальную сеть организации, как указано в лабораторной работе

![Настройка доступа из Интернета (WWW-сервер)](image/18.png){#fig:018 width=70%}

## Настройка доступа из внешней сети в локальную сеть организации, как указано в лабораторной работе

![Настройка доступа из Интернета (файловый сервер)](image/19.png){#fig:019 width=70%}

## Настройка доступа из внешней сети в локальную сеть организации, как указано в лабораторной работе

![Настройка доступа из Интернета (почтовый сервер)](image/20.png){#fig:020 width=70%}

## Настройка доступа из внешней сети в локальную сеть организации, как указано в лабораторной работе

![Настройка доступа из Интернета (доступ по RDP)](image/21.png){#fig:021 width=70%}

## Проверка работоспособности

![Проверка](image/22.png){#fig:022 width=70%}

# Выводы

В ходе выполнения лабораторной работы мы приобрели практические навыки по настройке доступа локальной сети к внешней сети посредством NAT.

## {.standout}

Спасибо за внимание!
