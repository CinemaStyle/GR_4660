# Работа с удалёнными репозиториями

## Просмотр удалённых репозиториев

Для того, чтобы просмотреть список настроенных удалённых репозиториев, вы можете запустить команду *git remote*. Она выведет названия доступных удалённых репозиториев. Если вы клонировали репозиторий, то увидите как минимум *origin* — имя по умолчанию, которое Git даёт серверу, с которого производилось клонирование:

*git clone https://github.com/schacon/ticgit*

*Cloning into 'ticgit'...*

*remote: Reusing existing pack: 1857, done.*

*remote: Total 1857 (delta 0), reused 0 (delta 0)*

*Receiving objects: 100% (1857/1857), 374.35 KiB | 268.00 KiB/s, done.*

*Resolving deltas: 100% (772/772), done.*

*Checking connectivity... done.*

*cd ticgit*

*git remote*

*origin*

## Добавление удалённых репозиториев

В предыдущих разделах мы уже упоминали и приводили примеры добавления удалённых репозиториев, сейчас рассмотрим эту операцию подробнее. Для того, чтобы добавить удалённый репозиторий и присвоить ему имя (*shortname*), просто выполните команду *git remote add <shortname> <url>*:

*git remote*

*origin*

*git remote add pb https://github.com/paulboone/ticgit*

*git remote -v*

*origin	https://github.com/schacon/ticgit (fetch)*

*origin	https://github.com/schacon/ticgit (push)*

*pb	https://github.com/paulboone/ticgit (fetch)*

*pb	https://github.com/paulboone/ticgit (push)*

## Получение изменений из удалённого репозитория — Fetch и Pull

Как вы только что узнали, для получения данных из удалённых проектов, следует выполнить:

*git fetch [remote-name]*

Данная команда связывается с указанным удалённым проектом и забирает все те данные проекта, которых у вас ещё нет. После того как вы выполнили команду, у вас должны появиться ссылки на все ветки из этого удалённого проекта, которые вы можете просмотреть или слить в любой момент.

Когда вы клонируете репозиторий, команда *clone* автоматически добавляет этот удалённый репозиторий под именем *«origin»*. Таким образом, *git fetch origin* извлекает все наработки, отправленные на этот сервер после того, как вы его клонировали (или получили изменения с помощью *fetch*). Важно отметить, что команда *git fetch* забирает данные в ваш локальный репозиторий, но не сливает их с какими-либо вашими наработками и не модифицирует то, над чем вы работаете в данный момент. Вам необходимо вручную слить эти данные с вашими, когда вы будете готовы.

## Отправка изменений в удалённый репозиторий (Push)

Когда вы хотите поделиться своими наработками, вам необходимо отправить их в удалённый репозиторий. Команда для этого действия простая: git push <remote-name> <branch-name>. Чтобы отправить вашу ветку master на сервер origin (повторимся, что клонирование обычно настраивает оба этих имени автоматически), вы можете выполнить следующую команду для отправки ваших коммитов:

*git push origin master*

Эта команда срабатывает только в случае, если вы клонировали с сервера, на котором у вас есть права на запись, и если никто другой с тех пор не выполнял команду push. Если вы и кто-то ещё одновременно клонируете, затем он выполняет команду push, а после него выполнить команду push попытаетесь вы, то ваш push точно будет отклонён. Вам придётся сначала получить изменения и объединить их с вашими и только после этого вам будет позволено выполнить push.

## Просмотр удалённого репозитория

Если хотите получить побольше информации об одном из удалённых репозиториев, вы можете использовать команду *git remote show <remote>*. Выполнив эту команду с некоторым именем, например, *origin*, вы получите следующий результат:

*git remote show origin*

*remote origin*

*Fetch URL: https://github.com/schacon/ticgit*

*Push  URL: https://github.com/schacon/ticgit*

*HEAD branch: master*

*Remote branches:*
    
    *master                               tracked*

    *dev-branch                           tracked*

*Local branch configured for 'git pull':*
    
    *master merges with remote master*

*Local ref configured for 'git push':*

    *master pushes to master (up to date)git remote show origin*

*remote origin*

*Fetch URL: https://github.com/schacon/ticgit*

*Push  URL: https://github.com/schacon/ticgit*
  
*HEAD branch: master*
  
*Remote branches:*
    
    *master                               tracked*
    
    *dev-branch                           tracked*
  
*Local branch configured for 'git pull':*
   
    *master merges with remote master*
    
*Local ref configured for 'git push':*
    
    *master pushes to master (up to date)*

