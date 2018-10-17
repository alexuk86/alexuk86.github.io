---
layout: post
title: Priori Information
---
An interesting little querk of iterative reconstruction is that it can be fed other data to start with. This is called *priori* data, and is essentially an estimate to begin calculating with. Iterative reconstruction will happily take a blank array as it's starting point, but depending on the step size of the iterations it might take quite some time to converge.<!--more-->

I usually describe filtered back-projection (FBP) as the *"quick and dirty"* method of reconstruction. It can actually be a fairly good estimate of the ideal reconstruction, depending on the circumstances. Regardless of the circumstances FBP is an excellent starting point for iterative reconstruction.

One of the down sides of iterative reconstruction is that it can take a great many iterations to produce a very sharp image, if it is starting from scratch. FBP, on the other hand, produces very sharp images in one iteration, although often with some level of artifact. 

For a practical example, this image was produced in 50 iterations starting from a FBP reconstruction. It is broadly of a similar image quality to the second image which is after 220 iterations starting from a blank slate. Priori information using complimentary reconstruction techniques can help to generate a faster reconstruction which displays the best of both techniques.

![50th Priori Iteration][priori50th] ![220th Iteration from scratch][200th]

For reference, here is the original mathematical phantom and the starting FBP image:

![Mathematical Phantom][Phantom] ![FBP Priori data][FBP]

[FBP]: https://catblo.gs/images/intro_FBP.png "Filtered Back-projection reconstruction"
[Phantom]: https://catblo.gs/images/intro_phantom.png "Original mathematical phantom"
[220th]: https://catblo.gs/images/iterative_220.png "220th Iteration"
[priori200th]: https://catblo.gs/images/priori_200.png "200th Iteration with priori data"
[priori50th]: https://catblo.gs/images/priori_50.png "50th Iteration with priori data"