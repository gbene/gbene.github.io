+++
date = '2020-12-20'
draft = false
title = 'Pyseismic'
tags = ["project"]
description = "Visual SUNT style application written in python."
showdate = true
showtags = false
link="https://github.com/gbene/pyseismic"
toc=true

+++


## The premise

Pyseismic is a simple python interface created to visualize and process seismic traces based on the [Obspy](https://docs.obspy.org/) package.

The aim of this project is to create a simple alternative to the more complex and costly Visual SUNT that can be used to do basic taks without the need to buy professional softwares. Since is entirely written in pyhon it can be run on every platform (Visual SUNT is only on Windows D:).

## Capabilities

For now there are very few functions available (the essentials). In particular:

+ Read and plot with matplotlib seismic traces from files supported on Obspy
{{% figure src="/pyseismic/1.png"%}}
+ Apply FFT analysis on single or multiple traces
{{% figure src="/pyseismic/2.png"%}}
+ Basic filtering (band pass, low and high pass)
{{% figure src="/pyseismic/3.png"%}}
+ First break picking with options of live dromochrome plot.
{{% figure src="/pyseismic/4.png"%}}


