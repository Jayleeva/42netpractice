# Protocole TCP/IP

Mis en place pour permettre la communication entre tous les ordinateurs, peu importe leur fabriquant.

Organise/ordonne la communication: 
- quand elle commence
- qui transmet quand
- est-ce que l'info a bien été transmise
- quand elle finit.

#### IP: 
identifie les adresses des ordinateurs impliqués.

#### TCP:
transmet les informations d'une adresse à l'autre.


Les informations sont transmises en **paquets** afin de ne pas devoir tout renvoyer en cas de problème. Ils sont réassemblés une fois arrivés. Chaque paquet peut prendre un chemin différent, pour faciliter la circulation.

Les informations sont également transmises en **4 couches**, afin de respecter des standards facilitant la communication (telle information dans telle couche) et la mise à jour (uniquement les couches concernées au lieu de l'ensemble).
