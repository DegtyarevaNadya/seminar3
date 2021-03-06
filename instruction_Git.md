# **Инструкция по работе с системой контроля версий Git**
Git (произносится «гит») — распределённая система управления версиями. Проект был создан Линусом Торвальдсом для управления разработкой ядра Linux, первая версия выпущена 7 апреля 2005 года. На сегодняшний день его поддерживает Джунио Хамано.

![Логотип](images/git2.png)

## Инициализация репозитория

Для инициализации репозитория используется команда:

    git init

## Проверка состояния репозитория

Для проверки состояния репозитория можно использовать команду:

    git status


## Добавление версионности

Добавить новый файл в репозиторий можно с помощью команды:

    git add <file name>


## Фиксация изменения

Для фиксации изменений, или записи изменений в репозиторий используется команда:

    git commit -m "Your short message"

## Просмотр истории коммитов

Просматривать изменения, внесенные в репозиторий можно с помощью команды:

    git log

А с помощью параметра -oneline можно вывести сокращенные данные коммита

    git log --oneline


## Переключение между версиями

Для перемещений между коммитами можно использовать команду:

    git checkout ind

Где "ind" - уникальный идентификатор коммита, можно также использовать первые несколько символов

Для перемещения к актуальной версии файла можно использовать

    git checkout master


## Просмотр отличий версий

Для вывода изменений в файлах по сравнению с последним коммитом, используется git diff без параметров

    git diff

Команда git diff позволяет сравнивать два различных коммита.

    git diff <id1> <id2>

## Ветвление в Git

Ветвление в Git позволяет нам работать параллельно с разными задачами в одном репозитории.


## Создание новой ветки

Чтобы создать новую ветку используется команда:

    git branch <имя ветки>

## Слияние веток

Чтобы влить одну ветку в другую нужно находясь на той ветку **куда** вливаем выполнить команду:

    git merge <имя вливаемой ветки>


## Перемещение между ветками

Для перемещения между ветками используется уже знакомая команда "git checkout":

    git checkout <имя ветки>

## Удаление веток

Чтобы удалить локальную ветку в Git нужно выполнить команду:

    git branch -d <имя ветки>

Так можно удалить ветку, данные которой влиты в другую. 
Для принудительного удаления ветки, без проверки слияния можно ипользовать флаг "-D":

    git branch -D <имя ветки>

## Просмотр веток

Для просмотра списка всех существующих локальных веток используется команда

    git branch

Для просмотра удаленных веток используется эта же команда с флагом "-r":

    git branch -r
