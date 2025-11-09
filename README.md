# Awesome Photonics [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of awesome resource for photonic engineers, physicists and hobbyists

Most tools in this list are written or have a python interface, which require some basic knowledge of python. If you are new to python you can find many [books](https://jakevdp.github.io/PythonDataScienceHandbook/index.html), [YouTube videos](https://www.youtube.com/c/anthonywritescode) and [courses](https://github.com/joamatab/practical-python) available online.
If you are new to Git and Python I recommend reading this [article](https://lightlab.readthedocs.io/en/latest/_static/gettingStarted/index.html)

## Contents

<!-- toc -->

- [layout](#layout): define the geometrical shapes that guide the light.
- [simulation](#simulation): simulate how photons propagate, and optimize the geometrical shapes
- [lab automation](#lab-automation): Control instruments in the lab
- [data analysis](#data-analysis)
- [visualization](#visualizatio)
- [electronics](#electronics)
- [other links](#other-links)

<!-- tocstop -->

## layout

- [gdsfactory](https://gdsfactory.github.io/gdsfactory/) [code](https://github.com/gdsfactory/gdsfactory) - includes plugins to other tools.
    - [gplugins](https://gdsfactory.github.io/gplugins)
    - [ubcpdk](https://gdsfactory.github.io/ubc) and [code](https://github.com/gdsfactory/ubc)
    - [skywater130](https://gdsfactory.github.io/skywater130) and [code](https://github.com/gdsfactory/skywater130)
    - [gf180](https://gdsfactory.github.io/gf180)
    - [vtt](https://gdsfactory.github.io/vtt)
- [gdstk](https://github.com/heitzmann/gdstk) - faster than gdspy (from same author)
  - [pyphotonics](https://github.com/rohanku/pyphotonics)
- [gdspy based tools](https://github.com/heitzmann/gdspy)
  - [phidl](https://github.com/amccaugh/phidl) - made for superconducting detectors
    - soen-pdk [docs](https://pages.nist.gov/SOEN-PDK/) and [code](https://github.com/usnistgov/SOEN-PDK)
  - [picwriter](https://github.com/DerekK88/PICwriter)
  - [BerkeleyPhotonicsGenerator](https://github.com/BerkeleyPhotonicsGenerator/BPG)
  - [Ayar cell generator](https://github.com/AyarLabs/ACG)
- [klayout](https://github.com/KLayout/klayout) - layout viewer with python API
  - [kfactory](https://github.com/gdsfactory/kfactory)
  - [zero-pdk](https://github.com/lightwave-lab/zeropdk) - klayout pure python pdk.
  - [flayout](https://github.com/flaport/flayout/)
  - [xsection, klayout-ipc, klayout-gadgets, lytest, lymask](https://github.com/atait?tab=repositories)
  - [KQcircuits](https://github.com/iqm-finland/KQCircuits) - Quantum circuits pdk.
  - [siepic-tools](https://github.com/lukasc-ubc/SiEPIC-Tools) - code driven PCells and GUI driven layouts.
  - [siepic-ebeam-pdk](https://github.com/lukasc-ubc/SiEPIC_EBeam_PDK)
  - [gds3xtrude](https://codeberg.org/tok)
  - [spicex: netlist extraction](https://github.com/fsitok/spicex)
  - [simplify polygons](https://github.com/fsitok/klayout-simplify)
  - [klayout python](https://github.com/shamil777/KLayout-python)
  - [klayout cross-section in python](https://github.com/gdsfactory/klayout_pyxs) - Port from ruby to python to xsection macro
- shapely based tools
  - [gdshelpers](https://github.com/HelgeGehring/gdshelpers) - includes superconducting detectors.
  - [dphox](https://github.com/solgaardlab/dphox) - includes 3D MEMs structures
- [masque](https://mpxd.net/code/jan/masque)
- [klamath](https://mpxd.net/code/jan/klamath)
- [nazca](https://nazca-design.org/download/)
- [qiskit-metal](https://github.com/Qiskit/qiskit-metal) - IBM superconducting based qubits.

- layout viewers
  - [klayout](https://www.klayout.de/) - Best open source layout viewer.
  - [kweb](https://github.com/gdsfactory/kweb)
  - [GDS3D](https://github.com/trilomix/GDS3D/)
  - [GDS2WebGL](https://github.com/s-holst/GDS2WebGL)

## simulation

- mode solver:

  - Finite Element
    - [femwell](https://helgegehring.github.io/femwell/)
    - [elmer](https://github.com/elmercsc/elmerfem)
    - [palace](https://awslabs.github.io/palace/stable/)
    - [ngsolve](https://github.com/NGSolve/ngsolve)
    - [jax-fem](https://github.com/deepmodeling/jax-fem)
     
  - Finite Difference
    - [tidy3d](https://github.com/flexcompute/tidy3d) Mode solver is open source
    - [khronos](https://github.com/facebookresearch/Khronos.jl)
    - [modes](https://modes.readthedocs.io/en/latest/)
    - [mpb](https://mpb.readthedocs.io/en/latest/Scheme_Tutorial/) - Bloch mode solver.
    - [EMpy](https://github.com/lbolla/EMpy)
    - [philsol](https://github.com/philmain28/philsol) - Allows bends.
    - [pymode](https://github.com/smartalecH/pyMode) - Allows bends.
      - [wgms3d](http://www.soundtracker.org/raw/wgms3d/)
    - [pyMWM](https://github.com/mnishida/PyMWM)
    - [mpb](https://mpb.readthedocs.io/en/latest/Scheme_Tutorial/) - Bloch mode solver.
    - [protis](https://protis.gitlab.io) - Bloch mode solver (2D only), support for multiple backends (numpy/autograd/torch/jax)

- component design:

  - FDTD - Finite differences time domain.
    - [khronos](https://github.com/facebookresearch/Khronos.jl)
    - [fdtdx](https://github.com/ymahlau/fdtdx)
    - [Luminescent](https://github.com/paulxshen/Luminescent.jl)
    - [fdtdz](https://github.com/spinsphotonics/fdtdz)
    - [meep FDTD](https://github.com/NanoComp/meep)
      - [meep ipkiss integration](https://github.com/luceda/ipkiss_meep_integration)
      - [meep docker image](https://hub.docker.com/r/mochen4/meepdocker) - [code](https://github.com/mochen4/meepdocker)
      - [grating coupler example](https://github.com/simbilod/grating_coupler_meep)
    - [emopt FDTD](https://github.com/anstmichaels/emopt)
    - [Python 3D FDTD simulator](https://github.com/flaport/fdtd) - Written in PyTorch.
    - tidy3d client [docs](https://docs.simulation.cloud/projects/tidy3d/en/latest/) and [code](https://github.com/flexcompute/tidy3d) - Server is propietary.
    - [GSvit](http://gsvit.net/) - GPU support
    - [ARTEMIS](https://github.com/AMReX-Microelectronics/artemis) - High-performance FDTD solver coupled with magnetization dynamics (LLG), GPU-accelerated for microelectronics and superconducting devices
  - FDFD - Finite differences frequency domain.
    - [spins FDFD on GPU](https://github.com/stanfordnqp/spins-b)
    - [ceviche (2D only) FDTD and FDFD](https://github.com/twhughes/ceviche)
    - [jaxwell](https://github.com/stanfordnqp/jaxwell)
  - EME - Eigen mode expansion.
    - [meow](https://github.com/flaport/meow)
    - [emepy](https://github.com/BYUCamachoLab/emepy)
    - [CAMFR](https://github.com/demisjohn/CAMFR)
  - FEM:
    - [gyptis](https://gyptis.gitlab.io) - based on FEniCS, automatic differentiation with dolfin-adjoint
  - RCWA:
    - [FMMAX](https://github.com/facebookresearch/fmmax)
    - [S4](https://github.com/victorliu/S4)
    - [grcwa](https://github.com/weiliangjinca/grcwa) - automatic differentiation included with autograd
    - [nannos](https://nannos.gitlab.io) - support for multiple backends (numpy/autograd/torch/jax)
    - [inkstone](https://github.com/alexysong/inkstone)
  - [Bempp](https://bempp.com) - Open-source computational boundary element platform to solve electrostatic, acoustic and electromagnetic problems
  - [OpenModes](https://openmodes.readthedocs.io) - Mode solver for open electromagnetic structures based on the method of moments (MOM)
  - [Sipkit](https://github.com/Photonic-Architecture-Laboratories/si-photonics-toolkit) - A JAX-compatible toolkit providing fundamental waveguide and material properties to aid in the design of silicon photonic components.
  - [pyGDM](https://homepages.laas.fr/pwiecha/pygdm_doc/) - Green dyadic method for nanophotonics, including evolutionary optimization
  - [SiPANN (neural networks for photonics component design)](https://github.com/contagon/SiPANN)
  - [Lightening-Transformer: A Dynamically-operated Optically-interconnected Photonic Transformer Accelerator](https://github.com/zhuhanqing/Lightening-Transformer)
  - [inverse design](http://metanet.stanford.edu/code/)
    - [glonet: global optimization based on generative neural networks](https://github.com/jonfanlab/GLOnet)
    - [wavetorch](https://github.com/fancompute/wavetorch)
    - [lumopt](https://github.com/chriskeraly/lumopt)
    - [angler](https://github.com/fancompute/angler/) - Frequency-domain photonic simulation and inverse design optimization for linear and nonlinear devices.
    - SPLayout [code](https://github.com/Hideousmon/SPLayout) [docs](https://splayout.readthedocs.io/en/latest/index.html)
    - ceviche-challenges [code](https://github.com/google/ceviche-challenges) - Photonic inverse designs based on the FDFD simulator Ceviche
    - [NIDN](https://github.com/esa/NIDN) - Inverse design of metamaterials, photonic crystals, ... using PyTorch
    - A Neural Operator-based Surrogate Solver for Free-Form Electromagnetic Inverse Design [[Paper](https://arxiv.org/pdf/2302.01934.pdf)] [[Github](https://github.com/tfp-photonics/neurop_invdes)]
  - [TCAD](https://tcadcentral.com/Software.html#open-source-tcad-software) [tcad repos](https://github.com/thesourcerer8/OpenSourceTCAD) [TCAD Overview spreadsheet here](https://docs.google.com/spreadsheets/d/1dK1GxGl1C7v3rhWKw3RcbeZsRre66HPAOPFbgYni74A/edit?pli=1#gid=0)
    - [devsim](https://devsim.org/) - Semiconductor Device Simulator
    - [BOSIM](https://eexu.home.ece.ust.hk/BOSIM.html)
    - [Suprem4](https://github.com/cogenda/Suprem4) - Process simulator (no python)
    - [pisces](https://github.com/ComputerWhisperer/pisces) - Poison and continuity equation solver (no python)
    - [TCAD docker containers](https://github.com/thesourcerer8/OpenSourceTCAD)
    - [Charon](https://charon.sandia.gov/) - Paralell TCAD simulator. [GitHub mirror](https://github.com/tcadsoftware/charon)
  - ray tracing:
    - [ray tracing](https://github.com/DCC-Lab/RayTracing)
    - [rayopt](https://github.com/quartiq/rayopt)
    - [rayoptics](https://github.com/mjhoptics/ray-optics) - Optical design and analysis in Python
    - [optiland](https://github.com/HarrisonKramer/optiland) - Comprehensive optical design with GPU-accelerated ray tracing via PyTorch
    - [pyrate](https://github.com/mess42/pyrate) - Optical raytracing based on Python
    - [scattering tools](https://github.com/rafael-fuente/diffractsim)
  - adaptive optics
    - [AOtools](https://github.com/AOtools)
  - multisolvers
    - [simphox (FDTD, beamPropagation, circuit simulation)](https://github.com/fancompute/simphox)
  - transfer matrix
    - [TMM](https://github.com/sbyrnes321/tmm)
    - [tmmax](https://github.com/bahremsd/tmmax)
    - [PyElli](https://github.com/PyEllips/pyElli) - Toolkit for 1D optical simulations, with a focus on ellipsometry

- circuit simulation:

  - Sparameter linear solvers
      * SAX [code](https://github.com/flaport/sax) and [docs](https://flaport.github.io/sax/) - Differentiable circuit solver.
      * [lekkersim](https://github.com/mpasson/lekkersim)
      * [simphony (linear circuit solver)](https://github.com/BYUCamachoLab/simphony)
      * [photontorch docs](https://docs.photontorch.com/) - [code](https://github.com/flaport/photontorch) - Includes time domain.
      * [opics](https://github.com/siepic/opics)
      * [SignalIntegrity (linear circuit simulation)](https://github.com/TeledyneLeCroy/SignalIntegrity)
      * [scikit-rf RF simulator](https://scikit-rf.readthedocs.io/en/latest/)
  - pyFDA filter design [code](https://github.com/chipmuenk/pyfda) and [docs](https://pyfda.readthedocs.io/en/latest/manual/input_specs.html)
  - Optical communications
    - [optiCommPy](https://github.com/edsonportosilva/OptiCommPy)
    - [QAMpy](https://github.com/ChalmersPhotonicsLab/QAMpy) - DSP chain for simulation and equalisation of optical communications signals
  - RF photonic link analysis
    - [Princeton RF photonic notebooks](https://github.com/ericcblow/MWP_RF_Sims/tree/main)
  - Spice
    - [Xyce](https://xyce.sandia.gov/) - open source, SPICE-compatible, high-performance analog circuit simulator.
    - [lcapy](https://github.com/mph-/lcapy) - Linear circuit analysis.
    - [pyspice](https://github.com/FabriceSalvaire/PySpice)
    - [VACASK](https://codeberg.org/arpadbuermen/VACASK) Verilog-A
    - [openVAF](https://github.com/pascalkuthe/OpenVAF) Verilog-A

- nonlinear schrodinger equation (NLSE): calculate the propagation of pulses along a fiber/waveguide in the presence of dispersion and nonlinearity.
    - [Laserfun](https://github.com/DanHickstein/laserfun) aims for simplicity
    - [PyNLO](https://github.com/pyNLO/PyNLO) more capable, but unmaintained
    - [PyNLO fork includes Chi2 simulation capabilities](https://cdfredrick.github.io/PyNLO/build/html/index.html)
- Lugiato Lefever Equation (LLE) to calculate propagation in ring resonators:
    - [PyGLLE](https://github.com/omelchert/pyGLLE) is nice and simple
    - [PyLLE](https://github.com/gregmoille/pyLLE) has more features

- material database

  - [rii pandas](https://github.com/mnishida/RII_Pandas)

- lithography simulation
  - [optolithium](https://github.com/xthebat/optolithium)
  - [notebooks](https://github.com/pierremifasol/Lithography-Simulation)
  - [dimmilitho](https://github.com/vincentlv/DimmiLitho)
  - [keras based litho model](https://github.com/Dusandinho/PreFab.git)

- free space
  - [diffractsim](https://github.com/rafael-fuente/diffractsim)
  - [waveprop](https://github.com/HelgeGehring/wavepropagation/)
  - [lightpipes](https://github.com/opticspy/lightpipes)
  - [TorchOptics](https://github.com/matthewfilipovich/torchoptics)
  - [POPPY](https://github.com/mperrin/poppy) - Physical Optics Propagation in Python for diffraction modeling
  - [prysm](https://github.com/brandondube/prysm) - Physical optics with integrated modeling, phase retrieval, segmented systems
  - [HCIPy](https://github.com/ehpor/hcipy) - High Contrast Imaging for Python
  - [Poke](https://github.com/Jashcraf/poke) - Polarization ray tracing and Gaussian beamlet module

## verification

- parasitic extraction
    - [speedsterpy](https://github.com/das-dias/speedsterpy)

## lab automation

- backend:

  - [PyVISA](https://pyvisa.readthedocs.io/en/latest/) - Allows you to control the lab instruments with python. As the backend you can use NI or [PyVISA-py](https://pyvisa-py.readthedocs.io/en/latest/).
  - [PySerial](https://github.com/pyserial/pyserial) - Issue simple serial commands (RS-232, RS485) to instruments (and read data).

- lab automation repos:
  - [pymeasure](https://github.com/pymeasure/pymeasure)
  - [autolab](https://github.com/autolab-project)
  - [autosweep](https://github.com/gdsfactory/autosweep) [docs](https://gdsfactory.github.io/autosweep/)
  - [measurement sequencer](https://github.com/SweepMe/pysweepme)
  - [drivers](https://github.com/SweepMe/instrument-drivers)
  - https://github.com/AlexShkarin/pyLabLib
  - [lightlab](https://github.com/lightwave-lab/lightlab) [docs](https://lightlab.readthedocs.io/en/latest/index.html)
  - [instrumental](https://github.com/mabuchilab/Instrumental)
  - [pyrolab](https://github.com/BYUCamachoLab/pyrolab)
  - LabEXT [docs](https://labext.readthedocs.io/en/latest/) and [code](https://github.com/LabExT/LabExT)
  - [SiePIC lab](https://github.com/SiEPIC/SiEPIClab)
  - [hardware testing framework](https://github.com/google/openhtf) - Google
  - [pic-wafer](https://github.com/DerekK88/PIC_WaferProbeSystem) 
  - [laval python lab](https://github.com/Simon-Belanger/ULPythonLab) 
  - [labrad](https://github.com/labrad/pylabrad)
  - [autogator](https://github.com/BYUCamachoLab/autogator) - camera-assisted motion control and experiment configuration of photonic integrated circuit interrogation platforms.

## data analysis

- pandas
- dask
- [wafermap](https://github.com/xlhaw/wfmap)
- [wafer data](https://github.com/guanghaofan/wafermap)
- Webapp
    - [voila](https://github.com/voila-dashboards/voila)
    - [streamlit](https://github.com/streamlit/streamlit)
    - [plotly dash](https://dash.plotly.com/)


## Visualization

- [Klayout](https://www.klayout.de/) for GDS files
- [Meshlab](https://github.com/cnr-isti-vclab/meshlab) for STL
- [ParaView](https://www.paraview.org/) for data visualization


## electronics

- schematic capture:
  - [skidl: netlist formatting, writing, and reading](https://github.com/devbisme/skidl)
  - elkjs [code](https://github.com/kieler/elkjs) [demo](https://rtsys.informatik.uni-kiel.de/elklive/elkgraph.html) - Javascript schematic editor.
- layout

  - [kicad PCB layout python](https://github.com/atait/kicad-python)
  - [VLSI placement](https://github.com/limbo018/DREAMPlace)

- circuit simulation

  - [Spice book](https://github.com/PyLCARS/Python-and-SPICE-Book)

- open source pdks

  - [skywater-pdk](https://github.com/google/skywater-pdk)

- transmission line [wcalc](https://github.com/dmcmahill/wcalc)

## other links

- [princeton notebooks](https://github.com/simbilod/ELE559-simulations)
- https://hackmd.io/@joamatab/rJngxJudr#/
- https://git.shivering-isles.com/shivering-isles/infrastructure
- https://github.com/awesome-selfhosted/awesome-selfhosted
- [epda](https://openepda.org)
- [Awesome quantum](https://github.com/qosf/awesome-quantum-software)
- [Awesome electronics](https://github.com/kitspace/awesome-electronics)
- [Awesome scientific computing](https://github.com/nschloe/awesome-scientific-computing)
- [Awesome lists](https://github.com/sindresorhus/awesome)
