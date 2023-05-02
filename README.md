About refinitiv-data-feedstock
==============================

Feedstock license: [BSD-3-Clause](https://github.com/conda-forge/refinitiv-data-feedstock/blob/main/LICENSE.txt)

Home: https://developers.refinitiv.com/en/api-catalog/refinitiv-data-platform/refinitiv-data-library-for-python

Package license: Apache-2.0

Summary: Client for Refinitiv Data Platform API's

Development: https://developers.refinitiv.com/en/api-catalog/refinitiv-data-platform/refinitiv-data-library-for-python/tutorials

Documentation: https://developers.refinitiv.com/en/api-catalog/refinitiv-data-platform/refinitiv-data-library-for-python/documentation

The Refinitiv Data Library for Python provides a set of ease-of-use interfaces offering your applications a uniform access to the breadth and depth of financial data and services available on the Refinitiv Data Platform.

With this library, the same Python code can be used to retrieve data whatever the access point you choose to connect your application to the Refinitiv Data Platform. It can be either via a direct connection, via Eikon, via Refinitiv Workspace, via CodeBook or even via a local Real-Time Distribution System.

The library provides several abstraction layers enabling different programming styles and technics suitable for all developers from Financial Coders to Seasoned Developers:

 - Using the Access layer is the easiest way to get Refinitiv data. The Access layer provides simple interfaces allowing you to rapidly prototype solutions within interactive environments such as Jupyter Notebooks. It has been designed for quick experimentation with our data and for Financial Coders specific needs.
 - The Content layer is the basement of the Access layer. It provides developers with interfaces suitable for more advanced use cases (synchronous function calls, async/await, event driven). The Content layer refers to logical market data objects like market data prices and quotes, fundamental & reference data, historical data, company research data and so on.
 - The Delivery layer is a low abstraction layer that defines interfaces used to interact with service agnostic delivery mechanisms of the Refinitiv Data Platform. The Delivery layer is a foundational component of the Content layer.
 - The Session layer defines interfaces allowing your application to connect to the Refinitiv Data Platform via different access points (either via a direct connection, via Eikon, via the Refinitiv Workspace, via CodeBook or even via a local Real-Time Distribution System).


Current build status
====================


<table><tr><td>All platforms:</td>
    <td>
      <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=18629&branchName=main">
        <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/refinitiv-data-feedstock?branchName=main">
      </a>
    </td>
  </tr>
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-refinitiv--data-green.svg)](https://anaconda.org/conda-forge/refinitiv-data) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/refinitiv-data.svg)](https://anaconda.org/conda-forge/refinitiv-data) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/refinitiv-data.svg)](https://anaconda.org/conda-forge/refinitiv-data) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/refinitiv-data.svg)](https://anaconda.org/conda-forge/refinitiv-data) |

Installing refinitiv-data
=========================

Installing `refinitiv-data` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
conda config --set channel_priority strict
```

Once the `conda-forge` channel has been enabled, `refinitiv-data` can be installed with `conda`:

```
conda install refinitiv-data
```

or with `mamba`:

```
mamba install refinitiv-data
```

It is possible to list all of the versions of `refinitiv-data` available on your platform with `conda`:

```
conda search refinitiv-data --channel conda-forge
```

or with `mamba`:

```
mamba search refinitiv-data --channel conda-forge
```

Alternatively, `mamba repoquery` may provide more information:

```
# Search all versions available on your platform:
mamba repoquery search refinitiv-data --channel conda-forge

# List packages depending on `refinitiv-data`:
mamba repoquery whoneeds refinitiv-data --channel conda-forge

# List dependencies of `refinitiv-data`:
mamba repoquery depends refinitiv-data --channel conda-forge
```


About conda-forge
=================

[![Powered by
NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](https://numfocus.org)

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[Azure](https://azure.microsoft.com/en-us/services/devops/), [GitHub](https://github.com/),
[CircleCI](https://circleci.com/), [AppVeyor](https://www.appveyor.com/),
[Drone](https://cloud.drone.io/welcome), and [TravisCI](https://travis-ci.com/)
it is possible to build and upload installable packages to the
[conda-forge](https://anaconda.org/conda-forge) [Anaconda-Cloud](https://anaconda.org/)
channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](https://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating refinitiv-data-feedstock
=================================

If you would like to improve the refinitiv-data recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/refinitiv-data-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@Mhoian](https://github.com/Mhoian/)
* [@PFaurel](https://github.com/PFaurel/)

