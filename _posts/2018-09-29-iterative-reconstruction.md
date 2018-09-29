---
layout: post
title: Iterative Reconstruction
---
Reconstruction of CT images is a process to *approximate* a solution to the problem. Back-projection and Filtered back-projection (FBP) are methods which do fairly well at low computational cost. Technically there is an ideal solution - the best that can be done with the data available; by looking at the problem as an enormous mass of simultaneous equations you reach the *ideal* solution ... at great computational cost. <!--more-->

Iterative reconstruction is that middle ground method. It's actually not just one method, but a few different variations. It allows greater image quality to be extracted from the same data when compared to FBP. It deals with certain types of lack of data well in general - as a result it is commonly used in the real world to reduce X-ray dose.

