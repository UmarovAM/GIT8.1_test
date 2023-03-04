
### Установка git из репозитория
sudo apt-get install git

Настройка git для корректного отображения автора коммитов
git config --global user.name "My Name"
git config --global user.email myEmail@example.com

Инициализация репозитория:
git init
git status


### Работа с git
Чтобы добавить файлы для отслеживания используется команда:
git add имя_файла

После этого изменения файла начнут отслеживаться и его можно закоммитить:
git commit -m "some useful comment here"
git commit -a -m "dev 1"
Изменить commit
git commit -amend

Перед каждым коммитом необходимо проиндексировать файлы, 
которые будут закоммичены. 
git add или git commit -a

Последний коммит в ветке обозначается как HEAD


### Работа с git: отмена изменений
До выполнения индексации:
git checkout имя файла

После индексации:
git reset HEAD имя файла

Откат изменений коммита осуществляется с помощью revert:
git revert HEAD --no-edit
Вместо HEAD можно указать любой id коммита из истории.

Просмотр истории:

git log
git log --oneline
git log --oneline --graph

### Работа с ветками
Создание веток:
git checkout -b имя_ветки
 git branch -v

Слияние веток:
git checkout master
git merge develop

### Клонирование репозитория
Клонировать репозиторий с сервера можно с помощью команды:
git clone https://github.com/

Репозиторий будет помещен в директорию ./имя_репозитория
Просмотр удаленных репозиториев:'
git remote

В ответ мы увидим имена всех существующих удаленных 
репозиториев (по умолчанию обычно origin):
git remote show origin

### Добавление удаленного репозитория

Добавление удаленного репозитория:
git remote add origin https://github.com

Отправка изменения в удаленный репозиторий:
git push origin master

Для того чтобы скачать себе последние изменения из репозитория:
git pull

### 
```
nano error.txt
git add error.txt
git commit -a -m "dev add error"
git log
rm error.txt
git reset --soft89a9a317cf71667194e7cc9254df6fd39796dcb
git rm error.txt
git reset --hard 589a9a317cf71667194e7cc9254df6fd39796dcb
git commit -a -m "finish"
git checkout master
nano gitfile.txt
git merge dev
```

```
git clone https://github.com/UmarovAM/git2.git
git status
cd git2
git status
ls -la
git remote rename origin old-origin
git remote add origin https://github.com/UmarovAM/git2.git
git checkout -b my-branch
nano git2.txt
git diff
git add .
git diff --staged
git commit -m "git2.txt 2"
git log
git diff ec2cb859ee761f2d299bdfd7d068ce9dbfe59042
git push
git push --set-upstream origin my-branch
```
