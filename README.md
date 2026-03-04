# DeepQShield: A Quantum-Resilient Deepfake Detection Framework

A **quantum-resilient deepfake detection system** combining **ResNeXt-based computer vision**, **lattice-based adversarial learning**, and **post-quantum cryptography (PQC)** to create a secure and robust deepfake detection pipeline.

---

# 📄 Research Publication

This project is based on our **peer-reviewed research paper published in Nature Scientific Reports**.

🔗 Paper Link  
https://www.nature.com/articles/s41598-026-38924-7

### Title
**A Quantum-Resilient Deepfake Detection Framework Using Enhanced ResNeXt and Post-Quantum Cryptography Defence**

### Citation

```
Shreeya, K. N., Subburaj, B., Saketh, K. S. G., Padmavathy, T. V.,
Alphonse, S., & Subramanian, G. (2026).
A Quantum-Resilient Deepfake Detection Framework using Enhanced
ResNeXt and Post-Quantum Cryptography Defence.
Scientific Reports (Nature Portfolio).
https://doi.org/10.1038/s41598-026-38924-7
```

If you use this repository in research, please cite the above paper.

---

# 🚀 Overview

Deepfake technology is becoming increasingly sophisticated, making detection systems vulnerable to adversarial manipulation and future quantum threats.

**DeepQShield** addresses these challenges through:

- Deep Learning based detection
- Lattice-based feature transformation
- Post-Quantum Cryptographic protection
- Secure verification of detection outputs

The system ensures **robust deepfake detection with cryptographic integrity**.

---

# 🧠 Key Features

- ResNeXt-based deepfake detection architecture
- Lattice-based adversarial robustness
- Quantum-safe cryptographic verification
- Hybrid classical + PQC security
- Secure inference pipeline
- High detection accuracy (>95%)

---

# 🏗 System Architecture

The detection framework integrates three core modules:

1. Deep Learning Module  
2. Lattice-Enhanced Feature Processing  
3. Post-Quantum Cryptography Security Layer  

Pipeline:

```
Input Image
      ↓
ResNeXt Feature Extraction
      ↓
Lattice-Based Feature Transformation
      ↓
Attention-Based Feature Fusion
      ↓
Classification Head
      ↓
Post-Quantum Cryptographic Verification
      ↓
Secure Detection Result
```

---

# 🔬 Technical Components

## 1. Lattice-Based Learning Module

The **LatticeLayer** introduces structured noise based on **Learning With Errors (LWE)** principles.

```python
class LatticeLayer(nn.Module):
    """
    Implements structured noise addition based on Learning with Errors (LWE)
    - Learnable lattice basis matrix
    - Configurable noise distribution
    - Feature normalization for stability
    """
```

### Benefits

- Improves adversarial robustness  
- Enhances feature diversity  
- Provides regularization similar to dropout  

---

## 2. Advanced ResNeXt Detector

The model architecture includes:

**Backbone**

ResNeXt-50 CNN feature extractor

**Enhancements**

- Lattice feature transformation  
- Attention based feature weighting  
- Feature fusion layers  

**Classifier**

Fully connected classification head with dropout.

---

# 🔐 Post-Quantum Cryptography Module

The project integrates **NIST-standardized PQC algorithms**.

## Kyber-1024

- Key encapsulation mechanism  
- 256-bit quantum security  
- Used for secure key exchange  

## Dilithium-5

- Quantum-safe digital signatures  
- Verification of detection outputs  

## Hybrid Cryptography

Combines:

- Classical cryptography  
- Post-quantum cryptography  

for stronger security.

---

# ⚙ Installation

## Requirements

Python 3.8+

GPU recommended for training.

Check environment:

```
python --version
nvidia-smi
```

---

# 📦 Install Dependencies

```
pip install torch torchvision torchaudio
pip install timm albumentations
pip install numpy pandas scikit-learn
pip install matplotlib seaborn
pip install opencv-python Pillow
pip install liboqs-python cryptography
pip install tqdm
```

Verify installation:

```
python test_pqc.py
```

---

# 📊 Dataset

Primary dataset used:

**140K Real and Fake Faces**

https://www.kaggle.com/datasets/xhlulu/140k-real-and-fake-faces

Alternative datasets supported:

- Celeb-DF (V2)
- FaceForensics++

Dataset format:

```
Final Dataset/
├── real/
├── fake/
└── dataset.csv
```

---

# 🏋 Model Training

Configuration example:

```python
config = Config()
config.data_root = "dataset_path"
config.batch_size = 32
config.num_epochs = 50
config.learning_rate = 1e-4
```

Training:

```python
model = AdvancedResNeXtDeepfakeDetector(config).to(config.device)

trainer = DeepfakeTrainer(model, config)

trainer.train(train_loader, val_loader)
```

---

# 📈 Evaluation

```
test_preds, test_probs, test_targets, test_features = evaluate_model(
    model, test_loader, config.device
)
```

Metrics evaluated:

- Accuracy  
- Precision  
- Recall  
- AUC-ROC  

---

# 🔐 Secure Inference

Example detection with PQC verification.

```python
secure_result = quantum_crypto_manager.secure_detection_result(
    detection_result={"prediction": "fake", "confidence": 0.95},
    image_metadata={"filename": "test.jpg"}
)
```

Verification:

```python
is_valid = quantum_crypto_manager.verify_cryptographic_proof(
    data=secure_result.detection_result,
    proof=secure_result.cryptographic_proof
)
```

---

# 📦 Model Export

Export trained model for deployment.

```python
export_model_for_deployment(model, config)
```

Generated files:

```
complete_model.pth
deepfake_model.onnx
config.json
model_summary.json
```

---

# 📊 Performance

Expected results:

| Metric | Value |
|------|------|
Accuracy | >95% |
AUC-ROC | >0.98 |
Inference Time | ~15–25 ms |

---

# 📁 Project Structure

```
DeepQShield/

deepfakefinal_final.ipynb
pqc.py
test_pqc.py
README.md
```

---

# 👩‍💻 Authors

**Kollipara Naga Shreeya**  
Vellore Institute of Technology, India

**Brindha Subburaj**  
Vellore Institute of Technology, India

**Kollipara Sai Govinda Saketh**  
Vellore Institute of Technology, India

**T V Padmavathy**  
Vellore Institute of Technology, India

**Sherly Alphonse**  
Vellore Institute of Technology, India

**Girish Subramanian**  
Penn State Harrisburg, United States

---

# 📜 License

This project is released for **research and academic purposes**.
