---
title: "GSOC Final update"
description: "GSoC has come to an end, BeagleSat carries on"
layout: post
tags: beaglebone, linux,  gsoc2015
category: BeagleSat 
comments: no
---

Google Summer of Code comes to an end. 

Let's make a rundown of what has been done and what lies ahead.

The BeagleSat project has set out with the goal of simplifying 
[small satellite construction](https://en.wikipedia.org/wiki/CubeSat) 
to a level that is approachable 
by anyone willing to hack together a compact embedded system.
Be they academics or aspiring high schoolers, students or teachers,
the goal is to make something as complicated as satellite design available
to individuals or groups willing to invest the time to build them.
Leveraging open-software and open-hardware to make this process affordable and reproducible for people around the world.

The platform is here to provide a basic set of tools and functions to 
facilitate this process. Based on work from NASA, ESA and a multitude of
researchers to develop state of the art tools, for the best price there is.
[Free as in Speech](https://en.wikipedia.org/wiki/Gratis_versus_libre#Beer).


During this GSoC we've been focusing on the first phase of the project,
that is, developing the tools needed to get clean magnetic measurements 
from a compact satellite without the local interference usually 
accompanying such cost saving designs, developing software to interface 
with magnetometers and IMUs and building an API for easy access to 
functions developed in this design.
A big part of phase one was completed, but there is still a lot to be done 
going forward.


What has been accomplished during this Google Summer of Code:

* Researching and testing data fitting algorithms in MATLAB/Octave and
  demonstrating that they can run in real-time on the BeagleBone Black
* Developing a feature complete software set to interface with the MPU9250 sensor using the PyBBIO library in Python
* Converting the time invariant fitting algorithm to Python and optimizing
  execution time using the linalg package
* Making a BeagleSat API Python package to lower the barrier for accessing
  tools in the PyBBIO and data fitting sub-modules
* Testing and documenting examples for processing data in all stages of the
  acquisition/processing/storing pipeline
* Data visualizer for user feedback during data collection and correction


Items to be completed after Google Summer of Code:

* Test code for the time invariant algorithm in Python
* Continue development on the Linux kernel module and move processing into C 
* Test all fitting algorithms in a magnetically controlled environment and
  simplify further testing
* Expand the BeagleSat API and documentation as needed

All these items will be done in the near future, before moving on to phases two and three. 
That's the summary, though keep a close eye on the [project GitHub page](https://github.com/nvisnjic/BeagleSat/)

My biggest thanks go to my mentors, Steve Arnold, for giving me an extremely challenging project to tackle during this summer (and beyond), and Alexander Hiam, for keeping me running straight when focus was needed, and to both of them for bearing with me when commits were slow.
Many thanks to all the swell members of the BeagleBoard community for their
much appreciated help and support.
Finally, a big thank you to BeagleBoard.org and Google for sponsoring this amazing Summer of Code.


While it was an astonishing program, through which 3 months of coding have passed by faster then a summer breeze, the BeagleSat project that was started during these eleven weeks has a long and probably bright future ahead.


Cheers, 

Niko


