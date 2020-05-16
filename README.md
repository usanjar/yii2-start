### запуск проекта php-fpm + nginx
скопировать env-example to .env
```bash
cp env-example .env
```
---
run docker containers
```bash
docker-compose up --build
```
### инициализация проекта
```bash
docker-compose exec php  /bin/bash
php init.php
```
настроить db-local.php и запускать миграция
```bash
docker-compose exec php  /bin/bash
php yii migrate
```
### настройка Phpstorm
откройте Yii.php файл `./vendor/yiisoft/yii2/Yii.php` и отметит как текст (Mark as plain text)