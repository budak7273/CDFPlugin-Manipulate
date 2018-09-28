# CDFPlugin-Manipulate
Since the Mathematica CDF plugin is no longer supported, I have replicated some of the functionality in a Manipulate.


# 'Magic Numbers' Explanation
The viewpoint is based around CMView. The number 3.1384709652950433 is the radius of the circle centered at {0,0} that CMView is located on. Obtainted via: 
```NSolve[{r Sin[t], r Cos[t]} == {2.7, 1.6}, {r, t}]```
See it in action here:
https://www.desmos.com/calculator/w7vewp6w0f
