# ============================================================
# Data Wrangling in Python: Combining, Merging, Reshaping, Pivoting
# ============================================================

# 1️⃣ Import pandas
import pandas as pd

# ------------------------------------------------------------
# 2️⃣ Create sample DataFrames
# ------------------------------------------------------------
# First dataset
df1 = pd.DataFrame({
    'ID': [1, 2, 3, 4],
    'Name': ['Alice', 'Bob', 'Charlie', 'David'],
    'Age': [25, 30, 35, 40]
})

# Second dataset
df2 = pd.DataFrame({
    'ID': [3, 4, 5, 6],
    'Department': ['HR', 'IT', 'Finance', 'Marketing'],
    'Salary': [40000, 50000, 60000, 70000]
})
print(df1)
print(df2)
# -----------------------------------------------------------
# 3️⃣ Merge DataFrames
# ------------------------------------------------------------
# Inner join (only matching IDs)
merged_inner = pd.merge(df1, df2, on='ID', how='inner')

# Outer join (all IDs from both)
merged_outer = pd.merge(df1, df2, on='ID', how='outer')

print("===== Inner Merge =====")
print(merged_inner)

print("\n===== Outer Merge =====")
print(merged_outer)

# ------------------------------------------------------------
# 4️⃣ Concatenation
# ------------------------------------------------------------
df3 = pd.DataFrame({
    'ID': [7, 8],
    'Name': ['Eva', 'Frank'],
    'Age': [28, 33]
})

combined = pd.concat([df1, df3], ignore_index=True)
print("\n===== Concatenated Data =====")
print(combined)

# ------------------------------------------------------------
# 5️⃣ Reshaping with melt (wide → long)
# ------------------------------------------------------------
melted = pd.melt(df1,
                 id_vars=['ID'],
                 value_vars=['Name', 'Age'],
                 var_name='Attribute',
                 value_name='Value')

print("\n===== Melted Data =====")
print(melted)

# ------------------------------------------------------------
# 6️⃣ Pivoting (long → wide)
# ------------------------------------------------------------
data = pd.DataFrame({
    'Month': ['Jan', 'Jan', 'Feb', 'Feb'],
    'Department': ['HR', 'IT', 'HR', 'IT'],
    'Revenue': [1000, 1500, 1200, 1600]
})

pivoted = data.pivot(index='Month',
                     columns='Department',
                     values='Revenue')

print("\n===== Pivoted Table =====")
print(pivoted)
