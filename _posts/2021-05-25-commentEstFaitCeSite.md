---
title: Comment est fait ce site ?
description: Présentation des outils techniques (stack technique) utilisés pour réaliser le site www.numerique-raisonne.fr
permalink: /stack-technique-du-site/
layout: post
---

# Site statique

numerique-raisonne.fr est un site statique, c'est à que le contenu est constitué de page HTML. 
Il n'y a pas de traitement effectué par le serveur au moment où vous tentez de consulter une page. L'absence de ce traitement serveur fait que la page s'affiche plus rapidement.

Les sites statiques se distinguent donc des sites dynamiques, qui peuvent être générés par du PHP, tels que Wordpress ou Drupal. 
Un site dynamique récupère en général le contenu dans une base de donnée, et assemble l'ensemble des données à la volée pour générer une page HTML.
Pour éviter d'avoir de mauvaises performances un site dynamique doit utiliser un système de cache. Un cache permet de stocker temporairement la page HTML générée.
Les CMS tel que Wordpress ou Drupal disposent de plugin à ajouter permettant de gérer ce cache.
Sans cache, les sites dynamiques seront plus lents à s'afficher. Si vous avez un site dynamique, pensez donc à ajouter un système de cache.
Afin de tenir compte des mises à jour du contenu en base de données, il faut alors effacer ce cache. Cette gestion du cache peut parfois être compliqué.

# Générateur de site statique : Jekyll

Bien que le site soit un site statique, je n'ai pas écris chaque page entièrement en HTML. J'utilise un générateur de site statique.
Un générateur de site statique permet de rédiger son contenu et structurer son site dans un autre format que le HTML plus simple à structurer et administrer.
Une étape permet alors de générer les pages HTML qui seront accessibles aux visiteurs.

Il existe plusieurs générateurs de site statique, mon choix s'est porté sur Jekyll. Le contenu est structuré avec les languages Markdown et Liquid.

# Git-based CMS

Le site est aussi un Git-based CMS, c'est à dire que son contenu n'est pas stockée en base de données mais versionné dans un repository git.
Cela permet de tout versionner et de facilement pouvoir revenir en arrière. Les pages et articles sont stockés sous forme de fichier Markdown.

# GitHub Pages

GitHub Pages permet d'hébergé de site Jekyll avec le mécanisme Git-based. En modifiant le contenu du site dans GitHub, celui-ci génère les pages HTML qui seront alors visibles des visiteurs.

# Framework CSS sans classe : SimpleCSS

Un framework CSS sans classe (en anglais "Classless CSS Framework" ou "No-Class CSS Framework") est un framework CSS ne se basant que sur les balises natives du HTML.
Il se dinstingue donc des autres framework CSS, comme Bootstrap, Tailwind CSS ou Foundation, qui vont proposer des classes CSS spécifiques au framework à ajouter dans votre HTML.

Les avantages des frameworks CSS sans classe sont donc de plus facilement pouvoir passer d'un framework CSS sans classe à un autre, puisqu'il n'y a pas de classe CSS spécifique. Ces frameworks sont aussi plus léger.

Les inconvénients c'est qu'ils proposent moins de fonctionnalités. Ils sont donc moins adaptés à la création de grosse applications web avec un travail en équipe, où l'usage d'un plus gros framework permettra d'harmoniser des composants plus élaborés d'un écran à un autre (système d'onglets, datePicker, modal, dropdown).

Pour le site numerique-raisonne.fr j'ai fait le choix de [SimpleCSS](https://simplecss.org/) qui ne pèse que 4kb alors que Bootstrap pèse 144Kb.

Comparatifs d'autres frameworks sans classes :
* (https://www.designinspiration.info/classless-css-frameworks)
* [https://dev.to/skypack/the-best-classless-css-frameworks-in-2021-427a]

# Aller plus loin

Si vous, ou des éditeurs du site, ne sont pas à l'aise avec le fait d'écrire des articles/pages en Mardown, alors il est possible possible d'utiliser un outil tel que [Forestry](https://forestry.io/) qui permet de gérer le contenu comme on le ferait dans un CMS Wordpress ou Drupal.
Forestry s'occupe alors de faire les actions dans git.
