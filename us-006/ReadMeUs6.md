# **Objectifs de la Story :**

>En tant qu'administrateur de ma Debian,
je souhaite renommer (hostnamectl) ma VM
afin de l'identifier aisément

# **Critères d'acceptation :**

>Le nom de ma VM dans VirtualBox n'est plus le nom par défaut.
>
>Le nom de ma Debian (hostname) n'est plus le nom par défaut.

# **Resultat :**

>- changer le nom de la vm : click droit sur la vm -> configuration ->  vm name : linux-debian
>
>**![Voir Exemple](<../us-001/pictures/Capture d'écran 2026-01-21 142837.png>)**
>
> - changer le nom du hostname:
la commande pour changer le hostname : " sudo hostnamectl set-hostname nouveau_hostname "
le nouveau nom du host est : **navi**
>
>**![Voir Exemple](<../us-001/pictures/Capture d'écran 2026-01-21 142702.png>)**
>
>Premièrement : " sudo nano /etc/hosts "
>
>Deuxièment : Trouve la ligne : " 127.0.1.1    debian12 "
>
>**![Voir Exemple](<../us-001/pictures/Capture d'écran 2026-01-22 142022.png>)**
>
>Troisièmement : Remplace-la par : " 127.0.1.1    navi "
>
>Quatrièment  : Faire **"ctrl+x"** puis **"O"** puis **"Enter"**
>
>Pour Finir : " sudo reboot "