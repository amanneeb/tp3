# Grille d'évaluation pour le TP3
## Structure, sémantique, accessibilité, API des formulaires HTML5
- [X] __Regrouper les éléments de formulaire de même nature__ (1 point)  
  - Utiliser des `<fieldsets>`  
  - Faire des groupes d’`<option>`s dans une liste déroulante
- [X] __Étiqueter__ (1 point)  
  - Étiqueter les groupes d’éléments de formulaire   
  - Nommer chaque groupe avec une `<legend>`  
  - Étiqueter un groupe d’`<option>`s d’une liste déroulante  
  - Étiqueter avec un `<label>` les champs de formulaire  
- [X] __Tester l'accessibilité__ (.85/1 point)  
  - Rendre (garder) le formulaire navigable au clavier  
  - Baliser avec précision les éléments de formulaire  
  - Bien choisir le type du `<input>`   
  - Code sémantique et valide pour l’ensemble du document  
- [X] __Ajouter des contraintes de saisie__ (.85/1 point)  
  - Identifier par un attribut approprié les champs obligatoires du formulaire  
  - Ajouter des contraintes de saisie sur les champs de formulaire  

## Styles CSS
- [X] __Aligner les éléments de formulaire__ (.85/1 point)
    - Contrôler les espacements 
- [X] __Intégrer tous les contenus__  (.9/1 point)  
  - Selon les guides visuels (ou mieux !)
- [X] __Styler l’interactivité__  (.75/1 point)
  - État focus, état checked des éléments de formulaires  
  - États des hyperliens (link, visited, hover, active)  
  - Styler les messages d’erreur
  - Utiliser des sprites CSS  
- [X] __Styler les boutons radio__  (.75/1 point) 
  - en les gardant accessibles au clavier

## Méthodes de travail favorisant la collaboration
- [X] __Organiser et documenter la feuille de styles__  (0.85/1 point)
- [X] __Utiliser le contrôle des versions GIT__  (1 point)
    - Un minimum de 3 commits est attendu pour les étapes html, css, contrôle qualité finale



## Commentaires
<span style='color:red'> 8.8/10 </span>

- Très bon travail d'intégration.

### HTML
- Il y a seulement quelques [erreurs html](images/erreurs-html.png)
  - Les requêtes media dans les balises `<source>` doivent être placées entre `()` parenthèses.
  ```html
  <source srcset="./images/bandeau_600.jpg" media="(max-width: 600px)">
  <source srcset="./images/bandeau_1200.jpg" media="(min-width: 600px)">
  ```
- Attention au choix des balises
  - `<time>` plutôt que `<date>`
  - `<strong>` plutôt que `<b>`
- C'est plus prudent de ne pas utiliser de caractères accentués pour les valeurs de `name` ou de `id`
  
### Accessibilité
- Définir la langue principale du document en ajoutant un attribut `lang="fr"` sur la balise racine `<html>` 

### Fonctionnalités
- Les boutons radio n'ont pas un comportement mutuellement exclusif parce que la valeur de leur attribut `name` n'est pas la même.
Voir correction dans le code du commit d'évaluation.

### CSS
Pour que les étiquettes des boutons radio soient plus faciles à styler, changer leur `display` est très utile.  
À noter que le sélecteur de frère adjacent permet de cibler précisément les balises `<label>` consécutives à un bouton `radio`
```css
input[type="radio"]+label{
   display: block;
   padding: 1px;
   border: 1px solid transparent;
}
```

## Barème
| Barème | sur 1 |
|--------|-------|
| A+     | 1     |
| A      | 0.95  |
| B+     | 0.9   |
| B      | 0.85  |
| C+     | 0.8   |
| C      | 0.75  |
| D      | 0.65  |
