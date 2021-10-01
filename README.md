# Photonic open source projects

If you are new to Git and Python I reccommend reading this [article](https://lightlab.readthedocs.io/en/latest/_static/gettingStarted/index.html)
Most tools in this list are written or have a python interface, which require some basic knowledge of python. If you are new to python you can find many [books](https://jakevdp.github.io/PythonDataScienceHandbook/index.html), [youTube videos](https://www.youtube.com/c/anthonywritescode) and [courses](https://github.com/joamatab/practical-python) available online.

## Layout: define the geometrical shapes that guide the light.

- [gdspy based tools](https://github.com/heitzmann/gdspy)
  - gdsfactory [docs](https://gdsfactory.readthedocs.io/en/latest/) [code](https://github.com/gdsfactory/gdsfactory)
  - [phidl](https://github.com/amccaugh/phidl)
  - [dphox](https://github.com/solgaardlab/dphox)
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
- [klamath](https://mpxd.net/code/jan/klamath)
- [epda](https://openepda.org)
- [nazca](https://nazca-design.org/download/)
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
    - [pyMWM](https://github.com/mnishida/PyMWM)
  - Band structure
    - [mpb](https://mpb.readthedocs.io/en/latest/Scheme_Tutorial/)

- component design:

  - [simphox](https://github.com/fancompute/simphox)
  - FDTD
    - [meep FDTD](https://github.com/NanoComp/meep)
      - [meep ipkiss integration](https://github.com/luceda/ipkiss_meep_integration)
      - [meep docker image](https://hub.docker.com/r/mochen4/meepdocker) [code](https://github.com/mochen4/meepdocker)
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
  - TCAD
    - [devsim](https://devsim.org/)
    - [BOSIM](https://eexu.home.ece.ust.hk/BOSIM.html)
  - ray tracing:
    - [ray tracing](https://github.com/DCC-Lab/RayTracing)
    - [rayopt](https://github.com/quartiq/rayopt)
  - adaptive optics
    - [AOtools](https://github.com/AOtools)

- circuit simulator:

  - [gdslib](https://gdslib.readthedocs.io/en/latest/)
  - [simphony (linear circuit solver)](https://github.com/BYUCamachoLab/simphony)
  - [sax](https://github.com/flaport/sax)
  - [photontorch](https://docs.photontorch.com/) [code](https://github.com/flaport/photontorch)
  - [opics](https://github.com/siepic/opics)
  - [SignalIntegrity (linear circuit simulation)](https://github.com/TeledyneLeCroy/SignalIntegrity)
  - [scikit-rf RF simulator](https://scikit-rf.readthedocs.io/en/latest/)

- system tools:

  - [skidl: netlist formatting, writing, and reading](https://xesscorp.github.io/skidl/docs/_site/)

- material database
    - [rii pandas](https://github.com/mnishida/RII_Pandas)

## Control instruments in the lab

[PyVISA](https://pyvisa.readthedocs.io/en/latest/) allows you to control the lab instruments with python. As the backend you can use NI or [PyVISA-py](https://pyvisa-py.readthedocs.io/en/latest/)

- lightlab [repo](https://github.com/lightwave-lab/lightlab) [docs](https://lightlab.readthedocs.io/en/latest/index.html)
- [pyrolab](https://github.com/BYUCamachoLab/pyrolab)
- [instrumental](https://github.com/mabuchilab/Instrumental)
- [pymeasure](https://github.com/ralph-group/pymeasure)
- [testing framework template](https://github.com/google/openhtf)
- [pic-wafer](https://github.com/DerekK88/PIC_WaferProbeSystem)
- [laval python lab](https://github.com/Simon-Belanger/ULPythonLab)
- [ubc automated pic-tester](https://github.com/lukasc-ubc/pyOptomip)
- [labrad](https://github.com/labrad/pylabrad)

## Data analysis

- pandas
- dask

## Tools summary

Here is a summary of the tools I use for Silicon Photonics design

| Purpose                               | Tool                                                                                                                                       |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Layout generator                      | [gdsfactory](https://gdsfactory.readthedocs.io/en/latest/)                                                                                 |
| Layout viewer                         | [klayout](https://www.klayout.de/)                                                                                                         |
| Mode solver                           | [Modes](https://modes.readthedocs.io/en/latest/) and [MPB](https://mpb.readthedocs.io/en/latest/Python_Tutorial/#our-first-band-structure) |
| FDTD                                  | [Meep](https://meep.readthedocs.io/en/latest/Installation/)                                                                                |
| Frequency domain circuit simulator    | [gdslib](https://gdslib.readthedocs.io/en/latest/)                                                                                         |
| lab measurements (instrument control) | [lightlab](https://lightlab.readthedocs.io/en/latest/index.html)                                                                           |

## Misc

- [princeton notebooks](https://github.com/simbilod/ELE559-simulations)
- javscript schematic editor [code](https://github.com/kieler/elkjs) [demo](https://rtsys.informatik.uni-kiel.de/elklive/elkgraph.html)
- [VLSI placement](https://github.com/limbo018/DREAMPlace)

## System admin

- https://git.shivering-isles.com/shivering-isles/infrastructure
- https://github.com/awesome-selfhosted/awesome-selfhosted
- https://git.cloudron.io/cloudron

## Documentation

- https://hackmd.io/: markdown collaborative notes
- https://docs.gitbook.com/content-editing/markdown
- https://github.com/joamatab/Gitbook-Template-Math
- https://hackmd.io/@joamatab/rJngxJudr#/
