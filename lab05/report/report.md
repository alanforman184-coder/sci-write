---
## Front matter
title: "Отчёт по лабораторной работе №5"
subtitle: "Computer Skills for Scientific Writing"
author: "Сунь Маосин"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Pdf output format
toc: true
toc-depth: 2
lof: true
lot: true
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
mainfont: Times New Roman
romanfont: Times New Roman
sansfont: Arial
monofont: Courier New
mathfont: Times New Roman
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
  - \usepackage{float}
  - \floatplacement{figure}{H}
---

# Цель работы

Изучение возможностей LaTeX по созданию и форматированию таблиц.

# Ход выполнения

## Компиляция исходного файла

На первом этапе был открыт исходный файл `tables.tex` и выполнена его компиляция командой `pdflatex`. В процессе компиляции использовался дистрибутив **TeX Live 2026** и пакеты для работы с таблицами.

![Компиляция tables.tex](image/01.png)

## Анализ сгенерированного документа

Сформированный PDF-файл содержит несколько страниц, демонстрирующих различные способы создания и форматирования таблиц в LaTeX.

### Титульный лист и простые таблицы

![Титульный лист и простые таблицы](image/02.png)

На первой странице представлены титульный лист и простые таблицы с использованием окружения `tabular`.

### Таблицы с пакетом booktabs

![Таблицы с booktabs](image/03.png)

Пакет `booktabs` создаёт профессионально выглядящие таблицы с помощью команд `toprule`, `midrule`, `bottomrule` и различных видов линий.

### Объединение ячеек

![Объединение ячеек](image/04.png)

С помощью команд `multicolumn` и `multirow` реализовано горизонтальное и вертикальное объединение ячеек.

### Комбинация объединений и фиксированная ширина

![Комбинация объединений и тип p](image/05.png)

Комбинация горизонтального и вертикального объединения, а также столбцы с фиксированной шириной типа `p`.

### Вертикальное выравнивание и пользовательские типы

![Типы m, b и пользовательские типы](image/06.png)

Столбцы с вертикальным выравниванием по центру (m) и по низу (b), а также пользовательские типы с изменением шрифта.

### Числовое выравнивание с siunitx

![Числовое выравнивание](image/07.png)

Пакет `siunitx` выравнивает числа по десятичной точке с помощью типа столбца `S`.

### Таблицы с фиксированной шириной (tabularx)

![Таблицы tabularx](image/08.png)

Пакет `tabularx` позволяет задать общую ширину таблицы с гибкими столбцами типа `X`.

### Многостраничные таблицы (longtable)

![Многостраничные таблицы longtable](image/09.png)

Пакет `longtable` используется для создания таблиц, занимающих несколько страниц.

### Таблицы с примечаниями, цветные таблицы и вывод

![Таблицы с примечаниями, цветные таблицы и вывод](image/10.png)

- Пакет `threeparttable` добавляет сноски к таблицам
- Пакет `xcolor` создаёт чередование цветов строк
- Заключительный вывод со списком изученных возможностей

# Вывод

В ходе выполнения лабораторной работы были изучены:

- создание простых таблиц с помощью окружения `tabular`;
- использование пакетов `array`, `booktabs`, `siunitx`, `tabularx`, `multirow`, `threeparttable`, `longtable`;
- объединение ячеек по горизонтали и вертикали;
- столбцы с фиксированной шириной;
- числовое выравнивание по десятичной точке;
- таблицы с заданной общей шириной;
- многостраничные таблицы;
- таблицы с примечаниями;
- цветное оформление таблиц.

Все файлы были успешно скомпилированы, полученный PDF-документ полностью соответствует ожидаемым результатам.