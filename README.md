# Slinky
Simulate the falling slinky problem with weight at the bottom.

This is a modified copy of https://vanderbei.princeton.edu/WebGL/Slinky.html. I have added a weight at the bottom of the slinky.

In this scientific paper the problem is explained, but without an aditional weight at the bottom: https://vanderbei.princeton.edu/tex/slinky/slinky.pdf

If you add a weight $ M $ at the bottom, instead of

$ y_{n − 1} (0) − y_n (0) = \frac{m g}{k} $

(page 3) you get this equation:

$ y_{n − 1} (0) − y_n (0) = (m + M) \frac{g}{k} $

If you solve the differential equation, $ b = \frac{m g}{2k} $ is the same, but $ a = - \frac{m g}{k} \left(\frac{M}{m} + n + \frac{1}{2} \right) $, There is an additional term $ \frac{M}{m} $, that is $0$ if $ M=0 $, so it is the same as in the paper.
The resulting equation describing the initial position of every element in equilibrium is:

$ y_j (0) = - \frac{m g}{k} \left(\frac{M}{m}  j + n * j - \frac{1}{2} j (j - 1) \right) $

In all following calculations you can increase the mass of the lowest element by $ M $.

You can try the simulation here: https://kr0k0bil.github.io/Slinky/