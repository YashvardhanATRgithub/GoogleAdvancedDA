# TikTok Video Analysis: Engagement, Claims Classification, and User Verification

## 🚀 Project Overview

This project undertakes a comprehensive analysis of a TikTok video dataset to uncover insights into user engagement, predict video claim status, and understand factors associated with user verification. The primary goal is to develop a machine learning model that can effectively classify videos as either "claims" or "opinions." Such a model can significantly aid in content moderation by helping to prioritize videos for review, thereby addressing the spread of potential misinformation more efficiently.

The project progresses through several key stages, from initial data inspection and exploratory data analysis (EDA) to hypothesis testing, regression modeling, and finally, the development and evaluation of classification models.

## 📁 Dataset

The core dataset for this project is `tiktok_dataset.csv`. It contains various features related to videos and their authors, including:

* **Video Engagement Metrics:**
    * `video_view_count`
    * `video_like_count`
    * `video_comment_count`
    * `video_share_count`
    * `video_download_count`
* **Video Characteristics:**
    * `video_duration_sec`
* **Author Information:**
    * `author_ban_status` (e.g., active, under review, banned)
    * `verified_status` (whether the author is a verified user)
* **Target Variable:**
    * `claim_status` (binary: identifies if a video makes a claim or is an opinion)

## 📂 Project Structure & Methodology

The project is structured across a series of Jupyter notebooks, each corresponding to a specific phase of the data analysis and modeling pipeline:

1.  **`Activity_Course 2 TikTok project lab.ipynb` - Initial Data Inspection & Understanding**
    * Loading and inspecting the dataset.
    * Basic data cleaning and formatting.
    * Preliminary analysis of variable distributions, particularly `claim_status`.
    * Identifying initial correlations, such as between engagement levels and claim status.

2.  **`Activity_Course 3 TikTok project lab.ipynb` - Exploratory Data Analysis (EDA) & Visualization**
    * In-depth EDA to understand data characteristics, identify outliers, and handle missing values.
    * Visualizing data distributions for key engagement metrics (views, likes, comments) using Matplotlib and Seaborn.
    * Analyzing the relationship between `author_ban_status` and engagement.
    * Comparing claim counts versus opinion counts.
    * *(Mentioned)* Creation of Tableau dashboards for reporting insights (details in `43TtFecwRU-4Nt_KoeD77w_78ab7080740e4e34b506c957581b0ef1_Activity-Exemplar_-TikTok-Course-3-executive-summary.pptx`)*

3.  **`Activity_Course 4 TikTok project lab.ipynb` - Statistical Analysis & Hypothesis Testing**
    * Formulating and testing hypotheses regarding relationships between different variables.
    * Applying statistical tests to draw inferences about the data (e.g., are engagement levels significantly different for claims vs. opinions?).

4.  **`Activity_Course 5 TikTok project lab.ipynb` - Regression Analysis for User Verification**
    * Building a logistic regression model to predict an author's `verified_status` based on video characteristics.
    * Identifying factors that are significantly associated with a user being verified.

5.  **`Exemplar_Course 6 TikTok project lab.ipynb` - Machine Learning for Claim Classification**
    * Preparing data for machine learning (feature engineering, splitting into training/validation/test sets).
    * Building and training tree-based classification models (Random Forest and XGBoost) to predict `claim_status`.
    * Evaluating model performance using appropriate metrics, with a focus on recall.
    * Identifying key features driving the classification.
    * *(Results summarized in `dUGw_SNtSPi5m4qioAlzSw_2d5d1030ddd646aeb0ac4436fa5164f1_Activity-Exemplar_-TikTok-Course-6-executive-summary.pptx`)*

## 📊 Key Findings & Insights

### From Exploratory Data Analysis (Course 3):
* **Skewed Data Distribution:** Video engagement metrics (view, like, and comment counts) are heavily right-skewed, with most videos having lower engagement. This needs consideration in modeling.
* **Null Values:** Several columns contain null values, requiring appropriate handling strategies before modeling.
* **Engagement & Claims:** Initial analysis suggests a correlation between higher engagement and claim status.

### From Regression Analysis (Course 5):
* The logistic regression model for `verified_status` identified video characteristics associated with an author being verified. Longer videos, for instance, tended to be associated with higher odds of the user being verified.

### From Machine Learning & Classification (Course 6):
* **High Model Performance:** Both Random Forest (RF) and XGBoost models performed exceptionally well in classifying videos as claims or opinions.
* **Champion Model:** The Random Forest model was selected as the champion model due to its superior recall score (0.995 on the validation set).
* **Key Predictors for Claims:** Video engagement levels (view count, like count, share count, download count) were the primary predictors for a video being classified as a claim. Videos with higher user engagement were much more likely to be claims.
* **Test Set Performance:** The champion RF model achieved near-perfect scores on the test holdout data, with very few misclassifications.

## 🛠️ Technologies Used

* **Programming Language:** Python
* **Data Manipulation & Analysis:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn (for Logistic Regression, Random Forest, XGBoost, model evaluation metrics)
* **Notebook Environment:** Jupyter Notebooks
* **External Visualization (mentioned):** Tableau

## ⚙️ How to Use This Repository

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd <repository-name>
    ```
2.  **Dataset:** Ensure the `tiktok_dataset.csv` file is present in the root directory or update the file paths in the notebooks accordingly.
3.  **Dependencies:** Install the necessary Python libraries. You can create a `requirements.txt` file based on the imports in the notebooks. A general list includes:
    ```
    pandas
    numpy
    matplotlib
    seaborn
    scikit-learn
    jupyterlab # or jupyter notebook
    ```
    Install them using pip:
    ```bash
    pip install -r requirements.txt
    ```
    *(If you create a `requirements.txt` file, list the exact libraries and versions used for reproducibility).*
4.  **Run the Notebooks:** Open and run the Jupyter notebooks sequentially (Course 2 through Course 6) to follow the project's progression. Each notebook typically builds upon the concepts or data processed in previous ones.
5.  **Review Executive Summaries:** The PowerPoint files (`*-executive-summary.pptx`) provide high-level overviews and key results for specific project stages.

## 🔮 Future Work & Recommendations

* **Monitor Feature Distributions:** Continuously monitor the distributions of key predictive features (like video engagement levels) to ensure model robustness over time.
* **Evaluate with Additional Data:** Further evaluate the model using additional, diverse subsets of user data before full-scale deployment.
* **Explore Other Features:** Consider incorporating other potentially relevant features, such as text analysis of video descriptions/comments or audio analysis, if available.
* **Investigate Null Values:** Conduct further analysis to understand the reasons behind null values and their potential impact.
* **Address Data Imbalance:** While the models performed well, explore advanced techniques for handling class imbalance if it becomes an issue with new data.

## 📧 Contact

* [Yashvardhan] - (https://www.linkedin.com/in/yashvardhan-4735121b9/)

## 📜 License

This project is for educational purposes and does not currently have a specific license.