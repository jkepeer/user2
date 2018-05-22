1. Создание приложения в докере

Создать 2 докер-приложения {username}/user1, {username}/user2

 * создать Dockerfile-ы на базе https://hub.docker.com/_/nginx/

 * приложения должны отличаться от базового только файлом index.html, для первого там должна быть фраза "Hello user1!", для второго "Hello User2!"

 * созданные докер образы должны быть запушены на docker hub

 *  исходный код (Dockerfile-ы ...) для каждого приложения должен быть залит в отдельные репозитории на github {username}/user1, {username}/user2

Проверка:

docker run -d -p 81:80 {username}/user1

docker run -d -p 82:80 {username}/user2

curl http://localhost:81/index.html - результат должен содержать "Hello User1!"

curl http://localhost:82/index.html - результат должен содержать "Hello User2!"


docker build  -t jkepeer1/user2 .

docker pull jkepeer1/user2
