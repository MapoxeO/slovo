# Slovo – Project Roadmap

This document outlines the planned improvements and future directions for the Slovo Russian Sign Language project.
Items are grouped by theme and ordered roughly from near-term to longer-term goals.

---

## ✅ Done
- [x] Release of the **Slovo dataset** (1,000 classes, 20,400 videos, ~16 GB)
- [x] MediaPipe hand-landmark annotations for every trimmed video
- [x] Baseline models: MViTv2-small, Swin-large, ResNet-i3d (ONNX + TorchScript)
- [x] SignFlow-A – state-of-the-art on WLASL-2000 (63.3 Top-1)
- [x] SignFlow-R – pre-trained on ~50,000 samples with GigaChat integration
- [x] Real-time webcam demo (`demo.py`) with optional multiprocessing
- [x] Jupyter example notebooks (ONNX and TorchScript inference, landmark visualisation)
- [x] Kaggle dataset mirror

---

## 🚧 In Progress / Near-term

### Dataset
- [ ] Expand to **2,000+ gesture classes** with additional recording sessions
- [ ] Add **sentence-level** annotations (sequences of consecutive signs)
- [ ] Improve annotation quality with second-pass review

### Models
- [ ] Publish lighter **mobile-friendly** models (MobileNet-based, <10 MB)
- [ ] Improve best single-model accuracy beyond **65% Top-1** on the full 1 000-class split
- [ ] Add **two-hand** detection prior to the classification backbone

### Tooling
- [ ] Package as a **pip-installable library** (`pip install slovo`)
- [ ] Add a `train.py` script with a reproducible training recipe
- [ ] Provide Docker image for zero-setup inference

---

## 🔭 Mid-term

### Recognition
- [ ] **Continuous sign language recognition** – detect gesture boundaries automatically instead of relying on pre-segmented clips
- [ ] **Sign Language Translation (SLT)** – map gesture sequences to natural Russian sentences
- [ ] Integration with **GigaChat / other LLMs** for context-aware transcription (extending SignFlow-R)

### Dataset
- [ ] Release **3D skeleton** annotations (body pose + hand keypoints per frame)
- [ ] Annotate **facial expressions** relevant to grammatical markers in RSL
- [ ] Collect a dedicated **test-in-the-wild** split recorded outside studio conditions

### Platform
- [ ] **REST API** endpoint for remote inference (FastAPI / gRPC)
- [ ] Lightweight **web demo** (WASM / ONNX.js) – no local install required
- [ ] Native **Android / iOS** demo app

---

## 🌐 Long-term

### Multilingual Sign Language
- [ ] Extend the approach to other sign languages (ASL, BSL, DGS, …) using a shared backbone
- [ ] Cross-lingual transfer learning experiments

### Accessibility
- [ ] Real-time **browser extension** for video-call captioning (e.g. integrations with popular conferencing tools)
- [ ] Open **public leaderboard** on Paperswithcode / Kaggle with standardised evaluation

### Research
- [ ] Publish results of sentence-level recognition experiments
- [ ] Few-shot / zero-shot generalisation to unseen signs
- [ ] Explore **self-supervised pre-training** on unlabelled sign video

---

## 💬 Contributing

Contributions, ideas, and feedback are welcome!
Please open an [issue](https://github.com/hukenovs/slovo/issues) or a pull request on GitHub.
