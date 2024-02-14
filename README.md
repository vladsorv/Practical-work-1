# Шпаргалка по работе с Git
## Создание репозитория
```bash
$ mkdir "Practical work 1"
$ cd "Practical work 1"
$ git init
```
## Создание README-файла
```bash
$ touch README.md
```
## Добавляем файл в коммит (два способа: все и выборочно)
```bash
$ git add --all
$ git add README.md
```
## Делаем коммит
```bash
$ git commit -m "Комментарий"
```
## Подключаем git к github
```bash
$ git remote add origin git@github.com:vladsorv/Practical-work-1.git
$ git remote -v
Создаём SSH
cd ~
$ ls -la .ssh/ # вывели список созданных ключей
$ ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub"
# скопировать содержимое ключа в буфер обмена: (нужно передать ключ в GitHub)
$ clip < ~/.ssh/id_ed25519.pub
# Проверка правильности ключа
$ ssh -T git@github.com
# Синхронизируем локальный репозиторий с репозиторием GitHub (перед этим нужно создать репозиторий в GitHub)
$ git push -u origin master
```