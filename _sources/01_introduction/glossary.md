# Glossary

This glossary contains terms used throughout the jupyter book. The descriptions should be interpreted in the context of biological image analysis.

## Active contours

Active contours generally refers to the [active contour model](https://en.wikipedia.org/wiki/Active_contour_model) of deforming a surface using an external force whilst maintaining internal forces. 

## Array

A common term for datastructures that contain multiple values. In python, two common array types are lists and tuples.
Multi-dimensional arrays are also called matrices (in linear algebra and general computing) and hyperstacks (in image processing).

## Binarization

Binarization is the act of segmenting an image into two classes: True and False. True typically is referring to a region in the image where there are objects, also calle the foreground.
False refers to the background region where there are no objects present.

## Binary image

A binary image is an image that contains only two different intensity values. For example the image can contain just boolean values either True and False, numbers such as 0 and 1, or in ImageJ, 0 and 255. Common practice is to associate 0 with False and all other values as True.

## Boolean

A variable of type boolean can only contain two values: True or False.

## Conformalized mean curvature flow (cMCF)


## Conformal map


## Clustering

Algorithms that group objects or pixels together according to their properties are clustering algorithms. These algorithms are used in u-Unwrap3D for i) identifying if a mesh vertex belongs to a protrusion or not (binary protrusion segmentation) and ii) segmenting individual protrusions (instance protrusion segmentation).

## Connected component labeling

Connected component analysis is an algorithm that operates on binary images as input to assign unique labels to each spatially contiguous region. That, is if two pixels are spatially neighboring, they have the same label id, otherwise they have different label ids. See also [wikipedia](https://en.wikipedia.org/wiki/Connected-component_labeling).
Instead of neighboring pixels, for surface meshes we have neighboring vertices and faces. 

## Equiareal map

## Filter

In image analysis, a filter is an operation that takes an input image to produce an output image. This operation is used to enhance desired image features for example smoothing out noise in the image or enhancing the edge contrast.

## Genus

Genus is a mathematical property of a shape. Intuitively it is the number of holes a shape has. See: [Wikipedia](https://en.wikipedia.org/wiki/Genus_(mathematics)). 
A genus-0 mesh is one that has no holes and can be deformed onto a 3D sphere without cutting or stitching. 

## Instance segmentation

Segmentation algorithms that identify individual objects, in particular assigning to each object a unique integer id. For images, this results in a label image or for meshes, labeled vertices or faces. All pixels, vertices, faces with the same id belong to the same object.

## Intensity image

Intensity images are typically produced by microscopes, cameras and medical tomography devices. The intensity in the pixels of the image describe a physical measurement, e.g. of the number of photons that hit the detector during acquisition.

## Isometric map

## Isotropic meshing

## Kernel

A filter kernel describes how local pixel intensities around a given pixel need to be combined using a weighted sum to [convolve](#convolution) an input image.

## Parametrization

Parametrization is the act of indexing a shape or space in terms of a coordinate system. For example spherical parameterization is indexing of a 3D surface using the spherical coordinate system. uv parameterization is the mapping of a 3D surface using a rectangular coordinate system.


## Reference surface


## Semantic segmentation

Associating pixels, mesh vertices, mesh faces with a category such as "cytoplasm" or "nucleus" but not specifying which cell or nucleus. 

## Spherical parameterization

## Surface meshing

The process of extracting a mesh of the surface from a [binary image](#binary-image). This is typically done by using algorithms that trace the contour of a shape e.g. [marching cubes](https://en.wikipedia.org/wiki/Marching_cubes).


## Surface protrusion


## Topographic space


## Topographic surface


## uv parameterization