# VisuaReader (Blink-Controlled Page Turner)

**VisuaReader** is a hands-free page navigation system using blink gestures. It's designed for accessibility, reading PDFs or ebooks using eye blinks captured via webcam.

---

## 🚀 Features

* Blink detection using EAR (Eye Aspect Ratio)
* Long blink → Next Page
* Double long blink → Previous Page
* Visual EAR debug overlay
* Webcam-based, lightweight, and easy to extend

---

## 🖥️ Demo

![demo.gif](assets/demo.gif)

---

## 📦 Requirements

Install dependencies using pip:

```bash
pip install -r requirements.txt
```

**Required Files:**

* `shape_predictor_68_face_landmarks.dat`

> ⚠️ This model is large (\~100MB) and should be downloaded separately:
> [Download from dlib's official site](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2)

---

## 📁 Project Structure

```
blinkreader/
├── main.py
├── requirements.txt
├── README.md
├── .gitignore
└── assets/
    └── demo.gif
```

---

## ▶️ How to Run

1. Place the `shape_predictor_68_face_landmarks.dat` in the root directory.
2. Launch the script:

```bash
python main.py
```

3. Press `q` to quit.

---

## 🔧 Customization

You can tweak the following thresholds in `main.py`:

```python
blink_thresh = 0.20
blink_duration_thresh = 0.3  # seconds
double_blink_gap = 1         # seconds
```

---

## 📚 Acknowledgements

* [dlib](http://dlib.net/)
* [imutils](https://github.com/jrosebr1/imutils)
* Eye Aspect Ratio concept from Soukupová & Čech (2016)

---

## 📜 License

MIT License. Feel free to use and modify.
