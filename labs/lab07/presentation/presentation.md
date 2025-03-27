---
## Front matter
lang: ru-RU
title: Лабораторная работы №7
subtitle: Учёт физических параметров сети
author:
  - Кузнецова С. В.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 27 марта 2025

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
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
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

![Создание нового проекта](image/1.png){#fig:001 width=80%}

## Физическая рабочая область Packet Tracer. Город — Moscow

![Открытие физической рабочей области Packet Tracer и присвоим названия городу](image/2.png){#fig:002 width=60%}

## Здание Donskaya. Здание Pavlovskaya

![Присвоение зданию названия Donskaya и добавление здания для территории Pavlovskaya](image/3.png){#fig:003 width=80%}

## Серверное помещение

![Перемещение изображения, обозначающее серверное помещение, внутрь здания](image/4.png){#fig:004 width=50%}

## Серверные стойки. Перенос коммутатора и двух оконечных устройства на территорию Pavlovskaya

![Перемещение коммутатора msk-pavlovskaya-svkuznecova-sw-1 на территорию Pavlovskaya](image/5.png){#fig:005 width=40%}

![Перемещение оконечных устройства dk-pavlovskaya-1 и other-pavlovskaya-1 на территорию Pavlovskaya](image/6.png){#fig:006 width=40%}

## Проверка работоспособности соединения

![Пинг с коммутатора msk-donskaya-svkuznecova-sw-1 коммутатор msk-pavlovskaya-svkuznecova-sw-1 (проверка работоспособности соединения)](image/7.png){#fig:007 width=70%}

## Enable Cable Length Effects

![Активация разрешения на учёт физических характеристик среды передачи](image/8.png){#fig:008 width=70%}

## Размещение двух территорий на расстоянии более 100 м друг от друга

![Размещение двух территории на расстоянии более 100 м друг от друга](image/9.png){#fig:009 width=70%}

## Проверка неработоспособности соединения

![Пинг с коммутатора msk-donskaya-svkuznecova-sw-1 коммутатор msk-pavlovskaya-svkuznecova-sw-1(проверка неработоспособности соединения)](image/10.png){#fig:010 width=80%}

## Добавление двух повторителей (Repeater-PT). Замена имеющихся модулей на PT-REPEATER- NM-1FFE и PT-REPEATER-NM-1CFE

![Добавление в логическую рабочую область два повторителя (Repeater-PT)](image/11.png){#fig:011 width=30%}

![Замена имеющиеся модули на PT-REPEATER- NM-1FFE и PT-REPEATER-NM-1CFE](image/12.png){#fig:012 width=40%}

## Перенос msk-pavlovskaya-svkuznecova-mc-1 на территорию Pavlovskaya

![Перемещение msk-pavlovskaya-svkuznecova-mc-1 на территорию Pavlovskaya](image/13.png){#fig:013 width=70%}

## Подключение коммутаторов 

![Подключение коммутаторов](image/14.png){#fig:014 width=70%}

## Проверка работоспособности соединения

![Пинг с коммутатора msk-donskaya-svkuznecova-sw-1 коммутатор msk-pavlovskaya-svkuznecova-sw-1(проверка работоспособности соединения)](image/15.png){#fig:015 width=80%}

# Выводы

В ходе выполнения лабораторной работы мы получили навыки работы с физической рабочей областью Packet Tracer, а также научились учитывать физические параметры сети.

## {.standout}

Спасибо за внимание!

