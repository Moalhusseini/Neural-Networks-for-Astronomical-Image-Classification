# Neural Networks for Astronomical Image Classification

## Overview

This project explores astronomical object classification using images from the Sloan Digital Sky Survey (SDSS). It compares traditional machine learning models with a Convolutional Neural Network (CNN) to classify objects into three categories: galaxies, quasars, and stars.

## Objectives

- Explore and prepare an astronomical image dataset.
- Extract RGB statistical features from images.
- Train and evaluate traditional machine learning models.
- Develop a CNN for direct image classification.
- Compare model performance using multiple evaluation metrics.

## Dataset

- **Source:** Sloan Digital Sky Survey (SDSS)
- **Total images:** 5,100
- **Classes:** GALAXY, QSO, STAR
- **Samples per class:** 1,700
- **CNN input size:** 96 × 96 RGB pixels
- **Data split:** 80% development and 20% testing, using stratified sampling

Official data source: https://www.sdss.org/

## Methodology

1. Data acquisition and validation.
2. Exploratory data analysis and sky-coordinate visualization.
3. RGB feature extraction using channel statistics and color histograms.
4. Training Random Forest and XGBoost models.
5. Training a Convolutional Neural Network on RGB images.
6. Evaluation and comparison using accuracy, macro F1-score, and macro ROC-AUC.

## Results

| Model | Test Accuracy | Macro F1-score | Macro ROC-AUC |
|---|---:|---:|---:|
| Random Forest | 65.78% | 65.97% | 0.8312 |
| XGBoost | 66.37% | 66.59% | 0.8347 |
| CNN | 79.90% | 79.67% | 0.9198 |

The CNN achieved the highest test performance among the three evaluated models. These results describe the selected dataset and experimental setup; further testing on independent data would be needed to assess generalization.

## Repository Contents

- `Neural_Networks_for_Astronomical_Image_Classification.ipynb` — the main notebook containing the analysis, implementation, visualizations, and model evaluation.

## Limitations

The traditional machine learning models use summary statistics and RGB histograms rather than the full spatial structure of the images. Model performance may also depend on the selected sample, preprocessing steps, and experimental configuration.

## References

- Sloan Digital Sky Survey (SDSS): https://www.sdss.org/
- Banerji, M., et al. (2010). *Galaxy Zoo: Reproducing galaxy morphologies via machine learning*. Monthly Notices of the Royal Astronomical Society, 406(1), 342–353. https://doi.org/10.1111/j.1365-2966.2010.16713.x

## Project Status

Completed — academic project and comparative model evaluation.
