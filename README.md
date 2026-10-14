# econ3916-lab06-sampling
econ3916-lab06-sampling
# Sampling for Machine Learning — Train-Test Splits

## Objective
To explore sample design, train-test splitting strategies, data leakage prevention, and the mechanics of sampling bias through hands-on data analysis.

## Methodology
* Explored the Titanic dataset containing 891 passengers with survival as the target variable.
* Compared naive and stratified train-test splits to verify how stratification preserves target proportions across subsets.
* Detected and repaired data leakage in `StandardScaler` and `SimpleImputer` preprocessing pipelines by fitting exclusively on training data.
* Developed a custom `split_by_share()` function to partition data by a specified test share and random seed.
* Simulated the 1936 Literary Digest polling failure across 10 million voters to study sampling bias.
* Computed Meng's data defect correlation and compared a biased sample of 4,382,503 responses against a random sample of 50,000.
* Executed 100 replications comparing the estimation error distribution of biased versus random samples.

## Key Findings
* Sample design outweighs sample size in determining estimate accuracy.
* A data defect correlation of 0.1475 produced a systematic error of 8.3 percentage points in the biased sample estimate.
* Random sampling with a smaller sample size (50,000) achieved an unbiased estimate centered near the true population parameter, whereas the massive biased sample remained tightly clustered around the wrong value.
