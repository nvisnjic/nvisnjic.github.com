---
title: "GSOC Week 3"
description: "Data collection working, onwards to the correction algorithm!"
layout: post
tags: beaglebone, linux, SPI, gsoc2015
category: BeagleSat 
comments: no
---

Week three of the GSoC 2015 BeagleSat project, a future CubeSat
development platform.


*Worked on:*

* Video is up! --> [https://youtu.be/ojDqtxv9oGY](https://youtu.be/ojDqtxv9oGY)
* Website just about done. -->
  [http://nvisnjic.com/beaglesat](/beaglesat)
* Got both sensors working and polling data into files (testing only)
* Started with Octave code for parameter estimator


*Issues:*

* Soon to begin testing data in Octave. A possible issue
  is that the data should come from rotating the sensor around a stable axis,
  which would require building an apparatus to hold the sensors while rotating
  in a stable
  orbit. If it turns out to be a blocker, I'll look into 3D printing such a
  device and rigging it to the BeagleBone
* Last weeks ML library issue should be a non issue, I'll use a matrix computation library when porting the code to C++, it should suffice


*To be worked on:*

* Currently using SPIDEV for the data, transfer to drivers later in the project
* More Octave stuff in the coming week
* Hackaday.io page soon


