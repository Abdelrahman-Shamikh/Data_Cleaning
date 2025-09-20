<div id="top">

<!-- HEADER STYLE: CLASSIC -->
<div align="center">

<img src=".\image\datacleaning.jpg" width="30%" style="position: relative; top: 0; right: 0;" alt="Project Logo"/>

# DATA CLEANING PROJECT

<em></em>

<!-- BADGES -->
<!-- local repository, no metadata badges. -->

<em> A comprehensive data cleaning and preprocessing pipeline for student academic data</em>

<em>Built with: Python • Pandas • NumPy • Matplotlib • Seaborn • Jupyter Notebook</em>

</div>
<br>

---

## Table of Contents

1. [Overview](#overview)  
2. [Features](#features)  
3. [Project Structure](#project-structure)  
4. [Getting Started](#getting-started)  
   - [Prerequisites](#prerequisites)  
   - [Installation](#installation)  
   - [Usage](#usage)  
5. [Testing](#testing)  
6. [Data Cleaning Process](#data-cleaning-process)  
7. [Results](#results) 
8. [Contribution](#contribution)
9. [Acknowledgments](#Acknowledgments)

---

## Overview


This project demonstrates a comprehensive data cleaning workflow for student academic records. The dataset contains information about 77 students including demographics, academic performance, and study habits. The cleaning process addresses common data quality issues including inconsistent categorical values, missing data, duplicate records, and outliers.

---

## Features

### 1. Data Quality Assessment
- **Dataset structure analysis:** 77 rows, 11 columns  
- **Missing value handling:** Identification and treatment  
- **Duplicate record detection:** Identification and removal  

### 2. Data Standardization
- **Categorical variable normalization:** Gender, country, education, residence  
- **Inconsistent value mapping:** Correction and standardization  
- **Data type optimization:** Ensure proper storage and processing  

### 3. Missing Data Imputation
- **Numerical variables:** Comparison of mean vs. median imputation  
- **Categorical variables:** Mode imputation  
- **Statistical validation:** Evaluate imputation effectiveness  

### 4. Outlier Detection and Treatment
- **Visualization:** Box plots for numerical variables  
- **Detection:** Range-based identification of outliers  
- **Correction:** Transformation for realistic value ranges  

### 5. Data Validation
- **Constraint enforcement:** Exam scores (0–100), reasonable age ranges  
- **Unit correction:** Normalization of study hours  
- **Final integrity checks:** Ensure consistency and correctness of the dataset

---

## Project Structure

```sh
└── Cleandata/
    ├── Cleaned_data.csv
    └── Cleaning Data.ipynb
    └── image/
    └── bi.csv
```

### Project Index

<details open>
	<summary><b><code>CLEANDATA/</code></b></summary>
	<!-- __root__ Submodule -->
	<details>
		<summary><b>__root__</b></summary>
		<blockquote>
			<div class='directory-path' style='padding: 8px 0; color: #666;'>
				<code><b>⦿ __root__</b></code>
			<table style='width: 100%; border-collapse: collapse;'>
			<thead>
				<tr style='background-color: #f8f9fa;'>
					<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
					<th style='text-align: left; padding: 8px;'>Summary</th>
				</tr>
			</thead>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='Cleandata/blob/master/Cleaning Data.ipynb'>Cleaning Data.ipynb</a></b></td>
					<td style='padding: 8px;'>Jupyter notebook containing the full data cleaning workflow.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='Cleandata/blob/master/cleaned_data.csv'>cleaned_data.csv</a></b></td>
					<td style='padding: 8px;'>Final cleaned dataset after preprocessing.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='Cleandata/blob/master/bi.csv'>bi.csv</a></b></td>
					<td style='padding: 8px;'>Original dataset file used for data cleaning.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='Cleandata/tree/master/image'>image/</a></b></td>
					<td style='padding: 8px;'>Assets folder containing project visuals (e.g., <code>datacleaning.jpg</code>).</td>
				</tr>
			</table>
		</blockquote>
	</details>
</details>

---

## Getting Started

### Prerequisites
- **Python:** 3.7 or higher  
- **Jupyter Notebook**  

### Required Python Packages
- `pandas`  
- `numpy`  
- `matplotlib`  
- `seaborn`

### Installation

Build Cleandata from the source and intsall dependencies:

1. **Clone the repository:**

    ```sh
    ❯ git clone https://github.com/Abdelrahman-Shamikh/Data_Cleaning.git
    ```

2. **Navigate to the project directory:**

    ```sh
    ❯ cd Cleandata
    ```

3. **Install the dependencies:**
    ```sh
    ❯    pip install pandas numpy matplotlib seaborn jupyter
    ```

### Usage

#### 1. Start Jupyter Notebook:

    ```sh
    ❯ jupyter notebook
    ```
#### 2. Run the Cleaning Pipeline
- Open `Cleaning Data.ipynb`  
- Execute all cells sequentially  
- Review the cleaning process and results
#### 3. Access Cleaned Data
- The cleaned dataset is saved as `Cleaned_data.csv`  
- Import it for further analysis

## Testing

The notebook includes validation checks throughout:  
- **Data integrity verification**  
- **Statistical comparison before/after imputation**  
- **Outlier detection validation**  
- **Final data quality assessment**
## Data Cleaning Process

### 1. Initial Data Assessment
- **Shape:** 77 rows × 11 columns  
- **Variables:** `fNAME`, `lNAME`, `Age`, `gender`, `country`, `residence`, `entryEXAM`, `prevEducation`, `studyHOURS`, `Python`, `DB`  
- **Issues identified:** Inconsistent categorical values, missing data in `Python` column (2 values)  

### 2. Categorical Data Standardization

**Country Normalization**
- `norway`, `Norge`, `Norway` → `norway`  
- `Rsa`, `South Africa` → `south africa`  
- `UK` → `united kingdom`  
- `somali` → `somalia`  

**Education Level Standardization**
- `Masters`, `master` → `master`  
- `Bachelors`, `Barrrchelors` → `bachelor`  
- `Diploma`, `diploma`, `DIPLOMA`, `Diplomaaa` → `diploma`  
- `HighSchool`, `High School` → `high school`  

**Gender Standardization**
- `Female`, `female`, `F` → `female`  
- `Male`, `male`, `M` → `male`  

**Residence Standardization**
- `BI-Residence`, `BIResidence`, `BI_Residence` → `BI Residence`  

### 3. Missing Data Treatment
- **Python column:** 2 missing values imputed using mean (75.85)  
- **Categorical variables:** Mode imputation applied  
- **Validation:** Compared mean vs. median imputation with identical results  

### 4. Duplicate Detection
- **Result:** 0 duplicate records found  

### 5. Outlier Treatment
- `studyHOURS`: Divided by 10 for realistic weekly hours  
- `Age`: Constrained to 20–80 years range  
- Exam scores (`entryEXAM`, `Python`, `DB`): Constrained to 0–100 range  
- **Reasoning:** IQR method produced unrealistic bounds; manual constraints applied  

### 6. Data Type Optimization
- Converted `Python` and `studyHOURS` to integer type  
- Ensured consistent data types across all columns  

## Results

### Final Dataset Characteristics
- **Records:** 77 students  
- **Complete cases:** 100% (no missing values)  
- **Data quality:** All values within realistic ranges  
- **Standardization:** Consistent categorical values  
- **File output:** `Cleaned_data.csv`  

### Key Transformations Applied
- Standardized 13 different country representations to consistent format  
- Normalized 10 education level variants to 5 standard categories  
- Unified 6 gender representations to 2 standard values  
- Corrected study hours scale from monthly to weekly basis  
- Applied realistic constraints to all numerical variables

---
## Contribution 

1. **Fork the Repository**: Start by forking the project repository to your LOCAL account.
2. **Clone Locally**: Clone the forked repository to your local machine using a git client.
   ```sh
   git clone Cleandata
   ```
3. **Create a New Branch**: Always work on a new branch, giving it a descriptive name.
   ```sh
   git checkout -b new-feature-x
   ```
4. **Make Your Changes**: Develop and test your changes locally.
5. **Commit Your Changes**: Commit with a clear message describing your updates.
   ```sh
   git commit -m 'Implemented new feature x.'
   ```
6. **Push to LOCAL**: Push the changes to your forked repository.
   ```sh
   git push origin new-feature-x
   ```
7. **Submit a Pull Request**: Create a PR against the original project repository. Clearly describe the changes and their motivations.
8. **Review**: Once your PR is reviewed and approved, it will be merged into the main branch. Congratulations on your contribution!
</details>



---
## Acknowledgments

- Developed as a Depi intern at the Ministry of Communication under the supervision of Eng. Baraa Abu Sallout

---

<div align="right">

[![][back-to-top]](#top)

</div>


[back-to-top]: https://img.shields.io/badge/-BACK_TO_TOP-151515?style=flat-square


---
