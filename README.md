# Mobile Games A/B Testing

## 📌 Project Overview
This project analyzes the results of an A/B test for the mobile puzzle game **Cookie Cats**. 
The study examines how moving the first "gate" (a progression barrier that forces a wait time or an in-app purchase) 
from **Level 30** to **Level 40** affects player retention and engagement.

The analysis focuses on **player psychology (Hedonic Adaptation)** and utilizes **statistical bootstrapping** 
to ensure the reliability of the conclusions.

## 🛠️ Tech Stack & Methodology
* **Language:** Python 3.x
* **Libraries:** `Pandas`, `Matplotlib`, `Seaborn`, `Scipy`
* **Key Concept:** **Bootstrapping Analysis** (Resampling the dataset 10,000 times to estimate the distribution and uncertainty of retention rates).
* **Primary Metrics:**
    * **Retention 1:** % of players who return 1 day after installing.
    * **Retention 7:** % of players who return 7 days after installing.
    * **Game Rounds:** Total number of levels played by the user within the first 14 days.

## 📂 Dataset

The dataset used in this project is the [Cookie Cats A/B Testing dataset](https://www.kaggle.com/datasets/mursideyarkin/mobile-games-ab-testing-cookie-cats), which is publicly available on Kaggle. It includes data from 90,189 players who installed the game while the A/B test was running.
* Source: Kaggle - Mobile Games A/B Testing: Cookie Cats 
* Format: CSV 
* Key Columns: userid, version (Gate 30/40), sum_gamerounds, retention_1, retention_7.

## 📊 Key Findings

| Metric | Gate 30 (Control) | Gate 40 (Test) | Difference |
| :--- | :--- | :--- | :--- |
| **Day-1 Retention** | 44.82% | 44.23% | **+0.59%** |
| **Day-7 Retention** | 19.02% | 18.20% | **+0.82%** |

### Statistical Significance (Bootstrapping)
Using bootstrapping analysis, the probability that **Gate 30** has higher Day-7 retention than **Gate 40** is calculated at **99.9%**. While a 0.8% difference may seem marginal, in high-scale mobile gaming, this represents a significant impact on long-term **LTV (Lifetime Value)** and overall revenue stability.

[Image of bootstrapping distribution for A/B testing with 95% confidence interval]

## 🧠 Business Insight: Why Gate 30?
The results strongly support the theory of **Hedonic Adaptation**. By introducing a progression barrier earlier (Level 30), the game effectively manages player burnout. This "forced break" increases the player's enjoyment and longing for the game, leading to higher long-term retention compared to allowing uninterrupted play until Level 40.

[Image of retention rate comparison bar chart for day 1 and day 7]

## 🚀 How to Run
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/cookie-cats-ab-test.git](https://github.com/yourusername/cookie-cats-ab-test.git)
    ```
2.  **Install dependencies:**
    ```bash
    pip install pandas matplotlib seaborn scipy
    ```
3.  **Run the analysis:** Open `analysis.ipynb` in Jupyter Notebook or Google Colab.

##