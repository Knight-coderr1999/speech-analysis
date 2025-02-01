# 🎵 Spectrogram Analysis & Windowing Techniques - UrbanSound8k 🎧

## 📌 Project Overview
This repository contains my implementation for **Experimenting with Spectrograms and Windowing Techniques** using **Python + PyTorch**. The project is divided into two major tasks:  
- **Task A**: Applying different windowing techniques to generate spectrograms and training a classifier.  
- **Task B**: Comparing spectrograms of different music genres and analyzing their characteristics.  

---

## 📂 Repository Structure
📁 Spectrogram-Analysis │── 📄 README.md # Project Documentation │── 📄 report.pdf # Final report with analysis and findings │── 📄 spectrogram_analysis.tex # LaTeX source file for the report │── 📁 src # Source code files │ ├── preprocess.py # Preprocessing UrbanSound8k dataset │ ├── windowing.py # Implementation of Hann, Hamming, and Rectangular windows │ ├── spectrograms.py # Generating and visualizing spectrograms │ ├── classifier.py # Neural network classifier for spectrogram-based classification │ ├── genre_analysis.py # Spectrogram analysis for different music genres │── 📁 datasets # UrbanSound8k dataset (not included due to size) │── 📁 results # Generated spectrogram images and classifier performance logs

---

## 🛠️ Technologies & Libraries Used
- **Python 3.8+**
- **PyTorch** (for neural network implementation)
- **Torchaudio** (for audio signal processing)
- **Matplotlib** (for spectrogram visualization)
- **Scikit-learn** (for classifier evaluation)
- **NumPy & Pandas** (for data handling)

---

## 🔍 Task A: Spectrograms & Classifier Performance

### 🎯 **What I Did**
✅ Implemented **three different windowing techniques**:  
- **Hann Window** – Best balance between time and frequency resolution  
- **Hamming Window** – Slightly better frequency localization  
- **Rectangular Window** – High spectral leakage, worst for spectrograms  

✅ Used **Short-Time Fourier Transform (STFT)** to generate spectrograms for UrbanSound8k audio samples.  

✅ Trained a **Neural Network classifier** on features extracted from spectrograms.  

✅ Compared **classifier performance** using different windowing techniques:  
| **Window Type**  | **Accuracy (%)** |
|------------------|----------------|
| Hann            | **85.2%**       |
| Hamming         | 84.8%           |
| Rectangular     | 78.4%           |

📝 **Conclusion:**  
Hann and Hamming windows **outperformed** the Rectangular window due to their **lower spectral leakage**, leading to better classification accuracy.

---

## 🎵 Task B: Spectrogram Analysis for Different Genres

### 🎯 **What I Did**
✅ Selected **4 different songs from different genres** (Pop, Classical, Jazz, Rock).  
✅ Generated **spectrograms for each genre** and analyzed their frequency characteristics.  
✅ Observed **distinct frequency patterns** that define each genre.  

| **Genre**    | **Spectrogram Characteristics** | **Dominant Frequency Range** |
|-------------|--------------------------------|------------------------------|
| **Pop**     | Structured, rhythmic patterns  | Mid-to-high frequencies      |
| **Classical** | Smooth, gradual frequency changes | Wide frequency range      |
| **Jazz**    | Complex harmonics, intricate variations | Mid and high frequencies |
| **Rock**    | Intense low-mid energy, strong beats | Low and mid frequencies   |

📝 **Conclusion:**  
Each genre exhibits **unique frequency distributions**. **Classical and Jazz** emphasize **harmonic richness**, while **Pop and Rock** focus more on **rhythm and strong beats**.

---

## 🚀 How to Run This Project

### 1️⃣ Clone this repository
```bash
git clone https://github.com/yourusername/Spectrogram-Analysis.git
cd Spectrogram-Analysis
2️⃣ Install dependencies
pip install -r requirements.txt
3️⃣ Run the spectrogram generation
python src/spectrograms.py
4️⃣ Train the classifier
python src/classifier.py
5️⃣ Perform genre analysis
python src/genre_analysis.py
