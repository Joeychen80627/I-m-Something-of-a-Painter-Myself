# Monet Style Image Generation with CycleGAN

This project uses **Generative Adversarial Networks (GANs)** to generate images in the style of **Claude Monet**.  
The goal is to train a model that can produce **7,000 to 10,000** images resembling Monet's paintings in style.

---

## Project Overview

The system consists of:

- A **generator network** that creates Monet-style images  
- A **discriminator network** that evaluates the authenticity of generated images  
- **Adversarial training** where both networks improve together  

### Key Features

- Unsupervised learning (**no class labels needed**)  
- Focuses on **artistic style transfer**  
- Processes **256×256 RGB** images  
- Uses **CycleGAN** architecture for **unpaired image translation**

---

## Dataset

The dataset contains:

- `monet_jpg`: **300 Monet paintings** (JPEG format)  
- `photo_jpg`: **7,038 real-world photos** (JPEG format)  
- `monet_tfrec`: **5 TFRecord files** (same 300 Monet images)  
- `photo_tfrec`: **20 TFRecord files** (~7,038 photos)  

All images are **256×256 pixels** with **RGB** color channels.

---

## Implementation

### Key Components

#### CycleGAN Class
- Handles the complete **GAN training pipeline**  
- Includes **generator** and **discriminator** models  
- Manages the **adversarial training** process  

#### Generator Architecture
- Uses **res**
