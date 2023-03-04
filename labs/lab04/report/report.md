---
## Front matter
title: "Отчёт по лабораторной работе №4"
subtitle: "дисциплина: Операционные системы"
author: "Яковин Илья Андреевич"

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

Целью данной лабораторной работы является приобритение практических навыков взаимодействия пользователя с системой посредством командной строки.

# Задание
1 Определите полное имя вашего домашнего каталога. Далее относительно этого
каталога будут выполняться последующие упражнения.
2 Выполните следующие действия:
• Перейдите в каталог /tmp.
• Выведите на экран содержимое каталога /tmp. Для этого используйте ко-
манду ls с различными опциями. Поясните разницу в выводимой на экран
информации.
• Определите, есть ли в каталоге /var/spool подкаталог с именем cron?
• Перейдите в Ваш домашний каталог и выведите на экран его содержимое.
Определите, кто является владельцем файлов и подкаталогов?
3 Выполните следующие действия:
• В домашнем каталоге создайте новый каталог с именем newdir.
• В каталоге ~/newdir создайте новый каталог с именем morefun.
• В домашнем каталоге создайте одной командой три новых каталога с именами
letters, memos, misk. Затем удалите эти каталоги одной командой.
• Попробуйте удалить ранее созданный каталог ~/newdir командой rm. Проверь-
те, был ли каталог удалён.
• Удалите каталог ~/newdir/morefun из домашнего каталога. Проверьте, был ли
каталог удалён.
4 С помощью команды man определите, какую опцию команды ls нужно ис-
пользовать для просмотра содержимое не только указанного каталога, но и подкаталогов, входящих в него.
5 С помощью команды man определите набор опций команды ls, позволяющий от-
сортировать по времени последнего изменения выводимый список содержимого
каталога с развёрнутым описанием файлов.
6 Используйте команду man для просмотра описания следующих команд: cd,
pwd, mkdir, rmdir, rm. Поясните основные опции этих команд.
7 Используя информацию, полученную при помощи команды history, выполните
модификацию и исполнение нескольких команд из буфера команд.



# Выполнение лабораторной работы

Определю полное имя домашнего каталога с помощью команды pwd

![Рис.1 Имя домашнего каталога](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/1.%20%D0%98%D0%BC%D1%8F%20%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%B3%D0%BE%20%D0%BA%D0%B0%D1%82%D0%B0%D0%BB%D0%BE%D0%B3%D0%B0.png)

Рис.1 Имя домашнего каталога

Дальше я перейду в каталог /tmp с помощью команды cd

![Рис.2 Каталог /tmp](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/2.%20%D0%9A%D0%B0%D1%82%D0%B0%D0%BB%D0%BE%D0%B3%20%20tmp.png)

Рис.2 Каталог /tmp

С помощью команды ls с разными опциями выведу на экран содержимое каталога /tmp
Команда ls нужна для просмотра содержимого каталога

![Рис.3 Команда ls](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/3.%20%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B0%20ls.png)

Рис.3 Команда ls

Для того,чтобы отобразить имена скрытых файлов я использую команду ls с опцией a

![Рис.4 ls -a](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/4.%20%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B0%20ls%20-a.png)

Рис.4 ls -a

Для вывода на экран подробной информации о файлах и каталогах я использую ls с опцией l

![Рис.5 ls -l](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/5.%20%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B0%20ls%20-l.png)

Рис.5 ls -l

Также можно получить информацию о типах файлов, для этого используется опция F

![Рис.6 ls -F](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/6.%20%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B0%20ls%20-F.png)

Рис.6 ls -F

Оптимизированная команда ls с различными опциями

![Рис.7 ls -alF ](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/7.%20%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B0%20ls%20-alF.png)

Рис.7 ls -alF 

Теперь определю,есть ли в каталоге /var/spool подкаталог с именем cron. Для этого вернусь в домашний каталог  и с помощью команды cd и с помощью комнды ls проверю его наличие.

![Рис.8 Отсутствие подкаталога cron](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/8.%20%D0%9E%D1%82%D1%81%D1%83%D1%82%D1%81%D1%82%D0%B2%D0%B8%D0%B5%20%D0%BF%D0%BE%D0%B4%D0%BA%D0%B0%D1%82%D0%B0%D0%BB%D0%BE%D0%B3%D0%B0%20cron.png)

Рис.8 Отсутствие подкаталога cron

Далее я перейду в домашний каталог с помощью cd и выведу его содержимое

![Рис.9 Содержимое домашннего каталога](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/9.%20%20%D0%A1%D0%BE%D0%B4%D0%B5%D1%80%D0%B6%D0%B8%D0%BC%D0%BE%D0%B5%20%D0%94%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%B3%D0%BE%20%D0%BA%D0%B0%D1%82%D0%B0%D0%BB%D0%BE%D0%B3%D0%B0.png)

Рис.9 Содержимое домашннего каталога

В домашнем каталоге создам новый каталог с именем newdir для этого использую команду mkdir

![Рис.10 Создание каталога mkdir](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/10.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%BA%D0%B0%D1%82%D0%B0%D0%BB%D0%BE%D0%B3%D0%B0%20newdir.png)

Рис.10 Создание каталога mkdir

В каталоге newdir создам новый каталог с именем morefun

![Рис.11 Создание подкаталога morefun](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/11.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%BF%D0%BE%D0%B4%D0%BA%D0%B0%D1%82%D0%B0%D0%BB%D0%BE%D0%B3%D0%B0%20%20morefun%20%D0%B2%20%D0%BA%D0%B0%D1%82%D0%B0%D0%BB%D0%BE%D0%B3%D0%B5%20newdir.png)

Рис.11 Создание подкаталога morefun

С помощью одной команды создам три новых каталога с именами letters,memos,misk. Затем с помощью одной команды mkdir удалю их

![Рис.12 Создание и удаление каталогов одной командой](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/12.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%B8%20%D1%83%D0%B4%D0%B0%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5%20%20%D0%BA%D0%B0%D1%82%D0%B0%D0%BB%D0%BE%D0%B3%D0%BE%D0%B2%20%D1%81%20%D0%BF%D0%BE%D0%BC%D0%BE%D1%89%D1%8C%D1%8E%20%D0%BE%D0%B4%D0%BD%D0%BE%D0%B9%20%D0%BA%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D1%8B.png)

[Рис.12 Создание и удаление каталогов одной командой

Попытаюсь удалить ранее созданный каталог newdir из домашнего каталога. Это оказывается невозможным.

![Рис.13 Попытка удалить каталог newdir](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/13.%20%D0%9F%D0%BE%D0%BF%D1%8B%D1%82%D0%BA%D0%B0%20%D1%83%D0%B4%D0%B0%D0%BB%D0%B8%D1%82%D1%8C%20%D0%BA%D0%B0%D1%82%D0%B0%D0%BB%D0%BE%D0%B3%20newdir.png)

Рис.13 Попытка удалить каталог newdir

Удалю каталог newdir и подкаталог morefun из домашнего каталога. Потом проведу проверку с помощью команды ls.

![Рис.14 Удаление каталога newdir и подкаталога morefun](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/14.%20%D0%A3%D0%B4%D0%B0%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%BF%D0%BE%D0%B4%D0%BA%D0%B0%D1%82%D0%B0%D0%BB%D0%BE%D0%B3%D0%B0%20morefun%20%20%D0%B8%20%D0%BA%D0%B0%D1%82%D0%B0%D0%BB%D0%BE%D0%B3%D0%B0%20newdir.png)

Рис.14 Удаление каталога newdir и подкаталога morefun

С помощью команды man ls выясню, что для просмотра содержимого не только указанного каталога, но и подкаталогов нужно использовать опцию -R

![Рис.15 Поиск нужной функции](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/15.%20%D0%9F%D0%BE%D0%B8%D1%81%D0%BA%20%D0%BD%D1%83%D0%B6%D0%BD%D0%BE%D0%B9%20%20%D0%BE%D0%BF%D1%86%D0%B8%D0%B8.png)

Рис.15 Поиск нужной функции

С помощью команды man ls определю набор опций команды, позволяющий отсортировать по времени последнего изменения выводимый список содержимого каталога. Таким набором является опция -c -lt

![Рис.16 Поиск ещё одной нужной функции](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/16.%20%D0%9F%D0%BE%D0%B8%D1%81%D0%BA%20%D0%B5%D1%89%D1%91%20%D0%BE%D0%B4%D0%BD%D0%BE%D0%B9%20%D0%BD%D1%83%D0%B6%D0%BD%D0%BD%D0%BE%D0%B9%20%D0%BE%D0%BF%D1%86%D0%B8%D0%B8.png)

Рис.16 Поиск ещё одной нужной функции

Использую команду man для просмотра описания команд cd,pwd,mkdir,rmdir,rn.
Команда cd используется для перемещения по файловой системе ОС типа Linux

![Рис.17 man cd](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/17.%20%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B0%20man%20cd.png)

Рис.17 man cd

Команда pwd нужна для определения абсолютного пути к текущему каталогу 

![Рис.18 man pwd](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/18.%20%20%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B0%20man%20pwd.png)

Рис.18 man pwd

Команда mkdir используется для создания каталогов

![Рис.19 man mkdir](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/19.%20%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B0%20man%20mkdir.png)

Рис.19 man mkdir

Команда rmdir используется для удаления пустых каталогов 

![Рис.20 man rmdir](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/20.%20%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B0%20man%20rmdir.png)

Рис.20 man rmdir

Команда rm используется для удаления файлов и каталогов

![Рис.21 man rm](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/21.%20%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B0%20man%20rm.png)

Рис.21 man rm

Используя информацию, которую я получил с помощью команды history, выполню модификации команды ls и исполню их.

![Рис.22 Модификация и исполнение команд](https://github.com/Florikan2/study_2022-2023_os-intro/blob/master/labs/lab04/report/image/22.%20%D0%9C%D0%BE%D0%B4%D0%B8%D1%84%D0%B8%D0%BA%D0%B0%D1%86%D0%B8%D1%8F%20%D0%B8%20%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%BA%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4.png)

Рис.22 Модификация и исполнение команд


# Контрольные вопросы

1 Что такое командная строка? Терминал Linux предоставляет интерфейс, в
котором можно вводить команды и видеть результат, напечатанный в виде
текста. Можно использовать терминал для выполнения таких задач, как пере-
мещение файлов или навигация по каталогу, без использования графического
интерфейса.
2 При помощи какой команды можно определить абсолютный путь текущего
каталога? Приведите пример. При помощи команды pwd.
3 При помощи какой команды и каких опций можно определить только тип
файлов и их имена в текущем каталоге? Приведите примеры. ls -F.
4 Каким образом отобразить информацию о скрытых файлах? Приведите при-
меры. Для того, чтобы отобразить имена скрытых файлов, необходимо исполь-
зовать команду ls с опцией a.
5 При помощи каких команд можно удалить файл и каталог? Можно ли это
сделать одной и той же командой? Приведите примеры. rmdir и rm.
6 Каким образом можно вывести информацию о последних выполненных поль-
зователем командах? работы?
7 Как воспользоваться историей команд для их модифицированного выполнения?
Приведите примеры. С помощью команды history.
8 Приведите примеры запуска нескольких команд в одной строке.
9 Дайте определение и приведите примера символов экранирования. Экраниро-
вание символов — замена в тексте управляющих символов на соответствующие
текстовые подстановки.
10 Охарактеризуйте вывод информации на экран после выполнения команды
ls с опцией l. Чтобы вывести на экран подробную информацию о файлах и
каталогах, необходимо использовать опцию l. При этом о каждом файле и
каталоге будет выведена следующая информация: тип файла, право доступа,
число ссылок, владелец, размер, дата последней ревизии, имя файла или
каталога.
11 Что такое относительный путь к файлу? Приведите примеры использования
относительного и абсолютного пути при выполнении какой-либо команды.
Относительный путь представляет собой путь по отношению к текущему
рабочему каталогу пользователя или активных приложений.
12 Как получить информацию об интересующей вас команде? При помощи ко-
манды man.
13 Какая клавиша или комбинация клавиш служит для автоматического допол-
нения вводимых команд? Tab.


# Выводы

В ходе выполнения лабораторной работы я приобрёл практические навыки
взаимодействия пользователя с системой посредством командной строки.


