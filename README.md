# Face Recognition using OpenCV and KNN

This project implements real-time face recognition using OpenCV and the K-Nearest Neighbors (KNN) algorithm. It consists of two main parts:
1. **Face Data Collection:** Capturing images from the webcam, detecting faces, and saving them as numpy arrays for training.
2. **Face Recognition:** Using a trained KNN classifier to recognize faces from a live video stream.

## Features
- Detect faces using OpenCV's Haarcascade classifier.
- Collect and store face data for multiple users.
- Recognize and label faces in real time using KNN.
- Display the detected faces with bounding boxes and names.

## Installation
Ensure you have Python and the required libraries installed.

### Prerequisites
Install the necessary dependencies using pip:
```bash
pip install numpy opencv-python
```

## Usage

### 1. Face Data Collection
Run the script to capture images and store face data:
```bash
python face_data_collection.py
```
- Enter your name when prompted.
- The script will detect and save your face images as numpy arrays in the `data/` directory.
- Press `a` to stop capturing.

### 2. Face Recognition
Run the face recognition script:
```bash
python face_recognition.py
```
- The script will load the stored face data and use KNN to classify faces in real time.
- Detected faces will be labeled with names.
- Press `a` to exit.

## Project Structure
```
├── data/                 # Directory to store face data (numpy arrays)
├── haarcascade_frontalface_alt.xml # Haarcascade file for face detection
├── face_data_collection.py  # Script to collect and store face data
├── face_recognition.py      # Script to recognize faces using KNN
├── README.md               # Project documentation
```

## Implementation Details
### Face Detection
- Uses OpenCV's `haarcascade_frontalface_alt.xml` for face detection.
- Captures face regions and resizes them to `100x100` pixels.
- Saves face data as `.npy` files.

### Face Recognition using KNN
- Loads the stored face data and labels.
- Computes Euclidean distances for classification.
- Maps predicted labels to corresponding user names.
- Displays the recognized faces in a live video feed.

## Future Improvements
- Improve face recognition accuracy with deep learning models like CNN.
- Implement a GUI for better user interaction.
- Store data in a database instead of numpy arrays.

## Contributing
Feel free to contribute to this project by improving the face recognition accuracy or adding new features.

## License
This project is licensed under the MIT License.

