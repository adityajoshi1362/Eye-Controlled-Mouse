# Eye-Controlled Mouse

## Overview
This project implements an eye-controlled mouse using OpenCV, MediaPipe, and PyAutoGUI. The system tracks head movements for cursor control and detects eye blinks for left-click actions. It enables hands-free computer interaction, particularly useful for individuals with mobility impairments.

## Features
- **Head Movement Control**: Moves the mouse cursor based on nose position tracking.
- **Eye Blink Click**: Performs a left click when both eyes are closed for a set duration.
- **Smooth and Responsive Control**: Uses real-time video processing with optimized landmark tracking.

## Dependencies
Ensure you have the following Python libraries installed:
```bash
pip install opencv-python mediapipe pyautogui numpy
```

## How It Works
1. **Nose Tracking for Cursor Movement**:
   - The program detects the nose landmark using MediaPipe's FaceMesh.
   - Movement of the nose is mapped to cursor movement using a sensitivity factor.

2. **Eye Blink Detection for Clicking**:
   - The program monitors the vertical distance between eye landmarks.
   - If both eyes remain closed for a specified duration, a left-click action is triggered.

## Usage
Run the script with:
```bash
python eye_controlled_mouse.py
```
### Controls:
- Move your **head** to move the cursor.
- Blink **both eyes** for at least 0.3 seconds to trigger a left click.
- Press **'q'** to exit the program.

## Code Explanation
- **Face Landmark Detection**: Uses MediaPipe to detect facial landmarks in real time.
- **Cursor Movement**: Computes displacement of the nose tip and maps it to screen coordinates.
- **Blink Detection**: Checks if the vertical eye ratio falls below a threshold to detect a blink.
- **Clicking Mechanism**: Executes a left-click using PyAutoGUI after confirming a valid blink.

## Future Improvements
- Add **right-click and drag functionality** based on different eye gestures.
- Implement **calibration settings** for different users.
- Improve **accuracy and robustness** for better usability.

## Acknowledgments
- [MediaPipe](https://developers.google.com/mediapipe) for real-time facial landmark detection.
- [OpenCV](https://opencv.org/) for image processing.
- [PyAutoGUI](https://pyautogui.readthedocs.io/en/latest/) for simulating mouse movements and clicks.

---
**Author**: Your Name  
**License**: MIT

