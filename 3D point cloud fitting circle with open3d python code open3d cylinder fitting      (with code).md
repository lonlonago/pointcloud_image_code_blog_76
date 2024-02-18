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
