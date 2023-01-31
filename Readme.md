# Инструкция по работе с Git и удалёнными репозиториями

## Что такое git?
**Git** - это наиболее популярная реализация распределённой системы контроля версий. Самая популярная реализация **Git** - это [GitHub](https://github.com/)

## Подготовка репозитория
Для сооздания репозитория используется команда *git init*. Для этого необходимо в терминале перейти в пустую папку, где в будущем будет репозиторий. Затем в терминале с папкой написать команду *git init*.

## Создание коммитов

### Добавление файла к коммиту
Для добавления файлов к будущему коммиту используется команда *git add*. Для этого в терминале с папкой-репозиторием неоходимо написать *git add <название файла>*. Перед тем, как добавлять файлы к коммиту, можно узнать, какие файлы были изменены, при помощи команды *git status*, написав ее в терминале с папкой-репозиторием. Тогда в терминале мы увидим список модифицированных файлов. С помощью команды *git diff*, также написанной в терминале с папкой-репозиторием, можно увидеть, какие изменения были внесены в файлы.

### Создание коммита
Для создания коммита используется команда *git commit*. Для этого в терминале с папкой репозиторием необходимо написать *git commit -m <сообщение к коммиту>*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО!!!***.

## Журнал изменений
Для просмотра журнала изменений используется команда *git log*. Для этого в терминале с папкой-репозиторием необходимо написать *git log*. Чтобы увидеть дерево коммитов, в терминале с папкой-репозиторием необходимо написать команду *git log --graph*.

## Перемещение между коммитами
Для перемещения на предущие коммиты используется команда *git checkout*. Для этого необходимо в журнале изменений, как показано в предыдущей части, найти необходимый коммит и его номер. После чего в терминале с папкой-репозиторием написать команду *git checkout <номер коммита>*. После примененения этой команды Вы попадёте в состояние **Detached head**, в котором никакие изменения фиксироваться не будут. Для возврата в обычное состояние необходимо написать команду *git checkout master*.

## Ветки в Git
### Создание веток в Git
Ветки нужны для разделения проекта на задания между разработчиками.
Для создания новой ветки используется команда *git branch*. Для этого в терминале с папкой репозитория необходимо написать *git branch <название ветки>*.

### Просмотр списка веток.
Для просмотра списка веток используется комнада *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать команду *git branch*. Зелёным цветом с символом **звёздочка** будет выделена текущая ветка.

### Переключение между вектами
Для перехода на другую ветку используется команда *git checkout*. Для этого в терминале с папкой-репозиторием пишем команду *git checkout <название ветки*. Для перехода на ветку ветка должна быть ***создана***!!!

## Слияние веток и разрешение конфликтов

### Слияние веток
Для слияния веток используется команда *git merge*. Для этого сначала нужно перейти на ветку, к которой мы будем присоединять необходимую ветку, с помощью команды *git checkout <название ветки>*. После этого в терминале с папкой-репозиторием следует написать команду *git merge <название присоединяемой ветки>*.

### Разрешение конфликтов
Часть конфликтов программа разрешает автоматически. В тех случаях, когда конфликты не разрешаются автоматически, приложение отмечает строки, содержащие конфликт. Разработчику необходимо удалить лишнюю информацию или дописать новую, после чего сохранить файл и создать новый коммит.

## Удаление веток
Для удаления ветки используется команда *git branch -d*. Для этого в терминале с папкой-репозиторием пишем команду *git branch -d <название удаляемой ветки>*.

## Удаленные репозитории

Контроль существует для того, чтобы над проектом могла работать команда программистов, соответственно, этот проект должен храниться в доступном для всех разработчиков, участвующих в проекте, месте, в случае Git - на сервере github. Репозиторий, хранящийся на сервере github, называется удаленным. Для того, чтобы пользоваться удаленными репозиториями с сервера github, первым делом необходимо создать аккаунт на сайте [GitHub](https://github.com/).

### Создание связи между удаленным репозиторием и локальным

Для того, чтобы связать созданный нами локальный репозиторий с удаленным, необходимо возпользоваться командой *git remote add origin <ссылка на удаленный репозиторй, хранящийся на github>*. *origin* - это название главного репозитория, если в проекте используется несколько удаленных репозиториев, то каждому из них присваивается собственное имя. После создания связи удаленного и локального репозиториев необходимо указать главную ветку, использовав команду *git branch -M main*, где *main* - это название главной ветки.

### Создание копии удаленного репозитория

Чтобы загрузить себе на компьютер чей-то уже готовый репозиторий, используется команда *git clone <ссылка на удаленный репозиторй, хранящийся на github>*. Эта команда скачивает репозиторий, создает папку с таким же названием и в эту папку помещает все то, что находилось в репозитории. В начальной папке не был инициализирован git, в клонированном репозитории он уже работает.

### Отправка изменений проекта в удаленный репозиторий

После сохранения изменений в репозитории при помощи коммитов, можно отправить новую версию проекта на удаленный сервер. Для этого используется команда *git push <название репозитория> <название ветки, в которую отправляется коммит>*. В нашем случае команда выглядит так: *git push origin main*. Таким образом мы отправим наши изменения в репозиторий с названием *origin*, в ветку *main*.

### Получение актуальной версии проекта

Для того, чтобы получить актуальную версию проекта со всеми внесенными в нее изменениями другими разработчиками, используется команда *git pull*. Эта команда не только вытягивает изменения с удаленного сервера, но и пытается объединить ветки. У команды *git pull* также имеются 2 параметра - это название репозитория и ветка, если мы их укажем, то мы внесем изменения в конкретную ветку нашего репозитория, например, команда *git pull origin main* скачает изменения, внесенные только в главную ветку репозитория.

### Fork и pull request

Чтобы создать копию чужого репозитория сразу на сервере Github, неоходимо зайти в этот репозиторий на сайте и нажать кнопку **Fork**. Тогда в вашем аккаунте появится копия этого репозитория. Для работы с ним необходимо скачать его на свой компьютер с помощью команды *git clone*. Вносить изменения нужно в новую ветку. После внесения изменений и их отправки на GitHub, появится кнопка **Compare and pull request**, с помощью которой можно предложить владельцу репозитория рассмотреть эти изменения.