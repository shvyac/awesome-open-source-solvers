# Awesome Open-Source Solvers

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[日本語版はこちら / Japanese](README.ja.md)

Curated open-source **solvers** and scientific-computing stacks — FEM, BEM, CFD, multibody/dynamics, particle methods, acoustics, combustion, quantum — plus linear algebra and mesh adjuncts. Prefer well-known, durable projects with official docs or GitHub homes. Overlap with CAD/CAE lists is fine; this list focuses on **solvers**, not CAD apps.

## Contents

- [Finite Element (FEM)](#finite-element-fem)
- [Boundary Element (BEM)](#boundary-element-bem)
- [CFD](#cfd)
- [Multibody / structural dynamics](#multibody--structural-dynamics)
- [Particle methods (MD / DEM / SPH / PIC)](#particle-methods-md--dem--sph--pic)
- [Acoustics / vibroacoustics](#acoustics--vibroacoustics)
- [Combustion / reacting flows](#combustion--reacting-flows)
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

### FreeFEM / SfePy / Firedrake
PDE/FEM platforms with DSL or Python interfaces for custom physics and research.

- https://freefem.org/ — https://github.com/FreeFem/FreeFem-sources
- https://sfepy.org/ — https://github.com/sfepy/sfepy
- https://www.firedrakeproject.org/ — https://github.com/firedrakeproject/firedrake

### MOOSE / libMesh / GetDP
Multiphysics Object-Oriented Simulation Environment (built on libMesh); GetDP for coupled FEM (often with Gmsh/ONELAB).

- https://mooseframework.inl.gov/ — https://github.com/idaholab/moose
- https://libmesh.github.io/ — https://github.com/libMesh/libmesh
- https://getdp.info/ — https://gitlab.onelab.info/getdp/getdp

### FrontISTR / MYSTRAN / FEBio / NGSolve
Large-scale nonlinear structures (FrontISTR); Nastran-like analysis (MYSTRAN); biomechanics nonlinear FEM (FEBio); Netgen + NGSolve FEM platform.

- https://www.frontistr.com/ — https://github.com/FrontISTR/FrontISTR
- https://mystran.com/ — https://github.com/dr-bill-c/MYSTRAN
- https://febio.org/ — https://github.com/febiosoftware/FEBio
- https://ngsolve.org/ — https://github.com/NGSolve/ngsolve

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
Most widely used open-source CFD toolbox — incompressible/compressible flow, heat transfer, multiphase, reactions; large ecosystem.

- https://www.openfoam.com/
- https://openfoam.org/
- https://github.com/OpenFOAM/OpenFOAM-dev

### SU2
Multiphysics PDE solver with gradient-based aerodynamic shape optimization and adjoint capabilities.

- https://su2code.github.io/
- https://github.com/su2code/SU2

### Nektar++ / Lethe
Spectral/hp element CFD (Nektar++); high-order CG CFD–DEM (Lethe).

- https://www.nektar.info/ — https://github.com/Nektar/Nektar
- https://lethe-cfd.github.io/lethe/ — https://github.com/lethe-cfd/lethe

### Palabos / waLBerla / OpenLB
Lattice Boltzmann Method (LBM) CFD frameworks for complex flows and HPC.

- https://palabos.unige.ch/ — https://gitlab.com/unigespc/palabos
- https://www.walberla.net/ — https://github.com/walberla/walberla
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

---

## Multibody / structural dynamics

Rigid and flexible multibody dynamics, mechanisms, and vehicle/robot simulation.

### Project Chrono
Multiphysics multibody platform — vehicles, robots, granular/DEM contact, FEA co-simulation.

- https://projectchrono.org/
- https://github.com/projectchrono/chrono

### MBDyn / Simbody / EXUDYN
General-purpose MBD (MBDyn); articulated biomechanics/robotics (Simbody); Python/C++ flexible multibody (EXUDYN).

- https://www.mbdyn.org/ — https://github.com/mbdyn/mbdyn
- https://github.com/simbody/simbody
- https://github.com/jgerstmayr/EXUDYN

### OpenSim / Pinocchio / Drake
Musculoskeletal dynamics (OpenSim); fast rigid-body dynamics for robotics (Pinocchio); robotics & control toolbox with dynamics (Drake).

- https://opensim.stanford.edu/ — https://github.com/opensim-org
- https://github.com/stack-of-tasks/pinocchio
- https://drake.mit.edu/ — https://github.com/RobotLocomotion/drake

### OpenFAST
NREL aero-servo-elastic wind turbine dynamics (coupled CFD/structural loads workflows).

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
- https://github.com/AndreaAmicarelli/SPHERA
- https://pysph.readthedocs.io/ — https://github.com/pypr/pysph

### LIGGGHTS / Yade / MercuryDPM
DEM for granular materials and industrial particle processes.

- https://www.cfdem.com/liggghtsolf — https://github.com/CFDEMproject/LIGGGHTS-PUBLIC
- https://yade-dem.org/ — https://gitlab.com/yade-dev/trunk
- https://www.mercurydpm.org/ — https://github.com/MercuryDPM/MercuryDPM

### WarpX / PIConGPU / Smilei
Exascale electromagnetic PIC (WarpX); GPU PIC (PIConGPU); plasma PIC (Smilei).

- https://warpx.readthedocs.io/ — https://github.com/ECP-WarpX/WarpX
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
MATLAB/C++ toolbox for time-domain acoustic and ultrasound wavefields.

- http://www.k-wave.org/
- https://github.com/ucl-bug/k-wave

### GetDP / ONELAB acoustics
Coupled FEM acoustics and multiphysics via GetDP + Gmsh/ONELAB workflows.

- https://getdp.info/
- https://onelab.info/

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
AMReX-based compressible and low-Mach reacting flow solvers (DOE Exascale combustion stack).

- https://amrex-combustion.github.io/
- https://github.com/AMReX-Combustion

### CoolProp
Open-source thermodynamic and transport properties (useful adjunct for reacting-flow workflows).

- https://coolprop.org/
- https://github.com/CoolProp/CoolProp

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
- https://wiki.fysik.dtu.dk/gpaw/ — https://gitlab.com/gpaw/gpaw

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

- https://eigen.tuxfamily.org/ — https://gitlab.com/libeigen/eigen
- https://www.openblas.net/ — https://github.com/OpenMathLib/OpenBLAS

### Dakota
Sandia toolkit for optimization, UQ, and model calibration wrapped around simulation codes.

- https://dakota.sandia.gov/
- https://github.com/snl-dakota/dakota

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
