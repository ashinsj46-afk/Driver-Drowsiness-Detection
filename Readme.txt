# Drowsiness Detection System

## Overview
The Drowsiness Detection System is a real-time application that monitors driver fatigue using computer vision and machine learning techniques. It captures video frames from a webcam, analyzes facial features, and triggers alerts when drowsiness is detected.

## Prerequisites
Before running the project, ensure you have the following installed on your system:

### Hardware Requirements:
- Laptop or PC with an integrated or external webcam
- Minimum 8GB RAM for smooth performance
- Intel Core i5 (10th Gen) or equivalent processor

### Software Requirements:
- Windows 10 or later / Linux (Ubuntu recommended) / macOS
- Python 3.8 or later
- Required Python libraries (listed below)

## Installation Steps

### 1. Install Python
Ensure you have Python installed. You can check the installed version using:
```bash
python --version
```
If Python is not installed, download and install it from [Python's official website](https://www.python.org/downloads/).

### 2. Install Required Libraries
Use the following command to install the necessary dependencies:
```bash
pip install opencv-python numpy dlib imutils scipy pygame twilio matplotlib pandas scikit-learn
```

### 3. Setting Up the Project
- Place all the project files in a dedicated directory.
- Ensure the dataset files are correctly stored in the appropriate folder (if applicable).

### 4. Running the Application
To start the drowsiness detection system, navigate to the project directory and execute:
```bash
python drowsiness_detection.py
```
This will activate the webcam and start real-time monitoring.

### 5. Understanding the Output
- If drowsiness is detected, an **alarm sound** will be triggered.
- A **WhatsApp alert** will be sent to the registered emergency contact.
- The Tkinter-based GUI will display real-time detection results.

## Configuration
### 1. Adjusting Sensitivity
You can fine-tune the drowsiness detection sensitivity by modifying the **Eye Aspect Ratio (EAR) threshold** in the code.
```python
EAR_THRESHOLD = 0.25  # Adjust based on testing
```

### 2. Twilio WhatsApp Alert Setup
If you wish to receive WhatsApp notifications, update the Twilio credentials in the code:
```python
TWILIO_ACCOUNT_SID = 'your_account_sid'
TWILIO_AUTH_TOKEN = 'your_auth_token'
TO_WHATSAPP_NUMBER = 'whatsapp:+recipient_number'
FROM_WHATSAPP_NUMBER = 'whatsapp:+twilio_number'
```

## Troubleshooting
- If the webcam feed is not displaying, ensure no other applications are using the camera.
- If dependencies fail to install, try running:
```bash
pip install --upgrade pip
```
followed by:
```bash
pip install -r requirements.txt
```
- If WhatsApp alerts are not being sent, verify your Twilio account settings.

## Future Enhancements
- Integration with vehicle systems for automated intervention.
- Deep learning-based improvements for more accurate detection.
- Support for mobile applications for real-time monitoring.

## Credits
Developed as part of the **B.Tech AI & ML** curriculum for real-time driver monitoring and safety enhancement.

---
For any issues or improvements, feel free to contribute or report bugs!

