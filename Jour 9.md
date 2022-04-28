                                                            Vendredi 22 avril
  
  
  
  ![LesGobelins conf](https://user-images.githubusercontent.com/97044657/165785861-54daade7-78c9-47fd-aaba-91020139ae88.png)

Lors de ce dernier TP, j'utilise la commande a2ensite LesGobelins.conf car a2ensite est une commande qui permet
de mettre notre site dans /etc/apache2/sites-enables qui sont les sites autorisés à l'affichage.
Une fois activé, il suffit de reload apache2.
Ensuite, à l'aide, de la commande nano /etc/hosts je configure 127.0.0.1 www.LesGobelins.com
Et 10.214.5.1 en 214-5.
Le Hosts est très important, car c'est lui qui est interrogé en premier avec une requête DNS sur les serveurs d'adresse du Web.
Il convertit les noms d'hôtes en adresses IP numériques.

![etc hosts](https://user-images.githubusercontent.com/97044657/165786699-f5f5c20b-a1d2-4721-a729-45c993566776.png)


Ensuite, il faut changer de nameserver car je suis dans celui de l’iut en 10.255.255.200
or lorsque l’on va rechercher notre site il sera introuvable car l’iut est relié « au monde ». Donc on le remplace par l’adresse IP de notre pc. 


![définir notre adresse de serveur avec etc resol conf](https://user-images.githubusercontent.com/97044657/165788951-b473e3e8-75d3-492c-a708-4818e7e28e2a.png)

Je teste la zone, pour voir si elle est correcte en faisant :

![test de la zone](https://user-images.githubusercontent.com/97044657/165790141-39a6bfd7-d4aa-4316-9602-2cf08848312a.png)

Il ne me reste plus qu’a faire les tests avec différents dig pour voir si j'arrive à avoir la page html.


![dig www lesgobelins com](https://user-images.githubusercontent.com/97044657/165791176-e355fc52-7169-4bf4-ae8a-ea2ab38bb003.png)
![dig lesgobelins com](https://user-images.githubusercontent.com/97044657/165791194-85b9a8ec-9429-4d83-84d6-dd850be46024.png)


![www lesgobelins com](https://user-images.githubusercontent.com/97044657/165792338-624b9f77-527d-434a-9870-7091b5956f83.png)
![lesgobelins com](https://user-images.githubusercontent.com/97044657/165792384-a853fa2f-5a0a-447b-8eb0-c7c983c48679.png)

C’est bon, j'ai réussi à configurer le serveur DNS et à savoir utiliser les éléments du serveur Web pour réussir cet exercice.
