# Hey, I'm Mohamed Dhia — but most people call me Guiga 👋

I'm an MSc student in Computing for Data Science at the Free University of Bozen-Bolzano, and honestly, the thing I like most is picking a messy real-world dataset and turning it into something that actually predicts, explains, or generates something useful. Healthcare data, chest X-rays, language models being polite (or not) — if there's a pattern in it, I want to dig it out.

I'm not a "run the model and ship it" person — I care about *why* it works: what a SHAP value is actually telling you, why a fine-tune beats a prompt (or doesn't), why a "99% accurate" model is sometimes a red flag rather than a win. That mindset runs through everything below.

---

## 🩺 Healthcare & applied ML

**[CKD Risk Simulator](https://github.com/CodeMeGuiga/ckd-risk-simulator)**
Predicts Chronic Kidney Disease from 23 clinical measurements and layers on something I think matters more: *how* the picture changes when a patient also has diabetes or hypertension. Random Forest hits 100% on the (highly separable) UCI dataset — and the README says so honestly, because a perfect score should make you suspicious, not proud. Ships as an interactive Streamlit app with live SHAP explanations and a "what-if" simulator so you can tweak a lab value and watch the prediction move.
`scikit-learn` `SHAP` `Streamlit`

**[Medical Image Classification (Chest X-Ray)](https://github.com/CodeMeGuiga/med-image-class-cnn)**
A CNN that separates pneumonia from healthy chest X-rays. Simple idea, but a great excuse to get properly hands-on with image preprocessing and CNN architecture choices instead of just importing a pretrained model and calling it done.
`TensorFlow/Keras` `OpenCV`

**[Unsupervised Patient Subtyping from EHR Data](https://github.com/CodeMeGuiga/ehr-patient-clustering)**
Clustering 8,000 synthetic hospital patients without any labels, and refusing to take the easy way there — instead of one-hot encoding everything into a fake Euclidean space, I compute a Gower distance matrix that handles mixed numerical/categorical data properly, run UMAP on top of *that*, and compare five algorithms (K-Means, DBSCAN, HDBSCAN, GMM, Agglomerative) with Gap Statistic and Dunn Index metrics I implemented from scratch, then stress-test cluster stability with bootstrap resampling before trusting any of it.
`scikit-learn` `Gower distance` `UMAP` `HDBSCAN`

---

## 🗣️ NLP & language models

**[Politeness vs. Asking for It](https://github.com/CodeMeGuiga/politeness-optimization)**
My favorite project so far. The question: does fine-tuning a model with DPO actually make it *more consistently* polite than just... asking nicely in a system prompt? I ran a proper three-way comparison (no intervention, prompt engineering, DPO fine-tuning) on Llama 3.2 3B across 50 emotionally-loaded scenarios, scored with an automated classifier, embedding similarity, and an LLM-as-judge rubric. Turns out the answer isn't as obvious as you'd think.
`PyTorch` `Hugging Face` `PEFT/LoRA` `DPO`

**[Abstractive Text Summarization](https://github.com/CodeMeGuiga/abstractive-text-summarization)**
Fine-tuned BART to summarize scientific papers from the PubMed subset of `scientific_papers` — full pipeline from tokenization/truncation through training with Hugging Face `Trainer` to ROUGE evaluation.
`Hugging Face Transformers` `BART`

**[Text Clustering on 20 Newsgroups](https://github.com/CodeMeGuiga/text-clustering-20newsgroups)**
A deep dive into something people gloss over: *which* distance metric you pick for clustering text actually changes your results. Compares cosine vs. Euclidean distance on TF-IDF vectors, handles the annoying edge case of zero vectors, and checks the difference with silhouette scores instead of just eyeballing it.
`scikit-learn` `NLTK`

---

## 👁️ Computer vision & classic ML

**[Focus Tracker Pro](https://github.com/CodeMeGuiga/focus-tracker)**
A desktop app I built for myself, honestly — it watches your webcam, reads your facial emotion with a CNN, tracks whether you've wandered off, and logs it all per active window (with a siren if you've been gone too long). Trained the emotion model myself on 48x48 face crops across 7 emotion classes, then wired it into a real-time OpenCV pipeline.
`TensorFlow/Keras` `OpenCV` `PyInstaller`

**[Music Genre Classification](https://github.com/CodeMeGuiga/music-genre-classification)**
Classifying audio into 10 genres from a dataset that was *intentionally* left messy — missing labels, noisy entries, the works. Feature extraction with `librosa` plus a healthy dose of data cleaning before any modeling happens.
`librosa` `scikit-learn`

**[Handwritten Digit Classification](https://github.com/CodeMeGuiga/handwritten-digit-classification)**
Same "messy dataset" philosophy applied to grayscale digit images — cleaning, preprocessing, and classifying 0-9 from a dataset with missing and corrupted samples baked in on purpose.
`scikit-learn`

---

## 🛠️ Stack

**Languages** Python · C++ · JavaScript/TypeScript
**ML/DL** PyTorch · TensorFlow/Keras · scikit-learn · Hugging Face Transformers · PEFT/LoRA/DPO · SHAP
**Data** pandas · NumPy · librosa · OpenCV
**Apps** Streamlit · React · Firebase

---

## 🚀 Currently

Finishing my MSc and building out projects that go past the notebook — trained models wired into real apps (Streamlit, desktop, mobile) rather than left as one-off experiments. Genuinely curious about model interpretability, and always happy to talk about a weird dataset or a surprising evaluation result.

Open to internships and freelance work in ML engineering and data science — [reach out](mailto:mrezgui@unibz.it).
