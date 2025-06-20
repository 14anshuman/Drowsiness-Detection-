# Real‑Time Drowsiness Detection System 😴🚗

A computer‑vision powered **real‑time driver drowsiness detection** application built using Python, OpenCV, Dlib, and facial landmark analysis. It monitors eye/mouth aspect ratios and triggers alerts when signs of drowsiness (eyes closed, yawning) are detected.

---
## Motivation
According to the National Highway Traffic Safety Administration, every year about 100,000 police-reported crashes involve drowsy driving. These crashes result in more than 1,550 fatalities and 71,000 injuries. The real number may be much higher, however, as it is difficult to determine whether a driver was drowsy at the time of a crash. So, we tried to build a system, that detects whether a person is drowsy and alert him.

---
## 🧠 Features

- Real-time video stream processing via webcam  
- Face detection using **Haar Cascades**  
- Facial landmark extraction with **Dlib’s 68-point predictor**  
- Eye Aspect Ratio (EAR) and Mouth Aspect Ratio (MAR) for blink and yawning detection  
- Threshold‑based alarm for sustained eye closure or yawning  
- Lightweight and easy to run on consumer hardware  
- No special hardware required—works with standard webcams

---
## 🧠 Architecture

1. **Webcam input** is captured frame by frame.
2. **Face detection** is performed using OpenCV’s Haar cascade classifier.
3. **Facial landmarks** (eyes, mouth) are extracted using Dlib.
4. **EAR and MAR** values are calculated to determine eye closure and yawning.
5. **Threshold logic** monitors EAR/MAR over time.
6. If thresholds are breached for several frames:
   - An **audio alert** is triggered using the `playsound` library.

