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

