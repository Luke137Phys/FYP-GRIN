A differential equation was derived describing the path of light in a medium with varying refractive index in both the paraxial and non-paraxial regions. [[Flynn2024]]

Due to the continuous nature of the quadratic GRIN profile, a differential equation is more suitable for ray tracing light as it passes through the GRIN media. The [[Paraxial Ray Tracing Equations]] can be used to form a differential equation to track the change in height within a medium with varying refractive index. It was shown that an increased number of iso-indicial contours leads to higher accuracy in ray tracing [[Liu2005]] . For this reason a continuous model for a GRIN lens is much better.

### Paraxial Differential Equation:

$$nh''+n'h'+2n_1h=0$$
where $n=n(z)$ is the refractive index at a point $z$ from the surface of the lens, $h=h(z)$ is the height from the optical axis and $n_1$ is the first GRIN coefficient.

This is a form of the ray equation in the paraxial region.

### Non-Paraxial Differential Equation:
$$\frac{nh''}{1+\frac{1}{2}(h')^2}+n'h'+2n_1h=0$$
In the paraxial region, $h\approx0$ so the fractional term goes away, leading back to the Paraxial Differential Equation.

##### Derivation of Non-Paraxial Equation:

Path light takes (simply Pythagoras' Theorem in 3D):
$$(ds)^2=(dx)^2+(dy)^2+(dz)^2$$
Set $dx=0$ and let $y=h(z)$ then:
$$(ds)^2=(dh)^2+(dz)^2$$
$$\Rightarrow \frac{(ds)^2}{(dz)^2}=1+\frac{(dh)^2}{(dz)^2}$$
$$\frac{ds}{dz}=\sqrt{1+ \left( \frac{dh}{dz}\right)}$$
with $\frac{dh}{dz}=h'(z)$ so that:

$$ds=\sqrt{1+(h')^2}dz$$
Multiply both sides by $n$ and integrate to get Fermat's principle on the left side:
$$\int_P^Qnds=\int_{z_P}^{z_Q}n(z,h)\sqrt{1+(h')^2}dz$$
where $z_P$ and $z_Q$ are the $z$ coordinates at points $P$ and $Q$.

Using Fermat's Principle, the integrand on the right:
$$f(z,h,h')=n(z,h)\sqrt{1+(h')^2}$$
can be used with the Euler equation:
$$\frac{d}{dz}(f_{h'})=f_{h}$$
here, $f_x$ denotes $\frac{df}{dx}$, such that the above can be expressed as:
$$\frac{d}{dz}\left(\frac{df}{dh'}\right)=\frac{df}{dh}$$
Calculating each part, use chain rule to get:
$$f_{h'}=\frac{nh'}{\sqrt{1+(h')^2}}$$
so:
$$\frac{d}{dz}f_{h'}=\frac{nh''}{\sqrt{1+(h')^2}}-n'$$
And again to get:
$$f_h=\frac{dn}{dh}\frac{ds}{dz}$$
Combining these to get:
$$\frac{nh''}{\sqrt{1+(h')^2}}+n'h'-n'=0$$
Using a Taylor series, this can be reduced to get:
$$\frac{nh''}{1+\frac{1}{2}(h')^2}+n'h'+2n_1h=0$$
This is the final form of the Non-Paraxial Equation.
[^1]: [[Flynn2024]]
