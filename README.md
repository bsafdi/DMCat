# DMCat

This is a repository for the full-sky catalog of DM annihilation and decay factors for nearby galaxies, outside of the local group, presented in arxiv:XXXXXX.  If this catalog contributes to a publication, please cite arxiv:XXXX.  DMCat is a catalog of extragalactic signatures of beyond-the-standard model physics in the dark sector that is built from the galaxy group catalogs arxiv:1503.03134 and arxiv:1705.08068.  

## Citing this work

If this catalog contributes to a publication, please cite the original paper arxiv:XXXX, along with the galaxy group catalogs that DMCat is based on: arxiv:1503.03134 and arxiv:1705.08068.  Please also check the `contributors.txt` file to see if there are any new contributions that are relevant for citation.

## Extending and Modifying this Catalog

`DMCat` is meant to be a living catalog.  If you feel there is an error in `DMCat`, an entry can be updated with a more precise value, or new groups can be added to the catalog, we encourage you to do so!  Please then add your name to the `contributors.txt` list, along with a brief description of your contribution and a link to any relevant publication, so that your contribution may be properly acknowledged.   

## Loading the Catalog

In `Python`, we recommend loading the catalog through the commands

```python
from astropy.io import ascii
DMCat =  ascii.read("DMCat.txt").to_pandas()
```


