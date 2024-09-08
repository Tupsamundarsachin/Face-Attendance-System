# face-attendance-system

The Face Attendance System is a computer vision-based application that detects and recognizes faces, then logs attendance automatically. If an unregistered user tries to log in, the system identifies the person as "unknown" and prompts for registration.

![face](https://github.com/user-attachments/assets/59221159-ffd9-4c6c-afa4-d6e382cba240)

## Dataset

Dataset used in this project is available on https://drive.google.com/drive/folders/1TnpUibuaSFFfT_Vps6wm082HoIHh2lby?usp=sharing


## Features

1) Face Detection and Recognition: Detects faces from a live webcam feed and matches them with registered users.
2) Automatic Attendance Logging: Logs the attendance of recognized users with timestamps.
3) New User Registration: Allows the registration of new users by capturing their facial data and storing it in a database.
4) Real-time Processing: Continuously processes webcam feed for immediate user recognition and feedback.

## Requirements

    cmake==3.17.2
    dlib==19.18.0
    opencv-python==4.6.0.66
    Pillow==9.2.0
    face_recognition==1.3.0


## Installation
Clone the repository:

     git clone https://github.com/Tupsamundarsachin/face-attendance-system.git
     cd face-attendance-system


## Create a virtual environment and activate it:
     python3 -m venv venv
     source venv/bin/activate



## Install the required dependencies:

for Linux

     pip install -r requirements.txt

for Windows

    pip install -r requirements_windows.txt

## Run the Application:
     python main.py
     
## Login:

Press the "Login" button on the main window.
The system captures the current webcam feed, checks for a face match in the database, and logs the attendance if the user is recognized.
If the user is not recognized, the system prompts for new user registration.



## Register a New User:

Click the "Register New User" button.
Enter the username in the prompted window and capture the image.
The system will save the facial data and associate it with the provided username.
Project Structure
main.py: The main application script, handling the GUI, webcam feed, user login, and registration.
util.py: Contains utility functions for the application, such as button creation, image processing, etc.
db/: Directory where user face encodings are stored.
log.txt: Attendance log file that stores login timestamps of users.


## How It Works

    a) Face Detection: Uses the face_recognition library to detect faces in the webcam feed.
    b) Face Recognition: Compares detected faces with stored encodings in the database to identify users.
    c) Database: Stores user face encodings in a .pickle file for quick lookup during recognition.





