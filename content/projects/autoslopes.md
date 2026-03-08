+++
date = '2020-10-25'
title = 'Automatic processing for referenced slopes'
tags = ["project"]
description = "Compute the difference between two referenced slopes reconstructed in Metashape Professional."
showdate = true
showtags = false
link="https://github.com/gbene/Python-orders/tree/main/25_11_2020"
+++


## Automatic processing for referenced slopes

The premise

This project was a request aimed to find a way to prepare different 3D models, in particular artificial slopes, and calculate the difference between two reconstructions after a given event directly in metashape without using external programs.

In particular the set of scripts needed to achive the following tasks:

+ Apply different masks for different sets of photos.
+ Count the total number of markers detected in all of the uploaded photos. The number of markers needed to be in total always 135.
+ Cut the resulting point clouds with constant dimensions and automatically apply a rotatation to make the plane horizontal.
+ Calculate the difference between two meshes. To make sure that the difference operation was applied properly the two chunks need to be aligned and the models need to be rotated flat and cropped.


{{% figure src="/autoslope/og_img.png" title=" Input image example "%}}
{{% figure src="/autoslope/slope_a2.png"%}}
{{% figure src="/autoslope/slope_b2.png" title="  Reconstructed slope before and after the event "%}}



## Summary

### Mask application

The model is constructed using photos that capture a different angle of the artificial plane. The first step is to isolate the relevant slope information by masking the parts of the slope that are not needed for the reconstruction (e.g. the container). To do this different masks were created to mask specific parts present in different sets of photos. The pairing is as follows:

+ photo 1 "Links_Initial.jpg"
+ photo 2 to 21 "Links_Regular.jpg"
+ photo 22 "Midden_Initial.jpg"
+ photo 23 to 42 "Midden_Regular.jpg"
+ photo 43 "Rechts_Initial.jpg"
+ photo 44 to 63 "Rechts_Regular.jpg"

This process was accomplished by writing the `mask.py` script.

### Marker count

For each model there is a known fixed number of total markers that need to be detected (135). The objective of this script is to count the total amount of markers detected in the model and print if there are less than 135. This check is done to see if the automatic markers present for each markers are somehow cropped or masked out.

The check process was automated using the `check_markers.py` script

### Cut and rotate the model point cloud

To apply correctly the difference between the two models they both need to have the same size, position and rotation. To do this it was decided to rotate first the psarse cloud model and then resize the bounding box to a determined size. To do this the following process was defined:

+ Define the region size
+ Find the minimum and maximum (for both x and y) points inside the bounding box and calculate the center (as the midpoint of points at opposite corners).
+ Translate the points on the same height of the center point
+ Set these points as tranform reference
+ Update transform (and so rotate the points)
+ Resize the bounding box

To accurately rotate the model the plane needs to fit in the bounding box as tightly as possibile and so the z value need to be low. Too low z values can crop too much of the plane (since the plane has a certain inclination angle) and so the rotation won’t be as precise.

This process is archived by using the `region_size.py` script.

### Mesh difference

Instead of caluclating the difference of the two meshes a quicker is to convert the meshes in Digital Elevation Models and then apply a per pixel difference.

## Final results and pipeline

{{% figure src="/autoslope/dem_a.png"%}}
{{% figure src="/autoslope/dem_b.png" title="Reconstructed DEM of the slope before and after the event"%}}
{{% figure src="/autoslope/diff2.png" title="DEM difference"%}}


![Pipeline](/autoslope/auto_slope_processing.png)