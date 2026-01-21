# **Objectifs de la Story :**

>En tant que gestionnaire de données, 
je veux créer un script Bash pour compresser (tar) le dossier /etc et le copier dans /data.

# **Critères d'acceptation :**

>Aucune action n'est effectuée directement avec root (sudo).
>
>Le nouveau disque ou partition est formaté (ext4).
>
>Le point de montage /data existe et le disque y est rattaché.
>
>Le disque se monte automatiquement après un redémarrage de la machine.
>
>Afficher l'espace disponible sur /data.
>
>Les archives compressées (format .tar.gz) ont un nom incluant un horodatage.
>
>Les archives sont créées régulièrement.
>
>Après redémarrage, les archives continuent d'être créées régulièrement.
>
>La restauration d'un fichier peut être effectué depuis l'une des archives.
>
>Les archives appartiennent à root et ne sont pas modifiables par des utilisateurs standards.
>
>Il est possible de démarrer une sauvegarde manuellement en cas d'urgence (procédure à fournir).
>
>L'équipe projet peut montrer les logs du cron de sauvegarde.