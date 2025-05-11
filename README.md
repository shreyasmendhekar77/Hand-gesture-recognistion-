# Hand-gesture-recognistion-
# 🤖 Hand Gesture Recognition for Media Control

## 📁 Project Category
**Image Processing**

---

## 🛠 Tools & Platform

- **Platform:** Anaconda Navigator  
- **IDE:** Spyder Console  
- **Programming Language:** Python 3.5  
- **Libraries:**  
  - OpenCV  
  - NumPy  
  - pyautogui  
- **Hardware:** Laptop with integrated camera  

---

## ⚙️ OpenCV Installation

Install OpenCV using one of the following commands:

```bash
# Option A
pip install file_path/opencv_python-3.4.2-cp36-cp36m-win_amd64.whl

# Option B (with contrib modules)
pip install file_path/opencv_python-3.4.2+contrib-cp36-cp36m-win_amd64.whl
```

---

## 🚀 Methodology / Working

### 1. Access Camera
- OpenCV accesses the laptop camera to capture real-time frames.

### 2. Preprocessing
- Convert frame to grayscale.
- Convert grayscale to binary to isolate Region of Interest (ROI) – the hand.

### 3. Apply Gaussian Blur
- Smoothens image and reduces noise.
- Useful for emphasizing object shape over detail.

### 4. Thresholding
- Segments hand from background using Otsu's method.
- Converts image to binary format.

### 5. Contour Detection
- Finds object boundaries in the binary image.
- Requires grayscale + binary thresholded image.

### 6. Convex Hull & Convexity Defects
- Convex hull wraps around the hand contour.
- Convexity defects identify finger gaps.
- Cosine rule applied to calculate angles between fingers.
- Count of angles < 90° gives number of fingers.

### 7. Gesture Recognition
- Extracts:
  - Start point
  - End point
  - Farthest point
  - Distance to farthest point
- Draws circles at defect points.
- Displays finger count on-screen.

### 8. Media Control Using Gestures (via `pyautogui`)

| Finger Count | Action           |
|--------------|------------------|
| 2            | Increase Volume  |
| 3            | Decrease Volume  |
| 4            | Fast Forward     |
| 5            | Stop / Pause     |

---

## 🔄 Workflow Diagram

```
Camera Input 
     ↓
Frame Capture 
     ↓
Grayscale & Thresholding 
     ↓
Contour Detection 
     ↓
Convex Hull & Defects 
     ↓
Finger Count Detection 
     ↓
pyautogui Media Control
```

---

## 🎯 Application Output

- Real-time gesture recognition via webcam.
- Displays finger count.
- Controls media player volume and playback using gestures.

---

## 🚀 Future Scope

- Extend functionality to detect multiple hand gestures.
- Develop cross-platform widget for gesture-based OS control.
- Integrate 3D modeling and supervised ML for better accuracy.
- Combine with face detection and body posture for robust interaction.

---

## ✅ Conclusion

This project shows a functional hand gesture recognition system using OpenCV and geometric rules. It offers an intuitive interface for media control and lays a foundation for broader gesture-based interaction applications in HCI, robotics, and AR/VR.

---

## 📬 Contact

For queries or contributions, feel free to open an issue or pull request.
