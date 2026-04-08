# Git - основной рабочий цикл с ветками

##Создать ветку и поработать
git checkout -b index-page(название ветки)  #создать новую ветку и переключиться на нее
nano index.html #создать/редактировать файл
git diff #посмотреть что изменилось
git add index.html #добавить файл в коммит
git commit -m"описание" #Зафиксировать изменения

##Отправить ветку на GitHub
git push origin index-page #Отправить новую ветку на GitHub

##Влить ветку в main
git checkout main #переключиться на ветку
git merge index-page #Влить изменения из ветки
git push #Обновить GitHub

##Синхронизация между двумя PC

git pull  #Забрать последние изменения из GitHub

##Все основные команды:

git init                         #создать репозиторий
git clone https//:bf/jh/lj.git   #скопировать репо
git status                       #посмотреть состояние
git diff                         #посмотреть изменения
git add                          #добавить файл в staging
git commit                       #зафиксирорвать изменения
git push                         #отправить на gitHub 
git pull                         #Забрать
git checkout -b                  #создать ветку и переключиться
git merge                        #слить ветки
git log --oneline                #история коммитов
git stash                        #спрятать изменения
git stash pop                    #вернуть спрятанные изменения
git commit -m                    #закоммитить уже добавленные изменения  
git commit -am                   #добавление + коммит уже отслеживаемых файлов
git commit -amend                #исправитьт последний коммит

##Полный цикл — от базовых команд до разрешения конфликтов
git init / clone          # создать / скопировать репозиторий
git status / diff         # смотреть состояние и изменения
git add / commit / push   # базовый цикл работы
git pull                  # синхронизация между ПК
git checkout -b / merge   # ветки и слияние
git stash / stash pop     # отложить изменения
git log --oneline --graph # история и визуализация веток
merge conflict            # конфликт и его решение

##Как восстановить потерянные коммиты

git reflog                    # найди хэш нужного коммита
git reset --hard ab12345      # вернись к нему

#Или создай новую ветку из потерянного коммита

git checkout -b recovery ab12345
