### GRIN Lens:

GRIN lenses are modelled using a higher order polynomial in distance from surface along the optical axis, $z$ and height above the optical axis and with GRIN coefficients $n_i$. [[Goncharov2007]]

$$n(z,h)=n_0+n_1h^2+n_2h^4+n_3z+n_4z^2+n_5z^3+n_6z^4$$
This can be simplified to a quadratic equation by setting some of the GRIN coefficients to zero:

$$n(z,h)=n_0+n_1h^2+n_3z+n_4z^2$$
#### Symmetric vs Asymmetric:

For a symmetric lens, only this equation is needed and setting $n_1=n_4$. This will increase to a maximum value, $n_{max}$ at the centre of the lens with a minimum value of $n_0$ at each outer surface. [[Flynn2024]]

For an asymmetric lens, two equations are needed. One for the anterior and one for the posterior:

$$n_a(z,h)=n_0-n1h^2+n_3z-n_4z^2$$
$$n_p(z,h)=n_{max}-n_1h+n_{3,2}z-n_{4,2}z^2$$
The first equation will increase from the minimum of $n_0$ until it reaches a maximum of $n_{max}$ while the second equation will decrease from the maximum of $n_{max}$ until it reaches a minimum at the boundary of $n_0$. [[Goncharov2007]]

#### Lens Shape and the GRIN Coefficients:

You can determine many of the characteristics of the lens using the GRIN equations above. The radii of iso-indicial contours can be determined using the above equations and the following "sag" equation:

$$h^2=2R(z)z-(1-k)z^2$$
where $R(z)$ is the radius of curvature of the lens surface and $k$ is the conic constant. Letting $n(z.h)=n_0$ and rearranging the GRIN equation gives:

$$h^2=\frac{n_3}{n_1}z-\frac{n_4}{n_1}z^2$$

Equating this to the above equation gives values for the radius of curvature and conic constant in terms of the GRIN coefficients:

$$R=\frac{n_3}{2n_1}$$
$$k=\frac{n_4}{n_1}-1$$

By adjusting the values of the GRIN coefficients the shape of the lens can be changed from spherical to elliptical to hyperbolic.

By taking the derivative of the GRIN equations with respect to $z$ and equating them to 0 the position and value of $n_{max}$ can be solved for.

$$\frac{\partial n(z,h)}{\partial z}=n_3-2n_4z=0$$

This is called the **Peak Plane**. This is the "midpoint" of the GRIN lens. It can determined from this that the length of the paraxial region is between $z=0$ and $z=\frac{n_3}{n_4}$. 

The maximum refractive index along the OA is located at $z=\frac{n_3}{2n_4}$. This can be used in the derived equation for $n_{max}$ to achieve:
$$n_{max}=n_0+n_3\left(\frac{n_3}{2n_4}\right)+n_4\left(\frac{n_3}{2n_4}\right)^2$$
$$\therefore n_{max}=n_0+\frac{n_3^2}{4n_4}$$
### Ray Tracing:

Ray tracing through GRIN media can be done in a few ways. It can be done in a continuous or discrete manner.

#### Paraxial Ray Tracing Equation:

In the paraxial region of the lens (very close to the OA), a differential equation can be derived from the standard "Paraxial Ray Tracing Equations". from geometric optics **[Add Citation Here]** These equations are given as:

$$n_{j+1}u_{j+1}=n_ju_j-h_jF_j$$
$$F_j= \frac{n_{j+1}-n_j}{R_j}$$
$$h_{j+1}=h_j+d_{j+1}u_{j+1}$$

where $n_j$ is the refractive index of the $jth$ contour, $u_j$ is the angle of the incident light to the OA after passing through the $jth$ contour, $h_j$ is the height of the ray from the OA as it passes through the $jth$ contour, $F_j$ is the power of the $jth$ contour, $R_j$ is the radius of curvature of the $jth$ contour and $d_j$ is the distance along the OA of the $jth$ contour. 

These equations can be combined, manipulated and reduce to achieve:

$$n\frac{d^2h}{dz^2}+\frac{dn}{dz}\frac{dh}{dz}+2n_1h=0$$
This can be solved numerically using software such as Zemax, or analytically. A semi-analytic solution to this can be found using Legendre polynomial and the refractive index profile for a GRIN lens giving:

$$h(z)=C_1P_{\frac{\sqrt{8n_1+n_4}-\sqrt{n_4}}{2\sqrt{n_4}}}\left(\frac{2n_4z-n_3}{\sqrt{-4n_1n_4h_0^2+n^2_3+4n_0n_4}}\right)+C_2Q_{\frac{\sqrt{8n_1+n_4}-\sqrt{n_4}}{2\sqrt{n_4}}}\left(\frac{2n_4z-n_3}{\sqrt{-4n_1n_4h_0^2+n^2_3+4n_0n_4}}\right)$$
This can be used for analytically ray tracing through GRIN media, which achieves a more accurate answer than when solving numerically. [[Flynn2024]]

#### Non-paraxial ray tracing equation:

A differential equation was derived by [[Flynn2024]] for ray tracing in the non-paraxial region of the lens.

By representing the path light takes as:

$$ds^2=dh^2+dz^2$$

and rearranging to get:

$$ds=\sqrt{1+(h'(z))^2}dz$$

This derivation starts from Fermat's principle:

$$\int nds=0$$
and ends up getting a differential equation from the Euler-Lagrange equations that can be reduced using a Taylor expansion to get:

$$\frac{nh''}{1+\frac{1}{2}(h')^2}+n'h'+2n_1h=0$$

This can also be solved both numerically and analytically. A semi-analytic solution can be found using the Frobenius method to give:

$$h(z)=\sum^\infty_{m=0}a_mz^m+\sum^\infty_{m=0}b_mz^m$$

where $a_m,b_m$ are Frobenius coefficients.

#### Solutions for Elliptic Lenses:

These methods were tested in [[Flynn2024]] on a quadratic GRIN lens with identical values for $n_0$ and $n_{max}$. The lens had the same semi-diameter as a spherical lens but half the thickness. This made it elliptical. This allows for testing of the lens for different conic constants. By manipulating the GRIN coefficients with the following formulas, the desired lens can be achieved:

$$d=\frac{n_3}{n_4}$$
$$D=\sqrt{\frac{n_3^2}{n_1n_4}}$$
$$n_{max}=n_0+\frac{n_3^2}{4n_4}$$

where $d$ is the lens thickness along the OA and $D$ is the diameter (height) of the lens. $D$ can also be called the aperture.

### EFL and BFD

**DERIVATION TO FOLLOW**

The EFL can be calculated using:

$$EFL=-\frac{h_0}{n_0h'(c)},$$
where $h_0$ is the intitial ray height, $n_0$ is the surface refractive index, $h'=\frac{\text{d}h}{\text{d}z}$ and $c$ is the exit position of the ray along the $z$ axis.

In the paraxial region, $c=d$, the thickness of the lens. 

In general at the surface using:

$$n_0=n_0-n_1h^2(z)+n_3z-n_4z^2$$
we get that:

$$h^2(z)=\frac{n_3z-n_4z^2}{n_1}$$
so:

$$h(z)=\sqrt{\frac{n_3z-n_4z^2}{n_1}}$$
Is the height of the ray at the surface. Solving this will give two roots, the larger of which is $c$.

Calculating BFD

Outside of the paraxial:
$$c=\Delta-d$$
For $\Delta$ asmall deviation along $z$. In a quadratic lens:
$$d=\frac{n3}{n4}$$

