# Spatial Resolution Improvement (Downscaling) of Daily-scale Weather Datasets Using Machine and Deep Learning 

## Motivation
The motivation of  this project comes from the `Environmental Clustering App` developed by `X company`. This app have various business values, such as understanding of germplasm response, G x E modeling, testing footprint optimization, finding alternative testing location, market expansion, etc. The app needs 20-yrs of weather data, soil, elevation data, but the bottleneck for improved resolution arises due to unavailability of high-resolution long-term weather data. Currently, the app uses weather datasets from AA (low spatial resolution – long temporal records) and BB (high spatial resolution – short temporal records) from data warehouse. But there is no sources of high-resolution long-term weather datasets in warehouse. Here, we have build a framework that uses machine learning/deep learning models and spatial interpolations methods to harmonize all datasets required for the clustering app to high resolution, specially the weather datasets.

## Resolution Improvement of Weather Data
The AA dataset in of low spatial resolution (28km) with extended (1979-present) daily temporal records. The BB historical weather datasets if of 4km and BB High-Resolution precipitation dataset if of 8km high spatial resolution, but with limited (2015-2023) daily temporal records. Our goal is to use AA datasets as input variables, along with other datasets like elevation, and BB datasets as target/training variable in a machine/deep learning (ML/DL) based framwework. The ML/DL models will generate high spatial resolution (4km) weather datasets for a 20 year timeline, thus resolvng the resolution issue of weather data in the clustering app. 

![image](https://github.com/mdfahimhasan/data-pipeline-env-model/assets/77580408/9beb1aee-1772-4cf8-8e52-9a89026cda69)

## Analytysis-Ready Dataset (ARD) Frameworks
The ML/DL models along with spatial interpolation techniques (e.g. Bilinear Interpolation) will be used in a framework that will generate Analytysis-Ready Dataset (ARD) for the Environmental Clustering App. In this pipeline, two versions of the framework for two spatial resolutions will be made. These two versions of the framework will create ARDs in 4km and 100m resolution. The `4km resolution ARD` consists of weather, soil, and elevation datasets. The `100m resolution ARD` consists of satellite data along with the weather, soil, and elevation datasets. Also, the 100m resolution ARD has only been developed for Woodland Site only as satellite data is available for this spatial extent only. In contrast, the 4km resolution ARD covers the entire Region of Interest (ROI) of this project, a part of Central valley, California.

## Repository (Pipeline) Strcuture
The pipeline consists of four (04) major processes each implemented in the respective folder mentioned below inside this repo.
   - Data Query : `query_codes` folder
   - Data Processing : `data_processing_codes` folder
   - ML/DL Models : `models` folder
   - ARD Compilation : `ARD_compilation` folder

Each of these folders have multiple scripts that performs the pipelined tasked required for generating the 4km and 100m ARDs. Each scripts has detail description of the processing steps. Also, inside each folder, there is a `Discussion.ipynb` script that explains the respective folder's structure and script running sequence. 

The four major processes and script running sequence is provided below-
![image](https://github.com/mdfahimhasan/data-pipeline-env-model/assets/77580408/3eb50b7b-ac4d-405c-a74f-30cf7226a9be)


## Other Folders in Repository
The following folders in the repo consists of the listed materials
- reference_rasters : The reference rasters used throughout the improved resolution ARD development pipeline.
- shapefiles_gids : Shapefiles of ROI, ROI Buffer, and others used in the pipeline.


## Improved Resolution 4km ARD Integrated Result
The 4km Improved Resolution ARD was integrated in clustering app. It imporved resolution of the clustering app result. Two (02) major improvements were evident-
- Improved Resolution of the clustering result
- Change in clustering extent with better understanding of the testing field’s environmental types





