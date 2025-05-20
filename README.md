
# 🎧 EEG Emotion-Based Music Decoder

This project detects emotions from EEG signals using a Support Vector Machine (SVM) classifier and plays music based on the predicted emotion.

## 📁 Dataset
EEG data is sourced from the [SpringerNature EEG Dataset](https://springernature.figshare.com/articles/dataset/Preprocessed_Dataset/25751097).

## 🧠 Pipeline Overview

1. **EEG Signal Processing**: 
   - Extract band power features (Alpha, Beta, Gamma) using Welch's method.

2. **Modeling**: 
   - Train a Support Vector Machine (SVM) on the extracted features.
   - Evaluate model performance with classification metrics.

3. **Audio Output**:
   - Based on the predicted emotion, play a corresponding tune using `playsound`.

## 📦 Requirements

Make sure to install the following packages (Python ≥ 3.10 recommended):

```bash
pip install numpy>=1.22
pip install scipy>=1.8
pip install scikit-learn>=1.1
pip install playsound==1.3.0
```

## 📂 Folder Structure

```
project/
│
├── data/
│   └── deap/                # Place EEG .pkl data files here
│
├── music/                   # Music files played on emotion detection
│
├── music_decoder.ipynb      # Main notebook
└── README.md                # This file
```

## 📝 Notes
- The notebook expects preprocessed EEG data stored in `.pkl` files inside the `data/deap/` directory.
- Music files should be placed in the `music/` directory, each corresponding to an emotion label.

---

**Author**: Rasa rezaei 
**License**: MIT
