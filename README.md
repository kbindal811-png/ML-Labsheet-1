# ML-Labsheet-1


Q1
import sys
print("Python Version:") print(sys.version)

Q2

pip install notebook jupyter notebook

Q3

pip install numpy
import numpy as np print("NumPy Version:", np.version)

Q4

pip install pandas
import pandas as pd print("Pandas Version:", pd.version)

Q5

pip install matplotlib
import matplotlib.pyplot as plt
x = [1, 2, 3, 4, 5] 
y = [10, 20, 15, 25, 30] 
plt.plot(x, y, marker="o") plt.title("Simple Line Plot") plt.xlabel("X Values") 
plt.ylabel("Y Values") 
plt.show()

Q6

import seaborn as sns
import matplotlib.pyplot as plt
data = sns.load_dataset("tips")
sns.scatterplot(data=data, x="total_bill", y="tip")
plt.title("Total Bill vs Tip")
plt.show()

Q7

pip install scikit-learn
import sklearn print("Scikit-learn Version:", sklearn.version)

Q8
name = input("Enter your name: ") print("Hello", name) print("Welcome to Python Programming!")

Q9
num1 = 10 num2 = 20 total = num1 + num2 print("First Number:", num1) print("Second Number:", num2) print("Sum =", total)

Q10

Create virtual environment:
python -m venv myenv

Activate on Windows:
myenv\Scripts\activate

Install required libraries:
pip install numpy pandas matplotlib seaborn scikit-learn

Check installed libraries:
pip list

Deactivate virtual environment:
deactivate

Q11

data = pd.read_csv("sample_data.csv") print(data)

Q12

data = pd.read_csv("sample_data.csv") print(data.head())

Q13

data = pd.read_csv("sample_data.csv") print(data.tail())

Q14

data = pd.read_csv("sample_data.csv") rows, columns = data.shape print("Total Rows:", rows) print("Total Columns:", columns)

Q15

data = pd.read_csv("sample_data.csv") print(data.columns)

Q16

data = pd.read_csv("sample_data.csv") print(data.dtypes)

Q17

data = pd.read_csv("sample_data.csv") print(data.describe())

Q18

data = pd.read_csv("sample_data.csv") data.info()

Q19

data = pd.read_csv("sample_data.csv") print(data.isnull())

Q20

data = pd.read_csv("sample_data.csv") print(data.isnull().sum())

Q21

data = pd.read_csv("sample_data.csv") print(data["Department"].unique())

Q22

data = pd.read_csv("sample_data.csv") print(data["Department"].value_counts())

Q23

import pandas as pd
data = pd.read_csv("student_data.csv")
data = data.rename(columns={
    "Name": "Student_Name",
    "Marks": "Student_Marks"
})
print(data)

Q24

import pandas as pd
data = pd.read_csv("student_data.csv")
selected_data = data.loc[0:2, ["Name", "Marks"]]
print(selected_data)

Q25

data = pd.read_csv("sample_data.csv") result = data.iloc[0:5, 0:2] print(result)

Q26

data = pd.read_csv("sample_data.csv") result = data[data["Age"] > 20] print(result)

Q27

data = pd.read_csv("sample_data.csv") sorted_data = data.sort_values(by="Age") print(sorted_data)

Q28

data = pd.read_csv("sample_data.csv") data["Status"] = "Active" print(data)

Q29

data = pd.read_csv("sample_data.csv") data = data.drop("Status", axis=1) print(data)

Q30

data = pd.read_csv("sample_data.csv") data = data.drop_duplicates() print(data)

Q31

data = pd.read_csv("sample_data.csv") data.to_csv("modified_data.csv", index=False) print("Dataset saved successfully.")

Q32

from sklearn.datasets import load_iris iris = load_iris() print("Feature Data:") print(iris.data) print("Target Data:") print(iris.target)

Q33

data = pd.read_csv("sample_data.csv") plt.hist(data["Age"], bins=5, edgecolor="black") plt.title("Histogram of Age") plt.xlabel("Age") plt.ylabel("Frequency") plt.show()

Q34

data = pd.read_csv("sample_data.csv") plt.scatter(data["Age"],data["Marks"]) plt.title("Relationship between Age and Marks") 
plt.xlabel("Age") 
plt.ylabel("Marks") 
plt.show()

Q35

data = pd.read_csv("sample_data.csv") correlation=data.select_dtypes(include="number").corr() sns.heatmap(correlation, annot=True, cmap="coolwarm") plt.title("Correlation Heatmap") plt.show()