# **Objectifs de la Story :**

>En tant qu'administrateur système, 
je veux automatiser la création d'une arborescence de projet standardisée (dossiers projets/, docs/ et /clones) en une seul script.

# **Critères d'acceptation :**

>Tous les scripts commencent par la shebang
>
>Le script d'installation utilise une commande de test pour vérifier la présence du logiciel avant de l'installer.
>
>Le script d'installation gère l'élévation de privilèges ou avertit l'utilisateur qu'il doit être sudo.
>
>Le script de création peut être lancé plusieurs fois sans générer d'erreurs si les dossiers existent déjà.
>
>Les dossiers projets/, docs/ et clones/ sont créés avec les permissions appropriées.
>
>Le script crée l'arborescence dans le répertoire personnel ($HOME) de l'utilisateur qui l'exécute.
>
>Au moins deux alias pointant vers les scripts des US précédentes.
>
>Les modifications sont inscrites dans le fichier ~/.bashrc et restent actives après une déconnexion/reconnexion.
>
>L'invite de commande affiche l'heure actuelle.