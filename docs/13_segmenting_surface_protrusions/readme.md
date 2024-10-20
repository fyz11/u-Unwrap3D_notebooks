# Segmenting surface protrusions

Cell surface protrusions have micron-scale curvature which may act as diffusion traps for molecular signals. They may also serve mechanically to interact with the environment or with other cells. Given a 3D cell surface, we would like to specifically identify what part of the surface are protrusions and potentially even each individual protrusion for further quantitative analysis, for example tracking the individual protrusions over time or 

In this section we present several possible methods for identifying protrusions using u-Shape3D. We distinguish between the task of 1) binary segmentation, identifying what is or is not protrusive and 2) instance segmentation, identifying each individual protrusion and their associated vertices and faces of the input mesh. 

1. Binary protrusion segmentation (Is this part of the surface a protrusion - Yes/No)
    - construct a protrusion 'height' function that can be evaluated at each vertex of the mesh 
    - measure the height at each vertex
    - binary threshold according to the measured height. 

2. Instance protrusion segmentation (Identifying each individual protrusion and assigning to each a unique label)
    - find positive curvature 'seeds' to binary identify tips of protrusions
    - use connected component analysis to identify individual spatially-contiguous areas as belonging to individual protrusions
    - Diffuse these seed label ids accounting for spatial connectivity and local surface convexity to cover the rest of the protrusion.

> [!NOTE] 
> We can segment protrusions using the above from either:
> 
>   i). input 3D $S(x,y,z)$ surface mesh
>
>   ii). topography 3D $S(d,u,v)$ surface mesh 
>
> $S(d,u,v)$ can pick up more protrusion particularly smaller protrusions however, it requires handling of the boundary conditions and an $S_{\text{ref}}(x,y,z)$ that allows each protrusion to be sufficiently visualized in $S(d,u,v)$. 

