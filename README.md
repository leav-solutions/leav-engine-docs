---
description: >-
  Cette documentation a pour objectif de vous aider a comprendre d'une part
  LEAV-Engine, ces avantages et bénéfices mais aussi de repenser la conception
  de base de données
---

# Welcome to LEAV-Engine



## The little story of LEAV Engine

Les principaux concepts de LEAV Engine ont été initié en 2001

Depuis plus de 30 ans, Didier Mombrun a créer plusieurs entreprises, toujours dans la communication mais toujours en lien avec les technologies.

{% hint style="warning" %}
Didier Mombrun est le fondateur de LEAV-Solutions et concepteur de LEAV-Engine et Data Studio
{% endhint %}

Dans les années 90, Didier est dirigant d'une société de prepress et réalise pour ses clients industriels et retailers des catalogues papier ainsi que leurs versions CDROM (Encore très populaire à l'époque) et les premiers sites web. C'est dans ce cadre qu'il s'intéresse à la possibilité de centraliser les données des catalogues produits dans une base de données pour alimenter avec les même informations l'ensemble des supports.

Ce n'est qu'en 2001, suite à la vente de son entreprise, qu'il décide d'investir dans le développement d'une solution de gestion des informations produits (PIM). Cette solution sera baptisé **Knowbox**. Alors que Didier ne connait pas de langage de programmation pour développer lui même une application full web, il utilise divers outils pour créer l'architecture et créer les premières maquettes de Knowbox. FileMaker mais également MySQL avec PHPMyAdmin ont beaucoup contribuer à sa réflexion pour concevoir le modèle Knowbox.&#x20;

Pour réaliser les développements de Knowbox, Didier fait appel à des développeurs indépendants et finance pendant plusieurs années avec ces propres économies ce projet ambitieux.

Les concepts fondamentaux de Knowbox sont la conséquence directe des délais et de la dépendance technique, économique avec les développements. En effet, dès la réception des premières interfaces et des correctifs a réaliser, une remarque a tout changé. Après avoir fait la recette de l'interface de la gestion des produits (Table des produits), celle-ci permet de lister, filtrer, afficher et d'éditer chaque enregistrement, ainsi que l'interface de gestion des Images (Visuels produits) et Documents (Notices, PDF...) avec les même fonctions, des dysfonctionnements sont indiqués sur la fonction de recherche de la bibliothèque des produits.&#x20;

Quelques semaines plus tard... les correctifs sont opérationnels sur la bibliothèque des produits, mais pas sur la même fonction de la bibliothèque des Images. Le développeur indique que ce n'est **pas le même code** et qu'il faudra non seulement attendre les correctifs pour cette partie mais assumer le coût supplémentaire associé.

A cet instant, Didier réalise l'importance d'être autonome mais aussi de ne plus dépendre des développements pour modifier et faire évoluer le data-modèle de Knowbox avec plusieurs objectifs :&#x20;

* Un seul code à maintenir pour toutes les fonctions communes et nécessaires à toutes les bibliothèques (Tables)
* Possibilité de créer dynamiquement des bibliothèques, des attributs et qu'ils soient immédiatement reconnu et utilisable dans la solution.

Pour cela, Didier a déjà les solutions et se souvient encore de la question qu'il croyait stupide, posée au développeur : \
Est il possible d'intégrer des variables dans une requête SQL, y compris le nom des tables et des champs ?

Didier se souvient encore du regard illuminé de ce développeur qui a répondu : "Oui bien sur !"

Après quelques semaines et la création des quelques tables systèmes permettant de référencer l'ensemble du modèles, les concepts de Knowbox Engine ont été défini. C'est actuellement le socle technique de la solution OmniPublish by ARiSTiD.

LEAV-Engine est l'évolution sur des technologies moderne et avec une expérience de 15 ans

{% hint style="success" %}
LEAV est l'acronyme de Library, Entity, Attribut, Value

En effet, une partie du modèle est basé sur le concept EAV (C'est lors de l'interfacage avec la plateforme ecommerce MAGENTO, que nous avons découvert 5 ans après qu'une partie du modèle était en fait un standard, remis à la mode par Magento ;-) Nous y avons ajouter la dimension relationnel avec les Liaisons entre bibliothèques.
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
