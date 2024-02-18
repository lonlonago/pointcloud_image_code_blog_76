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
