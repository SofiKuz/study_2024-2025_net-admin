---
## Front matter
title: "Отчёт по лабораторной работе №1"
subtitle: "дисциплина: Основы информационной безопасности"
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
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
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
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Выполнение лабораторной работы

Произведём скачивание и установку виртуальной машины через сайт: https://www.virtualbox.org/.

![Скачивание виртуальной машины](image/1.png){ #fig:001 width=70% }

Следующим шагом нужно скачать дистрибутив Linux Rocky, воспользовавшись сайтом: https://rockylinux.org/download/. 

![Скачивание дистрибутива Linux Rocky](image/2.png){ #fig:002 width=70% }

Создаём новую виртуальную машину: в VirtualBox выберите Машина Создать. Указываем имя виртуальной машины, тип операционной системы — Linux, версию операционной системы — RedHat (64-bit). Указываем путь к iso-образу устанавливаемого дистрибутива, отмечаем «Пропустить автоматическую установку».
    	   	
![Окно «Имя и операционная система виртуальной машины», путь к iso-образу](image/3.png){ #fig:003 width=70% }

Указываем размер основной памяти виртуальной машины 4096 МБ и число процессоров 2.
	
![Окно «Оборудование»](image/4.png){ #fig:004 width=70% }

Задаём размер виртуального жёсткого диска – 40ГБ.
	
![Окно «Виртуальный жёсткий диск»](image/5.png){ #fig:005 width=70% }

После выставления всех требуемых параметров нужно запустить виртуальную машину. 

![Запуск виртуальной машины](image/6.png){ #fig:006 width=70% }

Устанавливаем Rocky Linux 9.2.

![Установка Rocky Linux 9.2](image/7.png){ #fig:007 width=70% }

Переходим к настройкам установки операционной системы и выбираем английский язык для интерфейса.

![Установка английского языка интерфейса ОС](image/8.png){ #fig:008 width=70% }

При выборе места установки оставляем параметры, которые были выставлены автоматически. 

![Окно настройки установки: место установки](image/9.png){ #fig:009 width=70% }

В разделе выбора программ указываем в качестве базового окружения Server with GUI , а в качестве дополнения — Development Tools.

![Окно настройки установки: выбор программ](image/10.png){ #fig:010 width=70% }

Отключаем KDUMP.

![Окно настройки установки: отключение KDUMP](image/11.png){ #fig:011 width=70% }

Включаем сетевое соединение и в качестве имени узла указываем svkuznecova.localdomain.

![Окно настройки установки: сеть и имя узла](image/12.png){ #fig:012 width=70% }

Скорректируем раскладку клавиатуры (добавим русский язык, но в качестве языка по умолчанию укажем английский язык; зададим комбинацию клавиш для переключения между раскладками клавиатуры - Alt + Shift ). 
    	   	
![Окно настройки установки: язык клавиатуры и горячие клавиши](image/13.png){ #fig:013 width=70% }

Устанавливаем пароль для root и пользователя с правами администратора.
	
![Установка пароля для root](image/14.png){ #fig:014 width=70% }

Начинаем процесс установки ОС.

![Установка ОС](image/15.png){ #fig:015 width=70% }

Дожидаемся и завершаем установку. После успешной установки выполняем перезагрузку системы. Последним пунктом нашей лабораторнойработы становится подключение образа диска Дополнительной гостевой ОC. 

![Подключение образа диска Дополнительной гостевой ОС](image/16.png){ #fig:016 width=70% }

# Выводы

В ходе выполнения лабораторной работы были приобретены практические навыки установки операционной системы на виртуальную машину и настройки минимально необходимых для дальнейшей работы.
