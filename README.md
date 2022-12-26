---
description: >-
  Cette documentation a pour objectif de vous aider a comprendre d'une part
  LEAV-Engine, ces avantages et bénéfices mais aussi de repenser la conception
  de base de données
---

# Welcome to LEAV-Engine



## The little story of LEAV Engine

Les principaux concepts de LEAV Engine ont été initié en 2001

Depuis 1987 date à laquelle il termine ses études en communication, Didier Mombrun a créer plusieurs entreprises, toujours dans la communication mais toujours en lien avec les technologies.

{% hint style="warning" %}
Didier Mombrun est le fondateur de LEAV-Solutions et concepteur de LEAV-Engine et Data Studio
{% endhint %}

En 1995, il est dirigant d'une société de prepress et produit de nombreux catalogues papier ainsi que leurs versions CDROM (Encore très populaire à l'époque) et les premiers sites web. C'est dans ce cadre qu'il s'interesse à la possibilité de centraliser et stocker les données des produits dans une base de données pour alimenter avec les même informations validées l'ensemble des ces support.

Ce n'est qu'en 2001, suite à la vente de son entreprise, qu'il décide d'investir dans le développement d'une solution de gestion des informations produits (PIM). Cette solution sera baptisé Knowbox. Alors qu'il ne connait pas de langage de programmation, Didier utilise divers outils pour créer l'architecture et les premières maquettes de sa solution, FileMaker mais également MySQL avec des outils graphique tels que PHPMyAdmin ont beaucoup contribuer à sa réflexion et très vite a concevoir des interfaces beaucoup plus conviviales.

La révélation fut directement lié d'une part au manque de réactivité et au coûts impliqué par les développements sous traités à des développeurs. Alors que les premières interfaces de knowbox était en cours de recette, la première interface concernait la bibliothèque (Table des produits), celle-ci permettait de lister, filtrer, afficher et d'éditer chaque enregistrement. La deuxième interface était celle des Images (Visuels produits) et Documents (Notices, PDF...) avec les même fonctions de recherches, filtres et éditions.

Lors de la recette, Didier constate des dysfonctionnement et demande au développeur de modifier un comportement sur la recherche et les filtres de la bibliothèque des produits. Lorsque la correction est effectué, il vérifie le bon fonctionnement, mais constate que le même problème n'est pas résolu sur la même fonction mais sur la bibliothèque des Images. En interrogant le développeur, celui-ci lui indique que ce n'est pas le même code et qu'il faudra non seulement attendre que la correction soit effectuée mais de payer le temps de travail associé.

C'est a ce moment là que la nécessité de maitriser les coûts a été l'étape qui a fait basculer Knowbox dans une dimension différente et de ne coder qu'une seule fois toutes les fonctions communes et nécessaires à toutes les bibliothèque de la solution.

Le premier problème était qu'a chaque besoin d'une nouvelle caractéristique et bien que le champs pouvait être créer directement en base, le développeur devait le connaitre dans son code et donc le déclarer.



## Quick links

{% content-ref url="getting-started/introduction.md" %}
[introduction.md](getting-started/introduction.md)
{% endcontent-ref %}

{% content-ref url="getting-started/data-model-concepts.md" %}
[data-model-concepts.md](getting-started/data-model-concepts.md)
{% endcontent-ref %}

## Get Started

We've put together some helpful guides for you to get setup with our product quickly and easily.

{% content-ref url="getting-started/premiers-parametrages/" %}
[premiers-parametrages](getting-started/premiers-parametrages/)
{% endcontent-ref %}

{% content-ref url="getting-started/premiers-parametrages/setting-permissions.md" %}
[setting-permissions.md](getting-started/premiers-parametrages/setting-permissions.md)
{% endcontent-ref %}

{% content-ref url="getting-started/premiers-parametrages/inviting-members.md" %}
[inviting-members.md](getting-started/premiers-parametrages/inviting-members.md)
{% endcontent-ref %}
