---
layout: page
title: About
permalink: /about/
mermaid: true
---

HamSCI Ray Tracing is a working group within HamSCI for amateur radio operators, citizen
scientists, software developers, and professional researchers interested in HF propagation and
ionospheric science. The group promotes the development and use of open-source HF ray-tracing
tools, the validation of ionospheric models using HamSCI observations, and collaborative studies
of space weather and unusual HF propagation. It also provides a forum for tutorials, technical
discussions, software feedback, and community research projects.

The group's flagship effort is a fully open-source 3D HF ray-tracing toolkit, implemented
natively in Python from the
[Jones & Stephenson (1975)](https://data.ngdc.noaa.gov/instruments/remote-sensing/active/profilers-sounders/ionosonde/documentation/Jones_3D_Ray_Tracing.pdf)
ray-tracing formulation. This toolkit is
independent of the team's earlier [PyLap](https://github.com/hamsci/pylap) toolkit — an
open-source Python wrapper for the proprietary PHaRLAP ray-tracing engine — which remains
available as prior, related work. The new toolkit integrates ionospheric model output (e.g., IRI,
SAMI3, and coupled SAMI3/WACCM-X) and HamSCI observational data (RBN, PSKReporter, WSPRNet, and
PSWS/GRAPE Doppler receivers) to validate ionospheric models and to study anomalous HF
propagation, including Equatorial Plasma Bubbles (EPBs) and understudied off-great-circle
(side-scatter) paths.

This work is supported by NASA ROSES 2024 B.21 Heliophysics Citizen Science Investigations
(H-CSI), award 80NSSC26K0051, *"Ionospheric Model Validation and Development of an Open-Source HF
Ray-Tracing Toolkit Leveraging HamSCI Citizen Science Data"* (PI: Kornyanat Hozumi, University of
Scranton).

For updates and to join bi-weekly meetings, join the Google Group
[here](https://groups.google.com/g/hamsci-ray-tracing?pli=1). Meeting announcements are sent out
on the mailing list.
