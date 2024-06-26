# Overview
- [Sketch-Based Modeling & Implicit Surfaces](#sketch-based-modeling--implicit-surfaces)
- [Tree Modeling & Reconstruction on Large Scales](#tree-modeling--reconstruction-on-large-scales)

# Sketch-based Modeling & Implicit Surfaces

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

## Bio-Sketch: A new medium for interactive storytelling illustrated by the phenomenon of infection (2023)

They develop a progressive sketching system, Bio-Sketch, to facilitate the creation of animated illustrations for communicating dynamic biological phenomena, focusing on the infection phenomenon. The goal is to bridge the gap between expert and non-expert audiences by providing an intuitive tool for enriching scientific representations in biology.

![Bio-Sketch](/img/Blood.png)

**Contributions:**

- **Progressive Sketching Paradigm:**
Introduces a seamless blend of 3D modeling and pattern-based shape distribution for creating animated biological illustrations.

- **Interactive Narrative Design Tools:**
Enables users to experiment with narrative design to foster effective communication in educational contexts.

- **Intuitive Creation of Environments:**
Offers intuitive tools for sketching complex biological structures to enhance visualization efficiency.

- **Empowering Visual Expression:**
Provides scientists with simplified yet comprehensive tools for visualizing hypotheses and findings.

- **Sketch-Based Motion Specification:**
Facilitates precise control over animation through sketch-based input to enhance storytelling capabilities.

- **Expressive Rendering Mechanism:**
Incorporates an expressive rendering approach using transparency and shape cuts.

**Paper Link:**

Bio-Sketch (Eurographics Workshop on Visual Computing for Biology and Medicine, 2023) [link](https://hal.science/hal-04216965/file/BioSketch_2023_Preprint.pdf)

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

# Tree Modeling & Reconstruction on Large Scales

## A Physically-inspired Approach to the Simulation of Plant Wilting (2023)

**Goal:**
to develop a physically-inspired approach for simulating plant wilting (focus on dynamic deformation caused by internal wilting processes due to insufficient water supply) They want to create a simulation framework that accurately captures the behavior of wilting plants by integrating a model of water distribution and its effect on plant stiffness

**Why important?**
They provide a tool for generating realistic synthetic training data for machine learning algorithms in agricultural applications

![Plant Wilting](/img/Wilting.png)

**Contributions:**

- **Understanding Plant Dynamics:**
Simulating Hidden Water Flow for Accurate Behavior Reproduction

- **Towards Realistic Plant Simulation:**
A Physically-Inspired Model for Hidden Water Flow

- **Integrating Water Flow Dynamics with Wilting Behavior:**
A Stiffness Mapping Approach for Physically Accurate Simulation

**Paper Link:**

Plant Wilting (SIGGRAPH Asia, 2023) [link](https://dl.acm.org/doi/pdf/10.1145/3610548.3618218)

## TREESKETCHNET: FROM SKETCH TO 3D TREE PARAMETERS GENERATION (2022)

The goal of the presented work is to address the challenge of manual mesh modeling of complex 3D objects, such as trees, by introducing an automated approach using deep learning. They introduce a method to efficiently create a large training dataset of synthetic tree sketches and corresponding parameters. This dataset encompasses various tree species and visual styles.


![TreeSketchNet](/img/SketchNet.png)

**Contributions:**

- **Custom Deep Neural Network (DNN) Architecture:**
A specialized DNN architecture is proposed, tailored to predict parameters governing the 3D geometry of trees based on input sketches. The architecture includes multiple output branches, each responsible for different parameter ranges, enhancing model adaptability and performance.

- **Parameter Analysis and Mapping:**
The study conducts an in-depth analysis of tree parameters, categorizing them into fixed and unfixed subsets with defined ranges. This analysis facilitates precise control over tree geometry during synthesis, ensuring fidelity to input sketches.

- **Overfitting and Underfitting Mitigation:**
To address common challenges in deep learning models, such as overfitting and underfitting, the paper employs various techniques like dropout layers, skip connections, and regularization. These techniques enhance model generalization and performance across diverse tree species and visual styles.

**Paper Link:**

TreeSketchNet (ACM Transactions on Intelligent Systems and Technology, 2022) [link](https://arxiv.org/pdf/2207.12297.pdf)

## ICTree: Automatic Perceptual Metrics for Tree Models (2021)

The authors introduce ICTree, a novel automatic no-reference realism predictor that evaluates the perceived level of realism of synthetic tree models either from images (ICTreeI) or from their easily calculated features (ICTreeF). The goal of the research is to develop an automated system for assessing the perceived visual realism of virtual tree models based on human perception. This system aims to bridge the gap between the geometric details of synthetic vegetation models and their perceived realism.

![ICTree](/img/ICTree.png)

**Contributions:**

- **CTree Framework Development:**
Creation of ICTree, a new framework for automatically assessing the perceived visual realism of synthetic tree models.

- **Datasets Preparation:**
Curation of three large datasets comprising 3D tree models with perceived user realism scores, tree images with corresponding realism scores, and tree view images for neural network training.

- **Feature Importance Analysis:**
Identification of critical features such as branching angles, branch length, and width through analysis of intrinsic tree attributes that significantly impact perceived realism.

- **Methodology Design:**
Design of a comprehensive methodology encompassing data generation, unification, user study design, and realism predictor training for automatic assessment of visual realism.

**Paper Link:**

ICTree (ACM Transactions on Graphics, 2021) [link](https://dl.acm.org/doi/pdf/10.1145/3478513.3480519)

## Learning to Reconstruct Botanical Trees from Single Images (2021)

The paper aims to address the challenging task of efficiently and accurately reconstructing realistic 3D tree models from single images, aiming to overcome the limitations of capturing tree geometry with limited sensor data while enabling large-scale reconstruction.

![Botanical Trees](/img/Botanics.png)

**Contributions:**

- **Introduction of Radial Bounding Volumes (RBVs):**
A novel lightweight fixed-size 3D representation for tree models, facilitating efficient encoding of tree form while preserving essential shape features.

- **Pipeline of Three Neural Networks:**
Proposal of a comprehensive pipeline consisting of three neural networks: semantic segmentation for mask generation, species identification for priming tree growth, and RBV estimation for geometric structure inference.

- **Novel Bi-Modal Developmental Model:**
Introduction of a unique bi-modal developmental model for trees, combining phenomenological and self-organizing growth mechanisms to simulate realistic branching structures.

- **Proposal of Novel Evaluation Metrics:**
Introduction of novel metrics to assess tree form similarity, including leaf area index and maximum radial tree distances, enabling quantitative evaluation of the reconstruction approach.

- **Enablement of Automatic Large-Scale Reconstruction:**
Development of an approach allowing for automatic large-scale reconstruction of tree models from single images, distinguishing it from existing methods requiring user annotations or intensive parameter tuning.

**Paper Link:**

Reconstruct Botanical Trees (ACM Transactions on Graphics, 2021) [link](https://dl.acm.org/doi/pdf/10.1145/3478513.3480525)

## Statistical Modeling ofthe 3D Geometry and Topology of Botanical Trees (2018)

The goal of the proposed framework is to provide a data-driven approach for synthesizing new 3D botanical trees by modeling the geometric and topological variability in a population of existing trees, facilitating the generation of diverse and realistic tree models for various applications such as virtual environments, gaming, and simulation.

![Statistical Modeling](/img/Statistical.png)

**Contributions:**

- **Tree-Shape Space Representation:**
Introducing a novel representation for botanical trees in a geometric and topological space, enabling comprehensive analysis and synthesis.

- **Elastic Metric for Tree Dissimilarities:**
Development of an elastic metric to quantify dissimilarities between botanical trees, enhancing accuracy in geodesics and deformations.

- **Statistical Modeling Techniques:**
Implementing statistical modeling techniques to compute mean trees and modes of variation within a population, providing insights into the variability of botanical trees.

- **Random Tree Synthesis:**
Synthesizing random instances of botanical trees by fitting probability distributions to the population in the tree-shape space, facilitating the generation of diverse tree models.

- **Interactive 3D Tree Synthesis:**
Introducing an interactive tree synthesis method using a simple sketching interface, enabling users to create customized tree models efficiently.

- **Experimental Evaluations and User Studies:**
Demonstrating the efficiency and effectiveness of the framework through rigorous experimental evaluations and user studies, validating the improvements in geodesics and synthesis results.

**Paper Link:**

Statistical Modeling (Computer Graphics Forum, 2018) [link](https://onlinelibrary.wiley.com/doi/epdf/10.1111/cgf.13501)

## Tree Growth Modelling Constrained by Growth Equations (2017)

The goal of the proposed integrated growth modelling (IGM) approach is to simulate tree growth while considering constraints from both tree properties and environmental factors such as light resource, space occupation, and environmental impacts. By integrating this information into growth equations using a small number of parameters, the method aims to generate realistic tree structures that accurately represent their shapes and growth processes.

![Growth Equations](/img/Growth.png)

**Contributions:**

- **Biological Constraints:**
The IGM approach incorporates biological and physical constraints to simulate tree growth realistically, aligning with established tree height theory and natural attributes.

- **Environmental Integration:**
By integrating environmental factors like light resource and space occupation, the method enhances the realism of simulated tree structures by considering external influences on growth.

- **Flexible Growth Equations:**
Offering a range of growth equations including logistic, Bertalanffy, and Weibull, the approach allows for diverse tree shapes and growth patterns tailored to specific needs.

- **Detailed Modelling Pipeline:**
The algorithm provides a comprehensive pipeline for tree growth modelling, covering resource allocation, branching direction determination, environmental impact calculation, and branch shedding.

- **Numerical Validation:**
Emphasizing numerical analysis for model validation ensures reliability by aligning simulated growth with established formulas and equations.

**Paper Link:**

Growth Equations (Computer Graphics Forum, 2017) [link](https://onlinelibrary.wiley.com/doi/pdf/10.1111/cgf.13263)

## Tree Modeling with Real Tree-Parts Examples (2016)

The goal is to develop an intuitive and efficient method for generating highly realistic 3D tree models with complex branching structures and fine-level geometric details, while minimizing the required user expertise and interaction effort. This includes leveraging database-driven techniques, allometric constraints, and user-guided foliage production to achieve naturalistic tree representations in various applications such as urban modeling, gaming, and movie production.

![Real Tree-Parts](/img/TreeParts.png)

**Contributions:**

- **Database Creation:**
Establishment of a database of 3D real-life trees captured using scanning devices.

- **Preprocessing Techniques:**
Development of preprocessing steps to reconstruct tree models into 3D meshes, focusing on branch geometries.

- **User-Friendly Interface:**
Implementation of a user-friendly modeling interface for selecting and positioning tree-cuts in 3D space.

- **Sketch-Based Retrieval Tool:**
Introduction of a sketch-based tree-cut retrieval tool to facilitate browsing and suggesting tree-cut candidates from the repository.

- **Allometric Constraints Integration:**
Integration of allometric constraints to optimize branching diameters and angles based on botanical realism.

- **Geometry Transfer:**
Application of geometry transfer techniques to enhance interpolated surfaces with detailed geometry from the database.

- **Foliage Production Control:**
Implementation of foliage production control, allowing users to sketch 2D loops to define major lobe contours and guide foliage growth.
User Study Evaluation: Conducting a user study to evaluate the effectiveness of the method in modeling complex trees with limited user expertise.

**Paper Link:**

Real Tree-Parts (IEEE Transactions on Visualization and Computer Graphics, 2016) [link](https://kops.uni-konstanz.de/server/api/core/bitstreams/0ead7c1e-e0dd-4d81-9936-06439c466b1e/content)

## A Procedural Approach to Modelling Virtual Climbing Plants With Tendrils (2016)

The goal of this study is to develop a procedural approach for modeling climbing plants with tendrils in a virtual environment. The focus is on producing visually plausible results rather than accurately simulating biological development. The aim is to generate climbing plant models with tendrils that exhibit realistic behavior, including twining around structures and exhibiting coiling patterns.

![Climbing Plants](/img/Climbing.png)

**Contributions:**

- **System Overview:**
Provides an overview of the proposed approach, outlining the components of a climbing plant model with tendrils, including the main stem, internodes, tendrils, and leaves.

- **Stems:**
Describes the growth behavior of stems, incorporating positive phototropism and negative geotropism. Details methods for determining stem growth direction and handling twining around cylindrical hosts.

- **Tendrils:**
Discusses the growth, searching behavior, and coiling patterns of tendrils. Describes how tendrils grow from stem nodes, search for host objects, and coil around them.

- **Collision Detection and Handling:**
Explains techniques for detecting and handling collisions between plant components, such as stems, tendrils, and leaves, and environmental objects.

**Paper Link:**

Climbing Plants (Computer Graphics Forum, 2015) [link](https://onlinelibrary.wiley.com/doi/pdf/10.1111/cgf.12736)

## Full 3D Plant Reconstruction via Intrusive Acquisition (2015)

Thy address the challenge of accurately acquiring and modeling the full geometry and topology of 3D plants from scans, aiming to overcome the limitations of standard scanning techniques and provide a robust framework for realistic plant reconstruction.

![Intrusive Acquisition](/img/Profile.png)

**Contributions:**

- **Intrusive Acquisition System:** 
Introduction of a novel intrusive acquisition system for reconstructing the full geometry and topology of plants from 3D scans.

- **Disassembly-Reassembly Approach:**
Development of a disassembly-reassembly approach to scan and model disjoint parts of the plant independently, mitigating self-occlusion issues.

- **Non-rigid Registration Algorithm:**
Proposal of a non-rigid registration algorithm that globally registers the disjoint parts back into the base geometry, ensuring accurate plant reconstruction.

- **Demonstration of Effectiveness:**
Demonstration of the effectiveness of the proposed framework in acquiring detailed 3D plant models, even in cases of complex topology and self-occlusions.

**Paper Link:**

Intrusive Acquisition (Computer Graphics Forum, 2015) [link](https://onlinelibrary.wiley.com/doi/pdf/10.1111/cgf.12724)

##   Procedural Tree Modeling with Guiding Vectors (2015)

The goal of the algorithm is to automate the process of tree modeling, specifically focusing on generating the spatial arrangement of tree architecture, including trunks and branches, without requiring manual intervention or external data inputs such as laser scans or photographs.

![Guiding Vectors](/img/Winter.png)

**Contributions:**

- **Introduction of Guiding Vectors:**
The algorithm introduces the concept of guiding vectors for setting edge weights in the tree graph. These vectors allow for local control over branch orientation, enabling the specification of medium-scale flow of branches while maintaining the advantages of single-source shortest paths.

- **Mechanism for Guiding Vector Assignment:** 
The algorithm proposes a mechanism for assigning guiding vectors to nodes incrementally as the shortest-paths algorithm progresses. This approach allows for the specification of intermediate-scale tree architecture with simple rules, enhancing the controllability of the modeling process.

- **Complete Graph-Based Tree Modeling System:**
The paper presents a comprehensive tree modeling system based on graphs, including automatic graph construction, endpoint selection, and hierarchical structure creation. This system enables the generation of diverse tree structures efficiently and autonomously.

**Paper Link:**

Guiding Vectors (Pacific Graphics, 2015) [link](https://onlinelibrary.wiley.com/doi/pdf/10.1111/cgf.12744)

## Data-Driven Synthetic Modeling of Trees (2014)

The goal of this research is to develop a data-driven approach for synthesizing realistic 3D tree models from single laser scan data, focusing on visible shape information recovery and non-visible information synthesis. This includes reconstructing tree models driven solely by scan data and incorporating human perception of tree shapes to generate accurate representations suitable for various applications.

![Synthetic Modeling](/img/Color.png)

**Contributions:**

- **New Tree Representation:**
Introducing a novel tree representation method driven by scan data, enabling precise modeling of tree shapes by defining and extracting tree shape features through shape analysis of laser scan data.

- **Algorithms Development:**
Marching Cylinder Algorithm: Proposed an algorithm for computing the skeletons and radii of visible branches from scan data, facilitating the reconstruction of main branch skeletons accurately.
Hierarchical Particle Flow Algorithm: Developed an automatic algorithm for modeling the crown shape consistent with scan data, enabling the synthesis of non-visible branches by guiding particle flows based on crown attraction points.

- **Multi-layer Tree Modeling:**
Presented a multi-layer representation of tree structures, extending existing methods to accurately represent branching hierarchies, which is particularly beneficial for large trees and user-friendliness.

- **Real-time Applications:**
Demonstrated the utility of the reconstructed tree models in real-time scenarios such as video games or simulators, enhancing their visual fidelity and realism.

- **Parameter Specification:**
Established parameters for tree reconstruction related to noise scale, point density, and tree structure, facilitating the application of the proposed methods in various environmental settings.

- **Model Completion:**
Completed the tree model by meshing branch models and attaching leaves to tertiary branches and twigs, providing a comprehensive solution for generating realistic 3D tree models from scan data.

**Paper Link:**

Synthetic Modeling (  IEEE Transactions on Visualization and Computer Graphics, 2014) [link](https://www.researchgate.net/profile/Xiaopeng-Zhang-9/publication/264243196_Data-Driven_Synthetic_Modeling_of_Trees/links/54f725100cf210398e9214b4/Data-Driven-Synthetic-Modeling-of-Trees.pdf)

## TreeSketch:Interactive Procedural Modeling of Trees on a Tablet (2012)

The paper aims to develop TreeSketch, a system that combines procedural tree generation with detailed control through a multi-touch tablet interface, enabling the creation of diverse and artistically expressive trees efficiently.

![TreeSketch](/img/TreeSketch.png)

**Contributions:**

- **Procedural Tree Generation:**
Introduction of a procedural component based on tree self-organization, allowing for the simulation of branch competition for space and light during tree development.

- **Multi-Touch Tablet Interface:**
Development of an intuitive interface that provides detailed control over tree form using a brush tool, enabling users to specify branch trajectories, define large branches, and direct growth into predefined shapes.

- **Combination of Procedural Methods with Detailed Control:**
Proposal of a method that combines procedural tree generation with interactive control over tree form, offering users the flexibility to direct growth, edit forms, and achieve diverse tree designs.

- **Selective Growth Mode:**
Introduction of a selective growth mode, enabling users to limit growth to specific branches, facilitating the creation of large new branches without interference from existing ones.

- **Editing Operations:**
Implementation of editing operations such as branch shape modification, selective branch width modification, pruning, and undo functionality, providing users with comprehensive tools for refining tree designs.

**Paper Link:**

TreeSketch (EUROGRAPHICS Symposium on Sketch-Based Interfaces and Modeling, 2012) [link](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=f185d46cfef880a2335fc71706f02d5a594ed730)

## Texture-Lobes for Tree Modelling (2011)

Present a lobe-based tree representation for efficient modeling and synthesis of tree geometry, along with encoding and decoding techniques. Highlight its advantages through reconstruction of laser-scanned trees and re-representation of existing models, emphasizing its applicability in various scenarios, including interactive urban environment applications.

![Texture-Lobes](/img/Lobes.png)

**Contributions:**

- **Introduction of Lobe-Based Representation:**
Proposing a novel lobe-based tree representation for efficient modeling and synthesis of tree geometry.

- **Encoding and Decoding Techniques:**
Development of techniques for encoding tree data into the lobe-based representation and decoding it for synthesis of detailed tree models.

- **Demonstration of Advantages:**
Illustrating the method's advantages through reconstruction of laser-scanned trees and re-representation of existing models.

- **Applicability Evaluation:**
Evaluating the method's applicability in various scenarios, including interactive urban environment applications.

- **Efficiency Insights:**
Providing insights into the potential of the lobe-based representation for efficient storage, transmission, and rendering of trees.

**Paper Link:**

Texture-Lobes (ACM Transactions on Graphics, 2011) [link](https://dl.acm.org/doi/pdf/10.1145/2010324.1964948)

## Automatic Reconstruction of Tree Skeletal Structures from Point Clouds (2010)

The goal of this paper is to present an automatic approach for reconstructing the skeletal structures of real-world trees from point cloud data obtained through active laser scanning. The method aims to robustly capture the geometry of trees, including their branching patterns and overall structure, without the need for significant user interaction.

![Automatic Reconstruction](/img/Reconstruction.png)

**Contributions:**

- **Global Optimization for Tree Reconstruction:**
Introduces a method based on global optimization techniques to reconstruct the skeletal structures of trees from sparse, incomplete, and noisy point cloud data

- **Automatic Tree Segmentation:** 
Presents a technique for automatically segmenting multiple overlapping trees from input point cloud data, eliminating the need for manual segmentation and enabling the reconstruction of individual trees within a dense vegetation environment.

- **Branch-Structure Graph (BSG) Representation:**
Proposes the use of Branch-Structure Graphs (BSGs) to represent the skeletal structures of trees, providing a compact and informative representation that facilitates further geometry completion and synthesis.

- **Iterative Refinement Process:**
Describes an iterative refinement process for improving the accuracy and completeness of tree reconstructions, which includes steps for refining the initial BSGs, optimizing vertex positions, and synthesizing fine geometry such as branches and leaves.

- **Data-Driven Reconstruction Pipeline:**
Presents a data-driven reconstruction pipeline that adapts to the characteristics of the input point cloud data, allowing for the reconstruction of trees of various types and sizes while maintaining robustness and scalability.

- **Experimental Validation:**
Demonstrates the effectiveness and robustness of the proposed approach through experiments conducted on raw scans capturing different tree varieties and environmental conditions.

**Paper Link:**

Automatic Reconstruction (ACM Transactions on Graphics, 2010) [link](https://dl.acm.org/doi/pdf/10.1145/1866158.1866177)

## Sketch-based Tree Modeling by Distribution Control on Planes (2010)

The goal of this research is to develop a method for generating realistic 3D models of trees from simple sketches or images, enabling easy and intuitive tree modeling for various applications in computer graphics and virtual environments.

![Distribution Control](/img/Distribution.png)

**Contributions:**

- **Image-based Sketching:**
Present a technique for using tree images as sketching guidance to mark up main branch structures and crown silhouettes, providing both structure and depth range information.

- **Construction of 3D Main Branches:**
Introduce a method for constructing 3D main branches from 2D skeletons while ensuring conformance to shape restrictions, utilizing distribution control theory to adjust branch distribution on multiple horizontal planes.

- **Extraction of Boundary Information:**
Propose a process for extracting depth range information from sketches containing boundary branches, facilitating the determination of 3D skeleton depth range.

- **Computation of Skeleton Depth Range:**
Describe a procedure for computing the depth range of skeleton points to convert 2D skeleton points into corresponding 3D points while considering different scenarios.

- **From 2D to 3D:**
Outline the steps involved in converting 2D skeleton points into 3D points, including the establishment of reference frames and the application of distribution control to ensure realistic 3D branch construction.

- **Small Branch Growth:**
Detail the method for modeling small branches by copying parts of main branches and linking them with an angle, enriching the tree crown through branch propagation while adhering to growth restrictions.

- **Adding Leaves:**
Explain how leaves or fruits are represented and added to the tree model, including the placement of textured quadrilateral leaf mesh models on small branches with random factors for variation.

**Paper Link:**

Distribution Control (ACM SIGGRAPH Conference on Virtual-Reality Continuum and its Applications in Industry, 2010) [link](https://dl.acm.org/doi/pdf/10.1145/1900179.1900219)

## Structure from silhouettes: a new paradigm for fast sketch-based design of trees (2009)

The goal of this research is to develop a computational approach for inferring the 3D structure of trees from multiple silhouettes, inspired by the drawing methodologies of botanists and traditional artists, enabling intuitive and efficient tree modeling in computer graphics applications.

![Structure from silhouettes](/img/Silhouettes.png)

**Contributions:**

- **Drawing Methodologies Fusion:**
Integrating the drawing techniques of botanists and artists, leveraging their insights to develop a novel method for inferring tree structures from multiple silhouettes, combining accuracy with artistic freedom.

- **Silhouette-Based Inference:**
Proposing a method for inferring the 2D structure of trees from their silhouettes, utilizing geometric skeleton analysis and botanical knowledge to accurately identify major branches and sub-silhouettes.

- **Branch Generation and Refinement:**
Introducing algorithms for inferring branch shapes and positions based on botanical principles and user input, facilitating the creation of natural-looking tree structures while allowing for user refinement.

- **Recursive Refinement and Style Transfer:**
Presenting a recursive refinement process for inferring sub-silhouette shapes and transferring style attributes between branches, enabling the creation of complex tree structures with consistent aesthetics.

- **3D Positioning and Optimization:**
Developing methods for positioning tree branches in 3D space while adhering to silhouette constraints and botanical laws, utilizing optimization techniques to generate realistic tree configurations.

- **Phyllotactic Pattern Modeling:**
Incorporating phyllotactic principles into the branch positioning process, allowing for the simulation of various organ arrangements observed in real plants and enhancing the realism of generated tree models.

**Paper Link:**

Structure from silhouettes (EUROGRAPHICS, 2009) [link](https://core.ac.uk/download/pdf/52632017.pdf)

## Self-organizing tree models for image synthesis (2009)

The paper aims to present a method for generating realistic models of temperate-climate trees and shrubs. It integrates self-organizing principles with architectural models, illustrating how simulations of this process can generate a wide range of realistic trees. Additionally, the paper demonstrates how these forms can be controlled using interactive techniques.

![Self-organizing tree models](/img/Tree.png)

**Contributions:**

- **Integration of Self-Organization and Architecture:**
The method combines self-organizing principles with architectural models, improving the visual realism of tree models. It captures the balance between regularity and variability seen in temperate-climate trees.

- **Apical Control for Tree Form Variation:**
Apical control inclusion enables the generation of diverse tree forms, enhancing the versatility of the models.

- **Interactive-Procedural Modeling:**
The paper introduces interactive techniques like procedural brushes and sketching, allowing users to manipulate tree development and form.

- **Implementation and Performance:**
Despite tree complexity, the method achieves short generation times using fast approximate algorithms. It's implemented within an L-system-based modeling environment, demonstrating practical applicability.

- **Visual Realism and Versatility:**
Through examples, the paper showcases the visual realism and versatility of the generated tree models, illustrating their usefulness in various applications.

**Paper Link:**

Self-organizing tree models (ACM Transactions on Graphics, 2009) [link](https://dl.acm.org/doi/pdf/10.1145/1531326.1531364)



