---
title: Materials & Methods for Henry Nording
author: David Haberthür
date: 16.04.2019
---

# MicroCT

The samples were embedded in paraffin.
For tomographic imaging, we shaped the samples down minimally with a scalpel, wrapped the samples in X-ray transparent Melamine resin foam (Basotect, SWILO GmbH, Sta. Maria, Switzerland), and mounted them in a standard sample holder inside a Bruker SkyScan1172 high resolution microtomography machine (Bruker microCT, Kontich,
Belgium).

The X-ray source was set to a voltage of 70 kV and a current of 142 μA, with a 0.5 mm Al filter in the beam path.
For the relatively low-resolution scans we show here, we recorded a set of 315 projections of 820 x 1224 pixels at every 0.6° over a 180° sample rotation. Every projection was exposed for 1410 ms, three projections were averaged to one to reduce image acquisition noise. To cover the whole leg, we performed an oversize scan with three subscans, stacked along the long axis of the leg. This resulted
in approximately 35 minutes of imaging time per per sample and an isometric voxel size of 21.6 μm in the final data sets.
The
projection images were then subsequently reconstructed into a 3D stack of 8 bit gray value PNG images with NRecon (Bruker,
Version: 1.7.4.2).

After reconstruction we visualized the legs with MeVisLab (Version 3.1 (2018-06-26 Release), MeVis Medical Solutions AG, Bremen, Germany). We extracted the bone with a gray value threshold based region growing algorithm with manually placed seed points inside the bone. The vessels were extracted with a `Vesselness` filter which is calculated as a function of the Hessian matrix. A threshold based segmentation of this Vesselness measure delivered us the vessels for a visualization with the MeVis Path Tracer which is a completely refactored fork of the `ExposureRender` framework by Thomas Kroes [1].

[1]: [**Exposure Render: An Interactive Photo-Realistic Volume Rendering Framework**   ](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0038586)
Kroes T,
Post FH,
Botha CP
(2012)
Exposure Render: An Interactive Photo-Realistic Volume Rendering Framework.
PLOS ONE  7(7): e38586.
<https://doi.org/10.1371/journal.pone.0038586>