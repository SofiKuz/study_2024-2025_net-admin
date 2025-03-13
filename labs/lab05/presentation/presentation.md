---
## Front matter
lang: ru-RU
title: Лабораторная работа №5
subtitle: Конфигурирование VLAN
author:
  - Кузнецова С. В.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 12 марта 2025

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

  * Кузнецова София Вадимона
  * Российский университет дружбы народов

# Ход работы

## Новый проект lab_PT-05.pkt

![Открытие проекта lab_PT-05.pkt](image/1.png){#fig:001 width=70%}

## Настройка Trunk-порта.

![Настройка Trunk-портов на коммутаторе msk-donskaya-svkuznecova-sw-1](image/2.png){#fig:002 width=40%}

## Настройка Trunk-порта.

![Настройка Trunk-портов на коммутаторе msk-donskaya-svkuznecova-sw-2](image/3.png){#fig:003 width=30%}

## Настройка Trunk-порта.

![Настройка Trunk-портов на коммутаторе msk-donskaya-svkuznecova-sw-3](image/4.png){#fig:004 width=30%}

## Настройка Trunk-порта.

![Настройка Trunk-портов на коммутаторе msk-donskaya-svkuznecova-sw-4](image/5.png){#fig:005 width=30%}

## Настройка Trunk-порта.

![Настройка Trunk-портов на коммутаторе msk-pavlovskaya-svkuznecova-sw-1](image/6.png){#fig:006 width=30%}

![Настройка Trunk-портов на коммутаторе msk-pavlovskaya-svkuznecova-sw-1](image/7.png){#fig:007 width=30%}

## Настройка коммутатора как VTP-сервер и пропишем на нём номера и названия

![Настройка коммутатора msk-donskaya-svkuznecova-sw-1 как VTP-сервер добавление номера и название VLAN](image/8.png){#fig:008 width=30%}

## Настройка коммутатора как VTP-клиенты и указание принадлежности к VLAN

![Настройка коммутатора msk-donskaya-svkuznecova-sw-2 как VTP-клиента и указание принадлежности к VLAN](image/9.png){#fig:009 width=40%}

## Настройка коммутатора как VTP-клиенты и указание принадлежности к VLAN

![Настройка коммутатора msk-donskaya-svkuznecova-sw-3 как VTP-клиента и указание принадлежности к VLAN](image/10.png){#fig:010 width=40%}


## Настройка коммутатора как VTP-клиенты и указание принадлежности к VLAN

![Настройка коммутатора msk-donskaya-svkuznecova-sw-4 как VTP-клиента и указание принадлежности к VLAN](image/11.png){#fig:011 width=30%}


## Настройка коммутатора как VTP-клиенты и указание принадлежности к VLAN

![Настройка коммутатора msk-pavlovskaya-svkuznecova-sw-1 как VTP-клиента и указание принадлежности к VLAN](image/12.png){#fig:012 width=60%}

## Cтатический IP-адрес на оконечных устройствах

![Пример указания статического IP-адреса на оконечном устройстве(Default Gateway)](image/13.png){#fig:013 width=40%}

## Cтатический IP-адрес на оконечных устройствах

![Пример указания статического IP-адреса на оконечном устройстве(IP Configuration)](image/14.png){#fig:014 width=40%}

## Команда ping 

![Проверка доступности устройства  Paket Tracer, принадлежащих одному VLAN, и недоступность устройств, принадлежащих разным VLAN](image/15.png){#fig:015 width=40%}

## Команда ping 

![Проверка доступности устройства  Paket Tracer, принадлежащих одному VLAN, и недоступность устройств, принадлежащих разным VLAN](image/16.png){#fig:016 width=40%}

## Режим симуляции в Packet Tracer

![Изучение процесса передвижения пакета ICMP по сети и режиме симуляции Packet Tracer](image/17.png){#fig:017 width=60%}

## Вывод

При выполнении лабораторной работы были получены основные навыки по настройке VLAN на коммутаторах сети.

## {.standout}

Спасибо за внимание!
