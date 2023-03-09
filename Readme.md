## Анализ рынка недвижимости

### Быстрый старт

  ```sh
  git clone https://github.com/alexkurov/Sber_DS_Final
  ```
  ```sh
  docker-compose up
  ```
  
### Настройки

  Основная часть настроек собрана в конфигурационных файлах в `\src`  
  * `proxies.txt` - список прокси
  * `proxies_stats.txt` - не настроки, создаётся в процессе работы DAG `download`, в файле перечислены прокси с указанием количества удачных (положительное число) или неудачных (отрицательное) попыток подключения
  * `parse_config.txt` - настройки парсинга json данных загруженных web страниц
  * `features.json` - перечисление фичей модели
  * `train.sql` - запрос для получения тренировочной выборки
  * `test.sql` - запрос для получения тестовой выборки
  * `sql\create.sql` - скрипт инициалиазции базы данных

### Директории
* `src` - базовые классы
* `src\model` - данные обученных моделей
* `airflow\dags` - задания
* `data\process` - загруженные файлы страниц, подлежащие обработке
* `data\processed` - обработанные файлы перемещаются в эту папку

### Доступ к базе данных

  Для доступа можно использовать контейнер pgAdmin http://localhost:5050/
  * `hostname`: `db`
  * `port`    : `5432`
  * `username`: `admin`
  * `password`: `admin`    
