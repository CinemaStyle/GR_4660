# Домашнее задание, контроль версий, семинар 3

# Начало работы в Git. Инструкция для работы с Markdown. Работа с Git и GitHub

## Что такое git?

Git - это консольная утилита для отслеживания и ведения истории изменения файлов. 
На данный момент является самой популярной утилитой по контролю версий.
С помощью Git-a можно откатить свой проект до более старой версии, сравнивать, анализировать или сливать свои изменения в репозиторий.
На данном этапе рассмотрим основные понятия и команды для работы в Git.


## Что такое репозиторий Git?

Репозиторий — это все файлы, находящиеся под контролем версий, вместе с историей их изменения и другой служебной информацией.

## Подготовка репозитория.

Репозиторий Git можно создать, либо выбрав любую папку на компьютере, либо клонировав себе уже существующий репозиторий.

## Создание коммитов.


### Git add.
Для добавления изменений в коммит используется команда *git add*. Чтобы использовать команду *git add* напишите *git add <имя файла>*. Для добавления всех файлов используйте команду *"git add ."*

### Просмотр состояния репозитория.

Для того, чтобы посмотреть состояние репозитория используется команда *git status*. 

### Создание коммитов.

Для того, чтобы создать коммит (сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "<сообщение к коммиту>". Все файлы для коммита должны быть *__ДОБАВЛЕНЫ__* и сообщение к коммиту писать *__ОБЯЗАТЕЛЬНО__*.

## Перемещение между сохранениями.

Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с репозиторием следующим образом: *git checkout <номер коммита>*.

> &#9888; **Warning!**  
> Во избежание ошибок, обязательно вернитесь на конец ветки **master** (**HEAD**) с помошью команды *git checkout master*.


## Журнал изменений.

Для того, чтобы посмотреть все сделанные изменения в репозитории, используется команда *git log*. Для этого достаточно выполнить команду *git log* в папке с репозиторием

## Ветки в git

### Создание ветки.

Для того, чтобы создать ветку, используется команда *git branch*. Делается это следующим образом в папке с репозиторием: *git branch <название новой ветки>*.

> &#128712; **Information**  
> Для вывода списка веток изпользуйте команду *git branch*. Ветка, на которой Вы сейчас находитесь будет отмечена звёздочкой (\*).

### Слияние веток и решение конфликтов.

Для того, чтобы добавить ветку в текущую ветку используется команда *git merge*. Команда будет выглядеть следующим образом: *git merge <название ветки>*.

> &#9757; **Important**  
> Важно помнить, что слияние веток происходит в ту, из которой Вы вызываете *git merge*.

Иногда, если в сливаемых ветках в одном и том же месте указаны разные данные, может возникнуть конфликт.  

В этом случае VS Code предложит Вам принять текущие (Current) изменения, входящие (Incoming) изменения, оба (Both) изменения или сравнить изменения (Compare Changes).

### Удаление веток

Для удаления ветки используется ключ *-d*. Необходимо ввести команду *git branch -d <имя ветки>*.

## Краткая сводка по командам
---
|Команда          |Действие|Примечание
|:-               |:-|:-
|git init         |Создание репозитория|Создаётся скрытая папка .git
|git add          |Добавление изменений в коммит|
|git status       |Просмотр состояния репозитория|
|git commit       |Создание коммита|Фиксация, сохранение, снимок изменений
|git log          |Вывод всех изменений в файле|Выводится хэш коммита, автор, его e-mail, дата и время коммита
|git checkout     |Перемещение между коммитами|И ветками
|git branch       |Создание новой ветки|Вывод списка веток на экран
|git merge        |Слияние веток|

### Удобные сокращенные команды.
---
|Команда          |Действие|Примечание
|:-               |:-|:-
|git сommit -am *"комментарий в кавычках"*|сочетание комманд **git add** и **git commit** |
|git checkout -b <имя ветви>|Создание и одновременный переход на новую ветвь
|git log --oneline|Вывод информации по логам в удобный, читаемый вид|

# Markdown

Markdown — это удобный в чтении и написании язык для форматирования обычного текста. 
Главный пример использования маркдауна, с которым мы часто сталкиваемся — файлы readme.md, которые есть в каждом репозитории на Гитхабе. Само расширение "*.md*" в имени файла  - является сокращением от markdown.

## Выделение текста.

Чтобы выделить текст курсивом, необходимо обрамить его звездочками (*) или знаком нижнего подчеркивания,(_). Например, *вот так*, или _вот так_.

Чтобы выделить текст полужирным, необходимо обрамить его двойными звездочками (**) или двойным знаком нижнего подчеркивания (__). Например, **вот так**, или __вот так__.

Альтернативные способы выделения текста жирным или курсивом нужны для того, чтобы мы могли совмещать оба этих способа. Например, _текст может быть выделен курсивом, и при этом быть **полужирным**_.

## Списки.

Чтобы добавить ненумерованные списки, необходимо пункиты выделить звездочкой (*) или знаком +. Например, вот так:
* Элемент 1
* Элемент 2
* Элемент 2
+ Элемент 4


Чтобы добавить нумерованные списки, необходимо пункты просто пронумеровать. Например, вот так:
1. Первый пункт
2. Второй пункт

## Работа с изображениями.

Чтобы вставить изображение в текст, достаточно написать следующее:

![Привет,это Ириска!](В скобках без пробелов укажите наименование изображения, обязательно с указанием расширения. Наример, (test.jpg) )

## Ссылки.

Стандартная разметка для ссылки имеет вид:

* [текст_ссылки](ссылка "текст_подсказки"). Например: [Наша Школа](https://gb.ru/ "текст_подсказки")
* текст_ссылки — явное указание текста ссылки. Cсылка — URL или путь до файла.
* "текст_подсказки" — подсказка, которая будет отображаться при наведении на текст ссылки. Необязательный параметр.
В зависимости от вида ссылки допускаются упрощения и другие варианты оформления.

Чтобы преобразовать URL или адрес электронной почты в ссылку, нужно добавить с двух сторон угловые скобки <>.

<https://gb.ru/>

<Danialumunij@gmail.com>

## Работа с таблицами.

### Создание таблицы.

Cинтаксис языка Markdown достаточно простой, чтобы можно было нарисовать таблицы самому. Для этого используются символ pipe или вертикальной черты ( | ) для разделения ячеек и дефиса ( - ) для создания строки заголовка.

Простейший пример таблицы:

| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Row 1    | Cell 2   | Cell 3   |
| Row 2    | Cell 5   | Cell 6   |
| Row 3    | Cell 8   | Cell 9   |

### Выравнивание таблицы.

Управлять выравниванием текста в столбцах таблицы можно при помощи двоеточий ( : ). **Обратим внимание** на двоеточия в строчке с дефисами. Текст в коде таблицы везде смещен влево, но на результате увидим, что он выровнялся в ту сторону, где мы разместили двоеточия.

Пример:


| Левое выравнивание |Выравнивание по Центру|Правое выравнивание|
|:------------------ |:--------------------:| -----------------:|
| Row 1              | Cell 2               | Cell 3            |
| Row 2              | Cell 5               | Cell 6            |
| Row 3              | Cell 8               | Cell 9            |
   

## Цитаты.

Для обозначения цитат в языке Markdown используется знак «больше» («>»). Его можно вставлять как перед каждой строкой цитаты, так и только перед первой строкой параграфа. Также синтаксис Markdown позволяет создавать вложенные цитаты (цитаты внутри цитат). Для их разметки используются дополнительные уровни знаков цитирования («>»). Цитаты в Markdown могут содержать всевозможные элементы разметки. Цитаты в языке Markdown выглядят следующим образом:

> Это пример цитаты,
> в которой перед каждой строкой
> ставится угловая скобка.

Вложение цитаты в цитату выглядит следующим образом:

> Первый уровень цитирования
>> Второй уровень цитирования
>>> Третий уровень цитирования

Тот же пример:

> Вам ли, любящим баб да блюда,
>> жизнь отдавать в угоду?!
>>> Я лучше в баре бл***м буду
>>>> подавать ананасную воду!


## Заключение.


Работа в Git с использованием языка Markdown чем-то напоминает работут на HTML и создание болванки сайта.

Безусловно, овладеть данной программой необходимо, дабы в целом набить руку для работы в будущем не только в Git, но и любой другой программе по работе с контролем версий.

Нельзя просто так взять и проигнорировать возможность обучения полезным навыкам.

# Раздел 2. Работа с удаленными репозиториями.**GitHub**

## Введение.

Для начала разберемся, что же есть **GitHub** <https://GitHub.com>.

GitHub -  это система управления проектами и версиями кода. Платформа, созданная для разработчиков.

Простыми словами - это социальная сеть, где вместо постов с рецептами и мемами разноуровненвые специалисты в сфере IT производят всевозможные действия со своими наработками: публикуют, делятся, обсуждают. 
Более практичное пояснение - это огромное хранилище различных проектов, оформленных в виде репозиториев. 

Для сравнения.
Наверняка, многим доводилось работать в гугл-таблицах. 
Помимо удобства, данный способ предполагает также массу *неудобств*: от закрытия доступа до "беготни" по всем ячейкам  в поисках изменений, если создатель отстутсвует (ибо нельзя детально посмотреть историю). 
**GitHub**, как вещь, созданная программистами, лишена всех этих недостатков, и предлагает удобство, оптимизацию и конкретный порядок в плане доступа к данным других пользователей. 
Например, репозиторий другого человека можно скопировать, и далее с ним работать. 
Давайте рассмотрим порядок действий для такого случая.

## Копирование удаленного репозитория для локальной работы.

1. Создаем аккаунт на GitHub. Для того, **чтобы скачать код, регистрация не нужна**. Но, так как нам еще в нем работать - лучше сделать это сейчас.
Регистрироваться рекомендую через учетную запись Гугл. На почте нужно словить письмо от GitHub и пройти окончательную верификацию.

2. Создаем на своем компьютере папку. Открываем через VS code. Не инитим! 


> &#9757; **Important**  
> На всякий случай, во избежание ошибок на старте, откройте терминал и с помощью команды *git status* убедитесь, что имеете результат *fatal: not a git repository...* . 
Значит, все хорошо, папка не инициирована. 
Нам как раз такая и нужна.

3. Заходим на страницу с интересующим нас репозиторием и находим зеленую кнопку **Code**. Нажимаем, копируем строку. Предположим, строка выглядит как **https://github.com/Vladekbar/GR_4660.git**

4. В терминале в VS code вводим... Еще раз, убедились, что ваша папка не инициирована? Ок.
В терминале в VS code вводим *git clone* **https://github.com/Vladekbar/GR_4660.git**. 
Жмем Enter.

5. Теперь внутри нашей папки появилась папка с точно таким же названием, которое было у скопированного репозитория.

6. Вызовите команду *git status*. Терминал выдаст все тот же  результат *fatal: not a git repository...*.
Почему так? Потому, что наша папка со скопированным репозиторием находится внутри другой, неиницированной папки. 
Нам необходимо переместиться в папку скопированного репозитория. 
Введите команду: *cd* *наименование папки скопированного репозитория*.

7. Далее можно создавать в папке  файл, изменять его, а конечный результат перенести в исходный репозиторий с уже новым содержимым.
## Алгоритм с нуля:

 1. Создаем репозиторий. Копируем ссылку.
 2. Создаем новую чистую папку, открываем ее в VSC.
 3. Вбиваем команду git clone *ссылка с репозитория*.
 4. Вбиваем команду сd *пробел_TAB*.
 5. Создаем файл в папке.
 6. git add *пробел_TAB*
 7. git commit -m
 8. git push

### Все. Репозиторий на ГитХабе, с которого Вы брали ссылку, изменится согласно локальным сохраненным изменениям.

## Создание удаленного репозитория на основе локального. Взаимосвязь.

1. Создаем папку на своем ПК. Например,  Repetition.

2. Открываем через VS Code. *Инитим*. Создадим файл в ней, например, Hello. Пишем текст, эддим, коммитим.

Теперь, так как мы хотим, чтобы наш репозиторий, **наш труд**, оказался на GitHub - то делаем следующее.

3. Создаем свой аккаунт. Хотя, я надеюсь, вы создали его на предыдущем, вышеописанном этапе.

4. На главной странице: Правый верхний угол --> Жмем "плюсик", выбираем "New repository" --> задаем ему имя.
Имя может быть любым, но я назову его как папку - Repetition. Далее ничего не выбираем и жмем внизу зеленую кнопку **Сreate repository**.

5. GitHub, как вещь практичная, предложит нам варианты, что делать дальше, исходя из планов.

**…or create a new repository on the command line**
echo "# Repetition" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/Vladekbar/Repetition.git
git push -u origin main

**…or push an existing repository from the command line**
git remote add origin https://github.com/Vladekbar/Repetition.git
git branch -M main
git push -u origin main

**…or import code from another repository**
You can initialize this repository with code from a Subversion, Mercurial, or TFS project.

6. В нашей ситуации выбираем средний вариант. 
Поочередно вводим команды:

* git remote add origin https://github.com/Vladekbar/Repetition.git
* git branch -M main
* git push -u origin main

Прошу обратить внимание, что при первом связывании необходимо будет "познакомить" GitHub с вашим репозиторием. 
Терминал подскажет, как. Процедура похожа на "первое представление" в VS Code.

7. Тем временем на GitHub.
Обновите страницу, и убедитесь - наш репозиторий "находится в интернете".
Теперь можно не сдавать домашки в архивах! Достаточно будет передать преподавателю ссылку на GitHub.
Одногруппник желает "списать"? Дайте ему ссылку!


Теперь давайте рассмотрим, каким образом можно менять данные в  удаленном репозитории, работая в локальном.
Например, вы захотели, чтобы репозиторий Repetition на GitHub был дополнен. 
Но интернета у вас не было, зато было много времени поработать в локальном.


## Взаимосвязь редактируемых данных в локальном и удаленном репозиториях.

### Из локального в удаленный.

1. В локальном файле Hello произведем изменения. Заэддим, закоммитим.
В удаленом файле Hello ничего не произойдет.

2. Чтобы изменения попали файл удаленного репозитория, зададим в терминале комманду *git push*.
Обновите страницу и проверьте. Изменения из локального перенеслись в удаленный.

### Из удаленного в локальный

1. Нажимаем на значок "карандашика", выбираем *Edit file*.

2. Набираем текст, с помощью зеленой кнопки эддим изменения, в окошке коммитим.

3. Чтобы "стянуть" данные из удаленного репозитория, в терминале VS Code набираем команду *git pull*.
Изменения эддим, коммитим.

> &#9757; **Important**  
> Данный навык в будущем пригодится для командной работы. Не ленитесь кратко, но не абы как, дать описание коммиту.


### Краткий перечень действий по взаимосвязи.

1. Создаем локальный репозиторий (значит - у себя на компьютере). 
2. Связываем локальный и удаленный репозитории.
3. Отправить (push) ваш локальный репозиторий в удаленный (на GitHub).
4. Провести изменения с другого компьютера.
5. Выкачать (pull) актуальное состояние из удаленного репозитория.

## Взаимодействие через GitHub. Fork. Pull request. 

Простой пример.
Один разработчкик выложил на GitHub свой проект, публично, состоящий из одного файла. Вы этот файла увидели, и хотите предложить ему свои изменения.

В таком случае алгоритм действий выглядит следующим образом.

1. На странице интересуемого нас репозитория с помощью кнопки **Fork**. Копия (ответвление) репозитрия переносится на нашу страницу. 
Название перенесется также. Теперь мы имеем полный доступ к файлу, который может меняться без ущерба реальному владельцу.


2. Далее можем склонироваьть это ответвление репозитория со своей страницы в нашу локальную папку.
Например, в папку инструкции по Markdown. Через VS Code открываем папку с инструкцией.

3. Скопировали строку на GitHub, в терминале через git clone *строка*. Эддим, коммитим.

4. Создаем новую ветку. В этой ветке мы и должны провести изменения. 
Изменяем, эддим, коммитим.

Теперь предложим владельцу свой вариант.

5. Направим изменения в свой, "форкнутый" репозиторий через **git push** и далее по подсказкам.

6. Обновим свою страницу на GitHub. Помимо отображение новой ветки, у нас появляется новая кнопка **Pull request**.
Нажимаем на эту кнопку, и, с нашим описанием, наше предложение отправляется владельцу аккаунта.

7. Новое поле на нашем аккаунте позволяет понять, есть ли с нами обратная связь, интересно ли владельцу наше предложение.

Это основа Open Source проекта.

