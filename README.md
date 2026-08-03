# Activity Data Exploration (STEG Billing History)
This repository/folder contains an exploratory data analysis and preprocessing pipeline for the billing history of the Tunisian electricity and gas company's (STEG) customers from 2005 to 2019. 
The main workflow is documented in the Jupyter Notebook `activity_data_explo.ipynb`.
## Dataset Overview
- **Source Dataset:** `STEG_BILLING_HISTORY.csv`
- **Description:** Contains millions of billing records spanning 14 years, providing insights into consumption levels, tariff types, and meter characteristics.
- **Key Features:** `client_id`, `invoice_date`, `tarif_type`, `counter_number`, `counter_code`, `consommation_level_1` through `4`, `old_index`, `new_index`, `months_number`, and `counter_type`.
## Tasks & Objectives
The notebook addresses several data preprocessing and exploration tasks:
1. **Data Loading & Inspection:**
   - Loading the large dataset efficiently.
   - Examining the first 10 rows and reviewing the data types.
   - Determining the total number of rows, columns, and the memory space consumed.
2. **Missing Values Handling:**
   - Inspecting the dataset for potential missing values (found in `counter_number` and `reading_remarque`).
   - Applying strategies to handle missing data, such as dropping the `reading_remarque` column and removing records with a missing `counter_number`.
3. **Data Manipulation & Transformation:**
   - Querying and selecting billing records for specific clients (e.g., `client_id = 'train_Client_0'`).
   - Cleaning up the DataFrame by deleting unnecessary columns (e.g., `counter_statue`).
   - Encoding categorical features, such as transforming the `counter_type` column (ELEC/GAZ) into a numeric format for future modeling.
## Project Structure
- `activity_data_explo.ipynb`: The main Jupyter Notebook containing the data exploration and preprocessing steps.
- `STEG_BILLING_HISTORY.csv`: The primary dataset used for the analysis.
- `data_explo.ipynb` / `cleaned_baby_data.csv`: Other exploratory notebooks and datasets included in the workspace.
## Requirements
To run the notebook successfully, you will need:
- Python 3.x
- `pandas` for data manipulation
- Jupyter Notebook or JupyterLab
## Usage
1. Clone or download the folder.
2. Ensure `STEG_BILLING_HISTORY.csv` is present in the same directory as the notebook.
3. Open `activity_data_explo.ipynb` using Jupyter Notebook and execute the cells sequentially.
