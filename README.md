Project Overview:

This project implements a Speech Emotion Detection system that classifies human emotions from speech audio using deep learning. The system analyzes audio signals and predicts the emotional state of a speaker.

The model is trained using two popular emotional speech datasets:
RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song)
TESS (Toronto Emotional Speech Set)
Due to their large size, the datasets are not included in this repository.

Methodology

The project is divided into two main components:
1. Model Training (1_model.ipynb)
In this notebook we:
Load and preprocess audio files from the RAVDESS and TESS datasets
Perform noise reduction and audio normalization
Extract important audio features (MFCCs) using Librosa
Encode emotion labels for classification
Train a deep learning model using stacked LSTM layers
The LSTM (Long Short-Term Memory) network helps capture temporal patterns in speech signals, making it suitable for analyzing sequential audio data.
The trained model weights and preprocessing components are saved for later use.

2. Real-Time Emotion Detection (2_realtime.ipynb)
This notebook performs real-time speech emotion prediction by:
Recording audio from the microphone using PyAudio
Extracting the same MFCC features used during training
Loading the trained LSTM model
Predicting the emotion of the input speech
This allows the system to detect emotions from live microphone input in real time.

Technologies Used
Python
TensorFlow / Keras
LSTM Neural Networks
Librosa (audio feature extraction)
NumPy & Scikit-learn
PyAudio (real-time audio capture)
Pydub & Noisereduce (audio preprocessing)
Emotions Detected

The model is trained to recognize emotions such as:
Angry
Happy
Sad
Fear
Neutral
Disgust
Surprise