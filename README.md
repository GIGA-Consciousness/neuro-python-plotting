# neuro-python-plotting
Various scripts to plot neuroimaging results using python:

* **barplotwithsamples.ipynb** is a Jupyter Notebook script to plot bars with 90% Confidence Interval error bars and also the subjects points and (optionally) the subjects labels. It just expects as input a txt file with one value per line (one value = one subject). It works particularly well with CONN REX output (results.ROIs.rex.data.txt). It can also plot multiple ROIs, and it can visualize the ROI maps on a glass brain and synchronize with the bar display (same color as glass brain + ROIs centers' coordinates will be displayed in the bar plot + atlas regions names covered by ROIs will be extracted from AAL2 atlas).

  ![barplotwithsamples example image](https://raw.githubusercontent.com/lrq3000/neuro-python-plotting/master/img/barplotwithsamples.png)

  ![rois_glass_brain example image](https://raw.githubusercontent.com/lrq3000/neuro-python-plotting/master/img/rois_glass_brain.png)

  ![rois_bars example image](https://raw.githubusercontent.com/lrq3000/neuro-python-plotting/master/img/rois_bars.png)

* **plot-residual-errors-recursive-checker.ipynb** is a Jupyter notebook that will recursively find all residual error images (ResMS.img|nii for SPM) of a General Linear Model (GLM) and will compute descriptive statistics. Alert thresholds can be set for any feature of these statistics, and a report of the images reaching above those thresholds will be generated, with a histogram plot of residual error repartition as well as a neuroimage plot to spatially localize where the biggest errors are localized.

![residual error recursive checker example image](https://raw.githubusercontent.com/lrq3000/neuro-python-plotting/master/img/residual-error-recursive-checker.png)

* **plot_correl_maps_overview.ipynb** is a Jupyter notebook to plot a LOT of correlation maps in a concise manner. The visualization consists of multiple glass brain images, stacked on a grid, according to your needs (eg, columns for contrasts, rows for groups/conditions). It can also plot a single image. It supports both plotting correlation maps and contours (particularly useful to plot unthresholded correlation map, with contours of significant/thresholded maps), both negative and positive. It can also synchronize the colorbar range, so that the same colorbar is used either for all figures, or for all figures in a row, or each figure with an individual colorbar (unsynchronized).