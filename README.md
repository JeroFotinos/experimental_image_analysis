# Analysis of Confocal Microscopy Images of Tumorspheres

## Contents
Notebooks:
- `Experimental Image Analysis.ipynb` is the first notebook ever, I mostly used it to explore the file format and Napari.
- `exp_image_analysis.ipynb` first complete analysis (on sph1).
- `pipeline.ipynb` improved and cleaned version for processing in the newly standardize way.
- `pipeline_sph3.ipynb` and `pipeline_sph4.ipynb` are copies of `pipeline.ipynb` for treating the new data of spheroids 3 and 4. The one for sph3 included a process that excluded cells outside a given radius. To avoid having to copy everything, instead of analyzing sph4 in `pipeline_sph4.ipynb`, I made a copy of `pipeline_sph3.ipynb` in `pipeline_in_sph_sph4.ipynb`.
- `pipeline_sph1_slice3.ipynb` is a copy of `pipeline_sph3.ipynb` to reprocess sph1 with a number of changes: the radius of inclusion, a more general way of excluding outliers, and other changes.
- `pipeline_sph1_slice3_artificial_boundary.ipynb` is a cleaned copy of `pipeline_sph1_slice3.ipynb`, sticking to the new approach of introducing artificial points in the Voronoi diagram for bounding the regions of the outer cells of the spheroid, that otherwise would have divergent areas.
- `pipeline_sph1_slice4_artificial_boundary.ipynb` is a copy of the previous one for slice 3 that incorporates some additional results, like the analysis for the robustness of the clustering when varying the random state and the analysis of the graph given by the Delaunay triangulation.
- `pipeline_sph1_slice3_artificial_boundary_NEW.ipynb` is a copy of the previous notebook for running the additional results for slice 3 of sph1.