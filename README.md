# GISTDA-Wildfire-Unsupervised

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

├── sentinel-2/                # Input folder with Sentinel-2 zip files
├── Classified_Image/          # Extracted JP2 bands organized by granule
├── Raster_Classified/         # Final processed images with spectral indices