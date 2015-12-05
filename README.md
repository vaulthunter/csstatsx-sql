# CSstatsX SQL
Запись статистики csstats в БД MySQL

## Установка
* Выполните импорт файла **csstats.sql** в вашу БД.
* Укажите данные для подключения к БД в исходнике плагина в следующих полях:
```
#define MYSQL_HOST	"localhost"	// хост
#define MYSQL_USER	"root" // пользователь
#define MYSQL_PASS	"" // пароль
#define MYSQL_DB	"amxx" // база данных
```
* Скомпилируйте плагин.

## Информация
* Модуль **CSX** используется для сбора статистики. 
* Ранги игроков обновляются в конце каждого раунда и при дисконнекте.
* Из-за особенности хранения данных в MySQL, плагин вернет наименьший ранг в случае если статистика 2х и более игроков совпадает.
* В **get_stats** используются прямые запросы, т.е. возможен лаг при вызове **/top15**.