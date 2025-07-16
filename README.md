# Protocole TCP/IP

Mis en place pour permettre la communication entre tous les ordinateurs, peu importe leur fabriquant.

Organise/ordonne la communication: 
- quand elle commence
- qui transmet quand
- est-ce que l'info a bien été transmise
- quand elle finit.

#### IP (Internet Protocol): 
identifie les adresses des ordinateurs impliqués.

#### TCP (Transmission Control Protocol):
transmet les informations d'une adresse à l'autre.


Les informations sont transmises en **paquets** afin de ne pas devoir tout renvoyer en cas de problème. Ils sont réassemblés une fois arrivés. Chaque paquet peut prendre un chemin différent, pour faciliter la circulation.

Les informations sont également transmises en **4 couches**, afin de respecter des standards facilitant la communication (telle information dans telle couche) et la mise à jour (uniquement les couches concernées au lieu de l'ensemble).

### Couche de liaison de données / d'interface réseau / d'accès réseau / physique 
Gère la partie physique de la transmission (envoi et réception) par le matériel (câble ethernet, carte d'interface réseau, pilote du périphérique, ...).

### Couche internet / couche réseau
Contrôle le mouvement des paquets sur le réseau.

### Couche transport
Fournit une connnexion fiable, divise en paquets, accuse réception, et vérifie les accusés de réception de l'autre appareil.

### Couche application
Ce que l'utilisateur voit.

Comme les paquets ne sont pas chiffrés, ils sont accessibles à qui sait y faire, d'autant plus sur un wifi public. Un VPN les chiffre.

## Les types d'adresses IP
Il existe 2 types:
- statique: reste toujours la même.
- dynamique: est modifiée de temps en temps et sert un peu de tampon: pour imager, on connaît l'adresse de l'hôtel mais pas le numéro de chambre.

Et 2 versions:
- IPv4 (version 4): ancienne version, quand on avait besoin de moins d'adresses IP et qu'elles étaient donc moins longues.
- IPv6 (version 6): nouvelle version, rallongée car besoin de plus d'adresses IP.

### IPv4
Les adresses IPv4 sont constituées de 32 bits, généralement représentées en format décimal par quatre nombres séparés par des points, chaque nombre représentant un octet (8 bits). Par exemple, 192.168.1.1 est représenté ainsi:
![protocol-ip-1 BKw1RFXH_Z1syQy](https://github.com/user-attachments/assets/6ee37ff5-2ae9-4070-b551-26e1a4bbe0e4)
