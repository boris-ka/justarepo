## Удаление нескольких последних коммитов из github (сетевого git-репозитория)

https://recalll.co/ask/get/topic/list/5a2f006d1126f4717b429968/0

=== CUT HERE ===
git push <<remote>> +dd61ab23^:master

git rebase --continue
git push <remote_repo> <remote_branch> -f

git rebase -i dd61ab23^

git reset HEAD^ --hard
git push <<remote>> -f

git revert dd61ab23

------ >8 ------

После этой операции в удаленном репозитории произойдет усечение коммитов:
git push https://github.com/user_name/repo_title.git +dd61ab23^:master

?? и затем можно сразу сделать усечение локального репозитория
git revert dd61ab23



## Исключение изменений файла из отслеживания, если он уже находится в репозитории git

Файл уже попал в репозиторий git и его удалять из репозитория не требуется.
Файл должен быть изменен локально, но эти изменения не должны попадать в репозиторий после операций commit.
А также файл не должен отображаться как изменённый при выполнении `git status`

https://stackoverflow.com/questions/936249/how-to-stop-tracking-and-ignore-changes-to-a-file-in-git

git update-index --assume-unchanged [path]


Допустим, в локальный файл .gitignore нужно было внести изменения.
При этом такой совет выполняет не то, что требуется: `git rm --cached .gitignore` - видно, что файл маркируется как удаленный в консоли git и в idea тоже.

$ git rm --cached .gitignore
$ git status
## master...origin/master
D  .gitignore
 M env/default/default.properties

$ git reset
Unstaged changes after reset:
 M .gitignore
 M env/default/default.properties
$ git status
## master...origin/master
M  .gitignore
M  env/default/default.properties

А вот так будет при требуемом результате - файл не отображается вообще
$ git update-index --assume-unchanged .gitignore
$ git status
## master...origin/master
 M env/default/default.properties

