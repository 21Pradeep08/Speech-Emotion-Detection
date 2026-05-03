## Project Overview

This project presents a Speech Emotion Detection system that uses deep learning to identify human emotions from audio signals. By analyzing speech patterns, the system predicts the emotional state of a speaker.

The model is trained on two widely used emotional speech datasets:
- RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song)
- TESS (Toronto Emotional Speech Set)

Note: Due to their large size, these datasets are not included in the repository.

---

## Approach

The project is divided into two main stages:

### 1. Model Training (1_model.ipynb)

This module focuses on building and training the model:

- Load and preprocess audio data from RAVDESS and TESS  
- Apply noise reduction and normalization  
- Extract MFCC features using Librosa  
- Encode emotion labels for classification  
- Train a stacked LSTM-based neural network  

LSTM networks capture temporal patterns in speech, making them effective for sequential audio analysis. The trained model and preprocessing components are saved for later use.

---

### 2. Real-Time Emotion Detection (2_realtime.ipynb)

This module enables live emotion prediction:

- Record audio using PyAudio  
- Extract MFCC features from input speech  
- Load the trained LSTM model  
- Predict emotions in real time  

This allows the system to perform real-time emotion recognition using microphone input.

---

## Technologies Used

- Python  
- TensorFlow / Keras  
- LSTM Neural Networks  
- Librosa (audio feature extraction)  
- NumPy, Scikit-learn  
- PyAudio (real-time audio capture)  
- Pydub, Noisereduce (audio preprocessing)  

---

## Emotions Detected

- Angry  
- Happy  
- Sad  
- Fear  
- Neutral  
- Disgust  
- Surprise  
