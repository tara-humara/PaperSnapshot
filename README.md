# Overview
- [Sketch-Based Modeling Papers](#sketch-based-modeling-papers)

# Sketch-based Modeling

## Synchronized-tracing of implicit surfaces (2023)

They propose an implicit rendering pipeline that decorrelates field evaluation complexity from the full blobtree size while avoiding preprocessing the full tree during base modeling operations.

![Synchronized-tracing](/img/Astronaut.png)

**Contributions:**

- **Focus on Data Management and Field Evaluation Efficiency:**
Emphasis on GPU-friendly data management and field evaluation, particularly for approximate signed distance fields (A-SDF).

- **Design of Compact CSG Operators for A-SDF:**
Drawing inspiration from compactly supported density fields, develop smooth constructive solid geometry (CSG) operators for A-SDF, facilitating simple computation of tight volume of interest for primitives.

- **Tile-Based View-Dependent Acceleration Structure:**
Utilize volumes from compact CSG operators to construct a tile-based view-dependent acceleration structure. This structure aids in workgroup synchronization and coherent access to relevant primitives.

- **Sparse Bottom-Up Tree Traversal:**
Propose on-the-fly tree pruning via sparse bottom-up tree traversal, accessing only a subset of blobtree nodes. This approach decorrelates field complexity from the full expression size.

**Paper Link:**

Synchronized-tracing (2023) [link](https://arxiv.org/pdf/2304.09673.pdf)

## N-ary implicit blends with topology control (2015)

The aim is to develop an N-ary blending operator that provides topology control while maintaining segmentation invariance, applicable to any family of skeleton-based implicit surfaces. The aim is to enable a range of blending behaviors for various modeling and animation scenarios, such as organic shape modeling, contact blending, distance blending, and context-dependent blending.

![N-ary implicit blends](/img/HairDragon.png)

**Contributions:**

- **Introduction of N-ary Blending Operator:**
Proposal of a novel blending operator that allows for the combination of multiple skeleton-based implicit primitives, providing topology control and segmentation invariance.

- **Blending Behavior Flexibility:**
Enable a spectrum of blending behaviors, including deformations without merging, merging on contact, merging at a distance, and context-dependent blending effects.

- **Applicability to Various Implicit Surfaces:**
Design of the blending operator to accommodate arbitrary skeleton-based implicit primitives, facilitating its usage across a wide range of shapes generated from different types of skeletons (e.g., points, curves, surfaces).

- **Simplicity of Topology Control:**
Introduction of a single parameter for topology control, offering a straightforward approach to adjust blending effects dynamically based on the desired context.

- **Correction Mechanism for Topological Changes:**
Development of a correction mechanism to mitigate unwanted topological changes resulting from the additive blending operator, ensuring the preservation of shape integrity.

- **Projection-based Adjustment:**
Utilization of projection onto a reference case in variation space to define the correction, allowing adjustments to be made uniformly across different spatial locations and implicit surface types.

- **Preservation of N-ary Nature:**
Retention of the n-ary nature of blending despite the correction mechanism, enabling the handling of complex shapes and skeleton graphs through a single blend operation.

- **Compatibility with Existing Models:**
Alignment with standard sum operators, ensuring compatibility with convolution and SCALIS surfaces, and maintaining the segmentation-invariant property crucial for efficient modeling.

**Paper Link:**

N-ary implicit blends (Computers & Graphics, 2015) [link](https://inria.hal.science/hal-01073088/document)

## SCALe-invariant Integral Surfaces (2013)

They introduce SCAle-invariant Integral Surfaces (SCALIS), a novel implicit modeling approach aimed at enhancing the usability of skeleton-based modeling. SCALIS combines convolution and space warps to address key challenges in constructive implicit modeling, with a focus on bulge suppression, controlled blending, and preservation of sharp details.

![SCALIS](/img/SCALIS.png)

**Contributions:**

- **Unified Model with SCALIS Operators:**
Introduction of a unified family of SCALIS operators that offer scale-invariant blending, controlled radii, and self-similar shape generation.

- **Parametrized Blending Control:**
Development of blending operators that allow explicit control over the radius of generated surfaces and ensure self-similar shapes across different scales.

- **Preservation of Sharp Details:**
Implementation of blending mechanisms that prevent excessive smoothing of small shape components when blended into larger ones, enabling detailed modeling.

- **Topology Preservation:**
Introduction of blending techniques that maintain the topology of the composed object, ensuring seamless integration of shapes without unintended filling of holes.

- **Efficient Radius Control Mechanism:**
Proposal of a method for explicit control of surface radii along skeletons, enabling precise adjustment of shape thickness and radius variations.

- **Optimized Rendering Method:**
Utilization of compact polynomial kernels and local marching cube algorithms for efficient rendering and interactive feedback during modeling.

- **Scale-Invariant Blending Properties:**
Demonstration of SCALIS's ability to seamlessly blend shapes regardless of the scale of the model, offering improved control and predictability in constructive modeling frameworks.

- **Compact Representation with Skeletons:**
Highlighting the potential of storing solid models in skeletal forms, providing a compact representation compared to B-reps and facilitating conceptual shape design, deformation, and animation.

- **Application to Reconstruction from Raw Data:**
Illustration of how SCALIS can aid in reconstructing smooth solids from raw data such as point sets or voxels, leveraging existing skeleton extraction techniques for efficient modeling.

**Paper Link:**

SCALIS (Computer Graphics Forum, 2013) [link](https://inria.hal.science/hal-00863523/file/EG_Homothetic_Surfaces.pdf)

## A Gradient-Based Implicit Blend (2012)

They introduce a new family of binary composition operators to address four major challenges in constructive implicit modeling:
- **Suppressing bulges during shape merging**
- **Preventing unwanted blending at a distance**
- **Ensuring the resulting shape maintains the topology of the union**
- **Allowing for the addition of sharp details without distortion**

![Gradient-Based implicit Blend](/img/Blending.png)

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

## Sketch-Based Modeling of Vascular Systems: a First Step Towards Interactive Teaching of Anatomy (2010)

Develop a sketch-based modeling system to create 3D models of branching vessels from single sketches, inspired by anatomical drawing conventions. This system aims to enhance the teaching of anatomy by allowing professors to sketch structures interactively on a virtual blackboard, generating 3D models for improved visualization and comprehension by students.

![Vascular Systems](/img/Vascular.png)

**Contributions:**

- **Sketch-Based Modeling System:**
The authors present a novel sketch-based modeling system inspired by anatomical drawing conventions. This system constructs plausible 3D models of branching vessels from a single sketch, allowing for interactive teaching of anatomy.
- **Depth Extraction and Modeling:**
The system extracts depth clues from the sketch using contour analysis, hatching, and junction classifications. It then constructs a plausible 3D geometry for the vessels by utilizing skeletal implicit surfaces generated from the sketch.
- **Interactive Visualization:**
To enhance understanding, the resulting 3D models are rendered using expressive rendering techniques that imitate chalk drawing on a blackboard. This visualization method provides intuitive representations of the vascular structures.
- **Performance Optimization:**
The system's performance is optimized to ensure real-time interaction. While computational steps like computing 3D skeletons and evaluating field functions may initially take some time, optimizations such as parallelization on GPU are explored to achieve interactive rendering speeds.
- **Results and Feasibility Demonstration:**
The system demonstrates the feasibility of sketch-based modeling for teaching anatomy by successfully reconstructing the geometry of simple vascular configurations. While no formal user study is conducted, feedback from anatomy professionals validates the effectiveness of the approach.

**Paper Link:**

Vascular Systems (EUROGRAPHICS Symposium on Sketch-Based Interfaces and Modeling, 2010) [link](https://hal.science/hal-00491988v1/file/SBIM2010.pdf)

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



