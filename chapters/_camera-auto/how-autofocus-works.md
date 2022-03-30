---
title: How Autofocus Works
---
There are two major kinds of autofocus technology in cameras today: Autofocus that works with dedicated focus sensors, found in DSLR's, and autofocus that works on the image sensor data, found in Mirrorless and compact cameras.

Before autofocus, one would use a "[rangefinder](https://en.wikipedia.org/wiki/Rangefinder_camera)" to measure subject distance and focus accordingly.

## Image Sensor Autofocus
At the highest level of overview, the goal of focus is pretty simple: Maximize the color difference in nearby pixels. An out-of-focus image will have adjacent pixels be closer to being the same color than an in-focus image. Perhaps you average the value-difference between all adjacent pixels across the entire image. The camera then calculates some score for the image (call it "contrasty-ness", "detail-level", "sharpness", or what-have-you). Now it can rate any single image with this score. Now, a search: Rack the focus of the camera, and calculate the score. Find what we may remember from algebra is a "local maximum" - in both directions, we have a worse score.

In reality, this is a primitive implementation. We probably only want to look at certain areas of the total image, we don't want to assume that our subject is static, and our "focus-score" algorithm can certainly be improved.

So what can we learn about this? It implies some drawbacks.
- It takes processing power to calculate focus quickly
- The camera's image sensor must be on (and using battery power)
- The lens has to search for focus by testing - adjusting the lens
- It will not be able to get focus of a scene with no contrast, like a blank wall
- It will not be able to get focus as well with an underexposed or overexposed image
- It is measured "through the lens" and 
## DSLR Autofocus
Most DSLR's use a more advanced form of autofocus. The mirror that bounces light up to the viewfinder is actually not entirely opaque. It is a tiny bit transparent. Some light can go right through the mirror, where another mirror bounces it down the bottom of the camera. Here, there exist 'Phase-Detection' sensors, which can detect the focus of the light.

### Phase Detection?
The

### Other Methods?
Other autofocus techniques include Canon's [Dual Pixel Autofocus](https://www.usa.canon.com/internet/portal/us/home/learn/education/topics/article/2018/July/Intro-to-Dual-Pixel-Autofocus-(DPAF)/Intro-to-Dual-Pixel-Autofocus-(DPAF)).
