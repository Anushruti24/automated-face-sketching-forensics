# Automated Face Sketching and Identification for Forensic Investigation

An AI-based forensic system that generates facial sketches from textual descriptions and identifies visually similar faces from a facial image database.

The project combines generative AI, computer vision, natural language-based descriptions, and deep learning-based face recognition to support forensic investigation when photographic evidence may not be available.

## Generative AI Approach

The project was initially designed around GAN-based image synthesis for generating facial sketches from textual descriptions.

Training a GAN from scratch would require a large, diverse dataset and significant computational resources. Therefore, the final implementation uses pretrained generative models, particularly Stable Diffusion with ControlNet, to perform the sketch-generation stage while retaining the project's underlying objective of AI-driven generative facial synthesis.

The generated sketch is subsequently processed through a deep-learning-based face identification pipeline using MTCNN, FaceNet/InceptionResnetV1, and cosine similarity.

---

## Overview

Traditional forensic sketching relies heavily on eyewitness descriptions and manual sketching by forensic artists. This process can be time-consuming and may be affected by limitations in human memory and artistic interpretation.

This project explores an automated approach in which a textual description of a person's facial characteristics is used to generate a facial sketch. The generated sketch is then compared against a facial image database to identify visually similar faces.

The system consists of two major phases:

### Phase 1 — Text-to-Sketch Generation

A textual description of facial features is provided as input to a generative image pipeline.

- Accepts descriptive facial attributes as text input.
- Uses **Stable Diffusion** for text-to-image generation.
- Uses **ControlNet** to provide additional structural guidance during generation.
- Produces a facial sketch based on the provided description.

### Phase 2 — Face Identification

The generated sketch is then processed for facial similarity matching.

- Detects and aligns the face using **MTCNN**.
- Extracts facial embeddings using **FaceNet / InceptionResnetV1**.
- Represents each face as a 512-dimensional embedding.
- Compares the generated sketch with precomputed facial embeddings using **cosine similarity**.
- Retrieves the top 3 matching faces from the database.

---

## System Pipeline

```text
Eyewitness Description
        ↓
Natural Language Input
        ↓
Stable Diffusion + ControlNet
        ↓
Generated Facial Sketch
        ↓
MTCNN Face Detection & Alignment
        ↓
FaceNet / InceptionResnetV1
        ↓
512-D Facial Embedding
        ↓
Cosine Similarity Matching
        ↓
Top 3 Matching Faces
```

---

## Key Features

- Text-based facial sketch generation
- Generative AI-based image synthesis
- Structural guidance using ControlNet
- Automated face detection and alignment
- Deep-learning-based facial embeddings
- Similarity-based face identification
- Top-match retrieval from a facial image database
- Interactive demonstration using a frontend and backend pipeline
- Research-oriented evaluation of sketch generation and face identification

---

## Technologies Used

### Generative AI & Deep Learning
- Stable Diffusion
- ControlNet
- FaceNet
- InceptionResnetV1
- Deep Learning

### Computer Vision
- MTCNN
- Facial Embeddings
- Cosine Similarity
- Image Processing
- Face Recognition

### Data & Development
- Python
- CelebA Dataset
- Google Colab
- T4 GPU

### Integration
- ngrok
- Frontend / Backend Integration

---

## Dataset

The project makes use of publicly available facial datasets for experimentation and identification.

### CelebA

CelebA (CelebFaces Attributes Dataset) provides facial images along with facial attribute annotations and was used as a source for facial image embeddings and similarity matching.

---

## Results

The system was evaluated across the two major stages of the pipeline.

### Sketch Generation

The system generated facial sketches from detailed textual descriptions containing attributes such as facial shape, eyes, eyebrows, nose, lips, hair, and other distinguishing characteristics.

The reported results showed that the generated sketches generally preserved the major facial characteristics described in the input prompt, although some stylization and exaggeration typical of generative models were observed.

### Face Identification

The generated sketch was converted into a facial embedding and compared against precomputed embeddings from the facial database using cosine similarity.

The reported top three matches achieved the following similarity scores:

| Rank | Cosine Similarity |
|------|-------------------|
| Top 1 | 0.8202 |
| Top 2 | 0.7718 |
| Top 3 | 0.7669 |

A similarity threshold of **0.75** was used in the reported experiment, with all three retrieved matches exceeding the threshold.

The highest reported similarity score was **0.8202**.

---

## Research Publication

The project resulted in research work exploring AI-based forensic face sketch generation and identification.

### Research Paper 1

**Applying GANs for Image Synthesis and Recognition in Forensic Contexts**

Published in the proceedings of:

**2025 12th International Conference on Computing for Sustainable Global Development (INDIACom)**

The research explored GAN-based approaches, including StackGAN, for forensic face sketch generation and recognition.

### Research Paper 2

The project was further developed into research focusing on generative AI-based forensic image synthesis and identification using diffusion-based generation and facial embeddings.

---

## Project Achievements

The project was presented at multiple academic and technical events and received recognition through various competitions and conferences.

- **INDIACom 2025** — Research paper presentation and publication
- **DIPEX** — Project participation
- **TechThesis / BharatiYugam** — Project participation
- **CODEBITS** — Project participation

Certificates and supporting documentation are available in the repository.

---

## Documentation

### Project Documentation

- [Final Project Report]
- [Final Project Presentation]

### Research Papers

- [Research Paper 1]
- [Research Paper 2]

### Certificates

Project-related competition and conference certificates are available in the repository.

---

## Future Scope

The project can be further extended through:

- Larger and more diverse facial datasets
- Improved text-to-sketch generation quality
- Better representation of fine-grained facial attributes
- Bias and fairness evaluation across demographic groups
- Explainable AI techniques for forensic decision support
- Real-time sketch-to-photo translation
- Improved similarity matching and confidence estimation
- Integration with practical forensic investigation workflows

---

## Disclaimer

This project is an academic and research prototype intended to explore the application of artificial intelligence in forensic investigation.

The generated sketches and similarity results should not be treated as definitive evidence of identity. Real-world forensic applications require rigorous validation, appropriate datasets, expert oversight, and legal and ethical safeguards.


