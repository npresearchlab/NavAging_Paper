# README

Welcome to the repository for **Bassil et al., 2025**: *"Distinct aging-related profiles of allocentric knowledge recall following navigation in an immersive, naturalistic, city-like environment"* (also nicknamed the NPRL "NavAging Paper").

Below is an explanation of the folder structure in this repository. Feel free to reach out to the Neural Plasticity Research Lab via our [website](https://npresearchlab.com) or contact Dr. Michael Borich at mborich@emory.edu with any questions.

---

## Folder Structure

### `data/`

Contains raw and processed data files:

- **`YA_Data/`** - Raw data from younger adults (YAs)
- **`OA_Data/`** - Raw data from older adults (OAs)
- **`non_nav_data.csv`** - Analyzed data for all non-NavCity measures (cognitive assessments, questionnaires, etc.)
- **`participants.csv`** - ID linking information to track participants in the lab with different IDs
- **`demographic_data.csv`** - Participant characteristics from study-specific questionnaire (gender, handedness, VR experience, video game usage, etc.)

### `data_analysis/`

Contains analysis scripts:

- **`0_runall.ipynb`** - Master script that runs all other analysis scripts to process raw data and create block-specific and averaged outcome measures for NavCity performance
  - **Note:** This file contains filepaths and inputs that need to be edited before use. Once configured, all other files can be run automatically.