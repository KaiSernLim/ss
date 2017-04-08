### CS 184: Computer Graphics and Imaging, Spring 2017
# Final Project Proposal: Subsurface Scattering
## by Kai-Sern Lim and Juchan Kim

## Description
In class, we implemented the BRDF which is a simplification of the BSSRDF. A BRDF is an approximation of the BSSRDF by assuming that the incident illumination is uniform. So for a BRDF, we assume that light scatters equally in all directions when reflecting off an object's surface. In the real world, not all materials reflect light in this matter. Some materials like human skin absorb some of the light which is emitted from another location on the object, which is called translucence. 

The goal of this project is to extend the raytracer to be able to handle BSSRDF light scattering so we can render more detailed objects. Many interesting looking materials have translucent properties and we want to render materials that have such properties, such as milk and marble.

## Goals

Our mission is to go beyond the simple metallic materials that we used in class, and create images that involve translucence like marble, jade and etc. We have included in the difference between regular BRDF with BSSRDF (subsurface scattering) that we are planning on implementing. 

It's easy to see the difference of which photo will look the most closest to the real life by actually comparing the photo that we created with the material that we can see with our own eyes. It is unclear how much we can speed up much as our main intention is to make a better rendering of the translucent material. It will be possible to measure with what inputs we can make the program faster. But if we have time, we also hope to make our program as fast as possible and see how much improvement we were able to see time-wise by graphing the speedups.

If we have time, we will try methods such as [Hybrid Monte Carlo](https://pdfs.semanticscholar.org/1a5f/b35237c112d7e9b2446bdb9c85427dac1a87.pdf) in rendering the translucent materials. So, understanding the math and calculations involved with this is very important before we even start coding anything.

We hope to see a photo with translucent materials that look like the actual material seen from the eye. Else, our understanding of math is probably wrong and should seek for help. But ideally, we would see a photo that rendered translucence correctly (at least imitates the real thing pretty well).

## Schedule

**1st week:** Figure out the complicated math, assemble the necessary resources, translate all resources into clear pseudocode, divide the path tracer into modules, and begin implementation.

**2nd week:** Finish coding at least half of the modules. Hopefully complete the majority of the implementation.

**3rd week:** Hope to finish coding if not yet there (leave 1 week for debugging), otherwise explore further extensions and stretch goals.

**4th week:** Tie up loose ends, focus on debugging, and maybe attempt the stretch goals. Spend time rendering quality images for your viewing pleasure.

## Resources

We are planning on starting from the ray tracer from project 3. By the end, with all the coding done, it will take a long time to run so we hope to run it by `ssh`-ing into the class account. We will need BSSRDF models and sufficient computing power to do the renders.

Our guiding resource is the paper provided in the spec:
[A Practical Model for Subsurface Light Transport](https://graphics.stanford.edu/papers/bssrdf/bssrdf.pdf)

However, we also found other papers that can be possibly useful alongside the main paper in implementing and understanding the math:

 - [Photon Beam Diffusion](http://disneyresearch.s3.amazonaws.com/wp-content/uploads/20140724021959/pbd1.pdf)
 - [Disney Using BSSRDF](http://blog.selfshadow.com/publications/s2015-shading-course/burley/s2015_pbs_disney_bsdf_slides.pdf)
 - [Hybrid Monte Carlo](https://pdfs.semanticscholar.org/1a5f/b35237c112d7e9b2446bdb9c85427dac1a87.pdf)
