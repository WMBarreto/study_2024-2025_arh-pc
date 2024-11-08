---
## Front matter
title: "Oтчёт по лабораторной работе №5"
subtitle: "Основы работы с Midnight Commander (mc)"
author: "Барето Вилиан Мануел"

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

Приобретение практических навыков работы в Midnight Commander. Освоение инструкций языка ассемблера mov и int.

# Задание

Здесь приводится описание задания в соответствии с рекомендациями
методического пособия и выданным вариантом.

# Теоретическое введение

Здесь описываются теоретические аспекты, связанные с выполнением работы.

Например, в табл. [-@tbl:std-dir] приведено краткое описание стандартных каталогов Unix.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |

Более подробно про Unix см. в [@tanenbaum_book_modern-os_ru; @robbins_book_bash_en; @zarrelli_book_mastering-bash_en; @newham_book_learning-bash_en].

# Выполнение лабораторной работы

## Порядок выполнения лабораторной работы

 Откройте Midnight Commander. (рис. [-@fig:001]).

![Вводим в консоль команду mc](image/1.png){#fig:001 width=70%}

Перейдите в каталог, созданный при выполнении лабораторной работы №4.(рис. [-@fig:002])

![Переходим в каталог](image/2.png){#fig:002 width=70%}

Создаем папку lab05 и перейдите в созданный каталог.(рис. [-@fig:003])

![Создаем каталог функциональной клавишей F7](image/3.png){#fig:003 width=70%}

Создаем файл lab5-1.asm.(рис. [-@fig:004])

![Воспользуемся командой touch](image/4.png){#fig:004 width=70%}

Открываем файл для редактирования и заполняем его по листингу.(рис. [-@fig:005])

![Открываем файл редактированой клавишей, заполняем и сохраняем](image/5.png){#fig:005 width=70%}

Транслируем текст программы и запускаем исполняемый файл.(рис. [-@fig:006])

![Проверяем, как работает данная программа](image/6.png){#fig:006 width=70%}

Скачиваем файл со страницы курса.(рис. [-@fig:007])

![Скачиваем файл](image/7.png){#fig:007 width=70%}

Копируем файл в нужную директоию (рис. [-@fig:008]).

![Копируем Скаченный файл](image/8.png){#fig:008 width=70%}

Создаем Копию файла lab5-1.asm (рис. [-@fig:009]).

![Создаем Копию файла клавишей F6](image/9.png){#fig:009 width=70%}

Проверяем созданный файл (рис. [-@fig:010]).

![Проверяем скопировался ли файл](image/10.png){#fig:010 width=70%}

Открываем новый файл и заполняем его в соответствии с листингом (рис. [-@fig:011]).

![Открываем и заполняем файл](image/11.png){#fig:011 width=70%}

Транслируем и запускаем новый файл (рис. [-@fig:012]).

![Смотрим, как работала программа](image/12.png){#fig:012 width=70%}

Снова открываем файл для редактированния и меняем sprintLF на sprint (рис. [-@fig:013]).

![Редактируем файл](image/13.png){#fig:013 width=70%}

Транслируем и запускаем файл (рис. [-@fig:014]).

![Смотрим, как работала программа и сравниваем с прошлой](image/14.png){#fig:014 width=70%}

Таким образом можем понять, что команда sprint выводит текст в той же строке, а sprintLF переносит на новую строку.

## Задание для самостоятельной работы

Создаем копию файла lab5-1.asm и называем его также (рис. [-@fig:015]).

![Создаем копию файла lab5-1.asm](image/15.png){#fig:015 width=70%}

Редактируем файл, чтобы введеный текст с клавиатуры выводился в консоль (рис. [-@fig:016]).

![Редактируем файл](image/16.png){#fig:016 width=70%}

Транслируем файл и запускаем программу (рис. [-@fig:017]).

![Проверяем правильность написания программы](image/17.png){#fig:017 width=70%}

    
# Выводы
 Мы приобрели навыки работы с Midnight Commander и освоили инструкцию
mov.


