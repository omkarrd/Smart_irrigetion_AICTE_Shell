# Smart Irrigation System 🌱

An ML-powered irrigation controller that predicts which sprinklers to activate across farm parcels based on real soil and environmental sensor data. Built during the AICTE / Shell India / Edunet Foundation internship under the **Skills4Future** program, with a focus on applying AI to sustainability challenges.

---

## Problem

Traditional irrigation systems run on fixed timers — they water crops whether the soil needs it or not. This wastes significant water and increases costs for farmers. The goal of this project was to use real sensor data to make smarter, data-driven decisions about when and where to irrigate.

---

## What It Does

- Takes 20 sensor readings as input (soil moisture, temperature, humidity, etc.)
- Runs them through a trained ML model
- Predicts which sprinklers across multiple farm parcels should be **ON** or **OFF**
- Delivers predictions through a simple, browser-based UI — no technical setup needed for the end user

---

## Tech Stack

| Layer | Tools |
|---|---|
| Data Analysis | Python, pandas, numpy, matplotlib, seaborn |
| ML Model | scikit-learn (multi-label classification) |
| Model Serialization | joblib (.pkl) |
| Web Interface | Streamlit |
| Development | Jupyter Notebook |

---

## Project Structure

```
Smart_irrigetion_AICTE_Shell/
│
├── irrigetion_System.ipynb      # Full ML pipeline: EDA → preprocessing → training → evaluation
├── app.py                       # Streamlit web app for real-time predictions
├── Farm_Irrigation_System.pkl   # Trained and serialized ML model
├── irrigation_machine.csv       # Raw sensor dataset used for training
└── README.md
```

---

## How to Run

**1. Clone the repo**
```bash
git clone https://github.com/omkarrd/Smart_irrigetion_AICTE_Shell.git
cd Smart_irrigetion_AICTE_Shell
```

**2. Install dependencies**
```bash
pip install streamlit scikit-learn numpy joblib pandas
```

**3. Launch the app**
```bash
streamlit run app.py
```

**4. Use it**
- Adjust the 20 sensor sliders (values from 0.0 to 1.0)
- Click **Predict Sprinklers**
- The app shows which sprinkler zones should be ON or OFF

---

## ML Pipeline (Notebook)

The `irrigetion_System.ipynb` notebook walks through the full process:

1. **Data loading** — read `irrigation_machine.csv` using pandas
2. **EDA** — `.info()`, `.describe()`, `.shape`, `.sample()` to understand the dataset
3. **Preprocessing** — feature selection, scaling sensor values to [0, 1] range
4. **Model training** — multi-label classifier using scikit-learn
5. **Evaluation** — accuracy metrics across all sprinkler output labels
6. **Export** — model saved as `Farm_Irrigation_System.pkl` using joblib

---

## Key Takeaway

This project demonstrates how a relatively simple ML model, trained on real sensor data, can automate a decision that farmers currently make manually or leave to fixed timers. The Streamlit interface makes the model accessible to non-technical users without any API or backend knowledge.

---

## Built As Part Of

**AICTE Internship Cycle 2** — Shell India & Edunet Foundation  
Skills4Future Program | Focus: Green Skills & AI for Sustainability

---

## Author

**Omkar Divekar**  
[GitHub](https://github.com/omkarrd) · [LinkedIn](https://linkedin.com/in/omkar-r-d) · omkarrdivekar2194@gmail.com
