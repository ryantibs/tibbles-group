# tibbles-group

Resources for Ryan Tibshirani's research group.

## latex/

This subfolder has various latex files and templates. Main files: 

- `general.bib`: general-purpose bib file for papers.
- `macros.tex`: latex macros/style file papers. 
- `template.tex`: latex template for a paper. You can see how it utilizes
  `macros.tex` and `general.bib`.

Note: the bib file is maintained via [BibDesk](https://bibdesk.sourceforge.io),
a free excellent tool that I highly recommend. If you contribute a PR (always 
welcome, thank you!) to the bib file, then please pay attention to the
[bib guidelines](bib-guidelines.md). 
  
There is also a `template-talk.tex` file that I use for my talks.

## tools/

This subfolder has various command line (Mac/Linux) tools. Main files: 

- `mk-new`: make a new folder for a new project. First you need to create a
  folder, say `lentilfilter`, for our new amazing project on Lentil Filtering.
  Then you call: 
  ```
  mk-new lentilfilter
  ```
  You can see how it populates a directory structure and fills it with various
  templates, and tools. 
- `cp-bib`: replace the local `general.bib` file with the latest one from the
  git repo. Typically, to be called within the `notes` or `paper` subfolders of
  a given project folder. 
- `cp-arxiv`: copy all the paper files into an `arxiv` subfolder, and zip it
  (for easy submission to arxiv). To be called within the `paper` subfolder of a
  given project folder.

There are also some talk tools, `mk-talks` and `cp-talks`.
