# Causal Biomarker Discovery in RNA-Seq Data

A 3-stage hybrid causal feature selection framework combining mutual-information filtering, conditional-independence local skeleton constraints, and continuous neural graph optimization to discover disease biomarkers from high-dimensional RNA-Seq datasets.

## Pipeline Architecture
1. **Stage 1 (mRMR Filtering):** Maximize gene-target relevance while minimizing inter-feature mutual redundancy.
2. **Stage 2 (Skeleton Superset Extraction):** Apply a modified PC algorithm using conditional-independence (CI) testing to locate target neighborhood supersets.
3. **Stage 3 (Continuous Graph Optimization):** Map candidates into continuous space using a DAG-GNN autoencoder constrained by the local graph skeleton to isolate the true Markov Blanket (MV).

## Repository Structure
- `cancerbiomarkeridentification.ipynb`: Main end-to-end execution notebook.
- `README.md`: Project description and usage guide.
- `.gitignore`: Configured to ignore python cache files and dataset artifacts.

## Datasets
- **TCGA-LUAD:** Binary lung adenocarcinoma dataset (~555 samples, 59k genes).
- **SixCa-Co:** Multi-class disease expression matrix (~285 samples, 57k genes across 7 classes).

## Quickstart
1. Clone the repository:
   ```bash
   git clone [https://github.com/Arif1412/causal-biomarker-discovery.git](https://github.com/Arif1412/causal-biomarker-discovery.git)
   cd causal-biomarker-discovery
