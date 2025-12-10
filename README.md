# NavAging Paper Repository

[![DOI](https://img.shields.io/badge/DOI-pending-blue)]() <!-- Add your DOI when available -->

This repository contains the data, code, and materials supporting:

**Bassil et al., 2025**: *"Distinct aging-related profiles of allocentric knowledge recall following navigation in an immersive, naturalistic, city-like environment"*

**Authors**: [List your authors here]  
**Affiliation**: Neural Plasticity Research Lab, Emory University  
**Contact**: Dr. Michael Borich ([mborich@emory.edu](mailto:mborich@emory.edu))  
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

This repository provides complete reproducibility materials for our study examining age-related differences in spatial navigation and allocentric knowledge recall using an immersive, naturalistic virtual environment (NavCity). The study compares younger adults (YAs) and older adults (OAs) across multiple cognitive and navigational assessments.

**Key Features:**
- Raw and processed data from all participants
- Complete analysis pipeline from raw data to final figures
- Statistical analysis scripts
- Publication-ready figures
- Demographic and cognitive assessment data

---

## Repository Structure

```
NavAging_Paper/
│
├── data/                      # Raw and processed data files
│   ├── YA_Data/              # Younger adult participant data
│   ├── OA_Data/              # Older adult participant data
│   ├── non_nav_data.csv      # Non-NavCity cognitive assessments
│   ├── participants.csv      # Participant ID mapping
│   └── demographic_data.csv  # Participant demographics and characteristics
│
├── data_analysis/            # Data processing and analysis scripts
│   └── 0_runall.ipynb       # Master script to process all raw data
│
├── figure_creation/          # Scripts to generate manuscript figures
│
├── final_figures/            # Publication-ready figures (output)
│
├── stat_tests/               # Statistical analysis scripts
│
├── submission/               # Manuscript and supplementary materials
│
├── .gitignore
└── README.md
```

---

## Data

### `/data/`

This directory contains all experimental data:

- **`YA_Data/`**: Raw navigation and performance data from younger adult participants (ages 18-35)
- **`OA_Data/`**: Raw navigation and performance data from older adult participants (ages 60+)
- **`non_nav_data.csv`**: Compiled data from cognitive assessments including:
  - Montreal Cognitive Assessment (MoCA)
  - Trail Making Test (TMT)
  - Santa Barbara Sense of Direction Scale (SBSOD)
  - Other validated neuropsychological measures
- **`participants.csv`**: Cross-reference file linking participant IDs across different data collection systems
- **`demographic_data.csv`**: Self-reported participant information:
  - Age, gender, handedness
  - VR experience level
  - Video game usage
  - Education level
  - Other relevant demographic variables

**Data Format**: CSV files with headers, UTF-8 encoding  
**Missing Data**: Coded as `NA` or blank cells

---

## Code

### `/data_analysis/`

Contains Jupyter notebooks and Python scripts for data processing and analysis.

- **`0_runall.ipynb`**: Master orchestration script
  - Runs all analysis scripts in sequence
  - Processes raw NavCity data files
  - Generates block-specific and session-averaged metrics
  - Outputs cleaned datasets for statistical analysis
  - **⚠️ Important**: This file contains hardcoded file paths. You must update these paths before running:
    - Line XX: Set your local data directory
    - Line YY: Set output directory for processed files
    - Line ZZ: Specify figure output location

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

- Figure 1: [Brief description]
- Figure 2: [Brief description]
- Figure 3: [Brief description]
- Supplementary figures

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

**Installation:**

```bash
pip install -r requirements.txt
```

Or install individually:

```bash
pip install numpy pandas matplotlib seaborn scipy statsmodels jupyter
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
   pip install -r requirements.txt
   ```

3. **Run the analysis pipeline:**
   - Open `data_analysis/0_runall.ipynb` in Jupyter
   - Update file paths in the configuration section
   - Run all cells to reproduce analyses

4. **Generate figures:**
   - Navigate to `figure_creation/`
   - Run figure generation scripts
   - Outputs will be saved to `final_figures/`

### Reproducing Specific Analyses

To reproduce specific analyses or figures:

```bash
# Example: Generate Figure 2
cd figure_creation/
python generate_figure2.py

# Example: Run statistical tests
cd stat_tests/
jupyter notebook statistical_analyses.ipynb
```

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

<!-- Choose one of the following: -->

**Data**: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) - Data are freely available with attribution

**Code**: [MIT License](LICENSE) - Code is freely available for reuse and modification

<!-- Or if you prefer: -->
<!-- This work is licensed under [specify your license]. See LICENSE file for details. -->

---

## Submission Materials

The `/submission/` directory contains:
- Final manuscript PDF
- Supplementary materials
- Response to reviewers (if applicable)
- Revision history

---

## Contributing

We welcome questions, bug reports, and suggestions for improvements. Please:

1. Check existing [Issues](https://github.com/npresearchlab/NavAging_Paper/issues)
2. Open a new issue with detailed description
3. For data questions, contact Dr. Michael Borich at [mborich@emory.edu](mailto:mborich@emory.edu)

---

## Acknowledgments

This research was supported by [funding sources]. We thank all study participants and the research team members who contributed to data collection and analysis.

---

## Additional Resources

- **Lab Website**: [npresearchlab.com](https://npresearchlab.com)
- **Pre-registration**: [Link if applicable]
- **Preprint**: [Link if available]
- **OSF Project**: [Link if applicable]

---

**Last Updated**: December 2025  
**Repository Maintainer**: [Your Name/Lab Name]