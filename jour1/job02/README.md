### VISUALISATION DE L'EXERCICE

D'abord, j'ai construis mon container "welcome-to-docker". il ressemblait à celà:

![Congratulations 1](./images/23.png)

2.J'ai ensuite modifié Le CSS de base dans App.css ainsi que le message d'affichage dans App.js:

![css](./images/21.PNG)
![js](./images/22.PNG)

3. Pour que les modifications soient visibles, j'ai d'abbord stoppé puis supprimé mon container, puis je l'ai built et run de nouveau. 

![terminal1](./images/18.PNG)
![terminal2](./images/19.PNG)

4. Voilà le résultat des modifications:

![Congratulations 2](./images/20.PNG)

### PARTAGE DE L'IMAGE

1. Tout d'abord, je dois me connecter à l'aide de la commmande "docker login -u <username>".

![login](./images/24.PNG)

2. Puis Je rajoute un tag à mon image, mon pseudo ainsi que "latest"

![tag](./images/25.PNG)
3. Puis j'effectue mon partage avec un push.

![push](./images/26.PNG)

### RECUPERATION DE L'IMAGE D'UN COLLABORATEUR 

1.J'ai choisi de récupérer l'image de ma collègue Aicha, et pour ce faire j'ai utilisé un pull avec son pseudo et le nom de son image:

![image Aicha](./images/27.PNG)

2. Je la lance pour ensuite la visualier dans le navigateur:


![image Aicha](./images/28.PNG)


Comme on peut le voir, je peux effectivement la visualiser:


![image Aicha](./images/29.PNG)

### Je N'AI PAS REUSSI A MODIFIER L'IMAGE DE AICHA...















