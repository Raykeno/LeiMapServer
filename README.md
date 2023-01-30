# LeiMapServer

Coté Serveur :

(En PHP surement, un petit framework Symphony + API)
https://digitalfortress.tech/tutorial/rest-api-with-symfony-and-api-platform/

Contexte :

« 
Organisateur de conférences, sujets variées

Application pour les invités,

Elle affiche une carte, avec des autres invités de la conférences sur différents endroits

On appuie un bouton pour dire ou je suis (check in, check out)

Liste des gens dans un endroit (Les gens ont une bio)
 »

https://digitalfortress.tech/tutorial/rest-api-with-symfony-and-api-platform/

Modèle :
- Participant (Nom, Email, Mot de Passe, Biographie)
- Lieu (Nom, Adresse, Image, liste des participants actuel au lieu, location(Apple MapKit))

Coté Serveur (Otto) :
- Serveur PHP REST API
- Database

Requêtes :
(Soit https://… comme adresse source)

* Voir tout les participants :  GET /participants/
* Voir tout les participants dans un lieu :  GET /lieu/$[id]/participants
* Récupérer les infos d’un participant : GET /partcipant/$[id]

Pour pouvoir utiliser le projet, il faut utiliser le CLI de Symfony, php 8.*, composer, et il faut avoir l'extension de SQLite3 de PHP d'activée!

symfony server:start dans le root du projet pour le lancer 
Pour accéder à l'API, il faut aller dans http://localhost:8000/api

à faire :
- Les requêtes avec jointures
- Avoir certains champs nulls
