# Домашнее задание к занятию "`Git`" - `Парфенова Елена`



---

### Задание 1
Что нужно сделать:

    Зарегистрируйте аккаунт на GitHub.
    Создайте новый отдельный публичный репозиторий. Обязательно поставьте галочку в поле «Initialize this repository with a README».
    Склонируйте репозиторий, используя https протокол git clone ....
    Перейдите в каталог с клоном репозитория.
    Произведите первоначальную настройку Git, указав своё настоящее имя и email: git config --global user.name и git config --global user.email johndoe@example.com.
    Выполните команду git status и запомните результат.
    Отредактируйте файл README.md любым удобным способом, переведя файл в состояние Modified.
    Ещё раз выполните git status и продолжайте проверять вывод этой команды после каждого следующего шага.
    Посмотрите изменения в файле README.md, выполнив команды git diff и git diff --staged.
    Переведите файл в состояние staged или, как говорят, добавьте файл в коммит, командой git add README.md.
    Ещё раз выполните команды git diff и git diff --staged.
    Теперь можно сделать коммит git commit -m 'First commit'.
    Сделайте git push origin master.

В качестве ответа добавьте ссылку на этот коммит в ваш md-файл с решением.

Решение 1
sudo apt-get install git
git clone https://github.com/elenaparf/git.git

cd git
git config --global user.name "elenaparf"
git config --global user.email "elenaparf28@gmail.com"
git init
git status
меняем файл readme.md
git add README.md
git status
git commit -m "Edit README.md file"
git push origin master
нет ветки master
git checkout -b master
git commit -m "Edit README.md file"

по логину и паролю доступ закрыт с 2021 года, поэтому на гите надо создать персональный токен по инструкции https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#creating-a-personal-access-token-classic

еще раз     git push origin master 
имя пользователя elenaparf, а вместо пароля  - скопированный токен
успешно
вот ссылка на коммит:

https://github.com/elenaparf/git/commit/b4358d6d9877c9e80d61ca1b33fc275705d1d7b0


---

### Задание 2
Что нужно сделать:

    Создайте файл .gitignore (обратите внимание на точку в начале файла) и проверьте его статус сразу после создания.
    Добавьте файл .gitignore в следующий коммит git add....
    Напишите правила в этом файле, чтобы игнорировать любые файлы .pyc, а также все файлы в директории cache.
    Сделайте коммит и пуш.

В качестве ответа добавьте ссылку на этот коммит в ваш md-файл с решением.
`Приведите ответ в свободной форме........`

Решение 2
touch .gitignore
git status
git add .gitignore
sudo nano .gitignore
		*.pyc
cache/
git status
git commit -m "Add .gitignore file with rules for ignoring .pyc and cache files"
git push origin master
ссылка на коммит https://github.com/elenaparf/git/commit/c8f89a65f2c1ab52c38229b7cde27c023959be15


---

### Задание 3
Что нужно сделать:

    Создайте новую ветку dev и переключитесь на неё.
    Создайте в ветке dev файл test.sh с произвольным содержимым.
    Сделайте несколько коммитов и пушей в ветку dev, имитируя активную работу над файлом в процессе разработки.
    Переключитесь на основную ветку.
    Добавьте файл main.sh в основной ветке с произвольным содержимым, сделайте комит и пуш . Так имитируется продолжение общекомандной разработки в основной ветке во время разработки отдельного функционала в dev ветке.
    Сделайте мердж dev ветки в основную с помощью git merge dev. Напишите осмысленное сообщение в появившееся окно комита.
    Сделайте пуш в основной ветке.
    Не удаляйте ветку dev.

В качестве ответа прикрепите ссылку на граф коммитов https://github.com/ваш-логин/ваш-репозиторий/network в ваш md-файл с решением.


Решение 3
git checkout -b dev
touch test.sh
git add test.sh
sudo nano test.sh
git commit -m "commit1 test.sh"
git add test.sh
git push origin dev
	так 3 раза
git checkout master
touch main.sh
git add main.sh
git commit -m "commit1 main.sh"
sudo nano main.sh
git commit -m "commit2 main.sh"
git push origin master
git merge dev
git push origin master


https://github.com/elenaparf/git/network

`При необходимости прикрепитe сюда скриншоты
![Название скриншота](ссылка на скриншот)`
