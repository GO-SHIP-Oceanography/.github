# Contributing

GO-SHIP welcomes codes and contributions from anyone who feels they can benefit the
community.

This document is designed to guide those who have a new code that they wish to bring
to the GO-SHIP Organisation.
For details on how to contribute to an existing repository please see the documentation
of that specific repository for guidance.

- [Pre-requisites](#pre-requisites)
- [Requirements](#requirements)
- [Desirables](#desirables)
- [Adding Code](#adding-code)
- [Code Management](#code_management)


## Pre-requisites

We welcome any codes/tools that are useful for oceanographic cruise purposes.
These can be written in any language (python, R, MATLAB etc.)

If you have a code that you would like to add to the organisation please
[open an issue](https://github.com/GO-SHIP-Oceanography/.github/issues) on this
repository using the _"New Code"_ template and title it `[New Code]: <Name_of_code>`.

Include a brief description of:

- what the code does,
- why it is beneficial to the oceanography community,
- contact details,
- license details for the code.

and, if possible, assign it the "new code" tag.

We will then review the application and create a repository for you.
Once this has been done we will support you with uploading and any initial
review/improvements.

If your code already exists under version control but you want it to be included in
these resources please note this.
We can either transfer the existing repository, redirect to the existing repository,
or set up a Mirror.


## Requirements

Please endeavour to make sure that your code meets the following requirements.
If you need help with these please ask for guidance as part of the aforementioned issue.

### Name

When naming your code please choose an 'active' name that makes it clear what
the code is used for.
For example, a code that is used to plot bathymetry around measurement stations should
be called something like `plot-bathymetry-at-station` rather than `plot-bathym` or
`station-bathymetry` etc.

### Code

Please ensure that the code is complete and runs.
This includes running on your personal computer, but also the ability to run on
another machine i.e. no 
[hard-coded filepaths](https://medium.com/@jordan.l.edmunds/please-stop-hard-coding-file-paths-609c769f9537)
etc.

Try to avoid committing binary data or large datasets.
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

In addition to the above the following are desirable qualities for research software.
If you would like assistance with adding these to your code, either before or after the
initial upload, please ask for assistance.

### Packaging

If you can package your code to make it easy for to install this is very useful.
This enables users to run an 'installation' procedure (e.g. `pip install` in python)
and then 'run' your code, rather than downloading a series of files and needing to
piece them together themselves.

For python codes we suggest using a
`[pyproject.toml](https://packaging.python.org/en/latest/guides/writing-pyproject-toml/)`
file. For R see [R Packages](https://r-pkgs.org/). For other languages check for the
recommended approach or ask for advice.

### Testing

Ideally codes should contain
[some tests](https://the-turing-way.netlify.app/reproducible-research/testing)
to ensure that they work correctly.
We realise that this may not be necessary in all cases and codes may well have been
written without testing.
If you would like help with adding tests to your code this please ask for advice - we
are happy to support you.

### Continuous Integration

[GitHub Actions](https://docs.github.com/en/actions) can be used to run checks on
any code that is added to a repository.
For example, ensuring that it meets certain style, linting, documentation guidelines,
or to auto-generate documentation and/or webpages.
We are happy to support you in doing this.


## Adding code

### Initial upload

After requesting to add a new code to GO-SHIP we will create a GitHub repository with
the bare minimum contents.
To populate this with your code you should navigate into the folder in which it is
installed on your computer and then run, from the terminal:
```bash
git init
git remote add origin git@github.com:GO-SHIP-Oceanography/<your-go-ship-repo>.git
git pull origin main
```
to pull any base documents (e.g. license).  
_Note: This assumes you are accessing a repository via ssh (advised). If you prefer to
access via https you can use
`git remote add origin https://github.com/GO-SHIP-Oceanography/<your-go-ship-repo>.git`
and will be prompted for your GitHub username and password each time you access._

Following this you can add files using `[git add](https://github.com/git-guides/git-add)`,
commit them using `[git commit](https://github.com/git-guides/git-commit)` and push them
to the repository using `[git push](https://github.com/git-guides/git-push)` as usual.
The [Turing Way guide](https://the-turing-way.netlify.app/reproducible-research/vcs/vcs-git)
is a useful guide for those new to these ideas.

We suggest that you perform your initial upload from a branch, allowing the code to be
reviewed before it is contributed to the main branch, and checked to ensure that it
works and is reproducible.
To do this run:
```bash
git checkout -b first-commit
```
before any `git add` or `git commit` commands.
Then, when you are ready, run:
```bash
git push origin first-commit
```
to upload the code to GitHub.

You can then open a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
from the repository webpage on GitHub to ask to add your code to the main branch.

If you are unsure about any part of this process we are happy to guide you through it.

### Further developments

Once you have performed the initial upload of the code to the main branch of your
repository you may wish to make further changes as features are added and
the code is improved.

We suggest any development work is done in git branches, with the updates then
being integrated back into the main repository via a pull request once work is
complete and the changes are reviewed.
It is suggested, but not required, to use the features of GitHub
(issues and pull requests) to manage this process ([see below](#code-management)).


## Code Management

When you add your code to the GO-SHIP GitHub organisation you will be given a repository
which you, unless otherwise requested, will be responsible for managing.
If you are new to git and version control workflows for software development we are
happy to provide assistance and advice.

We suggest that users follow the conventional approach for managing software projects
via git, with development being performed in git branches that are then merged into the
main once work is complete via a reviewed pull request.

For small projects you can add (or request addition) of trusted collaborators to the
repository where they can perform development.
If you have a large project with many contributors we suggest they
[create a fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)
and contribute using the "fork-and-pull" approach.

If at any point you need advice on code management or would like pointing to further
resources please get in touch.

### Cruise-specific code

If a code needs modifying for a specific cruise in a way that is more than just a local
change we suggest creating a branch for that cruise.
It can then be decided at a later date whether to tidy this code and merge any updates
back into the main repository branch.
