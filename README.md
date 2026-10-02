# Awesome Open-Source Solvers

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[日本語版はこちら / Japanese](README.ja.md)

Curated open-source **solvers** and scientific-computing stacks — FEM, BEM, CFD, multibody/dynamics, particle methods, acoustics, electronic circuits/EM, combustion, weather/climate, quantum — plus linear algebra and mesh adjuncts. Prefer well-known, durable projects with official docs or GitHub homes. Overlap with CAD/CAE lists is fine; this list focuses on **solvers**, not CAD apps.

## Contents

- [Finite Element (FEM)](#finite-element-fem)
- [Boundary Element (BEM)](#boundary-element-bem)
- [CFD](#cfd)
- [Multibody / structural dynamics](#multibody--structural-dynamics)
- [Particle methods (MD / DEM / SPH / PIC)](#particle-methods-md--dem--sph--pic)
- [Acoustics / vibroacoustics](#acoustics--vibroacoustics)
- [Electronic circuits / electromagnetics](#electronic-circuits--electromagnetics)
- [Combustion / reacting flows](#combustion--reacting-flows)
- [Weather / climate](#weather--climate)
- [Quantum / electronic structure / quantum dynamics](#quantum--electronic-structure--quantum-dynamics)
- [Linear algebra & parallel solvers](#linear-algebra--parallel-solvers)
- [Mesh / pre-post (brief)](#mesh--pre-post-brief)
- [Related lists](#related-lists)
- [Contributing](#contributing)

---

## Finite Element (FEM)

Libraries and industrial/research FEM codes for structural, thermal, and multiphysics PDEs.

### deal.II
C++ FEM library for adaptive, parallel, and matrix-free discretizations — from laptops to HPC. Strong tutorials and community.

- https://dealii.org/
- https://github.com/dealii/dealii

### FEniCS / DOLFINx
Python-first FEM platform for rapid variational formulations and coupled PDEs (FEniCSx / DOLFINx).

- https://fenicsproject.org/
- https://github.com/FEniCS

### MFEM
Lightweight, scalable C++ FEM toolbox for high-order methods, GPU/HPC, and research discretizations (Galerkin, DG, mixed, DPG).

- https://mfem.org/
- https://github.com/mfem/mfem

### CalculiX
Abaqus-like open-source 3D structural FEM (ccx solver + cgx). Widely used with FreeCAD FEM and PrePoMax GUIs.

- https://www.dhondt.de/
- https://github.com/Dhondtguido/CalculiX
- https://github.com/calculix

### Code_Aster
EDF’s industrial structural mechanics / multiphysics FEM suite; often paired with SALOME-Meca for pre/post.

- https://code-aster.org/
- https://gitlab.com/codeaster

### Elmer
Open multiphysics FEM (fluid, solid, EM, heat, and coupled problems) with GUI and parallel solvers.

- https://www.elmerfem.org/
- https://github.com/ElmerCSC/elmerfem

### FreeFEM / SfePy / Firedrake / scikit-fem
PDE/FEM platforms with DSL or Python interfaces for custom physics and research.

- https://freefem.org/ — https://github.com/FreeFem/FreeFem-sources
- https://sfepy.org/ — https://github.com/sfepy/sfepy
- https://www.firedrakeproject.org/ — https://github.com/firedrakeproject/firedrake
- https://scikit-fem.readthedocs.io/ — https://github.com/kinnala/scikit-fem

### MOOSE / libMesh / GetDP
Multiphysics Object-Oriented Simulation Environment (built on libMesh); GetDP for coupled FEM (often with Gmsh/ONELAB).

- https://mooseframework.inl.gov/ — https://github.com/idaholab/moose
- https://libmesh.github.io/ — https://github.com/libMesh/libmesh
- https://getdp.info/ — https://gitlab.onelab.info/getdp/getdp

### FrontISTR / MYSTRAN / FEBio / NGSolve
Large-scale nonlinear structures (FrontISTR); Nastran-like analysis (MYSTRAN); biomechanics nonlinear FEM (FEBio); Netgen + NGSolve FEM platform.

- https://www.frontistr.com/ — https://gitlab.com/FrontISTR-Commons/FrontISTR (main development; GitHub is a mirror)
- https://mystran.com/ — https://github.com/dr-bill-c/MYSTRAN
- https://febio.org/ — https://github.com/febiosoftware/FEBio
- https://ngsolve.org/ — https://github.com/NGSolve/ngsolve

### Kratos Multiphysics
BSD-licensed C++/Python framework for parallel multi-disciplinary simulation — structures, fluids, DEM, FSI, and optimization applications.

- https://kratosmultiphysics.github.io/Kratos/
- https://github.com/KratosMultiphysics/Kratos

---

## Boundary Element (BEM)

Surface-integral solvers for acoustics, electromagnetics, and exterior problems.

### Bempp
Python BEM platform for electrostatics, acoustics, and electromagnetics; Gmsh/VTK I/O and optional FEniCS FEM–BEM coupling.

- https://bempp.com/
- https://github.com/bempp

### scuff-em
BEM suite for electromagnetic scattering, Casimir/radiative heat transfer, and nanophotonics (EFIE / PMCHWT, RWG bases).

- https://github.com/HomerReid/scuff-em
- http://homerreid.github.io/scuff-em-documentation/

### OpenBEM
MATLAB Helmholtz / acoustic BEM codes for 2D and 3D geometries.

- https://openbem.dk/

---

## CFD

Finite-volume, finite-element, and lattice-Boltzmann fluid solvers.

### OpenFOAM
Most widely used open-source CFD toolbox — incompressible/compressible flow, heat transfer, multiphase, reactions; large ecosystem. Latest OpenCFD release is v2606 (June 2026); its repositories moved to gitlab.com/openfoam in Nov 2025.

- https://www.openfoam.com/ — https://gitlab.com/openfoam
- https://openfoam.org/
- https://github.com/OpenFOAM/OpenFOAM-dev

### SU2
Multiphysics PDE solver with gradient-based aerodynamic shape optimization and adjoint capabilities.

- https://su2code.github.io/
- https://github.com/su2code/SU2

### Nektar++ / Lethe
Spectral/hp element CFD (Nektar++); high-order CG CFD–DEM (Lethe).

- https://www.nektar.info/ — https://gitlab.nektar.info/nektar/nektar
- https://chaos-polymtl.github.io/lethe/ — https://github.com/chaos-polymtl/lethe

### Palabos / waLBerla / OpenLB
Lattice Boltzmann Method (LBM) CFD frameworks for complex flows and HPC.

- https://palabos.unige.ch/ — https://gitlab.com/unigespc/palabos
- https://www.walberla.net/ — https://github.com/lssfau/walberla (mirror of the official FAU GitLab)
- https://www.openlb.net/ — https://gitlab.com/openlb/release

### Fire Dynamics Simulator (FDS)
NIST fire-driven flow CFD with Smokeview visualization.

- https://pages.nist.gov/fds-smv/
- https://github.com/firemodels/fds

### Code_Saturne / Nek5000 / nekRS
EDF industrial CFD (Code_Saturne); spectral-element CFD (Nek5000 / nekRS).

- https://www.code-saturne.org/
- https://nek5000.mcs.anl.gov/ — https://github.com/Nek5000/Nek5000
- https://github.com/Nek5000/nekRS

### JAX-Fluids / XLB
GPU-accelerated, differentiable CFD in Python for physics-based ML — compressible/multiphase finite-volume (JAX-Fluids) and lattice Boltzmann on JAX / NVIDIA Warp (XLB).

- https://github.com/tumaer/JAXFLUIDS
- https://github.com/Autodesk/XLB

---

## Multibody / structural dynamics

Rigid and flexible multibody dynamics, mechanisms, and vehicle/robot simulation.

### Project Chrono
Multiphysics multibody platform — vehicles, robots, granular/DEM contact, FEA co-simulation.

- https://projectchrono.org/
- https://github.com/projectchrono/chrono

### MBDyn / Simbody / EXUDYN
General-purpose MBD (MBDyn); articulated biomechanics/robotics (Simbody); Python/C++ flexible multibody (EXUDYN).

- https://www.mbdyn.org/ — https://public.gitlab.polimi.it/DAER/mbdyn
- https://github.com/simbody/simbody
- https://github.com/jgerstmayr/EXUDYN

### OpenSim / Pinocchio / Drake
Musculoskeletal dynamics (OpenSim); fast rigid-body dynamics for robotics (Pinocchio); robotics & control toolbox with dynamics (Drake).

- https://opensim.stanford.edu/ — https://github.com/opensim-org
- https://github.com/stack-of-tasks/pinocchio
- https://drake.mit.edu/ — https://github.com/RobotLocomotion/drake

### OpenFAST
NLR (formerly NREL) aero-servo-elastic wind turbine dynamics (coupled CFD/structural loads workflows).

- https://openfast.readthedocs.io/
- https://github.com/OpenFAST/openfast

---

## Particle methods (MD / DEM / SPH / PIC)

Molecular dynamics, discrete element, smoothed particle hydrodynamics, and particle-in-cell codes.

### LAMMPS
Large-scale Atomic/Molecular Massively Parallel Simulator — materials MD, coarse-grained and mesoscale particle models.

- https://www.lammps.org/
- https://github.com/lammps/lammps

### GROMACS
High-performance molecular dynamics for biomolecules and soft matter; strong GPU support.

- https://www.gromacs.org/
- https://github.com/gromacs/gromacs

### DualSPHysics / SPHERA / PySPH
SPH free-surface / coastal / industrial flows (DualSPHysics); engineering SPH (SPHERA); Python SPH framework (PySPH).

- https://dual.sphysics.org/ — https://github.com/DualSPHysics/DualSPHysics
- https://github.com/GiordanoAgateRSE/SPHERA
- https://pysph.readthedocs.io/ — https://github.com/pypr/pysph

### LIGGGHTS / Yade / MercuryDPM
DEM for granular materials and industrial particle processes.

- https://www.cfdem.com/liggghtsr-open-source-discrete-element-method-particle-simulation-code — https://github.com/CFDEMproject/LIGGGHTS-PUBLIC (commercial successor: Aspherix)
- https://yade-dem.org/ — https://gitlab.com/yade-dev/trunk
- https://www.mercurydpm.org/ — https://github.com/MercuryDPM/MercuryDPM

### WarpX / PIConGPU / Smilei
Exascale electromagnetic PIC (WarpX); GPU PIC (PIConGPU); plasma PIC (Smilei).

- https://warpx.readthedocs.io/ — https://github.com/BLAST-WarpX/warpx
- https://picongpu.readthedocs.io/ — https://github.com/ComputationalRadiationPhysics/picongpu
- https://smileipic.github.io/Smilei/ — https://github.com/SmileiPIC/Smilei

### HOOMD-blue / OpenMM
GPU-accelerated MD for soft matter (HOOMD-blue); high-performance biomolecular MD toolkit (OpenMM).

- https://glotzerlab.engin.umich.edu/hoomd-blue/ — https://github.com/glotzerlab/hoomd-blue
- https://openmm.org/ — https://github.com/openmm/openmm

---

## Acoustics / vibroacoustics

Wave propagation, room/outdoor acoustics, and coupled vibroacoustic solvers.

### FEM vibroacoustics (Code_Aster / Elmer / CalculiX)
Structural–acoustic coupling via industrial FEM suites (see FEM section).

- https://code-aster.org/
- https://www.elmerfem.org/
- https://www.dhondt.de/

### Acoustic BEM (Bempp / OpenBEM / scuff-em)
Exterior and interior Helmholtz / EM–acoustic boundary-element solvers (see BEM section).

- https://bempp.com/
- https://openbem.dk/
- http://homerreid.github.io/scuff-em-documentation/

### k-Wave
MATLAB/C++ toolbox for time-domain acoustic and ultrasound wavefields. v1.4.x is the last full k-Wave-I release; a community rewrite (k-Wave-II) is planned. Python interface via k-wave-python.

- http://www.k-wave.org/
- https://github.com/ucl-bug/k-wave
- https://github.com/waltsims/k-wave-python

### GetDP / ONELAB acoustics
Coupled FEM acoustics and multiphysics via GetDP + Gmsh/ONELAB workflows.

- https://getdp.info/
- https://onelab.info/

---

## Electronic circuits / electromagnetics

Circuit (SPICE) simulators and electromagnetic field solvers. See also Elmer / GetDP (FEM electromagnetics) and scuff-em (BEM). Freeware but closed-source tools such as LTspice and QSPICE are out of scope.

### ngspice
Open-source mixed-signal SPICE simulator (successor of Berkeley SPICE3f5); built into KiCad and used as a backend by Qucs-S and PySpice.

- https://ngspice.sourceforge.io/ — https://sourceforge.net/p/ngspice/ngspice/

### Xyce
Sandia's massively parallel, SPICE-compatible circuit simulator for large analog circuits (GPL v3).

- https://xyce.sandia.gov/ — https://github.com/Xyce/Xyce

### Qucs-S / PySpice
GUI schematic capture and simulation front end driving ngspice, Xyce, or QucsatorRF (Qucs-S); Python interface to ngspice / Xyce for scripted circuit analysis (PySpice; docs site not updated since 2021).

- https://ra3xdh.github.io/ — https://github.com/ra3xdh/qucs_s
- https://pyspice.fabrice-salvaire.fr/ — https://github.com/PySpice-org/PySpice

### openEMS / Meep
FDTD electromagnetic field solvers — antennas and PCB/RF structures with MATLAB/Octave/Python interfaces (openEMS); nanophotonics and general EM with Python scripting (Meep, MIT).

- https://www.openems.de/ — https://github.com/thliebig/openEMS-Project
- https://meep.readthedocs.io/ — https://github.com/NanoComp/meep

### Palace
AWS 3D finite-element solver for computational electromagnetics (eigenmodes, frequency/time domain, electrostatics, magnetostatics), used e.g. for superconducting quantum circuits; built on MFEM.

- https://awslabs.github.io/palace/stable/ — https://github.com/awslabs/palace

---

## Combustion / reacting flows

Chemical kinetics, reacting CFD, and fire/combustion packages.

### Cantera
Chemical kinetics, thermodynamics, and transport library — mechanisms, 0D/1D reactors, and CFD coupling.

- https://cantera.org/
- https://github.com/Cantera/cantera

### OpenFOAM reacting / combustion solvers
Built-in reacting / chemistry / combustion packages on the OpenFOAM toolboxes.

- https://www.openfoam.com/documentation/
- https://openfoam.org/

### Fire Dynamics Simulator (FDS)
Fire-driven reacting buoyancy flows (see also CFD).

- https://pages.nist.gov/fds-smv/
- https://github.com/firemodels/fds

### PeleC / PeleLMeX / PelePhysics
AMReX-based compressible and low-Mach reacting flow solvers (DOE Exascale combustion stack, now published as the Pele Suite).

- https://pele-suite.github.io/
- https://github.com/Pele-Suite

### CoolProp
Open-source thermodynamic and transport properties (useful adjunct for reacting-flow workflows).

- https://coolprop.org/
- https://github.com/CoolProp/CoolProp

---

## Weather / climate

Numerical weather prediction (NWP), Earth-system / climate models, and machine-learning weather forecasting. Check each model's license for trained weights before use.

### WRF / MPAS
Weather Research and Forecasting model — the most widely used open limited-area NWP model (NCAR); MPAS-Atmosphere, unstructured Voronoi-mesh global-to-regional model (NCAR / LANL).

- https://www.mmm.ucar.edu/models/wrf — https://github.com/wrf-model/WRF
- https://mpas-dev.github.io/ — https://github.com/MPAS-Dev/MPAS-Model

### UFS Weather Model
NOAA Unified Forecast System built on the FV3 dynamical core — the community model behind the operational GFS.

- https://ufs.epic.noaa.gov/
- https://github.com/ufs-community/ufs-weather-model

### ICON
Icosahedral nonhydrostatic weather and climate model of DWD / MPI-M; open source under BSD-3-Clause since 2024.

- https://www.icon-model.org/
- https://gitlab.dkrz.de/icon/icon-model

### CESM / E3SM
Coupled Earth-system models for climate simulation — atmosphere, ocean, land, sea ice (CESM by NCAR; E3SM by US DOE).

- https://www.cesm.ucar.edu/ — https://github.com/ESCOMP/CESM
- https://e3sm.org/ — https://github.com/E3SM-Project/E3SM

### Anemoi / AIFS
ECMWF framework for training and running ML weather models (datasets, graphs, models, training, inference); ECMWF's operational AI forecast AIFS is built on it (weights CC BY 4.0).

- https://anemoi.readthedocs.io/ — https://github.com/ecmwf/anemoi-core
- https://huggingface.co/ecmwf/aifs-single-1.1

### GraphCast / GenCast / NeuralGCM
Google DeepMind ML medium-range forecasting — deterministic GraphCast and ensemble GenCast (repo renamed from graphcast to weathernext); NeuralGCM, a hybrid differentiable dynamical core + ML atmosphere model.

- https://github.com/google-deepmind/weathernext
- https://neuralgcm.readthedocs.io/ — https://github.com/neuralgcm/neuralgcm

### Earth2Studio / Aurora / Pangu-Weather
NVIDIA framework for running AI weather/climate models (FourCastNet and others); Microsoft Aurora Earth-system foundation model; Huawei Pangu-Weather 3D transformer forecaster.

- https://nvidia.github.io/earth2studio/ — https://github.com/NVIDIA/earth2studio
- https://microsoft.github.io/aurora/ — https://github.com/microsoft/aurora
- https://github.com/198808xc/Pangu-Weather

---

## Quantum / electronic structure / quantum dynamics

DFT, many-body electronic structure, and open quantum systems.

### Quantum ESPRESSO
Plane-wave DFT / electronic-structure suite for materials and molecules; large user community.

- https://www.quantum-espresso.org/
- https://gitlab.com/QEF/q-e

### ABINIT / CP2K / SIESTA / GPAW
Plane-wave and localized-orbital DFT codes for solids, chemistry, and nanosystems.

- https://www.abinit.org/ — https://github.com/abinit/abinit
- https://www.cp2k.org/ — https://github.com/cp2k/cp2k
- https://gitlab.com/siesta-project/siesta
- https://gpaw.readthedocs.io/ — https://gitlab.com/gpaw/gpaw

### QuTiP
Quantum Toolbox in Python — open quantum systems, master equations, and quantum optics dynamics.

- https://qutip.org/
- https://github.com/qutip/qutip

### NWChem / Psi4 / PySCF
Computational chemistry suites (NWChem); quantum chemistry (Psi4); Python quantum chemistry (PySCF).

- https://nwchemgit.github.io/ — https://github.com/nwchemgit/nwchem
- https://psicode.org/ — https://github.com/psi4/psi4
- https://pyscf.org/ — https://github.com/pyscf/pyscf

### Yambo / BerkeleyGW / Octopus
Many-body perturbation theory / GW-BSE (Yambo, BerkeleyGW); real-space TDDFT (Octopus).

- https://www.yambo-code.eu/ — https://github.com/yambo-code/yambo
- https://berkeleygw.org/ — https://github.com/BerkeleyGW/BGW-public
- https://octopus-code.org/ — https://gitlab.com/octopus-code/octopus

---

## Linear algebra & parallel solvers

Sparse iterative/direct solvers and HPC numerical libraries that underpin many of the codes above.

### PETSc (+ TAO)
Portable Extensible Toolkit for Scientific Computation — Krylov solvers, preconditioners, nonlinear/time steppers, and TAO optimization; C/Fortran/Python (petsc4py).

- https://petsc.org/
- https://gitlab.com/petsc/petsc
- https://github.com/petsc/petsc

### Trilinos
Package ecosystem for HPC linear algebra, solvers, discretizations, and multiphysics (Belos, Ifpack2, MueLu, Tpetra, …).

- https://trilinos.github.io/
- https://github.com/trilinos/Trilinos

### hypre
High-performance parallel multigrid preconditioners and solvers for large sparse systems (BoomerAMG, etc.).

- https://computing.llnl.gov/projects/hypre-scalable-linear-solvers-multigrid-methods
- https://github.com/hypre-space/hypre

### SuperLU / MUMPS / SuiteSparse
Sparse direct solvers — SuperLU / SuperLU_DIST; MUMPS multifrontal; SuiteSparse (UMFPACK, CHOLMOD, SPQR, …).

- https://portal.nersc.gov/project/sparse/superlu/ — https://github.com/xiaoyeli/superlu
- https://mumps-solver.org/
- https://people.engr.tamu.edu/davis/suitesparse.html — https://github.com/DrTimothyAldenDavis/SuiteSparse

### Eigen / OpenBLAS
Dense linear algebra building blocks used inside many solvers.

- https://libeigen.gitlab.io/ — https://gitlab.com/libeigen/eigen
- https://openmathlib.org/OpenBLAS/ — https://github.com/OpenMathLib/OpenBLAS

### Dakota
Sandia toolkit for optimization, UQ, and model calibration wrapped around simulation codes.

- https://dakota.sandia.gov/
- https://github.com/snl-dakota/dakota

### preCICE
Coupling library for partitioned multiphysics (FSI, conjugate heat transfer) with ready adapters for OpenFOAM, CalculiX, Code_Aster, deal.II, FEniCS, SU2, and more.

- https://precice.org/
- https://github.com/precice/precice

---

## Mesh / pre-post (brief)

Geometry meshing and visualization typically paired with the solvers above (not a full CAD list).

### Gmsh
Open-source 3D FE mesh generator with CAD kernel options, `.geo` scripting, and post-processing.

- https://gmsh.info/
- https://gitlab.onelab.info/gmsh/gmsh

### Netgen / SALOME / meshio
Tetrahedral meshing (Netgen); CAD/mesh pre-post platform (SALOME); mesh format I/O in Python (meshio).

- https://ngsolve.org/ — https://github.com/NGSolve/netgen
- https://www.salome-platform.org/
- https://github.com/nschloe/meshio

### ParaView / VTK / VisIt
Scientific visualization for CFD/FEM results (ParaView, VTK); VisIt for large parallel datasets.

- https://www.paraview.org/ — https://github.com/Kitware/ParaView
- https://vtk.org/ — https://github.com/Kitware/VTK
- https://visit-dav.github.io/visit-website/ — https://github.com/visit-dav/visit

---

## Related lists

- https://github.com/shvyac/awesome-cad-cae — CAD / CAE / EDA / formats (broader toolchain)
- https://github.com/mlightcad/awesome-cad — open-source CAD software & libraries
- https://github.com/kimimgo/awesome-ai-cae — AI-callable CAE/CAD tooling
- https://github.com/IgorAherne/awesome-CAD — CAD-related awesome list
- https://awesome.re/ — Awesome manifesto

---

## Contributing

PRs and issues welcome. Prefer **open-source solvers** with durable official or GitHub URLs, a short blurb, and clear category fit. Avoid CAD-only apps (point those to [awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae)). Keep EN and JA READMEs in sync.

License for this list: content is dedicated to the public domain where possible; individual linked projects retain their own licenses (GPL, LGPL, BSD, Apache-2.0, etc).
