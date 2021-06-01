---
title: Analyser l'impact environnement de son site Internet
description: Présentation des outils permettant d'analyser les impacts environnementaux de son site Internet
permalink: /analyser-impact-environnement-site-internet/
layout: post
category: tech
tags: [site internet]
---

# Analyser l'impact environnement de son site Internet

## WebsiteCarbon

WebsiteCarbon donne une estimation de l'empreinte carbone de l'URL donnée.

* [WebsiteCarbon](https://www.websitecarbon.com/)

## EcoIndex

L'ecoindex est un outil indiquant :
* la performance environnement absolue d'un site Internet, avec un score sur 100
* la performance environnement relative d'un site Internet, à l'aide d'une note de A à G
* l’empreinte technique de la page (complexité du DOM, poids, nombre de requêtes, etc.)
* l’empreinte environnementale associée (empreinte carbone, consommation d'eau etc.)

Le calcul est Open Source, et peut être utilisé avec :
* [Une extension dans votre navigateur](http://www.ecoindex.fr/)
* [Cette ligne de commande](https://github.com/cnumr/ecoindex_cli)
* [Ce simulateur en ligne](https://rachelwe.github.io/Simulateur-ecoindex/)

[En savoir plus sur son fonctionnement](http://www.ecoindex.fr/quest-ce-que-ecoindex/)

Selon le type de site réalisé, il est plus ou moins aisé d'avoir une bonne note. La page d'accueil d'un moteur de recherche peut être très sobre et obtenir un bon score, alors que ce sera plus difficile sur la page d'accueil d'un site d'information. Un site d'information peut en revanche tenter d'avoir le meilleur score possible.

Comparaison des moteurs de recherche (testé en mai 2021)

| Moteur de recherche         | Score           | Note            |
| --------------- | --------------- | --------------- |
| Qwant           | 79              | A{.ecoIndexA} |
| DuckDuckGo      | 79 | {% include tooltip.html note="A" %} |
| Ecosia          | 68 | B{.ecoIndexB} |
|    Google       |    75    | {% include tooltip.html note="B" %} |
|    Lilo         |    43    | D |
|    Bing         |    32    | E   |
|    Yahoo        |    20    | F   |

Comparaison des sites d'informations (testé en mai 2021)

| Moteur          | Score           | Note            |
| --------------- | --------------- | --------------- |
| Mediapart          | 44 | D |
| Franceinfo          | 47 | D |
| L'Équipe          | 47 | D |
|    Slate       |    32    | E |
|    20minutes       |    26    | E |
|    Libération       |    22    | E |
|    Le Monde         |    18    | F |
|    Le Point         |    6    | F   |
|    Le Parisien         |    5    | G   |
|    Le Figaro        |    0    | G   |
