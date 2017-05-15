# sdf-dragon
A signed distance field embedding of the well-known dragon 3D model, courtesy of [Stanford University Computer Graphics Laboratory](https://graphics.stanford.edu/data/3Dscanrep/)

The original model contains some small holes. To create a manifold (water-tight) mesh, a Poisson reconstruction was first performed, using [Meshlab](www.meshlab.net), with a depth of 10. 

The final signed distance field embedding was computed using [SDFGen](https://github.com/christopherbatty/SDFGen), with the following parameters (0.001 units per voxel and 16 voxels of padding around the model bounds):

```./SDFGen dragon.obj 0.001 16```

The resulting SDF available through this repository, as a VTI file (visualization toolkit image). It can be opened using [ParaView](http://www.paraview.org/).

[![SDF Embedding, in ParaView](https://i.ytimg.com/vi/4CZbFTY0xjw/0.jpg)](https://youtu.be/4CZbFTY0xjw "SDF Embedding, in ParaView")
