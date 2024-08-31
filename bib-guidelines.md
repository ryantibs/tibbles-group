# Bib Guidelines

These are a set of guidelines for the formatting in bib files, particularly
`general.bib` in the tibbles group repo.

## Journal papers

Journal papers are almost always BibTex type `@article`. The "must-have" fields
are `author`, `title`, `journal`, `number`, `pages`, `volume`, `year`. An
example entry is:
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
- BibDesk adds `date-added` and `date-modiied` fields; don't worry about it,
  they won't appear in the rendered bibliography. They also don't need to be
  there.
- 
unless it appears as a
paper published in a book, in which case it would be `@incollection` (pretty
rare). Guidelines
