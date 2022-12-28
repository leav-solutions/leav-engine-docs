---
description: >-
  Cette documentation a pour objectif de vous aider a comprendre d'une part
  LEAV-Engine, ces avantages et bénéfices mais aussi de repenser la conception
  de base de données
---

# Welcome to LEAV-Engine



## The little story of LEAV Engine

Les principaux concepts de LEAV Engine ont été initié en 2001

Depuis plus de 30 ans, Didier Mombrun a créé plusieurs entreprises dans la communication mais toujours en lien avec les technologies.

{% hint style="warning" %}
Didier Mombrun est co-fondateur de LEAV-Solutions et co-concepteur de LEAV-Engine et Data Studio
{% endhint %}

Dans les années 90, Didier est dirigant d'une société de communication et de prepress qui réalise pour ses clients industriels et retailers des catalogues papier ainsi que leurs versions CDROM (Encore très populaire à l'époque) et les premiers sites web. C'est dans ce cadre qu'il s'intéresse à la possibilité de centraliser les données des produits dans une base de données pour alimenter avec les même informations l'ensemble des supports.

Ce n'est qu'en 2001, suite à la vente de son entreprise, qu'il décide d'investir dans le développement d'une solution de gestion des informations produits (PIM). Didier ne connait pas de langage de programmation pour développer lui même une application full web, il utilise divers outils pour créer l'architecture et créer les premières maquettes de la solution avec FileMaker mais également MySQL / PHPMyAdmin.&#x20;

Pour réaliser les développements, il fait appel à des développeurs indépendants et finance pendant plusieurs années avec ces propres économies ce projet ambitieux.

Les premières livraisons des développements concernent les interfaces de gestion des produits et de gestion des images (Asset). Ces deux interfaces ont des fonctions communes pour lister, filtrer et éditer les enregistrements. C'est une demande de modification sur l'interface de gestion produit qui n'est pas effective sur l'interface des images qui sera révélatrice...

En effet, le développeur indique que bien que les fonctions sont communes et le code similaire, c'est une copie du code pour chaque interface car les requêtes bien que identiques n'interrogent pas les même tables. Le développeur ajoute qu'il faudra non seulement un délais mais aussi un coût supplémentaire.

Dépendant des délais et coûts de développements mais aussi la frustation de ne pas être autonome pour créer sans code le data-modèle (Tables et champs) et les relations ont été la motivation principale pour concevoir un modèle de données permettant avec un code et des requêtes communes de visualiser au travers d'une même interface n'importe qu'elle table de la base de données.

* Un seul code à maintenir pour toutes les fonctions communes et nécessaires à toutes les bibliothèques (Tables), Attributs (Champs) et relations
* Possibilité de créer dynamiquement des bibliothèques, des attributs et qu'ils soient immédiatement reconnu et utilisable dans la solution.

C'est ainsi que la solution PIM est née elle est actuellement le socle technique de la solution [OmniPublish by ARiSTiD](http://www.aristid.com) depuis plus de dix ans.

LEAV-Engine est puissante et moderne data plateforme 100% OPEN SOURCE et une forte expérience avec pour objectif de servir un plus large domaine d'applications

{% hint style="success" %}
LEAV est l'acronyme de Library, Entity, Attribut, Value

En effet, l'une des fonctions les plus avancé du modèle LEAV-Engine est la possibilité de gérer des attributs spécifiques une infinité de versions de valeurs
{% endhint %}



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
