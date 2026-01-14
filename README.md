# PosePal 🧘‍♀️

**PosePal** is a web-based yoga pose classification system that uses a Convolutional Neural Network (CNN) to identify yoga poses from live webcam input. The project applies deep learning to human posture recognition and integrates the trained model into a lightweight, real-time web application.

## Problem Statement
Correct yoga posture is essential for safe and effective practice. This project classifies yoga poses from live webcam input to help users identify the pose they are performing.

## Machine Learning Approach
- **Task:** Supervised multi-class image classification  
- **Input:** RGB video frame from webcam (300 × 300)  
- **Output:** Yoga pose class  

Each webcam frame is processed independently and passed to the CNN for classification.

## Dataset
- Image-based yoga pose dataset with folder-based class labeling  
- **Classes:** Mountain, Downward Dog, Tree, Warrior I, Warrior II, Goddess  

## Data Preprocessing
- Resize to 300 × 300  
- Pixel normalization to [0, 1]  
- Training-time data augmentation: rotation, zoom, shear, horizontal flip  

## Model Architecture
- Custom CNN with convolution + max pooling layers  
- Fully connected dense layers  
- Softmax output for multi-class classification  

## Training Details
- Optimizer: Adam  
- Loss: Categorical Crossentropy  
- Batch size: 8  
- Metric: Accuracy  

> **Note:** The notebook used for model training is **not included**, as the model was trained using an external source. Only the trained model is included in this repository.

## Webcam Inference
- Captures live video frames from the user’s webcam  
- Each frame is resized and normalized  
- CNN predicts the yoga pose for each frame  
- Predictions are smoothed over the last several frames to reduce flicker  
- Predicted pose is updated in real time on the web interface  

## Limitations & Future Improvements
**Limitations:**  
- Frame-by-frame prediction can be noisy  
- Visually similar poses may be confused  
- No explicit joint or keypoint modeling  

**Future Improvements:**  
- Pose keypoint–based methods (e.g., MediaPipe)  
- Temporal smoothing across frames  
- Video-based pose analysis  
- Real-time posture feedback  

## Live Demo
Check out PosePal in action here: **[[https://swatiaggrawal.github.io/PosePal/](https://swatiaggrawal.github.io/PosePal/)]**
