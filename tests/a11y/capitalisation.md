
# Accessibilité & Tests

Se focus uniquement sur les outils qui tournent en CI et ces manières de tester?

Nombreuses extensions navigateurs ou applications SaaS qui analysent des pages via une URL

## Les tests spécifiques aux critères d'accessibilités 

### Les tests sans assertions spécifique 

Test un ensemble de critères qui doivent être systématiquement être validés. Comme par exemple : 
- présence d'une alternative textuelle sur une image
- respect de la hierarchie des headings (de h1 à h6 sans "saut de niveau")
- contraste de luminance des couleurs suffisant entre le texte et le fond 

Peut se faire au niveau d'une page entière, ou au niveau d'un composant

Pas d'assertions particulières à écrire, on lance un test type "checkA11y()" sur notre composant / notre page et l'erreur remontée doit nous apprendre ce qui ne va pas.

#### Sous quelles formes ça existe? 

- Vérification de la sémantique HTML
- Unitaire - axe?
- Intégration à des outils de tests d'applications existants - Cypress + extension, Browserstack + extension 
- Extensions navigateurs : WAVE, etc...

### Les assertions spécifique pour tester l'accessibilité dans nos applications 

Par exemple, je construis une bibliothèque de composants réutilisables, je veux m'assurer que les composants répondent 
Dans le cas d'un composant "Accordéon" = entête qui permet de "déplier" un contenu. Je vais tester les valeurs d'un attribut `aria-expanded` des click / de la visibilité de mes éléments. 

## Les bonnes pratiques de tests pour ne pas oublier l'accessibilité dans nos autres tests

Ex : getByRole dans testing library 

En vrac, message posté sur MM
```
Pour les assertions, j'essaierai au maximum de passer par un truc type getByRole : 
https://testing-library.com/docs/queries/byrole/

Ça te permet un juste équilibre entre validation d'un HTML correct (nécessaire  pour des questions d'accessibilité) et expressivité du test pour ne pas être fragile / couplé à l'implem
Tu peux trouver la liste des roles ici : https://www.w3.org/TR/html-aria/#docconformance


Par exemple, tu veux tester un bouton, avec le getByRole=button tu vas pouvoir cibler à la fois les éléments natifs HTML button mais aussi des éléments auquel on aurait rajouté un role=button manuellement
(plus rare mais ça arrive, et ça peut rester accessible même sans utiliser l'élément natif)

Et l'avantage, c'est que tu ne cibleras pas les trucs du genre <div onClick={...}> Je suis un faux bouton pas accessible </div> 

Malheureusement tous les utilisateurs n'ont pas de souris pour faire un "click" sur le texte "Soumettre le formulaire"

Pour quelqu'un qui navigue au clavier, je dois m'assurer que l'élément est focusable / actionnable (et ça peut se vérifier si avec un getByRole :smile: )
```



## Name dropping des technos / ressources (à trier) 

https://docs.google.com/presentation/d/1kKwmHREBJ7E3LzR28lMcaZnMKwMOqkbW3m_D2AXHIzA/edit#slide=id.gf91f2b3736_0_0

https://www.w3.org/WAI/ER/tools/

https://docs.google.com/spreadsheets/d/1qeiWQIGx1HDuH-7vgbpCMnaOvgz5yirqeAmW4J8Np2E/edit#gid=0

https://drive.google.com/drive/folders/1BBdNGqTAqO4FR2J6kAhfkemuXCixSfBP

### A tester / mettre en avant : 

- axe avec implémentation sur un test Jest (via jest-axe?)

TODO : Vérifier si contrast de couleurs peuvent être vérifier dans un JSDOM? ([à priori non?](https://www.npmjs.com/package/jest-axe?activeTab=explore) cf désactivation ) 
Sinon souligner importance de le tester à un endroit donné ? 
