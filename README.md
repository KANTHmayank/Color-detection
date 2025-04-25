# 🎯 Real-Time Color Tracker using OpenCV

This project is a real-time color detection system built using Python and OpenCV. It tracks a specified color in a live video feed from your webcam and draws a bounding box around it.


## 🛠️ Features

- Detects and tracks a target color in real-time using OpenCV.
- Converts BGR input to HSV and dynamically computes color thresholds.
- Displays bounding boxes over detected regions.
- Modular design: color logic separated into `util.py`.

---

## 🧠 How It Works

1. **Color Conversion**: The target color (e.g. yellow `[0, 255, 255]` in BGR) is converted to HSV to handle lighting variations.
2. **Mask Generation**: A color range around the target hue is computed and used to isolate matching pixels.
3. **Bounding Box Detection**: Using `PIL.Image.getbbox()`, a rectangle is drawn around the largest detected region.

---

## 🚀 Getting Started

### Prerequisites

- Python 3.7+
- OpenCV
- Pillow
- NumPy

### Installation

git clone https://github.com/yourusername/color-tracker.git
cd color-tracker
pip install -r requirements.txt


### Run the App

python main.py

Press q to quit the live window.


📂 Project Structure

Color-detection/
├── main.py         # Main script to capture video and display tracking
├── util.py         # Helper function to generate color limits
└── README.md       # Project documentation
├── requirements.txt  # necessary packages


Edit this line in main.py to change the target color:

yellow = [0, 255, 255]  # BGR color to detect

📌 Future Enhancements

Click-to-track: Allow user to click on a color in the frame.

Integration with object detection models (YOLO/SSD) for enhanced functionality.






