# Установка программ внутри докер-машины

Интересует установка именно для VBox докера, а не контейнера


## Попасть внутрь VBox boot2docker:
`$ docker-machine ssh`


## Установка программ внутри докер-машины


Загрузка дистрибутивов из интернет:
`tce-load -wi vim.tcz`

`tce-load -wi mc.tcz`

Запустить его не удалось, вывод ошибки в консоль:
docker@default:~$ mc
Unknown terminal: cygwin
Check the TERM environment variable.
Also make sure that the terminal is defined in the terminfo database.
Alternatively, set the TERMCAP environment variable to the desired
termcap entry.


Или такая ошибка:
docker@default:~$ nano
Error opening terminal: cygwin.

wget и curl уже присутствуют, но, возможно, это не "канонические" версии, а специальные обрезки под busybox

