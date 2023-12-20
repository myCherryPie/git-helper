# Гит-помощник

В этом файле будет аннотация курса гит и никакой воды.

---

## Работа с консолью

**pwd** - узнать в какой директории ты сейчас

**cd** - изменить директорию

**cd/** или **cd** ~ - путь в домашнюю директорию

*Если в названиях есть пробелы - пиши их в ковычках!*

**..** - возврат на уровень выше 

**.** - обращение к текущему дерикторию 

**tab** - автозаполнение 

**cd name+tab** - покажет возможные пути

---

**ls** - содержание текущей директории

* **ls -a** - расширенный список содержимого

* **ls** ~ - содержание домашней директории

* **ls ..** - содержание родительской директории

* **/+ 2 click tab** - покажет содержание корневой директории

*Если нужно написать несколько комманд сразу - раздели их &&*

---

## Работа с файлами и директориями

**touch %name.расширение%** - создать файл

**touch ../../name** - создание файла на 2 уровня выше

* **mkdir name** - создание директория
* **mkdir -p имя/имя/имя** - создание структуры директорий
* **mkdir ~ имя** - создание директория в домашней директории
* **mkdir .. имя** -тоже самое, но только в родительской директории

---

**cp name.расширение путь/куда/копировать** - копирование файла

**mv name.расширение** - перемещение файла

**cat neme.расширение** - чтение файла

* **rm name.расширение** - удалить файл
* **rmdir name** - удаление только пустой директории 
* **rm -r name** - принудительно удаление директории со всем содержимым

## Работа с фалом gitconfig

В данном файле хранятся глобальные настройки

**git config --global user.name "youreName"** - установка имени

**git config --global user.email youreEmail** - установка email

**cat ~/.gitconfig** or **git config --list** - чтение файла

## Инициализация репозиторя add & commit

**git init** - инициализация репозитория, запускать из нужного файла

**rm -rf .git** - разгитить репозиторий

**git status** - статус репозитория

**git add name** - подготовка к сохранению файла

**git add --all** или . вместо --all - сохраняем все файлы в папке

**git commit -m** - делаем коммит, -м для подписи произведенных изменений

**git log** - история коммитов

## Проверка наличия SSH ключа

*Проверка делается в домашней директории.*

**ls la .ssh/** - проверка дирректории на ключ

*Если есть неизвестный ключ удалить файл и создать новый.*

**ssh-keygen -t ed25519 -C "email from github"** - генерация ключа
*Генерируется 2 ключа:личный и публичный с расширением pub*

*или*

**ssh-keygen -t rsa -b4096 -C "email from github"** - альтернативный вариант генерации ключа

**pbcopy <~/.ssh/id_ed25519.pub** или подставить **rsa** - копирование потока данных публичного ключа

**ssh -T git@github.com** - проверка ключа

## Связывание локального и удаленного репозитория

**git remote add origin git@github.com:имя аккаунта на гитхаб/имя репозитория на гитхаб** 

**git push -u origin master (or main)** - первая отправка данных на удаленный директорий, далее можно вводить только git push

**git remote set-url origin newURL** - изменение URL удаленного репозитория

## Оформление файла Readme

## - заголовок, кол-во решеток = уровень заголовка

--- - черта-разделитель

**two spase or <br>** - разрыв текста

**two enter** - новый параграф

* text * - выделение курсивом

** text ** - выделение полужирным

~~ text ~~ - зачеркнутый текст

1. text - нумерованный список
2. text

* text - не нумерованный список
- text

[Текст] (URL "Всплывающая подсказка") - ссылка в тексте со всплывающей подсказкой

**```** - оформление кода в тексте, по три ковычки с каждой стороны кода
