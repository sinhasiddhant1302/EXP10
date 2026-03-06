## **AIM**

To study and implement basic operations of **Pandas Series and DataFrame**, including creation, inspection of structure, indexing, updating, deletion, statistical analysis, and conditional filtering.

---

## **THEORY**

### **1. Importing Pandas Library**

`import pandas as pd`

* Imports the **Pandas library**.
* `pd` is an alias used to access Pandas functions conveniently.

---

### **2. Creating a Series**

`pd.Series([10,20,30,40])`

* A **Series** is a one-dimensional labeled array.
* It can store integers, floats, strings, etc.
* Automatically assigns index values starting from 0.

`print(s)`

* Displays the Series along with its index.

---

### **3. Creating a DataFrame**

`pd.DataFrame(data)`

* A **DataFrame** is a two-dimensional labeled data structure (rows and columns).
* Created using a dictionary where:

  * Keys → Column names
  * Values → List of column values

`print(df)`

* Displays the DataFrame in tabular form.

---

### **4. Inspecting DataFrame Structure**

`df.head()`

* prints first 5 rows.

`df.tail()`

* prints last 5 rows.

`df.shape`

* Returns a tuple representing **(number of rows, number of columns)**.

`df.ndim`

* Returns the number of dimensions.
* DataFrame has 2 dimensions.

`df.size`

* Returns total number of elements.
* Formula: rows × columns.

`df.columns`

* Returns the column labels of the DataFrame.

`df.dtypes`

* Displays the datatype of each column.

`df["Name"]`

* Accesses a specific column.
* Returns the column as a Series.

---

### **5. Indexing and Selecting Data**

`df.iloc[1]`

* `iloc` → Integer location-based indexing.
* Retrieves row at index position 1.

`df.loc[1,"Marks"]`

* `loc` → Label-based indexing.
* Accesses specific row and column using labels.

`df.iloc[0,1]`

* Accesses element using row index 0 and column index 1.

---

### **6. Adding a New Column**

`df["Grade"] = [...]`

* Adds a new column named "Grade".
* Assigns values corresponding to each row.

---

### **7. Updating Data**

`df.loc[1,"Marks"] = 88`

* Updates value using label-based indexing.

`df.iloc[0,1] = 91`

* Updates value using position-based indexing.

---

### **8. Deleting a Column**

`df.drop("Grade", axis=1)`

* Removes a column.
* `axis=1` specifies column deletion.
* Returns a new DataFrame (original remains unchanged unless reassigned).

---

### **9. Statistical Functions**

`df["Marks"].mean()`

* Calculates average value of the column.

`df["Marks"].min()`

* Returns minimum value.

`df["Marks"].max()`

* Returns maximum value.

These functions are used for basic statistical analysis.

---

### **10. Conditional Filtering**

`df[df["Marks"] > 80]`

* Applies condition on the DataFrame.
* Returns rows where Marks > 80.
* Used for filtering data based on criteria.

---

## ALGORITHM:

### 1. Add a New Column
Objective: Add a "Grade" column to the existing DataFrame based on predefined values.

* Step 1: Define a list of values representing the grades (e.g., ["First class", "Distinction", "Second Class"]).
* Step 2: Create a new column by referencing the DataFrame with the new column name (e.g., df["Grade"]).
* Step 3: Assign the list of values to this new column.
* Step 4: Display the updated DataFrame.

### 2. Update Data in DataFrame
Objective: Change a specific value in the DataFrame (e.g., updating Student A's marks to 81).

* Step 1: Locate the specific cell you want to modify. You can do this using label-based indexing (row index 0, column name "Marks") or integer-based indexing (row index 0, column index 1).
* Step 2: Reassign the new value (81) to that specific location using the assignment operator (=).
* Step 3: Display the updated DataFrame to verify the change.

### 3. Delete a Column
Objective: Remove the previously added "Grade" column.

* Step 1: Call the column drop function on the DataFrame.
* Step 2: Specify the name of the column to be removed ("Grade").
* Step 3: Specify the axis parameter as 1 to instruct the function to look for columns (rather than rows).
* Step 4: Store the output in a new DataFrame variable (e.g., df1) so the original DataFrame remains unchanged.
* Step 5: Display the newly created DataFrame.

### 4. Perform Basic Statistical Analysis (Mean)
Objective: Calculate the average marks of all students.

* Step 1: Access the specific column containing the numeric data (df["Marks"]).
* Step 2: Apply the built-in mean calculation function (.mean()) to that column.
* Step 3: Store the calculated value in a variable and display it.

### 5. Perform Basic Statistical Analysis (Max and Min)
Objective: Find the highest and lowest marks in the class.

* Step 1: Access the column containing the numeric data (df["Marks"]).
* Step 2: Apply the maximum value function (.max()) to the column and print the result.
* Step 3: Apply the minimum value function (.min()) to the same column and print the result.

### 6. Apply Condition (Filtering)
Objective: Display only the records of students who scored more than 80 marks.

* Step 1: Access the column you want to evaluate (df["Marks"]).
* Step 2: Create a conditional statement checking if the values in that column are strictly greater than 80 (> 80). This evaluates to a series of True/False (boolean) values for each row.
* Step 3: Pass this boolean series back into the DataFrame bracket notation (df[...]).
* Step 4: The DataFrame will filter and display only the rows where the condition evaluated to True.

---
## **CONCLUSION**

Thus, the experiment successfully demonstrates the creation and manipulation of **Pandas Series and DataFrame**. Various operations such as inspecting structure, accessing data using `loc` and `iloc`, adding and deleting columns, updating values, performing statistical analysis, and applying conditional filtering were implemented. These operations form the foundation of data handling and analysis in Python using Pandas.
