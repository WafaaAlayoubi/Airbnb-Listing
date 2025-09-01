# Exploratory Data Analysis of Airbnb Listings

## Project Overview

This project provides a comprehensive Exploratory Data Analysis (EDA) on a large dataset of Airbnb listings. The primary objective is to uncover the underlying factors that influence guest ratings and to understand the key characteristics of the Airbnb market landscape.

The analysis follows a structured, professional workflow, moving from high-level data inspection and cleaning to deep-dive univariate and bivariate analysis. The entire process is documented in a Kaggle notebook, emphasizing data-driven insights and clear, effective visualizations.

**Dataset:** The data is a snapshot of Airbnb listings, containing over 45,000 rows and 79 columns, including detailed information on pricing, location, host information, amenities, and guest reviews.

---

## Key Questions Addressed

1.  What is the distribution of guest ratings, and what defines a "typical" listing?
2.  How does the price of a listing correlate with its rating?
3.  What are the most common types of properties and rooms available?
4.  Are there strong, linear relationships between numerical features (like price, host tenure, or number of bedrooms) and the final guest rating?

---

## Key Findings & Insights

The analysis revealed several counter-intuitive and significant insights:

-   **The Price Myth:** There is **no significant linear correlation** between the price of a listing and its `review_scores_rating`. High price is not an indicator of a better guest experience. The market is dominated by affordable listings with near-perfect scores.
-   **The 5-Star Saturation:** The dataset is heavily skewed towards perfection. The median rating is an exceptionally high **4.91**, making the modeling challenge one of distinguishing between "great" and "truly exceptional" listings.
-   **Market Dominance of Entire Homes:** "Entire home/apt" listings constitute over **73%** of the market and maintain an extremely high median rating, indicating this is the standard, preferred experience.
-   **A Non-Linear Problem:** The lack of strong correlations suggests that predicting ratings is a complex, non-linear problem. Success in modeling will depend heavily on advanced feature engineering (e.g., from `amenities` and text descriptions) rather than relying on the raw numerical features.

---

## Technical Stack

-   **Python:** Core programming language for the analysis.
-   **Pandas:** For data manipulation, cleaning, and processing.
-   **NumPy:** For numerical operations.
-   **Matplotlib & Seaborn:** For creating a wide range of static, informative, and beautiful visualizations.
-   **ydata-profiling:** For generating a rapid, automated overview of the dataset to accelerate the initial EDA phase.

---

## Repository Structure

```
├── airbnb-full-eda.ipynb       # The main Jupyter/Kaggle notebook with the full analysis.
├── docs/
│   └── eda_report.html
├── README.md                      # This README file.
└── requirements.txt               # List of Python dependencies for reproducibility.
```

---

## How to Run This Project

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/WafaaAlayoubi/Airbnb-Listing
    cd Airbnb-Listing
    ```

2.  **Set up a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Launch Jupyter Notebook and open the main file:**
    ```bash
    jupyter notebook airbnb-full-eda.ipynb
    ```
*(Note: to download the data `listings.csv` you can find it at https://www.kaggle.com/datasets/wafaaalayoubi/los-angeles-airbnb-data-june-2025)*

---

## Final Conclusion

This EDA provides a foundational understanding of the Airbnb dataset and delivers a clear, strategic roadmap for any subsequent machine learning or feature engineering tasks. The key takeaway is that predicting guest satisfaction is a nuanced challenge that requires looking beyond simple metrics like price.