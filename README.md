# Analysis of Confocal Microscopy Images of Tumorspheres

## Contents
Notebooks:
- `Experimental Image Analysis.ipynb` is the first notebook ever, I mostly used it to explore the file format and Napari.
- `exp_image_analysis.ipynb` first complete analysis (on sph1).
- `pipeline.ipynb` improved and cleaned version for processing in the newly standardize way.
- `pipeline_sph3.ipynb` and `pipeline_sph4.ipynb` are copies of `pipeline.ipynb` for treating the new data of spheroids 3 and 4. The one for sph3 included a process that excluded cells outside a given radius. To avoid having to copy everything, instead of analyzing sph4 in `pipeline_sph4.ipynb`, I made a copy of `pipeline_sph3.ipynb` in `pipeline_in_sph_sph4.ipynb`.
- `pipeline_sph1.ipynb` is a copy of `pipeline_sph3.ipynb` to reprocess sph1 with a number of changes: the radius of inclusion, a more general way of excluding outliers, and other changes.