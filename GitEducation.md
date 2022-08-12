# Руководство по работе с контролем версий

## Первоначальная настройка git

* `git --version` — проверка установленного git и вывод номера версии;
* `git config --global user.name <name>` — задать глобальное имя пользователя (для всех репозиториев);
* `git config --global user.email <email>` — задать e-mail пользователя (для всех репозиториев);
* `git config --global init.defaultBranch main` — задать имя главной ветки по умолчанию для всех репозиториев.

## Работа с репозиторием

* `git init` — инициализировать репозиторий в текущей директории;
* `git status` — показать текущую ветку и статусы файлов, измененённых/добавленных/удалённых с момента последнего коммита;
* `git status -u` — в явном виде указать, чтобы в статусе отобразились неотслеживаемые файлы, если по умолчанию в git настроено их игнорирование;
* `git add <filename>` — добавить новый файл к отслеживанию или зафиксировать (добавить к индексу) изменённый файл для следующего коммита;
* `git commit -m "message"` — выполнить коммит, указав комментарий;
* `git log` — посмотреть журнал коммитов;
* `git checkout <commit>` — перейти к какой-либо версии, можно указывать первые 4 символа хеш-кода;
* `git diff` — показать отличия текущих файлов от последнего коммита.

---
![Working tree, staging area, and Git directory](https://git-scm.com/book/en/v2/images/areas.png)

## Статусы файлов
* U — untracked
* A — added
* M — modified
* D — deleted
* R — renamed (отображается, когда в индекс добавлен файл и с новым, и со старым именем)

---
![The lifecycle of the status of your files](https://git-scm.com/book/en/v2/images/lifecycle.png)


## Полезные ссылки
Актуальная версия книги Pro Git на [английском](https://git-scm.com/book/en/v2) и [русском](https://git-scm.com/book/ru).

---
_"I’m very happy with git. It works remarkably well for the kernel and is still meeting all my expectations."
— Linus Torvalds_
---

## Ветвление в git

* `git branch` — показать список веток;
* `git branch <name>` — создать новую ветку, указав её имя;
* `git checkout <name>` — переключиться на указанную ветку;
* `git merge <name>` — слияние указанной ветки с текущей;
* `git branch -d <name>` — удаление ветки (черновика) после слияния.