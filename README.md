В репозитории Яндекса мы можем найти зеркала репозиториев для всех версий начиная с 8 – Jessie.

Нам нужно исправить содержимое файла /etc/apt/sources.list

Сперва сделаем резервную копию файла: 
cp /etc/apt/sources.list ~/

Изменим файл: 
mcedit /etc/apt/sources.list

Заменим содержимое файла строками: 
deb http://mirror.yandex.ru/debian/ bullseye main
deb-src http://mirror.yandex.ru/debian/ bullseye main

deb http://mirror.yandex.ru/debian-security bullseye-security main contrib
deb-src http://mirror.yandex.ru/debian-security bullseye-security main contrib

deb http://mirror.yandex.ru/debian/ bullseye-updates main contrib
deb-src http://mirror.yandex.ru/debian/ bullseye-updates main contrib

Запустим: 
sudo apt update
