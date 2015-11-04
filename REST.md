# Une application REST

Initialement les applications WEB étaient juste des arborescences de fichiers situées sous une racine.

  Par exemple :
  - http://www.bacqueferronnerie.fr/Escaliers_P1_2.htm  --> Le fichier *Escaliers_P1_2.htm* existe physiquement et le serveur web ne fait que le transmettre au navigateur
  -  http://www.bacqueferronnerie.fr/slimbox-1.58/Images_escaliers/elicoidal_GF_small.jpg --> le fichier *elicoidal_GF_small.jpg*  existe physiquement dans le répertoire *slimbox-1.58/Images_escaliers/*
La preuve : http://www.bacqueferronnerie.fr/slimbox-1.58/Images_escaliers/

 **Il y a donc correspondance physique entre les URL et les ressources dans ce genre d'application**

 **Les applications REST étendent la notion d'URL à des ressources non physiquement présentes** 
 
<p align="center">
<img src="https://raw.githubusercontent.com/francoisandre/gdp/master/images/rest.png" />
</p>

Autre Exemple : 
 https://stackedit.io/viewer#!url=https://raw.githubusercontent.com/francoisandre/gdp/master/gdp.md
 (Notez la double URL)