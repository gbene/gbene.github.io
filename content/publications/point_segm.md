+++
date = '2023-09-21'
title = 'Methods for merging fragmented facets obtained from point cloud segmentation algorithms.'
tags = ["presentation"]
description = "Joint congress SIMP, SGI, SOGEI, AIV. | Potenza, Italy"
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

{{< linkTo link="/point_segm/presentation.pdf" display="Presentation" >}}


## Abstract
With the new point cloud visualization and data analysis module for the open source 3D geomodelling software PZero (Bistacchi et al., 2021), it is now possible to import and analyse digital Outcrop Models (DOMs). Furthermore, the users are now enabled to carry out geological, and in particular structural, analysis on DOMs and replicate a working segmentation workflow, already tested in CloudCompare, to extrapolate fracture facets (i.e. the morphological expression of planar discontinuities on an outcrop face, Dewez et al., 2016). Our pipeline can be used to analyse fracture networks on outcrops with arbitrary orientation, but unfortunately, as an inevitable by-product of the segmentation procedure, continuous fracture facets are usually fragmented in multiple adjacent smaller polygons. This effect ultimately leads to skewing towards smaller values the estimation of statistical distributions of many important fracture network parameters, such as spacing, length, and height. Moreover, the results of topological analysis of fracture connectivity are completely distorted by this kind of problem. 

We propose new techniques and approaches to overcome these obstacles. The introduction of new geometrical and topological constraints, in addition to classical orientation parameters, can be used to identify which facet can be merged. We also implement new topological and spacing distribution analysis modules to extrapolate significant fracture set and network information, needed as input parameters for the creation of stochastic Discrete Fracture Networks models. 

By including these methods, new possible applications arise such as filtering and cleaning the model from “improper” facets, training more sophisticated algorithms to automate the merging process and calibrating fracture network parameters (such as P32). The open nature of PZero and the readability of its Python code, offers a clear advantage over other closed alternatives in terms of ease of editing and writing new functions. By embracing the open science philosophy, external revisions and contributions are encouraged, thus leading to a faster development cycle and quicker results. By including the DOM workflow in a geomodelling package, geologists can approach the modelling problem with new valid tools and techniques, seamlessly including in the final model quantitative and statistically robust properties (Bistacchi et al., 2015). 