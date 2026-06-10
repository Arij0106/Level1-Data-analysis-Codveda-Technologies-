# Level1-Data-analysis-Codveda-Technologies-

# Coveda Technologies Internship - Tasks 1 & 3 Portfolio

This repository contains my implementations for **Task 1 (Data Cleaning & Preprocessing)** and **Task 3 (Basic Data Visualization)** using the classic Iris dataset.

---
## Project Structure & Execution Workflow

###  Task 1: Data Cleaning and Preprocessing
The goal was to audit the dataset structure, handle missing entries, and remove data redundancy before feeding it into any analysis.

1. **Data Loading**: Mounted Google Drive and read the raw `iris.csv` file into a Pandas DataFrame.
2. **Structural Audit (`df.info()`)**: Confirmed a dataset size of 150 rows across 5 columns (4 floating-point metrics and 1 categorical text column).
3. **Missing Values Check (`df.isnull().sum()`)**: Verified there were 0 null values across all features.
4. **Deduplication (`df.duplicated().sum()`)**: Found **3 duplicate entries** (`np.int64(3)`).
5. **Data Refinement**: Removed the duplicate rows and sequentially realigned the tracking order using:
   ```python
   df = df.drop_duplicates().reset_index(drop=True)
   ```

---

###  Task 3: Basic Data Visualization
Using `matplotlib` and `seaborn`, I constructed three distinct chart styles, applied best-practice layouts, and exported clean image reports.

#### 1. Bar Plot (Categorical Comparison)
* **Objective**: Compare numeric averages across categories.
* **Implementation**: Plotted the average petal length across the different Iris species. The `hue` parameter was mapped cleanly with `legend=False` to respect the latest Seaborn standards.
* **Output saved as**: `plot1.png` (300 DPI)

#### 2. Line Chart (Trend Tracking)
* **Objective**: Track variations along an index or sequence.
* **Implementation**: Mapped the evolution of `sepal_length` across sample indices, colored explicitly by target species.
* **Output saved as**: `plot2.png` (300 DPI)

#### 3. Scatter Plot (Relationship Analysis)
* **Objective**: Evaluate correlation patterns between two numerical variables.
* **Implementation**: Demonstrated the positive correlation between `petal_length` and `petal_width`, grouping classifications through distinct shapes and colors.
* **Output saved as**: `plot3.png` (300 DPI)

---

##  Tech Stack
* **Python 3**
* **Pandas** & **NumPy** (Data wrangling)
* **Matplotlib** (Figure management and image exports)
* **Seaborn** (Aesthetic statistics rendering)

---

##  How to Run the Environment
1. Open the project in Google Colab.
2. Link your active Google Drive to retrieve your `iris.csv`.
3. Execute all code blocks. The script will automatically filter out duplicates and generate 3 production-grade visual files (`plot1.png`, `plot2.png`, `plot3.png`) within your environment root folder.
