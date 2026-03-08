+++
date = '2021-02-10'
draft = false
title = 'Rocpy'
tags = ["project"]
description = "Python port of RocPy"
showdate = true
showtags = false
link="https://github.com/gbene/rocpy"
+++


## The premise

RocLab is a very useful piece of free software written in 2011 for determining rock mass strength parameters, based on the generalized Hoek-Brown failure criterion (Hoek et al. 2002). The main problem is that it is discontinued and the only version is available for windows. With this project I want to archive the same objective as RocLab’s using python to increase the overall accessibility of the program and improve the plot’s interfaces (thanks to matplotlib).

## Capabilities

1. Calculate Hoek-Brown criterion parameters
2. Calculate Rock mass parameters ($\sigma_t$, $\sigma_c$, $\sigma_{cm}$, $E_{rm}$)
3. Calculate $\sigma^{max}_3$ based on different applications (e.g tunnels)
4. Calculate Mohr-Coulomb parameters ($c$ and $\phi$)
5. Plot H-B and M-C envelope.
6. Plot failure mohr circle and calculate the value.


{{% figure src="/rocpy/HB.png" title="Main view with the HB criterion plot"%}}
{{% figure src="/rocpy/HB_MC.png" title="Main view with the HB and MC criterion plot"%}}
{{% figure src="/rocpy/Mohr.png" title="Secondary view with the Mohr-Coulomb failure circle"%}}


## What is missing

+ Tabulated list values for D
+ Tabulated list values for $m_i$
+ Import data
+ Export data