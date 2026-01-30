 The [[# Differential Equations#Paraxial Differential Equation|Paraxial Differential Equation]] can be solved using the Frobenius method to get the infinite sum solution:
 $$h(z)=\sum_{m=0}^\infty a_mz^m + \sum_{m=0}^\infty b_mz^{m+1}$$
	
Using this in the paraxial region with $h_0=0.0001$ and  $u_0=0$ the following values for EFL and BFD are found:

$$EFL= 12.9885,$$
$$BFD=15.7942.$$
### Hyperbolic Lens

In order for a hyperbolic lens to work need a GRIN equation for the posterior and anterior region. The anterior will take the form:

$$n_a(z,h) = n_0 - n_1h^2 + n_3z + n_4z^2$$
This will create two hyperbolic profiles with two roots at $h=0$ of $z=0$ and $z=-4$ . By taking away  $8$ (twice the separation between the two hyperbolas) and swapping the signs of $n_1$ and $n_4$, an equation can be found for the posterior region:

$$n_p(z,h)=n_0 + n1h^2=n_3(z-8)-n_4(z-8)^2$$
These two lenses can then be ray traced through separately. The initial conditions for the anterior region are:

$$h_{0_a}=h_0=0.0001$$ and $$u_{0_a}=h'_0=0$$ For the posterior region we get:
$$h_{0_p}=h_a(4)$$
and 
$$u_{0_p}=h'(4)$$
The initial conditions for the posterior region are the "exit conditions" for the anterior region.