# Z-Image Turbo: Few‑Step Text‑to‑Image Generation

## Overview

**Z-Image Turbo** is a fast **text-to-image diffusion inference project** built on top of the Z-Image architecture. It focuses on generating high-quality images using **only a few denoising steps** to reduce inference latency, making it suitable for interactive applications and large-scale deployment.

This repository focuses on inference usage only — how to run Z‑Image Turbo for text‑to‑image generation, and how its internal pipeline works.

---

## Features

- ⚡ **Fast inference** with very few denoising steps  
- 🧠 **Diffusion Transformer (DiT)** backbone  
- 📝 Strong text understanding via **Qwen3-4B text encoder**  
- 🖼️ High-quality image decoding using **Flux VAE**
- 🔁 Deterministic and stable sampling, ideal for production use
- 🧩 Modular design, easy to integrate with existing diffusion pipelines

---

## Model Pipeline

Below is the end‑to‑end pipeline for text‑to‑image inference using Z‑Image Turbo:
- **Text Prompt**
  ↓
- **Text Encoder (Qwen3-4B)**
  ↓
- **Text Embeddings**
  ↓
- **Gaussian Noise Latents (z_T)**
  ↓
- **Few-Step Diffusion Transformer (Z-Image Turbo)**
  ↓
- **Denoised Latents (z_0)**
  ↓
- **VAE Decoder (Flux VAE)**
  ↓
- **Final RGB Image**

