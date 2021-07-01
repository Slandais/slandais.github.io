---
title: Wordpress - eco-conception de l'intégration d'une vidéo Youtube avec Elementor
description: Comment éco-concevoir l'intégration d'une vidéo hébergée sur Youtube sur un site Wordpress utilisant Elementor
layout: post
category: tech
tags: [wordpress, youtube]
---

# Intro

Lorsque vous intégrez l'iframe Youtube sur votre site, celle-ci effectue plus de 14 requêtes aux serveurs Youtube pour charger les différents élements.


Sur un site dont vous maitrisez totalement le rendu HTML vous pouvez :

* [Utiliser l'attribut srcdoc de la balide iframe](https://dev.to/haggen/lazy-load-embedded-youtube-videos-520g) : ainsi seule la miniature est chargée. Le reste de l'iframe n'est chargé que si l'utilisateur clic pour voir la vidéo.
* [Utiliser le lecteur Youlazy](https://www.nuweb.fr/blog/post/793/youlazy-un-lecteur-youtube-eco-concu-et-accessible.html) : même principe en plus optimisée, puisque la miniature n'est chargé que si le navigateur doit l'afficher. Si celle-ci se situe en pied de page, elle ne sera pas affichée tant que l'utilisateur n'a pas scrollé.

# Wordpress & Elementor

Mais sur Elementor vous n'avez pas la main sur cet attribut srcdoc ou sur youlazy. Elementor vous permet tout de même de ne charger que la miniature à l'initialisation de la page.


Dans Elementor, ouvrez le panneau de modification de la vidéo et cliquez sur "Superposition d'image".


Activez les éléments suivants :

* Superposition d'image => Afficher
* Choisissez une image => la miniature de la vidéo (explication plus bas)
* Chargement différé => Oui
* Taille de l'image => Entière
* Icone de lecture => Oui
* Visionneuse => Arrêt


L'image de la miniature doit désormais être ajoutée à votre site. Voici comment la récupérer :

Récupérez l'identifiant de votre vidéo :

Par exemple l'identifiant de cette vidéo : [https://www.youtube.com/watch?v=jA8aHSMZ_DI](https://www.youtube.com/watch?v=jA8aHSMZ_DI)
est : jA8aHSMZ_DI


La miniature peut ainsi être récupérée en modifiant l'identifiant dans cette URL : [https://img.youtube.com/vi/jA8aHSMZ_DI/hqdefault.jpg](https://img.youtube.com/vi/jA8aHSMZ_DI/hqdefault.jpg)


Téléchargez-la et ajoutez-la dans Elementor dans le bloc Superposition d'image à la vidéo.
