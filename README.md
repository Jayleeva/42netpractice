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
Il existe 2 types de durée:
- statique: reste toujours la même.
- dynamique: est modifiée de temps en temps et sert un peu de tampon: pour imager, on connaît l'adresse de l'hôtel mais pas le numéro de chambre.

Et 2 types d'accès:
- privée: utilisée au sein de réseaux locaux, n'est pas routable sur Internet. Pour la version 4, des plages spécifiques sont réservées pour les adresses privées, comme 192.168.x.x, 10.x.x.x et 172.16.x.x à 172.31.x.x.
- publique: permet de se connecter à internt. Chaque IP publique est uniques à travers le monde. 

Et 2 versions:
- IPv4 (version 4): ancienne version, quand on avait besoin de moins d'adresses IP et qu'elles étaient donc moins longues.
- IPv6 (version 6): nouvelle version, rallongée car besoin de plus d'adresses IP.

### IPv4
Les adresses IPv4 sont constituées de 32 bits, généralement représentées en format décimal par quatre nombres séparés par des points, chaque nombre représentant un octet (8 bits). Par exemple, 192.168.1.1 est représenté ainsi:
![protocol-ip-1 BKw1RFXH_Z1syQy](https://github.com/user-attachments/assets/6ee37ff5-2ae9-4070-b551-26e1a4bbe0e4)

La subdivision d’un réseau en sous-réseaux permet une utilisation plus efficace des adresses IP et améliore la sécurité et la performance du réseau. Les masques de réseau en IPv4 sont utilisés pour déterminer quelle partie d’une adresse IP représente le réseau et quelle partie représente l’hôte au sein de ce réseau. Voici comment ils fonctionnent :
![protocol-ip-2 DyNLspFm_ZzmCRd](https://github.com/user-attachments/assets/fdd55f2e-c7da-4d30-b8ec-ae64fb1418e1)

Ce graphe utilise une représentation binaire pour montrer comment un masque de sous-réseau est appliqué à une adresse IP :
- L’adresse IP Exemple est 192.168.1.10, représentée en binaire comme 11000000.10101000.00000001.00001010.
- Le Masque de Sous-Réseau utilisé est 255.255.255.0, représenté en binaire comme 11111111.11111111.11111111.00000000.
- La Partie Réseau obtenue est 192.168.1, représentée en binaire comme 11000000.10101000.00000001.
- La Partie Hôte est 0.0.0.10, représentée en binaire comme 00000000.
- Le Résultat affiche l’adresse du réseau dans la notation CIDR, ici 192.168.1.0/24, où /24 indique que les 24 premiers bits sont utilisés pour l’adresse réseau.

#### Détermination du Réseau et de l’Hôte :
Lorsqu’un masque de réseau est appliqué (opération logique ET) à une adresse IP, les bits du masque à 1 indiquent la partie réseau de l’adresse, tandis que les bits à 0 indiquent la partie hôte.

Par exemple, avec l’adresse IP 192.168.1.10 et le masque 255.255.255.0, l’adresse de réseau est 192.168.1.0 et l’adresse de l’hôte est 0.0.0.10.

#### Notation CIDR (Classless Inter-Domain Routing) :

Avant, on utilisait une notion de classe d'adresse, qui a été remplacée par CIDR, la notion de classes d’adresse a été remplacée par un système plus flexible. CIDR utilise une notation en barre oblique (/) suivie du nombre de bits à 1 dans le masque. Par exemple, /24 pour 255.255.255.0.



### IPv6
Contrairement aux adresses IPv4 qui sont composées de 32 bits (par exemple, 192.168.1.1), les adresses IPv6 sont composées de 128 bits. 

Les adresses IPv6 sont représentées en notation hexadécimale, avec huit groupes de quatre chiffres hexadécimaux séparés par des deux-points. Par exemple : 2001:0db8:85a3:0000:0000:8a2e:0370:7334.


