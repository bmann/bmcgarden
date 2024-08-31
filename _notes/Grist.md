---
tags:
  - opensource
  - app
  - spreadsheet
  - python
github: https://github.com/gristlabs/grist-core/
---
Open source, Apache licensed cloud spreadsheet. Not quite an Airtable clone, but similar capabilities. Some of the layout and linking makes it feel like Filemaker.

> Grist is a modern relational spreadsheet. It combines the flexibility of a spreadsheet with the robustness of a database.

Grist is a hybrid database/spreadsheet, meaning that:

- Columns work like they do in databases: they are named, and they hold one kind of data.
- Columns can be filled by formula, spreadsheet-style, with automatic updates when referenced cells change.

There is a [user-created packaging of Grist](https://git.cloudron.io/walski/grist-app) for [[Cloudron]].

## Grist essentials

1. **Relational database** that’s easy to create and use by non-technical people.
2. **Data/view** separation, for app-like functionality, easy to set up and use by non-technical people.
3. Sharing and **access controls** that allow users to address complex real-world access requirements.
4. **Open source**, for transparency and trust in the software’s promises, and freedom for technical users to improve it. [Read more](https://www.getgrist.com/blog/grist-a-hacker-friendly-spreadsheet/) on this.
5. Options to run **self-managed**, or on the desktop; reliance on a service provider is optional.
6. Support for spreadsheet-like **formulas**, to extend use cases and empower users.
7. Extensibility via **APIs** and other integration points.
8. Data is **portable**, allowing lossless export in a well-supported format, and common export/import options.
9. Comprehensive **documentation** and learning materials.
10. **High quality** implementation, well-tested, with a focus on reliability and performance.

## Python and Excel Formulas

From the [function reference](https://support.getgrist.com/functions/):

> Grist formulas support most Excel functions, as well as the Python programming language.
> 
> The table below lists Grist-specific functions, and the suite of the included Excel-like functions. In addition, the entire [Python standard library](https://docs.python.org/3/library/) is available. For more about using formulas in Grist, see [Intro to Formulas](https://support.getgrist.com/formulas/).
> 
> [Grist uses Python (version 3.11)](https://support.getgrist.com/python/) for formulas. You can use nearly all features of Python (see [Python documentation](https://docs.python.org/3.11/)).

Also a new [AI Formula assistant](https://support.getgrist.com/ai-assistant/).
## Grist Labs

From Github README:

> The `grist-core` repo is the heart of Grist, including the hosted services offered by [Grist Labs](https://getgrist.com/), an NYC-based company 🇺🇸 and Grist's main developer. The French government agency [ANCT Données et Territoires](https://donnees.incubateur.anct.gouv.fr/toolbox/grist) 🇫🇷 has also made significant contributions to the codebase.

I've captured more on the [[Grist Labs]] -- a very inspiring team / company. They

