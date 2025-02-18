---
title: Better BibTeX for Zotero
weight: 5
aliases:
  - /Home
---
<!-- WARNING: GENERATED FROM https://github.com/retorquere/zotero-better-bibtex/blob/master/README.md. EDITS WILL BE OVERWRITTEN -->

# Better BibTeX for Zotero



Better BibTeX (BBT) is an extension for [Zotero](https://www.zotero.org) and [Juris-M](https://juris-m.github.io) that makes it easier to manage bibliographic data, especially for people authoring documents using text-based toolchains (e.g. based on [LaTeX](https://www.latex-project.org) / [Markdown](https://www.markdownguide.org)).

## Features

### Facilities for generating citation keys
* Stable [citation keys]({{< ref "retorque.re" >}}), without key clashes! Generates citation keys that take into account other existing keys in your library
  that are not part of the items you export. Prevent random breakage!
* Set your own, fixated [citation keys]({{< ref "retorque.re" >}}), generate citation keys from [JabRef patterns](https://help.jabref.org/en/BibtexKeyPatterns), drag and drop LaTeX citations, add other custom BibLaTeX fields.

### Conversion between formats and encodings
* Zotero does all its work in UTF-8 Unicode, which is absolutely the right thing to do. Unfortunately, for those shackled
to BibTeX and who cannot (yet) move to BibLaTeX, unicode is a major PITA. Also, Zotero supports some simple HTML markup
in your references that Bib(La)TeX won't understand.

* BBT will convert from/to HTML/LaTeX:

  - `<i>...</i>`&#8660;`\emph{...}`/`\textit{...}`
  - `<b>...</b>`&#8660;`\textbf{...}`
  - `<sup>...</sup>`&#8660;`\_{...}` and `<sub>...</sub>`&#8660;`^{...}`. 
  
  More can be added on request.
  
  BBT contains a comprehensive list of LaTeX constructs, so stuff like `\"{o}` or `\"o` will be converted to their unicode equivalents on import (e.g., `\"{o}` to `ö`), and their unicode equivalents back to `\"{o}` if you have that option enabled (but you don't have to if you use BibLaTeX, which has fairly good Unicode support).
  
  If you need literal LaTeX in your export: surround it with `<script>`...`</script>` (or `<pre>`...`</pre>`, which do the same) markers.
  
### Facilities for exporting data from Zotero
* Highly [customized exports]({{< ref "retorque.re" >}}).
* Fixes date field exports: export dates like 'forthcoming' as 'forthcoming' instead of empty, but normalize valid dates
  to unambiguous international format.
* [Auto export]({{< ref "retorque.re" >}}) of collections or entire libraries when they change.
* [Pull export]({{< ref "retorque.re" >}}) from the embedded webserver.
* Automatic [journal abbreviation]({{< ref "retorque.re" >}}).

## Getting started
To get started, read the [installation instructions]({{< ref "retorque.re" >}}).

## How does it work ?
At its core, BBT behaves like any Zotero import/export module; anywhere you can export or import bibliography items in Zotero,
you'll find *Better X* listed among the choices.  

If nothing else, you could keep your existing workflow as-is, and just enjoy the improved LaTeX &harr; unicode translation on import and export and more accurate field mapping.

Better BibTeX works from [BibTeXing](http://ctan.cs.uu.nl/biblio/bibtex/base/btxdoc.pdf) and [Tame the
BeaST](http://www.lsv.ens-cachan.fr/~markey/BibTeX/doc/ttb_en.pdf) for BibTeX, and
[The Biblatex Package](http://mirrors.ctan.org/macros/latex/contrib/biblatex/doc/biblatex.pdf) for BibLaTeX, but
since there isn't really a definitive manual for either format that is universally followed by Bib(La)TeX
editors/processors, I'm pragmatic about implementing what works.

## Got problems? We got fixes!

If you have any questions on BBT's use, do not hesitate to [file a GitHub issue](https://github.com/retorquere/zotero-better-bibtex/issues/new) and ask for help. 

If you're reporting a bug in BBT, please take a moment to glance through the [support request guidelines]({{< ref "retorque.re" >}}); it will make sure I get your problem fixed as quick as possible.
Clear bug reports commonly have really short time-to-fix, so if you report something, stick around -- it may be done as you wait.

The support request guidelines are very detailed, perhaps to the point of being off-putting, but please do not fret; these guidelines simply express my ideal bug submission.
I of course prefer very clearly documented issue reports over fuzzy ones, but I prefer fuzzy ones over missed ones.

## Sponsoring BBT

While the development needs of BBT are to a large extent covered
by the generosity towards open-source developers of services such
as github and travis, my development system does require the
occasional upgrade; also, I enjoy getting the occasional frivolous
tech-toy that I wouldn't otherwise grant myself. While you should
feel in no way obligated to pay for BBT, [anything you can spare](https://www.paypal.me/retorquere) is very much appreciated.
If you'd rather contribute a little bit each month (and a little
means a lot) so I can save up for a replacement a year or so down
the line, head on over to [Patreon](https://www.patreon.com/retorquere),
but mind that Patreon takes a fairly large cut of what you give.

Many, many thanks, also to the existing contributors -- thanks to you I've hit my first target and have been able to replace my trusty macbook air with a newer macbook pro which has much more breathing room.

