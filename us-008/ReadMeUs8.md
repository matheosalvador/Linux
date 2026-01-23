# **Objectifs de la Story :**

>En tant qu'utilisateur, 
je veux créer et organiser des répertoires et fichiers, 
afin de structurer mes données efficacement.

# **Critères d'acceptation :**

>Créer un répertoire simple et une arborescence complexe en une seule commande.
>
>Créer un fichier vide de plusieurs manières avec touch ou avec une redirection.
>
>Organiser ses données en déplaçant ou en renommant des fichiers et dossiers sans perte de données.
>
>Copier un fichier vers un autre répertoire.
>
>Copier récursivement pour dupliquer des dossiers entiers.
>
>Supprimer des fichiers, des dossiers vides et des dossiers pleins.
>
>Lire le contenu d'un fichier texte sans l'ouvrir, ceci de plusieurs manières.
>
>Visualiser une arborescence de dossiers (tree).
>
>Ne pas utiliser les espaces et les caractères spéciaux/accentués dans les noms de fichiers et de dossiers.
>
>Utiliser les guillemets ou l'échappement \ si un nom de fichier contient malgré tout un espace.

# **Résultat :**

>la commande pour créer un répertoire simple et une arborescence complexe est mkdir -p DossierNiveau1/Niveau2/Niveau3/Niveau4.a
>on met du texte à la ligne avec la commande suivante : "echo -n" puis on crée un fichier vide avec "echo -n > file_name"
>Puis on lit le code du fichier avec la commande suivante : "cat file_name"
>Puis on verifie les droits d'écriture et de lecture avec la commande suivante : " ls -l
>
>**[Voir exemple sur la console](../us-001/pictures/Capture_decran_2026-01-21_120150.png)**
>
>On affiche toutes les informations de son pc avec la commande suivante : "ps aux " et on peut les mettre dans un fichier avec "ps aux > file_name"
>"ps aux | grep bobby" permet d'afficher uniquement les informations contenant bobby, si on rajoute un "| tail -n 2" on affiche uniquement les 2 >dernières lignes, si on le remplace par "| head -n 3" on affiche uniquement les 3 premières lignes et si on remplace par "| head -n 5 | tail -n >1" on affiche uniquement la 5ème ligne.
>
>**[Voir exemple sur la console ](../us-001/pictures/Capture_decran_2026-01-21_115831.png)**