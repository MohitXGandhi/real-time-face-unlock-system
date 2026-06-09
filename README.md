#  Real-Time Face Unlock System

A real-time face recognition based authentication system built as a Final Year BTech CSE (Data Science & AIML) project.

---

##  Project Overview

This system uses computer vision and deep learning to recognize faces in real time using a webcam. It supports multi-user registration, authentication using face recognition, and maintains access logs with timestamps.

---

##  Features

-  **Face Registration** — Register multiple users via webcam
-  **Real-Time Face Unlock** — Recognize faces instantly using webcam
-  **Confidence Score** — Shows match confidence percentage for each recognition
-  **Multiple User Support** — Register and manage multiple faces
-  **Access Logs** — Every unlock attempt is saved with timestamp to CSV
-  **Delete Users** — Remove registered users from the system
-  **Clean Menu Interface** — Easy to use terminal-based menu

---

##  Tech Stack

| Technology | Purpose |
|------------|---------|
| Python 3.11 | Core programming language |
| OpenCV | Webcam access and video processing |
| face_recognition | Face detection and encoding |
| dlib | Deep learning face recognition models |
| NumPy | Array and image processing |
| Pickle | Saving and loading face encodings |
| CSV | Access log storage |

---

##  Project Structure
```
Face_unlock_system/
│
├── src/
│   ├── main.py
│   ├── register_face.py
│   └── unlock.py
│
├── data/
│   └── access_log.csv
│
├── models/
│   └── faces.pkl
│
├── requirements.txt
└── README.md
```

---

##  Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/MohitXGandhi/real-time-face-unlock-system.git
cd real-time-face-unlock-system
```

### 2. Create and activate virtual environment

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install dlib (Python 3.11 wheel)

```bash
pip install https://github.com/z-mahmud22/Dlib_Windows_Python3.x/raw/main/dlib-19.24.1-cp311-cp311-win_amd64.whl
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

---

##  Usage

```bash
python src/main.py
```

### Menu Options

| Option | Description |
|--------|-------------|
| 1 | Register a new face |
| 2 | Launch face unlock |
| 3 | List registered users |
| 4 | Delete a user |
| 5 | View access logs |
| 6 | Exit |

---

##  How It Works

1. The system captures a user's face using a webcam
2. Facial encodings are generated using dlib's deep learning model
3. Encodings are stored in `models/faces.pkl`
4. During authentication, live webcam frames are compared against stored encodings
5. If the similarity threshold is matched, access is granted
6. All attempts are logged in `data/access_log.csv`

---

## Future Improvements

- GUI-based interface
- Liveness/blink detection
- Web-based authentication system
- Cloud deployment
- Database integration
- Mobile application support

---

##  Author

**Mohit Gandhi**  
BTech CSE (Data Science & AIML)
