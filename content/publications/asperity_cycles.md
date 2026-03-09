+++
date = '2025-04-27'
draft = false
title = 'Asperity cycle simulation using observed seismicity: Applications to the Bárðarbunga caldera'
tags = ["publication"]
description = "EGU25 poster"
showdate = true
showtags = false
openaccess=true
pub=false
firstauthor=true
contributingauthor=false
link="https://meetingorganizer.copernicus.org/EGU25/EGU25-13050.html"
posterorpresentation = true
weight=2
toc=true

+++
{{<linkTo link="/asperity/poster.pdf" display="Poster" >}}


## Abstract
Repeating earthquakes most often occur as frequent small magnitude events, with repeating time increasing with magnitude. The Bárðarbunga caldera however is a rare example where moderate magnitudes (Mw ≥ 5) repeat frequently. During the 6 months caldera collapse event (2014-2015), 77 Mw ≥ 5 earthquakes were recorded and, in the years following the collapse, observations show quasi-periodic Mw ≥ 5 events. Recent seismological field campaigns have provided further constraints on the caldera’s geometry, mapping out a ring fault structure and offering excellent depth constraints. The repetitive nature of the earthquake sequences and good structural controls, make this case especially suitable to investigate using Sequences of Earthquakes and Aseismic Slip (SEAS) models. Furthermore, the periodicity of the ring fault is well captured to the first order by adopting a Spectral Boundary Integral approach. To mimic the observed data, we project relatively relocated seismic events to a mesh representation of the ring fault; we then convert the projected point clusters into frictional parameter maps that define the distribution of the rate weakening and rate strengthening asperities in the simulation. Finally, we quantify the differences between the simulated results and the observed seismic data by comparing for example reoccurrence time, magnitudes and partial rupture characteristics. We use the JAX Python library to achieve well resolved simulations, realistic frictional parameters and domain size. This library provides tools such as Just-In-Time (JIT) and Ahead-Of-Time (AOT) compilation, automatic differentiation and vectorization, all of which significantly speed up runtime. Moreover, JAX provides a flexible framework for running code on different accelerators such as GPUs, drastically reducing code runtime for parallelizable operations such as FFT computations.


## How to cite

 Benedetti, G., Heimisson, E. R., Winder, T., and De Vries, Y. A.: Asperity cycle simulation using observed seismicity: Applications to the Bárðarbunga caldera, EGU General Assembly 2025, Vienna, Austria, 27 Apr–2 May 2025, EGU25-13050, https://doi.org/10.5194/egusphere-egu25-13050, 2025. 

```bibtex
@inproceedings{benedetti2025asperity,
  title={Asperity cycle simulation using observed seismicity: Applications to the B{\'a}r{\dh}arbunga caldera},
  author={Benedetti, Gabriele and Rafn Heimisson, El{\'\i}as and Winder, Tom and De Vries, Ylse Anna},
  booktitle={EGU General Assembly Conference Abstracts},
  pages={EGU25--13050},
  year={2025}
}
```