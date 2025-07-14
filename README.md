
# Robotic Fan Fault Detection Using Machine Learning

This project applies machine learning to detect mechanical imbalance in a fan system using accelerometer data — simulating vibration-based predictive maintenance in robotic or industrial systems. Two powerful classifiers, Random Forest and Support Vector Machine (SVM), are trained and tuned using `GridSearchCV`, followed by comprehensive metric comparisons.

---

## 🔍 Project Motivation

Mechanical imbalance in motors and fans can lead to failure in robotic and industrial systems. Detecting these imbalances early through vibration data enables:
- Preventive maintenance  
- Reduced downtime  
- Increased safety and reliability  

This project models that scenario with accelerometer data collected from a fan with different weight configurations.

---

## 📦 Dataset

**Source:**  
UCI Machine Learning Repository  
🔗 [https://archive.ics.uci.edu/dataset/846/accelerometer](https://archive.ics.uci.edu/dataset/846/accelerometer)

**Original Study:**  
> _Prediction of Motor Failure Time Using An Artificial Neural Network_  
> DOI: [10.3390/s19194342](https://doi.org/10.3390/s19194342)

### 📘 Additional Information

This dataset was generated using a cooler fan with weights on its blades to simulate vibrations caused by mechanical imbalance. An MMA8452Q accelerometer was attached to the fan to record vibration data.

Three distinct configurations were created:
1. **Red (Normal)** – Weights on neighboring blades  
2. **Blue (Perpendicular)** – Weights at a 90° angle  
3. **Green (Opposite)** – Weights on opposite blades  

### ⚙️ Devices Used
- **Fan:** Akasa AK-FN059 12cm Viper cooling fan (1900 rpm max)
- **Sensor:** MMA8452Q Accelerometer

### 🧪 Data Collection
- 17 fan speeds (20% to 100% at 5% intervals)  
- Each speed ran for 1 minute at 20ms sampling = 3,000 samples per speed  
- Total records: **153,000**

### 📊 Features
| Feature   | Description                                                  |
|-----------|--------------------------------------------------------------|
| `wconfid` | Weight Configuration ID (1=Red, 2=Blue, 3=Green)             |
| `pctid`   | Fan speed percentage (e.g., 20 = 20% of max speed)           |
| `x`       | Accelerometer X-axis reading                                 |
| `y`       | Accelerometer Y-axis reading                                 |
| `z`       | Accelerometer Z-axis reading                                 |

---

## 🎯 Goals

- Preprocess accelerometer and fan speed data  
- Train and evaluate two classifiers:
  - **Random Forest** (with `GridSearchCV` tuning)  
  - **Support Vector Machine (SVM)** (with `GridSearchCV` tuning)  
- Compare models using:
  - Confusion Matrices  
  - Macro F1 Score   
- Visualize key performance insights

---

## 🛠️ Tools and Libraries

- Python  
- Pandas, NumPy  
- Seaborn, Matplotlib  
- Scikit-learn  

---

## 🚀 Running the Project

1. Clone the repo:
   ```bash
   git clone https://github.com/your-username/ml-project-robotic-fan-fault-detection.git
   cd ml-project-robotic-fan-fault-detection
   ```

2. Run the Jupyter notebook:
   ```bash
   jupyter notebook ml-project-robotic-fan-fault-detection.ipynb
   ```
