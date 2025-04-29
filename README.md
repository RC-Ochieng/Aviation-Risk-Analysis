
# Aviation Risk Analysis Project

## Overview
This project aims to identify the safest aircraft models based on historical aviation accident data. The analysis involves loading, cleaning, and exploring the dataset to calculate risk scores for various aircraft models. The goal is to provide actionable insights for the company's expansion into aviation by recommending the safest aircraft to purchase.

## Project Structure
The project is organized into the following sections:

1. **Introduction**:  
   - Objective: Identify aircraft models with the lowest risk based on historical data.  
   - Tasks: Data loading, cleaning, exploratory analysis, and risk assessment.

2. **Data Loading**:  
   - The dataset `AviationData.csv` is loaded using pandas with `latin1` encoding to handle special characters.  
   - Initial exploration includes displaying the first and last few rows of the dataset.

3. **Data Cleaning**:  
   - Handling missing values in injury columns (`Total.Fatal.Injuries`, `Total.Serious.Injuries`, `Total.Minor.Injuries`).  
   - Creating a combined `Make_Model` column for standardized aircraft identification.  
   - Calculating a `Risk_Score` based on weighted injury data (fatal injuries weighted highest, followed by serious and minor injuries).

4. **Exploratory Data Analysis (EDA)**:  
   - The analysis ranks aircraft models from safest to least safe based on the calculated `Risk_Score`.  
   - The output includes a list of aircraft models sorted by their risk scores, providing a clear recommendation for the safest options.

## Key Findings
- The dataset contains over 88,000 entries with 33 columns, including details like event dates, locations, aircraft make/model, and injury statistics.  
- The `Risk_Score` is derived from a weighted sum of injuries, prioritizing fatal injuries (weight = 3), serious injuries (weight = 2), and minor injuries (weight = 1).  
- The analysis identifies aircraft models with the lowest risk scores, which are recommended for purchase due to their historically safer performance.

## Usage
1. **Prerequisites**:  
   - Python 3.x  
   - Libraries: pandas, numpy, matplotlib  

2. **Running the Notebook**:  
   - Clone the repository and navigate to the project directory.  
   - Install the required libraries:  
     ```bash
     pip install pandas numpy matplotlib
     ```
   - Open and run the Jupyter notebook `AviationRiskAnalysisNotebook.ipynb` to reproduce the analysis.

## Dataset
The dataset used in this project is `AviationData.csv`, which contains historical aviation accident records. Key columns include:
- `Event.Id`: Unique identifier for each event.  
- `Make_Model`: Combined field for aircraft make and model.  
- `Total.Fatal.Injuries`, `Total.Serious.Injuries`, `Total.Minor.Injuries`: Injury statistics used for risk calculation.  
- `Risk_Score`: Calculated score indicating the risk level of each aircraft model.

## Results
The notebook outputs a ranked list of aircraft models by their `Risk_Score`, from safest to least safe. This list serves as a practical guide for selecting low-risk aircraft for the company's aviation operations.

