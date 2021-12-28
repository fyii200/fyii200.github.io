---
layout: post
title:  "Idenfying refractive error with a significant non-axial component"
date:   2021-12-26 14:49:02 +0000
categories: jekyll update
---
Refractive error arises from a mismatch between axial length (AL) and the refractive components of the eye, i.e. cornea, crystalline lens. Such mismatch is **predominantly axial** in most cases. AL is typically high (>24mm as a fairly useful rule of thumb) in myopes. Importantly, axial elongation is mainly attributable to changes in vitreous chamber depth. This explains why myopia is associated with clinical features in the posterior segment of the eye, e.g. peripapillary atrophy (PPA), tesselation.

In an attempt to elucidate what a deep learning (DL) model such as [Varadarajan's](https://iovs.arvojournals.org/article.aspx?articleid=2683803) looks at when predicting (regression) refractive error from fundus images, I think it is sensible to believe that a large part of the model is really just predicting the axial component of ametropia. My conviction is based on the understanding that: 
1. Variation in corneal and lenticular features are hardly reflected in a fundus image.
2. Retinal features that could possibly hold information about ametropia are mostly axial in nature.

These retinal features **need not be biologically meaningful**, i.e. retinal thinning, PPA, etc., but can also be related to the complex interactions between the camera system and the optics of the eye. One prominent example of the latter is the **variation in fundus magnification** across different levels of ametropia, which I will focus on in another post. For now, it is suffice to say that: 
> the source of variation in fundus magnification, as far as ocular components are concerned, seems to be largely attributable to AL rather than cornea/ lens curvature.

Therefore, we can hypothesise that:
> DL should be at least as good at predicting AL from fundus images as it is at predictng ametropia.

By extension, this also implies that:
> DL is not as capable of predicting ametropia with a significant refractive component as it is of ametropia that is largely axial in nature.

When modelled with a simple linear regression, however, AL alone does not explain the observed variance in spherical equivalent refraction (SER) to a very high degree. Published studies have reported <img src="https://latex.codecogs.com/svg.image?R^2" title="R^2" /> values of [0.580](https://journals.lww.com/optvissci/Abstract/1994/09000/Role_of_the_Axial_Length_Corneal_Radius_Ratio_in.5.aspx) and [0.432](https://journals.plos.org/plosone/article/file?id=10.1371/journal.pone.0111766&type=printable). When **anterior corneal radius (CR)** is considered alongside AL, i.e. AL/CR, the observed variance in SER increases to **0.837** and **0.658**, respectively. 

This is corroborated by an unpublished dataset that I am playing with (412 instances; unknown age but likely to be university students). <img src="https://latex.codecogs.com/svg.image?R^2" title="R^2" /> increases from 0.697 with AL to 0.817 with AL/CR (see Figure 1). Older age could [partly explain](https://iovs.arvojournals.org/article.aspx?articleid=2183169) why our <img src="https://latex.codecogs.com/svg.image?R^2" title="R^2" />  is higher, since compensatory lens/ corneal changes are more likely to be seen in younger children (in the two studies above, age ≤ 12y/o) than adults. 

The remaining uncaptured variance can plausibly be accounted for by lens curvature.[^1] Apart from measurement error, noise associated with normal variation in posterior corneal curvature as well as the refractive indices of cornea, aqueous humour, crystalline lens and vitreous humour is also likely to have attenuated <img src="https://latex.codecogs.com/svg.image?R^2" title="R^2" /> to some extent.[^2]


[^1]: Since the lens contributes about 1/3 of the effective power of the eye, it is, alongside anterior corneal curvature, implicated in refractive ametropia. if left unaccounted in a linear regression model, the residuals won't be normally distributed with centre at 0. This results in lower <img src="https://latex.codecogs.com/svg.image?R^2" title="R^2" />.
[^2]: These parameters are not usually implicated in refractive ametropia, e.g. posterior corneal curvature contributes little to the effective power of the eye because the difference in refractive index between the cornea, 1.376, and aqueous humour, 1.336, is small. And recall that <img src="https://latex.codecogs.com/svg.image?F&space;=&space;\frac{n^{'}-n}{r}&space;" title="F = \frac{n^{'}-n}{r} " />. Hence, they lower <img src="https://latex.codecogs.com/svg.image?R^2" title="R^2" /> by means of adding Gaussian noise (assuming normal distribution).
