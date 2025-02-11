# GISTDA-Wildfire-Unsupervised

## Prerequisites

### Anaconda
You need to download Anaconda at https://www.anaconda.com/download and install. And then you would need to create environment from environment.yml file on your computer.

### Anaconda Environment Preparement
Environment Prepare step:
- Open Anaconda Terminal (Anaconda Prompt) on your computer after you installed.
- use following command: ```conda env create -f /path/to/folder/environment.yml```
Example: ```conda env create -f "D:\Sentinel-2 Environment\environment.yml"```

## Sentinel-2 Image Processing Pipeline

### Overview

**This repository provides a Python-based pipeline for processing Sentinel-2 satellite imagery. The pipeline automates the extraction of Sentinel-2 .zip archives, selects the highest-resolution .jp2 bands, resamples them, and computes key spectral indices for wildfire and environmental analysis.**

**Features:**

- Extracts Sentinel-2 .zip archives while preserving folder structures.

- Selects and organizes the highest resolution Sentinel-2 JP2 bands (Bands 1-12 and Band 8A).

- Computes key spectral indices:

    - NBR (Normalized Burn Ratio) for wildfire detection

    - NDVI (Normalized Difference Vegetation Index) for vegetation health monitoring

    - NDWI (Normalized Difference Water Index) for water detection

    - NBRSWIR (Modified NBR using SWIR bands) for enhanced burn area analysis

- Handles long file paths on Windows.

- Resamples images to a target resolution using GDAL.

- Efficiently organizes output into structured directories.

## Folder Structure:

```python
├── sentinel-2/                 # Input folder with Sentinel-2 zip files
├── Classified_Image/           # Extracted JP2 bands organized by granule
├── clustered_result/           # Directories to store clustered results as GeoTIFF
├── Raster_Classified/          # Final processed images with spectral indices
```

## Unsupervised Learning
This response is generated from the `Clustering_KMeans-Sentinel2.ipynb` notebook, which includes code for unsupervised learning using K-Means clustering. With K value is declared equal to 50 and number of Iteration is declared equal to 50.

## References
- Andrew Cutts, Satellite_Imagery_Python / Clustering_KMeans-Sentinel2: https://github.com/acgeospatial/Satellite_Imagery_Python/blob/master/Clustering_KMeans-Sentinel2.ipynb