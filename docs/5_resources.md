---
layout: page
title: Resources
permalink: /resources/
---

## Introduction
{:.no_toc}

Resources for newcomers to the group and to HF ray-tracing / ionospheric model validation.

## Table of Contents 
{:.no_toc}
* TOC
{:toc}

## Software
- The group's 3D HF ray-tracing engine is implemented natively in Python, based on the Jones &
  Stephenson ray-tracing formulation, independent of PHaRLAP's proprietary core. It is under
  active development; see [`src/README.md`](https://github.com/HamSCI/hamsci-raytracing/blob/main/src/README.md)
  for its current status.
- [PyLap](https://github.com/hamsci/pylap) — the team's earlier open-source 2D Python wrapper
  for PHaRLAP's ray-tracing engine. Separate from the 3D engine above; kept here as related prior
  work.
- [HamSCI GitHub](https://github.com/hamsci/) — where this project's ray-tracing, model
  validation, and analysis code will be posted as it matures.
- [HF-START](https://hfstart.nict.go.jp/) — a related near real-time public HF 3D ray-tracing
  service developed by the PI.

## HamSCI Data Networks
- [Reverse Beacon Network (RBN)](http://www.reversebeacon.net/)
- [PSKReporter](https://pskreporter.info/)
- [WSPRNet](https://www.wsprnet.org/)
- [Personal Space Weather Station (PSWS) / GRAPE](https://hamsci.org/psws-overview) — HF Doppler
  shift receivers
- [Madrigal Database](http://madrigal.haystack.mit.edu/) — public archive that includes
  HamSCI spot data
- [ARRL Maidenhead Grid Squares](https://www.arrl.org/grid-squares)

## Archives
- [HamSCI Zenodo Community](https://zenodo.org/communities/hamsci?page=1&size=20) — ionospheric
  model outputs and ray-tracing results for this project will be archived here
- [HamSCI Website](https://hamsci.org/)
- [HamSCI Working Groups](https://hamsci.org/working-groups)

## Further Reading
- Jones, R. M., & Stephenson, J. J. (1975). *A versatile three-dimensional ray tracing computer
  program for radio waves in the ionosphere.* OT Report 75-76.
  [PDF](https://data.ngdc.noaa.gov/instruments/remote-sensing/active/profilers-sounders/ionosonde/documentation/Jones_3D_Ray_Tracing.pdf) —
  the foundational ray-tracing formulation the group's 3D engine implements natively in Python.
- Frissell, N. A., et al. (2023). *Heliophysics and amateur radio: citizen science
  collaborations for atmospheric, ionospheric, and space physics research and operations.*
  Frontiers in Astronomy and Space Science. [doi:10.3389/fspas.2023.1184171](https://doi.org/10.3389/fspas.2023.1184171)
- Diehl, D., et al. (2023). *PyLap: An open source python interface to the PHaRLAP ionospheric
  ray-tracing toolkit.* HamSCI Workshop 2023. [Link](https://hamsci.org/publications/pylap-open-source-python-interface-pharlap-ionospheric-raytracing-toolkit)
- Griffiths, G., et al. (2023). *HF two-hop sidescatter: identification, modeling and
  observations of an underappreciated propagation mode.* AGU Fall Meeting 2023.
  [Link](https://agu.confex.com/agu/fm23/meetingapp.cgi/Paper/1301410)

See the [Results and Publications]({{ '/results/' | relative_url }}) page for a fuller, citable bibliography.
