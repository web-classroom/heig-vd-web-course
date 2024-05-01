# Question

L'équipe de développement que vous avez récemment rejointe a décidé de mettre en
place une stratégie de tests pour leur application web. Pour l'instant, aucun
test n'est implémenté et vous avez été désigné pour mettre en place cette
stratégie. Pour l'instant, l'interface du côté client est assez simple. C'est la
logique de l'application qui est plus complexe. L'équipe a peu de moyens et vous
devez donc trouver une solution qui soit à la fois efficace et peu coûteuse.

Entre des tests unitaires et des tests d'intégration, que choisiriez-vous de
mettre en place en premier et pourquoi ? Et en quoi consistent-t-ils ?

Aucun code n'est nécessaire pour cette question.

# Réponses

### Quoi choisir?!

Les tests les plus importants à mettre en place en premier sont les **tests
unitaires**. On ne peut pas faire de tests d'intégration si on est même pas sûr
du fonctionnement de base de nos fonctions...

Il est plus important d'être en premier sûr que chaque fonction passent les
tests avant de faire des tests d'intégrations plus couteux.

En plus vu qu'ils sont bien plus simple à mettre en place, ils reviennent à
moins cher pour notre entreprise.

### En quoi consistent-t-ils ?

#### Test unitaire

- On test chaque fonctions ou module indépendamment du système au sens large.
- On vérifie si ces fonctions font bien ce qu'elle sont censé faire.
- Rapide à mettre en place vu qu'on vérifie le fonctionnement d'une seule
  entité, le comportement est prévisible.
- Exemple -> Vérifier qu'un email est valide (merci regex)

#### Test d'intégration

- On test des composants de notre application, on met ensemble différentes
  fonctions et on vérifie qu'elles fonctionnent bien ensemble
- Lent à mettre en place car vu qu'il y a plusieurs éléments qui intéragissent
  ensemble, les résultats sont moins prévisible.
- Exemple -> Vérifier si l'email est déjà dans une database et indiquer à
  l'utilisateur si son email est existant ou pas

#### En général, pour tester notre programme on va écrire :

- Beaucoup de tests unitaires
- Quelques tests d'intégrations
- Et plus rarement des tests systèmes

---

Les tests unitaires vérifient qu'une partie du programme fonctionne
correctement, indépendemment du plus grand système dont elle fait partie. Par
exemple, on va tester juste une fonction ou un modèle pour vérifier qu'il
fonctionne comme attendu, sans prendre en compte le fait qu'il fasse partie d'un
plus grand système. Ce type de test est rapide à mettre en place, facile à
exécuter et donc peu coûteux.

Les tests d'intégration prennent les unités qui ont déjà passé les tests
unitaires et les regroupent afin de créer un composant. Le test d'intégration va
ensuite vérifier que les composants qui sont faits de plusieurs unités du
programme interagissent correctement. A ce stade, les différentes parties d'un
composant sont considérées comme correctes et fonctionnant comme attendu. Ce
type de test peut être parfois lent à implémenter et exécuter.

En se basant sur les définitions des tests unitaires et des tests d'intégration
ci-dessus, je choisirais de mettre en place les tests unitaires en premier. En
effet, nous avons vu que les tests d'intégration partent du principe que les
unit tests on été faits et ont passé donc ça n'aurait pas de sens de commencer
pas ceux-ci. On ne peut pas partir du principe que les unités du programme
fonctionnent sans les tester. (Si ce n'est pas testé, il faut partir du principe
que ça ne fonctionne pas.) De plus, il est dit que l'équipe de développement a
peu de moyens et les tests unitaires sont peu coûteux à mettre en place, ce qui
semble convenir à la situation.

Ceci dit, il serait bien de mettre aussi en place les tests d'intégration dans
un second temps (et si les moyens le permettent à ce moment-là), afin d'assurer
que les composants fonctionnent et interagissent comme attendu, en particulier
puisqu'il est précsié que l'application est complexe.

---

Les tests unitaires sont généralement des petits tests **faciles à écrire** qui
**vérifient le comportement d'une fonction ou méthode** pour vérifier que ses
valeurs de retour sont correctes en fonction de ses arguments. Le but est de
tester une petite partie de la logique (des calculs, des branchements
compliqués, des validations de donnée) afin de vérifier qu'il fonctionne quand
cela doit marcher mais qu'ils détectent également les erreurs. Ces tests
unitaires testent généralement des fonctions qui sont isolés et n'accède pas à
des ressources externes (la DB, le réseau, le disque, au DOM, au localStorage,
...) ils sont donc **très rapides** à exécuter (moins d'1s pour des centaines de
tests).  
_Exemple: tester qu'une fonction `isPhoneNumberValid()` utilisant une regex,
valide correctement un numéro de téléphone._

Les tests d'intégration quant à eux, permettent de **tester que plusieurs
composants fonctionnent correctement ensemble**. Ils sont un peu plus difficiles
à écrire et prennent plus de temps à développer car ils nécessitent de simuler
des ressources/un environnement autour (avec du mocking ou des stub). Ils
permettent de voir si les composants inclus sont bien intégrés ensemble. En
partie à des ressources externes, il prennent également plus de temps
d'exécution (pour remplir la DB de données de tests par ex.).  
_Exemple: tester que notre composant VueJS `RegisterForm.vue` (qui contient un
champ email, prénom, nom, numéro de téléphone) est capable d'afficher une erreur
si le téléphone est mal écrit (et donc de voir s'il utilise correctement
`isPhoneNumberValid()`)._  
_Autre exemple: tester que le controlleur de notre app MVC backend permet bel et
bien de se créer un compte, en vérifiant que les inputs sont validés, de
sauvegarder des données dans la DB, de répondre le bon code de statut et les
données de l'utilisateur créé en retour._

Pour revenir à notre équipe, je conseillerai pour gagner du temps de **faire des
tests unitaires** en premier, ce qui va permettre de s'assurer que la logique
coeur est bien solide, il faudra l'extraire dans des fonctions isolées
réutilisées par le reste de la logique et des composants graphiques. Ensuite si
l'équipe a le temps et que certaines parties de l'interface ou des mises
ensemble de fonctions deviennent complexes, d'écrire des tests d'intégration...
