# Setup

This document contains step-by-step instructions for setting up the GO-SHIP codes
on a computer.

We assume a basic level of familiarity with Linux and the
[Unix shell](https://en.wikipedia.org/wiki/Unix_shell).

### Main directory

We advise keeping all GO-SHIP related code in a single directory.
From within the shell/terminal navigate to the location you want to place this and run:
```bash
mkdir go-ship
cd go-ship
```
to create the `go-ship/` directory and enter it.

### Data

We will now create a `data/` directory to hold any datasets the GO-SHIP tools might use.
From within the `go-ship/` directory run:
```bash
mkdir data
```
This will be the default location that programs and scripts use to look for and save
datasets.

### Virtual Environment

A number of the GO-SHIP tools are written in the [python](https://www.python.org/)
programming language.
We strongly recommend using a
[virtual environment](https://docs.python.org/3/library/venv.html) to run these.
This helps to isolate dependencies and keep your system clean.  
Where possible<sup>1</sup> we recommend a single virtual environment for all GO-SHIP codes.

To create a virtual environment run:
```bash
python3 -m venv gs-venv
```
This will create the directory `gs-venv` with the relevant contents.  
The virtual environment can then be 'activated' with:
```bash
source gs-venv/bin/activate
```
and you will see `(gs-venv)` appear by your terminal prompt.  
You can then carry out work as usual. When finished deactivate the environment with:
```bash
deactivate
```
It will remain exactly as you left it, with all previously installed software packages
available.

You will need to reactivate the environment when you do further work by navigating to
the `go-ship/` directory and running:
```bash
source gs-venv/bin/activate
```

<sup>1</sup> _It may be that multiple environments are required if any packages have 
conflicting dependencies. In this case you should create a separate environment for the
conflicting tool, and activate it instead when using that tool._

### Downloading GO-SHIP tools

You are now ready to obtain and use the tools provided by the GO-SHIP repositories.

To do this select the tool you wish to use from the
[list of repositories](https://github.com/orgs/GO-SHIP-Oceanography/repositories).
Then follow the instructions on the appropriate page to install the software.

This will usually involve cloning the repository.
We recommend cloning each tool inside the `go-ship/` directory to keep things
self-contained.

For example, suppose you want the
[station_bathymetry](https://github.com/GO-SHIP-Oceanography/station_bathymetry) tool.
following the instructions on the repository we would
[clone it](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)
using:
```bash
git clone https://github.com/GO-SHIP-Oceanography/station_bathymetry.git
```
which will create the directory `station_bathymetry/` with the code inside.  
we can navigate to that directory using:
```bash
cd station_bathymetry
```
and install the software using:
```bash
python3 -m pip install .
```
as described in the
[station_bathymetry](https://github.com/GO-SHIP-Oceanography/station_bathymetry)
repository.


### Resource structure

The suggested layout, after following the above instructions, is sketched below, with
the virtual environment, data, and software packages all contained within the `go-ship/`
directory:
```
go-ship/
|
|
|-gs-venv/
|  |- <virtual environment docs>
|  |- ...
|
|
|-data/
|  |- <go-ship datasets>
|  |- ...
|
|
|-station_bathymetry/
|  |- resources/
|  |   |- a16n_2023_track_leg2.csv
|  |- plot_bathymetry_at_station.ipynb
|  |- README.md/
|  |- ...
|
|
|-other_repository/
|  |-<other_repository_code> 
|  |- resources/
|  |- ...
|
|
...

```
