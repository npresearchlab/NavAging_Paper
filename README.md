# NavAging Paper Repository

[![DOI](https://img.shields.io/badge/DOI-pending-blue)]() <!-- Add your DOI when available -->

Welcome to the repository for the paper ***"Distinct aging-related profiles of allocentric knowledge recall following navigation in an immersive, naturalistic, city-like environment"*** (also nicknamed the NPRL "NavAging Paper"). 

This project examines aging-related differences in spatial navigation in an immersive, naturalistic virtual environment (*NavCity*) and associated allocentric knowledge recall.

## What's Here?

This repository contains all **analysis code, figures, and statistical tests** associated with this study. 

All **data** for this paper can be found on the associated [NavAging OSF Project](https://osf.io/qmwyk/overview).

Below is an explanation of the folder structure in this repository. Feel free to reach out to the Neural Plasticity Research Lab via our [website](https://npresearchlab.com) or contact Yasmine Bassil at [ybassil@emory.edu](mailto:ybassil@emory.edu) with any questions.

## Citation & Details

> Bassil, Y., Kanukolanu, A., Funderburg, E., Cui, E., Brown, T., & Borich, M. R. (2025). Distinct aging-related profiles of allocentric knowledge recall following navigation in an immersive, naturalistic, city-like environment. *PsyArXiv*. https://osf.io/qmwyk.

**Authors**: Yasmine Bassil, Anisha Kanukolanu, Emma Funderburg, Emily Cui, Thackery Brown, Michael R. Borich
**Affiliation**: Neural Plasticity Research Lab, Emory University  
**Contact**: Dr. Michael Borich, PhD, DPT, PT ([mborich@emory.edu](mailto:mborich@emory.edu))  
**Lab Website**: [npresearchlab.com](https://npresearchlab.com)

---

## Table of Contents

- [Overview](#overview)
- [Repository Structure](#repository-structure)
- [Data](#data)
- [Code](#code)
- [Figures](#figures)
- [Requirements](#requirements)
- [Usage](#usage)
- [Citation](#citation)
- [License](#license)

---

## Overview

This repository provides complete reproducibility materials for our study examining aging-related differences in spatial navigation and allocentric knowledge recall using an immersive, naturalistic virtual environment (*NavCity*). The study compares younger adults (YAs) and older adults (OAs) across multiple cognitive and navigational assessments.

**Key Features:**
- Complete analysis pipeline from raw data to final figures
- Statistical analysis scripts
- Publication-ready figures

---

## Repository Structure

```
NavAging_Paper/
│
├── data_analysis/            # Data processing and analysis scripts
│   └── 0_runall.ipynb        # Master script to process all raw data
│   └── 1_calculate_outcomes.ipynb  # Calculates outcome measures from raw data
│   └── 2_merge_data.ipynb    # Collects outcome measures per block per participant in one dataframe
│   └── 3_average_data.ipynb  # Averages outcome measures over blocks per participant
│   └── 4_target_data.ipynb   # Creates dataframes for overall paths per block across participants
│   └── 5_graph_data.ipynb    # Creates overhead path map figures per block across participants
│   └── 6_post_analyses.ipynb # Cleans up data based on documented errors during data collection
|
├── figure_creation/          # Scripts to generate manuscript figures
│
├── final_figures/            # Publication-ready figures (output)
│
├── stat_tests/               # Statistical analysis scripts
│
├── .gitignore
├── LICENSE
└── README.md
```

---

## Data

### `/data/`

All experimental data can be found in the Open Science Framework (OSF) project associated with this study: [NavAging OSF Project](https://osf.io/qmwyk/overview)

---

## Code

### `/data_analysis/`

Contains Jupyter notebooks and Python scripts for data processing and analysis.

- **`0_runall.ipynb`**: Master orchestration script
  - Runs all analysis scripts (labeled 1 through 6) in sequence
  - Processes raw *NavCity* data files
  - Generates block-specific and session-averaged metrics
  - Outputs cleaned datasets for statistical analysis

**⚠️ Important**: This file contains hardcoded file paths. You must update file paths before running on your local machine. To get started, you may set the following:
  - Line 15: Set your local data directory for YA data
  - Line 16: Set your local data directory for OA data
  - Line 19: Set your local directory to analysis codes (scripts 0 through 6)

Outputs from analysis scripts will be located in the *parent directory* of the YA data and OA data, respectively.

**To Run the Complete Pipeline:**
1. Clone this repository
2. Install required packages (see [Requirements](#requirements))
3. Update file paths in `0_runall.ipynb`
4. Run all cells in `0_runall.ipynb`

### `/stat_tests/`

Statistical analysis scripts for hypothesis testing and generating results reported in the manuscript.

- Includes mixed-effects models
- Between-group comparisons (YA vs OA)
- Correlation analyses
- Effect size calculations

### `/figure_creation/`

Scripts to generate all manuscript figures from processed data.

- Figure 2: Included plots from `1_average_plots.Rmd` and `2_by_block_plots.Rmd` (for *NavCity* primary measures)
- Figure 3: Included plots from `1_average_plots.Rmd` and `2_by_block_plots.Rmd` (for *NavCity* secondary measures)
- Figure 4: Included plots from `4_corr_plots.Rmd` and `5_nara_plots.Rmd`
- Figure 5: Included plots from `6_cohorts_average_plots.Rmd` and `2_cohorts_by_block_plots.Rmd` (for *NavCity* primary measures)
- Figure 6: Included plots from `6_cohorts_average_plots.Rmd` and `2_cohorts_by_block_plots.Rmd` (for *NavCity* secondary measures)

**⚠️ Important**: All figure creation scripts contains hardcoded file paths. You must update file paths before running on your local machine.

---

## Figures

### `/final_figures/`

This directory contains publication-ready figures in high-resolution formats (PNG, PDF, SVG).

All figures follow journal specifications:
- 300+ DPI resolution
- Colorblind-friendly palettes
- Clear axis labels and legends

---

## Requirements

### Software Dependencies

**Python 3.8+** with the following packages:

```bash
numpy>=1.20.0
pandas>=1.3.0
matplotlib>=3.4.0
seaborn>=0.11.0
scipy>=1.7.0
statsmodels>=0.12.0
jupyter>=1.0.0
```

### Hardware Requirements

- Minimum 8GB RAM recommended
- ~500MB disk space for repository
- Standard computing hardware sufficient

---

## Usage

### Quick Start

1. **Clone the repository:**
   ```bash
   git clone https://github.com/npresearchlab/NavAging_Paper.git
   cd NavAging_Paper
   ```

2. **Install dependencies:**
   ```bash
   pip install numpy pandas matplotlib seaborn scipy statsmodels jupyter
   ```

3. **Run the analysis pipeline:**
   - Open `data_analysis/0_runall.ipynb` in preferred IDE
   - Update file paths in the configuration section
   - Run all cells to reproduce analyses

4. **Generate figures:**
   - Navigate to `figure_creation/`
   - Run figure generation scripts
   - Outputs will be saved to `final_figures/`

---

## Citation

If you use this code or data in your research, please cite:

```bibtex
@article{bassil2025navaging,
  title={Distinct aging-related profiles of allocentric knowledge recall following navigation in an immersive, naturalistic, city-like environment},
  author={Bassil, [FirstName] and [Co-authors]},
  journal={[Journal Name]},
  year={2025},
  volume={[Volume]},
  pages={[Pages]},
  doi={[DOI]}
}
```

---

## License

**Data**: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) - Data are freely available with attribution

**Code**: [MIT License](LICENSE) - Code is freely available for reuse and modification

---

## Contributing

We welcome questions, bug reports, and suggestions for improvements. Please:

1. Check existing [Issues](https://github.com/npresearchlab/NavAging_Paper/issues)
2. Open a new issue with detailed description
3. For data questions, contact Dr. Michael Borich at mborich [at] emory.edu

---

## Acknowledgments

This research was supported by [funding sources]. We thank all study participants and the research team members who contributed to data collection and analysis.

---

## Additional Resources

- **Lab Website**: [npresearchlab.com](https://npresearchlab.com)
- **Preprint**: [NavAging Preprint](https://osf.io/daq64)
- **OSF Project**: [OSF Data Repository](https://osf.io/qmwyk/overview)

---

**Last Updated**: December 2025  
**Repository Maintainer**: Yasmine Bassil, Neuroscience PhD Candidate, Neural Plasticity Research Lab, Emory University