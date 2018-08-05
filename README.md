# HexBinPlots

[![Build Status](https://travis-ci.org/RalphAS/HexBinPlots.jl.svg?branch=master)](https://travis-ci.org/RalphAS/HexBinPlots.jl)

`HexBinPlots.jl` provides hexbin histogram plots to the Plots/StatPlots ecosystem.

Example:

```julia
#Pkg.clone("git@github.com:RalphAS/HexBinPlots.jl.git")
using HexBinPlots
using Plots

N=10^4
x=randn(N)
y=randn(N)
hexbins(x,y,colorbar=true,color_palette=:viridis_r)
```

![example](https://user-images.githubusercontent.com/18298838/43689358-345450fa-98c7-11e8-86cc-6aad328fedf1.png)

Note: Plots does have a `hexbin` series type, but only for the PyPlot backend,
and it doesn't seem as versatile as this (the extra `s` here disambiguates).
`hexbins` requires `shape` and color gradient capabilities, so it
does not work with all backends.
