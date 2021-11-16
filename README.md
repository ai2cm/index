# Ai2 Climate Modeling Repostories

Our work is spread across a few key open-source, open-development repositories. These are roughly divided in to Applications and Libraries.

## Applications

The domain specific language (DSL) and machine learning (ML) teams are each producing two top-level applications. DSL is creating a *faster* climate model, and ML is creating a *better* one:

- (better) https://github.com/ai2cm/fv3net. A machine-learning capable climate model, machine learning training schemes, and diagnostics. This repository uses a monorepo style to suit the ML team's highly coordinated development approach.
- (faster) https://github.com/ai2cm/pace. Pace is the Python version of the FV3GFS dynamical core and physical parameterizations based on the GT4Py domain-specific language (see Libraries below) which can run on x86 CPUs and NVIDIA GPUs.

We also maintain a fork of the *baseline* FV3GFS model with improved diagnostic capability and continuous integration.

- (baseline) https://github.com/ai2cm/fv3gfs-fortran. A containerized Vulcan fork of the FV3GFS model.

## Libraries

The applications above depend on a series of libraries:
- https://github.com/a2icm/fv3gfs-wrapper. A python wrapper of FV3, used to apply python-based ML predictions in fv3net.
- https://github.com/ai2cm/fv3config. A tool for configuring and preparing input data for FV3GFS. Used to provision test data for several repos, and to configure scientific experiments declaratively or programatically with python.
- https://github.com/ai2cm/pace/tree/main/fv3gfs-util. A toolkit of Python objects and routines for writing weather and climate models. Contains features like halo-exchange and parallel I/O. Used by fv3gfs-wrapper and fv3core.

We also maintain a fork of the baseline GT4Py library for our own rapid development before contributing new features upstream.

- https://github.com/ai2cm/gt4py. GT4Py Python library for generating high-performance implementation of stencil kernels from a high-level defintion using regular Python functions.

