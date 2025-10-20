# Multi-Scale-Airplane-Detection-using-YOLO-v8

This repository contains the implementation of a progressive, multi-stage training pipeline for **small and multi-scale object detection** based on **YOLOv8**. The project extends the work of *Dillon et al.* by adapting the pipeline to the **OpenImages V6** dataset with a focus on **tiling, progressive resizing, and test-time augmentation (TTA)** to improve detection accuracy under limited compute conditions.

---

## 🚀 Key Features

- **Progressive Training Pipeline** — multi-stage fine-tuning with increasing image resolutions.  
- **Tiling Preprocessing** — improves visibility and recall of small or distant objects.  
- **Domain Adaptation** — extended to OpenImages V6 subset for generalized aerial-like data.  
- **Test-Time Augmentation (TTA)** — boosts validation performance using geometric and photometric variations.  
- **Reproducible Configuration** — includes YAML-based dataset, augmentation configs, and logged hyperparameters.

---

## 🧠 Novel Contributions

1. **Extension of YOLOv8 to OpenImages V6** — first known experiment of this kind.  
2. **Integrated Tiling Pipeline** — for enhanced small-object detection at high resolution.  
3. **Optimized Hyperparameter Sweep** — for learning rate and weight decay under transfer learning settings.  

---

## 📦 Dataset and Preprocessing

- **Source:** Downloaded 500 labeled images from **FiftyOne Zoo’s OpenImages V6** subset across multiple classes.  
- **Format:** Converted to YOLOv8 format using FiftyOne’s export utilities.  
- **Split:** 400 training, 50 validation, 50 testing images (80/10/10).  
- **Preprocessing:** Tiling, mosaic, cutmix, and progressive resizing augmentations.  

---

## ⚙️ Requirements

### Hardware

| Component | Minimum | Recommended |
|------------|-----------|-------------|
| **GPU** | NVIDIA T4 / RTX 3060 (8GB VRAM) | NVIDIA A100 / RTX 4090 (24GB VRAM) |
| **CPU** | Quad-core | 8-core or higher |
| **RAM** | 12 GB | 32 GB+ |
| **Disk Space** | 10 GB | 30 GB+ |

> ⚠️ **Note:**  
> Experiments were conducted on **Google Colab Pro**, but GPU memory constraints limited large-scale training.  
> The pipeline is GPU-accelerated (PyTorch backend). Training on CPUs is **not recommended**.


---


## 📚 Citation

If you use this work, please cite:

```bibtex
@misc{progressive_yolov8_multiscale_2025,
  title= {Progressive Multi-Scale Object Detection with YOLOv8 and Tiling},
  author= {Hanaanee Hana},
  year={2025},
  howpublished={\url{https://github.com/hanaahh21/Multi-Scale-Airplane-Detection-using-YOLO-v8}},
  note={GitHub repository}
}
```

---

## 🧑‍💻 Author

**Hanaanee Hana**  
Department of Computer Science and Engineering  
University of Moratuwa, Sri Lanka  
