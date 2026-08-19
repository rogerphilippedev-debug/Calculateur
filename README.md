Kover
​
Présentation et Objectifs de Kover
• Kover est une application web métier (Single Page Application) conçue selon une approche mobile-first pour les équipes de vente en magasin.
• Son objectif est d'estimer instantanément et de manière fiable les quantités de matériaux nécessaires pour des projets de décoration murale.
• L'outil optimise le temps de conseil client tout en limitant les risques d'erreurs de métrage (surplus ou manque de marchandise).

Modules Fonctionnels de l'Application
• L'application propose une interface dynamique séparée en trois modules de calcul métiers, ainsi qu'un espace collaboratif :
• Papier Peint : Calcul du nombre de rouleaux intégrant les algorithmes de pertes liées aux raccords (raccord droit, raccord sauté) et la gestion par dimensions murales ou surface au sol.
• Adhésifs & Carreaux : Évaluation du nombre de paquets requis en fonction du conditionnement (pièces/paquet) et de la surface cible.
• Moulures & Cimaises : Calepinage des baguettes pour des poses linéaires ou la création d'encadrements décoratifs multiples.
• Espace Collaboratif : Compteur en ligne synchronisé en temps réel affichant le nombre de vendeurs actuellement connectés à l'outil.

Architecture Technique et Technologies Utilisées
• Kover repose sur une architecture Serverless garantissant rapidité de déploiement et haute disponibilité :
• Frontend : HTML5, CSS3 natif (utilisation avancée de Flexbox, variables CSS et effets Glassmorphism via backdrop-filter), et JavaScript Vanilla (ES6+).
• BaaS (Backend as a Service) : Intégration du SDK Firebase v8 pour l'authentification et l'utilisation de la base de données temps réel.
• Infrastructures tiers : Hébergement web via GitHub Pages et suivi télémétrique via Google Analytics.

Sécurité et Configuration Firebase
• Afin de protéger cet outil interne, une politique de sécurité stricte est appliquée sur l'authentification et l'accès aux données :

Contrôle d'Accès par Domaine d'Email
• ​Restriction de domaine : L'interface JavaScript rejette toute tentative de création de compte ou de connexion provenant d'e-mails n'appartenant pas aux domaines professionnels autorisés.

Validation Sécurisée des Données en Temps Réel
• ​Règles Realtime Database : Les opérations de lecture et d'écriture sur le nœud visiteurs_actifs sont soumises à une double vérification côté serveur : la présence d'un token d'authentification valide ET la vérification par expression régulière (regex) du domaine de l'utilisateur.

Protection de la Vie Privée et Conformité RGPD
• ​RGPD : Les calculs sont exécutés exclusivement côté client (navigateur). Aucune dimension de projet ni donnée personnelle client n'est collectée ou transmise au serveur.
