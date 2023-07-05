# GR_4660

# Инструкция для работы с Git и удалёнными репозиториями

## Что такое Git?
Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.

## Подготовка репозитория
Для создание репозитория необходимо выполнить команду *git init* в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

## Создание коммитов (комментариев) в логах и редактирование их 

Для добавления измений в коммит используется команда *git add*. Чтобы использовать команду *git add* напишите git *add <имя файла>*

## Просмотр состояния репозитория
 Для того, чтобы посмотреть состояние репозитория используется команда git status. Для этого необходимо в папке с репозиторием написать git status, и Вы увидите были ли измения в файлах, или их не было.

## Создание коммитов
 Для того, чтобы создать коммит(сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "<сообщение к коммиту>*. Все файлы для коммита должны быть ДОБАВЛЕНЫ и сообщение к коммиту писать ОБЯЗАТЕЛЬНО.

## Перемещение между сохранениями
Для того, чтобы перемещаться между коммитами, используется команда git checkout. Используется она в папке с пепозиторием следующим образом: git checkout <номер коммита>
.
## Журнал изменений
Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда *git log*. Для этого достаточно выполнить команду *git log* в папке с репозиторием.

## Ветки в Git
### Создание ветки
Для того, чтобы создать ветку, используется команда *git branch*. Делается это следующим образом в папке с репозиторием: *git branch <название новой ветки>*.

## Слияние веток
Для того чтобы дабавить ветку в текущую ветку используется команда *git merge branch_name*.

## Удаление веток
Для удаления ветки ввести команду *git branch -d branch_name*.

## Проверка версии
Проверка версии *git* , которая установлена на компьютере *git --version*.

## Провекрка различия файлов
 Команда, которая производит сравнение между предыдущими версиями файла, проверяет коммиты, ветки и т.д. - *git diff*

## Что делать, если появился **End** или не работает строка?
для того, чтобы принудительно завершить wim (после добавления commit без описания выходит end) в *git* - необходимо ввести команду *:wQ!* или просто нажать *Q*.

## Удобные команды
Для просмотра истории действий в одну строку достаточно ввести команду: *git log --oneline* - вывод компактного лога действий по файлу.

 *git log --graph* - графическое отображение взаимосвязь коммитов, увидеть ветки.

*git commit -am -add "комментарий"* - короткая команда, которую придумали программисты, чтобы не писать две команды *add* и *commit* для сохранения и написания комментария в изменении файла

Для того, чтобы изменить последний комментарий в истории действий файла , заменить его  есть команда *git commit -amend -m "комментарий"* 

## Как добавить изображение в git?
Для начала надо найти изображание, которое будет прикрепляться к файлу в папку, в которой мы работаем.
После добавления файла достаточно написать следующее:
![Инструкция по редактированию текста в Markdown из лекции 2](photo_2023-06-28_18-42-10.jpg)

После добавления изображения можно добавить файл изображения в игнор лист, достаточно в данной папке сделать файл **.gitignore** и добавить изображение в этот файл. И сделать add этого файла, чтобы система его сохранила и оставить коммит.

## Работа с удаленным репозиторием

Для того, чтобы Скопировать файл из **GitHub** необходимо зайти на просмотр файла на сайте, нажать на зеленую надпить **Code** и далее скопировать ссылку. После копирования заходим в обычную папку, в терминал и пишем команду *git clone* - вуаля, у нас теперь есть файл, на котором можно посмотреть ветки, логи и прочее.

Для того, чтобы вносить изменения в данном файле необходимо на сайте **GitHub** сначала его "форкнуть" - т.е. зайти на страницу файла и справа наверху нажать на кнопочку "Fork" (вилка) и после этого файл будет отображаться у нас с надписью пр. forked from CinemaStyle/GR_4660.
После чего можно этот файл снова клонировать и уже можно вносить изменения в него и в последствии реквестить (предалагать) владельцу файла эти изменения.

Для того, чтобы сохранить наши изменения в файле физически в Visual Code и внести их в удаленный репозиторий на сайте GitHub необходимо ввести команду *git push* , обязательно надо быть авторизованным.

Также, если изменения были внесены наоборот в удаленном репозитории, т.е. на сайте - необходимо ввести *git pull*, чтобы изменения "стянулись" в файл, который есть на компьютере.
