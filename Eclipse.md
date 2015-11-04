# Quelques notions d'Eclipse

## Préambule

![enter image description here](http://www.touilleur-express.fr/wp-content/uploads/2012/01/erich_gamma-150x150.jpg)

Qui est Erich Gamma ?

## Eclipse et les autres IDE
Eclipse est un IDE - Integrated Development Environment - c'est à dire un outil permettant d'effectuer l'intégralité des tâches de développement (édition, compilation, génération, ...)

Il fait partie des 3 grands IDE gratuits avec Netbeans (<i class="icon-flash"></i>) et IntelliJ

**Il est souvent critiqué pour sa lourdeur.**

La dernière version en date nommée *Mars* est sortie en mars 2015 et correspond au numéro 4.5. 

## Extensibilité

### Les plugins
Eclipse est à la base dédié au travail autour de Java. Toutefois, il peut être étendu en rajoutant des modules complémentaires, *plugin*.

Par exemple on va trouver :
 - Des modules pour **coder dans un autre langage** (PHP, Python, ...)
 - Des modules pour **se connecter à des sources de données** (exploration de bases de données)
 - Des modules pour lire des formats de fichiers de manière plus efficace (XML, maquetteur graphiques...)
 - Des modules pour **se brancher à d'autres outils** (MantisBT, Mylin, Maven, Sonar...)
 - ...

#### Installer de nouveaux plugins

Les plugins peuvent s'installer de plusieurs manières.

La plus simple - car plus automatique - consiste à utiliser le dépôt de plugin fourni par Eclipse dans *Help > Eclipse MarketPlace...* et d'indiquer le nom du module que l'on cherche :

<p align="center">
<img src="https://raw.githubusercontent.com/francoisandre/gdp/master/images/eclipseMarketPlace.png" />
</p>

*Remarque*
Les autres plugins - non référencés sur le *market place* - peut s'installer via *Help > Install new software...* 

#### Deux petits plugins utiles 
 - Note Pad
 - StartExplorer

### La plate forme RCP

Il est également possible d'utiliser le socle d'Eclipse pour construire des clients lourds en bénéficiant d'une base fiable et robuste. C'est la plateforme Eclipse RCP. Les développements s'effectuent dans ce cas en Java.

Exemple : GanttProject, Rational Rose, ...

## Terminologie 

### Espace de travail (Workspace)
Un espace  de travail est un regroupement de projets. On peut se créer autant d'espaces de travail que nécessaire ou basculer de l'un à l'autre (*File > Switch workspace*).

On ne peut pas avoir plusieurs instances d'Eclipse ouvertes simultanément sur le même espace de travail.

*Remarque*
Si des modifications de fichiers sont effectuées de manière externe à Eclipse, il va être nécessaire d'effectuer un rafraîchissement afin qu'Eclipse les prenne en compte.

### Perspective
Une perspective est un regroupement de vue et d'éditeurs correspondant à une activité de développement (ex: Java, Debug,...).

On peut basculer de l'une à l'autre via la barre de perspective:
<p align="center" >
<img src="https://raw.githubusercontent.com/francoisandre/gdp/master/images/perspectives.png"   />
</p> 

### Vue
Une vue est un composant graphique, représenté sur la forme d'un onglet, et proposant la visualisation thématique d'une information (Ex: l'arborescence des fichiers, la console, ...).

<p align="center" >
<img src="https://raw.githubusercontent.com/francoisandre/gdp/master/images/vues.png"   />
</p> 

*Remarque*
On peut déplacer les vues au sein d'une perspective ou ajouter à une perspective des vue initialement absente.

### Éditeur
Occupant la partie centrale d'Eclipse, les éditeurs permettent l'édition des fichiers. Ils sont souvent dotés de fonctionnalités riches :  coloration syntaxique, identification des erreurs lors de la frappe, rendu graphique, ...

<p align="center" >
<img src="https://raw.githubusercontent.com/francoisandre/gdp/master/images/editors.png"   />
</p> 

## Utilisation du clavier

### Raccourcis
Raccourci     | Rôle
-------- | ---
`Ctrl`+`D` | Suppression ligne
`Alt` + <i class="icon-up"/><i class="icon-down"/>    | Déplacement de ligne
`Ctrl` + `1` | Quick fix / Proposition de modèles
`Ctrl`+`Espace` | Complétion automatique / Proposition de modèle
`Ctrl` + `Shift` + `T` | Ouverture d'une classe Java
`Ctrl` + `Shift` + `R` | Ouverture d'un fichier
`Ctrl` + `Shift` + `L` | Fiche de rappel des raccourcis
`Alt` + `Shift` + `R` | Activation refactoring

*Exemple* : création automatique des Getters/Setters

### CamelCase
En Java le nom des types et des variables font souvent alterner majuscule et minuscules. Ex : *StringBuffer*, *maVariableBienNommee*

Le *CameCase* consiste à utiliser cette alternance afin de ne pas avoir à taper toutes les lettres, notamment lors de la complétion automatique. 

*Exemple :* 
`BRA` suivi de `Ctrl`+`Espace` va proposer toutes les classes dont le nom contient la structure B*R*A* ou les * sont des minuscules (à l'exception de la dernière qui correspond soit à des minuscules soit à des majuscules). La liste va également proposer les constantes commençant par *BRA*.
<p align="center" >
<img src="https://raw.githubusercontent.com/francoisandre/gdp/master/images/camelCase.png"   />
</p> 

*Remarques*

- Pour préciser la liste, on peut indiquer certaines minuscules. Ainsi BiRA correspond aux chaines Bi*R*A*.
- Le camelCase est utilisable pour les variables, dans les fenêtres de dialogue munies de la complétion automatique 

<p align="center" >
<img src="https://raw.githubusercontent.com/francoisandre/gdp/master/images/contentAssist.png"   />
</p> 

## Gestion des préférences

Les préférences se gèrent via la fenêtre *Window > Preferences*


- Activation du formatage lors de la sauvegarde
- Mise en place automatique du *;* 
