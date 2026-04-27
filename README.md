README — BookList (Diallo Mamadou, Diallo Ibrahima, Diallo Fatoumata Binta, Diop Sidy, Kane Aissé)
Application web de gestion de bibliothèque personnelle (Laravel)
Description du projet:
BookList est une application web permettant aux utilisateurs de gérer leur bibliothèque personnelle.
Elle offre une interface moderne et intuitive pour :
•	Ajouter, modifier et supprimer des livres
•	Organiser les livres par catégories
•	Suivre l’état de lecture (À lire, En cours, Terminé)
•	Visualiser des statistiques personnalisées via un tableau de bord
•	Accéder à un site public (Accueil, À propos, Contact)
•	Envoyer un message via un formulaire de contact
Le projet a été réalisé en équipe de cinq étudiants dans le cadre du module de développement web.
Organisation de l’équipe
L’équipe était composée de cinq membres, répartis comme suit :
Frontend (1 personne)
•	Création des pages HTML/CSS
•	Intégration du design
•	Conversion des pages en Blade (.blade.php)
Base de données (2 personnes)
•	Conception du schéma
Le schéma a été conçu pour répondre à une architecture strictement personnelle : chaque utilisateur est isolé dans ses données.
Table users : Gère l'authentification via Laravel Breeze (ID, nom, email, mot de passe).
Table categories : Permet l'organisation par genres (nom, description). Chaque catégorie appartient à un utilisateur unique.
Table books : Stocke les informations des ouvrages (titre, auteur, description, date de publication, note).
Table contacts : Enregistre les messages envoyés depuis la partie publique pour un traitement ultérieur par l'administrateur.

•	Création des migrations, modèles, seeders et factories
Le remplissage de la base a été automatisé pour permettre des tests UI/UX rapides:
Factories : Génération de données aléatoires réalistes (titres de livres, noms d'auteurs) en respectant les champs obligatoires.
Statuts de lecture : Utilisation de générateurs pour distribuer les livres entre les états "À lire", "En cours", et "Terminé".
DatabaseSeeder : Création d'un environnement de test complet avec un utilisateur pré-configuré possédant déjà une bibliothèque remplie pour valider le Dashboard.


•	Mise en place des relations entre les entités
Pour faciliter le travail du Backend, les relations ont été définies pour refléter la structure logique du projet:
One-to-Many (1:N) : Un utilisateur possède plusieurs livres et plusieurs catégories.
BelongsTo : Un livre appartient à une seule catégorie et à un seul utilisateur.
Contraintes d'intégrité : Utilisation de onDelete('cascade') pour les utilisateurs et onDelete('set null') pour les catégories afin d'éviter les données orphelines.

Backend et coordination (2 personnes)
•	Création des routes et controllers
•	Mise en place du CRUD complet (livres, catégories)
•	Développement du tableau de bord
•	Intégration du frontend dans Laravel
•	Coordination générale du projet

Technologies utilisées:
Backend
•	Laravel 10
•	Eloquent ORM
•	Middleware d’authentification (Breeze)
•	Blade (templating)
Frontend
•	HTML5 / CSS3
•	CSS personnalisé
•	Blade Components
Base de données
•	MySQL
Outils
•	Composer
•	Git / GitHub
Le schéma a été conçu pour répondre à une architecture strictement personnelle : chaque utilisateur est isolé dans ses données.
•	Table users : Gère l'authentification via Laravel Breeze (ID, nom, email, mot de passe).
•	Table categories : Permet l'organisation par genres (nom, description). Chaque catégorie appartient à un utilisateur unique.
•	Table books : Stocke les informations des ouvrages (titre, auteur, description, date de publication, note).
•	Table contacts : Enregistre les messages envoyés depuis la partie publique pour un traitement ultérieur par l'administrateur.
