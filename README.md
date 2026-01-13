# Cookie Cats: A/B Testing Level Gate Placement
Link on Kaggle: https://www.kaggle.com/code/mitty527/mobile-game-a-b-testing

## 📌 Project Overview
This project analyzes an A/B test for the popular mobile puzzle game, **Cookie Cats**. The goal was to determine if moving the first "gate" (a point where players are forced to wait or make a purchase) from **Level 30 to Level 40** affects player retention and game engagement.

## 📊 The Dataset
The dataset contains results from an A/B test where:
- **Control Group:** `gate_30`
- **Test Group:** `gate_40`
- **Metrics:** Day-1 Retention, Day-7 Retention, and `sum_gamerounds` (Engagement).

## 🧪 Statistical Methodology
To ensure scientific accuracy, different statistical tests were applied based on the data distribution:

1. **Retention (Categorical):** Two-sample **Z-Tests** for proportions.
2. **Engagement (Numerical/Skewed):** **Mann-Whitney U Test** (Non-parametric) to account for outliers and highly skewed game-round data.

## 📈 Key Findings
| Metric | Result | P-Value | Statistical Significance |
| :--- | :--- | :--- | :--- |
| **Day-1 Retention** | No Change | 0.0739 | Not Significant |
| **Day-7 Retention** | **Drop** | 0.0008 | **Highly Significant** |
| **Engagement** | No Change | 0.0509 | Not Significant |


## 💡 Conclusion & Recommendation
While moving the gate to Level 40 did not significantly impact the number of rounds played, it caused a **statistically significant drop in long-term (Day 7) retention.** **Recommendation:** The game should **keep the gate at Level 30**. Moving the gate further back likely disrupts the player's habit-forming loop, making them less likely to return a week later.

## 🛠️ Tech Stack
- **Language:** Python
- **Libraries:** Pandas, Scipy, Statsmodels, Matplotlib/Seaborn
