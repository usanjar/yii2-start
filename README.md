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
docker-compose exec php php init.php
```
запуск миграцию
```bash
docker-compose exec php php yii migrate
```
### настройка Phpstorm
откройте Yii.php файл `./vendor/yiisoft/yii2/Yii.php` и отметит как текст (Mark as plain text)