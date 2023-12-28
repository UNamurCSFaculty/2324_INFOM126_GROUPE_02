# Contribution Guidelines and Best Practices

1. [Gestion du nom des branches](#gestion-du-nom-des-branches)
2. [Conventions relatives aux commits](#conventions-relatives-aux-commits)
3. [Gestion des issues](#gestion-des-issues)
4. [Conditions de merge sur main](#conditions-de-merge-sur-main)
5. [Scan Sonar](#scan-sonar)
6. [Release Plan](#release-plan)

# Gestion du nom des branches

Plusieurs politiques de nomenclature des branches sont envisageables,
elles sont un ensemble de _best pratices_ qu'un contributeur doit respecter au maximum.

## Utiliser des séparateurs et définir le type de la branche

Utilisez des séparateurs comme "-" ou "/" pour faciliter la lecture.
Utilisez également en premier lieu un des mots parmi la liste suivante :

![](https://github.com/UNamurCSFaculty/2324_INFOM126_GROUPE_02/blob/main/docs/contrib_img/word.png)

exemple :

    `test-login-new-user OR test/login/new/user`

## Utiliser une nomenclature incrémentale

Donnez à chaque nouvelle _issue_ rencontrée un id unique

exemple :

    `wip-202-invalid-post-blog`

## Inclure le nom de l'auteur de la branche

Il est vivement recommandé d'inclure votre nom/pseudonyme dans celui de la branche
en suivant le format "**auteur**-**catégorie**-**nom**"

exemple :

    `nohbruh-bugfix-private-blog-access-control`

## A ne pas faire

**N'ayez pas de noms de branche trop longs et évitez d'utiliser uniquement des chiffres.**

# Conventions relatives aux commits

Typiquement, les conventions des messages de commit se basent sur le template
suivant :

    <type>[optional scope]: <description>

    [optional body]

    [optional footer(s)]

Le contributeur est appelé à faire preuve d'un _best effort_ lors de ses commits.

Pour plus d'[informations complémentaires](https://www.conventionalcommits.org/en/v1.0.0/)

# Gestion des issues

## Sécurité

Avec notre analyse codeql de la codebase, il est possible que des vulnérabilités au sein de l'application soient
identifiées. Si vous pensez être capable de les résoudre, créez une nouvelle branche **pour CHAQUE issue** en respectant la nomenclature décrite
plus haut. Une fois résolue, ouvrez un nouveau ticket de _security advisory_ via le template fourni sur le repository
du projet sur github.

[https://github.com/UNamurCSFaculty/2324_INFOM126_GROUPE_02/issues](https://github.com/UNamurCSFaculty/2324_INFOM126_GROUPE_02/issues)

## Bug Report et proposition de Features

Si vous découvrez des bugs au sein de l'application, rapportez-les sur la page des [issues](https://github.com/UNamurCSFaculty/2324_INFOM126_GROUPE_02/issues)
du repository en suivant le template fourni. Pour ce qui est de la proposition de nouvelles features que vous aimeriez
voir dans l'application, la démarche reste la même : allez sur la page des issues et choississez le template relatif à votre
demande.

# Conditions de merge sur main

Le merge sur la branche main lors de vos pull_request ne sera possible que si le build d'intégration continue (via les actions GitHub)
est concluant, c'est à dire :

1. Le build `maven` et les tests unitaires sont passés
2. Les tests du module `Node.js` sont passés
3. les `Quality Gates` définies sur le SonarCloud du projet sont passés

En cas d'échec de l'un de ces workflows, le pull_request sera rejetée.

# Scan Sonar

Pour autant que vous fassiez partie de l'organisation et que vous ayiez les droits d'analyse sur le projet,
vous pouvez lancer localement un scan sonar avec la commande suivante (n'oubliez pas de faire un `mvn clean verify` au préalable):

    mvn sonar:sonar \
    -Dsonar.projectKey=UNamurCSFaculty_2324_INFOM126_GROUPE_02 \
    -Dsonar.organization=unamurcsfaculty \
    -Dsonar.host.url=https://sonarcloud.io \
    -Dsonar.login=<YOUR_TOKEN>

avec `Your_TOKEN` étant votre token généré via la page Sécurité de votre profil servant
à vous authentifier

# Release Plan

Idéalement, nous souhaitons tenir un rythme d'1 release mineure toutes les 3 ou 4 semaines et 1 majeure par an.
En ce qui concerne les mineures, dans l'éventualité où il serait impossible que des issues soient résolues pour la release,
cette dernière peut-être postponée ou les features reportées à la release suivante. Dans tous les cas, à l'approche de la release,
faites de votre mieux pour finir ce que vous aviez commencé [**de corriger/implémenter**].
