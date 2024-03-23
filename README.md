# Overview
- [Sketch-Based Modeling Papers](#sketch-based-modeling-papers)

# Sketch-based Modeling

## A Gradient-Based Implicit Blend (2012)

They introduce a new family of binary composition operators to address four major challenges in constructive implicit modeling:
- **Suppressing bulges during shape merging**
- **Preventing unwanted blending at a distance**
- **Ensuring the resulting shape maintains the topology of the union**
- **Allowing for the addition of sharp details without distortion**

**Contributions:**

- **Unified Solution with Generic Operators:**
Introduction of a versatile family of composition operators addressing the identified challenges comprehensively.

- **Parametrized Blending Control:**
Utilization of gradient angles between field functions to parametrize blending, enabling interpolation between union and blend within the same composition.

- **Localized Blends near Intersections:**
Implementation of blending techniques that localize blends near intersections without additional implicit primitives, enhancing efficiency and scalability.

- **C∞ Continuous Operators:**
Adoption of C∞ continuous operators, ensuring smooth blending while accommodating successive compositions.

- **Preservation of Sharp Details:**
Preservation of sharp details and precise control over blend localization, facilitating predictable composition and maintaining the topology of the union.

- **Dynamic Animation Capabilities:**
Tunability of operators to facilitate progressive separation of soft materials and prevent disjoint parts from blending at a distance, enhancing realism in animated simulations of soft object interactions.

**Paper Link:**

Gradient-Based implicit Blend (ACM Transactions on Graphics, 2012) [link](https://inria.hal.science/hal-00753246/document)

## Implicit Blending Revisited (2010)

The goal is to develop an automatic method for defining blends between functionally-based implicit surfaces that ensures blending occurs only at surface intersections, preventing unwanted blending at a distance. This approach should offer intuitive control over the extent of blending, independent of the supporting field functions.

![Implicit Blending](/img/Dragon.png)

**Contributions:**

- **Efficient Intersection Curve Computation:**
Introduction of a precise method to compute intersection curves between implicit objects and define blending volumes around them.

- **Clean Union Operator:**
Development of a clean union operator outside blending volumes to prevent unwanted blending effects and ensure C1 continuous field generation.

- **Detail-Preserving Smooth Blend:**
Implementation of a smooth blending mechanism that preserves small shape details by adjusting blending distance based on local feature sizes.

- **Region-Painting Metaphor for Shape Creation:**
Introduction of a region-painting metaphor simplifying the creation of shape components with arbitrary topological genus, enhancing ease of use and flexibility in shape design.

- **Automatic Depth Inference for Shape Components:**
Development of improved, automatic methods for inferring the depth of shape components from existing elements, enhancing the accuracy and efficiency of shape creation.

- **Local Blending Mechanism with Automatic Parameter Adjustment:**
Implementation of a new local blending mechanism that blends components based on user-painted overlap, with automatic parameter adjustment to preserve small details and prevent blurring into larger shapes.

- **Adaptive Meshing Algorithm for Surface Resolution:**
Integration of an adaptive meshing algorithm that adjusts mesh resolution based on feature size and dynamically re-meshes surfaces after blending operations, ensuring optimal surface quality throughout the modeling process.

- **Smooth Blend at Intersection Curves:**
Introduction of a method to ensure a seamless transition with the outer region, preventing blurring of small shapes when blended into larger, smooth ones at intersection curves.

- **Automatic Blending Volume Definition:**
Development of a method to automatically define blending volumes around intersection curves using finite support skeleton-generated field functions, enhancing intuitive modeling and animation applications.

**Paper Link:**

Implicit Blending Revisited (Computer Graphics Forum, 2010) [link](https://www.irit.fr/recherches/VORTEX/publications/rendu-geometrie/EG2010_Bernhardt_et_al.pdf)


## Matisse: Painting 2D regions for Modeling Free-Form Shapes (2008)

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

## Extending the CSG Tree: Warping, Blending and Boolean Operations in an Implicit Surface Modeling System (1999)

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



