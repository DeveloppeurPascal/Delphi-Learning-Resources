---
title: How to contribute to this project
lang: en
---
# Contributing

[This project]({{ site.github.repository_url }}) manages a dataset of website links classified in topics by languages.

The idea behind this project is to simplify discovering of websites in developers languages. Search engines have too many results and sometimes it's easier to see a directory of links and choose where to look at than surfing on search results.

English is not the only language for developers. It's time to proove it and help non english speaking people to learn and practice programming languages in their language. I know the irony of saying that in english. o:-)

If you want to help, you are free to translate this page as "CONTRIBUTING-xx.md" (with xx the ISO 2 letters language code of the translation) and submit a pull request.

## How to contribute

This project is open to pull requests for datasets (languages, topics, links), for flags images (only if you have rights on the pictures) and for web design (after discuting of the changes you wants to do or need).

If you use GitHub, fork the repository, do your updated in your copy and send a pull request.

Please do a COMMIT by change. Don't group thousends of changes in the same COMMIT, it would be too complex to verify links and allow/deny them.

## Manage the dataset (add, edit or remove links, topics, languages)

### Adding or editing website texts (language messages file and its translation)

You can translate (or edit translations) for standard messages from folder "/_translated_texts".

If you add a translation file, please check if a flag is available in "/images" and if not : add one or open an issue for it.

### Adding a new language resources

Copy an existing file from "/_data_languages" and edit it or copy the file "_template_files_for_data_collections/_data_languages-template.md" to "/_data_languages" folder and edit it.

Check if the flag for this language is already in "/images" folder. If not add one or open an issue for it.

Check if a texts file is available for this language in "/_translated_texts". If not, and if you can, translate one or open a new issue.

### Add or edit topics for a language

Use the template file "_template_files_for_data_collections/_data_topics-template.md" or copy an existing topic file in folder "/_data_topics".

## Properties of each data file

### Properties of a language

* lang: 2 letters language ISO code
* lang_name : the name of the language in the language ("english" for "en", "français" for "fr", "deutsch" for "de", ...)
* lang_flag: the file name of the flag. Typically the 2 letters ISO code and extension .gif, .JPG or .PNG depending on the available file "in /images".
* permalink: the webpage name for this language. Typically "index-XX.html" with XX as the 2 code letters for the langauge (same as "lang" property).
* title: the text used as page title. Make it as simple and short as possible. Of course in the good language.

After that you can write a description displayed in the language page. It's in markdown. You can use standard MD codes but don't do it too much.

Respect the rules : a language page is an access to topics where are the links. The description must be a global description of the website in the choosen language.

See "lang" as a primary key for languages. It must be unique or the generated website won't do what you expect.

### Properties for topics

* lang: 2 letters language ISO code
* family: the family name of the topic. See authorized values for family property bellow.
* topic_name: label of the topic, it's used as link in the navigation bar.
* title: the text used as page title. Make it as simple and short as possible. Of course in the good language.
* summary: one or two sentences to tell what the prupose of this topic.It will be display in topics list on language page.

After that you can write a description displayed in the link page. It's in markdown. You can use standard MD codes but don't do it too much.

Respect the rules : a topic page displays the links to website resources. Don't tell your life or an other story in the description, it's only to explain the topic and why those links are there.

The "lang" property is a link to a language page. A corresponding language must exists in "_data_languages" folder.

The "family" property is a link between topics in many languages but either a link between a topic (for a language) and links to show in its page.

See the couple lang/family as a primary key (unique) for topics. And the lang property as a foreign key from languages.

### Properties for links

* lang: 2 letters language ISO code
* family: the family name of the topic. See authorized values for family property bellow.
* title: the name of the website
* absolute_url: the absolute URL to the website (must start with http:// or https://)

And you have a description to tell what is this website and what users will see on it.

The couple "lang/family" must exists as a topic. If not this link will never be displayed.

By default the generated website has no page for each link. So the description is only available in links list on a topic page. Be simple and short, but not too short. One paragraph is good.

### The "family" property

This property is used to bind topics in different languages (when available) and to bind links to there topic.

For this purpose the family values can't be totally free. It must be the same in the same language for the same use even if topics have different "topic_name" or "title" properties depending on the language.

As family property value please use one of them :

* "official" : for official websites (like editor, distributor or documentation)
* "vod" : for YouTube, Vimeo or other video websites where people can look at videos on demand (for free or not, but tell it in the description)
* "learning" : for courses (text or videos), ... in self learning process
* "training" : for exercizes resources or websites where you can test things. Regular or permanent code challenges can be added there.
* "sample" : for website sample projects or reposiroties with many samples. Please don't link all GitHub projects about this technology, it's the role of "awesome" repositories. You can link repositories with a lot of samples used to learn things or to use as code snippets.
* "book" : for online or not books websites
* "community" : forums and websites where users help each others
* "usergroup" : users groups in real world (clubs and others)
* "job" : websites available to find job offers or freelance job targeting this technology (listing générics job site has no totaly interest)
* "blog" : links to RSS agregators and (maintained / live) blogs about this technology

If you see an other topic to use, please submit an issue or open a discussion.

## Web site and web design

If you want to change something to the web design of the generated website, please open an issue or a discussion before doing it.

If you have suggestions about accessibility for the generated website, please tell us by opening a discussion or an issue. And if you can't do that for any reason (GitHub is not totally accessible) and only in that case, [contact Patrick Prémartin](https://developpeur-pascal.fr/nous-contacter.php).
