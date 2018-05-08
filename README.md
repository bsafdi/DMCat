# DMCat

**A catalog of extragalactic dark matter halos and their annihilation and decay factors.**

[![arXiv](https://img.shields.io/badge/arXiv-1708.09385%20-green.svg)](https://arxiv.org/abs/1708.09385)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

![Full Sky J](https://github.com/bsafdi/DMCat/blob/master/plots/jfactors.png "Full Sky Map of Extragalactic J-factors")

DMCat is a repository for the full-sky catalog of dark matter (DM) annihilation and decay factors for nearby galaxies presented in [1708.09385](https://arxiv.org/abs/1708.09385). 
This is a catalog of extragalactic signatures of beyond-the-standard model physics in the dark sector 
that is built from the galaxy group catalogs [1503.03134](https://arxiv.org/abs/1503.03134) and 
[1705.08068](https://arxiv.org/abs/1705.08068).
Much of the formalism used to create this catalog derives from the work in [1709.00416](https://arxiv.org/abs/1709.00416).

## Citing this work

If this catalog contributes to a publication, please cite the original paper 
[1708.09385](https://arxiv.org/abs/1708.09385) and companion work [1709.00416](https://arxiv.org/abs/1709.00416), along with the galaxy group catalogs that DMCat is based on: [1503.03134](https://arxiv.org/abs/1503.03134) and 
[1705.08068](https://arxiv.org/abs/1705.08068).  
Please also check the `CONTRIBUTORS.txt` file to see if there are any new contributions that are relevant for citation.

## Extending and Modifying this Catalog

`DMCat` is meant to be a living catalog.  If you feel there is an error in `DMCat`, an entry can be updated with a more precise value, or new groups can be added to the catalog, we encourage you to do so!  Please do this via a pull request.  Then, add your name to the `CONTRIBUTORS.txt` list, along with a brief description of your contribution and a link to any relevant publication, so that your contribution may be properly acknowledged.   

A permanent copy of the original version of this catalog, as it was first used in [1708.09385](https://arxiv.org/abs/1708.09385), is maintained [here](https://dspace.mit.edu/handle/1721.1/111283).

## Loading the Catalog

In `Python`, we recommend loading the catalog as a Pandas DataFrame through the commands

```python
import pandas as pd
DMCat =  pd.read_csv("DMCat.csv")
```

## The Catalog: `DMCat/DMCat.csv`

### Units

All J-factors (for annihilation) have units of `GeV^2 cm^-5 sr`, all D-factors (for decay) have units of `GeV cm^-2 sr`, all masses are in units of `solar mass`, `dA` and `dc` distances are in `Mpc`, `rvir`, `rs`, and `r200` distances are in `kpc`, and all angles are in `degrees`.

### Entries

`DMCat/DMCat.csv` consists of the following entries:
	
1. `Name`: Name of the brightest central galaxy (BCG) from the T15 or T17 catalogs.
2. `GName`: Common group name associated to the group, if one exists, cross-referenced from the `CosmicFlows-3` catalog ([1605.01765](https://arxiv.org/abs/1605.01765)).
3. `mulog10J`: `log_{10}` of the inferred J-factor, using the fiducial boost factor in [1507.08656](https://arxiv.org/abs/1507.08656).  This boost factor is calculated assuming the NFW DM profile.
4. `siglog10J`: Standard error on the measurement of `mulog10J`, in log space.
5. `mulog10Jnb`: Same as 2., except without the boost factor.
6. `siglog10Jnb`: Same as 3., except without the boost factor.
7. `mulog10JB`: Same as 2., except assuming the Burkert DM profile.
8. `siglog10JB`: Same as 3., except assuming the Burkert DM profile.
9. `mulog10JBnb`: Same as 4., except assuming the Burkert DM profile.
10. `siglog10JBnb`: Same as 5., except assuming the Burkert DM profile.
11. `mulog10D`: `log_{10}` of the inferred decay factor `D`.
12. `siglog10D`: Standard error on the measurement of `mulog10D`, in log space.
13. `log10Mvir`: `log_{10}` of the inferred virial mass.
14. `sigmalog10Mvir`: Standard error on the measurement of `log10Mvir` in log space.
15. `cvir`: Inferred central concentration parameter using the model of [1502.00391](https://arxiv.org/abs/1502.00391).
16. `sigmalog10cvir`: The standard error on the measurement of `log10(cvir)` in log space.
17. `z`: Cosmological redshift.
18. `dA`: Angular diameter distance to the central galaxy.
18. `dc`: Comoving distance to the central galaxy.
19. `rvir`: Inferred NFW virial radius of the halo.
20. `rs`: Inferred scale radius of the halo.
21. `Ng`: Number of group members in the galaxy group.
22. `l`: Galactic longitude of the central galaxy.
23. `b`: Galactic latitude of the central galaxy.
24. `ra`: Right ascension of the central galaxy in the ICRS frame.
25. `dec`: Declination of the central galaxy in the ICRS frame.
26. `theta_s`: Angular extension associated with the halo scale radius.
27. `log10M200`: `log_{10}` of the inferred 200 mass.
28. `r200`: Inferred NFW 200 radius of the halo.
