# exercise12
***
###Abstract
In this assignment, we are going to investigate the electric field problem. As is konwn to all, the field poccesses some basic qualities, the intensity and its potential. The electric intensity could be discribed as the gradient of the potential, which means it's a vector while the potential is a scalar. To enumerate the distribution of intensity and potential, we can take advantage of SOR method, Gauss-Sield method as well as some other methods.First, we will see some visualized model in 3d, then we will solve the prblems.
***
###Background
 ####Problem 5.8 
 > Extend out treatment of a point charge in a metal box to dela with the case in which the charge is located near one face of the box.Study how the equipotential contours are affected by the proximity of a grounded surface.
 ***
 
###Exercise
####Analysis

As is known to all, the electric potential obeys Laplace's equation:

<img src="http://latex.codecogs.com/gif.latex?\frac{\partial^{2}V}{\partial(x)^{2}}+\frac{\partial^{2}V}{\partial(y)^{2}}+\frac{\partial^{2}V}{\partial(z)^{2}}=0" alt="" title="" />

To enumarate the problem numerically, we can write the derivate with respect to x at the point(i,j,k) as:

<img src="http://latex.codecogs.com/gif.latex?\frac{\partial(V)}{\partial(x)}\approx\frac{V(i,j,k)-V(i-1,j,k)}{\Delta(x)}" alt="" title="" />

Thus, the potential could be written as:

V(i,j,k)=[V(i+1,j,k)+V(i-1,j,k)+V(i,j+1,k)+V(i,j-1,k)+V(i,j,k+1)+V(i,j,k-1)]/6

When there is an electron in the space, the former equation should add a term on the right side:<img src="http://latex.codecogs.com/gif.latex?\frac{\rho\Delata(x)^2}{6}" alt="" title="" />

To make our calculation more accurate, we can introduce the Laplace-calculate routine, which will judge the value of the sum of delta V, and if the variance is within the range that could be tolerated, we will accept the result, otherwise we will continue the calculating loop untill the former requisite is satisfied. The other way is Gaussian-Sield method, which uses alpha times delta V every time and make the consequence converge to the real value. The coefficient alpah will change in different conditions.

####Visualization
![img](https://github.com/LuxAsteria/test3/blob/master/screenshot_20161211_195118.png)


####Exercise

First, let's start with the simplest problem: the field of the capacitor.

![ing](https://github.com/LuxAsteria/test3/blob/master/capacity%20e.png)
![img](https://github.com/LuxAsteria/test3/blob/master/capacity%20v.png)
![img](https://github.com/LuxAsteria/test3/blob/master/capacity.png)

Second,the point electron.
Because the geometric size of the point is extremely small in 2d space, to avoid some infinite problems in calculation, we can assume that the point have a relatively tiny 'size'.

![img](https://github.com/LuxAsteria/test3/blob/master/2%20same%20point.png)
![img](https://github.com/LuxAsteria/test3/blob/master/3point%20e.png)
![img](https://github.com/LuxAsteria/test3/blob/master/point%20equal.png)


![img](https://github.com/LuxAsteria/test3/blob/master/point%202.png)
![img](https://github.com/LuxAsteria/test3/blob/master/point%20notequal.png)
![img](https://github.com/LuxAsteria/test3/blob/master/point3d%20equal.png)
![img](https://github.com/LuxAsteria/test3/blob/master/屏幕快照%202016-12-10%20下午4.02.20.png)
![img](https://github.com/LuxAsteria/test3/blob/master/屏幕快照%202016-12-11%20下午7.39.51.png)

 Third, when the point is near the face of box, we can see the potential field like this:
 
 ![img](https://github.com/LuxAsteria/test3/blob/master/屏幕快照%202016-12-11%20下午6.00.33.png)
 ![img](https://github.com/LuxAsteria/test3/blob/master/屏幕快照%202016-12-11%20下午7.16.07.png)
 
 From the rings we can see the contour in 3d
 ![img](https://github.com/LuxAsteria/test3/blob/master/屏幕快照%202016-12-11%20下午7.17.30.png)
 
 Contours in 2d

 ![img](https://github.com/LuxAsteria/test3/blob/master/屏幕快照%202016-12-11%20下午7.18.12.png)
 
 [FOR CODE PLEASE CLICK HERE](https://github.com/LuxAsteria/exercise12/blob/master/CODE)
 
 ***
 ###Conclusion
 In this assignment, we investigate the electronic potential field, and we see that the boundry will influence the field a lot. What's more, to calculate the point's intensity field, using the function 'gradient' will be more convinent and direct.
 
 ###Acknowledge
 
 [1]Computational Physics, Edition 2, Nicholas J.Giordano & Hisao Nakanishi
 
 
 ##PS:ALL RIGHTS RESERVED
 
 
