---
description: >-
  Cette documentation a pour objectif de vous aider à comprendre comment mettre
  en œuvre LEAV-Engine avec ses avantages et bénéfices et ainsi, repenser la
  conception d'applications de base de données.
---

# Welcome to LEAV-Engine

LEAV Engine a été imaginé pour permettre à des spécialistes sans connaissances de langage de programmation d'être autonome pour développer des applications de gestion de données modernes et évoluées. En résumé, on passe directement du besoin à la réalisation.

Pour cela nous avons dissocié le code du modèle des données. Ce sont les données métiers qui portent toute l'intelligence. Le code de LEAV Engine est utile pour la manipulation des données afin de créer, modifier, exporter et bien d'autres fonctions courantes de toutes les applications de datas.

Nous expliquons dans cette documentation, comment les interfaces LEAV Data Studio et l'API LEAV Engine, supervisent le modèle générique et les données dans la base ArangoDB afin de préserver ses performances, sa cohérence et d'en tirer toute la puissance et évolutivité.

Nous expliquons comment LEAV Engine est allé plus loin que la plupart des applications NoCode disponibles sur les bases de données qui se contentent pour la plupart de gérer des tables, des champs et des relations.&#x20;

LEAV Engine propose plusieurs manières de stocker des valeurs et des liens, avec des modèles  dit "verticaux", "horizontaux" et "hiérarchiques". Ce jargon métier vous sera expliqué et vous comprendrez, sans avoir fait de hautes études en architecture de base de données, que ces termes correspondent à des méthodes que vous utilisez intuitivement sans savoir qu'elle ont un nom et qu'elles sont documentées.\


{% hint style="info" %}
**LEAV** est l'acronyme de **Library, Entity, Attribut, Value**

Le modèle LEAV-Engine offre en plus des modèles classiques, une fonction très avancée permettant de lier à un attribut (champs) une infinité de versions de valeurs ou de liens. Outre la gestion classique de champs multivalués, cette fonction permet sur un même attribut d'associer des versions des valeurs ou liaisons en fonction de variables.\
Ces variables peuvent être la langue pour gérer le multilingue, mais aussi tout autre notion utile à votre application telle que, par exemple, des versions de prix en fonction des régions ou Pays - ceci sans devoir multiplier le nombre d'attributs.

Pour mettre en œuvre cette fonction avancée, nous nous sommes inspirés du modèle EAV (Dit Vertical) auquel nous avons ajouté la dimension de Liaisons et de [Librairies](configuration/data-model/library.md)\

{% endhint %}

## Quick links

{% content-ref url="getting-started/what-is-leav-engine.md" %}
[what-is-leav-engine.md](getting-started/what-is-leav-engine.md)
{% endcontent-ref %}

{% content-ref url="getting-started/data-model-and-concepts.md" %}
[data-model-and-concepts.md](getting-started/data-model-and-concepts.md)
{% endcontent-ref %}

## Get Started

Des guides pour démarrer avec LEAV-Engine.

{% content-ref url="getting-started/premiers-parametrages/" %}
[premiers-parametrages](getting-started/premiers-parametrages/)
{% endcontent-ref %}

{% content-ref url="getting-started/premiers-parametrages/setting-permissions.md" %}
[setting-permissions.md](getting-started/premiers-parametrages/setting-permissions.md)
{% endcontent-ref %}

{% content-ref url="getting-started/premiers-parametrages/inviting-members.md" %}
[inviting-members.md](getting-started/premiers-parametrages/inviting-members.md)
{% endcontent-ref %}
