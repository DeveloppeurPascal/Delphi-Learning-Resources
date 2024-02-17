---
title: About this project and website
lang: en
---
# Website template for languages/topics/links websites hosted on Github Pages

[This repository]({{ site.github.repository_url }}) is a template for web site generation with MD files.

## What does it do ?

this repository generate a 3 level website :
- index with list of languages
- a page for each language with its topics list
- a page for each topic with its links list

## Why a website and not simple MD/text files ?

Simply for visibility reasons. Markdown / text files are simple to use and maintain in a repository but we can only read them when we stay on repository platform.

It's not as visible on search engines than websites.

Creating the website from MD files is a sort of best of 2 worlds : MD files maintaining on Github is simple, generating the website is automatic, and we can use this website on GitHub Pages as any other website with links, SEO and SEA.

## How to use it ?

Copy this repository template as a new repository directly from GitHub.

Remove "/.github" folder or change the sponsor links in it (don't lets mine on your repos !).

Change the copyright in "/includes/footer.html" file if you want. By default it displays datas from your GitHub repository datas.

Edit the "/index.html" file to change it's "title" property.

Copy templates files (and rename copies) from "/_template_files_for_data_collections" folder to :
* "/_data_languages" for languages pages (one file per language)
* "/_data_topics" for topics pages (one file per language/topic with the same "family" property)
* "/_data_links" for links (as many files you need per language/topic)

After adapting your "css/styles.css" file, activate GitHub Pages on your repository (go to "Settings / Pages" for that).

GitHub will launch Jekyll on your repository from a GitHub action and generate a website each time you push your commits.

GitHub allow us to use our domaine name for free. For SEO reasons it's better than a subfolder on github.io domain. Do it if you want to share your work with the rest of the world !

## How to add a new language ?

As web site content, simply create a new file in "/_data_languages" folder by copying an existing one or the template.

As web site language you can copy one file from "/_translated_texts" and translate it.

In the two cases you need a flag. Check if it's already available in "/images" folder or add a new one.

## Where is it used ?

This repository was done after creating three "learning resources" websites for [Delphi](https://developpeurpascal.github.io/Delphi-Learning-Resources/), [Lazarus](https://developpeurpascal.github.io/Lazarus-Learning-Resources/) and [Pascal language](https://developpeurpascal.github.io/Pascal-Learning-Resources/) because I think it's simple to personalize and easy to use.

## Translations

The original standard texts where translated from FR or EN to CN, DE, DK, HU, JP, PL, RU, SE, SP and TR with [Deepl](https://deepl.com) translation service.

## You are happy ? Tell it !

If you like this project and if you use it, tell it.

And if you can please thinks about sponsoring my activities on the web (see links on GitHub) and perhaps subscribing to my [Zone-Abo membership program](https://zone-abo.fr).

## You are not happy ? Tell it too !

You can contact me from one of my web site, [open a new discussion]({{ site.github.repository_url }}/discussions) or [create an issue]({{ site.github.issues_url }}) if you want to talk or report anything about this project.

## Support the project and its author

If you think this project is useful and want to support it, please make a donation to [its author](https://github.com/DeveloppeurPascal). It will help to maintain the code and binaries.

You can use one of those services :

* [GitHub Sponsors](https://github.com/sponsors/DeveloppeurPascal)
* [Liberapay](https://liberapay.com/PatrickPremartin)
* [Patreon](https://www.patreon.com/patrickpremartin)
* [Paypal](https://www.paypal.com/paypalme/patrickpremartin)

or if you speack french you can [subscribe to Zone Abo](https://zone-abo.fr/nos-abonnements.php) on a monthly or yearly basis and get a lot of resources as videos and articles.
