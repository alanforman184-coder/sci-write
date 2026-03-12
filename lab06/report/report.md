---
## Front matter
title: "Отчёт по лабораторной работе №6"
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

Изучение возможностей LaTeX по управлению библиографическими ссылками с использованием пакета `natbib`.

# Ход выполнения

## Компиляция исходного файла

На первом этапе был открыт исходный файл `bibliography_natbib.tex` и выполнена его компиляция с помощью команды `pdflatex`. Для корректного отображения ссылок потребовалось несколько компиляций: pdflatex, затем biber, затем pdflatex.

![Компиляция bibliography_natbib.tex](image/01.png)

## База данных references.bib

Была создана внешняя база данных в формате `.bib` с именем `references.bib`, содержащая четыре источника различных типов: статья, книга, материалы конференции и интернет-ресурс.

![Содержание файла references.bib](image/02.png)

## Анализ сгенерированного документа

### Титульный лист и цель работы

![Титульный лист и цель работы](image/03.png)

На первой странице представлены титульный лист с названием работы, автором и датой, а также цель работы — изучение управления библиографическими ссылками.

### Текстовое цитирование (citet)

![Текстовое цитирование](image/04.png)

С помощью команды `\citet` реализовано текстовое цитирование, где имена авторов являются частью предложения. Например: "Smith и др. показали, что LaTeX улучшает качество научных работ."

### Цитирование в скобках (citep)

![Цитирование в скобках](image/05.png)

Команда `\citep` используется для цитирования в скобках, когда ссылка находится в конце предложения. Например: "Как показано в исследованиях (Ivanov и др., 2023)."

### Цитирование с указанием страниц и множественное цитирование

![Цитирование со страницами и множественное цитирование](image/06.png)

Пакет `natbib` позволяет добавлять номера страниц в квадратные скобки: `\citet[p.~45]{smith2023}`. Также поддерживается множественное цитирование: `\citep{smith2023,latex2024,konference2023}`.

### Список литературы

![Список литературы](image/07.png)

В конце документа автоматически сгенерирован список литературы с использованием стиля `plainnat`. Все цитированные источники отображаются в алфавитном порядке.

## Процесс компиляции с библиографией

Для корректной работы с библиографией необходимо выполнить следующую последовательность команд:

1. `pdflatex bibliography_natbib.tex` - первая компиляция
2. `biber bibliography_natbib` - обработка библиографии
3. `pdflatex bibliography_natbib.tex` - вторая компиляция
4. `pdflatex bibliography_natbib.tex` - третья компиляция для финального результата

# Вывод

В ходе выполнения лабораторной работы были изучены основные возможности управления библиографией в LaTeX с помощью пакета `natbib`:

- создание базы данных `.bib` с различными типами источников;
- текстовое цитирование с помощью команды `\citet`;
- цитирование в скобках с помощью команды `\citep`;
- цитирование с указанием страниц;
- множественное цитирование;
- генерация списка литературы с использованием стиля `plainnat`;
- последовательность компиляции для корректного отображения ссылок.

Все файлы были успешно скомпилированы, полученный PDF-документ полностью соответствует ожидаемым результатам.