## 📌 Project Overview

This project implements a Variational Quantum Classifier (VQC) to predict late delivery risk in a supply chain dataset. The model explores how quantum circuit design and dataset size affect classification performance.

The goal is to experimentally evaluate:

- Effect of dataset size on quantum model accuracy
  
- Impact of circuit depth (reps)
  
- Influence of rotation gates (RY vs RY + RZ)

---

## 📂 Dataset

- The dataset used is: DataCo Supply Chain Dataset

- Target variable:  Late_delivery_risk

- Selected features:

1. Days for shipping (real)

2. Days for shipment (scheduled)

3. Benefit per order

4. Sales per customer

5. Product Price

---

## ⚙️ Preprocessing Pipeline

1. Feature selection

2. Standard scaling

3. PCA dimensionality reduction

4. Random sampling of experiment subsets

5. Train-test split

---

## 🧠 Quantum Model Design

**Feature Map**

- ZZFeatureMap

- 5 qubits

- Encodes classical data into quantum states

**Ansatz Circuit**

- TwoLocal variational circuit

- Rotation gates tested:

   - RY only

   - RY + RZ

- Entanglement: CZ gates

- Variable circuit depth (reps)

**Optimizer**

COBYLA optimizer

---

## 🧪 Experiments Conducted

- The project compares performance across configurations:
  
- **Configuartion - 1**
  
  - Dataset sizes: 400 vs 1800 samples

  - Circuit depth: reps = 1 vs reps = 2

  - Rotation blocks: RY vs RY+RZ
    
- **Configuartion - 2**
  
  - Dataset sizes: 4000 vs 18000 samples

  - Circuit depth: reps = 1 vs reps = 2

  - Rotation blocks: RY vs RY+RZ

- Accuracy and training time are recorded for each configuration.

---

## 📊 Output Visualization

The script generates:

- Accuracy comparison bar chart

- Training time tracking per experiment

- This helps evaluate trade-offs between circuit complexity and performance.

---

## 🚀 How to Run the Project

1️⃣ **Create virtual environment**

   - python -m venv qml_env

2️⃣ **Activate environment**

   - Windows
     
   - qml_env\Scripts\activate

3️⃣ **Install dependencies**

  - pip install pandas numpy scikit-learn matplotlib qiskit qiskit-machine-learni

4️⃣ **Run notebook or script**

  - Open qml.ipynb in Jupyter or VS Code and run all cells.
 ---

 ## 📈 Future Improvements

- Stratified sampling for class balance

- Hyperparameter tuning of quantum circuits

- Use quantum simulators with noise models

- Compare with classical ML baselines

- Save trained quantum model weights

---
