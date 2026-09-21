# Awesome Open-Source Solvers（日本語）

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[English README](README.md)

オープンソースの**ソルバ**と科学計算スタックのキュレーション — FEM、BEM、CFD、マルチボディ／ダイナミクス、粒子法、音響、燃焼、量子、および線形代数・メッシュ補助。公式ドキュメントや GitHub のある耐久性の高いプロジェクトを優先。CAD/CAE リストとの重複は可。本リストは CAD アプリではなく**ソルバ**に焦点を当てる。

## 目次

- [有限要素法（FEM）](#有限要素法fem)
- [境界要素法（BEM）](#境界要素法bem)
- [CFD](#cfd)
- [マルチボディ／構造ダイナミクス](#マルチボディ構造ダイナミクス)
- [粒子法（MD / DEM / SPH / PIC）](#粒子法md--dem--sph--pic)
- [音響／構造音響](#音響構造音響)
- [燃焼／反応流れ](#燃焼反応流れ)
- [量子／電子構造／量子ダイナミクス](#量子電子構造量子ダイナミクス)
- [線形代数と並列ソルバ](#線形代数と並列ソルバ)
- [メッシュ／プリポスト（簡潔）](#メッシュプリポスト簡潔)
- [関連リスト](#関連リスト)
- [コントリビューション](#コントリビューション)

---

## 有限要素法（FEM）

構造・熱・マルチフィジックス PDE 向けのライブラリおよび産業／研究用 FEM コード。

### deal.II
適応・並列・行列フリー離散化向けの C++ FEM ライブラリ。ノート PC から HPC まで。チュートリアルとコミュニティが充実。

- https://dealii.org/
- https://github.com/dealii/dealii

### FEniCS / DOLFINx
変分定式化と連成 PDE を迅速に書ける Python ファーストの FEM プラットフォーム（FEniCSx / DOLFINx）。

- https://fenicsproject.org/
- https://github.com/FEniCS

### MFEM
高次手法・GPU/HPC・研究向け離散化（Galerkin、DG、混合、DPG）のための軽量でスケーラブルな C++ FEM ツールボックス。

- https://mfem.org/
- https://github.com/mfem/mfem

### CalculiX
Abaqus 風のオープンソース 3D 構造 FEM（ccx ソルバ + cgx）。FreeCAD FEM や PrePoMax GUI と広く併用。

- https://www.dhondt.de/
- https://github.com/Dhondtguido/CalculiX
- https://github.com/calculix

### Code_Aster
EDF の産業向け構造力学／マルチフィジックス FEM スイート。プリ／ポストは SALOME-Meca と組み合わせることが多い。

- https://code-aster.org/
- https://gitlab.com/codeaster

### Elmer
流体・固体・電磁・熱および連成問題向けのオープンなマルチフィジックス FEM。GUI と並列ソルバあり。

- https://www.elmerfem.org/
- https://github.com/ElmerCSC/elmerfem

### FreeFEM / SfePy / Firedrake
カスタム物理や研究向けに、DSL または Python インタフェースを持つ PDE/FEM プラットフォーム。

- https://freefem.org/ — https://github.com/FreeFem/FreeFem-sources
- https://sfepy.org/ — https://github.com/sfepy/sfepy
- https://www.firedrakeproject.org/ — https://github.com/firedrakeproject/firedrake

### MOOSE / libMesh / GetDP
libMesh 上のマルチフィジックス環境（MOOSE）。GetDP は連成 FEM（しばしば Gmsh/ONELAB と併用）。

- https://mooseframework.inl.gov/ — https://github.com/idaholab/moose
- https://libmesh.github.io/ — https://github.com/libMesh/libmesh
- https://getdp.info/ — https://gitlab.onelab.info/getdp/getdp

### FrontISTR / MYSTRAN / FEBio / NGSolve
大規模非線形構造（FrontISTR）；Nastran 風解析（MYSTRAN）；生体力学の非線形 FEM（FEBio）；Netgen + NGSolve FEM プラットフォーム。

- https://www.frontistr.com/ — https://github.com/FrontISTR/FrontISTR
- https://mystran.com/ — https://github.com/dr-bill-c/MYSTRAN
- https://febio.org/ — https://github.com/febiosoftware/FEBio
- https://ngsolve.org/ — https://github.com/NGSolve/ngsolve

---

## 境界要素法（BEM）

音響・電磁・外部問題向けの表面積分ソルバ。

### Bempp
静電・音響・電磁向けの Python BEM プラットフォーム。Gmsh/VTK I/O、FEniCS による FEM–BEM 連成も可能。

- https://bempp.com/
- https://github.com/bempp

### scuff-em
電磁散乱、Casimir／放射熱伝達、ナノフォトニクス向け BEM スイート（EFIE / PMCHWT、RWG 基底）。

- http://homerreid.github.io/scuff-em-documentation/
- https://github.com/HomerReid/scuff-em

### OpenBEM
2D／3D 幾何向けの MATLAB Helmholtz／音響 BEM コード集。

- https://openbem.dk/

### BEMUSE / NiHu
研究寄りの BEM ライブラリ（音響／工学向け BEM スタック）。

- https://github.com/BEMUSE/BEMUSE
- https://github.com/nikolaszk/NiHu

---

## CFD

有限体積・有限要素・格子ボルツマンによる流体ソルバ。

### OpenFOAM
最も広く使われるオープンソース CFD ツールボックス — 非圧縮／圧縮流れ、伝熱、多相、反応。大きな生態系。

- https://www.openfoam.com/
- https://openfoam.org/
- https://github.com/OpenFOAM/OpenFOAM-dev

### SU2
勾配ベースの空力形状最適化と随伴機能を備えたマルチフィジックス PDE ソルバ。

- https://su2code.github.io/
- https://github.com/su2code/SU2

### Nektar++ / deal.II CFD / Lethe
スペクトル／hp 要素 CFD（Nektar++）；高次 CG CFD–DEM（Lethe）。多くの CFD が deal.II / MFEM 上にも構築される。

- https://www.nektar.info/ — https://github.com/Nektar/Nektar
- https://lethe-cfd.github.io/lethe/ — https://github.com/lethe-cfd/lethe

### Palabos / waLBerla / OpenLB
複雑流れと HPC 向けの格子ボルツマン法（LBM）CFD フレームワーク。

- https://palabos.unige.ch/ — https://gitlab.com/unigespc/palabos
- https://www.walberla.net/ — https://github.com/walberla/walberla
- https://www.openlb.net/ — https://gitlab.com/openlb/release

### Fire Dynamics Simulator (FDS)
NIST の火災駆動流れ CFD。Smokeview 可視化付き。

- https://pages.nist.gov/fds-smv/
- https://github.com/firemodels/fds

### Code_Saturne / Fluidity / Nek5000 / nekRS
EDF 産業向け CFD（Code_Saturne）；FE/FV 流体（Fluidity）；スペクトル要素 CFD（Nek5000 / nekRS）。

- https://www.code-saturne.org/
- https://fluidityproject.github.io/
- https://nek5000.mcs.anl.gov/ — https://github.com/Nek5000/Nek5000
- https://github.com/Nek5000/nekRS

---

## マルチボディ／構造ダイナミクス

剛体・柔軟マルチボディ、機構、車両／ロボットシミュレーション。

### Project Chrono
車両・ロボット・粉体／DEM 接触・FEA 連成などのマルチフィジックス・マルチボディ基盤。

- https://projectchrono.org/
- https://github.com/projectchrono/chrono

### MBDyn / Simbody / EXUDYN
汎用 MBD（MBDyn）；関節付き生体力学／ロボティクス（Simbody）；Python/C++ 柔軟マルチボディ（EXUDYN）。

- https://www.mbdyn.org/ — https://github.com/mbdyn/mbdyn
- https://github.com/simbody/simbody
- https://github.com/jgerstmayr/EXUDYN

### OpenSim / Pinocchio / Drake
筋骨格ダイナミクス（OpenSim）；ロボティクス向け高速剛体ダイナミクス（Pinocchio）；ダイナミクス付きロボティクス／制御（Drake）。

- https://opensim.stanford.edu/ — https://github.com/opensim-org
- https://github.com/stack-of-tasks/pinocchio
- https://drake.mit.edu/ — https://github.com/RobotLocomotion/drake

### OpenFAST
NREL の空力・サーボ・弾性風力タービンダイナミクス（CFD／構造荷重連成ワークフロー）。

- https://openfast.readthedocs.io/
- https://github.com/OpenFAST/openfast

---

## 粒子法（MD / DEM / SPH / PIC）

分子動力学、離散要素、SPH、粒子インセルのコード。

### LAMMPS
大規模原子／分子質量並列シミュレータ — 材料 MD、粗視化・メソスケール粒子モデル。

- https://www.lammps.org/
- https://github.com/lammps/lammps

### GROMACS
生体分子・ソフトマター向け高性能分子動力学。GPU サポートが強い。

- https://www.gromacs.org/
- https://github.com/gromacs/gromacs

### DualSPHysics / SPHERA / PySPH
自由表面／沿岸／産業流れの SPH（DualSPHysics）；工学 SPH（SPHERA）；Python SPH フレームワーク（PySPH）。

- https://dual.sphysics.org/ — https://github.com/DualSPHysics/DualSPHysics
- https://github.com/AndreaAmicarelli/SPHERA
- https://pysph.readthedocs.io/ — https://github.com/pypr/pysph

### LIGGGHTS / Yade / MercuryDPM
粉粒体・産業粒子プロセス向け DEM（LAMMPS 関連または専用 DEM スタック）。

- https://www.cfdem.com/liggghtsolf — https://github.com/CFDEMproject/LIGGGHTS-PUBLIC
- https://yade-dem.org/ — https://gitlab.com/yade-dev/trunk
- https://www.mercurydpm.org/ — https://github.com/MercuryDPM/MercuryDPM

### WarpX / PIConGPU / Smilei
エクサスケール電磁 PIC（WarpX）；GPU PIC（PIConGPU）；プラズマ PIC（Smilei）。

- https://warpx.readthedocs.io/ — https://github.com/ECP-WarpX/WarpX
- https://picongpu.readthedocs.io/ — https://github.com/ComputationalRadiationPhysics/picongpu
- https://smileipic.github.io/Smilei/ — https://github.com/SmileiPIC/Smilei

### HOOMD-blue / OpenMM
ソフトマター向け GPU 加速 MD（HOOMD-blue）；高性能生体分子 MD ツールキット（OpenMM）。

- https://glotzerlab.engin.umich.edu/hoomd-blue/ — https://github.com/glotzerlab/hoomd-blue
- https://openmm.org/ — https://github.com/openmm/openmm

---

## 音響／構造音響

波動伝播、室内／屋外音響、連成構造音響ソルバ。

### Code_Aster / CalculiX / Elmer（構造音響）
産業向け FEM スイートによる構造–音響連成（FEM 節を参照）。Elmer と Code_Aster には音響／連成モジュールがある。

- https://code-aster.org/
- https://www.elmerfem.org/

### Bempp / OpenBEM（音響 BEM）
境界要素による外部／内部 Helmholtz 音響（BEM 節を参照）。

- https://bempp.com/
- https://openbem.dk/

### K-Wave / AcouSTO
時間領域の音響／超音波波動場向け MATLAB/C++ ツールボックス（k-Wave）；研究用音響ソルバ（AcouSTO）。

- http://www.k-wave.org/ — https://github.com/ucl-bug/k-wave
- https://github.com/AntoninoM/AcouSTO

### GetDP / ONELAB 音響
GetDP + Gmsh/ONELAB ワークフローによる連成 FEM 音響とマルチフィジックス。

- https://getdp.info/
- https://onelab.info/

---

## 燃焼／反応流れ

化学反応速度論、反応 CFD、火災／燃焼パッケージ。

### Cantera
化学反応速度・熱力学・輸送ライブラリ — 反応機構、0D/1D 反応器、CFD 連成。

- https://cantera.org/
- https://github.com/Cantera/cantera

### OpenFOAM 反応／燃焼ソルバ
OpenFOAM ツールボックス上の reactingEulerFoam / chemFoam / combustion パッケージおよびコミュニティ燃焼フォーク。

- https://www.openfoam.com/documentation/
- https://openfoam.org/

### Fire Dynamics Simulator (FDS)
火災駆動の反応浮力流れ（CFD 節も参照）。

- https://pages.nist.gov/fds-smv/
- https://github.com/firemodels/fds

### PeleC / PeleLMeX / PelePhysics
AMReX ベースの圧縮性／低マッハ反応流れソルバ（DOE エクサスケール燃焼スタック）。

- https://amrex-combustion.github.io/
- https://github.com/AMReX-Combustion

### CoolProp（物性補助）
OSS ワークフローでは Cantera や CoolProp など完全オープンな物性スタックを優先。

- https://coolprop.org/ — https://github.com/CoolProp/CoolProp

---

## 量子／電子構造／量子ダイナミクス

DFT、多体電子構造、開放量子系。

### Quantum ESPRESSO
材料・分子向け平面波 DFT／電子構造スイート。大きなユーザコミュニティ。

- https://www.quantum-espresso.org/
- https://gitlab.com/QEF/q-e

### ABINIT / CP2K / SIESTA / GPAW
固体・化学・ナノ系向けの平面波および局在軌道 DFT コード。

- https://www.abinit.org/ — https://github.com/abinit/abinit
- https://www.cp2k.org/ — https://github.com/cp2k/cp2k
- https://departments.icmab.es/leem/siesta/ — https://gitlab.com/siesta-project/siesta
- https://wiki.fysik.dtu.dk/gpaw/ — https://gitlab.com/gpaw/gpaw

### QuTiP
Python の量子ツールボックス — 開放量子系、マスター方程式、量子光学ダイナミクス。

- https://qutip.org/
- https://github.com/qutip/qutip

### NWChem / Psi4 / PySCF
計算化学スイート（NWChem）；量子化学（Psi4）；Python 量子化学（PySCF）。

- https://nwchemgit.github.io/ — https://github.com/nwchemgit/nwchem
- https://psicode.org/ — https://github.com/psi4/psi4
- https://pyscf.org/ — https://github.com/pyscf/pyscf

### Yambo / BerkeleyGW / Octopus
多体摂動論／GW-BSE（Yambo、BerkeleyGW）；実空間 TDDFT（Octopus）。

- https://www.yambo-code.eu/ — https://github.com/yambo-code/yambo
- https://berkeleygw.org/ — https://github.com/BerkeleyGW/BGW-public
- https://octopus-code.org/ — https://gitlab.com/octopus-code/octopus

---

## 線形代数と並列ソルバ

上記の多くのコードを支える疎行列反復／直接ソルバと HPC 数値ライブラリ。

### PETSc（+ TAO）
科学計算向けポータブル拡張ツールキット — Krylov ソルバ、前処理、非線形／時間積分、TAO 最適化。C/Fortran/Python（petsc4py）。

- https://petsc.org/
- https://gitlab.com/petsc/petsc
- https://github.com/petsc/petsc

### Trilinos
HPC 線形代数・ソルバ・離散化・マルチフィジックス向けパッケージ群（Belos、Ifpack2、MueLu、Tpetra など）。

- https://trilinos.github.io/
- https://github.com/trilinos/Trilinos

### hypre
大規模疎行列向け高性能並列マルチグリッド前処理・ソルバ（BoomerAMG など）。

- https://www.llnl.gov/casc/hypre/
- https://github.com/hypre-space/hypre

### SuperLU / MUMPS / SuiteSparse
疎行列直接ソルバ — SuperLU / SuperLU_DIST；MUMPS マルチフロンタル；SuiteSparse（UMFPACK、CHOLMOD、SPQR など）。

- https://portal.nersc.gov/project/sparse/superlu/ — https://github.com/xiaoyeli/superlu
- https://mumps-solver.org/
- https://people.engr.tamu.edu/davis/suitesparse.html — https://github.com/DrTimothyAldenDavis/SuiteSparse

### Eigen / Armadillo / BLAS-LAPACK スタック
多くのソルバ内部で使われる密行列線形代数の部品（OpenBLAS などのベンダー BLAS も含む）。

- https://eigen.tuxfamily.org/ — https://gitlab.com/libeigen/eigen
- https://arma.sourceforge.net/
- https://www.openblas.net/ — https://github.com/OpenMathLib/OpenBLAS

### Dakota
シミュレーションコードを包む Sandia の最適化・UQ・モデル校正ツールキット。

- https://dakota.sandia.gov/
- https://github.com/snl-dakota/dakota

---

## メッシュ／プリポスト（簡潔）

上記ソルバと組み合わせる幾何メッシングと可視化（フル CAD リストではない）。

### Gmsh
CAD カーネルオプション、`.geo` スクリプト、ポスト処理を備えたオープンソース 3D FE メッシュ生成器。

- https://gmsh.info/
- https://gitlab.onelab.info/gmsh/gmsh

### Netgen / SALOME / meshio
四面体メッシング（Netgen）；CAD／メッシュのプリポスト（SALOME）；Python メッシュ形式 I/O（meshio）。

- https://ngsolve.org/ — https://github.com/NGSolve/netgen
- https://www.salome-platform.org/
- https://github.com/nschloe/meshio

### ParaView / VTK / VisIt
CFD/FEM 結果の科学可視化（ParaView、VTK）；大規模並列データ向け VisIt。

- https://www.paraview.org/ — https://github.com/Kitware/ParaView
- https://vtk.org/ — https://github.com/Kitware/VTK
- https://visit-dav.github.io/visit-website/ — https://github.com/visit-dav/visit

---

## 関連リスト

- https://github.com/shvyac/awesome-cad-cae — CAD / CAE / EDA / フォーマット（より広いツールチェーン）
- https://github.com/mlightcad/awesome-cad — オープンソース CAD ソフトウェアとライブラリ
- https://github.com/fffaraz/awesome-cpp — C++ リソース（多くのソルバスタック）
- https://awesome.re/ — Awesome manifesto

---

## コントリビューション

PR と issue を歓迎。耐久性のある公式または GitHub URL、短い説明、明確なカテゴリ適合を持つ**オープンソースソルバ**を優先。CAD のみのアプリは避け、[awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae) へ誘導。EN と JA の README を同期すること。

本リストのライセンス：可能な範囲でパブリックドメイン相当。リンク先プロジェクトは各々のライセンス（GPL、LGPL、BSD、Apache-2.0 など）を保持。
