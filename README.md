# [Welcome](https://fyii200.github.io)
I am a PhD candidate based in the [Centre for Clinical Brain Sciences](https://www.ed.ac.uk/clinical-brain-sciences), with affliations to [SCONe](https://www.ed.ac.uk/clinical-sciences/ophthalmology/scone/about-scone) and [VAMPIRE](https://vampire.computing.dundee.ac.uk). The big picture of my PhD 
is to apply artificial intelligence approaches to predicting *short-sightedness **(myopia)***. The primary aim of this site is to support the [Open Science Initiative](https://en.wikipedia.org/wiki/Open_science) and document my work where possible, i.e. if not at risk of confidential data breaches.

**PS, this is just the repository for the site where code, figures, etc. are stored. I also give a high-level but rather convoluted overview of the background of my research below. 
Actual site can be accessed [here](https://fyii200.github.io).**

## Why myopia? 
### Because it is far more than just an optical inconvinience
Myopia is the most common form of refractive error. In 2020, over 30% of the global population is believed to be myopic, and this figure is set to reach nearly 50% by 2050<sup>1</sup>. But what's the big deal? Some may ask. Well, in addition to the significant economic burden, which is in and of itself a big topic (I refer keen readers to this [chapter](https://link.springer.com/chapter/10.1007/978-981-13-8491-2_3)<sup>2</sup> from *Updates on Myopia*), myopia increases the risk of a host of potentially sight-threatening eye diseases, e.g. retinal detachment, myopic maculopathy, glaucoma-like optic neuropathy, etc. Evidence now rejects such term as 'physiological myopia' because it carries the erroneous implication that some level of myopia is safe <sup>3</sup>. 

## Aetiology of myopia 
### Nature or nurture?
Following the seminal work of Wiesel and Raviola<sup>4</sup> in 1977, numerous animal studies provide strong evidence that refractive error of a developing eye can be manipulated under laboratory conditions (for an excellent review, see [IMI](https://myopiainstitute.org) report on experimental models of myopia<sup>5</sup>). For instance, one can quite literally induce some desired amount of refractive error by forcing the eye concerned to look through a lens of equivalent power for a protracted period of time. We can play God so to speak — the development of myopia is not purely deterministic after all. It is now widely accepted that the development of myopia arises from a complex interplay between genetic and environmental factors<sup>6</sup>. Epidemiologic studies point towards reduced outdoor time (light intensity probably plays an important role but this is still an area of active research) and intensive education as strong environmental risk factors<sup>7</sup>.

## 'Myo'cene: dawn of the epoch of myopia interventions
### The driving force<sup>5</sup>
The plethora of animal models and, to a lesser extent human models, in myopia research has got us closer to deciphering the origin of myopia (though we are still far from there in absolute terms). For instance, we now know that refractive error can still be modulated under laboratory conditions even when the connection between the eye and brain is cut off, or when the fovea (central part of the retina which we rely heavily on for high-resolution vision) is ablated. Taken together, the driving force of myopia is local to the eye and peripheral retina also plays an active role. 

At present, it is believed that some kind of visual stimuli, e.g. defocus/ blur, set off a cascade of biochemical changes in the retina, choroid and sclera. The whole cascade of events eventually leads to scleral (white coat of the eye) remodelling, making it weaker and more amenable to stretching. It is for this reason that an overwhelming majority of people with myopia are myopic because of longer eyes (axial myopia). Elongation of the eye, as it turns out, has deleterious effect on the posterior structures of the eye. This explains why (axial) myopia is associated myriad posterior eye diseases.  

### Beyond standard optical correction<sup>8</sup>
Thanks to these new insights, interventions that aim to slow down childhood progression of myopia are becoming available in recent years. These are usually optical interventions that impose myopic defocus on peripheral retina, i.e. force the light to focus before the retina in the periphery so the central high-resolution vision is not affected. Pharmaceutical interventions, most popular being atropine (routinely used in parts of the world), arrived on the scene rather serendipituously. They were initially used for myopia control based on the theory that the accommodative system plays a role in myopia development and progression, but later evidence tilts the favour against this theory. 

Although the exact mechanisms remain nebulous, atropine and a number of optical interventions have been shown to be effective in slowing down myopia progression in many clinical trials. Behavioural interventions, most notably increased outdoor time, also appear to be promising in mitigating myopia development. An increasing number of eye care practitioners are beginning to offer these interventions. **The advent of 'Myo'cene opens up exciting opportunities to tackle the myopia epidemic, but it also brings about new challenges...** 

## Towards precision medicine
### Striking the right balance between risk and benefit
Clinicians and scientitsts alike are painfully aware of the great phenotypic variation in myopia progression between individuals. Interventions such as atropine exhibit a dose-dependent response, i.e. higher concentrations (in the case of atropine) result in greater retardation of myopia progression and side effects. As a result, risk-benefit assessment  becomes an integral part of myopia management. Stronger interventions associated with stronger side effects are clinically justifiable if the likelihood of rapid progression is high. Conversely, even a small risk becomes inordinately large if the likelihood of clinically significant progression is near zero.

### One-size-fits all
It should now be clear that such assessment is contigent upon our ability to predict future trajectory of myopia. Clinical decisions based on the coarsest assessment can be seen as one-size-fits-all, e.g. 0.01% atropine for every patient who might benefit from myopia control, and is therefore most susceptible to inter-individual variability. 

### Population-based estimates? Finer but not enough.
Fortunately, existing prediction methods provide us with means of patient stratification. However, methods such as axial length centile curves (i.e. based on current axial length, which growth percentile does my patient belong to?) and epidemiologic risk models (i.e. given known risk factors like parental myopia, outdoor time, baseline refraction, etc., does my patient belong to the at-risk group?) only give **population-based** estimates. Although good at representing the **average risk** within a sub-population, population-based estimates are still susceptible to inter-individual variability. For instance, having two myopic parents increase the risk of future myopia, but still, just over 20% of those who remain non-myopic have two myopic parents.

Worse still, anecdotal accounts and personal experience suggest that some clinicians do not even bother using such evidence-based, population-based estimates. These methods are seen as belonging to the realm to the ivory tower or lacking practicality (e.g. community practices are usually not equipped with an ocular biometer). In this scenario, clinicians either resort to the one-size-fits-all approach or base their clinical decision on historical progression rate. The downside of the former approach is obvious. The latter approach, though seems sensible, is not reliable as a single predictive factor and does not allow earlier intervention.

### Individual-level prediction



