# GR_4660

## Команды Git
### Основные команды

Две довольно распространённые команды, используемые как сразу после установки Git, так и в повседневной практике для настройки и получения помощи — это *config* и *help*

## Основные команды  
__git add__  
Команда __git add__ добавляет содержимое рабочего каталога в индекс (staging area) для последующего коммита. 

__git status__   
Команда __git status__ показывает состояния файлов в рабочем каталоге и индексе: какие файлы изменены, но не добавлены в индекс; какие ожидают коммита в индексе.

__git diff__  
Команда __git dif_ используется для вычисления разницы между любыми двумя Git деревьями.

__git commit__  
Команда __git commit__ берёт все данные, добавленные в индекс с помощью __git add__, и сохраняет их слепок во внутренней базе данных, а затем сдвигает указатель текущей ветки на этот слепок.

__git clean__  
Команда __git clean__ используется для удаления мусора из рабочего каталога. Это могут быть результаты сборки проекта или файлы конфликтов слияний.

### Ветвление и слияния  
__git branch__  
Команда __git branch__ — это своего рода "менеджер веток". Она умеет перечислять ваши ветки, создавать новые, удалять и переименовывать их.

__git checkout__  
Команда __git checkout__ используется для переключения веток и выгрузки их содержимого в рабочий каталог.

__git merge__  
Команда __git merge__ используется для слияния одной или нескольких веток в текущую. Затем она устанавливает указатель текущей ветки на результирующий коммит.

__git mergetool__
Команда __git mergetool__ просто вызывает внешнюю программу слияний, в случае если у вас возникли проблемы слияния.

__git log__
Команда __git log__ используется для просмотра истории коммитов, начиная с самого свежего и уходя к истокам проекта.
#### Опции
* __--oneline__ – показывает каждый коммит в одной строке. Кроме того, она показывает лишь префикс ID коммита.
*  __--graph__ чтобы просматривать историю в виде дерева.

### Совместная работа и обновление проектов 

__git pull__  
Команда __git pull__ работает как комбинация команд git fetch и git merge, т. е. Git вначале забирает изменения из указанного удалённого репозитория, а затем пытается слить их с текущей веткой.

__git push__  
Команда __git push__ используется для установления связи с удалённым репозиторием, вычисления локальных изменений отсутствующих в нём, и собственно их передачи в вышеупомянутый репозиторий. Этой команде нужно право на запись в репозиторий, поэтому она использует аутентификацию.

__git archive__  
Команда __git archive__ используется для упаковки в архив указанных коммитов или всего репозитория.