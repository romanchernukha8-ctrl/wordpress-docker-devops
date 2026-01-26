WordPress Docker DevOps Lab

Запуск:
docker compose up -d

Сценарий 1:
Изменить MYSQL_PASSWORD в docker-compose.yml.
Результат: Ошибка подключения к БД в логах.

Сценарий 2:
Изменить ports на 8081:81.
Результат: Сайт недоступен.

Сценарий 3:
Выполнить chmod -R 000 wp/.
Результат: Permission denied в логах.
