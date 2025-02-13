# Utiliser une image de base contenant PHP et Nginx
FROM php:7.4-fpm

# Installer Nginx
RUN apt-get update && apt-get install -y nginx && rm -rf /var/lib/apt/lists/*

# Copier les fichiers du jeu dans le conteneur
COPY index.html /var/www/html/
COPY save.php /var/www/html/
COPY results.json /var/www/html/

# Donner les bons droits
RUN chmod -R 777 /var/www/html/results.json

# Configurer Nginx
RUN echo 'server {
    listen 80;
    root /var/www/html;
    index index.html index.php;
    location / {
        try_files $uri $uri/ =404;
    }
    location ~ \.php$ {
        include fastcgi_params;
        fastcgi_pass 127.0.0.1:9000;
        fastcgi_index index.php;
        fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
    }
}' > /etc/nginx/sites-available/default

# Exposer le port 80 pour accéder au jeu
EXPOSE 80

# Démarrer PHP et Nginx
CMD service nginx start && php-fpm
