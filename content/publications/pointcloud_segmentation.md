+++
date = '2023-04-23'
draft = false
title = 'Point cloud analysis and segmentation procedures in the PZero software'
tags = ["poster"]
description = "EGU23 poster"
showdate = true
showtags = false
openaccess=true
pub=false
firstauthor=true
contributingauthor=false
link="https://meetingorganizer.copernicus.org/EGU23/EGU23-9549.html"
posterorpresentation = true
weight=2
toc=true

+++

{{< linkTo link="/pointcloud_segmentation/poster.pdf" display="Poster" >}}

## Abstract

With the rapid increase in computing power, 3D modelling and efficient visualization of complex geological features has become more common and accessible. We propose a new point cloud visualization and data analysis module for the open source 3D geomodelling software PZero (https://github.com/andrea-bistacchi/PZero) with the goal to carry out geological, and in particular structural, analysis on Digital Outcrop Models (DOMs). A solid codebase was implemented in PZero to import and analyse DOM data enabling the users to:

+ Import and visualize dense point cloud data sets
+ Calculate normals data if missing
+ Pick plane orientation
+ Segment the point cloud both manually and semi-automatically

The possibility to study and extrapolate properties from dense point clouds directly in a geomodelling software is a big advantage. Bistacchi et al. (2015) demonstrated that carrying out DOM analysis within a geomodelling package improves both the precision and the accuracy of the resulting 3D model, while Martinelli et al. (2020) demonstrated that reservoir-scale characterization could be carried out starting from the analysis of km-scale DOMs.

The open nature of PZero and the readability of its Python code, offers a clear advantage over other closed alternatives in terms of ease of editing and writing new functions. Moreover PZero is robust and efficient in visualizing dense datasets, allowing to easily render on a laptop point clouds reaching hundreds of millions of points. As a result large high-resolution DOMs can be exploited to map complex structures or to carry out dense statistical analysis at the reservoir scale. By including the DOM workflow in a geomodelling package, geologists can approach the modelling problem with new valid tools and techniques and seamlessly include in the final model quantitative and statistically robust properties.


## How to cite

Benedetti, G., Casiraghi, S., Bistacchi, A., Arienti, G., and Bertolo, D.: Point cloud analysis and segmentation procedures in the PZero software, EGU General Assembly 2023, Vienna, Austria, 23–28 Apr 2023, EGU23-9549, https://doi.org/10.5194/egusphere-egu23-9549, 2023. 

```bibtex
@inproceedings{benedetti2023point,
  title={Point cloud analysis and segmentation procedures in the PZero software},
  author={Benedetti, Gabriele and Casiraghi, Stefano and Bistacchi, Andrea and Arienti, Gloria and Bertolo, Davide},
  booktitle={EGU General Assembly Conference Abstracts},
  pages={EGU--9549},
  year={2023}
}
```