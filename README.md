# NeutrinoAnnihilationPaper
Deaton et al. 2015

This paper uses a general relativistic ray tracing code to examine the neutrino
annihilation mechanism as an energy source for the relativistic jet linking
a short gamma ray burst to its central engine. We will examine one or a few
specific gr-hydro models of nuclear accretion disks formed from the debris of a
neutron star merger. The gr-hydro code is SpEC, developed by Matt Duez, Francois
Foucart, and others in the SXS collaboration. The ray tracing code is a module
within SpEC developed by Andy Bohn (for gravitational lensing and event horizon
finding in numerical spacetimes) and Brett Deaton (using Andy's framework
to find neutrino trajectories).

The principle statements of the paper are (or in the case of #2, may be):

1. Here's a new raytracing code for neutrino emission; here's where it's valid,
   here's where it sucks.
2. The trend in the literature is that neutrino annihilation is insufficient to
   power the most luminous short gamma ray burst jets. But in some high mass disk
   cases, for example this M14_6-S9 merger, it is amply luminous at early times.
