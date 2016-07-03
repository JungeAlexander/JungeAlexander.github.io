---
layout: post
title: Towards reproducibility with (bio)conda
---
The first thing I do before starting to work on a new project is creating a virtual environment using conda.
This is a short tutorial explaining how conda and bioconda can help ensuring reproducibility in a (bioinformatics)
software project.

[Conda](http://conda.pydata.org/docs/) is an open source package manager that also handles virtual environments.
The [bioconda](https://bioconda.github.io/) projects aims to provide an easy installation of many
bioinformatics-related software packages through conda.
The bioconda community is very active and welcome contributions by anyone who would like to add their favorite piece of
software to conda. Find the project repository on GitHub [here](https://github.com/bioconda/bioconda-recipes).

Below I will briefly outline how we are using conda in a collaborative project:

## Basic conda usage when working on a collaborative project

{% highlight shell %}
# add R and bioconda channels
# these channels provide packages not available in base conda
conda config --add channels r
conda config --add channels bioconda

# create virtual environment named ourenv containing Python 3.5, Bioconductor, IPython
# and the Python ML-library scikit-learn
conda create --name ourenv python=3.5 bioconductor-biobase=2.30.0 jupyer scikit-learn
{% endhighlight shell %}

Note that the above command will automatically install all dependencies of software to be installed.
For instance, base R will automatically be installed since Bioconductor depends on it.

The current state of the virtual environment with all programs installed in it can then be exported by executing:

{% highlight shell %}
conda env export > environment.yml
{% endhighlight shell %}

Then simply add the file `environment.yml` to the source code repository used in the collaborative project.
`environment.yml` not only lists the dependencies of the project but also the *exact version* for each dependency.
The file looks like this:

{% highlight shell %}
name: ourenv
dependencies:
- bioconductor-biobase=2.30.0=0
- bioconductor-biocgenerics=0.16.1=r3.2.2_0
- bioconductor-iranges=2.4.8=0
- bioconductor-s4vectors=0.8.11=0
- ipykernel=4.3.1=py27_0
- ipython=4.2.0=py27_0
- ipython_genutils=0.1.0=py27_0
- jupyter_client=4.2.2=py27_0
- jupyter_console=4.1.1=py27_0
- jupyter_core=4.1.0=py27_0
- [...]
{% endhighlight shell %}

A new user starting to work in the projects can then obtain a virtual environment where all binaries are identical
to those used by other team members by executing the following steps (after cloning the source code repository):

{% highlight shell %}
# add R and bioconda channels
conda config --add channels r
conda config --add channels bioconda

# install all dependencies in virtual environment called ourenv
conda env create -f environment.yml

# active virtual environment that was just created
source activate ourenv

# good to go
{% endhighlight shell %}

By allowing all project members to work with the same versions of all
project dependencies, (bio)conda provides an essential step towards ensuring reproducibility of any bioinformatics
project.
