+++
date = '2021-05-01'
draft = false
title = 'Pydip'
tags = ["project"]
description = "Python program to generate random structural data such as planes, folds, faults and focal mechanisms."
showdate = true
showtags = false
link="https://github.com/gbene/pydip"
+++



Pydip is a python program with the main objective to give a stereoplot reading practice platform by generating random planes, folds, faults and focal mechanisms.

As a secondary future objective, for now not implemented, the software will be able to plot and elaborate structural measurements obtained on the field (similar to [Stereonet](https://www.rickallmendinger.net/stereonet)).

The plots are generated with [mplstereonet](https://mplstereonet.readthedocs.io/en/latest/mplstereonet.html) library.

## Capabilities

### Generate multiple random sets of planes
{{% figure src="/pydip/1.png"%}}

The program chooses a random dip direction and angle for every set and depending on that plane the planes will be generated with a normal distribuition with a random std value.

The parameters that can be tweaked are:

+ Number of sets
+ Number of planes
+ Plot planes and/or poles

### Generate multiple random sets of folds
{{% figure src="/pydip/2.png"%}}

The program can generate n sets of random planes that follow random cilindrical fold parameters (axial plane and hinge line inclination etcetc).

The parameters that can be tweaked are:

+ Number of sets of folds
+ Number of planes for every fold limb
+ Plot limb planes and/or poles
+ Plot plane axis and/or hinge line

### Generate random focal mechanisms
{{% figure src="/pydip/3.png"%}}



### Data table view and selection
{{% figure src="/pydip/4.png"%}}
