# **Objectifs de la Story :**

En tant qu'administrateur de ma Debian, 
je souhaite renommer (hostnamectl) ma VM 
afin de l'identifier aisément

# **Critères d'acceptation :**

Le nom de ma VM dans VirtualBox n'est plus le nom par défaut.

Le nom de ma Debian (hostname) n'est plus le nom par défaut.
 
# **Resultat :**

>- changer le nom de la vm : click droit sur la vm >configuration >  vm name : linux-debian


> - changer le nom du hostname:
la commande pour changer le hostname : < sudo hostnamectl set-hostname nouveau_hostname >
le nouveau nom du host est : navi