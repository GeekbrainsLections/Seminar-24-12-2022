# Инструкция по работе с Git и удалёнными репозиториями

## Что такое git?
**Git** - это наиболее популярная реализация распределённой системы контроля версий. Самая популярная реализация **Git** - это [GitHub](https://github.com/)

## Подготовка репозитория
Для сооздания репозитория используется команда *git init*. Для этого необходимо в терминале перейти в пустую папку, где в будущем будет репозиторий. Затем в терминале с папкой написать команду *git init*.

## Создание коммитов

### Добавление файла к коммиту
Для добавления файла к будущему коммиту используется команда *git add*. Для этого в терминале с папкой-репозиторием необходимо написать *git add <название файла>*.

### Создание коммита
Для создания коммита используется команда *git commit*. Для этого в терминале с папкой репозиторием необходимо написать *git commit -m <сообщение к коммиту>*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО!!!***.

## Журнал изменений
Для просмотра журнала изменений используется команда *git log*. Для этого в терминале с папкой-репозиторием необходимо написать *git log*.

## Перемещение между коммитами
Для перемещения на предущие коммиты используется команда *git checkout*. Для этого необходимо в журнале изменений, как показано в предыдущей части, найти необходимый коммит и его номер. После чего в терминале с папкой-репозиторием написать команду *git checkout <номер коммита>*. После примененения этой команды Вы попадёте в состояние **Detached head**, в котором никакие изменения фиксироваться не будут. Для возврата в обычное состояние необходимо написать команду *git checkout master*.

## Ветки в Git
### Создание веток в Git
Для создания новой ветки используется команда *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать *git branch <название ветки>*
### Просмотр списка веток
Для просмотра списка веток используется комнада *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать команду *git branch*. Зелёным цветом с символом **звёздочка** будет выделена текущая ветка

### Переключение между вектами
Для перехода на другую ветку используется команда *git checkout*. Для этого в терминале с папкой-репозиторием пишем команду *git checkout <название ветки*. Для перехода на ветку ветка должна быть ***создана***!!!

## Ветки в Git и слияние их
Под веткой принято понимать независимую последовательность коммитов в хронологическом порядке. Для того чтобы создать ветку нужно в файле репозитория в терминале воспользоваться командой *git branch <название ветки>*. После этого командой *git checkout <название ветки>* выполнить перемещение в созданную ветку. Затем внести изменения, обязательно сохранить файл и выполнить коммит. После этого командой *git checkout main* выполнить возврат в основную ветку. 
Для того чтобы выполнить слияние веток необходимо воспользоваться командой *git merge <имя объединяемой ветки>*. Для этого в файле репозитория в терминале нужно выполнить команду *git merge <имя объединяемой ветки>*.


##  Разрешение конфликтов
При объединении веток может возникнуть ситуация конфликта. Она возникает, когда объединённые ветви изменяют одну и ту же строку файла по - разному или когда одна ведвь изменяет файл, а другая ветвь его удоляет. При возникновении конфликта в нашем файле появится информация с заголовком *<<<<<<<< HEAD* и разделительными линиями  *=========*, а в заключении *>>>>>>> <имя ветки с которой слияние>*. Для того чтобы разрешить конфликт требуется отредактировать конфликтующий файл путём удаления разделителей конфликта **<<<<<<<< HEAD,=========,>>>>>>> <имя ветки с которой слияние>**. После того как отредактировали конфликт следует выполнить сохранение файла и добавить его к комиту командой *git commit*.

## Удаление веток

## Клонирование удалённого репозитория

## Создание в удалённом репозитории ветки master

## Добавление удалённый репозиториев

## Отправка изменений в удалённый репозиторий

