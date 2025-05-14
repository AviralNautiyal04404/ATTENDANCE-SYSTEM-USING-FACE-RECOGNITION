Attendance Marking System using Face Recognition
This project implements a real-time Face Recognition based Attendance System using OpenCV's Deep Neural Network (DNN) module. It uses a CNN model to recognize faces and logs attendance into a CSV file with timestamps.

🔧 Features
🎥 Real-time face detection using OpenCV DNN

🧠 Face recognition using a trained CNN model

📷 Image capture and dataset creation

🏷️ Register new students with their images

🧠 Retrain CNN model on new data (Real-time retraining)

📝 Attendance logging with timestamps in CSV

🖥️ GUI Interface using tkinter

📦 Converts to .exe for standalone usage

📁 Project Structure
bash
Copy
Edit
Attendance-System/
│
├── dataset/                    # Captured face images of students (subfolder per student)
├── model/
│   └── cnn_face_recog.h5       # Trained CNN model
│
├── deploy.prototxt             # DNN model architecture file (Caffe format)
├── res10_300x300_ssd_iter_140000.caffemodel  # DNN pretrained weights
│
├── attendance.csv              # Output attendance log
├── main.py                     # Main application (GUI + logic)
├── train_model.py              # CNN training script
├── requirements.txt            # All required Python dependencies
└── README.md                   # This file
💻 Requirements
Install the following dependencies using pip or conda:

bash
Copy
Edit
pip install opencv-python numpy keras tensorflow pandas pillow
OR with conda:

bash
Copy
Edit
conda install -c conda-forge opencv numpy keras tensorflow pandas pillow
🚀 How to Run
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/AviralNautiyal04404/attendance-system-face-recognition.git
cd attendance-system-face-recognition
2. Add Required Model Files
Place these in your D:/PROJECT/ directory (or update paths in the script):

deploy.prototxt

res10_300x300_ssd_iter_140000.caffemodel

You can download them from OpenCV GitHub:

deploy.prototxt

res10_300x300_ssd_iter_140000.caffemodel

3. Run the App
bash
Copy
Edit
python main.py
4. Register a New Student
Click Register Student, enter the name.

Capture images using your webcam.

Images will be saved under dataset/<student_name>/.

5. Train the CNN Model
bash
Copy
Edit
python train_model.py
It will save the trained model as cnn_face_recog.KERAS inside model/.

6. Start Attendance
Click the Start Attendance button in the GUI.

Detected and recognized students will be logged in attendance.csv.

📦 Optional: Convert to .exe
To create a standalone executable:

bash
Copy
Edit
pip install pyinstaller
pyinstaller --onefile --windowed main.py
Your .exe will be in the dist/ folder.
