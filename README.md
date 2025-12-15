# Music–Emotion Analysis (DEAM Dataset)

This project explores the relationship between musical emotion dimensions — **valence** and **arousal** — using the DEAM (Dynamic Emotion Annotations in Music) dataset.  
It is a practical mini-project designed to demonstrate data analysis, baseline modeling, and the implementation of a simple recommender system.

---

## Project Goals

- Load and analyze a real-world dataset
- Perform basic data validation and exploratory analysis
- Build simple baseline prediction models
- Evaluate models using interpretable metrics
- Implement a small mood-based recommender prototype
- Present results in a clear, reproducible way

This is a **practical portfolio project**, not a research paper.

---

## Dataset

**DEAM – Dynamic Emotion Annotations in Music**

- Static averaged annotations were used
- Each song is annotated with:
  - `valence_mean` (positivity)
  - `arousal_mean` (energy / intensity)
- Emotion values are on an approximate **1–9 scale**

The dataset files are **not included** in this repository.

---

## Methods

### 1. Data Understanding & Exploration
- Checked missing values and duplicates
- Verified valid value ranges
- Visualized distributions of valence and arousal
- Analyzed the relationship between valence and arousal

### 2. Baseline Prediction Models
- Train/test split (80% / 20%)
- Baseline predictor (mean value)
- Linear regression models:
  - Predicting arousal from valence
  - Predicting valence from arousal
- Evaluation metric: **Mean Absolute Error (MAE)**

### 3. Mood-Based Recommender
- Songs represented in **valence–arousal space**
- Features standardized before distance computation
- k-Nearest Neighbors (kNN) used to find similar songs
- Recommender returns songs with similar emotional profiles
- Visualization included for interpretability

---

## Results (Summary)

- Valence and arousal show a **moderate positive correlation**
- Linear regression models improve over baseline predictions but retain substantial error
- Results indicate that valence and arousal capture related but distinct aspects of musical emotion
- The recommender successfully retrieves songs with similar emotional characteristics

---

## Project Structure
```
music-emotion-deam/
├── notebooks/
│   └── 01_baseline.ipynb
├── results/
│   └── recommendations_example.csv
├── README.md
├── requirements.txt
└── .gitignore
```

---

## How to Run

1. Clone the repository
2. Create and activate a virtual environment
3. Install dependencies:
   ```bash
   pip install -r requirements.txt 
   ```
4. Place DEAM CSV files in a local data/ directory
5. Open and run notebooks/01_baseline.ipynb

---

## Notes

- This project focuses on clarity and reproducibility
- All models are intentionally simple and interpretable
- The notebook is designed to run top-to-bottom

---

## Future Work

- Incorporate audio features
- Explore nonlinear models
- Extend the recommender with user preferences

---

