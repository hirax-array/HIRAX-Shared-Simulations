# Survey Description

- 49 array elements in a 7x7 square grid with 6m spacing
- Boosted redundancy factor by 20x to emulate 1000 element sensitivity
- 64 frequency bands from 550-650 MHz
- 7 pointings from -10 to +10 degrees off zenith at -30 degree latitude
- mmax = lmax = 400
- Simple Gaussian beam with FWHM = lambda/6m
- Tsys = 50K with nominal sensitivity equivalent to 120days per pointing

# Outputs Produced

## Products

- Beam Transfer Matrices
- SVD Decompositions
- A large set of KL transform modes with different thresholds

## Pipeline

- SVD Maps
- KL Maps
- Timestreams with 21cm + galactic foregrounds with and without thermal noise

# Repository Statuses

- hirax-transfer: [f91a79](https://github.com/hirax-array/hirax_transfer/commit/f91a7938004302be20673be399ba3c4b53e16219)
- driftscan: [3947b3](https://github.com/hirax-array/driftscan/commit/3947b3fe57725ca51ecee0f88c7f1816ccadcf85)
- cora: [f2b256](https://github.com/radiocosmology/cora/commit/f2b25635b80ae5fb3adf4fd37ec11fd248f2f885)
- caput: [47736b](https://github.com/radiocosmology/caput/commit/47736b574062020fcb76c9351d33b8c18b85ad23)

# Approximate Runtimes

Products step run on 20 x 20 core nodes on hippo

- Beam transfer and SVDs: ~19.25hr
- KL Transforms: ~13hr

Pipeline steps run on 10 x 20 core nodes on hippo

- Timestreams and maps: ~12hr


