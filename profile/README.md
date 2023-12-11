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
For a complete step-by-step guide please see the further documentation.

### Repositories

As described above, each repository in this organisation contains a specific piece
of software.
It is likely users will want several of these.
We advise creating a single directory, e.g. `go-ship/` and cloning any repositories
inside this.

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
Where possible<sup>1</sup>]
we recommend a single virtual environment for all GO-SHIP codes.

To create a virtual environment run:
```bash
python3 -m venv gs-venv
```
This will create the directory `gs-venv` with the relevant contents.  
The environment can then be 'activated' with:
```bash
source gs-venv/bin/activate
```
and you will see `(gs-venv)` appear by your terminal prompt.  
You can then carry out work as usual. When finished deactivate the environment with:
```bash
deactivate
```
You will need to reactivate each time you come to do work.
It will remain exactly as you left it, with all previously installed software packages
available.

As with data, we advise placing the virtual environment adjacent to the cloned
repositories inside `go-ship/`.

<sup>1</sup> _It may be that multiple environments are required if any packages have 
conflicting dependencies. In this case you should create a separate environment for the
conflicting tool, and activate it instead when using that tool._

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

There are some guidelines for developers available in an additional document.
