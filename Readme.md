# Команда Git
## Состояние репозитория.
### Команда $git status выводит статус репозитороия: добовление и удаление файлов а так же их изменение.
## Сохронение файлов в репозитории.
### Команда $git add сохраняет файлы в репозитории. Команда $git add --all сохранит все файлы в репозитории. Команда $git add. добавляе в репозиторий текущую папку со всеми файлами
## Коммит
### 1. Команда $git commit -m "коммит" присвоет коммит всем файлам в репозитории.
### 2. Команда $git log выводит список коммитов, команда $git log --oneline выведит краткий список.
## Связование репозиториеев
### Для связывания локального и удалённого репозитория используются команды $git remote add ИМЯ_РЕПОЗИТОРИЯ SSH_ССЫЛКА и $git push -u ИМЯ_РЕПОЗИТОРИЯ. SSH ссылку можно найти на удалённом репозитории [GitHub](https://github.com/) Для удаления связи с репозиторием используется комнда $git remote remove ИМЯ_РЕПОЗИТОРИЯ.
# Файл HEAD
### Файл HEAD один из служебных файлов в папке git он указывает на коммит который сделан последним.
### $pwd # где мы наход
### $cd .git/ #переходим в скрытую папку git
### $ls # смотрим содержимое папки
### $cat HEAD # показывает содержимое файлов
### В файле будет н6аходится ссылка ref:refs/heads/master. В этом файле будет находится хеш последнего коммита
# Статусы файлов репозитория
## Untraked (неотслеживаемый)
### Статус новых файлов
## Stage (подготовка)
### данный статус присваевается файлу после команды $git add
## Traked (отслежеваемый)
### файлы которые зафиксированные $git commit
## Modified (изменённый)
### данный статус означает что команда git сравнивал содержимое файла с последним сохранённым версией и нашёл отличие

```mermaid
%% Схему изменения статусов
graph LR
untacked --"git add"--> staged
staged --"git commit"--> traked
traked --"изменяем файл"--> modifire
modifire --"git add"--> staged
```
