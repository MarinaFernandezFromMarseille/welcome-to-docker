# Welcome to Docker

This is a repo for new users getting started with Docker.

You can try it out using the following command.
```
docker run -d -p 8088:80 --name welcome-to-docker docker/welcome-to-docker
```
And open `http://localhost:8088` in your browser.

# Building

Maintainers should see [MAINTAINERS.md](MAINTAINERS.md).

Build and run:
```
docker build -t welcome-to-docker . 
docker run -d -p 8088:3000 --name welcome-to-docker welcome-to-docker
```
Open `http://localhost:8088` in your browser.

### VISUALISATION DE L'EXERCICE

1.D'abord, j'ai construis mon container "welcome-to-docker". il ressemblait à celà:

![Congratulations 1](./src/Images/23.png)

2.J'ai ensuite modifié Le CSS de base dans App.css ainsi que le message d'affichage dans App.js:

![css](./src/Images/21.png)
![js](./src/Images/22.png)

3. Pour que les modifications soient visibles, j'ai d'abbord stoppé puis supprimé mon container, puis je l'ai built et run de nouveau. 

![terminal1](./src/Images/18.png)
![terminal2](./src/Images/19.png)

4. Voilà le résultat des modifications:

![Congratulations 2](./src/Images/20.png)

### DESOLEE J'AI OUBLIE DE COMMIT REGULIEREMENT 😬



