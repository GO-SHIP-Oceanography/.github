# ![](https://avatars.githubusercontent.com/GO-SHIP-Oceanography?size=28) GO-SHIP Oceanography

This organization contains
[various repositories](https://github.com/orgs/GO-SHIP-Oceanography/repositories)
for utilities that are used on physical oceanography cruises.

The software provided here is community-developed, free, and open-source.
It has been collated under the [GO-SHIP](https://www.go-ship.org/) program, but is
open to anyone to download and use.


## Usage

Each [repository](https://github.com/orgs/GO-SHIP-Oceanography/repositories) under
this organisation represents a single tool for use on cruise.

The sections below contain general advice for getting set on a cruise computer.  
For a complete step-by-step guide please see the
[detailed setup documentation](setup.md).

### Repositories

As described above, each repository in this organisation contains a specific piece
of software.
It is likely users will want several of these.
We advise creating a single directory, e.g. `go-ship/` and 
[cloning](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)
any repositories inside this.

### Data

A number of the scripts require large datasets, some of which overlap.
To avoid downloading these multiple times we suggest placing them in a single, common
location at which the scripts/programs point to.  
Instructions on how to do this are provided in the documentation for each repository.

We advise using a directory `data/` adjacent to the cloned repositories in `go-ship/`.

### Virtual Environments

It is strongly advised to run any python code from GO-SHIP inside a 
[virtual environment](https://docs.python.org/3/library/venv.html).
This helps to isolate dependencies and keep your system clean.  
We recommend a single virtual environment for all GO-SHIP codes where possible.  
If you are not familiar with virtual environments, a full step-by-step guide is provided
in the [detailed setup documentation](setup.md).

As with data, we advise placing the virtual environment adjacent to the cloned
repositories inside `go-ship/`.

### Field preparation

If using these resources in the field there are a number of steps that should be taken
in advance of leaving port.

Internet and data access can be severely limited during a cruise, so ensure that you
have cloned all repositories and downloaded all datasets.

It is also strongly advised to familiarise yourself with using the tools and making
sure they work as expected on your computer.


## Contributions

Contributions are welcome from all members of the oceanography community.  
If you have code that you would like to add, or a request for code, please
[open an issue](https://github.com/GO-SHIP-Oceanography/.github/issues) with a
description and your contact details.

There are some guidelines for developers available in an
[additional document](contributing.md).

### Code of Conduct

Everyone participating in the GO-SHIP git Organisation, is expected to treat others
with respect and, more generally, to follow the guidelines articulated in the
[Python Community Code of Conduct](https://www.python.org/psf/conduct/).


## Licensing

Due to their varied origins the software under the GO-SHIP organisation is provided
under a range of different licenses.
Please see the individual repositories for details of the license attached to a specific
piece of software.


## People

The codes within the GO-SHIP Organization have been contributed by a number of authors.
Please see individual repositories for details of their authors and owners.

The GO-SHIP git organization is managed by 
Jack Atkinson ([@jackatkinson1000](https://github.com/jatkinson1000)) and
Laura Cimoli ([lcimoli](https://github.com/lcimoli)) of the
[ICCS](https://github.com/Cambridge-ICCS).
It was set up after Laura recognised the need for the research software on oceanographic
cruises to be more findable and re-usable.
