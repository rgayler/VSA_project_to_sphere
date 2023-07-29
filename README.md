# VSA_project_to_sphere

<!-- badges: start -->

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

<!-- badges: end -->

This is the work of [Ross W. Gayler](https://www.rossgayler.com/) and [Jeff Orchard](https://cs.uwaterloo.ca/~jorchard/).

This repository generates a [Quarto website](https://quarto.org/docs/websites) that demonstrates the action of [Vector Symbolic Architecture](https://www.hd-computing.com/) operators by projecting the hypervectors to the surface of a sphere.
We hope that this will help people to get a better intuitive understanding of Vector Symbolic Architectures.

The website generated from the rendered project documents is at <https://rgayler.github.io/VSA_project_to_sphere/>

------------------------------------------------------------------------

This is an open, shareable, reproducible, computational research project.
The point of making it an open, shareable, reproducible project is that anyone should be able to copy it, reproduce the analyses, and try out modifications (although we suspect that the vast majority of people who find this website will only want to read it).

**All materials other than code** are released under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

**Code** is released under the [MIT license](https://choosealicense.com/licenses/mit/).

## Project organisation

-   All the computational work and document preparation is done with the [R](https://www.r-project.org/) statistical computing environment and the [RStudio](https://posit.co/products/open-source/rstudio/) integrated development environment.

-   The entire research project is contained in a single directory that corresponds to an RStudio R project.

-   The project is structured as a [Quarto website](https://quarto.org/docs/websites).

-   The [`renv`](https://rstudio.github.io/renv/) package is used to manage the R package versions used by the project

-   The project code and documents are shared publicly on GitHub at <https://github.com/rgayler/VSA_project_to_sphere>

-   The website generated from the rendered project documents is at <https://rgayler.github.io/VSA_project_to_sphere/>

## Project directory structure

### `renv` directory

The [`renv`](https://rstudio.github.io/renv/) package keeps track of the R packages (and their versions) used by the project.
It allows anyone to reinstate the same packages and versions in their local copy of the project.
`renv` does *not* address system dependencies (e.g. R version, system libraries), so if these are critical you will need to find a workaround.

The `renv` directory contains the information need by `renv` to reinstate the local package environment.

### `docs` directory

The rendered static website is stored in the `docs` directory so that it can be served by GitHub pages.
This website is served on the internet at <https://rgayler.github.io/VSA_project_sphere>

### `.gitignore`

`.gitignore` in the R project root directory is used for all the manually created entries, so that all the manual rules are in one place.
Packages, such as `renv`, may create their own `.gitignore` files in subdirectories that they manage.

## Installation

This assumes that you already have current versions of R and RStudio installed.

1.  Clone the project repository <https://github.com/rgayler/VSA_project_to_sphere> from GitHub

2.  Open the cloned repository as an RStudio project

You can combine steps 1 and 2 using RStudio by creating a new project from the GitHub repository:\
`File | New Project... | Version Control | Git | Create Project`

When you open the project you will get warning messages about packages not being installed.
This is because you need to use the [`renv`](https://rstudio.github.io/renv/) package to reinstate the packages that are used by the project.

1.  Install [`renv`](https://rstudio.github.io/renv/) in that project if it is not already installed

2.  Use `renv::restore()` to install all the needed packages in the project-specific library:

    ```         
    renv::restore()
    ```
