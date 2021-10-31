# Photonic open source projects

If you are new to Git and Python I reccommend reading this [article](https://lightlab.readthedocs.io/en/latest/_static/gettingStarted/index.html)
Most tools in this list are written or have a python interface, which require some basic knowledge of python. If you are new to python you can find many [books](https://jakevdp.github.io/PythonDataScienceHandbook/index.html), [youTube videos](https://www.youtube.com/c/anthonywritescode) and [courses](https://github.com/joamatab/practical-python) available online.

## Layout: define the geometrical shapes that guide the light.

- [gdspy based tools](https://github.com/heitzmann/gdspy)
  - gdsfactory [docs](https://gdsfactory.readthedocs.io/en/latest/) [code](https://github.com/gdsfactory/gdsfactory)
  - [phidl](https://github.com/amccaugh/phidl)
    - soen-pdk [docs](https://pages.nist.gov/SOEN-PDK/) and [code](https://github.com/usnistgov/SOEN-PDK)
  - [picwriter](https://github.com/DerekK88/PICwriter)
- [gdstk](https://github.com/heitzmann/gdstk)
- [klayout](https://github.com/KLayout/klayout)
  - [xsection, klayout-ipc, klayout-gadgets, lytest, lymask](https://github.com/atait?tab=repositories)
  - [zero-pdk](https://github.com/lightwave-lab/zeropdk)
  - [KQcircuits](https://github.com/iqm-finland/KQCircuits)
  - [siepic-tools](https://github.com/lukasc-ubc/SiEPIC-Tools)
  - [siepic-ebeam-pdk](https://github.com/lukasc-ubc/SiEPIC_EBeam_PDK)
  - [gds3xtrude](https://codeberg.org/tok)
  - [spicex: netlist extraction](https://github.com/fsitok/spicex)
  - [simplify polygons](https://github.com/fsitok/klayout-simplify)
- [shapely based tools]
  - [gdshelpers](https://github.com/HelgeGehring/gdshelpers)
  - [dphox](https://github.com/solgaardlab/dphox)
- [masque](https://mpxd.net/code/jan/masque)
- [klamath](https://mpxd.net/code/jan/klamath)
- [nazca](https://nazca-design.org/download/)
- Technology Specific:

  - [Ayar cell generator](https://github.com/AyarLabs/ACG)
  - [BerkeleyPhotonicsGenerator](https://github.com/BerkeleyPhotonicsGenerator/BPG)
  - [qiskit-metal](https://github.com/Qiskit/qiskit-metal)

- layout viewers
  - [GDS3D](https://github.com/trilomix/GDS3D/)
  - [GDS2WebGL](https://github.com/s-holst/GDS2WebGL)

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

  - FDTD
    - [meep FDTD](https://github.com/NanoComp/meep)
      - [meep ipkiss integration](https://github.com/luceda/ipkiss_meep_integration)
      - [meep docker image](https://hub.docker.com/r/mochen4/meepdocker) [code](https://github.com/mochen4/meepdocker)
      - [grating coupler example](https://github.com/simbilod/grating_coupler_meep)
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
  - [simphox](https://github.com/fancompute/simphox)

- circuit simulation:

  - [gdslib](https://gdslib.readthedocs.io/en/latest/)
  - [simphony (linear circuit solver)](https://github.com/BYUCamachoLab/simphony)
  - [sax](https://github.com/flaport/sax)
  - [photontorch](https://docs.photontorch.com/) [code](https://github.com/flaport/photontorch)
  - [opics](https://github.com/siepic/opics)
  - [SignalIntegrity (linear circuit simulation)](https://github.com/TeledyneLeCroy/SignalIntegrity)
  - [scikit-rf RF simulator](https://scikit-rf.readthedocs.io/en/latest/)

- material database

  - [rii pandas](https://github.com/mnishida/RII_Pandas)

- lithography simulation
  - [optolithium](https://github.com/xthebat/optolithium)
  - [notebooks](https://github.com/pierremifasol/Lithography-Simulation)
  - [dimmilitho](https://github.com/vincentlv/DimmiLitho)

## Control instruments in the lab

backend:

- [PyVISA](https://pyvisa.readthedocs.io/en/latest/) allows you to control the lab instruments with python. As the backend you can use NI or [PyVISA-py](https://pyvisa-py.readthedocs.io/en/latest/)
- [PySerial](https://github.com/pyserial/pyserial) is a great way to issue simple serial commands (RS-232, RS485) to instruments (and read data)

repos:

- lightlab [repo](https://github.com/lightwave-lab/lightlab) [docs](https://lightlab.readthedocs.io/en/latest/index.html)
- [pyrolab](https://github.com/BYUCamachoLab/pyrolab)
- [instrumental](https://github.com/mabuchilab/Instrumental)
- [pymeasure](https://github.com/ralph-group/pymeasure)
- LabEXT [docs](https://labext.readthedocs.io/en/latest/) and [code](https://github.com/LabExT/LabExT)
- [testing framework template](https://github.com/google/openhtf)
- [pic-wafer](https://github.com/DerekK88/PIC_WaferProbeSystem)
- [laval python lab](https://github.com/Simon-Belanger/ULPythonLab)
- [ubc automated pic-tester](https://github.com/lukasc-ubc/pyOptomip)
- [labrad](https://github.com/labrad/pylabrad)

## Data analysis

- pandas
- dask

# Electronics

- schematic capture:
  - [skidl: netlist formatting, writing, and reading](https://xesscorp.github.io/skidl/docs/_site/)
  - javscript schematic editor [code](https://github.com/kieler/elkjs) [demo](https://rtsys.informatik.uni-kiel.de/elklive/elkgraph.html)
- layout
  - [kicad PCB layout python](https://github.com/atait/kicad-python)
  - [VLSI placement](https://github.com/limbo018/DREAMPlace)
- circuit simulation
  - [lcapy](https://github.com/mph-/lcapy) linear circuit analysis
  - [pyspice](https://github.com/FabriceSalvaire/PySpice)
  - [Spice book](https://github.com/PyLCARS/Python-and-SPICE-Book)

## Tools For PIC development

For Silicon Photonics design you need different tools:

| Purpose                               | Tool                                                                                                                                       |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Layout generator                      | [gdsfactory](https://gdsfactory.readthedocs.io/en/latest/)                                                                                 |
| Layout viewer                         | [klayout](https://www.klayout.de/)                                                                                                         |
| Mode solver                           | [Modes](https://modes.readthedocs.io/en/latest/) and [MPB](https://mpb.readthedocs.io/en/latest/Python_Tutorial/#our-first-band-structure) |
| FDTD                                  | [Meep](https://meep.readthedocs.io/en/latest/Installation/)                                                                                |
| Frequency domain circuit simulator    | [gdslib](https://gdslib.readthedocs.io/en/latest/)                                                                                         |
| lab measurements (instrument control) | [lightlab](https://lightlab.readthedocs.io/en/latest/index.html)                                                                           |

## Other links

- https://hackmd.io/: markdown collaborative notes
- https://docs.gitbook.com/content-editing/markdown
- https://github.com/joamatab/Gitbook-Template-Math
- https://hackmd.io/@joamatab/rJngxJudr#/
- [princeton notebooks](https://github.com/simbilod/ELE559-simulations)
- https://git.shivering-isles.com/shivering-isles/infrastructure
- https://github.com/awesome-selfhosted/awesome-selfhosted
- https://git.cloudron.io/cloudron
- [epda](https://openepda.org)
