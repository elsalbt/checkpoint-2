CHECKPOINT 2


Fichier réponses


Exercice 1 :
a.	Théorie


Q.1.1 Réponse à la question


Client : config IP static, pas sur le même réseau/serveur, en cas de routeur pas de broadcast
Serveur : éteint, pool plein, dhcp inactif

 
Q.1.2 Réponse à la question
Pas sur le même réseau


Q.1.3 Réponse à la question

Réutilisation d’un addrese dhcp si le bail n’est pas terminé sur la première addresse
La première addresse est déjà prise par une autre machine
Régle d’exclusion sur la première addresse
Le client à une addresse réservé su la plage DHCP qui n’est pas cette addresse


Q.1.4 Réponse à la question

serveur : configurer la réservation / client : IP configuration dynamique  ipconfig /release   et   ipconfig /renew


Q.1.5 Réponse à la question

fe 80 ::/10 adresse liens local, communication avec les machines sur le même réseau, passage routeur impossible

Q.1.6 Réponse à la question

Unicast local unique fc00 ::/7 ou /8 Adresse privé / routable en interne (ex  : VPN)
Global unicast 2001 ::/16 va sur internet
Bouclage ::1/128 elle corespond à la machine elle même
Multicast ff00 ::/ est une forme de diffusion d'un émetteur

Q.1.7 Réponse à la question
Oui c’est possible.

Q.1.8 Réponse à la question
DNS Domain Name System
Protocol Windows => Net Bios
- MDNS Protocol décentralisé
- LLMNR = MDNS mais dévelopé par Microsft permet la résolution de nom sur un liens local, en utilisant des requetes multicasts
  
Q.1.9 Réponse à la question
- Convention IPv6 à la priorité
- ping -4 <IP>

Q.1.10 Réponse à la question

- Fichier host => c:\windows\system32\etc\hosts on met l’IP du client 192.168.100.20 CLIENT1 CLIENT_TEST
- Renseigner le DNS dans le client  et Il faut créer un enregistrement A => CNAME Alias
  
b.	Mise en pratique

Q.1.11
Copie d’écran d’un ping depuis le serveur vers le client en IPv4.

![image](https://github.com/user-attachments/assets/03d19087-25e0-430c-b4bf-4765dda91700)


Copie d’écran du résultat de la commande ipconfig/all sur le client.

![image](https://github.com/user-attachments/assets/b4a47847-a72b-4f93-b05a-15d94d94cc97)



Copie d’écran d’un ping depuis le serveur vers le client en IPv4 (après modification).

![image](https://github.com/user-attachments/assets/03c28f4b-81ac-463d-85ae-27b1cddc490c)



Q.1.12
Copie d’écran du résultat de la commande ipconfig/all sur le client.

![image](https://github.com/user-attachments/assets/066984b1-3556-44b8-a583-55ae3be77a54)


Copie d’écran d’un ping depuis le serveur vers le client en IPv4.

![image](https://github.com/user-attachments/assets/ae4f89bf-8fab-4604-a822-d6a508cca6e6)


Q.1.13
Copie d’écran de la configuration DHCP sur le serveur.

![image](https://github.com/user-attachments/assets/c65fdaa0-d347-418c-9627-bd988557f57d)


Copie d’écran du résultat de la commande ipconfig/all sur le client.

![image](https://github.com/user-attachments/assets/1f56ee3b-8258-4e62-83d1-c59f09e36b3e)


Q.1.14
Copie d’écran de la configuration modifiée sur le serveur.




Copie d’écran du résultat de la commande ipconfig/all sur le client.

![image](https://github.com/user-attachments/assets/3c007f6b-a46d-40a1-bd4e-cae13a4d397a)













Q.1.15
Copie d’écran d’un ping depuis le serveur vers le client en IPv6.
Copie(s) d'écran













Q.1.16
Copie d’écran de la configuration DHCPv6 sur le serveur.
Copie(s) d'écran


Q.1.17
Copie d’écran d’un ping depuis le client vers le serveur avec le nom du serveur (IP de sortie en v4).
Copie(s) d'écran







Q.1.18
Copie d’écran de la modification de la configuration sur le serveur.
Copie(s) d'écran
Le ping est déjà fonctionnel :







Copie d’écran d’un ping depuis le serveur vers la machine CLIENT_TEST avec le nom CLIENT_TEST.
Copie(s) d'écran
Création Host A

Création d’ALIAS




















Ajouter le Suffix DNS Ethernet => IPv4 properties => Advanced










DNS ajouter le sufix du domain

















Exercice 2 :
b.	Théorie
Q.2.1
Copie d’écran de la configuration pour le partage de dossier.
Copie(s) d'écran
1) Créer le partage sur le dossier script à la racine sur le serveur => Advanced sharing….











2) File and Storage Services => Disks => clic droit New Share… => SMB Share Quick
3) Définir le chemin du partage du dossier à la racine


4) Spécifier le nom du partage












5) autoriser User1 ( l’utilisateur créer sur ADDS et sur lequel Client1 est maintenant connecté)











6) vérifier avec PS





7) Configurer le partage chez le clients
New-PSDrive -Name "Z" -PSProvider FileSystem -Root "\\SRVWIN01\Docs" -Persist
Et c’est un BINGO










Q.2.2
Copie d’écran de la modification du code pour que AddLocalUsers.ps1 s’exécute correctement.Copie(s) d'écran

Q.2.3
Copie d’écran de la modification du code pour que le 1er utilisateur soit crée.
Copie(s) d'écran

Copie d’écran montrant que le 1er utilisateur est créer.
Copie(s) d'écran


Q.2.4
Copie d’écran de la modification du code pour importation correcte du fichier CSV.
Copie(s) d'écran




Copie d’écran montrant que le champ « Description » est bien importé.
Copie(s) d'écran
Q.2.5
Copie d’écran de la modification du code pour bonne utilisation des champs du fichier CSV.
Copie(s) d'écran
Q.2.6
Copie d’écran de la modification du code pour avoir l’affichage d’un message lorsque l’utilisateur est crée.
Copie(s) d'écran



Q.2.7
Copie d’écran de la modification du code pour l’intégration de la fonction « Log ».
Copie(s) d'écran

Q.2.8
Copie d’écran N°1 d’un exemple de journalisation du code en utilisant la fonction « Log ».
Copie(s) d'écran


Copie d’écran N°2 d’un exemple de journalisation du code en utilisant la fonction « Log ».
Copie(s) d'écran
Q.2.9
Copie d’écran de la modification du code pour avoir l’affichage d’un message lorsque l’utilisateur existe déjà.
Copie(s) d'écran


Q.2.10
Copie d’écran de la modification du code pour que l’ajout des utilisateurs au groupe local fonctionne correctement.
Copie(s) d'écran


Q.2.11
Copie d’écran de la modification du code pour que le mot de passe des utilisateurs n’expirent plus.
Copie(s) d'écran








