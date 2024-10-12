---
## Front matter
title: "Отчёт по лабораторной работе №3"
subtitle: "Простейший вариант"
author: "Тимур Ринатович Каримов"

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

Целью работы является освоение процедуры оформления отчетов с помощью легковесного
языка разметки Markdown.

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

Для начала перейдем в каталог, сформированный при выполнении лабораторной работы №2 и скачаем изменения из удаленного репозитория с помощью команды(рис [-@fig:001]):

![Обновлние локального репозитория](image/Снимок экрана от 2024-09-29 01-10-28.jpg){#fig:001 width=70%}

Далее перейдем в каталог с шаблоном отчета по лабораторной работы № 3 и сгенерируем файлы report.pdf и report.docx, затем удалим их.(рис. [-@fig:002])

![Компиляцию шаблона с использованием Makefile и удаление полученных данных.](image/Снимок экрана от 2024-10-09 21-01-55.jpg){#fig:002 width=70%}

Затем откроем файл report.md с помощью текстового редактора gedit, заполним отчет и скомпелируем его.(рис. [-@fig:003])

![Открытие файла report.md](image/Снимок экрана от 2024-10-09 21-08-21.jpg){#fig:003 width=70%}

Перейдем в ветку с соответствующимися файлами и перенесем изменения из рабочего каталога в раздел проиндексированных файлов и сделаем снимок текущего состояния изменений.(рис [-@fig:004])

![Перенос изменений и снимок текущего состояния](image/Снимок экрана от 2024-10-09 21-11-09.jpg){#fig:004 width=70%}

В заключение, отправим локальную ветку в удаленный репозиторий.(рис. [-@fig:005])

![Загрузка файлов на GitHub](image/Снимок экрана от 2024-10-09 21-13-04.jpg){#fig:005 width=70%}

**Приступим к выполнению самостоятельной работы.**

Перейдем в каталог с шаблоном отчета по лабораторной работе №2 и откроем файл report.md с помощью текстового редактора.(рис. [-@fig:006])

![Открытие файла с шаблоном отчета](image/Снимок экрана от 2024-10-12 19-22-42.jpg){#fig:006 width=70%}

Перейдем в ветку с соответствующимися файлами и перенесем изменения из рабочего каталога в раздел проиндексированных файлов и сделаем снимок текущего состояния изменений.(рис [-@fig:007])

![Перенос изменений и снимок текущего состояния](image/Снимок экрана от 2024-10-12 21-35-24.jpg){#fig:007 width=70%}

В заключение, отправим локальную ветку в удаленный репозиторий.(рис. [-@fig:008])

![Загрузка файлов на GitHub](image/Снимок экрана от 2024-10-12 21-42-19.jpg){#fig:008 width=70%}

# Выводы

В ходе работы была освоена процедура оформления отчетов с использованием легковесного языка разметки Markdown.освоение Markdown не только повысило навыки работы с текстовой разметкой, но и обеспечило понимание принципов создания структурированных и профессионально оформленных документов.

# Список литературы{.unnumbered}

::: {#refs}
:::
