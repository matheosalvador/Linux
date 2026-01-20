# **Objectifs de la Story :**

En tant qu’utilisateur, 
je veux comprendre les différences entre les processus en avant-plan et en arrière-plan, afin de mieux les gérer avec des commandes comme bg et fg.

# **Critères d'acceptation :**

Interrompre et tuer définitivement un processus en avant-plan.

Mettre un processus en pause (suspendre) et reprendre la main sur le terminal.

Basculer un processus suspendu vers l'arrière-plan pour qu'il continue son exécution sans bloquer le terminal.

Ramener un processus d'arrière-plan vers l'avant-plan pour interagir à nouveau avec lui.

Lancer une commande directement en arrière-plan.

Lister tous les travaux en cours dans la session actuelle.

Faire la différence entre un PID (identifiant système global) et un Job ID.

Expliquer ce qui arrive à un processus en arrière-plan si on ferme le terminal … et savoir utiliser nohup.