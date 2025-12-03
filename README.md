# Multimodal-Biometric-Authentication-for-E-vehicles
A deep-learning–based multimodal authentication system using face and voice biometrics for secure E-Vehicle access.

## 🚀 Overview
This project implements a multimodal biometric authentication system that fuses face recognition and voice verification to provide a secure access mechanism for electric vehicles.
Traditional PINs and single-biometric systems falter under noise, lighting changes, and spoofing attempts — this framework counteracts those weaknesses with deep-learning embeddings and combined decision logic.
The system uses:
- *RetinaFace + FaceNet* for facial embedding extraction
- *SpeechBrain ECAPA-TDNN* for speaker verification
- *Decision-level fusion* to strengthen reliability
- A simple *UI for user registration & authentication*

## 🧠 Features
- Deep-learning based face recognition
- Voiceprint authentication using ECAPA-TDNN
- Multimodal fusion for improved accuracy & spoof-resistance
- Real-time registration & authentication interface
- Tested on LFW, GRID, and custom real-world datasets
- Threshold tuning & multi-sample enrollment support

## System Architecture
The system has four core layers:
*1. Data Acquisition*
   - Webcam (face), microphone (voice)
*2. Feature Extraction*
   - FaceNet → 128-D face embeddings
   - SpeechBrain ECAPA-TDNN → speaker embeddings
   - Cosine / Euclidean similarity scoring
*3. Decision Fusion*
   - Final authentication combines two independent matching scores.
*4. User Interface*
   - Registration & authentication workflow with real-time capture.

## Dataset Summary
*Face:*
- LFW (13k+ unconstrained faces)
- GRID (frontal, consistent lighting)
*Voice:*
- GRID audio
- Custom dataset recorded in noisy, real-world settings
This blend ensures robustness across lighting, noise, and device variation.

## 📈 Performance Highlights

| Modality        | 1 Sample | 5 Samples |
|-----------------|----------|-----------|
| **Face**        | 76.06%   | 89.01%    |
| **Voice**       | 37.47%   | 87.40%    |
| **Face + Voice**| —        | **93.53%** |

**Best threshold:** `0.65`  
Increasing enrollment samples greatly improves stability and accuracy.
