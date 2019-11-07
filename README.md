# Installation

The easiest way to install all the required packages is to use the provided `conda_environment/environment.yml` to
initialise a conda environement. If you have anaconda or miniconda installed you should just be
able to do:

`conda env create --name=hirax_sims -f environment.yml`

Then you can swicth to this environment with

`conda activate hirax_sims`

Note that this will install `caput`, `cora`, `driftscan`, `draco` and `hirax_transfer` from their
git repositories/forks from the hirax-array github collaboration. If you will be modifying code
from these repos, you might want to keep separately maintained and manually install repos.

# Typical Workflow

Generally there are two steps to running simulations.

First you generate the beam transfer matrices and associated products with:

`drift-makeproducts run prod_params.yaml`

And then these products can be used to generate simulated data and science products using
either drift-runpipeline:

`drift-runpipeline run pipe_params.yaml`

or using caput-pipeline to run analysis tasks from draco, e.g.:

`caput-pipeline run config_draco.yaml`

The latter is the preferred method going forward. See below for a brief description of the
some standard configuration files.

# Configuration Files

The configuration files in this repo and their associated descriptions represent the setup for
simulation runs whose outputs are considered useful. Additionally there are some small scale
simulation configurations in the `test_configs` directory for test running the code.

TODO: Configuration file explanation

