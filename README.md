# 🧠 Eye-Controlled Mouse 👁️🖱️

Control your mouse using your **eyes** with this Python-based real-time project using **OpenCV**, **MediaPipe**, and **PyAutoGUI**. No mouse, no touchpad — just blink and move your eyes!

![ChatGPT Image May 20, 2025, 01_42_43 PM](https://github.com/user-attachments/assets/0182829d-90c5-45e1-9763-6709c77a9e19)



## ✨ Features

- 🧿 Real-time eye tracking using MediaPipe Face Mesh  
- 🖱️ Mouse pointer movement using iris detection  
- 👁️ Left click using eye blink detection  
- 🔁 Flipped webcam feed for intuitive movement  
- 🖥️ Works on most standard webcams

---

## 🔧 Requirements

- Python 3.7 or higher  
- `opencv-python`  
- `mediapipe`  
- `pyautogui`

Install dependencies:

```bash
pip install opencv-python mediapipe pyautogui
```
---

## 🧪 How It Works

- The webcam captures your face in real-time.
- MediaPipe’s Face Mesh detects 468 facial landmarks.
- Landmarks around the right eye (indexes 474–478) are used to track the iris position.
- Cursor position is updated using `pyautogui.moveTo()` based on eye location.
- Eye blink detection is done using the vertical distance between eyelid landmarks (145 and 159).
- If the distance is small (i.e., eyes closed), a left click is triggered using `pyautogui.click()`.

---


