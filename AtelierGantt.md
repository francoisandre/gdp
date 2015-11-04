# Atelier Gantt

## Objectif 
L'objectif de cet atelier est d'établir et manipuler un diagramme de Gantt.

Plusieurs outils existent pour ce faire. Le plus utilisé étant *MS-Project*. De nombreuses variantes existent (en ligne, open-source,...) comme par exemple OpenWorkbench ou OpenProj

Nous utiliserons le produit **GanttProject** (http://www.ganttproject.biz/).

Le logiciel peut se télécharger (http://www.ganttproject.biz/download) sous plusieurs formes. 
En cas de doute, la version .zip ne nécessite pas d'installation.

## Quelques notions

Ressource
: Personne affectée sur le projet

Tâche
: Élément de base de la planification qui correspond à la plus fine décomposition de travail.
Une tâche est décrite par :  
- Une charge (estimée en jours)
- Des liens avec des tâches précédentes. Ce lien peut être de plusieurs types 
	- Fin à début (la plupart des cas)
	- Début à début
	- Fin à Fin
	- Début à Fin (rares)
- Une date de début et une date de fin (résultat des tâches précédentes ou de contraintes extérieures
- Un état d'avancement
- Une ou plusieurs ressources associées
- Un ensemble de tâches peuvent être regroupées sous forme de *tâche récapitulative* ou de *lot*.

Jalon
: Tâche de charge nulle représentant une étape du projet (remise de livrable, début ou fin d'une période contractuelle)
 
Chemin critique
: Ensemble des tâches pour lesquelles toute modification de durée entraîne une modification sur la date de livraison finale du projet.
 
 Le chemin critique permet donc d'identifier les tâches sur lesquelles pèsent un risque sur les délais.

## Principe de Gantt
La décomposition de l'intégralité en tâche et l'affectation des ressources correspondantes permet de déduire de manière déterministe la date de fin du projet.

## Exercice

### Ennoncé

Définition des tâches

tâches | nature  | durée en jours | prédécesseurs
---|---|---|---
A |acceptation des plans par le propriétaire | 4|
B | préparation du terrain |2|
C |commande des matériaux |1| A
D |creusage des fondations |4 |B
E |commande des portes et fenêtres| 2| A
F |livraison des matériaux |2| C
G |coulage des fondations| 2 |D, F
H |livraison des portes et fenêtres |10| E
I |pose des murs, de la charpente et du toit| 4 |G
J| mise en place des portes et fenêtres |1 |H, I 

Source : http://www.univ-paris13.fr/eufms/images/stories/Documents/exercicesgdp.pdf

###Questions

- Etablir le diagramme de Gantt

<p align="center" >
<img src="https://raw.githubusercontent.com/francoisandre/gdp/master/images/ganttEx1.png"   />
</p> 
- Identifier le chemin critique
- Si deux personnes sont affectées au projet, quel problème identifiez vous ? Comment le résoudre ?

Solution : https://raw.githubusercontent.com/francoisandre/gdp/master/images/exerciceGantt.gan 