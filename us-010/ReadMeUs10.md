# **Objectifs de la Story :**

>En tant qu'équipe, 
nous voulons montrer comment démarrer, arrêter, redémarrer et connaître l'état d'un service (par exemple sshd) avec systemctl, 
afin de comprendre la gestion des services sous
Linux.

# **Critères d'acceptation :**

>Vérifier l'état d'un service et interpréter les couleurs/statuts.
>
>Arrêter et démarrer un service manuellement.
>
>Expliquer la différence entre restart et reload.
>
>Expliquer la distinction entre un service actif et un service activé.
>
>Rendre un service permanent.
>
>Empêcher le démarrage automatique d'un service.
>
>Vérifier si un service démarrera de manière automatique ou non.

# **Resultat:**

>systemctl status <service> : donne les informations d'un service
>![Voir Exemple](../us-001/pictures/Capture_decran_2026-01-23_110036.png)
>sudo systemctl stop <service> : arrête un service
>![alt text](../us-001/pictures/Capture_decran_2026-01-23_110200.png)
>sudo systemctl start <service> : démarre un service
>![alt text](../us-001/pictures/Capture_decran_2026-01-23_110348.png)
>systemctl reload <service> : relis la configuration logicielle et la recharge, pas d'interruption de service
>systemctl restart <service> : arrête le service et le redémarre.
>service actif : en cours d'exécution.
>service activé : service chargé mais pas nécessairement en cours d'exécution.
>sudo systemctl enable <service> : permet de rendre un service permanent.
>sudo systemctl disable application.service : empêche le démarrage automatique d'un service
>![Voir Exemple](../us-001/pictures/Capture_decran_2026-01-23_111717.png)
>systemctl is-enabled application.service : vérifie si un service démarre de manière automatique ou non