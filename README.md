# FL-NonIID-Benchmark 🚀

<p align="center">
  <a href="https://github.com/noushad999/FL-NonIID-Benchmark">
    <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=1000&color=2463EB&center=true&vCenter=true&width=500&lines=Federated+Learning+Benchmark;FedProx+vs.+FedAvg+Analysis;Quantifying+Privacy+Tradeoffs;Non-IID+Challenge+in+IoT+Anomaly+Detection" alt="Typing SVG">
  </a>
</p>

<p align="center">
  <a href="https://colab.research.google.com/github/noushad999/FL-NonIID-Benchmark/blob/main/FL_NonIID_Benchmark.ipynb">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab">
  </a>
  <img src="https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/PyTorch-2.0-EE4C2C?logo=pytorch&logoColor=white">
  <img src="https://img.shields.io/github/license/noushad999/FL-NonIID-Benchmark?style=flat">
  <img src="https://img.shields.io/github/repo-size/noushad999/FL-NonIID-Benchmark">
  <a href="http://makeapullrequest.com">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square">
  </a>
</p>

---

## 📚 Overview

**FL-NonIID-Benchmark** is a privacy-preserving AI system for cyber-attack detection in IoT (Internet of Things) networks.  
It **benchmarks Federated Learning (FL) algorithms** on *realistic, non-IID distributed data*, asking:

> **When does the robust [`FedProx`] algorithm actually outperform the classic [`FedAvg`]? What performance do we trade for better privacy?**

---

## 🔍 Visualizing the Non-IID Challenge

Watch **FedProx** (Green) thrive where **FedAvg** (Red) struggles ($\alpha=0.1$, extreme Non-IID):

<p align="center">
  <img src="images/training_comparison.gif" alt="Live Training Comparison" width="700">
</p>

---

## 🌟 Key Findings

| Category | Discovery | Impact |
|:---------|:----------|:-------|
| 🏆 **Benchmark**      | Centralized **XGBoost (F1 0.9962)** outperforms Deep Learning | Sets the “Gold Standard” baseline |
| 💸 **Cost of Privacy**| FL’s `FedAvg` drops to **F1 0.9388** | ~5.74% performance loss for privacy |
| 📈 **Tipping Point**  | `FedProx` *only* wins at **α = 0.1** (extreme Non-IID) | Shows `FedProx` is only optimal at extreme skew |
| 🐞 **Failure**        | `FedProx` crashes (*F1 0.00*) at moderate skew (α=0.5) | Indicates strong hyperparameter sensitivity |

---

## 🛠 Tech Stack

<p align="center">
  <img src="https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white">
  <img src="https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white">
  <img src="https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white">
  <img src="https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white">
  <img src="https://img.shields.io/badge/XGBoost-%23EB4C4C.svg?style=for-the-badge&logo=xgboost&logoColor=white">
</p>

---

## 🚀 Quick Start

### ▶️ Option 1: Google Colab (Recommended)

Run everything (including animations) instantly in your browser:

<p align="center">
  <a href="https://colab.research.google.com/github/noushad999/FL-NonIID-Benchmark/blob/main/FL_NonIID_Benchmark.ipynb">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open in Colab" height="38">
  </a>
</p>

---

### 💻 Option 2: Local Installation

```bash
# 1. Clone the repository
git clone https://github.com/noushad999/FL-NonIID-Benchmark.git
cd FL-NonIID-Benchmark

# 2. Create & activate a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the benchmark notebook (download dataset as per notebook instructions)
jupyter notebook FL_NonIID_Benchmark.ipynb
```

---

## 📂 Project Structure

<details>
<summary>Click to expand directory tree</summary>

```
FL-NonIID-Benchmark/
│
├── FL_NonIID_Benchmark.ipynb   # 🧠 Core notebook
├── requirements.txt            # 📦 Dependencies
├── .gitignore                  # 🚫 Ignored files
├── LICENSE                     # 📜 MIT License
├── README.md                   # 🏠 This file
└── images/                     # 🎨 Visual assets
    └── training_comparison_fixed.gif
```
</details>

---

## 📜 Citation

If you use our benchmark, please cite:

```bibtex
@misc{Noushad2025FLBenchmark,
  author = {Noushad Jahan Ramim},
  title  = {A Novel Benchmark of Federated Learning for Non-IID Anomaly Detection},
  year   = {2025},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/noushad999/FL-NonIID-Benchmark}}
}
```

---

## 🤝 Contributing & Feedback

- **Found a bug?** [Open an Issue](https://github.com/noushad999/FL-NonIID-Benchmark/issues).
- **Feature/Idea?** [Fork & Pull Request](https://github.com/noushad999/FL-NonIID-Benchmark/pulls).
- **Say hi:** [Connect on LinkedIn](https://www.linkedin.com/in/ramim-noushad).

---

<p align="center">
  <sub>
    Built with ❤️ by <a href="https://github.com/noushad999" target="_blank">Noushad Jahan Ramim</a> using PyTorch & XGBoost.
  </sub>
</p>
