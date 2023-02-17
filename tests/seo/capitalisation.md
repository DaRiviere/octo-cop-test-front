# SEO & Tests

## Pratiques et outils pour optimiser SEO dès le développement

À date : pas de framework ni de librairie de tests SEO identifiés [à vérifier], en revanche plusieurs outils d'audit disponibles.

## MàJ et compléments infos de la RefCard

- WooRank : outil freemium d'audit SEO, fournit un score + un bilan détaillé.
  - Avantages :
    - plugin multibrowser ;
    - interface user-friendly ;
    - info hiérarchisée et filtrable (par statut, impact et effort) ;
    - bilan très complet (+65 critères accessibles gratuitement) ;
    - explications claires quant aux modifications à apporter pour optimiser son score ;
    - rapidité de l'audit : immédiat si déjà réalisé avec date + alerte si possibilité d'obsolescence / sinon 15-20 sec.

  - Limites :
    - n'est pas utilisable en local (boucle de feedback longue) ;
    - payant pour un bilan complet (mais critères payants peu orientés dev) ;


- SEOQuake : outil gratuit d'audit SEO, fournit plusieurs bilans thématiques.
  - Avantages :
    - plugin multibrowser ;
    - paramétrable ;
    - extrêmement complet ;
    - peut être lancé en local (boucle de feedback rapide) ;
    - explications claires quant aux modifications à apporter pour optimiser son score 
    - redirige vers les ressources de référence sur chaque critère ;
  - Limites :
    - prise en main et interface peu intuitives (beaucoup d'infos et de possibilités, pas de filtres) ;


- Google tools for webmasters :
    - Nom à màj : Google Search Console (https://search.google.com/search-console/welcome) ;
    - Outil à tester pour plus d'infos.

## À ajouter

- Chrome Lighthouse : fournit un score + un (petit) audit SEO.
  - Avantages :
    - built-in Chrome ; 
    - concis, reprend les critères principaux ;
    - peut être lancé en local (boucle de feedback rapide) ;
  - Limites :
    - seulement 15 points de check.

# Todo
- Vérifier l'existence de frameworks/libs de tests SEO ;
- Tester Google Search Console : nécessite une vérification de la propriété du domaine => besoin d'un projet de test ;
- Ajouter infos LighthouseCI ?
- Faire le tri dans les outils (built-in / plugins / sites web...)
- Ajouter des ressources (guides bonnes pratiques SEO, structure de données - schema.org etc) ?
