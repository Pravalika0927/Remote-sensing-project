# Land Cover Classification of the Australian Bushlands (2019–2020 Bushfires)

**Author:** Pravalika Ravula  
**Course:** GEOG711 – Remote Sensing  
**Instructor:** Prof. Leonhard Blesius  
**Term:** Spring 2023

## Project Overview

This project investigates the land cover changes in the bushlands of southeastern Australia before and after the catastrophic bushfires that occurred between **September 2019 and March 2020**. Using **Landsat 8/9 satellite imagery**, the analysis applies **Object-Based Image Analysis (OBIA)** techniques in **eCognition** to classify land cover types and quantify fire damage across various ecological zones.

## Study Area

The area of interest spans across **East Gippsland, Victoria**, including:
- **Coopracambra**, **Errinundra**, **Croajingolong**, and **Point Hicks Marine National Parks**
- Regions such as **Mallacoota**, **Tamboon**, **Chandlers Creek**, **Wallagaraugh River**, and parts of **New South Wales' Nadgee and Timbillica**

These regions host significant biodiversity and ecosystems that were severely affected by the fires.

## Data Sources

- **Satellite Imagery:** Landsat 8/9 (USGS Earth Explorer)  
  - **Pre-fire:** May 21, 2019  
  - **Post-fire:** June 8, 2020  
- **Bands used:** Blue, Green, Red, NIR, SWIR1, SWIR2

## Methodology

### Pre-processing
- Image stacking and subsetting using **ERDAS Imagine**

### Image Segmentation
- **Multi-Resolution Segmentation** with scale parameter: `160`

### Feature Extraction
- **NDVI (Normalized Difference Vegetation Index)** for vegetation health
- **NBR (Normalized Burn Ratio)** for detecting burn severity

### Classification
- Land cover types (Vegetation, Water, Burned Area) classified using eCognition's **Assign Class** algorithm
- Conditional thresholds:
  - **Vegetation:** `NDVI > 0.15`
  - **Water:** `NIR < 7500`
  - **Burned Area:** `NBR < 0.08`

## Results

- Clear differentiation between **burned** and **unburned** areas
- High classification accuracy using OBIA methods
- Some **unclassified pixels** due to shadows or spectral similarity

## Key Insights

- Burned areas were effectively identified and visualized
- eCognition proved robust for complex landscape classification
- Supports **post-disaster assessment**, **habitat restoration**, and **ecological management**

## Few References

- Polychronaki & Gitas (2012) – Burned Area Mapping in Greece using OBIA  
- Hay & Castilla (2006) – SWOT Analysis of OBIA  
- Various peer-reviewed articles on the 2019–2020 Australian bushfires and OBIA applications  
