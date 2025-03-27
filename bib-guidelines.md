# Bib Guidelines

These are a set of guidelines for the formatting in bib files, particularly
`general.bib` in the tibbles group repo. These are not "official rules" in any
way, they're just my opinion and how I like to maintain the bib files. The
general rationale is that these are supposed to represent balance between
something that is simple and easy to maintain, and close to traditional
conventions. 

General note: for my cite keys, regardless of the type of entry (journal paper,
conference paper, etc.) I use the following structure:

```
(author-last-name)(year)(title-first-word)
```

as in `tibshirani2012degrees`. I maintain my bib files with
[BibDesk](https://bibdesk.sourceforge.io), which is a free excellent tool that I 
highly recommend. 

## Journal papers

Journal papers are BibTex type `@article`. The standard "must-have" fields are:
`author`, `title`, `journal`, `number`, `pages`, `volume`, `year`. An example
entry is: 

```
@article{schwarz1978estimating, 
  author = {Gideon Schwarz},
  title = {Estimating the dimension of a model},
  journal = {Annals of Statistics},
  number = {2},
  pages = {461--464},
  volume = {6}, 
  date-added = {2024-07-06 12:10:02 +0200},
  date-modified = {2024-07-06 12:10:52 +0200},
  year = {1978}}
```

Notes:

- I often go to great lengths trying to find an author's first name. Don't
  settle for `G. Schwartz`. Sometimes you will hit a dead end, it's ok! (I have 
  had to give up a few times with older Russian papers ...)
- Middle initials can be used in place of middle names (just do this based on
  whether they're used in the publication itself). Use a period: `Ryan
  J. Tibshirani`, and not `Ryan J Tibshirani`. 
- *Personal note: please always use my middle initial, helps distinguish from
  that other Tibshirani!* 
- The `title` field will be usually translated into "initial caps" style (only
  the first letter will be capitalized). Make sure to use braces to force
  capitalization when you need it, as in `A high-dimensional test for
  {Gaussianity}`.
- The `journal` field will usually be preserved as-is in terms of
  capitalization. Make sure to use "title caps" style for this field, as in
  `Annals of Statistics`.
- Sometimes journals won't have volumes; just omit the `volume` field.
- Make sure to use two dashes for the page range, as in `461--464`.
- BibDesk often adds `date-added` and `date-modiied` fields; don't worry about
  it, they won't appear in the rendered bibliography.
- You don't need anything else; for example, I never include `publisher` or 
  `abstract` or anything like that.
  
## Conference papers

Conference papers are BibTex type `@article`. The standard "must-have" fields
are fewer: `author`, `title`, `booktitle`, `year`. An example entry is: 

```
@inproceedings{vu2013fantope,
  author = {Vincent Q. Vu and Juhee Cho and Jing Lei and Karl Rohe},
  title = {Fantope projection and selection: {A} near-optimal convex relaxation of sparse {PCA}}, 
  booktitle = {Advances in Neural Information Processing Systems},
  year = {2013}}
```

Notes:
- The paper title goes in `title` and the conference name goes in `booktitle`.
- The `booktitle` field is usually preserved as-is in terms of capitalization;
  make sure to use "title caps". The actual name to use is a bit
  tricky/ambiguous, but here's what I use, for consistency: 
    * NeurIPS: `Advances in Neural Information Processing Systems`.
    * ICML: `Proceedings of the International Conference on Machine Learning`.
    * AISTATS: `Proceedings of the International Conference on Artificial
      Intelligence and Statistics`.
  And so on. Basically, the default is to prepend "Proceedings of " unless the
  conference specifically has some different way of suggesting formatting as
  part of its own bib examples or documentation, like NeurIPS. I never use the
  number (volume) of the conference in the name; as in "Proceedings of the 
  Thirteenth ...".
- You don't need anything else; for example, I never include `volume` or `pages` 
  or `publisher` or `editors`. Keep it simple! (Virtually all of these
  conference proceedings are nicely-catalogued and available for free online so
  the paper name and year is enough for people to find it.) 

## Books

Books are BibTex type `@book`. The standard "must-have" fields are: `author`,
`title`, `publisher`, `year`. Here's an example: 

```
@book{hastie2009elements,
  author = {Hastie, Trevor and Tibshirani, Robert and Friedman, Jerome}, 
  title = {The Elements of Statistical Learning: Data Mining, Inference and Prediction},
  edition = {second},
  publisher = {Springer},
  year = {2009}}
```

Notes:
- The book title goes in `title`. This field is field is usually preserved as-is
  in terms of capitalization; make sure to use "title caps".
- You can include `edition` if the book you're referencing is not the first
  edition. Beyond that, you don't need anything else, like `address` or anything
  like that. Keep it simple!

## Papers appearing in a book or special collection

Papers appearing as part of a book or special collection are BibTex type
`@incollection` (pretty rare). The standard "must-have" fields are `author`,
`title`, `booktitle`, `publisher`, `pages`, `year`. Here's an example: 

```
@incollection{duchon1977splines,
  author = {Duchon, Jean}, 
  title = {Splines minimizing rotation-invariant semi-norms in {Sobolev} spaces},
  booktitle = {Constructive Theory of Functions of Several Variables}, 
  publisher = {Springer},
  pages = {85--100},
  year = {1977}}
```

Notes:
- The paper title goes in `title` and the book title goes in `booktitle`.
- Because this is a book, include the `publisher` field. Try to include `pages`
  if you can find the page range. 
- You don't need anything else; for example, I don't include editors' names in 
  the`editor`field. Keep it simple!
  
## Unpublished papers

Papers that are unpublished (typically on arXiv) are BibTex type `@unpublished`.
The standard "must-have" fields are `author`, `title`, `note`, `year`. Here's an
example:

```
@unpublished{montanari2023sampling,
  author = {Andrea Montanari}, 
  title = {Sampling, diffusions, and stochastic localization},
  note = {arXiv: 2305.10690},
  year = {2023}}
```

Notes:
- Everything as usual, and the `note` field refers to where you can find it. For
  arXiv papers, I just put the identifier (same with bioRxiv, medRxiv, HAL, and
  so on). 

## Miscellaneous tips

When the `title` is converted to "initial caps" style, you may have to force
capitalization for certain words using curly braces. What appears in between
curly braces is printed verbatim---all capitalization is preserved. For example: 

```
@article{ball1993reverse,
  author = {Keith Ball},
  journal = {Discrete \& Computational Geometry},
  number = {4},
  pages = {411--420},
  title = {The reverse isoperimetric problem for {Gaussian} measure},
  volume = {10},
  year = {1993}}
```

As a general rule, I also capitalize the first word after a colon in a title
(since this part effectively acts as a subtitle), as in:

```
@article{hoerl1970ridge,
  author = {Arthur Hoerl and Robert Kennard},
  journal = {Technometrics},
  number = {1},
  pages = {55--67},
  title = {Ridge regression: {Biased} estimation for nonorthogonal problems},
  volume = {12},
  year = {1970}}
```
