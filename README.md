1. Первым делом, для работы сервера, устанавливаем глобально npm пакет `tileserver-gl-light`
   ```
   npm install -g tileserver-gl-light
   ```
   

2. Скачиваем репозиторий, со всеми необходимыми ресурсами, для локального сервера [Ссылка на архив](https://disk.yandex.ru/d/NfjsE3u2AS_UzQ)
3. В папке `tileserver-gl/mbtiles` распаковываем файлы `*.mbtiles` из архива `mbtiles.zip` и кладем их сюда же
4. В файле `config.json`, можно изменить свойство `options.domains` на нужный хост по которому будем получать данные карты (остальное не трогаем)
5. В консоли запускаем сервер с помощью команды (укзываем путь до `config.json`):
    ```
    tileserver-gl-light --config <pathToServer>/tileserver-gl/config.json
    ```
   - в консоли должны увидеть следующее:

   ![ConEmu64_g4GroO1Dtf](https://github.com/starmatf/opti-tileserver/assets/21096671/5fdda2ec-01e2-4cc7-b2f1-ba2621c6027f)
   - если всё гуд, то можем проверить работу сервера перейдя по ссылке `http://localhost:8080/styles/basic/` (по умолчанию)
