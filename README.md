## Tools for Cosmological Parameter Estimation

    def write_patch_centers(self, file_name):
        """Write the patch centers to a file.

        The output file will include the following columns:

        ========      =======================================================
        Column        Description
        ========      =======================================================
        patch         patch number (0..npatch-1)
        x             mean x values
        y             mean y values
        z             mean z values (only for spherical or 3d coordinates)
        ========      =======================================================

        It will write a FITS file if the file name ends with '.fits', otherwise an ASCII file.

        Parameters:
            file_name (str):    The name of the file to write to.
        """
        self.logger.info('Writing centers to %s',file_name)

        centers = self.patch_centers
        col_names = ['patch', 'x', 'y']
        if self.coords != 'flat':
            col_names.append('z')
        columns = [np.arange(centers.shape[0])]
        for i in range(centers.shape[1]):
            columns.append(centers[:,i])

        with make_writer(file_name, precision=16, logger=self.logger) as writer:
            writer.write(col_names, columns)


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

