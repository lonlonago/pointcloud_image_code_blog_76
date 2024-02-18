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
