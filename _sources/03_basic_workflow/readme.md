# Standard workflow for unwrapping 3D surfaces

This chapter will illustrate in code how to implement the illustrated standard workflow of mapping an input cell surface segmented from a microscopy image into other lower-dimensional representations which can be used for computing and visualization purposes. Throughout the transformation, we will map the mean curvature of the original surface denoted $S(x,y,z)$ 

![](../01_introduction/u_unwrap3D_overview.png)


## A note on mathematical nomenclature

- **Notation for surface geometry **
    - $S(x,y,z)$: input 3D Cartesian $(x,y,z)$ surface
    - $S_{\text{ref}}(x,y,z)$: reference 3D Cartesian $(x,y,z)$ surface
    - $S_{\text{ref}}(r,\theta,\phi)$: 3D spherical parameterization of $S_{\text{ref}}(x,y,z)$
        - $S_{\text{ref}^{\mathcal{Q}}}(r,\theta,\phi)$: (quasi-)conformal spherical parameterization of $S_{\text{ref}}(x,y,z)$
        - $S_{\text{ref}^{\Ohm}}(r,\theta,\phi)$: (quasi-)equiareal spherical parameterization of $S_{\text{ref}}(x,y,z)$
    - $S_{\text{ref}}(u,v)$: 2D uv parameterization of $S_{\text{ref}}(x,y,z)$
    - $S(d,u,v)$: 3D topographic surface of $S(x,y,z)$, relative to $S_{\text{ref}}(x,y,z)$