# MSCS_634_Lab_6 - Association Rule Mining

## Purpose
The purpose of this lab is to apply association rule mining techniques—specifically the Apriori and FP-Growth algorithms—on a real-world transactional dataset. The objective is to discover frequent itemsets and generate association rules that reveal meaningful relationships between items.

## Key Insights
- The most frequently viewed/purchased items were identified and visualized using bar plots.
- Both Apriori and FP-Growth successfully extracted meaningful item combinations with significant support and confidence.
- Association rules with high lift and confidence were visualized to support product bundling or recommendation logic.
- FP-Growth generated results faster and handled the dataset more efficiently than Apriori, especially with larger transaction sets.

## Challenges & Decisions
- **Missing Columns**: The original dataset lacked the expected `event_type` column, requiring dynamic handling of column names.
- **Kernel Crash on Apriori**: When attempting to run Apriori on the full dataset, the notebook kernel crashed due to memory overload. This was resolved by sampling a subset of transactions (e.g., 5000) before applying Apriori, while using the full dataset for FP-Growth.
- **Library Compatibility**: Adjustments were made to Seaborn visualizations to avoid deprecation warnings by explicitly assigning `hue` and suppressing the legend.

## How to Run
1. Ensure all required Python packages are installed: `pandas`, `matplotlib`, `seaborn`, `mlxtend`, `ipykernel`.
2. Activate your virtual environment and register it as a Jupyter kernel.
3. Launch Jupyter Notebook and open `Lab6_AssociationRules.ipynb`.
4. Confirm that the dataset file `archive/events.csv` exists in the correct location.
5. Run the notebook and switch to the `Python (venv)` kernel if needed.

