+++
date = '2023-05-19'
draft = false
title = 'Fracability'
tags = ["library"]
description = "Python toolbox to analyse fracture networks for digitalized rock outcrops. "
showdate = true
showtags = false
firstauthor=true
contributingauthor=false
repo="https://github.com/gecos-lab/FracAbility"
docs="https://fracability.readthedocs.io/en/latest/"
+++

![logo](/fracability/logo.png)


Fracture networks are essential for the analysis and modelling of mechanical and hydraulic properties of rock masses. Recently, the use of Digital Outcrop Models (DOMs) provided a solid framework for the collection of large and quantitative datasets from which different properties can be extracted. Because of the complex nature of exposed rock outcrops, statistical model fitting can sometimes be challenging. Areas covered by rock debree, vegetation patches or simply the outer boundaries of the outcrop can introduce right-censoring bias and can often lead to parameter underestimation. Tools are needed to correct for estimating the correct distribution parameters while taking into account this bias. Survival analysis techniques, although usually applied in function of time and not length, accomplishes exactly this.

FracAbility is a Python toolbox that can be used to analyse fracture networks and estimate length distributions considering and correcting the effect of right-censoring using survival analysis. This package provides tools to:

+ Define the topology of fracture networks
+ Estimate multiple fracture length distributions while taking into consideration right censoring effects.
+ Provide methods to choose the most representative distribution using both a visual and a quantitative approach

Please refer to the [Docs](https://fracability.readthedocs.io/en/latest/) for a more in depth introduction to the problem, theoretical background, examples and API overview. 

Check out the repo on Github! [https://github.com/gecos-lab/FracAbility](https://github.com/gecos-lab/FracAbility)