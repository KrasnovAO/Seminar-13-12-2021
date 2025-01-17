# Инструкция для работы с Git и удалёнными репозиториями

## Что такое Git?
Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.
## Подготовка репозитория
Для создание репозитория необходимо выполнить команду *git init*  в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

## Создание коммитов
Для создания коомита в удаленном репозитории, необходимо воспользоваться известными ранее команда *__git add <наименование файла>__* и сделать коммит командой *__git commit -m <Сообщение коммиту>__*. Чтобы данные изменения внеслись не только в локальный репозиторий, но и в удаленный, находящийся на сервере изпользу команду *__ git push__*
### Git add
Для добавления измений в коммит используется команда *git add*. Чтобы использовать команду *git add* напишите *git add <имя файла>*

### Просмотр состояния репозитория
Для того, чтобы посмотреть состояние репозитория используется команда *git status*. Для этого необходимо в папке с репозиторием написать *git status*, и Вы увидите были ли измения в файлах, или их не было.

### Создание коммитов
Для того, чтобы создать коммит(сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "<сообщение к коммиту>*. Все файлы для коммита должны быть ***ДОБАВЛЕНЫ*** и сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***.

## Перемещение между сохранениями
Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с пепозиторием следующим образом: *git checkout <номер коммита>*

## Журнал изменений
Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда *git log*. Для этого достаточно выполнить команду *git log* в папке с репозиторием

## Ветки в Git
 Ветки в гит нужны для работы в части файла, не внося изменения в основную часть.
 Если необходимо нескольким людям дорабатывать документ или его часть, то для них создается отдельная ветка. При работе в ней, если мы стоим на головной ветке , то не будет видно изменений в файле, которые производятся в других ветках
### Создание ветки

Для того, чтобы создать ветку, используется команда *git branch*. Делается это следующим образом в папке с репозиторием: *git branch <название новой ветки>*

## Слияние веток
Для того чтобы слить информацию из одной ветки в другую, необходимо встать в ту ветку , в которую необходимо слить информацию из другой ветки команндой *__git checkout <имя ветки__*, затем используем комaнду **_git merge <имя ветки>_**

## Удаление веток
Для того чтобы удалить ветку, сначала нужно слить с нее информацию в другую ветку и затем ипользовать команду **_git branch -d <имя ветки>_**, но если вы не хотите сливать ветку, то замени `-d` на `-D`
## Копирование удаленного репозитория

Открой в VS Code папку в которую ты хочешь залить удаленный репозиторий. Вызови терминал. Введи команду **_git clone <ссылка с сайта>_**. Все готово, но неоходимо перейти в этот репозиторий команндой **_cd <наименование папки>_**. Если у удаленного репозитория несколько веток, то нужно узнать их название на сайте и ввести для каждой ветки комманду **_git checkout <наименование ветки>_**.

## Сохранение в удаленный репозиторий

При необходимости внести сохранение в удаленный репозиторий используй команду *__git push__*. А если ты находишься не в головной ветви, то используй комманду *__git push origin <имя ветки>__*

## Выкачивание изменений из удаленного репозитория

Если необходимо выкачать изменения из удаленного репозитория используй комманду
*__git pull__*, но это составная команда, которая использует функцию merge, не забывай об этом!

## Предложение по внесению изменений в чей-либо файл.

Для этого на сайте использую кнопку `Compare & Pull request` и напиши комментарий поясняющий то что ты сделал!