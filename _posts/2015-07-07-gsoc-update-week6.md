---
title: "GSOC Week 6"
description: "Moved on to requirements and API design. Linux kernel modules are fascinating and (not very) hard."
layout: post
tags: beaglebone, linux, SPI, gsoc2015
category: BeagleSat 
comments: no
---

While I thinker with a solution to my [last week's equation
problem](http://nvisnjic.com/2015/06/30/gsoc-update-week5.html), I started
working on the API design and how to put all the work in a Linux Kernel module.
After failing miserably at my first attempt, I revisited my bookmarked library
and found this [brilliant guide](
http://derekmolloy.ie/kernel-gpio-programming-buttons-and-leds/) to LKMs on the BeagleBone Black. 

Now I just have to go from a piece of paper with my requirements to some runnable kernel code.

*Worked on*

* Educating myself on sysfs and Linux Kernel Module programming
* Requirements and API design (and still working on it)


*Issues:*

* Tried writing an overall design and it wasn't looking quite good, went back to read a bit on sysfs and LKMs 
* Yury's method works extremely well; still have to figure out how to get a
  rotation matrix from eigenvector output
* Solving the non-linear equations is currently on hold; Mathematica is a
  possible solution


*To be worked on:*

* Write API header from requirements
* Overall systems design (and put it on a graph)
* Choose a sysfs structure, start writing the kernel module
* Figure out the eigenvector rotation matrix
