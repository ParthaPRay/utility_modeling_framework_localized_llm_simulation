# A Holistic Utility-Based Modeling Framework for Quality–Efficiency Trade-offs in Edge Language Models

**Author:** Partha Pratim Ray  
**Affiliation:** Sikkim University  
**Email:** parthapratimray1986@gmail.com  

---

## 📌 Overview

This repository provides the implementation and experimental framework for the paper:

> **“A Holistic Utility-Based Modeling Framework for Quality–Efficiency Trade-offs in Edge Language Models”**

The work introduces a **multi-objective, utility-driven evaluation framework** for selecting Large Language Models (LLMs) in **resource-constrained edge environments** such as Raspberry Pi.

Unlike traditional benchmarks focused solely on accuracy, this framework jointly models:

- ✅ Quality (semantic performance)  
- ⚡ Latency  
- 🔋 Energy consumption  
- 💾 Memory usage  
- 🌡️ Thermal behavior  

---

## 🎯 Key Contributions

- **Holistic Utility Function** integrating quality and system constraints  
- **Scenario-aware model selection** (latency-critical, energy-critical, etc.)  
- **Composite efficiency metrics**:
  - QEE (Quality–Energy Efficiency)
  - QLE (Quality–Latency Efficiency)
  - QRE (Quality–Resource Efficiency)
- **Pareto-optimal model analysis**  
- **Risk-sensitive utility modeling**  
- **End-to-end evaluation pipeline with visualization + LaTeX outputs**

---

## 📂 Repository Structure


```bash
├── edge_llm_results.csv        # Input dataset
├── main.py                     # Core evaluation script
├── paper_outputs/              # Generated outputs
│   ├── model_summary.csv
│   ├── scenario_winners.csv
│   ├── fig_01.png
│   ├── fig_02.pdf
│   ├── table_results.tex
│   └── fig_summary.csv
└── README.md
```
---

## 📊 Input Data Format


```bash
model,quality,latency_s,energy_j,memory_mb,thermal_c,tokens_per_sec,power_w
Qwen2.5,0.86,18.5,92.5,2100,61.2,11.4,5.0
Llama3.2,0.81,16.0,88.0,2300,63.5,8.1,5.5
SmolLM2,0.74,36.5,109.0,2500,66.8,4.4,3.0
Granite3,0.83,33.3,95.0,2050,60.1,6.7,2.9
```
---

## ⚙️ Installation

pip install numpy pandas matplotlib

---

## ▶️ Usage

python main.py

---

## 📈 Outputs

All outputs are saved in:

paper_outputs/

### 🔹 Tables

- model_summary.csv → Overall ranking  
- scenario_winners.csv → Best model per deployment scenario  
- table_*.tex → LaTeX-ready tables for paper  

### 🔹 Figures

| Figure | Description                         |
|--------|-------------------------------------|
| Fig 1  | Holistic normalized metric profile  |
| Fig 2  | Pareto frontier (quality vs energy) |
| Fig 3  | Composite efficiency metrics        |
| Fig 4  | Scenario-based utilities            |
| Fig 5  | Thermal vs power region             |
| Fig 6  | Correlation matrix                  |
| Fig 7  | Risk-sensitive utility              |

---

## 🧠 Methodology

### 1. Normalization

Min–max normalization applied to all metrics  
Cost metrics are inverted.

### 2. Utility Function

U(m) = αQ − βL − γE − δR − ηT

### 3. Scenario-Based Evaluation

Balanced, Latency-critical, Energy-critical, Quality-critical, Memory-critical, Thermal-critical

### 4. Pareto Optimization

Benefit: Quality ↑  
Costs: Latency ↓, Energy ↓, Memory ↓, Thermal ↓  

### 5. Risk-Sensitive Utility

U_risk = U − λ·Var(L, E, R, T)

---

## 📌 Key Results

### 🔹 Best Overall Model (Balanced Scenario)

Qwen2.5

### 🔹 Pareto-Optimal Models

- Qwen2.5  
- Llama3.2  
- Granite3  

---

## 🔬 Research Impact

- Edge AI deployment decisions  
- Energy-aware LLM selection  
- Thermal-safe model deployment  
- Multi-objective optimization  

---

## 🚀 Future Work

- Hardware validation  
- Adaptive model selection  
- Kubernetes integration  
- Cross-hardware benchmarking  

---

## 📜 License

Academic and research use.

---

## 📧 Contact

Dr. Partha Pratim Ray  
parthapratimray1986@gmail.com
