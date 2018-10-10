Локальные настройки проекта хранятся в файле .git\config

Вносим изменения

=== CUT HERE ===
[user]
	name = it is me
	email = user@jmail.com
[alias]
	ech = !echo 2>NUL && echo  	OK, it was a git alias used.
	alias = !echo 2>/dev/null && echo  	GiT has no alias command, echo aliases are only configured in settings file. && `git alias `
	stat = status -s --branch	; список веток
	what = whatchanged --first-parent -n 3 --date=iso --format=\"%n%ad %h %s\"
#	Узнать текущий коммит (hash)
	now = log -1
------ 8< ------

