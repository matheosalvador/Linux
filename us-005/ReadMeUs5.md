# **Objectifs de la Story :**

>En tant qu'administrateur de ma Debian, 
je souhaite protéger ma VM en changeant les mots de passe par défaut 
afin d'éviter que d'autres personnes se connectent sur ma VM

# **Critères d'acceptation :**

>Changer le mot de passe (passwd) du compte bobby
>
>Changer le mot de passe du compte root
>
>Vérifier que les changements de mot de passe sont effectifs
# **Resultat:**

> ### **les commandes pour changer le user password :**
>- changer le password du compte : d abord avoir les droits administrateurs avec la commande sudo  ,sudo permet de emprunter temporairement les pouvoirs de l administrateur avec un compte utilisateur limité ,la commande a rentré est  : "sudo su "  ici on fait sudo pour eviter de taper le password de root que on a pas ,  puis:  "passwd username" ,le mot de passe : **ploufplouf**  puis "exit" et tester en se reconnectant ;
>
>**[Voir Exemple](<../us-001/pictures/Capture d'écran 2026-01-21 142309.png>)**
>
>- changer le password root  avec la commande "sudo passwd root"
le mot de passe : "**miao**";
>
>**[Voir Exemple](<../us-001/pictures/Capture d'écran 2026-01-21 142530.png>)**