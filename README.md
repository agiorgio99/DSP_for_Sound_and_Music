# Digital Signal Processing for Sound & Music

This repository contains a collection of Jupyter Notebooks covering fundamental and advanced topics in Digital Signal Processing (DSP) applied to audio. The exercises progress from basic signal manipulation to complex spectral modeling and machine learning applications for sound description.

## 📂 Notebooks Overview

### **1. Basics & Fundamentals**
* **E1 - Python and Sounds**
    * Introduction to handling audio signals in Python using `sms-tools`.
    * Basic array manipulation, indexing, and reading/writing `.wav` files.
    * Understanding sampling rates, downsampling, and the phenomenon of **aliasing**.

* **E2 - Sinusoids and the DFT**
    * Generation of real and complex sinusoids.
    * Implementation of the **Discrete Fourier Transform (DFT)** and Inverse DFT (IDFT) from first principles.
    * Computation and visualization of magnitude spectra.

* **E3 - Fourier Properties**
    * Deep dive into Fourier theorems and DFT properties.
    * Understanding spectral leakage and minimizing energy spread.
    * The effects of **zero-padding** and FFT size on spectral resolution.
    * Symmetry properties of real, even, and odd signals.

### **2. Spectral Analysis**
* **E4 - Short-Time Fourier Transform (STFT)**
    * Analysis of windowing functions (main lobe width vs. side lobe attenuation).
    * Time-frequency analysis using the **STFT**.
    * Feature extraction: Computing energy bands and implementing an **Onset Detection Function (ODF)** for rhythm analysis.

### **3. Spectral Modeling**
* **E5 - Sinusoidal Model**
    * Modeling sounds as a sum of time-varying sinusoids.
    * Techniques for **peak detection** and parabolic interpolation to minimize frequency estimation error.
    * Tracking spectral peaks over time (sine tracking) to handle non-stationary signals like chirps.

* **E6 - Harmonic Model**
    * Focus on monophonic harmonic sounds.
    * Fundamental frequency (**$f_0$**) estimation using the Two-Way Mismatch (TWM) algorithm.
    * Quantifying **inharmonicity** (e.g., in piano strings) and segmenting audio based on stable pitch regions.

* **E7 - Sinusoidal Plus Residual Model**
    * Implementation of the **Harmonic plus Stochastic (HPS)** model.
    * Decomposing sound into a deterministic harmonic component and a stochastic residual component (noise).
    * Parameter tuning for accurate analysis/synthesis of speech and instruments.

### **4. Advanced Processing & ML**
* **E8 - Sound Transformations**
    * Creative manipulation of sound using the HPS model.
    * Techniques include **frequency scaling** (pitch shifting), **time scaling** (time-stretching), and timbre preservation.
    * Frequency stretching to create inharmonic effects.

* **E9 - Sound and Music Description**
    * Introduction to Music Information Retrieval (MIR).
    * Using the **Freesound API** to download datasets and descriptors.
    * Unsupervised learning: Clustering sounds using **K-means**.
    * Supervised learning: Classifying instrument sounds using **K-Nearest Neighbors (k-NN)**.

---

## 🎓 Final Exam Project

**Topic:** Analysis and Creative Transformation of Vocal Audio
**File:** `u269602_exam-Dec-2025_DSP.ipynb`

This final project demonstrates the practical application of the HPS model on a specific vocal sample (*"ninad_p__bhairav_phrase"*).

### **Key Tasks:**
1.  **Analysis:**
    * Detailed spectral analysis of the original vocal phrase.
    * Extraction of the fundamental frequency ($f_0$) and harmonic trajectories.
2.  **Creative Sound Design:**
    * The project involves generating a multi-layered soundscape by transforming the original voice into distinct "voices":
        * **Bass Layer:** Transposing the voice down by one octave.
        * **Soprano Layer:** Transposing the voice up by one octave.
        * **Sparkles Layer:** A creative effect involving a +2kHz frequency shift and high-pass filtering to create an inharmonic, high-frequency texture.
3.  **Synthesis:**
    * Recombining these transformed layers to verify the spectral modifications and achieve a cohesive aesthetic result.