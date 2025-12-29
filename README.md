# Neural-Image-Caption-Generator

An end-to-end deep learning model for automatically generating captions for images using a CNN-LSTM encoder-decoder architecture implemented through TensorFlow Keras.

## Architecture Overview

[[paper](https://arxiv.org/abs/1608.06993)] **DenseNet201** - Pre-trained DenseNet201 as the image encoder  
[[paper](https://arxiv.org/abs/2105.06756)] **LSTM** - LSTM network as the caption decoder  

**Dataset** - **Flickr30k** 31,783 images with 158,915 captions (5 per image)  
**Train/Test split** - 85% / 15%  
**Vocabulary size** - 8,001 unique words  

---

## 📦 Model Files

| File | Description |
|------|-------------|
| `model.keras` | Trained caption generation model (LSTM decoder) |
| `tokenizer.pkl` | Fitted tokenizer with vocabulary (8,001 words) |
| `feature_extractor.keras` | DenseNet201 feature extractor (frozen weights) |
| `ESRGAN-SuperResolution-Images.ipynb` | Image enhancement for low-resolution inputs |

---

### ESRGAN Enhancement 
[ESRGAN](https://github.com/xinntao/Real-ESRGAN)
Upscales low-resolution images (2x/4x) to improve feature extraction quality and caption accuracy (for images <256px)

## Training metrics: 
<img width="1208" height="524" alt="Architecture Diagram" src="https://github.com/user-attachments/assets/a5f775b0-efd3-4470-af6a-ba9031803a21" />
