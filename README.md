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
- [electronics](#electronics)
- [other links](#other-links)

<!-- tocstop -->

## layout

- [gdspy based tools](https://github.com/heitzmann/gdspy)
  - gdsfactory [docs](https://gdsfactory.readthedocs.io/en/latest/) [code](https://github.com/gdsfactory/gdsfactory) - includes plugins to other tools.
  - [phidl](https://github.com/amccaugh/phidl) - made for superconducting detectors
    - soen-pdk [docs](https://pages.nist.gov/SOEN-PDK/) and [code](https://github.com/usnistgov/SOEN-PDK)
  - [picwriter](https://github.com/DerekK88/PICwriter)
- [gdstk](https://github.com/heitzmann/gdstk) - from gdspy author, made it faster
- [klayout](https://github.com/KLayout/klayout) - layout viewer with python API
  - [xsection, klayout-ipc, klayout-gadgets, lytest, lymask](https://github.com/atait?tab=repositories)
  - [zero-pdk](https://github.com/lightwave-lab/zeropdk) - klayout pure python pdk.
  - [KQcircuits](https://github.com/iqm-finland/KQCircuits) - Quantum circuits pdk.
  - [siepic-tools](https://github.com/lukasc-ubc/SiEPIC-Tools) - code driven PCells and GUI driven layouts.
  - [siepic-ebeam-pdk](https://github.com/lukasc-ubc/SiEPIC_EBeam_PDK)
  - [gds3xtrude](https://codeberg.org/tok)
  - [spicex: netlist extraction](https://github.com/fsitok/spicex)
  - [simplify polygons](https://github.com/fsitok/klayout-simplify)
  - [klayout python](https://github.com/shamil777/KLayout-python)
  - [klayout cross-section in python](https://github.com/dimapu/klayout_pyxs) - Port from ruby to python to xsection macro
- shapely based tools
  - [gdshelpers](https://github.com/HelgeGehring/gdshelpers) - includes superconducting detectors.
  - [dphox](https://github.com/solgaardlab/dphox) - includes 3D MEMs structures
- [masque](https://mpxd.net/code/jan/masque)
- [klamath](https://mpxd.net/code/jan/klamath)
- [nazca](https://nazca-design.org/download/)
- Technology Specific:

  - [Ayar cell generator](https://github.com/AyarLabs/ACG)
  - [BerkeleyPhotonicsGenerator](https://github.com/BerkeleyPhotonicsGenerator/BPG)
  - [qiskit-metal](https://github.com/Qiskit/qiskit-metal) - IBM superconducting based qubits.

- layout viewers
  - [klayout](https://www.klayout.de/) - Best open source layout viewer.
  - [GDS3D](https://github.com/trilomix/GDS3D/)
  - [GDS2WebGL](https://github.com/s-holst/GDS2WebGL)

## simulation

- mode solver:

  - Finite Difference
    - [modes](https://modes.readthedocs.io/en/latest/)
    - [EMpy](https://github.com/lbolla/EMpy)
    - [philsol](https://github.com/philmain28/philsol) - Allows bends.
    - [pymode](https://github.com/smartalecH/pyMode) - Allows bends.
      - [wgms3d](http://www.soundtracker.org/raw/wgms3d/)
    - [pyMWM](https://github.com/mnishida/PyMWM)
    - [mpb](https://mpb.readthedocs.io/en/latest/Scheme_Tutorial/) - Bloch mode solver.

- component design:

  - FDTD - Finite differences time domain.
    - [meep FDTD](https://github.com/NanoComp/meep)
      - [meep ipkiss integration](https://github.com/luceda/ipkiss_meep_integration)
      - [meep docker image](https://hub.docker.com/r/mochen4/meepdocker) - [code](https://github.com/mochen4/meepdocker)
      - [grating coupler example](https://github.com/simbilod/grating_coupler_meep)
    - [emopt FDTD](https://github.com/anstmichaels/emopt)
    - [Python 3D FDTD simulator](https://github.com/flaport/fdtd) - Written in PyTorch.
    - tidy3d client [docs](https://docs.simulation.cloud/projects/tidy3d/en/latest/) and [code](https://github.com/flexcompute/tidy3d) - Server is propietary.
    - [GSvit](http://gsvit.net/) - GPU support
  - FDFD - Finite differences frequency domain.
    - [spins FDFD on GPU](https://github.com/stanfordnqp/spins-b)
    - [ceviche (2D only) FDTD and FDFD](https://github.com/twhughes/ceviche)
    - [jaxwell](https://github.com/stanfordnqp/jaxwell)
  - EME - Eigen mode expansion.
    - [emepy](https://github.com/BYUCamachoLab/emepy)
    - [CAMFR](https://github.com/demisjohn/CAMFR)
  - RCWA:
    - [S4](https://github.com/victorliu/S4)
    - [grcwa](https://github.com/weiliangjinca/grcwa) - automatic differentiation included with autograd
  - [SiPANN (neural networks for photonics component design)](https://github.com/contagon/SiPANN)
  - [inverse design](http://metanet.stanford.edu/code/)
    - [glonet: global optimization based on generative neural networks](https://github.com/jonfanlab/GLOnet)
    - [wavetorch](https://github.com/fancompute/wavetorch)
    - [lumopt](https://github.com/chriskeraly/lumopt)
    - [angler](https://github.com/fancompute/angler/) - Frequency-domain photonic simulation and inverse design optimization for linear and nonlinear devices.
    - SPLayout [code](https://github.com/Hideousmon/SPLayout) [docs](https://splayout.readthedocs.io/en/latest/index.html)
    - ceviche-challenges [code](https://github.com/google/ceviche-challenges) - Photonic inverse designs based on the FDFD simulator Ceviche
    - [NIDN](https://github.com/esa/NIDN) - Inverse design of metamaterials, photonic crystals, ... using PyTorch
  - [TCAD](https://tcadcentral.com/Software.html#open-source-tcad-software)
    - [devsim](https://devsim.org/) - Semiconductor Device Simulator
    - [BOSIM](https://eexu.home.ece.ust.hk/BOSIM.html)
    - [Suprem4](https://github.com/cogenda/Suprem4) - Process simulator (no python)
    - [pisces](https://github.com/ComputerWhisperer/pisces) - Poison and continuity equation solver (no python)
    - [TCAD docker containers](https://github.com/thesourcerer8/OpenSourceTCAD)
    - [Charon](https://charon.sandia.gov/) - Paralell TCAD simulator.
  - ray tracing:
    - [ray tracing](https://github.com/DCC-Lab/RayTracing)
    - [rayopt](https://github.com/quartiq/rayopt)
  - adaptive optics
    - [AOtools](https://github.com/AOtools)
  - [simphox](https://github.com/fancompute/simphox)

- circuit simulation:

  - SAX [code](https://github.com/flaport/sax) and [docs](https://flaport.github.io/sax/) - Differentiable circuit solver.
  - [simphony (linear circuit solver)](https://github.com/BYUCamachoLab/simphony)
  - [photontorch docs](https://docs.photontorch.com/) - [code](https://github.com/flaport/photontorch) - Includes time domain.
  - [opics](https://github.com/siepic/opics)
  - [SignalIntegrity (linear circuit simulation)](https://github.com/TeledyneLeCroy/SignalIntegrity)
  - [scikit-rf RF simulator](https://scikit-rf.readthedocs.io/en/latest/)
  - pyFDA filter design [code](https://github.com/chipmuenk/pyfda) and [docs](https://pyfda.readthedocs.io/en/latest/manual/input_specs.html)
  - [Xyce](https://xyce.sandia.gov/) - open source, SPICE-compatible, high-performance analog circuit simulator.

- material database

  - [rii pandas](https://github.com/mnishida/RII_Pandas)

- lithography simulation
  - [optolithium](https://github.com/xthebat/optolithium)
  - [notebooks](https://github.com/pierremifasol/Lithography-Simulation)
  - [dimmilitho](https://github.com/vincentlv/DimmiLitho)

## lab automation

- backend:

  - [PyVISA](https://pyvisa.readthedocs.io/en/latest/) - Allows you to control the lab instruments with python. As the backend you can use NI or [PyVISA-py](https://pyvisa-py.readthedocs.io/en/latest/).
  - [PySerial](https://github.com/pyserial/pyserial) - Issue simple serial commands (RS-232, RS485) to instruments (and read data).

- lab automation repos:
  - lightlab [repo](https://github.com/lightwave-lab/lightlab) [docs](https://lightlab.readthedocs.io/en/latest/index.html)
  - [instrumental](https://github.com/mabuchilab/Instrumental)
  - [pymeasure](https://github.com/ralph-group/pymeasure)
  - [pyrolab](https://github.com/BYUCamachoLab/pyrolab)
  - LabEXT [docs](https://labext.readthedocs.io/en/latest/) and [code](https://github.com/LabExT/LabExT)
  - [hardware testing framework](https://github.com/google/openhtf) - Google
  - [pic-wafer](https://github.com/DerekK88/PIC_WaferProbeSystem) - MIT
  - [laval python lab](https://github.com/Simon-Belanger/ULPythonLab) 
  - [ubc automated pic-tester](https://github.com/lukasc-ubc/pyOptomip)
  - [labrad](https://github.com/labrad/pylabrad)
  - [autogator](https://github.com/BYUCamachoLab/autogator) - camera-assisted motion control and experiment configuration of photonic integrated circuit interrogation platforms.

## data analysis

- pandas
- dask

## electronics

- schematic capture:
  - [skidl: netlist formatting, writing, and reading](https://github.com/devbisme/skidl)
  - elkjs [code](https://github.com/kieler/elkjs) [demo](https://rtsys.informatik.uni-kiel.de/elklive/elkgraph.html) - Javascript schematic editor.
- layout

  - [kicad PCB layout python](https://github.com/atait/kicad-python)
  - [VLSI placement](https://github.com/limbo018/DREAMPlace)

- circuit simulation

  - [lcapy](https://github.com/mph-/lcapy) - Linear circuit analysis.
  - [pyspice](https://github.com/FabriceSalvaire/PySpice)
  - [Spice book](https://github.com/PyLCARS/Python-and-SPICE-Book)

- open source pdks

  - [skywater-pdk](https://github.com/google/skywater-pdk)

## other links

- [princeton notebooks](https://github.com/simbilod/ELE559-simulations)
- https://hackmd.io/@joamatab/rJngxJudr#/
- https://git.shivering-isles.com/shivering-isles/infrastructure
- https://github.com/awesome-selfhosted/awesome-selfhosted
- [epda](https://openepda.org)
- [Awesome quantum](https://github.com/qosf/awesome-quantum-software)
- [Awesome electronics](https://github.com/kitspace/awesome-electronics)
- [Awesome lists](https://github.com/sindresorhus/awesome)
