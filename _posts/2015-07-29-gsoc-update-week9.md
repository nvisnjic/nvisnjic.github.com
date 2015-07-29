---
title: "GSOC Week 9"
description: "C is the key, but Python is quicker."
layout: post
tags: beaglebone, linux, SPI, gsoc2015
category: BeagleSat 
comments: no
---

Last week's discussion left an impression that things weren't going fast
enough while tackling the API, LKM and all other parts of the project at once.
After talking to my mentors, we decided for a quicker approach to the
development cycle and that means switching to a faster animal, or should I say
snake. 

C is the end goal for stability and portability, but for the prototyping
phase Python is king.

*Worked on*

* Transferring stuff to Python
* Wrote a PyBBIO library to communicate with the MPU9250 ->
  [code](https://github.com/nvisnjic/PyBBIO/blob/master/bbio/libraries/MPU9250/MPU9250.py)
* Noticed [a second
  library](https://github.com/richards-tech/RTIMULib/tree/master/RTEllipsoidFit) 
  is using the same data correction (based on Yury's, but without the time
  variant part) as I do, going to be looking into the code over the next week

*Issues:*

* The AK8963 magnetometer sandwiched with the MPU9250 was a royal PITA to 
 interface with via SPI (but it works now!), -1 for elaborate datasheets missing important info
* Solver for the equations? (Candidate solutions: Mathematica, 
expand on Yury's work, or something third)

*To be worked on:*

* Add self-test functions to the MPU9250 library and other corrections 
so it fits nicely with PyBBIO
* Transfer API for data processing control
* Solve the solver and connect to data input in Python
