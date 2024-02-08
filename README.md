# Analysis of Confocal Microscopy Images of Tumorspheres
Code for analyzing confocal microscopy images. The `.czi` stack files for each spheroid can be found in the `data` directory. For the analysis of each one of them, refer to the list of “current pipelines” at the end of the Contents section.

![](https://github.com/JeroFotinos/experimental_image_analysis/raw/main/results/sph1_reprocessed/slice_3/nuclei_voronoi_in_sph_only_sox2_clustered_tails_cut_in_sph_with_artificial_boundary_cropped_NEW.png)

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
- `pipeline_sph3_slice3_artificial_boundary.ipynb` is a copy of `pipeline_sph1_slice4_artificial_boundary.ipynb` for running the additional results for this case.
- `pipeline_sph4_slice2_artificial_boundary.ipynb` is a copy of `pipeline_sph3_slice3_artificial_boundary.ipynb` for running the additional results for this case.

Current pipelines:
- For `Sph1`, slice 3, `pipeline_sph1_slice3_artificial_boundary_NEW.ipynb`;
- For `Sph1`, slice 4, `pipeline_sph1_slice4_artificial_boundary.ipynb`;
- For `Sph3`, slice 3, `pipeline_sph3_slice3_artificial_boundary.ipynb`;
- For `Sph4`, slice 2, `pipeline_sph4_slice2_artificial_boundary.ipynb`.
