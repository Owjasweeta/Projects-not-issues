# Results

Copy every `results_*.csv` file from `revision_results.zip` (written by the last step of the notebook to
`MyDrive/agent_routing`) into this folder. The main files are:

| File | Produced by | Content |
|---|---|---|
| `results_rolling_windows.csv` | Step 2 | Every policy and method per monthly window |
| `results_rolling_predictions.csv` | Step 2 | Score and decision for each of the 21,016 test issues |
| `results_bootstrap_ci.csv` | Step 4 | Repository-clustered 95% intervals |
| `results_within_repo_auc.csv` | Step 4 | AUC within each repository |
| `results_feature_within_repo.csv` | Step 8 | Pooled and within-repository AUC of each feature |
| `results_shap.csv` | Step 3 | Mean absolute SHAP value per feature and month |
| `results_llm_baseline.csv` | Step 6 | Zero-shot Qwen2.5-1.5B baseline |
| `results_llm_comparison.csv` | Step 6b | Five open language models on the same issues |
| `results_alpha_sweep.csv` | Step 9 | Results for budgets from 0.05 to 0.30 |
| `results_biweekly.csv`, `results_biweekly_summary.csv` | Step 10 | Bi-weekly deployment and simple safeguards |
| `results_cold_start.csv` | Step 10 | Results by repository history |
| `results_classification_metrics.csv` | Step 12 | Accuracy, precision, recall, F1 |
| `results_warmup*.csv` | Step 14 | Policies for new repositories |
| `results_timeline_lags.csv`, `results_decision_shift.csv` | Step 15 | Decision-time checks |
| `results_hierarchical*.csv` | Step 16 | Group-conditional thresholds |
| `results_online_early*.csv` | Step 17 | Online control with early review signals |
| `results_online_asymmetric*.csv` | Step 18 | Asymmetric online control |
| `results_repo_level*.csv` | Step 19 | Broader repository history and metadata |
| `results_ablation_combined.csv` | Step 20 | Ablation and the combined policy |
