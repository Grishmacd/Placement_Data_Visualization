# Placement_Data_Visualization

This notebook explores a **student placement dataset** and focuses on understanding placement outcomes using simple visualizations. The dataset is loaded from a CSV file and the notebook creates charts to show salary distribution and placement status distribution.

---

## Problem Statement

Using placement data, the goal is to:
- Understand how **salary values are distributed**
- Analyze the overall **placement status** of students (Placed / Not Placed)
- Visualize placement insights clearly using charts

---

## Selection of Data

**Dataset Type Used:** Structured tabular dataset (CSV)

File used in the notebook:
- `Placement_data_full_class.csv`

Important columns used:
- `salary`
- `status`

---

## Collection of Data

The dataset is uploaded in Google Colab using:
- `from google.colab import files`
- `files.upload()`

Then loaded using pandas:
- `df = pd.read_csv("Placement_data_full_class.csv")`

---

## Analysis and Visualizations Created

### 1) Dataset Preview
- `df.head()` is used to preview the first few rows and confirm the dataset loaded correctly.

### 2) Salary Distribution (Histogram)
- A histogram is created using:
  - `df['salary'].dropna()` (removes missing salary values)
- This helps understand the spread and frequency of salary values.

### 3) Placement Status Count (Bar Chart)
- `df['status'].value_counts()` is used to count how many students fall under each status.
- A bar chart displays the placement count comparison.

### 4) Placement Status Trend View (Area Chart)
- An area-style plot is created using `plt.fill_between()` on status counts.
- This gives a filled visual view of placement status counts.

### 5) Placement Status Share (Pie Chart)
- A pie chart shows the percentage split of each placement status using:
  - `autopct='%1.1f%%'`

---

## Main Libraries Used (and why)

1. `pandas`  
   - Loads the CSV dataset and selects columns like `salary` and `status`.

2. `matplotlib.pyplot`  
   - Creates histogram, bar chart, area chart (`fill_between`), and pie chart.

3. `seaborn`  
   - Imported for visualization styling/support (even if most plots are done using Matplotlib).

4. `google.colab.files`  
   - Uploads the CSV file into the Colab runtime.

---

## Output

- Dataset preview (first rows)
- Salary histogram showing frequency distribution
- Placement status bar chart (counts)
- Placement status area chart (filled comparison view)
- Placement status pie chart (percentage distribution)

---

## Developer
Grishma C.D

