<!-- markdownlint-disable MD041 -->

## Supported platforms

`linux/amd64` platform `debian`, `ubuntu:focal` and `ubuntu:jammy`.

If the `useTesting` is `true`, `linux/arm64` platform `debian` also supported.

## R package installation

### Binary installation via apt

This feature will configure apt to install R and R packages.

Packages that can be installed via apt can be displayed with the following command.

```sh
apt-cache search "^r-.*" | sort
```

For example, the following command installs the `dplyr` package.

```sh
apt-get -y install --no-install-recommends r-cran-dplyr
```

Thanks to [r2u](https://eddelbuettel.github.io/r2u/), on Ubuntu,
all packages on CRAN and BioConductor can be installed via apt.

### Source installation via R

Packages that cannot be installed via apt must be installed using the R functions.

For more information, please check [the Rocker Project website](https://rocker-project.org/use/extending.html).

## Python package installation

This feature has some options to install Python packages such as `jupyterlab`.
When installing Python packages, if `python3 -m pip` is not available, it will install `python3-pip` via apt.
