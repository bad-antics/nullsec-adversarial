<div align="center">

# 🧠 NullSec Adversarial

### Adversarial Machine Learning Attack Toolkit

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)]()
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)]()
[![NullSec](https://img.shields.io/badge/NullSec-Linux_v5.0-00ff41?style=for-the-badge&logo=linux&logoColor=white)](https://github.com/bad-antics/nullsec-linux)

*Evasion, poisoning, and extraction attacks against ML models*

</div>

---

## 🎯 Overview

NullSec Adversarial is a comprehensive toolkit for testing machine learning model robustness. It implements state-of-the-art adversarial attacks — evasion (FGSM, PGD, C&W, AutoAttack), model extraction, membership inference, and model inversion — across image classifiers, NLP models, and tabular ML pipelines.

## ⚡ Features

| Feature | Description |
|---------|-------------|
| **Evasion Attacks** | FGSM, PGD, C&W, DeepFool, AutoAttack |
| **Model Extraction** | Query-based model stealing with knockoff networks |
| **Membership Inference** | Determine if a sample was in training data |
| **Model Inversion** | Reconstruct training data from model outputs |
| **Transferability** | Generate transferable adversarial examples |
| **Defence Evaluation** | Test adversarial training, certified defences |
| **Framework Support** | PyTorch, TensorFlow, scikit-learn, ONNX |

## �� Attack Matrix

| Attack | Type | Domain | Threat Model |
|--------|------|--------|--------------|
| FGSM | Evasion | Image/NLP | White-box |
| PGD | Evasion | Image/NLP | White-box |
| C&W | Evasion | Image | White-box |
| AutoAttack | Evasion | Image | White-box |
| HopSkipJump | Evasion | Image | Black-box |
| Knockoff Nets | Extraction | Any | Black-box |
| Shadow Models | Membership | Any | Black-box |
| MI-FACE | Inversion | Image | White-box |

## 🚀 Quick Start

```bash
# Run PGD evasion attack on an image classifier
nullsec-adversarial evasion pgd --model resnet50.onnx --input samples/ --eps 0.03

# Black-box model extraction
nullsec-adversarial extract --target-url http://api.example.com/predict --queries 10000

# Membership inference attack
nullsec-adversarial membership --model target.pt --members train.csv --non-members test.csv

# Evaluate adversarial robustness
nullsec-adversarial benchmark --model model.pt --dataset cifar10 --attacks all
```

## 🔗 Related Projects

| Project | Description |
|---------|-------------|
| [nullsec-llmred](https://github.com/bad-antics/nullsec-llmred) | LLM red-teaming framework |
| [nullsec-datapoisoning](https://github.com/bad-antics/nullsec-datapoisoning) | Training data poisoning detection |
| [nullsec-modelaudit](https://github.com/bad-antics/nullsec-modelaudit) | ML model security auditing |
| [nullsec-promptinject](https://github.com/bad-antics/nullsec-promptinject) | Prompt injection payloads |
| [nullsec-linux](https://github.com/bad-antics/nullsec-linux) | Security Linux distro (140+ tools) |

## ⚠️ Legal

For **authorized ML security testing only**. Do not use against models or systems without explicit permission.

## 📜 License

MIT License — [@bad-antics](https://github.com/bad-antics)

---

<div align="center">

*Part of the [NullSec AI/ML Security Suite](https://github.com/bad-antics)*

</div>
