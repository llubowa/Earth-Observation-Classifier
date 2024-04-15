# Earth-Observation-Classifier
Welcome to Earth Observation Classifier, a project focused on land use and land cover classification using machine learning techniques applied to satellite imagery.
Sure, here's a README file you can share on GitHub:

---

# Land Use and Land Cover Classification

## Overview
This project aims to classify land use and land cover (LULC) categories using machine learning techniques applied to satellite imagery. By leveraging the EuroSAT dataset, the project systematically categorizes landscapes into various land cover types, facilitating environmental monitoring, urban planning, and agricultural management.

## Data
The project utilizes the EuroSAT dataset, derived from Sentinel-2 satellite imagery. EuroSAT contains 27,000 labeled and geo-referenced images across 10 LULC classes, providing rich information about Earth's surface. Two versions are available: EuroSAT_RGB.zip includes RGB-encoded JPEG images, while EuroSAT_MS.zip contains multi-spectral data with 13 Sentinel-2 bands.

## Data Processing
We process the EuroSAT_MS.zip dataset by iterating through class folders, extracting spectral bands from .tif files using rasterio. Each class folder represents a distinct LULC category. We construct a Pandas DataFrame for model training, with rows representing image samples and columns representing spectral bands and target labels.

## Machine Learning Approach
The categorical target column is encoded numerically using LabelEncoder. The dataset is split into training (80%) and testing (20%) subsets. We employ a Random Forest Classifier to learn spectral features from satellite imagery. The model achieves an accuracy score of 82.04% on the test set, demonstrating its effectiveness in classifying LULC categories.

## Model Deployment
The entire workflow, from data processing to model training and evaluation, is documented in the provided notebook. The trained model can be deployed for real-world applications such as automated land use and cover classification, facilitating environmental monitoring, urban planning, and agricultural management.

## References
- EuroSAT Dataset: [Zenodo](https://zenodo.org/records/7711810)
