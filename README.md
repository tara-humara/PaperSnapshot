# Extending the CSG Tree: Warping, Blending and Boolean Operations in an Implicit Surface Modeling System (1999)

This work aims to organize blending, warping, and Boolean operations to facilitate both global and local operations intuitively. The goal is achieved by structuring implicit surface models using a tree-based approach called the BlobTree, allowing for flexible modeling of complex shapes.

![Extending the CSG Tree](/img/Stamingo.png)

**Contributions:**

- **Complex Model Construction:** 
  The BlobTree enables the creation of complex models using a small set of primitives with arbitrary combinations of blending, warping, and Boolean operations.
  
- **Prototyping by Polygonization:** 
  Facilitates prototyping through polygonization, enabling translation into polygonal representations for visualization and analysis.
  
- **Efficient Ray Tracing:** 
  Implements efficient direct ray tracing for high-quality visualizations.
  
- **Continuous Joins:** 
  Primitives smoothly transition between blend and union operations, offering flexibility in model construction.
  
- **Global and Local Warping:** 
  Allows for control of warping either globally or locally, with support for arbitrary functions such as Barr deformations and affine transformations implemented as space warps.

**Paper Link:**

Extending the CSG Tree (Computer Graphics Forum, 1999) [link](https://perso.liris.cnrs.fr/eric.galin/Articles/1999-blobtree-model.pdf)

# Matisse: Painting 2D regions for Modeling Free-Form Shapes (2008)

The goal is to develop an interactive modeling system that enables untrained users to effortlessly design free-form 3D shapes. This addresses the inadequacy of standard modeling systems, which typically demand understanding of complex geometrical representations, indirect control methods, and extensive training to master.

![Matisse](/img/Matisse.png)

**Contributions:**

- **Interactive Modeling System for Novice Users:**
Development of an intuitive modeling interface tailored for individuals without prior training in 3D modeling.

- **Creation of Smooth, Free-form Shapes:**
Introduction of a method for progressively blending surfaces from various viewing angles and zoom factors to generate smooth, free-form shapes with arbitrary topological genus.

- **Region-Painting Metaphor for Shape Creation:**
Introduction of a region-painting metaphor simplifying the creation of shape components with arbitrary topological genus, enhancing ease of use and flexibility in shape design.

- **Efficient Reconstruction of Implicit Surfaces:**
Implementation of a mechanism for reconstructing regions with implicit surfaces without the need for optimization steps, streamlining the modeling process for users.

- **Automatic Depth Inference for Shape Components:**
Development of improved, automatic methods for inferring the depth of shape components from existing elements, enhancing the accuracy and efficiency of shape creation.

- **Local Blending Mechanism with Automatic Parameter Adjustment:**
Implementation of a new local blending mechanism that blends components based on user-painted overlap, with automatic parameter adjustment to preserve small details and prevent blurring into larger shapes.

- **Adaptive Meshing Algorithm for Surface Resolution:**
Integration of an adaptive meshing algorithm that adjusts mesh resolution based on feature size and dynamically re-meshes surfaces after blending operations, ensuring optimal surface quality throughout the modeling process.

**Paper Link:**

Matisse (Eurographics Workshop on Sketch-Based Interfaces and Modeling, 2008) [link](https://inria.hal.science/inria-00336688v1/document)