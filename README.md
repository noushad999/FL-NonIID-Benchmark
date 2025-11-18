# FL-NonIID-Benchmark

<div align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=1000&color=2463EB&center=true&vCenter=true&width=500&lines=Federated+Learning+Benchmark;FedProx+vs.+FedAvg+Analysis;Quantifying+the+Cost+of+Privacy;Robustness+on+Non-IID+Data" alt="Typing SVG" />
  </a>
</div>

<div align="center">

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/noushad999/FL-NonIID-Benchmark/blob/main/FL_NonIID_Benchmark.ipynb)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0-EE4C2C?logo=pytorch&logoColor=white)
![License](https://img.shields.io/github/license/noushad999/FL-NonIID-Benchmark?style=flat)
![Repo Size](https://img.shields.io/github/repo-size/noushad999/FL-NonIID-Benchmark)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

</div>

---

## 📖 Overview
This repository hosts the official implementation of the research: **"Quantifying the Cost of Privacy: A Benchmark of Federated vs. Centralized Learning for Non-IID Anomaly Detection."**

The goal is to stress-test Federated Learning (FL) algorithms against the harsh reality of **Non-IID (Non-Identical and Independently Distributed)** data in IoT networks. We answer:
> *When does the robust `FedProx` algorithm actually beat the standard `FedAvg`, and what performance do we sacrifice for privacy?*

---

## 📊 Visualizing the Challenge

### The "Tipping Point" (Live Training)
Watch how **FedProx** (Green) successfully learns in an extreme Non-IID environment ($\alpha=0.1$), while the standard **FedAvg** (Red) struggles to converge.

<p align="center">
  <img src="images/training_comparison_fixed.gif" alt="Live Training Comparison" width="700">
</p>

---

## 💡 Key Research Findings (The "Novelty")

Our comprehensive benchmark on the **TON_IoT** dataset revealed three critical insights often overlooked in standard literature:

| Finding Category | Discovery | Impact |
| :--- | :--- | :--- |
| **🏆 The Benchmark** | Centralized **XGBoost (F1 0.9962)** beats all Deep Learning models. | Establishes the true "Gold Standard". |
| **💸 Cost of Privacy** | FL (`FedAvg`) drops to **F1 0.9388** vs Centralized. | Privacy costs **~5.74%** performance loss. |
| **📈 The Tipping Point** | `FedProx` only wins at **$\alpha=0.1$** (Extreme Non-IID). | Shows `FedProx` is a specialized tool, not universal. |
| **🐞 Failure Analysis** | `FedProx` crashes (**F1 0.00**) at moderate skew ($\alpha=0.5$). | Highlights critical hyperparameter sensitivity. |

---

## 🛠️ Tech Stack
This project is built using industry-standard tools for reproducibility and performance.

![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-%23EB4C4C.svg?style=for-the-badge&logo=xgboost&logoColor=white)

---

## 🚀 Quick Start

### Option 1: Google Colab (Recommended)
The fastest way to reproduce the results (including the animations) is to run the notebook directly in the browser.

<a href="https://colab.research.google.com/github/noushad999/FL-NonIID-Benchmark/blob/main/FL_NonIID_Benchmark.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab" height="30"/>
</a>

### Option 2: Local Installation
If you prefer running it locally:

```bash
# 1. Clone the repository
git clone [https://github.com/noushad999/FL-NonIID-Benchmark.git](https://github.com/noushad999/FL-NonIID-Benchmark.git)
cd FL-NonIID-Benchmark

# 2. Create and activate a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the benchmark
# Note: Ensure the dataset is downloaded as per the notebook instructions
jupyter notebook FL_NonIID_Benchmark.ipynb
````

-----

## 📂 Project Structure

\<details\>
\<summary\>Click to expand directory tree\</summary\>

```
FL-NonIID-Benchmark/
│
├── FL_NonIID_Benchmark.ipynb   # 🧠 The Core Logic (Colab Notebook)
├── requirements.txt            # 📦 Dependencies
├── .gitignore                  # 🚫 Ignored files
├── LICENSE                     # 📜 MIT License
├── README.md                   # 🏠 Home Page
│
└── images/                     # 🎨 Assets
    ├── training_comparison_fixed.gif
    └── findings_table.png
```

\</details\>

-----

## 📜 Citation

If you find this benchmark useful for your research, please consider citing:

```bibtex
@misc{Noushad2025FLBenchmark,
  author = {Noushad Jahan Ramim},
  title  = {A Novel Benchmark of Federated Learning for Non-IID Anomaly Detection},
  year   = {2025},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{[https://github.com/noushad999/FL-NonIID-Benchmark](https://github.com/noushad999/FL-NonIID-Benchmark)}}
}
```

-----

## 🤝 Contributing & Feedback

I actively welcome feedback from the research community\!

  * **Found a bug?** Open an [Issue](https://www.google.com/search?q=https://github.com/noushad999/FL-NonIID-Benchmark/issues).
  * **Have an idea?** Fork the repo and submit a Pull Request.
  * **Just want to say hi?** Connect with me on [LinkedIn](https://linkedin.com/in/your-profile).

-----

\<div align="center"\>
\<sub\>Built with ❤️ by \<a href="https://www.google.com/search?q=https://github.com/noushad999"\>Noushad Jahan Ramim\</a\> using PyTorch & XGBoost\</sub\>
\</div\>

```
