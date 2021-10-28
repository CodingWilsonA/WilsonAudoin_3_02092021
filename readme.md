# Projet Ohmyfood!

## Index
* Description
* Project tree
* How to

### Description
 Ohmyfood! est une jeune startup qui voudrait s'imposer sur le marché de la restauration. L'objectif est de développer un site 100% mobile qui répertorie les menus de restaurants gastronomiques. En plus des systèmes classiques de réservation, les clients pourront composer le menu de leur repas pour que les plats soient prêts à leur arrivée.

 ### Project tree

```
|   delice-sens.html
|   index.html
|   menu-francaise.html
|   note-enchantee.html
|   package-lock.json
|   package.json
|   palette-gout.html
|   readme.md
|
+---img
|       delice-sens.jpg
|       la-francaise.jpg
|       note-enchantee.jpg
|       palette-gout.jpg
|
+---public
|   \---css
|       |   style.css
|       |   style.css.map
|       |
|       \---prefixed
|               style.css
|
+---Sass
|   |   styles.scss
|   |
|   +---Base
|   |       _global.scss
|   |
|   +---Components
|   |       _buttons.scss
|   |       _home-spinner.scss
|   |
|   +---Layout
|   |       _footer.scss
|   |       _headers.scss
|   |
|   +---Pages
|   |       _home-container.scss
|   |       _home-guide.scss
|   |       _home-intro.scss
|   |       _home-location.scss
|   |       _home-places.scss
|   |       _menu-figure.scss
|   |       _menu-rest-container.scss
|   |
|   \---Utils
|           _mixins.scss
|           _variables.scss
|
\---zoning
        Accueil.png
        Menu - À la française.png
        Menu - La note enchantée.png
        Menu - La palette du goût.png
        Menu - Le délice des sens.png
        menu-delice.png
        Menu-francaise.png
```
### How to
Reprend le Project tree pour détailler certains points importants.


* Sass

Les partiels sont importés vers styles.scss qui est compilé vers public/style.css puis préfixé dans public/prefixed/style.css

    * Pages
    Le code scss des pages est découpé selon les blocs html principaux du body de chaque page.

    * Pages/_home-places.scss
    Pour afficher la liste de restaurants, j'ai utilisé une boucle while qui créé des modificateurs d'éléments via la syntaxe d'interpolation. Dans cette boucle, j'ai ajouté une structure conditionnelle qui génère deux mixins tant que la variable comparée est strictement inférieure à 3 : la mixin d'affichage du fichier jpg et celle de l'étiquette "Nouveau". À partir de 3 et au-delà, elle génère seulement la mixin pour l'affichage du fichier jpg.

    * Pages/_menu-rest-container.scss
    L'affichage des plats est généré par une boucle while. Celle-ci génère aussi une animation dont le départ et retardé d'avantage à chaque itération d'un élément modifié via la syntaxe d'interpolation.

* zoning
Deux zonings du projet. Ce sont des prototypes de la structure html et BEM. Seulement deux exemples car les 4 pages des menus sont identiques en termes d'affichage.