# PAPER SUMMARY: Extending the CSG Tree Warping, Blending and Boolean Operations in an Implicit Surface Modeling System (1999)

This work aims to organize blending, warping, and Boolean operations to facilitate both global and local operations intuitively. The goal is achieved by structuring implicit surface models using a tree-based approach called the BlobTree, allowing for flexible modeling of complex shapes.

![Implicit Surface Modeling System](/img/Stamingo.png)

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


## Paper Link

You can access the full paper [here](https://perso.liris.cnrs.fr/eric.galin/Articles/1999-blobtree-model.pdf).