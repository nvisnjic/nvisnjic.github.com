---
title: "GSOC Week 11"
description: "A commit a day makes (almost) all bugs go away"
layout: post
tags: beaglebone, linux, SPI, gsoc2015
category: BeagleSat 
comments: no
---

The Python API got it's basic structure and will be nearing completion 
before the weekend, the PyBBIO library driver for MPU9250 is 
feature-complete and ready for integration into PyBBIO.
Next steps, integrate the solver and start documenting everything everywhere!

*Worked on*

* The MPU9250 driver is completed and documented, ready for general usage, [code available here](https://github.com/nvisnjic/PyBBIO/blob/master/bbio/libraries/MPU9250/MPU9250.py) 
* Added all the bells and whistles needed for the MPU9250 to work like a charm
* Python API structure is set up, now to finish the helper functions


*Issues:*

* A bug with the MPU9250 occurs only on full register reset, tried getting to
  the bottom of it but to no avail. It doesn't influence the current code 
  functionality though, will work on that one after GSoC.
* Solver for the equations? Working on that this week and integrating into Python code

*To be worked on:*

* Finish the Python API
* Integrate solver into Python, either via NumPy or through Matlab code (other suggestions?)
* Documentation and examples
