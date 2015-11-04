
#Avoir simplement des icônes élégantes pour ses applications avec Font Awesome

## Problématique

Pour un développeur, mettre en place les icônes dans une application Web ne présente pas de soucis technologique. En effet les pages Web permettent facilement la mise en place d'images. De plus certains sites (https://thenounproject.com/) permettent trouver des icônes variées plus ou moins libres de droits.

Toutefois, deux problèmes se posent :

- L'adaptation d'icônes existantes ou la création de nouvelles icônes dans le but d'avoir une charte graphique homogène nécessite souvent des compétences graphiques sortant du périmètre des savoirs du développeur.
- L'utilisation d'images de type png, gif… peut s'avèrer inadaptée dans la constition de l'IHM. En effet, par exemple, le fait qu'elles ne soient pas efficacement modifiable en taille ou couleur introduit une distance par rapport aux autres composants de la page stylables via CSS.

##La solution Font Awesome

[Font Awesome](http://fortawesome.github.io/Font-Awesome/) est une librairie Open Source proposant plusieurs centaines d'icônes sous forme d'une police de caractère liée à une feuille de style CSS.

Cela permet de résoudre les deux premiers problèmes susmentionnés :

- les icônes peuvent être stylées via du CSS de la même manière que du texte normal.
- les icônes sont vectorielles et donc le rendu est conservé avec la taille

De fait, la solution est compatible avec toutes les technologies Web (Java, PHP,…) et tous les navigateurs.

##Installation

Font awesome reposant sur du CSS la méthode la plus rapide est d'inclure un lien pérenne vers la feuille de style principale:

    <link rel="stylesheet" href="//maxcdn.bootstrapcdn.com/font-awesome/4.3.0/css/font-awesome.min.css">

Toutefois, la librairie peut également être téléchargée et mise en place au sein de votre application.

##Utilisation

La librairie s'utilise via un jeux de classe à ajouter sur la balise qui va devenir l'icône. Cette balise devrait logiquement être un `<span>` mais traditionnellement c'est une balise `<i>` qui est utilisée.

Les principaux points à retenir sont les suivants:

- La première classe à ajouter est fa qui indique que la police à utiliser est celle de Font Awesome.
- Ensuite, à chaque icone est associée une classe particulière. Ces classes peuvent être retrouvée sur la La feuille récapitulative. Exemple : fa-user est la classe correspondant à l'icone user.
- De plus, plusieurs classes vont permettre de modifier facilement la taille, l'orientation ou l'animation d'une image. Exemples :
Taille (fa-2x: taille double, fa-3x: taille triple…)
Rotation : fa-spin
- Enfin, les icônes sont stylables via les styles CSS classiques (color, …)
Exemple

Le code suivant permet d'avoir un icône de téléphone assez grosse, colorée en rouge et tournante.

    <i class="fa fa-phone fa-5x fa-spin" style="color:red" /> 

<span>
<i class="fa fa-phone fa-5x fa-spin" style="color:red" />
</span>