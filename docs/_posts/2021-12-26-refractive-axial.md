---
layout: post
title:  "Why care about differentiating axial from refractive ametropia?"
date:   2021-12-26 14:49:02 +0000
categories: jekyll update
---
Refractive error (ametropia thereafter) arises from a mismatch between axial length (AL) and the effective power of the refractive components of the eye, i.e. cornea, crystalline lens. Such mismatch is often (predominantly) **axial** in nature. AL is typically high (>24mm as a fairly useful rule of thumb) in myopes. Importantly, axial elongation is mainly attributable to changes in vitreous chamber depth. This explains why myopia is associated with clinical features in the posterior segment of the eye, e.g. peripapillary atrophy (PPA), tesselation.

In trying to elucidate what a deep learning (DL) model such as [Varadarajan's](https://iovs.arvojournals.org/article.aspx?articleid=2683803) looks at when predicting refractive error (regression task) from fundus images, I'm drawn to think that a large part of the model is really just predicting the axial component of ametropia. This is based on the understanding that: 
1. Variation in corneal and lenticular features is hardly reflected in a fundus image.
2. Retinal features that could possibly hold information about ametropia are mostly axial in nature.

Regarding (2), these retinal features **does not necessarily have to be biologically meaningful**, i.e. retinal thinning, PPA, etc., but they can also be related to the complex interactions between the camera system and the optics peculiar to the eye. One prominent example of the latter is the **variation in fundus magnification** across different levels of ametropia, which I will focus on in another post. For now, it is suffice to say that: 
> the main source of variation in fundus magnification is variation in AL rather than cornea/ lens curvature.

Therefore, we can hypothesise that:
> DL should at least be as good at predicting AL from fundus images as it is at predictng ametropia.

By extension, this also implies that:
> DL can predict axial ametropia better than refractive ametropia. 
 
**To test the last hypothesis, I first explore how classification of refractive ametropia and axial ametropia can be done in another post.** If the null hypothesis is to be rejected, then a lack of information pertaining to corneal/ lens curvature in retinal images could have some negative impact on a model's regression performance. One would, therefore, naturally hope that the **axial ametropia that we so often speak of is purely axial**, i.e. like a Gullstrand's schematic eye with axial ametropia where the effective power of the eye is fixed at +58.60D, and the only variable is AL.   

But real-world data suggest otherwise. We get a fuller picture of an eye's refractive state with the addition of anterior corneal radius (CR). When modelled with a simple linear regression, AL alone does not explain the observed variance in spherical equivalent refraction (SER) to a very high degree. Published studies have reported <img src="https://latex.codecogs.com/svg.image?R^2" title="R^2" /> values of [0.580](https://journals.lww.com/optvissci/Abstract/1994/09000/Role_of_the_Axial_Length_Corneal_Radius_Ratio_in.5.aspx) and [0.432](https://journals.plos.org/plosone/article/file?id=10.1371/journal.pone.0111766&type=printable). When **anterior CR** is considered alongside AL, i.e. AL/CR, the observed variance in SER increases **considerably** to **0.837** and **0.658**, respectively.

This is corroborated by an unpublished dataset that I am playing with (412 instances; unknown age but likely to be university students). <img src="https://latex.codecogs.com/svg.image?R^2" title="R^2" /> increases from **0.697** with AL to **0.817** with AL/CR (see Figure 1). Older age could [partly explain](https://iovs.arvojournals.org/article.aspx?articleid=2183169) why our <img src="https://latex.codecogs.com/svg.image?R^2" title="R^2" />  is higher, since compensatory lens/ corneal changes are more likely to be seen in younger children (in the two studies above, age ≤ 12y/o) than adults. 

### Figure 1
![Figure 1](/figures/2021-12-26-fig1.png)

The remaining uncaptured variance (after incorporating anterior CR) can plausibly be (partly) accounted for by lens curvature.[^1] Besides measurement error, noise associated with the normal variation in posterior corneal curvature as well as the refractive indices of cornea, aqueous humour, crystalline lens and vitreous humour is also likely to have reduced <img src="https://latex.codecogs.com/svg.image?R^2" title="R^2" /> to some extent.[^2]

This naturally leads one to wonder:
> Can we further improve the performance of DL that predicts ametropia from retinal images with the addition of anterior CR data?

<br>

---
[^1]: Since the lens contributes about 1/3 of the effective power of the eye, it is, alongside anterior corneal curvature, implicated in refractive ametropia. if left unaccounted for in a linear regression model, the residuals won't be normally distributed with centre at 0. This results in lower <img src="https://latex.codecogs.com/svg.image?R^2" title="R^2" />.
[^2]: These parameters are not usually implicated in refractive ametropia, e.g. posterior corneal curvature contributes little to the effective power of the eye because the difference in refractive index between the cornea, 1.376, and aqueous humour, 1.336, is small. And recall that <img src="https://latex.codecogs.com/svg.image?F&space;=&space;\frac{n^{'}-n}{r}&space;" title="F = \frac{n^{'}-n}{r} " />. But individual variation in these parameters add Gaussian (assuming normal distribution) noise to the underlying functon and may therefore reduce <img src="https://latex.codecogs.com/svg.image?R^2" title="R^2" />.
