# Pathogen-Data-Analysis-Training
 R training for descriptive and statistical data analysis of microbial and molecular pathogens in environmental samples.

This workshop uses simulated datasets representing common environmental microbiology and molecular surveillance data. Workshop objectives are to: 

    1. Practice data cleaning and preparation using realistic formats and variables; 
    2. Learn how to process multiple variables with efficient code;
    3. Practice using packages that generate formatted descriptive tables and manuscript-ready figures;
    4. Learn to implement statistical methods to assess associations between microbial and molecular pathogen data and survey data for epidemiological analyses and practice with simulated datasets.

## Datasets
1. microbial_data_simulated.csv (folder: /simulated_data/)

    Description: Simulated microbiological data from IDEXX and culture-based methods for environmental samples (e.g., effluent, compost, produce).

    Key variables include:

    sample_id: Encoded ID with household, sample type, and sample number.
    wet_weight, dry_weight, plate_weight: Used to calculate soil moisture.
    esbl_e_coli_cfu: ESBL-producing E. coli colony-forming units.
    small_cell_count and large_cell_count: IDEXX tray results for estimating most probable number (MPN) of target organisms (Total Coliform, E. coli, and antibiotic-resistant Total Coliform and antibiotic resistant E. coli. .

    Workshop tasks: Calculating derived variables (e.g., soil moisture, log-transformed concentrations), estimating MPNs using quantitray, and adjusting for moisture and sample volume.

2. TAC Data Files (folder: /simulated_data/simulated_cards/)

    Description: Simulated output from quantitative PCR (TaqMan Array Cards) output files.

    Format: Each .csv file represents a batch of 7 samples and 1 non-template control (NTC), formatted with standard output from qPCR software.

    Workshop tasks: Combining multiple .csv files into one data frame. Cleaning and transforming qPCR data (e.g., extracting household/sample IDs, generating detection indicators).
    
3. survey_data_simulated.csv (folder: /simulated_data/)

    Description: This file contains simulated survey data collected from household participants in a rural setting. The dataset is designed to reflect responses related to household demographics, sanitation practices, water access, hygiene behaviors, and reported health outcomes (e.g., diarrhea, recent antibiotic use).

    Key variables include:
    
    household_id: Unique identifier for each household
    respondent_age: Age of the respondent
    num_children_under5: Number of children under 5 in the household
    toilet_type: Type of toilet used (e.g., improved, unimproved, open defecation)
    handwashing_station: Presence of a handwashing station (yes/no)
    water_source: Primary drinking water source
    reported_diarrhea: Whether any household member had diarrhea in the past 7 days (yes/no)
    recent_antibiotic_use: Whether antibiotics were taken by any household member in the past month (yes/no)

    Workshop tasks: Import the dataset using read_csv() and inspect variable types. Use mutate() to create new variables such as a binary indicator for improved sanitation. Summarize prevalence of reported diarrhea and antibiotic use by household characteristics. Join survey data with microbiological or TAC datasets using household_id.
    

#### Output
During the workshop, you will generate the following additional datasets:  

    /clean_data/microbial_data_cleaned.csv

    /clean_data/tac_data_cleaned.csv

These files contain cleaned and transformed data, ready for statistical analysis or visualization in subsequent data analysis scripts.