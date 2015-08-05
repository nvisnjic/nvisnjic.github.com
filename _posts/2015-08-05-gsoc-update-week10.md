---
title: "GSOC Week "
description: "Note to self: Documentation is *super* important!"
layout: post
tags: beaglebone, linux, SPI, gsoc2015
category: BeagleSat 
comments: no
---

Last week was an interesting roller-coaster of reading documentation on and 
around the InvenSense MPU9250 9DOF sensor to patch up the PyBBIO driver to be
fully featured. It's practically there, but the documentation was less than
helpful. Onwards to the Python API. 

*Worked on*

* Transferring stuff to Python
* Added last couple of functions needed for a full featured MPU9250 PyBBIO library [code here](https://github.com/nvisnjic/PyBBIO/blob/master/bbio/libraries/MPU9250/MPU9250.py) 
* Self-test works good, range setup and magnetometer all green
* Gyro and accelerometer calibration has some issues still
* Noticed the on-board AK8963 can work at 100Hz (!!!) without an issue


*Issues:*

* Also noticed the InvenSense documentation is beyond horrible 
* Solver for the equations? Still need a fix

*To be worked on:*

* Patch up the remaining bugs in the MPU9250 library
* Python API
* Implement solver and connect to data input in Python
