+++
date = '2022-10-05'
title = 'New tools for Digital Outcrop Models analysis: Implementation for the PZero software'
tags = ["thesis"]
description = "Masters thesis"
showdate = true
showtags = false
openaccess=true
pub=false
firstauthor=true
contributingauthor=false
link=""
posterorpresentation = false
thesis=true
weight=3
toc=true

+++
{{< linkTo link="/msc/thesis.pdf" display="Thesis" >}}


## Introduction
The main goal of this thesis is to add a new point cloud data analysis module to the
open source 3D geomodelling software PZero (https://github.com/andrea-bistacchi/PZero) with the objective to carry out geological, and in particular structural, analysis
on Digital Outcrop Models (DOMs). There are many benefits related to the use of
DOM based analysis. These types of models are able to represent with centimetric
to millimetric precision extended rock outcrops thus enabling anyone to visualize and
explore from different points of view the given region without the need to be physically
present. Moreover these types of analysis offer the possibility to extrapolate with high
precision robust statistical and dense quantitative data from the outcrop on a scale
much bigger than the on site techniques.
At the moment, the state of the art for point cloud based analysis is CloudCom-
pare. This free and open-source software is able to import different types of data formats
(.las/.laz, .csv, .ply and more) and efficiently visualize dense point clouds. Moreover
there are many tools that can be used to both filtering data in different ways to clean
the point cloud from outliers and calculate properties from the raw data such as nor-
mals, curvature or point density distribution and more. In addition CloudCompare
(since version 2.9) can be used to carry out computer-assisted digitization of structural
traces in point clouds improving by a range of 35-66% the effort needed to extract geo-
logical properties from three-dimensional dense datasets (Thiele et al. 2017). Using the
compass tool geologists now can measure orientation data for exposed planar features
such as fractures, bedding surfaces and more. Once a high number of planes are locally
measured the user can automatically segment the rest of the point cloud and precisely
isolate surfaces. The possibility to study and extrapolate properties from dense point
clouds directly in a geomodelling software is a big advantage. Bistacchi et al. (2015)
demonstrated that unifying point cloud-based analysis with model driven approaches
for geomodelling improves both the precision and the accuracy of the resulting 3D
model, while Martinelli et al. (2020) demonstrated that reservoir-scale characterization
could be carried out starting from the analysis of Km-scale DOMs.
This thesis resulted in a solid code base for PZero to import and analyse DOM data
but also presents a draft workflow to replicate in PZero the already established pipeline
that in CloudCompare is used to automatically segment and classify fracture sets in
the digital outcrop.