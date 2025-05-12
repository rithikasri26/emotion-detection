
# 😄 Facial and Voice Emotion Detection using Deep Learning 🎙️

This project integrates **computer vision** and **audio signal processing** to detect human emotions from both **facial expressions** and **voice input**. It uses pre-trained deep learning models and open-source libraries to analyze user-uploaded media and identify emotional states.

---

## 📌 Features

- Upload **images** to detect facial emotions.
- Upload **audio files** to detect voice-based emotions and transcribe speech.
- Multi-format audio support (`.mp3`, `.mp4`, `.wav`, `.opus`, `.m4a`)
- Detects spoken **language** using OpenAI's Whisper model.
- Uses **Whisper** for speech-to-text transcription and a dummy **SVM** model for voice emotion classification.
- Visual feedback with image annotation for detected facial emotions.

---

## 🛠️ Technologies Used

- Python
- OpenCV
- Keras (Mini-XCEPTION model for emotion detection)
- Whisper (by OpenAI)
- Librosa (audio feature extraction)
- Pydub & FFMPEG (audio conversion)
- Scikit-learn (SVM for dummy voice emotion classification)
- Google Colab

---

## 🚀 How to Run

1. Open the notebook in **Google Colab**.
2. Install the required libraries:
   ```bash
   !pip install -q keras opencv-python librosa moviepy openai-whisper pydub ffmpeg-python
   ```
3. Download the pre-trained facial emotion detection model:
   ```bash
   !wget -q https://github.com/oarriaga/face_classification/raw/master/trained_models/emotion_models/fer2013_mini_XCEPTION.102-0.66.hdf5 -O emotion_model.h5
   ```
4. Upload an **image** or **audio** file when prompted.

---

## 📚 Functional Breakdown

- **Facial Emotion Detection**:
  - Uses Haar cascade to detect faces.
  - Applies a pre-trained CNN model to classify into: `Angry`, `Disgust`, `Fear`, `Happy`, `Sad`, `Surprise`, `Neutral`.

- **Voice Emotion Detection**:
  - Converts any format audio to WAV.
  - Extracts MFCC & pitch features with `librosa`.
  - Classifies emotion using a basic trained SVM model (for demonstration).
  - Transcribes speech and detects language using `whisper`.

---


## ⚠️ Note

- The voice emotion classifier is a **placeholder model** trained on random data. Replace it with a real dataset for production use.
- Whisper's performance may vary depending on audio quality and accents.

---

## 🔮 Future Work

- Use real datasets (e.g., RAVDESS) to train a robust audio emotion classifier.
- Add live webcam and microphone support.
- Integrate with a real-time web interface using Streamlit or Flask.


This project is open-source and free to use for educational and non-commercial purposes.
