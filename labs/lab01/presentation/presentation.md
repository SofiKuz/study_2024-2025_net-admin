---
## Front matter
lang: ru-RU
title: Лабораторная работы №1
subtitle: Знакомство с Cisco PacketTracer
author:
  - Кузнецова С. В.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 14 февраля 2025

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

## Создание нового проекта lab_PT-01.pkt

![Создание нового проекта](image/1.png){ #fig:001 width=35% }

## Концентратор (Hub-PT-svkuznecova) и четыре оконечных устройства PC-svkuznecova

![Размещение концентратора и четырёх оконечных устройств](image/2.png){ #fig:002 width=20% }

![Присвоение статического IP-адреса и маски подсети](image/3.png){ #fig:003 width=20% }

## <<Add Simple PDU (P)>>

![Переход из режима реального времени в режим моделирования](image/4.png){ #fig:004 width=25% }

![<<Add Simple PDU (P)>>](image/5.png){ #fig:005 width=25% }

![Появление в рабочей области двух конвертов, обозначающих пакеты](image/6.png){ #fig:006 width=20% }

## <<Add Simple PDU (P)>>

![Появление двух событий на панели моделирования, относящихся к пакетам ARP и ICMP](image/7.png){ #fig:007 width=20% }

![Нажатие на панели моделирования кнопки <<Play>> и отслеживание движений пакетов ARP и ICMP](image/8.png){ #fig:008 width=20% }

## Challenge Me

![Challenge Me - ответы на вопросы](image/9.png){ #fig:009 width=50% }

## Пакет ICMP
	
![Исследование структуры пакета ICNP](image/10.png){ #fig:010 width=35% }

## PDU
![Очистка списка событий, удалив сценарий соделирования](image/11.png){ #fig:011 width=10% }

![PC0-svkuznecova -> PC2-svkuznecova. PC2-svkuznecova -> PC0-svkuznecova](image/12.png){ #fig:012 width=10% }

![Просмотр в списке событий информации о PDU](image/13.png){ #fig:013 width=10% }

## Коммутатор и 4 оконечных устройства PC

![Размещение в рабочем пространстве коммутатора и 4 оконечных устройства PC. Соединение оконечных устройств с коммутатором прямым кабелем](image/14.png){ #fig:014 width=15% }

![Присвоение статического IP-адреса и маски подсети](image/15.png){ #fig:015 width=15% }

## Два пакета и два события

![Появление в рабочей области двух конвертов, обозначающих пакеты](image/16.png){ #fig:016 width=25% }

![Появление в списке событий на панели моделирования двух событий, относящихся к пакетам ARP и ICMP](image/17.png){ #fig:017 width=25% }

## PC4-> PC6. PC6 -> PC4

![PC4-> PC6. PC6 -> PC4](image/18.png){ #fig:018 width=50% }

## Кроссовый кабель концентратора и коммутатора

![Соединение в рабочем пространстве кроссовым кабелем концентратора и коммутатора](image/19.png){ #fig:019 width=30% }

![PC0-> PC4. PC4 -> PC0](image/20.png){ #fig:020 width=30% }

## STP

![Исследование структуры STP](image/21.png){ #fig:021 width=50% }

## Маршрутизатора Cisco 2811

![Добавление в рабочем пространстве маршрутизатора Cisco 2811 и соединие прямым кабелем коммутатора и маршрутизатора](image/22.png){ #fig:022 width=20% }

![Присвоение статического IP-адрес 192.168.1.254 с маской 255.255.255.0, активация порта](image/23.png){ #fig:023 width=20% }

## CDP
    	   	
![PC-svkuznecova-> маршрутизатор](image/24.png){ #fig:024 width=30% }
	
![Исследование структуры пакета CDP](image/25.png){ #fig:025 width=30% }

# Выводы

В ходе выполнения лабораторной работы были приобретены практические навыки установки инструмента моделирования конфигурации сети Cisco Packet Tracer [3], знакомство с его интерфейсом.

## {.standout}

Спасибо за внимание!

