# Retinal Disease Classification Using Pretrained CNN Models

## Overview
This repository contains the code and methodology for the classification of retinal diseases such as **Diabetic Macular Edema (DME)**, **Drusen Macular Degeneration (DMD)**, and **Choroidal Neovascularization (CNV)** using Convolutional Neural Networks (CNN) and Spectral Domain (SD) Optical Coherence Tomography (OCT) images.

The aim of this research is to develop a fast and accurate diagnosis system for retinal diseases using **Computer-Aided Diagnosis (CAD)**, providing doctors and medical practitioners with a reliable diagnostic tool.

## Problem Statement
Retinal diseases like DME, DMD, and CNV exhibit similar patterns in OCT images, making classification difficult. Challenges include:

- **Noise in OCT images** obscuring retinal characteristics.
- **Data preprocessing complexity**, requiring proper denoising, augmentation, and filtering.
- **Large dataset** size, leading to high computational costs and risks of overfitting.
- **Training CNN models** like ResNet50, InceptionV3, and DenseNet121, which are resource-intensive.

## Key Features
1. **Preprocessing Pipeline**: 
   - Applied noise reduction techniques (Median/Wiener filters), gamma correction, resizing (224x224).
   - Augmentation: rotation, cropping, flipping, translation.
   
2. **CNN Models**:
   - Pre-trained models: ResNet50, InceptionV3, DenseNet121.
   - Fine-tuned and adjusted for retinal disease classification.
   - **Ensemble model** combining ResNet50 and InceptionV3 for improved accuracy.

3. **Evaluation Metrics**:
   - Accuracy, Precision, Recall, F1-Score.
   - Confusion matrix to analyze model predictions.

## Dataset
- **OCT images** from patients with normal retinas, DME, DMD, and CNV.
- **Source**: [UCSD OCT Dataset](https://data.mendeley.com/datasets/rscbjbr9sj/3) (Kermany et al., 2018).
- **Training & Testing Split**: K-fold cross-validation with subsampling (5,415 and 10,830 images).

## Results
- The **ensemble model** achieved **94.6% accuracy**, outperforming individual models.
- Speckle noise reduction combined with augmentation improved the overall model performance.

## Research Stages
1. **Literature Study**: Gathered information on CNN, preprocessing techniques, transfer learning, and performance metrics.
2. **Data Collection and Preprocessing**: 
   - Filtered OCT images using speckle denoising.
   - Tested and selected the best filter combination (Median + Wiener).
3. **Model Training**:
   - Fine-tuned pre-trained models for retinal disease classification.
   - Used 3-fold cross-validation for reliable performance.
4. **Evaluation**:
   - Evaluated using metrics: accuracy, precision, recall, and F1-Score.
   - Tested models on a hold-out testing dataset.
5. **Report**: Final report includes a comparison of the models’ performance.

## Conclusion
This research demonstrates the effectiveness of ensemble models in improving the classification accuracy of retinal diseases using OCT images. By implementing a robust preprocessing pipeline and fine-tuning pre-trained models, we improved classification results compared to previous research. This system can serve as a reliable tool for aiding in the early detection of retinal diseases.

## Acknowledgements
- **UCSD OCT Dataset** (Kermany et al., 2018) for providing OCT image data.
- Research contributions from **Kim & Tran (2021)**, **Rajagopalan et al. (2020)**, and others in the field of retinal disease classification.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
