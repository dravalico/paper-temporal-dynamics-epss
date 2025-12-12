# Analysing the Temporal Dynamics of the Exploit Prediction Scoring System (EPSS)

This repository contains two Jupyter notebooks used for the analysis presented in the paper "Analysing the Temporal Dynamics of the Exploit Prediction Scoring Systems (EPSS)". Both notebooks are already executed and include all output figures, exactly as shown in the paper. In addition, they contain several other plots and exploratory visualizations that go beyond what is included in the manuscript.

- [1_epss3_current.ipynb](1_epss3_current.ipynb): contains analysis performed on EPSS and the combination with CVSS and CPE as well as KEV
- [2_cvss_cpe_21-24.ipynb](2_cvss_cpe_21-24.ipynb): focuses on CVE's metadata (i.e., CVSS and CPE) availability and readiness

To be able to run the code, please refer to the following section.

## Run the code

1. Clone the repository (requires [`git`](https://git-scm.com/)) and move into the project directory:

    ```bash
    git clone https://github.com/dravalico/paper-temporal-dynamics-epss
    cd paper-temporal-dynamics-epss
    ```

2. Download the [zipped dataset hosted on Zenodo](https://doi.org/10.5281/zenodo.15807706)
3. **Extract the archive and place its contents in the root directory of the project**
4. Check the following prerequisites before starting

### Prerequisites

- [Python](https://www.python.org/); the code was developed with Python 3.9.13 and also tested with Python 3.9.6
- An environment with Jupyter support (e.g., Jupyter Notebook, JupyterLab, or VS Code with the Jupyter extension)
- [LaTeX](https://www.latex-project.org/) (used for plot rendering)

   If LaTeX is _not_ available, you need to edit the third cell where `PLOT_ARGS` is defined (in both notebooks) by removing the following lines:

   ```python
   'style': 'latex',
   'rcParams': {'text.latex.preamble': r'\usepackage{amsmath}'}
   ```

   Please note that without LaTeX, some plot titles or axis labels may not display correctly.
- All code was developed using Python packages in a specific version, listed in the second cell of each notebook; to run the code without having to modify it, simply execute that cell
