# Component Testing
*******************
**// WIP a retravaillé ne pas prendre tel quel WIP**

**// WIP cette fiche est un regroupement d'info uniquement WIP**
## Les differents types de tests
*******************
1. ###**Tests unitaires :**
   Les tests unitaires visent à tester une partie spécifique d'un composant en isolant cette partie des autres parties du système. Cela permet de vérifier si le code répond correctement aux entrées attendues et si les résultats obtenus sont conformes aux attentes. Les tests unitaires sont généralement écrits par les développeurs eux-mêmes, car ils ont une connaissance approfondie du code et de son fonctionnement. Ces tests sont souvent automatisés à l'aide de frameworks de test, tels que JUnit pour Java, NUnit pour .NET ou Pytest pour Python. Les tests unitaires doivent couvrir toutes les branches du code, y compris les cas limites et les scénarios d'erreur. Ils sont exécutés fréquemment pour détecter rapidement les erreurs et permettre aux développeurs de les corriger avant qu'elles ne se propagent à d'autres parties du système.
2. ###**Tests d'intégration :**
   Les tests d'intégration visent à tester comment le composant s'intègre avec d'autres parties du système. Cela peut inclure des tests de communication avec d'autres composants, des tests de flux de données entre les composants et des tests de compatibilité entre différents systèmes. Les tests d'intégration peuvent être manuels ou automatisés et sont généralement effectués après que les tests unitaires ont été exécutés. Les tests d'intégration sont importants car ils permettent de détecter des erreurs qui peuvent ne pas être visibles lors de tests unitaires isolés.
3. ###**Tests de régression :**
   Les tests de régression visent à vérifier que les modifications apportées au code n'ont pas affecté les fonctionnalités existantes du composant. Les tests de régression sont exécutés chaque fois que des modifications sont apportées au code pour s'assurer que les fonctionnalités existantes ne sont pas cassées. Ces tests sont souvent automatisés à l'aide de frameworks de test et peuvent être effectués à chaque compilation ou à chaque déploiement. Les tests de régression sont particulièrement importants pour les projets à long terme, où le code est souvent modifié et étendu au fil du temps.
4. ###**Tests de charge :**
   Les tests de charge visent à tester les performances du composant en situation de charge. Cela peut inclure des tests de charge de stress, où la charge est augmentée progressivement jusqu'à ce que le système atteigne sa limite, ou des tests de charge de montée en charge, où la charge est augmentée progressivement pour évaluer comment le système gère les demandes simultanées. Les tests de charge sont importants pour garantir que le composant peut gérer une charge élevée sans échouer ou causer des retards inacceptables. Les résultats des tests de charge peuvent être utilisés pour identifier les goulots d'étranglement du système et pour améliorer les performances du composant.
5. ###**Tests de sécurité :**
   Les tests de sécurité visent à identifier les vulnérabilités de sécurité potentielles du composant. Cela peut inclure des tests de pénétration, où un testeur évalue le système en essayant de le pirater, des tests de vulnérabilité, où le système est analysé pour identifier les vulnérabilités
## Les avantages de chaque outils de test front
*******************
### Jest :

Avantages :

- Configuration facile à mettre en place
- Syntaxe simple et intuitive
- Fournit des fonctionnalités de test automatisées
- Possibilité de test en continu

Inconvénients :

- Ne convient pas à toutes les applications, spécialement celles qui ne sont pas basées sur React, Vue ou Angular

### Cypress :

Avantages :

- Facile à configurer et à utiliser
- Interface utilisateur intuitive
- Possibilité de tester en continu
- Capacité à exécuter les tests dans un navigateur intégré

Inconvénients :

- Pas adapté à tous les types d'applications, spécialement celles qui ne sont pas basées sur React, Vue ou Angular

### Protractor :

Avantages :

- Conçu spécifiquement pour tester des applications Angular
- Capacité à gérer des opérations asynchrones
- Possibilité de tester en continu

Inconvénients :

- Peut ne pas être adapté à toutes les applications web, spécialement celles qui ne sont pas basées sur Angular

### Puppeteer :

Avantages :

- Offre une grande flexibilité dans l'automatisation de tâches liées au navigateur
- Possibilité de générer des captures d'écran pour une visualisation rapide des résultats de test
- Grande capacité à simuler des interactions utilisateur

Inconvénients :

- Peut être plus difficile à configurer que certains des autres outils de test

### Selenium :

Avantages :

- Disponible dans différents langages de programmation, ce qui le rend flexible et adaptable à une variété de besoins de test
- Peut être utilisé pour une grande variété d'applications web
- Permet de simuler des interactions utilisateur et de valider les résultats

Inconvénients :

- Peut être plus difficile à configurer et à utiliser que certains des autres outils de test

### Karma :

Avantages :

- Configuration facile à mettre en place
- Possibilité de tester en continu
- Surveille les modifications de code et réexécute les tests de manière continue

Inconvénients :

- Ne convient pas à tous les types d'applications, spécialement celles qui ne nécessitent pas de tests unitaires en continu.

## Comment mettre en place une stratégie de test
*******************
###**Analyse des exigences :** 
Cette étape consiste à comprendre les exigences du composant front-end et à déterminer les fonctionnalités qui doivent être testées. Il est important de se concentrer sur les fonctionnalités les plus importantes pour les utilisateurs, et de déterminer les scénarios de test qui couvrent ces fonctionnalités. Il est également important de déterminer les critères d'acceptation des tests pour chaque fonctionnalité, afin de savoir quand un test est considéré comme réussi.
###**Développement des tests :** 
À partir des scénarios de test identifiés à l'étape précédente, l'équipe de test peut élaborer des plans de test détaillés pour chaque fonctionnalité. Les plans de test doivent inclure des cas de test unitaires, des tests d'intégration et des tests fonctionnels. Pour chaque cas de test, il est important de spécifier les entrées et les sorties attendues, ainsi que les conditions préalables et postérieures pour s'assurer que le test est bien isolé et reproductible. Les tests peuvent être développés en utilisant un outil de test automatisé tel que Cypress, Selenium, Jest ou Mocha.
###**Exécution des tests :** 
Les tests automatisés peuvent être exécutés à chaque fois qu'il y a une nouvelle version du composant front-end, en utilisant une plate-forme de test automatisée ou une solution de CI/CD. Il est important de s'assurer que les tests sont exécutés dans un environnement de test isolé qui reflète autant que possible l'environnement de production. Les résultats des tests peuvent être enregistrés et analysés pour détecter les erreurs. Les tests peuvent être exécutés manuellement pour les tests exploratoires, mais l'objectif est d'automatiser autant de tests que possible.
###**Rapport des erreurs :** 
Les erreurs détectées lors de l'exécution des tests doivent être signalées à l'équipe de développement pour être corrigées. Il est important de fournir des informations détaillées sur les erreurs, telles que la description de l'erreur, le scénario de test qui a échoué, les entrées et les sorties qui ont causé l'erreur, etc. Cela aidera l'équipe de développement à reproduire et à corriger l'erreur plus rapidement.
###**Régression des tests :** 
Après avoir corrigé les erreurs, les tests doivent être exécutés à nouveau pour s'assurer que les corrections ont résolu les problèmes sans causer de nouveaux problèmes. Il est important de s'assurer que les corrections ont été testées dans le contexte de l'application globale et qu'elles n'ont pas affecté d'autres fonctionnalités du composant front-end.
###**Optimisation des tests :** 
L'équipe de test peut également rechercher des moyens d'optimiser les tests en améliorant les scripts de test, en réduisant le temps d'exécution des tests et en augmentant la couverture des tests. L'objectif est de trouver un équilibre entre la couverture des tests et le temps d'exécution des tests pour maximiser la qualité des tests tout en minimisant le temps et les ressources nécessaires pour les exécut

## Quelle est-la solution magique ?
*******************
Il n'y a pas de réponse universelle à cette question, car chaque solution a ses propres avantages et inconvénients, et leur pertinence dépend des besoins spécifiques du projet. Par exemple, si votre application est basée sur Angular, Protractor peut être la solution la plus adaptée pour les tests automatisés de votre front-end. Si vous recherchez une solution plus souple et plus générique pour les tests de front-end, Selenium pourrait être le meilleur choix.

En fin de compte, le choix de la meilleure solution pour les tests de front-end dépendra de facteurs tels que la complexité de l'application, les technologies impliquées, la taille de l'équipe de développement, les compétences techniques de l'équipe de test et les ressources disponibles. Il est recommandé de bien réfléchir à vos besoins de test, à vos contraintes et à vos capacités avant de choisir une solution de test de front-end.
