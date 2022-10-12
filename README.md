# tibbles-group

Resources for Ryan Tibshirani's research group.

## latex/

This subfolder has various latex files and templates. Main files: 

- `ryantibs.bib`: bibliography for all Ryan's papers.
- `ryantibs.tex`: latex style file for Ryan's papers. 
- `template.tex`: latex template for a paper. You can see how it utilizes
  `ryantibs.tex` and `ryantibs.bib`.

Note: the bib file is maintained via [BibDesk](https://bibdesk.sourceforge.io),
a free excellent tool that I highly recommend. If you contribute a PR (always 
welcome, thank you!) to the bib file, then please pay attention to the
[bib guidelines](). 
  
There is also a `template-talk.tex` file for Ryan's talks.

## tools/

This subfolder has various command line (Mac/Linux) tools. Main files: 

- `mk-new`: make a new folder for a new project. To be called as in:
  ```
  mk-new lentilfilter
  ```
  for our new amazing project on Lentil Filtering. You can see how it populates
  a directory structure and fills it with various templates, and tools. 
- `cp-bib`: grab the latest bib file from this git repo. Typically, to be called
  within the `notes` of `paper` subfolders of a given project folder. 
- `cp-arxiv`: copy all the paper files into an `arxiv` subfolder, and zip it
  (for easy submission to arxiv). To be called within the `paper` subfolder of a
  given project folder.

There are also some talk tools, `mk-talks` and `cp-talks`.
