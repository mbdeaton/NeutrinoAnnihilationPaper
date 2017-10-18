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
2. One application (presented here) is to measure neutrino fluxes and spectra
   around a post-merger accretion disk.

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

* Use abstract tensor notation, no bold or bbold for vectors.
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

### PRD Guidelines
These guidelines help us conform to the Physical Review D editorial rules.

* __Figures__.
  Provide figures in eps and pdf form, since PRD prefers ps which pdflatex
  can't easily handle. Convert with epstopdf.

* __Figures__.
  For Latex typesetting in gnuplot, use the following sequence of commands
  ```
  gnuplot> set term epslatex color size 4in,2.8in;
  gnuplot> set output 'fig.tex';
  ```
  generating two files `fig.eps` and `fig.tex`; convert to pdf using
  `epstopdf fig.eps`. Then insert into paper using
  ```
  \begin{figure}
    \resizebox{\columnwidth}{!}{\input{fig.tex}}
    \caption{This is a figure about things.}
  \end{figure}
  ```

* __Figures__.
  Get a good font size in gnuplot terminal epslatex by setting the plot size as
  above, and using the default 11pt. You'll also shift labels in gnuplot:
  ```
  gnuplot> set xlabel 'x' offset 0,0.5
  gnuplot> set ylabel 'y' offset 1.5,0
  ```
  A good example is in plot-avg_eps_vs_cosA.gnu.

* __Figures__.
  Describe the location of the data and the plotting scripts for each figure
  in nearby latex comments.

### Reviews
There are some internal and external reviews of the paper in ../PaperReviews.
