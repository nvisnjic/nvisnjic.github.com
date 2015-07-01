---
title: "GSOC Week 5"
description: "Improved 2D correction and hit a bump with 3D fitting. Apparently, MATLAB isn't happy with solving a 9 unknowns 9 non-linear equation system symbolically."
layout: post
tags: beaglebone, linux, SPI, gsoc2015
category: BeagleSat 
comments: no
---

Midterm checkpoint on Friday. Finished checking the 2D fitting and got halfway
through with 3D fitting. Unfortunately, it seems that a (realistically to long)
set of non-linear equations that need to be solved symbolically to compute the
conversion factors is to big of a bite for MATLAB to chew in any reasonable
amount of time. Until I figure out a solution to the solver, [alternatives](http://www.mathworks.com/matlabcentral/fileexchange/24693-ellipsoid-fit) are being researched.

*Worked on:*

* 2D Correction algorithm in MATLAB, scales properly now for different field
  magnitude measures
* Moved both to Octave so I can test on the BBB 
* 2D Octave code is quite fast on BeagleBone (~0.022s for 500 point dataset)
* 3D Octave code working, adapted from Yury's fitting algorithm (~ 0.081s for
  512 point dataset)
* Fitting code: [https://github.com/nvisnjic/BeagleSat](https://github.com/nvisnjic/BeagleSat)

*Issues:*

* Haven't figure out yet how to get rotational matrix from the eigenvector
  output, scaling and centering works fine
* Solving the non-linear equations to convert from intermediate linear terms to
  correction parameters (rot, trans, scale) for the data proved to be
  impossible/takes too long; used Yury's method for now


*To be worked on:*

* Solving parameter EQs with a different method
* Figure out the eigenvector rotation matrix
* Adding time-variant error compensation using telemetry and additional inputs
* Testing on real measurements (2D case ready; 3D should work as well) 
* Framework design \& overall systems design
