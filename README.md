# Optical-Based Self-Attention Dynamic Frame Detection (SADFFD) Network
#Introduction
Welcome to the repository for the Optical-Based Self-Attention Dynamic Frame Detection (SADFFD) Network. This project implements a novel deepfake detection system using a combination of optical flow and self-attention mechanisms. Our approach is designed to identify both spatial and temporal inconsistencies common in deepfake videos.

## Abstract
Deepfake videos manipulate faces in videos to create fake content, posing significant challenges. To address this, we developed the SADFFD Network. Our method utilizes optical flow to capture movement between video frames and self-attention mechanisms to detect inconsistencies. The system is tested on UADFV and Celeb-DF V1 datasets, showing high accuracy in identifying fake videos.

## Approach
Our method involves the following steps:

1.**Data Preprocessing:**
[U+25CB] Detect faces in video frames using Haar cascades.
[U+25CB] Crop and resize faces to 224x224 pixels.
[U+25CB] Convert frames to grayscale.
[U+25CB] Calculate optical flow between frames.
[U+25CB] Save optical flow fields as .npy files. 

(![Screenshot 2024-10-21 004438](https://github.com/user-attachments/assets/81b01840-db7e-4b24-876f-0eb46f0b4a7c))
## 2.Model Architecture:

[U+25CB] **Upper Branch:** Extracts basic spatial features using convolution and MBConv blocks.
[U+25CB] **Lower Branch:** Uses self-attention mechanisms to focus on crucial facial areas.
Concatenation of features from both branches.
Global Average Pooling (GAP) and classification using an activation function.
# Datasets
We evaluated our model on two datasets:

(U+25CF) **UADFV Dataset:** Includes 49 real and 49 fake videos created using FaceSwap.
(U+25CF) **Celeb-DF V1 Dataset:** Contains 158 real and 795 fake videos created using advanced GAN-based techniques.
## Results
Our model achieved the following results:

(U+25CF) **Celeb-DF V1 Dataset:**
[U+25CB] Accuracy: 79.88%
[U+25CB] Precision: 90%
[U+25CB] Recall: 76%
(U+25CF) **UADFV Dataset:**
[U+25CB] Accuracy: 85.26%
[U+25CB] Precision: 95%
[U+25CB] Recall: 76%
## Conclusion
The SADFFD Network is a robust tool for deepfake detection, capable of capturing temporal inconsistencies and spatial deviations. Future work includes refining the model, expanding the datasets, and integrating the system into real-time applications.
