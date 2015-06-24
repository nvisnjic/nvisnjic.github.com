---
title: "GSOC Week 4"
description: "2D correction works like a charm, forward to 3D and other nice dimensions"
layout: post
tags: beaglebone, linux, SPI, gsoc2015
category: BeagleSat 
comments: no
---

Week four is upon us, more stuff has been done, more stuff to be done.
Finished the 2D correction algorithm in MATLAB, [more about that here](http://nvisnjic.com/2015/06/24/2d-correction-in-action.html).

*Worked on:*

* 2D Correction algorithm in MATLAB, works like a charm
* Parameter estimator is very fast locally, will be porting to Octave to test execution speed on the BeagleBone
* Parameter estimation on simulated data yields less than 1% error on all
  deformations except rotation (rotation is variable in error, but less 
  than 2%)


*Issues:*

* Research was helpful, but the algorithm part could have been a bit more elaborate
* Octave was super uncooperative with the symbolic toolbox, have to look i
into that and move the MATLAB code to Octave (go team open-source!)
* Sensor testing complexity still unknown (last week's issue), will be testing in the coming weeks


*To be worked on:*

* Expanding the 2D correction algorithm to a 3-axis one
* Adding time-variant error compensation using telemetry and additional inputs
* Currently using SPIDEV for the data readouts, transfer to proper drivers later in the project



