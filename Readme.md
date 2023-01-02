# Инструкция по работе с Git и удаленными репозиториями

## Что такое git?
**Git** - это наиболее популярная реализаия распределенной системы контроля версий. Самая популярная реализация **Git** - [это GitHub] (https://github.com/)

## Подготовка репозитория
Для создания репозитория используется команда "git init". Для этого необходимо в терминале перейти в пустую папку, где в будущем будет репозиторий. Затем в терминале с папкой написать команду "git init"

## Создание коммита
Для создания коммита используется команда "git commit". Для этого в терминале с папкой репозиторием необходимо написать *git commit -m <сообщение к коммиту>*. Cообщение к коммиту писать ***ОБЯЗАТЕЛЬНО!!!***.

### добавление файла к коммиту
для добавления к будущему коммиту используется команда "git add". Для этого в терминале с папкой-репозиторием необходимо написать *git add <название файла>*.

## Создание коммитов
Для этого необходимо выполнить две команды: Первая команда: git add - добавляет все измененные данные в файл. А вторая команда создает коммит: git commit -m "Commit message."

## Журнал изменений
Для просмотра журнала изменений используется команда *git log*. Для этого в терминале с папкой-репозиторием необходимо написать *git log*.

## Перемещение между коммитами
Для перемещения на предыдущие коммиты используется команда *git checkout*. Для этого необходимо в журнале изменений, как показано в предыдущей части, найти необходимый коммит и его номер. После чего в терминале с папкой-репозиторием написать команду *git checkout <номер коммита>*. После применения этой команды вы попадете в состояние **Detached head**. в котором никакние изменения фиксироваться не будут. Для возврата в обычное состояние необходимо написать команду *git checkout master*.

## Ветки в Git
Ветки - как черновики в Git, создав ветку мы можем как второй вариант оставить, также показав коллеге или начальнику мы можем убедиться в том, что можно продолжать или удалить, при этом оригинал держать в чистом варианте. 
1) Для проверки количество веток нужно в терминале ввести: *git branch*. 
2) Для создания новой ветки: *git branch +название ветки*
3) Для перемещения между ветками: *git checkout +название ветки*

## Слияние веток и разрешение конфликтов
Для слияния веток, нужно находиться в ветке master (или в нужной вам ветке), затем в терминале вводим: *git merge +название ветки*

## Удаление веток
Для удаления ненужной ветки, нужно в терминале ввести: *git branc -d +название ветки*. **Главное не забудьте перед этим проверить, все ли перевели или точно нужно удалять?)**

## Git status
Для того чтобы посмотреть текущее состояние ветки, например, какие файлы добавлены или не добавлены для создания commit, можно выполнить команду: *git status*

## Git diff
Просмотреть изменения относительно двух веток можно командой: *git diff*

## Ветки в Git2
Для создания новой ветки используется команда *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать *git branch <название ветки>*

### Просмотр списка веток2
Для просмотра списка веток используется команда *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать команду *git branch*. Зеленым цветом с символом **здвездочка** будет выделена текущая ветка

### Переключение между ветками
Для перехода на другую ветку используется команда "git checkout". Для этого в терминале с папкой-репозиторием пишем команду "git checkout <название ветки>". Для перехода на ветку ветка должна быть ***создана***!!!

# Дополнительная информация для третьего семинара (дз)
## Настройка git
Для того, чтобы указать свое имя: git config --global user.name "My Name"
Для того, чтобы указать свою почту: git config --global amirhan75@gmail.com
Настройть таким образом нам нужно для того, чтобы другие пользователи знали - кто вносит изменения в git документ =)

## Перемещение между папками cd
Для того, чтобы переклачаться между папками нам нужно указать cd + название папки (которую в той же папке создали) Пример: cd '.\git.new\'

## Клонирование удаленного репозитория к себе в компьютер
Клонирование - это когда вы копируете удаленный репозиторий к себе на ПК.
Для этого на сайте [github](https://github.com/) открываем нужный репозиторий и с помощью книпки:  *code* копируем и в темринале своего ПК прописываем: git clone +ссылка

## Подключение к удаленному репозиторий 
Чтобы подключиться к удаленному репозиторию пишем: git remote add origin +ссылка

## Отправка изменений на сервер
Если мы захотим отправить изменений на сайт, то нам нужно будет сделать следующее: git push origin master
Тем самым мы направим наши изменения в наш удаленный проект и будет на сайте [github](https://github.com/)

## Запрос изменений с сервера 
Чтобы запросить изменений с сайте (к примеру вам заявили, на сайте отличное обновление) git pull origin master

>PS: Updated HomeWork date 02.01.2023 (final version) (but it's a git clone)
