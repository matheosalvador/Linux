# **Objectifs de la Story :**

En tant que responsable d'équipe, 
je veux créer un dossier /opt/partage où tous les membres du groupe peuvent lire et écrire des fichiers, 
mais où les autres n'y ont aucun accès.

# **Critères d'acceptation :**

Aucune action n'est effectuée directement avec root (sudo).

Existence d'au moins trois utilisateurs tests dans le groupe.

Un script permet de créer un utilisateur.

Le script ne plante pas si l'utilisateur à créer existe déjà.

Un script permet de supprimer proprement un utilisateur.

Le script effectue le nettoyage du répertoire /home de l'utilisateur.

Le script ne plante pas si l'utilisateur à supprimer n'existe pas.

Le répertoire /opt/partage appartient à root pour le propriétaire et à projet_linux pour le groupe.

Les droits interdisent tout accès aux utilisateurs n'appartenant pas au groupe.

Tout nouveau fichier créé à l'intérieur hérite automatiquement du groupe projet_linux.

Un membre du groupe peut modifier ses fichiers mais ne peut pas supprimer ceux des autres membres.

Les permissions de /etc/shadow sont vérifiées : seul root peut y accéder.