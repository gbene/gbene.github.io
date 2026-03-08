+++
date = '2025-05-15'
draft = false
title = 'Unbiased statistical length analysis of linear features: adapting survival analysis to geological applications'
tags = ["published", "first author"]
description = "At any scale, the limited size of a study area introduces a bias in the interpretation of linear features, defined as right-censoring bias. We show the effects of not considering such bias and apply survival analysis techniques to obtain unbiased estimates of multiple parametrical distributions in three censored length datasets. Finally, we propose a novel approach to select the most representative model from a sensible candidate pool using the probability integral transform technique."
showdate = true
showtags = false
openaccess=true
pub=true
firstauthor=true
link="https://se.copernicus.org/articles/16/367/2025/"
weight=1
+++

## Abstract

A proper quantitative statistical characterization of fracture length or height is of paramount importance when analysing outcrops of fractured rocks. Past literature suggests adopting a non-parametric approach, such as circular scanlines, for the unbiased estimation of the fracture-length mean value. This is due to the fact that, in the past, estimating any type of statistical distribution was difficult and there was no real interest in defining precise parametrical models. However, due to the recent rise in popularity of digital outcrop models (DOMs) and of stochastic discrete fracture networks (DFNs), there is an increasing demand for distribution-based solutions that output a correct estimation of parameters for a given proposed model (e.g. mean and standard deviation). This change in demand highlights in the geological literature the absence of properly structured theoretical works on this topic. Our methodology, presented for the first time in this contribution, represents a powerful alternative to non-parametrical methods, aimed at specifically treating censoring bias and obtaining an unbiased trace-length statistical model. As our first objective, we propose to tackle the censoring bias by applying survival analysis techniques: a branch of statistics focused on modelling time-to-event data and correctly estimating model parameters with data affected by censoring. As a second objective, we propose a novel approach for selecting the most representative parametric model. We combine a direct visual approach and the calculation of four statistics to quantify how well proposed models reflect the data. We apply survival analysis to correctly estimate statistical parameters of a censored length dataset in three different case studies and show the effects of the censoring percentage on parametrical estimations that do not use this paradigm. The presented analyses are carried out using an open-source Python package called FracAbility, which we purposefully created to carry out the described workflow ([https://github.com/gecos-lab/FracAbility](https://github.com/gecos-lab/FracAbility), last access: 8 September 2024).


## Awards

This work has won the [Outstanding Student and PhD candidate Presentation](https://www.egu.eu/awards-medals/ospp-award/2024/gabriele-benedetti/) (OSPP) Awards for the European Geosciences Union (EGU24) and the best student presentation award for the 24th International Conference on Deformation Mechanisms, Rheology and Tectonics (DRT24)! To download the poster or presentation go [here](/publications/fracability_press)
## How to cite

Benedetti, G., Casiraghi, S., Bertacchi, D., and Bistacchi, A.: Unbiased statistical length analysis of linear features: adapting survival analysis to geological applications, Solid Earth, 16, 367–390, https://doi.org/10.5194/se-16-367-2025, 2025. 

```bibtex
@article{benedetti2025unbiased,
  title={Unbiased statistical length analysis of linear features: adapting survival analysis to geological applications},
  author={Benedetti, Gabriele and Casiraghi, Stefano and Bertacchi, Daniela and Bistacchi, Andrea},
  journal={Solid Earth},
  volume={16},
  number={4/5},
  pages={367--390},
  year={2025},
  publisher={Copernicus Publications G{\"o}ttingen, Germany}
}

```

