# Ray Tracing Methods Paper
Deaton et al. 2016-2017

### Overview
This paper presents a general relativistic ray tracing code useful for computing
neutrino distribution functions in a general hydrodynamical spacetime. The
gr-hydro code is SpEC, developed by Matt Duez, Francois Foucart, and others in
the SXS collaboration. The ray tracing code is a module within SpEC developed by
Andy Bohn (for gravitational lensing and event horizon finding in numerical
spacetimes) and Brett Deaton (using Andy's framework to find neutrino
trajectories).

The principle statements of the paper are:

1. Here's a new raytracing code for neutrino emission; here's where it's valid,
   here's where it sucks.
2. One application (presented here) is to estimate the power from neutrino
   annihilation around a post-merger accretion disk.

### Build Instructions
Compile the paper with the usual pdflatex sequence:
```
pdflatex paper.tex
bibtex paper
pdflatex paper.tex
pdflatex paper.tex
```
The `bibtex` and subsequent `pdflatex` calls are redundant if no new references
have been added between compiles.

### Text Guidelines
These guidelines establish conventions to improve the text of the article.
"Prefer to..." below means break the rule if it makes sense to.

* Prefer to write things in words not letters throughout: e.g. avoid "NSBH" or
  "MRI".
* Prefer to use "neutron star--black hole" to "black hole--neutron star"
  because this paper focuses on the matter.
* Prefer to use abbreviations like "Eqn." and "Fig." in the text.

### LaTeX Guidelines
These guidelines establish conventions to make it easier to read and write
the raw LaTeX in paper.tex.

* __Object labels__.
  Use four letters or fewer for the class (e.g. `sec`, `ssec`, `fig`, etc.),
  followed by a colon,
  followed by a shortish underscore separated name (e.g. `nu_energy_spectrum`).
  Example: `\label{fig:nu_energy_spectrum}`.
* __BibTeX keys__.
  The key format in references.bib is `<surname><year>-<unique>` where
  `<surname>` is the 1st four (or fewer) letters of the 1st author's surname,
  `<date>` is the four-digit year of publication, and
  `<unique>` is a unique specifier from the title journal or whatever.
  Example: `deat2013-leakage`.
