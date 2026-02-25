# scRNA-seq Gene Expression Analysis

Jupyter notebook for exploring single-cell RNA-seq AnnData objects: UMI filtering and per-cell count extraction for genes of interest.

## Setup

```bash
conda env create -f envs/scrnaseq.yaml
conda activate scrnaseq
jupyter notebook
```

## Usage

Open `notebooks/gene_expression_analysis.ipynb` and edit the **CONFIG** cell at the top:

- `H5AD_PATH` — path to your `.h5ad` file
- `GENES_OF_INTEREST` — list of gene symbols to analyse
- `MIN_UMI` / `MAX_UMI` — UMI count thresholds for cell filtering (set after inspecting the distribution plot)
- `OUTPUT_CSV` — output filename for per-cell count table

Run cells in order. After Cell 3 (UMI distribution), update the thresholds and re-run from Cell 4 onwards.

## Outputs

- Per-cell count table (CSV) for all genes of interest
- Summary statistics (% expressing, mean, median)
- Violin plots and scatter plots
