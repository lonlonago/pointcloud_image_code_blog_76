Used to calculate the verticality of each point

This function obtains the verticality by finding the surrounding points and then finding the angle between this normal and the positive z-axis.

The z component of the normal vector must be positive, so if it is negative, multiply by -1 to ensure that the resulting ratio is positive.

The program uses the following formula:

= arccos [（ xa * xb + ya * yb + za * zb ） / (√ （ xa ^ 2 + ya ^ 2 + za ^ 2 ） * √ ） xb ^ 2 + yb ^ 2 + zb ^ 2 ）]

Where (xa, ya, za) = (the x, y, and z components of the normal vector) and (xb, yb, zb) = (0, 0, 1) (the vector of the z axis).

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574687704
  ```  
