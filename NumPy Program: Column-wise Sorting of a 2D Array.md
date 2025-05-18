## NAME: DEEPIKA P
## REGISTER NO: 212223240024

# NumPy Program: Column-wise Sorting of a 2D Array

## 🎯 Aim
To write a NumPy program that converts a 1-D array into a 2-D array with 3 rows..

## 🧠 Algorithm

1. Import the numpy module.

2. Create a 1-D array with the given elements.

3. Use the .reshape() method with 3 rows and appropriate number of columns (len(array)//3).

4. Print the original array and the reshaped 2-D array.

## 🧾 Program
import numpy as np

# Create a 1-D array
array_1d = np.array(eval(input()))

# Convert the 1-D array to a 2-D array with 3 rows
array_2d = np.reshape(array_1d, (3, -1))

# Print the result
print("The original array:")
print(f" {array_1d}")

print("\n3 x 3 Array:")
print(f" {array_2d}")

## Output
![Screenshot 2025-05-18 205944](https://github.com/user-attachments/assets/0eb1e527-d380-4c0b-a4ff-4709b886f09c)

## Result
The program successfully reshapes the 1-D array into a 3x3 2-D array as required.

# # NumPy Program: Create a numPy program to delete the second column from a given array and insert the given new column in its space.

## 🎯 Aim
To delete the second column from a NumPy array and insert a new column at the same position.

## 🧠 Algorithm
1. Import the NumPy library.

2. Define the original 2D array.

3. Define the new column to be inserted.

4. Use np.delete() to remove the second column (index 1) from the original array along axis 1.

5. Use np.insert() to insert the new column at index 1 along axis 1.

6. Print the original array, array after deletion, and array after insertion.

## 🧾 Program

import numpy as np\
A=np.array(eval(input()))\
print("Printing Original array")\
print(A)

modified=np.delete(A,1,axis=1)\
print("Array after deleting column 2 on axis 1")\
print(modified)

column=np.array(eval(input()))

ans=np.insert(modified,1,column,axis=1)\
print("Array after inserting column 2 on axis 1")\
print(ans)

## Output
![Screenshot 2025-05-18 210702](https://github.com/user-attachments/assets/c6a98ed2-6738-4633-a293-554e6f496ba3)

## Result
The program deletes the second column successfully and inserts the new column of 10s in its place as expected.

# NumPy Program: Create a numpy program for the following problem statement.You are given a 2-D array with dimensions NXM.

## 🎯 Aim
To write a NumPy program that finds the maximum of the minimum values of each row in a 2-D array.
## 🧠 Algorithm
1. Import the numpy library.

2. Create a 2-D NumPy array using the given input.

3. Apply np.min() on axis 1 (row-wise) to get the minimum of each row.

4. Apply np.max() to get the maximum of these minimum values.

5. Print the result.

## 🧾 Program
import numpy as np\
n,m=map(int,input().split())\
A=np.array([list(map(int,input().split()))for _ in range(n)])\
min_v=np.min(A,axis=1)\
max_v=np.max(min_v)\
print(max_v)

## Output
![Screenshot 2025-05-18 211111](https://github.com/user-attachments/assets/e6efdb50-1932-4039-8bf4-dcb472f04d0e)

## Result
The program successfully computes the maximum of the row-wise minimum values for a given 2-D array.

# Pandas Program: Create and Display a DataFrame with Custom Index Labels

## 🎯 Aim

To create and display a **DataFrame** using the **Pandas** library in Python from a given dictionary, and apply specific index labels to the rows.

## 🧠 Algorithm

1. **Import Libraries**: Import the required libraries – `pandas` and `numpy`.
2. **Create Dictionary**: Define a dictionary `exam_data` with keys: `'name'`, `'score'`, `'attempts'`, and `'qualify'`.
3. **Index Labels**: Create a list of custom index labels called `labels`.
4. **Create DataFrame**: Use `pd.DataFrame()` to create the DataFrame by passing the dictionary and index labels.
5. **Display Output**: Display the DataFrame using `print()` or by simply calling the DataFrame variable.


## 💻 Program

import pandas as pd
import numpy as np

# Provided data
data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}

# Provided index labels
index_labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']

# Create DataFrame
df = pd.DataFrame(data, index=index_labels)

# Display the DataFrame
print(df)


## Output
![Screenshot 2025-05-18 211324](https://github.com/user-attachments/assets/d135145d-0ca3-449e-b500-bc2c9de6627a)

## Result
The program successfully creates and displays a DataFrame using dictionary data with custom index labels.

# 🧪 Pandas Program: Join Two DataFrames Along Rows

## 🎯 AIM

To write a Python program using Pandas to **join two DataFrames along rows** (row-wise concatenation) and assign all data to a new DataFrame.

---

## 🧠 ALGORITHM

1. **Import Libraries**: Import the `pandas` library.
2. **Create First DataFrame**: Use a dictionary to create `student_data1`.
3. **Create Second DataFrame**: Use another dictionary to create `student_data2`.
4. **Concatenate DataFrames**: Use `pd.concat()` with `axis=0` to concatenate both DataFrames row-wise.
5. **Display Result**: Print the new combined DataFrame.

---

## 💻 Program

import pandas as pd

# Input dataframes
df1 = pd.DataFrame({
    's_id': ['S1', 'S2', 'S3', 'S4', 'S5'],
    'name': ['Fenton', 'Ryder', 'Bryce', 'Bernal', 'Morin'],
    'marks': [200, 210, 190, 222, 199]
})

df2 = pd.DataFrame({
    's_id': ['S4', 'S5', 'S6', 'S7', 'S8'],
    'name': ['Scarlette', 'Carla', 'Dante', 'Kaiser', 'Madeeha'],
    'marks': [201, 200, 198, 219, 201]
})

df3 = pd.DataFrame({
    's_id': ['S1', 'S2', 'S3', 'S4', 'S5', 'S7', 'S8', 'S9', 'S10', 'S11', 'S12', 'S13'],
    'ex_id': [23, 45, 12, 67, 21, 55, 33, 14, 56, 83, 88, 12]
})

print("Original DataFrames:")
print(df1)
print(df2)
print(df3)
# Concatenate df1 and df2 along rows
combined_df = pd.concat([df1, df2], ignore_index=False)
print()
print("Join first two said dataframes along rows:")
print(combined_df)

# Merge the combined dataframe with df3 on the 's_id' column
merged_df = pd.merge(combined_df, df3, on='s_id', how='inner')

# Print the final dataframe
print()
print("Now join the said result_data and df_exam_data along student_id:")
print(merged_df)


## Output
![Screenshot 2025-05-18 211621](https://github.com/user-attachments/assets/73cdf5ca-29eb-4be3-82c5-154fc6b16621)

## Result
The program joins the two student DataFrames row-wise and merges the result with exam data based on the student ID (s_id). It handles duplicate s_ids gracefully during merging.



