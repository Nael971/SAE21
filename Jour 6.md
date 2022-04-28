                                                                      Jeudi 14 avril
                                                                      
Lors du cours d'une heure avec monsieur Druon, j'ai compris qu'il fallait également configurer son fichier personnel le mien /etc/bind/db.LesGobelins.com.
Pour le configurer nous devons faire, nano /etc/bind/db.lesgobelins.com. 

La partie de SOA, est utile en cas de panne du serveur DNS, c’est pour cela qu’il y a le mail du gérant du DNS pour le contacter en cas de soucis.
Ensuite il y a tous les paramètres par défaut qu’il ne faut pas changer comme Serial, Refresh etc… Il est conseiller d’utiliser la commande $ORIGIN LesGobelins.com.
Cela permet de compléter les noms symboliques n’étant pas terminés par un point.


@	IN	NS	dns.LesGobelins.com. 
Permet de dire que le serveur DNS s’appelle LesGobelins.com.

dns = LesGobelins.com.		IN	A	10.214.5.1
Permet de dire que le dns se trouve en 10.214.5.1

www	IN	A	10.214.5.1
Cela permet de dire que le nom symbolique www.LesGobelins.com. Se retrouve en 10.214.5.1

@	IN	A	10.214.5.1
Cela nous permet de taper juste LesGobelins.com. Pour tomber sur le site www.LesGobelins.com. Qui est toujours rattacher à l’adresse 10.214.5. 



![etc bind db LesGobelins com](https://user-images.githubusercontent.com/97044657/165733579-75c3b281-a704-462e-8d6a-29812d17ed02.png)

