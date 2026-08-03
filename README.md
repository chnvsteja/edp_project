# This is WEEK-1 Learnings

## Google Play Store Dataset – Load and Clean Data using Pandas

### Aim

To load the Google Play Store dataset, clean the data using Pandas, remove missing values and duplicate records, and prepare it for analysis.

---

## Step 1: Import the Pandas Library

```python
import pandas as pd
import numpy as np
```

### Explanation

- Pandas is used for data manipulation.
- NumPy is used for numerical operations.

---

## Step 2: Load the Dataset

```python
df = pd.read_csv("googleplaystore.csv")
```

### Explanation

- Loads the CSV file into a DataFrame.
- The DataFrame is stored in the variable `df`.

---

## Step 3: Display the First Five Rows

```python
df.head()
```

### Explanation

- Displays the first five records.

---

## Step 4: Check Dataset Information

```python
df.info()
```

### Explanation

- Displays column names.
- Displays data types.
- Displays non-null values.

---

## Step 5: Check Missing Values

```python
df.isnull().sum()
```

### Explanation

- Shows the number of missing values in each column.

---

## Step 6: Remove Missing Values

```python
df.dropna(inplace=True)
```

### Explanation

- Removes all rows containing missing values.

---

## Step 7: Check Duplicate Rows

```python
df.duplicated().sum()
```

### Explanation

- Counts duplicate rows.

---

## Step 8: Remove Duplicate Rows

```python
df.drop_duplicates(inplace=True)
```

### Explanation

- Removes duplicate records from the dataset.

---

## Step 9: Rename Columns

```python
df.rename(columns={
    "Content Rating":"Content_Rating",
    "Current Ver":"Current_Version",
    "Android Ver":"Android_Version"
}, inplace=True)
```

---

## Step 10: Save the Cleaned Dataset

```python
df.to_csv("cleaned_googleplaystore.csv", index=False)
```

### Explanation

- Saves the cleaned dataset as a new CSV file.

---

## Output

- ✔ Loaded the dataset successfully
- ✔ Removed missing values
- ✔ Removed duplicate rows
- ✔ Renamed columns
- ✔ Saved the cleaned dataset
