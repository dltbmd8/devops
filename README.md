Проект демонстрирует настройку веб-сервера Nginx с HTML-страницей "Hello, DevOps World!" и его запуск через Docker-контейнер.

   Локальный запуск Nginx

1. Установите Nginx:
   sudo apt update
   sudo apt install nginx -y
2. Скопируйте index.html:
   sudo cp index.html /var/www/html/index.html
3. Перезагрузите Nginx:
   sudo systemctl restart nginx
4. Откройте в браузере
   http://localhost

Запуск через Docker Запуск через Docker

Dockerfile:
FROM nginx:latest
COPY index.html /usr/share/nginx/html/index.html
EXPOSE 80

1. Постройте образ:
   docker build -t nginx-devops .
2. Запустите контейнер:
   docker run -d -p 8080:80 nginx-devops
3. Проверьте страницу:
   http://localhost:8080

   Работа с Git

1. Клонируйте репозиторий:
   git clone https://gitlab.com/username/your-repository.git
   cd your-repository
 2. Создайте ветку `dev`, добавьте изменения и сделайте коммит:
   git checkout -b dev
   git add .
   git commit -m "Add project files"
   git push origin dev
3. Смержите с основной веткой:
   git checkout main
   git merge dev
   git push origin main


