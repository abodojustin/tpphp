# Tp PHP Avance

## Objectif du TP:
>Mettre en place un raccourcisseur d’url. Pour ce TP, nous nous sommes inspires du template Caroussel de Bootstrap. 
>Nous allons implementer les fonctionnalites telles que : inscription, connexion et mettre en place un espace membre. 
>Suivez ces etapes pour mettre en place le code base, pour terminer le tp a la prochaine session en matinee puis de créer une api dans l’apres-midi. 
>Pour chaque TP, je mettrais en place un code base.

Priere de suivre les etapes suivantes :
  1. Creer et demarrer votre projet symphony (```symfony serve:start```) ;
  2. Puis etant a la racine du projet, vous tapez les commandes suivantes :
      *	```composer install``` ;
      *	```composer require symfony/webpack-encore-bundle``` : pour nous permettre de gerer nos dependances javaScript et css ;
      * Et du coup, il va vous falloir installer [Node js](https://nodejs.org/en/download/) puis taper ```npm install``` ;
      * ```npm install bootstrap sass sass-loader chart.js @fortawesome/fontawesome-free```;
      * Puis vous ouvrez le projet avec l’IDE que vous voulez, pour ma part je vais l’ouvrir avec **PHPStorm** ;
      * Puis dans le fichier **composer.json**, indiquer que votre application correspond a une version 8.0 minimum de php ; ```php: >=8.0``` ;
      * Dans le dossier **templates**, decommenter les lignes qui se trouvent dans le fichier _base.html.twig_, pour taper la commande ```npm run dev``` pour voir nos modules geres dans _public/build_ pour un deploiement optimise ;
      * Nous allons créer deux controleurs a l’aide de la commande : ```php bin/console make:controller```. Ils auront pour nom : _UrlController_ et _HomeController_ ; Ca va nous créer pour chacune des deux commandes un dossier _url_ et _home_ dans **templates**, et leur controleur correspondant ;
      * Nous voulons que le point d’entree de notre application soit **HomeController**. Pour le faire nous allons changer les parametres de la route dans _HomeController_ ‘/home’ par ‘/’ et donner le nom ‘app_homepage’ ;
      * Si on fait un ```symfony serve```, nous allons constater qu’on aura une erreur du au fait que nous n’avons pas configurer de bases de donnees pour ce projet.
      
      > Créer une base de donnees dans phpmyadmin, puis renseigner les informations db_user, password et le nom de la bd dans le fichier .env, commenter postgresql ensuite decommenter mysql et redemarrer le projet symfony ;
      * Puis copier le code du fichier _base.html.twig_ du dossier **templates** du projet ensuite vous le collez dans le votre. Pour que bootstrap soit actif, il faudrait l’importer dans le fichier assets/styles/app.scss. > NB : REMPLACER assets/styles/app.css PAR assets/styles/app.scss ;
      * On va lancer la commande ```npm run watch``` pour pouvoir construire les dependances. Pour corriger les erreurs visibles a la sortie de cette commande, il faut : 
      > activer le sass-loader dans le fichier webpack.config.js en decommentant .enableSassLoader() puis relancer le build avec ```npm run watch``` ;
      * Il faudrait bien verifier que dans le app.js, on a bien importer la feuille de styles : _import ‘./styles/app.scss’_ ;
      * Puis copier le contenu du fichier **templates/home/index.html.twig** et coller dans votre projet puis relancer le build et actualisez la page pour voir le rendu.  
      
> Vous devez pouvoir realiser ce code base de votre cote tout seul.
> la prochaine seance nous allons faire de la programmation PHP Avance en life
> Si vous avez des questions n'hesitez surtout pas a me faire un mail.

# Bonne Chance
