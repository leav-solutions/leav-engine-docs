---
description: >-
  Cette documentation a pour objectifs de vous aider à comprendre comment mettre
  en œuvre LEAV-Engine avec ces avantages, bénéfices et repenser la conception
  d'applications de base de données.
---

# Welcome to LEAV-Engine

LEAV Engine a été imaginé pour permettre à des spécialistes sans connaissance de langage de programmation d'être autonome pour développer des applications de gestion de données modernes et évolués. En résumé, de passer directement du besoin à la réalisation.

Pour cela nous avons dissocié le code du modèle et des données. Ce sont les données métiers qui portent toute l'intelligence et non pas le code qui n'est utile qu'à la manipulation des données pour créer, modifier, exporter et bien d'autres fonctions courantes et nécessaires à toutes les applications qui s'appuient sur des données.

Nous expliquons dans cette documentation, comment les interfaces LEAV Data Studio et l'API LEAV Engine, supervise le modèle et les données dans la base ArangoDB afin de préserver ses performances, sa cohérence afin d'en tirer toute la puissance et évolutivité.

Nous expliquons comment LEAV Engine est aller plus loin que la plupart des applications NoCode disponibles sur les bases de données et pour gérer des tables, des champs des relations.&#x20;

LEAV Engine propose plusieurs manière de stocker des valeurs et des liens, tels que les modèles  dit "Verticaux", "horizontaux" et "hierarchiques". Ce jargon métier vous sera expliqué et vous comprendrez sans études professionnelles en architecture de base de données que ces termes correspondent à des méthodes que vous utilisez intuitivement sans savoir qu'elle ont un nom et qu'elles sont documentés.\


{% hint style="info" %}
LEAV est l'acronyme de Library, Entity, Attribut, Value

En effet, le modèle LEAV-Engine offre en plus des modèles classique, une fonction très avancée permettant de lier à un attributs (Champs), une infinité de versions de valeurs ou de liens. Outre la gestion classique de champs multivalués, cette fonction permet sur un même attribut d'afficher une version des valeurs ou liaisons en fonction de variables.\
Ces variables peuvent être la langue, pour gérer le multilingue, mais tout autres notions utiles à votre application tels que par exemple des versions de prix en fonction des régions ou Pays sans avoir a multiplier le nombre d'attributs.

Pour mettre en œuvre cette fonction avancé, nous nous sommes inspiré du modèle EAV auquel nous avons ajouté la dimension de Liaison et de [Librairie](configuration/data-model/library.md)\

{% endhint %}

## Quick links

{% content-ref url="getting-started/introduction.md" %}
[introduction.md](getting-started/introduction.md)
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
