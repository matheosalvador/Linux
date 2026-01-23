# **Objectifs de la Story :**

>En tant qu'expert sécurité, 
je veux configurer les pare-feu (ufw) 
afin que seuls les servicesnécessaires (dont SSH) soient accessibles afin de protéger mes serveurs

# **Critères d'acceptation :**
>
>Aucune action n'est effectuée directement avec root (sudo).
>
>Le service MySQL écoute sur l'interface réseau appropriée.
>
>Un utilisateur SQL spécifique a été créé avec des droits appropriés (restriction des actions possible et à l'interface réseau autorisée).
>
>Une base de données contient au moins une table avec des données.
>
>PDO est activé sur le serveur Apache.
>
>Les scripts PHP sont présents dans /var/www/html.
>
>Le script ne contient pas de mot de passe "en dur" en clair dans un dossier public sans protection.
>
>Le serveur Web peut contacter le port 3306 du serveur BDD.
>
>En ouvrant l'URL http://IP_SRV_WEB/NOM_SCRIPT depuis un navigateur tiers, les données s'affichent.
>
>En cas d'arrêt du service MySQL, la page Web affiche un message d'erreur de connexion propre (pas d'erreur 500).
>
>Afficher l'état du pare-feu.
>
>Par défaut, le pare-feu refuse tout le trafic entrant et accepte tout le trafic sortant.
>
>Les pare-feu autorisent SSH sur les deux serveurs.
>
>Le pare-feu du serveur BDD bloque toute tentative de connexion SQL ne provenant pas du serveur Web.
>
>Les pare-feu sont actifs après un redémarrage des serveurs.