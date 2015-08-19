---
title: "GSOC Week 12"
description: "A working Python example (almost) complete"
layout: post
tags: beaglebone, linux, SPI, gsoc2015
category: BeagleSat 
comments: no
---

Found an adequate solution to the solver using Python. The inspiration came
from a
[blogpost](http://www.varesano.net/blog/fabio/ellipsoid-sphere-optimization-using-numpy-and-linalg) 
for a similar ellipsoid fitting optimization. It's gonna need a bit of fixing
to work more like the Octave setup I have now, but that shouldn't be a problem.

Next up, write ALL the documentation!

*Worked on*

* Found a proper solution to the ellipsoid fitting in Python.
* Needs a bit of fixing, but will be up and running in a couple of hours.
* Plotting the fitted data in a nice example program.


*Issues:*

* Good news, I found out what's happening under the hood in the eig() function
  in MATLAB. Partially bad news, it's pre-compiled FORTRAN.
* Since Python's NumPy library uses the same solver underneath, will just go
  with that for now.
* Well, 48 hours a day would be nice, but probably still not enough.

*To be worked on:*

* Patch up the solver, and integrate it into the code.
* Split it up into a proper Python package.
* Document everything! 
