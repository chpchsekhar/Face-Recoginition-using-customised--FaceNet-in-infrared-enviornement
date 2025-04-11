[![forthebadge](https://forthebadge.com/images/badges/made-with-python.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/uses-machine-learning.svg)](https://forthebadge.com)

# Real-time Face Recognition Using FaceNet on TensorFlow 2.X

A robust real-time facial recognition system using the pretrained FaceNet model and MTCNN for face detection.

![Demo](MEDIA/gif.gif)

## Table of Contents
- [Features](#features)
- [Quick Start](#quick-start)
- [Detailed Usage](#detailed-usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [Troubleshooting](#troubleshooting)
- [Credits](#credits)

## Features
- Real-time face detection and recognition
- Support for multiple faces in the same frame
- Easy addition of new faces to the recognition system
- Works with TensorFlow 2.X
- Pre-trained weights available for quick setup

## Quick Start

1. Clone this repository
2. Download pre-trained weights from [here](https://drive.google.com/drive/folders/1scGoVCQp-cNwKTKOUqevCP1N2LlyXU3l?usp=sharing) and place in project root
3. Add your face images:
   ```bash
   mkdir Faces/YourName
   # Add 2-3 clear photos of your face to this directory
   ```
4. Train the system:
   ```bash
   python train_v2.py
   ```
5. Run real-time recognition:
   ```bash
   python detect.py
   ```

## Detailed Usage

### Training
- The system requires at least 2-3 images per person for effective recognition
- Images should be clear, well-lit, and show the face from different angles
- Training will generate encodings in `encodings/encodings.pkl`

### Detection
- Press 'q' to quit the real-time detection
- The system shows confidence scores for recognized faces
- Unknown faces will be labeled as "Unknown"

## Project Structure
```
Face-recognition-Using-Facenet-On-Tensorflow-2.X/
├── architecture.py       # FaceNet model architecture for TF 2.X
├── detect.py             # Real-time face detection script
├── train_v2.py           # Training script
├── Custo_face_net_1.ipynb # Jupyter notebook with custom implementation
├── facenet_keras_weights.h5 # Pretrained weights
├── LICENSE
├── README.md
├── encodings/
│   └── encodings.pkl     # Saved face encodings
├── Faces/                # Training images
│   ├── Person1/
│   ├── Person2/
│   └── .../
└── MEDIA/
    └── gif.gif           # Demo gif
```

## Dependencies
```
TensorFlow 2.3.0+
numpy
opencv-python
mtcnn
scikit-learn
scipy
```

Install with:
```bash
pip install -r requirements.txt
```

## Troubleshooting
- If you get shape mismatch errors, ensure you're using the correct pretrained weights
- For performance issues, try reducing the input resolution in detect.py
- Make sure all face images are properly aligned and visible

## Credits
- Original FaceNet paper: [FaceNet: A Unified Embedding for Face Recognition and Clustering](https://arxiv.org/abs/1503.03832)
- Inspired by: [Practical-AI/Face](https://github.com/Practical-AI/Face)
- Detailed explanation: [Face Recognition with FaceNet and MTCNN](https://arsfutura.com/magazine/face-recognition-with-facenet-and-mtcnn/)

![visitors](https://visitor-badge.glitch.me/badge?page_id=page.https://github.com/R4j4n/Face-recognition-Using-Facenet-On-Tensorflow-2.X)
