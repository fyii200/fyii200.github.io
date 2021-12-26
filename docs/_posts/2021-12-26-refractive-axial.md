---
layout: post
title:  "Idenfying refractive error with a significant non-axial component"
date:   2021-12-26 14:49:02 +0000
categories: jekyll update
---
Refractive error arises from a mismatch between axial length (AL) and the refractive components of the eye, i.e. cornea, crystalline lens. Such mismatch is predominantly axial in most cases. AL is typically high (>24mm as a fairly useful rule of thumb) in myopes. Importantly, axial elongation is mainly attributable to changes in vitreous chamber depth. This explains why myopia is associated with clinical features in the posterior segment of the eye, e.g. peri-papillary atrophy, tesselation.

When modelled with a simple linear regression, however, AL alone does not explain the observed variance in spherical equivalent refraction (SER) to a very high degree. Published studies have reported R^2 values of [0.580](https://journals.lww.com/optvissci/Abstract/1994/09000/Role_of_the_Axial_Length_Corneal_Radius_Ratio_in.5.aspx) and [0.432](https://journals.plos.org/plosone/article/file?id=10.1371/journal.pone.0111766&type=printable). When anterior corneal radius (CR) is considered alongside AL, i.e. AL/CR, the observed variance in SER increases to **0.837** and **0.658**, respectively. This is corroborated by an unpublished dataset that I am playing with (412 instances; unknown age but likely to be university students). R^2 increases from 0.697 with AL to 0.817 with AL/CR (see Figure 1). Older age could [partly explain](https://iovs.arvojournals.org/article.aspx?articleid=2183169) why our R^2 is higher, since compensatory lens/ corneal changes are more likely to be evident in younger children (seen in the two published studies, <= 12y/o) than adults. 

Apart from measurement error, the remaining uncaptured variance can probably be accounted for by posterior corneal curvature, lenticular curvature (anterior and posterior), as well as the refractive indices of cornea, aqeuous humour, lens and vitreous humour. Given that these fea 

A DL model, 

