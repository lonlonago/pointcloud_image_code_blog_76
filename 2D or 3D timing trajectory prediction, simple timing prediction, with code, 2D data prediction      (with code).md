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

