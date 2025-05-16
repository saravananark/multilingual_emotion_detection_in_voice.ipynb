# multilingual_emotion_detection_in_voice.ipynb

### 🧠 Purpose:

To transcribe audio using Whisper and detect the speaker's emotion using audio features.

---

### 📦 Libraries Used:

* `openai-whisper`: for transcription and language detection
* `librosa`: for audio processing and feature extraction
* `scikit-learn`: for machine learning classification (SVM)
* `moviepy`: to convert MP4 video files to WAV audio

---

### 🔧 Main Steps in the Code:

1. **Install Dependencies**:

   ```python
   pip install openai-whisper librosa scikit-learn
   ```

2. **Load Whisper Model**:

   ```python
   model = whisper.load_model("base")
   ```

3. **Transcribe Audio**:
   Uses Whisper to transcribe spoken content and detect the language.

4. **Extract Audio Features**:
   Extracts MFCC (Mel-frequency cepstral coefficients) and pitch from the audio using `librosa`.

5. **Train Emotion Classifier**:
   A basic SVM classifier is trained on random synthetic data (you'd replace this with real emotion-labeled audio data in practice).

6. **Classify Emotion**:
   Predicts the emotion based on audio features.

7. **Convert MP4 to WAV**:
   Converts video input into audio format suitable for processing.

8. **Complete Pipeline**:
   The function `emotion_aware_speech_recognition(mp4_path)` handles the whole workflow:

   * MP4 → WAV
   * Transcription
   * Emotion classification
   * Outputs emotion, transcription, and language

---

### 📌 Notes:

* The classifier is currently trained on random data—this is a placeholder and should be replaced with real labeled training data for meaningful predictions.
* There are no markdown cells explaining the code—just the code cells.

