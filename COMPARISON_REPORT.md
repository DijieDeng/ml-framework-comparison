# Machine Learning Framework Comparison Report

> **TensorFlow · PyTorch · scikit-learn · Keras**

This report compares four of the most popular open-source machine learning frameworks across feature sets, installation methods, supported APIs, and GitHub activity metrics. Data was gathered from each framework's official documentation website and its primary GitHub repository.

---

## Table of Contents

1. [Executive Summary](#1-executive-summary)
2. [GitHub Statistics Overview](#2-github-statistics-overview)
3. [TensorFlow](#3-tensorflow)
4. [PyTorch](#4-pytorch)
5. [scikit-learn](#5-scikit-learn)
6. [Keras](#6-keras)
7. [Feature Comparison Matrix](#7-feature-comparison-matrix)
8. [Installation Guide Comparison](#8-installation-guide-comparison)
9. [Recent Commit Activity](#9-recent-commit-activity)
10. [Open Issues Snapshot](#10-open-issues-snapshot)
11. [Recommendations](#11-recommendations)

---

## 1. Executive Summary

| Attribute | TensorFlow | PyTorch | scikit-learn | Keras |
|---|---|---|---|---|
| **GitHub Repo** | tensorflow/tensorflow | pytorch/pytorch | scikit-learn/scikit-learn | keras-team/keras |
| **Stars** | 196,124 | 101,559 | 66,536 | 64,154 |
| **Forks** | 75,336 | 28,289 | 27,139 | 19,756 |
| **Primary Language** | C++ | Python | Python | Python |
| **License** | Apache-2.0 | BSD-style | BSD-3-Clause | Apache-2.0 |
| **Latest Stable** | 2.21.0 (ref. from issues) | 2.7.0 | 1.9.1 | 3.x |
| **Primary Use Case** | End-to-end ML platform (research + production) | Deep learning research + production | Classical ML algorithms | High-level deep learning API |
| **Multi-Backend** | No (native) | No (native) | N/A | Yes (JAX, TF, PyTorch, OpenVINO) |
| **Open Issues** | ~693 | ~14,050 | 1+ (recent) | 1+ (recent) |

---

## 2. GitHub Statistics Overview

### Repository Comparison

| Metric | TensorFlow | PyTorch | scikit-learn | Keras |
|---|---|---|---|---|
| **Stars** ⭐ | 196,124 | 101,559 | 66,536 | 64,154 |
| **Forks** 🍴 | 75,336 | 28,289 | 27,139 | 19,756 |
| **License** | Apache-2.0 | BSD-style | BSD-3-Clause | Apache-2.0 |
| **Website** | [tensorflow.org](https://tensorflow.org) | [pytorch.org](https://pytorch.org) | [scikit-learn.org](https://scikit-learn.org) | [keras.io](https://keras.io) |

### Star Count Ranking

1. **TensorFlow** — 196,124 stars (highest)
2. **PyTorch** — 101,559 stars
3. **scikit-learn** — 66,536 stars
4. **Keras** — 64,154 stars

---

## 3. TensorFlow

### Overview

TensorFlow is an end-to-end open source platform for machine learning, originally developed by Google Brain. It provides a comprehensive ecosystem of tools, libraries, and community resources for both researchers and production developers.

### Feature Set

- **End-to-end ML platform**: From data preprocessing to model deployment
- **TensorFlow.js**: Train and run models directly in the browser using JavaScript or Node.js
- **LiteRT (formerly TensorFlow Lite)**: Deploy ML on mobile and edge devices (Android, iOS, Raspberry Pi, Edge TPU)
- **tf.data**: Preprocess data and create input pipelines for ML models
- **TFX (TensorFlow Extended)**: Production ML pipelines and MLOps best practices
- **tf.keras**: TensorFlow's high-level API for model building
- **TensorFlow Datasets**: Standard datasets for training and validation
- **TensorBoard**: Visualization and tracking of ML model development
- **TensorFlow GNN**: Graph neural networks for relational data analysis
- **TensorFlow Agents**: Reinforcement learning for recommendation systems
- **Kaggle Models**: Pre-trained models for fine-tuning and deployment

### Supported APIs

- **Python** (stable, backward-compatible)
- **C++** (stable, backward-compatible)
- **Other languages** (non-guaranteed backward compatibility)

### Installation Guide

```bash
# Full installation with CUDA GPU support (Ubuntu and Windows)
pip install tensorflow

# CPU-only package
pip install tensorflow-cpu

# Nightly builds
pip install tf-nightly        # GPU
pip install tf-nightly-cpu    # CPU-only
```

Additional installation options:
- **Docker containers**: Supported for containerized deployments
- **Build from source**: For custom configurations
- **Device plugins**: DirectX and macOS Metal support via plugins
- **Upgrade**: Add `--upgrade` flag to update

### Documentation Highlights (from tensorflow.org)

- Interactive code samples and tutorials
- Multi-language documentation (English, Spanish, French, Portuguese, Chinese, Japanese, Korean)
- Web AI Summit content for client-side model execution
- Community forum, YouTube, LinkedIn, and X (Twitter) presence

---

## 4. PyTorch

### Overview

PyTorch is a Python package providing tensor computation with strong GPU acceleration and deep neural networks built on a tape-based autograd system. It is maintained by the PyTorch Foundation and emphasizes flexibility, speed, and a Python-first design.

### Feature Set

- **GPU-ready tensor library**: NumPy-like tensors with GPU acceleration
- **Dynamic neural networks**: Tape-based autograd for flexible model building
- **Python-first**: Deeply integrated into Python; use with NumPy, SciPy, Cython, Numba
- **Imperative execution**: Intuitive, linear code execution with clear stack traces
- **Fast and lean**: Integrates Intel MKL, NVIDIA cuDNN, and NCCL for speed
- **Production ready**: TorchScript for seamless eager-to-graph transitions; TorchServe for deployment
- **Distributed training**: torch.distributed backend for scalable multi-GPU/multi-node training
- **Robust ecosystem**: Captum (model interpretability), PyTorch Geometric (graph learning), skorch (scikit-learn compatibility)
- **Cloud support**: AWS, Google Cloud, Azure, Lightning Studios, Alibaba Cloud

### Supported APIs / Components

| Component | Description |
|---|---|
| `torch` | Tensor library like NumPy with strong GPU support |
| `torch.autograd` | Tape-based automatic differentiation |
| `torch.jit` | TorchScript compilation stack for serializable/optimizable models |
| `torch.nn` | Neural networks library deeply integrated with autograd |
| `torch.multiprocessing` | Python multiprocessing with shared memory for tensors |
| `torch.utils` | DataLoader and utility functions |

**Languages**: Python (primary), C++/Java (via LibTorch)

### Installation Guide

```bash
# Stable release with CUDA 11.8
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118

# CPU-only
pip3 install torch torchvision torchaudio
```

Install options:
- **Build**: Stable (2.7.0) or Preview (Nightly)
- **OS**: Linux, macOS, Windows
- **Package**: pip, LibTorch (C++), Source
- **Compute Platform**: CUDA 11.8, CUDA 12.6, CUDA 12.8, ROCm 6.3, CPU
- **Docker**: `docker run --gpus all --rm -ti --ipc=host pytorch/pytorch:latest`
- **From source**: Requires Python 3.10+, C++20 compiler, 10 GB disk space
- **Previous versions**: Available at [pytorch.org/get-started/previous-versions](https://pytorch.org/get-started/previous-versions)

### Documentation Highlights (from pytorch.org)

- Interactive install selector (OS, package, language, compute platform)
- Quick start with cloud partners (AWS, GCP, Azure, Alibaba Cloud, Lightning Studios)
- PyTorch Conference announcements and community events
- PyTorch Certification program
- Landscape project browser for ecosystem tools

---

## 5. scikit-learn

### Overview

scikit-learn is a Python module for machine learning built on top of SciPy, distributed under the 3-Clause BSD license. Started in 2007 as a Google Summer of Code project, it is maintained by a team of volunteers and is the go-to library for classical ML algorithms.

### Feature Set

- **Classification**: Spam detection, image recognition — Gradient boosting, nearest neighbors, random forest, logistic regression, and more
- **Regression**: Drug response, stock prices — Gradient boosting, nearest neighbors, random forest, ridge, and more
- **Clustering**: Customer segmentation — k-Means, HDBSCAN, hierarchical clustering, and more
- **Dimensionality reduction**: Visualization, efficiency — PCA, feature selection, NMF, and more
- **Model selection**: Grid search, cross-validation, metrics, parameter tuning
- **Preprocessing**: Feature extraction, normalization, text transformation

### Key Characteristics

- Simple and efficient tools for predictive data analysis
- Accessible to everybody and reusable in various contexts
- Built on NumPy, SciPy, and matplotlib
- Open source, commercially usable (BSD license)
- Latest stable version: **1.9.1** (September 2026)

### Supported APIs

- **Python** (primary and only)
- Consistent `fit` / `predict` / `transform` API across all estimators
- Pipeline API for chaining preprocessing and modeling steps
- Plotting capabilities (functions starting with `plot_`, classes ending with `Display`)

### Installation Guide

```bash
# Via pip
pip install -U scikit-learn

# Via conda
conda install -c conda-forge scikit-learn
```

**Dependencies**:
- Python >= 3.11
- NumPy >= 1.24.1
- SciPy >= 1.10.0
- Narwhals >= 2.0.1
- joblib >= 1.4.0
- threadpoolctl >= 3.5.0

**Optional dependencies** (for examples/plotting):
- Matplotlib >= 3.6.1
- scikit-image >= 0.22.0
- pandas >= 1.5.0
- seaborn >= 0.13.0
- Plotly >= 5.22.0

### Documentation Highlights (from scikit-learn.org)

- Stable and development version documentation
- Release highlights with visual examples
- Extensive example gallery organized by ML task
- FAQ and community support channels (Discord, Stack Overflow, GitHub Discussions)
- Active social media presence (LinkedIn, YouTube, Bluesky, Mastodon)

---

## 6. Keras

### Overview

Keras 3 is a multi-backend deep learning framework designed for human beings, not machines. It supports JAX, TensorFlow, PyTorch, and OpenVINO (inference-only), allowing developers to build and train models that can move seamlessly across frameworks.

### Feature Set

- **Multi-backend architecture**: Run on JAX, TensorFlow, PyTorch, or OpenVINO (inference-only)
- **Accelerated model development**: High-level UX with easy-to-debug runtimes
- **State-of-the-art performance**: 20–350% speedups by choosing the optimal backend
- **Datacenter-scale training**: Scale from laptop to GPU/TPU clusters
- **KerasHub**: Pre-trained model architectures (Gemma, Llama, Stable Diffusion, Mistral) with checkpoints on Kaggle Models
- **Functional API**: Build models using functional building patterns
- **Built-in training & evaluation**: `model.fit()`, `model.compile()`, `model.evaluate()`
- **Custom layers via subclassing**: Extend Keras layers for custom architectures
- **Domain coverage**: Computer vision, NLP, generative deep learning (diffusion models, GANs, transformers)
- **Backwards compatibility**: Drop-in replacement for `tf.keras`

### Supported APIs / Backends

| Backend | Minimum Supported Version | Use Case |
|---|---|---|
| TensorFlow | >= 2.16.1 | Full training + inference |
| JAX | >= 0.4.20 | Full training + inference (often fastest) |
| PyTorch | >= 2.1.0 | Full training + inference |
| OpenVINO | >= 2025.3.0 | Inference-only |

**Primary language**: Python

### Installation Guide

```bash
# Step 1: Install Keras
pip install keras --upgrade

# Step 2: Install a backend (choose one)
pip install tensorflow   # TensorFlow backend
pip install jax         # JAX backend
pip install torch       # PyTorch backend
```

**Configuring the backend**:
```bash
# Via environment variable
export KERAS_BACKEND="jax"

# Or via config file at ~/.keras/keras.json
```

Additional notes:
- **GPU support**: Use `requirements-{backend}-cuda.txt` files for CUDA dependencies
- **Local development**: `pip install -r requirements.txt && python pip_build.py --install`
- **Windows**: WSL2 recommended
- **Note**: Backend must be configured *before* importing `keras`

### Documentation Highlights (from keras.io)

- API documentation, developer guides, and code examples
- Quickstart notebooks (Google Colab integration)
- KerasHub model documentation (Gemma, Llama, Stable Diffusion, Mistral)
- Roadmap and contribution guide on GitHub
- Community meetings, Discord, and Google AI forum
- Used by CERN, NASA, NIH, Waymo

---

## 7. Feature Comparison Matrix

| Feature | TensorFlow | PyTorch | scikit-learn | Keras |
|---|---|---|---|---|
| **Deep Learning** | ✅ Full | ✅ Full | ❌ | ✅ Full |
| **Classical ML** | ⚠️ Limited | ⚠️ Limited | ✅ Full | ❌ |
| **GPU Support** | ✅ CUDA, Metal, DirectX | ✅ CUDA, ROCm, MPS | ❌ CPU-only | ✅ (via backends) |
| **Distributed Training** | ✅ | ✅ torch.distributed | ❌ | ✅ (via backends) |
| **Mobile/Edge Deployment** | ✅ LiteRT | ✅ ExecuTorch | ❌ | ⚠️ (via backends) |
| **Web/Browser** | ✅ TensorFlow.js | ❌ | ❌ | ❌ |
| **Graph Neural Networks** | ✅ TF GNN | ✅ PyG | ❌ | ⚠️ |
| **Reinforcement Learning** | ✅ TF Agents | ⚠️ (via ecosystem) | ❌ | ⚠️ |
| **Model Interpretability** | ⚠️ | ✅ Captum | ⚠️ | ⚠️ |
| **Production Pipelines** | ✅ TFX | ✅ TorchServe | ❌ | ⚠️ |
| **Visualization** | ✅ TensorBoard | ⚠️ | ✅ Built-in plotting | ⚠️ |
| **Multi-Backend** | ❌ | ❌ | N/A | ✅ JAX/TF/PyTorch/OpenVINO |
| **Dynamic Computation Graph** | ⚠️ (eager mode) | ✅ Native | N/A | ⚠️ (via backends) |
| **Python API** | ✅ Stable | ✅ Native | ✅ Native | ✅ Native |
| **C++ API** | ✅ Stable | ✅ LibTorch | ❌ | ❌ |
| **Java API** | ⚠️ | ⚠️ | ❌ | ❌ |

---

## 8. Installation Guide Comparison

| Aspect | TensorFlow | PyTorch | scikit-learn | Keras |
|---|---|---|---|---|
| **pip install** | `pip install tensorflow` | `pip3 install torch torchvision torchaudio` | `pip install -U scikit-learn` | `pip install keras --upgrade` + backend |
| **conda install** | ⚠️ (community) | ✅ | `conda install -c conda-forge scikit-learn` | ⚠️ |
| **CPU-only option** | ✅ `tensorflow-cpu` | ✅ (default CPU wheel) | ✅ (CPU-only by design) | ✅ (via backend) |
| **GPU support** | ✅ CUDA (pip) | ✅ CUDA, ROCm (index-url) | ❌ | ✅ (via backend + CUDA reqs) |
| **Docker** | ✅ | ✅ | ⚠️ | ⚠️ |
| **Build from source** | ✅ | ✅ | ✅ | ✅ |
| **Nightly builds** | ✅ tf-nightly | ✅ Preview builds | ✅ Nightly wheels | ⚠️ |
| **Min Python version** | 3.10+ (ref.) | 3.10+ | 3.11+ | 3.10+ (ref.) |
| **Cloud platforms** | ✅ GCP, AWS, Azure | ✅ AWS, GCP, Azure, Alibaba | ❌ | ⚠️ (via backends) |
| **Package size** | Large | Large | Medium | Small (+ backend) |

---

## 9. Recent Commit Activity

### TensorFlow (tensorflow/tensorflow) — Latest commits as of Aug 22, 2026

| SHA | Message | Author |
|---|---|---|
| 63f4e71 | Merge PR #125581: fix/dtensor-collective-key-cache-lock | TensorFlower Gardener |
| 57ab3a6 | Automated Code Change | A. Unique TensorFlower |
| 1e139c2 | Automated Code Change | A. Unique TensorFlower |
| 9cf2d0c | Add GetEventOrMetadataStat to XEventVisitor | A. Unique TensorFlower |
| a1abd9e | Automated Code Change | A. Unique TensorFlower |

### PyTorch (pytorch/pytorch) — Latest commits as of Sep 13, 2026

| SHA | Message | Author |
|---|---|---|
| b8bd7cf | Revert "Fix operator benchmark CUDA timing double count (#192331)" | PyTorch MergeBot |
| 34219e6 | [BE] Update NVTX submodule to v3.6.0 (#196618) | Aaron Gokaslan |
| 58fbd57 | [BE] Update mimalloc submodule to 2.5.2 (#196623) | Aaron Gokaslan |
| f3d3b37 | [MPS] Add float8_e4m3fn support to eye (#196915) | Isalia20 |
| e1b01c2 | [dynamo] Skip already-bound name when installing a global (#196822) | Bob Ren |

### scikit-learn (scikit-learn/scikit-learn) — Latest commits as of Sep 11–12, 2026

| SHA | Message | Author |
|---|---|---|
| dd3ca57 | DOC/CI Speed up plot_randomized_search.py example (#34944) | Jérémie du Boisberranger |
| 91c6d0e | CI Speed-up doc builds (#34936) | Jérémie du Boisberranger |
| 7eec52f | DOC Add new members to contributor experience team (#34931) | Stefanie Senger |
| e015b7a | MNT Update SECURITY.md after 1.9.1 (#34930) | Jérémie du Boisberranger |
| 3dfd201 | DOC Tweak git shortlog command for release contributors (#34906) | Loïc Estève |

### Keras (keras-team/keras) — Latest commits as of Sep 15, 2026

| SHA | Message | Author |
|---|---|---|
| 62b89e1 | numpy.testing assert functions (#23605) | hertschuh |
| f3b31e4 | fix: R2Score returns NaN for zero-variance data (#23420) | Gaurav Gandhi |
| a1d33cc | fix(torch): slice() preserves dynamic dims under torch.export (#23190) | RAHUL KUMAR |
| 56eb6cf | Dot scale attention compatible with dtensor (#23403) | Suhana |
| a718e34 | Warn when OrbaxCheckpoint fails to finalize checkpoints (#23610) | Gargi Gupta |

---

## 10. Open Issues Snapshot

### TensorFlow — ~693 open issues total

| # | Title | Labels | Created |
|---|---|---|---|
| 127346 | Large CPU/GPU numerical discrepancy in tf.linalg.matmul for float32 | type:bug | 2026-09-14 |
| 127290 | [Feature Request] Fused Linear Cross-Entropy API in tf.nn | type:feature, comp:apis | 2026-09-12 |
| 127249 | tf.keras.metrics.categorical_crossentropy wrong class count for label smoothing | type:bug, comp:keras | 2026-09-11 |
| 127248 | tf.keras.ops.numpy.rot90 returns incorrect values for two rotations | type:bug, comp:ops | 2026-09-11 |
| 127247 | tf.keras.ops.image.gaussian_blur swaps height and width sigma | type:bug, comp:ops | 2026-09-11 |

### PyTorch — ~14,050 open issues total

| # | Title | Labels | Created |
|---|---|---|---|
| 197144 | DISABLED test_package_keeps_a_loaded_device_a_recompile | module: xpu, skipped | 2026-09-15 |
| 197121 | [CUDA] Add scalar scatter kernel for fp8 | module: cuda, enhancement | 2026-09-15 |
| 197112 | [fake tensor] torch.abs complex out dtype mismatch under torch.compile | module: complex, oncall: pt2 | 2026-09-15 |
| 197110 | [dynamo] str(KeyError) quotes behavior difference in compiled code | module: dynamo, oncall: pt2 | 2026-09-15 |
| 197109 | [inductor] F.channel_shuffle drops channels_last memory format | module: inductor, oncall: pt2 | 2026-09-15 |

### scikit-learn — Recent open issues

| # | Title | Labels | Created |
|---|---|---|---|
| 34964 | Cannot get development Codespace into intended environment | Bug, Needs Triage | 2026-09-15 |

### Keras — Recent open issues

| # | Title | Labels | Created |
|---|---|---|---|
| 23638 | soft_shrink, sparse_plus and selu mangle integer inputs (multi-backend inconsistency) | backend:torch, backend:tensorflow, backend:jax, backend:OpenVino | 2026-09-15 |

---

## 11. Recommendations

### Choose TensorFlow if you:
- Need an end-to-end ML platform with production-grade tooling (TFX, TensorBoard)
- Want to deploy models to web (TensorFlow.js), mobile/edge (LiteRT)
- Are working in a Google Cloud-centric environment
- Need stable Python and C++ APIs

### Choose PyTorch if you:
- Prioritize research flexibility with dynamic computation graphs
- Want a Python-first, intuitive development experience
- Need distributed training at scale (torch.distributed)
- Work with CUDA or AMD ROCm GPUs
- Want the richest ecosystem for cutting-edge research (Captum, PyG, skorch)

### Choose scikit-learn if you:
- Work with classical machine learning algorithms (classification, regression, clustering, dimensionality reduction)
- Need a simple, consistent API (`fit` / `predict` / `transform`)
- Want a lightweight, CPU-based library with minimal dependencies
- Are doing data preprocessing, model selection, or feature engineering

### Choose Keras if you:
- Want a high-level, human-friendly API for deep learning
- Need multi-backend flexibility (JAX, TensorFlow, PyTorch, OpenVINO)
- Want to avoid framework lock-in and future-proof your code
- Need pre-trained models via KerasHub (Gemma, Llama, Stable Diffusion, Mistral)
- Prefer concise, readable, easy-to-debug code

### Combining Frameworks

Many teams use multiple frameworks together:
- **scikit-learn + PyTorch/TF**: Use scikit-learn for preprocessing and classical baselines, then deep learning frameworks for neural models
- **Keras + JAX**: Use Keras 3 as the high-level API on top of JAX for maximum performance
- **PyTorch + scikit-learn**: Use `skorch` for scikit-learn-compatible PyTorch models
- **TensorFlow + Keras**: Keras is bundled as `tf.keras` in TensorFlow for the high-level API

---

## Data Collection Methodology

All data in this report was collected via:
1. **Web scraping** of official documentation sites (tensorflow.org, pytorch.org, scikit-learn.org/stable, keras.io)
2. **GitHub REST API** for repository metadata, commit history, and issue tracking
3. Data reflects the state at the time of collection (see commit date of this file)

---

_This report is for informational purposes. Always refer to official documentation for the most up-to-date information._
