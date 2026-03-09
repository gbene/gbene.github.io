+++
date = '2024-01-01'
draft = false
title = 'FracAbility: A python toolbox for survival analysis in fractured rock systems'
tags = ["poster","presentation"]
description = "TSG24, EGU24, DRT24 presentations"
showdate = true
showtags = false
openaccess=true
pub=false
firstauthor=true
contributingauthor=false
link=""
posterorpresentation = true
weight=2
toc=true

+++

Here are the talks and poster that I gave in 2024 regarding the publication: [Unbiased statistical length analysis of linear features: adapting survival analysis to geological applications](/publications/fracability). The TSG and EGU abstracts are identical as they were submitted one after the other.

## Tectonic Study Group 2024 | St. Andrews, UK
<hr>
{{< linkTo link="/fracability/presentation_tsg.pdf" display="Presentation" >}}

### Abstract
When analysing fractured rock outcrops, the fracture network's topology and length statistics are of fundamental importance. Past literature focused on adopting a non-parametric approach for the unbiased estimation of fracture length data mean, and with some additional steps, the variance of a population. However, technology improved, and necessities shifted. Now it is possible to quickly obtain dense length datasets with thousands of measurements and the emergence of stochastic DFNs increased the demand for parametric solutions to correctly fit several types of distributions. These conditions highlighted an absence of works on these topics. Of particular interest is the right censoring bias effect of the interpretational boundary on the fracture length statistics. We tackle this problem by applying survival analysis techniques, a branch of statistics that includes methods for modelling time to event data and correctly estimating the model’s parameters with data affected by censoring. Synthetic testing has been carried out, showing a reliable estimate of the distribution parameters with up to 80% of the total measurements being censored. Moreover, it is shown that the correction is independent from the orientation of the fracture set or boundary geometry. We propose FracAbility, a new open-source Python package capable to both analyse the topology of fracture networks and, by using the latest SciPy version, correctly fit different parametrical distributions on length data with right-censored measurements. The library and the proposed approach have been applied to real world data, successfully correcting length distributions affected by censoring. 

## European Geosciences Union 2024 | Wien, Austria
<hr>

{{< linkTo link="https://meetingorganizer.copernicus.org/EGU24/EGU24-22156.html" display="EGU link" >}}

{{< linkTo link="/fracability/poster.pdf" display="Poster" >}}

{{< callout text="This work has won the Outstanding Student and PhD candidate Presentation (OSPP) award!" >}}


### Abstract
When analysing fractured rock outcrops, the fracture network's topology and length statistics are of fundamental importance. Past literature focused on adopting a non-parametric approach for the unbiased estimation of fracture length data mean, and with some additional steps, the variance of a population. However, technology improved, and necessities shifted. Now it is possible to quickly obtain dense length datasets with thousands of measurements and the emergence of stochastic DFNs increased the demand for parametric solutions to correctly fit several types of distributions. These conditions highlighted an absence of works on these topics. Of particular interest is the right censoring bias effect of the interpretational boundary on the fracture length statistics. We tackle this problem by applying survival analysis techniques, a branch of statistics that includes methods for modelling time to event data and correctly estimating the model’s parameters with data affected by censoring. Synthetic testing has been carried out, showing a reliable estimate of the distribution parameters with up to 80% of the total measurements being censored. Moreover, it is shown that the correction is independent from the orientation of the fracture set or boundary geometry. We propose FracAbility, a new open-source Python package capable to both analyse the topology of fracture networks and, by using the latest SciPy version, correctly fit different parametrical distributions on length data with right censored measurements. The library and the proposed approach have been applied to real world data, successfully correcting length distributions affected by censoring.

### How to Cite
Benedetti, G., Casiraghi, S., Bistacchi, A., and Bertacchi, D.: FracAbility: A python toolbox for survival analysis in fractured rock systems, EGU General Assembly 2024, Vienna, Austria, 14–19 Apr 2024, EGU24-22156, https://doi.org/10.5194/egusphere-egu24-22156, 2024.

```bibtex
@inproceedings{benedetti2024fracability,
  title={FracAbility: A python toolbox for survival analysis in fractured rock systems},
  author={Benedetti, Gabriele and Casiraghi, Stefano and Bistacchi, Andrea and Bertacchi, Daniela},
  journal={European Geosciences Union General Assembly 2024 (EGU24)},
  pages={22156},
  year={2024}
}
```



## 24th International Conference on Deformation Mechanisms, Rheology and Tectonics | Barcelona, Spain
<hr>
{{< linkTo link="/fracability/presentation_drt.pdf" display="Presentation" >}}


{{<callout text="This work has won the Best Student Presentation award!">}}

### Abstract
From thin section to satellite image scale, the limited size of the study area introduces a bias in the interpretation of linear features, defined as right-censoring bias. We apply survival analysis techniques to obtain an unbiased estimate of multiple parametrical distributions in censored length datasets. Moreover, we show the effects of not considering such biases and propose a novel approach to select the best fitting model(s) using the Probability Integral Transform (PIT) technique.  





