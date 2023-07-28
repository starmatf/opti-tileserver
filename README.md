1. Первым делом, для работы сервера, устанавливаем глобально npm пакет `tileserver-gl-light`
   ```
   npm install -g tileserver-gl-light
   ```
   

2. Скачиваем подготовленный архив, со всеми (почти...) необходимыми ресурсами, для локальной работы карты [Ссылка на архив](https://disk.yandex.ru/d/NfjsE3u2AS_UzQ)

   - в архиве не хватает основного файла с данными OSM. К сожалению Яндекс Диск не позволяет загружать файлы больше 50гб, поэтому его качаем по [ссылке](https://osmlab.github.io/osm-qa-tiles/). Далее распаковываем файл с расширением `.mbtiles` в папку `tileserver-gl/mbtiles` и переименовываем его в `OSM.mbtiles`


3. В файле `config.json`, можно изменить домен и порт по которому будем получать данные карты (остальное не трогаем)

   ![image](https://private-user-images.githubusercontent.com/21096671/256735201-960e0660-5b5c-45eb-bac5-0b5eaff23c54.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTEiLCJleHAiOjE2OTA1MjM2NTMsIm5iZiI6MTY5MDUyMzM1MywicGF0aCI6Ii8yMTA5NjY3MS8yNTY3MzUyMDEtOTYwZTA2NjAtNWI1Yy00NWViLWJhYzUtMGI1ZWFmZjIzYzU0LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFJV05KWUFYNENTVkVINTNBJTJGMjAyMzA3MjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjMwNzI4VDA1NDkxM1omWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWI0MDEzMTc0YTdjOTA2NzUxOTNkMGMxZWEwMTM2YWM0OTVjYmQ5ZWRiM2YwMjRmOTg4OWMxZTVkN2E4NjNiOTMmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.nsSPtaWQr9CRT2LLiO9gYmWuUdvFJKGCw9uyH7wHmeU)


4. В консольке переходим в нашу папку `/tileserver-gl/` и отсюда запускаем сервер с помощью команды: 
    ```
    tileserver-gl-light --config config.json
    ```
   - в консоли должны увидеть следующее:

   ![image](https://private-user-images.githubusercontent.com/21096671/256735238-32d1b743-d803-4f40-a325-d9d96f349938.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTEiLCJleHAiOjE2OTA1MjM2NTMsIm5iZiI6MTY5MDUyMzM1MywicGF0aCI6Ii8yMTA5NjY3MS8yNTY3MzUyMzgtMzJkMWI3NDMtZDgwMy00ZjQwLWEzMjUtZDlkOTZmMzQ5OTM4LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFJV05KWUFYNENTVkVINTNBJTJGMjAyMzA3MjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjMwNzI4VDA1NDkxM1omWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTU4MGEzOWQyMDBhNTgyMmI3ZGMyMTVhZDI5YmFiYjUyZWUwYjI1OGFiYmU1ZWZjMmFmYTZjNDgzMjNjMzJiZDUmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.z2wUxjDHLhcNdkG19XpvUGQp7r03t21UaX6VUwJlh0o)

   - если всё гуд, то можем проверить работу сервера перейдя по ссылке `http://localhost:8080/styles/basic/`
