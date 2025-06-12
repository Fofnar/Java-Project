Space Shooter 2D (Java / LibGDX / Tiled) 

Rapport de projet 

🎖 Contributions clés (Fodeba Fofana) 

Architecte moteur & gameplay : conception et implémentation du coeur du moteur de jeu (mécaniques de tir, collisions, IA, progression dynamique) 

Intégration avancée de Tiled : choix technique, configuration de OrthogonalTiledMapRenderer et chargement des maps .tmx 

Qualité & tests : élaboration de la stratégie testing (unitaires & intégration), 80 % de couverture 

CI/CD & déploiement : setup des pipelines Jenkins, scripts Gradle pour build et exécution 

🎮 Introduction 

Ce projet vise à créer un jeu 2D de type Space Shooter avec LibGDX, où le joueur contrôle un vaisseau spatial pour combattre des ennemis, accumuler des points et monter en niveau. La difficulté augmente progressivement pour offrir une expérience dynamique et engageante. L'intégration de Tiled permet de gérer des arrière-plans variés et interactifs, enrichissant l'univers graphique. 

 

🚀 Fonctionnalités principales 

Gameplay & progression 

Contrôle du vaisseau : déplacements dans les quatre directions. 

Combat & score : élimination d’ennemis pour gagner des points et monter en niveau. 

Difficulté adaptative : ennemis plus nombreux/rapides selon le score. 

Graphismes & modularité 

LibGDX : moteur de jeu, gestion des graphismes, entrées utilisateur. 

Tiled : création d’arrière-plans (.tmx) avec OrthogonalTiledMapRenderer et TmxMapLoader. 

Architecture modulaire : ajout futur facile de niveaux, ennemis ou objets interactifs. 

Son & interface 

Gestion sonore : réglage volume via touches increase/decrease dans le menu Settings. 

Échappatoire : quitter la partie avec la touche Échap pour revenir au menu principal. 

 

🛠️ Technologies & outils 

Java 17 

LibGDX 1.13.1 

Tiled (TMX maps) 

Gradle (build & exécution) 

Git (versioning) 

CI/CD : intégration des builds via scripts Gradle 

 

📦 Installation & exécution 

Prérequis : Java 17, Gradle (ou ./gradlew fourni) 

Compilation : 

./gradlew core:build lwjgl3:build 
  

Exécution : 

./gradlew lwjgl3:run 
  

Génération du JAR : 

./gradlew build 
  

Si ./gradlew non reconnu, utilisez gradle. En cas d’erreur, vérifiez la version Java. 

 

🗂️ Configuration Tiled 

Ouvrir assets/maps/FullBackground.tmx dans Tiled. 

Ajouter/éditer des tuiles (dans assets/tiles/). 

Si FullBackground.tmx est manquant, le fond par défaut background.txt est chargé. 

 

📐 Architecture du moteur 

Organisé en packages : 

state : gestion des écrans (menu, play) 

play : logique de jeu (moteur, entités) 

key : gestion des entrées clavier 

sound : gestion audio 

 

⚙️ Extensibilité 

Pour ajouter un ennemi : 

Créer une classe étendant Enemy. 

Modifier la vitesse ou le comportement via setters. 

Utiliser Play pour configurer nombre d’ennemis/par niveau. 

Pour ajouter des objets : utiliser Item et ajuster Play. 

 

🔗 Références 

Documentation LibGDX : https://libgdx.com 

Tutoriels Tiled : https://gamefromscratch.com/libgdx-tutorial-series/ 

 

 

🎯 Perspectives 

Menu de configuration des touches clavier. 

Système de meilleurs scores via JSON. 

Nouveaux types d’ennemis et textures dynamiques. 

 

🤝 Contribution de Scotto Lucas 

Développement de l’interface menu et de la gestion sonore 

Rédaction de la documentation utilisateur et diagrammes UML 

 
