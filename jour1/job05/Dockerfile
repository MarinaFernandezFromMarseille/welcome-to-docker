### Dockerfile
FROM nginx:latest

# Copier les fichiers du jeu dans le répertoire HTML de Nginx
COPY index.html /usr/share/nginx/html/
COPY save.php /usr/share/nginx/html/

# Installer PHP et les extensions nécessaires
RUN apt-get update && apt-get install -y php-fpm && rm -rf /var/lib/apt/lists/*

# Configuration Nginx pour interpréter PHP
RUN echo 'server {
    listen 80;
    root /usr/share/nginx/html;
    index index.html index.php;
    location / {
        try_files $uri $uri/ =404;
    }
    location ~ \.php$ {
        fastcgi_pass 127.0.0.1:9000;
        fastcgi_index index.php;
        include fastcgi.conf;
    }
}' > /etc/nginx/conf.d/default.conf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]

### docker-compose.yml
version: '3.8'

services:
  web:
    build: .
    ports:
      - "8080:80"
    volumes:
      - game-results:/usr/share/nginx/html
    container_name: morpion_game

volumes:
  game-results:
    driver: local