The existing data are, t1, x1, y1, z1, t2, x2, y2, z2... 

 That is, the xyz coordinate corresponding to each timestamp, you need to predict its XYZ position in the next or next N timestamps 

 The predicted effect, red is the actual track point, blue is the predicted track point: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574687444
  ```  
 That is, the xyz coordinate corresponding to each timestamp, you need to predict its XYZ position in the next or next N timestamps 

  The actual idea and practice is very simple and crude, that is, to do one-dimensional linear interpolation, but instead of the commonly used interpolation, we use linear interpolation instead of quadratic or cubic interpolation because in the case of interpolation, the performance of the latter two is very poor, which is very different from the actual situation. We use timestamp as the x value and position value as the y value to fit three linear trajectories, and then interpolate. 

 The code is as follows: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574687444
  ```  
  The data file here is not given, you can use the above data saved as txt as an example; 

  Disadvantages: Because of linear interpolation, the prediction effect is better at the position of the straight line of the trajectory, but there will be a slight deviation from the actual next trajectory where the degree of bending is relatively large; 



--------------------------------------------------------------------------------

![avatar]( 40eb25a38c9349ff86c0c51abad5f3f8.png) 

 The circle fitting method can be divided into the following steps: 

 2.1 Fitting the plane by SVD 

 Suppose we want to find a plane that is as close as possible to a 3D point set, and the proximity is measured by the sum of squares of the orthogonal distances between the plane and the points. 

 2.2 Projecting points onto the fitting plane 

 We can use the Rodriguez rotation formula to project 3D points onto the fitted plane and obtain their 2D X-Y coordinates in the coordinate system of the plane. Note that we need to choose the axis of rotation k as the cross product between the plane normal and the normal of the new X-Y coordinates 

 2.3 Circle Fitting in Projected 2D Coordinates 

 Suppose we want to fit a circle to a point n. The two-dimensional implicit equation r for a circle of radius 

 We introduce the vector where c = (c0, c1, c2) for unknown parameters. Applied to all input points, it produces a system of linear equations 

 Since we have more equations than unknowns, we need to find an approximate solution by least squares to minimize the sum of squares of the residuals 

 The least squares method is already implemented in the package NumPy by a function we can call with the input data numpy.linalg.lstsq 

 If we need to weight the points, we can modify the input data W through the diagonal matrix. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574695775
  ```  


--------------------------------------------------------------------------------

Just change the launch file 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574630571
  ```  


--------------------------------------------------------------------------------

 Because I didn't see a Python version of the point cloud area growth code, I wrote one myself, and the effect is as follows: 

 ![avatar]( fd93de1123e74d82880396c8f7e1580c.png) 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574630636
  ```  


--------------------------------------------------------------------------------

The need to merge multiple point clouds often arises, and they can be merged directly.

 ![avatar]( eb4a1e4822254716a01f578f67e75a45.png) 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574679145
  ```  


--------------------------------------------------------------------------------

 Using the extend method, there are three possible ways to add one or more points to an existing point cloud.

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574670056
  ```  


--------------------------------------------------------------------------------

 We simulate the process of adding text, adding numbers to random 3D positions in the point cloud

 ![avatar]( 33119e8ef4cf41c2a5102e7df7c8ab36.png) 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574620989
  ```  


--------------------------------------------------------------------------------

As an amateur software developer, I have come up with another interesting little thing that is completely free to use. 

 It uses the existing deep learning network for audio recognition, and then packages it into a separate module. The way to use it is to download the software, and then open the folder where the audio is located. It will automatically scan the file at the end of the wav, mp3 suffix and perform the conversion. 

 ![avatar]( 3872912719f0b6a0dfd028a19a84dd51.png) 

 ​ 

 Download address: 

 Link: https://pan.baidu.com/s/1WQQ8kaDilaagjoK5IrYZzA 

 Extraction code: 1111 



--------------------------------------------------------------------------------

 As an amateur software developer, I have come up with another interesting little thing that is completely free to use. 

 It uses the deep learning network of the existing audio TTS, and then encapsulates it into a separate module. The way to use it is to download the software, and then open the folder where the txt text is located. It will automatically scan the text file at the end of the txt suffix and perform the conversion wav. 

 The disadvantage of the software is that it is relatively large, because the models are placed locally, so there is no need to go to the Internet to call the model interfaces of major Internet companies, but if your computer is running slowly, it may not be suitable for use. 

 Download address: 

 Link: https://pan.baidu.com/s/1WQQ8kaDilaagjoK5IrYZzA 

 Extraction code: 1111 



--------------------------------------------------------------------------------

 Implements a code that relies entirely on C++ parsing LVX data, is not complicated, and does not rely on any other libraries including the official SDK. 

 And use timestamp as the intensity value, so it looks like the color will be different from normal; 

 ![avatar]( 4c887fb2711c4f1e8fce268f88c2f744.png) 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574617933
  ```  


--------------------------------------------------------------------------------

 Use the following formula to calculate the average curvature

E=1+(Fx**2/Fz**2)

F=Fx*Fy/Fz**2

G=1+(Fy**2/Fz**2)

L=(1/(Fz**2*grad_F))*det([Fxx,Fxz,Fx],[Fxz、Fzz、Fz]、[Fx、Fz,0])

M=(1/(Fz**2*grad_F))*det(([Fxy,Fyz,Fy],[Fxz,Fzz,Fz],[F x,Fz,0])

N = (1 / (Fz * * 2 * degree _ F)) * det ([Fyy, Fyz, Fy], [Fyx, Fzz, Fz], [Fly, Fz, 0])

A=（[L，M]，[M，N]）

B=（[E，F]，[F，G]）

B_inv=逆（B）

k_values = eigenvalues (points (B_inv, A))

By B_inv * A (the dot product of two matrices), k1 and k2.

Finally, calculate the average curvature of the points:

Average curvature = (k1 + k2)/2 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574610736
  ```  


--------------------------------------------------------------------------------

Start by finding the Gaussian curvature of the point by finding the equation of the best-fitting surface

The equation is created from the surrounding points and is formatted as follows:

a*x**2+b*y**2+c*z**2+d*x*y+e*y*z+f*x*z+g*x+h*y+i*z+j=0

(a,b,c,d,e,f,g,h,i,j)

Next, the point closest to the current point of interest is found on the surface of the best fit. Then

The program finds the first and second partial derivatives of the equation with respect to x, y, and z

Layer of the equation. The coordinates of the nearest point are used to calculate the values of x, y, and z in this table,

Then the program calculates the Gaussian curvature using the following formula:

E=1+(Fx**2/Fz**2)

F=Fx*Fy/Fz**2

G=1+(Fy**2/Fz**2)

L=(1/(Fz**2*grad_F))*det([Fxx,Fxz,Fx],[Fxz,Fzz,Fz],[Fx,Fz,0]))

M=(1/(Fz**2*grad_F))*det(([Fxy,Fyz,Fy],[Fxz,Fzz,Fz],[Fx,Fz,0]))

N=(1/(Fz**2*grad_F))*det(([Fyy,Fyz,Fy],[Fyz,Fzz,Fz],[Fy,Fz,0]))

A=（[L，M]，[M，N]）

B=（[E，F]，[F，G]）

B_inv=逆（B）

k_values = eigenvalues (points (B_inv, A))

Where Fx is the first-order derivative of the function with respect to x, and Fy is the first-order differential of the function

With respect to y, Fz is the first derivative of the function with respect to z, and Fxx is the second derivative of the function

B_inv the eigenvalues of * A (dot product of two matrices), k1 and k2.

Finally, calculate the Gaussian curvature of the point:

Gaussian curvature = k1 * k2

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574691685
  ```  


--------------------------------------------------------------------------------

 Calculate the local maximum z-directional difference for each point in a given 3D point

Start looking for the maximum height difference of a point by looking up the z-coordinate of each point in "pts"

Then find the minimum and maximum values in these coordinates. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574644121
  ```  


--------------------------------------------------------------------------------

Calculate the maximum and minimum values of each axis range for all point clouds of X, Y, and Z.

After using 2 methods, you can get the final desired value 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574620249
  ```  


--------------------------------------------------------------------------------

Calculate the layer for each point

Start looking up the layers of points by looking up normal vectors and points on the surface

The plane of best fit for the point and surrounding points. Normalize the normal vector and then calculate the slope in the specified direction

If the "axisxyz" input is "z", the z coordinate of the normal is checked. If the value is negative, the entire

Multiply the normal vector by -1 to make the z coordinate positive. Then calculate the slope by the following formula:

Slope = sqrt (x ** 2 + y ** 2)

If the "axisxyz" input is "x", the x coordinate of the normal is checked. If the value is negative, the entire

Multiply the normal vector by -1 to make the x-coordinate positive. Then calculate the slope by the following formula:

Slope = sqrt (y ** 2 + z ** 2)

If the "axisxyz" input is "y", the y coordinate of the normal is checked. If the value is negative, the entire

Multiply the normal vector by -1 to make the y-coordinate positive. Then calculate the slope by the following formula:

Slope = sqrt (x ** 2 + z ** 2)

If "axisxyz" is not entered as "x", "y", or "z", the function throws the exception "axisxyz must be x, y, or z".

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957468290
  ```  


--------------------------------------------------------------------------------

Calculate the plane fitted by N points around a point, and then calculate the distance from that point to this plane as the roughness of that point.

The average roughness at each point is the overall roughness of the point cloud

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574618420
  ```  


--------------------------------------------------------------------------------

Used to calculate the verticality of each point

This function obtains the verticality by finding the surrounding points and then finding the angle between this normal and the positive z-axis.

The z component of the normal vector must be positive, so if it is negative, multiply by -1 to ensure that the resulting ratio is positive.

The program uses the following formula:

= arccos [（ xa * xb + ya * yb + za * zb ） / (√ （ xa ^ 2 + ya ^ 2 + za ^ 2 ） * √ ） xb ^ 2 + yb ^ 2 + zb ^ 2 ）]

Where (xa, ya, za) = (the x, y, and z components of the normal vector) and (xb, yb, zb) = (0, 0, 1) (the vector of the z axis).

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574687704
  ```  


--------------------------------------------------------------------------------

 For each point, the distance to its nearest point is calculated.

From this, we can determine the average distance between all the points in the cloud.

From this average distance, it can be used to estimate the radius parameters of some other algorithms, the distance parameters,

For example, the field distance parameter of normal vector calculation, the distance threshold parameter of the distance.

In addition, different sampling devices and different distance from the scene will cause differences in point cloud density.

Most of the existing methods for estimating point cloud density are based on distance.

The average distance density representation based on distance is calculated by calculating the average distance of each point in the point cloud

To estimate the density of point cloud distribution. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574658748
  ```  


--------------------------------------------------------------------------------

When drawing a point cloud, color is used to represent its height.

We first calculated the height range of the point cloud, and then mapped the color of each point according to the height

 Modifying the code slightly, we can also make the height color gradual change to the X-wheelbase color gradual change:

 ![avatar]( 7c5c5a84a8014d3da74ac42fb5d1eb26.png) 

 Modifying the code slightly, we can also make the height color gradual change to the X-wheelbase color gradual change:

 ![avatar]( 484f6a5ee1a0499abac0e58884e44811.png) 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574611448
  ```  


--------------------------------------------------------------------------------

WeChat 394467238 

 The previous article tried to write a way to remove watermarks from images, but later found that there were still some problems when processing videos. 

 The article link is: lonlon ago: Python code for video dewatermarking 

 The method of this article is to get the watermark mask first, and then randomly select nearby points to replace the points inside the mask. The problem is that some parts will appear white noise-like areas, so I have tried some other methods later. This article compares the effect of these methods. 

 1 randomly select nearby points to replace the watermark 

 2 OpenCV inpaint method 

 3 randomly select nearby areas to replace the watermark 

 4 Replace the watermark by interpolation 

 5 Black Box Magic 

 The original image is as follows: 

 ![avatar]( e117934d86d378112fee9ed660430f98.png) 

 The multiple synthesized mask images are as follows, and so far this step has been very successful: 

 ![avatar]( 6012a29cc70b82dca595e1b18f7e4d5c.png) 

 For areas with poor magnification, the watermark in the red box is replaced with a point like white noise, losing the outline of the object: 

 ![avatar]( 1d4d1f138f784ecdb238d9747559e1c5.png) 

 2. The effect of OpenCV's inpaint method is that the watermark part becomes transparent as a whole, but the watermark traces can still be seen: 

 ![avatar]( 1ff1885d4892f6d168bb62091599c1d3.png) 

 Zoom in to see the effect: 

 ![avatar]( 2cbe76e5c6815fb61c8f8ee081b64e9b.png) 

 3. The method of randomly selecting nearby areas to replace the watermark, the initial idea is that random points will cause the same effect as white noise, and there is no outline, so randomly selecting areas to replace should be better, but in fact the effect is not good, there is another problem, there will be a mosaic-like effect: 

 Zoom in to see the areas that are not working well: 

 ![avatar]( 86d172bd128d0f7714d7d59a4c457ddc.png) 

 4. By interpolating and replacing the watermark, in theory, the result he obtained should be the smoothest and most ideal, but in fact it is not satisfactory 

 Zoom in to see the effect, it feels like a watermark that has been evenly smeared, and the effect is not good. The problem may be that the interpolation range is too large, resulting in the inability to perform effective interpolation: 

 ![avatar]( 17f1d4d53295446cc6a615aa4efc8051.png) 

 5. Black box magic, the effect is perfect. Try it above. 

 It's okay to zoom in. 

 ![avatar]( 0617b86d90a6911b08abeae7fb09e6cb.png) 



--------------------------------------------------------------------------------

