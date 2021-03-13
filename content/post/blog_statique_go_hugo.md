---
title: "Creation d'un blog statique thème Github avec GoHugo"
date: 2021-03-13T12:24:39+01:00
draft: false
---

<!--more-->

# Création d'un blog statique en Markdown avec GoHugo

* [Site officiel GoHugo](https://gohugo.io)
   
* [Choisir votre thème](https://themes.gohugo.io)

* [Installer GoHugo](https://gohugo.io/getting-started/quick-start/)

* [URL du thème choisi](https://github.com/MeiK2333/github-style)

## Intialiser le site

Ouvrez un terminal dans le dossier de conteneur de votre futur blog

```
hugo new site blog
cd blog
git init
cd themes
git submodule add https://github.com/MeiK2333/github-style
cd ..
mkdir content/post
cp themes/github-style/config.template.toml config.toml

hugo new readme.md
echo '`Mon blog avec GoHugo!`' > content/readme.md
hugo new post/my_first_post.md
echo '`Contenu de mon premier blog post`' > content/post/my_first_post.md
hugo serve
```

Server web démarré sur [http://localhost:1313/](http://localhost:1313/)

#### TODO

* Modifier la config de votre site dans config.toml
* Ajouter votre avatar dans static/images/avatar.png
* Ajouter dans la section params du config.toml ``avatar = "/images/avatar.png"``
* Ajouter vos sources dans un projet Github
* Modifier la présentation votre blog **content/readme.md**
* Ecrire votre premier post **content/post/my_first_post.md**

### Générer les fichiers statiques

```
hugo
```

Fichiers générés dans ./public

Prochain post : déployer facilement avec [Qovery](https://www.qovery.com/)
