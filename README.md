# Automated Face Sketching and Identification for Forensic Investigation

An AI-based forensic system designed to automate facial sketch generation from textual descriptions and identify visually similar faces from a facial database.

## Overview

Traditional forensic sketching relies on eyewitness descriptions and manual sketching, which can be time-consuming and subjective. This project explores an automated approach that combines generative AI and face recognition techniques to support forensic investigation.

The system is organized into two main phases:

1. **Text-to-Sketch Generation**
   - Takes a textual description of facial features as input.
   - Uses Stable Diffusion with ControlNet to generate a facial sketch based on the description.

2. **Face Identification**
   - Uses the generated sketch as input.
   - Extracts facial representations using a deep face-recognition model.
   - Compares the generated sketch against facial images using cosine similarity.
   - Retrieves the top matching faces from the database.

## System Pipeline
```text
Eyewitness Description
        ↓
Natural Language Input
        ↓
Text-to-Sketch Generation
(Stable Diffusion + ControlNet)
        ↓
Generated Facial Sketch
        ↓
Face Embedding Extraction
        ↓
Cosine Similarity Matching
        ↓
Top Matching Faces
```

# Technologies:
  - Python
  - Stable Diffusion
  - ControlNet
  - Deep Learning
  - Computer Vision
  - Face Recognition
  - Face Embeddings
  - Cosine Similarity
  - CelebA / FFHQ datasets
  - Google Colab
  - T4 GPU

# Project Objectives:
  - Automate facial sketch generation from textual descriptions.
  - Reduce dependence on manual forensic sketching.
  - Support identification by matching generated sketches with facial databases.
  - Improve the efficiency and consistency of the forensic identification process.
  - Explore the application of generative AI and computer vision in forensic investigation.
    
# Research Publication:
The project also resulted in research work on generative AI-based forensic image synthesis and identification.

Paper: Exploring GANs for Image Synthesis and Recognition in Forensic Contexts

Presented at INDIACom-2025 – 12th International Conference on Computing for Sustainable Global Development.
