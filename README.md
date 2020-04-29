# Перед merge request

git fetch -all
git rebase origin/master
git push origin Branche_Name\* \*Если ветка отстала от master: git push --force

# Push процесс ветки

Простые коммиты: git push
Ammend коммиты: git push --force

# Pull процесс ветки

git fetch --all 2.1. Если последний был простой коммит: git pull 2.2. Если работа перетекла из офиса в дом или наоборот: git reset --hard origin Branche_Name

# Переименование ветки
git branch -m old_name new_name

# Массовые операции над коммитами (удаление, переименование и т.д.)

git rebase -i HEAD~n (n-число последних коммитов на корректировку)
Делаем изменения
git push --force

# Удаленное удаление несуществующих веток

> git fetch --prune

# выборочное удаление коммита

git reset --soft HEAD^

# как установить редактор по умолчанию git

git config --global core.editor "ваш редактор"

# Как склеить коммиты squash

Сначала узнаем, сколько коммитов нужно склеить. Эта команда покажет, какие коммиты у вас прибавились по сравнению с веткой master:

> git cherry -v master

А эта — сколько их всего:

> git cherry -v master | wc -l

затем:

> git rebase -i HEAD~3

флаг -i — значит в интерактивном режиме.

> pick: 234432423 тут ваш коммит // на который хотим склейить

> squash: 234432423 тут другой ваш коммит // удалятся

> squash: 234432423 тут другой ваш коммит // удалятся

То есть я говорю гиту «используй первый коммит, а остальные приклей к нему».
выход с сохранением
Гит склеивает коммиты и предлагает мне ввести коммит-месседж (показывает коммит-месседжи всех склеенных коммитов): комментируем # не нужные коммиты и сохраняем

> git push --force
