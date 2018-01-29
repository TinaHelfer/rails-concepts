# rails-concepts
# Quelle est la différence entre un site statique et un site dynamique?

- Un site *statique* est un site dont la page visible par le visiteur est perçue comme elle a été concue. La page ne changera pas et c'est en cela qu'elle est statique.


- Un site *dynamique* a été conçu en fonction de *l'interaction du visiteur avec le système*.Le contenu est issu d'une base de données en fonction de critères établis par l'internaute puis mis en page en temps réel.
Comme l'expliquait Félix, Facebook en est un car au lieu de simplement dire bonjour à son utilisateur , comme un site statique, il va interagir avec l'utilisateur en nommant son prénom.


# Qu'est ce qu'un MVC?

Un MVC ou *Model View Controller* est un patron de conception utilisé pour réaliser des sites web. C'est un outil qui permet de comprendre la relation entre les données, l'affichage des informations et les actions de l'utilisateur.

- Model : Etat de l'application web et des données

- View : Est la vision globale de ce que l'on voit à l'écran composé de code HTML

 - Controller : Fait le lien entre la vue et le modèle et gère les interactions avec l'utilisateur. Il est au centre du système.


# Qu'est ce que les routes?

 Les routes permettent de _transformer une URL en une action d’un contrôleur_. On peut créer ses propres routes comme par exemple dans la vidéo de Félix avec :

 ```Rails.application.routes.draw do
     get 'welcome/index'
  end
  ```

# Qu'est ce qu'une base de donnée?

Une base de données est comme un tableau Excel avec plusieurs tables dans laquelle sont _stockées toutes les données d'un thème_ comme par exemple des articles. On peut manipuler la structure , y avoir accès etc... Il existe plusieurs types de modèles de données:

- relationnel : Trie les données dans des _tables_, que l'on appelle aussi des relations, dont chacune se compose de colonnes et de lignes.

- hiérarchique : Le modèle hiérarchique organise les données dans une structure _arborescente_.

- réseau : Implique plusieurs enregistrements connexes. _Un enregistrement_ peut être un membre ou un enfant dans plusieurs ensembles. Chaque ensemble se compose d'un enregistrement parent et d'un ou plusieurs enregistrements enfants.

- orientée objet : Définit une base de données comme une _collection d'objets_, associés à des caractéristiques et des méthodes.

- entité-association ou en étoile : Les éléments constituants la base de données sont appelés _les entités_ et ont des attributs qui sont stockés ensemble dans un domaine. L'une des formes courantes du diagramme entité-association est le schéma en étoile, dans lequel une table centrale des faits se connecte à plusieurs tables dimensionnelles.
etc...



## En rapport avec les bases de données, nous allons voir le concept de migration

La migration est un procédé qui consiste à informer rails qu'il va _modifier la base de données_. On peut en générer avec la commande : rails generate migration suivie du changement.



# Quelle est la différence entre GET et POST ?

 Dans le cas d'un site qui contient des articles:

                                  GET                                                      POST
    Le contrôleur va renvoyer à l'utilisateur la liste de tous les articles  | Le contrôleur va envoyer un formulaire à remplir, il poste un formulaire.

Ces deux méthodes sont utilisées dans des routes.



# Qu'est ce que le CRUD et à quoi sert-il?

 1. Create : créer : méthode *POST*
 2. Read : lire : méthode *GET*
 3. Update : mettre à jour : *PUT*
 4. Delete : supprimer : *DELETE*

Ce sont les quatre opérations de base pour le stockage d'informations en base de données. On peut les associer chacune à une méthode HTTP.             
