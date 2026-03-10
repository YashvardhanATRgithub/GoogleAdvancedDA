# YouTube Shorts Video Analysis: Engagement, Claims Classification & User Verification

## Overview

This project analyzes a YouTube Shorts video dataset to uncover engagement insights, predict video claim status, and understand user verification factors. The primary goal is to build a machine learning model that classifies videos as **claims** or **opinions** — helping content moderators prioritize reviews and address potential misinformation.

The project progresses through data inspection, exploratory data analysis, hypothesis testing, regression modeling, and classification model development.

## Dataset

**File:** `data/yt_shorts_dataset.csv` — 19,382 videos with 12 features.

| Feature | Description |
|---|---|
| `claim_status` | **Target** — `claim` or `opinion` |
| `video_duration_sec` | Video length (5–60s) |
| `video_transcription_text` | Transcript of video audio |
| `verified_status` | `verified` or `not verified` |
| `author_ban_status` | `active`, `under review`, or `banned` |
| `video_view_count` | Views |
| `video_like_count` | Likes |
| `video_share_count` | Shares |
| `video_download_count` | Downloads |
| `video_comment_count` | Comments |

## Project Structure

```
├── data/
│   └── yt_shorts_dataset.csv
├── notebooks/
│   ├── 01_data_inspection.ipynb
│   ├── 02_eda_visualization.ipynb
│   ├── 03_hypothesis_testing.ipynb
│   ├── 04_logistic_regression.ipynb
│   └── 05_claim_classification.ipynb
├── reports/
│   ├── eda_executive_summary.pptx
│   └── ml_executive_summary.pptx
├── requirements.txt
└── README.md
```

### Notebooks

| # | Notebook | Focus |
|---|---|---|
| 1 | `01_data_inspection.ipynb` | Load, inspect, and summarize the dataset |
| 2 | `02_eda_visualization.ipynb` | EDA, outlier analysis, and data visualization |
| 3 | `03_hypothesis_testing.ipynb` | Hypothesis test: verified vs. unverified view counts |
| 4 | `04_logistic_regression.ipynb` | Logistic regression to predict `verified_status` |
| 5 | `05_claim_classification.ipynb` | Random Forest & XGBoost to classify `claim_status` |

## Key Results

- **Champion Model:** Random Forest with **0.995 recall** on the validation set
- **Top Predictors:** Video engagement metrics (views, likes, shares, downloads) are the strongest signals for classifying a video as a claim
- **Hypothesis Test:** Verified and unverified accounts have statistically significant differences in average view counts
- **Logistic Regression:** Longer videos and higher engagement are associated with verified authors

## Technologies

- **Python** — pandas, NumPy, Matplotlib, Seaborn, SciPy
- **Machine Learning** — scikit-learn (Logistic Regression, Random Forest), XGBoost
- **Visualization** — Tableau (executive summaries)
- **Environment** — Jupyter Notebooks

## Getting Started

```bash
git clone <repository-url>
cd GoogleAdvancedDA
pip install -r requirements.txt
jupyter lab
```

Open notebooks sequentially (`01` → `05`) to follow the analysis pipeline.

## Contact

- **LinkedIn:** [Yashvardhan](https://www.linkedin.com/in/yashvardhan-4735121b9/)

## License

This project is for educational purposes.
