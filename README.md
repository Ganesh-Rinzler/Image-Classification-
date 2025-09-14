# Airplanes, Motorbikes & Schooners – Transfer Learning & Fine-Tuning

This project classifies images of **airplanes**, **motorbikes**, and **schooners** using three powerful pre-trained CNN models to achieve high accuracy with efficient training.

## Features
- **Transfer Learning**  
  Custom classifier heads with Batch Normalization and Dropout layers adapted for each model:  
  - **Xception**: 25 % dropout  
  - **ResNet101V2**: 35 % dropout  
  - **InceptionResNetV2**: 15 % dropout  
  Best models saved automatically via callbacks during 10-epoch training.

- **Fine-Tuning**  
  Gradual unfreezing of layers for deeper training:  
  - **Xception**: top 75 % of layers trainable  
  - **ResNet101V2**: top 65 % of layers trainable  
  - **InceptionResNetV2**: all layers trainable  
  Fine-tuned for 10 additional epochs using the best transfer-learning weights.

- **Dataset Preparation**  
  Images split into **75 % training** and **25 % testing**, with resizing, normalization, and augmentation.

- **Performance Evaluation**  
  Each fine-tuned model is assessed using:
  - **Confusion Matrix**
  - **Precision, Recall, and F1-Score**

