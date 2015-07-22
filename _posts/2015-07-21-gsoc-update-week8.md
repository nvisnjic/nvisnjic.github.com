---
title: "GSOC Week 8"
description: "Got some basic API code in, also an input-output Linux loadable kernel module (LKM) for testing. Floating point stuff in the LKM module not there yet."
layout: post
tags: beaglebone, linux, SPI, gsoc2015
category: BeagleSat 
comments: no
---

Finally got some code up on GitHub, set up the proper Makefile structure
to make building Doxygen documentation as easy as invoking "make doxy".
Next stop, expanding the API header to some real-life usable code.
Added a LKM module to start testing sysfs interfacing next week.

*Worked on*

* API code, more to come
* Uploaded a basic input-output Linux kernel module, works fine for ints, have to fix cflags to get floating point in the code

*Issues:*

* Had trouble compiling floating point into kernel code. Tried -mhard-float got "gcc: error: -msoft-float and -mhard_float may not be used together", tried more focused flags, and compiled a program that optimizes out sscanf()'s format to a static string. GCC not being nice.
* Solving the non-linear equations is currently on hold; Mathematica is a
  possible solution (working on it!)

*To be worked on:*

* (Much) more work on the API, got to fix stuff
* Fix the floating point thing in the LKM
* Improve LKM processing stage; add an interrupt driven processing step, with an extra enable sysfs flag or something similar 
* Overall systems design (and put it on a graph?)
* Figure out the eigenvector rotation matrix
