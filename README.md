# Minimal MySTmd Notebook Execution
## Motivation
This repo is intended to be executed via `myst build --execute`.

It will be used to diagnose and document instances where the spawned Jupyter server remains running 
after the execution completes.

## Observed behavior
`myst build --execute` runs to completion. An ephemeral Jupyter server is spawned, and exits normally after 
the command completes successfully.

`myst build --execute --html` runs to completion. An ephemeral Jupyter server is spawned, but remains running after the command completes successfully.

## Expected behavior
The ephemeral Jupyter server process should exit normally in both command line invocations of `myst build`.

## Systems tested
Mac OS 15.5, M1; Oracle Linux 8,  x86_64

## Relevant Python packages
mystmd==1.5.1
jupyterlab_server==2.27.3
jupyterlab-myst==2.4.2
jupyterlab==4.4.4

## Authors

[Kevin Tyle](https://github.com/ktyle)
