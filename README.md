# docker-alpine-web-server

Веб сервер для локальной разработки.
Включает в себя 
- apache2
- nginx
- mysql
- php-fpm+xdebug
- mariadb
- adminer
- mailhog
- nodejs
- clickhouse
- elasticsearch
- kibana
- memcached
- sphinx

### Запуск сборки фронтенда 
Если вам нужно собирать фронтенд, то в файле /etc/nodejs/entrypoint.sh указаны команды которые будут запущены при старте образа, в dockerfile можно указать версию nodejs

### ssl сертификаты
Для локальной разработки выпускатся внутри контейнера. Можно будет открыть https://, но браузер будет ругаться.

### Отправка и просмотр писем
Для отправки писем используется smtp от mailhog  
Для просмотра просто зайдите на localhost:8025

Так же имеются подготоввленные конфиги для запуска 
- memcached php7.4 можно распространить на другие версии
- elasticsearch и dashboard kibana
- sphinx
- nodejs + автозапуск сборки описанный выше

Настроить необходимые версии можно в файле .env

В файле docker-compsoe.yaml перечислены севрисы которые можно подключать и отключать по необходимости
