# Templates

<img src="https://www.sgdsn.gouv.fr/files/styles/ds_image_paragraphe/public/files/Notre_Organisation/logo_anssi.png" alt="Logo ANSSI" width="30%">

## Agence nationale de la sécurité des systèmes d'information

[![badge_repo](https://img.shields.io/badge/ANSSI--FR-template-white)](https://github.com/ANSSI-FR/template)
[![badge_catégorie_interne](https://img.shields.io/badge/catégorie-interne-%23d08fce)](https://anssi-fr.github.io/#types-de-projets)
[![badge_ouverture_C](https://img.shields.io/badge/code.gouv.fr-publié-orange)](https://documentation.ouvert.numerique.gouv.fr/les-parcours-de-documentation/ouvrir-un-projet-num%C3%A9rique/#niveau-ouverture)

*Ce projet est édité par l'[ANSSI](https://cyber.gouv.fr/). Pour en savoir plus, voir la [page dédiée à la stratégie open source de l'ANSSI](https://cyber.gouv.fr/open-source-lanssi). Vous pouvez également cliquer sur les badges pour en savoir plus sur leur signification.*

## A propos

Ce dépôt contient des fichiers modèles pour les dépôts créés dans
l'organisation ANSSI-FR. Ces fichiers, disponibles dans le répertoire [`modeles`](/modeles/) représentent la politique par défaut pour
les projets open source de l'ANSSI et peuvent être adaptés en fonction de la feuille de route souhaitée par le projet.

- [LICENSE](modeles/LICENSE) contient la license par défaut (Apache 2.0)
- [CONTRIBUTING](modeles/CONTRIBUTING.md) contient la politique de contribution par
  défaut:
  - les contributions extérieures ne sont pas activement recherchées
  - sont uniquement acceptées les contributions concernant la sécurité
- [SECURITY](modeles/SECURITY.md) contient la politique de sécurité (contacter
  [opensource@ssi.gouv.fr](mailto:opensource@ssi.gouv.fr) en cas de problème de sécurité sur un projet)

En complément de ces modèles, un chapô a mettre en début du fichier `README.md` est aussi disponible dans le répertoire [`modeles`](modeles/). Ce dernier est disponible en français ([`chapo_README_FR.md`](modeles/chapo_README_FR.md)) et en anglais ([`chapo_README_EN.md`](modeles/chapo_README_EN.md)) et est à adapter pour refléter le contexte du projet.

## Configuration du chapô

Le chapô contient trois badges qu'il convient d'adapter au contexte du projet.

### Nom du projet

Le premier badge identifie le projet. 

```md
![badge_repo](https://img.shields.io/badge/ANSSI--FR-template-white)
```
Remplacer la partie **nom_du_projet** de l'url par le nom de votre projet. Si celui-ci comprend des `-`, doubler ce caractère pour qu'il soit pris en compte.

Par exemple, utiliser `template--test` pour afficher ![badge_repo](https://img.shields.io/badge/ANSSI--FR-template--test-white).

### Catégorie du projet

Ce badge fait référence à la stratégie open source de l'ANSSI présentée sur la [page Open source du site de l'agence](https://cyber.gouv.fr/enjeux-technologiques/open-source/). Les différents types de projets sont aussi présentés sur la [page `README.md`](https://anssi-fr.github.io/#types-de-projets) de l'organisation **ANSSI-FR**. A chacune des trois catégories est associé un badge que vous pouvez copier/coller pour configurer le chapô. Pour faciliter l'intégration, nous reprenons ici les trois badges et la ligne markdown associée :

* projets doctrinaux [![badge_catégorie_doctrinal](https://img.shields.io/badge/catégorie-doctrinal-%23e9c7e7)](https://anssi-fr.github.io/#types-de-projets)
```md
[![badge_catégorie_doctrinal](https://img.shields.io/badge/catégorie-doctrinal-%23e9c7e7)](https://anssi-fr.github.io/#types-de-projets)
```

* les outils internes [![badge_catégorie_interne](https://img.shields.io/badge/catégorie-interne-%23d08fce)](https://anssi-fr.github.io/#types-de-projets)

```md
[![badge_catégorie_interne](https://img.shields.io/badge/catégorie-interne-%23d08fce)](https://anssi-fr.github.io/#types-de-projets)
```

* les outils externes [![badge_catégorie_externe](https://img.shields.io/badge/catégorie-externe-%23b556b6)](https://anssi-fr.github.io/#types-de-projets)

```md
[![badge_catégorie_externe](https://img.shields.io/badge/catégorie-externe-%23b556b6)](https://anssi-fr.github.io/#types-de-projets)
```

#### Version anglaise

Pour les projets en anglais, vous pouvez utiliser les badges suivants :

* doctrinal projects [![category_badge_doctrinal](https://img.shields.io/badge/category-doctrinal-%23e9c7e7)](https://anssi-fr.github.io/README.en.html#project-categories)
```md
[![category_badge_doctrinal](https://img.shields.io/badge/category-doctrinal-%23e9c7e7)](https://anssi-fr.github.io/README.en.html#project-categories)
```

* internal tools [![category_badge_internal](https://img.shields.io/badge/category-internal-%23d08fce)](https://anssi-fr.github.io/README.en.html#project-categories)

```md
[![category_badge_internal](https://img.shields.io/badge/category-internal-%23d08fce)](https://anssi-fr.github.io/README.en.html#project-categories)
```

* external tools [![category_badge_external](https://img.shields.io/badge/category-external-%23b556b6)](https://anssi-fr.github.io/README.en.html#project-categories)

```md
[![category_badge_external](https://img.shields.io/badge/category-external-%23b556b6)](https://anssi-fr.github.io/README.en.html#project-categories)
```

### Niveau d'ouverture

Le niveau de contribution attendu par le projet open source est indiqué à l'aide de trois badges tirés de la [classification élaborée par la DINUM](https://documentation.ouvert.numerique.gouv.fr/les-parcours-de-documentation/ouvrir-un-projet-num%C3%A9rique/#niveau-ouverture). Les badges disponibles pour adapter le chapô sont repris avec le visuel et la ligne markdown associée :

* 📘 Niveau A - **contributif** [![badge_ouverture_A](https://img.shields.io/badge/code.gouv.fr-contributif-blue)](https://documentation.ouvert.numerique.gouv.fr/les-parcours-de-documentation/ouvrir-un-projet-num%C3%A9rique/#niveau-ouverture)

```md
[![badge_ouverture_A](https://img.shields.io/badge/code.gouv.fr-contributif-blue)](https://documentation.ouvert.numerique.gouv.fr/les-parcours-de-documentation/ouvrir-un-projet-num%C3%A9rique/#niveau-ouverture)
```

* 📗 Niveau B - **ouvert** [![badge_ouverture_B](https://img.shields.io/badge/code.gouv.fr-ouvert-green)](https://documentation.ouvert.numerique.gouv.fr/les-parcours-de-documentation/ouvrir-un-projet-num%C3%A9rique/#niveau-ouverture)

```md
[![badge_ouverture_B](https://img.shields.io/badge/code.gouv.fr-ouvert-green)](https://documentation.ouvert.numerique.gouv.fr/les-parcours-de-documentation/ouvrir-un-projet-num%C3%A9rique/#niveau-ouverture)
```

* 📙 Niveau C - **publié** [![badge_ouverture_C](https://img.shields.io/badge/code.gouv.fr-publié-orange)](https://documentation.ouvert.numerique.gouv.fr/les-parcours-de-documentation/ouvrir-un-projet-num%C3%A9rique/#niveau-ouverture)

```md
[![badge_ouverture_C](https://img.shields.io/badge/code.gouv.fr-publié-orange)](https://documentation.ouvert.numerique.gouv.fr/les-parcours-de-documentation/ouvrir-un-projet-num%C3%A9rique/#niveau-ouverture)
```

#### Version anglaise

Pour les projets en anglais, vous pouvez utiliser les badges suivants :

* 📘 Level A - **collaborative** [![openess_badge_A](https://img.shields.io/badge/code.gouv.fr-collaborative-blue)](https://documentation.ouvert.numerique.gouv.fr/les-parcours-de-documentation/ouvrir-un-projet-num%C3%A9rique/#niveau-ouverture)

```md
[![openess_badge_A](https://img.shields.io/badge/code.gouv.fr-collaborative-blue)](https://documentation.ouvert.numerique.gouv.fr/les-parcours-de-documentation/ouvrir-un-projet-num%C3%A9rique/#niveau-ouverture)
```

* 📗 Level B - **open** [![openess_badge_B](https://img.shields.io/badge/code.gouv.fr-open-green)](https://documentation.ouvert.numerique.gouv.fr/les-parcours-de-documentation/ouvrir-un-projet-num%C3%A9rique/#niveau-ouverture)

```md
[![openess_badge_B](https://img.shields.io/badge/code.gouv.fr-open-green)](https://documentation.ouvert.numerique.gouv.fr/les-parcours-de-documentation/ouvrir-un-projet-num%C3%A9rique/#niveau-ouverture)
```

* 📙 Niveau C - **published** [![openess_badge_C](https://img.shields.io/badge/code.gouv.fr-published-orange)](https://documentation.ouvert.numerique.gouv.fr/les-parcours-de-documentation/ouvrir-un-projet-num%C3%A9rique/#niveau-ouverture)

```md
[![openess_badge_C](https://img.shields.io/badge/code.gouv.fr-published-orange)](https://documentation.ouvert.numerique.gouv.fr/les-parcours-de-documentation/ouvrir-un-projet-num%C3%A9rique/#niveau-ouverture)
```
