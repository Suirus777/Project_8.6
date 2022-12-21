<h2><center>B8.6. Итоговая практическая работа</center></H2> <br>

 Добавить страницу в мои закладки<br><br>
Задание:<br><br>

1. Возьмите исходники простейшего PHP-приложения. <br>
Результат: <br>
<b>Был сделан git clone данного приложения</b><br><br>
 
2. Добавьте docker-compose.yml конфигурацию с двумя сервисами: php и nginx. <br>
Nginx должен использовать готовый докер-образ, сервис php должен собираться из текущей директории. Для этого в репозитории есть Dockerfile.<br>
 Результат: <br>
  <b>Был создан docker-compose.yml c конфигурацией для двух сервисов Nginx и php</b><br><br>

3. Добавьте healthcheck для php-сервиса, который ходил бы на http://nginx и проверял содержимое на наличие строки «works» (это можно сделать через curl и grep). <br>
Результат: <br>
   Был добавлен тест для php - сервиса который проверяет содержимое на наличие строки <b>«works»</b> в течении 5 секунд 5 проверок. <br>
     <b> healthcheck: <br>
      test: curl -sS http://127.0.0.1 | grep -c works > /dev/null<br>
      interval: 5s <br>
      timeout: 5s <br>
      retries: 5 <br></b><br>
Проверка работает: <br>
f03bb3d10875   nginx:alpine    "/docker-entrypoint.…"   16 minutes ago  <b>Up 16 minutes <u> (healthy) </u> </b>  0.0.0.0:80->80/tcp   practik86_web_1 <br>
<br>
4. Запустить приложение через Docker Compose. <br>
Результат: <br>
   Был запущен docker <br> <br>
<b>
root@docker1:practik8.6# docker ps <br>
CONTAINER ID   IMAGE           COMMAND                  CREATED          STATUS                    PORTS                NAMES <br>
f03bb3d10875   nginx:alpine    "/docker-entrypoint.…"   16 minutes ago   Up 16 minutes (healthy)   0.0.0.0:80->80/tcp   practik86_web_1 <br>
7c0e8feceac8   practik86_php   "docker-php-entrypoi…"   35 minutes ago   Up 35 minutes             9000/tcp             practik86_php_1 <br><br>

</b>

5. Результатом проверки будет скриншот из браузера по доступному приложению на http://127.0.0.1:80/ и содержимое docker-compose.yml. <br><br>
Результат: <br>
   Данная работа производилась в Я-облаке <br>
   <a href=http://51.250.90.228/> <b> ссылка на результат работы </b><a>
 <br>
Сервер будет работать, но он прерываемый, также в git будет лежать скриншот ссылки.
 <br>
   
