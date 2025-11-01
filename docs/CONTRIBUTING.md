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
3. Soumettre votre PR et attendre les relecture des administrateurs


**Check-list avant de proposer une PR**
 - Le site en local démarre sans erreur.
 - Aucune erreur dans la console du navigateur.
 - L'affichage est correct sur mobile et desktop.
 - Les liens et images fonctionnent.
 - Le code respecte le style du projet.

### Lancer le projet en local
 Prérequis : Installer [Ruby](https://www.ruby-lang.org/fr/documentation/installation/)

```sh
# bootstrapping your local development environment
ruby -v
gem -v
bundler -v

# install the dependencies:
script/bootstrap
# Make sure the tests pass on your machine
script/cibuild

# télécharger et installer jekyll, github-pages, jekyll-seo-tag, etc.
# + un fichier Gemfile.lock pour verrouiller les versions.
bundle install
bundle exec jekyll serve --livereload --baseurl ""

```

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