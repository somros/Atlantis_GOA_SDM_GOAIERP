# Spatial distributions from GOAIERP with `sdmTMB`

This code produces distribution maps of GOA species from GOAIERP surface trawl surveys and the `sdmTMB` [package](https://github.com/pbs-assess/sdmTMB) (Anderson et al. 2022), to inform Atlantis GOA initial conditions and seasonal distributions (i.e., S1-S4 parameters). These (from GOAIERP data) will only be used for some stages of some species, like herring and juvenile salmon. See [here](https://github.com/somros/Atlantis_GOA_SDM_coupling_and_initbiom) for details.

This code performs 3 tasks:

1. Using the stage definitions in the data (Jamal Moss pers. comm.), it calculates the CPUE of juveniles and adults at each haul location. No length-weight relationship is used here for ontogenetic allocation.
2. Loads CPUE data into a knitter file, which subsets to the species of interest.
3. Runs the `sdmTMB` routine: fits the model, produces figures, output tables and validation metrics by species and stage. 

The output tables will be open [here](https://github.com/somros/Atlantis_GOA_SDM_coupling_and_initbiom) to get final distributions and biomasses.

__References__

Anderson, S.C., E.J. Ward, P.A. English, L.A.K. Barnett. 2022. sdmTMB: an R package for fast, flexible, and user-friendly generalized linear mixed effects models with spatial and spatiotemporal random fields. bioRxiv 2022.03.24.485545; doi: https://doi.org/10.1101/2022.03.24.485545