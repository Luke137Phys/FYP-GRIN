
### What is a GRIN Lens?

> [!Definition]
> A GRIN lens is a lens where the refractive index changes with distance as light passes through the medium. "Eye lenses of all species, thus far, measured, are gradient index (GRIN) structures. The index gradation is one that increases from the periphery of the lens to its centre but the steepness of the gradient and the magnitudes of the refractive index vary so that the optics of the lens accords with visual demands." [[Pierscionek2012]]


### There are three main types of grin lens [[Pierscionek2012]]:

#### 1. Spherical Gradient:

- This is a perfect sphere with a spherically symmetric refractive index gradient.
- Decreases from the centre to the edge of the sphere
- Maxwell's Fisheye Lens is an example of one.
	- Limited by the application only to rays emanating from points on the lens surface.
- [Luneberg Lens](https://en.wikipedia.org/wiki/Luneburg_lens) is another example of one.
	- Capable of imaging objects beyond the lens surface
	- More simple equation and has the ability to focus parallel rays to a single point
- Spherical lenses have never been found in the eye of any species

Spherical GRIN Profile:
![[Spherical.jpg]]

#### 2. Radial Gradients

- In a radial gradient the refractive index distribution increases or decreases perpendicular to the optical axis
- The Wood lens is an example of this that [[Pierscionek2012]].
- Refractive power can be altered by varying lens thickness and [[aberrations]] can be controlled by altering the function of the index distribution

Radial GRIN Profile:
![[Radial.jpg]]

#### 3. Axial Gradient

- Here the refractive index varies as distance from a given plane
- Usually it is the plane which is orthogonal to the optical axis
- Thin-layered axial GRIN structures are designed to minimise reflections ad can reduce spherical aberration. 
- An axial GRIN medium does not have focusing properties.
	- This is instead determined by the lens surface
	[[Pierscionek2012]]

Axial GRIN Profile:
![[Axial.jpg]]

## Iso-indicial Contours:


> [!NOTE] Iso-indicial Contours Definition
> Iso-indicial contours break up a lens into concentric shells of varying refractive index. 
> 

The shells can be modelled using the order polynomial in the sagital direction:

$$n(z,r)=n_{00}+n_{01}z+n_{02}z^2+n_{10}r+n_{20}r^2\dots$$
where $r$ is radial distance from optical axis and $z$ is distance along the optical axis. [[Goncharov2007c]] . This is expanded upon in more detail in [[Maths of the lens]]
