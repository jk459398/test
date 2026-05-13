# Spatiotemporal Signal Propagation Analysis

## Project Description
This project investigates the intercellular propagation and coordination of extracellular signal-regulated kinase (ERK) signaling within epithelial cell populations using single-cell tracking data. By employing graph-based exposure metrics and computing the Relative Risk ($RR$), the study systematically evaluates how different oncogenic mutations alter spatiotemporal signaling relay scales, paracrine communication speeds, and local coordination robustly across varying analytical parameters.

## Environment Setup
* **Python Version:** Python 3.12 or higher is recommended.
* **Installation:** Install all required dependencies via the provided `requirements.txt` file.

```bash
# Optional: Create and activate a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

# Install required packages
pip install -r requirements.txt
Step-by-Step Reproduction CommandsTo fully reproduce the analysis and generate all output deliverables for Part A, execute the following Jupyter notebooks sequentially. You can run them directly from the command line using nbconvert or open them in your IDE (Jupyter/VS Code) and select "Restart & Run All".Task A1: Mutation ComparisonEvaluates spatial coordination across Wild Type (WT) and mutant cell lines using multi-block summaries and statistical hypothesis testing.Bashjupyter nbconvert --to notebook --execute TaskA1_MutationComparison.ipynb
Task A2: Lagged Exposure AnalysisInvestigates communication speeds by shifting neighbor activation timestamps across temporal lags ($\tau$) to identify the optimal propagation timescale ($\tau^*$).Bashjupyter nbconvert --to notebook --execute TaskA2_LaggedExposure.ipynb
Task A3: Parameter Robustness AssessmentTests the sensitivity and statistical stability of the Relative Risk metric across a sweep of spatial neighborhood radii ($r$).Bashjupyter nbconvert --to notebook --execute TaskA3_ParameterRobustness.ipynb
Generated Output FilesExecuting the tasks above will generate the following primary deliverables in the outputs/ directory:TaskOutput File NameDescriptionA1mutations_comparison_table.csvSummary statistics (mean RR, standard error, adjusted p-values) comparing mutants to WT.A1mutations_comparison_plot.pngBar plot with error bars illustrating mutant RR values against the WT baseline.A2lagged_exposure_plot_AKT_PTEN.pngLine plot of $RR(\tau)$ vs. lag $\tau$ displaying propagation timescales and $\tau^*$ markers.A3A3_full_parameter_sweep_r.csvComprehensive data table containing all graph and exposure parameters across the spatial radius sweep.A3parameter_robustness_radius.pngRobustness curve demonstrating how Relative Risk scales with spatial radius $r$.