# Guide de contribution au site Canislupa

### Code of conduct

Ce projet est régi par le code de conduite du [Contributor Covenant](https://www.contributor-covenant.org/fr/version/2/1/code_of_conduct/). En participant, vous vous engagez à respecter ce code.

### Vous avez trouvé un bug ou souhaitez suggérer une idée ?

Vérifiez d'abord que le bug n'a pas déjà été signalé dans les [Issues](https://github.com/canislupa-services/website/issues).  
Sinon, créez une nouvelle issue avec un titre clair, une description et autant d'informations que possible.

### Comment titrer vos commits ?

Un commit sert à décrire et enregistrer le changement que vous venez d'apporter au projet. Vous pouvez soit utiliser la [convention de commit](https://www.conventionalcommits.org/) standard, soit simplement avoir une petite desciption clair avec un résumé court du changement (≤ 50 caractères).

Exemple de message de commit :  
`"Ajout d'une adresse dans la page contact"`

### Vous voulez apporter une contribution au site et soummettre une Pull Request ?

1. Créez une nouvelle [branche](https://conventional-branch.github.io/):  
   `git checkout -b my-branch-name`
2. Implémentez vos modifications ou correctifs dans cette branche
3. Valider la check liste ci-dessous
4. Soumettre votre PR et attendre les relecture des administrateurs

**Check-list avant de proposer une PR**

- Le site en local démarre sans erreur.
- Aucune erreur dans la console du navigateur.
- L'affichage est correct sur mobile et desktop.
- Les liens et images fonctionnent.
- Le code respecte le style du projet.

### Lancer le projet en local

Prérequis : Installer [Ruby](https://www.ruby-lang.org/fr/documentation/installation/)

```sh
# bootstrappé l'environnement de dev local
ruby -v
gem -v
bundler -v

# installer les dependences:
./script/bootstrap

# lancer le server en local
./script/server
# -> Visitez localhost:4000 dans votre navigateur pour prévisualiser le site

# tester la validation html en local
./script/validate-html

# lancer tous les tests de validation
./script/cibuild

```

### Informations sur le projet

[![.github/workflows/ci.yaml](https://github.com/pages-themes/cayman/actions/workflows/ci.yaml/badge.svg)](https://github.com/pages-themes/cayman/actions/workflows/ci.yaml) [![Gem Version](https://badge.fury.io/rb/jekyll-theme-cayman.svg)](https://badge.fury.io/rb/jekyll-theme-cayman)

_Cayman is a Jekyll theme for GitHub Pages. You can [preview the theme to see what it looks like](http://pages-themes.github.io/cayman), or even [use it today](#usage)._

**Design**
On utilise la base de thème Cayman avec la balise `@import`, qu'on customise dans `/assets/css/style.scss`.
On peut personaliser la mise en page du site dans le fichier `/_layouts/default.html`

**Variables de configuration**
Cayman respecte les variables suivantes, si elles sont définies dans les paramètres de \_config.yml :

```yml
title: [The title of your site]
description: [A short description of your site's purpose]
```

De plus, vous pouvez choisir de définir des variables facultatives :

```yml
show_downloads: ["true" or "false" (unquoted) to indicate whether to provide a download URL]
google_analytics: [Your Google Analytics tracking ID]
```

**Layouts**

- Pour certaines modifications, comme une personnalisation favicon, vous pouvez ajouter des fichiers personnalisés dans votre \_includes dossier local. Les fichiers [fournis avec le thème](https://github.com/pages-themes/cayman/tree/master/_includes) constituent un point de départ et sont inclus par le modèle de mise en page d'origine.

**overriding GitHub-generated URLs**
Consultez le code source du template pour déterminer le nom de la variable. Il sera sous la forme de {{ site.github.zip_url }}.
Spécifiez l'URL que vous souhaitez que le modèle utilise dans le code HTML de votre site \_config.yml. Par exemple, si la variable est `site.github.url`, vous ajouterez ce qui suit :

```yml
github:
  zip_url: http://example.com/download.zip
  another_url: another value
```

Lors de la création de votre site, Jekyll utilisera l'URL que vous avez spécifiée, plutôt que celle par défaut fournie par GitHub.
Remarque : Vous devez supprimer le site.préfixe, et chaque nom de variable (après le github.) doit être indenté de deux espaces en dessous github:.

Pour plus d'informations, consultez la documentation [the Jekyll variables documentation](https://jekyllrb.com/docs/variables/).

### Docs utils :

- [Jekyll style guide](https://ben.balter.com/jekyll-style-guide)
- [Soumettre une Pull Requests](https://help.github.com/articles/using-pull-requests/)
- [GitHub Help](https://help.github.com)

### Licence et crédits

En contribuant, vous acceptez [la licence](../LICENSE) tous droits réservés du projet.

### Contact

Des questions ? Ouvrez une [Issues](https://github.com/canislupa-services/website/issues).

### 💚 MERCI !

Pour votre contribution et votre implication et n'hésitez pas à demander de l'aide, tout le monde a été débutant un jour !
