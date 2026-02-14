# 😎 Face Recognition with Python

> Simple. Fast. Cool.
> A lightweight face recognition project built using **Python**, **OpenCV**, and **face_recognition**. Detect, encode, and recognize faces in real time with clean and minimal code.

---

## ✨ Features

* 🎯 Real-time face detection via webcam
* 🧠 Face encoding & matching
* 👥 Multiple face recognition
* ⚡ Fast and lightweight
* 🧩 Easy to customize & extend

---

## 🛠️ Tech Stack

* **Python 3.x**
* **OpenCV**
* **face_recognition (dlib)**
* **NumPy**

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/your-username/face-recognition-python.git
cd face-recognition-python
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Or manually:

```bash
pip install opencv-python face_recognition numpy
```

---

## 📂 Project Structure

```
face-recognition-python/
│
├── faces/                # Known face images
│   ├── person1.jpg
│   ├── person2.jpg
│
├── encode_faces.py       # Encode known faces
├── recognize_faces.py    # Real-time recognition
├── requirements.txt
└── README.md
```

---

## 🧠 Encode Known Faces

Add images of known people inside the **faces/** folder, then run:

```bash
python encode_faces.py
```

This generates face encodings for recognition.

---

## 🎥 Run Face Recognition

```bash
python recognize_faces.py
```

* Webcam opens 📷
* Faces detected in real time
* Names displayed automatically

Press **Q** to quit.

---

## 🧩 Example (Core Logic)

```python
import face_recognition
import cv2

image = face_recognition.load_image_file("faces/person1.jpg")
encoding = face_recognition.face_encodings(image)[0]

unknown = face_recognition.load_image_file("test.jpg")
unknown_encoding = face_recognition.face_encodings(unknown)[0]

results = face_recognition.compare_faces([encoding], unknown_encoding)
print("Match Found:", results[0])
```

---

## ⚙️ Requirements

* Python ≥ 3.8
* Webcam (for real-time mode)
* Good lighting for better accuracy

---

## 🚀 Future Improvements

* GUI interface
* Face database (SQLite / JSON)
* Emotion detection 😄😐😢
* Mask detection 😷
* Web / Flask API

---

## 🤝 Contributing

Pull requests are welcome. For major changes, open an issue first.

---

## 📜 License

MIT License — free to use, modify, and distribute.

---

## ⭐ Support

If you like this project, give it a **star ⭐** and share it with others.

**Stay cool. Keep building.** 😎
