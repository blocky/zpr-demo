# zpr-demo
Jupyter notebooks for various demos


## Getting started

I assume that you are working on Ubuntu 20.04 (But that is just what I am using.
There isn't anything special going on here.  Any OS running python should
be fine).  Like all python projects, you will need:

- python
- pip

And you can install the dependencies with

    pip install -r requirements.txt

**A note from Dave**
Personally, I recommend sand boxing your python environments.  My choice of
tools is mini-conda (**note the mini**).  If you are using mini-conda, setup
with:

    conda create --name zpr-demo pip

Activate the environment

    conda activate zpr-demo

And then install the dependencies

    pip install -r requirements.txt

You get out of the environment with

    conda deactivate

And whenever you come back to working on the project, make sure to active the
environment with:

    conda activate zpr-demo

## Doing some development

Startup the notebook server locally with

    jupyter notebook

It should pop open a window on your browser and start a server.  Navigate to the
`notebooks` folder and open the one you want to work on.

### Version control and Jupter

Note that jupyter notebooks are notoriously annoying to use in version control
because while we want to version the code, we do not want to version control the
cell evaluations.  There are lots of ways to handle the annoyance.  In this
project, we use a program called
[nbstripout](https://github.com/kynan/nbstripout), which when combined with git,
removes does not commit cell evaluations.
