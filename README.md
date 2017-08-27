# DMCat

![Full Sky J](https://github.com/bsafdi/DMCat/blob/master/plots/jfactors.png "Full Sky Map of Extragalactic J-factors")

This is a repository for the full-sky catalog of DM annihilation and decay factors for nearby galaxies, outside of the local group, presented in arxiv:XXXXXX.  If this catalog contributes to a publication, please cite arxiv:XXXX.  DMCat is a catalog of extragalactic signatures of beyond-the-standard model physics in the dark sector that is built from the galaxy group catalogs arxiv:1503.03134 and arxiv:1705.08068.  

## Citing this work

If this catalog contributes to a publication, please cite the original paper arxiv:XXXX, along with the galaxy group catalogs that DMCat is based on: arxiv:1503.03134 and arxiv:1705.08068.  Please also check the `contributors.txt` file to see if there are any new contributions that are relevant for citation.

## Extending and Modifying this Catalog

`DMCat` is meant to be a living catalog.  If you feel there is an error in `DMCat`, an entry can be updated with a more precise value, or new groups can be added to the catalog, we encourage you to do so!  Please do this via a `Pull request`.  Then, add your name to the `contributors.txt` list, along with a brief description of your contribution and a link to any relevant publication, so that your contribution may be properly acknowledged.   

## Loading the Catalog

In `Python`, we recommend loading the catalog through the commands

```python
from astropy.io import ascii
DMCat =  ascii.read("DMCat.txt").to_pandas()
```

## The Catalog: `DMcat/DMCat.txt`

### Units

All J-factors (for annihilation) have units of `GeV^2 cm^-5 sr`, all D-factors (for decay) have units of `GeV cm^-2 sr`, all masses are in units of `solar mass`, all distances are in `Mpc`, and all angles are in `degrees`.


### Entries

`DMCat/DMCat.txt` consists of the following entries:
	
1.  `Name`: the known group name, if one exists.
2.  `mulog10J_inf`: `log_{10}` of the inferred J factor, using the fiducial boost factor in arxiv:XXXX.  This boost factor is calculated assuming the NFW DM profile.
3.	`siglog10J_inf`: the standard error on the measurement of `mulog10J_inf`, in log space.
4.  `mulog10Jnb_inf`: the same as 2., except without the boost factor.
5. `siglog10Jnb_inf`: the same 3., except without the boost factor.
6. `mulog10JB_inf`: the same as 2., except assuming the Burkert DM profile.
7. `siglog10JB_inf`: the same as 3., except assuming the Burkert DM profile.
8. `mulog10JBnb_inf`: the same as 4., except assuming the Burkert DM profile.
9. `siglog10JBnb_inf`: the same as 5., except assuming the Burkert DM profile.
10. `mulog10D_inf`: `log_{10}` of the inferred decay factor `D`.
11. `siglog10D_inf`: the standard error on the measurement of `mulog10D_inf`, in log space.
12. `log10Mvir_inf`: `log_{10}` of the inferred virial mass.
13. `z`: redshift
14. `Nest`: 
15. `Ng`: the number of galaxies in the galaxy group
16. `l`: Galactic longitude of the central galaxy.
17. `b`: Galactic latitude of the central galaxy.
18. `cvir_inf`: the inferred central concentration parameter.
19. `rvir_inf`: the inferred virial radius.
20. `rs`: the inferred NFW scale radius.
21. `ID_2MASXJ`:
22. `Bib_z`:
23. `GName`: known name of the central galaxy, if one exists.
24. `ang_ext`: 
25. `theta_vir`:
26. `log10M200_inf`: `log_{10}` of the inferred `M_200` mass.
27. `ra`: right ascension of central galaxy.
28. `dec`: declination of central galaxy.
29. `dA`: distance to central galaxy.


