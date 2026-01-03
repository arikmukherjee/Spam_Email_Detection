# Spam Mail Detection ✅

A Python project that trains a simple SMS spam classifier (Multinomial Naive Bayes + CountVectorizer) on the provided `spam.csv` dataset and exposes a quick Streamlit UI to try predictions.

---

## 🔍 Project overview

- **Goal:** Detect whether an SMS message is Spam or Not Spam.
- **Model:** Multinomial Naive Bayes using `CountVectorizer` (bag-of-words).
- **UI:** Streamlit app (`spam_email_detection.py`) with a text input to test messages.
- **Dataset:** `spam.csv` (SMS messages labeled `ham` or `spam`).

---

## 📁 Repository structure

- `spam_email_detection.py` — model training and Streamlit UI
- `app.py` — small example Streamlit app
- `spam.csv` — SMS dataset used to train the model
- `myenv/` — local virtual environment (optional, already present in this workspace)

---

## ⚙️ Requirements

- Python 3.8+
- Packages: `pandas`, `numpy`, `scikit-learn`, `streamlit`

You can install the packages with pip:

```bash
# (recommended) from the project root
python -m venv myenv
myenv\Scripts\activate   # Windows
pip install pandas numpy scikit-learn streamlit
```

Optionally create a `requirements.txt` with these packages for reproducible installs.

---

## ▶️ How to run

1. Make sure `spam.csv` is in the same folder as the scripts (project root).
2. Start the Streamlit app:

```bash
streamlit run spam_email_detection.py
or,
python -m streamlit run spam_email_detection.py
```

This opens a browser UI where you can enter messages and click `Predict` to see the model's label.

Tip: `app.py` is a minimal Streamlit example; run it with `streamlit run app.py`.

---

## 📝 Notes & suggestions

- The current script trains the model on import / run. For larger workflows consider:
  - Saving the trained model with `joblib` or `pickle` and loading it for inference.
  - Adding text preprocessing (normalization, stemming/lemmatization, n-grams).
  - Adding unit tests and a simple CLI to perform batch predictions.

---

## ⚖️ License

This project is provided under the **MIT License**. Feel free to adapt and improve it.

---

If you'd like, I can: add a `requirements.txt`, persist the trained model, or improve the Streamlit UI (e.g., show probabilities and confusion matrix). Which would you like next?