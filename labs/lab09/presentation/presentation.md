---
## Front matter
lang: ru-RU
title: Лабораторная работы №9
subtitle: Использование протокола STP. Агрегирование каналов
author:
  - Кузнецова С. В.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 11 апреля 2025

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

## Создание нового проекта lab_PT-09.pkt

![Создание нового проекта](image/1.png){ #fig:001 width=80% }

## Резервное соединение между коммутаторами msk-donskaya-svkuznecova-sw-1 и msk-donskaya-svkuznecova-sw-3

![Резервное соединение](image/2.png){#fig:002 width=65%}

## Порт на интерфейсе Gig0/2 

![Транковый порт](image/3.png){#fig:003 width=40%}

## Теперь соединение между коммутаторами msk-donskaya-svkuznecova-sw-1 и msk-donskaya-svkuznecova-sw-4 сделаем через интерфейсы Fa0/23

![Соединение между коммутаторов через интерфейсы Fa0/23](image/4.png){#fig:004 width=55%}

## Транковый режим

![Активация в транковом режиме](image/5.png){#fig:005 width=50%}

## Транковый режим

![Активация в транковом режиме](image/6.png){#fig:006 width=50%}

## Пинг серверов mail и web

![Пинг](image/7.png){#fig:007 width=30%}

## Режим симуляции

![Режим симуляции](image/8.png){#fig:008 width=35%}

![Режим симуляции](image/9.png){#fig:009 width=35%}

## Информация, связанная с протоколом STP

![Cостояние протокола STP для vlan 3](image/10.png){#fig:010 width=50%}

## Корневой коммутатор STP 

![Корневой коммутатор](image/11.png){#fig:011 width=80%}

## Режим симуляции

![Режим симуляции](image/12.png){#fig:012 width=35%}

![Режим симуляции](image/13.png){#fig:013 width=35%}

## Режим Portfast 

![msk-donskaya-svkuznecova-sw-2](image/14.png){#fig:014 width=45%}

## Режим Portfast 

![msk-donskaya-svkuznecova-sw-3](image/15.png){#fig:015 width=45%}

## Отказоустойчивость протокола STP 

![Отказоустойчивость](image/16.png){#fig:016 width=35%}

![Отказоустойчивость](image/17.png){#fig:017 width=35%}

## Режим работы по протоколу Rapid PVST+

![Протокол Rapid PVST+](image/18.png){#fig:018 width=80%}

## Отказоустойчивость протокола Rapid PVST+ 

![Отказоустойчивость](image/19.png){#fig:019 width=35%}

![Отказоустойчивость](image/20.png){#fig:020 width=35%}

## Агрегированное соединение интерфейсов 

![Агрегированное соединение интерфейсов](image/21.png){#fig:021 width=70%}

## Агрегированное соединение интерфейсов 

![msk-donskaya-svkuznecova-sw-1](image/22.png){#fig:022 width=35%}

## Агрегированное соединение интерфейсов 

![msk-donskaya-svkuznecova-sw-4](image/23.png){#fig:023 width=35%}

# Выводы

В ходе выполнения лабораторной работы изучила возможности протокола STP и его модификаций по обеспечению отказоустойчивости сети, агрегированию интерфейсов и перераспределению нагрузки между ними.

## {.standout}

Спасибо за внимание!
