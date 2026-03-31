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
