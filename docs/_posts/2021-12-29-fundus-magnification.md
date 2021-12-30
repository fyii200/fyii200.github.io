---
layout: post
title:  "Axial length and corneal curvature, which affects fundus magnification more?"
date:   2021-12-29 13:51:46 +0000
categories: jekyll update
tags: fundus magnification across different levels of ametropia
---

In the previous post, I hypothesised that a fundus-based DL model would have difficulty predicting the refractive component of ametropia, i.e. that part of refractive error attributable to corneal/ lens curvature. This is due not only to the absence of biologically meaningful features associated with corneal/ lens curvature in fundus images, but also because **variation in corneal/ lens curvature gives rise to relatively small variation in fundus magnification.** There is little information about corneal/ lens curvature in fundus images so to speak. I discuss below how I arrived at this conclusion.

## Theoretical evidence
##### Figure 1: ray diagram depicting a myopic three-surface schematic eye in front of an objective (condenser) lens with telecentric design (taken from [Bennett et al. 1994](https://link.springer.com/content/pdf/10.1007/BF00175988.pdf))
![Figure 1](/figures/2021-12-29-fig1.png)

`About the ray diagram`
1. the condenser (assuming thin lens) is the lens that is closest to the eye. It is placed in such a way that its primary focal point, `F`, coincides with the primary principal point of the eye, `P`.
2. Recall that a principal point is where the principal plane (refraction can be said to occur in this plane in a thick/ compound lens system) intersects with the optical axis.
3. Hence, any light rays emerging from `P`, e.g. `FE`, will exit the condenser parallel to the optical axis, e.g.`EG`. Similarly, `HJ` will converge to point `F`.
4. A light ray emanating from a retinal point, `Q`, directed towards `P'`, will be refracted at `P`, and ends up as image `Q'1` at the **far point** of the eye, which is `k` distance away from `P`. *PS, far point is by definition the point in space that's conjugate with the retina when accommodation is relaxed; since the depicted eye is myopic, far point is located at a finite distance (reciprocal of refractive error).*
5. `Q'1` then becomes an object for the condenser. The first construction ray we can use to find where the image will be formed is one that passes through the optical centre, `O`. The second construction ray is `FE` (behavior already discussed in 3). The intersection of these two construction rays is where the resultant image, `Q'2` is formed.
<details><summary>Extra</summary>
<p>light ray passing through `O` will not be refracted, since nodal points coincide in a thin lens system. The two principal points also coincide at `O` because the refractive index is similar on both the object and image sides of the lens.</p>
</details>
<br>

---
#### Deriving the equation for total magnification (using Figure 1 as reference)
Total magnification depends on the magnification due to the camera and that due to the optics of an eye. In deriving the equation for total magnification, it is helpful to keep in mind the general equation for magnification, `M`:

<p align="center"> (1) <img src="https://latex.codecogs.com/svg.image?M&space;=&space;\frac{s}{t}" title="M = \frac{s}{t}" /> </p> 

*where `s` is image size on the fundus camera film; `t` is the size of the retinal feature of interest (object).*

The following derivation will be based on two assumptions:
1. Small-angle approximation of Gaussian optics; that is, `tanθ≈θ; sinθ≈θ; cosθ≈1`, where θ is in radian.
2. Telecentric camera system where the ratio of image size on the camera film, `s`, to `y` (OE; see Figure 1), is a constant `p` over a wide range of ametropia, such that <img src="https://latex.codecogs.com/svg.image?\frac{y}{s}&space;=&space;p" title="\frac{y}{s} = p" />.

### Let's first express object size, `t`
Assuming `t` is small (not unreasonable), we can use trigonometry:

<p align="center"> (2) <img src="https://latex.codecogs.com/svg.image?tan(U')&space;=&space;\frac{t}{k'}" title="tan(U') = \frac{t}{k'}" /> </p>

Given the small-angle approximation, (2) can be rewritten as:

<p align="center"> (3) <img src="https://latex.codecogs.com/svg.image?U'&space;=&space;\frac{t}{k'}" title="U' = \frac{t}{k'}" /> </p>

Hence:
<p align="center"> (4) <img src="https://latex.codecogs.com/svg.image?t&space;=&space;u'\times&space;k'" title="t = u'\times k'" /> </p>

Because of the small-angle approximation, we can also rewrite Snell's Law, <img src="https://latex.codecogs.com/svg.image?n_{1}\cdot&space;&space;sin(\theta_{1})&space;=&space;n_{2}\cdot&space;&space;sin(\theta_{2})" title="n_{1}\cdot sin(\theta_{1}) = n_{2}\cdot sin(\theta_{2})" />, as:

<p align="center"> (5) <img src="https://latex.codecogs.com/svg.image?n_{1}\cdot&space;&space;\theta_{1}&space;=&space;n_{2}\cdot&space;&space;\theta_{2}" title="n_{1}\cdot \theta_{1} = n_{2}\cdot \theta_{2}" /> </p>

Considering `QP'` and `PE`, n1 is the refractive index of aqeuous/ vitreous humour **(1.336)**, while n2 is the refractive index of air **(1.000)**. Likewise, `θ1=U'` and `θ2=U`:

<p align="center"> (6) <img src="https://latex.codecogs.com/svg.image?U'&space;=&space;\frac{U}{1.336}" title="U' = \frac{U}{1.336}" /> </p>

Substituting (6) into (4):

<p align="center"> (7) <img src="https://latex.codecogs.com/svg.image?t&space;=&space;\frac{U&space;\cdot&space;k'}{1.336}" title="t = \frac{U \cdot k'}{1.336}" /> </p>

`U` is in radian because the small-angle approximation only works if the unit is radian. Let's convert it to degree:

<p align="center"> (8) <img src="https://latex.codecogs.com/svg.image?t&space;=&space;\frac{U^{o}&space;\cdot&space;k'}{1.336&space;\times&space;&space;57.2958}&space;=&space;0.01306&space;\cdot&space;k'&space;\cdot&space;U^{o}" title="t = \frac{U^{o} \cdot k'}{1.336 \times 57.2958} = 0.01306 \cdot k' \cdot U^{o}" /> </p>

<br>
### Now express image size, `s`

We can re-express `s` from our telecentric assumption:

<p align="center"> (9) <img src="https://latex.codecogs.com/svg.image?s&space;=&space;\frac{y}{p}" title="s = \frac{y}{p}" /> </p>

where `p` is a camera-specific constant. It tells us:
> How big of a change in `y` size should we expect to see a 1-unit change in image size?

Assuming that the distance between the eye `p` and the condenser is constant (e.g. minimal head movement, etc.), the only variable that could effect `y` is the angle between the refracted ray (by the eye) and optical axis, `U`. Hence:

<p align="center"> (10) <img src="https://latex.codecogs.com/svg.image?s&space;=&space;\frac{U}{p}" title="s = \frac{U}{p}" /> </p>

After re-expressing (10), i.e. `U = s.p, we can substitute the resultant expression into (8):

<p align="center"> (11) <img src="https://latex.codecogs.com/svg.image?t&space;=&space;0.01306&space;\cdot&space;k'&space;\cdot&space;s&space;\cdot&space;p" title="t = 0.01306 \cdot k' \cdot s \cdot p" /> </p>


### Final magnification equation

We can move `s` to the other side of the equation and arrive at our final equation for magnification, `M`:

<p align="center"> (12) <img src="https://latex.codecogs.com/svg.image?M&space;=&space;\frac{s}{t}&space;=\frac{1}{0.01306&space;\cdot&space;k'&space;\cdot&space;p&space;}&space;" title="M = \frac{s}{t} =\frac{1}{0.01306 \cdot k' \cdot p } " /> </p>

Since `p` is a constant (can be thought of as the camera magnification factor with a telecentric design), the only variable that affects magnification is `K'`, which is the distance between the secondary principal point of the eye, `P'` and the centre of the retina. Therefore:

<p align="center"> (13) <img src="https://latex.codecogs.com/svg.image?k'&space;=&space;AL&space;-&space;A_{1}P'&space;" title="k' = AL - A_{1}P' " /> </p>

*where AL is axial length and <img src="https://latex.codecogs.com/svg.image?A_{1}P'&space;" title="A_{1}P' " /> is the distance between the corneal apex and `P'`.*

> It is now obvious that total magnification is dependent on axial length, i.e. the longer the eye (tend to be more myopic), the smaller the magnification.

> Total magnification also depends on the position of P' from the corneal apex, which is in turn dependent on corneal and lens powers.

<br>

### Justification that axial length affects `M` to a larger extent
Let's assume that the eye in Figure 1 depicts the Gullstrand-Emsley schematic eye. Table 12.6 in the book by [Bennett & Rebbetts 1984](https://www.semanticscholar.org/paper/Clinical-Visual-Optics-Bennett-Rabbetts/e29470029b10319e205205eaf3caa69883726858) shows how <img src="https://latex.codecogs.com/svg.image?A_{1}P'&space;" title="A_{1}P' " /> changes over a wide range of corneal and lens powers. The table also shows the equivalent power of the eye, <img src="https://latex.codecogs.com/svg.image?F_{eye}" title="F_{eye}" />, for each combination of corneal and lens powers. One important observation is:

> <img src="https://latex.codecogs.com/svg.image?A_{1}P'&space;" title="A_{1}P' " /> varies only by a small amount (1.35mm - 2.35mm) over a wide range of corneal-lens power combinations

<br>
##### Table 1: Column marked with asterisks represents emmetropia in the Gullstrand-Emsley schematic eye. 

<table>
<tr>
<td  colspan=1>Corneal power (D)</td> <td style="text-align:center" colspan=3> +38.00</td>  <td style="text-align:center" colspan=3> +42.73 </td> <td style="text-align:center" colspan=3> +48.00</td>
</tr>

<tr>
<td colspan=1>Lens power (D)</td> <td colspan=1>+15.0</td> <td colspan=1>+21.3</td> <td colspan=1>+29.0</td> <td colspan=1>+15.0</td> <td colspan=1> *+21.3*</td> <td colspan=1>+29.0</td> <td colspan=1>+15.00</td> <td colspan=1>+21.30</td> <td colspan=1>+29.00</td> 
</tr>

<tr>
<td colspan=1> <img src="https://latex.codecogs.com/svg.image?F_{eye}" title="F_{eye}" /> (D) </td> <td colspan=1>+51.24</td> <td colspan=1>+56.20</td> <td colspan=1>+61.60</td> <td colspan=1>+55.65</td> <td colspan=1> *+60.49* </td> <td colspan=1>+65.76</td> <td colspan=1>+60.55</td> <td colspan=1>+65.26</td> <td colspan=1>+70.39</td> 
</tr>

<tr>
<td colspan=1> <img src="https://latex.codecogs.com/svg.image?A_{1}P'&space;" title="A_{1}P' " /> (mm)</td> <td colspan=1>1.65</td> <td colspan=1>2.03</td> <td colspan=1>2.35</td> <td colspan=1>1.50</td> <td colspan=1> *1.85* </td> <td colspan=1>2.17</td> <td colspan=1>1.35</td> <td colspan=1>1.69</td> <td colspan=1>1.98</td>
</tr>
</table>

#### Modelling refractive ametropia using Table 1
We will hold AL constant with a value that would normally give rise to emmetropia and use different combinations of corneal-lens power in Table 1. Emmetropic AL can be found by first calculating `k'`, i.e. distance from `P'` (because refraction occurs here) to back of the eye:

<p align="center"> (14) <img src="https://latex.codecogs.com/svg.image?F_{eye}&space;=&space;\frac{n'}{k'}&space;-&space;L" title="F_{eye} = \frac{n'}{k'} - L" /> </p>

*Where <img src="https://latex.codecogs.com/svg.image?F_{eye}" title="F_{eye}" /> is the equivalent power of an emmetropic eye; `n'` is the refractive index of aqeuous/ vitreous humour; `L` is the vergence of the incident light.* `L` is 0 in an emmetropic eye because its far point is at inifinity. Thus, solving the following equation:

<p align="center"> <img src="https://latex.codecogs.com/svg.image?60.49&space;=&space;\frac{1.333}{k'}&space;-&space;0" title="60.49 = \frac{1.333}{AL} - 0" /> </p>

gives us **`k'`= 22.04mm**. 

**`AL`** is simply <img src="https://latex.codecogs.com/svg.image?A_{1}P'" title="A_{1}P'" /> + `k'`= 22.04mm + 1.85mm (Table 1) = **23.89mm**.

We can then repurpose equation (14) to calculate (refractive) ametropia, i.e. solve for `L` because it represents ametropia (its reciprocal is equal to the far point) 




![Figure 2](/figures/2021-12-29-fig2.png)

