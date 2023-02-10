    +++
title = "LeCodeEtMoI"
sort_by = "weight"
+++

# LeCodeEtMoi

## Comment créé une page web  le guide complet 

# Les bases 

Pour pouvoir programmer une pages web il faut avoir un editeur de code ( SublimeTexte , Visual Studio Code Note++) a vous de choisir .
Une fois installer nous allons voir 2 version une version avec le code HTML et l'autre avec du Markdown
Si vouler metre votre page web sur Internet et qu'elle soit accesible  a tout moment vous dervrait sur la version 2 sinon nous devons suivre la version 1

# Version 1 

Nous allons donc dire a notre éditeur de code que nous allons utiliser le code HTML . Pour programmer notre page web on comment toujour comme sa 
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title></title>
</head>
<body>

</body>
</html>
```
Normalement que l'on tape html , il va vous proposé la même infrastructure

Entre les balise <title></title> vous metter le nom de votre site web , c'est ce qui va s'afficher sur l'onglet 

Nous ont va écrire a l'interieur des <body></body> . Vous l'avez peut être compris mais les balises vonction en pair la premier balise <> et la dernier balise </> 

Nous allons metre du texte dans notre page web . Pour mettre du texte il y a plusieur balise a savoir
Les balise pour le texte 
```html
La taille de police 
<h1></h1> Souvent utiliser pour un titre 
<h2></h2>
<h3></h3>
<h4></h4>

Pour faire un paragraphe 
<p></p>

Pour metre en gras 
<b></b>
Pour metre en italique 
<i></i>

Pour revenir a la ligne
<br>

Pour faire des listes 
<ul></ul>
et rajouter <ol></ol> pour que la liste soit en chiffre
```
Donc voici un exemple 

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title></title>
</head>
<body>
<h1>Bonjour a tous </h1>
<p>Nous allons voir un tutoriel qui nous montre comment faire un site web et voici 2 mot que j'ai appris 
<ol>
 <ul>balise</ul>
 <ul>HTML</ul>   
</ol>
</p>
</body>
</html>

```

Apres il y a beaucoup de balise voici [un site qui les reference tout] https://www.w3schools.com/html/default.asp


# Version 2

Pour pouvoir mettre son site en ligne nous allons utiliser gituhb 


















# Installation

> **Zola** is a prerequisite. Please refer to the [Zola installation](https://www.getzola.org/documentation/getting-started/installation/) docs.

First download this theme to your `themes` directory:

```bash
$ cd themes
$ git clone https://github.com/huhu/juice.git


or add as a submodule
```bash
$ git submodule add https://github.com/huhu/juice  themes/juice
```

and then enable it in your `config.toml`:

```toml
theme = "juice"
```

# Structure

### Hero

**Juice** is designed for product websites, hence we let **hero** part fills whole of screen.
You can customize your **hero** by using `hero` block in the `templates/index.html`.

```html
{% extends "juice/templates/index.html" %}
{% block hero %}
    <div>
        Your cool hero html...
    </div>
{% endblock hero %}
```

### Page

Every markdown file located in `content` directory will become a **Page**. There also will display as
a navigate link on the top-right corner. 
You can change the frontmatter's `weight` value to sort the order (ascending order).

```
+++
title = "Changelog"
description = "Changelog"
weight = 2
+++

```

### CSS variables

You can override theme variable by creating a file named `_variables.html` in your `templates` directory.

```html
<style>
    :root {
        /* Primary theme color */
        --primary-color: #FED43F;
        /* Primary theme text color */
        --primary-text-color: #543631;
        /* Primary theme link color */
        --primary-link-color: #F9BB2D;
        /* Secondary color: the background body color */
        --secondary-color: #fcfaf6;
        --secondary-text-color: #303030;
        /* Highlight text color of table of content */
        --toc-highlight-text-color: #d46e13;
    }
</style>
```

### Favicon

```html
{% extends "juice/templates/index.html" %}
{% block favicon %}
    <link rel="icon" type="image/png" href="/favicon.ico">
{% endblock favicon %}
```

# Configuration

You can customize some builtin property in `config.toml` file:

```toml
[extra]
juice_logo_name = "Juice"
juice_logo_path = "juice.svg"
juice_extra_menu = [
    { title = "Github", link = "https://github.com/huhu/juice"}
]
repository_url = "https://github.com/huhu/juice"
```

# Shortcodes

**Juice** have some builtin shortcodes available in `templates/shortcodes` directory. 

- `issue(id)` - A shortcode to render issue url, e.g. `issue(id=1)` would render to the link `https://github.com/huhu/juice/issue/1`.
  
> The `repository_url` is required.

# Showcases

Please see the [showcases page](/showcases).

# Contributing

Thank you very much for considering contributing to this project!

We appreciate any form of contribution:

- New issues (feature requests, bug reports, questions, ideas, ...)
- Pull requests (documentation improvements, code improvements, new features, ...)
