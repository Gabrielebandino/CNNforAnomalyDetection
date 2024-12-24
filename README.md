# Crowd Anomaly Detection Using CNNs

https://github.com/user-attachments/assets/c8e1da53-ef88-489a-bb69-1c4e7558c064



This project focuses on detecting **crowd anomalies** using a Convolutional Neural Network (CNN) applied to video frames. By analyzing the **anomaly score** for each frame, we can identify **major anomalies**, such as people running, and **micro anomalies**, such as pushing, bullying, or other subtle deviations from normal crowd behavior. These anomalies are represented in the graphs with a **threshold line** and the corresponding **anomaly score**, providing an intuitive way to visualize the results.

---

## Key Features

- **Video Frame Analysis**: Frames are extracted from videos and processed into grayscale images for model input.
- **Major and Micro Anomaly Detection**:
  - **Major Anomalies**: Obvious deviations like people running or scattering.
  - **Micro Anomalies**: Subtle deviations like pushing or bullying, detected through refined anomaly scoring.
- **Visualization**:
  - Heatmaps using **Grad-CAM** overlay highlight the areas contributing most to the detected anomalies.
  - Exported results as a **GIF** and **MP4 video** for better interpretability.
- **ROC Curve and Metrics**: Receiver Operating Characteristic (ROC) curve and AUC are computed to evaluate model performance.
- **Robustness Testing**: Model tested on unseen videos to validate its ability to generalize.

---

## Technical Workflow

1. **Dataset Preparation**:
   - Video frames are extracted and labeled as normal or anomalous.
   - Frames are resized and normalized for input to the CNN.

2. **Model Architecture**:
   - A custom CNN with two convolutional layers, max pooling, dropout, and a dense layer for binary classification.
   - **Binary Crossentropy Loss** and **Adam Optimizer** used for training.

3. **Anomaly Detection**:
   - Each video frame is scored based on the model's prediction.
   - Anomalies are identified when the score surpasses a pre-defined **threshold**.

4. **Heatmap Generation**:
   - Heatmaps are generated using **Grad-CAM** to visualize regions of interest in each frame.
   - Heatmaps are overlaid onto the original frames to create a comprehensive visualization.

5. **Validation and Results**:
   - Accuracy: ~97.62% on validation data.
   - Robustness tested on unseen video datasets.
   - Results exported as visualizations (GIF/MP4) for clear presentation.

---
