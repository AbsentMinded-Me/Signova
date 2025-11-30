# **Signova – Sign Language to Text Converter**

Signova is an AI-powered sign language reader designed to convert **ASL (American Sign Language) hand signs** into **text**.
The current version supports **ASL alphabet recognition**, and future releases will expand to full-word and full-sentence detection.

---

## **Features**

*  Real-time detection of ASL alphabet gestures
*  Converts hand signs into English text
*  Easy-to-use interface
*  Built using state-of-the-art deep learning techniques
*  Modular codebase for easy improvement

---

## **Model Used**

This project uses a pre-trained model hosted on **Hugging Face**:

**Model:** `prithivMLmods/Alphabet-Sign-Language-Detection`
**Task:** Image Classification (ASL Alphabets)

The model is loaded using the Hugging Face `transformers` pipeline:

```python
from transformers import pipeline

pipe = pipeline("image-classification",
                model="prithivMLmods/Alphabet-Sign-Language-Detection")

result = pipe("your_image.png")
print(result)
```

---

## **Installation**

Clone the repository:

```bash
git clone https://github.com/yourusername/Signova.git
cd Signova
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## **Usage**

Run your inference script (example):

```python
from model_utils import predict_sign

prediction = predict_sign("sample_image.jpg")
print("Detected Sign:", prediction)
```

For real-time webcam detection:

```bash
python run_webcam.py
```

---

## **Project Structure**

```
Signova/
│── models/              # Model files & checkpoints
│── utils/               # Helpers for preprocessing & prediction
│── data/                # Dataset or sample images
│── run_webcam.py        # Real-time prediction script
│── inference.py         # Single image prediction
│── requirements.txt     # Dependencies
│── README.md            # Project Documentation
```

---

## **Tech Stack**

* Python
* PyTorch / TensorFlow (depending on your implementation)
* Hugging Face Transformers
* OpenCV
* NumPy & Pandas

---

## **Future Improvements**

* ⬜ Word-level sign recognition
* ⬜ Sentence-level translation
* ⬜ Multi-hand gesture detection
* ⬜ Support for other sign languages (ISL, BSL, etc.)
* ⬜ Deploy as a web or mobile app

---

## **Contributors**

* **Tanisha Gupta** – Backend developer
* **Tanvi Haldaun** – Frontend developer

