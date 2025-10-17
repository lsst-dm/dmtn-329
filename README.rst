.. image:: https://img.shields.io/badge/dmtn--329-lsst.io-brightgreen.svg
   :target: https://dmtn-329.lsst.io
.. image:: https://github.com/lsst-dm/dmtn-329/workflows/CI/badge.svg
   :target: https://github.com/lsst-dm/dmtn-329/actions/

#############################################
Brighter-Fatter effect in LSSTCam CCD sensors
#############################################

DMTN-329
========

The brighter-fatter effect (BF) is a subtle yet critical manifestation of pixel-to-pixel correlations in CCDs, where brighter sources induce a redistribution of charge that broadens object shapes. Caused by electrostatic deflections from accumulated charge, the BF effect introduces flux-dependent distortions that can bias precision astronomical measurements, notably in weak lensing surveys. In this study, we investigate the influence of the incident wavelength on BF coefficients, using both LSST camera data and electrostatic modeling. We explore how variations in illumination modify the local electric field within the CCD, thereby altering charge drift paths. We are developing an electrostatic model to quantify these distortions. Our results show that BF coefficients depend not only on charge accumulation but also on the incident wavelength, adding a new layer of complexity to their interpretation. This has direct implications for calibration strategies and the accuracy of shape measurements in current and future imaging surveys.

Links
=====

- Live drafts: https://dmtn-329.lsst.io
- GitHub: https://github.com/lsst-dm/dmtn-329

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst-dm/dmtn-329

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the `acronyms.tex` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
