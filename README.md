# CDFPlugin-Manipulate
##### Made by Rob and Mason
Since the Mathematica CDF plugin is no longer supported, we have replicated the ability to move the camera around and zoom in on the output of Mathematica plots. Intended for use in CDF files, the Notebook, or a system such as U of I Courseware.

# Use It Now!
Copy the contents of one of the following into your Input Box. That's it - you're set!
  + **[Basic Manipulate](https://raw.githubusercontent.com/budak7273/CDFPlugin-Manipulate/master/Basic_Manipulate)**, which supports rotating around the z axis, raising and lowering the viewpoint, and zooming.
  + **[Mason Edition](https://raw.githubusercontent.com/budak7273/CDFPlugin-Manipulate/master/Mason_Edition)**, similar to Basic Manipulate but uses [Euler Angles](https://www.youtube.com/watch?v=zZM2uUkEoFw&list=PLW3Zl3wyJwWOpdhYedlD-yCB7WQoHf-My&index=13) to calculate the view position.
  + **[PitchZoom Manipulate](https://raw.githubusercontent.com/budak7273/CDFPlugin-Manipulate/master/PitchZoom_Manipulate)**, which all that Basic does plus view [pitching](https://goo.gl/sSxczV).

---
---

# 'Magic Numbers' Explanation
The viewpoint is based around CMView. The number 3.1384709652950433 is the radius of the circle in the XY plane centered at {0,0} that CMView ({2.7, 1.6, 1.2}) is located on. The preset rotation t value of 1.0358412530088001 is the t value on said circle that produces the point {2.7, 1.6}.

Both of these values were obtained via: 
```NSolve[{r Sin[t], r Cos[t]} == {2.7, 1.6}, {r, t}]```
Two sets of solutions exist, but we only care about the positive ones.

See it in action [here](https://www.desmos.com/calculator/w7vewp6w0f).


The initial value 0.47 of the zoom slider was determined through trial and error, checking what value looked 'close enough' to the zoom level that CMView positions the camera at.

# Learn More
These links may be helpful if you'd like to help develop the CDF plugin.
  + https://reference.wolfram.com/language/howto/RotateZoomAndPanGraphics.html
  + https://reference.wolfram.com/language/ref/ViewVector.html
  + https://reference.wolfram.com/language/ref/ViewPoint.html
  + https://reference.wolfram.com/language/ref/ViewAngle.html
  + https://reference.wolfram.com/language/ref/ViewVertical.html
