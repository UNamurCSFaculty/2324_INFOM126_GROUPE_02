# Contribution Guidelines and Best Practices

1. [Gestion du nom des branches](#gestion-du-nom-des-branches)
2. [Conventions relatives aux commits](#conventions-relatives-aux-commits)
3. [placeholder](#)
4. [placeholder](#)
5. [placeholder](#)

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

# Release Plan

Idéalement, nous souhaitons tenir un rythme d'1 release mineure toutes les 3 ou 4 semaines et 1 majeure par an.
En ce qui concerne les mineures, dans l'éventualité où il serait impossible que des issues soient résolues pour la release,
cette dernière peut-être postponée ou les features reportées à la release suivante.
