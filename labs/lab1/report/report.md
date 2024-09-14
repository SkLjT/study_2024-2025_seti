---
## Front matter
title: "Лабораторная работа 1" 
subtitle: "Методы кодирования и модуляция сигналов"
author: "Лушин Артём Андреевич"

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
biblatex: false
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

Изучение методов кодирования и модуляции сигналов с помощью высокоуровнего языка программирования Octave. Определение спектра и параметров сигнала. Демонстрация принципов модуляции сигнала на примере аналоговой амплитудной модуляции. Исследование свойства самосинхронизации сигнала.

# Выполнение лабораторной работы

1) Я создал и сохранил файл plot_sin.m. В этом файле написал код, чтобы построить функцию. После исполнения кода вывелся график. 

![Код plot_sin.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/1.jpg){#fig:001 width=70%}

![График plot_sin.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/2.jpg){#fig:002 width=70%}

2) Создали новый файл и написал код, который основыватся на коде из прошлого пункта, но добавляет и функцию с косинусом. Сгенерировал рисунок. 

![Код plot_combo.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/3.jpg){#fig:003 width=70%}

![Рисунок plot_combo.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/4.jpg){#fig:004 width=70%}

3) Создал новый файл meandr для реализации графики меандра, реализованный с различным количеством гармоник. Реализовывал через косинусы.

![Код meandr.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/5.jpg){#fig:005 width=70%}

![Рисунок meandr.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/6.jpg){#fig:006 width=70%}

4) Изменил код файла meandr, чтобы он реализовывался через синусы. 

![Код изменённого meandr.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/7.jpg){#fig:007 width=70%}

![Рисунок изменённого meandr.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/8.jpg){#fig:008 width=70%}

5) Создал новый каталог spectre1, а в нём файл spectre.m. Файл будет определять спектр двух отдельных сигналов и их сумму. 

![Код spectre.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/9.jpg){#fig:009 width=70%}

![Рисунок spectre.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/10.jpg){#fig:010 width=70%}

6) Затем изменил код файла spectre, чтобы он использовал преобразования Фурье.

![Код spectre.m с Фурье](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/11.jpg){#fig:011 width=70%}

![Рисунок spectre.m с Фурье](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/12.jpg){#fig:012 width=70%}

7) Я улучшил график преобразования Фурье, чтоб он отбрасывал дублирующие отрицательные частоты.

![Код spectre.m с улучшенным Фурье](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/13.jpg){#fig:013 width=70%}

![Рисунок spectre.m с улучшенным Фурье](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/14.jpg){#fig:014 width=70%}

8) Я создал каталог spectr_sum и в нём создал файл spectre_sum.m. Вписал следующий код и на выходе доказал, что спектр сумм сигналов равен сумме спектров сигнала.

![Код spectre_sum.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/15.jpg){#fig:015 width=70%}

![Рисунок spectre_sum.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/16.jpg){#fig:016 width=70%}

![Рисунок2 spectre_sum.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/17.jpg){#fig:017 width=70%}

9) Создал каталог modulation, а внутри создал файл am. Этот код нам показывает, что спектр произведения составляет свёртку спектров. 

![Код am.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/18.jpg){#fig:018 width=70%}

![Рисунок am.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/19.jpg){#fig:019 width=70%}

![Рисунок2 am.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/20.jpg){#fig:020 width=70%}

10) Я создал каталог coding. В нём создал файлы main.m, maptowave.m,unipolar.m,ami.m,bipolarnrz.m,bipolarrz.m,manchester.m, diffmanc.m, calcspectre.m. Проверил установлен ли пакет расширений. 

![Проверка пакета расширений](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/21.jpg){#fig:021 width=70%}

11) Вписал код в каждый файл. Основной файл - main. С помощью него запускаются все остальные файлы.

![Код main.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/22.jpg){#fig:022 width=70%}

![Код maptowave.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/23.jpg){#fig:023 width=70%}

![Код unipolar.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/24.jpg){#fig:024 width=70%}

![Код ami.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/25.jpg){#fig:025 width=70%}

![Код bipolarnrz.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/26.jpg){#fig:026 width=70%}

![Код bipolarrz.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/27.jpg){#fig:027 width=70%}

![Код manchester.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/28.jpg){#fig:028 width=70%}

![Код diffmanc.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/29.jpg){#fig:029 width=70%}

![Код calcspectre.m](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/30.jpg){#fig:030 width=70%}

12) После запуска файла main у меня создались 3 каталога и создались несколько графиков, которые соответствуют каждому файлу.

![Рисунки в каталоге signal](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/31.jpg){#fig:031 width=70%}

![Рисунки в каталоге sync](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/32.jpg){#fig:032 width=70%}

![Рисунки в каталоге spectre](/home/aalushin/фдд/new2/study_2024-2025_seti/labs/lab1/report/image/33.jpg){#fig:033 width=70%}


# Вывод 

Я изучил методы кодирования и модуляции сигналов с помощью языка Octave. Определил спектры и параметры сигнала. Продемонстрировал принципы модуляции сигналов на примере аналоговой амплитудной модуляции. Исследовал свойства самосинхронизации сигнала. 



