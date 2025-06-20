## Activity #1 - Computational Thinking with the Titanic Dataset using Python

The whole code:
```py
import pandas as pd
# Load the dataset
df = pd.read_csv("titanic.csv")
# Display the first few rows
df.head()

# Checking null values
df.isnull().sum()

# Getting the average of the "Survived" column with age = null
df["Survived"].mean()

# Getting the average of the "Survived" column without age = null
df_cleaned = df.dropna(subset=["Age"])
df_cleaned["Survived"].mean()

import matplotlib.pyplot as plt
# Plot age distribution of survivors vs. non-survivors
plt.hist(df[df["Survived"] == 1]["Age"].dropna(), bins=20, alpha=0.5, label="Survived")
plt.hist(df[df["Survived"] == 0]["Age"].dropna(), bins=20, alpha=0.5, label="Did Not Survive")
plt.legend()
plt.xlabel("Age")
plt.ylabel("Count")
plt.show()
```

### Questions:

1. Up to this point, determine the underlying tasks needed to be done for loading and handling the data based on the steps described in this part? Write this as a text in your Colab notebook
   - This uses pandas library which uses the `read_csv()` method that uses "titanic.csv" as the file to navigate and change. Then, the `head()` method returns first few rows. By default, it is 5, but you can change the row display.
2. Using computation thinking, determine the blank values in the data. Write the algorithm as a text in your Google Colab. Which columns contain missing values? Should we remove or fill them?
   - There are three null columns: Age, Cabin, and Embarked. The columns Cabin & Embarked can be filled with N/A values. However, the age column is difficult to provide N/A values. In conclusion, while the cabin & embarked can be filled up, removing the null age columns is better than providing N/A that can hinder getting the mean value.
3. Using computation thinking, determine the survival rate of all passengers in the dataset. Write the algorithm as a text in your Google Colab. What can you deduce on the survival rate of the passengers?
   - Based on the given dataset, there is 0.38% repeating percent of survival rate. On the other hand, if we removed the age columns being null, the survival rate becomes 0.40%.
4. Using computation thinking, determine the average age of the survivors and non-survivors in the dataset. Write the algorithm as a text in your Google Colab. Does age impact survival? How?
   - Based on the graph, the ages 20-30 has the highest death than the elderly. It is because during the 1900s where ethics and morals are different from modern times, the elderly, pregnant women, and children are permitted to embark the rafts provided by the ship. But due to overwhelming number of passengers and the number of rafts, it cannot cater all passengers, resulting in the deaths of young to adults.