---
## Front matter
lang: ru-RU
title: Лабораторная работа №14
subtitle: Статическая маршрутизация в Интернете. Настройка
author:
  - Кузнецова С. В.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 10 мая 2025

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

## Создание нового проекта lab_PT-14.pkt

![Создание нового проекта](image/1.png){ #fig:001 width=80% }

## Настройка линка между площадками

![Настройка интерфейсов коммутатора provider-svkuznecova-sw-1](image/2.png){#fig:002 width=40%}

## Настройка линка между площадками

![Настройка интерфейсов маршрутизатора msk-donskaya-svkuznecova-gw-1](image/3.png){#fig:003 width=55%}

## Настройка линка между площадками

![Настройка интерфейсов маршрутизатора msk-q42-svkuznecova-gw-1](image/4.png){#fig:004 width=55%}

## Настройка линка между площадками

![Настройка интерфейсов коммутатора sch-sochi-svkuznecova-sw-1](image/5.png){#fig:005 width=55%}

## Настройка линка между площадками

![Настройка интерфейсов маршрутизатора sch-sochi-svkuznecova-gw-1](image/6.png){#fig:006 width=55%}

## Настройка площадки 42-го квартала

![Настройка интерфейсов маршрутизатора msk-q42-svkuznecova-gw-1](image/7.png){#fig:007 width=40%}

## Настройка площадки 42-го квартала

![Настройка интерфейсов коммутатора msk-q42-svkuznecova-sw-1](image/8.png){#fig:008 width=55%}

## Настройка площадки 42-го квартала

![Настройка интерфейсов маршрутизирующего коммутатора msk-hostel-svkuznecova-gw-1](image/9.png){#fig:009 width=45%}

## Настройка площадки 42-го квартала

![Настройка интерфейсов коммутатора msk-hostel-svkuznecova-sw-1](image/10.png){#fig:010 width=50%}

## Настройка площадки в Сочи

![Настройка интерфейсов маршрутизатора sch-sochi-svkuznecova-gw-1](image/11.png){#fig:011 width=50%}

## Настройка площадки в Сочи

![Настройка интерфейсов коммутатора sch-sochi-svkuznecova-sw-1](image/12.png){#fig:012 width=55%}

## Настройка маршрутизации между площадками

![Настройка маршрутизатора msk-donskaya-svkuznecova-gw-1](image/13.png){#fig:013 width=65%}

## Настройка маршрутизации между площадками

![Настройка маршрутизатора msk-q42-svkuznecova-gw-1](image/14.png){#fig:014 width=70%}

## Настройка маршрутизации между площадками

![Настройка маршрутизатора sch-sochi-svkuznecova-gw-1](image/15.png){#fig:015 width=65%}

## Настройка маршрутизации на 42 квартале

![Настройка маршрутизатора msk-q42-svkuznecova-gw-1](image/16.png){#fig:016 width=65%}

## Настройка маршрутизации на 42 квартале

![Настройка интерфейсов маршрутизирующего коммутатора msk-hostel-svkuznecova-gw-1](image/17.png){#fig:017 width=60%}

## Настройка NAT на маршрутизаторе msk-donskaya-svkuznecova-gw-1

![Настройка NAT на маршрутизаторе msk-donskaya-svkuznecova-gw-1](image/18.png){#fig:018 width=55%}

# Выводы

В ходе выполнения лабораторной работы мы настроили взаимодействие через сеть провайдера посредством статической маршрутизации локальной сети организации с сетью основного здания, расположенного в 42-м квартале в Москве, и сетью филиала, расположенного в г. Сочи.

## {.standout}

Спасибо за внимание!
