# Graphify
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# 🔹 Load Raw Data from CSV
file_path = "data.csv"  # Change this to your file
df = pd.read_csv(file_path)

# 📊 Display First Few Rows
print("📊 Raw Data Preview:\n", df.head())

# 🔹 Set Seaborn Style
sns.set(style="whitegrid")

# 📌 1. Line Plot (Change column names accordingly)
plt.figure(figsize=(10, 5))
sns.lineplot(x=df["Date"], y=df["Sales"], marker="o", color="b")
plt.title("📈 Sales Over Time")
plt.xlabel("Date")
plt.ylabel("Sales")
plt.xticks(rotation=45)
plt.show()

# 📌 2. Bar Chart
plt.figure(figsize=(10, 5))
sns.barplot(x=df["Category"], y=df["Sales"], palette="viridis")
plt.title("📊 Sales by Category")
plt.xlabel("Category")
plt.ylabel("Sales")
plt.xticks(rotation=45)
plt.show()

# 📌 3. Scatter Plot
plt.figure(figsize=(8, 5))
sns.scatterplot(x=df["Sales"], y=df["Profit"], color="r")
plt.title("🔴 Sales vs Profit")
plt.xlabel("Sales")
plt.ylabel("Profit")
plt.show()
