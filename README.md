# Telegram бот для просмотра мультфильмов
## Первичный запуск
Установка и запуск ~~довльно сложен~~<br>
Потребуется установленный python3 и pip<br>
В консоли вводим
```no-highlight
pip install wget
pip install aiogram
pip install colorama
pip install BeautifulSoup4
pip install requests
pip install lxml
```
Позже будет единый файл со всеми нужными пакетами для установки
После установки всех пакетов открывает config.ini 
И в строку "token" вводим токен бота который можно получить у Bot Father
```no-highlight
token = токен бота
get_id_video = False #отсавляем False если не нужны индивидуальне айди видео
```
## Получение индивидуального ID файла в телеграм 
Для этого
```no-highlight
get_id_video = True
```
Далее запускаем бота и вводим команду /update_db
Это надо для получение свежих ссылок на каждое видео с сайта
После вводим команду /download_video он скачивает все (!!!) видео 
Сохраненные в базу данных "serial.sqlite3"

После скачивания всех видео скидываем боту видео и ждём когда он запишет все id серий к себе в базу

После завершения
Меняем в конфиге 
```no-highlight 
get_id_video = False
```
Что бы он больше не добавлял в базу id и не возникало ошибок
