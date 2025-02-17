# Utiliser l'image officielle Nginx
FROM nginx:alpine

# Copier les fichiers de l'application dans le conteneur
COPY index.html /usr/share/nginx/html/index.html
COPY save.php /usr/share/nginx/html/save.php
COPY results.json /usr/share/nginx/html/results.json

# Créer un volume pour sauvegarder les résultats du jeu
VOLUME /usr/share/nginx/html/results.json

# Exposer le port 80 pour Nginx
EXPOSE 80

# Démarrer Nginx
CMD ["nginx", "-g", "daemon off;"]
