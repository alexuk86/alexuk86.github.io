---
layout: post
title: Field of View
---
One thing you might have noticed on the posts so far is the circular artifact which occurs towards the edge of all the reconstructions. The circle is the same diameter as the square of the reconstruction image. The reason this occurs is because as we approach the corners of the square, there is less and less data available. Only inside the central circle is where there is a consistant maxima of data with which to reconstuct the image<!--more-->

The area within the circle is considered to be the "Field of View", or FOV. Even if you're able to reconstuct data outside of the FOV, it won't be as accurate or reliable as what you can get within the FOV. Especially in medicine, the area outside of the FOV will be overwritten so the observer does not mistakenly rely on the image outside of the FOV. Generally a radiographer will try to avoid any part of the subject falling outside of the FOV.

Here you can see the FOV circle clearly on a FBP reconstruction:
![FOV circle on FBP][FBP]

A common feature of CT reconstruction algorithms is that they struggle with missing data. Algorithms that are tolerant to missing data do exist - often these are used to gain better quality images where high attenuation objects are within the reconstruction volume. This is very common on pelvis CT scans in medicine where the patient has had one or both hips replaced with artifical joints. Here are a few examples from Varian's pages on iterative reconstruction where metal artifacts exists:

![FBP, Iterative][varian]

It is possible to adapt both the filtered back-projection and iterative algorithms that we've seen before to do a better job in the corners of the reconstruction volume. The key is to know how much data is available for each pixel and apply a correction based on that, kind of accounting for the missing data.



[FBP]: https://catblo.gs/images/intro_FBP.png "Filtered Back-projection reconstruction"
[Phantom]: https://catblo.gs/images/intro_phantom.png "Original mathematical phantom"
[220th]: https://catblo.gs/images/iterative_220.png "220th Iteration"
[varian]: https://catblo.gs/images/HN2c.jpg "FBP CBCT, Iterative CBCT"