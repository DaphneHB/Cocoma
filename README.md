### Cocoma
##COordination et COncensus Multi-Agents (Coordination and Multi Agents consensus)

Projet de simulation multi-agents réalisé dans le cadre de l'enseignement COCOMA du Master ANDROIDE de l'Université Pierre et Marie Curie et encadré par Amal El Fallah Seghrouchni, Cédric Herpson et Aurélie Beynier, professeurs et chercheurs du LIP6.


Le projet consiste en une simulation 3D en NetLogo, simulation d'une mission de drones protégeant et escortant un convoi POKESAFE de leur base à un endroit donné transportant des marchandises essentielles : les POKERAR, et étant donné des ennemis hostiles actifs sur le terrain.


# Scénario
Été 2016, une nouvelle espèce apparaît sur la planète terre. Facile à capturer, les rangs de cette espèce sont rapidement décimés par les collectionneurs privés. Pour éviter la disparition de cette expèce atypique, l'ONU décide immédiatement de  créer une réserve hautement protégée : la POKESAFE, et y transporte et libère les représentants les plus rares.


Dans le cadre de l'opération FREEDOM4POKERAR, un convoi composé de K véhicules de transports banalisés, dont l'un transportant un espèce rare, doit relier la réserve des POKERAR au départ du centre de naissance INGRESS le 5 décembre 2016, 11h00 UTC.


En tant que responsable de cette mission, nous disposons d'une connaissance a priori du terrain et sommes donc en mesure de planifier le trajet de notre convoi. Néanmoins, la position d'éventuels éléments hostiles et désireux de s'en emparer, par nature changeante, ne nous est pas connue.


La région où se trouve la réserve n'étant pas encore stabilisée, et la cargaison de haute importance, le commandement a affecté le nouvel escadron de drones autonomes de l'armée de l'air à la protection du convoie. Ces drones armés sont en mesure d'évoluer dans un environnement inconnu et ouvert, de réaliser tant des missions de reconnaissance que de destruction, de se coordonner tant entre eux qu'avec les unités au sol via leurs leader respectifs, et de prendre leurs propres décision en fonction des informations perçues.


## Problématique
Notre objectif est de faire parvenir le véhicule transportant la cargaison à destination.

Dans ce but, nous avons du concevoir, modéliser et implémenter le système de communication et de décision dont est doté l'escadron de drones, en nous appuyant sur le paradigme agent. À partir du théâtre d'opération fourni, nous avons du réaliser une simulation du bon déroulement de cette mission.


Au cours de la simulation, nous supposerons les agents comme simulés, nous n'aurons donc aucun contrôle sur ces derniers.


Par soucis de réalisme, la simulation comportera plusieurs contraintes au niveau des agents et de l'environnement :
    * Les drones composant l'escadron peuvent partager leurs informations sans contrainte de communication.
    * Les drones ne peuvent échanger les informations dont ils disposent qu'avec les unités de même type à portée.
    * Les unités ennemies (terrestres) sont dotées de comportements hostiles.
    * Les différents véhicules du convoi sont dotés de comportements définis (calcul de chemin, évitement, dispersion).
    * Les drones et unités ennemies sont limités par des resources finies (carburant, munitions) et doivent se ravitailler.
    * Les drones peuvent agir selon divers comportement (exploration, protection, destruction, coordination).
    * Les drones et le convoi adaptent leurs stratégies et rôles selon les pertes et le terrain.
    * Centralisation de l'information chez les drones et mise à jour des connaissances.
    * Communication drones-convoi par l'intermédiaire des leaders.
    * Exploitation des données sur les changements de l'environnement.


La mise en oeuvre de ce projet a été réalisée sur la plate-forme de simulation NetLogo 3D. Nous avons aussi utilisé l'extension BDI de lias Sakellariou, Petros Kefalas, and Ioanna Stamatopolou. Enhancing netlogo to simulatebdi communicating agents. Artificial Intelligence : Theories, Models and Applications, pages263–275, 2008.


Le code source du projet présenté ci-dessous peut être téléchargée à cette adresse https://github.com/DaphneHB/Cocoma
