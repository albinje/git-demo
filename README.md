## Tools for Cosmological Parameter Estimation


## 3D - Two-point correlation function with TreeCorr

With TreeCorr, to get 3d-2pcf, one has to use the metric (metric defining space) - 'Rperp'. Currently, 2D binning is not possible with this metric.

**Input format** - (ra, dec, r) where r is the comoving distance.

In the Rperp metric, the metric separation is $r_{\perp}$. Even though 2D binning is not available with Rperp, there is an argument called 'min_rpar' and 'max_rpar' through which we can loop over r_par.

For our case with input format = (ra, dec, z), we can restrict to pairs that are separated by a particular redshift range by using (min_rpar, max_rpar). Then we have to do binning in $r_{\perp}$ ( by defining min_sep, max_sep, bin_width). 

In the output of TreeCorr 2pcf, we get $\xi$ as a function of $r_{\perp}$ ($\delta \theta$)) for the choice of (min_rpar, max_rpar), which we have defined earlier.

For a test, I used the input data set (DES sim data) provided with TreeCorr, which has 390k objects with (ra, dec, z).




The plot depicts 2pcf vs $r_{\perp}$ for various redshift ranges.


This github attempts to collects all open source packages for cosmological parameter estimation.

---
## Table of Contents
#### Section List
- [Cobaya](#cobaya)
  - [Installation](#cobaya_install)
- [CosmoMC](#cosmomc)
  - [Installation](#cosmo_install)
- [Monte Python](#monte)
  - [Installation](#monte_install)


<a name='cobaya'></a>
## Cobaya
Cobaya (code for bayesian analysis, and Spanish for Guinea Pig) is a framework for sampling and statistical modelling: it allows you to explore an arbitrary prior or posterior using a range of Monte Carlo samplers (including the advanced MCMC sampler from CosmoMC, and the advanced nested sampler PolyChord). The results of the sampling can be analysed with GetDist. It supports MPI parallelization (and very soon HPC containerization with Docker/Shifter and Singularity).
<a name='cobaya_install'></a>
#### Installation

https://cobaya.readthedocs.io/en/latest/   | https://cobaya.readthedocs.io/en/latest/installation_cosmo.html


<a name='cosmomc'></a>
## CosmoMc
Cosmological Monte Carlo 
<a name='cosmo_install'></a>
#### Installation

https://cobaya.readthedocs.io/en/latest/   | https://cobaya.readthedocs.io/en/latest/installation_cosmo.html

<a name='monte'></a>
## Monte Python
Another tool for parameter estimation
<a name='monte_install'></a>
#### Installation

https://cobaya.readthedocs.io/en/latest/   | https://cobaya.readthedocs.io/en/latest/installation_cosmo.html

----
| Installation  | Website |
| ------------- | ------------- |
| https://cobaya.readthedocs.io/en/latest/installation_cosmo.html  | https://cobaya.readthedocs.io/en/latest/  |
| new cell1  | new cell  |

