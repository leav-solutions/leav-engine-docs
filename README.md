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

En 1995, il est dirigant d'une société de prepress et réalise pour ces clients industriels et retailer de nombreux catalogues papier ainsi que leurs versions CDROM (Encore très populaire à l'époque) et les premiers sites web. C'est dans ce cadre qu'il s'interesse à la possibilité de centraliser et stocker les données des produits dans une base de données pour alimenter avec les même informations validées l'ensemble des ces support.

Ce n'est qu'en 2001, suite à la vente de son entreprise, qu'il décide d'investir dans le développement d'une solution de gestion des informations produits (PIM). Cette solution sera baptisé Knowbox. Alors que Didier ne connait pas de langage de programmation, il utilise divers outils pour créer l'architecture et les premières maquettes de sa solution. FileMaker mais également MySQL avec des outils graphique tels que PHPMyAdmin ont beaucoup contribuer à sa réflexion et très vite a concevoir des interfaces beaucoup plus conviviales.

La révélation fut directement lié d'une part au manque de réactivité et au coûts impliqués par les développements sous traités à des développeurs pour obtenir une application FullWeb. Knowbox était entièrement financé par ces propres économies. Didier est alors impatient de pouvoir tester les premières interfaces de knowbox. Ce n'est que quelque mois plus tard qu'il reçoit la première version et de tester la première bibliothèque (Table des produits), celle-ci permettait de lister, filtrer, afficher et d'éditer chaque enregistrement. La deuxième interface était celle des Images (Visuels produits) et Documents (Notices, PDF...) avec les même fonctions de recherches, filtres et éditions.

Lors de la recette, Didier constate des dysfonctionnement et demande au développeur de modifier un comportement sur la recherche et les filtres de la bibliothèque des produits. Lorsque la correction est effectué, quelques semaines plus tard... il réceptionne et vérifie le bon fonctionnement, mais constate que le même problème n'est pas résolu sur la même fonction de la bibliothèque des Images. Il interroge le développeur et celui-ci lui indique que ce n'est pas le même code et qu'il faudra non seulement attendre que la nouvelle correction mais le coût supplémentaire associé.

La nécessité d'être autonome mais aussi de maitriser les coûts de développements ont fait basculer Knowbox dans une dimension différente avec deux objectifs : coder une seule fois toutes les fonctions communes et nécessaires à toutes les bibliothèque de la solution et pouvoir créer le data modèle depuis une interface graphique conviviale.

Pour cela il fallait concevoir une deuxième version de Knowbox avec un moteur adapté à ces contraintes; pouvoir créer dynamiquement des attributs, Bibliothèques et faire en sorte que celles-ci soient dynamiquement et automatiquement pris en compte par un code commun. La question posée au développeur a été ainsi formulé : Est il possible que dans une requête SQL, le nom des tables et des champs soient des variables ? La réponse a été OUI !

Knowbox Engine est né est actuellement le socle technique de la solution OmniPublish



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
