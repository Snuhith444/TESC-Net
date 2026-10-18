# TESC-Net: Tumor-aware Evidence Separation and Consistency Network

## Overview

TESC-Net is a deep learning framework for joint brain MRI tumor segmentation and four-class classification. The framework uses a shared convolutional encoder and a segmentation decoder to identify tumor regions. The predicted segmentation mask guides the separation of tumor-focused and background-focused evidence from the learned feature representations.

The resulting full-image, tumor-focused, and background-focused representations are used for classification into four categories: glioma, meningioma, no tumor, and pituitary tumor.

## Research Objectives

- Perform brain MRI tumor segmentation and four-class classification.
- Separate tumor-related features from background-related features.
- Evaluate classification performance using multiple evidence representations.
- Assess generalization using an independent external MRI dataset.

## Datasets

The datasets used in this research are available from their respective sources.

1. **BRISC 2025:** Used for internal training, validation, and testing.  
   Dataset: https://www.kaggle.com/datasets/briscdataset/brisc2025/

2. **BraTS 2021:** Used for encoder pretraining. Access is subject to the dataset provider's registration and data-access requirements.  
   Official website: https://www.med.upenn.edu/cbica/brats2021/

3. **BDNeuro-MRI:** Used for external evaluation of model generalization.  
   Dataset: https://data.mendeley.com/datasets/zwr4ntf94j

Please obtain the datasets directly from their respective providers and comply with their access conditions and usage terms. The original MRI datasets are not redistributed in this repository.

## Methodology

The TESC-Net pipeline consists of the following main stages:

1. MRI image preprocessing and normalization.
2. Encoder initialization using BraTS 2021 pretraining.
3. Hierarchical feature extraction from MRI images.
4. Tumor segmentation using a dedicated decoder.
5. Separation of full-image, tumor-focused, and background-focused evidence.
6. Projection of evidence representations into compact feature vectors.
7. Four-class classification.
8. Evaluation on BRISC 2025 and external testing on BDNeuro-MRI.

## Implementation

The implementation code is provided in this repository.

**Code file:** Replace this line with the actual filename of your uploaded code file.

Refer to the code for the implemented model architecture, preprocessing operations, training configuration, and evaluation procedure.

## Environment and Dependencies

The implementation uses Python and PyTorch. Additional libraries and their versions should be documented in `requirements.txt` after verifying the actual imports and execution environment.

Before running the code, install the required dependencies and configure the dataset paths to match your local environment. Follow the dataset providers' instructions for downloading and accessing the data.

## Reported Results

The manuscript reports the following results for TESC-Net:

- BRISC 2025, selected model variation: 98.20% classification accuracy, 98.34% Macro-F1 score, and 82.82% segmentation Dice score.
- BDNeuro-MRI external evaluation: 48.28% classification accuracy.

These results are reported as presented in the manuscript and depend on the corresponding experimental configuration.

## Reproducibility

For reproducibility, use the dataset splits, preprocessing procedures, model configuration, and evaluation protocol documented in the accompanying code and research manuscript. Consult the code for the implemented random seed and training settings.

## Citation

If you use this implementation in your research, please cite the associated research paper once its publication details are available.

**Paper title:** TESC-Net: Tumor-aware Evidence Separation and Consistency Network for Brain MRI Tumor Segmentation and Four-Class Classification.

## License

A license has not yet been specified. Please add an appropriate license after confirming that you have the right to distribute the code and selecting the terms under which others may reuse it.
