# Cricket Cover Drive Analysis – AI-Powered Pose Evaluation

## About the Project
This project analyzes a cricket player’s cover drive technique using computer vision. It tracks key body movements—like elbow angle, spine posture, head position, and foot alignment—to give meaningful feedback for improving batting performance. Think of it as a digital cricket coach that can guide you with real-time insights!

---

## What It Does
- **Automatic Video Input:** You can use a local video or download one directly from YouTube.  
- **Real-Time Pose Detection:** Detects body landmarks using MediaPipe Pose.  
- **Performance Metrics:**  
  - **Elbow Angle** – checks if your arms are properly extended.  
  - **Spine Lean** – monitors posture and balance.  
  - **Head-Knee Alignment** – makes sure your head is correctly positioned over your front knee.  
  - **Foot Alignment** – ensures your front foot is oriented correctly for stability.  
- **Swing Smoothness:** Tracks elbow movement to measure consistency in your swing.  
- **Visual Feedback:** The output video shows angles, scores, and feedback on-screen.  
- **Quantitative Analysis:** A JSON file summarizes your scores and gives comments for Footwork, Head Position, Swing Control, Balance, and Follow-through.  

---

## How It Works

### Video Handling
- Downloads YouTube videos automatically if not available locally.  
- Reads frames one by one using OpenCV.  

### Pose Detection
- Identifies landmarks such as shoulders, elbows, wrists, hips, knees, feet, and nose.  
- Converts these landmarks to pixel coordinates for accurate calculations.  

### Metrics & Scoring
- Uses trigonometry to calculate angles and distances between key points.  
- Applies Exponential Moving Average (EMA) to smooth out the metrics.  
- Compares metrics against thresholds and generates scores (1–10) with textual feedback.  

### Outputs
- **Annotated Video:** Shows landmarks, angles, and real-time feedback.  
- **JSON File:** `evaluation.json` contains detailed scores, comments, and thresholds.  

---

## Getting Started

1. **Install the required packages:**
```bash
pip install opencv-python mediapipe numpy yt-dlp


Run the Python script or Jupyter Notebook.


Outputs will be generated in the output/ folder:

annotated_video.mp4 → Video with annotated pose and feedback.

evaluation.json → Detailed numeric scores and comments.

Applications & Skills Demonstrated

Sports analytics for cricket coaching and performance enhancement.

Real-time computer vision and pose estimation implementation.

Python programming, vector mathematics, and data visualization.

Data-driven evaluation using thresholds and quantitative metrics.

Contact

Ayush Kumar – LinkedIn Profile
