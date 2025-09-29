Weak Signal ML Pipeline 🚀
📌 Project Overview

This project explores a real-world regression challenge where the dataset contained data leakage and very weak predictive signals.

At first glance, the model appeared to perform extremely well — but this was only because of an ID column leaking information. After carefully detecting and removing the leakage, performance dropped significantly. This provided an opportunity to practice building a robust ML pipeline even when results aren’t perfect.

The project emphasizes process > performance, mirroring the kind of messy, noisy datasets often encountered in production.

⚡ Key Learnings

🔍 Data Leakage Detection: Identified that the Id column was artificially inflating scores.

🧹 Pipeline Building: Implemented preprocessing, train/test splits, and baseline checks.

📉 Weak Signals: Demonstrated that some datasets have very little true predictive power.

🧪 Experiments Tried:

Random Forest (good with leakage, collapsed without)

XGBoost with hyperparameter tuning

Polynomial features & PCA

Regularization methods (Lasso)

Dummy Regressor (baseline check confirming weak signal)

📊 Results

With Leakage (Id included):

R² ≈ 0.91

MAE ≈ 2.23

MSE ≈ 9.49

Without Leakage (cleaned dataset):

Best R² ≈ 0.31 (Polynomial + Tree Models)

Typical R² ≈ 0.05–0.28

Dummy R² ≈ 0.00 (confirmed weak dataset)

💡 Takeaways

High performance isn’t always real — always check for leakage.

Sometimes, datasets simply lack predictive power. That’s still valuable learning.

Success isn’t only about metrics; it’s about building pipelines that work on both clean and messy data.

🛠️ Tech Stack

Python (pandas, numpy, matplotlib, seaborn)

scikit-learn (RandomForest, Linear Models, PolynomialFeatures, PCA, DummyRegressor)

XGBoost

🔮 Future Work

Try feature engineering beyond polynomial features.

Explore domain-specific transformations (if metadata is available).

Use SHAP values for interpretability, even in weak-signal datasets.

📢 Final Note

This project reflects a real-world ML scenario:
➡️ Detect leakage
➡️ Accept weak signals
➡️ Focus on process, robustness, and honesty in reporting

IMAGE Link
