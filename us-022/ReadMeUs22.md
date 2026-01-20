# **Objectifs de la Story :**

En tant qu'expert sécurité, 
je veux configurer un pare-feu (ufw) pour n'autoriser que le trafic HTTP (80) et SSH (22), 
afin de protéger le serveur.

# **Critères d'acceptation :**

Aucune action n'est effectuée directement avec root (sudo).

Le serveur Apache2 est actif.

La page d'accueil personnalisée est accessible via l'adresse IP du serveur depuis un poste client.

Les droits sur le répertoire /var/www/html sont restreints.

Le pare-feu est activé, même suite à un redémarrage du serveur.

Seuls les deux ports utilisés répondent positivement aux scans.

Un test de connexion sur un port non autorisé échoue.

L'outil htop est fonctionnel.

Cibler spécifiquement le service SSH dans les journaux système.

Limiter l'affichage aux erreurs récentes dans les journaux système.

Utiliser le mode "suivi en temps réel" pour observer les tentatives de connexion quand elles se produisent.

Afficher les lignes des journaux système concernant une connexion réussie.

Afficher les lignes des journaux système concernant un utilisateur inconnu.

Compter le nombre d'échecs de connexion.

Afficher les lignes des journaux système concernant une erreur de mot de passe.

Trouver l'adresse IP qui a provoqué une erreur de connexion.