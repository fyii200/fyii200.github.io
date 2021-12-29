---
layout: post
title:  "Axial length and corneal curvature, which affects fundus magnification more?"
date:   2021-12-29 13:51:46 +0000
categories: jekyll update
tags: fundus magnification across different levels of ametropia
---

In the previous post, I hypothesised that a fundus-based DL model would have difficulty predicting the refractive component of ametropia, i.e. that part of refractive error explained by corneal/ lens curvature. This is due not only to the absence of biologically meaningful features associated with corneal/ lens curvature in fundus images, but also because **variation in corneal/ lens curvature gives rise to relatively small variation in fundus magnification.** There is little information about corneal/ lens curvature in fundus images so to speak. I attempt to explain below how I arrived at this conclusion.

### Theoretical evidence
#### Figure 1: ray diagram depicting a myopic Bennett-Rabbetts three-surface schematic eye in front of an objective (condenser) lens with telecentric design ([Bennett et al. 1994](https://link.springer.com/content/pdf/10.1007/BF00175988.pdf))
![Figure 1](/figures/2021-12-29-fig1.png)

`About the ray diagram`
1. the condenser (assuming thin lens) is the lens that is closest to the eye. It is placed in such a way that its primary focal point, `F`, coincides with the primary principal point of the eye, `P`.
2. Recall that a principal point is where the principal plane (refraction can be said to occur in this plane in a thick/ compound lens system) intersects with the optical axis.
3. Hence, any light rays emerging from `P`, e.g. `FE`, will exit the condenser parallel to the optical axis, e.g.`EG`. Similarly, `HJ` will converge to point `F`.
4. A light ray emanating from a retinal point, `Q`, directed towards `P'`, will be refracted at `P`, and ends up as image `Q'1` at the **far point** of the eye, which is `k` distance away from `P`. *PS, far point is by definition the point in space that's conjugate with the retina when accommodation is relaxed; since the depicted eye is myopic, far point is located at a finite distance (reciprocal of refractive error).*
5. `Q'1` then becomes an object for the condenser. The first construction ray that we can use to find where the image will be formed is one that passes through the optical centre, `O`. The second ray is `FE` and already discussed in (2). The intersection of these two construction rays is where the resultant image, `Q'2` can be found.
<details><summary>Extra</summary>
<p>light ray passing through `O` will not be refracted, since nodal points coincide in a thin lens system. The two nodal points, along with the two principal points, all coincide at `O` because the refractive index is similar on both object and image sides.</p>
</details>
<br>

---
#### Deriving the equation for total magnification (using Figure 1 as reference)
Total magnification depends on the magnification due to the camera and that due to the optics of an eye. In deriving the equation for total magnification, it is helpful to keep in mind the general equation for magnification, `M`:

<p align="center"> (1) <img src="https://latex.codecogs.com/svg.image?M&space;=&space;\frac{s}{t}" title="M = \frac{s}{t}" width="80" /> </p> 

*where `s` is image size on the fundus camera film; `t` is the size of the retinal feature (object).*

My derivation will be based on two assumptions:
1. Small angle approximation of Gaussian optics; that is, `tanθ≈θ; sinθ≈θ; cosθ≈1`, where θ is in radian.
2. Telecentric camera system where the ratio of image size on the camera film, `s`, to `y` (OE; see Figure 1), is a constant `p`, such that <img src="https://latex.codecogs.com/svg.image?\frac{y}{s}&space;=&space;p" title="\frac{y}{s} = p" /> 

