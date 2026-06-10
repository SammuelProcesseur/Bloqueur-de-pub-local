# Bloqueur de pub avec un RaspberryPi

Matériel:
Un Raspberry Pi
Une alimentation de Raspberry Pi
Une micro SD
Un flasheur pour micro SD

1:

Lancer votre Raspberry Pi avec une OS sans interface graphique (exemple : Raspberry Pi OS Lite) à l'aide de votre flasheur et de l'imager : https://www.raspberrypi.com/software/

2:

tapez : sudo nmtui faite entrer puis sélectionner edit

3:

dans IPv4 configuration, choisissez : manual. Cliquez sur show à gauche et entrez une adresse IP statique dans Addresses. Cette IP doit être en dehors de votre routeur DNS maison (exemple:192.168.1.201). Puis dans Gateway sélectionnez l'adresse de Broadcast (exemple:192.168.1.254) et enfin dans DNS servers, remettez l'adresse sélectionnée dans Addresses.

(vous pouvez voir les adresses IP en dehors de votre DNS maison en tapant ces adresses IP dans un onglet Google
Livebox (Orange) → passerelle = 192.168.1.1
Freebox → passerelle = 192.168.1.254 ✓
SFR → passerelle = 192.168.1.1 ou 192.168.0.1
Bbox (Bouygues) → passerelle = 192.168.1.254)

4:

faites OK en bas de page, puis sélectionnez Back puis Quit

5:

faite un : sudo reboot

6:

entrée la commande suivante : sudo curl -sSL https://install.pi-hole.net | bash

7:

attendez la fin de l'installation, puis faites OK deux fois, puis continuez.

8: 

choisissez votre DNS (Google si vous ne savez pas lequel choisir).

9: 

sélectionnez YES.

10:

sélectionnez votre mode de confidentialité.
(Hide domains and clients, si vous ne savez pas quoi choisir)

11: 

vous pouvez voir votre login Password, retenez-le bien.

12: 

dans une nouvelle fenêtre, tapez : https://addresse Ip du Pi/admin/login et rentrez votre mot de passe de l'étape précédente.

13:

Allez dans Settings, DHCP, et cochez DHCP server enabled.

14:

Dans Range of IP addresses to hand out, sélectionnez plage d'adresse IP que vous avez vue dans votre routeur (exemple dans Start: 192.168.1.1, dans End: 192.168.1.200 et dans Router: 192.168.1.254).

15:

Et enfin, dans la page web opérateur, décocher le DHCP.
(exemple:
Livebox (Orange) → passerelle = 192.168.1.1
Freebox → passerelle = 192.168.1.254 ✓
SFR → passerelle = 192.168.1.1 ou 192.168.0.1
Bbox (Bouygues) → passerelle = 192.168.1.254)
