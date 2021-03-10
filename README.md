R + Jupyterlab [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/davidfastovich/R-Jupyter-Tutorial/main?urlpath=lab)

RStudio [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/davidfastovich/R-Jupyter-Tutorial/main?urlpath=rstudio)

Important caveat, this Binder instance is built on the conda-forge R-base environment. By using conda-forge R-base and conda-forge R packages we avoid having to compile CRAN R packages from source. If you've ever used R in Linux, you are aware of how long this can take for even a handful of R packages. This is compounded by the poor hardware resources Binder alots for every Jupyterlab instance (e.g. only 2 GBs of RAM). The speed at which a conda-forge environment builds in Binder is a large advantage, but we lose access to all CRAN R packages. conda-forge contains a large amount of the most popular CRAN packages, but less popular ones are not pre-compiled and hosted on conda-forge - neotoma being a key missing package. Not a problem through! If you find yourself wanting to produce a GitHub repository that works with Binder for reproducibility and still uses CRAN R packages follow this guide:

https://github.com/binder-examples/r

Briefly, the environment.yml file is replaced by runtime.txt and that tells Binder to build an environment from the MRAN R repository, which supports CRAN packages. This will take **much** longer to initialize, but it will work!
