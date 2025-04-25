# MSCD
Dataset and code release for "A Multi-Spectral Change Detection Dataset (MSCD) using Sentinel-2 satellite imagery". Visualization of MSCD samples with RGB images, single infrared band images and binary change detection masks are as shown as :

<img width="750" alt="image" src="">

**Abstract**: Change detection is a key research topic in the field of remote sensing image analysis. It aims to identify changes on the Earth's surface by comparing images captured at different times over the same geographic area. However, change detection based on visible light images is often susceptible to illumination variations, which can significantly degrade performance. To address this limitation, we construct a Multi-Spectral Change Detection Dataset (MSCD) using Sentinel-2 satellite imagery and provide benchmark results using several deep learning methods. Furthermore, it is feasible to evaluate the effectiveness of incorporating infrared bands by proposing an improved network based on STANet tailored for multi-spectral change detection. Experimental results demonstrate that multi-spectral fusion methods significantly outperform those using only visible or infrared bands individually, highlighting the advantages of multi-spectral data for change detection tasks and offering a reliable solution for analyzing surface changes in complex scenarios.

# Requirements
- mmengine>=2.0
- pytorch>=2.0

# Usage
- Download fro
- Training: `python runner_shift_4_sam.py`
- Test: `python infer.py`
