# CDFPlugin-Manipulate
Since the Mathematica CDF plugin is no longer supported, I have replicated some of the functionality in a Manipulate.


# 'Magic Numbers' Explanation
The viewpoint is based around CMView. The number 3.1384709652950433 is the radius of the circle in the XY plane centered at {0,0} that CMView ({2.7, 1.6, 1.2}) is located on. The preset rotation t value of 1.0358412530088001 is the t value on said circle that produces the point {2.7, 1.6}.

Both of these values were obtained via: 
```NSolve[{r Sin[t], r Cos[t]} == {2.7, 1.6}, {r, t}]```
Two sets of solutions exist, but we only care about the positive ones.

See it in action here:
https://www.desmos.com/calculator/w7vewp6w0f

The initial value 0.47 of the zoom slider was determined through trial and error, checking what value looked 'close enough' to the zoom level that CMView positions the camera at.
