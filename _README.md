Welcome to the README for this repository, which contains all code used to produce the Bassil et al., 2025 paper titled, "Distinct aging-related profiles of allocentric knowledge recall following navigation in an immersive, naturalistic, city-like environment" (also nicknamed the NPRL "NavAging Paper").

Below is an explanation of the folder structure in this repository. Feel free to reach out to the Neural Plasticity Research Lab via our website (npresearchlab.com) or contact Dr. Michael Borich (mborich [at] emory.edu) with any questions. 

*Folder Structure*
data
  YA_Data: contains raw data from younger adults (YAs)
  OA_Data: contains raw data from older adults (OAs)
  non_nav_data.csv: contains analyzed data for all non-NavCity measures (i.e., cognitive assessments, questionnaires, etc.)
  participants.csv: contains ID linking information to track participants in the lab with different IDs
  demographic_data.csv: contains information about participant characteristics from our study-specific questionnaire (i.e., gender, handedness, VR experience, video game usage, etc.)
data analysis
  0_runall.ipynb: contains the script that runs all other analysis scripts to take raw data and create block-specific and averaged outcome measures for NavCity performance. This file has filepaths and inputs that need to be edited to be used appopriately, and then all other files can be run automatically.

