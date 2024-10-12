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
**Базовые сведения о Markdown**
Чтобы создать заголовок, используйте знак #, например:
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
Чтобы задать для текста полужирное начертание, заключите его в двойные звездочки:
This text is **bold**.
Чтобы задать для текста курсивное начертание, заключите его в одинарные звездочки:
This text is *italic*.
Чтобы задать для текста полужирное и курсивное начертание, заключите его в тройные
звездочки:
This is text is both ***bold and italic***.
Блоки цитирования создаются с помощью символа >:
> The drought had lasted now for ten million years, and the reign of the
↪terrible lizards had long since ended. Here on the Equator, in the
↪continent which would one day be known as Africa, the battle for existence
↪had reached a new climax of ferocity, and the victor was not yet in sight.
↪In this barren and desiccated land, only the small or the swift or the
↪fierce could flourish, or even hope to survive.

Упорядоченный список можно отформатировать с помощью соответствующих цифр:

1. First instruction
	1. Sub-instruction
	1. Sub-instruction
1. Second instruction

Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка:

1. First instruction
1. Second instruction
1. Third instruction

Неупорядоченный (маркированный) список можно отформатировать с помощью звездочек или тире:
* List item 1
* List item 2
* List item 3
Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка:
- List item 1
- List item A
- List item B
- List item 2
Синтаксис Markdown для встроенной ссылки состоит из части [link text], представляющей текст гиперссылки, и части (file-name.md) – URL-адреса или имени файла, на который
дается ссылка:
[link text](file-name.md)
или
[link text](http://example.com/ "Необязательная подсказка")
Markdown поддерживает как встраивание фрагментов кода в предложение, так и их размещение между предложениями в виде отдельных огражденных блоков. Огражденные блоки
кода — это простой способ выделить синтаксис для фрагментов кода. Общий формат огражденных блоков кода:

``` language
your code goes in here
```

**Оформление формул в Markdown**

Внутритекстовые формулы делаются аналогично формулам LaTeX. Например, формула
sin^2(𝑥) + cos^2(𝑥) = 1 запишется как
$\sin^2 (x) + \cos^2 (x) = 1$
Выключение формулы:
sin2(𝑥) + cos2(𝑥) = 1 (3.1)
со ссылкой в тексте «Смотри формулу ({-eq. 3.1}).» записывается как
$$
\sin^2 (x) + \cos^2 (x) = 1
$$ {#eq:eq1}
Смотри формулу (`[-@eq:eq1]`).

**Оформление изображений в Markdown**
В Markdown вставить изображение в документ можно с помощью непосредственного
указания адреса изображения. Синтаксис данной команды выглядит следующим образом:
![Подпись к рисунку](/путь/к/изображению.jpg "Необязательная подсказка"){
↪ #fig:fig1 width=70% }
Здесь:
• в квадратных скобках указывается подпись к изображению;
• в круглых скобках указывается URL-адрес или относительный путь изображения, а также (необязательно) всплывающую подсказку, заключённую в двойные или одиночные
кавычки.
• в фигурных скобках указывается идентификатор изображения (#fig:fig1) для ссылки
на него по тексту и размер изображения относительно ширины страницы (width=90%)
Ссылка на изображение (рис. 3.1) может быть оформлена следующим образом (рис. [-
@fig:fig1])

**Обработка файлов в формате Markdown**

Преобразовать файл README.md можно следующим образом:
pandoc README.md -o README.pdf

или так

pandoc README.md -o README.docx

Для компиляции отчетов по лабораторным работам предлагается использовать следующий Makefile

```
FILES = $(patsubst %.md, %.docx, $(wildcard *.md))
FILES += $(patsubst %.md, %.pdf, $(wildcard *.md))
LATEX_FORMAT =
FILTER = --filter pandoc-crossref
%.docx: %.md
-pandoc "$<" $(FILTER) -o "$@"
%.pdf: %.md
-pandoc "$<" $(LATEX_FORMAT) $(FILTER) -o "$@"
all: $(FILES)
@echo $(FILES)
clean:
-rm $(FILES) *~
```

# Выполнение лабораторной работы

Для начала перейдем в каталог, сформированный при выполнении лабораторной работы №2 и скачаем изменения из удаленного репозитория с помощью команды(рис [-@fig:001]):

![Обновлние локального репозитория](Снимок экрана от 2024-09-29 01-10-28.png){#fig:001 width=70%}

Далее перейдем в каталог с шаблоном отчета по лабораторной работы № 3 и сгенерируем файлы report.pdf и report.docx, затем удалим их.(рис. [-@fig:002])

![Компиляцию шаблона с использованием Makefile и удаление полученных данных.](Снимок экрана от 2024-10-09 21-01-55.png){#fig:002 width=70%}

Затем откроем файл report.md с помощью текстового редактора gedit, заполним отчет и скомпелируем его.(рис. [-@fig:003])

![Открытие файла report.md](Снимок экрана от 2024-10-09 21-08-21.png){#fig:003 width=70%}

Перейдем в ветку с соответствующимися файлами и перенесем изменения из рабочего каталога в раздел проиндексированных файлов и сделаем снимок текущего состояния изменений.(рис [-@fig:004])

![Перенос изменений и снимок текущего состояния](Снимок экрана от 2024-10-09 21-11-09.png){#fig:004 width=70%}

В заключение, отправим локальную ветку в удаленный репозиторий.(рис. [-@fig:005])

![Загрузка файлов на GitHub](Снимок экрана от 2024-10-09 21-13-04.png){#fig:005 width=70%}

**Приступим к выполнению самостоятельной работы.**

Перейдем в каталог с шаблоном отчета по лабораторной работе №2 и откроем файл report.md с помощью текстового редактора.(рис. [-@fig:006])

![Открытие файла с шаблоном отчета](Снимок экрана от 2024-10-12 19-22-42.png){#fig:006 width=70%}

Затем загрузим файлы на Github(рис. [-@fig:007])

![Открытие файла с шаблоном отчета](Снимок экрана от 2024-10-12 19-22-42.png){#fig:007 width=70%}

# Выводы

В ходе работы была освоена процедура оформления отчетов с использованием легковесного языка разметки Markdown.освоение Markdown не только повысило навыки работы с текстовой разметкой, но и обеспечило понимание принципов создания структурированных и профессионально оформленных документов.

# Список литературы{.unnumbered}

::: {#refs}
:::
