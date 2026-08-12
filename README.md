# RF Signal Measurement & Spectrum Analysis System

## 📌 Overview

The **RF Signal Measurement & Spectrum Analysis System** is an SDR-based digital signal processing project designed to capture, analyze, and visualize RF signals in the frequency domain. The system processes I/Q samples obtained from an SDR receiver and applies FFT-based signal processing to identify signal frequency, amplitude, bandwidth, noise characteristics, and spectral peaks.

The project demonstrates the fundamentals of **RF measurement, Digital Signal Processing (DSP), spectrum analysis, signal detection, and measurement validation**.

---

## 🎯 Objectives

* Acquire RF/IQ samples using an SDR receiver.
* Convert time-domain samples into frequency-domain information using FFT.
* Detect and characterize RF signals.
* Estimate frequency, amplitude, bandwidth, and noise floor.
* Visualize RF activity using spectrum and waterfall plots.
* Validate detected signal parameters against known reference signals.

---

## 🏗️ System Architecture

```text
RF Signal
    ↓
Antenna / RF Source
    ↓
SDR Receiver
    ↓
I/Q Data Acquisition
    ↓
Signal Preprocessing
    ↓
Windowing & Filtering
    ↓
FFT Processing
    ↓
Power Spectrum Calculation
    ↓
Peak Detection
    ↓
Frequency / Bandwidth Estimation
    ↓
Spectrum & Waterfall Visualization
    ↓
Measurement Validation
```

---

## ⚙️ Working Principle

### 1. RF Signal Acquisition

The SDR receiver captures RF signals and converts them into complex **In-phase (I)** and **Quadrature (Q)** samples.

Configurable parameters include:

* Center Frequency
* Sample Rate
* RF Gain
* FFT Size
* Frequency Span

### 2. Signal Preprocessing

The acquired samples are conditioned before frequency-domain analysis.

Processing includes:

* DC offset removal
* Signal normalization
* Noise reduction
* Digital filtering

### 3. Windowing

A window function such as Hann, Hamming, or Blackman is applied to reduce spectral leakage before FFT processing.

### 4. FFT-Based Spectrum Analysis

The preprocessed IQ samples are transformed into the frequency domain using FFT. The resulting frequency spectrum is used to identify dominant signal components.

### 5. Peak Detection

An automatic peak-detection algorithm identifies significant RF signals above the estimated noise floor.

The system extracts:

* Peak frequency
* Peak magnitude
* Signal threshold
* Number of detected signals

### 6. Bandwidth Estimation

The bandwidth of detected signals is estimated using threshold-based or -3 dB measurement techniques.

### 7. Waterfall Visualization

Successive FFT frames are stored over time to generate a waterfall display, allowing observation of:

* Continuous signals
* Intermittent signals
* Frequency changes
* Interference
* Signal-strength variations

### 8. Measurement Validation

The system is tested using known-frequency signals and different signal strengths. Measured frequency and spectral parameters are compared against expected values to evaluate system accuracy.

---

## 🧪 Testing

The system can be evaluated using:

| Test                       | Purpose                        |
| -------------------------- | ------------------------------ |
| Single-frequency signal    | Verify frequency detection     |
| Multiple-frequency signals | Verify peak detection          |
| Different signal strengths | Evaluate detection sensitivity |
| Added noise                | Evaluate robustness            |
| Different sampling rates   | Verify sampling performance    |
| Different FFT sizes        | Analyze frequency resolution   |

---

## 📊 Parameters Measured

* Center Frequency
* Peak Frequency
* Signal Amplitude
* Bandwidth
* Noise Floor
* Signal-to-Noise Ratio
* Frequency Detection Error
* Spectral Peaks

---

## 🛠️ Technologies Used

**Software:** Python, NumPy, SciPy, Matplotlib/PyQtGraph

**Hardware:** RTL-SDR / SDR Receiver, Antenna

**DSP:** FFT, Windowing, Digital Filtering, IQ Processing, Peak Detection, Spectrum Analysis

**RF:** RF Signal Acquisition, Frequency Measurement, Bandwidth Analysis, Noise Analysis

---

## 📁 Project Structure

```text
RF-Signal-Measurement-Spectrum-Analysis/
│
├── src/
│   ├── acquisition.py
│   ├── preprocessing.py
│   ├── fft_processor.py
│   ├── peak_detector.py
│   ├── bandwidth.py
│   └── main.py
│
├── data/
│   └── sample_iq/
│
├── results/
│   ├── spectrum.png
│   └── waterfall.png
│
├── tests/
│   ├── test_fft.py
│   └── test_peak_detection.py
│
├── requirements.txt
└── README.md
```

---

## 🚀 Future Enhancements

* Real-time SDR signal acquisition
* Automated frequency sweeping
* RF signal classification
* Automated interference detection
* Signal modulation identification
* Calibration using a reference signal generator
* Integration with laboratory spectrum-analyzer measurements

---

## 📌 Applications

* RF signal monitoring
* Spectrum analysis
* Communication-system testing
* Interference detection
* SDR experimentation
* RF measurement and characterization
* DSP algorithm development

---

## 📈 Learning Outcomes

This project provides practical experience with:

* RF signal acquisition
* I/Q signal processing
* FFT-based spectrum analysis
* Digital filtering
* Signal detection
* Frequency and bandwidth measurement
* Noise analysis
* SDR technology
* Algorithm testing and validation

---

## 👩‍💻 Author

**Lasyasri**

Electronics & Communication Engineering
Interests: Digital Signal Processing · RF Systems · Radar · Embedded Systems

