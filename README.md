# Photonic open source projects

## Layout: define the geometrical shapes that guide the light.

- [gdspy based tools](https://github.com/heitzmann/gdspy)
  - [gdsfactory](https://github.com/gdsfactory/gdsfactory)
  - [phidl](https://github.com/amccaugh/phidl)
  - [picwriter](https://github.com/DerekK88/PICwriter)
  - [gdshelpers](https://github.com/HelgeGehring/gdshelpers)
  - soen-pdk [docs](https://pages.nist.gov/SOEN-PDK/) and [code](https://github.com/usnistgov/SOEN-PDK)
- [klayout](https://github.com/KLayout/klayout)
  - [xsection, klayout-ipc, klayout-gadgets, lytest, lymask](https://github.com/atait?tab=repositories)
  - [zero-pdk](https://github.com/lightwave-lab/zeropdk)
  - [siepic-tools](https://github.com/lukasc-ubc/SiEPIC-Tools)
  - [siepic-ebeam-pdk](https://github.com/lukasc-ubc/SiEPIC_EBeam_PDK)
  - [gds3xtrude](https://codeberg.org/tok)
  - [spicex: netlist extraction](https://github.com/fsitok/spicex)
  - [simplify polygons](https://github.com/fsitok/klayout-simplify)
- [masque](https://mpxd.net/code/jan/masque)
- [epda](https://openepda.org/openepda_data_format.html)
- [nazca (freeware, not open source)](https://nazca-design.org/download/)
- Technology Specific:
    - [Ayar cell generator](https://github.com/AyarLabs/ACG)
    - [BerkeleyPhotonicsGenerator](https://github.com/BerkeleyPhotonicsGenerator/BPG)
    - [qiskit-metal](https://github.com/Qiskit/qiskit-metal)

## Simulation: simulate how photons propagate, and optimize the geometrical shapes

- mode solver:

  - Finite Difference
    - [modes](https://modes.readthedocs.io/en/latest/)
    - [EMpy](https://github.com/lbolla/EMpy)
    - [philsol](https://github.com/philmain28/philsol)
    - [pymode](https://github.com/smartalecH/pyMode) allows bends
      - [wgms3d](http://www.soundtracker.org/raw/wgms3d/)
  - Band structure
    - [mpb](https://mpb.readthedocs.io/en/latest/Scheme_Tutorial/)

- component design:

  - FDTD
    - [meep FDTD](https://github.com/NanoComp/meep)
      - [meep ipkiss integration](https://github.com/luceda/ipkiss_meep_integration)
    - [emopt FDTD](https://github.com/anstmichaels/emopt)
    - [Python 3D FDTD simulator](https://github.com/flaport/fdtd)
  - FDFD
    - [spins FDFD on GPU](https://github.com/stanfordnqp/spins-b)
    - [ceviche (2D only) FDTD and FDFD](https://github.com/twhughes/ceviche)
    - [jaxwell](https://github.com/stanfordnqp/jaxwell)
  - EME
    - [emepy](https://github.com/BYUCamachoLab/emepy)
    - [CAMFR](https://github.com/demisjohn/CAMFR)
  - RCWA:
    - [S4](https://github.com/victorliu/S4)
  - [SiPANN (neural networks for photonics component design)](https://github.com/contagon/SiPANN)
  - [inverse design](http://metanet.stanford.edu/code/)
    - [glonet: global optimization based on generative neural networks](https://github.com/jonfanlab/GLOnet)
    - [wavetorch](https://github.com/fancompute/wavetorch)
    - [lumopt](https://github.com/chriskeraly/lumopt)
    - [angler](https://github.com/fancompute/angler/) Frequency-domain photonic simulation and inverse design optimization for linear and nonlinear devices
  - ray tracing:
    - [ray tracing](https://github.com/DCC-Lab/RayTracing)
    - [rayopt](https://github.com/quartiq/rayopt)

- circuit simulator:

  - [simphony (linear circuit solver)](https://github.com/BYUCamachoLab/simphony)
  - [sax](https://github.com/flaport/sax)
  - [photontorch](https://docs.photontorch.com/) [code](https://github.com/flaport/photontorch)
  - [opics](https://github.com/siepic/opics)

- system tools:

  - [skidl: netlist formatting, writing, and reading](https://xesscorp.github.io/skidl/docs/_site/)
  - [scikit-rf RF simulator](https://scikit-rf.readthedocs.io/en/latest/)

## Control instruments in the lab

- [testing framework template](https://github.com/google/openhtf)
- [instrumental](https://github.com/mabuchilab/Instrumental)
- [lightlab](https://github.com/lightwave-lab/lightlab)
- [pymeasure](https://github.com/ralph-group/pymeasure)
- [pic-wafer](https://github.com/DerekK88/PIC_WaferProbeSystem)
- [laval python lab](https://github.com/Simon-Belanger/ULPythonLab)
- [ubc automated pic-tester](https://github.com/lukasc-ubc/pyOptomip)
- [labrad](https://github.com/labrad/pylabrad)

## Data analysis

- [ant](https://github.com/jaspreetj/manufacturing-variability-analysis-tool/tree/master/ANT_data_march_2019)
- [dask](https://docs.dask.org/en/latest/)

# Misc

- [princeton notebooks](https://github.com/simbilod/ELE559-simulations)
- javscript schematic editor [code](https://github.com/kieler/elkjs) [demo](https://rtsys.informatik.uni-kiel.de/elklive/elkgraph.html)
- [VLSI placement](https://github.com/limbo018/DREAMPlace)

# System admin

- https://git.shivering-isles.com/shivering-isles/infrastructure
- https://github.com/awesome-selfhosted/awesome-selfhosted
- https://git.cloudron.io/cloudron

# Documentation

- https://hackmd.io/: markdown collaborative notes
- https://docs.gitbook.com/content-editing/markdown
- https://github.com/joamatab/Gitbook-Template-Math
- https://hackmd.io/@joamatab/rJngxJudr#/
