---
description: >-
  LEAV-Engine et DATA STUDIO simplifient l'accès et le partage de vos données et
  vos fichiers
---

# Data model & Concepts

Vos données et vos fichiers restent totalement accessibles par n'importe qu'elles autres moyen ou interfaces ou codes de votre création. LEAV-Engine est une autre façon d'y accéder.

DATA Studio n'est qu'une interface graphique alimentée par l'API, qui permet aux développeurs, aux utilisateurs professionnels et aux analystes d'avoir un même accès centralisé aux données et aux fichiers.

{% hint style="info" %}
A la différence de beaucoup de solutions proposées dans la galaxy NoCode & LowCode, LEAV-Engine est basé sur une base de données DOCUMENTS orienté Graph de l'éditeur ARANGO DB OpenSource (Community edition).
{% endhint %}

## Un modèle de données sous contrôle

#### For performance, the LEAV-Engine data-model has some constrain and prérequisite

A set of system collections to control the user data model. The need of an identifier in all collections, attributs, trees and any LEAV Engine object.

**Généralité sur les bases de données relationnelles classiques vs Documents**

Dans une base de données relationnelle classique il y a des **tables** avec des **lignes** et des **colonnes.** Une ligne est appelé « enregistrement » ou « entités » Une colonne est appelé « champs » De ce fait, tout les champs même vides sont communs à toutes les lignes d'une même table.

Considérons une table contacts avec les champs suivant : \
Nom, Prénom, adresse, n°Contact, type contact,  

Considérons l’enregistrement de contacts avec les valeurs suivantes comme des couples (Champ : Valeur) : \
 (N°Contact : 01) (Nom : Dupont) (Prénom : Michel) (Adresse : 12 rue du parc) (Type contact : client) (N°Entreprise : 1234) \
(N°Contact : 02) (Nom : Durant) (Prénom : Jean) (Adresse : ) (Type contact :) (N°Entreprise :)  

Afin de créer une liaison entre le contact et l’entreprise il est nécessaire de référencer l’identifiant de l’entreprise sur chaque contact

(N°Entreprise : 1234) (Nom : Newco) \
(N°Entreprise : 5678) (Nom : Acme)

Grâce à la jointure sur « N°Entreprise» on pourra afficher le nom de l’entreprise et retrouver tout les contacts de celle-ci.&#x20;

\=> « Michel Dupont » fait parti de l’entreprise « Newco » &#x20;

**Utilisation du modèle EAV (Entités - Attributs - Valeurs)**&#x20;

{% hint style="info" %}
Le modèle EAV est souvent et intuitivement utilisé sans même savoir qu’il a un nom et qu’il est documenté. Ce modèle permet entre autre de créer une architecture facilement extensible notamment pour gérer des données complexes et hétérogènes. Plus généralement de gérer des champs multi-valués et aussi lorsqu’il y a beaucoup de champs et dont seulement un petit nombre sont utiles pour chaque enregistrement.
{% endhint %}

Bien que controversé, le modèle EAV ne doit pas être la seule alternative mais un complément presque incontournable dans certaines configuration avancées. C’est la raison pour laquelle nous avons intégré notre vision du modèle EAV dans LEAV Engine.

Dans un modèle classique, les valeurs sont intimement liées à chaque colonne (Champs). Cependant, dans le cas d’une colonne avec des valeurs multiples, il est recommandé de créer une table pivot dédié à ces valeurs. Cette table devra contenir au moins 2 colonnes voir 3 colonnes si mutualisés pour tout les attributs multi-valués d'une même table.

* Une colonne pour l’identifiant de la ligne contact (Entité)
* Une colonne pour l’identifiant de la colonne (Attribut)
* Une colonne pour la valeur (Value)&#x20;

Dans cette configuration, il n’y a pas la nécessité de créer réellement la colonne (champ) dans la table parent. Pour cela il faut une table spécifiques pour référencer tout les attributs et leurs propriétés, y compris les attributs faisant réellement référence à un champ, cette méthode permet entre autre de gérer le libellé des colonnes et ses éventuelles traductions.

Ainsi chaque valeur sera une ligne dans la table pivot

Considérons que les contacts ci-dessus ont plusieurs N° de téléphone et adresses

(Attribut : phone), (N°contact : 01), (Value : 01 02 03 04 05)\
(Attribut : phone), (N°contact : 01), (Value : 01 05 06 04 99)\
(Attribut : adresse), (N°contact : 01), (Value : 24, rue albert)\
(Attribut : adresse), (N°contact : 01), (Value : 24, rue des roses)\
(Attribut : phone), (N°contact : 02), (Value : 04 23 24 25 26)\
(Attribut : phone), (N°contact : 02), (Value : 08 81 82 83 84)\
(Attribut : adresse), (N°contact : 02), (Value : 12, rue Elisabeth)\
(Attribut : adresse), (N°contact : 02), (Value : 24, avenue des Lilas)

{% hint style="info" %}
Nos explication sont volontairement simplifiée dans le seul but d’illustrer le concept EAV. En effet, il existe une multitude de variantes de ce modèles chacun avec ces avantages et inconvénients. Nous y consacrerons un article dans notre Blog.
{% endhint %}

### **Quelques généralité sur la base de données documents ArangoDB**

Notre propos est de présenter en simplifiant, les similitudes entre une base de données relationnel et documents dans le seul but d’aider un spécialiste de base de données relationnel à ce projeter dans un modèle Document orienté graph.

Dans une base de données Documents, On ne parle pas de tables mais de collections qui sont l’équivalent. Chaque enregistrement d’une collection est appelé « document » ces propriétés et informations sont structurées au format JSON. Les propriétés (Metadonnées) de chaque document sont sous la forme de Clé / Valeur. C’est l’équivalent des (Champ : Valeur) d’une base relationnelle.&#x20;

Contrairement à une table ou chaque enregistrement a toujours les même champs, un document contient uniquement les champs qui lui sont utiles.  

« Contact : \
N°Contact : 01 \
nom : Dupont \
prénom : Michel \
adresse : 12 rue du parc \
typecontact : client »

« Contact : \
N°Contact : 02 \
nom : Dupont \
prénom : Michel \
adresse : 12 rue du parc »

« Entreprise : \
N°Entreprise : 1234 \
nom : Newco »

La relation entre le contact et l’entreprise est réalisé via un attribut de LIAISON. Dans ce cas il s’agit de l’attribut « Entreprise ».

{% hint style="info" %}
Dans une base NoSQL orienté graph les liaisons sont matérialisés par des « arc ». ArangoDB ce sont des collections « EDGE » ou chaque enregistrement (Document) contient les clés / valeurs : « from / to » \
« from » est la clé \[contact] et « to » la clé \[entreprise] \
Cette méthode peut être assimilé à une table de jointure N To N dans une base de données relationnelle.
{% endhint %}

Exemple de la liaison \
« Entreprise : \
from : 01 \
to : 1234 »

Dans LEAV Engine nous avons rassembler et intégrés ces relations dans 4 types d’attributs pour l’ensemble des relations One to One, One to Many, One to Any et Many to Many.

* **Attribut simple** : \[clé : valeurs] enregistrés dans le document
* **Attribut liaison simple** : \[clé : valeurs] enregistrés dans le document. Dans ce cas la valeur est elle même la clé d'un document(s). Ce type de relation est techniquement effectué avec une jointure.
* **Attributs avancé** : Liaison « edge » \[From : To] pour lier des documents. Cette relation est exclusivement utilisé pour des liaisons vers des valeurs (Table Pivot de type EAV)
* **Attributs liaisons avancé** : Liaison « edge » \[From : To] pour lier des documents. Cette relation est utilisé pour lier tout type de documents de toutes bibliothèques

Chacun de ces attributs sont au choix Mono ou Multi-valués.

### **Application du modèle EAV by LEAV-Engine**

Prenon l'exemple d'une bibliothèque de produits avec des caractéristiques multilingues et des prix en fonction du pay

Variable : Langue = fr/FR, Prix = France&#x20;

« produits : \
N°Produit : 01 \
<mark style="color:blue;">Libellé : Tuyau</mark> \
référence : 23456 \
<mark style="color:blue;">Couleur : gris</mark> \
Diamètre : 25 \
<mark style="color:blue;">Prix: 12€</mark> »

« Produits : \
N°Produit : 02 \
<mark style="color:blue;">Libellé : Vis</mark> \
référence : 5678 \
<mark style="color:blue;">matière : métal</mark> \
longueur : 12 \
<mark style="color:blue;">Prix : 0.3€</mark>»

Variable : Langue = it/IT, Prix = Italie&#x20;

« Produits : \
N°Produit : 01 \
<mark style="color:blue;">Libellé : Tubo</mark> \
référence : 23456 \
<mark style="color:blue;">Couleur : grigio</mark> \
Diamètre : 25 \
<mark style="color:blue;">Prix: 10€</mark>»

« Produits : \
N°Produit : 02 \
<mark style="color:blue;">Libellé : Vite</mark> \
référence : 5678 \
<mark style="color:blue;">matière : metallo</mark> \
longueur : 12 \
<mark style="color:blue;">Prix : 0.25€</mark> »

L'utilisation du modèle EAV by LEAV Engine permet de gérer des valeurs multiples et/ou des versions par exemple pour gérer les traductions (Multilingue).&#x20;

Les valeurs en "bleu" ci-dessus sont externalisées dans une bibliothèque pivot avec une liaison EDGE pour la langue "Libellé", "matière".&#x20;

**Ci-dessous le schémas pour afficher la version \[Langue] frFR / itIT et le \[Prix] Francais, Italie.**

**Collection (EDGE) :**\
« Libellé : \
From : 01 \
To : 5678 »

« Libellé : \
From : 01 \
To : 5679 »

« couleur : \
From : 01 \
To : 6789 »

« couleur : \
From : 01 \
To : 6790 »

« Prix : \
From : 01 \
To : 5680 »

« Prix : \
From : 01 \
To : 5681 »

**Collection : "value"**\
« value : \
id : 5678 \
value : Tuyau \
langue : frFR »

« value : \
id : 5679 \
value : Tubo \
langue : itIT »\
\
« value : \
id : 6789 \
value : gris \
langue : frFR »

« value : \
id : 6790 \
value : Grigio \
langue : itIT »

« value : \
id : 5680 \
value : 12€ \
pay : france »

« value : \
id : 5681 \
value : 10€ \
pay : italie »
