# 👁️‍🗨️ Face Recognition-Based Attendance System

This is a real-time Python-based face recognition attendance system. It uses OpenCV for face detection and a K-Nearest Neighbors (KNN) model to recognize and record attendance. Names and facial data are stored securely using Python's `pickle` module. CSV files are generated to log timestamped attendance. A custom UI with background and voice output is also included for enhanced experience.

---

## 🧠 Features

- 📷 Real-time face detection using Haar Cascades
- 🔍 Face recognition using K-Nearest Neighbors (KNN)
- ✍️ Face data storage using Python pickle
- 📅 Attendance recorded in daily CSV logs
- 🖼️ Optional background UI with custom frame embedding

---

## 📁 Project Structure

face-attendance-system/
│
├── data/
│ ├── haarcascade_frontalface_default.xml
│ ├── names.pkl
│ └── faces_data.pkl
│
├── Attendance/
│ └── Attendance_<DD-MM-YYYY>.csv #created while taking attendance
│
├── add_faces.py # Script to capture and save face data
├── test.py # Script to recognize faces and record attendance
├── background.png # Background image for display
└── README.md # Project documentation

## 🛠️ Requirements
Install the required libraries using pip:

    pip install opencv-python numpy scikit-learn pywin32

## 🚀 How to Use
Step 1: Add New User Faces
Run the face capture script:

    python add_faces.py
Enter your name when prompted.
It will collect and store 100 face images.

These are stored in faces_data.pkl and associated with your name in names.pkl.

Step 2: Run the Attendance System

    python test.py
The system will start real-time webcam feed and face recognition.

On face detection and identification:

Press a to take attendance

Press q to quit

Step 3:Output
A CSV file is created in the Attendance/ folder with:

User's name

Time of attendance

## Sample Output

Enter Your Name: <name>

100 face samples captured and saved.

Shape of Faces matrix --> (300, 7500)

[During recognition]
Attendance Taken..
CSV saved to: Attendance/Attendance_19-06-2025.csv
## Technologies Used
Face Detection: OpenCV + Haar Cascade Classifier

Face Recognition: KNN Classifier (scikit-learn)

Storage: pickle for storing face arrays and names

UI Customization: Streamlit
