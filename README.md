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

{% hint style="info" %}
Didier Mombrun travail depuis plusieurs années avec Jérome et Teddy (développeurs de talent) qui sont maintenant ses associés et co-concepteurs de LEAV-Engine.
{% endhint %}

Dans les années 90, Didier est dirigant d'une société de communication et de prepress qui réalise pour ses clients industriels et retailers des catalogues papier ainsi que leurs versions CDROM (Encore très populaire à l'époque) et les premiers sites web. C'est dans ce cadre qu'il s'intéresse à la possibilité de centraliser les données des produits dans une base de données pour alimenter avec les même informations l'ensemble des supports.

En 2001, suite à la vente de son entreprise, il décide d'investir dans le développement d'une solution de gestion des informations produits (PIM). Didier ne connait pas de langage de programmation pour développer lui même une application full web, il utilise divers outils pour créer l'architecture et les premières maquettes du PIM avec Claris FileMaker mais également MySQL / PHPMyAdmin et bien entendu Excel.&#x20;

Pour réaliser les développements, il fait appel à des développeurs indépendants et finance pendant plusieurs années avec ces propres économies ce projet ambitieux.

Les premières versions livrées concernent les interfaces de gestion des produits et de gestion des images (Asset). Ces deux interfaces ont des fonctions communes pour lister, filtrer et éditer les enregistrements pourtant et bien que identique le code est dupliqué pour chaque interface car les requêtes n'interrogent pas les même tables.&#x20;

Cette solution n'est pas satisfaisante car coûteuse en développement et maintenance sachant que d'autres interfaces sont nécessaires, tel que les projets, les pages, les articles, les fournisseurs etc... Toutes ont un point commun qui est de créer, modifier, supprimer mais aussi rechercher, filtrer, exporter, importer et gérer des permissions.

Trop dépendant des délais et coûts de développements mais aussi frustré de ne pas être autonome pour créer le data-modèle, les tables, les champs, les relations via une interface web conviviale, Didier décide de revoir la conception en se consacrant plus sur le socle technique que sur les interfaces et fonctions métiers. Il a la conviction qu'il est possible de concevoir et unifier un code, des requêtes et des interfaces pour afficher n'importe quelles tables, ses entités, ses valeurs et ses relations.

Après quelques semaines de travail et prototypes, le modèle très simple de la solution est défini puis le code et les interfaces développées en quelques mois. Une interface d'administration permet de créer graphiquement par clic, drag& drop des bibliothèques (Tables), des attributs (Champs), des relations et de paramétrer l'affichage et les permissions., la solution était enfin disponible.

Le concept est donc de gérer avec un seul code commun pour les fonctions et les interfaces, l'ensemble du data modèles indifféremment des tables, des champs et des relations.

* CRUD (Create, Read, Update, Delete)
* Recherche, filtres...
* Import, Export
* Rôles et permissions
* Une API Rest
* Et bien d'autres...

C'est ainsi que la solution PIM est née, elle est actuellement le socle technique de la solution [OmniPublish by ARiSTiD](https://www.aristid.com/cacom-produits-omnipublish/) plateforme leader de communication omnicanale pour piloter la promotion, la production et la diffusion des offres commerciales des principales enseignes de la grande distribution Française.

Après 15 ans et cette fabuleuse expérience nous avons décider de lancer LEAV-Engine, une puissante et moderne data plateforme 100% OPEN SOURCE avec pour objectif de servir un plus large domaine d'applications et démocratiser la gestion des données

{% hint style="info" %}
LEAV est l'acronyme de Library, Entity, Attribut, Value

En effet, l'une des spécificité du modèle LEAV-Engine est de proposer une fonction avancé permettant une infinité de versions de valeurs ou de relation s’appuyant sur le modèle EAV auquel nous avons ajouté la dimension relationnelle "**L**ibrary".
{% endhint %}



## Quick links

{% content-ref url="getting-started/introduction.md" %}
[introduction.md](getting-started/introduction.md)
{% endcontent-ref %}

{% content-ref url="getting-started/data-model-and-concepts.md" %}
[data-model-and-concepts.md](getting-started/data-model-and-concepts.md)
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
