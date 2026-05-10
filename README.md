# VisionAIHackathon - Hot Desk Optimization

## Project Overview
This hackathon project is designed to optimize hot desk utilization by detecting employee presence in video footage. The system checks each frame in the video to determine if an employee exists at a particular desk.

## Features
- **Employee Detection**: Analyzes video frames to detect if an employee is present at a desk
- **Frame-by-Frame Analysis**: Processes each frame in the video to provide comprehensive coverage
- **Model Training**: Utilized Roboflow for training the detection model with optimal accuracy

## How It Works
1. **Video Input**: Takes video footage of desks as input
2. **Frame Processing**: Checks each frame individually for employee presence
3. **Detection**: Uses the trained model to identify whether an employee exists in each frame
4. **Output**: Generates results showing employee presence patterns over time

## Training & Model
- **Training Platform**: Roboflow
- **Model Type**: Object detection model trained to identify employees at desks
- **Data Processing**: Video frames extracted and processed for model training

## Technical Stack
- **Deep Learning Framework**: YOLOv8 (Ultralytics)
- **Object Detection**: Real-time employee detection in video frames
- **Tracking**: ByteTrack for multi-object tracking
- **GPU Acceleration**: NVIDIA GPU support for faster inference
- **Dataset Management**: Roboflow for data hosting and annotation

## Implementation Workflow

### 1. Setup & Installation
- GPU validation using `nvidia-smi`
- Installation of Ultralytics and Roboflow libraries

### 2. Dataset Preparation
- Download employee surveillance dataset from Roboflow
- Dataset includes annotated images with "cabin" (employee) labels
- Data split into training, validation, and test sets

### 3. Model Training
- **Base Model**: YOLOv8s (small variant for balance between speed and accuracy)
- **Training Parameters**: 
  - 70 epochs
  - Image size: 600x600
  - Generates performance plots
- **Output**: Best performing model weights saved

### 4. Model Validation
- Validation against the test dataset
- Performance metrics calculation

### 5. Inference & Detection
- **Frame-by-Frame Analysis**: Processes video frame by frame
- **Employee Detection**: Identifies and detects employees in each frame
- **Real-time Tracking**: Uses ByteTrack to maintain consistent employee IDs across frames
- **Analytics**: Tracks visible employees at 5-second intervals
- **Output**: Annotated video with bounding boxes and employee detection

### 6. Output Generation
- Generates predicted video with detection bounding boxes
- Saves annotation results
- Produces timeline showing employee presence throughout the video

## Project Structure
- `HotDeskOptimisationTrail1.ipynb`: Main Jupyter notebook containing the complete implementation
- `RawVideo/`: Directory containing input video files for processing
- `OutputVideo/`: Directory containing processed output videos with detection annotations