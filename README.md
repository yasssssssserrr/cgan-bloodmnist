# Conditional GAN for BloodMNIST

This repo contains the complete solution notebook and assignment sheet for a cGAN trained on **BloodMNIST**. The generator is conditioned on **8 blood-cell classes** and learns to synthesize class-specific 32×32 color images. We evaluate the model via (1) visual inspection, (2) **sample-level metrics** (α-Precision, β-Recall, Authenticity), and (3) **predictive performance** by training a classifier on generated images and testing on real BloodMNIST data.


## Data: BloodMNIST

We use BloodMNIST from MedMNIST v2. The notebook downloads the data via medmnist APIs. Images are resized to 32×32 and provided with class labels:
Basophil, Eosinophil, Erythroblast, Immature Granulocyte, Lymphocyte, Monocyte, Neutrophil, Platelet (8 classes).
## Context
This work is completed as part of CS4332: Modell- und KI-basierte Bildverarbeitung in der Medizin (SoSe 2025), Übungszettel 4. See docs/MoKiBi_P4_Aufgabenblatt.pdf for the official assignment prompt and grading scope.

## How to run

1. Open notebooks/abgabe_praktikum4__Ibourk_Shafieyoun.ipynb (Colab or local GPU).
2. Run the setup cell (installs medmnist etc.).
3. Execute cells in order: Dataset & visualization -> Model definitions (Generator, Discriminator) -> Adversarial training loop -> Evaluation: plots + α-Precision / β-Recall / Authenticity + classifier accuracy.
