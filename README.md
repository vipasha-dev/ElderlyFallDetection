Human Pose Classification for Elderly Fall Detection using MediaPipe and XGBoost
This project demonstrates a robust pipeline for human pose classification. It uses MediaPipe to detect 33 body keypoints from images, extracts this data into a CSV file, and then trains a powerful XGBoost classifier to predict different poses or actions based on the keypoint data.

Features
Keypoint Detection: Utilizes MediaPipe's state-of-the-art pose estimation to accurately detect 33 body landmarks (x, y, z coordinates).

Data Preparation: Automatically processes a folder of images, extracts keypoints, and saves them to a structured CSV file for machine learning.

Model Training: Trains two XGBoost models to classify poses based on both a numeric class ID (class_no) and a class name (class_name).

Inference: Provides a script to load the trained models and predict the pose for a new, single image.

Visualization: Includes a utility to visualize the detected keypoints and skeletal connections on an image.

Prerequisites
You'll need Python 3.6 or newer. The following libraries are required:

mediapipe: For body keypoint detection.

opencv-contrib-python: For image processing and display.

pandas: For data manipulation and CSV handling.

xgboost: The core machine learning model for classification.

scikit-learn: For data splitting and evaluation metrics.

joblib: For saving and loading the trained models.

Installation
You can install all the necessary libraries using pip.

Usage
The project workflow is divided into three main steps: data extraction, model training, and prediction/visualization.

1. Extracting Keypoints from a Folder of Images
First, use the provided script to process a dataset of images and store their keypoints in a CSV file. This script will create a CSV file containing all the keypoint coordinates for each image in your specified folder.

2. Training the Classification Models
Once you have your keypoints_dataset.csv (which should include class_name and class_no columns), you can train the XGBoost models. After running this script, you will have two trained models saved as model_class_no.pkl and model_class_name.pkl.

3. Making Predictions and Visualizing Results
To test the trained models on a new image and see the results, you'll first extract the keypoints from a single image into a CSV file. Then, use that keypoint data to predict the pose class. Finally, you can use the visualization script to see the detected landmarks drawn on the new image.

Acknowledgments
MediaPipe: The robust framework for pose estimation.

XGBoost: The highly efficient gradient boosting library.
