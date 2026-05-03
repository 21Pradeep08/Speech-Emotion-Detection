Project Overview

This project presents a Speech Emotion Detection system that uses deep learning to identify human emotions from audio signals. By analyzing speech patterns, the system predicts the emotional state of a speaker.

The model is trained on two widely used emotional speech datasets:

RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song)
TESS (Toronto Emotional Speech Set)

Note: Due to their large size, these datasets are not included in the repository.

Approach

The project is divided into two main stages:

1. Model Training (1_model.ipynb)

This module focuses on building and training the model:

Loading and preprocessing audio data from RAVDESS and TESS
Applying noise reduction and normalization techniques
Extracting MFCC features using Librosa
Encoding emotion labels for supervised learning
Training a stacked LSTM-based neural network

LSTM networks are used to effectively capture temporal dependencies in speech, making them suitable for sequential audio analysis.
The trained model and preprocessing pipeline are saved for later use.

2. Real-Time Emotion Detection (2_realtime.ipynb)

This module enables live emotion prediction:

Capturing audio input through a microphone using PyAudio
Extracting MFCC features from real-time audio
Loading the trained LSTM model
Predicting the emotion instantly

This allows the system to perform real-time emotion recognition from speech input.

Technologies Used
Python
TensorFlow / Keras
LSTM Neural Networks
Librosa (feature extraction)
NumPy, Scikit-learn
PyAudio (real-time audio input)
Pydub, Noisereduce (audio preprocessing)
Emotions Detected

The model classifies speech into the following emotions:

Angry
Happy
Sad
Fear
Neutral
Disgust
Surprise
