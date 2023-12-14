# Contributing

GO-SHIP welcomes codes and contributions from anyone who feels they can benefit the
community.

This document is designed to guide those who have a new code that they wish to bring
to the GO-SHIP Organisation.
For details on how to contribute to an existing repository please see the documentation
of that specific repository for guidance.

- [Pre-requisites](#pre-requisites)
- [Requirements](#requirements)
- [Code Management](#code_management)

## Pre-requisites

We welcome any codes/tools that are useful for oceanographic cruise purposes.
These can be written in any language (python, R, MATLAB etc.)

If you have a code that you would like to add to the organisation please
[open an issue](https://github.com/GO-SHIP-Oceanography/.github/issues) on this
repository with the title `[New Code]: <Name_of_code>`.

Include a brief description of:

- what the code does,
- why it is beneficial to the oceanography community,
- contact details,
- license details for the code.

and, if possible, assign it the "new code" tag.


## Requirements

Please endeavour to make sure that your code meets the following requirements.
If you need help with these please ask for guidance as part of the aforementioned issue.

### Code

Please ensure that the code is complete and runs.
This includes running on your personal computer, but also the ability to run on
another machine i.e. no 
[hard-coded filepaths](https://medium.com/@jordan.l.edmunds/please-stop-hard-coding-file-paths-609c769f9537)
etc.

Do not commit binary data or large datasets.
Files generated during build, executables, pdfs, and large datasets generally don't
belong in git repositories.
Instead you should include instructions to build code and download data etc.  
Placing a [`.gitignore`](https://www.atlassian.com/git/tutorials/saving-changes/gitignore)
file at the top of the repository can help with this.

### License

All codes **must** have a suitable
[open-source license](https://opensource.org/licenses/) attached to them.  
If your code does not already have one we suggest the
[MIT License](https://mit-license.org/).
However, please check with any relevant institutions or funding bodies as they may
have restrictions on the licenses that may be used.

If you are unsure about this please reach out to us and we can provide guidance.  
An introduction to software licenses can be found in a 
[Code for Thought podcast episode](https://codeforthought.buzzsprout.com/1326658/11564212)
and there is advice on selecting at [choosealicense.com](https://choosealicense.com/).


### Readme

Your code should come with an appropriate Readme file.  
This should ideally be written in [Markdown](https://en.wikipedia.org/wiki/Markdown)
and stored at the top level as `README.md`.

The Readme file should include the following information:

- description of the code and what it does
- license information
- dependencies (other things you need to run the code)
- installation instructions
- usage/getting started instructions
- how to raise issues
- guidelines for contributing
- authors/managers of the code

Examples of `README.md` files can be found in the existing repositories.

### Data storage

GO-SHIP codes are often used in conjunction with several others, all of which may share
the same datasets (e.g. ocean bathymetry).
If you make use of one of these shared datasets we advise storing them in a directory
`data/` that is adjacent to the [setup instructions](setup.md), or providing the ability
for users to set the dataset location.


## Desirables

### Packaging

### Testing

### 


## Adding code




## Code Management

Adding your code 
