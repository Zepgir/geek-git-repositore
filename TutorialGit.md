# Руководство по работе с Git

<!--- Источник: https://training.github.com/downloads/ru/github-git-cheat-sheet/--->

  [Источник](https://training.github.com/downloads/ru/github-git-cheat-sheet/ "Справочник Git")

>Хорошо бы это все запомнить

## Настройка

* **Настройка информации о пользователе для всех локальных репозиториев** 

* Устанавливает имя, которое будет отображаться в поле автора у выполняемых вами коммитов
$ git config --global user.name "[имя]"

* Устанавливает адрес электронной почты, который будет отображаться в информации о выполняемых вами коммитах

$ git config --global user.email "[адрес электронной почты]"



**Создание репозитория**

* Создаёт новый локальный репозиторий с заданным именем

$ git init [название проекта]

Скачивает репозиторий вместе со всей его историей изменений

$ git clone [url-адрес]



***



## Внесение изменений

Проверка, какие файлы будут добавлены в репозиторий.

git add -n *


**Просмотр изменений и создание коммитов (фиксация изменений)**

$ git status

**Перечисляет все новые или изменённые файлы, которые нуждаются в фиксации**

$ git diff

Показывает различия по внесённым изменениям в ещё не проиндексированных файлах

$ git add [файл]

Индексирует указанный файл для последующего коммита

$ git diff --staged

Показывает различия между проиндексированной и последней зафиксированной версиями файлов

$ git reset [файл]

Отменяет индексацию указанного файла, при этом сохраняет его содержимое

$ git commit -m "[сообщение с описанием]"

Фиксирует проиндексированные изменения и сохраняет их в историю версий


## Просмотр истории

![Пример какой то ](/img/primer.png)
Просмотр и изучение истории изменений файлов проекта

$ git log

История коммитов для текущей ветки

$ git log --follow [файл]

История изменений конкретного файла, включая его переименование

$ git diff [первая ветка]...[вторая ветка]

Показывает разницу между содержанием коммитов двух веток

$ git show [коммит]

Выводит информацию и показывает изменения в выбранном коммите


## Сохранение фрагментов
Сохранение и восстановление незавершённых изменений

$ git stash

Временно сохраняет все незафиксированные изменения отслеживаемых файлов

$ git stash pop

Восстанавливает состояние ранее сохранённых версий файлов

$ git stash list

Выводит список всех временных сохранений

$ git stash drop

Сбрасывает последние временно сохранённыe изменения



## Манипуляции с ветками 

## Игнорирование файлов

Если вы хотите сохранить файлы в локальном каталоге Git, но не хотите фиксировать их в проекте, вы можете добавить эти файлы в свой файл .gitignore, чтобы они не вызывали конфликтов.

Используйте текстовый редактор, например nano, чтобы добавить файлы в файл .gitignore.

nano .gitignore

## Манипуляции с ветками 
 new_story1

Показать список всех веток

git branch	

Создать новую ветку

git branch имяновойветки

Создать новую ветку и переключиться на неё.

git branch -b имяновойветки

Удалить ветку

git branch -D имяветки

## Коммиты

Переименуйте ветку.

git branch -m current-branch-name new-branch-name
new_story

git branch -m current-branch-name new-branch-name
 new_story1

После того, как обновления были помещены в индекс, вы готовы их зафиксировать – создать коммит, что запишет изменения, внесенные вами в репозиторий.

Чтобы зафиксировать индексированные файлы, запустите команду commit с сообщением о коммите (эти сообщения позволяют отслеживать коммиты).

git commit -m "Commit message"

Вы можете сжать все индексированные файлы и отправить коммит с помощью одной команды.

git commit -am "Commit message"

Если вам нужно изменить сообщение о коммите, вы можете сделать это с помощью флага –amend.

git commit --amend -m "New commit message"

## Просмотр информации 

Чтобы вывести историю коммитов для текущей активной ветки, введите:

git log

Также можно просмотреть коммиты, которые изменили определенный файл. Укажите имя файла (даже если он был переименован).

git log --follow my_script.py

Чтобы просмотреть коммиты конкретной ветки можно использовать следующую команду. Она покажет коммиты в ветке a-branch, которых нет в b-branch.

git log a-branch..b-branch

Чтобы просмотреть логи ссылок (reflog) и увидеть, когда ссылки обновлялись в репозитории последний раз, введите:

git reflog

Вы можете запросить любой объект в Git через строку его коммита или хэш в более удобном для восприятия формате.

git show de754f5
(Просмотр информации)

##  Работа с удалёнными репозиториями

git remote

git remote add <name> <url>
  команда git remote — это интерфейс для управления списком записей об удаленных подключениях, которые хранятся в файле /.git/config репозитория


git push <remote> <branch>

  Публикация указанной ветки в удаленном репозитории вместе со всеми необходимыми коммитами и внутренними объектами
  

 для извлечения и загрузки содержимого из удаленного репозитория и немедленного обновления локального репозитория этим содержимым.
 git 
 git pull

## Aff


