# Bib Guidelines

These are a set of guidelines for the formatting in bib files, particularly
`general.bib` in the tibbles group repo. These are not "official" in any way, 
they're just my opinion and how I like to maintain the bib files.

General note: for my cite keys, regardless of the type of entry (journal paper,
conference paper, etc.) I always use:

```
{author-last-name}{year}{title-first-word}
```

I maintain my bib files with [BibDesk](https://bibdesk.sourceforge.io), which is
a free excellent tool that I highly recommend. 

## Journal papers

Journal papers are BibTex type `@article`. The standard "must-have" fields are:
`author`, `title`, `journal`, `number`, `pages`, `volume`, `year`. An example
entry is: 

```
@article{schwarz1978estimating, 
	author = {Gideon Schwarz},
	title = {Estimating the dimension of a model},
	date-added = {2024-07-06 12:10:02 +0200},
	date-modified = {2024-07-06 12:10:52 +0200},
	journal = {Annals of Statistics},
	number = {2},
	pages = {461--464},
	volume = {6},
	year = {1978}}
```

Notes:

- I often go to great lengths trying to find an author's first name. Don't
  settle for `G. Schwartz`. Sometimes you will hit a dead end. It's ok. 
- Middle initials can be used in place of middle names (just do this based on
  whether they're used in the publication itself). Always use a period: `Ryan
  J. Tibshirani`, and not `Ryan J Tibshirani`.
- Personal note: please always use my middle initial, helps distinguish from 
  that other Tibshirani. 
- The `title` field will be usually translated into "initial caps" style (only
  the first letter will be capitalized). Make sure to use braces to force
  capitalization when you need it, as in `A high-dimensional test for
  {Gaussianity}`.
- The `journal` field will usually be preserved as-is in terms of
  capitalization. Make sure to use "title caps" style for this field, as in
  `Annals of Statistics`.
- Sometimes journals won't have volumes; just omit the `volume` field.
- Make sure to use two dashes for the page range, as in `461--464`.
- BibDesk adds `date-added` and `date-modiied` fields; don't worry about it,
  they won't appear in the rendered bibliography.
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
`title`, `publisher`, `year`. 

```
@book{hastie2009elements,
	author = {Hastie, Trevor and Tibshirani, Robert and Friedman, Jerome},
	date-modified = {2023-12-12 19:12:48 -0800},
	edition = {second},
	publisher = {Springer},
	title = {The Elements of Statistical Learning: Data Mining, Inference and Prediction},
	year = 2009}
```

Notes:
- The paper title goes in `title` and the conference name goes in `booktitle`.
- The style for the conference name is a bit tricky/ambiguous, but here's what I
  use, for consistency:
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
- Because this is a book, include the `publisher` field. Always try to include
  `pages` if you can find the page range.
- You don't need anything else; for example, I don't include editors' names in 
  the`editor`field. 
