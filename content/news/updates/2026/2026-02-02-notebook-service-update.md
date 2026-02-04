---
title: JASMIN Notebook Service Environment Updates
date: 2026-02-02 11:30:00
tags: ['news', 'jasmin']
thumbnail:
icon: fas book text-info
---
Dear JASMIN Users,

We are making some changes to the software environments provided by the JASMIN notebook service, in order to make it more compatible with the environment on the rest of JASMIN.
The environments provided on the notebook service will now be identical to that provided on the sci machines and LOTUS.

The new environment brings a number of advantages:
* Environments created anywhere on JASMIN should work across the notebook service, sci machines and LOTUS.
* We have released general availability of GPU notebooks to all users. If you need to use a GPU, select this from the start screen.
* It is now possible to run notebooks based on any of the supported versions of Jaspy.
* It is now possible to use JasR, JASMIN’s environment for R, in the notebook service.
* As an experimental feature, we now have documentation on how to use Julia in the notebook service.
* In the future, this change lays the groundwork to allow us to provide a version of Jaspy specialised for machine learning.

Breaking change: it will now be possible to create a virtual environment which works across JASMIN. However, old environments which were created based on the notebook service (specifically based on the Python found in `/opt/jaspy` in the notebook service) will stop working in *one month*. You can migrate by:
1. Activating your current environment and running `pip freeze > req.txt` .
1. Creating a new environment according to {{<link "https://help.jasmin.ac.uk/docs/software-on-jasmin/python-virtual-environments/#in-the-jasmin-notebook-service">}}the new instructions here{{</link>}}.
1. Running `pip install -r req.txt` in the new environment.

The documentation has been updated please see:
* {{<link "https://help.jasmin.ac.uk/docs/interactive-computing/jasmin-notebooks-service/">}}Updated description of the notebook service{{</link>}}
* {{<link "https://help.jasmin.ac.uk/docs/software-on-jasmin/conda-environments-and-python-virtual-environments/">}}General info about conda environments{{</link>}}
* {{<link "https://help.jasmin.ac.uk/docs/software-on-jasmin/python-virtual-environments/#in-the-jasmin-notebook-service">}}How to create a virtual environment and turn it into a Jupyter kernel{{</link>}}
