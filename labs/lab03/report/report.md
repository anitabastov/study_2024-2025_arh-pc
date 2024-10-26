---
## Front matter
title: "Лабораторная работа №3" 
subtitle: "Архитектура компьютера"
author: "Баштованович Анита"

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
Освоить процедуры оформления отчетов с помощью легковесного языка разметки Markdown.

# Задание

1. В соответствующем каталоге сделать отчёт по лабораторной работе №3 в формате Markdown. В качестве отчёта необходимо предоставить отчёты в 3 форматах: pdf, docx и md.
2. Загрузить файлы на github.

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

Описываются проведённые действия, в качестве иллюстрации даётся ссылка на иллюстрацию (рис. [-@fig:001]).
1. Откроем терминал
2. Перейдем в каталог курса сформированный при выполнении лабораторной работы №2[-@fig:001]

![Рис.1 переход в каталог](image/1.jpg){#fig:001 width=100%}

Обновим локальный репозиторий, скачав изменения из удаленного репозитория с помощью команды git pull[-@fig:002]

![Рис.2 команда git pull](image/2.jpg){#fig:002 width=100%}

3. Перейдем в каталог с шаблоном отчета по лабораторной работе № 3[-@fig:003]

![Рис.3 переход в каталог л.р.3](image/3.jpg){#fig:003 width=100%}

4. Проведем компиляцию шаблона с использованием Makefile. Для этого введем команду make. [-@fig:004]

![Рис.4 команда make](image/4.jpg){#fig:004 width=100%}

При успешной компиляции должны сгенерироваться файлы report.pdf и report.docx. Откроем и проверим корректность полученных файлов. [-@fig:005]

![Рис.5 проверка файлов](image/5.jpg){#fig:005 width=100%}

5. Удалим полученные файлы с использованием Makefile. Для этого введем команду make clean. Проверим, что после этой команды файлы report.pdf и report.docx были удалены.[-@fig:006]

![Рис.6 команда make clean](image/6.jpg){#fig:006 width=100%}

6. Откроем файл report.md c помощью любого текстового редактора, например gedit. Внимательно изучим структуру этого файла.[-@fig:007]

![Рис.7 команда gedit](image/7.jpg){#fig:007 width=100%}

7. Заполним отчет и скомпилируем отчет с использованием Makefile. Проверим корректность полученных файлов. (Обратим внимание, для корректного отображения
скриншотов они должны быть размещены в каталоге image)[-@fig:008]

![Рис.](){#fig:008 width=100%}

8. Загрузим файлы на Github.[-@fig:009]

![Рис.](){#fig:009 width=100%}


# Выводы
Я освоила процедуры оформления отчетов с помощью легковесного языка разметки Markdown


# Список литературы{.unnumbered}

::: {#refs}
:::
