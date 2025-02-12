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

D'abord, j'ai construis mon container "welcome-to-docker". il ressemblait à celà:

![Congratulations 1](./src/Images/23.png)

2.J'ai ensuite modifié Le CSS de base dans App.css ainsi que le message d'affichage dans App.js:

![css](./src/Images/21.PNG)
![js](./src/Images/22.PNG)

3. Pour que les modifications soient visibles, j'ai d'abbord stoppé puis supprimé mon container, puis je l'ai built et run de nouveau. 

![terminal1](./src/Images/18.PNG)
![terminal2](./src/Images/19.PNG)

4. Voilà le résultat des modifications:

![Congratulations 2](./src/Images/20.PNG)

### PARTAGE DE L'IMAGE

1. Tout d'abord, je dois me connecter à l'aide de la commmande "docker login -u <username>".

![login](./src/Images/24.PNG)

2. Puis Je rajoute un tag à mon image, mon pseudo ainsi que "latest"

![tag](./src/Images/25.PNG)

3. Puis j'effectue mon partage avec un push.

![push](./src/Images/26.PNG)

### RECUPERATION DE L'IMAGE D'UN COLLABORATEUR 

1.J'ai choisi de récupérer l'image de ma collègue Aicha, et pour ce faire j'ai utilisé un pull avec son pseudo et le nom de son image:

![image Aicha](./src/Images/27.PNG)

2. Je la lance pour ensuite la visualier dans le navigateur:


![image Aicha](./src/Images/28.PNG)


Comme on peut le voir, je peux effectivement la visualiser:


![image Aicha](./src/Images/29.PNG)















