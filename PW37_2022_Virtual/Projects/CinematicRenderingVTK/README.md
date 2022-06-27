Back to [Projects List](../../README.md#ProjectsList)

# Cinematic rendering in Slicer leveraging VTK Physically Based Rendering (PBR)

## Key Investigators

- Shreeraj Jadhav, Kitware, USA
- Jiayi Xu, Kitware, USA
- Jean-Christophe Fillion-Robin Kitware, USA

# Project Description

<!-- Add a short paragraph describing the project. -->
- The goal of this project is to identify and evaluate Kitware's previous efforts on cinematic rendering and how these can be leveraged in Slicer.
- Slicer internally uses VTK as its rendering engine to display the 2D and 3D viewports in its interface. Since release 9.0, VTK has more enhanced rendering capabilities such as the Physically Based Rendering (PBR) lighting model and the integration of ray tracing backends such as the Nvidia OptiX and intel's OSPRay engine. These capabilities are already being leveraged in Paraview as discussed in the following blog posts [here](https://www.kitware.com/vtk-pbr/) and [here](https://www.kitware.com/physically-based-rendering-improvements-in-paraview/).

- Primary focus will be on VTK's PBR capabilities and ray tracing backends (OptiX, OSPRay). Since Slicer already uses VTK rendering pipeline, and it will be significantly easier to incorporate/leverage these capabilities from within Slicer.


## Objective

<!-- Describe here WHAT you would like to achieve (what you will have as end result). -->



## Approach and Plan

<!-- Describe here HOW you would like to achieve the objectives stated above. -->
1. Review accessible offerings on cinematic rendering (VTK PBR, VTK backends: OSPRay and OptiX, omniverse, etc) that can be utilized inside Slicer.
2. Develop prototypes showing how these can be enabled and used in Slicer.
   - Start with surface rendering (PBR, ambient occlusion, global ilumination)
   - Investigate what capabilities can be enabled for volume rendering (perhaps OSPRay).
   - Tradeoffs: Performance vs Image Quality without degrading user experience.
   - Changes to user interface, parameters tuning, simplification.
3. Review existing Slicer modules (such as [Light Module](https://discourse.slicer.org/t/new-module-to-customize-lighting-in-3d-view/8804)) that enhance Slicer's rendering capabilities and evaluate how these can be included in the current effort.
4. Evaluate how integrating these in Slicer will affect other modules such as LookingGlass, OpenXR, etc.

## Progress and Next Steps

<!-- Update this section as you make progress, describing of what you have ACTUALLY DONE. If there are specific steps that you could not complete then you can describe them here, too. -->

# Illustrations

<!-- Add pictures and links to videos that demonstrate what has been accomplished.
![Description of picture](Example2.jpg)
![Some more images](Example2.jpg)
-->

# Background and References

<!-- If you developed any software, include link to the source code repository. If possible, also add links to sample data, and to any relevant publications. -->
Slicer Discourse References:
1. [https://discourse.slicer.org/t/how-to-perform-3d-cinematic-rendering/7313](https://discourse.slicer.org/t/how-to-perform-3d-cinematic-rendering/7313)
1. [https://discourse.slicer.org/t/is-there-interest-in-higher-quality-rendering-for-slicer/6862/5](https://discourse.slicer.org/t/is-there-interest-in-higher-quality-rendering-for-slicer/6862/5)
1. [https://discourse.slicer.org/t/2021-01-19-hangout/15585/2](https://discourse.slicer.org/t/2021-01-19-hangout/15585/2)

VTK References:
1. VTK PBR [https://www.kitware.com/vtk-pbr/](https://www.kitware.com/vtk-pbr/)
1. PBR integration in Paraview [https://www.kitware.com/physically-based-rendering-improvements-in-paraview/](https://www.kitware.com/physically-based-rendering-improvements-in-paraview/) 
1. Related merge request for VTK [https://gitlab.kitware.com/vtk/vtk/-/merge_requests/5584](https://gitlab.kitware.com/vtk/vtk/-/merge_requests/5584)