# [Welcome](https://fyii200.github.io)
I am a PhD candidate based in the [Centre for Clinical Brain Sciences](https://www.ed.ac.uk/clinical-brain-sciences), with affliations to [SCONe](https://www.ed.ac.uk/clinical-sciences/ophthalmology/scone/about-scone) and [VAMPIRE](https://vampire.computing.dundee.ac.uk). The big picture of my PhD 
is to apply artificial intelligence approaches to predicting *short-sightedness **(myopia)***. The primary aim of this site is to support the [Open Science Initiative](https://en.wikipedia.org/wiki/Open_science) and document my work where possible, i.e. if not at risk of confidential data breaches.

*PS, this is just the repository for the site where code, figures, etc. are stored. I also give a high-level, not too geeky-techie but rather convoluted overview of the background of my PhD below. **[Actual site can be accessed here](https://fyii200.github.io).***

## Why myopia? 
### Because it is far more than just an optical inconvinience
Myopia is the most common form of refractive error. In 2020, over 30% of the global population is believed to be myopic, and this figure is set to reach nearly 50% by 2050<sup>1</sup>. But what's the big deal? Some may ask. Well, in addition to the significant economic burden, which is in and of itself a big topic (I refer keen readers to this [chapter](https://link.springer.com/chapter/10.1007/978-981-13-8491-2_3)<sup>2</sup> from *Updates on Myopia*), myopia increases the risk of a host of potentially sight-threatening eye diseases, e.g. retinal detachment, myopic maculopathy, glaucoma-like optic neuropathy, etc. Evidence now rejects such term as 'physiological myopia' because it carries the erroneous implication that some level of myopia is safe <sup>3</sup>. 

## Aetiology of myopia 
### Nature or nurture?
Following the seminal work of Wiesel and Raviola<sup>4</sup> in 1977, numerous animal studies provide strong evidence that refractive error of a developing eye can be manipulated under laboratory conditions (for an excellent review, see [IMI](https://myopiainstitute.org) report on experimental models of myopia<sup>5</sup>). For instance, one can quite literally induce some desired amount of refractive error by forcing the eye concerned to look through a lens of equivalent power for a protracted period of time. We can play God so to speak — the development of myopia is not purely deterministic after all. It is now widely accepted that the development of myopia arises from a complex interplay between genetic and environmental factors<sup>6</sup>. Epidemiologic studies point towards reduced outdoor time (light intensity probably plays an important role but this is still an area of active research) and intensive education as strong environmental risk factors<sup>7</sup>.

## 'Myo'cene: dawn of the epoch of myopia interventions
### The driving force<sup>5</sup>
The plethora of animal models and, to a lesser extent human models, in myopia research has got us closer to deciphering the origin of myopia (though we are still far from there in absolute terms). For instance, we now know that refractive error can still be modulated under laboratory conditions even when the connection between the eye and brain is cut off, or when the fovea (central part of the retina which we rely heavily on for high-resolution vision) is ablated. The driving force of myopia, therefore, seems to be local to the eye, and the peripheral retina plays an active role. 

At present, it is believed that some kind of visual stimuli, e.g. defocus/ blur, set off a cascade of biochemical changes in the retina (light-sensitive part of the eye), choroid (rich in blood vessels) and sclera (white coat of the eye). The whole cascade of events eventually leads to the remodelling of the sclera, making it weaker and more amenable to stretching. It is for this reason that an overwhelming majority of people with myopia are myopic because of longer eyes (axial myopia). Elongation of the eye, as it turns out, has deleterious effect on the posterior structures of the eye. This explains why (axial) myopia is associated myriad posterior eye diseases.  

### Beyond standard optical correction<sup>8</sup>
Thanks to these new insights, interventions that aim to slow childhood progression of myopia are becoming available in recent years. These are usually optical interventions that impose myopic defocus on the peripheral retina, i.e. force the image to focus in front of the peripheral retina to discourage eye growth. Pharmaceutical interventions, most popular being atropine (routinely used in parts of the world), arrived on the scene rather serendipituously. They were initially used for myopia control based on the theory that the accommodative system plays a role in myopia development and progression, but later evidence tilts the favour against this theory. 

Although the exact mechanisms remain nebulous, atropine and a number of optical interventions have been shown to be effective in slowing myopia progression in many clinical trials. Behavioural interventions, most notably increased outdoor time, also appear to be promising in mitigating myopia development. An increasing number of eye care practitioners are beginning to offer these interventions. **The advent of 'Myo'cene opens up exciting opportunities to tackle the myopia epidemic, but it also brings about new challenges...** 

## Towards precision medicine
### Striking the right balance between risk and benefit
Clinicians and scientitsts alike are painfully aware of the great phenotypic variation in myopia progression between individuals. For instance, the axial length (AL), aka eye length, among Chinese children in the 25th percentile increases by 2.51mm from 4 to 18 years of age, but children in the 75th percentile experience 4.43mm of eye growth during the same period <sup>9</sup>. Interventions such as atropine exhibit a dose-dependent response, i.e. higher concentrations (in the case of atropine) result in greater retardation of myopia progression and side effects<sup>8</sup>. As a result, risk-benefit assessment  becomes an integral part of myopia management. Stronger interventions associated with stronger side effects are clinically justifiable if the likelihood of rapid progression is high. Conversely, even a small risk becomes inordinately large if the likelihood of clinically significant progression is near zero.

### One size fits all
It should now be clear that such assessment is contigent upon our ability to predict future trajectory of myopia. Clinical decisions based on the coarsest risk-benefit assessment can be seen as one-size-fits-all, e.g. 0.01% atropine for every patient who might benefit from myopia control, and is therefore most susceptible to inter-individual variability.  

### Population-based estimates? Finer but not enough.
Fortunately, existing prediction methods provide us with means of patient stratification. However, methods such as axial length centile curves<sup>9, 10</sup> (i.e. based on current axial length, which growth percentile does my patient belong to?) and epidemiologic risk models<sup>10</sup> (i.e. given known risk factors like parental myopia, outdoor time, baseline refraction, etc., is my patient at risk of fast progression?) only give **population-based** estimates. Although good at representing the **average risk** within a sub-population, population-based estimates are still susceptible to inter-individual variability. For instance, having two myopic parents increase the risk of future myopia, but still, just over 20% of those who remain non-myopic have two myopic parents<sup>11</sup>.

Worse still, anecdotal accounts and personal experience suggest that some clinicians do not even bother using such population-based estimates. These methods are seen as belonging to the realm of the ivory tower or lacking practicality (e.g. community practices are not usually equipped with an ocular biometer). Clinicians typically resort to a one-size-fits-all approach or base their clinical decision on historical progression rate<sup>12</sup>. The downside of the former approach is obvious enough. The latter approach, though seems sensible, is not very reliable<sup>13</sup> and does not allow for earlier intervention.

### The aim: individual-level prediction
#### Machine Learning (ML)<sup>14</sup>
Given the discussion in the foregoing paragraphs, a natural question to ask is, **'can we predict myopia at the individual level?'** Maybe. One way to go about that is to build  high-dimensional models that take myriad features (e.g. baseline refraction, age, sex, parental myopia, outdoor time, baseline axial length, anterior corneal curvature, etc.) as input and output a prediction, e.g. risk of myopia onset, future myopia progression etc. With the incorporation of a large number of (pertinent) features, our prediction is more individualised. One could of course use conventional models like multiple linear regression or logistic regression (i.e. multiple predictive variables but just one output), but their capacity is limited by the linear decision boundary that they produce. 

More advanced ML algorithms, such as Support Vector Machine, Random Forest, etc., produce complex decision boundaries so are better at capturing complex patterns in the data. That said, these models, including multiple linear/ logistic regression, may not make it far into clinical practice due to the requirement for many input features. Measurements like axial length are not routinely collected in the community, and many clinicians can tell you just how laborious it is to deal with young patients! Additionally, such models can also suffer from the curse of dimensionality (i.e. high-dimensional data, where there are many input features, requires a massive amount of training data), and they also require careful selection of features (some features may be redundant).

#### Deep learning (DL)<sup>15</sup>
DL, a subset of ML, mitigates some of the challenges outlined above. In particular, it takes away the need for feature engineering as it learns to represent the features in the data at various levels of abstraction. This makes DL ideal for computer vision tasks. This naturally leads to the following question: **'Can we tap into the high representaion power of DL to predict myopia onset/ progression at the individual level from retinal images?'** 

This has several implications. First, clinicians will only have to take retinal images. This removes the hassle to link various sources of clinical data and input them in a structured manner to a model. Second, there is a wealth of information contained within retinal images, some of which may have even eluded our domain knowledge. Many features of myopia, such as tesselation and peri-papillary atrophy, can be seen from retinal images. Third, by probing where a trained DL model looks at when making prediction, we **may** discover novel biomarkers for myopia onset/ progression. I should add the caveat that we are only able to uncover the **predictive features** that a model utilises to produce its output. These features need not be biologically meaningful, e.g. differences in vessel metrics due to ocular magnification, but are valuable insofar as they can be used to generate new hypotheses about myopia development/ progression. 

### What about individual-level intervention?
**We can speak of various degrees of granularity of personalised intervention as we can of prediction.** Unlike prediction of myopia onset/progression though, I have reservations about the possibility of highly personalised myopia intervention in the medium term. One important hindrance, as I see it, is our rather limited understanding of the dose-dependent effect of many interventions. For instance, We do not yet know conclusively if optical interventions, e.g. ortho-K, DIMS, etc., also exhibit a dose-dependent response like atropine or if there is also a dose-dependent rebound effect. We also do not have a clear answer on how different groups of patients, e.g. slow progressors vs fast progressors, might respond differently to different treatment strengths. 

**We may soon have the means, *e.g. with the help of DL and polygenic risk score<sup>6</sup>*, to stratify patients with a level of granularity unimaginable years ago, but what use is such highly individualised prediction if we cannot yet achieve a comparable level of personalised intervention, *e.g. beyond just 0.025% atropine and 0.05% atropine?*** That said, I am hopeful that the advent of individualised prediction will encourage or aid further research into personalised intervention, not least because a successfully validated DL prediction model can help stratify participants into different risk groups in clinical trials that aim to elucidate some of the aforementioned questions. 

## Pathologic myopia (PM)
### Prelude
I should first say a few words to highlight the disntinction between the implications of predicting myopia onset and progression. We are concerned with children who aren't already myopic when we speak of myopia onset. It is the **risk** of **developing** myopia that we are trying to predict here. The implication of such prediction, though more limited than progression prediction, is that it allows early interventions to be put in place. At present, the only interventions to delay myopia onset are behavioural changes such as increased ourdoor time (strong evidence) and reduced near work (mixed evidence)<sup>8</sup>. Increased outdoor time, in particular, is most important insofar as myopia onset is concerned because it is more effective when a child is not already myopic. 

On the other hand, we are concerned with those who are already myopic when we speak of myopia progression. The aim of progression prediction is to single out patients at risk of high progression rate to justify the use of stronger interventions, e.g. higher-dose atropine, combination strategies, etc. **Ultimately, the goal is to keep the end point of myopia to a minimum so as to reduce the risk of irreversible visual impairment caused by diseases associated with myopia and PM.**

*PS, PM refers to excessive eye growth associated with myopia that leads to deleterious structural changes in the posterior segment of the eye, e.g. staphyloma and myopic maculopathy<sup>16</sup>.*

### High myopia, too late to help? Maybe Not.
Models that predict myopia onset and progression are pointless where adult patients are concerned (myopia usually develops and progresses during childhood). However, if an adult patient suffers from high (axial) myopia, one question one might be intrigued to ask is, **'Does this patient have PM?'** Knowing if someone has PM will enable timely management (where such intervention is available and backed by evidence), e.g. anti-vascular endothelial growth factor (anti-VEGF) for myopic macular neovascularisation (MNV)<sup>16</sup>, although there is no cure per se to reverse any structural changes that have already occured. DL models that detect different categories of PM with good performance are already available<sup>17,18</sup>.

Another question one might want to consider is, **'How likely is future PM?'** There is currently no DL model that makes such prediction. This is due in part to the lack of big longitudinal data, but this is being addressed by the large-scale effort of [SCONe](https://www.ed.ac.uk/clinical-sciences/ophthalmology/scone/about-scone) (introduced below). Though the application of such a model is somewhat more limited at present owing to the lack of prophylaxis for PM generally, things may change for myopic maculopathy and staphyloma in the future<sup>16</sup>. Therefore, another focus of my research is to develop models that make temporal prediction about PM using the META-PM<sup>19</sup> classification system.

## Axial length (AL)
### What matters at the end of the day
Given the importance of eye length in the pathogenesis of ocular complications associated with myopia, AL changes are now an important outcome measure in every myopia clinical trial. All myopia interventions are based on the premise that they will slow axial elongation (eye growth) to some extent. Indeed, refractive error is just a useful proxy measure of AL where myopia control is concerned. Moreover, to evaluate the success of ortho-K (a special, hard contact lens worn overnight to reshape the front clear 'window' of the eye) as a myopia intervention, AL measurement is also of paramount importance. This is because true changes in refractive error between visits are masked by changes in corneal curvature.

### Predict AL from retinal images
The secondary aim of my research is to see if one can predict AL from retinal images using DL. It would also be interesting to see if temporal changes in AL can be predicted using a similar approach.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

<sub> 1. Holden B, Fricke T, Wilson D, Jong M, Naidoo K, Sankaridurg P et al. Global Prevalence of Myopia and High Myopia and Temporal Trends from 2000 through 2050. Ophthalmology. 2016;123(5):1036-1042. </sub>

<sub> 2. Chua S.Y.L., Foster P.J. (2020) The Economic and Societal Impact of Myopia and High Myopia. In: Ang M., Wong T. (eds) Updates on Myopia. Springer, Singapore. </sub>

<sub> 3. Flitcroft D. The complex interactions of retinal, optical and environmental factors in myopia aetiology. Progress in Retinal and Eye Research. 2012;31(6):622-660. </sub>

<sub> 4. Wiesel T, Raviola E. Myopia and eye enlargement after neonatal lid fusion in monkeys. Nature. 1977;266(5597):66-68. </sub>

<sub> 5. Troilo D, Smith E, Nickla D, Ashby R, Tkatchenko A, Ostrin L et al. IMI – Report on Experimental Models of Emmetropization and Myopia. Investigative Opthalmology & Visual Science. 2019;60(3):M31. </sub>

<sub> 6. Tedja M, Haarman A, Meester-Smoor M, Kaprio J, Mackey D, Guggenheim J et al. IMI – Myopia Genetics Report. Investigative Opthalmology & Visual Science. 2019;60(3):M89. </sub>

<sub> 7. Morgan I, Wu P, Ostrin L, Tideman J, Yam J, Lan W et al. IMI Risk Factors for Myopia. Investigative Opthalmology & Visual Science. 2021;62(5):3. </sub>
<sub> 8. Wildsoet C, Chia A, Cho P, Guggenheim J, Polling J, Read S et al. IMI – Interventions for Controlling Myopia Onset and Progression Report. Investigative Opthalmology & Visual Science. 2019;60(3):M106. </sub>

<sub> 9. He X, Sankaridurg P, Naduvilath T, Wang J, Xiong S, Weng R et al. Normative data and percentile curves for axial length and axial length/corneal curvature in Chinese children and adolescents aged 4–18 years. British Journal of Ophthalmology. 2021;:bjophthalmol-2021-319431. </sub>

<sub> 10. Han X, Liu C, Chen Y, He M. Myopia prediction: a systematic review. Eye. 2021;. </sub>

<sub> 11. Jones L, Sinnott L, Mutti D, Mitchell G, Moeschberger M, Zadnik K. Parental History of Myopia, Sports and Outdoor Activities, and Future Myopia. Investigative Opthalmology & Visual Science. 2007;48(8):3524. </sub>

<sub> 12. Leshno A, Farzavandi S, Gomez-de-Liaño R, Sprunger D, Wygnanski-Jaffe T, Mezer E. Practice patterns to decrease myopia progression differ among paediatric ophthalmologists around the world. British Journal of Ophthalmology. 2019;104(4):535-540. </sub>

<sub> 13. Matsumura S, Lanca C, Htoon H, Brennan N, Tan C, Kathrani B et al. Annual Myopia Progression and Subsequent 2-Year Myopia Progression in Singaporean Children. Translational Vision Science & Technology. 2020;9(13):12. </sub>

<sub> 14. Hastie T, Tibshirani R, Friedman J. The elements of statistical learning. 2nd ed. Springer; 2009. </sub>

<sub> 15. Goodfellow I, Bengio Y, Courville A. Deep learning. Cambridge (EE. UU.): MIT Press; 2016. </sub>

<sub> 16. Ohno-Matsui K, Wu P, Yamashiro K, Vutipongsatorn K, Fang Y, Cheung C et al. IMI Pathologic Myopia. Investigative Opthalmology & Visual Science. 2021;62(5):5. </sub>

<sub> 17. Du R, Xie S, Fang Y, Igarashi-Yokoi T, Moriyama M, Ogata S et al. Deep Learning Approach for Automated Detection of Myopic Maculopathy and Pathologic Myopia in Fundus Images. Ophthalmology Retina. 2021;5(12):1235-1244. </sub>

<sub> 18. Hemelings R, Elen B, Blaschko M, Jacob J, Stalmans I, De Boever P. Pathological myopia classification with simultaneous lesion segmentation using deep learning. Computer Methods and Programs in Biomedicine. 2021;199:105920. </sub>

<sub> 19. Ohno-Matsui K, Kawasaki R, Jonas J, Cheung C, Saw S, Verhoeven V et al. International Photographic Classification and Grading System for Myopic Maculopathy. American Journal of Ophthalmology. 2015;159(5):877-883.e7. </sub>
