![Баннер](https://149611589.v2.pressablecdn.com/wp-content/uploads/2014/06/revisr-banner.png)
# GR_4660
# <span style="color:#CD5C5C">**Инструкция для работы с Git и удалёнными репозиториями**</span>

## <span style="color:#E9967A">**Что такое Git?**
---
<span style="color:#F0E68C">Git</span> - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.

## <span style="color:#E9967A">**Подготовка репозитория**
---
Для создание репозитория необходимо выполнить команду <span style="color:#00FF7F">*git init*</span> в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

## <span style="color:#E9967A">**Создание коммитов**
---
### <span style="color:#FF6347">**Git add**
Для добавления измений в коммит используется команда <span style="color:#00FF7F">*git add.*</span> Чтобы использовать команду <span style="color:#00FF7F">*git add*</span> напишите <span style="color:#00FF7F">*git add <имя файла>*</span>

## <span style="color:#E9967A">**Просмотр состояния репозитория**
Для того, чтобы посмотреть состояние репозитория используется команда <span style="color:#00FF7F">*git status.*</span> Для этого необходимо в папке с репозиторием написать <span style="color:#00FF7F">*git status*</span>, и Вы увидите были ли измения в файлах, или их не было.

### <span style="color:#FF6347">**Создание коммитов**
Для того, чтобы создать коммит(сохранение) необходимо выполнить команду <span style="color:#00FF7F">*git commit.*</span> Выполняется она так: <span style="color:#00FF7F">*git commit -m "<сообщение к коммиту>*</span>. Все файлы для коммита должны быть **_ДОБАВЛЕНЫ_** и сообщение к коммиту писать **_ОБЯЗАТЕЛЬНО._**

## <span style="color:#E9967A">**Перемещение между сохранениями**
---
Для того, чтобы перемещаться между коммитами, используется команда <span style="color:#00FF7F">*git checkout.*</span>Используется она в папке с пепозиторием следующим образом: <span style="color:#00FF7F">*git checkout <номер коммита>*

## <span style="color:#E9967A">**Журнал изменений**
---
Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда <span style="color:#00FF7F">*git log.*</span> Для этого достаточно выполнить команду <span style="color:#00FF7F">*git log*</span> в папке с репозиторием

## <span style="color:#E9967A">**Ветки в Git**
---
### <span style="color:#FF6347">**Создание ветки**
Для того, чтобы создать ветку, используется команда <span style="color:#00FF7F">*git branch*</span>. Делается это следующим образом в папке с репозиторием: <span style="color:#00FF7F">*git branch <название новой ветки>*

## <span style="color:#E9967A">**Слияние веток**
---
Для того чтобы дабавить ветку в текущую ветку используется команда <span style="color:#00FF7F">*git merge*

## <span style="color:#E9967A">**Удаление веток**
---
Для удаления ветки ввести команду <span style="color:#00FF7F">*"git branch -d 'name branch'"*

# <span style="color:#CD5C5C">**Углубляемся в контроль версий**

## <span style="color:#E9967A">**Разграничение понятий Git и GitHub**
|        <span style="color:#CD5C5C">**Git**                            |            <span style="color:#CD5C5C">**GitHub**           |
|-------------------------------------------|---------------------------------|
| 1. Освоить работу с удаленными            |1. Сервис компании Майкрософт для|
| репозиториями, которые находятся          |организации работы удаленных     |
| не на локальной, а на удаленной машине,   |репозиториев                     |
| например, на сервере.                     |2. Самый популярный сервис Git   |
|2. git — одна из систем контроля версий    |Много полезных функций           |
|3. Способ организации и поддержания        |3. Огромный архив различного кода|
|версионности                               |                                 |
|4. Самая популярная система контроля версий|                                 |

## <span style="color:#E9967A">Работа с удаленными репозиториями. Скачивание из текущего репозитория и слияние со своей версией

Освоить работу с удаленными репозиториями, которые находятся не на локальной,
а на удаленной машине, например, на сервере.
Копировать внешний репозиторий на свой ПК можно командой <span style="color:#00FF7F">**_git clone._**


Команда <span style="color:#00FF7F">**_git clone_**</span> составная: она не только
загружает все изменения, но и пытается слить 
все ветки на локальном компьютере и в
удаленном репозитории.

### <span style="color:#FF6347">**git pull**
* Эта команда позволяет скачать все из текущего репозитория и автоматически
сделать merge с нашей версией

![Пример команды git pull](https://joprblob.azureedge.net/site/blog/50fa5f40-93ac-475e-895d-8724cc761d19/pull.gif)

### <span style="color:#FF6347">**git push**

Отправить свою версию репозитория во
внешний репозиторий поможет команда git
push. При первом её использовании нужна
<span style="color:#00FF7F">**_git pull_**</span> авторизация.
* Эта команда позволяет отправить нашу
версию репозитория на внешний
репозиторий. **ТРЕБУЕТ АВТОРИЗАЦИИ** на внешнем репозитории.

![Пример команды git pull](https://wac-cdn.atlassian.com/dam/jcr:0d181327-3fb0-44ec-9ab4-d6dea0fd406f/01%20Git%20push%20discussion.svg?cdnVersion=1090)

## <span style="color:#E9967A">**Как настроить совместную работу**

1. Создать аккаунт на GitHub.com
2. Создать локальный репозиторий
3. “Подружить” ваш локальный и удалённый репозитории. 
 **_GitHub при создании нового репозитория подскажет, как это можно сделать_**
4. Отправить (**_push_**) ваш локальный репозиторий в удалённый (на GitHub), при этом, возможно, вам нужно будет авторизоваться на удалённом репозитории
5. Провести изменения “с другого компьютера”
6. Выкачать (**_pull_**) актуальное состояние из удалённого репозитория

## <span style="color:#E9967A">**pull request**
* **команда для предложения изменений**

* **запрос на вливание изменений в репозиторий**

В больших компаниях один ответственный за проект создает аккаунт. Другие пользователи дают
команду **pull request**. Предлагать изменения на __GitHub__ нужно в отдельной ветке. Сначала
пользователь копирует репозиторий на свой компьютер, делает *fork* репозитория, затем
клонирует версию на своём ПК, создаёт ветку с предлагаемыми изменениями, отправляет
изменения командой push в свой аккаунт на *GitHub* и даёт команду <span style="color:#00FF7F">*pull request.*

## <span style="color:#E9967A">**Как сделать _pull request_**
* Делаем   (ответвление) репозитория fork
* Делаем <span style="color:#00FF7F">**_git clone_**</span>  версии репозитория **_СВОЕЙ_**
* Создаем новую ветку и в **_НЕЕ_** вносим свои изменения
* Фиксируем изменения (делаем коммиты)
* Отправляем свою версию в свой __GitHub__
* На сайте __GitHub__ нажимаем кнопку <span style="color:#00FF7F">**_pull request_**

