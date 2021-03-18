# Vulcan Climate Modeling Repostories

Our work is spread across a few key repositories. These are roughly divided in to Libraries and Applications.

## Applications

The DSL and ML teams are each producing two top-level applications. DSL is creating a *faster* climate model, and ML is creating a *better* one:

- (better) https://github.com/VulcanClimateModeling/fv3net/. A machine-learning capable climate model, machine learning training schemes, and diagnostics. This repository uses a monorepo style to suit the ML team's highly coordinated development approach.
- (faster) https://github.com/VulcanClimateModeling/fv3core. FV3core is a Python version, using GridTools GT4Py with CPU and GPU backend options, of the FV3 dynamical core (fv3gfs-fortran repo).

We also maintain a fork of the *baseline* FV3GFS model with improved diagnostic capability and continuous integration.

- (baseline) https://github.com/VulcanClimateModeling/fv3gfs-fortran. A containerized Vulcan fork of the FV3GFS model.

## Libraries

The applications above depend on a series of libraries:
- https://github.com/VulcanClimateModeling/fv3gfs-wrapper. A python wrapper of FV3, used to apply python-based ML predictions in fv3net.
- https://github.com/VulcanClimateModeling/fv3config. A tool for configuring and preparing input data for FV3GFS. Used to provision test data for several repos, and to configure scientific experiments declaratively or programatically with python.
- https://github.com/VulcanClimateModeling/fv3gfs-util. A toolkit of Python objects and routines for writing weather and climate models. Contains features like halo-exchange and parallel I/O. Used by fv3gfs-wrapper and fv3core.

