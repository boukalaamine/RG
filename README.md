Partie 2 : Curl

Après avoir lancé la commande suivante  : 
curl https://fr.wikipedia.org/wiki/Java_EE
Le code HTML a été affiché sur le terminal.
En ouvrant le code source sur le navigateur, j’observe qu’il s’agit du même code source qui est affiché dans les deux affichages présentés précédemment.
La différence entre les deux : 
En exécutant la commande : curl https://fr.wikipedia.org/wiki/Java_EE 
Curl envoie une requête GET à l’URI et affiche la réponse reçue par le serveur.
Avec le navigateur, il y a des échanges de messages HTTP basés sur des requêtes d’envoi et de réception.

2) En lançant la commande  :
curl https://httpbin.org/image
Le message suivant est affiché  : 
{"message": "Client did not request a supported media type.", "accept": ["image/webp", "image/svg+xml", "image/jpeg", "image/png", "image/*"]}

Ainsi, on relance la commande en spécifiant le format accepté.

Par exemple :

La commande  : 
curl https://httpbin.org/image/jpeg --output projet/file.jpeg 
nous a permis d’enregistrer l’image .jpeg dans le répertoire projet sous le nom file.jpeg
Nous avons obtenu le résultat suivant dans le terminal  : 



L’image enregistrée est la suivante  : 


De manière analogue, nous pouvons enregistrer tous les autres formats proposés et acceptés.

La requête pour obtenir le résultat attendu est  :

curl -X GET --header 'Accept: application/json' 'https://en.wikipedia.org/w/api.php?action=query&prop=revisions&titles=Bertrand_Russell&format=json&rvend=20170729000000&rvstart=20170801000000' 

