Face Recognition Attendance System
A real-time Face Recognition Attendance System built with Python, Flask, OpenCV, and face_recognition. The system detects faces through webcam, marks attendance in a CSV file, and provides a modern web interface with live updates.
📌 Features
•	Real-time face recognition using webcam
•	Attendance logging in a CSV file (with name, time, status: Present/Late)
•	Web interface with:
•	 - Company header and footer
•	 - Live camera feed
•	 - Attendance table (auto-updating)
•	 - Download CSV button
•	 - “Done” button with a success modal
•	Blue-themed UI with clean styling
⚙️ Installation
1. Clone the repository
git clone https://github.com/your-username/face-recognition-attendance.git
cd face-recognition-attendance
2. Create & activate virtual environment
Windows (cmd / PowerShell):
python -m venv faceenv
faceenv\Scripts\activate
Mac/Linux:
python3 -m venv faceenv
source faceenv/bin/activate
3. Install dependencies
pip install -r requirements.txt
📂 Project Structure
app.py                  # Main Flask app
persons/                # Folder containing employee images
    John.jpg
    Alice.png
attendance.csv          # Auto-created after first run
requirements.txt        # Python dependencies
templates/
    index.html          # Frontend HTML
static/
    css/
        style.css       # Custom styling
    js/
        script.js       # Frontend logic
🧑‍🤝‍🧑 Adding Employees
Place employee images in the persons/ folder.
Important: Name each image as the employee’s real name.
Example:
 - John Smith.jpg → will appear as JOHN SMITH in camera feed and CSV
 - Alice.png → will appear as ALICE

⚠️ Only one clear image per person is recommended for best results.
▶️ Running the App
After setup:
python app.py

Open your browser and go to: http://127.0.0.1:5000/
Press q in the camera window or click Done button on the webpage to stop.
📊 Attendance Output
Attendance is stored in attendance.csv automatically.
Each row contains:

Name | Time | Status
---- | ---- | ------
JOHN SMITH | 09:02 AM | Present
ALICE | 09:15 AM | Late
🚀 Future Improvements
•	Database support (MySQL / MongoDB)
•	Admin dashboard with login
•	Export to Excel with charts
•	Multi-camera support
💡 Tech Stack
•	Python (Flask, OpenCV, face_recognition, NumPy, Pandas)
•	Frontend (HTML, CSS, JavaScript)
