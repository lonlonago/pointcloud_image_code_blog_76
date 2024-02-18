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
