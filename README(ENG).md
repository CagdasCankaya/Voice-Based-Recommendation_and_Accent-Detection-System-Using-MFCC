# Voice-Based Accent Recognition and Recommendation System: An MFCC and Web-Based Machine Learning Approach
In this project, MFCC (Mel-Frequency Cepstral Coefficients) features are extracted from a user's voice recording to predict potential preferences or areas of interest.
These extracted features are fed into a machine learning model to form the foundation of a voice-based recommendation system.
Additionally, users can record their voice through a microphone, and a simple API is provided via Flask for interaction.

# Technologies and Libraries Used
Python
Librosa – For extracting MFCC features from audio signals
NumPy – Numerical processing and array management
Pandas – Reading and processing datasets
Scikit-learn – Machine learning modeling (Random Forest)
Sounddevice & Wavio – Recording audio via microphone
Matplotlib – Visualizing feature distributions
Flask – Building a lightweight web interface/API

# PROJECT WORKFLOW
# 1. Data Preparation:
Audio files are extracted from a .tar archive. File paths and labels (accents or categories) are read from the train.tsv file.

# 2. Feature Extraction:
MFCC features are extracted from each audio file. The time-averaged values of these features are calculated to create fixed-size vectors.
A sample rate of 44,100 Hz is used for high-resolution audio processing.

# 3. Model Training:
The MFCC features are matched with corresponding labels, and a RandomForestClassifier is trained.
Achieved accuracy: 82% (accuracy = 0.824)

# 4. Audio Recording:
Users can record audio via a microphone. The recordings are saved in .wav format and prepared for analysis.

# 5. API Development:
A basic web interface is provided via Flask. In the future, this API can be extended to accept live audio input and return classification/prediction results.

# File Structure
├── extracted_features.npy       # Saved MFCC feature vectors
├── voiceDatas.tar               # Compressed voice dataset
├── extracted_files/             # Extracted audio and .tsv files
├── train.tsv                    # Labeled training data
├── recorded_audio.wav           # User-recorded audio sample
├── app.py                       # Flask web API
├── model_training.py            # Feature extraction and model training code
└── README.md

# Future Improvements
Enhance the model using deep learning techniques (e.g., CNN, LSTM).
Enrich the recommendation system by collecting and integrating more user voice data.

# Project Owner:
Çağdaş ÇANKAYA
